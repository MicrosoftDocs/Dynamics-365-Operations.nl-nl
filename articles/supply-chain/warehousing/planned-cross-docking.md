---
title: Gepland cross-docken
description: In dit onderwerp wordt geavanceerd gepland cross-docking beschreven, waarbij de voorraadhoeveelheid die nodig is voor een order rechtstreeks van ontvangst of maken naar het juiste outbound dock of klaarzetlocatie wordt gestuurd. Alle resterende voorraad uit de inkomende bron wordt via het normale wegzetproces naar de juiste opslaglocatie gestuurd.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911243"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="4d74a-104">Gepland cross-docken</span><span class="sxs-lookup"><span data-stu-id="4d74a-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d74a-105">In dit onderwerp wordt geavanceerd gepland cross-docking beschreven.</span><span class="sxs-lookup"><span data-stu-id="4d74a-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="4d74a-106">Cross-docking is een magazijnproces waarbij de voorraadhoeveelheid die nodig is voor een order rechtstreeks van ontvangst of maken naar het juiste outbound dock of klaarzetlocatie wordt gestuurd.</span><span class="sxs-lookup"><span data-stu-id="4d74a-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="4d74a-107">Alle resterende voorraad uit de inkomende bron wordt via het normale wegzetproces naar de juiste opslaglocatie gestuurd.</span><span class="sxs-lookup"><span data-stu-id="4d74a-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="4d74a-108">Bij cross-docken kunnen de werknemers het wegzetten van inkomende artikelen en het verzamelen voor uitgaande artikelen overslaan voor voorraat die al voor een uitgaande order is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="4d74a-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="4d74a-109">Zo wordt het aantal aanrakingsmomenten voor voorraad waar mogelijk zo klein mogelijk gehouden.</span><span class="sxs-lookup"><span data-stu-id="4d74a-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="4d74a-110">Omdat er minder interactie is met het systeem, kan worden bespaard op tijd en ruimte op de magazijnvloer.</span><span class="sxs-lookup"><span data-stu-id="4d74a-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="4d74a-111">Voordat u cross-docken kunt uitvoeren, moet u een nieuwe sjabloon voor cross-docken configureren, waarin de voorraadbron en andere reeksen vereisten voor cross-docken worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="4d74a-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="4d74a-112">Wanneer de uitgaande order wordt gemaakt, moet de regel worden gemarkeerd voor een inkomende order die hetzelfde artikel bevat.</span><span class="sxs-lookup"><span data-stu-id="4d74a-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="4d74a-113">U kunt het veld met de richtlijncode selecteren in de sjabloon voor cross-docken, vergelijkbaar met de manier waarop u aanvullings- en inkooporders instelt.</span><span class="sxs-lookup"><span data-stu-id="4d74a-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="4d74a-114">Bij ontvangst van inkomende orders identificeert de cross-dockingconfiguratie automatisch dat cross-docken vereist is, en maakt het werk aan voor verplaatsing van de vereiste hoeveelheid op basis van de configuratie van de locatie-instructie.</span><span class="sxs-lookup"><span data-stu-id="4d74a-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="4d74a-115">Registratie van voorraadtransacties wordt *niet* ongedaan gemaakt wanneer het cross-dockingwerk wordt geannuleerd, zelfs als de instelling voor deze mogelijkheid is ingeschakeld in de parameters van magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="4d74a-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="4d74a-116">De functies voor gepland cross-docken inschakelen</span><span class="sxs-lookup"><span data-stu-id="4d74a-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="4d74a-117">Als de functies die in dit onderwerp worden beschreven, nog niet in het systeem aanwezig zijn, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de volgende functies in de volgende volgorde in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="4d74a-118">*Gepland cross-docken*</span><span class="sxs-lookup"><span data-stu-id="4d74a-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="4d74a-119">*Sjablonen met locatie-instructies voor cross-docken*</span><span class="sxs-lookup"><span data-stu-id="4d74a-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="4d74a-120">Met deze functie kunt u het veld **Richtlijncode** opgeven in de sjabloon voor cross-docken, vergelijkbaar met de manier waarop u aanvullingssjablonen instelt.</span><span class="sxs-lookup"><span data-stu-id="4d74a-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="4d74a-121">Als u deze functie inschakelt, kunt u geen richtlijncode toevoegen aan de regels van de werksjabloon voor cross-docken voor de laatste regel *Wegzetten*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="4d74a-122">Zo zorgt u ervoor dat de uiteindelijke plaats kan worden bepaald tijdens het maken van het werk voordat er werksjablonen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4d74a-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="4d74a-123">Instelling</span><span class="sxs-lookup"><span data-stu-id="4d74a-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="4d74a-124">Boekingsmethoden voor lading opnieuw genereren</span><span class="sxs-lookup"><span data-stu-id="4d74a-124">Regenerate load posting methods</span></span>

