---
title: Positionering van locatie nummerplaat
description: Met positionering van de nummerplaatlocatie kunt u zien waar een nummerplaat zich bevindt in een locatie met meerdere pallets, zoals een locatie waar pallets dubbeldiep worden weggezet.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: e5fd7a9a9703f9ab6802def0aac096e29aa04f1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831380"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="930dd-103">Positionering van locatie nummerplaat</span><span class="sxs-lookup"><span data-stu-id="930dd-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="930dd-104">Met positionering van de nummerplaatlocatie kunt u zien waar een nummerplaat zich bevindt in een locatie met meerdere pallets, zoals een locatie waar pallets dubbeldiep worden weggezet.</span><span class="sxs-lookup"><span data-stu-id="930dd-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="930dd-105">De functie voegt een volgnummer toe aan elke nummerplaat die op een opslaglocatie wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="930dd-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="930dd-106">Dit volgnummer wordt gebruikt om de nummerplaten op de opslaglocatie te bestellen.</span><span class="sxs-lookup"><span data-stu-id="930dd-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="930dd-107">De functie ondersteunt daarom op intelligente wijze scenario's waarin klanten een doorrolstelling gebruiken en die voor het verzamelen van producten moeten weten welke nummerplaat zich vooraan bevindt.</span><span class="sxs-lookup"><span data-stu-id="930dd-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="930dd-108">Dit onderwerp bespreekt een scenario waarin wordt uitgelegd hoe u de functie instelt en gebruikt.</span><span class="sxs-lookup"><span data-stu-id="930dd-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="930dd-109">De functie Positionering van locatie nummerplaat inschakelen</span><span class="sxs-lookup"><span data-stu-id="930dd-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="930dd-110">Voordat u de functie Positionering van locatie nummerplaat kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="930dd-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="930dd-111">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="930dd-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="930dd-112">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="930dd-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="930dd-113">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="930dd-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="930dd-114">**Functienaam:** *Positionering van locatie nummerplaat*</span><span class="sxs-lookup"><span data-stu-id="930dd-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="930dd-115">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="930dd-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="930dd-116">Voorbeeldgegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="930dd-116">Make sample data available</span></span>

<span data-ttu-id="930dd-117">Om dit scenario te doorlopen met de waarden die hier worden voorgesteld, moet u werken op een systeem waarop voorbeeldgegevens zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="930dd-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="930dd-118">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="930dd-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="930dd-119">De functie instellen voor dit scenario</span><span class="sxs-lookup"><span data-stu-id="930dd-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="930dd-120">Voer de volgende procedures uit om de functie *Positionering van locatie nummerplaat* in te stellen voor het scenario dat in dit onderwerp wordt besproken.</span><span class="sxs-lookup"><span data-stu-id="930dd-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="930dd-121">Locatieprofielen</span><span class="sxs-lookup"><span data-stu-id="930dd-121">Location profiles</span></span>

<span data-ttu-id="930dd-122">De functie moet worden ingeschakeld in het locatieprofiel voor elke locatie waar de functie wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="930dd-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="930dd-123">Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.</span><span class="sxs-lookup"><span data-stu-id="930dd-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="930dd-124">Selecteer in de lijst met locatieprofielen in het linkerdeel venster de optie **BULK-06**.</span><span class="sxs-lookup"><span data-stu-id="930dd-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="930dd-125">Op het sneltabblad **Algemeen** zijn twee nieuwe opties toegevoegd door de functie.</span><span class="sxs-lookup"><span data-stu-id="930dd-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="930dd-126">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="930dd-126">Set the following values:</span></span>

    - <span data-ttu-id="930dd-127">**Positie van kentekenplaat inschakelen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="930dd-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="930dd-128">Als deze optie is ingesteld op *Ja*, wordt de positie van de nummerplaat vastgehouden voor nummerplaten op deze locatie.</span><span class="sxs-lookup"><span data-stu-id="930dd-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="930dd-129">**Positie nummerplaat tonen op mobiel apparaat:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="930dd-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="930dd-130">Wanneer deze optie is ingesteld op *Ja*, wordt de positie van de nummerplaat getoond aan gebruikers van mobiele apparaten tijdens corrigeren en tellen.</span><span class="sxs-lookup"><span data-stu-id="930dd-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="930dd-131">U kunt de instelling van deze optie alleen wijzigen als de functie is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="930dd-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="930dd-132">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="930dd-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="930dd-133">Locatie-instructies</span><span class="sxs-lookup"><span data-stu-id="930dd-133">Location directives</span></span>

