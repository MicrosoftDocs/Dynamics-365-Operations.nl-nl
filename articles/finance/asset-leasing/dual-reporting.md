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
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229545"
---
# <a name="dual-reporting"></a><span data-ttu-id="0ed26-103">Dubbele rapportage</span><span class="sxs-lookup"><span data-stu-id="0ed26-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ed26-104">In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="0ed26-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="0ed26-105">Vertrouwdheid met boekingslagen in Microsoft Dynamics 365 Finance is vereist en maakt het voorbeeld gemakkelijker te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="0ed26-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="0ed26-106">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="0ed26-106">Example</span></span>

<span data-ttu-id="0ed26-107">In het volgende voorbeeld wordt een lease verantwoord onder de Italiaanse wettelijke rapportering door middel van de cash-basis-methode en de IFRS-rapportagemethoden.</span><span class="sxs-lookup"><span data-stu-id="0ed26-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="0ed26-108">Het bedrijf moet drie boeken maken om te verantwoorden voor zowel de Italiaanse wettelijke vereisten als de IFRS 16-vereisten.</span><span class="sxs-lookup"><span data-stu-id="0ed26-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="0ed26-109">Eén boek is vereist voor IFRS 16, één boek is vereist voor wettelijke vereisten en één boek is vereist om de wettelijke boekingen automatisch terug te boeken.</span><span class="sxs-lookup"><span data-stu-id="0ed26-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="0ed26-110">De boeken worden ingesteld, zoals in de volgende tabellen wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0ed26-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="0ed26-111">**IFRS 16-boek**</span><span class="sxs-lookup"><span data-stu-id="0ed26-111">**IFRS 16 book**</span></span>

<span data-ttu-id="0ed26-112">Het IFRS 16 boek is zo ingesteld dat het voldoet aan de IFRS 16-boekhoudnorm.</span><span class="sxs-lookup"><span data-stu-id="0ed26-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="0ed26-113">Alle posten die in dit boek worden geboekt, worden naar een aangepaste laag geboekt.</span><span class="sxs-lookup"><span data-stu-id="0ed26-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="0ed26-114">Naam</span><span class="sxs-lookup"><span data-stu-id="0ed26-114">Name</span></span>                                    | <span data-ttu-id="0ed26-115">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="0ed26-116">Boektype</span><span class="sxs-lookup"><span data-stu-id="0ed26-116">Book type</span></span>                               | <span data-ttu-id="0ed26-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="0ed26-117">IFRS 16</span></span>        |
| <span data-ttu-id="0ed26-118">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-118">Book description</span></span>                        | <span data-ttu-id="0ed26-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="0ed26-119">IFRS 16</span></span>        |
| <span data-ttu-id="0ed26-120">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="0ed26-120">Posting Layer</span></span>                           | <span data-ttu-id="0ed26-121">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="0ed26-121">Custom layer 1</span></span> |
| <span data-ttu-id="0ed26-122">Leasetype</span><span class="sxs-lookup"><span data-stu-id="0ed26-122">Lease Type</span></span>                              | <span data-ttu-id="0ed26-123">Finance</span><span class="sxs-lookup"><span data-stu-id="0ed26-123">Finance</span></span>        |
| <span data-ttu-id="0ed26-124">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="0ed26-124">Accounting Framework</span></span>                    | <span data-ttu-id="0ed26-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="0ed26-125">IFRS 16</span></span>        |
| <span data-ttu-id="0ed26-126">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="0ed26-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="0ed26-127">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-127">0.00</span></span>           |
| <span data-ttu-id="0ed26-128">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="0ed26-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="0ed26-129">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-129">0.00</span></span>           |
| <span data-ttu-id="0ed26-130">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="0ed26-130">Short-term threshold</span></span>                    | <span data-ttu-id="0ed26-131">12</span><span class="sxs-lookup"><span data-stu-id="0ed26-131">12</span></span>             |
| <span data-ttu-id="0ed26-132">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="0ed26-132">Low Value Threshold</span></span>                     | <span data-ttu-id="0ed26-133">5.000,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-133">5,000.00</span></span>       |
| <span data-ttu-id="0ed26-134">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="0ed26-134">Pay to Vendor</span></span>                           | <span data-ttu-id="0ed26-135">No</span><span class="sxs-lookup"><span data-stu-id="0ed26-135">No</span></span>             |

<span data-ttu-id="0ed26-136">**Wettelijk boek**</span><span class="sxs-lookup"><span data-stu-id="0ed26-136">**Statutory book**</span></span>

<span data-ttu-id="0ed26-137">Het wettelijke boek is een cash-basis-boek waar het bedrijf de leasekosten zal verantwoorden als het bedrag aan geld dat maandelijks wordt betaald voor huur.</span><span class="sxs-lookup"><span data-stu-id="0ed26-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="0ed26-138">Dit boek produceert geen RoU-activum of leaseverplichtingen.</span><span class="sxs-lookup"><span data-stu-id="0ed26-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="0ed26-139">Naam</span><span class="sxs-lookup"><span data-stu-id="0ed26-139">Name</span></span>                                    | <span data-ttu-id="0ed26-140">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="0ed26-141">Boektype</span><span class="sxs-lookup"><span data-stu-id="0ed26-141">Book type</span></span>                               | <span data-ttu-id="0ed26-142">Wettelijk</span><span class="sxs-lookup"><span data-stu-id="0ed26-142">Statutory</span></span>   |
| <span data-ttu-id="0ed26-143">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-143">Book description</span></span>                        | <span data-ttu-id="0ed26-144">Lokale GAAP</span><span class="sxs-lookup"><span data-stu-id="0ed26-144">Local GAAP</span></span>  |
| <span data-ttu-id="0ed26-145">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="0ed26-145">Posting Layer</span></span>                           | <span data-ttu-id="0ed26-146">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-146">Current</span></span>     |
| <span data-ttu-id="0ed26-147">Leasetype</span><span class="sxs-lookup"><span data-stu-id="0ed26-147">Lease Type</span></span>                              | <span data-ttu-id="0ed26-148">Automatisch</span><span class="sxs-lookup"><span data-stu-id="0ed26-148">Automatic</span></span>   |
| <span data-ttu-id="0ed26-149">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="0ed26-149">Accounting Framework</span></span>                    | <span data-ttu-id="0ed26-150">Contante basis</span><span class="sxs-lookup"><span data-stu-id="0ed26-150">Cash basis</span></span>  |
| <span data-ttu-id="0ed26-151">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="0ed26-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="0ed26-152">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-152">0.00</span></span>        |
| <span data-ttu-id="0ed26-153">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="0ed26-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="0ed26-154">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-154">0.00</span></span>        |
| <span data-ttu-id="0ed26-155">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="0ed26-155">Short-term threshold</span></span>                    | <span data-ttu-id="0ed26-156">0</span><span class="sxs-lookup"><span data-stu-id="0ed26-156">0</span></span>           |
| <span data-ttu-id="0ed26-157">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="0ed26-157">Low Value Threshold</span></span>                     | <span data-ttu-id="0ed26-158">0</span><span class="sxs-lookup"><span data-stu-id="0ed26-158">0</span></span>           |
| <span data-ttu-id="0ed26-159">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="0ed26-159">Pay to Vendor</span></span>                           | <span data-ttu-id="0ed26-160">No</span><span class="sxs-lookup"><span data-stu-id="0ed26-160">No</span></span>          |

