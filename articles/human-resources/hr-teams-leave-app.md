---
title: Verlofaanvragen beheren in Teams
description: In dit onderwerp wordt beschreven hoe u verlof kunt aanvragen in de Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d24c257054578282f1a2eafa050094194a358aa0
ms.sourcegitcommit: 369639cd92e03fe792ed9d61a329d842aafa052f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4418066"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="c3a3b-103">Verlofaanvragen beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="c3a3b-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c3a3b-104">Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunt u snel verlof aanvragen en informatie over uw verlofsaldo bekijken rechtstreeks vanuit Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="c3a3b-105">U kunt werken met een bot om informatie aan te vragen en een verlofaanvraag te starten.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="c3a3b-106">Het tabblad **Verlof** bevat meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="c3a3b-107">U kunt mensen ook informatie sturen over uw geplande verlof in teams en chats buiten de app Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-107">You can also send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="c3a3b-108">De app installeren</span><span class="sxs-lookup"><span data-stu-id="c3a3b-108">Install the app</span></span>

<span data-ttu-id="c3a3b-109">De Human resources-app is te vinden in het Teams-archief.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="c3a3b-110">Selecteer de drie puntjes in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Drie puntjes in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="c3a3b-112">Zoek naar Dynamics 365 Human Resources en selecteer de tegel **Human resources**.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-tegel van verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="c3a3b-114">Selecteer de knop **Toevoegen** om de app te installeren.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-114">Select the **Add** button to install the app.</span></span>

   ![Installatie van verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="c3a3b-116">Als u niet automatisch wordt aangemeld bij de app, selecteert u het tabblad **Instellingen** om zich aan te melden.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Tabblad Instellingen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="c3a3b-118">Als er geen dialoogvenster voor aanmelding wordt weergegeven, controleert u de instellingen van uw browser om pop-ups toe te staan.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="c3a3b-119">Als u toegang hebt tot meer dan één exemplaar van Human resources, kunt u de omgeving selecteren waarmee u verbinding wilt maken op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="c3a3b-120">De app ondersteunt nu de beveiligingsrol Systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="c3a3b-121">De bot gebruiken</span><span class="sxs-lookup"><span data-stu-id="c3a3b-121">Use the bot</span></span>

<span data-ttu-id="c3a3b-122">Na de installatie van de app wordt er een welkomstbericht weergegeven, zodat u weet welke acties de bot namens u kan ondernemen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Welkomstbericht in verlof-app voor Human Resource Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="c3a3b-124">Bij het eerste contact met de bot moet u zich mogelijk aanmelden.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="c3a3b-125">Als er geen dialoogvenster voor aanmelding wordt weergegeven, controleert u de instellingen van uw browser om pop-ups toe te staan.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="c3a3b-126">U kunt de bot vragen om het volgende te doen:</span><span class="sxs-lookup"><span data-stu-id="c3a3b-126">You can ask the bot to:</span></span>

- <span data-ttu-id="c3a3b-127">Informatie over verlofsaldo weergeven voor elk verloftype waarvoor u zich hebt ingeschreven.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Saldo weergeven in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="c3a3b-129">Aanvullende informatie weergeven over een bepaald verloftype.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-129">Show additional details about a specific leave type.</span></span>

   ![Details weergeven in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="c3a3b-131">Een verlofaanvraag voor u starten.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-131">Start a leave request for you.</span></span>

   ![Verlof aanvragen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="c3a3b-133">Nadat u een verlofaanvraag hebt gestart, kunt u de dagen direct in de kaart aanpassen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Aanvraag bewerken in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="c3a3b-135">Wanneer u klaar bent met het invoeren van gegevens, selecteert u **Verzenden** om deze ter goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="c3a3b-136">U kunt ook **Opslaan als concept** selecteren als u later wilt terugkeren naar het concept.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-136">You can also select **Save as draft** to come back to it later.</span></span>

![Aanvraag indienen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="c3a3b-138">Uw verlof beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="c3a3b-138">Manage your leave in Teams</span></span>

<span data-ttu-id="c3a3b-139">Op het tabblad **Verlof** kunt u het volgende bekijken:</span><span class="sxs-lookup"><span data-stu-id="c3a3b-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="c3a3b-140">Saldo-informatie voor elk type verlof waarvoor u zich hebt ingeschreven</span><span class="sxs-lookup"><span data-stu-id="c3a3b-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="c3a3b-141">Aanstaande verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="c3a3b-141">Upcoming leave requests</span></span>

- <span data-ttu-id="c3a3b-142">Verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="c3a3b-142">Time-off requests</span></span>

- <span data-ttu-id="c3a3b-143">Conceptaanvragen voor verlof</span><span class="sxs-lookup"><span data-stu-id="c3a3b-143">Draft leave requests</span></span>

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="c3a3b-145">Een nieuwe aanvraag maken</span><span class="sxs-lookup"><span data-stu-id="c3a3b-145">Create a new request</span></span>

1. <span data-ttu-id="c3a3b-146">Selecteer **Nieuwe aanvraag** om een nieuwe verlofaanvraag te maken.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-146">To create a new leave request, select **New request**.</span></span>

   ![Nieuwe aanvraag in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="c3a3b-148">Voer de dag of dagen in die u wilt vrijnemen en selecteer vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Verlof toevoegen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="c3a3b-150">Voer een redencode in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="c3a3b-151">Voer ook eventuele opmerkingen in en voeg eventuele bijlagen toe.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="c3a3b-152">Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="c3a3b-153">U kunt ook **Opslaan als concept** opgeven als u later wilt terugkeren naar het concept.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="c3a3b-154">Conceptaanvragen beheren</span><span class="sxs-lookup"><span data-stu-id="c3a3b-154">Manage draft requests</span></span>

1. <span data-ttu-id="c3a3b-155">Selecteer het tabblad **Concepten**.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-155">Select the **Drafts** tab.</span></span>

   ![Tabblad Concepten in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="c3a3b-157">Selecteer het potlood om de aanvraag te bewerken of selecteer de prullenmand om de aanvraag te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="c3a3b-158">Voer eventueel benodigde wijzigingen uit.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-158">Make any necessary changes.</span></span> <span data-ttu-id="c3a3b-159">Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="c3a3b-160">U kunt ook **Opslaan als concept** selecteren als u later wilt terugkeren naar het concept.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Concept bewerken in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="c3a3b-162">Reageren op meldingen van teams</span><span class="sxs-lookup"><span data-stu-id="c3a3b-162">Respond to Teams notifications</span></span>

<span data-ttu-id="c3a3b-163">Wanneer u of een werknemer waarvoor u een fiatteur bent een verlofaanvraag indient, ontvangt u een melding in de Human Resources-app in Teams.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="c3a3b-164">U kunt de melding selecteren die u wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-164">You can select the notification to view it.</span></span> <span data-ttu-id="c3a3b-165">Meldingen worden ook weergegeven in het gebied **Chat**.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="c3a3b-166">Als u een fiatteur bent, kunt u **Goedkeuren** of **Weigeren** selecteren in de melding.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="c3a3b-167">U kunt ook een optioneel bericht opgeven.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-167">You can also provide an optional message.</span></span>

![Melding voor verlofaanvraag in Teams-app Human Resources](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="c3a3b-169">Informatie over gepland verlof aan uw collega's verzenden</span><span class="sxs-lookup"><span data-stu-id="c3a3b-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="c3a3b-170">Nadat u de app Human Resources voor Teams hebt geïnstalleerd, kunt u eenvoudig informatie over uw gepland verlof aan uw collega's in teams of chats sturen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="c3a3b-171">Selecteer in een team of chat in Teams de knop Human Resources onder het chatvenster.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Human Resources-knop onder chatvenster](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="c3a3b-173">Selecteer de verlofaanvraag die u wilt delen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-173">Select the leave request you want to share.</span></span> <span data-ttu-id="c3a3b-174">Als u een conceptverlofaanvraag wilt delen, selecteert u eerst **Concepten**.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Een aanvraag voor gepland verlof selecteren om te delen](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="c3a3b-176">Uw verlofaanvraag wordt in de chat weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-176">Your leave request will display in the chat.</span></span>

![Verlofaanvraagkaart Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="c3a3b-178">Als u een conceptaanvraag hebt gedeeld, wordt deze als een concept weergegeven:</span><span class="sxs-lookup"><span data-stu-id="c3a3b-178">If you shared a draft request, it will display as a draft:</span></span>

![Conceptverlofaanvraagkaart van Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="c3a3b-180">de verlofkalender van uw team weergeven</span><span class="sxs-lookup"><span data-stu-id="c3a3b-180">View your team's leave calendar</span></span>

<span data-ttu-id="c3a3b-181">Als u een manager met directe ondergeschikten bent, kunt u de goedgekeurde en in behandeling zijnde verlofaanvragen van uw team bekijken.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="c3a3b-182">Selecteer **Verlof** in de Human Resources-app in Teams.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="c3a3b-183">Selecteer **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-183">Select **Team calendar**.</span></span>

   ![Kalender weergeven in Teams-app Human Resources](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="c3a3b-185">In de kalender worden de goedgekeurde en in behandeling zijnde verlofaanvragen van uw directe ondergeschikten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Verlofkalender in Teams-app Human Resources](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="c3a3b-187">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="c3a3b-187">Troubleshooting</span></span>

<span data-ttu-id="c3a3b-188">Als u problemen ondervindt met het aanmelden bij of het gebruik van de Human Resources Teams-app, volgt u de onderstaande instructies voor het oplossen van problemen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="c3a3b-189">Als u na het oplossen van problemen nog steeds problemen ondervindt, neemt u contact op met de ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="c3a3b-190">Zie voor meer informatie [Ondersteuning krijgen](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="c3a3b-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="c3a3b-191">Kan me niet aanmelden bij de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="c3a3b-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="c3a3b-192">Als u zich niet kunt aanmelden bij de app, is het mogelijk dat de account die u gebruikt om u aan te melden bij Microsoft Teams niet is gekoppeld aan een werknemersrecord in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c3a3b-193">Neem contact op met uw systeembeheerder om er zeker van te zijn dat de werknemersrecord goed is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="c3a3b-194">Fout bij het goedkeuren van verlofaanvragen in de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="c3a3b-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="c3a3b-195">Als u een foutmelding krijgt tijdens het goedkeuren van verlofaanvragen in de Teams-app, probeer dan de volgende stappen voor het oplossen van problemen:</span><span class="sxs-lookup"><span data-stu-id="c3a3b-195">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="c3a3b-196">Controleer of de account waarmee u zich aanmeldt bij Microsoft Teams dezelfde account is als de account die u gebruikt om toegang te krijgen tot Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="c3a3b-197">Controleer of u een geldige fiatteur bent voor de aanvraag door de werkstroominstellingen te controleren op verlofgoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="c3a3b-198">Zie [Een werkstroom voor een verlofaanvraag maken](hr-leave-and-absence-workflow.md) voor meer informatie over werkstromen voor verlofaanvragen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="c3a3b-199">Bekende toegankelijkheidsproblemen</span><span class="sxs-lookup"><span data-stu-id="c3a3b-199">Known accessibility issues</span></span>

<span data-ttu-id="c3a3b-200">De app Human Resources in teams heeft de volgende toegankelijkheidsproblemen, die in toekomstige versies worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-200">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="c3a3b-201">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="c3a3b-201">Issue</span></span> | <span data-ttu-id="c3a3b-202">Tijdelijke oplossing of uitleg</span><span class="sxs-lookup"><span data-stu-id="c3a3b-202">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="c3a3b-203">Door te zoomen naar 400% op het bureaublad zijn enkele actieknoppen niet meer zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-203">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="c3a3b-204">U kunt beter een vergrootglas gebruiken, totdat dit zoomniveau wel wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-204">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="c3a3b-205">Op het tabblad **Vrije tijd** kondigt VoiceOver een actieknop aan tijdens het lezen van de koptekst voor het vrijetijdsrooster.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-205">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="c3a3b-206">De koptekst en elementen in het rooster worden gegroepeerd per jaar en ze kunnen worden samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-206">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="c3a3b-207">VoiceOver interpreteert dit als een uitvoerbaar item, maar dat is niet zo.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-207">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="c3a3b-208">Als u swipet terwijl een pop-up of menu is geopend, slaat VoiceOver de inhoud van het pop-upmenu of menu over.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-208">If you swipe while a popup or menu is open, voiceover skips reading the popup or menu contents.</span></span> | <span data-ttu-id="c3a3b-209">Verken de inhoud met vingerscannen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-209">Explore the content using finger scanning.</span></span> |
| <span data-ttu-id="c3a3b-210">Op het tabblad **Vrije tijd** is er een extra veeggebaar wanneer u naar **Redencode** navigeert in een nieuw verzoek.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-210">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="c3a3b-211">Er is geen verborgen besturingselement waar het veeggebaar naartoe probeert te navigeren.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-211">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="c3a3b-212">Als u op het tabblad **Vrij tijd** veegt terwijl de kalender geopend is, komt u buiten het besturingselement terecht in plaats van bovenaan een nieuwe aanvraag of tijdens het bewerken van een aanvraag.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-212">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="c3a3b-213">Wanneer u bij **Ga naar vandaag** komt, zie dat dan als het einde van het besturingselement en veeg in de omgekeerde richting om terug te gaan naar het begin.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-213">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="c3a3b-214">VoiceOver leest de labels voor datums niet.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-214">Voiceover doesn't read the labels for dates.</span></span> | <span data-ttu-id="c3a3b-215">De datums in paren zijn altijd **Begindatum** en **Einddatum**.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-215">The dates encountered in pairs are always **Start date** and **End date**.</span></span> |
| <span data-ttu-id="c3a3b-216">Op het tabblad **Chat** wordt de focus naar boven verplaatst wanneer u een datum invoert terwijl u het hulpprogramma of de toetsenbordnavigatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-216">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="c3a3b-217">Druk op de Tab-toets totdat u het invoergebied weer bereikt.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-217">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="c3a3b-218">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="c3a3b-218">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="c3a3b-219">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="c3a3b-219">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="c3a3b-220">Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-220">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="c3a3b-221">De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="c3a3b-221">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="c3a3b-222">Lees  [hier](https://www.luis.ai/) meer over LUIS.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-222">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="c3a3b-223">De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit).</span><span class="sxs-lookup"><span data-stu-id="c3a3b-223">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="c3a3b-224">Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/) van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-224">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="c3a3b-225">Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-225">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="c3a3b-226">De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-226">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c3a3b-227">Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-227">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="c3a3b-228">De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-228">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="c3a3b-229">Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-229">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="c3a3b-230">Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="c3a3b-230">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="c3a3b-231">Microsoft Teams, Azure Event Grid en Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c3a3b-231">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="c3a3b-232">Bij gebruik van de app Dynamics 365 Human Resources in Microsoft Teams kunnen bepaalde klantgegevens buiten het geografische gebied stromen waarin de Human Resources-service van de tenant is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-232">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="c3a3b-233">Dynamics 365 Human Resources verzendt het verlofverzoek van de werknemer en de werkstroomtaakgegevens naar Microsoft Azure Event Grid en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-233">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="c3a3b-234">Deze gegevens kunnen maximaal 24 uur worden opgeslagen in Microsoft Azure Event Grid en worden verwerkt in de Verenigde Staten, worden in transit en in rusttoestand versleuteld en worden niet door Microsoft of haar subverwerkers gebruikt voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-234">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="c3a3b-235">Zie [Locatie van gegevens in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) voor meer informatie over de opslag van uw gegevens in Teams.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-235">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="c3a3b-236">Tijdens een conversatie met de chatbot in de app Human Resources kan de inhoud van de conversatie worden opgeslagen in Azure Cosmos DB en worden verzonden naar Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-236">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="c3a3b-237">Deze gegevens kunnen maximaal 24 uur in Azure Cosmos DB worden opgeslagen en kunnen worden verwerkt buiten het geografische gebied waar de Human Resources-service van uw tenant is geïmplementeerd, worden in transit en in rusttoestand versleuteld en worden niet gebruikt door Microsoft of haar subverwerkers voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-237">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="c3a3b-238">Zie [Locatie van gegevens in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) voor meer informatie over de opslag van uw gegevens in Teams.</span><span class="sxs-lookup"><span data-stu-id="c3a3b-238">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="c3a3b-239">Als u toegang tot de app Human Resources in Microsoft Teams wilt beperken voor uw organisatie of gebruikers in uw organisatie, raadpleegt u [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="c3a3b-239">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="c3a3b-240">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c3a3b-240">See also</span></span>

[<span data-ttu-id="c3a3b-241">Microsoft Teams downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="c3a3b-241">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="c3a3b-242">Microsoft Teams-helpcentrum</span><span class="sxs-lookup"><span data-stu-id="c3a3b-242">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="c3a3b-243">Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="c3a3b-243">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
