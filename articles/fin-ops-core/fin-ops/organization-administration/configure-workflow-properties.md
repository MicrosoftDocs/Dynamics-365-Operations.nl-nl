---
title: Workfloweigenschappen configureren
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een workflow configureert.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40118f329a676ffb30870eb882d127e3eb258599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566962"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="12af6-103">Workfloweigenschappen configureren</span><span class="sxs-lookup"><span data-stu-id="12af6-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12af6-104">In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een workflow configureert.</span><span class="sxs-lookup"><span data-stu-id="12af6-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="12af6-105">Open de workflow in de workfloweditor om de eigenschappen van een specifiek workflowelement te configureren.</span><span class="sxs-lookup"><span data-stu-id="12af6-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="12af6-106">Klik op het tekenpapier van de workfloweditor en klik op **Eigenschappen** om de pagina **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="12af6-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="12af6-107">Met behulp van de volgende procedures kunt u de verschillende eigenschappen van de workflow configureren.</span><span class="sxs-lookup"><span data-stu-id="12af6-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="12af6-108">Naam voor de workflow opgeven</span><span class="sxs-lookup"><span data-stu-id="12af6-108">Name the workflow</span></span>

<span data-ttu-id="12af6-109">Voer deze stappen uit om een naam op te geven voor de workflow.</span><span class="sxs-lookup"><span data-stu-id="12af6-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="12af6-110">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="12af6-111">Geef in het veld **Naam** een unieke naam voor de workflow op.</span><span class="sxs-lookup"><span data-stu-id="12af6-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="12af6-112">Als u bijvoorbeeld een workflow voor opdrachten tot inkoop maakt voor elk land of elke regio waarin uw bedrijf actief is, kunt u als naam voor de workflow **Inkoopbestelopdrachten Denemarken** of **Inkoopbestelopdrachten Spanje** opgeven.</span><span class="sxs-lookup"><span data-stu-id="12af6-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="12af6-113">Eigenaar van de workflow opgeven</span><span class="sxs-lookup"><span data-stu-id="12af6-113">Specify the workflow owner</span></span>

<span data-ttu-id="12af6-114">De eigenaar van de workflow is degene die deze workflow beheert en onderhoudt.</span><span class="sxs-lookup"><span data-stu-id="12af6-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="12af6-115">Voer de volgende stappen uit om de eigenaar van de workflow op te geven.</span><span class="sxs-lookup"><span data-stu-id="12af6-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="12af6-116">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="12af6-117">Selecteer in de lijst **Eigenaar** de naam van degene die de workflow beheert.</span><span class="sxs-lookup"><span data-stu-id="12af6-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="12af6-118">Een e-mailsjabloon selecteren</span><span class="sxs-lookup"><span data-stu-id="12af6-118">Select an email template</span></span>

<span data-ttu-id="12af6-119">Volg deze stappen om de e-mailsjabloon te selecteren die wordt gebruikt om meldingen te genereren voor deze workflow.</span><span class="sxs-lookup"><span data-stu-id="12af6-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="12af6-120">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="12af6-121">Selecteer in de lijst **E-mailsjabloon voor workflowmeldingen** de gewenste sjabloon.</span><span class="sxs-lookup"><span data-stu-id="12af6-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="12af6-122">Instructies voor gebruikers opgeven</span><span class="sxs-lookup"><span data-stu-id="12af6-122">Enter instructions for users</span></span>

