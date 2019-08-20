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
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841484"
---
# <a name="overhead-calculation"></a><span data-ttu-id="07ef2-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="07ef2-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07ef2-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="07ef2-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="07ef2-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="07ef2-105">Term definition</span></span>
---------------

<span data-ttu-id="07ef2-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="07ef2-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="07ef2-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="07ef2-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="07ef2-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="07ef2-109">Huur</span><span class="sxs-lookup"><span data-stu-id="07ef2-109">Rent</span></span>
-   <span data-ttu-id="07ef2-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-110">Electricity</span></span>
-   <span data-ttu-id="07ef2-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="07ef2-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="07ef2-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="07ef2-112">Overhead calculation overview</span></span>
<span data-ttu-id="07ef2-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="07ef2-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="07ef2-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="07ef2-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="07ef2-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="07ef2-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="07ef2-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="07ef2-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="07ef2-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="07ef2-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="07ef2-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="07ef2-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="07ef2-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="07ef2-119">Version type</span></span>
-   <span data-ttu-id="07ef2-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="07ef2-120">Date and time</span></span>
-   <span data-ttu-id="07ef2-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="07ef2-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="07ef2-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="07ef2-122">Fiscal year</span></span>
-   <span data-ttu-id="07ef2-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="07ef2-123">Fiscal period</span></span>

<span data-ttu-id="07ef2-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="07ef2-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="07ef2-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="07ef2-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="07ef2-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="07ef2-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="07ef2-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="07ef2-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="07ef2-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="07ef2-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="07ef2-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="07ef2-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="07ef2-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="07ef2-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="07ef2-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="07ef2-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="07ef2-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="07ef2-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="07ef2-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="07ef2-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="07ef2-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="07ef2-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="07ef2-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="07ef2-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="07ef2-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="07ef2-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="07ef2-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="07ef2-140">Main account</span></span></th>
<th><span data-ttu-id="07ef2-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="07ef2-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="07ef2-143">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-143">CC099</span></span></td>
<td><span data-ttu-id="07ef2-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-144">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-145">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-145">10001</span></span></td>
<td><span data-ttu-id="07ef2-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-146">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="07ef2-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="07ef2-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="07ef2-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="07ef2-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="07ef2-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="07ef2-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="07ef2-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="07ef2-151">Define the cost behavior rule</span></span>

<span data-ttu-id="07ef2-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="07ef2-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="07ef2-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="07ef2-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="07ef2-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="07ef2-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="07ef2-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="07ef2-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="07ef2-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="07ef2-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="07ef2-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="07ef2-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="07ef2-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="07ef2-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-160">Journal</span></span></th>
<th><span data-ttu-id="07ef2-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="07ef2-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="07ef2-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="07ef2-163">Versie</span><span class="sxs-lookup"><span data-stu-id="07ef2-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-164">00001</span><span class="sxs-lookup"><span data-stu-id="07ef2-164">00001</span></span></td>
<td><span data-ttu-id="07ef2-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="07ef2-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-166">Fiscal</span></span></td>
<td><span data-ttu-id="07ef2-167">2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-167">2017</span></span></td>
<td><span data-ttu-id="07ef2-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-168">Period 1</span></span></td>
<td><span data-ttu-id="07ef2-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="07ef2-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="07ef2-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-173">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-174">Cost behavior</span></span></th>
<th><span data-ttu-id="07ef2-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="07ef2-177">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-177">CC099</span></span></td>
<td><span data-ttu-id="07ef2-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-178">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-179">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-179">10001</span></span></td>
<td><span data-ttu-id="07ef2-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-180">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="07ef2-181">Unclassified</span></span></td>
<td><span data-ttu-id="07ef2-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="07ef2-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="07ef2-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-185">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-186">Cost behavior</span></span></th>
<th><span data-ttu-id="07ef2-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-187">Amount</span></span></th>
<th><span data-ttu-id="07ef2-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-189">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-189">CC099</span></span></td>
<td><span data-ttu-id="07ef2-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-190">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-191">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-191">10001</span></span></td>
<td><span data-ttu-id="07ef2-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-192">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="07ef2-193">Unclassified</span></span></td>
<td><span data-ttu-id="07ef2-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-194">10,000.00</span></span></td>
<td><span data-ttu-id="07ef2-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-196">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-196">CC099</span></span></td>
<td><span data-ttu-id="07ef2-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-197">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-198">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-198">10001</span></span></td>
<td><span data-ttu-id="07ef2-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-199">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="07ef2-200">Unclassified</span></span></td>
<td><span data-ttu-id="07ef2-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-201">-10,000.00</span></span></td>
<td><span data-ttu-id="07ef2-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-203">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-203">CC099</span></span></td>
<td><span data-ttu-id="07ef2-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-204">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-205">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-205">10001</span></span></td>
<td><span data-ttu-id="07ef2-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-206">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-207">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-208">1,000.00</span></span></td>
<td><span data-ttu-id="07ef2-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-210">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-210">CC099</span></span></td>
<td><span data-ttu-id="07ef2-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-211">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-212">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-212">10001</span></span></td>
<td><span data-ttu-id="07ef2-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-213">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-214">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-215">9,000.00</span></span></td>
<td><span data-ttu-id="07ef2-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="07ef2-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="07ef2-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="07ef2-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="07ef2-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="07ef2-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="07ef2-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="07ef2-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="07ef2-221">Define the cost distribution rule</span></span>

