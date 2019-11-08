---
title: Btw-tarieven op basis van Marginale basis en Berekeningsmethoden
description: In dit onderwerp wordt beschreven hoe de waarden in de velden Marginale basis en Berekeningsmethode het btw-tarief in verkoop- en inkooptransacties bepalen.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e7e3f37d759953b7b4f70fe9eae78154da44d1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177113"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="5dcce-103">Btw-tarieven op basis van Marginale basis en Berekeningsmethoden</span><span class="sxs-lookup"><span data-stu-id="5dcce-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dcce-104">In dit onderwerp wordt beschreven hoe de waarden in de velden Marginale basis en Berekeningsmethode het btw-tarief in verkoop- en inkooptransacties bepalen.</span><span class="sxs-lookup"><span data-stu-id="5dcce-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="5dcce-105">De marginale basis op het sneltabblad Berekening van de pagina Btw-codes bepaalt welk bedrag wordt gebruikt om het gewenste btw-tarief te kiezen uit de percentages op de pagina Waarden btw-code.</span><span class="sxs-lookup"><span data-stu-id="5dcce-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="5dcce-106">Het bedragtype in het veld Marginale basis, in combinatie met de methode in het veld Berekeningsmethode, definieert de logica om het juiste btw-tarief voor een transactie te bepalen.</span><span class="sxs-lookup"><span data-stu-id="5dcce-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="5dcce-107">Verschillende combinaties van waarden in deze velden resulteren in heel verschillende btw-berekeningen, zoals u in de volgende voorbeelden kunt zien.</span><span class="sxs-lookup"><span data-stu-id="5dcce-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="5dcce-108">In de voorbeelden worden dezelfde btw-intervalwaarden gebruikt die zijn ingesteld voor elke btw-code op de pagina Waarden btw-code.</span><span class="sxs-lookup"><span data-stu-id="5dcce-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="5dcce-109">Als u deze pagina wilt openen, klikt u op de pagina Btw-codes op Btw-code &gt; Waarden.</span><span class="sxs-lookup"><span data-stu-id="5dcce-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="5dcce-110">Als de marginale basis voor een of meer van uw btw-codes is gebaseerd op een regelbedragen of eenheden, moet de waarde van het veld Berekeningsmethode op de pagina Grootboekparameters zijn ingesteld op Regel.</span><span class="sxs-lookup"><span data-stu-id="5dcce-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="5dcce-111">Nettobedrag per regel</span><span class="sxs-lookup"><span data-stu-id="5dcce-111">Net amount per line</span></span>
<span data-ttu-id="5dcce-112">Selecteer deze optie om de btw-tarieven te berekenen op basis van het nettobedrag voor de factuurregels, exclusief eventuele overige belastingen.</span><span class="sxs-lookup"><span data-stu-id="5dcce-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="5dcce-113">voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5dcce-113">Example</span></span>

<span data-ttu-id="5dcce-114">De btw-tarieven worden ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="5dcce-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="5dcce-115">Bedraginterval</span><span class="sxs-lookup"><span data-stu-id="5dcce-115">Amount interval</span></span>    | <span data-ttu-id="5dcce-116">Btw-tarief</span><span class="sxs-lookup"><span data-stu-id="5dcce-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="5dcce-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="5dcce-117">0 - 50</span></span>             | <span data-ttu-id="5dcce-118">30%</span><span class="sxs-lookup"><span data-stu-id="5dcce-118">30%</span></span>      |
| <span data-ttu-id="5dcce-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="5dcce-119">50 - 100</span></span>           | <span data-ttu-id="5dcce-120">20%</span><span class="sxs-lookup"><span data-stu-id="5dcce-120">20%</span></span>      |
| <span data-ttu-id="5dcce-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="5dcce-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="5dcce-122">10%</span><span class="sxs-lookup"><span data-stu-id="5dcce-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="5dcce-123">De bovengrens van nul (0) in het laatste interval betekent dat alle bedragen die hoger zijn dan 100, worden opgenomen in het interval.</span><span class="sxs-lookup"><span data-stu-id="5dcce-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="5dcce-124">Marginale basis: **Nettobedrag per regel**</span><span class="sxs-lookup"><span data-stu-id="5dcce-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="5dcce-125">Berekeningsmethode: **Interval**</span><span class="sxs-lookup"><span data-stu-id="5dcce-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="5dcce-126">U koopt 8 lampen die 25,00 per stuk kosten.</span><span class="sxs-lookup"><span data-stu-id="5dcce-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="5dcce-127">Het nettobedrag voor de factuurregel is EUR 200,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="5dcce-128">De btw wordt als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="5dcce-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="5dcce-129">Totale btw = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = EUR 35,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="5dcce-130">Totaal factuurbedrag = 200,00 + 35,00 = EUR 235,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="5dcce-131">**Ander voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="5dcce-131">**Variation**</span></span> 

