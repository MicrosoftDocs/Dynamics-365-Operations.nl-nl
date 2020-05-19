---
title: Dynamics 365 Supply Chain Management (Asset Management) integreren met Dynamics 365 Guides
description: In dit onderwerp wordt uitgelegd hoe u de module Asset Management in Microsoft Dynamics 365 Supply Chain Management kunt integreren met Dynamics 365 Guides om de mixed-reality guides toe te passen in uw dagelijkse service- en onderhoudswerkstromen.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f9ee7f1af8e88f56589c84bfaa063ea005aa353a
ms.sourcegitcommit: 88b4a9d19d16b0ef6543adf7c378a08bf0e07b3a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/29/2020
ms.locfileid: "3311776"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="f849d-103">Dynamics 365 Supply Chain Management (Asset Management) integreren met Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="f849d-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="f849d-104">U kunt de module **Asset Management** in Microsoft Dynamics 365 Supply Chain Management integreren met Dynamics 365 Guides om de mixed-reality guides toe te passen in uw dagelijkse service- en onderhoudswerkstromen.</span><span class="sxs-lookup"><span data-stu-id="f849d-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="f849d-105">Als er een guide is gekoppeld aan een Asset Management-werkorder, ziet een werknemer die de onderhoudscontrolelijst van de werkorder opent in de mobiele app Supply Chain Management (Dynamics 365) dat er een guide beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="f849d-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="f849d-106">De werknemer kan vervolgens de guide zoeken en openen in de Dynamics 365 Guides HoloLens-app.</span><span class="sxs-lookup"><span data-stu-id="f849d-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f849d-107">Vereisten</span><span class="sxs-lookup"><span data-stu-id="f849d-107">Prerequisites</span></span>

