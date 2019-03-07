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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "335112"
---
# <a name="overhead-calculation"></a><span data-ttu-id="f6c86-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="f6c86-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6c86-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="f6c86-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="f6c86-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="f6c86-105">Term definition</span></span>
---------------

<span data-ttu-id="f6c86-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="f6c86-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="f6c86-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="f6c86-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="f6c86-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="f6c86-109">Huur</span><span class="sxs-lookup"><span data-stu-id="f6c86-109">Rent</span></span>
-   <span data-ttu-id="f6c86-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-110">Electricity</span></span>
-   <span data-ttu-id="f6c86-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="f6c86-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="f6c86-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="f6c86-112">Overhead calculation overview</span></span>
<span data-ttu-id="f6c86-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f6c86-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="f6c86-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="f6c86-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="f6c86-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="f6c86-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="f6c86-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="f6c86-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="f6c86-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="f6c86-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="f6c86-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="f6c86-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="f6c86-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="f6c86-119">Version type</span></span>
-   <span data-ttu-id="f6c86-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="f6c86-120">Date and time</span></span>
-   <span data-ttu-id="f6c86-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="f6c86-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="f6c86-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="f6c86-122">Fiscal year</span></span>
-   <span data-ttu-id="f6c86-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="f6c86-123">Fiscal period</span></span>

<span data-ttu-id="f6c86-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f6c86-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="f6c86-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="f6c86-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="f6c86-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f6c86-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="f6c86-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="f6c86-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="f6c86-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="f6c86-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="f6c86-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="f6c86-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="f6c86-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="f6c86-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="f6c86-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="f6c86-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="f6c86-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="f6c86-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="f6c86-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="f6c86-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="f6c86-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="f6c86-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="f6c86-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="f6c86-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="f6c86-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="f6c86-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f6c86-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="f6c86-140">Main account</span></span></th>
<th><span data-ttu-id="f6c86-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="f6c86-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="f6c86-143">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-143">CC099</span></span></td>
<td><span data-ttu-id="f6c86-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-144">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-145">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-145">10001</span></span></td>
<td><span data-ttu-id="f6c86-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-146">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="f6c86-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="f6c86-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="f6c86-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="f6c86-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="f6c86-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="f6c86-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="f6c86-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="f6c86-151">Define the cost behavior rule</span></span>

<span data-ttu-id="f6c86-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="f6c86-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="f6c86-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="f6c86-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="f6c86-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="f6c86-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="f6c86-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="f6c86-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="f6c86-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="f6c86-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="f6c86-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="f6c86-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="f6c86-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="f6c86-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-160">Journal</span></span></th>
<th><span data-ttu-id="f6c86-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f6c86-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="f6c86-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f6c86-163">Versie</span><span class="sxs-lookup"><span data-stu-id="f6c86-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-164">00001</span><span class="sxs-lookup"><span data-stu-id="f6c86-164">00001</span></span></td>
<td><span data-ttu-id="f6c86-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="f6c86-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-166">Fiscal</span></span></td>
<td><span data-ttu-id="f6c86-167">2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-167">2017</span></span></td>
<td><span data-ttu-id="f6c86-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-168">Period 1</span></span></td>
<td><span data-ttu-id="f6c86-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f6c86-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="f6c86-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-173">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-174">Cost behavior</span></span></th>
<th><span data-ttu-id="f6c86-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="f6c86-177">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-177">CC099</span></span></td>
<td><span data-ttu-id="f6c86-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-178">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-179">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-179">10001</span></span></td>
<td><span data-ttu-id="f6c86-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-180">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="f6c86-181">Unclassified</span></span></td>
<td><span data-ttu-id="f6c86-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f6c86-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="f6c86-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-185">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-186">Cost behavior</span></span></th>
<th><span data-ttu-id="f6c86-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-187">Amount</span></span></th>
<th><span data-ttu-id="f6c86-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-189">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-189">CC099</span></span></td>
<td><span data-ttu-id="f6c86-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-190">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-191">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-191">10001</span></span></td>
<td><span data-ttu-id="f6c86-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-192">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="f6c86-193">Unclassified</span></span></td>
<td><span data-ttu-id="f6c86-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-194">10,000.00</span></span></td>
<td><span data-ttu-id="f6c86-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-196">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-196">CC099</span></span></td>
<td><span data-ttu-id="f6c86-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-197">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-198">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-198">10001</span></span></td>
<td><span data-ttu-id="f6c86-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-199">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="f6c86-200">Unclassified</span></span></td>
<td><span data-ttu-id="f6c86-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-201">-10,000.00</span></span></td>
<td><span data-ttu-id="f6c86-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-203">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-203">CC099</span></span></td>
<td><span data-ttu-id="f6c86-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-204">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-205">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-205">10001</span></span></td>
<td><span data-ttu-id="f6c86-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-206">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-207">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-208">1,000.00</span></span></td>
<td><span data-ttu-id="f6c86-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-210">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-210">CC099</span></span></td>
<td><span data-ttu-id="f6c86-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-211">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-212">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-212">10001</span></span></td>
<td><span data-ttu-id="f6c86-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-213">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-214">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-215">9,000.00</span></span></td>
<td><span data-ttu-id="f6c86-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f6c86-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="f6c86-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="f6c86-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="f6c86-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="f6c86-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="f6c86-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="f6c86-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="f6c86-221">Define the cost distribution rule</span></span>

