---
title: Planning met negatieve voorhanden hoeveelheden
description: In dit onderwerp wordt uitgelegd hoe negatieve voorhanden voorraad wordt verwerkt wanneer u planningsoptimalisatie gebruikt.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ca12d13f7318f649cb1dbc0f7c3cf56502c9d3ea
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077479"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="f6f6e-103">Planning met negatieve voorhanden hoeveelheden</span><span class="sxs-lookup"><span data-stu-id="f6f6e-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6f6e-104">Als in het systeem een negatieve cumulatieve hoeveelheid voorhanden voorraad wordt weergegeven, behandelt de planningsengine de hoeveelheid als 0 (nul) om te voorkomen dat er te veel voorraad wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="f6f6e-105">Deze functionaliteit werkt als volgt:</span><span class="sxs-lookup"><span data-stu-id="f6f6e-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="f6f6e-106">Met de functie voor planningsoptimalisatie worden voorhanden hoeveelheden op het laagste niveau van de behoefteplanningsdimensies samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="f6f6e-107">(Als *locatie* bijvoorbeeld geen behoefteplanningsdimensie is, worden in planningsoptimalisatie de voorhanden hoeveelheden geaggregeerd op het niveau *magazijn*.)</span><span class="sxs-lookup"><span data-stu-id="f6f6e-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="f6f6e-108">Als de totale voorhanden voorraad op het laagste niveau van de behoefteplanningsdimensies negatief is, wordt er in het systeem van uitgegaan dat de voorhanden voorraad in werkelijkheid 0 (nul) is.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6f6e-109">De nauwkeurigheid van het planningssysteem is afhankelijk van de invoergegevens.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="f6f6e-110">Als de invoergegevens onjuist zijn, geven negatieve voorhanden records aan dat de voorraadinformatie in Microsoft Dynamics 365 Supply Chain Management niet meer synchroon loopt met de echte wereld.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="f6f6e-111">Daarom bevat het planningsresultaat fouten.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="f6f6e-112">Om een nauwkeurig planningsresultaat te krijgen, moet u het aantal records beperken dat een negatieve voorhanden hoeveelheid weergeeft.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="f6f6e-113">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="f6f6e-113">Example 1</span></span>

<span data-ttu-id="f6f6e-114">Magazijn 13 wordt op de volgende manier geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="f6f6e-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="f6f6e-115">**Behoefteplanningscode:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="f6f6e-116">**Minimum:** 15 stuks (st)</span><span class="sxs-lookup"><span data-stu-id="f6f6e-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="f6f6e-117">**Maximum:** 25 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="f6f6e-118">Het laagste niveau van behoefteplanningsdimensies is *magazijn* en de volgende voorhanden hoeveelheden worden geregistreerd op het niveau *locatie*:</span><span class="sxs-lookup"><span data-stu-id="f6f6e-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="f6f6e-119">**Vestiging 1, magazijn 13, locatie 1:** 20 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="f6f6e-120">**Vestiging 1, magazijn 13, locatie 2:** &minus;8 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="f6f6e-121">Daarom is de gecumuleerde voorhanden hoeveelheid voor magazijn 13 12 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="f6f6e-122">(= 20 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-122">(= 20 pcs.</span></span> <span data-ttu-id="f6f6e-123">&minus; 8 st.).</span><span class="sxs-lookup"><span data-stu-id="f6f6e-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="f6f6e-124">In dit geval gebruikt de planningsengine een cumulatieve voorhanden hoeveelheid van 12 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="f6f6e-125">voor magazijn 13.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-125">for warehouse 13.</span></span>

<span data-ttu-id="f6f6e-126">Het resultaat is een geplande order van 13 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="f6f6e-127">(= 25 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-127">(= 25 pcs.</span></span> <span data-ttu-id="f6f6e-128">&minus; 12 st.) om magazijn 13 opnieuw te vullen op basis van 12 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="f6f6e-129">tot 25 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="f6f6e-130">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="f6f6e-130">Example 2</span></span>

<span data-ttu-id="f6f6e-131">Magazijn 13 wordt op de volgende manier geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="f6f6e-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="f6f6e-132">**Behoefteplanningscode:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="f6f6e-133">**Minimum:** 15 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="f6f6e-134">**Maximum:** 25 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="f6f6e-135">Het laagste niveau van behoefteplanningsdimensies is *magazijn* en de volgende voorhanden hoeveelheden worden geregistreerd op het niveau *locatie*:</span><span class="sxs-lookup"><span data-stu-id="f6f6e-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="f6f6e-136">**Vestiging 1, magazijn 13, locatie 1:** 4 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="f6f6e-137">**Vestiging 1, magazijn 13, locatie 2:** &minus;8 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="f6f6e-138">Daarom is de gecumuleerde voorhanden hoeveelheid voor magazijn 13 &minus;4 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="f6f6e-139">(= 4 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-139">(= 4 pcs.</span></span> <span data-ttu-id="f6f6e-140">&minus; 8 st.).</span><span class="sxs-lookup"><span data-stu-id="f6f6e-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="f6f6e-141">Dat wil zeggen dat de voorraad minder dan 0 (nul) is.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="f6f6e-142">In dit geval gaat de planningsengine ervan uit dat de voorhanden hoeveelheid voor magazijn 13 0 st. bedraagt.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="f6f6e-143">in plaats van &minus;4 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="f6f6e-144">Het resultaat is een geplande order van 25 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="f6f6e-145">(= 25 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-145">(= 25 pcs.</span></span> <span data-ttu-id="f6f6e-146">&minus; 0 st.) om magazijn 13 opnieuw te vullen op basis van 0 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="f6f6e-147">tot 25 st.</span><span class="sxs-lookup"><span data-stu-id="f6f6e-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="f6f6e-148">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="f6f6e-148">Related resources</span></span>

[<span data-ttu-id="f6f6e-149">Overzicht van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="f6f6e-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="f6f6e-150">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="f6f6e-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="f6f6e-151">Analyse voor passende Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="f6f6e-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="f6f6e-152">Planhistorie en planningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="f6f6e-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="f6f6e-153">Een planningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="f6f6e-153">Cancel a planning job</span></span>](cancel-planning-job.md)