<span data-ttu-id="07ef2-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="07ef2-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="07ef2-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="07ef2-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="07ef2-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="07ef2-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="07ef2-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="07ef2-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="07ef2-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="07ef2-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="07ef2-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-228">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="07ef2-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-230">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-230">CC001</span></span></td>
<td><span data-ttu-id="07ef2-231">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-231">HR</span></span></td>
<td><span data-ttu-id="07ef2-232">1.000</span><span class="sxs-lookup"><span data-stu-id="07ef2-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-233">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-233">CC002</span></span></td>
<td><span data-ttu-id="07ef2-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-234">Finance</span></span></td>
<td><span data-ttu-id="07ef2-235">6.000</span><span class="sxs-lookup"><span data-stu-id="07ef2-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-236">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-236">CC003</span></span></td>
<td><span data-ttu-id="07ef2-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-237">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-238">0</span><span class="sxs-lookup"><span data-stu-id="07ef2-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-240">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="07ef2-241">Magnitude</span></span></th>
<th><span data-ttu-id="07ef2-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="07ef2-242">Allocation factor</span></span></th>
<th><span data-ttu-id="07ef2-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-244">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-244">CC001</span></span></td>
<td><span data-ttu-id="07ef2-245">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-245">HR</span></span></td>
<td><span data-ttu-id="07ef2-246">1.000</span><span class="sxs-lookup"><span data-stu-id="07ef2-246">1,000</span></span></td>
<td><span data-ttu-id="07ef2-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="07ef2-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="07ef2-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-249">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-249">CC002</span></span></td>
<td><span data-ttu-id="07ef2-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-250">Finance</span></span></td>
<td><span data-ttu-id="07ef2-251">6.000</span><span class="sxs-lookup"><span data-stu-id="07ef2-251">6,000</span></span></td>
<td><span data-ttu-id="07ef2-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="07ef2-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="07ef2-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-254">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-254">CC003</span></span></td>
<td><span data-ttu-id="07ef2-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-255">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-256">0</span><span class="sxs-lookup"><span data-stu-id="07ef2-256">0</span></span></td>
<td><span data-ttu-id="07ef2-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="07ef2-258">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="07ef2-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="07ef2-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-261">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-262">Formule</span><span class="sxs-lookup"><span data-stu-id="07ef2-262">Formula</span></span></th>
<th><span data-ttu-id="07ef2-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="07ef2-263">Magnitude</span></span></th>
<th><span data-ttu-id="07ef2-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="07ef2-264">Allocation factor</span></span></th>
<th><span data-ttu-id="07ef2-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-266">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-266">CC001</span></span></td>
<td><span data-ttu-id="07ef2-267">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-267">HR</span></span></td>
<td><span data-ttu-id="07ef2-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="07ef2-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="07ef2-269">1</span><span class="sxs-lookup"><span data-stu-id="07ef2-269">1</span></span></td>
<td><span data-ttu-id="07ef2-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="07ef2-271">500,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-272">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-272">CC002</span></span></td>
<td><span data-ttu-id="07ef2-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-273">Finance</span></span></td>
<td><span data-ttu-id="07ef2-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="07ef2-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="07ef2-275">1</span><span class="sxs-lookup"><span data-stu-id="07ef2-275">1</span></span></td>
<td><span data-ttu-id="07ef2-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="07ef2-277">500,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-278">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-278">CC003</span></span></td>
<td><span data-ttu-id="07ef2-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-279">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="07ef2-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="07ef2-281">0</span><span class="sxs-lookup"><span data-stu-id="07ef2-281">0</span></span></td>
<td><span data-ttu-id="07ef2-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="07ef2-283">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="07ef2-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-285">Journal</span></span></th>
<th><span data-ttu-id="07ef2-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="07ef2-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="07ef2-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="07ef2-288">Versie</span><span class="sxs-lookup"><span data-stu-id="07ef2-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-289">00002</span><span class="sxs-lookup"><span data-stu-id="07ef2-289">00002</span></span></td>
<td><span data-ttu-id="07ef2-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="07ef2-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="07ef2-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-291">Fiscal</span></span></td>
<td><span data-ttu-id="07ef2-292">2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-292">2017</span></span></td>
<td><span data-ttu-id="07ef2-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-293">Period 1</span></span></td>
<td><span data-ttu-id="07ef2-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="07ef2-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="07ef2-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-298">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-299">Cost behavior</span></span></th>
<th><span data-ttu-id="07ef2-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-302">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-302">CC099</span></span></td>
<td><span data-ttu-id="07ef2-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-303">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-304">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-304">10001</span></span></td>
<td><span data-ttu-id="07ef2-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-305">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-306">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-309">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-309">CC099</span></span></td>
<td><span data-ttu-id="07ef2-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-310">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-311">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-311">10001</span></span></td>
<td><span data-ttu-id="07ef2-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-312">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-313">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="07ef2-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="07ef2-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-317">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-318">Cost behavior</span></span></th>
<th><span data-ttu-id="07ef2-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-319">Amount</span></span></th>
<th><span data-ttu-id="07ef2-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-321">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-321">CC099</span></span></td>
<td><span data-ttu-id="07ef2-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-322">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-323">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-323">10001</span></span></td>
<td><span data-ttu-id="07ef2-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-324">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-325">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-326">-1,000.00</span></span></td>
<td><span data-ttu-id="07ef2-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-328">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-328">CC001</span></span></td>
<td><span data-ttu-id="07ef2-329">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-329">HR</span></span></td>
<td><span data-ttu-id="07ef2-330">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-330">10001</span></span></td>
<td><span data-ttu-id="07ef2-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-331">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-332">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-333">500,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-333">500.00</span></span></td>
<td><span data-ttu-id="07ef2-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-335">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-335">CC002</span></span></td>
<td><span data-ttu-id="07ef2-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-336">Finance</span></span></td>
<td><span data-ttu-id="07ef2-337">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-337">10001</span></span></td>
<td><span data-ttu-id="07ef2-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-338">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-339">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-340">500,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-340">500.00</span></span></td>
<td><span data-ttu-id="07ef2-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-342">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-342">CC099</span></span></td>
<td><span data-ttu-id="07ef2-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="07ef2-343">Default cost center</span></span></td>
<td><span data-ttu-id="07ef2-344">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-344">10001</span></span></td>
<td><span data-ttu-id="07ef2-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-345">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-346">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-347">-9,000.00</span></span></td>
<td><span data-ttu-id="07ef2-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-349">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-349">CC001</span></span></td>
<td><span data-ttu-id="07ef2-350">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-350">HR</span></span></td>
<td><span data-ttu-id="07ef2-351">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-351">10001</span></span></td>
<td><span data-ttu-id="07ef2-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-352">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-353">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="07ef2-354">1,285.71</span></span></td>
<td><span data-ttu-id="07ef2-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-356">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-356">CC002</span></span></td>
<td><span data-ttu-id="07ef2-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-357">Finance</span></span></td>
<td><span data-ttu-id="07ef2-358">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-358">10001</span></span></td>
<td><span data-ttu-id="07ef2-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-359">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-360">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="07ef2-361">7,714.29</span></span></td>
<td><span data-ttu-id="07ef2-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="07ef2-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="07ef2-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="07ef2-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="07ef2-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="07ef2-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="07ef2-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="07ef2-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="07ef2-367">Define the overhead rate</span></span>

