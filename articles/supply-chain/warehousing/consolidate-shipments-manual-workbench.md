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
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b1a2c9506b4444fc98a9e4f0389cbd69db4ce052
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383745"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="47d1c-103">Zendingen consolideren met de workbench voor het consolideren van zendingen</span><span class="sxs-lookup"><span data-stu-id="47d1c-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47d1c-104">Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd in zendingen via de workbench voor het consolideren van zendingen.</span><span class="sxs-lookup"><span data-stu-id="47d1c-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="47d1c-105">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="47d1c-105">Make demo data available</span></span>

<span data-ttu-id="47d1c-106">Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="47d1c-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="47d1c-107">Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="47d1c-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="47d1c-108">Consolidatiebeleid voor zendingen en productfilters instellen</span><span class="sxs-lookup"><span data-stu-id="47d1c-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="47d1c-109">In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="47d1c-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="47d1c-110">Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.</span><span class="sxs-lookup"><span data-stu-id="47d1c-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="47d1c-111">De functie voor handmatige zendingsconsolidatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="47d1c-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="47d1c-112">Voordat u de functie *Handmatige zendingsconsolidatie* kunt gebruiken, moet u deze in het systeem inschakelen.</span><span class="sxs-lookup"><span data-stu-id="47d1c-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="47d1c-113">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="47d1c-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="47d1c-114">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="47d1c-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="47d1c-115">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="47d1c-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="47d1c-116">**Functienaam:** *Handmatige zendingsconsolidatie*</span><span class="sxs-lookup"><span data-stu-id="47d1c-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="47d1c-117">Zoals vermeld in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md), moet u ook de functie *Zending consolideren* inschakelen voordat u beleid kunt maken.</span><span class="sxs-lookup"><span data-stu-id="47d1c-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="47d1c-118">U moet die stap echter al hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="47d1c-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="47d1c-119">De verkooporders voor dit scenario maken</span><span class="sxs-lookup"><span data-stu-id="47d1c-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="47d1c-120">Maak eerst een verzameling verkooporders waarmee u kunt werken.</span><span class="sxs-lookup"><span data-stu-id="47d1c-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="47d1c-121">U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS).</span><span class="sxs-lookup"><span data-stu-id="47d1c-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="47d1c-122">Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="47d1c-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="47d1c-123">Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="47d1c-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="47d1c-124">Orderset 1 maken</span><span class="sxs-lookup"><span data-stu-id="47d1c-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="47d1c-125">Verkooporders 1-1 en 1-2</span><span class="sxs-lookup"><span data-stu-id="47d1c-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="47d1c-126">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="47d1c-127">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="47d1c-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="47d1c-128">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="47d1c-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="47d1c-129">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-130">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-131">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-132">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="47d1c-133">Verkooporder 1-3</span><span class="sxs-lookup"><span data-stu-id="47d1c-133">Sales order 1-3</span></span>

