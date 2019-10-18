---
title: Handmatige beslissingen configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige beslissing configureert.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f46b875f52d3d3e7c755ee92dcd5faddf0d94356
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177254"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="92ea3-103">Handmatige beslissingen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="92ea3-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92ea3-104">In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige beslissing configureert.</span><span class="sxs-lookup"><span data-stu-id="92ea3-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="92ea3-105">Om een handmatige beslissing te configureren, klikt u in de workfloweditor met de rechtermuisknop op de handmatige beslissing en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="92ea3-106">Vervolgens kunt u met de volgende procedures de eigenschappen van de handmatige beslissing configureren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="92ea3-107">Naam van de beslissing</span><span class="sxs-lookup"><span data-stu-id="92ea3-107">Name the decision</span></span>

<span data-ttu-id="92ea3-108">Voer deze stappen uit om een naam op te geven voor de handmatige beslissing.</span><span class="sxs-lookup"><span data-stu-id="92ea3-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="92ea3-109">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="92ea3-110">Voer in het veld **Naam** een unieke naam voor de handmatige beslissing in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="92ea3-111">Een onderwerpregel en instructies invoeren</span><span class="sxs-lookup"><span data-stu-id="92ea3-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="92ea3-112">U moet een onderwerpregel en instructies invoeren voor de gebruikers die aan de handmatige beslissing zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="92ea3-113">Als u bijvoorbeeld een beslissing voor opdrachten tot inkoop configureert, ziet de gebruiker die aan de beslissing is toegewezen de onderwerpregel en instructies op de pagina **Opdrachten tot inkoop**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="92ea3-114">De onderwerpregel verschijnt in de berichtenbalk van de pagina.</span><span class="sxs-lookup"><span data-stu-id="92ea3-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="92ea3-115">De gebruiker kan vervolgens klikken op het pictogram op de berichtenbalk om de instructies weer te geven.</span><span class="sxs-lookup"><span data-stu-id="92ea3-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="92ea3-116">Voer deze stappen uit om een onderwerpregel en instructies in te voeren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="92ea3-117">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="92ea3-118">Op het tabblad **Instructies** voert u in het veld **Onderwerp werkitem** de onderwerpregel in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="92ea3-119">Als u de onderwerpregel wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="92ea3-120">Wanneer de onderwerpregel aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="92ea3-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="92ea3-121">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="92ea3-122">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="92ea3-123">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="92ea3-124">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="92ea3-125">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-125">Click **Insert**.</span></span>

4. <span data-ttu-id="92ea3-126">Voer de onderstaande stappen uit om vertalingen van de onderwerpregel toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="92ea3-127">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="92ea3-128">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="92ea3-129">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="92ea3-130">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="92ea3-131">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 3.</span><span class="sxs-lookup"><span data-stu-id="92ea3-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="92ea3-132">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-132">Click **Close**.</span></span>

5. <span data-ttu-id="92ea3-133">Voer in het veld **Instructies werkitem** de instructies in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="92ea3-134">Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="92ea3-135">Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="92ea3-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="92ea3-136">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="92ea3-137">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="92ea3-138">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="92ea3-139">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="92ea3-140">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-140">Click **Insert**.</span></span>

7. <span data-ttu-id="92ea3-141">Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="92ea3-142">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="92ea3-143">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="92ea3-144">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="92ea3-145">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="92ea3-146">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 6.</span><span class="sxs-lookup"><span data-stu-id="92ea3-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="92ea3-147">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="92ea3-148">De mogelijke resultaten van een beslissing opgeven</span><span class="sxs-lookup"><span data-stu-id="92ea3-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="92ea3-149">Wanneer een document aan een besluitvormer is toewezen, krijgt de besluitvormer doorgaans een vraag voorgelegd.</span><span class="sxs-lookup"><span data-stu-id="92ea3-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="92ea3-150">Het antwoord op deze vraag is doorgaans **Ja** of **Nee**, of **Waar** of **Onwaar**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="92ea3-151">Voer de volgende stappen uit om de mogelijk resultaten op te geven van de handmatige beslissing.</span><span class="sxs-lookup"><span data-stu-id="92ea3-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="92ea3-152">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="92ea3-153">Geef op het tabblad **Resultaten** in het veld **Resultaat 1** de naam van het resultaat of de optie op.</span><span class="sxs-lookup"><span data-stu-id="92ea3-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="92ea3-154">Voer de onderstaande stappen uit om vertalingen van het resultaat toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="92ea3-155">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="92ea3-156">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="92ea3-157">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="92ea3-158">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="92ea3-159">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-159">Click **Close**.</span></span>

