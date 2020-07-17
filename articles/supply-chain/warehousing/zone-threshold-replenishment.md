---
title: Aanvulling op basis van zonedrempels
description: Bij het aanvullen op basis van zones wordt een min/max-aanvullingsstrategie (minimum/maximum) gebruikt, maar gehele magazijnzones worden geëvalueerd in plaats van afzonderlijke locaties. Daarom kunnen magazijnbeheerders sneller ervaren wanneer er extra voorraad nodig is in een orderverzamelzone.
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7e9fdf0a546bf449f249eacdded1f4b4d1b4d1af
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530599"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="57199-104">Aanvulling op basis van zonedrempels</span><span class="sxs-lookup"><span data-stu-id="57199-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57199-105">Bij het aanvullen op basis van zones wordt een [min/max-aanvullingsstrategie](replenishment.md) (minimum/maximum) gebruikt, maar gehele magazijnzones worden geëvalueerd in plaats van afzonderlijke locaties.</span><span class="sxs-lookup"><span data-stu-id="57199-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="57199-106">Daarom kunnen magazijnbeheerders sneller ervaren wanneer er extra voorraad nodig is in een orderverzamelzone.</span><span class="sxs-lookup"><span data-stu-id="57199-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="57199-107">De instelling voor deze functie is vergelijkbaar met de instelling voor aanvulling op basis van locatie.</span><span class="sxs-lookup"><span data-stu-id="57199-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="57199-108">Wanneer u echter een sjabloon instelt voor min/max-aanvulling, kunt u ook opgeven of de drempel per locatie of per zone moet worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="57199-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="57199-109">Als u een evaluatie instelt die is gebaseerd op zones, moet u specifieke zones toevoegen aan de query voor zoneselectie.</span><span class="sxs-lookup"><span data-stu-id="57199-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="57199-110">Net als bij op locatie gebaseerde min/max-aanvulling, is op zones gebaseerde min/max-aanvulling gebaseerd op de configuratie van een drempel voor minimumvoorraad die het aanmaken van aanvullingswerk voor geselecteerde artikelen triggert.</span><span class="sxs-lookup"><span data-stu-id="57199-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="57199-111">Met dit aanvulllingswerk wordt de voorraad verhoogd tot de opgegeven maximumdrempel voor de zone.</span><span class="sxs-lookup"><span data-stu-id="57199-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="57199-112">Aanvullingsprocessen voor zones voor productvarianten worden niet ondersteund in de huidige versie.</span><span class="sxs-lookup"><span data-stu-id="57199-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="57199-113">In tegenstelling tot min/max-aanvulling op basis van locaties, vereist op zones gebaseerde min/max-aanvulling geen vaste locaties om te evalueren of op een locatie een specifiek artikel moet worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="57199-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="57199-114">Daarom kunt u met behulp van op zones gebaseerde aanvulling min/max-aanvulling gebruiken, ook als u geen vaste locaties hebt voor elk artikel of elke artikelvariant in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="57199-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="57199-115">Wanneer een hoeveelheid in de zone onder de opgegeven minimum drempel zakt, wordt het aanvullingswerk gemaakt.</span><span class="sxs-lookup"><span data-stu-id="57199-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="57199-116">In de locatie-instructies wordt bepaald op welke specifieke locatie de voorraad moet worden weggezet.</span><span class="sxs-lookup"><span data-stu-id="57199-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="57199-117">De functie Aanvulling op basis van zonedrempels inschakelen</span><span class="sxs-lookup"><span data-stu-id="57199-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="57199-118">Voordat u de functie *Aanvulling op basis van zonedrempels* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="57199-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="57199-119">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="57199-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="57199-120">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="57199-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="57199-121">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="57199-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="57199-122">**Functienaam:** *Aanvulling op basis van zonedrempels*</span><span class="sxs-lookup"><span data-stu-id="57199-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="57199-123">Aanvulling op basis van zones instellen</span><span class="sxs-lookup"><span data-stu-id="57199-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="57199-124">Als u aanvulling op basis van zones wilt instellen, moet u verschillende onderdelen van het systeem configureren.</span><span class="sxs-lookup"><span data-stu-id="57199-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="57199-125">In deze sectie worden de verschillende instellingen geïntroduceerd en worden waarden voor demogegevens weergegeven die u kunt invoeren als u het scenario aan het einde van dit onderwerp wilt doorlopen.</span><span class="sxs-lookup"><span data-stu-id="57199-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="57199-126">Instructiecodes instellen</span><span class="sxs-lookup"><span data-stu-id="57199-126">Set up directive codes</span></span>

