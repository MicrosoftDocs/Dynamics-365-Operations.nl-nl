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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442149"
---
# <a name="dual-reporting"></a><span data-ttu-id="7adad-103">Dubbele rapportage</span><span class="sxs-lookup"><span data-stu-id="7adad-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7adad-104">In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="7adad-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="7adad-105">Vertrouwdheid met boekingslagen in Microsoft Dynamics 365 Finance is vereist en maakt het voorbeeld gemakkelijker te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="7adad-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="7adad-106">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7adad-106">Example</span></span>

<span data-ttu-id="7adad-107">In het volgende voorbeeld wordt een lease verantwoord onder de Italiaanse wettelijke rapportering door middel van de cash-basis-methode en de IFRS-rapportagemethoden.</span><span class="sxs-lookup"><span data-stu-id="7adad-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="7adad-108">Het bedrijf moet drie boeken maken om te verantwoorden voor zowel de Italiaanse wettelijke vereisten als de IFRS 16-vereisten.</span><span class="sxs-lookup"><span data-stu-id="7adad-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="7adad-109">Eén boek is vereist voor IFRS 16, één boek is vereist voor wettelijke vereisten en één boek is vereist om de wettelijke boekingen automatisch terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="7adad-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="7adad-110">De boeken worden ingesteld, zoals in de volgende tabellen wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7adad-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="7adad-111">**IFRS 16-boek**</span><span class="sxs-lookup"><span data-stu-id="7adad-111">**IFRS 16 book**</span></span>

<span data-ttu-id="7adad-112">Het IFRS 16 boek is zo ingesteld dat het voldoet aan de IFRS 16-boekhoudnorm.</span><span class="sxs-lookup"><span data-stu-id="7adad-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="7adad-113">Alle posten die in dit boek worden geboekt, worden naar een aangepaste laag geboekt.</span><span class="sxs-lookup"><span data-stu-id="7adad-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="7adad-114">Naam</span><span class="sxs-lookup"><span data-stu-id="7adad-114">Name</span></span>                                    | <span data-ttu-id="7adad-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="7adad-116">Boektype</span><span class="sxs-lookup"><span data-stu-id="7adad-116">Book type</span></span>                               | <span data-ttu-id="7adad-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="7adad-117">IFRS 16</span></span>        |
| <span data-ttu-id="7adad-118">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-118">Book description</span></span>                        | <span data-ttu-id="7adad-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="7adad-119">IFRS 16</span></span>        |
| <span data-ttu-id="7adad-120">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="7adad-120">Posting Layer</span></span>                           | <span data-ttu-id="7adad-121">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="7adad-121">Custom layer 1</span></span> |
| <span data-ttu-id="7adad-122">Leasetype</span><span class="sxs-lookup"><span data-stu-id="7adad-122">Lease Type</span></span>                              | <span data-ttu-id="7adad-123">Finance</span><span class="sxs-lookup"><span data-stu-id="7adad-123">Finance</span></span>        |
| <span data-ttu-id="7adad-124">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="7adad-124">Accounting Framework</span></span>                    | <span data-ttu-id="7adad-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="7adad-125">IFRS 16</span></span>        |
| <span data-ttu-id="7adad-126">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="7adad-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="7adad-127">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-127">0.00</span></span>           |
| <span data-ttu-id="7adad-128">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="7adad-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="7adad-129">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-129">0.00</span></span>           |
| <span data-ttu-id="7adad-130">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="7adad-130">Short-term threshold</span></span>                    | <span data-ttu-id="7adad-131">12</span><span class="sxs-lookup"><span data-stu-id="7adad-131">12</span></span>             |
| <span data-ttu-id="7adad-132">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="7adad-132">Low Value Threshold</span></span>                     | <span data-ttu-id="7adad-133">5.000,00</span><span class="sxs-lookup"><span data-stu-id="7adad-133">5,000.00</span></span>       |
| <span data-ttu-id="7adad-134">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="7adad-134">Pay to Vendor</span></span>                           | <span data-ttu-id="7adad-135">No</span><span class="sxs-lookup"><span data-stu-id="7adad-135">No</span></span>             |

<span data-ttu-id="7adad-136">**Wettelijk boek**</span><span class="sxs-lookup"><span data-stu-id="7adad-136">**Statutory book**</span></span>

<span data-ttu-id="7adad-137">Het wettelijke boek is een cash-basis-boek waar het bedrijf de leasekosten zal verantwoorden als het bedrag aan geld dat maandelijks wordt betaald voor huur.</span><span class="sxs-lookup"><span data-stu-id="7adad-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="7adad-138">Dit boek produceert geen RoU-activum of leaseverplichtingen.</span><span class="sxs-lookup"><span data-stu-id="7adad-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="7adad-139">Naam</span><span class="sxs-lookup"><span data-stu-id="7adad-139">Name</span></span>                                    | <span data-ttu-id="7adad-140">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="7adad-141">Boektype</span><span class="sxs-lookup"><span data-stu-id="7adad-141">Book type</span></span>                               | <span data-ttu-id="7adad-142">Wettelijk</span><span class="sxs-lookup"><span data-stu-id="7adad-142">Statutory</span></span>   |
| <span data-ttu-id="7adad-143">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-143">Book description</span></span>                        | <span data-ttu-id="7adad-144">Lokale GAAP</span><span class="sxs-lookup"><span data-stu-id="7adad-144">Local GAAP</span></span>  |
| <span data-ttu-id="7adad-145">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="7adad-145">Posting Layer</span></span>                           | <span data-ttu-id="7adad-146">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-146">Current</span></span>     |
| <span data-ttu-id="7adad-147">Leasetype</span><span class="sxs-lookup"><span data-stu-id="7adad-147">Lease Type</span></span>                              | <span data-ttu-id="7adad-148">Automatisch</span><span class="sxs-lookup"><span data-stu-id="7adad-148">Automatic</span></span>   |
| <span data-ttu-id="7adad-149">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="7adad-149">Accounting Framework</span></span>                    | <span data-ttu-id="7adad-150">Contante basis</span><span class="sxs-lookup"><span data-stu-id="7adad-150">Cash basis</span></span>  |
| <span data-ttu-id="7adad-151">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="7adad-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="7adad-152">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-152">0.00</span></span>        |
| <span data-ttu-id="7adad-153">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="7adad-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="7adad-154">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-154">0.00</span></span>        |
| <span data-ttu-id="7adad-155">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="7adad-155">Short-term threshold</span></span>                    | <span data-ttu-id="7adad-156">0</span><span class="sxs-lookup"><span data-stu-id="7adad-156">0</span></span>           |
| <span data-ttu-id="7adad-157">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="7adad-157">Low Value Threshold</span></span>                     | <span data-ttu-id="7adad-158">0</span><span class="sxs-lookup"><span data-stu-id="7adad-158">0</span></span>           |
| <span data-ttu-id="7adad-159">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="7adad-159">Pay to Vendor</span></span>                           | <span data-ttu-id="7adad-160">No</span><span class="sxs-lookup"><span data-stu-id="7adad-160">No</span></span>          |