<span data-ttu-id="0ed26-161">**Wettelijk terugboekingsboek**</span><span class="sxs-lookup"><span data-stu-id="0ed26-161">**Statutory reversal book**</span></span>

<span data-ttu-id="0ed26-162">Het wettelijke terugboekingsboek wordt op dezelfde manier ingesteld als het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="0ed26-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="0ed26-163">Naam</span><span class="sxs-lookup"><span data-stu-id="0ed26-163">Name</span></span>                                    | <span data-ttu-id="0ed26-164">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="0ed26-165">Boektype</span><span class="sxs-lookup"><span data-stu-id="0ed26-165">Book type</span></span>                               | <span data-ttu-id="0ed26-166">Wettelijk - terugboeking</span><span class="sxs-lookup"><span data-stu-id="0ed26-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="0ed26-167">Boekomschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-167">Book description</span></span>                        | <span data-ttu-id="0ed26-168">Boek om wettelijk boek terug te boeken</span><span class="sxs-lookup"><span data-stu-id="0ed26-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="0ed26-169">Boekingslaag</span><span class="sxs-lookup"><span data-stu-id="0ed26-169">Posting Layer</span></span>                           | <span data-ttu-id="0ed26-170">Aangepaste laag 1</span><span class="sxs-lookup"><span data-stu-id="0ed26-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="0ed26-171">Leasetype</span><span class="sxs-lookup"><span data-stu-id="0ed26-171">Lease Type</span></span>                              | <span data-ttu-id="0ed26-172">Automatisch</span><span class="sxs-lookup"><span data-stu-id="0ed26-172">Automatic</span></span>                      |
| <span data-ttu-id="0ed26-173">Boekhoudraamwerk</span><span class="sxs-lookup"><span data-stu-id="0ed26-173">Accounting Framework</span></span>                    | <span data-ttu-id="0ed26-174">Contante basis</span><span class="sxs-lookup"><span data-stu-id="0ed26-174">Cash basis</span></span>                     |
| <span data-ttu-id="0ed26-175">Leasetermijn/economische levensduur instellen</span><span class="sxs-lookup"><span data-stu-id="0ed26-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="0ed26-176">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-176">0.00</span></span>                           |
| <span data-ttu-id="0ed26-177">Huidige waarde/reële waarde van activum instellen</span><span class="sxs-lookup"><span data-stu-id="0ed26-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="0ed26-178">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-178">0.00</span></span>                           |
| <span data-ttu-id="0ed26-179">Drempel voor de korte termijn</span><span class="sxs-lookup"><span data-stu-id="0ed26-179">Short-term threshold</span></span>                    | <span data-ttu-id="0ed26-180">0</span><span class="sxs-lookup"><span data-stu-id="0ed26-180">0</span></span>                              |
| <span data-ttu-id="0ed26-181">Drempel voor geringe waarde</span><span class="sxs-lookup"><span data-stu-id="0ed26-181">Low Value Threshold</span></span>                     | <span data-ttu-id="0ed26-182">0</span><span class="sxs-lookup"><span data-stu-id="0ed26-182">0</span></span>                              |
| <span data-ttu-id="0ed26-183">Betalen aan leverancier</span><span class="sxs-lookup"><span data-stu-id="0ed26-183">Pay to Vendor</span></span>                           | <span data-ttu-id="0ed26-184">No</span><span class="sxs-lookup"><span data-stu-id="0ed26-184">No</span></span>                             |

<span data-ttu-id="0ed26-185">Voor dit voorbeeld is er een lease gemaakt met de volgende instellingen op de tabbladen **Algemeen** en **Betalingsschemaregels**.</span><span class="sxs-lookup"><span data-stu-id="0ed26-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="0ed26-186">**Tabblad Algemeen**</span><span class="sxs-lookup"><span data-stu-id="0ed26-186">**General tab**</span></span>

| <span data-ttu-id="0ed26-187">Veld</span><span class="sxs-lookup"><span data-stu-id="0ed26-187">Field</span></span>                      | <span data-ttu-id="0ed26-188">Waarde</span><span class="sxs-lookup"><span data-stu-id="0ed26-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="0ed26-189">Verhoogd leningtarief</span><span class="sxs-lookup"><span data-stu-id="0ed26-189">Incremental borrowing rate</span></span> | <span data-ttu-id="0ed26-190">5%</span><span class="sxs-lookup"><span data-stu-id="0ed26-190">5%</span></span>               |
| <span data-ttu-id="0ed26-191">Begindatum</span><span class="sxs-lookup"><span data-stu-id="0ed26-191">Commencement date</span></span>          | <span data-ttu-id="0ed26-192">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="0ed26-192">1/1/2020</span></span>         |
| <span data-ttu-id="0ed26-193">Leasegroep</span><span class="sxs-lookup"><span data-stu-id="0ed26-193">Lease group</span></span>                | <span data-ttu-id="0ed26-194">Gebouwen</span><span class="sxs-lookup"><span data-stu-id="0ed26-194">Buildings</span></span>        |
| <span data-ttu-id="0ed26-195">Leverancier</span><span class="sxs-lookup"><span data-stu-id="0ed26-195">Vendor</span></span>                     | <span data-ttu-id="0ed26-196">1001</span><span class="sxs-lookup"><span data-stu-id="0ed26-196">1001</span></span>             |
| <span data-ttu-id="0ed26-197">Reële waarde van het activum</span><span class="sxs-lookup"><span data-stu-id="0ed26-197">Fair value of the asset</span></span>    | <span data-ttu-id="0ed26-198">245,000</span><span class="sxs-lookup"><span data-stu-id="0ed26-198">245,000</span></span>          |
| <span data-ttu-id="0ed26-199">Economische levensduur activum</span><span class="sxs-lookup"><span data-stu-id="0ed26-199">Asset useful life</span></span>          | <span data-ttu-id="0ed26-200">120</span><span class="sxs-lookup"><span data-stu-id="0ed26-200">120</span></span>              |
| <span data-ttu-id="0ed26-201">Type annuïteit</span><span class="sxs-lookup"><span data-stu-id="0ed26-201">Annuity type</span></span>               | <span data-ttu-id="0ed26-202">Normale annuïteit</span><span class="sxs-lookup"><span data-stu-id="0ed26-202">Ordinary annuity</span></span> |
| <span data-ttu-id="0ed26-203">Samenstellingsinterval</span><span class="sxs-lookup"><span data-stu-id="0ed26-203">Compounding interval</span></span>       | <span data-ttu-id="0ed26-204">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="0ed26-204">Monthly</span></span>          |

