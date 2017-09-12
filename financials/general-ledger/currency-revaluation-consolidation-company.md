---
title: Valutaherwaardering in een consolidatiebedrijf
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: nl-nl
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="e28af-102">Valutaherwaardering in een consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="e28af-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="e28af-103">Wanneer u gegevens van een valuta voor boekhouding naar een andere consolideert, moet u herwaardering alsnog uitvoeren als er een wijziging in wisselkoersen is, zodat de rekeningsaldo's correct worden geherwaardeerd.</span><span class="sxs-lookup"><span data-stu-id="e28af-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="e28af-104">Als u oorspronkelijk de gegevens consolideert, gebruik het **Valutaomzetting** tabblad om de oorspronkelijke wisselkoers te selecteren voor vertaling tijdens het consolidatieproces.</span><span class="sxs-lookup"><span data-stu-id="e28af-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="e28af-105">Nadat een nieuwe wisselkoers (bijvoorbeeld in de volgende maand) is ingevoerd, moet u de rekeningsaldo's herwaarderen.</span><span class="sxs-lookup"><span data-stu-id="e28af-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="e28af-106">De ongerealiseerde winst of verlies worden vervolgens overeenkomstig bijgewerkt, op basis van de nieuwe wisselkoers en datum.</span><span class="sxs-lookup"><span data-stu-id="e28af-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="e28af-107">Het volgende voorbeeld illustreert de journaalregels die tijdens het proces zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e28af-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="e28af-108">Bedrijfsinstellingen</span><span class="sxs-lookup"><span data-stu-id="e28af-108">Company setup</span></span>
-   <span data-ttu-id="e28af-109">**Bron/werken bedrijf (USMF)** - Amerikaanse dollars (USD) worden gebruikt als boekhouding- en aangiftevaluta.</span><span class="sxs-lookup"><span data-stu-id="e28af-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="e28af-110">**Geconsolideerd bedrijf (CON)** Euro's (EUR) worden gebruikt als de boekhouding- en aangiftevaluta.</span><span class="sxs-lookup"><span data-stu-id="e28af-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="e28af-111">Gerealiseerde winst – Grootboekrekening 801500</span><span class="sxs-lookup"><span data-stu-id="e28af-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="e28af-112">**Gerealiseerd verlies**– Grootboekrekening 801600</span><span class="sxs-lookup"><span data-stu-id="e28af-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="e28af-113">**Ongerealiseerde winst** - Grootboekrekening 801600</span><span class="sxs-lookup"><span data-stu-id="e28af-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="e28af-114">**Ongerealiseerd verlies** - Grootboekrekening 801400</span><span class="sxs-lookup"><span data-stu-id="e28af-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="e28af-115">Oorspronkelijke transacties</span><span class="sxs-lookup"><span data-stu-id="e28af-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="e28af-116">Kasontvangsttransacties in USMF</span><span class="sxs-lookup"><span data-stu-id="e28af-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="e28af-117">Datum</span><span class="sxs-lookup"><span data-stu-id="e28af-117">Date</span></span>       | <span data-ttu-id="e28af-118">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="e28af-118">Ledger account</span></span>               | <span data-ttu-id="e28af-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="e28af-119">Currency</span></span> | <span data-ttu-id="e28af-120">Bedrag</span><span class="sxs-lookup"><span data-stu-id="e28af-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="e28af-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="e28af-121">10/11/2015</span></span> | <span data-ttu-id="e28af-122">110110 - Contant geld</span><span class="sxs-lookup"><span data-stu-id="e28af-122">110110 – Cash</span></span>                | <span data-ttu-id="e28af-123">USD</span><span class="sxs-lookup"><span data-stu-id="e28af-123">USD</span></span>      | <span data-ttu-id="e28af-124">500</span><span class="sxs-lookup"><span data-stu-id="e28af-124">500</span></span>    |
| <span data-ttu-id="e28af-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="e28af-125">10/11/2015</span></span> | <span data-ttu-id="e28af-126">130100 - Debiteuren</span><span class="sxs-lookup"><span data-stu-id="e28af-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="e28af-127">USD</span><span class="sxs-lookup"><span data-stu-id="e28af-127">USD</span></span>      | <span data-ttu-id="e28af-128">-500</span><span class="sxs-lookup"><span data-stu-id="e28af-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="e28af-129">Wisselkoersen</span><span class="sxs-lookup"><span data-stu-id="e28af-129">Exchange rates</span></span>
| <span data-ttu-id="e28af-130">Vanuit valuta</span><span class="sxs-lookup"><span data-stu-id="e28af-130">From currency</span></span> | <span data-ttu-id="e28af-131">Naar valuta</span><span class="sxs-lookup"><span data-stu-id="e28af-131">To currency</span></span> | <span data-ttu-id="e28af-132">Begindatum</span><span class="sxs-lookup"><span data-stu-id="e28af-132">Start date</span></span> | <span data-ttu-id="e28af-133">Wisselkoers</span><span class="sxs-lookup"><span data-stu-id="e28af-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="e28af-134">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-134">EUR</span></span>           | <span data-ttu-id="e28af-135">USD</span><span class="sxs-lookup"><span data-stu-id="e28af-135">USD</span></span>         | <span data-ttu-id="e28af-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="e28af-136">10/1/2015</span></span>  | <span data-ttu-id="e28af-137">200</span><span class="sxs-lookup"><span data-stu-id="e28af-137">200</span></span>           |
| <span data-ttu-id="e28af-138">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-138">EUR</span></span>           | <span data-ttu-id="e28af-139">USD</span><span class="sxs-lookup"><span data-stu-id="e28af-139">USD</span></span>         | <span data-ttu-id="e28af-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="e28af-140">11/1/2015</span></span>  | <span data-ttu-id="e28af-141">150</span><span class="sxs-lookup"><span data-stu-id="e28af-141">150</span></span>           |
| <span data-ttu-id="e28af-142">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-142">EUR</span></span>           | <span data-ttu-id="e28af-143">USD</span><span class="sxs-lookup"><span data-stu-id="e28af-143">USD</span></span>         | <span data-ttu-id="e28af-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="e28af-144">12/1/2012</span></span>  | <span data-ttu-id="e28af-145">100</span><span class="sxs-lookup"><span data-stu-id="e28af-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="e28af-146">Voer de consolidatie voor Oktober 2015 uit</span><span class="sxs-lookup"><span data-stu-id="e28af-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e28af-147">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="e28af-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="e28af-148">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="e28af-148">Ledger account</span></span> | <span data-ttu-id="e28af-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="e28af-149">Currency</span></span> | <span data-ttu-id="e28af-150">Bedrag</span><span class="sxs-lookup"><span data-stu-id="e28af-150">Amount</span></span> | <span data-ttu-id="e28af-151">Berekening</span><span class="sxs-lookup"><span data-stu-id="e28af-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="e28af-152">110110</span><span class="sxs-lookup"><span data-stu-id="e28af-152">110110</span></span>         | <span data-ttu-id="e28af-153">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-153">EUR</span></span>      | <span data-ttu-id="e28af-154">250</span><span class="sxs-lookup"><span data-stu-id="e28af-154">250</span></span>    | <span data-ttu-id="e28af-155">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="e28af-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="e28af-156">130100</span><span class="sxs-lookup"><span data-stu-id="e28af-156">130100</span></span>         | <span data-ttu-id="e28af-157">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-157">EUR</span></span>      | <span data-ttu-id="e28af-158">-250</span><span class="sxs-lookup"><span data-stu-id="e28af-158">-250</span></span>   | <span data-ttu-id="e28af-159">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="e28af-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="e28af-160">Voer de valuta herwaardering voor de rekeningen van 1 oktober 2015, tot en met 30 november 2015</span><span class="sxs-lookup"><span data-stu-id="e28af-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e28af-161">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="e28af-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="e28af-162">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="e28af-162">Ledger account</span></span> | <span data-ttu-id="e28af-163">Valuta</span><span class="sxs-lookup"><span data-stu-id="e28af-163">Currency</span></span> | <span data-ttu-id="e28af-164">Bedrag</span><span class="sxs-lookup"><span data-stu-id="e28af-164">Amount</span></span>  | <span data-ttu-id="e28af-165">Berekening</span><span class="sxs-lookup"><span data-stu-id="e28af-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="e28af-166">110110</span><span class="sxs-lookup"><span data-stu-id="e28af-166">110110</span></span>         | <span data-ttu-id="e28af-167">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-167">EUR</span></span>      | <span data-ttu-id="e28af-168">333.33</span><span class="sxs-lookup"><span data-stu-id="e28af-168">333.33</span></span>  | <span data-ttu-id="e28af-169">Oorspronkelijk bedrag van 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="e28af-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="e28af-170">130100</span><span class="sxs-lookup"><span data-stu-id="e28af-170">130100</span></span>         | <span data-ttu-id="e28af-171">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-171">EUR</span></span>      | <span data-ttu-id="e28af-172">-333.33</span><span class="sxs-lookup"><span data-stu-id="e28af-172">-333.33</span></span> | <span data-ttu-id="e28af-173">Oorspronkelijk bedrag van -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="e28af-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="e28af-174">801400</span><span class="sxs-lookup"><span data-stu-id="e28af-174">801400</span></span>         | <span data-ttu-id="e28af-175">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-175">EUR</span></span>      | <span data-ttu-id="e28af-176">83.33</span><span class="sxs-lookup"><span data-stu-id="e28af-176">83.33</span></span>   | <span data-ttu-id="e28af-177">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="e28af-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="e28af-178">801600</span><span class="sxs-lookup"><span data-stu-id="e28af-178">801600</span></span>         | <span data-ttu-id="e28af-179">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-179">EUR</span></span>      | <span data-ttu-id="e28af-180">-83.33</span><span class="sxs-lookup"><span data-stu-id="e28af-180">-83.33</span></span>  | <span data-ttu-id="e28af-181">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="e28af-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="e28af-182">U kunt extra transacties voor de aangiftevalutabedragen zien.</span><span class="sxs-lookup"><span data-stu-id="e28af-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="e28af-183">Voer de valuta herwaardering voor de rekeningen van 1 oktober 2015 tot en met 31 december 2015</span><span class="sxs-lookup"><span data-stu-id="e28af-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e28af-184">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="e28af-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="e28af-185">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="e28af-185">Ledger account</span></span> | <span data-ttu-id="e28af-186">Valuta</span><span class="sxs-lookup"><span data-stu-id="e28af-186">Currency</span></span> | <span data-ttu-id="e28af-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="e28af-187">Amount</span></span>  | <span data-ttu-id="e28af-188">Berekening</span><span class="sxs-lookup"><span data-stu-id="e28af-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="e28af-189">110110</span><span class="sxs-lookup"><span data-stu-id="e28af-189">110110</span></span>         | <span data-ttu-id="e28af-190">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-190">EUR</span></span>      | <span data-ttu-id="e28af-191">500,00</span><span class="sxs-lookup"><span data-stu-id="e28af-191">500.00</span></span>  | <span data-ttu-id="e28af-192">Oorspronkelijk bedrag van 500 × 1</span><span class="sxs-lookup"><span data-stu-id="e28af-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="e28af-193">130100</span><span class="sxs-lookup"><span data-stu-id="e28af-193">130100</span></span>         | <span data-ttu-id="e28af-194">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-194">EUR</span></span>      | <span data-ttu-id="e28af-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="e28af-195">-500.00</span></span> | <span data-ttu-id="e28af-196">Oorspronkelijk bedrag van -500 × 1</span><span class="sxs-lookup"><span data-stu-id="e28af-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="e28af-197">801400</span><span class="sxs-lookup"><span data-stu-id="e28af-197">801400</span></span>         | <span data-ttu-id="e28af-198">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-198">EUR</span></span>      | <span data-ttu-id="e28af-199">250</span><span class="sxs-lookup"><span data-stu-id="e28af-199">250</span></span>     | <span data-ttu-id="e28af-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="e28af-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="e28af-201">801600</span><span class="sxs-lookup"><span data-stu-id="e28af-201">801600</span></span>         | <span data-ttu-id="e28af-202">EUR</span><span class="sxs-lookup"><span data-stu-id="e28af-202">EUR</span></span>      | <span data-ttu-id="e28af-203">-250</span><span class="sxs-lookup"><span data-stu-id="e28af-203">-250</span></span>    | <span data-ttu-id="e28af-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="e28af-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






