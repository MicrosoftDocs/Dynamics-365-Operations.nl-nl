---
title: Put to wall - put to store
description: Dit onderwerp bevat informatie over de functionaliteit Put to wall - put to store. Met deze functie kunt u scenario's afhandelen waarin u een product moet consolideren naar een inpakvoorbereidingsruimte op basis van configureerbare criteria. Dit helpt om de orderverzameltijd te verkorten omdat orderverzamelen op één doelnummerplaat mogelijk is en meer wegzetplaatsen kunnen worden gebruikt dan bij het clusterverzamelen.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425778"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="d6be1-105">Put to wall - put to store</span><span class="sxs-lookup"><span data-stu-id="d6be1-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6be1-106">Met de functie *Put to wall - put to store* kunt u scenario's afhandelen waarin u een product moet consolideren naar een inpakvoorbereidingsruimte op basis van configureerbare criteria.</span><span class="sxs-lookup"><span data-stu-id="d6be1-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="d6be1-107">Omdat deze functionaliteit orderverzamelen op één doelnummerplaat toestaat en meer wegzetposities kan gebruiken dan bij clusterverzamelen, hebben bedrijven die aan winkels leveren of kleine artikelen verwerken minder tijd nodig voor orderverzamelen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="d6be1-108">De werkstroom voor deze functionaliteit zorgt ervoor dat het verzamelde product naar een sorteerlocatie wordt gestuurd voor distributie in verschillende containertypen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="d6be1-109">Meestal bevat elke sorteerlocatie meerdere sorteerposities.</span><span class="sxs-lookup"><span data-stu-id="d6be1-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="d6be1-110">Elke sorteerpositie wordt toegewezen op basis van de criteria die zijn ingesteld door het bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="d6be1-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="d6be1-111">Standaardcriteria zijn de uiteindelijke bestemming, verzending of lading.</span><span class="sxs-lookup"><span data-stu-id="d6be1-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="d6be1-112">Nadat een product is ontvangen, wordt het gedistribueerd naar elke sorteerpositie op basis van de hoeveelheid die is gekoppeld aan de order, bestemming, verzending of lading.</span><span class="sxs-lookup"><span data-stu-id="d6be1-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="d6be1-113">Wanneer een container vol of volledig is, wordt deze verplaatst naar een faserings- of verzend locatie voor verdere verwerking, afhankelijk van het bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="d6be1-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="d6be1-114">Voor deze magazijn functionaliteit wordt ook naar andere namen verwezen, zoals 'put-to-light' en 'break opens'.</span><span class="sxs-lookup"><span data-stu-id="d6be1-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="d6be1-115">De functie voor uitgaande sortering inschakelen</span><span class="sxs-lookup"><span data-stu-id="d6be1-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="d6be1-116">Voordat u de functie *Put to wall - put to store* gebruikt, moet de functie *Uitgaande sortering* worden ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="d6be1-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="d6be1-117">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d6be1-118">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="d6be1-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d6be1-119">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="d6be1-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d6be1-120">**Functienaam:** *Uitgaande sortering*</span><span class="sxs-lookup"><span data-stu-id="d6be1-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="d6be1-121">De functie *Uitgaande sortering* kan worden gebruikt in combinatie met de functie *Organisatiebrede wavestapcode* als deze is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d6be1-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="d6be1-122">U moet deze functie ook inschakelen als u vooraf gedefinieerde codes wilt gebruiken die zijn ingesteld op wavestapcodes.</span><span class="sxs-lookup"><span data-stu-id="d6be1-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="d6be1-123">Schakel in het werkgebied **Functiebeheer** deze functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="d6be1-124">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="d6be1-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d6be1-125">**Functienaam:** *Organisatiebrede wave-stapcode*</span><span class="sxs-lookup"><span data-stu-id="d6be1-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="d6be1-126">Instellen</span><span class="sxs-lookup"><span data-stu-id="d6be1-126">Setup</span></span>

<span data-ttu-id="d6be1-127">Voor deze demo worden standaard Contoso-gegevens en magazijn *62* gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="d6be1-128">Sommige toevoegingen die verderop worden vermeld, worden ook gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="d6be1-129">Locatietype</span><span class="sxs-lookup"><span data-stu-id="d6be1-129">Location type</span></span>

1. <span data-ttu-id="d6be1-130">Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locatietypen**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="d6be1-131">Selecteer in het actievenster de optie **Nieuw** om een locatietype voor sorteren te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="d6be1-132">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-132">Set the following values:</span></span>

    - <span data-ttu-id="d6be1-133">**Locatietype:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="d6be1-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="d6be1-134">**Omschrijving:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="d6be1-135">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="d6be1-136">Parameters voor magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="d6be1-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="d6be1-137">Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="d6be1-138">Voer op het tabblad **Algemeen** op het sneltabblad **Locatietypen** in het veld **Locatietype voor sorteren** *SORTEREN* in.</span><span class="sxs-lookup"><span data-stu-id="d6be1-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="d6be1-139">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="d6be1-140">Locatieprofiel</span><span class="sxs-lookup"><span data-stu-id="d6be1-140">Location profile</span></span>

1. <span data-ttu-id="d6be1-141">Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="d6be1-142">Selecteer in het actievenster de optie **Nieuw** om een locatieprofiel voor de sorteerlocatie te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="d6be1-143">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6be1-144">**Locatieprofiel-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="d6be1-145">**Naam:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="d6be1-146">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6be1-147">**Locatie-indeling:** *INPAKKEN*</span><span class="sxs-lookup"><span data-stu-id="d6be1-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="d6be1-148">**Locatietype:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="d6be1-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="d6be1-149">**Bijhouden nummerplaat gebruiken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d6be1-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="d6be1-150">**Gemengde artikelen toestaan:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d6be1-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="d6be1-151">**Gemengde voorraadstatussen toestaan:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d6be1-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="d6be1-152">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="d6be1-153">Locaties</span><span class="sxs-lookup"><span data-stu-id="d6be1-153">Locations</span></span>

