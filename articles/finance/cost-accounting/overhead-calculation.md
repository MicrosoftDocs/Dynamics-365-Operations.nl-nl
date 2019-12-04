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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770799"
---
# <a name="overhead-calculation"></a><span data-ttu-id="4a5ae-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="4a5ae-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a5ae-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4a5ae-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="4a5ae-105">Term definition</span></span>
---------------

<span data-ttu-id="4a5ae-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4a5ae-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4a5ae-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="4a5ae-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4a5ae-109">Huur</span><span class="sxs-lookup"><span data-stu-id="4a5ae-109">Rent</span></span>
-   <span data-ttu-id="4a5ae-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-110">Electricity</span></span>
-   <span data-ttu-id="4a5ae-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="4a5ae-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4a5ae-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="4a5ae-112">Overhead calculation overview</span></span>
<span data-ttu-id="4a5ae-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4a5ae-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4a5ae-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4a5ae-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4a5ae-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4a5ae-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="4a5ae-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4a5ae-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="4a5ae-119">Version type</span></span>
-   <span data-ttu-id="4a5ae-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="4a5ae-120">Date and time</span></span>
-   <span data-ttu-id="4a5ae-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="4a5ae-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4a5ae-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="4a5ae-122">Fiscal year</span></span>
-   <span data-ttu-id="4a5ae-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="4a5ae-123">Fiscal period</span></span>

<span data-ttu-id="4a5ae-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4a5ae-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4a5ae-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4a5ae-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4a5ae-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4a5ae-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4a5ae-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4a5ae-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4a5ae-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="4a5ae-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4a5ae-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4a5ae-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4a5ae-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4a5ae-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4a5ae-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="4a5ae-140">Main account</span></span></th>
<th><span data-ttu-id="4a5ae-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="4a5ae-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-143">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-144">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-145">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-145">10001</span></span></td>
<td><span data-ttu-id="4a5ae-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-146">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4a5ae-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="4a5ae-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4a5ae-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4a5ae-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4a5ae-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4a5ae-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4a5ae-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4a5ae-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="4a5ae-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4a5ae-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="4a5ae-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4a5ae-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4a5ae-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="4a5ae-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4a5ae-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="4a5ae-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4a5ae-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-160">Journal</span></span></th>
<th><span data-ttu-id="4a5ae-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4a5ae-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4a5ae-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4a5ae-163">Versie</span><span class="sxs-lookup"><span data-stu-id="4a5ae-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-164">00001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-164">00001</span></span></td>
<td><span data-ttu-id="4a5ae-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4a5ae-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-166">Fiscal</span></span></td>
<td><span data-ttu-id="4a5ae-167">2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-167">2017</span></span></td>
<td><span data-ttu-id="4a5ae-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-168">Period 1</span></span></td>
<td><span data-ttu-id="4a5ae-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4a5ae-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-173">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4a5ae-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-177">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-178">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-179">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-179">10001</span></span></td>
<td><span data-ttu-id="4a5ae-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-180">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="4a5ae-181">Unclassified</span></span></td>
<td><span data-ttu-id="4a5ae-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4a5ae-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="4a5ae-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-185">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4a5ae-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-187">Amount</span></span></th>
<th><span data-ttu-id="4a5ae-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-189">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-190">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-191">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-191">10001</span></span></td>
<td><span data-ttu-id="4a5ae-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-192">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="4a5ae-193">Unclassified</span></span></td>
<td><span data-ttu-id="4a5ae-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-194">10,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-196">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-197">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-198">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-198">10001</span></span></td>
<td><span data-ttu-id="4a5ae-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-199">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="4a5ae-200">Unclassified</span></span></td>
<td><span data-ttu-id="4a5ae-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-203">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-204">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-205">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-205">10001</span></span></td>
<td><span data-ttu-id="4a5ae-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-206">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-208">1,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-210">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-211">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-212">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-212">10001</span></span></td>
<td><span data-ttu-id="4a5ae-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-213">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-214">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-215">9,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4a5ae-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="4a5ae-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4a5ae-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4a5ae-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4a5ae-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-221">Define the cost distribution rule</span></span>

