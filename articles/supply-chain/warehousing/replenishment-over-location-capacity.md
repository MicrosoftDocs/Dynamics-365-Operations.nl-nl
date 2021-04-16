---
title: Aanvulling boven locatiecapaciteit
description: Dit onderwerp biedt informatie over de functie Aanvulling boven locatiecapaciteit. Deze functie schakelt alle aanvullingswerk in dat nodig is voor de dag om te worden gemaakt en beheert de beschikbaarheid van dat aanvullingswerk om ervoor te zorgen dat de verzamellocatie niet door voorraad heen raakt en ook niet boven de capaciteit komt.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 309df56671bf258e1669ae6d5393de01e2b500f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823234"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="4edbb-104">Aanvulling boven locatiecapaciteit</span><span class="sxs-lookup"><span data-stu-id="4edbb-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4edbb-105">In sommige magazijnen met een groot volume of weinig ruimte moeten meer artikelen in een dag worden verzonden dan op de verzamellocatie passen.</span><span class="sxs-lookup"><span data-stu-id="4edbb-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="4edbb-106">De functie *Aanvulling boven locatiecapaciteit* schakelt alle aanvullingswerk in dat nodig is voor de dag om te worden gemaakt en beheert de beschikbaarheid van dat aanvullingswerk om ervoor te zorgen dat de verzamellocatie niet door voorraad heenraakt en ook niet boven de capaciteit komt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="4edbb-107">Met de functie kan meer aanvullingswerk worden gemaakt dan op een locatie past en wordt voltooiing van aanvullingswerk geblokkeerd wanneer de locatie vol is.</span><span class="sxs-lookup"><span data-stu-id="4edbb-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="4edbb-108">Als voorraad op de verzamellocatie daalt onder een configureerbare drempel, wordt meer aanvullingswerk beschikbaar gesteld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="4edbb-109">De functie Aanvulling boven locatiecapaciteit inschakelen</span><span class="sxs-lookup"><span data-stu-id="4edbb-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="4edbb-110">Als u deze functie beschikbaar wilt maken, schakelt u de volgende functies in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in (in deze volgorde):</span><span class="sxs-lookup"><span data-stu-id="4edbb-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="4edbb-111">Werk blokkeren voor de hele organisatie</span><span class="sxs-lookup"><span data-stu-id="4edbb-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="4edbb-112">Aanvulling boven locatiecapaciteit</span><span class="sxs-lookup"><span data-stu-id="4edbb-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="4edbb-113">De functie instellen voor het voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="4edbb-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="4edbb-114">Deze sectie bevat richtlijnen en een voorbeeld waarin wordt uitgelegd hoe u deze functie instelt en voorbeeldgegevens voorbereidt voor het voorbeeldscenario dat verderop in dit onderwerp wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="4edbb-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="4edbb-115">Voorbeeldgegevens inschakelen</span><span class="sxs-lookup"><span data-stu-id="4edbb-115">Enable sample data</span></span>