<span data-ttu-id="0ed26-205">**Tabblad Regels van betalingsschema**</span><span class="sxs-lookup"><span data-stu-id="0ed26-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="0ed26-206">Veld</span><span class="sxs-lookup"><span data-stu-id="0ed26-206">Field</span></span>             | <span data-ttu-id="0ed26-207">Waarde</span><span class="sxs-lookup"><span data-stu-id="0ed26-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="0ed26-208">Begindatum</span><span class="sxs-lookup"><span data-stu-id="0ed26-208">Start date</span></span>        | <span data-ttu-id="0ed26-209">1-1-2020</span><span class="sxs-lookup"><span data-stu-id="0ed26-209">1/1/2020</span></span>   |
| <span data-ttu-id="0ed26-210">Periode-interval</span><span class="sxs-lookup"><span data-stu-id="0ed26-210">Period interval</span></span>   | <span data-ttu-id="0ed26-211">Maanden</span><span class="sxs-lookup"><span data-stu-id="0ed26-211">Months</span></span>     |
| <span data-ttu-id="0ed26-212">Perioden</span><span class="sxs-lookup"><span data-stu-id="0ed26-212">Periods</span></span>           | <span data-ttu-id="0ed26-213">24</span><span class="sxs-lookup"><span data-stu-id="0ed26-213">24</span></span>         |
| <span data-ttu-id="0ed26-214">Einddatum</span><span class="sxs-lookup"><span data-stu-id="0ed26-214">End date</span></span>          | <span data-ttu-id="0ed26-215">31-12-2020</span><span class="sxs-lookup"><span data-stu-id="0ed26-215">12/31/2020</span></span> |
| <span data-ttu-id="0ed26-216">Betalingsfrequentie</span><span class="sxs-lookup"><span data-stu-id="0ed26-216">Payment frequency</span></span> | <span data-ttu-id="0ed26-217">Maandelijks</span><span class="sxs-lookup"><span data-stu-id="0ed26-217">Monthly</span></span>    |
| <span data-ttu-id="0ed26-218">Betalingsbedrag</span><span class="sxs-lookup"><span data-stu-id="0ed26-218">Payment amount</span></span>    | <span data-ttu-id="0ed26-219">1.000</span><span class="sxs-lookup"><span data-stu-id="0ed26-219">1,000</span></span>      |

