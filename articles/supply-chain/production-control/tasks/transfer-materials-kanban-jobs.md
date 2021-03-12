---
title: Materialen overboeken met kanbantaken
description: Deze procedure richt zich op het uitvoeren van een opnamekanbantaak om materialen te boeken.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8808b168d2b3845b315e6bbcfb376e37f31fe4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981026"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="a5551-103">Materialen overboeken met kanbantaken</span><span class="sxs-lookup"><span data-stu-id="a5551-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5551-104">Deze procedure richt zich op het uitvoeren van een opnamekanbantaak om materialen te boeken.</span><span class="sxs-lookup"><span data-stu-id="a5551-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="a5551-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="a5551-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a5551-106">Deze procedure is bedoeld voor de magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="a5551-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="a5551-107">Overboekingstaken weergeven</span><span class="sxs-lookup"><span data-stu-id="a5551-107">Display transfer jobs</span></span>
1. <span data-ttu-id="a5551-108">Ga naar Productiebeheer > Kanban > Kanbanbord voor overboekingstaken.</span><span class="sxs-lookup"><span data-stu-id="a5551-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="a5551-109">Vouw de sectie Filters uit of samen.</span><span class="sxs-lookup"><span data-stu-id="a5551-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="a5551-110">In de sectie Filters kunt u opgeven welke taken u wilt weergeven door op Productiestroom, Activiteitsnaam Van magazijn en locatie en Naar magazijn en locatie te filteren.</span><span class="sxs-lookup"><span data-stu-id="a5551-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="a5551-111">Typ "11" in het veld Van magazijn.</span><span class="sxs-lookup"><span data-stu-id="a5551-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="a5551-112">Typ "12" in het veld Naar locatie.</span><span class="sxs-lookup"><span data-stu-id="a5551-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="a5551-113">Een overboekingstaak starten</span><span class="sxs-lookup"><span data-stu-id="a5551-113">Start a transfer job</span></span>
1. <span data-ttu-id="a5551-114">Schakel in de lijst de geselecteerde rij uit, indien aanwezig.</span><span class="sxs-lookup"><span data-stu-id="a5551-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="a5551-115">Selecteer rij 4 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5551-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="a5551-116">Selecteer de eerste taak met de status Niet gepland.</span><span class="sxs-lookup"><span data-stu-id="a5551-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="a5551-117">Zorg ervoor dat dit de enige geselecteerde taak is.</span><span class="sxs-lookup"><span data-stu-id="a5551-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="a5551-118">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="a5551-118">Click Start.</span></span>
    * <span data-ttu-id="a5551-119">Merk op dat een pictogram aangeeft dat de taak is gestart.</span><span class="sxs-lookup"><span data-stu-id="a5551-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="a5551-120">Een tweede overboekingstaak en wijzigingshoeveelheid selecteren</span><span class="sxs-lookup"><span data-stu-id="a5551-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="a5551-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5551-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a5551-122">U kunt meerdere geselecteerde taken hebben, maar selecteert nu moment rij 5.</span><span class="sxs-lookup"><span data-stu-id="a5551-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="a5551-123">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5551-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a5551-124">Zorg ervoor de taak in de vorige stap de enige geselecteerde taak is.</span><span class="sxs-lookup"><span data-stu-id="a5551-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="a5551-125">Maak de selectie van alle andere taken ongedaan.</span><span class="sxs-lookup"><span data-stu-id="a5551-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="a5551-126">Noteer de waarde in het veld Taakhoeveelheid zodat u er later naar kunt verwijzen</span><span class="sxs-lookup"><span data-stu-id="a5551-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="a5551-127">Stel Taakhoeveelheid in op "30".</span><span class="sxs-lookup"><span data-stu-id="a5551-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="a5551-128">Let op de waarschuwing!</span><span class="sxs-lookup"><span data-stu-id="a5551-128">Notice the warning!</span></span> <span data-ttu-id="a5551-129">U mag niet 30 overboeken.</span><span class="sxs-lookup"><span data-stu-id="a5551-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="a5551-130">Volgens de instellingen van de kanbanregel, kunt u alleen de originele hoeveelheid overboeken.</span><span class="sxs-lookup"><span data-stu-id="a5551-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="a5551-131">Gebruik de eerder genoteerde waarde in het veld Taakhoeveelheid</span><span class="sxs-lookup"><span data-stu-id="a5551-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="a5551-132">Stel de taakhoeveelheid in op de vorige waarde.</span><span class="sxs-lookup"><span data-stu-id="a5551-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="a5551-133">De tweede overboekingstaak starten</span><span class="sxs-lookup"><span data-stu-id="a5551-133">Start the second transfer job</span></span>
1. <span data-ttu-id="a5551-134">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="a5551-134">Click Start.</span></span>
    * <span data-ttu-id="a5551-135">Hiermee wordt de overboeking van de taak in rij 5 gestart.</span><span class="sxs-lookup"><span data-stu-id="a5551-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="a5551-136">Beide overboekingstaken voltooien</span><span class="sxs-lookup"><span data-stu-id="a5551-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="a5551-137">Selecteer rij 4 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a5551-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="a5551-138">Nu worden twee overboekingstaken geselecteerd op rij 4 en 5.</span><span class="sxs-lookup"><span data-stu-id="a5551-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="a5551-139">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="a5551-139">Click Complete.</span></span>
    * <span data-ttu-id="a5551-140">Hiermee wordt de overboeking van beide taken voltooid.</span><span class="sxs-lookup"><span data-stu-id="a5551-140">This will complete the transfer of both jobs.</span></span>  

