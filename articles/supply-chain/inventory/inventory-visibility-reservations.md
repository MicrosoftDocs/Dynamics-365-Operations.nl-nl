---
title: Reserveringen voor Inventory Visibility
description: In dit artikel wordt beschreven hoe u de reserveringsfunctie instelt om reserveringen te maken, reserveringen op te nemen en/of gespecificeerde voorraadhoeveelheden ongedaan te maken met behulp van Voorraadzichtbaarheid.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762717"
---
# <a name="inventory-visibility-reservations"></a>Reserveringen voor Inventory Visibility

[!include [banner](../includes/banner.md)]

In dit artikel wordt een standaard gebruikscase voor zachte reserveringen beschreven en wordt uitgelegd hoe u deze in Voorraadzichtbaarheid instelt. Het artikel bevat informatie over het maken van zachte reserveringen, het verrekening met het fysieke verbruik en het al dan niet aanpassen aan of verwijderen uit de gereserveerde voorraadhoeveelheden.

## <a name="sample-use-case-for-soft-reservation"></a>Voorbeeldgebruik voor zachte reservering

Met zachte reserveringen hebben organisaties één bron voor beschikbare voorraad, met name tijdens het afhandelingsproces voor de order. Deze functionaliteit is handig voor organisaties die de volgende voorwaarden voldoen:

- De organisatie heeft ten minste twee verschillende systemen die direct uitgaande orders aannemen.
- De organisatie is erg strikt en wil dubbele boeking van productvoorraad voorkomen, wat kan gebeuren als meerdere systemen het laatste deel van de voorraad kunnen overboeken. Deze situatie wordt voorkomen wanneer alle ordersystemen directe API-aanroepen voor zachte reservering kunnen maken naar Voorraadzichtbaarheid, waardoor één transparante bron voor de voorraadbeschikbaarheid mogelijk is.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="Zachte reserveringen voor voorraadzichtbaarheid" width="720" />](media/inventory-visibility-soft-reservation.png)

In de vorige afbeelding ziet u hoe zachte reservering werkt en worden de volgende bewerkingen aangegeven:

