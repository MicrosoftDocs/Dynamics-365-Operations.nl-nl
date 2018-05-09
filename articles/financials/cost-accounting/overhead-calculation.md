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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2f37b5957974c927ade698fea65de7e3807d998a
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="ffb44-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="ffb44-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffb44-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="ffb44-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="ffb44-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="ffb44-105">Term definition</span></span>
---------------

<span data-ttu-id="ffb44-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="ffb44-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="ffb44-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="ffb44-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="ffb44-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="ffb44-109">Huur</span><span class="sxs-lookup"><span data-stu-id="ffb44-109">Rent</span></span>
-   <span data-ttu-id="ffb44-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-110">Electricity</span></span>
-   <span data-ttu-id="ffb44-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="ffb44-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="ffb44-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="ffb44-112">Overhead calculation overview</span></span>
<span data-ttu-id="ffb44-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ffb44-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="ffb44-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="ffb44-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="ffb44-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="ffb44-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="ffb44-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="ffb44-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="ffb44-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="ffb44-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="ffb44-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="ffb44-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="ffb44-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="ffb44-119">Version type</span></span>
-   <span data-ttu-id="ffb44-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="ffb44-120">Date and time</span></span>
-   <span data-ttu-id="ffb44-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="ffb44-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="ffb44-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="ffb44-122">Fiscal year</span></span>
-   <span data-ttu-id="ffb44-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="ffb44-123">Fiscal period</span></span>

<span data-ttu-id="ffb44-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ffb44-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="ffb44-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="ffb44-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="ffb44-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ffb44-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="ffb44-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="ffb44-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="ffb44-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="ffb44-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="ffb44-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="ffb44-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="ffb44-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="ffb44-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="ffb44-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="ffb44-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="ffb44-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="ffb44-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="ffb44-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="ffb44-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="ffb44-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="ffb44-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="ffb44-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="ffb44-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="ffb44-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="ffb44-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="ffb44-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="ffb44-140">Main account</span></span></th>
<th><span data-ttu-id="ffb44-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="ffb44-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="ffb44-143">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-143">CC099</span></span></td>
<td><span data-ttu-id="ffb44-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-144">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-145">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-145">10001</span></span></td>
<td><span data-ttu-id="ffb44-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-146">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="ffb44-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="ffb44-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="ffb44-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="ffb44-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="ffb44-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="ffb44-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="ffb44-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="ffb44-151">Define the cost behavior rule</span></span>

<span data-ttu-id="ffb44-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="ffb44-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="ffb44-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="ffb44-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="ffb44-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="ffb44-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="ffb44-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="ffb44-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="ffb44-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="ffb44-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="ffb44-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="ffb44-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="ffb44-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="ffb44-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-160">Journal</span></span></th>
<th><span data-ttu-id="ffb44-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ffb44-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ffb44-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ffb44-163">Versie</span><span class="sxs-lookup"><span data-stu-id="ffb44-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-164">00001</span><span class="sxs-lookup"><span data-stu-id="ffb44-164">00001</span></span></td>
<td><span data-ttu-id="ffb44-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="ffb44-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-166">Fiscal</span></span></td>
<td><span data-ttu-id="ffb44-167">2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-167">2017</span></span></td>
<td><span data-ttu-id="ffb44-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-168">Period 1</span></span></td>
<td><span data-ttu-id="ffb44-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ffb44-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="ffb44-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-173">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-174">Cost behavior</span></span></th>
<th><span data-ttu-id="ffb44-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="ffb44-177">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-177">CC099</span></span></td>
<td><span data-ttu-id="ffb44-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-178">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-179">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-179">10001</span></span></td>
<td><span data-ttu-id="ffb44-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-180">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="ffb44-181">Unclassified</span></span></td>
<td><span data-ttu-id="ffb44-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ffb44-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="ffb44-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-185">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-186">Cost behavior</span></span></th>
<th><span data-ttu-id="ffb44-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-187">Amount</span></span></th>
<th><span data-ttu-id="ffb44-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-189">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-189">CC099</span></span></td>
<td><span data-ttu-id="ffb44-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-190">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-191">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-191">10001</span></span></td>
<td><span data-ttu-id="ffb44-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-192">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="ffb44-193">Unclassified</span></span></td>
<td><span data-ttu-id="ffb44-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-194">10,000.00</span></span></td>
<td><span data-ttu-id="ffb44-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-196">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-196">CC099</span></span></td>
<td><span data-ttu-id="ffb44-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-197">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-198">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-198">10001</span></span></td>
<td><span data-ttu-id="ffb44-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-199">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="ffb44-200">Unclassified</span></span></td>
<td><span data-ttu-id="ffb44-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-201">-10,000.00</span></span></td>
<td><span data-ttu-id="ffb44-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-203">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-203">CC099</span></span></td>
<td><span data-ttu-id="ffb44-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-204">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-205">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-205">10001</span></span></td>
<td><span data-ttu-id="ffb44-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-206">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-207">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-208">1,000.00</span></span></td>
<td><span data-ttu-id="ffb44-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-210">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-210">CC099</span></span></td>
<td><span data-ttu-id="ffb44-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-211">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-212">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-212">10001</span></span></td>
<td><span data-ttu-id="ffb44-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-213">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-214">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-215">9,000.00</span></span></td>
<td><span data-ttu-id="ffb44-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-217">Zie Kostengedragbeleid voor gedetailleerde informatie over kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="ffb44-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="ffb44-218">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="ffb44-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="ffb44-219">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="ffb44-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="ffb44-220">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="ffb44-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="ffb44-221">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="ffb44-222">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="ffb44-222">Define the cost distribution rule</span></span>

