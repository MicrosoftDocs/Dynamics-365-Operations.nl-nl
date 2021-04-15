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
ms.openlocfilehash: 49807c90c145eee55fae2d515fd19925eb2d944c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810409"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="d944c-104">Gepland cross-docken</span><span class="sxs-lookup"><span data-stu-id="d944c-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d944c-105">In dit onderwerp wordt geavanceerd gepland cross-docking beschreven.</span><span class="sxs-lookup"><span data-stu-id="d944c-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="d944c-106">Cross-docking is een magazijnproces waarbij de voorraadhoeveelheid die nodig is voor een order rechtstreeks van ontvangst of maken naar het juiste outbound dock of klaarzetlocatie wordt gestuurd.</span><span class="sxs-lookup"><span data-stu-id="d944c-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="d944c-107">Alle resterende voorraad uit de inkomende bron wordt via het normale wegzetproces naar de juiste opslaglocatie gestuurd.</span><span class="sxs-lookup"><span data-stu-id="d944c-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="d944c-108">Bij cross-docken kunnen de werknemers het wegzetten van inkomende artikelen en het verzamelen voor uitgaande artikelen overslaan voor voorraat die al voor een uitgaande order is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="d944c-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="d944c-109">Zo wordt het aantal aanrakingsmomenten voor voorraad waar mogelijk zo klein mogelijk gehouden.</span><span class="sxs-lookup"><span data-stu-id="d944c-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="d944c-110">Omdat er minder interactie is met het systeem, kan worden bespaard op tijd en ruimte op de magazijnvloer.</span><span class="sxs-lookup"><span data-stu-id="d944c-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="d944c-111">Voordat cross-docken kan worden uitgevoerd, moet de gebruiker een nieuwe sjabloon voor cross-docken configureren, waarin de voorraadbron en andere reeksen vereisten voor cross-docken worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="d944c-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="d944c-112">Wanneer de uitgaande order wordt gemaakt, moet de regel worden gemarkeerd voor een inkomende order die hetzelfde artikel bevat.</span><span class="sxs-lookup"><span data-stu-id="d944c-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="d944c-113">Bij ontvangst van inkomende orders identificeert de cross-dockingconfiguratie automatisch dat cross-docken vereist is, en maakt het werk aan voor verplaatsing van de vereiste hoeveelheid op basis van de configuratie van de locatie-instructie.</span><span class="sxs-lookup"><span data-stu-id="d944c-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="d944c-114">Registratie van voorraadtransacties wordt **niet** ongedaan gemaakt wanneer het cross-dockingwerk wordt geannuleerd, zelfs als de instelling voor deze mogelijkheid is ingeschakeld in de parameters van magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="d944c-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="d944c-115">De functies voor gepland cross-docken inschakelen</span><span class="sxs-lookup"><span data-stu-id="d944c-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="d944c-116">Als de functies die in dit onderwerp worden beschreven, nog niet in het systeem aanwezig zijn, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de volgende functies in de volgende volgorde in:</span><span class="sxs-lookup"><span data-stu-id="d944c-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="d944c-117">*Gepland cross-docken*</span><span class="sxs-lookup"><span data-stu-id="d944c-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="d944c-118">*Sjablonen met locatie-instructies voor cross-docken*</span><span class="sxs-lookup"><span data-stu-id="d944c-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="d944c-119">Instelling</span><span class="sxs-lookup"><span data-stu-id="d944c-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="d944c-120">Boekingsmethoden voor lading opnieuw genereren</span><span class="sxs-lookup"><span data-stu-id="d944c-120">Regenerate load posting methods</span></span>

