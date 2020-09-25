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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759467"
---
# <a name="overhead-calculation"></a><span data-ttu-id="718da-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="718da-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="718da-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="718da-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="718da-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="718da-105">Term definition</span></span>
---------------

<span data-ttu-id="718da-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="718da-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="718da-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="718da-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="718da-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="718da-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="718da-109">Huur</span><span class="sxs-lookup"><span data-stu-id="718da-109">Rent</span></span>
-   <span data-ttu-id="718da-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-110">Electricity</span></span>
-   <span data-ttu-id="718da-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="718da-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="718da-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="718da-112">Overhead calculation overview</span></span>
<span data-ttu-id="718da-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="718da-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="718da-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="718da-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="718da-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="718da-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="718da-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="718da-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="718da-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="718da-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="718da-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="718da-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="718da-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="718da-119">Version type</span></span>
-   <span data-ttu-id="718da-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="718da-120">Date and time</span></span>
-   <span data-ttu-id="718da-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="718da-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="718da-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="718da-122">Fiscal year</span></span>
-   <span data-ttu-id="718da-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="718da-123">Fiscal period</span></span>

<span data-ttu-id="718da-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="718da-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="718da-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="718da-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="718da-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="718da-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="718da-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="718da-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="718da-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="718da-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="718da-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="718da-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="718da-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="718da-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="718da-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="718da-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="718da-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="718da-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="718da-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="718da-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="718da-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="718da-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="718da-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="718da-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="718da-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="718da-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="718da-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="718da-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="718da-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="718da-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="718da-140">Main account</span></span></th>
<th><span data-ttu-id="718da-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="718da-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="718da-143">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-143">CC099</span></span></td>
<td><span data-ttu-id="718da-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-144">Default cost center</span></span></td>
<td><span data-ttu-id="718da-145">10001</span><span class="sxs-lookup"><span data-stu-id="718da-145">10001</span></span></td>
<td><span data-ttu-id="718da-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-146">Electricity</span></span></td>
<td><span data-ttu-id="718da-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="718da-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="718da-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="718da-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="718da-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="718da-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="718da-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="718da-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="718da-151">Define the cost behavior rule</span></span>

<span data-ttu-id="718da-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="718da-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="718da-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="718da-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="718da-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="718da-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="718da-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="718da-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="718da-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="718da-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="718da-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="718da-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="718da-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="718da-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="718da-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="718da-160">Journal</span></span></th>
<th><span data-ttu-id="718da-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="718da-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="718da-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="718da-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="718da-163">Versie</span><span class="sxs-lookup"><span data-stu-id="718da-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-164">00001</span><span class="sxs-lookup"><span data-stu-id="718da-164">00001</span></span></td>
<td><span data-ttu-id="718da-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="718da-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="718da-166">Fiscal</span></span></td>
<td><span data-ttu-id="718da-167">2017</span><span class="sxs-lookup"><span data-stu-id="718da-167">2017</span></span></td>
<td><span data-ttu-id="718da-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="718da-168">Period 1</span></span></td>
<td><span data-ttu-id="718da-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="718da-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="718da-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="718da-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="718da-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="718da-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-173">Cost element</span></span></th>
<th><span data-ttu-id="718da-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-174">Cost behavior</span></span></th>
<th><span data-ttu-id="718da-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="718da-177">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-177">CC099</span></span></td>
<td><span data-ttu-id="718da-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-178">Default cost center</span></span></td>
<td><span data-ttu-id="718da-179">10001</span><span class="sxs-lookup"><span data-stu-id="718da-179">10001</span></span></td>
<td><span data-ttu-id="718da-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-180">Electricity</span></span></td>
<td><span data-ttu-id="718da-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="718da-181">Unclassified</span></span></td>
<td><span data-ttu-id="718da-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="718da-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="718da-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="718da-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-185">Cost element</span></span></th>
<th><span data-ttu-id="718da-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-186">Cost behavior</span></span></th>
<th><span data-ttu-id="718da-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-187">Amount</span></span></th>
<th><span data-ttu-id="718da-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-189">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-189">CC099</span></span></td>
<td><span data-ttu-id="718da-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-190">Default cost center</span></span></td>
<td><span data-ttu-id="718da-191">10001</span><span class="sxs-lookup"><span data-stu-id="718da-191">10001</span></span></td>
<td><span data-ttu-id="718da-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-192">Electricity</span></span></td>
<td><span data-ttu-id="718da-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="718da-193">Unclassified</span></span></td>
<td><span data-ttu-id="718da-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-194">10,000.00</span></span></td>
<td><span data-ttu-id="718da-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-196">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-196">CC099</span></span></td>
<td><span data-ttu-id="718da-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-197">Default cost center</span></span></td>
<td><span data-ttu-id="718da-198">10001</span><span class="sxs-lookup"><span data-stu-id="718da-198">10001</span></span></td>
<td><span data-ttu-id="718da-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-199">Electricity</span></span></td>
<td><span data-ttu-id="718da-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="718da-200">Unclassified</span></span></td>
<td><span data-ttu-id="718da-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="718da-201">-10,000.00</span></span></td>
<td><span data-ttu-id="718da-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-203">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-203">CC099</span></span></td>
<td><span data-ttu-id="718da-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-204">Default cost center</span></span></td>
<td><span data-ttu-id="718da-205">10001</span><span class="sxs-lookup"><span data-stu-id="718da-205">10001</span></span></td>
<td><span data-ttu-id="718da-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-206">Electricity</span></span></td>
<td><span data-ttu-id="718da-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-207">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-208">1,000.00</span></span></td>
<td><span data-ttu-id="718da-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-210">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-210">CC099</span></span></td>
<td><span data-ttu-id="718da-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-211">Default cost center</span></span></td>
<td><span data-ttu-id="718da-212">10001</span><span class="sxs-lookup"><span data-stu-id="718da-212">10001</span></span></td>
<td><span data-ttu-id="718da-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-213">Electricity</span></span></td>
<td><span data-ttu-id="718da-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-214">Variable cost</span></span></td>
<td><span data-ttu-id="718da-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-215">9,000.00</span></span></td>
<td><span data-ttu-id="718da-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="718da-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="718da-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="718da-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="718da-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="718da-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="718da-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="718da-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="718da-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="718da-221">Define the cost distribution rule</span></span>

