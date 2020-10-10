---
title: Human resources-app in Teams
description: In dit onderwerp maakt u kennis met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
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
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828909"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="24dea-103">Human resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="24dea-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="24dea-104">Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunnen werknemers snel verlof aanvragen en informatie over hun verlofsaldo bekijken in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="24dea-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="24dea-105">Werknemers kunnen communiceren met een bot om informatie aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="24dea-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="24dea-106">Het tabblad **Verlof** bevat gedetailleerdere informatie. Bovendien kan aan mensen informatie worden verzonden over gepland verlof in teams en chats buiten de app Human Resources.</span><span class="sxs-lookup"><span data-stu-id="24dea-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Bot voor verlof-app in Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Verlofaanvraagkaart Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="24dea-110">Installeren en instellen</span><span class="sxs-lookup"><span data-stu-id="24dea-110">Install and setup</span></span>

<span data-ttu-id="24dea-111">De Human resources-app is te vinden in het Teams-archief.</span><span class="sxs-lookup"><span data-stu-id="24dea-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="24dea-112">Zie [Verlofaanvragen in Teams beheren](hr-teams-leave-app.md) voor meer informatie over het installeren van de Teams-app.</span><span class="sxs-lookup"><span data-stu-id="24dea-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="24dea-113">Zie [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) voor informatie over het beheren van app-machtigingen in Teams.</span><span class="sxs-lookup"><span data-stu-id="24dea-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="24dea-114">Meldingen inschakelen voor de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="24dea-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="24dea-115">Als u wilt dat gebruikers meldingen over verlofaanvragen ontvangen in de Teams-app, moet u meldingen in Human Resources inschakelen.</span><span class="sxs-lookup"><span data-stu-id="24dea-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="24dea-116">Alleen gebruikers die zijn aangemeld bij Teams en de Teams-app Human Resources gebruiken, ontvangen meldingen.</span><span class="sxs-lookup"><span data-stu-id="24dea-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="24dea-117">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="24dea-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="24dea-118">Selecteer **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="24dea-118">Select **Links**.</span></span>