<span data-ttu-id="57199-127">Met [instructiecodes](control-warehouse-location-directives.md) kunt u specifieker bepalen welke locatiesjabloon in een werksjabloon wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="57199-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="57199-128">Met elke code wordt een algemene waarde ingesteld waarnaar u kunt verwijzen wanneer u elk type sjabloon configureert.</span><span class="sxs-lookup"><span data-stu-id="57199-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="57199-129">Instructiecodes weergeven en bewerken</span><span class="sxs-lookup"><span data-stu-id="57199-129">View and edit directive codes</span></span>

<span data-ttu-id="57199-130">Om de instructiecodes weer te geven of te bewerken, gaat u naar **Magazijnbeheer \> Instellingen \> Instructiecodes**.</span><span class="sxs-lookup"><span data-stu-id="57199-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="57199-131">Instructiecodes voor demogegevens voorbereiden</span><span class="sxs-lookup"><span data-stu-id="57199-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="57199-132">In dit voorbeeld wordt getoond hoe u een instructiecode voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="57199-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="57199-133">Als u het scenario aan het einde van dit onderwerp wilt doorlopen, gebruikt u de voorbeeldgegevenswaarden die hier worden getoond.</span><span class="sxs-lookup"><span data-stu-id="57199-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="57199-134">Gebruik anders uw eigen waarden.</span><span class="sxs-lookup"><span data-stu-id="57199-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="57199-135">Selecteer de rechtspersoon **USMF** om te werken met de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="57199-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="57199-136">Ga naar **Magazijnbeheer \> Instellen \> Instructiecodes**.</span><span class="sxs-lookup"><span data-stu-id="57199-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="57199-137">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="57199-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="57199-138">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="57199-139">**Instructiecode:** _Zoneaanvulling_</span><span class="sxs-lookup"><span data-stu-id="57199-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="57199-140">**Instructiebeschrijving:** _Zoneaanvulling_</span><span class="sxs-lookup"><span data-stu-id="57199-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="57199-141">Selecteer **Opslaan** om de nieuwe code op te slaan.</span><span class="sxs-lookup"><span data-stu-id="57199-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="57199-142">Aanvullingssjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="57199-142">Set up replenishment templates</span></span>

<span data-ttu-id="57199-143">[Sjablonen voor min/max-aanvulling](tasks/set-up-min-max-replenishment-process.md) zijn het belangrijkste mechanisme voor het onderhouden van optimale niveaus op orderverzamellocaties.</span><span class="sxs-lookup"><span data-stu-id="57199-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="57199-144">In deze sjablonen moet u de regels instellen die worden gebruikt om voorraad aan te vullen in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="57199-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="57199-145">De aanvulling waarvoor de sjablonen kunnen worden gebruikt, omvatten aanvulling op basis van zones.</span><span class="sxs-lookup"><span data-stu-id="57199-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="57199-146">Aanvullingssjablonen weergeven en bewerken</span><span class="sxs-lookup"><span data-stu-id="57199-146">View and edit replenishment templates</span></span>

