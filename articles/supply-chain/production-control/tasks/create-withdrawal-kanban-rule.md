---
title: Een opnamekanbanregel maken
description: Deze procedure toont de instellingen die nodig zijn om een kanbanregel voor opname te maken om materiaal in een lean-omgeving over te boeken.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba30e9d09e9eeb0cd7428aafc1195d6b7e7caaa4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574468"
---
# <a name="create-a-withdrawal-kanban-rule"></a>Een opnamekanbanregel maken

[!include [banner](../../includes/banner.md)]

Deze procedure toont de instellingen die nodig zijn om een kanbanregel voor opname te maken om materiaal in een lean-omgeving over te boeken. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de Procesingenieur of de Waardestroombeheerder, want zij bereiden de aanvulling van nieuw of gewijzigd materiaal voor.


## <a name="create-new-kanban-rule"></a>Nieuwe kanbanregel maken
1. Ga naar Kanbanregels.
2. Klik op Nieuw.
3. Selecteer Opname in het veld Type.
    * Het opnametype wordt gebruikt voor kanbanregels om materiaal of goederen over te boeken.  
4. Typ of selecteer een waarde in het veld Eerste planactiviteit.
    * Selecteer ReplenishSpeakerComponents.   Deze activiteit wordt ingesteld om onderdelen van magazijn 11, locatie 11 naar magazijn 12 en locatie 12 te verplaatsen.  
5. Typ of selecteer een waarde in het veld Product.
    * Selecteer M0007.  
6. Voer in het veld Levertijd een nummer in.
    * Bijvoorbeeld 60.  
7. Typ of selecteer een waarde in het veld Maateenheid.
    * Bijvoorbeeld Minuten.  

## <a name="set-quantities-for-kanban"></a>Hoeveelheden voor kanban instellen
1. Stel Standaardhoeveelheid in op '5'.
    * Dit is de hoeveelheid die voor elke kanban wordt overgeboekt.  
2. Voer 2 in het veld Vaste kanbanhoeveelheid in.
    * Dit is het aantal kanbans die actief moeten zijn. In dit geval 2 kanbans die elk 5 overboeken.  
3. Typ '1' in het veld Minimum waarschuwingsgrens.
    * Gebruikt om het minimumaantal van volledige kanbans bij te houden die bij de bestemming moeten zijn. Dit wordt bijvoorbeeld gebruikt op het overzicht van kanbanhoeveelheid.  
4. Typ '2' in het veld Maximum waarschuwingsgrens.
    * Gebruikt om het maximumaantal van volledige kanbans bij te houden die bij de bestemming moeten zijn. Dit wordt bijvoorbeeld gebruikt op het overzicht van kanbanhoeveelheid.  

## <a name="create-kanbans"></a>Kanbans maken
1. Klik op Opslaan.
    * De kanbanregel moet worden opgeslagen voordat kanbans kunnen worden gemaakt.  
2. Klik op Toevoegen.
    * Er zijn geen actieve kanbans, omdat het voorgestelde 'Aantal nieuwe kanbans' 2 is. Dit is gelijk aan de 'Vaste kanbanhoeveelheid'.  
3. Klik op Maken.
    * Hierdoor worden twee kanbans gemaakt.  
    * Voor deze opnamekanbanregel werden er 2 kanbans gemaakt, voor elk 5.  Dit is de laatste stap in deze procedure.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]