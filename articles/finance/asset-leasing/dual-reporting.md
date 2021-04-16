---
title: Dubbele rapportage
description: In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c9f2bae330e688e1e941277d46ddcbd38916f8c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815975"
---
# <a name="dual-reporting"></a><span data-ttu-id="a9351-103">Dubbele rapportage</span><span class="sxs-lookup"><span data-stu-id="a9351-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9351-104">In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="a9351-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="a9351-105">Vertrouwdheid met boekingslagen in Microsoft Dynamics 365 Finance is vereist en maakt het voorbeeld gemakkelijker te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="a9351-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="a9351-106">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a9351-106">Example</span></span>

<span data-ttu-id="a9351-107">In het volgende voorbeeld wordt een lease verantwoord onder de Italiaanse wettelijke rapportering door middel van de cash-basis-methode en de IFRS-rapportagemethoden.</span><span class="sxs-lookup"><span data-stu-id="a9351-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="a9351-108">Het bedrijf moet drie boeken maken om te verantwoorden voor zowel de Italiaanse wettelijke vereisten als de IFRS 16-vereisten.</span><span class="sxs-lookup"><span data-stu-id="a9351-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="a9351-109">Eén boek is vereist voor IFRS 16, één boek is vereist voor wettelijke vereisten en één boek is vereist om de wettelijke boekingen automatisch terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="a9351-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="a9351-110">De boeken worden ingesteld, zoals in de volgende tabellen wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a9351-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="a9351-111">**IFRS 16-boek**</span><span class="sxs-lookup"><span data-stu-id="a9351-111">**IFRS 16 book**</span></span>

<span data-ttu-id="a9351-112">Het IFRS 16 boek is zo ingesteld dat het voldoet aan de IFRS 16-boekhoudnorm.</span><span class="sxs-lookup"><span data-stu-id="a9351-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="a9351-113">Alle posten die in dit boek worden geboekt, worden naar een aangepaste laag geboekt.</span><span class="sxs-lookup"><span data-stu-id="a9351-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="a9351-114">Naam</span><span class="sxs-lookup"><span data-stu-id="a9351-114">Name</span></span>                                    | <span data-ttu-id="a9351-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="a9351-116">Boektype</span><span class="sxs-lookup"><span data-stu-id="a9351-116">Book type</span></span>                               | <span data-ttu-id="a9351-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="a9351-117">IFRS 16</span></span>        |
| <span data-ttu-id="a9351-118">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-118">Book description</span></span>                        | <span data-ttu-id="a9351-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="a9351-119">IFRS 16</span></span>        |
| <span data-ttu-id="a9351-120">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="a9351-120">Posting Layer</span></span>                           | <span data-ttu-id="a9351-121">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="a9351-121">Custom layer 1</span></span> |
| <span data-ttu-id="a9351-122">Leasetype</span><span class="sxs-lookup"><span data-stu-id="a9351-122">Lease Type</span></span>                              | <span data-ttu-id="a9351-123">Finance</span><span class="sxs-lookup"><span data-stu-id="a9351-123">Finance</span></span>        |
| <span data-ttu-id="a9351-124">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="a9351-124">Accounting Framework</span></span>                    | <span data-ttu-id="a9351-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="a9351-125">IFRS 16</span></span>        |
| <span data-ttu-id="a9351-126">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="a9351-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a9351-127">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-127">0.00</span></span>           |
| <span data-ttu-id="a9351-128">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="a9351-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a9351-129">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-129">0.00</span></span>           |
| <span data-ttu-id="a9351-130">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="a9351-130">Short-term threshold</span></span>                    | <span data-ttu-id="a9351-131">12</span><span class="sxs-lookup"><span data-stu-id="a9351-131">12</span></span>             |
| <span data-ttu-id="a9351-132">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="a9351-132">Low Value Threshold</span></span>                     | <span data-ttu-id="a9351-133">5.000,00</span><span class="sxs-lookup"><span data-stu-id="a9351-133">5,000.00</span></span>       |
| <span data-ttu-id="a9351-134">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="a9351-134">Pay to Vendor</span></span>                           | <span data-ttu-id="a9351-135">No</span><span class="sxs-lookup"><span data-stu-id="a9351-135">No</span></span>             |

<span data-ttu-id="a9351-136">**Wettelijk boek**</span><span class="sxs-lookup"><span data-stu-id="a9351-136">**Statutory book**</span></span>

<span data-ttu-id="a9351-137">Het wettelijke boek is een cash-basis-boek waar het bedrijf de leasekosten zal verantwoorden als het bedrag aan geld dat maandelijks wordt betaald voor huur.</span><span class="sxs-lookup"><span data-stu-id="a9351-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="a9351-138">Dit boek produceert geen RoU-activum of leaseverplichtingen.</span><span class="sxs-lookup"><span data-stu-id="a9351-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="a9351-139">Naam</span><span class="sxs-lookup"><span data-stu-id="a9351-139">Name</span></span>                                    | <span data-ttu-id="a9351-140">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="a9351-141">Boektype</span><span class="sxs-lookup"><span data-stu-id="a9351-141">Book type</span></span>                               | <span data-ttu-id="a9351-142">Wettelijk</span><span class="sxs-lookup"><span data-stu-id="a9351-142">Statutory</span></span>   |
| <span data-ttu-id="a9351-143">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-143">Book description</span></span>                        | <span data-ttu-id="a9351-144">Lokale GAAP</span><span class="sxs-lookup"><span data-stu-id="a9351-144">Local GAAP</span></span>  |
| <span data-ttu-id="a9351-145">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="a9351-145">Posting Layer</span></span>                           | <span data-ttu-id="a9351-146">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-146">Current</span></span>     |
| <span data-ttu-id="a9351-147">Leasetype</span><span class="sxs-lookup"><span data-stu-id="a9351-147">Lease Type</span></span>                              | <span data-ttu-id="a9351-148">Automatisch</span><span class="sxs-lookup"><span data-stu-id="a9351-148">Automatic</span></span>   |
| <span data-ttu-id="a9351-149">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="a9351-149">Accounting Framework</span></span>                    | <span data-ttu-id="a9351-150">Contante basis</span><span class="sxs-lookup"><span data-stu-id="a9351-150">Cash basis</span></span>  |
| <span data-ttu-id="a9351-151">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="a9351-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a9351-152">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-152">0.00</span></span>        |
| <span data-ttu-id="a9351-153">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="a9351-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a9351-154">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-154">0.00</span></span>        |
| <span data-ttu-id="a9351-155">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="a9351-155">Short-term threshold</span></span>                    | <span data-ttu-id="a9351-156">0</span><span class="sxs-lookup"><span data-stu-id="a9351-156">0</span></span>           |
| <span data-ttu-id="a9351-157">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="a9351-157">Low Value Threshold</span></span>                     | <span data-ttu-id="a9351-158">0</span><span class="sxs-lookup"><span data-stu-id="a9351-158">0</span></span>           |
| <span data-ttu-id="a9351-159">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="a9351-159">Pay to Vendor</span></span>                           | <span data-ttu-id="a9351-160">No</span><span class="sxs-lookup"><span data-stu-id="a9351-160">No</span></span>          |

