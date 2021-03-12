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
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983920"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="4ae6b-103">Voorbeelden en logica voor naar ouderdom gerangschikt voorraadrapport</span><span class="sxs-lookup"><span data-stu-id="4ae6b-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ae6b-104">Dit onderwerp bevat enkele voorbeelden voor het interpreteren van de resultaten van een **Naar ouderdom gerangschikt voorraadrapport**.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="4ae6b-105">Dit rapport categoriseert de voorhanden hoeveelheid en voorraadwaarden voor een geselecteerd artikel of een geselecteerde artikelgroep in verschillende periodebuckets.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="4ae6b-106">In dit onderwerp wordt ook de interne logica van het rapport weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="4ae6b-107">In de voorbeelden in dit onderwerp worden resultaten weergegeven in een standaard **naar ouderdom gerangschikt voorraadrapport**.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="4ae6b-108">In het algemeen is het echter raadzaam om de [opslagversie van het naar ouderdom gerangschikte voorraadrapport](inventory-aging-report-storage.md) te gebruiken, vooral wanneer u veel artikelen en magazijnen moet verwerken.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="4ae6b-109">Met Opslag naar ouderdom gerangschikt rapport wordt elk gegenereerd rapport opgeslagen, worden de resultaten weergegeven als een interactieve pagina en een grafiek, en kunt u elk opgeslagen rapport exporteren.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="4ae6b-110">Voorbeeldgegevens die in deze voorbeelden worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="4ae6b-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="4ae6b-111">De voorbeelden in dit onderwerp zijn gebaseerd op de voorbeeldgegevens voor voorraadtransacties die in deze sectie worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="4ae6b-112">Instellingen opslagdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="4ae6b-112">Storage dimension setup</span></span>

<span data-ttu-id="4ae6b-113">Het voorbeeldsysteem bevat de volgende instellingen voor opslagdimensies.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="4ae6b-114">Naam</span><span class="sxs-lookup"><span data-stu-id="4ae6b-114">Name</span></span>      | <span data-ttu-id="4ae6b-115">Actief</span><span class="sxs-lookup"><span data-stu-id="4ae6b-115">Active</span></span> | <span data-ttu-id="4ae6b-116">Fysieke voorraad</span><span class="sxs-lookup"><span data-stu-id="4ae6b-116">Physical inventory</span></span> | <span data-ttu-id="4ae6b-117">Financiële voorraad</span><span class="sxs-lookup"><span data-stu-id="4ae6b-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="4ae6b-118">Locatie</span><span class="sxs-lookup"><span data-stu-id="4ae6b-118">Site</span></span>      | <span data-ttu-id="4ae6b-119">Ja</span><span class="sxs-lookup"><span data-stu-id="4ae6b-119">Yes</span></span>    | <span data-ttu-id="4ae6b-120">Ja</span><span class="sxs-lookup"><span data-stu-id="4ae6b-120">Yes</span></span>                | <span data-ttu-id="4ae6b-121">Ja</span><span class="sxs-lookup"><span data-stu-id="4ae6b-121">Yes</span></span>                 |
| <span data-ttu-id="4ae6b-122">Magazijn</span><span class="sxs-lookup"><span data-stu-id="4ae6b-122">Warehouse</span></span> | <span data-ttu-id="4ae6b-123">Ja</span><span class="sxs-lookup"><span data-stu-id="4ae6b-123">Yes</span></span>    | <span data-ttu-id="4ae6b-124">Ja</span><span class="sxs-lookup"><span data-stu-id="4ae6b-124">Yes</span></span>                | <span data-ttu-id="4ae6b-125">No</span><span class="sxs-lookup"><span data-stu-id="4ae6b-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="4ae6b-126">Voorraadwaarderingsmodel</span><span class="sxs-lookup"><span data-stu-id="4ae6b-126">Inventory model</span></span>