<span data-ttu-id="5dcce-132">Als de factuur twee regels met vier artikelen op elke regel heeft, is het nettobedrag op elke regel 100,00 en wordt de btw als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="5dcce-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="5dcce-133">Btw-regel 1 = 50 x 30% + 50 x 20% = 15 + 10 = EUR 25,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="5dcce-134">Btw-regel 2 = 50 x 30% + 50 x 20% = 15 + 10 = EUR 25,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="5dcce-135">Totale btw = 25,00 + 25,00 = EUR 50,00</span><span class="sxs-lookup"><span data-stu-id="5dcce-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="5dcce-136">Totaal factuurbedrag = 200,00 + 50,00 = EUR 250,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="5dcce-137">Nettobedrag per eenheid</span><span class="sxs-lookup"><span data-stu-id="5dcce-137">Net amount per unit</span></span>
<span data-ttu-id="5dcce-138">Selecteer deze optie om het btw-tarief te berekenen op basis van de waarde van elke eenheid, exclusief eventuele overige belastingen.</span><span class="sxs-lookup"><span data-stu-id="5dcce-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="5dcce-139">Als een marginale basis op basis van een eenheid is geselecteerd, dan moet voor de btw-code ook een eenheid worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="5dcce-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="5dcce-140">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5dcce-140">Example</span></span>

<span data-ttu-id="5dcce-141">De btw-tarieven worden ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="5dcce-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="5dcce-142">Bedrag</span><span class="sxs-lookup"><span data-stu-id="5dcce-142">Amount</span></span>             | <span data-ttu-id="5dcce-143">Btw-tarief</span><span class="sxs-lookup"><span data-stu-id="5dcce-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="5dcce-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="5dcce-144">0 - 50</span></span>             | <span data-ttu-id="5dcce-145">30%</span><span class="sxs-lookup"><span data-stu-id="5dcce-145">30%</span></span>      |
| <span data-ttu-id="5dcce-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="5dcce-146">50 - 100</span></span>           | <span data-ttu-id="5dcce-147">20%</span><span class="sxs-lookup"><span data-stu-id="5dcce-147">20%</span></span>      |
| <span data-ttu-id="5dcce-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="5dcce-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="5dcce-149">10%</span><span class="sxs-lookup"><span data-stu-id="5dcce-149">10%</span></span>      |

<span data-ttu-id="5dcce-150">Marginale basis: **Nettobedrag per eenheid**</span><span class="sxs-lookup"><span data-stu-id="5dcce-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="5dcce-151">Berekeningsmethode: **Volledige bedrag**</span><span class="sxs-lookup"><span data-stu-id="5dcce-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="5dcce-152">U koopt 8 lampen die 25,00 per stuk kosten.</span><span class="sxs-lookup"><span data-stu-id="5dcce-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="5dcce-153">Het nettobedrag voor de factuurregel is EUR 200,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="5dcce-154">De btw wordt als volgt berekend: Btw per eenheid = 25,00 x 30% = 7,50 Totale btw = 7,50 x 8 eenheden = 60,00 Totaal factuurbedrag = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="5dcce-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="5dcce-155">Nettobedrag van factuursaldo</span><span class="sxs-lookup"><span data-stu-id="5dcce-155">Net amount of invoice balance</span></span>

<span data-ttu-id="5dcce-156">Selecteer deze optie om het btw-tarief te berekenen op basis van de totale waarde van de factuur, exclusief eventuele overige belastingen.</span><span class="sxs-lookup"><span data-stu-id="5dcce-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="5dcce-157">voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5dcce-157">Example</span></span>

<span data-ttu-id="5dcce-158">De btw-tarieven worden ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="5dcce-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="5dcce-159">Bedrag</span><span class="sxs-lookup"><span data-stu-id="5dcce-159">Amount</span></span>            | <span data-ttu-id="5dcce-160">Btw-tarief</span><span class="sxs-lookup"><span data-stu-id="5dcce-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="5dcce-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="5dcce-161">0 - 50</span></span>            | <span data-ttu-id="5dcce-162">30%</span><span class="sxs-lookup"><span data-stu-id="5dcce-162">30%</span></span>      |
| <span data-ttu-id="5dcce-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="5dcce-163">50 - 100</span></span>          | <span data-ttu-id="5dcce-164">20%</span><span class="sxs-lookup"><span data-stu-id="5dcce-164">20%</span></span>      |
| <span data-ttu-id="5dcce-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="5dcce-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="5dcce-166">10%</span><span class="sxs-lookup"><span data-stu-id="5dcce-166">10%</span></span>      |

