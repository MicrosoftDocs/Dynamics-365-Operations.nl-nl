---
title: Power BI-inhoud - inkoop- en uitgavenanalyse
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Analyse inkoopuitgaven.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9741b5f30f5e62b9e80000953113377fe016253
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749364"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="afa95-103">Power BI-inhoud - inkoop- en uitgavenanalyse</span><span class="sxs-lookup"><span data-stu-id="afa95-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afa95-104">In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Analyse inkoopuitgaven**.</span><span class="sxs-lookup"><span data-stu-id="afa95-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="afa95-105">U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.</span><span class="sxs-lookup"><span data-stu-id="afa95-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="afa95-106">Overzicht</span><span class="sxs-lookup"><span data-stu-id="afa95-106">Overview</span></span>

<span data-ttu-id="afa95-107">De Power BI-inhoud **Inkoopuitgavenanalyse** is ontworpen om inkoopmanagers en managers met budgetverantwoordelijkheid te helpen de inkoopuitgaven bij te houden.</span><span class="sxs-lookup"><span data-stu-id="afa95-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="afa95-108">Managers kunnen inkoopuitgaven op de volgende manieren analyseren:</span><span class="sxs-lookup"><span data-stu-id="afa95-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="afa95-109">Inkoop jaar tot heden (op leveranciersgroep en afzonderlijke leveranciers, aanschaffingscategorie en afzonderlijke producten en locatie van de leverancier)</span><span class="sxs-lookup"><span data-stu-id="afa95-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="afa95-110">Wijzigingen jaar tot jaar in inkoop (op leveranciersgroep en aanschaffingscategorie)</span><span class="sxs-lookup"><span data-stu-id="afa95-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="afa95-111">Op basis van gegevens voor inkooptransacties biedt de inhoud zowel een samengevoegde weergave van de inkoopcijfers uit het hele bedrijf als ook een analyse van de inkoopuitgaven op leverancier en product.</span><span class="sxs-lookup"><span data-stu-id="afa95-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="afa95-112">Rapporten maken wijzigingen in de inkoopuitgaven in het verloop van de tijd duidelijk.</span><span class="sxs-lookup"><span data-stu-id="afa95-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="afa95-113">Daarom kunnen de rapporten worden gebruikt om managers te wijzen op positieve en negatieve trends in de uitgaven voor afzonderlijke leveranciers en producten.</span><span class="sxs-lookup"><span data-stu-id="afa95-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="afa95-114">Daarnaast geven grafieken de inkoopuitgaven weer voor verschillende inkoopcategorieën en leveranciersgroepen.</span><span class="sxs-lookup"><span data-stu-id="afa95-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="afa95-115">Categorie- en regiomanagers kunnen met deze grafieken veranderingen in het uitgavegedrag opsporen.</span><span class="sxs-lookup"><span data-stu-id="afa95-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="afa95-116">Toegang tot de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="afa95-116">Accessing the Power BI content</span></span>
<span data-ttu-id="afa95-117">De Power BI-inhoud **Analyse inkoopuitgaven** wordt weergegeven op de pagina **Inkoop- en uitgavenanalyse** (**Inkoopbeheer** \> **Query's en rapporten** \> **Inkoopprestatieanalyse** \> **Inkoop- en uitgavenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="afa95-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="afa95-118">Metrische gegevens die zijn opgenomen in de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="afa95-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="afa95-119">Het Power BI-inhoudpakket **Analyse inkoopuitgaven** bevat een rapport dat uit een verzameling van metrische gegevens bestaat.</span><span class="sxs-lookup"><span data-stu-id="afa95-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="afa95-120">Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen.</span><span class="sxs-lookup"><span data-stu-id="afa95-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="afa95-121">De volgende secties bieden een overzicht van de visualisaties.</span><span class="sxs-lookup"><span data-stu-id="afa95-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="afa95-122">Pagina Inkoop op leverancier (rapport)</span><span class="sxs-lookup"><span data-stu-id="afa95-122">Purchase by vendor report page</span></span>
<span data-ttu-id="afa95-123">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="afa95-123">**Charts**</span></span>
- <span data-ttu-id="afa95-124">Top 10-leveranciers op inkoop (gestapeld staafdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="afa95-125">Totale inkoop op groep / land / naam leverancier (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="afa95-126">Inkoop op groep / land / naam leverancier (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="afa95-127">Gemiddelde inkoop op groep / land / naam leverancier (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="afa95-128">**Tegels**</span><span class="sxs-lookup"><span data-stu-id="afa95-128">**Tiles**</span></span>
- <span data-ttu-id="afa95-129">Totaalinkoop</span><span class="sxs-lookup"><span data-stu-id="afa95-129">Total purchase</span></span>
- <span data-ttu-id="afa95-130">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="afa95-130">YOY purchase growth</span></span>
- <span data-ttu-id="afa95-131">Totaal aantal leveranciers</span><span class="sxs-lookup"><span data-stu-id="afa95-131">Total # vendors</span></span>
- <span data-ttu-id="afa95-132">Totaal aantal actieve leveranciers</span><span class="sxs-lookup"><span data-stu-id="afa95-132">Total # of active vendors</span></span>

<span data-ttu-id="afa95-133">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="afa95-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="afa95-134">Pagina Inkoop op product (rapport)</span><span class="sxs-lookup"><span data-stu-id="afa95-134">Purchase by product report page</span></span>

<span data-ttu-id="afa95-135">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="afa95-135">**Charts**</span></span>
- <span data-ttu-id="afa95-136">Inkoop per aanschaffingscategorie / productnaam (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="afa95-137">Totale inkoop per aanschaffingscategorie / productnaam (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="afa95-138">Top 10-producten op inkoop (gestapeld staafdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="afa95-139">**Tegels**</span><span class="sxs-lookup"><span data-stu-id="afa95-139">**Tiles**</span></span>
- <span data-ttu-id="afa95-140">Totaal aantal producten</span><span class="sxs-lookup"><span data-stu-id="afa95-140">Total # of products</span></span></li>
- <span data-ttu-id="afa95-141">Totaal aantal actieve producten percentage van totale aantal producten</span><span class="sxs-lookup"><span data-stu-id="afa95-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="afa95-142">Aantal producten dat 80% van inkoop oplevert</span><span class="sxs-lookup"><span data-stu-id="afa95-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="afa95-143">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="afa95-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="afa95-144">Pagina Inkoop op periode (rapport)</span><span class="sxs-lookup"><span data-stu-id="afa95-144">Purchase by period report page</span></span>
<span data-ttu-id="afa95-145">Deze pagina geeft inkopen van dit jaar en vorig jaar en groei per aanschaffingscategorie weer.</span><span class="sxs-lookup"><span data-stu-id="afa95-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="afa95-146">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="afa95-146">**Charts**</span></span> 
- <span data-ttu-id="afa95-147">Inkoop op maand / dag (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="afa95-148">Cumulatieve inkoop afwijking jaar-op-jaar (watervalgrafiek)</span><span class="sxs-lookup"><span data-stu-id="afa95-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="afa95-149">Totale inkoop groei jaar-op-jaar (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="afa95-150">Inkoopoverzicht (matrix)</span><span class="sxs-lookup"><span data-stu-id="afa95-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="afa95-151">**Tegels**</span><span class="sxs-lookup"><span data-stu-id="afa95-151">**Tiles**</span></span>
- <span data-ttu-id="afa95-152">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="afa95-152">YOY purchase growth</span></span>
- <span data-ttu-id="afa95-153">Inkoopgroei jaar-op-jaar %</span><span class="sxs-lookup"><span data-stu-id="afa95-153">YOY purchase growth %</span></span>

<span data-ttu-id="afa95-154">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="afa95-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="afa95-155">Pagina Inkoop op leverancierslocatie (rapport)</span><span class="sxs-lookup"><span data-stu-id="afa95-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="afa95-156">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="afa95-156">**Charts**</span></span>
- <span data-ttu-id="afa95-157">Inkoop op stad</span><span class="sxs-lookup"><span data-stu-id="afa95-157">Purchase by city</span></span>
- <span data-ttu-id="afa95-158">Inkoop groei jaar-op-jaar %</span><span class="sxs-lookup"><span data-stu-id="afa95-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="afa95-159">Inkoop op land</span><span class="sxs-lookup"><span data-stu-id="afa95-159">Purchase by country</span></span>

<span data-ttu-id="afa95-160">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="afa95-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="afa95-161">Pagina Analyse inkoopuitgaven op tijd (rapport)</span><span class="sxs-lookup"><span data-stu-id="afa95-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="afa95-162">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="afa95-162">**Charts**</span></span> 
- <span data-ttu-id="afa95-163">Inkoop huidige jaar op maand / dag (lijndiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="afa95-164">Inkooporders huidig en vorig jaar (lijn- en kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="afa95-165">**Voorbeeld:**</span><span class="sxs-lookup"><span data-stu-id="afa95-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="afa95-166">Pagina Analyse inkoopuitgaven op leverancier (rapport)</span><span class="sxs-lookup"><span data-stu-id="afa95-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="afa95-167">**Diagrammen**</span><span class="sxs-lookup"><span data-stu-id="afa95-167">**Charts**</span></span> 
- <span data-ttu-id="afa95-168">Top 10 leverancier inkoop % van inkoop (trechterdiagram)</span><span class="sxs-lookup"><span data-stu-id="afa95-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="afa95-169">Top 10 leveranciers met een gestegen uitgaven jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="afa95-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="afa95-170">Top 10 leveranciers met een gedaalde uitgaven jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="afa95-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="afa95-171">**voorbeeld** 
</span><span class="sxs-lookup"><span data-stu-id="afa95-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="afa95-172">Gegevensmodel en entiteiten</span><span class="sxs-lookup"><span data-stu-id="afa95-172">Data model and entities</span></span>
<span data-ttu-id="afa95-173">De volgende gegevens worden gebruikt om de rapportpagina's in de Power BI-inhoud **Analyse inkoopuitgaven** te vullen.</span><span class="sxs-lookup"><span data-stu-id="afa95-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="afa95-174">Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag.</span><span class="sxs-lookup"><span data-stu-id="afa95-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="afa95-175">De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses.</span><span class="sxs-lookup"><span data-stu-id="afa95-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="afa95-176">Zie voor meer informatie [Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="afa95-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="afa95-177">De samengevoegde metingen in dit inhoudpakket zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Inkoop-cube in Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="afa95-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="afa95-178">Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken.</span><span class="sxs-lookup"><span data-stu-id="afa95-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="afa95-179">Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in [Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="afa95-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="afa95-180">De volgende belangrijke samengevoegde metingen zijn rechtstreeks vanuit de entiteit Factuurregels beschikbaar en worden gebruikt als basis voor de inhoud.</span><span class="sxs-lookup"><span data-stu-id="afa95-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="afa95-181">Entiteit</span><span class="sxs-lookup"><span data-stu-id="afa95-181">Entity</span></span>        | <span data-ttu-id="afa95-182">Belangrijke samengevoegde metingen</span><span class="sxs-lookup"><span data-stu-id="afa95-182">Key aggregate measurements</span></span> | <span data-ttu-id="afa95-183">Gegevensbron</span><span class="sxs-lookup"><span data-stu-id="afa95-183">Data source</span></span>                                 | <span data-ttu-id="afa95-184">Veld</span><span class="sxs-lookup"><span data-stu-id="afa95-184">Field</span></span>              | <span data-ttu-id="afa95-185">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="afa95-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="afa95-186">Factuurregels</span><span class="sxs-lookup"><span data-stu-id="afa95-186">Invoice lines</span></span> | <span data-ttu-id="afa95-187">Inkoop</span><span class="sxs-lookup"><span data-stu-id="afa95-187">Purchase</span></span>                   | <span data-ttu-id="afa95-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="afa95-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="afa95-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="afa95-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="afa95-190">Het bedrag in de valuta voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="afa95-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="afa95-191">De volgende tabel toont de belangrijkste metingen in de inhoud die worden berekend op basis van de entiteit Factuurregels.</span><span class="sxs-lookup"><span data-stu-id="afa95-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="afa95-192">Maat</span><span class="sxs-lookup"><span data-stu-id="afa95-192">Measure</span></span>               | <span data-ttu-id="afa95-193">Berekening</span><span class="sxs-lookup"><span data-stu-id="afa95-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa95-194">Inkoop huidig jaar</span><span class="sxs-lookup"><span data-stu-id="afa95-194">Purchase current year</span></span> | <span data-ttu-id="afa95-195">Inkoop huidig jaar = SUM('Factuurregels\[Inkoop\])</span><span class="sxs-lookup"><span data-stu-id="afa95-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="afa95-196">Inkoop vorig jaar</span><span class="sxs-lookup"><span data-stu-id="afa95-196">Purchase last year</span></span>    | <span data-ttu-id="afa95-197">Inkoop vorig jaar = CALCULATE(SUM('Factuurregels\[Inkoop\]), SAMEPERIODLASTYEAR(Datums\[Datum\]))</span><span class="sxs-lookup"><span data-stu-id="afa95-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="afa95-198">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="afa95-198">YOY purchase growth</span></span>   | <span data-ttu-id="afa95-199">Groei inkoop jaar-op-jaar = \[Inkoop huidig jaar\] - \[Inkoop vorig jaar\]</span><span class="sxs-lookup"><span data-stu-id="afa95-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="afa95-200">De volgende belangrijke dimensies in de inhoud worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.</span><span class="sxs-lookup"><span data-stu-id="afa95-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="afa95-201">Entiteit</span><span class="sxs-lookup"><span data-stu-id="afa95-201">Entity</span></span>                 | <span data-ttu-id="afa95-202">Voorbeelden van kenmerken</span><span class="sxs-lookup"><span data-stu-id="afa95-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="afa95-203">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="afa95-203">Vendors</span></span>                | <span data-ttu-id="afa95-204">Leveranciersgroepen, Land/regio van leverancier, Leveranciersnaam</span><span class="sxs-lookup"><span data-stu-id="afa95-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="afa95-205">Producten</span><span class="sxs-lookup"><span data-stu-id="afa95-205">Products</span></span>               | <span data-ttu-id="afa95-206">Productnummer, Productnaam, Naam van artikelengroep</span><span class="sxs-lookup"><span data-stu-id="afa95-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="afa95-207">Inkoopcategorieën</span><span class="sxs-lookup"><span data-stu-id="afa95-207">Procurement categories</span></span> | <span data-ttu-id="afa95-208">Aanschaffingscategorie, namen van Aanschaffingscategorieën</span><span class="sxs-lookup"><span data-stu-id="afa95-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="afa95-209">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="afa95-209">Legal entities</span></span>         | <span data-ttu-id="afa95-210">Rechtspersoonnaam</span><span class="sxs-lookup"><span data-stu-id="afa95-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="afa95-211">Datums</span><span class="sxs-lookup"><span data-stu-id="afa95-211">Dates</span></span>                  | <span data-ttu-id="afa95-212">Datums, Jaarverschuiving</span><span class="sxs-lookup"><span data-stu-id="afa95-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="afa95-213">Standaard worden gegevens in de inhoud weergegeven voor het huidige kalenderjaar.</span><span class="sxs-lookup"><span data-stu-id="afa95-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="afa95-214">U kunt echter het datumfilter in de sectie rapportfilters wijzigen.</span><span class="sxs-lookup"><span data-stu-id="afa95-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="afa95-215">U kunt ook het bedrijfsfilter wijzigen.</span><span class="sxs-lookup"><span data-stu-id="afa95-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]