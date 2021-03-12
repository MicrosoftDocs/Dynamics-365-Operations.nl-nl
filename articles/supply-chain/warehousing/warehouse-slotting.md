---
title: Magazijnvakken
description: Dit onderwerp biedt informatie over magazijnvakken. Met magazijnvakken kunt u de vraag consolideren op basis van artikel en maateenheid vanuit orders met de status Besteld, Gereserveerd of Vrijgegeven. Hiermee kunnen magazijnbeheerders orderverzamellocaties intelligent plannen voordat orders naar het magazijn worden vrijgegeven en het orderverzamelwerk wordt gemaakt.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993748"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="ef2a0-105">Magazijnvakken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef2a0-106">Met de diverse functies voor magazijnvakken kunnen magazijnbeheerders orderverzamellocaties intelligent plannen voordat orders naar het magazijn worden vrijgegeven en het orderverzamelwerk wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="ef2a0-107">Met *Functie voor magazijnvakken* kunt u de vraag consolideren op basis van artikel en maateenheid vanuit orders met de status *Besteld*, *Gereserveerd* of *Vrijgegeven*.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="ef2a0-108">Gegenereerde vraag kan vervolgens worden toegepast op locaties die worden gebruikt voor orderverzamelen, op basis van hoeveelheid, eenheid, fysieke afmetinge, vaste locaties en meer.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="ef2a0-109">Nadat het vakkenplan is ingesteld, kunt u aanvullingswerk maken om de gewenste voorraadhoeveelheid naar alle locaties te brengen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="ef2a0-110">Met de functie *Magazijnvakken voor transferorders* kunnen magazijnbeheerders de orderverzamellocaties aanvullen op basis van de vraag vanuit transferorders die nog niet zijn vrijgegeven aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="ef2a0-111">Hiermee zorgt u ervoor dat verzamellocaties alle artikelen bevatten die nodig zijn voor de transferorders nadat ze zijn vrijgegeven aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="ef2a0-112">Voor deze functie moet u ook de functie *Functie voor magazijnvakken* inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="ef2a0-113">Met de functie *Uitbreidingen voor vakkentoewijzing in magazijn* voegt u een optie toe voor de sjabloonregels die worden gebruikt door de functie *Functie voor magazijnvakken*.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="ef2a0-114">Met deze optie kan het systeem rekening houden met de bestaande voorhanden voorraad op een doellocatie.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="ef2a0-115">Het is dus mogelijk dat er minder aanvullingen worden gegenereerd voor magazijnvakken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="ef2a0-116">Voor de functie *Uitbreidingen voor vakkentoewijzing in magazijn* moet u ook de functie *Functie voor magazijnvakken* inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="ef2a0-117">Deze kan optioneel worden gebruikt in combinatie met de functie *Magazijnvakken voor transferorders*.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="ef2a0-118">De functies voor magazijnvakken inschakelen</span><span class="sxs-lookup"><span data-stu-id="ef2a0-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="ef2a0-119">Voordat u deze functies kunt gebruiken, moeten deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="ef2a0-120">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functies te controleren en deze zo nodig in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="ef2a0-121">Schakel zo nodig de volgende functies in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="ef2a0-122">Functie Magazijnvakken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="ef2a0-123">Magazijnvakken voor transferorders</span><span class="sxs-lookup"><span data-stu-id="ef2a0-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ef2a0-124">De functie *Functie voor magazijnvakken* moet voor deze functie zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="ef2a0-125">Uitbreidingen voor vakkentoewijzing in magazijn</span><span class="sxs-lookup"><span data-stu-id="ef2a0-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ef2a0-126">De functie *Functie voor magazijnvakken* moet voor deze functie zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="ef2a0-127">Magazijnvakken instellen</span><span class="sxs-lookup"><span data-stu-id="ef2a0-127">Set up warehouse slotting</span></span>

