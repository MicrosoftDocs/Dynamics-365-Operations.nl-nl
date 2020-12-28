---
title: 'Cyclustelling definiëren '
description: Cyclustelling is een magazijnproces dat u kunt gebruiken om voorhanden voorraadartikelen te controleren.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8b7f39fc9a91d9fe219445e409d000266e24775
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425802"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="33c5c-103">Cyclustelling definiëren </span><span class="sxs-lookup"><span data-stu-id="33c5c-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33c5c-104">Cyclustelling is een magazijnproces dat u kunt gebruiken om voorhanden voorraadartikelen te controleren.</span><span class="sxs-lookup"><span data-stu-id="33c5c-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="33c5c-105">Deze taakregistratie laat zien hoe u: de standaardprioriteit van telwerk instelt; een menuoptie voor mobiele apparaten inschakelt om zowel verzamel- als telbewerkingen te verwerken; een teldrempeltrigger inschakelt wanneer een locatie leeg raakt; een cyclustelplan inschakelt voor een specifiek artikel in een specifiek magazijn.</span><span class="sxs-lookup"><span data-stu-id="33c5c-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="33c5c-106">Deze taken worden gewoonlijk uitgevoerd door een magazijnmanager.</span><span class="sxs-lookup"><span data-stu-id="33c5c-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="33c5c-107">U kunt deze procedure doorlopen in het demobedrijf USMF of in uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="33c5c-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="33c5c-108">De prioriteit van telwerk instellen</span><span class="sxs-lookup"><span data-stu-id="33c5c-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="33c5c-109">Ga in het **navigatievenster** naar **Modules > Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="33c5c-110">Klik op het tabblad **Cyclustelling**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="33c5c-111">Voer een getal in het veld **Standaard werkprioriteit van cyclustelling** in.</span><span class="sxs-lookup"><span data-stu-id="33c5c-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="33c5c-112">Deze stap wijzigt de prioriteit van cyclustelwerk vergeleken met andere soorten werk in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="33c5c-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="33c5c-113">Als u een nummer invoert dat lager is dan het nummer voor andere typen werk, verhoogt u de prioriteit van het cyclustelwerk.</span><span class="sxs-lookup"><span data-stu-id="33c5c-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="33c5c-114">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-114">Click **Save**.</span></span>
5. <span data-ttu-id="33c5c-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33c5c-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="33c5c-116">Het mobiel apparaat inschakelen</span><span class="sxs-lookup"><span data-stu-id="33c5c-116">Enable the mobile device</span></span>
1. <span data-ttu-id="33c5c-117">Ga in het **navigatievenster** naar **Modules > Magazijnbeheer > Instellingen > Mobiel apparaat > Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="33c5c-118">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-118">Click **New**.</span></span>
3. <span data-ttu-id="33c5c-119">Typ een waarde in het veld **Menuoptie**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="33c5c-120">Typ een waarde in het veld **Titel**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="33c5c-121">Selecteer Werk in het veld **Modus**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="33c5c-122">Stel de optie **Bestaand werk gebruiken** in op Ja.</span><span class="sxs-lookup"><span data-stu-id="33c5c-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="33c5c-123">Wanneer u deze optie instelt op Ja, zoekt het systeem naar bestaand werk wanneer de menuoptie van het mobiele apparaat wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="33c5c-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="33c5c-124">Selecteer Door systeem bestuurd in het veld **Bestuurd door**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="33c5c-125">Wanneer 'Door systeem bestuurd' is ingeschakeld, wordt de magazijnmedewerker doorgestuurd naar open werk in de gedefinieerde werkklassen.</span><span class="sxs-lookup"><span data-stu-id="33c5c-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="33c5c-126">(We maken deze klassen vervolgens.)</span><span class="sxs-lookup"><span data-stu-id="33c5c-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="33c5c-127">Vouw het sneltabblad **Werkklassen** uit.</span><span class="sxs-lookup"><span data-stu-id="33c5c-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="33c5c-128">Vervolgens maken we twee werkklassen die worden gebruikt met deze menuoptie voor een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="33c5c-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="33c5c-129">Wanneer de menuoptie wordt gebruikt, worden query's op deze werkklassen uitgevoerd en wordt het werk met de hoogste prioriteit aan de gebruiker weergegeven.</span><span class="sxs-lookup"><span data-stu-id="33c5c-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="33c5c-130">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-130">Click **New**.</span></span>
10. <span data-ttu-id="33c5c-131">Selecteer een waarde in het veld **Werkklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="33c5c-132">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-132">Click **New**.</span></span>
12. <span data-ttu-id="33c5c-133">Selecteer een waarde in het veld **Werkklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="33c5c-134">Klik in het **actievenster** op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="33c5c-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33c5c-135">Close the page.</span></span>
15. <span data-ttu-id="33c5c-136">Ga in het **navigatievenster** naar **Modules > Magazijnbeheer > Instellingen > Mobiel apparaat > Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="33c5c-137">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="33c5c-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="33c5c-138">Selecteer in de structuur 'de menuoptie die u zojuist hebt gemaakt'.</span><span class="sxs-lookup"><span data-stu-id="33c5c-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="33c5c-139">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-139">Click **Edit**.</span></span>
19. <span data-ttu-id="33c5c-140">Klik op de pijl om de menuoptie aan het menu toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="33c5c-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="33c5c-141">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="33c5c-142">Een teldrempel maken</span><span class="sxs-lookup"><span data-stu-id="33c5c-142">Create a counting threshold</span></span>
1. <span data-ttu-id="33c5c-143">Ga in het **navigatievenster** naar **Modules > Magazijnbeheer > Instellingen > Cyclustelling > Drempels voor cyclustelling**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="33c5c-144">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-144">Click **New**.</span></span>
3. <span data-ttu-id="33c5c-145">Typ een waarde in het veld **Id cyclustellingsdrempel**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="33c5c-146">Stel de optie **Cyclustellingsplan onmiddellijk verwerken** in op Ja.</span><span class="sxs-lookup"><span data-stu-id="33c5c-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="33c5c-147">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="33c5c-148">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-148">Click **Save**.</span></span>
7. <span data-ttu-id="33c5c-149">Klik op **Locaties selecteren**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="33c5c-150">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="33c5c-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="33c5c-151">Selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="33c5c-152">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-152">Click **OK**.</span></span>
11. <span data-ttu-id="33c5c-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33c5c-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="33c5c-154">Een cyclustelplan maken</span><span class="sxs-lookup"><span data-stu-id="33c5c-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="33c5c-155">Ga in het **navigatievenster** naar **Modules > Magazijnbeheer > Instellingen > Cyclustelling > Cyclustelplannen**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="33c5c-156">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-156">Click **New**.</span></span>
3. <span data-ttu-id="33c5c-157">Typ een waarde in het veld **Id cyclustelplan**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="33c5c-158">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="33c5c-159">Voer een getal in het veld **Maximumaantal cyclustellingen** in.</span><span class="sxs-lookup"><span data-stu-id="33c5c-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="33c5c-160">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-160">Click **Save**.</span></span>
7. <span data-ttu-id="33c5c-161">Klik op **Locaties selecteren**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="33c5c-162">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="33c5c-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="33c5c-163">Selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="33c5c-164">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-164">Click **OK**.</span></span>
11. <span data-ttu-id="33c5c-165">Voer een getal in het veld **Dagen tussen cyclustellingen** in.</span><span class="sxs-lookup"><span data-stu-id="33c5c-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="33c5c-166">Als de waarde in het veld **Dagen tussen cyclustellingen** bijvoorbeeld 5 is, wordt om de vijf dagen cyclustellingswerk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="33c5c-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="33c5c-167">Als cyclustellingswerk echter op dag drie wordt verwerkt, wordt het volgende cyclustellingswerk gecreëerd vijf dagen nadat de laatste cyclustelling werd verwerkt, op dag acht.</span><span class="sxs-lookup"><span data-stu-id="33c5c-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="33c5c-168">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-168">Click **Save**.</span></span>
13. <span data-ttu-id="33c5c-169">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-169">Click **New**.</span></span>
14. <span data-ttu-id="33c5c-170">Typ een getal in het veld **Volgnummer**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="33c5c-171">De sorteervolgorde is van het kleinste getal naar het grootste getal.</span><span class="sxs-lookup"><span data-stu-id="33c5c-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="33c5c-172">De waarde moet groter zijn dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="33c5c-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="33c5c-173">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="33c5c-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="33c5c-174">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="33c5c-175">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-175">Click **Save**.</span></span>
18. <span data-ttu-id="33c5c-176">Klik op **Productquery definiëren**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="33c5c-177">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="33c5c-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="33c5c-178">Typ of selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="33c5c-179">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="33c5c-179">Click **OK**.</span></span>
22. <span data-ttu-id="33c5c-180">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33c5c-180">Close the page.</span></span>

