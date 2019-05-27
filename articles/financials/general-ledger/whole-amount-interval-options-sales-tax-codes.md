---
title: Berekeningsopties Volledige bedrag en Interval voor btw-codes
description: In dit artikel worden de opties voor het veld Berekeningsmethode voor btw-codes uitgelegd en wordt uitgelegd hoe btw wordt berekend voor intervallen en gehele bedragen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16ea19a6d3cfea325281f301e0502bb051381d9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566744"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="a7b36-103">Berekeningsopties Volledige bedrag en Interval voor btw-codes</span><span class="sxs-lookup"><span data-stu-id="a7b36-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="a7b36-104">In dit artikel worden de opties voor het veld Berekeningsmethode voor btw-codes uitgelegd en wordt uitgelegd hoe btw wordt berekend voor intervallen en gehele bedragen.</span><span class="sxs-lookup"><span data-stu-id="a7b36-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="a7b36-105">U kunt een btw-code instellen die moet worden berekend op basis van het gehele bedrag of een intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="a7b36-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="a7b36-106">Gebruik op de pagina Btw-codes het veld Berekeningsmethode op het sneltabblad Berekening om te selecteren hoe u een btw-code berekent.</span><span class="sxs-lookup"><span data-stu-id="a7b36-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="a7b36-107">Volledige bedrag – Het btw-tarief wordt toegepast op het gehele belastbare bedrag.</span><span class="sxs-lookup"><span data-stu-id="a7b36-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="a7b36-108">Interval – Het belastbare bedrag is verdeeld in delen en elk deel valt in een bereik met een bepaald btw-tarief.</span><span class="sxs-lookup"><span data-stu-id="a7b36-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="a7b36-109">Het deel van het bedrag dat in een bepaald interval valt, wordt belast volgens het btw-tarief voor dat interval.</span><span class="sxs-lookup"><span data-stu-id="a7b36-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="a7b36-110">De btw is de som van de btw-bedragen die worden berekend voor elk intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="a7b36-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="a7b36-111">De optie Interval is alleen beschikbaar wanneer u Regel selecteert in het veld Berekeningsmethode in het btw-gebied van de pagina Grootboekparameters.</span><span class="sxs-lookup"><span data-stu-id="a7b36-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="a7b36-112">Intervallen worden ingesteld op de pagina Waarden btw-code door bedragen voor Ondergrens en Bovengrens in te voeren per btw-tarief.</span><span class="sxs-lookup"><span data-stu-id="a7b36-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="a7b36-113">Voor btw die moet worden berekend over alle belastbare bedragen - ongeacht welke berekeningsmethode is geselecteerd - moeten de intervallen voldoen aan de volgende regels:</span><span class="sxs-lookup"><span data-stu-id="a7b36-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="a7b36-114">Het eerste interval moet een ondergrens van nul hebben.</span><span class="sxs-lookup"><span data-stu-id="a7b36-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="a7b36-115">Het laatste interval moet een bovengrens van nul hebben, wat oneindig betekent.</span><span class="sxs-lookup"><span data-stu-id="a7b36-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="a7b36-116">De bovengrens van een interval moet de ondergrens van het volgende interval zijn.</span><span class="sxs-lookup"><span data-stu-id="a7b36-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="a7b36-117">Als een bedrag de bovengrens van het vorige interval en de ondergrens van het volgende interval is, wordt het tarief van het eerste interval toegepast op het bedrag.</span><span class="sxs-lookup"><span data-stu-id="a7b36-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="a7b36-118">Als een bedrag buiten de intervallen valt die zijn gedefinieerd door de boven- en ondergrens, wordt een btw-tarief van 0 toegepast.</span><span class="sxs-lookup"><span data-stu-id="a7b36-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="a7b36-119">Voorbeeld: Berekeningsmethode is volledige bedrag</span><span class="sxs-lookup"><span data-stu-id="a7b36-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="a7b36-120">Op de pagina Waarden btw-code worden de btw-tarieven ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="a7b36-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="a7b36-121">**Ondergrens**</span><span class="sxs-lookup"><span data-stu-id="a7b36-121">**Minimum limit**</span></span> | <span data-ttu-id="a7b36-122">**Bovengrens**</span><span class="sxs-lookup"><span data-stu-id="a7b36-122">**Maximum limit**</span></span> | <span data-ttu-id="a7b36-123">**Btw-tarief**</span><span class="sxs-lookup"><span data-stu-id="a7b36-123">**Tax rate**</span></span> |
| <span data-ttu-id="a7b36-124">0,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-124">0.00</span></span>              | <span data-ttu-id="a7b36-125">50,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-125">50.00</span></span>             | <span data-ttu-id="a7b36-126">30%</span><span class="sxs-lookup"><span data-stu-id="a7b36-126">30%</span></span>          |
| <span data-ttu-id="a7b36-127">50,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-127">50.00</span></span>             | <span data-ttu-id="a7b36-128">100,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-128">100.00</span></span>            | <span data-ttu-id="a7b36-129">20%</span><span class="sxs-lookup"><span data-stu-id="a7b36-129">20%</span></span>          |
| <span data-ttu-id="a7b36-130">100,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-130">100.00</span></span>            | <span data-ttu-id="a7b36-131">0,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-131">0.00</span></span>              | <span data-ttu-id="a7b36-132">10%</span><span class="sxs-lookup"><span data-stu-id="a7b36-132">10%</span></span>          |

