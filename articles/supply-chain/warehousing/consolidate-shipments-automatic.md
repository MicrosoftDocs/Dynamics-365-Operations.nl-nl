---
title: Zendingen consolideren wanneer deze naar het magazijn worden vrijgegeven met Automatische vrijgave van verkooporders
description: Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde geautomatiseerde procedure voor het periodiek vrijgeven naar een magazijn.
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
ms.openlocfilehash: 373b6bf6219ef76bacef3c67a816aec4c084c405
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383743"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="eccfb-103">Zendingen consolideren wanneer deze naar het magazijn worden vrijgegeven met Automatische vrijgave van verkooporders</span><span class="sxs-lookup"><span data-stu-id="eccfb-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eccfb-104">Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde geautomatiseerde procedure voor het periodiek vrijgeven naar een magazijn.</span><span class="sxs-lookup"><span data-stu-id="eccfb-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="eccfb-105">De orders worden automatisch geconsolideerd in zendingen op basis van regels die zijn gedefinieerd als consolidatiebeleid voor zendingen.</span><span class="sxs-lookup"><span data-stu-id="eccfb-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="eccfb-106">Tijdens het scenario maakt u sets verkooporders en geeft u elke set vrij naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="eccfb-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="eccfb-107">U gaat vervolgens de zendingen bekijken die worden gemaakt of bijgewerkt tijdens de consolidatie van de zending, op basis van het geconfigureerde beleid.</span><span class="sxs-lookup"><span data-stu-id="eccfb-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="eccfb-108">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="eccfb-108">Make demo data available</span></span>

<span data-ttu-id="eccfb-109">Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="eccfb-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="eccfb-110">Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="eccfb-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="eccfb-111">Consolidatiebeleid voor zendingen en productfilters instellen</span><span class="sxs-lookup"><span data-stu-id="eccfb-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="eccfb-112">In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="eccfb-113">Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.</span><span class="sxs-lookup"><span data-stu-id="eccfb-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="eccfb-114">De verkooporders voor dit scenario maken</span><span class="sxs-lookup"><span data-stu-id="eccfb-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="eccfb-115">Maak eerst een verzameling verkooporders waarmee u kunt werken.</span><span class="sxs-lookup"><span data-stu-id="eccfb-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="eccfb-116">U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS).</span><span class="sxs-lookup"><span data-stu-id="eccfb-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="eccfb-117">Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eccfb-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="eccfb-118">Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="eccfb-119">Orderset 1 maken</span><span class="sxs-lookup"><span data-stu-id="eccfb-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="eccfb-120">Verkooporder 1-1</span><span class="sxs-lookup"><span data-stu-id="eccfb-120">Sales order 1-1</span></span>

1. <span data-ttu-id="eccfb-121">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-122">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="eccfb-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="eccfb-123">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="eccfb-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="eccfb-124">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-125">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-126">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="eccfb-127">Verkooporder 1-2</span><span class="sxs-lookup"><span data-stu-id="eccfb-127">Sales order 1-2</span></span>

1. <span data-ttu-id="eccfb-128">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-129">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="eccfb-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="eccfb-130">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="eccfb-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="eccfb-131">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-132">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-133">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="eccfb-134">Verkooporder 1-3</span><span class="sxs-lookup"><span data-stu-id="eccfb-134">Sales order 1-3</span></span>

1. <span data-ttu-id="eccfb-135">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-136">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="eccfb-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="eccfb-137">**Leveringsmethode:** *10*</span><span class="sxs-lookup"><span data-stu-id="eccfb-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="eccfb-138">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-139">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-140">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="eccfb-141">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-142">**Artikelnummer:** *A0002* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-143">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="eccfb-144">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="eccfb-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="eccfb-145">Orderset 2 maken</span><span class="sxs-lookup"><span data-stu-id="eccfb-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="eccfb-146">Verkooporders 2-1 en 2-2</span><span class="sxs-lookup"><span data-stu-id="eccfb-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="eccfb-147">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="eccfb-148">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="eccfb-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="eccfb-149">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-150">**Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="eccfb-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="eccfb-151">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="eccfb-152">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-153">**Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="eccfb-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="eccfb-154">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="eccfb-155">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="eccfb-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="eccfb-156">Orderset 3 maken</span><span class="sxs-lookup"><span data-stu-id="eccfb-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="eccfb-157">Verkooporder 3-1</span><span class="sxs-lookup"><span data-stu-id="eccfb-157">Sales order 3-1</span></span>

