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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009513"
---
# <a name="overhead-calculation"></a><span data-ttu-id="bd8ce-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="bd8ce-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd8ce-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="bd8ce-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="bd8ce-105">Term definition</span></span>
---------------

<span data-ttu-id="bd8ce-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="bd8ce-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="bd8ce-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="bd8ce-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="bd8ce-109">Huur</span><span class="sxs-lookup"><span data-stu-id="bd8ce-109">Rent</span></span>
-   <span data-ttu-id="bd8ce-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-110">Electricity</span></span>
-   <span data-ttu-id="bd8ce-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="bd8ce-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="bd8ce-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="bd8ce-112">Overhead calculation overview</span></span>
<span data-ttu-id="bd8ce-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="bd8ce-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="bd8ce-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="bd8ce-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="bd8ce-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="bd8ce-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="bd8ce-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="bd8ce-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="bd8ce-119">Version type</span></span>
-   <span data-ttu-id="bd8ce-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="bd8ce-120">Date and time</span></span>
-   <span data-ttu-id="bd8ce-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="bd8ce-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="bd8ce-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="bd8ce-122">Fiscal year</span></span>
-   <span data-ttu-id="bd8ce-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="bd8ce-123">Fiscal period</span></span>

<span data-ttu-id="bd8ce-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="bd8ce-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="bd8ce-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="bd8ce-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="bd8ce-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="bd8ce-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="bd8ce-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="bd8ce-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="bd8ce-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="bd8ce-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="bd8ce-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="bd8ce-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="bd8ce-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="bd8ce-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="bd8ce-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="bd8ce-140">Main account</span></span></th>
<th><span data-ttu-id="bd8ce-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="bd8ce-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-143">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-143">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-144">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-145">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-145">10001</span></span></td>
<td><span data-ttu-id="bd8ce-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-146">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="bd8ce-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="bd8ce-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="bd8ce-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="bd8ce-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="bd8ce-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-151">Define the cost behavior rule</span></span>

<span data-ttu-id="bd8ce-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="bd8ce-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="bd8ce-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="bd8ce-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="bd8ce-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="bd8ce-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="bd8ce-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="bd8ce-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="bd8ce-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="bd8ce-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="bd8ce-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="bd8ce-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-160">Journal</span></span></th>
<th><span data-ttu-id="bd8ce-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bd8ce-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bd8ce-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bd8ce-163">Versie</span><span class="sxs-lookup"><span data-stu-id="bd8ce-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-164">00001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-164">00001</span></span></td>
<td><span data-ttu-id="bd8ce-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="bd8ce-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-166">Fiscal</span></span></td>
<td><span data-ttu-id="bd8ce-167">2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-167">2017</span></span></td>
<td><span data-ttu-id="bd8ce-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-168">Period 1</span></span></td>
<td><span data-ttu-id="bd8ce-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bd8ce-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-173">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-174">Cost behavior</span></span></th>
<th><span data-ttu-id="bd8ce-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-177">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-177">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-178">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-179">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-179">10001</span></span></td>
<td><span data-ttu-id="bd8ce-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-180">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="bd8ce-181">Unclassified</span></span></td>
<td><span data-ttu-id="bd8ce-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bd8ce-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="bd8ce-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-185">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-186">Cost behavior</span></span></th>
<th><span data-ttu-id="bd8ce-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-187">Amount</span></span></th>
<th><span data-ttu-id="bd8ce-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-189">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-189">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-190">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-191">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-191">10001</span></span></td>
<td><span data-ttu-id="bd8ce-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-192">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="bd8ce-193">Unclassified</span></span></td>
<td><span data-ttu-id="bd8ce-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-194">10,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-196">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-196">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-197">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-198">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-198">10001</span></span></td>
<td><span data-ttu-id="bd8ce-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-199">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="bd8ce-200">Unclassified</span></span></td>
<td><span data-ttu-id="bd8ce-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-201">-10,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-203">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-203">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-204">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-205">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-205">10001</span></span></td>
<td><span data-ttu-id="bd8ce-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-206">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-207">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-208">1,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-210">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-210">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-211">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-212">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-212">10001</span></span></td>
<td><span data-ttu-id="bd8ce-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-213">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-214">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-215">9,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="bd8ce-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="bd8ce-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="bd8ce-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="bd8ce-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="bd8ce-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-221">Define the cost distribution rule</span></span>

