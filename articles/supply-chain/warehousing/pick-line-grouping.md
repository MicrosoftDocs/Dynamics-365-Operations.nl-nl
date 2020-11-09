---
title: Orderverzamelregels groeperen
description: Dit onderwerp bevat een overzicht van de groepering van orderverzamelregels.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017731"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="0555a-103">Orderverzamelregels groeperen</span><span class="sxs-lookup"><span data-stu-id="0555a-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0555a-104">Bij het groeperen van orderverzamelregels kunnen meerdere werkregels met hetzelfde artikel en dezelfde locatie worden gecombineerd in één orderverzameling die voor de gebruiker wordt weergegeven op een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="0555a-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="0555a-105">Op deze manier kunnen magazijnmedewerkers de meest efficiënte instructies ontvangen die mogelijk zijn, maar de vereiste scheiding van werkregels in het systeem wordt ook gehandhaafd (bijvoorbeeld voor verschillende containers en orders).</span><span class="sxs-lookup"><span data-stu-id="0555a-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="0555a-106">De groepering van orderverzamelregels instellen</span><span class="sxs-lookup"><span data-stu-id="0555a-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="0555a-107">Een menuopdracht van mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="0555a-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="0555a-108">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat** en maak een nieuwe menuoptie met de naam **Orderverzameling voor verkoopgroepsregels – Door gebruiker gestuurd**.</span><span class="sxs-lookup"><span data-stu-id="0555a-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items** , and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="0555a-109">Stel onder **Menuopties voor mobiel apparaat** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="0555a-109">Under **Mobile device menu items** , set the following values:</span></span>

    - <span data-ttu-id="0555a-110">Voer in het veld **Naam van menuopdracht** de tekst **Orderverzamelen verkoop - Groepsregel** in.</span><span class="sxs-lookup"><span data-stu-id="0555a-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="0555a-111">Voer in het veld **Titel** de tekst **Orderverzamelen verkoop - Groepsregel** in.</span><span class="sxs-lookup"><span data-stu-id="0555a-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="0555a-112">Selecteer **Werk** in het veld **Modus**.</span><span class="sxs-lookup"><span data-stu-id="0555a-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="0555a-113">Stel de optie **Bestaand werk gebruiken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0555a-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="0555a-114">Op het sneltabblad **Algemeen** kunt u de volgende waarden instellen:</span><span class="sxs-lookup"><span data-stu-id="0555a-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="0555a-115">Selecteer **Door gebruiker bestuurd** in het veld **Bestuurd door**.</span><span class="sxs-lookup"><span data-stu-id="0555a-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="0555a-116">Stel de optie **Nummerplaat maken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0555a-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="0555a-117">Stel de optie **Groep verzamelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0555a-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="0555a-118">Voer op het sneltabblad **Werkklassen** de volgende stappen uit om de geldige werkklassen voor de menuopdracht voor mobiele apparaten te configureren:</span><span class="sxs-lookup"><span data-stu-id="0555a-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="0555a-119">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0555a-119">Select **New**.</span></span>
    2. <span data-ttu-id="0555a-120">Selecteer in het veld **Werkklasse-id** de optie **Verkoop** of **VO verzamelen** , afhankelijk van het magazijn dat u gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0555a-120">In the **Work class ID** field, select **Sales** or **SO Pick** , depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="0555a-121">Selecteer **Verkooporders** in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="0555a-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="0555a-122">Een menu van een mobiel apparaat instellen</span><span class="sxs-lookup"><span data-stu-id="0555a-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="0555a-123">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="0555a-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="0555a-124">Voeg de zojuist gemaakte menuoptie toe aan het gewenste menu.</span><span class="sxs-lookup"><span data-stu-id="0555a-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="0555a-125">Een werksjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="0555a-125">Set up a work template</span></span>

