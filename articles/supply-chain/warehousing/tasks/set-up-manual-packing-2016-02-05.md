--- 
title: Handmatig verpakken instellen (uitsluitend februari en mei 2016)
description: In het verpakkingsproces kunt u producten valideren en verpakken in containers.
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
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
ms.openlocfilehash: 714fd4762ae54f8f6638e81dd19fdd636091b88e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="dc1df-103">Handmatig verpakken instellen (uitsluitend februari en mei 2016)</span><span class="sxs-lookup"><span data-stu-id="dc1df-103">Set up manual packing (February & May 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc1df-104">In het verpakkingsproces kunt u producten valideren en verpakken in containers.</span><span class="sxs-lookup"><span data-stu-id="dc1df-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="dc1df-105">In dit proces verzamelen magazijnmedewerkers producten van de opslaglocaties en verplaatsen deze naar een inpakstation waar ze de typen en hoeveelheden van artikelen controleren en deze aan de juiste containers toewijzen.</span><span class="sxs-lookup"><span data-stu-id="dc1df-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="dc1df-106">Wanneer een container volledig is verpakt, kunnen ze de container sluiten en verplaatsen naar de outbound docks. De producten zijn dan gereed om te verzenden.</span><span class="sxs-lookup"><span data-stu-id="dc1df-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="dc1df-107">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="dc1df-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="dc1df-108">Locatieprofielen instellen</span><span class="sxs-lookup"><span data-stu-id="dc1df-108">Set up location profiles</span></span>
1. <span data-ttu-id="dc1df-109">Ga naar Magazijnbeheer > Instellingen > Magazijn > Locatieprofielen.</span><span class="sxs-lookup"><span data-stu-id="dc1df-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="dc1df-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="dc1df-110">Click New.</span></span>
    * <span data-ttu-id="dc1df-111">Het locatieprofiel wordt gebruikt voor inpakstations en bevat informatie en regels voor een locatie.</span><span class="sxs-lookup"><span data-stu-id="dc1df-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="dc1df-112">Typ een waarde in het veld Locatieprofiel-id.</span><span class="sxs-lookup"><span data-stu-id="dc1df-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="dc1df-113">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="dc1df-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="dc1df-114">Typ of selecteer een waarde in het veld Locatie-indeling.</span><span class="sxs-lookup"><span data-stu-id="dc1df-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="dc1df-115">Typ of selecteer een waarde in het veld Locatietype.</span><span class="sxs-lookup"><span data-stu-id="dc1df-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="dc1df-116">Selecteer Ja in het veld Gemengde artikelen toestaan.</span><span class="sxs-lookup"><span data-stu-id="dc1df-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="dc1df-117">Selecteer Ja in het veld Gemengde voorraadstatussen toestaan.</span><span class="sxs-lookup"><span data-stu-id="dc1df-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="dc1df-118">Selecteer Ja in het veld Regel voor batchdagen overschrijven.</span><span class="sxs-lookup"><span data-stu-id="dc1df-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="dc1df-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="dc1df-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="dc1df-120">Parameters voor magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="dc1df-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="dc1df-121">Ga naar Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="dc1df-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="dc1df-122">Klik op het tabblad Verpakking.</span><span class="sxs-lookup"><span data-stu-id="dc1df-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="dc1df-123">Typ of selecteer een waarde in het veld Profiel-ID voor verpakkingslocatie.</span><span class="sxs-lookup"><span data-stu-id="dc1df-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="dc1df-124">Selecteer het locatieprofiel dat u voor verpakking wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="dc1df-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="dc1df-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="dc1df-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="dc1df-126">Containertypen instellen</span><span class="sxs-lookup"><span data-stu-id="dc1df-126">Set up container types</span></span>
1. <span data-ttu-id="dc1df-127">Ga naar Magazijnbeheer > Instellingen > Containers > Containertypen.</span><span class="sxs-lookup"><span data-stu-id="dc1df-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="dc1df-128">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="dc1df-128">Click New.</span></span>
    * <span data-ttu-id="dc1df-129">U kunt de typen containers definiëren die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="dc1df-129">You can define the types of containers to use.</span></span> <span data-ttu-id="dc1df-130">U kunt de fysieke afmetingen van de container opgeven, waaronder tarragewicht, maximumgewicht, maximumvolume, lengte, breedte en gewicht.</span><span class="sxs-lookup"><span data-stu-id="dc1df-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="dc1df-131">De kenmerken zijn aangepaste velden waarmee u extra afmetingen voor het containertype kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="dc1df-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="dc1df-132">Typ een waarde in het veld Containertype.</span><span class="sxs-lookup"><span data-stu-id="dc1df-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="dc1df-133">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="dc1df-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dc1df-134">Voer een getal in het veld Tarragewicht in.</span><span class="sxs-lookup"><span data-stu-id="dc1df-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="dc1df-135">Voer in het veld Maximumgewicht een getal in.</span><span class="sxs-lookup"><span data-stu-id="dc1df-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="dc1df-136">Voer een getal in het veld Volume in.</span><span class="sxs-lookup"><span data-stu-id="dc1df-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="dc1df-137">Voer een getal in het veld Lengte in.</span><span class="sxs-lookup"><span data-stu-id="dc1df-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="dc1df-138">Voer een getal in het veld Breedte in.</span><span class="sxs-lookup"><span data-stu-id="dc1df-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="dc1df-139">Voer een getal in het veld Hoogte in.</span><span class="sxs-lookup"><span data-stu-id="dc1df-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="dc1df-140">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="dc1df-140">Click Save.</span></span>
12. <span data-ttu-id="dc1df-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="dc1df-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="dc1df-142">Verpakkingsprofielen instellen</span><span class="sxs-lookup"><span data-stu-id="dc1df-142">Set up packing profiles</span></span>
1. <span data-ttu-id="dc1df-143">Ga naar Magazijnbeheer > Instellingen > Verpakking > Verpakkingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="dc1df-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="dc1df-144">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="dc1df-144">Click New.</span></span>
3. <span data-ttu-id="dc1df-145">Typ een waarde in het veld Verpakkingsprofiel-ID.</span><span class="sxs-lookup"><span data-stu-id="dc1df-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="dc1df-146">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="dc1df-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dc1df-147">Typ of selecteer een waarde in het veld Afsluitingsprofiel-ID van container.</span><span class="sxs-lookup"><span data-stu-id="dc1df-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="dc1df-148">Een afsluitingsprofiel-ID voor containers is optioneel en is het standaardafsluitingsprofiel voor containers voor dit verpakkingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="dc1df-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="dc1df-149">Selecteer een optie in het veld Modus container-ID.</span><span class="sxs-lookup"><span data-stu-id="dc1df-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="dc1df-150">Met deze optie wordt bepaald of een container-ID automatisch wordt gegenereerd wanneer een container wordt gemaakt of dat een container-ID handmatig wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dc1df-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="dc1df-151">Typ of selecteer een waarde in het veld Containertype.</span><span class="sxs-lookup"><span data-stu-id="dc1df-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="dc1df-152">Het containertype wordt standaard worden gebruikt wanneer een nieuwe container wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dc1df-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="dc1df-153">Schakel het selectievakje Automatisch container maken bij sluiten van container in.</span><span class="sxs-lookup"><span data-stu-id="dc1df-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="dc1df-154">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="dc1df-154">Click Save.</span></span>
10. <span data-ttu-id="dc1df-155">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="dc1df-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="dc1df-156">Containerafsluitingsprofielen instellen</span><span class="sxs-lookup"><span data-stu-id="dc1df-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="dc1df-157">Ga naar Magazijnbeheer > Instellingen > Containers > Afsluitingsprofielen van container.</span><span class="sxs-lookup"><span data-stu-id="dc1df-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="dc1df-158">Met containerafsluitingsprofielen wordt bepaald wat er gebeurt wanneer een container wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="dc1df-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="dc1df-159">U kunt meerdere afsluitingsprofielen voor containers instellen.</span><span class="sxs-lookup"><span data-stu-id="dc1df-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="dc1df-160">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="dc1df-160">Click New.</span></span>
3. <span data-ttu-id="dc1df-161">Typ een waarde in het veld Afsluitingsprofiel-ID van container.</span><span class="sxs-lookup"><span data-stu-id="dc1df-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="dc1df-162">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="dc1df-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dc1df-163">Selecteer een optie in het veld Manifesteren op.</span><span class="sxs-lookup"><span data-stu-id="dc1df-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="dc1df-164">Geef op of manifesteren wordt gebruikt bij het afsluiten van containers of bij het bevestigen van de zending.</span><span class="sxs-lookup"><span data-stu-id="dc1df-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="dc1df-165">Voor manifesteren is Transportbeheer vereist.</span><span class="sxs-lookup"><span data-stu-id="dc1df-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="dc1df-166">Manifesteren moet in de transportengines worden geïmplementeerd. Anders werken ze niet.</span><span class="sxs-lookup"><span data-stu-id="dc1df-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="dc1df-167">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="dc1df-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="dc1df-168">Typ of selecteer een waarde in het veld Standaard locatie voor uiteindelijke verzending.</span><span class="sxs-lookup"><span data-stu-id="dc1df-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="dc1df-169">Dit is de locatie waarnaar producten worden verplaatst nadat de containers zijn gesloten.</span><span class="sxs-lookup"><span data-stu-id="dc1df-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="dc1df-170">Voor deze locatie moet een locatieprofiel zijn gedefinieerd in de magazijnparameters.</span><span class="sxs-lookup"><span data-stu-id="dc1df-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="dc1df-171">Typ of selecteer een waarde in het veld Gewichtseenheid.</span><span class="sxs-lookup"><span data-stu-id="dc1df-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="dc1df-172">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="dc1df-172">Click Save.</span></span>


