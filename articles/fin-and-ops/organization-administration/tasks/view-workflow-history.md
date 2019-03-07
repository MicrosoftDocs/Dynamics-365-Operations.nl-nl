---
title: Workflowhistorie bekijken
description: Met de volgende stappen kunt u de status en geschiedenis weergeven van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: a40fe377322e2d64b751f6cace3eda20736cd321
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "309651"
---
# <a name="view-workflow-history"></a><span data-ttu-id="43922-103">Workflowhistorie bekijken</span><span class="sxs-lookup"><span data-stu-id="43922-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43922-104">Met de volgende stappen kunt u de status en geschiedenis weergeven van een document dat voor verwerking en goedkeuring bij het workflowsysteem is ingediend.</span><span class="sxs-lookup"><span data-stu-id="43922-104">Use these steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="43922-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="43922-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="43922-106">Ga naar de Algemeen > Query's > Workflow > Workflowhistorie.</span><span class="sxs-lookup"><span data-stu-id="43922-106">Go to Common > Inquiries > Workflow > Workflow history.</span></span>
    * <span data-ttu-id="43922-107">U kunt dit formulier gebruiken als u de status wilt weergeven van een document dat ter verwerking of goedkeuring is verzonden naar het workflowsysteem.</span><span class="sxs-lookup"><span data-stu-id="43922-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    * <span data-ttu-id="43922-108">De exemplaar-id is de identificatiecode van het workflowexemplaar dat het document verwerkt of heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="43922-108">The Instance ID is      the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="43922-109">De status is de workflowstatus van het document.</span><span class="sxs-lookup"><span data-stu-id="43922-109">The Status is the workflow status of the document.</span></span>  
    * <span data-ttu-id="43922-110">De Workflow-ID is de identificatiecode van de workflow die het document verwerkt of heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="43922-110">The Workflow ID is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="43922-111">De Document-ID is de identificatiecode van het document.</span><span class="sxs-lookup"><span data-stu-id="43922-111">The Document is the identification code of the document.</span></span>  
    * <span data-ttu-id="43922-112">Het Documenttype is het type document dat is ingediend voor verwerking.</span><span class="sxs-lookup"><span data-stu-id="43922-112">The Document type is the type of document that was submitted for processing.</span></span>  
    * <span data-ttu-id="43922-113">De Workflow is de naam van de workflow die het document verwerkt of heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="43922-113">The Workflow is the name of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="43922-114">De Versie is het versienummer van de workflow die het document verwerkt of heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="43922-114">The Version is the version number of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="43922-115">De Aanmaakdatum en -tijd is de datum en het tijdstip waarop het document is ingediend.</span><span class="sxs-lookup"><span data-stu-id="43922-115">The Created date and time is the date and time that the document was submitted.</span></span>  
    * <span data-ttu-id="43922-116">De Verstreken tijd is de hoeveelheid tijd die is verstreken sinds het document is ingediend.</span><span class="sxs-lookup"><span data-stu-id="43922-116">The Elapsed time is the time that has passed since the document was submitted.</span></span>  
    * <span data-ttu-id="43922-117">Met de knop Hervatten kunt u het workflowproces voor het geselecteerde document weer in gang zetten.</span><span class="sxs-lookup"><span data-stu-id="43922-117">The Resume button allows you to resume the workflow process for the selected document.</span></span>  
    * <span data-ttu-id="43922-118">Met de knop Intrekken kunt u het geselecteerde document intrekken, zodat het niet wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="43922-118">The Recall button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="43922-119">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="43922-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="43922-120">Zorg ervoor dat de sectie Werkitems is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="43922-120">Make sure the Work items section is expanded.</span></span>    <span data-ttu-id="43922-121">In deze sectie kunt u werkitems weergeven, die gekoppeld zijn aan het geselecteerde document.</span><span class="sxs-lookup"><span data-stu-id="43922-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="43922-122">Dit kan bijvoorbeeld een taak zijn die moet worden voltooid of een document dat moet worden goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="43922-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    * <span data-ttu-id="43922-123">Met de knop Opnieuw toewijzen opent u een dialoogvenster waarin u een werkitem aan een andere gebruiker kunt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="43922-123">The Reassign button will open a dialog box where you can reassign a work item to another user.</span></span>  
    * <span data-ttu-id="43922-124">Zorg ervoor dat de sectie Details tracering is uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="43922-124">Make sure the Tracking details section is expanded.</span></span>    <span data-ttu-id="43922-125">In deze sectie ziet u de workflowhistorie van het geselecteerde document.</span><span class="sxs-lookup"><span data-stu-id="43922-125">In this section you can view the workflow history of the selected document.</span></span>  

