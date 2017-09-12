---
title: Overheadberekening
description: In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 1eb5560ba795ab6df61b5af889049810dd00d79e
ms.contentlocale: nl-nl
ms.lasthandoff: 06/29/2017


---

# <a name="overhead-calculation"></a><span data-ttu-id="1ba31-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="1ba31-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1ba31-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="1ba31-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="1ba31-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="1ba31-105">Term definition</span></span>
---------------

<span data-ttu-id="1ba31-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="1ba31-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="1ba31-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="1ba31-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="1ba31-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="1ba31-109">Huur</span><span class="sxs-lookup"><span data-stu-id="1ba31-109">Rent</span></span>
-   <span data-ttu-id="1ba31-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-110">Electricity</span></span>
-   <span data-ttu-id="1ba31-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="1ba31-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="1ba31-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="1ba31-112">Overhead calculation overview</span></span>
<span data-ttu-id="1ba31-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1ba31-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="1ba31-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="1ba31-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="1ba31-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="1ba31-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="1ba31-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="1ba31-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="1ba31-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="1ba31-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="1ba31-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="1ba31-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="1ba31-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="1ba31-119">Version type</span></span>
-   <span data-ttu-id="1ba31-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="1ba31-120">Date and time</span></span>
-   <span data-ttu-id="1ba31-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="1ba31-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="1ba31-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="1ba31-122">Fiscal year</span></span>
-   <span data-ttu-id="1ba31-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="1ba31-123">Fiscal period</span></span>

<span data-ttu-id="1ba31-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1ba31-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="1ba31-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="1ba31-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="1ba31-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1ba31-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="1ba31-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="1ba31-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="1ba31-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="1ba31-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="1ba31-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="1ba31-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="1ba31-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="1ba31-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="1ba31-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="1ba31-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="1ba31-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="1ba31-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="1ba31-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="1ba31-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="1ba31-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="1ba31-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="1ba31-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="1ba31-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="1ba31-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="1ba31-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="1ba31-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="1ba31-140">Main account</span></span></th>
<th><span data-ttu-id="1ba31-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="1ba31-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="1ba31-143">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-143">CC099</span></span></td>
<td><span data-ttu-id="1ba31-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-144">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-145">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-145">10001</span></span></td>
<td><span data-ttu-id="1ba31-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-146">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="1ba31-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="1ba31-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="1ba31-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="1ba31-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="1ba31-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="1ba31-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="1ba31-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="1ba31-151">Define the cost behavior rule</span></span>

<span data-ttu-id="1ba31-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="1ba31-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="1ba31-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="1ba31-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="1ba31-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="1ba31-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="1ba31-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="1ba31-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="1ba31-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="1ba31-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="1ba31-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="1ba31-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="1ba31-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="1ba31-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-160">Journal</span></span></th>
<th><span data-ttu-id="1ba31-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1ba31-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1ba31-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1ba31-163">Versie</span><span class="sxs-lookup"><span data-stu-id="1ba31-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-164">00001</span><span class="sxs-lookup"><span data-stu-id="1ba31-164">00001</span></span></td>
<td><span data-ttu-id="1ba31-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="1ba31-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-166">Fiscal</span></span></td>
<td><span data-ttu-id="1ba31-167">2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-167">2017</span></span></td>
<td><span data-ttu-id="1ba31-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-168">Period 1</span></span></td>
<td><span data-ttu-id="1ba31-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1ba31-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="1ba31-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-173">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-174">Cost behavior</span></span></th>
<th><span data-ttu-id="1ba31-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="1ba31-177">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-177">CC099</span></span></td>
<td><span data-ttu-id="1ba31-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-178">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-179">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-179">10001</span></span></td>
<td><span data-ttu-id="1ba31-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-180">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="1ba31-181">Unclassified</span></span></td>
<td><span data-ttu-id="1ba31-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1ba31-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="1ba31-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-185">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-186">Cost behavior</span></span></th>
<th><span data-ttu-id="1ba31-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-187">Amount</span></span></th>
<th><span data-ttu-id="1ba31-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-189">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-189">CC099</span></span></td>
<td><span data-ttu-id="1ba31-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-190">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-191">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-191">10001</span></span></td>
<td><span data-ttu-id="1ba31-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-192">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="1ba31-193">Unclassified</span></span></td>
<td><span data-ttu-id="1ba31-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-194">10,000.00</span></span></td>
<td><span data-ttu-id="1ba31-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-196">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-196">CC099</span></span></td>
<td><span data-ttu-id="1ba31-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-197">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-198">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-198">10001</span></span></td>
<td><span data-ttu-id="1ba31-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-199">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="1ba31-200">Unclassified</span></span></td>
<td><span data-ttu-id="1ba31-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-201">-10,000.00</span></span></td>
<td><span data-ttu-id="1ba31-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-203">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-203">CC099</span></span></td>
<td><span data-ttu-id="1ba31-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-204">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-205">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-205">10001</span></span></td>
<td><span data-ttu-id="1ba31-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-206">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-207">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-208">1,000.00</span></span></td>
<td><span data-ttu-id="1ba31-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-210">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-210">CC099</span></span></td>
<td><span data-ttu-id="1ba31-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-211">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-212">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-212">10001</span></span></td>
<td><span data-ttu-id="1ba31-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-213">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-214">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-215">9,000.00</span></span></td>
<td><span data-ttu-id="1ba31-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-217">Zie Kostengedragbeleid voor gedetailleerde informatie over kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="1ba31-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="1ba31-218">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="1ba31-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="1ba31-219">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="1ba31-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="1ba31-220">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="1ba31-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="1ba31-221">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="1ba31-222">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="1ba31-222">Define the cost distribution rule</span></span>

