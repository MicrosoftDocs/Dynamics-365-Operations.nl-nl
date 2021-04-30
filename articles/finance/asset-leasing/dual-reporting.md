---
title: Dubbele rapportage
description: In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86f42f8db707f3b8c62b9ec4c39ad6464f080748
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881151"
---
# <a name="dual-reporting"></a><span data-ttu-id="ad954-103">Dubbele rapportage</span><span class="sxs-lookup"><span data-stu-id="ad954-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad954-104">In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="ad954-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="ad954-105">Vertrouwdheid met boekingslagen in Microsoft Dynamics 365 Finance is vereist en maakt het voorbeeld gemakkelijker te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="ad954-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="ad954-106">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="ad954-106">Example</span></span>

<span data-ttu-id="ad954-107">In het volgende voorbeeld wordt een lease verantwoord onder de Italiaanse wettelijke rapportering door middel van de cash-basis-methode en de IFRS-rapportagemethoden.</span><span class="sxs-lookup"><span data-stu-id="ad954-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="ad954-108">Het bedrijf moet drie boeken maken om te verantwoorden voor zowel de Italiaanse wettelijke vereisten als de IFRS 16-vereisten.</span><span class="sxs-lookup"><span data-stu-id="ad954-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="ad954-109">Eén boek is vereist voor IFRS 16, één boek is vereist voor wettelijke vereisten en één boek is vereist om de wettelijke boekingen automatisch terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="ad954-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="ad954-110">De boeken worden ingesteld, zoals in de volgende tabellen wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad954-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="ad954-111">**IFRS 16-boek**</span><span class="sxs-lookup"><span data-stu-id="ad954-111">**IFRS 16 book**</span></span>

<span data-ttu-id="ad954-112">Het IFRS 16 boek is zo ingesteld dat het voldoet aan de IFRS 16-boekhoudnorm.</span><span class="sxs-lookup"><span data-stu-id="ad954-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="ad954-113">Alle posten die in dit boek worden geboekt, worden naar een aangepaste laag geboekt.</span><span class="sxs-lookup"><span data-stu-id="ad954-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="ad954-114">Naam</span><span class="sxs-lookup"><span data-stu-id="ad954-114">Name</span></span>                                    | <span data-ttu-id="ad954-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="ad954-116">Boektype</span><span class="sxs-lookup"><span data-stu-id="ad954-116">Book type</span></span>                               | <span data-ttu-id="ad954-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="ad954-117">IFRS 16</span></span>        |
| <span data-ttu-id="ad954-118">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-118">Book description</span></span>                        | <span data-ttu-id="ad954-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="ad954-119">IFRS 16</span></span>        |
| <span data-ttu-id="ad954-120">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="ad954-120">Posting Layer</span></span>                           | <span data-ttu-id="ad954-121">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="ad954-121">Custom layer 1</span></span> |
| <span data-ttu-id="ad954-122">Leasetype</span><span class="sxs-lookup"><span data-stu-id="ad954-122">Lease Type</span></span>                              | <span data-ttu-id="ad954-123">Finance</span><span class="sxs-lookup"><span data-stu-id="ad954-123">Finance</span></span>        |
| <span data-ttu-id="ad954-124">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="ad954-124">Accounting Framework</span></span>                    | <span data-ttu-id="ad954-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="ad954-125">IFRS 16</span></span>        |
| <span data-ttu-id="ad954-126">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="ad954-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="ad954-127">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-127">0.00</span></span>           |
| <span data-ttu-id="ad954-128">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="ad954-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="ad954-129">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-129">0.00</span></span>           |
| <span data-ttu-id="ad954-130">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="ad954-130">Short-term threshold</span></span>                    | <span data-ttu-id="ad954-131">12</span><span class="sxs-lookup"><span data-stu-id="ad954-131">12</span></span>             |
| <span data-ttu-id="ad954-132">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="ad954-132">Low Value Threshold</span></span>                     | <span data-ttu-id="ad954-133">5.000,00</span><span class="sxs-lookup"><span data-stu-id="ad954-133">5,000.00</span></span>       |
| <span data-ttu-id="ad954-134">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="ad954-134">Pay to Vendor</span></span>                           | <span data-ttu-id="ad954-135">No</span><span class="sxs-lookup"><span data-stu-id="ad954-135">No</span></span>             |

<span data-ttu-id="ad954-136">**Wettelijk boek**</span><span class="sxs-lookup"><span data-stu-id="ad954-136">**Statutory book**</span></span>

<span data-ttu-id="ad954-137">Het wettelijke boek is een cash-basis-boek waar het bedrijf de leasekosten zal verantwoorden als het bedrag aan geld dat maandelijks wordt betaald voor huur.</span><span class="sxs-lookup"><span data-stu-id="ad954-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="ad954-138">Dit boek produceert geen RoU-activum of leaseverplichtingen.</span><span class="sxs-lookup"><span data-stu-id="ad954-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="ad954-139">Naam</span><span class="sxs-lookup"><span data-stu-id="ad954-139">Name</span></span>                                    | <span data-ttu-id="ad954-140">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="ad954-141">Boektype</span><span class="sxs-lookup"><span data-stu-id="ad954-141">Book type</span></span>                               | <span data-ttu-id="ad954-142">Wettelijk</span><span class="sxs-lookup"><span data-stu-id="ad954-142">Statutory</span></span>   |
| <span data-ttu-id="ad954-143">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-143">Book description</span></span>                        | <span data-ttu-id="ad954-144">Lokale GAAP</span><span class="sxs-lookup"><span data-stu-id="ad954-144">Local GAAP</span></span>  |
| <span data-ttu-id="ad954-145">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="ad954-145">Posting Layer</span></span>                           | <span data-ttu-id="ad954-146">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-146">Current</span></span>     |
| <span data-ttu-id="ad954-147">Leasetype</span><span class="sxs-lookup"><span data-stu-id="ad954-147">Lease Type</span></span>                              | <span data-ttu-id="ad954-148">Automatisch</span><span class="sxs-lookup"><span data-stu-id="ad954-148">Automatic</span></span>   |
| <span data-ttu-id="ad954-149">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="ad954-149">Accounting Framework</span></span>                    | <span data-ttu-id="ad954-150">Contante basis</span><span class="sxs-lookup"><span data-stu-id="ad954-150">Cash basis</span></span>  |
| <span data-ttu-id="ad954-151">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="ad954-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="ad954-152">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-152">0.00</span></span>        |
| <span data-ttu-id="ad954-153">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="ad954-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="ad954-154">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-154">0.00</span></span>        |
| <span data-ttu-id="ad954-155">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="ad954-155">Short-term threshold</span></span>                    | <span data-ttu-id="ad954-156">0</span><span class="sxs-lookup"><span data-stu-id="ad954-156">0</span></span>           |
| <span data-ttu-id="ad954-157">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="ad954-157">Low Value Threshold</span></span>                     | <span data-ttu-id="ad954-158">0</span><span class="sxs-lookup"><span data-stu-id="ad954-158">0</span></span>           |
| <span data-ttu-id="ad954-159">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="ad954-159">Pay to Vendor</span></span>                           | <span data-ttu-id="ad954-160">No</span><span class="sxs-lookup"><span data-stu-id="ad954-160">No</span></span>          |

