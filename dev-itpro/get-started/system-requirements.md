---
title: Systeemvereisten
description: In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Finance and Operations beschreven voor implementaties in de cloud en on-premises.
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: nl-nl
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Systeemvereisten

[!include[banner](../includes/banner.md)]


In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Finance and Operations beschreven, voor implementaties in de cloud en on-premises. Voordat u Finance and Operations installeert, controleert u indien van toepassing of het systeem waarmee u werkt, voldoet aan de minimale vereisten voor netwerk, hardware en software.


## <a name="supported-microsoft-office-applications"></a>Ondersteunde Microsoft Office-toepassingen
De volgende Office-toepassingen worden ondersteund in implementaties van Finance and Operations in de cloud en on-premises.
-   Als u de invoegtoepassingen voor Microsoft Word en Microsoft Excel wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd. Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Systeemvereisten die specifiek zijn voor implementaties in de cloud
## <a name="network-requirements"></a>Netwerkvereisten
-   Finance and Operations is ontworpen voor netwerken met een vertragingstijd van 250-300 milliseconden (ms) of minder. Dit is de latentie in een browserclient naar het Microsoft Azure-datacentrum waar Finance and Operations wordt gehost. Het wordt aangeraden om uw netwerklatentie te testen op <http://www.azurespeed.com>.
-   De bandbreedtevereisten voor Finance and Operations zijn afhankelijk van uw scenario. De meest voorkomende scenario's vereisen een bandbreedte van meer dan 50 kilobytes per seconde (kbps). Voor scenario's met hoge vereisten nettolading, zoals werkgebieden of scenario's voor uitgebreide aanpassingsmogelijkheden wordt meer bandbreedte aanbevolen.

Over het algemeen is Finance and Operations geoptimaliseerd voor het internet. Het aantal roundtrips vanuit een browserclient naar het Azure-datacentrum is erg klein en de gehele nettolading is gecomprimeerd. 

> [!WARNING]
> Bereken bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten. Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen. Gebruik voor klanten die zich zorgen maken over de bandbreedtevereisten, een evaluatieversie van Finance and Operations.

## <a name="net-framework-requirements"></a>.NET Framework-vereisten
Finance and Operations vereist .NET Framework versie 4.6.2 voor alle ClickOnce-toepassingen, zoals de documentrouterinsgagent. Zie voor de installatie-instructies [.NET Framework installeren](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Ondersteunde webbrowsers
De webtoepassing kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:


-   Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
-   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
-   Google Chrome (meest recente openbaar beschikbare release) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10-tablet
-   Apple Safari (meest recente openbaar beschikbare release) op Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) of Apple iPad

Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant. 