1. <span data-ttu-id="930dd-134">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="930dd-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="930dd-135">Controleer in het linkerdeel venster of het veld **Werkordertype** is ingesteld op *Verkooporders*.</span><span class="sxs-lookup"><span data-stu-id="930dd-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="930dd-136">Selecteer in de lijst met locatie-instructies **61 VO Orderverzamelingsorder**.</span><span class="sxs-lookup"><span data-stu-id="930dd-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="930dd-137">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="930dd-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="930dd-138">Selecteer op het sneltabblad **Regels** de regel met het **volgnummer** *2*.</span><span class="sxs-lookup"><span data-stu-id="930dd-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="930dd-139">Selecteer op het sneltabblad **Locatie-instructieacties** de regel met de **Naam**-waarde *Verzamelen voor minder dan pallet* (dit moet de enige regel zijn) en wijzig de waarde van het **Volgnummer** in *2*.</span><span class="sxs-lookup"><span data-stu-id="930dd-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="930dd-140">Selecteer **Nieuw** boven het raster om een regel voor een nieuwe locatie-instructieactie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="930dd-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="930dd-141">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="930dd-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="930dd-142">**Volgnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="930dd-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="930dd-143">**Naam:** *Pickpositie 1*</span><span class="sxs-lookup"><span data-stu-id="930dd-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="930dd-144">Selecteer de optie **Query bewerken** boven het raster terwijl de nieuwe regel nog steeds is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="930dd-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="930dd-145">Selecteer in de query-editor het tabblad **Joins**.</span><span class="sxs-lookup"><span data-stu-id="930dd-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="930dd-146">Vouw de tabeljoin **Locaties** uit om de join met de tabel **Voorraaddimensies** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="930dd-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="930dd-147">Vouw de tabeljoin **Voorraaddimensies** uit om de join met de tabel **Voorhanden voorraad** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="930dd-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="930dd-148">Selecteer **Voorraaddimensies** en selecteer vervolgens **Tabeljoin toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="930dd-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="930dd-149">Selecteer in de lijst met tabellen die wordt geopend in de kolom **Relatie** de waarde **Nummerplaat (nummerplaat)**.</span><span class="sxs-lookup"><span data-stu-id="930dd-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="930dd-150">Selecteer vervolgens **Selecteren** om **Nummerplaat** toe te voegen aan de tabeljoin **Voorraaddimensies**.</span><span class="sxs-lookup"><span data-stu-id="930dd-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="930dd-151">Terwijl **Nummerplaat** nog is geselecteerd, selecteert u **Tabeljoin toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="930dd-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="930dd-152">Selecteer in de lijst met tabellen die wordt geopend in de kolom **Relatie** de waarde **Positionering van locatie nummerplaat (nummerplaat)**.</span><span class="sxs-lookup"><span data-stu-id="930dd-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="930dd-153">Selecteer vervolgens **Selecteren** om **Positionering van locatie nummerplaat** toe te voegen aan de tabeljoin **Voorraaddimensies**.</span><span class="sxs-lookup"><span data-stu-id="930dd-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="930dd-154">![Tabeljoins](media/LpTableJoin.png "Tabeljoins")</span><span class="sxs-lookup"><span data-stu-id="930dd-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="930dd-155">Klik op **OK** om de bijgewerkte gekoppelde tabellen te bevestigen en de query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="930dd-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="930dd-156">Selecteer op het sneltabblad **Locatie-instructieacties** opnieuw de optie **Query bewerken** om de query-editor te openen.</span><span class="sxs-lookup"><span data-stu-id="930dd-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="930dd-157">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="930dd-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="930dd-158">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="930dd-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="930dd-159">**Tabel:** *Positionering van locatie nummerplaat*</span><span class="sxs-lookup"><span data-stu-id="930dd-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="930dd-160">**Afgeleide tabel:** *Positionering van locatie nummerplaat*</span><span class="sxs-lookup"><span data-stu-id="930dd-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="930dd-161">**Veld:** *Positie NP*</span><span class="sxs-lookup"><span data-stu-id="930dd-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="930dd-162">**Criteria:** *1*</span><span class="sxs-lookup"><span data-stu-id="930dd-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="930dd-163">![Nieuw bereik](media/LpPositionCriteria.png "Nieuw bereik")</span><span class="sxs-lookup"><span data-stu-id="930dd-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="930dd-164">Selecteer **OK** om de wijzigingen te bevestigen en de query-editor te sluiten.</span><span class="sxs-lookup"><span data-stu-id="930dd-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="930dd-165">Voorbeeldgegevens instellen voor dit scenario</span><span class="sxs-lookup"><span data-stu-id="930dd-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="930dd-166">Voor dit scenario moet de gebruiker zich aanmelden bij de mobiele magazijnapp door een werknemer te gebruiken die is ingesteld om werk uit te voeren in magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="930dd-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="930dd-167">De gebruiker moet ook transacties uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="930dd-167">The user must also complete transactions.</span></span>

