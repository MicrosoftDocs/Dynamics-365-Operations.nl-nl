---
title: Configuratie van Voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven hoe u Voorraadzichtbaarheid configureert.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345028"
---
# <a name="inventory-visibility-configuration"></a>Configuratie van Voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In dit onderwerp wordt beschreven hoe u Voorraadzichtbaarheid configureert.

## <a name="introduction"></a><a name="introduction"></a>Inleiding

Voordat u met Voorraadzichtbaarheid begint te werken, moet u de volgende configuratie voltooien zoals beschreven in dit onderwerp:

- [Configuratie van de gegevensbron](#data-source-configuration)
- [Configuratie van de partitie](#partition-configuration)
- [Configuratie van de productindexhiërarchie](#index-configuration)
- [Configuratie van de reservering (optioneel)](#reservation-configuration)
- [Voorbeeld van een standaardconfiguratie](#default-configuration-sample)

> [!NOTE]
> U kunt configuraties voor Voorraadzichtbaarheid weergeven en bewerken in [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration). Nadat de configuratie is voltooid, selecteert u **Configuratie bijwerken** in de app.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Configuratie van de gegevensbron

De gegevensbron vertegenwoordigt het systeem waar uw gegevens vandaan komen. Voorbeelden zijn `fno` (wat Dynamics 365 Finance and Operations-apps betekent) en `pos` (wat verkooppunt betekent).

De configuratie van de gegevensbron omvat de volgende onderdelen:

- Dimensie (dimensietoewijzing)
- Fysieke meting
- Berekende meting

> [!NOTE]
> De `fno`-gegevensbron is gereserveerd voor Dynamics 365 Supply Chain Management.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensie (dimensietoewijzing)

Het doel van dimensieconfiguratie is het standaardiseren van de integratie met meerdere systemen voor boekingsgebeurtenissen en query's op basis van combinaties van dimensies.

Voorraadzichtbaarheid ondersteunt de volgende algemene basisdimensie.

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
| Voorraad (aangepast) | `InventDimension1` via `InventDimension12` |
| Toestel | `ExtendedDimension1` via `ExtendedDimension8` |

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

### <a name="physical-measures"></a>Fysieke metingen

Met fysieke metingen wordt de hoeveelheid aangepast en de voorraadstatus weergegeven. U kunt uw eigen fysieke metingen definiëren op basis van uw behoeften.

Voorraadweergave biedt een lijst met standaard fysieke metingen die zijn gekoppeld aan Supply Chain Management (de `fno`-gegevensbron). In de volgende tabel wordt een voorbeeld gegeven van fysieke metingen.

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

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Berekende metingen

Berekende metingen bieden een aangepaste berekeningsformule die uit een combinatie van fysieke metingen bestaat. Met deze functie kunt u een set fysieke metingen definiëren die wordt toegevoegd, en/of een set fysieke metingen definiëren die wordt afgetrokken om de aangepaste meting te vormen.

Stel dat u het volgende queryresultaat hebt.

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

De `MyCustomAvailableforReservation`-uitvoer, gebaseerd op de berekeningsinstelling in de aangepaste metingen, is 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Configuratie van de partitie

De partitieconfiguratie bestaat uit een combinatie van basisdimensies. Hiermee wordt het patroon van de gegevensdistributie gedefinieerd. Gegevensbewerkingen in dezelfde partitie ondersteunen hoge prestaties en kosten niet te veel. Goede partitiepatronen kunnen daarom aanzienlijke voordelen opleveren.

Voorraadweergave biedt de volgende standaardpartitieconfiguratie.

| Basisdimensie | Hiërarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> De standaardpartitieconfiguratie dient alleen ter informatie. U hoeft deze niet te definiëren in Voorraadzichtbaarheid. Op dit moment wordt de upgrade van de partitieconfiguratie niet ondersteund.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Configuratie van de productindexhiërarchie

Meestal staat de query voor voorhanden voorraad niet alleen op het hoogste niveau 'totaal'. In plaats daarvan wilt u mogelijk ook resultaten bekijken die worden samengevoegd op basis van de voorraaddimensies.

Voorraadzichtbaarheid biedt flexibiliteit door u de _indexen_ te laten instellen. Deze indexen zijn gebaseerd op een dimensie of een combinatie van dimensies. Een index bestaat uit een *setnummer*, een *dimensie* en een *hiërarchie*, zoals gedefinieerd in de volgende tabel.

| Naam | Beschrijving |
|---|---|
| Setnummer | Dimensies die tot dezelfde set (index) behoren, worden gegroepeerd en krijgen hetzelfde setnummer toegewezen. |
| Dimensie | Basisdimensies op basis daarvan wordt het queryresultaat is samengevoegd. |
| Hiërarchie | De hiërarchie wordt gebruikt om de ondersteunde dimensiecombinaties te definiëren waarop een query kan worden uitgevoerd. U stelt bijvoorbeeld een dimensieset in met een hiërarchievolgorde van `(ColorId, SizeId, StyleId)`. In dit geval ondersteunt het systeem query's op vier dimensiecombinaties. De eerste combinatie is leeg, de tweede is `(ColorId)`, de derde is `(ColorId, SizeId)` en de vierde is `(ColorId, SizeId, StyleId)`. De andere combinaties worden niet ondersteund. Zie het volgende voorbeeld voor meer informatie. |

### <a name="example"></a>Voorbeeld

In deze sectie vindt u een voorbeeld van de manier waarop de hiërarchie werkt.

U hebt de volgende artikelen in uw voorraad.

| Artikel | ColorId | SizeId | StyleId | Hoeveelheid |
|---|---|---|---|---|
| T-shirt | Zwart | Klein | Breed | 1 |
| T-shirt | Zwart | Klein | Normaal | 2 |
| T-shirt | Zwart | Groot | Breed | 3 |
| T-shirt | Zwart | Groot | Normaal | 4 |
| T-shirt | Rood | Klein | Breed | 5 |
| T-shirt | Rood | Klein | Normaal | 6 |
| T-shirt | Rood | Groot | Normaal | 7 |

Hier volgt de index.

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

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Configuratie van de reservering (optioneel)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

De reserveringsconfiguratie is vereist als u de functie voor zachte reservering wilt gebruiken. De configuratie bestaat uit twee fundamentele onderdelen:

- Zachte reserveringstoewijzing
- Zachte reserveringshiërarchie

### <a name="soft-reservation-mapping"></a>Zachte reserveringstoewijzing

Als u een reservering maakt, wilt u mogelijk weten of voorhanden voorraad momenteel beschikbaar is voor reservering. De validatie is gekoppeld aan een berekende meting die een berekeningsformule van een combinatie van fysieke metingen vertegenwoordigt.

Een reserveringsmeting is bijvoorbeeld gebaseerd op de fysieke meting `SoftReservOrdered` van de `iv`-gegevensbron (Voorraadzichtbaarheid). In dit geval kunt u de berekende meting `AvailableToReserve` van de `iv`-gegevensbron instellen, zoals hier wordt weergegeven.

| Berekeningstype | Gegevensbron | Fysieke meting |
|---|---|---|
| Optellen | `fno` | `AvailPhysical` |
| Optellen | `pos` | `Inbound` |
| Aftrekken | `pos` | `Outbound` |
| Aftrekken | `iv` | `SoftReservOrdered` |

Stel vervolgens een zachte reserveringstoewijzing in om een toewijzing te bieden van de reserveringsmeting `SoftReservOrdered` naar de berekende meting `AvailableToReserve`.

| Gegevensbron van fysieke meting | Fysieke meting | Beschikbaar voor reserveringsgegevensbron | Beschikbaar voor reservering van berekende meting |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

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

### <a name="soft-reservation-hierarchy"></a>Zachte reserveringshiërarchie

In de reserveringshiërarchie wordt de volgorde van dimensies beschreven die moeten worden opgegeven wanneer er reserveringen worden gemaakt. Dit werkt op dezelfde manier als de productindexhiërarchie voor voorhanden query's.

De reserveringshiërarchie is onafhankelijk van de productindexhiërarchie. Met deze onafhankelijkheid kunt u categoriebeheer implementeren, waarbij gebruikers de dimensies kunnen opsplitsen in details om de vereisten voor het maken van nauwkeurige reserveringen op te geven.

Hier volgt een voorbeeld van een zachte reserveringshiërarchie.

| Basisdimensie | Hiërarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

In dit voorbeeld kunt u reserveringen maken in de volgende dimensievolgordes:

- `()`: er is geen dimensie opgegeven.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Een geldige dimensievolgorde moet strikt de reserveringshiërarchie, dimensie per dimensie, volgen. De hiërarchievolgorde `(SiteId, LocationId, SizeId)` is bijvoorbeeld niet geldig omdat `ColorId` ontbreekt.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Voorbeeld van een standaardconfiguratie

Tijdens de initialisatiefase wordt door Voorraadweergave een standaardconfiguratie ingesteld. U kunt de configuratie desgewenst wijzigen.

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

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

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
