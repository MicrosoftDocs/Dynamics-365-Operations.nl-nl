---
title: Overheadberekening
description: In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: nl-nl
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="4e613-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="4e613-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e613-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="4e613-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4e613-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="4e613-105">Term definition</span></span>
---------------

<span data-ttu-id="4e613-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="4e613-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4e613-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="4e613-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4e613-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="4e613-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4e613-109">Huur</span><span class="sxs-lookup"><span data-stu-id="4e613-109">Rent</span></span>
-   <span data-ttu-id="4e613-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-110">Electricity</span></span>
-   <span data-ttu-id="4e613-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="4e613-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4e613-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="4e613-112">Overhead calculation overview</span></span>
<span data-ttu-id="4e613-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4e613-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4e613-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="4e613-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4e613-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="4e613-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4e613-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="4e613-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4e613-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="4e613-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4e613-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="4e613-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4e613-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="4e613-119">Version type</span></span>
-   <span data-ttu-id="4e613-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="4e613-120">Date and time</span></span>
-   <span data-ttu-id="4e613-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="4e613-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4e613-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="4e613-122">Fiscal year</span></span>
-   <span data-ttu-id="4e613-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="4e613-123">Fiscal period</span></span>

<span data-ttu-id="4e613-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4e613-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4e613-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="4e613-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4e613-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4e613-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4e613-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="4e613-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4e613-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="4e613-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4e613-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="4e613-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4e613-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="4e613-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4e613-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4e613-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4e613-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="4e613-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4e613-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="4e613-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4e613-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="4e613-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4e613-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="4e613-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4e613-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="4e613-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4e613-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="4e613-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="4e613-140">Main account</span></span></th>
<th><span data-ttu-id="4e613-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="4e613-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4e613-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-143">CC099</span></span></td>
<td><span data-ttu-id="4e613-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-144">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-145">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-145">10001</span></span></td>
<td><span data-ttu-id="4e613-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-146">Electricity</span></span></td>
<td><span data-ttu-id="4e613-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4e613-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="4e613-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4e613-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="4e613-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4e613-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="4e613-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4e613-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="4e613-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4e613-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="4e613-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4e613-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="4e613-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4e613-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="4e613-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4e613-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="4e613-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4e613-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4e613-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="4e613-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4e613-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="4e613-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4e613-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-160">Journal</span></span></th>
<th><span data-ttu-id="4e613-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e613-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4e613-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e613-163">Versie</span><span class="sxs-lookup"><span data-stu-id="4e613-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-164">00001</span><span class="sxs-lookup"><span data-stu-id="4e613-164">00001</span></span></td>
<td><span data-ttu-id="4e613-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4e613-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="4e613-166">Fiscal</span></span></td>
<td><span data-ttu-id="4e613-167">2017</span><span class="sxs-lookup"><span data-stu-id="4e613-167">2017</span></span></td>
<td><span data-ttu-id="4e613-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4e613-168">Period 1</span></span></td>
<td><span data-ttu-id="4e613-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4e613-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e613-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="4e613-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-173">Cost element</span></span></th>
<th><span data-ttu-id="4e613-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4e613-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4e613-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-177">CC099</span></span></td>
<td><span data-ttu-id="4e613-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-178">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-179">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-179">10001</span></span></td>
<td><span data-ttu-id="4e613-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-180">Electricity</span></span></td>
<td><span data-ttu-id="4e613-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="4e613-181">Unclassified</span></span></td>
<td><span data-ttu-id="4e613-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e613-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="4e613-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-185">Cost element</span></span></th>
<th><span data-ttu-id="4e613-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4e613-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-187">Amount</span></span></th>
<th><span data-ttu-id="4e613-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-189">CC099</span></span></td>
<td><span data-ttu-id="4e613-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-190">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-191">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-191">10001</span></span></td>
<td><span data-ttu-id="4e613-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-192">Electricity</span></span></td>
<td><span data-ttu-id="4e613-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="4e613-193">Unclassified</span></span></td>
<td><span data-ttu-id="4e613-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-194">10,000.00</span></span></td>
<td><span data-ttu-id="4e613-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-196">CC099</span></span></td>
<td><span data-ttu-id="4e613-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-197">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-198">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-198">10001</span></span></td>
<td><span data-ttu-id="4e613-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-199">Electricity</span></span></td>
<td><span data-ttu-id="4e613-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="4e613-200">Unclassified</span></span></td>
<td><span data-ttu-id="4e613-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="4e613-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4e613-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-203">CC099</span></span></td>
<td><span data-ttu-id="4e613-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-204">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-205">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-205">10001</span></span></td>
<td><span data-ttu-id="4e613-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-206">Electricity</span></span></td>
<td><span data-ttu-id="4e613-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-208">1,000.00</span></span></td>
<td><span data-ttu-id="4e613-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-210">CC099</span></span></td>
<td><span data-ttu-id="4e613-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-211">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-212">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-212">10001</span></span></td>
<td><span data-ttu-id="4e613-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-213">Electricity</span></span></td>
<td><span data-ttu-id="4e613-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-214">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-215">9,000.00</span></span></td>
<td><span data-ttu-id="4e613-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4e613-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4e613-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="4e613-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4e613-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="4e613-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4e613-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="4e613-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4e613-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="4e613-221">Define the cost distribution rule</span></span>

