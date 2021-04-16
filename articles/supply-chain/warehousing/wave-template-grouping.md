---
title: Wave-sjabloongroepering
description: Met de functie Wave-sjabloongroepering kan het systeem wave-sjabloonconfiguraties gebruiken om te bepalen, op basis van criteria die u definieert, hoe vrijgegeven regels moeten worden gesplitst en aan nieuwe of bestaande waves worden toegewezen. Deze functie kan handig zijn in magazijnen waar waves worden gemaakt op basis van specifieke criteria, maar waar managers liever automatisch waves laten maken in plaats van handmatig.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a591624f6611148abe4888e67d8d3a9bbea9cd27
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838029"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="89e18-104">Wave-sjabloongroepering</span><span class="sxs-lookup"><span data-stu-id="89e18-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89e18-105">Met de functie Wave-sjabloongroepering kan het systeem [wave-sjabloon](tasks/configure-wave-processing.md)configuraties gebruiken om te bepalen, op basis van criteria die u definieert, hoe vrijgegeven regels moeten worden gesplitst en aan nieuwe of bestaande waves worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="89e18-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="89e18-106">Deze functie kan handig zijn in magazijnen waar waves worden gemaakt op basis van specifieke criteria, maar waar managers liever automatisch waves laten maken in plaats van handmatig.</span><span class="sxs-lookup"><span data-stu-id="89e18-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="89e18-107">Het systeem kan elke pas vrijgegeven zending toevoegen aan de eerste wave die wordt gevonden met overeenkomende groeperingsveldwaarden.</span><span class="sxs-lookup"><span data-stu-id="89e18-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="89e18-108">Als geen overeenkomst wordt gevonden, maakt het systeem een nieuwe wave aan voor de nieuwe zending.</span><span class="sxs-lookup"><span data-stu-id="89e18-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89e18-109">Wave-sjabloongroepering wordt niet ondersteund voor de werktypen *verzamelen van grondstoffen voor produtie* of *kanbanorderverzamelen*.</span><span class="sxs-lookup"><span data-stu-id="89e18-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="89e18-110">De reden hiervoor is dat de wavegroepering is gebaseerd op zendingen en dat deze werk typen geen zendingen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="89e18-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="89e18-111">De functie Wave-sjabloongroepering inschakelen</span><span class="sxs-lookup"><span data-stu-id="89e18-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="89e18-112">Voordat u de functie *Wave-sjabloongroepering* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="89e18-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="89e18-113">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="89e18-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="89e18-114">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="89e18-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="89e18-115">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="89e18-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="89e18-116">**Functienaam:** *Wave-sjabloongroepering*</span><span class="sxs-lookup"><span data-stu-id="89e18-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="89e18-117">Een wave-sjabloon instellen voor gebruik met wave-sjabloongroepering</span><span class="sxs-lookup"><span data-stu-id="89e18-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="89e18-118">Voer de volgende stappen uit om uw [wave-sjabloon in te stellen](tasks/configure-wave-processing.md) om wave-sjabloongroepering beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="89e18-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="89e18-119">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="89e18-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="89e18-120">Selecteer in het linkerdeelvenster de wave-sjabloon die u wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="89e18-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="89e18-121">Als u het scenario later in dit onderwerp wilt doorlopen met behulp van voorbeeldgegevens, selecteert u de sjabloon **62 Shipping default**.</span><span class="sxs-lookup"><span data-stu-id="89e18-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="89e18-122">Selecteer de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.</span><span class="sxs-lookup"><span data-stu-id="89e18-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="89e18-123">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="89e18-124">**Het maken van waves automatiseren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="89e18-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="89e18-125">**Toewijzen aan open waves:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="89e18-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="89e18-126">**Wave verwerken bij vrijgave door magazijn:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="89e18-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="89e18-127">Selecteer in het actievenster de optie **Query bewerken** het query-dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="89e18-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="89e18-128">Bekijk in het querydialoogvenster op het tabblad **Sorteren** de sorteercriteria en zorg ervoor dat er een regel is die het veld bevat dat u wilt gebruiken om uw waves te groeperen.</span><span class="sxs-lookup"><span data-stu-id="89e18-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="89e18-129">Als u het scenario wilt doorlopen met behulp van demogegevens, voegt u een rij toe die de volgende waarden bevat:</span><span class="sxs-lookup"><span data-stu-id="89e18-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="89e18-130">**Tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="89e18-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="89e18-131">**Afgeleide tabel:** *Zendingen*</span><span class="sxs-lookup"><span data-stu-id="89e18-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="89e18-132">**Veld:** *Vervoerdersservice*</span><span class="sxs-lookup"><span data-stu-id="89e18-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="89e18-133">Nadat u deze waarde hebt geselecteerd, kan de volgende melding worden weergegeven: "Vervoerdersservice is geen indexveld.</span><span class="sxs-lookup"><span data-stu-id="89e18-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="89e18-134">Wilt u hieraan sortering toevoegen?"</span><span class="sxs-lookup"><span data-stu-id="89e18-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="89e18-135">Selecteer **Ja** om sortering toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="89e18-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="89e18-136">**Zoekrichting:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="89e18-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="89e18-137">Selecteer **OK** om de wijzigingen op te slaan en het querydialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="89e18-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="89e18-138">Selecteer in het actievenster de optie **Wave-sjabloongroepering**.</span><span class="sxs-lookup"><span data-stu-id="89e18-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="89e18-139">Schakel op de pagina **Wave-sjabloongroepering** het selectievakje **Groeperen op** in voor elke rij die u wilt gebruiken om de orderregels in waves te groeperen.</span><span class="sxs-lookup"><span data-stu-id="89e18-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="89e18-140">Als u het scenario wilt doorlopen met behulp van voorbeeldgegevens, schakelt u het selectievakje **Groeperen op** in voor de rij *Vervoerderservice*.</span><span class="sxs-lookup"><span data-stu-id="89e18-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="89e18-141">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="89e18-141">Select **Save**.</span></span>
1. <span data-ttu-id="89e18-142">Sluit de pagina **Wave-sjabloongroepering**.</span><span class="sxs-lookup"><span data-stu-id="89e18-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="89e18-143">Klik op **Opslaan** om de sjabloon op te slaan.</span><span class="sxs-lookup"><span data-stu-id="89e18-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="89e18-144">Scenario's</span><span class="sxs-lookup"><span data-stu-id="89e18-144">Scenario</span></span>

