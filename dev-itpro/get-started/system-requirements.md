---
title: Systeemvereisten
description: In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Operations beschreven.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 86053196a3aad6b7b5d7830860e1af347dd969d8
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="system-requirements"></a>Systeemvereisten

[!include[banner](../includes/banner.md)]


In dit onderwerp worden systeemvereisten voor de actuele versie van Microsoft Dynamics 365 for Operations beschreven.

<a name="supported-web-browsers"></a>Ondersteunde webbrowsers
----------------------

De Microsoft Dynamics 365 for Operations-webtoepassing kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:

-   Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
-   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
-   Google Chrome (meest recente openbaar beschikbare release) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10-tablet
-   Apple Safari (meest recente openbaar beschikbare release) op Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) of Apple iPad

Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant. **Opmerkingen:**

-   Om schermopnamen vast te leggen die door Taakrecorder zijn gegenereerd en deze op te nemen in Microsoft Word-documenten, moet u een Chrome-invoegtoepassing hebben geïnstalleerd. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   De workfloweditor wordt als ClickOnce-toepassing gestart. Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen. De ClickOnce-toepassing Workfloweditor vereist een compatibel 64-bits besturingssysteem.
-   De Report Designer voor financiële rapportage wordt als ClickOnce-toepassing gestart. Hiervoor is een compatibel 64-bits besturingssysteem vereist. Als u Chrome gebruikt, moet u een ClickOnce-extensie installeren om de rapportontwerper-client te downloaden. Als u in de incognito modus van Chrome werkt, moet u ervoor zorgen dat de ClickOnce-extensie ook voor de incognito modus is ingeschakeld.
-   Als u PDF-bestanden wilt bekijken, raden wij u aan moderne browsers te gebruiken, zoals Microsoft Edge (meest recente openbaar beschikbare versie) op Windows 10 of Google Chrome (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10 tablet.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Ondersteunde webbrowsers voor Retail Cloud POS

Retail Cloud POS voor Microsoft Dynamics 365 for Operations kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien:

-   Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
-   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
-   Chroom (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1 of Windows 7

## <a name="network-requirements"></a>Netwerkvereisten
-   Dynamics 365 for Operations is ontworpen voor netwerken met latentie van minder dan 150 milliseconden (ms). Dit is de latentie in een browserclient naar het Microsoft Azure-datacentrum waar Dynamics 365 for Operations wordt gehost. Het wordt aangeraden om uw netwerklatentie te testen op <http://www.azurespeed.com>.
-   De bandbreedtevereisten voor Dynamics 365 for Operations zijn afhankelijk van uw scenario. De meest voorkomende scenario's vereisen een bandbreedte van meer dan 50 kilobytes per seconde (kbps). Voor scenario's met hoge vereisten nettolading, zoals werkgebieden of scenario's voor uitgebreide aanpassingsmogelijkheden wordt meer bandbreedte aanbevolen.

Over het algemeen is Dynamics 365 for Operations geoptimaliseerd voor het internet. Het aantal roundtrips vanuit een browserclient naar het Azure-datacentrum is erg klein en de gehele nettolading is gecomprimeerd. **Waarschuwing:** Bereken bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten. Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen. Gebruik voor klanten die zich zorgen maken over de bandbreedtevereisten, een evaluatieversie van Dynamics 365 for Operations.

## <a name="net-framework-requirements"></a>.NET Framework-vereisten
Dynamics 365 for Operations vereist .NET Framework versie 4.6.2 voor alle ClickOnce-toepassingen, zoals de documentrouterinsgagent. Zie voor de installatie-instructies [.NET Framework installeren](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Ondersteunde Microsoft Office-toepassingen
-   Als u de invoegtoepassingen voor Microsoft Word en Microsoft Excel wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd. Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.

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
    -   De Windows 7-versies Professional, Enterprise en Ultimate **Opmerking:** Windows 7 wordt alleen ondersteund als Internet Explorer 11 handmatig op het systeem is geïnstalleerd.
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

## <a name="requirements-for-development-on-local-vms"></a>Vereisten voor ontwikkeling op lokale VM's
Zie voor informatie over de vereisten voor de ontwikkeling op lokale virtuele machines (VM's) [VM on-premises uitvoeren](../dev-tools/access-instances.md).

<a name="see-also"></a>Zie ook
--------

[Een evaluatie-exemplaar van Dynamics 365 for Operations ophalen](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)




