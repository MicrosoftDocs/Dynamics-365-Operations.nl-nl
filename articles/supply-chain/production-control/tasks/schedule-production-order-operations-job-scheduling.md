---
title: Een productieorder plannen met bewerkingen en taakplanning
description: Dit onderwerp is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3023d6a6fe09c84b47839a2c4b78c37907754ded
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914879"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="da513-103">Een productieorder plannen met bewerkingen en taakplanning</span><span class="sxs-lookup"><span data-stu-id="da513-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da513-104">Dit onderwerp is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.</span><span class="sxs-lookup"><span data-stu-id="da513-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="da513-105">Er worden geen taken gemaakt met bewerkingsplanning, terwijl er wel taken worden gemaakt met taakplanning.</span><span class="sxs-lookup"><span data-stu-id="da513-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="da513-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="da513-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="da513-107">Deze procedure is bedoeld voor de productiemanager, productieplanner of werkvloersupervisor in een discrete productie-omgeving.</span><span class="sxs-lookup"><span data-stu-id="da513-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="da513-108">Een productieorder maken</span><span class="sxs-lookup"><span data-stu-id="da513-108">Create a production order</span></span>
1. <span data-ttu-id="da513-109">Ga in het navigatievenster naar **Modules > Productiebeheer > Productieorders > Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="da513-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="da513-110">Selecteer **Nieuwe productieorder**.</span><span class="sxs-lookup"><span data-stu-id="da513-110">Select **New production order**.</span></span>
3. <span data-ttu-id="da513-111">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="da513-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="da513-112">Selecteer artikelnummer **D0001**.</span><span class="sxs-lookup"><span data-stu-id="da513-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="da513-113">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="da513-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="da513-114">Bewerkingen plannen voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="da513-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="da513-115">Markeer de nieuwe rij.</span><span class="sxs-lookup"><span data-stu-id="da513-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="da513-116">Selecteer in het actievenster de optie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="da513-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="da513-117">Selecteert **Bewerkingen plannen**.</span><span class="sxs-lookup"><span data-stu-id="da513-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="da513-118">Selecteer in het veld **Planningsrichting** de optie **Verder vanaf planningsdatum**.</span><span class="sxs-lookup"><span data-stu-id="da513-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="da513-119">Voer in het veld **Planningsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="da513-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="da513-120">Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week.</span><span class="sxs-lookup"><span data-stu-id="da513-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="da513-121">Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.</span><span class="sxs-lookup"><span data-stu-id="da513-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="da513-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="da513-122">Select **OK**.</span></span>
7. <span data-ttu-id="da513-123">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="da513-123">In the list, mark the selected row.</span></span> <span data-ttu-id="da513-124">Houd er rekening mee dat de status wordt gewijzigd in **Gepland**.</span><span class="sxs-lookup"><span data-stu-id="da513-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="da513-125">Selecteer **Alle taken**.</span><span class="sxs-lookup"><span data-stu-id="da513-125">Select **All jobs**.</span></span> <span data-ttu-id="da513-126">Houd er rekening mee dat er geen taken worden gemaakt met bewerkingsplanning.</span><span class="sxs-lookup"><span data-stu-id="da513-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="da513-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="da513-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="da513-128">Taken plannen voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="da513-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="da513-129">Selecteer in het actievenster de optie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="da513-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="da513-130">Selecteer **Taken plannen**.</span><span class="sxs-lookup"><span data-stu-id="da513-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="da513-131">Selecteer in het veld **Planningsrichting** de optie **Verder vanaf planningsdatum**.</span><span class="sxs-lookup"><span data-stu-id="da513-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="da513-132">Voer in het veld **Planningsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="da513-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="da513-133">Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week.</span><span class="sxs-lookup"><span data-stu-id="da513-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="da513-134">Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.</span><span class="sxs-lookup"><span data-stu-id="da513-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="da513-135">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="da513-135">Select **OK**.</span></span>
6. <span data-ttu-id="da513-136">Selecteer **Productieorder** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="da513-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="da513-137">Selecteer **Alle taken**.</span><span class="sxs-lookup"><span data-stu-id="da513-137">Select **All jobs**.</span></span> <span data-ttu-id="da513-138">Merk op dat op basis van de actieve route, 5 taken worden gemaakt met taakplanning.</span><span class="sxs-lookup"><span data-stu-id="da513-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

