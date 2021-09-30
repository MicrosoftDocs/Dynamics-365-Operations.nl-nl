---
title: GS1-streepjescodes en QR-codes
description: In dit onderwerp wordt beschreven hoe u GS1-streepjescodes en QR-codes in moet stellen zodat labels in een magazijn kunnen worden gescand.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8f438e18356a6c16cc75bb59153ae7353d984a5a
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500325"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1-streepjescodes en QR-codes

[!include [banner](../includes/banner.md)]

Magazijnmedewerkers moeten vaak verschillende taken uitvoeren wanneer ze een mobiele scanner gebruiken om de verplaatsing van een artikel, palet of container te registreren. Dit zijn bijvoorbeeld taken zoals het scannen van streepjescodes en het handmatig invoeren van gegevens op het mobiele apparaat. Voor de streepjescodes wordt een bedrijfsspecifieke indeling gebruikt die u met Microsoft Dynamics 365 Supply Chain Management definieert en beheert.

GS1-streepjescode- en QR-code-indelingen voor verzendlabels zijn ontwikkeld om een globale standaard te bieden voor de uitwisseling van gegevens tussen bedrijven. Met GS1-indelingen worden niet alleen de gegevens gecodeerd, maar kunt u ook een vooraf gedefinieerde lijst met *toepassings-id's* gebruiken om de betekenis van de gegevens te definiëren. Met de GS1-standaard definieert u de gegevensindeling en de verschillende soorten gegevens die kunnen worden gebruikt om te coderen. GS1-streepjescodes kunnen, in tegenstelling tot oudere streepjescodes, meerdere gegevenselementen hebben. Daarom kunt u met één streepjescodescan verschillende typen productgegevens vastleggen, zoals de batch en de vervaldatum.

GS1-ondersteuning in Supply Chain Management vereenvoudigt het scanproces in magazijnen enorm, waarbij pallets en containers worden gelabeld met codes in GS1-indeling. Magazijnmedewerkers kunnen alle vereiste informatie extraheren via één scan van een GS1-streepjescode. Doordat er niet meer meerdere scans hoeven te worden gemaakt en/of gegevens niet meer handmatig hoeven te worden ingevoerd, bent u met GS1-streepjescodes minder tijd kwijt aan dit soort taken. Tegelijkertijd zorgen ze ook voor een betere nauwkeurigheid.

Logistieke managers moeten de vereiste lijst met toepassings-id's instellen en elk van deze id's koppelen aan de juiste menuopdrachten voor mobiele apparaten. De toepassings-id's kunnen vervolgens in verschillende magazijnen worden gebruikt als algemene instelling voor verplaatsen en verpakken. Daarom krijgen alle verzendlabels een uniforme vorm.

Tenzij anders aangegeven, wordt in dit onderwerp de term *streepjescode* gebruikt om naar zowel streepjescodes als QR-codes te verwijzen.

## <a name="turn-on-the-gs1-feature"></a>De GS1-functie inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *GS1-streepjescodes scannen*

## <a name="set-up-global-gs1-options"></a>Algemene GS1-opties instellen

Op de pagina **Parameters voor magazijnbeheer** vindt u enkele instellingen voor algemene GS1-opties.

Volg deze stappen om algemene GS1-opties in te stellen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het sneltabblad **Streepjescodes** de volgende velden in:

    - **FNC1-teken**: geef tekens op die moeten worden geïnterpreteerd als voorvoegsel wanneer een streepjescode wordt geparseerd.
    - **Datamatrix-teken**: geef tekens op die moeten worden geïnterpreteerd als voorvoegsel wanneer een datamatrix wordt geparseerd.
    - **QR-codeteken**: geef tekens op die moeten worden geïnterpreteerd als voorvoegsel wanneer een QR-code wordt geparseerd.
    - **Groepsscheidingsteken:** geef het teken op waarmee afzonderlijke delen van een streepjescode of QR-code worden aangegeven.
    - **Maximale lengte van id**: geef het maximumaantal tekens op dat voor de toepassings-id is toegestaan.

> [!NOTE]
> Voorvoegsels geven aan dat een streepjescode wordt gecodeerd volgens de GS1-standaard. Er kunnen maximaal drie voorvoegsels (**FNC1-teken**, **Datamatrix-teken** en **QR-code**) tegelijk en voor verschillende doeleinden worden gebruikt.

## <a name="gs1-application-identifiers"></a>GS1-toepassings-id's

