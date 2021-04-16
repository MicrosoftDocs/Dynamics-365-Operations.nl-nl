---
title: Wegzetclusters
description: Wegzetclusters bieden u de mogelijkheid om meerdere nummerplaten tegelijk te verzamelen en ze vervolgens mee te nemen om op verschillende locaties weg te zetten. Dit kan zeer nuttig zijn voor handelsbedrijven, waarbij de nummerplaten doorgaans geen volledige pallets met voorraad zijn.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b3a7d1b7109b83b26c8187a7f0d271f1c82f6d63
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840360"
---
# <a name="putaway-clusters"></a><span data-ttu-id="98c89-104">Wegzetclusters</span><span class="sxs-lookup"><span data-stu-id="98c89-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98c89-105">Wegzetclusters bieden u de mogelijkheid om meerdere nummerplaten tegelijk te verzamelen en ze vervolgens mee te nemen om op verschillende locaties weg te zetten.</span><span class="sxs-lookup"><span data-stu-id="98c89-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="98c89-106">Naar dit proces wordt vaak verwezen als een *milk run*.</span><span class="sxs-lookup"><span data-stu-id="98c89-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="98c89-107">Wegzetclusters kunnen zeer nuttig zijn voor handelsbedrijven, waarbij de nummerplaten doorgaans geen volledige pallets met voorraad zijn.</span><span class="sxs-lookup"><span data-stu-id="98c89-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="98c89-108">De functie Cluster wegzetten inschakelen</span><span class="sxs-lookup"><span data-stu-id="98c89-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="98c89-109">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="98c89-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="98c89-110">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="98c89-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="98c89-111">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="98c89-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="98c89-112">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="98c89-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="98c89-113">**Functie naam:** *functie Cluster wegzetten*</span><span class="sxs-lookup"><span data-stu-id="98c89-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="98c89-114">Instellingen voor het voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="98c89-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="98c89-115">Clusterprofielen</span><span class="sxs-lookup"><span data-stu-id="98c89-115">Cluster profiles</span></span>

