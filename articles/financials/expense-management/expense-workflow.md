---
title: Onkostenworkflow
description: In dit onderwerp wordt uitgelegd hoe u het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations kunt gebruiken om een beoordelingsproces voor onkostenrapporten in Onkostenbeheer in te stellen.
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 21815fccc91961653189f844718712faf573d2d7
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="expense-workflow"></a><span data-ttu-id="ad60b-103">Onkostenworkflow</span><span class="sxs-lookup"><span data-stu-id="ad60b-103">Expense workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad60b-104">U kunt het workflowsysteem in Microsoft Dynamics 365 for Finance and Operations gebruiken om een beoordelingsproces voor onkostenrapporten in Onkostenbeheer in te stellen.</span><span class="sxs-lookup"><span data-stu-id="ad60b-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="ad60b-105">U kunt een workflow instellen die de volgende criteria gebruikt om te bepalen wie onkostenrapporten goedkeurt:</span><span class="sxs-lookup"><span data-stu-id="ad60b-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="ad60b-106">De rapporteringshiërarchie van werknemers en vooraf gedefinieerde goedkeuringslimieten</span><span class="sxs-lookup"><span data-stu-id="ad60b-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="ad60b-107">Goedkeuring op meerdere niveaus die ondersteuning biedt voor tussentijdse fiatteurs en een definitieve fiatteur</span><span class="sxs-lookup"><span data-stu-id="ad60b-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="ad60b-108">Financiële dimensies en de projectverantwoordelijkheid</span><span class="sxs-lookup"><span data-stu-id="ad60b-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="ad60b-109">Toewijzing aan specifieke gebruikers of gebruikersgroepen</span><span class="sxs-lookup"><span data-stu-id="ad60b-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="ad60b-110">Workflowgoedkeuringen kunnen worden gemaakt voor onkostenrapporten, reisopdrachten, vooruitbetalingen in contanten en terugvordering van de belasting toegevoegde waarde (btw).</span><span class="sxs-lookup"><span data-stu-id="ad60b-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="ad60b-111">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="ad60b-111">**Example**</span></span>

<span data-ttu-id="ad60b-112">Het volgende proces is een voorbeeld van een onkostenbeheerwerkstroom voor een onkostennota.</span><span class="sxs-lookup"><span data-stu-id="ad60b-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="ad60b-113">Een werknemer maakt een onkostenrapport en slaat het op.</span><span class="sxs-lookup"><span data-stu-id="ad60b-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="ad60b-114">De werknemer dient het onkostenrapport in ter goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="ad60b-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="ad60b-115">De fiatteur wordt geïdentificeerd op basis van de regels die zijn gedefinieerd wanneer de werkstroom werd ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ad60b-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="ad60b-116">De fiatteur ontvangt een bericht wanneer de onkostennota klaar is om te worden goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="ad60b-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="ad60b-117">De fiatteur bekijkt de onkostennota en controleert of aan de volgende voorwaarden wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="ad60b-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="ad60b-118">De onkosten zijn niet in strijd met onkostenbeleidsregels.</span><span class="sxs-lookup"><span data-stu-id="ad60b-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="ad60b-119">Als onkosten in strijd zijn met een beleidsregel, controleert de fiatteur of de onkostennota een geldige zakelijke reden bevat.</span><span class="sxs-lookup"><span data-stu-id="ad60b-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="ad60b-120">Er zijn elektronische ontvangstbewijzen gekoppeld aan de onkostennota.</span><span class="sxs-lookup"><span data-stu-id="ad60b-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="ad60b-121">De fiatteur keurt de onkostennota goed.</span><span class="sxs-lookup"><span data-stu-id="ad60b-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="ad60b-122">De onkostennota wordt aan de coördinator van Leveranciers toegewezen om te worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="ad60b-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="ad60b-123">Een van de volgende stappen treedt op, afhankelijk van of automatische boeking is geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="ad60b-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="ad60b-124">Als automatische boeking is geconfigureerd, wordt de onkostennota verwerkt voor betaling en wordt de status van de onkostennota bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="ad60b-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="ad60b-125">Als automatische boeking niet is geconfigureerd, controleert de coördinator van Leveranciers of alle oorspronkelijke ontvangsten zijn ingediend en alle ontvangsten zijn uitgelijnd met de onkosten in de onkostennota.</span><span class="sxs-lookup"><span data-stu-id="ad60b-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="ad60b-126">Alle ingevoerde btw-codes op de onkostennota moeten ook worden geverifieerd als correct.</span><span class="sxs-lookup"><span data-stu-id="ad60b-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="ad60b-127">Nadat deze vereisten zijn gecontroleerd, wordt de onkostennota geboekt.</span><span class="sxs-lookup"><span data-stu-id="ad60b-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="ad60b-128">Nadat de onkostennota is geboekt, wordt betaling voor de onkostennota toegestaan en wordt de werknemer vergoed.</span><span class="sxs-lookup"><span data-stu-id="ad60b-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

