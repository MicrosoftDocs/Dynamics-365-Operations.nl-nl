---
title: Gegevensupgrade in sandboxomgeving
description: In dit onderwerp wordt uitgelegd hoe u een gegevensupgrade uitvoert van AX 2012 naar Dynamics 365 for Finance and Operations in een sandboxomgeving.
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: nl-nl
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>Gegevensupgrade in sandboxomgeving

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

De uitvoer van deze taak is een bijgewerkte database, die u in een sandboxomgeving gebruiken kunt. Een sandboxomgeving is een omgeving waar zakelijke gebruikers en functionele teamleden toepassingsfunctionaliteit kunnen valideren. Deze functionaliteit omvat aanpassingen en de gegevens die vanuit Microsoft Dynamics AX 2012 is overgebracht.

Het wordt aangeraden dat u de gegevensupgrade in een ontwikkelomgeving uitvoert, voordat u deze in een gedeelde sandboxomgeving uitvoert. Deze aanpak helpt de totale tijd te reduceren die nodig is voor een geslaagde gegevensupgrade. Zie voor meer informatie [Gegevensupgrade in een ontwikkelomgeving](prepare-data-upgrade.md).

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>Overzicht van het upgradeproces voor sandboxgegevens

Voordat u gegevens bijwerkt in een sandboxomgeving, hebt u al gegevens geüpgraded in een ontwikkelomgeving, zoals beschreven in [Gegevensupgrade in een ontwikkelomgeving](prepare-data-upgrade.md). De twee processen lijken sterk op elkaar. Het belangrijkste verschil is dat een sandboxomgeving een Microsoft Azure SQL-database voor gegevensopslag gebruikt, terwijl een ontwikkelomgeving gebruikmaakt van Microsoft SQL Server. Dit technische verschil in de databaselaag vereist dat u de gegevensupgradeprocedure in een sandboxomgeving iets aanpast, omdat een back-up van het AX 2012-database-exemplaar niet zomaar kan worden hersteld naar SQL Database.

![Upgradeprocess voor sandboxgegevens](./media/data-upgrade-sandbox.png)

Hier vindt u de high-level stappen in het upgradeproces.

1. Maak een kopie van de AX 2012-database. Het wordt aangeraden een kopie te gebruiken, omdat u bepaalde objecten moet verwijderen in de kopie die u wilt exporteren.
2. Exporteer de gekopieerde database naar een bacpac-bestand door middel van SQLPackage.exe, een gratis SQL Server-hulpprogramma. Dit hulpprogramma biedt een speciaal soort databaseback-up die kan worden geïmporteerd in SQL Database.
3. Upload het bacpac-bestand naar de Azure-opslag.
4. Download het bacpac-bestand naar de AOS-machine (Application Object Server) in de sandboxomgeving en importeer het daarna door middel van SQLPackage.exe. Voer vervolgens een script uit op de geïmporteerde database om de SQL-database-gebruikers opnieuw in te stellen.
5. Voer het pakket MajorVersionDataUpgrade.zip uit om de gegevensupgrade op de geïmporteerde database uit te voeren.

## <a name="create-a-copy-of-the-ax-2012-database"></a>Een kopie van de AX 2012-database maken

U moet een kopie van de AX 2012-database maken die u wilt upgraden, omdat u een aantal objecten uit de database verwijderen moet. Deze objecten bevatten alle gebruikers van Microsoft Windows-verificatie. Deze wijzigingen maken de gewijzigde database onbruikbaar voor AX 2012. Tijdens deze stap maakt u een kopie van de database en verwijdert u deze objecten.

Deze stap moet worden uitgevoerd door de databasebeheerder (DBA) of een persoon met soortgelijke kennis en ervaring.

Om een databasekopie te maken, maakt u een back-up van de oorspronkelijke database die u dan weer herstelt met een nieuwe naam. Let erop dat er voldoende ruimte beschikbaar voor beide databases is. U kunt de kopie ook op een andere server maken. Het maakt niet uit welke versie van SQL Server de database uitvoert.

Hier volgt een voorbeeld van de code waarmee u een databasekopie maakt. U moet dit voorbeeld aanpassen om uw eigen databasenamen in te voegen.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Nadat de kopie is gemaakt, kunt u het volgende T-SQL-script hierop uitvoeren.
Taaklijst 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>De gekopieerde database exporteren naar een bacpac-bestand

Exporteer de gekopieerde database naar een bacpac-bestand door middel van de tool SQLPackage.exe. Deze stap moet uitgevoerd worden door de DBA of een teamlid met vergelijkbare kennis.

Het is belangrijk dat u de meest recente versie van SQL Server Management Studio installeert voordat u deze stap start. Hoewel SQLPackage aanwezig is in eerdere versies van Management Studio is, werkt het niet correct voor deze stap tenzij u eerst de meest recente versie installeert.

