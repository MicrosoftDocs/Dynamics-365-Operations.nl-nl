---
title: Werk splitsen
description: Dit onderwerp bevat informatie over de functionaliteit voor gesplitst werk. Met deze functie kunt u grote werkorders splitsen in meerdere kleinere werkorders die u vervolgens aan meerdere magazijnmedewerkers kunt toewijzen. Op deze manier kan het werk tegelijkertijd worden verzameld door verschillende magazijnmedewerkers.
author: mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eae1e722a7c4d819cbca398eb14a2b36fa04eec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830757"
---
# <a name="work-split"></a><span data-ttu-id="2cf47-105">Werk splitsen</span><span class="sxs-lookup"><span data-stu-id="2cf47-105">Work split</span></span>

<span data-ttu-id="2cf47-106">Met functionaliteit voor gesplitst werk kunt u grote werkorder-id's splitsen in meerdere kleinere werkorder-id's die u vervolgens aan meerdere magazijnmedewerkers kunt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="2cf47-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="2cf47-107">Op deze manier kan één werkaanmaaknummer tegelijkertijd worden verzameld door verschillende magazijnmedewerkers.</span><span class="sxs-lookup"><span data-stu-id="2cf47-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2cf47-108">U kunt alleen werkorders splitsen met de status *Openstaand* of *In uitvoering*.</span><span class="sxs-lookup"><span data-stu-id="2cf47-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="2cf47-109">De functionaliteit voor gesplitst werk inschakelen</span><span class="sxs-lookup"><span data-stu-id="2cf47-109">Turn on the work split functionality</span></span>