<span data-ttu-id="f849d-108">Voordat u guides kunt koppelen aan werkorders voor Asset Management, moet u de volgende vereisten voltooien:</span><span class="sxs-lookup"><span data-stu-id="f849d-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="f849d-109">[Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) versie 10.0.9 of later installeren.</span><span class="sxs-lookup"><span data-stu-id="f849d-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="f849d-110">[Twee keer wegschrijven inschakelen voor Supply Chain Management-apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="f849d-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="f849d-111">[Flight inschakelen](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) voor de functie **MRGuidesFeature**.</span><span class="sxs-lookup"><span data-stu-id="f849d-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="f849d-112">(Voor productieomgevingen moet u eerst een ondersteuningsticket indienen om uw tenant aan de flightinggroep toe te voegen.)</span><span class="sxs-lookup"><span data-stu-id="f849d-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="f849d-113">[Schakel de volgende configuratiesleutels](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) in op de pagina **Licentieconfiguratie**:</span><span class="sxs-lookup"><span data-stu-id="f849d-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="f849d-114">Asset Management \> Asset Management mixed reality</span><span class="sxs-lookup"><span data-stu-id="f849d-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="f849d-115">Mixed reality \> Mixed reality-guide</span><span class="sxs-lookup"><span data-stu-id="f849d-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="f849d-116">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versie 200.0.0.96 of later installeren.</span><span class="sxs-lookup"><span data-stu-id="f849d-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="f849d-117">Dynamics 365 Guides gebruiken met Asset Management</span><span class="sxs-lookup"><span data-stu-id="f849d-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="f849d-118">Als u een guide wilt koppelen, gebruikt u een regel in de onderhoudscontrolelijst in Asset Management.</span><span class="sxs-lookup"><span data-stu-id="f849d-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="f849d-119">U kunt de koppeling maken via een sjabloon voor de onderhoudscontrolelijst, een onderhoudstaaktype of een werkorder, omdat deze drie regels voor onderhoudscontrolelijsten bevatten.</span><span class="sxs-lookup"><span data-stu-id="f849d-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="f849d-120">U kunt tijd besparen met een sjabloon, omdat een sjabloon kan worden gekoppeld aan alle onderhoudstaaktypen die hiervan gebruikmaken.</span><span class="sxs-lookup"><span data-stu-id="f849d-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="f849d-121">Een guide die is gekoppeld aan een onderhoudstaaktype, wordt bijvoorbeeld automatisch gekoppeld aan alle werkorders waarmee het taaktype wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="f849d-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="f849d-122">Anderzijds bestaat een guide die alleen voor die werkorder direct aan een werkorder wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f849d-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="f849d-123">Een guide aan een sjabloon voor onderhoudscontrolelijsten koppelen</span><span class="sxs-lookup"><span data-stu-id="f849d-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="f849d-124">Voer de volgende stappen uit om een guide aan een sjabloon voor onderhoudscontrolelijsten te koppelen.</span><span class="sxs-lookup"><span data-stu-id="f849d-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="f849d-125">Maak een guide met de apps Dynamics 365 Guides voor pc en HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f849d-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="f849d-126">De volgende onderwerpen bevatten informatie over het maken van guides:</span><span class="sxs-lookup"><span data-stu-id="f849d-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="f849d-127">De pc-app gebruiken om een guide te maken</span><span class="sxs-lookup"><span data-stu-id="f849d-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="f849d-128">De HoloLens-app gebruiken om uw hologrammen te plaatsen</span><span class="sxs-lookup"><span data-stu-id="f849d-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="f849d-129">Maak in Supply Chain Management [een sjabloon voor onderhoudscontrolelijsten](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="f849d-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="f849d-130">Koppel de guide die u hebt gemaakt aan een regel voor de onderhoudscontrolelijst in de nieuwe sjabloon voor onderhoudscontrolelijsten:</span><span class="sxs-lookup"><span data-stu-id="f849d-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="f849d-131">Selecteer op het sneltabblad **Regels onderhoudscontrolelijsten** de regel waaraan u de guide wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="f849d-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="f849d-132">Selecteer op het sneltabblad **Gekoppelde guides** de optie **Guide toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f849d-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="f849d-133">![Een guide aan een regel van een onderhoudscontrolelijst koppelen](media/am-guides-integration-add-guide.png "Een guide aan een regel van een onderhoudscontrolelijst koppelen")</span><span class="sxs-lookup"><span data-stu-id="f849d-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="f849d-134">Selecteer in het veld **Naam** een guide en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f849d-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="f849d-135">![Een guide selecteren in het veld Naam](media/am-guides-integration-select-guide.png "Een guide selecteren in het veld Naam")</span><span class="sxs-lookup"><span data-stu-id="f849d-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="f849d-136">De sjabloon voor onderhoudscontrolelijsten koppelen aan een taaktype:</span><span class="sxs-lookup"><span data-stu-id="f849d-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="f849d-137">[Maak een onderhoudstaaktype](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) of selecteer een bestaand type onderhoudstaak.</span><span class="sxs-lookup"><span data-stu-id="f849d-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="f849d-138">Selecteer in het actievenster **Standaardwaarden voor het onderhoudstaaktype**.</span><span class="sxs-lookup"><span data-stu-id="f849d-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="f849d-139">![Knop voor standaardinstellingen voor onderhoudstaaktypen](media/am-guides-integration-job-defaults.png "Knop voor standaardinstellingen voor onderhoudstaaktypen")</span><span class="sxs-lookup"><span data-stu-id="f849d-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="f849d-140">Maak een regel en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f849d-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="f849d-141">![Een regel maken](media/am-guides-integration-add-line.png "Een regel maken")</span><span class="sxs-lookup"><span data-stu-id="f849d-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="f849d-142">Selecteer in het actievenster de optie **Onderhoudscontrolelijst**.</span><span class="sxs-lookup"><span data-stu-id="f849d-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="f849d-143">![Knop Onderhoudscontrolelijst](media/am-guides-integration-maintenance-checklist.png "Knop Onderhoudscontrolelijst")</span><span class="sxs-lookup"><span data-stu-id="f849d-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="f849d-144">Voeg op het sneltabblad **Regels onderhoudscontrolelijsten** een regel toe en wijzig vervolgens de waarde van het veld **Type** in **Sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="f849d-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="f849d-145">![De waarde voor Type wijzigen](media/am-guides-integration-checklist-lines.png "De waarde voor Type wijzigen")</span><span class="sxs-lookup"><span data-stu-id="f849d-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="f849d-146">Selecteer op het sneltabblad **Regeldetails** in het veld **Sjabloon** de sjabloon waaraan u de guide hebt gekoppeld en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f849d-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="f849d-147">![De sjabloon selecteren](media/am-guides-integration-checklist-line-details.png "De sjabloon selecteren")</span><span class="sxs-lookup"><span data-stu-id="f849d-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="f849d-148">[Maak een werkorder](work-orders/manually-created-workorders.md#create-work-order) en selecteer het type onderhoudstaak dat gebruikmaakt van de sjabloon voor onderhoudscontrolelijsten waaraan u de guide hebt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="f849d-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="f849d-149">De guide wordt automatisch gekoppeld aan de werkorder.</span><span class="sxs-lookup"><span data-stu-id="f849d-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="f849d-150">![Een type onderhoudstaak selecteren](media/am-guides-integration-create-work-order.png "Een type onderhoudstaak selecteren")</span><span class="sxs-lookup"><span data-stu-id="f849d-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="f849d-151">Bekijk de guide die aan de werkorder en werknemers is gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="f849d-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="f849d-152">Open de [mobiele werkruimte Asset Management](asset-management-mobile-workspace.md) om de werkorder te openen.</span><span class="sxs-lookup"><span data-stu-id="f849d-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="f849d-153">[Open de onderhoudscontrolelijst](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) voor de werkorder.</span><span class="sxs-lookup"><span data-stu-id="f849d-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="f849d-154">Selecteer een controlelijstregel om de bijbehorende guide weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f849d-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="f849d-155">![Guide gekoppeld met een controlelijstregel](media/am-guides-integration-show-guide.png "Guide gekoppeld met een controlelijstregel")</span><span class="sxs-lookup"><span data-stu-id="f849d-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="f849d-156">Open de guide op HoloLens.</span><span class="sxs-lookup"><span data-stu-id="f849d-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="f849d-157">![De guide on HoloLens openen](media/am-guides-integration-hololens-select.png "De guide op HoloLens openen")</span><span class="sxs-lookup"><span data-stu-id="f849d-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="f849d-158">U kunt een guide ook rechtstreeks aan de controlelijst voor onderhoud van een werkorder of taaktype koppelen.</span><span class="sxs-lookup"><span data-stu-id="f849d-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f849d-159">Er is een bekend probleem dat optreedt wanneer u een sjabloon voor onderhoudscontrolelijsten aan een standaard onderhoudstaaktype koppelt. De guide die aan de sjabloon is gekoppeld, wordt dan niet weergegeven op het sneltabblad **Gekoppelde guides** van de pagina **Standaardinstellingen onderhoudstaaktype**.</span><span class="sxs-lookup"><span data-stu-id="f849d-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="f849d-160">De guide wordt echter weergegeven nadat het taaktype is toegepast op een werkorder op het sneltabblad **Gekoppelde guides**.</span><span class="sxs-lookup"><span data-stu-id="f849d-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="f849d-161">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f849d-161">See also</span></span>

- [<span data-ttu-id="f849d-162">Overzicht van twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="f849d-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="f849d-163">Overzicht van activabeheer</span><span class="sxs-lookup"><span data-stu-id="f849d-163">Asset management overview</span></span>](index.md)
