---
title: Ondersteuning voor Inventory Visibility voor WMS-artikelen
description: In dit artikel wordt de ondersteuning van Voorraadzichtbaarheid beschreven voor artikelen die zijn ingeschakeld voor magazijnbeheerprocessen (WMS-artikelen).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066605"
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

Gebruik functie Advanced WMS voor Voorraadzichtbaarheid in scenario's waarin aan alle volgende voorwaarden is voldaan:

- U synchroniseert Supply Chain Management-gegevens met Voorraadzichtbaarheid.
- U gebruikt WMS in Supply Chain Management.
- Gebruikers maken reserveringen voor WMS-artikelen op andere niveaus dan het magazijnniveau (bijvoorbeeld omdat u magazijnwerk gebruikt).

In andere scenario's is het mogelijk dat resultaten van query's voor voorhanden voorraad hetzelfde zijn, ongeacht of de functie Advanced WMS voor Voorraadzichtbaarheid is ingeschakeld. Bovendien zijn de prestaties beter als u de functie in deze scenario's niet inschakelt, omdat er minder berekeningen zijn en minder overhead.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>De functie Advanced WMS voor Voorraadzichtbaarheid inschakelen

Voer deze stappen uit om de functie Advanced WMS voor Voorraadzichtbaarheid in te schakelen.

1. Meld u aan bij Supply Chain Management als beheerder.
1. Open het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakel de volgende functies in deze volgorde in:

    1. *Integratie van voorraadzichtbaarheid*
    1. *Magazijnartikelen inschakelen voor Voorraadzichtbaarheid*

1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor Voorraadzichtbaarheidsintegratie**.
1. Stel op het tabblad **WMS-artikelen inschakelen** de optie **WMS-artikelen inschakelen** in op *Ja*.
1. Meld u aan bij Power Apps.
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

Alle andere fysieke metingen worden op dezelfde wijze berekend als wanneer de functie Advanced WMS voor Voorraadzichtbaarheid is uitgeschakeld.

Zie het technisch document [Reserveringen in Magazijnbeheer](https://www.microsoft.com/download/details.aspx?id=43284) voor gedetailleerde informatie over berekeningen van voorhanden WMS-artikelen.

De gegevensentiteiten die worden geëxporteerd naar Dataverse, kunnen de hoeveelheden voor WMS-artikelen niet bijwerken. De hoeveelheden die in de gegevensentiteiten worden weergegeven, zijn correct voor niet-WMS-artikelen en voor hoeveelheden die niet worden beïnvloed door WMS-logica (dus metingen behalve `AvailPhysical`, `AvailOrdered`, `ReservPhysical` en `ReservOrdered` in de `fno`-gegevensbron).

Het is niet toegestaan wijzigingen aan te brengen in de hoeveelheid WMS-artikelen die zijn opgeslagen in de gegevensbron van Supply Chain Management. Net als bij andere functies van Voorraadzichtbaarheid wordt deze beperking toegepast om conflicten te voorkomen.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>Zachte reserveringen voor WMS-artikelen in Voorraadzichtbaarheid

In het algemeen worden [zachte reserveringen](inventory-visibility-reservations.md) op WMS-artikelen ondersteund. U kunt aan WMS gerelateerde fysieke metingen opnemen in berekeningen voor zachte reserveringen. 

Het is een bekende beperking dat de berekening *beschikbaar voor reservering* op dit moment niet ondersteund voor WMS-artikelen. Als er bij een reservering boven de huidige dimensies een zachte reservering plaatsvindt, is de berekening *beschikbaar voor reservering* daarom onjuist. Dit heeft geen invloed op zachte reserveringen als de optie **ifCheckAvailForReserv** is uitgeschakeld in [de API voor zachte reservering](inventory-visibility-api.md#create-one-reservation-event).

Deze beperking is ook van toepassing op functies en aanpassingen die zijn gebaseerd op zachte reserveringen (zoals toewijzing).

## <a name="calculate-available-to-promise-quantities"></a>Available to promise-hoeveelheden berekenen

De oplossing ondersteunt volledig [ATP (available to promise)](inventory-visibility-available-to-promise.md) voor WMS-artikelen. U kunt ATP-berekeningen definiëren zonder WMS-specifieke details te bepalen.
