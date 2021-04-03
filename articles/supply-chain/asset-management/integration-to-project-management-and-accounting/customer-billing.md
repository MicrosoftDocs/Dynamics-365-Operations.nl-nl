---
title: Factureren voor onderhoud aan activa van klanten
description: In dit onderwerp wordt uitgelegd hoe u onderhoudswerkzaamheden aan de activa die uw klanten in eigendom hebben, maakt, verwerkt en factureert.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a93436d101e6201c9d86279ea5b1a37fcc644fd1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500449"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="22f8e-103">Factureren voor onderhoud aan activa van klanten</span><span class="sxs-lookup"><span data-stu-id="22f8e-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="22f8e-104">Met de functie *Facturering werkorder* kunt u onderhoudswerk maken, verwerken en factureren dat wordt uitgevoerd op activa van uw klanten.</span><span class="sxs-lookup"><span data-stu-id="22f8e-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="22f8e-105">Met deze functie kunt u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="22f8e-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="22f8e-106">Klanten koppelen aan de activa waarvan ze eigenaar zijn.</span><span class="sxs-lookup"><span data-stu-id="22f8e-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="22f8e-107">Een klant selecteren en de activa bekijken die klant bezit wanneer u een werkorder maakt.</span><span class="sxs-lookup"><span data-stu-id="22f8e-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="22f8e-108">Een bovenliggend project instellen voor elke klant.</span><span class="sxs-lookup"><span data-stu-id="22f8e-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="22f8e-109">Uren, artikelen, onkosten en tarieven voor de werkorder registreren en vervolgens later een factuurvoorstel maken voor de klant.</span><span class="sxs-lookup"><span data-stu-id="22f8e-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="22f8e-110">Bovendien bevat de functie de volgende functionaliteit:</span><span class="sxs-lookup"><span data-stu-id="22f8e-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="22f8e-111">Het projectcontract uit het bovenliggende project van een klant wordt automatisch gekopieerd naar het relevante werkorderproject.</span><span class="sxs-lookup"><span data-stu-id="22f8e-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="22f8e-112">Activabeheer kan nu het type projecttransactie *tarief* gebruiken voor zowel werkorderprognoses als werkorderjournalen.</span><span class="sxs-lookup"><span data-stu-id="22f8e-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="22f8e-113">De functie klant factureren inschakelen</span><span class="sxs-lookup"><span data-stu-id="22f8e-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="22f8e-114">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="22f8e-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="22f8e-115">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="22f8e-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="22f8e-116">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="22f8e-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="22f8e-117">**Module:** *Projectbeheer en boekhouding*</span><span class="sxs-lookup"><span data-stu-id="22f8e-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="22f8e-118">**Functienaam:** *Facturering werkorder*</span><span class="sxs-lookup"><span data-stu-id="22f8e-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="22f8e-119">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="22f8e-119">Example scenario</span></span>

