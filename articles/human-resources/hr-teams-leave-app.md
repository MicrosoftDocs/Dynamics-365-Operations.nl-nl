---
title: Verlofaanvragen beheren in Teams
description: In dit onderwerp wordt beschreven hoe u verlof kunt aanvragen in de Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: b3daa76385518ad4c7150fa93ce33be0351bfd57
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428823"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="5140d-103">Verlofaanvragen beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="5140d-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5140d-104">Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunt u snel verlof aanvragen en informatie over uw verlofsaldo bekijken rechtstreeks vanuit Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5140d-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="5140d-105">U kunt communiceren met een bot om informatie aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="5140d-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="5140d-106">Het tabblad **Verlof** bevat meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="5140d-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="5140d-107">De app installeren</span><span class="sxs-lookup"><span data-stu-id="5140d-107">Install the app</span></span>

<span data-ttu-id="5140d-108">De Human resources-app is te vinden in het Teams-archief.</span><span class="sxs-lookup"><span data-stu-id="5140d-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="5140d-109">Selecteer de drie puntjes in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5140d-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Drie puntjes in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="5140d-111">Zoek naar Dynamics 365 Human Resources en selecteer de tegel **Human resources**.</span><span class="sxs-lookup"><span data-stu-id="5140d-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-tegel van verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="5140d-113">Selecteer de knop **Toevoegen** om de app te installeren.</span><span class="sxs-lookup"><span data-stu-id="5140d-113">Select the **Add** button to install the app.</span></span>

   ![Installatie van verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="5140d-115">Als u niet automatisch wordt aangemeld bij de app, selecteert u het tabblad **Instellingen** om zich aan te melden.</span><span class="sxs-lookup"><span data-stu-id="5140d-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Tabblad Instellingen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="5140d-117">Als er geen dialoogvenster voor aanmelding wordt weergegeven, controleert u de instellingen van uw browser om pop-ups toe te staan.</span><span class="sxs-lookup"><span data-stu-id="5140d-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="5140d-118">Als u toegang hebt tot meer dan één exemplaar van Human resources, kunt u de omgeving selecteren waarmee u verbinding wilt maken op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="5140d-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="5140d-119">De app biedt momenteel geen ondersteuning voor de beveiligingsrol van Systeembeheerder en er wordt een foutbericht weergegeven als u zich aanmeldt met een systeembeheerdersaccount.</span><span class="sxs-lookup"><span data-stu-id="5140d-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="5140d-120">Als u zich wilt aanmelden met een ander account, selecteert u op het tabblad **Instellingen** de knop **Van account wisselen** en meldt u zich vervolgens aan met een gebruikersaccount zonder systeembeheerdersbevoegdheden.</span><span class="sxs-lookup"><span data-stu-id="5140d-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="5140d-121">De bot gebruiken</span><span class="sxs-lookup"><span data-stu-id="5140d-121">Use the bot</span></span>

<span data-ttu-id="5140d-122">Na de installatie van de app wordt er een welkomstbericht weergegeven, zodat u weet welke acties de bot namens u kan ondernemen.</span><span class="sxs-lookup"><span data-stu-id="5140d-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Welkomstbericht in verlof-app voor Human Resource Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="5140d-124">Bij het eerste contact met de bot moet u zich mogelijk aanmelden.</span><span class="sxs-lookup"><span data-stu-id="5140d-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="5140d-125">Als er geen dialoogvenster voor aanmelding wordt weergegeven, controleert u de instellingen van uw browser om pop-ups toe te staan.</span><span class="sxs-lookup"><span data-stu-id="5140d-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="5140d-126">U kunt de bot vragen om het volgende te doen:</span><span class="sxs-lookup"><span data-stu-id="5140d-126">You can ask the bot to:</span></span>

- <span data-ttu-id="5140d-127">Informatie over verlofsaldo weergeven voor elk verloftype waarvoor u zich hebt ingeschreven.</span><span class="sxs-lookup"><span data-stu-id="5140d-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Saldo weergeven in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="5140d-129">Aanvullende informatie weergeven over een bepaald verloftype.</span><span class="sxs-lookup"><span data-stu-id="5140d-129">Show additional details about a specific leave type.</span></span>

   ![Details weergeven in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="5140d-131">Een verlofaanvraag voor u starten.</span><span class="sxs-lookup"><span data-stu-id="5140d-131">Start a leave request for you.</span></span>

   ![Verlof aanvragen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="5140d-133">Nadat u een verlofaanvraag hebt gestart, kunt u de dagen rechtstreeks vanaf de kaart aanpassen of kunt u **Details bewerken** selecteren om aanvullende informatie aan uw aanvraag toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="5140d-133">After you start a leave request, you can adjust the days right within the card, or you can select **Edit details** to add additional information to your request.</span></span>

![Aanvraag bewerken in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="5140d-135">Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="5140d-135">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="5140d-136">U kunt ook **Opslaan als concept** opgeven als u later wilt terugkeren naar het concept.</span><span class="sxs-lookup"><span data-stu-id="5140d-136">You can also type **Save as draft** to come back to it later.</span></span>

![Aanvraag indienen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="5140d-138">Uw verlof beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="5140d-138">Manage your leave in Teams</span></span>

<span data-ttu-id="5140d-139">Op het tabblad **Verlof** kunt u het volgende bekijken:</span><span class="sxs-lookup"><span data-stu-id="5140d-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="5140d-140">Saldo-informatie voor elk type verlof waarvoor u zich hebt ingeschreven</span><span class="sxs-lookup"><span data-stu-id="5140d-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="5140d-141">Aanstaande verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="5140d-141">Upcoming leave requests</span></span>

- <span data-ttu-id="5140d-142">Verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="5140d-142">Time-off requests</span></span>

- <span data-ttu-id="5140d-143">Conceptaanvragen voor verlof</span><span class="sxs-lookup"><span data-stu-id="5140d-143">Draft leave requests</span></span>

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="5140d-145">Een nieuwe aanvraag maken</span><span class="sxs-lookup"><span data-stu-id="5140d-145">Create a new request</span></span>

1. <span data-ttu-id="5140d-146">Selecteer **Nieuwe aanvraag** om een nieuwe verlofaanvraag te maken.</span><span class="sxs-lookup"><span data-stu-id="5140d-146">To create a new leave request, select **New request**.</span></span>

   ![Nieuwe aanvraag in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="5140d-148">Voer de dag of dagen in die u wilt vrijnemen en selecteer vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="5140d-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Verlof toevoegen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="5140d-150">Voer een redencode in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="5140d-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="5140d-151">Voer ook eventuele opmerkingen in en voeg eventuele bijlagen toe.</span><span class="sxs-lookup"><span data-stu-id="5140d-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="5140d-152">Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="5140d-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="5140d-153">U kunt ook **Opslaan als concept** opgeven als u later wilt terugkeren naar het concept.</span><span class="sxs-lookup"><span data-stu-id="5140d-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="5140d-154">Conceptaanvragen beheren</span><span class="sxs-lookup"><span data-stu-id="5140d-154">Manage draft requests</span></span>

1. <span data-ttu-id="5140d-155">Selecteer het tabblad **Concepten**.</span><span class="sxs-lookup"><span data-stu-id="5140d-155">Select the **Drafts** tab.</span></span>

   ![Tabblad Concepten in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="5140d-157">Selecteer het potlood om de aanvraag te bewerken of selecteer de prullenmand om de aanvraag te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="5140d-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="5140d-158">Voer eventueel benodigde wijzigingen uit.</span><span class="sxs-lookup"><span data-stu-id="5140d-158">Make any necessary changes.</span></span> <span data-ttu-id="5140d-159">Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen.</span><span class="sxs-lookup"><span data-stu-id="5140d-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="5140d-160">U kunt ook **Opslaan als concept** selecteren als u later wilt terugkeren naar het concept.</span><span class="sxs-lookup"><span data-stu-id="5140d-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Concept bewerken in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a><span data-ttu-id="5140d-162">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="5140d-162">Privacy notice</span></span>

<span data-ttu-id="5140d-163">Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="5140d-163">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="5140d-164">De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="5140d-164">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="5140d-165">Lees  [hier](https://www.luis.ai/) meer over LUIS.</span><span class="sxs-lookup"><span data-stu-id="5140d-165">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="5140d-166">De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit).</span><span class="sxs-lookup"><span data-stu-id="5140d-166">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="5140d-167">Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/)  van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery.</span><span class="sxs-lookup"><span data-stu-id="5140d-167">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="5140d-168">Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="5140d-168">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="5140d-169">De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5140d-169">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5140d-170">Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="5140d-170">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="5140d-171">De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering.</span><span class="sxs-lookup"><span data-stu-id="5140d-171">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="5140d-172">Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="5140d-172">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="5140d-173">Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="5140d-173">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="5140d-174">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5140d-174">See also</span></span>

[<span data-ttu-id="5140d-175">Microsoft Teams downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="5140d-175">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="5140d-176">Microsoft Teams-helpcentrum</span><span class="sxs-lookup"><span data-stu-id="5140d-176">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="5140d-177">Human resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="5140d-177">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
