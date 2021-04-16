---
title: Tariefmodellen instellen
description: Deze procedure laat zien hoe u een tariefmodel instelt.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808985"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="01d83-103">Tariefmodellen instellen</span><span class="sxs-lookup"><span data-stu-id="01d83-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01d83-104">Deze procedure laat zien hoe u een tariefmodel instelt.</span><span class="sxs-lookup"><span data-stu-id="01d83-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="01d83-105">De logistiek manager stelt meestal tariefmodellen in, afhankelijk van de contracten die met de vervoerders worden ondertekend.</span><span class="sxs-lookup"><span data-stu-id="01d83-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="01d83-106">In dit scenario gaat u een tariefmodel instellen voor een luchtvaartmaatschappij.</span><span class="sxs-lookup"><span data-stu-id="01d83-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="01d83-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="01d83-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="01d83-108">Een pauzemodel instellen</span><span class="sxs-lookup"><span data-stu-id="01d83-108">Set up break master</span></span>

1. <span data-ttu-id="01d83-109">Ga naar **Transportbeheer > Instellingen > Beoordeling > Pauzemodel**.</span><span class="sxs-lookup"><span data-stu-id="01d83-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="01d83-110">Pauzemodellen worden gebruikt om de prijsstructuur en de onderbrekingspunten te definiëren.</span><span class="sxs-lookup"><span data-stu-id="01d83-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="01d83-111">De prijsstructuur maakt gebruik van gelaagde prijzen die op fysieke afmetingen zijn gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="01d83-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="01d83-112">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="01d83-112">Select **New**.</span></span>
1. <span data-ttu-id="01d83-113">Voer een waarde in het veld **Pauzemodel** in.</span><span class="sxs-lookup"><span data-stu-id="01d83-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="01d83-114">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="01d83-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="01d83-115">Selecteer in het veld **Gegevenstype** het gegevenstype.</span><span class="sxs-lookup"><span data-stu-id="01d83-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="01d83-116">Voer in het veld **Vergelijking** het gewenste type vergelijking in (met behulp van operatoren).</span><span class="sxs-lookup"><span data-stu-id="01d83-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="01d83-117">Voer in het veld **Pauze-eenheid** de pauze-eenheid in.</span><span class="sxs-lookup"><span data-stu-id="01d83-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="01d83-118">Maak in de sectie **Details** zoveel pauzes als nodig zijn voor de prijsstructuur.</span><span class="sxs-lookup"><span data-stu-id="01d83-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="01d83-119">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="01d83-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="01d83-120">Tariefmodel instellen</span><span class="sxs-lookup"><span data-stu-id="01d83-120">Set up rate master</span></span>

1. <span data-ttu-id="01d83-121">Ga naar **Transportbeheer > Instellingen > Beoordeling > Tariefmodel**.</span><span class="sxs-lookup"><span data-stu-id="01d83-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="01d83-122">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="01d83-122">Select **New**.</span></span>
1. <span data-ttu-id="01d83-123">Typ een waarde in het veld **Tariefmodel**.</span><span class="sxs-lookup"><span data-stu-id="01d83-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="01d83-124">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="01d83-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="01d83-125">Selecteer in het veld **Id metagegevens beoordeling** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="01d83-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="01d83-126">De metagegevens-id van de beoordeling bepaalt welke gegevens nodig zijn voor het tariefmodel, aangezien hiermee de metagegevens worden gedefinieerd die de Transportbeheerengine verwacht bij gebruik van dit tariefmodel.</span><span class="sxs-lookup"><span data-stu-id="01d83-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="01d83-127">Selecteer voor dit voorbeeld de optie P2P.</span><span class="sxs-lookup"><span data-stu-id="01d83-127">For this example, select the P2P option.</span></span> <span data-ttu-id="01d83-128">Dit is al gedefinieerd in de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="01d83-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="01d83-129">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="01d83-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="01d83-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="01d83-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="01d83-131">Tariefbasis instellen</span><span class="sxs-lookup"><span data-stu-id="01d83-131">Set up rate base</span></span>

