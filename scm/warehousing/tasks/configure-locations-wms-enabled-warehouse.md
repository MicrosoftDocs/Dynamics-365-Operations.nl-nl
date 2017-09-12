--- 
title: Locaties in een WMS-magazijn configureren
description: Deze begeleiding toont hoe u de locatie-instelling configureert voor een nieuw WMS-magazijn (een magazijn dat geavanceerde magazijnbeheerprocessen gebruikt).
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1082c86361180db84bb2b5c0b8158816f76a219e
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="76efd-103">Locaties in een WMS-magazijn configureren</span><span class="sxs-lookup"><span data-stu-id="76efd-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76efd-104">Deze begeleiding toont hoe u de locatie-instelling configureert voor een nieuw WMS-magazijn (een magazijn dat geavanceerde magazijnbeheerprocessen gebruikt).</span><span class="sxs-lookup"><span data-stu-id="76efd-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="76efd-105">Het proces wordt gewoonlijk uitgevoerd door een magazijnmanager.</span><span class="sxs-lookup"><span data-stu-id="76efd-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="76efd-106">U kunt deze begeleiding uitvoeren in het demobedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="76efd-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="76efd-107">Een preconditie is dat u ten minste één geconfigureerde site hebt.</span><span class="sxs-lookup"><span data-stu-id="76efd-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="76efd-108">Een nieuw magazijn maken</span><span class="sxs-lookup"><span data-stu-id="76efd-108">Create a new warehouse</span></span>
1. <span data-ttu-id="76efd-109">Ga naar Magazijnen.</span><span class="sxs-lookup"><span data-stu-id="76efd-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="76efd-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-110">Click New.</span></span>
3. <span data-ttu-id="76efd-111">Typ een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="76efd-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="76efd-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="76efd-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="76efd-113">Typ een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="76efd-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="76efd-114">Vouw de sectie Magazijn uit of samen.</span><span class="sxs-lookup"><span data-stu-id="76efd-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="76efd-115">Stel de optie Magazijnbeheerprocessen gebruiken in op Ja.</span><span class="sxs-lookup"><span data-stu-id="76efd-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="76efd-116">Met deze instelling kunt u geavanceerde magazijnprocessen uitvoeren met magazijnwerk en mobiele apparaten.</span><span class="sxs-lookup"><span data-stu-id="76efd-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="76efd-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="76efd-118">Een locatie-indeling definiëren</span><span class="sxs-lookup"><span data-stu-id="76efd-118">Define a location format</span></span>
1. <span data-ttu-id="76efd-119">Ga naar Locatie-indelingen.</span><span class="sxs-lookup"><span data-stu-id="76efd-119">Go to Location formats.</span></span>
    * <span data-ttu-id="76efd-120">Locatie-indelingen zijn een naamsysteem dat wordt gebruikt om unieke en consistente namen te maken voor verschillende locatiebakposities die binnen een magazijn worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="76efd-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="76efd-121">Het kan handig zijn om scheidingstekens als onderdeel van de locatie-indeling te gebruiken om het gemakkelijker te maken onderdelen van de locatie zoals het gangnummer te identificeren.</span><span class="sxs-lookup"><span data-stu-id="76efd-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="76efd-122">In dit voorbeeld wordt er een naam met vier onderdelen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76efd-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="76efd-123">Dit kunnen bijvoorbeeld gang, rek, plank en bak zijn.</span><span class="sxs-lookup"><span data-stu-id="76efd-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="76efd-124">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-124">Click New.</span></span>