<span data-ttu-id="a9351-161">**Wettelijk terugboekingsboek**</span><span class="sxs-lookup"><span data-stu-id="a9351-161">**Statutory reversal book**</span></span>

<span data-ttu-id="a9351-162">Het wettelijke terugboekingsboek wordt op dezelfde manier ingesteld als het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="a9351-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="a9351-163">Naam</span><span class="sxs-lookup"><span data-stu-id="a9351-163">Name</span></span>                                    | <span data-ttu-id="a9351-164">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="a9351-165">Boektype</span><span class="sxs-lookup"><span data-stu-id="a9351-165">Book type</span></span>                               | <span data-ttu-id="a9351-166">Wettelijk - terugboeking</span><span class="sxs-lookup"><span data-stu-id="a9351-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="a9351-167">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-167">Book description</span></span>                        | <span data-ttu-id="a9351-168">Boek om wettelijk boek terug te boeken</span><span class="sxs-lookup"><span data-stu-id="a9351-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="a9351-169">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="a9351-169">Posting Layer</span></span>                           | <span data-ttu-id="a9351-170">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="a9351-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="a9351-171">Leasetype</span><span class="sxs-lookup"><span data-stu-id="a9351-171">Lease Type</span></span>                              | <span data-ttu-id="a9351-172">Automatisch</span><span class="sxs-lookup"><span data-stu-id="a9351-172">Automatic</span></span>                      |
| <span data-ttu-id="a9351-173">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="a9351-173">Accounting Framework</span></span>                    | <span data-ttu-id="a9351-174">Contante basis</span><span class="sxs-lookup"><span data-stu-id="a9351-174">Cash basis</span></span>                     |
| <span data-ttu-id="a9351-175">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="a9351-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="a9351-176">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-176">0.00</span></span>                           |
| <span data-ttu-id="a9351-177">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="a9351-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="a9351-178">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-178">0.00</span></span>                           |
| <span data-ttu-id="a9351-179">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="a9351-179">Short-term threshold</span></span>                    | <span data-ttu-id="a9351-180">0</span><span class="sxs-lookup"><span data-stu-id="a9351-180">0</span></span>                              |
| <span data-ttu-id="a9351-181">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="a9351-181">Low Value Threshold</span></span>                     | <span data-ttu-id="a9351-182">0</span><span class="sxs-lookup"><span data-stu-id="a9351-182">0</span></span>                              |
| <span data-ttu-id="a9351-183">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="a9351-183">Pay to Vendor</span></span>                           | <span data-ttu-id="a9351-184">No</span><span class="sxs-lookup"><span data-stu-id="a9351-184">No</span></span>                             |

<span data-ttu-id="a9351-185">Voor dit voorbeeld is er een lease gemaakt met de volgende instellingen op de tabbladen **Algemeen** en **Betalingsschemaregels**.</span><span class="sxs-lookup"><span data-stu-id="a9351-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="a9351-186">**Tabblad Algemeen**</span><span class="sxs-lookup"><span data-stu-id="a9351-186">**General tab**</span></span>

| <span data-ttu-id="a9351-187">Veld</span><span class="sxs-lookup"><span data-stu-id="a9351-187">Field</span></span>                      | <span data-ttu-id="a9351-188">Waarde</span><span class="sxs-lookup"><span data-stu-id="a9351-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="a9351-189">Verhoogd leningtarief</span><span class="sxs-lookup"><span data-stu-id="a9351-189">Incremental borrowing rate</span></span> | <span data-ttu-id="a9351-190">5%</span><span class="sxs-lookup"><span data-stu-id="a9351-190">5%</span></span>               |
| <span data-ttu-id="a9351-191">Begindatum</span><span class="sxs-lookup"><span data-stu-id="a9351-191">Commencement date</span></span>          | <span data-ttu-id="a9351-192">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="a9351-192">1/1/2020</span></span>         |
| <span data-ttu-id="a9351-193">Leasegroep</span><span class="sxs-lookup"><span data-stu-id="a9351-193">Lease group</span></span>                | <span data-ttu-id="a9351-194">Gebouwen</span><span class="sxs-lookup"><span data-stu-id="a9351-194">Buildings</span></span>        |
| <span data-ttu-id="a9351-195">Leverancier</span><span class="sxs-lookup"><span data-stu-id="a9351-195">Vendor</span></span>                     | <span data-ttu-id="a9351-196">1001</span><span class="sxs-lookup"><span data-stu-id="a9351-196">1001</span></span>             |
| <span data-ttu-id="a9351-197">Reële waarde van het activum</span><span class="sxs-lookup"><span data-stu-id="a9351-197">Fair value of the asset</span></span>    | <span data-ttu-id="a9351-198">245,000</span><span class="sxs-lookup"><span data-stu-id="a9351-198">245,000</span></span>          |
| <span data-ttu-id="a9351-199">Economische levensduur activum</span><span class="sxs-lookup"><span data-stu-id="a9351-199">Asset useful life</span></span>          | <span data-ttu-id="a9351-200">120</span><span class="sxs-lookup"><span data-stu-id="a9351-200">120</span></span>              |
| <span data-ttu-id="a9351-201">Type annuïteit</span><span class="sxs-lookup"><span data-stu-id="a9351-201">Annuity type</span></span>               | <span data-ttu-id="a9351-202">Normale annuïteit</span><span class="sxs-lookup"><span data-stu-id="a9351-202">Ordinary annuity</span></span> |
| <span data-ttu-id="a9351-203">Samenstellingsinterval</span><span class="sxs-lookup"><span data-stu-id="a9351-203">Compounding interval</span></span>       | <span data-ttu-id="a9351-204">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="a9351-204">Monthly</span></span>          |

