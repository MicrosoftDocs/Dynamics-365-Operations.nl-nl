---
title: Zendingen consolideren wanneer deze naar het magazijn worden vrijgegeven met Automatische vrijgave van verkooporders
description: Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde geautomatiseerde procedure voor het periodiek vrijgeven naar een magazijn.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 376c7418b61c0192f9071a879b50b9ece7699894
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970351"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a>Zendingen consolideren wanneer deze naar het magazijn worden vrijgegeven met Automatische vrijgave van verkooporders

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven in dezelfde geautomatiseerde procedure voor het periodiek vrijgeven naar een magazijn. De orders worden automatisch geconsolideerd in zendingen op basis van regels die zijn gedefinieerd als consolidatiebeleid voor zendingen.

Tijdens het scenario maakt u sets verkooporders en geeft u elke set vrij naar het magazijn. U gaat vervolgens de zendingen bekijken die worden gemaakt of bijgewerkt tijdens de consolidatie van de zending, op basis van het geconfigureerde beleid.

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

#### <a name="sales-order-1-2"></a>Verkooporder 1-2

1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Leveringsmethode:** *Airwa-Air*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

#### <a name="sales-order-1-3"></a>Verkooporder 1-3

1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Leveringsmethode:** *10*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Voeg een tweede orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0002* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*
    - **Leveringsmethode:** *Airwa-Air*

### <a name="create-order-set-2"></a>Orderset 2 maken

#### <a name="sales-orders-2-1-and-2-2"></a>Verkooporders 2-1 en 2-2

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-002*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)
    - **Hoeveelheid:** *1.00*

1. Voeg een tweede orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)
    - **Hoeveelheid:** *1.00*
    - **Leveringsmethode:** *Airwa-Air*

### <a name="create-order-set-3"></a>Orderset 3 maken

#### <a name="sales-order-3-1"></a>Verkooporder 3-1

1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-002*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *M9200* (een artikel waarvoor het filter **Code 4** op *Ontvlambaar* is ingesteld)
    - **Hoeveelheid:** *1.00*

1. Voeg een tweede orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *M9201* (een artikel waarvoor het filter **Code 4** op *Explosief* is ingesteld)
    - **Hoeveelheid:** *1.00*
    - **Leveringsmethode:** *Airwa-Air*

> [!NOTE]
> Deze order is gelijk aan de twee orders die u hebt gemaakt voor orderset 2. Deze wordt echter weergegeven als een eigen order omdat u deze later in dit scenario afzonderlijk vrijgeeft.

### <a name="create-order-set-4"></a>Orderset 4 maken

#### <a name="sales-order-4-1"></a>Verkooporder 4-1

1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Bestelopdracht van klant:** *1*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

### <a name="create-order-set-5"></a>Orderset 5 maken

#### <a name="sales-orders-5-1-and-5-2"></a>Verkooporders 5-1 en 5-2

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Bestelopdracht van klant:** *2*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

#### <a name="sales-order-5-3"></a>Verkooporder 5-3

1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Bestelopdracht van klant:** *1*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

### <a name="create-order-set-6"></a>Orderset 6 maken

#### <a name="sales-orders-6-1-and-6-2"></a>Verkooporders 6-1 en 6-2

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-003*
    - **Bestelopdracht van klant:** *2*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Verkooporders 6-3 en 6-4

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-004*
    - **Bestelopdracht van klant:** *1*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Verkooporders 6-5 en 6-6

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-007*
    - **Locatie:** *6*
    - **Magazijn:** *61*
    - **Groep:** *ShipCons*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Verkooporders 6-7 en 6-8

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-007*
    - **Locatie:** *6*
    - **Magazijn:** *61*
    - **Groep:** laat dit veld leeg.

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Automatische vrijgave van verkooporders naar het magazijn

Voor elke set verkooporders die u eerder hebt gemaakt, voltooit u een procedure voor het automatisch vrijgeven naar het magazijn. In beide gevallen doorloopt u de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) die hier wordt beschreven.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Basisprocedure voor vrijgave naar het magazijn