Deze stap is belangrijk, omdat de export opnieuw moet worden uitgevoerd tijdens de downtime vóór de go-live. Hieronder vindt u enkele tips:

- Het bacpac-proces vraagt veel I/O en CPU-vermogen. Voer daarom de export uit op een krachtige computer.
- SQLPackage moet lokaal worden uitgevoerd op de computer waarop de database wordt gehost. Voer SQLPackage niet uit op een lokale laptop die verbinding heeft met de databasecomputer, omdat dit proces ook veel netwerkverkeer genereert.

Open vervolgens het venster **Opdrachtprompt** in de beheerdersmodus en voer de volgende opdrachten uit.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Hier volgt een uitleg van de parameters:

- **ssn** (source server name, bronservernaam): de naam van de SQL Server van waaruit u wilt exporteren. Voor dit proces moet deze parameter altijd zijn ingesteld op **localhost**.
- **sdn** (source database name, bronddatabasenaam): de naam van de te exporteren database.
- **tf** (target file, doelbestand): het pad en de naam van het bestand waarnaar u wilt exporteren. De map moet al bestaan, maar het bestand wordt gemaakt door het proces.
- **/p:CommandTimeout**: de time-outwaarde voor elke afzonderlijke query. Met deze parameter kunt u grotere tabellen exporteren zonder in een time-out te lopen.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Het bacpac-bestand uploaden naar Azure-opslag

Upload uw bacpac-bestand naar de Azure-opslag. Zie UsingStorageExplorer.docx Taaklijst

### <a name="import-the-bacpac-file-into-sql-database"></a>Het bacpac-bestand in SQL-database importeren

Tijdens deze stap, importeert u het geëxporteerde bacpac-bestand in het SQL Database-exemplaar dat uw sandboxomgeving gebruikt. U moet eerst de meest recente versie van Management Studio op de sandbox-AOS-computer installeren. U importeert het bestand vervolgens met het hulpprogramma SQLPackage.exe.

U voert deze taken rechtstreeks uit op de AOS-computer in uw sandboxomgeving, omdat er firewall-regels zijn die de toegang tot het SQL Database-exemplaar beperken. Als u echter de AOS-machine gebruikt, hebt u wel toegang.

Net als bij de exportstap moet de nieuwste versie van Management Studio zijn geïnstalleerd voordat u het importeren start. Deze stap werkt niet als u een oudere versie hebt.

Voor betere prestaties wordt aangeraden om het bacpac-bestand te plaatsen op station D op de AOS-computer. Station D op een Azure-VM is een fysieke schijf die doorgaans betere prestaties levert dan andere beschikbare schijven.

Open het venster **Opdrachtprompt** in de beheerdersmodus en voer de volgende opdrachten uit.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Hier volgt een uitleg van de parameters:

- **tsn** (target server name, doelservernaam): de naam van de SQL Azure-server waarin u wilt importeren. U vindt de naam in LCS. Voeg hieraan het achtervoegsel **.database.windows.net** toe.
- **tdn** (target database name, doeldatabasenaam): de naam van de database waarin u de gegevens wilt importeren. De database mag nog niet bestaan. Het importproces maakt een nieuwe database aan.
- **sf** (source file, bronbestand): de pad en het naam van waaruit u de gegevens importeert.
- **tp** (target password, wachtwoord doel-db): het SQL-wachtwoord voor het doelexemplaar van SQL Database.
- **tu** (target user, gebruiker doel-db): de SQL-gebruikersnaam voor het doelexemplaar van SQL Database. Het wordt aangeraden om **sqladmin** te gebruiken. U kunt het wachtwoord voor deze gebruiker ophalen uit uw LCS-project.
- **/p:CommandTimeout**: de time-outwaarde voor elke afzonderlijke query. Met deze parameter kunt u grotere tabellen exporteren zonder in een time-out te lopen.
- **/p:DatabaseServiceObjective**: het serviceniveau van de gemaakte database. U kunt de waarde voor de bestaande database controleren door middel van Management Studio. Klik met de rechtermuisknop op de database en selecteer **Eigenschappen**.

Nadat u de opdrachten hebt uitgevoerd, ontvangt u de volgende waarschuwing. U kunt deze gewoon negeren.

![Sandbox-fout](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>Het pakket MajorVersionDataUpgrade.zip uitvoeren

Voer het implementatiepakket voor gegevensupgrade uit volgens de beschrijving in [Gegevens upgraden in ontwikkel-, demo- of sandboxomgevingen](upgrade-data-to-latest-update.md).

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>Een kopie van de database in een ontwikkelomgeving upgraden

Het is nuttig om een kopie van dezelfde database in een ontwikkelomgeving te upgraden. Als u een kopie van de database hebt voor ontwikkelomgevingen, is het veel eenvoudiger om fouten te onderzoeken die zijn gevonden in de bijgewerkte sandboxomgeving.

