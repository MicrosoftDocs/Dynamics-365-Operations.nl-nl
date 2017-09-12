---
title: Berekeningsopties Volledige bedrag en Interval voor btw-codes
description: In dit artikel worden de opties voor het veld Berekeningsmethode voor btw-codes uitgelegd en wordt uitgelegd hoe btw wordt berekend voor intervallen en gehele bedragen.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 55cb0f20dbd671e39d0f409a87cec93efd9ce4d6
ms.openlocfilehash: bab0f6ca21f4216b70cccf24f5781e0dbf48b7f8
ms.contentlocale: nl-nl
ms.lasthandoff: 07/07/2017


---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="3eb97-103">Berekeningsopties Volledige bedrag en Interval voor btw-codes</span><span class="sxs-lookup"><span data-stu-id="3eb97-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



<span data-ttu-id="3eb97-104">In dit artikel worden de opties voor het veld Berekeningsmethode voor btw-codes uitgelegd en wordt uitgelegd hoe btw wordt berekend voor intervallen en gehele bedragen.</span><span class="sxs-lookup"><span data-stu-id="3eb97-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="3eb97-105">U kunt een btw-code instellen die moet worden berekend op basis van het gehele bedrag of een intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="3eb97-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="3eb97-106">Gebruik op de pagina Btw-codes het veld Berekeningsmethode op het sneltabblad Berekening om te selecteren hoe u een btw-code berekent.</span><span class="sxs-lookup"><span data-stu-id="3eb97-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
-   <span data-ttu-id="3eb97-107">Volledige bedrag – Het btw-tarief wordt toegepast op het gehele belastbare bedrag.</span><span class="sxs-lookup"><span data-stu-id="3eb97-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
-   <span data-ttu-id="3eb97-108">Interval – Het belastbare bedrag is verdeeld in delen en elk deel valt in een bereik met een bepaald btw-tarief.</span><span class="sxs-lookup"><span data-stu-id="3eb97-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="3eb97-109">Het deel van het bedrag dat in een bepaald interval valt, wordt belast volgens het btw-tarief voor dat interval.</span><span class="sxs-lookup"><span data-stu-id="3eb97-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="3eb97-110">De btw is de som van de btw-bedragen die worden berekend voor elk intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="3eb97-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
> [!NOTE]                                                                                                                              
> <span data-ttu-id="3eb97-111">De optie Interval is alleen beschikbaar wanneer u Regel selecteert in het veld Berekeningsmethode in het btw-gebied van de pagina Grootboekparameters.</span><span class="sxs-lookup"><span data-stu-id="3eb97-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="3eb97-112">Intervallen worden ingesteld op de pagina Waarden btw-code door bedragen voor Ondergrens en Bovengrens in te voeren per btw-tarief.</span><span class="sxs-lookup"><span data-stu-id="3eb97-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="3eb97-113">Voor btw die moet worden berekend over alle belastbare bedragen - ongeacht welke berekeningsmethode is geselecteerd - moeten de intervallen voldoen aan de volgende regels:</span><span class="sxs-lookup"><span data-stu-id="3eb97-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="3eb97-114">Het eerste interval moet een ondergrens van nul hebben.</span><span class="sxs-lookup"><span data-stu-id="3eb97-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="3eb97-115">Het laatste interval moet een bovengrens van nul hebben, wat oneindig betekent.</span><span class="sxs-lookup"><span data-stu-id="3eb97-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="3eb97-116">De bovengrens van een interval moet de ondergrens van het volgende interval zijn.</span><span class="sxs-lookup"><span data-stu-id="3eb97-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="3eb97-117">Als een bedrag de bovengrens van het vorige interval en de ondergrens van het volgende interval is, wordt het tarief van het eerste interval toegepast op het bedrag.</span><span class="sxs-lookup"><span data-stu-id="3eb97-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="3eb97-118">Als een bedrag buiten de intervallen valt die zijn gedefinieerd door de boven- en ondergrens, wordt een btw-tarief van 0 toegepast.</span><span class="sxs-lookup"><span data-stu-id="3eb97-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="3eb97-119">Voorbeeld: Berekeningsmethode is volledige bedrag</span><span class="sxs-lookup"><span data-stu-id="3eb97-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="3eb97-120">Op de pagina Waarden btw-code worden de btw-tarieven ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="3eb97-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>
|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="3eb97-121">**Ondergrens**</span><span class="sxs-lookup"><span data-stu-id="3eb97-121">**Minimum limit**</span></span> | <span data-ttu-id="3eb97-122">**Bovengrens**</span><span class="sxs-lookup"><span data-stu-id="3eb97-122">**Maximum limit**</span></span> | <span data-ttu-id="3eb97-123">**Btw-tarief**</span><span class="sxs-lookup"><span data-stu-id="3eb97-123">**Tax rate**</span></span> |
| <span data-ttu-id="3eb97-124">0,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-124">0.00</span></span>              | <span data-ttu-id="3eb97-125">50,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-125">50.00</span></span>             | <span data-ttu-id="3eb97-126">30%</span><span class="sxs-lookup"><span data-stu-id="3eb97-126">30%</span></span>          |
| <span data-ttu-id="3eb97-127">50,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-127">50.00</span></span>             | <span data-ttu-id="3eb97-128">100,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-128">100.00</span></span>            | <span data-ttu-id="3eb97-129">20%</span><span class="sxs-lookup"><span data-stu-id="3eb97-129">20%</span></span>          |
| <span data-ttu-id="3eb97-130">100,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-130">100.00</span></span>            | <span data-ttu-id="3eb97-131">0,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-131">0.00</span></span>              | <span data-ttu-id="3eb97-132">10%</span><span class="sxs-lookup"><span data-stu-id="3eb97-132">10%</span></span>          |

