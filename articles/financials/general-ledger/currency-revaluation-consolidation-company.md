---
title: Valutaherwaardering in een consolidatiebedrijf
description: In dit onderwerp wordt beschreven hoe valuta wordt geherwaardeerd in een consolidatiebedrijf.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 27059b0d2a781453a7594bdc430005df6ea5c167
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="15618-103">Valutaherwaardering in een consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="15618-103">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="15618-104">Wanneer u gegevens van een valuta voor boekhouding naar een andere consolideert, moet u herwaardering alsnog uitvoeren als er een wijziging in wisselkoersen is, zodat de rekeningsaldo's correct worden geherwaardeerd.</span><span class="sxs-lookup"><span data-stu-id="15618-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="15618-105">Als u oorspronkelijk de gegevens consolideert, gebruik het **Valutaomzetting** tabblad om de oorspronkelijke wisselkoers te selecteren voor vertaling tijdens het consolidatieproces.</span><span class="sxs-lookup"><span data-stu-id="15618-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="15618-106">Nadat een nieuwe wisselkoers (bijvoorbeeld in de volgende maand) is ingevoerd, moet u de rekeningsaldo's herwaarderen.</span><span class="sxs-lookup"><span data-stu-id="15618-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="15618-107">De ongerealiseerde winst of verlies worden vervolgens overeenkomstig bijgewerkt, op basis van de nieuwe wisselkoers en datum.</span><span class="sxs-lookup"><span data-stu-id="15618-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="15618-108">Het volgende voorbeeld illustreert de journaalregels die tijdens het proces zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="15618-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="15618-109">Bedrijfsinstellingen</span><span class="sxs-lookup"><span data-stu-id="15618-109">Company setup</span></span>
-   <span data-ttu-id="15618-110">**Bron/werken bedrijf (USMF)** - Amerikaanse dollars (USD) worden gebruikt als boekhouding- en aangiftevaluta.</span><span class="sxs-lookup"><span data-stu-id="15618-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="15618-111">**Geconsolideerd bedrijf (CON)** Euro's (EUR) worden gebruikt als de boekhouding- en aangiftevaluta.</span><span class="sxs-lookup"><span data-stu-id="15618-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="15618-112">**Gerealiseerde winst** – Grootboekrekening 801500</span><span class="sxs-lookup"><span data-stu-id="15618-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="15618-113">**Gerealiseerd verlies**– Grootboekrekening 801600</span><span class="sxs-lookup"><span data-stu-id="15618-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="15618-114">**Ongerealiseerde winst** - Grootboekrekening 801600</span><span class="sxs-lookup"><span data-stu-id="15618-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="15618-115">**Ongerealiseerd verlies** - Grootboekrekening 801400</span><span class="sxs-lookup"><span data-stu-id="15618-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="15618-116">Oorspronkelijke transacties</span><span class="sxs-lookup"><span data-stu-id="15618-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="15618-117">Kasontvangsttransacties in USMF</span><span class="sxs-lookup"><span data-stu-id="15618-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="15618-118">Datum</span><span class="sxs-lookup"><span data-stu-id="15618-118">Date</span></span>       | <span data-ttu-id="15618-119">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="15618-119">Ledger account</span></span>               | <span data-ttu-id="15618-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="15618-120">Currency</span></span> | <span data-ttu-id="15618-121">Bedrag</span><span class="sxs-lookup"><span data-stu-id="15618-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="15618-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="15618-122">10/11/2015</span></span> | <span data-ttu-id="15618-123">110110 - Contant geld</span><span class="sxs-lookup"><span data-stu-id="15618-123">110110 – Cash</span></span>                | <span data-ttu-id="15618-124">USD</span><span class="sxs-lookup"><span data-stu-id="15618-124">USD</span></span>      | <span data-ttu-id="15618-125">500</span><span class="sxs-lookup"><span data-stu-id="15618-125">500</span></span>    |
| <span data-ttu-id="15618-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="15618-126">10/11/2015</span></span> | <span data-ttu-id="15618-127">130100 - Debiteuren</span><span class="sxs-lookup"><span data-stu-id="15618-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="15618-128">USD</span><span class="sxs-lookup"><span data-stu-id="15618-128">USD</span></span>      | <span data-ttu-id="15618-129">-500</span><span class="sxs-lookup"><span data-stu-id="15618-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="15618-130">Wisselkoersen</span><span class="sxs-lookup"><span data-stu-id="15618-130">Exchange rates</span></span>
| <span data-ttu-id="15618-131">Vanuit valuta</span><span class="sxs-lookup"><span data-stu-id="15618-131">From currency</span></span> | <span data-ttu-id="15618-132">Naar valuta</span><span class="sxs-lookup"><span data-stu-id="15618-132">To currency</span></span> | <span data-ttu-id="15618-133">Begindatum</span><span class="sxs-lookup"><span data-stu-id="15618-133">Start date</span></span> | <span data-ttu-id="15618-134">Wisselkoers</span><span class="sxs-lookup"><span data-stu-id="15618-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="15618-135">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-135">EUR</span></span>           | <span data-ttu-id="15618-136">USD</span><span class="sxs-lookup"><span data-stu-id="15618-136">USD</span></span>         | <span data-ttu-id="15618-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="15618-137">10/1/2015</span></span>  | <span data-ttu-id="15618-138">200</span><span class="sxs-lookup"><span data-stu-id="15618-138">200</span></span>           |
| <span data-ttu-id="15618-139">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-139">EUR</span></span>           | <span data-ttu-id="15618-140">USD</span><span class="sxs-lookup"><span data-stu-id="15618-140">USD</span></span>         | <span data-ttu-id="15618-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="15618-141">11/1/2015</span></span>  | <span data-ttu-id="15618-142">150</span><span class="sxs-lookup"><span data-stu-id="15618-142">150</span></span>           |
| <span data-ttu-id="15618-143">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-143">EUR</span></span>           | <span data-ttu-id="15618-144">USD</span><span class="sxs-lookup"><span data-stu-id="15618-144">USD</span></span>         | <span data-ttu-id="15618-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="15618-145">12/1/2012</span></span>  | <span data-ttu-id="15618-146">100</span><span class="sxs-lookup"><span data-stu-id="15618-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="15618-147">Voer de consolidatie voor Oktober 2015 uit</span><span class="sxs-lookup"><span data-stu-id="15618-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="15618-148">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="15618-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="15618-149">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="15618-149">Ledger account</span></span> | <span data-ttu-id="15618-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="15618-150">Currency</span></span> | <span data-ttu-id="15618-151">Bedrag</span><span class="sxs-lookup"><span data-stu-id="15618-151">Amount</span></span> | <span data-ttu-id="15618-152">Berekening</span><span class="sxs-lookup"><span data-stu-id="15618-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="15618-153">110110</span><span class="sxs-lookup"><span data-stu-id="15618-153">110110</span></span>         | <span data-ttu-id="15618-154">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-154">EUR</span></span>      | <span data-ttu-id="15618-155">250</span><span class="sxs-lookup"><span data-stu-id="15618-155">250</span></span>    | <span data-ttu-id="15618-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="15618-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="15618-157">130100</span><span class="sxs-lookup"><span data-stu-id="15618-157">130100</span></span>         | <span data-ttu-id="15618-158">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-158">EUR</span></span>      | <span data-ttu-id="15618-159">-250</span><span class="sxs-lookup"><span data-stu-id="15618-159">-250</span></span>   | <span data-ttu-id="15618-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="15618-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="15618-161">Voer de valuta herwaardering voor de rekeningen van 1 oktober 2015, tot en met 30 november 2015</span><span class="sxs-lookup"><span data-stu-id="15618-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="15618-162">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="15618-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="15618-163">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="15618-163">Ledger account</span></span> | <span data-ttu-id="15618-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="15618-164">Currency</span></span> | <span data-ttu-id="15618-165">Bedrag</span><span class="sxs-lookup"><span data-stu-id="15618-165">Amount</span></span>  | <span data-ttu-id="15618-166">Berekening</span><span class="sxs-lookup"><span data-stu-id="15618-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="15618-167">110110</span><span class="sxs-lookup"><span data-stu-id="15618-167">110110</span></span>         | <span data-ttu-id="15618-168">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-168">EUR</span></span>      | <span data-ttu-id="15618-169">333.33</span><span class="sxs-lookup"><span data-stu-id="15618-169">333.33</span></span>  | <span data-ttu-id="15618-170">Oorspronkelijk bedrag van 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="15618-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="15618-171">130100</span><span class="sxs-lookup"><span data-stu-id="15618-171">130100</span></span>         | <span data-ttu-id="15618-172">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-172">EUR</span></span>      | <span data-ttu-id="15618-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="15618-173">-333.33</span></span> | <span data-ttu-id="15618-174">Oorspronkelijk bedrag van -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="15618-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="15618-175">801400</span><span class="sxs-lookup"><span data-stu-id="15618-175">801400</span></span>         | <span data-ttu-id="15618-176">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-176">EUR</span></span>      | <span data-ttu-id="15618-177">83.33</span><span class="sxs-lookup"><span data-stu-id="15618-177">83.33</span></span>   | <span data-ttu-id="15618-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="15618-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="15618-179">801600</span><span class="sxs-lookup"><span data-stu-id="15618-179">801600</span></span>         | <span data-ttu-id="15618-180">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-180">EUR</span></span>      | <span data-ttu-id="15618-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="15618-181">-83.33</span></span>  | <span data-ttu-id="15618-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="15618-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="15618-183">U kunt extra transacties voor de aangiftevalutabedragen zien.</span><span class="sxs-lookup"><span data-stu-id="15618-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="15618-184">Voer de valuta herwaardering voor de rekeningen van 1 oktober 2015 tot en met 31 december 2015</span><span class="sxs-lookup"><span data-stu-id="15618-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="15618-185">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="15618-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="15618-186">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="15618-186">Ledger account</span></span> | <span data-ttu-id="15618-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="15618-187">Currency</span></span> | <span data-ttu-id="15618-188">Bedrag</span><span class="sxs-lookup"><span data-stu-id="15618-188">Amount</span></span>  | <span data-ttu-id="15618-189">Berekening</span><span class="sxs-lookup"><span data-stu-id="15618-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="15618-190">110110</span><span class="sxs-lookup"><span data-stu-id="15618-190">110110</span></span>         | <span data-ttu-id="15618-191">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-191">EUR</span></span>      | <span data-ttu-id="15618-192">500,00</span><span class="sxs-lookup"><span data-stu-id="15618-192">500.00</span></span>  | <span data-ttu-id="15618-193">Oorspronkelijk bedrag van 500 × 1</span><span class="sxs-lookup"><span data-stu-id="15618-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="15618-194">130100</span><span class="sxs-lookup"><span data-stu-id="15618-194">130100</span></span>         | <span data-ttu-id="15618-195">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-195">EUR</span></span>      | <span data-ttu-id="15618-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="15618-196">-500.00</span></span> | <span data-ttu-id="15618-197">Oorspronkelijk bedrag van -500 × 1</span><span class="sxs-lookup"><span data-stu-id="15618-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="15618-198">801400</span><span class="sxs-lookup"><span data-stu-id="15618-198">801400</span></span>         | <span data-ttu-id="15618-199">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-199">EUR</span></span>      | <span data-ttu-id="15618-200">250</span><span class="sxs-lookup"><span data-stu-id="15618-200">250</span></span>     | <span data-ttu-id="15618-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="15618-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="15618-202">801600</span><span class="sxs-lookup"><span data-stu-id="15618-202">801600</span></span>         | <span data-ttu-id="15618-203">EUR</span><span class="sxs-lookup"><span data-stu-id="15618-203">EUR</span></span>      | <span data-ttu-id="15618-204">-250</span><span class="sxs-lookup"><span data-stu-id="15618-204">-250</span></span>    | <span data-ttu-id="15618-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="15618-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






