---
title: Een hoofdplanningsuitvoering controleren
description: In dit onderwerp wordt beschreven hoe de productieplanner kan zien of een hoofdplanning wordt uitgevoerd.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 159043f37b067df26fdd1de5610eafd663bf6a57
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209554"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="d2dd6-103">Een hoofdplanningsuitvoering controleren</span><span class="sxs-lookup"><span data-stu-id="d2dd6-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="d2dd6-104">Een Gantt-diagram gebruiken om de voortgang van de hoofdplanning te visualiseren</span><span class="sxs-lookup"><span data-stu-id="d2dd6-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="d2dd6-105">Op de pagina **Voortgang van hoofdplanning weergeven** kunt u details van historische hoofdplanningsuitvoeringen als een Gantt-diagram weergeven.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="d2dd6-106">Deze functionaliteit kan u helpen om te begrijpen hoeveel tijd wordt besteed aan de verschillende fasen van de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="d2dd6-107">Voor een huidige actieve planningstaak kan de pagina **Voortgang van hoofdplanning weergeven** worden gebruikt om de voortgang bij te houden en de geschatte resterende tijd weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="d2dd6-108">De functie voor visualisatie van de voortgang van de hoofdplanning inschakelen en gebruiken</span><span class="sxs-lookup"><span data-stu-id="d2dd6-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="d2dd6-109">Volg deze stappen om deze functionaliteit te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="d2dd6-110">Selecteer **Visualisatie van voortgang van hoofdplanning** in de lijst op het tabblad **Nieuw** van het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="d2dd6-111">Als de functie niet wordt weergegeven op het tabblad **Nieuw**, kijkt u op de tabbladen **Niet ingeschakeld** en **Alle**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="d2dd6-112">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-112">Select **Enable now**.</span></span> <span data-ttu-id="d2dd6-113">U kunt ook **Planning** selecteren en vervolgens het tijdstip selecteren waarop u de functie wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="d2dd6-114">Op de pagina **Voortgang van hoofdplanning weergeven** kunnen zowel historische planningstaken als actieve planningstaken worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="d2dd6-115">Er zijn twee opties voor het weergeven van historische planningstaken.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="d2dd6-116">Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen** en selecteer in het actievenster de optie **Historie**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="d2dd6-117">Selecteer de gewenste taak en selecteer **Query's** en **Voortgang weergeven**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="d2dd6-118">Ga naar **Hoofdplanning \> Werkgebieden \> Hoofdplanning** en klik op de tegel Hoofdplanning op **Historie**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="d2dd6-119">Selecteer de gewenste taak en selecteer **Query's** en **Voortgang weergeven**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="d2dd6-120">Er zijn twee opties voor het weergeven van actieve planningstaken.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="d2dd6-121">Ga naar **Hoofdplanning \> Werkgebieden \> Hoofdplanning** en selecteer in het actievenster de optie **Onvoltooid planningsproces**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="d2dd6-122">Selecteer de gewenste taak en selecteer **Query's** en **Voortgang weergeven**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="d2dd6-123">Ga naar **Hoofdplanning \> Werkgebieden \> Hoofdplanning** en klik op de tegel Hoofdplanning op **Voortgang weergeven**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="d2dd6-124">Selecteer de gewenste taak en selecteer **Query's** en **Voortgang weergeven**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="d2dd6-125">U kunt actieve taken alleen weergeven wanneer een planningstaak wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="d2dd6-126">Een hoofdplanningstaak analyseren</span><span class="sxs-lookup"><span data-stu-id="d2dd6-126">Analyze a master planning job</span></span>

<span data-ttu-id="d2dd6-127">In het Gantt-diagram kunt u elk van de volgende planningsprocessen uitvouwen om extra details weer te geven over de tijd die wordt besteed:</span><span class="sxs-lookup"><span data-stu-id="d2dd6-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="d2dd6-128">Bezig met initialiseren</span><span class="sxs-lookup"><span data-stu-id="d2dd6-128">Initializing</span></span>
- <span data-ttu-id="d2dd6-129">Gegevens verwijderen en invoegen</span><span class="sxs-lookup"><span data-stu-id="d2dd6-129">Deleting and inserting data</span></span>
- <span data-ttu-id="d2dd6-130">Behoefteplan</span><span class="sxs-lookup"><span data-stu-id="d2dd6-130">Coverage planning</span></span>
- <span data-ttu-id="d2dd6-131">Vertragingen</span><span class="sxs-lookup"><span data-stu-id="d2dd6-131">Delays</span></span>
- <span data-ttu-id="d2dd6-132">Actieberichten</span><span class="sxs-lookup"><span data-stu-id="d2dd6-132">Action messages</span></span>
- <span data-ttu-id="d2dd6-133">Voltooiing</span><span class="sxs-lookup"><span data-stu-id="d2dd6-133">Finalization</span></span>
- <span data-ttu-id="d2dd6-134">Automatische fiattering</span><span class="sxs-lookup"><span data-stu-id="d2dd6-134">Auto-firming</span></span>

