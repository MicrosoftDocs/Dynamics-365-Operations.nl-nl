--- 
title: Een kanbanregel voor gebeurtenis stuklijstregel maken
description: Deze taak is gericht op de instellingen die nodig zijn om een gebeurteniskanbanregel te maken om te zorgen voor levering voor BOM-productiestuklijstregels in een gemengde lean- en klassieke productieomgeving.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 452cc5cf6060b71f91ad43e39e756dc23d759448
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="b5354-103">Een kanbanregel voor gebeurtenis stuklijstregel maken</span><span class="sxs-lookup"><span data-stu-id="b5354-103">Create a BOM line event kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5354-104">Deze taak is gericht op de instellingen die nodig zijn om een gebeurteniskanbanregel te maken om te zorgen voor levering voor BOM-productiestuklijstregels in een gemengde lean- en klassieke productieomgeving.</span><span class="sxs-lookup"><span data-stu-id="b5354-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="b5354-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="b5354-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="b5354-106">Deze taak is bedoeld voor de procesingenieur of de waardestroombeheerder, want zij bereiden de productie van een nieuw of gewijzigd product voor.</span><span class="sxs-lookup"><span data-stu-id="b5354-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="b5354-107">Een nieuwe kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="b5354-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="b5354-108">Ga naar Productiebeheer > Periodieke taken > Berekening kanbanhoeveelheid > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="b5354-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="b5354-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b5354-109">Click New.</span></span>
3. <span data-ttu-id="b5354-110">Selecteer Opname in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="b5354-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="b5354-111">Het opnametype wordt gebruikt om overboekingskanbans te maken.</span><span class="sxs-lookup"><span data-stu-id="b5354-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="b5354-112">Selecteer 'Gebeurtenis' in het veld Aanvullingsstrategie.</span><span class="sxs-lookup"><span data-stu-id="b5354-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="b5354-113">De gebeurtenisstrategie wordt geselecteerd om de overboeking van kanbans op basis van een gebeurtenis te maken.</span><span class="sxs-lookup"><span data-stu-id="b5354-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="b5354-114">Later in de taakbegeleiding wordt dit geactiveerd door een productieorder te ramen.</span><span class="sxs-lookup"><span data-stu-id="b5354-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="b5354-115">Typ of selecteer een waarde in het veld Eerste planactiviteit.</span><span class="sxs-lookup"><span data-stu-id="b5354-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="b5354-116">Typ of selecteer ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="b5354-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="b5354-117">Deze overboekingsactiviteit heeft magazijn en locatie 12 voor ontvangst (uitvoer), wat betekent dat materiaal naar locatie 12 in magazijn 12 wordt verplaatst.</span><span class="sxs-lookup"><span data-stu-id="b5354-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="b5354-118">Vouw de sectie Details uit.</span><span class="sxs-lookup"><span data-stu-id="b5354-118">Expand the Details section.</span></span>
7. <span data-ttu-id="b5354-119">Typ of selecteer M0001 in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="b5354-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="b5354-120">Vouw de sectie Gebeurtenissen uit.</span><span class="sxs-lookup"><span data-stu-id="b5354-120">Expand the Events section.</span></span>
9. <span data-ttu-id="b5354-121">Selecteer 'Automatisch' in het veld Stuklijstgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="b5354-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="b5354-122">Met het veld Stuklijstregelgebeurtenis ingesteld op Automatisch wordt de kanban gemaakt om aan de materiaalvereisten voor productieorderstuklijstregels te voldoen.</span><span class="sxs-lookup"><span data-stu-id="b5354-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="b5354-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5354-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="b5354-124">Een nieuwe productieorder maken en wijzigen</span><span class="sxs-lookup"><span data-stu-id="b5354-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="b5354-125">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="b5354-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="b5354-126">Klik op Nieuwe productieorder.</span><span class="sxs-lookup"><span data-stu-id="b5354-126">Click New production order.</span></span>
3. <span data-ttu-id="b5354-127">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="b5354-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b5354-128">Typ of selecteer 'L0001'.</span><span class="sxs-lookup"><span data-stu-id="b5354-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="b5354-129">Artikel L0001 wordt gebruikt omdat artikel M0001 in de stuklijst voor artikel L0001 is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b5354-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="b5354-130">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="b5354-130">Click Create.</span></span>
5. <span data-ttu-id="b5354-131">Klik in de lijst op de koppeling in de rij voor L0001.</span><span class="sxs-lookup"><span data-stu-id="b5354-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="b5354-132">Klik op Stuklijst.</span><span class="sxs-lookup"><span data-stu-id="b5354-132">Click BOM.</span></span>
7. <span data-ttu-id="b5354-133">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5354-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b5354-134">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="b5354-134">Click Edit.</span></span>
9. <span data-ttu-id="b5354-135">Selecteer 'Getraceerd aanbod' in het veld Regeltype.</span><span class="sxs-lookup"><span data-stu-id="b5354-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="b5354-136">Getraceerd aanbod wordt geselecteerd om het maken van aanbod van een kanban te activeren.</span><span class="sxs-lookup"><span data-stu-id="b5354-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="b5354-137">Selecteer Nee in het veld Resourceverbruik.</span><span class="sxs-lookup"><span data-stu-id="b5354-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="b5354-138">Als het selectievakje Resourceverbruik wordt uitgeschakeld, kan het magazijn worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b5354-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="b5354-139">Vouw de sectie Voorraaddimensies uit.</span><span class="sxs-lookup"><span data-stu-id="b5354-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="b5354-140">Typ "12" in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="b5354-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="b5354-141">Het magazijn is ingesteld op 12 omdat dit het uitvoermagazijn voor de opnameactiviteit is.</span><span class="sxs-lookup"><span data-stu-id="b5354-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="b5354-142">Typ 12 in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="b5354-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="b5354-143">Locatie is ingesteld op 12 omdat dit de uitvoerlocatie van de opnameactiviteit is.</span><span class="sxs-lookup"><span data-stu-id="b5354-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="b5354-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5354-144">Close the page.</span></span>
15. <span data-ttu-id="b5354-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5354-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="b5354-146">Een schatting maken van de productieorder en de gemaakte kanban weergeven</span><span class="sxs-lookup"><span data-stu-id="b5354-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="b5354-147">Klik op Raming.</span><span class="sxs-lookup"><span data-stu-id="b5354-147">Click Estimate.</span></span>
    * <span data-ttu-id="b5354-148">Door de productieorder te ramen wordt het maken van de gekoppelde kanban geactiveerd om artikel M0001 te leveren.</span><span class="sxs-lookup"><span data-stu-id="b5354-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="b5354-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b5354-149">Click OK.</span></span>
3. <span data-ttu-id="b5354-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5354-150">Close the page.</span></span>
4. <span data-ttu-id="b5354-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b5354-151">Close the page.</span></span>
5. <span data-ttu-id="b5354-152">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="b5354-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="b5354-153">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5354-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b5354-154">Selecteer de gebeurteniskanbanregel die is gemaakt voor artikel M0001.</span><span class="sxs-lookup"><span data-stu-id="b5354-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="b5354-155">Vouw de sectie Kanbans uit.</span><span class="sxs-lookup"><span data-stu-id="b5354-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="b5354-156">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b5354-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b5354-157">Let op de kanban die is gemaakt om M0001 te leveren voor de geschatte productieorder.</span><span class="sxs-lookup"><span data-stu-id="b5354-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="b5354-158">Dit is de laatste stap.</span><span class="sxs-lookup"><span data-stu-id="b5354-158">This is the last step!</span></span>  


