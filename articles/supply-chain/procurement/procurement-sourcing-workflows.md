---
title: Workflows voor inkoopbeheer
description: Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd. U kunt een budgetteringsworkflow maken om een workflow in te stellen.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd9ee69e180f2ff605c4f373a95d2346ccc73c0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807939"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="8a4af-104">Workflows voor inkoopbeheer</span><span class="sxs-lookup"><span data-stu-id="8a4af-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a4af-105">Bepaalde organisaties vereisen dat opdrachten tot inkoop en inkooporders worden goedgekeurd door een andere gebruiker dan de persoon die de transactie heeft ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="8a4af-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="8a4af-106">U kunt een budgetteringsworkflow maken om een workflow in te stellen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="8a4af-107">Een workflow vertegenwoordigt een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="8a4af-107">A workflow represents a business process.</span></span> <span data-ttu-id="8a4af-108">Een werkstroom definieert hoe een document zich door het systeem begeeft en geeft aan wie een taak moet voltooien of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="8a4af-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="8a4af-109">Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:</span><span class="sxs-lookup"><span data-stu-id="8a4af-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="8a4af-110">**Consistente processen**: u kunt het goedkeuringsproces voor specifieke documenten definiëren, zoals opdrachten tot inkoop en onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="8a4af-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="8a4af-111">Door gebruik van het werkstroomsysteem garandeert u dat documenten op een consistente, efficiënte manier worden verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="8a4af-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="8a4af-112">**Zichtbaarheid van processen**: met het werkstroomsysteem kunt u de status, historie en prestatiegegevens van een specifiek workflowexemplaar volgen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="8a4af-113">Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="8a4af-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="8a4af-114">**Gecentraliseerde werklijst**— Gebruikers kunnen een gecentraliseerde werklijst raadplegen die werkstroomtaken en goedkeuringen weergeven die aan hen zijn toegewezen in alle werkstromen waaraan ze deelnemen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="8a4af-115">Dit is beschikbaar op de pagina Werkitems.</span><span class="sxs-lookup"><span data-stu-id="8a4af-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="8a4af-116"> De typen werkstromen die u kunt maken</span><span class="sxs-lookup"><span data-stu-id="8a4af-116">The types of workflows that you can create</span></span>

<span data-ttu-id="8a4af-117">De volgende workflowtypen zijn beschikbaar voor Inkoop en sourcing.</span><span class="sxs-lookup"><span data-stu-id="8a4af-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="8a4af-118">Type</span><span class="sxs-lookup"><span data-stu-id="8a4af-118">Type</span></span> | <span data-ttu-id="8a4af-119">Met dit type kunt u</span><span class="sxs-lookup"><span data-stu-id="8a4af-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="8a4af-120">Controle inkoopbestelopdracht</span><span class="sxs-lookup"><span data-stu-id="8a4af-120">Purchase requisition review</span></span> | <span data-ttu-id="8a4af-121">Controle- en goedkeuringsworkflows maken voor opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="8a4af-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="8a4af-122">Controle van opdracht tot inkoopregel</span><span class="sxs-lookup"><span data-stu-id="8a4af-122">Purchase requisition line review</span></span> | <span data-ttu-id="8a4af-123">Controle- en goedkeuringsworkflows maken voor regels van opdrachten tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="8a4af-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="8a4af-124">Workflow voor inkooporders</span><span class="sxs-lookup"><span data-stu-id="8a4af-124">Purchase order workflow</span></span> | <span data-ttu-id="8a4af-125">Controle- en goedkeuringsworkflows maken voor inkooporders.</span><span class="sxs-lookup"><span data-stu-id="8a4af-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="8a4af-126">Workflow voor inkooporderregels</span><span class="sxs-lookup"><span data-stu-id="8a4af-126">Purchase order line workflow</span></span> | <span data-ttu-id="8a4af-127">Controle- en goedkeuringsworkflows maken voor inkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="8a4af-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="8a4af-128">Workflow voor toepassing voor het toevoegen van leveranciers</span><span class="sxs-lookup"><span data-stu-id="8a4af-128">Vendor add application workflow</span></span> | <span data-ttu-id="8a4af-129">Controle- en goedkeuringsworkflows maken voor het toevoegen van nieuwe leveranciers via leverancieraanvragen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="8a4af-130">Wanneer u een nieuwe werkstroom toevoegt, worden mogelijk ook de volgende verouderde werkstromen weergegeven in het dialoogvenster **Werkstroom maken**.</span><span class="sxs-lookup"><span data-stu-id="8a4af-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="8a4af-131">Deze zijn gerelateerd aan de functionaliteit *bevestiging van ontvangst* die beschikbaar was in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), maar die nu is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="8a4af-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="8a4af-132">Deze werkstromen worden momenteel niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="8a4af-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="8a4af-133">Workflow voor melding van vervaldatum levering</span><span class="sxs-lookup"><span data-stu-id="8a4af-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="8a4af-134">Workflow voor melding van ontvangen factuur</span><span class="sxs-lookup"><span data-stu-id="8a4af-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="8a4af-135">Workflow voor melding van mislukte productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="8a4af-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="8a4af-136">Workflow voor meldingen van de afwijzing van een onbevestigde productontvangstbon</span><span class="sxs-lookup"><span data-stu-id="8a4af-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="8a4af-137">Een werkstroom maken</span><span class="sxs-lookup"><span data-stu-id="8a4af-137">Creating a workflow</span></span>

