---
title: Kandidaten zoeken met LinkedIn Recruiter in Attract
description: Gebruik de LinkedIn-integratie van Microsoft Dynamics 365 Talent - Attract om kandidaten te zoeken via LinkedIn Recruiter.
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
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
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528264"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a>Kandidaten zoeken met LinkedIn Recruiter in Attract

[!include [banner](includes/banner.md)]

LinkedIn is het grootste onlinenetwerk voor professionals ter wereld en biedt u toegang tot de beste talenten wereldwijd. Met Microsoft Dynamics 365 Talent: Attract kunt u kandidaten rechtstreeks vanuit LinkedIn zoeken. Het is dus eenvoudiger dan ooit om het talent te vinden dat u nodig hebt om uw openstaande posities in te vullen. Nadat u de verbinding met LinkedIn hebt ingesteld via Attract, kunt u potentiële LinkedIn-kandidaten voor uw posities weergeven en deze met slechts één klik exporteren in Attract.

Neem contact op met uw beheerder als u niet over deze mogelijkheid lijkt te beschikken. Voordat u optimaal gebruik kunt maken van LinkedIn Recruiter van Attract, moet uw beheerder de [integratie met LinkedIn instellen](./attract-admin-linkedin.md). U kunt vervolgens de verbinding met LinkedIn Recruiter instellen en beginnen met het zoeken naar kandidaten.

>[!IMPORTANT]
>Vanaf 1 juli 2020 wordt LinkedIn niet meer ondersteund door Internet Explorer 11. Gebruikers hebben nog steeds toegang tot LinkedIn met Internet Explorer 11, maar moeten een upgrade uitvoeren of een andere browser gebruiken. Zie [Ondersteunde internetbrowsers voor LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin) voor meer informatie.

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>Uw verbinding met LinkedIn Recruiter instellen

Voordat u met LinkedIn Recruiter kunt werken via Attract, moet u de verbinding met LinkedIn Recruiter instellen. Voor deze stap hebt u uw LinkedIn Recruiter-referenties nodig.

1. Selecteer de knop **Instellingen** (tandwielpictogram) in de rechterbovenhoek van de pagina.
2. Selecteer **Gebruikersinstellingen**.
3. Selecteer op het tabblad **Verbindingen** de optie **Verbinden** naast **LinkedIn**. Volg de instructies van LinkedIn.

    ![[Verbinding met LinkedIn Recruiter instellen vanuit Attract](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>LinkedIn-kandidaten weergeven in Attract

Nadat u verbinding hebt gemaakt met LinkedIn Recruiter, kunt u de LinkedIn-profielen van de kandidaten weergeven in Attract.

>[!NOTE]
>Als er een Recruiter-seat aan u is toegewezen, kunt u de volledige informatie over de kandidaten bekijken.<br><br>
>Als u een Hiring Manager-seat hebt of als er geen seat aan u is toegewezen, moet u zich afmelden bij LinkedIn of LinkedIn Recruiter voordat u naar het tabblad LinkedIn gaat om een kandidaat in Attract te zoeken. U kunt de basisgegevens van het openbare profiel van de kandidaat zien, zoals hun voor- en achternaam.

1. Selecteer in Attract de optie **Functies** of **Talentenpools** links en selecteer vervolgens een sollicitant.

    ![[LinkedIn-kandidaten weergeven in Attract](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. Selecteer in het profiel van de kandidaat het tabblad **LinkedIn**. U kunt het profiel van de kandidaat en de InMail-historie bekijken.

   ![De LinkedIn-gegevens van een kandidaat bekijken](./media/attract-candidate-linkedin-tab.png)

Van hieruit kunt u de volgende acties uitvoeren:

- Het tabblad **Wervingsactiviteiten** selecteren om weer te geven:
   
   - Wervingsnotities (zowel openbare als privé). Standaard zijn notities privé en alleen zichtbaar voor de eigenaar ervan.
   - InMail-activiteit (maar niet de InMail-inhoud). Scroll naar de onderkant van de pagina om de InMail-uitwisseling met uw prospect te bekijken en andere gebruikers in uw organisatie te bekijken die contact hebben gehad met uw prospect.
   - Afwijzingsactiviteit kandidaat

- Selecteer **Verzenden InMail** om InMail te versturen zonder Attract te verlaten.

- Selecteer **Opslaan onder vacature** om de vacature op te slaan zonder Attract te verlaten.

> [!NOTE]
> Het LinkedIn-profiel van een kandidaat wordt getoond in Attract als de informatie van de kandidaat overeenkomt met de LinkedIn-gegevens. Hierbij worden de volgende vergelijkingsregels gebruikt:
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

    ![[Attract-gegevens weergeven van LinkedIn Recruiter](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> Kandidaats- en sollicitatiegegevens worden niet gesynchroniseerd met LinkedIn Recruiter als de kandidaat de prospectfase niet voorbijkomt.

## <a name="view-linkedin-talent-pools"></a>LinkedIn-talentenpools weergeven

Als kandidaten ermee instemmen hun LinkedIn-profielen te delen met gebruikers in uw organisatie, wordt een nieuwe kandidaatrecord gemaakt in Attract. Deze kandidaten worden vervolgens weergegeven in een door het systeem gemaakte LinkedIn-talentenpool.

1. Selecteer in Attract de optie **Talentenpools** links.
2. Selecteer de LinkedIn-talentenpool. U ziet een lijst met kandidaten en hun stubprofielen van LinkedIn. Stubprofielen bevatten de voor- en achternaam en het e-mail adres van de kandidaat, als de kandidaat ervoor heeft gekozen om deze te delen.

## <a name="see-also"></a>Zie ook

[Veelgestelde vragen over integratie van Attract met LinkedIn](./attract-linkedin-faq.md)

[Integratie met LinkedIn instellen voor Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md)

[Functies maken, goedkeuren en boeken in Attract](./creating-jobs-attract.md)

[Vacatures plaatsen op LinkedIn vanuit Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md)

[Problemen met integratie met LinkedIn en Microsoft Dynamics 365 Talent - Attract oplossen](./attract-troubleshoot-linkedin.md)
