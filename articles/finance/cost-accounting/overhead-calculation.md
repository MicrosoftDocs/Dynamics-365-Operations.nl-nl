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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177175"
---
# <a name="overhead-calculation"></a><span data-ttu-id="7ecc4-103">Overheadberekening</span><span class="sxs-lookup"><span data-stu-id="7ecc4-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ecc4-104">In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="7ecc4-105">Definitie van term</span><span class="sxs-lookup"><span data-stu-id="7ecc4-105">Term definition</span></span>
---------------

<span data-ttu-id="7ecc4-106">Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="7ecc4-107">Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="7ecc4-108">Hieronder staan enkele voorbeelden van overheadkosten:</span><span class="sxs-lookup"><span data-stu-id="7ecc4-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="7ecc4-109">Huur</span><span class="sxs-lookup"><span data-stu-id="7ecc4-109">Rent</span></span>
-   <span data-ttu-id="7ecc4-110">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-110">Electricity</span></span>
-   <span data-ttu-id="7ecc4-111">Administratieve salarissen</span><span class="sxs-lookup"><span data-stu-id="7ecc4-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="7ecc4-112">Overzicht van overheadberekening</span><span class="sxs-lookup"><span data-stu-id="7ecc4-112">Overhead calculation overview</span></span>
<span data-ttu-id="7ecc4-113">Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="7ecc4-114">U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="7ecc4-115">Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="7ecc4-116">De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="7ecc4-117">Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="7ecc4-118">De unieke versie-id bestaat uit de volgende elementen:</span><span class="sxs-lookup"><span data-stu-id="7ecc4-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="7ecc4-119">Versietype</span><span class="sxs-lookup"><span data-stu-id="7ecc4-119">Version type</span></span>
-   <span data-ttu-id="7ecc4-120">Datum en tijd</span><span class="sxs-lookup"><span data-stu-id="7ecc4-120">Date and time</span></span>
-   <span data-ttu-id="7ecc4-121">Grootboek van kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="7ecc4-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="7ecc4-122">Boekjaar</span><span class="sxs-lookup"><span data-stu-id="7ecc4-122">Fiscal year</span></span>
-   <span data-ttu-id="7ecc4-123">Boekperiode</span><span class="sxs-lookup"><span data-stu-id="7ecc4-123">Fiscal period</span></span>

