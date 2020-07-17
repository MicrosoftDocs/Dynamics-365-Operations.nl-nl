---
title: Productdimensies op locaties combineren
description: Dit onderwerp biedt informatie over het combineren van productdimensies op locaties. Deze functionaliteit voor locatieprofielen helpt het locatiebeheer te verbeteren wanneer productvarianten of producten met dimensies worden gebruikt, zoals in de kledingsector. Hiermee kunt u bepalen of configuraties, kleuren, stijlen en formaat kunnen worden gecombineerd voor een bepaald locatieprofiel, of dat een van deze dimensies of een combinatie van deze dimensies op dezelfde locatie kan worden geplaatst.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 968777b918d59b810a189139fbf4d6fee1b5d3f5
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529978"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="37451-105">Productdimensies op locaties combineren</span><span class="sxs-lookup"><span data-stu-id="37451-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37451-106">Productdimensies op locaties combineren is functionaliteit voor locatieprofielen die helpt het locatiebeheer te verbeteren wanneer productvarianten of producten met dimensies worden gebruikt, zoals in de kledingsector.</span><span class="sxs-lookup"><span data-stu-id="37451-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="37451-107">Hiermee kunt u bepalen of configuraties, kleuren, stijlen en formaat kunnen worden gecombineerd voor een bepaald locatieprofiel, of dat een van deze dimensies of een combinatie van deze dimensies op dezelfde locatie kan worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="37451-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="37451-108">De functie voor het combineren van productdimensies op locaties inschakelen</span><span class="sxs-lookup"><span data-stu-id="37451-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="37451-109">Voordat u de functie Combineren van productdimensies op locaties kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="37451-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="37451-110">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="37451-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="37451-111">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="37451-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="37451-112">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="37451-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="37451-113">**Functienaam:** *Combineren van productdimensies op locaties*</span><span class="sxs-lookup"><span data-stu-id="37451-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="37451-114">Instellen</span><span class="sxs-lookup"><span data-stu-id="37451-114">Setup</span></span>

