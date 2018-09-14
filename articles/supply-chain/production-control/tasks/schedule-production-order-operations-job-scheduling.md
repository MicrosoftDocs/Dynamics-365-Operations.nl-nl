--- 
title: Een productieorder plannen met bewerkingen en taakplanning
description: Deze procedure is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="7245b-103">Een productieorder plannen met bewerkingen en taakplanning</span><span class="sxs-lookup"><span data-stu-id="7245b-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7245b-104">Deze procedure is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.</span><span class="sxs-lookup"><span data-stu-id="7245b-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="7245b-105">Er worden geen taken gemaakt met bewerkingsplanning, terwijl er wel taken worden gemaakt met taakplanning.</span><span class="sxs-lookup"><span data-stu-id="7245b-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="7245b-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="7245b-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="7245b-107">Deze procedure is bedoeld voor de productiemanager, productieplanner of werkvloersupervisor in een discrete productie-omgeving.</span><span class="sxs-lookup"><span data-stu-id="7245b-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="7245b-108">Een productieorder maken</span><span class="sxs-lookup"><span data-stu-id="7245b-108">Create a production order</span></span>
1. <span data-ttu-id="7245b-109">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="7245b-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="7245b-110">Klik op Nieuwe productieorder.</span><span class="sxs-lookup"><span data-stu-id="7245b-110">Click New production order.</span></span>
3. <span data-ttu-id="7245b-111">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="7245b-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7245b-112">Selecteer artikelnummer D0001.</span><span class="sxs-lookup"><span data-stu-id="7245b-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="7245b-113">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="7245b-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="7245b-114">Bewerkingen plannen voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="7245b-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="7245b-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="7245b-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7245b-116">Selecteer de productieorder die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7245b-116">Select the production order that you have just created.</span></span> <span data-ttu-id="7245b-117">Deze moet boven aan de lijst staan.</span><span class="sxs-lookup"><span data-stu-id="7245b-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="7245b-118">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="7245b-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="7245b-119">Klik op Bewerkingen plannen.</span><span class="sxs-lookup"><span data-stu-id="7245b-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="7245b-120">Selecteer in het veld Planningsrichting de optie "Verder vanaf planningsdatum".</span><span class="sxs-lookup"><span data-stu-id="7245b-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="7245b-121">Voer in het veld Planningsdatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="7245b-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="7245b-122">Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week.</span><span class="sxs-lookup"><span data-stu-id="7245b-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="7245b-123">Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.</span><span class="sxs-lookup"><span data-stu-id="7245b-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="7245b-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7245b-124">Click OK.</span></span>
7. <span data-ttu-id="7245b-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="7245b-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7245b-126">Houd er rekening mee dat de status wordt gewijzigd in Gepland.</span><span class="sxs-lookup"><span data-stu-id="7245b-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="7245b-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="7245b-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7245b-128">Klik op Alle taken.</span><span class="sxs-lookup"><span data-stu-id="7245b-128">Click All jobs.</span></span>
    * <span data-ttu-id="7245b-129">Houd er rekening mee dat er geen taken worden gemaakt met bewerkingsplanning.</span><span class="sxs-lookup"><span data-stu-id="7245b-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="7245b-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7245b-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="7245b-131">Taken plannen voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="7245b-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="7245b-132">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="7245b-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="7245b-133">Klik op Taken plannen.</span><span class="sxs-lookup"><span data-stu-id="7245b-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="7245b-134">Selecteer in het veld Planningsrichting de optie "Verder vanaf planningsdatum".</span><span class="sxs-lookup"><span data-stu-id="7245b-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="7245b-135">Voer in het veld Planningsdatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="7245b-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="7245b-136">Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week.</span><span class="sxs-lookup"><span data-stu-id="7245b-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="7245b-137">Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.</span><span class="sxs-lookup"><span data-stu-id="7245b-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="7245b-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7245b-138">Click OK.</span></span>
6. <span data-ttu-id="7245b-139">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="7245b-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="7245b-140">Klik op Alle taken.</span><span class="sxs-lookup"><span data-stu-id="7245b-140">Click All jobs.</span></span>
    * <span data-ttu-id="7245b-141">Merk op dat op basis van de actieve route, 5 taken worden gemaakt met taakplanning.</span><span class="sxs-lookup"><span data-stu-id="7245b-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  