<span data-ttu-id="f6c86-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="f6c86-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="f6c86-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="f6c86-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="f6c86-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="f6c86-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="f6c86-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="f6c86-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="f6c86-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="f6c86-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="f6c86-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-228">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="f6c86-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-230">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-230">CC001</span></span></td>
<td><span data-ttu-id="f6c86-231">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-231">HR</span></span></td>
<td><span data-ttu-id="f6c86-232">1.000</span><span class="sxs-lookup"><span data-stu-id="f6c86-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-233">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-233">CC002</span></span></td>
<td><span data-ttu-id="f6c86-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-234">Finance</span></span></td>
<td><span data-ttu-id="f6c86-235">6.000</span><span class="sxs-lookup"><span data-stu-id="f6c86-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-236">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-236">CC003</span></span></td>
<td><span data-ttu-id="f6c86-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-237">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-238">0</span><span class="sxs-lookup"><span data-stu-id="f6c86-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-240">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="f6c86-241">Magnitude</span></span></th>
<th><span data-ttu-id="f6c86-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="f6c86-242">Allocation factor</span></span></th>
<th><span data-ttu-id="f6c86-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-244">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-244">CC001</span></span></td>
<td><span data-ttu-id="f6c86-245">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-245">HR</span></span></td>
<td><span data-ttu-id="f6c86-246">1.000</span><span class="sxs-lookup"><span data-stu-id="f6c86-246">1,000</span></span></td>
<td><span data-ttu-id="f6c86-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f6c86-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f6c86-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-249">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-249">CC002</span></span></td>
<td><span data-ttu-id="f6c86-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-250">Finance</span></span></td>
<td><span data-ttu-id="f6c86-251">6.000</span><span class="sxs-lookup"><span data-stu-id="f6c86-251">6,000</span></span></td>
<td><span data-ttu-id="f6c86-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f6c86-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f6c86-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-254">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-254">CC003</span></span></td>
<td><span data-ttu-id="f6c86-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-255">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-256">0</span><span class="sxs-lookup"><span data-stu-id="f6c86-256">0</span></span></td>
<td><span data-ttu-id="f6c86-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f6c86-258">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="f6c86-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="f6c86-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-261">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-262">Formule</span><span class="sxs-lookup"><span data-stu-id="f6c86-262">Formula</span></span></th>
<th><span data-ttu-id="f6c86-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="f6c86-263">Magnitude</span></span></th>
<th><span data-ttu-id="f6c86-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="f6c86-264">Allocation factor</span></span></th>
<th><span data-ttu-id="f6c86-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-266">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-266">CC001</span></span></td>
<td><span data-ttu-id="f6c86-267">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-267">HR</span></span></td>
<td><span data-ttu-id="f6c86-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f6c86-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f6c86-269">1</span><span class="sxs-lookup"><span data-stu-id="f6c86-269">1</span></span></td>
<td><span data-ttu-id="f6c86-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f6c86-271">500,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-272">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-272">CC002</span></span></td>
<td><span data-ttu-id="f6c86-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-273">Finance</span></span></td>
<td><span data-ttu-id="f6c86-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f6c86-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f6c86-275">1</span><span class="sxs-lookup"><span data-stu-id="f6c86-275">1</span></span></td>
<td><span data-ttu-id="f6c86-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f6c86-277">500,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-278">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-278">CC003</span></span></td>
<td><span data-ttu-id="f6c86-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-279">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f6c86-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f6c86-281">0</span><span class="sxs-lookup"><span data-stu-id="f6c86-281">0</span></span></td>
<td><span data-ttu-id="f6c86-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f6c86-283">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f6c86-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-285">Journal</span></span></th>
<th><span data-ttu-id="f6c86-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f6c86-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="f6c86-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f6c86-288">Versie</span><span class="sxs-lookup"><span data-stu-id="f6c86-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-289">00002</span><span class="sxs-lookup"><span data-stu-id="f6c86-289">00002</span></span></td>
<td><span data-ttu-id="f6c86-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="f6c86-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="f6c86-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-291">Fiscal</span></span></td>
<td><span data-ttu-id="f6c86-292">2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-292">2017</span></span></td>
<td><span data-ttu-id="f6c86-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-293">Period 1</span></span></td>
<td><span data-ttu-id="f6c86-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f6c86-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="f6c86-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-298">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-299">Cost behavior</span></span></th>
<th><span data-ttu-id="f6c86-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-302">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-302">CC099</span></span></td>
<td><span data-ttu-id="f6c86-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-303">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-304">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-304">10001</span></span></td>
<td><span data-ttu-id="f6c86-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-305">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-306">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-309">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-309">CC099</span></span></td>
<td><span data-ttu-id="f6c86-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-310">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-311">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-311">10001</span></span></td>
<td><span data-ttu-id="f6c86-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-312">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-313">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f6c86-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="f6c86-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-317">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-318">Cost behavior</span></span></th>
<th><span data-ttu-id="f6c86-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-319">Amount</span></span></th>
<th><span data-ttu-id="f6c86-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-321">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-321">CC099</span></span></td>
<td><span data-ttu-id="f6c86-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-322">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-323">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-323">10001</span></span></td>
<td><span data-ttu-id="f6c86-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-324">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-325">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-326">-1,000.00</span></span></td>
<td><span data-ttu-id="f6c86-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-328">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-328">CC001</span></span></td>
<td><span data-ttu-id="f6c86-329">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-329">HR</span></span></td>
<td><span data-ttu-id="f6c86-330">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-330">10001</span></span></td>
<td><span data-ttu-id="f6c86-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-331">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-332">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-333">500,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-333">500.00</span></span></td>
<td><span data-ttu-id="f6c86-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-335">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-335">CC002</span></span></td>
<td><span data-ttu-id="f6c86-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-336">Finance</span></span></td>
<td><span data-ttu-id="f6c86-337">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-337">10001</span></span></td>
<td><span data-ttu-id="f6c86-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-338">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-339">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-340">500,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-340">500.00</span></span></td>
<td><span data-ttu-id="f6c86-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-342">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-342">CC099</span></span></td>
<td><span data-ttu-id="f6c86-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="f6c86-343">Default cost center</span></span></td>
<td><span data-ttu-id="f6c86-344">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-344">10001</span></span></td>
<td><span data-ttu-id="f6c86-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-345">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-346">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-347">-9,000.00</span></span></td>
<td><span data-ttu-id="f6c86-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-349">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-349">CC001</span></span></td>
<td><span data-ttu-id="f6c86-350">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-350">HR</span></span></td>
<td><span data-ttu-id="f6c86-351">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-351">10001</span></span></td>
<td><span data-ttu-id="f6c86-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-352">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-353">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f6c86-354">1,285.71</span></span></td>
<td><span data-ttu-id="f6c86-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-356">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-356">CC002</span></span></td>
<td><span data-ttu-id="f6c86-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-357">Finance</span></span></td>
<td><span data-ttu-id="f6c86-358">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-358">10001</span></span></td>
<td><span data-ttu-id="f6c86-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-359">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-360">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f6c86-361">7,714.29</span></span></td>
<td><span data-ttu-id="f6c86-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f6c86-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="f6c86-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="f6c86-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="f6c86-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="f6c86-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="f6c86-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="f6c86-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="f6c86-367">Define the overhead rate</span></span>

