---
title: Orderverzamelregels groeperen
description: Dit onderwerp bevat een overzicht van de groepering van orderverzamelregels.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fe0e63ef742b7bfd09684a94d273a1841d24599c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828268"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="7bfde-103">Orderverzamelregels groeperen</span><span class="sxs-lookup"><span data-stu-id="7bfde-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bfde-104">Bij het groeperen van orderverzamelregels kunnen meerdere werkregels met hetzelfde artikel en dezelfde locatie worden gecombineerd in één orderverzameling die voor de gebruiker wordt weergegeven op het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="7bfde-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="7bfde-105">Op deze manier kunnen magazijnmedewerkers de meest efficiënte instructies ontvangen, maar wordt tegelijkertijd de vereiste scheiding van werkregels in het systeem gehandhaafd (bijvoorbeeld voor verschillende containers, orders enzovoort).</span><span class="sxs-lookup"><span data-stu-id="7bfde-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="7bfde-106">De functie Orderverzamelregels groeperen inschakelen</span><span class="sxs-lookup"><span data-stu-id="7bfde-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="7bfde-107">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="7bfde-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="7bfde-108">Beheerders kunnen gebruikmaken van het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en de functie desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="7bfde-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7bfde-109">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="7bfde-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7bfde-110">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="7bfde-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7bfde-111">**Functienaam:** *Orderverzamelregels groeperen*</span><span class="sxs-lookup"><span data-stu-id="7bfde-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="7bfde-112">De groepering van orderverzamelregels instellen</span><span class="sxs-lookup"><span data-stu-id="7bfde-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="7bfde-113">Een menuopdracht van mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="7bfde-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="7bfde-114">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="7bfde-115">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="7bfde-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7bfde-116">Voer in het veld **Naam menuopdracht** *Orderverzameling voor verkoopgroepsregels* in.</span><span class="sxs-lookup"><span data-stu-id="7bfde-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="7bfde-117">Voer in het veld **Titel** *Orderverzameling voor verkoopgroepsregel* in.</span><span class="sxs-lookup"><span data-stu-id="7bfde-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="7bfde-118">Deze titel wordt weergegeven in het menu van het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="7bfde-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="7bfde-119">Selecteer **Werk** in het veld *Modus*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="7bfde-120">Stel de optie **Bestaand werk gebruiken** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="7bfde-121">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="7bfde-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7bfde-122">Selecteer **Door gebruiker bestuurd** in het veld *Bestuurd door*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="7bfde-123">Stel de optie **Nummerplaat maken** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="7bfde-124">Stel de optie **Groep verzamelen** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="7bfde-125">Accepteer de standaardwaarden voor de overige opties.</span><span class="sxs-lookup"><span data-stu-id="7bfde-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="7bfde-126">Voer de volgende stappen uit om de geldige werkklassen voor de menuopdracht voor mobiele apparaten te configureren:</span><span class="sxs-lookup"><span data-stu-id="7bfde-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="7bfde-127">Selecteer **Nieuw** op het sneltabblad **Werkklassen**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="7bfde-128">In het veld **Werkklasse-id** kunt u *Verkoop* of *VO verzamelen* selecteren, afhankelijk van het magazijn dat u gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7bfde-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="7bfde-129">Selecteer voor dit scenario *VO verzamelen*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="7bfde-130">Het veld **Werkordertype** wordt automatisch ingesteld op *Verkooporders*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="7bfde-131">Een menu van een mobiel apparaat instellen</span><span class="sxs-lookup"><span data-stu-id="7bfde-131">Set up a mobile device menu</span></span>

<span data-ttu-id="7bfde-132">Voer deze stappen uit om de menuopdracht die u zojuist hebt gemaakt, toe te voegen aan het menu **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="7bfde-133">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="7bfde-134">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="7bfde-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="7bfde-135">In het lijstvenster worden alle bestaande menu's van het mobiele apparaat weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7bfde-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="7bfde-136">Selecteer *Uitgaand* in de lijst.</span><span class="sxs-lookup"><span data-stu-id="7bfde-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="7bfde-137">Zoek en selecteer in de lijst **Beschikbare menu's en menuopdrachten** de menuopdracht *Orderverzameling voor verkoopgroepsregel* die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7bfde-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="7bfde-138">Selecteer de pijlknop naar rechts om de menuopdracht *Orderverzameling voor verkoopgroepsregel* te verplaatsen naar de lijst **Menustructuur**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="7bfde-139">Gebruik de pijlknoppen omhoog en omlaag om de menuopdracht naar de gewenste positie in de menustructuur te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="7bfde-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="7bfde-140">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="7bfde-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="7bfde-141">Een werksjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="7bfde-141">Set up a work template</span></span>