<span data-ttu-id="0ed26-220">Als u deze lease onder twee raamwerken wilt verantwoorden, gebruikt u een huidige boekingslaag en een aangepaste boekingslaag.</span><span class="sxs-lookup"><span data-stu-id="0ed26-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="0ed26-221">In de volgende tabel ziet u een voorbeeld van elke journaalpost die voor elke rapportagestandaard de financiële waarde reëel moet representeren.</span><span class="sxs-lookup"><span data-stu-id="0ed26-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="0ed26-222">Hierna wordt een gedetailleerde omschrijving gegeven van elke journaalpost voor de eerste maand van de lease.</span><span class="sxs-lookup"><span data-stu-id="0ed26-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="0ed26-223">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="0ed26-224">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="0ed26-225">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="0ed26-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="0ed26-226">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="0ed26-226">Current layer total</span></span></th>
<th><span data-ttu-id="0ed26-227">Terugboekingsboek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="0ed26-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="0ed26-228">IFRS 16-boek (aangepaste laag)</span><span class="sxs-lookup"><span data-stu-id="0ed26-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="0ed26-229">Huidige laag + aangepaste laagtotaal</span><span class="sxs-lookup"><span data-stu-id="0ed26-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0ed26-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="0ed26-230">JE-100</span></span></th>
<th><span data-ttu-id="0ed26-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="0ed26-231">JE-110</span></span></th>
<th><span data-ttu-id="0ed26-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="0ed26-232">JE-120</span></span></th>
<th><span data-ttu-id="0ed26-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="0ed26-233">JE-130</span></span></th>
<th><span data-ttu-id="0ed26-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="0ed26-234">JE-140</span></span></th>
<th><span data-ttu-id="0ed26-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="0ed26-235">JE-150</span></span></th>
<th><span data-ttu-id="0ed26-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="0ed26-236">JE-160</span></span></th>
<th><span data-ttu-id="0ed26-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="0ed26-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0ed26-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0ed26-246">1</span><span class="sxs-lookup"><span data-stu-id="0ed26-246">1</span></span></td>
<td><span data-ttu-id="0ed26-247">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="0ed26-247">Lease expense</span></span></td>
<td><span data-ttu-id="0ed26-248">1.000,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-249">1,000.00</span></span></td>
<td><span data-ttu-id="0ed26-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-251">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-252">2</span><span class="sxs-lookup"><span data-stu-id="0ed26-252">2</span></span></td>
<td><span data-ttu-id="0ed26-253">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-254">3,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-255">3.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-256">3.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-257">3</span><span class="sxs-lookup"><span data-stu-id="0ed26-257">3</span></span></td>
<td><span data-ttu-id="0ed26-258">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-259">5.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-260">5.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-261">5.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-262">4</span><span class="sxs-lookup"><span data-stu-id="0ed26-262">4</span></span></td>
<td><span data-ttu-id="0ed26-263">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="0ed26-263">Clearing account</span></span></td>
<td><span data-ttu-id="0ed26-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-264">-1,000.00</span></span></td>
<td><span data-ttu-id="0ed26-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-266">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-266">0.00</span></span></td>
<td><span data-ttu-id="0ed26-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-269">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-270">5</span><span class="sxs-lookup"><span data-stu-id="0ed26-270">5</span></span></td>
<td><span data-ttu-id="0ed26-271">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="0ed26-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-272">-1,008.00</span></span></td>
<td><span data-ttu-id="0ed26-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-273">1,008.00</span></span></td>
<td><span data-ttu-id="0ed26-274">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-275">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-276">6</span><span class="sxs-lookup"><span data-stu-id="0ed26-276">6</span></span></td>
<td><span data-ttu-id="0ed26-277">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="0ed26-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-278">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="0ed26-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-281">7</span><span class="sxs-lookup"><span data-stu-id="0ed26-281">7</span></span></td>
<td><span data-ttu-id="0ed26-282">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="0ed26-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-283">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-284">-22,794.00</span></span></td>
<td><span data-ttu-id="0ed26-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-285">1,000.00</span></span></td>
<td><span data-ttu-id="0ed26-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="0ed26-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="0ed26-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-288">8</span><span class="sxs-lookup"><span data-stu-id="0ed26-288">8</span></span></td>
<td><span data-ttu-id="0ed26-289">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="0ed26-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-290">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-291">94.97</span><span class="sxs-lookup"><span data-stu-id="0ed26-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-292">94.97</span><span class="sxs-lookup"><span data-stu-id="0ed26-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-293">9</span><span class="sxs-lookup"><span data-stu-id="0ed26-293">9</span></span></td>
<td><span data-ttu-id="0ed26-294">Contant</span><span class="sxs-lookup"><span data-stu-id="0ed26-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-295">-1,008.00</span></span></td>
<td><span data-ttu-id="0ed26-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-298">10</span><span class="sxs-lookup"><span data-stu-id="0ed26-298">10</span></span></td>
<td><span data-ttu-id="0ed26-299">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-300">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-301">949.75</span><span class="sxs-lookup"><span data-stu-id="0ed26-301">949.75</span></span></td>
<td><span data-ttu-id="0ed26-302">949.75</span><span class="sxs-lookup"><span data-stu-id="0ed26-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-303">11</span><span class="sxs-lookup"><span data-stu-id="0ed26-303">11</span></span></td>
<td><span data-ttu-id="0ed26-304">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-305">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="0ed26-306">-949.75</span></span></td>
<td><span data-ttu-id="0ed26-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="0ed26-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0ed26-308">Zoals in de bovenstaande tabel wordt aangegeven, moeten drie boeken worden gerapporteerd onder zowel wettelijke als IFRS-rapportage.</span><span class="sxs-lookup"><span data-stu-id="0ed26-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="0ed26-309">In het wettelijke boek wordt de leasebetaling vastgelegd volgens de regels voor cash-basis-boekhouding onder de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="0ed26-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="0ed26-310">Het wettelijke terugboekingsboek keert de wettelijke journaalposten om.</span><span class="sxs-lookup"><span data-stu-id="0ed26-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="0ed26-311">In het IFRS 16 boek worden de journaalposten gemaakt die zijn vereist volgens IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="0ed26-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="0ed26-312">U moet een lease slechts één keer invoeren.</span><span class="sxs-lookup"><span data-stu-id="0ed26-312">You must enter a lease only one time.</span></span> <span data-ttu-id="0ed26-313">Vervolgens kunt u de pagina **Boeken** openen om alle boeken te zien die aan de lease zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="0ed26-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="0ed26-314">Wanneer u de boeken maakt, moeten alle drie aan dezelfde leaserecord zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="0ed26-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="0ed26-315">De eerste journaalpost registreert de leasekosten uit hoofde van het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="0ed26-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="0ed26-316">U kunt de betalingen maken in een batch of door het betalingsschema te selecteren in het wettelijke boek.</span><span class="sxs-lookup"><span data-stu-id="0ed26-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="0ed26-317">Voor dit voorbeeld wordt de volgende journaalpost gemaakt voor het wettelijk boek van het betalingsschema.</span><span class="sxs-lookup"><span data-stu-id="0ed26-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="0ed26-318">Leasebetaling – 31-1-2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="0ed26-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="0ed26-319">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="0ed26-319">Account type</span></span> | <span data-ttu-id="0ed26-320">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-320">Account number</span></span> | <span data-ttu-id="0ed26-321">Laag</span><span class="sxs-lookup"><span data-stu-id="0ed26-321">Layer</span></span>   | <span data-ttu-id="0ed26-322">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-322">Account description</span></span> | <span data-ttu-id="0ed26-323">Debet</span><span class="sxs-lookup"><span data-stu-id="0ed26-323">Debit</span></span>    | <span data-ttu-id="0ed26-324">Krediet</span><span class="sxs-lookup"><span data-stu-id="0ed26-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="0ed26-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-325">Ledger</span></span>       | <span data-ttu-id="0ed26-326">1</span><span class="sxs-lookup"><span data-stu-id="0ed26-326">1</span></span>              | <span data-ttu-id="0ed26-327">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-327">Current</span></span> | <span data-ttu-id="0ed26-328">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="0ed26-328">Lease expense</span></span>       | <span data-ttu-id="0ed26-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-329">1,000.00</span></span> |          |
| <span data-ttu-id="0ed26-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-330">Ledger</span></span>       | <span data-ttu-id="0ed26-331">4</span><span class="sxs-lookup"><span data-stu-id="0ed26-331">4</span></span>              | <span data-ttu-id="0ed26-332">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-332">Current</span></span> | <span data-ttu-id="0ed26-333">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="0ed26-333">Clearing account</span></span>    |          | <span data-ttu-id="0ed26-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-334">1,000.00</span></span> |

