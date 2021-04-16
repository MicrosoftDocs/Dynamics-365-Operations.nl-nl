---
title: Locatiegebruik bij artikelconsolidatie
description: Dit onderwerp bevat informatie over de functionaliteit waarmee magazijnbeheerders het volumetrische gebruik van locaties in het magazijn kunnen weergeven en filteren. Managers kunnen locaties selecteren en voorraadmutaties uitvoeren, rechtstreeks vanaf de pagina Artikelconsolidatie om artikelen te consolideren en zodoende de magazijnruimte beter te gebruiken.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 892190ea7bad34dfd308796b93a1828e0e8e11b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835560"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="c7b0b-104">Locatiegebruik bij artikelconsolidatie</span><span class="sxs-lookup"><span data-stu-id="c7b0b-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7b0b-105">Dit onderwerp bevat informatie over de functionaliteit waarmee magazijnbeheerders het volumetrische gebruik van locaties in het magazijn kunnen weergeven en filteren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="c7b0b-106">Managers kunnen locaties selecteren en voorraadmutaties uitvoeren, rechtstreeks vanaf de pagina **Artikelconsolidatie** om artikelen te consolideren en zodoende de magazijnruimte beter te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="c7b0b-107">De functies inschakelen</span><span class="sxs-lookup"><span data-stu-id="c7b0b-107">Turn on the features</span></span>

<span data-ttu-id="c7b0b-108">Voordat u de in dit onderwerp beschreven functies kunt gebruiken, moet u deze in het systeem inschakelen.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="c7b0b-109">Beheerders kunnen gebruikmaken van het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functies te controleren en deze zo nodig in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="c7b0b-110">Schakel de beide volgende functies in in de volgorde waarin ze worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="c7b0b-111">(Beide functies zijn voor de module **Magazijnbeheer**.)</span><span class="sxs-lookup"><span data-stu-id="c7b0b-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="c7b0b-112">Status magazijnlocatie</span><span class="sxs-lookup"><span data-stu-id="c7b0b-112">Warehouse location status</span></span>
2. <span data-ttu-id="c7b0b-113">Locatiegebruik artikelconsolidatie</span><span class="sxs-lookup"><span data-stu-id="c7b0b-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="c7b0b-114">Status magazijnlocatie</span><span class="sxs-lookup"><span data-stu-id="c7b0b-114">Warehouse location status</span></span>

<span data-ttu-id="c7b0b-115">Met de functie *Status magazijnlocatie* kunt u vier nieuwe velden toevoegen aan de pagina **Locaties** om extra informatie over de huidige staat van de locatie bij te houden:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="c7b0b-116">**Artikelnummer:** Het artikel dat zich momenteel op de locatie bevindt.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="c7b0b-117">Als de locatie meerdere artikelen bevat, is dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="c7b0b-118">**Datum en tijd van de laatste activiteit:** De tijdstempel van de laatste magazijntransactie die is uitgevoerd op de locatie.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="c7b0b-119">**Ouderdomsdatum:** De datum waarop de voorraad op de locatie in het magazijn is binnengebracht.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="c7b0b-120">Deze datum wordt berekend op basis van de ouderdomsdatum van de nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="c7b0b-121">Deze waarde is nauwkeurig voor locaties die met een nummerplaat worden gevolgd, maar mogelijk niet juist voor locaties die niet worden gevolgd met een nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="c7b0b-122">**Locatiestatus:** De status van de locatie.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="c7b0b-123">Er zijn vier waarden beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-123">Four values are available:</span></span>

    - <span data-ttu-id="c7b0b-124">**Onbepaald:** het locatieprofiel kan de status niet bijhouden.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="c7b0b-125">Daarom is de huidige status onbekend.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="c7b0b-126">**Leeg:** er is momenteel geen voorraad op de locatie.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="c7b0b-127">**Orderverzameling:** uitgaande transacties zijn uitgevoerd op de locatie nadat deze voor het laatst leeg was.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="c7b0b-128">**Opslag:** alleen ingaande transacties zijn uitgevoerd sinds de locatie voor het laatst leeg was.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="c7b0b-129">Met behulp van deze velden kunnen magazijnbeheerders een beter overzicht krijgen van de status van de magazijnlocaties.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="c7b0b-130">Ze bieden ook meer mogelijkheden voor geavanceerde rapportage en filteren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="c7b0b-131">Artikelconsolidatie en locatiegebruik instellen</span><span class="sxs-lookup"><span data-stu-id="c7b0b-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="c7b0b-132">In deze sectie wordt beschreven hoe u uw systeem voorbereidt op het gebruik van artikelconsolidatie en locatiegebruik.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="c7b0b-133">In de procedures worden voorbeeldwaarden uit de standaard demogegevens gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="c7b0b-134">Als u het voorbeeldscenario dat verderop in dit onderwerp wordt beschreven wilt doorlopen, selecteert u de rechtspersoon **USMF** (die de standaard demogegevens bevat) en maakt u elke record die in deze sectie wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="c7b0b-135">Als u het voorbeeldscenario niet wilt doorlopen, kunt u de waarden die hier worden opgegeven, beschouwen als voorbeelden van de typen instellingen die u moet voltooien om de functies te kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="c7b0b-136">Vrijgegeven product</span><span class="sxs-lookup"><span data-stu-id="c7b0b-136">Released product</span></span>

