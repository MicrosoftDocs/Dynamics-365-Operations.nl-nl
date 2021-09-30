---
title: Reserveringen voor Voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven hoe u de reserveringsfunctie instelt om reserveringen te maken, reserveringen op te nemen en/of gespecificeerde voorraadhoeveelheden ongedaan te maken met behulp van Voorraadzichtbaarheid.
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
ms.openlocfilehash: 4a85520c0911bb7eed5842b3fd5bd706009351e5
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500350"
---
# <a name="inventory-visibility-reservations"></a>Voorraadzichtbaarheid-reserveringen

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In dit onderwerp wordt beschreven hoe u de reserveringsfunctie instelt om reserveringen te maken, reserveringen op te nemen en/of gespecificeerde voorraadhoeveelheden ongedaan te maken met behulp van Voorraadzichtbaarheid.

Reserveringen leggen een hoeveelheid voorraad vast die in de toekomst wordt gebruikt. Wanneer u een reservering maakt, voorkomt het systeem dat andere orders de gereserveerde goederen reserveren of opnemen, totdat de reservering wordt opgenomen of ongedaan wordt gemaakt. Reserveringen worden gemaakt, opgenomen en geannuleerd door API-aanroepen voor de service voor Voorraadzichtbaarheid te gebruiken.

U kunt Microsoft Dynamics 365 Supply Chain Management (en andere systemen van externe partijen) zodanig instellen dat de gereserveerde hoeveelheid automatisch wordt verrekend via Voorraadzichtbaarheid. De verrekende hoeveelheid wordt uit de reserveringsrecords in de Voorraadzichtbaarheid verwijderd.

Wanneer u de reserveringsfunctie inschakelt, is Supply Chain Management er automatisch klaar voor om reserveringen te verrekenen die met behulp van Voorraadzichtbaarheid worden gemaakt.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>De reserveringsfunctie inschakelen en instellen

Voer de volgende stappen uit om de reserveringsfunctie in te schakelen.

1. Meld u aan bij Power Apps en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Schakel in het tabblad **Functiebeheer** de functie *OnHandReservation* in.
1. Meld u aan bij Supply Chain Management.
1. Ga naar de werkruimte **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** en schakel de functie *Integratie van Voorraadzichtbaarheid met tegenreservering* in (hiervoor is versie 10.0.22 of hoger vereist).
1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor integratie van Voorraadzichtbaarheid**, open het tabblad **Tegenreservering** en stel het volgende in:
    - **Tegenreservering inschakelen**: stel de optie in op *Ja* om deze functionaliteit in te schakelen.
    - **Modificator voor tegenreservering**: selecteer de status van de voorraadtransactie om reserveringen die zijn gemaakt in Voorraadzichtbaarheid, te compenseren. Met deze instelling wordt de fase van de orderverwerking bepaald waarmee tegenreserveringen worden geactiveerd. De fase wordt door de voorraadtransactiestatus van de order opgevolgd. Kies een van de volgende opties:
        - *In bestelling*: voor de status *Op transactie* wordt een aanvraag voor een tegenreservering verzonden wanneer deze wordt gemaakt. De verrekende hoeveelheid is de hoeveelheid van de gemaakte order.
        - *Reserveren*: voor de status *Bestelde transactie reserveren* verzendt een order een tegenreserveringsaanvraag wanneer deze gereserveerd, verzameld, via de pakbon geboekt of gefactureerd wordt. De aanvraag wordt slechts eenmaal voor de eerste stap geactiveerd wanneer het bovengenoemde proces plaatsvindt. De verrekende hoeveelheid is de hoeveelheid waarvoor de status van de voorraadtransactie is gewijzigd van *Besteld* in *Gereserveerd* (of een latere status) op de corresponderende orderregel.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>De reserveringsfunctie in Voorraadzichtbaarheid gebruiken

Wanneer u de reserverings-API oproept, markeert het systeem de reservering van de opgegeven goederen en hoeveelheden. U moet een reserveringshiërarchie vastleggen en aanvragen boeken die met deze reserveringshiërarchie overeenkomen. De reserveringen kunnen vervolgens worden gemaakt door de reserverings-API's rechtstreeks op te roepen.

### <a name="configure-the-reservation-hierarchy"></a>De reserveringshiërarchie configureren

In de reserveringshiërarchie wordt de volgorde van dimensies beschreven die moeten worden opgegeven wanneer er reserveringen worden gemaakt. Dit werkt op dezelfde manier als de indexhiërarchie voor voorhanden query's.

