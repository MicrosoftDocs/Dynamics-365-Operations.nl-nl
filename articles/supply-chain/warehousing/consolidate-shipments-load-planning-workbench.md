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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 396a038dbf2f4b6835ecbb5fd8cb39a3a3608af7
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383746"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="a458c-103">Zendingen consolideren met Vrijgave naar magazijn vanuit de workbench voor ladingplanning</span><span class="sxs-lookup"><span data-stu-id="a458c-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a458c-104">Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde lading en vervolgens automatisch worden geconsolideerd in zendingen.</span><span class="sxs-lookup"><span data-stu-id="a458c-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="a458c-105">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="a458c-105">Make demo data available</span></span>

<span data-ttu-id="a458c-106">Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="a458c-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a458c-107">Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="a458c-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="a458c-108">Consolidatiebeleid voor zendingen en productfilters instellen</span><span class="sxs-lookup"><span data-stu-id="a458c-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="a458c-109">In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="a458c-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="a458c-110">Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.</span><span class="sxs-lookup"><span data-stu-id="a458c-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="a458c-111">De verkooporders voor dit scenario maken</span><span class="sxs-lookup"><span data-stu-id="a458c-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="a458c-112">Maak eerst een verzameling verkooporders waarmee u kunt werken.</span><span class="sxs-lookup"><span data-stu-id="a458c-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="a458c-113">U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS).</span><span class="sxs-lookup"><span data-stu-id="a458c-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="a458c-114">Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a458c-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="a458c-115">Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="a458c-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="a458c-116">Orderset 1 maken</span><span class="sxs-lookup"><span data-stu-id="a458c-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="a458c-117">Verkooporder 1-1</span><span class="sxs-lookup"><span data-stu-id="a458c-117">Sales order 1-1</span></span>

1. <span data-ttu-id="a458c-118">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a458c-119">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a458c-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a458c-120">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a458c-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a458c-121">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-122">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-123">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-124">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="a458c-125">Verkooporder 1-2</span><span class="sxs-lookup"><span data-stu-id="a458c-125">Sales order 1-2</span></span>

1. <span data-ttu-id="a458c-126">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a458c-127">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a458c-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a458c-128">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a458c-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a458c-129">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-130">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-131">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-132">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="a458c-133">Verkooporder 1-3</span><span class="sxs-lookup"><span data-stu-id="a458c-133">Sales order 1-3</span></span>

1. <span data-ttu-id="a458c-134">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a458c-135">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a458c-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a458c-136">**Leveringsmethode:** *10*</span><span class="sxs-lookup"><span data-stu-id="a458c-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="a458c-137">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-138">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-139">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-140">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="a458c-141">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-142">**Artikelnummer:** *A0002* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-143">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="a458c-144">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a458c-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a458c-145">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="a458c-146">Orderset 2 maken</span><span class="sxs-lookup"><span data-stu-id="a458c-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="a458c-147">Verkooporders 2-1 en 2-2</span><span class="sxs-lookup"><span data-stu-id="a458c-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="a458c-148">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a458c-149">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a458c-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="a458c-150">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-151">**Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="a458c-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="a458c-152">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-153">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="a458c-154">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-155">**Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="a458c-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="a458c-156">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="a458c-157">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a458c-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a458c-158">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="a458c-159">Orderset 3 maken</span><span class="sxs-lookup"><span data-stu-id="a458c-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="a458c-160">Verkooporders 3-1 en 3-2</span><span class="sxs-lookup"><span data-stu-id="a458c-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="a458c-161">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a458c-162">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a458c-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a458c-163">**Bestelopdracht van klant:** *1*</span><span class="sxs-lookup"><span data-stu-id="a458c-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="a458c-164">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-165">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-166">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-167">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="a458c-168">Verkooporders 3-3 en 3-4</span><span class="sxs-lookup"><span data-stu-id="a458c-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="a458c-169">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a458c-170">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a458c-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a458c-171">**Bestelopdracht van klant:** *2*</span><span class="sxs-lookup"><span data-stu-id="a458c-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="a458c-172">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-173">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-174">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-175">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="a458c-176">Orderset 4 maken</span><span class="sxs-lookup"><span data-stu-id="a458c-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="a458c-177">Verkooporders 4-1 en 4-2</span><span class="sxs-lookup"><span data-stu-id="a458c-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="a458c-178">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a458c-179">**Klantrekening:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="a458c-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="a458c-180">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-181">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-182">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-183">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="a458c-184">Verkooporders 4-3 en 4-4</span><span class="sxs-lookup"><span data-stu-id="a458c-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="a458c-185">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a458c-186">**Klantrekening:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="a458c-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="a458c-187">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-188">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-189">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-190">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="a458c-191">Verkooporders 4-5 en 4-6</span><span class="sxs-lookup"><span data-stu-id="a458c-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="a458c-192">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a458c-193">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a458c-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="a458c-194">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="a458c-194">**Site:** *6*</span></span>
    - <span data-ttu-id="a458c-195">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="a458c-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a458c-196">**Groep:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="a458c-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="a458c-197">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-198">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-199">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-200">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="a458c-201">Verkooporders 4-7 en 4-8</span><span class="sxs-lookup"><span data-stu-id="a458c-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="a458c-202">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="a458c-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a458c-203">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a458c-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="a458c-204">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="a458c-204">**Site:** *6*</span></span>
    - <span data-ttu-id="a458c-205">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="a458c-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a458c-206">**Groep:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="a458c-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="a458c-207">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="a458c-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a458c-208">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="a458c-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a458c-209">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a458c-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a458c-210">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="a458c-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="a458c-211">De workbench voor ladingplanning gebruiken om ladingen te maken en deze vrij te geven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="a458c-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="a458c-212">Voer de volgende stappen uit om een lading te maken voor elke orderset die u voor dit scenario hebt gemaakt en deze vervolgens vrij te geven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="a458c-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="a458c-213">Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="a458c-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="a458c-214">Op het tabblad **Verkoopregels** zoekt en selecteert u alle verkooporderregels uit een van de ordersets die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a458c-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="a458c-215">Selecteer in het actievenster op het tabblad **Vraag en aanbod** de optie **Toevoegen \> Aan nieuwe lading** om de geselecteerde orderregels aan een nieuwe lading toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="a458c-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="a458c-216">Selecteer in het dialoogvenster **Ladingsjabloon toewijzen** in het veld **Ladingsjabloon-id** een ladingssjabloon, zoals *Standaardladingssjabloon*.</span><span class="sxs-lookup"><span data-stu-id="a458c-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="a458c-217">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="a458c-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="a458c-218">In de sectie **Ladingen** zoekt en selecteert u de lading die u net hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a458c-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="a458c-219">Selecteer **Vrijgeven \>Vrijgave naar magazijn** om de geselecteerde lading vrij te geven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="a458c-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="a458c-220">Herhaal deze procedure voor de drie overige ordersets die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a458c-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="a458c-221">De zendingen verifiëren</span><span class="sxs-lookup"><span data-stu-id="a458c-221">Verify the shipments</span></span>

