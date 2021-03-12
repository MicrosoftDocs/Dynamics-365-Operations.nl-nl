---
title: Gepland cross-docken
description: In dit onderwerp wordt geavanceerd gepland cross-docking beschreven, waarbij de voorraadhoeveelheid die nodig is voor een order rechtstreeks van ontvangst of maken naar het juiste outbound dock of klaarzetlocatie wordt gestuurd. Alle resterende voorraad uit de inkomende bron wordt via het normale wegzetproces naar de juiste opslaglocatie gestuurd.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: fb598b3ac7dd72e8c500f0c2eaf07462009c67f7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970301"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="dfc04-104">Gepland cross-docken</span><span class="sxs-lookup"><span data-stu-id="dfc04-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfc04-105">In dit onderwerp wordt geavanceerd gepland cross-docking beschreven.</span><span class="sxs-lookup"><span data-stu-id="dfc04-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="dfc04-106">Cross-docking is een magazijnproces waarbij de voorraadhoeveelheid die nodig is voor een order rechtstreeks van ontvangst of maken naar het juiste outbound dock of klaarzetlocatie wordt gestuurd.</span><span class="sxs-lookup"><span data-stu-id="dfc04-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="dfc04-107">Alle resterende voorraad uit de inkomende bron wordt via het normale wegzetproces naar de juiste opslaglocatie gestuurd.</span><span class="sxs-lookup"><span data-stu-id="dfc04-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="dfc04-108">Bij cross-docken kunnen de werknemers het wegzetten van inkomende artikelen en het verzamelen voor uitgaande artikelen overslaan voor voorraat die al voor een uitgaande order is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="dfc04-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="dfc04-109">Zo wordt het aantal aanrakingsmomenten voor voorraad waar mogelijk zo klein mogelijk gehouden.</span><span class="sxs-lookup"><span data-stu-id="dfc04-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="dfc04-110">Omdat er minder interactie is met het systeem, kan worden bespaard op tijd en ruimte op de magazijnvloer.</span><span class="sxs-lookup"><span data-stu-id="dfc04-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="dfc04-111">Voordat cross-docken kan worden uitgevoerd, moet de gebruiker een nieuwe sjabloon voor cross-docken configureren, waarin de voorraadbron en andere reeksen vereisten voor cross-docken worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="dfc04-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="dfc04-112">Wanneer de uitgaande order wordt gemaakt, moet de regel worden gemarkeerd voor een inkomende order die hetzelfde artikel bevat.</span><span class="sxs-lookup"><span data-stu-id="dfc04-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="dfc04-113">Bij ontvangst van inkomende orders identificeert de cross-dockingconfiguratie automatisch dat cross-docken vereist is, en maakt het werk aan voor verplaatsing van de vereiste hoeveelheid op basis van de configuratie van de locatie-instructie.</span><span class="sxs-lookup"><span data-stu-id="dfc04-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="dfc04-114">Registratie van voorraadtransacties wordt **niet** ongedaan gemaakt wanneer het cross-dockingwerk wordt geannuleerd, zelfs als de instelling voor deze mogelijkheid is ingeschakeld in de parameters van magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="dfc04-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="dfc04-115">De functie Gepland cross-docken inschakelen</span><span class="sxs-lookup"><span data-stu-id="dfc04-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="dfc04-116">Voordat u geavanceerd gepland cross-docken kunt gebruiken, moet de functie zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="dfc04-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="dfc04-117">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="dfc04-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="dfc04-118">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="dfc04-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="dfc04-119">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="dfc04-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="dfc04-120">**Functienaam:** *Gepland cross-docken*</span><span class="sxs-lookup"><span data-stu-id="dfc04-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="dfc04-121">Instellen</span><span class="sxs-lookup"><span data-stu-id="dfc04-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="dfc04-122">Boekingsmethoden voor lading opnieuw genereren</span><span class="sxs-lookup"><span data-stu-id="dfc04-122">Regenerate load posting methods</span></span>

