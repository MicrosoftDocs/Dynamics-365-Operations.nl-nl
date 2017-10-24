---
title: Overheadberekening
description: In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.
author: AndersGirke
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
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="a35ad-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="a35ad-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a35ad-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="a35ad-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="a35ad-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="a35ad-105">Term definition</span></span>
---------------

<span data-ttu-id="a35ad-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="a35ad-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="a35ad-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="a35ad-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="a35ad-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="a35ad-109">Huur</span><span class="sxs-lookup"><span data-stu-id="a35ad-109">Rent</span></span>
-   <span data-ttu-id="a35ad-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-110">Electricity</span></span>
-   <span data-ttu-id="a35ad-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="a35ad-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="a35ad-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="a35ad-112">Overhead calculation overview</span></span>
<span data-ttu-id="a35ad-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a35ad-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="a35ad-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="a35ad-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="a35ad-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="a35ad-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="a35ad-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="a35ad-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="a35ad-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="a35ad-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="a35ad-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="a35ad-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="a35ad-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="a35ad-119">Version type</span></span>
-   <span data-ttu-id="a35ad-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="a35ad-120">Date and time</span></span>
-   <span data-ttu-id="a35ad-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="a35ad-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="a35ad-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="a35ad-122">Fiscal year</span></span>
-   <span data-ttu-id="a35ad-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="a35ad-123">Fiscal period</span></span>

<span data-ttu-id="a35ad-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a35ad-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="a35ad-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="a35ad-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="a35ad-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a35ad-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="a35ad-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="a35ad-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="a35ad-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="a35ad-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="a35ad-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="a35ad-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="a35ad-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="a35ad-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="a35ad-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="a35ad-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="a35ad-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="a35ad-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="a35ad-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="a35ad-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="a35ad-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="a35ad-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="a35ad-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="a35ad-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="a35ad-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="a35ad-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="a35ad-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="a35ad-140">Main account</span></span></th>
<th><span data-ttu-id="a35ad-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="a35ad-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="a35ad-143">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-143">CC099</span></span></td>
<td><span data-ttu-id="a35ad-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-144">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-145">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-145">10001</span></span></td>
<td><span data-ttu-id="a35ad-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-146">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="a35ad-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="a35ad-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="a35ad-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="a35ad-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="a35ad-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="a35ad-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="a35ad-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="a35ad-151">Define the cost behavior rule</span></span>

<span data-ttu-id="a35ad-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="a35ad-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="a35ad-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="a35ad-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="a35ad-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="a35ad-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="a35ad-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="a35ad-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="a35ad-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="a35ad-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="a35ad-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="a35ad-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="a35ad-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="a35ad-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-160">Journal</span></span></th>
<th><span data-ttu-id="a35ad-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a35ad-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="a35ad-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a35ad-163">Versie</span><span class="sxs-lookup"><span data-stu-id="a35ad-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-164">00001</span><span class="sxs-lookup"><span data-stu-id="a35ad-164">00001</span></span></td>
<td><span data-ttu-id="a35ad-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="a35ad-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-166">Fiscal</span></span></td>
<td><span data-ttu-id="a35ad-167">2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-167">2017</span></span></td>
<td><span data-ttu-id="a35ad-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-168">Period 1</span></span></td>
<td><span data-ttu-id="a35ad-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a35ad-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="a35ad-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-173">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-174">Cost behavior</span></span></th>
<th><span data-ttu-id="a35ad-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="a35ad-177">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-177">CC099</span></span></td>
<td><span data-ttu-id="a35ad-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-178">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-179">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-179">10001</span></span></td>
<td><span data-ttu-id="a35ad-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-180">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="a35ad-181">Unclassified</span></span></td>
<td><span data-ttu-id="a35ad-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a35ad-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="a35ad-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-185">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-186">Cost behavior</span></span></th>
<th><span data-ttu-id="a35ad-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-187">Amount</span></span></th>
<th><span data-ttu-id="a35ad-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-189">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-189">CC099</span></span></td>
<td><span data-ttu-id="a35ad-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-190">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-191">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-191">10001</span></span></td>
<td><span data-ttu-id="a35ad-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-192">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="a35ad-193">Unclassified</span></span></td>
<td><span data-ttu-id="a35ad-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-194">10,000.00</span></span></td>
<td><span data-ttu-id="a35ad-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-196">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-196">CC099</span></span></td>
<td><span data-ttu-id="a35ad-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-197">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-198">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-198">10001</span></span></td>
<td><span data-ttu-id="a35ad-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-199">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="a35ad-200">Unclassified</span></span></td>
<td><span data-ttu-id="a35ad-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-201">-10,000.00</span></span></td>
<td><span data-ttu-id="a35ad-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-203">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-203">CC099</span></span></td>
<td><span data-ttu-id="a35ad-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-204">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-205">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-205">10001</span></span></td>
<td><span data-ttu-id="a35ad-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-206">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-207">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-208">1,000.00</span></span></td>
<td><span data-ttu-id="a35ad-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-210">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-210">CC099</span></span></td>
<td><span data-ttu-id="a35ad-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-211">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-212">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-212">10001</span></span></td>
<td><span data-ttu-id="a35ad-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-213">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-214">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-215">9,000.00</span></span></td>
<td><span data-ttu-id="a35ad-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-217">Zie Kostengedragbeleid voor gedetailleerde informatie over kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="a35ad-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="a35ad-218">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="a35ad-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="a35ad-219">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="a35ad-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="a35ad-220">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="a35ad-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="a35ad-221">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="a35ad-222">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="a35ad-222">Define the cost distribution rule</span></span>

