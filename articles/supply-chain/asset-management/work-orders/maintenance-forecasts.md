---
title: Prognoses voor onderhoud
description: In dit onderwerp wordt uitgelegd wat prognoses voor onderhoud zijn in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2686dd6db032239e2a3aac03f3998cee055302f6
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425893"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="9f196-103">Prognoses voor onderhoud</span><span class="sxs-lookup"><span data-stu-id="9f196-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="9f196-104">Wanneer u een werkorder maakt, kunt u werkordertaken maken die gerelateerde activa en typen onderhoudstaken hebben.</span><span class="sxs-lookup"><span data-stu-id="9f196-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="9f196-105">Wanneer u een type onderhoudstaak selecteert dat prognoses voor onderhoud bevat, worden de prognoses automatisch naar de werkorder gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="9f196-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="9f196-106">U kunt mogelijk prognoseregels toevoegen aan of verwijderen uit een werkorder.</span><span class="sxs-lookup"><span data-stu-id="9f196-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="9f196-107">De instelling van de levenscyclusstatus van de werkorder, het gerelateerde projecttype en de faseregels die betrekking hebben op het projecttype bepalen of u journaalregels kunt toevoegen of bewerken.</span><span class="sxs-lookup"><span data-stu-id="9f196-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="9f196-108">Zie [Prognoses, werkorders en projecten](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)voor meer informatie over levenscyclusstatussen van werkorders en gerelateerde projectfasen.</span><span class="sxs-lookup"><span data-stu-id="9f196-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="9f196-109">Selecteer **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="9f196-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9f196-110">Selecteer de werkorder in de lijst en selecteer vervolgens in het actievenster > tabblad **Werkorder** > groep **Project** de optie **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="9f196-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="9f196-111">Op de pagina **Prognose voor onderhoud** worden de prognoseregels van het type onderhoudstaak dat in de werkordertaak is geselecteerd, weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9f196-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="9f196-112">Een urenprognose aan een werkorder toevoegen</span><span class="sxs-lookup"><span data-stu-id="9f196-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="9f196-113">Selecteer op de pagina **Onderhoudsprognose voor werkorders** de werkordertaak waaraan u een prognose wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9f196-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="9f196-114">Selecteer op het sneltabblad **Uren** de optie **Toevoegen** om een nieuwe regel te maken.</span><span class="sxs-lookup"><span data-stu-id="9f196-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="9f196-115">Selecteer een categorie in het veld **Categorie**.</span><span class="sxs-lookup"><span data-stu-id="9f196-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="9f196-116">Voer het aantal voorspelde uren in het veld **Uren** in.</span><span class="sxs-lookup"><span data-stu-id="9f196-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="9f196-117">Selecteer in het veld **Regeleigenschap** het toeslagtype dat op de regel moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9f196-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="9f196-118">Een prognose voor artikelen toevoegen aan een werkorder</span><span class="sxs-lookup"><span data-stu-id="9f196-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="9f196-119">Er zijn drie manieren om artikelen aan een onderhoudsprognose voor werkorders toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="9f196-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="9f196-120">U kunt regels maken voor artikelen (reserve-onderdelen) die niet zijn opgenomen in de lijst met reserve-onderdelen of activumstuklijst, u kunt reserve-onderdelen selecteren in de lijst met goedgekeurde onderdelen of u kunt artikelen selecteren in de activumstuklijst.</span><span class="sxs-lookup"><span data-stu-id="9f196-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="9f196-121">Selecteer op de pagina **Onderhoudsprognose voor werkorders** de werkordertaak waaraan u een prognose wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9f196-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="9f196-122">Voeg op het sneltabblad **Artikelen** de artikelen toe aan de onderhoudsprognose via de desbetreffende methode.</span><span class="sxs-lookup"><span data-stu-id="9f196-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="9f196-123">Als u een nieuwe regel wilt maken voor een reserve-onderdeel dat nog niet voorkomt in de lijst met reserve-onderdelen of de activumstuklijst, voert u de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="9f196-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="9f196-124">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9f196-124">Select **Add**.</span></span>
2. <span data-ttu-id="9f196-125">Selecteer het artikel in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="9f196-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="9f196-126">Voer in het veld **Verkoophoeveelheid** de hoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="9f196-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="9f196-127">Selecteer de maateenheid van de hoeveelheid in het veld **Eenheid**.</span><span class="sxs-lookup"><span data-stu-id="9f196-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="9f196-128">Geef in de velden **Kostprijs** en **Valuta** de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="9f196-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="9f196-129">Selecteer een regeleigenschap in het veld **Regeleigenschap**.</span><span class="sxs-lookup"><span data-stu-id="9f196-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="9f196-130">Als u de lijst met dimensies wilt wijzigen die op de artikelregels wordt weergegeven, selecteert u **Voorraad** > **Weergavedimensies**, selecteert u de dimensies en stelt u de optie **Instellingen opslaan** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9f196-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="9f196-131">Voer de volgende stappen uit om een reserveonderdeel toe te voegen uit een lijst met goedgekeurde reserveonderdelen:</span><span class="sxs-lookup"><span data-stu-id="9f196-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="9f196-132">Selecteer **Reserveonderdelen toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9f196-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="9f196-133">Selecteer het reserveonderdeel en bewerk zo nodig de gerelateerde gegevens.</span><span class="sxs-lookup"><span data-stu-id="9f196-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="9f196-134">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f196-134">Select **OK**.</span></span>