<span data-ttu-id="12af6-123">Het is mogelijk om instructies op te geven voor gebruikers die documenten voor verwerking en goedkeuring indienen.</span><span class="sxs-lookup"><span data-stu-id="12af6-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="12af6-124">Deze gebruikers worden ook wel aangeduid als *opdrachtgevers*.</span><span class="sxs-lookup"><span data-stu-id="12af6-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="12af6-125">Stel dat u een workflow voor inkoopbestelopdrachten voor Spanje maakt en instructies invoert.</span><span class="sxs-lookup"><span data-stu-id="12af6-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="12af6-126">Deze instructies kunnen vervolgens door gebruikers worden bekeken die inkoopopdrachten invoeren op de pagina **Opdrachten tot inkoop**.</span><span class="sxs-lookup"><span data-stu-id="12af6-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="12af6-127">De starter klikt op het pictogram op de berichtenbalk om instructies weer te geven.</span><span class="sxs-lookup"><span data-stu-id="12af6-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="12af6-128">Voer de volgende stappen uit om instructies voor gebruikers op te geven.</span><span class="sxs-lookup"><span data-stu-id="12af6-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="12af6-129">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="12af6-130">Voer in het veld **Indieningsinstructies** de instructies in.</span><span class="sxs-lookup"><span data-stu-id="12af6-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="12af6-131">Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="12af6-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="12af6-132">Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="12af6-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="12af6-133">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="12af6-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="12af6-134">Klik in het veld **Indieningsinstructies** om op te geven waar de tijdelijke aanduiding moet verschijnen.</span><span class="sxs-lookup"><span data-stu-id="12af6-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="12af6-135">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="12af6-136">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="12af6-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="12af6-137">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-137">Click **Insert**.</span></span>

4. <span data-ttu-id="12af6-138">Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="12af6-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="12af6-139">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="12af6-140">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="12af6-141">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="12af6-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="12af6-142">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="12af6-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="12af6-143">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="12af6-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="12af6-144">Zie de stap 3 voor instructies voor het invoeren van een tijdelijke aanduiding.</span><span class="sxs-lookup"><span data-stu-id="12af6-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="12af6-145">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="12af6-145">Click **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="12af6-146">Tijdelijke aanduidingen kunnen niet worden toegevoegd met kopiëren en plakken, omdat de doelgegevens niet op de juiste manier worden geplakt.</span><span class="sxs-lookup"><span data-stu-id="12af6-146">Placeholders cannot be added using copy and paste because the target information is not pasted in correctly.</span></span> <span data-ttu-id="12af6-147">Gebruik de interface om tijdelijke aanduidingen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="12af6-147">Use the interface to add placeholders.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="12af6-148">Geef op wanneer deze workflow wordt gebruikt via activeringsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="12af6-148">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="12af6-149">Het is mogelijk om op basis van hetzelfde workflowtype meerdere workflows te maken.</span><span class="sxs-lookup"><span data-stu-id="12af6-149">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="12af6-150">Als u meerdere workflows op hetzelfde type hebt gebaseerd, moet u voor elke workflow opgeven wanneer deze wordt gebruikt met activeringsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="12af6-150">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="12af6-151">Als niet aan de activeringsvoorwaarden wordt voldaan, wordt de standaardworkflow gebruikt.</span><span class="sxs-lookup"><span data-stu-id="12af6-151">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="12af6-152">Als er slechts één workflowconfiguratie is gedefinieerd voor een workflowtype, wordt die workflowconfiguratie gebruikt, ongeacht de activeringsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="12af6-152">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="12af6-153">U kunt bijvoorbeeld een workflow voor opdrachten tot inkoop maken voor elk land of elke regio waarin uw bedrijf actief is, zoals Inkoopbestelopdrachten Denemarken en Inkoopbestelopdrachten Spanje, met de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="12af6-153">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="12af6-154">Opdrachten tot inkoop Denemarken wordt gebruikt als: land/regio = DK</span><span class="sxs-lookup"><span data-stu-id="12af6-154">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="12af6-155">Opdrachten tot inkoop Spanje wordt gebruikt als: land/regio = ES.</span><span class="sxs-lookup"><span data-stu-id="12af6-155">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="12af6-156">Voer de volgende stappen uit om op te geven wanneer de workflow die u configureert, wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="12af6-156">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="12af6-157">Klik in het linkerdeelvenster op **Activering**.</span><span class="sxs-lookup"><span data-stu-id="12af6-157">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="12af6-158">Schakel het selectievakje **De voorwaarden voor het uitvoeren van deze workflow instellen** in.</span><span class="sxs-lookup"><span data-stu-id="12af6-158">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="12af6-159">Klik op **Voorwaarde toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-159">Click **Add condition**.</span></span>
4. <span data-ttu-id="12af6-160">Een voorwaarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="12af6-160">Enter a condition.</span></span>
5. <span data-ttu-id="12af6-161">Geef desgewenst vereiste extra voorwaarden op.</span><span class="sxs-lookup"><span data-stu-id="12af6-161">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="12af6-162">Voer de workflow uit met een aantal doelrecords om te controleren of de voorwaarde op de juiste manier records opneemt en uitsluit.</span><span class="sxs-lookup"><span data-stu-id="12af6-162">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="12af6-163">Opgeven wanneer meldingen worden verzonden</span><span class="sxs-lookup"><span data-stu-id="12af6-163">Specify when notifications are sent</span></span>

