---
title: Overheadberekening
description: In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544050"
---
# <a name="overhead-calculation"></a><span data-ttu-id="acc53-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="acc53-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acc53-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="acc53-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="acc53-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="acc53-105">Term definition</span></span>
---------------

<span data-ttu-id="acc53-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="acc53-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="acc53-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="acc53-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="acc53-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="acc53-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="acc53-109">Huur</span><span class="sxs-lookup"><span data-stu-id="acc53-109">Rent</span></span>
-   <span data-ttu-id="acc53-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-110">Electricity</span></span>
-   <span data-ttu-id="acc53-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="acc53-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="acc53-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="acc53-112">Overhead calculation overview</span></span>
<span data-ttu-id="acc53-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="acc53-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="acc53-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="acc53-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="acc53-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="acc53-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="acc53-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="acc53-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="acc53-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="acc53-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="acc53-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="acc53-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="acc53-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="acc53-119">Version type</span></span>
-   <span data-ttu-id="acc53-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="acc53-120">Date and time</span></span>
-   <span data-ttu-id="acc53-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="acc53-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="acc53-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="acc53-122">Fiscal year</span></span>
-   <span data-ttu-id="acc53-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="acc53-123">Fiscal period</span></span>

<span data-ttu-id="acc53-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="acc53-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="acc53-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="acc53-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="acc53-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="acc53-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="acc53-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="acc53-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="acc53-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="acc53-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="acc53-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="acc53-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="acc53-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="acc53-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="acc53-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="acc53-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="acc53-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="acc53-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="acc53-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="acc53-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="acc53-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="acc53-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="acc53-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="acc53-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="acc53-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="acc53-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="acc53-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="acc53-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="acc53-140">Main account</span></span></th>
<th><span data-ttu-id="acc53-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="acc53-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="acc53-143">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-143">CC099</span></span></td>
<td><span data-ttu-id="acc53-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-144">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-145">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-145">10001</span></span></td>
<td><span data-ttu-id="acc53-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-146">Electricity</span></span></td>
<td><span data-ttu-id="acc53-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="acc53-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="acc53-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="acc53-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="acc53-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="acc53-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="acc53-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="acc53-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="acc53-151">Define the cost behavior rule</span></span>

<span data-ttu-id="acc53-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="acc53-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="acc53-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="acc53-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="acc53-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="acc53-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="acc53-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="acc53-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="acc53-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="acc53-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="acc53-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="acc53-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="acc53-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="acc53-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-160">Journal</span></span></th>
<th><span data-ttu-id="acc53-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="acc53-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="acc53-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="acc53-163">Versie</span><span class="sxs-lookup"><span data-stu-id="acc53-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-164">00001</span><span class="sxs-lookup"><span data-stu-id="acc53-164">00001</span></span></td>
<td><span data-ttu-id="acc53-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="acc53-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="acc53-166">Fiscal</span></span></td>
<td><span data-ttu-id="acc53-167">2017</span><span class="sxs-lookup"><span data-stu-id="acc53-167">2017</span></span></td>
<td><span data-ttu-id="acc53-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="acc53-168">Period 1</span></span></td>
<td><span data-ttu-id="acc53-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="acc53-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="acc53-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="acc53-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-173">Cost element</span></span></th>
<th><span data-ttu-id="acc53-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-174">Cost behavior</span></span></th>
<th><span data-ttu-id="acc53-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="acc53-177">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-177">CC099</span></span></td>
<td><span data-ttu-id="acc53-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-178">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-179">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-179">10001</span></span></td>
<td><span data-ttu-id="acc53-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-180">Electricity</span></span></td>
<td><span data-ttu-id="acc53-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="acc53-181">Unclassified</span></span></td>
<td><span data-ttu-id="acc53-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="acc53-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="acc53-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-185">Cost element</span></span></th>
<th><span data-ttu-id="acc53-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-186">Cost behavior</span></span></th>
<th><span data-ttu-id="acc53-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-187">Amount</span></span></th>
<th><span data-ttu-id="acc53-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-189">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-189">CC099</span></span></td>
<td><span data-ttu-id="acc53-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-190">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-191">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-191">10001</span></span></td>
<td><span data-ttu-id="acc53-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-192">Electricity</span></span></td>
<td><span data-ttu-id="acc53-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="acc53-193">Unclassified</span></span></td>
<td><span data-ttu-id="acc53-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-194">10,000.00</span></span></td>
<td><span data-ttu-id="acc53-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-196">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-196">CC099</span></span></td>
<td><span data-ttu-id="acc53-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-197">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-198">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-198">10001</span></span></td>
<td><span data-ttu-id="acc53-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-199">Electricity</span></span></td>
<td><span data-ttu-id="acc53-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="acc53-200">Unclassified</span></span></td>
<td><span data-ttu-id="acc53-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="acc53-201">-10,000.00</span></span></td>
<td><span data-ttu-id="acc53-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-203">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-203">CC099</span></span></td>
<td><span data-ttu-id="acc53-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-204">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-205">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-205">10001</span></span></td>
<td><span data-ttu-id="acc53-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-206">Electricity</span></span></td>
<td><span data-ttu-id="acc53-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-207">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-208">1,000.00</span></span></td>
<td><span data-ttu-id="acc53-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-210">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-210">CC099</span></span></td>
<td><span data-ttu-id="acc53-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-211">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-212">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-212">10001</span></span></td>
<td><span data-ttu-id="acc53-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-213">Electricity</span></span></td>
<td><span data-ttu-id="acc53-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-214">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-215">9,000.00</span></span></td>
<td><span data-ttu-id="acc53-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="acc53-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="acc53-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="acc53-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="acc53-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="acc53-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="acc53-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="acc53-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="acc53-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="acc53-221">Define the cost distribution rule</span></span>

