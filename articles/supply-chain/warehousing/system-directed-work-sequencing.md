---
title: Door systeem gestuurde werksequentiëring
description: Dit onderwerp geeft informatie over door het systeem gestuurde werksequentiëring. Met deze functie kunt u de werkorders sorteren en filteren die door het systeem aan gebruikers worden gepresenteerd voor uitvoering. Het is nuttig in scenario's waarin extra criteria nodig zijn om het verzamelproces in het magazijn aan te sturen.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017019"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="73f43-105">Door systeem gestuurde werksequentiëring</span><span class="sxs-lookup"><span data-stu-id="73f43-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73f43-106">Met door het systeem gestuurde werksequeuntiëring kunt u de werkorders sorteren en filteren die door het systeem aan gebruikers worden gepresenteerd voor uitvoering.</span><span class="sxs-lookup"><span data-stu-id="73f43-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="73f43-107">Het is nuttig in scenario's waarin aanvullende criteria vereist zijn (zoals de verzendtijd, de orderverzamellocatie, het locatieprofiel of een combinatie van verschillende criteria) om het verzamelproces in het magazijn aan te sturen.</span><span class="sxs-lookup"><span data-stu-id="73f43-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="73f43-108">Deze functionaliteit breidt de huidige door het systeem gestuurde verzamelfunctionaliteit uit, door een queryvolgorde toe te voegen, waarin gebruikers een sequentie en een of meer query's kunnen instellen waarmee alle werkorders worden geëvalueerd die worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="73f43-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="73f43-109">Alleen werkorders die voldoen aan de criteria die zijn opgegeven in de instellingen van de menuopdracht op mobiele apparaten, worden vastgelegd en gepresenteerd.</span><span class="sxs-lookup"><span data-stu-id="73f43-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="73f43-110">Deze functionaliteit biedt daarom verdere optimalisatie van verzamelprocessen in het magazijn, aangezien werkorders worden geïdentificeerd die aan de opgegeven criteria voldoen, deze toewijzen aan de juiste menuopdracht op het mobiele apparaat en deze vervolgens worden weergegeven aan een werknemer op basis van een specifieke reeks kwalificaties, apparatuur voor orderverzamelen of andere vereisten.</span><span class="sxs-lookup"><span data-stu-id="73f43-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="73f43-111">Als verschillende criteria nodig zijn, moeten meerdere menuopdrachten voor mobiele apparaten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="73f43-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="73f43-112">De functie Organisatiebrede, door het systeem gestuurde werksequentiëring inschakelen</span><span class="sxs-lookup"><span data-stu-id="73f43-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="73f43-113">Voordat u door het systeem gestuurde werksequentiëring kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="73f43-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="73f43-114">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="73f43-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="73f43-115">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="73f43-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="73f43-116">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="73f43-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="73f43-117">**Functienaam** *Organisatiebrede, door het systeem gestuurde werksequentiëring*</span><span class="sxs-lookup"><span data-stu-id="73f43-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="73f43-118">Instellen</span><span class="sxs-lookup"><span data-stu-id="73f43-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="73f43-119">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="73f43-119">Make demo data available</span></span>

