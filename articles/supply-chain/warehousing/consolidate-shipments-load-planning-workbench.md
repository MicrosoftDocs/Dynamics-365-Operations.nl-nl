---
title: Zendingen consolideren met Vrijgave naar magazijn vanuit de workbench voor ladingplanning
description: Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde lading en vervolgens automatisch worden geconsolideerd in zendingen.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: c0af6764742532cbe181c8a20e7bf783b0e6d7cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983086"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="483d4-103">Zendingen consolideren met Vrijgave naar magazijn vanuit de workbench voor ladingplanning</span><span class="sxs-lookup"><span data-stu-id="483d4-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="483d4-104">Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde lading en vervolgens automatisch worden geconsolideerd in zendingen.</span><span class="sxs-lookup"><span data-stu-id="483d4-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="483d4-105">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="483d4-105">Make demo data available</span></span>

<span data-ttu-id="483d4-106">Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="483d4-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="483d4-107">Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="483d4-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="483d4-108">Consolidatiebeleid voor zendingen en productfilters instellen</span><span class="sxs-lookup"><span data-stu-id="483d4-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="483d4-109">In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="483d4-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="483d4-110">Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.</span><span class="sxs-lookup"><span data-stu-id="483d4-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="483d4-111">De verkooporders voor dit scenario maken</span><span class="sxs-lookup"><span data-stu-id="483d4-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="483d4-112">Maak eerst een verzameling verkooporders waarmee u kunt werken.</span><span class="sxs-lookup"><span data-stu-id="483d4-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="483d4-113">U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS).</span><span class="sxs-lookup"><span data-stu-id="483d4-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="483d4-114">Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="483d4-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="483d4-115">Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="483d4-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="483d4-116">Orderset 1 maken</span><span class="sxs-lookup"><span data-stu-id="483d4-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="483d4-117">Verkooporder 1-1</span><span class="sxs-lookup"><span data-stu-id="483d4-117">Sales order 1-1</span></span>

1. <span data-ttu-id="483d4-118">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="483d4-119">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="483d4-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="483d4-120">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="483d4-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="483d4-121">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-122">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-123">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-124">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="483d4-125">Verkooporder 1-2</span><span class="sxs-lookup"><span data-stu-id="483d4-125">Sales order 1-2</span></span>

1. <span data-ttu-id="483d4-126">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="483d4-127">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="483d4-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="483d4-128">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="483d4-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="483d4-129">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-130">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-131">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-132">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="483d4-133">Verkooporder 1-3</span><span class="sxs-lookup"><span data-stu-id="483d4-133">Sales order 1-3</span></span>

1. <span data-ttu-id="483d4-134">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="483d4-135">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="483d4-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="483d4-136">**Leveringsmethode:** *10*</span><span class="sxs-lookup"><span data-stu-id="483d4-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="483d4-137">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-138">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-139">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-140">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="483d4-141">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-142">**Artikelnummer:** *A0002* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-143">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="483d4-144">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="483d4-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="483d4-145">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="483d4-146">Orderset 2 maken</span><span class="sxs-lookup"><span data-stu-id="483d4-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="483d4-147">Verkooporders 2-1 en 2-2</span><span class="sxs-lookup"><span data-stu-id="483d4-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="483d4-148">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="483d4-149">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="483d4-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="483d4-150">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-151">**Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="483d4-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="483d4-152">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-153">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="483d4-154">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-155">**Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="483d4-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="483d4-156">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="483d4-157">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="483d4-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="483d4-158">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="483d4-159">Orderset 3 maken</span><span class="sxs-lookup"><span data-stu-id="483d4-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="483d4-160">Verkooporders 3-1 en 3-2</span><span class="sxs-lookup"><span data-stu-id="483d4-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="483d4-161">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="483d4-162">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="483d4-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="483d4-163">**Bestelopdracht van klant:** *1*</span><span class="sxs-lookup"><span data-stu-id="483d4-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="483d4-164">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-165">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-166">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-167">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="483d4-168">Verkooporders 3-3 en 3-4</span><span class="sxs-lookup"><span data-stu-id="483d4-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="483d4-169">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="483d4-170">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="483d4-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="483d4-171">**Bestelopdracht van klant:** *2*</span><span class="sxs-lookup"><span data-stu-id="483d4-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="483d4-172">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-173">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-174">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-175">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="483d4-176">Orderset 4 maken</span><span class="sxs-lookup"><span data-stu-id="483d4-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="483d4-177">Verkooporders 4-1 en 4-2</span><span class="sxs-lookup"><span data-stu-id="483d4-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="483d4-178">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="483d4-179">**Klantrekening:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="483d4-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="483d4-180">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-181">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-182">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-183">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="483d4-184">Verkooporders 4-3 en 4-4</span><span class="sxs-lookup"><span data-stu-id="483d4-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="483d4-185">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="483d4-186">**Klantrekening:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="483d4-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="483d4-187">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-188">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-189">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-190">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="483d4-191">Verkooporders 4-5 en 4-6</span><span class="sxs-lookup"><span data-stu-id="483d4-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="483d4-192">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="483d4-193">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="483d4-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="483d4-194">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="483d4-194">**Site:** *6*</span></span>
    - <span data-ttu-id="483d4-195">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="483d4-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="483d4-196">**Groep:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="483d4-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="483d4-197">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-198">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-199">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-200">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="483d4-201">Verkooporders 4-7 en 4-8</span><span class="sxs-lookup"><span data-stu-id="483d4-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="483d4-202">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="483d4-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="483d4-203">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="483d4-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="483d4-204">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="483d4-204">**Site:** *6*</span></span>
    - <span data-ttu-id="483d4-205">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="483d4-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="483d4-206">**Groep:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="483d4-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="483d4-207">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="483d4-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="483d4-208">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="483d4-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="483d4-209">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="483d4-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="483d4-210">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="483d4-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="483d4-211">De workbench voor ladingplanning gebruiken om ladingen te maken en deze vrij te geven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="483d4-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="483d4-212">Voer de volgende stappen uit om een lading te maken voor elke orderset die u voor dit scenario hebt gemaakt en deze vervolgens vrij te geven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="483d4-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="483d4-213">Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="483d4-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="483d4-214">Op het tabblad **Verkoopregels** zoekt en selecteert u alle verkooporderregels uit een van de ordersets die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="483d4-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="483d4-215">Selecteer in het actievenster op het tabblad **Vraag en aanbod** de optie **Toevoegen \> Aan nieuwe lading** om de geselecteerde orderregels aan een nieuwe lading toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="483d4-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="483d4-216">Selecteer in het dialoogvenster **Ladingsjabloon toewijzen** in het veld **Ladingsjabloon-id** een ladingssjabloon, zoals *Standaardladingssjabloon*.</span><span class="sxs-lookup"><span data-stu-id="483d4-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="483d4-217">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="483d4-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="483d4-218">In de sectie **Ladingen** zoekt en selecteert u de lading die u net hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="483d4-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="483d4-219">Selecteer **Vrijgeven \>Vrijgave naar magazijn** om de geselecteerde lading vrij te geven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="483d4-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="483d4-220">Herhaal deze procedure voor de drie overige ordersets die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="483d4-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="483d4-221">De zendingen verifiëren</span><span class="sxs-lookup"><span data-stu-id="483d4-221">Verify the shipments</span></span>

