---
title: Goedkeuringsprocessen configureren in een workflow
description: Met behulp van de volgende procedure kunt u de eigenschappen van het goedkeuringsproces configureren.
author: sericks007
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f58e227542b1e5ca1235748d14e71bddac826ee
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983759"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="f7e46-103">Goedkeuringsprocessen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="f7e46-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7e46-104">Met behulp van de volgende procedure kunt u de eigenschappen van het goedkeuringsproces configureren.</span><span class="sxs-lookup"><span data-stu-id="f7e46-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="f7e46-105">Als u een goedkeuringsproces wilt configureren, klikt u in de workfloweditor met de rechtermuisknop op het goedkeuringselement en klikt u vervolgens op **Eigenschappen** om het formulier **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="f7e46-106">Het goedkeuringsproces een naam geven</span><span class="sxs-lookup"><span data-stu-id="f7e46-106">Name the approval process</span></span>

<span data-ttu-id="f7e46-107">Voer deze stappen uit om een naam op te geven voor de goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="f7e46-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="f7e46-108">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f7e46-109">Geef in het veld **Naam** een unieke naam op voor het goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="f7e46-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="f7e46-110">Opgeven wanneer het systeem automatisch op het document reageert</span><span class="sxs-lookup"><span data-stu-id="f7e46-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="f7e46-111">U kunt het systeem zo configureren dat er automatisch wordt gereageerd het document als aan specifieke voorwaarden is voldaan.</span><span class="sxs-lookup"><span data-stu-id="f7e46-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="f7e46-112">Het systeem kan bijvoorbeeld onkostennota´s goedkeuren met een totaalbedrag dat lager is dan 100 EUR.</span><span class="sxs-lookup"><span data-stu-id="f7e46-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="f7e46-113">Voer de volgende stappen uit om op te geven wanneer het systeem op het document reageert.</span><span class="sxs-lookup"><span data-stu-id="f7e46-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="f7e46-114">Klik in het linkerdeelvenster op **Automatische acties**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="f7e46-115">Vink het selectievakje **Automatische acties inschakelen** aan.</span><span class="sxs-lookup"><span data-stu-id="f7e46-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="f7e46-116">Klik op **Voorwaarde toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="f7e46-117">Een voorwaarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="f7e46-117">Enter a condition.</span></span>
5. <span data-ttu-id="f7e46-118">Geef desgewenst aanvullende voorwaarden op.</span><span class="sxs-lookup"><span data-stu-id="f7e46-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="f7e46-119">Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="f7e46-120">Klik op **Testen** om het formulier **Workflowvoorwaarde testen** te openen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="f7e46-121">Selecteer een record in het gebied **Voorwaarde valideren** van het formulier.</span><span class="sxs-lookup"><span data-stu-id="f7e46-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="f7e46-122">Klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-122">Click **Test**.</span></span> <span data-ttu-id="f7e46-123">Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="f7e46-124">Klik op **OK** of **Annuleren** om terug te gaan naar het formulier **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="f7e46-125">Selecteer in de lijst **Actie AutoAanvullen** de actie die het systeem op het document moet uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="f7e46-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="f7e46-126">Opgeven wanneer meldingen worden verzonden</span><span class="sxs-lookup"><span data-stu-id="f7e46-126">Specify when notifications are sent</span></span>

<span data-ttu-id="f7e46-127">U kunt meldingen naar gebruikers verzenden wanneer een document is goedgekeurd, afgewezen, gedelegeerd of geëscaleerd, of wanneer een wijziging is aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="f7e46-128">Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="f7e46-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="f7e46-129">Klik in het linkerdeelvenster op **Meldingen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="f7e46-130">Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:</span><span class="sxs-lookup"><span data-stu-id="f7e46-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="f7e46-131">**Delegeren**: wanneer een document aan een andere gebruiker ter goedkeuring is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="f7e46-132">**Escaleren**: wanneer de toegewezen gebruiker niet binnen de toegekend tijd op het document heeft gereageerd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="f7e46-133">**Goedkeuren**: wanneer een document is goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="f7e46-134">**Afwijzen**: wanneer een document is afgewezen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="f7e46-135">**Wijziging aanvraag**: wanneer de toegewezen gebruiker een wijziging van een ingediend document heeft aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="f7e46-136">Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="f7e46-137">Klik op het tabblad **Meldingstekst**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="f7e46-138">Geef in het tekstvak de tekst voor de melding op.</span><span class="sxs-lookup"><span data-stu-id="f7e46-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="f7e46-139">Om de tekst te personaliseren, kunt u ook tijdelijke aanduidingen invoegen die worden vervangen door de gewenste gegevens wanneer de instructies worden weergegeven voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="f7e46-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="f7e46-140">Volg deze stappen om een tijdelijke aanduiding in te voegen:</span><span class="sxs-lookup"><span data-stu-id="f7e46-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="f7e46-141">Klik in het tekstvak op de locatie waar de tijdelijke aanduiding moet verschijnen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f7e46-142">Klik op **Tijdelijke aanduiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f7e46-143">Selecteer in de lijst die wordt weergegeven de tijdelijke aanduiding die u wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f7e46-144">Klik op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-144">Click **Insert**.</span></span>

