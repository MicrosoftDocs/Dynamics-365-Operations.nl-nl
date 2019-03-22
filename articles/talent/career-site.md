---
title: Functionaliteit Vacaturesite in Attract
description: Dit onderwerp bevat een overzicht van de functionaliteit voor op kandidaten gerichte vacaturesite in Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/13/2019
ms.locfileid: "389956"
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

    >   [!NOTE] 
    >   De logoafbeelding die wordt weergegeven op de vacaturesite heeft een vaste hoogte van 20 pixels (px). De afbeelding die u in het beheercentrum toevoegt, wordt passend gemaakt. Daarom kan de breedte afhankelijk van de afbeelding veranderen.
 
Als u de waarden voor de volgende items wilt instellen, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** en selecteert u vervolgens het tabblad **Beheer van vacaturesite**.

-   **Optimalisatie van zoekmachine**: wanneer deze optie is ingeschakeld, kan naar alle openbare vacatures die zijn gepubliceerd naar de Attract-vacaturestite, worden gezocht met zoekmachines zoals Bing en Google.

    >   [!NOTE] 
    >   Er kan een vertraging optreden tussen het inschakelen van deze instelling en de weergave van zoekresultaten. Dit is afhankelijk van de zoekmachine die u gebruikt.
         
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

## <a name="create-and-maintain-a-profile"></a>Een profiel maken en onderhouden

Nadat kandidaten zich hebben aangemeld bij de vacaturesite, kunnen ze **Mijn profiel** selecteren op de navigatiebalk boven aan de pagina om hun profiel te maken en te onderhouden.
Het profiel bevat persoonlijke gegevens, informatie over werkervaring, opleidingsdetails, documenten, koppelingen en informatie over vaardigheden. Nadat een profiel is gemaakt, kan het worden gebruikt om te solliciteren naar functies waarin de kandidaat geïnteresseerd is. Profielen helpen Attract de juiste functies aan kandidaten aan te bevelen.

>   [!NOTE]
>   Als een kandidaat een e-mail-ID gebruikt voor aanmelding met een van de hierboven vermelde verificatieproviders, wordt die e-mail-ID standaard ingesteld op de e-mail-ID van de contactpersoon die is gekoppeld aan het profiel. De laatst genoemde kan echter op elk gewenst moment worden gewijzigd en is volledig onafhankelijk van de eerst genoemde. In Attract wordt de e-mail-ID van de contactpersoon gebruikt om deze aan uw profiel te koppelen voor alle e-mailberichten.

## <a name="find-the-right-job"></a>De juiste functie zoeken

Op de functielijstpagina kunnen kandidaten zoeken naar een bepaalde functie door zoektermen in te voeren. Met de zoekfunctionaliteit wordt gezocht naar de zoektermen in functietitels en functiebeschrijvingen en worden relevante functies als resultaat getoond. Kandidaten kunnen de resultaten op elk gewenst moment filteren op basis van de functielocatie of de functiepositie.

Kandidaten kunnen ook een reeks aanbevolen functies weergeven op de vacaturesite. De functies die worden aanbevolen aan een kandidaat, zijn gebaseerd op eerdere sollicitaties, het profiel en cv's van de kandidaat.

>   [!NOTE] 
>   Functieaanbevelingen worden alleen weergegeven als ten minste 10 functies zijn gepubliceerd op de vacaturesite en als de kandidaat zijn of haar profiel heeft ingevuld.

## <a name="apply-for-jobs"></a>Solliciteren op functies

Als kandidaten de juiste functie hebben gevonden, kunnen ze solliciteren met de knop **Solliciteren** op de pagina **Functiedetails**. Op dit moment kunnen kandidaten een nieuw profiel maken of de gegevens in hun bestaande profiel bekijken.
Kandidaten kunnen indien nodig ook een cv uploaden en vervolgens de sollicitatie indienen.

## <a name="check-application-status"></a>Sollicitatiestatus controleren

Nadat kandidaten voor een of meer functies hebben gesolliciteerd, kunnen ze **Sollicitaties** selecteren op de navigatiebalk boven aan de pagina om hun openstaande en afgesloten sollicitaties weer te geven. Wanneer kandidaten een van hun sollicitaties openen, zien ze de huidige fase en in behandeling zijnde actie-items die ze moeten voltooien. Als een kandidaat bijvoorbeeld mogelijke potentiële datums voor een persoonlijk sollicitatiegesprek moet verschaffen, worden op de pagina de beschikbare opties weergegeven.

## <a name="internal-jobs"></a>Interne functies

Op dit moment worden functies die zijn gemarkeerd als intern en op de Attract-vacaturesite zijn geplaatst, niet op de vacaturesite weergegeven. Ze zijn alleen toegankelijk via de rechtstreekse URL **Solliciteren** die kan worden gekopieerd uit de Attract-sollicitatie.