1. <span data-ttu-id="7bfde-142">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="7bfde-143">Selecteer *Verkooporders* in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="7bfde-144">Zoek en selecteer in het raster **Overzicht** de werksjabloon die met deze functie moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7bfde-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="7bfde-145">Selecteer voor dit scenario de sjabloon *51 orderverzamelen voor klaarzetten*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="7bfde-146">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="7bfde-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="7bfde-147">Selecteer in het dialoogvenster Query-editor op het tabblad **Sorteren** de optie **Toevoegen** en stel vervolgens de volgende waarden voor de nieuwe rij in:</span><span class="sxs-lookup"><span data-stu-id="7bfde-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="7bfde-148">Selecteer **Tijdelijke werktransacties** in de kolom *Tabel*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="7bfde-149">Selecteer **Tijdelijke werktransacties** in de kolom *Afgeleide tabel*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="7bfde-150">Selecteer **Artikelnummer** in de kolom *Veld*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="7bfde-151">Selecteer **Oplopend** in de kolom *Zoekrichting*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="7bfde-152">Selecteer **OK** om het dialoogvenster te sluiten en uw selectie op te slaan.</span><span class="sxs-lookup"><span data-stu-id="7bfde-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="7bfde-153">Het volgende bericht wordt weergegeven: 'Groeperen wordt opnieuw ingesteld, doorgaan?'</span><span class="sxs-lookup"><span data-stu-id="7bfde-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="7bfde-154">Selecteer **Ja** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="7bfde-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bfde-155">De groepering van orderverzamelregels werkt alleen als de werkregels zijn gesorteerd op artikel-id.</span><span class="sxs-lookup"><span data-stu-id="7bfde-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="7bfde-156">Als regels met dezelfde artikels niet na elkaar worden geordend, worden ze niet gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="7bfde-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="7bfde-157">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7bfde-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="7bfde-158">Orderverzamelingswerk maken</span><span class="sxs-lookup"><span data-stu-id="7bfde-158">Create picking work</span></span>

