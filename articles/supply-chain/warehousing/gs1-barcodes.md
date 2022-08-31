---
title: GS1-streepjescodes
description: In dit artikel wordt beschreven hoe u GS1-streepjescodes en QR-codes in moet stellen zodat labels in een magazijn kunnen worden gescand.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: e1c1c274054ed1c14c9b3fc0595baa029bf3124d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336360"
---
# <a name="gs1-bar-codes"></a>GS1-streepjescodes

[!include [banner](../includes/banner.md)]

Magazijnmedewerkers moeten vaak verschillende taken uitvoeren wanneer ze een mobiele scanner gebruiken om de verplaatsing van een artikel, palet of container te registreren. Dit zijn bijvoorbeeld taken zoals het scannen van streepjescodes en het handmatig invoeren van gegevens op het mobiele apparaat. Voor de streepjescodes wordt een bedrijfsspecifieke indeling gebruikt die u met Microsoft Dynamics 365 Supply Chain Management definieert en beheert.

GS1-streepjescodes voor verzendlabels zijn ontwikkeld om een globale standaard te bieden voor de uitwisseling van gegevens tussen bedrijven. Deze zijn beschikbaar in lineaire (1D) symbolen (streepjescode-indelingen), zoals GS1-128, en 2D-symbolen, zoals GS1 DataMatrix- en GS1 QR-codes. Met GS1-streepjescodes worden niet alleen gegevens gecodeerd, maar kunt u ook een vooraf gedefinieerde lijst met *toepassings-id's* gebruiken om de betekenis van die gegevens te definiëren. Met de GS1-standaard definieert u de gegevensindeling en de verschillende soorten gegevens die kunnen worden gebruikt om te coderen. GS1-streepjescodes kunnen, in tegenstelling tot oudere streepjescodestandaarden, meerdere gegevenselementen hebben. Daarom kunt u met één streepjescodescan verschillende typen productgegevens vastleggen, zoals de batch en de vervaldatum.

GS1-ondersteuning in Supply Chain Management vereenvoudigt het scanproces in magazijnen enorm, waarbij pallets en containers worden gelabeld met streepjescodes in GS1-indeling. Magazijnmedewerkers kunnen alle vereiste informatie extraheren via één scan van een GS1-streepjescode. Doordat er niet meer meerdere scans hoeven te worden gemaakt en/of gegevens niet meer handmatig hoeven te worden ingevoerd, bent u met GS1-streepjescodes minder tijd kwijt aan dit soort taken. Tegelijkertijd zorgen ze ook voor een betere nauwkeurigheid.

Logistieke managers moeten de vereiste lijst met toepassings-id's instellen en elk van deze id's koppelen aan de juiste menuopdrachten voor mobiele apparaten. De toepassings-id's kunnen vervolgens in verschillende magazijnen worden gebruikt als algemene instelling voor verplaatsen en verpakken. Daarom krijgen alle verzendlabels een uniforme vorm.

Tenzij anders aangegeven, wordt in dit artikel de term *streepjescode* gebruikt om naar zowel lineaire (1D) streepjescodes als 2D-streepjescodes te verwijzen.

## <a name="the-gs1-bar-code-format"></a>De GS1-streepjescode-indeling

De algemene GS1-specificaties bepalen welke symbolen kunnen worden gebruikt voor GS1-streepjescodes en hoe de gegevens in de streepjescode kunnen worden gecodeerd. Deze sectie bevat een korte inleiding op het artikel. Zie de [algemene GS1-specificaties](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf) die door GS1 worden gepubliceerd voor volledige details. Het document met GS1-specificaties wordt regelmatig bijgewerkt en de informatie hierin komt overeen met die in versie 22.0 van de algemene GS1-specificaties.

GS1-streepjescodes gebruiken de volgende symbolen:

- **Lineaire of 1D-streepjescodes**: GS1-128 en GS1 DataBar
- **2D-streepjescodes**: GS1 DataMatrix, GS1-QQR-code en GS1 Dotcode

