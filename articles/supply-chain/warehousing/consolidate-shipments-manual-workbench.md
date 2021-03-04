---
title: Zendingen consolideren met de workbench voor het consolideren van zendingen
description: Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd in zendingen via de workbench voor het consolideren van zendingen.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1eec1a8e3a9a2a0f95302e1d6ea68eb90b9a3b93
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425785"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Zendingen consolideren met de workbench voor het consolideren van zendingen

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd in zendingen via de workbench voor het consolideren van zendingen.

## <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Consolidatiebeleid voor zendingen en productfilters instellen

In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven. Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a>De functie voor handmatige zendingsconsolidatie inschakelen

Voordat u de functie *Handmatige zendingsconsolidatie* kunt gebruiken, moet u deze in het systeem inschakelen. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Handmatige zendingsconsolidatie*

Zoals vermeld in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md), moet u ook de functie *Zending consolideren* inschakelen voordat u beleid kunt maken. U moet die stap echter al hebben voltooid.

## <a name="create-the-sales-orders-for-this-scenario"></a>De verkooporders voor dit scenario maken

Maak eerst een verzameling verkooporders waarmee u kunt werken. U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS). Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.

Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.

### <a name="create-order-set-1"></a>Orderset 1 maken

#### <a name="sales-orders-1-1-and-1-2"></a>Verkooporders 1-1 en 1-2

1. Maak twee identieke verkooporders met de volgende instellingen:

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
    - **Leveringsmethode:** *Airwa-Air*

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

## <a name="release-the-orders-to-the-warehouse"></a>De orders vrijgeven naar het magazijn

Voer de volgende stappen uit om elke verkooporder die u voor dit scenario hebt gemaakt, vrij te geven naar het magazijn.

1. Ga naar **Klanten \> Orders \> Alle verkooporders**.
1. Zoek en selecteer de verkooporder om vrij te geven.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Acties \> Vrijgave naar magazijn** om de geselecteerde verkooporder vrij te geven.
1. Herhaal deze procedure voor elke andere verkooporder die u voor dit scenario hebt gemaakt.

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>De zendingen consolideren met de workbench voor het consolideren van zendingen

1. Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Workbench zendingsconsolidatie**.
1. Selecteer **Query bewerken** in het actievenster.
1. Selecteer in de het dialoogvenster van de query-editor op het tabblad **Bereik** de optie **Toevoegen** om een rij met de volgende instellingen aan het raster toe te voegen:

    - **Tabel:** *Verkooporders*
    - **Veld:** *Verkooporder*
    - **Criteria:** voer een door komma's gescheiden lijst in van de verkoopordernummers voor elke orderset die u voor dit scenario hebt gemaakt.

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Selecteer in het actievenster de optie **Zendingen consolideren**.
1. Selecteer alle zendingen en selecteer in het actievenster de optie **Consolideren**.

## <a name="verify-the-shipments"></a>De zendingen verifiëren

Met de volgende procedure kunt u de zendingen controleren die zijn gemaakt of bijgewerkt als gevolg van een zendingsconsolidatie. Gebruik deze om alle ordersets te controleren die u voor dit scenario hebt gemaakt en bekijk vervolgens de subsecties die volgen om te controleren of u de verwachte resultaten hebt verkregen.

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Zoek en selecteer de vereiste zending.
1. Als een consolidatiebeleid is gebruikt bij het maken of bijwerken van de zending, wordt dit weergegeven in het veld **Consolidatiebeleid voor zendingen**.

### <a name="related-shipments-for-order-set-1"></a>Gerelateerde zendingen voor orderset 1

Er moeten twee zendingen zijn gemaakt:

- De eerste zending bevat drie regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerMode*.
- De tweede zending, die geen gebruikmaakt van de leveringsmethode *Airways*, is gemaakt met het consolidatiebeleid voor zending *CustomerOrderNo*.

### <a name="related-shipments-for-order-set-2"></a>Gerelateerde zendingen voor orderset 2

Er moeten drie zendingen zijn gemaakt:

- De eerste zending bevat items van het type *Ontvlambaar*.
- Elk van de twee overige zendingen bevat één regel met het item *Explosief*.

### <a name="related-shipments-for-order-set-3"></a>Gerelateerde zendingen voor orderset 3

Er moeten twee zendingen zijn gemaakt:

- De eerste zending bevat orderregels uit de verkooporder waarvoor het veld **Bestelopdracht van klant** is ingesteld op *1*.
- De tweede zending bevat orderregels uit verkooporders waarvoor het veld **Bestelopdracht van klant** is ingesteld op *2*.

### <a name="related-shipments-for-order-set-4"></a>Gerelateerde zendingen voor orderset 4

Er moeten vier zendingen zijn gemaakt:

- Regels van twee orders voor klant *US-003* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van twee orders voor klant *US-004* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van verkooporders 4-5 en 4-6 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *Ordergroep*.
- Regels van verkooporders 4-7 en 4-8 voor klanten *US-007* zijn gegroepeerd in één zending via het consolidatiebeleid voor zendingen van het type *CrossOrder*.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Beleidsregels voor consolidatie van zendingen](about-shipment-consolidation-policies.md)
- [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]