---
title: Voorbeelden en logica voor naar ouderdom gerangschikt voorraadrapport
description: Dit onderwerp bevat enkele voorbeelden voor het interpreteren van de resultaten van een naar ouderdom gerangschikt voorraadrapport.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: cb7b7a055c26b53ee3acc3b872acf04fcf089eca
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597235"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="7efc3-103">Voorbeelden en logica voor naar ouderdom gerangschikt voorraadrapport</span><span class="sxs-lookup"><span data-stu-id="7efc3-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7efc3-104">Dit onderwerp bevat enkele voorbeelden voor het interpreteren van de resultaten van een **Naar ouderdom gerangschikt voorraadrapport**.</span><span class="sxs-lookup"><span data-stu-id="7efc3-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="7efc3-105">Dit rapport categoriseert de voorhanden hoeveelheid en voorraadwaarden voor een geselecteerd artikel of een geselecteerde artikelgroep in verschillende periodebuckets.</span><span class="sxs-lookup"><span data-stu-id="7efc3-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="7efc3-106">In dit onderwerp wordt ook de interne logica van het rapport weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7efc3-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="7efc3-107">In de voorbeelden in dit onderwerp worden resultaten weergegeven in een standaard **naar ouderdom gerangschikt voorraadrapport**.</span><span class="sxs-lookup"><span data-stu-id="7efc3-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="7efc3-108">In het algemeen is het echter raadzaam om de [opslagversie van het naar ouderdom gerangschikte voorraadrapport](inventory-aging-report-storage.md) te gebruiken, vooral wanneer u veel artikelen en magazijnen moet verwerken.</span><span class="sxs-lookup"><span data-stu-id="7efc3-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="7efc3-109">Met Opslag naar ouderdom gerangschikt rapport wordt elk gegenereerd rapport opgeslagen, worden de resultaten weergegeven als een interactieve pagina en een grafiek, en kunt u elk opgeslagen rapport exporteren.</span><span class="sxs-lookup"><span data-stu-id="7efc3-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="7efc3-110">Voorbeeldgegevens die in deze voorbeelden worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="7efc3-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="7efc3-111">De voorbeelden in dit onderwerp zijn gebaseerd op de voorbeeldgegevens voor voorraadtransacties die in deze sectie worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="7efc3-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="7efc3-112">Instellingen opslagdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="7efc3-112">Storage dimension setup</span></span>

<span data-ttu-id="7efc3-113">Het voorbeeldsysteem bevat de volgende instellingen voor opslagdimensies.</span><span class="sxs-lookup"><span data-stu-id="7efc3-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="7efc3-114">Naam</span><span class="sxs-lookup"><span data-stu-id="7efc3-114">Name</span></span>      | <span data-ttu-id="7efc3-115">Actief</span><span class="sxs-lookup"><span data-stu-id="7efc3-115">Active</span></span> | <span data-ttu-id="7efc3-116">Fysieke voorraad</span><span class="sxs-lookup"><span data-stu-id="7efc3-116">Physical inventory</span></span> | <span data-ttu-id="7efc3-117">Financiële voorraad</span><span class="sxs-lookup"><span data-stu-id="7efc3-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="7efc3-118">Locatie</span><span class="sxs-lookup"><span data-stu-id="7efc3-118">Site</span></span>      | <span data-ttu-id="7efc3-119">Ja</span><span class="sxs-lookup"><span data-stu-id="7efc3-119">Yes</span></span>    | <span data-ttu-id="7efc3-120">Ja</span><span class="sxs-lookup"><span data-stu-id="7efc3-120">Yes</span></span>                | <span data-ttu-id="7efc3-121">Ja</span><span class="sxs-lookup"><span data-stu-id="7efc3-121">Yes</span></span>                 |
| <span data-ttu-id="7efc3-122">Magazijn</span><span class="sxs-lookup"><span data-stu-id="7efc3-122">Warehouse</span></span> | <span data-ttu-id="7efc3-123">Ja</span><span class="sxs-lookup"><span data-stu-id="7efc3-123">Yes</span></span>    | <span data-ttu-id="7efc3-124">Ja</span><span class="sxs-lookup"><span data-stu-id="7efc3-124">Yes</span></span>                | <span data-ttu-id="7efc3-125">No</span><span class="sxs-lookup"><span data-stu-id="7efc3-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="7efc3-126">Voorraadwaarderingsmodel</span><span class="sxs-lookup"><span data-stu-id="7efc3-126">Inventory model</span></span>

