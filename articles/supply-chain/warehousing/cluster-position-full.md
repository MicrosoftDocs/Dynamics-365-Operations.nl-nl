---
title: Clusterpositie vol
description: Dit onderwerp bevat informatie over de functie Clusterpositie vol. Deze functie biedt een alternatief voor strengere handhaving van regels voor werkonderbrekingen wanneer clusterverzameling wordt gebruikt omdat hierdoor een grotere foutmarge mogelijk is in de volumetrische beperkingen van containers of totes.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b6a7cad070377de58d21a8eb91ee3e1ffaf1c660
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233002"
---
# <a name="cluster-position-full"></a><span data-ttu-id="4b977-104">Clusterpositie vol</span><span class="sxs-lookup"><span data-stu-id="4b977-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b977-105">De functie *Clusterpositie vol* biedt een alternatief voor strengere handhaving van regels voor werkonderbrekingen wanneer clusterverzameling wordt gebruikt omdat hierdoor een grotere foutmarge mogelijk is in de volumetrische beperkingen van containers of totes.</span><span class="sxs-lookup"><span data-stu-id="4b977-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="4b977-106">In een algemeen scenario passen niet alle items in een werkorder in een geselecteerde container.</span><span class="sxs-lookup"><span data-stu-id="4b977-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="4b977-107">Magazijnmedewerkers die een clusterverzameling maken, hebben niet veel opties in dit scenario: ze moeten een grotere containergrootte kiezen of met hun supervisor samenwerken om tot een andere oplossing te komen.</span><span class="sxs-lookup"><span data-stu-id="4b977-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="4b977-108">Deze functie introduceert de mogelijkheid om knop **Vol** uit te voeren voor een van de werkeenheden in een cluster.</span><span class="sxs-lookup"><span data-stu-id="4b977-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="4b977-109">In oudere versies was deze optie alleen beschikbaar voor reguliere orderverzameling, niet voor clusterverzamelingen.</span><span class="sxs-lookup"><span data-stu-id="4b977-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="4b977-110">Deze functie verschilt echter van de standaardknop **Vol** omdat het resterende werk wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="4b977-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="4b977-111">Er wordt niet voorgesteld dat de gebruiker nog een bak aan hetzelfde cluster toevoegt en er wordt niet automatisch nieuw werk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4b977-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="4b977-112">De functie Clusterpositie vol inschakelen</span><span class="sxs-lookup"><span data-stu-id="4b977-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="4b977-113">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="4b977-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="4b977-114">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="4b977-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="4b977-115">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="4b977-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="4b977-116">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="4b977-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4b977-117">**Functienaam:** *Clusterpositie vol*</span><span class="sxs-lookup"><span data-stu-id="4b977-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="4b977-118">Instelling</span><span class="sxs-lookup"><span data-stu-id="4b977-118">Setup</span></span>

<span data-ttu-id="4b977-119">Deze sectie bevat richtlijnen en een voorbeeld waarin wordt aangegeven hoe u de functie *Clusterpositie vol* instelt en gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4b977-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="4b977-120">Voorbeeldgegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="4b977-120">Make sample data available</span></span>