<span data-ttu-id="7adad-161">**Wettelijk terugboekingsboek**</span><span class="sxs-lookup"><span data-stu-id="7adad-161">**Statutory reversal book**</span></span>

<span data-ttu-id="7adad-162">Het wettelijke terugboekingsboek wordt op dezelfde manier ingesteld als het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="7adad-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="7adad-163">Naam</span><span class="sxs-lookup"><span data-stu-id="7adad-163">Name</span></span>                                    | <span data-ttu-id="7adad-164">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="7adad-165">Boektype</span><span class="sxs-lookup"><span data-stu-id="7adad-165">Book type</span></span>                               | <span data-ttu-id="7adad-166">Wettelijk - terugboeking</span><span class="sxs-lookup"><span data-stu-id="7adad-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="7adad-167">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-167">Book description</span></span>                        | <span data-ttu-id="7adad-168">Boek om wettelijk boek terug te boeken</span><span class="sxs-lookup"><span data-stu-id="7adad-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="7adad-169">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="7adad-169">Posting Layer</span></span>                           | <span data-ttu-id="7adad-170">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="7adad-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="7adad-171">Leasetype</span><span class="sxs-lookup"><span data-stu-id="7adad-171">Lease Type</span></span>                              | <span data-ttu-id="7adad-172">Automatisch</span><span class="sxs-lookup"><span data-stu-id="7adad-172">Automatic</span></span>                      |
| <span data-ttu-id="7adad-173">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="7adad-173">Accounting Framework</span></span>                    | <span data-ttu-id="7adad-174">Contante basis</span><span class="sxs-lookup"><span data-stu-id="7adad-174">Cash basis</span></span>                     |
| <span data-ttu-id="7adad-175">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="7adad-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="7adad-176">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-176">0.00</span></span>                           |
| <span data-ttu-id="7adad-177">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="7adad-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="7adad-178">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-178">0.00</span></span>                           |
| <span data-ttu-id="7adad-179">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="7adad-179">Short-term threshold</span></span>                    | <span data-ttu-id="7adad-180">0</span><span class="sxs-lookup"><span data-stu-id="7adad-180">0</span></span>                              |
| <span data-ttu-id="7adad-181">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="7adad-181">Low Value Threshold</span></span>                     | <span data-ttu-id="7adad-182">0</span><span class="sxs-lookup"><span data-stu-id="7adad-182">0</span></span>                              |
| <span data-ttu-id="7adad-183">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="7adad-183">Pay to Vendor</span></span>                           | <span data-ttu-id="7adad-184">No</span><span class="sxs-lookup"><span data-stu-id="7adad-184">No</span></span>                             |

<span data-ttu-id="7adad-185">Voor dit voorbeeld is er een lease gemaakt met de volgende instellingen op de tabbladen **Algemeen** en **Betalingsschemaregels**.</span><span class="sxs-lookup"><span data-stu-id="7adad-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="7adad-186">**Tabblad Algemeen**</span><span class="sxs-lookup"><span data-stu-id="7adad-186">**General tab**</span></span>

| <span data-ttu-id="7adad-187">Veld</span><span class="sxs-lookup"><span data-stu-id="7adad-187">Field</span></span>                      | <span data-ttu-id="7adad-188">Waarde</span><span class="sxs-lookup"><span data-stu-id="7adad-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="7adad-189">Verhoogd leningtarief</span><span class="sxs-lookup"><span data-stu-id="7adad-189">Incremental borrowing rate</span></span> | <span data-ttu-id="7adad-190">5%</span><span class="sxs-lookup"><span data-stu-id="7adad-190">5%</span></span>               |
| <span data-ttu-id="7adad-191">Begindatum</span><span class="sxs-lookup"><span data-stu-id="7adad-191">Commencement date</span></span>          | <span data-ttu-id="7adad-192">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="7adad-192">1/1/2020</span></span>         |
| <span data-ttu-id="7adad-193">Leasegroep</span><span class="sxs-lookup"><span data-stu-id="7adad-193">Lease group</span></span>                | <span data-ttu-id="7adad-194">Gebouwen</span><span class="sxs-lookup"><span data-stu-id="7adad-194">Buildings</span></span>        |
| <span data-ttu-id="7adad-195">Leverancier</span><span class="sxs-lookup"><span data-stu-id="7adad-195">Vendor</span></span>                     | <span data-ttu-id="7adad-196">1001</span><span class="sxs-lookup"><span data-stu-id="7adad-196">1001</span></span>             |
| <span data-ttu-id="7adad-197">Reële waarde van het activum</span><span class="sxs-lookup"><span data-stu-id="7adad-197">Fair value of the asset</span></span>    | <span data-ttu-id="7adad-198">245,000</span><span class="sxs-lookup"><span data-stu-id="7adad-198">245,000</span></span>          |
| <span data-ttu-id="7adad-199">Economische levensduur activum</span><span class="sxs-lookup"><span data-stu-id="7adad-199">Asset useful life</span></span>          | <span data-ttu-id="7adad-200">120</span><span class="sxs-lookup"><span data-stu-id="7adad-200">120</span></span>              |
| <span data-ttu-id="7adad-201">Type annuïteit</span><span class="sxs-lookup"><span data-stu-id="7adad-201">Annuity type</span></span>               | <span data-ttu-id="7adad-202">Normale annuïteit</span><span class="sxs-lookup"><span data-stu-id="7adad-202">Ordinary annuity</span></span> |
| <span data-ttu-id="7adad-203">Samenstellingsinterval</span><span class="sxs-lookup"><span data-stu-id="7adad-203">Compounding interval</span></span>       | <span data-ttu-id="7adad-204">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="7adad-204">Monthly</span></span>          |

