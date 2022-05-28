---
title: Systeemvereisten
description: In dit onderwerp worden de systeemvereisten voor Microsoft Dynamics 365 Human Resources weergegeven.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e88006ebf174f1a416fa6d8572d439a0395f0e44
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690857"
---
# <a name="system-requirements"></a>Systeemvereisten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de systeemvereisten voor Microsoft Dynamics 365 Human Resources weergegeven. Het artikel bevat ook een overzicht van de landen en regio's waarin Human Resources beschikbaar is, plus informatie over talen en lokalisatie voor Human Resources-gegevens.

## <a name="supported-web-browsers"></a>Ondersteunde webbrowsers

Gebruikers kunnen Microsoft Dynamics 365 Human Resources uitvoeren in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien: 

*   Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
*   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
*   Google Chrome (meest recente openbaar beschikbare versie)
*   Apple Safari (meest recente openbaar beschikbare versie)

Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant. 

## <a name="special-considerations"></a>Speciale overwegingen

* Installeer een voorlopige versie van een Chrome-invoegtoepassing om Taakrecorder in te schakelen voor het vastleggen van schermopnamen en om deze te laten opnemen in gegenereerde Microsoft Word-documenten
* De workfloweditor wordt als ClickOnce-toepassing gestart. Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen. De ClickOnce-toepassing Workfloweditor vereist een compatibel 64-bits besturingssysteem.
* Als u PDF-bestanden wilt bekijken, raden wij u aan moderne browsers te gebruiken, zoals Microsoft Edge (meest recente openbaar beschikbare versie) op Windows 10 of Google Chrome (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10 tablet.

## <a name="network-requirements"></a>Netwerkvereisten

* Human Resources is ontworpen voor netwerken met een latentie van 250-300 milliseconden (ms) of minder. Dit is de latentie van een browserclient naar het Microsoft Azure-datacentrum waar Human Resources wordt gehost. Het wordt aangeraden om uw netwerklatentie te testen op [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").
* Bandbreedtevereisten voor Human Resources zijn afhankelijk van uw scenario. De meest voorkomende scenario's vereisen een bandbreedte van meer dan 50 kilobytes per seconde (kbps).
 
> [!WARNING]
> Bereken bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten. Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen. Gebruik voor klanten die zich zorgen maken over de bandbreedtevereisten, een evaluatieversie van Human Resources.

## <a name="supported-microsoft-office-applications"></a>Ondersteunde Microsoft Office-toepassingen

* Als u de invoegtoepassingen voor Microsoft Excel en Word wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd. Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Problemen met Office-integratie oplossen").
* Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.

## <a name="regional-availability-languages-and-localization"></a>Regionale beschikbaarheid, talen en lokalisatie

U kunt een PDF-bestand downloaden met de landen, regio's en talen die door Human Resources worden ondersteund in [Internationale beschikbaarheid van Microsoft Dynamics 365](/dynamics365/get-started/availability). 

> [!NOTE]
> Terwijl de gebruikersinterface wordt gelokaliseerd in andere talen, worden alle gebruikersgegevens opgeslagen in de taal waarin deze zijn ingevoerd. U kunt e-mails en sjablonen in andere talen maken, maar gegevens zoals planningsgegevens zijn op dit moment alleen in het Engels beschikbaar.

Zie [Globalisatie](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region) als u een ontwikkelaar bent die geïnteresseerd is in het maken van land- of regiospecifieke aanpassingen of in het maken van een oplossing voor een land dat of regio die momenteel niet door Microsoft wordt ondersteund.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
