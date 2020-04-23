---
title: Kanbantaken plannen
description: Deze procedure richt zich op het plannen van proceskanbantaken voor een specifieke werkcel.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8342bf6c56adc41cc4944dc709152246ad93a3e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210451"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="5290f-103">Kanbantaken plannen</span><span class="sxs-lookup"><span data-stu-id="5290f-103">Schedule kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5290f-104">Deze procedure richt zich op het plannen van proceskanbantaken voor een specifieke werkcel.</span><span class="sxs-lookup"><span data-stu-id="5290f-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="5290f-105">De procedure "Een proceskanbantaak voorbereiden wanneer de materialen niet beschikbaar zijn" is een vereiste voor het maken van deze procedure.</span><span class="sxs-lookup"><span data-stu-id="5290f-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="5290f-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="5290f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5290f-107">Deze taak is bedoeld voor de werkvloersupervisor en de productieplanner die met kanbans werken.</span><span class="sxs-lookup"><span data-stu-id="5290f-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="5290f-108">Kanbantaken selecteren voor een werkcel</span><span class="sxs-lookup"><span data-stu-id="5290f-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="5290f-109">Ga naar Productiebeheer > Kanban > Kanbantaakplanning.</span><span class="sxs-lookup"><span data-stu-id="5290f-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="5290f-110">Vouw het feitenvak Capaciteit van periode uit</span><span class="sxs-lookup"><span data-stu-id="5290f-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="5290f-111">Vouw het feitenvak Kanban uit.</span><span class="sxs-lookup"><span data-stu-id="5290f-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="5290f-112">Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="5290f-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5290f-113">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5290f-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5290f-114">Selecteer werkcel 1250.</span><span class="sxs-lookup"><span data-stu-id="5290f-114">Select work cell 1250.</span></span> <span data-ttu-id="5290f-115">Hiermee wordt de weergave gefilterd zodat alleen de taken voor werkcel 1250 worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5290f-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="5290f-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5290f-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5290f-117">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="5290f-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="5290f-118">Een kanbantaak plannen tijdens de eerste beschikbare periode</span><span class="sxs-lookup"><span data-stu-id="5290f-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="5290f-119">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5290f-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5290f-120">Selecteer de eerste rij in de lijst die de status Niet gepland heeft.</span><span class="sxs-lookup"><span data-stu-id="5290f-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="5290f-121">Het gestippelde pictogram in het veld Taakstatus geeft Niet gepland aan.</span><span class="sxs-lookup"><span data-stu-id="5290f-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="5290f-122">Klik op Plannen.</span><span class="sxs-lookup"><span data-stu-id="5290f-122">Click Schedule.</span></span>
    * <span data-ttu-id="5290f-123">Hiermee wordt de kanbantaak gepland tijdens de eerste beschikbare periode.</span><span class="sxs-lookup"><span data-stu-id="5290f-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="5290f-124">Merk op dat de kanbantaak naar het einde van de lijst wordt verplaatst omdat deze is toegevoegd aan de periode die vanaf vandaag start.</span><span class="sxs-lookup"><span data-stu-id="5290f-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="5290f-125">Als de periode die vandaag begint volledig is volgeboekt, wordt de taak naar de eerste beschikbare periode verplaatst.</span><span class="sxs-lookup"><span data-stu-id="5290f-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="5290f-126">Twee kanbantaken plannen voor een bepaalde dag</span><span class="sxs-lookup"><span data-stu-id="5290f-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="5290f-127">Selecteer rij 1 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5290f-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="5290f-128">U zult zien dat de eerste rij de status Niet gepland heeft in het veld Taakstatus.</span><span class="sxs-lookup"><span data-stu-id="5290f-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="5290f-129">Selecteer rij 2 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5290f-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="5290f-130">U zult zien dat de tweede rij de status Niet gepland heeft in het veld Taakstatus.</span><span class="sxs-lookup"><span data-stu-id="5290f-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="5290f-131">Nu hebt u de eerste twee taken geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="5290f-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="5290f-132">Klik op Plan vanaf datum om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="5290f-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="5290f-133">Schakel het selectievakje Overschrijf reactie bij capaciteitstekort in of uit.</span><span class="sxs-lookup"><span data-stu-id="5290f-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="5290f-134">Met deze optie kunt u de tekortreactie van de standaardcapaciteit negeren.</span><span class="sxs-lookup"><span data-stu-id="5290f-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="5290f-135">Selecteer in het veld Capaciteitstekort de optie Toevoegen aan de aangevraagde periode.</span><span class="sxs-lookup"><span data-stu-id="5290f-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="5290f-136">Deze optie zorgt ervoor dat de taak wordt toegevoegd aan de aangevraagde periode ongeacht of de werkcel mogelijk overbelast is.</span><span class="sxs-lookup"><span data-stu-id="5290f-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="5290f-137">Klik op Plannen.</span><span class="sxs-lookup"><span data-stu-id="5290f-137">Click Schedule.</span></span>
    * <span data-ttu-id="5290f-138">Merk op dat beide taken zijn toegevoegd aan de gewenste periode.</span><span class="sxs-lookup"><span data-stu-id="5290f-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="5290f-139">In de sectie Periodecapaciteit kunt u de belasting voor elke periode weergeven.</span><span class="sxs-lookup"><span data-stu-id="5290f-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="5290f-140">Het veld Verbruik geeft het geplande verbruik tijdens deze periode aan.</span><span class="sxs-lookup"><span data-stu-id="5290f-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="5290f-141">Als het geplande verbruik hoger is dan de beschikbare capaciteit tijdens deze periode, wordt het overbelaste verbruik geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="5290f-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

