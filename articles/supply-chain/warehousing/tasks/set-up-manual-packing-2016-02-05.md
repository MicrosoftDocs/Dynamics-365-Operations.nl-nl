---
title: Handmatige verpakking instellen (februari en mei 2016)
description: In het verpakkingsproces kunt u producten valideren en verpakken in containers.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e1e99b479752a027c60a878c57bd35d4219981
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425827"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="5aa92-103">Handmatige verpakking instellen (februari en mei 2016)</span><span class="sxs-lookup"><span data-stu-id="5aa92-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5aa92-104">In het verpakkingsproces kunt u producten valideren en verpakken in containers.</span><span class="sxs-lookup"><span data-stu-id="5aa92-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="5aa92-105">In dit proces verzamelen magazijnmedewerkers producten van de opslaglocaties en verplaatsen deze naar een inpakstation waar ze de typen en hoeveelheden van artikelen controleren en deze aan de juiste containers toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5aa92-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="5aa92-106">Wanneer een container volledig is verpakt, kunnen ze de container sluiten en verplaatsen naar de outbound docks. De producten zijn dan gereed om te verzenden.</span><span class="sxs-lookup"><span data-stu-id="5aa92-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="5aa92-107">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5aa92-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="5aa92-108">Deze procedure is uitsluitend bedoeld voor de versies van februari 2016 en mei 2016 van Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="5aa92-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="5aa92-109">Locatieprofielen instellen</span><span class="sxs-lookup"><span data-stu-id="5aa92-109">Set up location profiles</span></span>
1. <span data-ttu-id="5aa92-110">Ga naar Magazijnbeheer > Instellingen > Magazijn > Locatieprofielen.</span><span class="sxs-lookup"><span data-stu-id="5aa92-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="5aa92-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5aa92-111">Click New.</span></span>
    * <span data-ttu-id="5aa92-112">Het locatieprofiel wordt gebruikt voor inpakstations en bevat informatie en regels voor een locatie.</span><span class="sxs-lookup"><span data-stu-id="5aa92-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="5aa92-113">Typ een waarde in het veld Locatieprofiel-id.</span><span class="sxs-lookup"><span data-stu-id="5aa92-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="5aa92-114">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5aa92-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5aa92-115">Typ of selecteer een waarde in het veld Locatie-indeling.</span><span class="sxs-lookup"><span data-stu-id="5aa92-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="5aa92-116">Typ of selecteer een waarde in het veld Locatietype.</span><span class="sxs-lookup"><span data-stu-id="5aa92-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="5aa92-117">Selecteer Ja in het veld Gemengde artikelen toestaan.</span><span class="sxs-lookup"><span data-stu-id="5aa92-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="5aa92-118">Selecteer Ja in het veld Gemengde voorraadstatussen toestaan.</span><span class="sxs-lookup"><span data-stu-id="5aa92-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="5aa92-119">Selecteer Ja in het veld Regel voor batchdagen overschrijven.</span><span class="sxs-lookup"><span data-stu-id="5aa92-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="5aa92-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5aa92-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="5aa92-121">Parameters voor magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="5aa92-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="5aa92-122">Ga naar Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="5aa92-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="5aa92-123">Klik op het tabblad Verpakking.</span><span class="sxs-lookup"><span data-stu-id="5aa92-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="5aa92-124">Typ of selecteer een waarde in het veld Profiel-ID voor verpakkingslocatie.</span><span class="sxs-lookup"><span data-stu-id="5aa92-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="5aa92-125">Selecteer het locatieprofiel dat u voor verpakking wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5aa92-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="5aa92-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5aa92-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="5aa92-127">Containertypen instellen</span><span class="sxs-lookup"><span data-stu-id="5aa92-127">Set up container types</span></span>
1. <span data-ttu-id="5aa92-128">Ga naar Magazijnbeheer > Instellingen > Containers > Containertypen.</span><span class="sxs-lookup"><span data-stu-id="5aa92-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="5aa92-129">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5aa92-129">Click New.</span></span>
    * <span data-ttu-id="5aa92-130">U kunt de typen containers definiëren die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5aa92-130">You can define the types of containers to use.</span></span> <span data-ttu-id="5aa92-131">U kunt de fysieke afmetingen van de container opgeven, waaronder tarragewicht, maximumgewicht, maximumvolume, lengte, breedte en gewicht.</span><span class="sxs-lookup"><span data-stu-id="5aa92-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="5aa92-132">De kenmerken zijn aangepaste velden waarmee u extra afmetingen voor het containertype kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5aa92-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="5aa92-133">Typ een waarde in het veld Containertype.</span><span class="sxs-lookup"><span data-stu-id="5aa92-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="5aa92-134">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="5aa92-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5aa92-135">Voer een getal in het veld Tarragewicht in.</span><span class="sxs-lookup"><span data-stu-id="5aa92-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="5aa92-136">Voer in het veld Maximumgewicht een getal in.</span><span class="sxs-lookup"><span data-stu-id="5aa92-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="5aa92-137">Voer een getal in het veld Volume in.</span><span class="sxs-lookup"><span data-stu-id="5aa92-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="5aa92-138">Voer een getal in het veld Lengte in.</span><span class="sxs-lookup"><span data-stu-id="5aa92-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="5aa92-139">Voer een getal in het veld Breedte in.</span><span class="sxs-lookup"><span data-stu-id="5aa92-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="5aa92-140">Voer een getal in het veld Hoogte in.</span><span class="sxs-lookup"><span data-stu-id="5aa92-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="5aa92-141">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5aa92-141">Click Save.</span></span>
