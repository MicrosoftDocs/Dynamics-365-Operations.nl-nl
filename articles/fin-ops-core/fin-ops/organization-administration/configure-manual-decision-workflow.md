---
title: Handmatige beslissingen configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige beslissing configureert.
author: ChrisGarty
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d351facbce02355ddb4bdf91d43d9df561e4f3b5
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798847"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="a3244-103">Handmatige beslissingen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="a3244-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3244-104">In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een handmatige beslissing configureert.</span><span class="sxs-lookup"><span data-stu-id="a3244-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="a3244-105">Om een handmatige beslissing te configureren, klikt u in de workfloweditor met de rechtermuisknop op de handmatige beslissing en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="a3244-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="a3244-106">Vervolgens kunt u met de volgende procedures de eigenschappen van de handmatige beslissing configureren.</span><span class="sxs-lookup"><span data-stu-id="a3244-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="a3244-107">Naam van de beslissing</span><span class="sxs-lookup"><span data-stu-id="a3244-107">Name the decision</span></span>

<span data-ttu-id="a3244-108">Voer deze stappen uit om een naam op te geven voor de handmatige beslissing.</span><span class="sxs-lookup"><span data-stu-id="a3244-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="a3244-109">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a3244-110">Voer in het veld **Naam** een unieke naam voor de handmatige beslissing in.</span><span class="sxs-lookup"><span data-stu-id="a3244-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="a3244-111">Een onderwerpregel en instructies invoeren</span><span class="sxs-lookup"><span data-stu-id="a3244-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="a3244-112">U moet een onderwerpregel en instructies invoeren voor de gebruikers die aan de handmatige beslissing zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a3244-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="a3244-113">Als u bijvoorbeeld een beslissing voor opdrachten tot inkoop configureert, ziet de gebruiker die aan de beslissing is toegewezen de onderwerpregel en instructies op de pagina **Opdrachten tot inkoop**.</span><span class="sxs-lookup"><span data-stu-id="a3244-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="a3244-114">De onderwerpregel verschijnt in de berichtenbalk van de pagina.</span><span class="sxs-lookup"><span data-stu-id="a3244-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="a3244-115">De gebruiker kan vervolgens klikken op het pictogram op de berichtenbalk om de instructies weer te geven.</span><span class="sxs-lookup"><span data-stu-id="a3244-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="a3244-116">Voer deze stappen uit om een onderwerpregel en instructies in te voeren.</span><span class="sxs-lookup"><span data-stu-id="a3244-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="a3244-117">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a3244-118">Op het tabblad **Instructies** voert u in het veld **Onderwerp werkitem** de onderwerpregel in.</span><span class="sxs-lookup"><span data-stu-id="a3244-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="a3244-119">Als u de onderwerpregel wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="a3244-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="a3244-120">Wanneer de onderwerpregel aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="a3244-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="a3244-121">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="a3244-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="a3244-122">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="a3244-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a3244-123">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a3244-124">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="a3244-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a3244-125">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-125">Click **Insert**.</span></span>

4. <span data-ttu-id="a3244-126">Voer de onderstaande stappen uit om vertalingen van de onderwerpregel toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="a3244-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="a3244-127">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="a3244-128">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a3244-129">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="a3244-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a3244-130">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="a3244-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a3244-131">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 3.</span><span class="sxs-lookup"><span data-stu-id="a3244-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="a3244-132">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="a3244-132">Click **Close**.</span></span>

5. <span data-ttu-id="a3244-133">Voer in het veld **Instructies werkitem** de instructies in.</span><span class="sxs-lookup"><span data-stu-id="a3244-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="a3244-134">Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="a3244-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="a3244-135">Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="a3244-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="a3244-136">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="a3244-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="a3244-137">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="a3244-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a3244-138">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a3244-139">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="a3244-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a3244-140">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-140">Click **Insert**.</span></span>

