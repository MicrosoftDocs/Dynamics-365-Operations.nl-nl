---
title: Overzicht van Uitgaand proces
description: Dit onderwerp biedt een overzicht van het uitgaande proces in Voorraadbeheer.
author: yufeihuang
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 27043828b44cf532d0d8d5091324ba30f3f90cf8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578507"
---
# <a name="outbound-process-overview"></a>Overzicht van Uitgaand proces

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van het uitgaande proces in Voorraadbeheer.

## <a name="output-orders"></a>Uitvoerorders

Uitvoerorders worden gebruikt om verkooporderregels en overboekingsorderregels te koppelen aan de processen voor uitgaande orderverzamelingen waarvoor wordt gebruikgemaakt van orderverzamellijsten.

Wanneer orderverzamellijsten worden gegenereerd op basis van verkooporders of overboekingsorders, worden er automatisch uitvoerorders en verzendingen gemaakt. Een orderverzamellijst heeft een één-op-één-relatie met een zending. De overboekingsorderzending of pakbon van de verkooporder kan worden verwerkt vanuit de zending. 

In het volgende diagram wordt een overzicht gegeven van het proces voor uitgaande orders. 

[![Overzicht van het proces voor uitgaande orders.](./media/outbound-order.png)](./media/outbound-order.png)

U kunt uitgaande regels instellen om te bepalen hoe het uitgaande proces moet worden uitgevoerd. U kunt het verzendproces aansturen door middel van deze regels. U kunt de regels in het bijzonder gebruiken om te bepalen tijdens welke fase van het proces een zending kan worden verzonden. De volgende instellingen bepalen hoe de uitgaande processen worden verwerkt.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Status van de orderverzamelroute voor verkoop- en overboekingsorders 

Ga naar **Klant** \> **Instellingen** \> **Parameters van module Klanten** en selecteer op het tabblad **Updates** een waarde in het veld **Status orderverzamelroute**.

[![Veld Status orderverzamelroute voor verkooporders.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Als het veld **Status orderverzamelroute** is ingesteld op **Voltooid**, wordt het orderverzamelproces automatisch uitgevoerd als onderdeel van het proces voor het genereren van orderverzamellijsten. Als het veld is ingesteld op **Geactiveerd**, moeten de regels van de orderverzamellijst handmatig worden bijgewerkt.

Dezelfde instellingen zijn van toepassing op overboekingsorders. Ga naar **Voorraadbeheer** \> **Instellingen** \> **Parameters voor voorraad- en magazijnbeheer** en selecteer op het tabblad **Transport** een waarde in het veld **Status orderverzamelroute**.

[![Veld Status orderverzamelroute voor overboekingsorders.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Uitvoerorders voor voorraad beëindigen

Ga naar **Voorraadbeheer** \> **Instellingen** \> **Parameters voor voorraad- en magazijnbeheer** en stel op het tabblad **Algemeen** de optie **Uitvoerorder voor voorraad beëindigen** in.

[![Optie Uitvoerorder voor voorraad beëindigen.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Als de orderverzamellijsthoeveelheden worden verlaagd door de magazijnmedewerker, worden de betreffende voorraadorderhoeveelheden verwijderd uit de zending. Als de orderverzamellijst op een bepaald moment wordt bijgewerkt, worden de resterende hoeveelheden weer gerapporteerd aan de order als de optie **Uitvoerorder voor voorraad beëindigen** is ingesteld op **Ja**. Als de optie **Uitvoerorder voor voorraad beëindigen** is ingesteld op **Nee**, worden de resterende hoeveelheden bewaard als openstaande uitvoerorderhoeveelheid en moeten deze worden toegevoegd aan een nieuwe orderverzamellijst als onderdeel van de functie **Openstaande uitvoerorders**. 

[![Opdracht Openstaande uitvoerorders in het menu Functies.](./media/open-output-order.png)](./media/open-output-order.png)

[![Menu Functies op de pagina Openstaande uitvoerorders.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Hoeveelheid verminderen

De derde parameter die u gebruiken kunt als onderdeel van het proces voor het genereren van orderverzamellijsten, is de parameter **Hoeveelheid verminderen**. De instelling van deze parameter werkt samen met de instelling **Reservering** om een reserveringsproces te genereren als onderdeel van de vrijgave naar het magazijn.

[![Parameter Hoeveelheid verminderen.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Voorbeeld van een uitgaand proces voor een verkooporder

In dit voorbeeld is er een verkooporder voor twee artikelen. Tijdens het genereren van de orderverzamellijst selecteert u de parameter **Hoeveelheid verminderen**. Daarom worden orderverzamelregels alleen gemaakt en vrijgegeven voor beschikbare voorhanden voorraad. De orderverzameling moet worden gerapporteerd via een registratieproces voor orderverzamellijsten (**Status orderverzamelroute** = **Geactiveerd**).

De voorraad die nog niet is gereserveerd, wordt gereserveerd tijdens het genereren van de orderverzamellijst. De niet-beschikbare voorraad kan worden verwijderd uit de verkooporder of worden vrijgegeven aan het magazijn voor uitgaande verwerking op een later tijdstip, wanneer voorraad beschikbaar is voor orderverzameling.

[![De orderverzamellijst bijwerken.](./media/update-picking-list.png)](./media/update-picking-list.png)

Zodra alle orderverzamelregels zijn verzameld op de pagina **Orderverzamellijstregistratie**, wordt de bijbehorende zending voltooid. Het proces voor pakbonnen voor verkooporders kan vervolgens worden geïnitialiseerd op basis van de verzamelde voorraad.

[![Uitgaande zendingen bijwerken.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]