---
title: Uitgaand sorteren
description: Dit onderwerp biedt informatie over uitgaand sorteren. Deze functionaliteit vereenvoudigt het verwerken van kleine containers en helpt magazijnmedewerkers de palletcapaciteit in de vrachtwagen beter te plannen en te organiseren.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e72249e26fb8f291f804cf5f2e4ce98bf88cd5bf
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596216"
---
# <a name="outbound-sorting"></a><span data-ttu-id="eba45-104">Uitgaand sorteren</span><span class="sxs-lookup"><span data-stu-id="eba45-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eba45-105">Deze functionaliteit vereenvoudigt het verwerken van kleine containers en helpt magazijnmedewerkers de palletcapaciteit in de vrachtwagen beter te plannen en te organiseren.</span><span class="sxs-lookup"><span data-stu-id="eba45-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="eba45-106">Wanneer u uitgaand sorteren gebruikt, kunt u verpakte containers naar de juiste pallet sorteren nadat deze op een inpakstation zijn geweest.</span><span class="sxs-lookup"><span data-stu-id="eba45-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="eba45-107">U kunt ook een inpakhiërarchie maken.</span><span class="sxs-lookup"><span data-stu-id="eba45-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="eba45-108">Met deze functie kunt u pallets maken vanuit containers die zijn verpakt via de inpakfunctionaliteit.</span><span class="sxs-lookup"><span data-stu-id="eba45-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="eba45-109">De container wordt niet naar de uiteindelijke verzendlocatie verzonden, omdat deze zich in de oorspronkelijke inpakstroom bevindt.</span><span class="sxs-lookup"><span data-stu-id="eba45-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="eba45-110">In plaats daarvan kunnen werknemers de container sluiten en verplaatsen naar een locatie van het sorteertype.</span><span class="sxs-lookup"><span data-stu-id="eba45-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="eba45-111">Ze kunnen vervolgens containers sorteren op posities die elk een nummerplaat (LP) hebben.</span><span class="sxs-lookup"><span data-stu-id="eba45-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="eba45-112">Nadat de containers zijn gesorteerd, kunt u werk maken om de gehele LP te verzenden naar de uiteindelijke verzend- of faseringslocaties, op basis van locatierichtlijnen of uw eigen vereisten.</span><span class="sxs-lookup"><span data-stu-id="eba45-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="eba45-113">Bovendien kan de actie van het afsluiten van de sorteerpositie de voorraad onmiddellijk naar de uiteindelijke verzendlocatie verplaatsen en de order verzamelen.</span><span class="sxs-lookup"><span data-stu-id="eba45-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="eba45-114">De functie voor uitgaande sortering inschakelen</span><span class="sxs-lookup"><span data-stu-id="eba45-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="eba45-115">Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="eba45-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="eba45-116">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="eba45-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="eba45-117">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="eba45-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="eba45-118">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="eba45-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="eba45-119">**Functienaam:** *Uitgaande sortering*</span><span class="sxs-lookup"><span data-stu-id="eba45-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="eba45-120">Instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-120">Setup</span></span>

<span data-ttu-id="eba45-121">Voor dit scenario moet u standaard **USMF**-demogegevens en magazijn *62*gebruiken.</span><span class="sxs-lookup"><span data-stu-id="eba45-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="eba45-122">U moet ook de instellingen voltooien die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="eba45-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="eba45-123">Een wavesjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-123">Set up a wave template</span></span>

<span data-ttu-id="eba45-124">Met deze instellingen wordt de wave automatisch verwerkt en wordt werk gemaakt wanneer een regel aan het magazijn wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="eba45-125">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="eba45-126">Selecteer **Magazijn 62** in de lijst met sjablonen.</span><span class="sxs-lookup"><span data-stu-id="eba45-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="eba45-127">Controleer op het sneltabblad **Algemeen** of de optie **Wave verwerken bij vrijgave door magazijn** is ingesteld op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="eba45-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="eba45-128">Een werknemer instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-128">Set up a worker</span></span>

<span data-ttu-id="eba45-129">Het inpakstation wordt gezien als een locatie.</span><span class="sxs-lookup"><span data-stu-id="eba45-129">The packing station is considered a location.</span></span> <span data-ttu-id="eba45-130">Magazijnmedewerkers die zich aanmelden bij het inpakstation zien en werken aan alleen verzendingen en containers die op die specifieke inpaklocatie zijn gepland.</span><span class="sxs-lookup"><span data-stu-id="eba45-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="eba45-131">Een gebruiker die zich aanmeldt bij Microsoft Dynamics 365, moet als werknemer zijn ingesteld in Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="eba45-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="eba45-132">Als de naam van de gebruiker niet wordt weergegeven in de lijst met werknemers, gebruikt u de volgende procedure om ze toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="eba45-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="eba45-133">Bij deze stappen wordt ervan uitgegaan dat de gebruiker al bestaat in het systeem en is gekoppeld als een werknemer of medewerker in de module **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="eba45-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="eba45-134">Ga naar **Magazijnbeheer \> Instellen \> Medewerker**.</span><span class="sxs-lookup"><span data-stu-id="eba45-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="eba45-135">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="eba45-135">Select **New**.</span></span>
1. <span data-ttu-id="eba45-136">Selecteer in het veld **Medewerker** de doelgebruiker in de lijst met werknemers.</span><span class="sxs-lookup"><span data-stu-id="eba45-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="eba45-137">Selecteer **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="eba45-137">Select **Select**.</span></span>
1. <span data-ttu-id="eba45-138">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="eba45-139">Selecteer in het sneltabblad **Gebruikers** de optie **Nieuw** om een account voor een mobiel apparaat te maken en stel hiervoor de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="eba45-140">**Gebruikers-id:** voer een unieke id in.</span><span class="sxs-lookup"><span data-stu-id="eba45-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="eba45-141">**Gebruikersnaam:** voer een naam in voor de id.</span><span class="sxs-lookup"><span data-stu-id="eba45-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="eba45-142">**Standaardmagazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="eba45-143">**Menunaam:** *Hoofd*</span><span class="sxs-lookup"><span data-stu-id="eba45-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="eba45-144">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="eba45-145">Het dialoogvenster **Wachtwoord instellen** wordt weergegeven. Maak een eenvoudig wachtwoord dat de gebruiker kan gebruiken om zich aan te melden bij de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="eba45-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="eba45-146">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-146">Set the following values:</span></span>

    - <span data-ttu-id="eba45-147">**Wachtwoord:** geef een eenvoudig wachtwoord op.</span><span class="sxs-lookup"><span data-stu-id="eba45-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="eba45-148">**Wachtwoord bevestigen:** voer nogmaals hetzelfde wachtwoord in.</span><span class="sxs-lookup"><span data-stu-id="eba45-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="eba45-149">Selecteer **Wachtwoord instellen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-149">Select **Set password**.</span></span>

    <span data-ttu-id="eba45-150">Een melding in het actiecentrum geeft aan dat het wachtwoord is ingesteld voor de gebruiker die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eba45-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="eba45-151">Een locatietype maken</span><span class="sxs-lookup"><span data-stu-id="eba45-151">Create a location type</span></span>