<span data-ttu-id="d2dd6-135">Het Gantt-diagram is een handige tool als u de gevolgen van het gebruik van actieberichten wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="d2dd6-136">Navigatie in het Gantt-diagram</span><span class="sxs-lookup"><span data-stu-id="d2dd6-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="d2dd6-137">Als u de geselecteerde groep wilt uitvouwen en de details wilt weergeven, selecteert u het plusteken (**+**) in de structuurweergave.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="d2dd6-138">Als u de geselecteerde groep wilt samenvouwen, selecteert u het minteken (**–**) in de structuurweergave.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="d2dd6-139">U kunt het toetsenbord gebruiken voor navigatie.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="d2dd6-140">Gebruik de toetsen **Pijl-omhoog** en **Pijl-omlaag** om tussen rijen te navigeren.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="d2dd6-141">Gebruik de toetsen **Pijl-rechts** en **Pijl-links** om groepen uit en samen te vouwen.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="d2dd6-142">Als u alle niveaus in het Gantt-diagram wilt openen of sluiten, selecteert u **Alles uitvouwen** of **Alles samenvouwen**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="d2dd6-143">Als u de bijbehorende verwerkingstijd wilt weergeven, plaatst u de muisaanwijzer op een taak.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="d2dd6-144">(Taken zijn het laagste niveau in het Gantt-diagram.)</span><span class="sxs-lookup"><span data-stu-id="d2dd6-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="d2dd6-145">Een extra hoofdplanningsuitvoering weergeven om taken te vergelijken</span><span class="sxs-lookup"><span data-stu-id="d2dd6-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="d2dd6-146">Door een hoofdplanningstaak te selecteren in het veld **Extra hoofdplanningsuitvoering weergeven**, kunt u een extra hoofdplanningsuitvoering weergeven in het Gantt-diagram en de twee taken met elkaar vergelijken.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="d2dd6-147">Weergave op stuklijstniveau</span><span class="sxs-lookup"><span data-stu-id="d2dd6-147">BOM-level display</span></span>

