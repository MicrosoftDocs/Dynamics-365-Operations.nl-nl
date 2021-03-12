---
title: Dubbele rapportage
description: In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003176"
---
# <a name="dual-reporting"></a><span data-ttu-id="805ab-103">Dubbele rapportage</span><span class="sxs-lookup"><span data-stu-id="805ab-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="805ab-104">In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="805ab-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="805ab-105">Vertrouwdheid met boekingslagen in Microsoft Dynamics 365 Finance is vereist en maakt het voorbeeld gemakkelijker te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="805ab-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="805ab-106">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="805ab-106">Example</span></span>

<span data-ttu-id="805ab-107">In het volgende voorbeeld wordt een lease verantwoord onder de Italiaanse wettelijke rapportering door middel van de cash-basis-methode en de IFRS-rapportagemethoden.</span><span class="sxs-lookup"><span data-stu-id="805ab-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="805ab-108">Het bedrijf moet drie boeken maken om te verantwoorden voor zowel de Italiaanse wettelijke vereisten als de IFRS 16-vereisten.</span><span class="sxs-lookup"><span data-stu-id="805ab-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="805ab-109">Eén boek is vereist voor IFRS 16, één boek is vereist voor wettelijke vereisten en één boek is vereist om de wettelijke boekingen automatisch terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="805ab-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="805ab-110">De boeken worden ingesteld, zoals in de volgende tabellen wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="805ab-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="805ab-111">**IFRS 16-boek**</span><span class="sxs-lookup"><span data-stu-id="805ab-111">**IFRS 16 book**</span></span>

<span data-ttu-id="805ab-112">Het IFRS 16 boek is zo ingesteld dat het voldoet aan de IFRS 16-boekhoudnorm.</span><span class="sxs-lookup"><span data-stu-id="805ab-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="805ab-113">Alle posten die in dit boek worden geboekt, worden naar een aangepaste laag geboekt.</span><span class="sxs-lookup"><span data-stu-id="805ab-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="805ab-114">Naam</span><span class="sxs-lookup"><span data-stu-id="805ab-114">Name</span></span>                                    | <span data-ttu-id="805ab-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="805ab-116">Boektype</span><span class="sxs-lookup"><span data-stu-id="805ab-116">Book type</span></span>                               | <span data-ttu-id="805ab-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="805ab-117">IFRS 16</span></span>        |
| <span data-ttu-id="805ab-118">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-118">Book description</span></span>                        | <span data-ttu-id="805ab-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="805ab-119">IFRS 16</span></span>        |
| <span data-ttu-id="805ab-120">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="805ab-120">Posting Layer</span></span>                           | <span data-ttu-id="805ab-121">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="805ab-121">Custom layer 1</span></span> |
| <span data-ttu-id="805ab-122">Leasetype</span><span class="sxs-lookup"><span data-stu-id="805ab-122">Lease Type</span></span>                              | <span data-ttu-id="805ab-123">Finance</span><span class="sxs-lookup"><span data-stu-id="805ab-123">Finance</span></span>        |
| <span data-ttu-id="805ab-124">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="805ab-124">Accounting Framework</span></span>                    | <span data-ttu-id="805ab-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="805ab-125">IFRS 16</span></span>        |
| <span data-ttu-id="805ab-126">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="805ab-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="805ab-127">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-127">0.00</span></span>           |
| <span data-ttu-id="805ab-128">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="805ab-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="805ab-129">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-129">0.00</span></span>           |
| <span data-ttu-id="805ab-130">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="805ab-130">Short-term threshold</span></span>                    | <span data-ttu-id="805ab-131">12</span><span class="sxs-lookup"><span data-stu-id="805ab-131">12</span></span>             |
| <span data-ttu-id="805ab-132">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="805ab-132">Low Value Threshold</span></span>                     | <span data-ttu-id="805ab-133">5.000,00</span><span class="sxs-lookup"><span data-stu-id="805ab-133">5,000.00</span></span>       |
| <span data-ttu-id="805ab-134">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="805ab-134">Pay to Vendor</span></span>                           | <span data-ttu-id="805ab-135">No</span><span class="sxs-lookup"><span data-stu-id="805ab-135">No</span></span>             |

<span data-ttu-id="805ab-136">**Wettelijk boek**</span><span class="sxs-lookup"><span data-stu-id="805ab-136">**Statutory book**</span></span>

<span data-ttu-id="805ab-137">Het wettelijke boek is een cash-basis-boek waar het bedrijf de leasekosten zal verantwoorden als het bedrag aan geld dat maandelijks wordt betaald voor huur.</span><span class="sxs-lookup"><span data-stu-id="805ab-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="805ab-138">Dit boek produceert geen RoU-activum of leaseverplichtingen.</span><span class="sxs-lookup"><span data-stu-id="805ab-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="805ab-139">Naam</span><span class="sxs-lookup"><span data-stu-id="805ab-139">Name</span></span>                                    | <span data-ttu-id="805ab-140">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="805ab-141">Boektype</span><span class="sxs-lookup"><span data-stu-id="805ab-141">Book type</span></span>                               | <span data-ttu-id="805ab-142">Wettelijk</span><span class="sxs-lookup"><span data-stu-id="805ab-142">Statutory</span></span>   |
| <span data-ttu-id="805ab-143">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-143">Book description</span></span>                        | <span data-ttu-id="805ab-144">Lokale GAAP</span><span class="sxs-lookup"><span data-stu-id="805ab-144">Local GAAP</span></span>  |
| <span data-ttu-id="805ab-145">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="805ab-145">Posting Layer</span></span>                           | <span data-ttu-id="805ab-146">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-146">Current</span></span>     |
| <span data-ttu-id="805ab-147">Leasetype</span><span class="sxs-lookup"><span data-stu-id="805ab-147">Lease Type</span></span>                              | <span data-ttu-id="805ab-148">Automatisch</span><span class="sxs-lookup"><span data-stu-id="805ab-148">Automatic</span></span>   |
| <span data-ttu-id="805ab-149">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="805ab-149">Accounting Framework</span></span>                    | <span data-ttu-id="805ab-150">Contante basis</span><span class="sxs-lookup"><span data-stu-id="805ab-150">Cash basis</span></span>  |
| <span data-ttu-id="805ab-151">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="805ab-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="805ab-152">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-152">0.00</span></span>        |
| <span data-ttu-id="805ab-153">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="805ab-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="805ab-154">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-154">0.00</span></span>        |
| <span data-ttu-id="805ab-155">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="805ab-155">Short-term threshold</span></span>                    | <span data-ttu-id="805ab-156">0</span><span class="sxs-lookup"><span data-stu-id="805ab-156">0</span></span>           |
| <span data-ttu-id="805ab-157">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="805ab-157">Low Value Threshold</span></span>                     | <span data-ttu-id="805ab-158">0</span><span class="sxs-lookup"><span data-stu-id="805ab-158">0</span></span>           |
| <span data-ttu-id="805ab-159">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="805ab-159">Pay to Vendor</span></span>                           | <span data-ttu-id="805ab-160">No</span><span class="sxs-lookup"><span data-stu-id="805ab-160">No</span></span>          |

