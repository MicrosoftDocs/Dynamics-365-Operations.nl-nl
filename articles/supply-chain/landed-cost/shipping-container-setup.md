---
title: Verzendcontainers
description: In dit onderwerp wordt beschreven hoe u verzendcontainers kunt instellen voor de module Francoprijzen.
author: sherry-zheng
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
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833708"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="c385d-103">Verzendingscontainer instellen</span><span class="sxs-lookup"><span data-stu-id="c385d-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c385d-104">In dit onderwerp wordt beschreven hoe u verzendcontainers kunt instellen voor de module **Francoprijzen**.</span><span class="sxs-lookup"><span data-stu-id="c385d-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="c385d-105">Verzendcontainertypen instellen</span><span class="sxs-lookup"><span data-stu-id="c385d-105">Set up shipping container types</span></span>

<span data-ttu-id="c385d-106">Met verzendcontainertypen worden de typen containers bepaald die kunnen worden gebruikt tijdens verzending en transport.</span><span class="sxs-lookup"><span data-stu-id="c385d-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="c385d-107">Als u wilt werken met de verzendcontainertypen, gaat u naar **Francoprijzen \> Containers instellen \> Verzendcontainertypen**.</span><span class="sxs-lookup"><span data-stu-id="c385d-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="c385d-108">Hier kunt u records voor uw containertypen weergeven, toevoegen en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c385d-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="c385d-109">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="c385d-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c385d-110">Veld</span><span class="sxs-lookup"><span data-stu-id="c385d-110">Field</span></span> | <span data-ttu-id="c385d-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c385d-111">Description</span></span> |
|---|---|
| <span data-ttu-id="c385d-112">Type verzendcontainer</span><span class="sxs-lookup"><span data-stu-id="c385d-112">Shipping container type</span></span> | <span data-ttu-id="c385d-113">Voer een unieke identificatienaam/-nummer voor het verzendcontainertype in.</span><span class="sxs-lookup"><span data-stu-id="c385d-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="c385d-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c385d-114">Description</span></span> | <span data-ttu-id="c385d-115">Voer een beschrijving van het verzendcontainertype in.</span><span class="sxs-lookup"><span data-stu-id="c385d-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="c385d-116">Volume</span><span class="sxs-lookup"><span data-stu-id="c385d-116">Volume</span></span> | <span data-ttu-id="c385d-117">Voer het maximale volume in dat is toegestaan in verzendcontainers van dit type.</span><span class="sxs-lookup"><span data-stu-id="c385d-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="c385d-118">Gewicht</span><span class="sxs-lookup"><span data-stu-id="c385d-118">Weight</span></span> | <span data-ttu-id="c385d-119">Voer het maximale gewicht in dat is toegestaan in verzendcontainers van dit type.</span><span class="sxs-lookup"><span data-stu-id="c385d-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="c385d-120">Retourneerbaar</span><span class="sxs-lookup"><span data-stu-id="c385d-120">Returnable</span></span> | <span data-ttu-id="c385d-121">Geef op of verzendingscontainers van dit type naar de leverancier kunnen worden geretourneerd nadat ze tijdens een levering zijn gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c385d-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="c385d-122">Als deze optie is ingesteld op *Ja*, zijn er mogelijk extra kosten van toepassing op het retourneren van containers van dit type naar de haven van oorsprong.</span><span class="sxs-lookup"><span data-stu-id="c385d-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="c385d-123">Verzendcontainers instellen</span><span class="sxs-lookup"><span data-stu-id="c385d-123">Set up shipping containers</span></span>

<span data-ttu-id="c385d-124">U gebruikt verzendcontainerrecords om elke container te identificeren die u tijdens het transport gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c385d-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="c385d-125">Wanneer u een transport maakt, kunt u er een specifieke container voor selecteren in de lijst met alle verzendcontainerrecords die u hier hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c385d-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="c385d-126">Deze functie is vooral nuttig als uw bedrijf eigenaar is van zijn eigen verzendcontainers.</span><span class="sxs-lookup"><span data-stu-id="c385d-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="c385d-127">U hoeft geen verzendcontainernummers in te voeren voor verzendcontainers die slechts één keer worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c385d-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="c385d-128">In plaats daarvan kunt u het verzendcontainernummer toevoegen wanneer u een transport maakt.</span><span class="sxs-lookup"><span data-stu-id="c385d-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="c385d-129">Verzendcontainerrecords worden alleen gebruikt in Francoprijzen.</span><span class="sxs-lookup"><span data-stu-id="c385d-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="c385d-130">Ze zijn niet beschikbaar in de standaardmodule **Transportbeheer** (TMS).</span><span class="sxs-lookup"><span data-stu-id="c385d-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="c385d-131">Als u wilt werken met verzendcontainers, gaat u naar **Francoprijzen \> Containers instellen \> Verzendcontainers**.</span><span class="sxs-lookup"><span data-stu-id="c385d-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="c385d-132">Hier kunt u records voor uw verzendcontainers weergeven, toevoegen en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c385d-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="c385d-133">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="c385d-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c385d-134">Veld</span><span class="sxs-lookup"><span data-stu-id="c385d-134">Field</span></span> | <span data-ttu-id="c385d-135">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c385d-135">Description</span></span> |
|---|---|
| <span data-ttu-id="c385d-136">Verzendcontainer</span><span class="sxs-lookup"><span data-stu-id="c385d-136">Shipping container</span></span> | <span data-ttu-id="c385d-137">Voer een unieke identificatienaam/-nummer voor de verzendcontainer in.</span><span class="sxs-lookup"><span data-stu-id="c385d-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="c385d-138">Type verzendcontainer</span><span class="sxs-lookup"><span data-stu-id="c385d-138">Shipping container type</span></span> | <span data-ttu-id="c385d-139">Selecteer het type verzendcontainer.</span><span class="sxs-lookup"><span data-stu-id="c385d-139">Select the type of shipping container.</span></span> <span data-ttu-id="c385d-140">Zie de sectie [Verzendcontainertypen instellen](#shipping-container-types) eerder in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c385d-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="c385d-141">Het instellen van verzendcontainers is optioneel.</span><span class="sxs-lookup"><span data-stu-id="c385d-141">The shipping container setup is optional.</span></span> <span data-ttu-id="c385d-142">Meestal gebruikt u deze alleen als uw bedrijf zelf verzendcontainers in eigendom heeft of vaak dezelfde verzendcontainers gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c385d-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="c385d-143">Voor het verzenden van verzendcontainernummers worden geen controlecijfers berekend.</span><span class="sxs-lookup"><span data-stu-id="c385d-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="c385d-144">Eenheidstypen instellen</span><span class="sxs-lookup"><span data-stu-id="c385d-144">Set up unit types</span></span>