1. <span data-ttu-id="eccfb-158">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-159">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="eccfb-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="eccfb-160">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-161">**Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="eccfb-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="eccfb-162">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="eccfb-163">Voeg een tweede orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-164">**Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)</span><span class="sxs-lookup"><span data-stu-id="eccfb-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="eccfb-165">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="eccfb-166">**Leveringsmethode:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="eccfb-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="eccfb-167">Deze order is gelijk aan de twee orders die u hebt gemaakt voor orderset 2.</span><span class="sxs-lookup"><span data-stu-id="eccfb-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="eccfb-168">Deze wordt echter weergegeven als een eigen order omdat u deze later in dit scenario afzonderlijk vrijgeeft.</span><span class="sxs-lookup"><span data-stu-id="eccfb-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="eccfb-169">Orderset 4 maken</span><span class="sxs-lookup"><span data-stu-id="eccfb-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="eccfb-170">Verkooporder 4-1</span><span class="sxs-lookup"><span data-stu-id="eccfb-170">Sales order 4-1</span></span>

1. <span data-ttu-id="eccfb-171">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-172">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="eccfb-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="eccfb-173">**Bestelopdracht van klant:** *1*</span><span class="sxs-lookup"><span data-stu-id="eccfb-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="eccfb-174">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-175">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-176">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="eccfb-177">Orderset 5 maken</span><span class="sxs-lookup"><span data-stu-id="eccfb-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="eccfb-178">Verkooporders 5-1 en 5-2</span><span class="sxs-lookup"><span data-stu-id="eccfb-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="eccfb-179">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="eccfb-180">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="eccfb-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="eccfb-181">**Bestelopdracht van klant:** *2*</span><span class="sxs-lookup"><span data-stu-id="eccfb-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="eccfb-182">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-183">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-184">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="eccfb-185">Verkooporder 5-3</span><span class="sxs-lookup"><span data-stu-id="eccfb-185">Sales order 5-3</span></span>

