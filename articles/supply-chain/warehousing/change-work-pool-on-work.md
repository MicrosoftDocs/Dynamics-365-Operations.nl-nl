---
title: Werkgroep voor werk wijzigen
description: In dit onderwerp wordt uitgelegd hoe u de knop Werkpool wijzigen kunt gebruiken voor werkitems om de werkpool van bestaande werkzaamheden te wijzigen.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001144"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="026f2-103">Werkgroep voor werk wijzigen</span><span class="sxs-lookup"><span data-stu-id="026f2-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="026f2-104">U kunt werkpools gebruiken om werk in groepen te organiseren.</span><span class="sxs-lookup"><span data-stu-id="026f2-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="026f2-105">U kunt bijvoorbeeld, een werkpool maken om werk te classificeren dat zich in een specifieke magazijnlocatie voordoet.</span><span class="sxs-lookup"><span data-stu-id="026f2-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="026f2-106">Met de functie *Werkpool voor werk wijzigen* wordt een knop **Werkpool wijzigen** toegevoegd aan het actievenster voor werkitems.</span><span class="sxs-lookup"><span data-stu-id="026f2-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="026f2-107">Daarom kunnen magazijnmanagers de werkpool van bestaand werk eenvoudig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="026f2-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="026f2-108">Met deze functie reageert de manager snel op wijzigingen op de werkvloer in het magazijn en kunnen ze beter aanpassen aan veranderende situaties en de noodzaak om werk over te brengen naar een andere werkpool.</span><span class="sxs-lookup"><span data-stu-id="026f2-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="026f2-109">Schakel de functie Werkpool voor werk wijzigen in</span><span class="sxs-lookup"><span data-stu-id="026f2-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="026f2-110">Voordat u deze functie gaat instellen of gebruiken, moet u controleren of deze beschikbaar is in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="026f2-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="026f2-111">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="026f2-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="026f2-112">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="026f2-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="026f2-113">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="026f2-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="026f2-114">**Functienaam:** *Werkpool voor werk wijzigen*</span><span class="sxs-lookup"><span data-stu-id="026f2-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="026f2-115">De functie Werkpool voor werk wijzigen instellen</span><span class="sxs-lookup"><span data-stu-id="026f2-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="026f2-116">Als u deze functie wilt gebruiken, moeten sommige werkpools zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="026f2-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="026f2-117">U kunt ook uw werksjablonen instellen zodat deze automatisch een pool toewijzen.</span><span class="sxs-lookup"><span data-stu-id="026f2-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="026f2-118">Als u het voorbeeldscenario wilt doorlopen dat verderop in dit onderwerp wordt beschreven, stelt u uw systeem in zoals in deze sectie wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="026f2-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="026f2-119">Werkpools instellen</span><span class="sxs-lookup"><span data-stu-id="026f2-119">Set up work pools</span></span>

<span data-ttu-id="026f2-120">Met werk pools kunt u werkitems op type ordenen.</span><span class="sxs-lookup"><span data-stu-id="026f2-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="026f2-121">Als u wilt werken met de functie *Werkpool voor werk wijzigen*, moeten er minimaal twee werkpools beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="026f2-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="026f2-122">Voer de volgende stappen uit om werkpools weer te geven en toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="026f2-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="026f2-123">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkpools**.</span><span class="sxs-lookup"><span data-stu-id="026f2-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="026f2-124">Als u werkt met demogegevens uit het **USMF**-bedrijf en het voorbeeldscenario verderop in dit onderwerp doorloopt, voegt u twee werkpools toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="026f2-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="026f2-125">Werkpool 1:</span><span class="sxs-lookup"><span data-stu-id="026f2-125">Work pool 1:</span></span>

        - <span data-ttu-id="026f2-126">**Werkpool-id:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="026f2-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="026f2-127">**Omschrijving:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="026f2-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="026f2-128">Werkpool 2:</span><span class="sxs-lookup"><span data-stu-id="026f2-128">Work pool 2:</span></span>

        - <span data-ttu-id="026f2-129">**Werkpool-id:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="026f2-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="026f2-130">**Omschrijving:** *Callcenter*</span><span class="sxs-lookup"><span data-stu-id="026f2-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="026f2-131">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="026f2-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="026f2-132">Werksjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="026f2-132">Set up work templates</span></span>