<span data-ttu-id="22f8e-120">Als u wilt weten hoe deze functie werkt, doorloopt u de volgende voorbeeldscenario's.</span><span class="sxs-lookup"><span data-stu-id="22f8e-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="22f8e-121">Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="22f8e-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="22f8e-122">U moet de rechtspersoon **USMF** selecteren voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="22f8e-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="22f8e-123">U kunt dit scenario ook gebruiken als instructie voor het gebruik van deze functie wanneer u met een productiesysteem werkt.</span><span class="sxs-lookup"><span data-stu-id="22f8e-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="22f8e-124">In dat geval moet u echter uw eigen waarden vervangen en hebt u mogelijk niet de beschikking over bepaalde typen vereiste records die met de standaard demogegevens worden verstrekt.</span><span class="sxs-lookup"><span data-stu-id="22f8e-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="22f8e-125">Stap 1: Een nieuw projectcontract voor de klant maken</span><span class="sxs-lookup"><span data-stu-id="22f8e-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="22f8e-126">Ga naar **Projectbeheer en boekhouding \> Projecten \> Projectcontracten**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="22f8e-127">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="22f8e-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="22f8e-128">Stel in het dialoogvenster **Nieuw projectcontract** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="22f8e-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="22f8e-129">**Naam:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="22f8e-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="22f8e-130">**Financieringstype:** *Klant*</span><span class="sxs-lookup"><span data-stu-id="22f8e-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="22f8e-131">**Financieringsbron:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="22f8e-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="22f8e-132">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="22f8e-133">Stap 2: Een nieuw bovenliggend project voor de klant maken</span><span class="sxs-lookup"><span data-stu-id="22f8e-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="22f8e-134">Het bovenliggende project dat u hier maakt, wordt gebruikt wanneer werkorders voor de klant worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="22f8e-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="22f8e-135">Ga naar **Projectbeheer en boekhouding \> Projecten \> Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="22f8e-136">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="22f8e-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="22f8e-137">Stel in het dialoogvenster **Nieuw project** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="22f8e-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="22f8e-138">**Projecttype:** *Tijd en materiaal*</span><span class="sxs-lookup"><span data-stu-id="22f8e-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="22f8e-139">**Projectnaam:** *Pelican Wholesales-werkorders*</span><span class="sxs-lookup"><span data-stu-id="22f8e-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="22f8e-140">**Projectgroep:** *TM*</span><span class="sxs-lookup"><span data-stu-id="22f8e-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="22f8e-141">**Projectcontract-ID:** *Pelican Wholesales* (het contract dat u eerder hebt gemaakt)</span><span class="sxs-lookup"><span data-stu-id="22f8e-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="22f8e-142">**Begindatum:** Selecteer de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="22f8e-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="22f8e-143">Selecteer **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-143">Select **Create project**.</span></span>
1. <span data-ttu-id="22f8e-144">Het nieuwe project wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="22f8e-144">The new project is opened.</span></span> <span data-ttu-id="22f8e-145">Noteer de **Project-ID**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="22f8e-146">U moet deze later invoeren.</span><span class="sxs-lookup"><span data-stu-id="22f8e-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="22f8e-147">Stap 3: Een nieuw type werkorder maken in Activabeheer</span><span class="sxs-lookup"><span data-stu-id="22f8e-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="22f8e-148">Ga naar **Activabeheer \> Instellen \> Werkorder \> Werkordertypen**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="22f8e-149">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="22f8e-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="22f8e-150">Er wordt een nieuwe record aan de lijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="22f8e-150">A new record is added to the list.</span></span> <span data-ttu-id="22f8e-151">Stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="22f8e-151">Set the following values for it:</span></span>

    - <span data-ttu-id="22f8e-152">**Werkordertype:** *Service*</span><span class="sxs-lookup"><span data-stu-id="22f8e-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="22f8e-153">**Naam:** *Servicewerkorders*</span><span class="sxs-lookup"><span data-stu-id="22f8e-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="22f8e-154">**Levenscyclusstatus van werkorder:** *Standaard*</span><span class="sxs-lookup"><span data-stu-id="22f8e-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="22f8e-155">Stap 4: Het klantaccount aan het bovenliggende project koppelen</span><span class="sxs-lookup"><span data-stu-id="22f8e-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="22f8e-156">U moet nu het klantaccount koppelen aan het bovenliggende project in de projectinstellingen in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="22f8e-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="22f8e-157">Ga naar **Activabeheer \> Instellen \> Werkorders \> Projectinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="22f8e-158">Selecteer op het tabblad **Bovenliggend project** de optie **Toevoegen** om een regel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="22f8e-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="22f8e-159">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="22f8e-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22f8e-160">**Klantaccount:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="22f8e-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="22f8e-161">**Project-ID:** Voer de project-ID in die u eerder hebt genoteerd.</span><span class="sxs-lookup"><span data-stu-id="22f8e-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="22f8e-162">Stap 5: De projectgroep en het type koppelen aan het werkorderproject</span><span class="sxs-lookup"><span data-stu-id="22f8e-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="22f8e-163">U moet nog steeds op de pagina **Projectinstellingen** staan (**Activabeheer \> Instellen \> Werkorders \> Projectinstellingen**).</span><span class="sxs-lookup"><span data-stu-id="22f8e-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="22f8e-164">Selecteer op het tabblad **Projectgroep** de optie **Toevoegen** om een regel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="22f8e-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="22f8e-165">Stel op de nieuwe regel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="22f8e-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22f8e-166">**Type werkorder:** *Service* (het werkordertype dat u eerder hebt gemaakt)</span><span class="sxs-lookup"><span data-stu-id="22f8e-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="22f8e-167">**Projectgroep:** *TM*</span><span class="sxs-lookup"><span data-stu-id="22f8e-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="22f8e-168">Het projectcontract voor het werkorderproject wordt altijd overgenomen van het bovenliggende project.</span><span class="sxs-lookup"><span data-stu-id="22f8e-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="22f8e-169">Stap 6: Een activum aan de klant-ID koppelen</span><span class="sxs-lookup"><span data-stu-id="22f8e-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="22f8e-170">Ga naar **Activabeheer \> Activa \> Actieve activa**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="22f8e-171">Voer in het veld **Filter** *VE-102* in en selecteer om te filteren op **Activum**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="22f8e-172">Selecteer het activum om de instellingen te openen.</span><span class="sxs-lookup"><span data-stu-id="22f8e-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="22f8e-173">Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="22f8e-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="22f8e-174">Het veld **Naam** wordt automatisch bijgewerkt naar *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="22f8e-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="22f8e-175">Stap 7: Een nieuw type werkorder maken voor het activum</span><span class="sxs-lookup"><span data-stu-id="22f8e-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="22f8e-176">Ga naar **Activabeheer \> Werkorders \> Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="22f8e-177">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="22f8e-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="22f8e-178">Stel in het dialoogvenster **Werkorder maken** de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="22f8e-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="22f8e-179">**Werkordertype:** *Service*</span><span class="sxs-lookup"><span data-stu-id="22f8e-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="22f8e-180">**Omschrijving:** *Vrachtwagen repareren*</span><span class="sxs-lookup"><span data-stu-id="22f8e-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="22f8e-181">**Klantaccount:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="22f8e-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="22f8e-182">**Activum:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="22f8e-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="22f8e-183">De opzoekactie toont alleen activa die aan het geselecteerde klantaccount zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="22f8e-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="22f8e-184">**Onderhoudstaaktype:** *Repareren*</span><span class="sxs-lookup"><span data-stu-id="22f8e-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="22f8e-185">**Handel:** *Mechanisch*</span><span class="sxs-lookup"><span data-stu-id="22f8e-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="22f8e-186">**Serviceniveau:** *4*</span><span class="sxs-lookup"><span data-stu-id="22f8e-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="22f8e-187">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="22f8e-188">Stap 8: De werkorder controleren en er aan beginnen te werken</span><span class="sxs-lookup"><span data-stu-id="22f8e-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="22f8e-189">In deze sectie werkt u aan de werkorder die u in de vorige sectie hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="22f8e-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="22f8e-190">Volg deze stappen om te controleren of het bovenliggende project het project *Pelican Wholesales-werkorder* is:</span><span class="sxs-lookup"><span data-stu-id="22f8e-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="22f8e-191">Selecteer in de sectie **Onderhoudstaken voor werkorders** een regel.</span><span class="sxs-lookup"><span data-stu-id="22f8e-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="22f8e-192">Controleer op het sneltabblad **Regeldetails** de waarde **Project-ID**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="22f8e-193">Dit moet een nummer met een streepje zijn in de vorm *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="22f8e-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="22f8e-194">Deze waarde is een koppeling.</span><span class="sxs-lookup"><span data-stu-id="22f8e-194">This value is a link.</span></span>
    1. <span data-ttu-id="22f8e-195">Selecteer de koppeling van een project-ID om een pagina te openen waarin u het bovenliggende project en de projectnamen kunt bekijken.</span><span class="sxs-lookup"><span data-stu-id="22f8e-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="22f8e-196">Selecteer in het actievenster op het tabblad **Werkorder** in de groep **Levenscyclusstatus** de optie **Status van werkorder bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="22f8e-197">Schakel in het dialoogvenster **Status van werkorder bijwerken** in de kolom **Selecteren** het selectievakje in voor de rij waar het veld **Levenscyclusstatus** is ingesteld op *In uitvoering*.</span><span class="sxs-lookup"><span data-stu-id="22f8e-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="22f8e-198">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-198">Select **OK**.</span></span>