<span data-ttu-id="930dd-168">Omdat de functie *Positionering van locatie nummerplaat* een nieuwe id toevoegt voor posities van de nummerplaat op een locatie, moet u eerst enkele gegevens aanmaken om het scenario te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="930dd-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="930dd-169">Plaatscyclustelling uitvoeren op de eerste locatie</span><span class="sxs-lookup"><span data-stu-id="930dd-169">Spot-count the first location</span></span>

1. <span data-ttu-id="930dd-170">Start de mobiele magazijnapp en meld u aan bij magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="930dd-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="930dd-171">Ga naar **Voorraad \> Plaatscyclustelling**.</span><span class="sxs-lookup"><span data-stu-id="930dd-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="930dd-172">Stel op de pagina **Plaatscyclustelling** het veld **Locatie** in op *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="930dd-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="930dd-173">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-173">Select **OK**.</span></span>

    <span data-ttu-id="930dd-174">Op de pagina wordt de locatie getoond die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="930dd-174">The page shows the location that you entered.</span></span> <span data-ttu-id="930dd-175">Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"</span><span class="sxs-lookup"><span data-stu-id="930dd-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="930dd-176">Selecteer **Vernieuwen** om een telling toe te voegen aan de locatie.</span><span class="sxs-lookup"><span data-stu-id="930dd-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="930dd-177">Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **Artikel** en voert u de waarde *A0001* in.</span><span class="sxs-lookup"><span data-stu-id="930dd-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="930dd-178">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-178">Select **OK**.</span></span>
1. <span data-ttu-id="930dd-179">Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **NP** en voert u de waarde *LP1001* in (of een ander nummerplaatnummer van uw keuze).</span><span class="sxs-lookup"><span data-stu-id="930dd-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="930dd-180">Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** wordt **Nummerplaatpositie 1** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="930dd-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="930dd-181">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-181">Select **OK**.</span></span>

    <span data-ttu-id="930dd-182">U moet nu de hoeveelheid opgeven van het artikel dat op de nummerplaat wordt geteld.</span><span class="sxs-lookup"><span data-stu-id="930dd-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="930dd-183">Stel het veld **Hoeveelheid** in op *10*.</span><span class="sxs-lookup"><span data-stu-id="930dd-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="930dd-184">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-184">Select **OK**.</span></span>

    <span data-ttu-id="930dd-185">Op de pagina wordt de locatie getoond die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="930dd-185">The page shows the location that you entered.</span></span> <span data-ttu-id="930dd-186">Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"</span><span class="sxs-lookup"><span data-stu-id="930dd-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="930dd-187">Selecteer **Vernieuwen** om nog een telling toe te voegen aan de locatie.</span><span class="sxs-lookup"><span data-stu-id="930dd-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="930dd-188">Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **Artikel** en voert u de waarde *A0002* in.</span><span class="sxs-lookup"><span data-stu-id="930dd-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="930dd-189">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-189">Select **OK**.</span></span>
1. <span data-ttu-id="930dd-190">Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **NP** en voert u de waarde *LP1002* in (of een ander nummerplaatnummer van uw keuze, mits deze verschilt van het nummerplaatnummer dat u eerder hebt opgegeven).</span><span class="sxs-lookup"><span data-stu-id="930dd-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="930dd-191">Wijzig de positie van de nummerplaat door het veld **Positie NP** in te stellen op *2*.</span><span class="sxs-lookup"><span data-stu-id="930dd-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="930dd-192">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-192">Select **OK**.</span></span>
1. <span data-ttu-id="930dd-193">Geef de hoeveelheid van het artikel op dat wordt geteld bij de nummerplaat door het veld **Hoeveelheid** in te stellen op *10*.</span><span class="sxs-lookup"><span data-stu-id="930dd-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="930dd-194">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-194">Select **OK**.</span></span>

    <span data-ttu-id="930dd-195">Op de pagina wordt de locatie getoond die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="930dd-195">The page shows the location that you entered.</span></span> <span data-ttu-id="930dd-196">Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"</span><span class="sxs-lookup"><span data-stu-id="930dd-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="930dd-197">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-197">Select **OK**.</span></span>