<span data-ttu-id="4edbb-116">Als u het [voorbeeldscenario](#example-scenario) wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="4edbb-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="4edbb-117">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="4edbb-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="4edbb-118">Locatieprofiel</span><span class="sxs-lookup"><span data-stu-id="4edbb-118">Location profile</span></span>

<span data-ttu-id="4edbb-119">Schakel de functionaliteit voor aanvulling boven capaciteit in het locatieprofiel in.</span><span class="sxs-lookup"><span data-stu-id="4edbb-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="4edbb-120">Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="4edbb-121">Selecteer **PICK-06** in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="4edbb-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="4edbb-122">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4edbb-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4edbb-123">Stel op het sneltabblad **Aanvulling** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4edbb-124">**Locatiecapaciteit overschrijven:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="4edbb-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="4edbb-125">Indien ingeschakeld, mag de maximale capaciteit van de locatie worden overschreden door aanvullingswerk.</span><span class="sxs-lookup"><span data-stu-id="4edbb-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="4edbb-126">Hierdoor worden ook andere velden op het sneltabblad **Aanvulling** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="4edbb-127">**Drempeltype werkbeschikbaarheid:** *Hoeveelheid*</span><span class="sxs-lookup"><span data-stu-id="4edbb-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="4edbb-128">Dit veld bepaalt de methode die wordt gebruikt om te bepalen wanneer meer werk moet worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="4edbb-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="4edbb-129">U kunt vrijgeven op hoeveelheid of percentage:</span><span class="sxs-lookup"><span data-stu-id="4edbb-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="4edbb-130">*Percentage*: selecteer deze optie om percentagecapaciteit te gebruiken die is gebaseerd op voorraadlimieten of volumes.</span><span class="sxs-lookup"><span data-stu-id="4edbb-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="4edbb-131">Als u deze optie selecteert , wordt het veld **Overschrijdingspercentage** ingeschakeld en worden de twee hoeveelheidsvelden, **Overschrijdingshoeveelheid** en **Overschrijdingseenheid** uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="4edbb-132">U kunt deze optie gebruiken als de verzamellocaties volumes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="4edbb-133">Als deze optie is geselecteerd, stelt u het veld **Overschrijdingspercentage** in op het percentage waarbij meer aanvullingswerk beschikbaar wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="4edbb-134">*Hoeveelheid*: selecteer deze optie om een specifieke hoeveelheidswaarde te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="4edbb-135">Als u deze optie selecteert , wordt het veld **Overschrijdingspercentage** uitgeschakeld en worden de twee hoeveelheidsvelden, **Overschrijdingshoeveelheid** en **Overschrijdingseenheid** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="4edbb-136">Gebruik deze optie wanneer u geen volumes gebruikt voor de locaties die worden aangevuld, of wanneer u consistente hoeveelheden hebt waarbij meer voorraad naar de locatie moet worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="4edbb-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="4edbb-137">Als deze optie is geselecteerd, stelt u de velden **Overschrijdingshoeveelheid** en **Overschrijdingseenheid** in op de hoeveelheid waarbij meer aanvullingswerk beschikbaar wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="4edbb-138">**Overschrijdingshoeveelheid:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="4edbb-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="4edbb-139">In dit veld wordt de hoeveelheid gedefinieerd waarbij de locatie overloopt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="4edbb-140">Werk is beschikbaar wanneer de som van de voorhanden voorraad op de locatie en de werkhoeveelheid onder deze waarde ligt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="4edbb-141">Aanvullingswerk dat boven deze waarde ligt, wordt geblokkeerd en moet handmatig worden gedeblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="4edbb-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="4edbb-142">Met locatievoorraadlimieten wordt rekening gehouden wanneer de werkhoeveelheid wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="4edbb-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="4edbb-143">**Overschrijdingseenheid:** *PL*</span><span class="sxs-lookup"><span data-stu-id="4edbb-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="4edbb-144">In dit veld wordt de eenheid gedefinieerd die aan de overschrijdingseenheid is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="4edbb-145">In dit geval wordt meer aanvullingswerk beschikbaar gesteld wanneer de locatie zakt tot 0,65 pallet (PL).</span><span class="sxs-lookup"><span data-stu-id="4edbb-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="4edbb-146">**Overlooppercentage**</span><span class="sxs-lookup"><span data-stu-id="4edbb-146">**Overflow percentage**</span></span>

        <span data-ttu-id="4edbb-147">In dit veld wordt het percentage gedefinieerd waarbij de locatie overloopt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="4edbb-148">Werk is beschikbaar wanneer de som van de voorhanden voorraad op de locatie en de werkhoeveelheid onder dit percentage ligt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="4edbb-149">Een hoeveelheidspercentage aanvullingswerk dat boven deze waarde ligt, wordt geblokkeerd en moet handmatig worden gedeblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="4edbb-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="4edbb-150">Met locatievoorraadlimieten wordt rekening gehouden wanneer het percentage wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="4edbb-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="4edbb-151">Als er geen locatievoorraadlimieten zijn gedefinieerd, wordt het percentage werkhoeveelheid berekend op basis van volume als volumebeperkingen voor het locatieprofiel zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="4edbb-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4edbb-152">Als u de demogegevens voor de rechtspersoon **USMF** gebruikt en eerder de functie *Positionering van locatie nummerplaat* hebt ingeschakeld , moet u de instelling **Positionering van nummerplaat inschakelen** uitschakelen voor het locatieprofiel **BULK-06** om de mobiele stappen in het voorbeeldscenario te voltooien.</span><span class="sxs-lookup"><span data-stu-id="4edbb-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="4edbb-153">Stapcode wave</span><span class="sxs-lookup"><span data-stu-id="4edbb-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="4edbb-154">Als u een wave-stapcode wilt instellen, zoals hier wordt beschreven, moet u eerst [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de functie in te schakelen met de naam *Organisatiebrede wave-stapcode inschakelen*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="4edbb-155">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wave-stapcodes**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="4edbb-156">Selecteer **Nieuwe** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="4edbb-157">**Wave-stapcode:** *Aanvulling*</span><span class="sxs-lookup"><span data-stu-id="4edbb-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="4edbb-158">**Beschrijving wavestap:** *Aanvulling*</span><span class="sxs-lookup"><span data-stu-id="4edbb-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="4edbb-159">**Type wavestap:** *Aanvulling*</span><span class="sxs-lookup"><span data-stu-id="4edbb-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="4edbb-160">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="4edbb-161">Aanvullingssjabloon</span><span class="sxs-lookup"><span data-stu-id="4edbb-161">Replenishment template</span></span>

<span data-ttu-id="4edbb-162">Aanvullingssjablonen zijn een set regels die bepalen wanneer en hoe een locatie wordt aangevuld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="4edbb-163">Ga naar **Magazijnbeheer \> Instellen \> Aanvulling \> Aanvullingssjablonen**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="4edbb-164">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4edbb-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4edbb-165">Selecteer in de sectie **Overzicht** de regel waar het veld **Aanvullingssjabloon** is ingesteld op *Vraag aanvullen*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="4edbb-166">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-166">Set the following values:</span></span>

    - <span data-ttu-id="4edbb-167">**Wave-stapcode:** *Aanvulling*</span><span class="sxs-lookup"><span data-stu-id="4edbb-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="4edbb-168">**Gebruik van niet-gereserveerde hoeveelheid door waveaanvraag toestaan:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="4edbb-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="4edbb-169">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="4edbb-170">Wavesjabloon</span><span class="sxs-lookup"><span data-stu-id="4edbb-170">Wave template</span></span>

1. <span data-ttu-id="4edbb-171">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="4edbb-172">Stel in het linkerdeelvenster het veld **Type wavesjabloon** in op *Verzenden*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="4edbb-173">Selecteer de sjabloon **61 Verzending** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4edbb-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="4edbb-174">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="4edbb-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4edbb-175">Stel op het sneltabblad **Algemeen** de optie **Vrijgave van aanvullingswerk automatiseren** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="4edbb-176">Stel deze optie in op *Ja* om op vraag gebaseerd aanvullingswerk te maken en dit automatisch vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="4edbb-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="4edbb-177">U moet de methode van de aanvullingswave toevoegen aan de wavesjabloon en een aanvullingssjabloon maken van het type **Waveaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="4edbb-178">Stel een aanvullingssjabloon in de pagina **Aanvullingssjablonen** in.</span><span class="sxs-lookup"><span data-stu-id="4edbb-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="4edbb-179">Als u een aanvullingssjabloon wilt instellen, moet u de aanvullingsmethode toevoegen aan de wavesjabloon.</span><span class="sxs-lookup"><span data-stu-id="4edbb-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="4edbb-180">Zoek op het sneltabblad **Methoden** in de kolom **Geselecteerde methoden** naar de volgende regel:</span><span class="sxs-lookup"><span data-stu-id="4edbb-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="4edbb-181">**Naam van methode:** *Aanvullen*</span><span class="sxs-lookup"><span data-stu-id="4edbb-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="4edbb-182">**Naam:** *Aanvulling*</span><span class="sxs-lookup"><span data-stu-id="4edbb-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="4edbb-183">Stel het veld **Wave-stepcode** voor deze regel in op *Aanvulling*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="4edbb-184">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="4edbb-185">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="4edbb-185">Example scenario</span></span>

<span data-ttu-id="4edbb-186">Nadat u alle eerder beschreven voorbeeldgegevens hebt gemaakt en ingesteld, kunt u dit scenario doorlopen om de functie *Aanvulling boven locatiecapaciteit* uit te proberen.</span><span class="sxs-lookup"><span data-stu-id="4edbb-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="4edbb-187">Bij de waarden die in dit scenario worden weergegeven, wordt ervan uitgegaan dat u werkt met de standaarddemonstratiegegevens, dat u de rechtspersoon **USMF** hebt geselecteerd en dat u de voorbeeldrecords hebt voorbereid die eerder in dit onderwerp zijn beschreven.</span><span class="sxs-lookup"><span data-stu-id="4edbb-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="4edbb-188">Dit scenario dient ook als voorbeeld waarin wordt aangegeven hoe de functie in een productie-instelling kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="4edbb-189">Aanvullingswerk maken</span><span class="sxs-lookup"><span data-stu-id="4edbb-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="4edbb-190">Verkooporder 1 maken</span><span class="sxs-lookup"><span data-stu-id="4edbb-190">Create sales order 1</span></span>

1. <span data-ttu-id="4edbb-191">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4edbb-192">Selecteer in het actievenster de optie **Nieuw** om een dialoogvenster te openen voor het maken van een nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4edbb-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="4edbb-193">Stel in het dialoogvenster de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="4edbb-194">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="4edbb-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="4edbb-195">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="4edbb-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4edbb-196">Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4edbb-197">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="4edbb-197">The new sales order is opened.</span></span> <span data-ttu-id="4edbb-198">Deze bevat een nieuwe, lege rij op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4edbb-199">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="4edbb-200">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4edbb-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4edbb-201">**Hoeveelheid:** *40*</span><span class="sxs-lookup"><span data-stu-id="4edbb-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="4edbb-202">Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="4edbb-203">Selecteer op de pagina **Reservering** **Partij reserveren**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="4edbb-204">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4edbb-204">Close the page.</span></span>
1. <span data-ttu-id="4edbb-205">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4edbb-206">U ontvangt informatieve meldingen waarin de wave-id en zending-id worden vermeld die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="4edbb-207">Er wordt ook een aanvullingswave gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="4edbb-208">U ontvangt ook een waarschuwingsbericht met de mededeling dat de blokkering van Werk-ID XXXX niet ongedaan kan worden gemaakt omdat deze onvoltooid aanvullingswerk bevat.</span><span class="sxs-lookup"><span data-stu-id="4edbb-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="4edbb-209">Verkooporder 2 maken</span><span class="sxs-lookup"><span data-stu-id="4edbb-209">Create sales order 2</span></span>

1. <span data-ttu-id="4edbb-210">Selecteer op de pagina **Alle verkooporders** in het actievenster de optie **Nieuw** om een dialoogvenster te openen voor het maken van een nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4edbb-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="4edbb-211">Stel in het dialoogvenster de volgende waarde in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="4edbb-212">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4edbb-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4edbb-213">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="4edbb-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4edbb-214">Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4edbb-215">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="4edbb-215">The new sales order is opened.</span></span> <span data-ttu-id="4edbb-216">Deze bevat een nieuwe, lege rij op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4edbb-217">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="4edbb-218">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4edbb-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4edbb-219">**Hoeveelheid:** *60*</span><span class="sxs-lookup"><span data-stu-id="4edbb-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="4edbb-220">Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="4edbb-221">Selecteer op de pagina **Reservering** **Partij reserveren**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="4edbb-222">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4edbb-222">Close the page.</span></span>
1. <span data-ttu-id="4edbb-223">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4edbb-224">U ontvangt informatieve meldingen waarin de wave-id en zending-id worden vermeld die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="4edbb-225">Er wordt ook een aanvullingswave gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="4edbb-226">U ontvangt ook een waarschuwingsbericht met de mededeling dat de blokkering van Werk-ID XXXX niet ongedaan kan worden gemaakt omdat deze onvoltooid aanvullingswerk bevat.</span><span class="sxs-lookup"><span data-stu-id="4edbb-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="4edbb-227">Verkooporder 3 maken</span><span class="sxs-lookup"><span data-stu-id="4edbb-227">Create sales order 3</span></span>

1. <span data-ttu-id="4edbb-228">Selecteer op de pagina **Alle verkooporders** in het actievenster de optie **Nieuw** om een dialoogvenster te openen voor het maken van een nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4edbb-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="4edbb-229">Stel in het dialoogvenster de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="4edbb-230">**Klantrekening:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="4edbb-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="4edbb-231">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="4edbb-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4edbb-232">Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4edbb-233">De nieuwe verkooporder wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="4edbb-233">The new sales order is opened.</span></span> <span data-ttu-id="4edbb-234">Deze bevat een nieuwe, lege rij op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4edbb-235">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="4edbb-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="4edbb-236">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4edbb-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4edbb-237">**Hoeveelheid:** *30*</span><span class="sxs-lookup"><span data-stu-id="4edbb-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="4edbb-238">Selecteer op het sneltabblad **Verkooporderregels** in **Voorraad \> Reservering**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="4edbb-239">Selecteer op de pagina **Reservering** **Partij reserveren**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="4edbb-240">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4edbb-240">Close the page.</span></span>
1. <span data-ttu-id="4edbb-241">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4edbb-242">U ontvangt informatieve meldingen waarin de wave-id en zending-id worden vermeld die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="4edbb-243">Er wordt ook een aanvullingswave gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="4edbb-244">U ontvangt ook een waarschuwingsbericht met de mededeling dat de blokkering van Werk-ID XXXX niet ongedaan kan worden gemaakt omdat deze onvoltooid aanvullingswerk bevat.</span><span class="sxs-lookup"><span data-stu-id="4edbb-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="4edbb-245">Werkdetails weergeven</span><span class="sxs-lookup"><span data-stu-id="4edbb-245">View work details</span></span>

1. <span data-ttu-id="4edbb-246">Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="4edbb-247">Filter in de sectie **Overzicht** de kolom **Magazijn** voor magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="4edbb-248">U ziet dat er zeven werk-id's zijn gemaakt voor de drie vraagverkooporders.</span><span class="sxs-lookup"><span data-stu-id="4edbb-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="4edbb-249">Drie van de zeven werk-id's hebben de **werkordertype**-waarde *Aanvulling* en vier hebben de **werkordertype**-waarde *Verkooporders*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="4edbb-250">Alle drie de werk-id's met een **werkordertype**-waarde van *Aanvulling* hebben dezelfde *verzamel-* en *wegzet*-locaties in de sectie **Regels**:</span><span class="sxs-lookup"><span data-stu-id="4edbb-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="4edbb-251">**Verzamelen:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="4edbb-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="4edbb-252">**Wegzetten:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="4edbb-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="4edbb-253">Er zijn twee werk-id's gemaakt voor verkooporder 1.</span><span class="sxs-lookup"><span data-stu-id="4edbb-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="4edbb-254">Noteer de werk-id's van de verkooporders.</span><span class="sxs-lookup"><span data-stu-id="4edbb-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="4edbb-255">Afhankelijk van de voorhanden hoeveelheden kunnen de hoeveelheden werk die worden gemaakt, enigszins variëren.</span><span class="sxs-lookup"><span data-stu-id="4edbb-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="4edbb-256">De gemaakte werkkoppen moeten echter wel overeenkomen met dit scenariovoorbeeld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="4edbb-257">Nummerplaat-id van voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="4edbb-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="4edbb-258">Verderop in dit scenario gebruikt u de mobiele app Magazijnbeheer (of een emulator), waarin u de nummerplaat moet identificeren om de scenario's voor verzameling en aanvulling te voltooien.</span><span class="sxs-lookup"><span data-stu-id="4edbb-258">Later in this scenario, you will use the Warehouse Management mobile app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="4edbb-259">Voer de volgende stappen uit om de nummerplaat-id's te vinden die u later nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="4edbb-260">Ga naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden voorraad**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="4edbb-261">Selecteer de knop **Filters weergeven** om het filterdeelvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4edbb-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="4edbb-262">Voer de volgende filtercriteria in om de nummerplaten voor het scenario op te halen.</span><span class="sxs-lookup"><span data-stu-id="4edbb-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="4edbb-263">Gebruik het filter *begint met*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="4edbb-264">**Artikelnummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4edbb-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4edbb-265">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="4edbb-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4edbb-266">Selecteer **Toepassing**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-266">Select **Apply**.</span></span>
1. <span data-ttu-id="4edbb-267">Selecteer in het actievenster de optie **Dimensies**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="4edbb-268">Selecteer in het dialoogvenster **Weergave van dimensies** in de sectie **Opslagdimensies** alle waarden.</span><span class="sxs-lookup"><span data-stu-id="4edbb-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="4edbb-269">Selecteer in de sectie **Transacties** **Artikelnummer** en **Hoeveelheid \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="4edbb-270">Wanneer u klaar bent, selecteert u **OK** om het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="4edbb-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="4edbb-271">Het raster **Voorhanden** toont de nummerplaatnummers voor artikel *T0100* op elke locatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="4edbb-272">Noteer de nummerplaat die zich op elke locatie bevindt, want u hebt deze gegevens later nodig.</span><span class="sxs-lookup"><span data-stu-id="4edbb-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="4edbb-273">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4edbb-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="4edbb-274">Processtappen</span><span class="sxs-lookup"><span data-stu-id="4edbb-274">Process steps</span></span>

<span data-ttu-id="4edbb-275">U voert de magazijnlocatieaanvulling uit voor de eerste twee werk-Id's.</span><span class="sxs-lookup"><span data-stu-id="4edbb-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="4edbb-276">Werk aan het derde aanvullingswerk wordt geblokkeerd totdat het voorraadniveau op de verzamellocatie onder de drempel valt.</span><span class="sxs-lookup"><span data-stu-id="4edbb-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="4edbb-277">Aanvulling</span><span class="sxs-lookup"><span data-stu-id="4edbb-277">Replenishment</span></span>

1. <span data-ttu-id="4edbb-278">Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker in magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-278">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="4edbb-279">(Geef *61* op als gebruikers-id en *1* als wachtwoord.)</span><span class="sxs-lookup"><span data-stu-id="4edbb-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="4edbb-280">Ga naar **Voorraad \> Aanvulling**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="4edbb-281">U wordt gevraagd om het eerste aanvullingswerk te voltooien.</span><span class="sxs-lookup"><span data-stu-id="4edbb-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="4edbb-282">Het artikelnummer, de hoeveelheid en de locatie waar moet worden verzameld, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4edbb-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="4edbb-283">Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="4edbb-284">Klik op de knop **OK** (vinkjesymbool).</span><span class="sxs-lookup"><span data-stu-id="4edbb-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="4edbb-285">Het systeem genereert een nummerplaatnummer voor de nieuwe nummerplaat voor het verzamelde artikel.</span><span class="sxs-lookup"><span data-stu-id="4edbb-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="4edbb-286">Selecteer **OK** om de waarde te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="4edbb-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="4edbb-287">Er wordt wegzetwerk weergegeven dat de gebruiker instrueert de doelnummerplaat op de aanvullingslocatie weg te zetten.</span><span class="sxs-lookup"><span data-stu-id="4edbb-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="4edbb-288">De *wegzet* locatie moet **06A01R2S1B** zijn.</span><span class="sxs-lookup"><span data-stu-id="4edbb-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="4edbb-289">Bevestig de wegzetgegevens en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="4edbb-290">U ontvangt het bericht 'Werk voltooid' en de details van de volgende aanvullingsverzameltaak worden weergegeven: het artikelnummer, de hoeveelheid en de locatie waaruit moet worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="4edbb-291">De verzamellocatie is gelijk aan de eerste aanvullingslocatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="4edbb-292">Daarom heeft de nummerplaat dezelfde nummerplaat-id die is gebruikt voor de eerste aanvullingswerktaak.</span><span class="sxs-lookup"><span data-stu-id="4edbb-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="4edbb-293">Herhaal de vorige stappen om het aanvullingswerk voor de tweede taak te voltooien.</span><span class="sxs-lookup"><span data-stu-id="4edbb-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="4edbb-294">De hoeveelheid en de doelnummerplaat verschillen van de hoeveelheid en de doelnummerplaat van de eerste werktaak.</span><span class="sxs-lookup"><span data-stu-id="4edbb-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="4edbb-295">Nadat het tweede aanvullingswerk is voltooid, wordt het bericht 'Werk voltooid' weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4edbb-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="4edbb-296">Het mobiele apparaat informeert u ook dat er geen werk beschikbaar is, zelfs als enig aanvullingswerk resteert.</span><span class="sxs-lookup"><span data-stu-id="4edbb-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="4edbb-297">Deze werking treedt op omdat het aanvullingswerk de beschikbaarheidsstatus *Geblokkeerd* heeft en daarom is gemarkeerd als **Geblokkeerd**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="4edbb-298">De status *Geblokkeerd* is ingeschakeld omdat het locatieprofiel voor de verzamellocatie waaraan het werk wordt toegewezen, een **Overschrijdingshoeveelheid**-waarde van *0,65 PL* heeft.</span><span class="sxs-lookup"><span data-stu-id="4edbb-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="4edbb-299">De twee eerdere aanvullingswerktaken hebben de locatie bijna tot op de overschrijdingslimiet gevuld voor artikel *T0100*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="4edbb-300">(De eenheidsomrekening voor het artikel is *1 PL = 100 stuks*.) Het resterende aanvullingswerk zou daarom de locatie de limiet doen overschrijden.</span><span class="sxs-lookup"><span data-stu-id="4edbb-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="4edbb-301">Dit aanvullingswerk blijft geblokkeerd tot er voldoende voorraad is verzameld vanaf deze locatie om de locatie onder de werkvrijgavedrempel te brengen in de menuopdracht van het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="4edbb-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="4edbb-302">Verkooporderverzameling</span><span class="sxs-lookup"><span data-stu-id="4edbb-302">Sales order pick</span></span>

<span data-ttu-id="4edbb-303">Voordat de resterende aanvullingswerktaak kan worden voltooid, moet de voorraad op de verzamellocatie worden verminderd tot een niveau waarop het resterende aanvullingswerk kan worden gedeblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="4edbb-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="4edbb-304">Met andere woorden, de som van de hoeveelheid voorhanden voorraad op de locatie en de aanvullingshoeveelheid mogen de waarde **Overschrijdingshoeveelheid** niet overschrijden.</span><span class="sxs-lookup"><span data-stu-id="4edbb-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="4edbb-305">Wanneer deze som kleiner is dan de overschrijdingshoeveelheid, wordt het resterende aanvullingswerk gedeblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="4edbb-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="4edbb-306">Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker in magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="4edbb-306">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="4edbb-307">(Geef *61* op als gebruikers-id en *1* als wachtwoord.)</span><span class="sxs-lookup"><span data-stu-id="4edbb-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="4edbb-308">Ga naar **Uitgaand \> Orderverzamelen**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="4edbb-309">Voer de eerste werk-id voor verkooporder 1 in.</span><span class="sxs-lookup"><span data-stu-id="4edbb-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="4edbb-310">Raadpleeg de werk-id's voor verkooporders waarvan u eerder een notitie hebt gemaakt, op de pagina **Werkgegevens**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="4edbb-311">Met de werk-id die u hier invoert, wordt verzamelwerk voor een hoeveelheid van 10 stuks gegenereerd vanaf twee aparte locaties.</span><span class="sxs-lookup"><span data-stu-id="4edbb-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="4edbb-312">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-312">Select **OK**.</span></span>

    <span data-ttu-id="4edbb-313">De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit voor de eerste locatie moet worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="4edbb-314">Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="4edbb-315">Klik op de knop **OK** (vinkjesymbool).</span><span class="sxs-lookup"><span data-stu-id="4edbb-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="4edbb-316">De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit voor de volgende locatie moet worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="4edbb-317">Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="4edbb-318">Klik op de knop **OK** (vinkjesymbool).</span><span class="sxs-lookup"><span data-stu-id="4edbb-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="4edbb-319">Op de pagina **Verkooporders: wegzetten** wordt aangegeven dat u het voltooide verzamelwerk moet wegzetten op de uitgaande faseringslocatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="4edbb-320">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-320">Select **OK**.</span></span>

    <span data-ttu-id="4edbb-321">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="4edbb-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="4edbb-322">Voer de tweede werk-id voor verkooporder 1 in.</span><span class="sxs-lookup"><span data-stu-id="4edbb-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="4edbb-323">Er is slechts één verzameltaak voor deze werk-id.</span><span class="sxs-lookup"><span data-stu-id="4edbb-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="4edbb-324">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-324">Select **OK**.</span></span>

    <span data-ttu-id="4edbb-325">De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit moet worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="4edbb-326">Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="4edbb-327">De nummerplaat die u opgeeft, is een van de door het systeem gegenereerde nummerplaten uit de aanvullingswerktaken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="4edbb-328">Als u er zeker van wilt zijn dat u de juiste nummerplaat-id gebruikt, controleert u de voorraad op de pagina **Voorhanden lijst** voor het artikel, de locatie en de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="4edbb-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="4edbb-329">Klik op de knop **OK** (vinkjesymbool).</span><span class="sxs-lookup"><span data-stu-id="4edbb-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="4edbb-330">Bevestig de instructies voor de wegzettaak naar de uitgaande faseringslocatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="4edbb-331">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-331">Select **OK**.</span></span>

    <span data-ttu-id="4edbb-332">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="4edbb-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="4edbb-333">Verkooporder 2 is geblokkeerd voor verzamelen omdat de aanvullingstaak waaraan deze is gekoppeld, niet is voltooid.</span><span class="sxs-lookup"><span data-stu-id="4edbb-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="4edbb-334">Op dit moment is er nog steeds een hoeveelheid van 30 stuks op de verzamellocatie en is de aanvullingshoeveelheid voor verkooporder 2 60 stuks.</span><span class="sxs-lookup"><span data-stu-id="4edbb-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="4edbb-335">De som van de voorhanden voorraad en de aanvullingsvoorraad (90 stuks) overschrijdt de overschrijdingshoeveelheid van 0,65 PL (of 65 stuks).</span><span class="sxs-lookup"><span data-stu-id="4edbb-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="4edbb-336">Voordat het aanvullingswerk kan worden voltooid, moet verkooporder 3 worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="4edbb-337">Voer de werk-id voor verkooporder 3 in.</span><span class="sxs-lookup"><span data-stu-id="4edbb-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="4edbb-338">Er is slechts één verzameltaak voor deze werk-id.</span><span class="sxs-lookup"><span data-stu-id="4edbb-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="4edbb-339">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-339">Select **OK**.</span></span>

    <span data-ttu-id="4edbb-340">De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit moet worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="4edbb-341">Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="4edbb-342">De nummerplaat die u opgeeft, is een van de door het systeem gegenereerde nummerplaten uit de aanvullingswerktaken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="4edbb-343">Als u er zeker van wilt zijn dat u de juiste nummerplaat-id gebruikt, controleert u de voorraad op de pagina **Voorhanden lijst** voor het artikel, de locatie en de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="4edbb-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="4edbb-344">Klik op de knop **OK** (vinkjesymbool).</span><span class="sxs-lookup"><span data-stu-id="4edbb-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="4edbb-345">Bevestig de instructies voor de wegzettaak naar de uitgaande faseringslocatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="4edbb-346">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-346">Select **OK**.</span></span>

    <span data-ttu-id="4edbb-347">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="4edbb-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="4edbb-348">Zodra de som van de voorhanden hoeveelheid op de verzamellocatie en de aanvullingshoeveelheid lager is dan de drempelwaarde, kunt u het resterende aanvullingswerk verwerken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="4edbb-349">Ga terug naar de pagina **Werkgegevens** en u ziet dat de beschikbaarheid van aanvullingswerk voor de laatste aanvulling (voor verkooporder 2) *Open* is, omdat er nu voldoende ruimte op de locatie is om de aanvulling te accepteren.</span><span class="sxs-lookup"><span data-stu-id="4edbb-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="4edbb-350">U kunt dit aanvullingswerk nu uitvoeren via het mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="4edbb-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="4edbb-351">Ga naar **Voorraad \> Aanvulling**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="4edbb-352">U wordt gevraagd om het resterende aanvullingswerk te voltooien.</span><span class="sxs-lookup"><span data-stu-id="4edbb-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="4edbb-353">Het artikelnummer, de hoeveelheid en de locatie waar moet worden verzameld, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4edbb-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="4edbb-354">Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="4edbb-355">Klik op de knop **OK** (vinkjesymbool).</span><span class="sxs-lookup"><span data-stu-id="4edbb-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="4edbb-356">Het systeem genereert een nummerplaatnummer voor de nieuwe nummerplaat voor het verzamelde artikel.</span><span class="sxs-lookup"><span data-stu-id="4edbb-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="4edbb-357">Selecteer **OK** om de waarde te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="4edbb-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="4edbb-358">Er wordt wegzetwerk weergegeven dat de gebruiker instrueert de doelnummerplaat op de aanvullingslocatie weg te zetten.</span><span class="sxs-lookup"><span data-stu-id="4edbb-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="4edbb-359">De *wegzet* locatie moet **06A01R2S1B** zijn.</span><span class="sxs-lookup"><span data-stu-id="4edbb-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="4edbb-360">Bevestig de wegzetgegevens en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="4edbb-361">U ontvangt berichten over 'Werk voltooid' en 'Geen werk beschikbaar'.</span><span class="sxs-lookup"><span data-stu-id="4edbb-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="4edbb-362">U kunt nu verkooporder 2 verzamelen.</span><span class="sxs-lookup"><span data-stu-id="4edbb-362">You can now pick sales order 2.</span></span> <span data-ttu-id="4edbb-363">Dit werd gedeblokkeerd toen het aanvullingswerk werd voltooid dat is gekoppeld aan de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4edbb-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="4edbb-364">Voer de werk-id voor verkooporder 2 in.</span><span class="sxs-lookup"><span data-stu-id="4edbb-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="4edbb-365">Er is slechts één verzameltaak voor deze werk-id.</span><span class="sxs-lookup"><span data-stu-id="4edbb-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="4edbb-366">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-366">Select **OK**.</span></span>

    <span data-ttu-id="4edbb-367">De taakpagina **Verkooporders: verzamelen** bevat het artikelnummer, de hoeveelheid en de locatie van waaruit moet worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="4edbb-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="4edbb-368">Voer in het veld **LP** het nummerplaatnummer in voor het artikel op de weergegeven locatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="4edbb-369">De nummerplaat die u opgeeft, is de door het systeem gegenereerde nummerplaat uit de aanvullingswerktaak.</span><span class="sxs-lookup"><span data-stu-id="4edbb-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="4edbb-370">Als u er zeker van wilt zijn dat u de juiste nummerplaat-id gebruikt, controleert u de voorraad op de pagina **Voorhanden lijst** voor het artikel, de locatie en de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="4edbb-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="4edbb-371">Klik op de knop **OK** (vinkjesymbool).</span><span class="sxs-lookup"><span data-stu-id="4edbb-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="4edbb-372">Bevestig de instructies voor de wegzettaak naar de uitgaande faseringslocatie.</span><span class="sxs-lookup"><span data-stu-id="4edbb-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="4edbb-373">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-373">Select **OK**.</span></span>

    <span data-ttu-id="4edbb-374">U ontvangt de melding Werk voltooid.</span><span class="sxs-lookup"><span data-stu-id="4edbb-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="4edbb-375">Opmerkingen en tips</span><span class="sxs-lookup"><span data-stu-id="4edbb-375">Notes and tips</span></span>

- <span data-ttu-id="4edbb-376">Deze functionaliteit werkt met alle aanvullingstypen: wavevraag, min/max, ladingsvraag en vakken.</span><span class="sxs-lookup"><span data-stu-id="4edbb-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="4edbb-377">U kunt desgewenst de beschikbaarheid van aanvullingswerk voor elke werkkop handmatig wijzigen vanaf de pagina **Werkgegevens**.</span><span class="sxs-lookup"><span data-stu-id="4edbb-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="4edbb-378">Wanneer het systeem de beschikbaarheid van aanvullingswerk instelt, houdt het rekening met voorraad die al aanwezig is op de locatie voordat enig werk is voltooid</span><span class="sxs-lookup"><span data-stu-id="4edbb-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="4edbb-379">Elk verkooporderwerk is gekoppeld aan specifiek aanvullingswerk.</span><span class="sxs-lookup"><span data-stu-id="4edbb-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="4edbb-380">Er is geen corresponderende functionaliteit voor beschikbaarheid van verkoopwerk.</span><span class="sxs-lookup"><span data-stu-id="4edbb-380">There is no corresponding sales work availability functionality.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]