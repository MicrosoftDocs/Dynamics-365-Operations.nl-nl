---
title: Reductiesleutels
description: Dit artikel bevat voorbeelden die het instellen van een reductiesleutel weergeven. Het bevat informatie over de verschillende reductiesleutelinstellingen en de resultaten van elk. U kunt een reductiesleutel gebruiken om te definiëren hoe prognosebehoeften worden gereduceerd.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7457aca4ca4d5188bafb497d3052276cfc154ad1
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2019
ms.locfileid: "770911"
---
# <a name="reduction-keys"></a><span data-ttu-id="3d662-105">Reductiesleutels</span><span class="sxs-lookup"><span data-stu-id="3d662-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d662-106">Dit artikel bevat voorbeelden die het instellen van een reductiesleutel weergeven.</span><span class="sxs-lookup"><span data-stu-id="3d662-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="3d662-107">Het bevat informatie over de verschillende reductiesleutelinstellingen en de resultaten van elk.</span><span class="sxs-lookup"><span data-stu-id="3d662-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="3d662-108">U kunt een reductiesleutel gebruiken om te definiëren hoe prognosebehoeften worden gereduceerd.</span><span class="sxs-lookup"><span data-stu-id="3d662-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="3d662-109">Voorbeeld 1: prognosereductiemethode Percentage - reductiesleutel</span><span class="sxs-lookup"><span data-stu-id="3d662-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="3d662-110">In dit voorbeeld wordt weergegeven hoe een reductiesleutel vraagprognosebehoeften reduceert overeenkomstig de percentages en perioden die door de reductiesleutel worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="3d662-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="3d662-111">Stel op de pagina **Reductiesleutels** de volgende regels in.</span><span class="sxs-lookup"><span data-stu-id="3d662-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="3d662-112">Wisselgeld</span><span class="sxs-lookup"><span data-stu-id="3d662-112">Change</span></span> | <span data-ttu-id="3d662-113">Eenheid</span><span class="sxs-lookup"><span data-stu-id="3d662-113">Unit</span></span>  | <span data-ttu-id="3d662-114">Procent</span><span class="sxs-lookup"><span data-stu-id="3d662-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="3d662-115">1</span><span class="sxs-lookup"><span data-stu-id="3d662-115">1</span></span>    | <span data-ttu-id="3d662-116">Maand</span><span class="sxs-lookup"><span data-stu-id="3d662-116">Month</span></span> |   <span data-ttu-id="3d662-117">100</span><span class="sxs-lookup"><span data-stu-id="3d662-117">100</span></span>   |
   |   <span data-ttu-id="3d662-118">2</span><span class="sxs-lookup"><span data-stu-id="3d662-118">2</span></span>    | <span data-ttu-id="3d662-119">Maand</span><span class="sxs-lookup"><span data-stu-id="3d662-119">Month</span></span> |   <span data-ttu-id="3d662-120">75</span><span class="sxs-lookup"><span data-stu-id="3d662-120">75</span></span>    |
   |   <span data-ttu-id="3d662-121">3</span><span class="sxs-lookup"><span data-stu-id="3d662-121">3</span></span>    | <span data-ttu-id="3d662-122">Maand</span><span class="sxs-lookup"><span data-stu-id="3d662-122">Month</span></span> |   <span data-ttu-id="3d662-123">50</span><span class="sxs-lookup"><span data-stu-id="3d662-123">50</span></span>    |
   |   <span data-ttu-id="3d662-124">4</span><span class="sxs-lookup"><span data-stu-id="3d662-124">4</span></span>    | <span data-ttu-id="3d662-125">Maand</span><span class="sxs-lookup"><span data-stu-id="3d662-125">Month</span></span> |   <span data-ttu-id="3d662-126">25</span><span class="sxs-lookup"><span data-stu-id="3d662-126">25</span></span>    |


