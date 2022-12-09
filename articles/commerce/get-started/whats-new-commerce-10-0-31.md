---
title: Preview van Dynamics 365 Commerce 10.0.31 (februari 2023)
description: In dit artikel worden de functies beschreven die in Microsoft Dynamics 365 Commerce 10.0.31 nieuw of gewijzigd zijn.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: ed4325095163415d05a56128cb1f0334440fe0e5
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787521"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Preview van Dynamics 365 Commerce 10.0.31 (februari 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Microsoft Dynamics 365 Commerce previewversie 10.0.31. Deze versie heeft het buildnummer 10.0.1406 en is beschikbaar volgens de onderstaande planning:

- **Preview van versie:** oktober 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** januari 2023
- **Algemene beschikbaarheid van versie (automatische update):** februari 2023

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit artikel gewijzigd om functies op te nemen die zijn toegevoegd na de oorspronkelijke publicatie van dit artikel.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door   |
|---|---|---|---|
| Foutcodes | Commerce heeft gestandaardiseerde foutverwijzingen ingevoerd die moeten worden opgenomen in betalingsfouten van online kanalen die worden getoond aan online klanten.| [Foutcodes voor betalingsmodule](../checkout-module-error-codes.md)  | Standaard ingeschakeld |
| Betalingen | [Apple Pay met Dynamics 365-betalingsconnector voor Adyen inschakelen](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | E-commerceklanten kunnen Apple Pay gebruiken op winkelwagen- en uitcheckpagina's wanneer ze ondersteunde apparaten of browsers gebruiken. | Opt-in voor ontwikkelaars |
| Betalingen  |  Commerce heeft de mogelijkheid toegevoegd om de interactie tussen gebruikers met terugkerende-betalingstokens in de gehele gebruikersinterface van Commerce headquarters te beperken. In betalingsformulieren, zoals de pagina **Verkooporder callcenter**, wordt het eerder gebruikte token voor terugkerende betalingen van een klant niet meer weergegeven voor gebruik in een nieuwe transactie. Alleen een bepaalde 'kaart in bestand' die op het Commerce-scherm **Betalingen van klant** wordt ingevoerd of met een overeenkomst met een klant terwijl deze via een verkooporder betaalt, wordt bij het verwerken van een betaling voor een nieuwe transactie gepresenteerd aan de gebruikers van het callcenter of gebruikers van Commerce headquarters. | [Het gebruik van tokens voor betalingen beperken](../dev-itpro/limit-token-usage.md)  |  Functiebeheer<p>*Gebruik van betalingstoken beperken tot ordercontext*  |
| POS | [Inkooporders maken vanuit POS](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Met de bewerking Inkomende voorraad in POS-app (Point of Sale) kunnen gebruikers inkooporderaanvragen maken, bewerken en bevestigen. |  Functiebeheer<p>*Mogelijkheid om een inkooporderaanvraag te maken in POS*   |
| Extra talen beschikbaar | Er zijn vier extra talen beschikbaar | Er zijn vier nieuwe talen beschikbaar voor de selectie van gebruikers in de lijst met voorkeurstaal: Koreaans, Portugees (Portugal), Vietnamees en Chinees (traditioneel). Als u deze optie wilt selecteren, gaat u naar **Gebruikersopties \> Voorkeuren \> Voorkeuren voor taal en land/regio**. | Gelokaliseerde voorkeuren |  



## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Commerce 10.0.31 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.31 van apps voor financiën en bedrijfsactiviteiten (februari 2023)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van versie 10.0.31, meldt u zich aan bij Lifecycle Services van Microsoft Dynamics en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2022

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk de [Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2022](/dynamics365-release-plan/2022wave2/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-commerce-features"></a>Verwijderde en afgeschafte Commerce-functies

In het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) worden functies beschreven die zijn verwijderd of afgeschaft voor Commerce.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Commerce](removed-deprecated-features-commerce.md).


Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
