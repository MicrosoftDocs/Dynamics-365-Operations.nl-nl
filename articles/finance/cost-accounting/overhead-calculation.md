---
title: Overheadberekening
description: In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822898"
---
# <a name="overhead-calculation"></a><span data-ttu-id="d52eb-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="d52eb-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d52eb-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="d52eb-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="d52eb-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="d52eb-105">Term definition</span></span>
---------------

<span data-ttu-id="d52eb-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="d52eb-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="d52eb-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="d52eb-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="d52eb-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="d52eb-109">Huur</span><span class="sxs-lookup"><span data-stu-id="d52eb-109">Rent</span></span>
-   <span data-ttu-id="d52eb-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-110">Electricity</span></span>
-   <span data-ttu-id="d52eb-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="d52eb-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="d52eb-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="d52eb-112">Overhead calculation overview</span></span>
<span data-ttu-id="d52eb-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d52eb-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="d52eb-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="d52eb-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="d52eb-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="d52eb-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="d52eb-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="d52eb-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="d52eb-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="d52eb-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="d52eb-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="d52eb-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="d52eb-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="d52eb-119">Version type</span></span>
-   <span data-ttu-id="d52eb-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="d52eb-120">Date and time</span></span>
-   <span data-ttu-id="d52eb-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="d52eb-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="d52eb-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="d52eb-122">Fiscal year</span></span>
-   <span data-ttu-id="d52eb-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="d52eb-123">Fiscal period</span></span>

<span data-ttu-id="d52eb-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d52eb-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="d52eb-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="d52eb-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="d52eb-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d52eb-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="d52eb-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="d52eb-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="d52eb-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="d52eb-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="d52eb-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="d52eb-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="d52eb-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="d52eb-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="d52eb-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="d52eb-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="d52eb-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="d52eb-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="d52eb-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="d52eb-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="d52eb-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="d52eb-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="d52eb-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="d52eb-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="d52eb-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="d52eb-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="d52eb-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="d52eb-140">Main account</span></span></th>
<th><span data-ttu-id="d52eb-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="d52eb-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="d52eb-143">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-143">CC099</span></span></td>
<td><span data-ttu-id="d52eb-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-144">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-145">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-145">10001</span></span></td>
<td><span data-ttu-id="d52eb-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-146">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="d52eb-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="d52eb-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="d52eb-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="d52eb-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="d52eb-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="d52eb-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="d52eb-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="d52eb-151">Define the cost behavior rule</span></span>

<span data-ttu-id="d52eb-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="d52eb-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="d52eb-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="d52eb-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="d52eb-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="d52eb-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="d52eb-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="d52eb-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="d52eb-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="d52eb-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="d52eb-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="d52eb-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="d52eb-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="d52eb-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-160">Journal</span></span></th>
<th><span data-ttu-id="d52eb-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d52eb-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="d52eb-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d52eb-163">Versie</span><span class="sxs-lookup"><span data-stu-id="d52eb-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-164">00001</span><span class="sxs-lookup"><span data-stu-id="d52eb-164">00001</span></span></td>
<td><span data-ttu-id="d52eb-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="d52eb-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-166">Fiscal</span></span></td>
<td><span data-ttu-id="d52eb-167">2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-167">2017</span></span></td>
<td><span data-ttu-id="d52eb-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-168">Period 1</span></span></td>
<td><span data-ttu-id="d52eb-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d52eb-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="d52eb-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-173">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-174">Cost behavior</span></span></th>
<th><span data-ttu-id="d52eb-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="d52eb-177">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-177">CC099</span></span></td>
<td><span data-ttu-id="d52eb-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-178">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-179">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-179">10001</span></span></td>
<td><span data-ttu-id="d52eb-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-180">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="d52eb-181">Unclassified</span></span></td>
<td><span data-ttu-id="d52eb-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d52eb-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="d52eb-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-185">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-186">Cost behavior</span></span></th>
<th><span data-ttu-id="d52eb-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-187">Amount</span></span></th>
<th><span data-ttu-id="d52eb-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-189">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-189">CC099</span></span></td>
<td><span data-ttu-id="d52eb-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-190">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-191">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-191">10001</span></span></td>
<td><span data-ttu-id="d52eb-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-192">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="d52eb-193">Unclassified</span></span></td>
<td><span data-ttu-id="d52eb-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-194">10,000.00</span></span></td>
<td><span data-ttu-id="d52eb-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-196">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-196">CC099</span></span></td>
<td><span data-ttu-id="d52eb-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-197">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-198">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-198">10001</span></span></td>
<td><span data-ttu-id="d52eb-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-199">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="d52eb-200">Unclassified</span></span></td>
<td><span data-ttu-id="d52eb-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-201">-10,000.00</span></span></td>
<td><span data-ttu-id="d52eb-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-203">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-203">CC099</span></span></td>
<td><span data-ttu-id="d52eb-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-204">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-205">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-205">10001</span></span></td>
<td><span data-ttu-id="d52eb-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-206">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-207">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-208">1,000.00</span></span></td>
<td><span data-ttu-id="d52eb-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-210">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-210">CC099</span></span></td>
<td><span data-ttu-id="d52eb-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-211">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-212">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-212">10001</span></span></td>
<td><span data-ttu-id="d52eb-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-213">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-214">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-215">9,000.00</span></span></td>
<td><span data-ttu-id="d52eb-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d52eb-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="d52eb-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="d52eb-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="d52eb-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="d52eb-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="d52eb-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="d52eb-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="d52eb-221">Define the cost distribution rule</span></span>