<span data-ttu-id="ad954-161">**Wettelijk terugboekingsboek**</span><span class="sxs-lookup"><span data-stu-id="ad954-161">**Statutory reversal book**</span></span>

<span data-ttu-id="ad954-162">Het wettelijke terugboekingsboek wordt op dezelfde manier ingesteld als het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="ad954-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="ad954-163">Naam</span><span class="sxs-lookup"><span data-stu-id="ad954-163">Name</span></span>                                    | <span data-ttu-id="ad954-164">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="ad954-165">Boektype</span><span class="sxs-lookup"><span data-stu-id="ad954-165">Book type</span></span>                               | <span data-ttu-id="ad954-166">Wettelijk - terugboeking</span><span class="sxs-lookup"><span data-stu-id="ad954-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="ad954-167">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-167">Book description</span></span>                        | <span data-ttu-id="ad954-168">Boek om wettelijk boek terug te boeken</span><span class="sxs-lookup"><span data-stu-id="ad954-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="ad954-169">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="ad954-169">Posting Layer</span></span>                           | <span data-ttu-id="ad954-170">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="ad954-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="ad954-171">Leasetype</span><span class="sxs-lookup"><span data-stu-id="ad954-171">Lease Type</span></span>                              | <span data-ttu-id="ad954-172">Automatisch</span><span class="sxs-lookup"><span data-stu-id="ad954-172">Automatic</span></span>                      |
| <span data-ttu-id="ad954-173">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="ad954-173">Accounting Framework</span></span>                    | <span data-ttu-id="ad954-174">Contante basis</span><span class="sxs-lookup"><span data-stu-id="ad954-174">Cash basis</span></span>                     |
| <span data-ttu-id="ad954-175">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="ad954-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="ad954-176">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-176">0.00</span></span>                           |
| <span data-ttu-id="ad954-177">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="ad954-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="ad954-178">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-178">0.00</span></span>                           |
| <span data-ttu-id="ad954-179">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="ad954-179">Short-term threshold</span></span>                    | <span data-ttu-id="ad954-180">0</span><span class="sxs-lookup"><span data-stu-id="ad954-180">0</span></span>                              |
| <span data-ttu-id="ad954-181">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="ad954-181">Low Value Threshold</span></span>                     | <span data-ttu-id="ad954-182">0</span><span class="sxs-lookup"><span data-stu-id="ad954-182">0</span></span>                              |
| <span data-ttu-id="ad954-183">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="ad954-183">Pay to Vendor</span></span>                           | <span data-ttu-id="ad954-184">No</span><span class="sxs-lookup"><span data-stu-id="ad954-184">No</span></span>                             |

<span data-ttu-id="ad954-185">Voor dit voorbeeld is er een lease gemaakt met de volgende instellingen op de tabbladen **Algemeen** en **Betalingsschemaregels**.</span><span class="sxs-lookup"><span data-stu-id="ad954-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="ad954-186">**Tabblad Algemeen**</span><span class="sxs-lookup"><span data-stu-id="ad954-186">**General tab**</span></span>

| <span data-ttu-id="ad954-187">Veld</span><span class="sxs-lookup"><span data-stu-id="ad954-187">Field</span></span>                      | <span data-ttu-id="ad954-188">Waarde</span><span class="sxs-lookup"><span data-stu-id="ad954-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="ad954-189">Verhoogd leningtarief</span><span class="sxs-lookup"><span data-stu-id="ad954-189">Incremental borrowing rate</span></span> | <span data-ttu-id="ad954-190">5%</span><span class="sxs-lookup"><span data-stu-id="ad954-190">5%</span></span>               |
| <span data-ttu-id="ad954-191">Begindatum</span><span class="sxs-lookup"><span data-stu-id="ad954-191">Commencement date</span></span>          | <span data-ttu-id="ad954-192">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="ad954-192">1/1/2020</span></span>         |
| <span data-ttu-id="ad954-193">Leasegroep</span><span class="sxs-lookup"><span data-stu-id="ad954-193">Lease group</span></span>                | <span data-ttu-id="ad954-194">Gebouwen</span><span class="sxs-lookup"><span data-stu-id="ad954-194">Buildings</span></span>        |
| <span data-ttu-id="ad954-195">Leverancier</span><span class="sxs-lookup"><span data-stu-id="ad954-195">Vendor</span></span>                     | <span data-ttu-id="ad954-196">1001</span><span class="sxs-lookup"><span data-stu-id="ad954-196">1001</span></span>             |
| <span data-ttu-id="ad954-197">Reële waarde van het activum</span><span class="sxs-lookup"><span data-stu-id="ad954-197">Fair value of the asset</span></span>    | <span data-ttu-id="ad954-198">245,000</span><span class="sxs-lookup"><span data-stu-id="ad954-198">245,000</span></span>          |
| <span data-ttu-id="ad954-199">Economische levensduur activum</span><span class="sxs-lookup"><span data-stu-id="ad954-199">Asset useful life</span></span>          | <span data-ttu-id="ad954-200">120</span><span class="sxs-lookup"><span data-stu-id="ad954-200">120</span></span>              |
| <span data-ttu-id="ad954-201">Type annuïteit</span><span class="sxs-lookup"><span data-stu-id="ad954-201">Annuity type</span></span>               | <span data-ttu-id="ad954-202">Normale annuïteit</span><span class="sxs-lookup"><span data-stu-id="ad954-202">Ordinary annuity</span></span> |
| <span data-ttu-id="ad954-203">Samenstellingsinterval</span><span class="sxs-lookup"><span data-stu-id="ad954-203">Compounding interval</span></span>       | <span data-ttu-id="ad954-204">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="ad954-204">Monthly</span></span>          |