<span data-ttu-id="718da-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="718da-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="718da-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="718da-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="718da-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="718da-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="718da-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="718da-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="718da-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="718da-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="718da-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="718da-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-228">Cost object</span></span></th>
<th><span data-ttu-id="718da-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="718da-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-230">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-230">CC001</span></span></td>
<td><span data-ttu-id="718da-231">HR</span><span class="sxs-lookup"><span data-stu-id="718da-231">HR</span></span></td>
<td><span data-ttu-id="718da-232">1.000</span><span class="sxs-lookup"><span data-stu-id="718da-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-233">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-233">CC002</span></span></td>
<td><span data-ttu-id="718da-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-234">Finance</span></span></td>
<td><span data-ttu-id="718da-235">6.000</span><span class="sxs-lookup"><span data-stu-id="718da-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-236">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-236">CC003</span></span></td>
<td><span data-ttu-id="718da-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-237">Assembly</span></span></td>
<td><span data-ttu-id="718da-238">0</span><span class="sxs-lookup"><span data-stu-id="718da-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="718da-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-240">Cost object</span></span></th>
<th><span data-ttu-id="718da-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="718da-241">Magnitude</span></span></th>
<th><span data-ttu-id="718da-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="718da-242">Allocation factor</span></span></th>
<th><span data-ttu-id="718da-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-244">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-244">CC001</span></span></td>
<td><span data-ttu-id="718da-245">HR</span><span class="sxs-lookup"><span data-stu-id="718da-245">HR</span></span></td>
<td><span data-ttu-id="718da-246">1.000</span><span class="sxs-lookup"><span data-stu-id="718da-246">1,000</span></span></td>
<td><span data-ttu-id="718da-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="718da-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="718da-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-249">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-249">CC002</span></span></td>
<td><span data-ttu-id="718da-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-250">Finance</span></span></td>
<td><span data-ttu-id="718da-251">6.000</span><span class="sxs-lookup"><span data-stu-id="718da-251">6,000</span></span></td>
<td><span data-ttu-id="718da-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="718da-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="718da-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-254">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-254">CC003</span></span></td>
<td><span data-ttu-id="718da-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-255">Assembly</span></span></td>
<td><span data-ttu-id="718da-256">0</span><span class="sxs-lookup"><span data-stu-id="718da-256">0</span></span></td>
<td><span data-ttu-id="718da-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="718da-258">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="718da-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="718da-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="718da-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-261">Cost object</span></span></th>
<th><span data-ttu-id="718da-262">Formule</span><span class="sxs-lookup"><span data-stu-id="718da-262">Formula</span></span></th>
<th><span data-ttu-id="718da-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="718da-263">Magnitude</span></span></th>
<th><span data-ttu-id="718da-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="718da-264">Allocation factor</span></span></th>
<th><span data-ttu-id="718da-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-266">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-266">CC001</span></span></td>
<td><span data-ttu-id="718da-267">HR</span><span class="sxs-lookup"><span data-stu-id="718da-267">HR</span></span></td>
<td><span data-ttu-id="718da-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="718da-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="718da-269">1</span><span class="sxs-lookup"><span data-stu-id="718da-269">1</span></span></td>
<td><span data-ttu-id="718da-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="718da-271">500,00</span><span class="sxs-lookup"><span data-stu-id="718da-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-272">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-272">CC002</span></span></td>
<td><span data-ttu-id="718da-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-273">Finance</span></span></td>
<td><span data-ttu-id="718da-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="718da-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="718da-275">1</span><span class="sxs-lookup"><span data-stu-id="718da-275">1</span></span></td>
<td><span data-ttu-id="718da-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="718da-277">500,00</span><span class="sxs-lookup"><span data-stu-id="718da-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-278">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-278">CC003</span></span></td>
<td><span data-ttu-id="718da-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-279">Assembly</span></span></td>
<td><span data-ttu-id="718da-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="718da-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="718da-281">0</span><span class="sxs-lookup"><span data-stu-id="718da-281">0</span></span></td>
<td><span data-ttu-id="718da-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="718da-283">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="718da-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="718da-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="718da-285">Journal</span></span></th>
<th><span data-ttu-id="718da-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="718da-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="718da-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="718da-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="718da-288">Versie</span><span class="sxs-lookup"><span data-stu-id="718da-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-289">00002</span><span class="sxs-lookup"><span data-stu-id="718da-289">00002</span></span></td>
<td><span data-ttu-id="718da-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="718da-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="718da-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="718da-291">Fiscal</span></span></td>
<td><span data-ttu-id="718da-292">2017</span><span class="sxs-lookup"><span data-stu-id="718da-292">2017</span></span></td>
<td><span data-ttu-id="718da-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="718da-293">Period 1</span></span></td>
<td><span data-ttu-id="718da-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="718da-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="718da-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="718da-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="718da-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="718da-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-298">Cost element</span></span></th>
<th><span data-ttu-id="718da-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-299">Cost behavior</span></span></th>
<th><span data-ttu-id="718da-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-302">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-302">CC099</span></span></td>
<td><span data-ttu-id="718da-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-303">Default cost center</span></span></td>
<td><span data-ttu-id="718da-304">10001</span><span class="sxs-lookup"><span data-stu-id="718da-304">10001</span></span></td>
<td><span data-ttu-id="718da-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-305">Electricity</span></span></td>
<td><span data-ttu-id="718da-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-306">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-309">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-309">CC099</span></span></td>
<td><span data-ttu-id="718da-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-310">Default cost center</span></span></td>
<td><span data-ttu-id="718da-311">10001</span><span class="sxs-lookup"><span data-stu-id="718da-311">10001</span></span></td>
<td><span data-ttu-id="718da-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-312">Electricity</span></span></td>
<td><span data-ttu-id="718da-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-313">Variable cost</span></span></td>
<td><span data-ttu-id="718da-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="718da-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="718da-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="718da-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-317">Cost element</span></span></th>
<th><span data-ttu-id="718da-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-318">Cost behavior</span></span></th>
<th><span data-ttu-id="718da-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-319">Amount</span></span></th>
<th><span data-ttu-id="718da-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-321">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-321">CC099</span></span></td>
<td><span data-ttu-id="718da-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-322">Default cost center</span></span></td>
<td><span data-ttu-id="718da-323">10001</span><span class="sxs-lookup"><span data-stu-id="718da-323">10001</span></span></td>
<td><span data-ttu-id="718da-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-324">Electricity</span></span></td>
<td><span data-ttu-id="718da-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-325">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="718da-326">-1,000.00</span></span></td>
<td><span data-ttu-id="718da-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-328">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-328">CC001</span></span></td>
<td><span data-ttu-id="718da-329">HR</span><span class="sxs-lookup"><span data-stu-id="718da-329">HR</span></span></td>
<td><span data-ttu-id="718da-330">10001</span><span class="sxs-lookup"><span data-stu-id="718da-330">10001</span></span></td>
<td><span data-ttu-id="718da-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-331">Electricity</span></span></td>
<td><span data-ttu-id="718da-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-332">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-333">500,00</span><span class="sxs-lookup"><span data-stu-id="718da-333">500.00</span></span></td>
<td><span data-ttu-id="718da-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-335">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-335">CC002</span></span></td>
<td><span data-ttu-id="718da-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-336">Finance</span></span></td>
<td><span data-ttu-id="718da-337">10001</span><span class="sxs-lookup"><span data-stu-id="718da-337">10001</span></span></td>
<td><span data-ttu-id="718da-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-338">Electricity</span></span></td>
<td><span data-ttu-id="718da-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-339">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-340">500,00</span><span class="sxs-lookup"><span data-stu-id="718da-340">500.00</span></span></td>
<td><span data-ttu-id="718da-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-342">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-342">CC099</span></span></td>
<td><span data-ttu-id="718da-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="718da-343">Default cost center</span></span></td>
<td><span data-ttu-id="718da-344">10001</span><span class="sxs-lookup"><span data-stu-id="718da-344">10001</span></span></td>
<td><span data-ttu-id="718da-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-345">Electricity</span></span></td>
<td><span data-ttu-id="718da-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-346">Variable cost</span></span></td>
<td><span data-ttu-id="718da-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="718da-347">-9,000.00</span></span></td>
<td><span data-ttu-id="718da-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-349">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-349">CC001</span></span></td>
<td><span data-ttu-id="718da-350">HR</span><span class="sxs-lookup"><span data-stu-id="718da-350">HR</span></span></td>
<td><span data-ttu-id="718da-351">10001</span><span class="sxs-lookup"><span data-stu-id="718da-351">10001</span></span></td>
<td><span data-ttu-id="718da-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-352">Electricity</span></span></td>
<td><span data-ttu-id="718da-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-353">Variable cost</span></span></td>
<td><span data-ttu-id="718da-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="718da-354">1,285.71</span></span></td>
<td><span data-ttu-id="718da-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-356">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-356">CC002</span></span></td>
<td><span data-ttu-id="718da-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-357">Finance</span></span></td>
<td><span data-ttu-id="718da-358">10001</span><span class="sxs-lookup"><span data-stu-id="718da-358">10001</span></span></td>
<td><span data-ttu-id="718da-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-359">Electricity</span></span></td>
<td><span data-ttu-id="718da-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-360">Variable cost</span></span></td>
<td><span data-ttu-id="718da-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="718da-361">7,714.29</span></span></td>
<td><span data-ttu-id="718da-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="718da-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="718da-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="718da-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="718da-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="718da-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="718da-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="718da-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="718da-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="718da-367">Define the overhead rate</span></span>