<span data-ttu-id="a9351-205">**Tabblad Regels van betalingsschema**</span><span class="sxs-lookup"><span data-stu-id="a9351-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="a9351-206">Veld</span><span class="sxs-lookup"><span data-stu-id="a9351-206">Field</span></span>             | <span data-ttu-id="a9351-207">Waarde</span><span class="sxs-lookup"><span data-stu-id="a9351-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="a9351-208">Begindatum</span><span class="sxs-lookup"><span data-stu-id="a9351-208">Start date</span></span>        | <span data-ttu-id="a9351-209">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="a9351-209">1/1/2020</span></span>   |
| <span data-ttu-id="a9351-210">Periode-interval</span><span class="sxs-lookup"><span data-stu-id="a9351-210">Period interval</span></span>   | <span data-ttu-id="a9351-211">Maanden</span><span class="sxs-lookup"><span data-stu-id="a9351-211">Months</span></span>     |
| <span data-ttu-id="a9351-212">Perioden</span><span class="sxs-lookup"><span data-stu-id="a9351-212">Periods</span></span>           | <span data-ttu-id="a9351-213">24</span><span class="sxs-lookup"><span data-stu-id="a9351-213">24</span></span>         |
| <span data-ttu-id="a9351-214">Einddatum</span><span class="sxs-lookup"><span data-stu-id="a9351-214">End date</span></span>          | <span data-ttu-id="a9351-215">31-12-2020</span><span class="sxs-lookup"><span data-stu-id="a9351-215">12/31/2020</span></span> |
| <span data-ttu-id="a9351-216">Betalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="a9351-216">Payment frequency</span></span> | <span data-ttu-id="a9351-217">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="a9351-217">Monthly</span></span>    |
| <span data-ttu-id="a9351-218">Betalingsbedrag</span><span class="sxs-lookup"><span data-stu-id="a9351-218">Payment amount</span></span>    | <span data-ttu-id="a9351-219">1.000</span><span class="sxs-lookup"><span data-stu-id="a9351-219">1,000</span></span>      |