<span data-ttu-id="57199-147">Een aanvullingssjabloon is een set regels die bepalen wanneer en hoe een locatie wordt aangevuld.</span><span class="sxs-lookup"><span data-stu-id="57199-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="57199-148">U selecteert een sjabloon om te bepalen wanneer en hoe aanvulling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="57199-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="57199-149">Om uw aanvullingssjablonen weer te geven en te bewerken gaat u naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen**.</span><span class="sxs-lookup"><span data-stu-id="57199-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="57199-150">Een aanvullingssjabloon met demogegevens voorbereiden</span><span class="sxs-lookup"><span data-stu-id="57199-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="57199-151">In dit voorbeeld wordt getoond hoe u een aanvullingssjabloon voorbereidt.</span><span class="sxs-lookup"><span data-stu-id="57199-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="57199-152">Als u het scenario aan het einde van dit onderwerp wilt doorlopen, gebruikt u de voorbeeldgegevenswaarden die hier worden getoond.</span><span class="sxs-lookup"><span data-stu-id="57199-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="57199-153">Gebruik anders uw eigen waarden.</span><span class="sxs-lookup"><span data-stu-id="57199-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="57199-154">Selecteer de rechtspersoon **USMF** om te werken met de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="57199-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="57199-155">Ga naar **Magazijnbeheer \> Instellen \> Aanvulling \> Aanvullingssjablonen**.</span><span class="sxs-lookup"><span data-stu-id="57199-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="57199-156">Selecteer de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.</span><span class="sxs-lookup"><span data-stu-id="57199-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="57199-157">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="57199-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="57199-158">Stel in de nieuwe rij de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="57199-158">In the new row, set the following values.</span></span> <span data-ttu-id="57199-159">Accepteer de standaardwaarden voor alle overige velden.</span><span class="sxs-lookup"><span data-stu-id="57199-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="57199-160">**Aanvullingssjabloon:** _Zone min/max-aanv_</span><span class="sxs-lookup"><span data-stu-id="57199-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="57199-161">**Beschrijving:** _Zone min/max-aanvulling_</span><span class="sxs-lookup"><span data-stu-id="57199-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="57199-162">**Aanvullingstype:** _Minimum of maximum_</span><span class="sxs-lookup"><span data-stu-id="57199-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="57199-163">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="57199-163">Select **Save**.</span></span>
1. <span data-ttu-id="57199-164">Terwijl de nieuwe rij nog steeds is geselecteerd in het raster **Overzicht**, selecteert u **Nieuw** boven het raster **Details van aanvullingssjabloon** om een rij toe te voegen die is gekoppeld aan de aanvullingssjabloon *Zone min/max-aanv* die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="57199-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="57199-165">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="57199-166">**Volgnummer:** Voer _1_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="57199-167">**Beschrijving:** Voer _Aanvulling orderverzamelzone_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="57199-168">**Aanvullingseenheid:** Selecteer _ea_.</span><span class="sxs-lookup"><span data-stu-id="57199-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="57199-169">**Aanvraagtype:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="57199-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="57199-170">**Instructiecode:** Met dit veld word de aanvullingssjabloon gekoppeld aan een locatie-instructie.</span><span class="sxs-lookup"><span data-stu-id="57199-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="57199-171">Selecteer de instructiecode voor de demogegevens die u eerder hebt gemaakt (_Zoneaanvulling_).</span><span class="sxs-lookup"><span data-stu-id="57199-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="57199-172">**Werksjabloon**: Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="57199-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="57199-173">**Minimumhoeveelheid:** In dit veld stelt u de hoeveelheid in waarbij de aanvulling wordt getriggered.</span><span class="sxs-lookup"><span data-stu-id="57199-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="57199-174">Voer _50_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-174">Enter _50_.</span></span>
    - <span data-ttu-id="57199-175">**Maximumaantal:** Met dit veld kunt u de maximumhoeveelheid van een artikel instellen die in een zone aanwezig kan zijn.</span><span class="sxs-lookup"><span data-stu-id="57199-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="57199-176">Door het gegenereerde aanvullingswerk wordt de voorraad vergroot tot deze hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="57199-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="57199-177">Voer _150_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-177">Enter _150_.</span></span>
    - <span data-ttu-id="57199-178">**Eenheid:** In dit veld wordt de eenheid voor de minimum- en maximumwaarden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="57199-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="57199-179">Selecteer _ea_.</span><span class="sxs-lookup"><span data-stu-id="57199-179">Select _ea_.</span></span>
    - <span data-ttu-id="57199-180">**Vraagverhoging:** Selecteer _Afronden naar boven_.</span><span class="sxs-lookup"><span data-stu-id="57199-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="57199-181">**Lege vaste locaties aanvullen:** Schakel dit selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="57199-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="57199-182">**Alleen vaste locaties aanvullen:** Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-183">**Productquerymodus:** Selecteer _Productquery_.</span><span class="sxs-lookup"><span data-stu-id="57199-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="57199-184">**Bereik aanvullingsdrempel:** Dit veld bepaalt of de sjabloon moet worden geëvalueerd per zone of op een specifieke locatie.</span><span class="sxs-lookup"><span data-stu-id="57199-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="57199-185">Selecteer _Zone_.</span><span class="sxs-lookup"><span data-stu-id="57199-185">Select _Zone_.</span></span>
    - <span data-ttu-id="57199-186">**Magazijn:** Selecteer _61_.</span><span class="sxs-lookup"><span data-stu-id="57199-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="57199-187">Selecteer **Producten selecteren** boven het raster **Details aanvullingssjabloon**.</span><span class="sxs-lookup"><span data-stu-id="57199-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="57199-188">Selecteer in het dialoogvenster **Productquery** op het tabblad **Bereik** de optie **Toevoegen** om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="57199-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="57199-189">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="57199-190">**Tabel:** _Artikelen_</span><span class="sxs-lookup"><span data-stu-id="57199-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="57199-191">**Afgeleide tabel:** _Artikelen_</span><span class="sxs-lookup"><span data-stu-id="57199-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="57199-192">**Veld:** _Artikelnummer_</span><span class="sxs-lookup"><span data-stu-id="57199-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="57199-193">**Criteria:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="57199-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="57199-194">Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="57199-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="57199-195">Selecteer **Zones selecteren voor aanvulling** boven het raster **Details aanvullingssjabloon**.</span><span class="sxs-lookup"><span data-stu-id="57199-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="57199-196">Voeg in het dialoogvenster **Zonequery** op het tabblad **Bereik** een regel aan het raster toe.</span><span class="sxs-lookup"><span data-stu-id="57199-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="57199-197">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="57199-198">**Tabel:** _Magazijnzone_</span><span class="sxs-lookup"><span data-stu-id="57199-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="57199-199">**Afgeleide tabel:** _Magazijnzone_</span><span class="sxs-lookup"><span data-stu-id="57199-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="57199-200">**Veld:** _Zone-id_</span><span class="sxs-lookup"><span data-stu-id="57199-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="57199-201">**Criteria:** _VERDIEPING_</span><span class="sxs-lookup"><span data-stu-id="57199-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="57199-202">Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="57199-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="57199-203">Locatie-instructies instellen</span><span class="sxs-lookup"><span data-stu-id="57199-203">Set up location directives</span></span>

