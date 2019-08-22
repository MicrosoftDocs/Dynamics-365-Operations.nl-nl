---
title: Kanbanregels wijzigen voor een procestaak
description: Deze procedure is gericht op het wijzigen van de gebruikte kanbanregel voor een bepaalde kanban.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c036f6aad79e33df6009913d1e21ff6176f22593
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843788"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Kanbanregels wijzigen voor een procestaak

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure is gericht op het wijzigen van de gebruikte kanbanregel voor een bepaalde kanban. Dit is handig om de belasting van resources te effenen of in het geval van opsplitsing. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de planner, die in een lean manufacturingbedrijf werkt en verantwoordelijk is voor de waardestroom.


## <a name="copy-kanban-rule"></a>Kanbanregel kopiëren
1. Ga naar Kanbanregels.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer gebeurteniskanbanregel 000022 voor L0001.  
3. Klik op Dubbele kanbanregel.
4. Klik op OK.

## <a name="change-kanban-rule"></a>Kanbanregel wijzigen
1. Sluit de pagina.
2. Ga naar Kanbantaakplanning.
3. Markeer in de lijst de geselecteerde rij.
    * Selecteer regel met kanban 000177.  
4. KIik op Alternatieve kanbanregel gebruiken.
5. Klik op Volgende.
6. Typ of selecteer een waarde in het veld Kanbanregel.
    * Selecteer de kanbanregel die u eerder hebt gemaakt. Dit is de kanbanregel met het hoogste cijfer.  
7. Klik op Voltooien.
    * Nu gebruikt de kanbantaak een andere kanbanregel. Dit kan nuttig zijn om de belasting van de werkcellen te effenen.  