<span data-ttu-id="73f43-120">Om het scenario te doorlopen met de waarden die in dit onderwerp worden voorgesteld, moet u werken op een systeem waarop de standaardvoorbeeldgegevens zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="73f43-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="73f43-121">U moet daarnaast ook de rechtspersoon **USMF** selecteren.</span><span class="sxs-lookup"><span data-stu-id="73f43-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="73f43-122">In het scenario wordt magazijn *51* uit de demogegevens gebruikt.</span><span class="sxs-lookup"><span data-stu-id="73f43-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73f43-123">Voordat u de orders aan het magazijn vrijgeeft, moet u ervoor zorgen dat de orderverzamellocaties voldoende voorraad hebben voor alle artikelen op de orders.</span><span class="sxs-lookup"><span data-stu-id="73f43-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="73f43-124">Dit scenario moet worden ondersteund door standaard USMF-gegevens.</span><span class="sxs-lookup"><span data-stu-id="73f43-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="73f43-125">Als u geen gebruik maakt van de demogegevens, controleert u de instelling **Locatie-instructie** om te zien welke orderverzamellocaties worden gebruikt voor het verzamelen van verkooporders.</span><span class="sxs-lookup"><span data-stu-id="73f43-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="73f43-126">Als u de voorraad moet corrigeren, kunt u handmatige verplaatsingen maken en aanvulling of elke andere stroom gebruiken.</span><span class="sxs-lookup"><span data-stu-id="73f43-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="73f43-127">Een menuopdracht voor een mobiel apparaat instellen</span><span class="sxs-lookup"><span data-stu-id="73f43-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="73f43-128">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="73f43-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="73f43-129">Selecteer in de lijst met menuopdrachten voor mobiele apparaten de optie **Verkoopverzamelen - systeem**.</span><span class="sxs-lookup"><span data-stu-id="73f43-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="73f43-130">De vereiste menuopdracht zou al moeten bestaan.</span><span class="sxs-lookup"><span data-stu-id="73f43-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="73f43-131">Bevestig de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="73f43-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="73f43-132">Op het sneltabblad **Algemeen** moet het veld **Gestuurd door** zijn ingesteld op *Door systeem bestuurd*.</span><span class="sxs-lookup"><span data-stu-id="73f43-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="73f43-133">Op het sneltabblad **Werkklassen** moeten de volgende instellingen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="73f43-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="73f43-134">Werkklasse-id</span><span class="sxs-lookup"><span data-stu-id="73f43-134">Work class ID</span></span> | <span data-ttu-id="73f43-135">Werkordertype</span><span class="sxs-lookup"><span data-stu-id="73f43-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="73f43-136">Verkoop</span><span class="sxs-lookup"><span data-stu-id="73f43-136">Sales</span></span> | <span data-ttu-id="73f43-137">Verkooporders</span><span class="sxs-lookup"><span data-stu-id="73f43-137">Sales orders</span></span> |
        | <span data-ttu-id="73f43-138">VO verzamelen</span><span class="sxs-lookup"><span data-stu-id="73f43-138">SO Pick</span></span> | <span data-ttu-id="73f43-139">Verkooporders</span><span class="sxs-lookup"><span data-stu-id="73f43-139">Sales orders</span></span> |

