---
title: Human resources-app in Teams
description: In dit onderwerp maakt u kennis met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3926acd07a68f59682c18f4f7bc290dc1e21d0b6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889735"
---
# <a name="human-resources-app-in-teams"></a>Human resources-app in Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunnen werknemers snel verlof aanvragen en informatie over hun verlofsaldo bekijken in Microsoft Teams. Werknemers kunnen communiceren met een bot om informatie aan te vragen. Het tabblad **Verlof** bevat meer gedetailleerde informatie. Daarnaast kunnen ze mensen informatie sturen over uw aanstaande verlof in teams en chats buiten de Human Resources-app.

![Bot voor verlof-app in Human Resources Teams](./media/hr-teams-leave-app-bot.png)

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Verlofaanvraagkaart Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Installeren en instellen

De Dynamics 365 Human Resources-app is te vinden in het Teams-archief. Zie [Verlofaanvragen in Teams beheren](hr-teams-leave-app.md) voor meer informatie over het installeren van de Teams-app.

Zie [Machtigingsbeleid voor apps beheren in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies) voor informatie over het beheren van app-machtigingen in Teams.

Als u wilt dat uw gebruikers de verlof- en verzuimkalender in de app bekijken, moet u de **Verlof- en verzuimkalender in Teams** in Functiebeheer inschakelen. Meer informatie over het inschakelen van functies vindt u in [Functies beheren](hr-admin-manage-features.md).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Meldingen inschakelen voor de Human Resources-app in Teams

Als u wilt dat gebruikers meldingen over verlofaanvragen ontvangen in de Teams-app, moet u meldingen in Dynamics 365 Human Resources inschakelen.

>[!NOTE]
>Alleen gebruikers die zijn aangemeld bij Teams en de Dynamics 365 Human Resources Teams-app gebruiken, ontvangen meldingen.

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Selecteer **Koppelingen**.

3. Selecteer onder **Instellingen** de optie **Systeemparameters**.