<span data-ttu-id="98c89-116">Het wegzetclusterprofiel bepaalt waar een artikel naartoe gaat, op basis van de locatie die aan het artikel is toegewezen op het moment van ontvangst.</span><span class="sxs-lookup"><span data-stu-id="98c89-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="98c89-117">Als verschillende wegzetclusters vereist zijn, moet voor elke menuoptie van het mobiele apparaat een ander wegzetcluster worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="98c89-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="98c89-118">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Clusterprofielen**.</span><span class="sxs-lookup"><span data-stu-id="98c89-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="98c89-119">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="98c89-120">Stel in de weergave **Koptekst** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="98c89-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="98c89-121">**Profiel-id van wegzetcluster:** *Cluster wegzetten*</span><span class="sxs-lookup"><span data-stu-id="98c89-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="98c89-122">**Naam profiel-id van wegzetcluster:** *Cluster wegzetten*</span><span class="sxs-lookup"><span data-stu-id="98c89-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="98c89-123">**Clustertype:** *Wegzetten*</span><span class="sxs-lookup"><span data-stu-id="98c89-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="98c89-124">**Volgnummer:** Accepteer de standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="98c89-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="98c89-125">Selecteer **Opslaan** om de vereiste velden op het sneltabblad **Algemeen** beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="98c89-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="98c89-126">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="98c89-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="98c89-127">**Toewijzingsmoment van cluster:** *bij ontvangst*</span><span class="sxs-lookup"><span data-stu-id="98c89-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="98c89-128">Dit veld bepaalt of het wegzetcluster direct moet worden toegewezen wanneer de voorraad wordt ontvangen, of dat het later moet worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="98c89-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="98c89-129">**Clustertoewijzingsregel:** *handmatig*</span><span class="sxs-lookup"><span data-stu-id="98c89-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="98c89-130">Dit veld bepaald of de clustertoewijzing automatisch door het systeem moet worden bepaald, of handmatig door de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="98c89-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="98c89-131">**Instructiecode:** Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="98c89-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="98c89-132">**Wegzetcluster locatie:** *Bij ontvangst*</span><span class="sxs-lookup"><span data-stu-id="98c89-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="98c89-133">De volgende waarden zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="98c89-133">The following values are available:</span></span>

        - <span data-ttu-id="98c89-134">**Bij ontvangst**: een locatie wordt direct gevonden tijdens ontvangst.</span><span class="sxs-lookup"><span data-stu-id="98c89-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="98c89-135">**Clusterafsluiting**: een locatie wordt gevonden wanneer het cluster wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="98c89-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="98c89-136">**Door gebruiker**: een locatie wordt gevonden wanneer de nummerplaat van het cluster wordt verzameld voor wegzetten.</span><span class="sxs-lookup"><span data-stu-id="98c89-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="98c89-137">In dit geval wordt geen locatie opgegeven wanneer het wegzetwerk wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="98c89-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="98c89-138">Tijdens het wegzetten moet de gebruiker de nummerplaat of de werk-id scannen om de plaatsingsstap te initiëren.</span><span class="sxs-lookup"><span data-stu-id="98c89-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="98c89-139">Het systeem zoekt vervolgens opnieuw de plaatsingslocatie en vertelt de gebruiker waar de verzamelde hoeveelheid moet worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="98c89-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="98c89-140">**Wegzetcluster per gebruiker:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="98c89-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="98c89-141">In dit veld definieert of elk cluster uniek moet zijn per gebruiker wanneer clusters automatisch worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="98c89-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="98c89-142">Deze optie is alleen beschikbaar als het veld **Clustertoewijzingsregel** is ingesteld op *Automatisch*.</span><span class="sxs-lookup"><span data-stu-id="98c89-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="98c89-143">**Eenheidsbeperking:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="98c89-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="98c89-144">In dit veld wordt de eenheid gedefinieerd die moet worden ontvangen voor een geldig profiel.</span><span class="sxs-lookup"><span data-stu-id="98c89-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="98c89-145">Als dit veld leeg wordt gelaten, zijn alle eenheden geldig.</span><span class="sxs-lookup"><span data-stu-id="98c89-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="98c89-146">**Werkeenheid opbreken:** *individueel*</span><span class="sxs-lookup"><span data-stu-id="98c89-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="98c89-147">In dit veld wordt gedefinieerd of alle voorraad moet worden geconsolideerd (met behulp van de cluster-id en de nummerplaat) op één nummerplaat wanneer een cluster wordt afgesloten en of het moet worden opgeslagen als een enkele nummerplaat of afzonderlijk op de ontvangen nummerplaten.</span><span class="sxs-lookup"><span data-stu-id="98c89-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="98c89-148">Dit veld is niet beschikbaar als het veld **Wegzetcluster locatie** is ingesteld op *Bij ontvangst*.</span><span class="sxs-lookup"><span data-stu-id="98c89-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="98c89-149">**Cluster blijft als bovenliggende nummerplaat:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="98c89-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="98c89-150">Als deze optie is ingesteld op *Ja* en de plaatsingsstap is voltooid, wordt de cluster-id een bovenliggende nummerplaat en worden alle artikelen op de cluster-id aan die bovenliggende nummerplaat gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="98c89-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="98c89-151">Op het sneltabblad **Clustersortering** kunt u sorteercriteria voor wegzetten definiëren.</span><span class="sxs-lookup"><span data-stu-id="98c89-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="98c89-152">Selecteer **Nieuw** op de werkbalk om een tweede regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="98c89-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="98c89-153">**Volgnummer:** Accepteer de standaard waarde.</span><span class="sxs-lookup"><span data-stu-id="98c89-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="98c89-154">**Veldnaam:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="98c89-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="98c89-155">In dit veld wordt het veld gedefinieerd dat door deze regel als een sorteercriterium moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="98c89-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="98c89-156">**Sorteren:** *Oplopend*</span><span class="sxs-lookup"><span data-stu-id="98c89-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="98c89-157">Met dit veld bepaalt u of de sortering in oplopende of aflopende volgorde wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="98c89-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="98c89-158">Selecteer in het sneltabblad **Werksjabloon voor cluster** **Nieuw** op de werkbalk om een regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="98c89-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="98c89-159">**Werkordertype:** *Inkooporders*</span><span class="sxs-lookup"><span data-stu-id="98c89-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="98c89-160">**Werksjabloon:** *61 PO direct*</span><span class="sxs-lookup"><span data-stu-id="98c89-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="98c89-161">Selecteer in het actievenster **Opslaan** en vervolgens **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="98c89-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="98c89-162">Selecteer in het dialoogvenster **Cluster wegzetten** op het tabblad **Bereik** de optie **Toevoegen** om een tweede regel aan de query toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="98c89-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="98c89-163">Werk vervolgens de queryregels bij, zoals wordt weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="98c89-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="98c89-164">Tabel</span><span class="sxs-lookup"><span data-stu-id="98c89-164">Table</span></span> | <span data-ttu-id="98c89-165">Afgeleide tabel</span><span class="sxs-lookup"><span data-stu-id="98c89-165">Derived table</span></span> | <span data-ttu-id="98c89-166">Veld</span><span class="sxs-lookup"><span data-stu-id="98c89-166">Field</span></span> | <span data-ttu-id="98c89-167">Criteria</span><span class="sxs-lookup"><span data-stu-id="98c89-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="98c89-168">Werk</span><span class="sxs-lookup"><span data-stu-id="98c89-168">Work</span></span> | <span data-ttu-id="98c89-169">Werk</span><span class="sxs-lookup"><span data-stu-id="98c89-169">Work</span></span> | <span data-ttu-id="98c89-170">Magazijn</span><span class="sxs-lookup"><span data-stu-id="98c89-170">Warehouse</span></span> | <span data-ttu-id="98c89-171">*61*</span><span class="sxs-lookup"><span data-stu-id="98c89-171">*61*</span></span> |
    | <span data-ttu-id="98c89-172">Werk</span><span class="sxs-lookup"><span data-stu-id="98c89-172">Work</span></span> | <span data-ttu-id="98c89-173">Werk</span><span class="sxs-lookup"><span data-stu-id="98c89-173">Work</span></span> | <span data-ttu-id="98c89-174">Werk-id</span><span class="sxs-lookup"><span data-stu-id="98c89-174">Work ID</span></span> | <span data-ttu-id="98c89-175">Laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="98c89-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="98c89-176">Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="98c89-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="98c89-177">Selecteer **Opslaan** in het actievenster en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="98c89-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98c89-178">Velden in het clusterprofiel die grijs worden weergegeven wanneer **Cluster-id genereren** is ingesteld op *Ja*, zijn niet beschikbaar en worden niet meegenomen als deze functie wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="98c89-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="98c89-179">Menuopties voor mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="98c89-179">Mobile device menu items</span></span>