<span data-ttu-id="5dcce-167">Marginale basis: **Nettobedrag van factuursaldo**</span><span class="sxs-lookup"><span data-stu-id="5dcce-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="5dcce-168">Berekeningsmethode: **Interval** een verkoopfactuur bevat 2 regels met 4 lampen op elke regel voor 25,00 per stuk.</span><span class="sxs-lookup"><span data-stu-id="5dcce-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="5dcce-169">Het nettobedrag van factuursaldo is 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="5dcce-170">De btw wordt als volgt berekend: Totale btw = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Totaal factuurbedrag = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="5dcce-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="5dcce-171">Brutobedrag per regel</span><span class="sxs-lookup"><span data-stu-id="5dcce-171">Gross amount per line</span></span>

<span data-ttu-id="5dcce-172">Selecteer deze optie om het btw-tarief te berekenen op basis van de waarde van de regel, inclusief alle overige belastingen voor die regel.</span><span class="sxs-lookup"><span data-stu-id="5dcce-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="5dcce-173">In een btw-groep kunt u maar één btw-code met deze selectie hebben in het veld Marginale basis.</span><span class="sxs-lookup"><span data-stu-id="5dcce-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="5dcce-174">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5dcce-174">Example</span></span>

<span data-ttu-id="5dcce-175">De btw-tarieven worden ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="5dcce-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="5dcce-176">Bedrag</span><span class="sxs-lookup"><span data-stu-id="5dcce-176">Amount</span></span>             | <span data-ttu-id="5dcce-177">Btw-tarief</span><span class="sxs-lookup"><span data-stu-id="5dcce-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="5dcce-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="5dcce-178">0 - 50</span></span>             | <span data-ttu-id="5dcce-179">30%</span><span class="sxs-lookup"><span data-stu-id="5dcce-179">30%</span></span>      |
| <span data-ttu-id="5dcce-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="5dcce-180">50 - 100</span></span>           | <span data-ttu-id="5dcce-181">20%</span><span class="sxs-lookup"><span data-stu-id="5dcce-181">20%</span></span>      |
| <span data-ttu-id="5dcce-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="5dcce-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="5dcce-183">10%</span><span class="sxs-lookup"><span data-stu-id="5dcce-183">10%</span></span>      |

<span data-ttu-id="5dcce-184">Marginale basis: **Brutobedrag per regel** Berekeningsmethode: **Interval** Daarnaast is er een andere btw-code voor berekening van een speciale heffing van 5,00 op elke lamp.</span><span class="sxs-lookup"><span data-stu-id="5dcce-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="5dcce-185">De heffing wordt toegevoegd aan het nettobedrag voordat de btw wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="5dcce-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="5dcce-186">U koopt 8 lampen die 25,00 per stuk kosten.</span><span class="sxs-lookup"><span data-stu-id="5dcce-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="5dcce-187">Het nettobedrag voor de factuurregel is EUR 200,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="5dcce-188">Het brutobedrag voor de factuurregel is 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="5dcce-189">De btw wordt als volgt berekend: Totale btw = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Totale heffing = 5,00 x 8 = 40,00 Totaal factuurbedrag = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="5dcce-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="5dcce-190">**Ander voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="5dcce-190">**Variation**</span></span> 

<span data-ttu-id="5dcce-191">Als de factuur wordt gemaakt met 2 factuurregels met 4 artikelen op elke regel, is het nettobedrag per factuurregel 100,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="5dcce-192">Het brutobedrag (inclusief de heffing van 4 x 5,00) per factuurregel zou 120,00 bedragen, en de btw wordt als volgt opgesteld: Btw factuurregel 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Btw factuurregel 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Totale btw = 27,00 + 27,00 = 54,00 Totale heffing = 5,00 x 8 = 40,00 Totaal factuurbedrag = 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="5dcce-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="5dcce-193">Brutobedrag per eenheid</span><span class="sxs-lookup"><span data-stu-id="5dcce-193">Gross amount per unit</span></span>

<span data-ttu-id="5dcce-194">Selecteer deze optie om het btw-tarief te berekenen op basis van de waarde van de eenheid, inclusief eventuele overige belastingen.</span><span class="sxs-lookup"><span data-stu-id="5dcce-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="5dcce-195">In een btw-groep kunt u maar één btw-code met deze selectie hebben in het veld Marginale basis.</span><span class="sxs-lookup"><span data-stu-id="5dcce-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="5dcce-196">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5dcce-196">Example</span></span>