<span data-ttu-id="f6c86-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="f6c86-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-370">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-371">Uren</span><span class="sxs-lookup"><span data-stu-id="f6c86-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-372">Proj 1</span></span></td>
<td><span data-ttu-id="f6c86-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-373">Project 1</span></span></td>
<td><span data-ttu-id="f6c86-374">3</span><span class="sxs-lookup"><span data-stu-id="f6c86-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-375">Proj 2</span></span></td>
<td><span data-ttu-id="f6c86-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-376">Project 2</span></span></td>
<td><span data-ttu-id="f6c86-377">1</span><span class="sxs-lookup"><span data-stu-id="f6c86-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="f6c86-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-379">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-380">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-381">Cost behavior</span></span></th>
<th><span data-ttu-id="f6c86-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="f6c86-382">Units</span></span></th>
<th><span data-ttu-id="f6c86-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="f6c86-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-384">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-384">CC001</span></span></td>
<td><span data-ttu-id="f6c86-385">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-385">HR</span></span></td>
<td><span data-ttu-id="f6c86-386">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-386">10001</span></span></td>
<td><span data-ttu-id="f6c86-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-387">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-388">1</span><span class="sxs-lookup"><span data-stu-id="f6c86-388">1</span></span></td>
<td><span data-ttu-id="f6c86-389">10</span><span class="sxs-lookup"><span data-stu-id="f6c86-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="f6c86-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-391">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="f6c86-392">Magnitude</span></span></th>
<th><span data-ttu-id="f6c86-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-393">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="f6c86-394">Allocation factor</span></span></th>
<th><span data-ttu-id="f6c86-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-396">Proj 1</span></span></td>
<td><span data-ttu-id="f6c86-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-397">Project 1</span></span></td>
<td><span data-ttu-id="f6c86-398">3</span><span class="sxs-lookup"><span data-stu-id="f6c86-398">3</span></span></td>
<td><span data-ttu-id="f6c86-399">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-399">10001</span></span></td>
<td><span data-ttu-id="f6c86-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f6c86-401">30,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-402">Proj 2</span></span></td>
<td><span data-ttu-id="f6c86-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-403">Project 2</span></span></td>
<td><span data-ttu-id="f6c86-404">1</span><span class="sxs-lookup"><span data-stu-id="f6c86-404">1</span></span></td>
<td><span data-ttu-id="f6c86-405">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-405">10001</span></span></td>
<td><span data-ttu-id="f6c86-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f6c86-407">10,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f6c86-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-409">Journal</span></span></th>
<th><span data-ttu-id="f6c86-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f6c86-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="f6c86-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f6c86-412">Versie</span><span class="sxs-lookup"><span data-stu-id="f6c86-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-413">00003</span><span class="sxs-lookup"><span data-stu-id="f6c86-413">00003</span></span></td>
<td><span data-ttu-id="f6c86-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="f6c86-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="f6c86-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-415">Fiscal</span></span></td>
<td><span data-ttu-id="f6c86-416">2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-416">2017</span></span></td>
<td><span data-ttu-id="f6c86-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-417">Period 1</span></span></td>
<td><span data-ttu-id="f6c86-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="f6c86-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="f6c86-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-421">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="f6c86-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-424">Proj 1</span></span></td>
<td><span data-ttu-id="f6c86-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f6c86-426">3,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-428">Proj 2</span></span></td>
<td><span data-ttu-id="f6c86-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f6c86-430">1,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f6c86-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="f6c86-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-433">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-434">Cost behavior</span></span></th>
<th><span data-ttu-id="f6c86-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-435">Amount</span></span></th>
<th><span data-ttu-id="f6c86-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="f6c86-437">CC0001</span></span></td>
<td><span data-ttu-id="f6c86-438">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-438">HR</span></span></td>
<td><span data-ttu-id="f6c86-439">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-439">10001</span></span></td>
<td><span data-ttu-id="f6c86-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-440">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-441">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-442">-30.00</span></span></td>
<td><span data-ttu-id="f6c86-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-444">Proj 1</span></span></td>
<td><span data-ttu-id="f6c86-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f6c86-446">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-446">10001</span></span></td>
<td><span data-ttu-id="f6c86-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-447">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-448">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-449">30,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-449">30.00</span></span></td>
<td><span data-ttu-id="f6c86-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-451">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-451">CC001</span></span></td>
<td><span data-ttu-id="f6c86-452">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-452">HR</span></span></td>
<td><span data-ttu-id="f6c86-453">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-453">10001</span></span></td>
<td><span data-ttu-id="f6c86-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-454">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-455">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-456">-10.00</span></span></td>
<td><span data-ttu-id="f6c86-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-458">Proj 2</span></span></td>
<td><span data-ttu-id="f6c86-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f6c86-460">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-460">10001</span></span></td>
<td><span data-ttu-id="f6c86-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-461">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-462">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-463">10.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-463">10.00</span></span></td>
<td><span data-ttu-id="f6c86-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="f6c86-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="f6c86-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="f6c86-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="f6c86-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="f6c86-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="f6c86-468">Finance and Operations ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="f6c86-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="f6c86-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="f6c86-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="f6c86-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="f6c86-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="f6c86-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="f6c86-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="f6c86-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="f6c86-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="f6c86-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="f6c86-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="f6c86-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="f6c86-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="f6c86-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="f6c86-475">Define the cost allocation</span></span>

