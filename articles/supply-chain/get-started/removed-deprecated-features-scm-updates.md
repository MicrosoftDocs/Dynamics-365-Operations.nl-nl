---
title: Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering in Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 2e41510f1f5810dde9683235384f89008f888471
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821268"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dit onderwerp wordt bijgewerkt zodra er nieuwe verwijderde of verouderde functies worden gedocumenteerd voor Dynamics 365 Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen.

> [!NOTE]
> Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://docs.microsoft.com/dynamics/s-e/). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Verwijderde of verouderde functies in versie 10.0.18 van Supply Chain Management

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations - Magazijnbeheer (de magazijn-app)

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Met ingang van april 2021 wordt *Dynamics 365 for Finance and Operations - Magazijnbeheer* (de magazijn-app) afgeschaft en wordt na april 2022 niet meer ondersteund. Het is nu vervangen door de *mobiele app Magazijnbeheer*, die werd uitgebracht met versie 10.0.17 van Supply Chain Management. De nieuwe app is een complete vervanging, maar maakt gebruik van hetzelfde onderliggende framework, waardoor migratie eenvoudig is. Indien nodig kunnen de twee apps naast elkaar worden gebruikt om gebruikers te helpen zich geleidelijk aan te passen terwijl ze de nieuwe app leren gebruiken.<br><br>Zie [Mobiele toepassing Magazijnbeheer](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) en [De mobiele app Magazijnbeheer installeren en verbinden](../warehousing/install-configure-warehouse-management-app.md) voor meer informatie over de mobiele app Magazijnbeheer. |
| **Vervangen door een andere functie?**   | Ja, vervangen door de nieuwe mobiele app Magazijnbeheer. |
| **Betrokken productgebieden**         | Supply Chain Management - magazijn-app |
| **Implementatieoptie**              | Cloud en on-premises |
| **Status**                         | Afgeschaft. De magazijn-app krijgt ondersteuning met fout- en beveiligingscorrecties, maar functieverbeteringen worden niet langer geleverd. Na april 2022 wordt de oude magazijn-app niet meer ondersteund en worden klanten gevraagd om over te stappen naar de nieuwe mobiele app Magazijnbeheer. De oude magazijn-app wordt vervolgens verwijderd uit de Microsoft Store en Google Play Store.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Verwijderde of verouderde functies in versie 10.0.15 van Supply Chain Management

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-ondersteuning voor Dynamics 365 is afgeschaft

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Met ingang van december 2020 wordt Microsoft Internet Explorer 11-ondersteuning voor alle Dynamics 365-producten afgeschaft en wordt Internet Explorer 11 na augustus 2021 niet meer ondersteund.<br><br>Dit heeft invloed op klanten die Dynamics 365-producten gebruiken die zijn ontworpen om via een Internet Explorer 11-interface te worden gebruikt. Na augustus 2021 wordt Internet Explorer 11 niet ondersteund voor dergelijke Dynamics 365-producten. |
| **Vervangen door een andere functie?**   | Wij raden klanten aan om overstappen op Microsoft Edge.|
| **Betrokken productgebieden**         | Alle Dynamics 365-producten |
| **Implementatieoptie**              | Alles|
| **Status**                         | Afgeschaft. Internet Explorer 11 wordt na augustus 2021 niet ondersteund.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Gebruik van ingebouwde hoofdplanningsengine voor Supply Chain Management voor productiescenario's

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Voor betere prestaties en een minimale belasting van de SQL-database tijdens de uitvoering van hoofdplanningen, wordt de ingebouwde engine voor de hoofdplanning van Supply Chain Management vervangen door Planningsoptimalisatie. Met Planningsoptimalisatie kunnen snel planningen worden uitgevoerd, zelfs tijdens kantooruren. Hierdoor kunnen planners direct reageren op wijzigingen in vraag- of planningsparameters. |
| **Vervangen door een andere functie?**   | Ja, Planningsoptimalisatie vervangt de bestaande ingebouwde Supply Chain Management-hoofdplanningsengine. |
| **Betrokken productgebieden**         | Supply Chain Management - hoofdplanning |
| **Implementatieoptie**              | Alleen Cloud. Planningsoptimalisatie wordt niet ondersteund voor on-premises implementaties. |
| **Status**                         | Afgeschaft. Per 1 oktober 2021 zullen productiescenario's niet langer worden ondersteund met de ingebouwde Dynamics 365 Supply Chain Management-hoofdplanningsengine. Voor productiescenario's moeten klanten Planningsoptimalisatie gebruiken voor het berekenen van hoofdplanningen. Zie [documentatie voor Planningsoptimalisatie](https://go.microsoft.com/fwlink/?linkid=2105830) voor meer informatie. Klanten met on-premises implementaties van Dynamics 365 Supply Chain Management kunnen de hoofdplanningsengine van Supply Chain Management blijven gebruiken voor productiescenario's na oktober 2021. Er zullen echter geen functieuitbreidingen meer worden aangeboden. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Verwijderde of verouderde functies in versie 10.0.11 van Supply Chain Management

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Gebruik van ingebouwde hoofdplanningsengine voor Supply Chain Management voor distributiescenario's

|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Voor betere prestaties en een minimale belasting van de SQL-database tijdens de uitvoering van hoofdplanningen, wordt de ingebouwde engine voor de hoofdplanning van Supply Chain Management vervangen door Planningsoptimalisatie. Met Planningsoptimalisatie kunnen snel planningen worden uitgevoerd, zelfs tijdens kantooruren. Hierdoor kunnen planners direct reageren op wijzigingen in vraag- of planningsparameters. |
| **Vervangen door een andere functie?**   | Ja, Planningsoptimalisatie vervangt de bestaande ingebouwde Supply Chain Management-hoofdplanningsengine. |
| **Betrokken productgebieden**         | Supply Chain Management - hoofdplanning |
| **Implementatieoptie**              | Alleen Cloud. Planningsoptimalisatie wordt niet ondersteund voor on-premises implementaties. |
| **Status**                         | Afgeschaft. Per 1 april 2021 zullen distributiescenario's niet langer worden ondersteund met de ingebouwde Dynamics 365 Supply Chain Management-hoofdplanningsengine. Voor distributiescenario's moeten klanten Planningsoptimalisatie gebruiken voor het berekenen van hoofdplanningen. Zie [documentatie voor Planningsoptimalisatie](https://go.microsoft.com/fwlink/?linkid=2105830) voor meer informatie. Klanten met on-premises implementaties van Dynamics 365 Supply Chain Management kunnen de hoofdplanningsengine van Supply Chain Management blijven gebruiken voor distributiescenario's na april 2021. Er zullen echter geen functieuitbreidingen meer worden aangeboden. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies

Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
