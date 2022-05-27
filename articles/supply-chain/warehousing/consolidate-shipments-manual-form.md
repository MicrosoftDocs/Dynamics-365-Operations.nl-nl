---
title: Zendingen handmatig consolideren via de pagina Zendingen consolideren
description: Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd via de pagina Zendingen consolideren.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 5a2f4a9ed05460f9beedf8653ec80b01c84a7b26
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677473"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Zendingen handmatig consolideren via de pagina Zendingen consolideren

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd via de pagina **Zendingen consolideren**.

## <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Consolidatiebeleid voor zendingen en productfilters instellen

In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven. Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.

## <a name="create-the-sales-orders-for-this-scenario"></a>De verkooporders voor dit scenario maken

Maak eerst een verzameling verkooporders waarmee u kunt werken. U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS). Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.

Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.

### <a name="create-sales-orders-1-and-2"></a>Verkooporders 1 en 2 maken

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-007*
    - **Groep:** *ShipCons*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

### <a name="create-sales-orders-3-and-4"></a>Verkooporders 3 en 4 maken

1. Maak twee identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-007*
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

## <a name="consolidate-shipments"></a>Verzendingen consolideren

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Zoek en selecteer een zending die is gemaakt toen verkooporder 1 werd vrijgegeven naar het magazijn. (Het veld **Consolidatiebeleid voor zendingen** moet zijn ingesteld op *Ordergroep*.)
1. Selecteer in het actievenster op het tabblad **Zendingen** de optie **Zendingen \> Zendingen consolideren**.
1. Controleer de zendingen die worden voorgesteld voor consolidatie. Er moet slechts één zending met hetzelfde beleid worden voorgesteld voor consolidatie.
1. Sluit de pagina **Zendingsconsolidatie**.
1. Zoek en selecteer een zending die is gemaakt toen verkooporder 3 werd vrijgegeven naar het magazijn. (Het veld **Consolidatiebeleid voor zendingen** moet zijn ingesteld op *Standaard*.)
1. Selecteer in het actievenster op het tabblad **Zendingen** de optie **Zendingen \> Zendingen consolideren**.
1. Controleer of geen zendingen worden voorgesteld voor consolidatie.
1. Selecteer **Filters weergeven**.
1. Verwijder in het deelvenster **Filters** het filter **Ordernummer** en selecteer vervolgens **Toepassen**.
1. Controleer de zendingen die worden voorgesteld voor consolidatie. Er moet slechts één zending met hetzelfde beleid worden voorgesteld voor consolidatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Beleidsregels voor consolidatie van zendingen](about-shipment-consolidation-policies.md)
- [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]