---
title: Kandidaten zoeken met LinkedIn Recruiter in Microsoft Dynamics 365 for Talent - Attract
description: Gebruik de LinkedIn-integratie van Microsoft Dynamics 365 for Talent - Attract om kandidaten te zoeken via LinkedIn Recruiter.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 14aba16fa81a8f25d0f88247319254407d428b2a
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739444"
---
# <a name="source-candidates-with-linkedin-recruiter"></a>Kandidaten zoeken met LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn is het grootste onlinenetwerk voor professionals ter wereld en biedt u toegang tot de beste talenten wereldwijd. Met Microsoft Dynamics 365 for Talent: Attract kunt u kandidaten rechtstreeks vanuit LinkedIn zoeken. Het is dus eenvoudiger dan ooit om het talent te vinden dat u nodig hebt om uw openstaande posities in te vullen. Nadat u de verbinding met LinkedIn hebt ingesteld via Attract, kunt u potentiële LinkedIn-kandidaten voor uw posities weergeven en deze met slechts één klik exporteren in Attract.

Neem contact op met uw beheerder als u niet over deze mogelijkheid lijkt te beschikken. Voordat u optimaal gebruik kunt maken van LinkedIn Recruiter van Attract, moet uw beheerder de [integratie met LinkedIn instellen](./attract-admin-linkedin.md). U kunt vervolgens de verbinding met LinkedIn Recruiter instellen en beginnen met het zoeken naar kandidaten.

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>Uw verbinding met LinkedIn Recruiter instellen

Voordat u met LinkedIn Recruiter kunt werken via Attract, moet u de verbinding met LinkedIn Recruiter instellen. Voor deze stap hebt u uw LinkedIn Recruiter-referenties nodig.

1. Selecteer de knop **Instellingen** (tandwielpictogram) in de rechterbovenhoek van de pagina.
2. Selecteer **Gebruikersinstellingen**.
3. Selecteer op het tabblad **Verbindingen** de optie **Verbinden** naast **LinkedIn**. Volg de instructies van LinkedIn.

    ![[Verbinding met LinkedIn Recruiter instellen vanuit Attract](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>LinkedIn-kandidaten weergeven in Attract

Nadat u verbinding hebt gemaakt met LinkedIn Recruiter, kunt u de LinkedIn-profielen van de kandidaten weergeven in Attract.

1. Selecteer in Attract de optie **Functies** of **Talentenpools** links en selecteer vervolgens een sollicitant.

    ![[LinkedIn-kandidaten weergeven in Attract](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. Selecteer in het profiel van de kandidaat het tabblad **LinkedIn**. U kunt het profiel van de kandidaat, de InMail-historie en historie van LinkedIn-notities weergeven.

Hier kunt u de kandidaat opslaan in een LinkedIn Recruiter-project, inMail verzenden of Update Me gebruiken om een waarschuwing in te stellen in LinkedIn Recruiter.

> [!NOTE]
> Het LinkedIn-profiel van een kandidaat wordt weergegeven in Attract als de informatie van de kandidaat overeenkomt met de LinkedIn-gegevens. Hierbij worden de volgende vergelijkingsregels gebruikt:
> 
> 1. Als het e-mail adres en de LinkedIn-id overeenkomen in Attract en LinkedIn, wordt het profiel van de kandidaat weergegeven. Kandidaten hebben nog steeds de optie om hun LinkedIn-profiel te koppelen of ontkoppelen in Attract.
> 2. Als het e-mail adres of de id van het LinkedIn-lid niet overeenkomt, wordt een lijst met mogelijke kandidaten weergegeven. U kunt vervolgens een kandidaat selecteren in de lijst en het profiel koppelen.
> 3. Als er geen goede overeenkomsten zijn, ontvangt u een melding dat er geen overeenkomst is gevonden.

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a>LinkedIn-kandidaten met één klik naar Attract exporteren

Wanneer u kandidaten in LinkedIn Recruiter bekijkt, kunt u deze exporteren naar vacatures die u momenteel hebt geopend in Attract. Voor deze stap hebt u machtigingen als werver of aanstellend manager nodig in Attract. Zie voor meer informatie over rollen in Attract [Beveiliging en rollenbeheer in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).

U moet er ook voor zorgen dat de functie ook een fase Prospect heeft. Zie [Activiteit Prospect](./activities-attract.md#prospect-activity) voor meer informatie.

1. Maak in Attract een functie, wijs de juiste rollen toe en activeer de functie.
2. Zoek in LinkedIn Recruiter een goede kandidaat voor de functie en ga naar het profiel van de kandidaat.
3. Zoek de functie met het functiezoekvak op de contactkaart aan de hand van de titel of de functie-id die is geactiveerd in Attract. Als u de functie niet kunt vinden, selecteert u **ATS wijzigen** om het juiste Attract-exemplaar te zoeken.
4. Selecteer de functie en selecteer **Exporteren**.
5. Open de functie in Attract. De geëxporteerde kandidaat wordt weergegeven op het tabblad **Prospect** van de functie.

## <a name="view-attract-information-in-linkedin-recruiter"></a>Attract-gegevens weergeven in LinkedIn Recruiter

In LinkedIn Recruiter kunt u bijhouden of een kandidaat op andere functies in uw organisatie heeft gesolliciteerd, kijken waar de kandidaat zich bevindt in de verschillende fasen van sollicitaties en feedback en opmerkingen uit Attract lezen.

1. Open LinkedIn Recruiter en selecteer een kandidaatprofiel.
2. Beweeg de muisaanwijzer over **In ATS**.
3. Selecteer een van de volgende opties om de kandidaatgegevens weer te geven die zijn opgeslagen in Attract:

    - **Functies en statussen**: zie van welke functies de kandidaat deel uitmaakt, de laatste status en de voortgang van de kandidaat voor elke functie.
    - **Feedback sollicitatiegesprek**: bekijk de feedback die interviewers in Attract hebben ingediend.
    - **Notities**: zie welke notities voor deze kandidaat zijn ingevoerd in Attract.

    ![[Attract-gegevens weergeven vanuit LinkedIn Recruiter](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> Kandidaats- en sollicitatiegegevens worden niet gesynchroniseerd met LinkedIn Recruiter als de kandidaat de prospectfase niet voorbijkomt.

## <a name="view-linkedin-talent-pools"></a>LinkedIn-talentenpools weergeven

Als kandidaten ermee instemmen hun LinkedIn-profielen te delen met gebruikers in uw organisatie, wordt een nieuwe kandidaatrecord gemaakt in Attract. Deze kandidaten worden vervolgens weergegeven in een door het systeem gemaakte LinkedIn-talentenpool.

1. Selecteer in Attract de optie **Talentenpools** links.
2. Selecteer de LinkedIn-talentenpool. U ziet een lijst met kandidaten en hun stubprofielen van LinkedIn. Stubprofielen bevatten de voor- en achternaam en het e-mail adres van de kandidaat, als de kandidaat ervoor heeft gekozen om deze te delen.

## <a name="see-also"></a>Zie ook

[Veelgestelde vragen over LinkedIn](./attract-linkedin-faq.md)

[Integratie met LinkedIn instellen](./attract-admin-linkedin.md)

[Vacatures maken](./creating-jobs-attract.md)

[Vacatures plaatsen op LinkedIn vanuit Attract](./attract-post-jobs-to-linkedin.md)

[Problemen met integratie met LinkedIn oplossen](./attract-troubleshoot-linkedin.md)
