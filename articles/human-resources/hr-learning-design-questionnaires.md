---
title: Vragenlijsten ontwerpen
description: Dit artikel beschrijft het proces om een vragenlijst te maken. Als eerste stap ontwerpt u de vragenlijst Wanneer u een vragenlijst ontwerpt, schrijft u niet alleen de vragen en antwoorden, maar maakt u ook de structuur waardoor antwoorden worden geregistreerd en getabelleerd.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: da4250b281438c29c82150af8db9cb8cca41c6c9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418043"
---
# <a name="design-questionnaires"></a>Vragenlijsten ontwerpen

Dit artikel beschrijft het proces om een vragenlijst te maken. Als eerste stap ontwerpt u de vragenlijst Wanneer u een vragenlijst ontwerpt, schrijft u niet alleen de vragen en antwoorden, maar maakt u ook de structuur waardoor antwoorden worden geregistreerd en getabelleerd. 

Door een vragenlijst zorgvuldig te ontwerpen, verhoogt u de kwaliteit van de gegevens die u verzamelt. Door een zorgvuldig ontwerp kunt u op het juiste moment beter de gewenste opties selecteren voor een vragenlijst. De volgende punten kunnen u helpen bij het plannen van een effectieve vragenlijst:

-   Definieer duidelijk het doel van de vragenlijst om te zorgen dat de vragen het doel ondersteunen.
-   Bepaal welke afzonderlijke persoon of groep mensen de vragenlijst moet invullen.
-   Schrijf vragen die worden weergegeven op de vragenlijst en neem antwoordopties op, indien van toepassing.
-   Zorg ervoor dat de vragenlijst logisch is opgebouwd, zodat de respondenten geïnteresseerd blijven.
-   Plaats vragen en antwoorden in de volgorde waarin ze moeten verschijnen voor respondenten.
-   Kies hoe de resultaten moeten worden geëvalueerd, indien van toepassing.
-   Bepaal of u extra functies nodig hebt. Bepaal bijvoorbeeld of en hoe resultaten moeten worden gecategoriseerd, of een tijdslimiet is vereist en of alle vragen verplicht zijn.

De ontwerpfase bevat vier categorieën van taken die u in deze volgorde moet voltooien:

1.  Stel vereisten in, indien nodig.
2.  Stel antwoordgroepen en antwoorden in, indien van toepassing.
3.  Stel vragen en de koppeling ervan met de antwoordgroepen in.
4.  Stel de vragenlijst zelf in en koppel er vragen aan.

## <a name="prerequisites"></a>Vereisten
Voordat u vragenlijsten en vragen kunt maken, moet u de voorwaarden opgeven. Echter, niet alle voorwaarden zijn vereist voor volledige functionaliteit.

### <a name="required"></a>Vereist

| Vereiste        | Beschrijving                |
|---------------------|----------------------------|
| Typen vragenlijst | Vragenlijsten categoriseren. |
| Vraagtypen      | Vragen categoriseren.      |

### <a name="optional"></a>Optioneel

| Vereiste             | Beschrijving                                                    |
|--------------------------|----------------------------------------------------------------|
| Vragenlijstparameters | Basisbesturingselementen en standaardinstellingen voor vragenlijsten wijzigen. |

### <a name="questionnaire-types"></a>Typen vragenlijst

Vragenlijsttypen zijn vereist en moeten worden toegewezen bij het maken van een vragenlijst. Met deze vragenlijsttypen kunt u vragenlijsten eenvoudiger beheren en classificeren. Gebruik vragenlijsttypen om vragenlijsten te classificeren en ze van elkaar te onderscheiden. Als u bijvoorbeeld meerdere vragenlijsten kunt selecteren, kunt u ze filteren op type om zo een specifieke vragenlijst gemakkelijker terug te kunnen vinden. Hieronder staan enkele voorbeelden van vragenlijsttypen:

-   Personeelontwikkeling
-   Klantenquêtes
-   Controleproces

### <a name="question-types"></a>Vraagtypen

Vraagtypen zijn vereist en moeten worden toegewezen bij het maken van een vraag. 

Gebruik vraagtypen om vragen voor rapportage te categoriseren. De vraagtypen maken het eenvoudiger om ook vragen te zoeken, omdat u typen kunt gebruiken als filters op de pagina **Vragen**. Hieronder staan enkele voorbeelden van vraagtypen:

-   Personeelsbeleid
-   Management
-   Cursusevaluatie

### <a name="questionnaire-parameters"></a>Vragenlijstparameters