<span data-ttu-id="a9351-220">Als u deze lease onder twee raamwerken wilt verantwoorden, gebruikt u een huidige boekingslaag en een aangepaste boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="a9351-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="a9351-221">In de volgende tabel ziet u een voorbeeld van elke journaalpost die voor elke rapportagestandaard de financiële waarde reëel moet representeren.</span><span class="sxs-lookup"><span data-stu-id="a9351-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="a9351-222">Hierna wordt een gedetailleerde omschrijving gegeven van elke journaalpost voor de eerste maand van de lease.</span><span class="sxs-lookup"><span data-stu-id="a9351-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="a9351-223">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="a9351-224">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="a9351-225">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="a9351-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a9351-226">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="a9351-226">Current layer total</span></span></th>
<th><span data-ttu-id="a9351-227">Terugboekingsboek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="a9351-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="a9351-228">IFRS 16-boek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="a9351-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a9351-229">Huidige laag + aangepaste laagtotaal</span><span class="sxs-lookup"><span data-stu-id="a9351-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a9351-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="a9351-230">JE-100</span></span></th>
<th><span data-ttu-id="a9351-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="a9351-231">JE-110</span></span></th>
<th><span data-ttu-id="a9351-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="a9351-232">JE-120</span></span></th>
<th><span data-ttu-id="a9351-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="a9351-233">JE-130</span></span></th>
<th><span data-ttu-id="a9351-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="a9351-234">JE-140</span></span></th>
<th><span data-ttu-id="a9351-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="a9351-235">JE-150</span></span></th>
<th><span data-ttu-id="a9351-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="a9351-236">JE-160</span></span></th>
<th><span data-ttu-id="a9351-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="a9351-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a9351-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a9351-246">1</span><span class="sxs-lookup"><span data-stu-id="a9351-246">1</span></span></td>
<td><span data-ttu-id="a9351-247">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="a9351-247">Lease expense</span></span></td>
<td><span data-ttu-id="a9351-248">1.000,00</span><span class="sxs-lookup"><span data-stu-id="a9351-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-249">1,000.00</span></span></td>
<td><span data-ttu-id="a9351-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="a9351-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-251">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-252">2</span><span class="sxs-lookup"><span data-stu-id="a9351-252">2</span></span></td>
<td><span data-ttu-id="a9351-253">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="a9351-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-254">3,00</span><span class="sxs-lookup"><span data-stu-id="a9351-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-255">3.00</span><span class="sxs-lookup"><span data-stu-id="a9351-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-256">3.00</span><span class="sxs-lookup"><span data-stu-id="a9351-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-257">3</span><span class="sxs-lookup"><span data-stu-id="a9351-257">3</span></span></td>
<td><span data-ttu-id="a9351-258">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="a9351-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-259">5.00</span><span class="sxs-lookup"><span data-stu-id="a9351-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-260">5.00</span><span class="sxs-lookup"><span data-stu-id="a9351-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-261">5.00</span><span class="sxs-lookup"><span data-stu-id="a9351-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-262">4</span><span class="sxs-lookup"><span data-stu-id="a9351-262">4</span></span></td>
<td><span data-ttu-id="a9351-263">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="a9351-263">Clearing account</span></span></td>
<td><span data-ttu-id="a9351-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="a9351-264">-1,000.00</span></span></td>
<td><span data-ttu-id="a9351-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-266">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-266">0.00</span></span></td>
<td><span data-ttu-id="a9351-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="a9351-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-269">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-270">5</span><span class="sxs-lookup"><span data-stu-id="a9351-270">5</span></span></td>
<td><span data-ttu-id="a9351-271">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="a9351-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="a9351-272">-1,008.00</span></span></td>
<td><span data-ttu-id="a9351-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a9351-273">1,008.00</span></span></td>
<td><span data-ttu-id="a9351-274">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-275">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-276">6</span><span class="sxs-lookup"><span data-stu-id="a9351-276">6</span></span></td>
<td><span data-ttu-id="a9351-277">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="a9351-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-278">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="a9351-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a9351-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-281">7</span><span class="sxs-lookup"><span data-stu-id="a9351-281">7</span></span></td>
<td><span data-ttu-id="a9351-282">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="a9351-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-283">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="a9351-284">-22,794.00</span></span></td>
<td><span data-ttu-id="a9351-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-285">1,000.00</span></span></td>
<td><span data-ttu-id="a9351-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="a9351-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="a9351-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-288">8</span><span class="sxs-lookup"><span data-stu-id="a9351-288">8</span></span></td>
<td><span data-ttu-id="a9351-289">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="a9351-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-290">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-291">94.97</span><span class="sxs-lookup"><span data-stu-id="a9351-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-292">94.97</span><span class="sxs-lookup"><span data-stu-id="a9351-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-293">9</span><span class="sxs-lookup"><span data-stu-id="a9351-293">9</span></span></td>
<td><span data-ttu-id="a9351-294">Contant</span><span class="sxs-lookup"><span data-stu-id="a9351-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="a9351-295">-1,008.00</span></span></td>
<td><span data-ttu-id="a9351-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="a9351-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="a9351-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-298">10</span><span class="sxs-lookup"><span data-stu-id="a9351-298">10</span></span></td>
<td><span data-ttu-id="a9351-299">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="a9351-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-300">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-301">949.75</span><span class="sxs-lookup"><span data-stu-id="a9351-301">949.75</span></span></td>
<td><span data-ttu-id="a9351-302">949.75</span><span class="sxs-lookup"><span data-stu-id="a9351-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-303">11</span><span class="sxs-lookup"><span data-stu-id="a9351-303">11</span></span></td>
<td><span data-ttu-id="a9351-304">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-305">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="a9351-306">-949.75</span></span></td>
<td><span data-ttu-id="a9351-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="a9351-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a9351-308">Zoals in de bovenstaande tabel wordt aangegeven, moeten drie boeken worden gerapporteerd onder zowel wettelijke als IFRS-rapportage.</span><span class="sxs-lookup"><span data-stu-id="a9351-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="a9351-309">In het wettelijke boek wordt de leasebetaling vastgelegd volgens de regels voor cash-basis-boekhouding onder de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="a9351-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="a9351-310">Het wettelijke terugboekingsboek keert de wettelijke journaalposten om.</span><span class="sxs-lookup"><span data-stu-id="a9351-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="a9351-311">In het IFRS 16 boek worden de journaalposten gemaakt die zijn vereist volgens IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="a9351-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="a9351-312">U moet een lease slechts één keer invoeren.</span><span class="sxs-lookup"><span data-stu-id="a9351-312">You must enter a lease only one time.</span></span> <span data-ttu-id="a9351-313">Vervolgens kunt u de pagina **Boeken** openen om alle boeken te zien die aan de lease zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="a9351-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="a9351-314">Wanneer u de boeken maakt, moeten alle drie aan dezelfde leaserecord zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="a9351-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="a9351-315">De eerste journaalpost registreert de leasekosten uit hoofde van het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="a9351-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="a9351-316">U kunt de betalingen maken in een batch of door het betalingsschema te selecteren in het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="a9351-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="a9351-317">Voor dit voorbeeld wordt de volgende journaalpost gemaakt voor het wettelijk boek van het betalingsschema.</span><span class="sxs-lookup"><span data-stu-id="a9351-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="a9351-318">Leasebetaling – 31-1-2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="a9351-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="a9351-319">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="a9351-319">Account type</span></span> | <span data-ttu-id="a9351-320">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-320">Account number</span></span> | <span data-ttu-id="a9351-321">Laag</span><span class="sxs-lookup"><span data-stu-id="a9351-321">Layer</span></span>   | <span data-ttu-id="a9351-322">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-322">Account description</span></span> | <span data-ttu-id="a9351-323">Debet</span><span class="sxs-lookup"><span data-stu-id="a9351-323">Debit</span></span>    | <span data-ttu-id="a9351-324">Krediet</span><span class="sxs-lookup"><span data-stu-id="a9351-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a9351-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-325">Ledger</span></span>       | <span data-ttu-id="a9351-326">1</span><span class="sxs-lookup"><span data-stu-id="a9351-326">1</span></span>              | <span data-ttu-id="a9351-327">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-327">Current</span></span> | <span data-ttu-id="a9351-328">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="a9351-328">Lease expense</span></span>       | <span data-ttu-id="a9351-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-329">1,000.00</span></span> |          |
| <span data-ttu-id="a9351-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-330">Ledger</span></span>       | <span data-ttu-id="a9351-331">4</span><span class="sxs-lookup"><span data-stu-id="a9351-331">4</span></span>              | <span data-ttu-id="a9351-332">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-332">Current</span></span> | <span data-ttu-id="a9351-333">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="a9351-333">Clearing account</span></span>    |          | <span data-ttu-id="a9351-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-334">1,000.00</span></span> |

