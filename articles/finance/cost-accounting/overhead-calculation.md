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
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442073"
---
# <a name="overhead-calculation"></a><span data-ttu-id="b22f1-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="b22f1-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b22f1-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="b22f1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="b22f1-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="b22f1-105">Term definition</span></span>
---------------

<span data-ttu-id="b22f1-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="b22f1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="b22f1-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="b22f1-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="b22f1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="b22f1-109">Huur</span><span class="sxs-lookup"><span data-stu-id="b22f1-109">Rent</span></span>
-   <span data-ttu-id="b22f1-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-110">Electricity</span></span>
-   <span data-ttu-id="b22f1-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="b22f1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="b22f1-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="b22f1-112">Overhead calculation overview</span></span>
<span data-ttu-id="b22f1-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b22f1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="b22f1-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="b22f1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="b22f1-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="b22f1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="b22f1-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="b22f1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="b22f1-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="b22f1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="b22f1-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="b22f1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="b22f1-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="b22f1-119">Version type</span></span>
-   <span data-ttu-id="b22f1-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="b22f1-120">Date and time</span></span>
-   <span data-ttu-id="b22f1-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="b22f1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="b22f1-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="b22f1-122">Fiscal year</span></span>
-   <span data-ttu-id="b22f1-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="b22f1-123">Fiscal period</span></span>

<span data-ttu-id="b22f1-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b22f1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="b22f1-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="b22f1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="b22f1-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b22f1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="b22f1-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="b22f1-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="b22f1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="b22f1-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="b22f1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="b22f1-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="b22f1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="b22f1-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="b22f1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="b22f1-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="b22f1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="b22f1-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="b22f1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="b22f1-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="b22f1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="b22f1-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="b22f1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="b22f1-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="b22f1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="b22f1-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="b22f1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="b22f1-140">Main account</span></span></th>
<th><span data-ttu-id="b22f1-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="b22f1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="b22f1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-143">CC099</span></span></td>
<td><span data-ttu-id="b22f1-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-144">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-145">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-145">10001</span></span></td>
<td><span data-ttu-id="b22f1-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-146">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="b22f1-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="b22f1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="b22f1-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="b22f1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="b22f1-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="b22f1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="b22f1-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="b22f1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="b22f1-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="b22f1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="b22f1-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="b22f1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="b22f1-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="b22f1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="b22f1-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="b22f1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="b22f1-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="b22f1-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="b22f1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="b22f1-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="b22f1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="b22f1-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-160">Journal</span></span></th>
<th><span data-ttu-id="b22f1-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b22f1-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="b22f1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b22f1-163">Versie</span><span class="sxs-lookup"><span data-stu-id="b22f1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-164">00001</span><span class="sxs-lookup"><span data-stu-id="b22f1-164">00001</span></span></td>
<td><span data-ttu-id="b22f1-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="b22f1-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-166">Fiscal</span></span></td>
<td><span data-ttu-id="b22f1-167">2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-167">2017</span></span></td>
<td><span data-ttu-id="b22f1-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-168">Period 1</span></span></td>
<td><span data-ttu-id="b22f1-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b22f1-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="b22f1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-173">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="b22f1-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="b22f1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-177">CC099</span></span></td>
<td><span data-ttu-id="b22f1-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-178">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-179">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-179">10001</span></span></td>
<td><span data-ttu-id="b22f1-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-180">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="b22f1-181">Unclassified</span></span></td>
<td><span data-ttu-id="b22f1-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b22f1-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="b22f1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-185">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="b22f1-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-187">Amount</span></span></th>
<th><span data-ttu-id="b22f1-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-189">CC099</span></span></td>
<td><span data-ttu-id="b22f1-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-190">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-191">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-191">10001</span></span></td>
<td><span data-ttu-id="b22f1-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-192">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="b22f1-193">Unclassified</span></span></td>
<td><span data-ttu-id="b22f1-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-194">10,000.00</span></span></td>
<td><span data-ttu-id="b22f1-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-196">CC099</span></span></td>
<td><span data-ttu-id="b22f1-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-197">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-198">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-198">10001</span></span></td>
<td><span data-ttu-id="b22f1-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-199">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="b22f1-200">Unclassified</span></span></td>
<td><span data-ttu-id="b22f1-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="b22f1-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-203">CC099</span></span></td>
<td><span data-ttu-id="b22f1-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-204">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-205">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-205">10001</span></span></td>
<td><span data-ttu-id="b22f1-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-206">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-208">1,000.00</span></span></td>
<td><span data-ttu-id="b22f1-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-210">CC099</span></span></td>
<td><span data-ttu-id="b22f1-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-211">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-212">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-212">10001</span></span></td>
<td><span data-ttu-id="b22f1-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-213">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-214">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-215">9,000.00</span></span></td>
<td><span data-ttu-id="b22f1-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b22f1-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="b22f1-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="b22f1-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="b22f1-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="b22f1-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="b22f1-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="b22f1-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="b22f1-221">Define the cost distribution rule</span></span>