1. <span data-ttu-id="c7b0b-137">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c7b0b-138">Selecteer **M9201** in het veld *Artikelnummer* en open de pagina Details.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="c7b0b-139">Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Magazijn** de optie **Fysieke afmetingen**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="c7b0b-140">Selecteer op de pagina **Fysieke afmetingen** in het actievenster de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="c7b0b-141">Er wordt een nieuwe regel aan het raster toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-141">A new line is added to the grid.</span></span> <span data-ttu-id="c7b0b-142">Het veld **Artikelnummer** is vooraf ingesteld.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="c7b0b-143">Selecteer **ea** in het veld *Eenheid*.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="c7b0b-144">De resterende velden op de regel worden automatisch ingesteld.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="c7b0b-145">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="c7b0b-146">Locatieprofiel</span><span class="sxs-lookup"><span data-stu-id="c7b0b-146">Location profile</span></span>

1. <span data-ttu-id="c7b0b-147">Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="c7b0b-148">Selecteer in de lijst met locatieprofielen de waarde **FLOOR-05**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="c7b0b-149">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c7b0b-150">Controleer op het sneltabblad **Algemeen** of beide volgende opties zijn ingesteld op *Ja*:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="c7b0b-151">Artikel in locatie inschakelen</span><span class="sxs-lookup"><span data-stu-id="c7b0b-151">Enable item in location</span></span>
    - <span data-ttu-id="c7b0b-152">Locatiestatus inschakelen</span><span class="sxs-lookup"><span data-stu-id="c7b0b-152">Enable location status</span></span>

1. <span data-ttu-id="c7b0b-153">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c7b0b-154">Als de opties **Artikel in locatie inschakelen** en **Locatiestatus inschakelen** al zijn ingesteld op *Ja*, gaat u verder met de instructies voor het instellen van het sneltabblad **Dimensies** in stap 10.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="c7b0b-155">Als de opties nog niet zijn ingesteld op *Ja*, moet u een consistentiecontrole uitvoeren voor de module **Magazijnbeheer**, nadat u deze handmatig hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="c7b0b-156">Ga in dat geval verder met de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="c7b0b-157">Als u de consistentiecontrole wilt uitvoeren, gaat u naar **Systeembeheer \> Periodieke taken \> Database \> Consistentiecontrole**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="c7b0b-158">Stel in het dialoogvenster **Consistentiecontrole** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c7b0b-159">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="c7b0b-160">**Controleren/corrigeren:** *Controleren*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="c7b0b-161">**Begindatum:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="c7b0b-162">**Consistentiecontrole status magazijnlocatie:** schakel dit selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="c7b0b-163">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="c7b0b-164">U ontvangt een melding wanneer de consistentiecontrole is voltooid.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="c7b0b-165">Open het [Actiecentrum](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) om het bericht weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="c7b0b-166">Selecteer **Berichtdetails** om de details weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="c7b0b-167">Als het bericht voor de consistentiecontrole als volgt luidt: 'Onjuiste locatiestatus gevonden voor locatie XXXX in magazijn XX', moet u de consistentiecontrole opnieuw uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="c7b0b-168">Stel het veld **Controleren/corrigeren** nu in op *Fout oplossen*.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="c7b0b-169">Geef de berichten weer om er zeker van te zijn dat er geen fouten zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="c7b0b-170">U moet nu het instellen van het locatieprofiel voltooien.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="c7b0b-171">Ga terug naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locatieprofielen**, selecteer locatieprofiel **FLOOR-05** en selecteer vervolgens **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c7b0b-172">Stel op het sneltabblad **Dimensies** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c7b0b-173">**Volumegebruikspercentage:** *100*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="c7b0b-174">**Volumetrische methode gebruikt voor voorraadlocatie:** *Locatievolume gebruiken*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="c7b0b-175">**Werkelijke locatiehoogte:** *10*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="c7b0b-176">**Werkelijke locatiebreedte:** *10*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="c7b0b-177">**Werkelijke locatiediepte:** *10*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="c7b0b-178">**Maximumgewicht:** *100*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="c7b0b-179">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="c7b0b-180">Menuopties voor mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="c7b0b-180">Mobile device menu items</span></span>