1. <span data-ttu-id="73f43-140">Selecteer in het actievenster **Door het systeem gestuurde werkreeksquery's**.</span><span class="sxs-lookup"><span data-stu-id="73f43-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="73f43-141">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="73f43-141">Select **Edit**.</span></span>
1. <span data-ttu-id="73f43-142">Verwijder de bestaande regel en bevestig de actie door **Ja** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="73f43-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="73f43-143">Selecteer in het actievenster **Nieuw** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="73f43-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="73f43-144">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73f43-145">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="73f43-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="73f43-146">**Veld Beschrijving:** *Werkhoeveelheid minder dan 20 en Aflopend*</span><span class="sxs-lookup"><span data-stu-id="73f43-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="73f43-147">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="73f43-147">Select **Save**.</span></span>
1. <span data-ttu-id="73f43-148">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="73f43-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="73f43-149">Vouw op het tabblad **Joins** de join-hiërarchie uit om de tabel **Werkregels** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="73f43-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="73f43-150">Selecteer de tabeljoin **Werkregels**.</span><span class="sxs-lookup"><span data-stu-id="73f43-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="73f43-151">Selecteer **Tabeljoin toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="73f43-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="73f43-152">Zoek en selecteer in de lijst die wordt weergegeven de rij met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="73f43-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="73f43-153">**Join-modus:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="73f43-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="73f43-154">**Relatie:** *Locaties (Locatie)*</span><span class="sxs-lookup"><span data-stu-id="73f43-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="73f43-155">Selecteer **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="73f43-155">Select **Select**.</span></span>

    <span data-ttu-id="73f43-156">Locaties worden toegevoegd aan de tabel-join.</span><span class="sxs-lookup"><span data-stu-id="73f43-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="73f43-157">Selecteer op het tabblad **Sorteren** de optie **Toevoegen** om een regel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="73f43-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="73f43-158">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73f43-159">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="73f43-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="73f43-160">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="73f43-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="73f43-161">**Veld:** *Werkhoeveelheid* (in het berichtvak dat wordt weergegeven, selecteert u **Ja** om aan dit veld sorteren toe te voegen.)</span><span class="sxs-lookup"><span data-stu-id="73f43-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="73f43-162">**Zoekrichting:** *Aflopend*</span><span class="sxs-lookup"><span data-stu-id="73f43-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="73f43-163">Selecteer het tabblad **Bereik**.</span><span class="sxs-lookup"><span data-stu-id="73f43-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="73f43-164">Als in het sequentiëren alleen specifieke werkcriteria moeten worden opgenomen, kunt u deze opgeven op het tabblad **Bereik**. In dit voorbeeld wilt u alleen werk opnemen waarbij de hoeveelheid kleiner is dan 20 ea (de laagste maateenheid).</span><span class="sxs-lookup"><span data-stu-id="73f43-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="73f43-165">Merk op dat sommige regels al zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="73f43-165">Notice that some lines are already included.</span></span> <span data-ttu-id="73f43-166">U moet deze regels niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="73f43-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="73f43-167">Selecteer **Toevoegen** om een regel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="73f43-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="73f43-168">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73f43-169">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="73f43-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="73f43-170">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="73f43-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="73f43-171">**Veld:** *Werkhoeveelheid voorraad*</span><span class="sxs-lookup"><span data-stu-id="73f43-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="73f43-172">**Criteria:** *\< 20* (minder dan 20)</span><span class="sxs-lookup"><span data-stu-id="73f43-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="73f43-173">Selecteer **Toevoegen** om nog een regel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="73f43-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="73f43-174">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73f43-175">**Tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="73f43-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="73f43-176">**Afgeleide tabel:** *Werkregels*</span><span class="sxs-lookup"><span data-stu-id="73f43-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="73f43-177">**Veld:** *Werktype*</span><span class="sxs-lookup"><span data-stu-id="73f43-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="73f43-178">**Criteria:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="73f43-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="73f43-179">Selecteer **Toevoegen** om nog een regel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="73f43-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="73f43-180">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="73f43-181">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="73f43-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="73f43-182">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="73f43-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="73f43-183">**Veld:** *Locatieprofiel-id*</span><span class="sxs-lookup"><span data-stu-id="73f43-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="73f43-184">**Criteria:** *!KLAARZETTEN*</span><span class="sxs-lookup"><span data-stu-id="73f43-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="73f43-185">Vergeet niet het uitroepteken ( *!* ) in te voegen vóór *KLAARZETTEN*.</span><span class="sxs-lookup"><span data-stu-id="73f43-185">Be sure to include the exclamation point ( *!* ) in front of *STAGE*.</span></span>