Daarnaast wordt GS1 speciaal genoemd in GS1-128 genoemd. Dit is een speciaal geval van de normale lineaire streepjescode Code-128, GS1 DataMatrix en GS1-QR-code. Het verschil tussen de GS1-versie en de niet-GS1-versie is de aanwezigheid van een speciaal teken (FNC1) als het eerste teken in de streepjescodegegevens. De aanwezigheid van een FNC1-teken geeft aan dat de gegevens in de streepjescode moeten worden geïnterpreteerd volgens de GS1-specificatie.

De gegevens in de streepjescode zelf bestaan uit meerdere gegevenselementen, die elk door een toepassings-id aan het begin van het veld worden geïdentificeerd. Meestal worden de gegevens ook weergegeven onder de streepjescode in een voor mensen leesbare vorm, waarbij de toepassings-id tussen haakjes wordt weergegeven. Hier volgt een voorbeeld: `(01) 09521101530001 (17) 210119 (10) AB-123`. Deze streepjescode bevat drie elementen:

- **Toepassings-id 01**: het GS1 GTIN (global trade item number)van het artikel.
- **Toepassings-id 17**: de vervaldatum.
- **Toepassings-id 10**: het batchnummer.

De gegevens kunnen voor elk element een vooraf gedefinieerde lengte of een variabele lengte hebben. Er bestaat een vaste lijst met toepassings-id's met vooraf gedefinieerde lengtes. Alle andere toepassings-id's hebben een variabele lengte en de lijst met GS1-toepassings-id's bepaalt de maximumlengte en -indeling van gegevens. Toepassings-id 01 heeft bijvoorbeeld een vooraf gedefinieerde lengte van zestien tekens (twee tekens voor de toepassings-id zelf en vervolgens veertien voor de GTIN) en toepassings-ID 17 heeft een vooraf gedefinieerde lengte van acht tekens (twee tekens voor de toepassings-id zelf en vervolgens zes voor de datum). Toepassings-id 10 heeft echter twee cijfers voor de toepassings-zelf en vervolgens maximaal twintig alfanumerieke tekens.

Wanneer elementen worden gecombineerd en een element een element van variabele lengte volgt, moet er een scheidingsteken worden gebruikt. Dit scheidingsteken kan het speciale FNC1-teken of het groepsscheidingsteken (een niet-afdrukbaar teken met ASCII-code 29 en hexadecimale code 1D) zijn. Het scheidingsteken mag niet na het laatste element worden gebruikt. Hoewel het scheidingsteken ook niet moet worden gebruikt na elementen met een vooraf gedefinieerde lengte, is de aanwezigheid van dit scheidingsteken geen kritieke fout.

