---
title: Overzicht van Workflowsysteem
description: In dit onderwerp wordt het werkstroomsysteem beschreven.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 068f464fe5385486827b2f904114eb663e08b2e8
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697964"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="330c4-103">Overzicht van Workflowsysteem</span><span class="sxs-lookup"><span data-stu-id="330c4-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="330c4-104">In dit onderwerp wordt het werkstroomsysteem beschreven.</span><span class="sxs-lookup"><span data-stu-id="330c4-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="330c4-105">Wat is een workflow?</span><span class="sxs-lookup"><span data-stu-id="330c4-105">What is workflow?</span></span>

<span data-ttu-id="330c4-106">De voorwaarde van *workflow* kan op twee manieren worden gedefinieerd: als een systeem en als bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="330c4-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="330c4-107">Workflow is een systeem</span><span class="sxs-lookup"><span data-stu-id="330c4-107">Workflow is a system</span></span>

<span data-ttu-id="330c4-108">Workflow is een systeem dat wordt uitgevoerd op de Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="330c4-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="330c4-109">Het workflowsysteem bevat functies waarmee u afzonderlijke workflows of bedrijfsprocessen kunt maken.</span><span class="sxs-lookup"><span data-stu-id="330c4-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="330c4-110">Workflow is een bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="330c4-110">Workflow is a business process</span></span>

<span data-ttu-id="330c4-111">Een workflow vertegenwoordigt een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="330c4-111">A workflow represents a business process.</span></span> <span data-ttu-id="330c4-112">Een workflow definieert hoe een document zich door het systeem begeeft of stroomt door aan te geven wie een taak moet voltooien, een beslissing moet nemen of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="330c4-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="330c4-113">De volgende illustratie toont bijvoorbeeld een workflow voor onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="330c4-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Een workflow met elementen die zijn toegewezen aan gebruikers](./media/workflow_user.gif)

<span data-ttu-id="330c4-115">Voor een beter begrip van deze workflow wordt aangenomen dat Sam een onkostenrapport voor 7.000 EUR indient.</span><span class="sxs-lookup"><span data-stu-id="330c4-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="330c4-116">In dit scenario moet Ivan de bonnen beoordelen die Sam naar hem heeft doorstuurt.</span><span class="sxs-lookup"><span data-stu-id="330c4-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="330c4-117">Vervolgens moeten Frank en Sue het onkostenrapport goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="330c4-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="330c4-118">Stel nu dat Sam een onkostennota van EUR 11.000 heeft ingediend.</span><span class="sxs-lookup"><span data-stu-id="330c4-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="330c4-119">In dit scenario moet Ivan de bonnen beoordelen en moeten Frank, Suzan en Anne het onkostenrapport goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="330c4-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="330c4-120">Voordelen van het gebruik van het workflowsysteem</span><span class="sxs-lookup"><span data-stu-id="330c4-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="330c4-121">Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:</span><span class="sxs-lookup"><span data-stu-id="330c4-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="330c4-122">**Consistente processen**: u kunt definiëren hoe specifieke documenten, zoals opdrachten tot inkoop en onkostennota's, worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="330c4-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="330c4-123">Door gebruik van het workflowsysteem garandeert u dat documenten op een consistente, efficiënte manier wordt verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="330c4-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="330c4-124">**Zichtbaarheid van processen**: u kunt de status, historie en prestatiegegevens van workflowexemplaren volgen.</span><span class="sxs-lookup"><span data-stu-id="330c4-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="330c4-125">Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="330c4-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="330c4-126">**Gecentraliseerde werklijst**: gebruikers kunnen een gecentraliseerde werklijst raadplegen die weergeeft welke workflowtaken en -goedkeuringen aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="330c4-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="330c4-127">Workflowinhoud</span><span class="sxs-lookup"><span data-stu-id="330c4-127">Workflow content</span></span>

+ [<span data-ttu-id="330c4-128">Workflowsysteemarchitectuur</span><span class="sxs-lookup"><span data-stu-id="330c4-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="330c4-129">Workflowelementen</span><span class="sxs-lookup"><span data-stu-id="330c4-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="330c4-130">Acties in goedkeuringsprocessen voor workflows</span><span class="sxs-lookup"><span data-stu-id="330c4-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="330c4-131">Overzicht van Workflows maken</span><span class="sxs-lookup"><span data-stu-id="330c4-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="330c4-132">Workfloweigenschappen configureren</span><span class="sxs-lookup"><span data-stu-id="330c4-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="330c4-133">Handmatige taken configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="330c4-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="330c4-134">Geautomatiseerde taken configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="330c4-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="330c4-135">Goedkeuringsprocessen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="330c4-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="330c4-136">Goedkeuringsstappen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="330c4-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="330c4-137">Handmatige beslissingen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="330c4-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="330c4-138">Voorwaardelijke beslissingen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="330c4-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="330c4-139">Parallelle activiteiten in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="330c4-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="330c4-140">Parallelle vertakkingen in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="330c4-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="330c4-141">Workflows voor regelitems configureren</span><span class="sxs-lookup"><span data-stu-id="330c4-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="330c4-142">Veelgestelde vragen over werkstromen</span><span class="sxs-lookup"><span data-stu-id="330c4-142">Workflow FAQ</span></span>](workflow-FAQ.md)