<span data-ttu-id="1ba31-223">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="1ba31-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="1ba31-224">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="1ba31-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="1ba31-225">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="1ba31-226">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="1ba31-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="1ba31-227">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="1ba31-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="1ba31-228">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="1ba31-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-229">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-229">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="1ba31-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-231">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-231">CC001</span></span></td>
<td><span data-ttu-id="1ba31-232">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-232">HR</span></span></td>
<td><span data-ttu-id="1ba31-233">1.000</span><span class="sxs-lookup"><span data-stu-id="1ba31-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-234">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-234">CC002</span></span></td>
<td><span data-ttu-id="1ba31-235">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-235">Finance</span></span></td>
<td><span data-ttu-id="1ba31-236">6.000</span><span class="sxs-lookup"><span data-stu-id="1ba31-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-237">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-237">CC003</span></span></td>
<td><span data-ttu-id="1ba31-238">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-238">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-239">0</span><span class="sxs-lookup"><span data-stu-id="1ba31-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-240">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-241">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-241">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-242">Magnitude</span><span class="sxs-lookup"><span data-stu-id="1ba31-242">Magnitude</span></span></th>
<th><span data-ttu-id="1ba31-243">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="1ba31-243">Allocation factor</span></span></th>
<th><span data-ttu-id="1ba31-244">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-245">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-245">CC001</span></span></td>
<td><span data-ttu-id="1ba31-246">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-246">HR</span></span></td>
<td><span data-ttu-id="1ba31-247">1.000</span><span class="sxs-lookup"><span data-stu-id="1ba31-247">1,000</span></span></td>
<td><span data-ttu-id="1ba31-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1ba31-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="1ba31-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-250">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-250">CC002</span></span></td>
<td><span data-ttu-id="1ba31-251">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-251">Finance</span></span></td>
<td><span data-ttu-id="1ba31-252">6.000</span><span class="sxs-lookup"><span data-stu-id="1ba31-252">6,000</span></span></td>
<td><span data-ttu-id="1ba31-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1ba31-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="1ba31-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-255">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-255">CC003</span></span></td>
<td><span data-ttu-id="1ba31-256">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-256">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-257">0</span><span class="sxs-lookup"><span data-stu-id="1ba31-257">0</span></span></td>
<td><span data-ttu-id="1ba31-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="1ba31-259">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-260">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="1ba31-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="1ba31-261">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-262">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-262">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-263">Formule</span><span class="sxs-lookup"><span data-stu-id="1ba31-263">Formula</span></span></th>
<th><span data-ttu-id="1ba31-264">Magnitude</span><span class="sxs-lookup"><span data-stu-id="1ba31-264">Magnitude</span></span></th>
<th><span data-ttu-id="1ba31-265">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="1ba31-265">Allocation factor</span></span></th>
<th><span data-ttu-id="1ba31-266">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-267">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-267">CC001</span></span></td>
<td><span data-ttu-id="1ba31-268">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-268">HR</span></span></td>
<td><span data-ttu-id="1ba31-269">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1ba31-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1ba31-270">1</span><span class="sxs-lookup"><span data-stu-id="1ba31-270">1</span></span></td>
<td><span data-ttu-id="1ba31-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1ba31-272">500,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-273">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-273">CC002</span></span></td>
<td><span data-ttu-id="1ba31-274">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-274">Finance</span></span></td>
<td><span data-ttu-id="1ba31-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1ba31-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1ba31-276">1</span><span class="sxs-lookup"><span data-stu-id="1ba31-276">1</span></span></td>
<td><span data-ttu-id="1ba31-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1ba31-278">500,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-279">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-279">CC003</span></span></td>
<td><span data-ttu-id="1ba31-280">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-280">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="1ba31-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="1ba31-282">0</span><span class="sxs-lookup"><span data-stu-id="1ba31-282">0</span></span></td>
<td><span data-ttu-id="1ba31-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="1ba31-284">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="1ba31-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-286">Journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-286">Journal</span></span></th>
<th><span data-ttu-id="1ba31-287">Type journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1ba31-288">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1ba31-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1ba31-289">Versie</span><span class="sxs-lookup"><span data-stu-id="1ba31-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-290">00002</span><span class="sxs-lookup"><span data-stu-id="1ba31-290">00002</span></span></td>
<td><span data-ttu-id="1ba31-291">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="1ba31-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="1ba31-292">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-292">Fiscal</span></span></td>
<td><span data-ttu-id="1ba31-293">2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-293">2017</span></span></td>
<td><span data-ttu-id="1ba31-294">Periode 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-294">Period 1</span></span></td>
<td><span data-ttu-id="1ba31-295">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1ba31-296">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="1ba31-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-297">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-298">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-299">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-299">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-300">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-300">Cost behavior</span></span></th>
<th><span data-ttu-id="1ba31-301">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-302">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-303">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-303">CC099</span></span></td>
<td><span data-ttu-id="1ba31-304">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-304">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-305">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-305">10001</span></span></td>
<td><span data-ttu-id="1ba31-306">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-306">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-307">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-307">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-309">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-310">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-310">CC099</span></span></td>
<td><span data-ttu-id="1ba31-311">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-311">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-312">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-312">10001</span></span></td>
<td><span data-ttu-id="1ba31-313">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-313">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-314">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-314">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-315">9.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1ba31-316">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="1ba31-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-317">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-318">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-318">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-319">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-319">Cost behavior</span></span></th>
<th><span data-ttu-id="1ba31-320">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-320">Amount</span></span></th>
<th><span data-ttu-id="1ba31-321">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-322">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-322">CC099</span></span></td>
<td><span data-ttu-id="1ba31-323">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-323">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-324">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-324">10001</span></span></td>
<td><span data-ttu-id="1ba31-325">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-325">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-326">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-326">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-327">-1,000.00</span></span></td>
<td><span data-ttu-id="1ba31-328">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-329">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-329">CC001</span></span></td>
<td><span data-ttu-id="1ba31-330">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-330">HR</span></span></td>
<td><span data-ttu-id="1ba31-331">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-331">10001</span></span></td>
<td><span data-ttu-id="1ba31-332">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-332">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-333">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-333">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-334">500,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-334">500.00</span></span></td>
<td><span data-ttu-id="1ba31-335">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-336">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-336">CC002</span></span></td>
<td><span data-ttu-id="1ba31-337">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-337">Finance</span></span></td>
<td><span data-ttu-id="1ba31-338">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-338">10001</span></span></td>
<td><span data-ttu-id="1ba31-339">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-339">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-340">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-340">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-341">500,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-341">500.00</span></span></td>
<td><span data-ttu-id="1ba31-342">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-343">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-343">CC099</span></span></td>
<td><span data-ttu-id="1ba31-344">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="1ba31-344">Default cost center</span></span></td>
<td><span data-ttu-id="1ba31-345">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-345">10001</span></span></td>
<td><span data-ttu-id="1ba31-346">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-346">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-347">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-347">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-348">-9,000.00</span></span></td>
<td><span data-ttu-id="1ba31-349">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-350">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-350">CC001</span></span></td>
<td><span data-ttu-id="1ba31-351">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-351">HR</span></span></td>
<td><span data-ttu-id="1ba31-352">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-352">10001</span></span></td>
<td><span data-ttu-id="1ba31-353">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-353">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-354">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-354">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="1ba31-355">1,285.71</span></span></td>
<td><span data-ttu-id="1ba31-356">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-357">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-357">CC002</span></span></td>
<td><span data-ttu-id="1ba31-358">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-358">Finance</span></span></td>
<td><span data-ttu-id="1ba31-359">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-359">10001</span></span></td>
<td><span data-ttu-id="1ba31-360">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-360">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-361">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-361">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="1ba31-362">7,714.29</span></span></td>
<td><span data-ttu-id="1ba31-363">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-364">Zie Kostenverdelingsbeleid en Toewijzigingsgrondslagen voor gedetailleerde informatie over kostenverdeling en toewijzingsgrondslagen.</span><span class="sxs-lookup"><span data-stu-id="1ba31-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="1ba31-365">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="1ba31-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="1ba31-366">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="1ba31-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="1ba31-367">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="1ba31-368">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="1ba31-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="1ba31-369">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="1ba31-369">Define the overhead rate</span></span>

