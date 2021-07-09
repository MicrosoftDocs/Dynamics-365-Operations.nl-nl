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
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="61fdf-103">Inkomende ASN's importeren via de V2-gegevensentiteit</span><span class="sxs-lookup"><span data-stu-id="61fdf-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61fdf-104">ASN's brengen u op de hoogte over leveringen van leveranciers.</span><span class="sxs-lookup"><span data-stu-id="61fdf-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="61fdf-105">Met behulp van deze informatie kan de afzender de inhoud van een zending en aanvullende informatie over de zending beschrijven, zoals de artikelen en de verpakking.</span><span class="sxs-lookup"><span data-stu-id="61fdf-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="61fdf-106">Met ASN's kunnen magazijnmedewerkers weten wat er arriveert en wanneer.</span><span class="sxs-lookup"><span data-stu-id="61fdf-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="61fdf-107">Dan kunnen ze zich dus voorbereiden.</span><span class="sxs-lookup"><span data-stu-id="61fdf-107">Therefore, they can prepare.</span></span> <span data-ttu-id="61fdf-108">Daarnaast kunnen magazijnmedewerkers ASN's gebruiken om de details van een zending te vergelijken met de gerelateerde inkooporder die eerder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="61fdf-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="61fdf-109">Dit onderwerp bevat een verzameling scenario's met voorbeelden voor hoe u met ASN-bestanden kunt werken.</span><span class="sxs-lookup"><span data-stu-id="61fdf-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61fdf-110">Importeren van *Inkomende ASN* is alleen van toepassing op artikelen die zijn ingeschakeld voor WMS (Advanced Magazijn Management).</span><span class="sxs-lookup"><span data-stu-id="61fdf-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="61fdf-111">Voordat u een ASN ontvangt, moet er een inkooporder in het systeem zijn geregistreerd voor de leverancier die de ASN verstuurt.</span><span class="sxs-lookup"><span data-stu-id="61fdf-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="61fdf-112">Inkomende ASN V2-entiteit</span><span class="sxs-lookup"><span data-stu-id="61fdf-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="61fdf-113">U importeert inkomende ASN's met de samengestelde gegevensentiteit *Inbound ASN V2*.</span><span class="sxs-lookup"><span data-stu-id="61fdf-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="61fdf-114">*Inkomende ASN V2* maakt gebruik van de volgende entiteiten:</span><span class="sxs-lookup"><span data-stu-id="61fdf-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="61fdf-115">Inkomende ladingskoptekst</span><span class="sxs-lookup"><span data-stu-id="61fdf-115">Inbound load header</span></span>
- <span data-ttu-id="61fdf-116">Koptekst van binnenkomende zending</span><span class="sxs-lookup"><span data-stu-id="61fdf-116">Inbound shipment header</span></span>
- <span data-ttu-id="61fdf-117">Verpakkingsstructuren van binnenkomende lading</span><span class="sxs-lookup"><span data-stu-id="61fdf-117">Inbound load packing structures</span></span>
- <span data-ttu-id="61fdf-118">Verpakkingsstructuurcases van binnenkomende lading</span><span class="sxs-lookup"><span data-stu-id="61fdf-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="61fdf-119">Verpakkingsstructuurcaselijnen van binnenkomende lading</span><span class="sxs-lookup"><span data-stu-id="61fdf-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="61fdf-120">Verpakkingsstructuurlijnen van binnenkomende lading</span><span class="sxs-lookup"><span data-stu-id="61fdf-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="61fdf-121">De samengestelde gegevensentiteit *Inbound ASN V2* is bedoeld voor asynchrone integratiescenario's waarbij importen op basis van XML-bestanden worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="61fdf-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="61fdf-122">XML-indeling voor het importeren van ASN's</span><span class="sxs-lookup"><span data-stu-id="61fdf-122">XML format for importing ASNs</span></span>

<span data-ttu-id="61fdf-123">Microsoft Dynamics 365 Supply Chain Management ondersteunt de volgende XML-indeling voor het importeren van ASN's.</span><span class="sxs-lookup"><span data-stu-id="61fdf-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="61fdf-124">Elk knooppunt in het XML-bestand vertegenwoordigt een kenmerk van een afzonderlijke entiteit.</span><span class="sxs-lookup"><span data-stu-id="61fdf-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

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

## <a name="examples"></a><span data-ttu-id="61fdf-125">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="61fdf-125">Examples</span></span>

<span data-ttu-id="61fdf-126">De volgende subsecties bieden voorbeelden van ASN XML-importbestanden voor leverancierszendingen.</span><span class="sxs-lookup"><span data-stu-id="61fdf-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="61fdf-127">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="61fdf-127">Example 1</span></span>

<span data-ttu-id="61fdf-128">Het volgende voorbeeld toont een XML-bestand voor het importeren van leverancierszendingen voor één inkooporder als er geen aanvraagdetails zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="61fdf-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

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

### <a name="example-2"></a><span data-ttu-id="61fdf-129">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="61fdf-129">Example 2</span></span>

<span data-ttu-id="61fdf-130">Het volgende voorbeeld toont een XML-bestand voor het importeren van leverancierszendingen voor één inkooporder als er aanvraagdetails zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="61fdf-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

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

### <a name="example-3"></a><span data-ttu-id="61fdf-131">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="61fdf-131">Example 3</span></span>

<span data-ttu-id="61fdf-132">Het volgende voorbeeld toont een XML-bestand voor het importeren van leverancierszendingen voor meerdere inkooporders als er aanvraagdetails zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="61fdf-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

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

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="61fdf-133">Controle van het resultaat na het importeren van een ASN-bestand</span><span class="sxs-lookup"><span data-stu-id="61fdf-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="61fdf-134">Volg deze stappen om het resultaat na het importeren van een ASN-bestand te controleren.</span><span class="sxs-lookup"><span data-stu-id="61fdf-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="61fdf-135">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="61fdf-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="61fdf-136">Een lading zoeken en openen die is gemaakt als onderdeel van een ASN-import.</span><span class="sxs-lookup"><span data-stu-id="61fdf-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="61fdf-137">Op het sneltab tabblad **Laden** ziet u waarden die zijn gebaseerd op het XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="61fdf-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="61fdf-138">Op het sneltabblad **Ladingsregels** ziet u inkoopordernummers en artikeldetails die zijn gebaseerd op het XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="61fdf-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="61fdf-139">Selecteer in het actievenster, op het tabblad **Verzenden en ontvangen**, in de groep **Ontvangen** de optie **Verpakkingsstructuur** om de verpakkingsstructuur van de lading te controleren.</span><span class="sxs-lookup"><span data-stu-id="61fdf-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="61fdf-140">Op het sneltab tabblad **Pallets** ziet u nummerplaten die zijn gebaseerd op het XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="61fdf-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="61fdf-141">Op het sneltab tabblad **Aanvragen** ziet u aanvragen die zijn gebaseerd op het XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="61fdf-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="61fdf-142">Op het sneltab tabblad **Artikelen** ziet u artikelen en hoeveelheden die zijn gebaseerd op het XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="61fdf-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
