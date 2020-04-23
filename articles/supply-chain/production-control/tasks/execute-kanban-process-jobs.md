---
title: Kanbanprocestaken uitvoeren
description: Deze procedure is gericht op het uitvoeren van kanbanprocestaken.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1c32b577007c400f3528a110436eb97aaabefe2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207020"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="26118-103">Kanbanprocestaken uitvoeren</span><span class="sxs-lookup"><span data-stu-id="26118-103">Execute kanban process jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26118-104">Deze procedure is gericht op het uitvoeren van kanbanprocestaken.</span><span class="sxs-lookup"><span data-stu-id="26118-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="26118-105">De eerste taak wordt voltooid met de verwachte hoeveelheid en heeft geen fouten.</span><span class="sxs-lookup"><span data-stu-id="26118-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="26118-106">De tweede taak wordt voltooid met fouten.</span><span class="sxs-lookup"><span data-stu-id="26118-106">The second job is completed with errors.</span></span> <span data-ttu-id="26118-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="26118-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="26118-108">Deze procedure is bedoeld voor de machineoperator.</span><span class="sxs-lookup"><span data-stu-id="26118-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="26118-109">Een kanbantaak selecteren</span><span class="sxs-lookup"><span data-stu-id="26118-109">Select a kanban job</span></span>
1. <span data-ttu-id="26118-110">Ga naar Productiebeheer > Kanban > Kanbanplanbord voor procestaken.</span><span class="sxs-lookup"><span data-stu-id="26118-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="26118-111">Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="26118-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="26118-112">Klik op de rij met resourcegroep 1250.</span><span class="sxs-lookup"><span data-stu-id="26118-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="26118-113">Hiermee wordt de lijst met taken gefilterd zodat alleen de taken voor werkcel 1250 worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="26118-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="26118-114">Markeer de rij met de status Geplande taak.</span><span class="sxs-lookup"><span data-stu-id="26118-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="26118-115">Een taak uitvoeren met verwachte hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="26118-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="26118-116">Vouw de sectie Details uit of samen.</span><span class="sxs-lookup"><span data-stu-id="26118-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="26118-117">Deze sectie bevat belangrijke informatie over kaartnummer, artikelnummer, bestelde hoeveelheid en activiteitsnaam.</span><span class="sxs-lookup"><span data-stu-id="26118-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="26118-118">Vouw de sectie Productie-instructies uit of samen.</span><span class="sxs-lookup"><span data-stu-id="26118-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="26118-119">Deze sectie bevat productie-instructies voor de activiteit.</span><span class="sxs-lookup"><span data-stu-id="26118-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="26118-120">De instructies kunnen tekst, afbeeldingen, tekeningen en andere documenten zijn.</span><span class="sxs-lookup"><span data-stu-id="26118-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="26118-121">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="26118-121">Click Start.</span></span>
    * <span data-ttu-id="26118-122">Selecteer een taak die niet voltooid is.</span><span class="sxs-lookup"><span data-stu-id="26118-122">Select a job that is not completed.</span></span> <span data-ttu-id="26118-123">Gebruik statuspictogrammen in het veld Taakstatus om de taakstatus weer te geven.</span><span class="sxs-lookup"><span data-stu-id="26118-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="26118-124">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="26118-124">Click Complete.</span></span>
    * <span data-ttu-id="26118-125">De taak is voltooid met de verwachte kwaliteit.</span><span class="sxs-lookup"><span data-stu-id="26118-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="26118-126">Een taak uitvoeren met fouten</span><span class="sxs-lookup"><span data-stu-id="26118-126">Complete a job with errors</span></span>
1. <span data-ttu-id="26118-127">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="26118-127">Click Start.</span></span>
    * <span data-ttu-id="26118-128">Wanneer een taak is voltooid, wordt de volgende taak in de lijst automatisch geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="26118-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="26118-129">Om deze reden hoeft u geen taak te selecteren voordat u op Start klikt.</span><span class="sxs-lookup"><span data-stu-id="26118-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="26118-130">Klik in het actievenster op Fabriceren.</span><span class="sxs-lookup"><span data-stu-id="26118-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="26118-131">Klik op Voltooien (details).</span><span class="sxs-lookup"><span data-stu-id="26118-131">Click Complete (details).</span></span>
4. <span data-ttu-id="26118-132">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="26118-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="26118-133">Voer in het veld Slechte hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="26118-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="26118-134">Voer in het veld Goede hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="26118-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="26118-135">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="26118-135">Click OK.</span></span>