<span data-ttu-id="1ba31-370">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="1ba31-371">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-372">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-372">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-373">Uren</span><span class="sxs-lookup"><span data-stu-id="1ba31-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-374">Proj 1</span></span></td>
<td><span data-ttu-id="1ba31-375">Project 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-375">Project 1</span></span></td>
<td><span data-ttu-id="1ba31-376">3</span><span class="sxs-lookup"><span data-stu-id="1ba31-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-377">Proj 2</span></span></td>
<td><span data-ttu-id="1ba31-378">Project 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-378">Project 2</span></span></td>
<td><span data-ttu-id="1ba31-379">1</span><span class="sxs-lookup"><span data-stu-id="1ba31-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-380">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="1ba31-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-381">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-381">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-382">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-382">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-383">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-383">Cost behavior</span></span></th>
<th><span data-ttu-id="1ba31-384">Eenheden</span><span class="sxs-lookup"><span data-stu-id="1ba31-384">Units</span></span></th>
<th><span data-ttu-id="1ba31-385">Tarief</span><span class="sxs-lookup"><span data-stu-id="1ba31-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-386">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-386">CC001</span></span></td>
<td><span data-ttu-id="1ba31-387">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-387">HR</span></span></td>
<td><span data-ttu-id="1ba31-388">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-388">10001</span></span></td>
<td><span data-ttu-id="1ba31-389">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-389">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-390">1</span><span class="sxs-lookup"><span data-stu-id="1ba31-390">1</span></span></td>
<td><span data-ttu-id="1ba31-391">10</span><span class="sxs-lookup"><span data-stu-id="1ba31-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-392">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="1ba31-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-393">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-393">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-394">Magnitude</span><span class="sxs-lookup"><span data-stu-id="1ba31-394">Magnitude</span></span></th>
<th><span data-ttu-id="1ba31-395">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-395">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-396">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="1ba31-396">Allocation factor</span></span></th>
<th><span data-ttu-id="1ba31-397">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-398">Proj 1</span></span></td>
<td><span data-ttu-id="1ba31-399">Project 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-399">Project 1</span></span></td>
<td><span data-ttu-id="1ba31-400">3</span><span class="sxs-lookup"><span data-stu-id="1ba31-400">3</span></span></td>
<td><span data-ttu-id="1ba31-401">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-401">10001</span></span></td>
<td><span data-ttu-id="1ba31-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="1ba31-403">30,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-404">Proj 2</span></span></td>
<td><span data-ttu-id="1ba31-405">Project 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-405">Project 2</span></span></td>
<td><span data-ttu-id="1ba31-406">1</span><span class="sxs-lookup"><span data-stu-id="1ba31-406">1</span></span></td>
<td><span data-ttu-id="1ba31-407">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-407">10001</span></span></td>
<td><span data-ttu-id="1ba31-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="1ba31-409">10,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="1ba31-410">Journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-411">Journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-411">Journal</span></span></th>
<th><span data-ttu-id="1ba31-412">Type journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1ba31-413">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1ba31-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1ba31-414">Versie</span><span class="sxs-lookup"><span data-stu-id="1ba31-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-415">00003</span><span class="sxs-lookup"><span data-stu-id="1ba31-415">00003</span></span></td>
<td><span data-ttu-id="1ba31-416">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="1ba31-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="1ba31-417">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-417">Fiscal</span></span></td>
<td><span data-ttu-id="1ba31-418">2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-418">2017</span></span></td>
<td><span data-ttu-id="1ba31-419">Periode 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-419">Period 1</span></span></td>
<td><span data-ttu-id="1ba31-420">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="1ba31-421">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="1ba31-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-422">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-423">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-423">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-424">Magnitude</span><span class="sxs-lookup"><span data-stu-id="1ba31-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-425">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-426">Proj 1</span></span></td>
<td><span data-ttu-id="1ba31-427">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="1ba31-428">3,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-429">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-430">Proj 2</span></span></td>
<td><span data-ttu-id="1ba31-431">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="1ba31-432">1,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1ba31-433">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="1ba31-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-434">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-435">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-435">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-436">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-436">Cost behavior</span></span></th>
<th><span data-ttu-id="1ba31-437">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-437">Amount</span></span></th>
<th><span data-ttu-id="1ba31-438">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="1ba31-439">CC0001</span></span></td>
<td><span data-ttu-id="1ba31-440">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-440">HR</span></span></td>
<td><span data-ttu-id="1ba31-441">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-441">10001</span></span></td>
<td><span data-ttu-id="1ba31-442">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-442">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-443">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-443">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-444">-30.00</span></span></td>
<td><span data-ttu-id="1ba31-445">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-446">Proj 1</span></span></td>
<td><span data-ttu-id="1ba31-447">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="1ba31-448">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-448">10001</span></span></td>
<td><span data-ttu-id="1ba31-449">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-449">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-450">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-450">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-451">30,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-451">30.00</span></span></td>
<td><span data-ttu-id="1ba31-452">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-453">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-453">CC001</span></span></td>
<td><span data-ttu-id="1ba31-454">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-454">HR</span></span></td>
<td><span data-ttu-id="1ba31-455">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-455">10001</span></span></td>
<td><span data-ttu-id="1ba31-456">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-456">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-457">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-457">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-458">-10.00</span></span></td>
<td><span data-ttu-id="1ba31-459">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-460">Proj 2</span></span></td>
<td><span data-ttu-id="1ba31-461">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="1ba31-462">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-462">10001</span></span></td>
<td><span data-ttu-id="1ba31-463">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-463">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-464">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-464">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-465">10,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-465">10.00</span></span></td>
<td><span data-ttu-id="1ba31-466">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-467">Zie Beleid voor overheadtarief en Toewijzingsgrondslagen voor gedetailleerde informatie over beleid voor overheadtarieven.</span><span class="sxs-lookup"><span data-stu-id="1ba31-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="1ba31-468">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="1ba31-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="1ba31-469">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="1ba31-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="1ba31-470">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="1ba31-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="1ba31-471">Finance and Operations ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="1ba31-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="1ba31-472">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="1ba31-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="1ba31-473">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="1ba31-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="1ba31-474">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="1ba31-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="1ba31-475">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="1ba31-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="1ba31-476">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="1ba31-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="1ba31-477">[![Wederzijdse methode](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="1ba31-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="1ba31-478">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="1ba31-478">Define the cost allocation</span></span>