3. <span data-ttu-id="76efd-125">Typ een waarde in het veld Locatie-indeling.</span><span class="sxs-lookup"><span data-stu-id="76efd-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="76efd-126">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="76efd-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="76efd-127">Typ een waarde in het veld Segmentomschrijving.</span><span class="sxs-lookup"><span data-stu-id="76efd-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="76efd-128">Dit onderdeel beschrijft wat het eerste onderdeel van de locatienaam betekent.</span><span class="sxs-lookup"><span data-stu-id="76efd-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="76efd-129">Dat kan bijvoorbeeld Gang zijn.</span><span class="sxs-lookup"><span data-stu-id="76efd-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="76efd-130">Voer een getal in het veld Lengte in.</span><span class="sxs-lookup"><span data-stu-id="76efd-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="76efd-131">Dit bepaalt hoeveel tekens dit gedeelte van de locatienaam moet hebben.</span><span class="sxs-lookup"><span data-stu-id="76efd-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="76efd-132">Let op dat het totaal van alle onderdelen in de naam, inclusief de scheidingstekens, niet 10 tekens kan overschrijden.</span><span class="sxs-lookup"><span data-stu-id="76efd-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="76efd-133">Typ een waarde in het veld Scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="76efd-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="76efd-134">Dit bepaalt welk teken of symbool tussen het eerste en het tweede onderdeel van de naam wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="76efd-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="76efd-135">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-135">Click New.</span></span>
9. <span data-ttu-id="76efd-136">Typ een waarde in het veld Segmentomschrijving.</span><span class="sxs-lookup"><span data-stu-id="76efd-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="76efd-137">Voer een getal in het veld Lengte in.</span><span class="sxs-lookup"><span data-stu-id="76efd-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="76efd-138">Typ een waarde in het veld Scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="76efd-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="76efd-139">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-139">Click New.</span></span>
13. <span data-ttu-id="76efd-140">Typ een waarde in het veld Segmentomschrijving.</span><span class="sxs-lookup"><span data-stu-id="76efd-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="76efd-141">Voer een getal in het veld Lengte in.</span><span class="sxs-lookup"><span data-stu-id="76efd-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="76efd-142">Typ een waarde in het veld Scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="76efd-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="76efd-143">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-143">Click New.</span></span>
17. <span data-ttu-id="76efd-144">Typ een waarde in het veld Segmentomschrijving.</span><span class="sxs-lookup"><span data-stu-id="76efd-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="76efd-145">Voer een getal in het veld Lengte in.</span><span class="sxs-lookup"><span data-stu-id="76efd-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="76efd-146">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="76efd-146">Click Save.</span></span>
20. <span data-ttu-id="76efd-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="76efd-148">Locatietypen definiëren</span><span class="sxs-lookup"><span data-stu-id="76efd-148">Define location types</span></span>
1. <span data-ttu-id="76efd-149">Ga naar Locatietypen.</span><span class="sxs-lookup"><span data-stu-id="76efd-149">Go to Location types.</span></span>
    * <span data-ttu-id="76efd-150">Locatietypen kunnen worden gebruikt als filteropties om de andere magazijnbeheerprocessen te controleren.</span><span class="sxs-lookup"><span data-stu-id="76efd-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="76efd-151">U moet ten minste faserings- en definitieve verzendlocatietypen maken om het uitgaande magazijnbeheerproces te definiëren.</span><span class="sxs-lookup"><span data-stu-id="76efd-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="76efd-152">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-152">Click New.</span></span>