<span data-ttu-id="a35ad-223">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="a35ad-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="a35ad-224">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="a35ad-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="a35ad-225">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="a35ad-226">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="a35ad-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="a35ad-227">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="a35ad-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="a35ad-228">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="a35ad-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-229">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-229">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="a35ad-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-231">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-231">CC001</span></span></td>
<td><span data-ttu-id="a35ad-232">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-232">HR</span></span></td>
<td><span data-ttu-id="a35ad-233">1.000</span><span class="sxs-lookup"><span data-stu-id="a35ad-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-234">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-234">CC002</span></span></td>
<td><span data-ttu-id="a35ad-235">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-235">Finance</span></span></td>
<td><span data-ttu-id="a35ad-236">6.000</span><span class="sxs-lookup"><span data-stu-id="a35ad-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-237">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-237">CC003</span></span></td>
<td><span data-ttu-id="a35ad-238">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-238">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-239">0</span><span class="sxs-lookup"><span data-stu-id="a35ad-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-240">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-241">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-241">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-242">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a35ad-242">Magnitude</span></span></th>
<th><span data-ttu-id="a35ad-243">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a35ad-243">Allocation factor</span></span></th>
<th><span data-ttu-id="a35ad-244">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-245">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-245">CC001</span></span></td>
<td><span data-ttu-id="a35ad-246">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-246">HR</span></span></td>
<td><span data-ttu-id="a35ad-247">1.000</span><span class="sxs-lookup"><span data-stu-id="a35ad-247">1,000</span></span></td>
<td><span data-ttu-id="a35ad-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a35ad-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a35ad-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-250">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-250">CC002</span></span></td>
<td><span data-ttu-id="a35ad-251">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-251">Finance</span></span></td>
<td><span data-ttu-id="a35ad-252">6.000</span><span class="sxs-lookup"><span data-stu-id="a35ad-252">6,000</span></span></td>
<td><span data-ttu-id="a35ad-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a35ad-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a35ad-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-255">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-255">CC003</span></span></td>
<td><span data-ttu-id="a35ad-256">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-256">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-257">0</span><span class="sxs-lookup"><span data-stu-id="a35ad-257">0</span></span></td>
<td><span data-ttu-id="a35ad-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a35ad-259">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-260">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="a35ad-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="a35ad-261">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-262">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-262">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-263">Formule</span><span class="sxs-lookup"><span data-stu-id="a35ad-263">Formula</span></span></th>
<th><span data-ttu-id="a35ad-264">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a35ad-264">Magnitude</span></span></th>
<th><span data-ttu-id="a35ad-265">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a35ad-265">Allocation factor</span></span></th>
<th><span data-ttu-id="a35ad-266">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-267">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-267">CC001</span></span></td>
<td><span data-ttu-id="a35ad-268">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-268">HR</span></span></td>
<td><span data-ttu-id="a35ad-269">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a35ad-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a35ad-270">1</span><span class="sxs-lookup"><span data-stu-id="a35ad-270">1</span></span></td>
<td><span data-ttu-id="a35ad-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a35ad-272">500,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-273">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-273">CC002</span></span></td>
<td><span data-ttu-id="a35ad-274">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-274">Finance</span></span></td>
<td><span data-ttu-id="a35ad-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a35ad-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a35ad-276">1</span><span class="sxs-lookup"><span data-stu-id="a35ad-276">1</span></span></td>
<td><span data-ttu-id="a35ad-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a35ad-278">500,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-279">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-279">CC003</span></span></td>
<td><span data-ttu-id="a35ad-280">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-280">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a35ad-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a35ad-282">0</span><span class="sxs-lookup"><span data-stu-id="a35ad-282">0</span></span></td>
<td><span data-ttu-id="a35ad-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a35ad-284">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a35ad-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-286">Journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-286">Journal</span></span></th>
<th><span data-ttu-id="a35ad-287">Type journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a35ad-288">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="a35ad-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a35ad-289">Versie</span><span class="sxs-lookup"><span data-stu-id="a35ad-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-290">00002</span><span class="sxs-lookup"><span data-stu-id="a35ad-290">00002</span></span></td>
<td><span data-ttu-id="a35ad-291">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="a35ad-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="a35ad-292">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-292">Fiscal</span></span></td>
<td><span data-ttu-id="a35ad-293">2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-293">2017</span></span></td>
<td><span data-ttu-id="a35ad-294">Periode 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-294">Period 1</span></span></td>
<td><span data-ttu-id="a35ad-295">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a35ad-296">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="a35ad-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-297">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-298">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-299">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-299">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-300">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-300">Cost behavior</span></span></th>
<th><span data-ttu-id="a35ad-301">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-302">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-303">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-303">CC099</span></span></td>
<td><span data-ttu-id="a35ad-304">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-304">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-305">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-305">10001</span></span></td>
<td><span data-ttu-id="a35ad-306">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-306">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-307">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-307">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-309">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-310">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-310">CC099</span></span></td>
<td><span data-ttu-id="a35ad-311">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-311">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-312">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-312">10001</span></span></td>
<td><span data-ttu-id="a35ad-313">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-313">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-314">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-314">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-315">9.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a35ad-316">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="a35ad-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-317">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-318">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-318">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-319">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-319">Cost behavior</span></span></th>
<th><span data-ttu-id="a35ad-320">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-320">Amount</span></span></th>
<th><span data-ttu-id="a35ad-321">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-322">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-322">CC099</span></span></td>
<td><span data-ttu-id="a35ad-323">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-323">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-324">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-324">10001</span></span></td>
<td><span data-ttu-id="a35ad-325">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-325">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-326">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-326">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-327">-1,000.00</span></span></td>
<td><span data-ttu-id="a35ad-328">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-329">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-329">CC001</span></span></td>
<td><span data-ttu-id="a35ad-330">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-330">HR</span></span></td>
<td><span data-ttu-id="a35ad-331">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-331">10001</span></span></td>
<td><span data-ttu-id="a35ad-332">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-332">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-333">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-333">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-334">500,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-334">500.00</span></span></td>
<td><span data-ttu-id="a35ad-335">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-336">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-336">CC002</span></span></td>
<td><span data-ttu-id="a35ad-337">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-337">Finance</span></span></td>
<td><span data-ttu-id="a35ad-338">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-338">10001</span></span></td>
<td><span data-ttu-id="a35ad-339">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-339">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-340">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-340">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-341">500,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-341">500.00</span></span></td>
<td><span data-ttu-id="a35ad-342">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-343">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-343">CC099</span></span></td>
<td><span data-ttu-id="a35ad-344">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="a35ad-344">Default cost center</span></span></td>
<td><span data-ttu-id="a35ad-345">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-345">10001</span></span></td>
<td><span data-ttu-id="a35ad-346">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-346">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-347">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-347">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-348">-9,000.00</span></span></td>
<td><span data-ttu-id="a35ad-349">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-350">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-350">CC001</span></span></td>
<td><span data-ttu-id="a35ad-351">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-351">HR</span></span></td>
<td><span data-ttu-id="a35ad-352">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-352">10001</span></span></td>
<td><span data-ttu-id="a35ad-353">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-353">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-354">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-354">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a35ad-355">1,285.71</span></span></td>
<td><span data-ttu-id="a35ad-356">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-357">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-357">CC002</span></span></td>
<td><span data-ttu-id="a35ad-358">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-358">Finance</span></span></td>
<td><span data-ttu-id="a35ad-359">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-359">10001</span></span></td>
<td><span data-ttu-id="a35ad-360">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-360">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-361">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-361">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a35ad-362">7,714.29</span></span></td>
<td><span data-ttu-id="a35ad-363">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-364">Zie Kostenverdelingsbeleid en Toewijzigingsgrondslagen voor gedetailleerde informatie over kostenverdeling en toewijzingsgrondslagen.</span><span class="sxs-lookup"><span data-stu-id="a35ad-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="a35ad-365">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="a35ad-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="a35ad-366">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="a35ad-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="a35ad-367">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="a35ad-368">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="a35ad-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="a35ad-369">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="a35ad-369">Define the overhead rate</span></span>

