---
title: Zendingen consolideren met de workbench voor het consolideren van zendingen
description: Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd in zendingen via de workbench voor het consolideren van zendingen.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9d0a2671e18603f701d343a4150128a04c626952
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963380"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="20323-103">Zendingen consolideren met de workbench voor het consolideren van zendingen</span><span class="sxs-lookup"><span data-stu-id="20323-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20323-104">Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd in zendingen via de workbench voor het consolideren van zendingen.</span><span class="sxs-lookup"><span data-stu-id="20323-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="20323-105">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="20323-105">Make demo data available</span></span>

<span data-ttu-id="20323-106">Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="20323-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="20323-107">Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="20323-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="20323-108">Consolidatiebeleid voor zendingen en productfilters instellen</span><span class="sxs-lookup"><span data-stu-id="20323-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="20323-109">In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="20323-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="20323-110">Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.</span><span class="sxs-lookup"><span data-stu-id="20323-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="20323-111">De functie voor handmatige zendingsconsolidatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="20323-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="20323-112">Voordat u de functie *Handmatige zendingsconsolidatie* kunt gebruiken, moet u deze in het systeem inschakelen.</span><span class="sxs-lookup"><span data-stu-id="20323-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="20323-113">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="20323-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="20323-114">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="20323-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="20323-115">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="20323-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="20323-116">**Functienaam:** *Handmatige zendingsconsolidatie*</span><span class="sxs-lookup"><span data-stu-id="20323-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="20323-117">Zoals vermeld in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md), moet u ook de functie *Zending consolideren* inschakelen voordat u beleid kunt maken.</span><span class="sxs-lookup"><span data-stu-id="20323-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="20323-118">U moet die stap echter al hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="20323-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="20323-119">De verkooporders voor dit scenario maken</span><span class="sxs-lookup"><span data-stu-id="20323-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="20323-120">Maak eerst een verzameling verkooporders waarmee u kunt werken.</span><span class="sxs-lookup"><span data-stu-id="20323-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="20323-121">U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS).</span><span class="sxs-lookup"><span data-stu-id="20323-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="20323-122">Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="20323-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="20323-123">Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="20323-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="20323-124">Orderset 1 maken</span><span class="sxs-lookup"><span data-stu-id="20323-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="20323-125">Verkooporders 1-1 en 1-2</span><span class="sxs-lookup"><span data-stu-id="20323-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="20323-126">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="20323-127">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="20323-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="20323-128">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="20323-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="20323-129">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-130">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-131">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-132">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="20323-133">Verkooporder 1-3</span><span class="sxs-lookup"><span data-stu-id="20323-133">Sales order 1-3</span></span>

1. <span data-ttu-id="20323-134">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="20323-135">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="20323-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="20323-136">**Leveringsmethode:** *10*</span><span class="sxs-lookup"><span data-stu-id="20323-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="20323-137">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-138">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-139">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-140">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="20323-141">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-142">**Artikelnummer:** *A0002* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-143">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="20323-144">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="20323-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="20323-145">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="20323-146">Orderset 2 maken</span><span class="sxs-lookup"><span data-stu-id="20323-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="20323-147">Verkooporders 2-1 en 2-2</span><span class="sxs-lookup"><span data-stu-id="20323-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="20323-148">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="20323-149">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="20323-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="20323-150">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="20323-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="20323-151">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-152">**Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="20323-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="20323-153">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-154">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="20323-155">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-156">**Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="20323-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="20323-157">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="20323-158">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="20323-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="20323-159">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="20323-160">Orderset 3 maken</span><span class="sxs-lookup"><span data-stu-id="20323-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="20323-161">Verkooporders 3-1 en 3-2</span><span class="sxs-lookup"><span data-stu-id="20323-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="20323-162">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="20323-163">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="20323-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="20323-164">**Bestelopdracht van klant:** *1*</span><span class="sxs-lookup"><span data-stu-id="20323-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="20323-165">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-166">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-167">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-168">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="20323-169">Verkooporders 3-3 en 3-4</span><span class="sxs-lookup"><span data-stu-id="20323-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="20323-170">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="20323-171">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="20323-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="20323-172">**Bestelopdracht van klant:** *2*</span><span class="sxs-lookup"><span data-stu-id="20323-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="20323-173">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-174">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-175">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-176">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="20323-177">Orderset 4 maken</span><span class="sxs-lookup"><span data-stu-id="20323-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="20323-178">Verkooporders 4-1 en 4-2</span><span class="sxs-lookup"><span data-stu-id="20323-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="20323-179">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="20323-180">**Klantrekening:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="20323-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="20323-181">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-182">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-183">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-184">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="20323-185">Verkooporders 4-3 en 4-4</span><span class="sxs-lookup"><span data-stu-id="20323-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="20323-186">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="20323-187">**Klantrekening:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="20323-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="20323-188">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-189">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-190">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-191">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="20323-192">Verkooporders 4-5 en 4-6</span><span class="sxs-lookup"><span data-stu-id="20323-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="20323-193">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="20323-194">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="20323-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="20323-195">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="20323-195">**Site:** *6*</span></span>
    - <span data-ttu-id="20323-196">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="20323-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="20323-197">**Groep:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="20323-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="20323-198">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-199">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-200">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-201">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="20323-202">Verkooporders 4-7 en 4-8</span><span class="sxs-lookup"><span data-stu-id="20323-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="20323-203">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="20323-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="20323-204">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="20323-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="20323-205">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="20323-205">**Site:** *6*</span></span>
    - <span data-ttu-id="20323-206">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="20323-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="20323-207">**Groep:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="20323-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="20323-208">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="20323-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="20323-209">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="20323-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="20323-210">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="20323-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="20323-211">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="20323-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="20323-212">De orders vrijgeven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="20323-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="20323-213">Voer de volgende stappen uit om elke verkooporder die u voor dit scenario hebt gemaakt, vrij te geven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="20323-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="20323-214">Ga naar **Klanten \> Orders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="20323-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="20323-215">Zoek en selecteer de verkooporder om vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="20323-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="20323-216">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Acties \> Vrijgave naar magazijn** om de geselecteerde verkooporder vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="20323-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="20323-217">Herhaal deze procedure voor elke andere verkooporder die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="20323-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="20323-218">De zendingen consolideren met de workbench voor het consolideren van zendingen</span><span class="sxs-lookup"><span data-stu-id="20323-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="20323-219">Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Workbench zendingsconsolidatie**.</span><span class="sxs-lookup"><span data-stu-id="20323-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="20323-220">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="20323-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="20323-221">Selecteer in de het dialoogvenster van de query-editor op het tabblad **Bereik** de optie **Toevoegen** om een rij met de volgende instellingen aan het raster toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="20323-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="20323-222">**Tabel:** *Verkooporders*</span><span class="sxs-lookup"><span data-stu-id="20323-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="20323-223">**Veld:** *Verkooporder*</span><span class="sxs-lookup"><span data-stu-id="20323-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="20323-224">**Criteria:** voer een door komma's gescheiden lijst in van de verkoopordernummers voor elke orderset die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="20323-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="20323-225">Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="20323-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="20323-226">Selecteer in het actievenster de optie **Zendingen consolideren**.</span><span class="sxs-lookup"><span data-stu-id="20323-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="20323-227">Selecteer alle zendingen en selecteer in het actievenster de optie **Consolideren**.</span><span class="sxs-lookup"><span data-stu-id="20323-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="20323-228">De zendingen verifiëren</span><span class="sxs-lookup"><span data-stu-id="20323-228">Verify the shipments</span></span>

