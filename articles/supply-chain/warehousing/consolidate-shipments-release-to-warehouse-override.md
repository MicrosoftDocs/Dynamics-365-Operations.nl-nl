---
title: Zendingen consolideren wanneer het consolidatiebeleid voor zendingen wordt overschreven via de pagina Vrijgave naar magazijn
description: In dit onderwerp wordt een scenario weergegeven waarbij een of meer verkoopregels handmatig naar het magazijn moeten worden vrijgegeven via de pagina Vrijgave naar magazijn. Het door het systeem gedefinieerde consolidatiebeleid voor zendingen moet worden overschreven vóór de vrijgave.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 406ff268eede4a9d448b3b9c1729a00fcec8f21e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986739"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a>Zendingen consolideren wanneer het consolidatiebeleid voor zendingen wordt overschreven via de pagina Vrijgave naar magazijn

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt een scenario weergegeven waarbij een of meer verkoopregels handmatig naar het magazijn moeten worden vrijgegeven via de pagina **Vrijgave naar magazijn**. Het door het systeem gedefinieerde consolidatiebeleid voor zendingen moet worden overschreven vóór de vrijgave. Een overschrijving van het consolidatiebeleid voor zendingen kan vereist zijn als een order die doorgaans niet met openstaande zendingen wordt geconsolideerd, moet worden geconsolideerd met openstaande zendingen.

In het scenario maakt u een set verkooporders en overschrijft u vervolgens het standaardbeleid voor consolidatie van zendingen voordat u de orders vrijgeeft naar het magazijn.

## <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Consolidatiebeleid voor zendingen en productfilters instellen

In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven. Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.

## <a name="create-the-sales-orders-for-this-scenario"></a>De verkooporders voor dit scenario maken

1. Ga naar **Klanten \> Orders \> Alle verkooporders** en maak drie identieke verkooporders met de volgende instellingen:

    - **Klantrekening:** *US-002*

1. Voeg een orderregel met de volgende instellingen toe:

    - **Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)
    - **Hoeveelheid:** *1.00*

1. Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>De verkooporders vrijgeven via de pagina Vrijgave naar magazijn

Volg deze stappen om het consolidatiebeleid voor zendingen te overschrijven tijdens de vrijgave naar het magazijn.

1. Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Vrijgave naar magazijn**.
1. Selecteer in het bovenste deelvenster de eerste verkooporder die u voor dit scenario hebt gemaakt.
1. Selecteer **Toevoegen** om de regel toe te voegen aan de vrijgave naar het magazijn. U ziet dat het beleid *Standaard* voor consolidatie van de zending wordt toegepast in het onderste deelvenster.
1. Selecteer **Nieuw consolidatiebeleid voor zending selecteren** in het onderste deelvenster.
1. Selecteer een beleid waarmee consolidatie met andere openstaande zendingen van hetzelfde beleid mogelijk is. Selecteer bijvoorbeeld het beleid *CustomerOrderNo*.
1. Selecteer **Vrijgave naar magazijn**.
1. Selecteer de tweede en derde verkooporder die u voor dit scenario hebt gemaakt.
1. Selecteer **Toevoegen** om de regels toe te voegen aan de vrijgave naar het magazijn. U ziet dat het beleid *Standaard* wordt toegepast in het onderste deelvenster.
1. Selecteer de tweede regel en selecteer vervolgens in het veld **Nieuw consolidatiebeleid voor zending selecteren** het beleid *CustomerOrderNo*.
1. Selecteer **Vrijgave naar magazijn** voor beide regels.

## <a name="verify-the-shipments"></a>De zendingen verifiëren

Er moeten twee zendingen zijn gemaakt:

- De eerste zending bevat twee regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerOrderNo*.
- De tweede zending bevat één regel en is gemaakt met het consolidatiebeleid voor zendingen *Standaard*.

Volg deze stappen om de gemaakte zendingen te controleren.

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Zoek en selecteer de vereiste zending.
1. Controleer in het veld **Consolidatiebeleid voor zendingen** het consolidatiebeleid dat is gebruikt bij het maken van de zending.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Beleidsregels voor consolidatie van zendingen](about-shipment-consolidation-policies.md)
- [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md)