Met GS1-indelingen worden niet alleen de gegevens gecodeerd, maar kunt u ook een vooraf gedefinieerde lijst met toepassings-id's gebruiken om de betekenis van de gegevens te definiëren. Logistieke managers moeten de vereiste lijst met toepassings-id's instellen en elk van deze id's koppelen aan de juiste menuopdrachten voor mobiele apparaten. De id's kunnen vervolgens in verschillende magazijnen worden gebruikt als algemene instelling voor verplaatsen en verpakken. Daarom krijgen alle verzendlabels een uniforme vorm.

Door het systeem worden de gegevens gebruikt, met name de vooraf gedefinieerde toepassings-id's, om de regels vast te stellen die moeten worden toegepast op de relevante gescande informatie.

Elke toepassings-id geeft aan het systeem door dat opeenvolgende tekens in de gescande streepjescode als een blok gecodeerde informatie moeten worden beschouwd. De instellingen van de toepassings-id's bepalen hoe een streepjescode moet worden geïnterpreteerd en worden opgeslagen als een waarde in het systeem.

Logistiek managers kunnen internationale standaardtoepassings-id's gebruiken en/of hun eigen id maken.

### <a name="load-the-standard-application-identifiers"></a>De standaardtoepassings-id's laden

U kunt een lijst met algemene internationale toepassings-id's laden om snel aan de slag te gaan. U kunt de lijst vervolgens later naar wens uitbreiden of bewerken.

Volg deze stappen om de standaardtoepassings-id's te laden.

1. Ga naar **Magazijnbeheer \> Instellen \> GS1 \> GS1-toepassings-id's**.
1. Selecteer **Standaardinstelling maken** in het actievenster.

> [!WARNING]
> Met de opdracht **Standaardinstellingen maken** worden alle momenteel gedefinieerde toepassings-id's verwijderd en door de standaardlijst vervangen. Nadat u de standaardinstellingen hebt geladen, kunt u de lijst echter naar wens aanpassen.

### <a name="set-up-custom-application-identifiers"></a>Aangepaste toepassings-id's instellen

Als een aantal of alle toepassings-id's die uw bedrijf gebruikt, afwijken van de standaardset, kunt u uw eigen codes zelf maken of de standaardset naar wens aanpassen.

Volg deze stappen als u uw eigen GS1-toepassings-id's wilt instellen en aanpassen.

1. Ga naar **Magazijnbeheer \> Instellen \> GS1 \> GS1-toepassings-id's**.
1. Volg één van deze stappen:

    - Selecteer **Nieuw** in het actievenster om een nieuwe id te maken.
    - Als u een bestaande id wilt bewerken, selecteert u de id en selecteert u vervolgens **Bewerken** in het actievenster.

1. Stel de volgende velden in voor de nieuwe of geselecteerde id:

    - **Toepassings-id**: voer de identificatiecode voor de toepassings-id in. Normaal gesproken is deze code een geheel getal met twee cijfers, maar dit kan langer zijn. Voor decimale waarden geeft het laatste cijfer het aantal decimalen aan. Zie de omschrijving van het selectievakje **Decimaal** later in deze lijst voor meer informatie.
    - **Omschrijving**: voer een korte omschrijving van de id in.
    - **Vaste lengte**: schakel dit selectievakje in als waarden die met deze toepassings-id worden gescand een vast aantal tekens hebben. Schakel dit selectievakje in als de lengte van waarden variabel is. In dit geval moet u het einde van de waarde aangeven met behulp van het groepsscheidingsteken dat u hebt opgegeven op de pagina **Parameters van magazijnbeheer**.
    - **Lengte**: voer het maximumaantal tekens in dat kan worden weergegeven in de waarden die worden gescand met deze toepassings-id. Als het selectievakje **Vaste lengte** is ingeschakeld, wordt precies dit aantal tekens verwacht.
    - **Type**: selecteer het type waarde dat wordt gescand met deze toepassings-id (*Numeriek*, *Alfanumeriek* of *Datum*). Voor datums is de verwachte indeling JJMMDD (zonder spaties of koppeltekens).
    - **Decimaal**: schakel dit selectievakje in als de waarde een impliciet decimaalteken bevat. Als dit vakje is ingeschakeld, wordt het laatste cijfer van de toepassings-id gebruikt om het aantal decimale plaatsen te bepalen. Als de toepassings-id bijvoorbeeld *3205* is, worden de meest rechtse vijf cijfers van de waarde geïnterpreteerd als komend na het decimaalteken.