<span data-ttu-id="4a5ae-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4a5ae-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4a5ae-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4a5ae-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="4a5ae-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4a5ae-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4a5ae-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-228">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="4a5ae-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-230">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-230">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-231">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-231">HR</span></span></td>
<td><span data-ttu-id="4a5ae-232">1.000</span><span class="sxs-lookup"><span data-stu-id="4a5ae-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-233">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-233">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-234">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-235">6.000</span><span class="sxs-lookup"><span data-stu-id="4a5ae-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-236">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-236">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-237">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-238">0</span><span class="sxs-lookup"><span data-stu-id="4a5ae-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-240">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4a5ae-241">Magnitude</span></span></th>
<th><span data-ttu-id="4a5ae-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4a5ae-242">Allocation factor</span></span></th>
<th><span data-ttu-id="4a5ae-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-244">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-244">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-245">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-245">HR</span></span></td>
<td><span data-ttu-id="4a5ae-246">1.000</span><span class="sxs-lookup"><span data-stu-id="4a5ae-246">1,000</span></span></td>
<td><span data-ttu-id="4a5ae-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-249">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-249">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-250">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-251">6.000</span><span class="sxs-lookup"><span data-stu-id="4a5ae-251">6,000</span></span></td>
<td><span data-ttu-id="4a5ae-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4a5ae-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-254">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-254">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-255">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-256">0</span><span class="sxs-lookup"><span data-stu-id="4a5ae-256">0</span></span></td>
<td><span data-ttu-id="4a5ae-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-258">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4a5ae-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-261">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-262">Formule</span><span class="sxs-lookup"><span data-stu-id="4a5ae-262">Formula</span></span></th>
<th><span data-ttu-id="4a5ae-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4a5ae-263">Magnitude</span></span></th>
<th><span data-ttu-id="4a5ae-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4a5ae-264">Allocation factor</span></span></th>
<th><span data-ttu-id="4a5ae-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-266">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-266">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-267">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-267">HR</span></span></td>
<td><span data-ttu-id="4a5ae-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4a5ae-269">1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-269">1</span></span></td>
<td><span data-ttu-id="4a5ae-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-271">500,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-272">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-272">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-273">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4a5ae-275">1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-275">1</span></span></td>
<td><span data-ttu-id="4a5ae-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-277">500,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-278">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-278">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-279">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4a5ae-281">0</span><span class="sxs-lookup"><span data-stu-id="4a5ae-281">0</span></span></td>
<td><span data-ttu-id="4a5ae-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-283">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4a5ae-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-285">Journal</span></span></th>
<th><span data-ttu-id="4a5ae-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4a5ae-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4a5ae-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4a5ae-288">Versie</span><span class="sxs-lookup"><span data-stu-id="4a5ae-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-289">00002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-289">00002</span></span></td>
<td><span data-ttu-id="4a5ae-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="4a5ae-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4a5ae-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-291">Fiscal</span></span></td>
<td><span data-ttu-id="4a5ae-292">2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-292">2017</span></span></td>
<td><span data-ttu-id="4a5ae-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-293">Period 1</span></span></td>
<td><span data-ttu-id="4a5ae-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4a5ae-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-298">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-299">Cost behavior</span></span></th>
<th><span data-ttu-id="4a5ae-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-302">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-302">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-303">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-304">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-304">10001</span></span></td>
<td><span data-ttu-id="4a5ae-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-305">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-306">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-309">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-309">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-310">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-311">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-311">10001</span></span></td>
<td><span data-ttu-id="4a5ae-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-312">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-313">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4a5ae-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="4a5ae-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-317">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-318">Cost behavior</span></span></th>
<th><span data-ttu-id="4a5ae-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-319">Amount</span></span></th>
<th><span data-ttu-id="4a5ae-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-321">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-321">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-322">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-323">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-323">10001</span></span></td>
<td><span data-ttu-id="4a5ae-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-324">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-325">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-326">-1,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-328">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-328">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-329">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-329">HR</span></span></td>
<td><span data-ttu-id="4a5ae-330">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-330">10001</span></span></td>
<td><span data-ttu-id="4a5ae-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-331">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-332">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-333">500,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-333">500.00</span></span></td>
<td><span data-ttu-id="4a5ae-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-335">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-335">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-336">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-337">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-337">10001</span></span></td>
<td><span data-ttu-id="4a5ae-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-338">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-339">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-340">500,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-340">500.00</span></span></td>
<td><span data-ttu-id="4a5ae-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-342">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-342">CC099</span></span></td>
<td><span data-ttu-id="4a5ae-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4a5ae-343">Default cost center</span></span></td>
<td><span data-ttu-id="4a5ae-344">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-344">10001</span></span></td>
<td><span data-ttu-id="4a5ae-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-345">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-346">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-347">-9,000.00</span></span></td>
<td><span data-ttu-id="4a5ae-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-349">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-349">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-350">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-350">HR</span></span></td>
<td><span data-ttu-id="4a5ae-351">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-351">10001</span></span></td>
<td><span data-ttu-id="4a5ae-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-352">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-353">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-354">1,285.71</span></span></td>
<td><span data-ttu-id="4a5ae-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-356">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-356">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-357">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-358">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-358">10001</span></span></td>
<td><span data-ttu-id="4a5ae-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-359">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-360">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4a5ae-361">7,714.29</span></span></td>
<td><span data-ttu-id="4a5ae-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4a5ae-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="4a5ae-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4a5ae-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4a5ae-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4a5ae-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-367">Define the overhead rate</span></span>