<span data-ttu-id="2cf47-110">Voordat u de functionaliteit voor gesplitst werk kunt gebruiken, moet u deze functie en de bijbehorende vereiste functie in uw systeem inschakelen.</span><span class="sxs-lookup"><span data-stu-id="2cf47-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="2cf47-111">Beheerders kunnen gebruikmaken van de instellingen van [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functies te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="2cf47-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="2cf47-112">Schakel eerst de bijbehorende vereiste functie *Werk blokkeren voor de hele organisatie* in als deze nog niet is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2cf47-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="2cf47-113">Schakel in het werkgebied **Functiebeheer** deze functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="2cf47-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="2cf47-114">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="2cf47-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2cf47-115">**Functienaam:** *Werk blokkeren voor de hele organisatie*</span><span class="sxs-lookup"><span data-stu-id="2cf47-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="2cf47-116">Wanneer deze functie is geactiveerd, wordt automatisch een gegevensupgrade toegepast nadat de functie is ingeschakeld voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="2cf47-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="2cf47-117">Schakel vervolgens de functie *Werk splitsen* in. Deze wordt op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="2cf47-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="2cf47-118">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="2cf47-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2cf47-119">**Functienaam:** *Werk splitsen*</span><span class="sxs-lookup"><span data-stu-id="2cf47-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="2cf47-120">Verbeteringen in de pagina's Werkgegevens en Alle werk</span><span class="sxs-lookup"><span data-stu-id="2cf47-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="2cf47-121">Met de functie *Werk splitsen* worden de volgende twee knoppen toegevoegd aan het tabblad **Werk** in het actievenster van de pagina's **Werkgegevens** en **Alle werk**:</span><span class="sxs-lookup"><span data-stu-id="2cf47-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="2cf47-122">**Werk splitsen**: splits de huidige werk-id in meerdere kleinere werk-id's die kunnen worden verwerkt door afzonderlijke werknemers.</span><span class="sxs-lookup"><span data-stu-id="2cf47-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="2cf47-123">**Werksplitsingssessie annuleren**: annuleer de sessie voor werksplitsing en maak het werk beschikbaar voor verwerking.</span><span class="sxs-lookup"><span data-stu-id="2cf47-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="2cf47-124">![De knoppen Werk splitsen en Werksplitsingssessie annuleren](media/Work_split_buttons.png "De knoppen Werk splitsen en Werksplitsingssessie annuleren")</span><span class="sxs-lookup"><span data-stu-id="2cf47-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2cf47-125">De knop **Werk splitsen** is niet beschikbaar als aan een van de volgende voorwaarden is voldaan:</span><span class="sxs-lookup"><span data-stu-id="2cf47-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="2cf47-126">De werkstatus is iets anders dan *Openstaand* of *In uitvoering*.</span><span class="sxs-lookup"><span data-stu-id="2cf47-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="2cf47-127">Er is een container-ID gekoppeld aan de werk-ID.</span><span class="sxs-lookup"><span data-stu-id="2cf47-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="2cf47-128">(Een container kan niet systematisch worden gesplitst, omdat hiervoor fysieke acties vereist zijn.)</span><span class="sxs-lookup"><span data-stu-id="2cf47-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="2cf47-129">Het werk is aan een cluster gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="2cf47-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="2cf47-130">Het werkordertype is iets anders dan een van de volgende typen:</span><span class="sxs-lookup"><span data-stu-id="2cf47-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="2cf47-131">Verkooporders</span><span class="sxs-lookup"><span data-stu-id="2cf47-131">Sales orders</span></span>
>    - <span data-ttu-id="2cf47-132">Orderverzameling van grondstoffen</span><span class="sxs-lookup"><span data-stu-id="2cf47-132">Raw material picking</span></span>
>    - <span data-ttu-id="2cf47-133">Overboekingsuitgifte</span><span class="sxs-lookup"><span data-stu-id="2cf47-133">Transfer issue</span></span>
>
> - <span data-ttu-id="2cf47-134">Het werk wordt momenteel gesplitst door een andere gebruiker.</span><span class="sxs-lookup"><span data-stu-id="2cf47-134">The work is currently being split by another user.</span></span> <span data-ttu-id="2cf47-135">Als u de splitsingspagina probeert te openen voor werk dat al wordt gesplitst door een andere gebruiker, wordt het volgende foutbericht weergegeven: "Het werk met id \#\#\#\# wordt momenteel gesplitst.</span><span class="sxs-lookup"><span data-stu-id="2cf47-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="2cf47-136">Probeer het over een paar minuten opnieuw.</span><span class="sxs-lookup"><span data-stu-id="2cf47-136">Retry in a few minutes.</span></span> <span data-ttu-id="2cf47-137">Neem contact op met een supervisor als u dit bericht blijft ontvangen."</span><span class="sxs-lookup"><span data-stu-id="2cf47-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="2cf47-138">Een nieuwe reden voor het blokkeren van werk, *Werk gesplitst*, geeft aan dat de werk-id op dat moment wordt gesplitst.</span><span class="sxs-lookup"><span data-stu-id="2cf47-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="2cf47-139">Deze wordt weergegeven op de pagina **Werk splitsen** en in de mobiele app Magazijnbeheer als een gebruiker het werk probeert uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="2cf47-139">It's shown both on the **Split work** page and in the Warehouse Management mobile app if a user tries to run the work.</span></span> <span data-ttu-id="2cf47-140">Wanneer er blokkeringsredenen worden gebruikt, wordt de naam van het veld **Geblokkeerde wave** van de werk-id gewijzigd in **Geblokkeerd**.</span><span class="sxs-lookup"><span data-stu-id="2cf47-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="2cf47-141">Een werksplitsing starten</span><span class="sxs-lookup"><span data-stu-id="2cf47-141">Initiate a work split</span></span>