<span data-ttu-id="a35ad-370">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="a35ad-371">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-372">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-372">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-373">Uren</span><span class="sxs-lookup"><span data-stu-id="a35ad-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-374">Proj 1</span></span></td>
<td><span data-ttu-id="a35ad-375">Project 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-375">Project 1</span></span></td>
<td><span data-ttu-id="a35ad-376">3</span><span class="sxs-lookup"><span data-stu-id="a35ad-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-377">Proj 2</span></span></td>
<td><span data-ttu-id="a35ad-378">Project 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-378">Project 2</span></span></td>
<td><span data-ttu-id="a35ad-379">1</span><span class="sxs-lookup"><span data-stu-id="a35ad-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-380">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="a35ad-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-381">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-381">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-382">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-382">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-383">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-383">Cost behavior</span></span></th>
<th><span data-ttu-id="a35ad-384">Eenheden</span><span class="sxs-lookup"><span data-stu-id="a35ad-384">Units</span></span></th>
<th><span data-ttu-id="a35ad-385">Tarief</span><span class="sxs-lookup"><span data-stu-id="a35ad-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-386">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-386">CC001</span></span></td>
<td><span data-ttu-id="a35ad-387">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-387">HR</span></span></td>
<td><span data-ttu-id="a35ad-388">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-388">10001</span></span></td>
<td><span data-ttu-id="a35ad-389">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-389">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-390">1</span><span class="sxs-lookup"><span data-stu-id="a35ad-390">1</span></span></td>
<td><span data-ttu-id="a35ad-391">10</span><span class="sxs-lookup"><span data-stu-id="a35ad-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-392">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="a35ad-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-393">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-393">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-394">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a35ad-394">Magnitude</span></span></th>
<th><span data-ttu-id="a35ad-395">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-395">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-396">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a35ad-396">Allocation factor</span></span></th>
<th><span data-ttu-id="a35ad-397">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-398">Proj 1</span></span></td>
<td><span data-ttu-id="a35ad-399">Project 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-399">Project 1</span></span></td>
<td><span data-ttu-id="a35ad-400">3</span><span class="sxs-lookup"><span data-stu-id="a35ad-400">3</span></span></td>
<td><span data-ttu-id="a35ad-401">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-401">10001</span></span></td>
<td><span data-ttu-id="a35ad-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a35ad-403">30,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-404">Proj 2</span></span></td>
<td><span data-ttu-id="a35ad-405">Project 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-405">Project 2</span></span></td>
<td><span data-ttu-id="a35ad-406">1</span><span class="sxs-lookup"><span data-stu-id="a35ad-406">1</span></span></td>
<td><span data-ttu-id="a35ad-407">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-407">10001</span></span></td>
<td><span data-ttu-id="a35ad-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a35ad-409">10,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a35ad-410">Journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-411">Journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-411">Journal</span></span></th>
<th><span data-ttu-id="a35ad-412">Type journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a35ad-413">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="a35ad-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a35ad-414">Versie</span><span class="sxs-lookup"><span data-stu-id="a35ad-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-415">00003</span><span class="sxs-lookup"><span data-stu-id="a35ad-415">00003</span></span></td>
<td><span data-ttu-id="a35ad-416">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="a35ad-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="a35ad-417">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-417">Fiscal</span></span></td>
<td><span data-ttu-id="a35ad-418">2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-418">2017</span></span></td>
<td><span data-ttu-id="a35ad-419">Periode 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-419">Period 1</span></span></td>
<td><span data-ttu-id="a35ad-420">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="a35ad-421">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="a35ad-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-422">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-423">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-423">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-424">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a35ad-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-425">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-426">Proj 1</span></span></td>
<td><span data-ttu-id="a35ad-427">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a35ad-428">3,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-429">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-430">Proj 2</span></span></td>
<td><span data-ttu-id="a35ad-431">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a35ad-432">1,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a35ad-433">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="a35ad-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-434">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-435">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-435">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-436">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-436">Cost behavior</span></span></th>
<th><span data-ttu-id="a35ad-437">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-437">Amount</span></span></th>
<th><span data-ttu-id="a35ad-438">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="a35ad-439">CC0001</span></span></td>
<td><span data-ttu-id="a35ad-440">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-440">HR</span></span></td>
<td><span data-ttu-id="a35ad-441">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-441">10001</span></span></td>
<td><span data-ttu-id="a35ad-442">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-442">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-443">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-443">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-444">-30.00</span></span></td>
<td><span data-ttu-id="a35ad-445">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-446">Proj 1</span></span></td>
<td><span data-ttu-id="a35ad-447">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a35ad-448">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-448">10001</span></span></td>
<td><span data-ttu-id="a35ad-449">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-449">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-450">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-450">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-451">30,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-451">30.00</span></span></td>
<td><span data-ttu-id="a35ad-452">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-453">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-453">CC001</span></span></td>
<td><span data-ttu-id="a35ad-454">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-454">HR</span></span></td>
<td><span data-ttu-id="a35ad-455">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-455">10001</span></span></td>
<td><span data-ttu-id="a35ad-456">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-456">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-457">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-457">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-458">-10.00</span></span></td>
<td><span data-ttu-id="a35ad-459">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-460">Proj 2</span></span></td>
<td><span data-ttu-id="a35ad-461">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a35ad-462">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-462">10001</span></span></td>
<td><span data-ttu-id="a35ad-463">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-463">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-464">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-464">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-465">10,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-465">10.00</span></span></td>
<td><span data-ttu-id="a35ad-466">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-467">Zie Beleid voor overheadtarief en Toewijzingsgrondslagen voor gedetailleerde informatie over beleid voor overheadtarieven.</span><span class="sxs-lookup"><span data-stu-id="a35ad-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="a35ad-468">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="a35ad-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="a35ad-469">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="a35ad-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="a35ad-470">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="a35ad-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="a35ad-471">Finance and Operations ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="a35ad-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="a35ad-472">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="a35ad-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="a35ad-473">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="a35ad-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="a35ad-474">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="a35ad-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="a35ad-475">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="a35ad-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="a35ad-476">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="a35ad-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="a35ad-477">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="a35ad-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="a35ad-478">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="a35ad-478">Define the cost allocation</span></span>

