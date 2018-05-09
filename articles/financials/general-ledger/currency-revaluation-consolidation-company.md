---
title: Valutaherwaardering in een consolidatiebedrijf
description: In dit onderwerp wordt beschreven hoe valuta wordt geherwaardeerd in een consolidatiebedrijf.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2368021864668c2721976e820c74263137c1ee00
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="a875f-103">Valutaherwaardering in een consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="a875f-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a875f-104">Wanneer u gegevens van een valuta voor boekhouding naar een andere consolideert, moet u herwaardering alsnog uitvoeren als er een wijziging in wisselkoersen is, zodat de rekeningsaldo's correct worden geherwaardeerd.</span><span class="sxs-lookup"><span data-stu-id="a875f-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="a875f-105">Als u oorspronkelijk de gegevens consolideert, gebruik het **Valutaomzetting** tabblad om de oorspronkelijke wisselkoers te selecteren voor vertaling tijdens het consolidatieproces.</span><span class="sxs-lookup"><span data-stu-id="a875f-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="a875f-106">Nadat een nieuwe wisselkoers (bijvoorbeeld in de volgende maand) is ingevoerd, moet u de rekeningsaldo's herwaarderen.</span><span class="sxs-lookup"><span data-stu-id="a875f-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="a875f-107">De ongerealiseerde winst of verlies worden vervolgens overeenkomstig bijgewerkt, op basis van de nieuwe wisselkoers en datum.</span><span class="sxs-lookup"><span data-stu-id="a875f-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="a875f-108">Het volgende voorbeeld illustreert de journaalregels die tijdens het proces zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a875f-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="a875f-109">Bedrijfsinstellingen</span><span class="sxs-lookup"><span data-stu-id="a875f-109">Company setup</span></span>
-   <span data-ttu-id="a875f-110">**Bron/werken bedrijf (USMF)** - Amerikaanse dollars (USD) worden gebruikt als boekhouding- en aangiftevaluta.</span><span class="sxs-lookup"><span data-stu-id="a875f-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="a875f-111">**Geconsolideerd bedrijf (CON)** Euro's (EUR) worden gebruikt als de boekhouding- en aangiftevaluta.</span><span class="sxs-lookup"><span data-stu-id="a875f-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="a875f-112">**Gerealiseerde winst** – Grootboekrekening 801500</span><span class="sxs-lookup"><span data-stu-id="a875f-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="a875f-113">**Gerealiseerd verlies**– Grootboekrekening 801600</span><span class="sxs-lookup"><span data-stu-id="a875f-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="a875f-114">**Ongerealiseerde winst** - Grootboekrekening 801600</span><span class="sxs-lookup"><span data-stu-id="a875f-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="a875f-115">**Ongerealiseerd verlies** - Grootboekrekening 801400</span><span class="sxs-lookup"><span data-stu-id="a875f-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="a875f-116">Oorspronkelijke transacties</span><span class="sxs-lookup"><span data-stu-id="a875f-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="a875f-117">Kasontvangsttransacties in USMF</span><span class="sxs-lookup"><span data-stu-id="a875f-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="a875f-118">Datum</span><span class="sxs-lookup"><span data-stu-id="a875f-118">Date</span></span>       | <span data-ttu-id="a875f-119">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="a875f-119">Ledger account</span></span>               | <span data-ttu-id="a875f-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="a875f-120">Currency</span></span> | <span data-ttu-id="a875f-121">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a875f-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="a875f-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="a875f-122">10/11/2015</span></span> | <span data-ttu-id="a875f-123">110110 - Contant geld</span><span class="sxs-lookup"><span data-stu-id="a875f-123">110110 – Cash</span></span>                | <span data-ttu-id="a875f-124">USD</span><span class="sxs-lookup"><span data-stu-id="a875f-124">USD</span></span>      | <span data-ttu-id="a875f-125">500</span><span class="sxs-lookup"><span data-stu-id="a875f-125">500</span></span>    |
| <span data-ttu-id="a875f-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="a875f-126">10/11/2015</span></span> | <span data-ttu-id="a875f-127">130100 - Debiteuren</span><span class="sxs-lookup"><span data-stu-id="a875f-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="a875f-128">USD</span><span class="sxs-lookup"><span data-stu-id="a875f-128">USD</span></span>      | <span data-ttu-id="a875f-129">-500</span><span class="sxs-lookup"><span data-stu-id="a875f-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="a875f-130">Wisselkoersen</span><span class="sxs-lookup"><span data-stu-id="a875f-130">Exchange rates</span></span>

