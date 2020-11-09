---
title: Kwaliteitscontrole
description: Dit onderwerp bevat informatie over de functie voor kwaliteitscontrole. Met deze functie kunnen magazijnmedewerkers snel controleren op kwaliteit terwijl zij artikelen ontvangen naar het inkomend docking-gebied.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dfb71f74732d65409003c4f6f74145442a1efa3f
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016626"
---
# <a name="quality-check"></a><span data-ttu-id="cd10d-104">Kwaliteitscontrole</span><span class="sxs-lookup"><span data-stu-id="cd10d-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd10d-105">Met de functie *Kwaliteitscontrole* kunnen magazijnmedewerkers snel controleren op kwaliteit terwijl zij artikelen ontvangen naar het inkomend docking-gebied.</span><span class="sxs-lookup"><span data-stu-id="cd10d-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="cd10d-106">Deze controles zijn nuttig wanneer werknemers verpakking of andere gemakkelijk herkenbare delen van een artikel controleren.</span><span class="sxs-lookup"><span data-stu-id="cd10d-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="cd10d-107">De functie helpt werknemers om snel te kijken of er iets misgaat of beschadigd raakt voordat ze de voorraad in de wegzetlocatie opslaan.</span><span class="sxs-lookup"><span data-stu-id="cd10d-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="cd10d-108">Deze functie is een alternatief voor het standaardproces voor kwaliteitscontrole.</span><span class="sxs-lookup"><span data-stu-id="cd10d-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="cd10d-109">Het biedt meer flexibiliteit en snellere verwerking.</span><span class="sxs-lookup"><span data-stu-id="cd10d-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="cd10d-110">Wanneer u deze functie gebruikt, worden de ontvangst en de kwaliteitscontrole op de volgende manier uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="cd10d-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="cd10d-111">Wanneer een zending arriveert, registreert een magazijnmedewerker de ontvangst.</span><span class="sxs-lookup"><span data-stu-id="cd10d-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="cd10d-112">De werknemer scant ook een nummerplaat om de locatie te registreren.</span><span class="sxs-lookup"><span data-stu-id="cd10d-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="cd10d-113">De werknemer voert een snelle kwaliteitscontrole uit en registreert het resultaat (geslaagd of mislukt) voor die nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="cd10d-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="cd10d-114">Een van de volgende acties wordt uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="cd10d-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="cd10d-115">Als de kwaliteitscontrole slaagt, wordt de nummerplaat op de gebruikelijke manier geaccepteerd en doorgeleid naar de locatie van ontvangst.</span><span class="sxs-lookup"><span data-stu-id="cd10d-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="cd10d-116">Als de kwaliteitscontrole mislukt, wordt de nummerplaat afgewezen en wordt het bestaande wegzetwerk ervoor omgeleid naar een alternatieve locatie voor verdere inspectie.</span><span class="sxs-lookup"><span data-stu-id="cd10d-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="cd10d-117">Er wordt een nieuwe kwaliteitsorder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-117">A new quality order is created.</span></span> <span data-ttu-id="cd10d-118">Als u de kwaliteitsorder wilt weergeven die is gemaakt voor de mislukte kwaliteitscontrole, gaat u naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="cd10d-119">Dit proces kan ook zo worden ingesteld dat alle gescande nummerplaten direct naar de locatie van de kwaliteitscontrole worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="cd10d-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="cd10d-120">De functie Kwaliteitscontrole inschakelen</span><span class="sxs-lookup"><span data-stu-id="cd10d-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="cd10d-121">Voordat u de functie *Kwaliteitscontrole* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="cd10d-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="cd10d-122">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="cd10d-123">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="cd10d-124">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="cd10d-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="cd10d-125">**Functienaam:** *Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="cd10d-126">De functie instellen voor het voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="cd10d-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="cd10d-127">Deze sectie bevat richtlijnen en een voorbeeld waarin wordt uitgelegd hoe u de functie *Kwaliteitscontrole* instelt en voorbeeldgegevens voorbereidt voor het voorbeeldscenario dat verderop in dit onderwerp wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="cd10d-128">Voorbeeldgegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="cd10d-128">Make sample data available</span></span>