<span data-ttu-id="026f2-133">Voor elk van uw werksjablonen kunt u een standaard werkpool instellen.</span><span class="sxs-lookup"><span data-stu-id="026f2-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="026f2-134">Voor elke relevante sjabloon wijst u een werkpool toe in de kolom **Werkpool-id**.</span><span class="sxs-lookup"><span data-stu-id="026f2-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="026f2-135">In dit geval nemen alle werkitems die met behulp van een bepaalde sjabloon worden gegenereerd, automatisch de toegewezen werkpool over.</span><span class="sxs-lookup"><span data-stu-id="026f2-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="026f2-136">Als u werkt met de demogegevens uit het **USMF**-bedrijf en het voorbeeldscenario verderop in dit onderwerp doorloopt, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="026f2-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="026f2-137">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="026f2-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="026f2-138">Selecteer in het actievenster de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.</span><span class="sxs-lookup"><span data-stu-id="026f2-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="026f2-139">U bewerkt de sjabloon door de volgende waarden in te stellen:</span><span class="sxs-lookup"><span data-stu-id="026f2-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="026f2-140">**Werksjabloon:** *62 Orderverzamelen voor inpakken*</span><span class="sxs-lookup"><span data-stu-id="026f2-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="026f2-141">**Werkpool-id:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="026f2-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="026f2-142">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="026f2-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="026f2-143">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="026f2-143">Example scenario</span></span>

<span data-ttu-id="026f2-144">In dit scenario ziet u hoe u de verwerkingsstroom van een bestaand werk item kunt wijzigen door de werkpool te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="026f2-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="026f2-145">Het gebruikt demogegevens uit het **USMF**-bedrijf en de instellingen die eerder in dit onderwerp zijn voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="026f2-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="026f2-146">Een verkooporder maken en vrijgeven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="026f2-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="026f2-147">Controleer of er voldoende voorhanden voorraad is voor artikelen *A0001* en *A0002* in magazijn *62*.</span><span class="sxs-lookup"><span data-stu-id="026f2-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="026f2-148">Ga naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden lijst** en bewerk de filters zoals hier wordt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="026f2-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="026f2-149">De waarde **Magazijn** begint met *62*.</span><span class="sxs-lookup"><span data-stu-id="026f2-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="026f2-150">De waarde **Artikelnummer** is *A001* of *A002*.</span><span class="sxs-lookup"><span data-stu-id="026f2-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="026f2-151">De voorbeeldgegevens moeten een hoeveelheid van 10 voor elk bevatten.</span><span class="sxs-lookup"><span data-stu-id="026f2-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="026f2-152">Vervolgens moet u een verkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="026f2-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="026f2-153">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="026f2-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="026f2-154">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="026f2-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="026f2-155">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="026f2-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="026f2-156">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="026f2-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="026f2-157">**Magazijn:** *62*</span><span class="sxs-lookup"><span data-stu-id="026f2-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="026f2-158">Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="026f2-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="026f2-159">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="026f2-159">The new sales order is opened.</span></span> <span data-ttu-id="026f2-160">Deze moet een nieuwe, lege regel bevatten in het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="026f2-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="026f2-161">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="026f2-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="026f2-162">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="026f2-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="026f2-163">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="026f2-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="026f2-164">Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="026f2-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="026f2-165">Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.</span><span class="sxs-lookup"><span data-stu-id="026f2-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="026f2-166">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="026f2-166">Close the page.</span></span>
1. <span data-ttu-id="026f2-167">Selecteer op het sneltabblad **Verkooporderregels** de optie **Regel toevoegen** om nog een regel toe te voegen aan uw verkooporder.</span><span class="sxs-lookup"><span data-stu-id="026f2-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="026f2-168">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="026f2-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="026f2-169">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="026f2-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="026f2-170">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="026f2-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="026f2-171">Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="026f2-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="026f2-172">Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren.</span><span class="sxs-lookup"><span data-stu-id="026f2-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="026f2-173">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="026f2-173">Close the page.</span></span>
1. <span data-ttu-id="026f2-174">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="026f2-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="026f2-175">U ontvangt een informatieve melding waarin de wave-id en zendings-id worden vermeld die zijn gemaakt door het vrijgeven.</span><span class="sxs-lookup"><span data-stu-id="026f2-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="026f2-176">Noteer de wave-id.</span><span class="sxs-lookup"><span data-stu-id="026f2-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="026f2-177">De uitgaande wave controleren</span><span class="sxs-lookup"><span data-stu-id="026f2-177">Review the outbound wave</span></span>