<span data-ttu-id="4b977-121">Als u het [voorbeeldscenario](#example-scenario) wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="4b977-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="4b977-122">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="4b977-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="4b977-123">U kunt het voorbeeldscenario ook gebruiken als instructie voor het gebruik van deze functie wanneer u met een productiesysteem werkt.</span><span class="sxs-lookup"><span data-stu-id="4b977-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="4b977-124">In dat geval moet u echter uw eigen waarden opgeven voor de instellingen die hier worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="4b977-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="4b977-125">Clusterprofielen</span><span class="sxs-lookup"><span data-stu-id="4b977-125">Cluster profiles</span></span>

<span data-ttu-id="4b977-126">U moet opgeven of cluster-Id's automatisch worden gegenereerd, hoeveel posities er worden gebruikt wanneer clusters worden uitgesplitst en hoe het orderverzamelingswerk wordt geordend en gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="4b977-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="4b977-127">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Clusterprofielen**.</span><span class="sxs-lookup"><span data-stu-id="4b977-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="4b977-128">Selecteer in het lijstvenster de record **Cluster maken**.</span><span class="sxs-lookup"><span data-stu-id="4b977-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="4b977-129">Verifieer op het sneltabblad **Algemeen** de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="4b977-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="4b977-130">**Cluster-id maken**: *Ja*</span><span class="sxs-lookup"><span data-stu-id="4b977-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="4b977-131">**Posities activeren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="4b977-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="4b977-132">**Aantal posities:** *2*</span><span class="sxs-lookup"><span data-stu-id="4b977-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="4b977-133">**Positienaam:** *Numeriek*</span><span class="sxs-lookup"><span data-stu-id="4b977-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="4b977-134">**Cluster opsplitsen bij**: *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="4b977-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="4b977-135">**Verificatietype sorteren:** *Positie scannen*</span><span class="sxs-lookup"><span data-stu-id="4b977-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="4b977-136">Op het sneltabblad **Cluster sorteren**.</span><span class="sxs-lookup"><span data-stu-id="4b977-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="4b977-137">Het raster moet leeg zijn (geen regels bevatten).</span><span class="sxs-lookup"><span data-stu-id="4b977-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="4b977-138">Werksjablonen</span><span class="sxs-lookup"><span data-stu-id="4b977-138">Work templates</span></span>

<span data-ttu-id="4b977-139">U moet opgeven hoe het verzamelwerk voor clusterverzameling wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4b977-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="4b977-140">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="4b977-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="4b977-141">Stel boven aan de pagina het veld **Werkordertype** in op *Verkooporders*.</span><span class="sxs-lookup"><span data-stu-id="4b977-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="4b977-142">Controleer of de volgende werksjablonen uit de voorbeeldgegevens worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4b977-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="4b977-143">Als deze niet beschikbaar zijn, kunt u het scenario niet voltooien.</span><span class="sxs-lookup"><span data-stu-id="4b977-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="4b977-144">61 SO Stage</span><span class="sxs-lookup"><span data-stu-id="4b977-144">61 SO Stage</span></span>
    - <span data-ttu-id="4b977-145">61 SO Cluster pick</span><span class="sxs-lookup"><span data-stu-id="4b977-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="4b977-146">Locatie-instructies</span><span class="sxs-lookup"><span data-stu-id="4b977-146">Location directives</span></span>

<span data-ttu-id="4b977-147">U moet opgeven waar artikelen worden verzameld en waar deze worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="4b977-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="4b977-148">Ga naar **Magazijnbeheer \> Instellen \> Locatie-instructies**.</span><span class="sxs-lookup"><span data-stu-id="4b977-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="4b977-149">Stel in de lijstkoptekst het veld **Werkordertype** in op *Verkooporders*.</span><span class="sxs-lookup"><span data-stu-id="4b977-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="4b977-150">Controleer of de volgende verkooporderinstructies uit de voorbeeldgegevens worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4b977-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="4b977-151">Als deze niet beschikbaar zijn, kunt u het scenario niet voltooien.</span><span class="sxs-lookup"><span data-stu-id="4b977-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="4b977-152">61 Cluster pick</span><span class="sxs-lookup"><span data-stu-id="4b977-152">61 Cluster pick</span></span>
    - <span data-ttu-id="4b977-153">61 SO Pick order</span><span class="sxs-lookup"><span data-stu-id="4b977-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="4b977-154">Menuopties voor mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="4b977-154">Mobile device menu items</span></span>

<span data-ttu-id="4b977-155">Configureer een menu-item voor een mobiel apparaat om bestaand werk te gebruiken dat wordt geleid door clusterverzameling.</span><span class="sxs-lookup"><span data-stu-id="4b977-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="4b977-156">U moet de parameter **Splitsing van werk toestaan** in het menu-item voor mobiele apparaten inschakelen en de werkklasse *VO verzamelen* moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4b977-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="4b977-157">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="4b977-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="4b977-158">Selecteer in het lijstvenster de record **Clusterverzameling maken**.</span><span class="sxs-lookup"><span data-stu-id="4b977-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="4b977-159">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4b977-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="4b977-160">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4b977-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4b977-161">**Gestuurd door:** *Clusterverzameling*</span><span class="sxs-lookup"><span data-stu-id="4b977-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="4b977-162">**Nummerplaat maken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="4b977-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="4b977-163">**Splitsing van werk toestaan:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="4b977-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="4b977-164">**Profiel-id van cluster:** *Cluster maken*</span><span class="sxs-lookup"><span data-stu-id="4b977-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="4b977-165">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="4b977-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="4b977-166">Voeg indien nodig de volgende twee regels toe op het sneltabblad **Werkklassen**:</span><span class="sxs-lookup"><span data-stu-id="4b977-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="4b977-167">Regel 1 (gewoonlijk aanwezig in voorbeeldgegevens):</span><span class="sxs-lookup"><span data-stu-id="4b977-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="4b977-168">**Werkklasse-id**: *Verkoop*</span><span class="sxs-lookup"><span data-stu-id="4b977-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="4b977-169">**Werkordertype:** *Verkooporders*</span><span class="sxs-lookup"><span data-stu-id="4b977-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="4b977-170">Regel 2 (waarschijnlijk niet aanwezig in voorbeeldgegevens):</span><span class="sxs-lookup"><span data-stu-id="4b977-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="4b977-171">**Werkklasse-id:** *VO verzamelen*</span><span class="sxs-lookup"><span data-stu-id="4b977-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="4b977-172">**Werkordertype:** *Verkooporders*</span><span class="sxs-lookup"><span data-stu-id="4b977-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="4b977-173">Ga naar **Werkbevestigingsinstellingen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4b977-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="4b977-174">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="4b977-174">Select **Edit**.</span></span>
1. <span data-ttu-id="4b977-175">Voer de volgende waarden op de regel in het raster in.</span><span class="sxs-lookup"><span data-stu-id="4b977-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="4b977-176">**Werktype** - *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="4b977-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="4b977-177">**Productbevestiging** - *Het selectievakje inschakelen*</span><span class="sxs-lookup"><span data-stu-id="4b977-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="4b977-178">Selecteer **Opslaan** in het actievenster en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4b977-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="4b977-179">Orderverzamelingswerk maken</span><span class="sxs-lookup"><span data-stu-id="4b977-179">Create picking work</span></span>

<span data-ttu-id="4b977-180">Voordat u kunt beginnen met clusterverzamelingen, moet u uitgaand werk maken.</span><span class="sxs-lookup"><span data-stu-id="4b977-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="4b977-181">Met het clusterprofiel dat u eerder hebt gemaakt, worden twee clusterposities opgegeven.</span><span class="sxs-lookup"><span data-stu-id="4b977-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="4b977-182">Daarom moet u minimaal twee werk-id's maken voor het orderverzamelen van verkooporders.</span><span class="sxs-lookup"><span data-stu-id="4b977-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="4b977-183">Voor dit scenario vinden transacties plaats in magazijn *61* en worden de artikelen *L0101* en *T0100* gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4b977-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="4b977-184">De voorbeeldgegevens moeten voldoende voorhanden voorraad van deze artikelen hebben.</span><span class="sxs-lookup"><span data-stu-id="4b977-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="4b977-185">Controleer of u voldoende voorraad hebt om de transacties te voltooien.</span><span class="sxs-lookup"><span data-stu-id="4b977-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="4b977-186">Verkooporder 1 maken</span><span class="sxs-lookup"><span data-stu-id="4b977-186">Create sales order 1</span></span>

1. <span data-ttu-id="4b977-187">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="4b977-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4b977-188">Selecteer **Nieuw** om verkooporder 1 te maken.</span><span class="sxs-lookup"><span data-stu-id="4b977-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="4b977-189">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4b977-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4b977-190">**Klantrekening:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="4b977-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="4b977-191">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="4b977-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4b977-192">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b977-192">Select **OK**.</span></span>
1. <span data-ttu-id="4b977-193">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="4b977-193">The new sales order is opened.</span></span> <span data-ttu-id="4b977-194">Voeg op het sneltabblad **Verkooporderregels** een regel toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="4b977-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="4b977-195">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4b977-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4b977-196">**Hoeveelheid:** *5*</span><span class="sxs-lookup"><span data-stu-id="4b977-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="4b977-197">Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Bevestigde leveringsdatum** in op de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="4b977-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="4b977-198">Voeg op het sneltabblad **Verkooporderregels** een tweede regel toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="4b977-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="4b977-199">**Artikelnummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="4b977-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="4b977-200">**Hoeveelheid:** *20*</span><span class="sxs-lookup"><span data-stu-id="4b977-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="4b977-201">Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Bevestigde leveringsdatum** in op de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="4b977-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="4b977-202">Volg voor elke regel die u zojuist hebt toegevoegd de volgende stappen om voorraad te reserveren:</span><span class="sxs-lookup"><span data-stu-id="4b977-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="4b977-203">Selecteer de regel die u wilt reserveren.</span><span class="sxs-lookup"><span data-stu-id="4b977-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="4b977-204">Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="4b977-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="4b977-205">Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.</span><span class="sxs-lookup"><span data-stu-id="4b977-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="4b977-206">Sluit de pagina **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="4b977-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="4b977-207">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="4b977-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4b977-208">Als de vrijgave is voltooid, ontvangt u een informatieve melding waarin de wave- en ladings-id's worden vermeld die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4b977-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="4b977-209">Verkooporder 2 maken</span><span class="sxs-lookup"><span data-stu-id="4b977-209">Create sales order 2</span></span>

1. <span data-ttu-id="4b977-210">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="4b977-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4b977-211">Selecteer **Nieuw** om verkooporder 2 te maken.</span><span class="sxs-lookup"><span data-stu-id="4b977-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="4b977-212">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4b977-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4b977-213">**Klantrekening:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="4b977-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="4b977-214">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="4b977-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4b977-215">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b977-215">Select **OK**.</span></span>
1. <span data-ttu-id="4b977-216">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="4b977-216">The new sales order is opened.</span></span> <span data-ttu-id="4b977-217">Voeg op het sneltabblad **Verkooporderregels** een regel toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="4b977-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="4b977-218">**Artikelnummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="4b977-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="4b977-219">**Hoeveelheid:** *20*</span><span class="sxs-lookup"><span data-stu-id="4b977-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="4b977-220">Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Bevestigde leveringsdatum** in op de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="4b977-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="4b977-221">Voeg op het sneltabblad **Verkooporderregels** een tweede regel toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="4b977-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="4b977-222">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4b977-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4b977-223">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="4b977-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="4b977-224">Stel op het sneltabblad **Regeldetails** op het tabblad **Levering** het veld **Bevestigde leveringsdatum** in op de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="4b977-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="4b977-225">Volg voor elke regel die u zojuist hebt toegevoegd de volgende stappen om voorraad te reserveren:</span><span class="sxs-lookup"><span data-stu-id="4b977-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="4b977-226">Selecteer de regel die u wilt reserveren.</span><span class="sxs-lookup"><span data-stu-id="4b977-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="4b977-227">Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="4b977-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="4b977-228">Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.</span><span class="sxs-lookup"><span data-stu-id="4b977-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="4b977-229">Sluit de pagina **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="4b977-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="4b977-230">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="4b977-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4b977-231">Als de vrijgave is voltooid, ontvangt u een informatieve melding waarin de wave- en ladings-id's worden vermeld die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4b977-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="4b977-232">Werk-id's en nummerplaatnummers ophalen</span><span class="sxs-lookup"><span data-stu-id="4b977-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="4b977-233">Er moeten twee werk-id's met elk twee pickregels zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4b977-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="4b977-234">Voer de volgende stappen uit om de toewijzingen van werk-id's en nummerplaten te vinden.</span><span class="sxs-lookup"><span data-stu-id="4b977-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="4b977-235">Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="4b977-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="4b977-236">Zoek in raster **Overzicht** de kolom **Ordernummer** voor de twee verkooporders die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4b977-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="4b977-237">Noteer voor elke verkooporder de bijbehorende werk-id.</span><span class="sxs-lookup"><span data-stu-id="4b977-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="4b977-238">Selecteer de rij voor elke verkooporder om gerelateerde informatie weer te geven in het raster **Regels**.</span><span class="sxs-lookup"><span data-stu-id="4b977-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="4b977-239">Noteer de locatie waar elk artikel wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="4b977-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="4b977-240">Ga naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden voorraad**.</span><span class="sxs-lookup"><span data-stu-id="4b977-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="4b977-241">Selecteer in het actievenster de optie **Dimensies** om het dialoogvenster **Weergave van dimensies** te openen.</span><span class="sxs-lookup"><span data-stu-id="4b977-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="4b977-242">Controleer of de selectievakjes **Nummerplaat**, **Magazijn** en **Artikelnummer** zijn ingeschakeld en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b977-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="4b977-243">Stel in het deelvenster **Filter** de volgende filters in:</span><span class="sxs-lookup"><span data-stu-id="4b977-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="4b977-244">**Artikelnummer** – **is één van** – *L0101* en *T100*</span><span class="sxs-lookup"><span data-stu-id="4b977-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="4b977-245">**Magazijn** – **begint met** – *61*</span><span class="sxs-lookup"><span data-stu-id="4b977-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="4b977-246">Noteer de weergegeven waarden voor **Nummerplaat**.</span><span class="sxs-lookup"><span data-stu-id="4b977-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="4b977-247">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="4b977-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="4b977-248">Uitvoering van stroom op mobiele apparaten - Werkbevestigingsinstellingen voor het product</span><span class="sxs-lookup"><span data-stu-id="4b977-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="4b977-249">Meld u aan bij de magazijnapp als een gebruiker in magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="4b977-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="4b977-250">Ga naar **Uitgaand \> Clusterverzameling maken**.</span><span class="sxs-lookup"><span data-stu-id="4b977-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="4b977-251">De pagina **TAAK: werk toewijzen aan cluster** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4b977-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="4b977-252">Voer de werk-id voor verkooporder 1 in om deze toe te wijzen aan clusterpositie 1.</span><span class="sxs-lookup"><span data-stu-id="4b977-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="4b977-253">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="4b977-254">Voer de werk-id voor verkooporder 2 in om deze toe te wijzen aan clusterpositie 2.</span><span class="sxs-lookup"><span data-stu-id="4b977-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="4b977-255">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="4b977-256">De pagina **TAAK: Clusterverzameling maken: Orderverzamelen** wordt weergegeven en bevat *Artikel L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="4b977-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="4b977-257">Omdat het clusterprofiel het aantal posities instelt op 2, leidt het systeem u automatisch naar de eerste consolidatieverzameling: twee pallets (PL) van artikel *L0101*.</span><span class="sxs-lookup"><span data-stu-id="4b977-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="4b977-258">Tijdens de volgende stappen kunt u op elk gewenst moment het tabblad **Details** selecteren om aanvullende informatie over de taak weer te geven, zoals de orderverzamellocatie.</span><span class="sxs-lookup"><span data-stu-id="4b977-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="4b977-259">Stel het veld **ARTIKEL** in op *L0101*.</span><span class="sxs-lookup"><span data-stu-id="4b977-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="4b977-260">Hiermee wordt het artikelnummer bevestigd dat vereist is voor deze menuopdracht (u hebt dit eerder geconfigureerd door **Werkbevestigingsinstellingen** te selecteren op de pagina **Menuopties voor mobiel apparaat** toen u deze menuopdracht maakte).</span><span class="sxs-lookup"><span data-stu-id="4b977-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="4b977-261">Voer het nummerplaatnummer dat is gekoppeld aan het artikel op de locatie dat wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="4b977-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="4b977-262">U verzamelt twee pallets.</span><span class="sxs-lookup"><span data-stu-id="4b977-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="4b977-263">Stel het veld **LP** in op *LP\_PICK\_01*.</span><span class="sxs-lookup"><span data-stu-id="4b977-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="4b977-264">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="4b977-265">De pagina **TAAK: Sorteren: Clusterverzameling maken** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4b977-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="4b977-266">Hier kunt u de twee verzamelde pallets in een orderverzamelingspositie sorteren.</span><span class="sxs-lookup"><span data-stu-id="4b977-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="4b977-267">Deze positie kan een tote of container zijn die wordt gebruikt om de verzamelde voorraad te scheiden op verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4b977-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="4b977-268">Bekijk de details die worden weergegeven voor het artikel (*L0101*) en aantal (*20* ea) dat wordt gesorteerd op positie 1 (voor verkooporder 1).</span><span class="sxs-lookup"><span data-stu-id="4b977-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="4b977-269">Stel het veld **POSITIE NA** in op *1*.</span><span class="sxs-lookup"><span data-stu-id="4b977-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="4b977-270">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="4b977-271">Bekijk de details die worden weergegeven voor het artikel (*L0101*) en aantal (*20* ea) dat wordt gesorteerd op positie 2 (voor verkooporder 2).</span><span class="sxs-lookup"><span data-stu-id="4b977-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="4b977-272">Stel het veld **POSITIE NA** in op *2*.</span><span class="sxs-lookup"><span data-stu-id="4b977-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="4b977-273">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="4b977-274">De pagina **TAAK: Clusterverzameling maken: Orderverzamelen** wordt weergegeven en bevat *Artikel L0100 7 ea*.</span><span class="sxs-lookup"><span data-stu-id="4b977-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="4b977-275">In dit scenario kan positie 1 niet de volledige hoeveelheid artikelen accepteren die moeten worden verzameld om verkooporder 1 af te handelen.</span><span class="sxs-lookup"><span data-stu-id="4b977-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="4b977-276">Een positie moet als volledig worden gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="4b977-276">A position must be marked as full.</span></span> <span data-ttu-id="4b977-277">In dit scenario verzamelt u het tweede artikel gedeeltelijk.</span><span class="sxs-lookup"><span data-stu-id="4b977-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="4b977-278">Het tweede artikel wordt gedeeltelijk verzameld voor positie 1 en er wordt nieuwe werk gemaakt om de resterende hoeveelheid te verzamelen om de order af te handelen.</span><span class="sxs-lookup"><span data-stu-id="4b977-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="4b977-279">Selecteer de menuknop boven aan de pagina (ook wel aangeduid als de hamburger of de hamburgerknop) en selecteer **Positie vol**.</span><span class="sxs-lookup"><span data-stu-id="4b977-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="4b977-280">Geef de positie aan die vol is en selecteer *1*.</span><span class="sxs-lookup"><span data-stu-id="4b977-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="4b977-281">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="4b977-282">Voer de orderverzamelhoeveelheid die nog kan worden verzameld in positie 1 in.</span><span class="sxs-lookup"><span data-stu-id="4b977-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="4b977-283">Het systeem kan bepalen welk artikelnummer wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="4b977-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="4b977-284">Voer *2* in.</span><span class="sxs-lookup"><span data-stu-id="4b977-284">Enter *2*.</span></span>
1. <span data-ttu-id="4b977-285">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="4b977-286">Bevestig het artikelnummer om de verzameling van het resterende artikel op positie 2 te voltooien.</span><span class="sxs-lookup"><span data-stu-id="4b977-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="4b977-287">Stel het veld **ARTIKEL** in op *T0100*.</span><span class="sxs-lookup"><span data-stu-id="4b977-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="4b977-288">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="4b977-289">Voer de nummerplaat in waarvan het artikel wordt verzameld door het veld **LP** in te stellen op *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="4b977-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="4b977-290">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="4b977-291">Bekijk de details die worden weergegeven voor het artikel (*T0100*) en aantal (*2* ea) dat wordt gesorteerd op positie 2 (voor verkooporder 2).</span><span class="sxs-lookup"><span data-stu-id="4b977-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="4b977-292">Stel het veld **POSITIE NA** in op *2*.</span><span class="sxs-lookup"><span data-stu-id="4b977-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="4b977-293">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="4b977-294">Bekijk de details die worden weergegeven voor het artikel (*T0100*) en aantal (*2* ea) dat wordt gesorteerd op positie 1 (voor verkooporder 1).</span><span class="sxs-lookup"><span data-stu-id="4b977-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="4b977-295">Stel het veld **POSITIE NA** in op *1*.</span><span class="sxs-lookup"><span data-stu-id="4b977-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="4b977-296">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="4b977-297">De pagina **TAAK: Clusterverzameling maken: Wegzetten** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4b977-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="4b977-298">In dit scenario is de clusterverzameling voltooid en wordt de gebruiker geïnstrueerd om de verzamelde artikelen van positie 1 en positie 2 weg te zetten op de faseringslocatie *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="4b977-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="4b977-299">Bekijk de gegevens op de pagina.</span><span class="sxs-lookup"><span data-stu-id="4b977-299">Review the information on the page.</span></span> <span data-ttu-id="4b977-300">Er wordt aangegeven dat het totale aantal van *44* wordt weggezet op de faseringslocatie.</span><span class="sxs-lookup"><span data-stu-id="4b977-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="4b977-301">Selecteer **OK** (symbool voor vinkje).</span><span class="sxs-lookup"><span data-stu-id="4b977-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="4b977-302">U ontvangt het bericht Cluster voltooid.</span><span class="sxs-lookup"><span data-stu-id="4b977-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="4b977-303">U kunt nu de menuoptie **Orderverzamelen** gebruiken om het resterende aantal te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="4b977-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="4b977-304">Vervolgens kunt u met de menuopdracht **Verkoop laden** de artikelen van de faseringslocatie naar het laaddok verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="4b977-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]