In de streepjescodegegevens uit het vorige voorbeeld van een streepjescode die de toepassings-id's 01, 17 en 10 bevat, worden de gegevens in een Code-128-, QR Code- of DataMatrix-symbool gecodeerd als `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` (toepassings-id's worden vet weergegeven). Het is aan te bevelen dat elk element met variabele lengte aan het einde wordt gezet, zodat geen extra groepsscheidingsteken hoeft te worden gebruikt. De streepjescode kan echter ook een andere volgorde van elementen hebben, waarbij het scheidingsteken verplicht is. Hier volgt een voorbeeld: `<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Datums en decimale getallen

Datums worden altijd weergegeven in de indeling *JJMMDD*, waarbij de eeuw van het jaar wordt bepaald door GS1-specificaties. Alleen datums van 49 jaar in het verleden tot en met 50 jaar in de toekomst (in relatie tot het huidige jaar) kunnen worden weergegeven.

Sommige gegevenselementen bevatten decimale getallen. Toepassings-id's 3100, 3101, ... 3105 staan bijvoorbeeld voor een nettogewicht in kilogram. Omdat deze toepassings-id's een vooraf gedefinieerde lengte van 10 hebben, zijn er zes cijfers beschikbaar voor de hoeveelheid. De positie van het decimaalteken wordt opgegeven door het laatste cijfer van de toepassings-id. Daarom kan deze familie van toepassings-id's ook worden weergegeven als *310n*. Omdat de GS1-standaard aangeeft dat er altijd minimaal één getal links van het decimaalteken moet zijn, zijn er maximaal vijf decimalen toegestaan.

Hieronder vindt u enkele voorbeelden die laten zien hoe het getal *123456* wordt geïnterpreteerd door verschillende toepassings-id's (vet weergegeven):

- **`3100`**`123456` &rarr; 123456 (geheel getal)
- **`3101`**`123456` &rarr; 12345,6 (één decimaal)
- **`3102`**`123456` &rarr; 1234,56 (twee decimalen)
- **`3103`**`123456` &rarr; 123,456 (drie decimalen)
- **`3104`**`123456` &rarr; 12,3456 (vier decimalen)
- **`3105`**`123456` &rarr; 1,23456 (vijf decimalen)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>GS1-streepjescodes scannen in Supply Chain Management

Magazijnmedewerkers gebruiken een scanner die is ingebouwd in of verbonden met een mobiel apparaat om GS1-streepjescodes te scannen. De scanner verzendt vervolgens de gescande streepjescode naar de als een reeks toetsenbordgebeurtenissen mobiele app Warehouse Management. Deze bewerkingsmodus wordt ook wel een *keyboard-wedge* of *wedge* genoemd. De mobiele app verzendt vervolgens de ontvangen tekst ongewijzigd naar Supply Chain Management. Wanneer het systeem invoergegevens ontvangt, wordt eerst bepaald of de gegevens beginnen met een van de geconfigureerde voorvoegsels om aan te geven dat de gegevens daadwerkelijk een GS1-streepjescode zijn (raadpleeg het gedeelte [Algemene GS1-opties instellen](#set-gs1-options)). Als de gescande gegevens niet met een van deze voorvoegsels beginnen, gebruikt het systeem een GS1-parser om de gegevens te parseren en afzonderlijke gegevenselementen op te halen op basis van hun toepassings-id's. Nadat de gegevens zijn geparseerd, wordt het huidige invoerveld of worden meerdere velden gevuld met de gescande gegevens.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Configuratie van hardware en software van de streepjescodescanner

Om GS1-streepjescodes correct te kunnen herkennen en decoderen in Supply Chain Management, moet de hardwarescanner of ondersteunende software zijn geconfigureerd om de volgende acties uit te voeren:

- Een voorvoegsel toevoegen aan de gescande streepjescodes, zodat het systeem een GS1-streepjescode kan herkennen.
- Het niet-afdrukbare ASCII-groepsscheidingsteken (ASCII-code 29 of hexadecimale code 1D) converteren naar een afdrukbaar teken, zoals een tilde (~).

Hoewel u elk voorvoegsel aan de gescande streepjescode kunt toevoegen, is het een optie om een ISO/IOMI 15424-symbookid, ook wel *AIM-id genoemd*, toe te voegen. Deze uit drie tekens bestaande id begint met een `]` en bestaat vervolgens uit één teken waarmee de gebruikte symbologie wordt aangegeven en een cijfer dat wordt gebruikt als een verdere modificator. Met de AIM-id `]C1` wordt bijvoorbeeld een Code 128-streepjescode (vanwege het teken `C`) opgegeven en de modificator `1` geeft aan dat er een FNC1-teken op de eerste positie van de gegevens staat. Aa de andere kant is `]C0` een Code 128-streepjescode die elk ander teken heeft als het eerste teken van de gegevens.

De volgende vijf symbool-id's komen overeen met GS1-streepjescodes die toepassings-id-elementen bevatten:

- `]C1` – Code 128 (`C`) met FNC1-teken op de eerste positie (`1`), ook wel GS1-128 genoemd.
- `]e0` – GS1 DataBar.
- `]d2` – DataMatrix (`d`) met ECC 200 en FNC1 op de eerste positie (`2`), ook wel GS1 DataMatrix genoemd.
- `]Q3` – QR Code (`Q`) Model 2-symbool met FNC1 op de eerste positie (`3`), ook wel GS1 QR Code genoemd.
- `]J1` – GS1 DotCode.

Als u deze id's gebruikt, is voor compatibiliteit met niet-GS1-streepjescodes vereist dat de scanners of scansoftware zijn geconfigureerd om eventuele id's te verwijderen die niet overeenkomen met de GS1-id's. Als u bijvoorbeeld een 'normale' Code 39-streepjescode scant, wordt het voorvoegsel `]A0` toegevoegd. Omdat dit voorvoegsel niet door het systeem wordt geïnterpreteerd als een van de GS1-voorvoegsels, wordt het geïnterpreteerd als gegevens en levert het onverwachte resultaten op.

> [!NOTE]
> Voor het gemak worden vanaf versie 2.0.17.0 en latere versies van de mobiele app Warehouse Management alle AIM-voorvoegsels verwijderd die niet in de vorige lijst zijn opgenomen. Dit gedrag ondersteunt gevallen waarin u de scanner kunt configureren om het AIM-voorvoegsel toe te voegen, maar niet om ongewenste voorvoegsels te verwijderen.

### <a name="single-and-multiple-field-scanning"></a>Scannen van enkele en meerdere velden

Nadat de gegevens zijn geparseerd via de streepjescode, worden ze in de stroombesturingselementen van het mobiele apparaat ingevoerd. Er zijn twee methoden die op hun beurt worden verwerkt:

- **Eén veld scannen**: deze methode vult alleen het veld in waarop de streepjescode is gescand. Als u bijvoorbeeld de streepjescode `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` scant terwijl de cursor in het veld **Artikel** staat, wordt de GTIN `09521101530001` van de streepjescode in dat veld ingevoerd. Als u dezelfde streepjescode scant terwijl de cursor in het veld **Batch-id** staat, wordt het batchnummer `AB-123` uit de streepjescode ingevoerd. Deze modus werkt voor alle velden in alle stromen en vereist alleen dat de algemene GS1-instellingen zijn geconfigureerd. Als een streepjescode meerdere elementen bevat, moet deze nog steeds meerdere keren worden gescand, omdat er maar één deel van de streepjescode tegelijk in de stroom van het mobiele apparaat wordt ingevoerd. Dit gedrag wordt bepaald door de algemene GS1-instellingen, zoals wordt beschreven in de sectie [De algemene GS1-instellingen instellen](#generic-gs1-setup).
- **Meerdere velden scannen**: deze methode vult meerdere velden in wanneer één streepjescode wordt gescand, door extra gegevens in de staat van de stroom van het mobiele apparaat te pushen. Het beleid wordt bijvoorbeeld geconfigureerd om toepassings-id 01 in het `ItemId`-besturingselement te pushen en toepassings-id 10 in het veld `InventBatchId` te pushen. Als u in dat geval de streepjescode `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` scant, worden gegevens voor beide variabelen tegelijkertijd gepusht. U wordt daarom niet gevraagd om het artikel- en/of batchnummer in de stroom. Dit gedrag wordt bepaald door GS1-beleid dat is gekoppeld aan menu-items, zoals wordt beschreven in [GS1-beleid instellen voor menu-items van een mobiel apparaat](#policies-for-menus).

> [!WARNING]
> Het standaard GS1-beleid is getest om te werken zonder onverwacht gedrag. Aanpassingen van GS1-beleid die aan menu-items zijn gekoppeld, kunnen echter tot onverwacht gedrag leiden omdat de stroom mogelijk niet verwacht dat bepaalde gegevens op een bepaald moment beschikbaar zijn.

## <a name="turn-on-the-gs1-feature"></a>De GS1-functie inschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Warehouse Management*
- **Functienaam:** *GS1-streepjescodes scannen*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>De functie Verbeterde parser voor GS1-streepjescodes inschakelen

Als u GS1-streepjescodes gebruikt, is het raadzaam om ook de functie *Verbeterde parser voor GS1-streepjescodes* aan te zetten. Deze functie zorgt voor een verbeterde implementatie van de GS1-streepjescodeparser. De volgende verbeteringen worden toegevoegd:

- Het volgt het algoritme voor het parseren van symboolgegevens uit de algemene GS1-specificatie en valideert of de gegevens in het symbool geldig zijn volgens de specificatie.
- U hoeft geen waarde voor **Maximumlengte van id** in te stellen en de langste voorvoegsels uit geconfigureerde toepassings-id's worden gematcht.
- U kunt hiermee gemakkelijker decimale toepassings-id's configureren door de letter *n* te gebruiken voor elk nummer. U kunt bijvoorbeeld slechts één toepassings-id (*310n*) configureren in plaats van afzonderlijke toepassings-id's (*3101*, *3102*, *3103*, enzovoort).
- Hiermee wordt een probleem opgelost waarbij onjuist gecodeerde gegevens worden geïnterpreteerd als veldgegevens.
- Dit is een aparte klasse die opnieuw kan worden gebruikt in andere contexten en waarmee een uitbreidbaarheidspunt kan worden gebruikt voor het bewerken van gescande gegevens voordat de stroomvelden worden ingevuld.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Algemene GS1-opties instellen

Op de pagina **Parameters voor magazijnbeheer** vindt u enkele instellingen voor algemene GS1-opties.

Volg deze stappen om algemene GS1-opties in te stellen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het sneltabblad **Streepjescodes** de volgende velden in:

    - **FNC1-teken**, **Datamatrixteken** en **QR-codeteken**: geef tekens op die moeten worden geïnterpreteerd als voorvoegsel voor elk type GS1-streepjescode.
    - **Groepsscheidingsteken**: geef het teken op dat het ASCII-groepsscheidingsteken vervangt.
    - **Maximale lengte van id**: geef het maximumaantal tekens op dat voor de toepassings-id is toegestaan. Dit veld is niet vereist als de functie *Verbeterde GS1-parser* voor het systeem is ingeschakeld.

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

    - **Toepassings-id**: voer de identificatiecode voor de toepassings-id in. Normaal gesproken is deze code een geheel getal met twee cijfers, maar dit kan langer zijn. Voor decimale waarden geeft het laatste cijfer het aantal decimalen aan. Zie de omschrijving van het selectievakje **Decimaal** later in deze lijst voor meer informatie. Als de functie *Verbeterde parser voor GS1-streepjescodes* is ingeschakeld, kunt u één toepassings-id maken voor alle varianten van decimalen door de letter *n* als laatste teken in de toepassings-id te gebruiken. U kunt bijvoorbeeld slechts één toepassings-id (*310n*) configureren in plaats van een afzonderlijke toepassings-id's voor elk aantal decimalen (*3101*, *3102*, *3103*, enzovoort).
    - **Omschrijving**: voer een korte omschrijving van de id in.
    - **Vaste lengte**: schakel dit selectievakje in als waarden die met deze toepassings-id worden gescand een vast aantal tekens hebben. Schakel dit selectievakje in als de lengte van waarden variabel is. In dit geval moet u het einde van de waarde aangeven met behulp van het groepsscheidingsteken dat u hebt opgegeven op de pagina **Parameters van magazijnbeheer**.
    - **Lengte**: voer het maximumaantal tekens in dat kan worden weergegeven in de waarden die worden gescand met deze toepassings-id. Als het selectievakje **Vaste lengte** is ingeschakeld, wordt precies dit aantal tekens verwacht.
    - **Type**: selecteer het type waarde dat wordt gescand met deze toepassings-id (*Numeriek*, *Alfanumeriek* of *Datum*). Zie de sectie [Datums en decimale getallen](#dates-and-decimal-numbers) voor meer informatie over de manier waarop datums en getallen in streepjescodegegevens worden weergegeven.
    - **Decimaal**: schakel dit selectievakje in als de waarde een impliciet decimaalteken bevat. Als dit vakje is ingeschakeld, wordt het laatste cijfer van de toepassings-id gebruikt om het aantal decimale plaatsen te bepalen. Zie de sectie [Datums en decimale getallen](#dates-and-decimal-numbers) voor meer informatie over de manier waarop datums en getallen in streepjescodegegevens worden weergegeven.

> [!WARNING]
> Hoewel het systeem u toestaat om het selectievakje **Vaste lengte** in te schakelen voor een toepassings-id, mag het volgens de algemene GS1-specificaties alleen worden gebruikt voor de subset van toepassings-id's met een vooraf gedefinieerde lengte. De verbeterde GS1-parser bevat al een lijst met alle toepassings-id's met vooraf gedefinieerde lengtes.

> [!NOTE]
> De waarde van **Groepsscheidingsteken** die is opgegeven op de pagina **Parameters voor magazijnbeheer** is optioneel als een waarde die wordt gevolgd door een toepassings-id een vaste lengte heeft.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>De algemene GS1-instellingen instellen

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

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a>GS1-beleid instellen voor menuopdrachten voor mobiele apparaten

Het doel van de GS1-standaard is dat medewerkers verschillende waarden kunnen laden wanneer ze één streepjescode één keer scannen. Logistiek managers moeten hiervoor een GS1-beleid instellen om aan te geven hoe streepjescodes met meerdere waarden moeten worden geïnterpreteerd. Later kunt u beleid toewijzen aan menuopdrachten van mobiele apparaten om te bepalen hoe een streepjescode wordt geïnterpreteerd wanneer medewerkers deze scannen terwijl ze een bepaalde menuopdracht gebruiken.

Als er geen GS1-beleid is toegewezen aan een menu-item, kan slechts één waarde worden vastgelegd. Deze waarde wordt toegepast op de invoer voor de mobiele app die wordt geselecteerd wanneer de medewerker de scan maakt, zoals is opgegeven in de algemene GS1-instellingen. Als er een GS1-beleid is toegewezen aan het menuopdracht, gebruikt het systeem nog steeds de algemene GS1-instellingen om de eerste streepjescodewaarde aan het geselecteerde veld toe te wijzen. Vervolgens kunnen echter aanvullende veldwaarden worden vastgelegd, zoals opgegeven in het toepasselijke beleid.

### <a name="load-the-standard-specific-gs1-policies"></a>Het specifieke GS1-standaardbeleid laden

U kunt een set GS1-beleidsregels laden om snel aan de slag te gaan. U kunt de beleidsregels vervolgens later naar wens uitbreiden of bewerken.

Volg deze stappen om de standaardtoepassings-id's te laden.

1. Ga naar **Magazijnbeheer \> Instellingen \> GS1 \> GS1-beleid**.
1. Selecteer **Standaardinstelling maken** in het actievenster.

> [!WARNING]
> Met de opdracht **Standaardinstellingen maken** worden alle momenteel gedefinieerde beleidsregels verwijderd en door de standaardset met beleidsregels vervangen. Nadat u de standaardinstellingen hebt geladen, kunt u de beleidsregels echter naar wens aanpassen.

### <a name="set-up-custom-specific-gs1-policies"></a>Aangepast specifiek GS1-beleid instellen

> [!WARNING]
> Sommige GS1-beleidsregels werken mogelijk niet met elke mobiele stroom die u gebruikt. Wanneer u aangepast GS1-beleid configureert, moet u de stroom van mobiele apparaten testen door verschillende gegevens te gebruiken die op verschillende punten in de stroom worden gescand. Op deze manier kunt u bepalen of de stroom zich op de juiste wijze gedraagt.

Volg deze stappen om uw GS1-beleid in te stellen en aan te passen.

1. Ga naar **Magazijnbeheer \> Instellingen \> GS1 \> GS1-beleid**.
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
1. Selecteer het veld **Item** en scan de volgende streepjescode: `]C10100000012345678~3030~10b1~17220215`.

Vanwege de instellingen die voor dit voorbeeld zijn vastgelegd, wordt de gescande streepjescode op de volgende manier gescand.

| Veldsleutel | Sollicitatie-ID | Waarde | Notitie |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Omdat de medewerker naar het veld **Item** heeft gescand, wordt de eerste waarde in de streepjescode aan dat veld toegewezen. De toewijzing wordt overgenomen uit de algemene GS1-instellingen. |
| Hoeveelheid | 30 | 30 | Aangezien verschillende veldwaarden in één scan worden vastgelegd, worden deze toewijzing en alle resterende toewijzingen overgenomen uit het GS1-beleid dat is toegewezen aan de menuopdracht **Inkoop ontvangen**. Deze warde is de hoeveelheid die is ontvangen. |
| InventBatchId | 10 | b1 | Deze waarde is de batch-id. |
| ExpDate | 17 | 220215 | De datumnotatie is JJMMDD. De vervaldatum is daarom 15 februari 2022. |

De ontvangst wordt vervolgens geregistreerd en de relevante databasewaarden worden na de ene scan ingevoerd.
