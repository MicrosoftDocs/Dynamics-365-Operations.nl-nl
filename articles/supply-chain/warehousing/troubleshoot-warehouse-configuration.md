---
title: Problemen met magazijnconfiguratie oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens het configureren van Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814387"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="ec02a-103">Problemen met magazijnconfiguratie oplossen</span><span class="sxs-lookup"><span data-stu-id="ec02a-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec02a-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens het configureren van Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec02a-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="ec02a-105">Het volgende foutbericht wordt weergegeven: "De nummerplaat of locatie is niet geldig."</span><span class="sxs-lookup"><span data-stu-id="ec02a-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ec02a-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ec02a-106">Issue description</span></span>

<span data-ttu-id="ec02a-107">Dit foutbericht wordt weergegeven wanneer u een nummerplaat-id of locatie scant.</span><span class="sxs-lookup"><span data-stu-id="ec02a-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ec02a-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ec02a-108">Issue resolution</span></span>

<span data-ttu-id="ec02a-109">Controleer of de id van de nummerplaat niet al is gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="ec02a-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="ec02a-110">Dit probleem doet zich voor wanneer de waarde die een gebruiker in de mobiele app Magazijnbeheer heeft gescand zowel een geldige locatie als een geldige id voor een nummerplaat is.</span><span class="sxs-lookup"><span data-stu-id="ec02a-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="ec02a-111">Dit probleem is echter opgelost in versie 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="ec02a-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="ec02a-112">Het volgende foutbericht wordt weergegeven: "De nummerplaat moet worden opgegeven voor deze locatie."</span><span class="sxs-lookup"><span data-stu-id="ec02a-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ec02a-113">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ec02a-113">Issue description</span></span>

<span data-ttu-id="ec02a-114">Dit foutbericht wordt weergegeven als u een overboekingsorder maakt met behulp van een magazijn dat is ingeschakeld voor geavanceerd magazijnbeheer (WMS) en vervolgens, als het werk is voltooid, probeert u de zending te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="ec02a-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ec02a-115">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ec02a-115">Issue resolution</span></span>

<span data-ttu-id="ec02a-116">Het veld **Standaardlocatie voor ontvangst** is leeg voor een transitmagazijn van het van-magazijn.</span><span class="sxs-lookup"><span data-stu-id="ec02a-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="ec02a-117">U kunt dit probleem oplossen door een standaardlocatie voor ontvangst op te geven in het transitmagazijn.</span><span class="sxs-lookup"><span data-stu-id="ec02a-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="ec02a-118">Zorg ervoor dat deze locatie een door nummerplaten beheerde locatie is.</span><span class="sxs-lookup"><span data-stu-id="ec02a-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="ec02a-119">Het volgende foutbericht wordt weergegeven: "U kunt geen werksjabloonregel maken voor Wijziging van voorraadstatus, omdat het werktype niet geldig is.</span><span class="sxs-lookup"><span data-stu-id="ec02a-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="ec02a-120">Selecteer een ander werktype."</span><span class="sxs-lookup"><span data-stu-id="ec02a-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ec02a-121">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ec02a-121">Issue description</span></span>

<span data-ttu-id="ec02a-122">Voor een werksjabloon kunt u *Wijziging van voorraadstatus* niet selecteren in de kolom **Werktype** van de sectie **Werksjabloongegevens**.</span><span class="sxs-lookup"><span data-stu-id="ec02a-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ec02a-123">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ec02a-123">Issue resolution</span></span>

<span data-ttu-id="ec02a-124">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="ec02a-124">This behavior is by design.</span></span> <span data-ttu-id="ec02a-125">Het werktype *Wijziging van voorraadstatus* wordt alleen door systeemprocessen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ec02a-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="ec02a-126">Deze waarde kan niet worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="ec02a-126">It can't be configured.</span></span> <span data-ttu-id="ec02a-127">Omdat de lijst met werktypen vast ligt als opsomming, kunnen de extra vermeldingen niet worden gefilterd uit de vervolgkeuzelijst **Werktype**.</span><span class="sxs-lookup"><span data-stu-id="ec02a-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="ec02a-128">Het volgende foutbericht wordt weergegeven: "De hoeveelheid is niet geldig voor eenheid 1%."</span><span class="sxs-lookup"><span data-stu-id="ec02a-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ec02a-129">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ec02a-129">Issue description</span></span>

