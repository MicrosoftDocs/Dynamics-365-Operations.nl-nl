---
title: Voorraadbeschikbaarheid in Twee keer wegschrijven
description: Dit onderwerp biedt informatie over het controleren van de voorraadbeschikbaarheid in Twee keer wegschrijven.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 48e54c043967ea5db15938857bd8f020dd4dfc64
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566734"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="1795e-103">Voorraadbeschikbaarheid in Twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="1795e-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1795e-104">Op basis van voorraadbeschikbaarheid kunt u uw voorraad controleren voordat u een product toevoegt aan de pagina **Offertes**, **Orders** of **Facturen** in Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="1795e-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="1795e-105">Het controleren van de voorraad en het bepalen van een afhandelingsdatum zijn bijvoorbeeld belangrijke taken in het proces [Prospect naar contant geld](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="1795e-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="1795e-106">Als u niet voldoende voorraad hebt, kunt u een leveringsdatum schatten op basis van verwachte voorraadontvangsten en -uitgiften.</span><span class="sxs-lookup"><span data-stu-id="1795e-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="1795e-107">U kunt ook de ATP-informatie (available to promise) van het product controleren, waar u de ATP-hoeveelheid kunt vinden in de vooraf gedefinieerde time fence.</span><span class="sxs-lookup"><span data-stu-id="1795e-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="1795e-108">Terhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="1795e-108">On-hand inventory</span></span>

<span data-ttu-id="1795e-109">In de koptekst van de pagina's **Offertes**, **Orders** en **Facturen** in Dynamics 365 Sales wordt een nieuwe knop **Voorhanden voorraad** toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="1795e-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="1795e-110">Wanneer u deze knop selecteert, wordt er een dialoogvenster weergegeven waarin u kunt het bedrijf en het product kunt opgeven waarvoor u de voorhanden voorraad wilt controleren.</span><span class="sxs-lookup"><span data-stu-id="1795e-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="1795e-111">In dit dialoogvenster wordt dezelfde informatie weergegeven als [voorhanden voorraad](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="1795e-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="1795e-112">In het dialoogvenster worden de voorraadgegevens opgehaald uit Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1795e-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1795e-113">Deze informatie bevat de volgende hoeveelheden:</span><span class="sxs-lookup"><span data-stu-id="1795e-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="1795e-114">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-114">On-hand quantity</span></span>
- <span data-ttu-id="1795e-115">Gereserveerde voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="1795e-116">Beschikbare voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-116">Available on-hand quantity</span></span>
- <span data-ttu-id="1795e-117">Bestelde hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-117">Ordered quantity</span></span>
- <span data-ttu-id="1795e-118">Hoeveelheid in bestelling</span><span class="sxs-lookup"><span data-stu-id="1795e-118">On-order quantity</span></span>
- <span data-ttu-id="1795e-119">Gereserveerde bestelde hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="1795e-120">Totale beschikbare hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="1795e-121">ATP-informatie</span><span class="sxs-lookup"><span data-stu-id="1795e-121">ATP information</span></span>

<span data-ttu-id="1795e-122">In Sales is een nieuwe knop **ATP-informatie** toegevoegd aan regelartikelen op de pagina's **Offertes**, **Orders** en **Facturen**.</span><span class="sxs-lookup"><span data-stu-id="1795e-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="1795e-123">Wanneer u deze knop selecteert, wordt er een dialoogvenster weergegeven waarin u het bedrijf, het product, de voorraadvestiging, het voorraadmagazijn en de bestelhoeveelheid kunt opgeven.</span><span class="sxs-lookup"><span data-stu-id="1795e-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="1795e-124">Dit dialoogvenster heeft dezelfde instellingen als worden beschreven bij [Orderbelofte](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="1795e-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="1795e-125">In het dialoogvenster worden de ATP-gegevens uit Supply Chain Management geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="1795e-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="1795e-126">Deze informatie bevat de volgende hoeveelheden:</span><span class="sxs-lookup"><span data-stu-id="1795e-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="1795e-127">ATP-hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-127">ATP quantity</span></span>
- <span data-ttu-id="1795e-128">Ontvangsthoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-128">Receipt quantity</span></span>
- <span data-ttu-id="1795e-129">Uitgiftehoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-129">Issue quantity</span></span>
- <span data-ttu-id="1795e-130">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="1795e-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="1795e-131">Hoe het werkt</span><span class="sxs-lookup"><span data-stu-id="1795e-131">How it works</span></span>

<span data-ttu-id="1795e-132">Wanneer u de knop **Voorhanden voorraad** selecteert op de pagina **Offertes**, **Orders** of **Facturen**, wordt er een live oproep voor twee keer wegschrijven gedaan naar de API **Voorhanden voorraad**.</span><span class="sxs-lookup"><span data-stu-id="1795e-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="1795e-133">De API berekent de voor het opgegeven product voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="1795e-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="1795e-134">Het resultaat wordt opgeslagen in de tabellen **InventCDSInventoryOnHandRequestEntity** en **InventCDSInventoryOnHandEntryEntity** en wordt vervolgens naar Dataverse geschreven door twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="1795e-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="1795e-135">Als u deze functionaliteit wilt gebruiken, moet u de volgende toewijzingen voor twee keer wegschrijven uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="1795e-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="1795e-136">Sla initiële synchronisatie over wanneer u de toewijzingen uitvoert.</span><span class="sxs-lookup"><span data-stu-id="1795e-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="1795e-137">Invoer van voorhanden voorraad voor CDS (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="1795e-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="1795e-138">Aanvragen voor voorhanden voorraad voor CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="1795e-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="1795e-139">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="1795e-139">Templates</span></span>
<span data-ttu-id="1795e-140">De volgende sjablonen zijn beschikbaar voor het weergeven van de voorhanden voorraadgegevens.</span><span class="sxs-lookup"><span data-stu-id="1795e-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="1795e-141">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="1795e-141">Finance and Operations apps</span></span> | <span data-ttu-id="1795e-142">Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="1795e-142">Customer engagement app</span></span> | <span data-ttu-id="1795e-143">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="1795e-143">Description</span></span> 
---|---|---
[<span data-ttu-id="1795e-144">Vermeldingen voorhanden CDS-voorraad</span><span class="sxs-lookup"><span data-stu-id="1795e-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="1795e-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="1795e-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="1795e-146">Aanvragen voorhanden CDS-voorraad</span><span class="sxs-lookup"><span data-stu-id="1795e-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="1795e-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="1795e-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="1795e-148">Invoer van voorhanden voorraad voor CDS (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="1795e-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="1795e-149">Deze sjabloon synchroniseert gegevens tussen Finance and Operations-apps en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1795e-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="1795e-150">Finance and Operations-veld</span><span class="sxs-lookup"><span data-stu-id="1795e-150">Finance and Operations field</span></span> | <span data-ttu-id="1795e-151">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="1795e-151">Map type</span></span> | <span data-ttu-id="1795e-152">Customer Engagement-veld</span><span class="sxs-lookup"><span data-stu-id="1795e-152">Customer engagement field</span></span> | <span data-ttu-id="1795e-153">Standaardwaarde</span><span class="sxs-lookup"><span data-stu-id="1795e-153">Default value</span></span>
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

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="1795e-154">Aanvragen voor voorhanden voorraad voor CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="1795e-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="1795e-155">Deze sjabloon synchroniseert gegevens tussen Finance and Operations-apps en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1795e-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="1795e-156">Finance and Operations-veld</span><span class="sxs-lookup"><span data-stu-id="1795e-156">Finance and Operations field</span></span> | <span data-ttu-id="1795e-157">Toewijzingstype</span><span class="sxs-lookup"><span data-stu-id="1795e-157">Map type</span></span> | <span data-ttu-id="1795e-158">Customer Engagement-veld</span><span class="sxs-lookup"><span data-stu-id="1795e-158">Customer engagement field</span></span> | <span data-ttu-id="1795e-159">Standaardwaarde</span><span class="sxs-lookup"><span data-stu-id="1795e-159">Default value</span></span>
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