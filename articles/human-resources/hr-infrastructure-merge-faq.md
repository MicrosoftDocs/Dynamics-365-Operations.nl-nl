---
title: Veelgestelde vragen over infrastructuursamenvoeging voor Dynamics 365 Human Resources
description: In dit artikel worden veelgestelde vragen beantwoord over het samenvoegen van de infrastructuur voor Microsoft Dynamics 365 Human Resources en apps voor financiën en bedrijfsactiviteiten.
author: twheeloc
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7325231718d7387450391b16b2866f9a2c05bdc4
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779630"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Veelgestelde vragen over infrastructuursamenvoeging voor Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Wat is Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources biedt hulpprogramma's waarmee HR-teams de organisatorische flexibiliteit kunnen vergroten, de werknemerservaring kunnen transformeren en HR-programma's kunnen optimaliseren om een werkplek te creëren die goed is voor mensen en het bedrijf. Zie voor meer informatie over Dynamics 365 Human Resources [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Werknemerservaringen transformeren.** Houd de prestaties op hoog niveau door managers en werknemers meer mogelijkheden te bieden via verbonden selfservice-ervaringen die zorgen voor meer betrokkenheid en groei.
- **HR-programma's optimaliseren.** Verlaag de operationele kosten en maak programma's voor op mensen gebaseerd beheer van verlof en verzuim, tijd, vergoedingen en compensatie.
- **Organisatorische flexibiliteit vergroten.** Stel HR in staat om te werken met de behendigheid die het bedrijf nodig heeft door Dataverse en Microsoft Power Platform te gebruiken om gegevens van personen te centraliseren en Dynamics 365 Human Resources eenvoudig uit te breiden.
- **Inzichten in personeel verkrijgen.** Neem gegevensgestuurde beslissingen via de mogelijkheid om gegevens over personen te analyseren en te visualiseren op uitgebreide dashboards die op elk apparaat beschikbaar zijn.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Toegevoegde waarde en voordelen van de infrastructuursamenvoeging

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Wat is de infrastructuursamenvoeging voor Dynamics 365 Human Resources?

Er zijn momenteel twee afzonderlijke sets HR-mogelijkheden beschikbaar in twee verschillende infrastructuren in Dynamics 365:

- **Dynamics 365 Human Resources**: een zelfstandige app die in een onafhankelijke infrastructuur wordt uitgevoerd. Toen deze app werd gelanceerd, was de infrastructuur gescheiden van andere Dynamics 365-apps voor bedrijfsactiviteiten. Onze klanten gebruiken deze app om organisatorische flexibiliteit te vergroten, HR-programma´s te optimaliseren, werknemerservaringen te transformeren en inzicht in personeel te verkrijgen.
- **HR-module**: een verouderde set mogelijkheden die eerder deel uitmaakte van de licentie-SKU (voorraadeenheid) van Unified Operations. De HR-module wordt uitgevoerd in de infrastructuur voor financiën en bedrijfsactiviteiten, die voor alle apps voor bedrijfsactiviteiten hetzelfde is. Deze apps zijn Dynamics 365 Finance, Dynamics 365 Project Operations en Dynamics 365 Supply Chain Management. Klanten hebben de HR-mogelijkheden als onderdeel van Dynamics 365 Finance of Dynamics 365 Supply Chain Management ontvangen.

In de afgelopen drie jaar heeft Microsoft geen nieuwe mogelijkheden of verbeteringen aan de HR-module toegevoegd. In plaats daarvan hebben we ons gericht op de app Dynamics 365 Human Resources.

Door deze twee sets mogelijkheden in dezelfde infrastructuur samen te brengen, helpen we klanten de volgende voordelen te krijgen:

- Verbeteringen die in de afgelopen drie jaar aan Dynamics 365 Human Resources zijn toegevoegd, waaronder verbeterd beheer van verlof en verzuim en vergoedingen en betere rapportage.
- Verbeterde uitbreidbaarheid via Microsoft Power Platform en de mogelijkheid om bedrijfslogica uit te breiden om pagina's te personaliseren.
- Verbeteringen in implementatie, updates en onderhoud die zorgen voor consistentie wat betreft ALM (Application Lifecycle Management), Lifecycle Services (LCS), geografische beschikbaarheid en meer.
- Meer technologische innovatie aangezien ons technisch team gedeelde services en hulpmiddelen gebruikt en platformkosten zijn verlaagd.