<span data-ttu-id="1ba31-479">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="1ba31-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="1ba31-480">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="1ba31-481">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-482">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-482">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-483">HR-services</span><span class="sxs-lookup"><span data-stu-id="1ba31-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-484">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-484">CC002</span></span></td>
<td><span data-ttu-id="1ba31-485">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-485">Finance</span></span></td>
<td><span data-ttu-id="1ba31-486">35</span><span class="sxs-lookup"><span data-stu-id="1ba31-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-487">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-487">CC003</span></span></td>
<td><span data-ttu-id="1ba31-488">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-488">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-489">55</span><span class="sxs-lookup"><span data-stu-id="1ba31-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-490">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-490">CC004</span></span></td>
<td><span data-ttu-id="1ba31-491">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-491">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-492">10</span><span class="sxs-lookup"><span data-stu-id="1ba31-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-493">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="1ba31-494">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-495">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-495">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-496">Financiële services</span><span class="sxs-lookup"><span data-stu-id="1ba31-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-497">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-497">CC003</span></span></td>
<td><span data-ttu-id="1ba31-498">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-498">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-499">65</span><span class="sxs-lookup"><span data-stu-id="1ba31-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-500">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-500">CC004</span></span></td>
<td><span data-ttu-id="1ba31-501">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-501">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-502">35</span><span class="sxs-lookup"><span data-stu-id="1ba31-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-503">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="1ba31-504">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-505">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-505">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-506">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="1ba31-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-507">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-508">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-508">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-509">60</span><span class="sxs-lookup"><span data-stu-id="1ba31-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-510">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-511">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-511">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-512">20</span><span class="sxs-lookup"><span data-stu-id="1ba31-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-513">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="1ba31-514">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-515">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-515">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-516">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="1ba31-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-517">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-518">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-518">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-519">80</span><span class="sxs-lookup"><span data-stu-id="1ba31-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-520">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-521">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-521">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-522">15</span><span class="sxs-lookup"><span data-stu-id="1ba31-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-523">**Opmerking:** In Finance and Operations kunnen statistische metingen, zoals de productie-uren die een product verbruikt, worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="1ba31-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="1ba31-524">Zie Sjablonen van provider van statistische maateenheden voor gedetailleerdere informatie over statistische providers van statistische maateenheden.</span><span class="sxs-lookup"><span data-stu-id="1ba31-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="1ba31-525">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.) In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="1ba31-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-526">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-526">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-527">Magnitude</span><span class="sxs-lookup"><span data-stu-id="1ba31-527">Magnitude</span></span></th>
<th><span data-ttu-id="1ba31-528">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="1ba31-528">Allocation factor</span></span></th>
<th><span data-ttu-id="1ba31-529">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-529">Amount</span></span></th>
<th><span data-ttu-id="1ba31-530">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-531">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-531">CC002</span></span></td>
<td><span data-ttu-id="1ba31-532">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-532">Finance</span></span></td>
<td><span data-ttu-id="1ba31-533">35</span><span class="sxs-lookup"><span data-stu-id="1ba31-533">35</span></span></td>
<td><span data-ttu-id="1ba31-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1ba31-535">175.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-535">175.00</span></span></td>
<td><span data-ttu-id="1ba31-536">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-537">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-537">CC003</span></span></td>
<td><span data-ttu-id="1ba31-538">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-538">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-539">55</span><span class="sxs-lookup"><span data-stu-id="1ba31-539">55</span></span></td>
<td><span data-ttu-id="1ba31-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1ba31-541">275.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-541">275.00</span></span></td>
<td><span data-ttu-id="1ba31-542">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-543">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-543">CC004</span></span></td>
<td><span data-ttu-id="1ba31-544">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-544">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-545">10</span><span class="sxs-lookup"><span data-stu-id="1ba31-545">10</span></span></td>
<td><span data-ttu-id="1ba31-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="1ba31-547">50,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-547">50.00</span></span></td>
<td><span data-ttu-id="1ba31-548">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-549">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-549">CC002</span></span></td>
<td><span data-ttu-id="1ba31-550">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-550">Finance</span></span></td>
<td><span data-ttu-id="1ba31-551">35</span><span class="sxs-lookup"><span data-stu-id="1ba31-551">35</span></span></td>
<td><span data-ttu-id="1ba31-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="1ba31-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1ba31-553">436.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-553">436.00</span></span></td>
<td><span data-ttu-id="1ba31-554">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-555">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-555">CC003</span></span></td>
<td><span data-ttu-id="1ba31-556">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-556">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-557">55</span><span class="sxs-lookup"><span data-stu-id="1ba31-557">55</span></span></td>
<td><span data-ttu-id="1ba31-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="1ba31-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1ba31-559">685.14</span><span class="sxs-lookup"><span data-stu-id="1ba31-559">685.14</span></span></td>
<td><span data-ttu-id="1ba31-560">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-561">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-561">CC004</span></span></td>
<td><span data-ttu-id="1ba31-562">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-562">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-563">10</span><span class="sxs-lookup"><span data-stu-id="1ba31-563">10</span></span></td>
<td><span data-ttu-id="1ba31-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="1ba31-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="1ba31-565">124.57</span><span class="sxs-lookup"><span data-stu-id="1ba31-565">124.57</span></span></td>
<td><span data-ttu-id="1ba31-566">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-567">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="1ba31-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-568">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-568">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-569">Magnitude</span><span class="sxs-lookup"><span data-stu-id="1ba31-569">Magnitude</span></span></th>
<th><span data-ttu-id="1ba31-570">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="1ba31-570">Allocation factor</span></span></th>
<th><span data-ttu-id="1ba31-571">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-571">Amount</span></span></th>
<th><span data-ttu-id="1ba31-572">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-573">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-573">CC003</span></span></td>
<td><span data-ttu-id="1ba31-574">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-574">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-575">65</span><span class="sxs-lookup"><span data-stu-id="1ba31-575">65</span></span></td>
<td><span data-ttu-id="1ba31-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="1ba31-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="1ba31-577">438.75</span><span class="sxs-lookup"><span data-stu-id="1ba31-577">438.75</span></span></td>
<td><span data-ttu-id="1ba31-578">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-579">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-579">CC004</span></span></td>
<td><span data-ttu-id="1ba31-580">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-580">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-581">35</span><span class="sxs-lookup"><span data-stu-id="1ba31-581">35</span></span></td>
<td><span data-ttu-id="1ba31-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="1ba31-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="1ba31-583">236.25</span><span class="sxs-lookup"><span data-stu-id="1ba31-583">236.25</span></span></td>
<td><span data-ttu-id="1ba31-584">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-585">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-585">CC003</span></span></td>
<td><span data-ttu-id="1ba31-586">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-586">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-587">65</span><span class="sxs-lookup"><span data-stu-id="1ba31-587">65</span></span></td>
<td><span data-ttu-id="1ba31-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="1ba31-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="1ba31-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="1ba31-589">5,297.69</span></span></td>
<td><span data-ttu-id="1ba31-590">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-591">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-591">CC004</span></span></td>
<td><span data-ttu-id="1ba31-592">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-592">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-593">35</span><span class="sxs-lookup"><span data-stu-id="1ba31-593">35</span></span></td>
<td><span data-ttu-id="1ba31-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="1ba31-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="1ba31-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="1ba31-595">2,852.60</span></span></td>
<td><span data-ttu-id="1ba31-596">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-597">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="1ba31-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-598">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-598">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-599">Magnitude</span><span class="sxs-lookup"><span data-stu-id="1ba31-599">Magnitude</span></span></th>
<th><span data-ttu-id="1ba31-600">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="1ba31-600">Allocation factor</span></span></th>
<th><span data-ttu-id="1ba31-601">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-601">Amount</span></span></th>
<th><span data-ttu-id="1ba31-602">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-603">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-604">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-604">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-605">60</span><span class="sxs-lookup"><span data-stu-id="1ba31-605">60</span></span></td>
<td><span data-ttu-id="1ba31-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="1ba31-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="1ba31-607">535.31</span><span class="sxs-lookup"><span data-stu-id="1ba31-607">535.31</span></span></td>
<td><span data-ttu-id="1ba31-608">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-609">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-610">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-610">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-611">20</span><span class="sxs-lookup"><span data-stu-id="1ba31-611">20</span></span></td>
<td><span data-ttu-id="1ba31-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="1ba31-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="1ba31-613">178.44</span><span class="sxs-lookup"><span data-stu-id="1ba31-613">178.44</span></span></td>
<td><span data-ttu-id="1ba31-614">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-615">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-616">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-616">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-617">60</span><span class="sxs-lookup"><span data-stu-id="1ba31-617">60</span></span></td>
<td><span data-ttu-id="1ba31-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="1ba31-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="1ba31-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="1ba31-619">4,487.12</span></span></td>
<td><span data-ttu-id="1ba31-620">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-621">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-622">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-622">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-623">20</span><span class="sxs-lookup"><span data-stu-id="1ba31-623">20</span></span></td>
<td><span data-ttu-id="1ba31-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="1ba31-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="1ba31-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="1ba31-625">1,495.71</span></span></td>
<td><span data-ttu-id="1ba31-626">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ba31-627">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="1ba31-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-628">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-628">Cost object</span></span></th>
<th><span data-ttu-id="1ba31-629">Magnitude</span><span class="sxs-lookup"><span data-stu-id="1ba31-629">Magnitude</span></span></th>
<th><span data-ttu-id="1ba31-630">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="1ba31-630">Allocation factor</span></span></th>
<th><span data-ttu-id="1ba31-631">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-631">Amount</span></span></th>
<th><span data-ttu-id="1ba31-632">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-633">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-634">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-634">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-635">80</span><span class="sxs-lookup"><span data-stu-id="1ba31-635">80</span></span></td>
<td><span data-ttu-id="1ba31-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="1ba31-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="1ba31-637">241.05</span><span class="sxs-lookup"><span data-stu-id="1ba31-637">241.05</span></span></td>
<td><span data-ttu-id="1ba31-638">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-639">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-640">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-640">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-641">15</span><span class="sxs-lookup"><span data-stu-id="1ba31-641">15</span></span></td>
<td><span data-ttu-id="1ba31-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="1ba31-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="1ba31-643">45.20</span><span class="sxs-lookup"><span data-stu-id="1ba31-643">45.20</span></span></td>
<td><span data-ttu-id="1ba31-644">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-645">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-646">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-646">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-647">80</span><span class="sxs-lookup"><span data-stu-id="1ba31-647">80</span></span></td>
<td><span data-ttu-id="1ba31-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="1ba31-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="1ba31-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="1ba31-649">2,507.09</span></span></td>
<td><span data-ttu-id="1ba31-650">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-651">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-652">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-652">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-653">15</span><span class="sxs-lookup"><span data-stu-id="1ba31-653">15</span></span></td>
<td><span data-ttu-id="1ba31-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="1ba31-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="1ba31-655">470.08</span><span class="sxs-lookup"><span data-stu-id="1ba31-655">470.08</span></span></td>
<td><span data-ttu-id="1ba31-656">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="1ba31-657">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="1ba31-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-658">Journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-658">Journal</span></span></th>
<th><span data-ttu-id="1ba31-659">Type journaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="1ba31-660">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1ba31-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="1ba31-661">Versie</span><span class="sxs-lookup"><span data-stu-id="1ba31-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-662">00004</span><span class="sxs-lookup"><span data-stu-id="1ba31-662">00004</span></span></td>
<td><span data-ttu-id="1ba31-663">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="1ba31-664">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-664">Fiscal</span></span></td>
<td><span data-ttu-id="1ba31-665">2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-665">2017</span></span></td>
<td><span data-ttu-id="1ba31-666">Periode 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-666">Period 1</span></span></td>
<td><span data-ttu-id="1ba31-667">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="1ba31-668">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="1ba31-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ba31-669">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-670">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-671">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-671">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-672">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-672">Cost behavior</span></span></th>
<th><span data-ttu-id="1ba31-673">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-674">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-675">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-675">CC001</span></span></td>
<td><span data-ttu-id="1ba31-676">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-676">HR</span></span></td>
<td><span data-ttu-id="1ba31-677">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-677">10001</span></span></td>
<td><span data-ttu-id="1ba31-678">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-678">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-679">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-679">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-680">500,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-681">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-682">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-682">CC001</span></span></td>
<td><span data-ttu-id="1ba31-683">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-683">HR</span></span></td>
<td><span data-ttu-id="1ba31-684">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-684">10001</span></span></td>
<td><span data-ttu-id="1ba31-685">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-685">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-686">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-686">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="1ba31-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-688">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-689">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-689">CC002</span></span></td>
<td><span data-ttu-id="1ba31-690">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-690">Finance</span></span></td>
<td><span data-ttu-id="1ba31-691">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-691">10001</span></span></td>
<td><span data-ttu-id="1ba31-692">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-692">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-693">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-693">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-694">675.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-695">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-696">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-696">CC002</span></span></td>
<td><span data-ttu-id="1ba31-697">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-697">Finance</span></span></td>
<td><span data-ttu-id="1ba31-698">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-698">10001</span></span></td>
<td><span data-ttu-id="1ba31-699">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-699">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-700">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-700">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="1ba31-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-702">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-703">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-703">CC003</span></span></td>
<td><span data-ttu-id="1ba31-704">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-704">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-705">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-705">10001</span></span></td>
<td><span data-ttu-id="1ba31-706">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-706">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-707">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-707">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-708">713.75</span><span class="sxs-lookup"><span data-stu-id="1ba31-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-709">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-710">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-710">CC003</span></span></td>
<td><span data-ttu-id="1ba31-711">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-711">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-712">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-712">10001</span></span></td>
<td><span data-ttu-id="1ba31-713">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-713">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-714">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-714">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="1ba31-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-716">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-717">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-717">CC003</span></span></td>
<td><span data-ttu-id="1ba31-718">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-718">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-719">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-719">10001</span></span></td>
<td><span data-ttu-id="1ba31-720">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-720">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-721">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-721">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-722">286.25</span><span class="sxs-lookup"><span data-stu-id="1ba31-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-723">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-724">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-724">CC003</span></span></td>
<td><span data-ttu-id="1ba31-725">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-725">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-726">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-726">10001</span></span></td>
<td><span data-ttu-id="1ba31-727">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-727">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-728">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-728">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="1ba31-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-730">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-731">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-732">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-732">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-733">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-733">10001</span></span></td>
<td><span data-ttu-id="1ba31-734">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-734">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-735">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-735">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-736">776.36</span><span class="sxs-lookup"><span data-stu-id="1ba31-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-737">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-738">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-739">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-739">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-740">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-740">10001</span></span></td>
<td><span data-ttu-id="1ba31-741">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-741">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-742">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-742">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="1ba31-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-744">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-745">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-746">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-746">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-747">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-747">10001</span></span></td>
<td><span data-ttu-id="1ba31-748">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-748">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-749">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-749">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-750">223.64</span><span class="sxs-lookup"><span data-stu-id="1ba31-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-751">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="1ba31-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-752">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-753">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-753">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-754">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-754">10001</span></span></td>
<td><span data-ttu-id="1ba31-755">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-755">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-756">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-756">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="1ba31-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="1ba31-758">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="1ba31-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="1ba31-759">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="1ba31-760">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-760">Cost element</span></span></th>
<th><span data-ttu-id="1ba31-761">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-761">Cost behavior</span></span></th>
<th><span data-ttu-id="1ba31-762">Bedrag</span><span class="sxs-lookup"><span data-stu-id="1ba31-762">Amount</span></span></th>
<th><span data-ttu-id="1ba31-763">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="1ba31-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ba31-764">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-764">CC001</span></span></td>
<td><span data-ttu-id="1ba31-765">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-765">HR</span></span></td>
<td><span data-ttu-id="1ba31-766">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-766">10001</span></span></td>
<td><span data-ttu-id="1ba31-767">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-767">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-768">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-768">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-769">-500.00</span></span></td>
<td><span data-ttu-id="1ba31-770">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-771">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-771">CC002</span></span></td>
<td><span data-ttu-id="1ba31-772">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-772">Finance</span></span></td>
<td><span data-ttu-id="1ba31-773">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-773">10001</span></span></td>
<td><span data-ttu-id="1ba31-774">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-774">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-775">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-775">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-776">175.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-776">175.00</span></span></td>
<td><span data-ttu-id="1ba31-777">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-778">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-778">CC003</span></span></td>
<td><span data-ttu-id="1ba31-779">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-779">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-780">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-780">10001</span></span></td>
<td><span data-ttu-id="1ba31-781">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-781">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-782">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-782">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-783">275.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-783">275.00</span></span></td>
<td><span data-ttu-id="1ba31-784">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-785">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-785">CC004</span></span></td>
<td><span data-ttu-id="1ba31-786">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-786">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-787">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-787">10001</span></span></td>
<td><span data-ttu-id="1ba31-788">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-788">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-789">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-789">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-790">50,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-790">50,00</span></span></td>
<td><span data-ttu-id="1ba31-791">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-792">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-792">CC001</span></span></td>
<td><span data-ttu-id="1ba31-793">HR</span><span class="sxs-lookup"><span data-stu-id="1ba31-793">HR</span></span></td>
<td><span data-ttu-id="1ba31-794">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-794">10001</span></span></td>
<td><span data-ttu-id="1ba31-795">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-795">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-796">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-796">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="1ba31-797">-1,245.71</span></span></td>
<td><span data-ttu-id="1ba31-798">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-799">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-799">CC002</span></span></td>
<td><span data-ttu-id="1ba31-800">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-800">Finance</span></span></td>
<td><span data-ttu-id="1ba31-801">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-801">10001</span></span></td>
<td><span data-ttu-id="1ba31-802">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-802">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-803">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-803">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-804">436.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-804">436.00</span></span></td>
<td><span data-ttu-id="1ba31-805">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-806">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-806">CC003</span></span></td>
<td><span data-ttu-id="1ba31-807">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-807">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-808">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-808">10001</span></span></td>
<td><span data-ttu-id="1ba31-809">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-809">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-810">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-810">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-811">685.14</span><span class="sxs-lookup"><span data-stu-id="1ba31-811">685.14</span></span></td>
<td><span data-ttu-id="1ba31-812">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-813">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-813">CC004</span></span></td>
<td><span data-ttu-id="1ba31-814">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-814">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-815">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-815">10001</span></span></td>
<td><span data-ttu-id="1ba31-816">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-816">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-817">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-817">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-818">124.57</span><span class="sxs-lookup"><span data-stu-id="1ba31-818">124.57</span></span></td>
<td><span data-ttu-id="1ba31-819">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-820">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-820">CC002</span></span></td>
<td><span data-ttu-id="1ba31-821">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-821">Finance</span></span></td>
<td><span data-ttu-id="1ba31-822">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-822">10001</span></span></td>
<td><span data-ttu-id="1ba31-823">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-823">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-824">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-824">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="1ba31-825">-675.00</span></span></td>
<td><span data-ttu-id="1ba31-826">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-827">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-827">CC003</span></span></td>
<td><span data-ttu-id="1ba31-828">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-828">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-829">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-829">10001</span></span></td>
<td><span data-ttu-id="1ba31-830">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-830">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-831">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-831">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-832">438.75</span><span class="sxs-lookup"><span data-stu-id="1ba31-832">438.75</span></span></td>
<td><span data-ttu-id="1ba31-833">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-834">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-834">CC004</span></span></td>
<td><span data-ttu-id="1ba31-835">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-835">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-836">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-836">10001</span></span></td>
<td><span data-ttu-id="1ba31-837">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-837">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-838">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-838">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-839">236.25</span><span class="sxs-lookup"><span data-stu-id="1ba31-839">236.25</span></span></td>
<td><span data-ttu-id="1ba31-840">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-841">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-841">CC002</span></span></td>
<td><span data-ttu-id="1ba31-842">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ba31-842">Finance</span></span></td>
<td><span data-ttu-id="1ba31-843">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-843">10001</span></span></td>
<td><span data-ttu-id="1ba31-844">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-844">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-845">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-845">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="1ba31-846">-8,150.29</span></span></td>
<td><span data-ttu-id="1ba31-847">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-848">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-848">CC003</span></span></td>
<td><span data-ttu-id="1ba31-849">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-849">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-850">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-850">10001</span></span></td>
<td><span data-ttu-id="1ba31-851">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-851">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-852">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-852">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="1ba31-853">5,297.69</span></span></td>
<td><span data-ttu-id="1ba31-854">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-855">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-855">CC004</span></span></td>
<td><span data-ttu-id="1ba31-856">Verpakking</span><span class="sxs-lookup"><span data-stu-id="1ba31-856">Packaging</span></span></td>
<td><span data-ttu-id="1ba31-857">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-857">10001</span></span></td>
<td><span data-ttu-id="1ba31-858">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-858">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-859">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-859">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="1ba31-860">2,852.60</span></span></td>
<td><span data-ttu-id="1ba31-861">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-862">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-862">CC003</span></span></td>
<td><span data-ttu-id="1ba31-863">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-863">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-864">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-864">10001</span></span></td>
<td><span data-ttu-id="1ba31-865">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-865">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-866">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-866">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="1ba31-867">-713.75</span></span></td>
<td><span data-ttu-id="1ba31-868">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-869">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-870">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-870">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-871">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-871">10001</span></span></td>
<td><span data-ttu-id="1ba31-872">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-872">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-873">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-873">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-874">535.31</span><span class="sxs-lookup"><span data-stu-id="1ba31-874">535.31</span></span></td>
<td><span data-ttu-id="1ba31-875">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-876">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-877">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-877">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-878">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-878">10001</span></span></td>
<td><span data-ttu-id="1ba31-879">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-879">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-880">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-880">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-881">178.44</span><span class="sxs-lookup"><span data-stu-id="1ba31-881">178.44</span></span></td>
<td><span data-ttu-id="1ba31-882">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-883">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-883">CC003</span></span></td>
<td><span data-ttu-id="1ba31-884">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-884">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-885">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-885">10001</span></span></td>
<td><span data-ttu-id="1ba31-886">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-886">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-887">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-887">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="1ba31-888">-5,982.83</span></span></td>
<td><span data-ttu-id="1ba31-889">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-890">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-891">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-891">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-892">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-892">10001</span></span></td>
<td><span data-ttu-id="1ba31-893">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-893">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-894">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-894">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="1ba31-895">4,487.12</span></span></td>
<td><span data-ttu-id="1ba31-896">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-897">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-898">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-898">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-899">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-899">10001</span></span></td>
<td><span data-ttu-id="1ba31-900">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-900">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-901">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-901">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="1ba31-902">1,495.71</span></span></td>
<td><span data-ttu-id="1ba31-903">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-904">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-904">CC003</span></span></td>
<td><span data-ttu-id="1ba31-905">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-905">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-906">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-906">10001</span></span></td>
<td><span data-ttu-id="1ba31-907">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-907">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-908">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-908">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="1ba31-909">-286.25</span></span></td>
<td><span data-ttu-id="1ba31-910">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-911">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-912">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-912">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-913">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-913">10001</span></span></td>
<td><span data-ttu-id="1ba31-914">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-914">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-915">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-915">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-916">241.05</span><span class="sxs-lookup"><span data-stu-id="1ba31-916">241.05</span></span></td>
<td><span data-ttu-id="1ba31-917">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-918">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-919">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-919">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-920">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-920">10001</span></span></td>
<td><span data-ttu-id="1ba31-921">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-921">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-922">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-922">Fixed cost</span></span></td>
<td><span data-ttu-id="1ba31-923">45.20</span><span class="sxs-lookup"><span data-stu-id="1ba31-923">45.20</span></span></td>
<td><span data-ttu-id="1ba31-924">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-925">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-925">CC003</span></span></td>
<td><span data-ttu-id="1ba31-926">Assembleren</span><span class="sxs-lookup"><span data-stu-id="1ba31-926">Assembly</span></span></td>
<td><span data-ttu-id="1ba31-927">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-927">10001</span></span></td>
<td><span data-ttu-id="1ba31-928">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-928">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-929">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-929">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="1ba31-930">-2,977.17</span></span></td>
<td><span data-ttu-id="1ba31-931">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-932">Prod 1</span></span></td>
<td><span data-ttu-id="1ba31-933">Product 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-933">Product 1</span></span></td>
<td><span data-ttu-id="1ba31-934">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-934">10001</span></span></td>
<td><span data-ttu-id="1ba31-935">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-935">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-936">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-936">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="1ba31-937">2,507.09</span></span></td>
<td><span data-ttu-id="1ba31-938">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ba31-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-939">Prod 2</span></span></td>
<td><span data-ttu-id="1ba31-940">Product 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-940">Product 2</span></span></td>
<td><span data-ttu-id="1ba31-941">10001</span><span class="sxs-lookup"><span data-stu-id="1ba31-941">10001</span></span></td>
<td><span data-ttu-id="1ba31-942">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-942">Electricity</span></span></td>
<td><span data-ttu-id="1ba31-943">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-943">Variable cost</span></span></td>
<td><span data-ttu-id="1ba31-944">470.08</span><span class="sxs-lookup"><span data-stu-id="1ba31-944">470.08</span></span></td>
<td><span data-ttu-id="1ba31-945">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="1ba31-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="1ba31-946">Conclusie</span><span class="sxs-lookup"><span data-stu-id="1ba31-946">Conclusion</span></span>
<span data-ttu-id="1ba31-947">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="1ba31-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="1ba31-948">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1ba31-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="1ba31-949">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="1ba31-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="1ba31-950">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="1ba31-951">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="1ba31-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="1ba31-952">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="1ba31-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="1ba31-953">Totaal</span><span class="sxs-lookup"><span data-stu-id="1ba31-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1ba31-954">CC099</span><span class="sxs-lookup"><span data-stu-id="1ba31-954">CC099</span></span></th>
<th><span data-ttu-id="1ba31-955">CC001</span><span class="sxs-lookup"><span data-stu-id="1ba31-955">CC001</span></span></th>
<th><span data-ttu-id="1ba31-956">CC002</span><span class="sxs-lookup"><span data-stu-id="1ba31-956">CC002</span></span></th>
<th><span data-ttu-id="1ba31-957">CC003</span><span class="sxs-lookup"><span data-stu-id="1ba31-957">CC003</span></span></th>
<th><span data-ttu-id="1ba31-958">CC004</span><span class="sxs-lookup"><span data-stu-id="1ba31-958">CC004</span></span></th>
<th><span data-ttu-id="1ba31-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-959">Proj 1</span></span></th>
<th><span data-ttu-id="1ba31-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-960">Proj 2</span></span></th>
<th><span data-ttu-id="1ba31-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="1ba31-961">Prod 1</span></span></th>
<th><span data-ttu-id="1ba31-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="1ba31-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="1ba31-963">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="1ba31-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="1ba31-973">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="1ba31-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-974">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="1ba31-975">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-976">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-977">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-978">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-979">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-980">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-981">776.36</span><span class="sxs-lookup"><span data-stu-id="1ba31-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-982">223.64</span><span class="sxs-lookup"><span data-stu-id="1ba31-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="1ba31-984">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="1ba31-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-985">000</span><span class="sxs-lookup"><span data-stu-id="1ba31-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-986">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-987">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-988">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-989">0,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-990">30,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-991">10,00</span><span class="sxs-lookup"><span data-stu-id="1ba31-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="1ba31-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="1ba31-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="1ba31-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="1ba31-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1ba31-995">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="1ba31-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="1ba31-996">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="1ba31-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="1ba31-997">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="1ba31-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="1ba31-998">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="1ba31-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="1ba31-999">Zie Beleid voor kostenaggregatie voor meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="1ba31-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="1ba31-1000">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="1ba31-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