<span data-ttu-id="a9351-335">Een medewerker leveranciers gebruikt de standaard Dynamics 365-functionaliteit om een factuur te maken die moet worden betaald voor de lease buiten Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="a9351-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="a9351-336">In plaats van **Leasekosten** te selecteren als de debetrekening, selecteert de medewerker leveranciers een vereffeningsrekening om de volgende post te genereren.</span><span class="sxs-lookup"><span data-stu-id="a9351-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="a9351-337">Leveranciersproces – 31-1-2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="a9351-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="a9351-338">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="a9351-338">Account type</span></span> | <span data-ttu-id="a9351-339">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-339">Account number</span></span> | <span data-ttu-id="a9351-340">Laag</span><span class="sxs-lookup"><span data-stu-id="a9351-340">Layer</span></span>   | <span data-ttu-id="a9351-341">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-341">Account description</span></span> | <span data-ttu-id="a9351-342">Debet</span><span class="sxs-lookup"><span data-stu-id="a9351-342">Debit</span></span>    | <span data-ttu-id="a9351-343">Krediet</span><span class="sxs-lookup"><span data-stu-id="a9351-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a9351-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-344">Ledger</span></span>       | <span data-ttu-id="a9351-345">4</span><span class="sxs-lookup"><span data-stu-id="a9351-345">4</span></span>              | <span data-ttu-id="a9351-346">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-346">Current</span></span> | <span data-ttu-id="a9351-347">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="a9351-347">Clearing account</span></span>    | <span data-ttu-id="a9351-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-348">1,000.00</span></span> |          |
| <span data-ttu-id="a9351-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-349">Ledger</span></span>       | <span data-ttu-id="a9351-350">2</span><span class="sxs-lookup"><span data-stu-id="a9351-350">2</span></span>              | <span data-ttu-id="a9351-351">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-351">Current</span></span> | <span data-ttu-id="a9351-352">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="a9351-352">Bank fee</span></span>            | <span data-ttu-id="a9351-353">3.00</span><span class="sxs-lookup"><span data-stu-id="a9351-353">3.00</span></span>     |          |
| <span data-ttu-id="a9351-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-354">Ledger</span></span>       | <span data-ttu-id="a9351-355">3</span><span class="sxs-lookup"><span data-stu-id="a9351-355">3</span></span>              | <span data-ttu-id="a9351-356">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-356">Current</span></span> | <span data-ttu-id="a9351-357">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="a9351-357">VAT expense</span></span>         | <span data-ttu-id="a9351-358">5.00</span><span class="sxs-lookup"><span data-stu-id="a9351-358">5.00</span></span>     |          |
| <span data-ttu-id="a9351-359">Leverancier</span><span class="sxs-lookup"><span data-stu-id="a9351-359">Vendor</span></span>       | <span data-ttu-id="a9351-360">5</span><span class="sxs-lookup"><span data-stu-id="a9351-360">5</span></span>              | <span data-ttu-id="a9351-361">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-361">Current</span></span> | <span data-ttu-id="a9351-362">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="a9351-362">Accounts payable</span></span>    |          | <span data-ttu-id="a9351-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a9351-363">1,008.00</span></span> |

<span data-ttu-id="a9351-364">Wanneer het overzicht naar de leverancier wordt verzonden, volgt u het normale betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="a9351-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="a9351-365">Tijdens dit proces wordt de volgende journaalpost gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="a9351-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="a9351-366">Contante betaling – 31-1-2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="a9351-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="a9351-367">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="a9351-367">Account type</span></span> | <span data-ttu-id="a9351-368">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-368">Account number</span></span> | <span data-ttu-id="a9351-369">Laag</span><span class="sxs-lookup"><span data-stu-id="a9351-369">Layer</span></span>   | <span data-ttu-id="a9351-370">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-370">Account description</span></span> | <span data-ttu-id="a9351-371">Debet</span><span class="sxs-lookup"><span data-stu-id="a9351-371">Debit</span></span>    | <span data-ttu-id="a9351-372">Krediet</span><span class="sxs-lookup"><span data-stu-id="a9351-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="a9351-373">Leverancier</span><span class="sxs-lookup"><span data-stu-id="a9351-373">Vendor</span></span>       | <span data-ttu-id="a9351-374">5</span><span class="sxs-lookup"><span data-stu-id="a9351-374">5</span></span>              | <span data-ttu-id="a9351-375">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-375">Current</span></span> | <span data-ttu-id="a9351-376">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="a9351-376">Accounts Payable</span></span>    | <span data-ttu-id="a9351-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a9351-377">1,008.00</span></span> |          |
| <span data-ttu-id="a9351-378">Bank</span><span class="sxs-lookup"><span data-stu-id="a9351-378">Bank</span></span>         | <span data-ttu-id="a9351-379">9</span><span class="sxs-lookup"><span data-stu-id="a9351-379">9</span></span>              | <span data-ttu-id="a9351-380">Huidig</span><span class="sxs-lookup"><span data-stu-id="a9351-380">Current</span></span> | <span data-ttu-id="a9351-381">Contant</span><span class="sxs-lookup"><span data-stu-id="a9351-381">Cash</span></span>                |          | <span data-ttu-id="a9351-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a9351-382">1,008.00</span></span> |

