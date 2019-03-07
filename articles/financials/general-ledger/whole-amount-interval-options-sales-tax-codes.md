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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "344059"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="07626-103">Berekeningsopties Volledige bedrag en Interval voor btw-codes</span><span class="sxs-lookup"><span data-stu-id="07626-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="07626-104">In dit artikel worden de opties voor het veld Berekeningsmethode voor btw-codes uitgelegd en wordt uitgelegd hoe btw wordt berekend voor intervallen en gehele bedragen.</span><span class="sxs-lookup"><span data-stu-id="07626-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="07626-105">U kunt een btw-code instellen die moet worden berekend op basis van het gehele bedrag of een intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="07626-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="07626-106">Gebruik op de pagina Btw-codes het veld Berekeningsmethode op het sneltabblad Berekening om te selecteren hoe u een btw-code berekent.</span><span class="sxs-lookup"><span data-stu-id="07626-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="07626-107">Volledige bedrag – Het btw-tarief wordt toegepast op het gehele belastbare bedrag.</span><span class="sxs-lookup"><span data-stu-id="07626-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="07626-108">Interval – Het belastbare bedrag is verdeeld in delen en elk deel valt in een bereik met een bepaald btw-tarief.</span><span class="sxs-lookup"><span data-stu-id="07626-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="07626-109">Het deel van het bedrag dat in een bepaald interval valt, wordt belast volgens het btw-tarief voor dat interval.</span><span class="sxs-lookup"><span data-stu-id="07626-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="07626-110">De btw is de som van de btw-bedragen die worden berekend voor elk intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="07626-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="07626-111">De optie Interval is alleen beschikbaar wanneer u Regel selecteert in het veld Berekeningsmethode in het btw-gebied van de pagina Grootboekparameters.</span><span class="sxs-lookup"><span data-stu-id="07626-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="07626-112">Intervallen worden ingesteld op de pagina Waarden btw-code door bedragen voor Ondergrens en Bovengrens in te voeren per btw-tarief.</span><span class="sxs-lookup"><span data-stu-id="07626-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="07626-113">Voor btw die moet worden berekend over alle belastbare bedragen - ongeacht welke berekeningsmethode is geselecteerd - moeten de intervallen voldoen aan de volgende regels:</span><span class="sxs-lookup"><span data-stu-id="07626-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="07626-114">Het eerste interval moet een ondergrens van nul hebben.</span><span class="sxs-lookup"><span data-stu-id="07626-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="07626-115">Het laatste interval moet een bovengrens van nul hebben, wat oneindig betekent.</span><span class="sxs-lookup"><span data-stu-id="07626-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="07626-116">De bovengrens van een interval moet de ondergrens van het volgende interval zijn.</span><span class="sxs-lookup"><span data-stu-id="07626-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="07626-117">Als een bedrag de bovengrens van het vorige interval en de ondergrens van het volgende interval is, wordt het tarief van het eerste interval toegepast op het bedrag.</span><span class="sxs-lookup"><span data-stu-id="07626-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="07626-118">Als een bedrag buiten de intervallen valt die zijn gedefinieerd door de boven- en ondergrens, wordt een btw-tarief van 0 toegepast.</span><span class="sxs-lookup"><span data-stu-id="07626-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="07626-119">Voorbeeld: Berekeningsmethode is volledige bedrag</span><span class="sxs-lookup"><span data-stu-id="07626-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="07626-120">Op de pagina Waarden btw-code worden de btw-tarieven ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="07626-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="07626-121">**Ondergrens**</span><span class="sxs-lookup"><span data-stu-id="07626-121">**Minimum limit**</span></span> | <span data-ttu-id="07626-122">**Bovengrens**</span><span class="sxs-lookup"><span data-stu-id="07626-122">**Maximum limit**</span></span> | <span data-ttu-id="07626-123">**Btw-tarief**</span><span class="sxs-lookup"><span data-stu-id="07626-123">**Tax rate**</span></span> |
| <span data-ttu-id="07626-124">0,00</span><span class="sxs-lookup"><span data-stu-id="07626-124">0.00</span></span>              | <span data-ttu-id="07626-125">50,00</span><span class="sxs-lookup"><span data-stu-id="07626-125">50.00</span></span>             | <span data-ttu-id="07626-126">30%</span><span class="sxs-lookup"><span data-stu-id="07626-126">30%</span></span>          |
| <span data-ttu-id="07626-127">50,00</span><span class="sxs-lookup"><span data-stu-id="07626-127">50.00</span></span>             | <span data-ttu-id="07626-128">100,00</span><span class="sxs-lookup"><span data-stu-id="07626-128">100.00</span></span>            | <span data-ttu-id="07626-129">20%</span><span class="sxs-lookup"><span data-stu-id="07626-129">20%</span></span>          |
| <span data-ttu-id="07626-130">100,00</span><span class="sxs-lookup"><span data-stu-id="07626-130">100.00</span></span>            | <span data-ttu-id="07626-131">0,00</span><span class="sxs-lookup"><span data-stu-id="07626-131">0.00</span></span>              | <span data-ttu-id="07626-132">10%</span><span class="sxs-lookup"><span data-stu-id="07626-132">10%</span></span>          |

