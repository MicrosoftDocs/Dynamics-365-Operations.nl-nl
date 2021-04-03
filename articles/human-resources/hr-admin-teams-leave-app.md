---
title: Human resources-app in Teams
description: In dit onderwerp maakt u kennis met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
manager: tfehr
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 86abe32f76f2cc21c773727be07a44be49cdbac7
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487868"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="cab6c-103">Human resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="cab6c-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cab6c-104">Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunnen werknemers snel verlof aanvragen en informatie over hun verlofsaldo bekijken in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cab6c-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="cab6c-105">Werknemers kunnen communiceren met een bot om informatie aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="cab6c-106">Het tabblad **Verlof** bevat meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="cab6c-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="cab6c-107">Daarnaast kunnen ze mensen informatie sturen over uw aanstaande verlof in teams en chats buiten de Human Resources-app.</span><span class="sxs-lookup"><span data-stu-id="cab6c-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Bot voor verlof-app in Human Resources Teams](./media/hr-teams-leave-app-bot.png)

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Verlofaanvraagkaart Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="cab6c-111">Installeren en instellen</span><span class="sxs-lookup"><span data-stu-id="cab6c-111">Install and setup</span></span>

<span data-ttu-id="cab6c-112">De Dynamics 365 Human Resources-app is te vinden in het Teams-archief.</span><span class="sxs-lookup"><span data-stu-id="cab6c-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="cab6c-113">Zie [Verlofaanvragen in Teams beheren](hr-teams-leave-app.md) voor meer informatie over het installeren van de Teams-app.</span><span class="sxs-lookup"><span data-stu-id="cab6c-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="cab6c-114">Zie [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) voor informatie over het beheren van app-machtigingen in Teams.</span><span class="sxs-lookup"><span data-stu-id="cab6c-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="cab6c-115">Als u wilt dat uw gebruikers de verlof- en verzuimkalender in de app bekijken, moet u de **Verlof- en verzuimkalender in Teams** in Functiebeheer inschakelen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="cab6c-116">Meer informatie over het inschakelen van functies vindt u in [Functies beheren](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="cab6c-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="cab6c-117">Meldingen inschakelen voor de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="cab6c-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="cab6c-118">Als u wilt dat gebruikers meldingen over verlofaanvragen ontvangen in de Teams-app, moet u meldingen in Dynamics 365 Human Resources inschakelen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="cab6c-119">Alleen gebruikers die zijn aangemeld bij Teams en de Dynamics 365 Human Resources Teams-app gebruiken, ontvangen meldingen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="cab6c-120">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="cab6c-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="cab6c-121">Selecteer **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="cab6c-121">Select **Links**.</span></span>