1. <span data-ttu-id="c7b0b-181">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c7b0b-182">Selecteer in het actievenster de optie **Nieuw** om een menuoptie te maken voor sorteren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="c7b0b-183">Stel in de header de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="c7b0b-184">**Naam menuopdracht:** *Correctie in*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="c7b0b-185">**Titel:** *Correctie in*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="c7b0b-186">**Modus:** *werk*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c7b0b-187">**Bestaand werk gebruiken:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="c7b0b-188">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c7b0b-189">**Procedure voor het maken van werk:** *Correctie in*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="c7b0b-190">**Voorraadcorrectietypen:** *Correctie in*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="c7b0b-191">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="c7b0b-192">Menu voor mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="c7b0b-192">Mobile device menu</span></span>

1. <span data-ttu-id="c7b0b-193">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="c7b0b-194">Selecteer in de lijst met menu's de waarde **Voorraad**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="c7b0b-195">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c7b0b-196">Zoek en selecteer in de lijst **Beschikbare menu's en menuopdrachten** de menuopdracht **Correctie in**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="c7b0b-197">Selecteer de knop pijl-rechts om **Correctie in** naar de lijst **Menustructuur** te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="c7b0b-198">Op deze manier voegt u de nieuwe menuopdracht toe aan het geselecteerde menu.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="c7b0b-199">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="c7b0b-200">Mutatietypen</span><span class="sxs-lookup"><span data-stu-id="c7b0b-200">Movement types</span></span>

1. <span data-ttu-id="c7b0b-201">Ga naar **Magazijnbeheer \> Instellingen \> Voorraad \> Mutatietypen**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="c7b0b-202">Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="c7b0b-203">**Code mutatietype:** *CONSOLIDEREN*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="c7b0b-204">**Omschrijving:** *Locaties consolideren*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="c7b0b-205">**Werkklasse-id:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="c7b0b-206">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c7b0b-207">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="c7b0b-207">Example scenario</span></span>

<span data-ttu-id="c7b0b-208">In het volgende scenario wordt de mobiele app Magazijnbeheer op een mobiel apparaat gebruikt om een *aanpassing in* voor de voorraad in te stellen op twee locaties in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-208">The following scenario uses the Warehouse Management mobile app to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="c7b0b-209">Voorraad toevoegen aan locaties</span><span class="sxs-lookup"><span data-stu-id="c7b0b-209">Add inventory to locations</span></span>

1. <span data-ttu-id="c7b0b-210">Meld u aan bij het mobiele apparaat als een gebruiker met instellingen voor magazijn *51*.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="c7b0b-211">Ga naar **Voorraad \> Correctie in**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="c7b0b-212">U gaat nu de eerste locatiecorrectie invoeren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="c7b0b-213">Selecteer in de taak **Correctie in** de locatie waarvoor u de voorraadcorrectie wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="c7b0b-214">Selecteer **LP-001** in het veld *LOC*.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="c7b0b-215">Bevestig de locatie.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-215">Confirm the location.</span></span>
1. <span data-ttu-id="c7b0b-216">Maak een nummerplaat-id voor het artikel dat aan de locatie wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="c7b0b-217">Voer in het veld **LP** de waarde *LP00101* in.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="c7b0b-218">Bevestig de nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="c7b0b-219">Voer het artikel in dat aan de nummerplaat wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="c7b0b-220">Voer in het veld **ITEM** de waarde *M9201* in.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="c7b0b-221">Bevestig het artikel.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-221">Confirm the item.</span></span>
1. <span data-ttu-id="c7b0b-222">Voer de hoeveelheid in van het artikel dat wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="c7b0b-223">Typ **10** in het veld *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="c7b0b-224">Bevestig de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-224">Confirm the quantity.</span></span>

    <span data-ttu-id="c7b0b-225">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="c7b0b-226">U gaat nu de tweede locatiecorrectie invoeren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="c7b0b-227">Selecteer in de taak **Correctie in** de locatie waarvoor u de voorraadcorrectie wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="c7b0b-228">Selecteer **LP-002** in het veld *LOC*.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="c7b0b-229">Bevestig de locatie.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-229">Confirm the location.</span></span>
