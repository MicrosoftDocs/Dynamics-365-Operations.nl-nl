---
title: Functionaliteit Vacaturesite in Attract
description: Dit onderwerp bevat een overzicht van de functionaliteit voor op kandidaten gerichte vacaturesite in Attract.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: e51fb00536884d2b3815c05a0968714d8b9326f2
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729698"
---
# <a name="career-site-functionality-in-attract"></a>Functionaliteit Vacaturesite in Attract

[!include[banner](../includes/banner.md)]

Dit onderwerp bevat een overzicht van de functionaliteit voor op kandidaten gerichte vacaturesite in Microsoft Dynamics 365 for Talent: Attract. Ook wordt uitgelegd hoe u deze functionaliteit instelt.

Attract biedt één vacaturesite voor elke omgeving in een tenant. Als een organisatie bijvoorbeeld beschikt over een ontwikkelomgeving en een testomgeving, wordt één vacaturesite ingericht voor de ontwikkelomgeving en een andere voor de testomgeving. Elke vacaturesite is volledig geïsoleerd en heeft een eigen verificatiemechanisme. Functies en kandidaatprofielen worden niet gedeeld tussen vacaturesites.

De vacaturesite is standaard openbaar. Daarom kunnen kandidaten alle functies weergeven die zijn gemarkeerd als extern zonder zich aan te melden. Voor alle overige acties is echter vereist dat kandidaten zich aanmelden.

## <a name="career-site-management"></a>Beheer van vacaturesite

Als u de waarden voor de volgende items wilt instellen, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** (het symbool met een tandwiel) en selecteert u vervolgens het tabblad **Bedrijfsgegevens**.

-   **Naam van organisatie**: de naam van de organisatie wordt weergegeven op de navigatiebalk boven aan de vacaturesite. Door de naam van de organisatie te selecteren gaan kandidaten naar een pagina met alle open functies.

-   **Logo van organisatie**: een afbeelding van het organisatielogo die wordt weergegeven in de linkerbovenhoek van de vacaturesite. Door de logoafbeelding te selecteren gaan kandidaten naar een pagina met alle open functies.

    > [!NOTE] 
    > De logoafbeelding die wordt weergegeven op de vacaturesite heeft een vaste hoogte van 20 pixels (px). De afbeelding die u in het beheercentrum toevoegt, wordt passend gemaakt. Daarom kan de breedte afhankelijk van de afbeelding veranderen.
 
Als u de waarden voor de volgende items wilt instellen, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** en selecteert u vervolgens het tabblad **Beheer van vacaturesite**.

-   **Optimalisatie van zoekmachine**: wanneer deze optie is ingeschakeld, kan naar alle openbare vacatures die zijn gepubliceerd naar de Attract-vacaturestite, worden gezocht met zoekmachines zoals Bing en Google. 

    > [!NOTE] 
    > Er kan een vertraging optreden tussen het inschakelen van deze instelling en de weergave van zoekresultaten. Dit is afhankelijk van de zoekmachine die u gebruikt.
    
-   **Algemene voorwaarden**: indien ingeschakeld moeten alle kandidaten de algemene voorwaarden van de organisatie accepteren wanneer ze solliciteren op een functie. De Attract-beheerder kan een eigen toestemmingstekst en koppeling naar de pagina voor algemene voorwaarden configureren. 

        
## <a name="career-site-urls"></a>URL´s vacaturesite

De volgende lijst bevat de meest gebruikte vacaturesite-URL's en hoe u toegang krijgt tot deze sites.

-   **Startpagina-URL van vacaturesite**: als u de startpagina-URL van een vacaturesite wilt weergeven, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** en selecteert u vervolgens het tabblad **Beheer van vacaturesite**.

