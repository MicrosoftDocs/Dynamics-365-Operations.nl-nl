---
title: Sourcing met LinkedIn Recruiter
description: Dit onderwerp biedt informatie over het gebruik van machine learning om aanbevelingen voor functies en functiekandidaten te krijgen.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
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
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517672"
---
# <a name="sourcing-with-linkedin-recruiter"></a>Sourcing met LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn is 's werelds grootste talentendatabase en vaak het primaire systeem dat wervers gebruiken om kandidaten te zoeken, mee te communiceren en aan te stellen voor de functies die wervers willen opvullen. LinkedIn Recruiter-integratie met Dynamics 365 for Talent: Attract maakt het eenvoudiger voor gebruikers om personen aan te stellen en de gegevens tussen twee systemen gesynchroniseerd te houden.

> [!NOTE]
> U hebt de Uitgebreide invoegtoepassing voor aanstellingen- en LinkedIn Recruiter-seats nodig om LinkedIn Recruiter-integratie met Attract te kunnen gebruiken.

## <a name="set-up-linkedin-recruiter-with-attract"></a>LinkedIn Recruiter met Attract instellen 

Voordat u de mogelijkheden van LinkedIn Recruiter kunt gebruiken, moet u toegang op contract- of bedrijfsniveau configureren met uw Attract-exemplaar. Als u het configuratieproces wilt voltooien, moet u werken met de gebruiker die een beheerder is in uw LinkedIn Recruiter-contract. Voer de volgende stappen uit voor het configureren van de LinkedIn Recruiter met Attract.

1.  Meld u aan bij Attract als beheerder en ga naar **Beheerinstellingen**.

2.  Klik in het linkerdeelvenster op het tabblad **LinkedIn-integratie**.

