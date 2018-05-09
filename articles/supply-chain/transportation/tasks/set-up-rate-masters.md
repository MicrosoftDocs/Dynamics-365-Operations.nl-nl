--- 
title: Tariefmodellen instellen
description: Deze procedure laat zien hoe u een tariefmodel instelt.
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2e44c4b4d96d9e3d7048a42a147713b682533b4f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-rate-masters"></a><span data-ttu-id="94656-103">Tariefmodellen instellen</span><span class="sxs-lookup"><span data-stu-id="94656-103">Set up rate masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94656-104">Deze procedure laat zien hoe u een tariefmodel instelt.</span><span class="sxs-lookup"><span data-stu-id="94656-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="94656-105">De logistiek manager stelt meestal tariefmodellen in, afhankelijk van de contracten die met de vervoerders worden ondertekend.</span><span class="sxs-lookup"><span data-stu-id="94656-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="94656-106">In dit scenario gaat u een tariefmodel instellen voor een luchtvaartmaatschappij.</span><span class="sxs-lookup"><span data-stu-id="94656-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="94656-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="94656-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="94656-108">Tariefmodel instellen</span><span class="sxs-lookup"><span data-stu-id="94656-108">Set up rate master</span></span>
1. <span data-ttu-id="94656-109">Ga naar Transportbeheer > Instellingen > Beoordeling > Tariefmodel.</span><span class="sxs-lookup"><span data-stu-id="94656-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="94656-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="94656-110">Click New.</span></span>
3. <span data-ttu-id="94656-111">Typ een waarde in het veld Tariefmodel.</span><span class="sxs-lookup"><span data-stu-id="94656-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="94656-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="94656-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="94656-113">Klik in het veld Id metagegevens beoordeling op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="94656-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="94656-114">De id metagegevens beoordeling bepaalt welke gegevens nodig zijn voor het tariefmodel, aangezien het de metagegevens definieert die de TMS-engine verwacht bij gebruik van dit tariefmodel.</span><span class="sxs-lookup"><span data-stu-id="94656-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="94656-115">Selecteer voor dit voorbeeld de optie P2P</span><span class="sxs-lookup"><span data-stu-id="94656-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="94656-116">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="94656-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="94656-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="94656-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="94656-118">Tariefbasis instellen</span><span class="sxs-lookup"><span data-stu-id="94656-118">Set up rate base</span></span>
1. <span data-ttu-id="94656-119">Klik op Tariefbasis.</span><span class="sxs-lookup"><span data-stu-id="94656-119">Click Rate base.</span></span>
    * <span data-ttu-id="94656-120">De tariefbasis bepaalt het tarief van de vervoerder en kan worden gebruikt voor het instellen van een tariefstructuur aangezien het de tarieven in de onderbrekingspunten structureert die in het pauzemodel zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="94656-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="94656-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="94656-121">Click New.</span></span>
3. <span data-ttu-id="94656-122">Typ een waarde in het veld Tariefbasis.</span><span class="sxs-lookup"><span data-stu-id="94656-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="94656-123">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="94656-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="94656-124">Klik in het veld Pauzemodel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="94656-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="94656-125">Pauzemodellen worden gebruikt om de prijsstructuur en de onderbrekingspunten te definiëren.</span><span class="sxs-lookup"><span data-stu-id="94656-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="94656-126">De prijsstructuur maakt gebruik van gelaagde prijzen die op fysieke afmetingen zijn gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="94656-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="94656-127">Gebruik gewicht voor dit voorbeeld</span><span class="sxs-lookup"><span data-stu-id="94656-127">For this example, use weight</span></span>
7. <span data-ttu-id="94656-128">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="94656-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="94656-129">Schakel de uitbreiding van de sectie Details om.</span><span class="sxs-lookup"><span data-stu-id="94656-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="94656-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="94656-130">Click New.</span></span>
10. <span data-ttu-id="94656-131">Typ "30301" in het veld Postcode van aflevering van.</span><span class="sxs-lookup"><span data-stu-id="94656-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="94656-132">Typ "30318" in het veld Postcode van aflevering naar.</span><span class="sxs-lookup"><span data-stu-id="94656-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="94656-133">Typ "VS" in het veld Afleverland/regio.</span><span class="sxs-lookup"><span data-stu-id="94656-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="94656-134">Typ "100" in het veld "1,00 pond".</span><span class="sxs-lookup"><span data-stu-id="94656-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="94656-135">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 1 pond is.</span><span class="sxs-lookup"><span data-stu-id="94656-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="94656-136">Typ '300' in het veld < 5,00 pond.</span><span class="sxs-lookup"><span data-stu-id="94656-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="94656-137">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 5 pond is.</span><span class="sxs-lookup"><span data-stu-id="94656-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="94656-138">Typ '500' in het veld < 20,00 pond.</span><span class="sxs-lookup"><span data-stu-id="94656-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="94656-139">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 20 pond is.</span><span class="sxs-lookup"><span data-stu-id="94656-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="94656-140">Typ '1000' in het veld < 100,00 pond.</span><span class="sxs-lookup"><span data-stu-id="94656-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="94656-141">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 100 pond is.</span><span class="sxs-lookup"><span data-stu-id="94656-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="94656-142">Typ '3000' in het veld < 1.000,00 pond.</span><span class="sxs-lookup"><span data-stu-id="94656-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="94656-143">Voeg het tarief per pond in als het totale gewicht van de lading minder dan 1000 pond is.</span><span class="sxs-lookup"><span data-stu-id="94656-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="94656-144">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="94656-144">Click Save.</span></span>
19. <span data-ttu-id="94656-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="94656-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="94656-146">Tariefbasis toewijzen</span><span class="sxs-lookup"><span data-stu-id="94656-146">Assign rate base</span></span>
1. <span data-ttu-id="94656-147">Schakel de uitbreiding van de sectie Toewijzingen tariefbasis om.</span><span class="sxs-lookup"><span data-stu-id="94656-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="94656-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="94656-148">Click New.</span></span>
    * <span data-ttu-id="94656-149">U kunt verschillende toewijzingen tariefbasis hebben voor elk tariefmodel.</span><span class="sxs-lookup"><span data-stu-id="94656-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="94656-150">Dit maakt het mogelijk om verschillende prijspunten voor elke vervoerder te maken afhankelijk van bestemmingen, services of verschillende tariefbasissen.</span><span class="sxs-lookup"><span data-stu-id="94656-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="94656-151">In deze procedure kunt u alleen één toewijzing tariefbasis maken.</span><span class="sxs-lookup"><span data-stu-id="94656-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="94656-152">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="94656-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="94656-153">Klik in het veld Tariefbasis op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="94656-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="94656-154">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="94656-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="94656-155">Klik in het veld Service op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="94656-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="94656-156">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="94656-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="94656-157">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="94656-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="94656-158">Typ "98052" in het veld Postcode voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="94656-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="94656-159">Geef op vanaf welke postcode deze toewijzing van de tariefbasis geldig moet zijn.</span><span class="sxs-lookup"><span data-stu-id="94656-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="94656-160">Typ "VS" in het veld Land/regio voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="94656-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="94656-161">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="94656-161">Click Save.</span></span>