<span data-ttu-id="2cf47-142">Met deze functie voegt u een nieuwe pagina **Werk splitsen** toe waarmee gebruikers werkregels van de werk-id kunnen splitsen.</span><span class="sxs-lookup"><span data-stu-id="2cf47-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="2cf47-143">Wanneer de pagina voor het eerst wordt geopend, worden regels met de werkstatus *Openstaand* weergegeven en kunnen deze worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="2cf47-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="2cf47-144">Selecteer in het actievenster de optie **Werk splitsen** om het geselecteerde werk te verwerken.</span><span class="sxs-lookup"><span data-stu-id="2cf47-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="2cf47-145">Voer de volgende stappen uit om werk te splitsen.</span><span class="sxs-lookup"><span data-stu-id="2cf47-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="2cf47-146">Open een van de volgende werkpagina's:</span><span class="sxs-lookup"><span data-stu-id="2cf47-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="2cf47-147">**Werkgegevens** (**Magazijnbeheer \> Werk \> Werkgegevens**)</span><span class="sxs-lookup"><span data-stu-id="2cf47-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="2cf47-148">**Alle werk** (**Magazijnbeheer \> Werk \> Alle werk**)</span><span class="sxs-lookup"><span data-stu-id="2cf47-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="2cf47-149">Selecteer in het raster een werk-id om te splitsen.</span><span class="sxs-lookup"><span data-stu-id="2cf47-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="2cf47-150">Het veld **Werkordertype** moet zijn ingesteld op een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="2cf47-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="2cf47-151">Verkooporders</span><span class="sxs-lookup"><span data-stu-id="2cf47-151">Sales orders</span></span>
    - <span data-ttu-id="2cf47-152">Orderverzameling van grondstoffen</span><span class="sxs-lookup"><span data-stu-id="2cf47-152">Raw material picking</span></span>
    - <span data-ttu-id="2cf47-153">Overboekingsuitgifte</span><span class="sxs-lookup"><span data-stu-id="2cf47-153">Transfer issue</span></span>