-   **Sollicitatie-URL afzonderlijke vacture**: wanneer u voor de eerste keer [een externe functie publiceert](Creating-jobs-Attract.md#postings), kunt u de koppeling **Solliciteren** kopiëren uit de Attract-toepassing. De URL voor deze koppeling heeft de volgende indeling: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **URL afzonderlijke vacature**: de URL van de vacature is een subreeks van de sollicitatie-URL. Deze reeks bestaat uit alles tot en met het vacaturenummer. Daarom is voor de voorgaande sollicitatie-URL de URL van de vacature [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e).

## <a name="authentication-options"></a>Verificatieopties

Kandidaten hebben de volgende aanmeldingsopties voor een Attract-vacaturesite:

-   Persoonlijk account:

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   Werk- of schoolaccount:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD-aanmelding is alleen bedoeld voor interne kandidaten. Daarom werkt het alleen voor interne kandidaten die de Azure AD-referenties van hun bedrijf gebruiken. Een kandidaat die momenteel een werknemer van Contoso Ltd is, wil bijvoorbeeld solliciteren naar een functie in een niet-gelieerd bedrijf Alpine Ski House. In dit geval is de aanmelding niet succesvol als de werknemer probeert zijn of haar Azure AD-referenties van Contoso, Ltd te gebruiken. 

Kandidaten moeten zich aanmelden met behulp van Azure AD als de functie die ze bekijken of waarop ze solliciteren, wordt weergegeven als alleen intern.

## <a name="create-and-maintain-a-profile"></a>Een profiel maken en onderhouden

Nadat kandidaten zich hebben aangemeld bij de vacaturesite, kunnen ze **Mijn profiel** selecteren op de navigatiebalk boven aan de pagina om hun profiel te maken en te onderhouden.
Het profiel bevat persoonlijke gegevens, informatie over werkervaring, opleidingsdetails, documenten, koppelingen en informatie over vaardigheden. Nadat een profiel is gemaakt, kan het worden gebruikt om te solliciteren naar functies waarin de kandidaat geïnteresseerd is. Profielen helpen Attract de juiste functies aan kandidaten aan te bevelen.

> [!NOTE]
> Als een kandidaat een e-mail-ID gebruikt voor aanmelding met een van de hierboven vermelde verificatieproviders, wordt die e-mail-ID standaard ingesteld op de e-mail-ID van de contactpersoon die is gekoppeld aan het profiel. De laatst genoemde kan echter op elk gewenst moment worden gewijzigd en is volledig onafhankelijk van de eerst genoemde. In Attract wordt de e-mail-ID van de contactpersoon gebruikt om deze aan uw profiel te koppelen voor alle e-mailberichten.

## <a name="find-the-right-job"></a>De juiste functie zoeken

Op de functielijstpagina kunnen kandidaten zoeken naar een bepaalde functie door zoektermen in te voeren. Met de zoekfunctionaliteit wordt gezocht naar de zoektermen in functietitels en functiebeschrijvingen en worden relevante functies als resultaat getoond. Kandidaten kunnen de resultaten op elk gewenst moment filteren op basis van de functielocatie of de functiepositie.

Kandidaten kunnen ook een reeks aanbevolen functies weergeven op de vacaturesite. De functies die worden aanbevolen aan een kandidaat, zijn gebaseerd op eerdere sollicitaties, het profiel en cv's van de kandidaat.

> [!NOTE] 
> Functieaanbevelingen worden alleen weergegeven als ten minste 10 functies zijn gepubliceerd op de vacaturesite en als de kandidaat zijn of haar profiel heeft ingevuld.

Interne kandidaten kunt ook zien wie de aanstellende manager en/of werver voor een functie is, voor het geval ze contact willen opnemen met die leden van het aanstellingsteam. Externe kandidaten hebben echter geen inzicht in de leden van het aanstellingsteam voor een functie.

## <a name="contact-the-hiring-team"></a>Neem contact op met het aanstellingsteam
Alleen interne kandidaten kunnen contact opnemen met het aanstellingsteam. Deze beperking geldt voor alle functies, ongeacht of deze alleen intern zijn of openbaar zijn gepubliceerd.

Kandidaten kunnen contact opnemen met het aanstellingsteam om aan te geven dat ze belangstelling hebben voor een functie die is gepubliceerd of om meer informatie erover te krijgen. Ze kunnen contact opnemen met een van de leden van het aanstellingsteam die worden weergegeven (aanstellende manager of wervers). Ze kunnen desgewenst ook een cv toevoegen aan het bericht of ze kunnen een bestaand cv selecteren dat ze eerder hebben geüpload als onderdeel van hun profiel.

Nadat een interne kandidaat leden van het aanstellingsteam hebben geselecteerd om contact op te nemen, wordt in Attract een e-mailbericht aan deze personen verzonden namens de kandidaat. Tegelijkertijd wordt het kandidaatprofiel toegevoegd aan de fase **Prospect**, als die fase beschikbaar is voor de functie. In de fase **Prospect** kunnen wervers of aanstellende managers de kandidaten bekijken die met hen contact hebben opgenomen. Ze kunnen ook kandidaatprofielen bekijken en potentiële kandidaten uitnodigen om te solliciteren.

Kandidaten kunnen solliciteren op een functie waarvoor ze al contact hebben opgenomen met leden van het aanstellingsteam. Nadat ze hebben gesolliciteerd, kunnen kandidaten niet langer contact opnemen met het aanstellingsteam via de vacaturesite.

## <a name="apply-for-jobs"></a>Solliciteren op functies

Als kandidaten de juiste functie hebben gevonden, kunnen ze solliciteren met de knop  **Solliciteren**  op de pagina  **Functiedetails**. Op dit moment kunnen kandidaten een nieuw profiel maken of de gegevens in hun bestaande profiel bekijken.
Kandidaten kunnen indien nodig ook een cv uploaden en vervolgens de sollicitatie indienen.

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a>Solliciteren op functies met LinkedIn-profielen inschakelen

U kunt het eenvoudig maken voor kandidaten om te solliciteren op uw posities door Attract zo te configureren dat ze kunnen solliciteren via LinkedIn.

> [!NOTE] 
> U moet een of meer werverlicenties van LinkedIn hebben voordat u kandidaten kunt toestaan om te solliciteren met LinkedIn.

1. Meld u aan bij Attract als beheerder.
2. Selecteer de knop **Instellingen** (het tandwielsymbool) in de rechterbovenhoek van de pagina en selecteer vervolgens **Beheercentrum**.
3. Selecteer het tabblad **LinkedIn-integratie** en maak verbinding met een LinkedIn Recruiter-account.
4. Selecteer in de sectie **LinkedIn Recruiter System Connect -integratie** **Ingeschakeld** voor de instelling **Solliciteren met LinkedIn**.

Nadat u de instelling hebt ingeschakeld, kunnen kandidaten alleen solliciteren met hun bestaande LinkedIn-profielgegevens. Wanneer kandidaten solliciteren door de knop **Solliciteren met LinkedIn** te kiezen, wordt hen gevraagd om te verifiëren met LinkedIn als ze nog niet zijn aangemeld. Nadat ze zijn geverifieerd, worden bestaande profielgegevens weergegeven op de sollicitatiepagina vervangen door hun LinkedIn-profiel. Kandidaten kunnen de gegevens zo nodig bewerken en de sollicitatie indienen. Als een kandidaat de pagina verlaat zonder op de functie te solliciteren, worden hun profielgegevens niet bijgewerkt in Attract.

## <a name="check-application-status"></a>Sollicitatiestatus controleren

Nadat kandidaten voor een of meer functies hebben gesolliciteerd, kunnen ze **Sollicitaties** selecteren op de navigatiebalk boven aan de pagina om hun openstaande en afgesloten sollicitaties weer te geven. Wanneer kandidaten een van hun sollicitaties openen, zien ze de huidige fase en in behandeling zijnde actie-items die ze moeten voltooien. Als een kandidaat bijvoorbeeld mogelijke potentiële datums voor een persoonlijk sollicitatiegesprek moet verschaffen, worden op de pagina de beschikbare opties weergegeven.

## <a name="internal-jobs"></a>Interne functies

Op dit moment worden functies die zijn gemarkeerd als intern en op de Attract-vacaturesite zijn geplaatst, niet op de vacaturesite weergegeven. Ze zijn alleen toegankelijk via de rechtstreekse URL **Solliciteren** die kan worden gekopieerd uit de Attract-sollicitatie.
