---
title: Planningen van wijzigingen in voorhanden hoeveelheid en available to promise in Voorraadzichtbaarheid
description: In dit artikel wordt beschreven hoe u toekomstige wijzigingen in de voorhanden hoeveelheid kunt plannen en ATP-hoeveelheden (Available-To-Promise) kunt berekenen.
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: f831c5d5719bbbd72c7cff37b8b35826f48ce6e4
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719286"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Planningen van wijzigingen in voorhanden hoeveelheid en available to promise in Voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u de functie *Planning van wijzigingen in voorhanden hoeveelheid* instelt om toekomstige wijzigingen in de voorhanden hoeveelheid te plannen en ATP-hoeveelheden (available-to-promise) te berekenen. ATP is de hoeveelheid van een artikel, die beschikbaar is en die aan een klant kan worden beloofd in de volgende periode. Het gebruik van deze berekening kan uw capaciteit voor het afhandelen van orders veel groter maken.

Voor veel fabrikanten, detailhandelaars of verkopers is het niet voldoende om alleen te weten wat er op dat moment voorhanden is. Zij moeten volledig zicht hebben op de toekomstige beschikbaarheid. Bij deze toekomstige beschikbaarheid moet rekening worden houden met toekomstig aanbod, toekomstige vraag en ATP.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>De functies inschakelen en instellen

Voordat u de ATP-hoeveelheid kunt gebruiken, moet u een of meer berekende metingen instellen om de ATP-hoeveelheden te kunnen berekenen. U moet de functie ook schakelen en ATP-instellingen configureren in Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Berekende metingen instellen voor ATP-hoeveelheden

De *berekende meting ATP* is een vooraf gedefinieerde berekende meting die gewoonlijk wordt gebruikt om te zoeken naar de voorhanden hoeveelheid die momenteel beschikbaar is. De *aanbodhoeveelheid* is de som van hoeveelheden voor die fysieke metingen die een modificatortype van *optelling* hebben, en de *vraaghoeveelheid* is de som van hoeveelheden voor die fysieke metingen die een modificatortype van *aftrekking* hebben.

U kunt meerdere berekende metingen toevoegen om meerdere ATP-hoeveelheden te berekenen. Het totale aantal verschillende fysieke metingen voor alle berekende ATP-metingen moet echter minder zijn dan negen.

> [!IMPORTANT]
> Een berekende meting is een samenstelling van fysieke metingen. De bijbehorende formule kan alleen fysieke metingen zonder dubbele waarden en niet berekende metingen bevatten.

U kunt bijvoorbeeld de volgende berekende meting instellen:

**Voorhanden beschikbaar** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

De som (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) vertegenwoordigt het aanbod en de som (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) vetegenwoordigt de vraag. Daarom kan de berekende meting als volgt worden gelezen:

**Voorhanden beschikbaar** = *Aanbod* – *Vraag*

U kunt nog een berekende meting toevoegen om de **fysieke voorhanden** ATP-hoeveelheid te berekenen.

**Voorhanden beschikbaar** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

Er zijn acht verschillende fysieke metingen in deze twee berekende ATP-metingen: *PhysicalInvent*, *OnHand*, *Unrestricted*, *QualityInspection*, *Inbound*, *ReservPhysical*, *SoftReservePhysical* en *Outbound*.

