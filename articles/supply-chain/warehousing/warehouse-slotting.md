---
title: Magazijnvakken
description: Dit onderwerp biedt informatie over magazijnvakken. Met magazijnvakken kunt u de vraag consolideren op basis van artikel en maateenheid vanuit orders met de status Besteld, Gereserveerd of Vrijgegeven. Hiermee kunnen magazijnbeheerders orderverzamellocaties intelligent plannen voordat orders naar het magazijn worden vrijgegeven en het orderverzamelwerk wordt gemaakt.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017409"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="1782e-105">Magazijnvakken</span><span class="sxs-lookup"><span data-stu-id="1782e-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1782e-106">Met magazijnvakken kunt u de vraag consolideren op basis van artikel en maateenheid vanuit orders met de status *Besteld* , *Gereserveerd* of *Vrijgegeven*.</span><span class="sxs-lookup"><span data-stu-id="1782e-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="1782e-107">Gegenereerde vraag kan vervolgens worden toegepast op locaties die worden gebruikt voor orderverzamelen, op basis van hoeveelheid, eenheid, fysieke afmetinge, vaste locaties en meer.</span><span class="sxs-lookup"><span data-stu-id="1782e-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="1782e-108">Nadat het vakkenplan is ingesteld, kunt u aanvullingswerk maken om de gewenste voorraadhoeveelheid naar alle locaties te brengen.</span><span class="sxs-lookup"><span data-stu-id="1782e-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="1782e-109">Met deze functionaliteit kunnen magazijnbeheerders orderverzamellocaties intelligent plannen voordat orders naar het magazijn worden vrijgegeven en het orderverzamelwerk wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1782e-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="1782e-110">De functie Magazijnvakken inschakelen</span><span class="sxs-lookup"><span data-stu-id="1782e-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="1782e-111">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="1782e-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1782e-112">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="1782e-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1782e-113">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="1782e-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1782e-114">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="1782e-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1782e-115">**Functienaam:** *Magazijnvakken*</span><span class="sxs-lookup"><span data-stu-id="1782e-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="1782e-116">Magazijnvakken instellen</span><span class="sxs-lookup"><span data-stu-id="1782e-116">Set up warehouse slotting</span></span>

<span data-ttu-id="1782e-117">Om de functie Magazijnvakken te gebruiken, moet u de volgende elementen configureren in het systeem:</span><span class="sxs-lookup"><span data-stu-id="1782e-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="1782e-118">Niveaus van maateenheden maken voor vakken</span><span class="sxs-lookup"><span data-stu-id="1782e-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="1782e-119">Met niveaus van maateenheden kunnen meerdere maateenheden samen worden gegroepeerd ten behoeve van de vakken.</span><span class="sxs-lookup"><span data-stu-id="1782e-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="1782e-120">Als bijvoorbeeld dozen met verschillende formaten allemaal worden verzameld in hetzelfde gebied voor doosverzamelen, kunt u één niveau maken voor alle formaten.</span><span class="sxs-lookup"><span data-stu-id="1782e-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="1782e-121">**U moet een regel maken voor elke maateenheid die deel moet uitmaken van het niveau.**</span><span class="sxs-lookup"><span data-stu-id="1782e-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="1782e-122">Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Niveaus van maateenheden voor vakken**.</span><span class="sxs-lookup"><span data-stu-id="1782e-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="1782e-123">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="1782e-123">Select **New**.</span></span>
1. <span data-ttu-id="1782e-124">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="1782e-125">**Maateenheid niveau:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="1782e-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="1782e-126">**Beschrijving:** *Each doos pallet*</span><span class="sxs-lookup"><span data-stu-id="1782e-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="1782e-127">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1782e-127">Select **Save**.</span></span>
1. <span data-ttu-id="1782e-128">Ga naar het sneltabblad **Maateenheden** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="1782e-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1782e-129">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1782e-130">**Eenheid:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="1782e-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="1782e-131">**Beschrijving:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="1782e-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="1782e-132">Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.</span><span class="sxs-lookup"><span data-stu-id="1782e-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="1782e-133">**Eenheidsklasse:** *Hoeveelheid*</span><span class="sxs-lookup"><span data-stu-id="1782e-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="1782e-134">Selecteer **Nieuw** om een tweede regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="1782e-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="1782e-135">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1782e-136">**Eenheid:** *EA*</span><span class="sxs-lookup"><span data-stu-id="1782e-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="1782e-137">**Beschrijving:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="1782e-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="1782e-138">Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.</span><span class="sxs-lookup"><span data-stu-id="1782e-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="1782e-139">**Eenheidsklasse:** *Hoeveelheid*</span><span class="sxs-lookup"><span data-stu-id="1782e-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="1782e-140">Selecteer **Nieuw** om een derde regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="1782e-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="1782e-141">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1782e-142">**Eenheid:** *PL*</span><span class="sxs-lookup"><span data-stu-id="1782e-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="1782e-143">**Beschrijving:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="1782e-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="1782e-144">Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.</span><span class="sxs-lookup"><span data-stu-id="1782e-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="1782e-145">**Eenheidsklasse:** *Hoeveelheid*</span><span class="sxs-lookup"><span data-stu-id="1782e-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="1782e-146">Selecteer **Opslaan** om het niveau op te slaan.</span><span class="sxs-lookup"><span data-stu-id="1782e-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="1782e-147">Een instructiecode maken voor vakken</span><span class="sxs-lookup"><span data-stu-id="1782e-147">Create a directive code for slotting</span></span>

