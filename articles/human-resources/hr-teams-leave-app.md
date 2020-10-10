---
title: Verlofaanvragen beheren in Teams
description: In dit onderwerp wordt beschreven hoe u verlof kunt aanvragen in de Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: c7b74983cbddf661456b0a65939e272078d59f6d
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828939"
---
# <a name="manage-leave-requests-in-teams"></a>Verlofaanvragen beheren in Teams

[!include [banner](includes/preview-feature.md)]

Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunt u snel verlof aanvragen en informatie over uw verlofsaldo bekijken rechtstreeks vanuit Microsoft Teams. U kunt werken met een bot om informatie aan te vragen en een verlofaanvraag te starten. Het tabblad **Verlof** bevat meer gedetailleerde informatie. Daarnaast kunt u mensen informatie sturen over uw geplande verlof in teams en chats buiten de app Human Resources.

## <a name="install-the-app"></a>De app installeren

De Human resources-app is te vinden in het Teams-archief.

1. Selecteer de drie puntjes in Microsoft Teams.

   ![Drie puntjes in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. Zoek naar Dynamics 365 Human Resources en selecteer de tegel **Human resources**.

   ![HR-tegel van verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. Selecteer de knop **Toevoegen** om de app te installeren.

   ![Installatie van verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

Als u niet automatisch wordt aangemeld bij de app, selecteert u het tabblad **Instellingen** om zich aan te melden.

![Tabblad Instellingen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Als er geen dialoogvenster voor aanmelding wordt weergegeven, controleert u de instellingen van uw browser om pop-ups toe te staan. 

Als u toegang hebt tot meer dan één exemplaar van Human resources, kunt u de omgeving selecteren waarmee u verbinding wilt maken op het tabblad **Instellingen**.

> [!NOTE]
> De app ondersteunt nu de beveiligingsrol Systeembeheerder.
 
## <a name="use-the-bot"></a>De bot gebruiken

Na de installatie van de app wordt er een welkomstbericht weergegeven, zodat u weet welke acties de bot namens u kan ondernemen.

![Welkomstbericht in verlof-app voor Human Resource Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Bij het eerste contact met de bot moet u zich mogelijk aanmelden. Als er geen dialoogvenster voor aanmelding wordt weergegeven, controleert u de instellingen van uw browser om pop-ups toe te staan.

U kunt de bot vragen om het volgende te doen:

- Informatie over verlofsaldo weergeven voor elk verloftype waarvoor u zich hebt ingeschreven.

   ![Saldo weergeven in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- Aanvullende informatie weergeven over een bepaald verloftype.

   ![Details weergeven in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- Een verlofaanvraag voor u starten.

   ![Verlof aanvragen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
Nadat u een verlofaanvraag hebt gestart, kunt u de dagen direct in de kaart aanpassen.

![Aanvraag bewerken in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
Wanneer u klaar bent met het invoeren van gegevens, selecteert u **Verzenden** om deze ter goedkeuring in te dienen. U kunt ook **Opslaan als concept** selecteren als u later wilt terugkeren naar het concept.

![Aanvraag indienen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Uw verlof beheren in Teams

Op het tabblad **Verlof** kunt u het volgende bekijken:

- Saldo-informatie voor elk type verlof waarvoor u zich hebt ingeschreven

- Aanstaande verlofaanvragen

- Verlofaanvragen

- Conceptaanvragen voor verlof

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Een nieuwe aanvraag maken

1. Selecteer **Nieuwe aanvraag** om een nieuwe verlofaanvraag te maken.

   ![Nieuwe aanvraag in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Voer de dag of dagen in die u wilt vrijnemen en selecteer vervolgens **Toevoegen**.

   ![Verlof toevoegen in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Voer een redencode in, indien van toepassing. Voer ook eventuele opmerkingen in en voeg eventuele bijlagen toe.

4. Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen. U kunt ook **Opslaan als concept** opgeven als u later wilt terugkeren naar het concept.

### <a name="manage-draft-requests"></a>Conceptaanvragen beheren

1. Selecteer het tabblad **Concepten**.

   ![Tabblad Concepten in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. Selecteer het potlood om de aanvraag te bewerken of selecteer de prullenmand om de aanvraag te verwijderen.

3. Voer eventueel benodigde wijzigingen uit. Wanneer u klaar bent met het invoeren van gegevens, typt u **Verzenden** om deze ter goedkeuring in te dienen. U kunt ook **Opslaan als concept** selecteren als u later wilt terugkeren naar het concept.

   ![Concept bewerken in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a>Reageren op meldingen van teams

Wanneer u of een werknemer waarvoor u een fiatteur bent een verlofaanvraag indient, ontvangt u een melding in de Human Resources-app in Teams. U kunt de melding selecteren die u wilt weergeven. Meldingen worden ook weergegeven in het gebied **Chat**.

Als u een fiatteur bent, kunt u **Goedkeuren** of **Weigeren** selecteren in de melding. U kunt ook een optioneel bericht opgeven.

![Melding voor verlofaanvraag in Teams-app Human Resources](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Informatie over gepland verlof aan uw collega's verzenden

Nadat u de app Human Resources voor Teams hebt geïnstalleerd, kunt u eenvoudig informatie over uw gepland verlof aan uw collega's in teams of chats sturen.

1. Selecteer in een team of chat in Teams de knop Human Resources onder het chatvenster.

   ![Human Resources-knop onder chatvenster](./media/hr-teams-leave-app-chat-button.png)

2. Selecteer de verlofaanvraag die u wilt delen. Als u een conceptverlofaanvraag wilt delen, selecteert u eerst **Concepten**.

   ![Een aanvraag voor gepland verlof selecteren om te delen](./media/hr-teams-leave-app-chat-search.png)

Uw verlofaanvraag wordt in de chat weergegeven.

![Verlofaanvraagkaart Human Resources](./media/hr-teams-leave-app-chat-card.png)

Als u een conceptaanvraag hebt gedeeld, wordt deze als een concept weergegeven:

![Conceptverlofaanvraagkaart van Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>de verlofkalender van uw team weergeven

Als u een manager met directe ondergeschikten bent, kunt u de goedgekeurde en in behandeling zijnde verlofaanvragen van uw team bekijken.

1. Selecteer **Verlof** in de Human Resources-app in Teams.

2. Selecteer **Teamkalender**.

   ![Kalender weergeven in Teams-app Human Resources](./media/hr-teams-leave-app-view-calendar.png)

In de kalender worden de goedgekeurde en in behandeling zijnde verlofaanvragen van uw directe ondergeschikten weergegeven.

![Verlofkalender in Teams-app Human Resources](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a>Privacyverklaring

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen. De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS). Lees  [hier](https://www.luis.ai/) meer over LUIS. De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit). Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/) van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery. 

Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers. De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources. Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden. 

De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering. Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services. 

Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid en Azure Cosmos DB

Bij gebruik van de app Dynamics 365 Human Resources in Microsoft Teams kunnen bepaalde klantgegevens buiten het geografische gebied stromen waarin de Human Resources-service van de tenant is geïmplementeerd.

Dynamics 365 Human Resources verzendt het verlofverzoek van de werknemer en de werkstroomtaakgegevens naar Microsoft Azure Event Grid en Microsoft Teams. Deze gegevens kunnen maximaal 24 uur worden opgeslagen in Microsoft Azure Event Grid en worden verwerkt in de Verenigde Staten, worden in transit en in rusttoestand versleuteld en worden niet door Microsoft of haar subverwerkers gebruikt voor opleidings- of serviceverbeteringen. Zie [Locatie van gegevens in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) voor meer informatie over de opslag van uw gegevens in Teams.

Tijdens een conversatie met de chatbot in de app Human Resources kan de inhoud van de conversatie worden opgeslagen in Azure Cosmos DB en worden verzonden naar Microsoft Teams. Deze gegevens kunnen maximaal 24 uur in Azure Cosmos DB worden opgeslagen en kunnen worden verwerkt buiten het geografische gebied waar de Human Resources-service van uw tenant is geïmplementeerd, worden in transit en in rusttoestand versleuteld en worden niet gebruikt door Microsoft of haar subverwerkers voor opleidings- of serviceverbeteringen. Zie [Locatie van gegevens in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) voor meer informatie over de opslag van uw gegevens in Teams.
 
Als u toegang tot de app Human Resources in Microsoft Teams wilt beperken voor uw organisatie of gebruikers in uw organisatie, raadpleegt u [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Zie ook

[Microsoft Teams downloaden en installeren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-helpcentrum](https://support.office.com/teams)</br>
[Human Resources-app in Teams](hr-admin-teams-leave-app.md)
