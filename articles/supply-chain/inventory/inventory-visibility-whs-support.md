---
title: Ondersteuning voor Inventory Visibility voor WMS-artikelen
description: In dit artikel wordt de ondersteuning van Voorraadzichtbaarheid beschreven voor artikelen die zijn ingeschakeld voor magazijnbeheerprocessen (WMS-artikelen).
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762734"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Ondersteuning voor Inventory Visibility voor WMS-artikelen

[!include [banner](../includes/banner.md)]

In dit artikel wordt de ondersteuning van Voorraadzichtbaarheid beschreven voor artikelen die zijn ingeschakeld voor magazijnbeheerprocessen (WMS-artikelen). De functie waarmee u deze mogelijkheid aan Voorraadzichtbaarheid toevoegt, heet *Advanced WMS*.

## <a name="wms-items"></a>WMS-artikelen

Een WMS-artikel is een artikel dat wordt ingeschakeld voor WMS en wordt verwerkt in een magazijn waarvoor WMS is ingeschakeld.

Meer informatie over WMS en de module **Warehouse management** in Microsoft Dynamics 365 Supply Chain Management vindt u in [Overzicht van Magazijnbeheer](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Reikwijdte van de functie

De functie Advanced WMS voor Voorraadzichtbaarheid is gericht op berekeningen van de voorraadhoeveelheid op basis van query's voor voorhanden voorraad. Deze functie is niet bedoeld om Voorraadzichtbaarheid te gebruiken om de verwerkingsactiviteiten van magazijnen in het algemeen te beheren. Bij Voorraadzichtbaarheid worden geen magazijnspecifieke concepten aan de gebruikers getoond. Dit zijn enkele voorbeelden van deze concepten:

- Reserveringshiërarchie
- Of voor een artikel of magazijn WMS is ingeschakeld
- Volgordegroep-id eenheid
- Magazijnspecifieke processen, zoals zendingen, ladingen, waves en werk

Voorraadzichtbaarheid leidt deze informatie af op basis van de gegevens die vanuit Supply Chain Management worden verzonden. De WMS-specifieke gegevens (met andere woorden gegevens uit de tabel `WHSInventReserve`) zijn niet zichtbaar voor gebruikers.

Wanneer u de functie Advanced WMS voor Voorraadzichtbaarheid gebruikt, zijn alle queryresultaten identiek aan de resultaten van query's die direct in Supply Chain Management zijn uitgevoerd. Ze zijn echter niet identiek aan de resultaten van query's van de mobiele app Warehouse Management, omdat de mobiele app een iets andere berekeningslogica gebruikt.

## <a name="when-to-use-the-feature"></a>Wanneer gebruikt u deze functie

Gebruik WMS-functie voor Voorraadzichtbaarheid in scenario's waarin aan alle volgende voorwaarden is voldaan:

- U synchroniseert Supply Chain Management-gegevens met Voorraadzichtbaarheid.
- U gebruikt WMS in Supply Chain Management.
- Gebruikers maken reserveringen voor WMS-artikelen op niveaus onder het magazijnniveau (bijvoorbeeld op naamplaatniveau omdat u magazijntaken verwerkt).

In andere scenario's is het mogelijk dat resultaten van query's voor voorhanden voorraad hetzelfde zijn, ongeacht of de functie Advanced WMS voor Voorraadzichtbaarheid is ingeschakeld. Bovendien zijn de prestaties beter als u de functie in deze scenario's niet inschakelt, omdat er minder berekeningen zijn en minder overhead.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>De functie WMS voor Voorraadzichtbaarheid inschakelen

Voer deze stappen uit om de functie WMS voor Voorraadzichtbaarheid in te schakelen.

1. Meld u aan bij Supply Chain Management als beheerder.
1. Open het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakel de volgende functies in deze volgorde in:

    1. *Integratie van voorraadzichtbaarheid*
    1. *Magazijnartikelen inschakelen voor Voorraadzichtbaarheid*

1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor Voorraadzichtbaarheidsintegratie**.
1. Stel op het tabblad **WMS-artikelen inschakelen** de optie **WMS-artikelen inschakelen** in op *Ja*.
1. Meld u aan bij uw Power Apps-omgeving en open **Voorraadzichtbaarheid**.
1. Open de pagina **Configuratie** en schakel op het tabblad **Functiebeheer** de functie *AdvancedWHS* in.
1. Ga in Supply Chain Management naar **Voorraadbeheer \> Periodieke taken \> Integratie van voorraadzichtbaarheid**.
1. Selecteer in het actievenster de optie **Uitschakelen** in om Voorraadzichtbaarheid tijdelijk uit te schakelen.
1. Selecteer in het actievenster **Inschakelen** om Voorraadzichtbaarheid weer in te schakelen. De invoegtoepassing wordt opnieuw geladen en de nieuwe functie is nu ingeschakeld. Uw WMS-gegevens worden gesynchroniseerd met Voorraadzichtbaarheid.

## <a name="query-on-hand-quantities-of-wms-items"></a>Query voorraadhoeveelheden van WMS-artikelen

Als u query's wilt uitvoeren op WMS-artikelen, gebruikt u dezelfde [API (Application Programming Interface) en berichtsyntaxis](inventory-visibility-api.md) als voor niet-WMS-artikelen. U hoeft niet op te geven of een artikel een WMS-artikel of een niet-WMS-artikel is. Bij Voorraadzichtbaarheid worden artikelen automatisch van elkaar onderscheiden op basis van de gegevens die zijn opgeslagen.

De resultaten van query's voor WMS-artikelen zijn in wezen gelijk aan de resultaten voor niet-WMS-artikelen. Het enige verschil is dat de volgende fysieke metingen uit de `fno`-gegevensbron worden berekend op basis van WMS-logica in Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Alle andere fysieke metingen worden op dezelfde wijze berekend als wanneer de functie WMS voor Voorraadzichtbaarheid is uitgeschakeld.

Zie het technisch document [Reserveringen in Magazijnbeheer](https://www.microsoft.com/download/details.aspx?id=43284) voor gedetailleerde informatie over berekeningen van voorhanden WMS-artikelen.

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>Lijstweergave met voorhanden voorraad en gegevensentiteit voor WMS-artikelen

De pagina **Overzicht voorraadzichtbaarheid vooraf laden** biedt een weergave voor de entiteit *Resultaten van voorhanden vooraf geladen index-query*. In tegenstelling tot de entiteit *Voorraadoverzicht* biedt de *Resultaten van voorhanden vooraf geladen index-query* een voorhanden voorraadlijst van producten met geselecteerde dimensies. Voorraadzichtbaarheid synchroniseert elke 15 minuten de vooraf geladen overzichtsgegevens.

Als u Voorraadzichtbaarheid gebruikt met WMS-artikelen en de lijst voor voorhanden voorraad wilt bekijken voor WMS-artikelen, kunt u het beste de functie *Het overzicht van voorraadzichtbaarheid vooraf laden* inschakelen (zie ook [Vooraf laden van een gestroomlijnde voorhanden query](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)). Een bijbehorende gegevensentiteit in Dataverse slaat het queryresultaat van vooraf laden op, en wordt elke 15 minuten bijgewerkt. De naam van de gegevensentiteit is `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> De entiteit Dataverse is alleen-lezen. U kunt de gegevens weergeven en exporteren in de Voorraadzichtbaarheid-entiteiten, maar **u kunt deze niet wijzigen**.

Het is niet toegestaan wijzigingen aan te brengen in de hoeveelheid WMS-artikelen die zijn opgeslagen in de gegevensbron van Supply Chain Management (`fno`). Dit gedrag komt overeen met het gedrag van andere functies van Voorraadzichtbaarheid. Deze beperking wordt afgedwongen om conflicten te voorkomen.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>Compatibiliteit van WMS-artikelen voor andere functies in Voorraadzichtbaarheid

[Zachte reserveringen](inventory-visibility-reservations.md) en [voorraadtoewijzing](inventory-visibility-allocation.md) van WMS-artikelen worden ondersteund. U kunt aan WMS gerelateerde fysieke metingen opnemen in berekeningen voor zachte reserveringen en toewijzingen.

## <a name="calculate-available-to-promise-quantities"></a>Available to promise-hoeveelheden berekenen

De oplossing ondersteunt volledig [ATP (available to promise)](inventory-visibility-available-to-promise.md) voor WMS-artikelen. U kunt ATP-berekeningen definiëren zonder WMS-specifieke details te bepalen.