<span data-ttu-id="4ae6b-127">Voor het voorbeeldsysteem is het voorraadmodel voor de vrijgegeven producten *FIFO* en de instelling voor **Kostprijs** voor het voorraadmodel is *Fysieke waarde opnemen*.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="4ae6b-128">Voorraadtransacties</span><span class="sxs-lookup"><span data-stu-id="4ae6b-128">Inventory transactions</span></span>

<span data-ttu-id="4ae6b-129">Het voorbeeldsysteem bevat de volgende voorraadtransacties voor een vrijgegeven product met artikelnummer *1000*.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="4ae6b-130">Verwijzing</span><span class="sxs-lookup"><span data-stu-id="4ae6b-130">Reference</span></span>      | <span data-ttu-id="4ae6b-131">Locatie</span><span class="sxs-lookup"><span data-stu-id="4ae6b-131">Site</span></span> | <span data-ttu-id="4ae6b-132">Magazijn</span><span class="sxs-lookup"><span data-stu-id="4ae6b-132">Warehouse</span></span> | <span data-ttu-id="4ae6b-133">Ontvangst</span><span class="sxs-lookup"><span data-stu-id="4ae6b-133">Receipt</span></span>   | <span data-ttu-id="4ae6b-134">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="4ae6b-134">Issue</span></span> | <span data-ttu-id="4ae6b-135">Fysieke datum</span><span class="sxs-lookup"><span data-stu-id="4ae6b-135">Physical date</span></span> | <span data-ttu-id="4ae6b-136">Fin. datum</span><span class="sxs-lookup"><span data-stu-id="4ae6b-136">Financial date</span></span> | <span data-ttu-id="4ae6b-137">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-137">Quantity</span></span> | <span data-ttu-id="4ae6b-138">Kosten</span><span class="sxs-lookup"><span data-stu-id="4ae6b-138">Cost amount</span></span> | <span data-ttu-id="4ae6b-139">Fysieke kostprijs</span><span class="sxs-lookup"><span data-stu-id="4ae6b-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="4ae6b-140">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="4ae6b-140">Purchase order</span></span> | <span data-ttu-id="4ae6b-141">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-141">1</span></span>    | <span data-ttu-id="4ae6b-142">11</span><span class="sxs-lookup"><span data-stu-id="4ae6b-142">11</span></span>        | <span data-ttu-id="4ae6b-143">Ingekocht</span><span class="sxs-lookup"><span data-stu-id="4ae6b-143">Purchased</span></span> |       | <span data-ttu-id="4ae6b-144">15 maart</span><span class="sxs-lookup"><span data-stu-id="4ae6b-144">March 15</span></span>      | <span data-ttu-id="4ae6b-145">15 maart</span><span class="sxs-lookup"><span data-stu-id="4ae6b-145">March 15</span></span>       | <span data-ttu-id="4ae6b-146">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-146">10</span></span>       | <span data-ttu-id="4ae6b-147">1.000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-147">1,000</span></span>       | <span data-ttu-id="4ae6b-148">1.000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-148">1,000</span></span>                |
| <span data-ttu-id="4ae6b-149">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="4ae6b-149">Purchase order</span></span> | <span data-ttu-id="4ae6b-150">2</span><span class="sxs-lookup"><span data-stu-id="4ae6b-150">2</span></span>    | <span data-ttu-id="4ae6b-151">21</span><span class="sxs-lookup"><span data-stu-id="4ae6b-151">21</span></span>        | <span data-ttu-id="4ae6b-152">Ingekocht</span><span class="sxs-lookup"><span data-stu-id="4ae6b-152">Purchased</span></span> |       | <span data-ttu-id="4ae6b-153">15 maart</span><span class="sxs-lookup"><span data-stu-id="4ae6b-153">March 15</span></span>      | <span data-ttu-id="4ae6b-154">15 maart</span><span class="sxs-lookup"><span data-stu-id="4ae6b-154">March 15</span></span>       | <span data-ttu-id="4ae6b-155">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-155">10</span></span>       | <span data-ttu-id="4ae6b-156">2,000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-156">2,000</span></span>       | <span data-ttu-id="4ae6b-157">2,000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-157">2,000</span></span>                |
| <span data-ttu-id="4ae6b-158">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="4ae6b-158">Purchase order</span></span> | <span data-ttu-id="4ae6b-159">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-159">1</span></span>    | <span data-ttu-id="4ae6b-160">11</span><span class="sxs-lookup"><span data-stu-id="4ae6b-160">11</span></span>        | <span data-ttu-id="4ae6b-161">Ontvangen</span><span class="sxs-lookup"><span data-stu-id="4ae6b-161">Received</span></span>  |       | <span data-ttu-id="4ae6b-162">15 april</span><span class="sxs-lookup"><span data-stu-id="4ae6b-162">April 15</span></span>      |                | <span data-ttu-id="4ae6b-163">5</span><span class="sxs-lookup"><span data-stu-id="4ae6b-163">5</span></span>        |             | <span data-ttu-id="4ae6b-164">375</span><span class="sxs-lookup"><span data-stu-id="4ae6b-164">375</span></span>                  |
| <span data-ttu-id="4ae6b-165">Transferorder</span><span class="sxs-lookup"><span data-stu-id="4ae6b-165">Transfer order</span></span> | <span data-ttu-id="4ae6b-166">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-166">1</span></span>    | <span data-ttu-id="4ae6b-167">11</span><span class="sxs-lookup"><span data-stu-id="4ae6b-167">11</span></span>        |           | <span data-ttu-id="4ae6b-168">Verkocht</span><span class="sxs-lookup"><span data-stu-id="4ae6b-168">Sold</span></span>  | <span data-ttu-id="4ae6b-169">mei 2</span><span class="sxs-lookup"><span data-stu-id="4ae6b-169">May 2</span></span>         | <span data-ttu-id="4ae6b-170">mei 2</span><span class="sxs-lookup"><span data-stu-id="4ae6b-170">May 2</span></span>          | <span data-ttu-id="4ae6b-171">-5</span><span class="sxs-lookup"><span data-stu-id="4ae6b-171">-5</span></span>       | <span data-ttu-id="4ae6b-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-172">-458.33</span></span>     | <span data-ttu-id="4ae6b-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-173">-458.33</span></span>              |
| <span data-ttu-id="4ae6b-174">Transferorder</span><span class="sxs-lookup"><span data-stu-id="4ae6b-174">Transfer order</span></span> | <span data-ttu-id="4ae6b-175">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-175">1</span></span>    | <span data-ttu-id="4ae6b-176">12</span><span class="sxs-lookup"><span data-stu-id="4ae6b-176">12</span></span>        | <span data-ttu-id="4ae6b-177">Ingekocht</span><span class="sxs-lookup"><span data-stu-id="4ae6b-177">Purchased</span></span> |       | <span data-ttu-id="4ae6b-178">mei 2</span><span class="sxs-lookup"><span data-stu-id="4ae6b-178">May 2</span></span>         | <span data-ttu-id="4ae6b-179">mei 2</span><span class="sxs-lookup"><span data-stu-id="4ae6b-179">May 2</span></span>          | <span data-ttu-id="4ae6b-180">5</span><span class="sxs-lookup"><span data-stu-id="4ae6b-180">5</span></span>        | <span data-ttu-id="4ae6b-181">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-181">458.33</span></span>      | <span data-ttu-id="4ae6b-182">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-182">458.33</span></span>               |
| <span data-ttu-id="4ae6b-183">Verkooporder</span><span class="sxs-lookup"><span data-stu-id="4ae6b-183">Sales order</span></span>    | <span data-ttu-id="4ae6b-184">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-184">1</span></span>    | <span data-ttu-id="4ae6b-185">12</span><span class="sxs-lookup"><span data-stu-id="4ae6b-185">12</span></span>        |           | <span data-ttu-id="4ae6b-186">Verkocht</span><span class="sxs-lookup"><span data-stu-id="4ae6b-186">Sold</span></span>  | <span data-ttu-id="4ae6b-187">mei 3</span><span class="sxs-lookup"><span data-stu-id="4ae6b-187">May 3</span></span>         | <span data-ttu-id="4ae6b-188">mei 3</span><span class="sxs-lookup"><span data-stu-id="4ae6b-188">May 3</span></span>          | <span data-ttu-id="4ae6b-189">-1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-189">-1</span></span>       | <span data-ttu-id="4ae6b-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="4ae6b-190">-91.67</span></span>      | <span data-ttu-id="4ae6b-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="4ae6b-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="4ae6b-192">Berekenen van hoeveelheden en bedragen in de periodebuckets</span><span class="sxs-lookup"><span data-stu-id="4ae6b-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="4ae6b-193">Met behulp van de voorbeeldgegevens die in de vorige secties worden beschreven, kunt u een **Naar ouderdom gerangschikt rapport** uitvoeren met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="4ae6b-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="4ae6b-194">**Vanaf datum:** *9 mei 2020*</span><span class="sxs-lookup"><span data-stu-id="4ae6b-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="4ae6b-195">**Locatie:** *Weergave*</span><span class="sxs-lookup"><span data-stu-id="4ae6b-195">**Site:** *View*</span></span>
- <span data-ttu-id="4ae6b-196">**Magazijn:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="4ae6b-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="4ae6b-197">**Artikelnummer:** *Totaal*</span><span class="sxs-lookup"><span data-stu-id="4ae6b-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="4ae6b-198">**Ouderdomsperiode:** Stel dit veld in om maandelijkse buckets te genereren.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="4ae6b-199">In dit geval is de inhoud van het gegenereerde rapport vergelijkbaar met het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="4ae6b-200">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="4ae6b-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-201">Locatie</span><span class="sxs-lookup"><span data-stu-id="4ae6b-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-202">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-203">Waarde voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="4ae6b-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-204">Hoeveelheid voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="4ae6b-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-205">Voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="4ae6b-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-206">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="4ae6b-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-207">8/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-208">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-209">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="4ae6b-210">P1:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-211">P1:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="4ae6b-212">P2:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-213">P2:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="4ae6b-214">P3:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-215">P3:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="4ae6b-216">1000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-216">1000</span></span></td>
    <td><span data-ttu-id="4ae6b-217">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-217">1</span></span></td>
    <td><span data-ttu-id="4ae6b-218">14</span><span class="sxs-lookup"><span data-stu-id="4ae6b-218">14</span></span></td>
    <td><span data-ttu-id="4ae6b-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-219">1,283.33</span></span></td>
    <td><span data-ttu-id="4ae6b-220">14</span><span class="sxs-lookup"><span data-stu-id="4ae6b-220">14</span></span></td>
    <td><span data-ttu-id="4ae6b-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-221">1,283.33</span></span></td>
    <td><span data-ttu-id="4ae6b-222">91.67</span><span class="sxs-lookup"><span data-stu-id="4ae6b-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-223">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-223">5.00</span></span></td>
    <td><span data-ttu-id="4ae6b-224">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-224">458.33</span></span></td>
    <td><span data-ttu-id="4ae6b-225">9.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-225">9.00</span></span></td>
    <td><span data-ttu-id="4ae6b-226">825.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae6b-227">1000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-227">1000</span></span></td>
    <td><span data-ttu-id="4ae6b-228">2</span><span class="sxs-lookup"><span data-stu-id="4ae6b-228">2</span></span></td>
    <td><span data-ttu-id="4ae6b-229">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-229">10</span></span></td>
    <td><span data-ttu-id="4ae6b-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-230">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae6b-231">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-231">10</span></span></td>
    <td><span data-ttu-id="4ae6b-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-232">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae6b-233">200.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-234">10.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-234">10.00</span></span></td>
    <td><span data-ttu-id="4ae6b-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="4ae6b-236"><strong>1000 Totalen</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="4ae6b-243">Let op de volgende details in dit voorbeeldrapport:</span><span class="sxs-lookup"><span data-stu-id="4ae6b-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="4ae6b-244">De waarden van **Hoeveelheid voorraadwaarde**, **Voorraadwaarde** en **Gemiddelde eenheidskosten** die in het rapport worden weergegeven, zijn waarden voor de financiële voorraaddimensie (**site** in dit geval).</span><span class="sxs-lookup"><span data-stu-id="4ae6b-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="4ae6b-245">Voor site 1 bevat het rapport bijvoorbeeld de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="4ae6b-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="4ae6b-246">De **Hoeveelheid voorraadwaarde** is *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="4ae6b-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="4ae6b-247">De **Voorraadwaarde** is *1.283,33* (= 1.000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="4ae6b-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="4ae6b-248">De **Gemiddelde eenheidskosten** is *91,67*.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="4ae6b-249">De waarde voor **Voorhanden voorraad** en de waarde voor **Bedrag** in elke periodebucket worden berekend met behulp van **Gemiddelde eenheidskosten**.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="4ae6b-250">Het rapport bepaalt de voorhanden hoeveelheid voor elke periodebucket door de totale ontvangen voorraadhoeveelheid voor elke periodebucket samen te vatten.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="4ae6b-251">Vervolgens wordt het FIFO-principe (First In, First Out) toegepast om de totale uitgegeven hoeveelheid af te trekken, ongeacht het voorraadmodel dat de artikelen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="4ae6b-252">Als u hetzelfde rapport opnieuw uitvoert, maar deze keer de velden **Site** en **Magazijn** instelt op *Weergeven*, ziet het nieuwe rapport eruit als in het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="4ae6b-253">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="4ae6b-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-254">Locatie</span><span class="sxs-lookup"><span data-stu-id="4ae6b-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-255">Magazijn</span><span class="sxs-lookup"><span data-stu-id="4ae6b-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-256">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-257">Waarde voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="4ae6b-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-258">Hoeveelheid voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="4ae6b-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-259">Voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="4ae6b-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-260">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="4ae6b-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-261">8/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-262">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-263">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="4ae6b-264">P1:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-265">P1:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="4ae6b-266">P2:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-267">P2:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="4ae6b-268">P3:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-269">P3:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="4ae6b-270">1000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-270">1000</span></span></td>
    <td><span data-ttu-id="4ae6b-271">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-271">1</span></span></td>
    <td><span data-ttu-id="4ae6b-272">11</span><span class="sxs-lookup"><span data-stu-id="4ae6b-272">11</span></span></td>
    <td><span data-ttu-id="4ae6b-273">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-273">10</span></span></td>
    <td><span data-ttu-id="4ae6b-274">916.67</span><span class="sxs-lookup"><span data-stu-id="4ae6b-274">916.67</span></span></td>
    <td><span data-ttu-id="4ae6b-275">14</span><span class="sxs-lookup"><span data-stu-id="4ae6b-275">14</span></span></td>
    <td><span data-ttu-id="4ae6b-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-276">1,283.33</span></span></td>
    <td><span data-ttu-id="4ae6b-277">91.67</span><span class="sxs-lookup"><span data-stu-id="4ae6b-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-278">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-278">5.00</span></span></td>
    <td><span data-ttu-id="4ae6b-279">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-279">458.33</span></span></td>
    <td><span data-ttu-id="4ae6b-280">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-280">5.00</span></span></td>
    <td><span data-ttu-id="4ae6b-281">458.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae6b-282">1000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-282">1000</span></span></td>
    <td><span data-ttu-id="4ae6b-283">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-283">1</span></span></td>
    <td><span data-ttu-id="4ae6b-284">12</span><span class="sxs-lookup"><span data-stu-id="4ae6b-284">12</span></span></td>
    <td><span data-ttu-id="4ae6b-285">4</span><span class="sxs-lookup"><span data-stu-id="4ae6b-285">4</span></span></td>
    <td><span data-ttu-id="4ae6b-286">366.67</span><span class="sxs-lookup"><span data-stu-id="4ae6b-286">366.67</span></span></td>
    <td><span data-ttu-id="4ae6b-287">14</span><span class="sxs-lookup"><span data-stu-id="4ae6b-287">14</span></span></td>
    <td><span data-ttu-id="4ae6b-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="4ae6b-288">1,283.33</span></span></td>
    <td><span data-ttu-id="4ae6b-289">91.67</span><span class="sxs-lookup"><span data-stu-id="4ae6b-289">91.67</span></span></td>
    <td><span data-ttu-id="4ae6b-290">4.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-290">4.00</span></span></td>
    <td><span data-ttu-id="4ae6b-291">366.67</span><span class="sxs-lookup"><span data-stu-id="4ae6b-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae6b-292">1000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-292">1000</span></span></td>
    <td><span data-ttu-id="4ae6b-293">2</span><span class="sxs-lookup"><span data-stu-id="4ae6b-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-294">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-294">10</span></span></td>
    <td><span data-ttu-id="4ae6b-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-295">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae6b-296">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-296">10</span></span></td>
    <td><span data-ttu-id="4ae6b-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-297">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae6b-298">200.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-299">10.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-299">10.00</span></span></td>
    <td><span data-ttu-id="4ae6b-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="4ae6b-301"><strong>1000 Totalen</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="4ae6b-310">Deze keer wordt site 1 opgesplitst in twee rijen, één voor magazijn 11 en één voor magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="4ae6b-311">De waarden van **Hoeveelheid voorraadwaarde**, **Voorraadwaarde** en **Gemiddelde eenheidskosten** zijn echter hetzelfde, omdat **Magazijn** geen financiële voorraaddimensie is.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="4ae6b-312">U ziet ook dat de hoeveelheidsdistributie van site 1 afwijkt.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="4ae6b-313">In het eerste rapport dat u hebt uitgevoerd, is de overdrachtsorder genegeerd die zich op dezelfde locatie heeft voorgedaan en wordt de hoeveelheid van de verkoopfactuur in mindering gebracht op de periodebucket **31/3/2020-1/3/2020** in site 1.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="4ae6b-314">In het nieuwe rapport trekt het systeem echter de hoeveelheid van de verkoopfactuur af van de periodebucket **8/5/2020-1/5/2020** in magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="4ae6b-315">Effecten van voorraadafsluiting</span><span class="sxs-lookup"><span data-stu-id="4ae6b-315">Effects of inventory closing</span></span>