<span data-ttu-id="07ef2-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="07ef2-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-370">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-371">Uren</span><span class="sxs-lookup"><span data-stu-id="07ef2-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-372">Proj 1</span></span></td>
<td><span data-ttu-id="07ef2-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-373">Project 1</span></span></td>
<td><span data-ttu-id="07ef2-374">3</span><span class="sxs-lookup"><span data-stu-id="07ef2-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-375">Proj 2</span></span></td>
<td><span data-ttu-id="07ef2-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-376">Project 2</span></span></td>
<td><span data-ttu-id="07ef2-377">1</span><span class="sxs-lookup"><span data-stu-id="07ef2-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="07ef2-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-379">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-380">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-381">Cost behavior</span></span></th>
<th><span data-ttu-id="07ef2-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="07ef2-382">Units</span></span></th>
<th><span data-ttu-id="07ef2-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="07ef2-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-384">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-384">CC001</span></span></td>
<td><span data-ttu-id="07ef2-385">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-385">HR</span></span></td>
<td><span data-ttu-id="07ef2-386">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-386">10001</span></span></td>
<td><span data-ttu-id="07ef2-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-387">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-388">1</span><span class="sxs-lookup"><span data-stu-id="07ef2-388">1</span></span></td>
<td><span data-ttu-id="07ef2-389">10</span><span class="sxs-lookup"><span data-stu-id="07ef2-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="07ef2-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-391">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="07ef2-392">Magnitude</span></span></th>
<th><span data-ttu-id="07ef2-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-393">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="07ef2-394">Allocation factor</span></span></th>
<th><span data-ttu-id="07ef2-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-396">Proj 1</span></span></td>
<td><span data-ttu-id="07ef2-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-397">Project 1</span></span></td>
<td><span data-ttu-id="07ef2-398">3</span><span class="sxs-lookup"><span data-stu-id="07ef2-398">3</span></span></td>
<td><span data-ttu-id="07ef2-399">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-399">10001</span></span></td>
<td><span data-ttu-id="07ef2-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="07ef2-401">30,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-402">Proj 2</span></span></td>
<td><span data-ttu-id="07ef2-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-403">Project 2</span></span></td>
<td><span data-ttu-id="07ef2-404">1</span><span class="sxs-lookup"><span data-stu-id="07ef2-404">1</span></span></td>
<td><span data-ttu-id="07ef2-405">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-405">10001</span></span></td>
<td><span data-ttu-id="07ef2-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="07ef2-407">10,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="07ef2-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-409">Journal</span></span></th>
<th><span data-ttu-id="07ef2-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="07ef2-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="07ef2-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="07ef2-412">Versie</span><span class="sxs-lookup"><span data-stu-id="07ef2-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-413">00003</span><span class="sxs-lookup"><span data-stu-id="07ef2-413">00003</span></span></td>
<td><span data-ttu-id="07ef2-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="07ef2-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="07ef2-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-415">Fiscal</span></span></td>
<td><span data-ttu-id="07ef2-416">2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-416">2017</span></span></td>
<td><span data-ttu-id="07ef2-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-417">Period 1</span></span></td>
<td><span data-ttu-id="07ef2-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="07ef2-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="07ef2-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-421">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="07ef2-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-424">Proj 1</span></span></td>
<td><span data-ttu-id="07ef2-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="07ef2-426">3,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-428">Proj 2</span></span></td>
<td><span data-ttu-id="07ef2-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="07ef2-430">1,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="07ef2-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="07ef2-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-433">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-434">Cost behavior</span></span></th>
<th><span data-ttu-id="07ef2-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-435">Amount</span></span></th>
<th><span data-ttu-id="07ef2-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="07ef2-437">CC0001</span></span></td>
<td><span data-ttu-id="07ef2-438">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-438">HR</span></span></td>
<td><span data-ttu-id="07ef2-439">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-439">10001</span></span></td>
<td><span data-ttu-id="07ef2-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-440">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-441">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-442">-30.00</span></span></td>
<td><span data-ttu-id="07ef2-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-444">Proj 1</span></span></td>
<td><span data-ttu-id="07ef2-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="07ef2-446">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-446">10001</span></span></td>
<td><span data-ttu-id="07ef2-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-447">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-448">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-449">30,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-449">30.00</span></span></td>
<td><span data-ttu-id="07ef2-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-451">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-451">CC001</span></span></td>
<td><span data-ttu-id="07ef2-452">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-452">HR</span></span></td>
<td><span data-ttu-id="07ef2-453">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-453">10001</span></span></td>
<td><span data-ttu-id="07ef2-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-454">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-455">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-456">-10.00</span></span></td>
<td><span data-ttu-id="07ef2-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-458">Proj 2</span></span></td>
<td><span data-ttu-id="07ef2-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="07ef2-460">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-460">10001</span></span></td>
<td><span data-ttu-id="07ef2-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-461">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-462">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-463">10.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-463">10.00</span></span></td>
<td><span data-ttu-id="07ef2-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="07ef2-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="07ef2-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="07ef2-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="07ef2-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="07ef2-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="07ef2-468">Finance and Operations ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="07ef2-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="07ef2-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="07ef2-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="07ef2-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="07ef2-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="07ef2-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="07ef2-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="07ef2-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="07ef2-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="07ef2-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="07ef2-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="07ef2-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="07ef2-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="07ef2-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="07ef2-475">Define the cost allocation</span></span>