7. <span data-ttu-id="f7e46-145">Klik op **Vertalingen** om vertalingen van de melding toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="f7e46-146">Selecteer de volgende stappen in het formulier dat wordt weergegeven:</span><span class="sxs-lookup"><span data-stu-id="f7e46-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="f7e46-147">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-147">Click **Add**.</span></span>
    2. <span data-ttu-id="f7e46-148">Selecteer in de lijst die wordt weergegeven de taal waarin u de tekst wilt invoeren.</span><span class="sxs-lookup"><span data-stu-id="f7e46-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="f7e46-149">Geef in het vak **Vertaalde tekst** de tekst op.</span><span class="sxs-lookup"><span data-stu-id="f7e46-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="f7e46-150">Voeg tijdelijke aanduidingen in om de tekst te personaliseren.</span><span class="sxs-lookup"><span data-stu-id="f7e46-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="f7e46-151">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-151">Click **Close**.</span></span>

8. <span data-ttu-id="f7e46-152">Klik op het tabblad **Ontvanger**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="f7e46-153">Vermeld naar wie de meldingen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="f7e46-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="f7e46-154">Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de optie voordat u naar stap 10 gaat.</span><span class="sxs-lookup"><span data-stu-id="f7e46-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f7e46-155">Optie</span><span class="sxs-lookup"><span data-stu-id="f7e46-155">Option</span></span></th>
    <th><span data-ttu-id="f7e46-156">Ontvangers van meldingen</span><span class="sxs-lookup"><span data-stu-id="f7e46-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="f7e46-157">Bijkomende stappen</span><span class="sxs-lookup"><span data-stu-id="f7e46-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f7e46-158"><strong>Deelnemer</strong></span><span class="sxs-lookup"><span data-stu-id="f7e46-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="f7e46-159">Gebruikers die aan een specifieke groep of rol zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="f7e46-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f7e46-160">Selecteer het tabblad <strong>Deelnemer</strong> en klik op het tabblad <strong>Rolgebaseerd</strong>.</span><span class="sxs-lookup"><span data-stu-id="f7e46-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="f7e46-161">Selecteer in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="f7e46-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="f7e46-162">Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="f7e46-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f7e46-163"><strong>Werkstroomgebruiker</strong></span><span class="sxs-lookup"><span data-stu-id="f7e46-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="f7e46-164">Gebruikers die aan de huidige workflow deelnemen</span><span class="sxs-lookup"><span data-stu-id="f7e46-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f7e46-165">Selecteer <strong>Workflowgebruiker</strong> en klik op het tabblad <strong>Workflowgebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="f7e46-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="f7e46-166">Selecteer in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</span><span class="sxs-lookup"><span data-stu-id="f7e46-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f7e46-167"><strong>Gebruiker</strong></span><span class="sxs-lookup"><span data-stu-id="f7e46-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="f7e46-168">Specifieke gebruikers</span><span class="sxs-lookup"><span data-stu-id="f7e46-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f7e46-169">Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</span><span class="sxs-lookup"><span data-stu-id="f7e46-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f7e46-170">Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</span><span class="sxs-lookup"><span data-stu-id="f7e46-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="f7e46-171">Herhaal stappen 3 tot en met 9 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="f7e46-172">Een definitieve fiatteur opgeven</span><span class="sxs-lookup"><span data-stu-id="f7e46-172">Specify a final approver</span></span>

<span data-ttu-id="f7e46-173">U kunt een laatste fiatteur aanwijzen voor scenario's waarbij de fiatteur de persoon is die het document ter goedkeuring heeft ingediend en de optie 'goedkeuring door indiener toestaan' wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f7e46-173">You can designate a final approver for scenarios where the approver is the person who submitted the document for approval and the "disallow approval by submitter" is being used.</span></span> <span data-ttu-id="f7e46-174">Volg deze stappen om een definitieve fiatteur op te geven.</span><span class="sxs-lookup"><span data-stu-id="f7e46-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="f7e46-175">Als u een goedkeuringsproces wilt configureren, klikt u in de workfloweditor met de rechtermuisknop op het goedkeuringselement en selecteert u **Eigenschappen** om het formulier **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-175">In the workflow editor, right-click the approval element, and then select **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="f7e46-176">Klik in het linkerdeelvenster op **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-176">In the left pane, click **Advanced settings**.</span></span>
3. <span data-ttu-id="f7e46-177">Schakel het selectievakje **Definitieve fiatteur gebruiken** in.</span><span class="sxs-lookup"><span data-stu-id="f7e46-177">Select the **Use final approver** check box.</span></span>
4. <span data-ttu-id="f7e46-178">Selecteer een gebruiker die de laatste fiatteur is in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f7e46-178">In the list, select a user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="f7e46-179">Een tijdslimiet instellen</span><span class="sxs-lookup"><span data-stu-id="f7e46-179">Set a time limit</span></span>

