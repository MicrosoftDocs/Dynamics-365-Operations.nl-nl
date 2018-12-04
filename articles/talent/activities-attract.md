---
title: Activiteiten in de processen
description: Dit onderwerp biedt informatie over de verschillende soorten activiteiten die kunnen worden gebruikt in het aanstellingsproces.
author: 
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: ccd9e2d0ff1f7fb6825c6823936b4013b3054f5d
ms.contentlocale: nl-nl
ms.lasthandoff: 10/22/2018

---

# <a name="activities-in-the-hiring-processes"></a>Activiteiten in de aanstellingsprocessen

[!include[banner](../includes/banner.md)]

Activiteiten kunnen worden toegevoegd als een onderdeel van het aanstellingsproces in Microsoft Dynamics 365 for Talent: Attract. Activiteiten kunnen worden toegevoegd aan een processjabloon of kunnen rechtstreeks aan het aanstellingsproces in de functie worden toegevoegd. Wanneer een functie is gedefinieerd, wordt een processjabloon geselecteerd en worden de activiteiten die zijn opgenomen in de sjabloon, toegepast op de functie. Als geen sjabloon is geselecteerd, wordt de standaardsjabloon gebruikt. Het aanstellingsproces kan ook in de functie worden gewijzigd nadat de sjabloon is toegepast.

> [!NOTE] 
> Processjablonen zijn beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.

## <a name="prospect-activity"></a>Activiteit Prospect

De activiteit Prospect bepaalt of prospects kunnen worden toegevoegd aan een functie. Standaard kunnen prospects worden toegevoegd aan een functie. Als u de activiteit Prospect wilt uitschakelen, stelt u de optie **Prospects inschakelen** in op **Uit**. Als de activiteit Prospect is ingeschakeld, kunnen aanstellend managers prospects toevoegen en weergeven en wordt het tabblad **Prospect** weergegeven in de functie.

## <a name="application-activity"></a>Activiteit Sollicitatie

De activiteit Sollicitatie is vereist in de aanstellingsprocessjabloon. Als u e-mail naar kandidaten wilt verzenden wanneer ze hun sollicitatie indienen of worden toegevoegd aan de fase Sollicitatie, stelt u de optie **Mail aan kandidaat verzenden** in op **Aan**.

## <a name="scheduler-activity"></a>Planneractiviteit

De planneractiviteit is optioneel. Deze activiteit bestaat uit twee onderdelen: Beschikbaarheid van kandidaat en Planning. Met de component Beschikbaarheid van kandidaat kunt u e-mail gebruiken om te informeren naar de beschikbaarheid van een kandidaat. De component Planning biedt de mogelijkheid sollicitatiegesprekken met de kandidaat en het aanstellend team te plannen. In de planneractiviteit kunnen de volgende opties worden geconfigureerd: **Beschikbaarheid van kandidaat aanvragen**, **Online vergadering** en **Mail aan kandidaat verzenden**.

- Als u e-mail aan kandidaten wilt verzenden om te informeren naar hun beschikbaarheid, stelt u de optie **Beschikbaarheid van kandidaat aanvragen** in op **Aan**. Als u de optie instelt op **Uit**, wordt deze stap niet weergegeven in het aanstellingsproces voor de functie.
- Als u een live-stream of een telefonische vergadering wilt houden met Skype voor Bedrijven, stelt u het veld **Online vergadering** in op **Skype voor Bedrijven**. De juiste **Deelnemen aan Skype-vergadering**-koppeling wordt dan toegevoegd aan het interviewvergaderverzoek dat naar interviewers wordt verzonden.
- Als u e-mail aan kandidaten wilt verzenden om de planning te voltooien, stelt u de optie **Mail aan kandidaat verzenden** in op **Aan**. Als u de optie instelt op **Uit**, ontvangen kandidaten de planning van het sollicitatiegesprek alleen wanneer ze zich aanmelden bij de kandidaatportal.

## <a name="feedback-activity"></a>Activiteit Feedback

De feedbackactiviteit is optioneel. Met deze activiteit kunnen deelnemers aan sollicitatiegesprekken aanbevelingen voor een sollicitant invoeren. Ze kunnen ook eventuele opmerkingen met feedback invoeren. Als u de optie **Feedback deelnemers overnemen van aanstellingsteam** inschakelt, worden de werver, de aanstellend manager en de interviewers automatisch ingevoerd in de feedbackactiviteit. Organisaties kunnen interviewers toestaan de feedback van anderen weer te geven voordat ze hun eigen feedback indienen. Organisaties kunnen interviewers ook toestaan hun feedback te bewerken nadat zij deze hebben ingediend.

## <a name="interview-activity"></a>Interviewactiviteit

De interviewactiviteit is optioneel. Deze activiteit bestaat uit drie onderdelen: Beschikbaarheid van kandidaat, Planning en Feedback. Met de component Beschikbaarheid van kandidaat kunt u e-mail gebruiken om te informeren naar de beschikbaarheid van een kandidaat. De component Planning biedt de mogelijkheid sollicitatiegesprekken met de kandidaat en het aanstellend team te plannen. In de planneractiviteit kunnen de volgende opties worden geconfigureerd: **Beschikbaarheid van kandidaat aanvragen**, **Online vergadering** en **Mail aan kandidaat verzenden**.