1. <span data-ttu-id="47d1c-134">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-135">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="47d1c-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="47d1c-136">**Leveringsmethode:** *10*</span><span class="sxs-lookup"><span data-stu-id="47d1c-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="47d1c-137">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-138">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-139">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-140">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="47d1c-141">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-142">**Artikelnummer:** *A0002* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-143">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="47d1c-144">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="47d1c-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="47d1c-145">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="47d1c-146">Orderset 2 maken</span><span class="sxs-lookup"><span data-stu-id="47d1c-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="47d1c-147">Verkooporders 2-1 en 2-2</span><span class="sxs-lookup"><span data-stu-id="47d1c-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="47d1c-148">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="47d1c-149">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="47d1c-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="47d1c-150">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="47d1c-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="47d1c-151">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-152">**Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="47d1c-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="47d1c-153">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-154">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="47d1c-155">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-156">**Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="47d1c-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="47d1c-157">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="47d1c-158">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="47d1c-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="47d1c-159">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="47d1c-160">Orderset 3 maken</span><span class="sxs-lookup"><span data-stu-id="47d1c-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="47d1c-161">Verkooporders 3-1 en 3-2</span><span class="sxs-lookup"><span data-stu-id="47d1c-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="47d1c-162">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="47d1c-163">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="47d1c-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="47d1c-164">**Bestelopdracht van klant:** *1*</span><span class="sxs-lookup"><span data-stu-id="47d1c-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="47d1c-165">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-166">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-167">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-168">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="47d1c-169">Verkooporders 3-3 en 3-4</span><span class="sxs-lookup"><span data-stu-id="47d1c-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="47d1c-170">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="47d1c-171">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="47d1c-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="47d1c-172">**Bestelopdracht van klant:** *2*</span><span class="sxs-lookup"><span data-stu-id="47d1c-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="47d1c-173">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-174">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-175">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-176">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="47d1c-177">Orderset 4 maken</span><span class="sxs-lookup"><span data-stu-id="47d1c-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="47d1c-178">Verkooporders 4-1 en 4-2</span><span class="sxs-lookup"><span data-stu-id="47d1c-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="47d1c-179">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="47d1c-180">**Klantrekening:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="47d1c-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="47d1c-181">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-182">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-183">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-184">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="47d1c-185">Verkooporders 4-3 en 4-4</span><span class="sxs-lookup"><span data-stu-id="47d1c-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="47d1c-186">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="47d1c-187">**Klantrekening:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="47d1c-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="47d1c-188">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-189">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-190">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-191">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="47d1c-192">Verkooporders 4-5 en 4-6</span><span class="sxs-lookup"><span data-stu-id="47d1c-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="47d1c-193">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="47d1c-194">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="47d1c-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="47d1c-195">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="47d1c-195">**Site:** *6*</span></span>
    - <span data-ttu-id="47d1c-196">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="47d1c-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="47d1c-197">**Groep:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="47d1c-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="47d1c-198">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-199">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-200">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-201">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="47d1c-202">Verkooporders 4-7 en 4-8</span><span class="sxs-lookup"><span data-stu-id="47d1c-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="47d1c-203">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="47d1c-204">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="47d1c-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="47d1c-205">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="47d1c-205">**Site:** *6*</span></span>
    - <span data-ttu-id="47d1c-206">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="47d1c-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="47d1c-207">**Groep:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="47d1c-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="47d1c-208">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="47d1c-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="47d1c-209">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="47d1c-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="47d1c-210">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="47d1c-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="47d1c-211">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="47d1c-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="47d1c-212">De orders vrijgeven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="47d1c-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="47d1c-213">Voer de volgende stappen uit om elke verkooporder die u voor dit scenario hebt gemaakt, vrij te geven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="47d1c-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="47d1c-214">Ga naar **Klanten \> Orders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="47d1c-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="47d1c-215">Zoek en selecteer de verkooporder om vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="47d1c-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="47d1c-216">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Acties \> Vrijgave naar magazijn** om de geselecteerde verkooporder vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="47d1c-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="47d1c-217">Herhaal deze procedure voor elke andere verkooporder die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="47d1c-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="47d1c-218">De zendingen consolideren met de workbench voor het consolideren van zendingen</span><span class="sxs-lookup"><span data-stu-id="47d1c-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="47d1c-219">Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Workbench zendingsconsolidatie**.</span><span class="sxs-lookup"><span data-stu-id="47d1c-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="47d1c-220">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="47d1c-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="47d1c-221">Selecteer in de het dialoogvenster van de query-editor op het tabblad **Bereik** de optie **Toevoegen** om een rij met de volgende instellingen aan het raster toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="47d1c-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="47d1c-222">**Tabel:** *Verkooporders*</span><span class="sxs-lookup"><span data-stu-id="47d1c-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="47d1c-223">**Veld:** *Verkooporder*</span><span class="sxs-lookup"><span data-stu-id="47d1c-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="47d1c-224">**Criteria:** voer een door komma's gescheiden lijst in van de verkoopordernummers voor elke orderset die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="47d1c-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="47d1c-225">Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="47d1c-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="47d1c-226">Selecteer in het actievenster de optie **Zendingen consolideren**.</span><span class="sxs-lookup"><span data-stu-id="47d1c-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="47d1c-227">Selecteer alle zendingen en selecteer in het actievenster de optie **Consolideren**.</span><span class="sxs-lookup"><span data-stu-id="47d1c-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="47d1c-228">De zendingen verifiëren</span><span class="sxs-lookup"><span data-stu-id="47d1c-228">Verify the shipments</span></span>

