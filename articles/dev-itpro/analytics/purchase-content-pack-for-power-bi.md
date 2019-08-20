---
title: Power BI-inhoud - inkoop- en uitgavenanalyse
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Analyse inkoopuitgaven. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850014"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="41ec5-104">Power BI-inhoud - inkoop- en uitgavenanalyse</span><span class="sxs-lookup"><span data-stu-id="41ec5-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41ec5-105">In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud **Analyse inkoopuitgaven**.</span><span class="sxs-lookup"><span data-stu-id="41ec5-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="41ec5-106">U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.</span><span class="sxs-lookup"><span data-stu-id="41ec5-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="41ec5-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="41ec5-107">Overview</span></span>

<span data-ttu-id="41ec5-108">De Power BI-inhoud **Inkoopuitgavenanalyse** is ontworpen om inkoopmanagers en managers met budgetverantwoordelijkheid te helpen de inkoopuitgaven bij te houden.</span><span class="sxs-lookup"><span data-stu-id="41ec5-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="41ec5-109">Managers kunnen inkoopuitgaven op de volgende manieren analyseren:</span><span class="sxs-lookup"><span data-stu-id="41ec5-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="41ec5-110">Inkoop jaar tot heden (op leveranciersgroep en afzonderlijke leveranciers, aanschaffingscategorie en afzonderlijke producten en locatie van de leverancier)</span><span class="sxs-lookup"><span data-stu-id="41ec5-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="41ec5-111">Wijzigingen jaar tot jaar in inkoop (op leveranciersgroep en aanschaffingscategorie)</span><span class="sxs-lookup"><span data-stu-id="41ec5-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="41ec5-112">Op basis van gegevens voor inkooptransacties biedt de inhoud zowel een samengevoegde weergave van de inkoopcijfers uit het hele bedrijf als ook een analyse van de inkoopuitgaven op leverancier en product.</span><span class="sxs-lookup"><span data-stu-id="41ec5-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="41ec5-113">Rapporten maken wijzigingen in de inkoopuitgaven in het verloop van de tijd duidelijk.</span><span class="sxs-lookup"><span data-stu-id="41ec5-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="41ec5-114">Daarom kunnen de rapporten worden gebruikt om managers te wijzen op positieve en negatieve trends in de uitgaven voor afzonderlijke leveranciers en producten.</span><span class="sxs-lookup"><span data-stu-id="41ec5-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="41ec5-115">Daarnaast geven grafieken de inkoopuitgaven weer voor verschillende inkoopcategorieën en leveranciersgroepen.</span><span class="sxs-lookup"><span data-stu-id="41ec5-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="41ec5-116">Categorie- en regiomanagers kunnen met deze grafieken veranderingen in het uitgavegedrag opsporen.</span><span class="sxs-lookup"><span data-stu-id="41ec5-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="41ec5-117">Toegang tot de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="41ec5-117">Accessing the Power BI content</span></span>
<span data-ttu-id="41ec5-118">De Power BI-inhoud **Analyse inkoopuitgaven** wordt weergegeven op de pagina **Inkoop- en uitgavenanalyse** (**Inkoopbeheer** \> **Query's en rapporten** \> **Inkoopprestatieanalyse** \> **Inkoop- en uitgavenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="41ec5-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="41ec5-119">Metrische gegevens die zijn opgenomen in de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="41ec5-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="41ec5-120">Het Power BI-inhoudpakket **Analyse inkoopuitgaven** bevat een rapport dat uit een verzameling van metrische gegevens bestaat.</span><span class="sxs-lookup"><span data-stu-id="41ec5-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="41ec5-121">Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen.</span><span class="sxs-lookup"><span data-stu-id="41ec5-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="41ec5-122">De volgende secties bieden een overzicht van de visualisaties.</span><span class="sxs-lookup"><span data-stu-id="41ec5-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="41ec5-123">Pagina Inkoop op leverancier (rapport)</span><span class="sxs-lookup"><span data-stu-id="41ec5-123">Purchase by vendor report page</span></span>
<span data-ttu-id="41ec5-124">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="41ec5-124">**Charts**</span></span>
- <span data-ttu-id="41ec5-125">Top 10-leveranciers op inkoop (gestapeld staafdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="41ec5-126">Totale inkoop op groep / land / naam leverancier (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="41ec5-127">Inkoop op groep / land / naam leverancier (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="41ec5-128">Gemiddelde inkoop op groep / land / naam leverancier (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="41ec5-129">**Tegels**</span><span class="sxs-lookup"><span data-stu-id="41ec5-129">**Tiles**</span></span>
- <span data-ttu-id="41ec5-130">Totaalinkoop</span><span class="sxs-lookup"><span data-stu-id="41ec5-130">Total purchase</span></span>
- <span data-ttu-id="41ec5-131">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="41ec5-131">YOY purchase growth</span></span>
- <span data-ttu-id="41ec5-132">Totaal aantal leveranciers</span><span class="sxs-lookup"><span data-stu-id="41ec5-132">Total # vendors</span></span>
- <span data-ttu-id="41ec5-133">Totaal aantal actieve leveranciers</span><span class="sxs-lookup"><span data-stu-id="41ec5-133">Total # of active vendors</span></span>

<span data-ttu-id="41ec5-134">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="41ec5-134">**Example**</span></span>
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="41ec5-135">Pagina Inkoop op product (rapport)</span><span class="sxs-lookup"><span data-stu-id="41ec5-135">Purchase by product report page</span></span>

<span data-ttu-id="41ec5-136">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="41ec5-136">**Charts**</span></span>
- <span data-ttu-id="41ec5-137">Inkoop per aanschaffingscategorie / productnaam (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="41ec5-138">Totale inkoop per aanschaffingscategorie / productnaam (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="41ec5-139">Top 10-producten op inkoop (gestapeld staafdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="41ec5-140">**Tegels**</span><span class="sxs-lookup"><span data-stu-id="41ec5-140">**Tiles**</span></span>
- <span data-ttu-id="41ec5-141">Totaal aantal producten</span><span class="sxs-lookup"><span data-stu-id="41ec5-141">Total # of products</span></span></li>
- <span data-ttu-id="41ec5-142">Totaal aantal actieve producten percentage van totale aantal producten</span><span class="sxs-lookup"><span data-stu-id="41ec5-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="41ec5-143">Aantal producten dat 80% van inkoop oplevert</span><span class="sxs-lookup"><span data-stu-id="41ec5-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="41ec5-144">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="41ec5-144">**Example**</span></span>


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="41ec5-145">Pagina Inkoop op periode (rapport)</span><span class="sxs-lookup"><span data-stu-id="41ec5-145">Purchase by period report page</span></span>
<span data-ttu-id="41ec5-146">Deze pagina geeft inkopen van dit jaar en vorig jaar en groei per aanschaffingscategorie weer.</span><span class="sxs-lookup"><span data-stu-id="41ec5-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="41ec5-147">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="41ec5-147">**Charts**</span></span> 
- <span data-ttu-id="41ec5-148">Inkoop op maand / dag (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="41ec5-149">Cumulatieve inkoop afwijking jaar-op-jaar (watervalgrafiek)</span><span class="sxs-lookup"><span data-stu-id="41ec5-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="41ec5-150">Totale inkoop groei jaar-op-jaar (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="41ec5-151">Inkoopoverzicht (matrix)</span><span class="sxs-lookup"><span data-stu-id="41ec5-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="41ec5-152">**Tegels**</span><span class="sxs-lookup"><span data-stu-id="41ec5-152">**Tiles**</span></span>
- <span data-ttu-id="41ec5-153">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="41ec5-153">YOY purchase growth</span></span>
- <span data-ttu-id="41ec5-154">Inkoopgroei jaar-op-jaar %</span><span class="sxs-lookup"><span data-stu-id="41ec5-154">YOY purchase growth %</span></span>

<span data-ttu-id="41ec5-155">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="41ec5-155">**Example**</span></span>
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="41ec5-156">Pagina Inkoop op leverancierslocatie (rapport)</span><span class="sxs-lookup"><span data-stu-id="41ec5-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="41ec5-157">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="41ec5-157">**Charts**</span></span>
- <span data-ttu-id="41ec5-158">Inkoop op stad</span><span class="sxs-lookup"><span data-stu-id="41ec5-158">Purchase by city</span></span>
- <span data-ttu-id="41ec5-159">Inkoop groei jaar-op-jaar %</span><span class="sxs-lookup"><span data-stu-id="41ec5-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="41ec5-160">Inkoop op land</span><span class="sxs-lookup"><span data-stu-id="41ec5-160">Purchase by country</span></span>

<span data-ttu-id="41ec5-161">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="41ec5-161">**Example**</span></span>
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="41ec5-162">Pagina Analyse inkoopuitgaven op tijd (rapport)</span><span class="sxs-lookup"><span data-stu-id="41ec5-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="41ec5-163">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="41ec5-163">**Charts**</span></span> 
- <span data-ttu-id="41ec5-164">Inkoop huidige jaar op maand / dag (lijndiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="41ec5-165">Inkooporders huidig en vorig jaar (lijn- en kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="41ec5-166">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="41ec5-166">**Example**</span></span>
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="41ec5-167">Pagina Analyse inkoopuitgaven op leverancier (rapport)</span><span class="sxs-lookup"><span data-stu-id="41ec5-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="41ec5-168">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="41ec5-168">**Charts**</span></span> 
- <span data-ttu-id="41ec5-169">Top 10 leverancier inkoop % van inkoop (trechterdiagram)</span><span class="sxs-lookup"><span data-stu-id="41ec5-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="41ec5-170">Top 10 leveranciers met een gestegen uitgaven jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="41ec5-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="41ec5-171">Top 10 leveranciers met een gedaalde uitgaven jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="41ec5-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="41ec5-172">**voorbeeld** 
</span><span class="sxs-lookup"><span data-stu-id="41ec5-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="41ec5-173">Gegevensmodel en entiteiten</span><span class="sxs-lookup"><span data-stu-id="41ec5-173">Data model and entities</span></span>
<span data-ttu-id="41ec5-174">De volgende gegevens worden gebruikt om de rapportpagina's in de Power BI-inhoud **Analyse inkoopuitgaven** te vullen.</span><span class="sxs-lookup"><span data-stu-id="41ec5-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="41ec5-175">Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag.</span><span class="sxs-lookup"><span data-stu-id="41ec5-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="41ec5-176">De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses.</span><span class="sxs-lookup"><span data-stu-id="41ec5-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="41ec5-177">Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="41ec5-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="41ec5-178">De samengevoegde metingen in dit inhoudpakket zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Inkoop-cube in Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="41ec5-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="41ec5-179">Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken.</span><span class="sxs-lookup"><span data-stu-id="41ec5-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="41ec5-180">Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Overzicht van Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="41ec5-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="41ec5-181">De volgende belangrijke samengevoegde metingen zijn rechtstreeks vanuit de entiteit Factuurregels beschikbaar en worden gebruikt als basis voor de inhoud.</span><span class="sxs-lookup"><span data-stu-id="41ec5-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="41ec5-182">Entiteit</span><span class="sxs-lookup"><span data-stu-id="41ec5-182">Entity</span></span>        | <span data-ttu-id="41ec5-183">Belangrijke samengevoegde metingen</span><span class="sxs-lookup"><span data-stu-id="41ec5-183">Key aggregate measurements</span></span> | <span data-ttu-id="41ec5-184">Gegevensbron</span><span class="sxs-lookup"><span data-stu-id="41ec5-184">Data source</span></span>                                 | <span data-ttu-id="41ec5-185">Veld</span><span class="sxs-lookup"><span data-stu-id="41ec5-185">Field</span></span>              | <span data-ttu-id="41ec5-186">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="41ec5-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="41ec5-187">Factuurregels</span><span class="sxs-lookup"><span data-stu-id="41ec5-187">Invoice lines</span></span> | <span data-ttu-id="41ec5-188">Inkoop</span><span class="sxs-lookup"><span data-stu-id="41ec5-188">Purchase</span></span>                   | <span data-ttu-id="41ec5-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="41ec5-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="41ec5-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="41ec5-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="41ec5-191">Het bedrag in de valuta voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="41ec5-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="41ec5-192">De volgende tabel toont de belangrijkste metingen in de inhoud die worden berekend op basis van de entiteit Factuurregels.</span><span class="sxs-lookup"><span data-stu-id="41ec5-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="41ec5-193">Maat</span><span class="sxs-lookup"><span data-stu-id="41ec5-193">Measure</span></span>               | <span data-ttu-id="41ec5-194">Berekening</span><span class="sxs-lookup"><span data-stu-id="41ec5-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41ec5-195">Inkoop huidig jaar</span><span class="sxs-lookup"><span data-stu-id="41ec5-195">Purchase current year</span></span> | <span data-ttu-id="41ec5-196">Inkoop huidig jaar = SUM('Factuurregels\[Inkoop\])</span><span class="sxs-lookup"><span data-stu-id="41ec5-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="41ec5-197">Inkoop vorig jaar</span><span class="sxs-lookup"><span data-stu-id="41ec5-197">Purchase last year</span></span>    | <span data-ttu-id="41ec5-198">Inkoop vorig jaar = CALCULATE(SUM('Factuurregels\[Inkoop\]), SAMEPERIODLASTYEAR(Datums\[Datum\]))</span><span class="sxs-lookup"><span data-stu-id="41ec5-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="41ec5-199">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="41ec5-199">YOY purchase growth</span></span>   | <span data-ttu-id="41ec5-200">Groei inkoop jaar-op-jaar = \[Inkoop huidig jaar\] - \[Inkoop vorig jaar\]</span><span class="sxs-lookup"><span data-stu-id="41ec5-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="41ec5-201">De volgende belangrijke dimensies in de inhoud worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.</span><span class="sxs-lookup"><span data-stu-id="41ec5-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="41ec5-202">Entiteit</span><span class="sxs-lookup"><span data-stu-id="41ec5-202">Entity</span></span>                 | <span data-ttu-id="41ec5-203">Voorbeelden van kenmerken</span><span class="sxs-lookup"><span data-stu-id="41ec5-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="41ec5-204">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="41ec5-204">Vendors</span></span>                | <span data-ttu-id="41ec5-205">Leveranciersgroepen, Land/regio van leverancier, Leveranciersnaam</span><span class="sxs-lookup"><span data-stu-id="41ec5-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="41ec5-206">Producten</span><span class="sxs-lookup"><span data-stu-id="41ec5-206">Products</span></span>               | <span data-ttu-id="41ec5-207">Productnummer, Productnaam, Naam van artikelengroep</span><span class="sxs-lookup"><span data-stu-id="41ec5-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="41ec5-208">Inkoopcategorieën</span><span class="sxs-lookup"><span data-stu-id="41ec5-208">Procurement categories</span></span> | <span data-ttu-id="41ec5-209">Aanschaffingscategorie, namen van Aanschaffingscategorieën</span><span class="sxs-lookup"><span data-stu-id="41ec5-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="41ec5-210">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="41ec5-210">Legal entities</span></span>         | <span data-ttu-id="41ec5-211">Rechtspersoonnaam</span><span class="sxs-lookup"><span data-stu-id="41ec5-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="41ec5-212">Datums</span><span class="sxs-lookup"><span data-stu-id="41ec5-212">Dates</span></span>                  | <span data-ttu-id="41ec5-213">Datums, Jaarverschuiving</span><span class="sxs-lookup"><span data-stu-id="41ec5-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="41ec5-214">Standaard worden gegevens in de inhoud weergegeven voor het huidige kalenderjaar.</span><span class="sxs-lookup"><span data-stu-id="41ec5-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="41ec5-215">U kunt echter het datumfilter in de sectie rapportfilters wijzigen.</span><span class="sxs-lookup"><span data-stu-id="41ec5-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="41ec5-216">U kunt ook het bedrijfsfilter wijzigen.</span><span class="sxs-lookup"><span data-stu-id="41ec5-216">You can also change the company filter.</span></span>
