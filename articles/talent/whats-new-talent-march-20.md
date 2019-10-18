---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (20 maart 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c16082bb18ac5c170aab30f1a2033e0790cbacc1
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025997"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-20-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (20 maart 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

### <a name="setting-the-audience-on-activities"></a>De doelgroep voor activiteiten instellen
Voor activiteiten in het systeem kan de doelgroep nu worden gedefinieerd. Procesgerelateerde activiteiten (zoals sollicitatiegesprek, planning, feedback en EEO) kunnen worden ingesteld op Alle kandidaten, Interne kandidaten en Externe kandidaten. Aangepaste activiteiten, zoals Microsoft Forms, YouTube-video's en webinhoud kunnen worden geleverd aan Alle kandidaten, Interne kandidaten, Externe kandidaten of het aanstellingsteam.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Vindbaarheid van functies op vacaturesite verbeteren: optimalisatie voor zoekmachines
Met deze functie kunnen zoekmachinecrawlers functiepublicaties op de Attract-vacaturesite bereiken en indexeren. Hiermee kunnen kandidaten functies vinden die met populaire zoekmachines naar de Attract-vacaturesite zijn gepubliceerd.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Aanmeldingshint tonen aan kandidaten die hun referenties hebben vergeten
Als kandidaten de sociale referenties zijn vergeten die zijn gebruikt om te solliciteren op een functie bij het openen van een koppeling die is opgeslagen of per e-mail is verzonden aan hen, zien ze voortaan een hint met de naam van de provider en de gebruikersnaam (afgeschermd). Op deze manier gebruiken ze de juiste referenties voor toegang tot hun sollicitatie.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Interne kandidaten helpen bij het verkennen van interne functies
Het probleem waarbij externe kandidaten de naam van de werver of de aanstellende manager van een functie kunnen zien, is opgelost. Nu kunnen alleen interne kandidaten de leden van het aanstellende team voor een functie zien. Ook is het gemakkelijker voor interne kandidaten om alleen-interne functies te bekijken en erop te solliciteren. Wanneer een kandidaat toegang probeert te krijgen tot de koppeling om een alleen-intern project te bekijken of erop te solliciteren, is verificatie met Azure Active Directory-referenties vereist. Interne kandidaten hebben ook de mogelijkheid om contact op te nemen met de leden van het aanstellende team om aan te geven dat ze belangstelling hebben voor de functie of er meer over willen weten. Deze functie is beschikbaar voor alle functies voor alleen interne kandidaten. Zie voor meer informatie [Vacaturesitefunctionaliteit in Attract](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Tweede plaatsen aanwijzen om sollicitanten met een hoge waarde voor toekomstige posities toe te wijzen
Wervers en aanstellende managers houden vaak een actieve lijst bij van sollicitanten die geschikt zijn voor de positie, maar aan wie de functie niet kan worden aangeboden omdat de positie al is ingevuld. Dergelijke sollicitanten, zogenaamde tweedeplaatskandidaten, zijn waardevol omdat ze tijd kunnen besparen als een vergelijkbare positie de volgende keer vrij komt. In Attract kunnen wervers en aanstellende managers tweedeplaatskandidaten op de lijst met sollicitanten aanwijzen als de sollicitant naar de fase Aanbieding is verplaatst. De aanduiding van tweede plaats wordt in de lijst met sollicitanten voor de functie weergegeven, maar ook in de weergave van de talentenpool wanneer deze sollicitanten lid zijn van een van de pools van de werver of aanstellende manager. Daarnaast worden de aanduiding weergegeven in de functiehistorie als onderdeel van het talentenpoolprofiel van een kandidaat. U kunt een voorbeeld van deze functie bekijken door een beheerder de functie te laten inschakelen met [Functiebeheer in het Beheercentrum](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="add-applicants-to-talent-pools"></a>Sollicitanten toevoegen aan talentenpools
Het is nu eenvoudiger om sollicitanten aan talentenpools toe te voegen door een nieuwe actie in de lijst met sollicitanten op te nemen. Door het pictogram **Toevoegen aan talentenpool** te selecteren, kan de werver of aanstellende manager kiezen uit de lijst met talentenpools en sollicitanten direct vanuit de lijst met sollicitanten voor een functie toevoegen aan talentenpools.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Configureren of een cv vereist is om te solliciteren voor een bepaalde functie
Op basis van feedback van klanten kunnen wervers nu configureren of een cv, in de vorm van een geüpload bestand, vereist is bij het solliciteren op een bepaalde functie. Deze configuratie maakt deel uit van de activiteit Sollicitatie in het aanstellingsproces. Wanneer deze functie is ingeschakeld, wordt elke potentiële sollicitant gevraagd een cv te uploaden wanneer ze solliciteren op deze positie. De sollicitatie wordt pas als voltooid beschouwd als een cv is geüpload. Dit helpt ruis in de sollicitantenpool te verminderen doordat ervoor wordt gezorgd dat alle sollicitanten voldoende informatie verschaffen zodat de werver hen kan beoordelen.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Kandidaten kunnen solliciteren op een functie met hun LinkedIn-profiel
Kandidaten die hun huidige bijgewerkte profiel al op LinkedIn hebben staan, kunnen met behulp van dat profiel solliciteren op functies met slechts één klik.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Bijhouden waar het profiel van een kandidaat vandaan komt in het systeem en waar uw sollicitanten de functies waarop ze solliciteren, hebben gevonden
U kunt nu uitzoeken waar een bepaald kandidaatprofiel vandaan komt in Attract door te kijken naar de profielbron onder kandidaatdetails op de pagina **Profiel** van een sollicitatie of talentenpoolprofiel. Op dezelfde manier kunt u uitzoeken hoe elke sollicitant de functie heeft gevonden door te kijken naar de toepassingsbron die wordt verschaft in de **Activiteit Sollicitatie** in de toepassingsactiviteitsfeed. Deze informatie is ook beschikbaar in de functiehistorie in het talentenpoolprofiel. Wanneer wervers of aanstellende managers kandidaten handmatig toevoegen, wordt hen ook gevraagd de bron van de sollicitatie of het kandidaatprofiel aan te wijzen. Wanneer kandidaten voor het eerst solliciteren, is de profielbron hetzelfde als de oorsprong van de sollicitatie. U kunt een voorbeeld van deze functie bekijken door een beheerder de functie te laten inschakelen met [Functiebeheer in het Beheercentrum](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature). Houd er rekening mee dat bestaande kandidaten en sollicitanten geen brongegevens hebben. Wervers kunnen deze informatie echter handmatig toevoegen.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract-integratie geeft de fout Dubbele records voor Sollicitaties
In deze update is een probleem met dubbele records opgelost. Dit probleem is zichtbaar bij het openen van het werkgebied **Personeelsbeheer**.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Formulier kan niet worden gesloten bij het bewerken van de naamsvolgorde
Er zijn wijzigingen aangebracht om een probleem bij het bewerken van de naamsvolgorde op het werknemersformulier op te lossen.

## <a name="coming-soon"></a>Binnenkort beschikbaar

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Geavanceerde compensatiebeveiliging (vast en variabel)
In veel organisaties kunnen managers voor compensaties en vergoedingen alleen toegang krijgen tot bepaalde compensatierecords. Dit kan voor leidinggevenden of regionale werknemers zijn. Met deze wijziging kan HR de compensatieplannen beheren en onderhouden voor verschillende werknemersgroepen in de organisatie. U kunt aan vaste en variabele plannen beveiligingsrollen toewijzen waarmee de toegang wordt bepaald tot de plannen en de werknemersgegevens die zijn gerelateerd aan de plannen, zoals salaris- of bonusrecords. Alleen de rollen met de verleende toegang kunnen compensatie voor deze werknemers verwerken.

###  <a name="email-support-for-alerts"></a>E-ondersteuning voor waarschuwingen
Met Platformupdate 24 voor Finance and Operations kunnen gebruikers waarschuwingsregels maken waarmee automatisch e-mailmeldingen worden verzonden naar contactpersonen wanneer meldingen door een gebeurtenis worden geactiveerd.

### <a name="duplicate-employee-check-interface-changes"></a>Controle of dubbele werknemers: interfacewijzigingen
Met deze wijziging worden dubbele records gedetecteerd wanneer u naamvelden invoert en met een status wordt het aantal dubbelen weergegeven. U kunt de opgegeven koppeling selecteren om een nieuwe pagina te openen om te beoordelen of de gedetecteerde overeenkomst moet worden gebruikt. Het formulier met dubbele records wordt niet automatisch geopend om te voorkomen dat gegevensinvoer wordt onderbroken.


