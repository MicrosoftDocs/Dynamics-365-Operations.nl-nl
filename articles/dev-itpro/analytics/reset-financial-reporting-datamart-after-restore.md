---
title: "De datamart voor financiële rapportage opnieuw instellen na het herstellen van een database"
description: "In dit onderwerp wordt beschreven hoe u de datamart voor financiële rapportage opnieuw instelt na het terugzetten van een Microsoft Dynamics 365 for Finance and Operations-database."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>De datamart voor financiële rapportage opnieuw instellen na het herstellen van een database

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u de datamart voor financiële rapportage opnieuw instelt na het terugzetten van een Microsoft Dynamics 365 for Finance and Operations-database.

Als u uw Finance and Operations-database vanaf een back-up moet terugzetten of de database uit een andere omgeving kopieert, moet u de stappen in dit onderwerp volgen om te zorgen dat de datamart voor financiële rapportage correct gebruikmaakt van de teruggezette Finance and Operations-database. 
> [!Note] 
> De stappen in dit proces worden ondersteund voor de release van mei 2016 van Dynamics 365 for Operations (App-build 7.0.1265.23014 en financiële rapportage-build 7.0.10000.4) en nieuwere versies. Als u een eerdere versie van Finance and Operations hebt, neem dan contact op met ons ondersteuningsteam voor hulp.

## <a name="export-report-definitions"></a>Rapportdefinities exporteren
Exporteer eerst de rapportontwerpen die zich in de Report Designer bevinden volgens de onderstaande procedure:

1.  Ga in Report Designer naar **Bedrijf** &gt; **Bouwsteengroepen**.
2.  Selecteer de bouwsteengroep die u wilt exporteren en klik op **Exporteren**. 

    > [!Note] 
    > Voor Finance and Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.
    
3.  Selecteer de rapportdefinities die u wilt exporteren:
    -   Om al uw rapportdefinities en de gekoppelde bouwstenen te exporteren klikt u op **Alles selecteren**.
    -   U kunt specifieke rapporten, rijen, kolommen, structuren of dimensiesets exporteren door op het gewenste tabblad te klikken en vervolgens de te exporteren items selecteren. Druk op Ctrl en houd deze toets ingedrukt om meerdere artikelen op een tabblad te selecteren. Wanneer u rapporten selecteert om te exporteren, worden de bijbehorende rijen, kolommen, structuren en dimensiegroepen ook geselecteerd.

4.  Klik op **Exporteren**.
5.  Voer een bestandsnaam in en selecteer de beveiligde locatie waar u de geëxporteerde rapportdefinities wilt opslaan.
6.  Klik op **Opslaan**.

U kunt het bestand kopiëren of uploaden naar een beveiligde locatie, zodat u het later kunt importeren in een andere omgeving. Informatie over het gebruik van een Microsoft Azure-opslagaccount vindt u in het onderwerp [Gegevensoverdracht met het opdrachtregelprogramma AzCopy](/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft biedt bij uw abonnement voor Finance and Operations geen opslagaccount aan. U moet een opslagaccount aanschaffen of een opslagaccount uit een separaat Azure-abonnement gebruiken. 
> [!WARNING]
> Houd rekening met het gedrag van het station D in virtuele Azure-machines. Bewaar uw geëxporteerde bouwsteengroepen hier niet permanent. Zie voor meer informatie over tijdelijke schijven het onderwerp [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Services afstoppen
Maak via Extern bureaublad verbinding met alle computers in de omgeving en stop de volgende Windows-services af door middel van services.msc:

-   World Wide Web Publishing-service (op alle AOS-computers)
-   Microsoft Dynamics 365 for Finance and Operations Batch Management-service (alleen op niet-privé AOS-computers)
-   Management Reporter 2012 Process Service (alleen op BI-computers)

Deze services hebben openstaande verbindingen met de Finance and Operations-database.

## <a name="reset"></a>Opnieuw instellen
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Zoek het meest recente pakket met MinorVersionDataUpgrade.zip en download het

Zoek het meest recente pakket MinorVersionDataUpgrade.zip met de aanwijzingen in het onderwerp [Downloaden van het meest recente bruikbare pakket met gegevensupgrade](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). De instructies geven aan hoe u de juiste versie van het gegevensupgradepakket voor uw omgeving vindt en downloadt. Een upgrade is niet vereist voor het downloaden van het pakket MinorVersionDataUpgrade.zip. U hoeft alleen de stappen in de sectie 'Downloaden van het meest recente bruikbare pakket met gegevensupgrade' uit te voeren zonder de overige stappen in het artikel voor het ophalen van een kopie van het pakket MinorVersionDataUpgrade.zip.

### <a name="execute-scripts-against-finance-and-operations-database"></a>Scripts uitvoeren op de Finance and Operations-database

Voer de volgende scripts uit op de Finance and Operations-database (niet op de database voor financiële rapportage).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Deze scripts zorgen ervoor dat de gebruikers, rollen en instellingen voor het bijhouden van wijzigingen juist zijn.

### <a name="execute-powershell-command-to-reset-database"></a>PowerShell-opdracht uitvoeren om de database opnieuw in te stellen

Voer op de AOS-computer als beheerder de volgende opdrachten in PowerShell uit om de integratie tussen Finance and Operations en de financiële rapportage opnieuw in te stellen:

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> Na uitvoering van de opdrachten wordt u gevraagd om 'J' in te voeren om te bevestigen.

Uitleg van parameters:

-   De geldige waarden voor -Reason zijn: SERVICING, BADDATA, OTHER.
-   Bij de parameter -ReasonDetail kunt u vrije tekst invoeren.
-   De waarden voor Reason en ReasonDetail worden vastgelegd in telemetrie/omgevingsbewaking.

## <a name="start-services"></a>Services opstarten
Start de services die u eerder hebt afgestopt opnieuw op door middel van services.msc:

-   World Wide Web Publishing-service (op alle AOS-computers)
-   Microsoft Dynamics 365 for Finance and Operations Batch Management-service (alleen op niet-privé AOS-computers)
-   Management Reporter 2012 Process Service (alleen op BI-computers)

## <a name="import-report-definitions"></a>Rapportdefinities importeren
Importeert uw rapportontwerpen vanuit de Report Designer, met behulp van het bestand dat bij het exporteren werd aangemaakt:

1.  Ga in Report Designer naar **Bedrijf** &gt; **Bouwsteengroepen**.
2.  Selecteer de bouwsteengroep die u wilt exporteren en klik op **Exporteren**. 

    > [!NOTE]
    > Voor Finance and Operations wordt slechts één bouwsteengroep ondersteund, namelijk **Standaard**.
    
3.  Selecteer de bouwsteen **Standaard** en klik op **Importeren**.
4.  Selecteer het bestand met de geëxporteerde rapportdefinities en klik op **Openen**.
5.  Selecteer in het dialoogvenster Importeren de te importeren rapportdefinities:
    -   Als u alle rapportdefinities en de ondersteunende bouwstenen wilt importeren, klikt u op **Alles selecteren**.
    -   Om specifieke rapporten, rijen, kolommen, structuren of dimensiesets te importeren, selecteert u de te importeren rapporten, rijen, kolommen, structuren of dimensiesets.

6.  Klik op **Importeren**.