7. <span data-ttu-id="a3244-141">Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="a3244-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="a3244-142">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="a3244-143">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a3244-144">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="a3244-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a3244-145">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="a3244-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a3244-146">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 6.</span><span class="sxs-lookup"><span data-stu-id="a3244-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="a3244-147">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="a3244-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="a3244-148">De mogelijke resultaten van een beslissing opgeven</span><span class="sxs-lookup"><span data-stu-id="a3244-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="a3244-149">Wanneer een document aan een besluitvormer is toewezen, krijgt de besluitvormer doorgaans een vraag voorgelegd.</span><span class="sxs-lookup"><span data-stu-id="a3244-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="a3244-150">Het antwoord op deze vraag is doorgaans **Ja** of **Nee**, of **Waar** of **Onwaar**.</span><span class="sxs-lookup"><span data-stu-id="a3244-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="a3244-151">Voer de volgende stappen uit om de mogelijk resultaten op te geven van de handmatige beslissing.</span><span class="sxs-lookup"><span data-stu-id="a3244-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="a3244-152">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a3244-153">Geef op het tabblad **Resultaten** in het veld **Resultaat 1** de naam van het resultaat of de optie op.</span><span class="sxs-lookup"><span data-stu-id="a3244-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="a3244-154">Voer de onderstaande stappen uit om vertalingen van het resultaat toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="a3244-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="a3244-155">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="a3244-156">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a3244-157">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="a3244-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a3244-158">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="a3244-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a3244-159">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="a3244-159">Click **Close**.</span></span>

4. <span data-ttu-id="a3244-160">Geef in het veld **Uitkomst 2** de naam van het resultaat of de optie op.</span><span class="sxs-lookup"><span data-stu-id="a3244-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="a3244-161">Voer de onderstaande stappen uit om vertalingen van het resultaat toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="a3244-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="a3244-162">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="a3244-163">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a3244-164">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="a3244-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a3244-165">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="a3244-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a3244-166">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="a3244-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="a3244-167">Opgeven wanneer meldingen worden verzonden</span><span class="sxs-lookup"><span data-stu-id="a3244-167">Specify when notifications are sent</span></span>

<span data-ttu-id="a3244-168">U kunt meldingen naar gebruikers verzenden wanneer een beslissing is genomen, gedelegeerd, geëscaleerd.</span><span class="sxs-lookup"><span data-stu-id="a3244-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="a3244-169">Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="a3244-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="a3244-170">Klik in het linkerdeelvenster op **Meldingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="a3244-171">Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:</span><span class="sxs-lookup"><span data-stu-id="a3244-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="a3244-172">**\[Keuze 1\]** – de toegewezen gebruiker heeft **\[Keuze 1\]** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a3244-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="a3244-173">**\[Keuze 2\]** – de toegewezen gebruiker heeft **\[Keuze 2\]** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a3244-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="a3244-174">**Delegeren**: de toegewezen gebruiker heeft de beslissing aan een andere gebruiker toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a3244-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="a3244-175">**Escaleren**: de toegewezen gebruiker heeft de beslssing niet niet binnen de toegekende tijd genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="a3244-176">Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a3244-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="a3244-177">Geef op het tabblad **Meldingstekst** de tekst van de melding op.</span><span class="sxs-lookup"><span data-stu-id="a3244-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="a3244-178">Als u de melding wilt personaliseren, kunt u tijdelijke aanduidingen invoegen.</span><span class="sxs-lookup"><span data-stu-id="a3244-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="a3244-179">Wanneer de melding aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="a3244-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="a3244-180">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="a3244-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="a3244-181">Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.</span><span class="sxs-lookup"><span data-stu-id="a3244-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a3244-182">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a3244-183">Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="a3244-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a3244-184">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-184">Click **Insert**.</span></span>

6. <span data-ttu-id="a3244-185">Voer de onderstaande stappen uit om vertalingen van de melding toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="a3244-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="a3244-186">Klik op **Vertalingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="a3244-187">Klik in de pagina die wordt geopend op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a3244-188">Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="a3244-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="a3244-189">Voer in het veld **Vertaalde tekst** de gewenste tekst in.</span><span class="sxs-lookup"><span data-stu-id="a3244-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a3244-190">Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 5.</span><span class="sxs-lookup"><span data-stu-id="a3244-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="a3244-191">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="a3244-191">Click **Close**.</span></span>