<span data-ttu-id="3eb97-133">De btw wordt berekend op het volledige belastbare bedrag.</span><span class="sxs-lookup"><span data-stu-id="3eb97-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="3eb97-134">Belastbaar bedrag (prijs)</span><span class="sxs-lookup"><span data-stu-id="3eb97-134">Taxable amount (price)</span></span> | <span data-ttu-id="3eb97-135">Berekening</span><span class="sxs-lookup"><span data-stu-id="3eb97-135">Calculation</span></span>    | <span data-ttu-id="3eb97-136">Btw</span><span class="sxs-lookup"><span data-stu-id="3eb97-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="3eb97-137">35,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-137">35.00</span></span>                  | <span data-ttu-id="3eb97-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="3eb97-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="3eb97-139">EUR 10,50</span><span class="sxs-lookup"><span data-stu-id="3eb97-139">10.50</span></span>     |
| <span data-ttu-id="3eb97-140">50,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-140">50.00</span></span>                  | <span data-ttu-id="3eb97-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="3eb97-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="3eb97-142">15,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-142">15.00</span></span>     |
| <span data-ttu-id="3eb97-143">85,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-143">85.00</span></span>                  | <span data-ttu-id="3eb97-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="3eb97-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="3eb97-145">17,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-145">17.00</span></span>     |
| <span data-ttu-id="3eb97-146">305,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-146">305.00</span></span>                 | <span data-ttu-id="3eb97-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="3eb97-147">305.00 \* 0.10</span></span> | <span data-ttu-id="3eb97-148">30,50</span><span class="sxs-lookup"><span data-stu-id="3eb97-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="3eb97-149">Voorbeeld: Berekeningsmethode Interval</span><span class="sxs-lookup"><span data-stu-id="3eb97-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="3eb97-150">Op de pagina Waarden worden de btw-tarieven ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="3eb97-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="3eb97-151">**Ondergrens**</span><span class="sxs-lookup"><span data-stu-id="3eb97-151">**Minimum limit**</span></span> | <span data-ttu-id="3eb97-152">**Bovengrens**</span><span class="sxs-lookup"><span data-stu-id="3eb97-152">**Maximum limit**</span></span> | <span data-ttu-id="3eb97-153">**Btw-tarief**</span><span class="sxs-lookup"><span data-stu-id="3eb97-153">**Tax rate**</span></span> |
| <span data-ttu-id="3eb97-154">0,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-154">0.00</span></span>              | <span data-ttu-id="3eb97-155">50,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-155">50.00</span></span>             | <span data-ttu-id="3eb97-156">30%</span><span class="sxs-lookup"><span data-stu-id="3eb97-156">30%</span></span>          |
| <span data-ttu-id="3eb97-157">50,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-157">50.00</span></span>             | <span data-ttu-id="3eb97-158">100,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-158">100.00</span></span>            | <span data-ttu-id="3eb97-159">20%</span><span class="sxs-lookup"><span data-stu-id="3eb97-159">20%</span></span>          |
| <span data-ttu-id="3eb97-160">100,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-160">100.00</span></span>            | <span data-ttu-id="3eb97-161">0,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-161">0.00</span></span>              | <span data-ttu-id="3eb97-162">10%</span><span class="sxs-lookup"><span data-stu-id="3eb97-162">10%</span></span>          |

<span data-ttu-id="3eb97-163">De btw is de som van de btw-bedragen die worden berekend voor elk intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="3eb97-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="3eb97-164">Belastbaar bedrag (prijs)</span><span class="sxs-lookup"><span data-stu-id="3eb97-164">Taxable amount (price)</span></span> | <span data-ttu-id="3eb97-165">Berekening</span><span class="sxs-lookup"><span data-stu-id="3eb97-165">Calculation</span></span>                                                               | <span data-ttu-id="3eb97-166">Btw</span><span class="sxs-lookup"><span data-stu-id="3eb97-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3eb97-167">35,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-167">35.00</span></span>                  | <span data-ttu-id="3eb97-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="3eb97-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="3eb97-169">EUR 10,50</span><span class="sxs-lookup"><span data-stu-id="3eb97-169">10.50</span></span>     |
| <span data-ttu-id="3eb97-170">50,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-170">50.00</span></span>                  | <span data-ttu-id="3eb97-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="3eb97-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="3eb97-172">15,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-172">15.00</span></span>     |
| <span data-ttu-id="3eb97-173">85,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-173">85.00</span></span>                  | <span data-ttu-id="3eb97-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="3eb97-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="3eb97-175">22,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-175">22.00</span></span>     |
| <span data-ttu-id="3eb97-176">305,00</span><span class="sxs-lookup"><span data-stu-id="3eb97-176">305.00</span></span>                 | <span data-ttu-id="3eb97-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="3eb97-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="3eb97-178">45,50</span><span class="sxs-lookup"><span data-stu-id="3eb97-178">45.50</span></span>     |

 

<span data-ttu-id="3eb97-179">Zie voor meer informatie het onderwerp [Btw-tarieven bepalen op basis van de velden Marginale basis en Berekeningsmethode](marginal-base-field.md)</span><span class="sxs-lookup"><span data-stu-id="3eb97-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>