<span data-ttu-id="5dcce-197">De btw-tarieven worden ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="5dcce-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="5dcce-198">Bedrag</span><span class="sxs-lookup"><span data-stu-id="5dcce-198">Amount</span></span>             | <span data-ttu-id="5dcce-199">Btw-tarief</span><span class="sxs-lookup"><span data-stu-id="5dcce-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="5dcce-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="5dcce-200">0 - 50</span></span>             | <span data-ttu-id="5dcce-201">30%</span><span class="sxs-lookup"><span data-stu-id="5dcce-201">30%</span></span>      |
| <span data-ttu-id="5dcce-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="5dcce-202">50 - 100</span></span>           | <span data-ttu-id="5dcce-203">20%</span><span class="sxs-lookup"><span data-stu-id="5dcce-203">20%</span></span>      |
| <span data-ttu-id="5dcce-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="5dcce-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="5dcce-205">10%</span><span class="sxs-lookup"><span data-stu-id="5dcce-205">10%</span></span>      |

<span data-ttu-id="5dcce-206">Marginale basis: **Brutobedrag per eenheid** Er is een speciale heffing van 5,00 op elke lamp.</span><span class="sxs-lookup"><span data-stu-id="5dcce-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="5dcce-207">De heffing wordt toegevoegd aan het nettobedrag voordat de btw wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="5dcce-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="5dcce-208">U koopt 8 lampen die 25,00 per stuk kosten.</span><span class="sxs-lookup"><span data-stu-id="5dcce-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="5dcce-209">Het brutobedrag per eenheid is EUR 30,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="5dcce-210">De btw wordt als volgt berekend: Btw per eenheid = 30 x 30% = 9,00 Totale btw = 9,00 x 8 = 72,00 Totale heffing = 5,00 x 8 = 40,00 Totaal factuurbedrag = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="5dcce-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="5dcce-211">Factuurtotaal incl. andere btw</span><span class="sxs-lookup"><span data-stu-id="5dcce-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="5dcce-212">Selecteer deze optie om het btw-tarief te berekenen op basis van de totale waarde van de factuur, inclusief eventuele overige belastingen.</span><span class="sxs-lookup"><span data-stu-id="5dcce-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="5dcce-213">In een btw-groep kunt u maar één btw-code met deze selectie hebben in het veld Marginale basis.</span><span class="sxs-lookup"><span data-stu-id="5dcce-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="5dcce-214">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5dcce-214">Example</span></span>

<span data-ttu-id="5dcce-215">De btw-tarieven worden ingesteld met de volgende intervallen:</span><span class="sxs-lookup"><span data-stu-id="5dcce-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="5dcce-216">Bedrag</span><span class="sxs-lookup"><span data-stu-id="5dcce-216">Amount</span></span>             | <span data-ttu-id="5dcce-217">Btw-tarief</span><span class="sxs-lookup"><span data-stu-id="5dcce-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="5dcce-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="5dcce-218">0 - 50</span></span>             | <span data-ttu-id="5dcce-219">30%</span><span class="sxs-lookup"><span data-stu-id="5dcce-219">30%</span></span>      |
| <span data-ttu-id="5dcce-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="5dcce-220">50 - 100</span></span>           | <span data-ttu-id="5dcce-221">20%</span><span class="sxs-lookup"><span data-stu-id="5dcce-221">20%</span></span>      |
| <span data-ttu-id="5dcce-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="5dcce-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="5dcce-223">10%</span><span class="sxs-lookup"><span data-stu-id="5dcce-223">10%</span></span>      |

<span data-ttu-id="5dcce-224">Marginale basis: **Factuurtotaal incl. andere btw-bedragen** berekeningsmethode: **Interval** </span><span class="sxs-lookup"><span data-stu-id="5dcce-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="5dcce-225">Op elke lamp is een speciale heffing van toepassing van EUR 5,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="5dcce-226">De heffing wordt toegevoegd aan het nettobedrag voordat de btw wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="5dcce-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="5dcce-227">U koopt 8 lampen die 25,00 per stuk kosten.</span><span class="sxs-lookup"><span data-stu-id="5dcce-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="5dcce-228">Het nettobedrag voor de factuur is EUR 200,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="5dcce-229">Het brutobedrag voor de factuur is 200,00 + (8 x 5,00) = EUR 240,00.</span><span class="sxs-lookup"><span data-stu-id="5dcce-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="5dcce-230">De btw wordt als volgt berekend: Totale btw = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Totale heffing = 5,00 x 8 = 40,00 Totaal factuurbedrag = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="5dcce-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="5dcce-231">Zie [De opties Volledig bedrag en Intervalberekening voor btw-codes](whole-amount-interval-options-sales-tax-codes.md) en [Btw-berekeningsmethoden in het veld Oorsprong](sales-tax-calculation-methods-origin-field.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5dcce-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>


