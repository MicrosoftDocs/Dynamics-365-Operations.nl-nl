---
title: Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management
description: In dit artikel worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering in Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f70d05f5663d8249b2435ad353421c278692a9ac
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218797"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dit artikel wordt bijgewerkt zodra er nieuwe verwijderde of verouderde functies worden gedocumenteerd voor Dynamics 365 Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen.

> [!NOTE]
> Gedetailleerde informatie over objecten in apps voor financiën en bedrijfsactiviteiten is te vinden in de [Rapporten met technische naslaginformatie](/dynamics/s-e/). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van apps voor financiën en bedrijfsactiviteiten.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Verwijderde of verouderde functies in versie 10.0.29 van Supply Chain Management

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Voorraadtransferorders met belasting op de transferprijs

| &nbsp;  | &nbsp;  |
|---|---|
| **Reden voor afschaffing/verwijdering** | De functionaliteit [voorraadtransferorders met belasting op de transferprijs](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) wordt vervangen door de functionaliteit [voorraadtransferorders voor India](../../finance/localizations/apac-ind-stock-transfer.md). |
| **Vervangen door een andere functie?**   | Ja, de functionaliteit [voorraadtransferorders met belasting op de transferprijs](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) wordt vervangen door de functionaliteit [voorraadtransferorders voor India](../../finance/localizations/apac-ind-stock-transfer.md). |
| **Betrokken productgebieden** | Supply Chain Management - voorraad |
| **Implementatieoptie** | Cloud en on-premises |
| **Status** | <p>Wordt afgeschaft. De functionaliteit *voorraadtransferorders met belasting op de transferprijs* wordt niet langer ondersteund met correcties voor fouten en beveiligingsfixes.</p><p>Na april 2023 wordt klanten gevraagd om standaard de verbeterde functionaliteit *Voorraadtransferorders voor India* te gebruiken. Na oktober 2023 is de functionaliteit *voorraadtransferorders met belasting op de transferprijs* niet langer beschikbaar en wordt klanten gevraagd de verbeterde functionaliteit *Voorraadtransferorders voor India* te gebruiken.</p><p>Raadpleeg [Voorraadtransferorders voor India](../../finance/localizations/apac-ind-stock-transfer.md) voor meer informatie.</p> |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Verwijderde of verouderde functies in versie 10.0.19 van Supply Chain Management

### <a name="job-card-device"></a>Apparaat voor taakkaarten