<span data-ttu-id="b22f1-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="b22f1-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="b22f1-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="b22f1-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="b22f1-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="b22f1-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="b22f1-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="b22f1-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="b22f1-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="b22f1-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="b22f1-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-228">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="b22f1-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-230">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-230">CC001</span></span></td>
<td><span data-ttu-id="b22f1-231">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-231">HR</span></span></td>
<td><span data-ttu-id="b22f1-232">1.000</span><span class="sxs-lookup"><span data-stu-id="b22f1-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-233">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-233">CC002</span></span></td>
<td><span data-ttu-id="b22f1-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-234">Finance</span></span></td>
<td><span data-ttu-id="b22f1-235">6.000</span><span class="sxs-lookup"><span data-stu-id="b22f1-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-236">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-236">CC003</span></span></td>
<td><span data-ttu-id="b22f1-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-237">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-238">0</span><span class="sxs-lookup"><span data-stu-id="b22f1-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-240">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="b22f1-241">Magnitude</span></span></th>
<th><span data-ttu-id="b22f1-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="b22f1-242">Allocation factor</span></span></th>
<th><span data-ttu-id="b22f1-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-244">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-244">CC001</span></span></td>
<td><span data-ttu-id="b22f1-245">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-245">HR</span></span></td>
<td><span data-ttu-id="b22f1-246">1.000</span><span class="sxs-lookup"><span data-stu-id="b22f1-246">1,000</span></span></td>
<td><span data-ttu-id="b22f1-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b22f1-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b22f1-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-249">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-249">CC002</span></span></td>
<td><span data-ttu-id="b22f1-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-250">Finance</span></span></td>
<td><span data-ttu-id="b22f1-251">6.000</span><span class="sxs-lookup"><span data-stu-id="b22f1-251">6,000</span></span></td>
<td><span data-ttu-id="b22f1-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b22f1-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b22f1-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-254">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-254">CC003</span></span></td>
<td><span data-ttu-id="b22f1-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-255">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-256">0</span><span class="sxs-lookup"><span data-stu-id="b22f1-256">0</span></span></td>
<td><span data-ttu-id="b22f1-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b22f1-258">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="b22f1-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="b22f1-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-261">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-262">Formule</span><span class="sxs-lookup"><span data-stu-id="b22f1-262">Formula</span></span></th>
<th><span data-ttu-id="b22f1-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="b22f1-263">Magnitude</span></span></th>
<th><span data-ttu-id="b22f1-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="b22f1-264">Allocation factor</span></span></th>
<th><span data-ttu-id="b22f1-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-266">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-266">CC001</span></span></td>
<td><span data-ttu-id="b22f1-267">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-267">HR</span></span></td>
<td><span data-ttu-id="b22f1-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b22f1-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b22f1-269">1</span><span class="sxs-lookup"><span data-stu-id="b22f1-269">1</span></span></td>
<td><span data-ttu-id="b22f1-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b22f1-271">500,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-272">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-272">CC002</span></span></td>
<td><span data-ttu-id="b22f1-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-273">Finance</span></span></td>
<td><span data-ttu-id="b22f1-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b22f1-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b22f1-275">1</span><span class="sxs-lookup"><span data-stu-id="b22f1-275">1</span></span></td>
<td><span data-ttu-id="b22f1-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b22f1-277">500,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-278">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-278">CC003</span></span></td>
<td><span data-ttu-id="b22f1-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-279">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b22f1-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b22f1-281">0</span><span class="sxs-lookup"><span data-stu-id="b22f1-281">0</span></span></td>
<td><span data-ttu-id="b22f1-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b22f1-283">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b22f1-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-285">Journal</span></span></th>
<th><span data-ttu-id="b22f1-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b22f1-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="b22f1-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b22f1-288">Versie</span><span class="sxs-lookup"><span data-stu-id="b22f1-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-289">00002</span><span class="sxs-lookup"><span data-stu-id="b22f1-289">00002</span></span></td>
<td><span data-ttu-id="b22f1-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="b22f1-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="b22f1-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-291">Fiscal</span></span></td>
<td><span data-ttu-id="b22f1-292">2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-292">2017</span></span></td>
<td><span data-ttu-id="b22f1-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-293">Period 1</span></span></td>
<td><span data-ttu-id="b22f1-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b22f1-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="b22f1-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-298">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-299">Cost behavior</span></span></th>
<th><span data-ttu-id="b22f1-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-302">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-302">CC099</span></span></td>
<td><span data-ttu-id="b22f1-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-303">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-304">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-304">10001</span></span></td>
<td><span data-ttu-id="b22f1-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-305">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-306">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-309">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-309">CC099</span></span></td>
<td><span data-ttu-id="b22f1-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-310">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-311">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-311">10001</span></span></td>
<td><span data-ttu-id="b22f1-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-312">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-313">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b22f1-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="b22f1-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-317">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-318">Cost behavior</span></span></th>
<th><span data-ttu-id="b22f1-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-319">Amount</span></span></th>
<th><span data-ttu-id="b22f1-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-321">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-321">CC099</span></span></td>
<td><span data-ttu-id="b22f1-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-322">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-323">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-323">10001</span></span></td>
<td><span data-ttu-id="b22f1-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-324">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-325">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-326">-1,000.00</span></span></td>
<td><span data-ttu-id="b22f1-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-328">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-328">CC001</span></span></td>
<td><span data-ttu-id="b22f1-329">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-329">HR</span></span></td>
<td><span data-ttu-id="b22f1-330">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-330">10001</span></span></td>
<td><span data-ttu-id="b22f1-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-331">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-332">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-333">500,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-333">500.00</span></span></td>
<td><span data-ttu-id="b22f1-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-335">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-335">CC002</span></span></td>
<td><span data-ttu-id="b22f1-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-336">Finance</span></span></td>
<td><span data-ttu-id="b22f1-337">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-337">10001</span></span></td>
<td><span data-ttu-id="b22f1-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-338">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-339">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-340">500,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-340">500.00</span></span></td>
<td><span data-ttu-id="b22f1-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-342">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-342">CC099</span></span></td>
<td><span data-ttu-id="b22f1-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="b22f1-343">Default cost center</span></span></td>
<td><span data-ttu-id="b22f1-344">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-344">10001</span></span></td>
<td><span data-ttu-id="b22f1-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-345">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-346">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-347">-9,000.00</span></span></td>
<td><span data-ttu-id="b22f1-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-349">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-349">CC001</span></span></td>
<td><span data-ttu-id="b22f1-350">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-350">HR</span></span></td>
<td><span data-ttu-id="b22f1-351">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-351">10001</span></span></td>
<td><span data-ttu-id="b22f1-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-352">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-353">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b22f1-354">1,285.71</span></span></td>
<td><span data-ttu-id="b22f1-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-356">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-356">CC002</span></span></td>
<td><span data-ttu-id="b22f1-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-357">Finance</span></span></td>
<td><span data-ttu-id="b22f1-358">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-358">10001</span></span></td>
<td><span data-ttu-id="b22f1-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-359">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-360">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b22f1-361">7,714.29</span></span></td>
<td><span data-ttu-id="b22f1-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b22f1-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="b22f1-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="b22f1-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="b22f1-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="b22f1-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="b22f1-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="b22f1-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="b22f1-367">Define the overhead rate</span></span>