1. <span data-ttu-id="2cf47-154">Selecteer in het actievenster op het tabblad **Werk** in de groep **Werk** de optie **Werk splitsen**.</span><span class="sxs-lookup"><span data-stu-id="2cf47-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="2cf47-155">De pagina **Werk splitsen** verschijnt en toont de werkregels die openstaan en kunnen worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="2cf47-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="2cf47-156">Standaard worden alleen de beschikbare werkregels weergegeven.</span><span class="sxs-lookup"><span data-stu-id="2cf47-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="2cf47-157">Als u alle regels voor de werk-id wilt weergeven (bijvoorbeeld regels met werktype *Wegzetten*), schakelt u het selectievakje **Alle regels weergeven** boven het raster in.</span><span class="sxs-lookup"><span data-stu-id="2cf47-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="2cf47-158">Het volgende bericht wordt weergegeven: "Gebruikers kunnen geen regels van het werk verwerken totdat u klaar bent met de splitsing en deze pagina hebt gesloten."</span><span class="sxs-lookup"><span data-stu-id="2cf47-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="2cf47-159">Het veld **Reden voor blokkeren van werk** voor het huidige werk wordt ingesteld op *Gesplitst werk* en het werk wordt geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="2cf47-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="2cf47-160">![Reden voor blokkering](media/Blocking_reason.png "Reden voor blokkering")</span><span class="sxs-lookup"><span data-stu-id="2cf47-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="2cf47-161">Selecteer de regels die u wilt verwijderen uit de huidige werk-id en toevoegen aan een nieuwe werk-id.</span><span class="sxs-lookup"><span data-stu-id="2cf47-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="2cf47-162">De volgende gebeurtenissen vinden plaats:</span><span class="sxs-lookup"><span data-stu-id="2cf47-162">The following events occur:</span></span>

    - <span data-ttu-id="2cf47-163">Wanneer u het werk splitst, worden de geselecteerde regel of regels van de oorspronkelijke werk-id geannuleerd en vervolgens naar een nieuwe werk-id gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="2cf47-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="2cf47-164">De bestaande werksjabloonstructuur en de wegzetlocatie (en ook toekomstige combinaties van verzamelen en wegzetten) blijven behouden.</span><span class="sxs-lookup"><span data-stu-id="2cf47-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="2cf47-165">De waarden voor de volgende werk-id-velden worden gekopieerd van het oorspronkelijke werk naar het nieuwe werk:</span><span class="sxs-lookup"><span data-stu-id="2cf47-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="2cf47-166">Lading-id</span><span class="sxs-lookup"><span data-stu-id="2cf47-166">Load ID</span></span>
        - <span data-ttu-id="2cf47-167">Zending-id</span><span class="sxs-lookup"><span data-stu-id="2cf47-167">Shipment ID</span></span>
        - <span data-ttu-id="2cf47-168">Werkordertype</span><span class="sxs-lookup"><span data-stu-id="2cf47-168">Work order type</span></span>
        - <span data-ttu-id="2cf47-169">Ordernummer</span><span class="sxs-lookup"><span data-stu-id="2cf47-169">Order number</span></span>
        - <span data-ttu-id="2cf47-170">Locatie</span><span class="sxs-lookup"><span data-stu-id="2cf47-170">Site</span></span>
        - <span data-ttu-id="2cf47-171">Magazijn</span><span class="sxs-lookup"><span data-stu-id="2cf47-171">Warehouse</span></span>
        - <span data-ttu-id="2cf47-172">Werkprioriteit</span><span class="sxs-lookup"><span data-stu-id="2cf47-172">Work priority</span></span>
        - <span data-ttu-id="2cf47-173">Werkgroep-id</span><span class="sxs-lookup"><span data-stu-id="2cf47-173">Work pool ID</span></span>
        - <span data-ttu-id="2cf47-174">Wave-id</span><span class="sxs-lookup"><span data-stu-id="2cf47-174">Wave ID</span></span>
        - <span data-ttu-id="2cf47-175">Werkaanmaaknummer</span><span class="sxs-lookup"><span data-stu-id="2cf47-175">Work creation number</span></span>

    - <span data-ttu-id="2cf47-176">De volgende velden worden niet naar de nieuwe werk-id gekopieerd:</span><span class="sxs-lookup"><span data-stu-id="2cf47-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="2cf47-177">**Werk-id**: er wordt een nieuwe werk-id gegenereerd op basis van de betreffende nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="2cf47-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="2cf47-178">**Werkstatus**: dit veld wordt ingesteld op *Openstaand*.</span><span class="sxs-lookup"><span data-stu-id="2cf47-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="2cf47-179">**Vergrendeld door**: dit veld wordt in eerste instantie op leeg ingesteld.</span><span class="sxs-lookup"><span data-stu-id="2cf47-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="2cf47-180">**Doelnummerplaat-id**: dit veld wordt niet ingevuld.</span><span class="sxs-lookup"><span data-stu-id="2cf47-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="2cf47-181">**Aanmaakdatum en -tijd**: dit veld wordt ingesteld op de huidige datum en tijd.</span><span class="sxs-lookup"><span data-stu-id="2cf47-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="2cf47-182">**Wave/werk geblokkeerd**: dit veld wordt opnieuw berekend voor de oorspronkelijke werk-id en de nieuwe werk-id.</span><span class="sxs-lookup"><span data-stu-id="2cf47-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="2cf47-183">Selecteer **Werk splitsen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="2cf47-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="2cf47-184">Terwijl het werk wordt gesplitst, wordt het volgende bericht weergegeven: "Bezig met verwerken -Werk splitsen".</span><span class="sxs-lookup"><span data-stu-id="2cf47-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="2cf47-185">Terwijl dit bericht zichtbaar is, kunt u de bewerking annuleren door **Annuleren** te selecteren in het berichtvenster.</span><span class="sxs-lookup"><span data-stu-id="2cf47-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="2cf47-186">Als het selectievakje **Alle regels weergeven** is uitgeschakeld, wordt de regel die is gesplitst en geannuleerd niet meer weergegeven in het raster.</span><span class="sxs-lookup"><span data-stu-id="2cf47-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="2cf47-187">Als het selectievakje is ingeschakeld, ziet u dat de waarde van het veld **Werkstatus** voor die regel is gewijzigd in *Geannuleerd*.</span><span class="sxs-lookup"><span data-stu-id="2cf47-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="2cf47-188">De volgende melding wordt weergegeven om aan te geven dat de nieuwe werk-id is gemaakt: "Werk \#\#\#\# is gemaakt door een splitsing van het oorspronkelijke werk \#\#\#\#."</span><span class="sxs-lookup"><span data-stu-id="2cf47-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="2cf47-189">Andere werkregels van de oorspronkelijke werk-id (zoals *Wegzetten*-regels) worden zo nodig aangepast aan de werkregels die zijn geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="2cf47-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="2cf47-190">Als de oorspronkelijke werk-id bijvoorbeeld een *Wegzetten*-regel heeft voor een hoeveelheid van 15 en *Verzamelen*-regels met een totale hoeveelheid van 10 die zijn geannuleerd, is de nieuwe hoeveelheid voor *Wegzetten* op de oorspronkelijke werk-id nu 5.</span><span class="sxs-lookup"><span data-stu-id="2cf47-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="2cf47-191">Het nieuwe werk wordt niet onmiddellijk aan een gebruiker toegewezen.</span><span class="sxs-lookup"><span data-stu-id="2cf47-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="2cf47-192">U kunt dit echter zo nodig nu aan een gebruiker toewijzen door de standaardfunctionaliteit van de pagina **Werkgegevens** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2cf47-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2cf47-193">U kunt alleen werk-id's splitsen die twee of meer beschikbare werkregels bevatten.</span><span class="sxs-lookup"><span data-stu-id="2cf47-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="2cf47-194">Als u **Werk splitsen** selecteert wanneer er slechts één werkregel is, wordt het volgende foutbericht weergegeven: "Ten minste één werkregel moet op het oorspronkelijke werk blijven."</span><span class="sxs-lookup"><span data-stu-id="2cf47-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="2cf47-195">In dit geval wordt er geen splitsing uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2cf47-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="2cf47-196">Een werksplitsing voltooien</span><span class="sxs-lookup"><span data-stu-id="2cf47-196">Finish a work split</span></span>

