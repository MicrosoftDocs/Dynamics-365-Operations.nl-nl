---
title: Verzendcontainers
description: In dit onderwerp wordt beschreven hoe u verzendcontainers kunt instellen voor de module Francoprijzen.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500953"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="09455-103">Verzendingscontainer instellen</span><span class="sxs-lookup"><span data-stu-id="09455-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="09455-104">In dit onderwerp wordt beschreven hoe u verzendcontainers kunt instellen voor de module **Francoprijzen**.</span><span class="sxs-lookup"><span data-stu-id="09455-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="09455-105">Verzendcontainertypen instellen</span><span class="sxs-lookup"><span data-stu-id="09455-105">Set up shipping container types</span></span>

<span data-ttu-id="09455-106">Met verzendcontainertypen worden de typen containers bepaald die kunnen worden gebruikt tijdens verzending en transport.</span><span class="sxs-lookup"><span data-stu-id="09455-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="09455-107">Als u wilt werken met de verzendcontainertypen, gaat u naar **Francoprijzen \> Containers instellen \> Verzendcontainertypen**.</span><span class="sxs-lookup"><span data-stu-id="09455-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="09455-108">Hier kunt u records voor uw containertypen weergeven, toevoegen en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="09455-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="09455-109">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="09455-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="09455-110">Veld</span><span class="sxs-lookup"><span data-stu-id="09455-110">Field</span></span> | <span data-ttu-id="09455-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="09455-111">Description</span></span> |
|---|---|
| <span data-ttu-id="09455-112">Type verzendcontainer</span><span class="sxs-lookup"><span data-stu-id="09455-112">Shipping container type</span></span> | <span data-ttu-id="09455-113">Voer een unieke identificatienaam/-nummer voor het verzendcontainertype in.</span><span class="sxs-lookup"><span data-stu-id="09455-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="09455-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="09455-114">Description</span></span> | <span data-ttu-id="09455-115">Voer een beschrijving van het verzendcontainertype in.</span><span class="sxs-lookup"><span data-stu-id="09455-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="09455-116">Volume</span><span class="sxs-lookup"><span data-stu-id="09455-116">Volume</span></span> | <span data-ttu-id="09455-117">Voer het maximale volume in dat is toegestaan in verzendcontainers van dit type.</span><span class="sxs-lookup"><span data-stu-id="09455-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="09455-118">Gewicht</span><span class="sxs-lookup"><span data-stu-id="09455-118">Weight</span></span> | <span data-ttu-id="09455-119">Voer het maximale gewicht in dat is toegestaan in verzendcontainers van dit type.</span><span class="sxs-lookup"><span data-stu-id="09455-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="09455-120">Retourneerbaar</span><span class="sxs-lookup"><span data-stu-id="09455-120">Returnable</span></span> | <span data-ttu-id="09455-121">Geef op of verzendingscontainers van dit type naar de leverancier kunnen worden geretourneerd nadat ze tijdens een levering zijn gebruikt.</span><span class="sxs-lookup"><span data-stu-id="09455-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="09455-122">Als deze optie is ingesteld op *Ja*, zijn er mogelijk extra kosten van toepassing op het retourneren van containers van dit type naar de haven van oorsprong.</span><span class="sxs-lookup"><span data-stu-id="09455-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="09455-123">Verzendcontainers instellen</span><span class="sxs-lookup"><span data-stu-id="09455-123">Set up shipping containers</span></span>

<span data-ttu-id="09455-124">U gebruikt verzendcontainerrecords om elke container te identificeren die u tijdens het transport gebruikt.</span><span class="sxs-lookup"><span data-stu-id="09455-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="09455-125">Wanneer u een transport maakt, kunt u er een specifieke container voor selecteren in de lijst met alle verzendcontainerrecords die u hier hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="09455-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="09455-126">Deze functie is vooral nuttig als uw bedrijf eigenaar is van zijn eigen verzendcontainers.</span><span class="sxs-lookup"><span data-stu-id="09455-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="09455-127">U hoeft geen verzendcontainernummers in te voeren voor verzendcontainers die slechts één keer worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="09455-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="09455-128">In plaats daarvan kunt u het verzendcontainernummer toevoegen wanneer u een transport maakt.</span><span class="sxs-lookup"><span data-stu-id="09455-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="09455-129">Verzendcontainerrecords worden alleen gebruikt in Francoprijzen.</span><span class="sxs-lookup"><span data-stu-id="09455-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="09455-130">Ze zijn niet beschikbaar in de standaardmodule **Transportbeheer** (TMS).</span><span class="sxs-lookup"><span data-stu-id="09455-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="09455-131">Als u wilt werken met verzendcontainers, gaat u naar **Francoprijzen \> Containers instellen \> Verzendcontainers**.</span><span class="sxs-lookup"><span data-stu-id="09455-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="09455-132">Hier kunt u records voor uw verzendcontainers weergeven, toevoegen en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="09455-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="09455-133">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="09455-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="09455-134">Veld</span><span class="sxs-lookup"><span data-stu-id="09455-134">Field</span></span> | <span data-ttu-id="09455-135">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="09455-135">Description</span></span> |
|---|---|
| <span data-ttu-id="09455-136">Verzendcontainer</span><span class="sxs-lookup"><span data-stu-id="09455-136">Shipping container</span></span> | <span data-ttu-id="09455-137">Voer een unieke identificatienaam/-nummer voor de verzendcontainer in.</span><span class="sxs-lookup"><span data-stu-id="09455-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="09455-138">Type verzendcontainer</span><span class="sxs-lookup"><span data-stu-id="09455-138">Shipping container type</span></span> | <span data-ttu-id="09455-139">Selecteer het type verzendcontainer.</span><span class="sxs-lookup"><span data-stu-id="09455-139">Select the type of shipping container.</span></span> <span data-ttu-id="09455-140">Zie de sectie [Verzendcontainertypen instellen](#shipping-container-types) eerder in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="09455-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="09455-141">Het instellen van verzendcontainers is optioneel.</span><span class="sxs-lookup"><span data-stu-id="09455-141">The shipping container setup is optional.</span></span> <span data-ttu-id="09455-142">Meestal gebruikt u deze alleen als uw bedrijf zelf verzendcontainers in eigendom heeft of vaak dezelfde verzendcontainers gebruikt.</span><span class="sxs-lookup"><span data-stu-id="09455-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="09455-143">Voor het verzenden van verzendcontainernummers worden geen controlecijfers berekend.</span><span class="sxs-lookup"><span data-stu-id="09455-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="09455-144">Eenheidstypen instellen</span><span class="sxs-lookup"><span data-stu-id="09455-144">Set up unit types</span></span>