7. <span data-ttu-id="a3244-192">Geef op het tabblad **Ontvanger** op aan wie de meldingen moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="a3244-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="a3244-193">Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de betreffende optie voordat u naar stap 8 gaat.</span><span class="sxs-lookup"><span data-stu-id="a3244-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a3244-194">Optie</span><span class="sxs-lookup"><span data-stu-id="a3244-194">Option</span></span></th>
    <th><span data-ttu-id="a3244-195">Ontvangers van meldingen</span><span class="sxs-lookup"><span data-stu-id="a3244-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="a3244-196">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="a3244-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a3244-197">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="a3244-197">Participant</span></span></td>
    <td><span data-ttu-id="a3244-198">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="a3244-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3244-199">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt laten verzenden.</span><span class="sxs-lookup"><span data-stu-id="a3244-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="a3244-200">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="a3244-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3244-201">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="a3244-201">Workflow user</span></span></td>
    <td><span data-ttu-id="a3244-202">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="a3244-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="a3244-203">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="a3244-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3244-204">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="a3244-204">User</span></span></td>
    <td><span data-ttu-id="a3244-205">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="a3244-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3244-206">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3244-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="a3244-207">De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="a3244-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="a3244-208">Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3244-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="a3244-209">Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a3244-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="a3244-210">Een beslissing toewijzen</span><span class="sxs-lookup"><span data-stu-id="a3244-210">Assign a decision</span></span>