1. <span data-ttu-id="d6be1-154">Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="d6be1-155">Schakel het selectievakje **Controlecijfers genereren voor locatie** uit.</span><span class="sxs-lookup"><span data-stu-id="d6be1-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="d6be1-156">Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d6be1-157">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6be1-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d6be1-158">**Locatie:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="d6be1-159">**Locatieprofiel-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="d6be1-160">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="d6be1-161">Verpakkingsprofielen</span><span class="sxs-lookup"><span data-stu-id="d6be1-161">Packing profiles</span></span>

1. <span data-ttu-id="d6be1-162">Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Verpakkingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="d6be1-163">Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d6be1-164">**Verpakkingsprofiel-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="d6be1-165">**Omschrijving:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="d6be1-166">**Inpakbeleid voor container:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="d6be1-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="d6be1-167">**Modus container-id:** *automatisch*</span><span class="sxs-lookup"><span data-stu-id="d6be1-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="d6be1-168">**Containertype:** *PALLET 48X48*</span><span class="sxs-lookup"><span data-stu-id="d6be1-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="d6be1-169">**Automatisch container maken bij sluiten van container:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="d6be1-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="d6be1-170">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="d6be1-171">Wave-stapcodes</span><span class="sxs-lookup"><span data-stu-id="d6be1-171">Wave step codes</span></span>

<span data-ttu-id="d6be1-172">Als u de functie *Organisatiebrede wavestapcode* hebt ingeschakeld, stelt u de volgende code in.</span><span class="sxs-lookup"><span data-stu-id="d6be1-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="d6be1-173">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavestapcodes**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="d6be1-174">Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d6be1-175">**Wavestapcode:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="d6be1-176">**Beschrijving wavestap:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="d6be1-177">**Type wavestap:** *Sorteersjabloon*</span><span class="sxs-lookup"><span data-stu-id="d6be1-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="d6be1-178">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="d6be1-179">Uitgaande sorteersjabloon</span><span class="sxs-lookup"><span data-stu-id="d6be1-179">Outbound sorting template</span></span>