<span data-ttu-id="acc53-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="acc53-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="acc53-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="acc53-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="acc53-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="acc53-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="acc53-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="acc53-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="acc53-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="acc53-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="acc53-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="acc53-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-228">Cost object</span></span></th>
<th><span data-ttu-id="acc53-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="acc53-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-230">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-230">CC001</span></span></td>
<td><span data-ttu-id="acc53-231">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-231">HR</span></span></td>
<td><span data-ttu-id="acc53-232">1.000</span><span class="sxs-lookup"><span data-stu-id="acc53-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-233">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-233">CC002</span></span></td>
<td><span data-ttu-id="acc53-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-234">Finance</span></span></td>
<td><span data-ttu-id="acc53-235">6.000</span><span class="sxs-lookup"><span data-stu-id="acc53-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-236">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-236">CC003</span></span></td>
<td><span data-ttu-id="acc53-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-237">Assembly</span></span></td>
<td><span data-ttu-id="acc53-238">0</span><span class="sxs-lookup"><span data-stu-id="acc53-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="acc53-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-240">Cost object</span></span></th>
<th><span data-ttu-id="acc53-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="acc53-241">Magnitude</span></span></th>
<th><span data-ttu-id="acc53-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="acc53-242">Allocation factor</span></span></th>
<th><span data-ttu-id="acc53-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-244">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-244">CC001</span></span></td>
<td><span data-ttu-id="acc53-245">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-245">HR</span></span></td>
<td><span data-ttu-id="acc53-246">1.000</span><span class="sxs-lookup"><span data-stu-id="acc53-246">1,000</span></span></td>
<td><span data-ttu-id="acc53-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="acc53-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="acc53-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-249">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-249">CC002</span></span></td>
<td><span data-ttu-id="acc53-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-250">Finance</span></span></td>
<td><span data-ttu-id="acc53-251">6.000</span><span class="sxs-lookup"><span data-stu-id="acc53-251">6,000</span></span></td>
<td><span data-ttu-id="acc53-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="acc53-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="acc53-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-254">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-254">CC003</span></span></td>
<td><span data-ttu-id="acc53-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-255">Assembly</span></span></td>
<td><span data-ttu-id="acc53-256">0</span><span class="sxs-lookup"><span data-stu-id="acc53-256">0</span></span></td>
<td><span data-ttu-id="acc53-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="acc53-258">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="acc53-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="acc53-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="acc53-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-261">Cost object</span></span></th>
<th><span data-ttu-id="acc53-262">Formule</span><span class="sxs-lookup"><span data-stu-id="acc53-262">Formula</span></span></th>
<th><span data-ttu-id="acc53-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="acc53-263">Magnitude</span></span></th>
<th><span data-ttu-id="acc53-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="acc53-264">Allocation factor</span></span></th>
<th><span data-ttu-id="acc53-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-266">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-266">CC001</span></span></td>
<td><span data-ttu-id="acc53-267">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-267">HR</span></span></td>
<td><span data-ttu-id="acc53-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="acc53-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="acc53-269">1</span><span class="sxs-lookup"><span data-stu-id="acc53-269">1</span></span></td>
<td><span data-ttu-id="acc53-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="acc53-271">500,00</span><span class="sxs-lookup"><span data-stu-id="acc53-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-272">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-272">CC002</span></span></td>
<td><span data-ttu-id="acc53-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-273">Finance</span></span></td>
<td><span data-ttu-id="acc53-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="acc53-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="acc53-275">1</span><span class="sxs-lookup"><span data-stu-id="acc53-275">1</span></span></td>
<td><span data-ttu-id="acc53-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="acc53-277">500,00</span><span class="sxs-lookup"><span data-stu-id="acc53-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-278">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-278">CC003</span></span></td>
<td><span data-ttu-id="acc53-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-279">Assembly</span></span></td>
<td><span data-ttu-id="acc53-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="acc53-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="acc53-281">0</span><span class="sxs-lookup"><span data-stu-id="acc53-281">0</span></span></td>
<td><span data-ttu-id="acc53-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="acc53-283">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="acc53-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-285">Journal</span></span></th>
<th><span data-ttu-id="acc53-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="acc53-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="acc53-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="acc53-288">Versie</span><span class="sxs-lookup"><span data-stu-id="acc53-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-289">00002</span><span class="sxs-lookup"><span data-stu-id="acc53-289">00002</span></span></td>
<td><span data-ttu-id="acc53-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="acc53-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="acc53-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="acc53-291">Fiscal</span></span></td>
<td><span data-ttu-id="acc53-292">2017</span><span class="sxs-lookup"><span data-stu-id="acc53-292">2017</span></span></td>
<td><span data-ttu-id="acc53-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="acc53-293">Period 1</span></span></td>
<td><span data-ttu-id="acc53-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="acc53-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="acc53-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="acc53-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-298">Cost element</span></span></th>
<th><span data-ttu-id="acc53-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-299">Cost behavior</span></span></th>
<th><span data-ttu-id="acc53-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-302">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-302">CC099</span></span></td>
<td><span data-ttu-id="acc53-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-303">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-304">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-304">10001</span></span></td>
<td><span data-ttu-id="acc53-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-305">Electricity</span></span></td>
<td><span data-ttu-id="acc53-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-306">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-309">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-309">CC099</span></span></td>
<td><span data-ttu-id="acc53-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-310">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-311">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-311">10001</span></span></td>
<td><span data-ttu-id="acc53-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-312">Electricity</span></span></td>
<td><span data-ttu-id="acc53-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-313">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="acc53-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="acc53-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-317">Cost element</span></span></th>
<th><span data-ttu-id="acc53-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-318">Cost behavior</span></span></th>
<th><span data-ttu-id="acc53-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-319">Amount</span></span></th>
<th><span data-ttu-id="acc53-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-321">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-321">CC099</span></span></td>
<td><span data-ttu-id="acc53-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-322">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-323">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-323">10001</span></span></td>
<td><span data-ttu-id="acc53-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-324">Electricity</span></span></td>
<td><span data-ttu-id="acc53-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-325">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="acc53-326">-1,000.00</span></span></td>
<td><span data-ttu-id="acc53-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-328">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-328">CC001</span></span></td>
<td><span data-ttu-id="acc53-329">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-329">HR</span></span></td>
<td><span data-ttu-id="acc53-330">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-330">10001</span></span></td>
<td><span data-ttu-id="acc53-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-331">Electricity</span></span></td>
<td><span data-ttu-id="acc53-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-332">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-333">500,00</span><span class="sxs-lookup"><span data-stu-id="acc53-333">500.00</span></span></td>
<td><span data-ttu-id="acc53-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-335">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-335">CC002</span></span></td>
<td><span data-ttu-id="acc53-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-336">Finance</span></span></td>
<td><span data-ttu-id="acc53-337">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-337">10001</span></span></td>
<td><span data-ttu-id="acc53-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-338">Electricity</span></span></td>
<td><span data-ttu-id="acc53-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-339">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-340">500,00</span><span class="sxs-lookup"><span data-stu-id="acc53-340">500.00</span></span></td>
<td><span data-ttu-id="acc53-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-342">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-342">CC099</span></span></td>
<td><span data-ttu-id="acc53-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="acc53-343">Default cost center</span></span></td>
<td><span data-ttu-id="acc53-344">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-344">10001</span></span></td>
<td><span data-ttu-id="acc53-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-345">Electricity</span></span></td>
<td><span data-ttu-id="acc53-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-346">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="acc53-347">-9,000.00</span></span></td>
<td><span data-ttu-id="acc53-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-349">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-349">CC001</span></span></td>
<td><span data-ttu-id="acc53-350">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-350">HR</span></span></td>
<td><span data-ttu-id="acc53-351">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-351">10001</span></span></td>
<td><span data-ttu-id="acc53-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-352">Electricity</span></span></td>
<td><span data-ttu-id="acc53-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-353">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="acc53-354">1,285.71</span></span></td>
<td><span data-ttu-id="acc53-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-356">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-356">CC002</span></span></td>
<td><span data-ttu-id="acc53-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-357">Finance</span></span></td>
<td><span data-ttu-id="acc53-358">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-358">10001</span></span></td>
<td><span data-ttu-id="acc53-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-359">Electricity</span></span></td>
<td><span data-ttu-id="acc53-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-360">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="acc53-361">7,714.29</span></span></td>
<td><span data-ttu-id="acc53-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="acc53-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="acc53-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="acc53-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="acc53-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="acc53-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="acc53-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="acc53-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="acc53-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="acc53-367">Define the overhead rate</span></span>