[![Attract-beheerweergave om LinkedIn Recruiter-integratie te starten](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Klik op **Verbinden** om de instelling te starten en te worden begeleid door het aanmeldingsproces voor LinkedIn.

4.  Als u seats in meerdere LinkedIn-contracten hebt, selecteert u het contract dat u wilt verbinden met het Attract-systeem. Als u een seat in slechts één LinkedIn-contract hebt, is deze stap niet nodig.

5.  De LinkedIn-widget wordt nu geladen in uw beheerinstellingen met de lijst van weergegeven integraties. Klik onder **Verbinding met Recruiter-systeem** op **Aanvragen**.

[![Attract-beheerweergave om LinkedIn Recruiter-integratie aan te vragen](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Nadat de integratie is aangevraagd vanuit Attract, wordt **Partner gereed** weergegeven en kan het worden ingeschakeld vanuit **Recruiter-beheerinstellingen**. Als u **Partner waarschuwen** op deze pagina ziet, wacht u enkele seconden, klikt u op **Partner waarschuwen** en vernieuwt u de pagina. Het wordt nu weergegeven als **Partner gereed**.

[![Attract-beheerweergave om aan te geven dat de Attract-zijde van aanvragen is voltooid](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Als u de volgende stap wilt uitvoeren, hebt u een beheerdersbevoegdheid nodig in uw LinkedIn Recruiter-contract.

7.  Meld u bij LinkedIn aan met het beheerdersaccount en ga rechtsboven naar LinkedIn Recruiter. 

8. Klik in het menu **meer** boven aan het scherm op **Beheerinstellingen** en klik vervolgens op het tabblad **ATS**.

Het Attract-systeem wordt weergegeven met een aantal opties die kunnen worden ingeschakeld.

9. Als u alleen met 1 klik exporteren voor de **In-ATS-indicator** en de **In-ATS-profielwidget** wilt inschakelen, selecteert u **Toegang op bedrijfsniveau**. Als u alle toegangsfuncties op bedrijfsniveau plus InMail-historie, notitiehistorie en de InMail-stub profieltoegang wilt inschakelen, selecteert u **Toegang op contractniveau**.

10. Schakel het gewenste toegangsniveau vanuit uw LinkedIn Recruiter **Admin-ATS**-instellingen in.

[![Attract-integratie inschakelen vanuit LinkedIn Recruiter-beheerweergave](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Ga terug naar de Attract-beheerinstellingen als AttractAdmin en selecteer het tabblad **LinkedIn integratie**. U moet nu bij laden van de LinkedIn-widget **Ingeschakeld** zien met het geselecteerde toegangsniveau ingeschakeld.

[![LinkedIn Recruiter-integratie voltooid](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>LinkedIn Recruiter-mogelijkheden gebruiken

Nadat LinkedIn Recruiter-mogelijkheden zijn ingeschakeld door de Attract-beheerder, is het beschikbaar voor toegang door aanstellend managers en wervers. Als u deze mogelijkheden wilt gebruiken, verbindt u uw LinkedIn-account onder **Gebruikersinstellingen**. Diverse mogelijkheden zijn beschikbaar nadat zowel de beheerders als gebruikersinstellingen zijn verbonden.

### <a name="in-ats-profile-widget"></a>In-ATS-profielwidget

U kunt het LinkedIn-profiel van de kandidaat in Attract weergeven. De LinkedIn-widget geeft het kandidaatprofiel weer wanneer de ATS-informatie overeenkomt met de LinkedIn-informatie van de gebruikers.

Als u een profiel wilt weergeven, gaat u naar het kandidaatprofiel vanuit een functie of talentenpool. Selecteer in het kandidaatprofiel het tabblad **LinkedIn** en de profielwidget wordt geladen. U kunt vanaf deze pagina ook de kandidaat opslaan in uw LinkedIn Recruiter-projecten.
1. Als LinkedIn de match heeft gevonden op basis van de e-mail- en lid-id voor LinkedIn (exacte match), wordt het kandidaatprofiel weergegeven. De gebruiker heeft nog steeds de optie om het profiel te koppelen of ontkoppelen.

2. Als de kandidaat niet kan worden gevonden op basis van de e-mail- of lid-id, wordt er een lijst met mogelijke kandidaten weergegeven op basis van de naam van de kandidaat en kan de gebruiker er hiervan één kiezen en het profiel koppelen.  

3. Als er geen kandidaten kunnen worden gevonden op basis van de naam, wordt aangegeven dat er geen match is gevonden.

### <a name="1-click-export"></a>Met 1 klik exporteren 

Tijdens het zoeken van kandidaten in LinkedIn, kunt u de kandidaat met 1 klik exporteren naar de functies die u momenteel open hebt. Volg de volgende stappen voor een export met 1 klik. Controleer voordat u deze stappen uitvoert of aan u de rol van Aanstellend manager of Werver voor de functie is toegewezen en of de functie de fase **Prospect** heeft.

1.  Maak de functie, wijs de juiste rollen toe en activeer de functie.

2.  Wanneer de functie is geactiveerd, gaat u naar LinkedIn Recruiter.

3.  Zoek de gewenste kandidaat en ga naar zijn of haar profiel.

4.  Zoek de functie met het functiezoekvak op de contactkaart aan de hand van de titel of de functie-id die is geactiveerd in Attract. Als u de functie niet kunt vinden, klikt u op **ATS wijzigen** om het juiste Attract-exemplaar te zoeken.

5. Nadat de functie is geselecteerd, klikt u op **Exporteren**. De kandidaat wordt nu opgehaald door Attract.

6.  Ga naar Attract en open de desbetreffende functie. U vindt de kandidaat die u zojuist hebt geëxporteerd, in de fase **Prospect** van de functie.

### <a name="in-ats-indicator"></a>In-ATS-indicator 

Met LinkedIn Recruiter kunt u bijhouden of een kandidaat naar andere functies in uw organisatie heeft gesolliciteerd, kijken waar hij of zij zich in verschillende fasen van sollicitaties bevindt en de feedback en opmerkingen vanuit Attract in LinkedIn Recruiter lezen.

1.  Open LinkedIn Recruiter en zoek het kandidaatprofiel dat u zoekt.

2.  Schuif omlaag om de sectie **In-ATS** weer te geven in het profiel van de kandidaat.

3.  U kunt deze widget gebruiken om alle informatie over de kandidaat die in Attract aanwezig is, weer te geven in de LinkedIn Recruiter-weergave.

4.  Selecteer het tabblad **Functies en statussen** om functies te zien waarvan ze deel uitmaken, de laatste status te zien en te zien hoe ze in elke functie zijn gegaan.

5.  Selecteer het tabblad **Feedback sollicitatiegesprek** om feedback te zien die de interviewers in Attract hebben ingediend.

6.  Selecteer het tabblad **Notities** om notities te zien die zijn vastgelegd voor deze sollicitant in Attract.

> [!NOTE]
> Kandidaats- en sollicitatiegegevens worden niet gesynchroniseerd met LinkedIn Recruiter als de kandidaat niet voorbij de prospectfase komt.

### <a name="inmail-history"></a>InMail-historie

De LinkedIn InMail-historie is beschikbaar met toegang op contractniveau met LinkedIn Recruiter. Als dit is ingeschakeld, kunt u uw volledige InMail-historie weergeven met de kandidaat. U kunt ook zien wie er verder in uw organisatie InMail heeft uitgewisseld met de kandidaat, maar u kunt de berichten tussen hen niet weergeven.

Als u InMail-historie wilt weergeven, gaat u naar het profiel van een kandidaat, gaat u naar het tabblad **LinkedIn** en schuift u naar de onderzijde van de pagina om de historie weer te geven. Als u een discussie met de kandidaat hebt gehad, kunt u de InMail-historie bekijken. De berichten vanuit InMail worden elke paar uur met Attract gesynchroniseerd.

### <a name="notes-history"></a>Notitiehistorie 

De historie van LinkedIn-notities is beschikbaar met toegang op contractniveau met LinkedIn Recruiter. Als het is ingeschakeld, kunt u de notities weergeven die zijn vastgelegd over de kandidaat door verschillende wervers uit uw organisatie.

Als u notitiehistorie wilt weergeven, gaat u naar het profiel van een kandidaat, gaat u naar het tabblad **LinkedIn** en schuift u naar de onderzijde van de pagina om de historie weer te geven. U kunt alle notities over de kandidaat weergeven vanuit LinkedIn Recruiter.

### <a name="inmail-stub-profile"></a>InMail-stubprofiel

Het InMail-stubprofiel is beschikbaar met toegang op contractniveau met LinkedIn Recruiter. Als kandidaten ermee instemmen hun LinkedIn-profiel te delen met een gebruiker in uw organisatie, kunt u de kandidaten in Attract bijhouden en wordt een nieuwe kandidaatrecord voor elke kandidaat gemaakt. U kunt het e-mailadres van de kandidaat weergeven als de kandidaat al in het systeem bestaat met een e-mailadres of ervoor heeft gekozen om zijn of haar adres te delen met de werver.

Als u de lijst met kandidaten wilt weergeven, gaat u naar **Talentenpools** om een door het systeem gemaakte LinkedIn-talentenpool te zien. Deze talentenpool bevat de lijst met kandidaten en hun stubprofielen, zoals ontvangen van LinkedIn, met de voornaam en achternaam van de kandidaat. De e-mail-id van de kandidaat wordt weergegeven als de kandidaat ervoor heeft gekozen zijn of haar e-mailadres te delen.