<span data-ttu-id="bd8ce-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="bd8ce-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="bd8ce-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="bd8ce-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="bd8ce-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="bd8ce-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="bd8ce-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-228">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="bd8ce-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-230">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-230">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-231">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-231">HR</span></span></td>
<td><span data-ttu-id="bd8ce-232">1.000</span><span class="sxs-lookup"><span data-stu-id="bd8ce-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-233">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-233">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-234">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-235">6.000</span><span class="sxs-lookup"><span data-stu-id="bd8ce-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-236">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-236">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-237">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-238">0</span><span class="sxs-lookup"><span data-stu-id="bd8ce-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-240">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="bd8ce-241">Magnitude</span></span></th>
<th><span data-ttu-id="bd8ce-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="bd8ce-242">Allocation factor</span></span></th>
<th><span data-ttu-id="bd8ce-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-244">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-244">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-245">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-245">HR</span></span></td>
<td><span data-ttu-id="bd8ce-246">1.000</span><span class="sxs-lookup"><span data-stu-id="bd8ce-246">1,000</span></span></td>
<td><span data-ttu-id="bd8ce-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-249">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-249">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-250">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-251">6.000</span><span class="sxs-lookup"><span data-stu-id="bd8ce-251">6,000</span></span></td>
<td><span data-ttu-id="bd8ce-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="bd8ce-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-254">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-254">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-255">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-256">0</span><span class="sxs-lookup"><span data-stu-id="bd8ce-256">0</span></span></td>
<td><span data-ttu-id="bd8ce-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-258">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="bd8ce-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-261">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-262">Formule</span><span class="sxs-lookup"><span data-stu-id="bd8ce-262">Formula</span></span></th>
<th><span data-ttu-id="bd8ce-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="bd8ce-263">Magnitude</span></span></th>
<th><span data-ttu-id="bd8ce-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="bd8ce-264">Allocation factor</span></span></th>
<th><span data-ttu-id="bd8ce-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-266">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-266">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-267">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-267">HR</span></span></td>
<td><span data-ttu-id="bd8ce-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bd8ce-269">1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-269">1</span></span></td>
<td><span data-ttu-id="bd8ce-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-271">500,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-272">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-272">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-273">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bd8ce-275">1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-275">1</span></span></td>
<td><span data-ttu-id="bd8ce-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-277">500,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-278">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-278">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-279">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="bd8ce-281">0</span><span class="sxs-lookup"><span data-stu-id="bd8ce-281">0</span></span></td>
<td><span data-ttu-id="bd8ce-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-283">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="bd8ce-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-285">Journal</span></span></th>
<th><span data-ttu-id="bd8ce-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bd8ce-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bd8ce-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bd8ce-288">Versie</span><span class="sxs-lookup"><span data-stu-id="bd8ce-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-289">00002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-289">00002</span></span></td>
<td><span data-ttu-id="bd8ce-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="bd8ce-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="bd8ce-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-291">Fiscal</span></span></td>
<td><span data-ttu-id="bd8ce-292">2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-292">2017</span></span></td>
<td><span data-ttu-id="bd8ce-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-293">Period 1</span></span></td>
<td><span data-ttu-id="bd8ce-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bd8ce-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-298">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-299">Cost behavior</span></span></th>
<th><span data-ttu-id="bd8ce-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-302">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-302">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-303">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-304">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-304">10001</span></span></td>
<td><span data-ttu-id="bd8ce-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-305">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-306">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-309">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-309">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-310">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-311">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-311">10001</span></span></td>
<td><span data-ttu-id="bd8ce-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-312">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-313">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bd8ce-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="bd8ce-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-317">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-318">Cost behavior</span></span></th>
<th><span data-ttu-id="bd8ce-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-319">Amount</span></span></th>
<th><span data-ttu-id="bd8ce-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-321">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-321">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-322">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-323">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-323">10001</span></span></td>
<td><span data-ttu-id="bd8ce-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-324">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-325">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-326">-1,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-328">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-328">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-329">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-329">HR</span></span></td>
<td><span data-ttu-id="bd8ce-330">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-330">10001</span></span></td>
<td><span data-ttu-id="bd8ce-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-331">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-332">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-333">500,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-333">500.00</span></span></td>
<td><span data-ttu-id="bd8ce-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-335">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-335">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-336">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-337">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-337">10001</span></span></td>
<td><span data-ttu-id="bd8ce-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-338">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-339">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-340">500,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-340">500.00</span></span></td>
<td><span data-ttu-id="bd8ce-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-342">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-342">CC099</span></span></td>
<td><span data-ttu-id="bd8ce-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="bd8ce-343">Default cost center</span></span></td>
<td><span data-ttu-id="bd8ce-344">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-344">10001</span></span></td>
<td><span data-ttu-id="bd8ce-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-345">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-346">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-347">-9,000.00</span></span></td>
<td><span data-ttu-id="bd8ce-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-349">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-349">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-350">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-350">HR</span></span></td>
<td><span data-ttu-id="bd8ce-351">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-351">10001</span></span></td>
<td><span data-ttu-id="bd8ce-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-352">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-353">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-354">1,285.71</span></span></td>
<td><span data-ttu-id="bd8ce-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-356">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-356">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-357">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-358">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-358">10001</span></span></td>
<td><span data-ttu-id="bd8ce-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-359">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-360">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="bd8ce-361">7,714.29</span></span></td>
<td><span data-ttu-id="bd8ce-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="bd8ce-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="bd8ce-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="bd8ce-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="bd8ce-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="bd8ce-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-367">Define the overhead rate</span></span>