<span data-ttu-id="d52eb-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="d52eb-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="d52eb-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="d52eb-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="d52eb-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="d52eb-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="d52eb-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="d52eb-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="d52eb-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="d52eb-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="d52eb-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-228">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="d52eb-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-230">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-230">CC001</span></span></td>
<td><span data-ttu-id="d52eb-231">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-231">HR</span></span></td>
<td><span data-ttu-id="d52eb-232">1.000</span><span class="sxs-lookup"><span data-stu-id="d52eb-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-233">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-233">CC002</span></span></td>
<td><span data-ttu-id="d52eb-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-234">Finance</span></span></td>
<td><span data-ttu-id="d52eb-235">6.000</span><span class="sxs-lookup"><span data-stu-id="d52eb-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-236">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-236">CC003</span></span></td>
<td><span data-ttu-id="d52eb-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-237">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-238">0</span><span class="sxs-lookup"><span data-stu-id="d52eb-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-240">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="d52eb-241">Magnitude</span></span></th>
<th><span data-ttu-id="d52eb-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="d52eb-242">Allocation factor</span></span></th>
<th><span data-ttu-id="d52eb-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-244">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-244">CC001</span></span></td>
<td><span data-ttu-id="d52eb-245">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-245">HR</span></span></td>
<td><span data-ttu-id="d52eb-246">1.000</span><span class="sxs-lookup"><span data-stu-id="d52eb-246">1,000</span></span></td>
<td><span data-ttu-id="d52eb-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d52eb-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d52eb-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-249">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-249">CC002</span></span></td>
<td><span data-ttu-id="d52eb-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-250">Finance</span></span></td>
<td><span data-ttu-id="d52eb-251">6.000</span><span class="sxs-lookup"><span data-stu-id="d52eb-251">6,000</span></span></td>
<td><span data-ttu-id="d52eb-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d52eb-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d52eb-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-254">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-254">CC003</span></span></td>
<td><span data-ttu-id="d52eb-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-255">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-256">0</span><span class="sxs-lookup"><span data-stu-id="d52eb-256">0</span></span></td>
<td><span data-ttu-id="d52eb-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d52eb-258">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="d52eb-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="d52eb-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-261">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-262">Formule</span><span class="sxs-lookup"><span data-stu-id="d52eb-262">Formula</span></span></th>
<th><span data-ttu-id="d52eb-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="d52eb-263">Magnitude</span></span></th>
<th><span data-ttu-id="d52eb-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="d52eb-264">Allocation factor</span></span></th>
<th><span data-ttu-id="d52eb-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-266">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-266">CC001</span></span></td>
<td><span data-ttu-id="d52eb-267">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-267">HR</span></span></td>
<td><span data-ttu-id="d52eb-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d52eb-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d52eb-269">1</span><span class="sxs-lookup"><span data-stu-id="d52eb-269">1</span></span></td>
<td><span data-ttu-id="d52eb-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d52eb-271">500,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-272">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-272">CC002</span></span></td>
<td><span data-ttu-id="d52eb-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-273">Finance</span></span></td>
<td><span data-ttu-id="d52eb-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d52eb-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d52eb-275">1</span><span class="sxs-lookup"><span data-stu-id="d52eb-275">1</span></span></td>
<td><span data-ttu-id="d52eb-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d52eb-277">500,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-278">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-278">CC003</span></span></td>
<td><span data-ttu-id="d52eb-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-279">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d52eb-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d52eb-281">0</span><span class="sxs-lookup"><span data-stu-id="d52eb-281">0</span></span></td>
<td><span data-ttu-id="d52eb-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d52eb-283">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d52eb-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-285">Journal</span></span></th>
<th><span data-ttu-id="d52eb-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d52eb-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="d52eb-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d52eb-288">Versie</span><span class="sxs-lookup"><span data-stu-id="d52eb-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-289">00002</span><span class="sxs-lookup"><span data-stu-id="d52eb-289">00002</span></span></td>
<td><span data-ttu-id="d52eb-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="d52eb-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="d52eb-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-291">Fiscal</span></span></td>
<td><span data-ttu-id="d52eb-292">2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-292">2017</span></span></td>
<td><span data-ttu-id="d52eb-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-293">Period 1</span></span></td>
<td><span data-ttu-id="d52eb-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d52eb-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="d52eb-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-298">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-299">Cost behavior</span></span></th>
<th><span data-ttu-id="d52eb-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-302">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-302">CC099</span></span></td>
<td><span data-ttu-id="d52eb-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-303">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-304">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-304">10001</span></span></td>
<td><span data-ttu-id="d52eb-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-305">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-306">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-309">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-309">CC099</span></span></td>
<td><span data-ttu-id="d52eb-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-310">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-311">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-311">10001</span></span></td>
<td><span data-ttu-id="d52eb-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-312">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-313">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d52eb-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="d52eb-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-317">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-318">Cost behavior</span></span></th>
<th><span data-ttu-id="d52eb-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-319">Amount</span></span></th>
<th><span data-ttu-id="d52eb-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-321">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-321">CC099</span></span></td>
<td><span data-ttu-id="d52eb-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-322">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-323">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-323">10001</span></span></td>
<td><span data-ttu-id="d52eb-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-324">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-325">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-326">-1,000.00</span></span></td>
<td><span data-ttu-id="d52eb-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-328">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-328">CC001</span></span></td>
<td><span data-ttu-id="d52eb-329">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-329">HR</span></span></td>
<td><span data-ttu-id="d52eb-330">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-330">10001</span></span></td>
<td><span data-ttu-id="d52eb-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-331">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-332">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-333">500,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-333">500.00</span></span></td>
<td><span data-ttu-id="d52eb-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-335">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-335">CC002</span></span></td>
<td><span data-ttu-id="d52eb-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-336">Finance</span></span></td>
<td><span data-ttu-id="d52eb-337">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-337">10001</span></span></td>
<td><span data-ttu-id="d52eb-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-338">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-339">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-340">500,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-340">500.00</span></span></td>
<td><span data-ttu-id="d52eb-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-342">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-342">CC099</span></span></td>
<td><span data-ttu-id="d52eb-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="d52eb-343">Default cost center</span></span></td>
<td><span data-ttu-id="d52eb-344">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-344">10001</span></span></td>
<td><span data-ttu-id="d52eb-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-345">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-346">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-347">-9,000.00</span></span></td>
<td><span data-ttu-id="d52eb-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-349">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-349">CC001</span></span></td>
<td><span data-ttu-id="d52eb-350">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-350">HR</span></span></td>
<td><span data-ttu-id="d52eb-351">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-351">10001</span></span></td>
<td><span data-ttu-id="d52eb-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-352">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-353">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d52eb-354">1,285.71</span></span></td>
<td><span data-ttu-id="d52eb-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-356">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-356">CC002</span></span></td>
<td><span data-ttu-id="d52eb-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-357">Finance</span></span></td>
<td><span data-ttu-id="d52eb-358">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-358">10001</span></span></td>
<td><span data-ttu-id="d52eb-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-359">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-360">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d52eb-361">7,714.29</span></span></td>
<td><span data-ttu-id="d52eb-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d52eb-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="d52eb-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="d52eb-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="d52eb-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="d52eb-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="d52eb-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="d52eb-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="d52eb-367">Define the overhead rate</span></span>