<span data-ttu-id="805ab-161">**Wettelijk terugboekingsboek**</span><span class="sxs-lookup"><span data-stu-id="805ab-161">**Statutory reversal book**</span></span>

<span data-ttu-id="805ab-162">Het wettelijke terugboekingsboek wordt op dezelfde manier ingesteld als het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="805ab-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="805ab-163">Naam</span><span class="sxs-lookup"><span data-stu-id="805ab-163">Name</span></span>                                    | <span data-ttu-id="805ab-164">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="805ab-165">Boektype</span><span class="sxs-lookup"><span data-stu-id="805ab-165">Book type</span></span>                               | <span data-ttu-id="805ab-166">Wettelijk - terugboeking</span><span class="sxs-lookup"><span data-stu-id="805ab-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="805ab-167">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-167">Book description</span></span>                        | <span data-ttu-id="805ab-168">Boek om wettelijk boek terug te boeken</span><span class="sxs-lookup"><span data-stu-id="805ab-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="805ab-169">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="805ab-169">Posting Layer</span></span>                           | <span data-ttu-id="805ab-170">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="805ab-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="805ab-171">Leasetype</span><span class="sxs-lookup"><span data-stu-id="805ab-171">Lease Type</span></span>                              | <span data-ttu-id="805ab-172">Automatisch</span><span class="sxs-lookup"><span data-stu-id="805ab-172">Automatic</span></span>                      |
| <span data-ttu-id="805ab-173">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="805ab-173">Accounting Framework</span></span>                    | <span data-ttu-id="805ab-174">Contante basis</span><span class="sxs-lookup"><span data-stu-id="805ab-174">Cash basis</span></span>                     |
| <span data-ttu-id="805ab-175">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="805ab-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="805ab-176">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-176">0.00</span></span>                           |
| <span data-ttu-id="805ab-177">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="805ab-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="805ab-178">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-178">0.00</span></span>                           |
| <span data-ttu-id="805ab-179">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="805ab-179">Short-term threshold</span></span>                    | <span data-ttu-id="805ab-180">0</span><span class="sxs-lookup"><span data-stu-id="805ab-180">0</span></span>                              |
| <span data-ttu-id="805ab-181">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="805ab-181">Low Value Threshold</span></span>                     | <span data-ttu-id="805ab-182">0</span><span class="sxs-lookup"><span data-stu-id="805ab-182">0</span></span>                              |
| <span data-ttu-id="805ab-183">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="805ab-183">Pay to Vendor</span></span>                           | <span data-ttu-id="805ab-184">No</span><span class="sxs-lookup"><span data-stu-id="805ab-184">No</span></span>                             |

<span data-ttu-id="805ab-185">Voor dit voorbeeld is er een lease gemaakt met de volgende instellingen op de tabbladen **Algemeen** en **Betalingsschemaregels**.</span><span class="sxs-lookup"><span data-stu-id="805ab-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="805ab-186">**Tabblad Algemeen**</span><span class="sxs-lookup"><span data-stu-id="805ab-186">**General tab**</span></span>

| <span data-ttu-id="805ab-187">Veld</span><span class="sxs-lookup"><span data-stu-id="805ab-187">Field</span></span>                      | <span data-ttu-id="805ab-188">Waarde</span><span class="sxs-lookup"><span data-stu-id="805ab-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="805ab-189">Verhoogd leningtarief</span><span class="sxs-lookup"><span data-stu-id="805ab-189">Incremental borrowing rate</span></span> | <span data-ttu-id="805ab-190">5%</span><span class="sxs-lookup"><span data-stu-id="805ab-190">5%</span></span>               |
| <span data-ttu-id="805ab-191">Begindatum</span><span class="sxs-lookup"><span data-stu-id="805ab-191">Commencement date</span></span>          | <span data-ttu-id="805ab-192">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="805ab-192">1/1/2020</span></span>         |
| <span data-ttu-id="805ab-193">Leasegroep</span><span class="sxs-lookup"><span data-stu-id="805ab-193">Lease group</span></span>                | <span data-ttu-id="805ab-194">Gebouwen</span><span class="sxs-lookup"><span data-stu-id="805ab-194">Buildings</span></span>        |
| <span data-ttu-id="805ab-195">Leverancier</span><span class="sxs-lookup"><span data-stu-id="805ab-195">Vendor</span></span>                     | <span data-ttu-id="805ab-196">1001</span><span class="sxs-lookup"><span data-stu-id="805ab-196">1001</span></span>             |
| <span data-ttu-id="805ab-197">Reële waarde van het activum</span><span class="sxs-lookup"><span data-stu-id="805ab-197">Fair value of the asset</span></span>    | <span data-ttu-id="805ab-198">245,000</span><span class="sxs-lookup"><span data-stu-id="805ab-198">245,000</span></span>          |
| <span data-ttu-id="805ab-199">Economische levensduur activum</span><span class="sxs-lookup"><span data-stu-id="805ab-199">Asset useful life</span></span>          | <span data-ttu-id="805ab-200">120</span><span class="sxs-lookup"><span data-stu-id="805ab-200">120</span></span>              |
| <span data-ttu-id="805ab-201">Type annuïteit</span><span class="sxs-lookup"><span data-stu-id="805ab-201">Annuity type</span></span>               | <span data-ttu-id="805ab-202">Normale annuïteit</span><span class="sxs-lookup"><span data-stu-id="805ab-202">Ordinary annuity</span></span> |
| <span data-ttu-id="805ab-203">Samenstellingsinterval</span><span class="sxs-lookup"><span data-stu-id="805ab-203">Compounding interval</span></span>       | <span data-ttu-id="805ab-204">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="805ab-204">Monthly</span></span>          |