1. <span data-ttu-id="73f43-186">Selecteer **OK** om de query op te slaan en te sluiten.</span><span class="sxs-lookup"><span data-stu-id="73f43-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="73f43-187">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="73f43-187">Select **Save**.</span></span>
1. <span data-ttu-id="73f43-188">Sluit de pagina om terug te gaan naar de pagina **Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="73f43-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="73f43-189">Deze instelling bepaalt welke criteria worden gebruikt om het in aanmerking komende werk door te geven aan het menu-item op het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="73f43-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="73f43-190">Als u meer criteriaregels aan de query toevoegt, wordt eerst de queryregel gebruikt die het laagste volgnummer heeft.</span><span class="sxs-lookup"><span data-stu-id="73f43-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="73f43-191">Met andere woorden, alle in aanmerking komende werk voor volgnummer 1 wordt eerst aan de gebruiker gepresenteerd en vervolgens alle werk voor volgnummer 2.</span><span class="sxs-lookup"><span data-stu-id="73f43-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="73f43-192">Als dus een specifiek bereik en specifieke sortering samen moeten worden gebruikt, moeten deze worden opgegeven in dezelfde query voor door het systeem gestuurde werksequentiëring.</span><span class="sxs-lookup"><span data-stu-id="73f43-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="73f43-193">Met deze configuratie wordt al het werk vastgelegd dat ten minste één regel bevat waarvan de hoeveelheid minder is dan 20 ea.</span><span class="sxs-lookup"><span data-stu-id="73f43-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="73f43-194">Als het werk bijvoorbeeld een regel heeft waarvan de hoeveelheid precies 20 ea of meer dan 20 ea is, is deze geldig, mits er ook minimaal één regel is met een hoeveelheid van minder dan 20 ea.</span><span class="sxs-lookup"><span data-stu-id="73f43-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="73f43-195">Locatie-instructies</span><span class="sxs-lookup"><span data-stu-id="73f43-195">Location directives</span></span>

<span data-ttu-id="73f43-196">Als u standaard Contoso-gegevens gebruikt, zijn geen wijzigingen vereist in de query voor de locatie-instructieactie.</span><span class="sxs-lookup"><span data-stu-id="73f43-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="73f43-197">Om er echter voor te zorgen dat de locatie-instructies de artikelen op de verkooporders vastleggen wanneer u de functie toepast in een omgeving buiten Contoso, maakt u een nieuwe locatie-instructie.</span><span class="sxs-lookup"><span data-stu-id="73f43-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="73f43-198">Voer de volgende stappen uit om de instellingen in de demo-omgeving te controleren.</span><span class="sxs-lookup"><span data-stu-id="73f43-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="73f43-199">Ga naar **Magazijnbeheer** \> **Instellen** \> **Locatie-instructies**.</span><span class="sxs-lookup"><span data-stu-id="73f43-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="73f43-200">Selecteer *Verkooporders* in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="73f43-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="73f43-201">Selecteer de locatie-instructie met de naam *51 Pick*.</span><span class="sxs-lookup"><span data-stu-id="73f43-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="73f43-202">Ga naar het sneltabblad **Locatie-instructieacties** en selecteer de regel voor de actie **Orderverzamelen**.</span><span class="sxs-lookup"><span data-stu-id="73f43-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="73f43-203">Selecteer boven het raster de opdracht **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="73f43-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="73f43-204">Controleer de query **Bereik**.</span><span class="sxs-lookup"><span data-stu-id="73f43-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="73f43-205">Zoek de regel waarin het veld **Veld** is ingesteld op *Locatie*.</span><span class="sxs-lookup"><span data-stu-id="73f43-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="73f43-206">Zorg ervoor dat het veld **Criteria** leeg is (dat wil zeggen dat er geen beperkingen zijn).</span><span class="sxs-lookup"><span data-stu-id="73f43-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="73f43-207">Scenario's</span><span class="sxs-lookup"><span data-stu-id="73f43-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="73f43-208">Werk voor orderverzamelen voor verkooporders maken</span><span class="sxs-lookup"><span data-stu-id="73f43-208">Create sales order picking work</span></span>