<span data-ttu-id="7adad-205">**Tabblad Regels van betalingsschema**</span><span class="sxs-lookup"><span data-stu-id="7adad-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="7adad-206">Veld</span><span class="sxs-lookup"><span data-stu-id="7adad-206">Field</span></span>             | <span data-ttu-id="7adad-207">Waarde</span><span class="sxs-lookup"><span data-stu-id="7adad-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="7adad-208">Begindatum</span><span class="sxs-lookup"><span data-stu-id="7adad-208">Start date</span></span>        | <span data-ttu-id="7adad-209">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="7adad-209">1/1/2020</span></span>   |
| <span data-ttu-id="7adad-210">Periode-interval</span><span class="sxs-lookup"><span data-stu-id="7adad-210">Period interval</span></span>   | <span data-ttu-id="7adad-211">Maanden</span><span class="sxs-lookup"><span data-stu-id="7adad-211">Months</span></span>     |
| <span data-ttu-id="7adad-212">Perioden</span><span class="sxs-lookup"><span data-stu-id="7adad-212">Periods</span></span>           | <span data-ttu-id="7adad-213">24</span><span class="sxs-lookup"><span data-stu-id="7adad-213">24</span></span>         |
| <span data-ttu-id="7adad-214">Einddatum</span><span class="sxs-lookup"><span data-stu-id="7adad-214">End date</span></span>          | <span data-ttu-id="7adad-215">31-12-2020</span><span class="sxs-lookup"><span data-stu-id="7adad-215">12/31/2020</span></span> |
| <span data-ttu-id="7adad-216">Betalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="7adad-216">Payment frequency</span></span> | <span data-ttu-id="7adad-217">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="7adad-217">Monthly</span></span>    |
| <span data-ttu-id="7adad-218">Betalingsbedrag</span><span class="sxs-lookup"><span data-stu-id="7adad-218">Payment amount</span></span>    | <span data-ttu-id="7adad-219">1.000</span><span class="sxs-lookup"><span data-stu-id="7adad-219">1,000</span></span>      |