<span data-ttu-id="89e18-145">Deze sectie bespreekt een scenario waarmee u kunt leren wat de functie doet en hoe u ermee kunt werken.</span><span class="sxs-lookup"><span data-stu-id="89e18-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="89e18-146">Voorbeeldgegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="89e18-146">Make sample data available</span></span>

<span data-ttu-id="89e18-147">Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="89e18-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="89e18-148">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="89e18-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="89e18-149">U kunt dit scenario ook gebruiken als instructie voor het gebruik van deze functie wanneer u met een productiesysteem werkt.</span><span class="sxs-lookup"><span data-stu-id="89e18-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="89e18-150">In dat geval moet u echter uw eigen waarden vervangen en hebt u mogelijk niet de beschikking over bepaalde typen vereiste records die met de standaard demogegevens worden verstrekt.</span><span class="sxs-lookup"><span data-stu-id="89e18-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="89e18-151">Scenario: Wave-sjabloongroepering</span><span class="sxs-lookup"><span data-stu-id="89e18-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="89e18-152">In dit scenario ziet u hoe u met wave-sjabloongroepering automatisch meerdere waves maakt op basis van groeperingscriteria die zijn gedefinieerd in een wave-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="89e18-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="89e18-153">In dit scenario wordt de wave-sjabloon geconfigureerd in het systeem om één wave per vervoerdersservice te maken.</span><span class="sxs-lookup"><span data-stu-id="89e18-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="89e18-154">Voordat u begint, moet u de wave-sjabloon voorbereiden zoals beschreven in de sectie [Een wave-sjabloon instellen voor gebruik met wave-sjabloongroepering](#set-up-template) eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="89e18-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="89e18-155">Als u voor dit scenario met demogegevens gaat werken, moet u ervoor zorgen dat u de voorbeeldgegevenswaarden gebruikt die in die procedure worden voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="89e18-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="89e18-156">Met deze configuratie worden de waves gegroepeerd op basis van de vervoerdersservice die voor elke verkooporder is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="89e18-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="89e18-157">Verkooporder 1 maken</span><span class="sxs-lookup"><span data-stu-id="89e18-157">Create sales order 1</span></span>