<span data-ttu-id="73f43-209">Voordat de door het systeem gestuurde orderverzameling wordt uitgevoerd, moet een deel van het uitgaande werk worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="73f43-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="73f43-210">Voor dit scenario maakt u vier verkooporders die zijn gebaseerd op de opgegeven de query's voor door het systeem gestuurde werksequentiëring.</span><span class="sxs-lookup"><span data-stu-id="73f43-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="73f43-211">U gaat voorraadhoeveelheden reserveren voor elke verkooporder.</span><span class="sxs-lookup"><span data-stu-id="73f43-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="73f43-212">Gereserveerde voorraad in het magazijn kan dus niet voor andere orders worden gebruikt, tenzij de reservering van de voorraad in zijn geheel of gedeeltelijk wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="73f43-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="73f43-213">Vervolgens geeft u elke verkooporder vrij naar het magazijn om het uitgaande werk te maken.</span><span class="sxs-lookup"><span data-stu-id="73f43-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="73f43-214">Verkooporder 1</span><span class="sxs-lookup"><span data-stu-id="73f43-214">Sales order 1</span></span>

1. <span data-ttu-id="73f43-215">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="73f43-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="73f43-216">Selecteer in het actievenster **Nieuw** om verkooporder 1 te maken.</span><span class="sxs-lookup"><span data-stu-id="73f43-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="73f43-217">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="73f43-218">Stel in de sectie **Klant** het veld **Klantaccount** in op *US-004*.</span><span class="sxs-lookup"><span data-stu-id="73f43-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="73f43-219">Stel in de sectie **Algemeen** het veld **Magazijn** in op *51*.</span><span class="sxs-lookup"><span data-stu-id="73f43-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="73f43-220">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="73f43-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="73f43-221">Noteer het nummer van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="73f43-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="73f43-222">Voeg een regel toe aan de nieuwe verkooporder en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="73f43-223">**Artikelnummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="73f43-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="73f43-224">**Hoeveelheid:** *20*</span><span class="sxs-lookup"><span data-stu-id="73f43-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="73f43-225">Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="73f43-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="73f43-226">Selecteer op de pagina **Reservering** de waarde **Partij reserveren** om de voorraad te reserveren.</span><span class="sxs-lookup"><span data-stu-id="73f43-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="73f43-227">Sluit de pagina **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="73f43-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="73f43-228">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgave naar magazijn** om werk voor het magazijn te maken.</span><span class="sxs-lookup"><span data-stu-id="73f43-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="73f43-229">U ontvangt een informatieve melding waarin de wave-id en zendings-id worden vermeld die zijn aangemaakt voor de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="73f43-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="73f43-230">Verkooporder 2</span><span class="sxs-lookup"><span data-stu-id="73f43-230">Sales order 2</span></span>

1. <span data-ttu-id="73f43-231">Selecteer in het actievenster **Nieuw** om verkooporder 2 te maken.</span><span class="sxs-lookup"><span data-stu-id="73f43-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="73f43-232">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="73f43-233">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="73f43-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="73f43-234">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="73f43-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="73f43-235">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="73f43-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="73f43-236">Noteer het nummer van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="73f43-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="73f43-237">Voeg een regel toe aan de nieuwe verkooporder en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="73f43-238">**Artikelnummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="73f43-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="73f43-239">**Hoeveelheid:** *5*</span><span class="sxs-lookup"><span data-stu-id="73f43-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="73f43-240">Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="73f43-241">**Artikelnummer:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="73f43-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="73f43-242">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="73f43-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="73f43-243">Reserveer voorraad voor beide regels.</span><span class="sxs-lookup"><span data-stu-id="73f43-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="73f43-244">Geef de order vrij naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="73f43-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="73f43-245">Verkooporder 3</span><span class="sxs-lookup"><span data-stu-id="73f43-245">Sales order 3</span></span>