<span data-ttu-id="4d74a-125">Gepland cross-docken wordt geïmplementeerd als een boekingsmethode voor lading.</span><span class="sxs-lookup"><span data-stu-id="4d74a-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="4d74a-126">Nadat u de functie hebt ingeschakeld, moet u de methoden opnieuw genereren.</span><span class="sxs-lookup"><span data-stu-id="4d74a-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="4d74a-127">Ga naar **Magazijnbeheer \> Instellen \> Boekingsmethoden voor lading**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="4d74a-128">Selecteer in het actievenster **Methoden opnieuw genereren**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="4d74a-129">Wanneer de regeneratie is voltooid, moet u een methode met de **methodenaam** *planCrossDocking* zien.</span><span class="sxs-lookup"><span data-stu-id="4d74a-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="4d74a-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4d74a-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="4d74a-131">Een cross-dockingsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="4d74a-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="4d74a-132">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Sjablonen voor cross-docken**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="4d74a-133">Selecteer in het actievenster **Nieuw** om een sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="4d74a-134">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="4d74a-135">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d74a-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="4d74a-136">Dit veld bepaalt de volgorde waarin sjablonen worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="4d74a-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="4d74a-137">**Id van cross-dockingsjabloon:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d74a-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="4d74a-138">**Beschrijving:** *Magazijn 51*</span><span class="sxs-lookup"><span data-stu-id="4d74a-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="4d74a-139">**Beleid voor vraagvrijgave:** *Voor ontvangst van levering*</span><span class="sxs-lookup"><span data-stu-id="4d74a-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="4d74a-140">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d74a-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="4d74a-141">De instellingen op het sneltabblad **Planning** bepalen hoe de sjabloon werkt.</span><span class="sxs-lookup"><span data-stu-id="4d74a-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="4d74a-142">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-142">Set the following values:</span></span>

    - <span data-ttu-id="4d74a-143">**Vereisten voor vraag:** *geen*</span><span class="sxs-lookup"><span data-stu-id="4d74a-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="4d74a-144">In dit veld worden de vereisten van de vraagvoorraad gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="4d74a-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="4d74a-145">Als de vraag vóór vrijgave moet worden gekoppeld aan de levering, selecteert u *Markering*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="4d74a-146">Selecteer *Orderreservering* als de vraag vóór vrijgave moet worden gereserveerd voor de levering.</span><span class="sxs-lookup"><span data-stu-id="4d74a-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="4d74a-147">**Lokaliseringstype:** *Verzendlocaties*</span><span class="sxs-lookup"><span data-stu-id="4d74a-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="4d74a-148">In dit veld wordt gedefinieerd of het werk voor cross-docken de klaarzet/ladinglocaties van de zending moet gebruiken of naar de locatie-instructies moet kijken om zelf een klaarzet-/ladinglocatie te vinden.</span><span class="sxs-lookup"><span data-stu-id="4d74a-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="4d74a-149">**Werksjabloon**: Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="4d74a-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="4d74a-150">In dit veld wordt de werksjabloon gedefinieerd die moet worden gebruikt bij het maken van cross-dockingwerk.</span><span class="sxs-lookup"><span data-stu-id="4d74a-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="4d74a-151">**Opnieuw valideren bij ontvangst levering:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="4d74a-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="4d74a-152">Met deze optie wordt bepaald of de levering opnieuw moet worden gevalideerd tijdens de ontvangst.</span><span class="sxs-lookup"><span data-stu-id="4d74a-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="4d74a-153">Als deze optie is ingesteld op *Ja*, worden zowel het maximumtijdvenster als het bereik voor vervaldagen gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="4d74a-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="4d74a-154">**Instructiecode:** laat dit veld leeg</span><span class="sxs-lookup"><span data-stu-id="4d74a-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="4d74a-155">Deze optie wordt ingeschakeld door de functie *Sjablonen voor cross-docken met locatierichtlijnen*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="4d74a-156">Het systeem gebruikt locatierichtlijnen om de beste locatie te bepalen waar de voorraad voor cross-docken naartoe kan worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="4d74a-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="4d74a-157">U kunt de optie instellen door een instructiecode toe te wijzen aan elke relevante sjabloon voor cross-docken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="4d74a-158">Als er instructiecode is ingesteld, worden de locatie-instructies niet op volgorde doorzocht, maar wordt er op instructiecode gezocht wanneer werk wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="4d74a-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="4d74a-159">Op deze manier kunt u locatierichtlijnen beperken die voor een bepaalde sjabloon voor cross-docken worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4d74a-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="4d74a-160">**Tijdvenster valideren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="4d74a-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="4d74a-161">Met deze optie wordt bepaald of het maximumtijdvenster moet worden geëvalueerd wanneer een voorraadbron wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="4d74a-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="4d74a-162">Als deze optie is ingesteld op *Ja*, worden de velden die zijn gerelateerd aan de maximum- en minimumtijdvensters beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="4d74a-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="4d74a-163">**Maximumtijdvenster:** *5*</span><span class="sxs-lookup"><span data-stu-id="4d74a-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="4d74a-164">In dit veld wordt de maximale periode gedefinieerd die is toegestaan tussen aankomst van een levering en vertrek van gevraagde artikelen.</span><span class="sxs-lookup"><span data-stu-id="4d74a-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="4d74a-165">**Eenheid maximumtijdvenster:** *Dagen*</span><span class="sxs-lookup"><span data-stu-id="4d74a-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="4d74a-166">**Minimumtijdvenster:** *0*</span><span class="sxs-lookup"><span data-stu-id="4d74a-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="4d74a-167">In dit veld wordt de minimale periode gedefinieerd die is toegestaan tussen aankomst van een levering en vertrek van gevraagde artikelen.</span><span class="sxs-lookup"><span data-stu-id="4d74a-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="4d74a-168">**Eenheid minimumtijdvenster:** *Dagen*</span><span class="sxs-lookup"><span data-stu-id="4d74a-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="4d74a-169">**Bereik vervaldagen:** *0*</span><span class="sxs-lookup"><span data-stu-id="4d74a-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="4d74a-170">*Criteria voor FEFO (First Expiry, First Out):* De waarde in dit veld bepaalt het maximumaantal dagen tussen de vervaldatum van de eerste batch die zich momenteel in het magazijn bevindt en de batch die wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="4d74a-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="4d74a-171">Op het sneltabblad **Leveringsbronnen** geeft u de typen leveringen op die geldig zijn voor deze sjabloon.</span><span class="sxs-lookup"><span data-stu-id="4d74a-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="4d74a-172">Selecteer **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="4d74a-173">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d74a-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4d74a-174">**Leveringsbron:** *Inkooporder*</span><span class="sxs-lookup"><span data-stu-id="4d74a-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="4d74a-175">Een werkklasse maken</span><span class="sxs-lookup"><span data-stu-id="4d74a-175">Create a work class</span></span>

