---
title: Stappictogrammen en -titels toewijzen voor de mobiele app Warehouse Management
description: In dit onderwerp wordt beschreven hoe u stappictogrammen en -titels kunt toewijzen voor nieuwe of aangepaste taakstromen voor de mobiele app Warehouse Management.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049359"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="0f791-103">Stappictogrammen en -titels toewijzen voor de mobiele app Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="0f791-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f791-104">In dit onderwerp wordt beschreven hoe u stappictogrammen en staptitels kunt toewijzen voor nieuwe of aangepaste taakstromen voor de mobiele app Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="0f791-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="0f791-105">In de volgende afbeeldingen ziet u hoe stappictogrammen en staptitels worden weergegeven in de mobiele app Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="0f791-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="0f791-106">![Voorbeeld van een stappictogram en een staptitel in de mobiele app Warehouse Management](media/step-icon-example.png "Voorbeeld van een stappictogram en een staptitel in de mobiele app Warehouse Management")</span><span class="sxs-lookup"><span data-stu-id="0f791-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="0f791-107">Deze functie inschakelen in uw systeem</span><span class="sxs-lookup"><span data-stu-id="0f791-107">Turn on this feature in your system</span></span>

<span data-ttu-id="0f791-108">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="0f791-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="0f791-109">Beheerders kunnen gebruikmaken van de [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-instellingen om de status van de functie te controleren en deze in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="0f791-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="0f791-110">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="0f791-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0f791-111">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="0f791-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0f791-112">**Functienaam:** *gebruikersinstellingen, pictogrammen en staptitels voor de nieuwe magazijnapp*</span><span class="sxs-lookup"><span data-stu-id="0f791-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="0f791-113">Standaard ID´s, klassen en pictogrammen van stappen</span><span class="sxs-lookup"><span data-stu-id="0f791-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="0f791-114">Elke stap in een taakstroom wordt aangeduid met een stap-ID en elke stap-ID heeft een bijbehorende stapklasse.</span><span class="sxs-lookup"><span data-stu-id="0f791-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="0f791-115">Het stappictogram en de titel worden opgegeven in elke stapklasse.</span><span class="sxs-lookup"><span data-stu-id="0f791-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="0f791-116">Stap-ID´s en stapklassen</span><span class="sxs-lookup"><span data-stu-id="0f791-116">Step IDs and step classes</span></span>

