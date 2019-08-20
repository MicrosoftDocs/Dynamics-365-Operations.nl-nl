---
title: Een productiestroom en -versie valideren
description: Deze procedure toont aan hoe u een nieuwe productiestroom en een eerste versie voor lean manufacturing maakt.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 523f6414ec212aef48eece487f4199ea2cf4b87e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836141"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="ab30e-103">Een productiestroom en -versie valideren</span><span class="sxs-lookup"><span data-stu-id="ab30e-103">Validate a production flow and version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab30e-104">Deze procedure toont aan hoe u een nieuwe productiestroom en een eerste versie voor lean manufacturing maakt.</span><span class="sxs-lookup"><span data-stu-id="ab30e-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="ab30e-105">Vereisten: De productieparameters voor lean manufacturing en de maateenheden voor de klasse Tijd moeten worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ab30e-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="ab30e-106">U moet een Waardestroom en een Productiegroep definiëren.</span><span class="sxs-lookup"><span data-stu-id="ab30e-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="ab30e-107">Raadpleeg de whitepapers over lean manufacturing om uzelf vertrouwd te maken met de concepten van productiestromen en activiteiten.</span><span class="sxs-lookup"><span data-stu-id="ab30e-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="ab30e-108">Deze procedure verwijst naar de rechtspersoon USMF in demogegevens.</span><span class="sxs-lookup"><span data-stu-id="ab30e-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="ab30e-109">Als we er echter van uitgaan dat de rechtspersoon voor lean manufacturing is geconfigureerd, kunnen andere rechtspersonen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ab30e-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="ab30e-110">Een productiestromen maken</span><span class="sxs-lookup"><span data-stu-id="ab30e-110">Create a production flow</span></span>
1. <span data-ttu-id="ab30e-111">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="ab30e-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="ab30e-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ab30e-112">Click New.</span></span>
3. <span data-ttu-id="ab30e-113">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="ab30e-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ab30e-114">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="ab30e-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ab30e-115">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ab30e-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ab30e-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ab30e-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ab30e-117">Een waardestroom is een operationele eenheid die alle activiteiten en stromen van de waardestroom dekt.</span><span class="sxs-lookup"><span data-stu-id="ab30e-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="ab30e-118">In deze fase zijn operationele eenheden beperkt tot een rechtspersoon en hebben ze verder geen functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="ab30e-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="ab30e-119">Klik in het veld Productiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="ab30e-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ab30e-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ab30e-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ab30e-121">Productieorders maken het definiëren van materiaal, arbeid en OHW-rekeningen mogelijk voor een productieproces.</span><span class="sxs-lookup"><span data-stu-id="ab30e-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="ab30e-122">Als u de boekhoudcontext wilt koppelen aan een productiestroom, moet een productiegroep zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ab30e-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="ab30e-123">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ab30e-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="ab30e-124">Een productiestroomversie maken</span><span class="sxs-lookup"><span data-stu-id="ab30e-124">Create a production flow version</span></span>
1. <span data-ttu-id="ab30e-125">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ab30e-125">Click Add.</span></span>
2. <span data-ttu-id="ab30e-126">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="ab30e-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="ab30e-127">U kunt de Vervaldatum van de versie op elk moment bijwerken, zelfs voor actieve versies.</span><span class="sxs-lookup"><span data-stu-id="ab30e-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="ab30e-128">Gebruik de vervaldatum van de versie om een stapsgewijze afschaffing van een versie te plannen.</span><span class="sxs-lookup"><span data-stu-id="ab30e-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="ab30e-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ab30e-129">Click OK.</span></span>
4. <span data-ttu-id="ab30e-130">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ab30e-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="ab30e-131">Typ een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="ab30e-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="ab30e-132">Selecteer de Takteenheid.</span><span class="sxs-lookup"><span data-stu-id="ab30e-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="ab30e-133">Voer in het veld Gemiddelde takttijd een getal in.</span><span class="sxs-lookup"><span data-stu-id="ab30e-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="ab30e-134">Definieer voor het taktbeheer van de productiestroomversie een beoogde gemiddelde takttijd.</span><span class="sxs-lookup"><span data-stu-id="ab30e-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="ab30e-135">Takt wordt gedefinieerd als hoeveelheid per periode.</span><span class="sxs-lookup"><span data-stu-id="ab30e-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="ab30e-136">In het voorbeeld is de takttijd 0,2 uur per 10 stuks.</span><span class="sxs-lookup"><span data-stu-id="ab30e-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="ab30e-137">Voor een werktijd van 8 uur correspondeert dat met een dagelijkse doorvoercapaciteit van 400 stuks.</span><span class="sxs-lookup"><span data-stu-id="ab30e-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="ab30e-138">Voer in het veld Hoeveelheid per cyclus een getal in.</span><span class="sxs-lookup"><span data-stu-id="ab30e-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="ab30e-139">Vouw de sectie Versiegegevens uit of samen.</span><span class="sxs-lookup"><span data-stu-id="ab30e-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="ab30e-140">Voer in het veld Minimumtakttijd een getal in.</span><span class="sxs-lookup"><span data-stu-id="ab30e-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="ab30e-141">De minimale takttijd moet korter zijn dan of gelijk zijn aan de gemiddelde takttijd.</span><span class="sxs-lookup"><span data-stu-id="ab30e-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="ab30e-142">Voer in het veld Maximumtakttijd een getal in.</span><span class="sxs-lookup"><span data-stu-id="ab30e-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="ab30e-143">De maximale takttijd moet langer zijn dan of gelijk zijn aan de gemiddelde takttijd.</span><span class="sxs-lookup"><span data-stu-id="ab30e-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="ab30e-144">Een aantal dagen invoeren bij Periode voor werkelijke cyclusduur</span><span class="sxs-lookup"><span data-stu-id="ab30e-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="ab30e-145">De periode voor de werkelijke cyclustijd is het aantal dagen dat taken worden samengevoegd vanaf de werkelijke minuut achterwaarts om de werkelijke cyclustijd te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ab30e-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="ab30e-146">De waarde kan altijd worden gewijzigd en wordt alleen gebruikt voor de berekening van de werkelijke cyclustijden.</span><span class="sxs-lookup"><span data-stu-id="ab30e-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="ab30e-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ab30e-147">Click Save.</span></span>