<span data-ttu-id="98c89-180">Voor deze functie zijn twee nieuwe menuopties voor mobiele apparaten beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="98c89-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="98c89-181">De menuoptie **Cluster ontvangen en sorteren** wordt gebruikt om de ontvangen voorraad bij ontvangst te sorteren in een wegzetcluster.</span><span class="sxs-lookup"><span data-stu-id="98c89-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="98c89-182">De menuoptie **Cluster wegzetten** wordt gebruikt om het cluster na toewijzing te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="98c89-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="98c89-183">Cluster ontvangen en sorteren</span><span class="sxs-lookup"><span data-stu-id="98c89-183">Receive and sort cluster</span></span>

<span data-ttu-id="98c89-184">Maak een nieuw menuoptie voor een mobiel apparaat voor het ontvangen van voorraad en het sorteren in een cluster.</span><span class="sxs-lookup"><span data-stu-id="98c89-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="98c89-185">Met deze menuoptie wordt inkomend werk gemaakt nadat de voorraad is ontvangen, waarmee wordt aangegeven dat de ontvangende menuoptie wordt gebruikt voor wegzetclusters.</span><span class="sxs-lookup"><span data-stu-id="98c89-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="98c89-186">De menuoptie **Cluster ontvangen en sorteren** kan worden gebruikt met de volgende ontvangende menuopties:</span><span class="sxs-lookup"><span data-stu-id="98c89-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="98c89-187">Ontvangen van inkooporderregel</span><span class="sxs-lookup"><span data-stu-id="98c89-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="98c89-188">Ontvangen van inkooporderartikel</span><span class="sxs-lookup"><span data-stu-id="98c89-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="98c89-189">Artikelontvangst laden</span><span class="sxs-lookup"><span data-stu-id="98c89-189">Load item receiving</span></span>