2. <span data-ttu-id="3d662-127">Koppel de reductiesleutel aan de behoefteplanningsgroep van het artikel.</span><span class="sxs-lookup"><span data-stu-id="3d662-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="3d662-128">Selecteer op de pagina **Hoofdplannen** in het veld **Reductiemethode** de optie **Percentage - reductiesleutel**.</span><span class="sxs-lookup"><span data-stu-id="3d662-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="3d662-129">Maak een vraagprognose van 1000 stuks per maand.</span><span class="sxs-lookup"><span data-stu-id="3d662-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="3d662-130">Als u de prognoseplanning op 1 januari uitvoert, worden de vraagprognosebehoeften verbruikt volgens de percentages die u instelt op de pagina **Reductiesleutels**.</span><span class="sxs-lookup"><span data-stu-id="3d662-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="3d662-131">De volgende behoeftehoeveelheden worden naar het hoofdplan overgebracht.</span><span class="sxs-lookup"><span data-stu-id="3d662-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="3d662-132">Maand</span><span class="sxs-lookup"><span data-stu-id="3d662-132">Month</span></span>                | <span data-ttu-id="3d662-133">Benodigd aantal stuks</span><span class="sxs-lookup"><span data-stu-id="3d662-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="3d662-134">januari</span><span class="sxs-lookup"><span data-stu-id="3d662-134">January</span></span>              | <span data-ttu-id="3d662-135">0</span><span class="sxs-lookup"><span data-stu-id="3d662-135">0</span></span>                         |
| <span data-ttu-id="3d662-136">februari</span><span class="sxs-lookup"><span data-stu-id="3d662-136">February</span></span>             | <span data-ttu-id="3d662-137">250</span><span class="sxs-lookup"><span data-stu-id="3d662-137">250</span></span>                       |
| <span data-ttu-id="3d662-138">maart</span><span class="sxs-lookup"><span data-stu-id="3d662-138">March</span></span>                | <span data-ttu-id="3d662-139">500</span><span class="sxs-lookup"><span data-stu-id="3d662-139">500</span></span>                       |
| <span data-ttu-id="3d662-140">april</span><span class="sxs-lookup"><span data-stu-id="3d662-140">April</span></span>                | <span data-ttu-id="3d662-141">750</span><span class="sxs-lookup"><span data-stu-id="3d662-141">750</span></span>                       |
| <span data-ttu-id="3d662-142">Mei tot en met december</span><span class="sxs-lookup"><span data-stu-id="3d662-142">May through December</span></span> | <span data-ttu-id="3d662-143">1.000</span><span class="sxs-lookup"><span data-stu-id="3d662-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="3d662-144">Voorbeeld 2: prognosereductiemethode Transacties - reductiesleutel</span><span class="sxs-lookup"><span data-stu-id="3d662-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="3d662-145">In dit voorbeeld wordt weergegeven hoe werkelijke orders, die plaatsvinden tijdens de perioden die zijn gedefinieerd door de reductiesleutel, vraagprognosebehoeften reduceren.</span><span class="sxs-lookup"><span data-stu-id="3d662-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="3d662-146">Selecteer op de pagina **Hoofdplannen** in het veld **Reductiemethode** de optie **Transacties - reductiesleutel**.</span><span class="sxs-lookup"><span data-stu-id="3d662-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="3d662-147">Op 1 januari waren er de volgende verkooporders.</span><span class="sxs-lookup"><span data-stu-id="3d662-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="3d662-148">Maand</span><span class="sxs-lookup"><span data-stu-id="3d662-148">Month</span></span>    | <span data-ttu-id="3d662-149">Besteld aantal stuks</span><span class="sxs-lookup"><span data-stu-id="3d662-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="3d662-150">januari</span><span class="sxs-lookup"><span data-stu-id="3d662-150">January</span></span>  | <span data-ttu-id="3d662-151">956</span><span class="sxs-lookup"><span data-stu-id="3d662-151">956</span></span>                      |
| <span data-ttu-id="3d662-152">februari</span><span class="sxs-lookup"><span data-stu-id="3d662-152">February</span></span> | <span data-ttu-id="3d662-153">1.176</span><span class="sxs-lookup"><span data-stu-id="3d662-153">1,176</span></span>                    |
| <span data-ttu-id="3d662-154">maart</span><span class="sxs-lookup"><span data-stu-id="3d662-154">March</span></span>    | <span data-ttu-id="3d662-155">451</span><span class="sxs-lookup"><span data-stu-id="3d662-155">451</span></span>                      |
| <span data-ttu-id="3d662-156">april</span><span class="sxs-lookup"><span data-stu-id="3d662-156">April</span></span>    | <span data-ttu-id="3d662-157">119</span><span class="sxs-lookup"><span data-stu-id="3d662-157">119</span></span>                      |