4. <span data-ttu-id="92ea3-160">Geef in het veld **Uitkomst 2** de naam van het resultaat of de optie op.</span><span class="sxs-lookup"><span data-stu-id="92ea3-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="92ea3-161">Voer de onderstaande stappen uit om vertalingen van het resultaat toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="92ea3-162">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="92ea3-163">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="92ea3-164">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="92ea3-165">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="92ea3-166">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="92ea3-167">Opgeven wanneer meldingen worden verzonden</span><span class="sxs-lookup"><span data-stu-id="92ea3-167">Specify when notifications are sent</span></span>

<span data-ttu-id="92ea3-168">U kunt meldingen naar gebruikers verzenden wanneer een beslissing is genomen, gedelegeerd, geëscaleerd.</span><span class="sxs-lookup"><span data-stu-id="92ea3-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="92ea3-169">Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="92ea3-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="92ea3-170">Klik in het linkerdeelvenster op **Meldingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="92ea3-171">Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:</span><span class="sxs-lookup"><span data-stu-id="92ea3-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="92ea3-172">**\[Keuze 1\]** – de toegewezen gebruiker heeft **\[Keuze 1\]** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="92ea3-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="92ea3-173">**\[Keuze 2\]** – de toegewezen gebruiker heeft **\[Keuze 2\]** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="92ea3-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="92ea3-174">**Delegeren**: de toegewezen gebruiker heeft de beslissing aan een andere gebruiker toegewezen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="92ea3-175">**Escaleren**: de toegewezen gebruiker heeft de beslssing niet niet binnen de toegekende tijd genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="92ea3-176">Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="92ea3-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="92ea3-177">Geef op het tabblad **Meldingstekst** de tekst van de melding op.</span><span class="sxs-lookup"><span data-stu-id="92ea3-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="92ea3-178">Als u de melding wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="92ea3-179">Wanneer de melding aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="92ea3-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="92ea3-180">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="92ea3-181">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="92ea3-182">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="92ea3-183">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="92ea3-184">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-184">Click **Insert**.</span></span>

6. <span data-ttu-id="92ea3-185">Voer de onderstaande stappen uit om vertalingen van de melding toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="92ea3-186">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="92ea3-187">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="92ea3-188">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="92ea3-189">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="92ea3-190">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 5.</span><span class="sxs-lookup"><span data-stu-id="92ea3-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="92ea3-191">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-191">Click **Close**.</span></span>

7. <span data-ttu-id="92ea3-192">Geef op het tabblad **Ontvanger** op aan wie de meldingen moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="92ea3-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="92ea3-193">Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de betreffende optie voordat u naar stap 8 gaat.</span><span class="sxs-lookup"><span data-stu-id="92ea3-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="92ea3-194">Optie</span><span class="sxs-lookup"><span data-stu-id="92ea3-194">Option</span></span></th>
    <th><span data-ttu-id="92ea3-195">Ontvangers van meldingen</span><span class="sxs-lookup"><span data-stu-id="92ea3-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="92ea3-196">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="92ea3-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="92ea3-197">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="92ea3-197">Participant</span></span></td>
    <td><span data-ttu-id="92ea3-198">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="92ea3-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="92ea3-199">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt laten verzenden.</span><span class="sxs-lookup"><span data-stu-id="92ea3-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="92ea3-200">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="92ea3-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="92ea3-201">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="92ea3-201">Workflow user</span></span></td>
    <td><span data-ttu-id="92ea3-202">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="92ea3-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="92ea3-203">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="92ea3-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="92ea3-204">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="92ea3-204">User</span></span></td>
    <td><span data-ttu-id="92ea3-205">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="92ea3-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="92ea3-206">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="92ea3-207">De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="92ea3-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="92ea3-208">Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="92ea3-209">Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="92ea3-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="92ea3-210">Een beslissing toewijzen</span><span class="sxs-lookup"><span data-stu-id="92ea3-210">Assign a decision</span></span>