<span data-ttu-id="9f196-135">Voer de volgende stappen uit om een artikel toe te voegen vanuit de activumstuklijst:</span><span class="sxs-lookup"><span data-stu-id="9f196-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="9f196-136">Selecteer **Stuklijstartikelen toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="9f196-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="9f196-137">Selecteer het onderdeel en bewerk zo nodig de gerelateerde gegevens.</span><span class="sxs-lookup"><span data-stu-id="9f196-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="9f196-138">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f196-138">Select **OK**.</span></span>

<span data-ttu-id="9f196-139">Voor een overzicht van waar het artikel op de geselecteerde regel wordt gebruikt in relatie tot activa, standaardwaarden voor taaktypen, reserveonderdelen en werkorders in Activabeheer, selecteert u **Artikel waar gebruikt**.</span><span class="sxs-lookup"><span data-stu-id="9f196-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="9f196-140">Zie [Artikel waar gebruikt](../controlling-and-reporting/item-where-used.md) voor meer informatie over dit overzicht.</span><span class="sxs-lookup"><span data-stu-id="9f196-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="9f196-141">Een onkostenprognose toevoegen aan een werkorder</span><span class="sxs-lookup"><span data-stu-id="9f196-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="9f196-142">Selecteer op de pagina **Onderhoudsprognose voor werkorders** de werkordertaak waaraan u een prognose wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="9f196-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="9f196-143">Selecteer op het sneltabblad **Onkosten** de optie **Toevoegen** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="9f196-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="9f196-144">Selecteer een categorie in het veld **Categorie**.</span><span class="sxs-lookup"><span data-stu-id="9f196-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="9f196-145">Voer in het veld **Hoeveelheid** de hoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="9f196-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="9f196-146">Voer de desbetreffende waarden in in de velden **Kostprijs**, **Verkoopvaluta** en **Verkoopprijs**.</span><span class="sxs-lookup"><span data-stu-id="9f196-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="9f196-147">Selecteer in het veld **Regeleigenschap** het toeslagtype dat op de regel moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9f196-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="9f196-148">Op het sneltabblad **Totalen van prognose voor onderhoud** wordt een overzicht weergegeven van het aantal regels dat op elk sneltabblad is gemaakt, voor de geselecteerde werkordertaak en voor de werkorder.</span><span class="sxs-lookup"><span data-stu-id="9f196-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="9f196-149">U ziet ook het totaal van de voorspelde werkuren voor de werkordertaak en de werkorder.</span><span class="sxs-lookup"><span data-stu-id="9f196-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="9f196-150">In de onderstaande afbeelding ziet u een voorbeeld van de pagina **Onderhoudsprognose werkorder**.</span><span class="sxs-lookup"><span data-stu-id="9f196-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Figuur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="9f196-152">Prognoses van werkorders automatisch bijwerken</span><span class="sxs-lookup"><span data-stu-id="9f196-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="9f196-153">Als uurkosten, artikelkosten en onkosten worden bijgewerkt in andere Microsoft Dynamics 365 for Finance and Operations-modules, kunnen prognoses voor werkorders in Activabeheer automatisch worden bijgewerkt met deze wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="9f196-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="9f196-154">Deze functie helpt garanderen dat altijd de laatste kostprijzen in uw prognoses voor werkorders gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9f196-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="9f196-155">U kunt ook soortgelijke updates uitvoeren voor [prognoses voor onderhoudstaken](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="9f196-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="9f196-156">Selecteer **Activabeheer** > **Periodiek** > **Prognose** > **Prognose voor werkorder bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="9f196-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="9f196-157">In het dialoogvenster **Prognose voor werkorder bijwerken** kunt u in het sneltabblad **Op te nemen records** zo nodig selecties toevoegen met betrekking tot specifieke werkorders of werkordertaken.</span><span class="sxs-lookup"><span data-stu-id="9f196-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="9f196-158">Klik op **Filter** om de relevante selecties te maken.</span><span class="sxs-lookup"><span data-stu-id="9f196-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="9f196-159">Indien nodig kunt u de automatische update op het Sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="9f196-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="9f196-160">Selecteer **OK** om de update van de prognose te starten.</span><span class="sxs-lookup"><span data-stu-id="9f196-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="9f196-161">In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Prognose voor werkorder bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="9f196-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Figuur 2](media/07-work-orders.png)
