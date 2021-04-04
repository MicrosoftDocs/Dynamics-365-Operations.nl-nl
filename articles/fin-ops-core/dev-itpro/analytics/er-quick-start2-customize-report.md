---
title: Een ER-indeling aanpassen om een aangepast elektronisch document te genereren
description: In dit onderwerp wordt uitgelegd hoe u een door Microsoft geleverde ER-indeling (Electronic Reporting) kunt aanpassen, zodat een aangepast elektronisch document wordt gegenereerd.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c643c913d9bc9233c891709593dff995284e2e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568992"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="cade4-103">Een ER-indeling aanpassen om een aangepast elektronisch document te genereren</span><span class="sxs-lookup"><span data-stu-id="cade4-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cade4-104">In de procedures in dit onderwerp wordt uitgelegd hoe een gebruiker in de rol Systeembeheerder of Functioneel consultant elektronische rapportage deze taken kan uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="cade4-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="cade4-105">[Parameters voor het ER-raamwerk (elektronische rapportage) configureren](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="cade4-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="cade4-106">Door Microsoft geleverde ER-configuraties importeren, waarmee een betalingsbestand wordt gegenereerd terwijl een [leveranciers betaling](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="cade4-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="cade4-107">Een aangepaste versie maken van een standaardconfiguratie voor een ER-indeling die door Microsoft wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="cade4-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="cade4-108">De aangepaste ER-indelingsconfiguratie aanpassen, zodat betalingsbestanden worden gegenereerd die voldoen aan de vereisten van een specifieke bank.</span><span class="sxs-lookup"><span data-stu-id="cade4-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="cade4-109">Wijzigingen in de standaardconfiguraties voor ER-indelingen overnemen in de aangepaste ER-indelingsconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="cade4-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="cade4-110">U kunt alle volgende procedures uitvoeren in het bedrijf **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="cade4-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="cade4-111">U hoeft hiervoor geen code te schrijven.</span><span class="sxs-lookup"><span data-stu-id="cade4-111">No coding is required.</span></span>

- [<span data-ttu-id="cade4-112">Het ER-raamwerk configureren</span><span class="sxs-lookup"><span data-stu-id="cade4-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="cade4-113">ER-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="cade4-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="cade4-114">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="cade4-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="cade4-115">De lijst met ER-configuratie providers bekijken</span><span class="sxs-lookup"><span data-stu-id="cade4-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="cade4-116">Een nieuwe ER-configuratieprovider toevoegen</span><span class="sxs-lookup"><span data-stu-id="cade4-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="cade4-117">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="cade4-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="cade4-118">De standaardconfiguraties voor ER-indeling importeren</span><span class="sxs-lookup"><span data-stu-id="cade4-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="cade4-119">De standaard-ER-configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="cade4-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="cade4-120">De geïmporteerde ER-configuraties bekijken</span><span class="sxs-lookup"><span data-stu-id="cade4-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="cade4-121">Een leveranciersbetaling voorbereiden voor verwerking</span><span class="sxs-lookup"><span data-stu-id="cade4-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="cade4-122">Bankgegevens toevoegen voor een leveranciersaccount</span><span class="sxs-lookup"><span data-stu-id="cade4-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="cade4-123">Een leveranciersbetaling invoeren</span><span class="sxs-lookup"><span data-stu-id="cade4-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="cade4-124">Een leveranciersbetaling verwerken met de standaard-ER-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="cade4-125">De elektronische betalingsmethode configureren</span><span class="sxs-lookup"><span data-stu-id="cade4-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="cade4-126">Een leveranciersbetaling verwerken</span><span class="sxs-lookup"><span data-stu-id="cade4-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="cade4-127">De standaard-ER-indeling aanpassen</span><span class="sxs-lookup"><span data-stu-id="cade4-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="cade4-128">Een aangepaste indeling maken</span><span class="sxs-lookup"><span data-stu-id="cade4-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="cade4-129">Een aangepaste indeling bewerken</span><span class="sxs-lookup"><span data-stu-id="cade4-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="cade4-130">Een aangepaste indeling markeren als uitvoerbaar</span><span class="sxs-lookup"><span data-stu-id="cade4-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="cade4-131">Een leveranciersbetaling verwerken met de aangepaste ER-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="cade4-132">De elektronische betalingsmethode configureren</span><span class="sxs-lookup"><span data-stu-id="cade4-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="cade4-133">Een leveranciersbetaling verwerken</span><span class="sxs-lookup"><span data-stu-id="cade4-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="cade4-134">Nieuwe versies van de standaardconfiguraties voor ER-indeling importeren</span><span class="sxs-lookup"><span data-stu-id="cade4-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="cade4-135">Nieuwe versies van de standaard-ER-configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="cade4-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="cade4-136">De geïmporteerde ER-indelingsconfiguraties bekijken</span><span class="sxs-lookup"><span data-stu-id="cade4-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="cade4-137">De wijzigingen in de nieuwe versie van een geïmporteerde indeling in een aangepaste indeling overnemen</span><span class="sxs-lookup"><span data-stu-id="cade4-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="cade4-138">De huidige conceptversie van een aangepaste indeling voltooien</span><span class="sxs-lookup"><span data-stu-id="cade4-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="cade4-139">Een aangepaste indeling rebasen op een nieuwe basisversie</span><span class="sxs-lookup"><span data-stu-id="cade4-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="cade4-140">Een leveranciersbetaling verwerken met de gerebasede ER-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="cade4-141">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="cade4-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="cade4-142">Het ER-raamwerk configureren</span><span class="sxs-lookup"><span data-stu-id="cade4-142">Configure the ER framework</span></span>

<span data-ttu-id="cade4-143">Als u een gebruiker bent in de rol Functioneel consultant elektronische rapportage, moet u de minimale set ER-parameters configureren voordat u het ER-framework kunt gaan gebruiken om een aangepaste versie van een standaard-ER-indeling te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="cade4-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="cade4-144">ER-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="cade4-144">Configure ER parameters</span></span>

1. <span data-ttu-id="cade4-145">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-146">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="cade4-147">Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Algemeen** de optie **Ontwerpmodus inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cade4-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="cade4-148">Stel op het tabblad **Bijlagen** de volgende parameters in:</span><span class="sxs-lookup"><span data-stu-id="cade4-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="cade4-149">Selecteer in het veld **Configuraties** het type **Bestand** voor het bedrijf **USMF**.</span><span class="sxs-lookup"><span data-stu-id="cade4-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="cade4-150">Selecteer in de velden **Taakarchief**, **Tijdelijk**, **Basislijn** en **Overige** het type **Bestand**.</span><span class="sxs-lookup"><span data-stu-id="cade4-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="cade4-151">Meer informatie over het configureren van ER-parameters vindt u in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cade4-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="cade4-152">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="cade4-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="cade4-153">Elke ER-configuratie die wordt toegevoegd, wordt gemarkeerd als het eigendom van een ER-configuratieprovider.</span><span class="sxs-lookup"><span data-stu-id="cade4-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="cade4-154">De ER-configuratieprovider die is geactiveerd in de werkruimte **Elektronische rapportage** wordt hiervoor gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cade4-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="cade4-155">Daarom moet u een ER-configuratieprovider activeren in de werkruimte **Elektronische rapportage** voordat u ER-configuraties gaat toevoegen of bewerken.</span><span class="sxs-lookup"><span data-stu-id="cade4-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="cade4-156">Alleen de eigenaar van een ER-configuratie kan deze bewerken.</span><span class="sxs-lookup"><span data-stu-id="cade4-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="cade4-157">Daarom moet een geschikte ER-configuratieprovider worden geactiveerd in de werkruimte **Elektronische rapportage**, voordat een ER-configuratie kan worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="cade4-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="cade4-158">De lijst met ER-configuratie providers bekijken</span><span class="sxs-lookup"><span data-stu-id="cade4-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="cade4-159">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-160">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="cade4-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="cade4-161">Op de tabelpagina **Configuratieproviders** heeft elke providerrecord een unieke naam en een unieke URL.</span><span class="sxs-lookup"><span data-stu-id="cade4-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="cade4-162">Bekijk de inhoud van deze pagina.</span><span class="sxs-lookup"><span data-stu-id="cade4-162">Review the contents of this page.</span></span> <span data-ttu-id="cade4-163">Als er al een record bestaat voor **Litware, Inc.** (`https://www.litware.com`), kunt u de volgende procedure, [Een nieuwe ER-configuratieprovider toevoegen](#ActivateProvider), overslaan.</span><span class="sxs-lookup"><span data-stu-id="cade4-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="cade4-164">Een nieuwe ER-configuratieprovider toevoegen</span><span class="sxs-lookup"><span data-stu-id="cade4-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="cade4-165">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-166">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="cade4-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="cade4-167">Selecteer **Nieuw** op de pagina **Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="cade4-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="cade4-168">Voer in het veld **Naam** de tekst **Litware, Inc.** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="cade4-169">Voer in het veld **Internetadres** de tekst `https://www.litware.com` in.</span><span class="sxs-lookup"><span data-stu-id="cade4-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="cade4-170">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cade4-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="cade4-171">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="cade4-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="cade4-172">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-173">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Litware, Inc.** en selecteer **Instellen als actief**.</span><span class="sxs-lookup"><span data-stu-id="cade4-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="cade4-174">Meer informatie over ER-configuratieproviders vindt u in [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="cade4-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="cade4-175">De standaardconfiguraties voor ER-indeling importeren</span><span class="sxs-lookup"><span data-stu-id="cade4-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="cade4-176">De standaard-ER-configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="cade4-176">Import the standard ER configurations</span></span>

<span data-ttu-id="cade4-177">Als u de standaard-ER-configuraties wilt toevoegen aan uw huidige exemplaar van Microsoft Dynamics 365 Finance, moet u deze importeren vanuit de ER-[opslagplaats](general-electronic-reporting.md#Repository) die voor dat exemplaar is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="cade4-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="cade4-178">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-179">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Microsoft** en selecteer vervolgens **Opslagplaatsen** om de lijst met opslagplaatsen voor de provider Microsoft weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cade4-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="cade4-180">Selecteer op de pagina **Opslagplaats van configuraties** de opslagplaats van het type **Algemeen** en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="cade4-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="cade4-181">Als u wordt gevraagd om toestemming te geven om verbinding te maken met de Regulatory Configuration Service, volgt u de instructies voor autorisatie.</span><span class="sxs-lookup"><span data-stu-id="cade4-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="cade4-182">Selecteer op de pagina **Opslagplaatsen van configuraties** in de configuratiestructuur in het linkerdeelvenster de indelingsconfiguratie **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="cade4-183">Selecteer op het sneltabblad **Versies** de versie **1.1** van de geselecteerde ER-indelingsconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="cade4-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="cade4-184">Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden naar het huidige Finance-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="cade4-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Configuratie archiefpagina](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="cade4-186">Als u problemen ondervindt met de toegang tot de [globale opslagplaats](er-download-configurations-global-repo.md), kunt u in plaats daarvan [configuraties downloaden](download-electronic-reporting-configuration-lcs.md) van Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cade4-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="cade4-187">De geïmporteerde ER-configuraties bekijken</span><span class="sxs-lookup"><span data-stu-id="cade4-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="cade4-188">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-189">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="cade4-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="cade4-190">Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit.</span><span class="sxs-lookup"><span data-stu-id="cade4-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="cade4-191">Naast de geselecteerde ER-indeling **BACS (UK)** zijn ook er nog andere vereiste-configuraties geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="cade4-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="cade4-192">Controleer of de volgende ER-configuraties beschikbaar zijn in de configuratiestructuur:</span><span class="sxs-lookup"><span data-stu-id="cade4-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="cade4-193">**Betalingsmodel**: Deze configuratie bevat het ER-onderdeel [Gegevensmodel](general-electronic-reporting.md#data-model-and-model-mapping-components) dat de gegevensstructuur van het zakelijke betalingsdomein vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="cade4-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="cade4-194">**Toewijzing voor betalingsmodel 1611**: Deze configuratie bevat het ER-onderdeel [Modeltoewijzing](general-electronic-reporting.md#data-model-and-model-mapping-components) dat aangeeft hoe het gegevensmodel tijdens runtime wordt ingevuld met toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="cade4-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="cade4-195">**BACS (UK)**: Deze configuratie bevat de ER-onderdelen [Indeling](general-electronic-reporting.md#FormatComponentOutbound) en Indelingstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="cade4-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="cade4-196">Het onderdeel Indeling specificeert de rapportindeling.</span><span class="sxs-lookup"><span data-stu-id="cade4-196">The format component specifies the report layout.</span></span> <span data-ttu-id="cade4-197">Het onderdeel indelingstoewijzing bevat de modelgegevensbron en geeft aan hoe de rapportindeling wordt ingevuld door deze gegevensbron te gebruiken tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="cade4-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Pagina Configuraties](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="cade4-199">Een leveranciersbetaling voorbereiden voor verwerking</span><span class="sxs-lookup"><span data-stu-id="cade4-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="cade4-200">Bankgegevens toevoegen voor een leveranciersaccount</span><span class="sxs-lookup"><span data-stu-id="cade4-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="cade4-201">U moet bankgegevens toevoegen voor een leveranciersaccount waarnaar later wordt verwezen in een geregistreerde betaling.</span><span class="sxs-lookup"><span data-stu-id="cade4-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="cade4-202">Ga naar **Leveranciers** \> **Leveranciers** \> **Alle leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="cade4-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="cade4-203">Selecteer op de pagina **Alle leveranciers** de leveranciersaccount **GB_SI_000001** en selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Instellen** de optie **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="cade4-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="cade4-204">Selecteer op de pagina **Bankrekeningen van leveranciers** de optie **Nieuw** en voer de volgende gegevens in:</span><span class="sxs-lookup"><span data-stu-id="cade4-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="cade4-205">Voer in het veld **Bankrekening** de waarde **GBP OPER** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="cade4-206">Selecteer in het veld **Bankgroepen** de waarde **BankGBP**.</span><span class="sxs-lookup"><span data-stu-id="cade4-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="cade4-207">Voer in het veld **Bankrekeningnummer** de waarde **202015** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="cade4-208">Voer in het veld **SWIFT-code** de waarde <a id="DefineSWIFTCode"></a>**CHASDEFXXXX** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="cade4-209">Voer in het veld **IBAN** de waarde **GB33BUKB20201555555555** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="cade4-210">U kunt in het veld **Routenummer** de standaardwaarde <a id="DefineRoutingNumber"></a>**123456** aanhouden.</span><span class="sxs-lookup"><span data-stu-id="cade4-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Pagina Bankrekeningen van leverancier](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="cade4-212">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cade4-212">Select **Save**.</span></span>
5. <span data-ttu-id="cade4-213">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cade4-213">Close the page.</span></span>
6. <span data-ttu-id="cade4-214">Open op de pagina **Alle leveranciers** de leveranciersrekening **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="cade4-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="cade4-215">Selecteer op de pagina met leveranciersgegevens de optie **Bewerken** om de pagina zo nodig bewerkbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="cade4-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="cade4-216">Ga naar het sneltabblad **Betaling** en selecteer in het veld **Bankrekening** de waarde **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="cade4-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Pagina Details leverancier](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="cade4-218">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cade4-218">Select **Save**.</span></span>
10. <span data-ttu-id="cade4-219">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cade4-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="cade4-220">Een leveranciersbetaling invoeren</span><span class="sxs-lookup"><span data-stu-id="cade4-220">Enter a vendor payment</span></span>

<span data-ttu-id="cade4-221">U moet een nieuwe leveranciersbetaling invoeren door middel van een [betalingsvoorstel](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span><span class="sxs-lookup"><span data-stu-id="cade4-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="cade4-222">Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="cade4-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="cade4-223">Selecteer **Nieuw** op de pagina **Journaal met betalingen van leverancier**.</span><span class="sxs-lookup"><span data-stu-id="cade4-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="cade4-224">Selecteer in het veld **Naam** de waarde **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="cade4-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="cade4-225">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="cade4-225">Select **Lines**.</span></span>
5. <span data-ttu-id="cade4-226">Selecteer **Betalingsvoorstel** \> **Betalingsvoorstel maken**.</span><span class="sxs-lookup"><span data-stu-id="cade4-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="cade4-227">Configureer in het dialoogvenster **Betalingsvoorstel voor leverancier** alleen voorwaarden voor het filteren van records met de leveranciersrekening **GB_SI_000001** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="cade4-228">Selecteer de regel voor de factuur **00000007_Inv** en selecteer vervolgens **Betaling maken**.</span><span class="sxs-lookup"><span data-stu-id="cade4-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Dialoogvenster Betalingsvoorstel voor leverancier](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="cade4-230">Controleer of de ingevoerde betaling is geconfigureerd voor gebruik van de betalingsmethode **Elektronisch**.</span><span class="sxs-lookup"><span data-stu-id="cade4-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Pagina Leveranciersbetalingen](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="cade4-232">Een leveranciersbetaling verwerken met de standaard-ER-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="cade4-233">De elektronische betalingsmethode configureren</span><span class="sxs-lookup"><span data-stu-id="cade4-233">Set up the electronic payment method</span></span>

<span data-ttu-id="cade4-234">U moet de betalingsmethode Elektronisch configureren, zodat deze de geïmporteerde ER-indelingsconfiguratie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cade4-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="cade4-235">Ga naar **Leveranciers** \> **Betalingsinstelling** \> **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="cade4-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="cade4-236">Selecteer op de pagina **Betalingsmethoden - leveranciers** de betalingsmethode **Elektronisch** in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="cade4-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="cade4-237">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="cade4-237">Select **Edit**.</span></span>
4. <span data-ttu-id="cade4-238">Stel op het sneltabblad **Bestandsindelingen** de optie **Algemene elektronische exportindeling** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cade4-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="cade4-239">Selecteer in het veld **Indelingsconfiguratie exporteren** de ER-indelingsconfiguratie **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Pagina Betalingsmethoden - leveranciers](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="cade4-241">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cade4-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="cade4-242">Een leveranciersbetaling verwerken</span><span class="sxs-lookup"><span data-stu-id="cade4-242">Process a vendor payment</span></span>

1. <span data-ttu-id="cade4-243">Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="cade4-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="cade4-244">Selecteer op de pagina **Betalingsjournaal van leverancier** het betalingsjournaal dat u eerder hebt toegevoegd en selecteer vervolgens **Regels**.</span><span class="sxs-lookup"><span data-stu-id="cade4-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="cade4-245">Selecteer op de pagina **Leveranciersbetalingen** de waarde **Betalingen genereren**.</span><span class="sxs-lookup"><span data-stu-id="cade4-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="cade4-246">Voer in het dialoogvenster **Betalingen genereren** de volgende informatie in:</span><span class="sxs-lookup"><span data-stu-id="cade4-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="cade4-247">Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.</span><span class="sxs-lookup"><span data-stu-id="cade4-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="cade4-248">Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="cade4-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="cade4-249">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-249">Select **OK**.</span></span>
6. <span data-ttu-id="cade4-250">Stel in het dialoogvenster **Parameters elektronische rapport** de optie **Controlerapport afdrukken** in op **Ja** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Pagina Parameters elektronisch rapport](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="cade4-252">Naast het betalingsbestand kunt u nu ook het controlerapport genereren.</span><span class="sxs-lookup"><span data-stu-id="cade4-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="cade4-253">Download het zip-bestand en pak de volgende bestanden uit:</span><span class="sxs-lookup"><span data-stu-id="cade4-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="cade4-254">Het controlerapport in Excel-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-254">The control report in Excel format</span></span>
    - <span data-ttu-id="cade4-255">Het betalingsbestand in txt-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-255">The payment file in TXT format</span></span>

        <span data-ttu-id="cade4-256">Merk op dat conform de [structuur](#PositionRoutingNumber) van de opgegeven ER-indeling de betalingsregel in het gegenereerde bestand begint met het routenummer dat was [gedefinieerd](#DefineRoutingNumber) voor de geconfigureerde bankrekening.</span><span class="sxs-lookup"><span data-stu-id="cade4-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Betalingsbestand in txt-indeling](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="cade4-258">De standaard-ER-indeling aanpassen</span><span class="sxs-lookup"><span data-stu-id="cade4-258">Customize the standard ER format</span></span>

<span data-ttu-id="cade4-259">Voor het voorbeeld dat in deze sectie wordt getoond, wilt u de ER-configuraties gebruiken die door Microsoft worden geleverd om betalingsbestanden voor leveranciers te genereren in de BACS-indeling. Maar u moet een aanpassing toevoegen om de behoeften van een bepaalde bank te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="cade4-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="cade4-260">U wilt ook uw aangepaste indeling kunnen upgraden wanneer er nieuwe versies van de ER-configuraties beschikbaar komen.</span><span class="sxs-lookup"><span data-stu-id="cade4-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="cade4-261">U wilt de upgrade echter wel uitvoeren tegen de laagste kosten.</span><span class="sxs-lookup"><span data-stu-id="cade4-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="cade4-262">In dit geval moet u als vertegenwoordiger van Litware, Inc. een nieuwe ER-indelingsconfiguratie maken (afleiden) met de door Microsoft geleverde configuratie **BACS (UK)** als basis.</span><span class="sxs-lookup"><span data-stu-id="cade4-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="cade4-263">Een aangepaste indeling maken</span><span class="sxs-lookup"><span data-stu-id="cade4-263">Create a custom format</span></span>

1. <span data-ttu-id="cade4-264">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="cade4-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="cade4-265">Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="cade4-266">Litware, Inc. gebruikt versie 1.1 van deze ER-indelingsconfiguratie als basis voor de aangepaste versie.</span><span class="sxs-lookup"><span data-stu-id="cade4-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="cade4-267">Klik op **Configuratie maken** om het dialoogvenster met de vervolgkeuzelijst te openen.</span><span class="sxs-lookup"><span data-stu-id="cade4-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="cade4-268">Met behulp van dit dialoogvenster kunt u een nieuwe configuratie voor een aangepaste betalingsindeling maken.</span><span class="sxs-lookup"><span data-stu-id="cade4-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="cade4-269">Selecteer in de veldgroep **Nieuw** de optie **Afleiden van naam: BACS (VK), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="cade4-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="cade4-270">Voer in het veld **Naam** de waarde **BACS (UK, aangepast)** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Het vervolgkeuzemenu Configuratie maken](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="cade4-272">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="cade4-272">Select **Create configuration**.</span></span>

<span data-ttu-id="cade4-273">Versie 1.1.1 van de ER-indelingsconfiguratie **BACS (UK, aangepast)** wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cade4-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="cade4-274">Deze versie heeft de [status](general-electronic-reporting.md#component-versioning) **Concept** en kan worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="cade4-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="cade4-275">De huidige inhoud van uw aangepaste ER-indeling komt overeen met de inhoud van de indeling die wordt geleverd door Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cade4-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Pagina Configuraties](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="cade4-277">Een aangepaste indeling bewerken</span><span class="sxs-lookup"><span data-stu-id="cade4-277">Edit a custom format</span></span>

<span data-ttu-id="cade4-278">U moet de aangepaste indeling zo configureren dat deze voldoet aan de vereisten die uw bank stelt.</span><span class="sxs-lookup"><span data-stu-id="cade4-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="cade4-279">Een bank kan bijvoorbeeld vereisen dat betalingsbestanden die zijn gegenereerd, de SWIFT-code (Society for Worldwide Interbank Financial Telecommunication) bevatten van een bank waaraan de rol van agent is toegewezen in de verwerkte leverancierbetaling.</span><span class="sxs-lookup"><span data-stu-id="cade4-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="cade4-280">SWIFT-codes zijn internationale bankcodes waarmee wereldwijd specifieke banken worden geïdentificeerd.</span><span class="sxs-lookup"><span data-stu-id="cade4-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="cade4-281">Deze worden ook wel BIC's (Bank Identifier Codes) genoemd.</span><span class="sxs-lookup"><span data-stu-id="cade4-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="cade4-282">De SWIFT-code moet 11 tekens lang zijn en moet aan het begin van elke betalingsregel in een gegenereerd betalingsbestand staan.</span><span class="sxs-lookup"><span data-stu-id="cade4-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="cade4-283">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="cade4-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="cade4-284">Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **BACS (UK, aangepast)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="cade4-285">Selecteer op het sneltabblad **Versies** de versie **1.1.1** van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="cade4-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="cade4-286">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="cade4-286">Select **Designer**.</span></span>
5. <span data-ttu-id="cade4-287">Selecteer op de pagina **Indelingsontwerper** de optie **Details weergeven** om meer informatie over de indelingselementen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cade4-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="cade4-288">Vouw de volgende elementen uit en bekijk ze:</span><span class="sxs-lookup"><span data-stu-id="cade4-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="cade4-289">Het element **BACSReportsFolder** van het type **Map**.</span><span class="sxs-lookup"><span data-stu-id="cade4-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="cade4-290">Dit element wordt gebruikt om uitvoer in zip-indeling te genereren.</span><span class="sxs-lookup"><span data-stu-id="cade4-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="cade4-291">Het element **bestand** van het type **Bestand**.</span><span class="sxs-lookup"><span data-stu-id="cade4-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="cade4-292">Dit element wordt gebruikt om een betalingsbestand in txt-indeling te genereren.</span><span class="sxs-lookup"><span data-stu-id="cade4-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="cade4-293">Het element **transactions** van het type **Reeks**.</span><span class="sxs-lookup"><span data-stu-id="cade4-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="cade4-294">Dit element wordt gebruikt om een enkele betalingsregel in een betalingsbestand te genereren.</span><span class="sxs-lookup"><span data-stu-id="cade4-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="cade4-295">Het element **transaction** van het type **Reeks**.</span><span class="sxs-lookup"><span data-stu-id="cade4-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="cade4-296">Dit element wordt gebruikt om individuele velden van een enkele betalingsregel te genereren.</span><span class="sxs-lookup"><span data-stu-id="cade4-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="cade4-297">Selecteer het element **transaction**.</span><span class="sxs-lookup"><span data-stu-id="cade4-297">Select the **transaction** element.</span></span>

    ![Het element transaction in de ER Operations-ontwerper](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="cade4-299">Het opgegeven rapport wordt zo geconfigureerd dat <a id="PositionRoutingNumber"></a>elke betalingsregel begint met het routenummer van de bank.</span><span class="sxs-lookup"><span data-stu-id="cade4-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="cade4-300">Hiervoor wordt het indelingselement **vendBankRouteNum** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cade4-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="cade4-301">Selecteer **Toevoegen** en selecteer vervolgens het type **Tekst\\tekenreeks** van het indelingselement dat u wilt toevoegen:</span><span class="sxs-lookup"><span data-stu-id="cade4-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="cade4-302">Voer in het veld **Naam** de tekst **vendBankSWIFT** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="cade4-303">Voer in het veld **Minimumlengte** **11** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="cade4-304">Voer in het veld **Maximumlengte** **11** in.</span><span class="sxs-lookup"><span data-stu-id="cade4-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="cade4-305">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cade4-306">Het element **vendBankSWIFT** wordt gebruikt om de SWIFT-code van de bank van een leverancier in gegenereerde bestanden in te voeren.</span><span class="sxs-lookup"><span data-stu-id="cade4-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="cade4-307">Selecteer in de boomstructuur met indelingsstructuren de waarde **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="cade4-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="cade4-308">Selecteer **Omhoog** om het geselecteerde opmaakelement één niveau omhoog te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="cade4-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="cade4-309">Herhaal deze stap totdat het element **vendBankSWIFT** het <a id="PositionSWIFTCode"></a>eerste element onder het bovenliggende element **transaction** is.</span><span class="sxs-lookup"><span data-stu-id="cade4-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT als eerste element onder transaction in de ER Operations-ontwerper](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="cade4-311">Terwijl het element **vendBankSWIFT** nog steeds is geselecteerd in de structuur met de indelingsstructuur, selecteert u het tabblad **Toewijzing** en vouwt u vervolgens de gegevensbron **model** uit.</span><span class="sxs-lookup"><span data-stu-id="cade4-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="cade4-312">Vouw **model.Payment** \> **model.Payment.CreditorAgent** uit en selecteert het gegevensbronveld **model.Payment.CreditorAgent.BICFI**.</span><span class="sxs-lookup"><span data-stu-id="cade4-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="cade4-313">Met dit veld van de gegevensbron wordt de SWIFT-code beschikbaar gemaakt van een leveranciersbank waaraan de rol van de agent in de verwerkte leverancierbetaling is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="cade4-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="cade4-314">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="cade4-314">Select **Bind**.</span></span> <span data-ttu-id="cade4-315">Het indelingselement **vendBankSWIFT** is nu gekoppeld aan het gegevensbronveld **model.Payment.CreditorAgent.BICFI**, zodat SWIFT-codes worden ingevoerd in gegenereerde betalingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="cade4-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![Indelingselement vendBankSWIFT dat is gekoppeld aan het gegevensbronveld model.Payment.CreditorAgent.BICFI in de ER Operations-ontwerper](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="cade4-317">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cade4-317">Select **Save**.</span></span>
15. <span data-ttu-id="cade4-318">Sluit de pagina met de ontwerper.</span><span class="sxs-lookup"><span data-stu-id="cade4-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="cade4-319">Een aangepaste indeling markeren als uitvoerbaar</span><span class="sxs-lookup"><span data-stu-id="cade4-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="cade4-320">Nu de eerste versie van uw aangepaste indeling is gemaakt en de status **Concept** heeft , kunt u deze versie uitvoeren om hem te testen.</span><span class="sxs-lookup"><span data-stu-id="cade4-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="cade4-321">Om het rapport uit te voeren, moet u een leveranciersbetaling verwerken met behulp van de betalingsmethode die verwijst naar door u aangepaste ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="cade4-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="cade4-322">Wanneer u een ER-indeling aanroept vanuit de toepassing, worden standaard alleen de versies met de status **Voltooid** en **Gedeeld** [meegenomen](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="cade4-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="cade4-323">Dit gedrag voorkomt dat ER-indelingsprofielen met niet-voltooide ontwerpen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cade4-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="cade4-324">Voor het testen kunt u de toepassing dwingen de versie van de ER-indeling te gebruiken met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="cade4-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="cade4-325">Op deze manier kunt u de versie van de huidige indelingsversie aanpassen als er wijzigingen nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="cade4-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="cade4-326">Meer informatie over dit onderwerp vindt u in [Toepasbaarheid](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="cade4-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="cade4-327">Als u de conceptversie van een ER-indeling wilt gebruiken, moet u de ER-indeling expliciet markeren.</span><span class="sxs-lookup"><span data-stu-id="cade4-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="cade4-328">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="cade4-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="cade4-329">Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="cade4-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="cade4-330">Stel in het dialoogvenster **Gebruikersparameters** de optie **Uitvoeringsinstellingen** in op **Ja** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="cade4-331">Selecteer zo nodig **Bewerken** om de huidige pagina bewerkbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="cade4-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="cade4-332">Selecteer in de configuratiestructuur in het linkerdeel venster de waarde **BACS (UK, aangepast)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="cade4-333">Stel de optie **Concept uitvoeren** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cade4-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![De optie Concept uitvoeren op de pagina Configuraties](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="cade4-335">Een leveranciersbetaling verwerken met de aangepaste ER-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="cade4-336">De elektronische betalingsmethode configureren</span><span class="sxs-lookup"><span data-stu-id="cade4-336">Set up the electronic payment method</span></span>

<span data-ttu-id="cade4-337">U moet de elektronische betalingsmethode configureren, zodat de aangepaste ER-indeling wordt gebruikt voor de verwerking van leveranciersbetalingen.</span><span class="sxs-lookup"><span data-stu-id="cade4-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="cade4-338">Ga naar **Leveranciers** \> **Betalingsinstelling** \> **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="cade4-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="cade4-339">Selecteer op de pagina **Betalingsmethoden - leveranciers** de betalingsmethode **Elektronisch** in het linkerdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="cade4-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="cade4-340">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="cade4-340">Select **Edit**.</span></span>
4. <span data-ttu-id="cade4-341">Stel op het sneltabblad **Bestandsindelingen** de optie **Algemene elektronische exportindeling** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cade4-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="cade4-342">Selecteer in het veld **Indelingsconfiguratie exporteren** de ER-indelingsconfiguratie **BACS (UK, aangepast)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Pagina Betalingsmethoden - leveranciers](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="cade4-344">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cade4-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="cade4-345">Een leveranciersbetaling verwerken</span><span class="sxs-lookup"><span data-stu-id="cade4-345">Process a vendor payment</span></span>

1. <span data-ttu-id="cade4-346">Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="cade4-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="cade4-347">Selecteer op de pagina **Betalingsjournaal van leverancier** het betalingsjournaal dat u eerder hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="cade4-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="cade4-348">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="cade4-348">Select **Lines**.</span></span>
4. <span data-ttu-id="cade4-349">Selecteer op de pagina **Leveranciersbetalingen** boven het raster **Betalingsstatus** \> **Geen**.</span><span class="sxs-lookup"><span data-stu-id="cade4-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="cade4-350">Selecteer **Betaling genereren**.</span><span class="sxs-lookup"><span data-stu-id="cade4-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="cade4-351">Voer in het dialoogvenster **Betalingen genereren** de volgende informatie in:</span><span class="sxs-lookup"><span data-stu-id="cade4-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="cade4-352">Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.</span><span class="sxs-lookup"><span data-stu-id="cade4-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="cade4-353">Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="cade4-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="cade4-354">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-354">Select **OK**.</span></span>
8. <span data-ttu-id="cade4-355">Stel in het dialoogvenster **Parameters elektronische rapport** de optie **Controlerapport afdrukken** in op **Ja** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cade4-356">Naast het betalingsbestand kunt u nu alleen het controlerapport genereren.</span><span class="sxs-lookup"><span data-stu-id="cade4-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="cade4-357">Download het zip-bestand en pak de volgende bestanden uit:</span><span class="sxs-lookup"><span data-stu-id="cade4-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="cade4-358">Het controlerapport in Excel-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-358">The control report in Excel format</span></span>
    - <span data-ttu-id="cade4-359">Het betalingsbestand in txt-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-359">The payment file in TXT format</span></span>

        <span data-ttu-id="cade4-360">Merk op dat, conform de structuur van uw aangepaste ER-indeling, de betalingsregel in het gegenereerde bestand nu [begint](#PositionSWIFTCode) met de SWIFT-code die is [ingevoerd](#DefineSWIFTCode) voor de bankrekening van de leverancier voor wie de betaling is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="cade4-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Betalingsbestand in txt-indeling](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="cade4-362">Nieuwe versies van de standaardconfiguraties voor ER-indeling importeren</span><span class="sxs-lookup"><span data-stu-id="cade4-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="cade4-363">Voor het voorbeeld dat in deze sectie wordt weergegeven, ontvangt u een melding over Knowledge Base-artikel [KB 3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="cade4-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="cade4-364">In dit bericht wordt u gewaarschuwd over de nieuwe versie van de ER-indeling **BACS (UK)** die door Microsoft is gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="cade4-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="cade4-365">Behalve het controlerapport kunnen gebruikers met deze nieuwe versie het betalingsadviesrapport en het bijbehorende notarapport genereren tijdens het verwerken van een leveranciersbetaling.</span><span class="sxs-lookup"><span data-stu-id="cade4-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="cade4-366">U wilt deze functionaliteit gaan gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cade4-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="cade4-367">Nieuwe versies van de standaard-ER-configuraties importeren</span><span class="sxs-lookup"><span data-stu-id="cade4-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="cade4-368">Als u de nieuwe versies van de ER-configuraties wilt toevoegen aan het huidige Finance-exemplaar, moet u deze importeren vanuit de ER-[opslagplaats](general-electronic-reporting.md#Repository) die u voor dat exemplaar hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="cade4-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="cade4-369">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-370">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Microsoft** en selecteer vervolgens **Opslagplaatsen** om de lijst met opslagplaatsen voor de provider Microsoft weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cade4-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="cade4-371">Selecteer op de pagina **Opslagplaats van configuraties** de opslagplaats van het type **Algemeen** en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="cade4-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="cade4-372">Als u wordt gevraagd om toestemming te geven om verbinding te maken met de Regulatory Configuration Service, volgt u de instructies voor autorisatie.</span><span class="sxs-lookup"><span data-stu-id="cade4-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="cade4-373">Selecteer op de pagina **Opslagplaatsen van configuraties** in de configuratiestructuur in het linkerdeelvenster de indelingsconfiguratie **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="cade4-374">Selecteer op het sneltabblad **Versies** de versie **3.3** van de geselecteerde ER-indelingsconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="cade4-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="cade4-375">Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden naar het huidige Finance-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="cade4-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Configuratie archiefpagina](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="cade4-377">Als u problemen ondervindt met de toegang tot de [globale opslagplaats](er-download-configurations-global-repo.md), kunt u in plaats daarvan [configuraties downloaden](download-electronic-reporting-configuration-lcs.md) van Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cade4-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="cade4-378">De geïmporteerde ER-indelingsconfiguraties bekijken</span><span class="sxs-lookup"><span data-stu-id="cade4-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="cade4-379">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-380">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="cade4-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="cade4-381">Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="cade4-382">Selecteer op het sneltabblad **Versies** de versie **3.3**.</span><span class="sxs-lookup"><span data-stu-id="cade4-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="cade4-383">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="cade4-383">Select **Designer**.</span></span>
6. <span data-ttu-id="cade4-384">Vouw op de **pagina Indelingsontwerper** het indelingselement **BACSReportsFolder** uit.</span><span class="sxs-lookup"><span data-stu-id="cade4-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="cade4-385">Merk op dat versie 3.3 het indelingselement **PaymentAdviceReport** bevat, dat wordt gebruikt om een betalingsadviesrapport te genereren wanneer een leveranciersbetaling wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="cade4-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![Het indelingselement PaymentAdviceReport in de ER Operations-ontwerper](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="cade4-387">Sluit de pagina met de ontwerper.</span><span class="sxs-lookup"><span data-stu-id="cade4-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="cade4-388">De wijzigingen in de nieuwe versie van een geïmporteerde indeling in een aangepaste indeling overnemen</span><span class="sxs-lookup"><span data-stu-id="cade4-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="cade4-389">De huidige conceptversie van een aangepaste indeling voltooien</span><span class="sxs-lookup"><span data-stu-id="cade4-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="cade4-390">Als u de huidige status van de aangepaste indeling wilt behouden, voltooit u de conceptversie 1.1.1 door de status te wijzigen van **Concept** in **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="cade4-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="cade4-391">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="cade4-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cade4-392">Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="cade4-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="cade4-393">Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit. Vouw hieronder **BACS (UK)** uit en selecteer **BACS (UK, aangepast)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="cade4-394">Selecteer op het sneltabblad **Versies** de optie **Status wijzigen** \> **Voltooien** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="cade4-395">De status van versie 1.1.1 wordt gewijzigd van **Concept** in **Voltooid** en de versie wordt alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="cade4-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="cade4-396">Er is een nieuwe bewerkbare versie 1.1.2 toegevoegd, met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="cade4-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="cade4-397">U kunt deze versie gebruiken om verdere wijzigingen aan te brengen in de aangepaste ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="cade4-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="cade4-398">Een aangepaste indeling rebasen op een nieuwe basisversie</span><span class="sxs-lookup"><span data-stu-id="cade4-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="cade4-399">Als u de nieuwe functionaliteit van versie 3.3 van de indeling **BACS (UK)** wilt gebruiken in uw aanpassingen, moet u de basisconfiguratieversie wijzigen voor de aangepaste configuratie, **BACS (UK, aangepast)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="cade4-400">Dit proces wordt [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) genoemd.</span><span class="sxs-lookup"><span data-stu-id="cade4-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="cade4-401">Gebruik in plaats van versie 1.1 van **BACS (UK)** de nieuwe versie 3.3.</span><span class="sxs-lookup"><span data-stu-id="cade4-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="cade4-402">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="cade4-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="cade4-403">Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **BACS (UK, aangepast)**.</span><span class="sxs-lookup"><span data-stu-id="cade4-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="cade4-404">Selecteer op het sneltabblad **Versies** versie **1.1.2** en selecteer vervolgens **Rebase**.</span><span class="sxs-lookup"><span data-stu-id="cade4-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="cade4-405">Selecteer in het dialoogvenster **Rebase** in het veld **Doelversie** de versie **3.3** van de basisconfiguratie om deze toe te passen als de nieuwe basis en gebruik deze om de configuratie bij te werken.</span><span class="sxs-lookup"><span data-stu-id="cade4-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Het dialoogvenster Rebase](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="cade4-407">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-407">Select **OK**.</span></span>
6. <span data-ttu-id="cade4-408">U ziet dat het nummer van de conceptversie is gewijzigd van **1.1.2** in **3.3.2**, wat de wijziging van de basisversie weergeeft.</span><span class="sxs-lookup"><span data-stu-id="cade4-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="cade4-409">Wanneer de aangepaste versie en een nieuwe basisversie worden samengevoegd, kunnen conflicten worden gedetecteerd vanwege indelingswijzigingen die niet automatisch kunnen worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="cade4-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Gerebasede configuratie met conflicten op de pagina Configuraties](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="cade4-411">Als conflicten worden gedetecteerd, moeten deze handmatig worden opgelost in de indelingsontwerper.</span><span class="sxs-lookup"><span data-stu-id="cade4-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="cade4-412">Selecteer op het sneltabblad **Versies** de versie **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="cade4-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="cade4-413">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="cade4-413">Select **Designer**.</span></span>
9. <span data-ttu-id="cade4-414">Selecteer op de pagina **Indelingsontwerper** op het sneltabblad **Details** een rebase-conflictrecord en selecteer vervolgens **Basiswaarde toepassen**.</span><span class="sxs-lookup"><span data-stu-id="cade4-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Een rebase-conflictrecord in de ER Operations-ontwerper](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="cade4-416">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cade4-416">Select **Save**.</span></span>

    <span data-ttu-id="cade4-417">De rebase-conflictrecord moet nu niet meer zichtbaar zijn op het sneltabblad **Details**.</span><span class="sxs-lookup"><span data-stu-id="cade4-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Conflict opgelost in de ER Operations-ontwerper](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="cade4-419">U hebt het conflict opgelost door te bevestigen dat versie 3 van het basis model moet worden gebruikt in deze ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="cade4-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="cade4-420">Navigeer naar **BACSReportsFolder** \> **bestand** \> **transacties** \> **transactie**.</span><span class="sxs-lookup"><span data-stu-id="cade4-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="cade4-421">Op het tabblad **Toewijzing** ziet u dat versie 3.3.2 van de aangepaste ER-indeling zowel uw aanpassing bevat (het indelingselement **vendBankSWIFT** en de binding ervan) als ook de nieuwe functionaliteit van versie 3.3 van de basis-ER-indeling, die door Microsoft is geleverd (het indelingselement **PaymentAdviceReport Format** samen met de geneste elementen en geconfigureerde bindingen).</span><span class="sxs-lookup"><span data-stu-id="cade4-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="cade4-422">Met slechts enkele muisklikken hebt u de wijzigingen van een nieuwe basisversie toegepast door deze samen te voegen met uw aanpassingen.</span><span class="sxs-lookup"><span data-stu-id="cade4-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Samengevoegde indeling in de ER Operations-ontwerper](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="cade4-424">Sluit de pagina met de ontwerper.</span><span class="sxs-lookup"><span data-stu-id="cade4-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="cade4-425">De rebase-actie kan ongedaan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="cade4-425">The rebase action is reversible.</span></span> <span data-ttu-id="cade4-426">Als u deze rebase wilt annuleren, selecteert u versie **1.1.1** van de indeling **BACS (UK, aangepast)** op het sneltabblad **Versies** en selecteert u **Deze versie ophalen**.</span><span class="sxs-lookup"><span data-stu-id="cade4-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="cade4-427">Versie 3.3.2 krijgt dan weer het nummer 1.1.2 en de inhoud van conceptversie 1.1.2 komt weer overeen met de inhoud van versie 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="cade4-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="cade4-428">Een leveranciersbetaling verwerken met de gerebasede ER-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="cade4-429">Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.</span><span class="sxs-lookup"><span data-stu-id="cade4-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="cade4-430">Selecteer op de pagina **Betalingsjournaal van leverancier** het betalingsjournaal dat u eerder hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="cade4-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="cade4-431">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="cade4-431">Select **Lines**.</span></span>
4. <span data-ttu-id="cade4-432">Selecteer op de pagina **Leveranciersbetalingen** boven het raster **Betalingsstatus** \> **Geen**.</span><span class="sxs-lookup"><span data-stu-id="cade4-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="cade4-433">Selecteer **Betaling genereren**.</span><span class="sxs-lookup"><span data-stu-id="cade4-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="cade4-434">Voer in het dialoogvenster **Betalingen genereren** de volgende informatie in:</span><span class="sxs-lookup"><span data-stu-id="cade4-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="cade4-435">Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.</span><span class="sxs-lookup"><span data-stu-id="cade4-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="cade4-436">Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="cade4-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="cade4-437">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-437">Select **OK**.</span></span>
8. <span data-ttu-id="cade4-438">Voer in het dialoogvenster **Parameters elektronisch rapport** de volgende informatie in:</span><span class="sxs-lookup"><span data-stu-id="cade4-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="cade4-439">Zet de optie **Controlerapport afdrukken** op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cade4-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="cade4-440">Zet de optie **Betalingsadvies afdrukken** op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cade4-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Dialoogvenster Parameters elektronisch rapport](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="cade4-442">Naast het betalingsbestand kunt u nu zowel het controlerapport als het betalingsadviesrapport genereren.</span><span class="sxs-lookup"><span data-stu-id="cade4-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="cade4-443">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="cade4-443">Select **OK**.</span></span>
10. <span data-ttu-id="cade4-444">Download het zip-bestand en pak de volgende bestanden uit:</span><span class="sxs-lookup"><span data-stu-id="cade4-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="cade4-445">Het controlerapport in Excel-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-445">The control report in Excel format</span></span>
    - <span data-ttu-id="cade4-446">Het betalingsadvies in Excel-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-446">The payment advice report in Excel format</span></span>

        ![Betalingsadviesrapport in Excel-indeling](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="cade4-448">Het betalingsbestand in txt-indeling</span><span class="sxs-lookup"><span data-stu-id="cade4-448">The payment file in TXT format</span></span>

        <span data-ttu-id="cade4-449">Merk op dat, conform de structuur van uw aangepaste ER-indeling, de betalingsregel in het gegenereerde bestand nu begint met de SWIFT-code die is ingevoerd voor de bankrekening van een leverancier voor wie de betaling is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="cade4-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Betalingsbestand in txt-indeling](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="cade4-451">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="cade4-451">Additional resources</span></span>

- [<span data-ttu-id="cade4-452">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="cade4-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cade4-453">ER-configuraties downloaden uit Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="cade4-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="cade4-454">ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice</span><span class="sxs-lookup"><span data-stu-id="cade4-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]