4. Stel op het tabblad **Algemeen** de optie **Meldingen inschakelen voor Teams-app** op **Ja** in.

   ![Meldingen van Teams-app inschakelen in Systeemparameters](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Als u Teams-meldingen voor alle gebruikers wilt inschakelen, selecteert u **Ja** bij de prompt.

   ![Teams-meldingen inschakelen voor alle gebruikers](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Teams-meldingen in- of uitschakelen voor afzonderlijke gebruikers

Nadat u meldingen voor de Dynamics 365 Human Resources Teams-app hebt ingeschakeld, kunt u meldingen in- of uitschakelen voor afzonderlijke gebruikers.

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Selecteer **Koppelingen**.

3. Selecteer **Gebruikersopties** onder **Gebruikers**.

4. Selecteer het tabblad **Werkstroom**.

5. Stel **Meldingen inschakelen voor Teams-app** in op **Ja** als u meldingen voor de gebruiker wilt inschakelen of op **Nee** als u meldingen voor de gebruiker wilt uitschakelen.

   ![Meldingen in Teams-app inschakelen in gebruikersopties op het tabblad Werkstroom](./media/hr-admin-teams-leave-app-notifications.png)

6. Selecteer **Opslaan**.

## <a name="supported-languages"></a>Ondersteunde talen

De Dynamics 365 Human Resources-app in Teams ondersteunt de volgende talen:

| Landinstellingen-id | Taal |
| --- | --- |
| de-DE | Duits (Duitsland) |
| es-ES | Spaans (Spanje) |
| es-MX | Spaans (Mexico) |
| fr-CA | Frans (Canada) |
| fr-FR | Frans (Frankrijk) |
| it-IT | Italiaans (Italië) |
| nl-NL | Nederlands (Nederland) |
| pt-BR | Portugees (Brazilië) |
| tr-TR | Turks (Turkije) |
| zh-CN | Chinees (vereenvoudigd) |

## <a name="notes"></a>Opmerkingen

De volgende werkitems staan op de planning voor toekomstige releases:

| Werkitem | Status |
| --- | --- |
| Het saldo is onjuist bij het indienen van verlof voor een toekomstige datum. | Prognose maken is nog niet beschikbaar. Het saldo wordt weergegeven voor de huidige datum. |
| Kan een aanvraag **Wordt gecontroleerd** niet annuleren. | Deze functionaliteit wordt momenteel niet ondersteund en wordt in een toekomstige versie toegevoegd. |
| Saldogegevens worden vanaf vandaag berekend. | Het systeem geeft momenteel geen saldi weer voor de toerekeningsperiode, zelfs als deze is geconfigureerd in de parameters voor verlof en verzuim. |

## <a name="troubleshooting"></a>Problemen oplossen

Als een gebruiker problemen heeft met het aanmelden bij of het gebruik van de Human Resources Teams-app, volgt u de onderstaande instructies voor het oplossen van problemen. Als u na het oplossen van problemen nog steeds problemen ondervindt, neemt u contact op met de ondersteuning. Zie voor meer informatie [Ondersteuning krijgen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Kan me niet aanmelden bij de Human Resources-app in Teams

Als een gebruiker contact met u opneemt omdat deze zich niet kan aanmelden bij de app, controleert u of de gebruiker een bijbehorende werknemersrecord heeft in Human Resources.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Fout bij het goedkeuren van verlofaanvragen in de Human Resources-app in Teams

Als gebruikers een foutmelding krijgen tijdens het goedkeuren van verlofaanvragen in de Teams-app, probeert u de volgende stappen voor het oplossen van problemen:

1. Controleer of hun Teams-account dezelfde is als de account die ze voor toegang tot Human Resources gebruiken.

2. Controleer of ze een geldige fiatteur zijn voor de aanvraag door de werkstroominstellingen te controleren op verlofgoedkeuring. Zie [Een werkstroom voor een verlofaanvraag maken](hr-leave-and-absence-workflow.md) voor meer informatie over werkstromen voor verlofaanvragen.

## <a name="privacy-notice"></a>Privacyverklaring

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen. De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS). Lees  [hier](https://www.luis.ai/) meer over LUIS. De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit). Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/) van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery. 

Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers. De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources. Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden. 

De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering. Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services. 

Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid en Azure Cosmos DB

Bij gebruik van de app Dynamics 365 Human Resources in Microsoft Teams kunnen bepaalde klantgegevens buiten het geografische gebied stromen waarin de Human Resources-service van de tenant is geïmplementeerd.

Dynamics 365 Human Resources verzendt het verlofverzoek van de werknemer en de werkstroomtaakgegevens naar Microsoft Azure Event Grid en Microsoft Teams. Deze gegevens kunnen maximaal 24 uur worden opgeslagen in Microsoft Azure Event Grid en worden verwerkt in de Verenigde Staten, worden in transit en in rusttoestand versleuteld en worden niet door Microsoft of haar subverwerkers gebruikt voor opleidings- of serviceverbeteringen. Zie [Locatie van gegevens in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide) voor meer informatie over de opslag van uw gegevens in Teams.

Tijdens een conversatie met de chatbot in de app Human Resources kan de inhoud van de conversatie worden opgeslagen in Azure Cosmos DB en worden verzonden naar Microsoft Teams. Deze gegevens kunnen maximaal 24 uur in Azure Cosmos DB worden opgeslagen en kunnen worden verwerkt buiten het geografische gebied waar de Human Resources-service van uw tenant is geïmplementeerd, worden in transit en in rusttoestand versleuteld en worden niet gebruikt door Microsoft of haar subverwerkers voor opleidings- of serviceverbeteringen. Zie [Locatie van gegevens in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide) voor meer informatie over de opslag van uw gegevens in Teams.
 
Als u toegang tot de app Human Resources in Microsoft Teams wilt beperken voor uw organisatie of gebruikers in uw organisatie, raadpleegt u [Machtigingsbeleid voor apps beheren in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Zie ook 

[Microsoft Teams downloaden en installeren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-helpcentrum](https://support.office.com/teams)</br>
[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]