1. <span data-ttu-id="98c89-190">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="98c89-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="98c89-191">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="98c89-192">Stel in de weergave **Koptekst** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="98c89-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="98c89-193">**Naam van menuoptie:** *Cluster ontvangen en sorteren*</span><span class="sxs-lookup"><span data-stu-id="98c89-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="98c89-194">**Titel:** *Cluster ontvangen en sorteren*</span><span class="sxs-lookup"><span data-stu-id="98c89-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="98c89-195">**Modus:** *werk*</span><span class="sxs-lookup"><span data-stu-id="98c89-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="98c89-196">**Bestaand werk gebruiken:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="98c89-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="98c89-197">Stel op het sneltabblad **Algemeen** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="98c89-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="98c89-198">**Werkcreatieproces:** *Inkooporderartikelen ontvangen*</span><span class="sxs-lookup"><span data-stu-id="98c89-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="98c89-199">**Nummerplaat maken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="98c89-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="98c89-200">**Wegzetcluster toewijzen:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="98c89-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="98c89-201">De optie **Wegzetcluster toewijzen** is alleen beschikbaar voor de enkele activiteit *Werkcreatieproces* voor ontvangst.</span><span class="sxs-lookup"><span data-stu-id="98c89-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="98c89-202">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="98c89-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="98c89-203">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="98c89-204">Clusteropslag</span><span class="sxs-lookup"><span data-stu-id="98c89-204">Cluster putaway</span></span>

<span data-ttu-id="98c89-205">Maak een nieuwe menuoptie voor mobiele apparaten om het cluster na toewijzing te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="98c89-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="98c89-206">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="98c89-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="98c89-207">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="98c89-208">Stel in de weergave **Koptekst** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="98c89-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="98c89-209">**Naam menuoptie:** *Cluster wegzetten*</span><span class="sxs-lookup"><span data-stu-id="98c89-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="98c89-210">**Titel:** *Cluster wegzetten*</span><span class="sxs-lookup"><span data-stu-id="98c89-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="98c89-211">**Modus:** *werk*</span><span class="sxs-lookup"><span data-stu-id="98c89-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="98c89-212">**Bestaand werk gebruiken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="98c89-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="98c89-213">Stel op het sneltabblad **Algemeen** het veld **Bestuurd door** in op *Cluster wegzetten*.</span><span class="sxs-lookup"><span data-stu-id="98c89-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="98c89-214">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="98c89-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="98c89-215">Stel op het sneltabblad **Werkklassen** de geldige werkklasse in voor deze menuoptie voor een mobiel apparaat:</span><span class="sxs-lookup"><span data-stu-id="98c89-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="98c89-216">**Werkklasse-id:** *Aankoop*</span><span class="sxs-lookup"><span data-stu-id="98c89-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="98c89-217">**Werkordertype:** *Inkooporders*</span><span class="sxs-lookup"><span data-stu-id="98c89-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="98c89-218">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="98c89-219">Menu voor mobiel apparaat</span><span class="sxs-lookup"><span data-stu-id="98c89-219">Mobile device menu</span></span>