<span data-ttu-id="4a5ae-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4a5ae-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-370">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-371">Uren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-372">Proj 1</span></span></td>
<td><span data-ttu-id="4a5ae-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-373">Project 1</span></span></td>
<td><span data-ttu-id="4a5ae-374">3</span><span class="sxs-lookup"><span data-stu-id="4a5ae-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-375">Proj 2</span></span></td>
<td><span data-ttu-id="4a5ae-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-376">Project 2</span></span></td>
<td><span data-ttu-id="4a5ae-377">1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-379">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-380">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-381">Cost behavior</span></span></th>
<th><span data-ttu-id="4a5ae-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="4a5ae-382">Units</span></span></th>
<th><span data-ttu-id="4a5ae-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="4a5ae-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-384">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-384">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-385">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-385">HR</span></span></td>
<td><span data-ttu-id="4a5ae-386">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-386">10001</span></span></td>
<td><span data-ttu-id="4a5ae-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-387">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-388">1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-388">1</span></span></td>
<td><span data-ttu-id="4a5ae-389">10</span><span class="sxs-lookup"><span data-stu-id="4a5ae-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-391">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4a5ae-392">Magnitude</span></span></th>
<th><span data-ttu-id="4a5ae-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-393">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4a5ae-394">Allocation factor</span></span></th>
<th><span data-ttu-id="4a5ae-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-396">Proj 1</span></span></td>
<td><span data-ttu-id="4a5ae-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-397">Project 1</span></span></td>
<td><span data-ttu-id="4a5ae-398">3</span><span class="sxs-lookup"><span data-stu-id="4a5ae-398">3</span></span></td>
<td><span data-ttu-id="4a5ae-399">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-399">10001</span></span></td>
<td><span data-ttu-id="4a5ae-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4a5ae-401">30,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-402">Proj 2</span></span></td>
<td><span data-ttu-id="4a5ae-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-403">Project 2</span></span></td>
<td><span data-ttu-id="4a5ae-404">1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-404">1</span></span></td>
<td><span data-ttu-id="4a5ae-405">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-405">10001</span></span></td>
<td><span data-ttu-id="4a5ae-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4a5ae-407">10,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4a5ae-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-409">Journal</span></span></th>
<th><span data-ttu-id="4a5ae-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4a5ae-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4a5ae-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4a5ae-412">Versie</span><span class="sxs-lookup"><span data-stu-id="4a5ae-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-413">00003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-413">00003</span></span></td>
<td><span data-ttu-id="4a5ae-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="4a5ae-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4a5ae-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-415">Fiscal</span></span></td>
<td><span data-ttu-id="4a5ae-416">2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-416">2017</span></span></td>
<td><span data-ttu-id="4a5ae-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-417">Period 1</span></span></td>
<td><span data-ttu-id="4a5ae-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4a5ae-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-421">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4a5ae-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-424">Proj 1</span></span></td>
<td><span data-ttu-id="4a5ae-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4a5ae-426">3,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-428">Proj 2</span></span></td>
<td><span data-ttu-id="4a5ae-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4a5ae-430">1,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4a5ae-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="4a5ae-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-433">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-434">Cost behavior</span></span></th>
<th><span data-ttu-id="4a5ae-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-435">Amount</span></span></th>
<th><span data-ttu-id="4a5ae-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-437">CC0001</span></span></td>
<td><span data-ttu-id="4a5ae-438">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-438">HR</span></span></td>
<td><span data-ttu-id="4a5ae-439">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-439">10001</span></span></td>
<td><span data-ttu-id="4a5ae-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-440">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-441">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-442">-30.00</span></span></td>
<td><span data-ttu-id="4a5ae-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-444">Proj 1</span></span></td>
<td><span data-ttu-id="4a5ae-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4a5ae-446">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-446">10001</span></span></td>
<td><span data-ttu-id="4a5ae-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-447">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-448">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-449">30,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-449">30.00</span></span></td>
<td><span data-ttu-id="4a5ae-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-451">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-451">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-452">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-452">HR</span></span></td>
<td><span data-ttu-id="4a5ae-453">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-453">10001</span></span></td>
<td><span data-ttu-id="4a5ae-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-454">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-455">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-456">-10.00</span></span></td>
<td><span data-ttu-id="4a5ae-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-458">Proj 2</span></span></td>
<td><span data-ttu-id="4a5ae-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4a5ae-460">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-460">10001</span></span></td>
<td><span data-ttu-id="4a5ae-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-461">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-462">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-463">10.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-463">10.00</span></span></td>
<td><span data-ttu-id="4a5ae-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4a5ae-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="4a5ae-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4a5ae-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4a5ae-468">Finance ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="4a5ae-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4a5ae-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4a5ae-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4a5ae-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4a5ae-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4a5ae-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4a5ae-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-475">Define the cost allocation</span></span>

