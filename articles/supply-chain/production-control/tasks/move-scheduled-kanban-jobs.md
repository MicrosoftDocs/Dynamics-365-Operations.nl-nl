---
title: Geplande kanbantaken verplaatsen
description: Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode.
author: ChristianRytt
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d58ee740824809f15da68db66616bb01d5dbfab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825009"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="686f2-103">Geplande kanbantaken verplaatsen</span><span class="sxs-lookup"><span data-stu-id="686f2-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="686f2-104">Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode.</span><span class="sxs-lookup"><span data-stu-id="686f2-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="686f2-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="686f2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="686f2-106">Deze procedure is bedoeld voor de werkvloersupervisor of de productieplanner die met kanbans werken.</span><span class="sxs-lookup"><span data-stu-id="686f2-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="686f2-107">Selecteer geplande kanbantaken.</span><span class="sxs-lookup"><span data-stu-id="686f2-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="686f2-108">Ga naar **Productiebeheer > Kanban > Kanbantaakplanning**.</span><span class="sxs-lookup"><span data-stu-id="686f2-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="686f2-109">Klik in het veld **Werkcel** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="686f2-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="686f2-110">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="686f2-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="686f2-111">Selecteer werkcel 1250.</span><span class="sxs-lookup"><span data-stu-id="686f2-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="686f2-112">Klik op **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="686f2-112">Click **Select**.</span></span> 

5. <span data-ttu-id="686f2-113">Selecteer in het veld **Taakstatus weergeven** de optie **Gepland**.</span><span class="sxs-lookup"><span data-stu-id="686f2-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="686f2-114">Hiermee wordt de takenlijst gefilterd om alleen de geplande kanbantaken weer te geven.</span><span class="sxs-lookup"><span data-stu-id="686f2-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="686f2-115">Verplaats kanbantaken naar een andere periode.</span><span class="sxs-lookup"><span data-stu-id="686f2-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="686f2-116">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="686f2-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="686f2-117">Selecteer een taak met de status **Geplande taak**, bijvoorbeeld een taak die is gepland op 20 december 2012 in het veld **Geplande periode**.</span><span class="sxs-lookup"><span data-stu-id="686f2-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="686f2-118">Verplaats vervolgens de taak naar de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="686f2-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="686f2-119">Klik op **Vorige periode**.</span><span class="sxs-lookup"><span data-stu-id="686f2-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="686f2-120">Klik op **Einde** om de taak naar het einde van de takenlijst te verplaatsen als laatste taak in de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="686f2-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="686f2-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="686f2-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="686f2-122">Selecteer een taak met de status **Geplande taak**, bijvoorbeeld een taak die is gepland op 18 december 2012 in het veld **Geplande periode**.</span><span class="sxs-lookup"><span data-stu-id="686f2-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="686f2-123">Verplaats vervolgens de taak naar de volgende periode.</span><span class="sxs-lookup"><span data-stu-id="686f2-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="686f2-124">Klik op **Volgende periode**.</span><span class="sxs-lookup"><span data-stu-id="686f2-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="686f2-125">Klik op **Begin** om de taak naar het begin van de takenlijst te verplaatsen als eerste taak in de vorige periode.</span><span class="sxs-lookup"><span data-stu-id="686f2-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="686f2-126">Verplaats een taak binnen een periode.</span><span class="sxs-lookup"><span data-stu-id="686f2-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="686f2-127">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="686f2-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="686f2-128">Selecteer een taak met de status Geplande taak, bijvoorbeeld de tweede taak die is gepland op 19 december 2012 in het veld **Geplande periode**.</span><span class="sxs-lookup"><span data-stu-id="686f2-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="686f2-129">Verplaats vervolgens de taak binnen de geplande periode.</span><span class="sxs-lookup"><span data-stu-id="686f2-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="686f2-130">Klik op **Vooruit**.</span><span class="sxs-lookup"><span data-stu-id="686f2-130">Click **Forward**.</span></span> <span data-ttu-id="686f2-131">Merk op dat de taak één regel omlaag in de lijst wordt verplaatst.</span><span class="sxs-lookup"><span data-stu-id="686f2-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="686f2-132">Klik op **Achteruit**.</span><span class="sxs-lookup"><span data-stu-id="686f2-132">Click **Backward**.</span></span> <span data-ttu-id="686f2-133">Merk op dat de taak één regel omhoog in de lijst wordt verplaatst.</span><span class="sxs-lookup"><span data-stu-id="686f2-133">Notice that the job is moved one line up on the list.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]