<span data-ttu-id="805ab-205">**Tabblad Regels van betalingsschema**</span><span class="sxs-lookup"><span data-stu-id="805ab-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="805ab-206">Veld</span><span class="sxs-lookup"><span data-stu-id="805ab-206">Field</span></span>             | <span data-ttu-id="805ab-207">Waarde</span><span class="sxs-lookup"><span data-stu-id="805ab-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="805ab-208">Begindatum</span><span class="sxs-lookup"><span data-stu-id="805ab-208">Start date</span></span>        | <span data-ttu-id="805ab-209">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="805ab-209">1/1/2020</span></span>   |
| <span data-ttu-id="805ab-210">Periode-interval</span><span class="sxs-lookup"><span data-stu-id="805ab-210">Period interval</span></span>   | <span data-ttu-id="805ab-211">Maanden</span><span class="sxs-lookup"><span data-stu-id="805ab-211">Months</span></span>     |
| <span data-ttu-id="805ab-212">Perioden</span><span class="sxs-lookup"><span data-stu-id="805ab-212">Periods</span></span>           | <span data-ttu-id="805ab-213">24</span><span class="sxs-lookup"><span data-stu-id="805ab-213">24</span></span>         |
| <span data-ttu-id="805ab-214">Einddatum</span><span class="sxs-lookup"><span data-stu-id="805ab-214">End date</span></span>          | <span data-ttu-id="805ab-215">31-12-2020</span><span class="sxs-lookup"><span data-stu-id="805ab-215">12/31/2020</span></span> |
| <span data-ttu-id="805ab-216">Betalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="805ab-216">Payment frequency</span></span> | <span data-ttu-id="805ab-217">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="805ab-217">Monthly</span></span>    |
| <span data-ttu-id="805ab-218">Betalingsbedrag</span><span class="sxs-lookup"><span data-stu-id="805ab-218">Payment amount</span></span>    | <span data-ttu-id="805ab-219">1.000</span><span class="sxs-lookup"><span data-stu-id="805ab-219">1,000</span></span>      |

