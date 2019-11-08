---
title: Workfloweigenschappen configureren
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een workflow configureert.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76d44c472989a73d71c2edd19f1187ecd09827ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190115"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="0ed19-103">Workfloweigenschappen configureren</span><span class="sxs-lookup"><span data-stu-id="0ed19-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ed19-104">In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een workflow configureert.</span><span class="sxs-lookup"><span data-stu-id="0ed19-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="0ed19-105">Open de workflow in de workfloweditor om de eigenschappen van een specifiek workflowelement te configureren.</span><span class="sxs-lookup"><span data-stu-id="0ed19-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="0ed19-106">Klik op het tekenpapier van de workfloweditor en klik op **Eigenschappen** om de pagina **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="0ed19-107">Met behulp van de volgende procedures kunt u de verschillende eigenschappen van de workflow configureren.</span><span class="sxs-lookup"><span data-stu-id="0ed19-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="0ed19-108">Naam voor de workflow opgeven</span><span class="sxs-lookup"><span data-stu-id="0ed19-108">Name the workflow</span></span>

<span data-ttu-id="0ed19-109">Voer deze stappen uit om een naam op te geven voor de workflow.</span><span class="sxs-lookup"><span data-stu-id="0ed19-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="0ed19-110">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="0ed19-111">Geef in het veld **Naam** een unieke naam voor de workflow op.</span><span class="sxs-lookup"><span data-stu-id="0ed19-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="0ed19-112">Als u bijvoorbeeld een workflow voor opdrachten tot inkoop maakt voor elk land of elke regio waarin uw bedrijf actief is, kunt u als naam voor de workflow **Inkoopbestelopdrachten Denemarken** of **Inkoopbestelopdrachten Spanje** opgeven.</span><span class="sxs-lookup"><span data-stu-id="0ed19-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="0ed19-113">Eigenaar van de workflow opgeven</span><span class="sxs-lookup"><span data-stu-id="0ed19-113">Specify the workflow owner</span></span>

<span data-ttu-id="0ed19-114">De eigenaar van de workflow is degene die deze workflow beheert en onderhoudt.</span><span class="sxs-lookup"><span data-stu-id="0ed19-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="0ed19-115">Voer de volgende stappen uit om de eigenaar van de workflow op te geven.</span><span class="sxs-lookup"><span data-stu-id="0ed19-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="0ed19-116">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="0ed19-117">Selecteer in de lijst **Eigenaar** de naam van degene die de workflow beheert.</span><span class="sxs-lookup"><span data-stu-id="0ed19-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="0ed19-118">Een e-mailsjabloon selecteren</span><span class="sxs-lookup"><span data-stu-id="0ed19-118">Select an email template</span></span>

<span data-ttu-id="0ed19-119">Volg deze stappen om de e-mailsjabloon te selecteren die wordt gebruikt om meldingen te genereren voor deze workflow.</span><span class="sxs-lookup"><span data-stu-id="0ed19-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="0ed19-120">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="0ed19-121">Selecteer in de lijst **E-mailsjabloon voor workflowmeldingen** de gewenste sjabloon.</span><span class="sxs-lookup"><span data-stu-id="0ed19-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="0ed19-122">Instructies voor gebruikers opgeven</span><span class="sxs-lookup"><span data-stu-id="0ed19-122">Enter instructions for users</span></span>

<span data-ttu-id="0ed19-123">Het is mogelijk om instructies op te geven voor gebruikers die documenten voor verwerking en goedkeuring indienen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="0ed19-124">Deze gebruikers worden ook wel aangeduid als *opdrachtgevers*.</span><span class="sxs-lookup"><span data-stu-id="0ed19-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="0ed19-125">Stel dat u een workflow voor inkoopbestelopdrachten voor Spanje maakt en instructies invoert.</span><span class="sxs-lookup"><span data-stu-id="0ed19-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="0ed19-126">Deze instructies kunnen vervolgens door gebruikers worden bekeken die inkoopopdrachten invoeren op de pagina **Opdrachten tot inkoop**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="0ed19-127">De starter klikt op het pictogram op de berichtenbalk om instructies weer te geven.</span><span class="sxs-lookup"><span data-stu-id="0ed19-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="0ed19-128">Voer de volgende stappen uit om instructies voor gebruikers op te geven.</span><span class="sxs-lookup"><span data-stu-id="0ed19-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="0ed19-129">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="0ed19-130">Voer in het veld **Indieningsinstructies** de instructies in.</span><span class="sxs-lookup"><span data-stu-id="0ed19-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="0ed19-131">Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="0ed19-132">Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="0ed19-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="0ed19-133">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="0ed19-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="0ed19-134">Klik in het veld **Indieningsinstructies** om op te geven waar de tijdelijke aanduiding moet verschijnen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="0ed19-135">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="0ed19-136">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="0ed19-137">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-137">Click **Insert**.</span></span>

4. <span data-ttu-id="0ed19-138">Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="0ed19-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="0ed19-139">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="0ed19-140">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="0ed19-141">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="0ed19-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="0ed19-142">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="0ed19-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="0ed19-143">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="0ed19-144">Zie de stap 3 voor instructies voor het invoeren van een tijdelijke aanduiding.</span><span class="sxs-lookup"><span data-stu-id="0ed19-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="0ed19-145">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="0ed19-146">Opgeven wanneer deze workflow wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="0ed19-146">Specify when this workflow is used</span></span>