<span data-ttu-id="4a5ae-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4a5ae-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4a5ae-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-479">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="4a5ae-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-481">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-481">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-482">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-483">35</span><span class="sxs-lookup"><span data-stu-id="4a5ae-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-484">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-484">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-485">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-486">55</span><span class="sxs-lookup"><span data-stu-id="4a5ae-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-487">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-487">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-488">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-489">10</span><span class="sxs-lookup"><span data-stu-id="4a5ae-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4a5ae-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-492">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="4a5ae-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-494">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-494">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-495">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-496">65</span><span class="sxs-lookup"><span data-stu-id="4a5ae-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-497">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-497">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-498">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-499">35</span><span class="sxs-lookup"><span data-stu-id="4a5ae-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4a5ae-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-502">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-504">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-505">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-506">60</span><span class="sxs-lookup"><span data-stu-id="4a5ae-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-507">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-508">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-509">20</span><span class="sxs-lookup"><span data-stu-id="4a5ae-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4a5ae-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-512">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-514">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-515">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-516">80</span><span class="sxs-lookup"><span data-stu-id="4a5ae-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-517">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-518">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-519">15</span><span class="sxs-lookup"><span data-stu-id="4a5ae-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4a5ae-520">Statistische metingen, zoals de productie-uren die een product verbruikt, kunnen worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4a5ae-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="4a5ae-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="4a5ae-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-523">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4a5ae-524">Magnitude</span></span></th>
<th><span data-ttu-id="4a5ae-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4a5ae-525">Allocation factor</span></span></th>
<th><span data-ttu-id="4a5ae-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-526">Amount</span></span></th>
<th><span data-ttu-id="4a5ae-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-528">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-528">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-529">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-530">35</span><span class="sxs-lookup"><span data-stu-id="4a5ae-530">35</span></span></td>
<td><span data-ttu-id="4a5ae-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4a5ae-532">175.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-532">175.00</span></span></td>
<td><span data-ttu-id="4a5ae-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-534">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-534">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-535">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-536">55</span><span class="sxs-lookup"><span data-stu-id="4a5ae-536">55</span></span></td>
<td><span data-ttu-id="4a5ae-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4a5ae-538">275.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-538">275.00</span></span></td>
<td><span data-ttu-id="4a5ae-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-540">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-540">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-541">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-542">10</span><span class="sxs-lookup"><span data-stu-id="4a5ae-542">10</span></span></td>
<td><span data-ttu-id="4a5ae-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4a5ae-544">50,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-544">50.00</span></span></td>
<td><span data-ttu-id="4a5ae-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-546">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-546">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-547">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-548">35</span><span class="sxs-lookup"><span data-stu-id="4a5ae-548">35</span></span></td>
<td><span data-ttu-id="4a5ae-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4a5ae-550">436.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-550">436.00</span></span></td>
<td><span data-ttu-id="4a5ae-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-552">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-552">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-553">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-554">55</span><span class="sxs-lookup"><span data-stu-id="4a5ae-554">55</span></span></td>
<td><span data-ttu-id="4a5ae-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4a5ae-556">685.14</span><span class="sxs-lookup"><span data-stu-id="4a5ae-556">685.14</span></span></td>
<td><span data-ttu-id="4a5ae-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-558">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-558">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-559">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-560">10</span><span class="sxs-lookup"><span data-stu-id="4a5ae-560">10</span></span></td>
<td><span data-ttu-id="4a5ae-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4a5ae-562">124.57</span><span class="sxs-lookup"><span data-stu-id="4a5ae-562">124.57</span></span></td>
<td><span data-ttu-id="4a5ae-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="4a5ae-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-565">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4a5ae-566">Magnitude</span></span></th>
<th><span data-ttu-id="4a5ae-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4a5ae-567">Allocation factor</span></span></th>
<th><span data-ttu-id="4a5ae-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-568">Amount</span></span></th>
<th><span data-ttu-id="4a5ae-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-570">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-570">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-571">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-572">65</span><span class="sxs-lookup"><span data-stu-id="4a5ae-572">65</span></span></td>
<td><span data-ttu-id="4a5ae-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4a5ae-574">438.75</span><span class="sxs-lookup"><span data-stu-id="4a5ae-574">438.75</span></span></td>
<td><span data-ttu-id="4a5ae-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-576">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-576">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-577">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-578">35</span><span class="sxs-lookup"><span data-stu-id="4a5ae-578">35</span></span></td>
<td><span data-ttu-id="4a5ae-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4a5ae-580">236.25</span><span class="sxs-lookup"><span data-stu-id="4a5ae-580">236.25</span></span></td>
<td><span data-ttu-id="4a5ae-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-582">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-582">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-583">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-584">65</span><span class="sxs-lookup"><span data-stu-id="4a5ae-584">65</span></span></td>
<td><span data-ttu-id="4a5ae-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4a5ae-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4a5ae-586">5,297.69</span></span></td>
<td><span data-ttu-id="4a5ae-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-588">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-588">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-589">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-590">35</span><span class="sxs-lookup"><span data-stu-id="4a5ae-590">35</span></span></td>
<td><span data-ttu-id="4a5ae-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4a5ae-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4a5ae-592">2,852.60</span></span></td>
<td><span data-ttu-id="4a5ae-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="4a5ae-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-595">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4a5ae-596">Magnitude</span></span></th>
<th><span data-ttu-id="4a5ae-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4a5ae-597">Allocation factor</span></span></th>
<th><span data-ttu-id="4a5ae-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-598">Amount</span></span></th>
<th><span data-ttu-id="4a5ae-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-600">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-601">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-602">60</span><span class="sxs-lookup"><span data-stu-id="4a5ae-602">60</span></span></td>
<td><span data-ttu-id="4a5ae-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4a5ae-604">535.31</span><span class="sxs-lookup"><span data-stu-id="4a5ae-604">535.31</span></span></td>
<td><span data-ttu-id="4a5ae-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-606">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-607">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-608">20</span><span class="sxs-lookup"><span data-stu-id="4a5ae-608">20</span></span></td>
<td><span data-ttu-id="4a5ae-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4a5ae-610">178.44</span><span class="sxs-lookup"><span data-stu-id="4a5ae-610">178.44</span></span></td>
<td><span data-ttu-id="4a5ae-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-612">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-613">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-614">60</span><span class="sxs-lookup"><span data-stu-id="4a5ae-614">60</span></span></td>
<td><span data-ttu-id="4a5ae-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4a5ae-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4a5ae-616">4,487.12</span></span></td>
<td><span data-ttu-id="4a5ae-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-618">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-619">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-620">20</span><span class="sxs-lookup"><span data-stu-id="4a5ae-620">20</span></span></td>
<td><span data-ttu-id="4a5ae-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4a5ae-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-622">1,495.71</span></span></td>
<td><span data-ttu-id="4a5ae-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a5ae-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="4a5ae-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-625">Cost object</span></span></th>
<th><span data-ttu-id="4a5ae-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4a5ae-626">Magnitude</span></span></th>
<th><span data-ttu-id="4a5ae-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4a5ae-627">Allocation factor</span></span></th>
<th><span data-ttu-id="4a5ae-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-628">Amount</span></span></th>
<th><span data-ttu-id="4a5ae-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-630">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-631">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-632">80</span><span class="sxs-lookup"><span data-stu-id="4a5ae-632">80</span></span></td>
<td><span data-ttu-id="4a5ae-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4a5ae-634">241.05</span><span class="sxs-lookup"><span data-stu-id="4a5ae-634">241.05</span></span></td>
<td><span data-ttu-id="4a5ae-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-636">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-637">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-638">15</span><span class="sxs-lookup"><span data-stu-id="4a5ae-638">15</span></span></td>
<td><span data-ttu-id="4a5ae-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4a5ae-640">45.20</span><span class="sxs-lookup"><span data-stu-id="4a5ae-640">45.20</span></span></td>
<td><span data-ttu-id="4a5ae-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-642">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-643">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-644">80</span><span class="sxs-lookup"><span data-stu-id="4a5ae-644">80</span></span></td>
<td><span data-ttu-id="4a5ae-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4a5ae-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4a5ae-646">2,507.09</span></span></td>
<td><span data-ttu-id="4a5ae-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-648">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-649">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-650">15</span><span class="sxs-lookup"><span data-stu-id="4a5ae-650">15</span></span></td>
<td><span data-ttu-id="4a5ae-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4a5ae-652">470.08</span><span class="sxs-lookup"><span data-stu-id="4a5ae-652">470.08</span></span></td>
<td><span data-ttu-id="4a5ae-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4a5ae-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="4a5ae-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-655">Journal</span></span></th>
<th><span data-ttu-id="4a5ae-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4a5ae-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4a5ae-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4a5ae-658">Versie</span><span class="sxs-lookup"><span data-stu-id="4a5ae-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-659">00004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-659">00004</span></span></td>
<td><span data-ttu-id="4a5ae-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4a5ae-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-661">Fiscal</span></span></td>
<td><span data-ttu-id="4a5ae-662">2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-662">2017</span></span></td>
<td><span data-ttu-id="4a5ae-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-663">Period 1</span></span></td>
<td><span data-ttu-id="4a5ae-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4a5ae-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="4a5ae-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4a5ae-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-668">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-669">Cost behavior</span></span></th>
<th><span data-ttu-id="4a5ae-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-672">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-672">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-673">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-673">HR</span></span></td>
<td><span data-ttu-id="4a5ae-674">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-674">10001</span></span></td>
<td><span data-ttu-id="4a5ae-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-675">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-676">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-677">500,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-679">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-679">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-680">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-680">HR</span></span></td>
<td><span data-ttu-id="4a5ae-681">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-681">10001</span></span></td>
<td><span data-ttu-id="4a5ae-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-682">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-683">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-686">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-686">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-687">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-688">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-688">10001</span></span></td>
<td><span data-ttu-id="4a5ae-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-689">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-690">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-691">675.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-693">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-693">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-694">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-695">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-695">10001</span></span></td>
<td><span data-ttu-id="4a5ae-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-696">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-697">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4a5ae-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-700">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-700">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-701">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-702">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-702">10001</span></span></td>
<td><span data-ttu-id="4a5ae-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-703">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-704">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-705">713.75</span><span class="sxs-lookup"><span data-stu-id="4a5ae-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-707">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-707">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-708">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-709">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-709">10001</span></span></td>
<td><span data-ttu-id="4a5ae-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-710">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-711">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4a5ae-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-714">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-714">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-715">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-716">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-716">10001</span></span></td>
<td><span data-ttu-id="4a5ae-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-717">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-718">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-719">286.25</span><span class="sxs-lookup"><span data-stu-id="4a5ae-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-721">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-721">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-722">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-723">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-723">10001</span></span></td>
<td><span data-ttu-id="4a5ae-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-724">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-725">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4a5ae-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-728">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-729">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-730">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-730">10001</span></span></td>
<td><span data-ttu-id="4a5ae-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-731">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-732">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-733">776.36</span><span class="sxs-lookup"><span data-stu-id="4a5ae-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-735">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-736">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-737">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-737">10001</span></span></td>
<td><span data-ttu-id="4a5ae-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-738">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-739">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4a5ae-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-742">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-743">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-744">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-744">10001</span></span></td>
<td><span data-ttu-id="4a5ae-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-745">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-746">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-747">223.64</span><span class="sxs-lookup"><span data-stu-id="4a5ae-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="4a5ae-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-749">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-750">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-751">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-751">10001</span></span></td>
<td><span data-ttu-id="4a5ae-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-752">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-753">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4a5ae-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4a5ae-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="4a5ae-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4a5ae-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4a5ae-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-757">Cost element</span></span></th>
<th><span data-ttu-id="4a5ae-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-758">Cost behavior</span></span></th>
<th><span data-ttu-id="4a5ae-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4a5ae-759">Amount</span></span></th>
<th><span data-ttu-id="4a5ae-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4a5ae-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4a5ae-761">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-761">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-762">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-762">HR</span></span></td>
<td><span data-ttu-id="4a5ae-763">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-763">10001</span></span></td>
<td><span data-ttu-id="4a5ae-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-764">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-765">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-766">-500.00</span></span></td>
<td><span data-ttu-id="4a5ae-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-768">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-768">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-769">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-770">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-770">10001</span></span></td>
<td><span data-ttu-id="4a5ae-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-771">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-772">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-773">175.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-773">175.00</span></span></td>
<td><span data-ttu-id="4a5ae-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-775">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-775">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-776">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-777">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-777">10001</span></span></td>
<td><span data-ttu-id="4a5ae-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-778">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-779">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-780">275.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-780">275.00</span></span></td>
<td><span data-ttu-id="4a5ae-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-782">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-782">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-783">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-784">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-784">10001</span></span></td>
<td><span data-ttu-id="4a5ae-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-785">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-786">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-787">50,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-787">50,00</span></span></td>
<td><span data-ttu-id="4a5ae-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-789">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-789">CC001</span></span></td>
<td><span data-ttu-id="4a5ae-790">HR</span><span class="sxs-lookup"><span data-stu-id="4a5ae-790">HR</span></span></td>
<td><span data-ttu-id="4a5ae-791">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-791">10001</span></span></td>
<td><span data-ttu-id="4a5ae-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-792">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-793">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-794">-1,245.71</span></span></td>
<td><span data-ttu-id="4a5ae-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-796">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-796">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-797">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-798">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-798">10001</span></span></td>
<td><span data-ttu-id="4a5ae-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-799">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-800">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-801">436.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-801">436.00</span></span></td>
<td><span data-ttu-id="4a5ae-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-803">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-803">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-804">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-805">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-805">10001</span></span></td>
<td><span data-ttu-id="4a5ae-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-806">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-807">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-808">685.14</span><span class="sxs-lookup"><span data-stu-id="4a5ae-808">685.14</span></span></td>
<td><span data-ttu-id="4a5ae-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-810">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-810">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-811">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-812">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-812">10001</span></span></td>
<td><span data-ttu-id="4a5ae-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-813">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-814">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-815">124.57</span><span class="sxs-lookup"><span data-stu-id="4a5ae-815">124.57</span></span></td>
<td><span data-ttu-id="4a5ae-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-817">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-817">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-818">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-819">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-819">10001</span></span></td>
<td><span data-ttu-id="4a5ae-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-820">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-821">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-822">-675.00</span></span></td>
<td><span data-ttu-id="4a5ae-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-824">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-824">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-825">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-826">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-826">10001</span></span></td>
<td><span data-ttu-id="4a5ae-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-827">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-828">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-829">438.75</span><span class="sxs-lookup"><span data-stu-id="4a5ae-829">438.75</span></span></td>
<td><span data-ttu-id="4a5ae-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-831">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-831">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-832">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-833">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-833">10001</span></span></td>
<td><span data-ttu-id="4a5ae-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-834">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-835">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-836">236.25</span><span class="sxs-lookup"><span data-stu-id="4a5ae-836">236.25</span></span></td>
<td><span data-ttu-id="4a5ae-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-838">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-838">CC002</span></span></td>
<td><span data-ttu-id="4a5ae-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="4a5ae-839">Finance</span></span></td>
<td><span data-ttu-id="4a5ae-840">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-840">10001</span></span></td>
<td><span data-ttu-id="4a5ae-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-841">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-842">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="4a5ae-843">-8,150.29</span></span></td>
<td><span data-ttu-id="4a5ae-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-845">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-845">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-846">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-847">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-847">10001</span></span></td>
<td><span data-ttu-id="4a5ae-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-848">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-849">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4a5ae-850">5,297.69</span></span></td>
<td><span data-ttu-id="4a5ae-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-852">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-852">CC004</span></span></td>
<td><span data-ttu-id="4a5ae-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4a5ae-853">Packaging</span></span></td>
<td><span data-ttu-id="4a5ae-854">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-854">10001</span></span></td>
<td><span data-ttu-id="4a5ae-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-855">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-856">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4a5ae-857">2,852.60</span></span></td>
<td><span data-ttu-id="4a5ae-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-859">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-859">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-860">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-861">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-861">10001</span></span></td>
<td><span data-ttu-id="4a5ae-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-862">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-863">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="4a5ae-864">-713.75</span></span></td>
<td><span data-ttu-id="4a5ae-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-866">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-867">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-868">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-868">10001</span></span></td>
<td><span data-ttu-id="4a5ae-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-869">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-870">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-871">535.31</span><span class="sxs-lookup"><span data-stu-id="4a5ae-871">535.31</span></span></td>
<td><span data-ttu-id="4a5ae-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-873">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-874">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-875">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-875">10001</span></span></td>
<td><span data-ttu-id="4a5ae-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-876">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-877">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-878">178.44</span><span class="sxs-lookup"><span data-stu-id="4a5ae-878">178.44</span></span></td>
<td><span data-ttu-id="4a5ae-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-880">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-880">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-881">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-882">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-882">10001</span></span></td>
<td><span data-ttu-id="4a5ae-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-883">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-884">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="4a5ae-885">-5,982.83</span></span></td>
<td><span data-ttu-id="4a5ae-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-887">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-888">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-889">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-889">10001</span></span></td>
<td><span data-ttu-id="4a5ae-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-890">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-891">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4a5ae-892">4,487.12</span></span></td>
<td><span data-ttu-id="4a5ae-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-894">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-895">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-896">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-896">10001</span></span></td>
<td><span data-ttu-id="4a5ae-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-897">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-898">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4a5ae-899">1,495.71</span></span></td>
<td><span data-ttu-id="4a5ae-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-901">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-901">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-902">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-903">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-903">10001</span></span></td>
<td><span data-ttu-id="4a5ae-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-904">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-905">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="4a5ae-906">-286.25</span></span></td>
<td><span data-ttu-id="4a5ae-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-908">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-909">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-910">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-910">10001</span></span></td>
<td><span data-ttu-id="4a5ae-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-911">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-912">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-913">241.05</span><span class="sxs-lookup"><span data-stu-id="4a5ae-913">241.05</span></span></td>
<td><span data-ttu-id="4a5ae-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-915">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-916">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-917">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-917">10001</span></span></td>
<td><span data-ttu-id="4a5ae-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-918">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-919">Fixed cost</span></span></td>
<td><span data-ttu-id="4a5ae-920">45.20</span><span class="sxs-lookup"><span data-stu-id="4a5ae-920">45.20</span></span></td>
<td><span data-ttu-id="4a5ae-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-922">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-922">CC003</span></span></td>
<td><span data-ttu-id="4a5ae-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4a5ae-923">Assembly</span></span></td>
<td><span data-ttu-id="4a5ae-924">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-924">10001</span></span></td>
<td><span data-ttu-id="4a5ae-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-925">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-926">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="4a5ae-927">-2,977.17</span></span></td>
<td><span data-ttu-id="4a5ae-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-929">Prod 1</span></span></td>
<td><span data-ttu-id="4a5ae-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-930">Product 1</span></span></td>
<td><span data-ttu-id="4a5ae-931">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-931">10001</span></span></td>
<td><span data-ttu-id="4a5ae-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-932">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-933">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4a5ae-934">2,507.09</span></span></td>
<td><span data-ttu-id="4a5ae-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a5ae-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-936">Prod 2</span></span></td>
<td><span data-ttu-id="4a5ae-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-937">Product 2</span></span></td>
<td><span data-ttu-id="4a5ae-938">10001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-938">10001</span></span></td>
<td><span data-ttu-id="4a5ae-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-939">Electricity</span></span></td>
<td><span data-ttu-id="4a5ae-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-940">Variable cost</span></span></td>
<td><span data-ttu-id="4a5ae-941">470.08</span><span class="sxs-lookup"><span data-stu-id="4a5ae-941">470.08</span></span></td>
<td><span data-ttu-id="4a5ae-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4a5ae-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4a5ae-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="4a5ae-943">Conclusion</span></span>
<span data-ttu-id="4a5ae-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4a5ae-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4a5ae-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4a5ae-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4a5ae-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4a5ae-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4a5ae-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4a5ae-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4a5ae-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="4a5ae-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4a5ae-951">CC099</span><span class="sxs-lookup"><span data-stu-id="4a5ae-951">CC099</span></span></th>
<th><span data-ttu-id="4a5ae-952">CC001</span><span class="sxs-lookup"><span data-stu-id="4a5ae-952">CC001</span></span></th>
<th><span data-ttu-id="4a5ae-953">CC002</span><span class="sxs-lookup"><span data-stu-id="4a5ae-953">CC002</span></span></th>
<th><span data-ttu-id="4a5ae-954">CC003</span><span class="sxs-lookup"><span data-stu-id="4a5ae-954">CC003</span></span></th>
<th><span data-ttu-id="4a5ae-955">CC004</span><span class="sxs-lookup"><span data-stu-id="4a5ae-955">CC004</span></span></th>
<th><span data-ttu-id="4a5ae-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-956">Proj 1</span></span></th>
<th><span data-ttu-id="4a5ae-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-957">Proj 2</span></span></th>
<th><span data-ttu-id="4a5ae-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4a5ae-958">Prod 1</span></span></th>
<th><span data-ttu-id="4a5ae-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4a5ae-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4a5ae-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4a5ae-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4a5ae-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="4a5ae-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-971">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4a5ae-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-973">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-975">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-978">776.36</span><span class="sxs-lookup"><span data-stu-id="4a5ae-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-979">223.64</span><span class="sxs-lookup"><span data-stu-id="4a5ae-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4a5ae-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4a5ae-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-982">000</span><span class="sxs-lookup"><span data-stu-id="4a5ae-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-983">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-984">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-985">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-987">30,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-988">10,00</span><span class="sxs-lookup"><span data-stu-id="4a5ae-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4a5ae-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4a5ae-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4a5ae-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4a5ae-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4a5ae-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4a5ae-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4a5ae-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4a5ae-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4a5ae-996">Zie [Beleid voor totalisering van kosten en overheadberekening](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4a5ae-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