<span data-ttu-id="930dd-198">Het werk is nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="930dd-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="930dd-199">Plaatscyclustelling uitvoeren op de tweede locatie</span><span class="sxs-lookup"><span data-stu-id="930dd-199">Spot-count the second location</span></span>

1. <span data-ttu-id="930dd-200">Stel op de pagina **Plaatscyclustelling** het veld **Locatie** in op *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="930dd-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="930dd-201">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-201">Select **OK**.</span></span>

    <span data-ttu-id="930dd-202">Op de pagina wordt de locatie getoond die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="930dd-202">The page shows the location that you entered.</span></span> <span data-ttu-id="930dd-203">Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"</span><span class="sxs-lookup"><span data-stu-id="930dd-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="930dd-204">Selecteer **Vernieuwen** om een telling toe te voegen aan de locatie.</span><span class="sxs-lookup"><span data-stu-id="930dd-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="930dd-205">Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **Artikel** en voert u de waarde *A0002* in.</span><span class="sxs-lookup"><span data-stu-id="930dd-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="930dd-206">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-206">Select **OK**.</span></span>
1. <span data-ttu-id="930dd-207">Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** selecteert u het veld **NP** en voert u de waarde *LP1003* in (of een ander nummerplaatnummer van uw keuze, mits deze verschilt van de beide nummerplaatnummers die u hebt opgegeven in de vorige procedure).</span><span class="sxs-lookup"><span data-stu-id="930dd-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="930dd-208">Op de pagina **Cyclustelling: nieuwe NP of artikel toevoegen** wordt **Nummerplaatpositie 1** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="930dd-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="930dd-209">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-209">Select **OK**.</span></span>
1. <span data-ttu-id="930dd-210">Geef de hoeveelheid van het artikel op dat wordt geteld bij de nummerplaat door het veld **Hoeveelheid** in te stellen op *10*.</span><span class="sxs-lookup"><span data-stu-id="930dd-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="930dd-211">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-211">Select **OK**.</span></span>

    <span data-ttu-id="930dd-212">Op de pagina wordt de locatie getoond die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="930dd-212">The page shows the location that you entered.</span></span> <span data-ttu-id="930dd-213">Ook wordt het volgende bericht weergegeven: "Locatie voltooid, nieuwe NP of artikel toevoegen?"</span><span class="sxs-lookup"><span data-stu-id="930dd-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="930dd-214">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-214">Select **OK**.</span></span>

