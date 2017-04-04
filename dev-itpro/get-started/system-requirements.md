---
title: Systeemvereisten
description: Dit onderwerp worden de systeemvereisten voor de huidige versie van Microsoft Dynamics 365 voor bewerkingen.
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Systeemvereisten

Dit onderwerp worden de systeemvereisten voor de huidige versie van Microsoft Dynamics 365 voor bewerkingen.

<a name="supported-web-browsers"></a>Ondersteunde webbrowsers
----------------------

De Microsoft Dynamics 365 voor webtoepassing bewerkingen kunt uitvoeren in een van de volgende webbrowsers die op de opgegeven besturingssystemen worden uitgevoerd:

-   Microsoft Edge (meest recente versie openbaar) op Windows 10
-   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
-   Google Chrome (meest recente versie openbaar) op 10 voor Windows, Windows 8.1, 8 voor Windows, Windows 7 of Google Nexus 10 tablet
-   Apple Safari (meest recente versie van openbaar) op Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10,12 (Sierra) en/of Apple iPad

Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant. **Opmerkingen:**

-   Voor het vastleggen van afbeeldingen die worden gegenereerd op basis van de taakregistratie en deze opnemen in Microsoft Word-documenten, moet u de extensie Verchroomd geïnstalleerd hebben. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   De workfloweditor wordt als ClickOnce-toepassing gestart. Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen. De workfloweditor ClickOnce-toepassing moet een 64-bits compatibel besturingssysteem.
-   De Report Designer voor financiële rapportage wordt als ClickOnce-toepassing gestart. Een 64-bits compatibel besturingssysteem vereist. Als u Verchroomd gebruikt, moet u een extensie ClickOnce wilt downloaden van het rapport designer-client installeren. Als u met de incognito modus Verchroomd gebruikt, ervoor zorgen dat de extensie ClickOnce ook is ingeschakeld voor de incognito modus.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Ondersteunde webbrowsers voor Retail Cloud POS

Cloud-POS detailhandel voor Dynamics 365 voor bewerkingen kunt uitvoeren in een van de volgende webbrowsers die op de opgegeven besturingssystemen worden uitgevoerd:

-   Microsoft Edge (meest recente versie openbaar) op Windows 10
-   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
-   Chroom (meest recente versie van openbaar) op 10 voor Windows, Windows 8.1 of Windows 7

## <a name="network-requirements"></a>Netwerkvereisten
-   Dynamics 365 voor bewerkingen is ontworpen voor netwerken met vertraging van minder dan 150 milliseconden (ms). Dit is de vertragingstijd in een browserclient naar het midden van Microsoft Azure gegevens die als host fungeert voor Dynamics 365 voor bewerkingen. Raadzaam netwerk vertragingstijd op te testen <http://www.azurespeed.com>.
-   Bandbreedtevereisten voor Dynamics 365 voor bewerkingen zijn afhankelijk van uw scenario. Meest voorkomende scenario's moet een bandbreedte van meer dan 50 kB per seconde (KBps). Voor scenario's met hoge nettolading vereisten, zoals werkruimten of scenario's voor uitgebreide aanpassingsmogelijkheden wordt meer bandbreedte echter aanbevolen.

In het algemeen is Dynamics 365 for Operations geoptimaliseerd voor het Internet. Het aantal retouren in een browserclient naar het midden Azure gegevens is erg klein en de gehele nettolading is gecomprimeerd. **Waarschuwing:** bandbreedtevereisten vanaf een client niet berekenen door te vermenigvuldigen met het aantal gebruikers de minimale bandbreedte-vereisten. Het gelijktijdige gebruik van een bepaalde locatie is zeer moeilijk te berekenen. Gebruik voor klanten die bezorgd over de bandbreedtevereisten zijn, een voorbeeldversie van Dynamics 365 voor bewerkingen.

