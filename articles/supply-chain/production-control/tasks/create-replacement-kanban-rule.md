---
title: Een vervangende kanbanregel maken
description: Deze procedure is gericht op het vervangen van een bestaande kanbanregel met een nieuwe kanbanregel op een specifieke datum.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2db44c1b43a6dc5e0ab37a7756c4eecaab468e15
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570052"
---
# <a name="create-a-replacement-kanban-rule"></a>Een vervangende kanbanregel maken

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]