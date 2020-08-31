---
title: Overzicht van Workflowsysteem
description: In dit onderwerp wordt het werkstroomsysteem beschreven.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 068f464fe5385486827b2f904114eb663e08b2e8
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697964"
---
# <a name="workflow-system-overview"></a>Overzicht van Workflowsysteem

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt het werkstroomsysteem beschreven.

## <a name="what-is-workflow"></a>Wat is een workflow?

De voorwaarde van *workflow* kan op twee manieren worden gedefinieerd: als een systeem en als bedrijfsproces.

### <a name="workflow-is-a-system"></a>Workflow is een systeem

Workflow is een systeem dat wordt uitgevoerd op de Application Object Server (AOS). Het workflowsysteem bevat functies waarmee u afzonderlijke workflows of bedrijfsprocessen kunt maken.

### <a name="workflow-is-a-business-process"></a>Workflow is een bedrijfsproces

Een workflow vertegenwoordigt een bedrijfsproces. Een workflow definieert hoe een document zich door het systeem begeeft of stroomt door aan te geven wie een taak moet voltooien, een beslissing moet nemen of een document moet goedkeuren. De volgende illustratie toont bijvoorbeeld een workflow voor onkostennota's.

![Een workflow met elementen die zijn toegewezen aan gebruikers](./media/workflow_user.gif)

Voor een beter begrip van deze workflow wordt aangenomen dat Sam een onkostenrapport voor 7.000 EUR indient. In dit scenario moet Ivan de bonnen beoordelen die Sam naar hem heeft doorstuurt. Vervolgens moeten Frank en Sue het onkostenrapport goedkeuren. Stel nu dat Sam een onkostennota van EUR 11.000 heeft ingediend. In dit scenario moet Ivan de bonnen beoordelen en moeten Frank, Suzan en Anne het onkostenrapport goedkeuren.

## <a name="benefits-of-using-the-workflow-system"></a>Voordelen van het gebruik van het workflowsysteem

Als uw organisatie werkt met het werkstroomsysteem, levert dat tal van voordelen op:

- **Consistente processen**: u kunt definiëren hoe specifieke documenten, zoals opdrachten tot inkoop en onkostennota's, worden verwerkt. Door gebruik van het workflowsysteem garandeert u dat documenten op een consistente, efficiënte manier wordt verwerkt en goedgekeurd.
- **Zichtbaarheid van processen**: u kunt de status, historie en prestatiegegevens van workflowexemplaren volgen. Op deze manier kunt u bepalen of de werkstroom moet worden gewijzigd om de efficiëntie te verbeteren.
- **Gecentraliseerde werklijst**: gebruikers kunnen een gecentraliseerde werklijst raadplegen die weergeeft welke workflowtaken en -goedkeuringen aan hen zijn toegewezen.


## <a name="workflow-content"></a>Workflowinhoud

+ [Workflowsysteemarchitectuur](workflow-system-architecture.md)
+ [Workflowelementen](workflow-elements.md)
+ [Acties in goedkeuringsprocessen voor workflows](workflow-actions.md)
+ [Overzicht van Workflows maken](create-workflow.md)
+ [Workfloweigenschappen configureren](configure-workflow-properties.md)
+ [Handmatige taken configureren in een workflow](configure-manual-task-workflow.md)
+ [Geautomatiseerde taken configureren in een workflow](configure-automated-task-workflow.md)
+ [Goedkeuringsprocessen configureren in een workflow](configure-approval-process-workflow.md)
+ [Goedkeuringsstappen configureren in een workflow](configure-approval-step-workflow.md)
+ [Handmatige beslissingen configureren in een workflow](configure-manual-decision-workflow.md)
+ [Voorwaardelijke beslissingen configureren in een workflow](configure-conditional-decision-workflow.md)
+ [Parallelle activiteiten in een workflow configureren](configure-parallel-activity-workflow.md)
+ [Parallelle vertakkingen in een workflow configureren](configure-parallel-branch-workflow.md)
+ [Workflows voor regelitems configureren](configure-line-item-workflow.md)
+ [Veelgestelde vragen over werkstromen](workflow-FAQ.md)
