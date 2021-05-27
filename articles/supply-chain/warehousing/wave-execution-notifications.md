---
title: Meldingen voor uitvoering van wave
description: In dit onderwerp worden meldingen voor uitvoeringen van waves beschreven en wordt uitgelegd hoe u deze instelt.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fee112d3211f619b2146dd21c4f8a52ad33667d6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019149"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="b7f1c-103">Meldingen voor uitvoering van wave</span><span class="sxs-lookup"><span data-stu-id="b7f1c-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="b7f1c-104">De functie *Wave-uitvoeringsmeldingen* maakt gebruik van zakelijke gebeurtenissen en het Actiecentrum om meldingen te leveren die verband houden met de uitvoering van een wave.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="b7f1c-105">U kunt hiermee de typen gebeurtenissen opgeven die meldingen genereren, de magazijnen die ze genereren en de gebruikers die ze ontvangen.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="b7f1c-106">De knop **Berichten weergeven** (belsymbool) aan de rechterkant van de navigatiebalk geeft aan wanneer een bericht uit het Actiecentrum beschikbaar is voor de huidige gebruiker.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="b7f1c-107">De gebruiker kan de knop **Berichten weergeven** selecteren om het Actiecentrum te openen en de berichten te bekijken.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="b7f1c-108">Zakelijke gebeurtenissen vinden plaats wanneer bedrijfsprocessen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="b7f1c-109">Bedrijfsprocessen bestaan uit taken.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="b7f1c-110">Tijdens een bedrijfsproces voeren de gebruikers die eraan deelnemen zakelijke acties uit om die taken te voltooien.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="b7f1c-111">Zakelijke gebeurtenissen bieden een mechanisme waarmee externe systemen meldingen vanuit Finance and Operations-toepassingen kunnen ontvangen.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="b7f1c-112">Op deze manier kunnen de systemen zakelijke acties uitvoeren als reactie op de zakelijke gebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="b7f1c-113">Zie [Overzicht van zakelijke gebeurtenissen](../../fin-ops-core/dev-itpro/business-events/home-page.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="b7f1c-114">De functie Meldingen voor uitvoering van wave inschakelen</span><span class="sxs-lookup"><span data-stu-id="b7f1c-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="b7f1c-115">Voordat u de functie *Meldingen voor uitvoering van wave* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b7f1c-116">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b7f1c-117">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="b7f1c-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b7f1c-118">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b7f1c-119">**Functienaam:** *Meldingen voor uitvoering van wave*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="b7f1c-120">Scenario: meldingen voor batchuitvoeringen van waves naar het Actiecentrum verzenden</span><span class="sxs-lookup"><span data-stu-id="b7f1c-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="b7f1c-121">In dit scenario wordt de end-to-end stroom weergegeven voor het verzenden van meldingen over fouten bij het uitvoeren van wavebatches naar een specifieke rol via het Actiecentrum.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="b7f1c-122">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="b7f1c-122">Make demo data available</span></span>

<span data-ttu-id="b7f1c-123">Voor dit scenario moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon **USMF** selecteren.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="b7f1c-124">Zorg ervoor dat waves worden uitgevoerd in batchmodus</span><span class="sxs-lookup"><span data-stu-id="b7f1c-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="b7f1c-125">Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="b7f1c-126">Stel op het sneltabblad **Waveverwerking** de optie **Waves verwerken in batch** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="b7f1c-127">Als u meldingen voor het uitvoeren van wavebatches wilt uitschakelen, stelt u de optie **Batchmeldingen voor waveverwerking uitschakelen** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="b7f1c-128">Een wavemeldingsbeleid configureren</span><span class="sxs-lookup"><span data-stu-id="b7f1c-128">Configure a wave notification policy</span></span>

<span data-ttu-id="b7f1c-129">Wavemeldingsbeleid definieert de typen meldingen die worden verzonden en de gebruikers die een melding ontvangen.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="b7f1c-130">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavemeldingsbeleid**.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="b7f1c-131">Maak een record met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="b7f1c-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="b7f1c-132">**Wavemeldingsbeleid:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="b7f1c-133">**Beschrijving**: *Wavebatchfout voor magazijn 24*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="b7f1c-134">**Melding verzenden bij**: *Alleen fout*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="b7f1c-135">**Naar rol:** *Systeembeheerder*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="b7f1c-136">Omdat dit scenario demogegevens gebruikt, wordt de rol *Systeembeheerder* geselecteerd omwille van de eenvoud.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="b7f1c-137">Daarom ontvangt u de meldingen omdat u bent aangemeld als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="b7f1c-138">In de praktijk moet u echter meestal een meer specifieke rol selecteren om te informeren over fouten bij het uitvoeren van wavebatches, zoals *Magazijnmanager*.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="b7f1c-139">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="b7f1c-140">Een wavesjabloon configureren</span><span class="sxs-lookup"><span data-stu-id="b7f1c-140">Configure a wave template</span></span>

<span data-ttu-id="b7f1c-141">Met wavesjablonen kunt u specifieke exemplaren van wavemethoden koppelen aan corresponderende wavelabelsjablonen.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="b7f1c-142">Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b7f1c-143">Stel in het lijstvenster het veld **Type wavesjabloon** in op *Verzending* en selecteer vervolgens de wavesjabloon *24 Standaardverzending* voor magazijn 24.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="b7f1c-144">Stel op het sneltabblad **Algemeen** het veld **Wavemeldingsbeleid** in op *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="b7f1c-145">Een werksjabloon configureren</span><span class="sxs-lookup"><span data-stu-id="b7f1c-145">Configure a work template</span></span>

<span data-ttu-id="b7f1c-146">Werksjablonen worden tijdens de uitvoering van de wave gebruikt om werk te genereren.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="b7f1c-147">Voor dit scenario zou wave-uitvoering een fout moeten veroorzaken.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="b7f1c-148">Door de werksjabloonquery in te stellen om een niet-bestaand magazijn te gebruiken, zorgt u ervoor dat de uitvoering van de wave mislukt en er een melding wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="b7f1c-149">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b7f1c-150">Stel in het lijstvenster het veld **Type werksjabloon** in op *Verkooporders* en selecteer vervolgens de werksjabloon *24 SO Stage* voor magazijn 24.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="b7f1c-151">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="b7f1c-152">Bewerk in het dialoogvenster query-editor op het tabblad **Bereik** de volgende rij (of voeg deze toe als deze niet bestaat):</span><span class="sxs-lookup"><span data-stu-id="b7f1c-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="b7f1c-153">**Tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="b7f1c-154">**Afgeleide tabel:** *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="b7f1c-155">**Veld:** *Magazijn*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="b7f1c-156">**Criteria**: wijzig de waarde van *24* in *Fout*.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="b7f1c-157">Selecteer **OK** en bevestig de wijziging.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="b7f1c-158">Een verkooporder maken en vrijgeven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="b7f1c-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="b7f1c-159">Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="b7f1c-160">Maak een verkooporder met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="b7f1c-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b7f1c-161">**Klantrekening:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b7f1c-162">**Magazijn:** *24*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="b7f1c-163">Voeg op het sneltabblad **Verkooporderregels** een verkooporderregel toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="b7f1c-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="b7f1c-164">**Artikelnummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b7f1c-165">**Hoeveelheid:** *10*</span><span class="sxs-lookup"><span data-stu-id="b7f1c-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="b7f1c-166">Deze artikelen en hoeveelheden zijn slechts voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-166">These items and quantities are only examples.</span></span> <span data-ttu-id="b7f1c-167">Er moet voldoende voorraad aanwezig zijn in het opgegeven magazijn.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="b7f1c-168">Terwijl de nieuwe regel nog steeds is geselecteerd op het sneltabblad **Verkooporderregels**, selecteert u **Voorraad \> Reservering** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="b7f1c-169">Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren**.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="b7f1c-170">Sluit de pagina vervolgens.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-170">Then close the page.</span></span>
1. <span data-ttu-id="b7f1c-171">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="b7f1c-172">Meldingen van uitvoering van wavebatchtaken</span><span class="sxs-lookup"><span data-stu-id="b7f1c-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="b7f1c-173">Afhankelijk van de installatie van uw zakelijke gebeurtenissen ontvangt u uiteindelijk een melding over een storing bij de uitvoering van de wave.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="b7f1c-174">Het bericht uit het Actiecentrum lijkt op het volgende voorbeeld en bevat een koppeling naar de wave die is mislukt.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="b7f1c-175">**Fout tijdens uitvoering van wave**</span><span class="sxs-lookup"><span data-stu-id="b7f1c-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="b7f1c-176">Er is een fout opgetreden tijdens het uitvoeren van wave USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="b7f1c-177">Laatste berichten: Er is geen werk gemaakt voor Wave USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="b7f1c-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="b7f1c-178">**STATUS**</span><span class="sxs-lookup"><span data-stu-id="b7f1c-178">**STATUS**</span></span>  
> <span data-ttu-id="b7f1c-179">Actief</span><span class="sxs-lookup"><span data-stu-id="b7f1c-179">Active</span></span>
>
> <span data-ttu-id="b7f1c-180">Wavegegevens openen</span><span class="sxs-lookup"><span data-stu-id="b7f1c-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