<span data-ttu-id="483d4-222">Met de volgende procedure kunt u de zendingen controleren die zijn gemaakt of bijgewerkt als gevolg van een zendingsconsolidatie.</span><span class="sxs-lookup"><span data-stu-id="483d4-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="483d4-223">Gebruik deze om alle ordersets te controleren die u voor dit scenario hebt gemaakt en bekijk vervolgens de subsecties die volgen om te controleren of u de verwachte resultaten hebt verkregen.</span><span class="sxs-lookup"><span data-stu-id="483d4-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="483d4-224">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="483d4-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="483d4-225">Zoek en selecteer de vereiste zending.</span><span class="sxs-lookup"><span data-stu-id="483d4-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="483d4-226">Als een consolidatiebeleid is gebruikt bij het maken of bijwerken van de zending, wordt dit weergegeven in het veld **Consolidatiebeleid voor zendingen**.</span><span class="sxs-lookup"><span data-stu-id="483d4-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="483d4-227">Orderset 1 vrijgeven in één lading</span><span class="sxs-lookup"><span data-stu-id="483d4-227">Release order set 1 in one load</span></span>

<span data-ttu-id="483d4-228">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="483d4-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="483d4-229">De eerste zending bevat drie regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="483d4-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="483d4-230">De tweede zending, die geen gebruikmaakt van de leveringsmethode *Airways*, is gemaakt met het consolidatiebeleid voor zending *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="483d4-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="483d4-231">Orderset 2 vrijgeven in één lading</span><span class="sxs-lookup"><span data-stu-id="483d4-231">Release order set 2 in one load</span></span>

<span data-ttu-id="483d4-232">Er moeten drie zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="483d4-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="483d4-233">De eerste zending bevat de items van het type *Ontvlambaar*.</span><span class="sxs-lookup"><span data-stu-id="483d4-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="483d4-234">Elk van de twee overige zendingen bevat één regel met het item *Explosief*.</span><span class="sxs-lookup"><span data-stu-id="483d4-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="483d4-235">Orderset 3 vrijgeven in één lading</span><span class="sxs-lookup"><span data-stu-id="483d4-235">Release order set 3 in one load</span></span>

<span data-ttu-id="483d4-236">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="483d4-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="483d4-237">De eerste zending bevat orderregels uit de verkooporder waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*.</span><span class="sxs-lookup"><span data-stu-id="483d4-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="483d4-238">De tweede zending bevat orderregels uit verkooporders waarvoor het veld **Bestelopdracht van klant** is ingesteld op *2*.</span><span class="sxs-lookup"><span data-stu-id="483d4-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="483d4-239">Orderset 4 vrijgeven in één lading</span><span class="sxs-lookup"><span data-stu-id="483d4-239">Release order set 4 in one load</span></span>

<span data-ttu-id="483d4-240">Er moeten vier zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="483d4-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="483d4-241">Regels van twee orders voor klantrekening *US-003* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="483d4-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="483d4-242">Regels van twee orders voor klantrekening *US-004* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="483d4-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="483d4-243">Regels van verkooporders 4-5 en 4-6 voor klantrekening *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="483d4-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="483d4-244">Regels van verkooporders 4-7 en 4-8 voor klantrekening *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="483d4-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="483d4-245">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="483d4-245">Additional resources</span></span>

- [<span data-ttu-id="483d4-246">Beleidsregels voor consolidatie van zendingen</span><span class="sxs-lookup"><span data-stu-id="483d4-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="483d4-247">Consolidatiebeleid voor zendingen configureren</span><span class="sxs-lookup"><span data-stu-id="483d4-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
