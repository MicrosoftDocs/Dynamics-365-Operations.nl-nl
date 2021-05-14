---
title: Verlofaanvragen beheren in Teams
description: In dit onderwerp wordt beschreven hoe u verlof kunt aanvragen in de Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2ea495259ba29f302753991e260d5a8fa990322b
ms.sourcegitcommit: e3f11fc9a9dae416a490437678bb482a0094f9a9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5953407"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="4a2bd-103">Verlofaanvragen beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="4a2bd-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4a2bd-104">Met de Dynamics 365 Human Resources-app in Microsoft Teams kunt u snel verlof aanvragen en informatie over uw verlofsaldo bekijken rechtstreeks vanuit Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="4a2bd-105">U kunt werken met een bot om informatie aan te vragen en een verlofaanvraag te starten.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="4a2bd-106">Het tabblad **Verlof** bevat meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="4a2bd-107">U kunt mensen ook informatie sturen over uw geplande verlof in Teams en chats buiten de app Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="4a2bd-108">De app installeren</span><span class="sxs-lookup"><span data-stu-id="4a2bd-108">Install the app</span></span>

<span data-ttu-id="4a2bd-109">De Dynamics 365 Human Resources-app is te vinden in het Teams-archief.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="4a2bd-110">Selecteer de drie puntjes in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Drie puntjes in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="4a2bd-112">Zoek naar Dynamics 365 Human Resources en selecteer de tegel **Human resources**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-tegel van verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="4a2bd-114">Selecteer de knop **Toevoegen** om de app te installeren.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-114">Select the **Add** button to install the app.</span></span>

   ![Installatie van verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="4a2bd-116">Als u niet automatisch wordt aangemeld bij de app, selecteert u het tabblad **Instellingen** om zich aan te melden.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Tabblad Instellingen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="4a2bd-118">Als er geen dialoogvenster voor aanmelding wordt weergegeven, controleert u de instellingen van uw browser om pop-ups toe te staan.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="4a2bd-119">Als u toegang hebt tot meer dan één exemplaar van Human resources, kunt u de omgeving selecteren waarmee u verbinding wilt maken op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="4a2bd-120">De app ondersteunt nu de beveiligingsrol Systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="4a2bd-121">De bot gebruiken</span><span class="sxs-lookup"><span data-stu-id="4a2bd-121">Use the bot</span></span>

<span data-ttu-id="4a2bd-122">Na de installatie van de app wordt er een welkomstbericht weergegeven, zodat u weet welke acties de bot namens u kan ondernemen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Welkomstbericht in verlof-app voor Human Resource Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="4a2bd-124">Bij het eerste contact met de bot moet u zich mogelijk aanmelden.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="4a2bd-125">Als er geen dialoogvenster voor aanmelding wordt weergegeven, controleert u de instellingen van uw browser om pop-ups toe te staan.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="4a2bd-126">U kunt de bot vragen om het volgende te doen:</span><span class="sxs-lookup"><span data-stu-id="4a2bd-126">You can ask the bot to:</span></span>

- <span data-ttu-id="4a2bd-127">Een verlofaanvraag voor u starten.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-127">Start a leave request for you.</span></span>

  ![Een verlofaanvraag starten in Teams-chat](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="4a2bd-129">In het chatgesprek wordt een verlofaanvraag voor u ingevuld.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="4a2bd-130">Selecteer **Verlof aanvragen** en bewerk de details voor uw aanvraag.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Details van verlofaanvraag bewerken](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="4a2bd-132">Wanneer u klaar bent met het bewerken van uw verlofaanvraagdetails, selecteert u **Indienen** om de aanvraag voor goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Verlofaanvraag indienen](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="4a2bd-134">Uw verlof beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="4a2bd-134">Manage your leave in Teams</span></span>

<span data-ttu-id="4a2bd-135">Op het tabblad **Verlof** kunt u het volgende bekijken:</span><span class="sxs-lookup"><span data-stu-id="4a2bd-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="4a2bd-136">Saldo-informatie voor elk type verlof waarvoor u zich hebt ingeschreven</span><span class="sxs-lookup"><span data-stu-id="4a2bd-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="4a2bd-137">Aanstaande verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="4a2bd-137">Upcoming leave requests</span></span>

- <span data-ttu-id="4a2bd-138">Verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="4a2bd-138">Time-off requests</span></span>

- <span data-ttu-id="4a2bd-139">Conceptaanvragen voor verlof</span><span class="sxs-lookup"><span data-stu-id="4a2bd-139">Draft leave requests</span></span>

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="4a2bd-141">Een nieuwe aanvraag maken</span><span class="sxs-lookup"><span data-stu-id="4a2bd-141">Create a new request</span></span>

1. <span data-ttu-id="4a2bd-142">Selecteer **Nieuwe aanvraag** om een nieuwe verlofaanvraag te maken.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-142">To create a new leave request, select **New request**.</span></span>

   ![Nieuwe aanvraag in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="4a2bd-144">Voer de dag of dagen in die u wilt vrijnemen en selecteer vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Verlof toevoegen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="4a2bd-146">Voer een redencode in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="4a2bd-147">Voer ook eventuele opmerkingen in en voeg eventuele bijlagen toe.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="4a2bd-148">Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="4a2bd-149">U kunt ook **Opslaan als concept** opgeven als u later wilt terugkeren naar het concept.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="4a2bd-150">Conceptaanvragen beheren</span><span class="sxs-lookup"><span data-stu-id="4a2bd-150">Manage draft requests</span></span>

1. <span data-ttu-id="4a2bd-151">Selecteer het tabblad **Concepten**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-151">Select the **Drafts** tab.</span></span>

   ![Tabblad Concepten in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="4a2bd-153">Selecteer het potlood om de aanvraag te bewerken of selecteer de prullenmand om de aanvraag te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="4a2bd-154">Voer eventueel benodigde wijzigingen uit.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-154">Make any necessary changes.</span></span> <span data-ttu-id="4a2bd-155">Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="4a2bd-156">U kunt ook **Opslaan als concept** selecteren als u later wilt terugkeren naar het concept.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Concept bewerken in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="4a2bd-158">Reageren op meldingen van teams</span><span class="sxs-lookup"><span data-stu-id="4a2bd-158">Respond to Teams notifications</span></span>

<span data-ttu-id="4a2bd-159">Wanneer u of een werknemer waarvoor u een fiatteur bent een verlofaanvraag indient, ontvangt u een melding in de Human Resources-app in Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="4a2bd-160">U kunt de melding selecteren die u wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-160">You can select the notification to view it.</span></span> <span data-ttu-id="4a2bd-161">Meldingen worden ook weergegeven in het gebied **Chat**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="4a2bd-162">Als u een fiatteur bent, kunt u **Goedkeuren** of **Weigeren** selecteren in de melding.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="4a2bd-163">U kunt ook een optioneel bericht opgeven.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-163">You can also provide an optional message.</span></span>

![Melding voor verlofaanvraag in Teams-app Human Resources](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="4a2bd-165">Informatie over gepland verlof aan uw collega's verzenden</span><span class="sxs-lookup"><span data-stu-id="4a2bd-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="4a2bd-166">Nadat u de app Human Resources voor Teams hebt geïnstalleerd, kunt u eenvoudig informatie over uw gepland verlof aan uw collega's in teams of chats sturen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="4a2bd-167">Selecteer in een team of chat in Teams de knop Human Resources onder het chatvenster.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Human Resources-knop onder chatvenster](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="4a2bd-169">Selecteer de verlofaanvraag die u wilt delen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-169">Select the leave request you want to share.</span></span> <span data-ttu-id="4a2bd-170">Als u een conceptverlofaanvraag wilt delen, selecteert u eerst **Concepten**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Een aanvraag voor gepland verlof selecteren om te delen](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="4a2bd-172">Uw verlofaanvraag wordt in de chat weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-172">Your leave request will display in the chat.</span></span>

![Verlofaanvraagkaart Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="4a2bd-174">Als u een conceptaanvraag hebt gedeeld, wordt deze als een concept weergegeven:</span><span class="sxs-lookup"><span data-stu-id="4a2bd-174">If you shared a draft request, it will display as a draft:</span></span>

![Conceptverlofaanvraagkaart van Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="4a2bd-176">de verlofkalender van uw team weergeven</span><span class="sxs-lookup"><span data-stu-id="4a2bd-176">View your team's leave calendar</span></span>

<span data-ttu-id="4a2bd-177">Als u een manager met directe ondergeschikten bent, kunt u de goedgekeurde en in behandeling zijnde verlofaanvragen van uw team bekijken.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="4a2bd-178">Selecteer **Verlof** in de Human Resources-app in Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="4a2bd-179">Selecteer **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-179">Select **Team calendar**.</span></span> <span data-ttu-id="4a2bd-180">In de kalender worden de goedgekeurde en in behandeling zijnde verlofaanvragen van uw directe ondergeschikten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Kalender weergeven in Teams-app Human Resources](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="4a2bd-182">Als u de teamkalender niet kunt zien, vraagt u uw beheerder deze in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="4a2bd-183">Zie [Installeren en instellen](hr-admin-teams-leave-app.md#install-and-setup) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="4a2bd-184">Ondersteunde talen</span><span class="sxs-lookup"><span data-stu-id="4a2bd-184">Supported languages</span></span>

<span data-ttu-id="4a2bd-185">De Dynamics 365 Human Resources-app in Teams ondersteunt de volgende talen:</span><span class="sxs-lookup"><span data-stu-id="4a2bd-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="4a2bd-186">Landinstellingen-id</span><span class="sxs-lookup"><span data-stu-id="4a2bd-186">Locale ID</span></span> | <span data-ttu-id="4a2bd-187">Taal</span><span class="sxs-lookup"><span data-stu-id="4a2bd-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="4a2bd-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="4a2bd-188">de-DE</span></span> | <span data-ttu-id="4a2bd-189">Duits (Duitsland)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-189">German (Germany)</span></span> |
| <span data-ttu-id="4a2bd-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="4a2bd-190">es-ES</span></span> | <span data-ttu-id="4a2bd-191">Spaans (Spanje)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="4a2bd-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="4a2bd-192">es-MX</span></span> | <span data-ttu-id="4a2bd-193">Spaans (Mexico)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="4a2bd-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="4a2bd-194">fr-CA</span></span> | <span data-ttu-id="4a2bd-195">Frans (Canada)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-195">French (Canada)</span></span> |
| <span data-ttu-id="4a2bd-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="4a2bd-196">fr-FR</span></span> | <span data-ttu-id="4a2bd-197">Frans (Frankrijk)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-197">French (France)</span></span> |
| <span data-ttu-id="4a2bd-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="4a2bd-198">it-IT</span></span> | <span data-ttu-id="4a2bd-199">Italiaans (Italië)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-199">Italian (Italy)</span></span> |
| <span data-ttu-id="4a2bd-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="4a2bd-200">nl-NL</span></span> | <span data-ttu-id="4a2bd-201">Nederlands (Nederland)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="4a2bd-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="4a2bd-202">pt-BR</span></span> | <span data-ttu-id="4a2bd-203">Portugees (Brazilië)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="4a2bd-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="4a2bd-204">tr-TR</span></span> | <span data-ttu-id="4a2bd-205">Turks (Turkije)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="4a2bd-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="4a2bd-206">zh-CN</span></span> | <span data-ttu-id="4a2bd-207">Chinees (vereenvoudigd)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="4a2bd-208">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="4a2bd-208">Troubleshooting</span></span>

<span data-ttu-id="4a2bd-209">Als u problemen ondervindt met het aanmelden bij of het gebruik van de Dynamics 365 Human Resources Teams-app, volgt u de onderstaande instructies voor het oplossen van problemen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="4a2bd-210">Als u na het oplossen van problemen nog steeds problemen ondervindt, neemt u contact op met de ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="4a2bd-211">Zie voor meer informatie [Ondersteuning krijgen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="4a2bd-211">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="4a2bd-212">Kan me niet aanmelden bij de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="4a2bd-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="4a2bd-213">Als u zich niet kunt aanmelden bij de app, is het mogelijk dat de account die u gebruikt om u aan te melden bij Microsoft Teams niet is gekoppeld aan een werknemersrecord in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4a2bd-214">Neem contact op met uw systeembeheerder om er zeker van te zijn dat de werknemersrecord goed is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="4a2bd-215">Vertalingen worden niet op de juiste manier weergegeven</span><span class="sxs-lookup"><span data-stu-id="4a2bd-215">Translations don't display correctly</span></span>

<span data-ttu-id="4a2bd-216">Als vertalingen niet worden weergegeven zoals u verwacht, moet u ervoor zorgen dat de taal die u selecteert in Teams overeenkomt met de taal die is geselecteerd bij **Gebruikersopties** in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="4a2bd-217">Kijk in Teams naar **Taal van de app** bij **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-217">In Teams, look at **App language** in **Settings**.</span></span>

![Teams-instellingen](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="4a2bd-219">Selecteer in Human Resources de optie **Instellingen** en **Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="4a2bd-220">Controleer of het veld **Taal** overeenkomt met het veld **Taal van de app** in Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Gebruikersopties in Human Resources](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="4a2bd-222">Als u nog steeds vertaalproblemen ondervindt, laat u het ons weten.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="4a2bd-223">Zie [Ondersteuning voor Finance and Operations-apps of Lifecycle Services (LCS) krijgen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="4a2bd-224">Fout bij het goedkeuren van verlofaanvragen in de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="4a2bd-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="4a2bd-225">Als u een foutmelding krijgt tijdens het goedkeuren van verlofaanvragen in de Teams-app, probeer dan de volgende stappen voor het oplossen van problemen:</span><span class="sxs-lookup"><span data-stu-id="4a2bd-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="4a2bd-226">Controleer of de account waarmee u zich aanmeldt bij Microsoft Teams dezelfde account is als de account die u gebruikt om toegang te krijgen tot Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="4a2bd-227">Controleer of u een geldige fiatteur bent voor de aanvraag door de werkstroominstellingen te controleren op verlofgoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="4a2bd-228">Zie [Een werkstroom voor een verlofaanvraag maken](hr-leave-and-absence-workflow.md) voor meer informatie over werkstromen voor verlofaanvragen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="4a2bd-229">Verloffiatteurs ontvangen geen Teams-chatberichten om verlofaanvragen goed te keuren</span><span class="sxs-lookup"><span data-stu-id="4a2bd-229">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="4a2bd-230">Zorg ervoor dat meldingen zijn ingeschakeld voor de omgeving en de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-230">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="4a2bd-231">Meer informatie over dit onderwerp vindt u in [Meldingen inschakelen voor de Human Resources-app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) en [Teams-meldingen in- of uitschakelen voor afzonderlijke gebruikers](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="4a2bd-231">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="4a2bd-232">Zorg ervoor dat gebruikers zijn aangemeld op het tabblad **Chats** met dezelfde referenties die ze gebruiken voor het goedkeuren van verlofaanvragen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-232">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="4a2bd-233">Gebruik de berichten "afmelden" en vervolgens "aanmelden" om u aan te melden met de juiste referenties.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-233">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="4a2bd-234">Als het probleem blijft bestaan, controleert u als systeembeheerder de status van de systeembatch taak Zakelijke gebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-234">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="4a2bd-235">Als de taak in de fase fase Wachtend of In uitvoering staat, controleert u deze nog eens over enkele minuten.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-235">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="4a2bd-236">Als de status niet verandert, kunt u een ondersteuningsticket indienen zodat ons team u kan helpen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-236">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="4a2bd-237">Bekende toegankelijkheidsproblemen</span><span class="sxs-lookup"><span data-stu-id="4a2bd-237">Known accessibility issues</span></span>

<span data-ttu-id="4a2bd-238">De app Human Resources in teams heeft de volgende toegankelijkheidsproblemen, die in toekomstige versies worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-238">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="4a2bd-239">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="4a2bd-239">Issue</span></span> | <span data-ttu-id="4a2bd-240">Tijdelijke oplossing of uitleg</span><span class="sxs-lookup"><span data-stu-id="4a2bd-240">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="4a2bd-241">Door te zoomen naar 400% op het bureaublad zijn enkele actieknoppen niet meer zichtbaar.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-241">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="4a2bd-242">U kunt beter een vergrootglas gebruiken, totdat dit zoomniveau wel wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-242">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="4a2bd-243">Op het tabblad **Vrije tijd** kondigt VoiceOver een actieknop aan tijdens het lezen van de koptekst voor het vrijetijdsrooster.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-243">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="4a2bd-244">De koptekst en elementen in het rooster worden gegroepeerd per jaar en ze kunnen worden samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-244">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="4a2bd-245">VoiceOver interpreteert dit als een uitvoerbaar item, maar dat is niet zo.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-245">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="4a2bd-246">Op het tabblad **Vrije tijd** is er een extra veeggebaar wanneer u naar **Redencode** navigeert in een nieuw verzoek.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-246">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="4a2bd-247">Er is geen verborgen besturingselement waar het veeggebaar naartoe probeert te navigeren.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-247">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="4a2bd-248">Als u op het tabblad **Vrij tijd** veegt terwijl de kalender geopend is, komt u buiten het besturingselement terecht in plaats van bovenaan een nieuwe aanvraag of tijdens het bewerken van een aanvraag.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-248">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="4a2bd-249">Wanneer u bij **Ga naar vandaag** komt, zie dat dan als het einde van het besturingselement en veeg in de omgekeerde richting om terug te gaan naar het begin.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-249">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="4a2bd-250">Op het tabblad **Chat** wordt de focus naar boven verplaatst wanneer u een datum invoert terwijl u het hulpprogramma of de toetsenbordnavigatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-250">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="4a2bd-251">Druk op de Tab-toets totdat u het invoergebied weer bereikt.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-251">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="4a2bd-252">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="4a2bd-252">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="4a2bd-253">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-253">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="4a2bd-254">Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-254">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="4a2bd-255">De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="4a2bd-255">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="4a2bd-256">Lees  [hier](https://www.luis.ai/) meer over LUIS.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-256">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="4a2bd-257">De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit).</span><span class="sxs-lookup"><span data-stu-id="4a2bd-257">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="4a2bd-258">Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/) van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-258">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="4a2bd-259">Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-259">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="4a2bd-260">De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-260">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4a2bd-261">Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-261">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="4a2bd-262">De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-262">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="4a2bd-263">Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-263">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="4a2bd-264">Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="4a2bd-264">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="4a2bd-265">Microsoft Teams, Azure Event Grid en Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="4a2bd-265">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="4a2bd-266">Bij gebruik van de app Dynamics 365 Human Resources in Microsoft Teams kunnen bepaalde klantgegevens buiten het geografische gebied stromen waarin de Human Resources-service van de tenant is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-266">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="4a2bd-267">Dynamics 365 Human Resources verzendt het verlofverzoek van de werknemer en de werkstroomtaakgegevens naar Microsoft Azure Event Grid en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-267">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="4a2bd-268">Deze gegevens kunnen maximaal 24 uur worden opgeslagen in Microsoft Azure Event Grid en worden verwerkt in de Verenigde Staten, worden in transit en in rusttoestand versleuteld en worden niet door Microsoft of haar subverwerkers gebruikt voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-268">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="4a2bd-269">Zie [Locatie van gegevens in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide) voor meer informatie over de opslag van uw gegevens in Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-269">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="4a2bd-270">Tijdens een conversatie met de chatbot in de app Human Resources kan de inhoud van de conversatie worden opgeslagen in Azure Cosmos DB en worden verzonden naar Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-270">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="4a2bd-271">Deze gegevens kunnen maximaal 24 uur in Azure Cosmos DB worden opgeslagen en kunnen worden verwerkt buiten het geografische gebied waar de Human Resources-service van uw tenant is geïmplementeerd, worden in transit en in rusttoestand versleuteld en worden niet gebruikt door Microsoft of haar subverwerkers voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-271">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="4a2bd-272">Zie [Locatie van gegevens in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide) voor meer informatie over de opslag van uw gegevens in Teams.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-272">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="4a2bd-273">Als u toegang tot de app Human Resources in Microsoft Teams wilt beperken voor uw organisatie of gebruikers in uw organisatie, raadpleegt u [Machtigingsbeleid voor apps beheren in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="4a2bd-273">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="4a2bd-274">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4a2bd-274">See also</span></span>

[<span data-ttu-id="4a2bd-275">Microsoft Teams downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="4a2bd-275">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="4a2bd-276">Microsoft Teams-helpcentrum</span><span class="sxs-lookup"><span data-stu-id="4a2bd-276">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="4a2bd-277">Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="4a2bd-277">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]