<span data-ttu-id="12af6-164">Als een document wordt ingediend voor verwerking, wordt een workflowexemplaar gemaakt.</span><span class="sxs-lookup"><span data-stu-id="12af6-164">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="12af6-165">Het is mogelijk om meldingen aan gebruikers te verzenden wanneer workflowexemplaren op basis van de workflow worden gestart, voltooid, beëindigd of gestopt vanwege een fout.</span><span class="sxs-lookup"><span data-stu-id="12af6-165">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="12af6-166">Voer de volgende stappen uit om op te geven wanneer meldingen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="12af6-166">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="12af6-167">Klik in het linkerdeelvenster op **Meldingen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-167">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="12af6-168">Vink het selectievakje aan voor elke gebeurtenis die meldingen moet activeren:</span><span class="sxs-lookup"><span data-stu-id="12af6-168">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="12af6-169">**Gestart**: meldingen verzenden wanneer een workflowexemplaar wordt gestart.</span><span class="sxs-lookup"><span data-stu-id="12af6-169">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="12af6-170">**Gestopt**: meldingen verzenden wanneer een workflowexemplaar wordt gestopt vanwege een fout.</span><span class="sxs-lookup"><span data-stu-id="12af6-170">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="12af6-171">**Voltooid**: meldingen verzenden wanneer een workflowexemplaar is voltooid.</span><span class="sxs-lookup"><span data-stu-id="12af6-171">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="12af6-172">**Onherstelbaar**: meldingen verzenden wanneer een workflowexemplaar wordt gestopt vanwege een onherstelbare fout.</span><span class="sxs-lookup"><span data-stu-id="12af6-172">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="12af6-173">**Beëindigd**: meldingen verzenden wanneer een workflowexemplaar is beëindigd.</span><span class="sxs-lookup"><span data-stu-id="12af6-173">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="12af6-174">Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="12af6-174">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="12af6-175">Geef op het tabblad **Meldingstekst** de tekst van de melding op.</span><span class="sxs-lookup"><span data-stu-id="12af6-175">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="12af6-176">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="12af6-176">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="12af6-177">Wanneer de tekst aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="12af6-177">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="12af6-178">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="12af6-178">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="12af6-179">Klik in het veld om op te geven waar de tijdelijke aanduiding moet verschijnen.</span><span class="sxs-lookup"><span data-stu-id="12af6-179">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="12af6-180">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-180">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="12af6-181">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="12af6-181">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="12af6-182">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-182">Click **Insert**.</span></span>
    5. <span data-ttu-id="12af6-183">Een algemene tijdelijke aanduiding **meldingstekst** om op te nemen is 'Laatste notities: %Workflow.Last note%', waarmee alle opmerkingen uit de vorige stap worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="12af6-183">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="12af6-184">Voer de onderstaande stappen uit om vertalingen van de tekst toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="12af6-184">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="12af6-185">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-185">Click **Translations**.</span></span>
    2. <span data-ttu-id="12af6-186">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-186">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="12af6-187">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="12af6-187">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="12af6-188">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="12af6-188">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="12af6-189">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="12af6-189">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="12af6-190">Zie de stap 5 voor instructies voor het invoeren van een tijdelijke aanduiding.</span><span class="sxs-lookup"><span data-stu-id="12af6-190">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="12af6-191">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="12af6-191">Click **Close**.</span></span>

