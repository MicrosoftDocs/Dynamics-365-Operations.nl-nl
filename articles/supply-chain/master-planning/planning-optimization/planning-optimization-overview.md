---
title: Overzicht van Planningsoptimalisatie
description: Dit onderwerp bevat een overzicht van de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f5b51047dbfc95406ebcdda2255b58e41044a6a6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992615"
---
# <a name="planning-optimization-overview"></a>Overzicht van Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

Met de invoegtoepassing Planningsoptimalisatie voor Microsoft Dynamics 365 Supply Chain Management kan de berekening van de hoofdplanning buiten Dynamics 365 Supply Chain Management en de gerelateerde SQL-database plaatsvinden. De voordelen die zijn gekoppeld aan de functionaliteit Planningsoptimalisatie omvatten betere prestaties en minimale gevolgen voor de SQL-database tijdens uitvoeringen van de hoofdplanning. Snelle planningsuitvoeringen kunnen zelfs tijdens kantooruren worden uitgevoerd, zodat planners direct kunnen reageren op vraag- of parameterwijzigingen.

Als u Planningsoptimalisatie wilt gebruiken, moet u de invoegtoepassing vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS) installeren en de functionaliteit Planningsoptimalisatie inschakelen in Supply Chain Management. Zie [Aan de slag met Planningsoptimalisatie](get-started.md) voor meer informatie.

In de volgende afbeelding wordt het voordeel van het uitvoeren van Planningsoptimalisatie tijdens kantooruren weergegeven.

![Voordeel van het uitvoeren van Planningsoptimalisatie tijdens kantoor uren](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Betere prestaties

Planningsoptimalisatie kan worden gebruikt in scenario's met langlopende hoofdplannen. De functie is speciaal ontworpen voor zeer snelle berekeningen met zeer grote hoeveelheden gegevens. Omdat deze functie is gebouwd als een hyperschaalbare service voor meerdere tenants, kunnen meerdere exemplaren tegelijk samenwerken om het plan te berekenen. Bovendien verwijdert de planningsservice de belasting van de hoofdplanning van uw systeem en werkt deze met een gegevensstroom waarmee de serverbelasting van de server wordt geminimaliseerd.

Met Planningsoptimalisatie kunt u de volgende doelstellingen bereiken:

- Verbeter de planningsprestaties met een kortere uitvoeringstijd.
- Verminder het effect op andere processen tijdens de uitvoering van de hoofdplanning.
- Voer vaker planningsuitvoeringen uit. (U bent niet beperkt tot dagelijkse uitvoeringen.)
- Zorg ervoor dat de toekomstige bedrijfsgroei het planningssysteem niet overbelast.

## <a name="architecture-and-data-flow"></a>Architectuur en gegevensstroom

Wanneer de invoegtoepassing Planningsoptimalisatie vanuit LCS is geïnstalleerd, wordt een beveiligde verbinding met de service Planningsoptimalisatie tot stand gebracht. De service bevindt zich in hetzelfde datacenterland (of regio) als het gerelateerde Supply Chain Management-exemplaar. Als Planningsoptimalisatie is ingesteld en de hoofdplanning wordt uitgevoerd, worden hoofdgegevens en transactiegegevens vanuit Supply Chain Management naar de service Planningsoptimalisatie verzonden.

Als de invoegtoepassing Planningsoptimalisatie wordt verwijderd, worden alle gerelateerde gegevens in de service Planningsoptimalisatie verwijderd.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Algemene gegevensstroom voor regeneratie-uitvoeringen

1. De Supply Chain Management-client verzendt een signaal om een planningsuitvoering vanuit Planningsoptimalisatie aan te vragen.
2. Planningsoptimalisatie vraagt de vereiste gegevens aan via de geïntegreerde connector.
3. De SQL-database verzendt de gevraagde informatie over de instellings-, hoofd- en transactiegegevens naar Planningsoptimalisatie via de connector. De connector zet gegevens tussen Supply Chain Management en de service Planningsoptimalisatie om.
4. De service Planningsoptimalisatie behoudt planningsgerelateerde gegevens in het geheugen en voert de vereiste berekeningen uit.
5. Het resultaat van de planning wordt via de connector naar de Supply Chain Management-data base verzonden. De resultaten omvatten informatie, zoals geplande orders en behoeftetraceringsinformatie. Met Planningsoptimalisatie wordt een signaal verzonden naar Supply Chain Management om aan te geven dat de planningsuitvoering is voltooid. Ook worden relevante berichten en waarschuwingen verzonden.

In de volgende afbeelding wordt de gegevensstroom weergegeven.

![Gegevensstroom voor regeneratie-uitvoeringen](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Gerelateerde bronnen

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Filters op een plan toepassen](plan-filters.md)

[Een planningstaak annuleren](cancel-planning-job.md)
