---
title: "Detailhandelsmededelingen definiëren (Commerce Data Exchange)"
description: Dit artikel biedt een overzicht van Commerce Data Exchange en de onderdelen hiervan. In dit artikel wordt uitgelegd welke rol elk onderdeel speelt in de overdacht van gegevens tussen Microsoft Dynamics 365 for Retail en detailhandelafzetkanalen.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Detailhandelsmededelingen definiëren (Commerce Data Exchange)

[!include[banner](../includes/banner.md)]


Dit artikel biedt een overzicht van Commerce Data Exchange en de onderdelen hiervan. In dit artikel wordt uitgelegd welke rol elk onderdeel speelt in de overdacht van gegevens tussen Microsoft Dynamics 365 for Retail en detailhandelafzetkanalen.

<a name="overview"></a>Overzicht
--------

Commerce Data Exchange is een systeem dat gegevens overzet tussen Dynamics 365 for Retail en afzetkanalen voor detailhandel, zoals online winkels of fysieke winkels. De database waarin gegevens voor een detailhandelkanaal worden opgeslagen, is afzonderlijk van de Dynamics 365 for Retail-database. De kanaaldatabase bevat alleen de gegevens die voor detailhandelstransacties zijn vereist. Hoofdgegevens worden geconfigureerd in Dynamics 365 for Retail en naar afzetkanalen gedistribueerd. Transactiegegevens worden gemaakt in het POS-systeem of de onlinewinkel, en worden vervolgens geüpload naar Dynamics 365 for Retail. De gegevensdistributie is asynchroon. Met andere woorden, het proces van verpakkingsgegevens verzamelen bij de bron vindt afzonderlijk plaats van het proces voor het ontvangen en toepassen van gegevens op de bestemming. Voor sommige scenario´s, zoals prijs- en voorraadzoekopdrachten, moeten de gegevens in realtime worden opgehaald. Ter ondersteuning van deze scenario's bevat Commerce Data Exchange ook een service die realtime communicatie tussen Dynamics 365 for Retail en een afzetkanaal mogelijk maakt. 

[![bijgewerkt-detailhandelsgrafiek](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async-service
Microsoft SQL Server-wijzigingstracering in de Dynamics 365 for Retail-database wordt gebruikt om de gegevenswijzigingen te bepalen die naar afzetkanalen moeten worden verzonden. Op basis van een distributieplanning worden die gegevens in Dynamics 365 for Retail verpakt en opgeslagen op een centrale opslag (Azure-blobopslag). Een afzonderlijk batchproces gebruikt Commerce Data Exchange: Async Client-bibliotheek om dit gegevenspakket in de kanaaldatabase te voegen. 

[![Async-service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Detailhandel planner

Plannertaken zijn het mechanisme voor het distribueren van gegevens naar en vanuit locaties. De taken worden samengesteld uit subtaken, die de tabellen en tabelvelden opgeven die de gegevens voor distributie bevatten. Dynamics 365 for Retail bevat vooraf gedefinieerde plannertaken en subtaken die aan de replicatiebehoeften van de meeste organisaties voldoen. De volgende typen vooraf gedefinieerde taken worden gemaakt:

-   **Downloadtaken**: downloadtaken verzenden gewijzigde gegevens van Dynamics 365 for Retail naar afzetkanaaldatabases. Wijzigingen in records worden gevolgd door SQL Server-wijzigingstracering.
-   **Uploadtaken (P-taken)**: uploadtaken vragen verkooptransacties op uit een afzetkanaal en plaatsen deze in de Dynamics 365 for Retail-database. P-taken uploaden gegevens oplopend. Wanneer een P-taak wordt uitgevoerd, controleert de Async Client-bibliotheek de replicatietelling voor records die al van een locatie zijn ontvangen. Een record wordt alleen geüpload als de replicatieteller hoger is dan de grootste waarde die is gevonden. P-taken werken geen gegevens bij die eerder zijn geüpload.

De distributieplanning wordt gebruikt om de gegevensoverdracht uit te voeren, handmatig of door een batchtaak in Dynamics 365 for Retail te plannen. Een distributieplanning kan een of meer kanaalgegevensgroepen en een of meer plannertaken bevatten.

## <a name="realtime-service"></a>Realtime Service
Commerce Data Exchange: Realtime Service is een geïntegreerde service die zorgt voor realtime communicatie tussen Dynamics 365 for Retail en detailhandelafzetkanalen. Met de Realtime Service is het mogelijk om in realtime afzonderlijke POS-computers en onlinewinkels specifieke gegevens uit Dynamics 365 for Retail op te halen. Hoewel de meeste hoofdbewerkingen in de lokale afzetkanaaldatabase kunnen worden uitgevoerd, vereisen de volgende scenario's directe toegang tot de gegevens die in Dynamics 365 for Retail zijn opgeslagen:

-   Geschenkbonnen uitgeven en inwisselen.
-   Loyaliteitspunten inwisselen.
-   Creditnota's uitgeven en inwisselen.
-   Klantrecords maken en bijwerken.
-   Verkooporders maken, bijwerken en voltooien.
-   Voorraad ontvangen voor een inkoop- of transferorder.
-   Voorraadtellingen uitvoeren
-   Verkooptransacties in meerdere winkels ophalen en retourtransacties voltooien.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Er wordt een vooraf gedefinieerd Real-time Service-profiel gemaakt.




