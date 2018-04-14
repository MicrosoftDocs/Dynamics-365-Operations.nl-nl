--- 
title: Een basislijnprognose maken
description: "Een productieplanner kan een basislijnprognose maken of door prognosemodellen voor de tijdreeks te gebruiken of door de historische vraag naar de prognose te kopiëren."
author: YuyuScheller
manager: AnnBe
ms.date: 111/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ef11f3779fc94fa95f082893f6863dde8d8c921e
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="219bb-103">Een basislijnprognose maken</span><span class="sxs-lookup"><span data-stu-id="219bb-103">Create a baseline forecast</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="219bb-104">Een productieplanner kan een basislijnprognose maken of door prognosemodellen voor de tijdreeks te gebruiken of door de historische vraag naar de prognose te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="219bb-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="219bb-105">Deze procedure laat zien hoe u de historische vraag kopieert om een basislijnprognose te maken voor alle producten met één artikeltoewijzingssleutel.</span><span class="sxs-lookup"><span data-stu-id="219bb-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="219bb-106">Een artikeltoewijzingssleutel instellen</span><span class="sxs-lookup"><span data-stu-id="219bb-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="219bb-107">Ga naar Hoofdplanning > Instellingen > Intercompany-planningsgroepen.</span><span class="sxs-lookup"><span data-stu-id="219bb-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="219bb-108">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="219bb-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="219bb-109">Filter bijvoorbeeld op het Veld Naam met een waarde van "10".</span><span class="sxs-lookup"><span data-stu-id="219bb-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="219bb-110">Vraagprognose uitvoeren voor verschillende rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="219bb-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="219bb-111">Daarom moet u alle bedrijven instellen waarvoor u prognoses wilt genereren in één intercompany-planningsgroep.</span><span class="sxs-lookup"><span data-stu-id="219bb-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="219bb-112">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="219bb-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="219bb-113">Klik op Artikeltoewijzingssleutels.</span><span class="sxs-lookup"><span data-stu-id="219bb-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="219bb-114">Selecteer alle artikeltoewijzingssleutels waarvoor u prognoses wilt maken.</span><span class="sxs-lookup"><span data-stu-id="219bb-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="219bb-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="219bb-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="219bb-116">Selecteer de artikeltoewijzingssleutel D_Aloc.</span><span class="sxs-lookup"><span data-stu-id="219bb-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="219bb-117">Klik op >.</span><span class="sxs-lookup"><span data-stu-id="219bb-117">Click >.</span></span>
7. <span data-ttu-id="219bb-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="219bb-118">Close the page.</span></span>
8. <span data-ttu-id="219bb-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="219bb-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="219bb-120">De parameters voor vraagprognose instellen</span><span class="sxs-lookup"><span data-stu-id="219bb-120">Set up the demand forecasting parameters</span></span>
1. <span data-ttu-id="219bb-121">Ga naar Hoofdplanning > Instellingen > Vraagprognose > Parameters voor vraagprognose.</span><span class="sxs-lookup"><span data-stu-id="219bb-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="219bb-122">Vouw de sectie Parameters van prognosealgoritme uit.</span><span class="sxs-lookup"><span data-stu-id="219bb-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="219bb-123">Selecteer in het veld Strategie voor aanmaken van vraagprognose de optie Kopieer over historische vraag.</span><span class="sxs-lookup"><span data-stu-id="219bb-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="219bb-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="219bb-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="219bb-125">Een basislijnprognose maken</span><span class="sxs-lookup"><span data-stu-id="219bb-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="219bb-126">Ga naar Hoofdplanning > Prognose > Vraagprognose > Statistische basislijnprognose maken.</span><span class="sxs-lookup"><span data-stu-id="219bb-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="219bb-127">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="219bb-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="219bb-128">Als u verkooporders hebt die vanaf 1 januari 2015 beginnen, voert u deze datum in.</span><span class="sxs-lookup"><span data-stu-id="219bb-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="219bb-129">Als dat niet zo is, voert u de vroegste datum van uw verkooporders in.</span><span class="sxs-lookup"><span data-stu-id="219bb-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="219bb-130">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="219bb-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="219bb-131">Voer de laatste datum van uw verkooporders in, bijvoorbeeld 31-03-2015.</span><span class="sxs-lookup"><span data-stu-id="219bb-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="219bb-132">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="219bb-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="219bb-133">Voer '01-04-2015' in.</span><span class="sxs-lookup"><span data-stu-id="219bb-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="219bb-134">Deze datum wordt automatisch berekend als begindatum van de volgende prognoseverzameling.</span><span class="sxs-lookup"><span data-stu-id="219bb-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="219bb-135">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="219bb-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="219bb-136">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="219bb-136">Click Filter.</span></span>
7. <span data-ttu-id="219bb-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="219bb-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="219bb-138">Markeer de rij waarbj Veld = intercompany-planningsgroep.</span><span class="sxs-lookup"><span data-stu-id="219bb-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="219bb-139">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="219bb-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="219bb-140">Typ de intercompany-planningsgroep, bijvoorbeeld 10, die u in de eerste taak hebt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="219bb-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="219bb-141">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="219bb-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="219bb-142">Selecteer de rij waarbij Veld = Artikeltoewijzingssleutel.</span><span class="sxs-lookup"><span data-stu-id="219bb-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="219bb-143">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="219bb-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="219bb-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="219bb-144">Click OK.</span></span>
12. <span data-ttu-id="219bb-145">Vouw de sectie Geavanceerde parameters uit.</span><span class="sxs-lookup"><span data-stu-id="219bb-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="219bb-146">Selecteer Maand in het veld Prognoseverzameling.</span><span class="sxs-lookup"><span data-stu-id="219bb-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="219bb-147">Voer "3" in het veld Prognoseperiode in.</span><span class="sxs-lookup"><span data-stu-id="219bb-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="219bb-148">Voer 1 in het veld Blokkering van de tijdlimiet in.</span><span class="sxs-lookup"><span data-stu-id="219bb-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="219bb-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="219bb-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="219bb-150">De vraagprognose visualiseren</span><span class="sxs-lookup"><span data-stu-id="219bb-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="219bb-151">Ga naar Hoofdplanning > Prognose > Vraagprognose > Gecorrigeerde vraagprognose.</span><span class="sxs-lookup"><span data-stu-id="219bb-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="219bb-152">Selecteer in de tabel met de samengestelde weergave de cel in rij 1, kolom 2.</span><span class="sxs-lookup"><span data-stu-id="219bb-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="219bb-153">Dit is de tweede maand waarvoor u een prognose hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="219bb-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="219bb-154">Stel QtyCell in op "400".</span><span class="sxs-lookup"><span data-stu-id="219bb-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="219bb-155">Voer in de cel een afwijkend aantal in dan was geraamd, bijvoorbeeld 400.</span><span class="sxs-lookup"><span data-stu-id="219bb-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="219bb-156">U hebt een handmatige correctie van de prognose uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="219bb-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="219bb-157">Zie de grafische indicatie in de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="219bb-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="219bb-158">Klik op Regeldetails voor prognose.</span><span class="sxs-lookup"><span data-stu-id="219bb-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="219bb-159">Op deze pagina kunt u de nauwkeurigheidswaarden, de historische vraag en de prognose zien.</span><span class="sxs-lookup"><span data-stu-id="219bb-159">On this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="219bb-160">U kunt ook wijzigingen aanbrengen in de prognose.</span><span class="sxs-lookup"><span data-stu-id="219bb-160">You can make changes to the forecast as well.</span></span>  