- Het oorspronkelijke voorraadniveau wordt gesynchroniseerd met Voorraadzichtbaarheid vanuit Microsoft Dynamics 365 Supply Chain Management.
- Zachte reserveringen worden vanuit elk van uw orderkanalen of systemen geboekt naar Voorraadzichtbaarheid. Met Voorraadzichtbaarheid wordt de beschikbare voorraad gevalideerd en wordt geprobeerd een zachte reservering te maken. Als een zachte reservering slaagt, wordt in Voorraadzichtbaarheid de zacht gereserveerde hoeveelheid toegevoegd en afgetrokken van de beschikbare hoeveelheid voor reservering (AFR). Vervolgens wordt gereageerd met een zachte reserverings-id.
- Op dit moment blijft de fysieke voorraadhoeveelheid hetzelfde.
- U kunt vervolgens één of samengevoegde zacht gereserveerde orders (orderregels) synchroniseren met Supply Chain Management om harde reserveringen te maken en deze naar het magazijn vrijgeven of de uiteindelijke voorraadhoeveelheid bijwerken.
- U kunt het systeem instellen om [zachte reserveringen te verrekenen](#offset-scm) wanneer de fysieke voorraad in Supply Chain Management wordt bijgewerkt.

Zachte reserveringen worden gewoonlijk gemaakt, opgenomen en geannuleerd door API-aanroepen voor de service voor Voorraadzichtbaarheid te gebruiken.

> [!NOTE]
> U kunt Supply Chain Management (en andere systemen van externe partijen) zodanig instellen dat de gereserveerde hoeveelheid automatisch wordt verrekend via Voorraadzichtbaarheid. De verrekende hoeveelheid wordt uit de reserveringsrecords in de Voorraadzichtbaarheid verwijderd.
>
> De verrekenfunctie wordt automatisch ingeschakeld wanneer u de functie voor zachte reservering inschakelt.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>De reserveringsfunctie inschakelen en instellen

Voer de volgende stappen uit om de reserveringsfunctie in te schakelen.

1. Meld u aan bij Power Apps en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie**.
1. Schakel in het tabblad **Functiebeheer** de functie *OnHandReservation* in.
1. Meld u aan bij uw Supply Chain Management-omgeving.
1. Ga naar de werkruimte **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** en schakel de functie *Integratie van Voorraadzichtbaarheid met tegenreservering* in (hiervoor is versie 10.0.22 of hoger vereist).
1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor integratie van Voorraadzichtbaarheid**, open het tabblad **Tegenreservering** en stel het volgende in:

    - **Tegenreservering inschakelen**: stel de optie in op *Ja* om deze functionaliteit in te schakelen.
    - **Modificator voor tegenreservering**: selecteer de status van de voorraadtransactie om reserveringen die zijn gemaakt in Voorraadzichtbaarheid, te compenseren. Met deze instelling wordt de fase van de orderverwerking bepaald waarmee tegenreserveringen worden geactiveerd. De fase wordt door de voorraadtransactiestatus van de order opgevolgd. Selecteer een van de volgende waarden:

        - *In bestelling*: voor orders met de status *In bestelling* wordt een aanvraag voor een tegenreservering verzonden wanneer deze wordt gemaakt. De verrekende hoeveelheid is de hoeveelheid van de gemaakte order(regel).
        - *Reserveren*: orders met de status *Reserve* verzenden een verrekenaanvraag als ze zijn gereserveerd voor de order of fysiek zijn gereserveerd. Wanneer u verrekent met de status *Reserve*, wordt een verrekeningsverzoek gedaan met een nieuwe voorraadstatus die het dichtst bij de gereserveerde en verzamelde order ligt (bijvoorbeeld verzamelen, geboekte pakbon of gefactureerd). Dit gedrag treedt zelfs op als u de reservering in Supply Chain Management overslaat en doorgaat naar een andere voorraadstatus (bijvoorbeeld als u van de vrijgave naar het magazijn naar verzamelen en verpakken gaat). De aanvraag wordt slechts eenmaal geactiveerd. Als deze is geactiveerd bij het verzamelen, wordt de verrekening niet dubbel uitgevoerd wanneer een pakbon wordt geboekt. De verrekende hoeveelheid is hetzelfde als de hoeveelheid van de voorraadtransactiestatus toen de verrekening werd geactiveerd (met andere woorden *Besteld en gereserveerd*/*Fysiek reserveren*, of een latere status, op de corresponderende orderregel).

1. Meld u weer aan bij de app Voorraadzichtbaarheid, ga naar de **configuratiepagina** en controleer vervolgens op het tabblad **Zachte reservering** de standaardhiërarchie voor zachte reservering. Voeg waar nodig nieuwe dimensies aan de hiërarchie toe.
1. Bekijk de standaardinstellingen in de sectie **Zachte reserveringstoewijzing instellen**. Standaard worden de zacht gereserveerde voorraadhoeveelheden geregistreerd op basis van de fysieke maateenheid `softreservephysical` van de gegevensbron `iv`. De berekende meting *Beschikbaar voor reservering* wordt toegewezen aan `availabletoreserve`. Als u de berekende meting `availabletoreserve` wilt bijwerken, gaat u naar de **configuratiepagina** en vouwt u op het tabblad **Berekende meting** de berekende meting uit en wijzigt u deze.

Zie [Voorraadzichtbaarheid configureren](inventory-visibility-configuration.md) voor meer informatie.

> [!NOTE]
> In de reserveringshiërarchie wordt de volgorde van dimensies beschreven die moeten worden opgegeven wanneer er reserveringen worden gemaakt. Deze werkt op dezelfde manier als de indexhiërarchie voor query's voor voorhanden voorraad, maar wordt onafhankelijk gebruikt, zodat gebruikers dimensiedetails kunnen opgeven om exactere reserveringen te maken.
>
> Uw zachte reserveringshiërarchie moet `SiteId` en `LocationId` als onderdelen bevatten, omdat ze de partitieconfiguratie vormen van Voorraadzichtbaarheid.

Zie [Reserveringsconfiguratie](inventory-visibility-configuration.md#reservation-configuration) voor meer informatie over het configureren van reserveringen.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>De reserveringsfunctie in Voorraadzichtbaarheid gebruiken

Wanneer u de reserverings-API oproept, markeert het systeem de reservering van de opgegeven goederen en hoeveelheden.

Hier is een voorbeeldscenario en een voorbeeld van een API-querytekst. Het bedrijf Contoso verkoopt product D0002 (Kast) via de e-commercewebsite. Een klant plaatst een verkooporder voor een kleine rode kast via de website. Contoso besluit deze order te vervullen met behulp van de volgende dimensies:

- Organisatie-id = usmf
- Site = 1
- Magazijn = 11
- Product = D0002
- Kleur = rood
- Formaat = klein

Contoso heeft al een API-verbinding met Voorraadzichtbaarheid ingesteld vanuit het eigen e-commercesysteem. Wanneer de order wordt ontvangen, activeert het systeem een API-aanroep om een zachte reservering te maken voor het artikel in Voorraadzichtbaarheid.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Zachte reserveringen maken met de reserverings-API

Reserveringen worden in de service voor Voorraadzichtbaarheid gemaakt door een aanvraag naar de URL van de service te verzenden, zoals `/api/environment/{environmentId}/onhand/reserve`.

Voor een reservering moet de hoofdtekst van de aanvraag een organisatie-ID, een product-ID, gereserveerde hoeveelheden en dimensies bevatten.

Wanneer u de reserverings-API aanroept, kunt u de reserveringsvalidatie beheren door de booleaanse parameter `ifCheckAvailForReserv` op te geven in de aanvraagbody. De waarde `True` betekent dat de validatie is vereist, terwijl de waarde `False` betekent dat de validatie niet is vereist. De standaardwaarde is `True`.

Als u een reservering wilt annuleren of de reservering van opgegeven voorraadhoeveelheden wilt verwijderen, stelt u de hoeveelheid in op een negatieve waarde en stelt u de parameter `ifCheckAvailForReserv` in op `False` om de validatie over te slaan.

Hier is een voorbeeld van de aanvraagbody die verwijst naar de verkooporder in de vorige context.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Een geslaagde aanvraag voor zachte reservering retourneert een *zachte reserverings-id* voor elke reserveringsrecord. De zachte reserverings-id is geen unieke id voor een afzonderlijke zachte reserveringsrecord, maar een combinatie van de product-id en dimensiewaarden die aan de zachte reserveringsaanvraag zijn gekoppeld. U kunt de zachte reserverings-id op de orderregel registreren wanneer u de gereserveerde orders synchroniseert met Supply Chain Management of een ander ERP-systeem om deze te verrekenen.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>Zachte reserveringen verrekenen in Supply Chain Management

U kunt een zacht gereserveerde hoeveelheid verrekenen nadat de hoeveelheid op een order fysiek is verminderd in Supply Chain Management of een ander ERP-systeem. Voorraadzichtbaarheid biedt een standaardintegratie voor verrekening van zachte reserveringen met Supply Chain Management.

Volg deze stappen om een zachte reservering te verrekenen.

1. Meld u aan bij Supply Chain Management.
1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Maak de externe verkooporder opnieuw en voeg een verkoopregel toe die dezelfde product-id, organisatie, locatie, magazijn en dimensiewaarden gebruikt.
1. Selecteer op het sneltabblad **Verkooporderregels** de zojuist ingevoerde verkoopregel, en vervolgens **Voorraad \> Reserverings-id** op de werkbalk.
1. Volg één van deze stappen:

    - Kopieer de zachte reserverings-id in het antwoord op de zachte reserveringsaanvraag en plak deze in het veld **Reserverings-id**.
    - Laat het veld **Reserverings-id** leeg, maar schakel het selectievakje **Automatisch verrekenen van voorraadservice** in. Op basis van de artikel-id en dimensiewaarden die op de geselecteerde regel zijn ingevoerd, wordt automatisch bepaald welke product- en productdimenssie er moeten worden verrekend.

1. Selecteer **OK**.
1. Maak met dezelfde orderregel nog geselecteerd een fysieke reservering van de bestelde hoeveelheid door op de werkbalk van het sneltabblad **Verkooporderregels** **Voorraad \> Reservering** te selecteren.
1. Als u het veld **Verschuivingsmodificator voor reservering** eerder hebt ingesteld op *Gereserveerd*, wordt de verrekening geactiveerd wanneer de orderregel de status *Fysiek reserveren* of *Besteld reserveren* heeft. Een batchtaak wordt eenmaal per minuut uitgevoerd om verrekenaanvragen van Supply Chain Management te synchroniseren met Voorraadzichtbaarheid.

> [!NOTE]
> Voor transactiestatussen die een gespecificeerde tegenreserveringsmodificator bevatten, verrekent de transactieupdate de bijbehorende reserveringsrecord als aan alle volgende voorwaarden voldaan is:
>
> - De reserverings-id van de voorraadtransactie komt overeen met de reserverings-id van de reserveringsrecord in de service voor Voorraadzichtbaarheid.
> - De dimensies van de voorraadtransactie komen overeen met de dimensies van de reserveringsrecord in de service voor Voorraadzichtbaarheid.
> - Wijzigingen in de status van de voorraadtransactie zorgen voor tegenreserveringen wanneer de voorraadtransactiestatus uitwijst dat een orderproces voltooid of overgeslagen is.

De verrekenhoeveelheden volgen de voorraadhoeveelheden die in de relevante voorraadtransacties zijn opgegeven. Een verrekening wordt alleen uitgevoerd als er gereserveerde hoeveelheid in Voorraadzichtbaarheid overblijft.

### <a name="cancel-or-revert-a-soft-reservation"></a>Een zachte reservering annuleren of terugdraaien

Als een oorspronkelijke orderregel wordt geannuleerd of verwijderd en u de bijbehorende zachte reservering moet terugdraaien, boekt u een negatieve hoeveelheid met exact dezelfde informatie in uw API-querybody.
