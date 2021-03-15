---
title: Voorraadbeschikbaarheid in Twee keer wegschrijven
description: Dit onderwerp biedt informatie over het controleren van de voorraadbeschikbaarheid in Twee keer wegschrijven.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839544"
---
# <a name="inventory-availability-in-dual-write"></a>Voorraadbeschikbaarheid in Twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

Op basis van voorraadbeschikbaarheid kunt u uw voorraad controleren voordat u een product toevoegt aan de pagina **Offertes**, **Orders** of **Facturen** in Microsoft Dynamics 365 Sales. Het controleren van de voorraad en het bepalen van een afhandelingsdatum zijn bijvoorbeeld belangrijke taken in het proces [Prospect naar contant geld](dual-write-prospect-to-cash.md).

Als u niet voldoende voorraad hebt, kunt u een leveringsdatum schatten op basis van verwachte voorraadontvangsten en -uitgiften. U kunt ook de ATP-informatie (available to promise) van het product controleren, waar u de ATP-hoeveelheid kunt vinden in de vooraf gedefinieerde time fence.

## <a name="on-hand-inventory"></a>Terhanden voorraad

In de koptekst van de pagina's **Offertes**, **Orders** en **Facturen** in Dynamics 365 Sales wordt een nieuwe knop **Voorhanden voorraad** toegevoegd. Wanneer u deze knop selecteert, wordt er een dialoogvenster weergegeven waarin u kunt het bedrijf en het product kunt opgeven waarvoor u de voorhanden voorraad wilt controleren. In dit dialoogvenster wordt dezelfde informatie weergegeven als [voorhanden voorraad](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

In het dialoogvenster worden de voorraadgegevens opgehaald uit Dynamics 365 Supply Chain Management. Deze informatie bevat de volgende hoeveelheden:

- Voorhanden hoeveelheid
- Gereserveerde voorhanden hoeveelheid
- Beschikbare voorhanden hoeveelheid
- Bestelde hoeveelheid
- Hoeveelheid in bestelling
- Gereserveerde bestelde hoeveelheid
- Totale beschikbare hoeveelheid

## <a name="atp-information"></a>ATP-informatie

In Sales is een nieuwe knop **ATP-informatie** toegevoegd aan regelartikelen op de pagina's **Offertes**, **Orders** en **Facturen**. Wanneer u deze knop selecteert, wordt er een dialoogvenster weergegeven waarin u het bedrijf, het product, de voorraadvestiging, het voorraadmagazijn en de bestelhoeveelheid kunt opgeven. Dit dialoogvenster heeft dezelfde instellingen als worden beschreven bij [Orderbelofte](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

In het dialoogvenster worden de ATP-gegevens uit Supply Chain Management geretourneerd. Deze informatie bevat de volgende hoeveelheden:

- ATP-hoeveelheid
- Ontvangsthoeveelheid
- Uitgiftehoeveelheid
- Voorhanden hoeveelheid

## <a name="how-it-works"></a>Hoe het werkt

Wanneer u de knop **Voorhanden voorraad** selecteert op de pagina **Offertes**, **Orders** of **Facturen**, wordt er een live oproep voor twee keer wegschrijven gedaan naar de API **Voorhanden voorraad**. De API berekent de voor het opgegeven product voorhanden voorraad. Het resultaat wordt opgeslagen in de tabellen **InventCDSInventoryOnHandRequestEntity** en **InventCDSInventoryOnHandEntryEntity** en wordt vervolgens naar Dataverse geschreven door twee keer wegschrijven. Als u deze functionaliteit wilt gebruiken, moet u de volgende toewijzingen voor twee keer wegschrijven uitvoeren. Sla initiële synchronisatie over wanneer u de toewijzingen uitvoert.

- Invoer van voorhanden voorraad voor CDS (msdyn_inventoryonhandentries)
- Aanvragen voor voorhanden voorraad voor CDS (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Sjablonen
De volgende sjablonen zijn beschikbaar voor het weergeven van de voorhanden voorraadgegevens.

Finance and Operations-apps | Customer Engagement-app | Beschrijving 
---|---|---
[Vermeldingen voorhanden CDS-voorraad](#145) | msdyn_inventoryonhandentries |
[Aanvragen voorhanden CDS-voorraad](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>Invoer van voorhanden voorraad voor CDS (msdyn_inventoryonhandentries)

Deze sjabloon synchroniseert gegevens tussen Finance and Operations-apps en Dataverse.

Finance and Operations-veld | Toewijzingstype | Customer Engagement-veld | Standaardwaarde
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>Aanvragen voor voorhanden voorraad voor CDS (msdyn_inventoryonhandrequests)

Deze sjabloon synchroniseert gegevens tussen Finance and Operations-apps en Dataverse.

Finance and Operations-veld | Toewijzingstype | Customer Engagement-veld | Standaardwaarde
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]