<span data-ttu-id="0ed19-147">Het is mogelijk om op basis van hetzelfde type meerdere workflows te maken.</span><span class="sxs-lookup"><span data-stu-id="0ed19-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="0ed19-148">U kunt bijvoorbeeld een workflow voor opdrachten tot inkoop maken voor elk land of elke regio waarin uw bedrijf actief is, zoals Inkoopbestelopdrachten Denemarken en Inkoopbestelopdrachten Spanje.</span><span class="sxs-lookup"><span data-stu-id="0ed19-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="0ed19-149">Als u meerdere workflows op hetzelfde type hebt gebaseerd, moet u voor elke workflow opgeven wanneer deze wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0ed19-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="0ed19-150">Voor het voorafgaande voorbeeld moet u dus de volgende voorwaarden opgeven:</span><span class="sxs-lookup"><span data-stu-id="0ed19-150">For the preceding example, you specify the following conditions:</span></span>

- <span data-ttu-id="0ed19-151">Opdrachten tot inkoop Denemarken wordt gebruikt als: land/regio = DK</span><span class="sxs-lookup"><span data-stu-id="0ed19-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="0ed19-152">Opdrachten tot inkoop Spanje wordt gebruikt als: land/regio = ES.</span><span class="sxs-lookup"><span data-stu-id="0ed19-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="0ed19-153">Voer de volgende stappen uit om op te geven wanneer de workflow die u configureert, wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0ed19-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="0ed19-154">Klik in het linkerdeelvenster op **Activering**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-154">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="0ed19-155">Schakel het selectievakje **De voorwaarden voor het uitvoeren van deze workflow instellen** in.</span><span class="sxs-lookup"><span data-stu-id="0ed19-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="0ed19-156">Klik op **Voorwaarde toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-156">Click **Add condition**.</span></span>
4. <span data-ttu-id="0ed19-157">Een voorwaarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="0ed19-157">Enter a condition.</span></span>
5. <span data-ttu-id="0ed19-158">Geef desgewenst vereiste extra voorwaarden op.</span><span class="sxs-lookup"><span data-stu-id="0ed19-158">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="0ed19-159">Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn ingesteld:</span><span class="sxs-lookup"><span data-stu-id="0ed19-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="0ed19-160">Klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-160">Click **Test**.</span></span>
    2. <span data-ttu-id="0ed19-161">Ga naar de pagina **Workflowvoorwaarde testen** en selecteer in het gebied **Voorwaarde valideren** een record.</span><span class="sxs-lookup"><span data-stu-id="0ed19-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="0ed19-162">Klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-162">Click **Test**.</span></span> <span data-ttu-id="0ed19-163">Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="0ed19-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="0ed19-164">Als u bijvoorbeeld een workflow voor opdrachten tot inkoop voor Spanje maakt, wordt in het gebied **Voorwaarde valideren** van de pagina een lijst met opdrachten tot inkoop getoond.</span><span class="sxs-lookup"><span data-stu-id="0ed19-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="0ed19-165">Als u op **Testen** klikt, wordt de geselecteerde opdracht tot inkoop door het systeem geëvalueerd om na te gaan of het land of de regio gelijk is aan ES.</span><span class="sxs-lookup"><span data-stu-id="0ed19-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="0ed19-166">Klik op **OK** of **Annuleren** om terug te gaan naar de pagina **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="0ed19-167">Opgeven wanneer meldingen worden verzonden</span><span class="sxs-lookup"><span data-stu-id="0ed19-167">Specify when notifications are sent</span></span>