<span data-ttu-id="7ecc4-124">De overheadberekening wordt onafhankelijk van de versie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="7ecc4-125">Daarom kunt u de budgetversie vóór de huidige versie berekenen.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="7ecc4-126">De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="7ecc4-127">In elke stap wordt een journaalkop gemaakt met journaalposten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="7ecc4-128">Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="7ecc4-129">Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="7ecc4-130">Daarom beschikt u altijd over volledige traceerbaarheid.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="7ecc4-131">[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="7ecc4-132">De overheadkosten voor elektriciteit berekenen en toewijzen</span><span class="sxs-lookup"><span data-stu-id="7ecc4-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="7ecc4-133">In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="7ecc4-134">Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="7ecc4-135">Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="7ecc4-136">Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="7ecc4-137">In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-138">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-139">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-140">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="7ecc4-140">Main account</span></span></th>
<th><span data-ttu-id="7ecc4-141">Bedrag in de boekhoudingsvaluta</span><span class="sxs-lookup"><span data-stu-id="7ecc4-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-142">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-143">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-143">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-144">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-144">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-145">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-145">10001</span></span></td>
<td><span data-ttu-id="7ecc4-146">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-146">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="7ecc4-148">Stap 1: Het gedrag voor kostenberekening verwerken</span><span class="sxs-lookup"><span data-stu-id="7ecc4-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="7ecc4-149">Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="7ecc4-150">Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="7ecc4-151">De regel voor kostengedrag definiëren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-151">Define the cost behavior rule</span></span>

<span data-ttu-id="7ecc4-152">In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="7ecc4-153">Elektriciteitrekeningen voldoen vaak aan deze definitie.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="7ecc4-154">Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh).</span><span class="sxs-lookup"><span data-stu-id="7ecc4-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="7ecc4-155">Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="7ecc4-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="7ecc4-156">Vast bedrag 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="7ecc4-157">0 &lt;= 1.000,00 = Vast</span><span class="sxs-lookup"><span data-stu-id="7ecc4-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="7ecc4-158">1.000,01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="7ecc4-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="7ecc4-159">Journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-160">Journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-160">Journal</span></span></th>
<th><span data-ttu-id="7ecc4-161">Type journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7ecc4-162">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="7ecc4-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7ecc4-163">Versie</span><span class="sxs-lookup"><span data-stu-id="7ecc4-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-164">00001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-164">00001</span></span></td>
<td><span data-ttu-id="7ecc4-165">Journaal van berekening kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="7ecc4-166">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-166">Fiscal</span></span></td>
<td><span data-ttu-id="7ecc4-167">2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-167">2017</span></span></td>
<td><span data-ttu-id="7ecc4-168">Periode 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-168">Period 1</span></span></td>
<td><span data-ttu-id="7ecc4-169">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7ecc4-170">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-171">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-172">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-173">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-173">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-174">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-174">Cost behavior</span></span></th>
<th><span data-ttu-id="7ecc4-175">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-176">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-177">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-177">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-178">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-178">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-179">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-179">10001</span></span></td>
<td><span data-ttu-id="7ecc4-180">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-180">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-181">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="7ecc4-181">Unclassified</span></span></td>
<td><span data-ttu-id="7ecc4-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7ecc4-183">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="7ecc4-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-184">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-185">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-185">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-186">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-186">Cost behavior</span></span></th>
<th><span data-ttu-id="7ecc4-187">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-187">Amount</span></span></th>
<th><span data-ttu-id="7ecc4-188">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-189">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-189">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-190">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-190">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-191">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-191">10001</span></span></td>
<td><span data-ttu-id="7ecc4-192">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-192">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-193">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="7ecc4-193">Unclassified</span></span></td>
<td><span data-ttu-id="7ecc4-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-194">10,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-195">3 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-196">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-196">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-197">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-197">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-198">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-198">10001</span></span></td>
<td><span data-ttu-id="7ecc4-199">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-199">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-200">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="7ecc4-200">Unclassified</span></span></td>
<td><span data-ttu-id="7ecc4-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-201">-10,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-202">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-203">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-203">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-204">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-204">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-205">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-205">10001</span></span></td>
<td><span data-ttu-id="7ecc4-206">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-206">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-207">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-207">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-208">1,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-209">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-210">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-210">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-211">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-211">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-212">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-212">10001</span></span></td>
<td><span data-ttu-id="7ecc4-213">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-213">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-214">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-214">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-215">9,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-216">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-217">Zie [Een kostengedragbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-behavior-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="7ecc4-218">Stap 2: De berekening van kostenverdeling verwerken</span><span class="sxs-lookup"><span data-stu-id="7ecc4-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="7ecc4-219">Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="7ecc4-220">Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="7ecc4-221">De regel voor kostenverdeling definiëren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-221">Define the cost distribution rule</span></span>

<span data-ttu-id="7ecc4-222">In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="7ecc4-223">In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="7ecc4-224">De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="7ecc4-225">De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh).</span><span class="sxs-lookup"><span data-stu-id="7ecc4-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="7ecc4-226">Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="7ecc4-227">Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-228">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-228">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="7ecc4-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-230">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-230">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-231">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-231">HR</span></span></td>
<td><span data-ttu-id="7ecc4-232">1.000</span><span class="sxs-lookup"><span data-stu-id="7ecc4-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-233">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-233">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-234">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-234">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-235">6.000</span><span class="sxs-lookup"><span data-stu-id="7ecc4-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-236">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-236">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-237">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-237">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-238">0</span><span class="sxs-lookup"><span data-stu-id="7ecc4-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-239">De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-240">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-240">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-241">Magnitude</span><span class="sxs-lookup"><span data-stu-id="7ecc4-241">Magnitude</span></span></th>
<th><span data-ttu-id="7ecc4-242">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="7ecc4-242">Allocation factor</span></span></th>
<th><span data-ttu-id="7ecc4-243">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-244">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-244">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-245">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-245">HR</span></span></td>
<td><span data-ttu-id="7ecc4-246">1.000</span><span class="sxs-lookup"><span data-stu-id="7ecc4-246">1,000</span></span></td>
<td><span data-ttu-id="7ecc4-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-249">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-249">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-250">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-250">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-251">6.000</span><span class="sxs-lookup"><span data-stu-id="7ecc4-251">6,000</span></span></td>
<td><span data-ttu-id="7ecc4-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7ecc4-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-254">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-254">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-255">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-255">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-256">0</span><span class="sxs-lookup"><span data-stu-id="7ecc4-256">0</span></span></td>
<td><span data-ttu-id="7ecc4-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-258">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-259">De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="7ecc4-260">U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-261">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-261">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-262">Formule</span><span class="sxs-lookup"><span data-stu-id="7ecc4-262">Formula</span></span></th>
<th><span data-ttu-id="7ecc4-263">Magnitude</span><span class="sxs-lookup"><span data-stu-id="7ecc4-263">Magnitude</span></span></th>
<th><span data-ttu-id="7ecc4-264">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="7ecc4-264">Allocation factor</span></span></th>
<th><span data-ttu-id="7ecc4-265">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-266">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-266">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-267">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-267">HR</span></span></td>
<td><span data-ttu-id="7ecc4-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7ecc4-269">1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-269">1</span></span></td>
<td><span data-ttu-id="7ecc4-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-271">500,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-272">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-272">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-273">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-273">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7ecc4-275">1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-275">1</span></span></td>
<td><span data-ttu-id="7ecc4-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-277">500,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-278">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-278">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-279">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-279">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7ecc4-281">0</span><span class="sxs-lookup"><span data-stu-id="7ecc4-281">0</span></span></td>
<td><span data-ttu-id="7ecc4-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-283">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7ecc4-284">Journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-285">Journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-285">Journal</span></span></th>
<th><span data-ttu-id="7ecc4-286">Type journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7ecc4-287">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="7ecc4-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7ecc4-288">Versie</span><span class="sxs-lookup"><span data-stu-id="7ecc4-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-289">00002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-289">00002</span></span></td>
<td><span data-ttu-id="7ecc4-290">Berekeningsjournaal voor kostenverdeling</span><span class="sxs-lookup"><span data-stu-id="7ecc4-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="7ecc4-291">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-291">Fiscal</span></span></td>
<td><span data-ttu-id="7ecc4-292">2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-292">2017</span></span></td>
<td><span data-ttu-id="7ecc4-293">Periode 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-293">Period 1</span></span></td>
<td><span data-ttu-id="7ecc4-294">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7ecc4-295">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-296">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-297">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-298">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-298">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-299">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-299">Cost behavior</span></span></th>
<th><span data-ttu-id="7ecc4-300">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-301">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-302">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-302">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-303">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-303">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-304">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-304">10001</span></span></td>
<td><span data-ttu-id="7ecc4-305">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-305">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-306">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-306">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-308">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-309">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-309">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-310">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-310">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-311">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-311">10001</span></span></td>
<td><span data-ttu-id="7ecc4-312">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-312">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-313">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-313">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7ecc4-315">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="7ecc4-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-316">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-317">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-317">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-318">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-318">Cost behavior</span></span></th>
<th><span data-ttu-id="7ecc4-319">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-319">Amount</span></span></th>
<th><span data-ttu-id="7ecc4-320">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-321">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-321">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-322">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-322">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-323">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-323">10001</span></span></td>
<td><span data-ttu-id="7ecc4-324">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-324">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-325">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-325">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-326">-1,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-327">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-328">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-328">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-329">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-329">HR</span></span></td>
<td><span data-ttu-id="7ecc4-330">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-330">10001</span></span></td>
<td><span data-ttu-id="7ecc4-331">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-331">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-332">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-332">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-333">500,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-333">500.00</span></span></td>
<td><span data-ttu-id="7ecc4-334">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-335">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-335">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-336">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-336">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-337">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-337">10001</span></span></td>
<td><span data-ttu-id="7ecc4-338">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-338">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-339">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-339">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-340">500,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-340">500.00</span></span></td>
<td><span data-ttu-id="7ecc4-341">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-342">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-342">CC099</span></span></td>
<td><span data-ttu-id="7ecc4-343">Standaardkostenplaats</span><span class="sxs-lookup"><span data-stu-id="7ecc4-343">Default cost center</span></span></td>
<td><span data-ttu-id="7ecc4-344">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-344">10001</span></span></td>
<td><span data-ttu-id="7ecc4-345">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-345">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-346">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-346">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-347">-9,000.00</span></span></td>
<td><span data-ttu-id="7ecc4-348">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-349">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-349">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-350">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-350">HR</span></span></td>
<td><span data-ttu-id="7ecc4-351">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-351">10001</span></span></td>
<td><span data-ttu-id="7ecc4-352">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-352">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-353">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-353">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-354">1,285.71</span></span></td>
<td><span data-ttu-id="7ecc4-355">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-356">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-356">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-357">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-357">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-358">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-358">10001</span></span></td>
<td><span data-ttu-id="7ecc4-359">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-359">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-360">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-360">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7ecc4-361">7,714.29</span></span></td>
<td><span data-ttu-id="7ecc4-362">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-363">Zie [Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="7ecc4-364">Stap 3: De berekening van overheadtarieven verwerken</span><span class="sxs-lookup"><span data-stu-id="7ecc4-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="7ecc4-365">Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="7ecc4-366">De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="7ecc4-367">Het overheadtarief definiëren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-367">Define the overhead rate</span></span>