<span data-ttu-id="f7e46-180">Volg deze stappen als het goedkeuringsproces binnen een opgegeven tijd moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="f7e46-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="f7e46-181">De opties die u in deze stappen selecteert, overschrijven de opties die u in de gebieden **Toewijzing** en **Escalatie** van elke goedkeuringsstap hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="f7e46-182">Klik in het linkerdeelvenster op **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="f7e46-183">Schakel het selectievakje **Een tijdslimiet instellen voor het** **workflowelement** in.</span><span class="sxs-lookup"><span data-stu-id="f7e46-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="f7e46-184">Geef in het veld **Duur** aan wanneer het goedkeuringsproces moet voltooid zijn.</span><span class="sxs-lookup"><span data-stu-id="f7e46-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="f7e46-185">Een van de volgende opties selecteren:</span><span class="sxs-lookup"><span data-stu-id="f7e46-185">Select one of the following options:</span></span>

    - <span data-ttu-id="f7e46-186">**Uren**: het aantal uren invoeren waarin het goedkeuringsproces moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="f7e46-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="f7e46-187">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="f7e46-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f7e46-188">**Dagen**: het aantal dagen invoeren waarin het goedkeuringsproces moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="f7e46-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="f7e46-189">Selecteer vervolgens de kalender die uw organisatie gebruikt en voer informatie in over de werkweek van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="f7e46-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f7e46-190">**Weken**: het aantal weken invoeren waarin het goedkeuringsproces moet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="f7e46-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="f7e46-191">**Maanden**: de dag en week selecteren wanneer het goedkeuringsproces moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="f7e46-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="f7e46-192">U kunt bijvoorbeeld aangeven dat het goedkeuringsproces vóór vrijdag in de derde week van de maand moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="f7e46-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="f7e46-193">**Jaren**: de dag, week en maand selecteren wanneer het goedkeuringsproces moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="f7e46-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="f7e46-194">U kunt bijvoorbeeld aangeven dat het goedkeuringsproces vóór vrijdag in de derde week van december moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="f7e46-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="f7e46-195">Als de tijdslimiet is overschreden, reageert het systeem automatisch op het document.</span><span class="sxs-lookup"><span data-stu-id="f7e46-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="f7e46-196">Selecteer de gewenste actie in de lijst **Actie**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="f7e46-197">Geef op welke acties voor de gebruiker beschikbaar zijn</span><span class="sxs-lookup"><span data-stu-id="f7e46-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="f7e46-198">Wanneer een document voor goedkeuring is toegewezen aan een gebruiker, moet de gebruiker reageren op het document.</span><span class="sxs-lookup"><span data-stu-id="f7e46-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="f7e46-199">Volg deze stappen om aan te geven welke acties de gebruiker kan ondernemen op het ingediende document.</span><span class="sxs-lookup"><span data-stu-id="f7e46-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="f7e46-200">Klik in het linkerdeelvenster op **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="f7e46-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="f7e46-201">Vink het selectievakje **Goedkeuren** aan als de gebruiker het document kan goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="f7e46-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="f7e46-202">Vink het selectievakje **Afwijzen** aan als de gebruiker het document kan afwijzen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="f7e46-203">Schakel het selectievakje **Wijziging aanvraag** in als u wilt dat de gebruiker wijzigingen in het document kan aanvragen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="f7e46-204">Schakel het selectievakje **Delegeren** in als de gebruiker het document ter goedkeuring aan een andere gebruiker kan toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="f7e46-205">Het selectievakje **Acties van de werklijst in Enterprise Portal activeren** is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="f7e46-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="f7e46-206"> De goedkeuringsstappen configureren</span><span class="sxs-lookup"><span data-stu-id="f7e46-206">Configure the approval steps</span></span>

<span data-ttu-id="f7e46-207">Een goedkeuringsproces bestaat uit goedkeuringsstappen.</span><span class="sxs-lookup"><span data-stu-id="f7e46-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="f7e46-208">Voer de volgende procedures uit om stappen aan het goedkeuringsproces toe te voegen en de stappen te configureren.</span><span class="sxs-lookup"><span data-stu-id="f7e46-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="f7e46-209">Dubbelklik in de workfloweditor op het goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="f7e46-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="f7e46-210">De workfloweditor geeft de stappen van het goedkeuringsproces weer.</span><span class="sxs-lookup"><span data-stu-id="f7e46-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="f7e46-211">Sleep de goedkeuringsstappen die u wilt toevoegen van het gebied **Workflowelementen** naar het tekenpapier.</span><span class="sxs-lookup"><span data-stu-id="f7e46-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="f7e46-212">Zie [Goedkeuringsstappen configureren in een workflow](configure-approval-step-workflow.md) als u een goedkeuringsstap wilt configureren.</span><span class="sxs-lookup"><span data-stu-id="f7e46-212">To configure an approval step, see [Configure approval steps in a workflow](configure-approval-step-workflow.md).</span></span>