<span data-ttu-id="d52eb-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="d52eb-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-370">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-371">Uren</span><span class="sxs-lookup"><span data-stu-id="d52eb-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-372">Proj 1</span></span></td>
<td><span data-ttu-id="d52eb-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-373">Project 1</span></span></td>
<td><span data-ttu-id="d52eb-374">3</span><span class="sxs-lookup"><span data-stu-id="d52eb-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-375">Proj 2</span></span></td>
<td><span data-ttu-id="d52eb-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-376">Project 2</span></span></td>
<td><span data-ttu-id="d52eb-377">1</span><span class="sxs-lookup"><span data-stu-id="d52eb-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d52eb-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-379">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-380">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-381">Cost behavior</span></span></th>
<th><span data-ttu-id="d52eb-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="d52eb-382">Units</span></span></th>
<th><span data-ttu-id="d52eb-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="d52eb-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-384">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-384">CC001</span></span></td>
<td><span data-ttu-id="d52eb-385">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-385">HR</span></span></td>
<td><span data-ttu-id="d52eb-386">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-386">10001</span></span></td>
<td><span data-ttu-id="d52eb-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-387">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-388">1</span><span class="sxs-lookup"><span data-stu-id="d52eb-388">1</span></span></td>
<td><span data-ttu-id="d52eb-389">10</span><span class="sxs-lookup"><span data-stu-id="d52eb-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="d52eb-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-391">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="d52eb-392">Magnitude</span></span></th>
<th><span data-ttu-id="d52eb-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-393">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="d52eb-394">Allocation factor</span></span></th>
<th><span data-ttu-id="d52eb-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-396">Proj 1</span></span></td>
<td><span data-ttu-id="d52eb-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-397">Project 1</span></span></td>
<td><span data-ttu-id="d52eb-398">3</span><span class="sxs-lookup"><span data-stu-id="d52eb-398">3</span></span></td>
<td><span data-ttu-id="d52eb-399">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-399">10001</span></span></td>
<td><span data-ttu-id="d52eb-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d52eb-401">30,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-402">Proj 2</span></span></td>
<td><span data-ttu-id="d52eb-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-403">Project 2</span></span></td>
<td><span data-ttu-id="d52eb-404">1</span><span class="sxs-lookup"><span data-stu-id="d52eb-404">1</span></span></td>
<td><span data-ttu-id="d52eb-405">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-405">10001</span></span></td>
<td><span data-ttu-id="d52eb-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d52eb-407">10,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d52eb-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-409">Journal</span></span></th>
<th><span data-ttu-id="d52eb-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d52eb-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="d52eb-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d52eb-412">Versie</span><span class="sxs-lookup"><span data-stu-id="d52eb-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-413">00003</span><span class="sxs-lookup"><span data-stu-id="d52eb-413">00003</span></span></td>
<td><span data-ttu-id="d52eb-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="d52eb-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="d52eb-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-415">Fiscal</span></span></td>
<td><span data-ttu-id="d52eb-416">2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-416">2017</span></span></td>
<td><span data-ttu-id="d52eb-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-417">Period 1</span></span></td>
<td><span data-ttu-id="d52eb-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="d52eb-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="d52eb-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-421">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="d52eb-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-424">Proj 1</span></span></td>
<td><span data-ttu-id="d52eb-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d52eb-426">3,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-428">Proj 2</span></span></td>
<td><span data-ttu-id="d52eb-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d52eb-430">1,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d52eb-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="d52eb-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-433">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-434">Cost behavior</span></span></th>
<th><span data-ttu-id="d52eb-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-435">Amount</span></span></th>
<th><span data-ttu-id="d52eb-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="d52eb-437">CC0001</span></span></td>
<td><span data-ttu-id="d52eb-438">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-438">HR</span></span></td>
<td><span data-ttu-id="d52eb-439">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-439">10001</span></span></td>
<td><span data-ttu-id="d52eb-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-440">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-441">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-442">-30.00</span></span></td>
<td><span data-ttu-id="d52eb-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-444">Proj 1</span></span></td>
<td><span data-ttu-id="d52eb-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d52eb-446">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-446">10001</span></span></td>
<td><span data-ttu-id="d52eb-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-447">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-448">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-449">30,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-449">30.00</span></span></td>
<td><span data-ttu-id="d52eb-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-451">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-451">CC001</span></span></td>
<td><span data-ttu-id="d52eb-452">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-452">HR</span></span></td>
<td><span data-ttu-id="d52eb-453">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-453">10001</span></span></td>
<td><span data-ttu-id="d52eb-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-454">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-455">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-456">-10.00</span></span></td>
<td><span data-ttu-id="d52eb-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-458">Proj 2</span></span></td>
<td><span data-ttu-id="d52eb-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d52eb-460">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-460">10001</span></span></td>
<td><span data-ttu-id="d52eb-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-461">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-462">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-463">10.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-463">10.00</span></span></td>
<td><span data-ttu-id="d52eb-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="d52eb-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="d52eb-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="d52eb-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="d52eb-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="d52eb-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="d52eb-468">Finance ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="d52eb-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="d52eb-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="d52eb-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="d52eb-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="d52eb-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="d52eb-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="d52eb-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="d52eb-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="d52eb-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="d52eb-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="d52eb-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="d52eb-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="d52eb-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="d52eb-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="d52eb-475">Define the cost allocation</span></span>