<span data-ttu-id="37451-115">Aan elke locatie in het magazijn moet een locatieprofiel zijn gekoppeld, dat de eigenschappen beschrijft van de locatie.</span><span class="sxs-lookup"><span data-stu-id="37451-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="37451-116">Dit betekent dat alle locaties die hetzelfde locatieprofiel gebruiken, de productdimensie kunnen combineren nadat deze is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="37451-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="37451-117">Locatieprofielen configureren om combinaties van productdimensies toe te staan</span><span class="sxs-lookup"><span data-stu-id="37451-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="37451-118">Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.</span><span class="sxs-lookup"><span data-stu-id="37451-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="37451-119">Selecteer in de lijst met locatieprofielen de waarde **BULK**.</span><span class="sxs-lookup"><span data-stu-id="37451-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="37451-120">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="37451-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="37451-121">Stel op het sneltabblad **Algemeen** de optie **Productdimensie-specifiek combineren op locatie inschakelen** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="37451-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="37451-122">U kunt deze optie alleen op *Ja* instellen als de optie **Gemengde artikelen toestaan** is ingesteld op *Nee*.</span><span class="sxs-lookup"><span data-stu-id="37451-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="37451-123">Stel op het sneltabblad **Toegestane productdimensiecombinaties** de optie **Formaat** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="37451-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="37451-124">In het scenario dat in dit onderwerp wordt beschreven, kan combineren alleen worden uitgevoerd voor producten met een verschillende dimensies voor **Formaat**.</span><span class="sxs-lookup"><span data-stu-id="37451-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="37451-125">Er zijn echter ook andere opties beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="37451-125">However, other options are also available.</span></span>
1. <span data-ttu-id="37451-126">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="37451-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="37451-127">Een nieuw productmodel en productvarianten maken</span><span class="sxs-lookup"><span data-stu-id="37451-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="37451-128">Ga naar **Productgegevensbeheer \> Producten \> Productmodellen**.</span><span class="sxs-lookup"><span data-stu-id="37451-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="37451-129">Selecteer in het actievenster **Nieuw** om een productmodel te maken.</span><span class="sxs-lookup"><span data-stu-id="37451-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="37451-130">Stel in het dialoogvenster **Nieuw product** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="37451-131">**Producttype:** *Artikel*</span><span class="sxs-lookup"><span data-stu-id="37451-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="37451-132">**Subtype van product:** *Productmodel*</span><span class="sxs-lookup"><span data-stu-id="37451-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="37451-133">**Productnummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="37451-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="37451-134">**Productnaam:** *B0001 Formaat*</span><span class="sxs-lookup"><span data-stu-id="37451-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="37451-135">**Productdimensiegroep:** *Formaat*</span><span class="sxs-lookup"><span data-stu-id="37451-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="37451-136">**Configuratietechnologie:** *Vooraf gedefinieerde variant*</span><span class="sxs-lookup"><span data-stu-id="37451-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="37451-137">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="37451-137">Select **OK**.</span></span>
1. <span data-ttu-id="37451-138">Stel op de pagina **Productgegevens** op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="37451-139">**Varianten automatisch genereren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="37451-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="37451-140">**Formaatgroep:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="37451-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="37451-141">Als u de vooraf gedefinieerde varianten wilt weergeven, selecteert u in het actievenster **Productvarianten**.</span><span class="sxs-lookup"><span data-stu-id="37451-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="37451-142">De pagina **Productvarianten** wordt geopend met een lijst met varianten uit de configuratie van de groep Formaat.</span><span class="sxs-lookup"><span data-stu-id="37451-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="37451-143">Producten vrijgeven aan het bedrijf USMF</span><span class="sxs-lookup"><span data-stu-id="37451-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="37451-144">Selecteer in het actievenster **Producten vrijgeven**.</span><span class="sxs-lookup"><span data-stu-id="37451-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="37451-145">Controleer op de pagina **Producten voor vrijgave selecteren** of het productnummer *B0001* in de lijst staat en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="37451-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="37451-146">Selecteer **Volgende** om de productvarianten te bevestigen die u wilt vrijgeven.</span><span class="sxs-lookup"><span data-stu-id="37451-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="37451-147">Selecteer op de pagina **Bedrijven selecteren waarnaar wordt vrijgegeven** de optie *USMF* en selecteer **Volgende** om de selectie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="37451-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="37451-148">Selecteer op de pagina **Selectie bevestigen** de optie **Voltooien** om de release te voltooien.</span><span class="sxs-lookup"><span data-stu-id="37451-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="37451-149">De melding "Bewerking voltooid" wordt getoond.</span><span class="sxs-lookup"><span data-stu-id="37451-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="37451-150">Een vrijgegeven product in het bedrijf USMF bijwerken</span><span class="sxs-lookup"><span data-stu-id="37451-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="37451-151">Zorg ervoor dat u bent aangemeld bij het bedrijf **USMF**.</span><span class="sxs-lookup"><span data-stu-id="37451-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="37451-152">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten** om het aanmaken van het vrijgegeven product af te ronden.</span><span class="sxs-lookup"><span data-stu-id="37451-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="37451-153">Zoek en selecteer het artikelnummer *B0001* om de pagina **Details van vrijgegeven product** te openen.</span><span class="sxs-lookup"><span data-stu-id="37451-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="37451-154">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="37451-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="37451-155">Controleer op het sneltabblad **Algemeen** of het veld **Artikelmodelgroep** is ingesteld op *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="37451-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="37451-156">Selecteer in het Actievenster op het tabblad **Product** in de groep **Instellen** de optie **Dimensiegroepen**.</span><span class="sxs-lookup"><span data-stu-id="37451-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="37451-157">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-157">Set the following values:</span></span>

    - <span data-ttu-id="37451-158">**Opslagdimensiegroep:** *Artikelen*</span><span class="sxs-lookup"><span data-stu-id="37451-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="37451-159">**Traceringsdimensiegroep:** *Geen*</span><span class="sxs-lookup"><span data-stu-id="37451-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="37451-160">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="37451-160">Select **OK**.</span></span>
1. <span data-ttu-id="37451-161">Selecteer in het Actievenster op het tabblad **Product** in de groep **Instellen** de optie **Reserveringshiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="37451-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="37451-162">Stel het veld **Reserveringshiërarchie** in op *Standaard* en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="37451-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="37451-163">Op het sneltabblad **Algemeen** in de sectie **Beheer** ziet u dat de selecties zijn bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="37451-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="37451-164">Ga naar het sneltabblad **Inkopen** en voer in het veld **Prijs** de waarde *10* in.</span><span class="sxs-lookup"><span data-stu-id="37451-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="37451-165">Voer op het sneltabblad **Kosten beheren** in het veld **Artikelgroep** de waarde *Audio* in.</span><span class="sxs-lookup"><span data-stu-id="37451-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="37451-166">Ga naar het sneltabblad **Inkopen** en voer in het veld **Prijs** de waarde *10* in.</span><span class="sxs-lookup"><span data-stu-id="37451-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="37451-167">Geef op het sneltabblad **Magazijn** in het veld **Eenheidvolgordegroep-id** de waarde *ea* op.</span><span class="sxs-lookup"><span data-stu-id="37451-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="37451-168">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="37451-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="37451-169">Maak een locatie-richtlijn.</span><span class="sxs-lookup"><span data-stu-id="37451-169">Create a location directive</span></span>