1. <span data-ttu-id="eccfb-186">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-187">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="eccfb-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="eccfb-188">**Bestelopdracht van klant:** *1*</span><span class="sxs-lookup"><span data-stu-id="eccfb-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="eccfb-189">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-190">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-191">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="eccfb-192">Orderset 6 maken</span><span class="sxs-lookup"><span data-stu-id="eccfb-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="eccfb-193">Verkooporders 6-1 en 6-2</span><span class="sxs-lookup"><span data-stu-id="eccfb-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="eccfb-194">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="eccfb-195">**Klantrekening:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="eccfb-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="eccfb-196">**Bestelopdracht van klant:** *2*</span><span class="sxs-lookup"><span data-stu-id="eccfb-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="eccfb-197">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-198">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-199">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="eccfb-200">Verkooporders 6-3 en 6-4</span><span class="sxs-lookup"><span data-stu-id="eccfb-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="eccfb-201">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="eccfb-202">**Klantrekening:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="eccfb-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="eccfb-203">**Bestelopdracht van klant:** *1*</span><span class="sxs-lookup"><span data-stu-id="eccfb-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="eccfb-204">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-205">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-206">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="eccfb-207">Verkooporders 6-5 en 6-6</span><span class="sxs-lookup"><span data-stu-id="eccfb-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="eccfb-208">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="eccfb-209">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="eccfb-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="eccfb-210">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="eccfb-210">**Site:** *6*</span></span>
    - <span data-ttu-id="eccfb-211">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="eccfb-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="eccfb-212">**Groep:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="eccfb-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="eccfb-213">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-214">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-215">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="eccfb-216">Verkooporders 6-7 en 6-8</span><span class="sxs-lookup"><span data-stu-id="eccfb-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="eccfb-217">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="eccfb-218">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="eccfb-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="eccfb-219">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="eccfb-219">**Site:** *6*</span></span>
    - <span data-ttu-id="eccfb-220">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="eccfb-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="eccfb-221">**Groep:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="eccfb-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="eccfb-222">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="eccfb-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="eccfb-223">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="eccfb-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="eccfb-224">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="eccfb-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="eccfb-225">Automatische vrijgave van verkooporders naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="eccfb-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="eccfb-226">Voor elke set verkooporders die u eerder hebt gemaakt, voltooit u een procedure voor het automatisch vrijgeven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="eccfb-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="eccfb-227">In beide gevallen doorloopt u de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) die hier wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="eccfb-228">Basisprocedure voor vrijgave naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="eccfb-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="eccfb-229">Voor elke set verkooporders die u eerder hebt gemaakt, voert u de drie procedures uit die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="eccfb-230">De wave-sjabloon bijwerken die tijdens de vrijgave wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="eccfb-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="eccfb-231">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="eccfb-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="eccfb-232">Stel het veld **Type wavesjabloon** in op *Verzenden*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="eccfb-233">Zoek en selecteer de wavesjabloon die is gekoppeld aan het magazijn dat u hebt gebruikt in de ordersets die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eccfb-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="eccfb-234">Als u bijvoorbeeld magazijn *24* hebt gebruikt , selecteert u de wavesjabloon **24 Standaardverzending**.</span><span class="sxs-lookup"><span data-stu-id="eccfb-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="eccfb-235">Als u magazijn *61* hebt gebruikt, selecteert u de wavesjabloon **61 Verzending**.</span><span class="sxs-lookup"><span data-stu-id="eccfb-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="eccfb-236">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eccfb-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="eccfb-237">Stel de optie **Wave verwerken bij vrijgave door magazijn** in op *Nee*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="eccfb-238">Vrijgave naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="eccfb-238">Release to the warehouse</span></span>