<span data-ttu-id="ad954-205">**Tabblad Regels van betalingsschema**</span><span class="sxs-lookup"><span data-stu-id="ad954-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="ad954-206">Veld</span><span class="sxs-lookup"><span data-stu-id="ad954-206">Field</span></span>             | <span data-ttu-id="ad954-207">Waarde</span><span class="sxs-lookup"><span data-stu-id="ad954-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="ad954-208">Begindatum</span><span class="sxs-lookup"><span data-stu-id="ad954-208">Start date</span></span>        | <span data-ttu-id="ad954-209">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="ad954-209">1/1/2020</span></span>   |
| <span data-ttu-id="ad954-210">Periode-interval</span><span class="sxs-lookup"><span data-stu-id="ad954-210">Period interval</span></span>   | <span data-ttu-id="ad954-211">Maanden</span><span class="sxs-lookup"><span data-stu-id="ad954-211">Months</span></span>     |
| <span data-ttu-id="ad954-212">Perioden</span><span class="sxs-lookup"><span data-stu-id="ad954-212">Periods</span></span>           | <span data-ttu-id="ad954-213">24</span><span class="sxs-lookup"><span data-stu-id="ad954-213">24</span></span>         |
| <span data-ttu-id="ad954-214">Einddatum</span><span class="sxs-lookup"><span data-stu-id="ad954-214">End date</span></span>          | <span data-ttu-id="ad954-215">31-12-2020</span><span class="sxs-lookup"><span data-stu-id="ad954-215">12/31/2020</span></span> |
| <span data-ttu-id="ad954-216">Betalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="ad954-216">Payment frequency</span></span> | <span data-ttu-id="ad954-217">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="ad954-217">Monthly</span></span>    |
| <span data-ttu-id="ad954-218">Betalingsbedrag</span><span class="sxs-lookup"><span data-stu-id="ad954-218">Payment amount</span></span>    | <span data-ttu-id="ad954-219">1.000</span><span class="sxs-lookup"><span data-stu-id="ad954-219">1,000</span></span>      |