<span data-ttu-id="f6c86-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="f6c86-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="f6c86-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="f6c86-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-479">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="f6c86-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-481">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-481">CC002</span></span></td>
<td><span data-ttu-id="f6c86-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-482">Finance</span></span></td>
<td><span data-ttu-id="f6c86-483">35</span><span class="sxs-lookup"><span data-stu-id="f6c86-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-484">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-484">CC003</span></span></td>
<td><span data-ttu-id="f6c86-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-485">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-486">55</span><span class="sxs-lookup"><span data-stu-id="f6c86-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-487">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-487">CC004</span></span></td>
<td><span data-ttu-id="f6c86-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-488">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-489">10</span><span class="sxs-lookup"><span data-stu-id="f6c86-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="f6c86-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-492">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="f6c86-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-494">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-494">CC003</span></span></td>
<td><span data-ttu-id="f6c86-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-495">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-496">65</span><span class="sxs-lookup"><span data-stu-id="f6c86-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-497">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-497">CC004</span></span></td>
<td><span data-ttu-id="f6c86-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-498">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-499">35</span><span class="sxs-lookup"><span data-stu-id="f6c86-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="f6c86-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-502">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="f6c86-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-504">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-505">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-506">60</span><span class="sxs-lookup"><span data-stu-id="f6c86-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-507">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-508">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-509">20</span><span class="sxs-lookup"><span data-stu-id="f6c86-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="f6c86-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-512">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="f6c86-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-514">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-515">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-516">80</span><span class="sxs-lookup"><span data-stu-id="f6c86-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-517">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-518">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-519">15</span><span class="sxs-lookup"><span data-stu-id="f6c86-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f6c86-520">In Finance and Operations kunnen statistische metingen, zoals de productie-uren die een product verbruikt, worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="f6c86-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="f6c86-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f6c86-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="f6c86-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="f6c86-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-523">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="f6c86-524">Magnitude</span></span></th>
<th><span data-ttu-id="f6c86-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="f6c86-525">Allocation factor</span></span></th>
<th><span data-ttu-id="f6c86-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-526">Amount</span></span></th>
<th><span data-ttu-id="f6c86-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-528">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-528">CC002</span></span></td>
<td><span data-ttu-id="f6c86-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-529">Finance</span></span></td>
<td><span data-ttu-id="f6c86-530">35</span><span class="sxs-lookup"><span data-stu-id="f6c86-530">35</span></span></td>
<td><span data-ttu-id="f6c86-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f6c86-532">175.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-532">175.00</span></span></td>
<td><span data-ttu-id="f6c86-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-534">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-534">CC003</span></span></td>
<td><span data-ttu-id="f6c86-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-535">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-536">55</span><span class="sxs-lookup"><span data-stu-id="f6c86-536">55</span></span></td>
<td><span data-ttu-id="f6c86-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f6c86-538">275.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-538">275.00</span></span></td>
<td><span data-ttu-id="f6c86-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-540">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-540">CC004</span></span></td>
<td><span data-ttu-id="f6c86-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-541">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-542">10</span><span class="sxs-lookup"><span data-stu-id="f6c86-542">10</span></span></td>
<td><span data-ttu-id="f6c86-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f6c86-544">50,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-544">50.00</span></span></td>
<td><span data-ttu-id="f6c86-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-546">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-546">CC002</span></span></td>
<td><span data-ttu-id="f6c86-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-547">Finance</span></span></td>
<td><span data-ttu-id="f6c86-548">35</span><span class="sxs-lookup"><span data-stu-id="f6c86-548">35</span></span></td>
<td><span data-ttu-id="f6c86-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="f6c86-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f6c86-550">436.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-550">436.00</span></span></td>
<td><span data-ttu-id="f6c86-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-552">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-552">CC003</span></span></td>
<td><span data-ttu-id="f6c86-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-553">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-554">55</span><span class="sxs-lookup"><span data-stu-id="f6c86-554">55</span></span></td>
<td><span data-ttu-id="f6c86-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="f6c86-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f6c86-556">685.14</span><span class="sxs-lookup"><span data-stu-id="f6c86-556">685.14</span></span></td>
<td><span data-ttu-id="f6c86-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-558">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-558">CC004</span></span></td>
<td><span data-ttu-id="f6c86-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-559">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-560">10</span><span class="sxs-lookup"><span data-stu-id="f6c86-560">10</span></span></td>
<td><span data-ttu-id="f6c86-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="f6c86-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f6c86-562">124.57</span><span class="sxs-lookup"><span data-stu-id="f6c86-562">124.57</span></span></td>
<td><span data-ttu-id="f6c86-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="f6c86-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-565">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="f6c86-566">Magnitude</span></span></th>
<th><span data-ttu-id="f6c86-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="f6c86-567">Allocation factor</span></span></th>
<th><span data-ttu-id="f6c86-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-568">Amount</span></span></th>
<th><span data-ttu-id="f6c86-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-570">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-570">CC003</span></span></td>
<td><span data-ttu-id="f6c86-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-571">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-572">65</span><span class="sxs-lookup"><span data-stu-id="f6c86-572">65</span></span></td>
<td><span data-ttu-id="f6c86-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="f6c86-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f6c86-574">438.75</span><span class="sxs-lookup"><span data-stu-id="f6c86-574">438.75</span></span></td>
<td><span data-ttu-id="f6c86-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-576">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-576">CC004</span></span></td>
<td><span data-ttu-id="f6c86-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-577">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-578">35</span><span class="sxs-lookup"><span data-stu-id="f6c86-578">35</span></span></td>
<td><span data-ttu-id="f6c86-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="f6c86-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f6c86-580">236.25</span><span class="sxs-lookup"><span data-stu-id="f6c86-580">236.25</span></span></td>
<td><span data-ttu-id="f6c86-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-582">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-582">CC003</span></span></td>
<td><span data-ttu-id="f6c86-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-583">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-584">65</span><span class="sxs-lookup"><span data-stu-id="f6c86-584">65</span></span></td>
<td><span data-ttu-id="f6c86-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="f6c86-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f6c86-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f6c86-586">5,297.69</span></span></td>
<td><span data-ttu-id="f6c86-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-588">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-588">CC004</span></span></td>
<td><span data-ttu-id="f6c86-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-589">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-590">35</span><span class="sxs-lookup"><span data-stu-id="f6c86-590">35</span></span></td>
<td><span data-ttu-id="f6c86-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="f6c86-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f6c86-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f6c86-592">2,852.60</span></span></td>
<td><span data-ttu-id="f6c86-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="f6c86-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-595">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="f6c86-596">Magnitude</span></span></th>
<th><span data-ttu-id="f6c86-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="f6c86-597">Allocation factor</span></span></th>
<th><span data-ttu-id="f6c86-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-598">Amount</span></span></th>
<th><span data-ttu-id="f6c86-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-600">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-601">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-602">60</span><span class="sxs-lookup"><span data-stu-id="f6c86-602">60</span></span></td>
<td><span data-ttu-id="f6c86-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="f6c86-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f6c86-604">535.31</span><span class="sxs-lookup"><span data-stu-id="f6c86-604">535.31</span></span></td>
<td><span data-ttu-id="f6c86-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-606">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-607">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-608">20</span><span class="sxs-lookup"><span data-stu-id="f6c86-608">20</span></span></td>
<td><span data-ttu-id="f6c86-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="f6c86-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f6c86-610">178.44</span><span class="sxs-lookup"><span data-stu-id="f6c86-610">178.44</span></span></td>
<td><span data-ttu-id="f6c86-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-612">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-613">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-614">60</span><span class="sxs-lookup"><span data-stu-id="f6c86-614">60</span></span></td>
<td><span data-ttu-id="f6c86-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="f6c86-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f6c86-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f6c86-616">4,487.12</span></span></td>
<td><span data-ttu-id="f6c86-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-618">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-619">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-620">20</span><span class="sxs-lookup"><span data-stu-id="f6c86-620">20</span></span></td>
<td><span data-ttu-id="f6c86-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="f6c86-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f6c86-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f6c86-622">1,495.71</span></span></td>
<td><span data-ttu-id="f6c86-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6c86-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="f6c86-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-625">Cost object</span></span></th>
<th><span data-ttu-id="f6c86-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="f6c86-626">Magnitude</span></span></th>
<th><span data-ttu-id="f6c86-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="f6c86-627">Allocation factor</span></span></th>
<th><span data-ttu-id="f6c86-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-628">Amount</span></span></th>
<th><span data-ttu-id="f6c86-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-630">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-631">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-632">80</span><span class="sxs-lookup"><span data-stu-id="f6c86-632">80</span></span></td>
<td><span data-ttu-id="f6c86-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="f6c86-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f6c86-634">241.05</span><span class="sxs-lookup"><span data-stu-id="f6c86-634">241.05</span></span></td>
<td><span data-ttu-id="f6c86-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-636">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-637">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-638">15</span><span class="sxs-lookup"><span data-stu-id="f6c86-638">15</span></span></td>
<td><span data-ttu-id="f6c86-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="f6c86-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f6c86-640">45.20</span><span class="sxs-lookup"><span data-stu-id="f6c86-640">45.20</span></span></td>
<td><span data-ttu-id="f6c86-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-642">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-643">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-644">80</span><span class="sxs-lookup"><span data-stu-id="f6c86-644">80</span></span></td>
<td><span data-ttu-id="f6c86-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="f6c86-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f6c86-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f6c86-646">2,507.09</span></span></td>
<td><span data-ttu-id="f6c86-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-648">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-649">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-650">15</span><span class="sxs-lookup"><span data-stu-id="f6c86-650">15</span></span></td>
<td><span data-ttu-id="f6c86-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="f6c86-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f6c86-652">470.08</span><span class="sxs-lookup"><span data-stu-id="f6c86-652">470.08</span></span></td>
<td><span data-ttu-id="f6c86-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f6c86-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="f6c86-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-655">Journal</span></span></th>
<th><span data-ttu-id="f6c86-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f6c86-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="f6c86-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f6c86-658">Versie</span><span class="sxs-lookup"><span data-stu-id="f6c86-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-659">00004</span><span class="sxs-lookup"><span data-stu-id="f6c86-659">00004</span></span></td>
<td><span data-ttu-id="f6c86-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="f6c86-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-661">Fiscal</span></span></td>
<td><span data-ttu-id="f6c86-662">2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-662">2017</span></span></td>
<td><span data-ttu-id="f6c86-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-663">Period 1</span></span></td>
<td><span data-ttu-id="f6c86-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="f6c86-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="f6c86-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6c86-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-668">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-669">Cost behavior</span></span></th>
<th><span data-ttu-id="f6c86-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-672">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-672">CC001</span></span></td>
<td><span data-ttu-id="f6c86-673">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-673">HR</span></span></td>
<td><span data-ttu-id="f6c86-674">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-674">10001</span></span></td>
<td><span data-ttu-id="f6c86-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-675">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-676">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-677">500,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-679">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-679">CC001</span></span></td>
<td><span data-ttu-id="f6c86-680">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-680">HR</span></span></td>
<td><span data-ttu-id="f6c86-681">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-681">10001</span></span></td>
<td><span data-ttu-id="f6c86-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-682">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-683">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="f6c86-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-686">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-686">CC002</span></span></td>
<td><span data-ttu-id="f6c86-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-687">Finance</span></span></td>
<td><span data-ttu-id="f6c86-688">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-688">10001</span></span></td>
<td><span data-ttu-id="f6c86-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-689">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-690">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-691">675.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-693">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-693">CC002</span></span></td>
<td><span data-ttu-id="f6c86-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-694">Finance</span></span></td>
<td><span data-ttu-id="f6c86-695">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-695">10001</span></span></td>
<td><span data-ttu-id="f6c86-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-696">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-697">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="f6c86-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-700">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-700">CC003</span></span></td>
<td><span data-ttu-id="f6c86-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-701">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-702">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-702">10001</span></span></td>
<td><span data-ttu-id="f6c86-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-703">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-704">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-705">713.75</span><span class="sxs-lookup"><span data-stu-id="f6c86-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-707">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-707">CC003</span></span></td>
<td><span data-ttu-id="f6c86-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-708">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-709">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-709">10001</span></span></td>
<td><span data-ttu-id="f6c86-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-710">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-711">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="f6c86-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-714">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-714">CC003</span></span></td>
<td><span data-ttu-id="f6c86-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-715">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-716">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-716">10001</span></span></td>
<td><span data-ttu-id="f6c86-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-717">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-718">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-719">286.25</span><span class="sxs-lookup"><span data-stu-id="f6c86-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-721">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-721">CC003</span></span></td>
<td><span data-ttu-id="f6c86-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-722">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-723">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-723">10001</span></span></td>
<td><span data-ttu-id="f6c86-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-724">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-725">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="f6c86-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-728">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-729">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-730">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-730">10001</span></span></td>
<td><span data-ttu-id="f6c86-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-731">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-732">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-733">776.36</span><span class="sxs-lookup"><span data-stu-id="f6c86-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-735">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-736">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-737">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-737">10001</span></span></td>
<td><span data-ttu-id="f6c86-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-738">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-739">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f6c86-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-742">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-743">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-744">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-744">10001</span></span></td>
<td><span data-ttu-id="f6c86-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-745">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-746">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-747">223.64</span><span class="sxs-lookup"><span data-stu-id="f6c86-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6c86-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-749">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-750">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-751">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-751">10001</span></span></td>
<td><span data-ttu-id="f6c86-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-752">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-753">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f6c86-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f6c86-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="f6c86-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6c86-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6c86-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-757">Cost element</span></span></th>
<th><span data-ttu-id="f6c86-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-758">Cost behavior</span></span></th>
<th><span data-ttu-id="f6c86-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f6c86-759">Amount</span></span></th>
<th><span data-ttu-id="f6c86-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="f6c86-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6c86-761">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-761">CC001</span></span></td>
<td><span data-ttu-id="f6c86-762">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-762">HR</span></span></td>
<td><span data-ttu-id="f6c86-763">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-763">10001</span></span></td>
<td><span data-ttu-id="f6c86-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-764">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-765">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-766">-500.00</span></span></td>
<td><span data-ttu-id="f6c86-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-768">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-768">CC002</span></span></td>
<td><span data-ttu-id="f6c86-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-769">Finance</span></span></td>
<td><span data-ttu-id="f6c86-770">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-770">10001</span></span></td>
<td><span data-ttu-id="f6c86-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-771">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-772">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-773">175.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-773">175.00</span></span></td>
<td><span data-ttu-id="f6c86-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-775">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-775">CC003</span></span></td>
<td><span data-ttu-id="f6c86-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-776">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-777">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-777">10001</span></span></td>
<td><span data-ttu-id="f6c86-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-778">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-779">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-780">275.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-780">275.00</span></span></td>
<td><span data-ttu-id="f6c86-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-782">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-782">CC004</span></span></td>
<td><span data-ttu-id="f6c86-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-783">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-784">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-784">10001</span></span></td>
<td><span data-ttu-id="f6c86-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-785">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-786">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-787">50,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-787">50,00</span></span></td>
<td><span data-ttu-id="f6c86-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-789">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-789">CC001</span></span></td>
<td><span data-ttu-id="f6c86-790">HR</span><span class="sxs-lookup"><span data-stu-id="f6c86-790">HR</span></span></td>
<td><span data-ttu-id="f6c86-791">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-791">10001</span></span></td>
<td><span data-ttu-id="f6c86-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-792">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-793">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="f6c86-794">-1,245.71</span></span></td>
<td><span data-ttu-id="f6c86-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-796">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-796">CC002</span></span></td>
<td><span data-ttu-id="f6c86-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-797">Finance</span></span></td>
<td><span data-ttu-id="f6c86-798">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-798">10001</span></span></td>
<td><span data-ttu-id="f6c86-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-799">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-800">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-801">436.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-801">436.00</span></span></td>
<td><span data-ttu-id="f6c86-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-803">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-803">CC003</span></span></td>
<td><span data-ttu-id="f6c86-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-804">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-805">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-805">10001</span></span></td>
<td><span data-ttu-id="f6c86-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-806">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-807">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-808">685.14</span><span class="sxs-lookup"><span data-stu-id="f6c86-808">685.14</span></span></td>
<td><span data-ttu-id="f6c86-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-810">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-810">CC004</span></span></td>
<td><span data-ttu-id="f6c86-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-811">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-812">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-812">10001</span></span></td>
<td><span data-ttu-id="f6c86-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-813">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-814">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-815">124.57</span><span class="sxs-lookup"><span data-stu-id="f6c86-815">124.57</span></span></td>
<td><span data-ttu-id="f6c86-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-817">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-817">CC002</span></span></td>
<td><span data-ttu-id="f6c86-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-818">Finance</span></span></td>
<td><span data-ttu-id="f6c86-819">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-819">10001</span></span></td>
<td><span data-ttu-id="f6c86-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-820">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-821">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="f6c86-822">-675.00</span></span></td>
<td><span data-ttu-id="f6c86-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-824">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-824">CC003</span></span></td>
<td><span data-ttu-id="f6c86-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-825">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-826">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-826">10001</span></span></td>
<td><span data-ttu-id="f6c86-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-827">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-828">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-829">438.75</span><span class="sxs-lookup"><span data-stu-id="f6c86-829">438.75</span></span></td>
<td><span data-ttu-id="f6c86-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-831">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-831">CC004</span></span></td>
<td><span data-ttu-id="f6c86-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-832">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-833">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-833">10001</span></span></td>
<td><span data-ttu-id="f6c86-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-834">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-835">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-836">236.25</span><span class="sxs-lookup"><span data-stu-id="f6c86-836">236.25</span></span></td>
<td><span data-ttu-id="f6c86-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-838">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-838">CC002</span></span></td>
<td><span data-ttu-id="f6c86-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="f6c86-839">Finance</span></span></td>
<td><span data-ttu-id="f6c86-840">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-840">10001</span></span></td>
<td><span data-ttu-id="f6c86-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-841">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-842">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="f6c86-843">-8,150.29</span></span></td>
<td><span data-ttu-id="f6c86-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-845">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-845">CC003</span></span></td>
<td><span data-ttu-id="f6c86-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-846">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-847">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-847">10001</span></span></td>
<td><span data-ttu-id="f6c86-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-848">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-849">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f6c86-850">5,297.69</span></span></td>
<td><span data-ttu-id="f6c86-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-852">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-852">CC004</span></span></td>
<td><span data-ttu-id="f6c86-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="f6c86-853">Packaging</span></span></td>
<td><span data-ttu-id="f6c86-854">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-854">10001</span></span></td>
<td><span data-ttu-id="f6c86-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-855">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-856">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f6c86-857">2,852.60</span></span></td>
<td><span data-ttu-id="f6c86-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-859">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-859">CC003</span></span></td>
<td><span data-ttu-id="f6c86-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-860">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-861">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-861">10001</span></span></td>
<td><span data-ttu-id="f6c86-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-862">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-863">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="f6c86-864">-713.75</span></span></td>
<td><span data-ttu-id="f6c86-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-866">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-867">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-868">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-868">10001</span></span></td>
<td><span data-ttu-id="f6c86-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-869">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-870">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-871">535.31</span><span class="sxs-lookup"><span data-stu-id="f6c86-871">535.31</span></span></td>
<td><span data-ttu-id="f6c86-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-873">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-874">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-875">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-875">10001</span></span></td>
<td><span data-ttu-id="f6c86-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-876">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-877">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-878">178.44</span><span class="sxs-lookup"><span data-stu-id="f6c86-878">178.44</span></span></td>
<td><span data-ttu-id="f6c86-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-880">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-880">CC003</span></span></td>
<td><span data-ttu-id="f6c86-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-881">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-882">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-882">10001</span></span></td>
<td><span data-ttu-id="f6c86-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-883">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-884">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="f6c86-885">-5,982.83</span></span></td>
<td><span data-ttu-id="f6c86-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-887">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-888">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-889">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-889">10001</span></span></td>
<td><span data-ttu-id="f6c86-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-890">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-891">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f6c86-892">4,487.12</span></span></td>
<td><span data-ttu-id="f6c86-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-894">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-895">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-896">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-896">10001</span></span></td>
<td><span data-ttu-id="f6c86-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-897">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-898">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f6c86-899">1,495.71</span></span></td>
<td><span data-ttu-id="f6c86-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-901">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-901">CC003</span></span></td>
<td><span data-ttu-id="f6c86-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-902">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-903">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-903">10001</span></span></td>
<td><span data-ttu-id="f6c86-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-904">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-905">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="f6c86-906">-286.25</span></span></td>
<td><span data-ttu-id="f6c86-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-908">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-909">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-910">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-910">10001</span></span></td>
<td><span data-ttu-id="f6c86-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-911">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-912">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-913">241.05</span><span class="sxs-lookup"><span data-stu-id="f6c86-913">241.05</span></span></td>
<td><span data-ttu-id="f6c86-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-915">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-916">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-917">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-917">10001</span></span></td>
<td><span data-ttu-id="f6c86-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-918">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-919">Fixed cost</span></span></td>
<td><span data-ttu-id="f6c86-920">45.20</span><span class="sxs-lookup"><span data-stu-id="f6c86-920">45.20</span></span></td>
<td><span data-ttu-id="f6c86-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-922">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-922">CC003</span></span></td>
<td><span data-ttu-id="f6c86-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="f6c86-923">Assembly</span></span></td>
<td><span data-ttu-id="f6c86-924">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-924">10001</span></span></td>
<td><span data-ttu-id="f6c86-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-925">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-926">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="f6c86-927">-2,977.17</span></span></td>
<td><span data-ttu-id="f6c86-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-929">Prod 1</span></span></td>
<td><span data-ttu-id="f6c86-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-930">Product 1</span></span></td>
<td><span data-ttu-id="f6c86-931">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-931">10001</span></span></td>
<td><span data-ttu-id="f6c86-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-932">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-933">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f6c86-934">2,507.09</span></span></td>
<td><span data-ttu-id="f6c86-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6c86-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-936">Prod 2</span></span></td>
<td><span data-ttu-id="f6c86-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-937">Product 2</span></span></td>
<td><span data-ttu-id="f6c86-938">10001</span><span class="sxs-lookup"><span data-stu-id="f6c86-938">10001</span></span></td>
<td><span data-ttu-id="f6c86-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-939">Electricity</span></span></td>
<td><span data-ttu-id="f6c86-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-940">Variable cost</span></span></td>
<td><span data-ttu-id="f6c86-941">470.08</span><span class="sxs-lookup"><span data-stu-id="f6c86-941">470.08</span></span></td>
<td><span data-ttu-id="f6c86-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="f6c86-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="f6c86-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="f6c86-943">Conclusion</span></span>
<span data-ttu-id="f6c86-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="f6c86-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="f6c86-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f6c86-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="f6c86-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f6c86-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="f6c86-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="f6c86-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="f6c86-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="f6c86-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="f6c86-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="f6c86-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="f6c86-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f6c86-951">CC099</span><span class="sxs-lookup"><span data-stu-id="f6c86-951">CC099</span></span></th>
<th><span data-ttu-id="f6c86-952">CC001</span><span class="sxs-lookup"><span data-stu-id="f6c86-952">CC001</span></span></th>
<th><span data-ttu-id="f6c86-953">CC002</span><span class="sxs-lookup"><span data-stu-id="f6c86-953">CC002</span></span></th>
<th><span data-ttu-id="f6c86-954">CC003</span><span class="sxs-lookup"><span data-stu-id="f6c86-954">CC003</span></span></th>
<th><span data-ttu-id="f6c86-955">CC004</span><span class="sxs-lookup"><span data-stu-id="f6c86-955">CC004</span></span></th>
<th><span data-ttu-id="f6c86-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-956">Proj 1</span></span></th>
<th><span data-ttu-id="f6c86-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-957">Proj 2</span></span></th>
<th><span data-ttu-id="f6c86-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f6c86-958">Prod 1</span></span></th>
<th><span data-ttu-id="f6c86-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f6c86-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="f6c86-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="f6c86-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="f6c86-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="f6c86-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-971">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="f6c86-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-973">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-974">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-975">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-976">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-977">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-978">776.36</span><span class="sxs-lookup"><span data-stu-id="f6c86-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-979">223.64</span><span class="sxs-lookup"><span data-stu-id="f6c86-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="f6c86-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="f6c86-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-982">000</span><span class="sxs-lookup"><span data-stu-id="f6c86-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-983">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-984">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-985">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-986">0,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-987">30,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-988">10,00</span><span class="sxs-lookup"><span data-stu-id="f6c86-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f6c86-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f6c86-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6c86-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6c86-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f6c86-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="f6c86-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="f6c86-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="f6c86-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="f6c86-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="f6c86-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="f6c86-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="f6c86-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="f6c86-996">Zie [Kostentotalisatie](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f6c86-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