<span data-ttu-id="ef2a0-128">Om magazijnvakken te gebruiken, moet u de volgende elementen configureren in het systeem:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="ef2a0-129">Niveaus van maateenheden voor vakken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="ef2a0-130">Instructiecodes</span><span class="sxs-lookup"><span data-stu-id="ef2a0-130">Directive codes</span></span>
- <span data-ttu-id="ef2a0-131">Vaksjablonen</span><span class="sxs-lookup"><span data-stu-id="ef2a0-131">Slotting templates</span></span>
- <span data-ttu-id="ef2a0-132">Locatie-instructies</span><span class="sxs-lookup"><span data-stu-id="ef2a0-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="ef2a0-133">Niveaus van maateenheden maken voor vakken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="ef2a0-134">Met niveaus van maateenheden kunnen meerdere maateenheden samen worden gegroepeerd ten behoeve van de vakken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="ef2a0-135">Als bijvoorbeeld dozen met verschillende formaten allemaal worden verzameld in hetzelfde gebied voor doosverzamelen, kunt u één niveau maken voor alle formaten.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="ef2a0-136">**U moet een regel maken voor elke maateenheid die deel moet uitmaken van het niveau.**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="ef2a0-137">Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Niveaus van maateenheden voor vakken**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="ef2a0-138">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-138">Select **New**.</span></span>
1. <span data-ttu-id="ef2a0-139">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-140">**Maateenheid niveau:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="ef2a0-141">**Beschrijving:** *Each doos pallet*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="ef2a0-142">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-142">Select **Save**.</span></span>
1. <span data-ttu-id="ef2a0-143">Ga naar het sneltabblad **Maateenheden** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ef2a0-144">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-145">**Eenheid:** *Doos*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="ef2a0-146">**Beschrijving:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="ef2a0-147">Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="ef2a0-148">**Eenheidsklasse:** *Hoeveelheid*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="ef2a0-149">Selecteer **Nieuw** om een tweede regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="ef2a0-150">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-151">**Eenheid:** *EA*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="ef2a0-152">**Beschrijving:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="ef2a0-153">Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="ef2a0-154">**Eenheidsklasse:** *Hoeveelheid*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="ef2a0-155">Selecteer **Nieuw** om een derde regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="ef2a0-156">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-157">**Eenheid:** *PL*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="ef2a0-158">**Beschrijving:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="ef2a0-159">Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="ef2a0-160">**Eenheidsklasse:** *Hoeveelheid*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="ef2a0-161">Selecteer **Opslaan** om het niveau op te slaan.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="ef2a0-162">Een instructiecode maken voor vakken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-162">Create a directive code for slotting</span></span>

<span data-ttu-id="ef2a0-163">U moet de instructiecode selecteren die aan een sjabloon moet worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="ef2a0-164">Ga naar **Magazijnbeheer \> Instellen \> Instructiecodes**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="ef2a0-165">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ef2a0-166">Voer in het veld **Instructiecode** de tekst *Vakken* in.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="ef2a0-167">Voer in het veld **Instructiebeschrijving** de tekst *Vakken* in.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="ef2a0-168">Vakkensjablonen configureren</span><span class="sxs-lookup"><span data-stu-id="ef2a0-168">Set up slotting templates</span></span>

<span data-ttu-id="ef2a0-169">Elke vakkensjabloon bepaalt hoe de voorraad wordt toegewezen aan locaties voor een bepaald magazijn.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="ef2a0-170">Elke sjabloon moet voor elke vakspecificatie een regel bevatten.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="ef2a0-171">Met de procedures in deze sectie kunt u vakkensjablonen instellen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="ef2a0-172">Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="ef2a0-173">Selecteer **Nieuw** om een sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-173">Select **New** to create a template.</span></span>

