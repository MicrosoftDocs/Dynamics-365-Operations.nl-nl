---
title: Workflowsysteem
description: In dit onderwerp wordt het werkstroomsysteem in Microsoft Dynamics 365 for Finance and Operations beschreven.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
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
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/01/2019
ms.locfileid: "773083"
---
# <a name="workflow-system"></a><span data-ttu-id="1b8f7-103">Workflowsysteem</span><span class="sxs-lookup"><span data-stu-id="1b8f7-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b8f7-104">In dit onderwerp wordt het werkstroomsysteem in Microsoft Dynamics 365 for Finance and Operations beschreven.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="1b8f7-105">Wat is een workflow?</span><span class="sxs-lookup"><span data-stu-id="1b8f7-105">What is workflow?</span></span>

<span data-ttu-id="1b8f7-106">De voorwaarde van *workflow* kan op twee manieren worden gedefinieerd: als een systeem en als bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="1b8f7-107">Workflow is een systeem</span><span class="sxs-lookup"><span data-stu-id="1b8f7-107">Workflow is a system</span></span>

<span data-ttu-id="1b8f7-108">Workflow is een systeem dat wordt geïnstalleerd met Finance and Operations en dat draait op de Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="1b8f7-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="1b8f7-109">Het workflowsysteem bevat functies waarmee u afzonderlijke workflows of bedrijfsprocessen kunt maken.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="1b8f7-110">Workflow is een bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="1b8f7-110">Workflow is a business process</span></span>

<span data-ttu-id="1b8f7-111">Een workflow vertegenwoordigt een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-111">A workflow represents a business process.</span></span> <span data-ttu-id="1b8f7-112">Een workflow definieert hoe een document zich door het systeem begeeft of stroomt door aan te geven wie een taak moet voltooien, een beslissing moet nemen of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="1b8f7-113">De volgende illustratie toont bijvoorbeeld een workflow voor onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Een workflow met elementen die zijn toegewezen aan gebruikers](./media/workflow_user.gif)

<span data-ttu-id="1b8f7-115">Voor een beter begrip van deze workflow wordt aangenomen dat Sam een onkostenrapport voor 7.000 EUR indient.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="1b8f7-116">In dit scenario moet Ivan de bonnen beoordelen die Sam naar hem heeft doorstuurt.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="1b8f7-117">Vervolgens moeten Frank en Sue het onkostenrapport goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="1b8f7-118">Stel nu dat Sam een onkostennota van EUR 11.000 heeft ingediend.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="1b8f7-119">In dit scenario moet Ivan de bonnen beoordelen en moeten Frank, Suzan en Anne het onkostenrapport goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="1b8f7-120">Voordelen van het gebruik van het workflowsysteem</span><span class="sxs-lookup"><span data-stu-id="1b8f7-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="1b8f7-121">Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:</span><span class="sxs-lookup"><span data-stu-id="1b8f7-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="1b8f7-122">**Consistente processen**: u kunt definiëren hoe specifieke documenten, zoals opdrachten tot inkoop en onkostennota's, worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="1b8f7-123">Door gebruik van het workflowsysteem garandeert u dat documenten op een consistente, efficiënte manier wordt verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="1b8f7-124">**Zichtbaarheid van processen**: u kunt de status, historie en prestatiegegevens van workflowexemplaren volgen.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="1b8f7-125">Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="1b8f7-126">**Gecentraliseerde werklijst**: gebruikers kunnen een gecentraliseerde werklijst raadplegen die weergeeft welke workflowtaken en -goedkeuringen aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="1b8f7-127">Workflowinhoud</span><span class="sxs-lookup"><span data-stu-id="1b8f7-127">Workflow content</span></span>

+ [<span data-ttu-id="1b8f7-128">Workflowarchitectuur</span><span class="sxs-lookup"><span data-stu-id="1b8f7-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="1b8f7-129">Workflowelementen</span><span class="sxs-lookup"><span data-stu-id="1b8f7-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="1b8f7-130">Workflowacties</span><span class="sxs-lookup"><span data-stu-id="1b8f7-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="1b8f7-131">Een workflow maken</span><span class="sxs-lookup"><span data-stu-id="1b8f7-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="1b8f7-132">Workfloweigenschappen configureren</span><span class="sxs-lookup"><span data-stu-id="1b8f7-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="1b8f7-133">Een handmatige taak configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="1b8f7-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="1b8f7-134">Een geautomatiseerde taak configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="1b8f7-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="1b8f7-135">Een goedkeuringsproces configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="1b8f7-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="1b8f7-136">Een goedkeuringsstap configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="1b8f7-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="1b8f7-137">Een handmatige beslissing configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="1b8f7-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="1b8f7-138">Een voorwaardelijke beslissing configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="1b8f7-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="1b8f7-139">Een parallelle activiteit in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="1b8f7-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="1b8f7-140">Een parallelle vertakking in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="1b8f7-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="1b8f7-141">Een workflow voor regelartikelen configureren</span><span class="sxs-lookup"><span data-stu-id="1b8f7-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="1b8f7-142">Veelgestelde vragen workflow</span><span class="sxs-lookup"><span data-stu-id="1b8f7-142">Workflow FAQ</span></span>](workflow-FAQ.md)
