---
title: Zendingen consolideren met vrijgave naar magazijn vanuit de workbench voor ladingplanning
description: Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde lading en vervolgens automatisch worden geconsolideerd in zendingen.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 30824bf1c8e84bab08b6885ee812ed5e3e9937bb
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117176"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a>Zendingen consolideren met vrijgave naar magazijn vanuit de workbench voor ladingplanning

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde lading en vervolgens automatisch worden geconsolideerd in zendingen.

## <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Consolidatiebeleid voor zendingen en productfilters instellen

In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven. Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.

## <a name="create-the-sales-orders-for-this-scenario"></a>De verkooporders voor dit scenario maken

Maak eerst een verzameling verkooporders waarmee u kunt werken. U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS). Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.

Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.

### <a name="create-order-set-1"></a>Orderset 1 maken

#### <a name="sales-order-1-1"></a>Verkooporder 1-1

1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Leveringsmethode:** *Airwa-Air*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

#### <a name="sales-order-1-2"></a>Verkooporder 1-2

1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Leveringsmethode:** *Airwa-Air*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

#### <a name="sales-order-1-3"></a>Verkooporder 1-3

1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Leveringsmethode:** *10*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.
1. Voeg een tweede orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0002* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*
    - **Leveringsmethode:** *Airwa-Air*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.

### <a name="create-order-set-2"></a>Orderset 2 maken

#### <a name="sales-orders-2-1-and-2-2"></a>Verkooporders 2-1 en 2-2

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-002*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.
1. Voeg een tweede orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)
    - **Hoeveelheid:** *1.00*
    - **Leveringsmethode:** *Airwa-Air*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de tweede orderregel te reserveren.

### <a name="create-order-set-3"></a>Orderset 3 maken

#### <a name="sales-orders-3-1-and-3-2"></a>Verkooporders 3-1 en 3-2

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Bestelopdracht van klant:** *1*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

#### <a name="sales-orders-3-3-and-3-4"></a>Verkooporders 3-3 en 3-4

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Bestelopdracht van klant:** *2*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

### <a name="create-order-set-4"></a>Orderset 4 maken

#### <a name="sales-orders-4-1-and-4-2"></a>Verkooporders 4-1 en 4-2

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-003*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

#### <a name="sales-orders-4-3-and-4-4"></a>Verkooporders 4-3 en 4-4

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-004*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

#### <a name="sales-orders-4-5-and-4-6"></a>Verkooporders 4-5 en 4-6

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-007*
    - **Locatie:** *6*
    - **Magazijn:** *61*
    - **Groep:** *ShipCons*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

#### <a name="sales-orders-4-7-and-4-8"></a>Verkooporders 4-7 en 4-8

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-007*
    - **Locatie:** *6*
    - **Magazijn:** *61*
    - **Groep:** laat dit veld leeg.

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>De workbench voor ladingplanning gebruiken om ladingen te maken en deze vrij te geven naar het magazijn

Voer de volgende stappen uit om een lading te maken voor elke orderset die u voor dit scenario hebt gemaakt en deze vervolgens vrij te geven naar het magazijn.

1. Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.
1. Op het tabblad **Verkoopregels** zoekt en selecteert u alle verkooporderregels uit een van de ordersets die u voor dit scenario hebt gemaakt.
1. Selecteer in het actievenster op het tabblad **Vraag en aanbod** de optie **Toevoegen \> Aan nieuwe lading** om de geselecteerde orderregels aan een nieuwe lading toe te voegen.
1. Selecteer in het dialoogvenster **Ladingsjabloon toewijzen** in het veld **Ladingsjabloon-id** een ladingssjabloon, zoals *Standaardladingssjabloon*.
1. Selecteer **OK** om het dialoogvenster te sluiten. 
1. In de sectie **Ladingen** zoekt en selecteert u de lading die u net hebt gemaakt.
1. Selecteer **Vrijgeven \>Vrijgave naar magazijn** om de geselecteerde lading vrij te geven naar het magazijn.
1. Herhaal deze procedure voor de drie overige ordersets die u voor dit scenario hebt gemaakt.

## <a name="verify-the-shipments"></a>De zendingen verifiëren

Met de volgende procedure kunt u de zendingen controleren die zijn gemaakt of bijgewerkt als gevolg van een zendingsconsolidatie. Gebruik deze om alle ordersets te controleren die u voor dit scenario hebt gemaakt en bekijk vervolgens de subsecties die volgen om te controleren of u de verwachte resultaten hebt verkregen.

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Zoek en selecteer de vereiste zending.
1. Als een consolidatiebeleid is gebruikt bij het maken of bijwerken van de zending, wordt dit weergegeven in het veld **Consolidatiebeleid voor zendingen**.

### <a name="release-order-set-1-in-one-load"></a>Orderset 1 vrijgeven in één lading

Er moeten twee zendingen zijn gemaakt:

- De eerste zending bevat drie regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerMode*.
- De tweede zending, die geen gebruikmaakt van de leveringsmethode *Airways*, is gemaakt met het consolidatiebeleid voor zending *CustomerOrderNo*.

### <a name="release-order-set-2-in-one-load"></a>Orderset 2 vrijgeven in één lading

Er moeten drie zendingen zijn gemaakt:

- De eerste zending bevat de items van het type *Ontvlambaar*.
- Elk van de twee overige zendingen bevat één regel met het item *Explosief*.

### <a name="release-order-set-3-in-one-load"></a>Orderset 3 vrijgeven in één lading

Er moeten twee zendingen zijn gemaakt:

- De eerste zending bevat orderregels uit de verkooporder waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*.
- De tweede zending bevat orderregels uit verkooporders waarvoor het veld **Bestelopdracht van klant** is ingesteld op *2*.

### <a name="release-order-set-4-in-one-load"></a>Orderset 4 vrijgeven in één lading

Er moeten vier zendingen zijn gemaakt:

- Regels van twee orders voor klantrekening *US-003* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van twee orders voor klantrekening *US-004* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van verkooporders 4-5 en 4-6 voor klantrekening *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van verkooporders 4-7 en 4-8 voor klantrekening *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *CrossOrder*.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Beleidsregels voor consolidatie van zendingen](about-shipment-consolidation-policies.md)
- [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]