<span data-ttu-id="20323-229">Met de volgende procedure kunt u de zendingen controleren die zijn gemaakt of bijgewerkt als gevolg van een zendingsconsolidatie.</span><span class="sxs-lookup"><span data-stu-id="20323-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="20323-230">Gebruik deze om alle ordersets te controleren die u voor dit scenario hebt gemaakt en bekijk vervolgens de subsecties die volgen om te controleren of u de verwachte resultaten hebt verkregen.</span><span class="sxs-lookup"><span data-stu-id="20323-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="20323-231">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="20323-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="20323-232">Zoek en selecteer de vereiste zending.</span><span class="sxs-lookup"><span data-stu-id="20323-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="20323-233">Als een consolidatiebeleid is gebruikt bij het maken of bijwerken van de zending, wordt dit weergegeven in het veld **Consolidatiebeleid voor zendingen**.</span><span class="sxs-lookup"><span data-stu-id="20323-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="20323-234">Gerelateerde zendingen voor orderset 1</span><span class="sxs-lookup"><span data-stu-id="20323-234">Related shipments for order set 1</span></span>

<span data-ttu-id="20323-235">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="20323-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="20323-236">De eerste zending bevat drie regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="20323-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="20323-237">De tweede zending, die geen gebruikmaakt van de leveringsmethode *Airways*, is gemaakt met het consolidatiebeleid voor zending *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="20323-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="20323-238">Gerelateerde zendingen voor orderset 2</span><span class="sxs-lookup"><span data-stu-id="20323-238">Related shipments for order set 2</span></span>

<span data-ttu-id="20323-239">Er moeten drie zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="20323-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="20323-240">De eerste zending bevat items van het type *Ontvlambaar*.</span><span class="sxs-lookup"><span data-stu-id="20323-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="20323-241">Elk van de twee overige zendingen bevat één regel met het item *Explosief*.</span><span class="sxs-lookup"><span data-stu-id="20323-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="20323-242">Gerelateerde zendingen voor orderset 3</span><span class="sxs-lookup"><span data-stu-id="20323-242">Related shipments for order set 3</span></span>

<span data-ttu-id="20323-243">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="20323-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="20323-244">De eerste zending bevat orderregels uit de verkooporder waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*.</span><span class="sxs-lookup"><span data-stu-id="20323-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="20323-245">De tweede zending bevat orderregels uit verkooporders waarvoor het veld **Bestelopdracht van klant** is ingesteld op *2*.</span><span class="sxs-lookup"><span data-stu-id="20323-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="20323-246">Gerelateerde zendingen voor orderset 4</span><span class="sxs-lookup"><span data-stu-id="20323-246">Related shipments for order set 4</span></span>

<span data-ttu-id="20323-247">Er moeten vier zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="20323-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="20323-248">Regels van twee orders voor klant *US-003* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="20323-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="20323-249">Regels van twee orders voor klant *US-004* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="20323-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="20323-250">Regels van verkooporders 4-5 en 4-6 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="20323-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="20323-251">Regels van verkooporders 4-7 en 4-8 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="20323-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20323-252">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="20323-252">Additional resources</span></span>

- [<span data-ttu-id="20323-253">Beleidsregels voor consolidatie van zendingen</span><span class="sxs-lookup"><span data-stu-id="20323-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="20323-254">Consolidatiebeleid voor zendingen configureren</span><span class="sxs-lookup"><span data-stu-id="20323-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