<span data-ttu-id="d944c-121">Gepland cross-docken wordt geïmplementeerd als een boekingsmethode voor lading.</span><span class="sxs-lookup"><span data-stu-id="d944c-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="d944c-122">Nadat u de functie hebt ingeschakeld, moet u de methoden opnieuw genereren.</span><span class="sxs-lookup"><span data-stu-id="d944c-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="d944c-123">Ga naar **Magazijnbeheer \> Instellen \> Boekingsmethoden voor lading**.</span><span class="sxs-lookup"><span data-stu-id="d944c-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="d944c-124">Selecteer in het actievenster **Methoden opnieuw genereren**.</span><span class="sxs-lookup"><span data-stu-id="d944c-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="d944c-125">Wanneer de regeneratie is voltooid, moet u een methode met de **methodenaam** *planCrossDocking* zien.</span><span class="sxs-lookup"><span data-stu-id="d944c-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="d944c-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d944c-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="d944c-127">Een cross-dockingsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="d944c-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="d944c-128">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Sjablonen voor cross-docken**.</span><span class="sxs-lookup"><span data-stu-id="d944c-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="d944c-129">Selecteer in het actievenster **Nieuw** om een sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="d944c-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="d944c-130">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="d944c-131">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="d944c-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="d944c-132">Dit veld bepaalt de volgorde waarin sjablonen worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="d944c-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="d944c-133">**Id van cross-dockingsjabloon:** *51*</span><span class="sxs-lookup"><span data-stu-id="d944c-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="d944c-134">**Beschrijving:** *Magazijn 51*</span><span class="sxs-lookup"><span data-stu-id="d944c-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="d944c-135">**Beleid voor vraagvrijgave:** *Voor ontvangst van levering*</span><span class="sxs-lookup"><span data-stu-id="d944c-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="d944c-136">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="d944c-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d944c-137">De instellingen op het sneltabblad **Planning** bepalen hoe de sjabloon werkt.</span><span class="sxs-lookup"><span data-stu-id="d944c-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="d944c-138">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-138">Set the following values:</span></span>

    - <span data-ttu-id="d944c-139">**Vereisten voor vraag:** *geen*</span><span class="sxs-lookup"><span data-stu-id="d944c-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="d944c-140">In dit veld worden de vereisten van de vraagvoorraad gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d944c-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="d944c-141">Als de vraag vóór vrijgave moet worden gekoppeld aan de levering, selecteert u *Markering*.</span><span class="sxs-lookup"><span data-stu-id="d944c-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="d944c-142">Selecteer *Orderreservering* als de vraag vóór vrijgave moet worden gereserveerd voor de levering.</span><span class="sxs-lookup"><span data-stu-id="d944c-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="d944c-143">**Lokaliseringstype:** *Verzendlocaties*</span><span class="sxs-lookup"><span data-stu-id="d944c-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="d944c-144">In dit veld wordt gedefinieerd of het werk voor cross-docken de klaarzet/ladinglocaties van de zending moet gebruiken of naar de locatie-instructies moet kijken om zelf een klaarzet-/ladinglocatie te vinden.</span><span class="sxs-lookup"><span data-stu-id="d944c-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="d944c-145">**Werksjabloon**: Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="d944c-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="d944c-146">In dit veld wordt de werksjabloon gedefinieerd die moet worden gebruikt bij het maken van cross-dockingwerk.</span><span class="sxs-lookup"><span data-stu-id="d944c-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="d944c-147">**Opnieuw valideren bij ontvangst levering:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="d944c-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="d944c-148">Met deze optie wordt bepaald of de levering opnieuw moet worden gevalideerd tijdens de ontvangst.</span><span class="sxs-lookup"><span data-stu-id="d944c-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="d944c-149">Als deze optie is ingesteld op *Ja*, worden zowel het maximumtijdvenster als het bereik voor vervaldagen gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d944c-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="d944c-150">**Instructiecode:** laat dit veld leeg</span><span class="sxs-lookup"><span data-stu-id="d944c-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="d944c-151">Met deze optie is het systeem in staat om locatie-instructies te gebruiken om de beste locatie te bepalen waar de voorraad voor cross-docken naartoe kan worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="d944c-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="d944c-152">U kunt de optie instellen door een instructiecode toe te wijzen aan elke relevante sjabloon voor cross-docken.</span><span class="sxs-lookup"><span data-stu-id="d944c-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="d944c-153">Elke instructiecode duidt een unieke locatie-instructie aan.</span><span class="sxs-lookup"><span data-stu-id="d944c-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="d944c-154">**Tijdvenster valideren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d944c-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="d944c-155">Met deze optie wordt bepaald of het maximumtijdvenster moet worden geëvalueerd wanneer een voorraadbron wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="d944c-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="d944c-156">Als deze optie is ingesteld op *Ja*, worden de velden die zijn gerelateerd aan de maximum- en minimumtijdvensters beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="d944c-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="d944c-157">**Maximumtijdvenster:** *5*</span><span class="sxs-lookup"><span data-stu-id="d944c-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="d944c-158">In dit veld wordt de maximale periode gedefinieerd die is toegestaan tussen aankomst van een levering en vertrek van gevraagde artikelen.</span><span class="sxs-lookup"><span data-stu-id="d944c-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d944c-159">**Eenheid maximumtijdvenster:** *Dagen*</span><span class="sxs-lookup"><span data-stu-id="d944c-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d944c-160">**Minimumtijdvenster:** *0*</span><span class="sxs-lookup"><span data-stu-id="d944c-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="d944c-161">In dit veld wordt de minimale periode gedefinieerd die is toegestaan tussen aankomst van een levering en vertrek van gevraagde artikelen.</span><span class="sxs-lookup"><span data-stu-id="d944c-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d944c-162">**Eenheid minimumtijdvenster:** *Dagen*</span><span class="sxs-lookup"><span data-stu-id="d944c-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d944c-163">**Bereik vervaldagen:** *0*</span><span class="sxs-lookup"><span data-stu-id="d944c-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="d944c-164">*Criteria voor FEFO (First Expiry, First Out):* De waarde in dit veld bepaalt het maximumaantal dagen tussen de vervaldatum van de eerste batch die zich momenteel in het magazijn bevindt en de batch die wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d944c-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="d944c-165">Op het sneltabblad **Leveringsbronnen** geeft u de typen leveringen op die geldig zijn voor deze sjabloon.</span><span class="sxs-lookup"><span data-stu-id="d944c-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="d944c-166">Selecteer **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d944c-167">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d944c-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d944c-168">**Leveringsbron:** *Inkooporder*</span><span class="sxs-lookup"><span data-stu-id="d944c-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="d944c-169">Een werkklasse maken</span><span class="sxs-lookup"><span data-stu-id="d944c-169">Create a work class</span></span>