<span data-ttu-id="d2dd6-148">Stuklijstniveaus worden anders weer gegeven voor behoefteplanningen, vertragingen, acties en fiatteringen.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="d2dd6-149">**Behoefteplan**: stuklijstniveaus worden zoals verwacht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="d2dd6-150">Ze worden van boven naar beneden berekend.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="d2dd6-151">**Voorbeeld**: stuklijstniveau 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="d2dd6-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="d2dd6-152">**Vertragingen**: stuklijstniveaus worden weer gegeven als de stuklijstniveaus van de behoefteplanning vermenigvuldigd met –1.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="d2dd6-153">(Met andere woorden, ze hebben een minteken.)</span><span class="sxs-lookup"><span data-stu-id="d2dd6-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="d2dd6-154">**Voorbeeld**: stuklijstniveau –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="d2dd6-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="d2dd6-155">**Actiebericht**: stuklijstniveaus worden zoals verwacht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="d2dd6-156">Ze worden van boven naar beneden berekend.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="d2dd6-157">**Voorbeeld**: stuklijstniveau 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="d2dd6-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="d2dd6-158">**Automatische fiattering**: stuklijstniveaus worden weergegeven als 999 min het stuklijstniveau van de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="d2dd6-159">**Voorbeeld**: stuklijstniveau 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="d2dd6-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="d2dd6-160">De volgende tabel biedt een overzicht van het gedrag.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="d2dd6-161">Stuklijstniveau dat wordt weergegeven</span><span class="sxs-lookup"><span data-stu-id="d2dd6-161">BOM level that is shown</span></span> | <span data-ttu-id="d2dd6-162">Eindartikel</span><span class="sxs-lookup"><span data-stu-id="d2dd6-162">End item</span></span> | <span data-ttu-id="d2dd6-163">Subonderdeel</span><span class="sxs-lookup"><span data-stu-id="d2dd6-163">Subcomponent</span></span> | <span data-ttu-id="d2dd6-164">Grondstoffen</span><span class="sxs-lookup"><span data-stu-id="d2dd6-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="d2dd6-165">Behoefteplan</span><span class="sxs-lookup"><span data-stu-id="d2dd6-165">Coverage planning</span></span> | <span data-ttu-id="d2dd6-166">0</span><span class="sxs-lookup"><span data-stu-id="d2dd6-166">0</span></span> | <span data-ttu-id="d2dd6-167">1</span><span class="sxs-lookup"><span data-stu-id="d2dd6-167">1</span></span> | <span data-ttu-id="d2dd6-168">2</span><span class="sxs-lookup"><span data-stu-id="d2dd6-168">2</span></span> |
| <span data-ttu-id="d2dd6-169">Vertragingen</span><span class="sxs-lookup"><span data-stu-id="d2dd6-169">Delays</span></span> | <span data-ttu-id="d2dd6-170">0</span><span class="sxs-lookup"><span data-stu-id="d2dd6-170">0</span></span> | <span data-ttu-id="d2dd6-171">–1</span><span class="sxs-lookup"><span data-stu-id="d2dd6-171">–1</span></span> | <span data-ttu-id="d2dd6-172">–2</span><span class="sxs-lookup"><span data-stu-id="d2dd6-172">–2</span></span> |
| <span data-ttu-id="d2dd6-173">Actiebericht</span><span class="sxs-lookup"><span data-stu-id="d2dd6-173">Action message</span></span> | <span data-ttu-id="d2dd6-174">0</span><span class="sxs-lookup"><span data-stu-id="d2dd6-174">0</span></span> | <span data-ttu-id="d2dd6-175">1</span><span class="sxs-lookup"><span data-stu-id="d2dd6-175">1</span></span> | <span data-ttu-id="d2dd6-176">2</span><span class="sxs-lookup"><span data-stu-id="d2dd6-176">2</span></span> |
| <span data-ttu-id="d2dd6-177">Automatische fiattering</span><span class="sxs-lookup"><span data-stu-id="d2dd6-177">Auto-firming</span></span> | <span data-ttu-id="d2dd6-178">999</span><span class="sxs-lookup"><span data-stu-id="d2dd6-178">999</span></span> | <span data-ttu-id="d2dd6-179">998</span><span class="sxs-lookup"><span data-stu-id="d2dd6-179">998</span></span> | <span data-ttu-id="d2dd6-180">997</span><span class="sxs-lookup"><span data-stu-id="d2dd6-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="d2dd6-181">Voortgang visualiseren</span><span class="sxs-lookup"><span data-stu-id="d2dd6-181">Visualize progress</span></span>

<span data-ttu-id="d2dd6-182">Als u een hoofdplanningstaak bekijkt die momenteel wordt uitgevoerd, wordt de voortgang met kleuren weergegeven in het Gantt-diagram.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="d2dd6-183">De volgende kleuren zijn van toepassing op het blauwe thema:</span><span class="sxs-lookup"><span data-stu-id="d2dd6-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="d2dd6-184">Voor andere kleurenthema's zijn de kleuren anders.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="d2dd6-185">**Donkerblauw**: voltooide planningstaken.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="d2dd6-186">**Oranje**: de taak die momenteel wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="d2dd6-187">**Lichtblauw**: de raming voor de resterende taken.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="d2dd6-188">De kleur wordt alleen weergegeven op het laagste niveau in het Gantt-diagram.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="d2dd6-189">Selecteer **Alles uitvouwen** om alle taken in de hoofdplanningstaak weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="d2dd6-190">De raming van de resterende taken is gebaseerd op historische hoofdplanningstaken.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="d2dd6-191">De hoofdplanning uitvoeren en verwerkingstijd bijhouden</span><span class="sxs-lookup"><span data-stu-id="d2dd6-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="d2dd6-192">Selecteer **Hoofdplanning** in het standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="d2dd6-193">Typ of selecteer een waarde in het veld **Plannen**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="d2dd6-194">Selecteer **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-194">Select **Run**.</span></span>
1. <span data-ttu-id="d2dd6-195">Stel de optie **Verwerkingstijd traceren** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="d2dd6-196">Voer een getal in het veld **Aantal threads** in.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="d2dd6-197">Selecteer **Filter** op het sneltabblad **Op te nemen records**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="d2dd6-198">Selecteer in het raster de rij waarin het veld **Veld** is ingesteld op **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="d2dd6-199">Voer een waarde in het veld **Criteria** in.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="d2dd6-200">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2dd6-200">Select **OK**.</span></span>
