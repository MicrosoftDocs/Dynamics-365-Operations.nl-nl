---
title: Activiteiten toevoegen aan een aanstellingsproces
description: Dit onderwerp biedt informatie over de verschillende soorten activiteiten die u kunt toevoegen aan een aanstellingsproces in Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833272"
---
# <a name="add-activities-to-a-hiring-process"></a>Activiteiten toevoegen aan een aanstellingsproces

[!include [banner](includes/banner.md)]

Activiteiten kunnen worden toegevoegd als een onderdeel van het aanstellingsproces in Microsoft Dynamics 365 Talent: Attract. Activiteiten kunnen worden toegevoegd aan een processjabloon of kunnen rechtstreeks aan het aanstellingsproces in de functie worden toegevoegd. Wanneer een functie is gedefinieerd, wordt een processjabloon geselecteerd en worden de activiteiten die zijn opgenomen in de sjabloon, toegepast op de functie. Als geen sjabloon is geselecteerd, wordt de standaardsjabloon gebruikt. Het aanstellingsproces kan ook in de functie worden gewijzigd nadat de sjabloon is toegepast.

> [!NOTE] 
> Processjablonen zijn beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen. Zie [Welke versie van Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md) voor meer informatie.

## <a name="prospect-activity"></a>Activiteit Prospect

De activiteit Prospect bepaalt of prospects kunnen worden toegevoegd aan een functie. Standaard kunnen prospects worden toegevoegd aan een functie. Als u de activiteit Prospect wilt uitschakelen, stelt u de optie **Prospects inschakelen** in op **Uit**. Als de activiteit Prospect is ingeschakeld, kunnen aanstellend managers prospects toevoegen en weergeven en wordt het tabblad **Prospect** weergegeven in de functie.

> [!NOTE]
> Als u wilt toestaan dat kandidaten aan een functie van LinkedIn kunnen worden toegevoegd, moet u de optie **Kandidaten inschakelen** instellen op **Aan**.

## <a name="application-activity"></a>Activiteit Sollicitatie

De activiteit Sollicitatie is vereist in de aanstellingsprocessjabloon. Als u e-mail naar kandidaten wilt verzenden wanneer ze hun sollicitatie indienen of worden toegevoegd aan de fase Sollicitatie, stelt u de optie **Mail aan kandidaat verzenden** in op **Aan**.

## <a name="interview-schedule-and-feedback-activity"></a>Planning van sollicitatiegesprekken en feedbackactiviteit