<span data-ttu-id="4e613-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="4e613-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4e613-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="4e613-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4e613-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4e613-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4e613-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="4e613-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4e613-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="4e613-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4e613-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="4e613-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-228">Cost object</span></span></th>
<th><span data-ttu-id="4e613-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="4e613-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-230">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-230">CC001</span></span></td>
<td><span data-ttu-id="4e613-231">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-231">HR</span></span></td>
<td><span data-ttu-id="4e613-232">1.000</span><span class="sxs-lookup"><span data-stu-id="4e613-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-233">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-233">CC002</span></span></td>
<td><span data-ttu-id="4e613-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-234">Finance</span></span></td>
<td><span data-ttu-id="4e613-235">6.000</span><span class="sxs-lookup"><span data-stu-id="4e613-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-236">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-236">CC003</span></span></td>
<td><span data-ttu-id="4e613-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-237">Assembly</span></span></td>
<td><span data-ttu-id="4e613-238">0</span><span class="sxs-lookup"><span data-stu-id="4e613-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="4e613-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-240">Cost object</span></span></th>
<th><span data-ttu-id="4e613-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4e613-241">Magnitude</span></span></th>
<th><span data-ttu-id="4e613-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4e613-242">Allocation factor</span></span></th>
<th><span data-ttu-id="4e613-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-244">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-244">CC001</span></span></td>
<td><span data-ttu-id="4e613-245">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-245">HR</span></span></td>
<td><span data-ttu-id="4e613-246">1.000</span><span class="sxs-lookup"><span data-stu-id="4e613-246">1,000</span></span></td>
<td><span data-ttu-id="4e613-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e613-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4e613-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-249">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-249">CC002</span></span></td>
<td><span data-ttu-id="4e613-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-250">Finance</span></span></td>
<td><span data-ttu-id="4e613-251">6.000</span><span class="sxs-lookup"><span data-stu-id="4e613-251">6,000</span></span></td>
<td><span data-ttu-id="4e613-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e613-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4e613-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-254">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-254">CC003</span></span></td>
<td><span data-ttu-id="4e613-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-255">Assembly</span></span></td>
<td><span data-ttu-id="4e613-256">0</span><span class="sxs-lookup"><span data-stu-id="4e613-256">0</span></span></td>
<td><span data-ttu-id="4e613-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e613-258">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="4e613-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4e613-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="4e613-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-261">Cost object</span></span></th>
<th><span data-ttu-id="4e613-262">Formule</span><span class="sxs-lookup"><span data-stu-id="4e613-262">Formula</span></span></th>
<th><span data-ttu-id="4e613-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4e613-263">Magnitude</span></span></th>
<th><span data-ttu-id="4e613-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4e613-264">Allocation factor</span></span></th>
<th><span data-ttu-id="4e613-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-266">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-266">CC001</span></span></td>
<td><span data-ttu-id="4e613-267">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-267">HR</span></span></td>
<td><span data-ttu-id="4e613-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4e613-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e613-269">1</span><span class="sxs-lookup"><span data-stu-id="4e613-269">1</span></span></td>
<td><span data-ttu-id="4e613-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e613-271">500,00</span><span class="sxs-lookup"><span data-stu-id="4e613-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-272">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-272">CC002</span></span></td>
<td><span data-ttu-id="4e613-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-273">Finance</span></span></td>
<td><span data-ttu-id="4e613-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4e613-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e613-275">1</span><span class="sxs-lookup"><span data-stu-id="4e613-275">1</span></span></td>
<td><span data-ttu-id="4e613-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e613-277">500,00</span><span class="sxs-lookup"><span data-stu-id="4e613-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-278">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-278">CC003</span></span></td>
<td><span data-ttu-id="4e613-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-279">Assembly</span></span></td>
<td><span data-ttu-id="4e613-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4e613-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e613-281">0</span><span class="sxs-lookup"><span data-stu-id="4e613-281">0</span></span></td>
<td><span data-ttu-id="4e613-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e613-283">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4e613-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-285">Journal</span></span></th>
<th><span data-ttu-id="4e613-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e613-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4e613-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e613-288">Versie</span><span class="sxs-lookup"><span data-stu-id="4e613-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-289">00002</span><span class="sxs-lookup"><span data-stu-id="4e613-289">00002</span></span></td>
<td><span data-ttu-id="4e613-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="4e613-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4e613-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="4e613-291">Fiscal</span></span></td>
<td><span data-ttu-id="4e613-292">2017</span><span class="sxs-lookup"><span data-stu-id="4e613-292">2017</span></span></td>
<td><span data-ttu-id="4e613-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4e613-293">Period 1</span></span></td>
<td><span data-ttu-id="4e613-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4e613-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e613-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="4e613-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-298">Cost element</span></span></th>
<th><span data-ttu-id="4e613-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-299">Cost behavior</span></span></th>
<th><span data-ttu-id="4e613-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-302">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-302">CC099</span></span></td>
<td><span data-ttu-id="4e613-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-303">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-304">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-304">10001</span></span></td>
<td><span data-ttu-id="4e613-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-305">Electricity</span></span></td>
<td><span data-ttu-id="4e613-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-306">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-309">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-309">CC099</span></span></td>
<td><span data-ttu-id="4e613-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-310">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-311">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-311">10001</span></span></td>
<td><span data-ttu-id="4e613-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-312">Electricity</span></span></td>
<td><span data-ttu-id="4e613-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-313">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e613-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="4e613-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-317">Cost element</span></span></th>
<th><span data-ttu-id="4e613-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-318">Cost behavior</span></span></th>
<th><span data-ttu-id="4e613-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-319">Amount</span></span></th>
<th><span data-ttu-id="4e613-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-321">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-321">CC099</span></span></td>
<td><span data-ttu-id="4e613-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-322">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-323">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-323">10001</span></span></td>
<td><span data-ttu-id="4e613-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-324">Electricity</span></span></td>
<td><span data-ttu-id="4e613-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-325">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="4e613-326">-1,000.00</span></span></td>
<td><span data-ttu-id="4e613-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-328">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-328">CC001</span></span></td>
<td><span data-ttu-id="4e613-329">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-329">HR</span></span></td>
<td><span data-ttu-id="4e613-330">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-330">10001</span></span></td>
<td><span data-ttu-id="4e613-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-331">Electricity</span></span></td>
<td><span data-ttu-id="4e613-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-332">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-333">500,00</span><span class="sxs-lookup"><span data-stu-id="4e613-333">500.00</span></span></td>
<td><span data-ttu-id="4e613-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-335">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-335">CC002</span></span></td>
<td><span data-ttu-id="4e613-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-336">Finance</span></span></td>
<td><span data-ttu-id="4e613-337">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-337">10001</span></span></td>
<td><span data-ttu-id="4e613-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-338">Electricity</span></span></td>
<td><span data-ttu-id="4e613-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-339">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-340">500,00</span><span class="sxs-lookup"><span data-stu-id="4e613-340">500.00</span></span></td>
<td><span data-ttu-id="4e613-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-342">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-342">CC099</span></span></td>
<td><span data-ttu-id="4e613-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="4e613-343">Default cost center</span></span></td>
<td><span data-ttu-id="4e613-344">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-344">10001</span></span></td>
<td><span data-ttu-id="4e613-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-345">Electricity</span></span></td>
<td><span data-ttu-id="4e613-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-346">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e613-347">-9,000.00</span></span></td>
<td><span data-ttu-id="4e613-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-349">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-349">CC001</span></span></td>
<td><span data-ttu-id="4e613-350">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-350">HR</span></span></td>
<td><span data-ttu-id="4e613-351">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-351">10001</span></span></td>
<td><span data-ttu-id="4e613-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-352">Electricity</span></span></td>
<td><span data-ttu-id="4e613-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-353">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4e613-354">1,285.71</span></span></td>
<td><span data-ttu-id="4e613-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-356">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-356">CC002</span></span></td>
<td><span data-ttu-id="4e613-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-357">Finance</span></span></td>
<td><span data-ttu-id="4e613-358">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-358">10001</span></span></td>
<td><span data-ttu-id="4e613-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-359">Electricity</span></span></td>
<td><span data-ttu-id="4e613-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-360">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4e613-361">7,714.29</span></span></td>
<td><span data-ttu-id="4e613-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4e613-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4e613-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="4e613-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4e613-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="4e613-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4e613-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="4e613-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4e613-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="4e613-367">Define the overhead rate</span></span>

