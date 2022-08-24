---
title: API's voor commerce-prijzen
description: In dit artikel worden verschillende API's voor prijzen beschreven die worden geleverd door de prijzen-engine van Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294110"
---
# <a name="commerce-pricing-apis"></a>API's voor commerce-prijzen

[!include [banner](../includes/banner.md)]

In dit artikel worden verschillende API's voor prijzen beschreven die worden geleverd door de prijzen-engine van Microsoft Dynamics 365 Commerce.

De prijzenengine van Dynamics 365 Commerce biedt de volgende Retail Server-API's die kunnen worden gebruikt door externe toepassingen om verschillende prijsscenario's te ondersteunen:

- **GetActivePrices**: deze API haalt de berekende prijs van een product op, inclusief eenvoudige kortingen.
- **CalculateSalesDocument**: deze API berekent prijzen en kortingen voor producten bij bepaalde hoeveelheden als ze samen worden gekocht.
- **GetAvailablePromotions**: deze API haalt toepasselijke kortingen op voor producten in de winkelwagen. 
- **AddCoupons**: deze API voegt coupons toe aan een winkelwagen.
- **RemoveCoupons**: deze API verwijdert coupons uit een winkelwagen.

Raadpleeg [Retail Server-API's verbruiken in externe toepassingen](dev-itpro/consume-retail-server-api.md) voor meer informatie over het verbruik van Retail Server-API's in externe toepassingen.

## <a name="getactiveprices"></a>GetActivePrices

De API *GetActivePrices* is geïntroduceerd in de release van Commerce versie 10.0.4. Deze API haalt de berekende prijs van een product op, inclusief eenvoudige kortingen. De API berekent geen meerregelkortingen en er wordt aangenomen dat elk product in een API-aanvraag een hoeveelheid van 1 heeft. Deze API kan ook een lijst met producten als invoer gebruiken en de prijs van afzonderlijke producten in bulk opvragen.

De API *GetActivePrices* ondersteunt de Commerce-rollen **Werknemer**, **Klant**, **Anoniem** en **Toepassing**.

De belangrijkste use case voor de API *GetActivePrices* is de pagina met productgegevens (PDP), waar detailhandelaren de beste prijs voor een product willen presenteren, inclusief eventuele geldende kortingen.

De volgende tabel toont de invoerparameters voor de API *GetActivePrices*.

| Name                                    | Subnaam | Type | Vereist/optioneel | Description |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Vereist | |
|                                         | ChannelId | long | Vereist | |
|                                         | CatalogId | long | Vereist | |
| productIds                              | | IEnumerable\<long\> | Vereist | De lijst met producten om prijzen voor te berekenen. |
| activeDate                              | | DateTimeOffset | Vereist | De datum waarop de prijzen worden berekend. |
| customerId                              | | tekenreeks | Optioneel | Het rekeningnummer van de klant. |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | Optioneel | De aansluitings- en loyaliteitsniveaus. |
|                                         | AffiliationId | long | Vereist | ID van de aansluiting. |
|                                         | LoyaltyTierId | long | Optioneel | De ID van het loyaliteitsniveau. |
| includeSimpleDiscountsInContextualPrice | | bool | Optioneel | Stel deze parameter in op **waar** om eenvoudige kortingen in de prijsberekening op te nemen. De standaardwaarde is **onwaar**. |
| includeVariantPriceRange                | | bool | Optioneel | Stel deze parameter in op **waar** om de minimum- en maximumprijzen op te halen van alle varianten voor een hoofdproduct. De standaardwaarde is **onwaar**. |
| includeAttainablePricesAndDiscounts     | | bool | Optioneel | Stel deze parameter in op **waar** om haalbare prijzen en kortingen op te halen. De standaardwaarde is **onwaar**. |

**Tekst van voorbeeldaanvraag**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Tekst voorbeeldrespons**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

De API *CalculateSalesDocument* is geïntroduceerd in de release van Commerce versie 10.0.25. Deze API berekent prijzen en kortingen voor producten bij bepaalde hoeveelheden als ze in een order samen worden gekocht. Bij de prijsberekening achter de API *CalculateSalesDocument* worden zowel kortingen voor één regel als kortingen voor meerdere regels meegenomen.

De belangrijkste use case voor de API *CalculateSalesDocument* is de prijsberekening in scenario's waarin volledige winkelwagencontext niet voortduurt (zoals verkoopoffertes). Scenario's in POS- en e-commerce van Commerce kunnen ook profiteren van deze use case. Een lagere totaalprijs wanneer winkelwagenartikelen worden berekend als een set (bijvoorbeeld voor discrete bundels, gekoppelde of aanbevolen producten of producten die al aan de winkelwagen zijn toegevoegd) kunnen klanten ertoe brengen producten aan de winkelwagen toe te voegen.

Het gegevensmodel voor zowel de aanvraag als het antwoord van de API *CalculateSalesDocument* is **Winkelwagen**. In de context van deze API heeft het gegevensmodel echter de naam **SalesDocument**. Aangezien de meeste eigenschappen optioneel zijn en slechts een paar van deze van invloed zijn op de prijsberekening, worden in de volgende tabel alleen prijsgerelateerde velden weergegeven. Het wordt niet aanbevolen om andere velden te gebruiken voor de API-aanvraag.

Het bereik van de API *CalculateSalesDocument* is alleen de berekening van prijzen en kortingen. Belastingen en toeslagen worden niet meegenomen.

De volgende tabel toont de invoerparameters in het object met de naam **salesDocument**.

| Name             | Subnaam | Type | Vereist/optioneel | Description |
|------------------|----------|------|-------------------|-------------|
| Id               | | tekenreeks | Vereist | De ID van het verkoopdocument. |
| CartLines        | | IList\<CartLine\> | Optioneel | De lijst met regels om prijzen en kortingen voor te berekenen. |
|                  | Product-id | long | Vereist in het bereik van CartLine | De record-ID van het product. |
|                  | ItemId | tekenreeks | Optioneel | De artikel-ID. Als er een waarde is opgegeven, moet deze overeenkomen met de waarde van de parameter **ProductId**. |
|                  | InventoryDimensionId | tekenreeks | Optioneel | De ID van de voorraaddimensie. Als er een waarde is opgegeven, moet de combinatie van de waarden van **ItemId** en **InventoryDimensionId** overeenkomen met de waarde van de parameter **ProductId**. |
|                  | Quantity | decimal | Vereist in het bereik van CartLine | De hoeveelheid van het product. |
|                  | UnitOfMeasureSymbol | tekenreeks | Optioneel | De eenheid van het product. Als er geen waarde is opgegeven, gebruikt de API standaard de verkoopeenheid van het product. |
| CustomerId       | | tekenreeks | Optioneel | Het rekeningnummer van de klant. |
| LoyaltyCardId    | | tekenreeks | Optioneel | De ID van de loyaliteitskaart. Een klantaccount dat aan de loyaliteitskaart is gekoppeld, moet overeenkomen met de waarde van de parameter **CustomerId** (als deze is opgegeven). Er wordt geen rekening gehouden met de loyaliteitskaart als deze niet wordt gevonden of als de status **geblokkeerd** is. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | Optioneel | Regels loyaliteitsniveau aansluiting. Als de waarde(n) voor **CustomerId** en/of **LoyaltyCardId** zijn opgegeven, worden de bijbehorende regels van het loyaliteitsniveau samengevoegd met de regels die zijn opgegeven in de waarde **AffiliationLines**. |
|                  | AffiliationId | long | Vereist in het bereik van AffiliationLoyaltyTier | De record-ID van de aansluiting. |
|                  | LoyaltyTierId | long | Vereist in het bereik van AffiliationLoyaltyTier | De record-ID van het loyaliteitsniveau. |
|                  | AffiliationTypeValue | int | Vereist in het bereik van AffiliationLoyaltyTier | Een waarde die aangeeft of de aansluitingsregel van het type **Algemeen** (**0**) of het type **Loyaliteit** (**1**) is. Als deze parameter is ingesteld op **0**, gebruikt de API de waarde van **AffiliationId** als de ID en wordt de waarde voor **LoyaltyTierId** genegeerd. Als de parameter is ingesteld op **1**, gebruikt de API de waarde van **LoyaltyTierId** als de ID en wordt de waarde voor **AffiliationId** genegeerd. |
|                  | ReasonCodeLines | Collectie\<ReasonCodeLine\> | Vereist in het bereik van AffiliationLoyaltyTier | Redencoderegels. Deze parameter heeft geen effect op de prijsberekening, maar is vereist als onderdeel van het object **AffiliationLoyaltyTier**. |
|                  | CustomerId | tekenreeks | Vereist in het bereik van AffiliationLoyaltyTier | Het rekeningnummer van de klant. |
| Coupons          | | IList\<Coupon\> | Optioneel | Coupons die niet van toepassing zijn (inactief, vervallen of niet zijn gevonden) worden niet meegenomen in de prijsberekening. |
|                  | Code | tekenreeks | Vereist in het bereik van Coupon | De couponcode. |
|                  | CodeId | tekenreeks | Optioneel | De couponcode-ID. Als er een waarde is opgegeven, moet deze overeenkomen met de waarde van de parameter **Code**. |
|                  | DiscountOfferId | tekenreeks | Optioneel | De korting-ID. Als er een waarde is opgegeven, moet deze overeenkomen met de waarde van de parameter **Code**. |

**Tekst van voorbeeldaanvraag**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Het gehele winkelwagenobject wordt als tekst van de respons geretourneerd. Als u prijzen en kortingen wilt controleren, moet u zich richten op de velden in de volgende tabel.

| Name           | Subnaam | Type | Description |
|----------------|----------|------|--------------|
| NetPrice       | | decimal | De nettoprijs van het hele verkoopdocument voordat kortingen zijn toegepast. |
| DiscountAmount | | decimal | Het totaalbedrag van de kortingen van het hele verkoopdocument. |
| TotalAmount    | | decimal | Het totaalbedrag van het hele verkoopdocument. |
| CartLines      | | IList\<CartLine\> | Berekende regels die gegevens over prijs en korting bevatten. |
|                | Prijs | decimal | De eenheidsprijs van het product. |
|                | NetPrice | decimal | De nettoprijs van de regel voordat kortingen zijn toegepast (= *Prijs* &times; *Hoeveelheid*). |
|                | DiscountAmount | decimal | Het kortingsbedrag. |
|                | TotalAmount | decimal | Het uiteindelijke totale prijsresultaat van de regel. |
|                | PriceLines | IList\<PriceLine\> | Prijsgegevens, inclusief de bron van de prijs (basisprijs, prijscorrectie of handelsovereenkomst) en het bedrag. |
|                | DiscountLines | IList\<DiscountLine\> | Kortingsgegevens. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Met als gegeven een winkelwagen met meerdere winkelwagenregels, retourneert de API *GetAvailablePromotions* alle van toepassing zijnde kortingen voor de winkelwagenregels. 

De belangrijkste use case voor de API *GetAvailablePromotions* is de winkelwagenpagina, waar detailhandelaren toegepaste kortingen of beschikbare coupons voor de huidige winkelwagentje willen presenteren.

De volgende tabel toont de invoerparameters voor de API *GetAvailablePromotions*.

| Name        | Type | Vereist/optioneel | Description |
|-------------|------|-------------------|-------------|
| sleutel         | tekenreeks | Vereist | De winkelwagen-ID. |
| cartLineIds | IEnumerable\<string\> | Optioneel | Stel deze parameter in om alleen kortingen voor geselecteerde winkelwagenregels te retourneren. |

**Tekst voorbeeldrespons**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

De API *AddCoupons* ondersteunt het toevoegen van een lijst met coupons aan een winkelwagen. Deze API retourneert het winkelwagenobject nadat de coupons zijn toegevoegd.

De volgende tabel toont de invoerparameters voor de API *AddCoupons*.

| Name                 | Type | Vereist/optioneel | Description |
|----------------------|------|-------------------|-------------|
| sleutel                  | tekenreeks | Vereist | De winkelwagen-ID. |
| couponCodes          | IEnumerable\<string\> | Vereist | De aan de winkelwagen toe te voegen couponcodes. |
| isLegacyDiscountCode | bool | Optioneel | Stel deze parameter in op **waar** om aan te geven dat de coupon een verouderde kortingscode is. De standaardwaarde is **onwaar**. |

## <a name="removecoupons"></a>RemoveCoupons

De API *RemoveCoupons* ondersteunt het verwijderen van een lijst met coupons uit een winkelwagen. Deze API retourneert het winkelwagenobject nadat de coupons zijn verwijderd.

De volgende tabel toont de invoerparameters voor de API *RemoveCoupons*.

| Name        | Type | Vereist/optioneel | Description |
|-------------|------|-------------------|-------------|
| sleutel         | tekenreeks | Vereist | De winkelwagen-ID. |
| couponCodes | IEnumerable\<string\> | Vereist | De uit de winkelwagen te verwijderen couponcodes. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
