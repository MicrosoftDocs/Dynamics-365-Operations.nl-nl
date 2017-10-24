---
title: Uitgaand proces
description: Dit onderwerp biedt een overzicht van het uitgaande proces in Voorraadbeheer.
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: nl-nl
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a>Uitgaand proces

[!include[banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van het uitgaande proces in Voorraadbeheer.

## <a name="output-orders"></a>Uitvoerorders

Uitvoerorders worden gebruikt om verkooporderregels en transferorderregels te koppelen aan de processen voor uitgaande orderverzamelingen waarvoor wordt gebruikgemaakt van orderverzamellijsten.

Wanneer orderverzamellijsten worden gegenereerd op basis van verkooporders of transferorders, worden er automatisch uitvoerorders en verzendingen gemaakt. Een orderverzamellijst heeft een één-op-één-relatie met een zending. De transferorderzending of pakbon van de verkooporder kan worden verwerkt vanuit de zending. 

In het volgende diagram wordt een overzicht gegeven van het proces voor uitgaande orders. 

[![Overzicht van het proces voor uitgaande orders](./media/outbound-order.png)](./media/outbound-order.png)

U kunt uitgaande regels instellen om te bepalen hoe het uitgaande proces moet worden uitgevoerd. U kunt het verzendproces aansturen door middel van deze regels. U kunt de regels in het bijzonder gebruiken om te bepalen tijdens welke fase van het proces een zending kan worden verzonden. De volgende instellingen bepalen hoe de uitgaande processen worden verwerkt.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Status van de orderverzamelroute voor verkoop- en transferorders 

Ga naar **Klant** \> **Instellingen** \> **Parameters van module Klanten** en selecteer op het tabblad **Updates** een waarde in het veld **Status orderverzamelroute**.

[![Veld Status orderverzamelroute voor verkooporders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Als het veld **Status orderverzamelroute** is ingesteld op **Voltooid**, wordt het orderverzamelproces automatisch uitgevoerd als onderdeel van het proces voor het genereren van orderverzamellijsten. Als het veld is ingesteld op **Geactiveerd**, moeten de regels van de orderverzamellijst handmatig worden bijgewerkt.

Dezelfde instellingen zijn van toepassing op transferorders. Ga naar **Voorraadbeheer** \> **Instellingen** \> **Parameters voor voorraad- en magazijnbeheer** en selecteer op het tabblad **Transport** een waarde in het veld **Status orderverzamelroute**.

[![Veld Status orderverzamelroute voor transferorders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Uitvoerorders voor voorraad beëindigen

Ga naar **Voorraadbeheer** \> **Instellingen** \> **Parameters voor voorraad- en magazijnbeheer** en stel op het tabblad **Algemeen** de optie **Uitvoerorder voor voorraad beëindigen** in.

[![Optie Uitvoerorder voor voorraad beëindigen](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Soms kunnen bepaalde artikelen in voorraad niet worden opgenomen als onderdeel van het orderverzamellijstproces. Deze situatie kan zich bijvoorbeeld voordoen als een magazijnmedewerker de aantallen op orderverzamelregels verlaagt en de orderverzamellijst verwerkt. Als het veld **Uitvoerorder voor voorraad beëindigen** is ingesteld op **Ja**, worden de resterende niet-verzamelde hoeveelheden teruggerapporteerd op orderniveau. Als de optie is ingesteld op **Nee**, blijven de resterende niet-verzamelde hoeveelheden behouden als openstaande uitvoerorderhoeveelheid. In dit geval blijven de hoeveelheden aan het magazijn vrijgegeven en moeten deze worden toegevoegd aan een nieuwe orderverzamellijst als onderdeel van de functionaliteit **Openstaande uitvoerorders**.

[![Opdracht Openstaande uitvoerorders in het menu Functies](./media/open-output-order.png)](./media/open-output-order.png)

[![Menu Functies op de pagina Openstaande uitvoerorders](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Hoeveelheid verminderen

De derde parameter die u gebruiken kunt als onderdeel van het proces voor het genereren van orderverzamellijsten, is de parameter **Hoeveelheid verminderen**. De instelling van deze parameter werkt samen met de instelling **Reservering** om een reserveringsproces te genereren als onderdeel van de vrijgave naar het magazijn.

[![Parameter Hoeveelheid verminderen](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Voorbeeld van een uitgaand proces voor een verkooporder

In dit voorbeeld is er een verkooporder voor twee artikelen. Tijdens het genereren van de orderverzamellijst selecteert u de parameter **Hoeveelheid verminderen**. Daarom worden orderverzamelregels alleen gemaakt en vrijgegeven voor beschikbare voorhanden voorraad. De orderverzameling moet worden gerapporteerd via een registratieproces voor orderverzamellijsten (**Status orderverzamelroute** = **Geactiveerd**).

De voorraad die nog niet is gereserveerd, wordt gereserveerd tijdens het genereren van de orderverzamellijst. De niet-beschikbare voorraad kan worden verwijderd uit de verkooporder of worden vrijgegeven aan het magazijn voor uitgaande verwerking op een later tijdstip, wanneer voorraad beschikbaar is voor orderverzameling.

[![De orderverzamellijst bijwerken](./media/update-picking-list.png)](./media/update-picking-list.png)

Zodra alle orderverzamelregels zijn verzameld op de pagina **Orderverzamellijstregistratie**, wordt de bijbehorende zending voltooid. Het proces voor pakbonnen voor verkooporders kan vervolgens worden geïnitialiseerd op basis van de verzamelde voorraad.

[![Uitgaande zendingen bijwerken](./media/outbound-shipments.png)](./media/outbound-shipments.png)