Zie [Berekende metingen](inventory-visibility-configuration.md#calculated-measures). voor meer informatie over berekende metingen.

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>De functie Planning van wijzigingen in voorhanden voorraad inschakelen en ATP-instellingen configureren

Volg deze stappen om de functie *Planning van wijzigingen in voorhanden voorraad* in te schakelen in Power Apps en de ATP-instellingen te configureren.

1. Meld u aan bij Power Apps en open Voorraadzichtbaarheid.
1. Open de pagina **Configuratie**.
1. Schakel op het tabblad **Functiebeheer** de functie *OnhandChangeSchedule* in.
1. Selecteer het tabblad **ATP-instelling**.
1. Wanneer u een query uitvoert op Voorraadzichtbaarheid, biedt dit een resultaat, inclusief elke berekende meting voor ATP die u hier toevoegt. Selecteer **Toevoegen** om een nieuwe berekende meting voor ATP toe te voegen.
1. Stel de volgende velden in:

    - **Gegevensbron**: selecteer de gegevensbron die aan de berekende meting is gekoppeld.
    - **Berekende meting**: selecteer de berekende meting die aan de geselecteerde gegevensbron is gekoppeld en die u wilt gebruiken om de momenteel beschikbare voorhanden hoeveelheid te zoeken.
    - **Planningsperiode**: voer het aantal dagen in dat gebruikers wijzigingen in de voorhanden hoeveelheid kunnen weergeven en indienen wanneer de geselecteerde berekende meting wordt gebruikt. Gebruikers die zoeken naar voorraadgegevens, krijgen de voorhanden hoeveelheid, de geplande wijzigingen in de voorhanden hoeveelheid en de ATP voor elke dag in deze periode, te beginnen met de huidige datum. Selecteer een geheel getal tussen 1 en 7.

    > [!IMPORTANT]
    > De planningsperiode omvat de huidige datum. Daarom kunnen gebruikers op elk moment wijzigingen in de voorhanden hoeveelheid plannen die plaatsvinden vanaf de huidige datum (de dag waarop de wijziging wordt ingediend) tot en met (planningsperiode – 1) dagen in de toekomst.

1. Selecteer **Opslaan**.
1. Herhaal stap 5 tot en met 7 totdat u alle berekende metingen hebt toegevoegd die u nodig hebt voor ATP.
1. Wanneer u alle vereiste instellingen hebt geconfigureerd, selecteert u **Configuratie bijwerken**.

Zie [De configuratie voltooien en bijwerken](inventory-visibility-configuration.md) voor meer informatie.

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>De manier waarop de planning van wijzigingen in de voorhanden hoeveelheid en ATP-berekeningen werken

Een *wijzigingsplanning voor voorhanden hoeveelheid* stelt verwachte datums en hoeveelheden van geplande wijzigingen in de voorhanden hoeveelheid vast. U kunt een wijzigingsplanning voor de voorhanden voorraad indienen bij Voorraadzichtbare gegevens, mits de datums binnen de periode liggen die is gedefinieerd door de instelling **Planningsperiode** (zie de sectie [De functies inschakelen en instellen](#setup)). Gebruikers die zoeken naar voorraadgegevens, krijgen de voorhanden hoeveelheid, de geplande wijzigingen in de voorhanden hoeveelheid en de ATP voor elke dag in die periode.

Geplande wijzigingen zijn in eerste instantie niet doorgevoerd en hebben daarom geen invloed op de werkelijke voorhanden hoeveelheden in het systeem. Als u de wijzigingen wilt doorvoeren, moet u een *wijzigingsgebeurtenis voor voorhanden hoeveelheid* indienen, waarmee de werkelijke beschikbare voorhanden hoeveelheid wordt bijgewerkt. U moet vervolgens de geplande wijziging terugdraaien door een planning van een wijziging in de voorhanden hoeveelheid in te dienen voor een overeenkomstige negatieve hoeveelheid.

U plaatst bijvoorbeeld een order voor 10 uur en verwacht dat deze morgen arriveert. Daarom dient u een planning voor wijziging van de voorhanden hoeveelheid in die een inkomende hoeveelheid van 10 heeft en morgen als leverdatum heeft. Wanneer de order de volgende dag binnenkomt, voegt u de fietsen toe aan uw fysieke voorhanden voorraad. U moet vervolgens de wijziging doorvoeren uw systeem om de werkelijke voorhanden hoeveelheid bij te werken. Als u de wijziging wilt doorvoeren, dient u een wijzigingsgebeurtenis voor voorhanden hoeveelheid in met een inkomende hoeveelheid van 10. U draait vervolgens de geplande wijziging terug door een planning van een wijziging in de voorhanden hoeveelheid in te dienen met een inkomende hoeveelheid van -10.

Wanneer u een query uitvoert op Voorraadzichtbaarheid voor voorhanden en ATP-hoeveelheden, worden de volgende gegevens voor elke dag in de planningsperiode geretourneerd:

- **Datum**: de datum waarop het resultaat van toepassing is. De tijdzone is UTC (Coordinated Universal Time).
- **Voorhanden hoeveelheid**: de werkelijke voorhanden hoeveelheid voor de opgegeven datum. Deze berekening wordt gemaakt volgens de door de ATP berekende meting die is geconfigureerd voor Voorraadzichtbaarheid.
- **Gepland aanbod**: de som van alle geplande inkomende hoeveelheden die nog niet fysiek beschikbaar zijn voor direct verbruik of zending vanaf de opgegeven datum.
- **Geplande vraag**: de som van alle geplande uitgaande hoeveelheden die niet zijn verbruikt of verzonden vanaf de opgegeven datum.
- **ATP-hoeveelheid**: de minimale verwachte voorhanden hoeveelheid die beschikbaar is vanaf de opgegeven datum tot en met het einde van de planningsperiode. Deze hoeveelheid bevat alle geplande hoeveelheidscorrecties. Dit is de maximumhoeveelheid die op de huidige leverings- of verbruiksdatum op die dag kan worden beloofd.

Als de huidige datum bijvoorbeeld 1 februari 2022 en de planningsperiode 7 is, kunnen gebruikers geplande wijzigingen in de voorhanden hoeveelheid indienen die naar verwachting zullen plaatsvinden van 1 februari tot en met 7 februari 2022. In dit geval wordt bijvoorbeeld de ATP-hoeveelheid voor 3 februari berekend op basis van de voorhanden hoeveelheid voor die dag en de geplande hoeveelheden van 3 februari tot en met 7 februari.

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld ziet u hoe een reeks geplande wijzigingen in de voorhanden hoeveelheid invloed heeft op de voorhanden en ATP-hoeveelheden waarvan Voorraadzichtbaarheid melding maakt. Het laat ook zien hoe u een geplande wijziging vastlegt, hoe een doorgevoerde wijziging in de planning de resultaten beïnvloedt en wat er kan gebeuren als u een geplande wijziging niet doorvoert.

De resultaten in dit voorbeeld geven een waarde voor *geprojecteerde voorhanden hoeveelheid*. Deze waarde omvat alle geplande updates voor illustratiedoeleinden, maar wordt niet daadwerkelijk gerapporteerd wanneer u een query uitvoert op Voorraadzichtbaarheid.

1. De volgende instellingen zijn geconfigureerd voor uw systeem op de pagina **ATP-instelling** in Power Apps:

    - **Berekende meting voor ATP**: u hebt een berekende meting met de naam *Voorhanden*. Deze wordt berekend als *Voorhanden hoeveelheid = Aanbod – Vraag*. U selecteert die meting hier.
    - **Planningsperiode**: u selecteert *7*.

1. De volgende voorwaarden zijn eveneens van toepassing:

    - De huidige datum is 1 februari 2022.
    - De huidige voorhanden hoeveelheid is 20.

1. Voor de huidige datum (1 februari 2022) dient u een geplande vraaghoeveelheid van 3 in bij Voorraadzichtbaarheid. Daarom is de geprojecteerde voorhanden hoeveelheid 17. De volgende tabel geeft het resultaat weer.

    | Datum | Voorhanden | Gepland aanbod | Geplande vraag | Geprojecteerde voorhanden hoeveelheid | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 01-02-2022 | 20 | | 3 | 17 | 17 |
    | 02-02-2022 | 20 | | | 17 | 17 |
    | 03-02-2022 | 20 | | | 17 | 17 |
    | 04-02-2022 | 20 | | | 17 | 17 |
    | 05-02-2022 | 20 | | | 17 | 17 |
    | 06-02-2022 | 20 | | | 17 | 17 |
    | 07-02-2022 | 20 | | | 17 | 17 |

1. Op de huidige datum (1 februari 2022) dient u een geplande aanbodhoeveelheid van 10 in voor 3 februari 2022. De volgende tabel geeft het resultaat weer.

    | Datum | Voorhanden | Gepland aanbod | Geplande vraag | Geprojecteerde voorhanden hoeveelheid | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 01-02-2022 | 20 | | 3 | 17 | 17 |
    | 02-02-2022 | 20 | | | 17 | 17 |
    | 03-02-2022 | 20 | 10 | | 27 | 27 |
    | 04-02-2022 | 20 | | | 27 | 27 |
    | 05-02-2022 | 20 | | | 27 | 27 |
    | 06-02-2022 | 20 | | | 27 | 27 |
    | 07-02-2022 | 20 | | | 27 | 27 |

1. Op de huidige datum (1 februari 2022) dient u de volgende geplande hoeveelheidswijzigingen in:

    - Vraaghoeveelheid van 15 voor 4 februari 2022
    - Aanbodhoeveelheid van 1 voor 5 februari 2022
    - Aanbodhoeveelheid van 3 voor 6 februari 2022

    De volgende tabel geeft het resultaat weer.

    | Datum | Voorhanden | Gepland aanbod | Geplande vraag | Geprojecteerde voorhanden hoeveelheid | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 01-02-2022 | 20 | | 3 | 17 | 12 |
    | 02-02-2022 | 20 | | | 17 | 12 |
    | 03-02-2022 | 20 | 10 | | 27 | 12 |
    | 04-02-2022 | 20 | | 15 | 12 | 12 |
    | 05-02-2022 | 20 | 1 | | 13 | 13 |
    | 06-02-2022 | 20 | 3 | | 16 | 16 |
    | 07-02-2022 | 20 | | | 16 | 16 |

1. Op de huidige datum (1 februari 2022) verzendt u de geplande vraaghoeveelheid van 3. Daarom moet u deze wijziging doorvoeren, zodat deze wordt weerspiegeld in uw werkelijke voorhanden hoeveelheid. U kunt de wijziging wilt doorvoeren door een wijzigingsgebeurtenis voor voorhanden hoeveelheid in te dienen met een uitkomende hoeveelheid van 3. U draait vervolgens de geplande wijziging terug door een planning van een wijziging in de voorhanden hoeveelheid in te dienen met een uitgaande hoeveelheid van -3. De volgende tabel geeft het resultaat weer.

    | Datum | Voorhanden | Gepland aanbod | Geplande vraag | Geprojecteerde voorhanden hoeveelheid | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 01-02-2022 | 17 | | 0 | 17 | 12 |
    | 02-02-2022 | 17 | | | 17 | 12 |
    | 03-02-2022 | 17 | 10 | | 27 | 12 |
    | 04-02-2022 | 17 | | 15 | 12 | 12 |
    | 05-02-2022 | 17 | 1 | | 13 | 13 |
    | 06-02-2022 | 17 | 3 | | 16 | 16 |
    | 07-02-2022 | 17 | | | 16 | 16 |

1. De volgende dag (2 februari 2022) schuift de planningsperiode één dag vooruit. De volgende tabel geeft het resultaat weer.

    | Datum | Voorhanden | Gepland aanbod | Geplande vraag | Geprojecteerde voorhanden hoeveelheid | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 02-02-2022 | 17 | | | 17 | 12 |
    | 03-02-2022 | 17 | 10 | | 27 | 12 |
    | 04-02-2022 | 17 | | 15 | 12 | 12 |
    | 05-02-2022 | 17 | 1 | | 13 | 13 |
    | 06-02-2022 | 17 | 3 | | 16 | 16 |
    | 07-02-2022 | 17 | | | 16 | 16 |
    | 08-02-2022 | 17 | | | 16 | 16 |

1. Twee dagen later (4 februari 2022) is de aanbodhoeveelheid van 10, die voor 3 februari was gepland, echter nog steeds niet gearriveerd. De volgende tabel geeft het resultaat weer.

    | Datum | Voorhanden | Gepland aanbod | Geplande vraag | Geprojecteerde voorhanden hoeveelheid | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 04-02-2022 | 17 | | 15 | 2 | 2 |
    | 05-02-2022 | 17 | 1 | | 3 | 3 |
    | 06-02-2022 | 17 | 3 | | 6 | 6 |
    | 07-02-2022 | 17 | | | 6 | 6 |
    | 08-02-2022 | 17 | | | 6 | 6 |
    | 09-02-2022 | 17 | | | 6 | 6 |
    | 10-02-2022 | 17 | | | 6 | 6 |

    Zoals u ziet, hebben de geplande (maar niet doorgevoerde) wijzigingen in de voorhanden hoeveelheid geen invloed op de werkelijke voorhanden hoeveelheid.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>Wijzigingsplanningen, wijzigingsgebeurtenissen en ATP-query's indienen via de API

U kunt de volgende API-URL's (Application Programming Interface) gebruiken om wijzigingsplanningen voor voorhanden hoeveelheden, wijzigingsgebeurtenissen en query's in te dienen.

| Pad | methode | Description |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Maak één geplande wijziging in de voorhanden hoeveelheid. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Maak meerdere geplande wijzigingen in de voorhanden hoeveelheid. |
| `/api/environment/{environmentId}/onhand` | `POST` | Maak één wijzigingsgebeurtenis voor de voorhanden hoeveelheid. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Maak meerdere wijzigingsgebeurtenissen. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Voer query uit met de `POST`-methode. |
| `/api/environment/{environmentId}/onhand` | `GET` | Voer query uit met de `GET`-methode. |
| `/api/environment/{environmentId}/onhand/exactquery` | `POST` | Voer een exacte query uit met de `POST`-methode. |

Zie [Openbare API's voor Voorraadzichtbaarheid](inventory-visibility-api.md) voor meer informatie.

### <a name="create-one-on-hand-change-schedule"></a>Eén planning van wijziging in voorhanden hoeveelheid maken

Er wordt een planning van wijziging van de voorhanden hoeveelheid gemaakt door een `POST`-aanvraag in te dienen bij de relevante URL van de service voor voorraadzichtbaarheid (zie de sectie [Wijzigingsplanningen, wijzigingsgebeurtenissen en ATP-query's indienen via de API](#api-urls)). U kunt ook bulkaanvragen indienen.

Een planning van wijziging in de voorhanden hoeveelheid kan alleen worden gemaakt als de geplande datum tussen de huidige datum en het einde van de huidige planningsperiode valt. De notatie voor datum/tijd moet *dag-maand-jaar* zijn ( **bijvoorbeeld 01-02-2022**). De tijdnotatie moet alleen tot op de dag nauwkeurig zijn.

Met deze API wordt één wijzigingsplanning voor voorhanden voorraad gemaakt.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

In het volgende voorbeeld wordt een voorbeeld gegeven van de inhoud van de hoofdtekst zonder `dimensionDataSource`.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Meerdere planningen van wijziging in voorhanden hoeveelheid maken

Met deze API kunnen meerdere records tegelijkertijd worden gemaakt. De enige verschillen tussen deze API en de API met één gebeurtenis zijn de waarden `Path` en `Body`. Voor deze API biedt `Body` een matrix van records. Het maximum aantal records is 512. Daarom kan de bulk-API voor planning van wijziging in voorhanden hoeveelheid maximaal 512 geplande wijzigingen per keer ondersteunen.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

In het volgende voorbeeld wordt een voorbeeld van de inhoud van de hoofdtekst weergegeven.

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Wijzigingsgebeurtenissen maken voor voorhanden voorraad

U kunt gebeurtenissen voor wijziging van de voorhanden hoeveelheid opstellen door een `POST`-aanvraag in te dienen bij de relevante URL van de service voor voorraadzichtbaarheid (zie de sectie [Wijzigingsplanningen, wijzigingsgebeurtenissen en ATP-query's indienen via de API](#api-urls)). U kunt ook bulkaanvragen indienen.

> [!NOTE]
> Gebeurtenissen voor het wijzigen van de voorhanden hoeveelheid zijn niet uniek voor de ATP-functionaliteit, maar maken deel uit van de standaard API voor Voorraadzichtbaarheid. Dit voorbeeld is opgenomen omdat gebeurtenissen relevant zijn wanneer u met ATP werkt. Gebeurtenissen voor wijziging van de voorhanden hoeveelheid lijken op reserveringen voor wijzigingen van de voorhanden hoeveelheid, maar gebeurtenisberichten moeten naar een andere API-URL worden verzonden en gebeurtenissen maken gebruik van `quantities` in plaats van `quantityByDate` in de hoofdtekst van het bericht. Zie [Openbare API's voor Voorraadzichtbaarheid](inventory-visibility-api.md#create-one-onhand-change-event) voor meer informatie over de gebeurtenissen voor het wijzigen van de voorhanden hoeveelheid en en andere functies van de API voor Voorraadzichtbaarheid.

In het volgende voorbeeld wordt een aanvraagbody weergegeven die een enkele gebeurtenis voor wijziging van de voorhanden hoeveelheid bevat.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Een query uitvoeren op de geplande wijzigingen in de voorhanden hoeveelheid en de ATP-resultaten

U kunt een query uitvoeren op geplande wijzigingen in de voorhanden hoeveelheid en ATP-resultaten door een `POST`-aanvraag of een `GET`-aanvraag in te dienen bij de juiste API-URL (zie de sectie [Wijzigingsplanningen, wijzigingsgebeurtenissen en ATP-query's indienen via de API](#api-urls)).

Stel in uw aanvraag `QueryATP` in op *true* als u een query wilt uitvoeren op de geplande wijzigingen in de voorhanden hoeveelheid en ATP-resultaten.

- Als u de aanvraag indient via de `GET`-methode, stelt u deze parameter in de URL in.
- Als u de aanvraag indient via de `POST`-methode, stelt u deze parameter in de aanvraagbody in.

> [!NOTE]
> Ongeacht of de parameter `returnNegative` is ingesteld op *true* of *false* in de aanvraagbody, het resultaat bevat negatieve waarden wanneer u een query uitvoert op geplande wijzigingen in de voorhanden hoeveelheid en ATP-resultaten. Deze negatieve waarden worden opgenomen omdat de geplande wijzigingen in de voorhanden hoeveelheid negatief zijn als er alleen vraagorders zijn gepland of als de aanbodhoeveelheden kleiner zijn dan de vraaghoeveelheden. Als negatieve waarden niet werden opgenomen, zouden de resultaten tot verwarring leiden. Zie [Openbare API's voor Voorraadzichtbaarheid](inventory-visibility-api.md#query-with-post-method) voor meer informatie over deze optie en de manier waarop deze werkt voor andere typen query's.

### <a name="query-by-using-the-post-method"></a>Een query uitvoeren met de POST-methode

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Het volgende voorbeeld laat zien hoe u een aanvraagbody met een index-query maakt die met behulp van de `POST`-methode bij Voorraadzichtbaarheid kan worden ingediend.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "SiteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-by-using-the-get-method"></a>Een query uitvoeren met de GET-methode

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

In het volgende voorbeeld wordt getoond hoe u een aanvraag-URL met een index-query maakt als `GET`-aanvraag.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Het resultaat van deze `GET`-aanvraag is exact hetzelfde als het resultaat van de `POST`-aanvraag in het vorige voorbeeld.

### <a name="exact-query-by-using-the-post-method"></a>Voer een exacte query uit met de POST-methode

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Het volgende voorbeeld laat zien hoe u een aanvraagbody met een exacte query maakt die met behulp van de `POST`-methode bij Voorraadzichtbaarheid kan worden ingediend.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "dimensions": ["SiteId", "LocationId"],
        "values": [
            ["1", "11"]
        ]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-result-example"></a>Voorbeeld van queryresultaat

Elk van de eerdere queryvoorbeelden kunnen het volgende antwoord opleveren. Voor dit voorbeeld is het systeem geconfigureerd met de volgende instellingen:

- **Berekende meting voor ATP:** *iv.onhand = pos.inbound – pos.outbound*
- **Planningsperiode:** *7*

Hier volgt een voorbeeld van de antwoordbody.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