<span data-ttu-id="d6be1-180">De sorteersjabloon bepaalt of er sorteerposities worden gemaakt, welke criteria worden gebruikt en andere kenmerken van het sorteerproces.</span><span class="sxs-lookup"><span data-stu-id="d6be1-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="d6be1-181">Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Uitgaande sorteersjabloon**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="d6be1-182">Selecteer in het actievenster **Nieuw** om een sorteersjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="d6be1-183">Stel in de koptekst van de nieuwe sjabloon de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="d6be1-184">**Id van uitgaande sorteersjabloon:** *Wave sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="d6be1-185">**Beschrijving:** *Wave sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="d6be1-186">**Sorteersjabloontype:** *Wavevraag*</span><span class="sxs-lookup"><span data-stu-id="d6be1-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="d6be1-187">Dit veld bepaalt het proces waarvoor de sorteersjabloon wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="d6be1-188">De volgende waarden zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="d6be1-188">The following values are available:</span></span>

        - <span data-ttu-id="d6be1-189">**Wavevraag**: de sorteersjabloon wordt gebruikt voor het proces *Put to wall*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="d6be1-190">Dit sjabloontype wordt gebruikt om de verpakkingsplaats over te slaan en de voorraad rechtstreeks uit de wave te verwerken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="d6be1-191">U kunt dit type alleen gebruiken als de **sorteermethode** van het waveproces wordt opgenomen in de wavesjabloon.</span><span class="sxs-lookup"><span data-stu-id="d6be1-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="d6be1-192">**Container**: de sorteersjabloon wordt gebruikt voor het proces *Pallet opbouwen na verpakking*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="d6be1-193">Dit sjabloontype wordt gebruikt voor het verwerken van containers die worden gesloten op de verpakkingsplaats en moeten worden gesorteerd op pallets.</span><span class="sxs-lookup"><span data-stu-id="d6be1-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="d6be1-194">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6be1-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d6be1-195">**Locatie:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="d6be1-196">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6be1-197">**Verificatie sorteren:** *Positie scannen*</span><span class="sxs-lookup"><span data-stu-id="d6be1-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="d6be1-198">In dit veld wordt de verificatie gedefinieerd die is vereist tijdens het sorteren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="d6be1-199">De volgende waarden zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="d6be1-199">The following values are available:</span></span>

        - <span data-ttu-id="d6be1-200">None</span><span class="sxs-lookup"><span data-stu-id="d6be1-200">None</span></span>
        - <span data-ttu-id="d6be1-201">Nummerplaat scannen</span><span class="sxs-lookup"><span data-stu-id="d6be1-201">License plate scan</span></span>
        - <span data-ttu-id="d6be1-202">Positie scannen</span><span class="sxs-lookup"><span data-stu-id="d6be1-202">Position scan</span></span>

    - <span data-ttu-id="d6be1-203">**Werk maken bij positie sluiten:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d6be1-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="d6be1-204">Als deze optie wordt ingesteld op *Ja*, wordt werk gemaakt wanneer de positie is gesloten om voorraad te verplaatsen naar de definitieve verzendlocatie.</span><span class="sxs-lookup"><span data-stu-id="d6be1-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="d6be1-205">Als dit wordt ingesteld op *Nee*, wordt voorraad onmiddellijk verzameld op de order wanneer de positie wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="d6be1-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="d6be1-206">**Positietoewijzing:** *Handmatig*</span><span class="sxs-lookup"><span data-stu-id="d6be1-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="d6be1-207">In dit veld wordt het type positietoewijzing gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d6be1-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="d6be1-208">De volgende waarden zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="d6be1-208">The following values are available:</span></span>

        - <span data-ttu-id="d6be1-209">**Handmatig**: de gebruiker moet altijd aangeven op welke positie de voorraad moet worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="d6be1-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="d6be1-210">**Automatisch**: het systeem wijst de voorraad automatisch toe aan een positie, indien mogelijk op basis van de opsplitsingen in de sorteersjablonen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="d6be1-211">**Criteria voor sorteerpositie toewijzen:** *alleen lege positie gebruiken*</span><span class="sxs-lookup"><span data-stu-id="d6be1-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="d6be1-212">Met dit veld wordt bepaald of rekening wordt gehouden met voorraad die al aanwezig is op sorteerposities bij het toewijzen van een positie voor de vraag.</span><span class="sxs-lookup"><span data-stu-id="d6be1-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="d6be1-213">De volgende waarden zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="d6be1-213">The following values are available:</span></span>

        - <span data-ttu-id="d6be1-214">**Alleen lege positie gebruiken**: er wordt rekening gehouden met posities waaraan al voorraad is gekoppeld</span><span class="sxs-lookup"><span data-stu-id="d6be1-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="d6be1-215">**Aannemen dat positie leeg is**: alle voorraad die al op de positie staat, wordt tijdens de toewijzing genegeerd.</span><span class="sxs-lookup"><span data-stu-id="d6be1-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="d6be1-216">Alle beschikbare posities worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-216">All available positions will be used.</span></span>

    - <span data-ttu-id="d6be1-217">**Wavestapcode:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="d6be1-218">Als de functie *Organisatiebrede wave-stapcode* is ingeschakeld, moet de wavestapcode *Sorteren* ook worden ingesteld in wavestapcodes.</span><span class="sxs-lookup"><span data-stu-id="d6be1-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="d6be1-219">**Sorteerpositie automatisch sluiten:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d6be1-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="d6be1-220">Wanneer deze optie is ingesteld op *Ja*, wordt de sorteerpositie automatisch gesloten wanneer alle werk voor de positie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="d6be1-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="d6be1-221">**Aantal sorteerposities:** *3*</span><span class="sxs-lookup"><span data-stu-id="d6be1-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="d6be1-222">Dit veld bepaalt het maximumaantal sorteerposities dat door het systeem wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="d6be1-223">**Voorvoegsel sorteerpositie:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="d6be1-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="d6be1-224">Dit veld definieert het voorvoegsel dat het systeem vóór het positienummer toewijst.</span><span class="sxs-lookup"><span data-stu-id="d6be1-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="d6be1-225">**Sorteerpositie automatisch inpakken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d6be1-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="d6be1-226">Als deze optie wordt ingesteld op *Ja*, wordt de voorraad op de sorteerpositie in een container verpakt wanneer de positie wordt afgesloten.</span><span class="sxs-lookup"><span data-stu-id="d6be1-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="d6be1-227">**Verpakkingsprofiel-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="d6be1-228">In dit veld wordt het verpakkingsprofiel bepaald dat wordt gebruikt wanneer de sorteerpositie in een container wordt verpakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="d6be1-229">Selecteer in het actievenster **Query bewerken** om de criteria op te geven die worden gebruikt voor deze sorteersjabloon.</span><span class="sxs-lookup"><span data-stu-id="d6be1-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="d6be1-230">Selecteer in het querydialoogvenster op het tabblad **Sorteren** de optie **Nieuw** om een regel toe te voegen en stel vervolgens de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="d6be1-231">**Tabel:** *Gegevens lading*</span><span class="sxs-lookup"><span data-stu-id="d6be1-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="d6be1-232">**Afgeleide tabel:** *Gegevens lading*</span><span class="sxs-lookup"><span data-stu-id="d6be1-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="d6be1-233">**Veld:** *Zending-id*</span><span class="sxs-lookup"><span data-stu-id="d6be1-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="d6be1-234">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="d6be1-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="d6be1-235">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-235">Select **OK**.</span></span>
1. <span data-ttu-id="d6be1-236">Het volgende bericht kan worden weergegeven: 'Groeperen wordt opnieuw ingesteld, doorgaan?'</span><span class="sxs-lookup"><span data-stu-id="d6be1-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="d6be1-237">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-237">Select **Yes**.</span></span>

    <span data-ttu-id="d6be1-238">De knop **Onderbrekingen van sjabloon uitgaande sortering** in het actievenster wordt beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="d6be1-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="d6be1-239">Selecteer in het actievenster **Onderbrekingen van sjabloon uitgaande sortering**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="d6be1-240">Schakel het selectievakje **Groeperen op-veld** in om te groeperen op zending-id.</span><span class="sxs-lookup"><span data-stu-id="d6be1-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="d6be1-241">Met deze instelling wordt één sorteerpositie gemaakt per zending die een container in de wave is.</span><span class="sxs-lookup"><span data-stu-id="d6be1-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="d6be1-242">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="d6be1-243">Methoden voor verwerking van waves</span><span class="sxs-lookup"><span data-stu-id="d6be1-243">Wave process methods</span></span>

1. <span data-ttu-id="d6be1-244">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="d6be1-245">Selecteer in het actievenster **Methoden opnieuw genereren**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="d6be1-246">De **sorteer** methode wordt toegevoegd aan de lijst met beschikbare methoden en het sjabloontype *Zending* voor de wave wordt hiervoor geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="d6be1-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="d6be1-247">Wavesjablonen</span><span class="sxs-lookup"><span data-stu-id="d6be1-247">Wave templates</span></span>