1. <span data-ttu-id="4d74a-176">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="4d74a-177">Selecteer in het actievenster **Nieuw** om een werkklasse te maken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="4d74a-178">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-178">Set the following values:</span></span>

    - <span data-ttu-id="4d74a-179">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="4d74a-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="4d74a-180">**Beschrijving:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="4d74a-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="4d74a-181">**Werkordertype:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="4d74a-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="4d74a-182">Een werksjabloon maken</span><span class="sxs-lookup"><span data-stu-id="4d74a-182">Create a work template</span></span>

1. <span data-ttu-id="4d74a-183">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="4d74a-184">Stel het veld **Werkordertype** in op *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="4d74a-185">Selecteer in het actievenster de optie **Nieuw** om een regel toe te voegen aan het tabblad **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="4d74a-186">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d74a-187">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d74a-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4d74a-188">**Werksjabloon:** *51 Cross-dock*</span><span class="sxs-lookup"><span data-stu-id="4d74a-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="4d74a-189">**Beschrijving werksjabloon:** *51 Cross-dock*</span><span class="sxs-lookup"><span data-stu-id="4d74a-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="4d74a-190">Selecteer **Opslaan** om het sneltabblad **Werksjabloongegevens** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="4d74a-191">Ga naar het sneltabblad **Werksjabloongegeven** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="4d74a-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4d74a-192">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d74a-193">**Werktype:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="4d74a-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="4d74a-194">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="4d74a-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="4d74a-195">Selecteer **Nieuw** om nog een regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="4d74a-196">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="4d74a-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="4d74a-197">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="4d74a-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="4d74a-198">Selecteer **Opslaan** en bevestig dat het selectievakje **Geldig** is ingeschakeld voor de sjabloon *51 Cross-docken*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="4d74a-199">De werkklasse-id's voor de werktypen *Verzamelen* en *Wegzetten* moeten hetzelfde zijn.</span><span class="sxs-lookup"><span data-stu-id="4d74a-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="4d74a-200">Maak locatie-instructies aan</span><span class="sxs-lookup"><span data-stu-id="4d74a-200">Create location directives</span></span>