<span data-ttu-id="c385d-145">Eenheidstypen vormen extra groeperingen en identificatiemethoden voor verzendcontainers.</span><span class="sxs-lookup"><span data-stu-id="c385d-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="c385d-146">Het eenheidstype wordt meestal gebruikt om het type container aan te geven waarin goederen zijn verpakt, zoals pallets of vaten.</span><span class="sxs-lookup"><span data-stu-id="c385d-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="c385d-147">U kunt een eenheidstype selecteren wanneer u een container instelt op de pagina **Alle verzendcontainers**.</span><span class="sxs-lookup"><span data-stu-id="c385d-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="c385d-148">Eenheidstypen worden alleen gebruikt in Francoprijzen.</span><span class="sxs-lookup"><span data-stu-id="c385d-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="c385d-149">Ze zijn niet beschikbaar in TMS.</span><span class="sxs-lookup"><span data-stu-id="c385d-149">They aren't available in TMS.</span></span>

<span data-ttu-id="c385d-150">Als u wilt werken met eenheidstypen, gaat u naar **Francoprijzen \> Containers instellen \> Eenheidstypen**.</span><span class="sxs-lookup"><span data-stu-id="c385d-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="c385d-151">Hier kunt u records voor uw eenheidstypen weergeven, toevoegen en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c385d-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="c385d-152">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="c385d-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c385d-153">Veld</span><span class="sxs-lookup"><span data-stu-id="c385d-153">Field</span></span> | <span data-ttu-id="c385d-154">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c385d-154">Description</span></span> |
|---|---|
| <span data-ttu-id="c385d-155">Eenheidstype</span><span class="sxs-lookup"><span data-stu-id="c385d-155">Unit type</span></span> | <span data-ttu-id="c385d-156">Voer een unieke identificatienaam/-nummer voor het eenheidstype in.</span><span class="sxs-lookup"><span data-stu-id="c385d-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="c385d-157">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c385d-157">Description</span></span> | <span data-ttu-id="c385d-158">Voer een beschrijving van het eenheidstype in.</span><span class="sxs-lookup"><span data-stu-id="c385d-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="c385d-159">Koelingstypen instellen</span><span class="sxs-lookup"><span data-stu-id="c385d-159">Set up refrigeration types</span></span>

<span data-ttu-id="c385d-160">Koelingstypen vormen extra groeperingen en identificatiemethoden voor verzendcontainers (gewoonlijk koelcontainers).</span><span class="sxs-lookup"><span data-stu-id="c385d-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="c385d-161">U kunt een koelingstype selecteren wanneer u een container instelt op de pagina **Alle verzendcontainers**.</span><span class="sxs-lookup"><span data-stu-id="c385d-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="c385d-162">Als u wilt werken met koelingstypen, gaat u naar **Francoprijzen \> Containers instellen \> Koelingstypen**.</span><span class="sxs-lookup"><span data-stu-id="c385d-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="c385d-163">Hier kunt u records voor uw koelingstypen weergeven, toevoegen en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c385d-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="c385d-164">In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.</span><span class="sxs-lookup"><span data-stu-id="c385d-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="c385d-165">Veld</span><span class="sxs-lookup"><span data-stu-id="c385d-165">Field</span></span> | <span data-ttu-id="c385d-166">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c385d-166">Description</span></span> |
|---|---|
| <span data-ttu-id="c385d-167">Koelingstype</span><span class="sxs-lookup"><span data-stu-id="c385d-167">Refrigeration type</span></span> | <span data-ttu-id="c385d-168">Voer een unieke identificatienaam/-nummer voor het koelingstype in.</span><span class="sxs-lookup"><span data-stu-id="c385d-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="c385d-169">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c385d-169">Description</span></span> | <span data-ttu-id="c385d-170">Voer een beschrijving van het koelingstype in.</span><span class="sxs-lookup"><span data-stu-id="c385d-170">Enter a description of the refrigeration type.</span></span> |