<span data-ttu-id="a9351-383">U hebt op dit punt volledig verantwoord voor deze lease onder wettelijke rapportagevereisten en kunt een proefbalans genereren met behulp van de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="a9351-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="a9351-384">Het systeem geeft een proefbalans weer met de volgende cijfers.</span><span class="sxs-lookup"><span data-stu-id="a9351-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="a9351-385">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="a9351-386">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="a9351-387">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="a9351-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="a9351-388">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="a9351-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a9351-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="a9351-389">JE-100</span></span></th>
<th><span data-ttu-id="a9351-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="a9351-390">JE-110</span></span></th>
<th><span data-ttu-id="a9351-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="a9351-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a9351-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="a9351-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="a9351-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a9351-395">1</span><span class="sxs-lookup"><span data-stu-id="a9351-395">1</span></span></td>
<td><span data-ttu-id="a9351-396">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="a9351-396">Lease expense</span></span></td>
<td><span data-ttu-id="a9351-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-399">2</span><span class="sxs-lookup"><span data-stu-id="a9351-399">2</span></span></td>
<td><span data-ttu-id="a9351-400">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="a9351-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-401">3.00</span><span class="sxs-lookup"><span data-stu-id="a9351-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-402">3.00</span><span class="sxs-lookup"><span data-stu-id="a9351-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-403">3</span><span class="sxs-lookup"><span data-stu-id="a9351-403">3</span></span></td>
<td><span data-ttu-id="a9351-404">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="a9351-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-405">5.00</span><span class="sxs-lookup"><span data-stu-id="a9351-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-406">5.00</span><span class="sxs-lookup"><span data-stu-id="a9351-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-407">4</span><span class="sxs-lookup"><span data-stu-id="a9351-407">4</span></span></td>
<td><span data-ttu-id="a9351-408">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="a9351-408">Clearing account</span></span></td>
<td><span data-ttu-id="a9351-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="a9351-409">-1,000.00</span></span></td>
<td><span data-ttu-id="a9351-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-411">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-412">5</span><span class="sxs-lookup"><span data-stu-id="a9351-412">5</span></span></td>
<td><span data-ttu-id="a9351-413">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="a9351-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="a9351-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="a9351-414">-1,008.00</span></span></td>
<td><span data-ttu-id="a9351-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="a9351-415">1,008.00</span></span></td>
<td><span data-ttu-id="a9351-416">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-417">6</span><span class="sxs-lookup"><span data-stu-id="a9351-417">6</span></span></td>
<td><span data-ttu-id="a9351-418">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="a9351-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-419">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-420">7</span><span class="sxs-lookup"><span data-stu-id="a9351-420">7</span></span></td>
<td><span data-ttu-id="a9351-421">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="a9351-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-422">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-423">8</span><span class="sxs-lookup"><span data-stu-id="a9351-423">8</span></span></td>
<td><span data-ttu-id="a9351-424">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="a9351-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-425">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-426">9</span><span class="sxs-lookup"><span data-stu-id="a9351-426">9</span></span></td>
<td><span data-ttu-id="a9351-427">Contant</span><span class="sxs-lookup"><span data-stu-id="a9351-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="a9351-428">-1,008.00</span></span></td>
<td><span data-ttu-id="a9351-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="a9351-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-430">10</span><span class="sxs-lookup"><span data-stu-id="a9351-430">10</span></span></td>
<td><span data-ttu-id="a9351-431">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="a9351-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-432">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a9351-433">11</span><span class="sxs-lookup"><span data-stu-id="a9351-433">11</span></span></td>
<td><span data-ttu-id="a9351-434">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="a9351-435">0,00</span><span class="sxs-lookup"><span data-stu-id="a9351-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a9351-436">Als u de IFRS 16 cijfers wilt gebruiken om dezelfde proefbalans uit te voeren, moeten de wettelijke boekhoudingsjournaalposten worden teruggeboekt en moeten de IFRS 16-journaalposten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="a9351-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="a9351-437">Voor het omkeren van de wettelijke journaalposten bevat dit voorbeeld een wettelijk terugboekingsboek met dezelfde instellingen als het wettelijke boek, maar een tegengesteld boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="a9351-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="a9351-438">Het wettelijke boek heeft bijvoorbeeld een leasekostenrekening *gedebiteerd*, maar het terugboekingsboek *crediteert* deze rekening.</span><span class="sxs-lookup"><span data-stu-id="a9351-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="a9351-439">Deze relaties worden eenvoudig gedefinieerd in de boekingsrekeningen Activa leasen op de pagina **Parameters voor activa leasing** (**Activa leasen \> Instellen \> Parameters voor activa leasing**).</span><span class="sxs-lookup"><span data-stu-id="a9351-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="a9351-440">Wanneer hetzelfde proces dat is gebruikt voor het wettelijke boek, wordt gebruikt voor het terugboekingsboek, wordt de volgende journaalpost geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="a9351-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="a9351-441">Het verschil is dat het terugboekingsboek de stornoposten uit het wettelijke boek boekt.</span><span class="sxs-lookup"><span data-stu-id="a9351-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="a9351-442">De stornoposten worden ook in de aangepaste laag aangebracht.</span><span class="sxs-lookup"><span data-stu-id="a9351-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="a9351-443">Wanneer een proefbalans wordt uitgevoerd op de huidige laag, worden de stornojournaalposten niet opgenomen.</span><span class="sxs-lookup"><span data-stu-id="a9351-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="a9351-444">Leasebetaling – 31-1-2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="a9351-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="a9351-445">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="a9351-445">Account type</span></span> | <span data-ttu-id="a9351-446">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-446">Account number</span></span> | <span data-ttu-id="a9351-447">Laag</span><span class="sxs-lookup"><span data-stu-id="a9351-447">Layer</span></span>  | <span data-ttu-id="a9351-448">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-448">Account description</span></span> | <span data-ttu-id="a9351-449">Debet</span><span class="sxs-lookup"><span data-stu-id="a9351-449">Debit</span></span>    | <span data-ttu-id="a9351-450">Krediet</span><span class="sxs-lookup"><span data-stu-id="a9351-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="a9351-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-451">Ledger</span></span>       | <span data-ttu-id="a9351-452">4</span><span class="sxs-lookup"><span data-stu-id="a9351-452">4</span></span>              | <span data-ttu-id="a9351-453">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-453">Custom</span></span> | <span data-ttu-id="a9351-454">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="a9351-454">Clearing account</span></span>    | <span data-ttu-id="a9351-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-455">1,000.00</span></span> |          |
| <span data-ttu-id="a9351-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-456">Ledger</span></span>       | <span data-ttu-id="a9351-457">1</span><span class="sxs-lookup"><span data-stu-id="a9351-457">1</span></span>              | <span data-ttu-id="a9351-458">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-458">Custom</span></span> | <span data-ttu-id="a9351-459">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="a9351-459">Lease expense</span></span>       |          | <span data-ttu-id="a9351-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-460">1,000.00</span></span> |

<span data-ttu-id="a9351-461">Nu u de wettelijk journaalposten hebt verwijderd, worden alle journaalposten geboekt die IFRS 16 vereist in het IFRS 16 boek.</span><span class="sxs-lookup"><span data-stu-id="a9351-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="a9351-462">Deze posten omvatten de eerste toerekening van het RoU activum en de verplichting, en de record van rente en afschrijving.</span><span class="sxs-lookup"><span data-stu-id="a9351-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="a9351-463">Initiële toerekening - 1-1-2020 - JE 140</span><span class="sxs-lookup"><span data-stu-id="a9351-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="a9351-464">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="a9351-464">Account type</span></span> | <span data-ttu-id="a9351-465">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-465">Account number</span></span> | <span data-ttu-id="a9351-466">Laag</span><span class="sxs-lookup"><span data-stu-id="a9351-466">Layer</span></span>  | <span data-ttu-id="a9351-467">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-467">Account description</span></span>      | <span data-ttu-id="a9351-468">Debet</span><span class="sxs-lookup"><span data-stu-id="a9351-468">Debit</span></span>     | <span data-ttu-id="a9351-469">Krediet</span><span class="sxs-lookup"><span data-stu-id="a9351-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="a9351-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-470">Ledger</span></span>       | <span data-ttu-id="a9351-471">6</span><span class="sxs-lookup"><span data-stu-id="a9351-471">6</span></span>              | <span data-ttu-id="a9351-472">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-472">Custom</span></span> | <span data-ttu-id="a9351-473">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="a9351-473">ROU Asset</span></span>                | <span data-ttu-id="a9351-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a9351-474">22,793.90</span></span> |           |
| <span data-ttu-id="a9351-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-475">Ledger</span></span>       | <span data-ttu-id="a9351-476">7</span><span class="sxs-lookup"><span data-stu-id="a9351-476">7</span></span>              | <span data-ttu-id="a9351-477">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-477">Custom</span></span> | <span data-ttu-id="a9351-478">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="a9351-478">Finance lease obligation</span></span> |           | <span data-ttu-id="a9351-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="a9351-479">22,793.90</span></span> |