1. <span data-ttu-id="73f43-246">Selecteer in het actievenster **Nieuw** om verkooporder 3 te maken.</span><span class="sxs-lookup"><span data-stu-id="73f43-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="73f43-247">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="73f43-248">**Klantrekening:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="73f43-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="73f43-249">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="73f43-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="73f43-250">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="73f43-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="73f43-251">Noteer het nummer van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="73f43-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="73f43-252">Voeg een regel toe aan de nieuwe verkooporder en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="73f43-253">**Artikelnummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="73f43-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="73f43-254">**Hoeveelheid:** *7*</span><span class="sxs-lookup"><span data-stu-id="73f43-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="73f43-255">Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="73f43-256">**Artikelnummer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="73f43-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="73f43-257">**Hoeveelheid:** *8*</span><span class="sxs-lookup"><span data-stu-id="73f43-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="73f43-258">Reserveer voorraad voor beide regels.</span><span class="sxs-lookup"><span data-stu-id="73f43-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="73f43-259">Geef de order vrij naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="73f43-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="73f43-260">Verkooporder 4</span><span class="sxs-lookup"><span data-stu-id="73f43-260">Sales order 4</span></span>

1. <span data-ttu-id="73f43-261">Selecteer in het actievenster **Nieuw** om verkooporder 4 te maken.</span><span class="sxs-lookup"><span data-stu-id="73f43-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="73f43-262">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="73f43-263">**Klantrekening:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="73f43-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="73f43-264">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="73f43-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="73f43-265">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="73f43-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="73f43-266">Noteer het nummer van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="73f43-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="73f43-267">Voeg een regel toe aan de nieuwe verkooporder en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="73f43-268">**Artikelnummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="73f43-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="73f43-269">**Hoeveelheid:** *25*</span><span class="sxs-lookup"><span data-stu-id="73f43-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="73f43-270">Selecteer **Regel toevoegen** om een tweede regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="73f43-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="73f43-271">**Artikelnummer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="73f43-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="73f43-272">**Hoeveelheid:** *10*</span><span class="sxs-lookup"><span data-stu-id="73f43-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="73f43-273">Reserveer voorraad voor beide regels.</span><span class="sxs-lookup"><span data-stu-id="73f43-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="73f43-274">Geef de order vrij naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="73f43-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="73f43-275">Werk-id's ophalen voor het gemaakte werk</span><span class="sxs-lookup"><span data-stu-id="73f43-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="73f43-276">Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="73f43-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="73f43-277">Filter op het veld **Magazijn** , zodat alleen werk voor magazijn *51* wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="73f43-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="73f43-278">Er moeten vier werk-id's zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="73f43-278">Four work IDs should have been created.</span></span> <span data-ttu-id="73f43-279">Noteer de werk-id van elke verkooporder.</span><span class="sxs-lookup"><span data-stu-id="73f43-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="73f43-280">Verkooporder-id</span><span class="sxs-lookup"><span data-stu-id="73f43-280">Sales order ID</span></span> | <span data-ttu-id="73f43-281">Werk-id</span><span class="sxs-lookup"><span data-stu-id="73f43-281">Work ID</span></span> | <span data-ttu-id="73f43-282">Werkhoeveelheid</span><span class="sxs-lookup"><span data-stu-id="73f43-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="73f43-283">Verkooporder 1</span><span class="sxs-lookup"><span data-stu-id="73f43-283">Sales Order 1</span></span> | <span data-ttu-id="73f43-284">Werk-id 1</span><span class="sxs-lookup"><span data-stu-id="73f43-284">Work ID 1</span></span> | <span data-ttu-id="73f43-285">20 ea</span><span class="sxs-lookup"><span data-stu-id="73f43-285">20 ea</span></span> |
    | <span data-ttu-id="73f43-286">Verkooporder 2</span><span class="sxs-lookup"><span data-stu-id="73f43-286">Sales Order 2</span></span> | <span data-ttu-id="73f43-287">Werk-id 2</span><span class="sxs-lookup"><span data-stu-id="73f43-287">Work ID 2</span></span> | <span data-ttu-id="73f43-288">6 ea (som van beide regels)</span><span class="sxs-lookup"><span data-stu-id="73f43-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="73f43-289">Verkooporder 3</span><span class="sxs-lookup"><span data-stu-id="73f43-289">Sales Order 3</span></span> | <span data-ttu-id="73f43-290">Werk-id 3</span><span class="sxs-lookup"><span data-stu-id="73f43-290">Work ID 3</span></span> | <span data-ttu-id="73f43-291">15 ea (som van beide regels)</span><span class="sxs-lookup"><span data-stu-id="73f43-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="73f43-292">Verkooporder 4</span><span class="sxs-lookup"><span data-stu-id="73f43-292">Sales Order 4</span></span> | <span data-ttu-id="73f43-293">Werk-id 4</span><span class="sxs-lookup"><span data-stu-id="73f43-293">Work ID 4</span></span> | <span data-ttu-id="73f43-294">35 ea (som van beide regels)</span><span class="sxs-lookup"><span data-stu-id="73f43-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="73f43-295">Voordat u de stroom uitvoert op het mobiele apparaat, moet u controleren of alleen het werk dat u zojuist hebt gemaakt de status *Open* heeft voor magazijn *51* en het werkordertype *Verkooporder* heeft.</span><span class="sxs-lookup"><span data-stu-id="73f43-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="73f43-296">Anders kunnen de resultaten van de test afwijken, omdat de door het systeem gestuurde orderverzameling alle in aanmerking komende werk bevat.</span><span class="sxs-lookup"><span data-stu-id="73f43-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="73f43-297">Ga naar **Magazijnbeheer \> Werk \> Uitgaand \> Open verkoopwerk**.</span><span class="sxs-lookup"><span data-stu-id="73f43-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="73f43-298">Filter in het raster **Open verkoopwerk** op het veld **Magazijn** , zodat alleen werk voor magazijn *51* wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="73f43-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="73f43-299">Controleer of alleen de vier werk-id's die u eerder hebt gemaakt, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="73f43-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="73f43-300">Sluit de pagina **Werk**.</span><span class="sxs-lookup"><span data-stu-id="73f43-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="73f43-301">Uitvoering van stroom op mobiele apparaten</span><span class="sxs-lookup"><span data-stu-id="73f43-301">Mobile device flow execution</span></span>