<span data-ttu-id="57199-204">Anders dan bij min/max-aanvulling op basis van op een locatie, vereist op zone gebaseerde min/max-aanvulling dat u beide locatie-instructies voor orderverzamelen en wegzetten configureert, omdat het systeem voor uitgaand werk de gehele zone evalueert, in plaats van alleen de orderverzamellocatie.</span><span class="sxs-lookup"><span data-stu-id="57199-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="57199-205">Locatie-instructies weergeven en bewerken</span><span class="sxs-lookup"><span data-stu-id="57199-205">View and edit location directives</span></span>

<span data-ttu-id="57199-206">Om de locatie-instructies weer te geven of te bewerken, gaat u naar **Magazijnbeheer \> Instellingen \> Locatie-instructies**.</span><span class="sxs-lookup"><span data-stu-id="57199-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="57199-207">In de volgende sectie vindt u voorbeelden waarin wordt uitgelegd hoe u met de instellingen de vereiste locatie-instructies voor orderverzamelen en wegzetten kunt maken.</span><span class="sxs-lookup"><span data-stu-id="57199-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="57199-208">Locatie-instructies voor demogegevens voorbereiden</span><span class="sxs-lookup"><span data-stu-id="57199-208">Prepare demo data location directives</span></span>

<span data-ttu-id="57199-209">Om demogegevens voor te bereiden zodat deze in het scenario aan het einde van dit onderwerp kunnen worden gebruikt, moet u twee locatie-instructies maken: een voor de orderverzamelen en een voor wegzetten.</span><span class="sxs-lookup"><span data-stu-id="57199-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="57199-210">Een instructie voor aanvullingsverzamelen maken</span><span class="sxs-lookup"><span data-stu-id="57199-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="57199-211">Selecteer de rechtspersoon **USMF** om te werken met de demogegevens.</span><span class="sxs-lookup"><span data-stu-id="57199-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="57199-212">Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.</span><span class="sxs-lookup"><span data-stu-id="57199-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="57199-213">Stel in het linkerdeelvenster het veld **Werkordertype** in op _Aanvullen_.</span><span class="sxs-lookup"><span data-stu-id="57199-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="57199-214">Selecteer in het actievenster **Nieuw** om een nieuwe instructie te maken.</span><span class="sxs-lookup"><span data-stu-id="57199-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="57199-215">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-215">Set the following values:</span></span>

    - <span data-ttu-id="57199-216">**Volgnummer:** Accepteer de standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="57199-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="57199-217">**Naam:** Voer _Zone verzamelen_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="57199-218">**Werktype:** Selecteer _Orderverzamelen_.</span><span class="sxs-lookup"><span data-stu-id="57199-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="57199-219">**Locatie:** Selecteer _6_.</span><span class="sxs-lookup"><span data-stu-id="57199-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="57199-220">**Magazijn:** Selecteer _61_.</span><span class="sxs-lookup"><span data-stu-id="57199-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="57199-221">**Instructiecode:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="57199-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="57199-222">**Meerdere SKU's:** Stel deze optie in op _Nee_.</span><span class="sxs-lookup"><span data-stu-id="57199-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="57199-223">Selecteer **Opslaan** om een instructie te maken met de instellingen die u tot op dit punt hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="57199-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="57199-224">Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="57199-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="57199-225">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="57199-226">**Volgnummer:** Voer _1_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="57199-227">**Vanaf hoeveelheid:** Voer _0_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="57199-228">**Tot hoeveelheid:** Voer _10000000_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="57199-229">**Eenheid:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="57199-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="57199-230">**Hoeveelheid zoeken:** Selecteer _Geen_.</span><span class="sxs-lookup"><span data-stu-id="57199-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="57199-231">**Beperken op eenheid:** Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-232">**Afronden naar eenheid:** Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-233">**Verpakkingshoeveelheid zoeken:** Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-234">**Splitsen toestaan:** Schakel dit selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="57199-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="57199-235">Selecteer **Opslaan** om de nieuwe regel op te slaan.</span><span class="sxs-lookup"><span data-stu-id="57199-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="57199-236">Terwijl de nieuwe regel nog steeds is geselecteerd in het raster **Regels**, selecteert u **Nieuw** op het sneltabblad **Locatie-instructieacties** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="57199-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="57199-237">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="57199-238">**Volgnummer:** Voer _1_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="57199-239">**Naam:** Kies _Verzamelen uit bulk_.</span><span class="sxs-lookup"><span data-stu-id="57199-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="57199-240">**Gebruik vaste locaties:** Selecteer _Vaste en niet-vaste locaties_.</span><span class="sxs-lookup"><span data-stu-id="57199-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="57199-241">**Negatieve voorraad toestaan**: Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-242">**Batch ingeschakeld**: Schakel dit selectie vakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-243">**Strategie:** Selecteer _Geen_.</span><span class="sxs-lookup"><span data-stu-id="57199-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="57199-244">Selecteer **Opslaan** om de nieuwe actie op te slaan.</span><span class="sxs-lookup"><span data-stu-id="57199-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="57199-245">Terwijl uw nieuwe actie nog steeds is geselecteerd, selecteert u **Query bewerken** boven het raster **Locatie-instructieacties**.</span><span class="sxs-lookup"><span data-stu-id="57199-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="57199-246">Een querydialoogvenster wordt geopend, waarin u de locaties kunt selecteren van waaruit u wilt aanvullen.</span><span class="sxs-lookup"><span data-stu-id="57199-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="57199-247">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="57199-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="57199-248">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="57199-249">**Tabel:** _Locaties_</span><span class="sxs-lookup"><span data-stu-id="57199-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="57199-250">**Afgeleide tabel:** _Locaties_</span><span class="sxs-lookup"><span data-stu-id="57199-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="57199-251">**Veld:** _Zone-id_</span><span class="sxs-lookup"><span data-stu-id="57199-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="57199-252">**Criteria:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="57199-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="57199-253">Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="57199-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="57199-254">Selecteer **Opslaan** om de locatie-instructie op te slaan.</span><span class="sxs-lookup"><span data-stu-id="57199-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="57199-255">Een instructie voor aanvullingswegzetten maken</span><span class="sxs-lookup"><span data-stu-id="57199-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="57199-256">Controleer op de pagina **Locatie-instructies** in het linkerdeelvenster of het veld **Werkordertype** nog is ingesteld op _Aanvulling_.</span><span class="sxs-lookup"><span data-stu-id="57199-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="57199-257">Selecteer in het actievenster **Nieuw** om nog een nieuwe instructie te maken.</span><span class="sxs-lookup"><span data-stu-id="57199-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="57199-258">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-258">Set the following values:</span></span>

    - <span data-ttu-id="57199-259">**Volgnummer:** Accepteer de standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="57199-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="57199-260">**Naam:** Voer _Zone wegzetten_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="57199-261">**Werkordertype:** Selecteer _Wegzetten_.</span><span class="sxs-lookup"><span data-stu-id="57199-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="57199-262">**Locatie:** Selecteer _6_.</span><span class="sxs-lookup"><span data-stu-id="57199-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="57199-263">**Magazijn:** Selecteer _61_.</span><span class="sxs-lookup"><span data-stu-id="57199-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="57199-264">**Instructiecode:** Selecteer _Zoneaanvulling_ om deze locatie-instructie te koppelen aan de aanvullingssjabloon die u eerder hebt gemaakt met behulp van de code die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="57199-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="57199-265">**Meerdere SKU's:** Stel deze optie in op _Nee_.</span><span class="sxs-lookup"><span data-stu-id="57199-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="57199-266">Selecteer **Opslaan** om een instructie te maken met de instellingen die u tot op dit punt hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="57199-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="57199-267">Ga naar het sneltabblad **Regels** en selecteer **Nieuw** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="57199-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="57199-268">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="57199-269">**Volgnummer:** Voer _1_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="57199-270">**Vanaf hoeveelheid:** Voer _0_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="57199-271">**Tot hoeveelheid:** Voer _10000000_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="57199-272">**Eenheid:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="57199-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="57199-273">**Hoeveelheid zoeken:** Selecteer _Geen_.</span><span class="sxs-lookup"><span data-stu-id="57199-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="57199-274">**Beperken op eenheid:** Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-275">**Afronden naar eenheid:** Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-276">**Verpakkingshoeveelheid zoeken:** Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-277">**Splitsen toestaan:** Schakel dit selectievakje in.</span><span class="sxs-lookup"><span data-stu-id="57199-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="57199-278">Selecteer **Opslaan** om de nieuwe regel op te slaan.</span><span class="sxs-lookup"><span data-stu-id="57199-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="57199-279">Terwijl de nieuwe regel nog steeds is geselecteerd in het raster **Regels**, selecteert u **Nieuw** op het sneltabblad **Locatie-instructieacties** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="57199-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="57199-280">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="57199-281">**Volgnummer:** Voer _1_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="57199-282">**Naam:** Voer _Zone wegzetten_ in.</span><span class="sxs-lookup"><span data-stu-id="57199-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="57199-283">**Gebruik vaste locaties:** Selecteer _Vaste en niet-vaste locaties_.</span><span class="sxs-lookup"><span data-stu-id="57199-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="57199-284">**Negatieve voorraad toestaan**: Schakel dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-285">**Batch ingeschakeld**: Schakel dit selectie vakje uit.</span><span class="sxs-lookup"><span data-stu-id="57199-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="57199-286">**Strategie:** Selecteer _Consolideren_.</span><span class="sxs-lookup"><span data-stu-id="57199-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="57199-287">Selecteer **Opslaan** om de nieuwe actie op te slaan.</span><span class="sxs-lookup"><span data-stu-id="57199-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="57199-288">Terwijl uw nieuwe actie nog steeds is geselecteerd, selecteert u **Query bewerken** boven het raster **Locatie-instructieacties**.</span><span class="sxs-lookup"><span data-stu-id="57199-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="57199-289">Een querydialoogvenster wordt geopend, waarin u de zone kunt selecteren waarnaar u wilt aanvullen.</span><span class="sxs-lookup"><span data-stu-id="57199-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="57199-290">Deze zone moet dezelfde zone zijn die is opgegeven in de aanvullingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="57199-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="57199-291">Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="57199-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="57199-292">Stel in de nieuwe rij de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="57199-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="57199-293">**Tabel:** _Locaties_</span><span class="sxs-lookup"><span data-stu-id="57199-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="57199-294">**Afgeleide tabel:** _Locaties_</span><span class="sxs-lookup"><span data-stu-id="57199-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="57199-295">**Veld:** _Zone-id_</span><span class="sxs-lookup"><span data-stu-id="57199-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="57199-296">**Criteria:** _VERDIEPING_</span><span class="sxs-lookup"><span data-stu-id="57199-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="57199-297">Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="57199-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="57199-298">Selecteer **Opslaan** om de locatie-instructie op te slaan.</span><span class="sxs-lookup"><span data-stu-id="57199-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="57199-299">Scenario's</span><span class="sxs-lookup"><span data-stu-id="57199-299">Scenario</span></span>