<span data-ttu-id="ad954-220">Als u deze lease onder twee raamwerken wilt verantwoorden, gebruikt u een huidige boekingslaag en een aangepaste boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="ad954-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="ad954-221">In de volgende tabel ziet u een voorbeeld van elke journaalpost die voor elke rapportagestandaard de financiële waarde reëel moet representeren.</span><span class="sxs-lookup"><span data-stu-id="ad954-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="ad954-222">Hierna wordt een gedetailleerde omschrijving gegeven van elke journaalpost voor de eerste maand van de lease.</span><span class="sxs-lookup"><span data-stu-id="ad954-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="ad954-223">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="ad954-224">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="ad954-225">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="ad954-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="ad954-226">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="ad954-226">Current layer total</span></span></th>
<th><span data-ttu-id="ad954-227">Terugboekingsboek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="ad954-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="ad954-228">IFRS 16-boek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="ad954-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="ad954-229">Huidige laag + aangepaste laagtotaal</span><span class="sxs-lookup"><span data-stu-id="ad954-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ad954-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="ad954-230">JE-100</span></span></th>
<th><span data-ttu-id="ad954-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="ad954-231">JE-110</span></span></th>
<th><span data-ttu-id="ad954-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="ad954-232">JE-120</span></span></th>
<th><span data-ttu-id="ad954-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="ad954-233">JE-130</span></span></th>
<th><span data-ttu-id="ad954-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="ad954-234">JE-140</span></span></th>
<th><span data-ttu-id="ad954-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="ad954-235">JE-150</span></span></th>
<th><span data-ttu-id="ad954-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="ad954-236">JE-160</span></span></th>
<th><span data-ttu-id="ad954-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="ad954-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ad954-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ad954-246">1</span><span class="sxs-lookup"><span data-stu-id="ad954-246">1</span></span></td>
<td><span data-ttu-id="ad954-247">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="ad954-247">Lease expense</span></span></td>
<td><span data-ttu-id="ad954-248">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ad954-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-249">1,000.00</span></span></td>
<td><span data-ttu-id="ad954-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ad954-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-251">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-252">2</span><span class="sxs-lookup"><span data-stu-id="ad954-252">2</span></span></td>
<td><span data-ttu-id="ad954-253">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="ad954-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-254">3,00</span><span class="sxs-lookup"><span data-stu-id="ad954-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-255">3.00</span><span class="sxs-lookup"><span data-stu-id="ad954-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-256">3.00</span><span class="sxs-lookup"><span data-stu-id="ad954-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-257">3</span><span class="sxs-lookup"><span data-stu-id="ad954-257">3</span></span></td>
<td><span data-ttu-id="ad954-258">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="ad954-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-259">5.00</span><span class="sxs-lookup"><span data-stu-id="ad954-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-260">5.00</span><span class="sxs-lookup"><span data-stu-id="ad954-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-261">5.00</span><span class="sxs-lookup"><span data-stu-id="ad954-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-262">4</span><span class="sxs-lookup"><span data-stu-id="ad954-262">4</span></span></td>
<td><span data-ttu-id="ad954-263">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="ad954-263">Clearing account</span></span></td>
<td><span data-ttu-id="ad954-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ad954-264">-1,000.00</span></span></td>
<td><span data-ttu-id="ad954-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-266">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-266">0.00</span></span></td>
<td><span data-ttu-id="ad954-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ad954-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-269">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-270">5</span><span class="sxs-lookup"><span data-stu-id="ad954-270">5</span></span></td>
<td><span data-ttu-id="ad954-271">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="ad954-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="ad954-272">-1,008.00</span></span></td>
<td><span data-ttu-id="ad954-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="ad954-273">1,008.00</span></span></td>
<td><span data-ttu-id="ad954-274">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-275">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-276">6</span><span class="sxs-lookup"><span data-stu-id="ad954-276">6</span></span></td>
<td><span data-ttu-id="ad954-277">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="ad954-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-278">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="ad954-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="ad954-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-281">7</span><span class="sxs-lookup"><span data-stu-id="ad954-281">7</span></span></td>
<td><span data-ttu-id="ad954-282">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="ad954-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-283">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="ad954-284">-22,794.00</span></span></td>
<td><span data-ttu-id="ad954-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-285">1,000.00</span></span></td>
<td><span data-ttu-id="ad954-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="ad954-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="ad954-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-288">8</span><span class="sxs-lookup"><span data-stu-id="ad954-288">8</span></span></td>
<td><span data-ttu-id="ad954-289">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="ad954-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-290">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-291">94.97</span><span class="sxs-lookup"><span data-stu-id="ad954-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-292">94.97</span><span class="sxs-lookup"><span data-stu-id="ad954-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-293">9</span><span class="sxs-lookup"><span data-stu-id="ad954-293">9</span></span></td>
<td><span data-ttu-id="ad954-294">Contant</span><span class="sxs-lookup"><span data-stu-id="ad954-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="ad954-295">-1,008.00</span></span></td>
<td><span data-ttu-id="ad954-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="ad954-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="ad954-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-298">10</span><span class="sxs-lookup"><span data-stu-id="ad954-298">10</span></span></td>
<td><span data-ttu-id="ad954-299">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="ad954-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-300">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-301">949.75</span><span class="sxs-lookup"><span data-stu-id="ad954-301">949.75</span></span></td>
<td><span data-ttu-id="ad954-302">949.75</span><span class="sxs-lookup"><span data-stu-id="ad954-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-303">11</span><span class="sxs-lookup"><span data-stu-id="ad954-303">11</span></span></td>
<td><span data-ttu-id="ad954-304">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-305">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="ad954-306">-949.75</span></span></td>
<td><span data-ttu-id="ad954-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="ad954-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ad954-308">Zoals in de bovenstaande tabel wordt aangegeven, moeten drie boeken worden gerapporteerd onder zowel wettelijke als IFRS-rapportage.</span><span class="sxs-lookup"><span data-stu-id="ad954-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="ad954-309">In het wettelijke boek wordt de leasebetaling vastgelegd volgens de regels voor cash-basis-boekhouding onder de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="ad954-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="ad954-310">Het wettelijke terugboekingsboek keert de wettelijke journaalposten om.</span><span class="sxs-lookup"><span data-stu-id="ad954-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="ad954-311">In het IFRS 16 boek worden de journaalposten gemaakt die zijn vereist volgens IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="ad954-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="ad954-312">U moet een lease slechts één keer invoeren.</span><span class="sxs-lookup"><span data-stu-id="ad954-312">You must enter a lease only one time.</span></span> <span data-ttu-id="ad954-313">Vervolgens kunt u de pagina **Boeken** openen om alle boeken te zien die aan de lease zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ad954-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="ad954-314">Wanneer u de boeken maakt, moeten alle drie aan dezelfde leaserecord zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ad954-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="ad954-315">De eerste journaalpost registreert de leasekosten uit hoofde van het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="ad954-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="ad954-316">U kunt de betalingen maken in een batch of door het betalingsschema te selecteren in het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="ad954-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="ad954-317">Voor dit voorbeeld wordt de volgende journaalpost gemaakt voor het wettelijk boek van het betalingsschema.</span><span class="sxs-lookup"><span data-stu-id="ad954-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="ad954-318">Leasebetaling – 31-1-2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="ad954-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="ad954-319">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="ad954-319">Account type</span></span> | <span data-ttu-id="ad954-320">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-320">Account number</span></span> | <span data-ttu-id="ad954-321">Laag</span><span class="sxs-lookup"><span data-stu-id="ad954-321">Layer</span></span>   | <span data-ttu-id="ad954-322">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-322">Account description</span></span> | <span data-ttu-id="ad954-323">Debet</span><span class="sxs-lookup"><span data-stu-id="ad954-323">Debit</span></span>    | <span data-ttu-id="ad954-324">Krediet</span><span class="sxs-lookup"><span data-stu-id="ad954-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="ad954-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-325">Ledger</span></span>       | <span data-ttu-id="ad954-326">1</span><span class="sxs-lookup"><span data-stu-id="ad954-326">1</span></span>              | <span data-ttu-id="ad954-327">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-327">Current</span></span> | <span data-ttu-id="ad954-328">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="ad954-328">Lease expense</span></span>       | <span data-ttu-id="ad954-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-329">1,000.00</span></span> |          |
| <span data-ttu-id="ad954-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-330">Ledger</span></span>       | <span data-ttu-id="ad954-331">4</span><span class="sxs-lookup"><span data-stu-id="ad954-331">4</span></span>              | <span data-ttu-id="ad954-332">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-332">Current</span></span> | <span data-ttu-id="ad954-333">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="ad954-333">Clearing account</span></span>    |          | <span data-ttu-id="ad954-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-334">1,000.00</span></span> |