<span data-ttu-id="1782e-148">U moet de instructiecode selecteren die aan een sjabloon moet worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="1782e-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="1782e-149">Ga naar **Magazijnbeheer \> Instellen \> Instructiecodes**.</span><span class="sxs-lookup"><span data-stu-id="1782e-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="1782e-150">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="1782e-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1782e-151">Voer in het veld **Instructiecode** de tekst *Vakken* in.</span><span class="sxs-lookup"><span data-stu-id="1782e-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="1782e-152">Voer in het veld **Instructiebeschrijving** de tekst *Vakken* in.</span><span class="sxs-lookup"><span data-stu-id="1782e-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="1782e-153">Vakkensjablonen configureren</span><span class="sxs-lookup"><span data-stu-id="1782e-153">Set up slotting templates</span></span>

<span data-ttu-id="1782e-154">Elke vakkensjabloon bepaalt hoe de voorraad wordt toegewezen aan locaties voor een bepaald magazijn.</span><span class="sxs-lookup"><span data-stu-id="1782e-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="1782e-155">Elke sjabloon moet voor elke vakspecificatie een regel bevatten.</span><span class="sxs-lookup"><span data-stu-id="1782e-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="1782e-156">Met de procedures in deze sectie kunt u vakkensjablonen instellen.</span><span class="sxs-lookup"><span data-stu-id="1782e-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="1782e-157">Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen**.</span><span class="sxs-lookup"><span data-stu-id="1782e-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="1782e-158">Selecteer **Nieuw** om een sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-158">Select **New** to create a template.</span></span>