<span data-ttu-id="73f43-302">Op basis van de instellingen voert het systeem de gebruiker het werk, dat is gesorteerd van de hoogste werkregelhoeveelheid tot de laagste.</span><span class="sxs-lookup"><span data-stu-id="73f43-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="73f43-303">De hoeveelheid op elke regel is minder dan 20 ea.</span><span class="sxs-lookup"><span data-stu-id="73f43-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="73f43-304">Onthoud dat met deze configuratie al het werk wordt vastgelegd dat ten minste één regel bevat waarvan de hoeveelheid minder is dan 20 ea.</span><span class="sxs-lookup"><span data-stu-id="73f43-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="73f43-305">Als het werk een andere regel heeft waarop de hoeveelheid precies 20 ea of meer dan 20 ea ist, is die regel ook geldig.</span><span class="sxs-lookup"><span data-stu-id="73f43-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="73f43-306">Mobiele app</span><span class="sxs-lookup"><span data-stu-id="73f43-306">Mobile app</span></span>

1. <span data-ttu-id="73f43-307">Meld u aan bij de magazijnapp als een gebruiker in magazijn *51*.</span><span class="sxs-lookup"><span data-stu-id="73f43-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="73f43-308">Ga naar **Uitgaand \> Verkoopverzamelen - systeem**.</span><span class="sxs-lookup"><span data-stu-id="73f43-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="73f43-309">De verzamelstap voor werk-id *4* wordt getoond.</span><span class="sxs-lookup"><span data-stu-id="73f43-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="73f43-310">Deze werk-id wordt als eerste gepresenteerd vanwege de configuratie van de door het systeem gestuurde query-volgorde, waarin u hebt opgegeven dat het werk aflopend moet worden geordend op basis van de hoeveelheid op de werkregel.</span><span class="sxs-lookup"><span data-stu-id="73f43-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="73f43-311">Voltooi het vereiste verzamelen en wegzetten om de werk-id te sluiten.</span><span class="sxs-lookup"><span data-stu-id="73f43-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="73f43-312">Vervolgens wordt werk-id *3* getoond.</span><span class="sxs-lookup"><span data-stu-id="73f43-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="73f43-313">Een van de werkregels daarvan staat nu in de volgorde, op basis van de hoeveelheid op de werkregel.</span><span class="sxs-lookup"><span data-stu-id="73f43-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="73f43-314">Voltooi het verzamelen en wegzetten om de werk-id te sluiten.</span><span class="sxs-lookup"><span data-stu-id="73f43-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="73f43-315">Vervolgens wordt werk-id *2* getoond.</span><span class="sxs-lookup"><span data-stu-id="73f43-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="73f43-316">De verzamelregel van deze werkregel is de volgende in de volgorde.</span><span class="sxs-lookup"><span data-stu-id="73f43-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="73f43-317">Voltooi het verzamelen en wegzetten om de werk-id te sluiten.</span><span class="sxs-lookup"><span data-stu-id="73f43-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="73f43-318">Daarna zou niet meer werk moeten worden getoond.</span><span class="sxs-lookup"><span data-stu-id="73f43-318">No further work should be presented to you.</span></span> <span data-ttu-id="73f43-319">Werk-id *1* komt niet in aanmerking voor dit menu-item op het mobiele apparaat, omdat de query opgeeft dat de werkkopteksten alleen worden meegenomen als de hoeveelheid op de werkregel minder is dan 20 ea.</span><span class="sxs-lookup"><span data-stu-id="73f43-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="73f43-320">Tips</span><span class="sxs-lookup"><span data-stu-id="73f43-320">Tips</span></span>