<span data-ttu-id="ec02a-130">De hoeveelheid is niet geldig voor de eenheid *ea* wanneer er orderverzamelingswerk is met meerdere nummerplaten op één locatie.</span><span class="sxs-lookup"><span data-stu-id="ec02a-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ec02a-131">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ec02a-131">Issue resolution</span></span>

<span data-ttu-id="ec02a-132">Controleer of de velden **Volgordegroep-id eenheid** en **Eenheidsomrekeningen** op het vrijgegeven product of de productvariant juist zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ec02a-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="ec02a-133">Het foutbericht is verbeterd in versie 10.0.15 (zie [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="ec02a-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="ec02a-134">Het nieuwe foutbericht is, "De hoeveelheid is niet geldig.</span><span class="sxs-lookup"><span data-stu-id="ec02a-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="ec02a-135">Verwacht wordt %1 %2."</span><span class="sxs-lookup"><span data-stu-id="ec02a-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="ec02a-136">In de locatie-instructies voor het wegzetwerk van verkooporders, worden met de optie voor meerdere SKU'S niet meerdere acties van een locatie-instructie geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="ec02a-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ec02a-137">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ec02a-137">Issue description</span></span>

<span data-ttu-id="ec02a-138">Locatie-instructies van het werkordertype *Verkooporders* en het werktype *Wegzetten* evalueren meerdere acties van een locatie-instructie niet wanneer de optie **Meerdere SKU's** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ec02a-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="ec02a-139">Alleen de eerste actie van een locatie-instructie wordt geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="ec02a-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ec02a-140">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ec02a-140">Issue resolution</span></span>

<span data-ttu-id="ec02a-141">Een nieuwe functie *Alle acties van locatie-instructies voor meerdere SKU's evalueren* is toegevoegd in versie 10.0.15 (zie [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="ec02a-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="ec02a-142">Met deze functie worden alle acties van locatie-instructies voor meerdere SKU's geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="ec02a-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="ec02a-143">Als u deze functie nodig hebt, kunt u deze met [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ec02a-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="ec02a-144">Ik kan de mobiele app Magazijnbeheer niet gebruiken om gedeeltelijke orderverzameling uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="ec02a-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ec02a-145">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ec02a-145">Issue description</span></span>

<span data-ttu-id="ec02a-146">Voor verkoop- en overboekingsorders kunt u geen artikelen overslaan en gedeeltelijke orderverzameling uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ec02a-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ec02a-147">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ec02a-147">Issue resolution</span></span>

<span data-ttu-id="ec02a-148">Schakel op de pagina **Menuopties voor mobiel apparaat** voor elke menuopdracht die is ingesteld op het verwerken van verkooporders of overboekingsorders de optie **Splitsing van werk toestaan** op het sneltabblad **Algemeen** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="ec02a-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="ec02a-149">Hoe kan ik een voorraadstatus wijzigen voor een gedeeltelijke hoeveelheid werk?</span><span class="sxs-lookup"><span data-stu-id="ec02a-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="ec02a-150">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ec02a-150">Issue description</span></span>

<span data-ttu-id="ec02a-151">U wilt een voorraadstatus wijzigen voor een gedeeltelijke hoeveelheid van een batch.</span><span class="sxs-lookup"><span data-stu-id="ec02a-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ec02a-152">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ec02a-152">Issue resolution</span></span>

<span data-ttu-id="ec02a-153">Om werknemers in staat te stellen deze wijziging door te voeren, kunt u een menuopdracht maken voor de mobiele app Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="ec02a-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="ec02a-154">Maak (of bewerk) op de pagina **Menuopties voor mobiel apparaat** een menuopdracht met een van de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="ec02a-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="ec02a-155">**Modus:** *werk*</span><span class="sxs-lookup"><span data-stu-id="ec02a-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="ec02a-156">**Bestaand werk gebruiken:** *Nee*</span><span class="sxs-lookup"><span data-stu-id="ec02a-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="ec02a-157">**Procedure voor het maken van werk:** *Verplaatsing*</span><span class="sxs-lookup"><span data-stu-id="ec02a-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="ec02a-158">**Voorraadstatus weergeven:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="ec02a-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="ec02a-159">U kunt desgewenst andere velden op de pagina instellen.</span><span class="sxs-lookup"><span data-stu-id="ec02a-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="ec02a-160">Het dockbeheerprofiel van een locatieprofiel zorgt er niet voor dat voorraadtypen niet worden gemengd.</span><span class="sxs-lookup"><span data-stu-id="ec02a-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ec02a-161">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ec02a-161">Issue description</span></span>

<span data-ttu-id="ec02a-162">U maakt gebruik van *Beleidsregels voor samenvoegen van zendingen*.</span><span class="sxs-lookup"><span data-stu-id="ec02a-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="ec02a-163">U hebt een *dockbeheerprofiel* ingesteld voor een *locatieprofiel*, maar wanneer er werk wordt gemaakt, worden de voorraadtypen gemengd op de laatste locatie.</span><span class="sxs-lookup"><span data-stu-id="ec02a-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ec02a-164">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ec02a-164">Issue resolution</span></span>

<span data-ttu-id="ec02a-165">Voor dockbeheerprofielen moet werk vooraf worden opgesplitst.</span><span class="sxs-lookup"><span data-stu-id="ec02a-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="ec02a-166">Met andere woorden, het dockbeheerprofiel verwacht dat een werkkoptekst niet meerdere wegzetlocaties bevat.</span><span class="sxs-lookup"><span data-stu-id="ec02a-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="ec02a-167">Er moet een werkkoptekstopsplitsing worden ingesteld om het mengen van voorraad op een effectieve manier te beheren via het dockbeheerprofiel.</span><span class="sxs-lookup"><span data-stu-id="ec02a-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="ec02a-168">In dit voorbeeld is ons dockbeheerprofiel zo geconfigureerd dat **Voorraadtypen die niet mogen worden gemengd** wordt ingesteld op *Zending-id*. Hiervoor stellen we een werkkoptekstopsplitsing in:</span><span class="sxs-lookup"><span data-stu-id="ec02a-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="ec02a-169">Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="ec02a-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ec02a-170">Selecteer het **Werkordertype** dat u wilt bewerken (bijvoorbeeld *Inkooporders*).</span><span class="sxs-lookup"><span data-stu-id="ec02a-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="ec02a-171">Selecteer de werksjabloon die u wilt bewerken.</span><span class="sxs-lookup"><span data-stu-id="ec02a-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="ec02a-172">Selecteer **Query bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ec02a-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="ec02a-173">Open het tabblad **Sorteren** en voeg een rij toe met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="ec02a-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="ec02a-174">**Tabel** - *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="ec02a-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="ec02a-175">**Afgeleide tabel** - *Tijdelijke werktransacties*</span><span class="sxs-lookup"><span data-stu-id="ec02a-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="ec02a-176">**Veld** - *Zending-id*</span><span class="sxs-lookup"><span data-stu-id="ec02a-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="ec02a-177">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec02a-177">Select **OK**.</span></span>
1. <span data-ttu-id="ec02a-178">U keert terug naar de pagina **Werksjablonen**.</span><span class="sxs-lookup"><span data-stu-id="ec02a-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="ec02a-179">Selecteer **Opsplitsingen voor werkkoptekst** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ec02a-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="ec02a-180">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ec02a-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ec02a-181">Schakel het selectievakje in dat is gekoppeld aan de **veldnaam** *Zending-id*.</span><span class="sxs-lookup"><span data-stu-id="ec02a-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="ec02a-182">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ec02a-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