<span data-ttu-id="930dd-215">Het werk is nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="930dd-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="930dd-216">Werkgegevens</span><span class="sxs-lookup"><span data-stu-id="930dd-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="930dd-217">Plaatscyclustellingen vanuit de mobiele app maken cyclustellingswerk aan in Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="930dd-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="930dd-218">Voor het werk moeten de tellingen worden geaccepteerd voordat ze naar de voorraad worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="930dd-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="930dd-219">Meld u aan bij Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="930dd-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="930dd-220">Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="930dd-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="930dd-221">Zoek op het tabblad **Overzicht** naar de regels met de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="930dd-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="930dd-222">**Werkordertype:** *Cyclustelling*</span><span class="sxs-lookup"><span data-stu-id="930dd-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="930dd-223">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="930dd-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="930dd-224">**Werkstatus:** *In afwachting van controle*</span><span class="sxs-lookup"><span data-stu-id="930dd-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="930dd-225">Voor deze regels moeten twee werk-id's zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="930dd-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="930dd-226">De telling voor beide werk-id's moet worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="930dd-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="930dd-227">Selecteer in het raster de eerste werk-id voor het werkordertype *Cyclustelling*.</span><span class="sxs-lookup"><span data-stu-id="930dd-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="930dd-228">Selecteer in het actievenster op het tabblad **Werk** in de groep **Werk** de optie **Cyclustelling**.</span><span class="sxs-lookup"><span data-stu-id="930dd-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="930dd-229">Er worden twee regels weergegeven: één voor elk artikel met nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="930dd-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="930dd-230">De waarden in de **velden Getelde hoeveelheid**, **Locatie**, **Nummerplaat** en **Artikel** moeten overeenkomen met de waarden van de tellingen die u op het mobiele apparaat hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="930dd-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="930dd-231">Als een of meer van deze velden niet zichtbaar zijn, selecteert u in het actievenster de optie **Dimensies weergeven** om ze aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="930dd-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="930dd-232">Selecteer beide regels.</span><span class="sxs-lookup"><span data-stu-id="930dd-232">Select both lines.</span></span>
1. <span data-ttu-id="930dd-233">Selecteer in het actievenster **Telling accepteren**.</span><span class="sxs-lookup"><span data-stu-id="930dd-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="930dd-234">U ziet de melding "Boeken - journaal".</span><span class="sxs-lookup"><span data-stu-id="930dd-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="930dd-235">Selecteer **Berichtdetails** om het geboekte journaalnummer weer te geven.</span><span class="sxs-lookup"><span data-stu-id="930dd-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="930dd-236">Sluit de berichtdetails.</span><span class="sxs-lookup"><span data-stu-id="930dd-236">Close the message details.</span></span>
1. <span data-ttu-id="930dd-237">Vernieuw de pagina **Werk**.</span><span class="sxs-lookup"><span data-stu-id="930dd-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="930dd-238">De eerste werk-id is gesloten en wordt niet meer weergegeven.</span><span class="sxs-lookup"><span data-stu-id="930dd-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="930dd-239">U kunt het afgesloten werk weergeven door het selectievakje **Gesloten weergeven** boven het raster in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="930dd-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="930dd-240">U accepteert nu het werk voor de nummerplaat op de locatie *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="930dd-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="930dd-241">Selecteer op het tabblad **Overzicht** de tweede werk-id voor het werkordertype *Cyclustelling*.</span><span class="sxs-lookup"><span data-stu-id="930dd-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="930dd-242">Selecteer in het actievenster op het tabblad **Werk** in de groep **Werk** de optie **Cyclustelling**.</span><span class="sxs-lookup"><span data-stu-id="930dd-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="930dd-243">Er wordt één regel weergegeven voor het artikel en de nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="930dd-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="930dd-244">De waarden in de **velden Getelde hoeveelheid**, **Locatie**, **Nummerplaat** en **Artikel** moeten overeenkomen met de waarden van de tellingen die u op het mobiele apparaat hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="930dd-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="930dd-245">Selecteer de regel.</span><span class="sxs-lookup"><span data-stu-id="930dd-245">Select the line.</span></span>
1. <span data-ttu-id="930dd-246">Selecteer in het actievenster **Telling accepteren**.</span><span class="sxs-lookup"><span data-stu-id="930dd-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="930dd-247">U ziet de melding "Boeken - journaal".</span><span class="sxs-lookup"><span data-stu-id="930dd-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="930dd-248">Selecteer **Berichtdetails** om het geboekte journaalnummer weer te geven.</span><span class="sxs-lookup"><span data-stu-id="930dd-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="930dd-249">Sluit de berichtdetails.</span><span class="sxs-lookup"><span data-stu-id="930dd-249">Close the message details.</span></span>
1. <span data-ttu-id="930dd-250">Vernieuw de pagina **Werk**.</span><span class="sxs-lookup"><span data-stu-id="930dd-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="930dd-251">De tweede werk-id is gesloten en wordt niet meer weergegeven.</span><span class="sxs-lookup"><span data-stu-id="930dd-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="930dd-252">U kunt het afgesloten werk weergeven door het selectievakje **Gesloten weergeven** boven het raster in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="930dd-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="930dd-253">Voorhanden voorraad per locatie</span><span class="sxs-lookup"><span data-stu-id="930dd-253">On-hand by location</span></span>