<span data-ttu-id="bd8ce-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="bd8ce-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-370">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-371">Uren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-372">Proj 1</span></span></td>
<td><span data-ttu-id="bd8ce-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-373">Project 1</span></span></td>
<td><span data-ttu-id="bd8ce-374">3</span><span class="sxs-lookup"><span data-stu-id="bd8ce-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-375">Proj 2</span></span></td>
<td><span data-ttu-id="bd8ce-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-376">Project 2</span></span></td>
<td><span data-ttu-id="bd8ce-377">1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-379">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-380">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-381">Cost behavior</span></span></th>
<th><span data-ttu-id="bd8ce-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="bd8ce-382">Units</span></span></th>
<th><span data-ttu-id="bd8ce-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="bd8ce-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-384">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-384">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-385">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-385">HR</span></span></td>
<td><span data-ttu-id="bd8ce-386">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-386">10001</span></span></td>
<td><span data-ttu-id="bd8ce-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-387">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-388">1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-388">1</span></span></td>
<td><span data-ttu-id="bd8ce-389">10</span><span class="sxs-lookup"><span data-stu-id="bd8ce-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-391">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="bd8ce-392">Magnitude</span></span></th>
<th><span data-ttu-id="bd8ce-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-393">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="bd8ce-394">Allocation factor</span></span></th>
<th><span data-ttu-id="bd8ce-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-396">Proj 1</span></span></td>
<td><span data-ttu-id="bd8ce-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-397">Project 1</span></span></td>
<td><span data-ttu-id="bd8ce-398">3</span><span class="sxs-lookup"><span data-stu-id="bd8ce-398">3</span></span></td>
<td><span data-ttu-id="bd8ce-399">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-399">10001</span></span></td>
<td><span data-ttu-id="bd8ce-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="bd8ce-401">30,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-402">Proj 2</span></span></td>
<td><span data-ttu-id="bd8ce-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-403">Project 2</span></span></td>
<td><span data-ttu-id="bd8ce-404">1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-404">1</span></span></td>
<td><span data-ttu-id="bd8ce-405">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-405">10001</span></span></td>
<td><span data-ttu-id="bd8ce-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="bd8ce-407">10,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="bd8ce-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-409">Journal</span></span></th>
<th><span data-ttu-id="bd8ce-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bd8ce-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bd8ce-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bd8ce-412">Versie</span><span class="sxs-lookup"><span data-stu-id="bd8ce-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-413">00003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-413">00003</span></span></td>
<td><span data-ttu-id="bd8ce-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="bd8ce-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="bd8ce-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-415">Fiscal</span></span></td>
<td><span data-ttu-id="bd8ce-416">2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-416">2017</span></span></td>
<td><span data-ttu-id="bd8ce-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-417">Period 1</span></span></td>
<td><span data-ttu-id="bd8ce-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="bd8ce-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-421">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="bd8ce-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-424">Proj 1</span></span></td>
<td><span data-ttu-id="bd8ce-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="bd8ce-426">3,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-428">Proj 2</span></span></td>
<td><span data-ttu-id="bd8ce-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="bd8ce-430">1,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bd8ce-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="bd8ce-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-433">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-434">Cost behavior</span></span></th>
<th><span data-ttu-id="bd8ce-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-435">Amount</span></span></th>
<th><span data-ttu-id="bd8ce-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-437">CC0001</span></span></td>
<td><span data-ttu-id="bd8ce-438">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-438">HR</span></span></td>
<td><span data-ttu-id="bd8ce-439">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-439">10001</span></span></td>
<td><span data-ttu-id="bd8ce-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-440">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-441">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-442">-30.00</span></span></td>
<td><span data-ttu-id="bd8ce-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-444">Proj 1</span></span></td>
<td><span data-ttu-id="bd8ce-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="bd8ce-446">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-446">10001</span></span></td>
<td><span data-ttu-id="bd8ce-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-447">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-448">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-449">30,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-449">30.00</span></span></td>
<td><span data-ttu-id="bd8ce-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-451">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-451">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-452">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-452">HR</span></span></td>
<td><span data-ttu-id="bd8ce-453">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-453">10001</span></span></td>
<td><span data-ttu-id="bd8ce-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-454">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-455">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-456">-10.00</span></span></td>
<td><span data-ttu-id="bd8ce-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-458">Proj 2</span></span></td>
<td><span data-ttu-id="bd8ce-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="bd8ce-460">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-460">10001</span></span></td>
<td><span data-ttu-id="bd8ce-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-461">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-462">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-463">10.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-463">10.00</span></span></td>
<td><span data-ttu-id="bd8ce-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="bd8ce-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="bd8ce-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="bd8ce-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="bd8ce-468">Finance ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="bd8ce-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="bd8ce-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="bd8ce-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="bd8ce-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="bd8ce-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="bd8ce-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="bd8ce-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-475">Define the cost allocation</span></span>