3. <span data-ttu-id="24dea-119">Selecteer onder **Instellingen** de optie **Systeemparameters**.</span><span class="sxs-lookup"><span data-stu-id="24dea-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="24dea-120">Stel op het tabblad **Algemeen** de optie **Meldingen inschakelen voor Teams-app** op **Ja** in.</span><span class="sxs-lookup"><span data-stu-id="24dea-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Meldingen van Teams-app inschakelen in Systeemparameters](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="24dea-122">Als u Teams-meldingen voor alle gebruikers wilt inschakelen, selecteert u **Ja** bij de prompt.</span><span class="sxs-lookup"><span data-stu-id="24dea-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Teams-meldingen inschakelen voor alle gebruikers](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="24dea-124">Teams-meldingen in- of uitschakelen voor afzonderlijke gebruikers</span><span class="sxs-lookup"><span data-stu-id="24dea-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="24dea-125">Nadat u meldingen voor de Teams-app Human Resources teams hebt ingeschakeld, kunt u meldingen in- of uitschakelen voor afzonderlijke gebruikers.</span><span class="sxs-lookup"><span data-stu-id="24dea-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="24dea-126">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="24dea-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="24dea-127">Selecteer **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="24dea-127">Select **Links**.</span></span>

3. <span data-ttu-id="24dea-128">Selecteer **Gebruikersopties** onder **Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="24dea-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="24dea-129">Selecteer het tabblad **Werkstroom**.</span><span class="sxs-lookup"><span data-stu-id="24dea-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="24dea-130">Stel **Meldingen inschakelen voor Teams-app** in op **Ja** als u meldingen voor de gebruiker wilt inschakelen of op **Nee** als u meldingen voor de gebruiker wilt uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="24dea-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Meldingen in Teams-app inschakelen in gebruikersopties op het tabblad Werkstroom](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="24dea-132">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="24dea-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="24dea-133">Bekende problemen</span><span class="sxs-lookup"><span data-stu-id="24dea-133">Known issues</span></span>

| <span data-ttu-id="24dea-134">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="24dea-134">Issue</span></span> | <span data-ttu-id="24dea-135">Status</span><span class="sxs-lookup"><span data-stu-id="24dea-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="24dea-136">Horizontaal schuiven werkt niet op Android-telefoons</span><span class="sxs-lookup"><span data-stu-id="24dea-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="24dea-137">Horizontaal schuiven is geen probleem op iOS- of bureaubladapparaten.</span><span class="sxs-lookup"><span data-stu-id="24dea-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="24dea-138">Wij werken aan een oplossing voor Android.</span><span class="sxs-lookup"><span data-stu-id="24dea-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="24dea-139">Het saldo is onjuist bij het indienen van verlof voor een toekomstige datum.</span><span class="sxs-lookup"><span data-stu-id="24dea-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="24dea-140">Prognose maken is nog niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="24dea-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="24dea-141">Het saldo wordt weergegeven voor de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="24dea-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="24dea-142">Kan een aanvraag **Wordt gecontroleerd** niet annuleren.</span><span class="sxs-lookup"><span data-stu-id="24dea-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="24dea-143">Deze functionaliteit wordt momenteel niet ondersteund en wordt in een toekomstige versie toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="24dea-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="24dea-144">Saldogegevens worden vanaf vandaag berekend.</span><span class="sxs-lookup"><span data-stu-id="24dea-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="24dea-145">Het systeem geeft momenteel geen saldi weer voor de toerekeningsperiode, zelfs als deze is geconfigureerd in de parameters voor verlof en verzuim.</span><span class="sxs-lookup"><span data-stu-id="24dea-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="24dea-146">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="24dea-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="24dea-147">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="24dea-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="24dea-148">Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="24dea-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="24dea-149">De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="24dea-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="24dea-150">Lees  [hier](https://www.luis.ai/) meer over LUIS.</span><span class="sxs-lookup"><span data-stu-id="24dea-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="24dea-151">De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit).</span><span class="sxs-lookup"><span data-stu-id="24dea-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="24dea-152">Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/) van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery.</span><span class="sxs-lookup"><span data-stu-id="24dea-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="24dea-153">Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="24dea-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="24dea-154">De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="24dea-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="24dea-155">Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="24dea-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="24dea-156">De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering.</span><span class="sxs-lookup"><span data-stu-id="24dea-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="24dea-157">Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="24dea-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="24dea-158">Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="24dea-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="24dea-159">Microsoft Teams, Azure Event Grid en Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="24dea-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="24dea-160">Bij gebruik van de app Dynamics 365 Human Resources in Microsoft Teams kunnen bepaalde klantgegevens buiten het geografische gebied stromen waarin de Human Resources-service van de tenant is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="24dea-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="24dea-161">Dynamics 365 Human Resources verzendt het verlofverzoek van de werknemer en de werkstroomtaakgegevens naar Microsoft Azure Event Grid en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="24dea-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="24dea-162">Deze gegevens kunnen maximaal 24 uur worden opgeslagen in Microsoft Azure Event Grid en worden verwerkt in de Verenigde Staten, worden in transit en in rusttoestand versleuteld en worden niet door Microsoft of haar subverwerkers gebruikt voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="24dea-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="24dea-163">Zie [Locatie van gegevens in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) voor meer informatie over de opslag van uw gegevens in Teams.</span><span class="sxs-lookup"><span data-stu-id="24dea-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="24dea-164">Tijdens een conversatie met de chatbot in de app Human Resources kan de inhoud van de conversatie worden opgeslagen in Azure Cosmos DB en worden verzonden naar Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="24dea-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="24dea-165">Deze gegevens kunnen maximaal 24 uur in Azure Cosmos DB worden opgeslagen en kunnen worden verwerkt buiten het geografische gebied waar de Human Resources-service van uw tenant is geïmplementeerd, worden in transit en in rusttoestand versleuteld en worden niet gebruikt door Microsoft of haar subverwerkers voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="24dea-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="24dea-166">Zie [Locatie van gegevens in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) voor meer informatie over de opslag van uw gegevens in Teams.</span><span class="sxs-lookup"><span data-stu-id="24dea-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="24dea-167">Als u toegang tot de app Human Resources in Microsoft Teams wilt beperken voor uw organisatie of gebruikers in uw organisatie, raadpleegt u [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="24dea-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="24dea-168">Zie ook</span><span class="sxs-lookup"><span data-stu-id="24dea-168">See also</span></span> 

[<span data-ttu-id="24dea-169">Microsoft Teams downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="24dea-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="24dea-170">Microsoft Teams-helpcentrum</span><span class="sxs-lookup"><span data-stu-id="24dea-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="24dea-171">Verlofaanvragen beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="24dea-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

