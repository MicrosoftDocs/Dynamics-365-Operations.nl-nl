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
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208842"
---
# <a name="overhead-calculation"></a><span data-ttu-id="a5aac-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="a5aac-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5aac-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="a5aac-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="a5aac-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="a5aac-105">Term definition</span></span>
---------------

<span data-ttu-id="a5aac-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="a5aac-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="a5aac-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="a5aac-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="a5aac-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="a5aac-109">Huur</span><span class="sxs-lookup"><span data-stu-id="a5aac-109">Rent</span></span>
-   <span data-ttu-id="a5aac-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-110">Electricity</span></span>
-   <span data-ttu-id="a5aac-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="a5aac-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="a5aac-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="a5aac-112">Overhead calculation overview</span></span>
<span data-ttu-id="a5aac-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a5aac-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="a5aac-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="a5aac-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="a5aac-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="a5aac-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="a5aac-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="a5aac-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="a5aac-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="a5aac-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="a5aac-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="a5aac-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="a5aac-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="a5aac-119">Version type</span></span>
-   <span data-ttu-id="a5aac-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="a5aac-120">Date and time</span></span>
-   <span data-ttu-id="a5aac-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="a5aac-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="a5aac-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="a5aac-122">Fiscal year</span></span>
-   <span data-ttu-id="a5aac-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="a5aac-123">Fiscal period</span></span>

<span data-ttu-id="a5aac-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a5aac-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="a5aac-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="a5aac-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="a5aac-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a5aac-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="a5aac-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="a5aac-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="a5aac-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="a5aac-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="a5aac-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="a5aac-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="a5aac-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="a5aac-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="a5aac-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="a5aac-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="a5aac-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="a5aac-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="a5aac-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="a5aac-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="a5aac-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="a5aac-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="a5aac-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="a5aac-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="a5aac-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="a5aac-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="a5aac-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="a5aac-140">Main account</span></span></th>
<th><span data-ttu-id="a5aac-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="a5aac-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="a5aac-143">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-143">CC099</span></span></td>
<td><span data-ttu-id="a5aac-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-144">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-145">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-145">10001</span></span></td>
<td><span data-ttu-id="a5aac-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-146">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="a5aac-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="a5aac-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="a5aac-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="a5aac-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="a5aac-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="a5aac-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="a5aac-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="a5aac-151">Define the cost behavior rule</span></span>

<span data-ttu-id="a5aac-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="a5aac-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="a5aac-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="a5aac-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="a5aac-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="a5aac-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="a5aac-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="a5aac-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="a5aac-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="a5aac-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="a5aac-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="a5aac-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="a5aac-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="a5aac-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-160">Journal</span></span></th>
<th><span data-ttu-id="a5aac-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a5aac-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="a5aac-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a5aac-163">Versie</span><span class="sxs-lookup"><span data-stu-id="a5aac-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-164">00001</span><span class="sxs-lookup"><span data-stu-id="a5aac-164">00001</span></span></td>
<td><span data-ttu-id="a5aac-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="a5aac-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-166">Fiscal</span></span></td>
<td><span data-ttu-id="a5aac-167">2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-167">2017</span></span></td>
<td><span data-ttu-id="a5aac-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-168">Period 1</span></span></td>
<td><span data-ttu-id="a5aac-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a5aac-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="a5aac-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-173">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-174">Cost behavior</span></span></th>
<th><span data-ttu-id="a5aac-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="a5aac-177">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-177">CC099</span></span></td>
<td><span data-ttu-id="a5aac-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-178">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-179">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-179">10001</span></span></td>
<td><span data-ttu-id="a5aac-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-180">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="a5aac-181">Unclassified</span></span></td>
<td><span data-ttu-id="a5aac-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a5aac-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="a5aac-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-185">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-186">Cost behavior</span></span></th>
<th><span data-ttu-id="a5aac-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-187">Amount</span></span></th>
<th><span data-ttu-id="a5aac-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-189">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-189">CC099</span></span></td>
<td><span data-ttu-id="a5aac-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-190">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-191">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-191">10001</span></span></td>
<td><span data-ttu-id="a5aac-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-192">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="a5aac-193">Unclassified</span></span></td>
<td><span data-ttu-id="a5aac-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-194">10,000.00</span></span></td>
<td><span data-ttu-id="a5aac-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-196">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-196">CC099</span></span></td>
<td><span data-ttu-id="a5aac-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-197">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-198">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-198">10001</span></span></td>
<td><span data-ttu-id="a5aac-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-199">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="a5aac-200">Unclassified</span></span></td>
<td><span data-ttu-id="a5aac-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-201">-10,000.00</span></span></td>
<td><span data-ttu-id="a5aac-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-203">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-203">CC099</span></span></td>
<td><span data-ttu-id="a5aac-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-204">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-205">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-205">10001</span></span></td>
<td><span data-ttu-id="a5aac-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-206">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-207">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-208">1,000.00</span></span></td>
<td><span data-ttu-id="a5aac-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-210">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-210">CC099</span></span></td>
<td><span data-ttu-id="a5aac-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-211">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-212">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-212">10001</span></span></td>
<td><span data-ttu-id="a5aac-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-213">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-214">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-215">9,000.00</span></span></td>
<td><span data-ttu-id="a5aac-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a5aac-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="a5aac-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="a5aac-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="a5aac-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="a5aac-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="a5aac-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="a5aac-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="a5aac-221">Define the cost distribution rule</span></span>

