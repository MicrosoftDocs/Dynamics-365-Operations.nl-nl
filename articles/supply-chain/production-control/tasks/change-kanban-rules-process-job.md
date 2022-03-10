---
title: Kanbanregels wijzigen voor een procestaak
description: Deze procedure is gericht op het wijzigen van de gebruikte kanbanregel voor een bepaalde kanban.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13798e3521efacda896ca88a39faf36ac979d42c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574492"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Kanbanregels wijzigen voor een procestaak

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]