<span data-ttu-id="ffb44-223">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="ffb44-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="ffb44-224">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="ffb44-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="ffb44-225">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="ffb44-226">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="ffb44-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="ffb44-227">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ffb44-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="ffb44-228">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="ffb44-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-229">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-229">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="ffb44-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-231">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-231">CC001</span></span></td>
<td><span data-ttu-id="ffb44-232">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-232">HR</span></span></td>
<td><span data-ttu-id="ffb44-233">1.000</span><span class="sxs-lookup"><span data-stu-id="ffb44-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-234">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-234">CC002</span></span></td>
<td><span data-ttu-id="ffb44-235">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-235">Finance</span></span></td>
<td><span data-ttu-id="ffb44-236">6.000</span><span class="sxs-lookup"><span data-stu-id="ffb44-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-237">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-237">CC003</span></span></td>
<td><span data-ttu-id="ffb44-238">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-238">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-239">0</span><span class="sxs-lookup"><span data-stu-id="ffb44-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-240">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-241">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-241">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-242">Magnitude</span><span class="sxs-lookup"><span data-stu-id="ffb44-242">Magnitude</span></span></th>
<th><span data-ttu-id="ffb44-243">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="ffb44-243">Allocation factor</span></span></th>
<th><span data-ttu-id="ffb44-244">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-245">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-245">CC001</span></span></td>
<td><span data-ttu-id="ffb44-246">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-246">HR</span></span></td>
<td><span data-ttu-id="ffb44-247">1.000</span><span class="sxs-lookup"><span data-stu-id="ffb44-247">1,000</span></span></td>
<td><span data-ttu-id="ffb44-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ffb44-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ffb44-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-250">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-250">CC002</span></span></td>
<td><span data-ttu-id="ffb44-251">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-251">Finance</span></span></td>
<td><span data-ttu-id="ffb44-252">6.000</span><span class="sxs-lookup"><span data-stu-id="ffb44-252">6,000</span></span></td>
<td><span data-ttu-id="ffb44-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ffb44-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ffb44-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-255">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-255">CC003</span></span></td>
<td><span data-ttu-id="ffb44-256">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-256">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-257">0</span><span class="sxs-lookup"><span data-stu-id="ffb44-257">0</span></span></td>
<td><span data-ttu-id="ffb44-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ffb44-259">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-260">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="ffb44-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="ffb44-261">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-262">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-262">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-263">Formule</span><span class="sxs-lookup"><span data-stu-id="ffb44-263">Formula</span></span></th>
<th><span data-ttu-id="ffb44-264">Magnitude</span><span class="sxs-lookup"><span data-stu-id="ffb44-264">Magnitude</span></span></th>
<th><span data-ttu-id="ffb44-265">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="ffb44-265">Allocation factor</span></span></th>
<th><span data-ttu-id="ffb44-266">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-267">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-267">CC001</span></span></td>
<td><span data-ttu-id="ffb44-268">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-268">HR</span></span></td>
<td><span data-ttu-id="ffb44-269">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ffb44-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ffb44-270">1</span><span class="sxs-lookup"><span data-stu-id="ffb44-270">1</span></span></td>
<td><span data-ttu-id="ffb44-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ffb44-272">500,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-273">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-273">CC002</span></span></td>
<td><span data-ttu-id="ffb44-274">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-274">Finance</span></span></td>
<td><span data-ttu-id="ffb44-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ffb44-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ffb44-276">1</span><span class="sxs-lookup"><span data-stu-id="ffb44-276">1</span></span></td>
<td><span data-ttu-id="ffb44-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ffb44-278">500,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-279">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-279">CC003</span></span></td>
<td><span data-ttu-id="ffb44-280">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-280">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ffb44-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ffb44-282">0</span><span class="sxs-lookup"><span data-stu-id="ffb44-282">0</span></span></td>
<td><span data-ttu-id="ffb44-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ffb44-284">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ffb44-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-286">Journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-286">Journal</span></span></th>
<th><span data-ttu-id="ffb44-287">Type journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ffb44-288">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ffb44-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ffb44-289">Versie</span><span class="sxs-lookup"><span data-stu-id="ffb44-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-290">00002</span><span class="sxs-lookup"><span data-stu-id="ffb44-290">00002</span></span></td>
<td><span data-ttu-id="ffb44-291">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="ffb44-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="ffb44-292">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-292">Fiscal</span></span></td>
<td><span data-ttu-id="ffb44-293">2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-293">2017</span></span></td>
<td><span data-ttu-id="ffb44-294">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-294">Period 1</span></span></td>
<td><span data-ttu-id="ffb44-295">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ffb44-296">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="ffb44-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-297">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-298">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-299">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-299">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-300">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-300">Cost behavior</span></span></th>
<th><span data-ttu-id="ffb44-301">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-302">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-303">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-303">CC099</span></span></td>
<td><span data-ttu-id="ffb44-304">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-304">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-305">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-305">10001</span></span></td>
<td><span data-ttu-id="ffb44-306">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-306">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-307">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-307">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-309">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-310">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-310">CC099</span></span></td>
<td><span data-ttu-id="ffb44-311">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-311">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-312">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-312">10001</span></span></td>
<td><span data-ttu-id="ffb44-313">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-313">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-314">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-314">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-315">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ffb44-316">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="ffb44-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-317">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-318">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-318">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-319">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-319">Cost behavior</span></span></th>
<th><span data-ttu-id="ffb44-320">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-320">Amount</span></span></th>
<th><span data-ttu-id="ffb44-321">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-322">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-322">CC099</span></span></td>
<td><span data-ttu-id="ffb44-323">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-323">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-324">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-324">10001</span></span></td>
<td><span data-ttu-id="ffb44-325">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-325">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-326">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-326">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-327">-1,000.00</span></span></td>
<td><span data-ttu-id="ffb44-328">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-329">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-329">CC001</span></span></td>
<td><span data-ttu-id="ffb44-330">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-330">HR</span></span></td>
<td><span data-ttu-id="ffb44-331">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-331">10001</span></span></td>
<td><span data-ttu-id="ffb44-332">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-332">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-333">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-333">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-334">500,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-334">500.00</span></span></td>
<td><span data-ttu-id="ffb44-335">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-336">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-336">CC002</span></span></td>
<td><span data-ttu-id="ffb44-337">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-337">Finance</span></span></td>
<td><span data-ttu-id="ffb44-338">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-338">10001</span></span></td>
<td><span data-ttu-id="ffb44-339">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-339">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-340">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-340">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-341">500,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-341">500.00</span></span></td>
<td><span data-ttu-id="ffb44-342">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-343">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-343">CC099</span></span></td>
<td><span data-ttu-id="ffb44-344">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="ffb44-344">Default cost center</span></span></td>
<td><span data-ttu-id="ffb44-345">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-345">10001</span></span></td>
<td><span data-ttu-id="ffb44-346">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-346">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-347">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-347">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-348">-9,000.00</span></span></td>
<td><span data-ttu-id="ffb44-349">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-350">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-350">CC001</span></span></td>
<td><span data-ttu-id="ffb44-351">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-351">HR</span></span></td>
<td><span data-ttu-id="ffb44-352">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-352">10001</span></span></td>
<td><span data-ttu-id="ffb44-353">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-353">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-354">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-354">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ffb44-355">1,285.71</span></span></td>
<td><span data-ttu-id="ffb44-356">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-357">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-357">CC002</span></span></td>
<td><span data-ttu-id="ffb44-358">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-358">Finance</span></span></td>
<td><span data-ttu-id="ffb44-359">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-359">10001</span></span></td>
<td><span data-ttu-id="ffb44-360">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-360">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-361">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-361">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ffb44-362">7,714.29</span></span></td>
<td><span data-ttu-id="ffb44-363">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-364">Zie Kostenverdelingsbeleid en Toewijzigingsgrondslagen voor gedetailleerde informatie over kostenverdeling en toewijzingsgrondslagen.</span><span class="sxs-lookup"><span data-stu-id="ffb44-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="ffb44-365">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="ffb44-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="ffb44-366">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="ffb44-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="ffb44-367">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="ffb44-368">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="ffb44-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="ffb44-369">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="ffb44-369">Define the overhead rate</span></span>