<span data-ttu-id="a5aac-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="a5aac-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="a5aac-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="a5aac-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="a5aac-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="a5aac-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="a5aac-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="a5aac-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="a5aac-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="a5aac-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="a5aac-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-228">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="a5aac-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-230">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-230">CC001</span></span></td>
<td><span data-ttu-id="a5aac-231">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-231">HR</span></span></td>
<td><span data-ttu-id="a5aac-232">1.000</span><span class="sxs-lookup"><span data-stu-id="a5aac-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-233">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-233">CC002</span></span></td>
<td><span data-ttu-id="a5aac-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-234">Finance</span></span></td>
<td><span data-ttu-id="a5aac-235">6.000</span><span class="sxs-lookup"><span data-stu-id="a5aac-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-236">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-236">CC003</span></span></td>
<td><span data-ttu-id="a5aac-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-237">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-238">0</span><span class="sxs-lookup"><span data-stu-id="a5aac-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-240">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a5aac-241">Magnitude</span></span></th>
<th><span data-ttu-id="a5aac-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a5aac-242">Allocation factor</span></span></th>
<th><span data-ttu-id="a5aac-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-244">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-244">CC001</span></span></td>
<td><span data-ttu-id="a5aac-245">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-245">HR</span></span></td>
<td><span data-ttu-id="a5aac-246">1.000</span><span class="sxs-lookup"><span data-stu-id="a5aac-246">1,000</span></span></td>
<td><span data-ttu-id="a5aac-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a5aac-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a5aac-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-249">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-249">CC002</span></span></td>
<td><span data-ttu-id="a5aac-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-250">Finance</span></span></td>
<td><span data-ttu-id="a5aac-251">6.000</span><span class="sxs-lookup"><span data-stu-id="a5aac-251">6,000</span></span></td>
<td><span data-ttu-id="a5aac-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a5aac-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a5aac-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-254">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-254">CC003</span></span></td>
<td><span data-ttu-id="a5aac-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-255">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-256">0</span><span class="sxs-lookup"><span data-stu-id="a5aac-256">0</span></span></td>
<td><span data-ttu-id="a5aac-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a5aac-258">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="a5aac-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="a5aac-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-261">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-262">Formule</span><span class="sxs-lookup"><span data-stu-id="a5aac-262">Formula</span></span></th>
<th><span data-ttu-id="a5aac-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a5aac-263">Magnitude</span></span></th>
<th><span data-ttu-id="a5aac-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a5aac-264">Allocation factor</span></span></th>
<th><span data-ttu-id="a5aac-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-266">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-266">CC001</span></span></td>
<td><span data-ttu-id="a5aac-267">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-267">HR</span></span></td>
<td><span data-ttu-id="a5aac-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a5aac-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a5aac-269">1</span><span class="sxs-lookup"><span data-stu-id="a5aac-269">1</span></span></td>
<td><span data-ttu-id="a5aac-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a5aac-271">500,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-272">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-272">CC002</span></span></td>
<td><span data-ttu-id="a5aac-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-273">Finance</span></span></td>
<td><span data-ttu-id="a5aac-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a5aac-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a5aac-275">1</span><span class="sxs-lookup"><span data-stu-id="a5aac-275">1</span></span></td>
<td><span data-ttu-id="a5aac-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a5aac-277">500,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-278">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-278">CC003</span></span></td>
<td><span data-ttu-id="a5aac-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-279">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a5aac-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a5aac-281">0</span><span class="sxs-lookup"><span data-stu-id="a5aac-281">0</span></span></td>
<td><span data-ttu-id="a5aac-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a5aac-283">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a5aac-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-285">Journal</span></span></th>
<th><span data-ttu-id="a5aac-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a5aac-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="a5aac-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a5aac-288">Versie</span><span class="sxs-lookup"><span data-stu-id="a5aac-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-289">00002</span><span class="sxs-lookup"><span data-stu-id="a5aac-289">00002</span></span></td>
<td><span data-ttu-id="a5aac-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="a5aac-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="a5aac-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-291">Fiscal</span></span></td>
<td><span data-ttu-id="a5aac-292">2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-292">2017</span></span></td>
<td><span data-ttu-id="a5aac-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-293">Period 1</span></span></td>
<td><span data-ttu-id="a5aac-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a5aac-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="a5aac-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-298">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-299">Cost behavior</span></span></th>
<th><span data-ttu-id="a5aac-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-302">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-302">CC099</span></span></td>
<td><span data-ttu-id="a5aac-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-303">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-304">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-304">10001</span></span></td>
<td><span data-ttu-id="a5aac-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-305">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-306">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-309">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-309">CC099</span></span></td>
<td><span data-ttu-id="a5aac-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-310">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-311">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-311">10001</span></span></td>
<td><span data-ttu-id="a5aac-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-312">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-313">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a5aac-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="a5aac-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-317">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-318">Cost behavior</span></span></th>
<th><span data-ttu-id="a5aac-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-319">Amount</span></span></th>
<th><span data-ttu-id="a5aac-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-321">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-321">CC099</span></span></td>
<td><span data-ttu-id="a5aac-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-322">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-323">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-323">10001</span></span></td>
<td><span data-ttu-id="a5aac-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-324">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-325">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-326">-1,000.00</span></span></td>
<td><span data-ttu-id="a5aac-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-328">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-328">CC001</span></span></td>
<td><span data-ttu-id="a5aac-329">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-329">HR</span></span></td>
<td><span data-ttu-id="a5aac-330">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-330">10001</span></span></td>
<td><span data-ttu-id="a5aac-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-331">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-332">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-333">500,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-333">500.00</span></span></td>
<td><span data-ttu-id="a5aac-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-335">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-335">CC002</span></span></td>
<td><span data-ttu-id="a5aac-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-336">Finance</span></span></td>
<td><span data-ttu-id="a5aac-337">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-337">10001</span></span></td>
<td><span data-ttu-id="a5aac-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-338">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-339">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-340">500,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-340">500.00</span></span></td>
<td><span data-ttu-id="a5aac-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-342">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-342">CC099</span></span></td>
<td><span data-ttu-id="a5aac-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a5aac-343">Default cost center</span></span></td>
<td><span data-ttu-id="a5aac-344">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-344">10001</span></span></td>
<td><span data-ttu-id="a5aac-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-345">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-346">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-347">-9,000.00</span></span></td>
<td><span data-ttu-id="a5aac-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-349">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-349">CC001</span></span></td>
<td><span data-ttu-id="a5aac-350">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-350">HR</span></span></td>
<td><span data-ttu-id="a5aac-351">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-351">10001</span></span></td>
<td><span data-ttu-id="a5aac-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-352">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-353">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a5aac-354">1,285.71</span></span></td>
<td><span data-ttu-id="a5aac-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-356">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-356">CC002</span></span></td>
<td><span data-ttu-id="a5aac-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-357">Finance</span></span></td>
<td><span data-ttu-id="a5aac-358">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-358">10001</span></span></td>
<td><span data-ttu-id="a5aac-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-359">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-360">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a5aac-361">7,714.29</span></span></td>
<td><span data-ttu-id="a5aac-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a5aac-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="a5aac-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="a5aac-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="a5aac-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="a5aac-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="a5aac-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="a5aac-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="a5aac-367">Define the overhead rate</span></span>