Deze overgang heeft gevolgen voor klanten die momenteel Dynamics 365 Human Resources of de verouderde HR-module gebruiken.

## <a name="glossary-of-terms-used-in-this-faq"></a>Woordenlijst van termen die in deze veelgestelde vragen worden gebruikt

- **Dynamics 365 Human Resources**: ons huidige en toekomstige product dat HR-mogelijkheden aan de markt biedt.
- **HR-module**: een set met verouderde mogelijkheden die eerder deel uitmaakten van het Unified Operations-aanbod. Deze mogelijkheden worden ingeschakeld wanneer een klant in bezit is van Dynamics 365 Finance of Dynamics 365 Supply Chain Management.
- **Infrastructuur voor financiën en bedrijfsactiviteiten**: de ontwikkelingsarchitectuur die wordt gebruikt door het portfolio van bedrijfsactiviteiten, zoals Dynamics 365 Finance, Dynamics 365 Supply Chain Management en Dynamics 365 Project Operations. Deze infrastructuur zal in de toekomst gebruikt worden. In deze veelgestelde vragen verwijst de term *samengevoegde infrastructuur* naar de omgeving voor financiën en bedrijfsactiviteiten.
- **Human resources-infrastructuur**: de ontwikkelingsarchitectuur die oorspronkelijk voor de app Dynamics 365 Human Resources werd gebruikt. Door de infrastructuursamenvoeging krijgt Dynamics 365 Human Resources dezelfde infrastructuur als apps voor financiën en bedrijfsactiviteiten. De zelfstandige infrastructuur wordt beëindigd.

## <a name="general-questions-about-the-infrastructure-merge"></a>Algemene vragen over de samenvoeging van de infrastructuur

### <a name="will-customers-lose-any-features-or-capabilities"></a>Gaan bepaalde functies of mogelijkheden voor klanten verloren?

Onze doelstelling is om de impact van deze overgang op klanten tot een minimum te beperken. Er worden geen functies of mogelijkheden verwijderd. Er zal functionele pariteit zijn tussen Dynamics 365 Human Resources en de HR-module. Wanneer een functie in beide infrastructuren voorkomt, wordt de Dynamics 365 Human Resources-ervaring gebruikt.

### <a name="will-the-user-experience-change"></a>Zal de gebruikerservaring veranderen?

De gebruikerservaring is consistent met de standaardervaring van het Dynamics 365-platform. Hoewel de algemene ervaring met het dashboard en de menu's vergelijkbaar blijft, wordt deze afgestemd op de standaardervaring van de Dynamics 365 Finance-app. De navigatie omvat zowel modules als werkgebieden, favorieten zijn toegestaan, en meer. De Dynamics 365 Human Resources-werkgebieden, zoals **Personeelsbeheer** en **Personen**, worden samengevoegd in de infrastructuur voor financiën en bedrijfsactiviteiten. In de toekomst worden nieuwe mogelijkheden verschaft via Functiebeheer, zodat klanten nieuwe functies kunnen bekijken en kunnen bepalen welke functies ze willen gebruiken. Zie [Overzicht van Functiebeheer](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en [Documentatie van gebruikersinterface](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json) voor meer informatie.

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Wanneer wordt de infrastructuursamenvoeging van Dynamics 365 Human Resources voltooid?

De infrastructuursamenvoeging wordt in fasen uitgevoerd om klanten tijd te geven de benodigde stappen te plannen en uit te voeren. We zijn begonnen met de implementatie van mogelijkheden in Dynamics 2021-release wave 2. We zijn van plan om alle productontwikkelingswerkzaamheden voor dit project af te ronden tegen het einde van 2022-release wave 2. Houd er rekening mee dat tijdlijnen kunnen worden gewijzigd. Zie [Releaseplannen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) voor de meest actuele informatie.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Welke training en resources zijn er beschikbaar om te helpen bij de infrastructuursamenvoeging?

We verstrekken documentatie waarin elke stap van het infrastructuursamenvoegingsproces gedetailleerd wordt beschreven. Wij verschaffen zo nodig extra trainingsresources, zoals video´s en workshops, om zoveel mogelijk voor een probleemloze overgang voor klanten en partners te zorgen.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Zijn er wijzigingen in ontwikkelingsmogelijkheden na samenvoeging van de infrastructuur?

