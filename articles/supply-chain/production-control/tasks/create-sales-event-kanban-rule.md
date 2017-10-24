--- 
title: Een kanbanregel voor verkoopgebeurtenis maken
description: Deze procedure is gericht op de instellingen die nodig is voor het maken van een kanbanregel die tijdens het maken van een verkooporder wordt geactiveerd.
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f1f66157b2e74ad1b490e10112cbc121ac9826fb
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="f2ae2-103">Een kanbanregel voor verkoopgebeurtenis maken</span><span class="sxs-lookup"><span data-stu-id="f2ae2-103">Create a sales event kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2ae2-104">Deze procedure is gericht op de instellingen die nodig is voor het maken van een kanbanregel die tijdens het maken van een verkooporder wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="f2ae2-105">De gebeurteniskanbanregel vult de vereisten aan die afkomstig zijn uit van verkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="f2ae2-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f2ae2-107">Deze procedure is bedoeld voor de procesingenieur of de waardestroombeheerder, want zij bereiden de productie van een nieuw of gewijzigd product voor.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="f2ae2-108">Een nieuwe kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="f2ae2-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="f2ae2-109">Ga naar Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="f2ae2-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-110">Click New.</span></span>
3. <span data-ttu-id="f2ae2-111">Selecteer 'Gebeurtenis' in het veld Aanvullingsstrategie.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="f2ae2-112">Door het selecteren van Gebeurtenis wordt de kanbanregel geactiveerd door een gebeurtenis, bijvoorbeeld, het maken van een verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="f2ae2-113">Dit wordt toegepast op gebieden waarin elke kanban de specifieke vraag moet verwerken.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="f2ae2-114">Typ of selecteer een waarde in het veld Eerste planactiviteit.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="f2ae2-115">Selecteer Definitieve assemblage.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="f2ae2-116">Vouw de sectie Details uit.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-116">Expand the Details section.</span></span>
6. <span data-ttu-id="f2ae2-117">Typ of selecteer een waarde in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="f2ae2-118">Selecteer L0050.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="f2ae2-119">Een gebeurtenis definiëren</span><span class="sxs-lookup"><span data-stu-id="f2ae2-119">Define an event</span></span>
1. <span data-ttu-id="f2ae2-120">Vouw de sectie Gebeurtenissen uit.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-120">Expand the Events section.</span></span>
2. <span data-ttu-id="f2ae2-121">Selecteer 'Automatisch' in het veld Verkoopgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="f2ae2-122">Door de verkoopgebeurtenis Automatisch te selecteren, wordt deze kanbanregel automatisch geactiveerd wanneer een verkoopregel overeenkomt met het product en de ontvangstlocatie.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="f2ae2-123">In deze procedure is dit product L0050 in magazijn 13.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="f2ae2-124">Stel Minimale gebeurtenishoeveelheid in op '50'.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="f2ae2-125">Met een minimale gebeurtenishoeveelheid van 50 wordt de kanbanregel alleen geactiveerd door gebeurtenissen met een hoeveelheid van 50 of meer.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="f2ae2-126">Vouw de sectie Productiestroom uit.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="f2ae2-127">De Ontvangstlocatie is magazijn 13.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="f2ae2-128">Dit betekent dat deze kanbanregel voor deze locatie zal worden geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="f2ae2-129">In dit voorbeeld zal een verkoopregel voor product L0050, met een hoeveelheid van 50 of meer, in magazijn 13, deze kanbanregel activeren.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="f2ae2-130">Een verkoopregel maken om een gebeurteniskanbanregel te activeren</span><span class="sxs-lookup"><span data-stu-id="f2ae2-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="f2ae2-131">Ga naar Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="f2ae2-132">Er wordt een waarschuwing weergegeven wanneer de kanbanregel is opgeslagen, wat aangeeft dat de kanbans in realtime worden gemaakt tijdens het maken van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="f2ae2-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-133">Click New.</span></span>
3. <span data-ttu-id="f2ae2-134">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="f2ae2-135">Selecteer bijvoorbeeld US-003.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="f2ae2-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-136">Click OK.</span></span>
5. <span data-ttu-id="f2ae2-137">Typ in het veld Artikelnummer de waarde 'L0050'.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="f2ae2-138">Typ '1' in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="f2ae2-139">Selecteer Site 1 omdat Magazijn 13 in Locatie 1 is.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="f2ae2-140">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f2ae2-141">Stel Magazijn in op 13.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="f2ae2-142">Stel Hoeveelheid in op '75'.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="f2ae2-143">Voer een hoeveelheid van 50 of meer in om de gemaakte kanbanregel te activeren.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="f2ae2-144">Controleer of de kanban is gemaakt</span><span class="sxs-lookup"><span data-stu-id="f2ae2-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="f2ae2-145">Klik op Product en voorraad.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-145">Click Product and supply.</span></span>
2. <span data-ttu-id="f2ae2-146">Klik op Behoeftetraceringsstructuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="f2ae2-147">Er wordt een kanban gemaakt met dezelfde hoeveelheid als de verkoopregel.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="f2ae2-148">U kunt ook de materiaaluitgiften zien die nodig zijn om L0050 te produceren.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="f2ae2-149">Dit is de laatste stap in deze procedure.</span><span class="sxs-lookup"><span data-stu-id="f2ae2-149">This is the last step in this procedure.</span></span>  


