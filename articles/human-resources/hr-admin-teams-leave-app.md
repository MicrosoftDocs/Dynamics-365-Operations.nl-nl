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
# <a name="human-resources-app-in-teams"></a>Human resources-app in Teams

[!include [banner](includes/preview-feature.md)]

Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunnen werknemers snel verlof aanvragen en informatie over hun verlofsaldo bekijken in Microsoft Teams. Werknemers kunnen communiceren met een bot om informatie aan te vragen. Het tabblad **Verlof** bevat meer gedetailleerde informatie.

![Bot voor verlof-app in Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Installeren en instellen

De Human resources-app is te vinden in het Teams-archief. Zie [Verlofaanvragen in Teams beheren](hr-teams-leave-app.md) voor meer informatie over het installeren van de Teams-app.

Zie [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) voor informatie over het beheren van app-machtigingen in Teams.

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Meldingen inschakelen voor de Human Resources-app in Teams

Als u wilt dat gebruikers meldingen over verlofaanvragen ontvangen in de Teams-app, moet u meldingen in Human Resources inschakelen.

>[!NOTE]
>Alleen gebruikers die zijn aangemeld bij Teams en de Teams-app Human Resources gebruiken, ontvangen meldingen.

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Selecteer **Koppelingen**.

3. Selecteer onder **Instellingen** de optie **Systeemparameters**.

4. Stel op het tabblad **Algemeen** de optie **Meldingen inschakelen voor Teams-app** op **Ja** in.

   ![Meldingen van Teams-app inschakelen in Systeemparameters](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Als u Teams-meldingen voor alle gebruikers wilt inschakelen, selecteert u **Ja** bij de prompt.

   ![Teams-meldingen inschakelen voor alle gebruikers](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Teams-meldingen in- of uitschakelen voor afzonderlijke gebruikers

Nadat u meldingen voor de Teams-app Human Resources teams hebt ingeschakeld, kunt u meldingen in- of uitschakelen voor afzonderlijke gebruikers.

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Selecteer **Koppelingen**.

3. Selecteer **Gebruikersopties** onder **Gebruikers**.

4. Selecteer het tabblad **Werkstroom**.

5. Stel **Meldingen inschakelen voor Teams-app** in op **Ja** als u meldingen voor de gebruiker wilt inschakelen of op **Nee** als u meldingen voor de gebruiker wilt uitschakelen.

   ![Meldingen in Teams-app inschakelen in gebruikersopties op het tabblad Werkstroom](./media/hr-admin-teams-leave-app-notifications.png)

6. Selecteer **Opslaan**.

## <a name="known-issues"></a>Bekende problemen

| Uitgeven | Status |
| --- | --- |
| Horizontaal schuiven werkt niet op Android-telefoons | Horizontaal schuiven is geen probleem op iOS- of bureaubladapparaten. Wij werken aan een oplossing voor Android. |
| Fout: er is een probleem met het vinden van een omgeving om verbinding mee te maken. | Dit foutbericht kan ook worden weergegeven als u hebt gecontroleerd of de gebruiker toegang heeft tot een of meer HRM-omgevingen. Ook ziet u mogelijk niet alle omgevingen die u verwacht. Tot wij dit probleem oplossen, kunt u dit probleem oplossen door de gebruiker te verwijderen en vervolgens opnieuw te importeren. |
| Het saldo is onjuist bij het indienen van verlof voor een toekomstige datum. | Prognose maken is nog niet beschikbaar. Het saldo wordt weergegeven voor de huidige datum. |
| Kan een aanvraag **Wordt gecontroleerd** niet annuleren. | Deze functionaliteit wordt momenteel niet ondersteund en wordt in een toekomstige versie toegevoegd. |
| Saldogegevens worden vanaf vandaag berekend. | Het systeem geeft momenteel geen saldi weer voor de toerekeningsperiode, zelfs als deze is geconfigureerd in de parameters voor verlof en verzuim. |

## <a name="privacy-notice"></a>Privacyverklaring

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen. De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS). Lees  [hier](https://www.luis.ai/) meer over LUIS. De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit). Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/) van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery. 

Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers. De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources. Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden. 

De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering. Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services. 

Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>Microsoft Azure Event Grid en Microsoft Teams

Wanneer u de meldingenfunctie voor de Dynamics 365 Human Resources-app in Teams gebruikt, stromen bepaalde klantgegevens buiten het geografische gebied waar de Human Resources-service van uw tenant is geïmplementeerd. Dynamics 365 Human Resources verzendt het verlofverzoek van de werknemer en de werkstroomtaakgegevens naar Microsoft Azure Event Grid en Microsoft Teams. Deze gegevens kunnen maximaal 24 uur worden opgeslagen en worden verwerkt in de Verenigde Staten, worden in transit en in rusttoestand versleuteld en worden niet door Microsoft of haar subverwerkers gebruikt voor opleidings- of serviceverbeteringen.

## <a name="see-also"></a>Zie ook 

[Microsoft Teams downloaden en installeren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-helpcentrum](https://support.office.com/teams)</br>
[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md)