<span data-ttu-id="0f791-117">In de volgende tabel wordt elke stap-ID vermeld die momenteel beschikbaar is, en de bijbehorende stapklasse.</span><span class="sxs-lookup"><span data-stu-id="0f791-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="0f791-118">De besturingselementnaam van het primaire invoerveld wordt gebruikt als de stap-ID.</span><span class="sxs-lookup"><span data-stu-id="0f791-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="0f791-119">Zie de implementatie van de methode `WHSMobileAppStepInfoBuilder.stepId()` in het gedeelte [Voorbeeld: Stappictogrammen en -titels toewijzen voor een aangepaste stroom](#example) verderop in dit onderwerp voor een voorbeeld hoe deze stap-ID´s en -klassen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0f791-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="0f791-120">Stap-id</span><span class="sxs-lookup"><span data-stu-id="0f791-120">Step ID</span></span> | <span data-ttu-id="0f791-121">Stapklasse</span><span class="sxs-lookup"><span data-stu-id="0f791-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="0f791-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="0f791-122">BatchDisposition</span></span> | <span data-ttu-id="0f791-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="0f791-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="0f791-124">Vervoerder</span><span class="sxs-lookup"><span data-stu-id="0f791-124">Carrier</span></span> | <span data-ttu-id="0f791-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="0f791-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="0f791-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-126">CatchWeight</span></span> | <span data-ttu-id="0f791-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="0f791-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="0f791-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="0f791-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="0f791-130">CatchWeightTag</span></span> | <span data-ttu-id="0f791-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="0f791-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="0f791-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="0f791-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="0f791-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="0f791-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="0f791-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="0f791-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="0f791-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="0f791-136">CheckDigit</span></span> | <span data-ttu-id="0f791-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="0f791-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="0f791-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="0f791-138">ClusterId</span></span> | <span data-ttu-id="0f791-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="0f791-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="0f791-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="0f791-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="0f791-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="0f791-142">ClusterPosition</span></span> | <span data-ttu-id="0f791-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="0f791-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="0f791-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="0f791-144">ConfigId</span></span> | <span data-ttu-id="0f791-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="0f791-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="0f791-146">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="0f791-146">Confirmation</span></span> | <span data-ttu-id="0f791-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="0f791-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="0f791-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="0f791-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="0f791-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="0f791-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="0f791-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="0f791-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="0f791-154">ContainerType</span></span> | <span data-ttu-id="0f791-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="0f791-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="0f791-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="0f791-156">CountingReasonCode</span></span> | <span data-ttu-id="0f791-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="0f791-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="0f791-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="0f791-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="0f791-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="0f791-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="0f791-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="0f791-160">CycleCountQty1</span></span> | <span data-ttu-id="0f791-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="0f791-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="0f791-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="0f791-162">CycleCountQty2</span></span> | <span data-ttu-id="0f791-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="0f791-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="0f791-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="0f791-164">CycleCountQty3</span></span> | <span data-ttu-id="0f791-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="0f791-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="0f791-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="0f791-166">CycleCountQty4</span></span> | <span data-ttu-id="0f791-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="0f791-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="0f791-168">Disposition</span><span class="sxs-lookup"><span data-stu-id="0f791-168">Disposition</span></span> | <span data-ttu-id="0f791-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="0f791-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="0f791-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="0f791-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="0f791-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="0f791-172">DriverCheckInId</span></span> | <span data-ttu-id="0f791-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="0f791-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="0f791-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="0f791-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="0f791-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="0f791-176">DriverCheckOutId</span></span> | <span data-ttu-id="0f791-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="0f791-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="0f791-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="0f791-178">ExpDate</span></span> | <span data-ttu-id="0f791-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="0f791-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="0f791-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="0f791-180">FromBatchDisposition</span></span> | <span data-ttu-id="0f791-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="0f791-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="0f791-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="0f791-182">FromInventoryStatus</span></span> | <span data-ttu-id="0f791-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="0f791-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="0f791-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="0f791-184">FullQty</span></span> | <span data-ttu-id="0f791-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="0f791-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="0f791-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="0f791-186">InboundPut</span></span> | <span data-ttu-id="0f791-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="0f791-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="0f791-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="0f791-188">InventBatchId</span></span> | <span data-ttu-id="0f791-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="0f791-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="0f791-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="0f791-190">InventColorId</span></span> | <span data-ttu-id="0f791-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="0f791-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="0f791-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-192">InventLocation</span></span> | <span data-ttu-id="0f791-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="0f791-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="0f791-194">InventLocationId</span></span> | <span data-ttu-id="0f791-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="0f791-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="0f791-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="0f791-196">InventSerialId</span></span> | <span data-ttu-id="0f791-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="0f791-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="0f791-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="0f791-198">InventSizeId</span></span> | <span data-ttu-id="0f791-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="0f791-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="0f791-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="0f791-200">InventStatusId</span></span> | <span data-ttu-id="0f791-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="0f791-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="0f791-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="0f791-202">InventStyleId</span></span> | <span data-ttu-id="0f791-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="0f791-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="0f791-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="0f791-204">InventVersionId</span></span> | <span data-ttu-id="0f791-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="0f791-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="0f791-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="0f791-206">ItemId</span></span> | <span data-ttu-id="0f791-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="0f791-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="0f791-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="0f791-208">ITMContainerID</span></span> | <span data-ttu-id="0f791-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="0f791-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="0f791-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="0f791-210">ITMShipmentID</span></span> | <span data-ttu-id="0f791-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="0f791-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="0f791-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="0f791-212">KanbanCardId</span></span> | <span data-ttu-id="0f791-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="0f791-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="0f791-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="0f791-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="0f791-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="0f791-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="0f791-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="0f791-216">KanbanOrCardId</span></span> | <span data-ttu-id="0f791-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="0f791-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="0f791-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-218">LicensePlateId</span></span> | <span data-ttu-id="0f791-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="0f791-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="0f791-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="0f791-220">LoadId</span></span> | <span data-ttu-id="0f791-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="0f791-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="0f791-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="0f791-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="0f791-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="0f791-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="0f791-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="0f791-224">LocOrLP</span></span> | <span data-ttu-id="0f791-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="0f791-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="0f791-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="0f791-226">LocOrLP_From</span></span> | <span data-ttu-id="0f791-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="0f791-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="0f791-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="0f791-228">LocOrLP_To</span></span> | <span data-ttu-id="0f791-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="0f791-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="0f791-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="0f791-230">LocOrLPCheck</span></span> | <span data-ttu-id="0f791-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="0f791-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="0f791-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-232">LocVerification</span></span> | <span data-ttu-id="0f791-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="0f791-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="0f791-234">LPAdjustIn</span></span> | <span data-ttu-id="0f791-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="0f791-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="0f791-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="0f791-236">LPBreakChildLP</span></span> | <span data-ttu-id="0f791-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="0f791-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="0f791-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="0f791-238">LPBreakParentLP</span></span> | <span data-ttu-id="0f791-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="0f791-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="0f791-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="0f791-240">LPBuildChildLP</span></span> | <span data-ttu-id="0f791-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="0f791-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="0f791-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="0f791-242">LPBuildParentLP</span></span> | <span data-ttu-id="0f791-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="0f791-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="0f791-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-244">LPVerification</span></span> | <span data-ttu-id="0f791-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="0f791-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="0f791-246">MergeContainerId</span></span> | <span data-ttu-id="0f791-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="0f791-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="0f791-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-248">MixedLPLineNum</span></span> | <span data-ttu-id="0f791-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="0f791-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="0f791-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="0f791-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="0f791-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="0f791-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="0f791-252">MovementConfirmCancel</span></span> | <span data-ttu-id="0f791-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="0f791-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="0f791-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-254">NewCaptureWeight</span></span> | <span data-ttu-id="0f791-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="0f791-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="0f791-256">NewQty</span></span> | <span data-ttu-id="0f791-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="0f791-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="0f791-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="0f791-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="0f791-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="0f791-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="0f791-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="0f791-260">OutboundPut</span></span> | <span data-ttu-id="0f791-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="0f791-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="0f791-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-262">OutboundWeight</span></span> | <span data-ttu-id="0f791-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="0f791-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-264">OverridePutNewLocation</span></span> | <span data-ttu-id="0f791-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="0f791-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="0f791-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="0f791-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-268">POLineNum</span></span> | <span data-ttu-id="0f791-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="0f791-270">Inkoopordernummer</span><span class="sxs-lookup"><span data-stu-id="0f791-270">PONum</span></span> | <span data-ttu-id="0f791-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="0f791-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="0f791-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="0f791-272">PositionFull</span></span> | <span data-ttu-id="0f791-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="0f791-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="0f791-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="0f791-274">PositionFullQty</span></span> | <span data-ttu-id="0f791-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="0f791-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="0f791-276">Potentie</span><span class="sxs-lookup"><span data-stu-id="0f791-276">Potency</span></span> | <span data-ttu-id="0f791-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="0f791-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="0f791-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="0f791-278">PrinterName</span></span> | <span data-ttu-id="0f791-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="0f791-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="0f791-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="0f791-280">ProdId</span></span> | <span data-ttu-id="0f791-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="0f791-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="0f791-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="0f791-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="0f791-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-284">ProductConfirmation</span></span> | <span data-ttu-id="0f791-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="0f791-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="0f791-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="0f791-288">Wegzetten</span><span class="sxs-lookup"><span data-stu-id="0f791-288">Put</span></span> | <span data-ttu-id="0f791-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="0f791-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="0f791-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="0f791-290">PutawayClusterId</span></span> | <span data-ttu-id="0f791-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="0f791-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="0f791-292">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0f791-292">Qty</span></span> | <span data-ttu-id="0f791-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="0f791-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="0f791-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="0f791-294">QtyAdjust</span></span> | <span data-ttu-id="0f791-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="0f791-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="0f791-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="0f791-296">QtyShort</span></span> | <span data-ttu-id="0f791-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="0f791-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="0f791-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="0f791-298">QtyToConsume</span></span> | <span data-ttu-id="0f791-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="0f791-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="0f791-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="0f791-300">QtyToPick</span></span> | <span data-ttu-id="0f791-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="0f791-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="0f791-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="0f791-302">QtyToPut</span></span> | <span data-ttu-id="0f791-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="0f791-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="0f791-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="0f791-304">QtyToScrap</span></span> | <span data-ttu-id="0f791-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="0f791-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="0f791-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-306">QtyVerification</span></span> | <span data-ttu-id="0f791-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="0f791-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="0f791-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="0f791-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="0f791-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="0f791-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="0f791-310">ReasonString</span></span> | <span data-ttu-id="0f791-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="0f791-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="0f791-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="0f791-312">RecvLocationId</span></span> | <span data-ttu-id="0f791-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="0f791-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="0f791-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="0f791-314">RemoveContainerId</span></span> | <span data-ttu-id="0f791-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="0f791-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="0f791-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="0f791-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="0f791-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="0f791-318">RMANum</span></span> | <span data-ttu-id="0f791-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="0f791-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="0f791-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="0f791-320">ShortPickReason</span></span> | <span data-ttu-id="0f791-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="0f791-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="0f791-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="0f791-322">SortConOrLP</span></span> | <span data-ttu-id="0f791-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="0f791-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="0f791-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-324">SortLicensePlateId</span></span> | <span data-ttu-id="0f791-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="0f791-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="0f791-326">SortPositionId</span></span> | <span data-ttu-id="0f791-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="0f791-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="0f791-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-328">SortVerification</span></span> | <span data-ttu-id="0f791-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="0f791-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="0f791-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="0f791-330">StartLocationId</span></span> | <span data-ttu-id="0f791-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="0f791-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="0f791-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="0f791-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="0f791-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-334">TargetLicensePlateId</span></span> | <span data-ttu-id="0f791-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="0f791-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-336">TOLineNum</span></span> | <span data-ttu-id="0f791-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="0f791-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-338">ToLocation</span></span> | <span data-ttu-id="0f791-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="0f791-340">TONum</span><span class="sxs-lookup"><span data-stu-id="0f791-340">TONum</span></span> | <span data-ttu-id="0f791-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="0f791-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="0f791-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="0f791-342">ToWarehouse</span></span> | <span data-ttu-id="0f791-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="0f791-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="0f791-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="0f791-344">TransportLoadId</span></span> | <span data-ttu-id="0f791-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="0f791-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="0f791-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="0f791-346">WaveLabelId</span></span> | <span data-ttu-id="0f791-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="0f791-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="0f791-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="0f791-348">WaveLblQty</span></span> | <span data-ttu-id="0f791-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="0f791-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="0f791-350">Gewicht</span><span class="sxs-lookup"><span data-stu-id="0f791-350">Weight</span></span> | <span data-ttu-id="0f791-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="0f791-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="0f791-352">WeightToConsume</span></span> | <span data-ttu-id="0f791-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="0f791-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="0f791-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="0f791-354">WHSAdjustmentType</span></span> | <span data-ttu-id="0f791-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="0f791-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="0f791-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="0f791-356">WHSReceivingException</span></span> | <span data-ttu-id="0f791-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="0f791-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="0f791-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="0f791-358">WHSWorkException</span></span> | <span data-ttu-id="0f791-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="0f791-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="0f791-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="0f791-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="0f791-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="0f791-362">WMSLocationId</span></span> | <span data-ttu-id="0f791-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="0f791-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="0f791-364">WorkId</span></span> | <span data-ttu-id="0f791-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="0f791-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="0f791-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="0f791-366">WorkIdToCancel</span></span> | <span data-ttu-id="0f791-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="0f791-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="0f791-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="0f791-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="0f791-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="0f791-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="0f791-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="0f791-370">WorkPoolId</span></span> | <span data-ttu-id="0f791-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="0f791-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="0f791-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="0f791-372">ZoneId</span></span> | <span data-ttu-id="0f791-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="0f791-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="0f791-374">Beschikbare stappictogrammen</span><span class="sxs-lookup"><span data-stu-id="0f791-374">Available step icons</span></span>

<span data-ttu-id="0f791-375">Het systeem bevat een verzameling standaard stappictogrammen die u ook voor uw aangepaste stappen kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0f791-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="0f791-376">U kunt op dit moment geen aangepaste stappictogrammen uploaden.</span><span class="sxs-lookup"><span data-stu-id="0f791-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="0f791-377">Daarom moet u altijd een van de standaardstappictogrammen selecteren.</span><span class="sxs-lookup"><span data-stu-id="0f791-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="0f791-378">In de volgende tabel wordt elk momenteel beschikbaar standaardstappictogram weergegeven, en de naam ervan.</span><span class="sxs-lookup"><span data-stu-id="0f791-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Informatie over stappictogram"><br><span data-ttu-id="0f791-380">Informatie</span><span class="sxs-lookup"><span data-stu-id="0f791-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Stappictogram Nummerplaat of artikel toevoegen"><br><span data-ttu-id="0f791-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="0f791-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Stappictogram Batchbeschikking"><br><span data-ttu-id="0f791-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="0f791-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Stappictogram Vervoerder"><br><span data-ttu-id="0f791-386">Vervoerder</span><span class="sxs-lookup"><span data-stu-id="0f791-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Stappictogram Catch weight-label"><br><span data-ttu-id="0f791-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="0f791-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Stappictogram Catch weight-label en -gewicht"><br><span data-ttu-id="0f791-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Stappictogram Controlecijfer"><br><span data-ttu-id="0f791-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="0f791-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Stappictogram ID voor in- of uitchecken"><br><span data-ttu-id="0f791-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="0f791-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Stappictogram Onderliggende nummerplaat"><br><span data-ttu-id="0f791-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="0f791-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Stappictogram Cluster-ID"><br><span data-ttu-id="0f791-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="0f791-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Stappictogram Clusterpositie"><br><span data-ttu-id="0f791-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="0f791-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Stappictogram Configuratie-ID"><br><span data-ttu-id="0f791-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="0f791-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Stappictogram Geconfigureerd veld"><br><span data-ttu-id="0f791-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="0f791-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Stappictogram Con. of NP"><br><span data-ttu-id="0f791-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="0f791-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Stappictogram Consolideren van nummerplaat-ID"><br><span data-ttu-id="0f791-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="0f791-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Stappictogram Consolideren tot nummerplaat-ID"><br><span data-ttu-id="0f791-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="0f791-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Stappictogram Containertype"><br><span data-ttu-id="0f791-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="0f791-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Stappictogram Tellen"><br><span data-ttu-id="0f791-414">Tellen</span><span class="sxs-lookup"><span data-stu-id="0f791-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Stappictogram Redencode voor telling"><br><span data-ttu-id="0f791-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="0f791-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Stappictogram Code land van oorsprong"><br><span data-ttu-id="0f791-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="0f791-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Stappictogram Beschikking"><br><span data-ttu-id="0f791-420">Disposition</span><span class="sxs-lookup"><span data-stu-id="0f791-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Stappictogram Gereed"><br><span data-ttu-id="0f791-422">Klaar</span><span class="sxs-lookup"><span data-stu-id="0f791-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Stappictogram Bevestiging van inchecken chauffeur"><br><span data-ttu-id="0f791-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Stappictogram ID voor inchecken chauffeur"><br><span data-ttu-id="0f791-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="0f791-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Stappictogram ID voor uitchecken chauffeur"><br><span data-ttu-id="0f791-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="0f791-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Stappictogram Vervaldatum"><br><span data-ttu-id="0f791-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="0f791-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Stappictogram Veld"><br><span data-ttu-id="0f791-432">Veld</span><span class="sxs-lookup"><span data-stu-id="0f791-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Stappictogram Van batchbeschikking"><br><span data-ttu-id="0f791-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="0f791-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Stappictogram Van voorraadstatus"><br><span data-ttu-id="0f791-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="0f791-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Stappictogram ID-kenmerk"><br><span data-ttu-id="0f791-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="0f791-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Stappictogram ID voorraadbatch"><br><span data-ttu-id="0f791-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="0f791-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Stappictogram ID voorraadkleur"><br><span data-ttu-id="0f791-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="0f791-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Stappictogram Voorraadlocatie"><br><span data-ttu-id="0f791-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Stappictogram Seriële ID voorraad"><br><span data-ttu-id="0f791-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="0f791-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Stappictogram ID voorraadgrootte"><br><span data-ttu-id="0f791-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="0f791-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Stappictogram ID voorraadstatus"><br><span data-ttu-id="0f791-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="0f791-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Stappictogram ID voorraadstijl"><br><span data-ttu-id="0f791-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="0f791-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Stappictogram ID voorraadversie"><br><span data-ttu-id="0f791-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="0f791-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Stappictogram Artikel-ID"><br><span data-ttu-id="0f791-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="0f791-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Stappictogram ID ITM-container"><br><span data-ttu-id="0f791-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="0f791-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Stappictogram ID ITM-zending"><br><span data-ttu-id="0f791-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="0f791-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Stappictogram Kanbankaart-ID"><br><span data-ttu-id="0f791-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="0f791-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Stappictogram Kanban of kaart-ID"><br><span data-ttu-id="0f791-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="0f791-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Stappictogram ID nummerplaat"><br><span data-ttu-id="0f791-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="0f791-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Stappictogram Lading-ID"><br><span data-ttu-id="0f791-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="0f791-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Stappictogram Positionering van locatie nummerplaat"><br><span data-ttu-id="0f791-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="0f791-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Stappictogram Locatie of nummerplaat"><br><span data-ttu-id="0f791-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="0f791-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Stappictogram Controle locatie of nummerplaat"><br><span data-ttu-id="0f791-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="0f791-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Stappictogram Locatie of nummerplaat van"><br><span data-ttu-id="0f791-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="0f791-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Stappictogram Locatie of nummerplaat tot"><br><span data-ttu-id="0f791-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="0f791-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Stappictogram Lang proces voltooid"><br><span data-ttu-id="0f791-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="0f791-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Stappictogram Bovenliggende NP van NP-pauze"><br><span data-ttu-id="0f791-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="0f791-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Stappictogram ID samenvoegcontainer"><br><span data-ttu-id="0f791-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="0f791-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Stappictogram Gecombineerd regelnummer nummerplaat"><br><span data-ttu-id="0f791-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Stappictogram Uitgaand gewicht"><br><span data-ttu-id="0f791-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="0f791-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Stappictogram Eigenaar"><br><span data-ttu-id="0f791-490">Eigenaar</span><span class="sxs-lookup"><span data-stu-id="0f791-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Stappictogram Bovenliggende nummerplaat"><br><span data-ttu-id="0f791-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="0f791-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Pictogram Bevestig"><br><span data-ttu-id="0f791-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="0f791-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Stappictogram Regelnummer inkooporder"><br><span data-ttu-id="0f791-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Stappictogram Inkoopordernummer"><br><span data-ttu-id="0f791-498">Inkoopordernummer</span><span class="sxs-lookup"><span data-stu-id="0f791-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Stappictogram Positie vol"><br><span data-ttu-id="0f791-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="0f791-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Stappictogram Potentie"><br><span data-ttu-id="0f791-502">Potentie</span><span class="sxs-lookup"><span data-stu-id="0f791-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Stappictogram Printernaam"><br><span data-ttu-id="0f791-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="0f791-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Stappictogram Prod.-ID"><br><span data-ttu-id="0f791-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="0f791-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Stappictogram Productbevestiging"><br><span data-ttu-id="0f791-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Stappictogram Wegzetten"><br><span data-ttu-id="0f791-510">Wegzetten</span><span class="sxs-lookup"><span data-stu-id="0f791-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Stappictogram Wegzetcluster-ID"><br><span data-ttu-id="0f791-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="0f791-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Stappictogram Hoeveelheid"><br><span data-ttu-id="0f791-514">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0f791-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Stappictogram Hoeveelheid aanpassen"><br><span data-ttu-id="0f791-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="0f791-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Stappictogram Tekort hoeveelheid"><br><span data-ttu-id="0f791-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="0f791-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Stappictogram Te verbruiken hoeveelheid"><br><span data-ttu-id="0f791-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="0f791-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Stappictogram Weg te zetten hoeveelheid"><br><span data-ttu-id="0f791-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="0f791-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Stappictogram Hoeveelheid voor uitval"><br><span data-ttu-id="0f791-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="0f791-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Stappictogram Bevestiging hoeveelheid"><br><span data-ttu-id="0f791-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="0f791-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Stappictogram Rapporteren als voltooide eindtaak"><br><span data-ttu-id="0f791-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="0f791-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Stappictogram ID ontvangstlocatie"><br><span data-ttu-id="0f791-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="0f791-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Stappictogram ID verwijderen container"><br><span data-ttu-id="0f791-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="0f791-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Stappictogram RMA-nummering"><br><span data-ttu-id="0f791-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="0f791-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Stappictogram Order selecteren"><br><span data-ttu-id="0f791-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="0f791-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Stappictogram Reden voor kort orderverzamelen"><br><span data-ttu-id="0f791-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="0f791-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Stappictogram ID sorteerpositie"><br><span data-ttu-id="0f791-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="0f791-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Stappictogram ID doelnummerplaat"><br><span data-ttu-id="0f791-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Stappictogram Tot regelnummer"><br><span data-ttu-id="0f791-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="0f791-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Stappictogram Tot locatie"><br><span data-ttu-id="0f791-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="0f791-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Stappictogram Tot nummer"><br><span data-ttu-id="0f791-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="0f791-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Stappictogram Tot magazijn"><br><span data-ttu-id="0f791-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="0f791-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Stappictogram ID transportlading"><br><span data-ttu-id="0f791-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="0f791-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Stappictogram ID leveranciersbatch"><br><span data-ttu-id="0f791-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="0f791-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Pictogram ID wavelabel"><br><span data-ttu-id="0f791-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="0f791-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Stappictogram Hoeveelheid wavelabel"><br><span data-ttu-id="0f791-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="0f791-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Stappictogram Gewicht"><br><span data-ttu-id="0f791-560">Gewicht</span><span class="sxs-lookup"><span data-stu-id="0f791-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Stappictogram Te verbruiken gewicht"><br><span data-ttu-id="0f791-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="0f791-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Stappictogram WHS-aanpassingstype"><br><span data-ttu-id="0f791-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="0f791-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Stappictogram WHS-ontvangstuitzondering"><br><span data-ttu-id="0f791-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="0f791-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Stappictogram ID WMS-locatie"><br><span data-ttu-id="0f791-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="0f791-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Stappictogram Werk-ID"><br><span data-ttu-id="0f791-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="0f791-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Stappictogram Te annuleren werk-ID"><br><span data-ttu-id="0f791-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="0f791-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Stappictogram ID nummerplaat werk"><br><span data-ttu-id="0f791-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0f791-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Stappictogram Wegzetcluster ID nummerplaat werk"><br><span data-ttu-id="0f791-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="0f791-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Stappictogram Werkpool"><br><span data-ttu-id="0f791-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="0f791-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Stappictogram Zone-ID"><br><span data-ttu-id="0f791-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="0f791-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="0f791-581">Voorbeeld: stappictogrammen en -titels voor een aangepaste stroom toewijzen</span><span class="sxs-lookup"><span data-stu-id="0f791-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="0f791-582">In dit voorbeeld wordt uitgelegd hoe u stappictogrammen en -titels kunt instellen voor een aangepaste taakstroom.</span><span class="sxs-lookup"><span data-stu-id="0f791-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="0f791-583">Het scenario is gebaseerd op een voorbeeld van een aangepaste taakstroom die wordt gepresenteerd en uitgebreider wordt besproken in het volgende blogbericht: [De mobiele magazijnapp aanpassen](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="0f791-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="0f791-584">De taakstroom werkt als volgt:</span><span class="sxs-lookup"><span data-stu-id="0f791-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="0f791-585">In de app wordt een pagina weergegeven die de werknemer vraagt een container-ID op te geven (bijvoorbeeld door een streepjescode te scannen).</span><span class="sxs-lookup"><span data-stu-id="0f791-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="0f791-586">Als de container-ID geldig is, opent de app een nieuwe pagina waarop de werknemer om het gewicht wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="0f791-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="0f791-587">(Als de container-ID niet geldig is, wordt de werknemer teruggestuurd naar de eerste pagina.)</span><span class="sxs-lookup"><span data-stu-id="0f791-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="0f791-588">Wanneer de werknemer een geldig gewicht invoert, wordt het gewicht opgeslagen en wordt de werknemer naar de eerste pagina teruggestuurd.</span><span class="sxs-lookup"><span data-stu-id="0f791-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="0f791-589">In de volgende afbeelding wordt de volgende taakstroom weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0f791-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="0f791-590">![Taakstroomdiagram](media/step-icons-example-task-flow.png "Taakstroomdiagram")</span><span class="sxs-lookup"><span data-stu-id="0f791-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="0f791-591">Een stapklasse maken voor de containerinvoerpagina</span><span class="sxs-lookup"><span data-stu-id="0f791-591">Create a step class for the container input page</span></span>

<span data-ttu-id="0f791-592">Op de containerinvoerpagina kan de werknemer een container-ID scannen of invoeren.</span><span class="sxs-lookup"><span data-stu-id="0f791-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="0f791-593">![Containerinvoerpagina](media/step-icons-example-container-input.png "Invoerpagina voor container")</span><span class="sxs-lookup"><span data-stu-id="0f791-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="0f791-594">Op de containerinvoerpagina is de besturingselementnaam van het invoerveld `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="0f791-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="0f791-595">Omdat deze besturingselementnaam niet in de [lijst met stap-ID's](#step-ids-classes) staat, wordt er geen bestaande stap gevonden die erop is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="0f791-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="0f791-596">Daarom moet u een stapklasse maken die de stap vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="0f791-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="0f791-597">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="0f791-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="0f791-598">De ID van het stappictogram wordt opgeslagen in het klasselid `defaultStepIcon` en de titel van de stap wordt opgeslagen in het klasselid `defaultStepTitle`.</span><span class="sxs-lookup"><span data-stu-id="0f791-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="0f791-599">Als u een stappictogram wilt toewijzen, stelt u `defaultStepIcon` in op een van de pictogram-ID's die worden vermeld in het gedeelte [Beschikbare stappictogrammen](#step-icons) eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="0f791-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="0f791-600">Een standaard of aangepast stappictogram en -titel gebruiken voor de invoer van gewicht</span><span class="sxs-lookup"><span data-stu-id="0f791-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="0f791-601">Op de invoerpagina voor gewicht kan de werknemer een gewicht invoeren.</span><span class="sxs-lookup"><span data-stu-id="0f791-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="0f791-602">![Invoerpagina voor gewicht](media/step-icons-example-weight-input.png "Invoerpagina voor gewicht")</span><span class="sxs-lookup"><span data-stu-id="0f791-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="0f791-603">Op de invoerpagina voor gewicht is de besturingselementnaam van het invoerveld `Weight`, die in de [lijst met stap-ID´s](#step-ids-classes) staat.</span><span class="sxs-lookup"><span data-stu-id="0f791-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="0f791-604">Daarom hoeft u niets te wijzigen voor deze stap als het stappictogram en de titel die in de klasse `WHSMobileAppStepWeight` zijn gedefinieerd voor u acceptabel zijn.</span><span class="sxs-lookup"><span data-stu-id="0f791-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="0f791-605">Als u voor deze stap echter liever een ander pictogram of andere titel gebruikt, kunt u de methode `stepId()` of de methode `stepInfo()` in de builderklasse overschrijven.</span><span class="sxs-lookup"><span data-stu-id="0f791-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="0f791-606">Elke taakstroom heeft een eigen stapinformatiebuilder.</span><span class="sxs-lookup"><span data-stu-id="0f791-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="0f791-607">De stepId()-methode overschrijven</span><span class="sxs-lookup"><span data-stu-id="0f791-607">Override the stepId() method</span></span>

<span data-ttu-id="0f791-608">In het volgende voorbeeld ziet u één manier waarop u een builderklasse kunt wijzigen door de methode `stepId()` te overschrijven.</span><span class="sxs-lookup"><span data-stu-id="0f791-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="0f791-609">Vervolgens maakt u een stapklasse voor de stap `NewWeight`.</span><span class="sxs-lookup"><span data-stu-id="0f791-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="0f791-610">De code moet lijken op de code voor het voorbeeld `ContainerId` dat eerder in dit onderwerp is weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0f791-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="0f791-611">De stepInfo()-methode overschrijven</span><span class="sxs-lookup"><span data-stu-id="0f791-611">Override the stepInfo() method</span></span>

<span data-ttu-id="0f791-612">In het volgende voorbeeld ziet u één manier waarop u een builderklasse kunt wijzigen door de methode `stepInfo()` te overschrijven.</span><span class="sxs-lookup"><span data-stu-id="0f791-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="0f791-613">U maakt vervolgens een `WHSMobileAppStepInfo`-object en stelt het pictogram en/of de titel rechtstreeks in.</span><span class="sxs-lookup"><span data-stu-id="0f791-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f791-614">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0f791-614">Additional resources</span></span>

- [<span data-ttu-id="0f791-615">De mobiele app Magazijnbeheer installeren en verbinden</span><span class="sxs-lookup"><span data-stu-id="0f791-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="0f791-616">Gebruikersinstellingen mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="0f791-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