<span data-ttu-id="7ecc4-368">Kostenobject CC001 HR draagt bij aan een reeks van interne projecten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="7ecc4-369">Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-370">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-370">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-371">Uren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-372">Proj 1</span></span></td>
<td><span data-ttu-id="7ecc4-373">Project 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-373">Project 1</span></span></td>
<td><span data-ttu-id="7ecc4-374">3</span><span class="sxs-lookup"><span data-stu-id="7ecc4-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-375">Proj 2</span></span></td>
<td><span data-ttu-id="7ecc4-376">Project 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-376">Project 2</span></span></td>
<td><span data-ttu-id="7ecc4-377">1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-378">Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-379">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-379">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-380">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-380">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-381">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-381">Cost behavior</span></span></th>
<th><span data-ttu-id="7ecc4-382">Eenheden</span><span class="sxs-lookup"><span data-stu-id="7ecc4-382">Units</span></span></th>
<th><span data-ttu-id="7ecc4-383">Tarief</span><span class="sxs-lookup"><span data-stu-id="7ecc4-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-384">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-384">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-385">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-385">HR</span></span></td>
<td><span data-ttu-id="7ecc4-386">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-386">10001</span></span></td>
<td><span data-ttu-id="7ecc4-387">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-387">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-388">1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-388">1</span></span></td>
<td><span data-ttu-id="7ecc4-389">10</span><span class="sxs-lookup"><span data-stu-id="7ecc4-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-390">De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-391">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-391">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-392">Magnitude</span><span class="sxs-lookup"><span data-stu-id="7ecc4-392">Magnitude</span></span></th>
<th><span data-ttu-id="7ecc4-393">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-393">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-394">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="7ecc4-394">Allocation factor</span></span></th>
<th><span data-ttu-id="7ecc4-395">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-396">Proj 1</span></span></td>
<td><span data-ttu-id="7ecc4-397">Project 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-397">Project 1</span></span></td>
<td><span data-ttu-id="7ecc4-398">3</span><span class="sxs-lookup"><span data-stu-id="7ecc4-398">3</span></span></td>
<td><span data-ttu-id="7ecc4-399">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-399">10001</span></span></td>
<td><span data-ttu-id="7ecc4-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7ecc4-401">30,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-402">Proj 2</span></span></td>
<td><span data-ttu-id="7ecc4-403">Project 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-403">Project 2</span></span></td>
<td><span data-ttu-id="7ecc4-404">1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-404">1</span></span></td>
<td><span data-ttu-id="7ecc4-405">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-405">10001</span></span></td>
<td><span data-ttu-id="7ecc4-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7ecc4-407">10,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7ecc4-408">Journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-409">Journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-409">Journal</span></span></th>
<th><span data-ttu-id="7ecc4-410">Type journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7ecc4-411">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="7ecc4-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7ecc4-412">Versie</span><span class="sxs-lookup"><span data-stu-id="7ecc4-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-413">00003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-413">00003</span></span></td>
<td><span data-ttu-id="7ecc4-414">Journaal voor berekening van overheadtarieven</span><span class="sxs-lookup"><span data-stu-id="7ecc4-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="7ecc4-415">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-415">Fiscal</span></span></td>
<td><span data-ttu-id="7ecc4-416">2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-416">2017</span></span></td>
<td><span data-ttu-id="7ecc4-417">Periode 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-417">Period 1</span></span></td>
<td><span data-ttu-id="7ecc4-418">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="7ecc4-419">Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-420">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-421">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-421">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-422">Magnitude</span><span class="sxs-lookup"><span data-stu-id="7ecc4-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-423">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-424">Proj 1</span></span></td>
<td><span data-ttu-id="7ecc4-425">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7ecc4-426">3,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-427">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-428">Proj 2</span></span></td>
<td><span data-ttu-id="7ecc4-429">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7ecc4-430">1,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7ecc4-431">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="7ecc4-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-432">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-433">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-433">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-434">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-434">Cost behavior</span></span></th>
<th><span data-ttu-id="7ecc4-435">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-435">Amount</span></span></th>
<th><span data-ttu-id="7ecc4-436">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-437">CC0001</span></span></td>
<td><span data-ttu-id="7ecc4-438">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-438">HR</span></span></td>
<td><span data-ttu-id="7ecc4-439">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-439">10001</span></span></td>
<td><span data-ttu-id="7ecc4-440">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-440">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-441">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-441">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-442">-30.00</span></span></td>
<td><span data-ttu-id="7ecc4-443">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-444">Proj 1</span></span></td>
<td><span data-ttu-id="7ecc4-445">intern proj 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7ecc4-446">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-446">10001</span></span></td>
<td><span data-ttu-id="7ecc4-447">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-447">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-448">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-448">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-449">30,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-449">30.00</span></span></td>
<td><span data-ttu-id="7ecc4-450">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-451">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-451">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-452">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-452">HR</span></span></td>
<td><span data-ttu-id="7ecc4-453">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-453">10001</span></span></td>
<td><span data-ttu-id="7ecc4-454">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-454">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-455">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-455">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-456">-10.00</span></span></td>
<td><span data-ttu-id="7ecc4-457">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-458">Proj 2</span></span></td>
<td><span data-ttu-id="7ecc4-459">intern proj 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7ecc4-460">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-460">10001</span></span></td>
<td><span data-ttu-id="7ecc4-461">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-461">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-462">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-462">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-463">10.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-463">10.00</span></span></td>
<td><span data-ttu-id="7ecc4-464">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-465">Zie [Overheadberekening uitvoeren](cost-rollup.md#perform-overhead-calculation) voor meer informatie over berekeningsparameters.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="7ecc4-466">Stap 4: De berekening van kostentoewijzing verwerken</span><span class="sxs-lookup"><span data-stu-id="7ecc4-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="7ecc4-467">Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="7ecc4-468">Finance ondersteunt de wederzijdse toewijzingsmethode.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="7ecc4-469">Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="7ecc4-470">Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="7ecc4-471">Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="7ecc4-472">Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="7ecc4-473">De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="7ecc4-474">[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="7ecc4-475">De kostentoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-475">Define the cost allocation</span></span>

<span data-ttu-id="7ecc4-476">Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="7ecc4-477">Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="7ecc4-478">Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-479">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-479">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-480">HR-services</span><span class="sxs-lookup"><span data-stu-id="7ecc4-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-481">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-481">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-482">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-482">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-483">35</span><span class="sxs-lookup"><span data-stu-id="7ecc4-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-484">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-484">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-485">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-485">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-486">55</span><span class="sxs-lookup"><span data-stu-id="7ecc4-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-487">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-487">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-488">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-488">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-489">10</span><span class="sxs-lookup"><span data-stu-id="7ecc4-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-490">Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="7ecc4-491">Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-492">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-492">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-493">Financiële services</span><span class="sxs-lookup"><span data-stu-id="7ecc4-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-494">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-494">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-495">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-495">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-496">65</span><span class="sxs-lookup"><span data-stu-id="7ecc4-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-497">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-497">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-498">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-498">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-499">35</span><span class="sxs-lookup"><span data-stu-id="7ecc4-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-500">Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="7ecc4-501">Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-502">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-502">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-503">Assemblageservices (uren)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-504">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-505">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-505">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-506">60</span><span class="sxs-lookup"><span data-stu-id="7ecc4-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-507">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-508">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-508">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-509">20</span><span class="sxs-lookup"><span data-stu-id="7ecc4-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-510">Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="7ecc4-511">Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-512">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-512">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-513">Verpakkingsservices (uren)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-514">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-515">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-515">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-516">80</span><span class="sxs-lookup"><span data-stu-id="7ecc4-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-517">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-518">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-518">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-519">15</span><span class="sxs-lookup"><span data-stu-id="7ecc4-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7ecc4-520">Statistische metingen, zoals de productie-uren die een product verbruikt, kunnen worden afgeleid uit brongegevens.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="7ecc4-521">Zie [Sjabloon van provider van statistische maateenheden](statistical-measure-provider-template.md#statistical-measure-provider-template) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="7ecc4-522">In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="7ecc4-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-523">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-523">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-524">Magnitude</span><span class="sxs-lookup"><span data-stu-id="7ecc4-524">Magnitude</span></span></th>
<th><span data-ttu-id="7ecc4-525">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="7ecc4-525">Allocation factor</span></span></th>
<th><span data-ttu-id="7ecc4-526">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-526">Amount</span></span></th>
<th><span data-ttu-id="7ecc4-527">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-528">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-528">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-529">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-529">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-530">35</span><span class="sxs-lookup"><span data-stu-id="7ecc4-530">35</span></span></td>
<td><span data-ttu-id="7ecc4-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7ecc4-532">175.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-532">175.00</span></span></td>
<td><span data-ttu-id="7ecc4-533">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-534">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-534">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-535">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-535">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-536">55</span><span class="sxs-lookup"><span data-stu-id="7ecc4-536">55</span></span></td>
<td><span data-ttu-id="7ecc4-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7ecc4-538">275.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-538">275.00</span></span></td>
<td><span data-ttu-id="7ecc4-539">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-540">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-540">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-541">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-541">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-542">10</span><span class="sxs-lookup"><span data-stu-id="7ecc4-542">10</span></span></td>
<td><span data-ttu-id="7ecc4-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7ecc4-544">50,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-544">50.00</span></span></td>
<td><span data-ttu-id="7ecc4-545">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-546">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-546">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-547">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-547">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-548">35</span><span class="sxs-lookup"><span data-stu-id="7ecc4-548">35</span></span></td>
<td><span data-ttu-id="7ecc4-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7ecc4-550">436.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-550">436.00</span></span></td>
<td><span data-ttu-id="7ecc4-551">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-552">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-552">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-553">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-553">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-554">55</span><span class="sxs-lookup"><span data-stu-id="7ecc4-554">55</span></span></td>
<td><span data-ttu-id="7ecc4-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7ecc4-556">685.14</span><span class="sxs-lookup"><span data-stu-id="7ecc4-556">685.14</span></span></td>
<td><span data-ttu-id="7ecc4-557">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-558">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-558">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-559">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-559">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-560">10</span><span class="sxs-lookup"><span data-stu-id="7ecc4-560">10</span></span></td>
<td><span data-ttu-id="7ecc4-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7ecc4-562">124.57</span><span class="sxs-lookup"><span data-stu-id="7ecc4-562">124.57</span></span></td>
<td><span data-ttu-id="7ecc4-563">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-564">In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="7ecc4-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-565">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-565">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-566">Magnitude</span><span class="sxs-lookup"><span data-stu-id="7ecc4-566">Magnitude</span></span></th>
<th><span data-ttu-id="7ecc4-567">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="7ecc4-567">Allocation factor</span></span></th>
<th><span data-ttu-id="7ecc4-568">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-568">Amount</span></span></th>
<th><span data-ttu-id="7ecc4-569">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-570">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-570">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-571">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-571">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-572">65</span><span class="sxs-lookup"><span data-stu-id="7ecc4-572">65</span></span></td>
<td><span data-ttu-id="7ecc4-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7ecc4-574">438.75</span><span class="sxs-lookup"><span data-stu-id="7ecc4-574">438.75</span></span></td>
<td><span data-ttu-id="7ecc4-575">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-576">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-576">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-577">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-577">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-578">35</span><span class="sxs-lookup"><span data-stu-id="7ecc4-578">35</span></span></td>
<td><span data-ttu-id="7ecc4-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7ecc4-580">236.25</span><span class="sxs-lookup"><span data-stu-id="7ecc4-580">236.25</span></span></td>
<td><span data-ttu-id="7ecc4-581">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-582">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-582">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-583">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-583">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-584">65</span><span class="sxs-lookup"><span data-stu-id="7ecc4-584">65</span></span></td>
<td><span data-ttu-id="7ecc4-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7ecc4-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7ecc4-586">5,297.69</span></span></td>
<td><span data-ttu-id="7ecc4-587">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-588">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-588">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-589">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-589">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-590">35</span><span class="sxs-lookup"><span data-stu-id="7ecc4-590">35</span></span></td>
<td><span data-ttu-id="7ecc4-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7ecc4-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7ecc4-592">2,852.60</span></span></td>
<td><span data-ttu-id="7ecc4-593">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-594">In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="7ecc4-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-595">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-595">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-596">Magnitude</span><span class="sxs-lookup"><span data-stu-id="7ecc4-596">Magnitude</span></span></th>
<th><span data-ttu-id="7ecc4-597">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="7ecc4-597">Allocation factor</span></span></th>
<th><span data-ttu-id="7ecc4-598">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-598">Amount</span></span></th>
<th><span data-ttu-id="7ecc4-599">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-600">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-601">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-601">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-602">60</span><span class="sxs-lookup"><span data-stu-id="7ecc4-602">60</span></span></td>
<td><span data-ttu-id="7ecc4-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7ecc4-604">535.31</span><span class="sxs-lookup"><span data-stu-id="7ecc4-604">535.31</span></span></td>
<td><span data-ttu-id="7ecc4-605">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-606">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-607">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-607">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-608">20</span><span class="sxs-lookup"><span data-stu-id="7ecc4-608">20</span></span></td>
<td><span data-ttu-id="7ecc4-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7ecc4-610">178.44</span><span class="sxs-lookup"><span data-stu-id="7ecc4-610">178.44</span></span></td>
<td><span data-ttu-id="7ecc4-611">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-612">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-613">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-613">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-614">60</span><span class="sxs-lookup"><span data-stu-id="7ecc4-614">60</span></span></td>
<td><span data-ttu-id="7ecc4-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7ecc4-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7ecc4-616">4,487.12</span></span></td>
<td><span data-ttu-id="7ecc4-617">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-618">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-619">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-619">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-620">20</span><span class="sxs-lookup"><span data-stu-id="7ecc4-620">20</span></span></td>
<td><span data-ttu-id="7ecc4-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7ecc4-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-622">1,495.71</span></span></td>
<td><span data-ttu-id="7ecc4-623">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ecc4-624">In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).</span><span class="sxs-lookup"><span data-stu-id="7ecc4-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-625">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-625">Cost object</span></span></th>
<th><span data-ttu-id="7ecc4-626">Magnitude</span><span class="sxs-lookup"><span data-stu-id="7ecc4-626">Magnitude</span></span></th>
<th><span data-ttu-id="7ecc4-627">Toewijzingsfactor</span><span class="sxs-lookup"><span data-stu-id="7ecc4-627">Allocation factor</span></span></th>
<th><span data-ttu-id="7ecc4-628">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-628">Amount</span></span></th>
<th><span data-ttu-id="7ecc4-629">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-630">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-631">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-631">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-632">80</span><span class="sxs-lookup"><span data-stu-id="7ecc4-632">80</span></span></td>
<td><span data-ttu-id="7ecc4-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7ecc4-634">241.05</span><span class="sxs-lookup"><span data-stu-id="7ecc4-634">241.05</span></span></td>
<td><span data-ttu-id="7ecc4-635">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-636">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-637">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-637">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-638">15</span><span class="sxs-lookup"><span data-stu-id="7ecc4-638">15</span></span></td>
<td><span data-ttu-id="7ecc4-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7ecc4-640">45.20</span><span class="sxs-lookup"><span data-stu-id="7ecc4-640">45.20</span></span></td>
<td><span data-ttu-id="7ecc4-641">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-642">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-643">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-643">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-644">80</span><span class="sxs-lookup"><span data-stu-id="7ecc4-644">80</span></span></td>
<td><span data-ttu-id="7ecc4-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7ecc4-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7ecc4-646">2,507.09</span></span></td>
<td><span data-ttu-id="7ecc4-647">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-648">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-649">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-649">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-650">15</span><span class="sxs-lookup"><span data-stu-id="7ecc4-650">15</span></span></td>
<td><span data-ttu-id="7ecc4-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7ecc4-652">470.08</span><span class="sxs-lookup"><span data-stu-id="7ecc4-652">470.08</span></span></td>
<td><span data-ttu-id="7ecc4-653">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7ecc4-654">Journaalboekingen (journaalboekingen voor kostenobjectsaldo)</span><span class="sxs-lookup"><span data-stu-id="7ecc4-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-655">Journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-655">Journal</span></span></th>
<th><span data-ttu-id="7ecc4-656">Type journaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7ecc4-657">Fiscale kalenderperiode</span><span class="sxs-lookup"><span data-stu-id="7ecc4-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7ecc4-658">Versie</span><span class="sxs-lookup"><span data-stu-id="7ecc4-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-659">00004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-659">00004</span></span></td>
<td><span data-ttu-id="7ecc4-660">Kostentoewijzingsjournaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="7ecc4-661">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-661">Fiscal</span></span></td>
<td><span data-ttu-id="7ecc4-662">2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-662">2017</span></span></td>
<td><span data-ttu-id="7ecc4-663">Periode 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-663">Period 1</span></span></td>
<td><span data-ttu-id="7ecc4-664">Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="7ecc4-665">Journaalregels</span><span class="sxs-lookup"><span data-stu-id="7ecc4-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7ecc4-666">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-667">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-668">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-668">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-669">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-669">Cost behavior</span></span></th>
<th><span data-ttu-id="7ecc4-670">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-671">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-672">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-672">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-673">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-673">HR</span></span></td>
<td><span data-ttu-id="7ecc4-674">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-674">10001</span></span></td>
<td><span data-ttu-id="7ecc4-675">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-675">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-676">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-676">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-677">500,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-678">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-679">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-679">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-680">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-680">HR</span></span></td>
<td><span data-ttu-id="7ecc4-681">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-681">10001</span></span></td>
<td><span data-ttu-id="7ecc4-682">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-682">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-683">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-683">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-685">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-686">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-686">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-687">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-687">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-688">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-688">10001</span></span></td>
<td><span data-ttu-id="7ecc4-689">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-689">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-690">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-690">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-691">675.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-692">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-693">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-693">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-694">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-694">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-695">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-695">10001</span></span></td>
<td><span data-ttu-id="7ecc4-696">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-696">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-697">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-697">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="7ecc4-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-699">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-700">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-700">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-701">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-701">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-702">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-702">10001</span></span></td>
<td><span data-ttu-id="7ecc4-703">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-703">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-704">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-704">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-705">713.75</span><span class="sxs-lookup"><span data-stu-id="7ecc4-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-706">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-707">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-707">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-708">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-708">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-709">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-709">10001</span></span></td>
<td><span data-ttu-id="7ecc4-710">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-710">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-711">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-711">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="7ecc4-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-713">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-714">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-714">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-715">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-715">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-716">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-716">10001</span></span></td>
<td><span data-ttu-id="7ecc4-717">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-717">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-718">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-718">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-719">286.25</span><span class="sxs-lookup"><span data-stu-id="7ecc4-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-720">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-721">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-721">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-722">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-722">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-723">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-723">10001</span></span></td>
<td><span data-ttu-id="7ecc4-724">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-724">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-725">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-725">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="7ecc4-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-727">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-728">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-729">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-729">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-730">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-730">10001</span></span></td>
<td><span data-ttu-id="7ecc4-731">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-731">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-732">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-732">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-733">776.36</span><span class="sxs-lookup"><span data-stu-id="7ecc4-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-734">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-735">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-736">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-736">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-737">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-737">10001</span></span></td>
<td><span data-ttu-id="7ecc4-738">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-738">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-739">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-739">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7ecc4-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-741">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-742">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-743">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-743">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-744">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-744">10001</span></span></td>
<td><span data-ttu-id="7ecc4-745">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-745">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-746">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-746">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-747">223.64</span><span class="sxs-lookup"><span data-stu-id="7ecc4-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-748">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="7ecc4-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-749">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-750">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-750">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-751">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-751">10001</span></span></td>
<td><span data-ttu-id="7ecc4-752">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-752">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-753">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-753">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7ecc4-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7ecc4-755">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="7ecc4-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7ecc4-756">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7ecc4-757">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-757">Cost element</span></span></th>
<th><span data-ttu-id="7ecc4-758">Kostengedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-758">Cost behavior</span></span></th>
<th><span data-ttu-id="7ecc4-759">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7ecc4-759">Amount</span></span></th>
<th><span data-ttu-id="7ecc4-760">Grootboekdatum</span><span class="sxs-lookup"><span data-stu-id="7ecc4-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7ecc4-761">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-761">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-762">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-762">HR</span></span></td>
<td><span data-ttu-id="7ecc4-763">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-763">10001</span></span></td>
<td><span data-ttu-id="7ecc4-764">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-764">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-765">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-765">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-766">-500.00</span></span></td>
<td><span data-ttu-id="7ecc4-767">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-768">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-768">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-769">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-769">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-770">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-770">10001</span></span></td>
<td><span data-ttu-id="7ecc4-771">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-771">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-772">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-772">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-773">175.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-773">175.00</span></span></td>
<td><span data-ttu-id="7ecc4-774">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-775">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-775">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-776">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-776">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-777">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-777">10001</span></span></td>
<td><span data-ttu-id="7ecc4-778">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-778">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-779">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-779">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-780">275.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-780">275.00</span></span></td>
<td><span data-ttu-id="7ecc4-781">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-782">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-782">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-783">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-783">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-784">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-784">10001</span></span></td>
<td><span data-ttu-id="7ecc4-785">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-785">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-786">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-786">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-787">50,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-787">50,00</span></span></td>
<td><span data-ttu-id="7ecc4-788">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-789">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-789">CC001</span></span></td>
<td><span data-ttu-id="7ecc4-790">HR</span><span class="sxs-lookup"><span data-stu-id="7ecc4-790">HR</span></span></td>
<td><span data-ttu-id="7ecc4-791">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-791">10001</span></span></td>
<td><span data-ttu-id="7ecc4-792">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-792">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-793">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-793">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-794">-1,245.71</span></span></td>
<td><span data-ttu-id="7ecc4-795">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-796">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-796">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-797">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-797">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-798">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-798">10001</span></span></td>
<td><span data-ttu-id="7ecc4-799">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-799">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-800">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-800">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-801">436.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-801">436.00</span></span></td>
<td><span data-ttu-id="7ecc4-802">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-803">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-803">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-804">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-804">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-805">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-805">10001</span></span></td>
<td><span data-ttu-id="7ecc4-806">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-806">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-807">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-807">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-808">685.14</span><span class="sxs-lookup"><span data-stu-id="7ecc4-808">685.14</span></span></td>
<td><span data-ttu-id="7ecc4-809">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-810">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-810">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-811">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-811">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-812">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-812">10001</span></span></td>
<td><span data-ttu-id="7ecc4-813">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-813">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-814">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-814">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-815">124.57</span><span class="sxs-lookup"><span data-stu-id="7ecc4-815">124.57</span></span></td>
<td><span data-ttu-id="7ecc4-816">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-817">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-817">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-818">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-818">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-819">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-819">10001</span></span></td>
<td><span data-ttu-id="7ecc4-820">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-820">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-821">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-821">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-822">-675.00</span></span></td>
<td><span data-ttu-id="7ecc4-823">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-824">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-824">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-825">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-825">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-826">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-826">10001</span></span></td>
<td><span data-ttu-id="7ecc4-827">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-827">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-828">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-828">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-829">438.75</span><span class="sxs-lookup"><span data-stu-id="7ecc4-829">438.75</span></span></td>
<td><span data-ttu-id="7ecc4-830">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-831">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-831">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-832">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-832">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-833">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-833">10001</span></span></td>
<td><span data-ttu-id="7ecc4-834">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-834">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-835">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-835">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-836">236.25</span><span class="sxs-lookup"><span data-stu-id="7ecc4-836">236.25</span></span></td>
<td><span data-ttu-id="7ecc4-837">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-838">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-838">CC002</span></span></td>
<td><span data-ttu-id="7ecc4-839">Financiën</span><span class="sxs-lookup"><span data-stu-id="7ecc4-839">Finance</span></span></td>
<td><span data-ttu-id="7ecc4-840">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-840">10001</span></span></td>
<td><span data-ttu-id="7ecc4-841">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-841">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-842">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-842">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="7ecc4-843">-8,150.29</span></span></td>
<td><span data-ttu-id="7ecc4-844">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-845">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-845">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-846">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-846">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-847">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-847">10001</span></span></td>
<td><span data-ttu-id="7ecc4-848">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-848">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-849">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-849">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7ecc4-850">5,297.69</span></span></td>
<td><span data-ttu-id="7ecc4-851">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-852">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-852">CC004</span></span></td>
<td><span data-ttu-id="7ecc4-853">Verpakking</span><span class="sxs-lookup"><span data-stu-id="7ecc4-853">Packaging</span></span></td>
<td><span data-ttu-id="7ecc4-854">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-854">10001</span></span></td>
<td><span data-ttu-id="7ecc4-855">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-855">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-856">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-856">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7ecc4-857">2,852.60</span></span></td>
<td><span data-ttu-id="7ecc4-858">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-859">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-859">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-860">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-860">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-861">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-861">10001</span></span></td>
<td><span data-ttu-id="7ecc4-862">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-862">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-863">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-863">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="7ecc4-864">-713.75</span></span></td>
<td><span data-ttu-id="7ecc4-865">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-866">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-867">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-867">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-868">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-868">10001</span></span></td>
<td><span data-ttu-id="7ecc4-869">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-869">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-870">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-870">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-871">535.31</span><span class="sxs-lookup"><span data-stu-id="7ecc4-871">535.31</span></span></td>
<td><span data-ttu-id="7ecc4-872">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-873">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-874">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-874">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-875">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-875">10001</span></span></td>
<td><span data-ttu-id="7ecc4-876">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-876">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-877">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-877">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-878">178.44</span><span class="sxs-lookup"><span data-stu-id="7ecc4-878">178.44</span></span></td>
<td><span data-ttu-id="7ecc4-879">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-880">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-880">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-881">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-881">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-882">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-882">10001</span></span></td>
<td><span data-ttu-id="7ecc4-883">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-883">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-884">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-884">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="7ecc4-885">-5,982.83</span></span></td>
<td><span data-ttu-id="7ecc4-886">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-887">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-888">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-888">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-889">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-889">10001</span></span></td>
<td><span data-ttu-id="7ecc4-890">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-890">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-891">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-891">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7ecc4-892">4,487.12</span></span></td>
<td><span data-ttu-id="7ecc4-893">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-894">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-895">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-895">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-896">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-896">10001</span></span></td>
<td><span data-ttu-id="7ecc4-897">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-897">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-898">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-898">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7ecc4-899">1,495.71</span></span></td>
<td><span data-ttu-id="7ecc4-900">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-901">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-901">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-902">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-902">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-903">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-903">10001</span></span></td>
<td><span data-ttu-id="7ecc4-904">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-904">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-905">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-905">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="7ecc4-906">-286.25</span></span></td>
<td><span data-ttu-id="7ecc4-907">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-908">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-909">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-909">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-910">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-910">10001</span></span></td>
<td><span data-ttu-id="7ecc4-911">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-911">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-912">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-912">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-913">241.05</span><span class="sxs-lookup"><span data-stu-id="7ecc4-913">241.05</span></span></td>
<td><span data-ttu-id="7ecc4-914">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-915">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-916">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-916">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-917">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-917">10001</span></span></td>
<td><span data-ttu-id="7ecc4-918">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-918">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-919">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-919">Fixed cost</span></span></td>
<td><span data-ttu-id="7ecc4-920">45.20</span><span class="sxs-lookup"><span data-stu-id="7ecc4-920">45.20</span></span></td>
<td><span data-ttu-id="7ecc4-921">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-922">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-922">CC003</span></span></td>
<td><span data-ttu-id="7ecc4-923">Assembleren</span><span class="sxs-lookup"><span data-stu-id="7ecc4-923">Assembly</span></span></td>
<td><span data-ttu-id="7ecc4-924">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-924">10001</span></span></td>
<td><span data-ttu-id="7ecc4-925">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-925">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-926">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-926">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="7ecc4-927">-2,977.17</span></span></td>
<td><span data-ttu-id="7ecc4-928">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-929">Prod 1</span></span></td>
<td><span data-ttu-id="7ecc4-930">Product 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-930">Product 1</span></span></td>
<td><span data-ttu-id="7ecc4-931">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-931">10001</span></span></td>
<td><span data-ttu-id="7ecc4-932">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-932">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-933">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-933">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7ecc4-934">2,507.09</span></span></td>
<td><span data-ttu-id="7ecc4-935">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ecc4-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-936">Prod 2</span></span></td>
<td><span data-ttu-id="7ecc4-937">Product 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-937">Product 2</span></span></td>
<td><span data-ttu-id="7ecc4-938">10001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-938">10001</span></span></td>
<td><span data-ttu-id="7ecc4-939">Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-939">Electricity</span></span></td>
<td><span data-ttu-id="7ecc4-940">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-940">Variable cost</span></span></td>
<td><span data-ttu-id="7ecc4-941">470.08</span><span class="sxs-lookup"><span data-stu-id="7ecc4-941">470.08</span></span></td>
<td><span data-ttu-id="7ecc4-942">31 januari 2017</span><span class="sxs-lookup"><span data-stu-id="7ecc4-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="7ecc4-943">Conclusie</span><span class="sxs-lookup"><span data-stu-id="7ecc4-943">Conclusion</span></span>
<span data-ttu-id="7ecc4-944">In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="7ecc4-945">Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="7ecc4-946">In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="7ecc4-947">Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="7ecc4-948">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="7ecc4-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="7ecc4-949">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ecc4-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="7ecc4-950">Totaal</span><span class="sxs-lookup"><span data-stu-id="7ecc4-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7ecc4-951">CC099</span><span class="sxs-lookup"><span data-stu-id="7ecc4-951">CC099</span></span></th>
<th><span data-ttu-id="7ecc4-952">CC001</span><span class="sxs-lookup"><span data-stu-id="7ecc4-952">CC001</span></span></th>
<th><span data-ttu-id="7ecc4-953">CC002</span><span class="sxs-lookup"><span data-stu-id="7ecc4-953">CC002</span></span></th>
<th><span data-ttu-id="7ecc4-954">CC003</span><span class="sxs-lookup"><span data-stu-id="7ecc4-954">CC003</span></span></th>
<th><span data-ttu-id="7ecc4-955">CC004</span><span class="sxs-lookup"><span data-stu-id="7ecc4-955">CC004</span></span></th>
<th><span data-ttu-id="7ecc4-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-956">Proj 1</span></span></th>
<th><span data-ttu-id="7ecc4-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-957">Proj 2</span></span></th>
<th><span data-ttu-id="7ecc4-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7ecc4-958">Prod 1</span></span></th>
<th><span data-ttu-id="7ecc4-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7ecc4-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="7ecc4-960">10001 Elektriciteit</span><span class="sxs-lookup"><span data-stu-id="7ecc4-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="7ecc4-970">Ongeclassificeerd</span><span class="sxs-lookup"><span data-stu-id="7ecc4-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-971">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="7ecc4-972">Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-973">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-974">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-975">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-976">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-977">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-978">776.36</span><span class="sxs-lookup"><span data-stu-id="7ecc4-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-979">223.64</span><span class="sxs-lookup"><span data-stu-id="7ecc4-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="7ecc4-981">Variabele kosten</span><span class="sxs-lookup"><span data-stu-id="7ecc4-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-982">000</span><span class="sxs-lookup"><span data-stu-id="7ecc4-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-983">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-984">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-985">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-986">0,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-987">30,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-988">10,00</span><span class="sxs-lookup"><span data-stu-id="7ecc4-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7ecc4-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7ecc4-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7ecc4-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7ecc4-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7ecc4-992">Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="7ecc4-993">Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="7ecc4-994">Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="7ecc4-995">Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="7ecc4-996">Zie [Kostentotalisatie](cost-rollup.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7ecc4-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