<span data-ttu-id="dfc04-123">Gepland cross-docken wordt geïmplementeerd als een boekingsmethode voor lading.</span><span class="sxs-lookup"><span data-stu-id="dfc04-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="dfc04-124">Nadat u de functie hebt ingeschakeld, moet u de methoden opnieuw genereren.</span><span class="sxs-lookup"><span data-stu-id="dfc04-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="dfc04-125">Ga naar **Magazijnbeheer \> Instellen \> Boekingsmethoden voor lading**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="dfc04-126">Selecteer in het actievenster **Methoden opnieuw genereren**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="dfc04-127">Wanneer de regeneratie is voltooid, moet u een methode met de **methodenaam** *planCrossDocking* zien.</span><span class="sxs-lookup"><span data-stu-id="dfc04-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="dfc04-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="dfc04-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="dfc04-129">Een cross-dockingsjabloon maken</span><span class="sxs-lookup"><span data-stu-id="dfc04-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="dfc04-130">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Sjablonen voor cross-docken**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="dfc04-131">Selecteer in het actievenster **Nieuw** om een sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="dfc04-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="dfc04-132">Stel in de koptekst de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="dfc04-133">**Reeks:** *1*</span><span class="sxs-lookup"><span data-stu-id="dfc04-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="dfc04-134">Dit veld bepaalt de volgorde waarin sjablonen worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="dfc04-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="dfc04-135">**Id van cross-dockingsjabloon:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc04-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="dfc04-136">**Beschrijving:** *Magazijn 51*</span><span class="sxs-lookup"><span data-stu-id="dfc04-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="dfc04-137">**Beleid voor vraagvrijgave:** *Voor ontvangst van levering*</span><span class="sxs-lookup"><span data-stu-id="dfc04-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="dfc04-138">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc04-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="dfc04-139">De instellingen op het sneltabblad **Planning** bepalen hoe de sjabloon werkt.</span><span class="sxs-lookup"><span data-stu-id="dfc04-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="dfc04-140">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-140">Set the following values:</span></span>

    - <span data-ttu-id="dfc04-141">**Vereisten voor vraag:** *geen*</span><span class="sxs-lookup"><span data-stu-id="dfc04-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="dfc04-142">In dit veld worden de vereisten van de vraagvoorraad gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="dfc04-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="dfc04-143">Als de vraag vóór vrijgave moet worden gekoppeld aan de levering, selecteert u *Markering*.</span><span class="sxs-lookup"><span data-stu-id="dfc04-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="dfc04-144">Selecteer *Orderreservering* als de vraag vóór vrijgave moet worden gereserveerd voor de levering.</span><span class="sxs-lookup"><span data-stu-id="dfc04-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="dfc04-145">**Lokaliseringstype:** *Verzendlocaties*</span><span class="sxs-lookup"><span data-stu-id="dfc04-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="dfc04-146">In dit veld wordt gedefinieerd of het werk voor cross-docken de klaarzet/ladinglocaties van de zending moet gebruiken of naar de locatie-instructies moet kijken om zelf een klaarzet-/ladinglocatie te vinden.</span><span class="sxs-lookup"><span data-stu-id="dfc04-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="dfc04-147">**Werksjabloon**: Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="dfc04-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="dfc04-148">In dit veld wordt de werksjabloon gedefinieerd die moet worden gebruikt bij het maken van cross-dockingwerk.</span><span class="sxs-lookup"><span data-stu-id="dfc04-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="dfc04-149">**Opnieuw valideren bij ontvangst levering:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="dfc04-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="dfc04-150">Met deze optie wordt bepaald of de levering opnieuw moet worden gevalideerd tijdens de ontvangst.</span><span class="sxs-lookup"><span data-stu-id="dfc04-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="dfc04-151">Als deze optie is ingesteld op *Ja*, worden zowel het maximumtijdvenster als het bereik voor vervaldagen gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="dfc04-151">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="dfc04-152">**Tijdvenster valideren:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="dfc04-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="dfc04-153">Met deze optie wordt bepaald of het maximumtijdvenster moet worden geëvalueerd wanneer een voorraadbron wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="dfc04-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="dfc04-154">Als deze optie is ingesteld op *Ja*, worden de velden die zijn gerelateerd aan de maximum- en minimumtijdvensters beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="dfc04-154">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="dfc04-155">**Maximumtijdvenster:** *5*</span><span class="sxs-lookup"><span data-stu-id="dfc04-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="dfc04-156">In dit veld wordt de maximale periode gedefinieerd die is toegestaan tussen aankomst van een levering en vertrek van gevraagde artikelen.</span><span class="sxs-lookup"><span data-stu-id="dfc04-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="dfc04-157">**Eenheid maximumtijdvenster:** *Dagen*</span><span class="sxs-lookup"><span data-stu-id="dfc04-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="dfc04-158">**Minimumtijdvenster:** *0*</span><span class="sxs-lookup"><span data-stu-id="dfc04-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="dfc04-159">In dit veld wordt de minimale periode gedefinieerd die is toegestaan tussen aankomst van een levering en vertrek van gevraagde artikelen.</span><span class="sxs-lookup"><span data-stu-id="dfc04-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="dfc04-160">**Eenheid minimumtijdvenster:** *Dagen*</span><span class="sxs-lookup"><span data-stu-id="dfc04-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="dfc04-161">**Bereik vervaldagen:** *0*</span><span class="sxs-lookup"><span data-stu-id="dfc04-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="dfc04-162">*Criteria voor FEFO (First Expiry, First Out):* De waarde in dit veld bepaalt het maximumaantal dagen tussen de vervaldatum van de eerste batch die zich momenteel in het magazijn bevindt en de batch die wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="dfc04-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="dfc04-163">Op het sneltabblad **Leveringsbronnen** geeft u de typen leveringen op die geldig zijn voor deze sjabloon.</span><span class="sxs-lookup"><span data-stu-id="dfc04-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="dfc04-164">Selecteer **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-164">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="dfc04-165">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="dfc04-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="dfc04-166">**Leveringsbron:** *Inkooporder*</span><span class="sxs-lookup"><span data-stu-id="dfc04-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="dfc04-167">Een werkklasse maken</span><span class="sxs-lookup"><span data-stu-id="dfc04-167">Create a work class</span></span>