3. <span data-ttu-id="cab6c-122">Selecteer onder **Instellingen** de optie **Systeemparameters**.</span><span class="sxs-lookup"><span data-stu-id="cab6c-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="cab6c-123">Stel op het tabblad **Algemeen** de optie **Meldingen inschakelen voor Teams-app** op **Ja** in.</span><span class="sxs-lookup"><span data-stu-id="cab6c-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Meldingen van Teams-app inschakelen in Systeemparameters](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="cab6c-125">Als u Teams-meldingen voor alle gebruikers wilt inschakelen, selecteert u **Ja** bij de prompt.</span><span class="sxs-lookup"><span data-stu-id="cab6c-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Teams-meldingen inschakelen voor alle gebruikers](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="cab6c-127">Teams-meldingen in- of uitschakelen voor afzonderlijke gebruikers</span><span class="sxs-lookup"><span data-stu-id="cab6c-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="cab6c-128">Nadat u meldingen voor de Dynamics 365 Human Resources Teams-app hebt ingeschakeld, kunt u meldingen in- of uitschakelen voor afzonderlijke gebruikers.</span><span class="sxs-lookup"><span data-stu-id="cab6c-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="cab6c-129">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="cab6c-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="cab6c-130">Selecteer **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="cab6c-130">Select **Links**.</span></span>

3. <span data-ttu-id="cab6c-131">Selecteer **Gebruikersopties** onder **Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="cab6c-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="cab6c-132">Selecteer het tabblad **Werkstroom**.</span><span class="sxs-lookup"><span data-stu-id="cab6c-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="cab6c-133">Stel **Meldingen inschakelen voor Teams-app** in op **Ja** als u meldingen voor de gebruiker wilt inschakelen of op **Nee** als u meldingen voor de gebruiker wilt uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Meldingen in Teams-app inschakelen in gebruikersopties op het tabblad Werkstroom](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="cab6c-135">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="cab6c-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="cab6c-136">Ondersteunde talen</span><span class="sxs-lookup"><span data-stu-id="cab6c-136">Supported languages</span></span>

<span data-ttu-id="cab6c-137">De Dynamics 365 Human Resources-app in Teams ondersteunt de volgende talen:</span><span class="sxs-lookup"><span data-stu-id="cab6c-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="cab6c-138">Landinstellingen-id</span><span class="sxs-lookup"><span data-stu-id="cab6c-138">Locale ID</span></span> | <span data-ttu-id="cab6c-139">Taal</span><span class="sxs-lookup"><span data-stu-id="cab6c-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="cab6c-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="cab6c-140">de-DE</span></span> | <span data-ttu-id="cab6c-141">Duits (Duitsland)</span><span class="sxs-lookup"><span data-stu-id="cab6c-141">German (Germany)</span></span> |
| <span data-ttu-id="cab6c-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="cab6c-142">es-ES</span></span> | <span data-ttu-id="cab6c-143">Spaans (Spanje)</span><span class="sxs-lookup"><span data-stu-id="cab6c-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="cab6c-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="cab6c-144">es-MX</span></span> | <span data-ttu-id="cab6c-145">Spaans (Mexico)</span><span class="sxs-lookup"><span data-stu-id="cab6c-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="cab6c-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="cab6c-146">fr-CA</span></span> | <span data-ttu-id="cab6c-147">Frans (Canada)</span><span class="sxs-lookup"><span data-stu-id="cab6c-147">French (Canada)</span></span> |
| <span data-ttu-id="cab6c-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="cab6c-148">fr-FR</span></span> | <span data-ttu-id="cab6c-149">Frans (Frankrijk)</span><span class="sxs-lookup"><span data-stu-id="cab6c-149">French (France)</span></span> |
| <span data-ttu-id="cab6c-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="cab6c-150">it-IT</span></span> | <span data-ttu-id="cab6c-151">Italiaans (Italië)</span><span class="sxs-lookup"><span data-stu-id="cab6c-151">Italian (Italy)</span></span> |
| <span data-ttu-id="cab6c-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="cab6c-152">nl-NL</span></span> | <span data-ttu-id="cab6c-153">Nederlands (Nederland)</span><span class="sxs-lookup"><span data-stu-id="cab6c-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="cab6c-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="cab6c-154">pt-BR</span></span> | <span data-ttu-id="cab6c-155">Portugees (Brazilië)</span><span class="sxs-lookup"><span data-stu-id="cab6c-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="cab6c-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="cab6c-156">tr-TR</span></span> | <span data-ttu-id="cab6c-157">Turks (Turkije)</span><span class="sxs-lookup"><span data-stu-id="cab6c-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="cab6c-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="cab6c-158">zh-CN</span></span> | <span data-ttu-id="cab6c-159">Chinees (vereenvoudigd)</span><span class="sxs-lookup"><span data-stu-id="cab6c-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="cab6c-160">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cab6c-160">Notes</span></span>

<span data-ttu-id="cab6c-161">De volgende werkitems staan op de planning voor toekomstige releases:</span><span class="sxs-lookup"><span data-stu-id="cab6c-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="cab6c-162">Werkitem</span><span class="sxs-lookup"><span data-stu-id="cab6c-162">Work item</span></span> | <span data-ttu-id="cab6c-163">Status</span><span class="sxs-lookup"><span data-stu-id="cab6c-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="cab6c-164">Het saldo is onjuist bij het indienen van verlof voor een toekomstige datum.</span><span class="sxs-lookup"><span data-stu-id="cab6c-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="cab6c-165">Prognose maken is nog niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="cab6c-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="cab6c-166">Het saldo wordt weergegeven voor de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="cab6c-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="cab6c-167">Kan een aanvraag **Wordt gecontroleerd** niet annuleren.</span><span class="sxs-lookup"><span data-stu-id="cab6c-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="cab6c-168">Deze functionaliteit wordt momenteel niet ondersteund en wordt in een toekomstige versie toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="cab6c-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="cab6c-169">Saldogegevens worden vanaf vandaag berekend.</span><span class="sxs-lookup"><span data-stu-id="cab6c-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="cab6c-170">Het systeem geeft momenteel geen saldi weer voor de toerekeningsperiode, zelfs als deze is geconfigureerd in de parameters voor verlof en verzuim.</span><span class="sxs-lookup"><span data-stu-id="cab6c-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="cab6c-171">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="cab6c-171">Troubleshooting</span></span>

<span data-ttu-id="cab6c-172">Als een gebruiker problemen heeft met het aanmelden bij of het gebruik van de Human Resources Teams-app, volgt u de onderstaande instructies voor het oplossen van problemen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="cab6c-173">Als u na het oplossen van problemen nog steeds problemen ondervindt, neemt u contact op met de ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="cab6c-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="cab6c-174">Zie voor meer informatie [Ondersteuning krijgen](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="cab6c-174">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="cab6c-175">Kan me niet aanmelden bij de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="cab6c-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="cab6c-176">Als een gebruiker contact met u opneemt omdat deze zich niet kan aanmelden bij de app, controleert u of de gebruiker een bijbehorende werknemersrecord heeft in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cab6c-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="cab6c-177">Fout bij het goedkeuren van verlofaanvragen in de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="cab6c-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="cab6c-178">Als gebruikers een foutmelding krijgen tijdens het goedkeuren van verlofaanvragen in de Teams-app, probeert u de volgende stappen voor het oplossen van problemen:</span><span class="sxs-lookup"><span data-stu-id="cab6c-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="cab6c-179">Controleer of hun Teams-account dezelfde is als de account die ze voor toegang tot Human Resources gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cab6c-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="cab6c-180">Controleer of ze een geldige fiatteur zijn voor de aanvraag door de werkstroominstellingen te controleren op verlofgoedkeuring.</span><span class="sxs-lookup"><span data-stu-id="cab6c-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="cab6c-181">Zie [Een werkstroom voor een verlofaanvraag maken](hr-leave-and-absence-workflow.md) voor meer informatie over werkstromen voor verlofaanvragen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="cab6c-182">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="cab6c-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="cab6c-183">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="cab6c-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="cab6c-184">Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="cab6c-185">De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="cab6c-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="cab6c-186">Lees  [hier](https://www.luis.ai/) meer over LUIS.</span><span class="sxs-lookup"><span data-stu-id="cab6c-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="cab6c-187">De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit).</span><span class="sxs-lookup"><span data-stu-id="cab6c-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="cab6c-188">Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/) van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery.</span><span class="sxs-lookup"><span data-stu-id="cab6c-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="cab6c-189">Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="cab6c-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="cab6c-190">De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cab6c-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cab6c-191">Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="cab6c-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="cab6c-192">De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering.</span><span class="sxs-lookup"><span data-stu-id="cab6c-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="cab6c-193">Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="cab6c-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="cab6c-194">Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="cab6c-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="cab6c-195">Microsoft Teams, Azure Event Grid en Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cab6c-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="cab6c-196">Bij gebruik van de app Dynamics 365 Human Resources in Microsoft Teams kunnen bepaalde klantgegevens buiten het geografische gebied stromen waarin de Human Resources-service van de tenant is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="cab6c-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="cab6c-197">Dynamics 365 Human Resources verzendt het verlofverzoek van de werknemer en de werkstroomtaakgegevens naar Microsoft Azure Event Grid en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cab6c-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="cab6c-198">Deze gegevens kunnen maximaal 24 uur worden opgeslagen in Microsoft Azure Event Grid en worden verwerkt in de Verenigde Staten, worden in transit en in rusttoestand versleuteld en worden niet door Microsoft of haar subverwerkers gebruikt voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="cab6c-199">Zie [Locatie van gegevens in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) voor meer informatie over de opslag van uw gegevens in Teams.</span><span class="sxs-lookup"><span data-stu-id="cab6c-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="cab6c-200">Tijdens een conversatie met de chatbot in de app Human Resources kan de inhoud van de conversatie worden opgeslagen in Azure Cosmos DB en worden verzonden naar Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cab6c-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="cab6c-201">Deze gegevens kunnen maximaal 24 uur in Azure Cosmos DB worden opgeslagen en kunnen worden verwerkt buiten het geografische gebied waar de Human Resources-service van uw tenant is geïmplementeerd, worden in transit en in rusttoestand versleuteld en worden niet gebruikt door Microsoft of haar subverwerkers voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="cab6c-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="cab6c-202">Zie [Locatie van gegevens in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) voor meer informatie over de opslag van uw gegevens in Teams.</span><span class="sxs-lookup"><span data-stu-id="cab6c-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="cab6c-203">Als u toegang tot de app Human Resources in Microsoft Teams wilt beperken voor uw organisatie of gebruikers in uw organisatie, raadpleegt u [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="cab6c-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="cab6c-204">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cab6c-204">See also</span></span> 

[<span data-ttu-id="cab6c-205">Microsoft Teams downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="cab6c-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="cab6c-206">Microsoft Teams-helpcentrum</span><span class="sxs-lookup"><span data-stu-id="cab6c-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="cab6c-207">Verlofaanvragen beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="cab6c-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]