## <a name="net-framework-requirements"></a>Vereisten voor .NET framework
Dynamics 365 voor bewerkingen is .NET Framework versie 4.6.2 voor alle Klik-eenmaal toepassingen, zoals de routering agent document. Zie voor de installatie-instructies, [installatie van .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Ondersteunde Microsoft Office-toepassingen
-   Als u wilt uitvoeren in de Microsoft Excel en Word-invoegtoepassingen, hebt u Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd. Zie voor meer informatie over de versievereisten [Office-integratie oplossen](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Als u wilt weergeven van documenten die worden gegenereerd door het exporteren naar Excel of exporteren naar Word-functionaliteit, moet Microsoft Office 2007 of hoger geïnstalleerd.

## <a name="retail-modern-pos-requirements"></a>Retail POS moderne vereisten
### <a name="supported-operating-systems"></a>Ondersteunde besturingssystemen

-   Retail POS op moderne is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86 en x64 architectuur.
-   Retail POS op moderne wordt alleen ondersteund op edities van Windows 10 Pro-, ondernemings- en Enterprise lange termijn onderhoud vertakking (LTSB).

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten

-   De minimale ondersteunde resolutie is 1280 × 1024.
-   De computer waarop de moderne POS detailhandel wordt uitgevoerd, moet aan deze vereisten voldoen:
    -   Moet hebben, ten minste een dual core-processor die wordt uitgevoerd op niet minder dan 2 GHz (gigahertz).
    -   Moet hebben, ten minste 3 gigabyte (GB) RAM.
    -   Internet-toegang moet hebben.

## <a name="retail-hardware-station-requirements"></a>Hardwarevereisten voor station detailhandel
### <a name="supported-operating-systems"></a>Ondersteunde besturingssystemen

-   Retail hardware station is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86 en x64 architectuur.
-   Retail hardware station wordt ondersteund door de volgende besturingssystemen:
    -   De edities Windows 7 Professional, Enterprise en Ultimate **opmerking:** Windows 7 wordt alleen ondersteund als Internet Explorer 11 handmatig op het systeem is geïnstalleerd.
    -   De edities Windows 8.1 Update 1 Professional, Enterprise en ingesloten
    -   Windows 10 Pro-, ondernemings- en LTSB Enterprise-edities

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten

De computer moet voldoen aan alle systeemvereisten voor het installeren en gebruiken van de volgende opties:

-   Internet Information Services (IIS)
-   Fabrikanten van hardware

## <a name="retail-store-scale-unit-requirements"></a>Detailhandel winkelvoorraad schaaleenheid vereisten
### <a name="supported-operating-systems"></a>Ondersteunde besturingssystemen

-   Retail Store schaaleenheid is een 32-bits toepassing, maar deze kan worden uitgevoerd op zowel x86 en x64 architectuur.
-   Retail Store schaaleenheid wordt ondersteund door de volgende besturingssystemen:
    -   De edities Windows 7 Professional, Enterprise en Ultimate
    -   De edities Windows 8.1 Update 1 Professional, Enterprise en ingesloten
    -   Windows 10 Pro-, ondernemings- en LTSB Enterprise-edities

### <a name="minimum-system-requirements"></a>Minimale systeemvereisten

-   4 GB RAM
-   1,6 GHz piekperiode CPU-snelheid per core (twee cores zijn de minimale.)
-   Ten minste 10 GB vrije ruimte (de kanaaldatabase kan een grote hoeveelheid ruimte vereist).

### <a name="recommended-system-requirements"></a>Aanbevolen systeemvereisten

-   6 GB RAM
-   2.4 GHz i7 (of equivalent) piekperiode CPU versnellen per core (vier cores worden aanbevolen.)
-   Ten minste 10 GB vrije ruimte (de kanaaldatabase kan een grote hoeveelheid ruimte vereist).

## <a name="requirements-for-development-on-local-vms"></a>Vereisten voor de ontwikkeling van lokale VMs
Zie voor informatie over de vereisten voor de ontwikkeling van lokale virtuele machines (VMs) [VM uitgevoerd op gebouwen](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Zie ook
--------

[Een evaluatie-exemplaar van Dynamics 365 voor bewerkingen ophalen](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