<span data-ttu-id="7adad-220">Als u deze lease onder twee raamwerken wilt verantwoorden, gebruikt u een huidige boekingslaag en een aangepaste boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="7adad-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="7adad-221">In de volgende tabel ziet u een voorbeeld van elke journaalpost die voor elke rapportagestandaard de financiële waarde reëel moet representeren.</span><span class="sxs-lookup"><span data-stu-id="7adad-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="7adad-222">Hierna wordt een gedetailleerde omschrijving gegeven van elke journaalpost voor de eerste maand van de lease.</span><span class="sxs-lookup"><span data-stu-id="7adad-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="7adad-223">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="7adad-224">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="7adad-225">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="7adad-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="7adad-226">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="7adad-226">Current layer total</span></span></th>
<th><span data-ttu-id="7adad-227">Terugboekingsboek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="7adad-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="7adad-228">IFRS 16-boek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="7adad-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="7adad-229">Huidige laag + aangepaste laagtotaal</span><span class="sxs-lookup"><span data-stu-id="7adad-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7adad-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="7adad-230">JE-100</span></span></th>
<th><span data-ttu-id="7adad-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="7adad-231">JE-110</span></span></th>
<th><span data-ttu-id="7adad-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="7adad-232">JE-120</span></span></th>
<th><span data-ttu-id="7adad-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="7adad-233">JE-130</span></span></th>
<th><span data-ttu-id="7adad-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="7adad-234">JE-140</span></span></th>
<th><span data-ttu-id="7adad-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="7adad-235">JE-150</span></span></th>
<th><span data-ttu-id="7adad-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="7adad-236">JE-160</span></span></th>
<th><span data-ttu-id="7adad-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="7adad-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7adad-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7adad-246">1</span><span class="sxs-lookup"><span data-stu-id="7adad-246">1</span></span></td>
<td><span data-ttu-id="7adad-247">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="7adad-247">Lease expense</span></span></td>
<td><span data-ttu-id="7adad-248">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7adad-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-249">1,000.00</span></span></td>
<td><span data-ttu-id="7adad-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="7adad-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-251">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-252">2</span><span class="sxs-lookup"><span data-stu-id="7adad-252">2</span></span></td>
<td><span data-ttu-id="7adad-253">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="7adad-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-254">3,00</span><span class="sxs-lookup"><span data-stu-id="7adad-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-255">3.00</span><span class="sxs-lookup"><span data-stu-id="7adad-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-256">3.00</span><span class="sxs-lookup"><span data-stu-id="7adad-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-257">3</span><span class="sxs-lookup"><span data-stu-id="7adad-257">3</span></span></td>
<td><span data-ttu-id="7adad-258">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="7adad-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-259">5.00</span><span class="sxs-lookup"><span data-stu-id="7adad-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-260">5.00</span><span class="sxs-lookup"><span data-stu-id="7adad-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-261">5.00</span><span class="sxs-lookup"><span data-stu-id="7adad-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-262">4</span><span class="sxs-lookup"><span data-stu-id="7adad-262">4</span></span></td>
<td><span data-ttu-id="7adad-263">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="7adad-263">Clearing account</span></span></td>
<td><span data-ttu-id="7adad-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="7adad-264">-1,000.00</span></span></td>
<td><span data-ttu-id="7adad-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-266">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-266">0.00</span></span></td>
<td><span data-ttu-id="7adad-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="7adad-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-269">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-270">5</span><span class="sxs-lookup"><span data-stu-id="7adad-270">5</span></span></td>
<td><span data-ttu-id="7adad-271">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="7adad-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="7adad-272">-1,008.00</span></span></td>
<td><span data-ttu-id="7adad-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="7adad-273">1,008.00</span></span></td>
<td><span data-ttu-id="7adad-274">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-275">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-276">6</span><span class="sxs-lookup"><span data-stu-id="7adad-276">6</span></span></td>
<td><span data-ttu-id="7adad-277">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="7adad-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-278">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="7adad-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="7adad-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-281">7</span><span class="sxs-lookup"><span data-stu-id="7adad-281">7</span></span></td>
<td><span data-ttu-id="7adad-282">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="7adad-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-283">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="7adad-284">-22,794.00</span></span></td>
<td><span data-ttu-id="7adad-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-285">1,000.00</span></span></td>
<td><span data-ttu-id="7adad-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="7adad-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="7adad-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-288">8</span><span class="sxs-lookup"><span data-stu-id="7adad-288">8</span></span></td>
<td><span data-ttu-id="7adad-289">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="7adad-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-290">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-291">94.97</span><span class="sxs-lookup"><span data-stu-id="7adad-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-292">94.97</span><span class="sxs-lookup"><span data-stu-id="7adad-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-293">9</span><span class="sxs-lookup"><span data-stu-id="7adad-293">9</span></span></td>
<td><span data-ttu-id="7adad-294">Contant</span><span class="sxs-lookup"><span data-stu-id="7adad-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="7adad-295">-1,008.00</span></span></td>
<td><span data-ttu-id="7adad-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="7adad-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="7adad-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-298">10</span><span class="sxs-lookup"><span data-stu-id="7adad-298">10</span></span></td>
<td><span data-ttu-id="7adad-299">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="7adad-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-300">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-301">949.75</span><span class="sxs-lookup"><span data-stu-id="7adad-301">949.75</span></span></td>
<td><span data-ttu-id="7adad-302">949.75</span><span class="sxs-lookup"><span data-stu-id="7adad-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-303">11</span><span class="sxs-lookup"><span data-stu-id="7adad-303">11</span></span></td>
<td><span data-ttu-id="7adad-304">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-305">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="7adad-306">-949.75</span></span></td>
<td><span data-ttu-id="7adad-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="7adad-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7adad-308">Zoals in de bovenstaande tabel wordt aangegeven, moeten drie boeken worden gerapporteerd onder zowel wettelijke als IFRS-rapportage.</span><span class="sxs-lookup"><span data-stu-id="7adad-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="7adad-309">In het wettelijke boek wordt de leasebetaling vastgelegd volgens de regels voor cash-basis-boekhouding onder de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="7adad-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="7adad-310">Het wettelijke terugboekingsboek keert de wettelijke journaalposten om.</span><span class="sxs-lookup"><span data-stu-id="7adad-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="7adad-311">In het IFRS 16 boek worden de journaalposten gemaakt die zijn vereist volgens IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="7adad-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="7adad-312">U moet een lease slechts één keer invoeren.</span><span class="sxs-lookup"><span data-stu-id="7adad-312">You must enter a lease only one time.</span></span> <span data-ttu-id="7adad-313">Vervolgens kunt u de pagina **Boeken** openen om alle boeken te zien die aan de lease zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7adad-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="7adad-314">Wanneer u de boeken maakt, moeten alle drie aan dezelfde leaserecord zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7adad-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="7adad-315">De eerste journaalpost registreert de leasekosten uit hoofde van het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="7adad-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="7adad-316">U kunt de betalingen maken in een batch of door het betalingsschema te selecteren in het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="7adad-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="7adad-317">Voor dit voorbeeld wordt de volgende journaalpost gemaakt voor het wettelijk boek van het betalingsschema.</span><span class="sxs-lookup"><span data-stu-id="7adad-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="7adad-318">Leasebetaling – 31-1-2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="7adad-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="7adad-319">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="7adad-319">Account type</span></span> | <span data-ttu-id="7adad-320">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-320">Account number</span></span> | <span data-ttu-id="7adad-321">Laag</span><span class="sxs-lookup"><span data-stu-id="7adad-321">Layer</span></span>   | <span data-ttu-id="7adad-322">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-322">Account description</span></span> | <span data-ttu-id="7adad-323">Debet</span><span class="sxs-lookup"><span data-stu-id="7adad-323">Debit</span></span>    | <span data-ttu-id="7adad-324">Krediet</span><span class="sxs-lookup"><span data-stu-id="7adad-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="7adad-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-325">Ledger</span></span>       | <span data-ttu-id="7adad-326">1</span><span class="sxs-lookup"><span data-stu-id="7adad-326">1</span></span>              | <span data-ttu-id="7adad-327">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-327">Current</span></span> | <span data-ttu-id="7adad-328">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="7adad-328">Lease expense</span></span>       | <span data-ttu-id="7adad-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-329">1,000.00</span></span> |          |
| <span data-ttu-id="7adad-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-330">Ledger</span></span>       | <span data-ttu-id="7adad-331">4</span><span class="sxs-lookup"><span data-stu-id="7adad-331">4</span></span>              | <span data-ttu-id="7adad-332">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-332">Current</span></span> | <span data-ttu-id="7adad-333">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="7adad-333">Clearing account</span></span>    |          | <span data-ttu-id="7adad-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-334">1,000.00</span></span> |