<span data-ttu-id="3d662-158">Als u dezelfde vraagprognose van 1000 stuks per maand gebruikt, worden de volgende behoeftehoeveelheden naar het hoofdplan overgebracht.</span><span class="sxs-lookup"><span data-stu-id="3d662-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="3d662-159">Maand</span><span class="sxs-lookup"><span data-stu-id="3d662-159">Month</span></span>                | <span data-ttu-id="3d662-160">Benodigd aantal stuks</span><span class="sxs-lookup"><span data-stu-id="3d662-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="3d662-161">januari</span><span class="sxs-lookup"><span data-stu-id="3d662-161">January</span></span>              | <span data-ttu-id="3d662-162">44</span><span class="sxs-lookup"><span data-stu-id="3d662-162">44</span></span>                        |
| <span data-ttu-id="3d662-163">februari</span><span class="sxs-lookup"><span data-stu-id="3d662-163">February</span></span>             | <span data-ttu-id="3d662-164">0</span><span class="sxs-lookup"><span data-stu-id="3d662-164">0</span></span>                         |
| <span data-ttu-id="3d662-165">maart</span><span class="sxs-lookup"><span data-stu-id="3d662-165">March</span></span>                | <span data-ttu-id="3d662-166">549</span><span class="sxs-lookup"><span data-stu-id="3d662-166">549</span></span>                       |
| <span data-ttu-id="3d662-167">april</span><span class="sxs-lookup"><span data-stu-id="3d662-167">April</span></span>                | <span data-ttu-id="3d662-168">881</span><span class="sxs-lookup"><span data-stu-id="3d662-168">881</span></span>                       |
| <span data-ttu-id="3d662-169">Mei tot en met december</span><span class="sxs-lookup"><span data-stu-id="3d662-169">May through December</span></span> | <span data-ttu-id="3d662-170">1.000</span><span class="sxs-lookup"><span data-stu-id="3d662-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="3d662-171">Voorbeeld 3: prognosereductiemethode Transacties - dynamische periode</span><span class="sxs-lookup"><span data-stu-id="3d662-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="3d662-172">In de meeste gevallen worden systemen zo ingesteld dat transacties vraagprognose reduceren in specifieke prognoseperioden: weken, maanden, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="3d662-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="3d662-173">Deze perioden worden gedefinieerd in de reductiesleutel.</span><span class="sxs-lookup"><span data-stu-id="3d662-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="3d662-174">De tijd tussen twee vraagprognoseregels kan echter ook een periode *impliceren*.</span><span class="sxs-lookup"><span data-stu-id="3d662-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="3d662-175">Maak een vraagprognose voor de volgende datums en hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="3d662-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="3d662-176">Datum</span><span class="sxs-lookup"><span data-stu-id="3d662-176">Date</span></span>       | <span data-ttu-id="3d662-177">Vraagprognose</span><span class="sxs-lookup"><span data-stu-id="3d662-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="3d662-178">1 januari</span><span class="sxs-lookup"><span data-stu-id="3d662-178">January 1</span></span>  | <span data-ttu-id="3d662-179">1.000</span><span class="sxs-lookup"><span data-stu-id="3d662-179">1,000</span></span>           |
   | <span data-ttu-id="3d662-180">5 januari</span><span class="sxs-lookup"><span data-stu-id="3d662-180">January 5</span></span>  | <span data-ttu-id="3d662-181">500</span><span class="sxs-lookup"><span data-stu-id="3d662-181">500</span></span>             |
   | <span data-ttu-id="3d662-182">12 januari</span><span class="sxs-lookup"><span data-stu-id="3d662-182">January 12</span></span> | <span data-ttu-id="3d662-183">1.000</span><span class="sxs-lookup"><span data-stu-id="3d662-183">1,000</span></span>           |

   <span data-ttu-id="3d662-184">In deze prognose is er geen duidelijke periode tussen de prognosedatums: tussen de eerste en tweede datum is er een vierdaags tijdsbestek en tussen de tweede en derde datum is er een zevendaags tijdsbestek.</span><span class="sxs-lookup"><span data-stu-id="3d662-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="3d662-185">Dit zijn de dynamische perioden.</span><span class="sxs-lookup"><span data-stu-id="3d662-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="3d662-186">Maak als volgt verkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="3d662-186">Create sales order lines as follows.</span></span>

   | <span data-ttu-id="3d662-187">Datum</span><span class="sxs-lookup"><span data-stu-id="3d662-187">Date</span></span>                             | <span data-ttu-id="3d662-188">Verkooporderhoeveelheid</span><span class="sxs-lookup"><span data-stu-id="3d662-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="3d662-189">15 december in het vorige jaar</span><span class="sxs-lookup"><span data-stu-id="3d662-189">December 15 in the previous year</span></span> | <span data-ttu-id="3d662-190">500</span><span class="sxs-lookup"><span data-stu-id="3d662-190">500</span></span>                  |
   | <span data-ttu-id="3d662-191">3 januari</span><span class="sxs-lookup"><span data-stu-id="3d662-191">January 3</span></span>                        | <span data-ttu-id="3d662-192">100</span><span class="sxs-lookup"><span data-stu-id="3d662-192">100</span></span>                  |
   | <span data-ttu-id="3d662-193">10 januari</span><span class="sxs-lookup"><span data-stu-id="3d662-193">January 10</span></span>                       | <span data-ttu-id="3d662-194">200</span><span class="sxs-lookup"><span data-stu-id="3d662-194">200</span></span>                  |

