---
title: Power BI-inhoud - inkoop- en uitgavenanalyse
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Analyse inkoopuitgaven. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "313837"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="d8a16-104">Power BI-inhoud - inkoop- en uitgavenanalyse</span><span class="sxs-lookup"><span data-stu-id="d8a16-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8a16-105">In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud **Analyse inkoopuitgaven**.</span><span class="sxs-lookup"><span data-stu-id="d8a16-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="d8a16-106">U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.</span><span class="sxs-lookup"><span data-stu-id="d8a16-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="d8a16-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="d8a16-107">Overview</span></span>

<span data-ttu-id="d8a16-108">De Power BI-inhoud **Analyse inkoopuitgaven** is ontworpen om inkoopmanagers en managers met budgetverantwoordelijkheid te helpen de inkoopuitgaven in de gaten te houden.</span><span class="sxs-lookup"><span data-stu-id="d8a16-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="d8a16-109">Managers kunnen inkoopuitgaven op de volgende manieren analyseren:</span><span class="sxs-lookup"><span data-stu-id="d8a16-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="d8a16-110">Inkoop jaar tot heden (op leveranciersgroep en afzonderlijke leveranciers, aanschaffingscategorie en afzonderlijke producten en locatie van de leverancier)</span><span class="sxs-lookup"><span data-stu-id="d8a16-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="d8a16-111">Wijzigingen jaar tot jaar in inkoop (op leveranciersgroep en aanschaffingscategorie)</span><span class="sxs-lookup"><span data-stu-id="d8a16-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="d8a16-112">Op basis van gegevens voor inkooptransacties biedt de inhoud zowel een samengevoegde weergave van de inkoopcijfers uit het hele bedrijf als ook een analyse van de inkoopuitgaven op leverancier en product.</span><span class="sxs-lookup"><span data-stu-id="d8a16-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="d8a16-113">Rapporten maken wijzigingen in de inkoopuitgaven in het verloop van de tijd duidelijk.</span><span class="sxs-lookup"><span data-stu-id="d8a16-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="d8a16-114">Daarom kunnen de rapporten worden gebruikt om managers te wijzen op positieve en negatieve trends in de uitgaven voor afzonderlijke leveranciers en producten.</span><span class="sxs-lookup"><span data-stu-id="d8a16-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="d8a16-115">Daarnaast geven grafieken de inkoopuitgaven weer voor verschillende inkoopcategorieën en leveranciersgroepen.</span><span class="sxs-lookup"><span data-stu-id="d8a16-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="d8a16-116">Categorie- en regiomanagers kunnen met deze grafieken veranderingen in het uitgavegedrag opsporen.</span><span class="sxs-lookup"><span data-stu-id="d8a16-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="d8a16-117">Toegang tot de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="d8a16-117">Accessing the Power BI content</span></span>
<span data-ttu-id="d8a16-118">De Power BI-inhoud **Analyse inkoopuitgaven** wordt weergegeven op de pagina **Inkoop- en uitgavenanalyse** (**Inkoopbeheer** \> **Query's en rapporten** \> **Inkoopprestatieanalyse** \> **Inkoop- en uitgavenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="d8a16-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="d8a16-119">Metrische gegevens die zijn opgenomen in de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="d8a16-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="d8a16-120">Het Power BI-inhoudpakket **Analyse inkoopuitgaven** bevat een rapport dat uit een verzameling van metrische gegevens bestaat.</span><span class="sxs-lookup"><span data-stu-id="d8a16-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="d8a16-121">Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen.</span><span class="sxs-lookup"><span data-stu-id="d8a16-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="d8a16-122">In de volgende tabel vindt u een overzicht van de visualisaties.</span><span class="sxs-lookup"><span data-stu-id="d8a16-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d8a16-123">Rapportpagina</span><span class="sxs-lookup"><span data-stu-id="d8a16-123">Report page</span></span></th>
<th><span data-ttu-id="d8a16-124">Diagrammen</span><span class="sxs-lookup"><span data-stu-id="d8a16-124">Charts</span></span></th>
<th><span data-ttu-id="d8a16-125">Tegels</span><span class="sxs-lookup"><span data-stu-id="d8a16-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d8a16-126">Inkoop op leverancier</span><span class="sxs-lookup"><span data-stu-id="d8a16-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="d8a16-127">Top 10-leveranciers op inkoop (gestapeld staafdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="d8a16-128">Totale inkoop op groep / land / naam leverancier (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="d8a16-129">Inkoop op groep / land / naam leverancier (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="d8a16-130">Gemiddelde inkoop op groep / land / naam leverancier (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d8a16-131">Totaalinkoop</span><span class="sxs-lookup"><span data-stu-id="d8a16-131">Total purchase</span></span></li>
<li><span data-ttu-id="d8a16-132">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="d8a16-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="d8a16-133">Totaal aantal leveranciers</span><span class="sxs-lookup"><span data-stu-id="d8a16-133">Total # vendors</span></span></li>
<li><span data-ttu-id="d8a16-134">Totaal aantal actieve leveranciers</span><span class="sxs-lookup"><span data-stu-id="d8a16-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="d8a16-135">Inkoop op product</span><span class="sxs-lookup"><span data-stu-id="d8a16-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="d8a16-136">Inkoop per aanschaffingscategorie / productnaam (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="d8a16-137">Totale inkoop per aanschaffingscategorie / productnaam (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="d8a16-138">Top 10-producten op inkoop (gestapeld staafdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d8a16-139">Totaal aantal producten</span><span class="sxs-lookup"><span data-stu-id="d8a16-139">Total # of products</span></span></li>
<li><span data-ttu-id="d8a16-140">Totaal aantal actieve producten percentage van totale aantal producten</span><span class="sxs-lookup"><span data-stu-id="d8a16-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="d8a16-141">Aantal producten dat 80% van inkoop oplevert</span><span class="sxs-lookup"><span data-stu-id="d8a16-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="d8a16-142">Inkoop op periode\*</span><span class="sxs-lookup"><span data-stu-id="d8a16-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="d8a16-143">Inkoop op maand / dag (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="d8a16-144">Cumulatieve inkoop afwijking jaar-op-jaar (watervalgrafiek)</span><span class="sxs-lookup"><span data-stu-id="d8a16-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="d8a16-145">Totale inkoop groei jaar-op-jaar (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="d8a16-146">Inkoopoverzicht (matrix)</span><span class="sxs-lookup"><span data-stu-id="d8a16-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d8a16-147">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="d8a16-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="d8a16-148">Inkoopgroei jaar-op-jaar %</span><span class="sxs-lookup"><span data-stu-id="d8a16-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="d8a16-149">Inkoop op leverancierlocatie</span><span class="sxs-lookup"><span data-stu-id="d8a16-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="d8a16-150">Inkoop op stad</span><span class="sxs-lookup"><span data-stu-id="d8a16-150">Purchase by city</span></span></li>
<li><span data-ttu-id="d8a16-151">Inkoop groei jaar-op-jaar %</span><span class="sxs-lookup"><span data-stu-id="d8a16-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="d8a16-152">Inkoop op land</span><span class="sxs-lookup"><span data-stu-id="d8a16-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="d8a16-153">Analyse inkoopuitgaven op tijd</span><span class="sxs-lookup"><span data-stu-id="d8a16-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="d8a16-154">Inkoop huidige jaar op maand / dag (lijndiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="d8a16-155">Inkooporders huidig en vorig jaar (lijn- en kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="d8a16-156">Analyse inkoopuitgaven op leverancier</span><span class="sxs-lookup"><span data-stu-id="d8a16-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="d8a16-157">Top 10 leverancier inkoop % van inkoop (trechterdiagram)</span><span class="sxs-lookup"><span data-stu-id="d8a16-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="d8a16-158">Top 10 leveranciers met een gestegen uitgaven jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="d8a16-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="d8a16-159">Top 10 leveranciers met een gedaalde uitgaven jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="d8a16-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d8a16-160">\* Inkoop dit jaar en vorig jaar en groei per aanschaffingscategorie</span><span class="sxs-lookup"><span data-stu-id="d8a16-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="d8a16-161">Gegevensmodel en entiteiten</span><span class="sxs-lookup"><span data-stu-id="d8a16-161">Data model and entities</span></span>
<span data-ttu-id="d8a16-162">De volgende gegevens worden gebruikt om de rapportpagina's in de Power BI-inhoud **Analyse inkoopuitgaven** te vullen.</span><span class="sxs-lookup"><span data-stu-id="d8a16-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="d8a16-163">Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag.</span><span class="sxs-lookup"><span data-stu-id="d8a16-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="d8a16-164">De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses.</span><span class="sxs-lookup"><span data-stu-id="d8a16-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="d8a16-165">Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="d8a16-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="d8a16-166">De samengevoegde metingen in dit inhoudpakket zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Inkoop-cube in Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="d8a16-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="d8a16-167">Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken.</span><span class="sxs-lookup"><span data-stu-id="d8a16-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="d8a16-168">Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Overzicht van Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="d8a16-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="d8a16-169">De volgende belangrijke samengevoegde metingen zijn rechtstreeks vanuit de entiteit Factuurregels beschikbaar en worden gebruikt als basis voor de inhoud.</span><span class="sxs-lookup"><span data-stu-id="d8a16-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="d8a16-170">Entiteit</span><span class="sxs-lookup"><span data-stu-id="d8a16-170">Entity</span></span>        | <span data-ttu-id="d8a16-171">Belangrijke samengevoegde metingen</span><span class="sxs-lookup"><span data-stu-id="d8a16-171">Key aggregate measurements</span></span> | <span data-ttu-id="d8a16-172">Gegevensbron</span><span class="sxs-lookup"><span data-stu-id="d8a16-172">Data source</span></span>                                 | <span data-ttu-id="d8a16-173">Veld</span><span class="sxs-lookup"><span data-stu-id="d8a16-173">Field</span></span>              | <span data-ttu-id="d8a16-174">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d8a16-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="d8a16-175">Factuurregels</span><span class="sxs-lookup"><span data-stu-id="d8a16-175">Invoice lines</span></span> | <span data-ttu-id="d8a16-176">Inkoop</span><span class="sxs-lookup"><span data-stu-id="d8a16-176">Purchase</span></span>                   | <span data-ttu-id="d8a16-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="d8a16-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="d8a16-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="d8a16-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="d8a16-179">Het bedrag in de valuta voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="d8a16-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="d8a16-180">De volgende tabel toont de belangrijkste metingen in de inhoud die worden berekend op basis van de entiteit Factuurregels.</span><span class="sxs-lookup"><span data-stu-id="d8a16-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="d8a16-181">Maat</span><span class="sxs-lookup"><span data-stu-id="d8a16-181">Measure</span></span>               | <span data-ttu-id="d8a16-182">Berekening</span><span class="sxs-lookup"><span data-stu-id="d8a16-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a16-183">Inkoop huidig jaar</span><span class="sxs-lookup"><span data-stu-id="d8a16-183">Purchase current year</span></span> | <span data-ttu-id="d8a16-184">Inkoop huidig jaar = SUM('Factuurregels\[Inkoop\])</span><span class="sxs-lookup"><span data-stu-id="d8a16-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="d8a16-185">Inkoop vorig jaar</span><span class="sxs-lookup"><span data-stu-id="d8a16-185">Purchase last year</span></span>    | <span data-ttu-id="d8a16-186">Inkoop vorig jaar = CALCULATE(SUM('Factuurregels\[Inkoop\]), SAMEPERIODLASTYEAR(Datums\[Datum\]))</span><span class="sxs-lookup"><span data-stu-id="d8a16-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="d8a16-187">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="d8a16-187">YOY purchase growth</span></span>   | <span data-ttu-id="d8a16-188">Groei inkoop jaar-op-jaar = \[Inkoop huidig jaar\] - \[Inkoop vorig jaar\]</span><span class="sxs-lookup"><span data-stu-id="d8a16-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="d8a16-189">De volgende belangrijke dimensies in de inhoud worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.</span><span class="sxs-lookup"><span data-stu-id="d8a16-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="d8a16-190">Entiteit</span><span class="sxs-lookup"><span data-stu-id="d8a16-190">Entity</span></span>                 | <span data-ttu-id="d8a16-191">Voorbeelden van kenmerken</span><span class="sxs-lookup"><span data-stu-id="d8a16-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="d8a16-192">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="d8a16-192">Vendors</span></span>                | <span data-ttu-id="d8a16-193">Leveranciersgroepen, Land/regio van leverancier, Leveranciersnaam</span><span class="sxs-lookup"><span data-stu-id="d8a16-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="d8a16-194">Producten</span><span class="sxs-lookup"><span data-stu-id="d8a16-194">Products</span></span>               | <span data-ttu-id="d8a16-195">Productnummer, Productnaam, Naam van artikelengroep</span><span class="sxs-lookup"><span data-stu-id="d8a16-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="d8a16-196">Inkoopcategorieën</span><span class="sxs-lookup"><span data-stu-id="d8a16-196">Procurement categories</span></span> | <span data-ttu-id="d8a16-197">Aanschaffingscategorie, namen van Aanschaffingscategorieën</span><span class="sxs-lookup"><span data-stu-id="d8a16-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="d8a16-198">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="d8a16-198">Legal entities</span></span>         | <span data-ttu-id="d8a16-199">Rechtspersoonnaam</span><span class="sxs-lookup"><span data-stu-id="d8a16-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="d8a16-200">Datums</span><span class="sxs-lookup"><span data-stu-id="d8a16-200">Dates</span></span>                  | <span data-ttu-id="d8a16-201">Datums, Jaarverschuiving</span><span class="sxs-lookup"><span data-stu-id="d8a16-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="d8a16-202">Standaard worden gegevens in de inhoud weergegeven voor het huidige kalenderjaar.</span><span class="sxs-lookup"><span data-stu-id="d8a16-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="d8a16-203">U kunt echter het datumfilter in de sectie rapportfilters wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d8a16-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="d8a16-204">U kunt ook het bedrijfsfilter wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d8a16-204">You can also change the company filter.</span></span>
