---
title: Overzicht van lean manufacturing
description: Dit artikel bevat een overzicht en beschrijving van de functies van lean manufacturing in Microsoft Dynamics AX.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19371
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3c608f13c93446329702f07ef7e8bb08a29d87b9
ms.lasthandoff: 03/31/2017


---

# <a name="lean-manufacturing-overview"></a>Overzicht van lean manufacturing

[!include[banner](../includes/banner.md)]


Dit artikel bevat een overzicht en beschrijving van de functies van lean manufacturing in Microsoft Dynamics AX.

Lean manufacturing biedt hulpprogramma's die u kunt gebruiken om lean-acties te modelleren. Deze hulpprogramma's ondersteunen en bevorderen van de volgende concepten en zakelijke activiteiten:
-   Lean manufacturing opzetten door het modelleren van productie- en logistieke processen als productiestromen.
-   Een flexibel pull-systeem implementeren met behulp van kanbans voor het melden van de vereisten van de aanvraag.
-   Kanbantaken beheren en bijhouden.

De architectuur voor lean manufacturing in Microsoft Dynamics AX 7 bestaat uit productiestromen, activiteiten en kanbanregels. Deze structuren zijn volledig geïntegreerd met de processen in Microsoft Dynamics AX 7. U kunt lean manufacturing gebruiken in een gemengde productieomgeving die verschillende leveringen, producties en sourcingstrategieën combineert. Deze strategieën omvatten productieorders, batchorders voor procesindustrieën, inkooporders en overdrachtorders.
| **Belangrijk **                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| U kunt Microsoft Dynamics AX 7 gebruiken om de implementatie van lean manufacturing met kanbans te ondersteunen. Een succesvolle implementatie van de principes van lean manufacturing is afhankelijk van de interne bedrijfsprocessen die u gebruikt en de werkelijke productieomstandigheden en de omgeving. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a>Productie- en logistieke processen modelleren als productiestromen
Lean manufacturing opzetten door het modelleren van de productie- en logistieke processen als productiestromen. Deze activiteit bestaat uit de volgende taken:
1.  De processen identificeren waarvoor u een flexibele aanvullingsstrategie wilt implementeren en dan deze processen modelleren als productiestromen. U kunt de processen dan analyseren en stroomlijnen. Eén van de doelstellingen van de implementatie van lean manufacturing is het verminderen van afval door de materiaal- en informatiestroom te verbeteren.
2.  Een productiestroom definiëren als een reeks activiteiten die de materiaalstroom beschrijft. Een overdrachtactiviteit definieert de verplaatsing van een product of producten vanaf een locatie naar een andere. Een procesactiviteit definieert een bewerking met toegevoegde waarde die wordt toegepast op een product.
3.  Een versie van de productiestroom maken die de vereisten voor takttijd definieert. Deze vereisten worden gebruikt voor het berekenen van de cyclustijden van elke activiteit in de productiestroom. U kunt meerdere versies van de productiestromen maken en deze versies dan gebruiken om processen te verbeteren.

## <a name="using-kanbans-to-signal-demand-requirements"></a>Kanbans gebruiken voor het melden van de vereisten van de aanvraag
Een pull-systeem produceert alleen goederen wanneer goederen nodig zijn. Deze praktijk verkort verkooplevertijden en overtollige voorraad. U kunt kanbans gebruiken voor het plannen, bijhouden en verwerken van vereisten die zijn gebaseerd op productiestromen. Een kanbanraamwerk maken, kanbanregels maken die bepalen wanneer kanbans worden gemaakt en hoe aan de vereisten wordt voldaan. U kunt twee typen kabanregels maken: Productieregels voor het opstellen van proceskanbantaken en intrekkingskanbanregels voor het opstellen van overdrachtkanbantaken. U kunt de volgende aanvullingsstrategieën opzetten:
-   Kanbanregels met **vaste hoeveelheid** worden gekoppeld aan een vast aantal verwerkingseenheden, wat betekent dat het aantal actieve kanbans constant is. Wanneer alle producten van een Kanban worden verbruikt en de verwerkingseenheden handmatig worden leeggemaakt, wordt een nieuwe kanban van hetzelfde type gemaakt. Wanneer u kanbanregels met vaste hoeveelheid opstelt, kunt u de optimale kanbanhoeveelheden en de producthoeveelheden die worden gebruikt berekenen. De berekening houdt rekening met prognoses, werkelijke vraag vanuit openstaande orders, doorlooptijd om artikelen aan te vullen en de historische vraag.
-   **Geplande** kabanregels vullen vereisten aan die door de hoofdplanning worden berekend. De hoofdplanning genereert geplande kanbans die aan kanbans kunnen worden gefiatteerd.
-   Kanbanregels van het type **Gebeurtenis** vullen vereisten aan die ontstaan uit verkooporderregels, productiestuklijstregels, kanbanregels en minimum voorraadinstellingen. Wanneer gebeurteniskanbans worden gegenereerd, worden ze gekoppeld aan de bronvereisten.