<span data-ttu-id="ad954-335">Een medewerker leveranciers gebruikt de standaard Dynamics 365-functionaliteit om een factuur te maken die moet worden betaald voor de lease buiten Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="ad954-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="ad954-336">In plaats van **Leasekosten** te selecteren als de debetrekening, selecteert de medewerker leveranciers een vereffeningsrekening om de volgende post te genereren.</span><span class="sxs-lookup"><span data-stu-id="ad954-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="ad954-337">Leveranciersproces – 31-1-2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="ad954-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="ad954-338">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="ad954-338">Account type</span></span> | <span data-ttu-id="ad954-339">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-339">Account number</span></span> | <span data-ttu-id="ad954-340">Laag</span><span class="sxs-lookup"><span data-stu-id="ad954-340">Layer</span></span>   | <span data-ttu-id="ad954-341">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-341">Account description</span></span> | <span data-ttu-id="ad954-342">Debet</span><span class="sxs-lookup"><span data-stu-id="ad954-342">Debit</span></span>    | <span data-ttu-id="ad954-343">Krediet</span><span class="sxs-lookup"><span data-stu-id="ad954-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="ad954-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-344">Ledger</span></span>       | <span data-ttu-id="ad954-345">4</span><span class="sxs-lookup"><span data-stu-id="ad954-345">4</span></span>              | <span data-ttu-id="ad954-346">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-346">Current</span></span> | <span data-ttu-id="ad954-347">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="ad954-347">Clearing account</span></span>    | <span data-ttu-id="ad954-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-348">1,000.00</span></span> |          |
| <span data-ttu-id="ad954-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-349">Ledger</span></span>       | <span data-ttu-id="ad954-350">2</span><span class="sxs-lookup"><span data-stu-id="ad954-350">2</span></span>              | <span data-ttu-id="ad954-351">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-351">Current</span></span> | <span data-ttu-id="ad954-352">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="ad954-352">Bank fee</span></span>            | <span data-ttu-id="ad954-353">3.00</span><span class="sxs-lookup"><span data-stu-id="ad954-353">3.00</span></span>     |          |
| <span data-ttu-id="ad954-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-354">Ledger</span></span>       | <span data-ttu-id="ad954-355">3</span><span class="sxs-lookup"><span data-stu-id="ad954-355">3</span></span>              | <span data-ttu-id="ad954-356">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-356">Current</span></span> | <span data-ttu-id="ad954-357">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="ad954-357">VAT expense</span></span>         | <span data-ttu-id="ad954-358">5.00</span><span class="sxs-lookup"><span data-stu-id="ad954-358">5.00</span></span>     |          |
| <span data-ttu-id="ad954-359">Leverancier</span><span class="sxs-lookup"><span data-stu-id="ad954-359">Vendor</span></span>       | <span data-ttu-id="ad954-360">5</span><span class="sxs-lookup"><span data-stu-id="ad954-360">5</span></span>              | <span data-ttu-id="ad954-361">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-361">Current</span></span> | <span data-ttu-id="ad954-362">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="ad954-362">Accounts payable</span></span>    |          | <span data-ttu-id="ad954-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="ad954-363">1,008.00</span></span> |

<span data-ttu-id="ad954-364">Wanneer het overzicht naar de leverancier wordt verzonden, volgt u het normale betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="ad954-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="ad954-365">Tijdens dit proces wordt de volgende journaalpost gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="ad954-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="ad954-366">Contante betaling – 31-1-2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="ad954-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="ad954-367">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="ad954-367">Account type</span></span> | <span data-ttu-id="ad954-368">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-368">Account number</span></span> | <span data-ttu-id="ad954-369">Laag</span><span class="sxs-lookup"><span data-stu-id="ad954-369">Layer</span></span>   | <span data-ttu-id="ad954-370">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-370">Account description</span></span> | <span data-ttu-id="ad954-371">Debet</span><span class="sxs-lookup"><span data-stu-id="ad954-371">Debit</span></span>    | <span data-ttu-id="ad954-372">Krediet</span><span class="sxs-lookup"><span data-stu-id="ad954-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="ad954-373">Leverancier</span><span class="sxs-lookup"><span data-stu-id="ad954-373">Vendor</span></span>       | <span data-ttu-id="ad954-374">5</span><span class="sxs-lookup"><span data-stu-id="ad954-374">5</span></span>              | <span data-ttu-id="ad954-375">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-375">Current</span></span> | <span data-ttu-id="ad954-376">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="ad954-376">Accounts Payable</span></span>    | <span data-ttu-id="ad954-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="ad954-377">1,008.00</span></span> |          |
| <span data-ttu-id="ad954-378">Bank</span><span class="sxs-lookup"><span data-stu-id="ad954-378">Bank</span></span>         | <span data-ttu-id="ad954-379">9</span><span class="sxs-lookup"><span data-stu-id="ad954-379">9</span></span>              | <span data-ttu-id="ad954-380">Huidig</span><span class="sxs-lookup"><span data-stu-id="ad954-380">Current</span></span> | <span data-ttu-id="ad954-381">Contant</span><span class="sxs-lookup"><span data-stu-id="ad954-381">Cash</span></span>                |          | <span data-ttu-id="ad954-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="ad954-382">1,008.00</span></span> |