<span data-ttu-id="7adad-335">Een medewerker leveranciers gebruikt de standaard Dynamics 365-functionaliteit om een factuur te maken die moet worden betaald voor de lease buiten Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="7adad-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="7adad-336">In plaats van **Leasekosten** te selecteren als de debetrekening, selecteert de medewerker leveranciers een vereffeningsrekening om de volgende post te genereren.</span><span class="sxs-lookup"><span data-stu-id="7adad-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="7adad-337">Leveranciersproces – 31-1-2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="7adad-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="7adad-338">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="7adad-338">Account type</span></span> | <span data-ttu-id="7adad-339">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-339">Account number</span></span> | <span data-ttu-id="7adad-340">Laag</span><span class="sxs-lookup"><span data-stu-id="7adad-340">Layer</span></span>   | <span data-ttu-id="7adad-341">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-341">Account description</span></span> | <span data-ttu-id="7adad-342">Debet</span><span class="sxs-lookup"><span data-stu-id="7adad-342">Debit</span></span>    | <span data-ttu-id="7adad-343">Krediet</span><span class="sxs-lookup"><span data-stu-id="7adad-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="7adad-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-344">Ledger</span></span>       | <span data-ttu-id="7adad-345">4</span><span class="sxs-lookup"><span data-stu-id="7adad-345">4</span></span>              | <span data-ttu-id="7adad-346">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-346">Current</span></span> | <span data-ttu-id="7adad-347">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="7adad-347">Clearing account</span></span>    | <span data-ttu-id="7adad-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-348">1,000.00</span></span> |          |
| <span data-ttu-id="7adad-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-349">Ledger</span></span>       | <span data-ttu-id="7adad-350">2</span><span class="sxs-lookup"><span data-stu-id="7adad-350">2</span></span>              | <span data-ttu-id="7adad-351">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-351">Current</span></span> | <span data-ttu-id="7adad-352">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="7adad-352">Bank fee</span></span>            | <span data-ttu-id="7adad-353">3.00</span><span class="sxs-lookup"><span data-stu-id="7adad-353">3.00</span></span>     |          |
| <span data-ttu-id="7adad-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-354">Ledger</span></span>       | <span data-ttu-id="7adad-355">3</span><span class="sxs-lookup"><span data-stu-id="7adad-355">3</span></span>              | <span data-ttu-id="7adad-356">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-356">Current</span></span> | <span data-ttu-id="7adad-357">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="7adad-357">VAT expense</span></span>         | <span data-ttu-id="7adad-358">5.00</span><span class="sxs-lookup"><span data-stu-id="7adad-358">5.00</span></span>     |          |
| <span data-ttu-id="7adad-359">Leverancier</span><span class="sxs-lookup"><span data-stu-id="7adad-359">Vendor</span></span>       | <span data-ttu-id="7adad-360">5</span><span class="sxs-lookup"><span data-stu-id="7adad-360">5</span></span>              | <span data-ttu-id="7adad-361">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-361">Current</span></span> | <span data-ttu-id="7adad-362">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="7adad-362">Accounts payable</span></span>    |          | <span data-ttu-id="7adad-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="7adad-363">1,008.00</span></span> |

<span data-ttu-id="7adad-364">Wanneer het overzicht naar de leverancier wordt verzonden, volgt u het normale betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="7adad-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="7adad-365">Tijdens dit proces wordt de volgende journaalpost gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="7adad-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="7adad-366">Contante betaling – 31-1-2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="7adad-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="7adad-367">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="7adad-367">Account type</span></span> | <span data-ttu-id="7adad-368">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-368">Account number</span></span> | <span data-ttu-id="7adad-369">Laag</span><span class="sxs-lookup"><span data-stu-id="7adad-369">Layer</span></span>   | <span data-ttu-id="7adad-370">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-370">Account description</span></span> | <span data-ttu-id="7adad-371">Debet</span><span class="sxs-lookup"><span data-stu-id="7adad-371">Debit</span></span>    | <span data-ttu-id="7adad-372">Krediet</span><span class="sxs-lookup"><span data-stu-id="7adad-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="7adad-373">Leverancier</span><span class="sxs-lookup"><span data-stu-id="7adad-373">Vendor</span></span>       | <span data-ttu-id="7adad-374">5</span><span class="sxs-lookup"><span data-stu-id="7adad-374">5</span></span>              | <span data-ttu-id="7adad-375">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-375">Current</span></span> | <span data-ttu-id="7adad-376">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="7adad-376">Accounts Payable</span></span>    | <span data-ttu-id="7adad-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="7adad-377">1,008.00</span></span> |          |
| <span data-ttu-id="7adad-378">Bank</span><span class="sxs-lookup"><span data-stu-id="7adad-378">Bank</span></span>         | <span data-ttu-id="7adad-379">9</span><span class="sxs-lookup"><span data-stu-id="7adad-379">9</span></span>              | <span data-ttu-id="7adad-380">Huidig</span><span class="sxs-lookup"><span data-stu-id="7adad-380">Current</span></span> | <span data-ttu-id="7adad-381">Contant</span><span class="sxs-lookup"><span data-stu-id="7adad-381">Cash</span></span>                |          | <span data-ttu-id="7adad-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="7adad-382">1,008.00</span></span> |