1. <span data-ttu-id="dfc04-168">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="dfc04-169">Selecteer in het actievenster **Nieuw** om een werkklasse te maken.</span><span class="sxs-lookup"><span data-stu-id="dfc04-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="dfc04-170">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-170">Set the following values:</span></span>

    - <span data-ttu-id="dfc04-171">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="dfc04-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="dfc04-172">**Beschrijving:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="dfc04-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="dfc04-173">**Werkordertype:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="dfc04-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="dfc04-174">Een werksjabloon maken</span><span class="sxs-lookup"><span data-stu-id="dfc04-174">Create a work template</span></span>

1. <span data-ttu-id="dfc04-175">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="dfc04-176">Stel het veld **Werkordertype** in op *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="dfc04-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="dfc04-177">Selecteer in het actievenster de optie **Nieuw** om een regel toe te voegen aan het tabblad **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="dfc04-178">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc04-179">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="dfc04-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="dfc04-180">**Werksjabloon:** *51 Cross-dock*</span><span class="sxs-lookup"><span data-stu-id="dfc04-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="dfc04-181">**Beschrijving werksjabloon:** *51 Cross-dock*</span><span class="sxs-lookup"><span data-stu-id="dfc04-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="dfc04-182">Selecteer **Opslaan** om het sneltabblad **Werksjabloongegevens** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="dfc04-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="dfc04-183">Ga naar het sneltabblad **Werksjabloongegeven** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="dfc04-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="dfc04-184">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc04-185">**Werktype:** *Orderverzamelen*</span><span class="sxs-lookup"><span data-stu-id="dfc04-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="dfc04-186">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="dfc04-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="dfc04-187">Selecteer **Nieuw** om nog een regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="dfc04-188">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="dfc04-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="dfc04-189">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="dfc04-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="dfc04-190">Selecteer **Opslaan** en bevestig dat het selectievakje **Geldig** is ingeschakeld voor de sjabloon *51 Cross-docken*.</span><span class="sxs-lookup"><span data-stu-id="dfc04-190">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="dfc04-191">De werkklasse-id's voor de werktypen *Verzamelen* en *Wegzetten* moeten hetzelfde zijn.</span><span class="sxs-lookup"><span data-stu-id="dfc04-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="dfc04-192">Maak locatie-instructies aan</span><span class="sxs-lookup"><span data-stu-id="dfc04-192">Create location directives</span></span>

