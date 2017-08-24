---
title: Systeemvereisten voor cloudimplementaties
description: In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Finance and Operations beschreven voor cloudimplementaties.
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46eacb2a01c3bfcc7144c7d8c39ee0189fd72e16
ms.contentlocale: nl-nl
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>Systeemvereisten voor cloudimplementaties

[!include[banner](../includes/banner.md)]

In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Finance and Operations beschreven voor cloudimplementaties. Voordat u Finance and Operations installeert, controleert u indien deze stap van toepassing is, of het systeem waarmee u werkt, voldoet aan de minimale vereisten voor netwerk, hardware en software.

## <a name="supported-web-browsers"></a>Ondersteunde webbrowsers
De webtoepassing kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:

-   Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
-   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
-   Google Chrome (meest recente openbaar beschikbare release) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10-tablet
-   Apple Safari (meest recente openbaar beschikbare release) op Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) of Apple iPad

Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant. 

> [!NOTE]
> -   Installeer een voorlopige versie van een Chrome-invoegtoepassing om Taakrecorder in te schakelen en schermopnamen te laten vastleggen en deze te laten opnemen in gegenereerde Microsoft Word-documenten. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   De workfloweditor wordt als ClickOnce-toepassing gestart. Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen. De ClickOnce-toepassing Workfloweditor vereist een compatibel 64-bits besturingssysteem.
> -   De Report Designer voor financiële rapportage wordt als ClickOnce-toepassing gestart. Hiervoor is een compatibel 64-bits besturingssysteem vereist. Als u Chrome gebruikt, moet u een ClickOnce-extensie installeren om de Report Designer-client te downloaden. Als u in de Incognito-modus van Chrome werkt, moet u ervoor zorgen dat de ClickOnce-extensie ook voor de Incognito-modus is ingeschakeld.
> -   Als u PDF-bestanden wilt bekijken, raden wij u aan moderne browsers te gebruiken, zoals Microsoft Edge (meest recente openbaar beschikbare versie) op Windows 10 of Google Chrome (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10 tablet.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Ondersteunde webbrowsers voor Retail Cloud POS

Retail Cloud POS kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:

-   Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
-   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
-   Chroom (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1 of Windows 7

## <a name="network-requirements"></a>Netwerkvereisten
-   Finance and Operations is ontworpen voor netwerken met een vertragingstijd van 250-300 milliseconden (ms) of minder. Dit is de latentie in een browserclient naar het Microsoft Azure-datacenter waar Finance and Operations wordt gehost. Het wordt aangeraden om uw netwerklatentie te testen op <http://www.azurespeed.com>.
-   De bandbreedtevereisten voor Finance and Operations zijn afhankelijk van uw scenario. De meest voorkomende scenario's vereisen een bandbreedte van meer dan 50 kilobytes per seconde (kbps). Voor scenario's met hoge vereisten voor nettolading, zoals scenario's waarbij werkgebieden met uitgebreide aanpassingsmogelijkheden zijn betrokken, wordt extra bandbreedte aanbevolen.

Over het algemeen is Finance and Operations geoptimaliseerd voor het internet. Het aantal roundtrips vanuit een browserclient naar het Azure-datacenter is erg klein en de gehele nettolading is gecomprimeerd. 

> [!WARNING]
> Bereken de bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten. Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen. Klanten die zich zorgen maken over de bandbreedtevereisten, kunnen het beste een evaluatieversie van Finance and Operations gebruiken.

## <a name="net-framework-requirements"></a>.NET Framework-vereisten
Finance and Operations vereist Microsoft .NET Framework versie 4.6.2 voor alle ClickOnce-toepassingen, zoals de documentrouterinsgagent. Zie voor de installatie-instructies [.NET Framework installeren](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Ondersteunde Microsoft Office-toepassingen
De volgende Microsoft Office-toepassingen worden ondersteund in implementaties van Finance and Operations in de cloud:

-   Als u de invoegtoepassingen voor Microsoft Word en Microsoft Excel wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd. Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.

## <a name="retail-modern-pos-requirements"></a>Vereisten voor Retail Modern POS

> [!NOTE]
> Als Retail Modern POS een offlinedatabase gebruikt, moet de computer voldoen aan alle systeemvereisten voor Microsoft SQL Server. Een offlinedatabase voor Retail Modern POS werkt op Microsoft SQL Server 2012 met Service Pack 3 of hoger, Microsoft SQL Server-2014 met Service Pack 2 of hoger en Microsoft SQL Server 2016. U kunt het beste altijd de meest recente versie gebruiken die beschikbaar is en de meest recente servicepacks installeren.

### <a name="supported-operating-systems"></a>Ondersteunde besturingssystemen

-   Retail Modern POS is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86- als ook x64-architectuur.
-   Retail Modern POS wordt alleen ondersteund op de Windows 10-versies Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten

-   De minimale ondersteunde resolutie is 1280 × 1024.
-   De computer waarop de Retail Modern POS wordt uitgevoerd, moet aan deze vereisten voldoen:

    -   Tenminste een dual core-processor, die wordt uitgevoerd met minstens 2 GHz.
    -   Er moet minimaal 3 gigabytes (GB) random-access memory (RAM) beschikbaar zijn.
    -   Er moet een internetverbinding zijn.

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

-   De connector voor Microsoft Dynamics AX heeft twee afzonderlijke installatieprogramma's, één voor Async Server Connector-service en één voor Real-time service voor Dynamics AX 2012 R3.
-   Beide componenten zijn 32-bits toepassingen, maar kunnen worden uitgevoerd op zowel x86- als ook x64-architectuur.
-   Beide onderdelen worden op de volgende besturingssystemen ondersteund:

    -   De Windows 7-versies Professional, Enterprise en Ultimate
    -   De Windows 8.1-versies Update 1 Professional, Enterprise en Embedded
    -   De Windows 10-versies Pro, Enterprise en Enterprise LTSB
    -   Microsoft Windows Server 2012 R2 en Microsoft Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten
-   2 GB RAM (4 GB RAM aanbevolen)
-   1,6 GHz piekprocessorsnelheid per core (twee cores minimaal)
-   Ten minste 10 GB vrije ruimte (de afzetkanaaldatabase kan veel opslagruimte nodig hebben).

## <a name="requirements-for-development-on-local-vms"></a>Vereisten voor ontwikkeling op lokale VM's
Zie voor informatie over de vereisten voor de ontwikkeling op lokale virtuele machines (VM's) [VM on-premises uitvoeren](../dev-tools/access-instances.md).


## <a name="see-also"></a>Zie ook

[Een evaluatie-exemplaar van Dynamics 365 for Finance and Operations, Enterprise-editie krijgen](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