1. <span data-ttu-id="c7b0b-230">Maak een nummerplaat-id voor het artikel dat aan de locatie wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="c7b0b-231">Voer in het veld **LP** de waarde *LP00201* in.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="c7b0b-232">Bevestig de nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="c7b0b-233">Voer het artikel in dat aan de nummerplaat wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="c7b0b-234">Voer in het veld **ITEM** de waarde *M9201* in.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="c7b0b-235">Bevestig het artikel.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-235">Confirm the item.</span></span>
1. <span data-ttu-id="c7b0b-236">Voer de hoeveelheid in van het artikel dat wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="c7b0b-237">Voer **15** in in het veld *Hoeveelheid*.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="c7b0b-238">Bevestig de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-238">Confirm the quantity.</span></span>

    <span data-ttu-id="c7b0b-239">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="c7b0b-240">Tik op de menuknop boven aan de pagina (ook wel aangeduid als de hamburger of de hamburgerknop) en selecteer **Annuleren** om de taak **Correctie in** af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="c7b0b-241">Locaties consolideren</span><span class="sxs-lookup"><span data-stu-id="c7b0b-241">Consolidate locations</span></span>

1. <span data-ttu-id="c7b0b-242">Ga naar **Magazijnbeheer \> Periodieke taken \> Artikelconsolidatie**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="c7b0b-243">Selecteer in de header een magazijn waarvoor u de consolidatie wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="c7b0b-244">Typ **51** in het veld *Magazijn*.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="c7b0b-245">Er wordt een record weergegeven voor elke locatie waar artikel *M9201* is gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="c7b0b-246">In de kolom **Gebruikspercentage** wordt de volumetrische capaciteit van elke locatie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="c7b0b-247">Als u de voorraad wilt consolideren, selecteert u alle locaties die moeten worden geconsolideerd en vervolgens selecteert u in het actievenster **Voorraad consolideren**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="c7b0b-248">Geef in het dialoogvenster **Voorraad consolideren** de locatie en het mutatietype op die moeten worden gebruikt om het werk voor de voorraadmutatie te maken.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="c7b0b-249">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="c7b0b-249">Set the following values:</span></span>

    - <span data-ttu-id="c7b0b-250">**Locatie:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="c7b0b-251">**Code mutatietype:** *CONSOLIDEREN*</span><span class="sxs-lookup"><span data-stu-id="c7b0b-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="c7b0b-252">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-252">Select **OK**.</span></span>
1. <span data-ttu-id="c7b0b-253">U ontvangt een informatieve melding de het mutatiewerk is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="c7b0b-254">Noteer de werk-id van de mutatie.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="c7b0b-255">Mutatiewerk weergeven</span><span class="sxs-lookup"><span data-stu-id="c7b0b-255">View movement work</span></span>

1. <span data-ttu-id="c7b0b-256">Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="c7b0b-257">Geef het werk weer dat is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-257">View the work that was created.</span></span> <span data-ttu-id="c7b0b-258">Gebruik de id van het mutatiewerk van de voorraadconsolidatie om het werkraster te filteren of te doorzoeken.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="c7b0b-259">In dit scenario wordt een bestaande locatie met voorraad gebruikt als de voorraadconsolidatielocatie.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="c7b0b-260">Er is daarom slechts één werk-id gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="c7b0b-261">Het systeem maakt voor elke verplaatsing één werk-id die moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="c7b0b-262">Als u een locatie opgeeft die al een voorraad bevat, wordt er slechts één werk-id gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="c7b0b-263">Als u een nieuwe locatie opgeeft, worden er twee werk-Id's gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c7b0b-263">If you specify a new location, two work IDs are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]