1. <span data-ttu-id="dfc04-193">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="dfc04-194">Stel in het linkerdeelvenster het veld **Werkordertype** in op *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="dfc04-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="dfc04-195">Selecteer in het actievenster **Nieuw** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-195">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="dfc04-196">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="dfc04-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="dfc04-197">**Naam:** *51 cross-docken voor wegzetten*</span><span class="sxs-lookup"><span data-stu-id="dfc04-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="dfc04-198">**Werktype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="dfc04-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="dfc04-199">**Locatie:** *5*</span><span class="sxs-lookup"><span data-stu-id="dfc04-199">**Site:** *5*</span></span>
    - <span data-ttu-id="dfc04-200">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc04-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="dfc04-201">Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="dfc04-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="dfc04-202">Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="dfc04-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="dfc04-203">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc04-204">**Vanaf hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="dfc04-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="dfc04-205">**Tot hoeveelheid:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="dfc04-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="dfc04-206">Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="dfc04-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="dfc04-207">Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="dfc04-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="dfc04-208">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc04-209">**Naam:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="dfc04-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="dfc04-210">**Gebruik vaste locaties:** *Vaste en niet-vaste locaties*</span><span class="sxs-lookup"><span data-stu-id="dfc04-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="dfc04-211">Selecteer **Opslaan** om de knop **Query bewerken** op de werkbalk **Locatie-instructieacties** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="dfc04-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="dfc04-212">Selecteer **Query bewerken** om de query-editor te openen.</span><span class="sxs-lookup"><span data-stu-id="dfc04-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="dfc04-213">Controleer of op het tabblad **Bereik** de volgende twee regels zijn geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="dfc04-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="dfc04-214">Regel 1:</span><span class="sxs-lookup"><span data-stu-id="dfc04-214">Line 1:</span></span>

        - <span data-ttu-id="dfc04-215">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="dfc04-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="dfc04-216">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="dfc04-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="dfc04-217">**Veld:** *Magazijn*</span><span class="sxs-lookup"><span data-stu-id="dfc04-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="dfc04-218">**Criteria:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc04-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="dfc04-219">Regel 2:</span><span class="sxs-lookup"><span data-stu-id="dfc04-219">Line 2:</span></span>

        - <span data-ttu-id="dfc04-220">**Tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="dfc04-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="dfc04-221">**Afgeleide tabel:** *Locaties*</span><span class="sxs-lookup"><span data-stu-id="dfc04-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="dfc04-222">**Veld:** *Locatie*</span><span class="sxs-lookup"><span data-stu-id="dfc04-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="dfc04-223">**Criteria:** *Laaddeur*</span><span class="sxs-lookup"><span data-stu-id="dfc04-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="dfc04-224">Selecteer **OK** om de query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="dfc04-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="dfc04-225">Een menuopdracht van mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="dfc04-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="dfc04-226">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="dfc04-227">Selecteer in de lijst met menuopdrachten in het linkerdeelvenster de optie **Opslag van inkoop**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="dfc04-228">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-228">Select **Edit**.</span></span>
1. <span data-ttu-id="dfc04-229">Ga naar het sneltabblad **Werkklassen** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="dfc04-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="dfc04-230">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc04-231">**Werkklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="dfc04-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="dfc04-232">**Werkordertype:** *Cross-docken*</span><span class="sxs-lookup"><span data-stu-id="dfc04-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="dfc04-233">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="dfc04-234">Scenario's</span><span class="sxs-lookup"><span data-stu-id="dfc04-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="dfc04-235">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="dfc04-235">Create a purchase order</span></span>

<span data-ttu-id="dfc04-236">Volg deze stappen om een inkooporder te maken als leveringsbron.</span><span class="sxs-lookup"><span data-stu-id="dfc04-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="dfc04-237">Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="dfc04-238">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="dfc04-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dfc04-239">Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dfc04-240">**Leverancierrekening:** *104*</span><span class="sxs-lookup"><span data-stu-id="dfc04-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="dfc04-241">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc04-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="dfc04-242">Selecteer **OK** en noteer het ordernummer.</span><span class="sxs-lookup"><span data-stu-id="dfc04-242">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="dfc04-243">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Inkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="dfc04-244">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="dfc04-245">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="dfc04-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="dfc04-246">**Hoeveelheid:** *5*</span><span class="sxs-lookup"><span data-stu-id="dfc04-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="dfc04-247">Verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="dfc04-247">Create a sales order</span></span>

<span data-ttu-id="dfc04-248">Volg deze stappen om een verkooporder te maken als een bron van vraag.</span><span class="sxs-lookup"><span data-stu-id="dfc04-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="dfc04-249">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="dfc04-250">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="dfc04-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dfc04-251">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dfc04-252">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="dfc04-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="dfc04-253">**Magazijn:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc04-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="dfc04-254">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-254">Select **OK**.</span></span>
1. <span data-ttu-id="dfc04-255">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dfc04-256">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="dfc04-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="dfc04-257">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="dfc04-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="dfc04-258">**Hoeveelheid:** *3*</span><span class="sxs-lookup"><span data-stu-id="dfc04-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="dfc04-259">Gepland cross-docken maken</span><span class="sxs-lookup"><span data-stu-id="dfc04-259">Create planned cross-docking</span></span>

