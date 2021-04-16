---
title: Workflowelementen
description: In dit onderwerp worden de diverse elementen beschreven waaruit een workflow bestaat.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20f320e84d5faaf964585f30581d24996131031c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747146"
---
# <a name="workflow-elements"></a><span data-ttu-id="319f2-103">Workflowelementen</span><span class="sxs-lookup"><span data-stu-id="319f2-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="319f2-104">In dit onderwerp worden de diverse elementen beschreven waaruit een workflow bestaat.</span><span class="sxs-lookup"><span data-stu-id="319f2-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="319f2-105">Een workflow bestaat uit elementen.</span><span class="sxs-lookup"><span data-stu-id="319f2-105">A workflow consists of elements.</span></span> <span data-ttu-id="319f2-106">In de hier volgende secties wordt elk type element beschreven.</span><span class="sxs-lookup"><span data-stu-id="319f2-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="319f2-107">Opdrachten</span><span class="sxs-lookup"><span data-stu-id="319f2-107">Tasks</span></span>

<span data-ttu-id="319f2-108">Een *taak* is een werkeenheid die moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="319f2-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="319f2-109">Er kunnen twee typen taken worden toegevoegd aan een werkstroom: handmatige taken en geautomatiseerde taken.</span><span class="sxs-lookup"><span data-stu-id="319f2-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="319f2-110">Handmatige taak</span><span class="sxs-lookup"><span data-stu-id="319f2-110">Manual task</span></span>

<span data-ttu-id="319f2-111">Een *handmatige taak* is een werkeenheid die moet worden uitgevoerd door een gebruiker.</span><span class="sxs-lookup"><span data-stu-id="319f2-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="319f2-112">Een workflow voor een onkostennota kan bijvoorbeeld handmatige taken omvatten waarbij de toegewezen gebruikers de volgende acties moeten uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="319f2-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="319f2-113">Ontvangstbewijzen controleren die samen met een onkostennota worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="319f2-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="319f2-114">De manager van een werknemer bellen.</span><span class="sxs-lookup"><span data-stu-id="319f2-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="319f2-115">Geautomatiseerde taak</span><span class="sxs-lookup"><span data-stu-id="319f2-115">Automated task</span></span>

<span data-ttu-id="319f2-116">Een *geautomatiseerde taak* is een werkeenheid die moet worden uitgevoerd door het systeem.</span><span class="sxs-lookup"><span data-stu-id="319f2-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="319f2-117">Er is geen menselijke tussenkomst nodig.</span><span class="sxs-lookup"><span data-stu-id="319f2-117">No human interaction is required.</span></span> <span data-ttu-id="319f2-118">Een workflow voor verkooporders kan bijvoorbeeld geautomatiseerde taken omvatten waarbij het systeem de volgende acties moet uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="319f2-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="319f2-119">Een kredietcontrole uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="319f2-119">Perform a credit check.</span></span>
- <span data-ttu-id="319f2-120">Een klantregistratie voor de klant maken als nog geen registratie bestaat.</span><span class="sxs-lookup"><span data-stu-id="319f2-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="319f2-121">Goedkeuringsprocessen</span><span class="sxs-lookup"><span data-stu-id="319f2-121">Approval processes</span></span>

<span data-ttu-id="319f2-122">Een *goedkeuringsproces* bestaat uit afzonderlijke stappen.</span><span class="sxs-lookup"><span data-stu-id="319f2-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="319f2-123">In elke goedkeuringsstap kan de gebruiker de volgende acties uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="319f2-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="319f2-124">Het document goedkeuren</span><span class="sxs-lookup"><span data-stu-id="319f2-124">Approve the document.</span></span>
- <span data-ttu-id="319f2-125">Het document afwijzen</span><span class="sxs-lookup"><span data-stu-id="319f2-125">Reject the document.</span></span>
- <span data-ttu-id="319f2-126">Een wijziging in het document aanvragen</span><span class="sxs-lookup"><span data-stu-id="319f2-126">Request a change to the document.</span></span>
- <span data-ttu-id="319f2-127">Het document aan een andere gebruiker toewijzen voor goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="319f2-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="319f2-128">Elementen van een workflow voor regelartikelen</span><span class="sxs-lookup"><span data-stu-id="319f2-128">Line-item workflow elements</span></span>