1. <span data-ttu-id="37451-170">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="37451-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="37451-171">Selecteer in het linkerdeelvenster in het veld **Werkordertype** de waarde *Inkooporders*.</span><span class="sxs-lookup"><span data-stu-id="37451-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="37451-172">Selecteer in de lijst de locatie-instructie met de naam *24 PO Direct*.</span><span class="sxs-lookup"><span data-stu-id="37451-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="37451-173">Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="37451-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="37451-174">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="37451-175">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="37451-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="37451-176">De nieuwe regel moet vóór de eerder bestaande regel staan.</span><span class="sxs-lookup"><span data-stu-id="37451-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="37451-177">Om de posities te wijzigen, gebruikt u de knoppen **Omhoog** en **Omlaag** op de werk balk, of u wijzigt de waarde van het **volgnummer** van de bestaande regel in *2*.</span><span class="sxs-lookup"><span data-stu-id="37451-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="37451-178">**Naam:** *Locatieprofiel wegzetten naar BULK*</span><span class="sxs-lookup"><span data-stu-id="37451-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="37451-179">**Gebruik vaste locaties:** *Vaste en niet-vaste locaties*</span><span class="sxs-lookup"><span data-stu-id="37451-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="37451-180">**Negatieve voorraad toestaan:** *Schakel dit selectievakje uit (= Nee)*</span><span class="sxs-lookup"><span data-stu-id="37451-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="37451-181">**Batch ingeschakeld:** *Schakel dit selectievakje uit (= Nee)*</span><span class="sxs-lookup"><span data-stu-id="37451-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="37451-182">**Strategie:** *Geen*</span><span class="sxs-lookup"><span data-stu-id="37451-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="37451-183">Selecteer de optie **Query bewerken** boven het raster terwijl de nieuwe regel nog steeds is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="37451-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="37451-184">Selecteer in het querydialoogvenster op het tabblad **Bereik** de optie **Toevoegen** om een regel aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="37451-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="37451-185">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="37451-186">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="37451-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="37451-187">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="37451-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="37451-188">**Veld:** *Locatieprofiel-id*</span><span class="sxs-lookup"><span data-stu-id="37451-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="37451-189">**Criteria:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="37451-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="37451-190">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="37451-190">Select **OK**.</span></span>
1. <span data-ttu-id="37451-191">Selecteer in het actievenster op de pagina **Locatie-instructies** **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="37451-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="37451-192">Ga naar het sneltabblad **Locatie-instructieactie**. Als u in het veld **Strategie** de locatiestrategie *Samenvoegen* gebruikt, wordt de configuratie van het snelttabblad **Toegestane productdimensiecombinaties** in de **Locatieprofielen** overschreven. Artikelen worden dan weggezet op dezelfde locatie, ook als dit gedrag niet is toegestaan volgens de configuratie.</span><span class="sxs-lookup"><span data-stu-id="37451-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="37451-193">Een menuopdracht van mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="37451-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="37451-194">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="37451-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="37451-195">Selecteer in het actievenster de optie **Nieuw** om een menuoptie te maken dat u wilt gebruiken voor sorteren.</span><span class="sxs-lookup"><span data-stu-id="37451-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="37451-196">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="37451-197">**Menuoptie:** *IO-regel ontvangst*</span><span class="sxs-lookup"><span data-stu-id="37451-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="37451-198">**Titel:** *IO-regel ontvangst*</span><span class="sxs-lookup"><span data-stu-id="37451-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="37451-199">**Modus:** *werk*</span><span class="sxs-lookup"><span data-stu-id="37451-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="37451-200">**Bestaand werk gebruiken:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="37451-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="37451-201">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="37451-202">**Proces van werkaanmaak:** *Ontvangen en wegzetten van inkooporderregel*</span><span class="sxs-lookup"><span data-stu-id="37451-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="37451-203">**Nummerplaat maken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="37451-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="37451-204">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="37451-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="37451-205">Het menu voor het mobiele apparaat configureren</span><span class="sxs-lookup"><span data-stu-id="37451-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="37451-206">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="37451-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="37451-207">Selecteer in de lijst met menu's de waarde **Inkomend**.</span><span class="sxs-lookup"><span data-stu-id="37451-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="37451-208">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="37451-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="37451-209">Zoek en selecteer in de lijst **Beschikbare menu's en menuopdrachten** de menuopdracht **IO-regel ontvangst**.</span><span class="sxs-lookup"><span data-stu-id="37451-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="37451-210">Selecteer de knop pijl-rechts om de menu opdracht **IO-regel ontvangst** te verplaatsen naar de **lijst Menustructuur**.</span><span class="sxs-lookup"><span data-stu-id="37451-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="37451-211">Op deze manier voegt u de nieuwe menuopdracht toe aan het geselecteerde menu.</span><span class="sxs-lookup"><span data-stu-id="37451-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="37451-212">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="37451-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="37451-213">Scenario's</span><span class="sxs-lookup"><span data-stu-id="37451-213">Scenario</span></span>

