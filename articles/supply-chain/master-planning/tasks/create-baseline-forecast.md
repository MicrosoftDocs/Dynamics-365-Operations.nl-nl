---
title: Een basislijnprognose maken
description: Een productieplanner kan een basislijnprognose maken of door prognosemodellen voor de tijdreeks te gebruiken of door de historische vraag naar de prognose te kopiëren.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f777503c6161376afc933322b5d60054e2468b34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983411"
---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="a4c2f-103">Een basislijnprognose maken</span><span class="sxs-lookup"><span data-stu-id="a4c2f-103">Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4c2f-104">Een productieplanner kan een basislijnprognose maken of door prognosemodellen voor de tijdreeks te gebruiken of door de historische vraag naar de prognose te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="a4c2f-105">Deze procedure laat zien hoe u de historische vraag kopieert om een basislijnprognose te maken voor alle producten met één artikeltoewijzingssleutel.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="a4c2f-106">Een artikeltoewijzingssleutel instellen</span><span class="sxs-lookup"><span data-stu-id="a4c2f-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="a4c2f-107">Ga naar Hoofdplanning > Instellingen > Intercompany-planningsgroepen.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="a4c2f-108">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a4c2f-109">Filter bijvoorbeeld op het Veld Naam met een waarde van "10".</span><span class="sxs-lookup"><span data-stu-id="a4c2f-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="a4c2f-110">Vraagprognose uitvoeren voor verschillende rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="a4c2f-111">Daarom moet u alle bedrijven instellen waarvoor u prognoses wilt genereren in één intercompany-planningsgroep.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="a4c2f-112">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a4c2f-113">Klik op Artikeltoewijzingssleutels.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="a4c2f-114">Selecteer alle artikeltoewijzingssleutels waarvoor u prognoses wilt maken.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="a4c2f-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a4c2f-116">Selecteer de artikeltoewijzingssleutel D_Aloc.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="a4c2f-117">Klik op >.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-117">Click >.</span></span>
7. <span data-ttu-id="a4c2f-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-118">Close the page.</span></span>
8. <span data-ttu-id="a4c2f-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="a4c2f-120">De parameters voor vraagprognose instellen</span><span class="sxs-lookup"><span data-stu-id="a4c2f-120">Set up the demand forecasting parameters</span></span>
1. <span data-ttu-id="a4c2f-121">Ga naar Hoofdplanning > Instellingen > Vraagprognose > Parameters voor vraagprognose.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="a4c2f-122">Vouw de sectie Parameters van prognosealgoritme uit.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="a4c2f-123">Selecteer in het veld Strategie voor aanmaken van vraagprognose de optie Kopieer over historische vraag.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="a4c2f-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="a4c2f-125">Een basislijnprognose maken</span><span class="sxs-lookup"><span data-stu-id="a4c2f-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="a4c2f-126">Ga naar Hoofdplanning > Prognose > Vraagprognose > Statistische basislijnprognose maken.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="a4c2f-127">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="a4c2f-128">Als u verkooporders hebt die vanaf 1 januari 2015 beginnen, voert u deze datum in.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="a4c2f-129">Als dat niet zo is, voert u de vroegste datum van uw verkooporders in.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="a4c2f-130">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="a4c2f-131">Voer de laatste datum van uw verkooporders in, bijvoorbeeld 31-03-2015.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="a4c2f-132">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="a4c2f-133">Voer '01-04-2015' in.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="a4c2f-134">Deze datum wordt automatisch berekend als begindatum van de volgende prognoseverzameling.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="a4c2f-135">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="a4c2f-136">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-136">Click Filter.</span></span>
7. <span data-ttu-id="a4c2f-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a4c2f-138">Markeer de rij waarbj Veld = intercompany-planningsgroep.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="a4c2f-139">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="a4c2f-140">Typ de intercompany-planningsgroep, bijvoorbeeld 10, die u in de eerste taak hebt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="a4c2f-141">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a4c2f-142">Selecteer de rij waarbij Veld = Artikeltoewijzingssleutel.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="a4c2f-143">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="a4c2f-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-144">Click OK.</span></span>
12. <span data-ttu-id="a4c2f-145">Vouw de sectie Geavanceerde parameters uit.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="a4c2f-146">Selecteer Maand in het veld Prognoseverzameling.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="a4c2f-147">Voer "3" in het veld Prognoseperiode in.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="a4c2f-148">Voer 1 in het veld Blokkering van de tijdlimiet in.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="a4c2f-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="a4c2f-150">De vraagprognose visualiseren</span><span class="sxs-lookup"><span data-stu-id="a4c2f-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="a4c2f-151">Ga naar Hoofdplanning > Prognose > Vraagprognose > Gecorrigeerde vraagprognose.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="a4c2f-152">Selecteer in de tabel met de samengestelde weergave de cel in rij 1, kolom 2.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="a4c2f-153">Dit is de tweede maand waarvoor u een prognose hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="a4c2f-154">Stel QtyCell in op "400".</span><span class="sxs-lookup"><span data-stu-id="a4c2f-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="a4c2f-155">Voer in de cel een afwijkend aantal in dan was geraamd, bijvoorbeeld 400.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="a4c2f-156">U hebt een handmatige correctie van de prognose uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="a4c2f-157">Zie de grafische indicatie in de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="a4c2f-158">Klik op Regeldetails voor prognose.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="a4c2f-159">Op deze pagina kunt u de nauwkeurigheidswaarden, de historische vraag en de prognose weergeven.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="a4c2f-160">U kunt ook wijzigingen aanbrengen in de prognose.</span><span class="sxs-lookup"><span data-stu-id="a4c2f-160">You can make changes to the forecast as well.</span></span>  