1. <span data-ttu-id="4d74a-201">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="4d74a-202">Stel in het linkerdeelvenster het veld **Werkordertype** in op *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="4d74a-203">Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="4d74a-204">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d74a-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4d74a-205">**Naam:** *51 cross-docken voor wegzetten*</span><span class="sxs-lookup"><span data-stu-id="4d74a-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="4d74a-206">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="4d74a-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="4d74a-207">**Locatie:** *5*</span><span class="sxs-lookup"><span data-stu-id="4d74a-207">**Site:** *5*</span></span>
    - <span data-ttu-id="4d74a-208">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d74a-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="4d74a-209">Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="4d74a-210">Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="4d74a-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4d74a-211">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d74a-212">**Vanaf hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d74a-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="4d74a-213">**Tot hoeveelheid:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="4d74a-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="4d74a-214">Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="4d74a-215">Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="4d74a-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4d74a-216">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d74a-217">**Naam:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="4d74a-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="4d74a-218">**Gebruik vaste locaties:** *Vaste en niet-vaste locaties*</span><span class="sxs-lookup"><span data-stu-id="4d74a-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="4d74a-219">Selecteer **Opslaan** om de knop **Query bewerken** op de werkbalk **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="4d74a-220">Selecteer **Query bewerken** om de query-editor te openen.</span><span class="sxs-lookup"><span data-stu-id="4d74a-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="4d74a-221">Controleer of op het tabblad **Bereik** de volgende twee regels zijn geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="4d74a-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="4d74a-222">Regel 1:</span><span class="sxs-lookup"><span data-stu-id="4d74a-222">Line 1:</span></span>

        - <span data-ttu-id="4d74a-223">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="4d74a-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="4d74a-224">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="4d74a-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="4d74a-225">**Veld:** *Magazijn*</span><span class="sxs-lookup"><span data-stu-id="4d74a-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="4d74a-226">**Criteria:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d74a-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="4d74a-227">Regel 2:</span><span class="sxs-lookup"><span data-stu-id="4d74a-227">Line 2:</span></span>

        - <span data-ttu-id="4d74a-228">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="4d74a-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="4d74a-229">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="4d74a-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="4d74a-230">**Veld:** *Locatie*</span><span class="sxs-lookup"><span data-stu-id="4d74a-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="4d74a-231">**Criteria:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="4d74a-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="4d74a-232">Selecteer **OK** om de query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="4d74a-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="4d74a-233">Een menuopdracht van mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="4d74a-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="4d74a-234">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="4d74a-235">Selecteer in de lijst met menuopdrachten in het linkerdeelvenster de optie **Opslag van inkoop**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="4d74a-236">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-236">Select **Edit**.</span></span>
1. <span data-ttu-id="4d74a-237">Ga naar het sneltabblad **Werkklassen** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="4d74a-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4d74a-238">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d74a-239">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="4d74a-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="4d74a-240">**Werkordertype:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="4d74a-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="4d74a-241">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="4d74a-242">Scenario's</span><span class="sxs-lookup"><span data-stu-id="4d74a-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="4d74a-243">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="4d74a-243">Create a purchase order</span></span>

<span data-ttu-id="4d74a-244">Volg deze stappen om een inkooporder te maken als leveringsbron.</span><span class="sxs-lookup"><span data-stu-id="4d74a-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="4d74a-245">Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="4d74a-246">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4d74a-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4d74a-247">Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4d74a-248">**Leverancierrekening:** *104*</span><span class="sxs-lookup"><span data-stu-id="4d74a-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="4d74a-249">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d74a-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="4d74a-250">Selecteer **OK** en noteer het ordernummer.</span><span class="sxs-lookup"><span data-stu-id="4d74a-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="4d74a-251">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Inkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="4d74a-252">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="4d74a-253">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4d74a-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4d74a-254">**Hoeveelheid:** *5*</span><span class="sxs-lookup"><span data-stu-id="4d74a-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="4d74a-255">Verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="4d74a-255">Create a sales order</span></span>