Voor elke set verkooporders die u eerder hebt gemaakt, voert u de drie procedures uit die in de volgende subsecties worden beschreven.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>De wave-sjabloon bijwerken die tijdens de vrijgave wordt gebruikt

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Stel het veld **Type wavesjabloon** in op *Verzenden*.
1. Zoek en selecteer de wavesjabloon die is gekoppeld aan het magazijn dat u hebt gebruikt in de ordersets die u voor dit scenario hebt gemaakt. Als u bijvoorbeeld magazijn *24* hebt gebruikt , selecteert u de wavesjabloon **24 Standaardverzending**. Als u magazijn *61* hebt gebruikt, selecteert u de wavesjabloon **61 Verzending**.
1. Selecteer **Bewerken** in het actievenster.
1. Stel de optie **Wave verwerken bij vrijgave door magazijn** in op *Nee*.

#### <a name="release-to-the-warehouse"></a>Vrijgave naar het magazijn

1. Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Automatische vrijgave van verkooporders**.
1. Stel het veld **Hoeveelheid voor vrijgave** in op *Alle*.
1. Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** om het querydialoogvenster te openen.
1. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een rij met de volgende instellingen aan het raster toe te voegen:

    - **Tabel:** *Verkooporder*
    - **Afgeleide tabel:** *Verkooporder*
    - **Veld:** *Verkooporder*
    - **Criteria:** voer een door komma's gescheiden lijst in van de verkoopordernummers uit de gewenste orderset.

1. Selecteer **OK** om uw query op te slaan.
1. Selecteer **OK** om de procedure *Automatische vrijgave naar magazijn* te starten.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>De zending controleren die is gemaakt of bijgewerkt

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Zoek en selecteer de vereiste zending.
1. Als een consolidatiebeleid is gebruikt bij het maken of bijwerken van de zending, wordt dit weergegeven in het veld **Consolidatiebeleid voor zendingen**.

### <a name="release-sales-orders-from-order-set-1"></a>Verkooporders vrijgeven vanuit orderset 1

Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 1 vrij te geven.

Wanneer u klaar bent, ziet u dat er twee zendingen zijn gemaakt:

- De eerste zending bevat drie regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerMode*.
- De tweede zending, die geen gebruikmaakt van de leveringsmethode *Airways*, is gemaakt met het consolidatiebeleid voor zending *CustomerOrderNo*.

### <a name="release-sales-orders-from-order-set-2"></a>Verkooporders vrijgeven vanuit orderset 2

Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 2 vrij te geven.

Wanneer u klaar bent, ziet u dat er drie zendingen zijn gemaakt:

- De eerste zending bevat items van het type *Ontvlambaar*.
- Elk van de twee overige zendingen bevat één regel met het item *Explosief*.

### <a name="release-sales-orders-from-order-set-3"></a>Verkooporders vrijgeven vanuit orderset 3

Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 3 vrij te geven.

Wanneer u klaar bent, ziet u dat de volgende acties zijn uitgevoerd:

- Eén bestaande zending (de zending die is gemaakt toen orderset 2 is vrijgegeven naar het magazijn) is bijgewerkt. Er is een regel toegevoegd waaraan het item *Ontvlambaar* is toegevoegd.
- Er is één nieuwe zending gemaakt die het item *Explosief* bevat.

### <a name="release-sales-orders-from-order-set-4"></a>Verkooporders vrijgeven vanuit orderset 4

Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 4 vrij te geven.

Wanneer u klaar bent, is één bestaande zending (waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*) is bijgewerkt. Hieraan is één nieuwe regel toegevoegd.

### <a name="release-sales-orders-from-order-set-5"></a>Verkooporders vrijgeven vanuit orderset 5

Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 5 vrij te geven.

Wanneer u klaar bent, ziet u dat de volgende acties zijn uitgevoerd:

- Eén bestaande zending (waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*) is bijgewerkt. Een regel uit verkooporder 5-3 (waarbij het veld **Bestelopdracht van klant** is ingesteld op *1*) is hieraan toegevoegd.
- Er is één nieuwe zending gemaakt, waarbij regels van verkooporders 5-1 en 5-2 in één zending worden gegroepeerd.

### <a name="release-sales-orders-from-order-set-6"></a>Verkooporders vrijgeven vanuit orderset 6

Volg de [basisprocedure voor vrijgave naar het magazijn](#release-procedure) om de verkooporders uit orderset 6 vrij te geven.

Wanneer u klaar bent, ziet u dat er vier zendingen zijn gemaakt:

- Regels van twee orders voor klant *US-003* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van twee orders voor klant *US-004* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van verkooporders 6-5 en 6-6 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van verkooporders 6-7 en 6-8 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *CrossOrder*.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Beleidsregels voor consolidatie van zendingen](about-shipment-consolidation-policies.md)
- [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]