<span data-ttu-id="37451-214">In dit demoscenario wordt weergegeven hoe twee verschillende productvarianten op dezelfde locatie kunnen worden geplaatst, wanneer het locatieprofiel gecombineerde artikelen niet toestaat, maar de functie *Productdimensies op locaties combineren* is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="37451-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="37451-215">In dit geval gebruikt u de variant **Formaat** als criterium.</span><span class="sxs-lookup"><span data-stu-id="37451-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="37451-216">Voordat u begint, moet u controleren of er lege locaties in magazijn *24* zijn die gebruikmaken van het locatieprofiel *BULK*.</span><span class="sxs-lookup"><span data-stu-id="37451-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="37451-217">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="37451-217">Create a purchase order</span></span>

<span data-ttu-id="37451-218">U maakt een inkoop order met drie regels: twee regels voor hetzelfde productnummer , maar met verschillende varianten voor **Formaat** en een derde regel voor een ander product zonder varianten.</span><span class="sxs-lookup"><span data-stu-id="37451-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="37451-219">Ga naar **Leveranciers \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="37451-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="37451-220">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="37451-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="37451-221">Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="37451-222">**Leverancieraccount:** *1001*</span><span class="sxs-lookup"><span data-stu-id="37451-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="37451-223">**Magazijn:** *24*</span><span class="sxs-lookup"><span data-stu-id="37451-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="37451-224">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="37451-224">Select **OK**.</span></span>
1. <span data-ttu-id="37451-225">De inkooporder wordt gemaakt en er wordt een nieuwe regel toegevoegd op het sneltabblad **Inkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="37451-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="37451-226">Noteer het nummer van de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="37451-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="37451-227">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="37451-228">**Artikelnummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="37451-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="37451-229">**Formaat:** *L*</span><span class="sxs-lookup"><span data-stu-id="37451-229">**Size** *L*</span></span>
    - <span data-ttu-id="37451-230">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="37451-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="37451-231">Selecteer **Regel toevoegen** boven het raster om een tweede inkooporderregel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="37451-232">**Artikelnummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="37451-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="37451-233">**Formaat:** *XL*</span><span class="sxs-lookup"><span data-stu-id="37451-233">**Size** *XL*</span></span>
    - <span data-ttu-id="37451-234">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="37451-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="37451-235">Selecteer **Regel toevoegen** boven het raster om een derde inkooporderregel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="37451-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="37451-236">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="37451-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="37451-237">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="37451-237">**Quantity:** *1*</span></span>

