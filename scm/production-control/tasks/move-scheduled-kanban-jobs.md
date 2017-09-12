--- 
title: Geplande kanbantaken verplaatsen
description: Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="6d6f9-103">Geplande kanbantaken verplaatsen</span><span class="sxs-lookup"><span data-stu-id="6d6f9-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d6f9-104">Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="6d6f9-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6d6f9-106">Deze procedure is bedoeld voor de werkvloersupervisor of de productieplanner die met kanbans werken.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="6d6f9-107">Geplande kanbantaken selecteren</span><span class="sxs-lookup"><span data-stu-id="6d6f9-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="6d6f9-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="6d6f9-109">!MtCMR!Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="6d6f9-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="6d6f9-110">áçêìõý !</span></span>
3. <span data-ttu-id="6d6f9-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="6d6f9-112">Selecteer werkcel 1250.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="6d6f9-113">Klik på Select.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-113">Klik på Select.</span></span>
5. <span data-ttu-id="6d6f9-114">Vælg 'Planlagt' i feltet Display job status.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="6d6f9-115">Hiermee wordt de takenlijst gefilterd om alleen de geplande kanbantaken weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="6d6f9-116">Kanbantaken verplaatsen naar een andere periode</span><span class="sxs-lookup"><span data-stu-id="6d6f9-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="6d6f9-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6d6f9-118">Selecteer een taak met de taakstatus Gepland, bijvoorbeeld een taak die is gepland op 20 december 2012 in het veld Geplande periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="6d6f9-119">Verplaats vervolgens de taak naar de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="6d6f9-120">Klik på Previous period.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="6d6f9-121">Klik på End.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-121">Klik på End.</span></span>
    * <span data-ttu-id="6d6f9-122">Hiermee wordt de taak naar het einde van de takenlijst verplaatst als laatste taak in de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="6d6f9-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6d6f9-124">Selecteer een taak met de taakstatus Gepland, bijvoorbeeld een taak die is gepland op 18 december 2012 in het veld Geplande periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="6d6f9-125">Verplaats vervolgens de taak naar de volgende periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="6d6f9-126">Klik på Next period.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-126">Klik på Next period.</span></span>
6. <span data-ttu-id="6d6f9-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-127">Klik på Start.</span></span>
    * <span data-ttu-id="6d6f9-128">Hiermee wordt de taak naar het begin van de takenlijst verplaatst als eerste taak in de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="6d6f9-129">Taak: Een taak binnen een periode verplaatsen</span><span class="sxs-lookup"><span data-stu-id="6d6f9-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="6d6f9-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6d6f9-131">Selecteer een taak met de taakstatus Gepland, bijvoorbeeld de tweede taak die is gepland op 19 december 2012 in het veld Geplande periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="6d6f9-132">Verplaats vervolgens de taak binnen de geplande periode.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="6d6f9-133">Klik på Forward.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-133">Klik på Forward.</span></span>
    * <span data-ttu-id="6d6f9-134">Merk op dat de taak één regel omlaag in de lijst wordt verplaatst.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="6d6f9-135">Klik på Backward.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-135">Klik på Backward.</span></span>
    * <span data-ttu-id="6d6f9-136">Merk op dat de taak één regel omhoog in de lijst wordt verplaatst.</span><span class="sxs-lookup"><span data-stu-id="6d6f9-136">Notice that the job is moved one line up on the list.</span></span>  