<span data-ttu-id="07626-133">De btw wordt berekend op het volledige belastbare bedrag.</span><span class="sxs-lookup"><span data-stu-id="07626-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="07626-134">Belastbaar bedrag (prijs)</span><span class="sxs-lookup"><span data-stu-id="07626-134">Taxable amount (price)</span></span> | <span data-ttu-id="07626-135">Berekening</span><span class="sxs-lookup"><span data-stu-id="07626-135">Calculation</span></span>    | <span data-ttu-id="07626-136">Btw</span><span class="sxs-lookup"><span data-stu-id="07626-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="07626-137">35,00</span><span class="sxs-lookup"><span data-stu-id="07626-137">35.00</span></span>                  | <span data-ttu-id="07626-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="07626-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="07626-139">EUR 10,50</span><span class="sxs-lookup"><span data-stu-id="07626-139">10.50</span></span>     |
| <span data-ttu-id="07626-140">50,00</span><span class="sxs-lookup"><span data-stu-id="07626-140">50.00</span></span>                  | <span data-ttu-id="07626-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="07626-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="07626-142">15,00</span><span class="sxs-lookup"><span data-stu-id="07626-142">15.00</span></span>     |
| <span data-ttu-id="07626-143">85,00</span><span class="sxs-lookup"><span data-stu-id="07626-143">85.00</span></span>                  | <span data-ttu-id="07626-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="07626-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="07626-145">17,00</span><span class="sxs-lookup"><span data-stu-id="07626-145">17.00</span></span>     |
| <span data-ttu-id="07626-146">305,00</span><span class="sxs-lookup"><span data-stu-id="07626-146">305.00</span></span>                 | <span data-ttu-id="07626-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="07626-147">305.00 \* 0.10</span></span> | <span data-ttu-id="07626-148">30,50</span><span class="sxs-lookup"><span data-stu-id="07626-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="07626-149">Voorbeeld: Berekeningsmethode Interval</span><span class="sxs-lookup"><span data-stu-id="07626-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="07626-150">Op de pagina Waarden worden de btw-tarieven ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="07626-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="07626-151">**Ondergrens**</span><span class="sxs-lookup"><span data-stu-id="07626-151">**Minimum limit**</span></span> | <span data-ttu-id="07626-152">**Bovengrens**</span><span class="sxs-lookup"><span data-stu-id="07626-152">**Maximum limit**</span></span> | <span data-ttu-id="07626-153">**Btw-tarief**</span><span class="sxs-lookup"><span data-stu-id="07626-153">**Tax rate**</span></span> |
| <span data-ttu-id="07626-154">0,00</span><span class="sxs-lookup"><span data-stu-id="07626-154">0.00</span></span>              | <span data-ttu-id="07626-155">50,00</span><span class="sxs-lookup"><span data-stu-id="07626-155">50.00</span></span>             | <span data-ttu-id="07626-156">30%</span><span class="sxs-lookup"><span data-stu-id="07626-156">30%</span></span>          |
| <span data-ttu-id="07626-157">50,00</span><span class="sxs-lookup"><span data-stu-id="07626-157">50.00</span></span>             | <span data-ttu-id="07626-158">100,00</span><span class="sxs-lookup"><span data-stu-id="07626-158">100.00</span></span>            | <span data-ttu-id="07626-159">20%</span><span class="sxs-lookup"><span data-stu-id="07626-159">20%</span></span>          |
| <span data-ttu-id="07626-160">100,00</span><span class="sxs-lookup"><span data-stu-id="07626-160">100.00</span></span>            | <span data-ttu-id="07626-161">0,00</span><span class="sxs-lookup"><span data-stu-id="07626-161">0.00</span></span>              | <span data-ttu-id="07626-162">10%</span><span class="sxs-lookup"><span data-stu-id="07626-162">10%</span></span>          |

<span data-ttu-id="07626-163">De btw is de som van de btw-bedragen die worden berekend voor elk intervalbedrag.</span><span class="sxs-lookup"><span data-stu-id="07626-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="07626-164">Belastbaar bedrag (prijs)</span><span class="sxs-lookup"><span data-stu-id="07626-164">Taxable amount (price)</span></span> | <span data-ttu-id="07626-165">Berekening</span><span class="sxs-lookup"><span data-stu-id="07626-165">Calculation</span></span>                                                               | <span data-ttu-id="07626-166">Btw</span><span class="sxs-lookup"><span data-stu-id="07626-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="07626-167">35,00</span><span class="sxs-lookup"><span data-stu-id="07626-167">35.00</span></span>                  | <span data-ttu-id="07626-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="07626-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="07626-169">EUR 10,50</span><span class="sxs-lookup"><span data-stu-id="07626-169">10.50</span></span>     |
| <span data-ttu-id="07626-170">50,00</span><span class="sxs-lookup"><span data-stu-id="07626-170">50.00</span></span>                  | <span data-ttu-id="07626-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="07626-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="07626-172">15,00</span><span class="sxs-lookup"><span data-stu-id="07626-172">15.00</span></span>     |
| <span data-ttu-id="07626-173">85,00</span><span class="sxs-lookup"><span data-stu-id="07626-173">85.00</span></span>                  | <span data-ttu-id="07626-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="07626-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="07626-175">22,00</span><span class="sxs-lookup"><span data-stu-id="07626-175">22.00</span></span>     |
| <span data-ttu-id="07626-176">305,00</span><span class="sxs-lookup"><span data-stu-id="07626-176">305.00</span></span>                 | <span data-ttu-id="07626-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="07626-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="07626-178">45,50</span><span class="sxs-lookup"><span data-stu-id="07626-178">45.50</span></span>     |



<span data-ttu-id="07626-179">Zie voor meer informatie het onderwerp [Btw-tarieven bepalen op basis van de velden Marginale basis en Berekeningsmethode](marginal-base-field.md)</span><span class="sxs-lookup"><span data-stu-id="07626-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





