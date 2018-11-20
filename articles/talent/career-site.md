---
title: Vacaturesitefunctionaliteit in Attract
description: Dit artikel bevat een overzicht van de vacaturesitefunctionaliteit voor kandidaten in Microsoft Dynamics 365 for Talent - Attract. Er wordt ook uitgelegd hoe u deze functionaliteit instelt.
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: nl-nl
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Vacaturesitefunctionaliteit in Attract

[!include [banner](includes/banner.md)]

Dit artikel bevat een overzicht van de vacaturesitefunctionaliteit voor kandidaten in Microsoft Dynamics 365 for Talent: Attract. Er wordt ook uitgelegd hoe u deze functionaliteit instelt.

## <a name="overview"></a>Overzicht

Attract biedt één vacaturesite voor elke omgeving in een tenant. Als een organisatie bijvoorbeeld beschikt over een ontwikkelomgeving en een testomgeving, wordt één vacaturesite ingericht voor de ontwikkelomgeving en een andere voor de testomgeving. Elke vacaturesite is **volledig geïsoleerd** en heeft een eigen verificatiemechanisme. Functies en kandidaatprofielen worden niet gedeeld tussen vacaturesites.

De vacaturesite is standaard openbaar. Daarom kunnen kandidaten alle functies weergeven die zijn gemarkeerd als extern zonder zich aan te melden. Echter, alle overige acties vereisen dat kandidaten zich aanmelden.

## <a name="career-site-management"></a>Beheer van vacaturesite

De volgende items op de vacaturesite worden bestuurd door instellingen:

- **Naam van organisatie:** de naam van de organisatie wordt weergegeven op de navigatiebalk boven aan de vacaturesite. Door de naam van de organisatie te selecteren gaan kandidaten naar een pagina met alle open functies.
- **Logo van organisatie:** een afbeelding van het organisatielogo die wordt weergegeven in de linkerbovenhoek van de vacaturesite. Door de logoafbeelding te selecteren gaan kandidaten naar een pagina met alle open functies.

Als u de waarden voor de organisatienaam en -logo wilt instellen, meldt u zich aan bij Attract als beheerder, selecteert u **Beheercentrum** in het menu **Instellingen** (het symbool met een tandwiel) en selecteert u vervolgens het tabblad **Bedrijfsgegevens**.

> [!NOTE]
> De logoafbeelding die wordt weergegeven op de vacaturesite heeft een vaste hoogte van 20 pixels (px). De afbeelding die u in het beheercentrum toevoegt, wordt passend gemaakt. Daarom kan de breedte afhankelijk van de afbeelding veranderen.

## <a name="career-site-url"></a>URL van vacaturesite

Wanneer u voor de eerste keer [een externe functie boekt](./Creating-jobs-Attract.md#postings), kunt u de koppeling **Solliciteren** kopiëren uit de Attract-toepassing. De URL voor deze koppeling heeft de volgende indeling: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

De URL van de vacaturesite is een subtekenreeks van de URL **Solliciteren**. Deze bestaat uit alles tot aan de bedrijfsnaam. Daarom is voor de voorgaande URL **Solliciteren** de URL van de vacaturesite `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Verificatieopties

Kandidaten hebben de volgende aanmeldingsopties voor een Attract-vacaturesite:

- Persoonlijk account:

    - LinkedIn
    - Microsoft
    - Google
    - Facebook

- Werk- of schoolaccount:

    - Microsoft Azure Active Directory (Azure AD)

Azure AD-aanmelding is alleen bedoeld voor interne kandidaten. Daarom werkt het alleen voor interne kandidaten die de Azure AD-referenties van hun bedrijf gebruiken. Een kandidaat die momenteel een werknemer van Contoso Ltd is, wil bijvoorbeeld solliciteren naar een functie in een niet-gelieerd bedrijf Alpine Ski House. In dit geval wordt de aanmelding niet succesvol als de werknemer probeert zijn of haar Azure AD-referenties van Contoso, Ltd te gebruiken.

## <a name="create-and-maintain-a-profile"></a>Een profiel maken en onderhouden

Nadat kandidaten zich hebben aangemeld bij de vacaturesite, kunnen ze **Mijn profiel** selecteren op de navigatiebalk boven aan de pagina om hun profiel te maken en te onderhouden. Het profiel bevat persoonlijke gegevens, informatie over werkervaring, opleidingsdetails, documenten, koppelingen en informatie over vaardigheden. Nadat een profiel is gemaakt, kan het worden gebruikt om te solliciteren naar functies waarin de kandidaat geïnteresseerd is. Profielen helpen Attract de juiste functies aan kandidaten aan te bevelen.

## <a name="find-the-right-job"></a>De juiste functie zoeken

Op de functielijstpagina kunnen kandidaten een bepaalde functie zoeken door zoektermen in te voeren. De zoekfunctionaliteit zoekt naar de zoektermen in functietitels en functiebeschrijvingen en toont relevante functies als resultaat. Kandidaten kunnen de resultaten op elk gewenst moment filteren op basis van de functielocatie of de functiepositie.

Kandidaten kunnen ook een reeks aanbevolen functies weergeven op de vacaturesite. De functies die worden aanbevolen aan een kandidaat, zijn gebaseerd op eerdere sollicitaties, het profiel en cv's van de kandidaat.

> [!NOTE]
> Functieaanbevelingen worden alleen weergegeven als ten minste 10 functies zijn geboekt op de vacaturesite en als de kandidaat zijn of haar profiel heeft voltooid.

## <a name="apply-for-jobs"></a>Aanmelden voor taken

Als kandidaten de juiste functie hebben gevonden, kunnen ze solliciteren met de knop **Solliciteren** op de pagina met functiedetails. Op dit moment kunnen kandidaten een nieuw profiel maken of de gegevens in hun bestaande profiel bekijken. Kandidaten kunnen ook een cv uploaden, indien nodig, en vervolgens de functiesollicitatie indienen.

## <a name="check-application-status"></a>Sollicitatiestatus controleren

Nadat kandidaten voor een of meer functies hebben gesolliciteerd, kunnen ze **Sollicitaties** selecteren op de navigatiebalk boven aan de pagina om hun openstaande en afgesloten sollicitaties weer te geven. Wanneer kandidaten een van hun sollicitaties openen, zien ze de huidige fase en in behandeling zijnde actie-items die ze moeten voltooien. Als een kandidaat bijvoorbeeld mogelijke potentiële datums voor een persoonlijk sollicitatiegesprek moet verschaffen, geeft de pagina zijn of haar opties weer.

## <a name="internal-jobs"></a>Interne functies

Op dit moment worden functies die zijn gemarkeerd als intern en op de Attract-vacaturesite zijn geplaatst, niet op de vacaturesite weergegeven. Ze zijn toegankelijk via de rechtstreekse URL **Solliciteren** die kan worden gekopieerd uit de Attract-sollicitatie.