<span data-ttu-id="ad954-383">U hebt op dit punt volledig verantwoord voor deze lease onder wettelijke rapportagevereisten en kunt een proefbalans genereren met behulp van de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="ad954-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="ad954-384">Het systeem geeft een proefbalans weer met de volgende cijfers.</span><span class="sxs-lookup"><span data-stu-id="ad954-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="ad954-385">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="ad954-386">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="ad954-387">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="ad954-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="ad954-388">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="ad954-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ad954-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="ad954-389">JE-100</span></span></th>
<th><span data-ttu-id="ad954-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="ad954-390">JE-110</span></span></th>
<th><span data-ttu-id="ad954-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="ad954-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ad954-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="ad954-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="ad954-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ad954-395">1</span><span class="sxs-lookup"><span data-stu-id="ad954-395">1</span></span></td>
<td><span data-ttu-id="ad954-396">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="ad954-396">Lease expense</span></span></td>
<td><span data-ttu-id="ad954-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-399">2</span><span class="sxs-lookup"><span data-stu-id="ad954-399">2</span></span></td>
<td><span data-ttu-id="ad954-400">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="ad954-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-401">3.00</span><span class="sxs-lookup"><span data-stu-id="ad954-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-402">3.00</span><span class="sxs-lookup"><span data-stu-id="ad954-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-403">3</span><span class="sxs-lookup"><span data-stu-id="ad954-403">3</span></span></td>
<td><span data-ttu-id="ad954-404">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="ad954-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-405">5.00</span><span class="sxs-lookup"><span data-stu-id="ad954-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-406">5.00</span><span class="sxs-lookup"><span data-stu-id="ad954-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-407">4</span><span class="sxs-lookup"><span data-stu-id="ad954-407">4</span></span></td>
<td><span data-ttu-id="ad954-408">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="ad954-408">Clearing account</span></span></td>
<td><span data-ttu-id="ad954-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ad954-409">-1,000.00</span></span></td>
<td><span data-ttu-id="ad954-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-411">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-412">5</span><span class="sxs-lookup"><span data-stu-id="ad954-412">5</span></span></td>
<td><span data-ttu-id="ad954-413">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="ad954-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="ad954-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="ad954-414">-1,008.00</span></span></td>
<td><span data-ttu-id="ad954-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="ad954-415">1,008.00</span></span></td>
<td><span data-ttu-id="ad954-416">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-417">6</span><span class="sxs-lookup"><span data-stu-id="ad954-417">6</span></span></td>
<td><span data-ttu-id="ad954-418">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="ad954-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-419">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-420">7</span><span class="sxs-lookup"><span data-stu-id="ad954-420">7</span></span></td>
<td><span data-ttu-id="ad954-421">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="ad954-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-422">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-423">8</span><span class="sxs-lookup"><span data-stu-id="ad954-423">8</span></span></td>
<td><span data-ttu-id="ad954-424">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="ad954-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-425">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-426">9</span><span class="sxs-lookup"><span data-stu-id="ad954-426">9</span></span></td>
<td><span data-ttu-id="ad954-427">Contant</span><span class="sxs-lookup"><span data-stu-id="ad954-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="ad954-428">-1,008.00</span></span></td>
<td><span data-ttu-id="ad954-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="ad954-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-430">10</span><span class="sxs-lookup"><span data-stu-id="ad954-430">10</span></span></td>
<td><span data-ttu-id="ad954-431">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="ad954-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-432">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ad954-433">11</span><span class="sxs-lookup"><span data-stu-id="ad954-433">11</span></span></td>
<td><span data-ttu-id="ad954-434">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="ad954-435">0,00</span><span class="sxs-lookup"><span data-stu-id="ad954-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ad954-436">Als u de IFRS 16 cijfers wilt gebruiken om dezelfde proefbalans uit te voeren, moeten de wettelijke boekhoudingsjournaalposten worden teruggeboekt en moeten de IFRS 16-journaalposten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="ad954-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="ad954-437">Voor het omkeren van de wettelijke journaalposten bevat dit voorbeeld een wettelijk terugboekingsboek met dezelfde instellingen als het wettelijke boek, maar een tegengesteld boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="ad954-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="ad954-438">Het wettelijke boek heeft bijvoorbeeld een leasekostenrekening *gedebiteerd*, maar het terugboekingsboek *crediteert* deze rekening.</span><span class="sxs-lookup"><span data-stu-id="ad954-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="ad954-439">Deze relaties worden eenvoudig gedefinieerd in de boekingsrekeningen Activa leasen op de pagina **Parameters voor activa leasing** (**Activa leasen \> Instellen \> Parameters voor activa leasing**).</span><span class="sxs-lookup"><span data-stu-id="ad954-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="ad954-440">Wanneer hetzelfde proces dat is gebruikt voor het wettelijke boek, wordt gebruikt voor het terugboekingsboek, wordt de volgende journaalpost geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="ad954-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="ad954-441">Het verschil is dat het terugboekingsboek de stornoposten uit het wettelijke boek boekt.</span><span class="sxs-lookup"><span data-stu-id="ad954-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="ad954-442">De stornoposten worden ook in de aangepaste laag aangebracht.</span><span class="sxs-lookup"><span data-stu-id="ad954-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="ad954-443">Wanneer een proefbalans wordt uitgevoerd op de huidige laag, worden de stornojournaalposten niet opgenomen.</span><span class="sxs-lookup"><span data-stu-id="ad954-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="ad954-444">Leasebetaling – 31-1-2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="ad954-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="ad954-445">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="ad954-445">Account type</span></span> | <span data-ttu-id="ad954-446">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-446">Account number</span></span> | <span data-ttu-id="ad954-447">Laag</span><span class="sxs-lookup"><span data-stu-id="ad954-447">Layer</span></span>  | <span data-ttu-id="ad954-448">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-448">Account description</span></span> | <span data-ttu-id="ad954-449">Debet</span><span class="sxs-lookup"><span data-stu-id="ad954-449">Debit</span></span>    | <span data-ttu-id="ad954-450">Krediet</span><span class="sxs-lookup"><span data-stu-id="ad954-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="ad954-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-451">Ledger</span></span>       | <span data-ttu-id="ad954-452">4</span><span class="sxs-lookup"><span data-stu-id="ad954-452">4</span></span>              | <span data-ttu-id="ad954-453">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-453">Custom</span></span> | <span data-ttu-id="ad954-454">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="ad954-454">Clearing account</span></span>    | <span data-ttu-id="ad954-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-455">1,000.00</span></span> |          |
| <span data-ttu-id="ad954-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-456">Ledger</span></span>       | <span data-ttu-id="ad954-457">1</span><span class="sxs-lookup"><span data-stu-id="ad954-457">1</span></span>              | <span data-ttu-id="ad954-458">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-458">Custom</span></span> | <span data-ttu-id="ad954-459">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="ad954-459">Lease expense</span></span>       |          | <span data-ttu-id="ad954-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-460">1,000.00</span></span> |

<span data-ttu-id="ad954-461">Nu u de wettelijk journaalposten hebt verwijderd, worden alle journaalposten geboekt die IFRS 16 vereist in het IFRS 16 boek.</span><span class="sxs-lookup"><span data-stu-id="ad954-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="ad954-462">Deze posten omvatten de eerste toerekening van het RoU activum en de verplichting, en de record van rente en afschrijving.</span><span class="sxs-lookup"><span data-stu-id="ad954-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="ad954-463">Initiële toerekening - 1-1-2020 - JE 140</span><span class="sxs-lookup"><span data-stu-id="ad954-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="ad954-464">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="ad954-464">Account type</span></span> | <span data-ttu-id="ad954-465">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-465">Account number</span></span> | <span data-ttu-id="ad954-466">Laag</span><span class="sxs-lookup"><span data-stu-id="ad954-466">Layer</span></span>  | <span data-ttu-id="ad954-467">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-467">Account description</span></span>      | <span data-ttu-id="ad954-468">Debet</span><span class="sxs-lookup"><span data-stu-id="ad954-468">Debit</span></span>     | <span data-ttu-id="ad954-469">Krediet</span><span class="sxs-lookup"><span data-stu-id="ad954-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="ad954-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-470">Ledger</span></span>       | <span data-ttu-id="ad954-471">6</span><span class="sxs-lookup"><span data-stu-id="ad954-471">6</span></span>              | <span data-ttu-id="ad954-472">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-472">Custom</span></span> | <span data-ttu-id="ad954-473">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="ad954-473">ROU Asset</span></span>                | <span data-ttu-id="ad954-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="ad954-474">22,793.90</span></span> |           |
| <span data-ttu-id="ad954-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-475">Ledger</span></span>       | <span data-ttu-id="ad954-476">7</span><span class="sxs-lookup"><span data-stu-id="ad954-476">7</span></span>              | <span data-ttu-id="ad954-477">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-477">Custom</span></span> | <span data-ttu-id="ad954-478">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="ad954-478">Finance lease obligation</span></span> |           | <span data-ttu-id="ad954-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="ad954-479">22,793.90</span></span> |

