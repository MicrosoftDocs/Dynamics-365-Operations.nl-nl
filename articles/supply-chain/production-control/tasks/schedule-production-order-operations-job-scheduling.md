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
ms.openlocfilehash: 2181a84aea08aac0ddb202f7211dbda6330a3d49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148832"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="aacac-103">Een productieorder plannen met bewerkingen en taakplanning</span><span class="sxs-lookup"><span data-stu-id="aacac-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aacac-104">Dit onderwerp is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.</span><span class="sxs-lookup"><span data-stu-id="aacac-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="aacac-105">Er worden geen taken gemaakt met bewerkingsplanning, terwijl er wel taken worden gemaakt met taakplanning.</span><span class="sxs-lookup"><span data-stu-id="aacac-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="aacac-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="aacac-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="aacac-107">Deze procedure is bedoeld voor de productiemanager, productieplanner of werkvloersupervisor in een discrete productie-omgeving.</span><span class="sxs-lookup"><span data-stu-id="aacac-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="aacac-108">Een productieorder maken</span><span class="sxs-lookup"><span data-stu-id="aacac-108">Create a production order</span></span>
1. <span data-ttu-id="aacac-109">Ga in het navigatievenster naar **Modules > Productiebeheer > Productieorders > Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="aacac-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="aacac-110">Selecteer **Nieuwe productieorder**.</span><span class="sxs-lookup"><span data-stu-id="aacac-110">Select **New production order**.</span></span>
3. <span data-ttu-id="aacac-111">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="aacac-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="aacac-112">Selecteer artikelnummer **D0001**.</span><span class="sxs-lookup"><span data-stu-id="aacac-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="aacac-113">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="aacac-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="aacac-114">Bewerkingen plannen voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="aacac-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="aacac-115">Markeer de nieuwe rij.</span><span class="sxs-lookup"><span data-stu-id="aacac-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="aacac-116">Selecteer in het actievenster de optie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="aacac-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="aacac-117">Selecteert **Bewerkingen plannen**.</span><span class="sxs-lookup"><span data-stu-id="aacac-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="aacac-118">Selecteer in het veld **Planningsrichting** de optie **Verder vanaf planningsdatum**.</span><span class="sxs-lookup"><span data-stu-id="aacac-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="aacac-119">Voer in het veld **Planningsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="aacac-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="aacac-120">Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week.</span><span class="sxs-lookup"><span data-stu-id="aacac-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="aacac-121">Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.</span><span class="sxs-lookup"><span data-stu-id="aacac-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="aacac-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="aacac-122">Select **OK**.</span></span>
7. <span data-ttu-id="aacac-123">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="aacac-123">In the list, mark the selected row.</span></span> <span data-ttu-id="aacac-124">Houd er rekening mee dat de status wordt gewijzigd in **Gepland**.</span><span class="sxs-lookup"><span data-stu-id="aacac-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="aacac-125">Selecteer **Alle taken**.</span><span class="sxs-lookup"><span data-stu-id="aacac-125">Select **All jobs**.</span></span> <span data-ttu-id="aacac-126">Houd er rekening mee dat er geen taken worden gemaakt met bewerkingsplanning.</span><span class="sxs-lookup"><span data-stu-id="aacac-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="aacac-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="aacac-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="aacac-128">Taken plannen voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="aacac-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="aacac-129">Selecteer in het actievenster de optie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="aacac-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="aacac-130">Selecteer **Taken plannen**.</span><span class="sxs-lookup"><span data-stu-id="aacac-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="aacac-131">Selecteer in het veld **Planningsrichting** de optie **Verder vanaf planningsdatum**.</span><span class="sxs-lookup"><span data-stu-id="aacac-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="aacac-132">Voer in het veld **Planningsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="aacac-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="aacac-133">Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week.</span><span class="sxs-lookup"><span data-stu-id="aacac-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="aacac-134">Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.</span><span class="sxs-lookup"><span data-stu-id="aacac-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="aacac-135">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="aacac-135">Select **OK**.</span></span>
6. <span data-ttu-id="aacac-136">Selecteer **Productieorder** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="aacac-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="aacac-137">Selecteer **Alle taken**.</span><span class="sxs-lookup"><span data-stu-id="aacac-137">Select **All jobs**.</span></span> <span data-ttu-id="aacac-138">Merk op dat op basis van de actieve route, 5 taken worden gemaakt met taakplanning.</span><span class="sxs-lookup"><span data-stu-id="aacac-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

