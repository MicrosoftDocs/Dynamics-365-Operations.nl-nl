---
title: Een kanbanregel maken met een kanbanregelgebeurtenis
description: Met deze procedure wordt een kanbanregel gemaakt door de instelling voor kanbanregelgebeurtenissen te gebruiken om pull van een procesactiviteit te activeren.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bff5f16c1911739a29d50c546c3c2a9ab85c2371
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "350223"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="f3e57-103">Een kanbanregel maken met een kanbanregelgebeurtenis</span><span class="sxs-lookup"><span data-stu-id="f3e57-103">Create a kanban rule using a kanban line event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3e57-104">Met deze procedure wordt een kanbanregel gemaakt door de instelling voor kanbanregelgebeurtenissen te gebruiken om pull van een procesactiviteit te activeren.</span><span class="sxs-lookup"><span data-stu-id="f3e57-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="f3e57-105">De kanbanregel wordt geactiveerd door een activiteit van het kanbanproces, met een hoeveelheid die gelijk is aan of hoger is dan 25 elk.</span><span class="sxs-lookup"><span data-stu-id="f3e57-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="f3e57-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f3e57-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f3e57-107">Deze taak is bedoeld voor de procestechnicus of de waardestroombeheerder bij het voorbereiden van de productie van een nieuw of gewijzigd product in een lean-omgeving.</span><span class="sxs-lookup"><span data-stu-id="f3e57-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="f3e57-108">Een kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="f3e57-108">Create a kanban rule</span></span>
1. <span data-ttu-id="f3e57-109">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="f3e57-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="f3e57-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f3e57-110">Click New.</span></span>
3. <span data-ttu-id="f3e57-111">Selecteer 'Gebeurtenis' in het veld Aanvullingsstrategie.</span><span class="sxs-lookup"><span data-stu-id="f3e57-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="f3e57-112">Hiermee worden rechtstreeks vanuit de vraag kanbans gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f3e57-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="f3e57-113">Hiermee worden regels ingesteld voor het definiëren van een maken op bestelling-scenario.</span><span class="sxs-lookup"><span data-stu-id="f3e57-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="f3e57-114">Typ of selecteer een waarde in het veld Eerste planactiviteit.</span><span class="sxs-lookup"><span data-stu-id="f3e57-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="f3e57-115">Typ of selecteer SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="f3e57-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="f3e57-116">De eerste activiteit van een kanbanregel voor productie is een verwerkingsactiviteit in de productiestroom.</span><span class="sxs-lookup"><span data-stu-id="f3e57-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="f3e57-117">Wanneer u de activiteit selecteert, worden de geldigheidsdatums van de activiteit gekopieerd naar de geldigheidsdatums van de kanbanregel.</span><span class="sxs-lookup"><span data-stu-id="f3e57-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="f3e57-118">Vouw de sectie Details uit.</span><span class="sxs-lookup"><span data-stu-id="f3e57-118">Expand the Details section.</span></span>
6. <span data-ttu-id="f3e57-119">Typ 'L0001' in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="f3e57-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="f3e57-120">Vouw de sectie Gebeurtenissen uit.</span><span class="sxs-lookup"><span data-stu-id="f3e57-120">Expand the Events section.</span></span>
8. <span data-ttu-id="f3e57-121">Selecteer 'Automatisch' in het veld Kanbanregelgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="f3e57-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="f3e57-122">Hiermee worden gebeurteniskanbans op aanvraag gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="f3e57-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="f3e57-123">Dit veldt wordt gebruikt voor het configureren van kanbanregels die materiaal aanvullen dat nodig is voor een downstream procesactiviteit.</span><span class="sxs-lookup"><span data-stu-id="f3e57-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="f3e57-124">Wanneer u Automatisch selecteert, worden de gebeurteniskanbans gemaakt bij de aanvraag.</span><span class="sxs-lookup"><span data-stu-id="f3e57-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="f3e57-125">Deze instelling wordt aangeraden als u verwacht op dezelfde dag productie te zullen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="f3e57-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="f3e57-126">Stel Minimale gebeurtenishoeveelheid in op '25'.</span><span class="sxs-lookup"><span data-stu-id="f3e57-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="f3e57-127">Gebeurteniskanbans worden gegenereerd wanneer de vraaghoeveelheid gelijk is aan of groter is dan dit veld.</span><span class="sxs-lookup"><span data-stu-id="f3e57-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="f3e57-128">Dit is handig als u een bestelhoeveelheid wilt produceren die kleiner is dan dit veld op de ene machine en meer dan dit veld op een andere machine.</span><span class="sxs-lookup"><span data-stu-id="f3e57-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="f3e57-129">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f3e57-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="f3e57-130">Verkooporder maken en kanbanketen activeren</span><span class="sxs-lookup"><span data-stu-id="f3e57-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="f3e57-131">Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="f3e57-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="f3e57-132">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f3e57-132">Click New.</span></span>
3. <span data-ttu-id="f3e57-133">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="f3e57-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="f3e57-134">Selecteer klantrekening US-003, Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="f3e57-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="f3e57-135">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3e57-135">Click OK.</span></span>
5. <span data-ttu-id="f3e57-136">Typ in het veld Artikelnummer de waarde 'L0001'.</span><span class="sxs-lookup"><span data-stu-id="f3e57-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="f3e57-137">L0001 is het artikel waarvoor u de kanbanregel hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f3e57-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="f3e57-138">Stel Hoeveelheid in op '27'.</span><span class="sxs-lookup"><span data-stu-id="f3e57-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="f3e57-139">Omdat 27 hoger is dan de minimumhoeveelheid van 25 op de kanbanregel, wordt hiermee een gebeurteniskanban geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="f3e57-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="f3e57-140">Typ '1' in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="f3e57-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="f3e57-141">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="f3e57-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f3e57-142">Selecteer magazijn 13.</span><span class="sxs-lookup"><span data-stu-id="f3e57-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="f3e57-143">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f3e57-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="f3e57-144">De kanban weergeven die door de kanbanregel wordt gegenereerd</span><span class="sxs-lookup"><span data-stu-id="f3e57-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="f3e57-145">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="f3e57-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="f3e57-146">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f3e57-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f3e57-147">Vouw de sectie Kanbans uit.</span><span class="sxs-lookup"><span data-stu-id="f3e57-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="f3e57-148">Merk op dat een kanban voor 27 is gemaakt om de activiteit te verwerken die is gebaseerd op de gemaakte kanbanregel.</span><span class="sxs-lookup"><span data-stu-id="f3e57-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="f3e57-149">Dit is de laatste stap.</span><span class="sxs-lookup"><span data-stu-id="f3e57-149">This is the last step.</span></span>  