<span data-ttu-id="d6be1-248">Bewerk de wavesjabloon die wordt gebruikt voor het sorteren van de wavevraag.</span><span class="sxs-lookup"><span data-stu-id="d6be1-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="d6be1-249">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="d6be1-250">Selecteer in het veld **Type wavesjabloon** de optie *Zending*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="d6be1-251">Selecteer de bestaande standaardsjabloon **62 zending**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="d6be1-252">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d6be1-253">Breng op het sneltabblad **Algemeen** de volgende wijzigingen aan:</span><span class="sxs-lookup"><span data-stu-id="d6be1-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="d6be1-254">Stel de optie **Wave verwerken bij vrijgave door magazijn** in op *Nee*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="d6be1-255">Stel de optie **Toewijzen aan open waves** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="d6be1-256">Stel op het sneltabblad **Methoden** de **sorteermethode** in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="d6be1-257">Selecteer **Sorteren** in het raster **Resterende methoden**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="d6be1-258">Selecteer de knop pijl-rechts om de methode **sorteren** te verplaatsen naar het raster **Geselecteerde methoden**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="d6be1-259">Selecteer **Sorteren** in het raster **Geselecteerde methoden**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="d6be1-260">Stel het veld **Wavestapcode** in op *Sorteren*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="d6be1-261">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="d6be1-262">Menuopties voor mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="d6be1-262">Mobile device menu items</span></span>

1. <span data-ttu-id="d6be1-263">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d6be1-264">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6be1-265">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6be1-266">**Naam menuopdracht:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="d6be1-267">**Titel:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="d6be1-268">**Modus:** *Indirect*</span><span class="sxs-lookup"><span data-stu-id="d6be1-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="d6be1-269">**Bestaand werk gebruiken:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="d6be1-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="d6be1-270">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6be1-271">**Activiteitscode:** *uitgaande sortering*</span><span class="sxs-lookup"><span data-stu-id="d6be1-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="d6be1-272">**Verwerkingsinstructies gebruiken:** *Ja* (standaardwaarde)</span><span class="sxs-lookup"><span data-stu-id="d6be1-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="d6be1-273">**Id van uitgaande sorteersjabloon:** *Wave sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="d6be1-274">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="d6be1-275">Menu voor mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="d6be1-275">Mobile device menu</span></span>

1. <span data-ttu-id="d6be1-276">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="d6be1-277">Selecteer in de lijst met menu's de waarde **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="d6be1-278">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d6be1-279">Zoek in het raster **Beschikbare menu's en menuopdrachten** de menuopdracht **Sorteren** die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="d6be1-280">Selecteer de knop pijl-rechts om **Sorteren** naar het raster **Menustructuur** te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="d6be1-281">Op deze manier voegt u de menuopdracht toe aan het menu **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="d6be1-282">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="d6be1-283">Locatie-instructies</span><span class="sxs-lookup"><span data-stu-id="d6be1-283">Location directives</span></span>

<span data-ttu-id="d6be1-284">U moet locatie-instructies maken om het werk te begeleiden dat wordt gemaakt nadat de sortering is voltooid.</span><span class="sxs-lookup"><span data-stu-id="d6be1-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="d6be1-285">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d6be1-286">Selecteer *Inkooporders* in het veld **Orderverzameling van gesorteerde voorraad**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="d6be1-287">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6be1-288">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6be1-289">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="d6be1-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="d6be1-290">**Naam:** *Wegzetten naar laaddeur*</span><span class="sxs-lookup"><span data-stu-id="d6be1-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="d6be1-291">Stel op het sneltabblad **Locatierichtlijnen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6be1-292">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="d6be1-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d6be1-293">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="d6be1-293">**Site:** *6*</span></span>
    - <span data-ttu-id="d6be1-294">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6be1-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d6be1-295">**Instructiecode:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="d6be1-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="d6be1-296">**Meerdere SKU's:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="d6be1-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="d6be1-297">Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d6be1-298">Selecteer **Nieuw** op het sneltabblad **Regels** en stel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="d6be1-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="d6be1-299">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="d6be1-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d6be1-300">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d6be1-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d6be1-301">**Vanaf hoeveelheid:** *0*</span><span class="sxs-lookup"><span data-stu-id="d6be1-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="d6be1-302">**Tot hoeveelheid:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d6be1-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="d6be1-303">Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d6be1-304">Selecteer **Nieuw** op het sneltabblad **Locatie-instructieacties** en stel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="d6be1-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="d6be1-305">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="d6be1-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d6be1-306">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d6be1-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d6be1-307">**Naam:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="d6be1-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="d6be1-308">Selecteer **Opslaan** om de knop **Query bewerken** op het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d6be1-309">Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d6be1-310">Zoek in het querydialoogvenster op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Locatie*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="d6be1-311">Stel het veld **Criteria** voor deze rij in op *Laaddeur*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="d6be1-312">Selecteer **OK** om de bewerking te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="d6be1-313">Werkklassen</span><span class="sxs-lookup"><span data-stu-id="d6be1-313">Work classes</span></span>

1. <span data-ttu-id="d6be1-314">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d6be1-315">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6be1-316">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6be1-317">**Werkklasse-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="d6be1-318">**Omschrijving:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="d6be1-319">**Type werkorder:** *Orderverzameling van gesorteerde voorraad*</span><span class="sxs-lookup"><span data-stu-id="d6be1-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="d6be1-320">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="d6be1-321">Werksjablonen</span><span class="sxs-lookup"><span data-stu-id="d6be1-321">Work templates</span></span>