<span data-ttu-id="0ed26-335">Een medewerker leveranciers gebruikt de standaard Dynamics 365-functionaliteit om een factuur te maken die moet worden betaald voor de lease buiten Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="0ed26-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="0ed26-336">In plaats van **Leasekosten** te selecteren als de debetrekening, selecteert de medewerker leveranciers een vereffeningsrekening om de volgende post te genereren.</span><span class="sxs-lookup"><span data-stu-id="0ed26-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="0ed26-337">Leveranciersproces – 31-1-2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="0ed26-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="0ed26-338">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="0ed26-338">Account type</span></span> | <span data-ttu-id="0ed26-339">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-339">Account number</span></span> | <span data-ttu-id="0ed26-340">Laag</span><span class="sxs-lookup"><span data-stu-id="0ed26-340">Layer</span></span>   | <span data-ttu-id="0ed26-341">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-341">Account description</span></span> | <span data-ttu-id="0ed26-342">Debet</span><span class="sxs-lookup"><span data-stu-id="0ed26-342">Debit</span></span>    | <span data-ttu-id="0ed26-343">Krediet</span><span class="sxs-lookup"><span data-stu-id="0ed26-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="0ed26-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-344">Ledger</span></span>       | <span data-ttu-id="0ed26-345">4</span><span class="sxs-lookup"><span data-stu-id="0ed26-345">4</span></span>              | <span data-ttu-id="0ed26-346">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-346">Current</span></span> | <span data-ttu-id="0ed26-347">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="0ed26-347">Clearing account</span></span>    | <span data-ttu-id="0ed26-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-348">1,000.00</span></span> |          |
| <span data-ttu-id="0ed26-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-349">Ledger</span></span>       | <span data-ttu-id="0ed26-350">2</span><span class="sxs-lookup"><span data-stu-id="0ed26-350">2</span></span>              | <span data-ttu-id="0ed26-351">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-351">Current</span></span> | <span data-ttu-id="0ed26-352">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-352">Bank fee</span></span>            | <span data-ttu-id="0ed26-353">3.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-353">3.00</span></span>     |          |
| <span data-ttu-id="0ed26-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-354">Ledger</span></span>       | <span data-ttu-id="0ed26-355">3</span><span class="sxs-lookup"><span data-stu-id="0ed26-355">3</span></span>              | <span data-ttu-id="0ed26-356">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-356">Current</span></span> | <span data-ttu-id="0ed26-357">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-357">VAT expense</span></span>         | <span data-ttu-id="0ed26-358">5.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-358">5.00</span></span>     |          |
| <span data-ttu-id="0ed26-359">Leverancier</span><span class="sxs-lookup"><span data-stu-id="0ed26-359">Vendor</span></span>       | <span data-ttu-id="0ed26-360">5</span><span class="sxs-lookup"><span data-stu-id="0ed26-360">5</span></span>              | <span data-ttu-id="0ed26-361">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-361">Current</span></span> | <span data-ttu-id="0ed26-362">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="0ed26-362">Accounts payable</span></span>    |          | <span data-ttu-id="0ed26-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-363">1,008.00</span></span> |

<span data-ttu-id="0ed26-364">Wanneer het overzicht naar de leverancier wordt verzonden, volgt u het normale betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="0ed26-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="0ed26-365">Tijdens dit proces wordt de volgende journaalpost gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0ed26-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="0ed26-366">Contante betaling – 31-1-2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="0ed26-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="0ed26-367">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="0ed26-367">Account type</span></span> | <span data-ttu-id="0ed26-368">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-368">Account number</span></span> | <span data-ttu-id="0ed26-369">Laag</span><span class="sxs-lookup"><span data-stu-id="0ed26-369">Layer</span></span>   | <span data-ttu-id="0ed26-370">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-370">Account description</span></span> | <span data-ttu-id="0ed26-371">Debet</span><span class="sxs-lookup"><span data-stu-id="0ed26-371">Debit</span></span>    | <span data-ttu-id="0ed26-372">Krediet</span><span class="sxs-lookup"><span data-stu-id="0ed26-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="0ed26-373">Leverancier</span><span class="sxs-lookup"><span data-stu-id="0ed26-373">Vendor</span></span>       | <span data-ttu-id="0ed26-374">5</span><span class="sxs-lookup"><span data-stu-id="0ed26-374">5</span></span>              | <span data-ttu-id="0ed26-375">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-375">Current</span></span> | <span data-ttu-id="0ed26-376">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="0ed26-376">Accounts Payable</span></span>    | <span data-ttu-id="0ed26-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-377">1,008.00</span></span> |          |
| <span data-ttu-id="0ed26-378">Bank</span><span class="sxs-lookup"><span data-stu-id="0ed26-378">Bank</span></span>         | <span data-ttu-id="0ed26-379">9</span><span class="sxs-lookup"><span data-stu-id="0ed26-379">9</span></span>              | <span data-ttu-id="0ed26-380">Huidig</span><span class="sxs-lookup"><span data-stu-id="0ed26-380">Current</span></span> | <span data-ttu-id="0ed26-381">Contant</span><span class="sxs-lookup"><span data-stu-id="0ed26-381">Cash</span></span>                |          | <span data-ttu-id="0ed26-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-382">1,008.00</span></span> |

