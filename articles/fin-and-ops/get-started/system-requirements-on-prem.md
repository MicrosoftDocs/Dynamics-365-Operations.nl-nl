---
title: Systeemvereisten voor on-premises implementaties
description: In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition beschreven voor implementaties on-premises.
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 25a6f326c57e84d6a7c356ac5407be7ed3095f83
ms.openlocfilehash: 5edc6f0b2240e9dd2d3b72a13f35e96f016aa013
ms.contentlocale: nl-nl
ms.lasthandoff: 10/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Systeemvereisten voor on-premises implementaties

[!include[banner](../includes/banner.md)]

In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition beschreven voor implementaties on-premises. Voordat u Finance and Operations installeert, controleert u indien deze stap van toepassing is, of het systeem waarmee u werkt, voldoet aan de minimale vereisten voor netwerk, hardware en software.

## <a name="network-requirements"></a>Netwerkvereisten
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) kan werken in netwerken die gebruikmaken van Internet Protocol versie 4 (IPv4) of Internet Protocol versie 6 (IPv6). Houd rekening met de netwerkomgeving bij het plannen van uw systeem en houd u aan de volgende richtlijnen.

### <a name="network-response-time"></a>Netwerkresponstijd
In de volgende tabel staan de minimale netwerkvereisten voor de verbinding tussen de webbrowser en de Application Object Server (AOS), en voor de verbinding tussen de AOS en de database in een on-premises systeem.

| Waarde     | Webbrowser met AOS                      | AOS met database |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Bandbreedte | 50 kilobytes per seconde (KBps) per gebruiker | 100 megabytes per seconde (MBps) |
| Vertragingstijd   | Minder dan 250-300 millisecondes (ms)     | Minder dan 1 ms (alleen LAN). AOS en de database moeten zich op dezelfde locatie bevinden. |

- Finance and Operations (on-premises) is ontworpen voor netwerken met een vertragingstijd van 250-300 milliseconden (ms) of minder. Dit is de vertragingstijd van een browserclient naar het datacentrum waar Finance and Operations wordt gehost.
- De bandbreedtevereisten voor Finance and Operations (on-premises) zijn afhankelijk van uw scenario. Typische scenario's vereisen een bandbreedte van meer dan 50 KBps tussen de browser en de Finance and Operations-server. Voor scenario's met hoge vereisten voor nettolading, zoals scenario's waarbij werkgebieden met uitgebreide aanpassingsmogelijkheden zijn betrokken, wordt meer bandbreedte aanbevolen. De specifieke hoeveelheid bandbreedte is afhankelijk van gebruik.

Implementaties waarbij de AOS en de Microsoft SQL Server-Database zich in verschillende datacenters bevinden, worden niet ondersteund. AOS en de SQL Server-database moeten zich op dezelfde locatie bevinden. 

Over het algemeen is Finance and Operations geoptimaliseerd voor het verminderen van het aantal roundtrips van browser naar server. Het aantal roundtrips vanuit een browserclient naar het datacenter is nul of één voor elke gebruikersinteractie en de nettolading is gecomprimeerd.

> [!WARNING]
> Bereken de bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten. Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen. Het is raadzaam om met een real-life simulatie in een niet-productieomgeving van Finance and Operations de beste prestaties te meten voor uw specifieke geval. 