1. <span data-ttu-id="d6be1-322">Ga naar **Magazijnbeheer \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d6be1-323">Selecteer *Verkooporders* in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="d6be1-324">Selecteer in het raster de werksjabloon **62 Orderverzamelen voor inpakken**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="d6be1-325">Selecteer **Opsplitsingen voor werkkoptekst** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="d6be1-326">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d6be1-327">Schakel op de regel waarvoor het veld **Veldnaam** is ingesteld op *Zending-id* het selectievakje **Groeperen op dit veld** uit.</span><span class="sxs-lookup"><span data-stu-id="d6be1-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="d6be1-328">Selecteer **Opslaan** en sluit het dialoogvenster **Opsplitsingen voor werkkoptekst**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="d6be1-329">Selecteer *Inkooporders* in het veld **Orderverzameling van gesorteerde voorraad**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="d6be1-330">Selecteer **Nieuw** om een werksjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="d6be1-331">Stel op de sectie **Overzicht** de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="d6be1-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="d6be1-332">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="d6be1-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d6be1-333">**Werksjabloon:** *Orderverzameling gesorteerd*</span><span class="sxs-lookup"><span data-stu-id="d6be1-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="d6be1-334">**Beschrijving werksjabloon:** *Orderverzameling gesorteerd*</span><span class="sxs-lookup"><span data-stu-id="d6be1-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="d6be1-335">Selecteer **Opslaan** om de sectie **Werksjabloongegevens** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="d6be1-336">Maak in de sectie **Details van werksjabloon** twee regels.</span><span class="sxs-lookup"><span data-stu-id="d6be1-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="d6be1-337">Selecteer **Nieuw** en stel de volgende waarden voor regel 1 in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="d6be1-338">**Werktype:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="d6be1-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d6be1-339">**Verplicht:** geselecteerd (= *Ja*)</span><span class="sxs-lookup"><span data-stu-id="d6be1-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="d6be1-340">**Werkklasse-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="d6be1-341">Selecteer nogmaals **Nieuw** en stel de volgende waarden voor regel 2 in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="d6be1-342">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="d6be1-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d6be1-343">**Verplicht:** geselecteerd (= *Ja*)</span><span class="sxs-lookup"><span data-stu-id="d6be1-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="d6be1-344">**Werkklasse-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="d6be1-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="d6be1-345">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="d6be1-346">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="d6be1-346">Example scenario</span></span>

<span data-ttu-id="d6be1-347">In dit scenario wordt een situatie gesimuleerd waarbij in het magazijn kleine artikelen op locaties worden opgeslagen die moeten worden ingepakt in dozen voordat ze worden verzonden, en waarbij de functionaliteit van het verpakkingsstation niet echt geschikt is.</span><span class="sxs-lookup"><span data-stu-id="d6be1-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="d6be1-348">Werknemers verzamelen orders voor meerdere klanten en verschillende adressen tegelijk om de verzamelsnelheid te verhogen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="d6be1-349">Nadat het orderverzamelen is voltooid, arriveren de werknemers op de sorteerlocatie, waar de verzamelde artikelen kunnen worden gesorteerd in de juiste doos op basis van vereiste criteria.</span><span class="sxs-lookup"><span data-stu-id="d6be1-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="d6be1-350">In dit voorbeeld wordt de zending-id gebruikt om de juiste doos te bepalen, omdat elke zending een ander adres heeft.</span><span class="sxs-lookup"><span data-stu-id="d6be1-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="d6be1-351">Nadat alle artikelen van de lading zijn ingepakt en gesorteerd op zending, worden de dozen verplaatst naar het klaarzetgebied en uiteindelijk op een truck geladen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="d6be1-352">Controleer voordat u het scenario start of alle standaard magazijnfuncties juist zijn ingesteld voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="d6be1-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="d6be1-353">Standaard wordt het Contoso-magazijn *62* gebruikt voor dit doeleinde.</span><span class="sxs-lookup"><span data-stu-id="d6be1-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="d6be1-354">Standaardconfiguraties zijn niet gewijzigd, behalve wat in de instellingen is beschreven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="d6be1-355">Vraag maken</span><span class="sxs-lookup"><span data-stu-id="d6be1-355">Create demand</span></span>

<span data-ttu-id="d6be1-356">Voordat u de functionaliteit kunt demonstreren, moet u een bepaalde vraag maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="d6be1-357">Voor dit scenario maakt u drie verkooporders voor drie verschillende klanten om verschillende afleveradressen te simuleren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="d6be1-358">Op deze manier maakt u drie afzonderlijke zendingen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="d6be1-359">Voordat u verkooprders en zendingen maakt, moet u er ook voor zorgen dat de orderverzamellocaties voldoende voorraad hebben voor alle artikelen op de orders.</span><span class="sxs-lookup"><span data-stu-id="d6be1-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="d6be1-360">Controleer de instellingen voor de locatie-instructie om de orderverzamellocaties te bevestigen worden gebruikt voor het verzamelen van verkooporders.</span><span class="sxs-lookup"><span data-stu-id="d6be1-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="d6be1-361">Als u de voorraad moet corrigeren, kunt u handmatige verplaatsingen maken en aanvulling of elke andere stroom gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="d6be1-362">Reserveer vervolgens de voorraad.</span><span class="sxs-lookup"><span data-stu-id="d6be1-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="d6be1-363">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d6be1-364">Selecteer **Nieuw** om een verkooporder voor order 1 te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="d6be1-365">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d6be1-366">**Klant:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d6be1-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="d6be1-367">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6be1-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d6be1-368">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-368">Select **OK**.</span></span>
1. <span data-ttu-id="d6be1-369">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d6be1-370">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-370">Set the following values:</span></span>

    - <span data-ttu-id="d6be1-371">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d6be1-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d6be1-372">**Hoeveelheid:** *5*</span><span class="sxs-lookup"><span data-stu-id="d6be1-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="d6be1-373">Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="d6be1-374">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="d6be1-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="d6be1-375">**Hoeveelheid:** *10*</span><span class="sxs-lookup"><span data-stu-id="d6be1-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="d6be1-376">Herhaal de volgende stappen voor elke verkoopregel op de order om de voorraad te reserveren:</span><span class="sxs-lookup"><span data-stu-id="d6be1-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="d6be1-377">Selecteer op het sneltabblad **Verkooporderregels** in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="d6be1-378">Ga naar de pagina **Reservering** en selecteer de optie **Partij reserveren** en sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="d6be1-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="d6be1-379">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-379">Select **Save**.</span></span>

