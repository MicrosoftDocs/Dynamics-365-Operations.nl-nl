---
title: Voorraadzichtbaarheid configureren
description: In dit onderwerp wordt beschreven hoe u Voorraadzichtbaarheid configureert.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: adab5ee3f626390355f4bab1227efd5fe58c2fcf
ms.sourcegitcommit: a3b121a8c8daa601021fee275d41a95325d12e7a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524516"
---
# <a name="configure-inventory-visibility"></a>Voorraadzichtbaarheid configureren

[!include [banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u de invoegtoepassing Voorraadzichtbaarheid gebruikt met de app Voorraadzichtbaarheid in Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Inleiding

Voordat u met Voorraadzichtbaarheid begint te werken, moet u de volgende configuratie voltooien zoals beschreven in dit onderwerp:

- [Configuratie van de gegevensbron](#data-source-configuration)
- [Configuratie van de partitie](#partition-configuration)
- [Configuratie van de productindexhiërarchie](#index-configuration)
- [Configuratie van de reservering (optioneel)](#reservation-configuration)
- [Voorbeeld van een standaardconfiguratie](#default-configuration-sample)

## <a name="prerequisites"></a>Vereisten

Installeer voordat u begint eerst de invoegtoepassing Voorraadzichtbaarheid en stel de app in zoals beschreven in [Voorraadzichtbaarheid installeren en instellen](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>De configuratiepagina van de app Voorraadzichtbaarheid

In Power Apps kunt u op de pagina **Configuratie** van de [app Voorraadzichtbaarheid](inventory-visibility-power-platform.md) de configuratie van voorhanden voorraad en zachte reservering instellen. Als de invoegtoepassing is geïnstalleerd, bevat de standaardconfiguratie de waarde van Microsoft Dynamics 365 Supply Chain Management (de `fno`-gegevensbron). U kunt de standaardinstellingen controleren. Daarnaast kunt u op basis van uw bedrijfsbehoeften en de voorraadboekingsvereisten van uw externe systeem de configuratie wijzigen om de manier te standaardiseren waarop voorraadwijzigingen kunnen worden geboekt, geordend en opgevraagd in de verschillende systemen. In de resterende secties van dit onderwerp wordt uitgelegd hoe u elk deel van de pagina **Configuratie** gebruikt.

Nadat de configuratie is voltooid, moet u **Configuratie bijwerken** selecteren in de app.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Functies voor Voorraadzichtbaarheid inschakelen in Power Apps-functiebeheer

Met de invoegingtoepassing Voorraadzichtbaarheid worden meerdere nieuwe functies aan uw Power Apps-installatie toegevoegd. Deze functies zijn standaard uitgeschakeld. Als u deze functies wilt gebruiken, opent u de pagina **Configuratie** en schakelt u ze vervolgens naar behoefte in op het tabblad **Functiebeheer**.

| Naam Functiebeheer | Description |
|---|---|
| OnHandReservation | Met deze functie kunt u reserveringen maken, reserveringen opnemen en/of de reservering van gespecificeerde voorraadhoeveelheden ongedaan maken met behulp van Voorraadzichtbaarheid. Zie [Voorraadzichtbaarheid reserveringen](inventory-visibility-reservations.md) voor meer informatie. |
| OnHandMostSpecificBackgroundService | De functie biedt een voorraadoverzicht voor producten samen met alle dimensies. De overzichtsgegevens van de voorraad worden periodiek gesynchroniseerd vanuit Voorraadzichtbaarheid. Zie [Voorraadoverzicht](inventory-visibility-power-platform.md#inventory-summary) voor meer informatie. |
| OnhandChangeSchedule | Met deze functie worden de functies voor planning van wijzigingen in voorhanden hoeveelheden en ATP (Available To Promise) ingeschakeld (optioneel). Zie [Planningen van wijzigingen in voorhanden hoeveelheid en available to promise in Voorraadzichtbaarheid](inventory-visibility-available-to-promise.md) voor meer informatie. |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Het service-eindpunt zoeken

Als u het juiste eindpunt van de service Voorraadzichtbaarheid niet weet, opent u de pagina **Configuratie** in Power Apps en selecteert u vervolgens **Service-eindpunt weergeven** in de rechterbovenhoek. Op deze pagina wordt het juiste service-eindpunt weergegeven.

## <a name="data-source-configuration"></a>Configuratie van de gegevensbron

Elke gegevensbron vertegenwoordigt een systeem waaruit uw gegevens afkomstig zijn. Voorbeelden van namen van gegevensbronnen zijn `fno` (wat voor apps voor Dynamics 365 Finance en bedrijfsactiviteiten staat) en `pos` (wat verkooppunt betekent). Standaard is Supply Chain Management ingesteld als een standaardgegevensbron (`fno`) in Voorraadzichtbaarheid.

> [!NOTE]
> De `fno`-gegevensbron is gereserveerd voor Supply Chain Management. Als de invoegtoepassing Voorraadzichtbaarheid is geïntegreerd met een Supply Chain Management-omgeving, raden we u aan om geen configuraties te verwijderen die betrekking hebben op `fno` in de gegevensbron.

Volg deze stappen om een gegevensbron toe te voegen.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Gegevensbron** de optie **Nieuwe gegevensbron** om een gegevensbron toe te voegen.

> [!NOTE]
> Wanneer u een gegevensbron toevoegt, moet u de naam, fysieke metingen en dimensietoewijzingen van uw gegevensbron valideren voordat u de configuratie voor de service voor Voorraadzichtbaarheid bijwerkt. U kunt deze instellingen niet meer wijzigen nadat u **Updateconfiguratie** hebt geselecteerd.

De configuratie van de gegevensbron omvat de volgende onderdelen:

- Dimensies (dimensietoewijzing)
- Fysieke metingen
- Berekende metingen

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensies (dimensietoewijzing)

Het doel van dimensieconfiguratie is het standaardiseren van de integratie met meerdere systemen voor boekingsgebeurtenissen en query's op basis van combinaties van dimensies. Voorraadzichtbaarheid biedt een lijst met basisdimensies die kunnen worden toegewezen vanuit de dimensies van uw gegevensbron. Er zijn 33 dimensies beschikbaar voor toewijzing.

- Als u Supply Chain Management als een van uw gegevensbronnen gebruikt, worden er standaard 13 dimensies aan de standaarddimensies van Supply Chain Management toegewezen. 12 andere dimensies (`inventDimension1` tot en met `inventDimension12`) worden aan aangepaste dimensies in Supply Chain Management toegewezen. De resterende acht dimensies zijn uitgebreide dimensies die u aan externe gegevensbronnen kunt toewijzen.
- Als u Supply Chain Management niet als een van uw gegevensbronnen gebruikt, kunt u de dimensies naar wens toewijzen. In de volgende tabel wordt de volledige lijst met beschikbare dimensies weergegeven.

> [!NOTE]
> Als uw dimensie niet in de standaarddimensielijst staat en u een externe gegevensbron gebruikt, raden we u aan `ExtendedDimension1` tot en met `ExtendedDimension8` voor de toewijzing te gebruiken.

| Dimensietype | Basisdimensie |
|---|---|
| Artikel | `ColorId` |
| Artikel | `SizeId` |
| Artikel | `StyleId` |
| Artikel | `ConfigId` |
| Tracering | `BatchId` |
| Tracering | `SerialId` |
| Locatie | `LocationId` |
| Locatie | `SiteId` |
| Voorraadstatus | `StatusId` |
| Magazijnspecifiek | `WMSLocationId` |
| Magazijnspecifiek | `WMSPalletId` |
| Magazijnspecifiek | `LicensePlateId` |
| Overig | `VersionId` |
| Voorraad (aangepast) | `InventDimension1` tot en met `InventDimension12` |
| Extensie | `ExtendedDimension1` tot en met `ExtendedDimension8` |
| System | `Empty` |

> [!NOTE]
> De dimensietypen die worden vermeld in de vorige tabel dienen alleen ter referentie. U hoeft deze niet te definiëren in Voorraadzichtbaarheid.
>
> Voorraaddimensies (aangepast) kunnen worden gereserveerd voor Supply Chain Management. In dat geval kunt u in plaats daarvan de uitgebreide dimensies gebruiken.

Externe systemen hebben toegang tot Voorraadzichtbaarheid via de RESTful-API's. Voor de integratie kunt u met Voorraadzichtbaarheid de _externe gegevensbron_ en de toewijzing van de _externe dimensies_ aan de _basisdimensies_ configureren. Hier volgt een voorbeeld van een tabel voor dimensietoewijzing.

| Externe dimensie | Basisdimensie |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Door een dimensietoewijzing te configureren, kunt u de externe dimensies rechtstreeks naar Voorraadzichtbaarheid verzenden. Voorraadzichtbaarheid converteert vervolgens automatisch externe dimensies naar basisdimensies.

Ga als volgt te werk om dimensietoewijzingen toe te voegen.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Gegevensbron** in de sectie **Dimensietoewijzingen** de optie **Toevoegen** om dimensietoewijzingen toe te voegen.
    ![Dimensietoewijzingen toevoegen](media/inventory-visibility-dimension-mapping.png "Dimensietoewijzingen toevoegen")

1. Geef in het veld **Dimensienaam** de brondimensie op.
1. Selecteer in het veld **Naar basisdimensie** de dimensie in Voorraadzichtbaarheid die u wilt toewijzen.
1. Selecteer **Opslaan**.

Als uw gegevensbron bijvoorbeeld een productkleurdimensie bevat, kunt u deze aan de basisdimensie `ColorId` toevoegen om een aangepaste dimensie `ProductColor` aan de gegevensbron `exterchannel` toe te voegen. Deze wordt vervolgens aan de basisdimensie `ColorId` toegevoegd.

### <a name="physical-measures"></a>Fysieke metingen

Wanneer vanuit een gegevensbron een voorraadwijziging naar Voorraadzichtbaarheid wordt geboekt, wordt die wijziging met behulp van *fysieke metingen* geboekt. Met fysieke metingen wordt de hoeveelheid aangepast en de voorraadstatus weergegeven. U kunt uw eigen fysieke metingen definiëren op basis van uw behoeften. Query's kunnen worden gebaseerd op de fysieke metingen.

Voorraadweergave biedt een lijst met standaard fysieke metingen die zijn gekoppeld aan Supply Chain Management (de `fno`-gegevensbron). Deze standaard fysieke metingen worden opgehaald uit de statussen van voorraadtransacties op de pagina **Voorhanden lijst** in Supply Chain Management (**Voorraadbeheer \> Vragen en rapport \> Voorhanden lijst**). In de volgende tabel wordt een voorbeeld gegeven van fysieke metingen.

| Naam van fysieke meting | Beschrijving |
|---|---|
| `NotSpecified` | Niet opgegeven |
| `Arrived` | Gearriveerd |
| `AvailOrdered` | Beschikbaar besteld |
| `AvailPhysical` | Fysiek beschikbaar |
| `Deducted` | Ingehouden |
| `OnOrder` | In bestelling |
| `Ordered` | Besteld |
| `PhysicalInvent` | Fysieke voorraad |
| `Picked` | Opgenomen |
| `PostedQty` | Boekingshoeveelheid |
| `QuotationIssue` | Uitgifte van offerte |
| `QuotationReceipt` | Offerte-ontvangst |
| `Received` | Ontvangen |
| `Registered` | Geregistreerd |
| `ReservOrdered` | Besteld en gereserveerd |
| `ReservPhysical` | Fysiek gereserveerd |

Als de gegevensbron Supply Chain Management is, hoeft u de standaard fysieke metingen niet opnieuw te maken. Voor externe gegevensbronnen kunt u echter nieuwe fysieke metingen maken door deze stappen uit te voeren.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Gegevensbron** in de sectie **Fysieke metingen** de optie **Toevoegen**, geef een naam voor de bronmeting op en sla de wijzigingen op.

### <a name="calculated-measures"></a>Berekende metingen

U kunt Voorraadzichtbaarheid gebruiken om een query uit te voeren op zowel fysieke metingen van de voorraad als op *aangepaste berekende metingen*. Berekende metingen bieden een aangepaste berekeningsformule die uit een combinatie van fysieke metingen bestaat. Met deze functie kunt u een set fysieke metingen definiëren die wordt toegevoegd, en/of een set fysieke metingen definiëren die wordt afgetrokken om de aangepaste meting te vormen.

Met de configuratie kunt u een set modificators definiëren die worden opgeteld of afgetrokken om het totale samengevoegde uitvoeraantal te krijgen.

Als u een aangepast berekende meting wilt instellen, gaat u als volgt te werk.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Berekende meting** de optie **Nieuwe berekende meting** om een berekende maat toe te voegen.
1. Stel de volgende velden in voor de nieuwe berekende meting:

    - **Naam van nieuwe berekende meting** : voer de naam van de berekende meting in.
    - **Gegevensbron**: selecteer de gegevensbron die aan de nieuwe modificator is gekoppeld. Het querysysteem is een gegevensbron.

1. Selecteer **Toevoegen** om een nieuwe modificator toe te voegen aan de nieuw berekende meting.
1. Stel de volgende velden in voor de nieuwe modificator:

    - **Modificator**: selecteer het modificatortype (*Optellen* of *Aftrekken*).
    - **Gegevensbron**: selecteer de gegevensbron waar de meting die de modificatorwaarde levert te vinden is.
    - **Meting**: selecteer de naam van de meting (vanuit de geselecteerde gegevensbron) die de waarde voor de modificator levert.

1. Herhaal stap 5 tot en met 6 totdat u alle vereiste modificatoren hebt toegevoegd.
1. Selecteer **Opslaan**.

U hebt bijvoorbeeld het volgende queryresultaat.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

U configureert vervolgens een berekende meting met de naam `MyCustomAvailableforReservation`, zoals in de volgende tabel wordt weergegeven. Deze berekende meting wordt verbruikt door het verbruikssysteem.

| Verbruikssysteem | Berekende meting | Gegevensbron | Fysieke meting | Berekeningstype |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Wanneer deze berekeningsformule wordt gebruikt, bevat het nieuwe queryresultaat de aangepaste meting.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

De `MyCustomAvailableforReservation`-uitvoer, gebaseerd op de berekeningsinstelling in de aangepaste metingen, is 100 + 50 - 10 + 80 - 20 + 90 + 30 - 60 - 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Configuratie van de partitie

De partitieconfiguratie bestaat momenteel uit twee basisdimensies (`SiteId` en `LocationId`) die aangeven hoe de gegevens worden gedistribueerd. Bewerkingen onder dezelfde partitie kunnen betere prestaties bieden tegen lagere kosten. In de volgende tabel wordt de standaardpartitieconfiguratie weergegeven die door de invoegtoepassing Voorraadzichtbaarheid wordt geboden.

| Basisdimensie | Hiërarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

De oplossing bevat standaard deze partitieconfiguratie. Daarom *hoeft u deze niet zelf te definiëren*.

> [!IMPORTANT]
> Pas de standaard partitieconfiguratie niet aan. Als u deze verwijdert of wijzigt, veroorzaakt u waarschijnlijk een onverwachte fout.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Configuratie van de productindexhiërarchie

Meestal staat de query voor voorhanden voorraad niet alleen op het hoogste niveau 'totaal'. In plaats daarvan wilt u mogelijk ook resultaten bekijken die worden samengevoegd op basis van de voorraaddimensies.

Voorraadzichtbaarheid biedt flexibiliteit door u de _indexen_ te laten instellen. Deze indexen zijn gebaseerd op een dimensie of een combinatie van dimensies. Een index bestaat uit een *setnummer*, een *dimensie* en een *hiërarchie*, zoals gedefinieerd in de volgende tabel.

| Naam | Beschrijving |
|---|---|
| Setnummer | Dimensies die tot dezelfde set (index) behoren, worden gegroepeerd en krijgen hetzelfde setnummer toegewezen. |
| Dimensie | Basisdimensies op basis daarvan wordt het queryresultaat is samengevoegd. |
| Hiërarchie | De hiërarchie wordt gebruikt om de ondersteunde dimensiecombinaties te definiëren waarop een query kan worden uitgevoerd. U stelt bijvoorbeeld een dimensieset in met een hiërarchievolgorde van `(ColorId, SizeId, StyleId)`. In dit geval ondersteunt het systeem query's op vier dimensiecombinaties. De eerste combinatie is leeg, de tweede is `(ColorId)`, de derde is `(ColorId, SizeId)` en de vierde is `(ColorId, SizeId, StyleId)`. De andere combinaties worden niet ondersteund. Zie het volgende voorbeeld voor meer informatie. |

Ga als volgt te werk om uw producthiërarchie-index in te stellen.

1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Selecteer op het tabblad **Producthiërarchie-index** in de sectie **Dimensietoewijzingen** de optie **Toevoegen** om dimensietoewijzingen toe te voegen.
1. Standaard wordt een lijst met indexen weergegeven. Als u een bestaande index wilt wijzigen, selecteert u **Bewerken** of **Toevoegen** in de sectie voor de relevante index. Als u een nieuwe indexset wilt maken, selecteert u **Nieuwe indexset**. Selecteer voor elke rij in elke indexset in het veld **Dimensie** een dimensie in de lijst met basisdimensies. Waarden voor de volgende velden worden automatisch gegenereerd:

    - **Setnummer**: dimensies die tot dezelfde groep (index) behoren, worden gegroepeerd en krijgen hetzelfde setnummer toegewezen.
    - **Hiërarchie**: de hiërarchie wordt gebruikt om de ondersteunde dimensiecombinaties te definiëren waarop een query kan worden uitgevoerd in een dimensiegroep (index). Als u bijvoorbeeld een dimensiegroep instelt met de hiërarchievolgorde *Stijl*, *Kleur* en *Maat*, ondersteunt het systeem het resultaat van drie querygroepen. De eerste groep is alleen stijl. De tweede groep is een combinatie van stijl en kleur. En de derde groep is een combinatie van stijl, kleur en maat. De andere combinaties worden niet ondersteund.

### <a name="example"></a>Voorbeeld

In deze sectie vindt u een voorbeeld van de manier waarop de hiërarchie werkt.

In de volgende tabel vindt u een lijst met beschikbare voorraad voor dit voorbeeld.

| Artikel | ColorId | SizeId | StyleId | Hoeveelheid |
|---|---|---|---|---|
| T-shirt | Zwart | Klein | Breed | 1 |
| T-shirt | Zwart | Klein | Normaal | 2 |
| T-shirt | Zwart | Groot | Breed | 3 |
| T-shirt | Zwart | Groot | Normaal | 4 |
| T-shirt | Rood | Klein | Breed | 5 |
| T-shirt | Rood | Klein | Normaal | 6 |
| T-shirt | Rood | Groot | Normaal | 7 |

De volgende tabel toont hoe de indexhiërarchie is ingesteld.

| Setnummer | Dimensie | Hiërarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Met de index kunt u op de volgende manieren query's uitvoeren op de voorhanden voorraad:

- `()`: gegroepeerd op alle

    - T-shirt, 28

- `(ColorId)`: gegroepeerd op `ColorId`

    - T-shirt, zwart, 10
    - T-shirt, rood, 18

- `(ColorId, SizeId)`: gegroepeerd op de combinatie van `ColorId` en `SizeId`

    - T-shirt, zwart, small, 3
    - T-shirt, zwart, large, 7
    - T-shirt, rood, small, 11
    - T-shirt, rood, large, 7

- `(ColorId, SizeId, StyleId)`: gegroepeerd op de combinatie van `ColorId`, `SizeId` en `StyleId`

    - T-shirt, zwart, small, wide, 1
    - T-shirt, zwart, small, regular, 2
    - T-shirt, zwart, large, wide, 3
    - T-shirt, zwart, large, regular, 4
    - T-shirt, rood, small, wide, 5
    - T-shirt, rood, small, regular, 6
    - T-shirt, rood, large, regular, 7

> [!NOTE]
> Basisdimensies die in de partitieconfiguratie zijn gedefinieerd, mogen niet worden gedefinieerd in indexconfiguraties.
> 
> Als u alleen een query hoeft uit te voeren op voorraad die wordt samengevoegd door alle dimensiecombinaties, kunt u één index instellen die de basisdimensie `Empty` bevat.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Configuratie van de reservering (optioneel)

De reserveringsconfiguratie is vereist als u de functie voor zachte reservering wilt gebruiken. De configuratie bestaat uit twee fundamentele onderdelen:

- Zachte reserveringstoewijzing
- Zachte reserveringshiërarchie

### <a name="soft-reservation-mapping"></a>Zachte reserveringstoewijzing

Als u een reservering maakt, wilt u mogelijk weten of voorhanden voorraad momenteel beschikbaar is voor reservering. De validatie is gekoppeld aan een berekende meting die een berekeningsformule van een combinatie van fysieke metingen vertegenwoordigt.

Door de toewijzing van de fysieke meting in te stellen op de berekende meting, schakelt u de service Voorraadzichtbaarheid in om automatisch de beschikbaarheid van reserveringen te valideren op basis van de fysieke meting.

Voordat u deze toewijzing instelt, moeten de fysieke metingen, berekende metingen en de bijbehorende gegevensbronnen worden gedefinieerd op de tabbladen **Gegevensbron** en **Berekende meting** van de pagina **Configuratie** in Power Apps (zoals eerder in dit onderwerp is beschreven).

Volg deze stappen om een zachte reserveringstoewijzing te definiëren.

1. Definieer de fysieke meting die als de zachte reserveringsmeting fungeert (bijvoorbeeld `SoftReservOrdered`).
1. Definieer op het tabblad **Berekende meting** van de pagina **Configuratie** de berekende meting *beschikbaar voor reservering* (AFR) die de AFR-berekeningsformule bevat die u aan de fysieke meting wilt toewijzen. U kunt bijvoorbeeld `AvailableToReserve` instellen (beschikbaar voor reservering) zodat deze wordt toegewezen aan de eerder gedefinieerde fysieke meting `SoftReservOrdered`. Op deze manier kunt u zoeken welke hoeveelheden met de voorraadstatus `SoftReservOrdered` er beschikbaar zijn voor reservering. In de volgende tabel wordt de AFR-berekeningsformule weergegeven.

    | Berekeningstype | Gegevensbron | Fysieke meting |
    |---|---|---|
    | Optellen | `fno` | `AvailPhysical` |
    | Optellen | `pos` | `Inbound` |
    | Aftrekken | `pos` | `Outbound` |
    | Aftrekken | `iv` | `SoftReservOrdered` |

    U wordt aangeraden de berekende meting zo in te stellen dat deze de fysieke meting bevat waarop de reserveringsmeting is gebaseerd. Op deze manier wordt de berekende metingshoeveelheid beïnvloed door de hoeveelheid van de reserveringsmeting. Daarom moet de berekende meting `AvailableToReserve` van de gegevensbron `iv` in dit voorbeeld de fysieke meting `SoftReservOrdered` van `iv` bevatten als onderdeel.

1. Open de pagina **Configuratie**.
1. Stel op het tabblad **Zachte reserveringstoewijzing** de toewijzing van de fysieke meting naar de berekende meting in. In het vorige voorbeeld kunt u de volgende instellingen gebruiken om `AvailableToReserve` op de eerder gedefinieerde fysieke meting `SoftReservOrdered` toe te wijzen.

    | Gegevensbron van fysieke meting | Fysieke meting | Beschikbaar voor reserveringsgegevensbron | Beschikbaar voor reservering van berekende meting |
    |---|---|---|---|
    | `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Als u het tabblad **Zachte reserveringstoewijzing** niet kunt bewerken, moet u mogelijk de functie *OnHandReservation* op het tabblad **Functiebeheer** inschakelen.

Als u nu reserveert op `SoftReservOrdered`, vindt Voorraadzichtbaarheid automatisch `AvailableToReserve` en de bijbehorende berekeningsformule om de validatie van de reservering uit te voeren.

U hebt bijvoorbeeld de volgende voorhanden voorraad in Voorraadzichtbaarheid.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

In dit geval is de berekening van toepassing:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Als u dus probeert reserveringen te maken op basis van `iv.SoftReservOrdered` en de hoeveelheid is minder dan of gelijk aan `AvailableToReserve` (10), kunt u de reservering maken.

> [!NOTE]
> Wanneer u de reserverings-API aanroept, kunt u de reserveringsvalidatie beheren door de booleaanse parameter `ifCheckAvailForReserv` op te geven in de aanvraagbody. De waarde `True` betekent dat de validatie is vereist, terwijl de waarde `False` betekent dat de validatie niet is vereist. De standaardwaarde is `True`.

### <a name="soft-reservation-hierarchy"></a>Zachte reserveringshiërarchie

In de reserveringshiërarchie wordt de volgorde van dimensies beschreven die moeten worden opgegeven wanneer er reserveringen worden gemaakt. Dit werkt op dezelfde manier als de productindexhiërarchie voor voorhanden query's.

De reserveringshiërarchie is onafhankelijk van de productindexhiërarchie. Met deze onafhankelijkheid kunt u categoriebeheer implementeren, waarbij gebruikers de dimensies kunnen opsplitsen in details om de vereisten voor het maken van nauwkeurige reserveringen op te geven. Uw zachte reserveringshiërarchie moet `SiteId` en `LocationId` als onderdelen bevatten, omdat ze de partitieconfiguratie vormen. Wanneer u de reservering maakt, moet u een partitie voor het product opgeven.

Hier volgt een voorbeeld van een zachte reserveringshiërarchie.

| Basisdimensie | Hiërarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

In dit voorbeeld kunt u reserveringen maken in de volgende dimensiereeksen. U moet een partitie voor het product opgeven wanneer u een reservering maakt. Daarom is `(SiteId, LocationId)` de basishiërarchie die u kunt gebruiken.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Een geldige dimensievolgorde moet strikt de reserveringshiërarchie, dimensie per dimensie, volgen. De hiërarchievolgorde `(SiteId, LocationId, SizeId)` is bijvoorbeeld niet geldig omdat `ColorId` ontbreekt.

## <a name="available-to-promise-configuration-optional"></a>Configuratie voor available to promise (optioneel)

U kunt Voorraadzichtbaarheid zo instellen dat u toekomstige wijzigingen in de voorhanden voorraad kunt plannen en ATP-hoeveelheden (Available-To-Promise) kunt berekenen. ATP is de hoeveelheid van een artikel, die beschikbaar is en die aan een klant kan worden beloofd in de volgende periode. Het gebruik van deze berekening kan uw capaciteit voor het afhandelen van orders veel groter maken. Als u deze functie wilt gebruiken, moet u deze inschakelen op het tabblad **Functiebeheer** en deze vervolgens instellen op het tabblad **ATP-instelling**. Zie [Planningen van wijzigingen in voorhanden hoeveelheid en available to promise in Voorraadzichtbaarheid](inventory-visibility-available-to-promise.md) voor meer informatie.

## <a name="complete-and-update-the-configuration"></a>De configuratie voltooien en bijwerken

Nadat u de configuratie hebt voltooid, moet u alle wijzigingen in Voorraadzichtbaarheid door te voeren. Selecteer **Configuratie bijwerken** in de rechterbovenhoek op de pagina **Configuratie** in Power Apps om de wijzigingen door te voeren.

De eerste keer dat u **Configuratie bijwerken** selecteert, vraagt het systeem om uw referenties.

- **Client-id**: de Azure-toepassings-id die u hebt gemaakt voor Voorraadzichtbaarheid.
- **Tenant-id**: uw Azure-tenant-id.
- **Clientgeheim**: het geheim van de Azure-toepassing die u hebt gemaakt voor Voorraadzichtbaarheid.

Nadat u zich hebt aangemeld, wordt de configuratie in de service Voorraadzichtbaarheid bijgewerkt.

> [!NOTE]
> Valideer de naam van uw gegevensbron, de fysieke metingen en de dimensietoewijzingen voordat u de configuratie voor de service voor Voorraadzichtbaarheid bijwerkt. U kunt deze instellingen niet meer wijzigen nadat u **Updateconfiguratie** hebt geselecteerd.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Voorbeeld van een standaardconfiguratie

Tijdens de initialisatiefase wordt door Voorraadzichtbaarheid een standaardconfiguratie ingesteld die hier uitgebreid aan de orde komt. U kunt deze configuratie desgewenst wijzigen.

### <a name="data-source-configuration"></a>Configuratie van de gegevensbron

#### <a name="configuration-of-the-iv-data-source"></a>Configuratie van de iv-gegevensbron

In deze sectie wordt beschreven hoe de `iv`-gegevensbron wordt geconfigureerd.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Fysieke metingen die zijn geconfigureerd voor de iv-gegevensbron

De volgende fysieke metingen worden geconfigureerd voor de `iv`-gegevensbron:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>Berekende meting OrderedTotal

De berekende meting `OrderedTotal` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `Ordered` |
| Optellen | `fno` | `Arrived` |
| Optellen | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Voorhanden berekende meting

De berekende meting `OnHand` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `PhysicalInvent` |
| Optellen | `iom` | `OnHand` |
| Optellen | `erp` | `Unrestricted` |
| Optellen | `erp` | `QualityInspection` |
| Optellen | `pos` | `PosInbound` |
| Aftrekken | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>Berekende meting ReservedTotal

De berekende meting `ReservedTotal` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `ReservPhysical` |
| Optellen | `fno` | `ReservOrdered` |
| Optellen | `iv` | `SoftReservPhysical` |
| Optellen | `iv` | `SoftReservOrdered` |
| Optellen | `iv` | `ReservPhysical` |
| Optellen | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>Berekende meting SoftReserved

De berekende meting `SoftReserved` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `iv` | `SoftReservPhysical` |
| Optellen | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>Berekende meting HardReserved

De berekende meting `HardReserved` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `ReservPhysical` |
| Optellen | `fno` | `ReservOrdered` |
| Optellen | `iv` | `ReservPhysical` |
| Optellen | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>Berekende meting OpenOrder

De berekende meting `OpenOrder` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `OnOrder` |
| Optellen | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>Berekende meting OnHandAvailable

De berekende meting `OnHandAvailable` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `PhysicalInvent` |
| Optellen | `iom` | `OnHand` |
| Optellen | `erp` | `Unrestricted` |
| Optellen | `erp` | `QualityInspection` |
| Optellen | `pos` | `PosInbound` |
| Aftrekken | `fno` | `ReservPhysical` |
| Aftrekken | `iv` | `SoftReservPhysical` |
| Aftrekken | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>Berekende meting AvailableToReserve

De berekende meting `AvailableToReserve` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `PhysicalInvent` |
| Optellen | `iom` | `OnHand` |
| Optellen | `erp` | `Unrestricted` |
| Optellen | `erp` | `QualityInspection` |
| Optellen | `pos` | `PosInbound` |
| Optellen | `fno` | `Ordered` |
| Optellen | `fno` | `Arrived` |
| Optellen | `iv` | `Ordered` |
| Aftrekken | `fno` | `ReservPhysical` |
| Aftrekken | `fno` | `ReservOrdered` |
| Aftrekken | `iv` | `SoftReservPhysical` |
| Aftrekken | `iv` | `SoftReservOrdered` |
| Aftrekken | `iv` | `ReservPhysical` |
| Aftrekken | `iv` | `ReservOrdered` |
| Aftrekken | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>Berekende meting InventorySupply

De berekende meting `InventorySupply` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `Ordered` |
| Optellen | `fno` | `Arrived` |
| Optellen | `iv` | `Ordered` |
| Optellen | `fno` | `PhysicalInvent` |
| Optellen | `iom` | `OnHand` |
| Optellen | `erp` | `Unrestricted` |
| Optellen | `erp` | `QualityInspection` |
| Optellen | `pos` | `PosInbound` |
| Aftrekken | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>Berekende meting InventoryDemand

De berekende meting `InventoryDemand` wordt geconfigureerd voor de `iv`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `OnOrder` |
| Optellen | `iom` | `OnOrder` |
| Optellen | `iv` | `SoftReservPhysical` |
| Optellen | `iv` | `SoftReservOrdered` |
| Optellen | `fno` | `ReservPhysical` |
| Optellen | `fno` | `ReservOrdered` |
| Optellen | `iv` | `ReservPhysical` |
| Optellen | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Configuratie van de fno-gegevensbron

In deze sectie wordt beschreven hoe de `fno`-gegevensbron wordt geconfigureerd.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Dimensietoewijzingen voor de fno-gegevensbron

De dimensietoewijzingen die in de volgende tabel worden weergegeven, worden geconfigureerd voor de `fno`-gegevensbron.

| Externe dimensie | Basisdimensie |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fysieke metingen die zijn geconfigureerd voor de fno-gegevensbron

De volgende fysieke metingen worden geconfigureerd voor de `fno`-gegevensbron:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Configuratie van de pos-gegevensbron

In deze sectie wordt beschreven hoe de gegevensbron `pos` wordt geconfigureerd.

##### <a name="physical-measures-for-the-pos-data-source"></a>Fysieke metingen voor de pos-gegevensbron

De volgende fysieke metingen worden geconfigureerd voor de `pos`-gegevensbron:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Berekende meting AvailQuantity

De berekende meting `AvailQuantity` wordt geconfigureerd voor de `pos`-gegevensbron, zoals in de volgende tabel wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `AvailPhysical` |
| Optellen | `pos` | `PosInbound` |
| Aftrekken | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Configuratie van de iom-gegevensbron

De volgende fysieke metingen worden geconfigureerd voor de `iom`-gegevensbron (intelligent order management):

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Configuratie van de erp-gegevensbron

De volgende fysieke metingen worden geconfigureerd voor de `erp`-gegevensbron (enterprise resource planning):

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Configuratie van de partitie

In de volgende tabel wordt de standaardpartitieconfiguratie weergegeven.

| Basisdimensie | Hiërarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Indexconfiguratie

In de volgende tabel wordt de standaardindexconfiguratie weergegeven.

| Setnummer | Dimensie | Hiërarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Reserveringsconfiguratie

In deze sectie wordt de standaardreserveringsconfiguratie beschreven.

#### <a name="reservation-mapping"></a>Reserveringstoewijzing

In de volgende tabel wordt de standaardreserveringsconfiguratie weergegeven.

| Gegevensbron van fysieke meting | Fysieke meting | Beschikbaar voor reserveringsgegevensbron | Beschikbaar voor reservering van berekende meting |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reserveringshiërarchie

In de volgende tabel wordt de standaardreserveringshiërarchie weergegeven.

| Basisdimensie | Hiërarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
