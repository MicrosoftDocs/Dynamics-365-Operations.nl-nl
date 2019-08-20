---
title: Een vervangende kanbanregel maken
description: Deze procedure is gericht op het vervangen van een bestaande kanbanregel met een nieuwe kanbanregel op een specifieke datum.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ded10b0972f07f4f86ee32cee596c5e30b15ebd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843764"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="ce1ea-103">Een vervangende kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="ce1ea-103">Create a replacement kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce1ea-104">Deze procedure is gericht op het vervangen van een bestaande kanbanregel met een nieuwe kanbanregel op een specifieke datum.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="ce1ea-105">Dit is handig wanneer wijzigingen in de productiestroom of aanvullingsregels moeten worden gecoördineerd en gepland.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="ce1ea-106">Het demobedrijf dat wordt gebruikt om de procedure te maken, is USMF.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="ce1ea-107">Deze procedure is bedoeld voor de procesingenieur of de waardestroombeheerder wanneer zij de productie voorbereiden voor een gewijzigde productiestroom of een nieuwe aanvullingsregel.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="ce1ea-108">Deze taak vervangt kanbanregel 000022 met een nieuwe regel en verhoogt de maximale hoeveelheid van 48 in 100 voor de nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="ce1ea-109">Selecteer een te vervangen kanbanregel.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="ce1ea-110">Ga naar Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ce1ea-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ce1ea-112">Selecteer kanbanregel 000022.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="ce1ea-113">Een vervangende kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="ce1ea-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="ce1ea-114">Klik op Kanbanregel vervangen.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="ce1ea-115">Typ in het veld Begindatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="ce1ea-116">Selecteer een datum in de toekomst, zoals één week vanaf nu.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="ce1ea-117">Dit is de datum en tijd wanneer de nieuwe kanbanregel actief wordt en de oude kanbanregel wordt vervangen.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="ce1ea-118">Als de kanbanregel het pad in de productiestroom wijzigt, kan een andere activiteit worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="ce1ea-119">In deze procedure wordt de activiteit intact gehouden.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="ce1ea-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-120">Click OK.</span></span>
    * <span data-ttu-id="ce1ea-121">Er wordt een nieuwe kanbanregel gemaakt om kanbanregel 000022 te vervangen.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="ce1ea-122">De ingangsdatum wordt ingesteld op basis van datum die is gekozen bij het vervangen van de kanbanregel.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="ce1ea-123">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ce1ea-124">Selecteer de vervangen kanbanregel 000022.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="ce1ea-125">De vervangen kanbanregel heeft dezelfde datum als de vervaldatum omdat dit de datum is waarop deze vervalt.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="ce1ea-126">Selecteer rij 1 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="ce1ea-127">Selecteer de nieuwe kanbanregel boven in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="ce1ea-128">Dit is de kanbanregel met het hoogste kanbanregelnummer.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="ce1ea-129">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ce1ea-130">Klik op het kanbanregelnummer om de kanbanregel te openen.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="ce1ea-131">Maximumhoeveelheid voor de vervangingskanbanregel wijzigen</span><span class="sxs-lookup"><span data-stu-id="ce1ea-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="ce1ea-132">Stel Maximumhoeveelheid in op '100'.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="ce1ea-133">Vouw het sneltabblad Hoeveelheden uit om het veld Maximumhoeveelheid te bekijken.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="ce1ea-134">Als u de maximale hoeveelheid wijzigt in 100, kunnen maximaal 100 kanbans worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="ce1ea-135">Dit is de laatste stap in deze taak.</span><span class="sxs-lookup"><span data-stu-id="ce1ea-135">This is the last step in this task.</span></span>  