7. <span data-ttu-id="12af6-192">Geef met de volgende opties op het tabblad **Ontvanger** op wie de meldingen moet ontvangen.</span><span class="sxs-lookup"><span data-stu-id="12af6-192">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="12af6-193">Optie</span><span class="sxs-lookup"><span data-stu-id="12af6-193">Option</span></span></th>
    <th><span data-ttu-id="12af6-194">Meldingen worden verzend naar deze gebruikers</span><span class="sxs-lookup"><span data-stu-id="12af6-194">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="12af6-195">Voer de volgende stappen uit meldingen te laten verzenden.</span><span class="sxs-lookup"><span data-stu-id="12af6-195">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="12af6-196">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="12af6-196">Participant</span></span></td>
    <td><span data-ttu-id="12af6-197">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="12af6-197">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="12af6-198">Klik op het tabblad <strong>Ontvanger</strong> op <strong>Deelnemer</strong>.</span><span class="sxs-lookup"><span data-stu-id="12af6-198">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="12af6-199">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="12af6-199">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="12af6-200">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="12af6-200">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="12af6-201">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="12af6-201">Workflow user</span></span></td>
    <td><span data-ttu-id="12af6-202">Gebruikers die deelnemers zijn in deze workflow</span><span class="sxs-lookup"><span data-stu-id="12af6-202">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="12af6-203">Klik op het tabblad <strong>Ontvanger</strong> op <strong>Workflowgebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="12af6-203">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="12af6-204">Selecteer op het tabblad <strong>Workflowgebruiker</strong> in de lijst <strong>Workflowgebruiker</strong> een deelnemer aan deze workflow.</span><span class="sxs-lookup"><span data-stu-id="12af6-204">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="12af6-205">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="12af6-205">User</span></span></td>
    <td><span data-ttu-id="12af6-206">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="12af6-206">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="12af6-207">Klik op het tabblad <strong>Ontvanger</strong> op <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="12af6-207">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="12af6-208">Op het tabblad <strong>Gebruiker</strong> bevat de lijst <strong>Beschikbare gebruikers</strong> alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="12af6-208">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="12af6-209">Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="12af6-209">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="12af6-210">Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="12af6-210">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="12af6-211">Ppmerkingen invoeren over de wijzigingen die u in de workflow hebt aangebracht</span><span class="sxs-lookup"><span data-stu-id="12af6-211">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="12af6-212">Voer de volgende stappen uit om opmerkingen in te voeren over de wijzigingen die u in deze workflow hebt aangebracht.</span><span class="sxs-lookup"><span data-stu-id="12af6-212">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="12af6-213">Klik in het linkerdeelvenster op **Opmerkingen**.</span><span class="sxs-lookup"><span data-stu-id="12af6-213">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="12af6-214">Voer in het veld **Opmerkingen over de workflow invoeren** uw opmerkingen in.</span><span class="sxs-lookup"><span data-stu-id="12af6-214">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="12af6-215">Uw opmerkingen controleren.</span><span class="sxs-lookup"><span data-stu-id="12af6-215">Review your comments.</span></span> <span data-ttu-id="12af6-216">Nadat u opmerkingen hebt toegevoegd, kunt u deze niet meer wijzigen.</span><span class="sxs-lookup"><span data-stu-id="12af6-216">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="12af6-217">Klik op **Toevoegen** om uw opmerkingen aan het gebied **Opmerkingshistorie** toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="12af6-217">Click **Add** to add your comments to the **Comment history** area.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]