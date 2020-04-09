---
title: Werkstroomhistorie bekijken
description: In dit onderwerp worden de stappen beschreven voor het weergeven van de status en geschiedenis van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd5b8d9f3fd2edab50b52a8345f254ebc6b31d0a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140393"
---
# <a name="view-workflow-history"></a><span data-ttu-id="c87ac-103">Werkstroomhistorie bekijken</span><span class="sxs-lookup"><span data-stu-id="c87ac-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c87ac-104">In dit onderwerp worden de stappen beschreven voor het weergeven van de status en geschiedenis van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend.</span><span class="sxs-lookup"><span data-stu-id="c87ac-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="c87ac-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="c87ac-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c87ac-106">Ga naar **navigatiedeelvenster > Modules > Algemeen > Query's > Workflow > Workflowhistorie**.</span><span class="sxs-lookup"><span data-stu-id="c87ac-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="c87ac-107">U kunt dit formulier gebruiken als u de status wilt weergeven van een document dat ter verwerking of goedkeuring is verzonden naar het workflowsysteem.</span><span class="sxs-lookup"><span data-stu-id="c87ac-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="c87ac-108">De optie **Exemplaar-id** bevat de identificatiecode van het workflowexemplaar dat het document verwerkt of heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="c87ac-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="c87ac-109">De optie **Status** geeft de workflowstatus van het document aan.</span><span class="sxs-lookup"><span data-stu-id="c87ac-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="c87ac-110">De optie **Workflow-id** bevat de identificatiecode van de workflow die het document verwerkt of heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="c87ac-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="c87ac-111">De optie **Document** bevat de identificatiecode van het document.</span><span class="sxs-lookup"><span data-stu-id="c87ac-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="c87ac-112">De optie **Documenttype** geeft het type document aan dat is ingediend voor verwerking.</span><span class="sxs-lookup"><span data-stu-id="c87ac-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="c87ac-113">De optie **Workflow** bevat de naam van de workflow die het document verwerkt of heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="c87ac-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="c87ac-114">De optie **Versie** geeft het versienummer aan van de workflow die het document verwerkt of heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="c87ac-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="c87ac-115">De optie **Aanmaakdatum en -tijd** bevat de datum en het tijdstip waarop het document is ingediend.</span><span class="sxs-lookup"><span data-stu-id="c87ac-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="c87ac-116">De optie **Verstreken tijd** geeft de hoeveelheid tijd aan die is verstreken sinds het document is ingediend.</span><span class="sxs-lookup"><span data-stu-id="c87ac-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="c87ac-117">Met de knop **Hervatten** kunt u het workflowproces voor het geselecteerde document weer in gang zetten.</span><span class="sxs-lookup"><span data-stu-id="c87ac-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="c87ac-118">Met de knop **Intrekken** kunt u het geselecteerde document intrekken, zodat het niet wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="c87ac-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="c87ac-119">Selecteer in de lijst de koppeling in de gewenste rij.</span><span class="sxs-lookup"><span data-stu-id="c87ac-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="c87ac-120">Zorg ervoor dat de sectie **Werkitems** is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="c87ac-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="c87ac-121">In deze sectie kunt u werkitems weergeven, die gekoppeld zijn aan het geselecteerde document.</span><span class="sxs-lookup"><span data-stu-id="c87ac-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="c87ac-122">Dit kan bijvoorbeeld een taak zijn die moet worden voltooid of een document dat moet worden goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="c87ac-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="c87ac-123">Met de knop **Opnieuw toewijzen** opent u een dialoogvenster waarin u een werkitem aan een andere gebruiker kunt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="c87ac-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="c87ac-124">Zorg ervoor dat de sectie **Details tracering** is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="c87ac-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="c87ac-125">In deze sectie ziet u de workflowhistorie van het geselecteerde document.</span><span class="sxs-lookup"><span data-stu-id="c87ac-125">In this section you can view the workflow history of the selected document.</span></span>  