3. <span data-ttu-id="76efd-153">Typ een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="76efd-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="76efd-154">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="76efd-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="76efd-155">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="76efd-156">Locatieprofiel definiëren</span><span class="sxs-lookup"><span data-stu-id="76efd-156">Define location profile</span></span>
1. <span data-ttu-id="76efd-157">Ga naar Locatieprofielen.</span><span class="sxs-lookup"><span data-stu-id="76efd-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="76efd-158">De definitie van locatieprofielen is zeer belangrijk.</span><span class="sxs-lookup"><span data-stu-id="76efd-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="76efd-159">Gegroepeerde locatiecapaciteit kan hier worden gecontroleerd, evenals het beleid dat bepaalt wat voor voorraad wordt opgeslagen en waar het wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="76efd-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="76efd-160">Locatieprofielen kunnen worden gebruikt als filteropties om de andere magazijnbeheerprocessen te controleren.</span><span class="sxs-lookup"><span data-stu-id="76efd-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="76efd-161">Als minimum moet u een gebruikerslocatieprofiel maken om de magazijnbeheerprocessen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="76efd-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="76efd-162">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-162">Click New.</span></span>
3. <span data-ttu-id="76efd-163">Typ een waarde in het veld Locatieprofiel-id.</span><span class="sxs-lookup"><span data-stu-id="76efd-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="76efd-164">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="76efd-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="76efd-165">Klik in het veld Locatie-indeling op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="76efd-166">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="76efd-167">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="76efd-168">Klik in het veld Locatietype op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="76efd-169">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="76efd-170">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="76efd-171">Schakel het selectievakje Gemengde voorraadstatussen toestaan in of uit.</span><span class="sxs-lookup"><span data-stu-id="76efd-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="76efd-172">Schakel deze optie in als u gemengde voorraadstatuswaarden wilt toestaan op de locaties die zullen worden gegroepeerd door dit locatieprofiel.</span><span class="sxs-lookup"><span data-stu-id="76efd-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="76efd-173">Schakel het selectievakje Regel voor batchdagen overschrijven in of uit.</span><span class="sxs-lookup"><span data-stu-id="76efd-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="76efd-174">Schakel deze optie in om de regel te overschrijven voor hoeveel dagen de voorraadbatchvervaldatums kunnen verschillen om mengen toe te staan van voorraadbatches die niet aan deze regel voldoen.</span><span class="sxs-lookup"><span data-stu-id="76efd-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="76efd-175">Schakel het selectievakje Cyclustelling toestaan in of uit.</span><span class="sxs-lookup"><span data-stu-id="76efd-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="76efd-176">Schakel deze optie in om cyclustellingsprocessen toe te staan op alle locaties die zullen worden gegroepeerd door dit locatieprofiel.</span><span class="sxs-lookup"><span data-stu-id="76efd-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="76efd-177">Vouw de sectie Dimensies uit of samen.</span><span class="sxs-lookup"><span data-stu-id="76efd-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="76efd-178">Met het tabblad Dimensies kunt u parameters en methoden definiëren om exacte berekeningen toe te staan van de belastingscapaciteit binnen alle locaties.</span><span class="sxs-lookup"><span data-stu-id="76efd-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="76efd-179">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="76efd-180">Parameters voor magazijnbeheer inschakelen</span><span class="sxs-lookup"><span data-stu-id="76efd-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="76efd-181">Ga naar Parameters voor magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="76efd-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="76efd-182">Als u magazijnwerk wilt kunnen verwerken, moet u parameters instellen voor het gebruikerslocatieprofiel, het faseringslocatietype en het definitieve verzendlocatietype. Zodra het uitgaande proces eindigt op het definitieve verzendlocatietype dat u definieert, worden de gerelateerde uitgaande transacties bijgewerkt naar 'Verzameld'.</span><span class="sxs-lookup"><span data-stu-id="76efd-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="76efd-183">Vouw de sectie Locatieprofielen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="76efd-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="76efd-184">Klik in het veld Gebruikerslocatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="76efd-185">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="76efd-186">Vouw de sectie Locatietypen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="76efd-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="76efd-187">Klik in het veld Faseringslocatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="76efd-188">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="76efd-189">Klik in het veld Uiteindelijk verzendlocatietype op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="76efd-190">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="76efd-191">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="76efd-192">Magazijnzonegroepen definiëren</span><span class="sxs-lookup"><span data-stu-id="76efd-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="76efd-193">Ga naar Magazijnzonegroepen.</span><span class="sxs-lookup"><span data-stu-id="76efd-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="76efd-194">Magazijnzones kunnen worden gebruikt als filters voor opties om de andere magazijnbeheerprocessen te controleren.</span><span class="sxs-lookup"><span data-stu-id="76efd-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="76efd-195">U moet een zonegroep maken voordat u een zone kunt definiëren.</span><span class="sxs-lookup"><span data-stu-id="76efd-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="76efd-196">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-196">Click New.</span></span>
3. <span data-ttu-id="76efd-197">Typ een waarde in het veld Zonegroep-id.</span><span class="sxs-lookup"><span data-stu-id="76efd-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="76efd-198">Typ een waarde in het veld Naam zonegroep.</span><span class="sxs-lookup"><span data-stu-id="76efd-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="76efd-199">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="76efd-200">Magazijnzones definiëren</span><span class="sxs-lookup"><span data-stu-id="76efd-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="76efd-201">Ga naar Zones.</span><span class="sxs-lookup"><span data-stu-id="76efd-201">Go to Zones.</span></span>
2. <span data-ttu-id="76efd-202">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-202">Click New.</span></span>
3. <span data-ttu-id="76efd-203">Typ een waarde in het veld Zone-id.</span><span class="sxs-lookup"><span data-stu-id="76efd-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="76efd-204">Typ een waarde in het veld Zonenaam.</span><span class="sxs-lookup"><span data-stu-id="76efd-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="76efd-205">Klik in het veld Zonegroep-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="76efd-206">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="76efd-207">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="76efd-208">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="76efd-209">Locaties maken met de wizard voor locatie-instelling</span><span class="sxs-lookup"><span data-stu-id="76efd-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="76efd-210">Ga naar Wizard voor locatie-instelling.</span><span class="sxs-lookup"><span data-stu-id="76efd-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="76efd-211">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="76efd-212">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="76efd-213">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="76efd-214">Klik in het veld Zone-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="76efd-215">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="76efd-216">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="76efd-217">Klik in het veld Locatieprofiel-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="76efd-218">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="76efd-219">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="76efd-220">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="76efd-221">Voer een getal in het veld Vanaf nummer in.</span><span class="sxs-lookup"><span data-stu-id="76efd-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="76efd-222">De velden Vanaf nummer en Tot nummer definiëren hoeveel locaties worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76efd-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="76efd-223">Stel dat u Van nummer instelt op 1 en Tot nummer op 3 voor alle vier de regels in de locatie-indeling. Er worden dan 81 locaties gemaakt (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="76efd-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="76efd-224">Voer een getal in het veld Tot nummer in.</span><span class="sxs-lookup"><span data-stu-id="76efd-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="76efd-225">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="76efd-226">Voer een getal in het veld Vanaf nummer in.</span><span class="sxs-lookup"><span data-stu-id="76efd-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="76efd-227">Voer een getal in het veld Tot nummer in.</span><span class="sxs-lookup"><span data-stu-id="76efd-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="76efd-228">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="76efd-229">Voer een getal in het veld Vanaf nummer in.</span><span class="sxs-lookup"><span data-stu-id="76efd-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="76efd-230">Voer een getal in het veld Tot nummer in.</span><span class="sxs-lookup"><span data-stu-id="76efd-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="76efd-231">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="76efd-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="76efd-232">Voer een getal in het veld Vanaf nummer in.</span><span class="sxs-lookup"><span data-stu-id="76efd-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="76efd-233">Voer een getal in het veld Tot nummer in.</span><span class="sxs-lookup"><span data-stu-id="76efd-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="76efd-234">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="76efd-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="76efd-235">Locaties handmatig maken</span><span class="sxs-lookup"><span data-stu-id="76efd-235">Create locations manually</span></span>
1. <span data-ttu-id="76efd-236">Ga naar Locaties.</span><span class="sxs-lookup"><span data-stu-id="76efd-236">Go to Locations.</span></span>
    * <span data-ttu-id="76efd-237">Handmatig locaties binnen een magazijn maken is eenvoudig.</span><span class="sxs-lookup"><span data-stu-id="76efd-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="76efd-238">De locatienaam en de locatieprofiel-id zijn verplichte waarden.</span><span class="sxs-lookup"><span data-stu-id="76efd-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="76efd-239">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-239">Click New.</span></span>