<span data-ttu-id="92ea3-211">Voer de volgende stappen uit om op te geven aan wie de handmatige beslissing moet worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="92ea3-212">Klik in het linkerdeelvensters op het pictogram **Toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="92ea3-213">Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 3 gaat.</span><span class="sxs-lookup"><span data-stu-id="92ea3-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="92ea3-214">Optie</span><span class="sxs-lookup"><span data-stu-id="92ea3-214">Option</span></span></th>
    <th><span data-ttu-id="92ea3-215">Gebruikers aan wie de beslissing is toegewezen</span><span class="sxs-lookup"><span data-stu-id="92ea3-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="92ea3-216">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="92ea3-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="92ea3-217">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="92ea3-217">Participant</span></span></td>
    <td><span data-ttu-id="92ea3-218">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="92ea3-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="92ea3-219">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waaraan u de beslissing wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="92ea3-220">Selecteer in de lijst <strong>Deelnemer</strong> het type groep of rol waaraan u de beslissing wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="92ea3-221">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="92ea3-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="92ea3-222">Gebruikers in een specifieke organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="92ea3-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="92ea3-223">Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waaraan u de beslissing wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="92ea3-224">Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="92ea3-225">Deze namen stellen gebruikers voor waaraan de beslissing kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="92ea3-226">Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:</span><span class="sxs-lookup"><span data-stu-id="92ea3-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="92ea3-227">Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="92ea3-228">Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven.</span><span class="sxs-lookup"><span data-stu-id="92ea3-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="92ea3-229">Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="92ea3-230">Geeft op het tabblad <strong>Hiërarchieopties</strong> op aan welke gebruikers in het bereik de beslissing moet worden toegewezen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="92ea3-231"><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de beslissing wordt toegewezen aan alle gebruikers in het bereik.</span><span class="sxs-lookup"><span data-stu-id="92ea3-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="92ea3-232"><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de beslissing wordt alleen aan de laatste gebruiker in het bereik toegewezen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="92ea3-233"><strong>Gebruikers met de volgende status uitsluiten</strong>: de beslissing wordt niet toegewezen aan een gebruiker in het bereik die aan een specifieke voorwaarde voldoet.</span><span class="sxs-lookup"><span data-stu-id="92ea3-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="92ea3-234">Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</span><span class="sxs-lookup"><span data-stu-id="92ea3-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="92ea3-235">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="92ea3-235">Workflow user</span></span></td>
    <td><span data-ttu-id="92ea3-236">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="92ea3-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="92ea3-237">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="92ea3-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="92ea3-238">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="92ea3-238">User</span></span></td>
    <td><span data-ttu-id="92ea3-239">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="92ea3-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="92ea3-240">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="92ea3-241">De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="92ea3-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="92ea3-242">Selecteer de gebruikers aan wie u de beslissing wilt toewijzen en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="92ea3-243">Wachtrij</span><span class="sxs-lookup"><span data-stu-id="92ea3-243">Queue</span></span></td>
    <td><span data-ttu-id="92ea3-244">Een wachtrij voor werkitems</span><span class="sxs-lookup"><span data-stu-id="92ea3-244">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="92ea3-245">Selecteer het tabblad <strong>Wachtrij</strong> en klik op het tabblad <strong>Wachtrijgebaseerd</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="92ea3-246">Voer deze stappen uit om de beslissing aan een specifieke wachtrij toe te wijzen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="92ea3-247">Selecteer in de lijst <strong>Wachtrijtype</strong> de waarde <strong>Wachtrijen voor werkitems</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="92ea3-248">Selecteer in de lijst <strong>Wachtrijnaam</strong> de gewenste wachtrij.</span><span class="sxs-lookup"><span data-stu-id="92ea3-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="92ea3-249">Als een specifieke voorwaarde moet bepalen aan welke wachtrij de beslissing wordt toegewezen, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="92ea3-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="92ea3-250">Selecteer in de lijst <strong>Wachtrijtype</strong> de waarde <strong>Voorwaardelijke wachtrijen voor werkitems</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="92ea3-251">Selecteer in de lijst <strong>Wachtrijnaam</strong> de waarde <strong>Voorwaardelijke wachtrij</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="92ea3-252">Deze optie wordt alleen bij enkele workflows toegepast, zoals Aanvraagbeheer.</span><span class="sxs-lookup"><span data-stu-id="92ea3-252">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="92ea3-253">Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="92ea3-254">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="92ea3-254">Select one of the following options:</span></span>

    - <span data-ttu-id="92ea3-255">**Uren**: voer het aantal uren in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="92ea3-256">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="92ea3-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="92ea3-257">**Dagen**: voer het aantal dagen in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="92ea3-258">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="92ea3-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="92ea3-259">**Weken**: voer het aantal weken in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="92ea3-260">**Maanden**: selecteer de dag en week waarop de gebruiker de beslissing uiterlijk moet hebben genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="92ea3-261">U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van de maand.</span><span class="sxs-lookup"><span data-stu-id="92ea3-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="92ea3-262">**Jaren**: selecteer de dag, week en maand waarop de gebruiker de beslissing uiterlijk moet hebben genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="92ea3-263">U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van december.</span><span class="sxs-lookup"><span data-stu-id="92ea3-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="92ea3-264">Als de gebruiker niet binnen de toegekende tijd de beslissing neemt, wordt de beslissing achterstallig.</span><span class="sxs-lookup"><span data-stu-id="92ea3-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="92ea3-265">Een beslissing die achterstallig is, wordt geëscaleerd op basis van de opties die u selecteert in het gebied **Escalatie** van deze pagina.</span><span class="sxs-lookup"><span data-stu-id="92ea3-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="92ea3-266">Aangeven wat moet gebeuren wanneer een beslissing achterstallig is</span><span class="sxs-lookup"><span data-stu-id="92ea3-266">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="92ea3-267">Als een gebruiker niet binnen de toegekende tijd de beslissing neemt, wordt de beslissing achterstallig.</span><span class="sxs-lookup"><span data-stu-id="92ea3-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="92ea3-268">Een achterstallige beslissing kan worden geëscaleerd of automatisch aan een andere gebruiker worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="92ea3-269">Voer de volgende stappen uit om de beslissing te escaleren als deze achterstallig is.</span><span class="sxs-lookup"><span data-stu-id="92ea3-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="92ea3-270">Klik in het linkerdeelvenster op **Escalatie**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="92ea3-271">Vink het selectievakje **Escalatiepad gebruiken** aan om een escalatiepad te maken.</span><span class="sxs-lookup"><span data-stu-id="92ea3-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="92ea3-272">Het systeem wijst de beslissing automatisch toe aan de gebruikers die in het escalatiepad zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="92ea3-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="92ea3-273">De volgende tabel kan bijvoorbeeld een escalatiepad voorstellen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-273">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="92ea3-274">Reeks</span><span class="sxs-lookup"><span data-stu-id="92ea3-274">Sequence</span></span> | <span data-ttu-id="92ea3-275">Escalatiepad</span><span class="sxs-lookup"><span data-stu-id="92ea3-275">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="92ea3-276">1</span><span class="sxs-lookup"><span data-stu-id="92ea3-276">1</span></span>        | <span data-ttu-id="92ea3-277">Toewijzen aan: Diana</span><span class="sxs-lookup"><span data-stu-id="92ea3-277">Assign to: Donna</span></span>           |
    | <span data-ttu-id="92ea3-278">2</span><span class="sxs-lookup"><span data-stu-id="92ea3-278">2</span></span>        | <span data-ttu-id="92ea3-279">Toewijzen aan: Erica</span><span class="sxs-lookup"><span data-stu-id="92ea3-279">Assign to: Erin</span></span>            |
    | <span data-ttu-id="92ea3-280">3</span><span class="sxs-lookup"><span data-stu-id="92ea3-280">3</span></span>        | <span data-ttu-id="92ea3-281">Laatste actie: \[Keuze 1\]</span><span class="sxs-lookup"><span data-stu-id="92ea3-281">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="92ea3-282">In dit voorbeeld wordt de achterstallige beslissing door het systeem automatisch toegewezen aan Diana.</span><span class="sxs-lookup"><span data-stu-id="92ea3-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="92ea3-283">Als Diana niet tijdig de beslissing neemt, wordt de beslissing door het systeem toegewezen aan Erica.</span><span class="sxs-lookup"><span data-stu-id="92ea3-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="92ea3-284">Als Erica niet tijdig de beslissing neemt, selecteert het systeem **\[Keuze 1\]** als beslissing</span><span class="sxs-lookup"><span data-stu-id="92ea3-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="92ea3-285">Klik op **Escalatie toevoegen** om gebruikers toe te voegen aan het escalatiepad.</span><span class="sxs-lookup"><span data-stu-id="92ea3-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="92ea3-286">Selecteer een van de opties in de volgende tabel en volg de bijkomende stappen voor de betreffende optie voordat u naar stap 4 gaat.</span><span class="sxs-lookup"><span data-stu-id="92ea3-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="92ea3-287">Optie</span><span class="sxs-lookup"><span data-stu-id="92ea3-287">Option</span></span></th>
    <th><span data-ttu-id="92ea3-288">Gebruikers naar wie de beslissing wordt geëscaleerd</span><span class="sxs-lookup"><span data-stu-id="92ea3-288">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="92ea3-289">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="92ea3-289">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="92ea3-290">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="92ea3-290">Hierarchy</span></span></td>
    <td><span data-ttu-id="92ea3-291">Gebruikers in een specifieke organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="92ea3-291">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="92ea3-292">Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waarnaar u de beslissing wilt escaleren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="92ea3-293">Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="92ea3-294">Deze namen vertegenwoordigen gebruikers naar wie de beslissing kan worden geëscaleerd.</span><span class="sxs-lookup"><span data-stu-id="92ea3-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="92ea3-295">Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:</span><span class="sxs-lookup"><span data-stu-id="92ea3-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="92ea3-296">Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="92ea3-297">Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven.</span><span class="sxs-lookup"><span data-stu-id="92ea3-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="92ea3-298">Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="92ea3-299">Geeft op het tabblad <strong>Hiërarchieopties</strong> op naar welke gebruikers in het bereik de beslissing moet worden geëscaleerd:</span><span class="sxs-lookup"><span data-stu-id="92ea3-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="92ea3-300"><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de beslissing wordt geëscaleerd naar alle gebruikers in het bereik.</span><span class="sxs-lookup"><span data-stu-id="92ea3-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="92ea3-301"><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de beslissing wordt alleen geëscaleerd naar de laatste gebruiker in het bereik.</span><span class="sxs-lookup"><span data-stu-id="92ea3-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="92ea3-302"><strong>Gebruikers met de volgende status uitsluiten</strong>: de beslissing wordt niet geëscaleerd naar een gebruiker in het bereik die aan een specifieke voorwaarde voldoet.</span><span class="sxs-lookup"><span data-stu-id="92ea3-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="92ea3-303">Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</span><span class="sxs-lookup"><span data-stu-id="92ea3-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="92ea3-304">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="92ea3-304">Workflow user</span></span></td>
    <td><span data-ttu-id="92ea3-305">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="92ea3-305">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="92ea3-306">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="92ea3-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="92ea3-307">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="92ea3-307">User</span></span></td>
    <td><span data-ttu-id="92ea3-308">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="92ea3-308">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="92ea3-309">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="92ea3-310">De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="92ea3-310">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="92ea3-311">Selecteer de gebruikers naar wie u de beslissing wilt escaleren en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="92ea3-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="92ea3-312">Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="92ea3-313">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="92ea3-313">Select one of the following options:</span></span>

    - <span data-ttu-id="92ea3-314">**Uren**: voer het aantal uren in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="92ea3-315">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="92ea3-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="92ea3-316">**Dagen**: voer het aantal dagen in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="92ea3-317">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="92ea3-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="92ea3-318">**Weken**: voer het aantal weken in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="92ea3-319">**Maanden**: selecteer de dag en week waarop de gebruiker de beslissing uiterlijk moet hebben genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="92ea3-320">U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van de maand.</span><span class="sxs-lookup"><span data-stu-id="92ea3-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="92ea3-321">**Jaren**: selecteer de dag, week en maand waarop de gebruiker de beslissing uiterlijk moet hebben genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="92ea3-322">U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van december.</span><span class="sxs-lookup"><span data-stu-id="92ea3-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="92ea3-323">Herhaal stappen 3 tot en met 4 voor elke gebruiker die u aan het escalatiepad wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="92ea3-324">U kunt de volgorde van de gebruikers wijzigen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="92ea3-325">Als de gebruikers in het escalatiepad niet binnen de gestelde tijd de beslissing nemen, reageert het systeem automatisch op de beslissing.</span><span class="sxs-lookup"><span data-stu-id="92ea3-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="92ea3-326">Om de optie in te stellen die het systeem selecteert, selecteert u de rij **Actie** en klikt u op het tabblad **Actie beëindigen**. Selecteer hier een optie.</span><span class="sxs-lookup"><span data-stu-id="92ea3-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="92ea3-327">Een tijdslimiet instellen</span><span class="sxs-lookup"><span data-stu-id="92ea3-327">Set a time limit</span></span>