1. <span data-ttu-id="026f2-178">Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.</span><span class="sxs-lookup"><span data-stu-id="026f2-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="026f2-179">Zoek in het raster naar de wave-id die is gemaakt op basis van de vrijgegeven verkooporder.</span><span class="sxs-lookup"><span data-stu-id="026f2-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="026f2-180">Selecteer de wave-id om de details weer te geven.</span><span class="sxs-lookup"><span data-stu-id="026f2-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="026f2-181">Controleer op het sneltabblad **Waveregels** of er een zending-id voor de verkooporder wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="026f2-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="026f2-182">Als de optie **Wave verwerken bij vrijgave door magazijn** is ingesteld op *Nee* in de instellingen voor de wavesjabloon van de zending, moet u de wave handmatig verwerken door **Verwerken** te selecteren op het tabblad **Wave** in het actievenster om werk te maken.</span><span class="sxs-lookup"><span data-stu-id="026f2-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="026f2-183">Controleer of de wave is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="026f2-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="026f2-184">Met deze verwerking wordt het vereiste werk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="026f2-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="026f2-185">Gegevens van werk weergeven en de werkpool wijzigen</span><span class="sxs-lookup"><span data-stu-id="026f2-185">View work details and change the work pool</span></span>

<span data-ttu-id="026f2-186">U kunt de pagina **Werkdetails** gebruiken om het werk weer te geven dat is gemaakt en om de werkpool te beheren.</span><span class="sxs-lookup"><span data-stu-id="026f2-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="026f2-187">Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="026f2-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="026f2-188">Selecteer de rij voor het werk dat u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="026f2-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="026f2-189">In de kolom **Ordernummer** wordt het verkoopordernummer weergegeven.</span><span class="sxs-lookup"><span data-stu-id="026f2-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="026f2-190">Het veld **Werkpool-id** wordt ingesteld op de werkpool-id die is ingesteld in de werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="026f2-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="026f2-191">Als u het veld **Werkpool-id** niet ziet, voegt u de kolom toe aan het raster en vernieuwt u de pagina.</span><span class="sxs-lookup"><span data-stu-id="026f2-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="026f2-192">Als u de werkpool wilt wijzigen die aan de werk-id is gekoppeld, selecteert u in het actievenster op het tabblad **Werk** de optie **Werkpool-id wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="026f2-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="026f2-193">Selecteer in het dialoogvenster **Werkpool wijzigen** de op het sneltabblad **Parameters** in het veld **Werkpool-id** de optie *Callcenter*.</span><span class="sxs-lookup"><span data-stu-id="026f2-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="026f2-194">Selecteer **OK** om de wijziging toe te passen.</span><span class="sxs-lookup"><span data-stu-id="026f2-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="026f2-195">U ziet dat de waarde van het veld **Werkpool-id** nu is gewijzigd in *Callcenter*.</span><span class="sxs-lookup"><span data-stu-id="026f2-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="026f2-196">Wanneer het dialoogvenster **Werkpool wijzigen** wordt weergegeven, is het veld **Werkpool-id** standaard leeg.</span><span class="sxs-lookup"><span data-stu-id="026f2-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="026f2-197">Als het veld leeg is wanneer u **OK** selecteert om wijzigingen toe te passen, wordt de werkpool volledig uit het werk verwijderd.</span><span class="sxs-lookup"><span data-stu-id="026f2-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="026f2-198">Naast het schakelen tussen werkpools kunt u deze procedure gebruiken om een werkpool toe te voegen aan een werkitem dat geen werkpools heeft of om een werkpool te verwijderen uit een werkitem dat wel een werkpool heeft.</span><span class="sxs-lookup"><span data-stu-id="026f2-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
