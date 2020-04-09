---
title: Geplande kanbantaken verplaatsen
description: Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cad61ad292f80d6092ecea679645f729469b8a8f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148967"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="8a402-103">Geplande kanbantaken verplaatsen</span><span class="sxs-lookup"><span data-stu-id="8a402-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a402-104">Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode.</span><span class="sxs-lookup"><span data-stu-id="8a402-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="8a402-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="8a402-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8a402-106">Deze procedure is bedoeld voor de werkvloersupervisor of de productieplanner die met kanbans werken.</span><span class="sxs-lookup"><span data-stu-id="8a402-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="8a402-107">Selecteer geplande kanbantaken.</span><span class="sxs-lookup"><span data-stu-id="8a402-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="8a402-108">Ga naar **Productiebeheer > Kanban > Kanbantaakplanning**.</span><span class="sxs-lookup"><span data-stu-id="8a402-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="8a402-109">Klik in het veld **Werkcel** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8a402-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="8a402-110">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8a402-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="8a402-111">Selecteer werkcel 1250.</span><span class="sxs-lookup"><span data-stu-id="8a402-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="8a402-112">Klik op **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="8a402-112">Click **Select**.</span></span> 

5. <span data-ttu-id="8a402-113">Selecteer in het veld **Taakstatus weergeven** de optie **Gepland**.</span><span class="sxs-lookup"><span data-stu-id="8a402-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="8a402-114">Hiermee wordt de takenlijst gefilterd om alleen de geplande kanbantaken weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8a402-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="8a402-115">Verplaats kanbantaken naar een andere periode.</span><span class="sxs-lookup"><span data-stu-id="8a402-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="8a402-116">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8a402-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a402-117">Selecteer een taak met de status **Geplande taak**, bijvoorbeeld een taak die is gepland op 20 december 2012 in het veld **Geplande periode**.</span><span class="sxs-lookup"><span data-stu-id="8a402-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="8a402-118">Verplaats vervolgens de taak naar de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="8a402-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="8a402-119">Klik op **Vorige periode**.</span><span class="sxs-lookup"><span data-stu-id="8a402-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="8a402-120">Klik op **Einde** om de taak naar het einde van de takenlijst te verplaatsen als laatste taak in de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="8a402-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="8a402-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8a402-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a402-122">Selecteer een taak met de status **Geplande taak**, bijvoorbeeld een taak die is gepland op 18 december 2012 in het veld **Geplande periode**.</span><span class="sxs-lookup"><span data-stu-id="8a402-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="8a402-123">Verplaats vervolgens de taak naar de volgende periode.</span><span class="sxs-lookup"><span data-stu-id="8a402-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="8a402-124">Klik op **Volgende periode**.</span><span class="sxs-lookup"><span data-stu-id="8a402-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="8a402-125">Klik op **Begin** om de taak naar het begin van de takenlijst te verplaatsen als eerste taak in de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="8a402-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="8a402-126">Verplaats een taak binnen een periode.</span><span class="sxs-lookup"><span data-stu-id="8a402-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="8a402-127">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8a402-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a402-128">Selecteer een taak met de status Geplande taak, bijvoorbeeld de tweede taak die is gepland op 19 december 2012 in het veld **Geplande periode**.</span><span class="sxs-lookup"><span data-stu-id="8a402-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="8a402-129">Verplaats vervolgens de taak binnen de geplande periode.</span><span class="sxs-lookup"><span data-stu-id="8a402-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="8a402-130">Klik op **Vooruit**.</span><span class="sxs-lookup"><span data-stu-id="8a402-130">Click **Forward**.</span></span> <span data-ttu-id="8a402-131">Merk op dat de taak één regel omlaag in de lijst wordt verplaatst.</span><span class="sxs-lookup"><span data-stu-id="8a402-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="8a402-132">Klik op **Achteruit**.</span><span class="sxs-lookup"><span data-stu-id="8a402-132">Click **Backward**.</span></span> <span data-ttu-id="8a402-133">Merk op dat de taak één regel omhoog in de lijst wordt verplaatst.</span><span class="sxs-lookup"><span data-stu-id="8a402-133">Notice that the job is moved one line up on the list.</span></span>