- Als u e-mail aan kandidaten wilt verzenden om te informeren naar hun beschikbaarheid, stelt u de optie **Beschikbaarheid van kandidaat aanvragen** in op **Aan**. Als u de optie instelt op **Uit**, wordt deze stap niet weergegeven in het aanstellingsproces voor de functie.
- Als u een live-stream of een telefonische vergadering wilt houden met Skype voor Bedrijven, stelt u het veld **Online vergadering** in op **Skype voor Bedrijven**. De juiste **Deelnemen aan Skype-vergadering**-koppeling wordt dan toegevoegd aan het interviewvergaderverzoek.
- Als u e-mail aan kandidaten wilt verzenden om de planning te voltooien, stelt u de optie **Mail aan kandidaat verzenden** in op **Aan**. Als u de optie instelt op **Uit**, ontvangen kandidaten de planning van het sollicitatiegesprek alleen wanneer ze zich aanmelden bij de kandidaatportal.

Met de component Feedback kunnen mensen aanbevelingen voor een sollicitant doen. Ze kunnen ook eventuele opmerkingen met feedback invoeren. Als u de optie **Feedback deelnemers overnemen van aanstellingsteam** inschakelt, worden de werver, de aanstellend manager en de interviewers automatisch ingevoerd in het onderdeel Feedback. Organisaties kunnen interviewers toestaan de feedback van anderen weer te geven voordat ze hun eigen feedback indienen. Organisaties kunnen interviewers ook toestaan hun feedback te bewerken nadat zij deze hebben ingediend.

## <a name="powerapps-activity"></a>Activiteit PowerApps

Met de activiteit PowerApps kunt u een Microsoft PowerApps-app insluiten in uw aanstellingsproces. De app kan worden vereist voor alle sollicitanten, alleen interne sollicitanten, alleen externe sollicitanten of geen sollicitanten. Als de app is gemarkeerd als vereist, moet deze worden voltooid voordat naar de volgende fase kan worden gegaan. Als de app niet is gemarkeerd als vereist, is de activiteit een optionele stap en kan ook naar de volgende fase worden gegaan als de app niet is voltooid.

Als u de activiteit PowerApps wilt opslaan in het aanstellingsproces, moet u een PowerApps-id invoeren. Als u de PowerApps-id zoekt, gaat u naar [PowerApps](https://web.powerapps.com), selecteert u **Apps** en selecteert u vervolgens **Details**.

Als u de optie **Toevoegen van deelnemers aan deze activiteit toestaan** inschakelt, kunnen aanvullende bijdragers worden toegevoegd voor een sollicitatie die de PowerApps-activiteit gebruikt. Een organisatie heeft bijvoorbeeld een PowerApps-app gemaakt die een bibliotheek met sollicitatiegesprekvragen is voor technische rollen. De organisatie neemt nu een nieuwe softwareontwikkelaar aan en heeft de activiteit PowerApps toegevoegd aan het aanstellingsproces voor de rol Softwareontwikkelaar. Als de optie **Toevoegen van deelnemers aan deze activiteit toestaan** is ingeschakeld, kan een werver of aanstellend manager die een sollicitant bekijkt voor de rol Softwareontwikkelaar, personen aan de activiteit PowerApps toevoegen. Deze personen kunnen de app met de sollicitatiegesprekvragen vervolgens weergeven.

> [!NOTE]
> De activiteit PowerApps is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.

## <a name="youtube-activity"></a>YouTube-activiteit

Met de activiteit YouTube kunt u een YouTube-video delen als onderdeel van uw aanstellingsproces. Als u de activiteit YouTube wilt opslaan in het aanstellingsproces, moet u de URL van de YouTube-video opgeven. Net als bij de activiteit PowerApps kunt u toestaan dat deelnemers worden toegevoegd aan de activiteit. Als u de optie **Alleen aan kandidaat tonen** inschakelt, wordt de video alleen weergegeven als onderdeel van de kandidaatervaring. De video wordt niet weergegeven in het aanstellingsproces in Attract.

> [!NOTE]
> De activiteit YouTube is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.

## <a name="web-content-activity"></a>Activiteit Webinhoud

Met de activiteit Webinhoud kunt u online inhoud in uw aanstellingsproces insluiten. Als u de activiteit Webinhoud wilt opslaan in het aanstellingsproces, moet u de URL van de content opgeven. Net als bij de activiteit PowerApps en YouTube kunt u toestaan dat deelnemers worden toegevoegd aan de activiteit. Als u de optie **Alleen aan kandidaat tonen** inschakelt, wordt de inhoud alleen weergegeven als onderdeel van de kandidaatervaring. De video wordt niet weergegeven in het aanstellingsproces in Attract. U kunt de grootte selecteren van de inhoud die wordt weergegeven.

> [!NOTE]
> De activiteit Webinhoud is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.

## <a name="microsoft-forms-activity"></a>Activiteit Microsoft Forms

Met de activiteit Microsoft Forms kunt u een Microsoft Forms-formulier insluiten in uw aanstellingsproces. Met Microsoft Forms kunt u quizzen, enquêtes en opiniepeilingen maken. Als u de activiteit Microsoft Forms wilt opslaan in het aanstellingsproces, moet u de URL van het formulier opgeven. Net als bij de activiteit PowerApps, YouTube en Webinhoud kunt u toestaan dat deelnemers worden toegevoegd aan de activiteit. Als u de optie **Alleen aan kandidaat tonen** inschakelt, wordt het formulier alleen weergegeven als onderdeel van de kandidaatervaring. De video wordt niet weergegeven in het aanstellingsproces in Attract.

In Microsoft Forms kunnen auteurs hun instellingen wijzigen om gebruikers buiten hun organisatie te laten antwoorden op hun quiz of enquête. In dit geval dienen gebruikers antwoorden anoniem in. Als u wilt zien wie uw enquête of quiz heeft ingevuld, kunt u vereisen dat respondenten hun naam invoeren als onderdeel van de enquête of quiz.

> [!NOTE]
> De activiteit Microsoft Forms is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.