1. <span data-ttu-id="930dd-254">Ga naar **Magazijnbeheer \> Query's en rapporten \> Voorhanden voorraad per locatie**.</span><span class="sxs-lookup"><span data-stu-id="930dd-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="930dd-255">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="930dd-255">Set the following values:</span></span>

    - <span data-ttu-id="930dd-256">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="930dd-256">**Site:** *6*</span></span>
    - <span data-ttu-id="930dd-257">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="930dd-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="930dd-258">**Vernieuwen op locaties:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="930dd-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="930dd-259">Merk op dat de locatie *01A01R1S1B* twee nummerplaten heeft:</span><span class="sxs-lookup"><span data-stu-id="930dd-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="930dd-260">**A0001**, waarbij het veld **Positie NP** is ingesteld op *1*</span><span class="sxs-lookup"><span data-stu-id="930dd-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="930dd-261">**A0002**, waarbij het veld **Positie NP** is ingesteld op *2*</span><span class="sxs-lookup"><span data-stu-id="930dd-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="930dd-262">Merk op dat de locatie *01A01R1S2B* één nummerplaat heeft:</span><span class="sxs-lookup"><span data-stu-id="930dd-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="930dd-263">**A0002**, waarbij het veld **Positie NP** is ingesteld op *1*</span><span class="sxs-lookup"><span data-stu-id="930dd-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="930dd-264">Scenario met verkooporder</span><span class="sxs-lookup"><span data-stu-id="930dd-264">Sales order scenario</span></span>

<span data-ttu-id="930dd-265">Nu de functie *Positionering van locatie nummerplaat* is ingesteld en de voorraad is klaargezet, moet u een verkooporder maken om werk voor orderverzamelen te genereren. De magazijnwerknemer moet dan artikel *A0002* ophalen bij de voorraadlocatie waarop de pallet-id zich bevindt in positie *1*.</span><span class="sxs-lookup"><span data-stu-id="930dd-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="930dd-266">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="930dd-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="930dd-267">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="930dd-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="930dd-268">Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="930dd-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="930dd-269">**Klantrekening:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="930dd-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="930dd-270">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="930dd-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="930dd-271">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="930dd-271">Select **OK**.</span></span>
1. <span data-ttu-id="930dd-272">Een nieuwe regel wordt toegevoegd aan het raster op het sneltabblad **Verkooporderregels**.</span><span class="sxs-lookup"><span data-stu-id="930dd-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="930dd-273">Stel op deze regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="930dd-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="930dd-274">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="930dd-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="930dd-275">**Hoeveelheid:** *1*</span><span class="sxs-lookup"><span data-stu-id="930dd-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="930dd-276">Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="930dd-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="930dd-277">Selecteer op de pagina **Reservering** in het actievenster de waarde **Partij reserveren** om voorraad te reserveren voor de orderregel.</span><span class="sxs-lookup"><span data-stu-id="930dd-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="930dd-278">Sluit de pagina **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="930dd-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="930dd-279">Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**.</span><span class="sxs-lookup"><span data-stu-id="930dd-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="930dd-280">U ontvangt een informatieve melding waarin de wave-id en zendings-id worden vermeld die zijn aangemaakt voor de order.</span><span class="sxs-lookup"><span data-stu-id="930dd-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="930dd-281">Selecteer op het sneltabblad **Verkooporderregels** in het menu **Magazijn** boven het raster de waarde **Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="930dd-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="930dd-282">De pagina **Werk** wordt weergegeven en toont het werk dat voor de verkoopregel is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="930dd-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="930dd-283">Noteer de werk-id die wordt getoond.</span><span class="sxs-lookup"><span data-stu-id="930dd-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="930dd-284">Scenario met orderverzamelen voor verkoop</span><span class="sxs-lookup"><span data-stu-id="930dd-284">Sales picking scenario</span></span>

1. <span data-ttu-id="930dd-285">Start de mobiele app en meld u aan bij magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="930dd-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="930dd-286">Ga naar **Uitgaand \> Orderverzamelen**.</span><span class="sxs-lookup"><span data-stu-id="930dd-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="930dd-287">Selecteer op de pagina **Een werk-id/nummerplaat-id scannen** het veld **Id** en voer vervolgens de werk-id van de verkoopregel in.</span><span class="sxs-lookup"><span data-stu-id="930dd-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="930dd-288">U ziet dat het verzamelwerk u artikel *A0002* laat ophalen vanuit locatie *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="930dd-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="930dd-289">U ontvangt deze instructie omdat artikel *A0002* op een nummerplaat staat die zich bevindt op positie *1* op die locatie.</span><span class="sxs-lookup"><span data-stu-id="930dd-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="930dd-290">![Locatie positie 1](media/LocationLicensePlatePositioning.png "Locatie positie 1")</span><span class="sxs-lookup"><span data-stu-id="930dd-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="930dd-291">Voer de nummerplaat-id in die u voor de locatie hebt gemaakt en volg de aanwijzingen om de verkooporder te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="930dd-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]