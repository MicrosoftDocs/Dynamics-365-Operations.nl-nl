---
title: Verwijderde of afgeschafte functies in Dynamics 365 Commerce
description: In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443913"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Verwijderde of afgeschafte functies in Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Commerce.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld om u de mogelijkheid te bieden voor uw eigen planning rekening te houden met deze verwijderingen en afschaffingen. 

> [!NOTE]
> Gedetailleerde informatie over objecten in Finance and Operations-apps is te vinden in de [Rapporten met technische naslaginformatie](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Verwijderde of verouderde functies in versie 10.0.11 van Commerce
### <a name="data-action-hooks"></a>Gegevensactie-hooks
|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De functie Gegevensactie-hooks is afgeschaft vanwege prestatieproblemen. |
| **Vervangen door een andere functie?**   | U wordt aangeraden [gegevensacties te overschrijven](../e-commerce-extensibility/data-action-overrides.md) om bedrijfslogica in de gegevensactielaag te wijzigen.|
| **Betrokken productgebieden**         | Uitbreidbaarheid van gegevensacties in e-commerce |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf versie 10.0.11. |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Verwijderde of verouderde functies in versie 10.0.10 van Commerce
### <a name="pos-operation-803---picking-and-receiving"></a>POS-bewerking 803 - Verzamelen en ontvangen
|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | De bewerkingen voor orderverzameling en ontvangst zijn verouderd vanwege een nieuwe bewerking. |
| **Vervangen door een andere functie?**   | Ja. Ze worden vervangen door twee nieuwe POS-bewerkingen: inkomende bewerking (804) en uitgaande bewerking (805).|
| **Betrokken productgebieden**         | Verkooppunttoepassing (POS) |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf release 10.0.10 worden voor de bewerking orderverzameling en ontvangst geen functie-updates meer ontvangen. Alleen kritieke fouten worden in toekomstige versies opgelost voor deze bewerking. Alle klanten wordt aangeraden om naar de nieuwe [inkomende bewerkingen](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) en [uitgaande transacties](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) over te stappen, die deel blijven uitmaken van onze productroutekaart voor de lange termijn. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Verwijderde of verouderde functies in versie 10.0.7 van Commerce
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities en GetAvailableInventoryNearby API's
|   |  |
|------------|--------------------|
| **Reden voor afschaffing/verwijdering** | Nieuwe geoptimaliseerde API's zijn gemaakt ter vervanging van de API's GetProductAvailabilities en GetAvailableInventoryNearby. |
| **Vervangen door een andere functie?**   | Ja: dit wordt vervangen door de API's GetEstimatedAvailability en GetEstimatedproductWarehouseAvailability. |
| **Betrokken productgebieden**         | SDK met e-Commerce-toepassing |
| **Implementatieoptie**              | Alle |
| **Status**                         | Afgeschaft: vanaf de release 10.0.7 wordt geen technische investering meer gedaan voor GetproductAvailabilities en GetAvailableInventoryNearby. Organisaties die deze API's gebruiken in hun e-Commerce-implementaties, moeten overstappen op de nieuwe API's GetEstimatedAvailability en GetEstimatedproductWarehouseAvailability en de [geoptimaliseerde berekeningsfunctie voor productbeschikbaarheid](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels) inschakelen.  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Eerdere aankondigingen over verwijderde of afgeschafte functies
Zie [Verwijderde of afgeschafte functies in eerdere versies](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json) voor meer informatie over functies die zijn verwijderd of vervangen in eerdere versies.