Zie [Startpagina van Ontwikkelen en aanpassen](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md) voor meer informatie over ontwikkelingsmogelijkheden.

## <a name="feature-availability-questions"></a>Vragen over functiebeschikbaarheid

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Werkt de integratie van LinkedIn Talent Hub in de infrastructuur voor financiën en bedrijfsactiviteiten?

Nee, de integratie van LinkedIn Talent is geen onderdeel van de samengevoegde infrastructuur. Openbare API´s (Application Programming Interfaces) zijn beschikbaar voor het bouwen van integraties met oplossingen voor werving en het sollicitantenvolgsysteem. Klanten die LinkedIn Talent Hub willen gebruiken, moeten samenwerken met hun Microsoft-partner om deze te integreren met behulp van de geleverde API's. Zie [Inleiding in integratie-API´s voor het sollicitantenvolgsysteem](./hr-admin-integration-ats-api-introduction.md) voor meer informatie over integratie-API´s voor het sollicitantenvolgsysteem (ATS).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Zijn de mogelijkheden die momenteel alleen beschikbaar zijn in Dynamics 365 Human Resources (bijvoorbeeld verlofbeheer en vergoedingenbeheer), beschikbaar nadat de samenvoeging is voltooid?

Ja. Alle mogelijkheden van Dynamics 365 Human Resources-toepassingen worden naar de infrastructuur voor financiën en bedrijfsactiviteiten overgebracht. De functies worden in fasen beschikbaar gemaakt. Controleer regelmatig de [releaseplannen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) voor actuele informatie over de beschikbaarheid van functies voor de samengevoegde infrastructuur.

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Zijn Ceridian-integraties met Dynamics 365 Human Resources beschikbaar nadat de infrastructuursamenvoeging is voltooid?

Ceridian is bezig met het maken van een V2-integratie met Dynamics 365 Human Resources waarbij gebruik wordt gemaakt van de API's voor salarisadministratie. De op bestanden gebaseerde integratie die momenteel bestaat in Dynamics 365 Human Resources, wordt niet naar de infrastructuur voor financiën en bedrijfsactiviteiten gemigreerd. Zie [Inleiding tot Salaris-API](./hr-admin-integration-payroll-api-introduction.md) voor meer informatie.

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Wordt de functionaliteit van sollicitantenvolgsystemen of onboarding/offboarding van werknemers opgenomen?

In vorige releases hebben we de API voor ATS-integratie (Applicant Tracking System) gemaakt om partners en klanten in staat te stellen ATS-integraties met Human Resources te maken. Extra aan ATS gerelateerde functionaliteit werd in 2022 wave 1 beschikbaar. Deze API's zullen in toekomstige releases verder worden verbeterd.

De HR-functionaliteit die momenteel bestaat in de infrastructuur voor financiën en bedrijfsactiviteiten, omvat een aantal functies voor wervingsbeheer dat niet bestaat in Dynamics 365 Human Resources. Na samenvoeging van de infrastructuur wordt deze functionaliteit beschikbaar voor alle klanten van Human Resources. Deze functionaliteit biedt lichte ATS-functionaliteit. We zijn echter niet van plan om deze functionaliteit in de toekomst uit te breiden. Klanten die meer geavanceerde functionaliteit nodig hebben, kunnen gebruikmaken van ATS-integraties van partners. Zie [Inleiding in integratie-API´s voor het sollicitantenvolgsysteem](./hr-admin-integration-ats-api-introduction.md) voor meer informatie over integratie-API´s voor het sollicitantenvolgsysteem (ATS).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Worden de upgradeprogramma's van Dynamics AX 2012 gebruikt voor het upgraden van de HR-module in AX 2012 naar de Dynamics 365 Human Resources-app?

Ja. Een upgrade van Dynamics AX 2012 naar Dynamics 365 Human Resources volgt hetzelfde upgradepad en gebruikt dezelfde hulpprogramma's als die worden gebruikt voor een upgrade naar de meest recente versie van andere Dynamics 365-apps voor bedrijfsactiviteiten zoals Dynamics 365 Finance of Dynamics 365 Supply Chain Management.

Zie [Veelgestelde vragen over Human Resources-klantmigratie](./customer-migration.md) voor meer informatie over de migratie naar de infrastructuur voor financiën en bedrijfsactiviteiten.
