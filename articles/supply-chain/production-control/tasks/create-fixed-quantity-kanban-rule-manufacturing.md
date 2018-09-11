--- 
title: Een kanbanregel met vaste hoeveelheid maken voor productie
description: Deze procedure is gericht op de instellingen die nodig is om een vaste kanbanregel voor fabricage te maken om de omzetting van activiteiten, in een werkcel, in lean omgeving te activeren.
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c21373c27f7cc1590790b297e98bc36d94386797
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="2d708-103">Een kanbanregel met vaste hoeveelheid maken voor productie</span><span class="sxs-lookup"><span data-stu-id="2d708-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d708-104">Deze procedure is gericht op de instellingen die nodig is om een vaste kanbanregel voor fabricage te maken om de omzetting van activiteiten, in een werkcel, in lean omgeving te activeren.</span><span class="sxs-lookup"><span data-stu-id="2d708-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="2d708-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="2d708-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2d708-106">Deze procedure is bedoeld voor de Procesingenieur of de Waardestroombeheerder, want zij bereiden de productie van een nieuw of gewijzigd product voor.</span><span class="sxs-lookup"><span data-stu-id="2d708-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="2d708-107">Nieuwe kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="2d708-107">Create new kanban rule</span></span>
1. <span data-ttu-id="2d708-108">Ga naar Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="2d708-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="2d708-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2d708-109">Click New.</span></span>
    * <span data-ttu-id="2d708-110">Het standaardtype is Productie en de Aanvullingsstrategie is Vast.</span><span class="sxs-lookup"><span data-stu-id="2d708-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="2d708-111">U moet deze parameters niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="2d708-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="2d708-112">Typ of selecteer een waarde in het veld Eerste planactiviteit.</span><span class="sxs-lookup"><span data-stu-id="2d708-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="2d708-113">Dit is de activiteit die wordt uitgevoerd voor kanbans die op basis van deze kanbanregel zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2d708-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="2d708-114">Selecteer 'SpeakerTestAndPackaging'.</span><span class="sxs-lookup"><span data-stu-id="2d708-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="2d708-115">Vouw de sectie Details uit.</span><span class="sxs-lookup"><span data-stu-id="2d708-115">Expand the Details section.</span></span>