<span data-ttu-id="47d1c-229">Met de volgende procedure kunt u de zendingen controleren die zijn gemaakt of bijgewerkt als gevolg van een zendingsconsolidatie.</span><span class="sxs-lookup"><span data-stu-id="47d1c-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="47d1c-230">Gebruik deze om alle ordersets te controleren die u voor dit scenario hebt gemaakt en bekijk vervolgens de subsecties die volgen om te controleren of u de verwachte resultaten hebt verkregen.</span><span class="sxs-lookup"><span data-stu-id="47d1c-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="47d1c-231">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="47d1c-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="47d1c-232">Zoek en selecteer de vereiste zending.</span><span class="sxs-lookup"><span data-stu-id="47d1c-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="47d1c-233">Als een consolidatiebeleid is gebruikt bij het maken of bijwerken van de zending, wordt dit weergegeven in het veld **Consolidatiebeleid voor zendingen**.</span><span class="sxs-lookup"><span data-stu-id="47d1c-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="47d1c-234">Gerelateerde zendingen voor orderset 1</span><span class="sxs-lookup"><span data-stu-id="47d1c-234">Related shipments for order set 1</span></span>

<span data-ttu-id="47d1c-235">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="47d1c-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="47d1c-236">De eerste zending bevat drie regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="47d1c-237">De tweede zending, die geen gebruikmaakt van de leveringsmethode *Airways*, is gemaakt met het consolidatiebeleid voor zending *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="47d1c-238">Gerelateerde zendingen voor orderset 2</span><span class="sxs-lookup"><span data-stu-id="47d1c-238">Related shipments for order set 2</span></span>

<span data-ttu-id="47d1c-239">Er moeten drie zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="47d1c-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="47d1c-240">De eerste zending bevat items van het type *Ontvlambaar*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="47d1c-241">Elk van de twee overige zendingen bevat één regel met het item *Explosief*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="47d1c-242">Gerelateerde zendingen voor orderset 3</span><span class="sxs-lookup"><span data-stu-id="47d1c-242">Related shipments for order set 3</span></span>

<span data-ttu-id="47d1c-243">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="47d1c-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="47d1c-244">De eerste zending bevat orderregels uit de verkooporder waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="47d1c-245">De tweede zending bevat orderregels uit verkooporders waarvoor het veld **Bestelopdracht van klant** is ingesteld op *2*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="47d1c-246">Gerelateerde zendingen voor orderset 4</span><span class="sxs-lookup"><span data-stu-id="47d1c-246">Related shipments for order set 4</span></span>

<span data-ttu-id="47d1c-247">Er moeten vier zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="47d1c-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="47d1c-248">Regels van twee orders voor klant *US-003* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="47d1c-249">Regels van twee orders voor klant *US-004* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="47d1c-250">Regels van verkooporders 4-5 en 4-6 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="47d1c-251">Regels van verkooporders 4-7 en 4-8 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="47d1c-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47d1c-252">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="47d1c-252">Additional resources</span></span>

- [<span data-ttu-id="47d1c-253">Beleidsregels voor consolidatie van zendingen</span><span class="sxs-lookup"><span data-stu-id="47d1c-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="47d1c-254">Consolidatiebeleid voor zendingen configureren</span><span class="sxs-lookup"><span data-stu-id="47d1c-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)