12. <span data-ttu-id="5aa92-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5aa92-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="5aa92-143">Verpakkingsprofielen instellen</span><span class="sxs-lookup"><span data-stu-id="5aa92-143">Set up packing profiles</span></span>
1. <span data-ttu-id="5aa92-144">Ga naar Magazijnbeheer > Instellingen > Verpakking > Verpakkingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="5aa92-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="5aa92-145">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5aa92-145">Click New.</span></span>
3. <span data-ttu-id="5aa92-146">Typ een waarde in het veld Verpakkingsprofiel-ID.</span><span class="sxs-lookup"><span data-stu-id="5aa92-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="5aa92-147">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="5aa92-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5aa92-148">Typ of selecteer een waarde in het veld Afsluitingsprofiel-ID van container.</span><span class="sxs-lookup"><span data-stu-id="5aa92-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="5aa92-149">Een afsluitingsprofiel-ID voor containers is optioneel en is het standaardafsluitingsprofiel voor containers voor dit verpakkingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="5aa92-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="5aa92-150">Selecteer een optie in het veld Modus container-ID.</span><span class="sxs-lookup"><span data-stu-id="5aa92-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="5aa92-151">Met deze optie wordt bepaald of een container-ID automatisch wordt gegenereerd wanneer een container wordt gemaakt of dat een container-ID handmatig wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5aa92-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="5aa92-152">Typ of selecteer een waarde in het veld Containertype.</span><span class="sxs-lookup"><span data-stu-id="5aa92-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="5aa92-153">Het containertype wordt standaard worden gebruikt wanneer een nieuwe container wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5aa92-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="5aa92-154">Schakel het selectievakje Automatisch container maken bij sluiten van container in.</span><span class="sxs-lookup"><span data-stu-id="5aa92-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="5aa92-155">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5aa92-155">Click Save.</span></span>
10. <span data-ttu-id="5aa92-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5aa92-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="5aa92-157">Containerafsluitingsprofielen instellen</span><span class="sxs-lookup"><span data-stu-id="5aa92-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="5aa92-158">Ga naar Magazijnbeheer > Instellingen > Containers > Afsluitingsprofielen van container.</span><span class="sxs-lookup"><span data-stu-id="5aa92-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="5aa92-159">Met containerafsluitingsprofielen wordt bepaald wat er gebeurt wanneer een container wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="5aa92-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="5aa92-160">U kunt meerdere afsluitingsprofielen voor containers instellen.</span><span class="sxs-lookup"><span data-stu-id="5aa92-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="5aa92-161">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5aa92-161">Click New.</span></span>
3. <span data-ttu-id="5aa92-162">Typ een waarde in het veld Afsluitingsprofiel-ID van container.</span><span class="sxs-lookup"><span data-stu-id="5aa92-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="5aa92-163">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="5aa92-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5aa92-164">Selecteer een optie in het veld Manifesteren op.</span><span class="sxs-lookup"><span data-stu-id="5aa92-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="5aa92-165">Geef op of manifesteren wordt gebruikt bij het afsluiten van containers of bij het bevestigen van de zending.</span><span class="sxs-lookup"><span data-stu-id="5aa92-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="5aa92-166">Voor manifesteren is Transportbeheer vereist.</span><span class="sxs-lookup"><span data-stu-id="5aa92-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="5aa92-167">Manifesteren moet in de transportengines worden geïmplementeerd. Anders werken ze niet.</span><span class="sxs-lookup"><span data-stu-id="5aa92-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="5aa92-168">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="5aa92-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="5aa92-169">Typ of selecteer een waarde in het veld Standaard locatie voor uiteindelijke verzending.</span><span class="sxs-lookup"><span data-stu-id="5aa92-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="5aa92-170">Dit is de locatie waarnaar producten worden verplaatst nadat de containers zijn gesloten.</span><span class="sxs-lookup"><span data-stu-id="5aa92-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="5aa92-171">Voor deze locatie moet een locatieprofiel zijn gedefinieerd in de magazijnparameters.</span><span class="sxs-lookup"><span data-stu-id="5aa92-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="5aa92-172">Typ of selecteer een waarde in het veld Gewichtseenheid.</span><span class="sxs-lookup"><span data-stu-id="5aa92-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="5aa92-173">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5aa92-173">Click Save.</span></span>

