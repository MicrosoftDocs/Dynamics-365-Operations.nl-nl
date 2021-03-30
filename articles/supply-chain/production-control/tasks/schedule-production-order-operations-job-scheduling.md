---
title: Een productieorder plannen met bewerkingen en taakplanning
description: Dit onderwerp is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ace204f1ec79cc8f9ce10ebfdc3606879e40d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215836"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="bb694-103">Een productieorder plannen met bewerkingen en taakplanning</span><span class="sxs-lookup"><span data-stu-id="bb694-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb694-104">Dit onderwerp is gericht op het plannen van een productieorder met bewerkingsplanning en taakplanning.</span><span class="sxs-lookup"><span data-stu-id="bb694-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="bb694-105">Er worden geen taken gemaakt met bewerkingsplanning, terwijl er wel taken worden gemaakt met taakplanning.</span><span class="sxs-lookup"><span data-stu-id="bb694-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="bb694-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="bb694-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bb694-107">Deze procedure is bedoeld voor de productiemanager, productieplanner of werkvloersupervisor in een discrete productie-omgeving.</span><span class="sxs-lookup"><span data-stu-id="bb694-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="bb694-108">Een productieorder maken</span><span class="sxs-lookup"><span data-stu-id="bb694-108">Create a production order</span></span>
1. <span data-ttu-id="bb694-109">Ga in het navigatievenster naar **Modules > Productiebeheer > Productieorders > Alle productieorders**.</span><span class="sxs-lookup"><span data-stu-id="bb694-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="bb694-110">Selecteer **Nieuwe productieorder**.</span><span class="sxs-lookup"><span data-stu-id="bb694-110">Select **New production order**.</span></span>
3. <span data-ttu-id="bb694-111">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="bb694-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="bb694-112">Selecteer artikelnummer **D0001**.</span><span class="sxs-lookup"><span data-stu-id="bb694-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="bb694-113">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="bb694-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="bb694-114">Bewerkingen plannen voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="bb694-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="bb694-115">Markeer de nieuwe rij.</span><span class="sxs-lookup"><span data-stu-id="bb694-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="bb694-116">Selecteer in het actievenster de optie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="bb694-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="bb694-117">Selecteert **Bewerkingen plannen**.</span><span class="sxs-lookup"><span data-stu-id="bb694-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="bb694-118">Selecteer in het veld **Planningsrichting** de optie **Verder vanaf planningsdatum**.</span><span class="sxs-lookup"><span data-stu-id="bb694-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="bb694-119">Voer in het veld **Planningsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="bb694-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="bb694-120">Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week.</span><span class="sxs-lookup"><span data-stu-id="bb694-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="bb694-121">Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.</span><span class="sxs-lookup"><span data-stu-id="bb694-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="bb694-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb694-122">Select **OK**.</span></span>
7. <span data-ttu-id="bb694-123">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="bb694-123">In the list, mark the selected row.</span></span> <span data-ttu-id="bb694-124">Houd er rekening mee dat de status wordt gewijzigd in **Gepland**.</span><span class="sxs-lookup"><span data-stu-id="bb694-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="bb694-125">Selecteer **Alle taken**.</span><span class="sxs-lookup"><span data-stu-id="bb694-125">Select **All jobs**.</span></span> <span data-ttu-id="bb694-126">Houd er rekening mee dat er geen taken worden gemaakt met bewerkingsplanning.</span><span class="sxs-lookup"><span data-stu-id="bb694-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="bb694-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bb694-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="bb694-128">Taken plannen voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="bb694-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="bb694-129">Selecteer in het actievenster de optie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="bb694-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="bb694-130">Selecteer **Taken plannen**.</span><span class="sxs-lookup"><span data-stu-id="bb694-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="bb694-131">Selecteer in het veld **Planningsrichting** de optie **Verder vanaf planningsdatum**.</span><span class="sxs-lookup"><span data-stu-id="bb694-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="bb694-132">Voer in het veld **Planningsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="bb694-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="bb694-133">Selecteer een datum in de toekomst, bijvoorbeeld vandaag plus één week.</span><span class="sxs-lookup"><span data-stu-id="bb694-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="bb694-134">Met de geselecteerde planningsrichting wordt de productieorder vooruit gepland vanaf deze datum.</span><span class="sxs-lookup"><span data-stu-id="bb694-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="bb694-135">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb694-135">Select **OK**.</span></span>
6. <span data-ttu-id="bb694-136">Selecteer **Productieorder** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="bb694-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="bb694-137">Selecteer **Alle taken**.</span><span class="sxs-lookup"><span data-stu-id="bb694-137">Select **All jobs**.</span></span> <span data-ttu-id="bb694-138">Merk op dat op basis van de actieve route, 5 taken worden gemaakt met taakplanning.</span><span class="sxs-lookup"><span data-stu-id="bb694-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]