### <a name="lan-environments"></a>LAN-omgevingen
In LAN-omgevingen is Microsoft Extern bureaublad in Microsoft Windows Server niet vereist om verbinding te maken met Finance and Operations. Extern bureaublad kan echter vereist zijn voor het afhandelen van bewerkingen op de virtuele machines (VM's) waaruit de serverimplementaties bestaan.

### <a name="wan-environments"></a>WAN-omgevingen
In WAN-netwerkomgevingen is Extern bureaublad in Windows Server niet vereist voor de verbinding met Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Vereisten voor internetverbinding
Finance and Operations (on-premises) vereist geen internetverbinding van de werkstations van gebruikers. Sommige functies zullen echter niet beschikbaar zijn zonder internetverbinding.

|                    |   |
|--------------------|---|
| **Browserclient** | Een intranetscenario zonder internetverbinding is een ontwerppunt voor de on-premises implementatie-optie. Sommige functies die cloudservices vereisen, zijn niet beschikbaar, zoals Help en taakbegeleiderbibliotheken in Microsoft Dynamics Lifecycle Services (LCS). |
| **Server**         | De AOS- of Microsoft Azure Service Fabric-laag moet kunnen communiceren met LCS. De on-premises browserclient vereist geen toegang tot internet. |
| **Telemetrie**      | Telemetriegegevens gaan mogelijk verloren bij lange onderbrekingen in de connectiviteit. Onderbrekingen in de verbinding met LCS hebben geen invloed op de functionaliteit van de on-premises toepassing. |
| **LCS**            | Verbinding met LCS is vereist voor implementatie, code-implementatie en onderhoudsactiviteiten. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetriegegevens overbrengen naar de cloud
De meeste telemetriegegevens worden lokaal opgeslagen en kan worden geopend met Logboeken in Microsoft Windows. Een kleine deel van de telemetriegebeurtenissen wordt overgebracht naar de Microsoft-telemetriepijplijn in de cloud voor diagnose. Klantgegevens en identificeerbare gebruikergegevens maken geen deel uit van de telemetriegegevens die naar Microsoft worden verzonden. VM-namen worden naar Microsoft verzonden als ondersteuning bij omgevingsbeheer en diagnose van het LCS-portal.

## <a name="domain-requirements"></a>Domeinvereisten
Houd rekening met de volgende domeinvereisten bij de installatie van Finance and Operations (on-premises):

- VM's die als host fungeren voor onderdelen van Finance and Operations (on-premises), moeten behoren bij een Active Directory-domein. Active Directory Domain Services (AD DS) moet worden geconfigureerd in de native modus.
- VM's waarop onderdelen van Finance and Operations (on-premises) worden uitgevoerd, moeten toegang hebben tot elkaar. Deze toegang is geconfigureerd in AD DS. 
- De domeincontroller moet Microsoft Windows Server 2012 R2 of hoger zijn en het domeinfunctionaliteitsniveau moet 2012 R2 of hoger zijn.

## <a name="hardware-requirements"></a>Hardwarevereisten
In deze sectie wordt de hardware beschreven die is vereist voor het uitvoeren van Finance and Operations (on-premises).

De werkelijke hardwarevereisten verschillen op basis van de systeemconfiguratie, de gegevenssamenstelling en de toepassingen en functies die u wilt gebruiken. Dit zijn enkele factoren die van invloed kunnen zijn op de keuze van de juiste hardware voor Finance and Operations (on-premises):

- Het aantal transacties per uur
- Het aantal gelijktijdige gebruikers

## <a name="minimum-infrastructure-requirements"></a>Minimale vereisten voor de infrastructuur
Finance and Operations (on-premises) maakt gebruik van Service Fabric als host voor AOS, batch- en gegevensbeheer, Management reporter en orchestratorservices voor de omgeving. 

SQL Server moet beschikken over een HADRON-installatie voor hoge beschikbaarheid met ten minste twee knooppunten voor de productie.

In de volgende illustratie wordt het aanbevolen minimumaantal knooppunten aangegeven in het Service Fabric-cluster.

[![Aanbevolen aantal knooppunten voor Service Fabric-cluster](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Processor en RAM-vereisten
De volgende tabellen bevatten het aantal processors en de hoeveelheid RAM-geheugen die vereist zijn voor elk van de functies die nodig zijn voor het uitvoeren van deze implementatieoptie. Lees voor meer informatie de aanbeveling voor de minimumvereisten voor een zelfstandige Service Fabric-cluster in [Service Fabric-cluster plannen en voorbereiden](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Als andere Microsoft-software wordt geïnstalleerd op dezelfde computer, moet het systeem ook voldoen aan de hardwarevereisten voor die software. Als andere servertoepassingen op dezelfde computer als AOS zijn geïnstalleerd, raden we aan om deze servertoepassingen te beperken tot 1 gigabyte (GB) RAM.

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

**Minimale grootte van ramingen voor de productie en de sandbox-implementaties\***

| Topologie                                        | Rol                          | Aantal exemplaren |
|-------------------------------------------------|-------------------------------|---------------------|
| Productie                                      | AOS (Gegevensbeheer, Batch)  | 3                   |
|                                                 | Management Reporter           | 2                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator\*\*              | 3                   |
| Sandbox                                         | AOS, Gegevensbeheer, Batch   | 2                   |
|                                                 | Management Reporter           | 1                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator                  | 3                   |
| *Overzicht voor productie en sandbox-topologieën* |                               | *16*                |

\* De getallen in deze tabel worden gevalideerd door onze testklanten en kunnen op basis van de feedback van deze klanten worden gecorrigeerd.

\*\* Orchestrator wordt aangewezen als het primaire knooppunttype en wordt ook gebruikt voor het uitvoeren van de Service Fabric-services.

**Aanvankelijke schattingen voor backend SQL Server en AD DS**

<table>
<thead>
<tr>
<th></th>
<th>Rol</th>
<th>VM's/exemplaren</th>
<th>Kernen</th>
<th>Totaal kernen</th>
<th>Geheugen per exemplaar (GB)</th>
<th>Totaal geheugen (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Gedeelde infrastructuur</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Bestandsserver/Storage Area Network/Opslag met hoge beschikbaarheid</td>
<td colspan="5"><p>De back-end opslagruimte moet zijn gebaseerd op solid-state drives (SSD) op een runtime storage area network (SAN).</p>
<p>Omvang en IOPS-verwerking (input/output operations per second) worden gebaseerd op de omvang van de werkbelasting.</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Samenvatting voor gedeelde infrastructuur</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*De omvang van de SQL Server is sterk afhankelijk van de werkbelasting. Zie voor meer informatie [Grootte van de hardware voor on-premises omgevingen vaststellen](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Opslag

- **AOS**: Finance and Operations (on-premises) gebruikt een SMB 3.0-share (Server Message Block) voor het opslaan van niet-gestructureerde gegevens. Zie voor meer informatie [Opslagruimte in Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL**: de volgende opties zijn beschikbaar:

    - Een SSD-installatie met hoge beschikbaarheid
    - Een SAN dat is geoptimaliseerd voor OLTP-doorvoercapaciteit (Online Transaction Processing)
    - Krachtige Direct-attached storage (DAS) 

- **IOPs voor SQL Server en gegevensbeheer**: de opslag voor gegevensbeheer en SQL Server moet ten minste 2000 IOPS hebben. Productie-IOPS is afhankelijk van veel factoren. Zie voor meer informatie [Grootte van de hardware voor on-premises omgevingen vaststellen](hardware-sizing-on-premises-environments.md).
- **VM IOPS** : elke VM moet ten minste 100 IOPS voor schrijven hebben.

## <a name="virtual-host-requirements"></a>Vereisten voor virtuele host
Zie de volgende richtlijnen bij het installeren van de virtuele hosts voor een Finance and Operations-omgeving (on-premises): [Service Fabric-cluster plannen en voorbereiden](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) en [Service Fabric-cluster beschrijven](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Elke virtuele host moet beschikken over voldoende cores voor de infrastructuur waarvoor het formaat wordt vastgesteld. Er zijn meerdere geavanceerde configuraties mogelijk, als SQL Server zich op fysieke hardware bevindt maar alle andere onderdelen gevirtualiseerd zijn. Als SQL Server is gevirtualiseerd, moet het schijfsubsysteem een snelle SAN of het equivalent daarvan zijn. In alle gevallen moet de basisinstallatie voor de virtuele host een hoge beschikbaarheid hebben en redundant zijn. Wanneer virtualisatie wordt gebruikt, moeten nooit VM-momentopnamen worden gemaakt.

## <a name="software-requirements-for-all-server-computers"></a>Softwarevereisten voor alle servercomputers
De volgende software moet aanwezig zijn op een computer voordat onderdelen voor Finance and Operations (on-premises) kunnen worden geïnstalleerd:

- Microsoft .NET Framework versie 4.5.1 of hoger
- Service Fabric

Voor meer informatie zie [Service Fabric-cluster plannen en voorbereiden](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Ondersteunde serverbesturingssystemen
De volgende tabel geeft een overzicht van de serverbesturingssystemen die worden ondersteund voor onderdelen van Finance and Operations.

| Besturingssysteem                                     | Opmerkingen |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter of Standard | Deze vereisten gelden voor de database en het Service Fabric-cluster dat als host fungeert voor AOS. |

## <a name="software-requirements-for-database-servers"></a>Softwarevereisten voor alle databaseservers

- Alleen 64-bits versies van SQL Server 2016 worden ondersteund.
- We raden aan om de meest recente cumulatieve update (CU) voor de gebruikte versie van SQL Server te installeren in een productieomgeving.
- Finance and Operations (on-premises) ondersteunt Unicode-sorteringen die niet hoofdlettergevoelig, accentgevoelig, kana-gevoelig en breedtegevoelig zijn. De sortering moet overeenkomen met de Windows-landinstellingen van de computers waarop AOS-exemplaren worden uitgevoerd. Als u een nieuwe installatie instelt, is het raadzaam dat u een Windows-sortering selecteert in plaats van een SQL Server-sortering. Zie voor meer informatie over het selecteren van een sortering voor een SQL Server-database de [documentatie bij SQL Server](/sql/sql-server/sql-server-technical-documentation).

De volgende tabel geeft een overzicht van de SQL Server-versies die worden ondersteund voor databases van Finance and Operations. Zie voor meer informatie de minimumvereisten voor hardware van [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Behoefte                                                      | Opmerkingen |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition of Enterprise Edition | Zie voor de hardwarevereisten voor SQL Server 2016 [Hardware- en softwarevereisten voor het installeren van SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Softwarevereisten voor Application Object Server (AOS) 
- SQL Server Integation Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Softwarevereisten voor Reporting Server (BI)
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>Softwarevereisten voor clientcomputers
De webtoepassing Finance and Operations werkt op elk apparaat met een HTML 5.0-compatibele webbrowser. Dit zijn enkele specifieke apparaat-/browsercombinaties die door Microsoft zijn bevestigd:

- Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
- Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
- Google Chrome (meest recente openbaar beschikbare release) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10-tablet
- Apple Safari (meest recente openbaar beschikbare release) op Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) of Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Softwarevereisten voor Active Directory Federation Services 
Active Directory Federation Services (AD FS) op Windows Server 2016 is vereist.

De domeincontroller moet Windows Server 2012 R2 of hoger zijn en het domeinfunctionaliteitsniveau moet 2012 R2 of hoger zijn. Voor meer informatie over niveaus voor domeinfunctionaliteit zie de volgende pagina's:

- [Wat zijn functionele niveaus in Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Inzicht in functionele niveaus voor Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Ondersteunde Microsoft Office-toepassingen
De volgende Microsoft Office-toepassingen worden ondersteund in implementaties van Finance and Operations in de cloud en on-premises:

-   Als u de invoegtoepassingen voor Microsoft Word en Microsoft Excel wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd. Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Hardware- en softwarevereisten voor Retail-onderdelen
Finance and Operations (on-premises) bevat op dit moment geen Retail-onderdelen.