<span data-ttu-id="07ef2-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="07ef2-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="07ef2-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="07ef2-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-479">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="07ef2-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-481">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-481">CC002</span></span></td>
<td><span data-ttu-id="07ef2-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-482">Finance</span></span></td>
<td><span data-ttu-id="07ef2-483">35</span><span class="sxs-lookup"><span data-stu-id="07ef2-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-484">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-484">CC003</span></span></td>
<td><span data-ttu-id="07ef2-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-485">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-486">55</span><span class="sxs-lookup"><span data-stu-id="07ef2-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-487">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-487">CC004</span></span></td>
<td><span data-ttu-id="07ef2-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-488">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-489">10</span><span class="sxs-lookup"><span data-stu-id="07ef2-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="07ef2-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-492">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="07ef2-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-494">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-494">CC003</span></span></td>
<td><span data-ttu-id="07ef2-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-495">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-496">65</span><span class="sxs-lookup"><span data-stu-id="07ef2-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-497">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-497">CC004</span></span></td>
<td><span data-ttu-id="07ef2-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-498">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-499">35</span><span class="sxs-lookup"><span data-stu-id="07ef2-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="07ef2-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-502">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="07ef2-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-504">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-505">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-506">60</span><span class="sxs-lookup"><span data-stu-id="07ef2-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-507">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-508">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-509">20</span><span class="sxs-lookup"><span data-stu-id="07ef2-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="07ef2-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-512">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="07ef2-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-514">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-515">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-516">80</span><span class="sxs-lookup"><span data-stu-id="07ef2-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-517">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-518">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-519">15</span><span class="sxs-lookup"><span data-stu-id="07ef2-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="07ef2-520">In Finance and Operations kunnen statistische metingen, zoals de productie-uren die een product verbruikt, worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="07ef2-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="07ef2-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="07ef2-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="07ef2-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="07ef2-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-523">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="07ef2-524">Magnitude</span></span></th>
<th><span data-ttu-id="07ef2-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="07ef2-525">Allocation factor</span></span></th>
<th><span data-ttu-id="07ef2-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-526">Amount</span></span></th>
<th><span data-ttu-id="07ef2-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-528">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-528">CC002</span></span></td>
<td><span data-ttu-id="07ef2-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-529">Finance</span></span></td>
<td><span data-ttu-id="07ef2-530">35</span><span class="sxs-lookup"><span data-stu-id="07ef2-530">35</span></span></td>
<td><span data-ttu-id="07ef2-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="07ef2-532">175.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-532">175.00</span></span></td>
<td><span data-ttu-id="07ef2-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-534">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-534">CC003</span></span></td>
<td><span data-ttu-id="07ef2-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-535">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-536">55</span><span class="sxs-lookup"><span data-stu-id="07ef2-536">55</span></span></td>
<td><span data-ttu-id="07ef2-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="07ef2-538">275.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-538">275.00</span></span></td>
<td><span data-ttu-id="07ef2-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-540">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-540">CC004</span></span></td>
<td><span data-ttu-id="07ef2-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-541">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-542">10</span><span class="sxs-lookup"><span data-stu-id="07ef2-542">10</span></span></td>
<td><span data-ttu-id="07ef2-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="07ef2-544">50,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-544">50.00</span></span></td>
<td><span data-ttu-id="07ef2-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-546">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-546">CC002</span></span></td>
<td><span data-ttu-id="07ef2-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-547">Finance</span></span></td>
<td><span data-ttu-id="07ef2-548">35</span><span class="sxs-lookup"><span data-stu-id="07ef2-548">35</span></span></td>
<td><span data-ttu-id="07ef2-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="07ef2-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="07ef2-550">436.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-550">436.00</span></span></td>
<td><span data-ttu-id="07ef2-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-552">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-552">CC003</span></span></td>
<td><span data-ttu-id="07ef2-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-553">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-554">55</span><span class="sxs-lookup"><span data-stu-id="07ef2-554">55</span></span></td>
<td><span data-ttu-id="07ef2-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="07ef2-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="07ef2-556">685.14</span><span class="sxs-lookup"><span data-stu-id="07ef2-556">685.14</span></span></td>
<td><span data-ttu-id="07ef2-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-558">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-558">CC004</span></span></td>
<td><span data-ttu-id="07ef2-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-559">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-560">10</span><span class="sxs-lookup"><span data-stu-id="07ef2-560">10</span></span></td>
<td><span data-ttu-id="07ef2-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="07ef2-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="07ef2-562">124.57</span><span class="sxs-lookup"><span data-stu-id="07ef2-562">124.57</span></span></td>
<td><span data-ttu-id="07ef2-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="07ef2-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-565">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="07ef2-566">Magnitude</span></span></th>
<th><span data-ttu-id="07ef2-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="07ef2-567">Allocation factor</span></span></th>
<th><span data-ttu-id="07ef2-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-568">Amount</span></span></th>
<th><span data-ttu-id="07ef2-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-570">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-570">CC003</span></span></td>
<td><span data-ttu-id="07ef2-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-571">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-572">65</span><span class="sxs-lookup"><span data-stu-id="07ef2-572">65</span></span></td>
<td><span data-ttu-id="07ef2-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="07ef2-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="07ef2-574">438.75</span><span class="sxs-lookup"><span data-stu-id="07ef2-574">438.75</span></span></td>
<td><span data-ttu-id="07ef2-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-576">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-576">CC004</span></span></td>
<td><span data-ttu-id="07ef2-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-577">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-578">35</span><span class="sxs-lookup"><span data-stu-id="07ef2-578">35</span></span></td>
<td><span data-ttu-id="07ef2-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="07ef2-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="07ef2-580">236.25</span><span class="sxs-lookup"><span data-stu-id="07ef2-580">236.25</span></span></td>
<td><span data-ttu-id="07ef2-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-582">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-582">CC003</span></span></td>
<td><span data-ttu-id="07ef2-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-583">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-584">65</span><span class="sxs-lookup"><span data-stu-id="07ef2-584">65</span></span></td>
<td><span data-ttu-id="07ef2-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="07ef2-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="07ef2-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="07ef2-586">5,297.69</span></span></td>
<td><span data-ttu-id="07ef2-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-588">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-588">CC004</span></span></td>
<td><span data-ttu-id="07ef2-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-589">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-590">35</span><span class="sxs-lookup"><span data-stu-id="07ef2-590">35</span></span></td>
<td><span data-ttu-id="07ef2-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="07ef2-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="07ef2-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="07ef2-592">2,852.60</span></span></td>
<td><span data-ttu-id="07ef2-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="07ef2-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-595">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="07ef2-596">Magnitude</span></span></th>
<th><span data-ttu-id="07ef2-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="07ef2-597">Allocation factor</span></span></th>
<th><span data-ttu-id="07ef2-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-598">Amount</span></span></th>
<th><span data-ttu-id="07ef2-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-600">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-601">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-602">60</span><span class="sxs-lookup"><span data-stu-id="07ef2-602">60</span></span></td>
<td><span data-ttu-id="07ef2-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="07ef2-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="07ef2-604">535.31</span><span class="sxs-lookup"><span data-stu-id="07ef2-604">535.31</span></span></td>
<td><span data-ttu-id="07ef2-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-606">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-607">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-608">20</span><span class="sxs-lookup"><span data-stu-id="07ef2-608">20</span></span></td>
<td><span data-ttu-id="07ef2-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="07ef2-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="07ef2-610">178.44</span><span class="sxs-lookup"><span data-stu-id="07ef2-610">178.44</span></span></td>
<td><span data-ttu-id="07ef2-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-612">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-613">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-614">60</span><span class="sxs-lookup"><span data-stu-id="07ef2-614">60</span></span></td>
<td><span data-ttu-id="07ef2-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="07ef2-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="07ef2-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="07ef2-616">4,487.12</span></span></td>
<td><span data-ttu-id="07ef2-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-618">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-619">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-620">20</span><span class="sxs-lookup"><span data-stu-id="07ef2-620">20</span></span></td>
<td><span data-ttu-id="07ef2-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="07ef2-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="07ef2-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="07ef2-622">1,495.71</span></span></td>
<td><span data-ttu-id="07ef2-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07ef2-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="07ef2-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-625">Cost object</span></span></th>
<th><span data-ttu-id="07ef2-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="07ef2-626">Magnitude</span></span></th>
<th><span data-ttu-id="07ef2-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="07ef2-627">Allocation factor</span></span></th>
<th><span data-ttu-id="07ef2-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-628">Amount</span></span></th>
<th><span data-ttu-id="07ef2-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-630">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-631">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-632">80</span><span class="sxs-lookup"><span data-stu-id="07ef2-632">80</span></span></td>
<td><span data-ttu-id="07ef2-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="07ef2-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="07ef2-634">241.05</span><span class="sxs-lookup"><span data-stu-id="07ef2-634">241.05</span></span></td>
<td><span data-ttu-id="07ef2-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-636">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-637">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-638">15</span><span class="sxs-lookup"><span data-stu-id="07ef2-638">15</span></span></td>
<td><span data-ttu-id="07ef2-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="07ef2-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="07ef2-640">45.20</span><span class="sxs-lookup"><span data-stu-id="07ef2-640">45.20</span></span></td>
<td><span data-ttu-id="07ef2-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-642">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-643">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-644">80</span><span class="sxs-lookup"><span data-stu-id="07ef2-644">80</span></span></td>
<td><span data-ttu-id="07ef2-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="07ef2-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="07ef2-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="07ef2-646">2,507.09</span></span></td>
<td><span data-ttu-id="07ef2-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-648">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-649">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-650">15</span><span class="sxs-lookup"><span data-stu-id="07ef2-650">15</span></span></td>
<td><span data-ttu-id="07ef2-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="07ef2-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="07ef2-652">470.08</span><span class="sxs-lookup"><span data-stu-id="07ef2-652">470.08</span></span></td>
<td><span data-ttu-id="07ef2-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="07ef2-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="07ef2-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-655">Journal</span></span></th>
<th><span data-ttu-id="07ef2-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="07ef2-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="07ef2-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="07ef2-658">Versie</span><span class="sxs-lookup"><span data-stu-id="07ef2-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-659">00004</span><span class="sxs-lookup"><span data-stu-id="07ef2-659">00004</span></span></td>
<td><span data-ttu-id="07ef2-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="07ef2-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-661">Fiscal</span></span></td>
<td><span data-ttu-id="07ef2-662">2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-662">2017</span></span></td>
<td><span data-ttu-id="07ef2-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-663">Period 1</span></span></td>
<td><span data-ttu-id="07ef2-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="07ef2-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="07ef2-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07ef2-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-668">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-669">Cost behavior</span></span></th>
<th><span data-ttu-id="07ef2-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-672">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-672">CC001</span></span></td>
<td><span data-ttu-id="07ef2-673">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-673">HR</span></span></td>
<td><span data-ttu-id="07ef2-674">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-674">10001</span></span></td>
<td><span data-ttu-id="07ef2-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-675">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-676">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-677">500,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-679">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-679">CC001</span></span></td>
<td><span data-ttu-id="07ef2-680">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-680">HR</span></span></td>
<td><span data-ttu-id="07ef2-681">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-681">10001</span></span></td>
<td><span data-ttu-id="07ef2-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-682">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-683">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="07ef2-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-686">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-686">CC002</span></span></td>
<td><span data-ttu-id="07ef2-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-687">Finance</span></span></td>
<td><span data-ttu-id="07ef2-688">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-688">10001</span></span></td>
<td><span data-ttu-id="07ef2-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-689">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-690">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-691">675.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-693">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-693">CC002</span></span></td>
<td><span data-ttu-id="07ef2-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-694">Finance</span></span></td>
<td><span data-ttu-id="07ef2-695">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-695">10001</span></span></td>
<td><span data-ttu-id="07ef2-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-696">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-697">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="07ef2-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-700">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-700">CC003</span></span></td>
<td><span data-ttu-id="07ef2-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-701">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-702">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-702">10001</span></span></td>
<td><span data-ttu-id="07ef2-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-703">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-704">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-705">713.75</span><span class="sxs-lookup"><span data-stu-id="07ef2-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-707">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-707">CC003</span></span></td>
<td><span data-ttu-id="07ef2-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-708">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-709">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-709">10001</span></span></td>
<td><span data-ttu-id="07ef2-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-710">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-711">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="07ef2-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-714">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-714">CC003</span></span></td>
<td><span data-ttu-id="07ef2-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-715">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-716">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-716">10001</span></span></td>
<td><span data-ttu-id="07ef2-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-717">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-718">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-719">286.25</span><span class="sxs-lookup"><span data-stu-id="07ef2-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-721">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-721">CC003</span></span></td>
<td><span data-ttu-id="07ef2-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-722">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-723">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-723">10001</span></span></td>
<td><span data-ttu-id="07ef2-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-724">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-725">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="07ef2-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-728">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-729">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-730">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-730">10001</span></span></td>
<td><span data-ttu-id="07ef2-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-731">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-732">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-733">776.36</span><span class="sxs-lookup"><span data-stu-id="07ef2-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-735">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-736">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-737">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-737">10001</span></span></td>
<td><span data-ttu-id="07ef2-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-738">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-739">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="07ef2-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-742">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-743">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-744">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-744">10001</span></span></td>
<td><span data-ttu-id="07ef2-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-745">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-746">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-747">223.64</span><span class="sxs-lookup"><span data-stu-id="07ef2-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="07ef2-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-749">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-750">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-751">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-751">10001</span></span></td>
<td><span data-ttu-id="07ef2-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-752">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-753">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="07ef2-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="07ef2-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="07ef2-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07ef2-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07ef2-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-757">Cost element</span></span></th>
<th><span data-ttu-id="07ef2-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-758">Cost behavior</span></span></th>
<th><span data-ttu-id="07ef2-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="07ef2-759">Amount</span></span></th>
<th><span data-ttu-id="07ef2-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="07ef2-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07ef2-761">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-761">CC001</span></span></td>
<td><span data-ttu-id="07ef2-762">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-762">HR</span></span></td>
<td><span data-ttu-id="07ef2-763">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-763">10001</span></span></td>
<td><span data-ttu-id="07ef2-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-764">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-765">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-766">-500.00</span></span></td>
<td><span data-ttu-id="07ef2-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-768">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-768">CC002</span></span></td>
<td><span data-ttu-id="07ef2-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-769">Finance</span></span></td>
<td><span data-ttu-id="07ef2-770">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-770">10001</span></span></td>
<td><span data-ttu-id="07ef2-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-771">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-772">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-773">175.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-773">175.00</span></span></td>
<td><span data-ttu-id="07ef2-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-775">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-775">CC003</span></span></td>
<td><span data-ttu-id="07ef2-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-776">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-777">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-777">10001</span></span></td>
<td><span data-ttu-id="07ef2-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-778">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-779">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-780">275.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-780">275.00</span></span></td>
<td><span data-ttu-id="07ef2-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-782">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-782">CC004</span></span></td>
<td><span data-ttu-id="07ef2-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-783">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-784">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-784">10001</span></span></td>
<td><span data-ttu-id="07ef2-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-785">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-786">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-787">50,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-787">50,00</span></span></td>
<td><span data-ttu-id="07ef2-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-789">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-789">CC001</span></span></td>
<td><span data-ttu-id="07ef2-790">HR</span><span class="sxs-lookup"><span data-stu-id="07ef2-790">HR</span></span></td>
<td><span data-ttu-id="07ef2-791">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-791">10001</span></span></td>
<td><span data-ttu-id="07ef2-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-792">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-793">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="07ef2-794">-1,245.71</span></span></td>
<td><span data-ttu-id="07ef2-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-796">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-796">CC002</span></span></td>
<td><span data-ttu-id="07ef2-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-797">Finance</span></span></td>
<td><span data-ttu-id="07ef2-798">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-798">10001</span></span></td>
<td><span data-ttu-id="07ef2-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-799">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-800">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-801">436.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-801">436.00</span></span></td>
<td><span data-ttu-id="07ef2-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-803">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-803">CC003</span></span></td>
<td><span data-ttu-id="07ef2-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-804">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-805">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-805">10001</span></span></td>
<td><span data-ttu-id="07ef2-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-806">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-807">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-808">685.14</span><span class="sxs-lookup"><span data-stu-id="07ef2-808">685.14</span></span></td>
<td><span data-ttu-id="07ef2-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-810">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-810">CC004</span></span></td>
<td><span data-ttu-id="07ef2-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-811">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-812">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-812">10001</span></span></td>
<td><span data-ttu-id="07ef2-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-813">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-814">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-815">124.57</span><span class="sxs-lookup"><span data-stu-id="07ef2-815">124.57</span></span></td>
<td><span data-ttu-id="07ef2-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-817">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-817">CC002</span></span></td>
<td><span data-ttu-id="07ef2-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-818">Finance</span></span></td>
<td><span data-ttu-id="07ef2-819">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-819">10001</span></span></td>
<td><span data-ttu-id="07ef2-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-820">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-821">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="07ef2-822">-675.00</span></span></td>
<td><span data-ttu-id="07ef2-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-824">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-824">CC003</span></span></td>
<td><span data-ttu-id="07ef2-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-825">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-826">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-826">10001</span></span></td>
<td><span data-ttu-id="07ef2-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-827">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-828">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-829">438.75</span><span class="sxs-lookup"><span data-stu-id="07ef2-829">438.75</span></span></td>
<td><span data-ttu-id="07ef2-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-831">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-831">CC004</span></span></td>
<td><span data-ttu-id="07ef2-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-832">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-833">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-833">10001</span></span></td>
<td><span data-ttu-id="07ef2-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-834">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-835">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-836">236.25</span><span class="sxs-lookup"><span data-stu-id="07ef2-836">236.25</span></span></td>
<td><span data-ttu-id="07ef2-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-838">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-838">CC002</span></span></td>
<td><span data-ttu-id="07ef2-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="07ef2-839">Finance</span></span></td>
<td><span data-ttu-id="07ef2-840">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-840">10001</span></span></td>
<td><span data-ttu-id="07ef2-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-841">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-842">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="07ef2-843">-8,150.29</span></span></td>
<td><span data-ttu-id="07ef2-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-845">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-845">CC003</span></span></td>
<td><span data-ttu-id="07ef2-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-846">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-847">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-847">10001</span></span></td>
<td><span data-ttu-id="07ef2-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-848">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-849">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="07ef2-850">5,297.69</span></span></td>
<td><span data-ttu-id="07ef2-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-852">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-852">CC004</span></span></td>
<td><span data-ttu-id="07ef2-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="07ef2-853">Packaging</span></span></td>
<td><span data-ttu-id="07ef2-854">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-854">10001</span></span></td>
<td><span data-ttu-id="07ef2-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-855">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-856">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="07ef2-857">2,852.60</span></span></td>
<td><span data-ttu-id="07ef2-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-859">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-859">CC003</span></span></td>
<td><span data-ttu-id="07ef2-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-860">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-861">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-861">10001</span></span></td>
<td><span data-ttu-id="07ef2-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-862">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-863">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="07ef2-864">-713.75</span></span></td>
<td><span data-ttu-id="07ef2-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-866">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-867">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-868">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-868">10001</span></span></td>
<td><span data-ttu-id="07ef2-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-869">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-870">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-871">535.31</span><span class="sxs-lookup"><span data-stu-id="07ef2-871">535.31</span></span></td>
<td><span data-ttu-id="07ef2-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-873">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-874">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-875">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-875">10001</span></span></td>
<td><span data-ttu-id="07ef2-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-876">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-877">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-878">178.44</span><span class="sxs-lookup"><span data-stu-id="07ef2-878">178.44</span></span></td>
<td><span data-ttu-id="07ef2-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-880">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-880">CC003</span></span></td>
<td><span data-ttu-id="07ef2-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-881">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-882">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-882">10001</span></span></td>
<td><span data-ttu-id="07ef2-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-883">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-884">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="07ef2-885">-5,982.83</span></span></td>
<td><span data-ttu-id="07ef2-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-887">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-888">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-889">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-889">10001</span></span></td>
<td><span data-ttu-id="07ef2-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-890">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-891">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="07ef2-892">4,487.12</span></span></td>
<td><span data-ttu-id="07ef2-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-894">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-895">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-896">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-896">10001</span></span></td>
<td><span data-ttu-id="07ef2-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-897">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-898">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="07ef2-899">1,495.71</span></span></td>
<td><span data-ttu-id="07ef2-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-901">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-901">CC003</span></span></td>
<td><span data-ttu-id="07ef2-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-902">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-903">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-903">10001</span></span></td>
<td><span data-ttu-id="07ef2-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-904">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-905">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="07ef2-906">-286.25</span></span></td>
<td><span data-ttu-id="07ef2-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-908">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-909">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-910">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-910">10001</span></span></td>
<td><span data-ttu-id="07ef2-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-911">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-912">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-913">241.05</span><span class="sxs-lookup"><span data-stu-id="07ef2-913">241.05</span></span></td>
<td><span data-ttu-id="07ef2-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-915">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-916">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-917">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-917">10001</span></span></td>
<td><span data-ttu-id="07ef2-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-918">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-919">Fixed cost</span></span></td>
<td><span data-ttu-id="07ef2-920">45.20</span><span class="sxs-lookup"><span data-stu-id="07ef2-920">45.20</span></span></td>
<td><span data-ttu-id="07ef2-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-922">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-922">CC003</span></span></td>
<td><span data-ttu-id="07ef2-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="07ef2-923">Assembly</span></span></td>
<td><span data-ttu-id="07ef2-924">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-924">10001</span></span></td>
<td><span data-ttu-id="07ef2-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-925">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-926">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="07ef2-927">-2,977.17</span></span></td>
<td><span data-ttu-id="07ef2-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-929">Prod 1</span></span></td>
<td><span data-ttu-id="07ef2-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-930">Product 1</span></span></td>
<td><span data-ttu-id="07ef2-931">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-931">10001</span></span></td>
<td><span data-ttu-id="07ef2-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-932">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-933">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="07ef2-934">2,507.09</span></span></td>
<td><span data-ttu-id="07ef2-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07ef2-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-936">Prod 2</span></span></td>
<td><span data-ttu-id="07ef2-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-937">Product 2</span></span></td>
<td><span data-ttu-id="07ef2-938">10001</span><span class="sxs-lookup"><span data-stu-id="07ef2-938">10001</span></span></td>
<td><span data-ttu-id="07ef2-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-939">Electricity</span></span></td>
<td><span data-ttu-id="07ef2-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-940">Variable cost</span></span></td>
<td><span data-ttu-id="07ef2-941">470.08</span><span class="sxs-lookup"><span data-stu-id="07ef2-941">470.08</span></span></td>
<td><span data-ttu-id="07ef2-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="07ef2-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="07ef2-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="07ef2-943">Conclusion</span></span>
<span data-ttu-id="07ef2-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="07ef2-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="07ef2-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="07ef2-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="07ef2-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="07ef2-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="07ef2-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="07ef2-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="07ef2-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="07ef2-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="07ef2-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="07ef2-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="07ef2-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="07ef2-951">CC099</span><span class="sxs-lookup"><span data-stu-id="07ef2-951">CC099</span></span></th>
<th><span data-ttu-id="07ef2-952">CC001</span><span class="sxs-lookup"><span data-stu-id="07ef2-952">CC001</span></span></th>
<th><span data-ttu-id="07ef2-953">CC002</span><span class="sxs-lookup"><span data-stu-id="07ef2-953">CC002</span></span></th>
<th><span data-ttu-id="07ef2-954">CC003</span><span class="sxs-lookup"><span data-stu-id="07ef2-954">CC003</span></span></th>
<th><span data-ttu-id="07ef2-955">CC004</span><span class="sxs-lookup"><span data-stu-id="07ef2-955">CC004</span></span></th>
<th><span data-ttu-id="07ef2-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-956">Proj 1</span></span></th>
<th><span data-ttu-id="07ef2-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-957">Proj 2</span></span></th>
<th><span data-ttu-id="07ef2-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="07ef2-958">Prod 1</span></span></th>
<th><span data-ttu-id="07ef2-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="07ef2-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="07ef2-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="07ef2-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="07ef2-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="07ef2-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-971">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="07ef2-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-973">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-974">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-975">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-976">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-977">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-978">776.36</span><span class="sxs-lookup"><span data-stu-id="07ef2-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-979">223.64</span><span class="sxs-lookup"><span data-stu-id="07ef2-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="07ef2-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="07ef2-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-982">000</span><span class="sxs-lookup"><span data-stu-id="07ef2-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-983">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-984">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-985">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-986">0,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-987">30,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-988">10,00</span><span class="sxs-lookup"><span data-stu-id="07ef2-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="07ef2-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="07ef2-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07ef2-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="07ef2-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="07ef2-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="07ef2-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="07ef2-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="07ef2-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="07ef2-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="07ef2-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="07ef2-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="07ef2-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="07ef2-996">Zie [Kostentotalisatie](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="07ef2-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