<span data-ttu-id="ad954-480">De leasebetaling wordt geboekt zoals de andere leasebetalingen.</span><span class="sxs-lookup"><span data-stu-id="ad954-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="ad954-481">De reden voor het gebruik van de vereffeningsrekening is ervoor te zorgen dat contant geld slechts één keer wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="ad954-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="ad954-482">Leasebetaling – 31-1-2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="ad954-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="ad954-483">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="ad954-483">Account type</span></span> | <span data-ttu-id="ad954-484">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-484">Account number</span></span> | <span data-ttu-id="ad954-485">Laag</span><span class="sxs-lookup"><span data-stu-id="ad954-485">Layer</span></span>  | <span data-ttu-id="ad954-486">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-486">Account description</span></span>      | <span data-ttu-id="ad954-487">Debet</span><span class="sxs-lookup"><span data-stu-id="ad954-487">Debit</span></span>    | <span data-ttu-id="ad954-488">Krediet</span><span class="sxs-lookup"><span data-stu-id="ad954-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="ad954-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-489">Ledger</span></span>       | <span data-ttu-id="ad954-490">7</span><span class="sxs-lookup"><span data-stu-id="ad954-490">7</span></span>              | <span data-ttu-id="ad954-491">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-491">Custom</span></span> | <span data-ttu-id="ad954-492">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="ad954-492">Finance lease obligation</span></span> | <span data-ttu-id="ad954-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-493">1,000.00</span></span> |          |
| <span data-ttu-id="ad954-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-494">Ledger</span></span>       | <span data-ttu-id="ad954-495">4</span><span class="sxs-lookup"><span data-stu-id="ad954-495">4</span></span>              | <span data-ttu-id="ad954-496">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-496">Custom</span></span> | <span data-ttu-id="ad954-497">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="ad954-497">Clearing account</span></span>         |          | <span data-ttu-id="ad954-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ad954-498">1,000.00</span></span> |

<span data-ttu-id="ad954-499">De journaalpost voor rentelasten wordt gegenereerd op basis van het afschrijvingsschema voor verplichtingen.</span><span class="sxs-lookup"><span data-stu-id="ad954-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="ad954-500">Rente-uitgaven - 31-1-2020 - JE 160</span><span class="sxs-lookup"><span data-stu-id="ad954-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="ad954-501">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="ad954-501">Account type</span></span> | <span data-ttu-id="ad954-502">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-502">Account number</span></span> | <span data-ttu-id="ad954-503">Laag</span><span class="sxs-lookup"><span data-stu-id="ad954-503">Layer</span></span>  | <span data-ttu-id="ad954-504">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-504">Account description</span></span>      | <span data-ttu-id="ad954-505">Debet</span><span class="sxs-lookup"><span data-stu-id="ad954-505">Debit</span></span> | <span data-ttu-id="ad954-506">Krediet</span><span class="sxs-lookup"><span data-stu-id="ad954-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="ad954-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-507">Ledger</span></span>       | <span data-ttu-id="ad954-508">8</span><span class="sxs-lookup"><span data-stu-id="ad954-508">8</span></span>              | <span data-ttu-id="ad954-509">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-509">Custom</span></span> | <span data-ttu-id="ad954-510">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="ad954-510">Interest expense</span></span>         | <span data-ttu-id="ad954-511">94.97</span><span class="sxs-lookup"><span data-stu-id="ad954-511">94.97</span></span> |        |
| <span data-ttu-id="ad954-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-512">Ledger</span></span>       | <span data-ttu-id="ad954-513">7</span><span class="sxs-lookup"><span data-stu-id="ad954-513">7</span></span>              | <span data-ttu-id="ad954-514">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-514">Custom</span></span> | <span data-ttu-id="ad954-515">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="ad954-515">Finance lease obligation</span></span> |       | <span data-ttu-id="ad954-516">94.97</span><span class="sxs-lookup"><span data-stu-id="ad954-516">94.97</span></span>  |

<span data-ttu-id="ad954-517">De journaalpost voor afschrijvingskosten wordt gegenereerd op basis van het schema activumafschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="ad954-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="ad954-518">Afschrijvingskosten - 31-1-2020 - JE 170</span><span class="sxs-lookup"><span data-stu-id="ad954-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="ad954-519">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="ad954-519">Account type</span></span> | <span data-ttu-id="ad954-520">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-520">Account number</span></span> | <span data-ttu-id="ad954-521">Laag</span><span class="sxs-lookup"><span data-stu-id="ad954-521">Layer</span></span>  | <span data-ttu-id="ad954-522">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-522">Account description</span></span>      | <span data-ttu-id="ad954-523">Debet</span><span class="sxs-lookup"><span data-stu-id="ad954-523">Debit</span></span>  | <span data-ttu-id="ad954-524">Krediet</span><span class="sxs-lookup"><span data-stu-id="ad954-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="ad954-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-525">Ledger</span></span>       | <span data-ttu-id="ad954-526">10</span><span class="sxs-lookup"><span data-stu-id="ad954-526">10</span></span>             | <span data-ttu-id="ad954-527">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-527">Custom</span></span> | <span data-ttu-id="ad954-528">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="ad954-528">Depreciation expense</span></span>     | <span data-ttu-id="ad954-529">949.75</span><span class="sxs-lookup"><span data-stu-id="ad954-529">949.75</span></span> |        |
| <span data-ttu-id="ad954-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="ad954-530">Ledger</span></span>       | <span data-ttu-id="ad954-531">11</span><span class="sxs-lookup"><span data-stu-id="ad954-531">11</span></span>             | <span data-ttu-id="ad954-532">Aangepast</span><span class="sxs-lookup"><span data-stu-id="ad954-532">Custom</span></span> | <span data-ttu-id="ad954-533">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="ad954-534">949.75</span><span class="sxs-lookup"><span data-stu-id="ad954-534">949.75</span></span> |

