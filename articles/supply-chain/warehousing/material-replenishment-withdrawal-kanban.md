---
title: Aanvulling met opnamekanbans
description: In dit onderwerp wordt beschreven hoe de opnamekanban wordt gebruikt voor materiaalaanvulling voor productieactiviteiten.
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 011da8cd894cc044b6af8b740e49ed8d7c3c0c67
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="replenishment-with-withdrawal-kanbans"></a>Aanvulling met opnamekanbans

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe de opnamekanban wordt gebruikt voor materiaalaanvulling voor productieactiviteiten.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Workflow voor materiaalaanvulling die gebruik maakt van de opnamekanban
-------------------------------------------------------------------

De opnamekanban kan worden gebruikt om een kanban met één artikel te verplaatsen tussen magazijnen en productielocaties waar het materiaal wordt verbruikt. De opnamekanban ondersteunt een pull-oplossing voor materiaalaanvulling, waarbij een pull-signaal vereist is om levering voor een specifieke vraag te activeren. 

In het volgende scenario ziet u een aanvullingssysteem op pull-basis, waarbij een pull-signaal het maken van een kanban triggert om materiaal aan te vullen voor een productieproces. 

[![Pull-signaal triggert het maken van een kanban voor het aanvullen van materiaal voor een productieproces](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Opnamekanban
2.  'Vanaf'-locatie en eindlocatie van kanban voor magazijnwerk
3.  'Naar'-locatie en productie-invoerlocatie van kanban
4.  Productieproces
5.  Magazijnwerk voor kanban-orderverzameling
6.  Magazijnlocaties voor grondstoffen
7.  Materiaalmagazijn
8.  Productiemagazijn

In dit scenario verbruikt een productieproces (4) materiaal van een productie-invoerlocatie (3) in het productiemagazijn (8). Wanneer een materiaalverwerkingseenheid (kanban) wordt verbruikt, wordt deze eenheid geregistreerd als leeg. Een aanvullingssignaal wordt gemaakt voor de artikeloorsprong en een nieuwe kanban (1) wordt gemaakt. In dit geval omvat de artikeloorsprong locaties in het materiaalmagazijn (7). Het materiaal voor de kanban wordt verzameld en naar een locatie (2) in hetzelfde magazijn gebracht. Wanneer het materiaal is verzameld, is het gereed om te worden overgebracht van locatie 2 naar de productie-invoerlocatie (3) in het productiemagazijn (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Magazijnwerk configureren voor kanbanorderverzameling voor de opnamekanban

Om het verzamelen van grondstoffen voor de opnamekanban in te schakelen, moet u wavesjablonen, werksjablonen en locatie-instructies configureren voor het werkordertype **Kanbanorderverzameling**. Dit werkordertype ondersteunt niet alleen het verzamelproces voor de opnamekanban. Het ondersteunt ook het orderverzamelproces voor de fabricagekanban. U kunt echter een afzonderlijke orderverzamelproces voor elk type kanban configureren, door de wavesjablonen, werksjablonen en locatie-instructies van elkaar te scheiden. Om de wavesjablonen, werksjablonen en locatie-instructies te scheiden, stelt u criteria in op het activiteitstype (**Proces** of **Verplaatsen**) in de query's voor deze entiteiten.

## <a name="configure-the-withdrawal-kanban"></a>De opnamekanban configureren

De overboekingsactiviteit die wordt gebruikt voor de opnamekanban wordt geconfigureerd als onderdeel van een geactiveerd activiteitsplan in een lean-productiestroom. Als onderdeel van de configuratie van de overboekingsactiviteit geeft u de 'vanaf'-locatie en de 'naar'-locatie voor de overboeking op. Nadat u de overboekingsactiviteit hebt geconfigureerd, kunt u deze toewijzen aan een kanbanregel van het type **Opname**. De kanbanregel stelt het beleid en de configuraties voor de opnamekanban in. De hoeveelheid van de kanban bepaalt hoeveel eenheden van de materiaalverwerkingseenheid de kanban meeneemt tijdens het overboekingsproces. De vaste kanbanhoeveelheid wordt gebruikt wanneer de aanvullingsstrategie Vast is geselecteerd. Deze hoeveelheid bepaalt hoeveel kanbans nodig zijn om te voorkomen dat de beschikbare voorraad of opbouwvoorraad wordt uitgeput bij de vraagbron. De vaste hoeveelheid kan worden berekend op basis van werkelijke vraag, historische vraag en serviceniveaus. In de volgende twee scenario's wordt beschreven hoe u materiaalaanvulling beheert waarbij de opnamekanban wordt gebruikt.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>Scenario 1: Een productie-invoerlocatie aanvullen met behulp van een opnamekanban van het type Vast

Een productieproces verbruikt een ingekochte grondstof vanuit een productie-invoerlocatie in het productiemagazijn. Wanneer de grondstof wordt ontvangen van de leverancier, wordt deze opgeslagen op locaties in het materiaalmagazijn. Omdat de vraag naar het materiaal wordt beschouwd als stabiel gedurende een periode, is deze geconfigureerd om de productie te beleveren in een kanbanstroom met een vaste hoeveelheid. Wanneer een kanban wordt verbruikt bij de productie-invoerlocatie, wordt een 'leeg'-signaal geregistreerd en een nieuwe kanban van hetzelfde type wordt toegevoegd aan de stroom. 

Het 'leeg'-signaal kan worden geconfigureerd om automatisch op te treden wanneer een kanban is voltooid. U kunt ook kunt het leeg-signaal instellen als een handmatige tussenkomst, die wordt uitgevoerd vanuit het kanbanoverboekingsbord of vanuit een menu op het handheldapparaat. Het kanbanoverboekingsbord is het werkgebied waar alle activiteiten in de levenscyclus van de kanban worden beheerd. 

Wanneer de kanban wordt gemaakt, wordt een waveregel voor de grondstof toegevoegd aan een kanbanwave voor het materiaalmagazijn. In de orderverzamelsectie van het kanbanoverboekingsbord kunt u de status van het materiaal en de bijbehorende magazijnprocessen volgen, vanaf het maken van de wave tot het maken van werk, totdat het materiaal voorhanden is in de 'vanaf'-locatie en gereed is om te worden overgedragen naar de productie-invoerlocaties. De kanban kan worden uitgevoerd vanuit het kanbanoverboekingsbord of vanuit een menu op het handheldapparaat. 

In dit scenario wordt het orderverzamelwerk in het materiaalmagazijn verwerkt als één activiteit. De activiteit voor overboeking van het materiaalmagazijn naar het productiemagazijn wordt verwerkt als een afzonderlijke activiteit. Deze benadering kan handig zijn als er bijvoorbeeld een grote fysieke afstand bestaat tussen de twee magazijnen. In dit geval kan de kanbanoverboekingsactiviteit een vrachtwagenlading vertegenwoordigen. 

Als de afstand tussen de magazijnlocaties en productie-invoerlocatie klein is, kan het efficiënter zijn om de overboekingsactiviteit op te nemen in het orderverzamelproces. Nadat het materiaal is verzameld, kan het dan direct in de productie-invoerlocatie worden ingevoerd. Ter ondersteuning van dit proces configureert u de overboekingsactiviteit zo dat deze wordt automatisch uitgevoerd wanneer het verzamelwerk van de opnamekanban is verwerkt.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>Scenario 2: De overboekingsactiviteit automatisch uitvoeren wanneer het kanbanverzamelwerk wordt verwerkt

In het volgende scenario is de overboekingsactiviteit van de opnamekanban geconfigureerd voor het overboeken tussen twee locaties in hetzelfde magazijn. De overboekingsactiviteit van de opnamekanban is zodanig ingesteld dat deze wordt automatisch uitgevoerd. 

[![De overboekingsactiviteit wordt automatisch uitgevoerd wanneer het kanbanverzamelwerk wordt verwerkt](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Gedeeld magazijn voor grondstoffen en productie
2.  Magazijnlocaties voor grondstoffen
3.  'Vanaf'-locatie en eindlocatie van kanban voor magazijnwerk
4.  Opnamekanban
5.  Productie-invoerlocatie
6.  Productieproces

Nadat een kanban is verbruikt bij de productie-invoerlocatie, wordt de kanban afgemeld als 'leeg' en een nieuwe kanban wordt toegevoegd aan de stroom. Wanneer de kanban wordt gemaakt, wordt een waveregel toegevoegd aan een kanbanwave. Wanneer de kanbanwave wordt verwerkt, wordt magazijnwerk voor het kanbanorderverzamelen gemaakt. De magazijnmedewerker verwerkt het werk voor het kanbanorderverzamelen en wordt door het werk aangestuurd om het materiaal voor de kanban te verzamelen op een magazijnlocatie. Als deze magazijnmedewerker het verzamelen bevestigt, wordt de kanban wordt automatisch voltooid en de magazijnmedewerker wordt geïnstrueerd om het materiaal naar de productie-invoerlocatie te brengen.