1. <span data-ttu-id="eba45-152">Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locatietypen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="eba45-153">Selecteer in het actievenster de optie **Nieuw** om een locatietype te maken en stel hiervoor de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="eba45-154">**Locatietype:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="eba45-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="eba45-155">**Omschrijving:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="eba45-156">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="eba45-157">Parameters voor Magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="eba45-158">Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="eba45-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="eba45-159">Stel op het tabblad **Algemeen** op het sneltabblad **Locatietypen** het veld **Locatietype voor sorteren** in op *SORTEREN*.</span><span class="sxs-lookup"><span data-stu-id="eba45-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="eba45-160">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="eba45-161">Een locatieprofiel instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-161">Set up a location profile</span></span>

1. <span data-ttu-id="eba45-162">Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="eba45-163">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-164">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="eba45-165">**Locatieprofiel-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="eba45-166">**Naam:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="eba45-167">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-168">**Locatie-indeling:** *ASRB* (gang-rek-plank-bak)</span><span class="sxs-lookup"><span data-stu-id="eba45-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="eba45-169">**Locatietype:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="eba45-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="eba45-170">**Bijhouden nummerplaat gebruiken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="eba45-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="eba45-171">**Gemengde artikelen toestaan:** *Ja* (wanneer u deze optie op *Ja* instelt, wordt de optie **Gemengde voorraadbatches toestaan** automatisch ingesteld op *Ja* en kan dit niet onafhankelijk worden gewijzigd.)</span><span class="sxs-lookup"><span data-stu-id="eba45-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="eba45-172">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="eba45-173">Een locatie instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-173">Set up a location</span></span>

1. <span data-ttu-id="eba45-174">Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.</span><span class="sxs-lookup"><span data-stu-id="eba45-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="eba45-175">Schakel in de koptekst het selectievakje **Controlecijfers genereren voor locatie** uit.</span><span class="sxs-lookup"><span data-stu-id="eba45-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="eba45-176">Selecteer in het actievenster de optie **Nieuw** om een locatie te maken en stel hiervoor de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="eba45-177">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eba45-178">**Locatie:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eba45-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="eba45-179">**Locatieprofiel-id:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="eba45-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="eba45-180">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="eba45-181">Een sjabloon voor uitgaande sortering instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="eba45-182">Met de sjabloon voor uitgaande sortering wordt bepaald of werk wordt gemaakt op basis van de sorteerlocatie en of handmatig of automatisch wordt gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="eba45-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="eba45-183">Voor dit scenario maakt u een uitgaande sorteersjabloon om pallets op te bouwen na het inpakstation.</span><span class="sxs-lookup"><span data-stu-id="eba45-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="eba45-184">Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Uitgaande sorteersjabloon**.</span><span class="sxs-lookup"><span data-stu-id="eba45-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="eba45-185">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-186">Stel in de koptekst van de nieuwe sjabloon de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="eba45-187">**Id van uitgaande sorteersjabloon:** *AutoWerk*</span><span class="sxs-lookup"><span data-stu-id="eba45-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="eba45-188">**Omschrijving:** *Automatisch werk maken*</span><span class="sxs-lookup"><span data-stu-id="eba45-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="eba45-189">**Sjabloontype uitgaande sortering:** *container*</span><span class="sxs-lookup"><span data-stu-id="eba45-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="eba45-190">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eba45-191">**Locatie:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eba45-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="eba45-192">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-193">**Verificatie sorteren:** *Positie scannen*</span><span class="sxs-lookup"><span data-stu-id="eba45-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="eba45-194">**Werk maken bij positie sluiten:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="eba45-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="eba45-195">Als deze optie wordt ingesteld op *Ja*, wordt werk gemaakt wanneer de positie is gesloten om voorraad te verplaatsen naar de definitieve verzendlocatie.</span><span class="sxs-lookup"><span data-stu-id="eba45-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="eba45-196">Als dit wordt ingesteld op *Nee*, wordt voorraad onmiddellijk verzameld op de order wanneer de positie wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="eba45-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="eba45-197">**Positietoewijzing:** *automatisch*</span><span class="sxs-lookup"><span data-stu-id="eba45-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="eba45-198">Als dit veld wordt ingesteld op *Handmatig*, moet de gebruiker altijd aangeven op welke positie de voorraad moet worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="eba45-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="eba45-199">Als dit wordt ingesteld op *Automatisch* wijst het systeem de voorraad automatisch toe aan een positie, indien mogelijk op basis van de opsplitsingen in de sorteersjablonen.</span><span class="sxs-lookup"><span data-stu-id="eba45-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="eba45-200">Selecteer **Opslaan** om de optie **Query bewerken** beschikbaar te maken in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="eba45-201">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="eba45-202">Voeg in de query-editor op het tabblad **Sorteren** een regel toe met de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="eba45-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="eba45-203">**Tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="eba45-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="eba45-204">**Afgeleide tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="eba45-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="eba45-205">**Veld:** *Vervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="eba45-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="eba45-206">Wanneer u deze waarde hebt geselecteerd, kan de volgende melding worden weergegeven: "Vervoerdersservice is geen indexveld.</span><span class="sxs-lookup"><span data-stu-id="eba45-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="eba45-207">Wilt u hieraan sortering toevoegen?"</span><span class="sxs-lookup"><span data-stu-id="eba45-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="eba45-208">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="eba45-208">Select **Yes**.</span></span>

    - <span data-ttu-id="eba45-209">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="eba45-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="eba45-210">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-210">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-211">Het volgende bericht kan worden weergegeven: 'Groeperen wordt opnieuw ingesteld, doorgaan?'</span><span class="sxs-lookup"><span data-stu-id="eba45-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="eba45-212">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="eba45-212">Select **Yes**.</span></span>

    <span data-ttu-id="eba45-213">De knop **Onderbrekingen van sjabloon uitgaande sortering** in het actievenster wordt beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="eba45-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="eba45-214">Selecteer in het actievenster **Onderbrekingen van sjabloon uitgaande sortering**.</span><span class="sxs-lookup"><span data-stu-id="eba45-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="eba45-215">Stel in het dialoogvenster **Criteria voor uitgaande sortering** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eba45-216">**Naam verwijzingstabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="eba45-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="eba45-217">**Naam verwijzingsveld:** *Vervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="eba45-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="eba45-218">**Groeperen op-veld:** schakel dit selectievakje in om zendingen te groeperen op vervoerdersservice.</span><span class="sxs-lookup"><span data-stu-id="eba45-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="eba45-219">Selecteer **OK** om de instellingen op te slaan en het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eba45-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="eba45-220">Inpakbeleid voor container instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-220">Set up container packing policies</span></span>