1. <span data-ttu-id="eccfb-239">Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Automatische vrijgave van verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="eccfb-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="eccfb-240">Stel het veld **Hoeveelheid voor vrijgave** in op *Alle*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="eccfb-241">Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** om het querydialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="eccfb-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="eccfb-242">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een rij met de volgende instellingen aan het raster toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="eccfb-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="eccfb-243">**Tabel:** *Verkooporder*</span><span class="sxs-lookup"><span data-stu-id="eccfb-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="eccfb-244">**Afgeleide tabel:** *Verkooporder*</span><span class="sxs-lookup"><span data-stu-id="eccfb-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="eccfb-245">**Veld:** *Verkooporder*</span><span class="sxs-lookup"><span data-stu-id="eccfb-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="eccfb-246">**Criteria:** voer een door komma's gescheiden lijst in van de verkoopordernummers uit de gewenste orderset.</span><span class="sxs-lookup"><span data-stu-id="eccfb-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="eccfb-247">Selecteer **OK** om uw query op te slaan.</span><span class="sxs-lookup"><span data-stu-id="eccfb-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="eccfb-248">Selecteer **OK** om de procedure *Automatische vrijgave naar magazijn* te starten.</span><span class="sxs-lookup"><span data-stu-id="eccfb-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="eccfb-249">De zending controleren die is gemaakt of bijgewerkt</span><span class="sxs-lookup"><span data-stu-id="eccfb-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="eccfb-250">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="eccfb-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="eccfb-251">Zoek en selecteer de vereiste zending.</span><span class="sxs-lookup"><span data-stu-id="eccfb-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="eccfb-252">Als een consolidatiebeleid is gebruikt bij het maken of bijwerken van de zending, wordt dit weergegeven in het veld **Consolidatiebeleid voor zendingen**.</span><span class="sxs-lookup"><span data-stu-id="eccfb-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="eccfb-253">Verkooporders vrijgeven vanuit orderset 1</span><span class="sxs-lookup"><span data-stu-id="eccfb-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="eccfb-254">Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 1 vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="eccfb-255">Wanneer u klaar bent, ziet u dat er twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="eccfb-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="eccfb-256">De eerste zending bevat drie regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="eccfb-257">De tweede zending, die geen gebruikmaakt van de leveringsmethode *Airways*, is gemaakt met het consolidatiebeleid voor zending *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="eccfb-258">Verkooporders vrijgeven vanuit orderset 2</span><span class="sxs-lookup"><span data-stu-id="eccfb-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="eccfb-259">Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 2 vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="eccfb-260">Wanneer u klaar bent, ziet u dat er drie zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="eccfb-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="eccfb-261">De eerste zending bevat items van het type *Ontvlambaar*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="eccfb-262">Elk van de twee overige zendingen bevat één regel met het item *Explosief*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="eccfb-263">Verkooporders vrijgeven vanuit orderset 3</span><span class="sxs-lookup"><span data-stu-id="eccfb-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="eccfb-264">Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 3 vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="eccfb-265">Wanneer u klaar bent, ziet u dat de volgende acties zijn uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="eccfb-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="eccfb-266">Eén bestaande zending (de zending die is gemaakt toen orderset 2 is vrijgegeven naar het magazijn) is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="eccfb-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="eccfb-267">Er is een regel toegevoegd waaraan het item *Ontvlambaar* is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="eccfb-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="eccfb-268">Er is één nieuwe zending gemaakt die het item *Explosief* bevat.</span><span class="sxs-lookup"><span data-stu-id="eccfb-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="eccfb-269">Verkooporders vrijgeven vanuit orderset 4</span><span class="sxs-lookup"><span data-stu-id="eccfb-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="eccfb-270">Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 4 vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="eccfb-271">Wanneer u klaar bent, is één bestaande zending (waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*) is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="eccfb-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="eccfb-272">Hieraan is één nieuwe regel toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="eccfb-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="eccfb-273">Verkooporders vrijgeven vanuit orderset 5</span><span class="sxs-lookup"><span data-stu-id="eccfb-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="eccfb-274">Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 5 vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="eccfb-275">Wanneer u klaar bent, ziet u dat de volgende acties zijn uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="eccfb-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="eccfb-276">Eén bestaande zending (waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*) is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="eccfb-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="eccfb-277">Een regel uit verkooporder 5-3 (waarbij het veld **Bestelopdracht van klant** is ingesteld op *1*) is hieraan toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="eccfb-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="eccfb-278">Er is één nieuwe zending gemaakt, waarbij regels van verkooporders 5-1 en 5-2 in één zending worden gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="eccfb-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="eccfb-279">Verkooporders vrijgeven vanuit orderset 6</span><span class="sxs-lookup"><span data-stu-id="eccfb-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="eccfb-280">Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 6 vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="eccfb-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="eccfb-281">Wanneer u klaar bent, ziet u dat er vier zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="eccfb-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="eccfb-282">Regels van twee orders voor klant *US-003* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="eccfb-283">Regels van twee orders voor klant *US-004* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="eccfb-284">Regels van verkooporders 6-5 en 6-6 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="eccfb-285">Regels van verkooporders 6-7 en 6-8 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *CrossOrder*.</span><span class="sxs-lookup"><span data-stu-id="eccfb-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eccfb-286">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="eccfb-286">Additional resources</span></span>

- [<span data-ttu-id="eccfb-287">Beleidsregels voor consolidatie van zendingen</span><span class="sxs-lookup"><span data-stu-id="eccfb-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="eccfb-288">Consolidatiebeleid voor zendingen configureren</span><span class="sxs-lookup"><span data-stu-id="eccfb-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)