---
title: Problemen met werkstromen voor inkoopbeheer oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met werkstromen voor inkoopbeheer.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e8274890c581fffc7330538430c9b2ba060041bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999098"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="9cc0f-103">Problemen met werkstromen voor inkoopbeheer oplossen</span><span class="sxs-lookup"><span data-stu-id="9cc0f-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="9cc0f-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met werkstromen voor inkoopbeheer.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="9cc0f-105">Fout bij het opnieuw indienen van een inkooporder bij de werkstroom na een wijziging: "Wijzigingen in inkooporder X zijn alleen toegestaan in een conceptstatus als wijzigingsbeheer is geactiveerd"</span><span class="sxs-lookup"><span data-stu-id="9cc0f-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="9cc0f-106">Dit probleem treedt alleen op als de inkooporder de status *Bevestigd* heeft op het moment dat u wijzigingen aanvraagt.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="9cc0f-107">Als u wijzigingen aanvraagt terwijl de inkooporder de status *Goedgekeurd* heeft, kan de werkstroom gewoon worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="9cc0f-108">Foutomschrijving</span><span class="sxs-lookup"><span data-stu-id="9cc0f-108">Error description</span></span>

<span data-ttu-id="9cc0f-109">De volgende fout treedt op in de werkstroom wanneer een inkooporder opnieuw wordt ingediend na een wijziging:</span><span class="sxs-lookup"><span data-stu-id="9cc0f-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="9cc0f-110">Gestopt (fout): X++-uitzondering: wijzigingen in inkooporder PO0000569 zijn alleen toegestaan in de status Concept wanneer wijzigingsbeheer is geactiveerd op</span><span class="sxs-lookup"><span data-stu-id="9cc0f-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="9cc0f-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="9cc0f-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="9cc0f-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="9cc0f-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="9cc0f-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="9cc0f-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="9cc0f-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="9cc0f-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9cc0f-115">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="9cc0f-115">Issue resolution</span></span>

<span data-ttu-id="9cc0f-116">Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="9cc0f-117">Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="9cc0f-118">Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="9cc0f-119">Het probleem wordt opgelost via [dit Microsoft Knowledge Base-artikel (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="9cc0f-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="9cc0f-120">Een of meer boekhoudingsverdelingen is te veel of te weinig verdeeld.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="9cc0f-121">Dit probleem kan optreden vanwege inconsistenties in inkooporderdistributies.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="9cc0f-122">Als u dit probleem wilt verhelpen en de inkooporder wilt terugzetten op de status *Concept*, gaat u naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Distributie van inkooporder opnieuw instellen**.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="9cc0f-123">Zie het volgende blogbericht voor meer informatie: [Fouten met IO-distributie in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) oplossen.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="9cc0f-124">Als een restant van een levering wordt geannuleerd op een inkooporder waarvoor wijzigingsbeheer is ingeschakeld, krijgt de inkooporder weer de status Bevestigd.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9cc0f-125">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="9cc0f-125">Issue description</span></span>

<span data-ttu-id="9cc0f-126">Als een inkooporder is onderworpen aan wijzigingsbeheer en de enige wijziging die wordt aangevraagd, de annulering van een leveringsrestant op een of meer van de regels is, krijgt de inkooporder weer direct de status *Bevestigd* bevestigd wanneer deze wordt goedgekeurd en wordt er geen journaal gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9cc0f-127">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="9cc0f-127">Issue resolution</span></span>

<span data-ttu-id="9cc0f-128">Annulering van een restant van de levering heeft geen invloed op de inhoud van het bevestigingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="9cc0f-129">Deze functionaliteit moet worden gebruikt wanneer de regel gedeeltelijk is ontvangen en de resterende kwaliteit in de processtap moet worden geannuleerd nadat de inkooporder met de leverancier is bevestigd.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="9cc0f-130">Als dit op de bevestiging van de inkoopordermoet worden weergegeven, moet de hoeveelheid op de inkooporderregel zo worden gecorrigeerd dat de bevestiging is vereist.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="9cc0f-131">Als er niets op de regel is ontvangen, kan de hoeveelheid worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="9cc0f-132">In dit geval is herbevestiging vereist.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="9cc0f-133">Geannuleerde inkooporders worden weergegeven in de conceptlijst in de werkruimte Voorbereiding van inkooporder.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9cc0f-134">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="9cc0f-134">Issue description</span></span>

<span data-ttu-id="9cc0f-135">Nadat u inkooporders hebt geannuleerd die de status *Bevestigd* hadden, worden de geannuleerde inkooporders nog steeds weergegeven in de lijst met conceptinkooporders in de werkruimte **Voorbereiding van inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9cc0f-136">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="9cc0f-136">Issue resolution</span></span>

<span data-ttu-id="9cc0f-137">Dit probleem doet zich alleen voor bij inkooporders waarvoor wijzigingsbeheer van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="9cc0f-138">Deze gebeurtenis treedt op omdat de annulering wordt beschouwd als een wijziging die moet worden goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="9cc0f-139">De goedkeuring kan automatisch door het systeem worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="9cc0f-140">Daarom moet de geannuleerde inkooporder worden ingediend bij de goedkeuringswerkstroom, zodat deze de status *Goedgekeurd* krijgt.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="9cc0f-141">Op dat moment wordt de inkooporder niet meer weergegeven in de lijst met conceptinkooporders in de werkruimte **Voorbereiding van inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="9cc0f-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