1. <span data-ttu-id="eba45-221">Ga naar **Magazijnbeheer \> Instellen \> Containers \> Inpakbeleid voor container**.</span><span class="sxs-lookup"><span data-stu-id="eba45-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="eba45-222">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-223">Stel in de koptekst van het nieuwe beleid de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="eba45-224">**Inpakbeleid voor container:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="eba45-225">**Omschrijving:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="eba45-226">Stel op het sneltabblad **Overzicht** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-227">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eba45-228">**Standaardlocatie voor sorteren:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="eba45-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="eba45-229">**Gewichteenheid:** *kg*</span><span class="sxs-lookup"><span data-stu-id="eba45-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="eba45-230">**Beleid van de containerafsluiting:** *automatische vrijgave*</span><span class="sxs-lookup"><span data-stu-id="eba45-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="eba45-231">**Vrijgavebeleid voor container:** *container aan uitgaande sorteerpositie toewijzen*</span><span class="sxs-lookup"><span data-stu-id="eba45-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="eba45-232">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="eba45-233">Verpakkingsprofielen instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-233">Set up packing profiles</span></span>

<span data-ttu-id="eba45-234">Maak een nieuw inpakprofiel dat wordt gebruikt in combinatie met de sorteerfunctionaliteit.</span><span class="sxs-lookup"><span data-stu-id="eba45-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="eba45-235">Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Verpakkingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="eba45-236">Selecteer in het actievenster de optie **Nieuw** om een regel te maken en stel hiervoor de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="eba45-237">**Verpakkingsprofiel-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="eba45-238">**Omschrijving:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="eba45-239">**Inpakbeleid voor container:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="eba45-240">**Modus container-id:** *automatisch*</span><span class="sxs-lookup"><span data-stu-id="eba45-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="eba45-241">**Containertype:** *doos-groot*</span><span class="sxs-lookup"><span data-stu-id="eba45-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="eba45-242">**Container automatisch maken bij sluiten van container:** uitgeschakeld (= *Nee*)</span><span class="sxs-lookup"><span data-stu-id="eba45-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="eba45-243">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="eba45-244">Werkklassen instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-244">Set up work classes</span></span>

<span data-ttu-id="eba45-245">Stel een werkklasse in die wordt gebruikt in combinatie met sorteren.</span><span class="sxs-lookup"><span data-stu-id="eba45-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="eba45-246">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="eba45-247">Selecteer in het actievenster de optie **Nieuw** om een werkklasse voor sorteren te maken en stel hiervoor de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="eba45-248">**Werkklasse-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="eba45-249">**Omschrijving:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="eba45-250">**Type werkorder:** *Orderverzameling van gesorteerde voorraad*</span><span class="sxs-lookup"><span data-stu-id="eba45-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="eba45-251">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="eba45-252">Menuopdrachten voor een mobiel apparaat instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="eba45-253">Een nieuwe menuopdracht voor pallets instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="eba45-254">Maak een menuopdracht voor mobiele apparaten om pallets op te bouwen tijdens het sorteren.</span><span class="sxs-lookup"><span data-stu-id="eba45-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="eba45-255">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="eba45-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="eba45-256">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-257">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="eba45-258">**Naam van menuopdracht:** *Pallet opbouwen*</span><span class="sxs-lookup"><span data-stu-id="eba45-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="eba45-259">**Titel:** *Pallet opbouwen*</span><span class="sxs-lookup"><span data-stu-id="eba45-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="eba45-260">**Modus:** *indirect*</span><span class="sxs-lookup"><span data-stu-id="eba45-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="eba45-261">**Bestaand werk gebruiken:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="eba45-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="eba45-262">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-263">**Activiteitscode:** *uitgaande sortering*</span><span class="sxs-lookup"><span data-stu-id="eba45-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="eba45-264">Als dit veld is ingesteld op *Uitgaande sortering*, wordt het veld **Id van uitgaande sorteersjabloon** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="eba45-265">**Verwerkingsinstructies gebruiken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="eba45-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="eba45-266">Als het veld **Activiteitscode** is ingesteld op *Uitgaande sortering*, wordt deze optie automatisch ingesteld op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="eba45-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="eba45-267">**Id van uitgaande sorteersjabloon:** *AutoWerk*</span><span class="sxs-lookup"><span data-stu-id="eba45-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="eba45-268">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="eba45-269">Een nieuwe menuopdracht voor laden instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-269">Set up a new loading menu item</span></span>

<span data-ttu-id="eba45-270">Maak vervolgens een menuopdracht waarmee gebruikers de gesorteerde voorraadartikelen kunnen verplaatsen naar de verzendlocatie.</span><span class="sxs-lookup"><span data-stu-id="eba45-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="eba45-271">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="eba45-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="eba45-272">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-273">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="eba45-274">**Naam menuopdracht:** *Laden uit sortering*</span><span class="sxs-lookup"><span data-stu-id="eba45-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="eba45-275">**Titel:** *Laden uit sortering*</span><span class="sxs-lookup"><span data-stu-id="eba45-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="eba45-276">**Modus:** *werk*</span><span class="sxs-lookup"><span data-stu-id="eba45-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="eba45-277">**Bestaand werk gebruiken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="eba45-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="eba45-278">Op het sneltabblad **Algemeen** moet het veld **Bestuurd door** zijn ingesteld op *Door gebruiker bestuurd*.</span><span class="sxs-lookup"><span data-stu-id="eba45-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="eba45-279">Selecteer **Nieuw** op het sneltabblad **Werkklassen** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="eba45-280">**Werkklasse-id:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="eba45-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="eba45-281">**Type werkorder:** *Orderverzameling van gesorteerde voorraad*</span><span class="sxs-lookup"><span data-stu-id="eba45-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="eba45-282">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="eba45-283">Het menu voor het mobiele apparaat instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-283">Set up the mobile device menu</span></span>

<span data-ttu-id="eba45-284">U moet nu de nieuwe menuopdrachten toevoegen aan het menu voor het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="eba45-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="eba45-285">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="eba45-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="eba45-286">Selecteer het menu **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="eba45-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="eba45-287">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="eba45-288">Zoek en selecteer **Pallet opbouwen** in de kolom **Beschikbare menu's en menu opdrachten**.</span><span class="sxs-lookup"><span data-stu-id="eba45-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="eba45-289">Selecteer de pijl naar rechts om **Pallet opbouwen** naar de kolom **Menustructuur** te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="eba45-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="eba45-290">Gebruik de knoppen pijl omhoog en pijl omlaag om de menuopdracht **Pallet opbouwen** op de gewenste positie in het menu van het mobiele apparaat te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="eba45-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="eba45-291">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-291">Select **Save**.</span></span>
1. <span data-ttu-id="eba45-292">Herhaal deze procedure om de menuoptie **Laden uit sorteren** toe te voegen aan het menu **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="eba45-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="eba45-293">Locatie-instructies instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-293">Set up location directives</span></span>