5. <span data-ttu-id="2d708-116">Typ of selecteer een waarde in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="2d708-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="2d708-117">Selecteer L0050.</span><span class="sxs-lookup"><span data-stu-id="2d708-117">Select L0050.</span></span>  
6. <span data-ttu-id="2d708-118">Typ of selecteer een waarde in het veld Maateenheid.</span><span class="sxs-lookup"><span data-stu-id="2d708-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="2d708-119">Selecteer minuten.</span><span class="sxs-lookup"><span data-stu-id="2d708-119">Select minutes.</span></span>  
7. <span data-ttu-id="2d708-120">Voer in het veld Levertijd een nummer in.</span><span class="sxs-lookup"><span data-stu-id="2d708-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="2d708-121">Voer 5 in.</span><span class="sxs-lookup"><span data-stu-id="2d708-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="2d708-122">Hoeveelheden instellen</span><span class="sxs-lookup"><span data-stu-id="2d708-122">Set quantities</span></span>
1. <span data-ttu-id="2d708-123">Vouw de sectie Hoeveelheden uit.</span><span class="sxs-lookup"><span data-stu-id="2d708-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="2d708-124">Stel Standaardhoeveelheid in op '10'.</span><span class="sxs-lookup"><span data-stu-id="2d708-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="2d708-125">Dit is de hoeveelheid die voor elke kanban wordt overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="2d708-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="2d708-126">Schakel het selectievakje Afwijking producthoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="2d708-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="2d708-127">Hiermee kunnen de geselecteerde kanbans worden voltooid met een afwijking van de standaardhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="2d708-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="2d708-128">Om toe te staan dat kanbans worden voltooid met een hoeveelheid van 8 tot 12, stelt u beide afwijkingen in op 2.</span><span class="sxs-lookup"><span data-stu-id="2d708-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="2d708-129">Stel Afwijking onder in op '2'.</span><span class="sxs-lookup"><span data-stu-id="2d708-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="2d708-130">Hierdoor is het mogelijk om minimaal 10 - 2 = 8 te voltooien</span><span class="sxs-lookup"><span data-stu-id="2d708-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="2d708-131">Stel Afwijking boven in op '2'.</span><span class="sxs-lookup"><span data-stu-id="2d708-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="2d708-132">Hierdoor is het mogelijk om maximaal 10 + 2 = 12 te voltooien</span><span class="sxs-lookup"><span data-stu-id="2d708-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="2d708-133">Typ een getal in het veld Vaste kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="2d708-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="2d708-134">Dit is het aantal kanbans die actief moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="2d708-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="2d708-135">In dit geval verwerken 5 kanbans elk 10.</span><span class="sxs-lookup"><span data-stu-id="2d708-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="2d708-136">Typ '2' in het veld Minimum waarschuwingsgrens.</span><span class="sxs-lookup"><span data-stu-id="2d708-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="2d708-137">Gebruikt om het minimumaantal van volledige kanbans bij te houden die bij de bestemming moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="2d708-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="2d708-138">Dit wordt bijvoorbeeld gebruikt op het overzicht van kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="2d708-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="2d708-139">Typ '4' in het veld Maximum waarschuwingsgrens.</span><span class="sxs-lookup"><span data-stu-id="2d708-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="2d708-140">Gebruikt om het maximumaantal van volledige kanbans bij te houden die bij de bestemming moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="2d708-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="2d708-141">Dit wordt bijvoorbeeld gebruikt op het overzicht van kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="2d708-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="2d708-142">Typ '1' in het veld Automatische planningshoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="2d708-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="2d708-143">Als u dit op 1 instelt, wordt elke kanban automatisch ingepland.</span><span class="sxs-lookup"><span data-stu-id="2d708-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="2d708-144">Als u 3 invoert, worden de kanbans niet gepland tot er 3 lege kanbans klaar zijn voor planning.</span><span class="sxs-lookup"><span data-stu-id="2d708-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="2d708-145">Dit is nuttig voor het groeperen van het werk en het voorkomen van te veel instellingen.</span><span class="sxs-lookup"><span data-stu-id="2d708-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="2d708-146">Kanbans maken</span><span class="sxs-lookup"><span data-stu-id="2d708-146">Create Kanbans</span></span>
1. <span data-ttu-id="2d708-147">Vouw de sectie Kanbans uit.</span><span class="sxs-lookup"><span data-stu-id="2d708-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="2d708-148">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="2d708-148">Click Save.</span></span>
    * <span data-ttu-id="2d708-149">De kanbanregel moet worden opgeslagen voordat kanbans kunnen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2d708-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="2d708-150">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2d708-150">Click Add.</span></span>
    * <span data-ttu-id="2d708-151">Houd er rekening mee dat er geen actieve kanbans zijn. Als gevolg hiervan is het voorgestelde 'Aantal nieuwe kanbans' 5.</span><span class="sxs-lookup"><span data-stu-id="2d708-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="2d708-152">Dit is gelijk aan de Vaste kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="2d708-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="2d708-153">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="2d708-153">Click Create.</span></span>
    * <span data-ttu-id="2d708-154">Hierdoor worden 5 kanbans gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2d708-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="2d708-155">Voor deze kanbanregel zijn werden er 5 kanbans gemaakt, voor elk 10.</span><span class="sxs-lookup"><span data-stu-id="2d708-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="2d708-156">Dit is de laatste stap in deze procedure.</span><span class="sxs-lookup"><span data-stu-id="2d708-156">This is the last step in this procedure.</span></span>  