<span data-ttu-id="2cf47-197">Als u het splitsen van werk wilt voltooien, moet de blokkeringsreden *Gesplitst werk* worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="2cf47-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="2cf47-198">Deze stap kunt u op twee manieren uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="2cf47-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="2cf47-199">De gebruiker die de werkzaamheden splitst, sluit de pagina **Werk splitsen** door de knop **Sluiten** (**X**) te selecteren in de rechterbovenhoek.</span><span class="sxs-lookup"><span data-stu-id="2cf47-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="2cf47-200">Wanneer de pagina wordt gesloten, wordt de blokkeringsreden *Werk splitsen* verwijderd.</span><span class="sxs-lookup"><span data-stu-id="2cf47-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="2cf47-201">De status *Geblokkeerd* van dit werk wordt opnieuw berekend en als er geen resterende blokkeringsredenen zijn voor dit werk, wordt de blokkering van het werk opgeheven.</span><span class="sxs-lookup"><span data-stu-id="2cf47-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="2cf47-202">Een gebruiker opent de werk-id en selecteert de knop **Werksplitsingssessie annuleren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="2cf47-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="2cf47-203">De blokkeringsreden *Gesplitst werk* wordt verwijderd en de status *Geblokkeerd* van dit werk wordt opnieuw berekend, zoals bij het sluiten van de pagina **Werk splitsen**.</span><span class="sxs-lookup"><span data-stu-id="2cf47-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="2cf47-204">Nadat de blokkeringsreden *Gesplitst werk* is verwijderd, kan het werk worden uitgevoerd op het mobiele apparaat, mits de status **Geblokkeerd** is ingesteld op *Nee* in de werk-id.</span><span class="sxs-lookup"><span data-stu-id="2cf47-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a><span data-ttu-id="2cf47-205">Gebruiker blokkeren in de mobiele app Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="2cf47-205">User blocking on the Warehouse Management mobile app</span></span>

<span data-ttu-id="2cf47-206">Als u de mobiele app Magazijnbeheer probeert te gebruiken voor verzamelen van werk voor een werk-id die al wordt gesplitst, wordt het volgende foutbericht weergegeven: "Het werk met id \#\#\#\# wordt momenteel gesplitst."</span><span class="sxs-lookup"><span data-stu-id="2cf47-206">If you try to use the Warehouse Management mobile app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="2cf47-207">Als dit foutbericht wordt weergegeven, selecteert u **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="2cf47-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="2cf47-208">Vervolgens kunt u doorgaan met het verwerken van ander werk.</span><span class="sxs-lookup"><span data-stu-id="2cf47-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="2cf47-209">Andere geblokkeerde bewerkingen</span><span class="sxs-lookup"><span data-stu-id="2cf47-209">Other blocked operations</span></span>

<span data-ttu-id="2cf47-210">Bewerkingen waarmee werkregels, werkvoorraadtransacties of aanvullingskoppelingen worden gewijzigd die zijn gerelateerd aan het werk dat wordt gesplitst, zullen mislukken en het volgende foutbericht wordt weergegeven: "Het werk met ID \#\#\#\# wordt momenteel gesplitst."</span><span class="sxs-lookup"><span data-stu-id="2cf47-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]