<span data-ttu-id="805ab-220">Als u deze lease onder twee raamwerken wilt verantwoorden, gebruikt u een huidige boekingslaag en een aangepaste boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="805ab-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="805ab-221">In de volgende tabel ziet u een voorbeeld van elke journaalpost die voor elke rapportagestandaard de financiële waarde reëel moet representeren.</span><span class="sxs-lookup"><span data-stu-id="805ab-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="805ab-222">Hierna wordt een gedetailleerde omschrijving gegeven van elke journaalpost voor de eerste maand van de lease.</span><span class="sxs-lookup"><span data-stu-id="805ab-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="805ab-223">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="805ab-224">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="805ab-225">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="805ab-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="805ab-226">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="805ab-226">Current layer total</span></span></th>
<th><span data-ttu-id="805ab-227">Terugboekingsboek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="805ab-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="805ab-228">IFRS 16-boek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="805ab-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="805ab-229">Huidige laag + aangepaste laagtotaal</span><span class="sxs-lookup"><span data-stu-id="805ab-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="805ab-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="805ab-230">JE-100</span></span></th>
<th><span data-ttu-id="805ab-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="805ab-231">JE-110</span></span></th>
<th><span data-ttu-id="805ab-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="805ab-232">JE-120</span></span></th>
<th><span data-ttu-id="805ab-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="805ab-233">JE-130</span></span></th>
<th><span data-ttu-id="805ab-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="805ab-234">JE-140</span></span></th>
<th><span data-ttu-id="805ab-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="805ab-235">JE-150</span></span></th>
<th><span data-ttu-id="805ab-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="805ab-236">JE-160</span></span></th>
<th><span data-ttu-id="805ab-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="805ab-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="805ab-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="805ab-246">1</span><span class="sxs-lookup"><span data-stu-id="805ab-246">1</span></span></td>
<td><span data-ttu-id="805ab-247">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="805ab-247">Lease expense</span></span></td>
<td><span data-ttu-id="805ab-248">1.000,00</span><span class="sxs-lookup"><span data-stu-id="805ab-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-249">1,000.00</span></span></td>
<td><span data-ttu-id="805ab-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="805ab-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-251">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-252">2</span><span class="sxs-lookup"><span data-stu-id="805ab-252">2</span></span></td>
<td><span data-ttu-id="805ab-253">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="805ab-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-254">3,00</span><span class="sxs-lookup"><span data-stu-id="805ab-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-255">3.00</span><span class="sxs-lookup"><span data-stu-id="805ab-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-256">3.00</span><span class="sxs-lookup"><span data-stu-id="805ab-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-257">3</span><span class="sxs-lookup"><span data-stu-id="805ab-257">3</span></span></td>
<td><span data-ttu-id="805ab-258">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="805ab-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-259">5.00</span><span class="sxs-lookup"><span data-stu-id="805ab-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-260">5.00</span><span class="sxs-lookup"><span data-stu-id="805ab-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-261">5.00</span><span class="sxs-lookup"><span data-stu-id="805ab-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-262">4</span><span class="sxs-lookup"><span data-stu-id="805ab-262">4</span></span></td>
<td><span data-ttu-id="805ab-263">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="805ab-263">Clearing account</span></span></td>
<td><span data-ttu-id="805ab-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="805ab-264">-1,000.00</span></span></td>
<td><span data-ttu-id="805ab-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-266">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-266">0.00</span></span></td>
<td><span data-ttu-id="805ab-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="805ab-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-269">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-270">5</span><span class="sxs-lookup"><span data-stu-id="805ab-270">5</span></span></td>
<td><span data-ttu-id="805ab-271">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="805ab-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="805ab-272">-1,008.00</span></span></td>
<td><span data-ttu-id="805ab-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="805ab-273">1,008.00</span></span></td>
<td><span data-ttu-id="805ab-274">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-275">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-276">6</span><span class="sxs-lookup"><span data-stu-id="805ab-276">6</span></span></td>
<td><span data-ttu-id="805ab-277">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="805ab-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-278">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="805ab-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="805ab-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-281">7</span><span class="sxs-lookup"><span data-stu-id="805ab-281">7</span></span></td>
<td><span data-ttu-id="805ab-282">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="805ab-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-283">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="805ab-284">-22,794.00</span></span></td>
<td><span data-ttu-id="805ab-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-285">1,000.00</span></span></td>
<td><span data-ttu-id="805ab-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="805ab-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="805ab-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-288">8</span><span class="sxs-lookup"><span data-stu-id="805ab-288">8</span></span></td>
<td><span data-ttu-id="805ab-289">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="805ab-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-290">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-291">94.97</span><span class="sxs-lookup"><span data-stu-id="805ab-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-292">94.97</span><span class="sxs-lookup"><span data-stu-id="805ab-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-293">9</span><span class="sxs-lookup"><span data-stu-id="805ab-293">9</span></span></td>
<td><span data-ttu-id="805ab-294">Contant</span><span class="sxs-lookup"><span data-stu-id="805ab-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="805ab-295">-1,008.00</span></span></td>
<td><span data-ttu-id="805ab-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="805ab-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="805ab-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-298">10</span><span class="sxs-lookup"><span data-stu-id="805ab-298">10</span></span></td>
<td><span data-ttu-id="805ab-299">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="805ab-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-300">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-301">949.75</span><span class="sxs-lookup"><span data-stu-id="805ab-301">949.75</span></span></td>
<td><span data-ttu-id="805ab-302">949.75</span><span class="sxs-lookup"><span data-stu-id="805ab-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-303">11</span><span class="sxs-lookup"><span data-stu-id="805ab-303">11</span></span></td>
<td><span data-ttu-id="805ab-304">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-305">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="805ab-306">-949.75</span></span></td>
<td><span data-ttu-id="805ab-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="805ab-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="805ab-308">Zoals in de bovenstaande tabel wordt aangegeven, moeten drie boeken worden gerapporteerd onder zowel wettelijke als IFRS-rapportage.</span><span class="sxs-lookup"><span data-stu-id="805ab-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="805ab-309">In het wettelijke boek wordt de leasebetaling vastgelegd volgens de regels voor cash-basis-boekhouding onder de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="805ab-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="805ab-310">Het wettelijke terugboekingsboek keert de wettelijke journaalposten om.</span><span class="sxs-lookup"><span data-stu-id="805ab-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="805ab-311">In het IFRS 16 boek worden de journaalposten gemaakt die zijn vereist volgens IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="805ab-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="805ab-312">U moet een lease slechts één keer invoeren.</span><span class="sxs-lookup"><span data-stu-id="805ab-312">You must enter a lease only one time.</span></span> <span data-ttu-id="805ab-313">Vervolgens kunt u de pagina **Boeken** openen om alle boeken te zien die aan de lease zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="805ab-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="805ab-314">Wanneer u de boeken maakt, moeten alle drie aan dezelfde leaserecord zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="805ab-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="805ab-315">De eerste journaalpost registreert de leasekosten uit hoofde van het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="805ab-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="805ab-316">U kunt de betalingen maken in een batch of door het betalingsschema te selecteren in het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="805ab-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="805ab-317">Voor dit voorbeeld wordt de volgende journaalpost gemaakt voor het wettelijk boek van het betalingsschema.</span><span class="sxs-lookup"><span data-stu-id="805ab-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="805ab-318">Leasebetaling – 31-1-2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="805ab-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="805ab-319">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="805ab-319">Account type</span></span> | <span data-ttu-id="805ab-320">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-320">Account number</span></span> | <span data-ttu-id="805ab-321">Laag</span><span class="sxs-lookup"><span data-stu-id="805ab-321">Layer</span></span>   | <span data-ttu-id="805ab-322">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-322">Account description</span></span> | <span data-ttu-id="805ab-323">Debet</span><span class="sxs-lookup"><span data-stu-id="805ab-323">Debit</span></span>    | <span data-ttu-id="805ab-324">Krediet</span><span class="sxs-lookup"><span data-stu-id="805ab-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="805ab-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-325">Ledger</span></span>       | <span data-ttu-id="805ab-326">1</span><span class="sxs-lookup"><span data-stu-id="805ab-326">1</span></span>              | <span data-ttu-id="805ab-327">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-327">Current</span></span> | <span data-ttu-id="805ab-328">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="805ab-328">Lease expense</span></span>       | <span data-ttu-id="805ab-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-329">1,000.00</span></span> |          |
| <span data-ttu-id="805ab-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-330">Ledger</span></span>       | <span data-ttu-id="805ab-331">4</span><span class="sxs-lookup"><span data-stu-id="805ab-331">4</span></span>              | <span data-ttu-id="805ab-332">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-332">Current</span></span> | <span data-ttu-id="805ab-333">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="805ab-333">Clearing account</span></span>    |          | <span data-ttu-id="805ab-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-334">1,000.00</span></span> |