1. <span data-ttu-id="89e18-158">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="89e18-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="89e18-159">Selecteer **Nieuw** om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="89e18-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="89e18-160">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="89e18-161">Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-004*.</span><span class="sxs-lookup"><span data-stu-id="89e18-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="89e18-162">Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *62*.</span><span class="sxs-lookup"><span data-stu-id="89e18-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="89e18-163">Selecteer **OK** om het dialoogvenster **Verkooporder maken** te sluiten en de nieuwe verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="89e18-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="89e18-164">De nieuwe verkooporder wordt geopend in de weergave **Regels**.</span><span class="sxs-lookup"><span data-stu-id="89e18-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="89e18-165">Noteer het nummer van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="89e18-166">Schakel over naar de weergave **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="89e18-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="89e18-167">Stel op het sneltabblad **Levering** in de sectie **Transport** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="89e18-168">**Vervoerder:** *Air Cargo*</span><span class="sxs-lookup"><span data-stu-id="89e18-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="89e18-169">**Vervoerdersservice:** *Air*</span><span class="sxs-lookup"><span data-stu-id="89e18-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="89e18-170">Ga terug naar de weergave **Regels**.</span><span class="sxs-lookup"><span data-stu-id="89e18-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="89e18-171">Selecteer in de sectie **Verkooporderrgels** de optie **Regel toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="89e18-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="89e18-172">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89e18-173">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="89e18-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="89e18-174">**Hoeveelheid:** *2*</span><span class="sxs-lookup"><span data-stu-id="89e18-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="89e18-175">Selecteer de nieuwe orderregel en selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="89e18-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="89e18-176">Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="89e18-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="89e18-177">Sluit de pagina **Reservering** om terug te keren naar de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="89e18-178">Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="89e18-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="89e18-179">U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="89e18-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="89e18-180">Noteer het id-nummer van de wave en de id-nummers van de zendingen.</span><span class="sxs-lookup"><span data-stu-id="89e18-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="89e18-181">De wave weergeven die is gemaakt op basis van verkooporder 1</span><span class="sxs-lookup"><span data-stu-id="89e18-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="89e18-182">Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.</span><span class="sxs-lookup"><span data-stu-id="89e18-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="89e18-183">Selecteer de wave-id die is aangemaakt op basis van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="89e18-184">Selecteer de koppeling van de wave-id om de pagina Wave-gegevens te openen.</span><span class="sxs-lookup"><span data-stu-id="89e18-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="89e18-185">U ziet dat de zending is toegevoegd aan het sneltabblad **Wave-regels**.</span><span class="sxs-lookup"><span data-stu-id="89e18-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="89e18-186">Verkooporder 2 maken</span><span class="sxs-lookup"><span data-stu-id="89e18-186">Create sales order 2</span></span>