<span data-ttu-id="0ed19-168">Als een document wordt ingediend voor verwerking, wordt een workflowexemplaar gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0ed19-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="0ed19-169">Het is mogelijk om meldingen aan gebruikers te verzenden wanneer workflowexemplaren op basis van de workflow worden gestart, voltooid, beëindigd of gestopt vanwege een fout.</span><span class="sxs-lookup"><span data-stu-id="0ed19-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="0ed19-170">Voer de volgende stappen uit om op te geven wanneer meldingen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="0ed19-170">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="0ed19-171">Klik in het linkerdeelvenster op **Meldingen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-171">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="0ed19-172">Vink het selectievakje aan voor elke gebeurtenis die meldingen moet activeren:</span><span class="sxs-lookup"><span data-stu-id="0ed19-172">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="0ed19-173">**Gestart**: meldingen verzenden wanneer een workflowexemplaar wordt gestart.</span><span class="sxs-lookup"><span data-stu-id="0ed19-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="0ed19-174">**Gestopt**: meldingen verzenden wanneer een workflowexemplaar wordt gestopt vanwege een fout.</span><span class="sxs-lookup"><span data-stu-id="0ed19-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="0ed19-175">**Voltooid**: meldingen verzenden wanneer een workflowexemplaar is voltooid.</span><span class="sxs-lookup"><span data-stu-id="0ed19-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="0ed19-176">**Onherstelbaar**: meldingen verzenden wanneer een workflowexemplaar wordt gestopt vanwege een onherstelbare fout.</span><span class="sxs-lookup"><span data-stu-id="0ed19-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="0ed19-177">**Beëindigd**: meldingen verzenden wanneer een workflowexemplaar is beëindigd.</span><span class="sxs-lookup"><span data-stu-id="0ed19-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="0ed19-178">Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0ed19-178">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="0ed19-179">Geef op het tabblad **Meldingstekst** de tekst van de melding op.</span><span class="sxs-lookup"><span data-stu-id="0ed19-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="0ed19-180">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="0ed19-181">Wanneer de tekst aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="0ed19-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="0ed19-182">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="0ed19-182">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="0ed19-183">Klik in het veld om op te geven waar de tijdelijke aanduiding moet verschijnen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-183">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="0ed19-184">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-184">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="0ed19-185">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-185">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="0ed19-186">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-186">Click **Insert**.</span></span>
    5. <span data-ttu-id="0ed19-187">Een algemene tijdelijke aanduiding **meldingstekst** om op te nemen is 'Laatste notities: %Workflow.Last note%', waarmee alle opmerkingen uit de vorige stap worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0ed19-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="0ed19-188">Voer de onderstaande stappen uit om vertalingen van de tekst toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="0ed19-188">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="0ed19-189">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-189">Click **Translations**.</span></span>
    2. <span data-ttu-id="0ed19-190">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-190">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="0ed19-191">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="0ed19-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="0ed19-192">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="0ed19-192">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="0ed19-193">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="0ed19-194">Zie de stap 5 voor instructies voor het invoeren van een tijdelijke aanduiding.</span><span class="sxs-lookup"><span data-stu-id="0ed19-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="0ed19-195">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-195">Click **Close**.</span></span>

7. <span data-ttu-id="0ed19-196">Geef met de volgende opties op het tabblad **Ontvanger** op wie de meldingen moet ontvangen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="0ed19-197">Optie</span><span class="sxs-lookup"><span data-stu-id="0ed19-197">Option</span></span></th>
    <th><span data-ttu-id="0ed19-198">Meldingen worden verzend naar deze gebruikers</span><span class="sxs-lookup"><span data-stu-id="0ed19-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="0ed19-199">Voer de volgende stappen uit meldingen te laten verzenden.</span><span class="sxs-lookup"><span data-stu-id="0ed19-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="0ed19-200">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="0ed19-200">Participant</span></span></td>
    <td><span data-ttu-id="0ed19-201">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="0ed19-201">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="0ed19-202">Klik op het tabblad <strong>Ontvanger</strong> op <strong>Deelnemer</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ed19-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="0ed19-203">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="0ed19-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="0ed19-204">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="0ed19-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="0ed19-205">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="0ed19-205">Workflow user</span></span></td>
    <td><span data-ttu-id="0ed19-206">Gebruikers die deelnemers zijn in deze workflow</span><span class="sxs-lookup"><span data-stu-id="0ed19-206">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="0ed19-207">Klik op het tabblad <strong>Ontvanger</strong> op <strong>Workflowgebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ed19-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="0ed19-208">Selecteer op het tabblad <strong>Workflowgebruiker</strong> in de lijst <strong>Workflowgebruiker</strong> een deelnemer aan deze workflow.</span><span class="sxs-lookup"><span data-stu-id="0ed19-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="0ed19-209">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="0ed19-209">User</span></span></td>
    <td><span data-ttu-id="0ed19-210">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="0ed19-210">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="0ed19-211">Klik op het tabblad <strong>Ontvanger</strong> op <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ed19-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="0ed19-212">Op het tabblad <strong>Gebruiker</strong> bevat de lijst <strong>Beschikbare gebruikers</strong> alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="0ed19-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="0ed19-213">Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ed19-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="0ed19-214">Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0ed19-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="0ed19-215">Ppmerkingen invoeren over de wijzigingen die u in de workflow hebt aangebracht</span><span class="sxs-lookup"><span data-stu-id="0ed19-215">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="0ed19-216">Voer de volgende stappen uit om opmerkingen in te voeren over de wijzigingen die u in deze workflow hebt aangebracht.</span><span class="sxs-lookup"><span data-stu-id="0ed19-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="0ed19-217">Klik in het linkerdeelvenster op **Opmerkingen**.</span><span class="sxs-lookup"><span data-stu-id="0ed19-217">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="0ed19-218">Voer in het veld **Opmerkingen over de workflow invoeren** uw opmerkingen in.</span><span class="sxs-lookup"><span data-stu-id="0ed19-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="0ed19-219">Uw opmerkingen controleren.</span><span class="sxs-lookup"><span data-stu-id="0ed19-219">Review your comments.</span></span> <span data-ttu-id="0ed19-220">Nadat u opmerkingen hebt toegevoegd, kunt u deze niet meer wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-220">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="0ed19-221">Klik op **Toevoegen** om uw opmerkingen aan het gebied **Opmerkingshistorie** toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="0ed19-221">Click **Add** to add your comments to the **Comment history** area.</span></span>