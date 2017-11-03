---
title: Power BI-inhoud voor analyse van inkoopuitgaven
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Analyse inkoopuitgaven. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6485f36802fc4e327e223f47d65c4bdca11c1609
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="39ffd-104">Power BI-inhoud Analyse inkoopuitgaven</span><span class="sxs-lookup"><span data-stu-id="39ffd-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="39ffd-105">In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Analyse inkoopuitgaven**.</span><span class="sxs-lookup"><span data-stu-id="39ffd-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="39ffd-106">In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.</span><span class="sxs-lookup"><span data-stu-id="39ffd-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="39ffd-107">Overzicht</span><span class="sxs-lookup"><span data-stu-id="39ffd-107">Overview</span></span>

<span data-ttu-id="39ffd-108">De Power BI-inhoud **Analyse inkoopuitgaven** is ontworpen om inkoopmanagers en managers met budgetverantwoordelijkheid te helpen de inkoopuitgaven in de gaten te houden.</span><span class="sxs-lookup"><span data-stu-id="39ffd-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="39ffd-109">Managers kunnen inkoopuitgaven op de volgende manieren analyseren:</span><span class="sxs-lookup"><span data-stu-id="39ffd-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="39ffd-110">Inkoop jaar tot heden (op leveranciersgroep en afzonderlijke leveranciers, aanschaffingscategorie en afzonderlijke producten en locatie van de leverancier)</span><span class="sxs-lookup"><span data-stu-id="39ffd-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="39ffd-111">Wijzigingen jaar tot jaar in inkoop (op leveranciersgroep en aanschaffingscategorie)</span><span class="sxs-lookup"><span data-stu-id="39ffd-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="39ffd-112">Op basis van gegevens voor inkooptransacties biedt de inhoud zowel een samengevoegde weergave van de inkoopcijfers uit het hele bedrijf als ook een analyse van de inkoopuitgaven op leverancier en product.</span><span class="sxs-lookup"><span data-stu-id="39ffd-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="39ffd-113">Rapporten maken wijzigingen in de inkoopuitgaven in het verloop van de tijd duidelijk.</span><span class="sxs-lookup"><span data-stu-id="39ffd-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="39ffd-114">Daarom kunnen de rapporten worden gebruikt om managers te wijzen op positieve en negatieve trends in de uitgaven voor afzonderlijke leveranciers en producten.</span><span class="sxs-lookup"><span data-stu-id="39ffd-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="39ffd-115">Daarnaast geven grafieken de inkoopuitgaven weer voor verschillende inkoopcategorieën en leveranciersgroepen.</span><span class="sxs-lookup"><span data-stu-id="39ffd-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="39ffd-116">Categorie- en regiomanagers kunnen met deze grafieken veranderingen in het uitgavegedrag opsporen.</span><span class="sxs-lookup"><span data-stu-id="39ffd-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="39ffd-117">Toegang tot de Power BI-inhoud verkrijgen</span><span class="sxs-lookup"><span data-stu-id="39ffd-117">Accessing the Power BI content</span></span>
<span data-ttu-id="39ffd-118">Als u werkt met Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), vindt u de Power BI-inhoud **Analyse inkoopuitgaven** op de pagina **Inkoop- en uitgavenanalyse** (**Inkoopbeheer** > **Query's en rapporten** > **Inkoopprestatieanalyse** > **Inkoop- en uitgavenanalyse**).</span><span class="sxs-lookup"><span data-stu-id="39ffd-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="39ffd-119">Metrische gegevens die zijn opgenomen in de Power BI-inhoud</span><span class="sxs-lookup"><span data-stu-id="39ffd-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="39ffd-120">De Power BI-inhoud **Analyse inkoopuitgaven** bevat een rapport dat uit een verzameling van metrische gegevens bestaat.</span><span class="sxs-lookup"><span data-stu-id="39ffd-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="39ffd-121">Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen.</span><span class="sxs-lookup"><span data-stu-id="39ffd-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="39ffd-122">In de volgende tabel vindt u een overzicht van de visualisaties.</span><span class="sxs-lookup"><span data-stu-id="39ffd-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39ffd-123">Rapportpagina</span><span class="sxs-lookup"><span data-stu-id="39ffd-123">Report page</span></span></th>
<th><span data-ttu-id="39ffd-124">Diagrammen</span><span class="sxs-lookup"><span data-stu-id="39ffd-124">Charts</span></span></th>
<th><span data-ttu-id="39ffd-125">Tegels</span><span class="sxs-lookup"><span data-stu-id="39ffd-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39ffd-126">Inkoop op leverancier</span><span class="sxs-lookup"><span data-stu-id="39ffd-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="39ffd-127">Top 10-leveranciers op inkoop (gestapeld staafdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="39ffd-128">Totale inkoop op groep / land / naam leverancier (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="39ffd-129">Inkoop op groep / land / naam leverancier (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="39ffd-130">Gemiddelde inkoop op groep / land / naam leverancier (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="39ffd-131">Totaalinkoop</span><span class="sxs-lookup"><span data-stu-id="39ffd-131">Total purchase</span></span></li>
<li><span data-ttu-id="39ffd-132">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="39ffd-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="39ffd-133">Totaal aantal leveranciers</span><span class="sxs-lookup"><span data-stu-id="39ffd-133">Total # vendors</span></span></li>
<li><span data-ttu-id="39ffd-134">Totaal aantal actieve leveranciers</span><span class="sxs-lookup"><span data-stu-id="39ffd-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39ffd-135">Inkoop op product</span><span class="sxs-lookup"><span data-stu-id="39ffd-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="39ffd-136">Inkoop per aanschaffingscategorie / productnaam (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="39ffd-137">Totale inkoop per aanschaffingscategorie / productnaam (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="39ffd-138">Top 10-producten op inkoop (gestapeld staafdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="39ffd-139">Totaal aantal producten</span><span class="sxs-lookup"><span data-stu-id="39ffd-139">Total # of products</span></span></li>
<li><span data-ttu-id="39ffd-140">Totaal aantal actieve producten percentage van totale aantal producten</span><span class="sxs-lookup"><span data-stu-id="39ffd-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="39ffd-141">Aantal producten dat 80% van inkoop oplevert</span><span class="sxs-lookup"><span data-stu-id="39ffd-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39ffd-142">Inkoop op periode*</span><span class="sxs-lookup"><span data-stu-id="39ffd-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="39ffd-143">Inkoop op maand / dag (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="39ffd-144">Cumulatieve inkoop afwijking jaar-op-jaar (watervalgrafiek)</span><span class="sxs-lookup"><span data-stu-id="39ffd-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="39ffd-145">Totale inkoop groei jaar-op-jaar (kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="39ffd-146">Inkoopoverzicht (matrix)</span><span class="sxs-lookup"><span data-stu-id="39ffd-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="39ffd-147">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="39ffd-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="39ffd-148">Inkoopgroei jaar-op-jaar %</span><span class="sxs-lookup"><span data-stu-id="39ffd-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39ffd-149">Inkoop op leverancierlocatie</span><span class="sxs-lookup"><span data-stu-id="39ffd-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="39ffd-150">Inkoop op stad</span><span class="sxs-lookup"><span data-stu-id="39ffd-150">Purchase by city</span></span></li>
<li><span data-ttu-id="39ffd-151">Inkoop groei jaar-op-jaar %</span><span class="sxs-lookup"><span data-stu-id="39ffd-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="39ffd-152">Inkoop op land</span><span class="sxs-lookup"><span data-stu-id="39ffd-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39ffd-153">Analyse inkoopuitgaven op tijd</span><span class="sxs-lookup"><span data-stu-id="39ffd-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="39ffd-154">Inkoop huidige jaar op maand / dag (lijndiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="39ffd-155">Inkooporders huidig en vorig jaar (lijn- en kolomdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39ffd-156">Analyse inkoopuitgaven op leverancier</span><span class="sxs-lookup"><span data-stu-id="39ffd-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="39ffd-157">Top 10 leverancier inkoop % van inkoop (trechterdiagram)</span><span class="sxs-lookup"><span data-stu-id="39ffd-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="39ffd-158">Top 10 leveranciers met een gestegen uitgaven jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="39ffd-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="39ffd-159">Top 10 leveranciers met een gedaalde uitgaven jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="39ffd-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="39ffd-160">\* Inkoop dit jaar en vorig jaar en groei per aanschaffingscategorie</span><span class="sxs-lookup"><span data-stu-id="39ffd-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="39ffd-161">De Power BI-inhoud uitbreiden</span><span class="sxs-lookup"><span data-stu-id="39ffd-161">Extending the Power BI content</span></span>
<span data-ttu-id="39ffd-162">Met behulp van de inhoudpakketten die beschikbaar zijn in Microsoft Dynamics Lifecycle Services (LCS) kunt u grondige analyses verschaffen aan personen die zich niet bij Microsoft Dynamics 365 aanmelden.</span><span class="sxs-lookup"><span data-stu-id="39ffd-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="39ffd-163">U kunt deze inhoudpakketten wijzigen zodat ze andere rapporten of visuele elementen bevatten, en de inhoudpakketten vervolgens publiceren naar uw Power BI.com-tenant voor analyse.</span><span class="sxs-lookup"><span data-stu-id="39ffd-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="39ffd-164">U vindt de Power BI-inhoud **Analyse inkoopuitgaven** in de bibliotheek voor gedeelde materialen in LCS.</span><span class="sxs-lookup"><span data-stu-id="39ffd-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="39ffd-165">Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="39ffd-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="39ffd-166">Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="39ffd-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="39ffd-167">Let erop dat u de inhoud **Analyse inkoopuitgaven** downloadt, die van toepassing is voor de versie van Dynamics 365 die u gebruikt.</span><span class="sxs-lookup"><span data-stu-id="39ffd-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="39ffd-168">Als u werkt met Microsoft Dynamics 365 for Operations, versie 1611, is KB 4011327 een voorwaarde voor gebruik van deze volgende Power BI-inhoud:</span><span class="sxs-lookup"><span data-stu-id="39ffd-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="39ffd-169">Nadat u zich bij LCS hebt aangemeld, kunt u de KB hier openen: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="39ffd-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="39ffd-170">Gegevensmodel en entiteiten</span><span class="sxs-lookup"><span data-stu-id="39ffd-170">Data model and entities</span></span>
<span data-ttu-id="39ffd-171">De volgende gegevens wordt gebruikt om de rapportpagina's in de Power BI-inhoud **Analyse inkoopuitgaven** te vullen.</span><span class="sxs-lookup"><span data-stu-id="39ffd-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="39ffd-172">Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag.</span><span class="sxs-lookup"><span data-stu-id="39ffd-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="39ffd-173">De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses.</span><span class="sxs-lookup"><span data-stu-id="39ffd-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="39ffd-174">Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="39ffd-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="39ffd-175">De samengevoegde metingen in deze inhoud zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Inkoop-cube in Microsoft Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="39ffd-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="39ffd-176">Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken.</span><span class="sxs-lookup"><span data-stu-id="39ffd-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="39ffd-177">Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Overzicht van Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="39ffd-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="39ffd-178">De volgende belangrijke samengevoegde metingen zijn rechtstreeks vanuit de entiteit Factuurregels beschikbaar en worden gebruikt als basis voor de inhoud.</span><span class="sxs-lookup"><span data-stu-id="39ffd-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="39ffd-179">Entiteit</span><span class="sxs-lookup"><span data-stu-id="39ffd-179">Entity</span></span>        | <span data-ttu-id="39ffd-180">Belangrijke samengevoegde metingen</span><span class="sxs-lookup"><span data-stu-id="39ffd-180">Key aggregate measurements</span></span> | <span data-ttu-id="39ffd-181">Gegevensbron</span><span class="sxs-lookup"><span data-stu-id="39ffd-181">Data source</span></span>                                 | <span data-ttu-id="39ffd-182">Veld</span><span class="sxs-lookup"><span data-stu-id="39ffd-182">Field</span></span>              | <span data-ttu-id="39ffd-183">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="39ffd-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="39ffd-184">Factuurregels</span><span class="sxs-lookup"><span data-stu-id="39ffd-184">Invoice lines</span></span> | <span data-ttu-id="39ffd-185">Inkoop</span><span class="sxs-lookup"><span data-stu-id="39ffd-185">Purchase</span></span>                   | <span data-ttu-id="39ffd-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="39ffd-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="39ffd-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="39ffd-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="39ffd-188">Het bedrag in de valuta voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="39ffd-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="39ffd-189">De volgende tabel toont de belangrijkste metingen in de inhoud die worden berekend op basis van de entiteit Factuurregels.</span><span class="sxs-lookup"><span data-stu-id="39ffd-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="39ffd-190">Maat</span><span class="sxs-lookup"><span data-stu-id="39ffd-190">Measure</span></span>               | <span data-ttu-id="39ffd-191">Berekening</span><span class="sxs-lookup"><span data-stu-id="39ffd-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39ffd-192">Inkoop huidig jaar</span><span class="sxs-lookup"><span data-stu-id="39ffd-192">Purchase current year</span></span> | <span data-ttu-id="39ffd-193">Inkoop huidig jaar = SUM('Factuurregels\[Inkoop\])</span><span class="sxs-lookup"><span data-stu-id="39ffd-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="39ffd-194">Inkoop vorig jaar</span><span class="sxs-lookup"><span data-stu-id="39ffd-194">Purchase last year</span></span>    | <span data-ttu-id="39ffd-195">Inkoop vorig jaar = CALCULATE(SUM('Factuurregels\[Inkoop\]), SAMEPERIODLASTYEAR(Datums\[Datum\]))</span><span class="sxs-lookup"><span data-stu-id="39ffd-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="39ffd-196">Inkoopgroei jaar-op-jaar</span><span class="sxs-lookup"><span data-stu-id="39ffd-196">YOY purchase growth</span></span>   | <span data-ttu-id="39ffd-197">Groei inkoop jaar-op-jaar = \[Inkoop huidig jaar\] - \[Inkoop vorig jaar\]</span><span class="sxs-lookup"><span data-stu-id="39ffd-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="39ffd-198">De volgende belangrijke dimensies in de inhoud worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.</span><span class="sxs-lookup"><span data-stu-id="39ffd-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="39ffd-199">Entiteit</span><span class="sxs-lookup"><span data-stu-id="39ffd-199">Entity</span></span>                 | <span data-ttu-id="39ffd-200">Voorbeelden van kenmerken</span><span class="sxs-lookup"><span data-stu-id="39ffd-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="39ffd-201">Leveranciers</span><span class="sxs-lookup"><span data-stu-id="39ffd-201">Vendors</span></span>                | <span data-ttu-id="39ffd-202">Leveranciersgroepen, Land/regio van leverancier, Leveranciersnaam</span><span class="sxs-lookup"><span data-stu-id="39ffd-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="39ffd-203">Producten</span><span class="sxs-lookup"><span data-stu-id="39ffd-203">Products</span></span>               | <span data-ttu-id="39ffd-204">Productnummer, Productnaam, Naam van artikelengroep</span><span class="sxs-lookup"><span data-stu-id="39ffd-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="39ffd-205">Inkoopcategorieën</span><span class="sxs-lookup"><span data-stu-id="39ffd-205">Procurement categories</span></span> | <span data-ttu-id="39ffd-206">Aanschaffingscategorie, namen van Aanschaffingscategorieën</span><span class="sxs-lookup"><span data-stu-id="39ffd-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="39ffd-207">Rechtspersonen</span><span class="sxs-lookup"><span data-stu-id="39ffd-207">Legal entities</span></span>         | <span data-ttu-id="39ffd-208">Rechtspersoonnaam</span><span class="sxs-lookup"><span data-stu-id="39ffd-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="39ffd-209">Datums</span><span class="sxs-lookup"><span data-stu-id="39ffd-209">Dates</span></span>                  | <span data-ttu-id="39ffd-210">Datums, Jaarverschuiving</span><span class="sxs-lookup"><span data-stu-id="39ffd-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="39ffd-211">Standaard worden gegevens in de inhoud weergegeven voor het huidige kalenderjaar.</span><span class="sxs-lookup"><span data-stu-id="39ffd-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="39ffd-212">U kunt echter het datumfilter in de sectie rapportfilters wijzigen.</span><span class="sxs-lookup"><span data-stu-id="39ffd-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="39ffd-213">U kunt ook het bedrijfsfilter wijzigen.</span><span class="sxs-lookup"><span data-stu-id="39ffd-213">You can also change the company filter.</span></span>

