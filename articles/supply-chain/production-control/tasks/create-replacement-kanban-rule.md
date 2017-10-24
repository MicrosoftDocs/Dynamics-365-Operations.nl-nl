--- 
title: Een vervangende kanbanregel maken
description: Deze procedure is gericht op het vervangen van een bestaande kanbanregel met een nieuwe kanbanregel op een specifieke datum.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5b27200a8d56192d473887f01076eced0f92e4c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-replacement-kanban-rule"></a>Een vervangende kanbanregel maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure is gericht op het vervangen van een bestaande kanbanregel met een nieuwe kanbanregel op een specifieke datum. Dit is handig wanneer wijzigingen in de productiestroom of aanvullingsregels moeten worden gecoördineerd en gepland. Het demobedrijf dat wordt gebruikt om de procedure te maken, is USMF. Deze procedure is bedoeld voor de procesingenieur of de waardestroombeheerder wanneer zij de productie voorbereiden voor een gewijzigde productiestroom of een nieuwe aanvullingsregel. Deze taak vervangt kanbanregel 000022 met een nieuwe regel en verhoogt de maximale hoeveelheid van 48 in 100 voor de nieuwe regel.


## <a name="select-a-kanban-rule-to-replace"></a>Selecteer een te vervangen kanbanregel.
1. Ga naar Kanbanregels.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer kanbanregel 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Een vervangende kanbanregel maken
1. Klik op Kanbanregel vervangen.
2. Typ in het veld Begindatum de datum en een tijd.
    * Selecteer een datum in de toekomst, zoals één week vanaf nu. Dit is de datum en tijd wanneer de nieuwe kanbanregel actief wordt en de oude kanbanregel wordt vervangen.  
    * Als de kanbanregel het pad in de productiestroom wijzigt, kan een andere activiteit worden geselecteerd.  In deze procedure wordt de activiteit intact gehouden.  
3. Klik op OK.
    * Er wordt een nieuwe kanbanregel gemaakt om kanbanregel 000022 te vervangen.  
    * De ingangsdatum wordt ingesteld op basis van datum die is gekozen bij het vervangen van de kanbanregel.  
4. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de vervangen kanbanregel 000022.  
    * De vervangen kanbanregel heeft dezelfde datum als de vervaldatum omdat dit de datum is waarop deze vervalt.  
5. Selecteer rij 1 in de lijst.
    * Selecteer de nieuwe kanbanregel boven in de lijst. Dit is de kanbanregel met het hoogste kanbanregelnummer.  
6. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Klik op het kanbanregelnummer om de kanbanregel te openen.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Maximumhoeveelheid voor de vervangingskanbanregel wijzigen
1. Stel Maximumhoeveelheid in op '100'.
    * Vouw het sneltabblad Hoeveelheden uit om het veld Maximumhoeveelheid te bekijken. Als u de maximale hoeveelheid wijzigt in 100, kunnen maximaal 100 kanbans worden verwerkt.    Dit is de laatste stap in deze taak.  