<span data-ttu-id="a9351-480">De leasebetaling wordt geboekt zoals de andere leasebetalingen.</span><span class="sxs-lookup"><span data-stu-id="a9351-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="a9351-481">De reden voor het gebruik van de vereffeningsrekening is ervoor te zorgen dat contant geld slechts één keer wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="a9351-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="a9351-482">Leasebetaling – 31-1-2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="a9351-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="a9351-483">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="a9351-483">Account type</span></span> | <span data-ttu-id="a9351-484">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-484">Account number</span></span> | <span data-ttu-id="a9351-485">Laag</span><span class="sxs-lookup"><span data-stu-id="a9351-485">Layer</span></span>  | <span data-ttu-id="a9351-486">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-486">Account description</span></span>      | <span data-ttu-id="a9351-487">Debet</span><span class="sxs-lookup"><span data-stu-id="a9351-487">Debit</span></span>    | <span data-ttu-id="a9351-488">Krediet</span><span class="sxs-lookup"><span data-stu-id="a9351-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="a9351-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-489">Ledger</span></span>       | <span data-ttu-id="a9351-490">7</span><span class="sxs-lookup"><span data-stu-id="a9351-490">7</span></span>              | <span data-ttu-id="a9351-491">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-491">Custom</span></span> | <span data-ttu-id="a9351-492">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="a9351-492">Finance lease obligation</span></span> | <span data-ttu-id="a9351-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-493">1,000.00</span></span> |          |
| <span data-ttu-id="a9351-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-494">Ledger</span></span>       | <span data-ttu-id="a9351-495">4</span><span class="sxs-lookup"><span data-stu-id="a9351-495">4</span></span>              | <span data-ttu-id="a9351-496">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-496">Custom</span></span> | <span data-ttu-id="a9351-497">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="a9351-497">Clearing account</span></span>         |          | <span data-ttu-id="a9351-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a9351-498">1,000.00</span></span> |

<span data-ttu-id="a9351-499">De journaalpost voor rentelasten wordt gegenereerd op basis van het afschrijvingsschema voor verplichtingen.</span><span class="sxs-lookup"><span data-stu-id="a9351-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="a9351-500">Rente-uitgaven - 31-1-2020 - JE 160</span><span class="sxs-lookup"><span data-stu-id="a9351-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="a9351-501">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="a9351-501">Account type</span></span> | <span data-ttu-id="a9351-502">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-502">Account number</span></span> | <span data-ttu-id="a9351-503">Laag</span><span class="sxs-lookup"><span data-stu-id="a9351-503">Layer</span></span>  | <span data-ttu-id="a9351-504">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-504">Account description</span></span>      | <span data-ttu-id="a9351-505">Debet</span><span class="sxs-lookup"><span data-stu-id="a9351-505">Debit</span></span> | <span data-ttu-id="a9351-506">Krediet</span><span class="sxs-lookup"><span data-stu-id="a9351-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="a9351-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-507">Ledger</span></span>       | <span data-ttu-id="a9351-508">8</span><span class="sxs-lookup"><span data-stu-id="a9351-508">8</span></span>              | <span data-ttu-id="a9351-509">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-509">Custom</span></span> | <span data-ttu-id="a9351-510">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="a9351-510">Interest expense</span></span>         | <span data-ttu-id="a9351-511">94.97</span><span class="sxs-lookup"><span data-stu-id="a9351-511">94.97</span></span> |        |
| <span data-ttu-id="a9351-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-512">Ledger</span></span>       | <span data-ttu-id="a9351-513">7</span><span class="sxs-lookup"><span data-stu-id="a9351-513">7</span></span>              | <span data-ttu-id="a9351-514">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-514">Custom</span></span> | <span data-ttu-id="a9351-515">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="a9351-515">Finance lease obligation</span></span> |       | <span data-ttu-id="a9351-516">94.97</span><span class="sxs-lookup"><span data-stu-id="a9351-516">94.97</span></span>  |

<span data-ttu-id="a9351-517">De journaalpost voor afschrijvingskosten wordt gegenereerd op basis van het schema activumafschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="a9351-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="a9351-518">Afschrijvingskosten - 31-1-2020 - JE 170</span><span class="sxs-lookup"><span data-stu-id="a9351-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="a9351-519">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="a9351-519">Account type</span></span> | <span data-ttu-id="a9351-520">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-520">Account number</span></span> | <span data-ttu-id="a9351-521">Laag</span><span class="sxs-lookup"><span data-stu-id="a9351-521">Layer</span></span>  | <span data-ttu-id="a9351-522">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-522">Account description</span></span>      | <span data-ttu-id="a9351-523">Debet</span><span class="sxs-lookup"><span data-stu-id="a9351-523">Debit</span></span>  | <span data-ttu-id="a9351-524">Krediet</span><span class="sxs-lookup"><span data-stu-id="a9351-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="a9351-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-525">Ledger</span></span>       | <span data-ttu-id="a9351-526">10</span><span class="sxs-lookup"><span data-stu-id="a9351-526">10</span></span>             | <span data-ttu-id="a9351-527">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-527">Custom</span></span> | <span data-ttu-id="a9351-528">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="a9351-528">Depreciation expense</span></span>     | <span data-ttu-id="a9351-529">949.75</span><span class="sxs-lookup"><span data-stu-id="a9351-529">949.75</span></span> |        |
| <span data-ttu-id="a9351-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="a9351-530">Ledger</span></span>       | <span data-ttu-id="a9351-531">11</span><span class="sxs-lookup"><span data-stu-id="a9351-531">11</span></span>             | <span data-ttu-id="a9351-532">Aangepast</span><span class="sxs-lookup"><span data-stu-id="a9351-532">Custom</span></span> | <span data-ttu-id="a9351-533">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="a9351-534">949.75</span><span class="sxs-lookup"><span data-stu-id="a9351-534">949.75</span></span> |

