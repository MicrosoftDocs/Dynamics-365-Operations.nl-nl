---
title: Een werksjabloon instellen voor inkooporders
description: In dit onderwerp wordt beschreven hoe u een eenvoudige werksjabloon instelt die u kunt gebruiken wanneer u ontvangen artikelen wegzet.
author: ShylaThompson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 227a6865df826caf8ce154f9c44ebe082acd76a5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916732"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="0f771-103">Een werksjabloon instellen voor inkooporders</span><span class="sxs-lookup"><span data-stu-id="0f771-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f771-104">In dit onderwerp wordt beschreven hoe u een eenvoudige werksjabloon instelt die u kunt gebruiken wanneer u ontvangen artikelen wegzet.</span><span class="sxs-lookup"><span data-stu-id="0f771-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="0f771-105">Werksjablonen bepalen de reeks instructies die op een mobiel apparaat aan de magazijnmedewerker worden voorgesteld wanneer deze artikelen van het ontvangende gebied verplaatst.</span><span class="sxs-lookup"><span data-stu-id="0f771-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="0f771-106">U kunt deze procedure gebruiken met de opgegeven gegevens van het demogegevensbedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="0f771-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="0f771-107">Maak voordat u deze handleiding start een werkgroep-id.</span><span class="sxs-lookup"><span data-stu-id="0f771-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="0f771-108">In dit voorbeeld wordt een werkgroep-id met de naam Binnenkomend gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0f771-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="0f771-109">Deze procedure is bedoeld voor de magazijnbeheerder.</span><span class="sxs-lookup"><span data-stu-id="0f771-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="0f771-110">Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellingen > Werk >Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="0f771-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="0f771-111">Selecteer **Inkooporders** in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="0f771-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="0f771-112">Een koptekst van een werksjabloon maken</span><span class="sxs-lookup"><span data-stu-id="0f771-112">Create a work template header</span></span>
1. <span data-ttu-id="0f771-113">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0f771-113">Select **New**.</span></span>
2. <span data-ttu-id="0f771-114">Typ een getal in het veld **Volgnummer**.</span><span class="sxs-lookup"><span data-stu-id="0f771-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="0f771-115">Dit is de volgorde waarin de werksjablonen worden beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="0f771-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="0f771-116">U kunt de volgorde wijzigen, als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="0f771-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="0f771-117">Typ een waarde in het veld **Werksjabloon**.</span><span class="sxs-lookup"><span data-stu-id="0f771-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="0f771-118">Dit is de unieke identificatie voor deze sjabloon.</span><span class="sxs-lookup"><span data-stu-id="0f771-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="0f771-119">Typ een waarde in het veld **Omschrijving van werksjabloon**.</span><span class="sxs-lookup"><span data-stu-id="0f771-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="0f771-120">De optie **Geldig** wordt niet ingeschakeld voordat u alle informatie die voor de sjabloon vereist is, hebt ingevuld en vervolgens op **Opslaan** hebt geklikt.</span><span class="sxs-lookup"><span data-stu-id="0f771-120">The **Valid** option will not be checked until you’ve completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="0f771-121">Een werkorder van het type **Inkooporder** kan niet automatisch worden verwerkt, dus laat de optie **Automatisch verwerken** ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="0f771-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="0f771-122">Typ een waarde in het veld **Werkgroep-id**.</span><span class="sxs-lookup"><span data-stu-id="0f771-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="0f771-123">Met werkgroep-id's kunt u werk in groepen organiseren.</span><span class="sxs-lookup"><span data-stu-id="0f771-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="0f771-124">De waarde die u hier instelt, wordt de standaardwaarde voor elk werk dat met deze sjabloon wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0f771-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="0f771-125">Typ `1` in het veld **Werkprioriteit**.</span><span class="sxs-lookup"><span data-stu-id="0f771-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="0f771-126">Dit geeft het belang van het werk aan. De waarde die u hier instelt, wordt de standaardwaarde voor elk werk dat met deze sjabloon wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0f771-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="0f771-127">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0f771-127">Select **Save**.</span></span> <span data-ttu-id="0f771-128">U moet de koptekst van de werksjabloon opslaan voordat de knop **Query bewerken** beschikbaar wordt.</span><span class="sxs-lookup"><span data-stu-id="0f771-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="0f771-129">De query voor de werksjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="0f771-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="0f771-130">Selecteer **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="0f771-130">Select **Edit query**.</span></span> <span data-ttu-id="0f771-131">We zullen een beperking instellen zodat de sjabloon alleen in een specifiek magazijn kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0f771-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="0f771-132">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0f771-132">Select **Add**.</span></span>
3. <span data-ttu-id="0f771-133">Typ `warehouse` in het veld **Veld**.</span><span class="sxs-lookup"><span data-stu-id="0f771-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="0f771-134">Typ een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="0f771-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="0f771-135">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f771-135">Select **OK**.</span></span>
6. <span data-ttu-id="0f771-136">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0f771-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="0f771-137">Werksjabloongegevens instellen</span><span class="sxs-lookup"><span data-stu-id="0f771-137">Set work template details</span></span>
1. <span data-ttu-id="0f771-138">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0f771-138">Select **New**.</span></span>
2. <span data-ttu-id="0f771-139">Selecteer **Verzamelen** in het veld **Werktype**.</span><span class="sxs-lookup"><span data-stu-id="0f771-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="0f771-140">Typ `purchase` in het veld **Werkklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="0f771-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="0f771-141">De werkklasse die u hier instelt, wordt de standaardwaarde op alle werkregels van type orderverzameling die met deze sjabloon worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0f771-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="0f771-142">De werkklasse kan niet worden overschreven via de werkorderregels.</span><span class="sxs-lookup"><span data-stu-id="0f771-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="0f771-143">Werkklassen worden gebruikt om het type werkorderregels te bepalen en/of beperken dat een magazijnmedewerker op een mobiel apparaat kan verwerken.</span><span class="sxs-lookup"><span data-stu-id="0f771-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="0f771-144">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0f771-144">Select **New**.</span></span>
5. <span data-ttu-id="0f771-145">Selecteer **Wegzetten** in het veld **Werktype**.</span><span class="sxs-lookup"><span data-stu-id="0f771-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="0f771-146">Typ een waarde in het veld **Werkklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="0f771-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="0f771-147">De instructies voor verzamelen en neerzetten zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0f771-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="0f771-148">Elk verzamel-/wegzetpaar moeten dezelfde werkklasse hebben.</span><span class="sxs-lookup"><span data-stu-id="0f771-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="0f771-149">Gebruik dezelfde werkklasse die u voor de instructie voor verzamelen hebt geleverd.</span><span class="sxs-lookup"><span data-stu-id="0f771-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="0f771-150">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="0f771-150">Select **Save**.</span></span> <span data-ttu-id="0f771-151">Het selectievakje **Geldig** is nu ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0f771-151">Note that the **Valid** checkbox is now checked.</span></span>  