<span data-ttu-id="8a4af-138">Om een werkstroom te maken, gaat u naar Inkoop en sourcing &gt; Instellingen &gt; Werkstromen voor inkoop en sourcing en maakt u een nieuwe werkstroom door het type werkstroom te selecteren dat u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="8a4af-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="8a4af-139">U kunt in het werkstroomcanvas werkstroomelementen in de ontwerper slepen en de elementen in een stroom koppelen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="8a4af-140">De werkstroomelementen moeten worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="8a4af-140">The workflow elements should be configured.</span></span> <span data-ttu-id="8a4af-141">Voor goedkeurings- en taakwerkstroomelementen kunt u configureren welke deelnemer de actie moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8a4af-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="8a4af-142">Typen deelnemers</span><span class="sxs-lookup"><span data-stu-id="8a4af-142">Types of participants</span></span>

<span data-ttu-id="8a4af-143">U kunt een goedkeuringsstap toewijzen aan de volgende groepen deelnemers.</span><span class="sxs-lookup"><span data-stu-id="8a4af-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="8a4af-144">Gebruikersgroep</span><span class="sxs-lookup"><span data-stu-id="8a4af-144">User group</span></span> | <span data-ttu-id="8a4af-145">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8a4af-145">Description</span></span> |
|---|---|
| <span data-ttu-id="8a4af-146">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="8a4af-146">Participant</span></span> | <span data-ttu-id="8a4af-147">De goedkeuringsstap aan leden van een groep of rol toewijzen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="8a4af-148">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="8a4af-148">Hierarchy</span></span> | <span data-ttu-id="8a4af-149">De goedkeuringsstap aan gebruikers in een specifieke organisatiehiërarchie toewijzen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="8a4af-150">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="8a4af-150">Workflow user</span></span> | <span data-ttu-id="8a4af-151">De goedkeuringsstap aan gebruikers van deze workflow toewijzen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="8a4af-152">Wachtrij</span><span class="sxs-lookup"><span data-stu-id="8a4af-152">Queue</span></span> | <span data-ttu-id="8a4af-153">De goedkeuringsstap aan een wachtrij voor werkitems toewijzen.</span><span class="sxs-lookup"><span data-stu-id="8a4af-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="8a4af-154">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="8a4af-154">User</span></span> | <span data-ttu-id="8a4af-155">Wijs de goedkeuringsstap aan specifieke gebruikers toe.</span><span class="sxs-lookup"><span data-stu-id="8a4af-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="8a4af-156">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8a4af-156">Additional resources</span></span>

- [<span data-ttu-id="8a4af-157">Bedrijfsprocesworkflows voor opdrachten tot inkoop definiëren</span><span class="sxs-lookup"><span data-stu-id="8a4af-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="8a4af-158">Workflow voor opdrachten tot inkoop</span><span class="sxs-lookup"><span data-stu-id="8a4af-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="8a4af-159">Leveranciers onboarden</span><span class="sxs-lookup"><span data-stu-id="8a4af-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]