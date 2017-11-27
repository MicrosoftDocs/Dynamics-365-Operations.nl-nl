---
title: Workflows voor inkoopbeheer
description: Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3bf244786e308ebcaee27a16fae378f41086f963
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="340e1-104">Workflows voor inkoopbeheer</span><span class="sxs-lookup"><span data-stu-id="340e1-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="340e1-105">Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="340e1-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="340e1-106">U kunt een budgetteringsworkflow maken om een workflow in te stellen.</span><span class="sxs-lookup"><span data-stu-id="340e1-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="340e1-107">Een workflow vertegenwoordigt een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="340e1-107">A workflow represents a business process.</span></span> <span data-ttu-id="340e1-108">Een werkstroom definieert hoe een document zich door het systeem begeeft en geeft aan wie een taak moet voltooien of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="340e1-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="340e1-109">Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:</span><span class="sxs-lookup"><span data-stu-id="340e1-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="340e1-110">**Consistente processen**: u kunt het goedkeuringsproces voor specifieke documenten definiëren, zoals opdrachten tot inkoop en onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="340e1-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="340e1-111">Door gebruik van het werkstroomsysteem garandeert u dat documenten op een consistente, efficiënte manier worden verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="340e1-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="340e1-112">**Zichtbaarheid van processen**: met het werkstroomsysteem kunt u de status, historie en prestatiegegevens van een specifiek workflowexemplaar volgen.</span><span class="sxs-lookup"><span data-stu-id="340e1-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="340e1-113">Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="340e1-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="340e1-114">**Gecentraliseerde werklijst**— Gebruikers kunnen een gecentraliseerde werklijst raadplegen die werkstroomtaken en goedkeuringen weergeven die aan hen zijn toegewezen in alle werkstromen waaraan ze deelnemen.</span><span class="sxs-lookup"><span data-stu-id="340e1-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="340e1-115">Dit is beschikbaar op de pagina Werkitems.</span><span class="sxs-lookup"><span data-stu-id="340e1-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="340e1-116"> De typen werkstromen die u kunt maken</span><span class="sxs-lookup"><span data-stu-id="340e1-116">The types of workflows that you can create</span></span>
<span data-ttu-id="340e1-117">De volgende workflowtypen zijn beschikbaar voor Inkoop en sourcing.</span><span class="sxs-lookup"><span data-stu-id="340e1-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="340e1-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="340e1-118">**Type**</span></span>                         | <span data-ttu-id="340e1-119">**Met dit type kunt u**</span><span class="sxs-lookup"><span data-stu-id="340e1-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="340e1-120">Controle inkoopbestelopdracht</span><span class="sxs-lookup"><span data-stu-id="340e1-120">Purchase requisition review</span></span>      | <span data-ttu-id="340e1-121">Controleworkflows maken voor opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="340e1-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="340e1-122">Controle van opdracht tot inkoopregel</span><span class="sxs-lookup"><span data-stu-id="340e1-122">Purchase requisition line review</span></span> | <span data-ttu-id="340e1-123">Controleworkflows maken voor regels in opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="340e1-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="340e1-124">Workflow voor inkooporders</span><span class="sxs-lookup"><span data-stu-id="340e1-124">Purchase order workflow</span></span>          | <span data-ttu-id="340e1-125">Controle- en goedkeuringsworkflows maken voor inkooporders.</span><span class="sxs-lookup"><span data-stu-id="340e1-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="340e1-126">Workflow voor inkooporderregels</span><span class="sxs-lookup"><span data-stu-id="340e1-126">Purchase order line workflow</span></span>     | <span data-ttu-id="340e1-127">Controle- en goedkeuringsworkflows maken voor inkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="340e1-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="340e1-128">Een werkstroom maken</span><span class="sxs-lookup"><span data-stu-id="340e1-128">Creating a workflow</span></span>
<span data-ttu-id="340e1-129">Om een werkstroom te maken, gaat u naar Inkoop en sourcing &gt; Instellingen &gt; Werkstromen voor inkoop en sourcing en maakt u een nieuwe werkstroom door het type werkstroom te selecteren dat u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="340e1-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="340e1-130">U kunt in het werkstroomcanvas werkstroomelementen in de ontwerper slepen en de elementen in een stroom koppelen.</span><span class="sxs-lookup"><span data-stu-id="340e1-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="340e1-131">De werkstroomelementen moeten worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="340e1-131">The workflow elements should be configured.</span></span> <span data-ttu-id="340e1-132">Voor goedkeurings- en taakwerkstroomelementen kunt u configureren welke deelnemer de actie moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="340e1-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="340e1-133">Typen deelnemers</span><span class="sxs-lookup"><span data-stu-id="340e1-133">Types of participants</span></span>
----------------------

<span data-ttu-id="340e1-134">U kunt een goedkeuringsstap toewijzen aan de volgende groepen deelnemers.</span><span class="sxs-lookup"><span data-stu-id="340e1-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="340e1-135">Gebruikersgroep</span><span class="sxs-lookup"><span data-stu-id="340e1-135">User group</span></span>    | <span data-ttu-id="340e1-136">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="340e1-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="340e1-137">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="340e1-137">Participant</span></span>   | <span data-ttu-id="340e1-138">De goedkeuringsstap aan leden van een groep of rol toewijzen.</span><span class="sxs-lookup"><span data-stu-id="340e1-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="340e1-139">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="340e1-139">Hierarchy</span></span>     | <span data-ttu-id="340e1-140">De goedkeuringsstap aan gebruikers in een specifieke organisatiehiërarchie toewijzen.</span><span class="sxs-lookup"><span data-stu-id="340e1-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="340e1-141">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="340e1-141">Workflow user</span></span> | <span data-ttu-id="340e1-142">De goedkeuringsstap aan gebruikers van deze workflow toewijzen.</span><span class="sxs-lookup"><span data-stu-id="340e1-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="340e1-143">Wachtrij</span><span class="sxs-lookup"><span data-stu-id="340e1-143">Queue</span></span>         | <span data-ttu-id="340e1-144">De goedkeuringsstap aan een wachtrij voor werkitems toewijzen.</span><span class="sxs-lookup"><span data-stu-id="340e1-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="340e1-145">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="340e1-145">User</span></span>          | <span data-ttu-id="340e1-146">Wijs de goedkeuringsstap aan specifieke gebruikers toe.</span><span class="sxs-lookup"><span data-stu-id="340e1-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="340e1-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="340e1-147">See also</span></span>
--------

[<span data-ttu-id="340e1-148">Bedrijfsprocesworkflows voor opdrachten tot inkoop definiëren</span><span class="sxs-lookup"><span data-stu-id="340e1-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="340e1-149">Werkstroom voor opdrachten tot inkoop</span><span class="sxs-lookup"><span data-stu-id="340e1-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