<span data-ttu-id="37451-238">9. Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="37451-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="37451-239">Inkooporderregels ontvangen in de magazijnapp</span><span class="sxs-lookup"><span data-stu-id="37451-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="37451-240">Meld u aan bij de magazijnapp als een gebruiker die toegang heeft tot magazijn *24*.</span><span class="sxs-lookup"><span data-stu-id="37451-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="37451-241">Selecteer het menu **Inkomend**.</span><span class="sxs-lookup"><span data-stu-id="37451-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="37451-242">Selecteer **IO-regel ontvangst**.</span><span class="sxs-lookup"><span data-stu-id="37451-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="37451-243">Selecteer het veld **PONUM** en voer vervolgens het inkoopordernummer in.</span><span class="sxs-lookup"><span data-stu-id="37451-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="37451-244">Bevestig uw invoer door te tikken op de knop Bevestigen (✔) onderaan de pagina.</span><span class="sxs-lookup"><span data-stu-id="37451-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="37451-245">Voer het regelnummer in van de inkooporder die u ontvangt.</span><span class="sxs-lookup"><span data-stu-id="37451-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="37451-246">Selecteer het veld **LINENUM** en voer vervolgens *1* in door middel van het cijfertoetsenblok.</span><span class="sxs-lookup"><span data-stu-id="37451-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="37451-247">Bevestig uw invoer.</span><span class="sxs-lookup"><span data-stu-id="37451-247">Confirm your entry.</span></span>
1. <span data-ttu-id="37451-248">Voer de hoeveelheid in die u ontvangt.</span><span class="sxs-lookup"><span data-stu-id="37451-248">Enter the quantity to receive.</span></span> <span data-ttu-id="37451-249">Selecteer de knop met het plusteken (**+**) twee keer om de waarde in het veld **Hoeveelheid** te verhogen naar *2*.</span><span class="sxs-lookup"><span data-stu-id="37451-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="37451-250">Registreer uw invoer door te tikken de knop (✔) onderaan de pagina en bevestig de invoer door opnieuw op de knop (✔) te tikken.</span><span class="sxs-lookup"><span data-stu-id="37451-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="37451-251">Bekijk de informatie op de pagina **Inkooporders: wegzetten**.</span><span class="sxs-lookup"><span data-stu-id="37451-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="37451-252">Op deze pagina wordt het werk weergegeven dat is gemaakt voor het wegzetten (Werk 1).</span><span class="sxs-lookup"><span data-stu-id="37451-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="37451-253">De locatie waar het ontvangen artikel wordt opgeslagen, de nummerplaat, het artikel, het formaat en de hoeveelheid van de taak **IO-order ontvangst** die u zojuist hebt voltooid, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="37451-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="37451-254">Bevestig het wegzetwerk.</span><span class="sxs-lookup"><span data-stu-id="37451-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="37451-255">Herhaal stappen 4 tot en met 11 voor inkooporderregel 2.</span><span class="sxs-lookup"><span data-stu-id="37451-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="37451-256">Geef echter in stap 8 als hoeveelheid *1* op.</span><span class="sxs-lookup"><span data-stu-id="37451-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="37451-257">Nieuw wegzetwerk (Werk 2) wordt gemaakt voor dezelfde locatie als Werk 1.</span><span class="sxs-lookup"><span data-stu-id="37451-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="37451-258">Herhaal stappen 4 tot en met 11 opnieuw voor inkooporderregel 2.</span><span class="sxs-lookup"><span data-stu-id="37451-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="37451-259">Geef echter in stap 8 als resterende hoeveelheid *1* op.</span><span class="sxs-lookup"><span data-stu-id="37451-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="37451-260">Nieuw wegzetwerk (Werk 3) wordt gemaakt voor dezelfde locatie als Werk 1 en Werk 2.</span><span class="sxs-lookup"><span data-stu-id="37451-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="37451-261">Dit gedrag treedt op omdat de locatie-instructiestrategie *Samenvoegen* wordt gebruikt en het sneltabblad **Toegestane productdimensiecombinaties** in de instellingen van de *Bulk*-**locatieprofielen** toestaat dat de variant **Formaat** op een locatie wordt gecombineerd.</span><span class="sxs-lookup"><span data-stu-id="37451-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="37451-262">Herhaal stappen 4 tot en met 11 voor inkooporderregel 3.</span><span class="sxs-lookup"><span data-stu-id="37451-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="37451-263">Geef in stap 8 als hoeveelheid *1* op voor artikel nummer *A0001*.</span><span class="sxs-lookup"><span data-stu-id="37451-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="37451-264">Nieuw wegzetwerk (Werk 4) worden gemaakt voor een andere locatie dan de locatie die wordt gebruikt voor inkooporderregels 1 en 2.</span><span class="sxs-lookup"><span data-stu-id="37451-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="37451-265">Dit gedrag treedt op omdat het locatieprofiel niet toestaat dat producten worden gecombineerd, maar wel toestaat dat verschillende dimensies van hetzelfde productmodel worden gecombineerd.</span><span class="sxs-lookup"><span data-stu-id="37451-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="37451-266">Tik op de menuknop boven aan de pagina (ook wel aangeduid als de hamburger of de hamburgerknop) en selecteer **Annuleren** om **IO-regel ontvangst** af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="37451-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="37451-267">U kunt dit scenario herhalen. Stel deze keer **Formaat** - *Nee* in op het sneltabblad **Toegestane productdimensiecombinaties** op de *BULK*-**locatieprofielen**, zodat geen van de productdimensies kunnen worden gecombineerd.</span><span class="sxs-lookup"><span data-stu-id="37451-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="37451-268">Wanneer u de inkooporder ontvangt, wordt in dit geval elke productvariant op een nieuwe locatie geplaatst.</span><span class="sxs-lookup"><span data-stu-id="37451-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>