| &nbsp;  | &nbsp;  |
|---|---|
| **Reden voor afschaffing/verwijdering** | Het [taakkaartapparaat](../production-control/config-job-card-device.md) is vervangen door de nieuwe [uitvoeringsinterface voor de werkvloer](../production-control/production-floor-execution-configure.md). |
| **Vervangen door een andere functie?**   | Ja, het [taakkaartapparaat](../production-control/config-job-card-device.md) wordt vervangen door de nieuwe [uitvoeringsinterface voor de werkvloer](../production-control/production-floor-execution-configure.md). |
| **Betrokken productgebieden** | Supply Chain Management - productiebeheer |
| **Implementatieoptie** | Cloud en on-premises |
| **Status** | Afgeschaft. Het taakkaartapparaat krijgt ondersteuning met fout- en beveiligingscorrecties, maar functieverbeteringen worden niet langer geleverd. Na april 2022 wordt het taakkaartapparaat niet meer ondersteund en worden klanten gevraagd om over te stappen naar de nieuwe uitvoeringsinterface voor de werkvloer. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Verwijderde of verouderde functies in versie 10.0.18 van Supply Chain Management

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a>Supply Chain Management - Magazijnbeheer (de magazijnapp)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Met ingang van april 2021 wordt *Supply Chain Management - Magazijnbeheer* (de magazijnapp) afgeschaft en wordt na april 2022 niet meer ondersteund. Het is nu vervangen door de *mobiele app Magazijnbeheer*, die werd uitgebracht met versie 10.0.17 van Supply Chain Management. De nieuwe app is een complete vervanging, maar maakt gebruik van hetzelfde onderliggende framework, waardoor migratie eenvoudig is. Indien nodig kunnen de twee apps naast elkaar worden gebruikt om gebruikers te helpen zich geleidelijk aan te passen terwijl ze de nieuwe app leren gebruiken.<br><br>Zie [Mobiele toepassing Magazijnbeheer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) en [De mobiele app Magazijnbeheer installeren en verbinden](../warehousing/install-configure-warehouse-management-app.md) voor meer informatie over de mobiele app Magazijnbeheer. |
| **Vervangen door een andere functie?**   | Ja, vervangen door de nieuwe mobiele app Magazijnbeheer. |
| **Betrokken productgebieden**         | Supply Chain Management - magazijn-app |
| **Implementatieoptie**              | Cloud en on-premises |
| **Status**                         | Afgeschaft. De magazijn-app krijgt ondersteuning met fout- en beveiligingscorrecties, maar functieverbeteringen worden niet langer geleverd. Na april 2022 wordt de oude magazijn-app niet meer ondersteund en worden klanten gevraagd om over te stappen naar de nieuwe mobiele app Magazijnbeheer. De oude magazijn-app wordt vervolgens verwijderd uit de Microsoft Store en Google Play Store.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Verwijderde of verouderde functies in versie 10.0.15 van Supply Chain Management

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-ondersteuning voor Dynamics 365 is afgeschaft

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Met ingang van december 2020 wordt Microsoft Internet Explorer 11-ondersteuning voor alle Dynamics 365-producten afgeschaft en wordt Internet Explorer 11 na augustus 2021 niet meer ondersteund.<br><br>Dit heeft invloed op klanten die Dynamics 365-producten gebruiken die zijn ontworpen om via een Internet Explorer 11-interface te worden gebruikt. Na augustus 2021 wordt Internet Explorer 11 niet ondersteund voor dergelijke Dynamics 365-producten. |
| **Vervangen door een andere functie?**   | Wij raden klanten aan om overstappen op Microsoft Edge.|
| **Betrokken productgebieden**         | Alle Dynamics 365-producten |
| **Implementatieoptie**              | Alles|
| **Status**                         | Afgeschaft. Internet Explorer 11 wordt na augustus 2021 niet ondersteund.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Gebruik van ingebouwde hoofdplanningsengine voor Supply Chain Management voor productiescenario's

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Voor betere prestaties en een minimale belasting van de SQL-database tijdens de uitvoering van hoofdplanningen, wordt de ingebouwde engine voor de hoofdplanning van Supply Chain Management vervangen door Planningsoptimalisatie. Met Planningsoptimalisatie kunnen snel planningen worden uitgevoerd, zelfs tijdens kantooruren. Hierdoor kunnen planners direct reageren op wijzigingen in vraag- of planningsparameters. |
| **Vervangen door een andere functie?**   | Ja, Planningsoptimalisatie vervangt de bestaande ingebouwde Supply Chain Management-hoofdplanningsengine. |
| **Betrokken productgebieden**         | Supply Chain Management - hoofdplanning |
| **Implementatieoptie**              | Alleen Cloud. Planningsoptimalisatie wordt niet ondersteund voor on-premises implementaties. |
| **Status**                         | Afgeschaft. Per 1 april 2022 zullen productiescenario's niet langer worden ondersteund voor de ingebouwde hoofdplanningsengine van Supply Chain Management. Vanaf die datum zal Microsoft alle actieve ontwikkeling van productiescenario's voor de ingebouwde planningsengine stoppen, geen nieuwe functies meer vrijgeven en alleen kritieke fouten herstellen. Na die datum moeten alle bedrijven die ondersteuning nodig hebben voor productiescenario's, Planningsoptimalisatie gebruiken voor de berekening van de hoofdplanning. Planningsoptimalisatie zal naar verwachting productiescenario's volledig ondersteunen vanaf oktober 2022. Zie [documentatie voor Planningsoptimalisatie](../master-planning/planning-optimization/planning-optimization-overview.md) voor meer informatie.<br><br>Bedrijven met on-premises implementaties van Supply Chain Management kunnen de ingebouwde hoofdplanningsengine van blijven gebruiken voor productiescenario's na april 2022. Er zullen echter geen functieuitbreidingen meer worden aangeboden. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Verwijderde of verouderde functies in versie 10.0.11 van Supply Chain Management

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Gebruik van ingebouwde hoofdplanningsengine voor Supply Chain Management voor distributiescenario's

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Voor betere prestaties en een minimale belasting van de SQL-database tijdens de uitvoering van hoofdplanningen, wordt de ingebouwde engine voor de hoofdplanning van Supply Chain Management vervangen door Planningsoptimalisatie. Met Planningsoptimalisatie kunnen snel planningen worden uitgevoerd, zelfs tijdens kantooruren. Hierdoor kunnen planners direct reageren op wijzigingen in vraag- of planningsparameters. |
| **Vervangen door een andere functie?**   | Ja, Planningsoptimalisatie vervangt de bestaande ingebouwde Supply Chain Management-hoofdplanningsengine. |
| **Betrokken productgebieden**         | Supply Chain Management - hoofdplanning |
| **Implementatieoptie**              | Alleen Cloud. Planningsoptimalisatie wordt niet ondersteund voor on-premises implementaties. |
| **Status**                         | Afgeschaft. Per 1 april 2021 zullen distributiescenario's niet langer worden ondersteund met de ingebouwde Dynamics 365 Supply Chain Management-hoofdplanningsengine. Voor distributiescenario's moeten klanten Planningsoptimalisatie gebruiken voor het berekenen van hoofdplanningen. Zie [documentatie voor Planningsoptimalisatie](../master-planning/planning-optimization/planning-optimization-overview.md) voor meer informatie. Klanten met on-premises implementaties van Dynamics 365 Supply Chain Management kunnen de hoofdplanningsengine van Supply Chain Management blijven gebruiken voor distributiescenario's na april 2021. Er zullen echter geen functieuitbreidingen meer worden aangeboden. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies

Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