<span data-ttu-id="4d74a-256">Volg deze stappen om een verkooporder te maken als een bron van vraag.</span><span class="sxs-lookup"><span data-stu-id="4d74a-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="4d74a-257">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4d74a-258">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4d74a-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4d74a-259">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4d74a-260">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="4d74a-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="4d74a-261">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d74a-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="4d74a-262">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-262">Select **OK**.</span></span>
1. <span data-ttu-id="4d74a-263">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4d74a-264">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4d74a-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="4d74a-265">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4d74a-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4d74a-266">**Hoeveelheid:** *3*</span><span class="sxs-lookup"><span data-stu-id="4d74a-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="4d74a-267">Gepland cross-docken maken</span><span class="sxs-lookup"><span data-stu-id="4d74a-267">Create planned cross-docking</span></span>

<span data-ttu-id="4d74a-268">Volg deze stappen om het geplande cross-docken te maken vanuit de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4d74a-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="4d74a-269">Ga naar de pagina **Verkooporderdetails** voor de verkooporder die u zojuist hebt gemaakt. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4d74a-270">Met de actie Vrijgeven naar magazijn wordt een zending- en laadregel gemaakt voor de verkooporderregel en wordt geprobeerd om voorraad toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="4d74a-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="4d74a-271">U ontvangt een melding.</span><span class="sxs-lookup"><span data-stu-id="4d74a-271">You receive an informational message.</span></span> <span data-ttu-id="4d74a-272">Ook wordt het volgende waarschuwingsbericht weergegeven: "Er is geen werk gemaakt voor wave XXXX.</span><span class="sxs-lookup"><span data-stu-id="4d74a-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="4d74a-273">Zie het logbestand voor werk aanmaken voor meer informatie."</span><span class="sxs-lookup"><span data-stu-id="4d74a-273">See the work creation history log for details."</span></span> <span data-ttu-id="4d74a-274">Dit gedrag is verwacht, omdat het magazijn geen voorraad bevat.</span><span class="sxs-lookup"><span data-stu-id="4d74a-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="4d74a-275">Selecteer op het sneltabblad **Verkooporderregels** in het menu **Magazijn** boven het raster de waarde **Details van zending**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="4d74a-276">De pagina **Details van zending** wordt weergegeven en toont de zending die voor de verkooporder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4d74a-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="4d74a-277">In het sneltabblad **Ladingsregels** ziet u dat het veld **Hoeveelheid voor gepland cross-docken** is ingesteld op *3*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="4d74a-278">Omdat er in het magazijn geen voorraad beschikbaar was, maar een geldige leveringsbron zal aankomen binnen het tijdvenster dat is gedefinieerd in de sjabloon voor cross-docken, is de hoeveelheid voor cross-docken gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4d74a-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="4d74a-279">Selecteer op het sneltabblad **Ladingsregels** de optie **Gepland cross-docken** om de details weer te geven van de aangemaakte cross-docking.</span><span class="sxs-lookup"><span data-stu-id="4d74a-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="4d74a-280">De cross-docking verwerken</span><span class="sxs-lookup"><span data-stu-id="4d74a-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="4d74a-281">Nummerplaat ontvangen in de mobiele magazijnapp</span><span class="sxs-lookup"><span data-stu-id="4d74a-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="4d74a-282">Het systeem ontvangt de 5 stuks van de inkooporder op de ontvangende locatie en er wordt twee keer werk aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="4d74a-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="4d74a-283">De eerste werk-id die wordt gemaakt, heeft als **werkordertype** *Cross-docken* en is gekoppeld aan de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4d74a-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="4d74a-284">De id heeft een hoeveelheid van 3 en wordt naar de uiteindelijke verzendlocatie gestuurd, zodat deze direct kan worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="4d74a-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="4d74a-285">De tweede werk-id die wordt gemaakt, heeft als **werkordertype** *Inkooporders* en is gekoppeld aan de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="4d74a-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="4d74a-286">Het bevat de resterende hoeveelheid van 2 die niet is gecross-docked en die moet worden weggezet in opslag.</span><span class="sxs-lookup"><span data-stu-id="4d74a-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="4d74a-287">Meld u aan bij het mobiele apparaat als een gebruiker in magazijn *51*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="4d74a-288">Ga naar **Inkomend \> Inkoop ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="4d74a-289">Voer in het veld **Inkoopordernummer** het inkoopordernummer in.</span><span class="sxs-lookup"><span data-stu-id="4d74a-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="4d74a-290">Voer in het veld **Hoeveelheid** de waarde *5* in.</span><span class="sxs-lookup"><span data-stu-id="4d74a-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="4d74a-291">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-291">Select **OK**.</span></span>
1. <span data-ttu-id="4d74a-292">Stel op de volgende pagina het veld **Artikel** in op *A0001*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="4d74a-293">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-293">Select **OK**.</span></span>
1. <span data-ttu-id="4d74a-294">Bevestig op de volgende pagina de waarden voor **Inkoopordernummer** , **Artikel** en **Hoeveelheid** door op **OK** te klikken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="4d74a-295">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="4d74a-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="4d74a-296">Selecteer **Annuleren** om af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="4d74a-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="4d74a-297">Wegzetten voor cross-docking en bulk</span><span class="sxs-lookup"><span data-stu-id="4d74a-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="4d74a-298">Momenteel hebben beide werk-id's dezelfde doelnummerplaat.</span><span class="sxs-lookup"><span data-stu-id="4d74a-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="4d74a-299">Om de volgende stappen uit te voeren, moet u de werk-id en de doelnummerplaat-id ophalen.</span><span class="sxs-lookup"><span data-stu-id="4d74a-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="4d74a-300">U kunt deze informatie ophalen uit de werkgegevens voor de inkooporderregel en de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="4d74a-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="4d74a-301">U kunt ook naar **Magazijnbeheer \> Werk \> Werkdetails** gaan en filteren op werk waar de waarde van **Magazijn** is ingesteld op *51*.</span><span class="sxs-lookup"><span data-stu-id="4d74a-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="4d74a-302">Ga op het mobiele apparaat naar de **Inkomend \> Opslag van inkoop** en voer het nummer van de doelnummerplaat van het werk in.</span><span class="sxs-lookup"><span data-stu-id="4d74a-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="4d74a-303">Voer in het veld **Id** de identificatiecode voor de doelnummerplaat uit de werkdetails in.</span><span class="sxs-lookup"><span data-stu-id="4d74a-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="4d74a-304">Op de pagina voor cross-dockingverzamelen worden de orderverzamellocatie (*RECV*), de doelnummerplaat (*nummerplaat*), het artikel (*A0001*) en de hoeveelheid (*3*) getoond.</span><span class="sxs-lookup"><span data-stu-id="4d74a-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="4d74a-305">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-305">Select **OK**.</span></span>
1. <span data-ttu-id="4d74a-306">Voer in het veld **Doel-NP** een doelnummerplaat in voor de nummerplaat-id die moet worden weggezet (cross-docked) naar de verzendlocatie.</span><span class="sxs-lookup"><span data-stu-id="4d74a-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="4d74a-307">U kunt elke gewenste nummerplaat-id selecteren.</span><span class="sxs-lookup"><span data-stu-id="4d74a-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="4d74a-308">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-308">Select **OK**.</span></span>
1. <span data-ttu-id="4d74a-309">Voer op de volgende pagina in het veld **Id** de identificatiecode voor de doelnummerplaat in.</span><span class="sxs-lookup"><span data-stu-id="4d74a-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="4d74a-310">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-310">Select **OK**.</span></span>
1. <span data-ttu-id="4d74a-311">Bevestig het werk voor het verzamelen van de resterende hoeveelheid van 2 en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d74a-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="4d74a-312">Selecteer op de volgende pagina **Gereed** om het orderverzamelproces te beëindigen en het wegzetproces te starten.</span><span class="sxs-lookup"><span data-stu-id="4d74a-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="4d74a-313">De mobiele app geeft u de locatie en de nummerplaat weer waarop u het artikel kunt wegzetten.</span><span class="sxs-lookup"><span data-stu-id="4d74a-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="4d74a-314">Bevestig de bulkopslag **Wegzetten** door **OK** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="4d74a-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="4d74a-315">Bevestig op de volgende pagina de cross-docking **Wegzetten** door op **OK** te klikken.</span><span class="sxs-lookup"><span data-stu-id="4d74a-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="4d74a-316">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="4d74a-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="4d74a-317">Selecteer **Annuleren** om af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="4d74a-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="4d74a-318">In de volgende afbeelding wordt weergegeven hoe het voltooide cross-dockingwerk kan worden weergegeven in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4d74a-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="4d74a-319">![Cross-dockingwerk voltooid](media/PlannedCrossDockingWork.png "Cross-dockingwerk voltooid")</span><span class="sxs-lookup"><span data-stu-id="4d74a-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]