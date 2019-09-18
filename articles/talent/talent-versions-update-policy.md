---
title: Systeemvereisten en updatebeleid voor Talent
description: In dit onderwerp worden vereisten voor Dynamics 365 for Talent weergegeven. Ook wordt het updatebeleid beschreven.
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6c881bf25e7145228ccf7ef73a7ef3637c115a49
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741770"
---
# <a name="talent-system-requirements-and-update-policy"></a>Systeemvereisten en updatebeleid voor Talent

[!include [banner](includes/banner.md)]

In dit onderwerp worden de vereisten beschreven voor Microsoft Dynamics 365 for Talent, met inbegrip van Attract, Onboard, en Core HR. Het bevat ook een overzicht van de landen en regio's waarin Talent beschikbaar is, plus informatie over talen en lokalisatie voor Talent-gegevens. In toevoegingen bevat dit onderwerp het updatebeleid voor Talent.

## <a name="supported-web-browsers"></a>Ondersteunde webbrowsers

De webtoepassing Microsoft Dynamics 365 for Talent kan worden uitgevoerd in alle onderstaande webbrowsers die op de opgegeven besturingssystemen draaien: 

*   Microsoft Edge (meest recente openbaar beschikbare release) op Windows 10
*   Internet Explorer 11 op Windows 10, Windows 8.1 of Windows 7
*   Google Chrome (meest recente openbaar beschikbare versie)
*   Apple Safari (meest recente openbaar beschikbare versie)

Als u de laatste versie van elke webbrowser wilt opzoeken, gaat u naar de website van de softwarefabrikant. 

> [!NOTE]
> * Om schermopnamen vast te leggen die door Taakrecorder zijn gegenereerd en deze op te nemen in Microsoft Word-documenten, moet u een Chrome-invoegtoepassing hebben geïnstalleerd. 
> * De workfloweditor wordt als ClickOnce-toepassing gestart. Alleen Microsoft Edge en Internet Explorer (op een ondersteunde versie van Microsoft Windows) ondersteunen ClickOnce-toepassingen. De ClickOnce-toepassing Workfloweditor vereist een compatibel 64-bits besturingssysteem.
> * Als u PDF-bestanden wilt bekijken, raden wij u aan moderne browsers te gebruiken, zoals Microsoft Edge (meest recente openbaar beschikbare versie) op Windows 10 of Google Chrome (meest recente openbaar beschikbare versie) op Windows 10, Windows 8.1, Windows 8, Windows 7 of Google Nexus 10 tablet.
>   Netwerkvereisten
> * Dynamics 365 for Talent is ontworpen voor netwerken met een vertragingstijd van 250-300 milliseconden (ms) of minder. Dit is de vertragingstijd van een browserclient naar het Microsoft Azure-datacentrum waar Dynamics 365 for Talent wordt gehost. Het wordt aangeraden om uw netwerklatentie te testen op [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").
> * Bandbreedtevereisten voor Dynamics 365 for Talent zijn afhankelijk van uw scenario. De meest voorkomende scenario's vereisen een bandbreedte van meer dan 50 kilobytes per seconde (kbps).
> 
> [!WARNING]
> Bereken bandbreedtevereisten vanaf een clientlocatie niet door het aantal gebruikers te vermenigvuldigen met de minimale bandbreedte-vereisten. Het gelijktijdige gebruik van een bepaalde locatie is zeer lastig te berekenen. Gebruik voor klanten die zich zorgen maken over de bandbreedtevereisten, een evaluatieversie van Dynamics 365 for Talent.

## <a name="supported-microsoft-office-applications"></a>Ondersteunde Microsoft Office-toepassingen

* Als u de invoegtoepassingen voor Microsoft Excel en Word wilt uitvoeren, moet Microsoft Office 2016 voor Windows of Mac zijn geïnstalleerd. Zie voor meer informatie over de versievereisten [Probleemoplossing voor Office-integratie](../dev-itpro/office-integration/office-integration-troubleshooting.md "Probleemoplossing voor Office-integratie").
* Als u documenten wilt weergeven die worden gegenereerd door de functie Exporteren naar Excel of Exporteren naar Word, moet Microsoft Office 2007 of hoger zijn geïnstalleerd.

## <a name="regional-availability-languages-and-localization"></a>Regionale beschikbaarheid, talen en lokalisatie

U kunt een PDF-bestand downloaden met de landen, regio's en talen die door Talent worden ondersteund in [Internationale beschikbaarheid van Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Terwijl de gebruikersinterface wordt gelokaliseerd in andere talen, worden alle gebruikersgegevens opgeslagen in de taal waarin deze zijn ingevoerd. U kunt e-mails en sjablonen in andere talen maken, maar gegevens zoals planningsgegevens zijn op dit moment alleen in het Engels beschikbaar.

Zie [Globalisatie](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region) als u een ontwikkelaar bent die geïnteresseerd is in het maken van land- of regiospecifieke aanpassingen of in het maken van een oplossing voor een land dat of regio die momenteel niet door Microsoft wordt ondersteund.

## <a name="update-policy"></a>Updatebeleid

Microsoft Dynamics 365 for Talent wordt aangeboden via de cloud. Updates voor Dynamics 365 for Talent vinden doorlopend plaats en worden automatisch toegepast door Microsoft.

Er worden regelmatig updates uitgebracht en doorgevoerd in alle omgevingen. Dynamics 365 for Talent wordt ondersteund volgens het [Microsoft Support Lifecycle-beleid](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), dat consistente en voorspelbare richtlijnen bevat voor de beschikbaarheid van productondersteuning.