> [!NOTE]
> -   Een voorlopige versie van een Chrome-invoegtoepassing moet zijn geïnstalleerd om Taakrecorder schermopnamen te laten vastleggen en op te laten nemen in Microsoft Word-documenten. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   De workfloweditor wordt als ClickOnce-toepassing gestart. Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen. De ClickOnce-toepassing Workfloweditor vereist een compatibel 64-bits besturingssysteem.
> -   De Report Designer voor financiële rapportage wordt als ClickOnce-toepassing gestart. Hiervoor is een compatibel 64-bits besturingssysteem vereist. Als u Chrome gebruikt, moet u een ClickOnce-extensie installeren om de rapportontwerper-client te downloaden. Als u in de incognito modus van Chrome werkt, moet u ervoor zorgen dat de ClickOnce-extensie ook voor de incognito modus is ingeschakeld.
> -   Als u PDF-bestanden wilt bekijken, raden wij u aan moderne browsers te gebruiken, zoals Microsoft Edge (meest recente openbaar beschikbare versie) op Windows 10 of Google Chrome (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10 tablet.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Ondersteunde webbrowsers voor Retail Cloud POS

Retail Cloud POS kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:

-   Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
-   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
-   Chroom (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1 of Windows 7

## <a name="retail-modern-pos-requirements"></a>Vereisten voor Retail Modern POS
### <a name="supported-operating-systems"></a>Ondersteunde besturingssystemen

-   Retail Modern POS is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86- als ook x64-architectuur.
-   Retail Modern POS wordt alleen ondersteund op de Windows 10-versies Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten

-   De minimale ondersteunde resolutie is 1280 × 1024.
-   De computer waarop de Retail Modern POS wordt uitgevoerd, moet aan deze vereisten voldoen:
    -   Tenminste een dual core-processor, die wordt uitgevoerd met minstens 2 GHz.
    -   Tenminste 3 GB RAM.
    -   Internet-verbinding.

## <a name="retail-hardware-station-requirements"></a>Vereisten voor Retail Hardware Station
### <a name="supported-operating-systems"></a>Ondersteunde besturingssystemen

-   Retail Hardware Station is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86- als ook x64-architectuur.
-   Retail Hardware Station wordt ondersteund op de volgende besturingssystemen:
    -   De Windows 7-versies Professional, Enterprise en Ultimate 
    
    > [!NOTE]
    > Windows 7 wordt alleen ondersteund als Internet Explorer 11 handmatig op het systeem is geïnstalleerd.

    -   De Windows 8.1-versies Update 1 Professional, Enterprise en Embedded
    -   De Windows 10-versies Pro, Enterprise en Enterprise LTSB

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten

De computer moet voldoen aan alle systeemvereisten voor het installeren en gebruiken van de volgende opties:

-   Internet Information Services (IIS)
-   Hardware van derden

## <a name="retail-store-scale-unit-requirements"></a>Vereisten voor Retail Store Scale Unit
### <a name="supported-operating-systems"></a>Ondersteunde besturingssystemen

-   Retail Store Scale Unit is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86- als ook x64-architectuur.
-   Retail Store Scale Unit wordt ondersteund op de volgende besturingssystemen:
    -   De Windows 7-versies Professional, Enterprise en Ultimate
    -   De Windows 8.1-versies Update 1 Professional, Enterprise en Embedded
    -   De Windows 10-versies Pro, Enterprise en Enterprise LTSB

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten

-   4 GB RAM
-   1,6 GHz piekprocessorsnelheid per core (twee cores minimaal)
-   Ten minste 10 GB vrije ruimte (de afzetkanaaldatabase kan veel opslagruimte nodig hebben).

### <a name="recommended-system-requirements"></a>Aanbevolen systeemvereisten

-   6 GB RAM
-   2,4 GHz i7 (of equivalent) piekprocessorsnelheid per core (vier cores aanbevolen)
-   Ten minste 10 GB vrije ruimte (de afzetkanaaldatabase kan veel opslagruimte nodig hebben).

## <a name="connector-requirements"></a>Connectorvereisten
### <a name="supported-operating-systems"></a>Ondersteunde besturingssystemen

-   De connector voor Microsoft Dynamics AX heeft twee afzonderlijke installatieprogramma's, de **Async Server Connector-service** en de **Real-time service voor Dynamics AX 2012 R3**.
-   Beide componenten zijn 32-bits toepassingen, maar kunnen worden uitgevoerd op zowel x86- als ook x64-architectuur.
-   Beide onderdelen worden op de volgende besturingssystemen ondersteund:
    -   De Windows 7-versies Professional, Enterprise en Ultimate
    -   De Windows 8.1-versies Update 1 Professional, Enterprise en Embedded
    -   De Windows 10-versies Pro, Enterprise en Enterprise LTSB
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten

-   2 GB RAM, 4 GB RAM aanbevolen
-   1,6 GHz piekprocessorsnelheid per core (twee cores minimaal)
-   Ten minste 10 GB vrije ruimte (de afzetkanaaldatabase kan veel opslagruimte nodig hebben).

## <a name="requirements-for-development-on-local-vms"></a>Vereisten voor ontwikkeling op lokale VM's
Zie voor informatie over de vereisten voor de ontwikkeling op lokale virtuele machines (VM's) [VM on-premises uitvoeren](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Systeemvereisten voor on-premises implementaties

## <a name="network-requirements"></a>Netwerkvereisten
Finance and Operations (on-premises) werkt in netwerken die gebruikmaken van Internet Protocol versie 4 (IPv4) of Internet Protocol versie 6 (IPv6). Houd rekening met de netwerkomgeving bij het plannen van uw systeem en houd u aan de volgende richtlijnen.

### <a name="network-response-time"></a>Netwerkresponstijd
In de volgende tabel staan de minimale netwerkvereisten voor de verbinding tussen de webbrowser en de Application Object Server (AOS), en voor de verbinding tussen de AOS en de database in een on-premises systeem.

| Waarde     | Webbrowser met AOS | AOS met database                                            |
|-----------|--------------------|------------------------------------------------------------|
| Bandbreedte | 50 KBps per gebruiker   | 100 MBps                                                   |
| Vertragingstijd   | < 250-300 ms       | < 1 ms (alleen LAN). AOS en database moeten zich op dezelfde locatie bevinden. |

- Finance and Operations (on-premises) is ontworpen voor netwerken met een vertragingstijd van 250-300 milliseconden (ms) of minder. Dit is de vertragingstijd van een browserclient naar het datacentrum waar Finance and Operations wordt gehost.
- De bandbreedtevereisten voor Finance and Operations (on-premises) zijn afhankelijk van uw scenario. Typische scenario's vereisen een bandbreedte van meer dan 50 kB per seconde (KBps) tussen de browser en de Finance and Operations-server. Voor scenario's met hoge vereisten voor nettolading, zoals werkruimten of scenario's voor uitgebreide aanpassingsmogelijkheden, wordt afhankelijk van het gebruik een hogere bandbreedte aanbevolen.
Implementaties waarbij de AOS en de SQL Server-Database zich in verschillende datacenters worden niet ondersteund. De AOS en de SQL Server-database moeten zich op dezelfde locatie bevinden. Over het algemeen is Finance and Operations geoptimaliseerd voor het verminderen van het aantal roundtrips van browser naar server. Het aantal roundtrips vanuit een browserclient naar het datacentrum is nul of één voor elke gebruikersinteractie en de nettolading is gecomprimeerd.

> [!WARNING]
> Bereken de bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten. Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen. Het is raadzaam om met een real-life simulatie in een niet-productieomgeving van Finance and Operations de beste prestaties te meten voor uw specifieke geval. 

### <a name="lan-environments"></a>LAN-omgevingen
In lokale netwerkomgevingen (LAN) is Microsoft Extern bureaublad in Microsoft Windows Server niet vereist voor de verbinding met Finance and Operations. Het kan echter zijn vereist voor het afhandelen van bewerkingen op de VM's waaruit de serverimplementaties bestaan.

### <a name="wan-environments"></a>WAN-omgevingen
In WAN-netwerkomgevingen is Extern bureaublad in Windows Server niet vereist voor de verbinding met Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Vereisten voor internetverbinding
Finance and Operations (on-premises) vereist geen internetverbinding van de werkstations van de eindgebruikers. Sommige functies zullen echter niet beschikbaar zijn zonder internetverbinding.

| Browserclient | Een intranetscenario zonder internetverbinding is een ontwerppunt voor de on-premises implementatie-optie. Sommige functies die cloudservices vereisen, zijn niet beschikbaar, zoals Help en taakbegeleiderbibliotheken in LCS. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server         | De AOS- of Service Fabric-laag moet kunnen communiceren met LCS. De on-premises browserclient vereist geen toegang tot internet.                                                                                |
| Telemetrie      | Telemetriegegevens gaan mogelijk verloren bij lange onderbrekingen in de connectiviteit. Onderbrekingen in de verbinding met LCS hebben geen invloed op de functionaliteit van de on-premises toepassing.                                                |
| LCS            | Verbinding met LCS is vereist voor implementatie, code-implementatie en onderhoudsactiviteiten.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetriegegevens overbrengen naar de cloud
De meeste telemetrie wordt lokaal opgeslagen en kan worden geopend met Logboeken in Microsoft Windows. Een kleine deel van de telemetriegebeurtenissen wordt overgebracht naar de Microsoft-telemetriepijplijn in de cloud voor diagnose. Klantgegevens en identificeerbare eindgebruikergegevens maken geen deel uit van de telemetrie die naar Microsoft wordt verzonden. VM-namen worden naar Microsoft verzonden als ondersteuning bij omgevingsbeheer en diagnose van het LCS-portal.

## <a name="domain-requirements"></a>Domeinvereisten
Houd rekening met de volgende domeinvereisten bij de installatie van Finance and Operations (on-premises):

- Virtuele machines die als host fungeren voor onderdelen van Finance and Operations (on-premises), moeten behoren bij een Active Directory-domein. Active Directory Domain Services (AD DS) moet worden geconfigureerd in de native modus.
- Voor virtuele machines waarop onderdelen van Finance and Operations (on-premises) worden uitgevoerd, moet toegang tot elkaar zijn geconfigureerd in Active Directory Domain Services. 
- De domeincontroller moet worden uitgevoerd op Microsoft Windows Server 2016.

## <a name="hardware-requirements"></a>Hardwarevereisten
In deze sectie wordt de hardware beschreven die is vereist voor het uitvoeren van Finance and Operations (on-premises).
De werkelijke hardwarevereisten zullen verschillen op basis van de systeemconfiguratie, de gegevenssamenstelling en de toepassingen en functies die u wilt gebruiken. Dit zijn enkele factoren die van invloed zijn op de keuze van de juiste hardware voor Finance and Operations (on-premises):

- Het aantal transacties per uur.
- Het aantal gelijktijdige gebruikers.

## <a name="minimum-infrastructure-requirements"></a>Minimale vereisten voor de infrastructuur
Finance and Operations (on-premises) maakt gebruik van Microsoft Azure Service Fabric als host voor AOS, batch- en gegevensbeheer, Management reporter en orchestratorservices voor de omgeving. Microsoft SQL Server Reporting Services (SSRS) wordt niet gehost in het Service Fabric-cluster.
SQL Server moet worden ingesteld in een HADRON-installatie voor hoge beschikbaarheid met ten minste twee knooppunten voor de productie.
In de volgende afbeelding wordt het aanbevolen minimumaantal knooppunten aangegeven in het Service Fabric-cluster.

[![Aanbevolen aantal knooppunten voor Service Fabric-cluster](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Processor en RAM-vereisten
De volgende tabel bevat het aantal processors en de hoeveelheid RAM-geheugen die vereist zijn voor elk van de functies voor het uitvoeren van deze implementatieoptie. Lees voor meer informatie de aanbeveling voor de minimumvereisten voor het zelfstandige Service Fabric-cluster [Service Fabric-cluster plannen en voorbereiden](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Als andere Microsoft-software wordt geïnstalleerd op dezelfde computer, moet het systeem ook voldoen aan de hardwarevereisten voor die software. Het is raadzaam om andere servertoepassingen op dezelfde computer als AOS te beperken tot 1 gigabyte (GB) RAM.

**Omvang per functie en topologietype**

| Topologie   | Functie (knooppunttype)              | Aanbevolen processorcores | Aanbevolen geheugen (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Productie | AOS, Gegevensbeheer, Batch   | 8                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |
| Sandbox    | AOS, Gegevensbeheer, Batch   | 4                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |

**Minimale grootte van ramingen voor de productie en de sandbox-implementaties**\*

| Topologie                                  | Rol                          | Aantal exemplaren |
|-------------------------------------------|-------------------------------|---------------------|
| Productie                                | AOS (Gegevensbeheer, Batch)  | 3                   |
|                                           | Management Reporter           | 2                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator\*\*                | 3                   |
| Sandbox                                   | AOS, Gegevensbeheer, Batch   | 2                   |
|                                           | Management Reporter           | 1                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator                  | 3                   |
| *Overzicht productie en de sandbox-topologieën* |                               | 16                  |

\*Deze aantallen worden gevalideerd door onze testklanten en zullen zo nodig worden gewijzigd op basis van deze feedback.

\*\*Orchestrator wordt aangewezen als het primaire knooppunttype en wordt ook gebruikt voor het uitvoeren van de Service Fabric-services.

**Aanvankelijke schattingen voor backend SQL Server en AD**

[![Aanvankelijke schattingen voor backend SQL Server en AD](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*De omvang van de SQL Server is sterk afhankelijk van de werkbelasting. Zie voor meer informatie de sectie [Grootte van de hardware voor on-premises omgevingen vaststellen](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Opslag

- **AOS**: Finance and Operations (on-premises) gebruikt een SMB 3.0-share (Server Message Block) voor het opslaan van niet-gestructureerde gegevens. Zie voor meer informatie [Opslagruimte in Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL**: mogelijke opties:
    - De installatie van een SSD (Solid-State Drive) met hoge beschikbaarheid.
    - Een SAN-netwerk (Storage Area Network) dat is geoptimaliseerd voor OLTP-doorvoercapaciteit.
    - Krachtige Direct-attached storage (DAS) 
- **IOPs voor SQL en gegevensbeheer**: de opslag voor gegevensbeheer en SQL Server moet ten minste 2000 invoer/uitvoer-bewerkingen per seconde (IOPs) hebben. Productie-IOPS is afhankelijk van veel factoren. Zie voor meer informatie de sectie Grootte van de hardware voor on-premises omgevingen vaststellen. 
- **IOPS Virtuele Machine**: elke virtuele machine moet ten minste 100 schrijfbewerkingen per seconde hebben.

## <a name="virtual-host-requirements"></a>Vereisten voor virtuele host
Hanteer de volgende richtlijnen bij het installeren van de virtuele hosts voor een Finance and Operations-omgeving (on-premises): [Service Fabric-cluster plannen en voorbereiden](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) en [Service Fabric-cluster beschrijven](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Elke virtuele host moet beschikken over voldoende cores voor de infrastructuur waarvoor het formaat wordt vastgesteld. Er zijn meerdere geavanceerde configuraties mogelijk, als SQL Server zich op fysieke hardware bevindt maar alle andere onderdelen gevirtualiseerd zijn. Als SQL Server is gevirtualiseerd, moet het schijfsubsysteem een snelle SAN of het equivalent daarvan zijn. In alle gevallen moet de basisinstallatie voor de virtuele host een hoge beschikbaarheid hebben en redundant zijn. Wanneer virtualisatie wordt gebruikt, moeten nooit VM-momentopnamen worden gemaakt.

## <a name="software-requirements-for-all-server-computers"></a>Softwarevereisten voor alle servercomputers
De volgende software moet aanwezig zijn op een computer voordat onderdelen voor Finance and Operations (on-premises) kunnen worden geïnstalleerd:

- Microsoft .NET Framework 4.5.1 of hoger
- Voor meer informatie over Service Fabric zie [Service Fabric-cluster plannen en voorbereiden](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Ondersteunde serverbesturingssystemen
De volgende tabel geeft een overzicht van de serverbesturingssystemen die worden ondersteund voor onderdelen van Finance and Operations.

| Besturingssysteem                                     | Opmerkingen                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter of Standard | Deze vereisten gelden voor de database en het Service Fabric-cluster dat als host fungeert voor AOS. |

## <a name="software-requirements-for-database-servers"></a>Softwarevereisten voor alle databaseservers

- Alleen 64-bits versies van SQL Server 2016 worden ondersteund.
- We raden aan om de meest recente cumulatieve update (CU) voor de gebruikte versie van SQL Server te installeren in een productieomgeving.
- Finance and Operations (on-premises) ondersteunt Unicode-sorteringen die niet hoofdlettergevoelig, accentgevoelig, kana-gevoelig en breedtegevoelig zijn. De sortering moet overeenkomen met de Windows-landinstellingen van de computers waarop AOS-exemplaren worden uitgevoerd. Als u een nieuwe installatie instelt, is het raadzaam dat u een Windows-sortering selecteert in plaats van een SQL Server-sortering. Zie voor meer informatie over het selecteren van een sortering voor een SQL Server-database de [documentatie bij SQL Server](/sql/sql-server/sql-server-technical-documentation).
De volgende tabel geeft een overzicht van de SQL Server-versies die worden ondersteund voor databases van Finance and Operations. Zie voor meer informatie de minimumvereisten voor hardware van [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Behoefte                                                      | Opmerkingen                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition of Enterprise Edition | Zie voor de hardwarevereisten voor SQL Server 2016 [Hardware- en softwarevereisten voor het installeren van SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Softwarevereisten voor clientcomputers
De webtoepassing Finance and Operations werkt op elk apparaat met een HTML5.0-compatibele webbrowser. Specifieke apparaat-/browsercombinaties die door Microsoft zijn bevestigd, omvatten:

- Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
- Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
- Google Chrome (meest recente openbaar beschikbare release) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10-tablet
- Apple Safari (meest recente openbaar beschikbare release) op Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) of Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Softwarevereisten voor Active Directory Federation Services 
Active Directory Federation Services (AD FS) op Windows Server 2016

De domeincontroller moet Windows Server 2012 R2 of hoger zijn met een domeinfunctionaliteitsniveau van 2012 R2 of hoger

Voor meer informatie over niveaus voor domeinfunctionaliteit zie: 
- [Wat zijn functionele niveaus in Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Inzicht in functionele niveaus voor Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Hardware- en softwarevereisten voor Retail-onderdelen
Finance and Operations (on-premises) bevat op dit moment geen Retail-onderdelen.

<a name="see-also"></a>Zie ook
--------

[Een evaluatie-exemplaar van Dynamics 365 for Finance and Operations, Enterprise-editie krijgen](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