<span data-ttu-id="7adad-383">U hebt op dit punt volledig verantwoord voor deze lease onder wettelijke rapportagevereisten en kunt een proefbalans genereren met behulp van de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="7adad-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="7adad-384">Het systeem geeft een proefbalans weer met de volgende cijfers.</span><span class="sxs-lookup"><span data-stu-id="7adad-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="7adad-385">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="7adad-386">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="7adad-387">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="7adad-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="7adad-388">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="7adad-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7adad-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="7adad-389">JE-100</span></span></th>
<th><span data-ttu-id="7adad-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="7adad-390">JE-110</span></span></th>
<th><span data-ttu-id="7adad-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="7adad-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7adad-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="7adad-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="7adad-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7adad-395">1</span><span class="sxs-lookup"><span data-stu-id="7adad-395">1</span></span></td>
<td><span data-ttu-id="7adad-396">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="7adad-396">Lease expense</span></span></td>
<td><span data-ttu-id="7adad-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-399">2</span><span class="sxs-lookup"><span data-stu-id="7adad-399">2</span></span></td>
<td><span data-ttu-id="7adad-400">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="7adad-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-401">3.00</span><span class="sxs-lookup"><span data-stu-id="7adad-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-402">3.00</span><span class="sxs-lookup"><span data-stu-id="7adad-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-403">3</span><span class="sxs-lookup"><span data-stu-id="7adad-403">3</span></span></td>
<td><span data-ttu-id="7adad-404">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="7adad-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-405">5.00</span><span class="sxs-lookup"><span data-stu-id="7adad-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-406">5.00</span><span class="sxs-lookup"><span data-stu-id="7adad-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-407">4</span><span class="sxs-lookup"><span data-stu-id="7adad-407">4</span></span></td>
<td><span data-ttu-id="7adad-408">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="7adad-408">Clearing account</span></span></td>
<td><span data-ttu-id="7adad-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="7adad-409">-1,000.00</span></span></td>
<td><span data-ttu-id="7adad-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-411">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-412">5</span><span class="sxs-lookup"><span data-stu-id="7adad-412">5</span></span></td>
<td><span data-ttu-id="7adad-413">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="7adad-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="7adad-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="7adad-414">-1,008.00</span></span></td>
<td><span data-ttu-id="7adad-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="7adad-415">1,008.00</span></span></td>
<td><span data-ttu-id="7adad-416">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-417">6</span><span class="sxs-lookup"><span data-stu-id="7adad-417">6</span></span></td>
<td><span data-ttu-id="7adad-418">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="7adad-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-419">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-420">7</span><span class="sxs-lookup"><span data-stu-id="7adad-420">7</span></span></td>
<td><span data-ttu-id="7adad-421">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="7adad-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-422">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-423">8</span><span class="sxs-lookup"><span data-stu-id="7adad-423">8</span></span></td>
<td><span data-ttu-id="7adad-424">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="7adad-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-425">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-426">9</span><span class="sxs-lookup"><span data-stu-id="7adad-426">9</span></span></td>
<td><span data-ttu-id="7adad-427">Contant</span><span class="sxs-lookup"><span data-stu-id="7adad-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="7adad-428">-1,008.00</span></span></td>
<td><span data-ttu-id="7adad-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="7adad-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-430">10</span><span class="sxs-lookup"><span data-stu-id="7adad-430">10</span></span></td>
<td><span data-ttu-id="7adad-431">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="7adad-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-432">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7adad-433">11</span><span class="sxs-lookup"><span data-stu-id="7adad-433">11</span></span></td>
<td><span data-ttu-id="7adad-434">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="7adad-435">0,00</span><span class="sxs-lookup"><span data-stu-id="7adad-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7adad-436">Als u de IFRS 16 cijfers wilt gebruiken om dezelfde proefbalans uit te voeren, moeten de wettelijke boekhoudingsjournaalposten worden teruggeboekt en moeten de IFRS 16-journaalposten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="7adad-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="7adad-437">Voor het omkeren van de wettelijke journaalposten bevat dit voorbeeld een wettelijk terugboekingsboek met dezelfde instellingen als het wettelijke boek, maar een tegengesteld boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="7adad-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="7adad-438">Het wettelijke boek heeft bijvoorbeeld een leasekostenrekening *gedebiteerd*, maar het terugboekingsboek *crediteert* deze rekening.</span><span class="sxs-lookup"><span data-stu-id="7adad-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="7adad-439">Deze relaties worden eenvoudig gedefinieerd in de boekingsrekeningen Activa leasen op de pagina **Parameters voor activa leasing** (**Activa leasen \> Instellen \> Parameters voor activa leasing**).</span><span class="sxs-lookup"><span data-stu-id="7adad-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="7adad-440">Wanneer hetzelfde proces dat is gebruikt voor het wettelijke boek, wordt gebruikt voor het terugboekingsboek, wordt de volgende journaalpost geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="7adad-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="7adad-441">Het verschil is dat het terugboekingsboek de stornoposten uit het wettelijke boek boekt.</span><span class="sxs-lookup"><span data-stu-id="7adad-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="7adad-442">De stornoposten worden ook in de aangepaste laag aangebracht.</span><span class="sxs-lookup"><span data-stu-id="7adad-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="7adad-443">Wanneer een proefbalans wordt uitgevoerd op de huidige laag, worden de stornojournaalposten niet opgenomen.</span><span class="sxs-lookup"><span data-stu-id="7adad-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="7adad-444">Leasebetaling – 31-1-2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="7adad-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="7adad-445">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="7adad-445">Account type</span></span> | <span data-ttu-id="7adad-446">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-446">Account number</span></span> | <span data-ttu-id="7adad-447">Laag</span><span class="sxs-lookup"><span data-stu-id="7adad-447">Layer</span></span>  | <span data-ttu-id="7adad-448">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-448">Account description</span></span> | <span data-ttu-id="7adad-449">Debet</span><span class="sxs-lookup"><span data-stu-id="7adad-449">Debit</span></span>    | <span data-ttu-id="7adad-450">Krediet</span><span class="sxs-lookup"><span data-stu-id="7adad-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="7adad-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-451">Ledger</span></span>       | <span data-ttu-id="7adad-452">4</span><span class="sxs-lookup"><span data-stu-id="7adad-452">4</span></span>              | <span data-ttu-id="7adad-453">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-453">Custom</span></span> | <span data-ttu-id="7adad-454">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="7adad-454">Clearing account</span></span>    | <span data-ttu-id="7adad-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-455">1,000.00</span></span> |          |
| <span data-ttu-id="7adad-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-456">Ledger</span></span>       | <span data-ttu-id="7adad-457">1</span><span class="sxs-lookup"><span data-stu-id="7adad-457">1</span></span>              | <span data-ttu-id="7adad-458">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-458">Custom</span></span> | <span data-ttu-id="7adad-459">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="7adad-459">Lease expense</span></span>       |          | <span data-ttu-id="7adad-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-460">1,000.00</span></span> |

<span data-ttu-id="7adad-461">Nu u de wettelijk journaalposten hebt verwijderd, worden alle journaalposten geboekt die IFRS 16 vereist in het IFRS 16 boek.</span><span class="sxs-lookup"><span data-stu-id="7adad-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="7adad-462">Deze posten omvatten de eerste toerekening van het RoU activum en de verplichting, en de record van rente en afschrijving.</span><span class="sxs-lookup"><span data-stu-id="7adad-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="7adad-463">Initiële toerekening - 1-1-2020 - JE 140</span><span class="sxs-lookup"><span data-stu-id="7adad-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="7adad-464">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="7adad-464">Account type</span></span> | <span data-ttu-id="7adad-465">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-465">Account number</span></span> | <span data-ttu-id="7adad-466">Laag</span><span class="sxs-lookup"><span data-stu-id="7adad-466">Layer</span></span>  | <span data-ttu-id="7adad-467">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-467">Account description</span></span>      | <span data-ttu-id="7adad-468">Debet</span><span class="sxs-lookup"><span data-stu-id="7adad-468">Debit</span></span>     | <span data-ttu-id="7adad-469">Krediet</span><span class="sxs-lookup"><span data-stu-id="7adad-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="7adad-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-470">Ledger</span></span>       | <span data-ttu-id="7adad-471">6</span><span class="sxs-lookup"><span data-stu-id="7adad-471">6</span></span>              | <span data-ttu-id="7adad-472">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-472">Custom</span></span> | <span data-ttu-id="7adad-473">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="7adad-473">ROU Asset</span></span>                | <span data-ttu-id="7adad-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="7adad-474">22,793.90</span></span> |           |
| <span data-ttu-id="7adad-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-475">Ledger</span></span>       | <span data-ttu-id="7adad-476">7</span><span class="sxs-lookup"><span data-stu-id="7adad-476">7</span></span>              | <span data-ttu-id="7adad-477">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-477">Custom</span></span> | <span data-ttu-id="7adad-478">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="7adad-478">Finance lease obligation</span></span> |           | <span data-ttu-id="7adad-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="7adad-479">22,793.90</span></span> |

