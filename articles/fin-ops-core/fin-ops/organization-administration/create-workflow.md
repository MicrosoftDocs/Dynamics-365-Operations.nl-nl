---
title: Overzicht van Workflows maken
description: In dit onderwerp wordt uitgelegd hoe u een workflow maakt.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 2168b33c8495eab61ec0c8262b042cd16420031c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190092"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="1ee7a-103">Overzicht van Workflows maken</span><span class="sxs-lookup"><span data-stu-id="1ee7a-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ee7a-104">In dit onderwerp wordt uitgelegd hoe u een workflow maakt.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="1ee7a-105">Open de workfloweditor</span><span class="sxs-lookup"><span data-stu-id="1ee7a-105">Open the workflow editor</span></span>

<span data-ttu-id="1ee7a-106">De module waarin u werkt, bepaalt de typen werkstroom die u kunt maken.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="1ee7a-107">Volg deze stappen om het workflowtype te selecteren dat u wilt maken en open de workfloweditor.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="1ee7a-108">Open de module waarvoor u een nieuwe workflow wilt maken.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="1ee7a-109">Als u bijvoorbeeld een workflow voor opdrachten tot inkoop wilt maken, klikt u op **Inkoopbeheer**.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="1ee7a-110">Klik op **Instellen** &gt; **\[Naam van module\] workflows**.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="1ee7a-111">Klik op **Nieuw** in de lijstpagina die verschijnt in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="1ee7a-112">Selecteer op de pagina **Workflow maken** het type workflow en klik vervolgens op **Workflow maken**.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="1ee7a-113">De workfloweditor verschijnt.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-113">The workflow editor appears.</span></span> <span data-ttu-id="1ee7a-114">U kunt nu de volgende procedures gebruiken om de workflow te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="1ee7a-115">Sleep workflowelementen op het tekenpapier</span><span class="sxs-lookup"><span data-stu-id="1ee7a-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="1ee7a-116">Het gebied **Workflowelementen** van de workfloweditor bevat de elementen die u aan uw workflow kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="1ee7a-117">Sleep de elementen die u aan de workflow wilt toevoegen naar het tekenpapier.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="1ee7a-118">De elementen verbinden</span><span class="sxs-lookup"><span data-stu-id="1ee7a-118">Connect the elements</span></span>

<span data-ttu-id="1ee7a-119">Om het ene workflowelement met het andere te verbinden, houdt u de aanwijzer boven een element tot er verbindingspunten verschijnen.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="1ee7a-120">Klik op een verbindingspunt en sleep het naar een ander element.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="1ee7a-121">Zorg ervoor dat u alle elementen verbindt.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="1ee7a-122">De eigenschappen van de workflow configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="1ee7a-123">Volg deze stappen om de eigenschappen van de workflow te configureren.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="1ee7a-124">Klik op het tekenpapier om ervoor te zorgen dat er geen workflowelement is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="1ee7a-125">Klik op **Eigenschappen** om het formulier **Eigenschappen** voor de workflow te openen.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="1ee7a-126">Volg de procedures in het onderwerp [De eigenschappen van een workflow configureren](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1ee7a-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="1ee7a-127">De elementen van de workflow configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="1ee7a-128">Configureer elk element dat u op het tekenpapier hebt gesleept.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="1ee7a-129">Zie de volgende onderwerpen voor meer informatie over het configureren van elk workflowelement:</span><span class="sxs-lookup"><span data-stu-id="1ee7a-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="1ee7a-130">Een handmatige taak configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="1ee7a-131">Een geautomatiseerde taak configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="1ee7a-132">Een goedkeuringsproces configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="1ee7a-133">Een goedkeuringsstap configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="1ee7a-134">Een handmatige beslissing configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="1ee7a-135">Een voorwaardelijke beslissing configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="1ee7a-136">Een parallelle activiteit configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="1ee7a-137">Een parallelle vertakking configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="1ee7a-138">Een workflow voor regelartikelen configureren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="1ee7a-139">Eventuele fouten of waarschuwingen oplossen</span><span class="sxs-lookup"><span data-stu-id="1ee7a-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="1ee7a-140">Het deelvenster **Fouten en waarschuwingen** onderaan in de workfloweditor geeft berichten weer die voor de workflow zijn gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="1ee7a-141">Om het element te vinden waar een fout of waarschuwing optreedt, dubbelklikt u op het fout- of waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="1ee7a-142">U moet alle fouten en waarschuwingen oplossen voordat u de workflow kunt activeren.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="1ee7a-143">De workflow opslaan en activeren</span><span class="sxs-lookup"><span data-stu-id="1ee7a-143">Save and activate the workflow</span></span>

<span data-ttu-id="1ee7a-144">Wanneer u klaar bent om de workflow op te slaan en te activeren, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="1ee7a-145">Klik op **Opslaan en sluiten** om de workflow te sluiten en de pagina **Workflow opslaan** te openen.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="1ee7a-146">Voer opmerkingen in over de wijzigingen die u in de workflow hebt aangebracht en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="1ee7a-147">Als alle fouten en waarschuwingen zijn opgelost, verschijnt de pagina **Workflow activeren**.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="1ee7a-148">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="1ee7a-148">Select one of the following options:</span></span>

    - <span data-ttu-id="1ee7a-149">Om deze versie van de workflow te activeren, klikt u op **De nieuwe versie activeren**.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="1ee7a-150">Wanneer een workflow actief is, kunnen gebruiker documenten ter verwerking bij de workflow aanbieden.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="1ee7a-151">Als u deze versie niet wilt activeren, klikt op **De nieuwe versie niet activeren**.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="1ee7a-152">U kunt de workflow later activeren.</span><span class="sxs-lookup"><span data-stu-id="1ee7a-152">You can activate the workflow later.</span></span>