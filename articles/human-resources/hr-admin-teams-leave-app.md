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
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776303"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="55edf-103">Human resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="55edf-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="55edf-104">Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunnen werknemers snel verlof aanvragen en informatie over hun verlofsaldo bekijken in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="55edf-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="55edf-105">Werknemers kunnen communiceren met een bot om informatie aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="55edf-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="55edf-106">Het tabblad **Verlof** bevat meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="55edf-106">The **Time off** tab provides more detailed information.</span></span>

![Bot voor verlof-app in Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="55edf-109">Installeren en instellen</span><span class="sxs-lookup"><span data-stu-id="55edf-109">Install and setup</span></span>

<span data-ttu-id="55edf-110">De Human resources-app is te vinden in het Teams-archief.</span><span class="sxs-lookup"><span data-stu-id="55edf-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="55edf-111">Zie [Verlofaanvragen in Teams beheren](hr-teams-leave-app.md) voor meer informatie over het installeren van de Teams-app.</span><span class="sxs-lookup"><span data-stu-id="55edf-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="55edf-112">Zie [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) voor informatie over het beheren van app-machtigingen in Teams.</span><span class="sxs-lookup"><span data-stu-id="55edf-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="55edf-113">Meldingen inschakelen voor de Human Resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="55edf-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="55edf-114">Als u wilt dat gebruikers meldingen over verlofaanvragen ontvangen in de Teams-app, moet u meldingen in Human Resources inschakelen.</span><span class="sxs-lookup"><span data-stu-id="55edf-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="55edf-115">Alleen gebruikers die zijn aangemeld bij Teams en de Teams-app Human Resources gebruiken, ontvangen meldingen.</span><span class="sxs-lookup"><span data-stu-id="55edf-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="55edf-116">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="55edf-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="55edf-117">Selecteer **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="55edf-117">Select **Links**.</span></span>

3. <span data-ttu-id="55edf-118">Selecteer onder **Instellingen** de optie **Systeemparameters**.</span><span class="sxs-lookup"><span data-stu-id="55edf-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="55edf-119">Stel op het tabblad **Algemeen** de optie **Meldingen inschakelen voor Teams-app** op **Ja** in.</span><span class="sxs-lookup"><span data-stu-id="55edf-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Meldingen van Teams-app inschakelen in Systeemparameters](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="55edf-121">Als u Teams-meldingen voor alle gebruikers wilt inschakelen, selecteert u **Ja** bij de prompt.</span><span class="sxs-lookup"><span data-stu-id="55edf-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Teams-meldingen inschakelen voor alle gebruikers](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="55edf-123">Teams-meldingen in- of uitschakelen voor afzonderlijke gebruikers</span><span class="sxs-lookup"><span data-stu-id="55edf-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="55edf-124">Nadat u meldingen voor de Teams-app Human Resources teams hebt ingeschakeld, kunt u meldingen in- of uitschakelen voor afzonderlijke gebruikers.</span><span class="sxs-lookup"><span data-stu-id="55edf-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="55edf-125">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="55edf-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="55edf-126">Selecteer **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="55edf-126">Select **Links**.</span></span>

3. <span data-ttu-id="55edf-127">Selecteer **Gebruikersopties** onder **Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="55edf-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="55edf-128">Selecteer het tabblad **Werkstroom**.</span><span class="sxs-lookup"><span data-stu-id="55edf-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="55edf-129">Stel **Meldingen inschakelen voor Teams-app** in op **Ja** als u meldingen voor de gebruiker wilt inschakelen of op **Nee** als u meldingen voor de gebruiker wilt uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="55edf-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Meldingen in Teams-app inschakelen in gebruikersopties op het tabblad Werkstroom](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="55edf-131">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="55edf-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="55edf-132">Bekende problemen</span><span class="sxs-lookup"><span data-stu-id="55edf-132">Known issues</span></span>

| <span data-ttu-id="55edf-133">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="55edf-133">Issue</span></span> | <span data-ttu-id="55edf-134">Status</span><span class="sxs-lookup"><span data-stu-id="55edf-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="55edf-135">Horizontaal schuiven werkt niet op Android-telefoons</span><span class="sxs-lookup"><span data-stu-id="55edf-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="55edf-136">Horizontaal schuiven is geen probleem op iOS- of bureaubladapparaten.</span><span class="sxs-lookup"><span data-stu-id="55edf-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="55edf-137">Wij werken aan een oplossing voor Android.</span><span class="sxs-lookup"><span data-stu-id="55edf-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="55edf-138">Fout: er is een probleem met het vinden van een omgeving om verbinding mee te maken.</span><span class="sxs-lookup"><span data-stu-id="55edf-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="55edf-139">Dit foutbericht kan ook worden weergegeven als u hebt gecontroleerd of de gebruiker toegang heeft tot een of meer HRM-omgevingen.</span><span class="sxs-lookup"><span data-stu-id="55edf-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="55edf-140">Ook ziet u mogelijk niet alle omgevingen die u verwacht.</span><span class="sxs-lookup"><span data-stu-id="55edf-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="55edf-141">Tot wij dit probleem oplossen, kunt u dit probleem oplossen door de gebruiker te verwijderen en vervolgens opnieuw te importeren.</span><span class="sxs-lookup"><span data-stu-id="55edf-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="55edf-142">Het saldo is onjuist bij het indienen van verlof voor een toekomstige datum.</span><span class="sxs-lookup"><span data-stu-id="55edf-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="55edf-143">Prognose maken is nog niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="55edf-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="55edf-144">Het saldo wordt weergegeven voor de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="55edf-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="55edf-145">Kan een aanvraag **Wordt gecontroleerd** niet annuleren.</span><span class="sxs-lookup"><span data-stu-id="55edf-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="55edf-146">Deze functionaliteit wordt momenteel niet ondersteund en wordt in een toekomstige versie toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="55edf-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="55edf-147">Saldogegevens worden vanaf vandaag berekend.</span><span class="sxs-lookup"><span data-stu-id="55edf-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="55edf-148">Het systeem geeft momenteel geen saldi weer voor de toerekeningsperiode, zelfs als deze is geconfigureerd in de parameters voor verlof en verzuim.</span><span class="sxs-lookup"><span data-stu-id="55edf-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="55edf-149">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="55edf-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="55edf-150">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="55edf-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="55edf-151">Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="55edf-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="55edf-152">De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="55edf-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="55edf-153">Lees  [hier](https://www.luis.ai/) meer over LUIS.</span><span class="sxs-lookup"><span data-stu-id="55edf-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="55edf-154">De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit).</span><span class="sxs-lookup"><span data-stu-id="55edf-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="55edf-155">Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/) van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery.</span><span class="sxs-lookup"><span data-stu-id="55edf-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="55edf-156">Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="55edf-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="55edf-157">De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="55edf-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="55edf-158">Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="55edf-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="55edf-159">De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering.</span><span class="sxs-lookup"><span data-stu-id="55edf-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="55edf-160">Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="55edf-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="55edf-161">Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="55edf-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="55edf-162">Microsoft Azure Event Grid en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="55edf-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="55edf-163">Wanneer u de meldingenfunctie voor de Dynamics 365 Human Resources-app in Teams gebruikt, stromen bepaalde klantgegevens buiten het geografische gebied waar de Human Resources-service van uw tenant is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="55edf-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="55edf-164">Dynamics 365 Human Resources verzendt het verlofverzoek van de werknemer en de werkstroomtaakgegevens naar Microsoft Azure Event Grid en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="55edf-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="55edf-165">Deze gegevens kunnen maximaal 24 uur worden opgeslagen en worden verwerkt in de Verenigde Staten, worden in transit en in rusttoestand versleuteld en worden niet door Microsoft of haar subverwerkers gebruikt voor opleidings- of serviceverbeteringen.</span><span class="sxs-lookup"><span data-stu-id="55edf-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="55edf-166">Zie ook</span><span class="sxs-lookup"><span data-stu-id="55edf-166">See also</span></span> 

[<span data-ttu-id="55edf-167">Microsoft Teams downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="55edf-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="55edf-168">Microsoft Teams-helpcentrum</span><span class="sxs-lookup"><span data-stu-id="55edf-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="55edf-169">Verlofaanvragen beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="55edf-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