<span data-ttu-id="805ab-335">Een medewerker leveranciers gebruikt de standaard Dynamics 365-functionaliteit om een factuur te maken die moet worden betaald voor de lease buiten Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="805ab-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="805ab-336">In plaats van **Leasekosten** te selecteren als de debetrekening, selecteert de medewerker leveranciers een vereffeningsrekening om de volgende post te genereren.</span><span class="sxs-lookup"><span data-stu-id="805ab-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="805ab-337">Leveranciersproces – 31-1-2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="805ab-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="805ab-338">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="805ab-338">Account type</span></span> | <span data-ttu-id="805ab-339">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-339">Account number</span></span> | <span data-ttu-id="805ab-340">Laag</span><span class="sxs-lookup"><span data-stu-id="805ab-340">Layer</span></span>   | <span data-ttu-id="805ab-341">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-341">Account description</span></span> | <span data-ttu-id="805ab-342">Debet</span><span class="sxs-lookup"><span data-stu-id="805ab-342">Debit</span></span>    | <span data-ttu-id="805ab-343">Krediet</span><span class="sxs-lookup"><span data-stu-id="805ab-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="805ab-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-344">Ledger</span></span>       | <span data-ttu-id="805ab-345">4</span><span class="sxs-lookup"><span data-stu-id="805ab-345">4</span></span>              | <span data-ttu-id="805ab-346">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-346">Current</span></span> | <span data-ttu-id="805ab-347">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="805ab-347">Clearing account</span></span>    | <span data-ttu-id="805ab-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-348">1,000.00</span></span> |          |
| <span data-ttu-id="805ab-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-349">Ledger</span></span>       | <span data-ttu-id="805ab-350">2</span><span class="sxs-lookup"><span data-stu-id="805ab-350">2</span></span>              | <span data-ttu-id="805ab-351">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-351">Current</span></span> | <span data-ttu-id="805ab-352">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="805ab-352">Bank fee</span></span>            | <span data-ttu-id="805ab-353">3.00</span><span class="sxs-lookup"><span data-stu-id="805ab-353">3.00</span></span>     |          |
| <span data-ttu-id="805ab-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-354">Ledger</span></span>       | <span data-ttu-id="805ab-355">3</span><span class="sxs-lookup"><span data-stu-id="805ab-355">3</span></span>              | <span data-ttu-id="805ab-356">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-356">Current</span></span> | <span data-ttu-id="805ab-357">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="805ab-357">VAT expense</span></span>         | <span data-ttu-id="805ab-358">5.00</span><span class="sxs-lookup"><span data-stu-id="805ab-358">5.00</span></span>     |          |
| <span data-ttu-id="805ab-359">Leverancier</span><span class="sxs-lookup"><span data-stu-id="805ab-359">Vendor</span></span>       | <span data-ttu-id="805ab-360">5</span><span class="sxs-lookup"><span data-stu-id="805ab-360">5</span></span>              | <span data-ttu-id="805ab-361">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-361">Current</span></span> | <span data-ttu-id="805ab-362">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="805ab-362">Accounts payable</span></span>    |          | <span data-ttu-id="805ab-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="805ab-363">1,008.00</span></span> |

<span data-ttu-id="805ab-364">Wanneer het overzicht naar de leverancier wordt verzonden, volgt u het normale betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="805ab-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="805ab-365">Tijdens dit proces wordt de volgende journaalpost gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="805ab-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="805ab-366">Contante betaling – 31-1-2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="805ab-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="805ab-367">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="805ab-367">Account type</span></span> | <span data-ttu-id="805ab-368">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-368">Account number</span></span> | <span data-ttu-id="805ab-369">Laag</span><span class="sxs-lookup"><span data-stu-id="805ab-369">Layer</span></span>   | <span data-ttu-id="805ab-370">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-370">Account description</span></span> | <span data-ttu-id="805ab-371">Debet</span><span class="sxs-lookup"><span data-stu-id="805ab-371">Debit</span></span>    | <span data-ttu-id="805ab-372">Krediet</span><span class="sxs-lookup"><span data-stu-id="805ab-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="805ab-373">Leverancier</span><span class="sxs-lookup"><span data-stu-id="805ab-373">Vendor</span></span>       | <span data-ttu-id="805ab-374">5</span><span class="sxs-lookup"><span data-stu-id="805ab-374">5</span></span>              | <span data-ttu-id="805ab-375">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-375">Current</span></span> | <span data-ttu-id="805ab-376">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="805ab-376">Accounts Payable</span></span>    | <span data-ttu-id="805ab-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="805ab-377">1,008.00</span></span> |          |
| <span data-ttu-id="805ab-378">Bank</span><span class="sxs-lookup"><span data-stu-id="805ab-378">Bank</span></span>         | <span data-ttu-id="805ab-379">9</span><span class="sxs-lookup"><span data-stu-id="805ab-379">9</span></span>              | <span data-ttu-id="805ab-380">Huidig</span><span class="sxs-lookup"><span data-stu-id="805ab-380">Current</span></span> | <span data-ttu-id="805ab-381">Contant</span><span class="sxs-lookup"><span data-stu-id="805ab-381">Cash</span></span>                |          | <span data-ttu-id="805ab-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="805ab-382">1,008.00</span></span> |