<span data-ttu-id="7adad-480">De leasebetaling wordt geboekt zoals de andere leasebetalingen.</span><span class="sxs-lookup"><span data-stu-id="7adad-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="7adad-481">De reden voor het gebruik van de vereffeningsrekening is ervoor te zorgen dat contant geld slechts één keer wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="7adad-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="7adad-482">Leasebetaling – 31-1-2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="7adad-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="7adad-483">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="7adad-483">Account type</span></span> | <span data-ttu-id="7adad-484">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-484">Account number</span></span> | <span data-ttu-id="7adad-485">Laag</span><span class="sxs-lookup"><span data-stu-id="7adad-485">Layer</span></span>  | <span data-ttu-id="7adad-486">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-486">Account description</span></span>      | <span data-ttu-id="7adad-487">Debet</span><span class="sxs-lookup"><span data-stu-id="7adad-487">Debit</span></span>    | <span data-ttu-id="7adad-488">Krediet</span><span class="sxs-lookup"><span data-stu-id="7adad-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="7adad-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-489">Ledger</span></span>       | <span data-ttu-id="7adad-490">7</span><span class="sxs-lookup"><span data-stu-id="7adad-490">7</span></span>              | <span data-ttu-id="7adad-491">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-491">Custom</span></span> | <span data-ttu-id="7adad-492">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="7adad-492">Finance lease obligation</span></span> | <span data-ttu-id="7adad-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-493">1,000.00</span></span> |          |
| <span data-ttu-id="7adad-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-494">Ledger</span></span>       | <span data-ttu-id="7adad-495">4</span><span class="sxs-lookup"><span data-stu-id="7adad-495">4</span></span>              | <span data-ttu-id="7adad-496">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-496">Custom</span></span> | <span data-ttu-id="7adad-497">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="7adad-497">Clearing account</span></span>         |          | <span data-ttu-id="7adad-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7adad-498">1,000.00</span></span> |

<span data-ttu-id="7adad-499">De journaalpost voor rentelasten wordt gegenereerd op basis van het afschrijvingsschema voor verplichtingen.</span><span class="sxs-lookup"><span data-stu-id="7adad-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="7adad-500">Rente-uitgaven - 31-1-2020 - JE 160</span><span class="sxs-lookup"><span data-stu-id="7adad-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="7adad-501">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="7adad-501">Account type</span></span> | <span data-ttu-id="7adad-502">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-502">Account number</span></span> | <span data-ttu-id="7adad-503">Laag</span><span class="sxs-lookup"><span data-stu-id="7adad-503">Layer</span></span>  | <span data-ttu-id="7adad-504">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-504">Account description</span></span>      | <span data-ttu-id="7adad-505">Debet</span><span class="sxs-lookup"><span data-stu-id="7adad-505">Debit</span></span> | <span data-ttu-id="7adad-506">Krediet</span><span class="sxs-lookup"><span data-stu-id="7adad-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="7adad-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-507">Ledger</span></span>       | <span data-ttu-id="7adad-508">8</span><span class="sxs-lookup"><span data-stu-id="7adad-508">8</span></span>              | <span data-ttu-id="7adad-509">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-509">Custom</span></span> | <span data-ttu-id="7adad-510">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="7adad-510">Interest expense</span></span>         | <span data-ttu-id="7adad-511">94.97</span><span class="sxs-lookup"><span data-stu-id="7adad-511">94.97</span></span> |        |
| <span data-ttu-id="7adad-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-512">Ledger</span></span>       | <span data-ttu-id="7adad-513">7</span><span class="sxs-lookup"><span data-stu-id="7adad-513">7</span></span>              | <span data-ttu-id="7adad-514">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-514">Custom</span></span> | <span data-ttu-id="7adad-515">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="7adad-515">Finance lease obligation</span></span> |       | <span data-ttu-id="7adad-516">94.97</span><span class="sxs-lookup"><span data-stu-id="7adad-516">94.97</span></span>  |

<span data-ttu-id="7adad-517">De journaalpost voor afschrijvingskosten wordt gegenereerd op basis van het schema activumafschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="7adad-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="7adad-518">Afschrijvingskosten - 31-1-2020 - JE 170</span><span class="sxs-lookup"><span data-stu-id="7adad-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="7adad-519">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="7adad-519">Account type</span></span> | <span data-ttu-id="7adad-520">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-520">Account number</span></span> | <span data-ttu-id="7adad-521">Laag</span><span class="sxs-lookup"><span data-stu-id="7adad-521">Layer</span></span>  | <span data-ttu-id="7adad-522">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-522">Account description</span></span>      | <span data-ttu-id="7adad-523">Debet</span><span class="sxs-lookup"><span data-stu-id="7adad-523">Debit</span></span>  | <span data-ttu-id="7adad-524">Krediet</span><span class="sxs-lookup"><span data-stu-id="7adad-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="7adad-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-525">Ledger</span></span>       | <span data-ttu-id="7adad-526">10</span><span class="sxs-lookup"><span data-stu-id="7adad-526">10</span></span>             | <span data-ttu-id="7adad-527">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-527">Custom</span></span> | <span data-ttu-id="7adad-528">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="7adad-528">Depreciation expense</span></span>     | <span data-ttu-id="7adad-529">949.75</span><span class="sxs-lookup"><span data-stu-id="7adad-529">949.75</span></span> |        |
| <span data-ttu-id="7adad-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="7adad-530">Ledger</span></span>       | <span data-ttu-id="7adad-531">11</span><span class="sxs-lookup"><span data-stu-id="7adad-531">11</span></span>             | <span data-ttu-id="7adad-532">Aangepast</span><span class="sxs-lookup"><span data-stu-id="7adad-532">Custom</span></span> | <span data-ttu-id="7adad-533">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="7adad-534">949.75</span><span class="sxs-lookup"><span data-stu-id="7adad-534">949.75</span></span> |