1. <span data-ttu-id="89e18-187">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="89e18-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="89e18-188">Selecteer **Nieuw** om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="89e18-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="89e18-189">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="89e18-190">Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-005*.</span><span class="sxs-lookup"><span data-stu-id="89e18-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="89e18-191">Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *62*.</span><span class="sxs-lookup"><span data-stu-id="89e18-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="89e18-192">Selecteer **OK** om het dialoogvenster **Verkooporder maken** te sluiten en de nieuwe verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="89e18-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="89e18-193">De nieuwe verkooporder wordt geopend in de weergave **Regels**.</span><span class="sxs-lookup"><span data-stu-id="89e18-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="89e18-194">Noteer het nummer van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="89e18-195">Schakel over naar de weergave **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="89e18-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="89e18-196">Stel op het sneltabblad **Levering** in de sectie **Transport** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="89e18-197">**Vervoerder:** *Flower moving*</span><span class="sxs-lookup"><span data-stu-id="89e18-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="89e18-198">**Vervoerdersservice:** *Std*</span><span class="sxs-lookup"><span data-stu-id="89e18-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="89e18-199">Ga terug naar de weergave **Regels**.</span><span class="sxs-lookup"><span data-stu-id="89e18-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="89e18-200">Selecteer in de sectie **Verkooporderrgels** de optie **Regel toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="89e18-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="89e18-201">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89e18-202">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="89e18-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="89e18-203">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="89e18-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="89e18-204">Selecteer de nieuwe orderregel en selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="89e18-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="89e18-205">Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="89e18-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="89e18-206">Sluit de pagina **Reservering** om terug te keren naar de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="89e18-207">Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="89e18-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="89e18-208">U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="89e18-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="89e18-209">Noteer het id-nummer van de wave en de id-nummers van de zendingen.</span><span class="sxs-lookup"><span data-stu-id="89e18-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="89e18-210">Merk op dat de wave-id anders is dan de wave-id van de eerste verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="89e18-211">De wave weergeven die is gemaakt op basis van verkooporder 2</span><span class="sxs-lookup"><span data-stu-id="89e18-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="89e18-212">Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.</span><span class="sxs-lookup"><span data-stu-id="89e18-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="89e18-213">Selecteer de wave-id die is aangemaakt op basis van de tweede verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="89e18-214">Selecteer de koppeling van de wave-id om de pagina Wave-gegevens te openen.</span><span class="sxs-lookup"><span data-stu-id="89e18-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="89e18-215">U ziet dat de zending is toegevoegd aan het sneltabblad **Wave-regels**.</span><span class="sxs-lookup"><span data-stu-id="89e18-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="89e18-216">Een nieuwe wave is gemaakt voor deze zending, omdat deze een andere vervoerdersservice gebruikt dan de eerste verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="89e18-217">Verkooporder 3 maken</span><span class="sxs-lookup"><span data-stu-id="89e18-217">Create sales order 3</span></span>

1. <span data-ttu-id="89e18-218">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="89e18-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="89e18-219">Selecteer **Nieuw** om een verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="89e18-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="89e18-220">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="89e18-221">Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-006*.</span><span class="sxs-lookup"><span data-stu-id="89e18-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="89e18-222">Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *62*.</span><span class="sxs-lookup"><span data-stu-id="89e18-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="89e18-223">Selecteer **OK** om het dialoogvenster **Verkooporder maken** te sluiten en de nieuwe verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="89e18-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="89e18-224">De nieuwe verkooporder wordt geopend in de weergave **Regels**.</span><span class="sxs-lookup"><span data-stu-id="89e18-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="89e18-225">Noteer het nummer van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="89e18-226">Schakel over naar de weergave **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="89e18-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="89e18-227">Stel op het sneltabblad **Levering** in de sectie **Transport** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="89e18-228">**Vervoerder:** *Air Cargo*</span><span class="sxs-lookup"><span data-stu-id="89e18-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="89e18-229">**Vervoerdersservice:** *Air*</span><span class="sxs-lookup"><span data-stu-id="89e18-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="89e18-230">Ga terug naar de weergave **Regels**.</span><span class="sxs-lookup"><span data-stu-id="89e18-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="89e18-231">Selecteer in de sectie **Verkooporderrgels** de optie **Regel toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="89e18-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="89e18-232">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="89e18-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89e18-233">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="89e18-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="89e18-234">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="89e18-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="89e18-235">Selecteer de nieuwe orderregel en selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="89e18-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="89e18-236">Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="89e18-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="89e18-237">Sluit de pagina **Reservering** om terug te keren naar de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="89e18-238">Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="89e18-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="89e18-239">U ontvangt een melding waarin de zending en de wave voor deze order worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="89e18-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="89e18-240">Noteer het id-nummer van de wave en de id-nummers van de zendingen.</span><span class="sxs-lookup"><span data-stu-id="89e18-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="89e18-241">De zending is toegewezen aan de bestaande wave van de eerste verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="89e18-242">De wave voor verkooporders 1 en 3 weergeven</span><span class="sxs-lookup"><span data-stu-id="89e18-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="89e18-243">Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.</span><span class="sxs-lookup"><span data-stu-id="89e18-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="89e18-244">Selecteer de wave-id die is aangemaakt op basis van de derde verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="89e18-245">Selecteer de koppeling van de wave-id om de pagina Wave-gegevens te openen.</span><span class="sxs-lookup"><span data-stu-id="89e18-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="89e18-246">U ziet dat de zending is toegevoegd aan het sneltabblad **Wave-regels** , samen met de zending voor de eerste verkooporder.</span><span class="sxs-lookup"><span data-stu-id="89e18-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]