1. <span data-ttu-id="d944c-170">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.</span><span class="sxs-lookup"><span data-stu-id="d944c-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d944c-171">Selecteer in het actievenster **Nieuw** om een werkklasse te maken.</span><span class="sxs-lookup"><span data-stu-id="d944c-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="d944c-172">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-172">Set the following values:</span></span>

    - <span data-ttu-id="d944c-173">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d944c-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d944c-174">**Beschrijving:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="d944c-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="d944c-175">**Werkordertype:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="d944c-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="d944c-176">Een werksjabloon maken</span><span class="sxs-lookup"><span data-stu-id="d944c-176">Create a work template</span></span>

1. <span data-ttu-id="d944c-177">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="d944c-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d944c-178">Stel het veld **Werkordertype** in op *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="d944c-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d944c-179">Selecteer in het actievenster de optie **Nieuw** om een regel toe te voegen aan het tabblad **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="d944c-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="d944c-180">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d944c-181">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d944c-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d944c-182">**Werksjabloon:** *51 Cross-dock*</span><span class="sxs-lookup"><span data-stu-id="d944c-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="d944c-183">**Beschrijving werksjabloon:** *51 Cross-dock*</span><span class="sxs-lookup"><span data-stu-id="d944c-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="d944c-184">Selecteer **Opslaan** om het sneltabblad **Werksjabloongegevens** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d944c-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="d944c-185">Ga naar het sneltabblad **Werksjabloongegeven** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="d944c-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d944c-186">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d944c-187">**Werktype:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="d944c-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d944c-188">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d944c-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d944c-189">Selecteer **Nieuw** om nog een regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="d944c-190">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="d944c-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d944c-191">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d944c-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d944c-192">Selecteer **Opslaan** en bevestig dat het selectievakje **Geldig** is ingeschakeld voor de sjabloon *51 Cross-docken*.</span><span class="sxs-lookup"><span data-stu-id="d944c-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="d944c-193">De werkklasse-id's voor de werktypen *Verzamelen* en *Wegzetten* moeten hetzelfde zijn.</span><span class="sxs-lookup"><span data-stu-id="d944c-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="d944c-194">Maak locatie-instructies aan</span><span class="sxs-lookup"><span data-stu-id="d944c-194">Create location directives</span></span>