<span data-ttu-id="4e613-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="4e613-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4e613-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4e613-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-370">Cost object</span></span></th>
<th><span data-ttu-id="4e613-371">Uren</span><span class="sxs-lookup"><span data-stu-id="4e613-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e613-372">Proj 1</span></span></td>
<td><span data-ttu-id="4e613-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="4e613-373">Project 1</span></span></td>
<td><span data-ttu-id="4e613-374">3</span><span class="sxs-lookup"><span data-stu-id="4e613-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e613-375">Proj 2</span></span></td>
<td><span data-ttu-id="4e613-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="4e613-376">Project 2</span></span></td>
<td><span data-ttu-id="4e613-377">1</span><span class="sxs-lookup"><span data-stu-id="4e613-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="4e613-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-379">Cost object</span></span></th>
<th><span data-ttu-id="4e613-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-380">Cost element</span></span></th>
<th><span data-ttu-id="4e613-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-381">Cost behavior</span></span></th>
<th><span data-ttu-id="4e613-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="4e613-382">Units</span></span></th>
<th><span data-ttu-id="4e613-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="4e613-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-384">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-384">CC001</span></span></td>
<td><span data-ttu-id="4e613-385">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-385">HR</span></span></td>
<td><span data-ttu-id="4e613-386">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-386">10001</span></span></td>
<td><span data-ttu-id="4e613-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-387">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-388">1</span><span class="sxs-lookup"><span data-stu-id="4e613-388">1</span></span></td>
<td><span data-ttu-id="4e613-389">10</span><span class="sxs-lookup"><span data-stu-id="4e613-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="4e613-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-391">Cost object</span></span></th>
<th><span data-ttu-id="4e613-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4e613-392">Magnitude</span></span></th>
<th><span data-ttu-id="4e613-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-393">Cost element</span></span></th>
<th><span data-ttu-id="4e613-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4e613-394">Allocation factor</span></span></th>
<th><span data-ttu-id="4e613-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e613-396">Proj 1</span></span></td>
<td><span data-ttu-id="4e613-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="4e613-397">Project 1</span></span></td>
<td><span data-ttu-id="4e613-398">3</span><span class="sxs-lookup"><span data-stu-id="4e613-398">3</span></span></td>
<td><span data-ttu-id="4e613-399">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-399">10001</span></span></td>
<td><span data-ttu-id="4e613-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4e613-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4e613-401">30,00</span><span class="sxs-lookup"><span data-stu-id="4e613-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e613-402">Proj 2</span></span></td>
<td><span data-ttu-id="4e613-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="4e613-403">Project 2</span></span></td>
<td><span data-ttu-id="4e613-404">1</span><span class="sxs-lookup"><span data-stu-id="4e613-404">1</span></span></td>
<td><span data-ttu-id="4e613-405">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-405">10001</span></span></td>
<td><span data-ttu-id="4e613-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4e613-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4e613-407">10,00</span><span class="sxs-lookup"><span data-stu-id="4e613-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4e613-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-409">Journal</span></span></th>
<th><span data-ttu-id="4e613-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e613-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4e613-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e613-412">Versie</span><span class="sxs-lookup"><span data-stu-id="4e613-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-413">00003</span><span class="sxs-lookup"><span data-stu-id="4e613-413">00003</span></span></td>
<td><span data-ttu-id="4e613-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="4e613-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4e613-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="4e613-415">Fiscal</span></span></td>
<td><span data-ttu-id="4e613-416">2017</span><span class="sxs-lookup"><span data-stu-id="4e613-416">2017</span></span></td>
<td><span data-ttu-id="4e613-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4e613-417">Period 1</span></span></td>
<td><span data-ttu-id="4e613-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4e613-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4e613-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="4e613-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-421">Cost object</span></span></th>
<th><span data-ttu-id="4e613-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4e613-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e613-424">Proj 1</span></span></td>
<td><span data-ttu-id="4e613-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="4e613-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4e613-426">3,00</span><span class="sxs-lookup"><span data-stu-id="4e613-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e613-428">Proj 2</span></span></td>
<td><span data-ttu-id="4e613-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="4e613-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4e613-430">1,00</span><span class="sxs-lookup"><span data-stu-id="4e613-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e613-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="4e613-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-433">Cost element</span></span></th>
<th><span data-ttu-id="4e613-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-434">Cost behavior</span></span></th>
<th><span data-ttu-id="4e613-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-435">Amount</span></span></th>
<th><span data-ttu-id="4e613-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="4e613-437">CC0001</span></span></td>
<td><span data-ttu-id="4e613-438">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-438">HR</span></span></td>
<td><span data-ttu-id="4e613-439">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-439">10001</span></span></td>
<td><span data-ttu-id="4e613-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-440">Electricity</span></span></td>
<td><span data-ttu-id="4e613-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-441">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="4e613-442">-30.00</span></span></td>
<td><span data-ttu-id="4e613-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e613-444">Proj 1</span></span></td>
<td><span data-ttu-id="4e613-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="4e613-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4e613-446">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-446">10001</span></span></td>
<td><span data-ttu-id="4e613-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-447">Electricity</span></span></td>
<td><span data-ttu-id="4e613-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-448">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-449">30,00</span><span class="sxs-lookup"><span data-stu-id="4e613-449">30.00</span></span></td>
<td><span data-ttu-id="4e613-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-451">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-451">CC001</span></span></td>
<td><span data-ttu-id="4e613-452">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-452">HR</span></span></td>
<td><span data-ttu-id="4e613-453">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-453">10001</span></span></td>
<td><span data-ttu-id="4e613-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-454">Electricity</span></span></td>
<td><span data-ttu-id="4e613-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-455">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="4e613-456">-10.00</span></span></td>
<td><span data-ttu-id="4e613-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e613-458">Proj 2</span></span></td>
<td><span data-ttu-id="4e613-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="4e613-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4e613-460">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-460">10001</span></span></td>
<td><span data-ttu-id="4e613-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-461">Electricity</span></span></td>
<td><span data-ttu-id="4e613-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-462">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-463">10.00</span><span class="sxs-lookup"><span data-stu-id="4e613-463">10.00</span></span></td>
<td><span data-ttu-id="4e613-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="4e613-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4e613-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="4e613-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4e613-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="4e613-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4e613-468">Finance and Operations ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="4e613-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="4e613-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="4e613-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4e613-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="4e613-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4e613-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="4e613-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4e613-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="4e613-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4e613-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="4e613-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4e613-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4e613-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4e613-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="4e613-475">Define the cost allocation</span></span>