<span data-ttu-id="319f2-129">Er kan een workflow worden gemaakt om documenten of de regelitems in een document te verwerken.</span><span class="sxs-lookup"><span data-stu-id="319f2-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="319f2-130">Bijvoorbeeld als u een goedkeuringsworkflow voor urenstaten hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="319f2-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="319f2-131">Deze workflow noemen we de *documentworkflow*. U kunt een element van een *workflow voor regelartikelen* toevoegen aan deze documentworkflow.</span><span class="sxs-lookup"><span data-stu-id="319f2-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="319f2-132">Wanneer het regelitemelement wordt uitgevoerd, wordt elk regelitem in het document ter verwerking aangeboden.</span><span class="sxs-lookup"><span data-stu-id="319f2-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="319f2-133">U wilt mogelijk alle regelitems laten verwerken door de workflow voor regelitems of u wilt dat elk regelitem door een andere workflow voor regelitems wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="319f2-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="319f2-134">Stel dat een werknemer een urenstaat heeft ingediend die op de volgende afbeelding lijkt.</span><span class="sxs-lookup"><span data-stu-id="319f2-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Workflow voor regelartikelen](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="319f2-136">In dit scenario wilt u mogelijk de volgende workflows voor regelartikelen maken:</span><span class="sxs-lookup"><span data-stu-id="319f2-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="319f2-137">**Workflow voor regelitems 1**: deze workflow wordt gebruikt om regelitems te verwerken waarbij de project-id 1111 is.</span><span class="sxs-lookup"><span data-stu-id="319f2-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="319f2-138">**Workflow voor regelitems 2**: deze workflow wordt gebruikt om regelitems te verwerken waarbij de project-id 2222 is.</span><span class="sxs-lookup"><span data-stu-id="319f2-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="319f2-139">**Workflow voor regelitems 3**: deze workflow wordt gebruikt om regelitems te verwerken waarbij de project-id 3333 is.</span><span class="sxs-lookup"><span data-stu-id="319f2-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="319f2-140">Stroombeheerelementen</span><span class="sxs-lookup"><span data-stu-id="319f2-140">Flow-control elements</span></span>

<span data-ttu-id="319f2-141">U kunt de volgende elementen gebruiken om workflows te ontwerpen met afwisselende vertakkingen of vertakkingen die op hetzelfde moment worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="319f2-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="319f2-142">Handmatige beslissing</span><span class="sxs-lookup"><span data-stu-id="319f2-142">Manual decision</span></span>

<span data-ttu-id="319f2-143">Een *handmatige beslissing* is een punt waarop een workflow zich in twee vertakkingen opsplitst.</span><span class="sxs-lookup"><span data-stu-id="319f2-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="319f2-144">Een gebruiker moet een beslissing nemen en deze beslissing systeem bepaalt welke tak wordt gebruikt om het aangeboden document te verwerken.</span><span class="sxs-lookup"><span data-stu-id="319f2-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="319f2-145">Voorwaardelijke beslissing</span><span class="sxs-lookup"><span data-stu-id="319f2-145">Conditional decision</span></span>

<span data-ttu-id="319f2-146">Een *voorwaardelijke beslissing* is eveneens een punt waarop een workflow zich in twee vertakkingen opsplitst.</span><span class="sxs-lookup"><span data-stu-id="319f2-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="319f2-147">Het systeem bepaalt echter welke tak van de workflow wordt gebruikt om het ingediende document te verwerken.</span><span class="sxs-lookup"><span data-stu-id="319f2-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="319f2-148">Om deze beslissing te nemen, evalueert het systeem het document om te bepalen of het aan de opgegeven voorwaarden voldoet.</span><span class="sxs-lookup"><span data-stu-id="319f2-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="319f2-149">Parallelle activiteit</span><span class="sxs-lookup"><span data-stu-id="319f2-149">Parallel activity</span></span>

<span data-ttu-id="319f2-150">Een *parallelle activiteit* is een workflowelement dat twee of meer workflowvertakkingen bevat die op hetzelfde moment worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="319f2-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="319f2-151">Subworkflow</span><span class="sxs-lookup"><span data-stu-id="319f2-151">Subworkflow</span></span>

<span data-ttu-id="319f2-152">Een *subworkflow* is een workflow die wordt uitgevoerd in de context van een andere workflow.</span><span class="sxs-lookup"><span data-stu-id="319f2-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]