<span data-ttu-id="98c89-220">Voeg de menuopties die u zojuist hebt gemaakt toe aan het inkomende menu van de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="98c89-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="98c89-221">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="98c89-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="98c89-222">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="98c89-223">Selecteer **Inkomend** in de menulijst.</span><span class="sxs-lookup"><span data-stu-id="98c89-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="98c89-224">Zoek en selecteer in de lijst **Beschikbare menu's en menuopties** de optie **Cluster ontvangen en sorteren**.</span><span class="sxs-lookup"><span data-stu-id="98c89-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="98c89-225">Selecteer de knop pijl-rechts om de geselecteerde menuoptie te verplaatsen naar de lijst **Menustructuur**.</span><span class="sxs-lookup"><span data-stu-id="98c89-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="98c89-226">Gebruik de knop pijl-omhoog of pijl-omlaag om de menuoptie naar de gewenste positie in het menu te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="98c89-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="98c89-227">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="98c89-228">Herhaal stap 4 tot en met 7 om de resterende menuopties toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="98c89-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="98c89-229">Cluster toewijzen</span><span class="sxs-lookup"><span data-stu-id="98c89-229">Assign cluster</span></span>
    - <span data-ttu-id="98c89-230">Clusteropslag</span><span class="sxs-lookup"><span data-stu-id="98c89-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="98c89-231">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="98c89-231">Example scenario</span></span>

<span data-ttu-id="98c89-232">Dit scenario simuleert het verwerken van wegzetclusters.</span><span class="sxs-lookup"><span data-stu-id="98c89-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="98c89-233">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="98c89-233">Create a purchase order</span></span>