<span data-ttu-id="a9351-535">Nadat al deze journaalposten zijn gemaakt en geboekt, ziet u de volgende waarden voor "aangepaste laag 1".</span><span class="sxs-lookup"><span data-stu-id="a9351-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="a9351-536">De laatste kolom bevat de bankkosten, de kosten voor de toegevoegde waarde (btw) en de reductie van contant geld uit de vorige laag, maar bevat niet de journaalposten voor wettelijke rapportage.</span><span class="sxs-lookup"><span data-stu-id="a9351-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="a9351-537">Daarom bereikt u echte mogelijkheden voor dubbele rapportage.</span><span class="sxs-lookup"><span data-stu-id="a9351-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="a9351-538">Op dit punt hoeft het bedrijf alleen zijn proefbalans uit te voeren en de huidige laag en de aangepaste laag combineren om een IFRS-proefbalans te maken.</span><span class="sxs-lookup"><span data-stu-id="a9351-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="a9351-539">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="a9351-539">Account No</span></span> | <span data-ttu-id="a9351-540">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-540">Description</span></span>              | <span data-ttu-id="a9351-541">Wettelijk boek\-Huidige laag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="a9351-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="a9351-542">Wettelijk boek\-Huidige laag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="a9351-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="a9351-543">Wettelijk boek\-Huidige laag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="a9351-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="a9351-544">Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="a9351-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="a9351-545">Terugboekingsboek\-Aangepaste laag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="a9351-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="a9351-546">IFRS 16-boek\-Aangepaste laag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="a9351-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="a9351-547">IFRS 16-boek\-Aangepaste laag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="a9351-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="a9351-548">IFRS 16-boek\-Aangepaste laag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="a9351-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="a9351-549">IFRS 16-boek\-Aangepaste laag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="a9351-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="a9351-550">Aangepaste laag \+ Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="a9351-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="a9351-551">1</span><span class="sxs-lookup"><span data-stu-id="a9351-551">1</span></span>          | <span data-ttu-id="a9351-552">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="a9351-552">Lease expense</span></span>            | <span data-ttu-id="a9351-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="a9351-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-554">1,000\.00</span></span>               |   | <span data-ttu-id="a9351-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="a9351-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="a9351-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-556">0\.00</span></span>                                   |
| <span data-ttu-id="a9351-557">2</span><span class="sxs-lookup"><span data-stu-id="a9351-557">2</span></span>          | <span data-ttu-id="a9351-558">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="a9351-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="a9351-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="a9351-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a9351-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-561">3\.00</span></span>                                   |
| <span data-ttu-id="a9351-562">3</span><span class="sxs-lookup"><span data-stu-id="a9351-562">3</span></span>          | <span data-ttu-id="a9351-563">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="a9351-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="a9351-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="a9351-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a9351-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-566">5\.00</span></span>                                   |
| <span data-ttu-id="a9351-567">4</span><span class="sxs-lookup"><span data-stu-id="a9351-567">4</span></span>          | <span data-ttu-id="a9351-568">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="a9351-568">Clearing account</span></span>         | <span data-ttu-id="a9351-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="a9351-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="a9351-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-571">0\.00</span></span>                   |   | <span data-ttu-id="a9351-572">1.000</span><span class="sxs-lookup"><span data-stu-id="a9351-572">1,000</span></span>                                           |                                                | <span data-ttu-id="a9351-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="a9351-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="a9351-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-574">0\.00</span></span>                                   |
| <span data-ttu-id="a9351-575">5</span><span class="sxs-lookup"><span data-stu-id="a9351-575">5</span></span>          | <span data-ttu-id="a9351-576">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="a9351-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="a9351-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="a9351-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-578">1,008\.00</span></span>                                         | <span data-ttu-id="a9351-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a9351-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-580">0\.00</span></span>                                   |
| <span data-ttu-id="a9351-581">6</span><span class="sxs-lookup"><span data-stu-id="a9351-581">6</span></span>          | <span data-ttu-id="a9351-582">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="a9351-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="a9351-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="a9351-584">22,794</span><span class="sxs-lookup"><span data-stu-id="a9351-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="a9351-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="a9351-585">22,793\.90</span></span>                              |
| <span data-ttu-id="a9351-586">7</span><span class="sxs-lookup"><span data-stu-id="a9351-586">7</span></span>          | <span data-ttu-id="a9351-587">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="a9351-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="a9351-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="a9351-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="a9351-589">\-22,794</span></span>                                       | <span data-ttu-id="a9351-590">1.000</span><span class="sxs-lookup"><span data-stu-id="a9351-590">1,000</span></span>                                          | <span data-ttu-id="a9351-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="a9351-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="a9351-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="a9351-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="a9351-593">8</span><span class="sxs-lookup"><span data-stu-id="a9351-593">8</span></span>          | <span data-ttu-id="a9351-594">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="a9351-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="a9351-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="a9351-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="a9351-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="a9351-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="a9351-597">94\.97</span></span>                                  |
| <span data-ttu-id="a9351-598">9</span><span class="sxs-lookup"><span data-stu-id="a9351-598">9</span></span>          | <span data-ttu-id="a9351-599">Contant</span><span class="sxs-lookup"><span data-stu-id="a9351-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="a9351-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="a9351-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="a9351-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="a9351-603">10</span><span class="sxs-lookup"><span data-stu-id="a9351-603">10</span></span>         | <span data-ttu-id="a9351-604">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="a9351-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="a9351-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="a9351-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="a9351-606">949\.75</span></span>                                        | <span data-ttu-id="a9351-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="a9351-607">949\.75</span></span>                                 |
| <span data-ttu-id="a9351-608">11</span><span class="sxs-lookup"><span data-stu-id="a9351-608">11</span></span>         | <span data-ttu-id="a9351-609">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="a9351-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="a9351-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="a9351-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="a9351-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="a9351-611">\-949\.75</span></span>                                      | <span data-ttu-id="a9351-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="a9351-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]