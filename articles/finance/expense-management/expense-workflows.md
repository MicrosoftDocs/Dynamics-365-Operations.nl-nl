---
title: Workflows voor onkosten instellen
description: U kunt een werkstroomproces instellen dat wordt gebruikt om documenten voor reizen en onkosten te beoordelen en goed te keuren.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177157"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="afecb-103">Workflows voor onkosten instellen</span><span class="sxs-lookup"><span data-stu-id="afecb-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afecb-104"> U kunt een workflowproces instellen dat wordt gebruikt om documenten voor reizen en onkosten te beoordelen en goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="afecb-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="afecb-105">Documenten waarvoor workflows kunnen worden gedefinieerd, zijn onkostenrapporten, aanvragen voor reizen en aanvragen voor contante voorschotten.</span><span class="sxs-lookup"><span data-stu-id="afecb-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="afecb-106">Een workflow vertegenwoordigt een bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="afecb-106">A workflow represents a business process.</span></span> <span data-ttu-id="afecb-107">Een werkstroom definieert hoe een document zich door het systeem begeeft en geeft aan wie een taak moet voltooien of een document moet goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="afecb-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="afecb-108">Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:</span><span class="sxs-lookup"><span data-stu-id="afecb-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="afecb-109">**Consistente processen**: u kunt het goedkeuringsproces voor specifieke documenten definiëren, zoals opdrachten tot inkoop en onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="afecb-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="afecb-110">Door gebruik van het werkstroomsysteem garandeert u dat documenten op een consistente, efficiënte manier worden verwerkt en goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="afecb-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="afecb-111">Zichtbaarheid van processen: met het werkstroomsysteem kunt u de status, historie en prestatiegegevens van een specifiek workflowexemplaar volgen.</span><span class="sxs-lookup"><span data-stu-id="afecb-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="afecb-112">Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="afecb-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="afecb-113">Gecentraliseerde werklijst: gebruikers kunnen een gecentraliseerde werklijst raadplegen om na te gaan welke werkstroomtaken en -goedkeuringen aan hen zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="afecb-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="afecb-114">**De types workflows die u kunt maken**</span><span class="sxs-lookup"><span data-stu-id="afecb-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="afecb-115">De volgende tabel bevat de workflowtypen die u in **Onkosten** kunt maken.</span><span class="sxs-lookup"><span data-stu-id="afecb-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="afecb-116"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="afecb-117"><strong>Met dit type kunt u</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="afecb-118"><strong>Onkostennota</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="afecb-119">Goedkeuringswerkstromen voor onkostenrapporten maken.</span><span class="sxs-lookup"><span data-stu-id="afecb-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="afecb-120"><strong>Automatische boeking van onkostennota</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="afecb-121">Automatische boeking van werkstromen voor onkostenrapporten maken.</span><span class="sxs-lookup"><span data-stu-id="afecb-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="afecb-122"><strong>Kostenregelartikel</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="afecb-123">Goedkeuringswerkstromen maken voor regelitems op onkostenrapporten.</span><span class="sxs-lookup"><span data-stu-id="afecb-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="afecb-124"><strong>Automatische boeking van uitgavenregelartikel</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="afecb-125">Automatische boekingswerkstromen maken voor regelitems op onkostenrapporten.</span><span class="sxs-lookup"><span data-stu-id="afecb-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="afecb-126"><strong>Reisopdracht</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="afecb-127">Goedkeuringswerkstromen maken voor reisaanvragen.</span><span class="sxs-lookup"><span data-stu-id="afecb-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="afecb-128"><strong>Aanvraag kasvoorschot</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="afecb-129">Goedkeuringswerkstromen maken voor aanvragen voor kasvoorschotten.</span><span class="sxs-lookup"><span data-stu-id="afecb-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="afecb-130"><strong>Btw-teruggave</strong></span><span class="sxs-lookup"><span data-stu-id="afecb-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="afecb-131">Goedkeuringswerkstromen maken voor terugvordering van de belasting over de toegevoegde waarde (BTW).</span><span class="sxs-lookup"><span data-stu-id="afecb-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