De reserveringshiërarchie kan verschillen van de indexhiërarchie. Met deze onafhankelijkheid kunt u categoriebeheer implementeren, waarbij gebruikers de dimensies kunnen opsplitsen in details om de vereisten voor het maken van nauwkeurige reserveringen op te geven.

Als u een hiërarchie voor een zachte reserveringen wilt configureren in Power Apps, opent u de pagina **Configuratie** en stelt u vervolgens op het tabblad **Zachte reserveringshiërarchie** de reserveringshiërarchie in door dimensies en de bijbehorende hiërarchieniveaus toe te voegen en/of te wijzigen.

Uw zachte reserveringshiërarchie moet `SiteId` en `LocationId` als onderdelen bevatten, omdat ze de partitieconfiguratie vormen.

Zie [Reserveringsconfiguratie](inventory-visibility-configuration.md#reservation-configuration) voor meer informatie over het configureren van reserveringen.

### <a name="call-the-reservation-api"></a>De reserverings-API oproepen

Reserveringen worden in de service voor Voorraadzichtbaarheid gemaakt door een aanvraag naar de URL van de service te verzenden, zoals `/api/environment/{environment-ID}/onhand/reserve`.

Voor een reservering moet de hoofdtekst van de aanvraag een organisatie-ID, een product-ID, gereserveerde hoeveelheden en dimensies bevatten. De aanvraag genereert een unieke reserverings-ID voor elke reserveringsrecord. De reserveringsrecord bevat de unieke combinatie van de product-ID en dimensies.

Wanneer u de reserverings-API aanroept, kunt u de reserveringsvalidatie beheren door de booleaanse parameter `ifCheckAvailForReserv` op te geven in de aanvraagbody. De waarde `True` betekent dat de validatie is vereist, terwijl de waarde `False` betekent dat de validatie niet is vereist. De standaardwaarde is `True`.

Als u een reservering wilt annuleren of de reservering van opgegeven voorraadhoeveelheden wilt verwijderen, stelt u de hoeveelheid in op een negatieve waarde en stelt u de parameter `ifCheckAvailForReserv` in op `False` om de validatie over te slaan.

Ter referentie volgt hier een voorbeeld van de hoofdtekst van een aanvraag.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Tegenreserveringen gebruiken in Supply Chain Management

Voor voorraadtransactiestatussen die een gespecificeerde tegenreserveringsmodificator bevatten, verrekent de transactieupdate de bijbehorende reserveringsrecord als aan alle volgende voorwaarden voldaan is:

- De reserverings-ID van de voorraadtransactie komt overeen met de reserverings-ID van de reserveringsrecord in de service voor Voorraadzichtbaarheid.
- De dimensies van de voorraadtransactie komen overeen met de dimensies van de reserveringsrecord in de service voor Voorraadzichtbaarheid.
- Wijzigingen in de status van de voorraadtransactie zorgen voor tegenreserveringen wanneer de voorraadtransactiestatus uitwijst dat een orderproces voltooid of overgeslagen is.

De tegengereserveerde hoeveelheid volgt de voorraadhoeveelheid die in de voorraadtransacties opgegeven is. De tegenreservering wordt niet uitgevoerd als er geen gereserveerde hoeveelheid in de service voor Voorraadzichtbaarheid overblijft.

### <a name="set-up-the-reservation-offset-modifier"></a>De modificator voor tegenreserveringen instellen

Als u dit nog niet hebt gedaan, stelt u de reserveringsmodificator in zoals beschreven in [De reserveringsfunctie inschakelen en instellen](#turn-on).

### <a name="set-up-reservation-ids"></a>Reserverings-ID's instellen

Met de reserverings-ID wordt een reserveringsrecord uniek gemarkeerd in de Voorraadzichtbaarheid. In Supply Chain Management plaatsen gebruikers reserveringen in orderregels om de tegenreservering voor de bijbehorende reserveringsrecord te markeren.

Als u reserverings-ID's in Supply Chain Management wilt instellen, gaat u als volgt te werk.

1. Open een verkooporder (bijvoorbeeld vanuit de pagina **Alle verkooporders**).
1. Selecteer een orderregel in het sneltabblad **Verkooporderregels**.
1. Selecteer in de werkbalk van het sneltabblad **Verkooporderregels** de opties **Regel bijwerken \> Voorraad \> Integratie met Voorraadzichtbaarheid**.
1. Voer de juist reserverings-ID's in.

De wijziging in de voorraadstatus komt overeen met de instelling van de modificator voor tegenreserveringen.