<span data-ttu-id="0ed26-383">U hebt op dit punt volledig verantwoord voor deze lease onder wettelijke rapportagevereisten en kunt een proefbalans genereren met behulp van de huidige laag.</span><span class="sxs-lookup"><span data-stu-id="0ed26-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="0ed26-384">Het systeem geeft een proefbalans weer met de volgende cijfers.</span><span class="sxs-lookup"><span data-stu-id="0ed26-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="0ed26-385">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="0ed26-386">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="0ed26-387">Wettelijk boek (huidige laag)</span><span class="sxs-lookup"><span data-stu-id="0ed26-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="0ed26-388">Huidig laagtotaal</span><span class="sxs-lookup"><span data-stu-id="0ed26-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0ed26-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="0ed26-389">JE-100</span></span></th>
<th><span data-ttu-id="0ed26-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="0ed26-390">JE-110</span></span></th>
<th><span data-ttu-id="0ed26-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="0ed26-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0ed26-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="0ed26-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="0ed26-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0ed26-395">1</span><span class="sxs-lookup"><span data-stu-id="0ed26-395">1</span></span></td>
<td><span data-ttu-id="0ed26-396">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="0ed26-396">Lease expense</span></span></td>
<td><span data-ttu-id="0ed26-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-399">2</span><span class="sxs-lookup"><span data-stu-id="0ed26-399">2</span></span></td>
<td><span data-ttu-id="0ed26-400">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-401">3.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-402">3.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-403">3</span><span class="sxs-lookup"><span data-stu-id="0ed26-403">3</span></span></td>
<td><span data-ttu-id="0ed26-404">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-405">5.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-406">5.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-407">4</span><span class="sxs-lookup"><span data-stu-id="0ed26-407">4</span></span></td>
<td><span data-ttu-id="0ed26-408">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="0ed26-408">Clearing account</span></span></td>
<td><span data-ttu-id="0ed26-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-409">-1,000.00</span></span></td>
<td><span data-ttu-id="0ed26-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-411">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-412">5</span><span class="sxs-lookup"><span data-stu-id="0ed26-412">5</span></span></td>
<td><span data-ttu-id="0ed26-413">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="0ed26-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="0ed26-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-414">-1,008.00</span></span></td>
<td><span data-ttu-id="0ed26-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-415">1,008.00</span></span></td>
<td><span data-ttu-id="0ed26-416">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-417">6</span><span class="sxs-lookup"><span data-stu-id="0ed26-417">6</span></span></td>
<td><span data-ttu-id="0ed26-418">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="0ed26-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-419">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-420">7</span><span class="sxs-lookup"><span data-stu-id="0ed26-420">7</span></span></td>
<td><span data-ttu-id="0ed26-421">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="0ed26-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-422">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-423">8</span><span class="sxs-lookup"><span data-stu-id="0ed26-423">8</span></span></td>
<td><span data-ttu-id="0ed26-424">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="0ed26-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-425">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-426">9</span><span class="sxs-lookup"><span data-stu-id="0ed26-426">9</span></span></td>
<td><span data-ttu-id="0ed26-427">Contant</span><span class="sxs-lookup"><span data-stu-id="0ed26-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-428">-1,008.00</span></span></td>
<td><span data-ttu-id="0ed26-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-430">10</span><span class="sxs-lookup"><span data-stu-id="0ed26-430">10</span></span></td>
<td><span data-ttu-id="0ed26-431">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-432">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0ed26-433">11</span><span class="sxs-lookup"><span data-stu-id="0ed26-433">11</span></span></td>
<td><span data-ttu-id="0ed26-434">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="0ed26-435">0,00</span><span class="sxs-lookup"><span data-stu-id="0ed26-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0ed26-436">Als u de IFRS 16 cijfers wilt gebruiken om dezelfde proefbalans uit te voeren, moeten de wettelijke boekhoudingsjournaalposten worden teruggeboekt en moeten de IFRS 16-journaalposten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="0ed26-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="0ed26-437">Voor het omkeren van de wettelijke journaalposten bevat dit voorbeeld een wettelijk terugboekingsboek met dezelfde instellingen als het wettelijke boek, maar een tegengesteld boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="0ed26-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="0ed26-438">Het wettelijke boek heeft bijvoorbeeld een leasekostenrekening *gedebiteerd*, maar het terugboekingsboek *crediteert* deze rekening.</span><span class="sxs-lookup"><span data-stu-id="0ed26-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="0ed26-439">Deze relaties worden eenvoudig gedefinieerd in de boekingsrekeningen Activa leasen op de pagina **Parameters voor activa leasing** (**Activa leasen \> Instellen \> Parameters voor activa leasing**).</span><span class="sxs-lookup"><span data-stu-id="0ed26-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="0ed26-440">Wanneer hetzelfde proces dat is gebruikt voor het wettelijke boek, wordt gebruikt voor het terugboekingsboek, wordt de volgende journaalpost geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="0ed26-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="0ed26-441">Het verschil is dat het terugboekingsboek de stornoposten uit het wettelijke boek boekt.</span><span class="sxs-lookup"><span data-stu-id="0ed26-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="0ed26-442">De stornoposten worden ook in de aangepaste laag aangebracht.</span><span class="sxs-lookup"><span data-stu-id="0ed26-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="0ed26-443">Wanneer een proefbalans wordt uitgevoerd op de huidige laag, worden de stornojournaalposten niet opgenomen.</span><span class="sxs-lookup"><span data-stu-id="0ed26-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="0ed26-444">Leasebetaling – 31-1-2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="0ed26-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="0ed26-445">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="0ed26-445">Account type</span></span> | <span data-ttu-id="0ed26-446">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-446">Account number</span></span> | <span data-ttu-id="0ed26-447">Laag</span><span class="sxs-lookup"><span data-stu-id="0ed26-447">Layer</span></span>  | <span data-ttu-id="0ed26-448">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-448">Account description</span></span> | <span data-ttu-id="0ed26-449">Debet</span><span class="sxs-lookup"><span data-stu-id="0ed26-449">Debit</span></span>    | <span data-ttu-id="0ed26-450">Krediet</span><span class="sxs-lookup"><span data-stu-id="0ed26-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="0ed26-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-451">Ledger</span></span>       | <span data-ttu-id="0ed26-452">4</span><span class="sxs-lookup"><span data-stu-id="0ed26-452">4</span></span>              | <span data-ttu-id="0ed26-453">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-453">Custom</span></span> | <span data-ttu-id="0ed26-454">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="0ed26-454">Clearing account</span></span>    | <span data-ttu-id="0ed26-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-455">1,000.00</span></span> |          |
| <span data-ttu-id="0ed26-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-456">Ledger</span></span>       | <span data-ttu-id="0ed26-457">1</span><span class="sxs-lookup"><span data-stu-id="0ed26-457">1</span></span>              | <span data-ttu-id="0ed26-458">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-458">Custom</span></span> | <span data-ttu-id="0ed26-459">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="0ed26-459">Lease expense</span></span>       |          | <span data-ttu-id="0ed26-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-460">1,000.00</span></span> |

<span data-ttu-id="0ed26-461">Nu u de wettelijk journaalposten hebt verwijderd, worden alle journaalposten geboekt die IFRS 16 vereist in het IFRS 16 boek.</span><span class="sxs-lookup"><span data-stu-id="0ed26-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="0ed26-462">Deze posten omvatten de eerste toerekening van het RoU activum en de verplichting, en de record van rente en afschrijving.</span><span class="sxs-lookup"><span data-stu-id="0ed26-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="0ed26-463">Initiële toerekening - 1-1-2020 - JE 140</span><span class="sxs-lookup"><span data-stu-id="0ed26-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="0ed26-464">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="0ed26-464">Account type</span></span> | <span data-ttu-id="0ed26-465">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-465">Account number</span></span> | <span data-ttu-id="0ed26-466">Laag</span><span class="sxs-lookup"><span data-stu-id="0ed26-466">Layer</span></span>  | <span data-ttu-id="0ed26-467">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-467">Account description</span></span>      | <span data-ttu-id="0ed26-468">Debet</span><span class="sxs-lookup"><span data-stu-id="0ed26-468">Debit</span></span>     | <span data-ttu-id="0ed26-469">Krediet</span><span class="sxs-lookup"><span data-stu-id="0ed26-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="0ed26-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-470">Ledger</span></span>       | <span data-ttu-id="0ed26-471">6</span><span class="sxs-lookup"><span data-stu-id="0ed26-471">6</span></span>              | <span data-ttu-id="0ed26-472">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-472">Custom</span></span> | <span data-ttu-id="0ed26-473">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="0ed26-473">ROU Asset</span></span>                | <span data-ttu-id="0ed26-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="0ed26-474">22,793.90</span></span> |           |
| <span data-ttu-id="0ed26-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-475">Ledger</span></span>       | <span data-ttu-id="0ed26-476">7</span><span class="sxs-lookup"><span data-stu-id="0ed26-476">7</span></span>              | <span data-ttu-id="0ed26-477">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-477">Custom</span></span> | <span data-ttu-id="0ed26-478">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="0ed26-478">Finance lease obligation</span></span> |           | <span data-ttu-id="0ed26-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="0ed26-479">22,793.90</span></span> |

