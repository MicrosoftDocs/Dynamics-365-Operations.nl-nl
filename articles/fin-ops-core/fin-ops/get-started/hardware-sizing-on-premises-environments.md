---
title: Vereisten vaststellen voor grootte van de hardware voor on-premises omgevingen
description: Vereisten vaststellen voor grootte van de hardware voor on-premises omgevingen
author: sericks007
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 443b80e44a90a68610fbb2bb5a5f4b6b7d545fa7ad772edb3672972fa82f8cbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763429"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>Vereisten vaststellen voor grootte van de hardware voor on-premises omgevingen

[!include [banner](../includes/banner.md)]

Voordat u de omvang gaat bepalen van de hardware en de infrastructuur van een on-premises omgeving, dient u vertrouwd zijn met de [systeemvereisten voor cloudimplementaties](system-requirements.md) en [instructies voor installatie en implementatie](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) om een goed begrip te krijgen van de onderliggende infrastructuur.

> [!NOTE]
> Let goed op de aanbevolen procedures voor de systeeminstellingen voor optimale prestaties.

Nadat u de documentatie hebt bekeken, kunt u gaan inschatten hoeveel transactionele en gelijktijdige gebruikers er zijn en welke omvang uw omgeving moet hebben op basis van de gemiddelde coredoorvoer.

## <a name="factors-that-affect-sizing"></a>Factoren die invloed hebben op de grootte

Alle factoren in de volgende afbeelding zijn bepalend voor de grootte. Hoe meer gedetailleerde informatie u verzamelt, hoe preciezer u de grootte kunt bepalen. Zonder ondersteunende gegevens kunt u de omvang van de hardware niet inschatten. De absolute minimumvereiste voor de benodigde gegevens is de piekbelasting voor de transactieregels per uur.

