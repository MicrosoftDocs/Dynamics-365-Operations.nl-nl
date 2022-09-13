---
title: Openbare API's voor Inventory Visibility
description: In dit artikel worden de openbare API's beschreven die worden geleverd door Voorraadzichtbaarheid.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 14812fc201ba1038a78ea3317686dbe189ffa687
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423590"
---
# <a name="inventory-visibility-public-apis"></a>Openbare API's voor Inventory Visibility

[!include [banner](../includes/banner.md)]


In dit artikel worden de openbare API's beschreven die worden geleverd door Voorraadzichtbaarheid.

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
| /api/environment/{environmentId}/onhand/unreserve | Boeken | [Eén reserveringsgebeurtenis terugdraaien](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | Boeken | [Meerdere reserveringsgebeurtenissen terugdraaien](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Boeken | [Eén geplande wijziging in de voorhanden hoeveelheid maken](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Boeken | [Meerdere geplande wijzigingen in de voorhanden hoeveelheid maken](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Boeken | [Een query uitvoeren met de post-methode](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Ophalen | [Een query uitvoeren met de get-methode](#query-with-get-method) |
| /api/environment/{environmentId}/allocation/allocate | Boeken | [Eén toewijzingsgebeurtenis maken](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/unallocate | Boeken | [Eén gebeurtenis voor ongedaan maken van toewijzing maken](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/reallocate | Boeken | [Eén gebeurtenis voor opnieuw toewijzen maken](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/consume | Boeken | [Eén verbruiksgebeurtenis maken](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/query | Boeken | [Querytoewijzingsresultaat](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Het deel {environmentId} van het pad is de omgevings-id in Microsoft Dynamics Lifecycle Services (LCS).
> 
> De bulk-API kan maximaal 512 records voor elke aanvraag retourneren.

Microsoft heeft een gebruiksklare *Postman*-aanvraagverzameling geleverd. U kunt deze verzameling in uw *Postman*-software importeren via de volgende gedeelde koppeling: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Het eindpunt vinden volgens uw Lifecycle Services-omgeving

De microservice van Voorraadzichtbaarheid wordt in Microsoft Azure Service Fabric geïmplementeerd in meerdere geografieën en regio's. Er is op dit moment geen centraal eindpunt waarmee uw aanvraag automatisch kan worden omgeleid naar de overeenkomstige geografie en regio. U moet daarom de stukken informatie in een URL samenstellen door het volgende patroon te gebruiken:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

De korte naam van de regio kunt u vinden in de Microsoft Dynamics Lifecycle Services-omgeving (LCS). In de volgende tabel worden de regio's weergegeven die momenteel beschikbaar zijn.

| Azure-regio        | Korte naam regio |
| ------------------- | ----------------- |
| Australië - oost      | eau               |
| Australië - zuidoost | seau              |
| Canada - centraal      | cca               |
| Canada - oost         | eca               |
| Noord-Europa        | neu               |
| West-Europa         | weu               |
| VS - oost             | eus               |
| VS - west             | wus               |
| VK -zuid            | suk               |
| VK - west             | wuk               |
| Japan - oost          | ejp               |
| Japan - west          | wjp               |
| Brazilië - zuid        | sbr               |
| Zuid-centraal VS    | scus              |

Het eilandnummer is waar uw LCS-omgeving is geïmplementeerd op Service Fabric. Er is op dit moment geen manier om deze informatie van gebruikers op te halen.

Microsoft heeft een gebruikersinterface (UI) in Power Apps gemaakt zodat u de beschikking hebt over het volledige eindpunt van de microservice. Zie [Het service-eindpunt vinden](inventory-visibility-configuration.md#get-service-endpoint) voor meer informatie.

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Authenticatie

Het beveiligingstoken voor het platform wordt gebruikt om de openbare API Voorraadzichtbaarheid aan te roepen. U moet daarom een _Azure Active Directory-token (Azure AD)_ genereren met uw Azure AD-toepassing. Vervolgens moet u het Azure AD-token gebruiken om het _toegangstoken_ op te halen van de beveiligingsservice.

Microsoft biedt een gebruiksklare *Postman*-verzameling voor het ophalen van tokens. U kunt deze verzameling in uw *Postman*-software importeren via de volgende gedeelde koppeling: <https://www.getpostman.com/collections/496645018f96b3f0455e>

Ga als volgt te werk om een beveiligingstoken voor de service te krijgen.

1. Meld u aan bij de Azure-portal en gebruik de portal om de waarden `clientId` en `clientSecret` voor uw Dynamics 365 Supply Chain Management-app te vinden.
1. Haal een Azure AD-token (`aadToken`) op door een HTTP-aanvraag met de volgende eigenschappen in te dienen:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
   - **Methode:** `GET`
   - **Inhoud hoofdtekst (formuliergegevens):**

     | Sleutel           | Waarde                                            |
     | ------------- | -------------------------------------------------|
     | client_id     | ${aadAppId}                                      |
     | client_secret | ${aadAppSecret}                                  |
     | grant_type    | client_credentials                               |
     | bereik         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

   U moet een Azure AD-token (`aadToken`) als reactie ontvangen. Het resultaat moet lijken op het volgende voorbeeld.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
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
       "context": "{$LCS_environment_id}",
       "context_type": "finops-env"
   }
   ```

   Let op de volgende punten:

   - De waarde `client_assertion` moet het Azure AD-token (`aadToken`) zijn dat u in de vorige stap hebt ontvangen.
   - De waarde `context` moet de LCS-omgevings-id zijn waarin u de invoegtoepassing wilt implementeren.
   - Stel alle andere waarden in zoals in het voorbeeld wordt weergegeven.

1. Haal een toegangstoken (`access_token`) op door een HTTP-aanvraag in te dienen met de volgende eigenschappen:

   - **URL:** `https://securityservice.operations365.dynamics.com/token`
   - **Methode:** `POST`
   - **HTTP-header:** neem de API-versie op. (De sleutel is `Api-Version` en de waarde is `1.0`.)
   - **Inhoud hoofdtekst:** neem de JSON-aanvraag op die u in de vorige stap hebt gemaakt.

   U moet een toegangstoken (`access_token`) als reactie ontvangen. U moet dit token gebruiken als Bearer-token voor het aanroepen van de API Voorraadzichtbaarheid. Dit is een voorbeeld.

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> Wanneer u de *Postman*-aanvraagverzameling gebruikt om openbare API's voor Voorraadzichtbaarheid aan te roepen, moet u voor elke aanvraag een Bearer-token toevoegen. Als u het Bearer-token wilt vinden, selecteert u het tabblad **Autorisatie** onder de aanvraag-URL, selecteert u het type **Bearer-token** en kopieert u het toegangstoken dat in de laatste stap is opgehaald. In latere secties van dit artikel wordt `$access_token` gebruikt om het token te vertegenwoordigen dat in de laatste stap is opgehaald.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Wijzigingsgebeurtenissen maken voor voorhanden voorraad

Er zijn twee API's voor het maken van wijzigingsgebeurtenissen voor voorhanden voorraad:

- Eén record maken: `/api/environment/{environmentId}/onhand`
- Meerdere records maken: `/api/environment/{environmentId}/onhand/bulk`

In de volgende tabel wordt de betekenis van elk veld in de JSON-tekst samengevat.

| Veld-id | Description |
|---|---|
| `id` | Een unieke id voor de specifieke wijzigingsgebeurtenis. Als vanwege een servicefout de gegevens opnieuw worden ingediend, wordt deze id gebruikt om ervoor te zorgen dat dezelfde gebeurtenis niet twee keer in het systeem wordt geteld. |
| `organizationId` | De id van de organisatie die aan de gebeurtenis is gekoppeld. Deze wordt toegewezen aan een organisatie of gegevensgebied-id in Supply Chain Management. |
| `productId` | De identificatie van het product. |
| `quantities` | De hoeveelheid waarmee de voorhanden hoeveelheid moet worden gewijzigd. Als er bijvoorbeeld 10 nieuwe boeken aan een plank worden toegevoegd, is deze waarde `quantities:{ shelf:{ received: 10 }}`. Als er drie boeken worden verwijderd van de plank of worden verkocht, is deze waarde `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | De gegevensbron van de dimensies die worden gebruikt bij het boeken van de wijzigingsgebeurtenis en de query. Als u de gegevensbron opgeeft, kunt u de aangepaste dimensies gebruiken van de opgegeven gegevensbron. Voorraadzichtbaarheid kan de dimensieconfiguratie gebruiken om de aangepaste dimensies toe te wijzen aan de algemene standaarddimensies. Als er geen waarde voor `dimensionDataSource` is opgegeven, kunt u alleen de algemene [basisdimensies](inventory-visibility-configuration.md#data-source-configuration-dimension) in uw query's gebruiken. |
| `dimensions` | Een dynamisch sleutelwaardepaar. De waarden worden aan enkele van de dimensies in Supply Chain Management toegewezen. U kunt echter ook aangepaste dimensies toevoegen (bijvoorbeeld _Bron_) om aan te geven of de gebeurtenis afkomstig is uit Supply Chain Management of uit een extern systeem. |

> [!NOTE]
> De parameters `locationId` en `siteId` vormen de [partitieconfiguratie](inventory-visibility-configuration.md#partition-configuration). U moet deze parameters daarom opgeven in dimensies wanneer u wijzigingsgebeurtenissen voor voorhanden voorraad maakt, voorhanden hoeveelheden instelt of overschrijft of reserveringsgebeurtenissen maakt.

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
    "organizationId": "SCM_IV",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

In het volgende voorbeeld wordt een voorbeeld gegeven van de inhoud van de hoofdtekst zonder `dimensionDataSource`. In dit geval zijn `dimensions` de [basisdimensies](inventory-visibility-configuration.md#data-source-configuration-dimension). Als `dimensionDataSource` is ingesteld, kunnen `dimensions` de gegevensbrondimensies of de basisdimensies zijn.

```json
{
    "id": "123456",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Meerdere wijzigingsgebeurtenissen maken

Met deze API kunnen meerdere records tegelijkertijd worden gemaakt. De enige verschillen tussen deze API en de [API met één gebeurtenis](#create-one-onhand-change-event) zijn de waarden `Path` en `Body`. Voor deze API biedt `Body` een matrix van records. Het maximum aantal records is 512, wat betekent dat de bulk-API voor wijziging van de voorhanden hoeveelheden tot 512 wijzigingsgebeurtenissen tegelijk kan ondersteunen.

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
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "posSite1",
            "posLocationId": "posLocation1",
            "posMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_2",
        "dimensions": {
            "siteId": "iv_postman_site",
            "locationId": "iv_postman_location",
            "colorId&quot;: &quot;black"
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

In het volgende voorbeeld wordt een voorbeeld van de inhoud van de hoofdtekst weergegeven. Het gedrag van deze API verschilt van het gedrag van de API's dat wordt beschreven in de sectie [Wijzigingsgebeurtenissen maken voor voorhanden voorraad](#create-onhand-change-event) eerder in dit artikel. In dit voorbeeld wordt de hoeveelheid van het product *T-shirt* ingesteld op 1.

```json
[
    {
        "id": "123456",
        "organizationId": "SCM_IV",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "iv_postman_site",
            "posLocationId": "iv_postman_location",
            "posMachineId": "0001"
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

Als u de *Reserve*-API wilt gebruiken, moet u de reserveringsfunctie inschakelen en de reserveringsconfiguratie voltooien. Zie [Reserveringscofiguratie (optioneel)](inventory-visibility-configuration.md#reservation-configuration) voor meer informatie.

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Eén reserveringsgebeurtenis maken

Er kan een reservering worden gemaakt met verschillende instellingen voor de gegevensbron. Als u dit type reservering wilt configureren, geeft u eerst de gegevensbron op in de parameter `dimensionDataSource`. Geef vervolgens in de parameter `dimensions` de dimensies op aan de hand van de dimensie-instellingen in de doelgegevensbron.

Wanneer u de reserverings-API aanroept, kunt u de reserveringsvalidatie beheren door de booleaanse parameter `ifCheckAvailForReserv` op te geven in de aanvraagbody. De waarde `True` betekent dat de validatie is vereist, terwijl de waarde `False` betekent dat de validatie niet is vereist. De standaardwaarde is `True`.

Als u een reservering wilt terugdraaien of de reservering van opgegeven voorraadhoeveelheden wilt verwijderen, stelt u de hoeveelheid in op een negatieve waarde en stelt u de parameter `ifCheckAvailForReserv` in op `False` om de validatie over te slaan. U kunt dit ook doen met een speciale API voor het opheffen van de reservering. Het verschil is alleen de manier waarop de twee API's worden aangeroepen. U kunt een specifieke reserveringsgebeurtenis eenvoudiger terugdraaien door gebruik te maken van `reservationId` met de *unreserve* API. Raadpleeg het gedeelte [_Eén reserveringsgebeurtenis terugdraaien_](#reverse-reservation-events) voor meer informatie.

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
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

In het volgende voorbeeld is een geslaagd antwoord gegeven.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Meerdere reserveringsgebeurtenissen maken

Deze API is een bulkversie van de [API voor één gebeurtenis](#create-reservation-events).

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

## <a name="reverse-reservation-events"></a>Reserveringsgebeurtenissen terugdraaien

De *Unreserve* API wordt gebruikt als de omgekeerde bewerking voor [*reserveringsgebeurtenissen*](#create-reservation-events). Het is een manier om een reserveringsgebeurtenis terug te draaien die is opgegeven met `reservationId` of om de reserveringshoeveelheid te verlagen.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>Eén reserveringsgebeurtenis terugdraaien

Wanneer u een reservering maakt, wordt een `reservationId` opgenomen in de antwoordtekst. Geef dezelfde `reservationId` op om de reservering te annuleren en neem dezelfde `organizationId` en `dimensions` op voor de API-aanroep voor reservering. Geef ten slotte een `OffsetQty`-waarde op voor het aantal items dat moet worden vrij gemaakt uit de vorige reservering. Een reservering kan volledig of gedeeltelijk worden teruggedraaid, afhankelijk van de opgegeven `OffsetQty`-reservering. Als er bijvoorbeeld *100* eenheden zijn gereserveerd, geeft u `OffsetQty: 10` op om *10* van de oorspronkelijke gereserveerde hoeveelheid terug te draaien.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

In de volgende code ziet u een voorbeeld van de inhoud van de hoofdtekst.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

In de volgende code ziet u een voorbeeld van een geslaagd antwoord.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Wanneer in de antwoordtekst `OffsetQty` kleiner is dan of gelijk is aan de reserveringshoeveelheid, is de `processingStatus` *geslaagd* en is `totalInvalidOffsetQtyByReservId` *0*.
>
> Als `OffsetQty` groter is dan de gereserveerde hoeveelheid, is `processingStatus` *partialSuccess* en geeft `totalInvalidOffsetQtyByReservId` het verschil aan tussen `OffsetQty` en de gereserveerde hoeveelheid.
>
>Als de reservering bijvoorbeeld een hoeveelheid van *10* heeft en `OffsetQty` een waarden van *12*, is `totalInvalidOffsetQtyByReservId` *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>Meerdere reserveringsgebeurtenissen terugdraaien

Deze API is een bulkversie van de [API voor één gebeurtenis](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Voorhanden query

Gebruik de API *Voorhanden query* om huidige voorhanden voorraadgegevens voor uw producten op te halen. De API ondersteunt momenteel query's met maximaal 5000 afzonderlijke artikelen per `productID`-waarde. Ook kunnen in elke query meerdere `siteID`- en `locationID`-waarden worden opgegeven. De maximumlimiet wordt met de volgende vergelijking gedefinieerd:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

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

In de hoofdtekst van deze aanvraag is `dimensionDataSource` nog steeds een optionele parameter. Als deze parameter niet is ingesteld, worden `filters` als *basisdimensies* beschouwd. Er zijn vier velden vereist voor `filters`: `organizationId`, `productId`, `siteId` en `locationId`.

- `organizationId` mag slechts één waarde bevatten, maar is nog steeds een matrix.
- `productId` kan een of meer waarden bevatten. Als het een lege matrix is, worden alle producten geretourneerd.
- `siteId` en `locationId` worden voor partitionering in Voorraadzichtbaarheid gebruikt. U kunt meer dan één waarde voor `siteId` en `locationId` opgeven in een aanvraag voor een *Voorhanden query*. In de huidige versie moet u zowel een waarde voor `siteId` als voor `locationId` opgeven.

De parameter `groupByValues` kan het beste uw configuratie voor indexering volgen. Zie [Configuratie van productindexhiërarchie](./inventory-visibility-configuration.md#index-configuration) voor meer informatie.

De parameter `returnNegative` bepaalt of de resultaten negatieve vermeldingen bevatten.

> [!NOTE]
> Als u de functies voor planning van wijzigingen in voorhanden voorraad en available to promise (ATP) hebt ingeschakeld, kan uw query ook de booleaanse parameter `QueryATP` bevatten, waarmee wordt bepaald of de queryresultaten ATP-informatie bevatten. Zie [Planningen van wijzigingen in voorhanden hoeveelheid en available to promise in Voorraadzichtbaarheid](inventory-visibility-available-to-promise.md) voor meer informatie en voorbeelden.

In het volgende voorbeeld wordt een voorbeeld van de inhoud van de hoofdtekst weergegeven.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Het volgende voorbeeld laat zien hoe u een query uitvoert op een specifieke site en locatie.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Een query uitvoeren met de get-methode

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

Hier is een voorbeeld van een get-URL. Deze get-aanvraag is exact hetzelfde als het post-voorbeeld dat eerder is opgegeven.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="available-to-promise"></a>Available to promise

U kunt Voorraadzichtbaarheid zo instellen dat u toekomstige wijzigingen in de voorhanden voorraad kunt plannen en ATP-hoeveelheden kunt berekenen. ATP is de hoeveelheid van een artikel, die beschikbaar is en die aan een klant kan worden beloofd in de volgende periode. Het gebruik van de ATP-berekening kan uw capaciteit voor het afhandelen van orders veel groter maken. Zie [Planningen van wijzigingen in voorhanden hoeveelheid en available to promise in Voorraadzichtbaarheid](inventory-visibility-available-to-promise.md#api-urls) voor informatie over hoe u deze functie kunt inschakelen en hoe u kunt communiceren met Voorraadzichtbaarheid via de bijbehorende API nadat de functie is ingeschakeld.

## <a name="allocation"></a>Toewijzing

Toewijzingsgerelateerde API's bevinden zich in de [toewijzing Voorraadzichtbaarheid](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