<span data-ttu-id="4ae6b-316">Als u de voorraadafsluiting uitvoert voor mei en vervolgens het vorige rapport opnieuw uitvoert, maar het veld **Begindatum** instelt op *31 mei 2020* , zult u de volgende resultaten opmerken:</span><span class="sxs-lookup"><span data-stu-id="4ae6b-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="4ae6b-317">De waarden voor **Voorraadwaarde** en **Gemiddelde eenheidskosten** worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="4ae6b-318">De **Waarde voorhanden voorraad** en alle waarden voor **Bedrag** in elke periodebucket worden dienovereenkomstig bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="4ae6b-319">Het nieuwe rapport lijkt op het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="4ae6b-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="4ae6b-320">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="4ae6b-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-321">Locatie</span><span class="sxs-lookup"><span data-stu-id="4ae6b-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-322">Magazijn</span><span class="sxs-lookup"><span data-stu-id="4ae6b-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-323">Voorhanden hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-324">Waarde voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="4ae6b-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-325">Hoeveelheid voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="4ae6b-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-326">Voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="4ae6b-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="4ae6b-327">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="4ae6b-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-328">31/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-329">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="4ae6b-330">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="4ae6b-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="4ae6b-331">P1:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-332">P1:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="4ae6b-333">P2:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-334">P2:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="4ae6b-335">P3:Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="4ae6b-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="4ae6b-336">P3:Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ae6b-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="4ae6b-337">1000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-337">1000</span></span></td>
    <td><span data-ttu-id="4ae6b-338">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-338">1</span></span></td>
    <td><span data-ttu-id="4ae6b-339">11</span><span class="sxs-lookup"><span data-stu-id="4ae6b-339">11</span></span></td>
    <td><span data-ttu-id="4ae6b-340">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-340">10</span></span></td>
    <td><span data-ttu-id="4ae6b-341">910.70</span><span class="sxs-lookup"><span data-stu-id="4ae6b-341">910.70</span></span></td>
    <td><span data-ttu-id="4ae6b-342">14</span><span class="sxs-lookup"><span data-stu-id="4ae6b-342">14</span></span></td>
    <td><span data-ttu-id="4ae6b-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-343">1,275.00</span></span></td>
    <td><span data-ttu-id="4ae6b-344">91.07</span><span class="sxs-lookup"><span data-stu-id="4ae6b-344">91.07</span></span></td>
    <td><span data-ttu-id="4ae6b-345">0,00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-346">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-346">5.00</span></span></td>
    <td><span data-ttu-id="4ae6b-347">455.36</span><span class="sxs-lookup"><span data-stu-id="4ae6b-347">455.36</span></span></td>
    <td><span data-ttu-id="4ae6b-348">5.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-348">5.00</span></span></td>
    <td><span data-ttu-id="4ae6b-349">455.36</span><span class="sxs-lookup"><span data-stu-id="4ae6b-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae6b-350">1000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-350">1000</span></span></td>
    <td><span data-ttu-id="4ae6b-351">1</span><span class="sxs-lookup"><span data-stu-id="4ae6b-351">1</span></span></td>
    <td><span data-ttu-id="4ae6b-352">12</span><span class="sxs-lookup"><span data-stu-id="4ae6b-352">12</span></span></td>
    <td><span data-ttu-id="4ae6b-353">4</span><span class="sxs-lookup"><span data-stu-id="4ae6b-353">4</span></span></td>
    <td><span data-ttu-id="4ae6b-354">364.29</span><span class="sxs-lookup"><span data-stu-id="4ae6b-354">364.29</span></span></td>
    <td><span data-ttu-id="4ae6b-355">14</span><span class="sxs-lookup"><span data-stu-id="4ae6b-355">14</span></span></td>
    <td><span data-ttu-id="4ae6b-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-356">1,275.00</span></span></td>
    <td><span data-ttu-id="4ae6b-357">91.07</span><span class="sxs-lookup"><span data-stu-id="4ae6b-357">91.07</span></span></td>
    <td><span data-ttu-id="4ae6b-358">4.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-358">4.00</span></span></td>
    <td><span data-ttu-id="4ae6b-359">364.29</span><span class="sxs-lookup"><span data-stu-id="4ae6b-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="4ae6b-360">1000</span><span class="sxs-lookup"><span data-stu-id="4ae6b-360">1000</span></span></td>
    <td><span data-ttu-id="4ae6b-361">2</span><span class="sxs-lookup"><span data-stu-id="4ae6b-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-362">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-362">10</span></span></td>
    <td><span data-ttu-id="4ae6b-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-363">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae6b-364">10</span><span class="sxs-lookup"><span data-stu-id="4ae6b-364">10</span></span></td>
    <td><span data-ttu-id="4ae6b-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-365">2,000.00</span></span></td>
    <td><span data-ttu-id="4ae6b-366">200.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-367">10.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-367">10.00</span></span></td>
    <td><span data-ttu-id="4ae6b-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="4ae6b-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="4ae6b-369"><strong>1000 Totalen</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="4ae6b-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="4ae6b-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="4ae6b-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