Deze activiteit bestaat uit drie onderdelen: Beschikbaarheid van kandidaat aanvragen, Planning en Feedback. Gebruik de sollicitatiegesprekactiviteit in de taaksjabloon als u de beschikbaarheidsaanvraag van de kandidaat, de planning en feedback wilt opnemen als onderdeel van het proces in plaats van deze afzonderlijk als onderdeel van het aanstellingsproces te gebruiken. Zie voor meer informatie [Plannen van sollicitatiegesprekken en feedback](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Power Apps-activiteit

Met de activiteit Power Apps kunt u een Microsoft Power Apps-app insluiten in uw aanstellingsproces. De app kan worden vereist voor alle sollicitanten, alleen interne sollicitanten, alleen externe sollicitanten of geen sollicitanten. Als de app is gemarkeerd als vereist, moet deze worden voltooid voordat naar de volgende fase kan worden gegaan. Om als voltooid te worden beschouwd, moet het veld **JobApplicationStatus** zijn ingesteld op **Voltooid**. Dit veld bevindt zich in de entiteit JobApplicationActivity. Dit veld moet dus met de Power Apps-app worden bijgewerkt voordat naar de volgende fase kan worden gegaan. Als de app niet is gemarkeerd als vereist, is de activiteit een optionele stap en kan ook naar de volgende fase worden gegaan als de app niet is voltooid.

Als u de activiteit Power Apps wilt opslaan in het aanstellingsproces, moet u een Power Apps-id invoeren. Als u de Power Apps-id zoekt, gaat u naar [Power Apps](https://web.powerapps.com), selecteert u **Apps** en vervolgens **Details**.

De Power Apps-activiteit is standaard beschikbaar voor de aanstellende manager, werver en hun gemachtigden. Als u de optie **Toevoegen van deelnemers aan deze activiteit toestaan** inschakelt, kunnen aanvullende deelnemers uit het aanstellingsteam worden toegevoegd voor een sollicitatie waarvoor de Power Apps-activiteit wordt gebruikt. Een organisatie heeft bijvoorbeeld een Power Apps-app gemaakt die een bibliotheek met sollicitatiegesprekvragen is voor technische rollen. De organisatie neemt nu een nieuwe softwareontwikkelaar aan en heeft de activiteit Power Apps toegevoegd aan het aanstellingsproces voor de rol Softwareontwikkelaar. Als de optie **Toevoegen van deelnemers aan deze activiteit toestaan** is ingeschakeld, kan een werver of aanstellend manager die een sollicitant bekijkt voor de rol Softwareontwikkelaar, interviewers aan de Power Apps-activiteit toevoegen. Deze personen kunnen de app met de sollicitatiegesprekvragen vervolgens weergeven.

> [!NOTE]
> De Power Apps-activiteit is alleen beschikbaar met de uitgebreide invoegtoepassing voor aanstellingen. Zie [Welke versie van Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md) voor meer informatie.

## <a name="youtube-activity"></a>YouTube-activiteit

Met de YouTube-activiteit kunt u een YouTube-video delen als onderdeel van uw aanstellingsproces. Als u de YouTube-activiteit wilt opslaan in het aanstellingsproces, moet u de URL van de YouTube-video opgeven. U kunt ervoor kiezen de inhoud weer te geven voor **Aanstellingsteam**, **Alleen interne kandidaten**, **Alleen externe kandidaten** of **Alle kandidaten**. Net als bij de Power Apps-activiteit kunt u toestaan dat deelnemers van het aanstellingsteam worden toegevoegd aan de activiteit. Als u ervoor kiest de inhoud aan kandidaten weer te geven, wordt de video alleen weergegeven als onderdeel van de kandidaatervaring en niet in het aanstellingsproces.

> [!NOTE]
> De YouTube-activiteit is alleen beschikbaar met de uitgebreide invoegtoepassing voor aanstellingen. Zie [Welke versie van Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md) voor meer informatie.

## <a name="web-content-activity"></a>Activiteit Webinhoud

Met de activiteit Webinhoud kunt u online inhoud in uw aanstellingsproces insluiten. Als u de activiteit Webinhoud wilt opslaan in het aanstellingsproces, moet u de URL van de content opgeven. U kunt ervoor kiezen de inhoud weer te geven voor **Aanstellingsteam**, **Alleen interne kandidaten**, **Alleen externe kandidaten** of **Alle kandidaten**. Net als bij de Power Apps- en YouTube-activiteiten kunt u toestaan dat deelnemers van het aanstellingsteam worden toegevoegd aan de activiteit. Als u ervoor kiest de inhoud aan kandidaten weer te geven, wordt de webinhoud alleen weergegeven als onderdeel van de kandidaatervaring en niet in het aanstellingsproces. U kunt de grootte kiezen van de inhoud die wordt weergegeven.

> [!NOTE]
> De activiteit Webinhoud is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen. Zie [Welke versie van Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md) voor meer informatie.

## <a name="microsoft-forms-activity"></a>Activiteit Microsoft Forms

Met de activiteit Microsoft Forms kunt u een Microsoft Forms-activiteit insluiten in uw aanstellingsproces. Met Microsoft Forms kunt u quizzen, enquêtes en opiniepeilingen maken. Als u de activiteit Microsoft Forms wilt opslaan in het aanstellingsproces, moet u de URL van het formulier opgeven. U kunt ervoor kiezen de inhoud weer te geven voor **Aanstellingsteam**, **Alleen interne kandidaten**, **Alleen externe kandidaten** of **Alle kandidaten**. Net als bij de Power Apps-, YouTube- en Webinhoud-activiteiten kunt u toestaan dat deelnemers van het aanstellingsteam worden toegevoegd aan de activiteit. Als u ervoor kiest de inhoud aan kandidaten weer te geven, wordt het formulier alleen weergegeven als onderdeel van de kandidaatervaring en niet in het aanstellingsproces.

In Microsoft Forms kunnen auteurs hun instellingen wijzigen om gebruikers buiten hun organisatie te laten antwoorden op hun quiz of enquête. In dit geval dienen gebruikers antwoorden anoniem in. Als u wilt zien wie uw enquête of quiz heeft ingevuld, kunt u vereisen dat respondenten hun naam invoeren als onderdeel van de enquête of quiz.

> [!NOTE]
> De activiteit Microsoft Forms is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen. Zie [Welke versie van Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md) voor meer informatie.

## <a name="offer-activity"></a>Aanbiedingsactiviteit

Voor de aanstellingsprocessjabloon is de aanbiedingsactiviteit vereist. Als u de geïntegreerde app voor aanbiedingsbeheer wilt gebruiken, stelt u **Aanbiedingsbeheer-app starten bij voorbereiden van aanbieding** naar **Aan**. Als deze instelling is uitgeschakeld, wordt de kandidaat niet weergegeven in de app Aanbieding. U moet updates voor de aanbiedingsactiviteit van een kandidaat dus handmatig bijhouden. Als wilt definiëren of aanstellende managers de aanbieding voor de kandidaat in de app Aanbieding kunnen voorbereiden, stelt u **Aanstellende managers kunnen aanbieding voorbereiden** in op **Aan**. Als aan de functie meerdere posities zijn gekoppeld, kunt u bepalen of u meerdere aanbiedingen voor hetzelfde positienummer wilt voorbereiden. Als u slechts één aanbieding per positie per functie wilt toestaan, stelt u **Toestaan dat posities opnieuw kunnen worden gebruikt binnen een functie** in op **Uit**.

> [!NOTE]
> De geïntegreerde app Aanbiedingsbeheer is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen. Zie [Welke versie van Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md) voor meer informatie.