> [!NOTE]
> Het groepsscheidingsteken dat op de pagina **Parameters van magazijnbeheer** is opgegeven, is optioneel als een waarde die door een toepassings-id wordt gevolgd een vaste lengte heeft of als de lengte ervan wordt gemaximaliseerd (dat wil zeggen: als de lengte gelijk is aan de waarde **Lengte** die voor de toepassings-id is ingesteld).

## <a name="establish-the-generic-gs1-setup"></a>De algemene GS1-instellingen instellen

Met de algemene GS1-instellingen wordt een verzameling gemeenschappelijke toewijzingen tot stand gebracht. Met deze toewijzingen wordt elk relevant invoerveld in de mobiele app gekoppeld aan de toepassings-id waarmee wordt bepaald hoe waarden van gescande streepjescodes moeten worden geïnterpreteerd en opgeslagen in dat veld. Standaard zijn deze instellingen van toepassing op alle scans voor alle menuopdrachten van een mobiel apparaat. Deze kunnen echter voor een of meer specifieke velden worden overschreven door een GS1-beleid dat aan een specifiek menuopdracht is toegewezen.

Met de algemene GS1-instellingen kan maar één waarde tegelijk worden gescand. Als u meerdere veldwaarden van één scan wilt laden, moet u daarom een GS1-beleid instellen voor de relevante menuopdrachten.

Zie het volgende onderdeel voor meer informatie over GS1-beleidsregels.

### <a name="load-the-standard-generic-gs1-setup"></a>De algemene GS1-standaardinstellingen laden

Op de pagina **Algemene GS1-instellingen** kunt u een standaardset toewijzingen laden tussen velden van mobiele apparaten en standaardtoepassings-id's die door de standaardinstelling zijn gemaakt.

Voor het tot stand brengen van de algemene GS1-instellingen gaat u naar **Magazijnbeheer \> Instellingen \> GS1 \> Algemene GS1-instellingen**. Selecteer vervolgens **Standaardinstellingen maken** om automatisch een geschikte toepassings-id toe te wijzen aan elk veld dat meestal door menuopdrachten van een mobiel apparaat wordt gebruikt.

> [!WARNING]
> Als er al algemene GS1-instellingen bestaan, worden deze door de opdracht **Standaardinstellingen maken** volledig verwijderd en worden de standaardinstellingen geladen.

### <a name="customize-the-standard-generic-gs1-setup"></a>Algemene GS1-standaardinstellingen aanpassen

Volg deze stappen om de algemene GS1-instellingen te voltooien.

1. Ga naar **Magazijnbeheer \> Instellingen \> GS1 \> Algemene GS1-instellingen**.
1. Volg één van deze stappen:

    - Selecteer in het actievenster **Nieuw** om een nieuwe toewijzing te maken.
    - Als u een bestaande toewijzing wilt bewerken, selecteert u de toewijzing en selecteert u vervolgens **Bewerken** in het actievenster.

1. Stel de volgende velden in voor de nieuwe of geselecteerde toewijzing:

    - **Veld**: selecteer of voer het invoerveld voor de mobiele app in waar de inkomende waarde aan moet worden toegewezen. De waarde is niet de weergavenaam die medewerkers zien. In plaats daarvan is dit de sleutelnaam die aan het veld in de onderliggende code wordt toegewezen. De standaardinstellingen bieden een verzameling velden die waarschijnlijk handig kunnen zijn. Ook bevatten ze de intuïtieve sleutelnamen voor elk veld en de bijbehorende geprogrammeerde functionaliteit. Het kan echter nodig zijn om met uw ontwikkelingspartners te praten om de juiste selecties voor uw implementatie te vinden.
    - **Toepassings-id**: selecteer de toepasselijke toepassings-id, zoals gedefinieerd op de pagina **GS1-toepassings-id's**. De id geeft aan hoe de streepjescode wordt geïnterpreteerd en opgeslagen als een waarde voor het benoemde veld. Nadat u een toepassings-id hebt geselecteerd, wordt in het veld **Omschrijving** de omschrijving van deze id weergegeven.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>GS1-beleid instellen dat u aan menuopdrachten voor mobiele apparaten kunt toewijzen