<span data-ttu-id="0ed26-480">De leasebetaling wordt geboekt zoals de andere leasebetalingen.</span><span class="sxs-lookup"><span data-stu-id="0ed26-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="0ed26-481">De reden voor het gebruik van de vereffeningsrekening is ervoor te zorgen dat contant geld slechts één keer wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="0ed26-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="0ed26-482">Leasebetaling – 31-1-2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="0ed26-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="0ed26-483">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="0ed26-483">Account type</span></span> | <span data-ttu-id="0ed26-484">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-484">Account number</span></span> | <span data-ttu-id="0ed26-485">Laag</span><span class="sxs-lookup"><span data-stu-id="0ed26-485">Layer</span></span>  | <span data-ttu-id="0ed26-486">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-486">Account description</span></span>      | <span data-ttu-id="0ed26-487">Debet</span><span class="sxs-lookup"><span data-stu-id="0ed26-487">Debit</span></span>    | <span data-ttu-id="0ed26-488">Krediet</span><span class="sxs-lookup"><span data-stu-id="0ed26-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="0ed26-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-489">Ledger</span></span>       | <span data-ttu-id="0ed26-490">7</span><span class="sxs-lookup"><span data-stu-id="0ed26-490">7</span></span>              | <span data-ttu-id="0ed26-491">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-491">Custom</span></span> | <span data-ttu-id="0ed26-492">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="0ed26-492">Finance lease obligation</span></span> | <span data-ttu-id="0ed26-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-493">1,000.00</span></span> |          |
| <span data-ttu-id="0ed26-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-494">Ledger</span></span>       | <span data-ttu-id="0ed26-495">4</span><span class="sxs-lookup"><span data-stu-id="0ed26-495">4</span></span>              | <span data-ttu-id="0ed26-496">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-496">Custom</span></span> | <span data-ttu-id="0ed26-497">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="0ed26-497">Clearing account</span></span>         |          | <span data-ttu-id="0ed26-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-498">1,000.00</span></span> |

<span data-ttu-id="0ed26-499">De journaalpost voor rentelasten wordt gegenereerd op basis van het afschrijvingsschema voor verplichtingen.</span><span class="sxs-lookup"><span data-stu-id="0ed26-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="0ed26-500">Rente-uitgaven - 31-1-2020 - JE 160</span><span class="sxs-lookup"><span data-stu-id="0ed26-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="0ed26-501">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="0ed26-501">Account type</span></span> | <span data-ttu-id="0ed26-502">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-502">Account number</span></span> | <span data-ttu-id="0ed26-503">Laag</span><span class="sxs-lookup"><span data-stu-id="0ed26-503">Layer</span></span>  | <span data-ttu-id="0ed26-504">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-504">Account description</span></span>      | <span data-ttu-id="0ed26-505">Debet</span><span class="sxs-lookup"><span data-stu-id="0ed26-505">Debit</span></span> | <span data-ttu-id="0ed26-506">Krediet</span><span class="sxs-lookup"><span data-stu-id="0ed26-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="0ed26-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-507">Ledger</span></span>       | <span data-ttu-id="0ed26-508">8</span><span class="sxs-lookup"><span data-stu-id="0ed26-508">8</span></span>              | <span data-ttu-id="0ed26-509">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-509">Custom</span></span> | <span data-ttu-id="0ed26-510">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="0ed26-510">Interest expense</span></span>         | <span data-ttu-id="0ed26-511">94.97</span><span class="sxs-lookup"><span data-stu-id="0ed26-511">94.97</span></span> |        |
| <span data-ttu-id="0ed26-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-512">Ledger</span></span>       | <span data-ttu-id="0ed26-513">7</span><span class="sxs-lookup"><span data-stu-id="0ed26-513">7</span></span>              | <span data-ttu-id="0ed26-514">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-514">Custom</span></span> | <span data-ttu-id="0ed26-515">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="0ed26-515">Finance lease obligation</span></span> |       | <span data-ttu-id="0ed26-516">94.97</span><span class="sxs-lookup"><span data-stu-id="0ed26-516">94.97</span></span>  |

<span data-ttu-id="0ed26-517">De journaalpost voor afschrijvingskosten wordt gegenereerd op basis van het schema activumafschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="0ed26-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="0ed26-518">Afschrijvingskosten - 31-1-2020 - JE 170</span><span class="sxs-lookup"><span data-stu-id="0ed26-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="0ed26-519">Rekeningtype</span><span class="sxs-lookup"><span data-stu-id="0ed26-519">Account type</span></span> | <span data-ttu-id="0ed26-520">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-520">Account number</span></span> | <span data-ttu-id="0ed26-521">Laag</span><span class="sxs-lookup"><span data-stu-id="0ed26-521">Layer</span></span>  | <span data-ttu-id="0ed26-522">Rekeningbeschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-522">Account description</span></span>      | <span data-ttu-id="0ed26-523">Debet</span><span class="sxs-lookup"><span data-stu-id="0ed26-523">Debit</span></span>  | <span data-ttu-id="0ed26-524">Krediet</span><span class="sxs-lookup"><span data-stu-id="0ed26-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="0ed26-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-525">Ledger</span></span>       | <span data-ttu-id="0ed26-526">10</span><span class="sxs-lookup"><span data-stu-id="0ed26-526">10</span></span>             | <span data-ttu-id="0ed26-527">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-527">Custom</span></span> | <span data-ttu-id="0ed26-528">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-528">Depreciation expense</span></span>     | <span data-ttu-id="0ed26-529">949.75</span><span class="sxs-lookup"><span data-stu-id="0ed26-529">949.75</span></span> |        |
| <span data-ttu-id="0ed26-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="0ed26-530">Ledger</span></span>       | <span data-ttu-id="0ed26-531">11</span><span class="sxs-lookup"><span data-stu-id="0ed26-531">11</span></span>             | <span data-ttu-id="0ed26-532">Aangepast</span><span class="sxs-lookup"><span data-stu-id="0ed26-532">Custom</span></span> | <span data-ttu-id="0ed26-533">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="0ed26-534">949.75</span><span class="sxs-lookup"><span data-stu-id="0ed26-534">949.75</span></span> |