<span data-ttu-id="805ab-383">U hebt op dit punt volledig verantwoord voor deze lease onder wettelijke rapportagevereisten en kunt een proefbalans genereren met behulp van de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="805ab-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="805ab-384">Het systeem geeft een proefbalans weer met de volgende cijfers.</span><span class="sxs-lookup"><span data-stu-id="805ab-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="805ab-385">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="805ab-386">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="805ab-387">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="805ab-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="805ab-388">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="805ab-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="805ab-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="805ab-389">JE-100</span></span></th>
<th><span data-ttu-id="805ab-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="805ab-390">JE-110</span></span></th>
<th><span data-ttu-id="805ab-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="805ab-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="805ab-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="805ab-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="805ab-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="805ab-395">1</span><span class="sxs-lookup"><span data-stu-id="805ab-395">1</span></span></td>
<td><span data-ttu-id="805ab-396">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="805ab-396">Lease expense</span></span></td>
<td><span data-ttu-id="805ab-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-399">2</span><span class="sxs-lookup"><span data-stu-id="805ab-399">2</span></span></td>
<td><span data-ttu-id="805ab-400">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="805ab-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-401">3.00</span><span class="sxs-lookup"><span data-stu-id="805ab-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-402">3.00</span><span class="sxs-lookup"><span data-stu-id="805ab-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-403">3</span><span class="sxs-lookup"><span data-stu-id="805ab-403">3</span></span></td>
<td><span data-ttu-id="805ab-404">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="805ab-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-405">5.00</span><span class="sxs-lookup"><span data-stu-id="805ab-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-406">5.00</span><span class="sxs-lookup"><span data-stu-id="805ab-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-407">4</span><span class="sxs-lookup"><span data-stu-id="805ab-407">4</span></span></td>
<td><span data-ttu-id="805ab-408">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="805ab-408">Clearing account</span></span></td>
<td><span data-ttu-id="805ab-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="805ab-409">-1,000.00</span></span></td>
<td><span data-ttu-id="805ab-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-411">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-412">5</span><span class="sxs-lookup"><span data-stu-id="805ab-412">5</span></span></td>
<td><span data-ttu-id="805ab-413">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="805ab-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="805ab-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="805ab-414">-1,008.00</span></span></td>
<td><span data-ttu-id="805ab-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="805ab-415">1,008.00</span></span></td>
<td><span data-ttu-id="805ab-416">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-417">6</span><span class="sxs-lookup"><span data-stu-id="805ab-417">6</span></span></td>
<td><span data-ttu-id="805ab-418">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="805ab-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-419">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-420">7</span><span class="sxs-lookup"><span data-stu-id="805ab-420">7</span></span></td>
<td><span data-ttu-id="805ab-421">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="805ab-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-422">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-423">8</span><span class="sxs-lookup"><span data-stu-id="805ab-423">8</span></span></td>
<td><span data-ttu-id="805ab-424">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="805ab-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-425">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-426">9</span><span class="sxs-lookup"><span data-stu-id="805ab-426">9</span></span></td>
<td><span data-ttu-id="805ab-427">Contant</span><span class="sxs-lookup"><span data-stu-id="805ab-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="805ab-428">-1,008.00</span></span></td>
<td><span data-ttu-id="805ab-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="805ab-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-430">10</span><span class="sxs-lookup"><span data-stu-id="805ab-430">10</span></span></td>
<td><span data-ttu-id="805ab-431">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="805ab-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-432">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="805ab-433">11</span><span class="sxs-lookup"><span data-stu-id="805ab-433">11</span></span></td>
<td><span data-ttu-id="805ab-434">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="805ab-435">0,00</span><span class="sxs-lookup"><span data-stu-id="805ab-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="805ab-436">Als u de IFRS 16 cijfers wilt gebruiken om dezelfde proefbalans uit te voeren, moeten de wettelijke boekhoudingsjournaalposten worden teruggeboekt en moeten de IFRS 16-journaalposten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="805ab-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="805ab-437">Voor het omkeren van de wettelijke journaalposten bevat dit voorbeeld een wettelijk terugboekingsboek met dezelfde instellingen als het wettelijke boek, maar een tegengesteld boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="805ab-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="805ab-438">Het wettelijke boek heeft bijvoorbeeld een leasekostenrekening *gedebiteerd*, maar het terugboekingsboek *crediteert* deze rekening.</span><span class="sxs-lookup"><span data-stu-id="805ab-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="805ab-439">Deze relaties worden eenvoudig gedefinieerd in de boekingsrekeningen Activa leasen op de pagina **Parameters voor activa leasing** (**Activa leasen \> Instellen \> Parameters voor activa leasing**).</span><span class="sxs-lookup"><span data-stu-id="805ab-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="805ab-440">Wanneer hetzelfde proces dat is gebruikt voor het wettelijke boek, wordt gebruikt voor het terugboekingsboek, wordt de volgende journaalpost geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="805ab-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="805ab-441">Het verschil is dat het terugboekingsboek de stornoposten uit het wettelijke boek boekt.</span><span class="sxs-lookup"><span data-stu-id="805ab-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="805ab-442">De stornoposten worden ook in de aangepaste laag aangebracht.</span><span class="sxs-lookup"><span data-stu-id="805ab-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="805ab-443">Wanneer een proefbalans wordt uitgevoerd op de huidige laag, worden de stornojournaalposten niet opgenomen.</span><span class="sxs-lookup"><span data-stu-id="805ab-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="805ab-444">Leasebetaling – 31-1-2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="805ab-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="805ab-445">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="805ab-445">Account type</span></span> | <span data-ttu-id="805ab-446">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-446">Account number</span></span> | <span data-ttu-id="805ab-447">Laag</span><span class="sxs-lookup"><span data-stu-id="805ab-447">Layer</span></span>  | <span data-ttu-id="805ab-448">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-448">Account description</span></span> | <span data-ttu-id="805ab-449">Debet</span><span class="sxs-lookup"><span data-stu-id="805ab-449">Debit</span></span>    | <span data-ttu-id="805ab-450">Krediet</span><span class="sxs-lookup"><span data-stu-id="805ab-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="805ab-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-451">Ledger</span></span>       | <span data-ttu-id="805ab-452">4</span><span class="sxs-lookup"><span data-stu-id="805ab-452">4</span></span>              | <span data-ttu-id="805ab-453">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-453">Custom</span></span> | <span data-ttu-id="805ab-454">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="805ab-454">Clearing account</span></span>    | <span data-ttu-id="805ab-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-455">1,000.00</span></span> |          |
| <span data-ttu-id="805ab-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-456">Ledger</span></span>       | <span data-ttu-id="805ab-457">1</span><span class="sxs-lookup"><span data-stu-id="805ab-457">1</span></span>              | <span data-ttu-id="805ab-458">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-458">Custom</span></span> | <span data-ttu-id="805ab-459">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="805ab-459">Lease expense</span></span>       |          | <span data-ttu-id="805ab-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-460">1,000.00</span></span> |

<span data-ttu-id="805ab-461">Nu u de wettelijk journaalposten hebt verwijderd, worden alle journaalposten geboekt die IFRS 16 vereist in het IFRS 16 boek.</span><span class="sxs-lookup"><span data-stu-id="805ab-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="805ab-462">Deze posten omvatten de eerste toerekening van het RoU activum en de verplichting, en de record van rente en afschrijving.</span><span class="sxs-lookup"><span data-stu-id="805ab-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="805ab-463">Initiële toerekening - 1-1-2020 - JE 140</span><span class="sxs-lookup"><span data-stu-id="805ab-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="805ab-464">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="805ab-464">Account type</span></span> | <span data-ttu-id="805ab-465">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-465">Account number</span></span> | <span data-ttu-id="805ab-466">Laag</span><span class="sxs-lookup"><span data-stu-id="805ab-466">Layer</span></span>  | <span data-ttu-id="805ab-467">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-467">Account description</span></span>      | <span data-ttu-id="805ab-468">Debet</span><span class="sxs-lookup"><span data-stu-id="805ab-468">Debit</span></span>     | <span data-ttu-id="805ab-469">Krediet</span><span class="sxs-lookup"><span data-stu-id="805ab-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="805ab-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-470">Ledger</span></span>       | <span data-ttu-id="805ab-471">6</span><span class="sxs-lookup"><span data-stu-id="805ab-471">6</span></span>              | <span data-ttu-id="805ab-472">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-472">Custom</span></span> | <span data-ttu-id="805ab-473">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="805ab-473">ROU Asset</span></span>                | <span data-ttu-id="805ab-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="805ab-474">22,793.90</span></span> |           |
| <span data-ttu-id="805ab-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-475">Ledger</span></span>       | <span data-ttu-id="805ab-476">7</span><span class="sxs-lookup"><span data-stu-id="805ab-476">7</span></span>              | <span data-ttu-id="805ab-477">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-477">Custom</span></span> | <span data-ttu-id="805ab-478">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="805ab-478">Finance lease obligation</span></span> |           | <span data-ttu-id="805ab-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="805ab-479">22,793.90</span></span> |

