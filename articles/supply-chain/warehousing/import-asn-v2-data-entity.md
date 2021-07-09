---
title: Inkomende ASN's importeren via de V2-gegevensentiteit
description: In dit onderwerp wordt uitgelegd hoe u het importeren van inkomende geavanceerde vervoerders meldingen (ASN's) via de inkomende ASN V2-gegevensentiteit beheert.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249081"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a>Inkomende ASN's importeren via de V2-gegevensentiteit

[!include [banner](../../includes/banner.md)]

ASN's brengen u op de hoogte over leveringen van leveranciers. Met behulp van deze informatie kan de afzender de inhoud van een zending en aanvullende informatie over de zending beschrijven, zoals de artikelen en de verpakking.

Met ASN's kunnen magazijnmedewerkers weten wat er arriveert en wanneer. Dan kunnen ze zich dus voorbereiden. Daarnaast kunnen magazijnmedewerkers ASN's gebruiken om de details van een zending te vergelijken met de gerelateerde inkooporder die eerder is gemaakt.

Dit onderwerp bevat een verzameling scenario's met voorbeelden voor hoe u met ASN-bestanden kunt werken.

> [!IMPORTANT]
> Importeren van *Inkomende ASN* is alleen van toepassing op artikelen die zijn ingeschakeld voor WMS (Advanced Magazijn Management). Voordat u een ASN ontvangt, moet er een inkooporder in het systeem zijn geregistreerd voor de leverancier die de ASN verstuurt.

## <a name="inbound-asn-v2-entity"></a>Inkomende ASN V2-entiteit

U importeert inkomende ASN's met de samengestelde gegevensentiteit *Inbound ASN V2*. *Inkomende ASN V2* maakt gebruik van de volgende entiteiten:

- Inkomende ladingskoptekst
- Koptekst van binnenkomende zending
- Verpakkingsstructuren van binnenkomende lading
- Verpakkingsstructuurcases van binnenkomende lading
- Verpakkingsstructuurcaselijnen van binnenkomende lading
- Verpakkingsstructuurlijnen van binnenkomende lading

De samengestelde gegevensentiteit *Inbound ASN V2* is bedoeld voor asynchrone integratiescenario's waarbij importen op basis van XML-bestanden worden gebruikt.

## <a name="xml-format-for-importing-asns"></a>XML-indeling voor het importeren van ASN's

Microsoft Dynamics 365 Supply Chain Management ondersteunt de volgende XML-indeling voor het importeren van ASN's. Elk knooppunt in het XML-bestand vertegenwoordigt een kenmerk van een afzonderlijke entiteit.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Voorbeelden

De volgende subsecties bieden voorbeelden van ASN XML-importbestanden voor leverancierszendingen.

### <a name="example-1"></a>Voorbeeld 1

Het volgende voorbeeld toont een XML-bestand voor het importeren van leverancierszendingen voor één inkooporder als er geen aanvraagdetails zijn opgenomen.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>Voorbeeld 2

Het volgende voorbeeld toont een XML-bestand voor het importeren van leverancierszendingen voor één inkooporder als er aanvraagdetails zijn opgenomen.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>Voorbeeld 3

Het volgende voorbeeld toont een XML-bestand voor het importeren van leverancierszendingen voor meerdere inkooporders als er aanvraagdetails zijn opgenomen.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>Controle van het resultaat na het importeren van een ASN-bestand

Volg deze stappen om het resultaat na het importeren van een ASN-bestand te controleren.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Een lading zoeken en openen die is gemaakt als onderdeel van een ASN-import.
1. Op het sneltab tabblad **Laden** ziet u waarden die zijn gebaseerd op het XML-bestand.
1. Op het sneltabblad **Ladingsregels** ziet u inkoopordernummers en artikeldetails die zijn gebaseerd op het XML-bestand.
1. Selecteer in het actievenster, op het tabblad **Verzenden en ontvangen**, in de groep **Ontvangen** de optie **Verpakkingsstructuur** om de verpakkingsstructuur van de lading te controleren.
1. Op het sneltab tabblad **Pallets** ziet u nummerplaten die zijn gebaseerd op het XML-bestand.
1. Op het sneltab tabblad **Aanvragen** ziet u aanvragen die zijn gebaseerd op het XML-bestand.
1. Op het sneltab tabblad **Artikelen** ziet u artikelen en hoeveelheden die zijn gebaseerd op het XML-bestand.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