<span data-ttu-id="1782e-159">Vervolgens moet u de koptekst van de sjabloon, vakspecificaties en de locatie-instructies instellen, zoals in de volgende subsecties wordt uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="1782e-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="1782e-160">Een koptekst voor een vakkensjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="1782e-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="1782e-161">Stel in de koptekst van de sjabloon de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="1782e-162">**Vaksjabloon:** _61_</span><span class="sxs-lookup"><span data-stu-id="1782e-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="1782e-163">**Beschrijving:** _61_</span><span class="sxs-lookup"><span data-stu-id="1782e-163">**Description:** _61_</span></span>
    - <span data-ttu-id="1782e-164">**Vraagtype:** *Verkooporder*</span><span class="sxs-lookup"><span data-stu-id="1782e-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="1782e-165">Momenteel is *Verkooporder* het enige vraagtype dat wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="1782e-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="1782e-166">**Vraagstrategie:** _Besteld_</span><span class="sxs-lookup"><span data-stu-id="1782e-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="1782e-167">De volgende waarden zijn beschikbaar in dit veld:</span><span class="sxs-lookup"><span data-stu-id="1782e-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="1782e-168">**Besteld:** De volledige bestelde hoeveelheid op de verkooporder moet als vraag worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="1782e-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="1782e-169">**Gereserveerd:** Alleen de verkooporderregelhoeveelheden die zijn gereserveerd (fysiek en besteld) moeten als vraag worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="1782e-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="1782e-170">**Magazijn:** _61_</span><span class="sxs-lookup"><span data-stu-id="1782e-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="1782e-171">**Gebruik van niet-gereserveerde hoeveelheid door waveaanvraag toestaan:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="1782e-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="1782e-172">U kunt ook een query opgeven om het bereik te beperken van de vraag die wordt beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="1782e-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="1782e-173">Vakspecificaties instellen voor elke sjabloon</span><span class="sxs-lookup"><span data-stu-id="1782e-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="1782e-174">Voer voor elke sjabloon die u maakt de volgende stappen uit om een regel voor elke vakspecificatie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="1782e-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="1782e-175">Ga naar het sneltabblad **Vaksjabloondetails** en selecteer **Nieuw** om een sjabloonregel te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="1782e-176">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1782e-177">**Reeks:** _1_</span><span class="sxs-lookup"><span data-stu-id="1782e-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="1782e-178">**Beschrijving:** _Vaste locatie_</span><span class="sxs-lookup"><span data-stu-id="1782e-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="1782e-179">**Minimumhoeveelheid:** _1_</span><span class="sxs-lookup"><span data-stu-id="1782e-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="1782e-180">Dit veld bepaalt de minimumhoeveelheid van vraag die nodig is voor de regel.</span><span class="sxs-lookup"><span data-stu-id="1782e-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="1782e-181">**Maximumhoeveelheid:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="1782e-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="1782e-182">Dit veld bepaalt de maximumhoeveelheid van vraag die geldig is voor de regel.</span><span class="sxs-lookup"><span data-stu-id="1782e-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="1782e-183">**Eenheid:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="1782e-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="1782e-184">Dit veld bepaalt de maateenheid waarnaar de minimum- en maximumhoeveelheden verwijzen.</span><span class="sxs-lookup"><span data-stu-id="1782e-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="1782e-185">**Maateenheid niveau:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="1782e-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="1782e-186">Dit veld bepaalt de maateenheden van vraag die geldig zijn voor de regel.</span><span class="sxs-lookup"><span data-stu-id="1782e-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="1782e-187">(Voor meer informatie, zie de sectie [Niveaus van maateenheden maken voor vakken](#unit-tiers) eerder in dit onderwerp.)</span><span class="sxs-lookup"><span data-stu-id="1782e-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="1782e-188">**Criteria voor vaktoewijzing:** _Hoeveelheid overwegen_</span><span class="sxs-lookup"><span data-stu-id="1782e-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="1782e-189">De volgende waarden zijn beschikbaar in dit veld:</span><span class="sxs-lookup"><span data-stu-id="1782e-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="1782e-190">**Uitgaan van leeg:** Er moet vanuit worden gegaan dat alle locaties in het orderverzamelgebied leeg zijn en dat deze locaties niet moeten worden gecontroleerd op voorraad.</span><span class="sxs-lookup"><span data-stu-id="1782e-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="1782e-191">**Hoeveelheid overwegen:** De lcoaties in het orderverzamelgebied moete worden gecontroleerd op voorraad en alle locaties die niet leeg zijn, moeten worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="1782e-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="1782e-192">**Instructiecode:** _Vakken_</span><span class="sxs-lookup"><span data-stu-id="1782e-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="1782e-193">In dit veld wordt de locatie-instructie gedefinieerd die wordt gebruikt om de orderverzamellocatie van het aanvullingswerk te zoeken.</span><span class="sxs-lookup"><span data-stu-id="1782e-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="1782e-194">**Overlooplocatie:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="1782e-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="1782e-195">In dit veld wordt de locatie gedefinieerd waar de voorraad wordt geplaatst als geen locatie voor de hoeveelheid wordt gevonden wanneer de regel wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="1782e-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="1782e-196">**Afname toestaan:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="1782e-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="1782e-197">Als deze optie is ingesteld op *Ja* en er vraag is die niet in vakken kan worden geplaatst, wordt mutatiewerk gemaakt om de voorraad weg te nemen van locaties waar er voorraad is, maar waar niets in vakken is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="1782e-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="1782e-198">De sjabloon wordt vervolgens opnieuw uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1782e-198">The template is then run again.</span></span> <span data-ttu-id="1782e-199">Deze keer word de voorraad op de locaties genegeerd.</span><span class="sxs-lookup"><span data-stu-id="1782e-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="1782e-200">Deze functionaliteit werkt het beste wanneer het veld **Criteria voor vaktoewijzing** is ingesteld op _Hoeveelheid overwegen_.</span><span class="sxs-lookup"><span data-stu-id="1782e-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="1782e-201">**Gebruik vaste locaties:** _Alleen vaste locaties voor het product_</span><span class="sxs-lookup"><span data-stu-id="1782e-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="1782e-202">De volgende waarden zijn beschikbaar in dit veld:</span><span class="sxs-lookup"><span data-stu-id="1782e-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="1782e-203">**Vaste en niet-vaste locaties:** Het systeem mag niet worden beperkt tot het gebruik van vaste locaties.</span><span class="sxs-lookup"><span data-stu-id="1782e-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="1782e-204">**Alleen vaste locaties voor het product:** Het systeem moet alleen vakken toewijzen voor locaties die vaste locaties zijn voor het product.</span><span class="sxs-lookup"><span data-stu-id="1782e-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="1782e-205">**Alleen vaste locaties voor de productvarian:** Het systeem moet alleen vakken toewijzen voor locaties die vaste locaties zijn voor de productvariant.</span><span class="sxs-lookup"><span data-stu-id="1782e-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="1782e-206">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1782e-206">Select **Save**.</span></span>
1. <span data-ttu-id="1782e-207">Selecteer **Nieuw** om een tweede sjabloonregel te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="1782e-208">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1782e-209">**Reeks:** _2_</span><span class="sxs-lookup"><span data-stu-id="1782e-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="1782e-210">**Beschrijving:** _Overige_</span><span class="sxs-lookup"><span data-stu-id="1782e-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="1782e-211">**Minimale hoeveelheid:** _1_</span><span class="sxs-lookup"><span data-stu-id="1782e-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="1782e-212">**Maximale hoeveelheid:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="1782e-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="1782e-213">**Eenheid:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="1782e-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="1782e-214">**Maateenheid niveau:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="1782e-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="1782e-215">**Criteria voor vaktoewijzing:** _Hoeveelheid overwegen_</span><span class="sxs-lookup"><span data-stu-id="1782e-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="1782e-216">**Instructiecode:** _Vakken_</span><span class="sxs-lookup"><span data-stu-id="1782e-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="1782e-217">**Overlooplocatie:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="1782e-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="1782e-218">**Afname toestaan:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="1782e-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="1782e-219">**Vaste locaties gebruiken:** _Vaste en niet-vaste locaties_</span><span class="sxs-lookup"><span data-stu-id="1782e-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="1782e-220">In de query voor de tweede regel geeft u nu de criteria op waarmee wordt bepaald naar welke locaties de vraag voor die regel kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1782e-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="1782e-221">Selecteer de regel waarin het veld **Volgnummer** is ingesteld op *2*.</span><span class="sxs-lookup"><span data-stu-id="1782e-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="1782e-222">Selecteer **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="1782e-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="1782e-223">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="1782e-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="1782e-224">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1782e-225">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="1782e-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="1782e-226">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="1782e-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="1782e-227">**Veld:** *Locatieprofiel-id*</span><span class="sxs-lookup"><span data-stu-id="1782e-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="1782e-228">**Criteria:** *Pick-06* (Selecteer het dubbele plusteken \[**++**\] in het veld om de lijst uit te vouwen en selecteer vervolgens *Pick-06* - *Orderverzamellocatie 6*.)</span><span class="sxs-lookup"><span data-stu-id="1782e-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="1782e-229">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="1782e-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="1782e-230">Locatie-instructies instellen</span><span class="sxs-lookup"><span data-stu-id="1782e-230">Set up location directives</span></span>

<span data-ttu-id="1782e-231">Er moet ten minste één locatie-instructie zijn ingesteld om het toewijzen van orderverzamelen te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="1782e-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="1782e-232">Met de procedures in deze sectie kunt u een nieuwe *aanvullingslocatie-instructie* instellen om orderverzamelen toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="1782e-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="1782e-233">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="1782e-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1782e-234">Selecteer in het linkerdeelvenster in het veld **Werkordertype** de waarde *Aanvulling*.</span><span class="sxs-lookup"><span data-stu-id="1782e-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="1782e-235">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="1782e-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1782e-236">Voer in de koptekst van de nieuw locatie-instructie in het veld **Naam** de tekst *61 Slotting pick* in.</span><span class="sxs-lookup"><span data-stu-id="1782e-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="1782e-237">Het sneltabblad Locatie-instructies configureren</span><span class="sxs-lookup"><span data-stu-id="1782e-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="1782e-238">Stel op het sneltabblad **Locatie-instructies** de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="1782e-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="1782e-239">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="1782e-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="1782e-240">**Werktype:** _Orderverzamelen_</span><span class="sxs-lookup"><span data-stu-id="1782e-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="1782e-241">**Locatie:** _6_</span><span class="sxs-lookup"><span data-stu-id="1782e-241">**Site:** _6_</span></span>
    - <span data-ttu-id="1782e-242">**Magazijn:** _61_</span><span class="sxs-lookup"><span data-stu-id="1782e-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="1782e-243">**Instructiecode:** _Vakken_</span><span class="sxs-lookup"><span data-stu-id="1782e-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="1782e-244">Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="1782e-245">Het sneltabblad Regels configureren</span><span class="sxs-lookup"><span data-stu-id="1782e-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="1782e-246">Selecteer op het sneltabblad **Regels** de optie **Nieuw** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="1782e-247">Stel op de nieuwe regel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="1782e-247">On the new line, set the following values.</span></span> <span data-ttu-id="1782e-248">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="1782e-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="1782e-249">**Vanaf hoeveelheid:** _0_</span><span class="sxs-lookup"><span data-stu-id="1782e-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="1782e-250">**Tot hoeveelheid:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="1782e-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="1782e-251">Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="1782e-252">Het sneltabblad Locatie-instructieacties configureren</span><span class="sxs-lookup"><span data-stu-id="1782e-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="1782e-253">Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="1782e-254">Stel op de nieuwe regel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="1782e-254">On the new line, set the following values.</span></span> <span data-ttu-id="1782e-255">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="1782e-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="1782e-256">**Naam:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="1782e-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="1782e-257">**Strategie:** _Geen_</span><span class="sxs-lookup"><span data-stu-id="1782e-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="1782e-258">Selecteer **Opslaan** om de knop **Query bewerken** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="1782e-259">De query bewerken</span><span class="sxs-lookup"><span data-stu-id="1782e-259">Edit the query</span></span>

1. <span data-ttu-id="1782e-260">Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="1782e-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="1782e-261">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="1782e-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="1782e-262">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1782e-263">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="1782e-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="1782e-264">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="1782e-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="1782e-265">**Veld:** *Zone-id*</span><span class="sxs-lookup"><span data-stu-id="1782e-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="1782e-266">**Criteria:** *Bulk* (Selecteer het dubbele plusteken \[**++**\] in het veld om de lijst uit te vouwen en selecteer vervolgens *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="1782e-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="1782e-267">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="1782e-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="1782e-268">Scenario's</span><span class="sxs-lookup"><span data-stu-id="1782e-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="1782e-269">Het scenario configureren</span><span class="sxs-lookup"><span data-stu-id="1782e-269">Set up the scenario</span></span>

<span data-ttu-id="1782e-270">Gebruik voor dit scenario de ingebouwde voorbeeldgegevens en maak de records die in deze sectie worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="1782e-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="1782e-271">De voorbeeldgegevens voor USMF gebruiken</span><span class="sxs-lookup"><span data-stu-id="1782e-271">Use the USMF sample data</span></span>

<span data-ttu-id="1782e-272">Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="1782e-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="1782e-273">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="1782e-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="1782e-274">Vraag maken</span><span class="sxs-lookup"><span data-stu-id="1782e-274">Create demand</span></span>

<span data-ttu-id="1782e-275">Voer de volgende stappen uit om de vraag te maken waarop u het toewijzen van vakken gaat toepassen.</span><span class="sxs-lookup"><span data-stu-id="1782e-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="1782e-276">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="1782e-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="1782e-277">Selecteer **Nieuw** om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="1782e-278">Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde _US-007_.</span><span class="sxs-lookup"><span data-stu-id="1782e-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="1782e-279">Selecteer **61** in het veld _Magazijn_.</span><span class="sxs-lookup"><span data-stu-id="1782e-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="1782e-280">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="1782e-280">Select **OK**.</span></span>
1. <span data-ttu-id="1782e-281">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="1782e-281">The new sales order is opened.</span></span> <span data-ttu-id="1782e-282">Deze bevat een lege rij in het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="1782e-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1782e-283">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="1782e-284">**Artikel:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="1782e-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="1782e-285">**Hoeveelheid:** _20_</span><span class="sxs-lookup"><span data-stu-id="1782e-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="1782e-286">Selecteer **Regel toevoegen** om een nieuwe regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="1782e-287">**Artikel:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="1782e-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="1782e-288">**Hoeveelheid:** _8_</span><span class="sxs-lookup"><span data-stu-id="1782e-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="1782e-289">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1782e-289">Select **Save**.</span></span>
1. <span data-ttu-id="1782e-290">Selecteer **Nieuw** om een tweede verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="1782e-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="1782e-291">Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde _US-008_.</span><span class="sxs-lookup"><span data-stu-id="1782e-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="1782e-292">Selecteer **61** in het veld _Magazijn_.</span><span class="sxs-lookup"><span data-stu-id="1782e-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="1782e-293">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="1782e-293">The new sales order is opened.</span></span> <span data-ttu-id="1782e-294">Deze bevat een lege rij in het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="1782e-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1782e-295">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="1782e-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="1782e-296">**Artikel:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="1782e-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="1782e-297">**Hoeveelheid:** _1_</span><span class="sxs-lookup"><span data-stu-id="1782e-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="1782e-298">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1782e-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="1782e-299">Een veelvoorkomend scenario voor vaktoewijzing doorlopen</span><span class="sxs-lookup"><span data-stu-id="1782e-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="1782e-300">Nadat alle vereiste elementen zijn geïmplementeerd zoals beschreven in het vorige gedeelte, kunt u de functie uitproberen door alle oefening in deze sectie te doorlopen.</span><span class="sxs-lookup"><span data-stu-id="1782e-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="1782e-301">Vraag genereren</span><span class="sxs-lookup"><span data-stu-id="1782e-301">Generate demand</span></span>

1. <span data-ttu-id="1782e-302">Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Vakkensjablonen** en selecteer de vakkensjabloon die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1782e-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="1782e-303">Selecteer **Vraag genereren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="1782e-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="1782e-304">Met deze opdracht evalueert u alle vraag in het systeem die voldoet aan de criteria in de query op de vakkensjabloon.</span><span class="sxs-lookup"><span data-stu-id="1782e-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="1782e-305">De totale vraag voor alle orders wordt vervolgens geconsolideerd in één regel per hoeveelheid/eenheid.</span><span class="sxs-lookup"><span data-stu-id="1782e-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="1782e-306">Er wordt een informatief bericht weergegeven wanneer het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="1782e-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="1782e-307">Vraag per vak</span><span class="sxs-lookup"><span data-stu-id="1782e-307">Slotting demand</span></span>

<span data-ttu-id="1782e-308">De *vakkenvraag* geeft de resultaten weer van het genereren van de vraag op basis van de instellingen van de vakkensjabloon.</span><span class="sxs-lookup"><span data-stu-id="1782e-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="1782e-309">Selecteer in het actievenster **Vakkenvraag** om de resultaten weer te geven van de opdracht **Vraag genereren**.</span><span class="sxs-lookup"><span data-stu-id="1782e-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="1782e-310">De regels in de vakkenvraag kunnen worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="1782e-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="1782e-311">U kunt een regel verwijderen, een nieuwe regel toevoegen of de regeldetails bewerken.</span><span class="sxs-lookup"><span data-stu-id="1782e-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="1782e-312">U kunt de vraag handmatig bewerken of u kunt deze vanuit een extern systeem importeren met gegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="1782e-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="1782e-313">Wat er in de vakvraag staat, wordt in de volgende stap gebruikt, ongeacht waar de vraag vandaan komt.</span><span class="sxs-lookup"><span data-stu-id="1782e-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="1782e-314">Vraag zoeken</span><span class="sxs-lookup"><span data-stu-id="1782e-314">Locate demand</span></span>

<span data-ttu-id="1782e-315">Nadat de vraag is gegenereerd, moet u de opdracht **Vraag zoeken** gebruiken om het *vakkenplan* te genereren.</span><span class="sxs-lookup"><span data-stu-id="1782e-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="1782e-316">Selecteer **Vraag zoeken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="1782e-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="1782e-317">Het vakkenproces wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1782e-317">The slotting process runs.</span></span> <span data-ttu-id="1782e-318">Er wordt een informatief bericht weergegeven wanneer het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="1782e-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="1782e-319">Plan voor vakken</span><span class="sxs-lookup"><span data-stu-id="1782e-319">Slotting plan</span></span>

<span data-ttu-id="1782e-320">Het vakkenplan toont de locatie waaraan elk artikel/elke hoeveelheid is toegewezen, of de overschrijding is gebruikt, of afnamewerk is gemaakt, en de sjabloonregel die werd gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1782e-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="1782e-321">**Elke vraag die niet aan vakken kan worden toegewezen, is rood gemarkeerd.**</span><span class="sxs-lookup"><span data-stu-id="1782e-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="1782e-322">Selecteer in het actievenster de optie **Vakkenplan** om de resultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="1782e-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="1782e-323">Aanvulling maken</span><span class="sxs-lookup"><span data-stu-id="1782e-323">Create replenishment</span></span>

<span data-ttu-id="1782e-324">Nadat het vakkenplan is gemaakt, moet u *aanvullingswerk maken* op basis van het plan.</span><span class="sxs-lookup"><span data-stu-id="1782e-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="1782e-325">Selecteer **Aanvulling uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="1782e-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="1782e-326">Er wordt een informatief bericht weergegeven wanneer het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="1782e-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="1782e-327">Dit bericht geeft het aantal kopteksten aan dat is gemaakt voor de werkbuild-id.</span><span class="sxs-lookup"><span data-stu-id="1782e-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="1782e-328">De locatie-instructies die worden gebruikt, worden geïdentificeerd op basis van de instructiecode die op elke sjabloonregel is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="1782e-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="1782e-329">Tips</span><span class="sxs-lookup"><span data-stu-id="1782e-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="1782e-330">Automatisch vakkentoewijzing configureren</span><span class="sxs-lookup"><span data-stu-id="1782e-330">Set up automatic slotting</span></span>

<span data-ttu-id="1782e-331">Nadat alle vereiste elementen zijn ingesteld, kunt u vaktoewijzing configureren om automatisch te worden uitgevoerd. U doet dit met de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="1782e-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="1782e-332">Ga naar **Magazijnbeheer \> Aanvulling \> Vakken uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="1782e-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="1782e-333">Geef op welke vakkenstappen moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1782e-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="1782e-334">Selecteer een of meer van de volgende vakkenstappen:</span><span class="sxs-lookup"><span data-stu-id="1782e-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="1782e-335">Vraag genereren</span><span class="sxs-lookup"><span data-stu-id="1782e-335">Generate demand</span></span>
    - <span data-ttu-id="1782e-336">Vraag zoeken</span><span class="sxs-lookup"><span data-stu-id="1782e-336">Locate demand</span></span>
    - <span data-ttu-id="1782e-337">Aanvullingswerk maken</span><span class="sxs-lookup"><span data-stu-id="1782e-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="1782e-338">De vakkenstappen zijn progressief.</span><span class="sxs-lookup"><span data-stu-id="1782e-338">The slotting steps are progressive.</span></span> <span data-ttu-id="1782e-339">Als u de optie *Vraag zoeken* wilt selecteren , moet u eerst de optie *Vraag genereren* selecteren.</span><span class="sxs-lookup"><span data-stu-id="1782e-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="1782e-340">Geef op welke vakkensjabloon u wilt laten gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1782e-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="1782e-341">Stel het herhalingspatroon desgewenst in op automatisch herhalen.</span><span class="sxs-lookup"><span data-stu-id="1782e-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="1782e-342">Stel voor de oefeningen in het scenario **niet** automatische vaktoewijzing in.</span><span class="sxs-lookup"><span data-stu-id="1782e-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