<span data-ttu-id="a5aac-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="a5aac-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-370">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-371">Uren</span><span class="sxs-lookup"><span data-stu-id="a5aac-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-372">Proj 1</span></span></td>
<td><span data-ttu-id="a5aac-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-373">Project 1</span></span></td>
<td><span data-ttu-id="a5aac-374">3</span><span class="sxs-lookup"><span data-stu-id="a5aac-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-375">Proj 2</span></span></td>
<td><span data-ttu-id="a5aac-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-376">Project 2</span></span></td>
<td><span data-ttu-id="a5aac-377">1</span><span class="sxs-lookup"><span data-stu-id="a5aac-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="a5aac-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-379">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-380">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-381">Cost behavior</span></span></th>
<th><span data-ttu-id="a5aac-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="a5aac-382">Units</span></span></th>
<th><span data-ttu-id="a5aac-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="a5aac-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-384">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-384">CC001</span></span></td>
<td><span data-ttu-id="a5aac-385">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-385">HR</span></span></td>
<td><span data-ttu-id="a5aac-386">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-386">10001</span></span></td>
<td><span data-ttu-id="a5aac-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-387">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-388">1</span><span class="sxs-lookup"><span data-stu-id="a5aac-388">1</span></span></td>
<td><span data-ttu-id="a5aac-389">10</span><span class="sxs-lookup"><span data-stu-id="a5aac-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="a5aac-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-391">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a5aac-392">Magnitude</span></span></th>
<th><span data-ttu-id="a5aac-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-393">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a5aac-394">Allocation factor</span></span></th>
<th><span data-ttu-id="a5aac-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-396">Proj 1</span></span></td>
<td><span data-ttu-id="a5aac-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-397">Project 1</span></span></td>
<td><span data-ttu-id="a5aac-398">3</span><span class="sxs-lookup"><span data-stu-id="a5aac-398">3</span></span></td>
<td><span data-ttu-id="a5aac-399">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-399">10001</span></span></td>
<td><span data-ttu-id="a5aac-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a5aac-401">30,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-402">Proj 2</span></span></td>
<td><span data-ttu-id="a5aac-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-403">Project 2</span></span></td>
<td><span data-ttu-id="a5aac-404">1</span><span class="sxs-lookup"><span data-stu-id="a5aac-404">1</span></span></td>
<td><span data-ttu-id="a5aac-405">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-405">10001</span></span></td>
<td><span data-ttu-id="a5aac-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a5aac-407">10,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a5aac-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-409">Journal</span></span></th>
<th><span data-ttu-id="a5aac-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a5aac-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="a5aac-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a5aac-412">Versie</span><span class="sxs-lookup"><span data-stu-id="a5aac-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-413">00003</span><span class="sxs-lookup"><span data-stu-id="a5aac-413">00003</span></span></td>
<td><span data-ttu-id="a5aac-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="a5aac-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="a5aac-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-415">Fiscal</span></span></td>
<td><span data-ttu-id="a5aac-416">2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-416">2017</span></span></td>
<td><span data-ttu-id="a5aac-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-417">Period 1</span></span></td>
<td><span data-ttu-id="a5aac-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="a5aac-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="a5aac-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-421">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a5aac-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-424">Proj 1</span></span></td>
<td><span data-ttu-id="a5aac-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a5aac-426">3,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-428">Proj 2</span></span></td>
<td><span data-ttu-id="a5aac-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a5aac-430">1,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a5aac-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="a5aac-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-433">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-434">Cost behavior</span></span></th>
<th><span data-ttu-id="a5aac-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-435">Amount</span></span></th>
<th><span data-ttu-id="a5aac-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="a5aac-437">CC0001</span></span></td>
<td><span data-ttu-id="a5aac-438">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-438">HR</span></span></td>
<td><span data-ttu-id="a5aac-439">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-439">10001</span></span></td>
<td><span data-ttu-id="a5aac-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-440">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-441">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-442">-30.00</span></span></td>
<td><span data-ttu-id="a5aac-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-444">Proj 1</span></span></td>
<td><span data-ttu-id="a5aac-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a5aac-446">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-446">10001</span></span></td>
<td><span data-ttu-id="a5aac-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-447">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-448">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-449">30,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-449">30.00</span></span></td>
<td><span data-ttu-id="a5aac-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-451">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-451">CC001</span></span></td>
<td><span data-ttu-id="a5aac-452">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-452">HR</span></span></td>
<td><span data-ttu-id="a5aac-453">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-453">10001</span></span></td>
<td><span data-ttu-id="a5aac-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-454">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-455">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-456">-10.00</span></span></td>
<td><span data-ttu-id="a5aac-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-458">Proj 2</span></span></td>
<td><span data-ttu-id="a5aac-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a5aac-460">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-460">10001</span></span></td>
<td><span data-ttu-id="a5aac-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-461">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-462">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-463">10.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-463">10.00</span></span></td>
<td><span data-ttu-id="a5aac-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="a5aac-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="a5aac-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="a5aac-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="a5aac-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="a5aac-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="a5aac-468">Finance ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="a5aac-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="a5aac-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="a5aac-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="a5aac-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="a5aac-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="a5aac-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="a5aac-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="a5aac-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="a5aac-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="a5aac-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="a5aac-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="a5aac-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="a5aac-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="a5aac-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="a5aac-475">Define the cost allocation</span></span>

