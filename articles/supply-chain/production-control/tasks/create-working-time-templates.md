---
title: Werktijdsjablonen maken
description: Werktijdsjablonen de definiëren de werkuren door een week en worden gebruikt om werktijden voor een periode te genereren.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8cc9fc58c9a14c20eecd486e3869a9b00c54c2c5
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149131"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="d0ee2-103">Werktijdsjablonen maken</span><span class="sxs-lookup"><span data-stu-id="d0ee2-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0ee2-104">Werktijdsjablonen de definiëren de werkuren door een week en worden gebruikt om werktijden voor een periode te genereren.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="d0ee2-105">Deze procedure toont hoe u een werktijdsjabloon bepaalt met behulp van eigenschappen van werktijdplanningen om werktijdsintervallen te categoriseren.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="d0ee2-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d0ee2-107">Ga naar Alle werkruimten > Levenscyclusbeheer bron.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="d0ee2-108">Klik op Werktijdsjablonen.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="d0ee2-109">Werktijdsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="d0ee2-109">Create working time template</span></span>
1. <span data-ttu-id="d0ee2-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-110">Click New.</span></span>
2. <span data-ttu-id="d0ee2-111">Typ een waarde in het veld Werktijdsjabloon.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="d0ee2-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d0ee2-113">Vouw de sectie Maandag uit.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="d0ee2-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-114">Click Add.</span></span>
6. <span data-ttu-id="d0ee2-115">Voer in het veld Van een tijd in.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="d0ee2-116">Geef de tijd op waarop het werk 's ochtends begint.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="d0ee2-117">Voer in het veld Tot een tijd in.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="d0ee2-118">Geef de tijd op waarop medewerkers lunchpauze hebben.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="d0ee2-119">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-119">Click Add.</span></span>
9. <span data-ttu-id="d0ee2-120">Voer in het veld Van een tijd in.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="d0ee2-121">Geef de tijd op waarop het werk na de lunch hervat.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="d0ee2-122">Voer in het veld Tot een tijd in.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="d0ee2-123">Geef het einde van de werkdag op.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="d0ee2-124">Werktijden repliceren naar alle weekdagen</span><span class="sxs-lookup"><span data-stu-id="d0ee2-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="d0ee2-125">Klik op Dag kopiëren.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-125">Click Copy day.</span></span>
    * <span data-ttu-id="d0ee2-126">Kopieer de definities van werktijden van maandag naar dinsdag.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="d0ee2-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-127">Click OK.</span></span>
3. <span data-ttu-id="d0ee2-128">Klik op Dag kopiëren.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-128">Click Copy day.</span></span>
    * <span data-ttu-id="d0ee2-129">Kopieer de definities van werktijden van maandag naar woensdag.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="d0ee2-130">Selecteer een optie in het veld Tot weekdag.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="d0ee2-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-131">Click OK.</span></span>
6. <span data-ttu-id="d0ee2-132">Klik op Dag kopiëren.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-132">Click Copy day.</span></span>
    * <span data-ttu-id="d0ee2-133">Kopieer de definities van werktijden van maandag naar donderdag.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="d0ee2-134">Selecteer een optie in het veld Tot weekdag.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="d0ee2-135">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-135">Click OK.</span></span>
9. <span data-ttu-id="d0ee2-136">Klik op Dag kopiëren.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-136">Click Copy day.</span></span>
    * <span data-ttu-id="d0ee2-137">Kopieer de definities van werktijden van maandag naar vrijdag.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="d0ee2-138">Selecteer een optie in het veld Tot weekdag.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="d0ee2-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="d0ee2-140">Tijdsleuven voor specifieke acties definiëren</span><span class="sxs-lookup"><span data-stu-id="d0ee2-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="d0ee2-141">Vouw de sectie Vrijdag uit.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="d0ee2-142">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d0ee2-143">Typ of selecteer een waarde in het veld Eigenschap.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="d0ee2-144">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d0ee2-145">Typ of selecteer een waarde in het veld Eigenschap.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="d0ee2-146">Weekenddagen markeren als Gesloten voor ophalen</span><span class="sxs-lookup"><span data-stu-id="d0ee2-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="d0ee2-147">Vouw de sectie Zaterdag uit.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="d0ee2-148">Selecteer Ja in het veld Gesloten voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="d0ee2-149">Vouw de sectie Zondag uit.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="d0ee2-150">Selecteer Ja in het veld Gesloten voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="d0ee2-150">Select Yes in the Closed for pickup field.</span></span>