<span data-ttu-id="eba45-294">De *locatierichtlijnen* zijn regels die verzamelings- en wegzetlocaties identificeren voor voorraadverplaatsing.</span><span class="sxs-lookup"><span data-stu-id="eba45-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="eba45-295">U moet nu een regel maken om het sorteerwerk te beheren.</span><span class="sxs-lookup"><span data-stu-id="eba45-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="eba45-296">Een richtlijn voor een enkele SKU instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="eba45-297">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="eba45-298">Wijzig in het linkerdeelvenster de waarde van het veld **Werkordertype** in *Orderverzameling van gesorteerde voorraad*.</span><span class="sxs-lookup"><span data-stu-id="eba45-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="eba45-299">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-300">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="eba45-301">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eba45-302">**Naam:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="eba45-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="eba45-303">Stel op het sneltabblad **Locatierichtlijnen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-304">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="eba45-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="eba45-305">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="eba45-305">**Site:** *6*</span></span>
    - <span data-ttu-id="eba45-306">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eba45-307">**Meerdere SKU's:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="eba45-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="eba45-308">Selecteer **Opslaan** om de werkbalk op het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="eba45-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="eba45-309">Selecteer **Nieuw** op het sneltabblad **Regels** en stel de volgende waarden in op de nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="eba45-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="eba45-310">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="eba45-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="eba45-311">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eba45-312">**Van:** *0*</span><span class="sxs-lookup"><span data-stu-id="eba45-312">**From:** *0*</span></span>
    - <span data-ttu-id="eba45-313">**Tot:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="eba45-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="eba45-314">Selecteer **Opslaan** om de werkbalk op het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="eba45-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="eba45-315">Selecteer **Nieuw** op het sneltabblad **Locatie-instructieacties** en stel de volgende waarden in op de nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="eba45-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="eba45-316">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="eba45-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="eba45-317">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eba45-318">**Naam:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="eba45-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="eba45-319">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-319">Select **Save**.</span></span>
1. <span data-ttu-id="eba45-320">Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="eba45-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="eba45-321">Zoek in de query-editor op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Locatie*.</span><span class="sxs-lookup"><span data-stu-id="eba45-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="eba45-322">Stel het veld **Criteria** voor deze rij in op *Laaddeur*.</span><span class="sxs-lookup"><span data-stu-id="eba45-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="eba45-323">Selecteer **OK** om de instellingen op te slaan en de query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eba45-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="eba45-324">Een richtlijn voor meerdere SKU's instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="eba45-325">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="eba45-326">Wijzig in het linkerdeelvenster de waarde van het veld **Werkordertype** in *Orderverzameling van gesorteerde voorraad*.</span><span class="sxs-lookup"><span data-stu-id="eba45-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="eba45-327">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-328">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="eba45-329">**Reeks:** *2*</span><span class="sxs-lookup"><span data-stu-id="eba45-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="eba45-330">**Naam:** *Meerdere laaddeuren*</span><span class="sxs-lookup"><span data-stu-id="eba45-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="eba45-331">Stel op het sneltabblad **Locatierichtlijnen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-332">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="eba45-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="eba45-333">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="eba45-333">**Site:** *6*</span></span>
    - <span data-ttu-id="eba45-334">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eba45-335">**Meerdere SKU'S:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="eba45-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="eba45-336">Selecteer **Opslaan** om de werkbalk op het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="eba45-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="eba45-337">Selecteer **Nieuw** op het sneltabblad **Regels** en stel de volgende waarden in op de nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="eba45-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="eba45-338">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="eba45-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="eba45-339">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eba45-340">**Van:** *0*</span><span class="sxs-lookup"><span data-stu-id="eba45-340">**From:** *0*</span></span>
    - <span data-ttu-id="eba45-341">**Tot:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="eba45-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="eba45-342">Selecteer **Opslaan** om de werkbalk op het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="eba45-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="eba45-343">Selecteer **Nieuw** op het sneltabblad **Locatie-instructieacties** en stel de volgende waarden in op de nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="eba45-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="eba45-344">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="eba45-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="eba45-345">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eba45-346">**Naam:** *Meerdere laaddeuren*</span><span class="sxs-lookup"><span data-stu-id="eba45-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="eba45-347">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-347">Select **Save**.</span></span>
1. <span data-ttu-id="eba45-348">Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="eba45-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="eba45-349">Zoek in de query-editor op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Locatie*.</span><span class="sxs-lookup"><span data-stu-id="eba45-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="eba45-350">Stel het veld **Criteria** voor deze rij in op *Laaddeur*.</span><span class="sxs-lookup"><span data-stu-id="eba45-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="eba45-351">Selecteer **OK** om de instellingen op te slaan en de query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eba45-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="eba45-352">Werksjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="eba45-352">Set up work templates</span></span>

1. <span data-ttu-id="eba45-353">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="eba45-354">Wijzig de waarde van het veld **Werkordertype** in *Orderverzameling van gesorteerde voorraad*.</span><span class="sxs-lookup"><span data-stu-id="eba45-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="eba45-355">Selecteer in het actievenster **Nieuw** om een werksjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="eba45-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="eba45-356">Stel op het tabblad **Overzicht** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="eba45-357">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eba45-358">**Werksjabloon:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="eba45-359">**Omschrijving werksjabloon:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="eba45-360">Selecteer **Opslaan** om het sneltabblad **Werksjabloongegevens** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="eba45-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="eba45-361">Selecteer **Nieuw** op het sneltabblad **Details van werksjabloon** om een regel toe te voegen en stel de volgende waarden voor de regel in:</span><span class="sxs-lookup"><span data-stu-id="eba45-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="eba45-362">**Werktype:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="eba45-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="eba45-363">**Werkklasse-id:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="eba45-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="eba45-364">Selecteer nogmaals **Nieuw** om een tweede regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="eba45-365">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="eba45-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="eba45-366">**Werkklasse-id:** *SORTEREN*</span><span class="sxs-lookup"><span data-stu-id="eba45-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="eba45-367">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="eba45-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="eba45-368">Scenario's</span><span class="sxs-lookup"><span data-stu-id="eba45-368">Scenario</span></span>

<span data-ttu-id="eba45-369">Dit scenario simuleert een situatie waarin verpakte containers automatisch worden gesorteerd op verschillende posities (pallets) na het inpakstation, afhankelijk van de vervoerdersservice.</span><span class="sxs-lookup"><span data-stu-id="eba45-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="eba45-370">Nadat alle artikelen van de lading zijn verpakt en op adres zijn gesorteerd, worden de pallets verplaatst naar de laaddeur.</span><span class="sxs-lookup"><span data-stu-id="eba45-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="eba45-371">Verkooporders en werk voor orderverzamelen maken</span><span class="sxs-lookup"><span data-stu-id="eba45-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="eba45-372">Verkooporder 1 maken</span><span class="sxs-lookup"><span data-stu-id="eba45-372">Create sales order 1</span></span>