<span data-ttu-id="7bfde-159">Voordat u de groepering van orderverzamelregels kunt instellen, moet u in aanmerking komend uitgaand werk maken.</span><span class="sxs-lookup"><span data-stu-id="7bfde-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="7bfde-160">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7bfde-161">Selecteer **Nieuw** om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="7bfde-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="7bfde-162">Selecteer *US-004* in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="7bfde-163">Selecteer op het sneltabblad **Algemeen** magazijn **51** in het veld *Magazijn*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="7bfde-164">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-164">Select **OK**.</span></span>
1. <span data-ttu-id="7bfde-165">Voeg op het sneltabblad **Verkooporderregels** de volgende zes regels toe:</span><span class="sxs-lookup"><span data-stu-id="7bfde-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="7bfde-166">**Regel 1:** selecteer in het veld **Artikelnummer** de optie *M9200*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="7bfde-167">Typ **3** in het veld *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="7bfde-168">**Regel 2:** selecteer in het veld **Artikelnummer** de optie *M9201*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="7bfde-169">Typ **3** in het veld *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="7bfde-170">**Regel 3:** selecteer in het veld **Artikelnummer** de optie *M9202*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="7bfde-171">Typ **2** in het veld *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="7bfde-172">**Regel 4:** selecteer in het veld **Artikelnummer** de optie *M9200*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="7bfde-173">Typ **1** in het veld *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="7bfde-174">**Regel 5:** selecteer in het veld **Artikelnummer** de optie *M9200*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="7bfde-175">Typ **3** in het veld *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="7bfde-176">**Regel 6:** selecteer in het veld **Artikelnummer** de optie *M9202*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="7bfde-177">Typ **7** in het veld *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="7bfde-178">Hier is een overzicht van de totale aantallen voor elk artikel:</span><span class="sxs-lookup"><span data-stu-id="7bfde-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="7bfde-179">**Artikel M9200:** *7* stuks</span><span class="sxs-lookup"><span data-stu-id="7bfde-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="7bfde-180">**Artikel M9201:** *3* stuks</span><span class="sxs-lookup"><span data-stu-id="7bfde-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="7bfde-181">**Artikel M9202:** *9* stuks</span><span class="sxs-lookup"><span data-stu-id="7bfde-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="7bfde-182">Voordat u de orders aan het magazijn vrijgeeft, moet u ervoor zorgen dat de picklocaties voldoende voorraad hebben voor alle artikelen op alle orders.</span><span class="sxs-lookup"><span data-stu-id="7bfde-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="7bfde-183">Controleer de instelling **Locatie-instructie** om te bepalen welke orderverzamellocaties worden gebruikt voor het verzamelen van verkooporders.</span><span class="sxs-lookup"><span data-stu-id="7bfde-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="7bfde-184">Als u de Demonstratiegegevensomgeving van Contoso voor magazijn *51* gebruikt, bevestigt u dat er beschikbare voorraad is.</span><span class="sxs-lookup"><span data-stu-id="7bfde-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="7bfde-185">U moet nu de voorraad voor elke regel reserveren.</span><span class="sxs-lookup"><span data-stu-id="7bfde-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="7bfde-186">Selecteer op het sneltabblad **Verkooporderregels** een van de regels die moeten worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="7bfde-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="7bfde-187">Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="7bfde-188">Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om de reservering toe te passen.</span><span class="sxs-lookup"><span data-stu-id="7bfde-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="7bfde-189">Sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="7bfde-189">Then close the page.</span></span>
1. <span data-ttu-id="7bfde-190">Herhaal stap 8 tot en met 10 voor de overige regels die moeten worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="7bfde-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="7bfde-191">U moet nu de verkooporder aan het magazijn vrijgeven.</span><span class="sxs-lookup"><span data-stu-id="7bfde-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="7bfde-192">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="7bfde-193">U ontvangt een bericht waarin wordt bericht dat er een zending en een wave zijn gemaakt en dat de wave is verzonden om te worden uitgevoerd in een batch.</span><span class="sxs-lookup"><span data-stu-id="7bfde-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="7bfde-194">Wanneer de wave en alle taken verderop in de stroom zijn voltooid, wordt een werk-id gemaakt voor werk met zes regels.</span><span class="sxs-lookup"><span data-stu-id="7bfde-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="7bfde-195">De regels worden gesorteerd op artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="7bfde-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="7bfde-196">Ga naar **Magazijnbeheer \> Werk \> Alle werkzaamheden** om het gemaakte werk weer te geven.</span><span class="sxs-lookup"><span data-stu-id="7bfde-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="7bfde-197">Noteer de waarde van de **Werk-id** omdat u deze in de volgende procedure nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="7bfde-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="7bfde-198">Order verzamelen starten vanaf het mobiele apparaat</span><span class="sxs-lookup"><span data-stu-id="7bfde-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="7bfde-199">Meld u aan bij het mobiele apparaat als een gebruiker met instellingen voor magazijn *51*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="7bfde-200">Selecteer op het mobiele apparaat het menu dat de nieuwe menuoptie voor mobiele apparaten bevat.</span><span class="sxs-lookup"><span data-stu-id="7bfde-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="7bfde-201">Selecteer voor dit scenario **Uitgaand**.</span><span class="sxs-lookup"><span data-stu-id="7bfde-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="7bfde-202">Selecteer de menuopdracht **Orderverzameling voor verkoopgroepsregels** en initieer de orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="7bfde-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="7bfde-203">Voer de waarde van de **werk-ID** in die u in de vorige procedure hebt genoteerd.</span><span class="sxs-lookup"><span data-stu-id="7bfde-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="7bfde-204">U ziet een verzamelstap waarin alle orderverzamelregels voor artikel *M9200* worden gegroepeerd, en u moet een instructie ontvangen om van elk artikel *M9200* *7* te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="7bfde-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7bfde-205">Op het mobiele apparaat is de orderverzameling voor de drie verzamelwerkregels samengevoegd in één verzamelstap voor de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="7bfde-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="7bfde-206">Bevestig de verzamelstap.</span><span class="sxs-lookup"><span data-stu-id="7bfde-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="7bfde-207">Ga naar de werkpagina voor de werk-id. U ziet dan dat alle drie de orderverzamelregels voor artikel *M9200* tegelijkertijd zijn gesloten.</span><span class="sxs-lookup"><span data-stu-id="7bfde-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="7bfde-208">Ga terug naar het mobiele apparaat en ga verder met verzamelen.</span><span class="sxs-lookup"><span data-stu-id="7bfde-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="7bfde-209">Werkregel 4 voor artikel *M9201* moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7bfde-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="7bfde-210">Aangezien de order slechts één werkregel heeft, hoeft er niets te worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="7bfde-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="7bfde-211">Bevestig de verzamelstap.</span><span class="sxs-lookup"><span data-stu-id="7bfde-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="7bfde-212">Met de laatste orderverzamelstap op het mobiele apparaat worden de laatste twee orderverzamelregels uit de werkorder samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="7bfde-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="7bfde-213">Voltooi de orderverzamelstap voor *9* stuks van artikel *M9202*.</span><span class="sxs-lookup"><span data-stu-id="7bfde-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="7bfde-214">Bevestig de wegzetstap en eventuele extra verzamel-/wegzetparen om het werk te voltooien.</span><span class="sxs-lookup"><span data-stu-id="7bfde-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="7bfde-215">Werkregels kunnen alleen worden gegroepeerd als ze op volgorde zijn.</span><span class="sxs-lookup"><span data-stu-id="7bfde-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="7bfde-216">De volgende functionaliteit wordt niet ondersteund:</span><span class="sxs-lookup"><span data-stu-id="7bfde-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="7bfde-217">Catch weight-artikelen.</span><span class="sxs-lookup"><span data-stu-id="7bfde-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="7bfde-218">Als er catch weight-artikelen voor het werk aanwezig zijn, wordt een foutbericht weergegeven voordat u begint te kiezen.</span><span class="sxs-lookup"><span data-stu-id="7bfde-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="7bfde-219">Orderverzameling</span><span class="sxs-lookup"><span data-stu-id="7bfde-219">Piece picking</span></span>
>   - <span data-ttu-id="7bfde-220">Werkregels met onvoltooid aanvullingswerk</span><span class="sxs-lookup"><span data-stu-id="7bfde-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="7bfde-221">Meerverzameling</span><span class="sxs-lookup"><span data-stu-id="7bfde-221">Over-picking</span></span>
>   - <span data-ttu-id="7bfde-222">Kort orderverzamelen met artikelhertoewijzing</span><span class="sxs-lookup"><span data-stu-id="7bfde-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]