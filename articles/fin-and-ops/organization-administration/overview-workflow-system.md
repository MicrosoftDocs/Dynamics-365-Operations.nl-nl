---
title: Overzicht van Workflowsysteem
description: In dit onderwerp wordt het werkstroomsysteem in Microsoft Dynamics 365 for Finance and Operations beschreven.
author: sericks007
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
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2692b9f3595ab001151f8e53a25010474bcd233
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864787"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="81d53-103">Overzicht van Workflowsysteem</span><span class="sxs-lookup"><span data-stu-id="81d53-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81d53-104">In dit onderwerp wordt het werkstroomsysteem in Microsoft Dynamics 365 for Finance and Operations beschreven.</span><span class="sxs-lookup"><span data-stu-id="81d53-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="81d53-105">Wat is een workflow?</span><span class="sxs-lookup"><span data-stu-id="81d53-105">What is workflow?</span></span>

<span data-ttu-id="81d53-106">De voorwaarde van *workflow* kan op twee manieren worden gedefinieerd: als een systeem en als bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="81d53-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="81d53-107">Workflow is een systeem</span><span class="sxs-lookup"><span data-stu-id="81d53-107">Workflow is a system</span></span>

<span data-ttu-id="81d53-108">Workflow is een systeem dat wordt geïnstalleerd met Finance and Operations en dat draait op de Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="81d53-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="81d53-109">Het workflowsysteem bevat functies waarmee u afzonderlijke workflows of bedrijfsprocessen kunt maken.</span><span class="sxs-lookup"><span data-stu-id="81d53-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="81d53-110">Workflow is een bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="81d53-110">Workflow is a business process</span></span>

<span data-ttu-id="81d53-111">Een workflow vertegenwoordigt een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="81d53-111">A workflow represents a business process.</span></span> <span data-ttu-id="81d53-112">Een workflow definieert hoe een document zich door het systeem begeeft of stroomt door aan te geven wie een taak moet voltooien, een beslissing moet nemen of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="81d53-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="81d53-113">De volgende illustratie toont bijvoorbeeld een workflow voor onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="81d53-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Een workflow met elementen die zijn toegewezen aan gebruikers](./media/workflow_user.gif)

<span data-ttu-id="81d53-115">Voor een beter begrip van deze workflow wordt aangenomen dat Sam een onkostenrapport voor 7.000 EUR indient.</span><span class="sxs-lookup"><span data-stu-id="81d53-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="81d53-116">In dit scenario moet Ivan de bonnen beoordelen die Sam naar hem heeft doorstuurt.</span><span class="sxs-lookup"><span data-stu-id="81d53-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="81d53-117">Vervolgens moeten Frank en Sue het onkostenrapport goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="81d53-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="81d53-118">Stel nu dat Sam een onkostennota van EUR 11.000 heeft ingediend.</span><span class="sxs-lookup"><span data-stu-id="81d53-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="81d53-119">In dit scenario moet Ivan de bonnen beoordelen en moeten Frank, Suzan en Anne het onkostenrapport goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="81d53-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="81d53-120">Voordelen van het gebruik van het workflowsysteem</span><span class="sxs-lookup"><span data-stu-id="81d53-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="81d53-121">Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:</span><span class="sxs-lookup"><span data-stu-id="81d53-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="81d53-122">**Consistente processen**: u kunt definiëren hoe specifieke documenten, zoals opdrachten tot inkoop en onkostennota's, worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="81d53-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="81d53-123">Door gebruik van het workflowsysteem garandeert u dat documenten op een consistente, efficiënte manier wordt verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="81d53-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="81d53-124">**Zichtbaarheid van processen**: u kunt de status, historie en prestatiegegevens van workflowexemplaren volgen.</span><span class="sxs-lookup"><span data-stu-id="81d53-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="81d53-125">Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="81d53-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="81d53-126">**Gecentraliseerde werklijst**: gebruikers kunnen een gecentraliseerde werklijst raadplegen die weergeeft welke workflowtaken en -goedkeuringen aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="81d53-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="81d53-127">Workflowinhoud</span><span class="sxs-lookup"><span data-stu-id="81d53-127">Workflow content</span></span>

+ [<span data-ttu-id="81d53-128">Workflowarchitectuur</span><span class="sxs-lookup"><span data-stu-id="81d53-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="81d53-129">Workflowelementen</span><span class="sxs-lookup"><span data-stu-id="81d53-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="81d53-130">Workflowacties</span><span class="sxs-lookup"><span data-stu-id="81d53-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="81d53-131">Een workflow maken</span><span class="sxs-lookup"><span data-stu-id="81d53-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="81d53-132">Workfloweigenschappen configureren</span><span class="sxs-lookup"><span data-stu-id="81d53-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="81d53-133">Een handmatige taak configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="81d53-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="81d53-134">Een geautomatiseerde taak configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="81d53-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="81d53-135">Een goedkeuringsproces configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="81d53-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="81d53-136">Een goedkeuringsstap configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="81d53-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="81d53-137">Een handmatige beslissing configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="81d53-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="81d53-138">Een voorwaardelijke beslissing configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="81d53-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="81d53-139">Een parallelle activiteit in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="81d53-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="81d53-140">Een parallelle vertakking in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="81d53-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="81d53-141">Een workflow voor regelartikelen configureren</span><span class="sxs-lookup"><span data-stu-id="81d53-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="81d53-142">Veelgestelde vragen workflow</span><span class="sxs-lookup"><span data-stu-id="81d53-142">Workflow FAQ</span></span>](workflow-FAQ.md)