1. <span data-ttu-id="98c89-234">Ga naar **Leveranciers \> Inkooporders \> Alle inkooporders**.</span><span class="sxs-lookup"><span data-stu-id="98c89-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="98c89-235">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="98c89-236">Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="98c89-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="98c89-237">**Leverancieraccount:** *1001*</span><span class="sxs-lookup"><span data-stu-id="98c89-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="98c89-238">**Magazijn:** *61*</span><span class="sxs-lookup"><span data-stu-id="98c89-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="98c89-239">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="98c89-239">Select **OK**.</span></span>

    <span data-ttu-id="98c89-240">De pagina **Alle inkooporders** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="98c89-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="98c89-241">Op de pagina **Alle inkooporders** in het sneltabblad **Inkooporderregels**, gebruikt u de knop **Regel toevoegen** om de volgende regels toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="98c89-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="98c89-242">Inkooporderregel 1:</span><span class="sxs-lookup"><span data-stu-id="98c89-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="98c89-243">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="98c89-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="98c89-244">**Hoeveelheid:** *10*</span><span class="sxs-lookup"><span data-stu-id="98c89-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="98c89-245">Inkooporderregel 2:</span><span class="sxs-lookup"><span data-stu-id="98c89-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="98c89-246">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="98c89-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="98c89-247">**Hoeveelheid:** *20*</span><span class="sxs-lookup"><span data-stu-id="98c89-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="98c89-248">Inkooporderregel 3:</span><span class="sxs-lookup"><span data-stu-id="98c89-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="98c89-249">**Artikelnummer:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="98c89-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="98c89-250">**Hoeveelheid:** *30*</span><span class="sxs-lookup"><span data-stu-id="98c89-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="98c89-251">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="98c89-252">Noteer het nummer van de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="98c89-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="98c89-253">Voorraad ontvangen en wegzetten vanaf het mobiele apparaat</span><span class="sxs-lookup"><span data-stu-id="98c89-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="98c89-254">De voorraad ontvangen en in een cluster sorteren</span><span class="sxs-lookup"><span data-stu-id="98c89-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="98c89-255">Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker die is ingesteld voor magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="98c89-255">Sign in to the Warehouse Management mobile app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="98c89-256">Selecteer **Inkomend** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="98c89-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="98c89-257">Selecteer in het menu **Inkomend** de optie **Cluster ontvangen en sorteren**.</span><span class="sxs-lookup"><span data-stu-id="98c89-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="98c89-258">Voer in het veld **Inkoopordernummer** het inkoopordernummer in.</span><span class="sxs-lookup"><span data-stu-id="98c89-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="98c89-259">Selecteer **OK** (vinkjesknop).</span><span class="sxs-lookup"><span data-stu-id="98c89-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="98c89-260">Selecteer het veld **Artikel**, voer het artikelnummer *A0001* in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="98c89-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="98c89-261">Selecteer het veld **Hoeveelheid**, voer *10* in met behulp van het numerieke blok en selecteer vervolgens de vinkjesknop.</span><span class="sxs-lookup"><span data-stu-id="98c89-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="98c89-262">Op de taakpagina **Hoeveelheid** selecteert u **OK** (vinkjesknop) om de ingevoerde hoeveelheid te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="98c89-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="98c89-263">Op de taakpagina **Artikel** selecteert u **OK** om te bevestigen dat artikel *A0001* is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="98c89-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="98c89-264">Selecteer het veld **Cluster-id** en voer een waarde in om een id toe te wijzen aan het cluster dat u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="98c89-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="98c89-265">De id die u hier invoert, wordt gebruikt wanneer de twee resterende artikelen op de inkooporder worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="98c89-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="98c89-266">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="98c89-266">Select **OK**.</span></span>

    <span data-ttu-id="98c89-267">De taakpagina **Inkoopordernummer** wordt weergegeven en toont een bericht dat het werk is voltooid.</span><span class="sxs-lookup"><span data-stu-id="98c89-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="98c89-268">Artikel *A0001* is nu ontvangen op de locatie *RECV* en is toegewezen aan de cluster-id die u in stap 10 hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="98c89-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="98c89-269">Herhaal stap 4 tot en met 11 om de overige twee artikelen van de inkooporder te ontvangen en toe te wijzen aan de cluster-id:</span><span class="sxs-lookup"><span data-stu-id="98c89-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="98c89-270">Een hoeveelheid van *20* voor artikel *A0002*</span><span class="sxs-lookup"><span data-stu-id="98c89-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="98c89-271">Een hoeveelheid van *30* voor artikel *M9215*</span><span class="sxs-lookup"><span data-stu-id="98c89-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="98c89-272">Het cluster afsluiten</span><span class="sxs-lookup"><span data-stu-id="98c89-272">Close the cluster</span></span>

