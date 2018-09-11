--- 
title: Kanbantaakstatus terugdraaien
description: Deze procedure is gericht op het terugdraaien van een onjuiste kanbantaakstatus.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: da37e9fdfdadeb727bbd123896cc5adfca9f2a59
ms.contentlocale: nl-nl
ms.lasthandoff: 09/11/2018

---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="88191-103">Kanbantaakstatus terugdraaien</span><span class="sxs-lookup"><span data-stu-id="88191-103">Revert kanban job status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88191-104">Deze procedure is gericht op het terugdraaien van een onjuiste kanbantaakstatus.</span><span class="sxs-lookup"><span data-stu-id="88191-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="88191-105">Dit is handig in het geval dat de machineoperator per ongeluk de verkeerde taak bijwerkt of de verkeerde status instelt.</span><span class="sxs-lookup"><span data-stu-id="88191-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="88191-106">In deze procedure wordt een kanbantaak per ongeluk als Voorbereid geregistreerd en wordt de status teruggedraaid.</span><span class="sxs-lookup"><span data-stu-id="88191-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="88191-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="88191-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="88191-108">Deze procedure is bedoeld voor de winkelsupervisor of machineoperator die in een lean manufacturingbedrijf werkt.</span><span class="sxs-lookup"><span data-stu-id="88191-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="88191-109">Verwerkingsbord voor de werkcel openen</span><span class="sxs-lookup"><span data-stu-id="88191-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="88191-110">Ga naar Kanbanplanbord voor procestaken.</span><span class="sxs-lookup"><span data-stu-id="88191-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="88191-111">Typ of selecteer een waarde in het veld Werkcel.</span><span class="sxs-lookup"><span data-stu-id="88191-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="88191-112">Selecteer werkcel 1260.</span><span class="sxs-lookup"><span data-stu-id="88191-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="88191-113">Kanbantaak voorbereiden</span><span class="sxs-lookup"><span data-stu-id="88191-113">Prepare kanban job</span></span>
1. <span data-ttu-id="88191-114">Klik op Voorbereiden.</span><span class="sxs-lookup"><span data-stu-id="88191-114">Click Prepare.</span></span>
    * <span data-ttu-id="88191-115">Als u niet op Voorbereiden kunt klikken omdat dit grijs is, moet u ervoor zorgen dat de geselecteerde kanbantaak de status Gepland heeft, wat wordt aangeduid door het lege kanbanpictogram.</span><span class="sxs-lookup"><span data-stu-id="88191-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="88191-116">Als Voorbereiden mislukt, moet u ervoor zorgen dat alle materialen in de Orderverzamellijst beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="88191-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="88191-117">Selecteer de voorbereide taak in de lijst.</span><span class="sxs-lookup"><span data-stu-id="88191-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="88191-118">Selecteer de eerste taak die u zojuist hebt voorbereid.</span><span class="sxs-lookup"><span data-stu-id="88191-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="88191-119">De takenstatus is voorbereid, wat wordt aangeduid door een driehoek in het kanbanpictogram.</span><span class="sxs-lookup"><span data-stu-id="88191-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="88191-120">De status van de voorbereide kanbantaak herstellen</span><span class="sxs-lookup"><span data-stu-id="88191-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="88191-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="88191-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="88191-122">Selecteer de eerste taak die was voorbereid.</span><span class="sxs-lookup"><span data-stu-id="88191-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="88191-123">Klik in het actievenster op Fabriceren.</span><span class="sxs-lookup"><span data-stu-id="88191-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="88191-124">Klik op Status herstellen</span><span class="sxs-lookup"><span data-stu-id="88191-124">Click Revert status.</span></span>
    * <span data-ttu-id="88191-125">U kunt een andere kanbanregel gebruiken wanneer aan de volgende voorwaarden wordt voldaan: - De aanvullingsstrategie is dezelfde voor beide regels.</span><span class="sxs-lookup"><span data-stu-id="88191-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="88191-126">- De versie van de productiestroom is dezelfde voor beide regels.</span><span class="sxs-lookup"><span data-stu-id="88191-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="88191-127">- Het product dat is geleverd is hetzelfde voor beide regels.</span><span class="sxs-lookup"><span data-stu-id="88191-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="88191-128">- Eventuele downstream activiteiten die voor de laatste activiteit van de kanbanregels zijn geconfigureerd, moeten dezelfde zijn voor beide regels.</span><span class="sxs-lookup"><span data-stu-id="88191-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="88191-129">- Dezelfde geleverde voorraaddimensies moeten voor beide regels zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="88191-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="88191-130">- De status van de verwerkingseenheid moet Niet toegewezen zijn.</span><span class="sxs-lookup"><span data-stu-id="88191-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="88191-131">- De configuratie voor gebeurteniskanbans moet dezelfde zijn.</span><span class="sxs-lookup"><span data-stu-id="88191-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="88191-132">Zorg ervoor dat de nieuwe status Gepland is.</span><span class="sxs-lookup"><span data-stu-id="88191-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="88191-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="88191-133">Click OK.</span></span>
5. <span data-ttu-id="88191-134">Maak in de lijst de markering van de geselecteerde rij ongedaan.</span><span class="sxs-lookup"><span data-stu-id="88191-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="88191-135">Selecteer dezelfde taak.</span><span class="sxs-lookup"><span data-stu-id="88191-135">Select the same job.</span></span>  
    * <span data-ttu-id="88191-136">De taakstatus voor de kanbantaak is terug Gepland, wat wordt aangeduid door een leeg kanbanpictogram.</span><span class="sxs-lookup"><span data-stu-id="88191-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  