<span data-ttu-id="a458c-222">Met de volgende procedure kunt u de zendingen controleren die zijn gemaakt of bijgewerkt als gevolg van een zendingsconsolidatie.</span><span class="sxs-lookup"><span data-stu-id="a458c-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="a458c-223">Gebruik deze om alle ordersets te controleren die u voor dit scenario hebt gemaakt en bekijk vervolgens de subsecties die volgen om te controleren of u de verwachte resultaten hebt verkregen.</span><span class="sxs-lookup"><span data-stu-id="a458c-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="a458c-224">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="a458c-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="a458c-225">Zoek en selecteer de vereiste zending.</span><span class="sxs-lookup"><span data-stu-id="a458c-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="a458c-226">Als een consolidatiebeleid is gebruikt bij het maken of bijwerken van de zending, wordt dit weergegeven in het veld **Consolidatiebeleid voor zendingen**.</span><span class="sxs-lookup"><span data-stu-id="a458c-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="a458c-227">Orderset 1 vrijgeven in één lading</span><span class="sxs-lookup"><span data-stu-id="a458c-227">Release order set 1 in one load</span></span>

<span data-ttu-id="a458c-228">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="a458c-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="a458c-229">De eerste zending bevat drie regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="a458c-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="a458c-230">De tweede zending, die geen gebruikmaakt van de leveringsmethode *Airways*, is gemaakt met het consolidatiebeleid voor zending *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="a458c-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="a458c-231">Orderset 2 vrijgeven in één lading</span><span class="sxs-lookup"><span data-stu-id="a458c-231">Release order set 2 in one load</span></span>

<span data-ttu-id="a458c-232">Er moeten drie zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="a458c-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="a458c-233">De eerste zending bevat de items van het type *Ontvlambaar*.</span><span class="sxs-lookup"><span data-stu-id="a458c-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="a458c-234">Elk van de twee overige zendingen bevat één regel met het item *Explosief*.</span><span class="sxs-lookup"><span data-stu-id="a458c-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="a458c-235">Orderset 3 vrijgeven in één lading</span><span class="sxs-lookup"><span data-stu-id="a458c-235">Release order set 3 in one load</span></span>

<span data-ttu-id="a458c-236">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="a458c-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="a458c-237">De eerste zending bevat orderregels uit de verkooporder waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*.</span><span class="sxs-lookup"><span data-stu-id="a458c-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="a458c-238">De tweede zending bevat orderregels uit verkooporders waarvoor het veld **Bestelopdracht van klant** is ingesteld op *2*.</span><span class="sxs-lookup"><span data-stu-id="a458c-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="a458c-239">Orderset 4 vrijgeven in één lading</span><span class="sxs-lookup"><span data-stu-id="a458c-239">Release order set 4 in one load</span></span>

<span data-ttu-id="a458c-240">Er moeten vier zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="a458c-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="a458c-241">Regels van twee orders voor klantrekening *US-003* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="a458c-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a458c-242">Regels van twee orders voor klantrekening *US-004* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="a458c-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a458c-243">Regels van verkooporders 4-5 en 4-6 voor klantrekening *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="a458c-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a458c-244">Regels van verkooporders 4-7 en 4-8 voor klantrekening *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="a458c-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a458c-245">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="a458c-245">Additional resources</span></span>

- [<span data-ttu-id="a458c-246">Beleidsregels voor consolidatie van zendingen</span><span class="sxs-lookup"><span data-stu-id="a458c-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="a458c-247">Consolidatiebeleid voor zendingen configureren</span><span class="sxs-lookup"><span data-stu-id="a458c-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