<span data-ttu-id="0ed26-535">Nadat al deze journaalposten zijn gemaakt en geboekt, ziet u de volgende waarden voor "aangepaste laag 1".</span><span class="sxs-lookup"><span data-stu-id="0ed26-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="0ed26-536">De laatste kolom bevat de bankkosten, de kosten voor de toegevoegde waarde (btw) en de reductie van contant geld uit de vorige laag, maar bevat niet de journaalposten voor wettelijke rapportage.</span><span class="sxs-lookup"><span data-stu-id="0ed26-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="0ed26-537">Daarom bereikt u echte mogelijkheden voor dubbele rapportage.</span><span class="sxs-lookup"><span data-stu-id="0ed26-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="0ed26-538">Op dit punt hoeft het bedrijf alleen zijn proefbalans uit te voeren en de huidige laag en de aangepaste laag combineren om een IFRS-proefbalans te maken.</span><span class="sxs-lookup"><span data-stu-id="0ed26-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="0ed26-539">Rekeningnummer</span><span class="sxs-lookup"><span data-stu-id="0ed26-539">Account No</span></span> | <span data-ttu-id="0ed26-540">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-540">Description</span></span>              | <span data-ttu-id="0ed26-541">Wettelijk boek\-Huidige laag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="0ed26-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="0ed26-542">Wettelijk boek\-Huidige laag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="0ed26-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="0ed26-543">Wettelijk boek\-Huidige laag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="0ed26-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="0ed26-544">Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="0ed26-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="0ed26-545">Terugboekingsboek\-Aangepaste laag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="0ed26-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="0ed26-546">IFRS 16-boek\-Aangepaste laag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="0ed26-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="0ed26-547">IFRS 16-boek\-Aangepaste laag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="0ed26-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="0ed26-548">IFRS 16-boek\-Aangepaste laag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="0ed26-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="0ed26-549">IFRS 16-boek\-Aangepaste laag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="0ed26-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="0ed26-550">Aangepaste laag \+ Huidige laag \- Totalen</span><span class="sxs-lookup"><span data-stu-id="0ed26-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="0ed26-551">1</span><span class="sxs-lookup"><span data-stu-id="0ed26-551">1</span></span>          | <span data-ttu-id="0ed26-552">Onkosten van lease</span><span class="sxs-lookup"><span data-stu-id="0ed26-552">Lease expense</span></span>            | <span data-ttu-id="0ed26-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="0ed26-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-554">1,000\.00</span></span>               |   | <span data-ttu-id="0ed26-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="0ed26-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="0ed26-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-556">0\.00</span></span>                                   |
| <span data-ttu-id="0ed26-557">2</span><span class="sxs-lookup"><span data-stu-id="0ed26-557">2</span></span>          | <span data-ttu-id="0ed26-558">Bankkosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="0ed26-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="0ed26-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="0ed26-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-561">3\.00</span></span>                                   |
| <span data-ttu-id="0ed26-562">3</span><span class="sxs-lookup"><span data-stu-id="0ed26-562">3</span></span>          | <span data-ttu-id="0ed26-563">Btw-kosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="0ed26-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="0ed26-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="0ed26-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-566">5\.00</span></span>                                   |
| <span data-ttu-id="0ed26-567">4</span><span class="sxs-lookup"><span data-stu-id="0ed26-567">4</span></span>          | <span data-ttu-id="0ed26-568">Vereffeningsrekening</span><span class="sxs-lookup"><span data-stu-id="0ed26-568">Clearing account</span></span>         | <span data-ttu-id="0ed26-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="0ed26-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="0ed26-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-571">0\.00</span></span>                   |   | <span data-ttu-id="0ed26-572">1.000</span><span class="sxs-lookup"><span data-stu-id="0ed26-572">1,000</span></span>                                           |                                                | <span data-ttu-id="0ed26-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="0ed26-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="0ed26-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-574">0\.00</span></span>                                   |
| <span data-ttu-id="0ed26-575">5</span><span class="sxs-lookup"><span data-stu-id="0ed26-575">5</span></span>          | <span data-ttu-id="0ed26-576">Crediteuren</span><span class="sxs-lookup"><span data-stu-id="0ed26-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="0ed26-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="0ed26-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-578">1,008\.00</span></span>                                         | <span data-ttu-id="0ed26-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="0ed26-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-580">0\.00</span></span>                                   |
| <span data-ttu-id="0ed26-581">6</span><span class="sxs-lookup"><span data-stu-id="0ed26-581">6</span></span>          | <span data-ttu-id="0ed26-582">RoU-activum</span><span class="sxs-lookup"><span data-stu-id="0ed26-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="0ed26-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="0ed26-584">22,794</span><span class="sxs-lookup"><span data-stu-id="0ed26-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="0ed26-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="0ed26-585">22,793\.90</span></span>                              |
| <span data-ttu-id="0ed26-586">7</span><span class="sxs-lookup"><span data-stu-id="0ed26-586">7</span></span>          | <span data-ttu-id="0ed26-587">Financiële leaseverplichting</span><span class="sxs-lookup"><span data-stu-id="0ed26-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="0ed26-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="0ed26-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="0ed26-589">\-22,794</span></span>                                       | <span data-ttu-id="0ed26-590">1.000</span><span class="sxs-lookup"><span data-stu-id="0ed26-590">1,000</span></span>                                          | <span data-ttu-id="0ed26-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="0ed26-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="0ed26-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="0ed26-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="0ed26-593">8</span><span class="sxs-lookup"><span data-stu-id="0ed26-593">8</span></span>          | <span data-ttu-id="0ed26-594">Rente-uitgaven</span><span class="sxs-lookup"><span data-stu-id="0ed26-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="0ed26-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="0ed26-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="0ed26-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="0ed26-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="0ed26-597">94\.97</span></span>                                  |
| <span data-ttu-id="0ed26-598">9</span><span class="sxs-lookup"><span data-stu-id="0ed26-598">9</span></span>          | <span data-ttu-id="0ed26-599">Contant</span><span class="sxs-lookup"><span data-stu-id="0ed26-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="0ed26-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="0ed26-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="0ed26-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="0ed26-603">10</span><span class="sxs-lookup"><span data-stu-id="0ed26-603">10</span></span>         | <span data-ttu-id="0ed26-604">Afschrijvingskosten</span><span class="sxs-lookup"><span data-stu-id="0ed26-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="0ed26-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="0ed26-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="0ed26-606">949\.75</span></span>                                        | <span data-ttu-id="0ed26-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="0ed26-607">949\.75</span></span>                                 |
| <span data-ttu-id="0ed26-608">11</span><span class="sxs-lookup"><span data-stu-id="0ed26-608">11</span></span>         | <span data-ttu-id="0ed26-609">Samengevoegde afschrijving</span><span class="sxs-lookup"><span data-stu-id="0ed26-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="0ed26-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="0ed26-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="0ed26-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="0ed26-611">\-949\.75</span></span>                                      | <span data-ttu-id="0ed26-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="0ed26-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]