<span data-ttu-id="718da-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="718da-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="718da-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="718da-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-370">Cost object</span></span></th>
<th><span data-ttu-id="718da-371">Uren</span><span class="sxs-lookup"><span data-stu-id="718da-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="718da-372">Proj 1</span></span></td>
<td><span data-ttu-id="718da-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="718da-373">Project 1</span></span></td>
<td><span data-ttu-id="718da-374">3</span><span class="sxs-lookup"><span data-stu-id="718da-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="718da-375">Proj 2</span></span></td>
<td><span data-ttu-id="718da-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="718da-376">Project 2</span></span></td>
<td><span data-ttu-id="718da-377">1</span><span class="sxs-lookup"><span data-stu-id="718da-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="718da-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-379">Cost object</span></span></th>
<th><span data-ttu-id="718da-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-380">Cost element</span></span></th>
<th><span data-ttu-id="718da-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-381">Cost behavior</span></span></th>
<th><span data-ttu-id="718da-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="718da-382">Units</span></span></th>
<th><span data-ttu-id="718da-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="718da-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-384">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-384">CC001</span></span></td>
<td><span data-ttu-id="718da-385">HR</span><span class="sxs-lookup"><span data-stu-id="718da-385">HR</span></span></td>
<td><span data-ttu-id="718da-386">10001</span><span class="sxs-lookup"><span data-stu-id="718da-386">10001</span></span></td>
<td><span data-ttu-id="718da-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-387">Variable cost</span></span></td>
<td><span data-ttu-id="718da-388">1</span><span class="sxs-lookup"><span data-stu-id="718da-388">1</span></span></td>
<td><span data-ttu-id="718da-389">10</span><span class="sxs-lookup"><span data-stu-id="718da-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="718da-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-391">Cost object</span></span></th>
<th><span data-ttu-id="718da-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="718da-392">Magnitude</span></span></th>
<th><span data-ttu-id="718da-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-393">Cost element</span></span></th>
<th><span data-ttu-id="718da-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="718da-394">Allocation factor</span></span></th>
<th><span data-ttu-id="718da-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="718da-396">Proj 1</span></span></td>
<td><span data-ttu-id="718da-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="718da-397">Project 1</span></span></td>
<td><span data-ttu-id="718da-398">3</span><span class="sxs-lookup"><span data-stu-id="718da-398">3</span></span></td>
<td><span data-ttu-id="718da-399">10001</span><span class="sxs-lookup"><span data-stu-id="718da-399">10001</span></span></td>
<td><span data-ttu-id="718da-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="718da-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="718da-401">30,00</span><span class="sxs-lookup"><span data-stu-id="718da-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="718da-402">Proj 2</span></span></td>
<td><span data-ttu-id="718da-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="718da-403">Project 2</span></span></td>
<td><span data-ttu-id="718da-404">1</span><span class="sxs-lookup"><span data-stu-id="718da-404">1</span></span></td>
<td><span data-ttu-id="718da-405">10001</span><span class="sxs-lookup"><span data-stu-id="718da-405">10001</span></span></td>
<td><span data-ttu-id="718da-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="718da-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="718da-407">10,00</span><span class="sxs-lookup"><span data-stu-id="718da-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="718da-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="718da-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="718da-409">Journal</span></span></th>
<th><span data-ttu-id="718da-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="718da-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="718da-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="718da-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="718da-412">Versie</span><span class="sxs-lookup"><span data-stu-id="718da-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-413">00003</span><span class="sxs-lookup"><span data-stu-id="718da-413">00003</span></span></td>
<td><span data-ttu-id="718da-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="718da-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="718da-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="718da-415">Fiscal</span></span></td>
<td><span data-ttu-id="718da-416">2017</span><span class="sxs-lookup"><span data-stu-id="718da-416">2017</span></span></td>
<td><span data-ttu-id="718da-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="718da-417">Period 1</span></span></td>
<td><span data-ttu-id="718da-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="718da-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="718da-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="718da-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="718da-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-421">Cost object</span></span></th>
<th><span data-ttu-id="718da-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="718da-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="718da-424">Proj 1</span></span></td>
<td><span data-ttu-id="718da-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="718da-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="718da-426">3,00</span><span class="sxs-lookup"><span data-stu-id="718da-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="718da-428">Proj 2</span></span></td>
<td><span data-ttu-id="718da-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="718da-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="718da-430">1,00</span><span class="sxs-lookup"><span data-stu-id="718da-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="718da-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="718da-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="718da-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-433">Cost element</span></span></th>
<th><span data-ttu-id="718da-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-434">Cost behavior</span></span></th>
<th><span data-ttu-id="718da-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-435">Amount</span></span></th>
<th><span data-ttu-id="718da-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="718da-437">CC0001</span></span></td>
<td><span data-ttu-id="718da-438">HR</span><span class="sxs-lookup"><span data-stu-id="718da-438">HR</span></span></td>
<td><span data-ttu-id="718da-439">10001</span><span class="sxs-lookup"><span data-stu-id="718da-439">10001</span></span></td>
<td><span data-ttu-id="718da-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-440">Electricity</span></span></td>
<td><span data-ttu-id="718da-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-441">Variable cost</span></span></td>
<td><span data-ttu-id="718da-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="718da-442">-30.00</span></span></td>
<td><span data-ttu-id="718da-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="718da-444">Proj 1</span></span></td>
<td><span data-ttu-id="718da-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="718da-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="718da-446">10001</span><span class="sxs-lookup"><span data-stu-id="718da-446">10001</span></span></td>
<td><span data-ttu-id="718da-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-447">Electricity</span></span></td>
<td><span data-ttu-id="718da-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-448">Variable cost</span></span></td>
<td><span data-ttu-id="718da-449">30,00</span><span class="sxs-lookup"><span data-stu-id="718da-449">30.00</span></span></td>
<td><span data-ttu-id="718da-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-451">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-451">CC001</span></span></td>
<td><span data-ttu-id="718da-452">HR</span><span class="sxs-lookup"><span data-stu-id="718da-452">HR</span></span></td>
<td><span data-ttu-id="718da-453">10001</span><span class="sxs-lookup"><span data-stu-id="718da-453">10001</span></span></td>
<td><span data-ttu-id="718da-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-454">Electricity</span></span></td>
<td><span data-ttu-id="718da-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-455">Variable cost</span></span></td>
<td><span data-ttu-id="718da-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="718da-456">-10.00</span></span></td>
<td><span data-ttu-id="718da-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="718da-458">Proj 2</span></span></td>
<td><span data-ttu-id="718da-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="718da-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="718da-460">10001</span><span class="sxs-lookup"><span data-stu-id="718da-460">10001</span></span></td>
<td><span data-ttu-id="718da-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-461">Electricity</span></span></td>
<td><span data-ttu-id="718da-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-462">Variable cost</span></span></td>
<td><span data-ttu-id="718da-463">10.00</span><span class="sxs-lookup"><span data-stu-id="718da-463">10.00</span></span></td>
<td><span data-ttu-id="718da-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="718da-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="718da-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="718da-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="718da-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="718da-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="718da-468">Finance ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="718da-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="718da-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="718da-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="718da-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="718da-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="718da-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="718da-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="718da-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="718da-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="718da-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="718da-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="718da-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="718da-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="718da-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="718da-475">Define the cost allocation</span></span>