1. <span data-ttu-id="eba45-373">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="eba45-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eba45-374">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-375">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eba45-376">**Klantrekening:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="eba45-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="eba45-377">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="eba45-378">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eba45-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="eba45-379">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="eba45-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="eba45-380">Schakel over naar de weergave **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="eba45-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="eba45-381">Stel op het sneltabblad **Levering** in de sectie **Transport** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="eba45-382">**Vervoerder:** *Air Cargo*</span><span class="sxs-lookup"><span data-stu-id="eba45-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="eba45-383">**Vervoerdersservice:** *Air*</span><span class="sxs-lookup"><span data-stu-id="eba45-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="eba45-384">Ga naar de weergave **Regels**.</span><span class="sxs-lookup"><span data-stu-id="eba45-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="eba45-385">Als een nieuwe, lege regel niet automatisch wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels** selecteert u de optie **Regel toevoegen** om een regel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="eba45-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="eba45-386">Stel de volgende waarden in voor de nieuwe orderregel:</span><span class="sxs-lookup"><span data-stu-id="eba45-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="eba45-387">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eba45-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="eba45-388">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="eba45-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="eba45-389">Terwijl de nieuwe orderregel nog steeds is geselecteerd op het sneltabblad **Verkooporderregels**, selecteert u **Reservering** in het menu **Voorraad** boven het raster.</span><span class="sxs-lookup"><span data-stu-id="eba45-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eba45-390">Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="eba45-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eba45-391">Sluit de pagina **Reservering** om terug te keren naar de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="eba45-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eba45-392">Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="eba45-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="eba45-393">U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="eba45-394">Noteer de nummers van de wave-id en de zending-id.</span><span class="sxs-lookup"><span data-stu-id="eba45-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="eba45-395">Verkooporder 2</span><span class="sxs-lookup"><span data-stu-id="eba45-395">Sales order 2</span></span>

1. <span data-ttu-id="eba45-396">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="eba45-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eba45-397">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eba45-398">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eba45-399">**Klantrekening:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="eba45-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="eba45-400">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="eba45-401">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eba45-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="eba45-402">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="eba45-402">The new sales order is opened.</span></span> <span data-ttu-id="eba45-403">Deze moet een nieuwe, lege regel bevatten in het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="eba45-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="eba45-404">Stel de volgende waarden in op deze orderregel:</span><span class="sxs-lookup"><span data-stu-id="eba45-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="eba45-405">**Artikel:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eba45-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="eba45-406">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="eba45-407">Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Leveringsmethode** in op *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="eba45-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="eba45-408">Selecteer **Regel toevoegen** op het sneltabblad **Regels verkooporder** en stel de volgende waarden in op de tweede orderregel:</span><span class="sxs-lookup"><span data-stu-id="eba45-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="eba45-409">**Artikel:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="eba45-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="eba45-410">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="eba45-411">Wijzig op het sneltabblad **Regeldetails** op het tabblad **Levering** de waarde van het veld **Leveringsmethode** in *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="eba45-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="eba45-412">Selecteer de eerste orderregel op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="eba45-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="eba45-413">Selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="eba45-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eba45-414">Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="eba45-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eba45-415">Sluit de pagina **Reservering** om terug te keren naar de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="eba45-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eba45-416">Selecteer de tweede orderregel op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="eba45-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="eba45-417">Selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="eba45-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eba45-418">Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="eba45-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eba45-419">Sluit de pagina **Reservering** om terug te keren naar de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="eba45-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eba45-420">Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="eba45-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="eba45-421">U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="eba45-422">Er zijn twee wave-id-nummers en twee verzend-id-nummers gemaakt, één voor elke leveringsmethode voor de verkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="eba45-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="eba45-423">De werk-id's ophalen uit de werkdetails</span><span class="sxs-lookup"><span data-stu-id="eba45-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="eba45-424">Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="eba45-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="eba45-425">Op de pagina worden de werk-id's weergegeven die zijn gemaakt op basis van verkooporders.</span><span class="sxs-lookup"><span data-stu-id="eba45-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="eba45-426">Gebruik de wave-id's en verzend-id's van de verkooporders die u hebt gemaakt om de werk-id voor elke wave en zending te vinden.</span><span class="sxs-lookup"><span data-stu-id="eba45-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="eba45-427">Noteer deze werk-id's omdat u ze in de volgende stappen nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="eba45-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="eba45-428">U ziet dat er twee werk-id's zijn gemaakt voor de tweede verkooporder.</span><span class="sxs-lookup"><span data-stu-id="eba45-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="eba45-429">Als er verschillende artikelen worden verzameld vanuit verschillende locaties, worden afzonderlijke werk-id's gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="eba45-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="eba45-430">Artikelen voor de verkooporders verzamelen</span><span class="sxs-lookup"><span data-stu-id="eba45-430">Pick items for the sales orders</span></span>