<span data-ttu-id="7adad-535">Nadat al deze journaalposten zijn gemaakt en geboekt, ziet u de volgende waarden voor "aangepaste laag 1".</span><span class="sxs-lookup"><span data-stu-id="7adad-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="7adad-536">De laatste kolom bevat de bankkosten, de kosten voor de toegevoegde waarde (btw) en de reductie van contant geld uit de vorige laag, maar bevat niet de journaalposten voor wettelijke rapportage.</span><span class="sxs-lookup"><span data-stu-id="7adad-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="7adad-537">Daarom bereikt u echte mogelijkheden voor dubbele rapportage.</span><span class="sxs-lookup"><span data-stu-id="7adad-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="7adad-538">Op dit punt hoeft het bedrijf alleen zijn proefbalans uit te voeren en de huidige laag en de aangepaste laag combineren om een IFRS-proefbalans te maken.</span><span class="sxs-lookup"><span data-stu-id="7adad-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="7adad-539">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7adad-539">Account No</span></span> | <span data-ttu-id="7adad-540">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-540">Description</span></span>              | <span data-ttu-id="7adad-541">Wettelijk boek\-Huidige laag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="7adad-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="7adad-542">Wettelijk boek\-Huidige laag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="7adad-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="7adad-543">Wettelijk boek\-Huidige laag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="7adad-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="7adad-544">Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="7adad-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="7adad-545">Terugboekingsboek\-Aangepaste laag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="7adad-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="7adad-546">IFRS 16-boek\-Aangepaste laag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="7adad-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="7adad-547">IFRS 16-boek\-Aangepaste laag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="7adad-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="7adad-548">IFRS 16-boek\-Aangepaste laag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="7adad-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="7adad-549">IFRS 16-boek\-Aangepaste laag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="7adad-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="7adad-550">Aangepaste laag \+ Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="7adad-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="7adad-551">1</span><span class="sxs-lookup"><span data-stu-id="7adad-551">1</span></span>          | <span data-ttu-id="7adad-552">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="7adad-552">Lease expense</span></span>            | <span data-ttu-id="7adad-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="7adad-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-554">1,000\.00</span></span>               |   | <span data-ttu-id="7adad-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="7adad-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="7adad-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-556">0\.00</span></span>                                   |
| <span data-ttu-id="7adad-557">2</span><span class="sxs-lookup"><span data-stu-id="7adad-557">2</span></span>          | <span data-ttu-id="7adad-558">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="7adad-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="7adad-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="7adad-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="7adad-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-561">3\.00</span></span>                                   |
| <span data-ttu-id="7adad-562">3</span><span class="sxs-lookup"><span data-stu-id="7adad-562">3</span></span>          | <span data-ttu-id="7adad-563">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="7adad-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="7adad-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="7adad-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="7adad-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-566">5\.00</span></span>                                   |
| <span data-ttu-id="7adad-567">4</span><span class="sxs-lookup"><span data-stu-id="7adad-567">4</span></span>          | <span data-ttu-id="7adad-568">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="7adad-568">Clearing account</span></span>         | <span data-ttu-id="7adad-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="7adad-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="7adad-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-571">0\.00</span></span>                   |   | <span data-ttu-id="7adad-572">1.000</span><span class="sxs-lookup"><span data-stu-id="7adad-572">1,000</span></span>                                           |                                                | <span data-ttu-id="7adad-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="7adad-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="7adad-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-574">0\.00</span></span>                                   |
| <span data-ttu-id="7adad-575">5</span><span class="sxs-lookup"><span data-stu-id="7adad-575">5</span></span>          | <span data-ttu-id="7adad-576">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="7adad-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="7adad-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="7adad-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-578">1,008\.00</span></span>                                         | <span data-ttu-id="7adad-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="7adad-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-580">0\.00</span></span>                                   |
| <span data-ttu-id="7adad-581">6</span><span class="sxs-lookup"><span data-stu-id="7adad-581">6</span></span>          | <span data-ttu-id="7adad-582">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="7adad-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="7adad-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="7adad-584">22,794</span><span class="sxs-lookup"><span data-stu-id="7adad-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="7adad-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="7adad-585">22,793\.90</span></span>                              |
| <span data-ttu-id="7adad-586">7</span><span class="sxs-lookup"><span data-stu-id="7adad-586">7</span></span>          | <span data-ttu-id="7adad-587">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="7adad-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="7adad-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="7adad-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="7adad-589">\-22,794</span></span>                                       | <span data-ttu-id="7adad-590">1.000</span><span class="sxs-lookup"><span data-stu-id="7adad-590">1,000</span></span>                                          | <span data-ttu-id="7adad-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="7adad-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="7adad-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="7adad-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="7adad-593">8</span><span class="sxs-lookup"><span data-stu-id="7adad-593">8</span></span>          | <span data-ttu-id="7adad-594">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="7adad-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="7adad-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="7adad-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="7adad-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="7adad-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="7adad-597">94\.97</span></span>                                  |
| <span data-ttu-id="7adad-598">9</span><span class="sxs-lookup"><span data-stu-id="7adad-598">9</span></span>          | <span data-ttu-id="7adad-599">Contant</span><span class="sxs-lookup"><span data-stu-id="7adad-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="7adad-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="7adad-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="7adad-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="7adad-603">10</span><span class="sxs-lookup"><span data-stu-id="7adad-603">10</span></span>         | <span data-ttu-id="7adad-604">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="7adad-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="7adad-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="7adad-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="7adad-606">949\.75</span></span>                                        | <span data-ttu-id="7adad-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="7adad-607">949\.75</span></span>                                 |
| <span data-ttu-id="7adad-608">11</span><span class="sxs-lookup"><span data-stu-id="7adad-608">11</span></span>         | <span data-ttu-id="7adad-609">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="7adad-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="7adad-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="7adad-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="7adad-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="7adad-611">\-949\.75</span></span>                                      | <span data-ttu-id="7adad-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="7adad-612">\-949\.75</span></span>                               |


