---
title: Human resources-app in Teams
description: In dit onderwerp maakt u kennis met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431125"
---
# <a name="human-resources-app-in-teams"></a>Human resources-app in Teams

[!include [banner](includes/preview-feature.md)]

Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunnen werknemers snel verlof aanvragen en informatie over hun verlofsaldo bekijken in Microsoft Teams. Werknemers kunnen communiceren met een bot om informatie aan te vragen. Het tabblad **Verlof** bevat meer gedetailleerde informatie.

![Bot voor verlof-app in Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Installeren en instellen

De Human resources-app is te vinden in het Teams-archief. Zie [Verlofaanvragen in Teams beheren](hr-teams-leave-app.md) voor meer informatie over het installeren van de Teams-app.

Zie [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) voor informatie over het beheren van app-machtigingen in Teams.

## <a name="known-issues"></a>Bekende problemen

| Uitgeven | Status |
| --- | --- |
| Fout: er is een probleem met het vinden van een omgeving om verbinding mee te maken. | Dit foutbericht kan ook worden weergegeven als u hebt gecontroleerd of de gebruiker toegang heeft tot een of meer HRM-omgevingen. Bovendien ziet u mogelijk niet alle omgevingen die u verwacht. Tot wij dit probleem oplossen, kunt u dit probleem oplossen door de gebruiker te verwijderen en vervolgens opnieuw te importeren. |
| Het saldo is onjuist bij het indienen van verlof voor een toekomstige datum. | Prognose maken is nog niet beschikbaar. Het saldo wordt weergegeven voor de huidige datum. |
| Bij het verminderen van het aantal uren in een bestaande aanvraag gaat het **Resterende saldo** omlaag in plaats van omhoog. | Dit bekende probleem wordt in de toekomst verholpen. De weergave is onjuist, maar de juiste bedragen worden aangepast bij het indienen. |
| Twee kaarten **Aanstaand verlof** worden weergegeven voor dezelfde datums. | De kaarten vertegenwoordigen afzonderlijke indieningen. We blijven feedback accepteren en wijzigingen aanbrengen. |
| Kan een aanvraag **Wordt gecontroleerd** niet annuleren. | Deze functionaliteit wordt momenteel niet ondersteund en wordt in een toekomstige versie toegevoegd. |
| Saldogegevens worden vanaf vandaag berekend. | Het systeem geeft momenteel geen saldi weer voor de toerekeningsperiode, zelfs als deze is geconfigureerd in de parameters voor verlof en verzuim. |

## <a name="privacy-notice"></a>Privacyverklaring

Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen. De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS). Lees  [hier](https://www.luis.ai/) meer over LUIS. De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit). Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/)  van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery. 

Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers. De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources. Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden. 

De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering. Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services. 

Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Zie ook 

[Microsoft Teams downloaden en installeren](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams-helpcentrum](https://support.office.com/teams)</br>
[Verlofaanvragen beheren in Teams](hr-teams-leave-app.md)

