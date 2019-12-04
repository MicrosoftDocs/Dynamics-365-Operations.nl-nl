---
title: Workflows voor inkoopbeheer
description: Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ceab555bf278ced13d8360956f6db65ba275f8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813449"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="ac759-104">Workflows voor inkoopbeheer</span><span class="sxs-lookup"><span data-stu-id="ac759-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac759-105">Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="ac759-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="ac759-106">U kunt een budgetteringsworkflow maken om een workflow in te stellen.</span><span class="sxs-lookup"><span data-stu-id="ac759-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="ac759-107">Een workflow vertegenwoordigt een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="ac759-107">A workflow represents a business process.</span></span> <span data-ttu-id="ac759-108">Een werkstroom definieert hoe een document zich door het systeem begeeft en geeft aan wie een taak moet voltooien of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="ac759-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ac759-109">Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:</span><span class="sxs-lookup"><span data-stu-id="ac759-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="ac759-110">**Consistente processen**: u kunt het goedkeuringsproces voor specifieke documenten definiëren, zoals opdrachten tot inkoop en onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="ac759-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ac759-111">Door gebruik van het werkstroomsysteem garandeert u dat documenten op een consistente, efficiënte manier worden verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="ac759-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="ac759-112">**Zichtbaarheid van processen**: met het werkstroomsysteem kunt u de status, historie en prestatiegegevens van een specifiek workflowexemplaar volgen.</span><span class="sxs-lookup"><span data-stu-id="ac759-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ac759-113">Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="ac759-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="ac759-114">**Gecentraliseerde werklijst**— Gebruikers kunnen een gecentraliseerde werklijst raadplegen die werkstroomtaken en goedkeuringen weergeven die aan hen zijn toegewezen in alle werkstromen waaraan ze deelnemen.</span><span class="sxs-lookup"><span data-stu-id="ac759-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="ac759-115">Dit is beschikbaar op de pagina Werkitems.</span><span class="sxs-lookup"><span data-stu-id="ac759-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="ac759-116"> De typen werkstromen die u kunt maken</span><span class="sxs-lookup"><span data-stu-id="ac759-116">The types of workflows that you can create</span></span>
<span data-ttu-id="ac759-117">De volgende workflowtypen zijn beschikbaar voor Inkoop en sourcing.</span><span class="sxs-lookup"><span data-stu-id="ac759-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ac759-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ac759-118">**Type**</span></span>                         | <span data-ttu-id="ac759-119">**Met dit type kunt u**</span><span class="sxs-lookup"><span data-stu-id="ac759-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="ac759-120">Controle inkoopbestelopdracht</span><span class="sxs-lookup"><span data-stu-id="ac759-120">Purchase requisition review</span></span>      | <span data-ttu-id="ac759-121">Controle- en goedkeuringsworkflows maken voor opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="ac759-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="ac759-122">Controle van opdracht tot inkoopregel</span><span class="sxs-lookup"><span data-stu-id="ac759-122">Purchase requisition line review</span></span> | <span data-ttu-id="ac759-123">Controle- en goedkeuringsworkflows maken voor regels van opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="ac759-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="ac759-124">Workflow voor inkooporders</span><span class="sxs-lookup"><span data-stu-id="ac759-124">Purchase order workflow</span></span>          | <span data-ttu-id="ac759-125">Controle- en goedkeuringsworkflows maken voor inkooporders.</span><span class="sxs-lookup"><span data-stu-id="ac759-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="ac759-126">Workflow voor inkooporderregels</span><span class="sxs-lookup"><span data-stu-id="ac759-126">Purchase order line workflow</span></span>     | <span data-ttu-id="ac759-127">Controle- en goedkeuringsworkflows maken voor inkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="ac759-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="ac759-128">Workflow voor toepassing voor het toevoegen van leveranciers</span><span class="sxs-lookup"><span data-stu-id="ac759-128">Vendor add application workflow</span></span>  | <span data-ttu-id="ac759-129">Controle- en goedkeuringsworkflows maken voor het toevoegen van nieuwe leveranciers via leverancieraanvragen.</span><span class="sxs-lookup"><span data-stu-id="ac759-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="ac759-130">Een werkstroom maken</span><span class="sxs-lookup"><span data-stu-id="ac759-130">Creating a workflow</span></span>

<span data-ttu-id="ac759-131">Om een werkstroom te maken, gaat u naar Inkoop en sourcing &gt; Instellingen &gt; Werkstromen voor inkoop en sourcing en maakt u een nieuwe werkstroom door het type werkstroom te selecteren dat u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="ac759-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="ac759-132">U kunt in het werkstroomcanvas werkstroomelementen in de ontwerper slepen en de elementen in een stroom koppelen.</span><span class="sxs-lookup"><span data-stu-id="ac759-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="ac759-133">De werkstroomelementen moeten worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="ac759-133">The workflow elements should be configured.</span></span> <span data-ttu-id="ac759-134">Voor goedkeurings- en taakwerkstroomelementen kunt u configureren welke deelnemer de actie moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ac759-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="ac759-135">Typen deelnemers</span><span class="sxs-lookup"><span data-stu-id="ac759-135">Types of participants</span></span>

<span data-ttu-id="ac759-136">U kunt een goedkeuringsstap toewijzen aan de volgende groepen deelnemers.</span><span class="sxs-lookup"><span data-stu-id="ac759-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="ac759-137">Gebruikersgroep</span><span class="sxs-lookup"><span data-stu-id="ac759-137">User group</span></span>    | <span data-ttu-id="ac759-138">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ac759-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="ac759-139">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="ac759-139">Participant</span></span>   | <span data-ttu-id="ac759-140">De goedkeuringsstap aan leden van een groep of rol toewijzen.</span><span class="sxs-lookup"><span data-stu-id="ac759-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="ac759-141">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="ac759-141">Hierarchy</span></span>     | <span data-ttu-id="ac759-142">De goedkeuringsstap aan gebruikers in een specifieke organisatiehiërarchie toewijzen.</span><span class="sxs-lookup"><span data-stu-id="ac759-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="ac759-143">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="ac759-143">Workflow user</span></span> | <span data-ttu-id="ac759-144">De goedkeuringsstap aan gebruikers van deze workflow toewijzen.</span><span class="sxs-lookup"><span data-stu-id="ac759-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="ac759-145">Wachtrij</span><span class="sxs-lookup"><span data-stu-id="ac759-145">Queue</span></span>         | <span data-ttu-id="ac759-146">De goedkeuringsstap aan een wachtrij voor werkitems toewijzen.</span><span class="sxs-lookup"><span data-stu-id="ac759-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="ac759-147">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="ac759-147">User</span></span>          | <span data-ttu-id="ac759-148">Wijs de goedkeuringsstap aan specifieke gebruikers toe.</span><span class="sxs-lookup"><span data-stu-id="ac759-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="ac759-149">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ac759-149">Additional resources</span></span>

- [<span data-ttu-id="ac759-150">Bedrijfsprocesworkflows voor opdrachten tot inkoop definiëren</span><span class="sxs-lookup"><span data-stu-id="ac759-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="ac759-151">Workflow voor opdrachten tot inkoop</span><span class="sxs-lookup"><span data-stu-id="ac759-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="ac759-152">Leveranciers onboarden</span><span class="sxs-lookup"><span data-stu-id="ac759-152">Onboard vendors</span></span>](vendor-onboarding.md)