[![Grootte van de hardware voor on-premises omgevingen vaststellen.](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Van links naar rechts gezien, is de eerste en de belangrijkste factor voor het nauwkeurig schatten een transactieprofiel of een karakterisering van de transacties. Het is van groot belang dat u altijd het transactionele piekvolume per uur weet. Als er meerdere piekuren zijn, moeten deze perioden correct zijn gedefinieerd.

Als u weet wat de belasting is van uw infrastructuur, moet u ook meer details weten van deze factoren:

- **Transacties**: transacties hebben doorgaans bepaalde pieken in de dag/week. Dit is meestal afhankelijk van het transactietype. Tijd- en onkostengegevens hebben meestal eenmaal per week een piek, terwijl verkoopordergegevens vaak in bulk binnenkomen via integratie of binnendruppelen gedurende de dag.
- **Aantal gelijktijdige gebruikers**: het aantal gelijktijdige gebruikers is de tweede belangrijkste factor voor de grootte. U kunt geen betrouwbare ramingen krijgen op basis van het aantal gelijktijdige gebruikers, dus als dit de enige gegevens zijn waarover u beschikt, schat u het aantal bij benadering en past u dit aan als u meer gegevens hebt. Een nauwkeurige definitie van het aantal gelijktijdige gebruikers houdt in:

    - Benoemde gebruikers zijn geen gelijktijdige gebruikers.
    - Gelijktijdige gebruikers zijn altijd een subset van de benoemde gebruikers. 
    - Maximale werkbelasting bepaalt de maximale gelijktijdigheid voor grootte.

    Criteria voor gelijktijdige gebruikers zijn dat de gebruiker voldoet aan de volgende criteria:

    - Heeft zich aangemeld.
    - Verwerkt transacties/query's op het moment van de telling.
    - Is geen niet-actieve sessie.

- **Gegevenssamenstelling**: dit betreft vooral hoe uw systeem wordt ingesteld en geconfigureerd. Bijvoorbeeld hoeveel rechtspersonen u hebt, hoeveel artikelen, het aantal stuklijstniveaus en de complexiteit van de beveiligingsinstellingen. Elk van deze factoren kan een kleine invloed hebben op prestaties, zodat deze factoren kunnen worden verrekend met behulp van slimme keuzes wanneer het gaat om de infrastructuur.
- **Uitbreidingen**: aanpassingen kunnen eenvoudig of complex zijn. Het aantal aanpassingen en de aard van de complexiteit en het gebruik heeft een uiteenlopende invloed op de omvang van de benodigde infrastructuur. Voor complexe aanpassingen wordt het aanbevolen om de werking te evalueren om te zorgen dat ze niet alleen worden getest op efficiëntie, maar ook op inzicht in wat nodig is voor de infrastructuur. Dit is nog belangrijker wanneer de uitbreidingen niet zijn gecodeerd volgens de beste methoden voor prestaties en schaalbaarheid.
- **Rapportage en analyse**: hiervoor moeten normaal gesproken zware query's worden uitgevoerd op de verschillende databases in het databasesysteem. Begrip en vermindering van de frequentie voor het uitvoeren van dure rapporten geeft meer inzicht in de gevolgen.
- **Oplossingen van andere leveranciers**: deze oplossingen, zoals ISV's, hebben dezelfde implicaties en aanbevelingen als uitbreidingen.

## <a name="sizing-your-environment"></a>De grootte van uw omgeving wijzigen

Als u inzicht wilt krijgen in welke omvang nodig is, moet u het piekvolume weten van de transacties die moeten worden verwerkt. Aanvullende systemen, zoals Management Reporter of SQL Server Reporting Services, zijn meestal minder bedrijfskritiek. Daarom richt dit document zich voornamelijk op de AOS en SQL Server.

> [!NOTE]
> Gewoonlijk worden de berekeningsniveaus schaalbaar uitgebreid en ingesteld als N+1. Als u dus een schatting maakt voor drie AOS, voegt u een vierde AOS toe. De databaselaag moet worden ingesteld als maximaal beschikbaar en Always On.

## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Grootte

- 3K tot 15K transactieregels per uur per core op de databaseserver.
- Normale verhouding van AOS-SQL-core 3:1 voor de primaire SQL-Server. Extra cores zijn vereist op basis van de gekozen configuratie voor hoge beschikbaarheid.

    - Door zware databasebewerkingen kan dit veranderen in 2:1.

- De volgende factoren beïnvloeden variaties:

    - Gebruikte parameterinstellingen.
    - Uitbreidingsniveaus.
    - Gebruik van aanvullende functionaliteit, zoals databaselogboeken en waarschuwingen. Door extreem gebruik van databaselogboeken daalt de doorvoer per uur per core onder 3K regels.
    - Complexiteit van de gegevenssamenstelling: een eenvoudig rekeningschema versus een gedetailleerd en specifiek rekeningschema heeft gevolgen voor de doorvoer (bijvoorbeeld).
    - Kenmerken van de transacties.
    - 2 GB tot 16 GB geheugen voor elke core.
    - Aanvullende databases op een databaseserver zoals Management Reporter en SSRS-databases.
    - Tijdelijke DB = 15% van de DB-omvang met evenveel bestanden als fysieke processors.
    - SAN-grootte en doorvoer op basis van het totale gelijktijdige transactievolume/gebruik.

### <a name="high-availability"></a>Hoge beschikbaarheid

Wij raden altijd aan om SQL Server te gebruiken voor cluster- of mirror-instellingen. Het tweede SQL-knooppunt moet hetzelfde aantal cores hebben als het primaire knooppunt.

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory Federation Services (AD FS)

Voor de omvang van AD FS raadpleegt u [de documentatie over de capaciteit van de AD FS-server](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Er is een [werkblad met de grootte](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) beschikbaar voor het plannen van het aantal exemplaren in uw implementatie.

## <a name="aos-online-and-batch"></a>AOS (online en batch)

### <a name="sizing"></a>Grootte

- Grootte op transactie volume/gebruik

    - 2K tot 6K regels per core
    - 16 GB per exemplaar
    - Standaard: 4 tot 24 cores
    - 10 tot 15 Enterprise-gebruikers per core
    - 15 tot 25 activiteitgebruikers per core
    - 25 tot 50 teamleden per core

- Batch

    - 1 tot 4 batchthreads per core
    - Grootte op basis van de kenmerken van het batchvenster

- Houd er rekening mee dat AOS, Gegevensbeheer en Batch dezelfde rol hebben in de Service Fabric. Gebruik een gecombineerde omvang voor deze drie werkbelastingen en niet afzonderlijk zoals in Microsoft Dynamics AX 2012.
- Dezelfde variabele factoren voor SQL Server zijn hier van toepassing.

### <a name="high-availability"></a>Hoge beschikbaarheid

- Zorg ervoor dat er minimaal 1 tot 2 meer AOS beschikbaar zijn dan de schatting.
- Zorg ervoor dat er ten minste 3 tot 4 virtuele hosts beschikbaar zijn.

## <a name="management-reporter"></a>Management Reporter

In de meeste gevallen, tenzij bij intensief gebruik, zijn de aanbevolen minimale eisen met twee knooppunten voldoende. Alleen in gevallen met intensief gebruik moet u meer dan twee knooppunten hebben. Breid dit naar behoeven uit.

## <a name="sql-server-reporting-services"></a>SQL Server Reporting Services

Voor de algemene beschikbaarheid hoeft slechts één SSRS-knooppunt te worden geïmplementeerd. Controleer SSRS-knooppunt bij het testen en verhoog het aantal beschikbare cores voor SSRS op basis van de behoefte. Zorg ervoor dat er een vooraf geconfigureerd secundair knooppunt beschikbaar is op een virtuele host die verschilt van de SSRS VM. Dit is belangrijk als er een probleem is met de virtuele machine die als host fungeert voor SSRS of met de virtuele host. Als dit het geval is, moeten ze worden vervangen.

Vanaf versie 10.0.17 kunt u extra SSRS-knooppunten configureren om een hoge beschikbaarheid te bereiken. Zie [Hoge beschikbaarheid configureren voor SSRS-knooppunten (SQL Server Reporting Services)](../../dev-itpro/deployment/onprem-ssrsha.md).

## <a name="environment-orchestrator"></a>Orchestrator-omgeving

De Orchestrator-service beheert uw implementatie en de gerelateerde communicatie met LCS. Deze service wordt geïmplementeerd als de primaire Service Fabric-service en vereist ten minste drie VM's. Deze service bevindt zich op dezelfde locatie als de Service Fabric-configuratieservices. De omvang moet voldoen aan de piekbelasting van het cluster. Zie voor meer informatie [Implementatie van Service Fabric-cluster plannen en voorbereiden](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="virtualization-and-oversubscription"></a>Virtualisering en te veel abonnementen

Bedrijfskritieke services, zoals de AOS, moeten worden gehost op virtuele hosts met eigen resources: cores, geheugen en schijfruimte.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