Het doel van de GS1-standaard is dat medewerkers verschillende waarden kunnen laden wanneer ze één streepjescode één keer scannen. Logistiek managers moeten hiervoor een GS1-beleid instellen om aan te geven hoe streepjescodes met meerdere waarden moeten worden geïnterpreteerd. Later kunt u beleid toewijzen aan menuopdrachten van mobiele apparaten om te bepalen hoe een streepjescode wordt geïnterpreteerd wanneer medewerkers deze scannen terwijl ze een bepaalde menuopdracht gebruiken.

Als er geen GS1-beleid is toegewezen aan een menu-item, kan slechts één waarde worden vastgelegd. Deze waarde wordt toegepast op de invoer voor de mobiele app die wordt geselecteerd wanneer de medewerker de scan maakt, zoals is opgegeven in de algemene GS1-instellingen. Als er een GS1-beleid is toegewezen aan het menuopdracht, gebruikt het systeem nog steeds de algemene GS1-instellingen om de eerste streepjescodewaarde aan het geselecteerde veld toe te wijzen. Vervolgens kunnen echter aanvullende veldwaarden worden vastgelegd, zoals opgegeven in het toepasselijke beleid.

### <a name="load-the-standard-specific-gs1-policies"></a>Het specifieke GS1-standaardbeleid laden

U kunt een set GS1-beleidsregels laden om snel aan de slag te gaan. U kunt de beleidsregels vervolgens later naar wens uitbreiden of bewerken.

Volg deze stappen om de standaardtoepassings-id's te laden.

1. Ga naar **Magazijnbeheer\>  Instellingen \> GS1 \> GS1-beleid**.
1. Selecteer **Standaardinstelling maken** in het actievenster.

> [!WARNING]
> Met de opdracht **Standaardinstellingen maken** worden alle momenteel gedefinieerde beleidsregels verwijderd en door de standaardset met beleidsregels vervangen. Nadat u de standaardinstellingen hebt geladen, kunt u de beleidsregels echter naar wens aanpassen.

### <a name="set-up-custom-specific-gs1-policies"></a>Aangepast specifiek GS1-beleid instellen

Volg deze stappen om uw GS1-beleid in te stellen en aan te passen.

1. Ga naar **Magazijnbeheer\>  Instellingen \> GS1 \> GS1-beleid**.
1. Volg één van deze stappen:

    - Selecteer in het actievenster **Nieuw** om een nieuw beleid te maken.
    - Als u een bestaand beleid wilt bewerken, selecteert u het beleid in het lijstvenster.

1. Stel in de koptekst van het nieuwe of geselecteerde beleid de volgende velden in:

    - **Beleidsnaam**: voer een naam voor het beleid in.
    - **Omschrijving**: voer een korte omschrijving van het beleid in.

1. Wijs in het sneltabblad onder de koptekst veldnamen toe aan de toepassings-id's die zijn vereist voor het huidige beleid. Gebruik de knoppen op de werkbalk om de gewenste rijen toe te voegen of te verwijderen. Stel voor elke rij de volgende velden in:

    - **Veld**: selecteer of voer het invoerveld voor de mobiele app in waar de inkomende waarde aan moet worden toegewezen. De waarde is niet de weergavenaam die medewerkers zien. In plaats daarvan is dit de sleutelnaam die aan het veld in de onderliggende code wordt toegewezen. De standaardinstellingen bieden een verzameling velden die waarschijnlijk handig kunnen zijn. Ook bevatten ze de intuïtieve sleutelnamen voor elk veld en de bijbehorende geprogrammeerde functionaliteit. Het kan echter nodig zijn om met uw ontwikkelingspartners te praten om de juiste selecties voor uw implementatie te vinden.
    - **Toepassings-id**: selecteer de toepasselijke toepassings-id, zoals gedefinieerd op de pagina **GS1-toepassings-id's**. De id geeft aan hoe de streepjescode wordt geïnterpreteerd en opgeslagen als een waarde voor het benoemde veld. Nadat u een toepassings-id hebt geselecteerd, wordt in het veld **Omschrijving** de omschrijving van deze id weergegeven.
    - **Sorteren**: elke streepjescode met meerdere waarden bevat een reeks toepassings-id's, die elk worden gevolgd door een waarde. Het toepasselijke GS1-beleid bepaalt welke toepassings-id aan elk databaseveld wordt toegevoegd. Als een streepjescode dezelfde toepassings-id echter meerdere keren gebruikt, wordt de volgorde gebruikt waarin toepassings-id's in de code worden weergegeven om deze aan velden toe te wijzen. Voor rijen die een toepassings-id delen met een of meer andere rijen, gebruikt u dit veld om de volgorde te bepalen waarin de overeenkomende rijen worden verwerkt. De rij met de laagste sorteerwaarde wordt als eerste verwerkt.