1. <span data-ttu-id="01d83-132">Selecteer **Tariefbasis**.</span><span class="sxs-lookup"><span data-stu-id="01d83-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="01d83-133">De tariefbasis bepaalt het tarief van de vervoerder en kan worden gebruikt voor het instellen van een tariefstructuur aangezien het de tarieven in de onderbrekingspunten structureert die in het pauzemodel zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="01d83-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="01d83-134">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="01d83-134">Select **New**.</span></span>
3. <span data-ttu-id="01d83-135">Typ een waarde in het veld **Tariefbasis**.</span><span class="sxs-lookup"><span data-stu-id="01d83-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="01d83-136">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="01d83-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="01d83-137">Selecteer in het veld **Pauzemodel** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="01d83-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="01d83-138">Pauzemodellen worden gebruikt om de prijsstructuur en de onderbrekingspunten te definiëren.</span><span class="sxs-lookup"><span data-stu-id="01d83-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="01d83-139">De prijsstructuur maakt gebruik van gelaagde prijzen die op fysieke afmetingen zijn gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="01d83-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="01d83-140">Gebruik gewicht voor dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="01d83-140">For this example, use weight.</span></span> <span data-ttu-id="01d83-141">Dit is al gedefinieerd in de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="01d83-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="01d83-142">Selecteer in de lijst de koppeling in de gemarkeerde rij.</span><span class="sxs-lookup"><span data-stu-id="01d83-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="01d83-143">Vouw de sectie **Details** uit.</span><span class="sxs-lookup"><span data-stu-id="01d83-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="01d83-144">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="01d83-144">Select **New**.</span></span>
10. <span data-ttu-id="01d83-145">Typ "30301" in het veld **Postcode van aflevering van**.</span><span class="sxs-lookup"><span data-stu-id="01d83-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="01d83-146">Typ "30318" in het veld **Postcode van aflevering naar**.</span><span class="sxs-lookup"><span data-stu-id="01d83-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="01d83-147">Typ "VS" in het veld **Afleverland/regio**.</span><span class="sxs-lookup"><span data-stu-id="01d83-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="01d83-148">Typ "100" in het veld **< 1,00 pond**.</span><span class="sxs-lookup"><span data-stu-id="01d83-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="01d83-149">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 1 pond is.</span><span class="sxs-lookup"><span data-stu-id="01d83-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="01d83-150">Typ "300" in het veld **< 5,00 pond**.</span><span class="sxs-lookup"><span data-stu-id="01d83-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="01d83-151">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 5 pond is.</span><span class="sxs-lookup"><span data-stu-id="01d83-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="01d83-152">Typ "500" in het veld **< 20,00 pond**.</span><span class="sxs-lookup"><span data-stu-id="01d83-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="01d83-153">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 20 pond is.</span><span class="sxs-lookup"><span data-stu-id="01d83-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="01d83-154">Typ "1000" in het veld **< 100,00 pond**.</span><span class="sxs-lookup"><span data-stu-id="01d83-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="01d83-155">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 100 pond is.</span><span class="sxs-lookup"><span data-stu-id="01d83-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="01d83-156">Typ "3000" in het veld **< 1000,00 pond**.</span><span class="sxs-lookup"><span data-stu-id="01d83-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="01d83-157">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 1000 pond is.</span><span class="sxs-lookup"><span data-stu-id="01d83-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="01d83-158">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="01d83-158">Select **Save**.</span></span>
19. <span data-ttu-id="01d83-159">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01d83-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="01d83-160">Tariefbasis toewijzen</span><span class="sxs-lookup"><span data-stu-id="01d83-160">Assign rate base</span></span>

1. <span data-ttu-id="01d83-161">Vouw de sectie **Toewijzingen tariefbasis** uit.</span><span class="sxs-lookup"><span data-stu-id="01d83-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="01d83-162">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="01d83-162">Select **New**.</span></span>
    * <span data-ttu-id="01d83-163">U kunt verschillende toewijzingen tariefbasis hebben voor elk tariefmodel.</span><span class="sxs-lookup"><span data-stu-id="01d83-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="01d83-164">Dit maakt het mogelijk om verschillende prijspunten voor elke vervoerder te maken afhankelijk van bestemmingen, services of verschillende tariefbasissen.</span><span class="sxs-lookup"><span data-stu-id="01d83-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="01d83-165">In deze procedure kunt u alleen één toewijzing tariefbasis maken.</span><span class="sxs-lookup"><span data-stu-id="01d83-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="01d83-166">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="01d83-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="01d83-167">Selecteer in het veld **Tariefbasis** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="01d83-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="01d83-168">Selecteer in de lijst de koppeling in de gemarkeerde rij.</span><span class="sxs-lookup"><span data-stu-id="01d83-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="01d83-169">Selecteer in het veld **Service** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="01d83-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="01d83-170">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="01d83-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="01d83-171">Selecteer in de lijst de koppeling in de gemarkeerde rij.</span><span class="sxs-lookup"><span data-stu-id="01d83-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="01d83-172">Typ "98052" in het veld **Postcode voor ophalen**.</span><span class="sxs-lookup"><span data-stu-id="01d83-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="01d83-173">Geef op vanaf welke postcode deze toewijzing van de tariefbasis geldig moet zijn.</span><span class="sxs-lookup"><span data-stu-id="01d83-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="01d83-174">Typ "VS" in het veld **Land/regio voor ophalen**.</span><span class="sxs-lookup"><span data-stu-id="01d83-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="01d83-175">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="01d83-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]