1. <span data-ttu-id="0555a-126">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="0555a-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="0555a-127">Zoek de werksjabloon die met deze functie moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0555a-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="0555a-128">Selecteer voor dit voorbeeld de standaardwerksjabloon van Contoso **51 Orderverzamelen voor fase**.</span><span class="sxs-lookup"><span data-stu-id="0555a-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="0555a-129">Selecteer **Query bewerken** in het menu.</span><span class="sxs-lookup"><span data-stu-id="0555a-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="0555a-130">Selecteer op het tabblad **Sorteren** de optie **Toevoegen** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="0555a-130">On the **Sorting** tab, select **Add** , and then set the following values:</span></span>

    - <span data-ttu-id="0555a-131">Selecteer **Tijdelijke werktransacties** in het veld **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="0555a-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="0555a-132">Selecteer **Tijdelijke werktransacties** in het veld **Afgeleide tabel**.</span><span class="sxs-lookup"><span data-stu-id="0555a-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="0555a-133">Selecteer **Artikelnummer** in het veld **Veld**.</span><span class="sxs-lookup"><span data-stu-id="0555a-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="0555a-134">Selecteer **Oplopend** in het veld **Zoekrichting**.</span><span class="sxs-lookup"><span data-stu-id="0555a-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="0555a-135">De groepering van orderverzamelregels werkt alleen als de werkregels zijn gesorteerd op artikel-id.</span><span class="sxs-lookup"><span data-stu-id="0555a-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="0555a-136">Als regels met dezelfde artikels niet na elkaar worden geordend, worden ze niet gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="0555a-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="0555a-137">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="0555a-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="0555a-138">Orderverzamelingswerk maken</span><span class="sxs-lookup"><span data-stu-id="0555a-138">Create picking work</span></span>

