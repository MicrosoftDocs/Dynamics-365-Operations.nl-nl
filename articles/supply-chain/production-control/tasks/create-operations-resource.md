---
title: Bron voor bedrijfsactiviteiten maken
description: Een bron voor bedrijfsactiviteiten voert de activiteiten van een project of een productieproces uit.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 514b0b27065b4318891a84f364b39e8e378d6a4a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255080"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="50bbe-103">Bron voor bedrijfsactiviteiten maken</span><span class="sxs-lookup"><span data-stu-id="50bbe-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50bbe-104">Een bron voor bedrijfsactiviteiten voert de activiteiten van een project of een productieproces uit.</span><span class="sxs-lookup"><span data-stu-id="50bbe-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="50bbe-105">Deze procedure toont u hoe u een bron voor bedrijfsactiviteiten definieert.</span><span class="sxs-lookup"><span data-stu-id="50bbe-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="50bbe-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="50bbe-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="50bbe-107">Ga naar Resources.</span><span class="sxs-lookup"><span data-stu-id="50bbe-107">Go to Resources.</span></span>
2. <span data-ttu-id="50bbe-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="50bbe-108">Click New.</span></span>
3. <span data-ttu-id="50bbe-109">Typ een waarde in het veld Bron.</span><span class="sxs-lookup"><span data-stu-id="50bbe-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="50bbe-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="50bbe-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="50bbe-111">Parameters voor capaciteit en verbruik definiëren</span><span class="sxs-lookup"><span data-stu-id="50bbe-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="50bbe-112">Vouw de sectie Bewerking uit.</span><span class="sxs-lookup"><span data-stu-id="50bbe-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="50bbe-113">Voer in het veld Uitvalpercentage een getal in.</span><span class="sxs-lookup"><span data-stu-id="50bbe-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="50bbe-114">Typ of selecteer een waarde in het veld Instelcategorie.</span><span class="sxs-lookup"><span data-stu-id="50bbe-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="50bbe-115">Geef de kostencategorie op die bepaalt hoe de kosten van de voorbereidingstijd moeten worden verantwoord.</span><span class="sxs-lookup"><span data-stu-id="50bbe-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="50bbe-116">Typ of selecteer een waarde in het veld Uitvoeringstijdcategorie.</span><span class="sxs-lookup"><span data-stu-id="50bbe-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="50bbe-117">Geef de kostencategorie op die bepaalt hoe de kosten van de uitvoeringstijd moeten worden verantwoord.</span><span class="sxs-lookup"><span data-stu-id="50bbe-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="50bbe-118">Typ of selecteer een waarde in het veld Hoeveelheidscategorie.</span><span class="sxs-lookup"><span data-stu-id="50bbe-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="50bbe-119">Geef de kostencategorie op die bepaalt hoe de resourcekosten op basis van de uitvoerhoeveelheid moeten worden verantwoord.</span><span class="sxs-lookup"><span data-stu-id="50bbe-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="50bbe-120">Selecteer een optie in het veld Capaciteitseenheid.</span><span class="sxs-lookup"><span data-stu-id="50bbe-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="50bbe-121">Geef de eenheid op waarin de capaciteit van de bron voor bedrijfsactiviteiten wordt uitgedrukt.</span><span class="sxs-lookup"><span data-stu-id="50bbe-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="50bbe-122">Voer een nummer in het veld Capaciteit in.</span><span class="sxs-lookup"><span data-stu-id="50bbe-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="50bbe-123">U moet een getal invoeren in het veld Efficiëntiepercentage.</span><span class="sxs-lookup"><span data-stu-id="50bbe-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="50bbe-124">Geef de efficiëntie op die u van de bron voor bedrijfsactiviteiten verwacht.</span><span class="sxs-lookup"><span data-stu-id="50bbe-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="50bbe-125">Het efficiëntiepercentage past de doorvoercapaciteit van de bron voor bedrijfsactiviteiten aan en beïnvloedt de tijd die voor de bron is gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="50bbe-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="50bbe-126">Voer in het veld Percentage bewerkingsplanning een getal in.</span><span class="sxs-lookup"><span data-stu-id="50bbe-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="50bbe-127">Geef het maximumpercentage van de capaciteit van de bron voor bedrijfsactiviteiten op die u in bewerkingsplanning wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="50bbe-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="50bbe-128">Selecteer Ja in het veld Eindige capaciteit.</span><span class="sxs-lookup"><span data-stu-id="50bbe-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="50bbe-129">Stel deze optie in op Ja als de bron voor bedrijfsactiviteiten moet worden gepland op basis van de werkelijke capaciteit die beschikbaar is, en als de bestaande capaciteitsreserveringen in aanmerking moeten worden genomen.</span><span class="sxs-lookup"><span data-stu-id="50bbe-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="50bbe-130">Als deze optie is ingesteld op Nee, wordt aangenomen dat de bron voor bedrijfsactiviteiten oneindige capaciteit heeft, en kan bron worden overboekt.</span><span class="sxs-lookup"><span data-stu-id="50bbe-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="50bbe-131">Selecteer Ja in het veld Bottleneck resource.</span><span class="sxs-lookup"><span data-stu-id="50bbe-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="50bbe-132">Werktijden definiëren</span><span class="sxs-lookup"><span data-stu-id="50bbe-132">Define working times</span></span>
1. <span data-ttu-id="50bbe-133">Vouw de sectie Kalenders uit.</span><span class="sxs-lookup"><span data-stu-id="50bbe-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="50bbe-134">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="50bbe-134">Click Add.</span></span>
3. <span data-ttu-id="50bbe-135">Typ of selecteer een waarde in het veld Kalender.</span><span class="sxs-lookup"><span data-stu-id="50bbe-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="50bbe-136">Geef de werktijdkalender op die de capaciteit (in uren) van de resource definieert.</span><span class="sxs-lookup"><span data-stu-id="50bbe-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="50bbe-137">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="50bbe-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="50bbe-138">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="50bbe-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="50bbe-139">Bronmogelijkheden definiëren</span><span class="sxs-lookup"><span data-stu-id="50bbe-139">Define resource capabilities</span></span>
1. <span data-ttu-id="50bbe-140">Vouw de sectie Mogelijkheden uit.</span><span class="sxs-lookup"><span data-stu-id="50bbe-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="50bbe-141">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="50bbe-141">Click Add.</span></span>
    * <span data-ttu-id="50bbe-142">Een capaciteit is de mogelijkheid van een bron voor bedrijfsactiviteiten om een bepaalde activiteit uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="50bbe-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="50bbe-143">De planningsengine wijst bronnen toe door de bronbehoeften van elke activiteit te vergelijken met de mogelijkheden van de beschikbare bronnen voor bedrijfsactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="50bbe-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="50bbe-144">Typ of selecteer een waarde in het veld Mogelijkheid.</span><span class="sxs-lookup"><span data-stu-id="50bbe-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="50bbe-145">Voer een nummer in het veld Niveau in.</span><span class="sxs-lookup"><span data-stu-id="50bbe-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="50bbe-146">Geef het vaardigheidsniveau op waarop de bron de capaciteit verwerkt.</span><span class="sxs-lookup"><span data-stu-id="50bbe-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="50bbe-147">Voer een getal in het veld Prioriteit in.</span><span class="sxs-lookup"><span data-stu-id="50bbe-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="50bbe-148">Geef de prioriteit van de bron voor bedrijfsactiviteiten met betrekking tot de capaciteit op.</span><span class="sxs-lookup"><span data-stu-id="50bbe-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="50bbe-149">Bij planning met prioriteit, wordt de bron voor bedrijfsactiviteiten met de hoogste prioriteit (de laagste numerieke waarde) als eerste geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="50bbe-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="50bbe-150">Resource toewijzen aan resourcegroep</span><span class="sxs-lookup"><span data-stu-id="50bbe-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="50bbe-151">Vouw de sectie Resourcegroepen uit.</span><span class="sxs-lookup"><span data-stu-id="50bbe-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="50bbe-152">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="50bbe-152">Click Add.</span></span>
    * <span data-ttu-id="50bbe-153">De resourcegroep definieert de locatie, productie-eenheid en magazijncontext voor bronnen voor bedrijfsactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="50bbe-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="50bbe-154">De bron voor bedrijfsactiviteiten kan alleen worden gepland indien toegewezen aan een resourcegroep, en alleen op de locatie waar de resourcegroep zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="50bbe-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="50bbe-155">Typ of selecteer een waarde in het veld Resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="50bbe-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="50bbe-156">Typ of selecteer een waarde in het veld Invoerlocatie.</span><span class="sxs-lookup"><span data-stu-id="50bbe-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="50bbe-157">Geef de magazijnlocatie op van waar de bron voor bedrijfsactiviteiten materialen verbruikt.</span><span class="sxs-lookup"><span data-stu-id="50bbe-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]