1. <span data-ttu-id="d6be1-380">Selecteer **Nieuw** om een verkooporder voor order 2 te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="d6be1-381">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d6be1-382">**Klant:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="d6be1-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="d6be1-383">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6be1-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d6be1-384">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-384">Select **OK**.</span></span>
1. <span data-ttu-id="d6be1-385">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d6be1-386">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-386">Set the following values:</span></span>

    - <span data-ttu-id="d6be1-387">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d6be1-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d6be1-388">**Hoeveelheid:** *7*</span><span class="sxs-lookup"><span data-stu-id="d6be1-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="d6be1-389">Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="d6be1-390">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="d6be1-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="d6be1-391">**Hoeveelheid:** *3*</span><span class="sxs-lookup"><span data-stu-id="d6be1-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="d6be1-392">Herhaal de volgende stappen voor elke verkoopregel op de order om de voorraad te reserveren:</span><span class="sxs-lookup"><span data-stu-id="d6be1-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="d6be1-393">Selecteer op het sneltabblad **Verkooporderregels** in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="d6be1-394">Ga naar de pagina **Reservering** en selecteer de optie **Partij reserveren** en sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="d6be1-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="d6be1-395">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-395">Select **Save**.</span></span>

1. <span data-ttu-id="d6be1-396">Selecteer **Nieuw** om een verkooporder voor order 3 te maken.</span><span class="sxs-lookup"><span data-stu-id="d6be1-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="d6be1-397">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d6be1-398">**Klant:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="d6be1-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="d6be1-399">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6be1-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d6be1-400">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-400">Select **OK**.</span></span>
1. <span data-ttu-id="d6be1-401">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d6be1-402">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d6be1-402">Set the following values:</span></span>

    - <span data-ttu-id="d6be1-403">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d6be1-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d6be1-404">**Hoeveelheid:** *8*</span><span class="sxs-lookup"><span data-stu-id="d6be1-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="d6be1-405">Om voorraad te reserveren voor een verkoopregel, voert u de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="d6be1-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="d6be1-406">Selecteer op het sneltabblad **Verkooporderregels** in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="d6be1-407">Ga naar de pagina **Reservering** en selecteer de optie **Partij reserveren** en sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="d6be1-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="d6be1-408">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-408">Select **Save**.</span></span>

<span data-ttu-id="d6be1-409">Voer de volgende procedure uit om elke verkooporder vrij te geven in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="d6be1-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="d6be1-410">Er worden drie verschillende zendingen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-410">Three different shipments will be created.</span></span> <span data-ttu-id="d6be1-411">Vervolgens voegt u de drie zendingen toe aan één nieuwe wave.</span><span class="sxs-lookup"><span data-stu-id="d6be1-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="d6be1-412">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d6be1-413">Selecteer in het raster de eerste verkooporder die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="d6be1-414">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d6be1-415">U ontvangt een informatieve melding waarin de wave-id en zending-id worden vermeld die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="d6be1-416">Herhaal de vorige stappen om verkooporders 2 en 3 aan het magazijn vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="d6be1-417">Het informatiebericht dat u ontvangt, geeft aan dat er een zending is toegevoegd aan de wave die is gemaakt bij het vrijgegeven van verkooporder 1.</span><span class="sxs-lookup"><span data-stu-id="d6be1-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="d6be1-418">Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="d6be1-419">Selecteer de wave-id die is gemaakt op basis van de vrijgegeven verkooporders om de pagina **Waves** te openen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="d6be1-420">Op deze pagina worden de wavegegevens weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-420">This page shows the wave details.</span></span> <span data-ttu-id="d6be1-421">Op het sneltabblad **Waveregels** worden de zendingen weergegeven die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="d6be1-422">U moet nu werk maken om artikelen van de orderverzamellocaties naar de sorteerlocatie te brengen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="d6be1-423">Selecteer **Verwerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="d6be1-424">Tijdens de waveverwerking gebruikt de sorteermethode de sorteersjabloon om de voorraad toe te wijzen voor de sorteerposities.</span><span class="sxs-lookup"><span data-stu-id="d6be1-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="d6be1-425">Wanneer de waveverwerking is voltooid, ontvangt u een bericht om aan te geven dat de wave is geboekt en het werk is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="d6be1-426">Selecteer in het actievenster op het tabblad **Wave** in de groep **Verwante informatie** de optie **Werk** om het gemaakte werk weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="d6be1-427">Noteer de werk-id.</span><span class="sxs-lookup"><span data-stu-id="d6be1-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="d6be1-428">Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Toewijzingen uitgaande sorteerpositie**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="d6be1-429">In de linkerkolom kunt u de uitgaande sorteerpositie weergeven die voor elke zending is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="d6be1-430">Op het sneltabblad **Criteria sorteerpositie** kunt u de zending-id voor die positie weergeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="d6be1-431">Er is één werk-id gemaakt om voorraad van de orderverzamellocaties naar de sorteerlocatie te brengen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="d6be1-432">Als u het werk wilt voltooien, hebt u de werk-id nodig die tijdens de waveverwerking is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="d6be1-433">Orderverzameling van verkooporders naar de sorteerlocatie</span><span class="sxs-lookup"><span data-stu-id="d6be1-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="d6be1-434">Meld u aan bij de mobiele app als een medewerker in magazijn *62*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="d6be1-435">Selecteer **Uitgaand** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="d6be1-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d6be1-436">Selecteer **Orderverzamelen** in het menu **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="d6be1-437">Selecteer het veld **Id** en voer de werk-id van de waveverwerking in.</span><span class="sxs-lookup"><span data-stu-id="d6be1-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="d6be1-438">Bevestig uw invoer.</span><span class="sxs-lookup"><span data-stu-id="d6be1-438">Confirm your entry.</span></span>

    <span data-ttu-id="d6be1-439">Vervolgens wordt u gevraagd om een doelnummerplaat in te voeren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="d6be1-440">U ziet dat regel 1 van verkooporder 1 moet worden opgenomen en toegevoegd aan de doelnummerplaat.</span><span class="sxs-lookup"><span data-stu-id="d6be1-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="d6be1-441">Het artikelnummer, de hoeveelheid, de artikelomschrijving en de verzamellocatie worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="d6be1-442">Voer in het veld **Doel-LP** het nummer van de nummerplaat in.</span><span class="sxs-lookup"><span data-stu-id="d6be1-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="d6be1-443">U gaat alle regels verzamelen die van de verwerkte wave op dezelfde doelnummerplaat zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6be1-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="d6be1-444">Bevestig uw invoer.</span><span class="sxs-lookup"><span data-stu-id="d6be1-444">Confirm your entry.</span></span>

    <span data-ttu-id="d6be1-445">In de mobiele app wordt nu een reeks pagina's met **pickinstructies** weergegeven over de orderverzamellocatie, en het artikel en de hoeveelheid die moeten worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="d6be1-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="d6be1-446">Nadat het verzamelde artikel aan de nummerplaat is toegevoegd, bevestigt u het pickaantal.</span><span class="sxs-lookup"><span data-stu-id="d6be1-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="d6be1-447">De laatste pagina geeft het werk aan om de verzamelde artikelen op de sorteerlocatie te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="d6be1-448">Bevestig de eerste orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="d6be1-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="d6be1-449">De volgende orderverzameling wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-449">The next pick work is shown.</span></span> <span data-ttu-id="d6be1-450">Bevestig de orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="d6be1-450">Confirm the pick.</span></span>