> [!NOTE]
> Voor streepjescodes die meer dan één identieke toepassings-id bevatten, *moet* u het veld **Sorteren** gebruiken om de volgorde van de velden te bepalen.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1-beleid toewijzen aan menuopdrachten voor mobiele apparaten

Standaard bieden alle menuopdrachten voor mobiele apparaten invoervelden waarin medewerkers één waarde kunnen scannen volgens de algemene GS1-instellingen. Als u wilt dat medewerkers meerdere veldwaarden in een enkele scan kunnen scannen voor een menuopdracht van een mobiel apparaat, moet u aan de hand van deze stappen een GS1-beleid toewijzen.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Maak of open een menuopdracht.
1. Stel op het sneltabblad **Algemeen** het veld **GS1-beleid** in op het beleid dat op de menuopdracht van toepassing is.

## <a name="gs1-setup-example"></a>Voorbeeld van GS1-instellingen

Dit voorbeeld is van toepassing op een systeem waarbij de GS1-opties als volgt worden ingesteld:

- Op de pagina **Parameters van magazijnbeheer** zijn de volgende algemene instellingen vastgelegd:

  - **FNC1-teken:** *\]C1*
  - **Groepsscheidingsteken:** *\~*

- Op de pagina **GS1-toepassings-id's** zijn de volgende toepassings-id's relevant voor dit voorbeeld.

    | Toepassings-id | Beschrijving | Vaste lengte | Lengte | Type | Decimaal |
    |---|---|---|---|---|---|
    | 01 | GTIN | Selectie | 14 | Numeriek | Verrekend |
    | 10 | Batchnummer | Verrekend | 20 | Alfanumeriek | Verrekend |
    | 17 | Vervaldatum | Selectie | 6 | Datum | Verrekend |
    | 30 | Ontvangen hoeveelheid | Verrekend | 8 | Numeriek | Verrekend |

- Op de pagina **Algemene GS1-instellingen** zijn de volgende instellingen voor het algemene GS1-beleid relevant voor dit voorbeeld.

    | Veld | Toepassings-id | Beschrijving |
    |---|---|---|
    | ItemId | 01 | GTIN |

- Op de pagina **GS1-beleid** staat het beleid waarbij het veld **Beleidsnaam** is ingesteld *Inkoop ontvangen*. Dit beleid bevat de volgende regels.

    | Veld | Toepassings-id | Beschrijving | Sorteren |
    |---|---|---|---|
    | ExpDate | 17 | Vervaldatum | 0 |
    | InventBatchId | 10 | Batchnummer | 0 |
    | Hoeveelheid | 30 | Ontvangen hoeveelheid | 0 |

- Op de pagina **Menuopdracht van mobiel apparaat** is er een menuopdracht met de naam *Inkoop ontvangen*. Het veld **GS1-beleid** is ingesteld op *Inkoop ontvangen*.

Nadat goederen voor een inkooporder in het magazijn zijn binnengekomen, volgt de medewerker deze stappen.

1. Selecteer op het mobiele apparaat de menuopdracht **Inkoop ontvangen**.
1. Voer het inkoopordernummer in.
1. Selecteer het veld **Item** en scan de volgende streepjescode: *\]C10100000012345678\~3030\~10b1\~17220215*.

Vanwege de instellingen die voor dit voorbeeld zijn vastgelegd, wordt de gescande streepjescode op de volgende manier gescand.

| Veldsleutel | Sollicitatie-ID | Waarde | Notitie |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Omdat de medewerker naar het veld **Item** heeft gescand, wordt de eerste waarde in de streepjescode aan dat veld toegewezen. De toewijzing wordt overgenomen uit de algemene GS1-instellingen. |
| Hoeveelheid | 30 | 30 | Aangezien verschillende veldwaarden in één scan worden vastgelegd, worden deze toewijzing en alle resterende toewijzingen overgenomen uit het GS1-beleid dat is toegewezen aan de menuopdracht **Inkoop ontvangen**. Deze warde is de hoeveelheid die is ontvangen. |
| InventBatchId | 10 | b1 | Deze waarde is de batch-id. |
| ExpDate | 17 | 220215 | De datumnotatie is JJMMDD. De vervaldatum is daarom 15 februari 2022. |

De ontvangst wordt vervolgens geregistreerd en de relevante databasewaarden worden na de ene scan ingevoerd.