<span data-ttu-id="ffb44-370">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="ffb44-371">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-372">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-372">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-373">Uren</span><span class="sxs-lookup"><span data-stu-id="ffb44-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-374">Proj 1</span></span></td>
<td><span data-ttu-id="ffb44-375">Project 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-375">Project 1</span></span></td>
<td><span data-ttu-id="ffb44-376">3</span><span class="sxs-lookup"><span data-stu-id="ffb44-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-377">Proj 2</span></span></td>
<td><span data-ttu-id="ffb44-378">Project 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-378">Project 2</span></span></td>
<td><span data-ttu-id="ffb44-379">1</span><span class="sxs-lookup"><span data-stu-id="ffb44-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-380">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ffb44-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-381">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-381">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-382">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-382">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-383">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-383">Cost behavior</span></span></th>
<th><span data-ttu-id="ffb44-384">Eenheden</span><span class="sxs-lookup"><span data-stu-id="ffb44-384">Units</span></span></th>
<th><span data-ttu-id="ffb44-385">Tarief</span><span class="sxs-lookup"><span data-stu-id="ffb44-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-386">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-386">CC001</span></span></td>
<td><span data-ttu-id="ffb44-387">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-387">HR</span></span></td>
<td><span data-ttu-id="ffb44-388">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-388">10001</span></span></td>
<td><span data-ttu-id="ffb44-389">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-389">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-390">1</span><span class="sxs-lookup"><span data-stu-id="ffb44-390">1</span></span></td>
<td><span data-ttu-id="ffb44-391">10</span><span class="sxs-lookup"><span data-stu-id="ffb44-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-392">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="ffb44-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-393">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-393">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-394">Magnitude</span><span class="sxs-lookup"><span data-stu-id="ffb44-394">Magnitude</span></span></th>
<th><span data-ttu-id="ffb44-395">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-395">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-396">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="ffb44-396">Allocation factor</span></span></th>
<th><span data-ttu-id="ffb44-397">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-398">Proj 1</span></span></td>
<td><span data-ttu-id="ffb44-399">Project 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-399">Project 1</span></span></td>
<td><span data-ttu-id="ffb44-400">3</span><span class="sxs-lookup"><span data-stu-id="ffb44-400">3</span></span></td>
<td><span data-ttu-id="ffb44-401">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-401">10001</span></span></td>
<td><span data-ttu-id="ffb44-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ffb44-403">30,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-404">Proj 2</span></span></td>
<td><span data-ttu-id="ffb44-405">Project 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-405">Project 2</span></span></td>
<td><span data-ttu-id="ffb44-406">1</span><span class="sxs-lookup"><span data-stu-id="ffb44-406">1</span></span></td>
<td><span data-ttu-id="ffb44-407">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-407">10001</span></span></td>
<td><span data-ttu-id="ffb44-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ffb44-409">10,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ffb44-410">Journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-411">Journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-411">Journal</span></span></th>
<th><span data-ttu-id="ffb44-412">Type journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ffb44-413">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ffb44-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ffb44-414">Versie</span><span class="sxs-lookup"><span data-stu-id="ffb44-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-415">00003</span><span class="sxs-lookup"><span data-stu-id="ffb44-415">00003</span></span></td>
<td><span data-ttu-id="ffb44-416">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="ffb44-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="ffb44-417">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-417">Fiscal</span></span></td>
<td><span data-ttu-id="ffb44-418">2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-418">2017</span></span></td>
<td><span data-ttu-id="ffb44-419">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-419">Period 1</span></span></td>
<td><span data-ttu-id="ffb44-420">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="ffb44-421">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="ffb44-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-422">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-423">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-423">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-424">Magnitude</span><span class="sxs-lookup"><span data-stu-id="ffb44-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-425">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-426">Proj 1</span></span></td>
<td><span data-ttu-id="ffb44-427">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ffb44-428">3,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-429">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-430">Proj 2</span></span></td>
<td><span data-ttu-id="ffb44-431">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ffb44-432">1,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ffb44-433">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="ffb44-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-434">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-435">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-435">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-436">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-436">Cost behavior</span></span></th>
<th><span data-ttu-id="ffb44-437">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-437">Amount</span></span></th>
<th><span data-ttu-id="ffb44-438">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="ffb44-439">CC0001</span></span></td>
<td><span data-ttu-id="ffb44-440">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-440">HR</span></span></td>
<td><span data-ttu-id="ffb44-441">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-441">10001</span></span></td>
<td><span data-ttu-id="ffb44-442">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-442">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-443">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-443">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-444">-30.00</span></span></td>
<td><span data-ttu-id="ffb44-445">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-446">Proj 1</span></span></td>
<td><span data-ttu-id="ffb44-447">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ffb44-448">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-448">10001</span></span></td>
<td><span data-ttu-id="ffb44-449">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-449">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-450">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-450">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-451">30,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-451">30.00</span></span></td>
<td><span data-ttu-id="ffb44-452">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-453">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-453">CC001</span></span></td>
<td><span data-ttu-id="ffb44-454">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-454">HR</span></span></td>
<td><span data-ttu-id="ffb44-455">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-455">10001</span></span></td>
<td><span data-ttu-id="ffb44-456">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-456">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-457">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-457">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-458">-10.00</span></span></td>
<td><span data-ttu-id="ffb44-459">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-460">Proj 2</span></span></td>
<td><span data-ttu-id="ffb44-461">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ffb44-462">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-462">10001</span></span></td>
<td><span data-ttu-id="ffb44-463">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-463">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-464">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-464">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-465">10,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-465">10.00</span></span></td>
<td><span data-ttu-id="ffb44-466">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-467">Zie Beleid voor overheadtarief en Toewijzingsgrondslagen voor gedetailleerde informatie over beleid voor overheadtarieven.</span><span class="sxs-lookup"><span data-stu-id="ffb44-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="ffb44-468">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="ffb44-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="ffb44-469">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="ffb44-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="ffb44-470">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="ffb44-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="ffb44-471">Finance and Operations ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="ffb44-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="ffb44-472">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="ffb44-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="ffb44-473">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="ffb44-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="ffb44-474">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="ffb44-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="ffb44-475">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="ffb44-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="ffb44-476">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="ffb44-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="ffb44-477">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="ffb44-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="ffb44-478">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="ffb44-478">Define the cost allocation</span></span>