1. <span data-ttu-id="d6be1-451">Ga door met het bevestigen van de resterende orderverzamelingen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="d6be1-452">De laatste stap is het voltooien van de wegzetwerkzaamheden.</span><span class="sxs-lookup"><span data-stu-id="d6be1-452">The last step is to complete the put work.</span></span> <span data-ttu-id="d6be1-453">Bevestig de opslag naar de sorteerlocatie.</span><span class="sxs-lookup"><span data-stu-id="d6be1-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="d6be1-454">U ziet de melding "Werk voltooid".</span><span class="sxs-lookup"><span data-stu-id="d6be1-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="d6be1-455">Sluit **Orderverzamelen** in de mobiele app af.</span><span class="sxs-lookup"><span data-stu-id="d6be1-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="d6be1-456">Sortering/put-to-wall</span><span class="sxs-lookup"><span data-stu-id="d6be1-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="d6be1-457">Nu alle voorraad op de sorteerlocatie is geplaatst, moet deze worden gesorteerd op de juiste sorteerpositie.</span><span class="sxs-lookup"><span data-stu-id="d6be1-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="d6be1-458">Meld u aan bij de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="d6be1-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="d6be1-459">Selecteer **Uitgaand** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="d6be1-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d6be1-460">Selecteer in het menu **Uitgaand** de optie **Sorteren** om de artikelen te gaan sorteren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="d6be1-461">Voer in het veld **LP/CON** de doelnummerplaat in van de verzamelde verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d6be1-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="d6be1-462">Bevestig uw invoer.</span><span class="sxs-lookup"><span data-stu-id="d6be1-462">Confirm your entry.</span></span>
1. <span data-ttu-id="d6be1-463">Voer het artikelnummer in dat u als eerste wilt sorteren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="d6be1-464">Het systeem bepaalt de eerste sorteerpositie die moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="d6be1-465">Bevestig de sorteerpositie.</span><span class="sxs-lookup"><span data-stu-id="d6be1-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="d6be1-466">U wordt gevraagd een nummerplaat aan de sorteerpositie toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="d6be1-467">Selecteer het veld **LP**, voer een nummer voor de nummerplaat in en bevestig uw invoer.</span><span class="sxs-lookup"><span data-stu-id="d6be1-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="d6be1-468">Omdat de sorteerpositie is gerelateerd aan de zending-id, kunt u de verzamelde artikelen op een nummerplaat sorteren die specifiek is voor de uitgaande zending en verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d6be1-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="d6be1-469">Op de volgende pagina worden de artikel-id, de hoeveelheid, de sorteerpositie-id en de nummerplaat-id's 'vanaf' (orderverzamelen) en 'naar' (sorteren) weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="d6be1-470">De informatie op deze pagina geeft aan dat u het opgegeven artikel en de hoeveelheden van de nummerplaat voor orderverzamelen te sorteren naar de nummerplaat voor het sorteren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="d6be1-471">Bevestig de sorteerpositie.</span><span class="sxs-lookup"><span data-stu-id="d6be1-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="d6be1-472">Sorteer de artikelen op de eerste sorteerpositie.</span><span class="sxs-lookup"><span data-stu-id="d6be1-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="d6be1-473">Wanneer u klaar bent, leidt het systeem u naar de volgende sorteerpositie.</span><span class="sxs-lookup"><span data-stu-id="d6be1-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="d6be1-474">Herhaal deze procedure voor alle verzamelde regels op de werkorder.</span><span class="sxs-lookup"><span data-stu-id="d6be1-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="d6be1-475">U moet dit proces ook gebruiken als er meerdere pickregels met hetzelfde artikelnummer zijn.</span><span class="sxs-lookup"><span data-stu-id="d6be1-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="d6be1-476">Wanneer u dit proces voor alle artikelen herhaalt, evalueert het systeem de criteria van het volgende gescande artikel (werkregel) en wordt bepaald op welke sorteerpositie het moet worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="d6be1-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="d6be1-477">U wordt automatisch doorverwezen om het artikel op de juiste sorteerpositie te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="d6be1-478">Afhankelijk van de bevestigingsinstellingen wordt u ook gevraagd om deze actie te bevestigen door het positienummer of de nummerplaat-id in te voeren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6be1-479">Als automatische sortering is ingeschakeld, is handmatig overschrijven niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="d6be1-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="d6be1-480">Wanneer u klaar bent, opent u in Microsoft Dynamics 365 Supply Chain Management de pagina **Toewijzingen voor uitgaande sorteerposities** om de status van de posities te controleren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="d6be1-481">Als posities automatisch worden gesloten, selecteert u **Gesloten weergeven** om de gesloten posities weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="d6be1-482">U ziet dat de transacties van de sorteerpositie worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="d6be1-483">Het artikel en de hoeveelheid die via de positie zijn verwerkt, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="d6be1-484">Wanneer u de sjabloon voor uitgaande sorteervolgorde instelt, stelt u de optie **Sorteerpositie automatisch sluiten** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d6be1-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="d6be1-485">Daarom wordt de positie automatisch gesloten wanneer de laatste verwachte voorraad is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="d6be1-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="d6be1-486">De sorteerposities hebben de status **Gesloten** en werk is gemaakt om de gesorteerde voorraad naar de locatie *Laaddeur* te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="d6be1-487">Voltooi de gesorteerde voorraadpicks om de voorraad naar de verzendlocatie te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="d6be1-488">Wanneer de voorraad gereed is, moet u de verzending bevestigen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="d6be1-489">Voor een correcte verwerking van gesorteerde voorraadpicks kan een menuopdracht van het mobiele apparaat met een werkklasse-id waarvoor het veld **Werkordertype** is ingesteld op *Gesorteerde voorraadverzameling*, worden gebruikt voor het verplaats- en laadproces.</span><span class="sxs-lookup"><span data-stu-id="d6be1-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="d6be1-490">Handmatig een positie sluiten (optioneel)</span><span class="sxs-lookup"><span data-stu-id="d6be1-490">Manually close a position (optional)</span></span>