<span data-ttu-id="eba45-431">Voltooi het gemaakte werk door met het mobiele apparaat de artikelen naar het inpakstation te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="eba45-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="eba45-432">Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).</span><span class="sxs-lookup"><span data-stu-id="eba45-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eba45-433">Selecteer **Uitgaand** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="eba45-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eba45-434">Selecteer **Orderverzamelen** in het menu **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="eba45-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="eba45-435">Voer in het veld **Id** de werk-id in die voor verkooporder 1 is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eba45-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="eba45-436">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-436">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-437">Voer op de pagina **Verkooporders - verzamelen** een doel-LP in die is gemaakt voor verkooporder 1.</span><span class="sxs-lookup"><span data-stu-id="eba45-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="eba45-438">U ziet dat de orderverzamellocatie (*bulk-001*), artikel (*A0001*) en hoeveelheid (*2 stuks*) worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="eba45-439">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-439">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-440">Bekijk de informatie op de pagina **Verkooporders: wegzetten**.</span><span class="sxs-lookup"><span data-stu-id="eba45-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="eba45-441">Het veld **Loc** moet aangeven dat de verzamelde artikelen naar de *Inpak*locatie gaan.</span><span class="sxs-lookup"><span data-stu-id="eba45-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="eba45-442">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-442">Select **OK**.</span></span>

    <span data-ttu-id="eba45-443">Op de pagina **Een werk-id/nummerplaat-id scannen** ziet u het bericht "Werk voltooid", wat aangeeft dat de werk-id van verkooporder 1 is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eba45-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="eba45-444">U gaat nu verkooporder 2 verzamelen.</span><span class="sxs-lookup"><span data-stu-id="eba45-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="eba45-445">Voer in het veld **Id** de werk-id in die voor verkooporder 2 is gemaakt, waarin regel 1 artikel *A0001* bevat.</span><span class="sxs-lookup"><span data-stu-id="eba45-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="eba45-446">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-446">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-447">Voer op de pagina **Verkooporders - verzamelen** een doel-LP in.</span><span class="sxs-lookup"><span data-stu-id="eba45-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="eba45-448">U ziet dat de orderverzamellocatie (*bulk-001*), artikel (*A0001*) en hoeveelheid (*1 stuks*) worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="eba45-449">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-449">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-450">Bekijk de informatie op de pagina **Verkooporders: wegzetten**.</span><span class="sxs-lookup"><span data-stu-id="eba45-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="eba45-451">Het veld **Loc** moet aangeven dat de verzamelde artikelen naar de *Inpak*locatie gaan.</span><span class="sxs-lookup"><span data-stu-id="eba45-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="eba45-452">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-452">Select **OK**.</span></span>

    <span data-ttu-id="eba45-453">Op de pagina **Een werk-id/nummerplaat-id scannen** ontvangt u het bericht "Werk voltooid".</span><span class="sxs-lookup"><span data-stu-id="eba45-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="eba45-454">Dit bericht geeft aan dat de werk-id van regel 1 van verkooporder 2 is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eba45-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="eba45-455">Voer in het veld **Id** de werk-id in die voor verkooporder 2 is gemaakt, waarin regel 2 artikel *A0002* bevat.</span><span class="sxs-lookup"><span data-stu-id="eba45-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="eba45-456">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-456">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-457">Voer op de pagina **Verkooporders - verzamelen** een doel-LP in.</span><span class="sxs-lookup"><span data-stu-id="eba45-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="eba45-458">U ziet dat de orderverzamellocatie (*bulk-002*), artikel (*A0001*) en hoeveelheid (*1 stuks*) worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="eba45-459">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-459">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-460">Bekijk de informatie op de pagina **Verkooporders: wegzetten**.</span><span class="sxs-lookup"><span data-stu-id="eba45-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="eba45-461">Het veld **Loc** moet aangeven dat de verzamelde artikelen naar de *Inpak*locatie gaan.</span><span class="sxs-lookup"><span data-stu-id="eba45-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="eba45-462">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-462">Select **OK**.</span></span>

    <span data-ttu-id="eba45-463">Op de pagina **Een werk-id/nummerplaat-id scannen** ontvangt u het bericht "Werk voltooid".</span><span class="sxs-lookup"><span data-stu-id="eba45-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="eba45-464">Dit bericht geeft aan dat de werk-id van regel 2 van verkooporder 2 is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eba45-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="eba45-465">Verkooporders in containers inpakken</span><span class="sxs-lookup"><span data-stu-id="eba45-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="eba45-466">Verkooporder 1 in containers inpakken</span><span class="sxs-lookup"><span data-stu-id="eba45-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="eba45-467">Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Verpakken**.</span><span class="sxs-lookup"><span data-stu-id="eba45-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="eba45-468">Het dialoogvenster **Inpakstation selecteren** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="eba45-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="eba45-469">Het veld **Medewerker** moet standaard zijn ingesteld op de naam van de medewerker die u eerder hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="eba45-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="eba45-470">Stel de volgende waarden in voor het weergeven en bewerken van zendingen en containers die zijn gepland op de specifieke inpaklocatie:</span><span class="sxs-lookup"><span data-stu-id="eba45-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="eba45-471">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="eba45-471">**Site:** *6*</span></span>
    - <span data-ttu-id="eba45-472">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="eba45-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eba45-473">**Locatie:** *Verpakken*</span><span class="sxs-lookup"><span data-stu-id="eba45-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="eba45-474">**Verpakkingsprofiel-id:** *Sorteren*</span><span class="sxs-lookup"><span data-stu-id="eba45-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="eba45-475">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="eba45-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="eba45-476">Voer op de pagina **Verpakken** in het veld **Nummerplaat of zending** de doel-LP in voor verkooporder 1.</span><span class="sxs-lookup"><span data-stu-id="eba45-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="eba45-477">Selecteer vervolgens de toets **Tab** of **ENTER** op het toetsenbord om het veld te verlaten.</span><span class="sxs-lookup"><span data-stu-id="eba45-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="eba45-478">Selecteer **Nieuwe container** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eba45-479">Accepteer alle standaardinstellingen en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="eba45-480">Noteer de container-id.</span><span class="sxs-lookup"><span data-stu-id="eba45-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="eba45-481">Stel op het sneltabblad **Artikel verpakken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-482">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eba45-483">**Id:** artikel *A0001*</span><span class="sxs-lookup"><span data-stu-id="eba45-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="eba45-484">Selecteer **Container sluiten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eba45-485">Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om het veld **Brutogewicht** bij te werken.</span><span class="sxs-lookup"><span data-stu-id="eba45-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="eba45-486">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-486">Select **OK**.</span></span> <span data-ttu-id="eba45-487">De container wordt verplaatst naar de locatie *SORTEREN* en kan worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="eba45-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="eba45-488">Maak een tweede container om het tweede artikel uit de nummerplaat voor verkooporder 1 toe te voegen aan een nieuwe container.</span><span class="sxs-lookup"><span data-stu-id="eba45-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="eba45-489">Selecteer **Nieuwe container** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eba45-490">Accepteer alle standaardinstellingen en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="eba45-491">Noteer de container-id.</span><span class="sxs-lookup"><span data-stu-id="eba45-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="eba45-492">Stel op het sneltabblad **Artikel verpakken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-493">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eba45-494">**Id:** artikel *A0001*</span><span class="sxs-lookup"><span data-stu-id="eba45-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="eba45-495">Selecteer **Container sluiten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eba45-496">Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om het veld **Brutogewicht** bij te werken.</span><span class="sxs-lookup"><span data-stu-id="eba45-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="eba45-497">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-497">Select **OK**.</span></span> <span data-ttu-id="eba45-498">De container wordt verplaatst naar de locatie *SORTEREN* en kan worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="eba45-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="eba45-499">Verkooporder 2 in containers inpakken</span><span class="sxs-lookup"><span data-stu-id="eba45-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="eba45-500">Voer op de pagina **Verpakken** in het veld **Nummerplaat of zending** de doel-LP in voor regel 1 van verkooporder 2.</span><span class="sxs-lookup"><span data-stu-id="eba45-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="eba45-501">Selecteer vervolgens de toets **Tab** of **ENTER** op het toetsenbord om het veld te verlaten.</span><span class="sxs-lookup"><span data-stu-id="eba45-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="eba45-502">Selecteer **Nieuwe container** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eba45-503">Accepteer alle standaardinstellingen en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="eba45-504">Noteer de container-id.</span><span class="sxs-lookup"><span data-stu-id="eba45-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="eba45-505">Stel op het sneltabblad **Artikel verpakken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-506">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eba45-507">**Id:** artikel *A0001*</span><span class="sxs-lookup"><span data-stu-id="eba45-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="eba45-508">Selecteer **Container sluiten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eba45-509">Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om het veld **Brutogewicht** bij te werken.</span><span class="sxs-lookup"><span data-stu-id="eba45-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="eba45-510">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-510">Select **OK**.</span></span> <span data-ttu-id="eba45-511">De container wordt verplaatst naar de locatie *SORTEREN* en kan worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="eba45-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="eba45-512">Voer in het veld **Nummerplaat of zending** de doel-LP in voor regel 2 van de verkooporder 2.</span><span class="sxs-lookup"><span data-stu-id="eba45-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="eba45-513">Selecteer vervolgens de toets **Tab** of **ENTER** op het toetsenbord om het veld te verlaten.</span><span class="sxs-lookup"><span data-stu-id="eba45-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="eba45-514">Selecteer **Nieuwe container** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eba45-515">Accepteer alle standaardinstellingen en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="eba45-516">Noteer de container-id.</span><span class="sxs-lookup"><span data-stu-id="eba45-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="eba45-517">Stel op het sneltabblad **Artikel verpakken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="eba45-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eba45-518">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="eba45-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eba45-519">**Id-veld:** artikel *A0002*</span><span class="sxs-lookup"><span data-stu-id="eba45-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="eba45-520">Selecteer **Container sluiten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eba45-521">Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om het veld **Brutogewicht** bij te werken.</span><span class="sxs-lookup"><span data-stu-id="eba45-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="eba45-522">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-522">Select **OK**.</span></span> <span data-ttu-id="eba45-523">De container wordt verplaatst naar de locatie *SORTEREN* en kan worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="eba45-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="eba45-524">Als u de containerdetails wilt weergeven, gaat u naar **Magazijnbeheer \> Verpakking en containervorming \> Containers** en zoekt u naar de container-id's die tijdens de verpakking zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eba45-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="eba45-525">De containers sorteren</span><span class="sxs-lookup"><span data-stu-id="eba45-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eba45-526">Wanneer u de menuopdracht **Pallet opbouwen** opent in de mobiele app om uitgaande sortering uit te voeren, ziet u een knop met het opschrift **Vol**.</span><span class="sxs-lookup"><span data-stu-id="eba45-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="eba45-527">*Gebruik de knop **Vol** niet om de positie te sorteren of te sluiten.*</span><span class="sxs-lookup"><span data-stu-id="eba45-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="eba45-528">De knop **Vol** is standaard aanwezig en kan niet worden uitgeschakeld of verwijderd van de pagina.</span><span class="sxs-lookup"><span data-stu-id="eba45-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="eba45-529">Deze wordt niet gebruikt voor de functie *Uitgaande sortering*.</span><span class="sxs-lookup"><span data-stu-id="eba45-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="eba45-530">Eerste container sorteren</span><span class="sxs-lookup"><span data-stu-id="eba45-530">Sort the first container</span></span>