<span data-ttu-id="a3244-211">Voer de volgende stappen uit om op te geven aan wie de handmatige beslissing moet worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a3244-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="a3244-212">Klik in het linkerdeelvensters op het pictogram **Toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="a3244-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="a3244-213">Selecteer in het tabblad **Toewijzingstype** een van de opties in de volgende tabel en voer de bijkomende stappen uit voor de optie voordat u naar stap 3 gaat.</span><span class="sxs-lookup"><span data-stu-id="a3244-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a3244-214">Optie</span><span class="sxs-lookup"><span data-stu-id="a3244-214">Option</span></span></th>
    <th><span data-ttu-id="a3244-215">Gebruikers aan wie de beslissing is toegewezen</span><span class="sxs-lookup"><span data-stu-id="a3244-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="a3244-216">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="a3244-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a3244-217">Deelnemer</span><span class="sxs-lookup"><span data-stu-id="a3244-217">Participant</span></span></td>
    <td><span data-ttu-id="a3244-218">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="a3244-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3244-219">Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waaraan u de beslissing wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="a3244-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="a3244-220">Selecteer in de lijst <strong>Deelnemer</strong> het type groep of rol waaraan u de beslissing wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="a3244-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3244-221">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="a3244-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="a3244-222">Gebruikers in een specifieke organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="a3244-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3244-223">Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waaraan u de beslissing wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="a3244-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="a3244-224">Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen.</span><span class="sxs-lookup"><span data-stu-id="a3244-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="a3244-225">Deze namen stellen gebruikers voor waaraan de beslissing kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a3244-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="a3244-226">Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:</span><span class="sxs-lookup"><span data-stu-id="a3244-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="a3244-227">Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3244-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="a3244-228">Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven.</span><span class="sxs-lookup"><span data-stu-id="a3244-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="a3244-229">Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</span><span class="sxs-lookup"><span data-stu-id="a3244-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="a3244-230">Geeft op het tabblad <strong>Hiërarchieopties</strong> op aan welke gebruikers in het bereik de beslissing moet worden toegewezen:</span><span class="sxs-lookup"><span data-stu-id="a3244-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="a3244-231"><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de beslissing wordt toegewezen aan alle gebruikers in het bereik.</span><span class="sxs-lookup"><span data-stu-id="a3244-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="a3244-232"><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de beslissing wordt alleen aan de laatste gebruiker in het bereik toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a3244-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="a3244-233"><strong>Gebruikers met de volgende status uitsluiten</strong>: de beslissing wordt niet toegewezen aan een gebruiker in het bereik die aan een specifieke voorwaarde voldoet.</span><span class="sxs-lookup"><span data-stu-id="a3244-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="a3244-234">Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</span><span class="sxs-lookup"><span data-stu-id="a3244-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3244-235">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="a3244-235">Workflow user</span></span></td>
    <td><span data-ttu-id="a3244-236">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="a3244-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="a3244-237">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="a3244-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3244-238">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="a3244-238">User</span></span></td>
    <td><span data-ttu-id="a3244-239">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="a3244-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3244-240">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3244-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="a3244-241">De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="a3244-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="a3244-242">Selecteer de gebruikers aan wie u de beslissing wilt toewijzen en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3244-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="a3244-243">Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="a3244-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="a3244-244">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="a3244-244">Select one of the following options:</span></span>

    - <span data-ttu-id="a3244-245">**Uren**: voer het aantal uren in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="a3244-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="a3244-246">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="a3244-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a3244-247">**Dagen**: voer het aantal dagen in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="a3244-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="a3244-248">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="a3244-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a3244-249">**Weken**: voer het aantal weken in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="a3244-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="a3244-250">**Maanden**: selecteer de dag en week waarop de gebruiker de beslissing uiterlijk moet hebben genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="a3244-251">U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van de maand.</span><span class="sxs-lookup"><span data-stu-id="a3244-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="a3244-252">**Jaren**: selecteer de dag, week en maand waarop de gebruiker de beslissing uiterlijk moet hebben genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="a3244-253">U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van december.</span><span class="sxs-lookup"><span data-stu-id="a3244-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="a3244-254">Als de gebruiker niet binnen de toegekende tijd de beslissing neemt, wordt de beslissing achterstallig.</span><span class="sxs-lookup"><span data-stu-id="a3244-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="a3244-255">Een beslissing die achterstallig is, wordt geëscaleerd op basis van de opties die u selecteert in het gebied **Escalatie** van deze pagina.</span><span class="sxs-lookup"><span data-stu-id="a3244-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="a3244-256">Aangeven wat moet gebeuren wanneer een beslissing achterstallig is</span><span class="sxs-lookup"><span data-stu-id="a3244-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="a3244-257">Als een gebruiker niet binnen de toegekende tijd de beslissing neemt, wordt de beslissing achterstallig.</span><span class="sxs-lookup"><span data-stu-id="a3244-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="a3244-258">Een achterstallige beslissing kan worden geëscaleerd of automatisch aan een andere gebruiker worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a3244-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="a3244-259">Voer de volgende stappen uit om de beslissing te escaleren als deze achterstallig is.</span><span class="sxs-lookup"><span data-stu-id="a3244-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="a3244-260">Klik in het linkerdeelvenster op **Escalatie**.</span><span class="sxs-lookup"><span data-stu-id="a3244-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="a3244-261">Vink het selectievakje **Escalatiepad gebruiken** aan om een escalatiepad te maken.</span><span class="sxs-lookup"><span data-stu-id="a3244-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="a3244-262">Het systeem wijst de beslissing automatisch toe aan de gebruikers die in het escalatiepad zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="a3244-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="a3244-263">De volgende tabel kan bijvoorbeeld een escalatiepad voorstellen.</span><span class="sxs-lookup"><span data-stu-id="a3244-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="a3244-264">Reeks</span><span class="sxs-lookup"><span data-stu-id="a3244-264">Sequence</span></span> | <span data-ttu-id="a3244-265">Escalatiepad</span><span class="sxs-lookup"><span data-stu-id="a3244-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="a3244-266">1</span><span class="sxs-lookup"><span data-stu-id="a3244-266">1</span></span>        | <span data-ttu-id="a3244-267">Toewijzen aan: Diana</span><span class="sxs-lookup"><span data-stu-id="a3244-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="a3244-268">2</span><span class="sxs-lookup"><span data-stu-id="a3244-268">2</span></span>        | <span data-ttu-id="a3244-269">Toewijzen aan: Erica</span><span class="sxs-lookup"><span data-stu-id="a3244-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="a3244-270">3</span><span class="sxs-lookup"><span data-stu-id="a3244-270">3</span></span>        | <span data-ttu-id="a3244-271">Laatste actie: \[Keuze 1\]</span><span class="sxs-lookup"><span data-stu-id="a3244-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="a3244-272">In dit voorbeeld wordt de achterstallige beslissing door het systeem automatisch toegewezen aan Diana.</span><span class="sxs-lookup"><span data-stu-id="a3244-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="a3244-273">Als Diana niet tijdig de beslissing neemt, wordt de beslissing door het systeem toegewezen aan Erica.</span><span class="sxs-lookup"><span data-stu-id="a3244-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="a3244-274">Als Erica niet tijdig de beslissing neemt, selecteert het systeem **\[Keuze 1\]** als beslissing</span><span class="sxs-lookup"><span data-stu-id="a3244-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="a3244-275">Klik op **Escalatie toevoegen** om gebruikers toe te voegen aan het escalatiepad.</span><span class="sxs-lookup"><span data-stu-id="a3244-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="a3244-276">Selecteer een van de opties in de volgende tabel en volg de bijkomende stappen voor de betreffende optie voordat u naar stap 4 gaat.</span><span class="sxs-lookup"><span data-stu-id="a3244-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a3244-277">Optie</span><span class="sxs-lookup"><span data-stu-id="a3244-277">Option</span></span></th>
    <th><span data-ttu-id="a3244-278">Gebruikers naar wie de beslissing wordt geëscaleerd</span><span class="sxs-lookup"><span data-stu-id="a3244-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="a3244-279">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="a3244-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a3244-280">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="a3244-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="a3244-281">Gebruikers in een specifieke organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="a3244-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3244-282">Selecteer op het tabblad <strong>Hiërarchieselectie</strong> de optie <strong>Hiërarchie</strong> en selecteer vervolgens in de lijst <strong>Type hiërarchie</strong> het type hiërarchie waarnaar u de beslissing wilt escaleren.</span><span class="sxs-lookup"><span data-stu-id="a3244-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="a3244-283">Het systeem moet een bereik van gebruikersnamen uit de hiërarchie ophalen.</span><span class="sxs-lookup"><span data-stu-id="a3244-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="a3244-284">Deze namen vertegenwoordigen gebruikers naar wie de beslissing kan worden geëscaleerd.</span><span class="sxs-lookup"><span data-stu-id="a3244-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="a3244-285">Volg deze stappen om het beginpunt en eindpunt van het bereik op te geven voor gebruikersnamen die het systeem ophaalt:</span><span class="sxs-lookup"><span data-stu-id="a3244-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="a3244-286">Geef het beginpunt op door een persoon te selecteren in de lijst <strong>Beginnen vanaf</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3244-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="a3244-287">Klik op <strong>Voorwaarde toevoegen</strong> om het eindpunt op te geven.</span><span class="sxs-lookup"><span data-stu-id="a3244-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="a3244-288">Geef vervolgens een voorwaarde op die bepaalt bij welk punt in de hiërarchie stopt met het ophalen van namen.</span><span class="sxs-lookup"><span data-stu-id="a3244-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="a3244-289">Geeft op het tabblad <strong>Hiërarchieopties</strong> op naar welke gebruikers in het bereik de beslissing moet worden geëscaleerd:</span><span class="sxs-lookup"><span data-stu-id="a3244-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="a3244-290"><strong>Aan alle opgehaalde gebruikers toewijzen</strong>: de beslissing wordt geëscaleerd naar alle gebruikers in het bereik.</span><span class="sxs-lookup"><span data-stu-id="a3244-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="a3244-291"><strong>Alleen aan laatst opgehaalde gebruiker toewijzen</strong>: de beslissing wordt alleen geëscaleerd naar de laatste gebruiker in het bereik.</span><span class="sxs-lookup"><span data-stu-id="a3244-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="a3244-292"><strong>Gebruikers met de volgende status uitsluiten</strong>: de beslissing wordt niet geëscaleerd naar een gebruiker in het bereik die aan een specifieke voorwaarde voldoet.</span><span class="sxs-lookup"><span data-stu-id="a3244-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="a3244-293">Klik op <strong>Voorwaarde toevoegen</strong> om de voorwaarde op te geven.</span><span class="sxs-lookup"><span data-stu-id="a3244-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3244-294">Werkstroomgebruiker</span><span class="sxs-lookup"><span data-stu-id="a3244-294">Workflow user</span></span></td>
    <td><span data-ttu-id="a3244-295">Gebruikers in de huidige workflow</span><span class="sxs-lookup"><span data-stu-id="a3244-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="a3244-296">Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="a3244-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3244-297">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="a3244-297">User</span></span></td>
    <td><span data-ttu-id="a3244-298">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="a3244-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3244-299">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3244-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="a3244-300">De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="a3244-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="a3244-301">Selecteer de gebruikers naar wie u de beslissing wilt escaleren en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3244-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="a3244-302">Geef op het tabblad **Tijdslimiet** in het veld **Duur** aan hoeveel tijd de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="a3244-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="a3244-303">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="a3244-303">Select one of the following options:</span></span>

    - <span data-ttu-id="a3244-304">**Uren**: voer het aantal uren in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="a3244-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="a3244-305">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="a3244-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a3244-306">**Dagen**: voer het aantal dagen in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="a3244-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="a3244-307">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="a3244-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a3244-308">**Weken**: voer het aantal weken in dat de gebruiker heeft om de beslissing te nemen.</span><span class="sxs-lookup"><span data-stu-id="a3244-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="a3244-309">**Maanden**: selecteer de dag en week waarop de gebruiker de beslissing uiterlijk moet hebben genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="a3244-310">U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van de maand.</span><span class="sxs-lookup"><span data-stu-id="a3244-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="a3244-311">**Jaren**: selecteer de dag, week en maand waarop de gebruiker de beslissing uiterlijk moet hebben genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="a3244-312">U kunt bijvoorbeeld aangeven dat de gebruiker de beslissing uiterlijk moet nemen op de vrijdag in de derde week van december.</span><span class="sxs-lookup"><span data-stu-id="a3244-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="a3244-313">Herhaal stappen 3 tot en met 4 voor elke gebruiker die u aan het escalatiepad wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a3244-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="a3244-314">U kunt de volgorde van de gebruikers wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a3244-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="a3244-315">Als de gebruikers in het escalatiepad niet binnen de gestelde tijd de beslissing nemen, reageert het systeem automatisch op de beslissing.</span><span class="sxs-lookup"><span data-stu-id="a3244-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="a3244-316">Om de optie in te stellen die het systeem selecteert, selecteert u de rij **Actie** en klikt u op het tabblad **Actie beëindigen**. Selecteer hier een optie.</span><span class="sxs-lookup"><span data-stu-id="a3244-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="a3244-317">Een tijdslimiet instellen</span><span class="sxs-lookup"><span data-stu-id="a3244-317">Set a time limit</span></span>

