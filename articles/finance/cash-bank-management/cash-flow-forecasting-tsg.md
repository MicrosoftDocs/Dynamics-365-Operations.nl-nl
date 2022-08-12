---
title: Problemen met het instellen van cashflowprognoses oplossen
description: Dit artikel bevat beantwoorden op vragen die u kunt hebben wanneer u cashflowprognoses configureert. Hierin komen veelgestelde vragen (FAQ) over de opzet voor cashflow, updates van cashflow en cashflow Power BI aan de orde.
author: angelad116
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 807a1da1906bdefec38954cea02ed29b0157d69e
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151396"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Problemen met het instellen van cashflowprognoses oplossen

[!include [banner](../includes/banner.md)]

Dit artikel bevat beantwoorden op vragen die u kunt hebben wanneer u cashflowprognoses configureert. Hierin komen veelgestelde vragen (FAQ) over de opzet voor cashflow, updates van cashflow en cashflow Power BI aan de orde.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Waarom wordt de cashflow voor slechts één rechtspersoon weergegeven?

Cashflowprognoses worden geconfigureerd en berekend per rechtspersoon. Power BI-rapporten en de cashflowprognosemogelijkheden in Finance Insights geven de resultaten weer.

Cashflowprognoses moeten worden ingesteld voor elke rechtspersoon voor wie u een prognose wilt bekijken. Controleer de configuratie van cashflowprognoses in al uw rechtspersonen. U kunt ook de configuratie van alle rechtspersonen voor cashflowprognose controleren en controleren of deze zijn ingesteld zoals u bedoeld hebt.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Waarom worden in Power BI niet alle cashflowgegevens weergegeven?

Er moeten verschillende stappen worden uitgevoerd voordat cashflowprognoses in Power BI-weergaven kunnen verschijnen. Loop de volgende controlelijst na en controleer of elke stap is voltooid:

- Stel de cashflow in voor elke rechtspersoon.
- In grootboekparameters stelt u de systeemvaluta en het systeemwisselkoerstype in.
- De valuta voor boekhouding van het grootboek en het wisselkoerstype instellen.
- Voer wisselkoersen in tussen de transactievaluta en de valuta voor de boekhouding.
- Voer wisselkoersen in tussen de valuta voor de boekhouding en de systeemvaluta.
- Voer wisselkoersen in tussen de valuta voor de boekhouding en elke bankvaluta.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Waarom werkt cashflow Power BI in vorige versies, maar is nu leeg?

Controleer of de metingen 'Cashflowmeting V2' en 'LedgerCovLiquidityMeasurement' van Entiteitopslag zijn geconfigureerd. Meer informatie over het werken met gegevens in Entiteitopslag vindt u in het onderwerp [Power BI-integratie met Entiteitopslag](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Controleer of alle benodigde stappen voor het weergeven van Power BI-inhoud zijn voltooid. Zie [Power BI-inhoud Overzicht van contant geld](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Zijn de entiteiten van de Entiteitopslag vernieuwd?

U moet uw entiteiten periodiek vernieuwen om er zeker van te zijn dat de gegevens actueel en nauwkeurig zijn. Als u een specifieke entiteit handmatig wilt vernieuwen, gaat u naar **Systeembeheer \> Setup \> Entiteitopslag**, selecteert u de entiteit en u vervolgens **Vernieuwen**. De gegevens kunnen ook automatisch worden bijgewerkt. Stel op de pagina **Entiteitopslag** de optie **Automatisch vernieuwen** in op **Ja**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Welke berekeningsmethode moet worden gebruikt bij het berekenen van cashflowprognoses?

De berekeningsmethode Cashflowprognose biedt twee belangrijke selectieopties. Met de optie **Nieuw** worden cashflowprognoses berekend voor nieuwe documenten en documenten die zijn gewijzigd sinds de laatste batchverwerking is uitgevoerd. Deze optie wordt meestal sneller uitgevoerd omdat een kleinere subset van documenten wordt verwerkt. Met de optie **Totaal** worden cashflowprognoses voor elk document in het systeem opnieuw berekend. Deze optie kost meer tijd omdat er meer werk te voltooien is.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Hoe verbeter ik de prestaties van de terugkerende batchtaak voor cashflowprognoses?

We raden u aan uw cashflowprognose eenmaal per dag uit te voeren tijdens daluren met behulp van de berekeningsmethode **Nieuw**. We raden u aan dit zes dagen per week te doen. Voer vervolgens eenmaal per week een cashflowprognose met de berekeningsmethode **Totaal** uit op de dag met de minste hoeveelheid activiteit.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