<span data-ttu-id="dfc04-260">Volg deze stappen om het geplande cross-docken te maken vanuit de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="dfc04-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="dfc04-261">Ga naar de pagina **Verkooporderdetails** voor de verkooporder die u zojuist hebt gemaakt. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="dfc04-262">Met de actie Vrijgeven naar magazijn wordt een zending- en laadregel gemaakt voor de verkooporderregel en wordt geprobeerd om voorraad toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="dfc04-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="dfc04-263">U ontvangt een melding.</span><span class="sxs-lookup"><span data-stu-id="dfc04-263">You receive an informational message.</span></span> <span data-ttu-id="dfc04-264">Ook wordt het volgende waarschuwingsbericht weergegeven: "Er is geen werk gemaakt voor wave XXXX.</span><span class="sxs-lookup"><span data-stu-id="dfc04-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="dfc04-265">Zie het logbestand voor werk aanmaken voor meer informatie."</span><span class="sxs-lookup"><span data-stu-id="dfc04-265">See the work creation history log for details."</span></span> <span data-ttu-id="dfc04-266">Dit gedrag is verwacht, omdat het magazijn geen voorraad bevat.</span><span class="sxs-lookup"><span data-stu-id="dfc04-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="dfc04-267">Selecteer op het sneltabblad **Verkooporderregels** in het menu **Magazijn** boven het raster de waarde **Details van zending**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="dfc04-268">De pagina **Details van zending** wordt weergegeven en toont de zending die voor de verkooporder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dfc04-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="dfc04-269">In het sneltabblad **Ladingsregels** ziet u dat het veld **Hoeveelheid voor gepland cross-docken** is ingesteld op *3*.</span><span class="sxs-lookup"><span data-stu-id="dfc04-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="dfc04-270">Omdat er in het magazijn geen voorraad beschikbaar was, maar een geldige leveringsbron zal aankomen binnen het tijdvenster dat is gedefinieerd in de sjabloon voor cross-docken, is de hoeveelheid voor cross-docken gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dfc04-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="dfc04-271">Selecteer op het sneltabblad **Ladingsregels** de optie **Gepland cross-docken** om de details weer te geven van de aangemaakte cross-docking.</span><span class="sxs-lookup"><span data-stu-id="dfc04-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="dfc04-272">De cross-docking verwerken</span><span class="sxs-lookup"><span data-stu-id="dfc04-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="dfc04-273">Nummerplaat ontvangen in de mobiele magazijnapp</span><span class="sxs-lookup"><span data-stu-id="dfc04-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="dfc04-274">Het systeem ontvangt de 5 stuks van de inkooporder op de ontvangende locatie en er wordt twee keer werk aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="dfc04-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="dfc04-275">De eerste werk-id die wordt gemaakt, heeft als **werkordertype** *Cross-docken* en is gekoppeld aan de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="dfc04-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="dfc04-276">De id heeft een hoeveelheid van 3 en wordt naar de uiteindelijke verzendlocatie gestuurd, zodat deze direct kan worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="dfc04-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="dfc04-277">De tweede werk-id die wordt gemaakt, heeft als **werkordertype** *Inkooporders* en is gekoppeld aan de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="dfc04-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="dfc04-278">Het bevat de resterende hoeveelheid van 2 die niet is gecross-docked en die moet worden weggezet in opslag.</span><span class="sxs-lookup"><span data-stu-id="dfc04-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="dfc04-279">Meld u aan bij het mobiele apparaat als een gebruiker in magazijn *51*.</span><span class="sxs-lookup"><span data-stu-id="dfc04-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="dfc04-280">Ga naar **Inkomend \> Inkoop ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="dfc04-281">Voer in het veld **Inkoopordernummer** het inkoopordernummer in.</span><span class="sxs-lookup"><span data-stu-id="dfc04-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="dfc04-282">Voer in het veld **Hoeveelheid** de waarde *5* in.</span><span class="sxs-lookup"><span data-stu-id="dfc04-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="dfc04-283">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-283">Select **OK**.</span></span>
1. <span data-ttu-id="dfc04-284">Stel op de volgende pagina het veld **Artikel** in op *A0001*.</span><span class="sxs-lookup"><span data-stu-id="dfc04-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="dfc04-285">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-285">Select **OK**.</span></span>
1. <span data-ttu-id="dfc04-286">Bevestig op de volgende pagina de waarden voor **Inkoopordernummer** , **Artikel** en **Hoeveelheid** door op **OK** te klikken.</span><span class="sxs-lookup"><span data-stu-id="dfc04-286">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="dfc04-287">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="dfc04-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="dfc04-288">Selecteer **Annuleren** om af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="dfc04-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="dfc04-289">Wegzetten voor cross-docking en bulk</span><span class="sxs-lookup"><span data-stu-id="dfc04-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="dfc04-290">Momenteel hebben beide werk-id's dezelfde doelnummerplaat.</span><span class="sxs-lookup"><span data-stu-id="dfc04-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="dfc04-291">Om de volgende stappen uit te voeren, moet u de werk-id en de doelnummerplaat-id ophalen.</span><span class="sxs-lookup"><span data-stu-id="dfc04-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="dfc04-292">U kunt deze informatie ophalen uit de werkgegevens voor de inkooporderregel en de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="dfc04-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="dfc04-293">U kunt ook naar **Magazijnbeheer \> Werk \> Werkdetails** gaan en filteren op werk waar de waarde van **Magazijn** is ingesteld op *51*.</span><span class="sxs-lookup"><span data-stu-id="dfc04-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="dfc04-294">Ga op het mobiele apparaat naar de **Inkomend \> Opslag van inkoop** en voer het nummer van de doelnummerplaat van het werk in.</span><span class="sxs-lookup"><span data-stu-id="dfc04-294">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="dfc04-295">Voer in het veld **Id** de identificatiecode voor de doelnummerplaat uit de werkdetails in.</span><span class="sxs-lookup"><span data-stu-id="dfc04-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="dfc04-296">Op de pagina voor cross-dockingverzamelen worden de orderverzamellocatie (*RECV*), de doelnummerplaat (*nummerplaat*), het artikel (*A0001*) en de hoeveelheid (*3*) getoond.</span><span class="sxs-lookup"><span data-stu-id="dfc04-296">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="dfc04-297">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-297">Select **OK**.</span></span>
1. <span data-ttu-id="dfc04-298">Voer in het veld **Doel-NP** een doelnummerplaat in voor de nummerplaat-id die moet worden weggezet (cross-docked) naar de verzendlocatie.</span><span class="sxs-lookup"><span data-stu-id="dfc04-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="dfc04-299">U kunt elke gewenste nummerplaat-id selecteren.</span><span class="sxs-lookup"><span data-stu-id="dfc04-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="dfc04-300">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-300">Select **OK**.</span></span>
1. <span data-ttu-id="dfc04-301">Voer op de volgende pagina in het veld **Id** de identificatiecode voor de doelnummerplaat in.</span><span class="sxs-lookup"><span data-stu-id="dfc04-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="dfc04-302">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-302">Select **OK**.</span></span>
1. <span data-ttu-id="dfc04-303">Bevestig het werk voor het verzamelen van de resterende hoeveelheid van 2 en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc04-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="dfc04-304">Selecteer op de volgende pagina **Gereed** om het orderverzamelproces te beëindigen en het wegzetproces te starten.</span><span class="sxs-lookup"><span data-stu-id="dfc04-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="dfc04-305">De mobiele app geeft u de locatie en de nummerplaat weer waarop u het artikel kunt wegzetten.</span><span class="sxs-lookup"><span data-stu-id="dfc04-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="dfc04-306">Bevestig de bulkopslag **Wegzetten** door **OK** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="dfc04-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="dfc04-307">Bevestig op de volgende pagina de cross-docking **Wegzetten** door op **OK** te klikken.</span><span class="sxs-lookup"><span data-stu-id="dfc04-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="dfc04-308">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="dfc04-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="dfc04-309">Selecteer **Annuleren** om af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="dfc04-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="dfc04-310">In de volgende afbeelding wordt weergegeven hoe het voltooide cross-dockingwerk kan worden weergegeven in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dfc04-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="dfc04-311">![Cross-dockingwerk voltooid](media/PlannedCrossDockingWork.png "Cross-dockingwerk voltooid")</span><span class="sxs-lookup"><span data-stu-id="dfc04-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