Vragenlijstparameters zijn optioneel. U kunt ze ook niet gebruiken, afhankelijk van de behoeften van uw bedrijf. 

Vragenlijstparameters bepalen de anonimiteit, nummerreekscodes en verwijzingstypen van een vragenlijst. Wanneer een organisatie een vragenlijst distribueert, kan de optie om respondenten toe te staan anoniem te blijven problematisch zijn. 

De nummerreekscodes worden gebruikt voor het ordenen van vragen en antwoorden. Op basis van deze nummerreekscodes worden waarden automatisch toegewezen aan artikelen. 

Definieer eerst alle parameters voordat u uw gegevens gaat maken. U kunt de instellingen van de vragenlijst op elk gewenst moment wijzigen.

## <a name="questionnaire-components"></a>Vragenlijstonderdelen
Vragenlijsten bestaat uit drie hoofdelementen: antwoordgroepen die de antwoorden voor meerkeuzevragen bevatten, en de vragenlijst zelf.  U kunt de vragen in een vragenlijst desgewenst in resultaatgroepen groeperen. Met resultaatgroepen kunt u vragen categoriseren en hebt u een nadere analyse op de vragenlijst. 

[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Antwoordgroepen en antwoorden

Er zijn twee manieren waarop respondenten een vraag kunnen beantwoorden, afhankelijk van het onderwerp van de vraag:

-   De open vragen vereisen geen antwoorden in een specifieke indeling. Respondenten kunnen een antwoord typen als tekst, een getal, een datum of een tijd. Bij deze vragen moeten respondenten meestal subjectieve informatie geven in hun antwoord, bijvoorbeeld een mening, beschrijving, beoordeling of schatting.
-   Meerkeuzevragen vereisen dat de respondent een antwoord in een lijst van mogelijke juiste antwoorden selecteert.

Om een lijst van mogelijke antwoorden voor meerkeuzevragen te geven, kunt u antwoorden op de pagina **Antwoordgroepen** maken. 

Antwoordgroepen en antwoorden zijn onderdelen van de hoeveelheid informatie waarvan de vragen worden gemaakt. Nadat u een antwoordgroep hebt gemaakt, kunt u de antwoordgroep aan een vraag koppelen in het veld **Antwoordgroep** op de pagina **Vragen**. 

U kunt een antwoordgroep gebruiken voor meer dan één vraag in dezelfde vragenlijst en in meer dan één vragenlijst. 

> [!NOTE]
> Als u antwoordtekst in antwoordgroepen aanpast die al is gebruikt op ingevulde vragenlijsten, kunnen de gegevens moeilijk te beoordelen worden, en zijn de vragenlijstresultaten mogelijk niet meer geldig. Als u een antwoordgroep moet wijzigen, overweeg dan om een nieuwe antwoordgroep te maken in plaats van het een bestaande te wijzigen. U kunt geen antwoordgroepen verwijderen die aan een vraag of antwoord zijn gekoppeld, of die zijn beantwoord.

### <a name="questions"></a>Vragen

Een vragenlijst moet vragen bevatten. Vragen kan open of meerkeuze zijn.

-   Antwoorden op open vragen worden niet geregeld en respondenten kunnen hun antwoorden typen.
-   Bij meerkeuzevragen is een lijst met vooraf gedefinieerde antwoordopties nodig en de vragen kunnen worden gestructureerd zodat een respondent een of meer antwoorden kan selecteren. De vragen moeten zijn ontworpen om specifieke informatie van een respondent te onthullen en moeten aan een antwoordgroep zijn gekoppeld die de antwoordopties voor elke meerkeuzevraag bevat. 

    > [!NOTE]
    > Voordat u meerkeuzevragen kunt instellen, moet u antwoordgroepen en antwoorden maken.

Vragen kunnen worden gerangschikt in een voorwaardelijke vragenhiërarchie, zodat secundaire vragen afhankelijk zijn van het antwoord dat de respondent op de vorige vraag heeft geselecteerd. U kunt de vragen eerst schrijven en ze vervolgens later in een hiërarchie ordenen.

## <a name="setting-up-questionnaires"></a>Vragenlijsten instellen

> [!NOTE]
> Voordat u een vragenlijst kunt instellen, moet u vragen, antwoorden en vereisten instellen. 

Voor elke vragenlijst kunt u de volgende informatie opgeven:

-   De totale tijd of tijdlimiet voor het beantwoorden van verplichte vragen.
-   Of alle vragen verplicht zijn.
-   Of u punten berekent in een vragenlijst.
-   Hoe u resultaten categoriseert.
-   Of de vragenlijst voor een beperkte set van respondenten beschikbaar is.
-   Of een formuliersjabloon moet worden weergegeven als achtergrond voor elke pagina van de vragenlijst.
-   Of extra notities vereist zijn om de bedoeling van de vragenlijst te verduidelijken voor de respondenten.
-   Of u vragen wilt weergeven in een vaste volgorde of dat u ze willekeurig uit een groep wilt selecteren.
-   Of vragen alleen worden gesteld als specifieke reacties op eerdere antwoorden zijn gegeven.

### <a name="set-up-a-questionnaire"></a>Een vragenlijst opstellen

De eerste pagina die u gebruikt om een vragenlijst in te stellen, is de pagina **Vragenlijsten**. Om een vragenlijst in te stellen voert u de volgende taken in deze volgorde uit:

1.  Een vragenlijst maken.
2.  Volg één van deze stappen om vragen in de vragenlijst te koppelen:
    -   Als u resultaatgroepen gebruikt, kunt u vragen aan een vragenlijst toevoegen door resultaatgroepen te gebruiken. Stel eerst de resultaatgroepen voor de vragenlijst in en voegt vervolgens vragen aan de resultaatgroepen toe.
    -   Als u geen gebruik wilt maken van resultaatgroepen, kunt u vragen rechtstreeks aan de vragenlijst koppelen.

3.  Een voorwaardelijke vragenhiërarchie instellen, indien nodig.
4.  De vragenlijst testen.

Klik op de pagina **Vragenlijsten** op **Valideren** om te testen of de vragenlijst juist is samengesteld. Wij raden u ook aan de vragenlijst in te vullen en zelf te testen voordat u deze distribueert.

### <a name="modify-a-questionnaire"></a>Een vragenlijst wijzigen

Op de pagina **Vragenlijsten** kunt u de volgende taken uitvoeren:

-   Informatie in de vragenlijst bewerken, zoals de resultaatgroepen en vragen.
-   Vragen verwijderen en toevoegen.
-   Wijzigingen aanbrengen in de resultaatgroepen en het volgnummer. 

> [!CAUTION]
> Wees voorzichtig wanneer u wijzigingen aanbrengt in vragenlijsten die al zijn beantwoord. Wijzigingen kunnen de juistheid van de statistieken negatief beïnvloeden, wat kan leiden tot een zwakke basis voor evaluatie. Het is beter een nieuwe vraag te maken dan er een te wijzigen die al is beantwoord.

In een vragenlijst kunt u de volgende typen vragen verwijderen:

-   Vragen die zijn gekoppeld aan een vragenlijst
-   Vragen die al zijn beantwoord en daarom worden weergegeven in het dialoogvenster **Antwoorden**.

### <a name="result-groups"></a>Resultaatgroepen

Resultaatgroepen zijn optioneel wanneer u vragen aan een vragenlijst koppelt. 

Een resultaatgroep wordt gebruikt om punten te berekenen en de resultaten van een vragenlijst te categoriseren. Als u resultaatgroepen gebruikt, kunt u de volgende taken uitvoeren:

-   Vragenlijstresultaten evalueren op basis van puntenstatistieken.
-   De score van een respondent evalueren voor elke ingestelde resultaatgroep.
-   Statistieken genereren voor elke resultaatgroep waarmee u de resultaten beter kunt analyseren.
-   Een rapport afdrukken met de resultaten voor elke resultaatgroep en ook optionele punten/teksten die zijn gebaseerd op punten die zijn verdiend in elke resultaatgroep.

> [!NOTE]
> Voordat u resultaatgroepen kunt configureren, moet u de volgende taken uitvoeren:

-   Gesloten vragen instellen. Voor een meerkeuzevraag, moet op de pagina **Vragen** het invoertype **Selectievakje**, **Alternatieve knop** of **Keuzelijst met invoervak** zijn.
-   Punten definiëren voor antwoorden in de antwoordgroepen die aan elke vraag zijn toegewezen.
-   Een vragenlijst opstellen.

Als u vragen wilt koppelen aan een vragenlijst door resultaatgroepen te gebruiken, moet u eerst resultaatgroepen instellen voor de vragenlijst en vervolgens vragen toevoegen aan de resultaatgroepen. Als u geen gebruik wilt maken van resultaatgroepen, kunt u vragen rechtstreeks aan een vragenlijst koppelen. 

U kunt meerdere resultaatgroepen instellen om de punten die door een respondent in elke categorie zijn verdiend, te evalueren. Nadat een vragenlijst is voltooid, kunt u de behaalde punten voor elke resultatengroep weergeven. 

> [!TIP]
> Als u een vragenlijst met punten wilt evalueren, maar niet voor afzonderlijke categorieën, kunt u alle vragen toevoegen aan één resultaatgroep. 

Voor elke resultaatgroep kunt u ook een of meer op punten gebaseerde berichten instellen die respondenten ontvangen nadat ze de vragenlijst hebben voltooid. De weergegeven tekst kan variëren afhankelijk van de score die een respondent bereikt in een resultaatgroep. Als u op punten gebaseerde berichten gebruikt, definieert u puntenintervallen en een omschrijving van elk interval. Als een respondent een score behaalt in een bepaald interval, wordt de tekst voor dat interval opgenomen in het resultaatrapport. 

Omdat een resultaatgroep betrekking heeft op punten die zijn gekoppeld aan specifieke groepen vragen op een vragenlijst, moet u een bepaalde resultaatgroep gebruiken voor een vragenlijst.

#### <a name="example-pointstexts-for-result-group-3"></a>Voorbeeld: punten/teksten voor resultaatgroep 3

U gebruikt een vragenlijst die voor een leiderschapstest 15 vragen in drie categorieën bevat. U maakt drie resultaatgroepen en voegt vijf vragen aan elke resultaatgroep toe. De punten worden vervolgens ingediend in de drie groepen. Dit zijn de drie resultaatgroepen:

-   Creatieve vaardigheden
-   Leiderschapsvaardigheden
-   Technische vaardigheden

Als u op punten gebaseerde berichten gebruikt, kunt u tekstintervallen voor elke resultaatgroep instellen. Aan elke vraag worden twee punten toegewezen. Daarom is het maximale puntentotaal in elke resultaatgroep 10. 

De volgende tabel geeft de op punten gebaseerde berichten weer die u voor de resultaatgroep "leidingsmogelijkheden" definieert.

| Punteninterval | Tekst                                       |
|----------------|--------------------------------------------|
| 1 tot 3         | U hebt gemiddelde leiderschapsvaardigheden.     |
| 4 tot 7         | U hebt goede leiderschapsvaardigheden.        |
| 8 tot 10        | U hebt uitstekende leiderschapsvaardigheden. |

U kunt puntintervallen en teksten instellen voor elke resultaatgroep op een vragenlijst. Teksten die overeenkomen met de score van elke respondent, worden voor elke resultaatgroep weergegeven. 

> [!NOTE]
> U kunt intervallen en teksten veranderen. Als een vragenlijst is voltooid, kunnen wijzigingen echter resulteren in verschillen tussen eerdere en nieuwe resultaatrapporten.

### <a name="conditional-question-hierarchies"></a>Hiërarchieën van voorwaardelijke vragen

Hiërarchieën van voorwaardelijke vragen zijn optioneel wanneer u een vragenlijst opstelt. 

> [!NOTE]
> Voordat u een hiërarchie van voorwaardelijke vragen kunt maken, moet u vragen waaraan antwoordgroepen zijn toegewezen, aan de vragenlijst koppelen. 

Voor het gebruiken van voorwaardelijke vragen voor het maken van een vraaghiërarchie in een vragenlijst kunt u de volgorde waarin vragen worden weergegeven afhankelijk maken van de antwoorden die door een respondent voor elke vraag worden geselecteerd. Door de vraagvolgorde te baseren op het antwoord van een respondent, kunt u de vragenlijst aanpassen terwijl de respondent hem invult.

#### <a name="examples"></a>Voorbeelden

Een rechtspersoon biedt zowel artikelen als services aan zijn klanten. Zoals meestal gebeurt in zulke gevallen kopen sommige klanten alleen artikelen of alleen diensten af en andere nemen beide af. Wanneer de rechtspersoon dus een klanttevredenheidsonderzoek houdt, wordt er een voorwaardelijke structuur toegepast op de vragenlijst om te voorkomen dat klanten die alleen diensten afnemen vragen moeten beantwoorden over artikelen. 

U kunt een vragenlijst ook zo opzetten dat als een respondent antwoord A selecteert voor vraag 1, vraag 2 de volgende vraag in de vragenreeks is. Als de respondent echter antwoord B voor vraag 1 selecteert, dan is vraag 5 de volgende vraag.