1. <span data-ttu-id="eba45-531">Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).</span><span class="sxs-lookup"><span data-stu-id="eba45-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eba45-532">Selecteer **Uitgaand** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="eba45-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eba45-533">Selecteer **Orderverzamelen** in het menu **Pallet opbouwen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="eba45-534">Voer in het veld **LP/con** de eerste container-id in die aan verkooporder 1 is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eba45-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="eba45-535">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-535">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-536">Omdat er nog geen sorteerposities bestaan, moet u deze opgeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="eba45-537">Voer in het veld **Sorteerpositie-id** de tekst *SP01* in.</span><span class="sxs-lookup"><span data-stu-id="eba45-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="eba45-538">Omdat er geen LP is gekoppeld aan sorteerpositie *SP01*, moet u deze opgeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="eba45-539">Voer in het veld **LP** de waarde *PLP01* in.</span><span class="sxs-lookup"><span data-stu-id="eba45-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="eba45-540">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-540">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-541">Aangezien de validatie van de sorteerpositie is ingeschakeld, moet u de sorteerpositie-id opnieuw invoeren.</span><span class="sxs-lookup"><span data-stu-id="eba45-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="eba45-542">Voer in het veld **Sorteerpositie-id** de tekst *SP01* in.</span><span class="sxs-lookup"><span data-stu-id="eba45-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="eba45-543">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-543">Select **OK**.</span></span>

    <span data-ttu-id="eba45-544">U ziet de melding "Werk voltooid".</span><span class="sxs-lookup"><span data-stu-id="eba45-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="eba45-545">Als u de sorteerpositie en de LP erin wilt weergeven, gaat u naar **Magazijnbeheer \> Verpakking en containervorming \> Toewijzingen uitgaande sorteerpositie**.</span><span class="sxs-lookup"><span data-stu-id="eba45-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="eba45-546">Op de pagina **Toewijzingen uitgaande sorteerpositie** worden alle sorteerposities weergegeven die momenteel actief zijn.</span><span class="sxs-lookup"><span data-stu-id="eba45-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="eba45-547">In het veld **Positietransacties sorteren** wordt de LP weergegeven die is gekoppeld aan elke sorteerpositie en de containers in de sorteerpositie.</span><span class="sxs-lookup"><span data-stu-id="eba45-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="eba45-548">U ziet dat er op dit moment één sorteerpositie bestaat en dat in het sneltabblad **Criteria voor sorteerpositie** een criterium wordt weergegeven voor **Zending - vervoerdersservice - Air**.</span><span class="sxs-lookup"><span data-stu-id="eba45-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="eba45-549">De resterende containers sorteren</span><span class="sxs-lookup"><span data-stu-id="eba45-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="eba45-550">Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).</span><span class="sxs-lookup"><span data-stu-id="eba45-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eba45-551">Selecteer **Uitgaand** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="eba45-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eba45-552">Selecteer **Orderverzamelen** in het menu **Pallet opbouwen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="eba45-553">Voer in het veld **LP/con** de tweede container-id in die aan verkooporder 1 is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eba45-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="eba45-554">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-554">Select **OK**.</span></span> <span data-ttu-id="eba45-555">Omdat de sorteersjabloon zo is ingesteld dat deze automatisch wordt gesorteerd en er al een sorteerpositie met overeenkomstige criteria bestaat, wordt u automatisch doorverwezen naar de juiste sorteerpositie.</span><span class="sxs-lookup"><span data-stu-id="eba45-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="eba45-556">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-556">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-557">Bevestig de sorteerpositie-id om aan te geven dat de voorraad zich op de juiste plaats bevindt.</span><span class="sxs-lookup"><span data-stu-id="eba45-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="eba45-558">Voer in het veld **Sorteerpositie-id** de tekst *SP01* in.</span><span class="sxs-lookup"><span data-stu-id="eba45-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="eba45-559">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-559">Select **OK**.</span></span>

    <span data-ttu-id="eba45-560">Het werk voor de tweede container wordt uitgevoerd vanuit verkooporder 1.</span><span class="sxs-lookup"><span data-stu-id="eba45-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="eba45-561">U gaat nu de overige containers van verkooporder 2 sorteren.</span><span class="sxs-lookup"><span data-stu-id="eba45-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="eba45-562">Voer in het veld **LP/Con** de container-id in van de container van verkooporder 2 die artikel *A0001* bevat.</span><span class="sxs-lookup"><span data-stu-id="eba45-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="eba45-563">Aangezien de vervoerdersservice verschilt, wordt u gevraagd een nieuwe sorteerpositie in te voeren en een LP aan die positie toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="eba45-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="eba45-564">Gebruik de sorteerpositie *SP02* en LP *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="eba45-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="eba45-565">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-565">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-566">Bevestig de sorteerpositie door *SP02* in te voeren in het veld **Sorteerpositie-id**.</span><span class="sxs-lookup"><span data-stu-id="eba45-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="eba45-567">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-567">Select **OK**.</span></span>

    <span data-ttu-id="eba45-568">Het werk voor de container is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eba45-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="eba45-569">Voer in het veld **LP/Con** de container-id in voor de resterende container van verkooporder 2 die artikel *A0002* bevat.</span><span class="sxs-lookup"><span data-stu-id="eba45-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="eba45-570">Aangezien de vervoerdersservice dezelfde is als de vervoerder voor verkooporder 1, wordt in het systeem de bestaande sorteerpositie weergegeven met de overeenkomstige criteria.</span><span class="sxs-lookup"><span data-stu-id="eba45-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="eba45-571">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-571">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-572">Bevestig de sorteerpositie door *SP01* in te voeren in het veld **Sorteerpositie-id**.</span><span class="sxs-lookup"><span data-stu-id="eba45-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="eba45-573">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-573">Select **OK**.</span></span>

    <span data-ttu-id="eba45-574">Het werk voor de container is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eba45-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="eba45-575">De uitgaande sorteerposities sluiten</span><span class="sxs-lookup"><span data-stu-id="eba45-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="eba45-576">Wanneer alle voorraad is gesorteerd, moet de positie worden gesloten voordat het werk kan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eba45-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="eba45-577">Werk voor de gesorteerde voorraadverzameling wordt gemaakt om de voorraad naar de laaddeur te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="eba45-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="eba45-578">Een positie vanaf het mobiele apparaat sluiten</span><span class="sxs-lookup"><span data-stu-id="eba45-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="eba45-579">Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).</span><span class="sxs-lookup"><span data-stu-id="eba45-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eba45-580">Selecteer **Uitgaand** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="eba45-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eba45-581">Selecteer **Orderverzamelen** in het menu **Pallet opbouwen**.</span><span class="sxs-lookup"><span data-stu-id="eba45-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="eba45-582">Voer in het veld **LP/Con** een container-id in die is gesorteerd om positie *SP01* te sorteren.</span><span class="sxs-lookup"><span data-stu-id="eba45-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="eba45-583">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-583">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-584">Het volgende bericht wordt weergegeven: "De container is al gesorteerd om SP01 te positioneren.</span><span class="sxs-lookup"><span data-stu-id="eba45-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="eba45-585">De positie sluiten?"</span><span class="sxs-lookup"><span data-stu-id="eba45-585">Close the position?"</span></span> <span data-ttu-id="eba45-586">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="eba45-586">Select **Close**.</span></span>

    <span data-ttu-id="eba45-587">Werk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eba45-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="eba45-588">Een positie sluiten vanuit toewijzingen voor een uitgaande sorteerpositie</span><span class="sxs-lookup"><span data-stu-id="eba45-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="eba45-589">Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Toewijzingen uitgaande sorteerpositie**.</span><span class="sxs-lookup"><span data-stu-id="eba45-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="eba45-590">Selecteer **SP02** in de linkerkolom.</span><span class="sxs-lookup"><span data-stu-id="eba45-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="eba45-591">Deze rij met de uitgaande sorteerpositie is de rij die u gaat sluiten.</span><span class="sxs-lookup"><span data-stu-id="eba45-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="eba45-592">Selecteer **Positie sluiten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="eba45-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="eba45-593">De sorteerpositierecord wordt gesloten en wordt niet meer weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eba45-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="eba45-594">Als u alle gesloten positierecords wilt weergeven, schakelt u het selectievakje **Gesloten weergeven** in.</span><span class="sxs-lookup"><span data-stu-id="eba45-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="eba45-595">Gesorteerde orderverzameling voorraad</span><span class="sxs-lookup"><span data-stu-id="eba45-595">Sorted inventory picking</span></span>