<span data-ttu-id="bd8ce-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="bd8ce-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="bd8ce-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-479">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="bd8ce-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-481">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-481">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-482">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-483">35</span><span class="sxs-lookup"><span data-stu-id="bd8ce-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-484">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-484">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-485">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-486">55</span><span class="sxs-lookup"><span data-stu-id="bd8ce-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-487">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-487">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-488">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-489">10</span><span class="sxs-lookup"><span data-stu-id="bd8ce-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="bd8ce-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-492">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="bd8ce-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-494">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-494">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-495">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-496">65</span><span class="sxs-lookup"><span data-stu-id="bd8ce-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-497">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-497">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-498">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-499">35</span><span class="sxs-lookup"><span data-stu-id="bd8ce-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="bd8ce-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-502">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-504">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-505">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-506">60</span><span class="sxs-lookup"><span data-stu-id="bd8ce-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-507">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-508">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-509">20</span><span class="sxs-lookup"><span data-stu-id="bd8ce-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="bd8ce-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-512">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-514">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-515">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-516">80</span><span class="sxs-lookup"><span data-stu-id="bd8ce-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-517">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-518">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-519">15</span><span class="sxs-lookup"><span data-stu-id="bd8ce-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bd8ce-520">Statistische metingen, zoals de productie-uren die een product verbruikt, kunnen worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="bd8ce-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="bd8ce-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="bd8ce-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-523">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="bd8ce-524">Magnitude</span></span></th>
<th><span data-ttu-id="bd8ce-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="bd8ce-525">Allocation factor</span></span></th>
<th><span data-ttu-id="bd8ce-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-526">Amount</span></span></th>
<th><span data-ttu-id="bd8ce-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-528">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-528">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-529">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-530">35</span><span class="sxs-lookup"><span data-stu-id="bd8ce-530">35</span></span></td>
<td><span data-ttu-id="bd8ce-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bd8ce-532">175.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-532">175.00</span></span></td>
<td><span data-ttu-id="bd8ce-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-534">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-534">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-535">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-536">55</span><span class="sxs-lookup"><span data-stu-id="bd8ce-536">55</span></span></td>
<td><span data-ttu-id="bd8ce-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bd8ce-538">275.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-538">275.00</span></span></td>
<td><span data-ttu-id="bd8ce-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-540">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-540">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-541">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-542">10</span><span class="sxs-lookup"><span data-stu-id="bd8ce-542">10</span></span></td>
<td><span data-ttu-id="bd8ce-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="bd8ce-544">50,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-544">50.00</span></span></td>
<td><span data-ttu-id="bd8ce-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-546">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-546">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-547">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-548">35</span><span class="sxs-lookup"><span data-stu-id="bd8ce-548">35</span></span></td>
<td><span data-ttu-id="bd8ce-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bd8ce-550">436.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-550">436.00</span></span></td>
<td><span data-ttu-id="bd8ce-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-552">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-552">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-553">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-554">55</span><span class="sxs-lookup"><span data-stu-id="bd8ce-554">55</span></span></td>
<td><span data-ttu-id="bd8ce-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bd8ce-556">685.14</span><span class="sxs-lookup"><span data-stu-id="bd8ce-556">685.14</span></span></td>
<td><span data-ttu-id="bd8ce-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-558">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-558">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-559">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-560">10</span><span class="sxs-lookup"><span data-stu-id="bd8ce-560">10</span></span></td>
<td><span data-ttu-id="bd8ce-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="bd8ce-562">124.57</span><span class="sxs-lookup"><span data-stu-id="bd8ce-562">124.57</span></span></td>
<td><span data-ttu-id="bd8ce-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="bd8ce-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-565">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="bd8ce-566">Magnitude</span></span></th>
<th><span data-ttu-id="bd8ce-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="bd8ce-567">Allocation factor</span></span></th>
<th><span data-ttu-id="bd8ce-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-568">Amount</span></span></th>
<th><span data-ttu-id="bd8ce-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-570">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-570">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-571">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-572">65</span><span class="sxs-lookup"><span data-stu-id="bd8ce-572">65</span></span></td>
<td><span data-ttu-id="bd8ce-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="bd8ce-574">438.75</span><span class="sxs-lookup"><span data-stu-id="bd8ce-574">438.75</span></span></td>
<td><span data-ttu-id="bd8ce-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-576">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-576">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-577">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-578">35</span><span class="sxs-lookup"><span data-stu-id="bd8ce-578">35</span></span></td>
<td><span data-ttu-id="bd8ce-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="bd8ce-580">236.25</span><span class="sxs-lookup"><span data-stu-id="bd8ce-580">236.25</span></span></td>
<td><span data-ttu-id="bd8ce-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-582">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-582">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-583">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-584">65</span><span class="sxs-lookup"><span data-stu-id="bd8ce-584">65</span></span></td>
<td><span data-ttu-id="bd8ce-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="bd8ce-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="bd8ce-586">5,297.69</span></span></td>
<td><span data-ttu-id="bd8ce-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-588">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-588">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-589">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-590">35</span><span class="sxs-lookup"><span data-stu-id="bd8ce-590">35</span></span></td>
<td><span data-ttu-id="bd8ce-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="bd8ce-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="bd8ce-592">2,852.60</span></span></td>
<td><span data-ttu-id="bd8ce-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="bd8ce-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-595">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="bd8ce-596">Magnitude</span></span></th>
<th><span data-ttu-id="bd8ce-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="bd8ce-597">Allocation factor</span></span></th>
<th><span data-ttu-id="bd8ce-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-598">Amount</span></span></th>
<th><span data-ttu-id="bd8ce-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-600">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-601">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-602">60</span><span class="sxs-lookup"><span data-stu-id="bd8ce-602">60</span></span></td>
<td><span data-ttu-id="bd8ce-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="bd8ce-604">535.31</span><span class="sxs-lookup"><span data-stu-id="bd8ce-604">535.31</span></span></td>
<td><span data-ttu-id="bd8ce-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-606">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-607">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-608">20</span><span class="sxs-lookup"><span data-stu-id="bd8ce-608">20</span></span></td>
<td><span data-ttu-id="bd8ce-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="bd8ce-610">178.44</span><span class="sxs-lookup"><span data-stu-id="bd8ce-610">178.44</span></span></td>
<td><span data-ttu-id="bd8ce-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-612">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-613">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-614">60</span><span class="sxs-lookup"><span data-stu-id="bd8ce-614">60</span></span></td>
<td><span data-ttu-id="bd8ce-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="bd8ce-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="bd8ce-616">4,487.12</span></span></td>
<td><span data-ttu-id="bd8ce-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-618">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-619">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-620">20</span><span class="sxs-lookup"><span data-stu-id="bd8ce-620">20</span></span></td>
<td><span data-ttu-id="bd8ce-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="bd8ce-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-622">1,495.71</span></span></td>
<td><span data-ttu-id="bd8ce-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bd8ce-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="bd8ce-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-625">Cost object</span></span></th>
<th><span data-ttu-id="bd8ce-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="bd8ce-626">Magnitude</span></span></th>
<th><span data-ttu-id="bd8ce-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="bd8ce-627">Allocation factor</span></span></th>
<th><span data-ttu-id="bd8ce-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-628">Amount</span></span></th>
<th><span data-ttu-id="bd8ce-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-630">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-631">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-632">80</span><span class="sxs-lookup"><span data-stu-id="bd8ce-632">80</span></span></td>
<td><span data-ttu-id="bd8ce-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="bd8ce-634">241.05</span><span class="sxs-lookup"><span data-stu-id="bd8ce-634">241.05</span></span></td>
<td><span data-ttu-id="bd8ce-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-636">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-637">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-638">15</span><span class="sxs-lookup"><span data-stu-id="bd8ce-638">15</span></span></td>
<td><span data-ttu-id="bd8ce-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="bd8ce-640">45.20</span><span class="sxs-lookup"><span data-stu-id="bd8ce-640">45.20</span></span></td>
<td><span data-ttu-id="bd8ce-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-642">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-643">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-644">80</span><span class="sxs-lookup"><span data-stu-id="bd8ce-644">80</span></span></td>
<td><span data-ttu-id="bd8ce-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="bd8ce-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="bd8ce-646">2,507.09</span></span></td>
<td><span data-ttu-id="bd8ce-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-648">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-649">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-650">15</span><span class="sxs-lookup"><span data-stu-id="bd8ce-650">15</span></span></td>
<td><span data-ttu-id="bd8ce-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="bd8ce-652">470.08</span><span class="sxs-lookup"><span data-stu-id="bd8ce-652">470.08</span></span></td>
<td><span data-ttu-id="bd8ce-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="bd8ce-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="bd8ce-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-655">Journal</span></span></th>
<th><span data-ttu-id="bd8ce-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="bd8ce-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="bd8ce-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="bd8ce-658">Versie</span><span class="sxs-lookup"><span data-stu-id="bd8ce-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-659">00004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-659">00004</span></span></td>
<td><span data-ttu-id="bd8ce-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="bd8ce-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-661">Fiscal</span></span></td>
<td><span data-ttu-id="bd8ce-662">2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-662">2017</span></span></td>
<td><span data-ttu-id="bd8ce-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-663">Period 1</span></span></td>
<td><span data-ttu-id="bd8ce-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="bd8ce-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="bd8ce-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bd8ce-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-668">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-669">Cost behavior</span></span></th>
<th><span data-ttu-id="bd8ce-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-672">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-672">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-673">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-673">HR</span></span></td>
<td><span data-ttu-id="bd8ce-674">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-674">10001</span></span></td>
<td><span data-ttu-id="bd8ce-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-675">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-676">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-677">500,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-679">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-679">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-680">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-680">HR</span></span></td>
<td><span data-ttu-id="bd8ce-681">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-681">10001</span></span></td>
<td><span data-ttu-id="bd8ce-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-682">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-683">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-686">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-686">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-687">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-688">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-688">10001</span></span></td>
<td><span data-ttu-id="bd8ce-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-689">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-690">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-691">675.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-693">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-693">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-694">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-695">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-695">10001</span></span></td>
<td><span data-ttu-id="bd8ce-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-696">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-697">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="bd8ce-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-700">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-700">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-701">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-702">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-702">10001</span></span></td>
<td><span data-ttu-id="bd8ce-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-703">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-704">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-705">713.75</span><span class="sxs-lookup"><span data-stu-id="bd8ce-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-707">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-707">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-708">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-709">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-709">10001</span></span></td>
<td><span data-ttu-id="bd8ce-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-710">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-711">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="bd8ce-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-714">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-714">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-715">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-716">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-716">10001</span></span></td>
<td><span data-ttu-id="bd8ce-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-717">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-718">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-719">286.25</span><span class="sxs-lookup"><span data-stu-id="bd8ce-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-721">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-721">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-722">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-723">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-723">10001</span></span></td>
<td><span data-ttu-id="bd8ce-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-724">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-725">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="bd8ce-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-728">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-729">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-730">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-730">10001</span></span></td>
<td><span data-ttu-id="bd8ce-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-731">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-732">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-733">776.36</span><span class="sxs-lookup"><span data-stu-id="bd8ce-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-735">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-736">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-737">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-737">10001</span></span></td>
<td><span data-ttu-id="bd8ce-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-738">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-739">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="bd8ce-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-742">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-743">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-744">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-744">10001</span></span></td>
<td><span data-ttu-id="bd8ce-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-745">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-746">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-747">223.64</span><span class="sxs-lookup"><span data-stu-id="bd8ce-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="bd8ce-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-749">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-750">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-751">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-751">10001</span></span></td>
<td><span data-ttu-id="bd8ce-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-752">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-753">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="bd8ce-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="bd8ce-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="bd8ce-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="bd8ce-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="bd8ce-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-757">Cost element</span></span></th>
<th><span data-ttu-id="bd8ce-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-758">Cost behavior</span></span></th>
<th><span data-ttu-id="bd8ce-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="bd8ce-759">Amount</span></span></th>
<th><span data-ttu-id="bd8ce-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="bd8ce-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bd8ce-761">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-761">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-762">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-762">HR</span></span></td>
<td><span data-ttu-id="bd8ce-763">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-763">10001</span></span></td>
<td><span data-ttu-id="bd8ce-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-764">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-765">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-766">-500.00</span></span></td>
<td><span data-ttu-id="bd8ce-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-768">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-768">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-769">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-770">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-770">10001</span></span></td>
<td><span data-ttu-id="bd8ce-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-771">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-772">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-773">175.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-773">175.00</span></span></td>
<td><span data-ttu-id="bd8ce-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-775">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-775">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-776">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-777">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-777">10001</span></span></td>
<td><span data-ttu-id="bd8ce-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-778">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-779">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-780">275.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-780">275.00</span></span></td>
<td><span data-ttu-id="bd8ce-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-782">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-782">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-783">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-784">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-784">10001</span></span></td>
<td><span data-ttu-id="bd8ce-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-785">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-786">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-787">50,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-787">50,00</span></span></td>
<td><span data-ttu-id="bd8ce-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-789">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-789">CC001</span></span></td>
<td><span data-ttu-id="bd8ce-790">HR</span><span class="sxs-lookup"><span data-stu-id="bd8ce-790">HR</span></span></td>
<td><span data-ttu-id="bd8ce-791">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-791">10001</span></span></td>
<td><span data-ttu-id="bd8ce-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-792">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-793">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-794">-1,245.71</span></span></td>
<td><span data-ttu-id="bd8ce-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-796">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-796">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-797">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-798">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-798">10001</span></span></td>
<td><span data-ttu-id="bd8ce-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-799">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-800">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-801">436.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-801">436.00</span></span></td>
<td><span data-ttu-id="bd8ce-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-803">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-803">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-804">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-805">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-805">10001</span></span></td>
<td><span data-ttu-id="bd8ce-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-806">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-807">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-808">685.14</span><span class="sxs-lookup"><span data-stu-id="bd8ce-808">685.14</span></span></td>
<td><span data-ttu-id="bd8ce-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-810">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-810">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-811">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-812">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-812">10001</span></span></td>
<td><span data-ttu-id="bd8ce-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-813">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-814">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-815">124.57</span><span class="sxs-lookup"><span data-stu-id="bd8ce-815">124.57</span></span></td>
<td><span data-ttu-id="bd8ce-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-817">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-817">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-818">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-819">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-819">10001</span></span></td>
<td><span data-ttu-id="bd8ce-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-820">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-821">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-822">-675.00</span></span></td>
<td><span data-ttu-id="bd8ce-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-824">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-824">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-825">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-826">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-826">10001</span></span></td>
<td><span data-ttu-id="bd8ce-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-827">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-828">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-829">438.75</span><span class="sxs-lookup"><span data-stu-id="bd8ce-829">438.75</span></span></td>
<td><span data-ttu-id="bd8ce-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-831">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-831">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-832">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-833">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-833">10001</span></span></td>
<td><span data-ttu-id="bd8ce-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-834">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-835">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-836">236.25</span><span class="sxs-lookup"><span data-stu-id="bd8ce-836">236.25</span></span></td>
<td><span data-ttu-id="bd8ce-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-838">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-838">CC002</span></span></td>
<td><span data-ttu-id="bd8ce-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="bd8ce-839">Finance</span></span></td>
<td><span data-ttu-id="bd8ce-840">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-840">10001</span></span></td>
<td><span data-ttu-id="bd8ce-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-841">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-842">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="bd8ce-843">-8,150.29</span></span></td>
<td><span data-ttu-id="bd8ce-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-845">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-845">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-846">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-847">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-847">10001</span></span></td>
<td><span data-ttu-id="bd8ce-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-848">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-849">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="bd8ce-850">5,297.69</span></span></td>
<td><span data-ttu-id="bd8ce-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-852">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-852">CC004</span></span></td>
<td><span data-ttu-id="bd8ce-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="bd8ce-853">Packaging</span></span></td>
<td><span data-ttu-id="bd8ce-854">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-854">10001</span></span></td>
<td><span data-ttu-id="bd8ce-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-855">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-856">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="bd8ce-857">2,852.60</span></span></td>
<td><span data-ttu-id="bd8ce-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-859">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-859">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-860">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-861">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-861">10001</span></span></td>
<td><span data-ttu-id="bd8ce-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-862">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-863">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="bd8ce-864">-713.75</span></span></td>
<td><span data-ttu-id="bd8ce-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-866">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-867">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-868">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-868">10001</span></span></td>
<td><span data-ttu-id="bd8ce-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-869">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-870">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-871">535.31</span><span class="sxs-lookup"><span data-stu-id="bd8ce-871">535.31</span></span></td>
<td><span data-ttu-id="bd8ce-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-873">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-874">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-875">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-875">10001</span></span></td>
<td><span data-ttu-id="bd8ce-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-876">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-877">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-878">178.44</span><span class="sxs-lookup"><span data-stu-id="bd8ce-878">178.44</span></span></td>
<td><span data-ttu-id="bd8ce-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-880">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-880">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-881">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-882">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-882">10001</span></span></td>
<td><span data-ttu-id="bd8ce-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-883">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-884">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="bd8ce-885">-5,982.83</span></span></td>
<td><span data-ttu-id="bd8ce-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-887">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-888">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-889">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-889">10001</span></span></td>
<td><span data-ttu-id="bd8ce-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-890">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-891">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="bd8ce-892">4,487.12</span></span></td>
<td><span data-ttu-id="bd8ce-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-894">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-895">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-896">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-896">10001</span></span></td>
<td><span data-ttu-id="bd8ce-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-897">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-898">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="bd8ce-899">1,495.71</span></span></td>
<td><span data-ttu-id="bd8ce-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-901">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-901">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-902">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-903">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-903">10001</span></span></td>
<td><span data-ttu-id="bd8ce-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-904">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-905">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="bd8ce-906">-286.25</span></span></td>
<td><span data-ttu-id="bd8ce-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-908">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-909">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-910">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-910">10001</span></span></td>
<td><span data-ttu-id="bd8ce-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-911">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-912">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-913">241.05</span><span class="sxs-lookup"><span data-stu-id="bd8ce-913">241.05</span></span></td>
<td><span data-ttu-id="bd8ce-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-915">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-916">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-917">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-917">10001</span></span></td>
<td><span data-ttu-id="bd8ce-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-918">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-919">Fixed cost</span></span></td>
<td><span data-ttu-id="bd8ce-920">45.20</span><span class="sxs-lookup"><span data-stu-id="bd8ce-920">45.20</span></span></td>
<td><span data-ttu-id="bd8ce-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-922">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-922">CC003</span></span></td>
<td><span data-ttu-id="bd8ce-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="bd8ce-923">Assembly</span></span></td>
<td><span data-ttu-id="bd8ce-924">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-924">10001</span></span></td>
<td><span data-ttu-id="bd8ce-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-925">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-926">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="bd8ce-927">-2,977.17</span></span></td>
<td><span data-ttu-id="bd8ce-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-929">Prod 1</span></span></td>
<td><span data-ttu-id="bd8ce-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-930">Product 1</span></span></td>
<td><span data-ttu-id="bd8ce-931">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-931">10001</span></span></td>
<td><span data-ttu-id="bd8ce-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-932">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-933">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="bd8ce-934">2,507.09</span></span></td>
<td><span data-ttu-id="bd8ce-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bd8ce-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-936">Prod 2</span></span></td>
<td><span data-ttu-id="bd8ce-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-937">Product 2</span></span></td>
<td><span data-ttu-id="bd8ce-938">10001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-938">10001</span></span></td>
<td><span data-ttu-id="bd8ce-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-939">Electricity</span></span></td>
<td><span data-ttu-id="bd8ce-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-940">Variable cost</span></span></td>
<td><span data-ttu-id="bd8ce-941">470.08</span><span class="sxs-lookup"><span data-stu-id="bd8ce-941">470.08</span></span></td>
<td><span data-ttu-id="bd8ce-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="bd8ce-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="bd8ce-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="bd8ce-943">Conclusion</span></span>
<span data-ttu-id="bd8ce-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="bd8ce-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="bd8ce-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="bd8ce-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="bd8ce-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="bd8ce-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="bd8ce-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="bd8ce-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="bd8ce-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="bd8ce-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bd8ce-951">CC099</span><span class="sxs-lookup"><span data-stu-id="bd8ce-951">CC099</span></span></th>
<th><span data-ttu-id="bd8ce-952">CC001</span><span class="sxs-lookup"><span data-stu-id="bd8ce-952">CC001</span></span></th>
<th><span data-ttu-id="bd8ce-953">CC002</span><span class="sxs-lookup"><span data-stu-id="bd8ce-953">CC002</span></span></th>
<th><span data-ttu-id="bd8ce-954">CC003</span><span class="sxs-lookup"><span data-stu-id="bd8ce-954">CC003</span></span></th>
<th><span data-ttu-id="bd8ce-955">CC004</span><span class="sxs-lookup"><span data-stu-id="bd8ce-955">CC004</span></span></th>
<th><span data-ttu-id="bd8ce-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-956">Proj 1</span></span></th>
<th><span data-ttu-id="bd8ce-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-957">Proj 2</span></span></th>
<th><span data-ttu-id="bd8ce-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="bd8ce-958">Prod 1</span></span></th>
<th><span data-ttu-id="bd8ce-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="bd8ce-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="bd8ce-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="bd8ce-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="bd8ce-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="bd8ce-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-971">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="bd8ce-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-973">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-974">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-975">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-976">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-977">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-978">776.36</span><span class="sxs-lookup"><span data-stu-id="bd8ce-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-979">223.64</span><span class="sxs-lookup"><span data-stu-id="bd8ce-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="bd8ce-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="bd8ce-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-982">000</span><span class="sxs-lookup"><span data-stu-id="bd8ce-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-983">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-984">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-985">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-986">0,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-987">30,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-988">10,00</span><span class="sxs-lookup"><span data-stu-id="bd8ce-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="bd8ce-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="bd8ce-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="bd8ce-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="bd8ce-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bd8ce-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="bd8ce-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="bd8ce-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="bd8ce-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="bd8ce-996">Zie [Beleid voor totalisering van kosten en overheadberekening](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="bd8ce-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



