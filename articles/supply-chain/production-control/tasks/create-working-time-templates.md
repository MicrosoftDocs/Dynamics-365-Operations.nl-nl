---
title: Werktijdsjablonen maken
description: Werktijdsjablonen de definiëren de werkuren door een week en worden gebruikt om werktijden voor een periode te genereren.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920923"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="3beaf-103">Werktijdsjablonen maken</span><span class="sxs-lookup"><span data-stu-id="3beaf-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3beaf-104">Werktijdsjablonen de definiëren de werkuren door een week en worden gebruikt om werktijden voor een periode te genereren.</span><span class="sxs-lookup"><span data-stu-id="3beaf-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="3beaf-105">Deze procedure toont hoe u een werktijdsjabloon bepaalt met behulp van eigenschappen van werktijdplanningen om werktijdsintervallen te categoriseren.</span><span class="sxs-lookup"><span data-stu-id="3beaf-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="3beaf-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3beaf-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="3beaf-107">Ga naar **Werkgebieden > Levenscyclusbeheer bron**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="3beaf-108">Selecteer **Werktijdsjablonen**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="3beaf-109">Werktijdsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="3beaf-109">Create working time template</span></span>

1. <span data-ttu-id="3beaf-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-110">Select **New**.</span></span>
1. <span data-ttu-id="3beaf-111">Typ een waarde in het veld **Werktijdsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="3beaf-112">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="3beaf-113">Vouw de sectie **Maandag** uit.</span><span class="sxs-lookup"><span data-stu-id="3beaf-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="3beaf-114">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-114">Select **Add**.</span></span>
1. <span data-ttu-id="3beaf-115">Voer in het veld **Van** een tijd in.</span><span class="sxs-lookup"><span data-stu-id="3beaf-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="3beaf-116">Geef de tijd op waarop het werk 's ochtends begint.</span><span class="sxs-lookup"><span data-stu-id="3beaf-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="3beaf-117">Voer in het veld **Tot** een tijd in.</span><span class="sxs-lookup"><span data-stu-id="3beaf-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="3beaf-118">Geef de tijd op waarop medewerkers lunchpauze hebben.</span><span class="sxs-lookup"><span data-stu-id="3beaf-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="3beaf-119">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-119">Select **Add**.</span></span>
1. <span data-ttu-id="3beaf-120">Voer in het veld **Van** een tijd in.</span><span class="sxs-lookup"><span data-stu-id="3beaf-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="3beaf-121">Geef de tijd op waarop het werk na de lunch hervat.</span><span class="sxs-lookup"><span data-stu-id="3beaf-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="3beaf-122">Voer in het veld **Tot** een tijd in.</span><span class="sxs-lookup"><span data-stu-id="3beaf-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="3beaf-123">Geef het einde van de werkdag op.</span><span class="sxs-lookup"><span data-stu-id="3beaf-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="3beaf-124">Werktijden repliceren naar alle weekdagen</span><span class="sxs-lookup"><span data-stu-id="3beaf-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="3beaf-125">Selecteer **Dag kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="3beaf-126">Kopieer de definities van werktijden van maandag naar dinsdag.</span><span class="sxs-lookup"><span data-stu-id="3beaf-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="3beaf-127">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-127">Select **OK**.</span></span>
1. <span data-ttu-id="3beaf-128">Selecteer **Dag kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="3beaf-129">Kopieer de definities van werktijden van maandag naar woensdag.</span><span class="sxs-lookup"><span data-stu-id="3beaf-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="3beaf-130">Selecteer een optie in het veld **Tot weekdag**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="3beaf-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-131">Select **OK**.</span></span>
1. <span data-ttu-id="3beaf-132">Selecteer **Dag kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="3beaf-133">Kopieer de definities van werktijden van maandag naar donderdag.</span><span class="sxs-lookup"><span data-stu-id="3beaf-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="3beaf-134">Selecteer een optie in het veld **Tot weekdag**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="3beaf-135">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-135">Select **OK**.</span></span>
1. <span data-ttu-id="3beaf-136">Selecteer **Dag kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="3beaf-137">Kopieer de definities van werktijden van maandag naar vrijdag.</span><span class="sxs-lookup"><span data-stu-id="3beaf-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="3beaf-138">Selecteer een optie in het veld **Tot weekdag**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="3beaf-139">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="3beaf-140">Tijdsleuven voor specifieke acties definiëren</span><span class="sxs-lookup"><span data-stu-id="3beaf-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="3beaf-141">Vouw de sectie **Vrijdag** uit.</span><span class="sxs-lookup"><span data-stu-id="3beaf-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="3beaf-142">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3beaf-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="3beaf-143">Typ of selecteer een waarde in het veld **Eigenschap**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="3beaf-144">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3beaf-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="3beaf-145">Typ of selecteer een waarde in het veld **Eigenschap**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="3beaf-146">Weekenddagen markeren als Gesloten voor ophalen</span><span class="sxs-lookup"><span data-stu-id="3beaf-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="3beaf-147">Vouw de sectie **Zaterdag** uit.</span><span class="sxs-lookup"><span data-stu-id="3beaf-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="3beaf-148">Selecteer *Ja* in het veld **Gesloten voor ophalen**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="3beaf-149">Vouw de sectie **Zondag** uit.</span><span class="sxs-lookup"><span data-stu-id="3beaf-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="3beaf-150">Selecteer *Ja* in het veld **Gesloten voor ophalen**.</span><span class="sxs-lookup"><span data-stu-id="3beaf-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]