<span data-ttu-id="acc53-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="acc53-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="acc53-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="acc53-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-370">Cost object</span></span></th>
<th><span data-ttu-id="acc53-371">Uren</span><span class="sxs-lookup"><span data-stu-id="acc53-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="acc53-372">Proj 1</span></span></td>
<td><span data-ttu-id="acc53-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="acc53-373">Project 1</span></span></td>
<td><span data-ttu-id="acc53-374">3</span><span class="sxs-lookup"><span data-stu-id="acc53-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="acc53-375">Proj 2</span></span></td>
<td><span data-ttu-id="acc53-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="acc53-376">Project 2</span></span></td>
<td><span data-ttu-id="acc53-377">1</span><span class="sxs-lookup"><span data-stu-id="acc53-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="acc53-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-379">Cost object</span></span></th>
<th><span data-ttu-id="acc53-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-380">Cost element</span></span></th>
<th><span data-ttu-id="acc53-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-381">Cost behavior</span></span></th>
<th><span data-ttu-id="acc53-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="acc53-382">Units</span></span></th>
<th><span data-ttu-id="acc53-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="acc53-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-384">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-384">CC001</span></span></td>
<td><span data-ttu-id="acc53-385">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-385">HR</span></span></td>
<td><span data-ttu-id="acc53-386">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-386">10001</span></span></td>
<td><span data-ttu-id="acc53-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-387">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-388">1</span><span class="sxs-lookup"><span data-stu-id="acc53-388">1</span></span></td>
<td><span data-ttu-id="acc53-389">10</span><span class="sxs-lookup"><span data-stu-id="acc53-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="acc53-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-391">Cost object</span></span></th>
<th><span data-ttu-id="acc53-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="acc53-392">Magnitude</span></span></th>
<th><span data-ttu-id="acc53-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-393">Cost element</span></span></th>
<th><span data-ttu-id="acc53-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="acc53-394">Allocation factor</span></span></th>
<th><span data-ttu-id="acc53-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="acc53-396">Proj 1</span></span></td>
<td><span data-ttu-id="acc53-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="acc53-397">Project 1</span></span></td>
<td><span data-ttu-id="acc53-398">3</span><span class="sxs-lookup"><span data-stu-id="acc53-398">3</span></span></td>
<td><span data-ttu-id="acc53-399">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-399">10001</span></span></td>
<td><span data-ttu-id="acc53-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="acc53-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="acc53-401">30,00</span><span class="sxs-lookup"><span data-stu-id="acc53-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="acc53-402">Proj 2</span></span></td>
<td><span data-ttu-id="acc53-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="acc53-403">Project 2</span></span></td>
<td><span data-ttu-id="acc53-404">1</span><span class="sxs-lookup"><span data-stu-id="acc53-404">1</span></span></td>
<td><span data-ttu-id="acc53-405">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-405">10001</span></span></td>
<td><span data-ttu-id="acc53-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="acc53-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="acc53-407">10,00</span><span class="sxs-lookup"><span data-stu-id="acc53-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="acc53-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-409">Journal</span></span></th>
<th><span data-ttu-id="acc53-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="acc53-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="acc53-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="acc53-412">Versie</span><span class="sxs-lookup"><span data-stu-id="acc53-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-413">00003</span><span class="sxs-lookup"><span data-stu-id="acc53-413">00003</span></span></td>
<td><span data-ttu-id="acc53-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="acc53-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="acc53-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="acc53-415">Fiscal</span></span></td>
<td><span data-ttu-id="acc53-416">2017</span><span class="sxs-lookup"><span data-stu-id="acc53-416">2017</span></span></td>
<td><span data-ttu-id="acc53-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="acc53-417">Period 1</span></span></td>
<td><span data-ttu-id="acc53-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="acc53-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="acc53-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="acc53-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-421">Cost object</span></span></th>
<th><span data-ttu-id="acc53-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="acc53-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="acc53-424">Proj 1</span></span></td>
<td><span data-ttu-id="acc53-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="acc53-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="acc53-426">3,00</span><span class="sxs-lookup"><span data-stu-id="acc53-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="acc53-428">Proj 2</span></span></td>
<td><span data-ttu-id="acc53-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="acc53-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="acc53-430">1,00</span><span class="sxs-lookup"><span data-stu-id="acc53-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="acc53-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="acc53-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-433">Cost element</span></span></th>
<th><span data-ttu-id="acc53-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-434">Cost behavior</span></span></th>
<th><span data-ttu-id="acc53-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-435">Amount</span></span></th>
<th><span data-ttu-id="acc53-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="acc53-437">CC0001</span></span></td>
<td><span data-ttu-id="acc53-438">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-438">HR</span></span></td>
<td><span data-ttu-id="acc53-439">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-439">10001</span></span></td>
<td><span data-ttu-id="acc53-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-440">Electricity</span></span></td>
<td><span data-ttu-id="acc53-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-441">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="acc53-442">-30.00</span></span></td>
<td><span data-ttu-id="acc53-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="acc53-444">Proj 1</span></span></td>
<td><span data-ttu-id="acc53-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="acc53-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="acc53-446">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-446">10001</span></span></td>
<td><span data-ttu-id="acc53-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-447">Electricity</span></span></td>
<td><span data-ttu-id="acc53-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-448">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-449">30,00</span><span class="sxs-lookup"><span data-stu-id="acc53-449">30.00</span></span></td>
<td><span data-ttu-id="acc53-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-451">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-451">CC001</span></span></td>
<td><span data-ttu-id="acc53-452">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-452">HR</span></span></td>
<td><span data-ttu-id="acc53-453">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-453">10001</span></span></td>
<td><span data-ttu-id="acc53-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-454">Electricity</span></span></td>
<td><span data-ttu-id="acc53-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-455">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="acc53-456">-10.00</span></span></td>
<td><span data-ttu-id="acc53-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="acc53-458">Proj 2</span></span></td>
<td><span data-ttu-id="acc53-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="acc53-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="acc53-460">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-460">10001</span></span></td>
<td><span data-ttu-id="acc53-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-461">Electricity</span></span></td>
<td><span data-ttu-id="acc53-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-462">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-463">10.00</span><span class="sxs-lookup"><span data-stu-id="acc53-463">10.00</span></span></td>
<td><span data-ttu-id="acc53-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="acc53-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="acc53-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="acc53-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="acc53-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="acc53-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="acc53-468">Finance and Operations ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="acc53-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="acc53-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="acc53-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="acc53-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="acc53-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="acc53-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="acc53-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="acc53-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="acc53-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="acc53-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="acc53-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="acc53-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="acc53-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="acc53-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="acc53-475">Define the cost allocation</span></span>