| <span data-ttu-id="a875f-131">Vanuit valuta</span><span class="sxs-lookup"><span data-stu-id="a875f-131">From currency</span></span> | <span data-ttu-id="a875f-132">Naar valuta</span><span class="sxs-lookup"><span data-stu-id="a875f-132">To currency</span></span> | <span data-ttu-id="a875f-133">Begindatum</span><span class="sxs-lookup"><span data-stu-id="a875f-133">Start date</span></span> | <span data-ttu-id="a875f-134">Wisselkoers</span><span class="sxs-lookup"><span data-stu-id="a875f-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="a875f-135">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-135">EUR</span></span>           | <span data-ttu-id="a875f-136">USD</span><span class="sxs-lookup"><span data-stu-id="a875f-136">USD</span></span>         | <span data-ttu-id="a875f-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="a875f-137">10/1/2015</span></span>  | <span data-ttu-id="a875f-138">200</span><span class="sxs-lookup"><span data-stu-id="a875f-138">200</span></span>           |
| <span data-ttu-id="a875f-139">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-139">EUR</span></span>           | <span data-ttu-id="a875f-140">USD</span><span class="sxs-lookup"><span data-stu-id="a875f-140">USD</span></span>         | <span data-ttu-id="a875f-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="a875f-141">11/1/2015</span></span>  | <span data-ttu-id="a875f-142">150</span><span class="sxs-lookup"><span data-stu-id="a875f-142">150</span></span>           |
| <span data-ttu-id="a875f-143">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-143">EUR</span></span>           | <span data-ttu-id="a875f-144">USD</span><span class="sxs-lookup"><span data-stu-id="a875f-144">USD</span></span>         | <span data-ttu-id="a875f-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="a875f-145">12/1/2012</span></span>  | <span data-ttu-id="a875f-146">100</span><span class="sxs-lookup"><span data-stu-id="a875f-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="a875f-147">Voer de consolidatie voor Oktober 2015 uit</span><span class="sxs-lookup"><span data-stu-id="a875f-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a875f-148">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="a875f-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="a875f-149">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="a875f-149">Ledger account</span></span> | <span data-ttu-id="a875f-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="a875f-150">Currency</span></span> | <span data-ttu-id="a875f-151">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a875f-151">Amount</span></span> | <span data-ttu-id="a875f-152">Berekening</span><span class="sxs-lookup"><span data-stu-id="a875f-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="a875f-153">110110</span><span class="sxs-lookup"><span data-stu-id="a875f-153">110110</span></span>         | <span data-ttu-id="a875f-154">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-154">EUR</span></span>      | <span data-ttu-id="a875f-155">250</span><span class="sxs-lookup"><span data-stu-id="a875f-155">250</span></span>    | <span data-ttu-id="a875f-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="a875f-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="a875f-157">130100</span><span class="sxs-lookup"><span data-stu-id="a875f-157">130100</span></span>         | <span data-ttu-id="a875f-158">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-158">EUR</span></span>      | <span data-ttu-id="a875f-159">-250</span><span class="sxs-lookup"><span data-stu-id="a875f-159">-250</span></span>   | <span data-ttu-id="a875f-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="a875f-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="a875f-161">Voer de valuta herwaardering voor de rekeningen van 1 oktober 2015, tot en met 30 november 2015</span><span class="sxs-lookup"><span data-stu-id="a875f-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a875f-162">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="a875f-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="a875f-163">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="a875f-163">Ledger account</span></span> | <span data-ttu-id="a875f-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="a875f-164">Currency</span></span> | <span data-ttu-id="a875f-165">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a875f-165">Amount</span></span>  | <span data-ttu-id="a875f-166">Berekening</span><span class="sxs-lookup"><span data-stu-id="a875f-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="a875f-167">110110</span><span class="sxs-lookup"><span data-stu-id="a875f-167">110110</span></span>         | <span data-ttu-id="a875f-168">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-168">EUR</span></span>      | <span data-ttu-id="a875f-169">333.33</span><span class="sxs-lookup"><span data-stu-id="a875f-169">333.33</span></span>  | <span data-ttu-id="a875f-170">Oorspronkelijk bedrag van 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="a875f-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="a875f-171">130100</span><span class="sxs-lookup"><span data-stu-id="a875f-171">130100</span></span>         | <span data-ttu-id="a875f-172">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-172">EUR</span></span>      | <span data-ttu-id="a875f-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="a875f-173">-333.33</span></span> | <span data-ttu-id="a875f-174">Oorspronkelijk bedrag van -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="a875f-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="a875f-175">801400</span><span class="sxs-lookup"><span data-stu-id="a875f-175">801400</span></span>         | <span data-ttu-id="a875f-176">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-176">EUR</span></span>      | <span data-ttu-id="a875f-177">83.33</span><span class="sxs-lookup"><span data-stu-id="a875f-177">83.33</span></span>   | <span data-ttu-id="a875f-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="a875f-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="a875f-179">801600</span><span class="sxs-lookup"><span data-stu-id="a875f-179">801600</span></span>         | <span data-ttu-id="a875f-180">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-180">EUR</span></span>      | <span data-ttu-id="a875f-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="a875f-181">-83.33</span></span>  | <span data-ttu-id="a875f-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="a875f-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="a875f-183">U kunt extra transacties voor de aangiftevalutabedragen zien.</span><span class="sxs-lookup"><span data-stu-id="a875f-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="a875f-184">Voer de valuta herwaardering voor de rekeningen van 1 oktober 2015 tot en met 31 december 2015</span><span class="sxs-lookup"><span data-stu-id="a875f-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a875f-185">Saldi in het consolidatiebedrijf</span><span class="sxs-lookup"><span data-stu-id="a875f-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="a875f-186">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="a875f-186">Ledger account</span></span> | <span data-ttu-id="a875f-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="a875f-187">Currency</span></span> | <span data-ttu-id="a875f-188">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a875f-188">Amount</span></span>  | <span data-ttu-id="a875f-189">Berekening</span><span class="sxs-lookup"><span data-stu-id="a875f-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="a875f-190">110110</span><span class="sxs-lookup"><span data-stu-id="a875f-190">110110</span></span>         | <span data-ttu-id="a875f-191">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-191">EUR</span></span>      | <span data-ttu-id="a875f-192">500,00</span><span class="sxs-lookup"><span data-stu-id="a875f-192">500.00</span></span>  | <span data-ttu-id="a875f-193">Oorspronkelijk bedrag van 500 × 1</span><span class="sxs-lookup"><span data-stu-id="a875f-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="a875f-194">130100</span><span class="sxs-lookup"><span data-stu-id="a875f-194">130100</span></span>         | <span data-ttu-id="a875f-195">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-195">EUR</span></span>      | <span data-ttu-id="a875f-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="a875f-196">-500.00</span></span> | <span data-ttu-id="a875f-197">Oorspronkelijk bedrag van -500 × 1</span><span class="sxs-lookup"><span data-stu-id="a875f-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="a875f-198">801400</span><span class="sxs-lookup"><span data-stu-id="a875f-198">801400</span></span>         | <span data-ttu-id="a875f-199">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-199">EUR</span></span>      | <span data-ttu-id="a875f-200">250</span><span class="sxs-lookup"><span data-stu-id="a875f-200">250</span></span>     | <span data-ttu-id="a875f-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="a875f-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="a875f-202">801600</span><span class="sxs-lookup"><span data-stu-id="a875f-202">801600</span></span>         | <span data-ttu-id="a875f-203">EUR</span><span class="sxs-lookup"><span data-stu-id="a875f-203">EUR</span></span>      | <span data-ttu-id="a875f-204">-250</span><span class="sxs-lookup"><span data-stu-id="a875f-204">-250</span></span>    | <span data-ttu-id="a875f-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="a875f-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