3. <span data-ttu-id="76efd-240">Typ een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="76efd-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="76efd-241">Typ een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="76efd-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="76efd-242">Merk op dat u hier een nieuwe locatie maakt, dus u moet een nieuwe, unieke naam typen in plaats van een bestaande te selecteren.</span><span class="sxs-lookup"><span data-stu-id="76efd-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="76efd-243">Typ een waarde in het veld Locatieprofiel-id.</span><span class="sxs-lookup"><span data-stu-id="76efd-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="76efd-244">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="76efd-245">Categorieën van verpakkingsgrootte definiëren</span><span class="sxs-lookup"><span data-stu-id="76efd-245">Define Pack size categories</span></span>
1. <span data-ttu-id="76efd-246">Ga naar Categorieën verpakkingsgrootte.</span><span class="sxs-lookup"><span data-stu-id="76efd-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="76efd-247">Verpakkingsgroottecategorieën kunnen worden gebruikt om artikelen te groeperen die soortgelijke fysieke verpakkingsgrootten hebben.</span><span class="sxs-lookup"><span data-stu-id="76efd-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="76efd-248">In dit voorbeeld wordt de verpakkingsgroottecategorie gebruikt om de capaciteit bij de orderverzamellocaties in een bepaalde zone van het magazijn te controleren.</span><span class="sxs-lookup"><span data-stu-id="76efd-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="76efd-249">De verpakkingsgrootte-id moet worden toegewezen aan de vrijgegeven productentiteit om te kunnen worden gebruikt als onderdeel van de verwerking van opslaglimieten.</span><span class="sxs-lookup"><span data-stu-id="76efd-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="76efd-250">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-250">Click New.</span></span>
3. <span data-ttu-id="76efd-251">Typ een waarde in het veld Verpakkingsgroottecategorie-id.</span><span class="sxs-lookup"><span data-stu-id="76efd-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="76efd-252">Typ een waarde in het veld Naam verpakkingsgroottecategorie.</span><span class="sxs-lookup"><span data-stu-id="76efd-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="76efd-253">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="76efd-254">Locatieopslaglimieten instellen</span><span class="sxs-lookup"><span data-stu-id="76efd-254">Define location stocking limits</span></span>
1. <span data-ttu-id="76efd-255">Ga naar Opslaglimieten van locatie.</span><span class="sxs-lookup"><span data-stu-id="76efd-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="76efd-256">Opslaglimieten van locaties helpen te zorgen dat geen werk wordt gemaakt om te verzoeken dat voorraad wordt geplaatst op een locatie die niet de fysieke capaciteit voor die voorraad heeft.</span><span class="sxs-lookup"><span data-stu-id="76efd-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="76efd-257">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-257">Click New.</span></span>
3. <span data-ttu-id="76efd-258">Typ een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="76efd-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="76efd-259">Typ een waarde in het veld Locatieprofiel-id.</span><span class="sxs-lookup"><span data-stu-id="76efd-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="76efd-260">Typ een waarde in het veld Verpakkingsgroottecategorie-id.</span><span class="sxs-lookup"><span data-stu-id="76efd-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="76efd-261">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="76efd-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="76efd-262">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="76efd-262">Click Save.</span></span>
8. <span data-ttu-id="76efd-263">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="76efd-264">Vaste orderverzamellocaties definiëren</span><span class="sxs-lookup"><span data-stu-id="76efd-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="76efd-265">Ga naar Vaste locaties.</span><span class="sxs-lookup"><span data-stu-id="76efd-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="76efd-266">U kunt de te gebruiken locaties definiëren per product of per productvariant.</span><span class="sxs-lookup"><span data-stu-id="76efd-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="76efd-267">Het is mogelijk om meerdere vaste locaties voor hetzelfde product binnen hetzelfde magazijn te maken.</span><span class="sxs-lookup"><span data-stu-id="76efd-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="76efd-268">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="76efd-268">Click New.</span></span>
3. <span data-ttu-id="76efd-269">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="76efd-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="76efd-270">Typ een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="76efd-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="76efd-271">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="76efd-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="76efd-272">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="76efd-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="76efd-273">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="76efd-273">Close the page.</span></span>


