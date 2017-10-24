--- 
title: Een productiestroomversie maken
description: Deze procedure is gericht op het maken van een nieuwe productstroomversie.
author: cvocph
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58b3c9cd265b97a814541315e4ba8378010eb2b2
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="69259-103">Een productiestroomversie maken</span><span class="sxs-lookup"><span data-stu-id="69259-103">Create a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="69259-104">Deze procedure is gericht op het maken van een nieuwe productstroomversie.</span><span class="sxs-lookup"><span data-stu-id="69259-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="69259-105">Voor deze procedure moeten de productieparameters voor lean manufacturing en de maateenheden voor klassetijd worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="69259-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="69259-106">U moet ook een waardestroom en een productiegroep definiëren.</span><span class="sxs-lookup"><span data-stu-id="69259-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="69259-107">Als u meer wilt weten over productiestromen en activiteiten in lean manufacturing, raadpleegt u de whitepapers over lean manufacturing voor Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="69259-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="69259-108">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="69259-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="69259-109">Een productiestromen maken</span><span class="sxs-lookup"><span data-stu-id="69259-109">Create a production flow</span></span>
1. <span data-ttu-id="69259-110">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="69259-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="69259-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="69259-111">Click New.</span></span>
3. <span data-ttu-id="69259-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="69259-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="69259-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="69259-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="69259-114">Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="69259-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="69259-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="69259-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="69259-116">Selecteer een operationele eenheid van het type waardestroom.</span><span class="sxs-lookup"><span data-stu-id="69259-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="69259-117">Een waardestroom is een operationele eenheid die alle activiteiten en stromen van de waardestroom omvat.</span><span class="sxs-lookup"><span data-stu-id="69259-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="69259-118">In deze fase zijn operationele eenheden beperkt tot een rechtspersoon en hebben ze verder geen functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="69259-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="69259-119">Klik in het veld Productiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="69259-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="69259-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="69259-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="69259-121">Selecteer een productiegroep voor de productiestroom.</span><span class="sxs-lookup"><span data-stu-id="69259-121">Select a production group for the production flow.</span></span> <span data-ttu-id="69259-122">Productieorders maken het definiëren van materiaal, arbeid en OHW-rekeningen mogelijk voor een productieproces.</span><span class="sxs-lookup"><span data-stu-id="69259-122">Production groups allow the definition of material, labour, and WIP accounts for a production process.</span></span> <span data-ttu-id="69259-123">Als u de boekhoudcontext wilt koppelen aan een productiestroom, moet een productiegroep zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="69259-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="69259-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="69259-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="69259-125">Een productiestroomversie maken</span><span class="sxs-lookup"><span data-stu-id="69259-125">Create a production flow version</span></span>
1. <span data-ttu-id="69259-126">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="69259-126">Click Add.</span></span>
2. <span data-ttu-id="69259-127">Voer in het veld Vervaldatum een datum en tijd in.</span><span class="sxs-lookup"><span data-stu-id="69259-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="69259-128">Definieer indien nodig een vervaldatum voor de versie.</span><span class="sxs-lookup"><span data-stu-id="69259-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="69259-129">U kunt deze op elk moment bijwerken, zelfs voor actieve versies.</span><span class="sxs-lookup"><span data-stu-id="69259-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="69259-130">U kunt deze gebruiken om een versie uit te faseren.</span><span class="sxs-lookup"><span data-stu-id="69259-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="69259-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="69259-131">Click OK.</span></span>
4. <span data-ttu-id="69259-132">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="69259-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="69259-133">Typ een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="69259-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="69259-134">Wijzig de takteenheid.</span><span class="sxs-lookup"><span data-stu-id="69259-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="69259-135">Voer in het veld Gemiddelde takttijd een getal in.</span><span class="sxs-lookup"><span data-stu-id="69259-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="69259-136">Definieer de gemiddelde takttijd van de versie.</span><span class="sxs-lookup"><span data-stu-id="69259-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="69259-137">Definieer voor het taktbeheer van de productiestroomversie een beoogde gemiddelde takttijd.</span><span class="sxs-lookup"><span data-stu-id="69259-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="69259-138">De takt wordt gedefinieerd als hoeveelheid per periode.</span><span class="sxs-lookup"><span data-stu-id="69259-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="69259-139">In het voorbeeld is de takttijd 0,2 uur per 10 stuks.</span><span class="sxs-lookup"><span data-stu-id="69259-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="69259-140">Voor een werktijd van 8 uur correspondeert dat met een dagelijkse doorvoercapaciteit van 400 stuks.</span><span class="sxs-lookup"><span data-stu-id="69259-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="69259-141">Voer in het veld Hoeveelheid per cyclus een getal in.</span><span class="sxs-lookup"><span data-stu-id="69259-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="69259-142">Definieer de hoeveelheid per cyclus, gerelateerd aan de gemiddelde takttijd.</span><span class="sxs-lookup"><span data-stu-id="69259-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="69259-143">Schakel de uitbreiding van de sectie Versiedetails om.</span><span class="sxs-lookup"><span data-stu-id="69259-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="69259-144">Voer in het veld Minimumtakttijd een getal in.</span><span class="sxs-lookup"><span data-stu-id="69259-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="69259-145">Definieer de minimale takttijd.</span><span class="sxs-lookup"><span data-stu-id="69259-145">Define the minimum takt time.</span></span> <span data-ttu-id="69259-146">De minimale takttijd moet korter zijn dan of gelijk zijn aan de gemiddelde takttijd.</span><span class="sxs-lookup"><span data-stu-id="69259-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="69259-147">Voer in het veld Maximumtakttijd een getal in.</span><span class="sxs-lookup"><span data-stu-id="69259-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="69259-148">De maximale takttijd moet langer zijn dan of gelijk zijn aan de gemiddelde takttijd.</span><span class="sxs-lookup"><span data-stu-id="69259-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="69259-149">Voer een getal in het veld Periode voor werkelijke cyclusduur (dagen) in.</span><span class="sxs-lookup"><span data-stu-id="69259-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="69259-150">Voer het aantal dagen in het veld Periode voor werkelijke cyclusduur in.</span><span class="sxs-lookup"><span data-stu-id="69259-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="69259-151">De periode voor de werkelijke cyclustijd is het aantal dagen dat taken worden samengevoegd vanaf de werkelijke minuut achterwaarts om de werkelijke cyclustijd te berekenen.</span><span class="sxs-lookup"><span data-stu-id="69259-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="69259-152">De waarde kan altijd worden gewijzigd en wordt alleen gebruikt voor de berekening van de werkelijke cyclustijden.</span><span class="sxs-lookup"><span data-stu-id="69259-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="69259-153">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="69259-153">Click Save.</span></span>