<span data-ttu-id="73f43-321">De door het systeem gestuurde query's voor werkvolgorde zijn *inclusief*.</span><span class="sxs-lookup"><span data-stu-id="73f43-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="73f43-322">Het is belangrijk dat u dit voor sommige situaties onthoudt.</span><span class="sxs-lookup"><span data-stu-id="73f43-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="73f43-323">U wilt bijvoorbeeld dat een bepaalde menuopdracht alleen werkt met de werk eenheid *ea* en u geeft deze beperking op op het tabblad **Bereik** van de query.</span><span class="sxs-lookup"><span data-stu-id="73f43-323">For example, you want a specific menu item to process only work where the work unit is *ea* , and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="73f43-324">In dit geval wordt al het werk waarin minstens voor één werkregel de werkeenheid is ingesteld op *ea* naar de werknemer geleid.</span><span class="sxs-lookup"><span data-stu-id="73f43-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="73f43-325">Daarom kan dit werk ook werk bevatte waarbij werkregels een andere werk eenheid dan *ea* hebben (zoals *doos* of *pallet* ).</span><span class="sxs-lookup"><span data-stu-id="73f43-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet* ).</span></span> <span data-ttu-id="73f43-326">In de query wordt alleen het werk uitgesloten waarbij op geen enkele regel de werkeenheid is ingesteld op *ea*.</span><span class="sxs-lookup"><span data-stu-id="73f43-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="73f43-327">Daarom werd in het voorbeeld uit dit scenario ook werk-id *4* vastgelegd door de query.</span><span class="sxs-lookup"><span data-stu-id="73f43-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="73f43-328">Toen deze id werd gemaakt, werden er twee regels toegevoegd: een voor 25 ea en een andere voor 10 ea.</span><span class="sxs-lookup"><span data-stu-id="73f43-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="73f43-329">Het werk werd nog steeds getoond aan de gebruiker, omdat ten minste één werkregel een hoeveelheid van minder dan 20 ea heeft.</span><span class="sxs-lookup"><span data-stu-id="73f43-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="73f43-330">Afhankelijk van het scenario kunt u dit gedrag voorkomen door werkopsplitsingen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="73f43-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