<span data-ttu-id="ef2a0-174">Vervolgens moet u de koptekst van de sjabloon, vakspecificaties en de locatie-instructies instellen, zoals in de volgende subsecties wordt uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="ef2a0-175">De instelling voor transferorders lijkt op de instelling voor magazijnvakken voor verkooporders, maar het veld **Type vraag** wordt ingesteld op *Transferorders* in plaats van op *Verkooporder*.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="ef2a0-176">De koptekst instellen voor een vakkensjabloon voor verkooporders</span><span class="sxs-lookup"><span data-stu-id="ef2a0-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="ef2a0-177">Stel in de koptekst van de sjabloon de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-178">**Vaksjabloon:** _61_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="ef2a0-179">**Beschrijving:** _61_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-179">**Description:** _61_</span></span>
    - <span data-ttu-id="ef2a0-180">**Vraagtype:** *Verkooporder*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="ef2a0-181">Momenteel zijn *Verkooporders* en *Transferorders* de enige ondersteunde vraagtypen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="ef2a0-182">U kunt *Transferorders* alleen selecteren als de functie *Magazijnvakken voor transferorders* is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="ef2a0-183">**Vraagstrategie:** _Besteld_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="ef2a0-184">De volgende waarden zijn beschikbaar in dit veld:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="ef2a0-185">**Besteld:** De volledige bestelde hoeveelheid op de verkooporder moet als vraag worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="ef2a0-186">**Gereserveerd:** Alleen de verkooporderregelhoeveelheden die zijn gereserveerd (fysiek en besteld) moeten als vraag worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="ef2a0-187">**Vrijgegeven**: de vrijgegeven hoeveelheid moet als vraag worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="ef2a0-188">**Magazijn:** _61_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="ef2a0-189">**Gebruik van niet-gereserveerde hoeveelheid door waveaanvraag toestaan:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="ef2a0-190">U kunt ook een query opgeven om het bereik te beperken van de vraag die wordt beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="ef2a0-191">Vakspecificaties instellen voor elke sjabloon</span><span class="sxs-lookup"><span data-stu-id="ef2a0-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="ef2a0-192">Voer voor elke verkooporder die u maakt de volgende stappen uit om een regel voor elke vakspecificatie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="ef2a0-193">Ga naar het sneltabblad **Vaksjabloondetails** en selecteer **Nieuw** om een sjabloonregel te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="ef2a0-194">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-195">**Reeks:** _1_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="ef2a0-196">**Beschrijving:** _Vaste locatie_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="ef2a0-197">**Minimumhoeveelheid:** _1_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="ef2a0-198">Dit veld bepaalt de minimumhoeveelheid van vraag die nodig is voor de regel.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="ef2a0-199">**Maximumhoeveelheid:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="ef2a0-200">Dit veld bepaalt de maximumhoeveelheid van vraag die geldig is voor de regel.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="ef2a0-201">**Eenheid:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="ef2a0-202">Dit veld bepaalt de maateenheid waarnaar de minimum- en maximumhoeveelheden verwijzen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="ef2a0-203">**Maateenheid niveau:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="ef2a0-204">Dit veld bepaalt de maateenheden van vraag die geldig zijn voor de regel.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="ef2a0-205">(Voor meer informatie, zie de sectie [Niveaus van maateenheden maken voor vakken](#unit-tiers) eerder in dit onderwerp.)</span><span class="sxs-lookup"><span data-stu-id="ef2a0-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="ef2a0-206">**Criteria voor vaktoewijzing:** _Hoeveelheid overwegen_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="ef2a0-207">De volgende waarden zijn beschikbaar in dit veld:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="ef2a0-208">**Uitgaan van leeg:** Er moet vanuit worden gegaan dat alle locaties in het orderverzamelgebied leeg zijn en dat deze locaties niet moeten worden gecontroleerd op voorraad.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="ef2a0-209">**Hoeveelheid overwegen:** De lcoaties in het orderverzamelgebied moete worden gecontroleerd op voorraad en alle locaties die niet leeg zijn, moeten worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="ef2a0-210">**Voorhanden voorraad in aanmerking nemen**: het systeem controleert of een doellocatie niet-gereserveerde hoeveelheden bevat voor het artikel op de vraagregel.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="ef2a0-211">Als de hoeveelheid groot genoeg is om te voldoen aan ten minste één eenheid van de vraagregel, wordt de gegenereerde vakkenplanrecord verlaagd met de beschikbare hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="ef2a0-212">Als de vraag bijvoorbeeld 10 kisten is en er één kist voorhanden is, wordt de gevonden vraag negen kisten.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="ef2a0-213">Als de vraag bijvoorbeeld 10 kisten is en elke kist voorhanden is, wordt de gevonden vraag 10 kisten.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="ef2a0-214">Deze waarde is alleen beschikbaar wanneer de functie *Uitbreidingen voor vakkentoewijzing in magazijn* is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="ef2a0-215">**Instructiecode:** _Vakken_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="ef2a0-216">In dit veld wordt de locatie-instructie gedefinieerd die wordt gebruikt om de orderverzamellocatie van het aanvullingswerk te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="ef2a0-217">**Overlooplocatie:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="ef2a0-218">In dit veld wordt de locatie gedefinieerd waar de voorraad wordt geplaatst als geen locatie voor de hoeveelheid wordt gevonden wanneer de regel wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="ef2a0-219">**Afname toestaan:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="ef2a0-220">Als deze optie is ingesteld op *Ja* en er vraag is die niet in vakken kan worden geplaatst, wordt mutatiewerk gemaakt om de voorraad weg te nemen van locaties waar er voorraad is, maar waar niets in vakken is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="ef2a0-221">De sjabloon wordt vervolgens opnieuw uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-221">The template is then run again.</span></span> <span data-ttu-id="ef2a0-222">Deze keer word de voorraad op de locaties genegeerd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="ef2a0-223">Deze functionaliteit werkt het beste wanneer het veld **Criteria voor vaktoewijzing** is ingesteld op _Hoeveelheid overwegen_.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="ef2a0-224">**Gebruik vaste locaties:** _Alleen vaste locaties voor het product_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="ef2a0-225">De volgende waarden zijn beschikbaar in dit veld:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="ef2a0-226">**Vaste en niet-vaste locaties:** Het systeem mag niet worden beperkt tot het gebruik van vaste locaties.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="ef2a0-227">**Alleen vaste locaties voor het product:** Het systeem moet alleen vakken toewijzen voor locaties die vaste locaties zijn voor het product.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="ef2a0-228">**Alleen vaste locaties voor de productvarian:** Het systeem moet alleen vakken toewijzen voor locaties die vaste locaties zijn voor de productvariant.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="ef2a0-229">Als de vakkensjabloon ten minste één regel bevat waar het veld **Criteria voor vaktoewijzing** is ingesteld op *Voorhanden voorraad in aanmerking nemen*, zijn afnames niet langer toegestaan voor alle regels in de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="ef2a0-230">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-230">Select **Save**.</span></span>
1. <span data-ttu-id="ef2a0-231">Selecteer **Nieuw** om een tweede sjabloonregel te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="ef2a0-232">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-233">**Reeks:** _2_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="ef2a0-234">**Beschrijving:** _Overige_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="ef2a0-235">**Minimale hoeveelheid:** _1_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="ef2a0-236">**Maximale hoeveelheid:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="ef2a0-237">**Eenheid:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="ef2a0-238">**Maateenheid niveau:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="ef2a0-239">**Criteria voor vaktoewijzing:** _Hoeveelheid overwegen_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="ef2a0-240">**Instructiecode:** _Vakken_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="ef2a0-241">**Overlooplocatie:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="ef2a0-242">**Afname toestaan:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="ef2a0-243">**Vaste locaties gebruiken:** _Vaste en niet-vaste locaties_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="ef2a0-244">In de query voor de tweede regel geeft u nu de criteria op waarmee wordt bepaald naar welke locaties de vraag voor die regel kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="ef2a0-245">Selecteer de regel waarin het veld **Volgnummer** is ingesteld op *2*.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="ef2a0-246">Selecteer **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="ef2a0-247">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="ef2a0-248">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-249">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="ef2a0-250">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="ef2a0-251">**Veld:** *Locatieprofiel-id*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="ef2a0-252">**Criteria:** *Pick-06* (Selecteer het dubbele plusteken \[**++**\] in het veld om de lijst uit te vouwen en selecteer vervolgens *Pick-06* - *Orderverzamellocatie 6*.)</span><span class="sxs-lookup"><span data-stu-id="ef2a0-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="ef2a0-253">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="ef2a0-254">Locatie-instructies instellen</span><span class="sxs-lookup"><span data-stu-id="ef2a0-254">Set up location directives</span></span>

<span data-ttu-id="ef2a0-255">Er moet ten minste één locatie-instructie zijn ingesteld om het toewijzen van orderverzamelen te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="ef2a0-256">Met de procedures in deze sectie kunt u een nieuwe *aanvullingslocatie-instructie* instellen om orderverzamelen toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="ef2a0-257">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ef2a0-258">Selecteer in het linkerdeelvenster in het veld **Werkordertype** de waarde *Aanvulling*.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="ef2a0-259">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ef2a0-260">Voer in de koptekst van de nieuw locatie-instructie in het veld **Naam** de tekst *61 Slotting pick* in.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="ef2a0-261">Accepteer de standaardwaarde in het veld **Volgnummer**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="ef2a0-262">Het sneltabblad Locatie-instructies configureren</span><span class="sxs-lookup"><span data-stu-id="ef2a0-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="ef2a0-263">Stel op het sneltabblad **Locatie-instructies** de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="ef2a0-264">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="ef2a0-265">**Werktype:** _Orderverzamelen_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="ef2a0-266">**Locatie:** _6_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-266">**Site:** _6_</span></span>
    - <span data-ttu-id="ef2a0-267">**Magazijn:** _61_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="ef2a0-268">**Instructiecode:** _Vakken_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="ef2a0-269">Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="ef2a0-270">Het sneltabblad Regels configureren</span><span class="sxs-lookup"><span data-stu-id="ef2a0-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="ef2a0-271">Selecteer op het sneltabblad **Regels** de optie **Nieuw** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="ef2a0-272">Stel op de nieuwe regel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="ef2a0-273">**Vanaf hoeveelheid:** _0_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="ef2a0-274">**Tot hoeveelheid:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="ef2a0-275">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="ef2a0-276">Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="ef2a0-277">Het sneltabblad Locatie-instructieacties configureren</span><span class="sxs-lookup"><span data-stu-id="ef2a0-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="ef2a0-278">Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="ef2a0-279">Stel op de nieuwe regel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-279">On the new line, set the following values.</span></span> <span data-ttu-id="ef2a0-280">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="ef2a0-281">**Volgnummer:** Accepteer de standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="ef2a0-282">**Naam:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="ef2a0-283">**Strategie:** _Geen_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="ef2a0-284">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="ef2a0-285">Selecteer **Opslaan** om de knop **Query bewerken** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="ef2a0-286">De query bewerken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-286">Edit the query</span></span>

1. <span data-ttu-id="ef2a0-287">Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="ef2a0-288">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="ef2a0-289">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-290">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="ef2a0-291">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="ef2a0-292">**Veld:** *Zone-id*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="ef2a0-293">**Criteria:** *Bulk* (Selecteer het dubbele plusteken \[**++**\] in het veld om de lijst uit te vouwen en selecteer vervolgens *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="ef2a0-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="ef2a0-294">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="ef2a0-295">Scenario's</span><span class="sxs-lookup"><span data-stu-id="ef2a0-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="ef2a0-296">Het scenario configureren</span><span class="sxs-lookup"><span data-stu-id="ef2a0-296">Set up the scenario</span></span>

<span data-ttu-id="ef2a0-297">Gebruik voor dit scenario de ingebouwde voorbeeldgegevens en maak de records die in deze sectie worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="ef2a0-298">De voorbeeldgegevens voor USMF gebruiken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-298">Use the USMF sample data</span></span>

<span data-ttu-id="ef2a0-299">Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="ef2a0-300">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="ef2a0-301">Vraag maken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-301">Create demand</span></span>

<span data-ttu-id="ef2a0-302">Voer de volgende stappen uit om de vraag te maken waarop u het toewijzen van vakken gaat toepassen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="ef2a0-303">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="ef2a0-304">Selecteer **Nieuw** om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="ef2a0-305">Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde _US-007_.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="ef2a0-306">Selecteer **61** in het veld _Magazijn_.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="ef2a0-307">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-307">Select **OK**.</span></span>
1. <span data-ttu-id="ef2a0-308">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-308">The new sales order is opened.</span></span> <span data-ttu-id="ef2a0-309">Deze bevat een lege rij in het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ef2a0-310">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-311">**Artikel:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="ef2a0-312">**Hoeveelheid:** _20_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="ef2a0-313">Selecteer **Regel toevoegen** om een nieuwe regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="ef2a0-314">**Artikel:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="ef2a0-315">**Hoeveelheid:** _8_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="ef2a0-316">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-316">Select **Save**.</span></span>
1. <span data-ttu-id="ef2a0-317">Selecteer **Nieuw** om een tweede verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="ef2a0-318">Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde _US-008_.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="ef2a0-319">Selecteer **61** in het veld _Magazijn_.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="ef2a0-320">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-320">The new sales order is opened.</span></span> <span data-ttu-id="ef2a0-321">Deze bevat een lege rij in het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ef2a0-322">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="ef2a0-323">**Artikel:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="ef2a0-324">**Hoeveelheid:** _1_</span><span class="sxs-lookup"><span data-stu-id="ef2a0-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="ef2a0-325">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="ef2a0-326">Een veelvoorkomend scenario voor vaktoewijzing doorlopen</span><span class="sxs-lookup"><span data-stu-id="ef2a0-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="ef2a0-327">Nadat alle vereiste elementen zijn geïmplementeerd zoals beschreven in het vorige gedeelte, kunt u de functie uitproberen door alle oefening in deze sectie te doorlopen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="ef2a0-328">Vraag genereren</span><span class="sxs-lookup"><span data-stu-id="ef2a0-328">Generate demand</span></span>

1. <span data-ttu-id="ef2a0-329">Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Vakkensjablonen** en selecteer de vakkensjabloon die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="ef2a0-330">Selecteer **Vraag genereren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="ef2a0-331">Met deze opdracht evalueert u alle vraag in het systeem die voldoet aan de criteria in de query op de vakkensjabloon.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="ef2a0-332">De totale vraag voor alle orders wordt vervolgens geconsolideerd in één regel per hoeveelheid/eenheid.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="ef2a0-333">Er wordt een informatief bericht weergegeven wanneer het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="ef2a0-334">Vraag per vak</span><span class="sxs-lookup"><span data-stu-id="ef2a0-334">Slotting demand</span></span>

<span data-ttu-id="ef2a0-335">De *vakkenvraag* geeft de resultaten weer van het genereren van de vraag op basis van de instellingen van de vakkensjabloon.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="ef2a0-336">Selecteer in het actievenster **Vakkenvraag** om de resultaten weer te geven van de opdracht **Vraag genereren**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="ef2a0-337">De regels in de vakkenvraag kunnen worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="ef2a0-338">U kunt een regel verwijderen, een nieuwe regel toevoegen of de regeldetails bewerken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="ef2a0-339">U kunt de vraag handmatig bewerken of u kunt deze vanuit een extern systeem importeren met gegevensbeheer.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="ef2a0-340">Wat er in de vakvraag staat, wordt in de volgende stap gebruikt, ongeacht waar de vraag vandaan komt.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="ef2a0-341">Vraag zoeken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-341">Locate demand</span></span>

<span data-ttu-id="ef2a0-342">Nadat de vraag is gegenereerd, moet u de opdracht **Vraag zoeken** gebruiken om het *vakkenplan* te genereren.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="ef2a0-343">Selecteer **Vraag zoeken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="ef2a0-344">Het vakkenproces wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-344">The slotting process runs.</span></span> <span data-ttu-id="ef2a0-345">Er wordt een informatief bericht weergegeven wanneer het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="ef2a0-346">Plan voor vakken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-346">Slotting plan</span></span>

<span data-ttu-id="ef2a0-347">Het vakkenplan toont de locatie waaraan elk artikel/elke hoeveelheid is toegewezen, of de overschrijding is gebruikt, of afnamewerk is gemaakt, en de sjabloonregel die werd gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="ef2a0-348">*Elke vraag die niet aan vakken kan worden toegewezen, is rood gemarkeerd.*</span><span class="sxs-lookup"><span data-stu-id="ef2a0-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="ef2a0-349">Selecteer in het actievenster de optie **Vakkenplan** om de resultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="ef2a0-350">De processen **Vraag genereren**, **Vraag zoeken** en **Aanvulling uitvoeren** worden nu in een sandbox uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="ef2a0-351">(Deze processen zijn beschikbaar vanuit het actievenster op de pagina **Vakkensjablonen**.)</span><span class="sxs-lookup"><span data-stu-id="ef2a0-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="ef2a0-352">De processen **Vraag genereren**, **Vraag zoeken** en **Aanvulling uitvoeren** hebben een vergrendeling om ervoor te zorgen dat deze niet tegelijkertijd kunnen worden geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="ef2a0-353">Anders kunnen de gegevens die worden gebruikt, worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="ef2a0-354">De processen **Vraag genereren** en **Vraag zoeken** geven een waarschuwing weer als de uitvoering geen records heeft gegenereerd of als er gegevens ontbreken in de records.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="ef2a0-355">Wanneer u **Vakkenplan** selecteert, bevat de pagina geen knoppen **Nieuw**, **Bewerken** of **Verwijderen** in het actievenster, omdat de gegevensbron niet kan worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="ef2a0-356">Wanneer u **Aanvulling uitvoeren** selecteert, valideert het systeem de geselecteerde vakkensjabloon en -processen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="ef2a0-357">Aanvulling maken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-357">Create replenishment</span></span>

<span data-ttu-id="ef2a0-358">Nadat het vakkenplan is gemaakt, moet u *aanvullingswerk maken* op basis van het plan.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="ef2a0-359">Selecteer **Aanvulling uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="ef2a0-360">Er wordt een informatief bericht weergegeven wanneer het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="ef2a0-361">Dit bericht geeft het aantal kopteksten aan dat is gemaakt voor de werkbuild-id.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="ef2a0-362">De locatie-instructies die worden gebruikt, worden geïdentificeerd op basis van de instructiecode die op elke sjabloonregel is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="ef2a0-363">Tips</span><span class="sxs-lookup"><span data-stu-id="ef2a0-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="ef2a0-364">Automatisch vakkentoewijzing configureren</span><span class="sxs-lookup"><span data-stu-id="ef2a0-364">Set up automatic slotting</span></span>

<span data-ttu-id="ef2a0-365">Nadat alle vereiste elementen zijn ingesteld, kunt u vaktoewijzing configureren om automatisch te worden uitgevoerd. U doet dit met de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="ef2a0-366">Ga naar **Magazijnbeheer \> Aanvulling \> Vakken uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="ef2a0-367">Geef op welke vakkenstappen moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="ef2a0-368">Selecteer een of meer van de volgende vakkenstappen:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="ef2a0-369">Vraag genereren</span><span class="sxs-lookup"><span data-stu-id="ef2a0-369">Generate demand</span></span>
    - <span data-ttu-id="ef2a0-370">Vraag zoeken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-370">Locate demand</span></span>
    - <span data-ttu-id="ef2a0-371">Aanvullingswerk maken</span><span class="sxs-lookup"><span data-stu-id="ef2a0-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef2a0-372">De vakkenstappen zijn progressief.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-372">The slotting steps are progressive.</span></span> <span data-ttu-id="ef2a0-373">Als u de optie *Vraag zoeken* wilt selecteren , moet u eerst de optie *Vraag genereren* selecteren.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="ef2a0-374">Geef op welke vakkensjabloon u wilt laten gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="ef2a0-375">Stel het herhalingspatroon desgewenst in op automatisch herhalen.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="ef2a0-376">Stel voor de oefeningen in het scenario **niet** automatische vaktoewijzing in.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
