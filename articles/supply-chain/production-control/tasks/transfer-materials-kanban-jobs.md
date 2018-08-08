--- 
title: Materialen overboeken met kanbantaken (uitsluitend februari 2016)
description: Deze procedure richt zich op het uitvoeren van een opnamekanbantaak om materialen te boeken.
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: a28755873cda431077c74ac8ac96061a986e55dd
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a><span data-ttu-id="a5fc7-103">Materialen overboeken met kanbantaken (uitsluitend februari 2016)</span><span class="sxs-lookup"><span data-stu-id="a5fc7-103">Transfer materials with kanban jobs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5fc7-104">Deze procedure richt zich op het uitvoeren van een opnamekanbantaak om materialen te boeken.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="a5fc7-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a5fc7-106">Deze procedure is bedoeld voor de magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="a5fc7-107">Overboekingstaken weergeven</span><span class="sxs-lookup"><span data-stu-id="a5fc7-107">Display transfer jobs</span></span>
1. <span data-ttu-id="a5fc7-108">Ga naar Productiebeheer > Kanban > Kanbanbord voor overboekingstaken.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="a5fc7-109">Vouw de sectie Filters uit of samen.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="a5fc7-110">In de sectie Filters kunt u opgeven welke taken u wilt weergeven door op Productiestroom, Activiteitsnaam Van magazijn en locatie en Naar magazijn en locatie te filteren.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="a5fc7-111">Typ "11" in het veld Van magazijn.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="a5fc7-112">Typ "12" in het veld Naar locatie.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="a5fc7-113">Een overboekingstaak starten</span><span class="sxs-lookup"><span data-stu-id="a5fc7-113">Start a transfer job</span></span>
1. <span data-ttu-id="a5fc7-114">Schakel in de lijst de geselecteerde rij uit, indien aanwezig.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="a5fc7-115">Selecteer rij 4 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="a5fc7-116">Selecteer de eerste taak met de status Niet gepland.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="a5fc7-117">Zorg ervoor dat dit de enige geselecteerde taak is.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="a5fc7-118">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-118">Click Start.</span></span>
    * <span data-ttu-id="a5fc7-119">Merk op dat een pictogram aangeeft dat de taak is gestart.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="a5fc7-120">Een tweede overboekingstaak en wijzigingshoeveelheid selecteren</span><span class="sxs-lookup"><span data-stu-id="a5fc7-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="a5fc7-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a5fc7-122">U kunt meerdere geselecteerde taken hebben, maar selecteert nu moment rij 5.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="a5fc7-123">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a5fc7-124">Zorg ervoor de taak in de vorige stap de enige geselecteerde taak is.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="a5fc7-125">Maak de selectie van alle andere taken ongedaan.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="a5fc7-126">Noteer de waarde in het veld Taakhoeveelheid zodat u er later naar kunt verwijzen</span><span class="sxs-lookup"><span data-stu-id="a5fc7-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="a5fc7-127">Stel Taakhoeveelheid in op "30".</span><span class="sxs-lookup"><span data-stu-id="a5fc7-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="a5fc7-128">Let op de waarschuwing!</span><span class="sxs-lookup"><span data-stu-id="a5fc7-128">Notice the warning!</span></span> <span data-ttu-id="a5fc7-129">U mag niet 30 overboeken.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="a5fc7-130">Volgens de instellingen van de kanbanregel, kunt u alleen de originele hoeveelheid overboeken.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="a5fc7-131">Gebruik de eerder genoteerde waarde in het veld Taakhoeveelheid</span><span class="sxs-lookup"><span data-stu-id="a5fc7-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="a5fc7-132">Stel de taakhoeveelheid in op de vorige waarde.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="a5fc7-133">De tweede overboekingstaak starten</span><span class="sxs-lookup"><span data-stu-id="a5fc7-133">Start the second transfer job</span></span>
1. <span data-ttu-id="a5fc7-134">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-134">Click Start.</span></span>
    * <span data-ttu-id="a5fc7-135">Hiermee wordt de overboeking van de taak in rij 5 gestart.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="a5fc7-136">Beide overboekingstaken voltooien</span><span class="sxs-lookup"><span data-stu-id="a5fc7-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="a5fc7-137">Selecteer rij 4 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="a5fc7-138">Nu worden twee overboekingstaken geselecteerd op rij 4 en 5.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="a5fc7-139">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-139">Click Complete.</span></span>
    * <span data-ttu-id="a5fc7-140">Hiermee wordt de overboeking van beide taken voltooid.</span><span class="sxs-lookup"><span data-stu-id="a5fc7-140">This will complete the transfer of both jobs.</span></span>  


