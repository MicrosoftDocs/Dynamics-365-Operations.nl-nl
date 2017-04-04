---
title: "Detailhandelsmededelingen definiëren (Commerce Data Exchange)"
description: Dit artikel biedt een overzicht van Commerce Data Exchange en de onderdelen hiervan. Het onderdeel waarvoor elke component bij de overdracht van gegevens tussen Microsoft Dynamics 365 voor bewerkingen en detailhandelkanalen speelt overgaat.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Detailhandelsmededelingen definiëren (Commerce Data Exchange)

Dit artikel biedt een overzicht van Commerce Data Exchange en de onderdelen hiervan. Het onderdeel waarvoor elke component bij de overdracht van gegevens tussen Microsoft Dynamics 365 voor bewerkingen en detailhandelkanalen speelt overgaat.

<a name="overview"></a>Overzicht
--------

Commerce Data Exchange is een systeem dat de gegevensoverdracht tussen Dynamics 365 for Operations en detailhandelkanalen, zoals onlinewinkels of markering boven en fysieke winkels. De database waarin gegevens voor de detailhandel is onafhankelijk van de Dynamics 365 voor bewerkingen-database. De kanaaldatabase bevat alleen de gegevens die voor detailhandelstransacties zijn vereist. Hoofdgegevens is geconfigureerd in Dynamics 365 for Operations en verdeeld over kanalen. Transactionele gegevens wordt gemaakt in de plaats van verkooppunten (POS)-systeem of de on line op te slaan en vervolgens geüpload naar Dynamics 365 voor bewerkingen. De gegevensdistributie is asynchroon. Met andere woorden, het proces van verpakkingsgegevens verzamelen bij de bron vindt afzonderlijk plaats van het proces voor het ontvangen en toepassen van gegevens op de bestemming. Voor sommige scenario´s, zoals prijs- en voorraadzoekopdrachten, moeten de gegevens in realtime worden opgehaald. Ter ondersteuning van deze scenario's, bevat Commerce Data Exchange ook een service waarmee real-time communicatie tussen Dynamics 365 for Operations en een kanaal. 

[![bijgewerkt retail grafiek](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async-service
Microsoft SQL Server-wijzigingen bijhouden in de Dynamics 365 voor bewerkingen database wordt gebruikt om te bepalen welke gegevenswijzigingen naar kanalen worden verzonden. Op basis van een distributieplanning, Dynamics 365 for Operations pakketten die gegevens en opgeslagen in de centrale opslag (Azure blobopslag). Een afzonderlijk batchproces gebruikt Commerce Data Exchange: Async Client-bibliotheek om dit gegevenspakket in de kanaaldatabase te voegen. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Detailhandel planner

Plannertaken zijn het mechanisme voor het distribueren van gegevens naar en vanuit locaties. De taken worden samengesteld uit subtaken, die de tabellen en tabelvelden opgeven die de gegevens voor distributie bevatten. Dynamics 365 voor bewerkingen bevat vooraf gedefinieerde plannertaken en subtaken die voldoen aan de replicatievereisten van de meeste organisaties. De volgende typen vooraf gedefinieerde taken worden gemaakt:

-   **Taken downloaden** : Download taken verzenden gegevens die is gewijzigd van Dynamics 365 for Operations kanaal databases. Wijzigingen in records worden gevolgd door SQL Server-wijzigingstracering.
-   **Uploaden van taken (P-taken)** : uploadtaken verkooptransacties van een kanaal in de Dynamics 365 voor bewerkingen database ophalen. P-taken uploaden gegevens oplopend. Wanneer een P-taak wordt uitgevoerd, controleert de Async Client-bibliotheek de replicatietelling voor records die al van een locatie zijn ontvangen. Een record wordt alleen geüpload als de replicatieteller hoger is dan de grootste waarde die is gevonden. P-taken werken geen gegevens bij die eerder zijn geüpload.

De distributieplanning wordt gebruikt voor het uitvoeren van de gegevensoverdracht handmatig of door het plannen van een batchtaak in Dynamics 365 voor bewerkingen. Een distributieplanning kan een of meer kanaalgegevensgroepen en een of meer plannertaken bevatten.

## <a name="realtime-service"></a>Realtime-Service
Commerce Data Exchange: Real-time Service is een geïntegreerde service waarmee real-time communicatie tussen Dynamics 365 for Operations en detailhandelkanalen. Real-time Service kan afzonderlijke POS-computers en on line winkels specifieke gegevens ophalen uit Dynamics 365 voor bewerkingen in real-time. Hoewel de meeste belangrijke bewerkingen kunnen worden uitgevoerd in de kanaaldatabase lokaal, moeten de volgende scenario's rechtstreeks toegang tot de gegevens die zijn opgeslagen in Dynamics 365 voor bewerkingen:

-   Geschenkbonnen uitgeven en inwisselen.
-   Loyaliteitspunten inwisselen.
-   Creditnota's uitgeven en inwisselen.
-   Klantrecords maken en bijwerken.
-   Verkooporders maken, bijwerken en voltooien.
-   Voorraad ontvangen voor een inkoop- of transferorder.
-   Voorraadtellingen uitvoeren
-   Verkooptransacties in meerdere winkels ophalen en retourtransacties voltooien.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Een vooraf gedefinieerde Real-time Service-profiel wordt gemaakt.