<span data-ttu-id="a7b36-133">De btw wordt berekend op het volledige belastbare bedrag.</span><span class="sxs-lookup"><span data-stu-id="a7b36-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="a7b36-134">Belastbaar bedrag (prijs)</span><span class="sxs-lookup"><span data-stu-id="a7b36-134">Taxable amount (price)</span></span> | <span data-ttu-id="a7b36-135">Berekening</span><span class="sxs-lookup"><span data-stu-id="a7b36-135">Calculation</span></span>    | <span data-ttu-id="a7b36-136">Btw</span><span class="sxs-lookup"><span data-stu-id="a7b36-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="a7b36-137">35,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-137">35.00</span></span>                  | <span data-ttu-id="a7b36-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="a7b36-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="a7b36-139">EUR 10,50</span><span class="sxs-lookup"><span data-stu-id="a7b36-139">10.50</span></span>     |
| <span data-ttu-id="a7b36-140">50,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-140">50.00</span></span>                  | <span data-ttu-id="a7b36-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="a7b36-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="a7b36-142">15,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-142">15.00</span></span>     |
| <span data-ttu-id="a7b36-143">85,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-143">85.00</span></span>                  | <span data-ttu-id="a7b36-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="a7b36-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="a7b36-145">17,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-145">17.00</span></span>     |
| <span data-ttu-id="a7b36-146">305,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-146">305.00</span></span>                 | <span data-ttu-id="a7b36-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="a7b36-147">305.00 \* 0.10</span></span> | <span data-ttu-id="a7b36-148">30,50</span><span class="sxs-lookup"><span data-stu-id="a7b36-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="a7b36-149">Voorbeeld: Berekeningsmethode Interval</span><span class="sxs-lookup"><span data-stu-id="a7b36-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="a7b36-150">Op de pagina Waarden worden de btw-tarieven ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="a7b36-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="a7b36-151">**Ondergrens**</span><span class="sxs-lookup"><span data-stu-id="a7b36-151">**Minimum limit**</span></span> | <span data-ttu-id="a7b36-152">**Bovengrens**</span><span class="sxs-lookup"><span data-stu-id="a7b36-152">**Maximum limit**</span></span> | <span data-ttu-id="a7b36-153">**Btw-tarief**</span><span class="sxs-lookup"><span data-stu-id="a7b36-153">**Tax rate**</span></span> |
| <span data-ttu-id="a7b36-154">0,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-154">0.00</span></span>              | <span data-ttu-id="a7b36-155">50,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-155">50.00</span></span>             | <span data-ttu-id="a7b36-156">30%</span><span class="sxs-lookup"><span data-stu-id="a7b36-156">30%</span></span>          |
| <span data-ttu-id="a7b36-157">50,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-157">50.00</span></span>             | <span data-ttu-id="a7b36-158">100,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-158">100.00</span></span>            | <span data-ttu-id="a7b36-159">20%</span><span class="sxs-lookup"><span data-stu-id="a7b36-159">20%</span></span>          |
| <span data-ttu-id="a7b36-160">100,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-160">100.00</span></span>            | <span data-ttu-id="a7b36-161">0,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-161">0.00</span></span>              | <span data-ttu-id="a7b36-162">10%</span><span class="sxs-lookup"><span data-stu-id="a7b36-162">10%</span></span>          |

<span data-ttu-id="a7b36-163">De btw is de som van de btw-bedragen die worden berekend voor elk intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="a7b36-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="a7b36-164">Belastbaar bedrag (prijs)</span><span class="sxs-lookup"><span data-stu-id="a7b36-164">Taxable amount (price)</span></span> | <span data-ttu-id="a7b36-165">Berekening</span><span class="sxs-lookup"><span data-stu-id="a7b36-165">Calculation</span></span>                                                               | <span data-ttu-id="a7b36-166">Btw</span><span class="sxs-lookup"><span data-stu-id="a7b36-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a7b36-167">35,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-167">35.00</span></span>                  | <span data-ttu-id="a7b36-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="a7b36-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="a7b36-169">EUR 10,50</span><span class="sxs-lookup"><span data-stu-id="a7b36-169">10.50</span></span>     |
| <span data-ttu-id="a7b36-170">50,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-170">50.00</span></span>                  | <span data-ttu-id="a7b36-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="a7b36-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="a7b36-172">15,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-172">15.00</span></span>     |
| <span data-ttu-id="a7b36-173">85,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-173">85.00</span></span>                  | <span data-ttu-id="a7b36-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="a7b36-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="a7b36-175">22,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-175">22.00</span></span>     |
| <span data-ttu-id="a7b36-176">305,00</span><span class="sxs-lookup"><span data-stu-id="a7b36-176">305.00</span></span>                 | <span data-ttu-id="a7b36-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="a7b36-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="a7b36-178">45,50</span><span class="sxs-lookup"><span data-stu-id="a7b36-178">45.50</span></span>     |



<span data-ttu-id="a7b36-179">Zie voor meer informatie het onderwerp [Btw-tarieven bepalen op basis van de velden Marginale basis en Berekeningsmethode](marginal-base-field.md)</span><span class="sxs-lookup"><span data-stu-id="a7b36-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