<span data-ttu-id="d6be1-491">Als de sorteerposities handmatig moeten worden gesloten, moet de optie **Sorteerpositie automatisch sluiten** voor de uitgaande sorteersjabloon zijn ingesteld op *Nee* en moet er worden afgesloten voordat de voorraad kan worden verplaatst naar het laaddeurgebied.</span><span class="sxs-lookup"><span data-stu-id="d6be1-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="d6be1-492">Posities kunnen op verschillende manieren worden gesloten:</span><span class="sxs-lookup"><span data-stu-id="d6be1-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="d6be1-493">Via de magazijnapp:</span><span class="sxs-lookup"><span data-stu-id="d6be1-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="d6be1-494">De gebruiker kan een van de artikelen scannen die zich al op de positie bevinden en vervolgens **Sluiten** selecteren om de positie te sluiten.</span><span class="sxs-lookup"><span data-stu-id="d6be1-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="d6be1-495">Als de gebruiker een container scant die al is gesorteerd, wordt een foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6be1-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="d6be1-496">De gebruiker kan echter wel doorgaan met het sluiten van de positie.</span><span class="sxs-lookup"><span data-stu-id="d6be1-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="d6be1-497">Op de pagina Microsoft Dynamics 365 Supply Chain Management **Toewijzingen voor uitgaande sorteerposities**:</span><span class="sxs-lookup"><span data-stu-id="d6be1-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="d6be1-498">De gebruiker kan de uitgaande positierecord selecteren en vervolgens **Positie sluiten** selecteren in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d6be1-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="d6be1-499">Tips</span><span class="sxs-lookup"><span data-stu-id="d6be1-499">Tips</span></span>

- <span data-ttu-id="d6be1-500">Artikelen kunnen niet worden verplaatst tussen posities nadat ze aan een positie zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d6be1-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="d6be1-501">Het systeem evalueert hoeveel van elk artikel naar een bepaalde positie moet gaan.</span><span class="sxs-lookup"><span data-stu-id="d6be1-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="d6be1-502">Sorteersjablonen kunnen zo worden geconfigureerd dat er automatisch containers worden gemaakt wanneer posities worden gesloten.</span><span class="sxs-lookup"><span data-stu-id="d6be1-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="d6be1-503">Met deze aanpak wordt een standaardstructuur met container-id's gemaakt die is gebaseerd op het opgegeven verpakkingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="d6be1-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6be1-504">Nadat de verplaatsingswerkzaamheden zijn gemaakt op basis van de sorteerlocatie, moet u het werk niet annuleren.</span><span class="sxs-lookup"><span data-stu-id="d6be1-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="d6be1-505">Anders worden de positie en de containers uit het systeem verwijderd en zijn ze niet beschikbaar voor verdere verwerking.</span><span class="sxs-lookup"><span data-stu-id="d6be1-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="d6be1-506">De voorraad wordt ook verwijderd.</span><span class="sxs-lookup"><span data-stu-id="d6be1-506">The inventory will also be removed.</span></span>