<span data-ttu-id="ffb44-479">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="ffb44-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="ffb44-480">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="ffb44-481">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-482">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-482">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-483">HR-services</span><span class="sxs-lookup"><span data-stu-id="ffb44-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-484">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-484">CC002</span></span></td>
<td><span data-ttu-id="ffb44-485">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-485">Finance</span></span></td>
<td><span data-ttu-id="ffb44-486">35</span><span class="sxs-lookup"><span data-stu-id="ffb44-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-487">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-487">CC003</span></span></td>
<td><span data-ttu-id="ffb44-488">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-488">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-489">55</span><span class="sxs-lookup"><span data-stu-id="ffb44-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-490">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-490">CC004</span></span></td>
<td><span data-ttu-id="ffb44-491">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-491">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-492">10</span><span class="sxs-lookup"><span data-stu-id="ffb44-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-493">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="ffb44-494">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-495">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-495">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-496">Financiële services</span><span class="sxs-lookup"><span data-stu-id="ffb44-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-497">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-497">CC003</span></span></td>
<td><span data-ttu-id="ffb44-498">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-498">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-499">65</span><span class="sxs-lookup"><span data-stu-id="ffb44-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-500">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-500">CC004</span></span></td>
<td><span data-ttu-id="ffb44-501">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-501">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-502">35</span><span class="sxs-lookup"><span data-stu-id="ffb44-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-503">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="ffb44-504">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-505">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-505">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-506">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="ffb44-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-507">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-508">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-508">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-509">60</span><span class="sxs-lookup"><span data-stu-id="ffb44-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-510">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-511">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-511">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-512">20</span><span class="sxs-lookup"><span data-stu-id="ffb44-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-513">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="ffb44-514">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-515">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-515">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-516">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="ffb44-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-517">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-518">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-518">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-519">80</span><span class="sxs-lookup"><span data-stu-id="ffb44-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-520">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-521">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-521">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-522">15</span><span class="sxs-lookup"><span data-stu-id="ffb44-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-523">**Opmerking:** In Finance and Operations kunnen statistische metingen, zoals de productie-uren die een product verbruikt, worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="ffb44-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="ffb44-524">Zie Sjablonen van provider van statistische maateenheden voor gedetailleerdere informatie over statistische providers van statistische maateenheden.</span><span class="sxs-lookup"><span data-stu-id="ffb44-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="ffb44-525">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.) In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="ffb44-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-526">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-526">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-527">Magnitude</span><span class="sxs-lookup"><span data-stu-id="ffb44-527">Magnitude</span></span></th>
<th><span data-ttu-id="ffb44-528">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="ffb44-528">Allocation factor</span></span></th>
<th><span data-ttu-id="ffb44-529">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-529">Amount</span></span></th>
<th><span data-ttu-id="ffb44-530">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-531">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-531">CC002</span></span></td>
<td><span data-ttu-id="ffb44-532">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-532">Finance</span></span></td>
<td><span data-ttu-id="ffb44-533">35</span><span class="sxs-lookup"><span data-stu-id="ffb44-533">35</span></span></td>
<td><span data-ttu-id="ffb44-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ffb44-535">175.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-535">175.00</span></span></td>
<td><span data-ttu-id="ffb44-536">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-537">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-537">CC003</span></span></td>
<td><span data-ttu-id="ffb44-538">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-538">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-539">55</span><span class="sxs-lookup"><span data-stu-id="ffb44-539">55</span></span></td>
<td><span data-ttu-id="ffb44-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ffb44-541">275.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-541">275.00</span></span></td>
<td><span data-ttu-id="ffb44-542">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-543">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-543">CC004</span></span></td>
<td><span data-ttu-id="ffb44-544">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-544">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-545">10</span><span class="sxs-lookup"><span data-stu-id="ffb44-545">10</span></span></td>
<td><span data-ttu-id="ffb44-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ffb44-547">50,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-547">50.00</span></span></td>
<td><span data-ttu-id="ffb44-548">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-549">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-549">CC002</span></span></td>
<td><span data-ttu-id="ffb44-550">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-550">Finance</span></span></td>
<td><span data-ttu-id="ffb44-551">35</span><span class="sxs-lookup"><span data-stu-id="ffb44-551">35</span></span></td>
<td><span data-ttu-id="ffb44-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ffb44-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ffb44-553">436.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-553">436.00</span></span></td>
<td><span data-ttu-id="ffb44-554">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-555">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-555">CC003</span></span></td>
<td><span data-ttu-id="ffb44-556">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-556">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-557">55</span><span class="sxs-lookup"><span data-stu-id="ffb44-557">55</span></span></td>
<td><span data-ttu-id="ffb44-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ffb44-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ffb44-559">685.14</span><span class="sxs-lookup"><span data-stu-id="ffb44-559">685.14</span></span></td>
<td><span data-ttu-id="ffb44-560">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-561">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-561">CC004</span></span></td>
<td><span data-ttu-id="ffb44-562">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-562">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-563">10</span><span class="sxs-lookup"><span data-stu-id="ffb44-563">10</span></span></td>
<td><span data-ttu-id="ffb44-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ffb44-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ffb44-565">124.57</span><span class="sxs-lookup"><span data-stu-id="ffb44-565">124.57</span></span></td>
<td><span data-ttu-id="ffb44-566">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-567">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="ffb44-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-568">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-568">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-569">Magnitude</span><span class="sxs-lookup"><span data-stu-id="ffb44-569">Magnitude</span></span></th>
<th><span data-ttu-id="ffb44-570">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="ffb44-570">Allocation factor</span></span></th>
<th><span data-ttu-id="ffb44-571">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-571">Amount</span></span></th>
<th><span data-ttu-id="ffb44-572">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-573">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-573">CC003</span></span></td>
<td><span data-ttu-id="ffb44-574">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-574">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-575">65</span><span class="sxs-lookup"><span data-stu-id="ffb44-575">65</span></span></td>
<td><span data-ttu-id="ffb44-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ffb44-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ffb44-577">438.75</span><span class="sxs-lookup"><span data-stu-id="ffb44-577">438.75</span></span></td>
<td><span data-ttu-id="ffb44-578">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-579">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-579">CC004</span></span></td>
<td><span data-ttu-id="ffb44-580">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-580">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-581">35</span><span class="sxs-lookup"><span data-stu-id="ffb44-581">35</span></span></td>
<td><span data-ttu-id="ffb44-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ffb44-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ffb44-583">236.25</span><span class="sxs-lookup"><span data-stu-id="ffb44-583">236.25</span></span></td>
<td><span data-ttu-id="ffb44-584">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-585">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-585">CC003</span></span></td>
<td><span data-ttu-id="ffb44-586">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-586">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-587">65</span><span class="sxs-lookup"><span data-stu-id="ffb44-587">65</span></span></td>
<td><span data-ttu-id="ffb44-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ffb44-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ffb44-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ffb44-589">5,297.69</span></span></td>
<td><span data-ttu-id="ffb44-590">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-591">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-591">CC004</span></span></td>
<td><span data-ttu-id="ffb44-592">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-592">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-593">35</span><span class="sxs-lookup"><span data-stu-id="ffb44-593">35</span></span></td>
<td><span data-ttu-id="ffb44-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ffb44-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ffb44-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ffb44-595">2,852.60</span></span></td>
<td><span data-ttu-id="ffb44-596">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-597">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="ffb44-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-598">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-598">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-599">Magnitude</span><span class="sxs-lookup"><span data-stu-id="ffb44-599">Magnitude</span></span></th>
<th><span data-ttu-id="ffb44-600">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="ffb44-600">Allocation factor</span></span></th>
<th><span data-ttu-id="ffb44-601">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-601">Amount</span></span></th>
<th><span data-ttu-id="ffb44-602">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-603">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-604">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-604">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-605">60</span><span class="sxs-lookup"><span data-stu-id="ffb44-605">60</span></span></td>
<td><span data-ttu-id="ffb44-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ffb44-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ffb44-607">535.31</span><span class="sxs-lookup"><span data-stu-id="ffb44-607">535.31</span></span></td>
<td><span data-ttu-id="ffb44-608">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-609">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-610">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-610">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-611">20</span><span class="sxs-lookup"><span data-stu-id="ffb44-611">20</span></span></td>
<td><span data-ttu-id="ffb44-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ffb44-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ffb44-613">178.44</span><span class="sxs-lookup"><span data-stu-id="ffb44-613">178.44</span></span></td>
<td><span data-ttu-id="ffb44-614">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-615">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-616">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-616">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-617">60</span><span class="sxs-lookup"><span data-stu-id="ffb44-617">60</span></span></td>
<td><span data-ttu-id="ffb44-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ffb44-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ffb44-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ffb44-619">4,487.12</span></span></td>
<td><span data-ttu-id="ffb44-620">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-621">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-622">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-622">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-623">20</span><span class="sxs-lookup"><span data-stu-id="ffb44-623">20</span></span></td>
<td><span data-ttu-id="ffb44-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ffb44-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ffb44-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ffb44-625">1,495.71</span></span></td>
<td><span data-ttu-id="ffb44-626">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ffb44-627">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="ffb44-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-628">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-628">Cost object</span></span></th>
<th><span data-ttu-id="ffb44-629">Magnitude</span><span class="sxs-lookup"><span data-stu-id="ffb44-629">Magnitude</span></span></th>
<th><span data-ttu-id="ffb44-630">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="ffb44-630">Allocation factor</span></span></th>
<th><span data-ttu-id="ffb44-631">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-631">Amount</span></span></th>
<th><span data-ttu-id="ffb44-632">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-633">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-634">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-634">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-635">80</span><span class="sxs-lookup"><span data-stu-id="ffb44-635">80</span></span></td>
<td><span data-ttu-id="ffb44-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ffb44-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ffb44-637">241.05</span><span class="sxs-lookup"><span data-stu-id="ffb44-637">241.05</span></span></td>
<td><span data-ttu-id="ffb44-638">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-639">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-640">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-640">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-641">15</span><span class="sxs-lookup"><span data-stu-id="ffb44-641">15</span></span></td>
<td><span data-ttu-id="ffb44-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ffb44-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ffb44-643">45.20</span><span class="sxs-lookup"><span data-stu-id="ffb44-643">45.20</span></span></td>
<td><span data-ttu-id="ffb44-644">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-645">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-646">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-646">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-647">80</span><span class="sxs-lookup"><span data-stu-id="ffb44-647">80</span></span></td>
<td><span data-ttu-id="ffb44-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ffb44-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ffb44-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ffb44-649">2,507.09</span></span></td>
<td><span data-ttu-id="ffb44-650">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-651">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-652">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-652">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-653">15</span><span class="sxs-lookup"><span data-stu-id="ffb44-653">15</span></span></td>
<td><span data-ttu-id="ffb44-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ffb44-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ffb44-655">470.08</span><span class="sxs-lookup"><span data-stu-id="ffb44-655">470.08</span></span></td>
<td><span data-ttu-id="ffb44-656">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ffb44-657">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="ffb44-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-658">Journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-658">Journal</span></span></th>
<th><span data-ttu-id="ffb44-659">Type journaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ffb44-660">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ffb44-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ffb44-661">Versie</span><span class="sxs-lookup"><span data-stu-id="ffb44-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-662">00004</span><span class="sxs-lookup"><span data-stu-id="ffb44-662">00004</span></span></td>
<td><span data-ttu-id="ffb44-663">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="ffb44-664">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-664">Fiscal</span></span></td>
<td><span data-ttu-id="ffb44-665">2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-665">2017</span></span></td>
<td><span data-ttu-id="ffb44-666">Periode 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-666">Period 1</span></span></td>
<td><span data-ttu-id="ffb44-667">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="ffb44-668">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="ffb44-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ffb44-669">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-670">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-671">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-671">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-672">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-672">Cost behavior</span></span></th>
<th><span data-ttu-id="ffb44-673">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-674">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-675">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-675">CC001</span></span></td>
<td><span data-ttu-id="ffb44-676">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-676">HR</span></span></td>
<td><span data-ttu-id="ffb44-677">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-677">10001</span></span></td>
<td><span data-ttu-id="ffb44-678">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-678">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-679">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-679">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-680">500,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-681">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-682">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-682">CC001</span></span></td>
<td><span data-ttu-id="ffb44-683">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-683">HR</span></span></td>
<td><span data-ttu-id="ffb44-684">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-684">10001</span></span></td>
<td><span data-ttu-id="ffb44-685">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-685">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-686">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-686">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="ffb44-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-688">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-689">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-689">CC002</span></span></td>
<td><span data-ttu-id="ffb44-690">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-690">Finance</span></span></td>
<td><span data-ttu-id="ffb44-691">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-691">10001</span></span></td>
<td><span data-ttu-id="ffb44-692">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-692">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-693">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-693">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-694">675.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-695">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-696">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-696">CC002</span></span></td>
<td><span data-ttu-id="ffb44-697">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-697">Finance</span></span></td>
<td><span data-ttu-id="ffb44-698">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-698">10001</span></span></td>
<td><span data-ttu-id="ffb44-699">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-699">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-700">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-700">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="ffb44-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-702">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-703">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-703">CC003</span></span></td>
<td><span data-ttu-id="ffb44-704">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-704">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-705">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-705">10001</span></span></td>
<td><span data-ttu-id="ffb44-706">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-706">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-707">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-707">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-708">713.75</span><span class="sxs-lookup"><span data-stu-id="ffb44-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-709">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-710">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-710">CC003</span></span></td>
<td><span data-ttu-id="ffb44-711">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-711">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-712">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-712">10001</span></span></td>
<td><span data-ttu-id="ffb44-713">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-713">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-714">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-714">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="ffb44-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-716">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-717">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-717">CC003</span></span></td>
<td><span data-ttu-id="ffb44-718">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-718">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-719">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-719">10001</span></span></td>
<td><span data-ttu-id="ffb44-720">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-720">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-721">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-721">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-722">286.25</span><span class="sxs-lookup"><span data-stu-id="ffb44-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-723">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-724">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-724">CC003</span></span></td>
<td><span data-ttu-id="ffb44-725">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-725">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-726">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-726">10001</span></span></td>
<td><span data-ttu-id="ffb44-727">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-727">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-728">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-728">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="ffb44-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-730">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-731">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-732">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-732">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-733">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-733">10001</span></span></td>
<td><span data-ttu-id="ffb44-734">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-734">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-735">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-735">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-736">776.36</span><span class="sxs-lookup"><span data-stu-id="ffb44-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-737">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-738">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-739">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-739">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-740">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-740">10001</span></span></td>
<td><span data-ttu-id="ffb44-741">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-741">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-742">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-742">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ffb44-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-744">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-745">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-746">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-746">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-747">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-747">10001</span></span></td>
<td><span data-ttu-id="ffb44-748">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-748">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-749">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-749">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-750">223.64</span><span class="sxs-lookup"><span data-stu-id="ffb44-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-751">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="ffb44-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-752">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-753">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-753">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-754">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-754">10001</span></span></td>
<td><span data-ttu-id="ffb44-755">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-755">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-756">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-756">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ffb44-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ffb44-758">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="ffb44-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ffb44-759">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ffb44-760">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-760">Cost element</span></span></th>
<th><span data-ttu-id="ffb44-761">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-761">Cost behavior</span></span></th>
<th><span data-ttu-id="ffb44-762">Bedrag</span><span class="sxs-lookup"><span data-stu-id="ffb44-762">Amount</span></span></th>
<th><span data-ttu-id="ffb44-763">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="ffb44-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb44-764">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-764">CC001</span></span></td>
<td><span data-ttu-id="ffb44-765">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-765">HR</span></span></td>
<td><span data-ttu-id="ffb44-766">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-766">10001</span></span></td>
<td><span data-ttu-id="ffb44-767">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-767">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-768">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-768">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-769">-500.00</span></span></td>
<td><span data-ttu-id="ffb44-770">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-771">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-771">CC002</span></span></td>
<td><span data-ttu-id="ffb44-772">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-772">Finance</span></span></td>
<td><span data-ttu-id="ffb44-773">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-773">10001</span></span></td>
<td><span data-ttu-id="ffb44-774">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-774">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-775">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-775">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-776">175.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-776">175.00</span></span></td>
<td><span data-ttu-id="ffb44-777">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-778">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-778">CC003</span></span></td>
<td><span data-ttu-id="ffb44-779">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-779">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-780">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-780">10001</span></span></td>
<td><span data-ttu-id="ffb44-781">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-781">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-782">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-782">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-783">275.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-783">275.00</span></span></td>
<td><span data-ttu-id="ffb44-784">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-785">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-785">CC004</span></span></td>
<td><span data-ttu-id="ffb44-786">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-786">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-787">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-787">10001</span></span></td>
<td><span data-ttu-id="ffb44-788">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-788">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-789">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-789">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-790">50,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-790">50,00</span></span></td>
<td><span data-ttu-id="ffb44-791">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-792">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-792">CC001</span></span></td>
<td><span data-ttu-id="ffb44-793">HR</span><span class="sxs-lookup"><span data-stu-id="ffb44-793">HR</span></span></td>
<td><span data-ttu-id="ffb44-794">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-794">10001</span></span></td>
<td><span data-ttu-id="ffb44-795">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-795">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-796">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-796">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="ffb44-797">-1,245.71</span></span></td>
<td><span data-ttu-id="ffb44-798">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-799">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-799">CC002</span></span></td>
<td><span data-ttu-id="ffb44-800">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-800">Finance</span></span></td>
<td><span data-ttu-id="ffb44-801">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-801">10001</span></span></td>
<td><span data-ttu-id="ffb44-802">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-802">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-803">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-803">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-804">436.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-804">436.00</span></span></td>
<td><span data-ttu-id="ffb44-805">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-806">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-806">CC003</span></span></td>
<td><span data-ttu-id="ffb44-807">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-807">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-808">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-808">10001</span></span></td>
<td><span data-ttu-id="ffb44-809">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-809">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-810">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-810">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-811">685.14</span><span class="sxs-lookup"><span data-stu-id="ffb44-811">685.14</span></span></td>
<td><span data-ttu-id="ffb44-812">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-813">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-813">CC004</span></span></td>
<td><span data-ttu-id="ffb44-814">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-814">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-815">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-815">10001</span></span></td>
<td><span data-ttu-id="ffb44-816">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-816">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-817">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-817">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-818">124.57</span><span class="sxs-lookup"><span data-stu-id="ffb44-818">124.57</span></span></td>
<td><span data-ttu-id="ffb44-819">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-820">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-820">CC002</span></span></td>
<td><span data-ttu-id="ffb44-821">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-821">Finance</span></span></td>
<td><span data-ttu-id="ffb44-822">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-822">10001</span></span></td>
<td><span data-ttu-id="ffb44-823">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-823">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-824">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-824">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="ffb44-825">-675.00</span></span></td>
<td><span data-ttu-id="ffb44-826">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-827">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-827">CC003</span></span></td>
<td><span data-ttu-id="ffb44-828">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-828">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-829">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-829">10001</span></span></td>
<td><span data-ttu-id="ffb44-830">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-830">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-831">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-831">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-832">438.75</span><span class="sxs-lookup"><span data-stu-id="ffb44-832">438.75</span></span></td>
<td><span data-ttu-id="ffb44-833">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-834">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-834">CC004</span></span></td>
<td><span data-ttu-id="ffb44-835">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-835">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-836">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-836">10001</span></span></td>
<td><span data-ttu-id="ffb44-837">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-837">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-838">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-838">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-839">236.25</span><span class="sxs-lookup"><span data-stu-id="ffb44-839">236.25</span></span></td>
<td><span data-ttu-id="ffb44-840">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-841">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-841">CC002</span></span></td>
<td><span data-ttu-id="ffb44-842">Financiën</span><span class="sxs-lookup"><span data-stu-id="ffb44-842">Finance</span></span></td>
<td><span data-ttu-id="ffb44-843">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-843">10001</span></span></td>
<td><span data-ttu-id="ffb44-844">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-844">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-845">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-845">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="ffb44-846">-8,150.29</span></span></td>
<td><span data-ttu-id="ffb44-847">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-848">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-848">CC003</span></span></td>
<td><span data-ttu-id="ffb44-849">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-849">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-850">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-850">10001</span></span></td>
<td><span data-ttu-id="ffb44-851">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-851">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-852">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-852">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ffb44-853">5,297.69</span></span></td>
<td><span data-ttu-id="ffb44-854">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-855">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-855">CC004</span></span></td>
<td><span data-ttu-id="ffb44-856">Verpakking</span><span class="sxs-lookup"><span data-stu-id="ffb44-856">Packaging</span></span></td>
<td><span data-ttu-id="ffb44-857">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-857">10001</span></span></td>
<td><span data-ttu-id="ffb44-858">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-858">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-859">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-859">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ffb44-860">2,852.60</span></span></td>
<td><span data-ttu-id="ffb44-861">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-862">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-862">CC003</span></span></td>
<td><span data-ttu-id="ffb44-863">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-863">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-864">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-864">10001</span></span></td>
<td><span data-ttu-id="ffb44-865">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-865">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-866">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-866">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="ffb44-867">-713.75</span></span></td>
<td><span data-ttu-id="ffb44-868">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-869">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-870">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-870">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-871">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-871">10001</span></span></td>
<td><span data-ttu-id="ffb44-872">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-872">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-873">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-873">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-874">535.31</span><span class="sxs-lookup"><span data-stu-id="ffb44-874">535.31</span></span></td>
<td><span data-ttu-id="ffb44-875">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-876">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-877">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-877">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-878">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-878">10001</span></span></td>
<td><span data-ttu-id="ffb44-879">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-879">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-880">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-880">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-881">178.44</span><span class="sxs-lookup"><span data-stu-id="ffb44-881">178.44</span></span></td>
<td><span data-ttu-id="ffb44-882">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-883">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-883">CC003</span></span></td>
<td><span data-ttu-id="ffb44-884">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-884">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-885">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-885">10001</span></span></td>
<td><span data-ttu-id="ffb44-886">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-886">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-887">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-887">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="ffb44-888">-5,982.83</span></span></td>
<td><span data-ttu-id="ffb44-889">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-890">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-891">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-891">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-892">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-892">10001</span></span></td>
<td><span data-ttu-id="ffb44-893">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-893">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-894">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-894">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ffb44-895">4,487.12</span></span></td>
<td><span data-ttu-id="ffb44-896">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-897">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-898">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-898">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-899">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-899">10001</span></span></td>
<td><span data-ttu-id="ffb44-900">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-900">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-901">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-901">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ffb44-902">1,495.71</span></span></td>
<td><span data-ttu-id="ffb44-903">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-904">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-904">CC003</span></span></td>
<td><span data-ttu-id="ffb44-905">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-905">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-906">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-906">10001</span></span></td>
<td><span data-ttu-id="ffb44-907">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-907">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-908">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-908">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="ffb44-909">-286.25</span></span></td>
<td><span data-ttu-id="ffb44-910">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-911">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-912">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-912">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-913">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-913">10001</span></span></td>
<td><span data-ttu-id="ffb44-914">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-914">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-915">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-915">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-916">241.05</span><span class="sxs-lookup"><span data-stu-id="ffb44-916">241.05</span></span></td>
<td><span data-ttu-id="ffb44-917">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-918">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-919">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-919">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-920">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-920">10001</span></span></td>
<td><span data-ttu-id="ffb44-921">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-921">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-922">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-922">Fixed cost</span></span></td>
<td><span data-ttu-id="ffb44-923">45.20</span><span class="sxs-lookup"><span data-stu-id="ffb44-923">45.20</span></span></td>
<td><span data-ttu-id="ffb44-924">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-925">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-925">CC003</span></span></td>
<td><span data-ttu-id="ffb44-926">Assembleren</span><span class="sxs-lookup"><span data-stu-id="ffb44-926">Assembly</span></span></td>
<td><span data-ttu-id="ffb44-927">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-927">10001</span></span></td>
<td><span data-ttu-id="ffb44-928">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-928">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-929">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-929">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="ffb44-930">-2,977.17</span></span></td>
<td><span data-ttu-id="ffb44-931">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-932">Prod 1</span></span></td>
<td><span data-ttu-id="ffb44-933">Product 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-933">Product 1</span></span></td>
<td><span data-ttu-id="ffb44-934">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-934">10001</span></span></td>
<td><span data-ttu-id="ffb44-935">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-935">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-936">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-936">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ffb44-937">2,507.09</span></span></td>
<td><span data-ttu-id="ffb44-938">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb44-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-939">Prod 2</span></span></td>
<td><span data-ttu-id="ffb44-940">Product 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-940">Product 2</span></span></td>
<td><span data-ttu-id="ffb44-941">10001</span><span class="sxs-lookup"><span data-stu-id="ffb44-941">10001</span></span></td>
<td><span data-ttu-id="ffb44-942">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-942">Electricity</span></span></td>
<td><span data-ttu-id="ffb44-943">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-943">Variable cost</span></span></td>
<td><span data-ttu-id="ffb44-944">470.08</span><span class="sxs-lookup"><span data-stu-id="ffb44-944">470.08</span></span></td>
<td><span data-ttu-id="ffb44-945">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="ffb44-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="ffb44-946">Conclusie</span><span class="sxs-lookup"><span data-stu-id="ffb44-946">Conclusion</span></span>
<span data-ttu-id="ffb44-947">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="ffb44-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="ffb44-948">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="ffb44-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="ffb44-949">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ffb44-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="ffb44-950">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="ffb44-951">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="ffb44-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="ffb44-952">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="ffb44-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="ffb44-953">Totaal</span><span class="sxs-lookup"><span data-stu-id="ffb44-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ffb44-954">CC099</span><span class="sxs-lookup"><span data-stu-id="ffb44-954">CC099</span></span></th>
<th><span data-ttu-id="ffb44-955">CC001</span><span class="sxs-lookup"><span data-stu-id="ffb44-955">CC001</span></span></th>
<th><span data-ttu-id="ffb44-956">CC002</span><span class="sxs-lookup"><span data-stu-id="ffb44-956">CC002</span></span></th>
<th><span data-ttu-id="ffb44-957">CC003</span><span class="sxs-lookup"><span data-stu-id="ffb44-957">CC003</span></span></th>
<th><span data-ttu-id="ffb44-958">CC004</span><span class="sxs-lookup"><span data-stu-id="ffb44-958">CC004</span></span></th>
<th><span data-ttu-id="ffb44-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-959">Proj 1</span></span></th>
<th><span data-ttu-id="ffb44-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-960">Proj 2</span></span></th>
<th><span data-ttu-id="ffb44-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ffb44-961">Prod 1</span></span></th>
<th><span data-ttu-id="ffb44-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ffb44-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="ffb44-963">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="ffb44-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="ffb44-973">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="ffb44-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-974">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="ffb44-975">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-976">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-977">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-978">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-979">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-980">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-981">776.36</span><span class="sxs-lookup"><span data-stu-id="ffb44-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-982">223.64</span><span class="sxs-lookup"><span data-stu-id="ffb44-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="ffb44-984">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="ffb44-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-985">000</span><span class="sxs-lookup"><span data-stu-id="ffb44-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-986">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-987">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-988">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-989">0,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-990">30,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-991">10,00</span><span class="sxs-lookup"><span data-stu-id="ffb44-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ffb44-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ffb44-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ffb44-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ffb44-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ffb44-995">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="ffb44-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="ffb44-996">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="ffb44-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="ffb44-997">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="ffb44-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="ffb44-998">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="ffb44-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="ffb44-999">Zie Beleid voor kostenaggregatie voor meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="ffb44-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="ffb44-1000">(Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="ffb44-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