1. <span data-ttu-id="22f8e-199">Klik in het dialoogvenster **Levenscyclusstatus: in uitvoering** op **OK**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="22f8e-200">Stap 9: De uren die aan de werkorder zijn besteed boeken en een nieuw factuurvoorstel maken</span><span class="sxs-lookup"><span data-stu-id="22f8e-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="22f8e-201">In deze sectie werkt u door aan de werkorder waaraan u werkte in de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="22f8e-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="22f8e-202">Ga in het Actievenster naar het tabblad **Werkorder** en selecteer in de groep **Project** de optie **Journalen**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="22f8e-203">De pagina **Werkorderjournalen** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="22f8e-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="22f8e-204">Hier kunt u de tijd registreren die u aan de werkorder hebt besteed.</span><span class="sxs-lookup"><span data-stu-id="22f8e-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="22f8e-205">Selecteer op het sneltabblad **Uren** de optie **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="22f8e-206">Stel op de nieuwe regel het veld **Uren** in op *4*.</span><span class="sxs-lookup"><span data-stu-id="22f8e-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="22f8e-207">Selecteer **Journalen boeken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="22f8e-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="22f8e-208">Sluit de pagina **Werkorderjournalen** om terug te keren naar de werkorder.</span><span class="sxs-lookup"><span data-stu-id="22f8e-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="22f8e-209">Selecteer in het actievenster op het tabblad **Factureren** de optie **Nieuw factuurvoorstel**.</span><span class="sxs-lookup"><span data-stu-id="22f8e-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="22f8e-210">Schakel in het dialoogvenster **Factuurvoorstel maken** in de sectie **Projecttransacties** het selectievakje **Selecteren** in voor elke regel die u wilt factureren.</span><span class="sxs-lookup"><span data-stu-id="22f8e-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="22f8e-211">Selecteer **OK** om het dialoogvenster te sluiten en het nieuwe factuurvoorstel te bekijken.</span><span class="sxs-lookup"><span data-stu-id="22f8e-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]