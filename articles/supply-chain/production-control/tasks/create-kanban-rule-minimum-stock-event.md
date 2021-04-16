---
title: Een kanbanregel maken met een gebeurtenis minimale voorraad
description: Deze procedure is gericht op de instellingen die nodig zijn om een kanbanregel te maken met een minimumvoorraadgebeurtenis om ervoor te zorgen dat een specifiek product altijd beschikbaar is op een specifieke locatie.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 598af59a1b30cfeb5c25c89d95e1a60e6707c899
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829085"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="1a10d-103">Een kanbanregel maken met een gebeurtenis minimale voorraad</span><span class="sxs-lookup"><span data-stu-id="1a10d-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a10d-104">Deze procedure is gericht op de instellingen die nodig zijn om een kanbanregel te maken met een minimumvoorraadgebeurtenis om ervoor te zorgen dat een specifiek product altijd beschikbaar is op een specifieke locatie.</span><span class="sxs-lookup"><span data-stu-id="1a10d-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="1a10d-105">Er wordt een kanbanregel gemaakt om materiaal naar de locatie over te dragen wanneer het voorraadniveau tot onder de 200 stuks daalt.</span><span class="sxs-lookup"><span data-stu-id="1a10d-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="1a10d-106">Door de verwerking van gebeurtenissen voor tracering van de behoefte uit te voeren, worden de benodigde kanbans gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1a10d-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="1a10d-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="1a10d-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="1a10d-108">Deze taak is bedoeld voor de procestechnicus of de waardestroombeheerder bij het voorbereiden van de productie van een nieuw of gewijzigd product in een lean-omgeving.</span><span class="sxs-lookup"><span data-stu-id="1a10d-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="1a10d-109">Een nieuwe kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="1a10d-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="1a10d-110">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="1a10d-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="1a10d-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1a10d-111">Click New.</span></span>
3. <span data-ttu-id="1a10d-112">Selecteer Opname in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="1a10d-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="1a10d-113">Dit type wordt gebruikt om overboekingskanbans te maken.</span><span class="sxs-lookup"><span data-stu-id="1a10d-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="1a10d-114">Selecteer 'Gebeurtenis' in het veld Aanvullingsstrategie.</span><span class="sxs-lookup"><span data-stu-id="1a10d-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="1a10d-115">De gebeurtenisstrategie wordt gebruikt voor het maken van overboekingskanbans op basis van een gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="1a10d-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="1a10d-116">Later in de procedure activeert u overboekingskanbans door voorraadaanvulling te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1a10d-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="1a10d-117">Typ of selecteer een waarde in het veld Eerste planactiviteit.</span><span class="sxs-lookup"><span data-stu-id="1a10d-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="1a10d-118">Typ of selecteer ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="1a10d-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="1a10d-119">Deze overboekingsactiviteit heeft magazijn en locatie 12 voor ontvangst (uitvoer), wat betekent dat materialen naar locatie 12 in magazijn 12 worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="1a10d-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="1a10d-120">Vouw de sectie Details uit.</span><span class="sxs-lookup"><span data-stu-id="1a10d-120">Expand the Details section.</span></span>
7. <span data-ttu-id="1a10d-121">Typ of selecteer een waarde in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="1a10d-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="1a10d-122">Selecteer M0007.</span><span class="sxs-lookup"><span data-stu-id="1a10d-122">Select M0007.</span></span>  
8. <span data-ttu-id="1a10d-123">Vouw de sectie Gebeurtenissen uit.</span><span class="sxs-lookup"><span data-stu-id="1a10d-123">Expand the Events section.</span></span>
9. <span data-ttu-id="1a10d-124">Selecteer 'Batch' in het veld Voorraadaanvullingsgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="1a10d-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="1a10d-125">Hiermee worden kanbans gemaakt om te voldoen materiaalbehoeften op de gerelateerde locatie tijdens de verwerking van gebeurtenissen voor tracering van de behoefte.</span><span class="sxs-lookup"><span data-stu-id="1a10d-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="1a10d-126">Stel de minimumhoeveelheid voor het artikel in.</span><span class="sxs-lookup"><span data-stu-id="1a10d-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="1a10d-127">Klik in het veld Product om de koppeling te volgen.</span><span class="sxs-lookup"><span data-stu-id="1a10d-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="1a10d-128">Klik om de koppeling in het veld Artikelnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="1a10d-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="1a10d-129">Vouw het feitenvak Productafbeelding uit.</span><span class="sxs-lookup"><span data-stu-id="1a10d-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="1a10d-130">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="1a10d-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="1a10d-131">Klik op Artikelbehoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="1a10d-131">Click Item coverage.</span></span>
6. <span data-ttu-id="1a10d-132">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1a10d-132">Click New.</span></span>
7. <span data-ttu-id="1a10d-133">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1a10d-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1a10d-134">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="1a10d-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1a10d-135">Stel Magazijn in op 12.</span><span class="sxs-lookup"><span data-stu-id="1a10d-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="1a10d-136">Stel Minimum in op '200'.</span><span class="sxs-lookup"><span data-stu-id="1a10d-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="1a10d-137">De taak voor het maken van een batchgebeurtenis uitvoeren</span><span class="sxs-lookup"><span data-stu-id="1a10d-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="1a10d-138">Ga naar Productiebeheer > Periodieke taken > Batchverwerking van kanbantaak > Verwerking van gebeurtenis voor tracering van de behoefte.</span><span class="sxs-lookup"><span data-stu-id="1a10d-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="1a10d-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1a10d-139">Click OK.</span></span>
3. <span data-ttu-id="1a10d-140">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="1a10d-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="1a10d-141">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1a10d-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1a10d-142">Selecteer de kanbanregel die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1a10d-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="1a10d-143">Vouw de sectie Kanbans uit.</span><span class="sxs-lookup"><span data-stu-id="1a10d-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="1a10d-144">Merk op dat een kanban is gemaakt om het benodigde materiaal over te dragen naar magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="1a10d-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]