<span data-ttu-id="a3244-318">Volg deze stappen als de beslissing binnen een opgegeven tijd moet worden genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="a3244-319">De hier geselecteerde opties hebben voorrang op de opties die u in de gebieden **Toewijzing** en **Escalatie** van de pagina hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a3244-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="a3244-320">Klik in het linkerdeelvenster op **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="a3244-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="a3244-321">Schakel het selectievakje **Een tijdslimiet instellen voor het workflowelement** in.</span><span class="sxs-lookup"><span data-stu-id="a3244-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="a3244-322">Geef in het veld **Duur** aan wanneer de beslissing moet genomen zijn.</span><span class="sxs-lookup"><span data-stu-id="a3244-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="a3244-323">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="a3244-323">Select one of the following options:</span></span>

    - <span data-ttu-id="a3244-324">**Uren**: voer het aantal uren in.</span><span class="sxs-lookup"><span data-stu-id="a3244-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="a3244-325">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="a3244-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a3244-326">**Dagen**: voer het aantal dagen in.</span><span class="sxs-lookup"><span data-stu-id="a3244-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="a3244-327">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="a3244-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a3244-328">**Weken**: voer het aantal weken in.</span><span class="sxs-lookup"><span data-stu-id="a3244-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="a3244-329">**Maanden**: selecteer de dag en week waarop de beslissing uiterlijk moet zijn genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="a3244-330">U kunt bijvoorbeeld aangeven dat de beslissing uiterlijk op de vrijdag in de derde week van de maand moet zijn genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="a3244-331">**Jaren**: selecteer de dag, week en maand waarop de beslissing uiterlijk moet zijn genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="a3244-332">U kunt bijvoorbeeld aangeven dat de beslissing uiterlijk op de vrijdag in de derde week van december moet zijn genomen.</span><span class="sxs-lookup"><span data-stu-id="a3244-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="a3244-333">Als de tijdslimiet is overschreden, dan neemt het systeem automatisch de beslissing.</span><span class="sxs-lookup"><span data-stu-id="a3244-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="a3244-334">Selecteer in de lijst **Actie** de optie die het systeem moet selecteren.</span><span class="sxs-lookup"><span data-stu-id="a3244-334">In the **Action** list, select the option that the system should select.</span></span>