Wanneer kanbans worden gemaakt, worden één of meer kanbantaken gegenereerd op basis van de kabanstroomactiviteiten die zijn gedefinieerd in de kanbanregels.

## <a name="monitoring-and-maintaining-kanban-jobs"></a>Kanbantaken beheren en bijhouden.
Lean manufacturing biedt inzicht in de huidige status van de productie- en logistieke activiteiten die onder de kabanregels vallen. Hierdoor kunt u de volgende taken plannen en voorrang geven:

-   Een overzicht verkrijgen van de huidige kanbantaakplanning.
-   Kanbantaken plannen en opnieuw plannen.
-   De status van kanbantaken bijhouden en vastleggen.

De volgende lijst beschrijft de speciale kanbanborden:
-   Kanbantaakplanning – Geeft een overzicht van de kanbantaken. Het bord geeft kanbantaken en hun status weer voor een of meerdere werkcellen. De taken worden opgesomd op basis van de planningsperioden (dagen of weken) die zijn gedefinieerd in het productiestroommodel. Het bord toont ook het capaciteitsverbruik voor elke planningsperiode zodat u de geplande belasting kunt beheren. U kunt de status van kabantaken veranderen, kanbantaken opnieuw plannen in verschillende planningsperioden en andere taken uitvoeren.
-   Kanbanbord voor overdrachttaken – Dit bord biedt een overzicht van de huidige overdrachttaken. U kunt orderverzamellijsten bijwerken en registreren, overdrachttaken starten en voltooien en andere taken uitvoeren.
-   Kanbanbord voor procestaken - Dit bord is ontworpen om de normale productiestroom te ondersteunen en geeft een overzicht van de actuele situatie in een of meerdere werkcellen. Vanaf dit bord kunt u prioriteit toekennen aan kanbans, of ze ophalen of fabriceren. Het bord is ook ontworpen om scannen van streepjescodes te ondersteunen voor het rapporteren van kanbans.

## <a name="kanban-jobs-and-integration-with-microsoft-dynamics-ax-processes"></a>Kabantaken en integratie met Microsoft Dynamics AX-processen
Kanbantaken zijn volledig geïntegreerd met de huidige processen voor voorraadtransacties in Microsoft Dynamics AX.
-   U kunt orderverzamelactiviteiten uitvoeren om materiaal aan te vullen dat wordt gebruikt om te voldoen aan de vereisten van kanbantaken.
-   U kunt kanbankaarten, rondgaande kanbankaarten en orderverzamellijsten printen ter ondersteuning van het gebruik van kanbans. Deze documenten worden gebruikt om kabantaken weer te geven, bij te houden en te registreren in het magazijn en op de productievloer.
-   U kunt de orderverzamel- en overdrachtactiviteiten registreren in de voorraad door streepjescodes te scannen.

Bovendien ondersteunt lean manufacturing de inkoop- en factureringsprocessen voor services waarnaar uitbestede activiteiten verwijzen.
-   U kunt inkoopovereenkomstregels en services toewijzen aan uitbestede activiteiten.
-   U kunt periodieke inkooporders en ontvangstadviezen opstellen ter ondersteuning van de inkoop en facturering van de services.