<span data-ttu-id="a5aac-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="a5aac-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="a5aac-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="a5aac-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-479">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="a5aac-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-481">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-481">CC002</span></span></td>
<td><span data-ttu-id="a5aac-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-482">Finance</span></span></td>
<td><span data-ttu-id="a5aac-483">35</span><span class="sxs-lookup"><span data-stu-id="a5aac-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-484">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-484">CC003</span></span></td>
<td><span data-ttu-id="a5aac-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-485">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-486">55</span><span class="sxs-lookup"><span data-stu-id="a5aac-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-487">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-487">CC004</span></span></td>
<td><span data-ttu-id="a5aac-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-488">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-489">10</span><span class="sxs-lookup"><span data-stu-id="a5aac-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="a5aac-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-492">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="a5aac-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-494">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-494">CC003</span></span></td>
<td><span data-ttu-id="a5aac-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-495">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-496">65</span><span class="sxs-lookup"><span data-stu-id="a5aac-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-497">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-497">CC004</span></span></td>
<td><span data-ttu-id="a5aac-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-498">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-499">35</span><span class="sxs-lookup"><span data-stu-id="a5aac-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="a5aac-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-502">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="a5aac-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-504">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-505">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-506">60</span><span class="sxs-lookup"><span data-stu-id="a5aac-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-507">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-508">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-509">20</span><span class="sxs-lookup"><span data-stu-id="a5aac-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="a5aac-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-512">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="a5aac-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-514">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-515">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-516">80</span><span class="sxs-lookup"><span data-stu-id="a5aac-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-517">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-518">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-519">15</span><span class="sxs-lookup"><span data-stu-id="a5aac-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a5aac-520">Statistische metingen, zoals de productie-uren die een product verbruikt, kunnen worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="a5aac-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="a5aac-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a5aac-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="a5aac-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="a5aac-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-523">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a5aac-524">Magnitude</span></span></th>
<th><span data-ttu-id="a5aac-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a5aac-525">Allocation factor</span></span></th>
<th><span data-ttu-id="a5aac-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-526">Amount</span></span></th>
<th><span data-ttu-id="a5aac-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-528">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-528">CC002</span></span></td>
<td><span data-ttu-id="a5aac-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-529">Finance</span></span></td>
<td><span data-ttu-id="a5aac-530">35</span><span class="sxs-lookup"><span data-stu-id="a5aac-530">35</span></span></td>
<td><span data-ttu-id="a5aac-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a5aac-532">175.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-532">175.00</span></span></td>
<td><span data-ttu-id="a5aac-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-534">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-534">CC003</span></span></td>
<td><span data-ttu-id="a5aac-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-535">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-536">55</span><span class="sxs-lookup"><span data-stu-id="a5aac-536">55</span></span></td>
<td><span data-ttu-id="a5aac-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a5aac-538">275.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-538">275.00</span></span></td>
<td><span data-ttu-id="a5aac-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-540">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-540">CC004</span></span></td>
<td><span data-ttu-id="a5aac-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-541">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-542">10</span><span class="sxs-lookup"><span data-stu-id="a5aac-542">10</span></span></td>
<td><span data-ttu-id="a5aac-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a5aac-544">50,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-544">50.00</span></span></td>
<td><span data-ttu-id="a5aac-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-546">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-546">CC002</span></span></td>
<td><span data-ttu-id="a5aac-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-547">Finance</span></span></td>
<td><span data-ttu-id="a5aac-548">35</span><span class="sxs-lookup"><span data-stu-id="a5aac-548">35</span></span></td>
<td><span data-ttu-id="a5aac-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a5aac-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a5aac-550">436.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-550">436.00</span></span></td>
<td><span data-ttu-id="a5aac-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-552">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-552">CC003</span></span></td>
<td><span data-ttu-id="a5aac-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-553">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-554">55</span><span class="sxs-lookup"><span data-stu-id="a5aac-554">55</span></span></td>
<td><span data-ttu-id="a5aac-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a5aac-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a5aac-556">685.14</span><span class="sxs-lookup"><span data-stu-id="a5aac-556">685.14</span></span></td>
<td><span data-ttu-id="a5aac-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-558">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-558">CC004</span></span></td>
<td><span data-ttu-id="a5aac-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-559">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-560">10</span><span class="sxs-lookup"><span data-stu-id="a5aac-560">10</span></span></td>
<td><span data-ttu-id="a5aac-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a5aac-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a5aac-562">124.57</span><span class="sxs-lookup"><span data-stu-id="a5aac-562">124.57</span></span></td>
<td><span data-ttu-id="a5aac-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="a5aac-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-565">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a5aac-566">Magnitude</span></span></th>
<th><span data-ttu-id="a5aac-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a5aac-567">Allocation factor</span></span></th>
<th><span data-ttu-id="a5aac-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-568">Amount</span></span></th>
<th><span data-ttu-id="a5aac-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-570">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-570">CC003</span></span></td>
<td><span data-ttu-id="a5aac-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-571">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-572">65</span><span class="sxs-lookup"><span data-stu-id="a5aac-572">65</span></span></td>
<td><span data-ttu-id="a5aac-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a5aac-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a5aac-574">438.75</span><span class="sxs-lookup"><span data-stu-id="a5aac-574">438.75</span></span></td>
<td><span data-ttu-id="a5aac-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-576">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-576">CC004</span></span></td>
<td><span data-ttu-id="a5aac-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-577">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-578">35</span><span class="sxs-lookup"><span data-stu-id="a5aac-578">35</span></span></td>
<td><span data-ttu-id="a5aac-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a5aac-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a5aac-580">236.25</span><span class="sxs-lookup"><span data-stu-id="a5aac-580">236.25</span></span></td>
<td><span data-ttu-id="a5aac-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-582">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-582">CC003</span></span></td>
<td><span data-ttu-id="a5aac-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-583">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-584">65</span><span class="sxs-lookup"><span data-stu-id="a5aac-584">65</span></span></td>
<td><span data-ttu-id="a5aac-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a5aac-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a5aac-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a5aac-586">5,297.69</span></span></td>
<td><span data-ttu-id="a5aac-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-588">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-588">CC004</span></span></td>
<td><span data-ttu-id="a5aac-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-589">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-590">35</span><span class="sxs-lookup"><span data-stu-id="a5aac-590">35</span></span></td>
<td><span data-ttu-id="a5aac-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a5aac-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a5aac-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a5aac-592">2,852.60</span></span></td>
<td><span data-ttu-id="a5aac-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="a5aac-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-595">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a5aac-596">Magnitude</span></span></th>
<th><span data-ttu-id="a5aac-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a5aac-597">Allocation factor</span></span></th>
<th><span data-ttu-id="a5aac-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-598">Amount</span></span></th>
<th><span data-ttu-id="a5aac-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-600">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-601">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-602">60</span><span class="sxs-lookup"><span data-stu-id="a5aac-602">60</span></span></td>
<td><span data-ttu-id="a5aac-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a5aac-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a5aac-604">535.31</span><span class="sxs-lookup"><span data-stu-id="a5aac-604">535.31</span></span></td>
<td><span data-ttu-id="a5aac-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-606">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-607">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-608">20</span><span class="sxs-lookup"><span data-stu-id="a5aac-608">20</span></span></td>
<td><span data-ttu-id="a5aac-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a5aac-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a5aac-610">178.44</span><span class="sxs-lookup"><span data-stu-id="a5aac-610">178.44</span></span></td>
<td><span data-ttu-id="a5aac-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-612">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-613">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-614">60</span><span class="sxs-lookup"><span data-stu-id="a5aac-614">60</span></span></td>
<td><span data-ttu-id="a5aac-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a5aac-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a5aac-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a5aac-616">4,487.12</span></span></td>
<td><span data-ttu-id="a5aac-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-618">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-619">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-620">20</span><span class="sxs-lookup"><span data-stu-id="a5aac-620">20</span></span></td>
<td><span data-ttu-id="a5aac-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a5aac-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a5aac-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a5aac-622">1,495.71</span></span></td>
<td><span data-ttu-id="a5aac-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a5aac-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="a5aac-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-625">Cost object</span></span></th>
<th><span data-ttu-id="a5aac-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a5aac-626">Magnitude</span></span></th>
<th><span data-ttu-id="a5aac-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a5aac-627">Allocation factor</span></span></th>
<th><span data-ttu-id="a5aac-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-628">Amount</span></span></th>
<th><span data-ttu-id="a5aac-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-630">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-631">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-632">80</span><span class="sxs-lookup"><span data-stu-id="a5aac-632">80</span></span></td>
<td><span data-ttu-id="a5aac-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a5aac-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a5aac-634">241.05</span><span class="sxs-lookup"><span data-stu-id="a5aac-634">241.05</span></span></td>
<td><span data-ttu-id="a5aac-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-636">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-637">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-638">15</span><span class="sxs-lookup"><span data-stu-id="a5aac-638">15</span></span></td>
<td><span data-ttu-id="a5aac-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a5aac-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a5aac-640">45.20</span><span class="sxs-lookup"><span data-stu-id="a5aac-640">45.20</span></span></td>
<td><span data-ttu-id="a5aac-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-642">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-643">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-644">80</span><span class="sxs-lookup"><span data-stu-id="a5aac-644">80</span></span></td>
<td><span data-ttu-id="a5aac-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a5aac-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a5aac-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a5aac-646">2,507.09</span></span></td>
<td><span data-ttu-id="a5aac-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-648">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-649">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-650">15</span><span class="sxs-lookup"><span data-stu-id="a5aac-650">15</span></span></td>
<td><span data-ttu-id="a5aac-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a5aac-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a5aac-652">470.08</span><span class="sxs-lookup"><span data-stu-id="a5aac-652">470.08</span></span></td>
<td><span data-ttu-id="a5aac-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a5aac-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="a5aac-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-655">Journal</span></span></th>
<th><span data-ttu-id="a5aac-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a5aac-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="a5aac-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a5aac-658">Versie</span><span class="sxs-lookup"><span data-stu-id="a5aac-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-659">00004</span><span class="sxs-lookup"><span data-stu-id="a5aac-659">00004</span></span></td>
<td><span data-ttu-id="a5aac-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="a5aac-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-661">Fiscal</span></span></td>
<td><span data-ttu-id="a5aac-662">2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-662">2017</span></span></td>
<td><span data-ttu-id="a5aac-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-663">Period 1</span></span></td>
<td><span data-ttu-id="a5aac-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="a5aac-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="a5aac-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a5aac-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-668">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-669">Cost behavior</span></span></th>
<th><span data-ttu-id="a5aac-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-672">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-672">CC001</span></span></td>
<td><span data-ttu-id="a5aac-673">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-673">HR</span></span></td>
<td><span data-ttu-id="a5aac-674">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-674">10001</span></span></td>
<td><span data-ttu-id="a5aac-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-675">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-676">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-677">500,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-679">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-679">CC001</span></span></td>
<td><span data-ttu-id="a5aac-680">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-680">HR</span></span></td>
<td><span data-ttu-id="a5aac-681">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-681">10001</span></span></td>
<td><span data-ttu-id="a5aac-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-682">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-683">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="a5aac-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-686">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-686">CC002</span></span></td>
<td><span data-ttu-id="a5aac-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-687">Finance</span></span></td>
<td><span data-ttu-id="a5aac-688">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-688">10001</span></span></td>
<td><span data-ttu-id="a5aac-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-689">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-690">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-691">675.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-693">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-693">CC002</span></span></td>
<td><span data-ttu-id="a5aac-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-694">Finance</span></span></td>
<td><span data-ttu-id="a5aac-695">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-695">10001</span></span></td>
<td><span data-ttu-id="a5aac-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-696">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-697">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="a5aac-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-700">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-700">CC003</span></span></td>
<td><span data-ttu-id="a5aac-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-701">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-702">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-702">10001</span></span></td>
<td><span data-ttu-id="a5aac-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-703">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-704">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-705">713.75</span><span class="sxs-lookup"><span data-stu-id="a5aac-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-707">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-707">CC003</span></span></td>
<td><span data-ttu-id="a5aac-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-708">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-709">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-709">10001</span></span></td>
<td><span data-ttu-id="a5aac-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-710">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-711">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="a5aac-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-714">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-714">CC003</span></span></td>
<td><span data-ttu-id="a5aac-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-715">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-716">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-716">10001</span></span></td>
<td><span data-ttu-id="a5aac-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-717">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-718">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-719">286.25</span><span class="sxs-lookup"><span data-stu-id="a5aac-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-721">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-721">CC003</span></span></td>
<td><span data-ttu-id="a5aac-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-722">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-723">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-723">10001</span></span></td>
<td><span data-ttu-id="a5aac-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-724">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-725">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="a5aac-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-728">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-729">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-730">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-730">10001</span></span></td>
<td><span data-ttu-id="a5aac-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-731">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-732">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-733">776.36</span><span class="sxs-lookup"><span data-stu-id="a5aac-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-735">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-736">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-737">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-737">10001</span></span></td>
<td><span data-ttu-id="a5aac-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-738">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-739">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a5aac-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-742">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-743">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-744">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-744">10001</span></span></td>
<td><span data-ttu-id="a5aac-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-745">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-746">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-747">223.64</span><span class="sxs-lookup"><span data-stu-id="a5aac-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="a5aac-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-749">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-750">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-751">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-751">10001</span></span></td>
<td><span data-ttu-id="a5aac-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-752">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-753">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a5aac-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a5aac-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="a5aac-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a5aac-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a5aac-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-757">Cost element</span></span></th>
<th><span data-ttu-id="a5aac-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-758">Cost behavior</span></span></th>
<th><span data-ttu-id="a5aac-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a5aac-759">Amount</span></span></th>
<th><span data-ttu-id="a5aac-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a5aac-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a5aac-761">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-761">CC001</span></span></td>
<td><span data-ttu-id="a5aac-762">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-762">HR</span></span></td>
<td><span data-ttu-id="a5aac-763">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-763">10001</span></span></td>
<td><span data-ttu-id="a5aac-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-764">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-765">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-766">-500.00</span></span></td>
<td><span data-ttu-id="a5aac-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-768">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-768">CC002</span></span></td>
<td><span data-ttu-id="a5aac-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-769">Finance</span></span></td>
<td><span data-ttu-id="a5aac-770">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-770">10001</span></span></td>
<td><span data-ttu-id="a5aac-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-771">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-772">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-773">175.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-773">175.00</span></span></td>
<td><span data-ttu-id="a5aac-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-775">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-775">CC003</span></span></td>
<td><span data-ttu-id="a5aac-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-776">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-777">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-777">10001</span></span></td>
<td><span data-ttu-id="a5aac-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-778">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-779">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-780">275.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-780">275.00</span></span></td>
<td><span data-ttu-id="a5aac-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-782">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-782">CC004</span></span></td>
<td><span data-ttu-id="a5aac-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-783">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-784">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-784">10001</span></span></td>
<td><span data-ttu-id="a5aac-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-785">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-786">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-787">50,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-787">50,00</span></span></td>
<td><span data-ttu-id="a5aac-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-789">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-789">CC001</span></span></td>
<td><span data-ttu-id="a5aac-790">HR</span><span class="sxs-lookup"><span data-stu-id="a5aac-790">HR</span></span></td>
<td><span data-ttu-id="a5aac-791">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-791">10001</span></span></td>
<td><span data-ttu-id="a5aac-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-792">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-793">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="a5aac-794">-1,245.71</span></span></td>
<td><span data-ttu-id="a5aac-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-796">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-796">CC002</span></span></td>
<td><span data-ttu-id="a5aac-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-797">Finance</span></span></td>
<td><span data-ttu-id="a5aac-798">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-798">10001</span></span></td>
<td><span data-ttu-id="a5aac-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-799">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-800">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-801">436.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-801">436.00</span></span></td>
<td><span data-ttu-id="a5aac-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-803">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-803">CC003</span></span></td>
<td><span data-ttu-id="a5aac-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-804">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-805">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-805">10001</span></span></td>
<td><span data-ttu-id="a5aac-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-806">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-807">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-808">685.14</span><span class="sxs-lookup"><span data-stu-id="a5aac-808">685.14</span></span></td>
<td><span data-ttu-id="a5aac-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-810">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-810">CC004</span></span></td>
<td><span data-ttu-id="a5aac-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-811">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-812">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-812">10001</span></span></td>
<td><span data-ttu-id="a5aac-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-813">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-814">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-815">124.57</span><span class="sxs-lookup"><span data-stu-id="a5aac-815">124.57</span></span></td>
<td><span data-ttu-id="a5aac-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-817">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-817">CC002</span></span></td>
<td><span data-ttu-id="a5aac-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-818">Finance</span></span></td>
<td><span data-ttu-id="a5aac-819">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-819">10001</span></span></td>
<td><span data-ttu-id="a5aac-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-820">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-821">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="a5aac-822">-675.00</span></span></td>
<td><span data-ttu-id="a5aac-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-824">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-824">CC003</span></span></td>
<td><span data-ttu-id="a5aac-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-825">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-826">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-826">10001</span></span></td>
<td><span data-ttu-id="a5aac-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-827">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-828">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-829">438.75</span><span class="sxs-lookup"><span data-stu-id="a5aac-829">438.75</span></span></td>
<td><span data-ttu-id="a5aac-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-831">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-831">CC004</span></span></td>
<td><span data-ttu-id="a5aac-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-832">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-833">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-833">10001</span></span></td>
<td><span data-ttu-id="a5aac-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-834">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-835">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-836">236.25</span><span class="sxs-lookup"><span data-stu-id="a5aac-836">236.25</span></span></td>
<td><span data-ttu-id="a5aac-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-838">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-838">CC002</span></span></td>
<td><span data-ttu-id="a5aac-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="a5aac-839">Finance</span></span></td>
<td><span data-ttu-id="a5aac-840">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-840">10001</span></span></td>
<td><span data-ttu-id="a5aac-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-841">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-842">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="a5aac-843">-8,150.29</span></span></td>
<td><span data-ttu-id="a5aac-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-845">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-845">CC003</span></span></td>
<td><span data-ttu-id="a5aac-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-846">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-847">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-847">10001</span></span></td>
<td><span data-ttu-id="a5aac-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-848">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-849">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a5aac-850">5,297.69</span></span></td>
<td><span data-ttu-id="a5aac-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-852">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-852">CC004</span></span></td>
<td><span data-ttu-id="a5aac-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a5aac-853">Packaging</span></span></td>
<td><span data-ttu-id="a5aac-854">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-854">10001</span></span></td>
<td><span data-ttu-id="a5aac-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-855">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-856">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a5aac-857">2,852.60</span></span></td>
<td><span data-ttu-id="a5aac-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-859">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-859">CC003</span></span></td>
<td><span data-ttu-id="a5aac-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-860">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-861">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-861">10001</span></span></td>
<td><span data-ttu-id="a5aac-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-862">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-863">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="a5aac-864">-713.75</span></span></td>
<td><span data-ttu-id="a5aac-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-866">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-867">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-868">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-868">10001</span></span></td>
<td><span data-ttu-id="a5aac-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-869">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-870">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-871">535.31</span><span class="sxs-lookup"><span data-stu-id="a5aac-871">535.31</span></span></td>
<td><span data-ttu-id="a5aac-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-873">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-874">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-875">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-875">10001</span></span></td>
<td><span data-ttu-id="a5aac-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-876">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-877">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-878">178.44</span><span class="sxs-lookup"><span data-stu-id="a5aac-878">178.44</span></span></td>
<td><span data-ttu-id="a5aac-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-880">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-880">CC003</span></span></td>
<td><span data-ttu-id="a5aac-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-881">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-882">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-882">10001</span></span></td>
<td><span data-ttu-id="a5aac-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-883">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-884">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="a5aac-885">-5,982.83</span></span></td>
<td><span data-ttu-id="a5aac-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-887">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-888">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-889">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-889">10001</span></span></td>
<td><span data-ttu-id="a5aac-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-890">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-891">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a5aac-892">4,487.12</span></span></td>
<td><span data-ttu-id="a5aac-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-894">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-895">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-896">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-896">10001</span></span></td>
<td><span data-ttu-id="a5aac-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-897">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-898">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a5aac-899">1,495.71</span></span></td>
<td><span data-ttu-id="a5aac-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-901">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-901">CC003</span></span></td>
<td><span data-ttu-id="a5aac-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-902">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-903">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-903">10001</span></span></td>
<td><span data-ttu-id="a5aac-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-904">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-905">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="a5aac-906">-286.25</span></span></td>
<td><span data-ttu-id="a5aac-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-908">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-909">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-910">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-910">10001</span></span></td>
<td><span data-ttu-id="a5aac-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-911">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-912">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-913">241.05</span><span class="sxs-lookup"><span data-stu-id="a5aac-913">241.05</span></span></td>
<td><span data-ttu-id="a5aac-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-915">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-916">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-917">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-917">10001</span></span></td>
<td><span data-ttu-id="a5aac-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-918">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-919">Fixed cost</span></span></td>
<td><span data-ttu-id="a5aac-920">45.20</span><span class="sxs-lookup"><span data-stu-id="a5aac-920">45.20</span></span></td>
<td><span data-ttu-id="a5aac-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-922">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-922">CC003</span></span></td>
<td><span data-ttu-id="a5aac-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a5aac-923">Assembly</span></span></td>
<td><span data-ttu-id="a5aac-924">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-924">10001</span></span></td>
<td><span data-ttu-id="a5aac-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-925">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-926">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="a5aac-927">-2,977.17</span></span></td>
<td><span data-ttu-id="a5aac-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-929">Prod 1</span></span></td>
<td><span data-ttu-id="a5aac-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-930">Product 1</span></span></td>
<td><span data-ttu-id="a5aac-931">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-931">10001</span></span></td>
<td><span data-ttu-id="a5aac-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-932">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-933">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a5aac-934">2,507.09</span></span></td>
<td><span data-ttu-id="a5aac-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a5aac-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-936">Prod 2</span></span></td>
<td><span data-ttu-id="a5aac-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-937">Product 2</span></span></td>
<td><span data-ttu-id="a5aac-938">10001</span><span class="sxs-lookup"><span data-stu-id="a5aac-938">10001</span></span></td>
<td><span data-ttu-id="a5aac-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-939">Electricity</span></span></td>
<td><span data-ttu-id="a5aac-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-940">Variable cost</span></span></td>
<td><span data-ttu-id="a5aac-941">470.08</span><span class="sxs-lookup"><span data-stu-id="a5aac-941">470.08</span></span></td>
<td><span data-ttu-id="a5aac-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a5aac-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="a5aac-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="a5aac-943">Conclusion</span></span>
<span data-ttu-id="a5aac-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="a5aac-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="a5aac-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a5aac-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="a5aac-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a5aac-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="a5aac-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="a5aac-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a5aac-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="a5aac-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a5aac-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="a5aac-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="a5aac-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a5aac-951">CC099</span><span class="sxs-lookup"><span data-stu-id="a5aac-951">CC099</span></span></th>
<th><span data-ttu-id="a5aac-952">CC001</span><span class="sxs-lookup"><span data-stu-id="a5aac-952">CC001</span></span></th>
<th><span data-ttu-id="a5aac-953">CC002</span><span class="sxs-lookup"><span data-stu-id="a5aac-953">CC002</span></span></th>
<th><span data-ttu-id="a5aac-954">CC003</span><span class="sxs-lookup"><span data-stu-id="a5aac-954">CC003</span></span></th>
<th><span data-ttu-id="a5aac-955">CC004</span><span class="sxs-lookup"><span data-stu-id="a5aac-955">CC004</span></span></th>
<th><span data-ttu-id="a5aac-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-956">Proj 1</span></span></th>
<th><span data-ttu-id="a5aac-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-957">Proj 2</span></span></th>
<th><span data-ttu-id="a5aac-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a5aac-958">Prod 1</span></span></th>
<th><span data-ttu-id="a5aac-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a5aac-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="a5aac-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a5aac-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="a5aac-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="a5aac-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-971">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="a5aac-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-973">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-974">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-975">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-976">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-977">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-978">776.36</span><span class="sxs-lookup"><span data-stu-id="a5aac-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-979">223.64</span><span class="sxs-lookup"><span data-stu-id="a5aac-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="a5aac-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a5aac-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-982">000</span><span class="sxs-lookup"><span data-stu-id="a5aac-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-983">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-984">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-985">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-986">0,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-987">30,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-988">10,00</span><span class="sxs-lookup"><span data-stu-id="a5aac-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a5aac-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a5aac-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a5aac-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a5aac-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a5aac-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="a5aac-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="a5aac-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="a5aac-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="a5aac-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="a5aac-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="a5aac-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="a5aac-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="a5aac-996">Zie [Beleid voor totalisering van kosten en overheadberekening](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a5aac-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]