<span data-ttu-id="57199-300">In deze sectie wordt een voorbeeldscenario besproken waarin u kunt zien hoe u met de functie kunt werken.</span><span class="sxs-lookup"><span data-stu-id="57199-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="57199-301">De voorbeeldgegevens voorbereiden die zijn vereist voor het voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="57199-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="57199-302">Voordat u het scenario gaat doorlopen, moet u voorbeeld gegevens activeren en de functie configureren, zoals beschreven in deze en de vorige sectie in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="57199-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="57199-303">De rechtspersoon USMF gebruiken</span><span class="sxs-lookup"><span data-stu-id="57199-303">Use the USMF legal entity</span></span>

<span data-ttu-id="57199-304">Als u het scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="57199-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="57199-305">U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="57199-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="57199-306">Extra voorbeeldgegevens voorbereiden</span><span class="sxs-lookup"><span data-stu-id="57199-306">Prepare additional sample data</span></span>

<span data-ttu-id="57199-307">Selecteer eerst de rechtspersoon **USMF** en voeg de benodigde aanvullende voorbeeldgegevens toe, zoals beschreven in de sectie [Op zone gebaseerde aanvulling instellen](#setup) eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="57199-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="57199-308">Controleer de voorhanden voorraad</span><span class="sxs-lookup"><span data-stu-id="57199-308">Check your on-hand inventory</span></span>

<span data-ttu-id="57199-309">Voer de volgende stappen uit om te controleren of uw systeem voldoende voorraad bevat om het voorbeeldscenario te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="57199-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="57199-310">Zorg ervoor dat er voorhanden voorraad is voor artikel *A0001* op twee verschillende locaties in de orderverzamelzone (*VERDIEPING*) die is opgegeven in de aanvullingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="57199-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="57199-311">De totale voorraad moet echter kleiner zijn dan de vereiste minimumhoeveelheid (*50*) die is opgegeven in de aanvullingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="57199-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="57199-312">Op deze manier kunt u simuleren hoe de berekening wordt uitgevoerd voor de gehele zone in plaats van alleen voor één locatie.</span><span class="sxs-lookup"><span data-stu-id="57199-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="57199-313">**U kunt alle relevante magazijnprocessen gebruiken om waar nodig de voorraad aan te passen.**</span><span class="sxs-lookup"><span data-stu-id="57199-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="57199-314">Zorg ervoor dat er voldoende voorraad is voor artikel *A0001* op een bulk locatie die is opgegeven in de locatie-instructie Zone orderverzamelen, waar het aanvullingswerk de artikelen uit zone-id *BULK* moet verzamelen.</span><span class="sxs-lookup"><span data-stu-id="57199-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="57199-315">De totale voorraad moet groter zijn dan de vereiste maximumhoeveelheid (*150*) die is opgegeven in de aanvullingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="57199-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="57199-316">Optioneel maar aanbevolen: Voer de volgende stappen uit om een voorraadcorrectiejournaal te maken:</span><span class="sxs-lookup"><span data-stu-id="57199-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="57199-317">Ga naar **Voorraadbeheer \> Journaalboekingen \> Artikelen \> Voorraadcorrectie**.</span><span class="sxs-lookup"><span data-stu-id="57199-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="57199-318">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="57199-318">Select **New**.</span></span>
    1. <span data-ttu-id="57199-319">Selecteer in het dialoogvenster **Voorraadjournaal maken** in het veld **Magazijn** de waarde *61*.</span><span class="sxs-lookup"><span data-stu-id="57199-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="57199-320">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="57199-320">Select **OK**.</span></span>
    1. <span data-ttu-id="57199-321">Gebruik op het sneltabblad **Journaalregels** de knop **Nieuw** om drie regels aan het raster toe te voegen en stel de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="57199-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="57199-322">Nadat u alle regels hebt ingesteld, selecteert u **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="57199-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="57199-323">**Regel 1:**</span><span class="sxs-lookup"><span data-stu-id="57199-323">**Line 1:**</span></span>

            - <span data-ttu-id="57199-324">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="57199-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="57199-325">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="57199-325">**Site:** *6*</span></span>
            - <span data-ttu-id="57199-326">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="57199-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="57199-327">**Locatie:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="57199-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="57199-328">**Nummerplaat:** Selecteer een bestaande nummerplaat in de lijst of maak een nieuwe nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="57199-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="57199-329">**Hoeveelheid:** *1000*</span><span class="sxs-lookup"><span data-stu-id="57199-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="57199-330">**Regel 2:**</span><span class="sxs-lookup"><span data-stu-id="57199-330">**Line 2:**</span></span>

            - <span data-ttu-id="57199-331">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="57199-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="57199-332">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="57199-332">**Site:** *6*</span></span>
            - <span data-ttu-id="57199-333">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="57199-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="57199-334">**Locatie:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="57199-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="57199-335">**Nummerplaat:** Selecteer een bestaande nummerplaat in de lijst of maak een nieuwe nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="57199-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="57199-336">**Hoeveelheid:** *15*</span><span class="sxs-lookup"><span data-stu-id="57199-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="57199-337">**Regel 3:**</span><span class="sxs-lookup"><span data-stu-id="57199-337">**Line 3:**</span></span>

            - <span data-ttu-id="57199-338">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="57199-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="57199-339">**Locatie:** *6*</span><span class="sxs-lookup"><span data-stu-id="57199-339">**Site:** *6*</span></span>
            - <span data-ttu-id="57199-340">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="57199-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="57199-341">**Locatie:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="57199-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="57199-342">**Nummerplaat:** Selecteer een bestaande nummerplaat in de lijst of maak een nieuwe nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="57199-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="57199-343">**Hoeveelheid:** *10*</span><span class="sxs-lookup"><span data-stu-id="57199-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="57199-344">Selecteer in het actievenster de optie **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="57199-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="57199-345">Verhelp eventuele fouten die worden gevonden voordat u doorgaat naar de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="57199-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="57199-346">Selecteer in het actievenster de optie **Boeken** om de voorraad naar het magazijn te boeken.</span><span class="sxs-lookup"><span data-stu-id="57199-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="57199-347">Voorbeeldscenario: Op zones gebaseerde min/max-aanvulling uitvoeren</span><span class="sxs-lookup"><span data-stu-id="57199-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="57199-348">Nadat alle vereiste voorbeeldgegevens zijn ingevoerd, kunt u aanvulling activeren door de volgende stappen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="57199-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="57199-349">Ga naar **Magazijnbeheer \> Aanvulling \> Aanvullingen**.</span><span class="sxs-lookup"><span data-stu-id="57199-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="57199-350">Selecteer in het dialoogvenster **Aanvulling** op het sneltabblad **Op te nemen records** de optie **Filteren**.</span><span class="sxs-lookup"><span data-stu-id="57199-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="57199-351">Bewerk in het dialgoogvenster **Query** op het tabblad **Bereik** de standaardtabelrij op de volgende manier:</span><span class="sxs-lookup"><span data-stu-id="57199-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="57199-352">**Tabel:** Selecteer _Aanvullingssjablonen_.</span><span class="sxs-lookup"><span data-stu-id="57199-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="57199-353">**Afgeleide tabel:** Selecteer _Aanvullingssjablonen_.</span><span class="sxs-lookup"><span data-stu-id="57199-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="57199-354">**Veld:** Selecteer _Aanvullingssjabloon_.</span><span class="sxs-lookup"><span data-stu-id="57199-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="57199-355">**Criteria:** Selecteer _Zone min/max-aanv_.</span><span class="sxs-lookup"><span data-stu-id="57199-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="57199-356">Deze aanvullingssjabloon is de aanvullingssjabloon die u hebt gemaakt toen u de demogegevens voor dit scenario voorbereidde.</span><span class="sxs-lookup"><span data-stu-id="57199-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="57199-357">Selecteer **OK** om de query op te slaan en terug te gaan naar het dialoogvenster **Aanvulling**.</span><span class="sxs-lookup"><span data-stu-id="57199-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="57199-358">Selecteer **OK** om de aanvullingssjabloon uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="57199-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="57199-359">Er wordt nu aanvullingswerk gemaakt om de voorraad uit de zone *BULK* te verzamelen en deze aan te vullen naar de zone *VERDIEPING*.</span><span class="sxs-lookup"><span data-stu-id="57199-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="57199-360">Opmerkingen en tips</span><span class="sxs-lookup"><span data-stu-id="57199-360">Notes and tips</span></span>

<span data-ttu-id="57199-361">Hier volgen enkele opmerkingen en tips voor het werken met de functie:</span><span class="sxs-lookup"><span data-stu-id="57199-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="57199-362">Als u aanvullingswerk wilt instellen dat naar de gewenste zone gaat, kunt u de regels van de aanvullingssjabloon en de locatie-instructies koppelen op een van de volgende manieren:</span><span class="sxs-lookup"><span data-stu-id="57199-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="57199-363">Bewerk de query voor de locatie-instructiekoptekst en filter de geselecteerde regels van de aanvullingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="57199-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="57199-364">Gebruik een instructiecode op de aanvullingssjabloonregel en laat deze overeenkomen met de locatie-instructie voor wegzetten.</span><span class="sxs-lookup"><span data-stu-id="57199-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="57199-365">Als u dynamische locaties gebruikt, wordt aanvullingswerk gemaakt voor de eerste beschikbare locatie of voor een locatie die al voorraad bevat, als de locatie-instructieactie is ingesteld op het gebruik van de strategie **Consolideren**.</span><span class="sxs-lookup"><span data-stu-id="57199-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="57199-366">Als u vaste locaties gebruikt in plaats van zones, moet u [standaard min/max-aanvulling gebruiken](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="57199-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