<span data-ttu-id="3d662-195">De prognose wordt als volgt gereduceerd:</span><span class="sxs-lookup"><span data-stu-id="3d662-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="3d662-196">De eerste verkooporder ligt niet binnen een periode, zodat het de prognose niet reduceert.</span><span class="sxs-lookup"><span data-stu-id="3d662-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="3d662-197">De tweede verkooporder ligt tussen 1 januari en 5 januari, zodat het de prognose voor 1 januari met 100 reduceert.</span><span class="sxs-lookup"><span data-stu-id="3d662-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="3d662-198">De derde verkooporder ligt tussen 5 januari en 12 januari, zodat het de prognose voor 5 januari met 200 reduceert.</span><span class="sxs-lookup"><span data-stu-id="3d662-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="3d662-199">De volgende geplande order wordt gemaakt om de prognose te vervullen.</span><span class="sxs-lookup"><span data-stu-id="3d662-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="3d662-200">Vraagprognosedatum</span><span class="sxs-lookup"><span data-stu-id="3d662-200">Demand forecast date</span></span> | <span data-ttu-id="3d662-201">Gereduceerde hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="3d662-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="3d662-202">1 januari</span><span class="sxs-lookup"><span data-stu-id="3d662-202">January 1</span></span>            | <span data-ttu-id="3d662-203">900</span><span class="sxs-lookup"><span data-stu-id="3d662-203">900</span></span>              |
| <span data-ttu-id="3d662-204">5 januari</span><span class="sxs-lookup"><span data-stu-id="3d662-204">January 5</span></span>            | <span data-ttu-id="3d662-205">300</span><span class="sxs-lookup"><span data-stu-id="3d662-205">300</span></span>              |
| <span data-ttu-id="3d662-206">12 januari</span><span class="sxs-lookup"><span data-stu-id="3d662-206">January 12</span></span>           | <span data-ttu-id="3d662-207">1.000</span><span class="sxs-lookup"><span data-stu-id="3d662-207">1,000</span></span>            |

<span data-ttu-id="3d662-208">Hier is een overzicht van de reductie **Transacties - dynamische periode**:</span><span class="sxs-lookup"><span data-stu-id="3d662-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="3d662-209">Prognosebehoeften worden gereduceerd door de werkelijke ordertransacties die tijdens de dynamische periode plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="3d662-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="3d662-210">De dynamische periode bestrijkt de huidige prognosedatums en eindigt bij het begin van de volgende prognose.</span><span class="sxs-lookup"><span data-stu-id="3d662-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="3d662-211">Deze methode gebruikt of vereist geen reductiesleutel.</span><span class="sxs-lookup"><span data-stu-id="3d662-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="3d662-212">Wanneer deze optie wordt gebruikt, vindt het volgende gedrag plaats:</span><span class="sxs-lookup"><span data-stu-id="3d662-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="3d662-213">Als de prognose volledig is gereduceerd, worden de prognosebehoeften voor de huidige prognose 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="3d662-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="3d662-214">Als er geen toekomstige prognose is, worden de prognosebehoeften van de laatste prognose die is ingevoerd, gereduceerd.</span><span class="sxs-lookup"><span data-stu-id="3d662-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="3d662-215">De timefences worden opgenomen in de berekening van de prognosereductie.</span><span class="sxs-lookup"><span data-stu-id="3d662-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="3d662-216">Positieve dagen zijn opgenomen in de berekening van de prognosereductie.</span><span class="sxs-lookup"><span data-stu-id="3d662-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="3d662-217">Als de werkelijke ordertransacties de prognosebehoeften overschrijden, worden de resterende transacties niet naar de volgende prognoseperiode doorgestuurd.</span><span class="sxs-lookup"><span data-stu-id="3d662-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="3d662-218">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3d662-218">Additional resources</span></span>
--------

[<span data-ttu-id="3d662-219">Hoofdplannen</span><span class="sxs-lookup"><span data-stu-id="3d662-219">Master plans</span></span>](master-plans.md)