<span data-ttu-id="92ea3-328">Volg deze stappen als de beslissing binnen een opgegeven tijd moet worden genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-328">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="92ea3-329">De hier geselecteerde opties hebben voorrang op de opties die u in de gebieden **Toewijzing** en **Escalatie** van de pagina hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="92ea3-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="92ea3-330">Klik in het linkerdeelvenster op **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="92ea3-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="92ea3-331">Schakel het selectievakje **Een tijdslimiet instellen voor het workflowelement** in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="92ea3-332">Geef in het veld **Duur** aan wanneer de beslissing moet genomen zijn.</span><span class="sxs-lookup"><span data-stu-id="92ea3-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="92ea3-333">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="92ea3-333">Select one of the following options:</span></span>

    - <span data-ttu-id="92ea3-334">**Uren**: voer het aantal uren in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="92ea3-335">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="92ea3-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="92ea3-336">**Dagen**: voer het aantal dagen in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="92ea3-337">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="92ea3-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="92ea3-338">**Weken**: voer het aantal weken in.</span><span class="sxs-lookup"><span data-stu-id="92ea3-338">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="92ea3-339">**Maanden**: selecteer de dag en week waarop de beslissing uiterlijk moet zijn genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="92ea3-340">U kunt bijvoorbeeld aangeven dat de beslissing uiterlijk op de vrijdag in de derde week van de maand moet zijn genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="92ea3-341">**Jaren**: selecteer de dag, week en maand waarop de beslissing uiterlijk moet zijn genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="92ea3-342">U kunt bijvoorbeeld aangeven dat de beslissing uiterlijk op de vrijdag in de derde week van december moet zijn genomen.</span><span class="sxs-lookup"><span data-stu-id="92ea3-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="92ea3-343">Als de tijdslimiet is overschreden, dan neemt het systeem automatisch de beslissing.</span><span class="sxs-lookup"><span data-stu-id="92ea3-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="92ea3-344">Selecteer in de lijst **Actie** de optie die het systeem moet selecteren.</span><span class="sxs-lookup"><span data-stu-id="92ea3-344">In the **Action** list, select the option that the system should select.</span></span>