<span data-ttu-id="eba45-596">U moet het werk voor de gesorteerde voorraadverzameling voltooien.</span><span class="sxs-lookup"><span data-stu-id="eba45-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="eba45-597">Wanneer dit is voltooid, wordt de voorraad verzameld voor de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="eba45-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="eba45-598">Op dat moment zijn alle andere magazijnprocessen van toepassing.</span><span class="sxs-lookup"><span data-stu-id="eba45-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="eba45-599">Meld u op het mobiele apparaat aan bij magazijn *62* met de gebruikers-id die u hebt gemaakt voor dit scenario (of de gebruikers-id van een bestaande gebruiker van demogegevens).</span><span class="sxs-lookup"><span data-stu-id="eba45-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eba45-600">Selecteer **Uitgaand** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="eba45-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eba45-601">Selecteer in het menu **Uitgaand** de optie **Laden uit sortering**.</span><span class="sxs-lookup"><span data-stu-id="eba45-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="eba45-602">Voer de id van het doel-LP in voor de eerste sorteerpositie *SP01*.</span><span class="sxs-lookup"><span data-stu-id="eba45-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="eba45-603">Stel het veld **Id** in op *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="eba45-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="eba45-604">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-604">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-605">De pagina **Orderverzameling van gesorteerde voorraad: orderverzamelen** toont het werk dat moet worden uitgevoerd voor het orderverzamelen.</span><span class="sxs-lookup"><span data-stu-id="eba45-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="eba45-606">Kies uit de locatie *SORTEREN* en de doel-LP *PLP01*, die meerdere artikelen en een hoeveelheid van *3* heeft.</span><span class="sxs-lookup"><span data-stu-id="eba45-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="eba45-607">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-607">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-608">De pagina **Orderverzameling van gesorteerde voorraad: wegzetten** toont het werk dat moet worden uitgevoerd voor het wegzetten.</span><span class="sxs-lookup"><span data-stu-id="eba45-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="eba45-609">Zet weg naar de locatie *Laaddeur* en de doel-LP *PLP01*, die meerdere artikelen en een hoeveelheid van *3* heeft.</span><span class="sxs-lookup"><span data-stu-id="eba45-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="eba45-610">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-610">Select **OK**.</span></span>

    <span data-ttu-id="eba45-611">Werk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eba45-611">Work is completed.</span></span>

1. <span data-ttu-id="eba45-612">Voer de id van het doelnummerplaat in voor de tweede sorteerpositie *SP02*.</span><span class="sxs-lookup"><span data-stu-id="eba45-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="eba45-613">Stel het veld **Id** in op *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="eba45-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="eba45-614">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-614">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-615">De pagina **Orderverzameling van gesorteerde voorraad: orderverzamelen** toont het werk dat moet worden uitgevoerd voor het orderverzamelen.</span><span class="sxs-lookup"><span data-stu-id="eba45-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="eba45-616">Kies uit de locatie *SORTEREN* en de doel-LP *PLP02*, die meerdere artikelen en een hoeveelheid van *1* heeft.</span><span class="sxs-lookup"><span data-stu-id="eba45-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="eba45-617">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-617">Select **OK**.</span></span>
1. <span data-ttu-id="eba45-618">De pagina **Orderverzameling van gesorteerde voorraad: wegzetten** toont het werk dat moet worden uitgevoerd voor het wegzetten.</span><span class="sxs-lookup"><span data-stu-id="eba45-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="eba45-619">Zet weg naar de locatie *Laaddeur* en de doel-LP *PLP02*, die meerdere artikelen en een hoeveelheid van *1* heeft.</span><span class="sxs-lookup"><span data-stu-id="eba45-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="eba45-620">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba45-620">Select **OK**.</span></span>

    <span data-ttu-id="eba45-621">Werk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eba45-621">Work is completed.</span></span>

<span data-ttu-id="eba45-622">Vanaf dit punt zijn alle andere magazijnprocessen van toepassing.</span><span class="sxs-lookup"><span data-stu-id="eba45-622">From this point forward, all other warehouse processes apply.</span></span>