<span data-ttu-id="98c89-273">Voordat de artikelen in het cluster kunnen worden weggezet, moet het cluster worden gesloten.</span><span class="sxs-lookup"><span data-stu-id="98c89-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="98c89-274">Ga in Supply Chain Management naar **Magazijnbeheer \> Werk \> Uitgaand \> Werkclusters**.</span><span class="sxs-lookup"><span data-stu-id="98c89-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="98c89-275">Op de pagina **Werkclusters**, in de sectie **Werkcluster** zoekt u in het veld **Cluster-id** naar de cluster-id die u eerder hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="98c89-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="98c89-276">Als het cluster niet wordt weergegeven, is het mogelijk al gesloten.</span><span class="sxs-lookup"><span data-stu-id="98c89-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="98c89-277">Om te bepalen of het cluster is gesloten, schakelt u het selectievakje **Gesloten werk weergeven** in en zoekt u naar de cluster-id die u eerder hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="98c89-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="98c89-278">Voer vervolgens een van deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="98c89-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="98c89-279">Als het cluster is gesloten, slaat u de resterende stappen van deze procedure over en gaat u door met de volgende procedure, [Het cluster wegzetten](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="98c89-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="98c89-280">Als het cluster niet is gesloten, voert u de resterende stappen van deze procedure uit om het cluster handmatig te sluiten.</span><span class="sxs-lookup"><span data-stu-id="98c89-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="98c89-281">Ga vervolgens door met de volgende procedure.</span><span class="sxs-lookup"><span data-stu-id="98c89-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="98c89-282">Selecteer in de sectie **Werkcluster** de cluster-id die u eerder hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="98c89-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="98c89-283">Selecteer **Cluster sluiten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="98c89-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="98c89-284">Nadat het cluster is afgesloten, wordt het niet meer weergegeven in de sectie **Werkcluster** (tenzij het selectievakje **Gesloten werk weergeven** is ingeschakeld).</span><span class="sxs-lookup"><span data-stu-id="98c89-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="98c89-285">Het cluster wegzetten</span><span class="sxs-lookup"><span data-stu-id="98c89-285">Put the cluster away</span></span>

1. <span data-ttu-id="98c89-286">Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker die is ingesteld voor magazijn *61*.</span><span class="sxs-lookup"><span data-stu-id="98c89-286">Sign in to the Warehouse Management mobile app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="98c89-287">Selecteer **Inkomend** in het hoofdmenu.</span><span class="sxs-lookup"><span data-stu-id="98c89-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="98c89-288">Selecteer in het menu **Inkomend** de optie **Cluster wegzetten**.</span><span class="sxs-lookup"><span data-stu-id="98c89-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="98c89-289">Selecteer **Cluster-id** en voer de cluster-id in die u eerder voor het gesloten cluster hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="98c89-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="98c89-290">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="98c89-290">Select **OK**.</span></span>

    <span data-ttu-id="98c89-291">De pagina **Cluster wegzetten: verzamelen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="98c89-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="98c89-292">Het bevat de cluster-ID, de orderverzamellocatie, de artikelen (de waarde *Meerdere* wordt weergegeven) en de totale hoeveelheid in het cluster dat moet worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="98c89-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="98c89-293">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="98c89-293">Select **OK**.</span></span>

    <span data-ttu-id="98c89-294">De pagina **Cluster wegzetten: plaatsen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="98c89-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="98c89-295">De instructies **Plaatsen** identificeren de cluster-id, de plaatsingslocatie, de artikelen, de totale hoeveelheid en de nummerplaat-id's voor de artikelen die op het cluster zijn ontvangen.</span><span class="sxs-lookup"><span data-stu-id="98c89-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="98c89-296">U hebt de standaardopties om deze stap te overschrijven of te negeren.</span><span class="sxs-lookup"><span data-stu-id="98c89-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="98c89-297">![De pagina Cluster wegzetten: plaatsen](media/Cluster_putaway-Put.png "De pagina Cluster wegzetten: plaatsen")</span><span class="sxs-lookup"><span data-stu-id="98c89-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="98c89-298">Selecteer **OK** om het wegzetten van het cluster te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="98c89-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="98c89-299">Het bericht Cluster voltooid wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="98c89-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="98c89-300">Opmerkingen en tips</span><span class="sxs-lookup"><span data-stu-id="98c89-300">Notes and tips</span></span>

<span data-ttu-id="98c89-301">Als de cluster-id de bovenliggende nummerplaat voor een genest pallet wordt, wordt de plaatsingspositie automatisch gegeven wanneer de cluster-id wordt gescand.</span><span class="sxs-lookup"><span data-stu-id="98c89-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="98c89-302">Er moet geen verdere nummerplaat worden gescand, zelfs als het genereren van nummerplaten is ingesteld op handmatig.</span><span class="sxs-lookup"><span data-stu-id="98c89-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]