<span data-ttu-id="ad954-535">Nadat al deze journaalposten zijn gemaakt en geboekt, ziet u de volgende waarden voor "aangepaste laag 1".</span><span class="sxs-lookup"><span data-stu-id="ad954-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="ad954-536">De laatste kolom bevat de bankkosten, de kosten voor de toegevoegde waarde (btw) en de reductie van contant geld uit de vorige laag, maar bevat niet de journaalposten voor wettelijke rapportage.</span><span class="sxs-lookup"><span data-stu-id="ad954-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="ad954-537">Daarom bereikt u echte mogelijkheden voor dubbele rapportage.</span><span class="sxs-lookup"><span data-stu-id="ad954-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="ad954-538">Op dit punt hoeft het bedrijf alleen zijn proefbalans uit te voeren en de huidige laag en de aangepaste laag combineren om een IFRS-proefbalans te maken.</span><span class="sxs-lookup"><span data-stu-id="ad954-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="ad954-539">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="ad954-539">Account No</span></span> | <span data-ttu-id="ad954-540">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-540">Description</span></span>              | <span data-ttu-id="ad954-541">Wettelijk boek\-Huidige laag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="ad954-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="ad954-542">Wettelijk boek\-Huidige laag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="ad954-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="ad954-543">Wettelijk boek\-Huidige laag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="ad954-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="ad954-544">Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="ad954-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="ad954-545">Terugboekingsboek\-Aangepaste laag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="ad954-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="ad954-546">IFRS 16-boek\-Aangepaste laag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="ad954-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="ad954-547">IFRS 16-boek\-Aangepaste laag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="ad954-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="ad954-548">IFRS 16-boek\-Aangepaste laag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="ad954-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="ad954-549">IFRS 16-boek\-Aangepaste laag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="ad954-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="ad954-550">Aangepaste laag \+ Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="ad954-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="ad954-551">1</span><span class="sxs-lookup"><span data-stu-id="ad954-551">1</span></span>          | <span data-ttu-id="ad954-552">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="ad954-552">Lease expense</span></span>            | <span data-ttu-id="ad954-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="ad954-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-554">1,000\.00</span></span>               |   | <span data-ttu-id="ad954-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="ad954-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="ad954-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-556">0\.00</span></span>                                   |
| <span data-ttu-id="ad954-557">2</span><span class="sxs-lookup"><span data-stu-id="ad954-557">2</span></span>          | <span data-ttu-id="ad954-558">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="ad954-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="ad954-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="ad954-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="ad954-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-561">3\.00</span></span>                                   |
| <span data-ttu-id="ad954-562">3</span><span class="sxs-lookup"><span data-stu-id="ad954-562">3</span></span>          | <span data-ttu-id="ad954-563">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="ad954-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="ad954-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="ad954-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="ad954-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-566">5\.00</span></span>                                   |
| <span data-ttu-id="ad954-567">4</span><span class="sxs-lookup"><span data-stu-id="ad954-567">4</span></span>          | <span data-ttu-id="ad954-568">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="ad954-568">Clearing account</span></span>         | <span data-ttu-id="ad954-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="ad954-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="ad954-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-571">0\.00</span></span>                   |   | <span data-ttu-id="ad954-572">1.000</span><span class="sxs-lookup"><span data-stu-id="ad954-572">1,000</span></span>                                           |                                                | <span data-ttu-id="ad954-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="ad954-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="ad954-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-574">0\.00</span></span>                                   |
| <span data-ttu-id="ad954-575">5</span><span class="sxs-lookup"><span data-stu-id="ad954-575">5</span></span>          | <span data-ttu-id="ad954-576">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="ad954-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="ad954-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="ad954-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-578">1,008\.00</span></span>                                         | <span data-ttu-id="ad954-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="ad954-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-580">0\.00</span></span>                                   |
| <span data-ttu-id="ad954-581">6</span><span class="sxs-lookup"><span data-stu-id="ad954-581">6</span></span>          | <span data-ttu-id="ad954-582">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="ad954-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="ad954-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="ad954-584">22,794</span><span class="sxs-lookup"><span data-stu-id="ad954-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="ad954-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="ad954-585">22,793\.90</span></span>                              |
| <span data-ttu-id="ad954-586">7</span><span class="sxs-lookup"><span data-stu-id="ad954-586">7</span></span>          | <span data-ttu-id="ad954-587">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="ad954-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="ad954-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="ad954-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="ad954-589">\-22,794</span></span>                                       | <span data-ttu-id="ad954-590">1.000</span><span class="sxs-lookup"><span data-stu-id="ad954-590">1,000</span></span>                                          | <span data-ttu-id="ad954-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="ad954-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="ad954-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="ad954-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="ad954-593">8</span><span class="sxs-lookup"><span data-stu-id="ad954-593">8</span></span>          | <span data-ttu-id="ad954-594">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="ad954-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="ad954-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="ad954-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="ad954-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="ad954-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="ad954-597">94\.97</span></span>                                  |
| <span data-ttu-id="ad954-598">9</span><span class="sxs-lookup"><span data-stu-id="ad954-598">9</span></span>          | <span data-ttu-id="ad954-599">Contant</span><span class="sxs-lookup"><span data-stu-id="ad954-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="ad954-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="ad954-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="ad954-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="ad954-603">10</span><span class="sxs-lookup"><span data-stu-id="ad954-603">10</span></span>         | <span data-ttu-id="ad954-604">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="ad954-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="ad954-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="ad954-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="ad954-606">949\.75</span></span>                                        | <span data-ttu-id="ad954-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="ad954-607">949\.75</span></span>                                 |
| <span data-ttu-id="ad954-608">11</span><span class="sxs-lookup"><span data-stu-id="ad954-608">11</span></span>         | <span data-ttu-id="ad954-609">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="ad954-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="ad954-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="ad954-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="ad954-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="ad954-611">\-949\.75</span></span>                                      | <span data-ttu-id="ad954-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="ad954-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