1. <span data-ttu-id="d944c-195">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="d944c-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d944c-196">Stel in het linkerdeelvenster het veld **Werkordertype** in op *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="d944c-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d944c-197">Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="d944c-198">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d944c-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d944c-199">**Naam:** *51 cross-docken voor wegzetten*</span><span class="sxs-lookup"><span data-stu-id="d944c-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="d944c-200">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="d944c-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d944c-201">**Locatie:** *5*</span><span class="sxs-lookup"><span data-stu-id="d944c-201">**Site:** *5*</span></span>
    - <span data-ttu-id="d944c-202">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="d944c-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d944c-203">Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d944c-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d944c-204">Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="d944c-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d944c-205">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d944c-206">**Vanaf hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="d944c-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="d944c-207">**Tot hoeveelheid:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d944c-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="d944c-208">Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d944c-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d944c-209">Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="d944c-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d944c-210">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d944c-211">**Naam:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="d944c-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="d944c-212">**Gebruik vaste locaties:** *Vaste en niet-vaste locaties*</span><span class="sxs-lookup"><span data-stu-id="d944c-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="d944c-213">Selecteer **Opslaan** om de knop **Query bewerken** op de werkbalk **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="d944c-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="d944c-214">Selecteer **Query bewerken** om de query-editor te openen.</span><span class="sxs-lookup"><span data-stu-id="d944c-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="d944c-215">Controleer of op het tabblad **Bereik** de volgende twee regels zijn geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="d944c-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="d944c-216">Regel 1:</span><span class="sxs-lookup"><span data-stu-id="d944c-216">Line 1:</span></span>

        - <span data-ttu-id="d944c-217">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="d944c-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d944c-218">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="d944c-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d944c-219">**Veld:** *Magazijn*</span><span class="sxs-lookup"><span data-stu-id="d944c-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="d944c-220">**Criteria:** *51*</span><span class="sxs-lookup"><span data-stu-id="d944c-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="d944c-221">Regel 2:</span><span class="sxs-lookup"><span data-stu-id="d944c-221">Line 2:</span></span>

        - <span data-ttu-id="d944c-222">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="d944c-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d944c-223">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="d944c-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d944c-224">**Veld:** *Locatie*</span><span class="sxs-lookup"><span data-stu-id="d944c-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="d944c-225">**Criteria:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="d944c-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="d944c-226">Selecteer **OK** om de query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="d944c-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d944c-227">Een menuopdracht van mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="d944c-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d944c-228">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="d944c-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d944c-229">Selecteer in de lijst met menuopdrachten in het linkerdeelvenster de optie **Opslag van inkoop**.</span><span class="sxs-lookup"><span data-stu-id="d944c-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="d944c-230">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d944c-230">Select **Edit**.</span></span>
1. <span data-ttu-id="d944c-231">Ga naar het sneltabblad **Werkklassen** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="d944c-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d944c-232">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d944c-233">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d944c-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d944c-234">**Werkordertype:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="d944c-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="d944c-235">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d944c-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d944c-236">Scenario's</span><span class="sxs-lookup"><span data-stu-id="d944c-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="d944c-237">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="d944c-237">Create a purchase order</span></span>

<span data-ttu-id="d944c-238">Volg deze stappen om een inkooporder te maken als leveringsbron.</span><span class="sxs-lookup"><span data-stu-id="d944c-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="d944c-239">Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="d944c-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d944c-240">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d944c-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d944c-241">Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d944c-242">**Leverancierrekening:** *104*</span><span class="sxs-lookup"><span data-stu-id="d944c-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="d944c-243">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="d944c-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d944c-244">Selecteer **OK** en noteer het ordernummer.</span><span class="sxs-lookup"><span data-stu-id="d944c-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="d944c-245">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Inkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="d944c-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="d944c-246">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="d944c-247">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d944c-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d944c-248">**Hoeveelheid:** *5*</span><span class="sxs-lookup"><span data-stu-id="d944c-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="d944c-249">Verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="d944c-249">Create a sales order</span></span>

<span data-ttu-id="d944c-250">Volg deze stappen om een verkooporder te maken als een bron van vraag.</span><span class="sxs-lookup"><span data-stu-id="d944c-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="d944c-251">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="d944c-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d944c-252">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="d944c-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d944c-253">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d944c-254">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d944c-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="d944c-255">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="d944c-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d944c-256">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d944c-256">Select **OK**.</span></span>
1. <span data-ttu-id="d944c-257">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="d944c-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d944c-258">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="d944c-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="d944c-259">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d944c-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d944c-260">**Hoeveelheid:** *3*</span><span class="sxs-lookup"><span data-stu-id="d944c-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="d944c-261">Gepland cross-docken maken</span><span class="sxs-lookup"><span data-stu-id="d944c-261">Create planned cross-docking</span></span>