<span data-ttu-id="b22f1-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="b22f1-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-370">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-371">Uren</span><span class="sxs-lookup"><span data-stu-id="b22f1-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-372">Proj 1</span></span></td>
<td><span data-ttu-id="b22f1-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-373">Project 1</span></span></td>
<td><span data-ttu-id="b22f1-374">3</span><span class="sxs-lookup"><span data-stu-id="b22f1-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-375">Proj 2</span></span></td>
<td><span data-ttu-id="b22f1-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-376">Project 2</span></span></td>
<td><span data-ttu-id="b22f1-377">1</span><span class="sxs-lookup"><span data-stu-id="b22f1-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="b22f1-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-379">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-380">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-381">Cost behavior</span></span></th>
<th><span data-ttu-id="b22f1-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="b22f1-382">Units</span></span></th>
<th><span data-ttu-id="b22f1-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="b22f1-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-384">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-384">CC001</span></span></td>
<td><span data-ttu-id="b22f1-385">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-385">HR</span></span></td>
<td><span data-ttu-id="b22f1-386">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-386">10001</span></span></td>
<td><span data-ttu-id="b22f1-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-387">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-388">1</span><span class="sxs-lookup"><span data-stu-id="b22f1-388">1</span></span></td>
<td><span data-ttu-id="b22f1-389">10</span><span class="sxs-lookup"><span data-stu-id="b22f1-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="b22f1-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-391">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="b22f1-392">Magnitude</span></span></th>
<th><span data-ttu-id="b22f1-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-393">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="b22f1-394">Allocation factor</span></span></th>
<th><span data-ttu-id="b22f1-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-396">Proj 1</span></span></td>
<td><span data-ttu-id="b22f1-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-397">Project 1</span></span></td>
<td><span data-ttu-id="b22f1-398">3</span><span class="sxs-lookup"><span data-stu-id="b22f1-398">3</span></span></td>
<td><span data-ttu-id="b22f1-399">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-399">10001</span></span></td>
<td><span data-ttu-id="b22f1-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b22f1-401">30,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-402">Proj 2</span></span></td>
<td><span data-ttu-id="b22f1-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-403">Project 2</span></span></td>
<td><span data-ttu-id="b22f1-404">1</span><span class="sxs-lookup"><span data-stu-id="b22f1-404">1</span></span></td>
<td><span data-ttu-id="b22f1-405">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-405">10001</span></span></td>
<td><span data-ttu-id="b22f1-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b22f1-407">10,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b22f1-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-409">Journal</span></span></th>
<th><span data-ttu-id="b22f1-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b22f1-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="b22f1-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b22f1-412">Versie</span><span class="sxs-lookup"><span data-stu-id="b22f1-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-413">00003</span><span class="sxs-lookup"><span data-stu-id="b22f1-413">00003</span></span></td>
<td><span data-ttu-id="b22f1-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="b22f1-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="b22f1-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-415">Fiscal</span></span></td>
<td><span data-ttu-id="b22f1-416">2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-416">2017</span></span></td>
<td><span data-ttu-id="b22f1-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-417">Period 1</span></span></td>
<td><span data-ttu-id="b22f1-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="b22f1-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="b22f1-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-421">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="b22f1-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-424">Proj 1</span></span></td>
<td><span data-ttu-id="b22f1-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b22f1-426">3,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-428">Proj 2</span></span></td>
<td><span data-ttu-id="b22f1-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b22f1-430">1,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b22f1-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="b22f1-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-433">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-434">Cost behavior</span></span></th>
<th><span data-ttu-id="b22f1-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-435">Amount</span></span></th>
<th><span data-ttu-id="b22f1-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="b22f1-437">CC0001</span></span></td>
<td><span data-ttu-id="b22f1-438">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-438">HR</span></span></td>
<td><span data-ttu-id="b22f1-439">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-439">10001</span></span></td>
<td><span data-ttu-id="b22f1-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-440">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-441">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-442">-30.00</span></span></td>
<td><span data-ttu-id="b22f1-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-444">Proj 1</span></span></td>
<td><span data-ttu-id="b22f1-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b22f1-446">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-446">10001</span></span></td>
<td><span data-ttu-id="b22f1-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-447">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-448">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-449">30,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-449">30.00</span></span></td>
<td><span data-ttu-id="b22f1-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-451">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-451">CC001</span></span></td>
<td><span data-ttu-id="b22f1-452">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-452">HR</span></span></td>
<td><span data-ttu-id="b22f1-453">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-453">10001</span></span></td>
<td><span data-ttu-id="b22f1-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-454">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-455">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-456">-10.00</span></span></td>
<td><span data-ttu-id="b22f1-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-458">Proj 2</span></span></td>
<td><span data-ttu-id="b22f1-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b22f1-460">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-460">10001</span></span></td>
<td><span data-ttu-id="b22f1-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-461">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-462">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-463">10.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-463">10.00</span></span></td>
<td><span data-ttu-id="b22f1-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="b22f1-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="b22f1-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="b22f1-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="b22f1-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="b22f1-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="b22f1-468">Finance ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="b22f1-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="b22f1-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="b22f1-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="b22f1-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="b22f1-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="b22f1-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="b22f1-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="b22f1-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="b22f1-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="b22f1-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="b22f1-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="b22f1-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="b22f1-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="b22f1-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="b22f1-475">Define the cost allocation</span></span>