<span data-ttu-id="d52eb-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="d52eb-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="d52eb-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="d52eb-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-479">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="d52eb-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-481">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-481">CC002</span></span></td>
<td><span data-ttu-id="d52eb-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-482">Finance</span></span></td>
<td><span data-ttu-id="d52eb-483">35</span><span class="sxs-lookup"><span data-stu-id="d52eb-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-484">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-484">CC003</span></span></td>
<td><span data-ttu-id="d52eb-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-485">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-486">55</span><span class="sxs-lookup"><span data-stu-id="d52eb-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-487">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-487">CC004</span></span></td>
<td><span data-ttu-id="d52eb-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-488">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-489">10</span><span class="sxs-lookup"><span data-stu-id="d52eb-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="d52eb-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-492">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="d52eb-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-494">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-494">CC003</span></span></td>
<td><span data-ttu-id="d52eb-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-495">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-496">65</span><span class="sxs-lookup"><span data-stu-id="d52eb-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-497">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-497">CC004</span></span></td>
<td><span data-ttu-id="d52eb-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-498">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-499">35</span><span class="sxs-lookup"><span data-stu-id="d52eb-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="d52eb-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-502">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="d52eb-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-504">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-505">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-506">60</span><span class="sxs-lookup"><span data-stu-id="d52eb-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-507">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-508">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-509">20</span><span class="sxs-lookup"><span data-stu-id="d52eb-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="d52eb-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-512">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="d52eb-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-514">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-515">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-516">80</span><span class="sxs-lookup"><span data-stu-id="d52eb-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-517">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-518">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-519">15</span><span class="sxs-lookup"><span data-stu-id="d52eb-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d52eb-520">Statistische metingen, zoals de productie-uren die een product verbruikt, kunnen worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="d52eb-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="d52eb-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d52eb-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="d52eb-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="d52eb-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-523">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="d52eb-524">Magnitude</span></span></th>
<th><span data-ttu-id="d52eb-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="d52eb-525">Allocation factor</span></span></th>
<th><span data-ttu-id="d52eb-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-526">Amount</span></span></th>
<th><span data-ttu-id="d52eb-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-528">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-528">CC002</span></span></td>
<td><span data-ttu-id="d52eb-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-529">Finance</span></span></td>
<td><span data-ttu-id="d52eb-530">35</span><span class="sxs-lookup"><span data-stu-id="d52eb-530">35</span></span></td>
<td><span data-ttu-id="d52eb-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d52eb-532">175.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-532">175.00</span></span></td>
<td><span data-ttu-id="d52eb-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-534">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-534">CC003</span></span></td>
<td><span data-ttu-id="d52eb-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-535">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-536">55</span><span class="sxs-lookup"><span data-stu-id="d52eb-536">55</span></span></td>
<td><span data-ttu-id="d52eb-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d52eb-538">275.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-538">275.00</span></span></td>
<td><span data-ttu-id="d52eb-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-540">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-540">CC004</span></span></td>
<td><span data-ttu-id="d52eb-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-541">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-542">10</span><span class="sxs-lookup"><span data-stu-id="d52eb-542">10</span></span></td>
<td><span data-ttu-id="d52eb-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d52eb-544">50,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-544">50.00</span></span></td>
<td><span data-ttu-id="d52eb-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-546">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-546">CC002</span></span></td>
<td><span data-ttu-id="d52eb-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-547">Finance</span></span></td>
<td><span data-ttu-id="d52eb-548">35</span><span class="sxs-lookup"><span data-stu-id="d52eb-548">35</span></span></td>
<td><span data-ttu-id="d52eb-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="d52eb-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d52eb-550">436.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-550">436.00</span></span></td>
<td><span data-ttu-id="d52eb-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-552">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-552">CC003</span></span></td>
<td><span data-ttu-id="d52eb-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-553">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-554">55</span><span class="sxs-lookup"><span data-stu-id="d52eb-554">55</span></span></td>
<td><span data-ttu-id="d52eb-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="d52eb-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d52eb-556">685.14</span><span class="sxs-lookup"><span data-stu-id="d52eb-556">685.14</span></span></td>
<td><span data-ttu-id="d52eb-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-558">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-558">CC004</span></span></td>
<td><span data-ttu-id="d52eb-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-559">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-560">10</span><span class="sxs-lookup"><span data-stu-id="d52eb-560">10</span></span></td>
<td><span data-ttu-id="d52eb-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="d52eb-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d52eb-562">124.57</span><span class="sxs-lookup"><span data-stu-id="d52eb-562">124.57</span></span></td>
<td><span data-ttu-id="d52eb-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="d52eb-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-565">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="d52eb-566">Magnitude</span></span></th>
<th><span data-ttu-id="d52eb-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="d52eb-567">Allocation factor</span></span></th>
<th><span data-ttu-id="d52eb-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-568">Amount</span></span></th>
<th><span data-ttu-id="d52eb-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-570">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-570">CC003</span></span></td>
<td><span data-ttu-id="d52eb-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-571">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-572">65</span><span class="sxs-lookup"><span data-stu-id="d52eb-572">65</span></span></td>
<td><span data-ttu-id="d52eb-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d52eb-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d52eb-574">438.75</span><span class="sxs-lookup"><span data-stu-id="d52eb-574">438.75</span></span></td>
<td><span data-ttu-id="d52eb-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-576">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-576">CC004</span></span></td>
<td><span data-ttu-id="d52eb-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-577">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-578">35</span><span class="sxs-lookup"><span data-stu-id="d52eb-578">35</span></span></td>
<td><span data-ttu-id="d52eb-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d52eb-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d52eb-580">236.25</span><span class="sxs-lookup"><span data-stu-id="d52eb-580">236.25</span></span></td>
<td><span data-ttu-id="d52eb-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-582">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-582">CC003</span></span></td>
<td><span data-ttu-id="d52eb-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-583">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-584">65</span><span class="sxs-lookup"><span data-stu-id="d52eb-584">65</span></span></td>
<td><span data-ttu-id="d52eb-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d52eb-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d52eb-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d52eb-586">5,297.69</span></span></td>
<td><span data-ttu-id="d52eb-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-588">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-588">CC004</span></span></td>
<td><span data-ttu-id="d52eb-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-589">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-590">35</span><span class="sxs-lookup"><span data-stu-id="d52eb-590">35</span></span></td>
<td><span data-ttu-id="d52eb-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d52eb-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d52eb-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d52eb-592">2,852.60</span></span></td>
<td><span data-ttu-id="d52eb-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="d52eb-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-595">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="d52eb-596">Magnitude</span></span></th>
<th><span data-ttu-id="d52eb-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="d52eb-597">Allocation factor</span></span></th>
<th><span data-ttu-id="d52eb-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-598">Amount</span></span></th>
<th><span data-ttu-id="d52eb-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-600">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-601">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-602">60</span><span class="sxs-lookup"><span data-stu-id="d52eb-602">60</span></span></td>
<td><span data-ttu-id="d52eb-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d52eb-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d52eb-604">535.31</span><span class="sxs-lookup"><span data-stu-id="d52eb-604">535.31</span></span></td>
<td><span data-ttu-id="d52eb-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-606">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-607">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-608">20</span><span class="sxs-lookup"><span data-stu-id="d52eb-608">20</span></span></td>
<td><span data-ttu-id="d52eb-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d52eb-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d52eb-610">178.44</span><span class="sxs-lookup"><span data-stu-id="d52eb-610">178.44</span></span></td>
<td><span data-ttu-id="d52eb-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-612">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-613">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-614">60</span><span class="sxs-lookup"><span data-stu-id="d52eb-614">60</span></span></td>
<td><span data-ttu-id="d52eb-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d52eb-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d52eb-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d52eb-616">4,487.12</span></span></td>
<td><span data-ttu-id="d52eb-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-618">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-619">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-620">20</span><span class="sxs-lookup"><span data-stu-id="d52eb-620">20</span></span></td>
<td><span data-ttu-id="d52eb-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d52eb-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d52eb-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d52eb-622">1,495.71</span></span></td>
<td><span data-ttu-id="d52eb-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d52eb-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="d52eb-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-625">Cost object</span></span></th>
<th><span data-ttu-id="d52eb-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="d52eb-626">Magnitude</span></span></th>
<th><span data-ttu-id="d52eb-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="d52eb-627">Allocation factor</span></span></th>
<th><span data-ttu-id="d52eb-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-628">Amount</span></span></th>
<th><span data-ttu-id="d52eb-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-630">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-631">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-632">80</span><span class="sxs-lookup"><span data-stu-id="d52eb-632">80</span></span></td>
<td><span data-ttu-id="d52eb-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d52eb-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d52eb-634">241.05</span><span class="sxs-lookup"><span data-stu-id="d52eb-634">241.05</span></span></td>
<td><span data-ttu-id="d52eb-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-636">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-637">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-638">15</span><span class="sxs-lookup"><span data-stu-id="d52eb-638">15</span></span></td>
<td><span data-ttu-id="d52eb-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d52eb-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d52eb-640">45.20</span><span class="sxs-lookup"><span data-stu-id="d52eb-640">45.20</span></span></td>
<td><span data-ttu-id="d52eb-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-642">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-643">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-644">80</span><span class="sxs-lookup"><span data-stu-id="d52eb-644">80</span></span></td>
<td><span data-ttu-id="d52eb-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d52eb-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d52eb-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d52eb-646">2,507.09</span></span></td>
<td><span data-ttu-id="d52eb-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-648">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-649">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-650">15</span><span class="sxs-lookup"><span data-stu-id="d52eb-650">15</span></span></td>
<td><span data-ttu-id="d52eb-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d52eb-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d52eb-652">470.08</span><span class="sxs-lookup"><span data-stu-id="d52eb-652">470.08</span></span></td>
<td><span data-ttu-id="d52eb-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d52eb-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="d52eb-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-655">Journal</span></span></th>
<th><span data-ttu-id="d52eb-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d52eb-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="d52eb-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d52eb-658">Versie</span><span class="sxs-lookup"><span data-stu-id="d52eb-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-659">00004</span><span class="sxs-lookup"><span data-stu-id="d52eb-659">00004</span></span></td>
<td><span data-ttu-id="d52eb-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="d52eb-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-661">Fiscal</span></span></td>
<td><span data-ttu-id="d52eb-662">2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-662">2017</span></span></td>
<td><span data-ttu-id="d52eb-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-663">Period 1</span></span></td>
<td><span data-ttu-id="d52eb-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="d52eb-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="d52eb-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d52eb-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-668">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-669">Cost behavior</span></span></th>
<th><span data-ttu-id="d52eb-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-672">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-672">CC001</span></span></td>
<td><span data-ttu-id="d52eb-673">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-673">HR</span></span></td>
<td><span data-ttu-id="d52eb-674">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-674">10001</span></span></td>
<td><span data-ttu-id="d52eb-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-675">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-676">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-677">500,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-679">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-679">CC001</span></span></td>
<td><span data-ttu-id="d52eb-680">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-680">HR</span></span></td>
<td><span data-ttu-id="d52eb-681">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-681">10001</span></span></td>
<td><span data-ttu-id="d52eb-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-682">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-683">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="d52eb-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-686">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-686">CC002</span></span></td>
<td><span data-ttu-id="d52eb-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-687">Finance</span></span></td>
<td><span data-ttu-id="d52eb-688">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-688">10001</span></span></td>
<td><span data-ttu-id="d52eb-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-689">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-690">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-691">675.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-693">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-693">CC002</span></span></td>
<td><span data-ttu-id="d52eb-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-694">Finance</span></span></td>
<td><span data-ttu-id="d52eb-695">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-695">10001</span></span></td>
<td><span data-ttu-id="d52eb-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-696">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-697">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="d52eb-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-700">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-700">CC003</span></span></td>
<td><span data-ttu-id="d52eb-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-701">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-702">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-702">10001</span></span></td>
<td><span data-ttu-id="d52eb-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-703">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-704">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-705">713.75</span><span class="sxs-lookup"><span data-stu-id="d52eb-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-707">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-707">CC003</span></span></td>
<td><span data-ttu-id="d52eb-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-708">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-709">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-709">10001</span></span></td>
<td><span data-ttu-id="d52eb-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-710">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-711">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="d52eb-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-714">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-714">CC003</span></span></td>
<td><span data-ttu-id="d52eb-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-715">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-716">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-716">10001</span></span></td>
<td><span data-ttu-id="d52eb-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-717">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-718">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-719">286.25</span><span class="sxs-lookup"><span data-stu-id="d52eb-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-721">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-721">CC003</span></span></td>
<td><span data-ttu-id="d52eb-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-722">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-723">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-723">10001</span></span></td>
<td><span data-ttu-id="d52eb-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-724">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-725">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="d52eb-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-728">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-729">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-730">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-730">10001</span></span></td>
<td><span data-ttu-id="d52eb-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-731">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-732">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-733">776.36</span><span class="sxs-lookup"><span data-stu-id="d52eb-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-735">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-736">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-737">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-737">10001</span></span></td>
<td><span data-ttu-id="d52eb-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-738">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-739">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d52eb-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-742">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-743">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-744">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-744">10001</span></span></td>
<td><span data-ttu-id="d52eb-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-745">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-746">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-747">223.64</span><span class="sxs-lookup"><span data-stu-id="d52eb-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="d52eb-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-749">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-750">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-751">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-751">10001</span></span></td>
<td><span data-ttu-id="d52eb-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-752">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-753">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d52eb-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d52eb-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="d52eb-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d52eb-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d52eb-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-757">Cost element</span></span></th>
<th><span data-ttu-id="d52eb-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-758">Cost behavior</span></span></th>
<th><span data-ttu-id="d52eb-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="d52eb-759">Amount</span></span></th>
<th><span data-ttu-id="d52eb-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="d52eb-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d52eb-761">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-761">CC001</span></span></td>
<td><span data-ttu-id="d52eb-762">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-762">HR</span></span></td>
<td><span data-ttu-id="d52eb-763">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-763">10001</span></span></td>
<td><span data-ttu-id="d52eb-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-764">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-765">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-766">-500.00</span></span></td>
<td><span data-ttu-id="d52eb-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-768">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-768">CC002</span></span></td>
<td><span data-ttu-id="d52eb-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-769">Finance</span></span></td>
<td><span data-ttu-id="d52eb-770">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-770">10001</span></span></td>
<td><span data-ttu-id="d52eb-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-771">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-772">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-773">175.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-773">175.00</span></span></td>
<td><span data-ttu-id="d52eb-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-775">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-775">CC003</span></span></td>
<td><span data-ttu-id="d52eb-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-776">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-777">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-777">10001</span></span></td>
<td><span data-ttu-id="d52eb-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-778">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-779">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-780">275.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-780">275.00</span></span></td>
<td><span data-ttu-id="d52eb-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-782">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-782">CC004</span></span></td>
<td><span data-ttu-id="d52eb-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-783">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-784">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-784">10001</span></span></td>
<td><span data-ttu-id="d52eb-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-785">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-786">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-787">50,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-787">50,00</span></span></td>
<td><span data-ttu-id="d52eb-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-789">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-789">CC001</span></span></td>
<td><span data-ttu-id="d52eb-790">HR</span><span class="sxs-lookup"><span data-stu-id="d52eb-790">HR</span></span></td>
<td><span data-ttu-id="d52eb-791">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-791">10001</span></span></td>
<td><span data-ttu-id="d52eb-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-792">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-793">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="d52eb-794">-1,245.71</span></span></td>
<td><span data-ttu-id="d52eb-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-796">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-796">CC002</span></span></td>
<td><span data-ttu-id="d52eb-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-797">Finance</span></span></td>
<td><span data-ttu-id="d52eb-798">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-798">10001</span></span></td>
<td><span data-ttu-id="d52eb-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-799">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-800">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-801">436.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-801">436.00</span></span></td>
<td><span data-ttu-id="d52eb-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-803">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-803">CC003</span></span></td>
<td><span data-ttu-id="d52eb-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-804">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-805">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-805">10001</span></span></td>
<td><span data-ttu-id="d52eb-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-806">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-807">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-808">685.14</span><span class="sxs-lookup"><span data-stu-id="d52eb-808">685.14</span></span></td>
<td><span data-ttu-id="d52eb-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-810">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-810">CC004</span></span></td>
<td><span data-ttu-id="d52eb-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-811">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-812">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-812">10001</span></span></td>
<td><span data-ttu-id="d52eb-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-813">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-814">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-815">124.57</span><span class="sxs-lookup"><span data-stu-id="d52eb-815">124.57</span></span></td>
<td><span data-ttu-id="d52eb-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-817">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-817">CC002</span></span></td>
<td><span data-ttu-id="d52eb-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-818">Finance</span></span></td>
<td><span data-ttu-id="d52eb-819">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-819">10001</span></span></td>
<td><span data-ttu-id="d52eb-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-820">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-821">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="d52eb-822">-675.00</span></span></td>
<td><span data-ttu-id="d52eb-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-824">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-824">CC003</span></span></td>
<td><span data-ttu-id="d52eb-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-825">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-826">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-826">10001</span></span></td>
<td><span data-ttu-id="d52eb-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-827">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-828">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-829">438.75</span><span class="sxs-lookup"><span data-stu-id="d52eb-829">438.75</span></span></td>
<td><span data-ttu-id="d52eb-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-831">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-831">CC004</span></span></td>
<td><span data-ttu-id="d52eb-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-832">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-833">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-833">10001</span></span></td>
<td><span data-ttu-id="d52eb-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-834">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-835">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-836">236.25</span><span class="sxs-lookup"><span data-stu-id="d52eb-836">236.25</span></span></td>
<td><span data-ttu-id="d52eb-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-838">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-838">CC002</span></span></td>
<td><span data-ttu-id="d52eb-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="d52eb-839">Finance</span></span></td>
<td><span data-ttu-id="d52eb-840">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-840">10001</span></span></td>
<td><span data-ttu-id="d52eb-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-841">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-842">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="d52eb-843">-8,150.29</span></span></td>
<td><span data-ttu-id="d52eb-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-845">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-845">CC003</span></span></td>
<td><span data-ttu-id="d52eb-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-846">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-847">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-847">10001</span></span></td>
<td><span data-ttu-id="d52eb-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-848">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-849">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d52eb-850">5,297.69</span></span></td>
<td><span data-ttu-id="d52eb-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-852">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-852">CC004</span></span></td>
<td><span data-ttu-id="d52eb-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="d52eb-853">Packaging</span></span></td>
<td><span data-ttu-id="d52eb-854">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-854">10001</span></span></td>
<td><span data-ttu-id="d52eb-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-855">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-856">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d52eb-857">2,852.60</span></span></td>
<td><span data-ttu-id="d52eb-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-859">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-859">CC003</span></span></td>
<td><span data-ttu-id="d52eb-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-860">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-861">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-861">10001</span></span></td>
<td><span data-ttu-id="d52eb-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-862">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-863">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="d52eb-864">-713.75</span></span></td>
<td><span data-ttu-id="d52eb-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-866">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-867">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-868">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-868">10001</span></span></td>
<td><span data-ttu-id="d52eb-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-869">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-870">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-871">535.31</span><span class="sxs-lookup"><span data-stu-id="d52eb-871">535.31</span></span></td>
<td><span data-ttu-id="d52eb-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-873">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-874">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-875">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-875">10001</span></span></td>
<td><span data-ttu-id="d52eb-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-876">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-877">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-878">178.44</span><span class="sxs-lookup"><span data-stu-id="d52eb-878">178.44</span></span></td>
<td><span data-ttu-id="d52eb-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-880">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-880">CC003</span></span></td>
<td><span data-ttu-id="d52eb-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-881">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-882">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-882">10001</span></span></td>
<td><span data-ttu-id="d52eb-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-883">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-884">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="d52eb-885">-5,982.83</span></span></td>
<td><span data-ttu-id="d52eb-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-887">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-888">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-889">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-889">10001</span></span></td>
<td><span data-ttu-id="d52eb-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-890">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-891">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d52eb-892">4,487.12</span></span></td>
<td><span data-ttu-id="d52eb-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-894">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-895">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-896">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-896">10001</span></span></td>
<td><span data-ttu-id="d52eb-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-897">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-898">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d52eb-899">1,495.71</span></span></td>
<td><span data-ttu-id="d52eb-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-901">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-901">CC003</span></span></td>
<td><span data-ttu-id="d52eb-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-902">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-903">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-903">10001</span></span></td>
<td><span data-ttu-id="d52eb-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-904">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-905">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="d52eb-906">-286.25</span></span></td>
<td><span data-ttu-id="d52eb-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-908">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-909">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-910">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-910">10001</span></span></td>
<td><span data-ttu-id="d52eb-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-911">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-912">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-913">241.05</span><span class="sxs-lookup"><span data-stu-id="d52eb-913">241.05</span></span></td>
<td><span data-ttu-id="d52eb-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-915">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-916">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-917">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-917">10001</span></span></td>
<td><span data-ttu-id="d52eb-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-918">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-919">Fixed cost</span></span></td>
<td><span data-ttu-id="d52eb-920">45.20</span><span class="sxs-lookup"><span data-stu-id="d52eb-920">45.20</span></span></td>
<td><span data-ttu-id="d52eb-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-922">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-922">CC003</span></span></td>
<td><span data-ttu-id="d52eb-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="d52eb-923">Assembly</span></span></td>
<td><span data-ttu-id="d52eb-924">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-924">10001</span></span></td>
<td><span data-ttu-id="d52eb-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-925">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-926">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="d52eb-927">-2,977.17</span></span></td>
<td><span data-ttu-id="d52eb-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-929">Prod 1</span></span></td>
<td><span data-ttu-id="d52eb-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-930">Product 1</span></span></td>
<td><span data-ttu-id="d52eb-931">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-931">10001</span></span></td>
<td><span data-ttu-id="d52eb-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-932">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-933">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d52eb-934">2,507.09</span></span></td>
<td><span data-ttu-id="d52eb-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d52eb-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-936">Prod 2</span></span></td>
<td><span data-ttu-id="d52eb-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-937">Product 2</span></span></td>
<td><span data-ttu-id="d52eb-938">10001</span><span class="sxs-lookup"><span data-stu-id="d52eb-938">10001</span></span></td>
<td><span data-ttu-id="d52eb-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-939">Electricity</span></span></td>
<td><span data-ttu-id="d52eb-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-940">Variable cost</span></span></td>
<td><span data-ttu-id="d52eb-941">470.08</span><span class="sxs-lookup"><span data-stu-id="d52eb-941">470.08</span></span></td>
<td><span data-ttu-id="d52eb-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="d52eb-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="d52eb-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="d52eb-943">Conclusion</span></span>
<span data-ttu-id="d52eb-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="d52eb-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="d52eb-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d52eb-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="d52eb-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d52eb-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="d52eb-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="d52eb-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="d52eb-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="d52eb-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="d52eb-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="d52eb-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="d52eb-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d52eb-951">CC099</span><span class="sxs-lookup"><span data-stu-id="d52eb-951">CC099</span></span></th>
<th><span data-ttu-id="d52eb-952">CC001</span><span class="sxs-lookup"><span data-stu-id="d52eb-952">CC001</span></span></th>
<th><span data-ttu-id="d52eb-953">CC002</span><span class="sxs-lookup"><span data-stu-id="d52eb-953">CC002</span></span></th>
<th><span data-ttu-id="d52eb-954">CC003</span><span class="sxs-lookup"><span data-stu-id="d52eb-954">CC003</span></span></th>
<th><span data-ttu-id="d52eb-955">CC004</span><span class="sxs-lookup"><span data-stu-id="d52eb-955">CC004</span></span></th>
<th><span data-ttu-id="d52eb-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-956">Proj 1</span></span></th>
<th><span data-ttu-id="d52eb-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-957">Proj 2</span></span></th>
<th><span data-ttu-id="d52eb-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d52eb-958">Prod 1</span></span></th>
<th><span data-ttu-id="d52eb-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d52eb-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="d52eb-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="d52eb-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="d52eb-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="d52eb-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-971">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="d52eb-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-973">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-974">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-975">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-976">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-977">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-978">776.36</span><span class="sxs-lookup"><span data-stu-id="d52eb-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-979">223.64</span><span class="sxs-lookup"><span data-stu-id="d52eb-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="d52eb-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="d52eb-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-982">000</span><span class="sxs-lookup"><span data-stu-id="d52eb-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-983">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-984">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-985">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-986">0,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-987">30,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-988">10,00</span><span class="sxs-lookup"><span data-stu-id="d52eb-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d52eb-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d52eb-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d52eb-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d52eb-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d52eb-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="d52eb-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="d52eb-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="d52eb-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="d52eb-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="d52eb-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="d52eb-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d52eb-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="d52eb-996">Zie [Beleid voor totalisering van kosten en overheadberekening](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d52eb-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]