<span data-ttu-id="805ab-480">De leasebetaling wordt geboekt zoals de andere leasebetalingen.</span><span class="sxs-lookup"><span data-stu-id="805ab-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="805ab-481">De reden voor het gebruik van de vereffeningsrekening is ervoor te zorgen dat contant geld slechts één keer wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="805ab-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="805ab-482">Leasebetaling – 31-1-2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="805ab-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="805ab-483">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="805ab-483">Account type</span></span> | <span data-ttu-id="805ab-484">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-484">Account number</span></span> | <span data-ttu-id="805ab-485">Laag</span><span class="sxs-lookup"><span data-stu-id="805ab-485">Layer</span></span>  | <span data-ttu-id="805ab-486">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-486">Account description</span></span>      | <span data-ttu-id="805ab-487">Debet</span><span class="sxs-lookup"><span data-stu-id="805ab-487">Debit</span></span>    | <span data-ttu-id="805ab-488">Krediet</span><span class="sxs-lookup"><span data-stu-id="805ab-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="805ab-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-489">Ledger</span></span>       | <span data-ttu-id="805ab-490">7</span><span class="sxs-lookup"><span data-stu-id="805ab-490">7</span></span>              | <span data-ttu-id="805ab-491">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-491">Custom</span></span> | <span data-ttu-id="805ab-492">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="805ab-492">Finance lease obligation</span></span> | <span data-ttu-id="805ab-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-493">1,000.00</span></span> |          |
| <span data-ttu-id="805ab-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-494">Ledger</span></span>       | <span data-ttu-id="805ab-495">4</span><span class="sxs-lookup"><span data-stu-id="805ab-495">4</span></span>              | <span data-ttu-id="805ab-496">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-496">Custom</span></span> | <span data-ttu-id="805ab-497">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="805ab-497">Clearing account</span></span>         |          | <span data-ttu-id="805ab-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="805ab-498">1,000.00</span></span> |

<span data-ttu-id="805ab-499">De journaalpost voor rentelasten wordt gegenereerd op basis van het afschrijvingsschema voor verplichtingen.</span><span class="sxs-lookup"><span data-stu-id="805ab-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="805ab-500">Rente-uitgaven - 31-1-2020 - JE 160</span><span class="sxs-lookup"><span data-stu-id="805ab-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="805ab-501">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="805ab-501">Account type</span></span> | <span data-ttu-id="805ab-502">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-502">Account number</span></span> | <span data-ttu-id="805ab-503">Laag</span><span class="sxs-lookup"><span data-stu-id="805ab-503">Layer</span></span>  | <span data-ttu-id="805ab-504">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-504">Account description</span></span>      | <span data-ttu-id="805ab-505">Debet</span><span class="sxs-lookup"><span data-stu-id="805ab-505">Debit</span></span> | <span data-ttu-id="805ab-506">Krediet</span><span class="sxs-lookup"><span data-stu-id="805ab-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="805ab-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-507">Ledger</span></span>       | <span data-ttu-id="805ab-508">8</span><span class="sxs-lookup"><span data-stu-id="805ab-508">8</span></span>              | <span data-ttu-id="805ab-509">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-509">Custom</span></span> | <span data-ttu-id="805ab-510">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="805ab-510">Interest expense</span></span>         | <span data-ttu-id="805ab-511">94.97</span><span class="sxs-lookup"><span data-stu-id="805ab-511">94.97</span></span> |        |
| <span data-ttu-id="805ab-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-512">Ledger</span></span>       | <span data-ttu-id="805ab-513">7</span><span class="sxs-lookup"><span data-stu-id="805ab-513">7</span></span>              | <span data-ttu-id="805ab-514">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-514">Custom</span></span> | <span data-ttu-id="805ab-515">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="805ab-515">Finance lease obligation</span></span> |       | <span data-ttu-id="805ab-516">94.97</span><span class="sxs-lookup"><span data-stu-id="805ab-516">94.97</span></span>  |

<span data-ttu-id="805ab-517">De journaalpost voor afschrijvingskosten wordt gegenereerd op basis van het schema activumafschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="805ab-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="805ab-518">Afschrijvingskosten - 31-1-2020 - JE 170</span><span class="sxs-lookup"><span data-stu-id="805ab-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="805ab-519">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="805ab-519">Account type</span></span> | <span data-ttu-id="805ab-520">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-520">Account number</span></span> | <span data-ttu-id="805ab-521">Laag</span><span class="sxs-lookup"><span data-stu-id="805ab-521">Layer</span></span>  | <span data-ttu-id="805ab-522">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-522">Account description</span></span>      | <span data-ttu-id="805ab-523">Debet</span><span class="sxs-lookup"><span data-stu-id="805ab-523">Debit</span></span>  | <span data-ttu-id="805ab-524">Krediet</span><span class="sxs-lookup"><span data-stu-id="805ab-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="805ab-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-525">Ledger</span></span>       | <span data-ttu-id="805ab-526">10</span><span class="sxs-lookup"><span data-stu-id="805ab-526">10</span></span>             | <span data-ttu-id="805ab-527">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-527">Custom</span></span> | <span data-ttu-id="805ab-528">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="805ab-528">Depreciation expense</span></span>     | <span data-ttu-id="805ab-529">949.75</span><span class="sxs-lookup"><span data-stu-id="805ab-529">949.75</span></span> |        |
| <span data-ttu-id="805ab-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="805ab-530">Ledger</span></span>       | <span data-ttu-id="805ab-531">11</span><span class="sxs-lookup"><span data-stu-id="805ab-531">11</span></span>             | <span data-ttu-id="805ab-532">Aangepast</span><span class="sxs-lookup"><span data-stu-id="805ab-532">Custom</span></span> | <span data-ttu-id="805ab-533">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="805ab-534">949.75</span><span class="sxs-lookup"><span data-stu-id="805ab-534">949.75</span></span> |