<span data-ttu-id="718da-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="718da-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="718da-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="718da-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="718da-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="718da-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-479">Cost object</span></span></th>
<th><span data-ttu-id="718da-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="718da-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-481">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-481">CC002</span></span></td>
<td><span data-ttu-id="718da-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-482">Finance</span></span></td>
<td><span data-ttu-id="718da-483">35</span><span class="sxs-lookup"><span data-stu-id="718da-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-484">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-484">CC003</span></span></td>
<td><span data-ttu-id="718da-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-485">Assembly</span></span></td>
<td><span data-ttu-id="718da-486">55</span><span class="sxs-lookup"><span data-stu-id="718da-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-487">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-487">CC004</span></span></td>
<td><span data-ttu-id="718da-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-488">Packaging</span></span></td>
<td><span data-ttu-id="718da-489">10</span><span class="sxs-lookup"><span data-stu-id="718da-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="718da-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="718da-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="718da-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-492">Cost object</span></span></th>
<th><span data-ttu-id="718da-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="718da-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-494">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-494">CC003</span></span></td>
<td><span data-ttu-id="718da-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-495">Assembly</span></span></td>
<td><span data-ttu-id="718da-496">65</span><span class="sxs-lookup"><span data-stu-id="718da-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-497">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-497">CC004</span></span></td>
<td><span data-ttu-id="718da-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-498">Packaging</span></span></td>
<td><span data-ttu-id="718da-499">35</span><span class="sxs-lookup"><span data-stu-id="718da-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="718da-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="718da-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="718da-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-502">Cost object</span></span></th>
<th><span data-ttu-id="718da-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="718da-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-504">Prod 1</span></span></td>
<td><span data-ttu-id="718da-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-505">Product 1</span></span></td>
<td><span data-ttu-id="718da-506">60</span><span class="sxs-lookup"><span data-stu-id="718da-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-507">Prod 2</span></span></td>
<td><span data-ttu-id="718da-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-508">Product 2</span></span></td>
<td><span data-ttu-id="718da-509">20</span><span class="sxs-lookup"><span data-stu-id="718da-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="718da-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="718da-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="718da-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-512">Cost object</span></span></th>
<th><span data-ttu-id="718da-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="718da-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-514">Prod 1</span></span></td>
<td><span data-ttu-id="718da-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-515">Product 1</span></span></td>
<td><span data-ttu-id="718da-516">80</span><span class="sxs-lookup"><span data-stu-id="718da-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-517">Prod 2</span></span></td>
<td><span data-ttu-id="718da-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-518">Product 2</span></span></td>
<td><span data-ttu-id="718da-519">15</span><span class="sxs-lookup"><span data-stu-id="718da-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="718da-520">Statistische metingen, zoals de productie-uren die een product verbruikt, kunnen worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="718da-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="718da-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="718da-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="718da-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="718da-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-523">Cost object</span></span></th>
<th><span data-ttu-id="718da-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="718da-524">Magnitude</span></span></th>
<th><span data-ttu-id="718da-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="718da-525">Allocation factor</span></span></th>
<th><span data-ttu-id="718da-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-526">Amount</span></span></th>
<th><span data-ttu-id="718da-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-528">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-528">CC002</span></span></td>
<td><span data-ttu-id="718da-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-529">Finance</span></span></td>
<td><span data-ttu-id="718da-530">35</span><span class="sxs-lookup"><span data-stu-id="718da-530">35</span></span></td>
<td><span data-ttu-id="718da-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="718da-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="718da-532">175.00</span><span class="sxs-lookup"><span data-stu-id="718da-532">175.00</span></span></td>
<td><span data-ttu-id="718da-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-534">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-534">CC003</span></span></td>
<td><span data-ttu-id="718da-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-535">Assembly</span></span></td>
<td><span data-ttu-id="718da-536">55</span><span class="sxs-lookup"><span data-stu-id="718da-536">55</span></span></td>
<td><span data-ttu-id="718da-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="718da-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="718da-538">275.00</span><span class="sxs-lookup"><span data-stu-id="718da-538">275.00</span></span></td>
<td><span data-ttu-id="718da-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-540">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-540">CC004</span></span></td>
<td><span data-ttu-id="718da-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-541">Packaging</span></span></td>
<td><span data-ttu-id="718da-542">10</span><span class="sxs-lookup"><span data-stu-id="718da-542">10</span></span></td>
<td><span data-ttu-id="718da-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="718da-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="718da-544">50,00</span><span class="sxs-lookup"><span data-stu-id="718da-544">50.00</span></span></td>
<td><span data-ttu-id="718da-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-546">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-546">CC002</span></span></td>
<td><span data-ttu-id="718da-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-547">Finance</span></span></td>
<td><span data-ttu-id="718da-548">35</span><span class="sxs-lookup"><span data-stu-id="718da-548">35</span></span></td>
<td><span data-ttu-id="718da-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="718da-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="718da-550">436.00</span><span class="sxs-lookup"><span data-stu-id="718da-550">436.00</span></span></td>
<td><span data-ttu-id="718da-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-552">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-552">CC003</span></span></td>
<td><span data-ttu-id="718da-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-553">Assembly</span></span></td>
<td><span data-ttu-id="718da-554">55</span><span class="sxs-lookup"><span data-stu-id="718da-554">55</span></span></td>
<td><span data-ttu-id="718da-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="718da-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="718da-556">685.14</span><span class="sxs-lookup"><span data-stu-id="718da-556">685.14</span></span></td>
<td><span data-ttu-id="718da-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-558">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-558">CC004</span></span></td>
<td><span data-ttu-id="718da-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-559">Packaging</span></span></td>
<td><span data-ttu-id="718da-560">10</span><span class="sxs-lookup"><span data-stu-id="718da-560">10</span></span></td>
<td><span data-ttu-id="718da-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="718da-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="718da-562">124.57</span><span class="sxs-lookup"><span data-stu-id="718da-562">124.57</span></span></td>
<td><span data-ttu-id="718da-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="718da-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-565">Cost object</span></span></th>
<th><span data-ttu-id="718da-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="718da-566">Magnitude</span></span></th>
<th><span data-ttu-id="718da-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="718da-567">Allocation factor</span></span></th>
<th><span data-ttu-id="718da-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-568">Amount</span></span></th>
<th><span data-ttu-id="718da-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-570">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-570">CC003</span></span></td>
<td><span data-ttu-id="718da-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-571">Assembly</span></span></td>
<td><span data-ttu-id="718da-572">65</span><span class="sxs-lookup"><span data-stu-id="718da-572">65</span></span></td>
<td><span data-ttu-id="718da-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="718da-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="718da-574">438.75</span><span class="sxs-lookup"><span data-stu-id="718da-574">438.75</span></span></td>
<td><span data-ttu-id="718da-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-576">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-576">CC004</span></span></td>
<td><span data-ttu-id="718da-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-577">Packaging</span></span></td>
<td><span data-ttu-id="718da-578">35</span><span class="sxs-lookup"><span data-stu-id="718da-578">35</span></span></td>
<td><span data-ttu-id="718da-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="718da-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="718da-580">236.25</span><span class="sxs-lookup"><span data-stu-id="718da-580">236.25</span></span></td>
<td><span data-ttu-id="718da-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-582">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-582">CC003</span></span></td>
<td><span data-ttu-id="718da-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-583">Assembly</span></span></td>
<td><span data-ttu-id="718da-584">65</span><span class="sxs-lookup"><span data-stu-id="718da-584">65</span></span></td>
<td><span data-ttu-id="718da-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="718da-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="718da-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="718da-586">5,297.69</span></span></td>
<td><span data-ttu-id="718da-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-588">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-588">CC004</span></span></td>
<td><span data-ttu-id="718da-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-589">Packaging</span></span></td>
<td><span data-ttu-id="718da-590">35</span><span class="sxs-lookup"><span data-stu-id="718da-590">35</span></span></td>
<td><span data-ttu-id="718da-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="718da-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="718da-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="718da-592">2,852.60</span></span></td>
<td><span data-ttu-id="718da-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="718da-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-595">Cost object</span></span></th>
<th><span data-ttu-id="718da-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="718da-596">Magnitude</span></span></th>
<th><span data-ttu-id="718da-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="718da-597">Allocation factor</span></span></th>
<th><span data-ttu-id="718da-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-598">Amount</span></span></th>
<th><span data-ttu-id="718da-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-600">Prod 1</span></span></td>
<td><span data-ttu-id="718da-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-601">Product 1</span></span></td>
<td><span data-ttu-id="718da-602">60</span><span class="sxs-lookup"><span data-stu-id="718da-602">60</span></span></td>
<td><span data-ttu-id="718da-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="718da-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="718da-604">535.31</span><span class="sxs-lookup"><span data-stu-id="718da-604">535.31</span></span></td>
<td><span data-ttu-id="718da-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-606">Prod 2</span></span></td>
<td><span data-ttu-id="718da-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-607">Product 2</span></span></td>
<td><span data-ttu-id="718da-608">20</span><span class="sxs-lookup"><span data-stu-id="718da-608">20</span></span></td>
<td><span data-ttu-id="718da-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="718da-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="718da-610">178.44</span><span class="sxs-lookup"><span data-stu-id="718da-610">178.44</span></span></td>
<td><span data-ttu-id="718da-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-612">Prod 1</span></span></td>
<td><span data-ttu-id="718da-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-613">Product 1</span></span></td>
<td><span data-ttu-id="718da-614">60</span><span class="sxs-lookup"><span data-stu-id="718da-614">60</span></span></td>
<td><span data-ttu-id="718da-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="718da-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="718da-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="718da-616">4,487.12</span></span></td>
<td><span data-ttu-id="718da-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-618">Prod 2</span></span></td>
<td><span data-ttu-id="718da-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-619">Product 2</span></span></td>
<td><span data-ttu-id="718da-620">20</span><span class="sxs-lookup"><span data-stu-id="718da-620">20</span></span></td>
<td><span data-ttu-id="718da-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="718da-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="718da-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="718da-622">1,495.71</span></span></td>
<td><span data-ttu-id="718da-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="718da-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="718da-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-625">Cost object</span></span></th>
<th><span data-ttu-id="718da-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="718da-626">Magnitude</span></span></th>
<th><span data-ttu-id="718da-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="718da-627">Allocation factor</span></span></th>
<th><span data-ttu-id="718da-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-628">Amount</span></span></th>
<th><span data-ttu-id="718da-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-630">Prod 1</span></span></td>
<td><span data-ttu-id="718da-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-631">Product 1</span></span></td>
<td><span data-ttu-id="718da-632">80</span><span class="sxs-lookup"><span data-stu-id="718da-632">80</span></span></td>
<td><span data-ttu-id="718da-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="718da-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="718da-634">241.05</span><span class="sxs-lookup"><span data-stu-id="718da-634">241.05</span></span></td>
<td><span data-ttu-id="718da-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-636">Prod 2</span></span></td>
<td><span data-ttu-id="718da-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-637">Product 2</span></span></td>
<td><span data-ttu-id="718da-638">15</span><span class="sxs-lookup"><span data-stu-id="718da-638">15</span></span></td>
<td><span data-ttu-id="718da-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="718da-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="718da-640">45.20</span><span class="sxs-lookup"><span data-stu-id="718da-640">45.20</span></span></td>
<td><span data-ttu-id="718da-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-642">Prod 1</span></span></td>
<td><span data-ttu-id="718da-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-643">Product 1</span></span></td>
<td><span data-ttu-id="718da-644">80</span><span class="sxs-lookup"><span data-stu-id="718da-644">80</span></span></td>
<td><span data-ttu-id="718da-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="718da-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="718da-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="718da-646">2,507.09</span></span></td>
<td><span data-ttu-id="718da-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-648">Prod 2</span></span></td>
<td><span data-ttu-id="718da-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-649">Product 2</span></span></td>
<td><span data-ttu-id="718da-650">15</span><span class="sxs-lookup"><span data-stu-id="718da-650">15</span></span></td>
<td><span data-ttu-id="718da-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="718da-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="718da-652">470.08</span><span class="sxs-lookup"><span data-stu-id="718da-652">470.08</span></span></td>
<td><span data-ttu-id="718da-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="718da-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="718da-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="718da-655">Journal</span></span></th>
<th><span data-ttu-id="718da-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="718da-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="718da-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="718da-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="718da-658">Versie</span><span class="sxs-lookup"><span data-stu-id="718da-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-659">00004</span><span class="sxs-lookup"><span data-stu-id="718da-659">00004</span></span></td>
<td><span data-ttu-id="718da-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="718da-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="718da-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="718da-661">Fiscal</span></span></td>
<td><span data-ttu-id="718da-662">2017</span><span class="sxs-lookup"><span data-stu-id="718da-662">2017</span></span></td>
<td><span data-ttu-id="718da-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="718da-663">Period 1</span></span></td>
<td><span data-ttu-id="718da-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="718da-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="718da-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="718da-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="718da-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="718da-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="718da-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-668">Cost element</span></span></th>
<th><span data-ttu-id="718da-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-669">Cost behavior</span></span></th>
<th><span data-ttu-id="718da-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-672">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-672">CC001</span></span></td>
<td><span data-ttu-id="718da-673">HR</span><span class="sxs-lookup"><span data-stu-id="718da-673">HR</span></span></td>
<td><span data-ttu-id="718da-674">10001</span><span class="sxs-lookup"><span data-stu-id="718da-674">10001</span></span></td>
<td><span data-ttu-id="718da-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-675">Electricity</span></span></td>
<td><span data-ttu-id="718da-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-676">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-677">500,00</span><span class="sxs-lookup"><span data-stu-id="718da-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-679">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-679">CC001</span></span></td>
<td><span data-ttu-id="718da-680">HR</span><span class="sxs-lookup"><span data-stu-id="718da-680">HR</span></span></td>
<td><span data-ttu-id="718da-681">10001</span><span class="sxs-lookup"><span data-stu-id="718da-681">10001</span></span></td>
<td><span data-ttu-id="718da-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-682">Electricity</span></span></td>
<td><span data-ttu-id="718da-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-683">Variable cost</span></span></td>
<td><span data-ttu-id="718da-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="718da-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-686">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-686">CC002</span></span></td>
<td><span data-ttu-id="718da-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-687">Finance</span></span></td>
<td><span data-ttu-id="718da-688">10001</span><span class="sxs-lookup"><span data-stu-id="718da-688">10001</span></span></td>
<td><span data-ttu-id="718da-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-689">Electricity</span></span></td>
<td><span data-ttu-id="718da-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-690">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-691">675.00</span><span class="sxs-lookup"><span data-stu-id="718da-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-693">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-693">CC002</span></span></td>
<td><span data-ttu-id="718da-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-694">Finance</span></span></td>
<td><span data-ttu-id="718da-695">10001</span><span class="sxs-lookup"><span data-stu-id="718da-695">10001</span></span></td>
<td><span data-ttu-id="718da-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-696">Electricity</span></span></td>
<td><span data-ttu-id="718da-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-697">Variable cost</span></span></td>
<td><span data-ttu-id="718da-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="718da-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-700">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-700">CC003</span></span></td>
<td><span data-ttu-id="718da-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-701">Assembly</span></span></td>
<td><span data-ttu-id="718da-702">10001</span><span class="sxs-lookup"><span data-stu-id="718da-702">10001</span></span></td>
<td><span data-ttu-id="718da-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-703">Electricity</span></span></td>
<td><span data-ttu-id="718da-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-704">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-705">713.75</span><span class="sxs-lookup"><span data-stu-id="718da-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-707">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-707">CC003</span></span></td>
<td><span data-ttu-id="718da-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-708">Assembly</span></span></td>
<td><span data-ttu-id="718da-709">10001</span><span class="sxs-lookup"><span data-stu-id="718da-709">10001</span></span></td>
<td><span data-ttu-id="718da-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-710">Electricity</span></span></td>
<td><span data-ttu-id="718da-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-711">Variable cost</span></span></td>
<td><span data-ttu-id="718da-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="718da-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-714">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-714">CC003</span></span></td>
<td><span data-ttu-id="718da-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-715">Packaging</span></span></td>
<td><span data-ttu-id="718da-716">10001</span><span class="sxs-lookup"><span data-stu-id="718da-716">10001</span></span></td>
<td><span data-ttu-id="718da-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-717">Electricity</span></span></td>
<td><span data-ttu-id="718da-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-718">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-719">286.25</span><span class="sxs-lookup"><span data-stu-id="718da-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-721">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-721">CC003</span></span></td>
<td><span data-ttu-id="718da-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-722">Packaging</span></span></td>
<td><span data-ttu-id="718da-723">10001</span><span class="sxs-lookup"><span data-stu-id="718da-723">10001</span></span></td>
<td><span data-ttu-id="718da-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-724">Electricity</span></span></td>
<td><span data-ttu-id="718da-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-725">Variable cost</span></span></td>
<td><span data-ttu-id="718da-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="718da-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-728">Prod 1</span></span></td>
<td><span data-ttu-id="718da-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-729">Product 1</span></span></td>
<td><span data-ttu-id="718da-730">10001</span><span class="sxs-lookup"><span data-stu-id="718da-730">10001</span></span></td>
<td><span data-ttu-id="718da-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-731">Electricity</span></span></td>
<td><span data-ttu-id="718da-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-732">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-733">776.36</span><span class="sxs-lookup"><span data-stu-id="718da-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-735">Prod 1</span></span></td>
<td><span data-ttu-id="718da-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-736">Product 1</span></span></td>
<td><span data-ttu-id="718da-737">10001</span><span class="sxs-lookup"><span data-stu-id="718da-737">10001</span></span></td>
<td><span data-ttu-id="718da-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-738">Electricity</span></span></td>
<td><span data-ttu-id="718da-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-739">Variable cost</span></span></td>
<td><span data-ttu-id="718da-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="718da-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-742">Prod 2</span></span></td>
<td><span data-ttu-id="718da-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-743">Product 1</span></span></td>
<td><span data-ttu-id="718da-744">10001</span><span class="sxs-lookup"><span data-stu-id="718da-744">10001</span></span></td>
<td><span data-ttu-id="718da-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-745">Electricity</span></span></td>
<td><span data-ttu-id="718da-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-746">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-747">223.64</span><span class="sxs-lookup"><span data-stu-id="718da-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="718da-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-749">Prod 2</span></span></td>
<td><span data-ttu-id="718da-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-750">Product 1</span></span></td>
<td><span data-ttu-id="718da-751">10001</span><span class="sxs-lookup"><span data-stu-id="718da-751">10001</span></span></td>
<td><span data-ttu-id="718da-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-752">Electricity</span></span></td>
<td><span data-ttu-id="718da-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-753">Variable cost</span></span></td>
<td><span data-ttu-id="718da-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="718da-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="718da-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="718da-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="718da-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="718da-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-757">Cost element</span></span></th>
<th><span data-ttu-id="718da-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="718da-758">Cost behavior</span></span></th>
<th><span data-ttu-id="718da-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="718da-759">Amount</span></span></th>
<th><span data-ttu-id="718da-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="718da-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="718da-761">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-761">CC001</span></span></td>
<td><span data-ttu-id="718da-762">HR</span><span class="sxs-lookup"><span data-stu-id="718da-762">HR</span></span></td>
<td><span data-ttu-id="718da-763">10001</span><span class="sxs-lookup"><span data-stu-id="718da-763">10001</span></span></td>
<td><span data-ttu-id="718da-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-764">Electricity</span></span></td>
<td><span data-ttu-id="718da-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-765">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="718da-766">-500.00</span></span></td>
<td><span data-ttu-id="718da-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-768">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-768">CC002</span></span></td>
<td><span data-ttu-id="718da-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-769">Finance</span></span></td>
<td><span data-ttu-id="718da-770">10001</span><span class="sxs-lookup"><span data-stu-id="718da-770">10001</span></span></td>
<td><span data-ttu-id="718da-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-771">Electricity</span></span></td>
<td><span data-ttu-id="718da-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-772">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-773">175.00</span><span class="sxs-lookup"><span data-stu-id="718da-773">175.00</span></span></td>
<td><span data-ttu-id="718da-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-775">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-775">CC003</span></span></td>
<td><span data-ttu-id="718da-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-776">Assembly</span></span></td>
<td><span data-ttu-id="718da-777">10001</span><span class="sxs-lookup"><span data-stu-id="718da-777">10001</span></span></td>
<td><span data-ttu-id="718da-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-778">Electricity</span></span></td>
<td><span data-ttu-id="718da-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-779">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-780">275.00</span><span class="sxs-lookup"><span data-stu-id="718da-780">275.00</span></span></td>
<td><span data-ttu-id="718da-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-782">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-782">CC004</span></span></td>
<td><span data-ttu-id="718da-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-783">Packaging</span></span></td>
<td><span data-ttu-id="718da-784">10001</span><span class="sxs-lookup"><span data-stu-id="718da-784">10001</span></span></td>
<td><span data-ttu-id="718da-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-785">Electricity</span></span></td>
<td><span data-ttu-id="718da-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-786">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-787">50,00</span><span class="sxs-lookup"><span data-stu-id="718da-787">50,00</span></span></td>
<td><span data-ttu-id="718da-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-789">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-789">CC001</span></span></td>
<td><span data-ttu-id="718da-790">HR</span><span class="sxs-lookup"><span data-stu-id="718da-790">HR</span></span></td>
<td><span data-ttu-id="718da-791">10001</span><span class="sxs-lookup"><span data-stu-id="718da-791">10001</span></span></td>
<td><span data-ttu-id="718da-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-792">Electricity</span></span></td>
<td><span data-ttu-id="718da-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-793">Variable cost</span></span></td>
<td><span data-ttu-id="718da-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="718da-794">-1,245.71</span></span></td>
<td><span data-ttu-id="718da-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-796">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-796">CC002</span></span></td>
<td><span data-ttu-id="718da-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-797">Finance</span></span></td>
<td><span data-ttu-id="718da-798">10001</span><span class="sxs-lookup"><span data-stu-id="718da-798">10001</span></span></td>
<td><span data-ttu-id="718da-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-799">Electricity</span></span></td>
<td><span data-ttu-id="718da-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-800">Variable cost</span></span></td>
<td><span data-ttu-id="718da-801">436.00</span><span class="sxs-lookup"><span data-stu-id="718da-801">436.00</span></span></td>
<td><span data-ttu-id="718da-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-803">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-803">CC003</span></span></td>
<td><span data-ttu-id="718da-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-804">Assembly</span></span></td>
<td><span data-ttu-id="718da-805">10001</span><span class="sxs-lookup"><span data-stu-id="718da-805">10001</span></span></td>
<td><span data-ttu-id="718da-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-806">Electricity</span></span></td>
<td><span data-ttu-id="718da-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-807">Variable cost</span></span></td>
<td><span data-ttu-id="718da-808">685.14</span><span class="sxs-lookup"><span data-stu-id="718da-808">685.14</span></span></td>
<td><span data-ttu-id="718da-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-810">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-810">CC004</span></span></td>
<td><span data-ttu-id="718da-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-811">Packaging</span></span></td>
<td><span data-ttu-id="718da-812">10001</span><span class="sxs-lookup"><span data-stu-id="718da-812">10001</span></span></td>
<td><span data-ttu-id="718da-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-813">Electricity</span></span></td>
<td><span data-ttu-id="718da-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-814">Variable cost</span></span></td>
<td><span data-ttu-id="718da-815">124.57</span><span class="sxs-lookup"><span data-stu-id="718da-815">124.57</span></span></td>
<td><span data-ttu-id="718da-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-817">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-817">CC002</span></span></td>
<td><span data-ttu-id="718da-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-818">Finance</span></span></td>
<td><span data-ttu-id="718da-819">10001</span><span class="sxs-lookup"><span data-stu-id="718da-819">10001</span></span></td>
<td><span data-ttu-id="718da-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-820">Electricity</span></span></td>
<td><span data-ttu-id="718da-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-821">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="718da-822">-675.00</span></span></td>
<td><span data-ttu-id="718da-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-824">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-824">CC003</span></span></td>
<td><span data-ttu-id="718da-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-825">Assembly</span></span></td>
<td><span data-ttu-id="718da-826">10001</span><span class="sxs-lookup"><span data-stu-id="718da-826">10001</span></span></td>
<td><span data-ttu-id="718da-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-827">Electricity</span></span></td>
<td><span data-ttu-id="718da-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-828">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-829">438.75</span><span class="sxs-lookup"><span data-stu-id="718da-829">438.75</span></span></td>
<td><span data-ttu-id="718da-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-831">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-831">CC004</span></span></td>
<td><span data-ttu-id="718da-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-832">Packaging</span></span></td>
<td><span data-ttu-id="718da-833">10001</span><span class="sxs-lookup"><span data-stu-id="718da-833">10001</span></span></td>
<td><span data-ttu-id="718da-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-834">Electricity</span></span></td>
<td><span data-ttu-id="718da-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-835">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-836">236.25</span><span class="sxs-lookup"><span data-stu-id="718da-836">236.25</span></span></td>
<td><span data-ttu-id="718da-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-838">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-838">CC002</span></span></td>
<td><span data-ttu-id="718da-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="718da-839">Finance</span></span></td>
<td><span data-ttu-id="718da-840">10001</span><span class="sxs-lookup"><span data-stu-id="718da-840">10001</span></span></td>
<td><span data-ttu-id="718da-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-841">Electricity</span></span></td>
<td><span data-ttu-id="718da-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-842">Variable cost</span></span></td>
<td><span data-ttu-id="718da-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="718da-843">-8,150.29</span></span></td>
<td><span data-ttu-id="718da-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-845">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-845">CC003</span></span></td>
<td><span data-ttu-id="718da-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-846">Assembly</span></span></td>
<td><span data-ttu-id="718da-847">10001</span><span class="sxs-lookup"><span data-stu-id="718da-847">10001</span></span></td>
<td><span data-ttu-id="718da-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-848">Electricity</span></span></td>
<td><span data-ttu-id="718da-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-849">Variable cost</span></span></td>
<td><span data-ttu-id="718da-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="718da-850">5,297.69</span></span></td>
<td><span data-ttu-id="718da-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-852">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-852">CC004</span></span></td>
<td><span data-ttu-id="718da-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="718da-853">Packaging</span></span></td>
<td><span data-ttu-id="718da-854">10001</span><span class="sxs-lookup"><span data-stu-id="718da-854">10001</span></span></td>
<td><span data-ttu-id="718da-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-855">Electricity</span></span></td>
<td><span data-ttu-id="718da-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-856">Variable cost</span></span></td>
<td><span data-ttu-id="718da-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="718da-857">2,852.60</span></span></td>
<td><span data-ttu-id="718da-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-859">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-859">CC003</span></span></td>
<td><span data-ttu-id="718da-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-860">Assembly</span></span></td>
<td><span data-ttu-id="718da-861">10001</span><span class="sxs-lookup"><span data-stu-id="718da-861">10001</span></span></td>
<td><span data-ttu-id="718da-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-862">Electricity</span></span></td>
<td><span data-ttu-id="718da-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-863">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="718da-864">-713.75</span></span></td>
<td><span data-ttu-id="718da-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-866">Prod 1</span></span></td>
<td><span data-ttu-id="718da-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-867">Product 1</span></span></td>
<td><span data-ttu-id="718da-868">10001</span><span class="sxs-lookup"><span data-stu-id="718da-868">10001</span></span></td>
<td><span data-ttu-id="718da-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-869">Electricity</span></span></td>
<td><span data-ttu-id="718da-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-870">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-871">535.31</span><span class="sxs-lookup"><span data-stu-id="718da-871">535.31</span></span></td>
<td><span data-ttu-id="718da-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-873">Prod 2</span></span></td>
<td><span data-ttu-id="718da-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-874">Product 2</span></span></td>
<td><span data-ttu-id="718da-875">10001</span><span class="sxs-lookup"><span data-stu-id="718da-875">10001</span></span></td>
<td><span data-ttu-id="718da-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-876">Electricity</span></span></td>
<td><span data-ttu-id="718da-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-877">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-878">178.44</span><span class="sxs-lookup"><span data-stu-id="718da-878">178.44</span></span></td>
<td><span data-ttu-id="718da-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-880">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-880">CC003</span></span></td>
<td><span data-ttu-id="718da-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-881">Assembly</span></span></td>
<td><span data-ttu-id="718da-882">10001</span><span class="sxs-lookup"><span data-stu-id="718da-882">10001</span></span></td>
<td><span data-ttu-id="718da-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-883">Electricity</span></span></td>
<td><span data-ttu-id="718da-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-884">Variable cost</span></span></td>
<td><span data-ttu-id="718da-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="718da-885">-5,982.83</span></span></td>
<td><span data-ttu-id="718da-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-887">Prod 1</span></span></td>
<td><span data-ttu-id="718da-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-888">Product 1</span></span></td>
<td><span data-ttu-id="718da-889">10001</span><span class="sxs-lookup"><span data-stu-id="718da-889">10001</span></span></td>
<td><span data-ttu-id="718da-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-890">Electricity</span></span></td>
<td><span data-ttu-id="718da-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-891">Variable cost</span></span></td>
<td><span data-ttu-id="718da-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="718da-892">4,487.12</span></span></td>
<td><span data-ttu-id="718da-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-894">Prod 2</span></span></td>
<td><span data-ttu-id="718da-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-895">Product 2</span></span></td>
<td><span data-ttu-id="718da-896">10001</span><span class="sxs-lookup"><span data-stu-id="718da-896">10001</span></span></td>
<td><span data-ttu-id="718da-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-897">Electricity</span></span></td>
<td><span data-ttu-id="718da-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-898">Variable cost</span></span></td>
<td><span data-ttu-id="718da-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="718da-899">1,495.71</span></span></td>
<td><span data-ttu-id="718da-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-901">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-901">CC003</span></span></td>
<td><span data-ttu-id="718da-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-902">Assembly</span></span></td>
<td><span data-ttu-id="718da-903">10001</span><span class="sxs-lookup"><span data-stu-id="718da-903">10001</span></span></td>
<td><span data-ttu-id="718da-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-904">Electricity</span></span></td>
<td><span data-ttu-id="718da-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-905">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="718da-906">-286.25</span></span></td>
<td><span data-ttu-id="718da-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-908">Prod 1</span></span></td>
<td><span data-ttu-id="718da-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-909">Product 1</span></span></td>
<td><span data-ttu-id="718da-910">10001</span><span class="sxs-lookup"><span data-stu-id="718da-910">10001</span></span></td>
<td><span data-ttu-id="718da-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-911">Electricity</span></span></td>
<td><span data-ttu-id="718da-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-912">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-913">241.05</span><span class="sxs-lookup"><span data-stu-id="718da-913">241.05</span></span></td>
<td><span data-ttu-id="718da-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-915">Prod 2</span></span></td>
<td><span data-ttu-id="718da-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-916">Product 2</span></span></td>
<td><span data-ttu-id="718da-917">10001</span><span class="sxs-lookup"><span data-stu-id="718da-917">10001</span></span></td>
<td><span data-ttu-id="718da-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-918">Electricity</span></span></td>
<td><span data-ttu-id="718da-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-919">Fixed cost</span></span></td>
<td><span data-ttu-id="718da-920">45.20</span><span class="sxs-lookup"><span data-stu-id="718da-920">45.20</span></span></td>
<td><span data-ttu-id="718da-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-922">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-922">CC003</span></span></td>
<td><span data-ttu-id="718da-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="718da-923">Assembly</span></span></td>
<td><span data-ttu-id="718da-924">10001</span><span class="sxs-lookup"><span data-stu-id="718da-924">10001</span></span></td>
<td><span data-ttu-id="718da-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-925">Electricity</span></span></td>
<td><span data-ttu-id="718da-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-926">Variable cost</span></span></td>
<td><span data-ttu-id="718da-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="718da-927">-2,977.17</span></span></td>
<td><span data-ttu-id="718da-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-929">Prod 1</span></span></td>
<td><span data-ttu-id="718da-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="718da-930">Product 1</span></span></td>
<td><span data-ttu-id="718da-931">10001</span><span class="sxs-lookup"><span data-stu-id="718da-931">10001</span></span></td>
<td><span data-ttu-id="718da-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-932">Electricity</span></span></td>
<td><span data-ttu-id="718da-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-933">Variable cost</span></span></td>
<td><span data-ttu-id="718da-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="718da-934">2,507.09</span></span></td>
<td><span data-ttu-id="718da-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="718da-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-936">Prod 2</span></span></td>
<td><span data-ttu-id="718da-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="718da-937">Product 2</span></span></td>
<td><span data-ttu-id="718da-938">10001</span><span class="sxs-lookup"><span data-stu-id="718da-938">10001</span></span></td>
<td><span data-ttu-id="718da-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-939">Electricity</span></span></td>
<td><span data-ttu-id="718da-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-940">Variable cost</span></span></td>
<td><span data-ttu-id="718da-941">470.08</span><span class="sxs-lookup"><span data-stu-id="718da-941">470.08</span></span></td>
<td><span data-ttu-id="718da-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="718da-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="718da-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="718da-943">Conclusion</span></span>
<span data-ttu-id="718da-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="718da-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="718da-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="718da-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="718da-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="718da-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="718da-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="718da-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="718da-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="718da-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="718da-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="718da-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="718da-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="718da-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="718da-951">CC099</span><span class="sxs-lookup"><span data-stu-id="718da-951">CC099</span></span></th>
<th><span data-ttu-id="718da-952">CC001</span><span class="sxs-lookup"><span data-stu-id="718da-952">CC001</span></span></th>
<th><span data-ttu-id="718da-953">CC002</span><span class="sxs-lookup"><span data-stu-id="718da-953">CC002</span></span></th>
<th><span data-ttu-id="718da-954">CC003</span><span class="sxs-lookup"><span data-stu-id="718da-954">CC003</span></span></th>
<th><span data-ttu-id="718da-955">CC004</span><span class="sxs-lookup"><span data-stu-id="718da-955">CC004</span></span></th>
<th><span data-ttu-id="718da-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="718da-956">Proj 1</span></span></th>
<th><span data-ttu-id="718da-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="718da-957">Proj 2</span></span></th>
<th><span data-ttu-id="718da-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="718da-958">Prod 1</span></span></th>
<th><span data-ttu-id="718da-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="718da-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="718da-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="718da-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="718da-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="718da-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="718da-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="718da-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="718da-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-971">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="718da-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="718da-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-973">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-974">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-975">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-976">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-977">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="718da-978">776.36</span><span class="sxs-lookup"><span data-stu-id="718da-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-979">223.64</span><span class="sxs-lookup"><span data-stu-id="718da-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="718da-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="718da-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-982">000</span><span class="sxs-lookup"><span data-stu-id="718da-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-983">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-984">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-985">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-986">0,00</span><span class="sxs-lookup"><span data-stu-id="718da-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-987">30,00</span><span class="sxs-lookup"><span data-stu-id="718da-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-988">10,00</span><span class="sxs-lookup"><span data-stu-id="718da-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="718da-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="718da-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="718da-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="718da-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="718da-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="718da-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="718da-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="718da-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="718da-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="718da-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="718da-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="718da-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="718da-996">Zie [Beleid voor totalisering van kosten en overheadberekening](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="718da-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