<span data-ttu-id="0555a-139">Voordat u de groepering van orderverzamelregels kunt instellen, moet u in aanmerking komend uitgaand werk maken.</span><span class="sxs-lookup"><span data-stu-id="0555a-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="0555a-140">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="0555a-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="0555a-141">Selecteer **Nieuw** om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="0555a-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="0555a-142">Selecteer een klant in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="0555a-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="0555a-143">Selecteer op het sneltabblad **Algemeen** magazijn **51** in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="0555a-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="0555a-144">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0555a-144">Then select **OK**.</span></span>
5. <span data-ttu-id="0555a-145">Voeg onder **Verkooporderregels** de volgende zes regels toe:</span><span class="sxs-lookup"><span data-stu-id="0555a-145">Under **Sales order lines** , add the following six lines:</span></span>

    - <span data-ttu-id="0555a-146">**Regel 1:** selecteer in het veld **Artikelnummer** de optie **M9200**.</span><span class="sxs-lookup"><span data-stu-id="0555a-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="0555a-147">Typ **3** in het veld **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="0555a-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="0555a-148">**Regel 2:** selecteer in het veld **Artikelnummer** de optie **M9201**.</span><span class="sxs-lookup"><span data-stu-id="0555a-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="0555a-149">Typ **3** in het veld **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="0555a-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="0555a-150">**Regel 3:** selecteer in het veld **Artikelnummer** de optie **M9202**.</span><span class="sxs-lookup"><span data-stu-id="0555a-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="0555a-151">Typ **2** in het veld **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="0555a-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="0555a-152">**Regel 4:** selecteer in het veld **Artikelnummer** de optie **M9200**.</span><span class="sxs-lookup"><span data-stu-id="0555a-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="0555a-153">Typ **1** in het veld **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="0555a-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="0555a-154">**Regel 5:** selecteer in het veld **Artikelnummer** de optie **M9200**.</span><span class="sxs-lookup"><span data-stu-id="0555a-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="0555a-155">Typ **3** in het veld **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="0555a-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="0555a-156">**Regel 6:** selecteer in het veld **Artikelnummer** de optie **M9202**.</span><span class="sxs-lookup"><span data-stu-id="0555a-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="0555a-157">Typ **7** in het veld **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="0555a-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="0555a-158">Hier is een overzicht van de totale aantallen voor elk artikel:</span><span class="sxs-lookup"><span data-stu-id="0555a-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="0555a-159">**Artikel M9200:** 7 elk</span><span class="sxs-lookup"><span data-stu-id="0555a-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="0555a-160">**Artikel M9201:** 3 elk</span><span class="sxs-lookup"><span data-stu-id="0555a-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="0555a-161">**Artikel M9202:** 9 elk</span><span class="sxs-lookup"><span data-stu-id="0555a-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="0555a-162">Voordat u de orders aan het magazijn vrijgeeft, moet u ervoor zorgen dat de picklocaties voldoende voorraad hebben voor alle artikelen op alle orders.</span><span class="sxs-lookup"><span data-stu-id="0555a-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="0555a-163">Controleer de instelling **Locatie-instructie** om te bepalen welke orderverzamellocaties worden gebruikt voor het verzamelen van verkooporders.</span><span class="sxs-lookup"><span data-stu-id="0555a-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="0555a-164">Reserveer de voorraad en geef deze vrij aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="0555a-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="0555a-165">Er wordt een werk-id met zes regels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0555a-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="0555a-166">De regels worden gesorteerd op artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="0555a-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="0555a-167">De stroom voor mobiele apparaten uitvoeren</span><span class="sxs-lookup"><span data-stu-id="0555a-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="0555a-168">Selecteer op het mobiele apparaat het menu dat de nieuwe menuoptie voor mobiele apparaten bevat.</span><span class="sxs-lookup"><span data-stu-id="0555a-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="0555a-169">Selecteer de menuoptie **Orderverzamelen verkoop - Groepsregel** en initieer de orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="0555a-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="0555a-170">Nadat u het menu hebt selecteren en de werk-id hebt ingevoerd, ziet u de verzamelstap waarin alle pickregels voor artikel M9200 zijn gegroepeerd.</span><span class="sxs-lookup"><span data-stu-id="0555a-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="0555a-171">U ontvangt de instructie om 7 stuks van elk artikel M9200 te kiezen.</span><span class="sxs-lookup"><span data-stu-id="0555a-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="0555a-172">Bevestig de verzamelstap.</span><span class="sxs-lookup"><span data-stu-id="0555a-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="0555a-173">Ga naar het clientscherm van het onderhanden werk om te zien dat alle drie de orderverzamelregels voor artikel M9200 tegelijkertijd zijn gesloten.</span><span class="sxs-lookup"><span data-stu-id="0555a-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="0555a-174">Werkregel 4 wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0555a-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="0555a-175">Bevestig de verzamelstap.</span><span class="sxs-lookup"><span data-stu-id="0555a-175">Confirm the pick step.</span></span>

    <span data-ttu-id="0555a-176">Met de laatste orderverzamelstap op het mobiele apparaat worden de laatste twee orderverzamelregels uit de werkorder samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="0555a-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="0555a-177">Voltooi de orderverzamelstap voor 9 stuks van elk artikel M9202.</span><span class="sxs-lookup"><span data-stu-id="0555a-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="0555a-178">Bevestig de wegzetstap en eventuele extra verzamel-/wegzetparen om het werk te voltooien.</span><span class="sxs-lookup"><span data-stu-id="0555a-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="0555a-179">Werkregels kunnen alleen worden gegroepeerd als ze op volgorde zijn.</span><span class="sxs-lookup"><span data-stu-id="0555a-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="0555a-180">De volgende functionaliteit wordt niet ondersteund:</span><span class="sxs-lookup"><span data-stu-id="0555a-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="0555a-181">Catch weight-artikelen.</span><span class="sxs-lookup"><span data-stu-id="0555a-181">Catch-weight items.</span></span> <span data-ttu-id="0555a-182">Als er catch weight-artikelen voor het werk aanwezig zijn, wordt een foutbericht weergegeven voordat u begint te kiezen.</span><span class="sxs-lookup"><span data-stu-id="0555a-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="0555a-183">Orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="0555a-183">Piece picking.</span></span>
>    - <span data-ttu-id="0555a-184">Werkregels met onvoltooid aanvullingswerk.</span><span class="sxs-lookup"><span data-stu-id="0555a-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="0555a-185">Meerverzameling.</span><span class="sxs-lookup"><span data-stu-id="0555a-185">Over-picking.</span></span>
>    - <span data-ttu-id="0555a-186">Kort orderverzamelen met artikelhertoewijzing</span><span class="sxs-lookup"><span data-stu-id="0555a-186">Short picking with item reallocation</span></span>
