--- 
title: Een opnamekanbanregel maken
description: Deze procedure toont de instellingen die nodig zijn om een kanbanregel voor opname te maken om materiaal in een lean-omgeving over te boeken.
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
ms.openlocfilehash: b0c1f0f4ea3035ffb7c5a12c83c12a132cc65fd5
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="02c62-103">Een opnamekanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="02c62-103">Create a withdrawal kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02c62-104">Deze procedure toont de instellingen die nodig zijn om een kanbanregel voor opname te maken om materiaal in een lean-omgeving over te boeken.</span><span class="sxs-lookup"><span data-stu-id="02c62-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="02c62-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="02c62-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="02c62-106">Deze procedure is bedoeld voor de Procesingenieur of de Waardestroombeheerder, want zij bereiden de aanvulling van nieuw of gewijzigd materiaal voor.</span><span class="sxs-lookup"><span data-stu-id="02c62-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="02c62-107">Nieuwe kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="02c62-107">Create new kanban rule</span></span>
1. <span data-ttu-id="02c62-108">Ga naar Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="02c62-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="02c62-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="02c62-109">Click New.</span></span>
3. <span data-ttu-id="02c62-110">Selecteer Opname in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="02c62-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="02c62-111">Het opnametype wordt gebruikt voor kanbanregels om materiaal of goederen over te boeken.</span><span class="sxs-lookup"><span data-stu-id="02c62-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="02c62-112">Typ of selecteer een waarde in het veld Eerste planactiviteit.</span><span class="sxs-lookup"><span data-stu-id="02c62-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="02c62-113">Selecteer ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="02c62-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="02c62-114">Deze activiteit wordt ingesteld om onderdelen van magazijn 11, locatie 11 naar magazijn 12 en locatie 12 te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="02c62-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="02c62-115">Typ of selecteer een waarde in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="02c62-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="02c62-116">Selecteer M0007.</span><span class="sxs-lookup"><span data-stu-id="02c62-116">Select M0007.</span></span>  
6. <span data-ttu-id="02c62-117">Voer in het veld Levertijd een nummer in.</span><span class="sxs-lookup"><span data-stu-id="02c62-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="02c62-118">Bijvoorbeeld 60.</span><span class="sxs-lookup"><span data-stu-id="02c62-118">For example, 60.</span></span>  
7. <span data-ttu-id="02c62-119">Typ of selecteer een waarde in het veld Maateenheid.</span><span class="sxs-lookup"><span data-stu-id="02c62-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="02c62-120">Bijvoorbeeld Minuten.</span><span class="sxs-lookup"><span data-stu-id="02c62-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="02c62-121">Hoeveelheden voor kanban instellen</span><span class="sxs-lookup"><span data-stu-id="02c62-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="02c62-122">Stel Standaardhoeveelheid in op '5'.</span><span class="sxs-lookup"><span data-stu-id="02c62-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="02c62-123">Dit is de hoeveelheid die voor elke kanban wordt overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="02c62-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="02c62-124">Voer 2 in het veld Vaste kanbanhoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="02c62-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="02c62-125">Dit is het aantal kanbans die actief moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="02c62-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="02c62-126">In dit geval 2 kanbans die elk 5 overboeken.</span><span class="sxs-lookup"><span data-stu-id="02c62-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="02c62-127">Typ '1' in het veld Minimum waarschuwingsgrens.</span><span class="sxs-lookup"><span data-stu-id="02c62-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="02c62-128">Gebruikt om het minimumaantal van volledige kanbans bij te houden die bij de bestemming moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="02c62-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="02c62-129">Dit wordt bijvoorbeeld gebruikt op het overzicht van kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="02c62-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="02c62-130">Typ '2' in het veld Maximum waarschuwingsgrens.</span><span class="sxs-lookup"><span data-stu-id="02c62-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="02c62-131">Gebruikt om het maximumaantal van volledige kanbans bij te houden die bij de bestemming moeten zijn.</span><span class="sxs-lookup"><span data-stu-id="02c62-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="02c62-132">Dit wordt bijvoorbeeld gebruikt op het overzicht van kanbanhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="02c62-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="02c62-133">Kanbans maken</span><span class="sxs-lookup"><span data-stu-id="02c62-133">Create kanbans</span></span>
1. <span data-ttu-id="02c62-134">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="02c62-134">Click Save.</span></span>
    * <span data-ttu-id="02c62-135">De kanbanregel moet worden opgeslagen voordat kanbans kunnen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="02c62-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="02c62-136">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="02c62-136">Click Add.</span></span>
    * <span data-ttu-id="02c62-137">Er zijn geen actieve kanbans, omdat het voorgestelde 'Aantal nieuwe kanbans' 2 is. Dit is gelijk aan de 'Vaste kanbanhoeveelheid'.</span><span class="sxs-lookup"><span data-stu-id="02c62-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="02c62-138">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="02c62-138">Click Create.</span></span>
    * <span data-ttu-id="02c62-139">Hierdoor worden twee kanbans gemaakt.</span><span class="sxs-lookup"><span data-stu-id="02c62-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="02c62-140">Voor deze opnamekanbanregel werden er 2 kanbans gemaakt, voor elk 5.</span><span class="sxs-lookup"><span data-stu-id="02c62-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="02c62-141">Dit is de laatste stap in deze procedure.</span><span class="sxs-lookup"><span data-stu-id="02c62-141">This is the last step in this procedure.</span></span>  