<span data-ttu-id="4e613-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="4e613-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4e613-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4e613-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4e613-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4e613-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-479">Cost object</span></span></th>
<th><span data-ttu-id="4e613-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="4e613-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-481">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-481">CC002</span></span></td>
<td><span data-ttu-id="4e613-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-482">Finance</span></span></td>
<td><span data-ttu-id="4e613-483">35</span><span class="sxs-lookup"><span data-stu-id="4e613-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-484">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-484">CC003</span></span></td>
<td><span data-ttu-id="4e613-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-485">Assembly</span></span></td>
<td><span data-ttu-id="4e613-486">55</span><span class="sxs-lookup"><span data-stu-id="4e613-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-487">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-487">CC004</span></span></td>
<td><span data-ttu-id="4e613-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-488">Packaging</span></span></td>
<td><span data-ttu-id="4e613-489">10</span><span class="sxs-lookup"><span data-stu-id="4e613-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4e613-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4e613-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4e613-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-492">Cost object</span></span></th>
<th><span data-ttu-id="4e613-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="4e613-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-494">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-494">CC003</span></span></td>
<td><span data-ttu-id="4e613-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-495">Assembly</span></span></td>
<td><span data-ttu-id="4e613-496">65</span><span class="sxs-lookup"><span data-stu-id="4e613-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-497">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-497">CC004</span></span></td>
<td><span data-ttu-id="4e613-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-498">Packaging</span></span></td>
<td><span data-ttu-id="4e613-499">35</span><span class="sxs-lookup"><span data-stu-id="4e613-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4e613-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4e613-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4e613-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-502">Cost object</span></span></th>
<th><span data-ttu-id="4e613-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="4e613-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-504">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-505">Product 1</span></span></td>
<td><span data-ttu-id="4e613-506">60</span><span class="sxs-lookup"><span data-stu-id="4e613-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-507">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-508">Product 2</span></span></td>
<td><span data-ttu-id="4e613-509">20</span><span class="sxs-lookup"><span data-stu-id="4e613-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="4e613-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4e613-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="4e613-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-512">Cost object</span></span></th>
<th><span data-ttu-id="4e613-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="4e613-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-514">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-515">Product 1</span></span></td>
<td><span data-ttu-id="4e613-516">80</span><span class="sxs-lookup"><span data-stu-id="4e613-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-517">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-518">Product 2</span></span></td>
<td><span data-ttu-id="4e613-519">15</span><span class="sxs-lookup"><span data-stu-id="4e613-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4e613-520">In Finance and Operations kunnen statistische metingen, zoals de productie-uren die een product verbruikt, worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="4e613-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4e613-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4e613-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="4e613-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="4e613-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-523">Cost object</span></span></th>
<th><span data-ttu-id="4e613-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4e613-524">Magnitude</span></span></th>
<th><span data-ttu-id="4e613-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4e613-525">Allocation factor</span></span></th>
<th><span data-ttu-id="4e613-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-526">Amount</span></span></th>
<th><span data-ttu-id="4e613-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-528">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-528">CC002</span></span></td>
<td><span data-ttu-id="4e613-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-529">Finance</span></span></td>
<td><span data-ttu-id="4e613-530">35</span><span class="sxs-lookup"><span data-stu-id="4e613-530">35</span></span></td>
<td><span data-ttu-id="4e613-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4e613-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e613-532">175.00</span><span class="sxs-lookup"><span data-stu-id="4e613-532">175.00</span></span></td>
<td><span data-ttu-id="4e613-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-534">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-534">CC003</span></span></td>
<td><span data-ttu-id="4e613-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-535">Assembly</span></span></td>
<td><span data-ttu-id="4e613-536">55</span><span class="sxs-lookup"><span data-stu-id="4e613-536">55</span></span></td>
<td><span data-ttu-id="4e613-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4e613-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e613-538">275.00</span><span class="sxs-lookup"><span data-stu-id="4e613-538">275.00</span></span></td>
<td><span data-ttu-id="4e613-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-540">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-540">CC004</span></span></td>
<td><span data-ttu-id="4e613-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-541">Packaging</span></span></td>
<td><span data-ttu-id="4e613-542">10</span><span class="sxs-lookup"><span data-stu-id="4e613-542">10</span></span></td>
<td><span data-ttu-id="4e613-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4e613-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e613-544">50,00</span><span class="sxs-lookup"><span data-stu-id="4e613-544">50.00</span></span></td>
<td><span data-ttu-id="4e613-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-546">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-546">CC002</span></span></td>
<td><span data-ttu-id="4e613-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-547">Finance</span></span></td>
<td><span data-ttu-id="4e613-548">35</span><span class="sxs-lookup"><span data-stu-id="4e613-548">35</span></span></td>
<td><span data-ttu-id="4e613-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4e613-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e613-550">436.00</span><span class="sxs-lookup"><span data-stu-id="4e613-550">436.00</span></span></td>
<td><span data-ttu-id="4e613-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-552">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-552">CC003</span></span></td>
<td><span data-ttu-id="4e613-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-553">Assembly</span></span></td>
<td><span data-ttu-id="4e613-554">55</span><span class="sxs-lookup"><span data-stu-id="4e613-554">55</span></span></td>
<td><span data-ttu-id="4e613-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4e613-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e613-556">685.14</span><span class="sxs-lookup"><span data-stu-id="4e613-556">685.14</span></span></td>
<td><span data-ttu-id="4e613-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-558">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-558">CC004</span></span></td>
<td><span data-ttu-id="4e613-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-559">Packaging</span></span></td>
<td><span data-ttu-id="4e613-560">10</span><span class="sxs-lookup"><span data-stu-id="4e613-560">10</span></span></td>
<td><span data-ttu-id="4e613-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4e613-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e613-562">124.57</span><span class="sxs-lookup"><span data-stu-id="4e613-562">124.57</span></span></td>
<td><span data-ttu-id="4e613-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="4e613-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-565">Cost object</span></span></th>
<th><span data-ttu-id="4e613-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4e613-566">Magnitude</span></span></th>
<th><span data-ttu-id="4e613-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4e613-567">Allocation factor</span></span></th>
<th><span data-ttu-id="4e613-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-568">Amount</span></span></th>
<th><span data-ttu-id="4e613-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-570">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-570">CC003</span></span></td>
<td><span data-ttu-id="4e613-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-571">Assembly</span></span></td>
<td><span data-ttu-id="4e613-572">65</span><span class="sxs-lookup"><span data-stu-id="4e613-572">65</span></span></td>
<td><span data-ttu-id="4e613-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4e613-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4e613-574">438.75</span><span class="sxs-lookup"><span data-stu-id="4e613-574">438.75</span></span></td>
<td><span data-ttu-id="4e613-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-576">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-576">CC004</span></span></td>
<td><span data-ttu-id="4e613-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-577">Packaging</span></span></td>
<td><span data-ttu-id="4e613-578">35</span><span class="sxs-lookup"><span data-stu-id="4e613-578">35</span></span></td>
<td><span data-ttu-id="4e613-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4e613-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4e613-580">236.25</span><span class="sxs-lookup"><span data-stu-id="4e613-580">236.25</span></span></td>
<td><span data-ttu-id="4e613-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-582">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-582">CC003</span></span></td>
<td><span data-ttu-id="4e613-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-583">Assembly</span></span></td>
<td><span data-ttu-id="4e613-584">65</span><span class="sxs-lookup"><span data-stu-id="4e613-584">65</span></span></td>
<td><span data-ttu-id="4e613-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4e613-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4e613-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4e613-586">5,297.69</span></span></td>
<td><span data-ttu-id="4e613-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-588">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-588">CC004</span></span></td>
<td><span data-ttu-id="4e613-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-589">Packaging</span></span></td>
<td><span data-ttu-id="4e613-590">35</span><span class="sxs-lookup"><span data-stu-id="4e613-590">35</span></span></td>
<td><span data-ttu-id="4e613-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4e613-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4e613-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4e613-592">2,852.60</span></span></td>
<td><span data-ttu-id="4e613-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="4e613-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-595">Cost object</span></span></th>
<th><span data-ttu-id="4e613-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4e613-596">Magnitude</span></span></th>
<th><span data-ttu-id="4e613-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4e613-597">Allocation factor</span></span></th>
<th><span data-ttu-id="4e613-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-598">Amount</span></span></th>
<th><span data-ttu-id="4e613-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-600">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-601">Product 1</span></span></td>
<td><span data-ttu-id="4e613-602">60</span><span class="sxs-lookup"><span data-stu-id="4e613-602">60</span></span></td>
<td><span data-ttu-id="4e613-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4e613-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4e613-604">535.31</span><span class="sxs-lookup"><span data-stu-id="4e613-604">535.31</span></span></td>
<td><span data-ttu-id="4e613-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-606">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-607">Product 2</span></span></td>
<td><span data-ttu-id="4e613-608">20</span><span class="sxs-lookup"><span data-stu-id="4e613-608">20</span></span></td>
<td><span data-ttu-id="4e613-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4e613-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4e613-610">178.44</span><span class="sxs-lookup"><span data-stu-id="4e613-610">178.44</span></span></td>
<td><span data-ttu-id="4e613-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-612">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-613">Product 1</span></span></td>
<td><span data-ttu-id="4e613-614">60</span><span class="sxs-lookup"><span data-stu-id="4e613-614">60</span></span></td>
<td><span data-ttu-id="4e613-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4e613-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4e613-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4e613-616">4,487.12</span></span></td>
<td><span data-ttu-id="4e613-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-618">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-619">Product 2</span></span></td>
<td><span data-ttu-id="4e613-620">20</span><span class="sxs-lookup"><span data-stu-id="4e613-620">20</span></span></td>
<td><span data-ttu-id="4e613-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4e613-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4e613-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4e613-622">1,495.71</span></span></td>
<td><span data-ttu-id="4e613-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e613-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="4e613-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-625">Cost object</span></span></th>
<th><span data-ttu-id="4e613-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="4e613-626">Magnitude</span></span></th>
<th><span data-ttu-id="4e613-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="4e613-627">Allocation factor</span></span></th>
<th><span data-ttu-id="4e613-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-628">Amount</span></span></th>
<th><span data-ttu-id="4e613-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-630">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-631">Product 1</span></span></td>
<td><span data-ttu-id="4e613-632">80</span><span class="sxs-lookup"><span data-stu-id="4e613-632">80</span></span></td>
<td><span data-ttu-id="4e613-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4e613-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4e613-634">241.05</span><span class="sxs-lookup"><span data-stu-id="4e613-634">241.05</span></span></td>
<td><span data-ttu-id="4e613-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-636">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-637">Product 2</span></span></td>
<td><span data-ttu-id="4e613-638">15</span><span class="sxs-lookup"><span data-stu-id="4e613-638">15</span></span></td>
<td><span data-ttu-id="4e613-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4e613-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4e613-640">45.20</span><span class="sxs-lookup"><span data-stu-id="4e613-640">45.20</span></span></td>
<td><span data-ttu-id="4e613-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-642">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-643">Product 1</span></span></td>
<td><span data-ttu-id="4e613-644">80</span><span class="sxs-lookup"><span data-stu-id="4e613-644">80</span></span></td>
<td><span data-ttu-id="4e613-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4e613-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4e613-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4e613-646">2,507.09</span></span></td>
<td><span data-ttu-id="4e613-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-648">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-649">Product 2</span></span></td>
<td><span data-ttu-id="4e613-650">15</span><span class="sxs-lookup"><span data-stu-id="4e613-650">15</span></span></td>
<td><span data-ttu-id="4e613-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4e613-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4e613-652">470.08</span><span class="sxs-lookup"><span data-stu-id="4e613-652">470.08</span></span></td>
<td><span data-ttu-id="4e613-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e613-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="4e613-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-655">Journal</span></span></th>
<th><span data-ttu-id="4e613-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="4e613-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e613-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="4e613-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e613-658">Versie</span><span class="sxs-lookup"><span data-stu-id="4e613-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-659">00004</span><span class="sxs-lookup"><span data-stu-id="4e613-659">00004</span></span></td>
<td><span data-ttu-id="4e613-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="4e613-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4e613-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="4e613-661">Fiscal</span></span></td>
<td><span data-ttu-id="4e613-662">2017</span><span class="sxs-lookup"><span data-stu-id="4e613-662">2017</span></span></td>
<td><span data-ttu-id="4e613-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="4e613-663">Period 1</span></span></td>
<td><span data-ttu-id="4e613-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="4e613-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4e613-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="4e613-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e613-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-668">Cost element</span></span></th>
<th><span data-ttu-id="4e613-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-669">Cost behavior</span></span></th>
<th><span data-ttu-id="4e613-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-672">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-672">CC001</span></span></td>
<td><span data-ttu-id="4e613-673">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-673">HR</span></span></td>
<td><span data-ttu-id="4e613-674">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-674">10001</span></span></td>
<td><span data-ttu-id="4e613-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-675">Electricity</span></span></td>
<td><span data-ttu-id="4e613-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-676">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-677">500,00</span><span class="sxs-lookup"><span data-stu-id="4e613-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-679">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-679">CC001</span></span></td>
<td><span data-ttu-id="4e613-680">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-680">HR</span></span></td>
<td><span data-ttu-id="4e613-681">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-681">10001</span></span></td>
<td><span data-ttu-id="4e613-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-682">Electricity</span></span></td>
<td><span data-ttu-id="4e613-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-683">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4e613-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-686">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-686">CC002</span></span></td>
<td><span data-ttu-id="4e613-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-687">Finance</span></span></td>
<td><span data-ttu-id="4e613-688">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-688">10001</span></span></td>
<td><span data-ttu-id="4e613-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-689">Electricity</span></span></td>
<td><span data-ttu-id="4e613-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-690">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-691">675.00</span><span class="sxs-lookup"><span data-stu-id="4e613-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-693">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-693">CC002</span></span></td>
<td><span data-ttu-id="4e613-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-694">Finance</span></span></td>
<td><span data-ttu-id="4e613-695">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-695">10001</span></span></td>
<td><span data-ttu-id="4e613-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-696">Electricity</span></span></td>
<td><span data-ttu-id="4e613-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-697">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4e613-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-700">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-700">CC003</span></span></td>
<td><span data-ttu-id="4e613-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-701">Assembly</span></span></td>
<td><span data-ttu-id="4e613-702">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-702">10001</span></span></td>
<td><span data-ttu-id="4e613-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-703">Electricity</span></span></td>
<td><span data-ttu-id="4e613-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-704">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-705">713.75</span><span class="sxs-lookup"><span data-stu-id="4e613-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-707">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-707">CC003</span></span></td>
<td><span data-ttu-id="4e613-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-708">Assembly</span></span></td>
<td><span data-ttu-id="4e613-709">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-709">10001</span></span></td>
<td><span data-ttu-id="4e613-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-710">Electricity</span></span></td>
<td><span data-ttu-id="4e613-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-711">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4e613-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-714">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-714">CC003</span></span></td>
<td><span data-ttu-id="4e613-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-715">Packaging</span></span></td>
<td><span data-ttu-id="4e613-716">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-716">10001</span></span></td>
<td><span data-ttu-id="4e613-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-717">Electricity</span></span></td>
<td><span data-ttu-id="4e613-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-718">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-719">286.25</span><span class="sxs-lookup"><span data-stu-id="4e613-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-721">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-721">CC003</span></span></td>
<td><span data-ttu-id="4e613-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-722">Packaging</span></span></td>
<td><span data-ttu-id="4e613-723">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-723">10001</span></span></td>
<td><span data-ttu-id="4e613-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-724">Electricity</span></span></td>
<td><span data-ttu-id="4e613-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-725">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4e613-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-728">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-729">Product 1</span></span></td>
<td><span data-ttu-id="4e613-730">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-730">10001</span></span></td>
<td><span data-ttu-id="4e613-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-731">Electricity</span></span></td>
<td><span data-ttu-id="4e613-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-732">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-733">776.36</span><span class="sxs-lookup"><span data-stu-id="4e613-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-735">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-736">Product 1</span></span></td>
<td><span data-ttu-id="4e613-737">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-737">10001</span></span></td>
<td><span data-ttu-id="4e613-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-738">Electricity</span></span></td>
<td><span data-ttu-id="4e613-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-739">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4e613-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-742">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-743">Product 1</span></span></td>
<td><span data-ttu-id="4e613-744">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-744">10001</span></span></td>
<td><span data-ttu-id="4e613-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-745">Electricity</span></span></td>
<td><span data-ttu-id="4e613-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-746">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-747">223.64</span><span class="sxs-lookup"><span data-stu-id="4e613-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e613-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-749">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-750">Product 1</span></span></td>
<td><span data-ttu-id="4e613-751">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-751">10001</span></span></td>
<td><span data-ttu-id="4e613-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-752">Electricity</span></span></td>
<td><span data-ttu-id="4e613-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-753">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4e613-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e613-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="4e613-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e613-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e613-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-757">Cost element</span></span></th>
<th><span data-ttu-id="4e613-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-758">Cost behavior</span></span></th>
<th><span data-ttu-id="4e613-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4e613-759">Amount</span></span></th>
<th><span data-ttu-id="4e613-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="4e613-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e613-761">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-761">CC001</span></span></td>
<td><span data-ttu-id="4e613-762">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-762">HR</span></span></td>
<td><span data-ttu-id="4e613-763">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-763">10001</span></span></td>
<td><span data-ttu-id="4e613-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-764">Electricity</span></span></td>
<td><span data-ttu-id="4e613-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-765">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="4e613-766">-500.00</span></span></td>
<td><span data-ttu-id="4e613-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-768">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-768">CC002</span></span></td>
<td><span data-ttu-id="4e613-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-769">Finance</span></span></td>
<td><span data-ttu-id="4e613-770">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-770">10001</span></span></td>
<td><span data-ttu-id="4e613-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-771">Electricity</span></span></td>
<td><span data-ttu-id="4e613-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-772">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-773">175.00</span><span class="sxs-lookup"><span data-stu-id="4e613-773">175.00</span></span></td>
<td><span data-ttu-id="4e613-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-775">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-775">CC003</span></span></td>
<td><span data-ttu-id="4e613-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-776">Assembly</span></span></td>
<td><span data-ttu-id="4e613-777">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-777">10001</span></span></td>
<td><span data-ttu-id="4e613-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-778">Electricity</span></span></td>
<td><span data-ttu-id="4e613-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-779">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-780">275.00</span><span class="sxs-lookup"><span data-stu-id="4e613-780">275.00</span></span></td>
<td><span data-ttu-id="4e613-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-782">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-782">CC004</span></span></td>
<td><span data-ttu-id="4e613-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-783">Packaging</span></span></td>
<td><span data-ttu-id="4e613-784">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-784">10001</span></span></td>
<td><span data-ttu-id="4e613-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-785">Electricity</span></span></td>
<td><span data-ttu-id="4e613-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-786">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-787">50,00</span><span class="sxs-lookup"><span data-stu-id="4e613-787">50,00</span></span></td>
<td><span data-ttu-id="4e613-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-789">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-789">CC001</span></span></td>
<td><span data-ttu-id="4e613-790">HR</span><span class="sxs-lookup"><span data-stu-id="4e613-790">HR</span></span></td>
<td><span data-ttu-id="4e613-791">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-791">10001</span></span></td>
<td><span data-ttu-id="4e613-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-792">Electricity</span></span></td>
<td><span data-ttu-id="4e613-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-793">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="4e613-794">-1,245.71</span></span></td>
<td><span data-ttu-id="4e613-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-796">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-796">CC002</span></span></td>
<td><span data-ttu-id="4e613-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-797">Finance</span></span></td>
<td><span data-ttu-id="4e613-798">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-798">10001</span></span></td>
<td><span data-ttu-id="4e613-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-799">Electricity</span></span></td>
<td><span data-ttu-id="4e613-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-800">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-801">436.00</span><span class="sxs-lookup"><span data-stu-id="4e613-801">436.00</span></span></td>
<td><span data-ttu-id="4e613-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-803">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-803">CC003</span></span></td>
<td><span data-ttu-id="4e613-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-804">Assembly</span></span></td>
<td><span data-ttu-id="4e613-805">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-805">10001</span></span></td>
<td><span data-ttu-id="4e613-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-806">Electricity</span></span></td>
<td><span data-ttu-id="4e613-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-807">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-808">685.14</span><span class="sxs-lookup"><span data-stu-id="4e613-808">685.14</span></span></td>
<td><span data-ttu-id="4e613-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-810">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-810">CC004</span></span></td>
<td><span data-ttu-id="4e613-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-811">Packaging</span></span></td>
<td><span data-ttu-id="4e613-812">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-812">10001</span></span></td>
<td><span data-ttu-id="4e613-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-813">Electricity</span></span></td>
<td><span data-ttu-id="4e613-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-814">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-815">124.57</span><span class="sxs-lookup"><span data-stu-id="4e613-815">124.57</span></span></td>
<td><span data-ttu-id="4e613-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-817">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-817">CC002</span></span></td>
<td><span data-ttu-id="4e613-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-818">Finance</span></span></td>
<td><span data-ttu-id="4e613-819">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-819">10001</span></span></td>
<td><span data-ttu-id="4e613-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-820">Electricity</span></span></td>
<td><span data-ttu-id="4e613-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-821">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="4e613-822">-675.00</span></span></td>
<td><span data-ttu-id="4e613-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-824">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-824">CC003</span></span></td>
<td><span data-ttu-id="4e613-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-825">Assembly</span></span></td>
<td><span data-ttu-id="4e613-826">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-826">10001</span></span></td>
<td><span data-ttu-id="4e613-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-827">Electricity</span></span></td>
<td><span data-ttu-id="4e613-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-828">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-829">438.75</span><span class="sxs-lookup"><span data-stu-id="4e613-829">438.75</span></span></td>
<td><span data-ttu-id="4e613-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-831">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-831">CC004</span></span></td>
<td><span data-ttu-id="4e613-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-832">Packaging</span></span></td>
<td><span data-ttu-id="4e613-833">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-833">10001</span></span></td>
<td><span data-ttu-id="4e613-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-834">Electricity</span></span></td>
<td><span data-ttu-id="4e613-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-835">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-836">236.25</span><span class="sxs-lookup"><span data-stu-id="4e613-836">236.25</span></span></td>
<td><span data-ttu-id="4e613-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-838">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-838">CC002</span></span></td>
<td><span data-ttu-id="4e613-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e613-839">Finance</span></span></td>
<td><span data-ttu-id="4e613-840">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-840">10001</span></span></td>
<td><span data-ttu-id="4e613-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-841">Electricity</span></span></td>
<td><span data-ttu-id="4e613-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-842">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="4e613-843">-8,150.29</span></span></td>
<td><span data-ttu-id="4e613-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-845">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-845">CC003</span></span></td>
<td><span data-ttu-id="4e613-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-846">Assembly</span></span></td>
<td><span data-ttu-id="4e613-847">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-847">10001</span></span></td>
<td><span data-ttu-id="4e613-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-848">Electricity</span></span></td>
<td><span data-ttu-id="4e613-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-849">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4e613-850">5,297.69</span></span></td>
<td><span data-ttu-id="4e613-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-852">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-852">CC004</span></span></td>
<td><span data-ttu-id="4e613-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="4e613-853">Packaging</span></span></td>
<td><span data-ttu-id="4e613-854">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-854">10001</span></span></td>
<td><span data-ttu-id="4e613-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-855">Electricity</span></span></td>
<td><span data-ttu-id="4e613-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-856">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4e613-857">2,852.60</span></span></td>
<td><span data-ttu-id="4e613-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-859">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-859">CC003</span></span></td>
<td><span data-ttu-id="4e613-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-860">Assembly</span></span></td>
<td><span data-ttu-id="4e613-861">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-861">10001</span></span></td>
<td><span data-ttu-id="4e613-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-862">Electricity</span></span></td>
<td><span data-ttu-id="4e613-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-863">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="4e613-864">-713.75</span></span></td>
<td><span data-ttu-id="4e613-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-866">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-867">Product 1</span></span></td>
<td><span data-ttu-id="4e613-868">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-868">10001</span></span></td>
<td><span data-ttu-id="4e613-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-869">Electricity</span></span></td>
<td><span data-ttu-id="4e613-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-870">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-871">535.31</span><span class="sxs-lookup"><span data-stu-id="4e613-871">535.31</span></span></td>
<td><span data-ttu-id="4e613-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-873">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-874">Product 2</span></span></td>
<td><span data-ttu-id="4e613-875">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-875">10001</span></span></td>
<td><span data-ttu-id="4e613-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-876">Electricity</span></span></td>
<td><span data-ttu-id="4e613-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-877">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-878">178.44</span><span class="sxs-lookup"><span data-stu-id="4e613-878">178.44</span></span></td>
<td><span data-ttu-id="4e613-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-880">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-880">CC003</span></span></td>
<td><span data-ttu-id="4e613-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-881">Assembly</span></span></td>
<td><span data-ttu-id="4e613-882">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-882">10001</span></span></td>
<td><span data-ttu-id="4e613-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-883">Electricity</span></span></td>
<td><span data-ttu-id="4e613-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-884">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="4e613-885">-5,982.83</span></span></td>
<td><span data-ttu-id="4e613-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-887">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-888">Product 1</span></span></td>
<td><span data-ttu-id="4e613-889">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-889">10001</span></span></td>
<td><span data-ttu-id="4e613-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-890">Electricity</span></span></td>
<td><span data-ttu-id="4e613-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-891">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4e613-892">4,487.12</span></span></td>
<td><span data-ttu-id="4e613-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-894">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-895">Product 2</span></span></td>
<td><span data-ttu-id="4e613-896">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-896">10001</span></span></td>
<td><span data-ttu-id="4e613-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-897">Electricity</span></span></td>
<td><span data-ttu-id="4e613-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-898">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4e613-899">1,495.71</span></span></td>
<td><span data-ttu-id="4e613-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-901">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-901">CC003</span></span></td>
<td><span data-ttu-id="4e613-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-902">Assembly</span></span></td>
<td><span data-ttu-id="4e613-903">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-903">10001</span></span></td>
<td><span data-ttu-id="4e613-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-904">Electricity</span></span></td>
<td><span data-ttu-id="4e613-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-905">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="4e613-906">-286.25</span></span></td>
<td><span data-ttu-id="4e613-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-908">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-909">Product 1</span></span></td>
<td><span data-ttu-id="4e613-910">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-910">10001</span></span></td>
<td><span data-ttu-id="4e613-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-911">Electricity</span></span></td>
<td><span data-ttu-id="4e613-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-912">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-913">241.05</span><span class="sxs-lookup"><span data-stu-id="4e613-913">241.05</span></span></td>
<td><span data-ttu-id="4e613-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-915">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-916">Product 2</span></span></td>
<td><span data-ttu-id="4e613-917">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-917">10001</span></span></td>
<td><span data-ttu-id="4e613-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-918">Electricity</span></span></td>
<td><span data-ttu-id="4e613-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-919">Fixed cost</span></span></td>
<td><span data-ttu-id="4e613-920">45.20</span><span class="sxs-lookup"><span data-stu-id="4e613-920">45.20</span></span></td>
<td><span data-ttu-id="4e613-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-922">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-922">CC003</span></span></td>
<td><span data-ttu-id="4e613-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="4e613-923">Assembly</span></span></td>
<td><span data-ttu-id="4e613-924">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-924">10001</span></span></td>
<td><span data-ttu-id="4e613-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-925">Electricity</span></span></td>
<td><span data-ttu-id="4e613-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-926">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="4e613-927">-2,977.17</span></span></td>
<td><span data-ttu-id="4e613-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-929">Prod 1</span></span></td>
<td><span data-ttu-id="4e613-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="4e613-930">Product 1</span></span></td>
<td><span data-ttu-id="4e613-931">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-931">10001</span></span></td>
<td><span data-ttu-id="4e613-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-932">Electricity</span></span></td>
<td><span data-ttu-id="4e613-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-933">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4e613-934">2,507.09</span></span></td>
<td><span data-ttu-id="4e613-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e613-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-936">Prod 2</span></span></td>
<td><span data-ttu-id="4e613-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="4e613-937">Product 2</span></span></td>
<td><span data-ttu-id="4e613-938">10001</span><span class="sxs-lookup"><span data-stu-id="4e613-938">10001</span></span></td>
<td><span data-ttu-id="4e613-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-939">Electricity</span></span></td>
<td><span data-ttu-id="4e613-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-940">Variable cost</span></span></td>
<td><span data-ttu-id="4e613-941">470.08</span><span class="sxs-lookup"><span data-stu-id="4e613-941">470.08</span></span></td>
<td><span data-ttu-id="4e613-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="4e613-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4e613-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="4e613-943">Conclusion</span></span>
<span data-ttu-id="4e613-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="4e613-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4e613-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="4e613-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4e613-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="4e613-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4e613-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="4e613-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4e613-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="4e613-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4e613-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="4e613-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4e613-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="4e613-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4e613-951">CC099</span><span class="sxs-lookup"><span data-stu-id="4e613-951">CC099</span></span></th>
<th><span data-ttu-id="4e613-952">CC001</span><span class="sxs-lookup"><span data-stu-id="4e613-952">CC001</span></span></th>
<th><span data-ttu-id="4e613-953">CC002</span><span class="sxs-lookup"><span data-stu-id="4e613-953">CC002</span></span></th>
<th><span data-ttu-id="4e613-954">CC003</span><span class="sxs-lookup"><span data-stu-id="4e613-954">CC003</span></span></th>
<th><span data-ttu-id="4e613-955">CC004</span><span class="sxs-lookup"><span data-stu-id="4e613-955">CC004</span></span></th>
<th><span data-ttu-id="4e613-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4e613-956">Proj 1</span></span></th>
<th><span data-ttu-id="4e613-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4e613-957">Proj 2</span></span></th>
<th><span data-ttu-id="4e613-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4e613-958">Prod 1</span></span></th>
<th><span data-ttu-id="4e613-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4e613-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4e613-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="4e613-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4e613-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4e613-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="4e613-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-971">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4e613-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-973">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-975">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4e613-978">776.36</span><span class="sxs-lookup"><span data-stu-id="4e613-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-979">223.64</span><span class="sxs-lookup"><span data-stu-id="4e613-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4e613-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="4e613-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-982">000</span><span class="sxs-lookup"><span data-stu-id="4e613-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-983">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-984">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-985">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4e613-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-987">30,00</span><span class="sxs-lookup"><span data-stu-id="4e613-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-988">10,00</span><span class="sxs-lookup"><span data-stu-id="4e613-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4e613-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4e613-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e613-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e613-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4e613-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="4e613-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4e613-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="4e613-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4e613-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="4e613-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4e613-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="4e613-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4e613-996">Zie [Kostentotalisatie](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4e613-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




