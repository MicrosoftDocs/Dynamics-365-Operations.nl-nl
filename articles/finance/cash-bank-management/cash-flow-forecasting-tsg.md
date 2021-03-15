---
title: Problemen met het instellen van cashflowprognoses oplossen
description: Dit onderwerp bevat beantwoorden op vragen die u kunt hebben wanneer u cashflowprognoses configureert. Hierin komen veelgestelde vragen (FAQ) over de opzet voor cashflow, updates van cashflow en cashflow Power BI aan de orde.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985282"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Problemen met het instellen van cashflowprognoses oplossen

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat beantwoorden op vragen die u kunt hebben wanneer u cashflowprognoses configureert. Hierin komen veelgestelde vragen (FAQ) over de opzet voor cashflow, updates van cashflow en cashflow Power BI aan de orde.

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

Controleer of de metingen 'Cashflowmeting V2' en 'LedgerCovLiquidityMeasurement' van Entiteitopslag zijn geconfigureerd. Zie [Power BI-integratie met Entiteitopslag](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) voor more informatie over hoe u kunt werken met Entiteitopslag. Controleer of alle vereiste stappen voor het weergeven van Power BI-inhoud zijn uitgevoerd. Zie [Power BI-inhoud Overzicht van contant geld](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Zijn de entiteiten van de Entiteitopslag vernieuwd?

U moet uw entiteiten periodiek vernieuwen om er zeker van te zijn dat de gegevens actueel en nauwkeurig zijn. Als u een specifieke entiteit handmatig wilt vernieuwen, gaat u naar **Systeembeheer \> Setup \> Entiteitopslag**, selecteert u de entiteit en u vervolgens **Vernieuwen**. De gegevens kunnen ook automatisch worden bijgewerkt. Stel op de pagina **Entiteitopslag** de optie **Automatisch vernieuwen** in op **Ja**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]