<span data-ttu-id="09455-145">Eenheidstypen vormen extra groeperingen en identificatiemethoden voor verzendcontainers.</span><span class="sxs-lookup"><span data-stu-id="09455-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="09455-146">Het eenheidstype wordt meestal gebruikt om het type container aan te geven waarin goederen zijn verpakt, zoals pallets of vaten.</span><span class="sxs-lookup"><span data-stu-id="09455-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="09455-147">U kunt een eenheidstype selecteren wanneer u een container instelt op de pagina **Alle verzendcontainers**.</span><span class="sxs-lookup"><span data-stu-id="09455-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="09455-148">Eenheidstypen worden alleen gebruikt in Francoprijzen.</span><span class="sxs-lookup"><span data-stu-id="09455-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="09455-149">Ze zijn niet beschikbaar in TMS.</span><span class="sxs-lookup"><span data-stu-id="09455-149">They aren't available in TMS.</span></span>

<span data-ttu-id="09455-150">Als u wilt werken met eenheidstypen, gaat u naar **Francoprijzen \> Containers instellen \> Eenheidstypen**.</span><span class="sxs-lookup"><span data-stu-id="09455-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="09455-151">Hier kunt u records voor uw eenheidstypen weergeven, toevoegen en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="09455-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="09455-152">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="09455-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="09455-153">Veld</span><span class="sxs-lookup"><span data-stu-id="09455-153">Field</span></span> | <span data-ttu-id="09455-154">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="09455-154">Description</span></span> |
|---|---|
| <span data-ttu-id="09455-155">Eenheidstype</span><span class="sxs-lookup"><span data-stu-id="09455-155">Unit type</span></span> | <span data-ttu-id="09455-156">Voer een unieke identificatienaam/-nummer voor het eenheidstype in.</span><span class="sxs-lookup"><span data-stu-id="09455-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="09455-157">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="09455-157">Description</span></span> | <span data-ttu-id="09455-158">Voer een beschrijving van het eenheidstype in.</span><span class="sxs-lookup"><span data-stu-id="09455-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="09455-159">Koelingstypen instellen</span><span class="sxs-lookup"><span data-stu-id="09455-159">Set up refrigeration types</span></span>

<span data-ttu-id="09455-160">Koelingstypen vormen extra groeperingen en identificatiemethoden voor verzendcontainers (gewoonlijk koelcontainers).</span><span class="sxs-lookup"><span data-stu-id="09455-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="09455-161">U kunt een koelingstype selecteren wanneer u een container instelt op de pagina **Alle verzendcontainers**.</span><span class="sxs-lookup"><span data-stu-id="09455-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="09455-162">Als u wilt werken met koelingstypen, gaat u naar **Francoprijzen \> Containers instellen \> Koelingstypen**.</span><span class="sxs-lookup"><span data-stu-id="09455-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="09455-163">Hier kunt u records voor uw koelingstypen weergeven, toevoegen en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="09455-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="09455-164">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="09455-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="09455-165">Veld</span><span class="sxs-lookup"><span data-stu-id="09455-165">Field</span></span> | <span data-ttu-id="09455-166">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="09455-166">Description</span></span> |
|---|---|
| <span data-ttu-id="09455-167">Koelingstype</span><span class="sxs-lookup"><span data-stu-id="09455-167">Refrigeration type</span></span> | <span data-ttu-id="09455-168">Voer een unieke identificatienaam/-nummer voor het koelingstype in.</span><span class="sxs-lookup"><span data-stu-id="09455-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="09455-169">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="09455-169">Description</span></span> | <span data-ttu-id="09455-170">Voer een beschrijving van het koelingstype in.</span><span class="sxs-lookup"><span data-stu-id="09455-170">Enter a description of the refrigeration type.</span></span> |