<span data-ttu-id="7efc3-127">Voor het voorbeeldsysteem is het voorraadmodel voor de vrijgegeven producten *FIFO* en de instelling voor **Kostprijs** voor het voorraadmodel is *Fysieke waarde opnemen*.</span><span class="sxs-lookup"><span data-stu-id="7efc3-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="7efc3-128">Voorraadtransacties</span><span class="sxs-lookup"><span data-stu-id="7efc3-128">Inventory transactions</span></span>

<span data-ttu-id="7efc3-129">Het voorbeeldsysteem bevat de volgende voorraadtransacties voor een vrijgegeven product met artikelnummer *1000*.</span><span class="sxs-lookup"><span data-stu-id="7efc3-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="7efc3-130">Verwijzing</span><span class="sxs-lookup"><span data-stu-id="7efc3-130">Reference</span></span>      | <span data-ttu-id="7efc3-131">Locatie</span><span class="sxs-lookup"><span data-stu-id="7efc3-131">Site</span></span> | <span data-ttu-id="7efc3-132">Magazijn</span><span class="sxs-lookup"><span data-stu-id="7efc3-132">Warehouse</span></span> | <span data-ttu-id="7efc3-133">Ontvangst</span><span class="sxs-lookup"><span data-stu-id="7efc3-133">Receipt</span></span>   | <span data-ttu-id="7efc3-134">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="7efc3-134">Issue</span></span> | <span data-ttu-id="7efc3-135">Fysieke datum</span><span class="sxs-lookup"><span data-stu-id="7efc3-135">Physical date</span></span> | <span data-ttu-id="7efc3-136">Fin. datum</span><span class="sxs-lookup"><span data-stu-id="7efc3-136">Financial date</span></span> | <span data-ttu-id="7efc3-137">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-137">Quantity</span></span> | <span data-ttu-id="7efc3-138">Kosten</span><span class="sxs-lookup"><span data-stu-id="7efc3-138">Cost amount</span></span> | <span data-ttu-id="7efc3-139">Fysieke kostprijs</span><span class="sxs-lookup"><span data-stu-id="7efc3-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="7efc3-140">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="7efc3-140">Purchase order</span></span> | <span data-ttu-id="7efc3-141">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-141">1</span></span>    | <span data-ttu-id="7efc3-142">11</span><span class="sxs-lookup"><span data-stu-id="7efc3-142">11</span></span>        | <span data-ttu-id="7efc3-143">Ingekocht</span><span class="sxs-lookup"><span data-stu-id="7efc3-143">Purchased</span></span> |       | <span data-ttu-id="7efc3-144">15 maart</span><span class="sxs-lookup"><span data-stu-id="7efc3-144">March 15</span></span>      | <span data-ttu-id="7efc3-145">15 maart</span><span class="sxs-lookup"><span data-stu-id="7efc3-145">March 15</span></span>       | <span data-ttu-id="7efc3-146">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-146">10</span></span>       | <span data-ttu-id="7efc3-147">1.000</span><span class="sxs-lookup"><span data-stu-id="7efc3-147">1,000</span></span>       | <span data-ttu-id="7efc3-148">1.000</span><span class="sxs-lookup"><span data-stu-id="7efc3-148">1,000</span></span>                |
| <span data-ttu-id="7efc3-149">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="7efc3-149">Purchase order</span></span> | <span data-ttu-id="7efc3-150">2</span><span class="sxs-lookup"><span data-stu-id="7efc3-150">2</span></span>    | <span data-ttu-id="7efc3-151">21</span><span class="sxs-lookup"><span data-stu-id="7efc3-151">21</span></span>        | <span data-ttu-id="7efc3-152">Ingekocht</span><span class="sxs-lookup"><span data-stu-id="7efc3-152">Purchased</span></span> |       | <span data-ttu-id="7efc3-153">15 maart</span><span class="sxs-lookup"><span data-stu-id="7efc3-153">March 15</span></span>      | <span data-ttu-id="7efc3-154">15 maart</span><span class="sxs-lookup"><span data-stu-id="7efc3-154">March 15</span></span>       | <span data-ttu-id="7efc3-155">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-155">10</span></span>       | <span data-ttu-id="7efc3-156">2,000</span><span class="sxs-lookup"><span data-stu-id="7efc3-156">2,000</span></span>       | <span data-ttu-id="7efc3-157">2,000</span><span class="sxs-lookup"><span data-stu-id="7efc3-157">2,000</span></span>                |
| <span data-ttu-id="7efc3-158">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="7efc3-158">Purchase order</span></span> | <span data-ttu-id="7efc3-159">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-159">1</span></span>    | <span data-ttu-id="7efc3-160">11</span><span class="sxs-lookup"><span data-stu-id="7efc3-160">11</span></span>        | <span data-ttu-id="7efc3-161">Ontvangen</span><span class="sxs-lookup"><span data-stu-id="7efc3-161">Received</span></span>  |       | <span data-ttu-id="7efc3-162">15 april</span><span class="sxs-lookup"><span data-stu-id="7efc3-162">April 15</span></span>      |                | <span data-ttu-id="7efc3-163">5</span><span class="sxs-lookup"><span data-stu-id="7efc3-163">5</span></span>        |             | <span data-ttu-id="7efc3-164">375</span><span class="sxs-lookup"><span data-stu-id="7efc3-164">375</span></span>                  |
| <span data-ttu-id="7efc3-165">Transferorder</span><span class="sxs-lookup"><span data-stu-id="7efc3-165">Transfer order</span></span> | <span data-ttu-id="7efc3-166">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-166">1</span></span>    | <span data-ttu-id="7efc3-167">11</span><span class="sxs-lookup"><span data-stu-id="7efc3-167">11</span></span>        |           | <span data-ttu-id="7efc3-168">Verkocht</span><span class="sxs-lookup"><span data-stu-id="7efc3-168">Sold</span></span>  | <span data-ttu-id="7efc3-169">mei 2</span><span class="sxs-lookup"><span data-stu-id="7efc3-169">May 2</span></span>         | <span data-ttu-id="7efc3-170">mei 2</span><span class="sxs-lookup"><span data-stu-id="7efc3-170">May 2</span></span>          | <span data-ttu-id="7efc3-171">-5</span><span class="sxs-lookup"><span data-stu-id="7efc3-171">-5</span></span>       | <span data-ttu-id="7efc3-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="7efc3-172">-458.33</span></span>     | <span data-ttu-id="7efc3-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="7efc3-173">-458.33</span></span>              |
| <span data-ttu-id="7efc3-174">Transferorder</span><span class="sxs-lookup"><span data-stu-id="7efc3-174">Transfer order</span></span> | <span data-ttu-id="7efc3-175">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-175">1</span></span>    | <span data-ttu-id="7efc3-176">12</span><span class="sxs-lookup"><span data-stu-id="7efc3-176">12</span></span>        | <span data-ttu-id="7efc3-177">Ingekocht</span><span class="sxs-lookup"><span data-stu-id="7efc3-177">Purchased</span></span> |       | <span data-ttu-id="7efc3-178">mei 2</span><span class="sxs-lookup"><span data-stu-id="7efc3-178">May 2</span></span>         | <span data-ttu-id="7efc3-179">mei 2</span><span class="sxs-lookup"><span data-stu-id="7efc3-179">May 2</span></span>          | <span data-ttu-id="7efc3-180">5</span><span class="sxs-lookup"><span data-stu-id="7efc3-180">5</span></span>        | <span data-ttu-id="7efc3-181">458.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-181">458.33</span></span>      | <span data-ttu-id="7efc3-182">458.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-182">458.33</span></span>               |
| <span data-ttu-id="7efc3-183">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="7efc3-183">Sales order</span></span>    | <span data-ttu-id="7efc3-184">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-184">1</span></span>    | <span data-ttu-id="7efc3-185">12</span><span class="sxs-lookup"><span data-stu-id="7efc3-185">12</span></span>        |           | <span data-ttu-id="7efc3-186">Verkocht</span><span class="sxs-lookup"><span data-stu-id="7efc3-186">Sold</span></span>  | <span data-ttu-id="7efc3-187">mei 3</span><span class="sxs-lookup"><span data-stu-id="7efc3-187">May 3</span></span>         | <span data-ttu-id="7efc3-188">mei 3</span><span class="sxs-lookup"><span data-stu-id="7efc3-188">May 3</span></span>          | <span data-ttu-id="7efc3-189">-1</span><span class="sxs-lookup"><span data-stu-id="7efc3-189">-1</span></span>       | <span data-ttu-id="7efc3-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="7efc3-190">-91.67</span></span>      | <span data-ttu-id="7efc3-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="7efc3-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="7efc3-192">Berekenen van hoeveelheden en bedragen in de periodebuckets</span><span class="sxs-lookup"><span data-stu-id="7efc3-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="7efc3-193">Met behulp van de voorbeeldgegevens die in de vorige secties worden beschreven, kunt u een **Naar ouderdom gerangschikt rapport** uitvoeren met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="7efc3-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="7efc3-194">**Vanaf datum:** *9 mei 2020*</span><span class="sxs-lookup"><span data-stu-id="7efc3-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="7efc3-195">**Locatie:** *Weergave*</span><span class="sxs-lookup"><span data-stu-id="7efc3-195">**Site:** *View*</span></span>
- <span data-ttu-id="7efc3-196">**Magazijn:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="7efc3-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="7efc3-197">**Artikelnummer:** *Totaal*</span><span class="sxs-lookup"><span data-stu-id="7efc3-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="7efc3-198">**Ouderdomsperiode:** Stel dit veld in om maandelijkse buckets te genereren.</span><span class="sxs-lookup"><span data-stu-id="7efc3-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="7efc3-199">In dit geval is de inhoud van het gegenereerde rapport vergelijkbaar met het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="7efc3-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="7efc3-200">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="7efc3-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-201">Locatie</span><span class="sxs-lookup"><span data-stu-id="7efc3-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-202">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-203">Waarde voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="7efc3-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-204">Hoeveelheid voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="7efc3-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-205">Voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="7efc3-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-206">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="7efc3-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-207">8/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-208">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-209">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="7efc3-210">P1:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-211">P1:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="7efc3-212">P2:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-213">P2:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="7efc3-214">P3:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-215">P3:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="7efc3-216">1000</span><span class="sxs-lookup"><span data-stu-id="7efc3-216">1000</span></span></td>
    <td><span data-ttu-id="7efc3-217">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-217">1</span></span></td>
    <td><span data-ttu-id="7efc3-218">14</span><span class="sxs-lookup"><span data-stu-id="7efc3-218">14</span></span></td>
    <td><span data-ttu-id="7efc3-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-219">1,283.33</span></span></td>
    <td><span data-ttu-id="7efc3-220">14</span><span class="sxs-lookup"><span data-stu-id="7efc3-220">14</span></span></td>
    <td><span data-ttu-id="7efc3-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-221">1,283.33</span></span></td>
    <td><span data-ttu-id="7efc3-222">91.67</span><span class="sxs-lookup"><span data-stu-id="7efc3-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-223">5.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-223">5.00</span></span></td>
    <td><span data-ttu-id="7efc3-224">458.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-224">458.33</span></span></td>
    <td><span data-ttu-id="7efc3-225">9.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-225">9.00</span></span></td>
    <td><span data-ttu-id="7efc3-226">825.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="7efc3-227">1000</span><span class="sxs-lookup"><span data-stu-id="7efc3-227">1000</span></span></td>
    <td><span data-ttu-id="7efc3-228">2</span><span class="sxs-lookup"><span data-stu-id="7efc3-228">2</span></span></td>
    <td><span data-ttu-id="7efc3-229">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-229">10</span></span></td>
    <td><span data-ttu-id="7efc3-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-230">2,000.00</span></span></td>
    <td><span data-ttu-id="7efc3-231">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-231">10</span></span></td>
    <td><span data-ttu-id="7efc3-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-232">2,000.00</span></span></td>
    <td><span data-ttu-id="7efc3-233">200.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-234">10.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-234">10.00</span></span></td>
    <td><span data-ttu-id="7efc3-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="7efc3-236"><strong>1000 Totalen</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="7efc3-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="7efc3-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="7efc3-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="7efc3-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="7efc3-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="7efc3-243">Let op de volgende details in dit voorbeeldrapport:</span><span class="sxs-lookup"><span data-stu-id="7efc3-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="7efc3-244">De waarden van **Hoeveelheid voorraadwaarde**, **Voorraadwaarde** en **Gemiddelde eenheidskosten** die in het rapport worden weergegeven, zijn waarden voor de financiële voorraaddimensie (**site** in dit geval).</span><span class="sxs-lookup"><span data-stu-id="7efc3-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="7efc3-245">Voor site 1 bevat het rapport bijvoorbeeld de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="7efc3-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="7efc3-246">De **Hoeveelheid voorraadwaarde** is *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="7efc3-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="7efc3-247">De **Voorraadwaarde** is *1.283,33* (= 1.000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="7efc3-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="7efc3-248">De **Gemiddelde eenheidskosten** is *91,67*.</span><span class="sxs-lookup"><span data-stu-id="7efc3-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="7efc3-249">De waarde voor **Voorhanden voorraad** en de waarde voor **Bedrag** in elke periodebucket worden berekend met behulp van **Gemiddelde eenheidskosten**.</span><span class="sxs-lookup"><span data-stu-id="7efc3-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="7efc3-250">Het rapport bepaalt de voorhanden hoeveelheid voor elke periodebucket door de totale ontvangen voorraadhoeveelheid voor elke periodebucket samen te vatten.</span><span class="sxs-lookup"><span data-stu-id="7efc3-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="7efc3-251">Vervolgens wordt het FIFO-principe (First In, First Out) toegepast om de totale uitgegeven hoeveelheid af te trekken, ongeacht het voorraadmodel dat de artikelen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7efc3-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="7efc3-252">Als u hetzelfde rapport opnieuw uitvoert, maar deze keer de velden **Site** en **Magazijn** instelt op *Weergeven*, ziet het nieuwe rapport eruit als in het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="7efc3-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="7efc3-253">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="7efc3-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-254">Locatie</span><span class="sxs-lookup"><span data-stu-id="7efc3-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-255">Magazijn</span><span class="sxs-lookup"><span data-stu-id="7efc3-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-256">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-257">Waarde voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="7efc3-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-258">Hoeveelheid voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="7efc3-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-259">Voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="7efc3-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-260">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="7efc3-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-261">8/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-262">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-263">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="7efc3-264">P1:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-265">P1:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="7efc3-266">P2:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-267">P2:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="7efc3-268">P3:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-269">P3:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="7efc3-270">1000</span><span class="sxs-lookup"><span data-stu-id="7efc3-270">1000</span></span></td>
    <td><span data-ttu-id="7efc3-271">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-271">1</span></span></td>
    <td><span data-ttu-id="7efc3-272">11</span><span class="sxs-lookup"><span data-stu-id="7efc3-272">11</span></span></td>
    <td><span data-ttu-id="7efc3-273">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-273">10</span></span></td>
    <td><span data-ttu-id="7efc3-274">916.67</span><span class="sxs-lookup"><span data-stu-id="7efc3-274">916.67</span></span></td>
    <td><span data-ttu-id="7efc3-275">14</span><span class="sxs-lookup"><span data-stu-id="7efc3-275">14</span></span></td>
    <td><span data-ttu-id="7efc3-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-276">1,283.33</span></span></td>
    <td><span data-ttu-id="7efc3-277">91.67</span><span class="sxs-lookup"><span data-stu-id="7efc3-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-278">5.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-278">5.00</span></span></td>
    <td><span data-ttu-id="7efc3-279">458.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-279">458.33</span></span></td>
    <td><span data-ttu-id="7efc3-280">5.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-280">5.00</span></span></td>
    <td><span data-ttu-id="7efc3-281">458.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="7efc3-282">1000</span><span class="sxs-lookup"><span data-stu-id="7efc3-282">1000</span></span></td>
    <td><span data-ttu-id="7efc3-283">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-283">1</span></span></td>
    <td><span data-ttu-id="7efc3-284">12</span><span class="sxs-lookup"><span data-stu-id="7efc3-284">12</span></span></td>
    <td><span data-ttu-id="7efc3-285">4</span><span class="sxs-lookup"><span data-stu-id="7efc3-285">4</span></span></td>
    <td><span data-ttu-id="7efc3-286">366.67</span><span class="sxs-lookup"><span data-stu-id="7efc3-286">366.67</span></span></td>
    <td><span data-ttu-id="7efc3-287">14</span><span class="sxs-lookup"><span data-stu-id="7efc3-287">14</span></span></td>
    <td><span data-ttu-id="7efc3-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="7efc3-288">1,283.33</span></span></td>
    <td><span data-ttu-id="7efc3-289">91.67</span><span class="sxs-lookup"><span data-stu-id="7efc3-289">91.67</span></span></td>
    <td><span data-ttu-id="7efc3-290">4.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-290">4.00</span></span></td>
    <td><span data-ttu-id="7efc3-291">366.67</span><span class="sxs-lookup"><span data-stu-id="7efc3-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="7efc3-292">1000</span><span class="sxs-lookup"><span data-stu-id="7efc3-292">1000</span></span></td>
    <td><span data-ttu-id="7efc3-293">2</span><span class="sxs-lookup"><span data-stu-id="7efc3-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="7efc3-294">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-294">10</span></span></td>
    <td><span data-ttu-id="7efc3-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-295">2,000.00</span></span></td>
    <td><span data-ttu-id="7efc3-296">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-296">10</span></span></td>
    <td><span data-ttu-id="7efc3-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-297">2,000.00</span></span></td>
    <td><span data-ttu-id="7efc3-298">200.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-299">10.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-299">10.00</span></span></td>
    <td><span data-ttu-id="7efc3-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="7efc3-301"><strong>1000 Totalen</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="7efc3-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="7efc3-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="7efc3-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="7efc3-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="7efc3-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="7efc3-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="7efc3-310">Deze keer wordt site 1 opgesplitst in twee rijen, één voor magazijn 11 en één voor magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="7efc3-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="7efc3-311">De waarden van **Hoeveelheid voorraadwaarde**, **Voorraadwaarde** en **Gemiddelde eenheidskosten** zijn echter hetzelfde, omdat **Magazijn** geen financiële voorraaddimensie is.</span><span class="sxs-lookup"><span data-stu-id="7efc3-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="7efc3-312">U ziet ook dat de hoeveelheidsdistributie van site 1 afwijkt.</span><span class="sxs-lookup"><span data-stu-id="7efc3-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="7efc3-313">In het eerste rapport dat u hebt uitgevoerd, is de overdrachtsorder genegeerd die zich op dezelfde locatie heeft voorgedaan en wordt de hoeveelheid van de verkoopfactuur in mindering gebracht op de periodebucket **31/3/2020-1/3/2020** in site 1.</span><span class="sxs-lookup"><span data-stu-id="7efc3-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="7efc3-314">In het nieuwe rapport trekt het systeem echter de hoeveelheid van de verkoopfactuur af van de periodebucket **8/5/2020-1/5/2020** in magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="7efc3-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="7efc3-315">Effecten van voorraadafsluiting</span><span class="sxs-lookup"><span data-stu-id="7efc3-315">Effects of inventory closing</span></span>

<span data-ttu-id="7efc3-316">Als u de voorraadafsluiting uitvoert voor mei en vervolgens het vorige rapport opnieuw uitvoert, maar het veld **Begindatum** instelt op *31 mei 2020* , zult u de volgende resultaten opmerken:</span><span class="sxs-lookup"><span data-stu-id="7efc3-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="7efc3-317">De waarden voor **Voorraadwaarde**en **Gemiddelde eenheidskosten** worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="7efc3-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="7efc3-318">De **Waarde voorhanden voorraad** en alle waarden voor **Bedrag** in elke periodebucket worden dienovereenkomstig bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="7efc3-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="7efc3-319">Het nieuwe rapport lijkt op het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="7efc3-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="7efc3-320">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="7efc3-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-321">Locatie</span><span class="sxs-lookup"><span data-stu-id="7efc3-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-322">Magazijn</span><span class="sxs-lookup"><span data-stu-id="7efc3-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-323">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-324">Waarde voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="7efc3-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-325">Hoeveelheid voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="7efc3-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-326">Voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="7efc3-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="7efc3-327">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="7efc3-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-328">31/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-329">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="7efc3-330">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="7efc3-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="7efc3-331">P1:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-332">P1:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="7efc3-333">P2:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-334">P2:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="7efc3-335">P3:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7efc3-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="7efc3-336">P3:Bedrag</span><span class="sxs-lookup"><span data-stu-id="7efc3-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="7efc3-337">1000</span><span class="sxs-lookup"><span data-stu-id="7efc3-337">1000</span></span></td>
    <td><span data-ttu-id="7efc3-338">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-338">1</span></span></td>
    <td><span data-ttu-id="7efc3-339">11</span><span class="sxs-lookup"><span data-stu-id="7efc3-339">11</span></span></td>
    <td><span data-ttu-id="7efc3-340">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-340">10</span></span></td>
    <td><span data-ttu-id="7efc3-341">910.70</span><span class="sxs-lookup"><span data-stu-id="7efc3-341">910.70</span></span></td>
    <td><span data-ttu-id="7efc3-342">14</span><span class="sxs-lookup"><span data-stu-id="7efc3-342">14</span></span></td>
    <td><span data-ttu-id="7efc3-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-343">1,275.00</span></span></td>
    <td><span data-ttu-id="7efc3-344">91.07</span><span class="sxs-lookup"><span data-stu-id="7efc3-344">91.07</span></span></td>
    <td><span data-ttu-id="7efc3-345">0,00</span><span class="sxs-lookup"><span data-stu-id="7efc3-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="7efc3-346">5.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-346">5.00</span></span></td>
    <td><span data-ttu-id="7efc3-347">455.36</span><span class="sxs-lookup"><span data-stu-id="7efc3-347">455.36</span></span></td>
    <td><span data-ttu-id="7efc3-348">5.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-348">5.00</span></span></td>
    <td><span data-ttu-id="7efc3-349">455.36</span><span class="sxs-lookup"><span data-stu-id="7efc3-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="7efc3-350">1000</span><span class="sxs-lookup"><span data-stu-id="7efc3-350">1000</span></span></td>
    <td><span data-ttu-id="7efc3-351">1</span><span class="sxs-lookup"><span data-stu-id="7efc3-351">1</span></span></td>
    <td><span data-ttu-id="7efc3-352">12</span><span class="sxs-lookup"><span data-stu-id="7efc3-352">12</span></span></td>
    <td><span data-ttu-id="7efc3-353">4</span><span class="sxs-lookup"><span data-stu-id="7efc3-353">4</span></span></td>
    <td><span data-ttu-id="7efc3-354">364.29</span><span class="sxs-lookup"><span data-stu-id="7efc3-354">364.29</span></span></td>
    <td><span data-ttu-id="7efc3-355">14</span><span class="sxs-lookup"><span data-stu-id="7efc3-355">14</span></span></td>
    <td><span data-ttu-id="7efc3-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-356">1,275.00</span></span></td>
    <td><span data-ttu-id="7efc3-357">91.07</span><span class="sxs-lookup"><span data-stu-id="7efc3-357">91.07</span></span></td>
    <td><span data-ttu-id="7efc3-358">4.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-358">4.00</span></span></td>
    <td><span data-ttu-id="7efc3-359">364.29</span><span class="sxs-lookup"><span data-stu-id="7efc3-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="7efc3-360">1000</span><span class="sxs-lookup"><span data-stu-id="7efc3-360">1000</span></span></td>
    <td><span data-ttu-id="7efc3-361">2</span><span class="sxs-lookup"><span data-stu-id="7efc3-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="7efc3-362">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-362">10</span></span></td>
    <td><span data-ttu-id="7efc3-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-363">2,000.00</span></span></td>
    <td><span data-ttu-id="7efc3-364">10</span><span class="sxs-lookup"><span data-stu-id="7efc3-364">10</span></span></td>
    <td><span data-ttu-id="7efc3-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-365">2,000.00</span></span></td>
    <td><span data-ttu-id="7efc3-366">200.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-367">10.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-367">10.00</span></span></td>
    <td><span data-ttu-id="7efc3-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="7efc3-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="7efc3-369"><strong>1000 Totalen</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="7efc3-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="7efc3-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="7efc3-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="7efc3-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="7efc3-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="7efc3-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="7efc3-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="7efc3-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