<span data-ttu-id="805ab-535">Nadat al deze journaalposten zijn gemaakt en geboekt, ziet u de volgende waarden voor "aangepaste laag 1".</span><span class="sxs-lookup"><span data-stu-id="805ab-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="805ab-536">De laatste kolom bevat de bankkosten, de kosten voor de toegevoegde waarde (btw) en de reductie van contant geld uit de vorige laag, maar bevat niet de journaalposten voor wettelijke rapportage.</span><span class="sxs-lookup"><span data-stu-id="805ab-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="805ab-537">Daarom bereikt u echte mogelijkheden voor dubbele rapportage.</span><span class="sxs-lookup"><span data-stu-id="805ab-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="805ab-538">Op dit punt hoeft het bedrijf alleen zijn proefbalans uit te voeren en de huidige laag en de aangepaste laag combineren om een IFRS-proefbalans te maken.</span><span class="sxs-lookup"><span data-stu-id="805ab-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="805ab-539">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="805ab-539">Account No</span></span> | <span data-ttu-id="805ab-540">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-540">Description</span></span>              | <span data-ttu-id="805ab-541">Wettelijk boek\-Huidige laag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="805ab-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="805ab-542">Wettelijk boek\-Huidige laag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="805ab-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="805ab-543">Wettelijk boek\-Huidige laag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="805ab-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="805ab-544">Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="805ab-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="805ab-545">Terugboekingsboek\-Aangepaste laag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="805ab-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="805ab-546">IFRS 16-boek\-Aangepaste laag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="805ab-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="805ab-547">IFRS 16-boek\-Aangepaste laag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="805ab-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="805ab-548">IFRS 16-boek\-Aangepaste laag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="805ab-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="805ab-549">IFRS 16-boek\-Aangepaste laag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="805ab-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="805ab-550">Aangepaste laag \+ Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="805ab-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="805ab-551">1</span><span class="sxs-lookup"><span data-stu-id="805ab-551">1</span></span>          | <span data-ttu-id="805ab-552">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="805ab-552">Lease expense</span></span>            | <span data-ttu-id="805ab-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="805ab-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-554">1,000\.00</span></span>               |   | <span data-ttu-id="805ab-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="805ab-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="805ab-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-556">0\.00</span></span>                                   |
| <span data-ttu-id="805ab-557">2</span><span class="sxs-lookup"><span data-stu-id="805ab-557">2</span></span>          | <span data-ttu-id="805ab-558">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="805ab-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="805ab-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="805ab-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="805ab-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-561">3\.00</span></span>                                   |
| <span data-ttu-id="805ab-562">3</span><span class="sxs-lookup"><span data-stu-id="805ab-562">3</span></span>          | <span data-ttu-id="805ab-563">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="805ab-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="805ab-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="805ab-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="805ab-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-566">5\.00</span></span>                                   |
| <span data-ttu-id="805ab-567">4</span><span class="sxs-lookup"><span data-stu-id="805ab-567">4</span></span>          | <span data-ttu-id="805ab-568">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="805ab-568">Clearing account</span></span>         | <span data-ttu-id="805ab-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="805ab-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="805ab-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-571">0\.00</span></span>                   |   | <span data-ttu-id="805ab-572">1.000</span><span class="sxs-lookup"><span data-stu-id="805ab-572">1,000</span></span>                                           |                                                | <span data-ttu-id="805ab-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="805ab-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="805ab-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-574">0\.00</span></span>                                   |
| <span data-ttu-id="805ab-575">5</span><span class="sxs-lookup"><span data-stu-id="805ab-575">5</span></span>          | <span data-ttu-id="805ab-576">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="805ab-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="805ab-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="805ab-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-578">1,008\.00</span></span>                                         | <span data-ttu-id="805ab-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="805ab-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-580">0\.00</span></span>                                   |
| <span data-ttu-id="805ab-581">6</span><span class="sxs-lookup"><span data-stu-id="805ab-581">6</span></span>          | <span data-ttu-id="805ab-582">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="805ab-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="805ab-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="805ab-584">22,794</span><span class="sxs-lookup"><span data-stu-id="805ab-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="805ab-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="805ab-585">22,793\.90</span></span>                              |
| <span data-ttu-id="805ab-586">7</span><span class="sxs-lookup"><span data-stu-id="805ab-586">7</span></span>          | <span data-ttu-id="805ab-587">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="805ab-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="805ab-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="805ab-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="805ab-589">\-22,794</span></span>                                       | <span data-ttu-id="805ab-590">1.000</span><span class="sxs-lookup"><span data-stu-id="805ab-590">1,000</span></span>                                          | <span data-ttu-id="805ab-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="805ab-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="805ab-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="805ab-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="805ab-593">8</span><span class="sxs-lookup"><span data-stu-id="805ab-593">8</span></span>          | <span data-ttu-id="805ab-594">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="805ab-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="805ab-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="805ab-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="805ab-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="805ab-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="805ab-597">94\.97</span></span>                                  |
| <span data-ttu-id="805ab-598">9</span><span class="sxs-lookup"><span data-stu-id="805ab-598">9</span></span>          | <span data-ttu-id="805ab-599">Contant</span><span class="sxs-lookup"><span data-stu-id="805ab-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="805ab-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="805ab-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="805ab-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="805ab-603">10</span><span class="sxs-lookup"><span data-stu-id="805ab-603">10</span></span>         | <span data-ttu-id="805ab-604">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="805ab-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="805ab-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="805ab-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="805ab-606">949\.75</span></span>                                        | <span data-ttu-id="805ab-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="805ab-607">949\.75</span></span>                                 |
| <span data-ttu-id="805ab-608">11</span><span class="sxs-lookup"><span data-stu-id="805ab-608">11</span></span>         | <span data-ttu-id="805ab-609">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="805ab-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="805ab-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="805ab-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="805ab-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="805ab-611">\-949\.75</span></span>                                      | <span data-ttu-id="805ab-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="805ab-612">\-949\.75</span></span>                               |