<span data-ttu-id="cd10d-129">Als u het [voorbeeldscenario](#example-scenario) wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="cd10d-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="cd10d-130">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="cd10d-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="cd10d-131">Sjabloon kwaliteitscontrole</span><span class="sxs-lookup"><span data-stu-id="cd10d-131">Quality check template</span></span>

<span data-ttu-id="cd10d-132">Met de sjabloon voor kwaliteitscontrole worden de regels gedefinieerd voor het uitvoeren van snelle controles op kwaliteit op het moment van ontvangst.</span><span class="sxs-lookup"><span data-stu-id="cd10d-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="cd10d-133">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Kwaliteitscontrolesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="cd10d-134">Selecteer **Nieuw** om een sjabloon toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="cd10d-135">Stel de volgende waarden in om de nieuwe sjabloon te definiëren:</span><span class="sxs-lookup"><span data-stu-id="cd10d-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="cd10d-136">**Naam van sjabloon voor kwaliteitscontrole:** *Dock-controle*</span><span class="sxs-lookup"><span data-stu-id="cd10d-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="cd10d-137">Voer een naam in die het beleid aanduidt dat voor deze sjabloon wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="cd10d-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="cd10d-138">**Acceptatiebeleid:** *Vragen aan gebruiker*</span><span class="sxs-lookup"><span data-stu-id="cd10d-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="cd10d-139">Geef op of gebruikers moet worden gevraagd de kwaliteit van de voorraad te accepteren of af te wijzen tijdens het verwerken van het werk, of dat de kwaliteit automatisch moet worden afgewezen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="cd10d-140">De beschikbare opties zijn *Automatisch afwijzen* en *Vragen aan gebruiker*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="cd10d-141">**Beleid voor kwaliteitsverwerkings:** *Kwaliteitsorder maken*</span><span class="sxs-lookup"><span data-stu-id="cd10d-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="cd10d-142">Selecteer het beleid dat moet worden gebruikt bij het afwijzen van de kwaliteit van de voorraad.</span><span class="sxs-lookup"><span data-stu-id="cd10d-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="cd10d-143">De volgende opties zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="cd10d-143">The following options are available:</span></span>

        - <span data-ttu-id="cd10d-144">*Alleen werk maken* : alleen werk maken om de voorraadverplaatsing te vergemakkelijken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="cd10d-145">*Kwaliteitsorder maken* : een kwaliteitsorder maken om kwaliteitstests te vergemakkelijken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="cd10d-146">**Testgroep:** *Monster*</span><span class="sxs-lookup"><span data-stu-id="cd10d-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="cd10d-147">Geef de testgroep op die moet worden gebruikt in de kwaliteitsorder die wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="cd10d-148">Testgroepen worden ingesteld in de module **Voorraadbeheer**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="cd10d-149">Laat de optie **Destructieve tekst** uitgeschakeld voor de testgroep.</span><span class="sxs-lookup"><span data-stu-id="cd10d-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="cd10d-150">Deze optie definieert wanneer het monster wordt vernietigd als onderdeel van de tests in de testgroep.</span><span class="sxs-lookup"><span data-stu-id="cd10d-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="cd10d-151">Als een destructieve test wordt gebruikt, genereert het systeem een voorraadtransactie wanneer een kwaliteitsorder voor het artikel wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="cd10d-152">De nieuwe voorraadtransactie voorspelt de voorraadreductie voor de testhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="cd10d-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="cd10d-153">De voorraadreductie treedt op wanneer de kwaliteitsorder wordt voltooid door de validatiestap.</span><span class="sxs-lookup"><span data-stu-id="cd10d-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="cd10d-154">De voorraadtransactie wordt aangeduid als een kwaliteitsorder.</span><span class="sxs-lookup"><span data-stu-id="cd10d-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="cd10d-155">Werkklasse: Kwaliteitscontrole</span><span class="sxs-lookup"><span data-stu-id="cd10d-155">Work class – Quality check</span></span>

<span data-ttu-id="cd10d-156">Werkklassen worden gebruikt om het type werkorderregels te bepalen en/of beperken dat magazijnwerknemers op een mobiel apparaat kunnen verwerken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="cd10d-157">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="cd10d-158">Selecteer **Nieuw** om een werkklasse te maken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="cd10d-159">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="cd10d-160">**Werkklasse-id:** *Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="cd10d-161">Voer een naam in waarmee de werkklasse wordt aangeduid.</span><span class="sxs-lookup"><span data-stu-id="cd10d-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="cd10d-162">**Omschrijving:** *Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="cd10d-163">Voer een korte omschrijving in waarmee wordt aangegeven waarvoor de werkklasse wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="cd10d-164">**Werkordertype:** *Kwaliteit in kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="cd10d-165">Het type werkorder selecteren dat door de werkklasse wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="cd10d-166">Wanneer u het kwaliteitscontrolewerk instelt, moet u altijd *Kwaliteit in kwaliteitscontrole* selecteren.</span><span class="sxs-lookup"><span data-stu-id="cd10d-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="cd10d-167">Laat op het tabblad **Geldige typen locaties voor plaatsing** het veld **Locatietype** leeg.</span><span class="sxs-lookup"><span data-stu-id="cd10d-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="cd10d-168">Als u een locatie type selecteert, beperkt u de locaties waar artikelen kunnen worden geplaatst nadat ze zijn verzameld.</span><span class="sxs-lookup"><span data-stu-id="cd10d-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="cd10d-169">Dit veld wordt gebruikt wanneer een locatierichtlijn probeert de locatie op te lossen of wanneer een magazijnwerknemer handmatig de locatie voor menuopdrachten van mobiele apparaten opgeeft.</span><span class="sxs-lookup"><span data-stu-id="cd10d-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="cd10d-170">Zie voor meer informatie over werkklassen en hoe u ze maakt [Werkklassen maken](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="cd10d-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="cd10d-171">Werksjabloon</span><span class="sxs-lookup"><span data-stu-id="cd10d-171">Work template</span></span>

<span data-ttu-id="cd10d-172">Op de pagina Werksjablonen kunt u de werkbewerkingen definiëren die in het magazijn moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="cd10d-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="cd10d-173">Doorgaans bestaan de bewerkingen van het magazijnwerk uit een tweetal acties: een magazijnwerknemer verzamelt voorhanden voorraad in één locatie en brengt de voorraad vervolgens naar een andere locatie.</span><span class="sxs-lookup"><span data-stu-id="cd10d-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="cd10d-174">Met een werksjabloon voor kwaliteitscontrole worden de werkbewerkingen gedefinieerd voor het uitvoeren van kwaliteitscontroles.</span><span class="sxs-lookup"><span data-stu-id="cd10d-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="cd10d-175">Inkooporders</span><span class="sxs-lookup"><span data-stu-id="cd10d-175">Purchase orders</span></span>

1. <span data-ttu-id="cd10d-176">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="cd10d-177">Stel in de koptekst het veld **Werkordertype** in op *Inkooporders*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="cd10d-178">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="cd10d-179">Selecteer een werksjabloon die een kwaliteitscontrolestap moet bevatten.</span><span class="sxs-lookup"><span data-stu-id="cd10d-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="cd10d-180">Selecteer in het gedeelte **Overzicht** in het veld **Werksjabloon** *51 IO-ontvangst*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="cd10d-181">In de sectie **Werksjabloongegevens** ziet u dat het raster twee bestaande regels bevat: een voor *Verzamelen* en een voor *Wegzetten*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="cd10d-182">Selecteer in de sectie **Werksjabloongegevens** **Nieuw** om een rij voor kwaliteitscontrole toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="cd10d-183">Het veld **Regelnummer** voor de nieuwe regel wordt ingesteld op *3*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="cd10d-184">Stel op de nieuwe regel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="cd10d-184">On the new line, set the following values.</span></span> <span data-ttu-id="cd10d-185">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="cd10d-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="cd10d-186">**Werksoort:** *Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="cd10d-187">**Werkklasse-id:** *Aankoop*</span><span class="sxs-lookup"><span data-stu-id="cd10d-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="cd10d-188">**Naam van sjabloon voor kwaliteitscontrole:** *Dock-controle*</span><span class="sxs-lookup"><span data-stu-id="cd10d-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="cd10d-189">Selecteer de unieke ID voor de werkklasse.</span><span class="sxs-lookup"><span data-stu-id="cd10d-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="cd10d-190">U gebruikt deze waarde om de menuopties op het mobiele apparaat en typen het werk te configureren die deze menu-items kunnen verwerken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="cd10d-191">Selecteer in het actievenster de optie **Opslaan** om uw werk tot dusverre op te slaan.</span><span class="sxs-lookup"><span data-stu-id="cd10d-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="cd10d-192">U ontvangt een bericht met de mededeling dat de kwaliteitscontrole direct na de verzameling moet komen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="cd10d-193">Daarom moet u de waarde **Regelnummer** wijzigen voor de regel die u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="cd10d-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="cd10d-194">Voer de volgende stappen uit om de waarde **Regelnummer** voor de nieuwe regel te wijzigen:</span><span class="sxs-lookup"><span data-stu-id="cd10d-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="cd10d-195">Selecteer in de sectie **Werksjabloongegevens** de regel waarvoor het veld **Werksoort** is ingesteld op *Kwaliteitscontrole*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="cd10d-196">Selecteer de knop **Omhoog verplaatsen** of **Omlaag verplaatsen** om de regel *Kwaliteitscontrole* te verplaatsen, zodat deze na de regel *Verzamelen* valt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="cd10d-197">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="cd10d-198">Kwaliteit in kwaliteitscontrole</span><span class="sxs-lookup"><span data-stu-id="cd10d-198">Quality in quality check</span></span>

<span data-ttu-id="cd10d-199">Maak vervolgens een werksjabloon voor de kwaliteitscontrole.</span><span class="sxs-lookup"><span data-stu-id="cd10d-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="cd10d-200">Wijzig in de koptekst van de pagina **Werksjablonen** de waarde van het veld **Werkordertype** in *Kwaliteitscontrole*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="cd10d-201">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster in de sectie **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="cd10d-202">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="cd10d-203">**Werksjabloon:** *51 Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="cd10d-204">Voer een naam voor de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="cd10d-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="cd10d-205">**Omschrijving werksjabloon:** *51 Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="cd10d-206">Selecteer in het actievenster **Opslaan** om de sectie **Werksjabloongegevens** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="cd10d-207">Selecteer terwijl de nieuwe sjabloon nog is geselecteerd in de sectie **Overzicht** **Nieuw** in de sectie **Werksjabloongegevens** om een rij toe te voegen aan het raster daar.</span><span class="sxs-lookup"><span data-stu-id="cd10d-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="cd10d-208">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="cd10d-209">**Werktype:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="cd10d-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="cd10d-210">**Werkklasse-id:** *Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="cd10d-211">Selecteer de naam van de [werkklasse](#work-class) die u eerder hebt gemaakt voor kwaliteitscontrolewerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="cd10d-212">Selecteer **Nieuw** in de sectie **Werksjabloongegevens** om nog een rij toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="cd10d-213">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="cd10d-214">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="cd10d-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="cd10d-215">**Werkklasse-id:** *Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="cd10d-216">Selecteer de naam van de [werkklasse](#work-class) die u eerder hebt gemaakt voor kwaliteitscontrolewerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="cd10d-217">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="cd10d-218">Zie voor meer informatie over werksjablonen [Magazijnwerk beheren met werksjablonen en locatierichtlijnen](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="cd10d-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="cd10d-219">Locatierichtlijn: Kwaliteitsproblemen</span><span class="sxs-lookup"><span data-stu-id="cd10d-219">Location directive – Quality failures</span></span>

<span data-ttu-id="cd10d-220">De locatierichtlijnen zijn regels die verzamelings- en wegzetlocaties identificeren voor voorraadverplaatsing.</span><span class="sxs-lookup"><span data-stu-id="cd10d-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="cd10d-221">Bijvoorbeeld, in een verkoopordertransactie, bepaalt een locatierichtlijn waar de artikelen worden verzameld en waar de verzamelde artikelen worden weggezet.</span><span class="sxs-lookup"><span data-stu-id="cd10d-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="cd10d-222">U moet een locatierichtlijnregel configureren om te definiëren hoe mislukte kwaliteitscontroles worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="cd10d-223">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="cd10d-224">Stel in het linkerdeelvenster het veld **Werkordertype** in op *Inkooporders* om te werken met locatierichtlijnen van dat type.</span><span class="sxs-lookup"><span data-stu-id="cd10d-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="cd10d-225">Selecteer in het actievenster de optie **Nieuw** om een locatierichtlijn voor kwaliteitscontroles te maken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="cd10d-226">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="cd10d-227">**Volgnummer:** Accepteer de standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="cd10d-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="cd10d-228">**Naam:** *51 Naar kwaliteit*</span><span class="sxs-lookup"><span data-stu-id="cd10d-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="cd10d-229">Stel op het sneltabblad **Locatie-instructies** de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="cd10d-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="cd10d-230">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="cd10d-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="cd10d-231">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="cd10d-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="cd10d-232">**Locatie:** *5*</span><span class="sxs-lookup"><span data-stu-id="cd10d-232">**Site:** *5*</span></span>
    - <span data-ttu-id="cd10d-233">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="cd10d-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="cd10d-234">Selecteer in het actievenster **Opslaan** om uw richtlijn op te slaan en het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="cd10d-235">Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="cd10d-236">Stel op de nieuwe regel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="cd10d-236">On the new line, set the following values.</span></span> <span data-ttu-id="cd10d-237">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="cd10d-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="cd10d-238">**Vanaf hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="cd10d-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="cd10d-239">**Tot hoeveelheid:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="cd10d-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="cd10d-240">Selecteer in het actievenster **Opslaan** om de nieuwe regel op te slaan en het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="cd10d-241">Terwijl de nieuwe regel nog steeds is geselecteerd op het sneltabblad **Regels** , selecteert u **Nieuw** op het sneltabblad **Locatie-instructieacties** om een rij toe te voegen aan het raster daar, zodat u een actie voor de regel kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="cd10d-242">Stel op de nieuwe rij het veld **Naam** in op *Kwaliteit*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="cd10d-243">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="cd10d-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="cd10d-244">Selecteer in het actievenster **Opslaan** om de knop **Query bewerken** op het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="cd10d-245">Terwijl de regel die u zojuist hebt toegevoegd nog steeds is geselecteerd op het sneltabblad **Locatie-instructieacties** , selecteert u **Query bewerken** om een dialoogvenster te openen waarin u de query voor de actie kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="cd10d-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="cd10d-246">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een rij toe te voegen aan de query.</span><span class="sxs-lookup"><span data-stu-id="cd10d-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="cd10d-247">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="cd10d-248">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="cd10d-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="cd10d-249">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="cd10d-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="cd10d-250">**Veld:** *Locatie*</span><span class="sxs-lookup"><span data-stu-id="cd10d-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="cd10d-251">**Criteria:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="cd10d-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="cd10d-252">De *QMS* -locatie is een magazijnlocatie voor kwaliteit.</span><span class="sxs-lookup"><span data-stu-id="cd10d-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="cd10d-253">Selecteer **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="cd10d-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="cd10d-254">U moet nu de volgorde van de bestaande inkooporderlocatierichtlijnen wijzigen voor magazijn *51*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="cd10d-255">Sla de nieuwe locatierichtlijn *51 Naar kwaliteit* op, vernieuw de pagina en selecteer de locatierichtlijn in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cd10d-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="cd10d-256">Gebruik vervolgens de knoppen **Omhoog verplaatsen** en **Omlaag verplaatsen** in het actievenster om de locatie-instructie voor magazijn *51* in de volgende volgorde te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="cd10d-257">(Voordat u **Omhoog verplaatsen** of **Omlaag verplaatsen** selecteert, moet u een locatierichtlijn selecteren in de lijst.)</span><span class="sxs-lookup"><span data-stu-id="cd10d-257">(Before you select **Move up** or **Move down** , you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="cd10d-258">51 Naar kwaliteit</span><span class="sxs-lookup"><span data-stu-id="cd10d-258">51 To Quality</span></span>
    2. <span data-ttu-id="cd10d-259">51 IO direct</span><span class="sxs-lookup"><span data-stu-id="cd10d-259">51 PO Direct</span></span>
    3. <span data-ttu-id="cd10d-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="cd10d-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="cd10d-261">Menuopties voor mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="cd10d-261">Mobile device menu items</span></span>

<span data-ttu-id="cd10d-262">Configureer een menuopdracht zodat mobiele apparaten de functie **Kwaliteitscontrole** kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="cd10d-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="cd10d-263">Opslag van inkoop</span><span class="sxs-lookup"><span data-stu-id="cd10d-263">Purchase putaway</span></span>

1. <span data-ttu-id="cd10d-264">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="cd10d-265">Selecteer de menuopdracht **Opslag van inkoop** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cd10d-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="cd10d-266">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="cd10d-267">Selecteer in de sectie **Werkklassen** **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="cd10d-268">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="cd10d-269">**Werkklasse-id:** *Kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="cd10d-270">Voer de naam in van de [werkklasse](#work-class) die u eerder hebt gemaakt voor kwaliteitscontrolewerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="cd10d-271">**Werkordertype:** *Kwaliteit in kwaliteitscontrole*</span><span class="sxs-lookup"><span data-stu-id="cd10d-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="cd10d-272">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="cd10d-273">Ontvangen van inkooporderregel</span><span class="sxs-lookup"><span data-stu-id="cd10d-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="cd10d-274">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="cd10d-275">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="cd10d-276">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="cd10d-277">**Menuoptie:** *IO-regel ontvangst*</span><span class="sxs-lookup"><span data-stu-id="cd10d-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="cd10d-278">**Titel:** *IO-regel ontvangst*</span><span class="sxs-lookup"><span data-stu-id="cd10d-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="cd10d-279">**Modus:** *werk*</span><span class="sxs-lookup"><span data-stu-id="cd10d-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="cd10d-280">**Bestaand werk gebruiken:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="cd10d-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="cd10d-281">Stel op het sneltabblad **Algemeen** de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="cd10d-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="cd10d-282">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="cd10d-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="cd10d-283">**Procedure voor het maken van werk:** *Ontvangen van inkooporderregel en wegzetten*</span><span class="sxs-lookup"><span data-stu-id="cd10d-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="cd10d-284">**Nummerplaat maken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="cd10d-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="cd10d-285">**Werksjabloon:** *51 IO ontvangst*</span><span class="sxs-lookup"><span data-stu-id="cd10d-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="cd10d-286">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="cd10d-287">De menuopdracht toevoegen aan het menu van een mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="cd10d-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="cd10d-288">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="cd10d-289">Selecteer het menu **Inkomend** in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="cd10d-290">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="cd10d-291">Selecteer in de kolom **Beschikbare menu's en menuopdrachten** de nieuwe menuopdracht **IO-regel ontvangst**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="cd10d-292">Selecteer de pijl naar rechts om **IO-regel ontvangst** naar de kolom **Menustructuur** te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="cd10d-293">Selecteer in de kolom **Menustructuur** de optie **IO-regel ontvangst** en selecteer vervolgens de knop pijl-omhoog of pijl-omlaag om de menuoptie naar de gewenste positie in het menu van het mobiele apparaat te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-293">In the **Menu structure** column, select **PO line receiving** , and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="cd10d-294">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="cd10d-295">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="cd10d-295">Example scenario</span></span>

<span data-ttu-id="cd10d-296">Nadat u alle eerder beschreven voorbeeldgegevens hebt gemaakt en ingesteld, kunt u dit scenario doorlopen om de functie *Kwaliteitscontrole* uit te proberen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="cd10d-297">Bij de waarden die in dit scenario worden weergegeven, wordt ervan uitgegaan dat u werkt met de standaarddemonstratiegegevens, dat u de rechtspersoon **USMF** hebt geselecteerd en dat u de voorbeeldrecords hebt voorbereid die eerder in dit onderwerp zijn beschreven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="cd10d-298">Dit scenario dient ook als voorbeeld waarin wordt aangegeven hoe de functie in een productie-instelling kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="cd10d-299">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="cd10d-299">Create a purchase order</span></span>

1. <span data-ttu-id="cd10d-300">Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="cd10d-301">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="cd10d-302">Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="cd10d-303">**Leverancierrekening:** *104*</span><span class="sxs-lookup"><span data-stu-id="cd10d-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="cd10d-304">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="cd10d-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="cd10d-305">Selecteer **OK** om het dialoogvenster te sluiten en de nieuwe inkooporder te openen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="cd10d-306">Op het sneltabblad **Inkooporderregels** bevat het raster een nieuwe, lege regel.</span><span class="sxs-lookup"><span data-stu-id="cd10d-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="cd10d-307">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="cd10d-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="cd10d-308">**Artikelnummer:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="cd10d-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="cd10d-309">**Hoeveelheid:** *3*</span><span class="sxs-lookup"><span data-stu-id="cd10d-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="cd10d-310">**Eenheid:** *PL*</span><span class="sxs-lookup"><span data-stu-id="cd10d-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="cd10d-311">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="cd10d-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="cd10d-312">Ontvangst controleren van proceskwaliteit</span><span class="sxs-lookup"><span data-stu-id="cd10d-312">Process quality check receiving</span></span>

<span data-ttu-id="cd10d-313">Nadat de inkooporder is gemaakt, kunt u deze ontvangen met de menuopdracht **IO-regel ontvangst** en de functionaliteit van de functie *Kwaliteitscontrole*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="cd10d-314">Pallet 1 ontvangen</span><span class="sxs-lookup"><span data-stu-id="cd10d-314">Receive pallet 1</span></span>

1. <span data-ttu-id="cd10d-315">Meld u aan bij de magazijnapp als een gebruiker voor magazijn *51*.</span><span class="sxs-lookup"><span data-stu-id="cd10d-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="cd10d-316">(Geef *51* op als gebruikers-id en *1* als wachtwoord.)</span><span class="sxs-lookup"><span data-stu-id="cd10d-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="cd10d-317">Ga naar **Inkomend \> IO-regel ontvangst**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="cd10d-318">Voer in het veld **Inkoopordernummer** het inkoopordernummer in.</span><span class="sxs-lookup"><span data-stu-id="cd10d-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="cd10d-319">Bevestig het inkoopordernummer.</span><span class="sxs-lookup"><span data-stu-id="cd10d-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="cd10d-320">Voer in het veld **Regelnummer** het regelnummer in van de inkooporderregel die u ontvangt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="cd10d-321">Aangezien de order slechts één regel bevat in dit scenario, voert u *1* in het veld **Regelnummer** in voor elke ontvangststap.</span><span class="sxs-lookup"><span data-stu-id="cd10d-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="cd10d-322">Controleer het regelnummer.</span><span class="sxs-lookup"><span data-stu-id="cd10d-322">Confirm the line number.</span></span>
1. <span data-ttu-id="cd10d-323">Voer in het veld **Hoeveelheid** de te ontvangen hoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="cd10d-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="cd10d-324">Aangezien de inkooporder voor drie pallets ( *PL* ) is in dit scenario en er drie ontvangststappen zijn, voert u *1* in het veld **Hoeveelheid** in voor elke ontvangststap.</span><span class="sxs-lookup"><span data-stu-id="cd10d-324">Because the purchase order is for three pallets ( *PL* ) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="cd10d-325">Bevestig de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="cd10d-325">Confirm the quantity.</span></span>

    <span data-ttu-id="cd10d-326">De pagina **Kwaliteitscontrole** die wordt weergegeven, bevat geen invoervelden.</span><span class="sxs-lookup"><span data-stu-id="cd10d-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="cd10d-327">De pagina bevat alleen de bevestigingsknop (vinkje) onderaan en de menuknop ( **≡** ) bovenaan.</span><span class="sxs-lookup"><span data-stu-id="cd10d-327">It has only the confirmation (check mark) button at the bottom and the Menu button ( **≡** ) at the top.</span></span> <span data-ttu-id="cd10d-328">(De menuknop wordt ook wel de hamburger of de hamburgerknop genoemd.) Om het proces voor de kwaliteitscontrole te versnellen, bevestigt de gebruiker alleen de pagina **Kwaliteitscontrole** wanneer de pallet langs de kwaliteitscontrole komt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="cd10d-329">![Pagina Kwaliteitscontrole](media/quality-check.png "Pagina Kwaliteitscontrole")</span><span class="sxs-lookup"><span data-stu-id="cd10d-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="cd10d-330">Selecteer de bevestigingsknop om de kwaliteitscontrole door te geven voor pallet 1 van regel 1.</span><span class="sxs-lookup"><span data-stu-id="cd10d-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="cd10d-331">Op de pagina **Inkoop orders: wegzetten** staan details van het wegzetwerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="cd10d-332">**LOC:** de door het systeem vastgestelde locatie</span><span class="sxs-lookup"><span data-stu-id="cd10d-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="cd10d-333">Deze locatie is de aangewezen wegzetlocatie voor het ontvangen van inkooporders.</span><span class="sxs-lookup"><span data-stu-id="cd10d-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="cd10d-334">**LP:** de door het systeem gegenereerde nummerplaat-id</span><span class="sxs-lookup"><span data-stu-id="cd10d-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="cd10d-335">**Artikel:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="cd10d-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="cd10d-336">**Hoeveelheid:** *1 PL: 100 stuks*</span><span class="sxs-lookup"><span data-stu-id="cd10d-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="cd10d-337">De artikelomschrijving wordt ook weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-337">The item description is also shown.</span></span>

1. <span data-ttu-id="cd10d-338">Bevestig het wegzetwerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="cd10d-339">Op de pagina **Taak** voor het ontvangen van inkooporderregels wordt het bericht 'Werk voltooid' weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="cd10d-340">Het veld **Regelnummer** is beschikbaar zodat u de volgende pallet kunt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="cd10d-341">Pallet 2 ontvangen</span><span class="sxs-lookup"><span data-stu-id="cd10d-341">Receive pallet 2</span></span>

<span data-ttu-id="cd10d-342">Voor dit scenario wordt pallet 2 afgewezen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="cd10d-343">Voer *1* in het veld **Regelnummer** in en bevestig het regelnummer.</span><span class="sxs-lookup"><span data-stu-id="cd10d-343">In the **LINENUM** field, enter *1* , and confirm the line number.</span></span>
1. <span data-ttu-id="cd10d-344">Het veld **Hoeveelheid** is nu beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="cd10d-344">The **QTY** field is now available.</span></span> <span data-ttu-id="cd10d-345">Voer *1* in en bevestig de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="cd10d-345">Enter *1* , and confirm the quantity.</span></span>

    <span data-ttu-id="cd10d-346">De pagina **Kwaliteitscontrole** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-346">The **Quality check** page appears.</span></span> <span data-ttu-id="cd10d-347">Voor deze ontvangst wordt de pallet afgewezen voor kwaliteit en wordt deze op de kwaliteitslocatie *QMS* weggezet.</span><span class="sxs-lookup"><span data-stu-id="cd10d-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="cd10d-348">Selecteer de menuknop ( **≡** ) boven aan de pagina en selecteer vervolgens in het menu de optie **Weigeren**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-348">Select the Menu button ( **≡** ) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="cd10d-349">Voer op de pagina **Taak** die verschijnt **QMS** in als de *wegzet* locatie voor het verzenden van de pallet voor verdere inspectie.</span><span class="sxs-lookup"><span data-stu-id="cd10d-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="cd10d-350">Op de pagina **Kwaliteit in kwaliteitscontrole: Wegzetten** , die wordt weergegeven, staan details van het wegzetwerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="cd10d-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="cd10d-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="cd10d-352">Deze locatie is de aangewezen wegzetlocatie voor wegens kwaliteit geweigerde ontvangst.</span><span class="sxs-lookup"><span data-stu-id="cd10d-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="cd10d-353">**LP:** de door het systeem gegenereerde nummerplaat-id</span><span class="sxs-lookup"><span data-stu-id="cd10d-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="cd10d-354">**Artikel:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="cd10d-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="cd10d-355">**Hoeveelheid:** *1 PL: 100 stuks*</span><span class="sxs-lookup"><span data-stu-id="cd10d-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="cd10d-356">De artikelomschrijving wordt ook weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-356">The item description is also shown.</span></span>

1. <span data-ttu-id="cd10d-357">Bevestig het wegzetwerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="cd10d-358">Op de pagina **Taak** voor het ontvangen van inkooporderregels wordt het bericht 'Werk voltooid' weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="cd10d-359">Het veld **Regelnummer** is beschikbaar zodat u de volgende pallet kunt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="cd10d-360">U hebt de kwaliteitscontrole nu voltooid en een kwaliteitsorder gemaakt voor de afgekeurde pallet.</span><span class="sxs-lookup"><span data-stu-id="cd10d-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="cd10d-361">Als u de gemaakte order wilt weergeven, gaat u naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.</span><span class="sxs-lookup"><span data-stu-id="cd10d-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="cd10d-362">Het testen van kwaliteitsorders kan nu worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="cd10d-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="cd10d-363">Kwaliteitstests worden niet behandeld in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="cd10d-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="cd10d-364">Zie voor meer informatie over kwaliteitsbeheer [Overzicht van kwaliteitsbeheer](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="cd10d-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="cd10d-365">Pallet 3 ontvangen</span><span class="sxs-lookup"><span data-stu-id="cd10d-365">Receive pallet 3</span></span>

<span data-ttu-id="cd10d-366">Voor dit scenario wordt pallet 3 geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="cd10d-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="cd10d-367">Voer *1* in het veld **Regelnummer** in en bevestig het regelnummer.</span><span class="sxs-lookup"><span data-stu-id="cd10d-367">In the **LINENUM** field, enter *1* , and confirm the line number.</span></span>
1. <span data-ttu-id="cd10d-368">Het veld **Hoeveelheid** is nu beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="cd10d-368">The **QTY** field is now available.</span></span> <span data-ttu-id="cd10d-369">Voer *1* in en bevestig de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="cd10d-369">Enter *1* , and confirm the quantity.</span></span>

    <span data-ttu-id="cd10d-370">De pagina **Kwaliteitscontrole** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-370">The **Quality check** page appears.</span></span> <span data-ttu-id="cd10d-371">Voor deze ontvangst wordt de pallet geaccepteerd voor kwaliteit en wordt deze op een bulkwegzetlocatie weggezet.</span><span class="sxs-lookup"><span data-stu-id="cd10d-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="cd10d-372">Selecteer de bevestigingsknop om de kwaliteitscontrole te laten slagen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="cd10d-373">Op de pagina **Inkoop orders: wegzetten** staan details van het wegzetwerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="cd10d-374">**LOC:** de door het systeem vastgestelde locatie</span><span class="sxs-lookup"><span data-stu-id="cd10d-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="cd10d-375">Deze locatie is de aangewezen wegzetlocatie voor het ontvangen van inkooporders.</span><span class="sxs-lookup"><span data-stu-id="cd10d-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="cd10d-376">**LP:** de door het systeem gegenereerde nummerplaat-id</span><span class="sxs-lookup"><span data-stu-id="cd10d-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="cd10d-377">**Artikel:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="cd10d-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="cd10d-378">**Hoeveelheid:** *1 PL: 100 stuks*</span><span class="sxs-lookup"><span data-stu-id="cd10d-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="cd10d-379">De artikelomschrijving wordt ook weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-379">The item description is also shown.</span></span>

1. <span data-ttu-id="cd10d-380">Bevestig het wegzetwerk.</span><span class="sxs-lookup"><span data-stu-id="cd10d-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="cd10d-381">Op de pagina **Taak** voor het ontvangen van inkooporderregels wordt het bericht 'Werk voltooid' weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd10d-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="cd10d-382">Het veld **Regelnummer** is beschikbaar zodat u de volgende pallet kunt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="cd10d-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="cd10d-383">Selecteer de menuknop ( **≡** ) boven aan de pagina en selecteer vervolgens in het menu de optie **Annuleren** om terug te keren naar het menu.</span><span class="sxs-lookup"><span data-stu-id="cd10d-383">Select the Menu button ( **≡** ) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="cd10d-384">U kunt nu de mobiele app sluiten.</span><span class="sxs-lookup"><span data-stu-id="cd10d-384">You can now close the mobile app.</span></span>