<span data-ttu-id="d944c-262">Volg deze stappen om het geplande cross-docken te maken vanuit de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d944c-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="d944c-263">Ga naar de pagina **Verkooporderdetails** voor de verkooporder die u zojuist hebt gemaakt. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="d944c-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d944c-264">Met de actie Vrijgeven naar magazijn wordt een zending- en laadregel gemaakt voor de verkooporderregel en wordt geprobeerd om voorraad toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="d944c-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="d944c-265">U ontvangt een melding.</span><span class="sxs-lookup"><span data-stu-id="d944c-265">You receive an informational message.</span></span> <span data-ttu-id="d944c-266">Ook wordt het volgende waarschuwingsbericht weergegeven: "Er is geen werk gemaakt voor wave XXXX.</span><span class="sxs-lookup"><span data-stu-id="d944c-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="d944c-267">Zie het logbestand voor werk aanmaken voor meer informatie."</span><span class="sxs-lookup"><span data-stu-id="d944c-267">See the work creation history log for details."</span></span> <span data-ttu-id="d944c-268">Dit gedrag is verwacht, omdat het magazijn geen voorraad bevat.</span><span class="sxs-lookup"><span data-stu-id="d944c-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="d944c-269">Selecteer op het sneltabblad **Verkooporderregels** in het menu **Magazijn** boven het raster de waarde **Details van zending**.</span><span class="sxs-lookup"><span data-stu-id="d944c-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="d944c-270">De pagina **Details van zending** wordt weergegeven en toont de zending die voor de verkooporder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d944c-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="d944c-271">In het sneltabblad **Ladingsregels** ziet u dat het veld **Hoeveelheid voor gepland cross-docken** is ingesteld op *3*.</span><span class="sxs-lookup"><span data-stu-id="d944c-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="d944c-272">Omdat er in het magazijn geen voorraad beschikbaar was, maar een geldige leveringsbron zal aankomen binnen het tijdvenster dat is gedefinieerd in de sjabloon voor cross-docken, is de hoeveelheid voor cross-docken gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d944c-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="d944c-273">Selecteer op het sneltabblad **Ladingsregels** de optie **Gepland cross-docken** om de details weer te geven van de aangemaakte cross-docking.</span><span class="sxs-lookup"><span data-stu-id="d944c-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="d944c-274">De cross-docking verwerken</span><span class="sxs-lookup"><span data-stu-id="d944c-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="d944c-275">Nummerplaat ontvangen in de mobiele magazijnapp</span><span class="sxs-lookup"><span data-stu-id="d944c-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="d944c-276">Het systeem ontvangt de 5 stuks van de inkooporder op de ontvangende locatie en er wordt twee keer werk aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="d944c-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="d944c-277">De eerste werk-id die wordt gemaakt, heeft als **werkordertype** *Cross-docken* en is gekoppeld aan de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d944c-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="d944c-278">De id heeft een hoeveelheid van 3 en wordt naar de uiteindelijke verzendlocatie gestuurd, zodat deze direct kan worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="d944c-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="d944c-279">De tweede werk-id die wordt gemaakt, heeft als **werkordertype** *Inkooporders* en is gekoppeld aan de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="d944c-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="d944c-280">Het bevat de resterende hoeveelheid van 2 die niet is gecross-docked en die moet worden weggezet in opslag.</span><span class="sxs-lookup"><span data-stu-id="d944c-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="d944c-281">Meld u aan bij het mobiele apparaat als een gebruiker in magazijn *51*.</span><span class="sxs-lookup"><span data-stu-id="d944c-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="d944c-282">Ga naar **Inkomend \> Inkoop ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="d944c-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="d944c-283">Voer in het veld **Inkoopordernummer** het inkoopordernummer in.</span><span class="sxs-lookup"><span data-stu-id="d944c-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="d944c-284">Voer in het veld **Hoeveelheid** de waarde *5* in.</span><span class="sxs-lookup"><span data-stu-id="d944c-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="d944c-285">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d944c-285">Select **OK**.</span></span>
1. <span data-ttu-id="d944c-286">Stel op de volgende pagina het veld **Artikel** in op *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d944c-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="d944c-287">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d944c-287">Select **OK**.</span></span>
1. <span data-ttu-id="d944c-288">Bevestig op de volgende pagina de waarden voor **Inkoopordernummer** , **Artikel** en **Hoeveelheid** door op **OK** te klikken.</span><span class="sxs-lookup"><span data-stu-id="d944c-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="d944c-289">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="d944c-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d944c-290">Selecteer **Annuleren** om af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="d944c-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="d944c-291">Wegzetten voor cross-docking en bulk</span><span class="sxs-lookup"><span data-stu-id="d944c-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="d944c-292">Momenteel hebben beide werk-id's dezelfde doelnummerplaat.</span><span class="sxs-lookup"><span data-stu-id="d944c-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="d944c-293">Om de volgende stappen uit te voeren, moet u de werk-id en de doelnummerplaat-id ophalen.</span><span class="sxs-lookup"><span data-stu-id="d944c-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="d944c-294">U kunt deze informatie ophalen uit de werkgegevens voor de inkooporderregel en de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="d944c-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="d944c-295">U kunt ook naar **Magazijnbeheer \> Werk \> Werkdetails** gaan en filteren op werk waar de waarde van **Magazijn** is ingesteld op *51*.</span><span class="sxs-lookup"><span data-stu-id="d944c-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="d944c-296">Ga op het mobiele apparaat naar de **Inkomend \> Opslag van inkoop** en voer het nummer van de doelnummerplaat van het werk in.</span><span class="sxs-lookup"><span data-stu-id="d944c-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="d944c-297">Voer in het veld **Id** de identificatiecode voor de doelnummerplaat uit de werkdetails in.</span><span class="sxs-lookup"><span data-stu-id="d944c-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="d944c-298">Op de pagina voor cross-dockingverzamelen worden de orderverzamellocatie (*RECV*), de doelnummerplaat (*nummerplaat*), het artikel (*A0001*) en de hoeveelheid (*3*) getoond.</span><span class="sxs-lookup"><span data-stu-id="d944c-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="d944c-299">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d944c-299">Select **OK**.</span></span>
1. <span data-ttu-id="d944c-300">Voer in het veld **Doel-NP** een doelnummerplaat in voor de nummerplaat-id die moet worden weggezet (cross-docked) naar de verzendlocatie.</span><span class="sxs-lookup"><span data-stu-id="d944c-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="d944c-301">U kunt elke gewenste nummerplaat-id selecteren.</span><span class="sxs-lookup"><span data-stu-id="d944c-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="d944c-302">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d944c-302">Select **OK**.</span></span>
1. <span data-ttu-id="d944c-303">Voer op de volgende pagina in het veld **Id** de identificatiecode voor de doelnummerplaat in.</span><span class="sxs-lookup"><span data-stu-id="d944c-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="d944c-304">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d944c-304">Select **OK**.</span></span>
1. <span data-ttu-id="d944c-305">Bevestig het werk voor het verzamelen van de resterende hoeveelheid van 2 en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d944c-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="d944c-306">Selecteer op de volgende pagina **Gereed** om het orderverzamelproces te beëindigen en het wegzetproces te starten.</span><span class="sxs-lookup"><span data-stu-id="d944c-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="d944c-307">De mobiele app geeft u de locatie en de nummerplaat weer waarop u het artikel kunt wegzetten.</span><span class="sxs-lookup"><span data-stu-id="d944c-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="d944c-308">Bevestig de bulkopslag **Wegzetten** door **OK** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="d944c-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="d944c-309">Bevestig op de volgende pagina de cross-docking **Wegzetten** door op **OK** te klikken.</span><span class="sxs-lookup"><span data-stu-id="d944c-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="d944c-310">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="d944c-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d944c-311">Selecteer **Annuleren** om af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="d944c-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="d944c-312">In de volgende afbeelding wordt weergegeven hoe het voltooide cross-dockingwerk kan worden weergegeven in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d944c-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d944c-313">![Cross-dockingwerk voltooid](media/PlannedCrossDockingWork.png "Cross-dockingwerk voltooid")</span><span class="sxs-lookup"><span data-stu-id="d944c-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]