<span data-ttu-id="b22f1-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="b22f1-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="b22f1-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="b22f1-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-479">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="b22f1-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-481">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-481">CC002</span></span></td>
<td><span data-ttu-id="b22f1-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-482">Finance</span></span></td>
<td><span data-ttu-id="b22f1-483">35</span><span class="sxs-lookup"><span data-stu-id="b22f1-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-484">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-484">CC003</span></span></td>
<td><span data-ttu-id="b22f1-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-485">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-486">55</span><span class="sxs-lookup"><span data-stu-id="b22f1-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-487">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-487">CC004</span></span></td>
<td><span data-ttu-id="b22f1-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-488">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-489">10</span><span class="sxs-lookup"><span data-stu-id="b22f1-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="b22f1-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-492">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="b22f1-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-494">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-494">CC003</span></span></td>
<td><span data-ttu-id="b22f1-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-495">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-496">65</span><span class="sxs-lookup"><span data-stu-id="b22f1-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-497">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-497">CC004</span></span></td>
<td><span data-ttu-id="b22f1-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-498">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-499">35</span><span class="sxs-lookup"><span data-stu-id="b22f1-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="b22f1-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-502">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="b22f1-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-504">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-505">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-506">60</span><span class="sxs-lookup"><span data-stu-id="b22f1-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-507">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-508">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-509">20</span><span class="sxs-lookup"><span data-stu-id="b22f1-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="b22f1-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-512">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="b22f1-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-514">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-515">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-516">80</span><span class="sxs-lookup"><span data-stu-id="b22f1-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-517">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-518">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-519">15</span><span class="sxs-lookup"><span data-stu-id="b22f1-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b22f1-520">Statistische metingen, zoals de productie-uren die een product verbruikt, kunnen worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="b22f1-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="b22f1-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b22f1-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="b22f1-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="b22f1-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-523">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="b22f1-524">Magnitude</span></span></th>
<th><span data-ttu-id="b22f1-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="b22f1-525">Allocation factor</span></span></th>
<th><span data-ttu-id="b22f1-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-526">Amount</span></span></th>
<th><span data-ttu-id="b22f1-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-528">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-528">CC002</span></span></td>
<td><span data-ttu-id="b22f1-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-529">Finance</span></span></td>
<td><span data-ttu-id="b22f1-530">35</span><span class="sxs-lookup"><span data-stu-id="b22f1-530">35</span></span></td>
<td><span data-ttu-id="b22f1-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b22f1-532">175.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-532">175.00</span></span></td>
<td><span data-ttu-id="b22f1-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-534">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-534">CC003</span></span></td>
<td><span data-ttu-id="b22f1-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-535">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-536">55</span><span class="sxs-lookup"><span data-stu-id="b22f1-536">55</span></span></td>
<td><span data-ttu-id="b22f1-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b22f1-538">275.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-538">275.00</span></span></td>
<td><span data-ttu-id="b22f1-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-540">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-540">CC004</span></span></td>
<td><span data-ttu-id="b22f1-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-541">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-542">10</span><span class="sxs-lookup"><span data-stu-id="b22f1-542">10</span></span></td>
<td><span data-ttu-id="b22f1-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b22f1-544">50,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-544">50.00</span></span></td>
<td><span data-ttu-id="b22f1-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-546">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-546">CC002</span></span></td>
<td><span data-ttu-id="b22f1-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-547">Finance</span></span></td>
<td><span data-ttu-id="b22f1-548">35</span><span class="sxs-lookup"><span data-stu-id="b22f1-548">35</span></span></td>
<td><span data-ttu-id="b22f1-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b22f1-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b22f1-550">436.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-550">436.00</span></span></td>
<td><span data-ttu-id="b22f1-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-552">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-552">CC003</span></span></td>
<td><span data-ttu-id="b22f1-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-553">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-554">55</span><span class="sxs-lookup"><span data-stu-id="b22f1-554">55</span></span></td>
<td><span data-ttu-id="b22f1-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b22f1-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b22f1-556">685.14</span><span class="sxs-lookup"><span data-stu-id="b22f1-556">685.14</span></span></td>
<td><span data-ttu-id="b22f1-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-558">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-558">CC004</span></span></td>
<td><span data-ttu-id="b22f1-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-559">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-560">10</span><span class="sxs-lookup"><span data-stu-id="b22f1-560">10</span></span></td>
<td><span data-ttu-id="b22f1-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b22f1-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b22f1-562">124.57</span><span class="sxs-lookup"><span data-stu-id="b22f1-562">124.57</span></span></td>
<td><span data-ttu-id="b22f1-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="b22f1-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-565">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="b22f1-566">Magnitude</span></span></th>
<th><span data-ttu-id="b22f1-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="b22f1-567">Allocation factor</span></span></th>
<th><span data-ttu-id="b22f1-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-568">Amount</span></span></th>
<th><span data-ttu-id="b22f1-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-570">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-570">CC003</span></span></td>
<td><span data-ttu-id="b22f1-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-571">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-572">65</span><span class="sxs-lookup"><span data-stu-id="b22f1-572">65</span></span></td>
<td><span data-ttu-id="b22f1-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b22f1-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b22f1-574">438.75</span><span class="sxs-lookup"><span data-stu-id="b22f1-574">438.75</span></span></td>
<td><span data-ttu-id="b22f1-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-576">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-576">CC004</span></span></td>
<td><span data-ttu-id="b22f1-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-577">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-578">35</span><span class="sxs-lookup"><span data-stu-id="b22f1-578">35</span></span></td>
<td><span data-ttu-id="b22f1-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b22f1-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b22f1-580">236.25</span><span class="sxs-lookup"><span data-stu-id="b22f1-580">236.25</span></span></td>
<td><span data-ttu-id="b22f1-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-582">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-582">CC003</span></span></td>
<td><span data-ttu-id="b22f1-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-583">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-584">65</span><span class="sxs-lookup"><span data-stu-id="b22f1-584">65</span></span></td>
<td><span data-ttu-id="b22f1-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b22f1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b22f1-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b22f1-586">5,297.69</span></span></td>
<td><span data-ttu-id="b22f1-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-588">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-588">CC004</span></span></td>
<td><span data-ttu-id="b22f1-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-589">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-590">35</span><span class="sxs-lookup"><span data-stu-id="b22f1-590">35</span></span></td>
<td><span data-ttu-id="b22f1-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b22f1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b22f1-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b22f1-592">2,852.60</span></span></td>
<td><span data-ttu-id="b22f1-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="b22f1-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-595">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="b22f1-596">Magnitude</span></span></th>
<th><span data-ttu-id="b22f1-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="b22f1-597">Allocation factor</span></span></th>
<th><span data-ttu-id="b22f1-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-598">Amount</span></span></th>
<th><span data-ttu-id="b22f1-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-600">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-601">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-602">60</span><span class="sxs-lookup"><span data-stu-id="b22f1-602">60</span></span></td>
<td><span data-ttu-id="b22f1-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b22f1-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b22f1-604">535.31</span><span class="sxs-lookup"><span data-stu-id="b22f1-604">535.31</span></span></td>
<td><span data-ttu-id="b22f1-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-606">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-607">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-608">20</span><span class="sxs-lookup"><span data-stu-id="b22f1-608">20</span></span></td>
<td><span data-ttu-id="b22f1-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b22f1-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b22f1-610">178.44</span><span class="sxs-lookup"><span data-stu-id="b22f1-610">178.44</span></span></td>
<td><span data-ttu-id="b22f1-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-612">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-613">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-614">60</span><span class="sxs-lookup"><span data-stu-id="b22f1-614">60</span></span></td>
<td><span data-ttu-id="b22f1-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b22f1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b22f1-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b22f1-616">4,487.12</span></span></td>
<td><span data-ttu-id="b22f1-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-618">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-619">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-620">20</span><span class="sxs-lookup"><span data-stu-id="b22f1-620">20</span></span></td>
<td><span data-ttu-id="b22f1-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b22f1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b22f1-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b22f1-622">1,495.71</span></span></td>
<td><span data-ttu-id="b22f1-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b22f1-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="b22f1-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-625">Cost object</span></span></th>
<th><span data-ttu-id="b22f1-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="b22f1-626">Magnitude</span></span></th>
<th><span data-ttu-id="b22f1-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="b22f1-627">Allocation factor</span></span></th>
<th><span data-ttu-id="b22f1-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-628">Amount</span></span></th>
<th><span data-ttu-id="b22f1-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-630">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-631">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-632">80</span><span class="sxs-lookup"><span data-stu-id="b22f1-632">80</span></span></td>
<td><span data-ttu-id="b22f1-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b22f1-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b22f1-634">241.05</span><span class="sxs-lookup"><span data-stu-id="b22f1-634">241.05</span></span></td>
<td><span data-ttu-id="b22f1-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-636">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-637">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-638">15</span><span class="sxs-lookup"><span data-stu-id="b22f1-638">15</span></span></td>
<td><span data-ttu-id="b22f1-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b22f1-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b22f1-640">45.20</span><span class="sxs-lookup"><span data-stu-id="b22f1-640">45.20</span></span></td>
<td><span data-ttu-id="b22f1-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-642">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-643">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-644">80</span><span class="sxs-lookup"><span data-stu-id="b22f1-644">80</span></span></td>
<td><span data-ttu-id="b22f1-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b22f1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b22f1-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b22f1-646">2,507.09</span></span></td>
<td><span data-ttu-id="b22f1-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-648">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-649">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-650">15</span><span class="sxs-lookup"><span data-stu-id="b22f1-650">15</span></span></td>
<td><span data-ttu-id="b22f1-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b22f1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b22f1-652">470.08</span><span class="sxs-lookup"><span data-stu-id="b22f1-652">470.08</span></span></td>
<td><span data-ttu-id="b22f1-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b22f1-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="b22f1-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-655">Journal</span></span></th>
<th><span data-ttu-id="b22f1-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b22f1-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="b22f1-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b22f1-658">Versie</span><span class="sxs-lookup"><span data-stu-id="b22f1-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-659">00004</span><span class="sxs-lookup"><span data-stu-id="b22f1-659">00004</span></span></td>
<td><span data-ttu-id="b22f1-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="b22f1-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-661">Fiscal</span></span></td>
<td><span data-ttu-id="b22f1-662">2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-662">2017</span></span></td>
<td><span data-ttu-id="b22f1-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-663">Period 1</span></span></td>
<td><span data-ttu-id="b22f1-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="b22f1-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="b22f1-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b22f1-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-668">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-669">Cost behavior</span></span></th>
<th><span data-ttu-id="b22f1-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-672">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-672">CC001</span></span></td>
<td><span data-ttu-id="b22f1-673">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-673">HR</span></span></td>
<td><span data-ttu-id="b22f1-674">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-674">10001</span></span></td>
<td><span data-ttu-id="b22f1-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-675">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-676">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-677">500,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-679">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-679">CC001</span></span></td>
<td><span data-ttu-id="b22f1-680">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-680">HR</span></span></td>
<td><span data-ttu-id="b22f1-681">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-681">10001</span></span></td>
<td><span data-ttu-id="b22f1-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-682">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-683">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="b22f1-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-686">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-686">CC002</span></span></td>
<td><span data-ttu-id="b22f1-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-687">Finance</span></span></td>
<td><span data-ttu-id="b22f1-688">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-688">10001</span></span></td>
<td><span data-ttu-id="b22f1-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-689">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-690">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-691">675.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-693">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-693">CC002</span></span></td>
<td><span data-ttu-id="b22f1-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-694">Finance</span></span></td>
<td><span data-ttu-id="b22f1-695">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-695">10001</span></span></td>
<td><span data-ttu-id="b22f1-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-696">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-697">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="b22f1-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-700">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-700">CC003</span></span></td>
<td><span data-ttu-id="b22f1-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-701">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-702">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-702">10001</span></span></td>
<td><span data-ttu-id="b22f1-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-703">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-704">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-705">713.75</span><span class="sxs-lookup"><span data-stu-id="b22f1-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-707">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-707">CC003</span></span></td>
<td><span data-ttu-id="b22f1-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-708">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-709">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-709">10001</span></span></td>
<td><span data-ttu-id="b22f1-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-710">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-711">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="b22f1-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-714">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-714">CC003</span></span></td>
<td><span data-ttu-id="b22f1-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-715">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-716">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-716">10001</span></span></td>
<td><span data-ttu-id="b22f1-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-717">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-718">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-719">286.25</span><span class="sxs-lookup"><span data-stu-id="b22f1-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-721">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-721">CC003</span></span></td>
<td><span data-ttu-id="b22f1-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-722">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-723">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-723">10001</span></span></td>
<td><span data-ttu-id="b22f1-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-724">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-725">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="b22f1-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-728">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-729">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-730">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-730">10001</span></span></td>
<td><span data-ttu-id="b22f1-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-731">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-732">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-733">776.36</span><span class="sxs-lookup"><span data-stu-id="b22f1-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-735">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-736">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-737">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-737">10001</span></span></td>
<td><span data-ttu-id="b22f1-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-738">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-739">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b22f1-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-742">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-743">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-744">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-744">10001</span></span></td>
<td><span data-ttu-id="b22f1-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-745">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-746">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-747">223.64</span><span class="sxs-lookup"><span data-stu-id="b22f1-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="b22f1-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-749">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-750">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-751">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-751">10001</span></span></td>
<td><span data-ttu-id="b22f1-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-752">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-753">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b22f1-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b22f1-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="b22f1-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b22f1-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b22f1-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-757">Cost element</span></span></th>
<th><span data-ttu-id="b22f1-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-758">Cost behavior</span></span></th>
<th><span data-ttu-id="b22f1-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="b22f1-759">Amount</span></span></th>
<th><span data-ttu-id="b22f1-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="b22f1-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b22f1-761">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-761">CC001</span></span></td>
<td><span data-ttu-id="b22f1-762">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-762">HR</span></span></td>
<td><span data-ttu-id="b22f1-763">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-763">10001</span></span></td>
<td><span data-ttu-id="b22f1-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-764">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-765">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-766">-500.00</span></span></td>
<td><span data-ttu-id="b22f1-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-768">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-768">CC002</span></span></td>
<td><span data-ttu-id="b22f1-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-769">Finance</span></span></td>
<td><span data-ttu-id="b22f1-770">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-770">10001</span></span></td>
<td><span data-ttu-id="b22f1-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-771">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-772">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-773">175.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-773">175.00</span></span></td>
<td><span data-ttu-id="b22f1-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-775">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-775">CC003</span></span></td>
<td><span data-ttu-id="b22f1-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-776">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-777">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-777">10001</span></span></td>
<td><span data-ttu-id="b22f1-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-778">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-779">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-780">275.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-780">275.00</span></span></td>
<td><span data-ttu-id="b22f1-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-782">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-782">CC004</span></span></td>
<td><span data-ttu-id="b22f1-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-783">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-784">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-784">10001</span></span></td>
<td><span data-ttu-id="b22f1-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-785">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-786">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-787">50,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-787">50,00</span></span></td>
<td><span data-ttu-id="b22f1-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-789">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-789">CC001</span></span></td>
<td><span data-ttu-id="b22f1-790">HR</span><span class="sxs-lookup"><span data-stu-id="b22f1-790">HR</span></span></td>
<td><span data-ttu-id="b22f1-791">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-791">10001</span></span></td>
<td><span data-ttu-id="b22f1-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-792">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-793">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="b22f1-794">-1,245.71</span></span></td>
<td><span data-ttu-id="b22f1-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-796">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-796">CC002</span></span></td>
<td><span data-ttu-id="b22f1-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-797">Finance</span></span></td>
<td><span data-ttu-id="b22f1-798">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-798">10001</span></span></td>
<td><span data-ttu-id="b22f1-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-799">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-800">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-801">436.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-801">436.00</span></span></td>
<td><span data-ttu-id="b22f1-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-803">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-803">CC003</span></span></td>
<td><span data-ttu-id="b22f1-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-804">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-805">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-805">10001</span></span></td>
<td><span data-ttu-id="b22f1-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-806">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-807">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-808">685.14</span><span class="sxs-lookup"><span data-stu-id="b22f1-808">685.14</span></span></td>
<td><span data-ttu-id="b22f1-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-810">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-810">CC004</span></span></td>
<td><span data-ttu-id="b22f1-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-811">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-812">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-812">10001</span></span></td>
<td><span data-ttu-id="b22f1-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-813">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-814">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-815">124.57</span><span class="sxs-lookup"><span data-stu-id="b22f1-815">124.57</span></span></td>
<td><span data-ttu-id="b22f1-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-817">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-817">CC002</span></span></td>
<td><span data-ttu-id="b22f1-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-818">Finance</span></span></td>
<td><span data-ttu-id="b22f1-819">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-819">10001</span></span></td>
<td><span data-ttu-id="b22f1-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-820">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-821">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="b22f1-822">-675.00</span></span></td>
<td><span data-ttu-id="b22f1-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-824">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-824">CC003</span></span></td>
<td><span data-ttu-id="b22f1-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-825">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-826">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-826">10001</span></span></td>
<td><span data-ttu-id="b22f1-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-827">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-828">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-829">438.75</span><span class="sxs-lookup"><span data-stu-id="b22f1-829">438.75</span></span></td>
<td><span data-ttu-id="b22f1-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-831">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-831">CC004</span></span></td>
<td><span data-ttu-id="b22f1-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-832">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-833">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-833">10001</span></span></td>
<td><span data-ttu-id="b22f1-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-834">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-835">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-836">236.25</span><span class="sxs-lookup"><span data-stu-id="b22f1-836">236.25</span></span></td>
<td><span data-ttu-id="b22f1-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-838">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-838">CC002</span></span></td>
<td><span data-ttu-id="b22f1-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="b22f1-839">Finance</span></span></td>
<td><span data-ttu-id="b22f1-840">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-840">10001</span></span></td>
<td><span data-ttu-id="b22f1-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-841">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-842">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="b22f1-843">-8,150.29</span></span></td>
<td><span data-ttu-id="b22f1-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-845">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-845">CC003</span></span></td>
<td><span data-ttu-id="b22f1-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-846">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-847">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-847">10001</span></span></td>
<td><span data-ttu-id="b22f1-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-848">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-849">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b22f1-850">5,297.69</span></span></td>
<td><span data-ttu-id="b22f1-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-852">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-852">CC004</span></span></td>
<td><span data-ttu-id="b22f1-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="b22f1-853">Packaging</span></span></td>
<td><span data-ttu-id="b22f1-854">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-854">10001</span></span></td>
<td><span data-ttu-id="b22f1-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-855">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-856">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b22f1-857">2,852.60</span></span></td>
<td><span data-ttu-id="b22f1-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-859">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-859">CC003</span></span></td>
<td><span data-ttu-id="b22f1-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-860">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-861">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-861">10001</span></span></td>
<td><span data-ttu-id="b22f1-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-862">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-863">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="b22f1-864">-713.75</span></span></td>
<td><span data-ttu-id="b22f1-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-866">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-867">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-868">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-868">10001</span></span></td>
<td><span data-ttu-id="b22f1-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-869">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-870">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-871">535.31</span><span class="sxs-lookup"><span data-stu-id="b22f1-871">535.31</span></span></td>
<td><span data-ttu-id="b22f1-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-873">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-874">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-875">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-875">10001</span></span></td>
<td><span data-ttu-id="b22f1-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-876">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-877">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-878">178.44</span><span class="sxs-lookup"><span data-stu-id="b22f1-878">178.44</span></span></td>
<td><span data-ttu-id="b22f1-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-880">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-880">CC003</span></span></td>
<td><span data-ttu-id="b22f1-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-881">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-882">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-882">10001</span></span></td>
<td><span data-ttu-id="b22f1-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-883">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-884">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="b22f1-885">-5,982.83</span></span></td>
<td><span data-ttu-id="b22f1-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-887">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-888">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-889">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-889">10001</span></span></td>
<td><span data-ttu-id="b22f1-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-890">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-891">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b22f1-892">4,487.12</span></span></td>
<td><span data-ttu-id="b22f1-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-894">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-895">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-896">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-896">10001</span></span></td>
<td><span data-ttu-id="b22f1-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-897">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-898">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b22f1-899">1,495.71</span></span></td>
<td><span data-ttu-id="b22f1-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-901">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-901">CC003</span></span></td>
<td><span data-ttu-id="b22f1-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-902">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-903">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-903">10001</span></span></td>
<td><span data-ttu-id="b22f1-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-904">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-905">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="b22f1-906">-286.25</span></span></td>
<td><span data-ttu-id="b22f1-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-908">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-909">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-910">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-910">10001</span></span></td>
<td><span data-ttu-id="b22f1-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-911">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-912">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-913">241.05</span><span class="sxs-lookup"><span data-stu-id="b22f1-913">241.05</span></span></td>
<td><span data-ttu-id="b22f1-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-915">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-916">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-917">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-917">10001</span></span></td>
<td><span data-ttu-id="b22f1-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-918">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-919">Fixed cost</span></span></td>
<td><span data-ttu-id="b22f1-920">45.20</span><span class="sxs-lookup"><span data-stu-id="b22f1-920">45.20</span></span></td>
<td><span data-ttu-id="b22f1-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-922">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-922">CC003</span></span></td>
<td><span data-ttu-id="b22f1-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="b22f1-923">Assembly</span></span></td>
<td><span data-ttu-id="b22f1-924">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-924">10001</span></span></td>
<td><span data-ttu-id="b22f1-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-925">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-926">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="b22f1-927">-2,977.17</span></span></td>
<td><span data-ttu-id="b22f1-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-929">Prod 1</span></span></td>
<td><span data-ttu-id="b22f1-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-930">Product 1</span></span></td>
<td><span data-ttu-id="b22f1-931">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-931">10001</span></span></td>
<td><span data-ttu-id="b22f1-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-932">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-933">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b22f1-934">2,507.09</span></span></td>
<td><span data-ttu-id="b22f1-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b22f1-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-936">Prod 2</span></span></td>
<td><span data-ttu-id="b22f1-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-937">Product 2</span></span></td>
<td><span data-ttu-id="b22f1-938">10001</span><span class="sxs-lookup"><span data-stu-id="b22f1-938">10001</span></span></td>
<td><span data-ttu-id="b22f1-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-939">Electricity</span></span></td>
<td><span data-ttu-id="b22f1-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-940">Variable cost</span></span></td>
<td><span data-ttu-id="b22f1-941">470.08</span><span class="sxs-lookup"><span data-stu-id="b22f1-941">470.08</span></span></td>
<td><span data-ttu-id="b22f1-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="b22f1-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="b22f1-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="b22f1-943">Conclusion</span></span>
<span data-ttu-id="b22f1-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="b22f1-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="b22f1-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="b22f1-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="b22f1-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="b22f1-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="b22f1-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="b22f1-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="b22f1-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="b22f1-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="b22f1-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="b22f1-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="b22f1-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b22f1-951">CC099</span><span class="sxs-lookup"><span data-stu-id="b22f1-951">CC099</span></span></th>
<th><span data-ttu-id="b22f1-952">CC001</span><span class="sxs-lookup"><span data-stu-id="b22f1-952">CC001</span></span></th>
<th><span data-ttu-id="b22f1-953">CC002</span><span class="sxs-lookup"><span data-stu-id="b22f1-953">CC002</span></span></th>
<th><span data-ttu-id="b22f1-954">CC003</span><span class="sxs-lookup"><span data-stu-id="b22f1-954">CC003</span></span></th>
<th><span data-ttu-id="b22f1-955">CC004</span><span class="sxs-lookup"><span data-stu-id="b22f1-955">CC004</span></span></th>
<th><span data-ttu-id="b22f1-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-956">Proj 1</span></span></th>
<th><span data-ttu-id="b22f1-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-957">Proj 2</span></span></th>
<th><span data-ttu-id="b22f1-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b22f1-958">Prod 1</span></span></th>
<th><span data-ttu-id="b22f1-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b22f1-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="b22f1-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="b22f1-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="b22f1-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="b22f1-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-971">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="b22f1-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-973">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-974">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-975">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-976">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-977">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-978">776.36</span><span class="sxs-lookup"><span data-stu-id="b22f1-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-979">223.64</span><span class="sxs-lookup"><span data-stu-id="b22f1-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="b22f1-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="b22f1-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-982">000</span><span class="sxs-lookup"><span data-stu-id="b22f1-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-983">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-984">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-985">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-986">0,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-987">30,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-988">10,00</span><span class="sxs-lookup"><span data-stu-id="b22f1-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b22f1-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b22f1-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b22f1-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b22f1-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b22f1-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="b22f1-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="b22f1-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="b22f1-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="b22f1-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="b22f1-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="b22f1-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="b22f1-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="b22f1-996">Zie [Beleid voor totalisering van kosten en overheadberekening](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b22f1-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