<span data-ttu-id="acc53-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="acc53-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="acc53-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="acc53-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="acc53-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="acc53-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-479">Cost object</span></span></th>
<th><span data-ttu-id="acc53-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="acc53-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-481">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-481">CC002</span></span></td>
<td><span data-ttu-id="acc53-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-482">Finance</span></span></td>
<td><span data-ttu-id="acc53-483">35</span><span class="sxs-lookup"><span data-stu-id="acc53-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-484">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-484">CC003</span></span></td>
<td><span data-ttu-id="acc53-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-485">Assembly</span></span></td>
<td><span data-ttu-id="acc53-486">55</span><span class="sxs-lookup"><span data-stu-id="acc53-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-487">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-487">CC004</span></span></td>
<td><span data-ttu-id="acc53-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-488">Packaging</span></span></td>
<td><span data-ttu-id="acc53-489">10</span><span class="sxs-lookup"><span data-stu-id="acc53-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="acc53-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="acc53-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="acc53-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-492">Cost object</span></span></th>
<th><span data-ttu-id="acc53-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="acc53-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-494">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-494">CC003</span></span></td>
<td><span data-ttu-id="acc53-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-495">Assembly</span></span></td>
<td><span data-ttu-id="acc53-496">65</span><span class="sxs-lookup"><span data-stu-id="acc53-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-497">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-497">CC004</span></span></td>
<td><span data-ttu-id="acc53-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-498">Packaging</span></span></td>
<td><span data-ttu-id="acc53-499">35</span><span class="sxs-lookup"><span data-stu-id="acc53-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="acc53-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="acc53-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="acc53-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-502">Cost object</span></span></th>
<th><span data-ttu-id="acc53-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="acc53-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-504">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-505">Product 1</span></span></td>
<td><span data-ttu-id="acc53-506">60</span><span class="sxs-lookup"><span data-stu-id="acc53-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-507">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-508">Product 2</span></span></td>
<td><span data-ttu-id="acc53-509">20</span><span class="sxs-lookup"><span data-stu-id="acc53-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="acc53-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="acc53-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="acc53-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-512">Cost object</span></span></th>
<th><span data-ttu-id="acc53-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="acc53-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-514">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-515">Product 1</span></span></td>
<td><span data-ttu-id="acc53-516">80</span><span class="sxs-lookup"><span data-stu-id="acc53-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-517">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-518">Product 2</span></span></td>
<td><span data-ttu-id="acc53-519">15</span><span class="sxs-lookup"><span data-stu-id="acc53-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="acc53-520">In Finance and Operations kunnen statistische metingen, zoals de productie-uren die een product verbruikt, worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="acc53-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="acc53-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="acc53-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="acc53-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="acc53-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-523">Cost object</span></span></th>
<th><span data-ttu-id="acc53-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="acc53-524">Magnitude</span></span></th>
<th><span data-ttu-id="acc53-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="acc53-525">Allocation factor</span></span></th>
<th><span data-ttu-id="acc53-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-526">Amount</span></span></th>
<th><span data-ttu-id="acc53-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-528">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-528">CC002</span></span></td>
<td><span data-ttu-id="acc53-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-529">Finance</span></span></td>
<td><span data-ttu-id="acc53-530">35</span><span class="sxs-lookup"><span data-stu-id="acc53-530">35</span></span></td>
<td><span data-ttu-id="acc53-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="acc53-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="acc53-532">175.00</span><span class="sxs-lookup"><span data-stu-id="acc53-532">175.00</span></span></td>
<td><span data-ttu-id="acc53-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-534">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-534">CC003</span></span></td>
<td><span data-ttu-id="acc53-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-535">Assembly</span></span></td>
<td><span data-ttu-id="acc53-536">55</span><span class="sxs-lookup"><span data-stu-id="acc53-536">55</span></span></td>
<td><span data-ttu-id="acc53-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="acc53-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="acc53-538">275.00</span><span class="sxs-lookup"><span data-stu-id="acc53-538">275.00</span></span></td>
<td><span data-ttu-id="acc53-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-540">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-540">CC004</span></span></td>
<td><span data-ttu-id="acc53-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-541">Packaging</span></span></td>
<td><span data-ttu-id="acc53-542">10</span><span class="sxs-lookup"><span data-stu-id="acc53-542">10</span></span></td>
<td><span data-ttu-id="acc53-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="acc53-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="acc53-544">50,00</span><span class="sxs-lookup"><span data-stu-id="acc53-544">50.00</span></span></td>
<td><span data-ttu-id="acc53-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-546">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-546">CC002</span></span></td>
<td><span data-ttu-id="acc53-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-547">Finance</span></span></td>
<td><span data-ttu-id="acc53-548">35</span><span class="sxs-lookup"><span data-stu-id="acc53-548">35</span></span></td>
<td><span data-ttu-id="acc53-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="acc53-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="acc53-550">436.00</span><span class="sxs-lookup"><span data-stu-id="acc53-550">436.00</span></span></td>
<td><span data-ttu-id="acc53-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-552">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-552">CC003</span></span></td>
<td><span data-ttu-id="acc53-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-553">Assembly</span></span></td>
<td><span data-ttu-id="acc53-554">55</span><span class="sxs-lookup"><span data-stu-id="acc53-554">55</span></span></td>
<td><span data-ttu-id="acc53-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="acc53-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="acc53-556">685.14</span><span class="sxs-lookup"><span data-stu-id="acc53-556">685.14</span></span></td>
<td><span data-ttu-id="acc53-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-558">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-558">CC004</span></span></td>
<td><span data-ttu-id="acc53-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-559">Packaging</span></span></td>
<td><span data-ttu-id="acc53-560">10</span><span class="sxs-lookup"><span data-stu-id="acc53-560">10</span></span></td>
<td><span data-ttu-id="acc53-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="acc53-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="acc53-562">124.57</span><span class="sxs-lookup"><span data-stu-id="acc53-562">124.57</span></span></td>
<td><span data-ttu-id="acc53-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="acc53-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-565">Cost object</span></span></th>
<th><span data-ttu-id="acc53-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="acc53-566">Magnitude</span></span></th>
<th><span data-ttu-id="acc53-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="acc53-567">Allocation factor</span></span></th>
<th><span data-ttu-id="acc53-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-568">Amount</span></span></th>
<th><span data-ttu-id="acc53-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-570">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-570">CC003</span></span></td>
<td><span data-ttu-id="acc53-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-571">Assembly</span></span></td>
<td><span data-ttu-id="acc53-572">65</span><span class="sxs-lookup"><span data-stu-id="acc53-572">65</span></span></td>
<td><span data-ttu-id="acc53-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="acc53-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="acc53-574">438.75</span><span class="sxs-lookup"><span data-stu-id="acc53-574">438.75</span></span></td>
<td><span data-ttu-id="acc53-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-576">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-576">CC004</span></span></td>
<td><span data-ttu-id="acc53-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-577">Packaging</span></span></td>
<td><span data-ttu-id="acc53-578">35</span><span class="sxs-lookup"><span data-stu-id="acc53-578">35</span></span></td>
<td><span data-ttu-id="acc53-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="acc53-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="acc53-580">236.25</span><span class="sxs-lookup"><span data-stu-id="acc53-580">236.25</span></span></td>
<td><span data-ttu-id="acc53-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-582">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-582">CC003</span></span></td>
<td><span data-ttu-id="acc53-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-583">Assembly</span></span></td>
<td><span data-ttu-id="acc53-584">65</span><span class="sxs-lookup"><span data-stu-id="acc53-584">65</span></span></td>
<td><span data-ttu-id="acc53-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="acc53-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="acc53-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="acc53-586">5,297.69</span></span></td>
<td><span data-ttu-id="acc53-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-588">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-588">CC004</span></span></td>
<td><span data-ttu-id="acc53-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-589">Packaging</span></span></td>
<td><span data-ttu-id="acc53-590">35</span><span class="sxs-lookup"><span data-stu-id="acc53-590">35</span></span></td>
<td><span data-ttu-id="acc53-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="acc53-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="acc53-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="acc53-592">2,852.60</span></span></td>
<td><span data-ttu-id="acc53-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="acc53-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-595">Cost object</span></span></th>
<th><span data-ttu-id="acc53-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="acc53-596">Magnitude</span></span></th>
<th><span data-ttu-id="acc53-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="acc53-597">Allocation factor</span></span></th>
<th><span data-ttu-id="acc53-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-598">Amount</span></span></th>
<th><span data-ttu-id="acc53-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-600">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-601">Product 1</span></span></td>
<td><span data-ttu-id="acc53-602">60</span><span class="sxs-lookup"><span data-stu-id="acc53-602">60</span></span></td>
<td><span data-ttu-id="acc53-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="acc53-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="acc53-604">535.31</span><span class="sxs-lookup"><span data-stu-id="acc53-604">535.31</span></span></td>
<td><span data-ttu-id="acc53-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-606">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-607">Product 2</span></span></td>
<td><span data-ttu-id="acc53-608">20</span><span class="sxs-lookup"><span data-stu-id="acc53-608">20</span></span></td>
<td><span data-ttu-id="acc53-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="acc53-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="acc53-610">178.44</span><span class="sxs-lookup"><span data-stu-id="acc53-610">178.44</span></span></td>
<td><span data-ttu-id="acc53-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-612">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-613">Product 1</span></span></td>
<td><span data-ttu-id="acc53-614">60</span><span class="sxs-lookup"><span data-stu-id="acc53-614">60</span></span></td>
<td><span data-ttu-id="acc53-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="acc53-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="acc53-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="acc53-616">4,487.12</span></span></td>
<td><span data-ttu-id="acc53-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-618">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-619">Product 2</span></span></td>
<td><span data-ttu-id="acc53-620">20</span><span class="sxs-lookup"><span data-stu-id="acc53-620">20</span></span></td>
<td><span data-ttu-id="acc53-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="acc53-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="acc53-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="acc53-622">1,495.71</span></span></td>
<td><span data-ttu-id="acc53-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acc53-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="acc53-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-625">Cost object</span></span></th>
<th><span data-ttu-id="acc53-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="acc53-626">Magnitude</span></span></th>
<th><span data-ttu-id="acc53-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="acc53-627">Allocation factor</span></span></th>
<th><span data-ttu-id="acc53-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-628">Amount</span></span></th>
<th><span data-ttu-id="acc53-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-630">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-631">Product 1</span></span></td>
<td><span data-ttu-id="acc53-632">80</span><span class="sxs-lookup"><span data-stu-id="acc53-632">80</span></span></td>
<td><span data-ttu-id="acc53-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="acc53-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="acc53-634">241.05</span><span class="sxs-lookup"><span data-stu-id="acc53-634">241.05</span></span></td>
<td><span data-ttu-id="acc53-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-636">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-637">Product 2</span></span></td>
<td><span data-ttu-id="acc53-638">15</span><span class="sxs-lookup"><span data-stu-id="acc53-638">15</span></span></td>
<td><span data-ttu-id="acc53-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="acc53-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="acc53-640">45.20</span><span class="sxs-lookup"><span data-stu-id="acc53-640">45.20</span></span></td>
<td><span data-ttu-id="acc53-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-642">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-643">Product 1</span></span></td>
<td><span data-ttu-id="acc53-644">80</span><span class="sxs-lookup"><span data-stu-id="acc53-644">80</span></span></td>
<td><span data-ttu-id="acc53-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="acc53-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="acc53-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="acc53-646">2,507.09</span></span></td>
<td><span data-ttu-id="acc53-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-648">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-649">Product 2</span></span></td>
<td><span data-ttu-id="acc53-650">15</span><span class="sxs-lookup"><span data-stu-id="acc53-650">15</span></span></td>
<td><span data-ttu-id="acc53-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="acc53-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="acc53-652">470.08</span><span class="sxs-lookup"><span data-stu-id="acc53-652">470.08</span></span></td>
<td><span data-ttu-id="acc53-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="acc53-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="acc53-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-655">Journal</span></span></th>
<th><span data-ttu-id="acc53-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="acc53-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="acc53-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="acc53-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="acc53-658">Versie</span><span class="sxs-lookup"><span data-stu-id="acc53-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-659">00004</span><span class="sxs-lookup"><span data-stu-id="acc53-659">00004</span></span></td>
<td><span data-ttu-id="acc53-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="acc53-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="acc53-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="acc53-661">Fiscal</span></span></td>
<td><span data-ttu-id="acc53-662">2017</span><span class="sxs-lookup"><span data-stu-id="acc53-662">2017</span></span></td>
<td><span data-ttu-id="acc53-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="acc53-663">Period 1</span></span></td>
<td><span data-ttu-id="acc53-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="acc53-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="acc53-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="acc53-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="acc53-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-668">Cost element</span></span></th>
<th><span data-ttu-id="acc53-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-669">Cost behavior</span></span></th>
<th><span data-ttu-id="acc53-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-672">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-672">CC001</span></span></td>
<td><span data-ttu-id="acc53-673">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-673">HR</span></span></td>
<td><span data-ttu-id="acc53-674">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-674">10001</span></span></td>
<td><span data-ttu-id="acc53-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-675">Electricity</span></span></td>
<td><span data-ttu-id="acc53-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-676">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-677">500,00</span><span class="sxs-lookup"><span data-stu-id="acc53-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-679">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-679">CC001</span></span></td>
<td><span data-ttu-id="acc53-680">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-680">HR</span></span></td>
<td><span data-ttu-id="acc53-681">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-681">10001</span></span></td>
<td><span data-ttu-id="acc53-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-682">Electricity</span></span></td>
<td><span data-ttu-id="acc53-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-683">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="acc53-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-686">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-686">CC002</span></span></td>
<td><span data-ttu-id="acc53-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-687">Finance</span></span></td>
<td><span data-ttu-id="acc53-688">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-688">10001</span></span></td>
<td><span data-ttu-id="acc53-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-689">Electricity</span></span></td>
<td><span data-ttu-id="acc53-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-690">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-691">675.00</span><span class="sxs-lookup"><span data-stu-id="acc53-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-693">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-693">CC002</span></span></td>
<td><span data-ttu-id="acc53-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-694">Finance</span></span></td>
<td><span data-ttu-id="acc53-695">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-695">10001</span></span></td>
<td><span data-ttu-id="acc53-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-696">Electricity</span></span></td>
<td><span data-ttu-id="acc53-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-697">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="acc53-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-700">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-700">CC003</span></span></td>
<td><span data-ttu-id="acc53-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-701">Assembly</span></span></td>
<td><span data-ttu-id="acc53-702">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-702">10001</span></span></td>
<td><span data-ttu-id="acc53-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-703">Electricity</span></span></td>
<td><span data-ttu-id="acc53-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-704">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-705">713.75</span><span class="sxs-lookup"><span data-stu-id="acc53-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-707">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-707">CC003</span></span></td>
<td><span data-ttu-id="acc53-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-708">Assembly</span></span></td>
<td><span data-ttu-id="acc53-709">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-709">10001</span></span></td>
<td><span data-ttu-id="acc53-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-710">Electricity</span></span></td>
<td><span data-ttu-id="acc53-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-711">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="acc53-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-714">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-714">CC003</span></span></td>
<td><span data-ttu-id="acc53-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-715">Packaging</span></span></td>
<td><span data-ttu-id="acc53-716">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-716">10001</span></span></td>
<td><span data-ttu-id="acc53-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-717">Electricity</span></span></td>
<td><span data-ttu-id="acc53-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-718">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-719">286.25</span><span class="sxs-lookup"><span data-stu-id="acc53-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-721">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-721">CC003</span></span></td>
<td><span data-ttu-id="acc53-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-722">Packaging</span></span></td>
<td><span data-ttu-id="acc53-723">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-723">10001</span></span></td>
<td><span data-ttu-id="acc53-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-724">Electricity</span></span></td>
<td><span data-ttu-id="acc53-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-725">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="acc53-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-728">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-729">Product 1</span></span></td>
<td><span data-ttu-id="acc53-730">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-730">10001</span></span></td>
<td><span data-ttu-id="acc53-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-731">Electricity</span></span></td>
<td><span data-ttu-id="acc53-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-732">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-733">776.36</span><span class="sxs-lookup"><span data-stu-id="acc53-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-735">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-736">Product 1</span></span></td>
<td><span data-ttu-id="acc53-737">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-737">10001</span></span></td>
<td><span data-ttu-id="acc53-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-738">Electricity</span></span></td>
<td><span data-ttu-id="acc53-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-739">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="acc53-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-742">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-743">Product 1</span></span></td>
<td><span data-ttu-id="acc53-744">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-744">10001</span></span></td>
<td><span data-ttu-id="acc53-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-745">Electricity</span></span></td>
<td><span data-ttu-id="acc53-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-746">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-747">223.64</span><span class="sxs-lookup"><span data-stu-id="acc53-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="acc53-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-749">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-750">Product 1</span></span></td>
<td><span data-ttu-id="acc53-751">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-751">10001</span></span></td>
<td><span data-ttu-id="acc53-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-752">Electricity</span></span></td>
<td><span data-ttu-id="acc53-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-753">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="acc53-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="acc53-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="acc53-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="acc53-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="acc53-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-757">Cost element</span></span></th>
<th><span data-ttu-id="acc53-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-758">Cost behavior</span></span></th>
<th><span data-ttu-id="acc53-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="acc53-759">Amount</span></span></th>
<th><span data-ttu-id="acc53-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="acc53-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="acc53-761">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-761">CC001</span></span></td>
<td><span data-ttu-id="acc53-762">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-762">HR</span></span></td>
<td><span data-ttu-id="acc53-763">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-763">10001</span></span></td>
<td><span data-ttu-id="acc53-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-764">Electricity</span></span></td>
<td><span data-ttu-id="acc53-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-765">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="acc53-766">-500.00</span></span></td>
<td><span data-ttu-id="acc53-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-768">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-768">CC002</span></span></td>
<td><span data-ttu-id="acc53-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-769">Finance</span></span></td>
<td><span data-ttu-id="acc53-770">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-770">10001</span></span></td>
<td><span data-ttu-id="acc53-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-771">Electricity</span></span></td>
<td><span data-ttu-id="acc53-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-772">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-773">175.00</span><span class="sxs-lookup"><span data-stu-id="acc53-773">175.00</span></span></td>
<td><span data-ttu-id="acc53-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-775">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-775">CC003</span></span></td>
<td><span data-ttu-id="acc53-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-776">Assembly</span></span></td>
<td><span data-ttu-id="acc53-777">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-777">10001</span></span></td>
<td><span data-ttu-id="acc53-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-778">Electricity</span></span></td>
<td><span data-ttu-id="acc53-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-779">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-780">275.00</span><span class="sxs-lookup"><span data-stu-id="acc53-780">275.00</span></span></td>
<td><span data-ttu-id="acc53-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-782">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-782">CC004</span></span></td>
<td><span data-ttu-id="acc53-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-783">Packaging</span></span></td>
<td><span data-ttu-id="acc53-784">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-784">10001</span></span></td>
<td><span data-ttu-id="acc53-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-785">Electricity</span></span></td>
<td><span data-ttu-id="acc53-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-786">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-787">50,00</span><span class="sxs-lookup"><span data-stu-id="acc53-787">50,00</span></span></td>
<td><span data-ttu-id="acc53-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-789">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-789">CC001</span></span></td>
<td><span data-ttu-id="acc53-790">HR</span><span class="sxs-lookup"><span data-stu-id="acc53-790">HR</span></span></td>
<td><span data-ttu-id="acc53-791">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-791">10001</span></span></td>
<td><span data-ttu-id="acc53-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-792">Electricity</span></span></td>
<td><span data-ttu-id="acc53-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-793">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="acc53-794">-1,245.71</span></span></td>
<td><span data-ttu-id="acc53-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-796">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-796">CC002</span></span></td>
<td><span data-ttu-id="acc53-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-797">Finance</span></span></td>
<td><span data-ttu-id="acc53-798">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-798">10001</span></span></td>
<td><span data-ttu-id="acc53-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-799">Electricity</span></span></td>
<td><span data-ttu-id="acc53-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-800">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-801">436.00</span><span class="sxs-lookup"><span data-stu-id="acc53-801">436.00</span></span></td>
<td><span data-ttu-id="acc53-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-803">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-803">CC003</span></span></td>
<td><span data-ttu-id="acc53-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-804">Assembly</span></span></td>
<td><span data-ttu-id="acc53-805">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-805">10001</span></span></td>
<td><span data-ttu-id="acc53-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-806">Electricity</span></span></td>
<td><span data-ttu-id="acc53-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-807">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-808">685.14</span><span class="sxs-lookup"><span data-stu-id="acc53-808">685.14</span></span></td>
<td><span data-ttu-id="acc53-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-810">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-810">CC004</span></span></td>
<td><span data-ttu-id="acc53-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-811">Packaging</span></span></td>
<td><span data-ttu-id="acc53-812">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-812">10001</span></span></td>
<td><span data-ttu-id="acc53-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-813">Electricity</span></span></td>
<td><span data-ttu-id="acc53-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-814">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-815">124.57</span><span class="sxs-lookup"><span data-stu-id="acc53-815">124.57</span></span></td>
<td><span data-ttu-id="acc53-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-817">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-817">CC002</span></span></td>
<td><span data-ttu-id="acc53-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-818">Finance</span></span></td>
<td><span data-ttu-id="acc53-819">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-819">10001</span></span></td>
<td><span data-ttu-id="acc53-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-820">Electricity</span></span></td>
<td><span data-ttu-id="acc53-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-821">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="acc53-822">-675.00</span></span></td>
<td><span data-ttu-id="acc53-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-824">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-824">CC003</span></span></td>
<td><span data-ttu-id="acc53-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-825">Assembly</span></span></td>
<td><span data-ttu-id="acc53-826">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-826">10001</span></span></td>
<td><span data-ttu-id="acc53-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-827">Electricity</span></span></td>
<td><span data-ttu-id="acc53-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-828">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-829">438.75</span><span class="sxs-lookup"><span data-stu-id="acc53-829">438.75</span></span></td>
<td><span data-ttu-id="acc53-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-831">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-831">CC004</span></span></td>
<td><span data-ttu-id="acc53-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-832">Packaging</span></span></td>
<td><span data-ttu-id="acc53-833">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-833">10001</span></span></td>
<td><span data-ttu-id="acc53-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-834">Electricity</span></span></td>
<td><span data-ttu-id="acc53-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-835">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-836">236.25</span><span class="sxs-lookup"><span data-stu-id="acc53-836">236.25</span></span></td>
<td><span data-ttu-id="acc53-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-838">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-838">CC002</span></span></td>
<td><span data-ttu-id="acc53-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="acc53-839">Finance</span></span></td>
<td><span data-ttu-id="acc53-840">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-840">10001</span></span></td>
<td><span data-ttu-id="acc53-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-841">Electricity</span></span></td>
<td><span data-ttu-id="acc53-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-842">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="acc53-843">-8,150.29</span></span></td>
<td><span data-ttu-id="acc53-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-845">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-845">CC003</span></span></td>
<td><span data-ttu-id="acc53-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-846">Assembly</span></span></td>
<td><span data-ttu-id="acc53-847">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-847">10001</span></span></td>
<td><span data-ttu-id="acc53-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-848">Electricity</span></span></td>
<td><span data-ttu-id="acc53-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-849">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="acc53-850">5,297.69</span></span></td>
<td><span data-ttu-id="acc53-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-852">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-852">CC004</span></span></td>
<td><span data-ttu-id="acc53-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="acc53-853">Packaging</span></span></td>
<td><span data-ttu-id="acc53-854">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-854">10001</span></span></td>
<td><span data-ttu-id="acc53-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-855">Electricity</span></span></td>
<td><span data-ttu-id="acc53-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-856">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="acc53-857">2,852.60</span></span></td>
<td><span data-ttu-id="acc53-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-859">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-859">CC003</span></span></td>
<td><span data-ttu-id="acc53-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-860">Assembly</span></span></td>
<td><span data-ttu-id="acc53-861">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-861">10001</span></span></td>
<td><span data-ttu-id="acc53-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-862">Electricity</span></span></td>
<td><span data-ttu-id="acc53-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-863">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="acc53-864">-713.75</span></span></td>
<td><span data-ttu-id="acc53-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-866">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-867">Product 1</span></span></td>
<td><span data-ttu-id="acc53-868">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-868">10001</span></span></td>
<td><span data-ttu-id="acc53-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-869">Electricity</span></span></td>
<td><span data-ttu-id="acc53-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-870">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-871">535.31</span><span class="sxs-lookup"><span data-stu-id="acc53-871">535.31</span></span></td>
<td><span data-ttu-id="acc53-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-873">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-874">Product 2</span></span></td>
<td><span data-ttu-id="acc53-875">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-875">10001</span></span></td>
<td><span data-ttu-id="acc53-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-876">Electricity</span></span></td>
<td><span data-ttu-id="acc53-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-877">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-878">178.44</span><span class="sxs-lookup"><span data-stu-id="acc53-878">178.44</span></span></td>
<td><span data-ttu-id="acc53-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-880">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-880">CC003</span></span></td>
<td><span data-ttu-id="acc53-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-881">Assembly</span></span></td>
<td><span data-ttu-id="acc53-882">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-882">10001</span></span></td>
<td><span data-ttu-id="acc53-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-883">Electricity</span></span></td>
<td><span data-ttu-id="acc53-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-884">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="acc53-885">-5,982.83</span></span></td>
<td><span data-ttu-id="acc53-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-887">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-888">Product 1</span></span></td>
<td><span data-ttu-id="acc53-889">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-889">10001</span></span></td>
<td><span data-ttu-id="acc53-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-890">Electricity</span></span></td>
<td><span data-ttu-id="acc53-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-891">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="acc53-892">4,487.12</span></span></td>
<td><span data-ttu-id="acc53-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-894">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-895">Product 2</span></span></td>
<td><span data-ttu-id="acc53-896">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-896">10001</span></span></td>
<td><span data-ttu-id="acc53-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-897">Electricity</span></span></td>
<td><span data-ttu-id="acc53-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-898">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="acc53-899">1,495.71</span></span></td>
<td><span data-ttu-id="acc53-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-901">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-901">CC003</span></span></td>
<td><span data-ttu-id="acc53-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-902">Assembly</span></span></td>
<td><span data-ttu-id="acc53-903">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-903">10001</span></span></td>
<td><span data-ttu-id="acc53-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-904">Electricity</span></span></td>
<td><span data-ttu-id="acc53-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-905">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="acc53-906">-286.25</span></span></td>
<td><span data-ttu-id="acc53-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-908">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-909">Product 1</span></span></td>
<td><span data-ttu-id="acc53-910">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-910">10001</span></span></td>
<td><span data-ttu-id="acc53-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-911">Electricity</span></span></td>
<td><span data-ttu-id="acc53-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-912">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-913">241.05</span><span class="sxs-lookup"><span data-stu-id="acc53-913">241.05</span></span></td>
<td><span data-ttu-id="acc53-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-915">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-916">Product 2</span></span></td>
<td><span data-ttu-id="acc53-917">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-917">10001</span></span></td>
<td><span data-ttu-id="acc53-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-918">Electricity</span></span></td>
<td><span data-ttu-id="acc53-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-919">Fixed cost</span></span></td>
<td><span data-ttu-id="acc53-920">45.20</span><span class="sxs-lookup"><span data-stu-id="acc53-920">45.20</span></span></td>
<td><span data-ttu-id="acc53-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-922">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-922">CC003</span></span></td>
<td><span data-ttu-id="acc53-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="acc53-923">Assembly</span></span></td>
<td><span data-ttu-id="acc53-924">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-924">10001</span></span></td>
<td><span data-ttu-id="acc53-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-925">Electricity</span></span></td>
<td><span data-ttu-id="acc53-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-926">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="acc53-927">-2,977.17</span></span></td>
<td><span data-ttu-id="acc53-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-929">Prod 1</span></span></td>
<td><span data-ttu-id="acc53-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="acc53-930">Product 1</span></span></td>
<td><span data-ttu-id="acc53-931">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-931">10001</span></span></td>
<td><span data-ttu-id="acc53-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-932">Electricity</span></span></td>
<td><span data-ttu-id="acc53-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-933">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="acc53-934">2,507.09</span></span></td>
<td><span data-ttu-id="acc53-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="acc53-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-936">Prod 2</span></span></td>
<td><span data-ttu-id="acc53-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="acc53-937">Product 2</span></span></td>
<td><span data-ttu-id="acc53-938">10001</span><span class="sxs-lookup"><span data-stu-id="acc53-938">10001</span></span></td>
<td><span data-ttu-id="acc53-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-939">Electricity</span></span></td>
<td><span data-ttu-id="acc53-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-940">Variable cost</span></span></td>
<td><span data-ttu-id="acc53-941">470.08</span><span class="sxs-lookup"><span data-stu-id="acc53-941">470.08</span></span></td>
<td><span data-ttu-id="acc53-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="acc53-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="acc53-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="acc53-943">Conclusion</span></span>
<span data-ttu-id="acc53-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="acc53-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="acc53-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="acc53-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="acc53-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="acc53-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="acc53-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="acc53-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="acc53-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="acc53-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="acc53-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="acc53-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="acc53-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="acc53-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="acc53-951">CC099</span><span class="sxs-lookup"><span data-stu-id="acc53-951">CC099</span></span></th>
<th><span data-ttu-id="acc53-952">CC001</span><span class="sxs-lookup"><span data-stu-id="acc53-952">CC001</span></span></th>
<th><span data-ttu-id="acc53-953">CC002</span><span class="sxs-lookup"><span data-stu-id="acc53-953">CC002</span></span></th>
<th><span data-ttu-id="acc53-954">CC003</span><span class="sxs-lookup"><span data-stu-id="acc53-954">CC003</span></span></th>
<th><span data-ttu-id="acc53-955">CC004</span><span class="sxs-lookup"><span data-stu-id="acc53-955">CC004</span></span></th>
<th><span data-ttu-id="acc53-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="acc53-956">Proj 1</span></span></th>
<th><span data-ttu-id="acc53-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="acc53-957">Proj 2</span></span></th>
<th><span data-ttu-id="acc53-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="acc53-958">Prod 1</span></span></th>
<th><span data-ttu-id="acc53-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="acc53-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="acc53-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="acc53-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="acc53-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="acc53-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="acc53-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-971">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="acc53-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-973">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-974">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-975">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-976">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-977">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="acc53-978">776.36</span><span class="sxs-lookup"><span data-stu-id="acc53-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-979">223.64</span><span class="sxs-lookup"><span data-stu-id="acc53-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="acc53-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="acc53-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-982">000</span><span class="sxs-lookup"><span data-stu-id="acc53-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-983">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-984">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-985">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-986">0,00</span><span class="sxs-lookup"><span data-stu-id="acc53-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-987">30,00</span><span class="sxs-lookup"><span data-stu-id="acc53-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-988">10,00</span><span class="sxs-lookup"><span data-stu-id="acc53-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="acc53-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="acc53-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="acc53-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="acc53-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="acc53-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="acc53-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="acc53-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="acc53-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="acc53-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="acc53-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="acc53-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="acc53-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="acc53-996">Zie [Kostentotalisatie](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="acc53-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