<span data-ttu-id="a35ad-479">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="a35ad-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="a35ad-480">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="a35ad-481">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-482">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-482">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-483">HR-services</span><span class="sxs-lookup"><span data-stu-id="a35ad-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-484">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-484">CC002</span></span></td>
<td><span data-ttu-id="a35ad-485">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-485">Finance</span></span></td>
<td><span data-ttu-id="a35ad-486">35</span><span class="sxs-lookup"><span data-stu-id="a35ad-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-487">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-487">CC003</span></span></td>
<td><span data-ttu-id="a35ad-488">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-488">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-489">55</span><span class="sxs-lookup"><span data-stu-id="a35ad-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-490">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-490">CC004</span></span></td>
<td><span data-ttu-id="a35ad-491">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-491">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-492">10</span><span class="sxs-lookup"><span data-stu-id="a35ad-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-493">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="a35ad-494">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-495">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-495">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-496">Financiële services</span><span class="sxs-lookup"><span data-stu-id="a35ad-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-497">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-497">CC003</span></span></td>
<td><span data-ttu-id="a35ad-498">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-498">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-499">65</span><span class="sxs-lookup"><span data-stu-id="a35ad-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-500">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-500">CC004</span></span></td>
<td><span data-ttu-id="a35ad-501">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-501">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-502">35</span><span class="sxs-lookup"><span data-stu-id="a35ad-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-503">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="a35ad-504">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-505">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-505">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-506">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="a35ad-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-507">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-508">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-508">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-509">60</span><span class="sxs-lookup"><span data-stu-id="a35ad-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-510">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-511">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-511">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-512">20</span><span class="sxs-lookup"><span data-stu-id="a35ad-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-513">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="a35ad-514">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-515">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-515">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-516">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="a35ad-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-517">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-518">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-518">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-519">80</span><span class="sxs-lookup"><span data-stu-id="a35ad-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-520">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-521">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-521">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-522">15</span><span class="sxs-lookup"><span data-stu-id="a35ad-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-523">**Opmerking:** In Finance and Operations kunnen statistische metingen, zoals de productie-uren die een product verbruikt, worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="a35ad-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="a35ad-524">Zie Sjablonen van provider van statistische maateenheden voor gedetailleerdere informatie over statistische providers van statistische maateenheden.</span><span class="sxs-lookup"><span data-stu-id="a35ad-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="a35ad-525">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.) In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="a35ad-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-526">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-526">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-527">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a35ad-527">Magnitude</span></span></th>
<th><span data-ttu-id="a35ad-528">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a35ad-528">Allocation factor</span></span></th>
<th><span data-ttu-id="a35ad-529">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-529">Amount</span></span></th>
<th><span data-ttu-id="a35ad-530">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-531">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-531">CC002</span></span></td>
<td><span data-ttu-id="a35ad-532">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-532">Finance</span></span></td>
<td><span data-ttu-id="a35ad-533">35</span><span class="sxs-lookup"><span data-stu-id="a35ad-533">35</span></span></td>
<td><span data-ttu-id="a35ad-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a35ad-535">175.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-535">175.00</span></span></td>
<td><span data-ttu-id="a35ad-536">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-537">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-537">CC003</span></span></td>
<td><span data-ttu-id="a35ad-538">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-538">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-539">55</span><span class="sxs-lookup"><span data-stu-id="a35ad-539">55</span></span></td>
<td><span data-ttu-id="a35ad-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a35ad-541">275.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-541">275.00</span></span></td>
<td><span data-ttu-id="a35ad-542">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-543">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-543">CC004</span></span></td>
<td><span data-ttu-id="a35ad-544">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-544">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-545">10</span><span class="sxs-lookup"><span data-stu-id="a35ad-545">10</span></span></td>
<td><span data-ttu-id="a35ad-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a35ad-547">50,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-547">50.00</span></span></td>
<td><span data-ttu-id="a35ad-548">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-549">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-549">CC002</span></span></td>
<td><span data-ttu-id="a35ad-550">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-550">Finance</span></span></td>
<td><span data-ttu-id="a35ad-551">35</span><span class="sxs-lookup"><span data-stu-id="a35ad-551">35</span></span></td>
<td><span data-ttu-id="a35ad-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a35ad-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a35ad-553">436.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-553">436.00</span></span></td>
<td><span data-ttu-id="a35ad-554">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-555">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-555">CC003</span></span></td>
<td><span data-ttu-id="a35ad-556">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-556">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-557">55</span><span class="sxs-lookup"><span data-stu-id="a35ad-557">55</span></span></td>
<td><span data-ttu-id="a35ad-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a35ad-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a35ad-559">685.14</span><span class="sxs-lookup"><span data-stu-id="a35ad-559">685.14</span></span></td>
<td><span data-ttu-id="a35ad-560">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-561">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-561">CC004</span></span></td>
<td><span data-ttu-id="a35ad-562">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-562">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-563">10</span><span class="sxs-lookup"><span data-stu-id="a35ad-563">10</span></span></td>
<td><span data-ttu-id="a35ad-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a35ad-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a35ad-565">124.57</span><span class="sxs-lookup"><span data-stu-id="a35ad-565">124.57</span></span></td>
<td><span data-ttu-id="a35ad-566">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-567">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="a35ad-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-568">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-568">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-569">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a35ad-569">Magnitude</span></span></th>
<th><span data-ttu-id="a35ad-570">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a35ad-570">Allocation factor</span></span></th>
<th><span data-ttu-id="a35ad-571">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-571">Amount</span></span></th>
<th><span data-ttu-id="a35ad-572">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-573">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-573">CC003</span></span></td>
<td><span data-ttu-id="a35ad-574">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-574">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-575">65</span><span class="sxs-lookup"><span data-stu-id="a35ad-575">65</span></span></td>
<td><span data-ttu-id="a35ad-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a35ad-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a35ad-577">438.75</span><span class="sxs-lookup"><span data-stu-id="a35ad-577">438.75</span></span></td>
<td><span data-ttu-id="a35ad-578">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-579">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-579">CC004</span></span></td>
<td><span data-ttu-id="a35ad-580">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-580">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-581">35</span><span class="sxs-lookup"><span data-stu-id="a35ad-581">35</span></span></td>
<td><span data-ttu-id="a35ad-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a35ad-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a35ad-583">236.25</span><span class="sxs-lookup"><span data-stu-id="a35ad-583">236.25</span></span></td>
<td><span data-ttu-id="a35ad-584">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-585">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-585">CC003</span></span></td>
<td><span data-ttu-id="a35ad-586">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-586">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-587">65</span><span class="sxs-lookup"><span data-stu-id="a35ad-587">65</span></span></td>
<td><span data-ttu-id="a35ad-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a35ad-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a35ad-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a35ad-589">5,297.69</span></span></td>
<td><span data-ttu-id="a35ad-590">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-591">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-591">CC004</span></span></td>
<td><span data-ttu-id="a35ad-592">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-592">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-593">35</span><span class="sxs-lookup"><span data-stu-id="a35ad-593">35</span></span></td>
<td><span data-ttu-id="a35ad-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a35ad-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a35ad-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a35ad-595">2,852.60</span></span></td>
<td><span data-ttu-id="a35ad-596">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-597">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="a35ad-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-598">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-598">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-599">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a35ad-599">Magnitude</span></span></th>
<th><span data-ttu-id="a35ad-600">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a35ad-600">Allocation factor</span></span></th>
<th><span data-ttu-id="a35ad-601">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-601">Amount</span></span></th>
<th><span data-ttu-id="a35ad-602">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-603">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-604">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-604">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-605">60</span><span class="sxs-lookup"><span data-stu-id="a35ad-605">60</span></span></td>
<td><span data-ttu-id="a35ad-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a35ad-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a35ad-607">535.31</span><span class="sxs-lookup"><span data-stu-id="a35ad-607">535.31</span></span></td>
<td><span data-ttu-id="a35ad-608">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-609">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-610">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-610">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-611">20</span><span class="sxs-lookup"><span data-stu-id="a35ad-611">20</span></span></td>
<td><span data-ttu-id="a35ad-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a35ad-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a35ad-613">178.44</span><span class="sxs-lookup"><span data-stu-id="a35ad-613">178.44</span></span></td>
<td><span data-ttu-id="a35ad-614">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-615">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-616">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-616">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-617">60</span><span class="sxs-lookup"><span data-stu-id="a35ad-617">60</span></span></td>
<td><span data-ttu-id="a35ad-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a35ad-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a35ad-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a35ad-619">4,487.12</span></span></td>
<td><span data-ttu-id="a35ad-620">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-621">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-622">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-622">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-623">20</span><span class="sxs-lookup"><span data-stu-id="a35ad-623">20</span></span></td>
<td><span data-ttu-id="a35ad-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a35ad-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a35ad-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a35ad-625">1,495.71</span></span></td>
<td><span data-ttu-id="a35ad-626">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35ad-627">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="a35ad-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-628">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-628">Cost object</span></span></th>
<th><span data-ttu-id="a35ad-629">Magnitude</span><span class="sxs-lookup"><span data-stu-id="a35ad-629">Magnitude</span></span></th>
<th><span data-ttu-id="a35ad-630">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="a35ad-630">Allocation factor</span></span></th>
<th><span data-ttu-id="a35ad-631">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-631">Amount</span></span></th>
<th><span data-ttu-id="a35ad-632">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-633">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-634">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-634">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-635">80</span><span class="sxs-lookup"><span data-stu-id="a35ad-635">80</span></span></td>
<td><span data-ttu-id="a35ad-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a35ad-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a35ad-637">241.05</span><span class="sxs-lookup"><span data-stu-id="a35ad-637">241.05</span></span></td>
<td><span data-ttu-id="a35ad-638">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-639">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-640">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-640">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-641">15</span><span class="sxs-lookup"><span data-stu-id="a35ad-641">15</span></span></td>
<td><span data-ttu-id="a35ad-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a35ad-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a35ad-643">45.20</span><span class="sxs-lookup"><span data-stu-id="a35ad-643">45.20</span></span></td>
<td><span data-ttu-id="a35ad-644">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-645">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-646">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-646">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-647">80</span><span class="sxs-lookup"><span data-stu-id="a35ad-647">80</span></span></td>
<td><span data-ttu-id="a35ad-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a35ad-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a35ad-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a35ad-649">2,507.09</span></span></td>
<td><span data-ttu-id="a35ad-650">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-651">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-652">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-652">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-653">15</span><span class="sxs-lookup"><span data-stu-id="a35ad-653">15</span></span></td>
<td><span data-ttu-id="a35ad-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a35ad-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a35ad-655">470.08</span><span class="sxs-lookup"><span data-stu-id="a35ad-655">470.08</span></span></td>
<td><span data-ttu-id="a35ad-656">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a35ad-657">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="a35ad-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-658">Journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-658">Journal</span></span></th>
<th><span data-ttu-id="a35ad-659">Type journaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a35ad-660">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="a35ad-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a35ad-661">Versie</span><span class="sxs-lookup"><span data-stu-id="a35ad-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-662">00004</span><span class="sxs-lookup"><span data-stu-id="a35ad-662">00004</span></span></td>
<td><span data-ttu-id="a35ad-663">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="a35ad-664">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-664">Fiscal</span></span></td>
<td><span data-ttu-id="a35ad-665">2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-665">2017</span></span></td>
<td><span data-ttu-id="a35ad-666">Periode 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-666">Period 1</span></span></td>
<td><span data-ttu-id="a35ad-667">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="a35ad-668">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="a35ad-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a35ad-669">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-670">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-671">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-671">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-672">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-672">Cost behavior</span></span></th>
<th><span data-ttu-id="a35ad-673">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-674">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-675">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-675">CC001</span></span></td>
<td><span data-ttu-id="a35ad-676">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-676">HR</span></span></td>
<td><span data-ttu-id="a35ad-677">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-677">10001</span></span></td>
<td><span data-ttu-id="a35ad-678">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-678">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-679">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-679">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-680">500,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-681">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-682">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-682">CC001</span></span></td>
<td><span data-ttu-id="a35ad-683">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-683">HR</span></span></td>
<td><span data-ttu-id="a35ad-684">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-684">10001</span></span></td>
<td><span data-ttu-id="a35ad-685">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-685">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-686">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-686">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="a35ad-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-688">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-689">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-689">CC002</span></span></td>
<td><span data-ttu-id="a35ad-690">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-690">Finance</span></span></td>
<td><span data-ttu-id="a35ad-691">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-691">10001</span></span></td>
<td><span data-ttu-id="a35ad-692">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-692">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-693">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-693">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-694">675.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-695">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-696">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-696">CC002</span></span></td>
<td><span data-ttu-id="a35ad-697">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-697">Finance</span></span></td>
<td><span data-ttu-id="a35ad-698">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-698">10001</span></span></td>
<td><span data-ttu-id="a35ad-699">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-699">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-700">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-700">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="a35ad-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-702">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-703">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-703">CC003</span></span></td>
<td><span data-ttu-id="a35ad-704">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-704">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-705">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-705">10001</span></span></td>
<td><span data-ttu-id="a35ad-706">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-706">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-707">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-707">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-708">713.75</span><span class="sxs-lookup"><span data-stu-id="a35ad-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-709">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-710">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-710">CC003</span></span></td>
<td><span data-ttu-id="a35ad-711">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-711">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-712">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-712">10001</span></span></td>
<td><span data-ttu-id="a35ad-713">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-713">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-714">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-714">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="a35ad-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-716">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-717">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-717">CC003</span></span></td>
<td><span data-ttu-id="a35ad-718">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-718">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-719">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-719">10001</span></span></td>
<td><span data-ttu-id="a35ad-720">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-720">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-721">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-721">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-722">286.25</span><span class="sxs-lookup"><span data-stu-id="a35ad-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-723">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-724">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-724">CC003</span></span></td>
<td><span data-ttu-id="a35ad-725">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-725">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-726">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-726">10001</span></span></td>
<td><span data-ttu-id="a35ad-727">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-727">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-728">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-728">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="a35ad-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-730">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-731">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-732">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-732">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-733">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-733">10001</span></span></td>
<td><span data-ttu-id="a35ad-734">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-734">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-735">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-735">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-736">776.36</span><span class="sxs-lookup"><span data-stu-id="a35ad-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-737">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-738">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-739">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-739">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-740">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-740">10001</span></span></td>
<td><span data-ttu-id="a35ad-741">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-741">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-742">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-742">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a35ad-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-744">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-745">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-746">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-746">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-747">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-747">10001</span></span></td>
<td><span data-ttu-id="a35ad-748">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-748">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-749">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-749">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-750">223.64</span><span class="sxs-lookup"><span data-stu-id="a35ad-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-751">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="a35ad-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-752">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-753">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-753">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-754">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-754">10001</span></span></td>
<td><span data-ttu-id="a35ad-755">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-755">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-756">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-756">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a35ad-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a35ad-758">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="a35ad-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a35ad-759">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a35ad-760">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-760">Cost element</span></span></th>
<th><span data-ttu-id="a35ad-761">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-761">Cost behavior</span></span></th>
<th><span data-ttu-id="a35ad-762">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a35ad-762">Amount</span></span></th>
<th><span data-ttu-id="a35ad-763">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="a35ad-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a35ad-764">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-764">CC001</span></span></td>
<td><span data-ttu-id="a35ad-765">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-765">HR</span></span></td>
<td><span data-ttu-id="a35ad-766">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-766">10001</span></span></td>
<td><span data-ttu-id="a35ad-767">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-767">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-768">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-768">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-769">-500.00</span></span></td>
<td><span data-ttu-id="a35ad-770">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-771">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-771">CC002</span></span></td>
<td><span data-ttu-id="a35ad-772">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-772">Finance</span></span></td>
<td><span data-ttu-id="a35ad-773">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-773">10001</span></span></td>
<td><span data-ttu-id="a35ad-774">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-774">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-775">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-775">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-776">175.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-776">175.00</span></span></td>
<td><span data-ttu-id="a35ad-777">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-778">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-778">CC003</span></span></td>
<td><span data-ttu-id="a35ad-779">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-779">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-780">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-780">10001</span></span></td>
<td><span data-ttu-id="a35ad-781">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-781">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-782">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-782">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-783">275.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-783">275.00</span></span></td>
<td><span data-ttu-id="a35ad-784">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-785">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-785">CC004</span></span></td>
<td><span data-ttu-id="a35ad-786">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-786">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-787">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-787">10001</span></span></td>
<td><span data-ttu-id="a35ad-788">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-788">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-789">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-789">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-790">50,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-790">50,00</span></span></td>
<td><span data-ttu-id="a35ad-791">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-792">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-792">CC001</span></span></td>
<td><span data-ttu-id="a35ad-793">HR</span><span class="sxs-lookup"><span data-stu-id="a35ad-793">HR</span></span></td>
<td><span data-ttu-id="a35ad-794">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-794">10001</span></span></td>
<td><span data-ttu-id="a35ad-795">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-795">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-796">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-796">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="a35ad-797">-1,245.71</span></span></td>
<td><span data-ttu-id="a35ad-798">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-799">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-799">CC002</span></span></td>
<td><span data-ttu-id="a35ad-800">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-800">Finance</span></span></td>
<td><span data-ttu-id="a35ad-801">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-801">10001</span></span></td>
<td><span data-ttu-id="a35ad-802">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-802">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-803">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-803">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-804">436.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-804">436.00</span></span></td>
<td><span data-ttu-id="a35ad-805">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-806">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-806">CC003</span></span></td>
<td><span data-ttu-id="a35ad-807">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-807">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-808">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-808">10001</span></span></td>
<td><span data-ttu-id="a35ad-809">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-809">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-810">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-810">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-811">685.14</span><span class="sxs-lookup"><span data-stu-id="a35ad-811">685.14</span></span></td>
<td><span data-ttu-id="a35ad-812">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-813">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-813">CC004</span></span></td>
<td><span data-ttu-id="a35ad-814">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-814">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-815">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-815">10001</span></span></td>
<td><span data-ttu-id="a35ad-816">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-816">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-817">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-817">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-818">124.57</span><span class="sxs-lookup"><span data-stu-id="a35ad-818">124.57</span></span></td>
<td><span data-ttu-id="a35ad-819">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-820">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-820">CC002</span></span></td>
<td><span data-ttu-id="a35ad-821">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-821">Finance</span></span></td>
<td><span data-ttu-id="a35ad-822">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-822">10001</span></span></td>
<td><span data-ttu-id="a35ad-823">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-823">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-824">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-824">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="a35ad-825">-675.00</span></span></td>
<td><span data-ttu-id="a35ad-826">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-827">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-827">CC003</span></span></td>
<td><span data-ttu-id="a35ad-828">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-828">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-829">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-829">10001</span></span></td>
<td><span data-ttu-id="a35ad-830">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-830">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-831">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-831">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-832">438.75</span><span class="sxs-lookup"><span data-stu-id="a35ad-832">438.75</span></span></td>
<td><span data-ttu-id="a35ad-833">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-834">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-834">CC004</span></span></td>
<td><span data-ttu-id="a35ad-835">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-835">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-836">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-836">10001</span></span></td>
<td><span data-ttu-id="a35ad-837">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-837">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-838">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-838">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-839">236.25</span><span class="sxs-lookup"><span data-stu-id="a35ad-839">236.25</span></span></td>
<td><span data-ttu-id="a35ad-840">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-841">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-841">CC002</span></span></td>
<td><span data-ttu-id="a35ad-842">Financiën</span><span class="sxs-lookup"><span data-stu-id="a35ad-842">Finance</span></span></td>
<td><span data-ttu-id="a35ad-843">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-843">10001</span></span></td>
<td><span data-ttu-id="a35ad-844">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-844">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-845">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-845">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="a35ad-846">-8,150.29</span></span></td>
<td><span data-ttu-id="a35ad-847">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-848">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-848">CC003</span></span></td>
<td><span data-ttu-id="a35ad-849">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-849">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-850">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-850">10001</span></span></td>
<td><span data-ttu-id="a35ad-851">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-851">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-852">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-852">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a35ad-853">5,297.69</span></span></td>
<td><span data-ttu-id="a35ad-854">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-855">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-855">CC004</span></span></td>
<td><span data-ttu-id="a35ad-856">Verpakking</span><span class="sxs-lookup"><span data-stu-id="a35ad-856">Packaging</span></span></td>
<td><span data-ttu-id="a35ad-857">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-857">10001</span></span></td>
<td><span data-ttu-id="a35ad-858">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-858">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-859">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-859">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a35ad-860">2,852.60</span></span></td>
<td><span data-ttu-id="a35ad-861">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-862">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-862">CC003</span></span></td>
<td><span data-ttu-id="a35ad-863">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-863">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-864">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-864">10001</span></span></td>
<td><span data-ttu-id="a35ad-865">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-865">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-866">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-866">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="a35ad-867">-713.75</span></span></td>
<td><span data-ttu-id="a35ad-868">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-869">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-870">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-870">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-871">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-871">10001</span></span></td>
<td><span data-ttu-id="a35ad-872">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-872">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-873">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-873">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-874">535.31</span><span class="sxs-lookup"><span data-stu-id="a35ad-874">535.31</span></span></td>
<td><span data-ttu-id="a35ad-875">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-876">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-877">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-877">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-878">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-878">10001</span></span></td>
<td><span data-ttu-id="a35ad-879">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-879">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-880">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-880">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-881">178.44</span><span class="sxs-lookup"><span data-stu-id="a35ad-881">178.44</span></span></td>
<td><span data-ttu-id="a35ad-882">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-883">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-883">CC003</span></span></td>
<td><span data-ttu-id="a35ad-884">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-884">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-885">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-885">10001</span></span></td>
<td><span data-ttu-id="a35ad-886">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-886">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-887">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-887">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="a35ad-888">-5,982.83</span></span></td>
<td><span data-ttu-id="a35ad-889">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-890">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-891">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-891">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-892">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-892">10001</span></span></td>
<td><span data-ttu-id="a35ad-893">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-893">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-894">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-894">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a35ad-895">4,487.12</span></span></td>
<td><span data-ttu-id="a35ad-896">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-897">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-898">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-898">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-899">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-899">10001</span></span></td>
<td><span data-ttu-id="a35ad-900">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-900">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-901">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-901">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a35ad-902">1,495.71</span></span></td>
<td><span data-ttu-id="a35ad-903">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-904">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-904">CC003</span></span></td>
<td><span data-ttu-id="a35ad-905">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-905">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-906">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-906">10001</span></span></td>
<td><span data-ttu-id="a35ad-907">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-907">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-908">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-908">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="a35ad-909">-286.25</span></span></td>
<td><span data-ttu-id="a35ad-910">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-911">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-912">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-912">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-913">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-913">10001</span></span></td>
<td><span data-ttu-id="a35ad-914">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-914">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-915">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-915">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-916">241.05</span><span class="sxs-lookup"><span data-stu-id="a35ad-916">241.05</span></span></td>
<td><span data-ttu-id="a35ad-917">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-918">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-919">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-919">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-920">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-920">10001</span></span></td>
<td><span data-ttu-id="a35ad-921">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-921">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-922">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-922">Fixed cost</span></span></td>
<td><span data-ttu-id="a35ad-923">45.20</span><span class="sxs-lookup"><span data-stu-id="a35ad-923">45.20</span></span></td>
<td><span data-ttu-id="a35ad-924">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-925">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-925">CC003</span></span></td>
<td><span data-ttu-id="a35ad-926">Assembleren</span><span class="sxs-lookup"><span data-stu-id="a35ad-926">Assembly</span></span></td>
<td><span data-ttu-id="a35ad-927">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-927">10001</span></span></td>
<td><span data-ttu-id="a35ad-928">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-928">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-929">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-929">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="a35ad-930">-2,977.17</span></span></td>
<td><span data-ttu-id="a35ad-931">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-932">Prod 1</span></span></td>
<td><span data-ttu-id="a35ad-933">Product 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-933">Product 1</span></span></td>
<td><span data-ttu-id="a35ad-934">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-934">10001</span></span></td>
<td><span data-ttu-id="a35ad-935">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-935">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-936">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-936">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a35ad-937">2,507.09</span></span></td>
<td><span data-ttu-id="a35ad-938">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a35ad-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-939">Prod 2</span></span></td>
<td><span data-ttu-id="a35ad-940">Product 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-940">Product 2</span></span></td>
<td><span data-ttu-id="a35ad-941">10001</span><span class="sxs-lookup"><span data-stu-id="a35ad-941">10001</span></span></td>
<td><span data-ttu-id="a35ad-942">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-942">Electricity</span></span></td>
<td><span data-ttu-id="a35ad-943">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-943">Variable cost</span></span></td>
<td><span data-ttu-id="a35ad-944">470.08</span><span class="sxs-lookup"><span data-stu-id="a35ad-944">470.08</span></span></td>
<td><span data-ttu-id="a35ad-945">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="a35ad-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="a35ad-946">Conclusie</span><span class="sxs-lookup"><span data-stu-id="a35ad-946">Conclusion</span></span>
<span data-ttu-id="a35ad-947">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="a35ad-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="a35ad-948">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a35ad-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="a35ad-949">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a35ad-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="a35ad-950">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="a35ad-951">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="a35ad-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="a35ad-952">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a35ad-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="a35ad-953">Totaal</span><span class="sxs-lookup"><span data-stu-id="a35ad-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a35ad-954">CC099</span><span class="sxs-lookup"><span data-stu-id="a35ad-954">CC099</span></span></th>
<th><span data-ttu-id="a35ad-955">CC001</span><span class="sxs-lookup"><span data-stu-id="a35ad-955">CC001</span></span></th>
<th><span data-ttu-id="a35ad-956">CC002</span><span class="sxs-lookup"><span data-stu-id="a35ad-956">CC002</span></span></th>
<th><span data-ttu-id="a35ad-957">CC003</span><span class="sxs-lookup"><span data-stu-id="a35ad-957">CC003</span></span></th>
<th><span data-ttu-id="a35ad-958">CC004</span><span class="sxs-lookup"><span data-stu-id="a35ad-958">CC004</span></span></th>
<th><span data-ttu-id="a35ad-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-959">Proj 1</span></span></th>
<th><span data-ttu-id="a35ad-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-960">Proj 2</span></span></th>
<th><span data-ttu-id="a35ad-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a35ad-961">Prod 1</span></span></th>
<th><span data-ttu-id="a35ad-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a35ad-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="a35ad-963">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="a35ad-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="a35ad-973">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="a35ad-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-974">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="a35ad-975">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-976">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-977">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-978">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-979">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-980">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-981">776.36</span><span class="sxs-lookup"><span data-stu-id="a35ad-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-982">223.64</span><span class="sxs-lookup"><span data-stu-id="a35ad-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="a35ad-984">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="a35ad-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-985">000</span><span class="sxs-lookup"><span data-stu-id="a35ad-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-986">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-987">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-988">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-989">0,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-990">30,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-991">10,00</span><span class="sxs-lookup"><span data-stu-id="a35ad-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a35ad-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a35ad-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a35ad-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a35ad-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a35ad-995">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="a35ad-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="a35ad-996">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="a35ad-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="a35ad-997">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="a35ad-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="a35ad-998">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="a35ad-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="a35ad-999">Zie Beleid voor kostenaggregatie voor meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="a35ad-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="a35ad-1000">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="a35ad-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




