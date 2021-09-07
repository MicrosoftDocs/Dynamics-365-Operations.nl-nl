---
title: Openbare API's voor Voorraadzichtbaarheid
description: In dit onderwerp worden de openbare API's beschreven die worden geleverd door Voorraadzichtbaarheid.
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
ms.openlocfilehash: 0aca5838ff6d7c9c4d881698be1e2da2e0e1c02e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343627"
---
# <a name="inventory-visibility-public-apis"></a>Openbare API's voor Voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In dit onderwerp worden de openbare API's beschreven die worden geleverd door Voorraadzichtbaarheid.

De openbare REST API van de invoegtoepassing Voorraadzichtbaarheid biedt verschillende specifieke eindpunten voor integratie. De API ondersteunt vier hoofdinteractietypen:

- Wijzigingen in de voorhanden voorraad naar de invoegtoepassing boeken vanuit een extern systeem
- Instellen of overschrijven van voorhanden voorraadhoeveelheden in de invoegtoepassing vanuit een extern systeem
- Reserveringsgebeurtenissen boeken naar de invoegtoepassing vanuit een extern systeem
- Huidige voorhanden hoeveelheden opvragen vanuit een extern systeem

De volgende tabel bevat de API's die momenteel beschikbaar zijn:

| Pad | methode | Beschrijving |
|---|---|---|
| /api/environment/{environmentId}/onhand | Plaatsen | [Eén wijzigingsgebeurtenis maken voor voorhanden voorraad](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Plaatsen | [Meerdere wijzigingsgebeurtenissen maken voor voorhanden voorraad](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Plaatsen | [Voorhanden hoeveelheden instellen/overschrijven](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Plaatsen | [Eén reserveringsgebeurtenis maken](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Plaatsen | [Meerdere reserveringsgebeurtenissen maken](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | Ophalen | [Een query uitvoeren met de post-methode](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | Plaatsen | [Een query uitvoeren met de get-methode](#query-with-get-method) |

Microsoft heeft een gebruiksklare *Postman*-aanvraagverzameling geleverd. U kunt deze verzameling in uw *Postman*-software importeren via de volgende gedeelde koppeling: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Het eindpunt vinden volgens uw Lifecycle Services-omgeving

De microservice van Voorraadzichtbaarheid wordt in Microsoft Azure Service Fabric geïmplementeerd in meerdere geografieën en regio's. Er is op dit moment geen centraal eindpunt waarmee uw aanvraag automatisch kan worden omgeleid naar de overeenkomstige geografie en regio. U moet daarom de stukken informatie in een URL samenstellen door het volgende patroon te gebruiken:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

De korte naam van de regio kunt u vinden in de Microsoft Dynamics Lifecycle Services-omgeving (LCS). In de volgende tabel worden de regio's weergegeven die momenteel beschikbaar zijn.

| Azure-regio | Korte naam regio |
|---|---|
| Australië - oost | eau |
| Australië - zuidoost | seau |
| Canada - centraal | cca |
| Canada - oost | eca |
| Noord-Europa | neu |
| West-Europa | weu |
| VS - oost | eus |
| VS - west | wus |
| VK -zuid | suk |
| VK - west | wuk |

Het eilandnummer is waar uw LCS-omgeving is geïmplementeerd op Service Fabric. Er is op dit moment geen manier om deze informatie van gebruikers op te halen.

Microsoft heeft een gebruikersinterface (UI) in Power Apps gemaakt zodat u de beschikking hebt over het volledige eindpunt van de microservice. Zie [Het service-eindpunt vinden](inventory-visibility-power-platform.md#get-service-endpoint) voor meer informatie.

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Authenticatie

Het beveiligingstoken voor het platform wordt gebruikt om de openbare API Voorraadzichtbaarheid aan te roepen. U moet daarom een _Azure Active Directory (Azure AD)-token_ genereren met de Azure AD-toepassing. Vervolgens moet u het Azure AD-token gebruiken om het _toegangstoken_ op te halen van de beveiligingsservice.

Ga als volgt te werk om een beveiligingstoken voor de service te krijgen.

1. Meld u aan bij de Azure-portal en gebruik de portal om de waarden `clientId` en `clientSecret` voor uw Dynamics 365 Supply Chain Management-app te vinden.
1. Haal een Azure AD-token (`aadToken`) op door een HTTP-aanvraag met de volgende eigenschappen in te dienen:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Methode:** `GET`
    - **Inhoud hoofdtekst (formuliergegevens):**

        | Sleutel | Waarde |
        |---|---|
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | resource | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

    U moet een Azure AD-token (`aadToken`) als reactie ontvangen. Het resultaat moet lijken op het volgende voorbeeld.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Formuleer een JSON-aanvraag (JavaScript Object Notation) die op het volgende voorbeeld lijkt.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Let op de volgende punten:

    - De waarde `client_assertion` moet het Azure AD-token (`aadToken`) zijn dat u in de vorige stap hebt ontvangen.
    - De waarde `context` moet de omgevings-id zijn waarin u de invoegtoepassing wilt implementeren.
    - Stel alle andere waarden in zoals in het voorbeeld wordt weergegeven.

1. Dien een HTTP-aanvraag in met de volgende eigenschappen:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Methode:** `POST`
    - **HTTP-header:** neem de API-versie op. (De sleutel is `Api-Version` en de waarde is `1.0`.)
    - **Inhoud hoofdtekst:** neem de JSON-aanvraag op die u in de vorige stap hebt gemaakt.

    U moet een toegangstoken (`access_token`) als reactie ontvangen. U moet dit token gebruiken als Bearer-token voor het aanroepen van de API Voorraadzichtbaarheid. Hier volgt een voorbeeld.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

In latere secties gebruikt u `$access_token` om het token te vertegenwoordigen dat in de laatste stap is opgehaald.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Wijzigingsgebeurtenissen maken voor voorhanden voorraad

Er zijn twee API's voor het maken van wijzigingsgebeurtenissen voor voorhanden voorraad:

- Eén record maken: `/api/environment/{environmentId}/onhand`
- Meerdere records maken: `/api/environment/{environmentId}/onhand/bulk`

In de volgende tabel wordt de betekenis van elk veld in de JSON-tekst samengevat.

| Veld-id | Beschrijving |
|---|---|
| `id` | Een unieke id voor de specifieke wijzigingsgebeurtenis. Deze id wordt gebruikt om ervoor te zorgen dat, als bij het boeken de communicatie met de service mislukt, dezelfde gebeurtenis niet twee keer in het systeem wordt geteld als deze opnieuw wordt ingediend. |
| `organizationId` | De id van de organisatie die aan de gebeurtenis is gekoppeld. Deze wordt toegewezen aan een organisatie of gegevensgebied-id in Supply Chain Management. |
| `productId` | De identificatie van het product. |
| `quantities` | De hoeveelheid waarmee de voorhanden hoeveelheid moet worden gewijzigd. Als er bijvoorbeeld 10 nieuwe boeken aan een plank worden toegevoegd, is deze waarde `quantities:{ shelf:{ received: 10 }}`. Als er drie boeken worden verwijderd van de plank of worden verkocht, is deze waarde `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | De gegevensbron van de dimensies die worden gebruikt bij het boeken van de wijzigingsgebeurtenis en de query. Als u de gegevensbron opgeeft, kunt u de aangepaste dimensies gebruiken van de opgegeven gegevensbron. Voorraadzichtbaarheid kan de dimensieconfiguratie gebruiken om de aangepaste dimensies toe te wijzen aan de algemene standaarddimensies. Als er geen waarde voor `dimensionDataSource` is opgegeven, kunt u alleen de algemene [basisdimensies](inventory-visibility-configuration.md#data-source-configuration-dimension) in uw query's gebruiken. |
| `dimensions` | Een dynamisch sleutelwaardepaar. De waarden worden aan enkele van de dimensies in Supply Chain Management toegewezen. U kunt echter ook aangepaste dimensies toevoegen (bijvoorbeeld _Bron_) om aan te geven of de gebeurtenis afkomstig is uit Supply Chain Management of uit een extern systeem. |

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Eén wijzigingsgebeurtenis maken voor voorhanden voorraad

Met deze API wordt ëén wijzigingsgebeurtenis gemaakt voor voorhanden voorraad.

```txt
Path:
    /api/environment/{environmentId}/onhand
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
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

In het volgende voorbeeld wordt een voorbeeld van de inhoud van de hoofdtekst weergegeven. In dit voorbeeld boekt u een wijzigingsgebeurtenis voor het product *T-shirt*. Deze gebeurtenis is afkomstig van het POS-systeem (verkooppunt) en de klant heeft een rood T-shirt teruggestuurd naar uw winkel. Met deze gebeurtenis wordt de hoeveelheid van het product *T-shirt* verhoogd met 1.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

In het volgende voorbeeld wordt een voorbeeld gegeven van de inhoud van de hoofdtekst zonder `dimensionDataSource`.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Meerdere wijzigingsgebeurtenissen maken

Met deze API kunnen meerdere records tegelijkertijd worden gemaakt. De enige verschillen tussen deze API en de [API met één gebeurtenis](#create-one-onhand-change-event) zijn de waarden `Path` en `Body`. Voor deze API biedt `Body` een matrix van records.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "@PRODUCT1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Voorhanden hoeveelheden instellen/overschrijven

Met de API _Voorhanden set_ worden de huidige gegevens voor het opgegeven product overschreven.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

In het volgende voorbeeld wordt een voorbeeld van de inhoud van de hoofdtekst weergegeven. Het gedrag van deze API verschilt van het gedrag van de API's dat wordt beschreven in de sectie [Wijzigingsgebeurtenissen maken voor voorhanden voorraad](#create-onhand-change-event) eerder in dit onderwerp. In dit voorbeeld wordt de hoeveelheid van het product *T-shirt* ingesteld op 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Reserveringsgebeurtenissen maken

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Als u de *Reserve*-API wilt gebruiken, moet u de reserveringsfunctie activeren en de reserveringsconfiguratie voltooien. Zie [Reserveringscofiguratie (optioneel)](inventory-visibility-configuration.md#reservation-configuration) voor meer informatie.

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Eén reserveringsgebeurtenis maken

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
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
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

In het volgende voorbeeld wordt een voorbeeld van de inhoud van de hoofdtekst weergegeven.

```json
{
    "id": "reserve-0",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Meerdere reserveringsgebeurtenissen maken

Deze API is een bulkversie van de [API voor één gebeurtenis](#create-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
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
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="query-on-hand"></a>Voorhanden query

De API _Voorhanden query_ wordt gebruikt om huidige voorhanden voorraadgegevens voor uw producten op te halen.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Een query uitvoeren met de post-methode

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
        organizationId: string,
        filters: {
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

In het volgende voorbeeld wordt een voorbeeld van de inhoud van de hoofdtekst weergegeven.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Een query uitvoeren met de get-methode

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
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

Hier is een voorbeeld van een get-URL. Deze get-aanvraag is exact hetzelfde als het post-voorbeeld dat eerder is opgegeven.

```txt
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
