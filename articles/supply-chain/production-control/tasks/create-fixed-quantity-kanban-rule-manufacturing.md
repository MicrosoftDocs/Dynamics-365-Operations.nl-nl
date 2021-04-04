---
title: Een kanbanregel met vaste hoeveelheid maken voor productie
description: Deze procedure is gericht op de instellingen die nodig is om een vaste kanbanregel voor fabricage te maken om de omzetting van activiteiten, in een werkcel, in lean omgeving te activeren.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 540df772f132f60c9d8e7e937e72d3f51f6759ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255248"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Een kanbanregel met vaste hoeveelheid maken voor productie

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op de instellingen die nodig is om een vaste kanbanregel voor fabricage te maken om de omzetting van activiteiten, in een werkcel, in lean omgeving te activeren. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de Procesingenieur of de Waardestroombeheerder, want zij bereiden de productie van een nieuw of gewijzigd product voor.


## <a name="create-new-kanban-rule"></a>Nieuwe kanbanregel maken
1. Ga naar Kanbanregels.
2. Klik op Nieuw.
    * Het standaardtype is Productie en de Aanvullingsstrategie is Vast. U moet deze parameters niet wijzigen.  
3. Typ of selecteer een waarde in het veld Eerste planactiviteit.
    * Dit is de activiteit die wordt uitgevoerd voor kanbans die op basis van deze kanbanregel zijn gemaakt.  Selecteer 'SpeakerTestAndPackaging'.  
4. Vouw de sectie Details uit.
5. Typ of selecteer een waarde in het veld Product.
    * Selecteer L0050.  
6. Typ of selecteer een waarde in het veld Maateenheid.
    * Selecteer minuten.  
7. Voer in het veld Levertijd een nummer in.
    * Voer 5 in.  

## <a name="set-quantities"></a>Hoeveelheden instellen
1. Vouw de sectie Hoeveelheden uit.
2. Stel Standaardhoeveelheid in op '10'.
    * Dit is de hoeveelheid die voor elke kanban wordt overgeboekt.  
3. Schakel het selectievakje Afwijking producthoeveelheid in.
    * Hiermee kunnen de geselecteerde kanbans worden voltooid met een afwijking van de standaardhoeveelheid.  Om toe te staan dat kanbans worden voltooid met een hoeveelheid van 8 tot 12, stelt u beide afwijkingen in op 2.  
4. Stel Afwijking onder in op '2'.
    * Hierdoor is het mogelijk om minimaal 10 - 2 = 8 te voltooien  
5. Stel Afwijking boven in op '2'.
    * Hierdoor is het mogelijk om maximaal 10 + 2 = 12 te voltooien  
6. Typ een getal in het veld Vaste kanbanhoeveelheid.
    * Dit is het aantal kanbans die actief moeten zijn. In dit geval verwerken 5 kanbans elk 10.  
7. Typ '2' in het veld Minimum waarschuwingsgrens.
    * Gebruikt om het minimumaantal van volledige kanbans bij te houden die bij de bestemming moeten zijn. Dit wordt bijvoorbeeld gebruikt op het overzicht van kanbanhoeveelheid.  
8. Typ '4' in het veld Maximum waarschuwingsgrens.
    * Gebruikt om het maximumaantal van volledige kanbans bij te houden die bij de bestemming moeten zijn. Dit wordt bijvoorbeeld gebruikt op het overzicht van kanbanhoeveelheid.  
9. Typ '1' in het veld Automatische planningshoeveelheid.
    * Als u dit op 1 instelt, wordt elke kanban automatisch ingepland.   Als u 3 invoert, worden de kanbans niet gepland tot er 3 lege kanbans klaar zijn voor planning. Dit is nuttig voor het groeperen van het werk en het voorkomen van te veel instellingen.  

## <a name="create-kanbans"></a>Kanbans maken
1. Vouw de sectie Kanbans uit.
2. Klik op Opslaan.
    * De kanbanregel moet worden opgeslagen voordat kanbans kunnen worden gemaakt.  
3. Klik op Toevoegen.
    * Houd er rekening mee dat er geen actieve kanbans zijn. Als gevolg hiervan is het voorgestelde 'Aantal nieuwe kanbans' 5. Dit is gelijk aan de Vaste kanbanhoeveelheid.  
4. Klik op Maken.
    * Hierdoor worden 5 kanbans gemaakt.  
    * Voor deze kanbanregel zijn werden er 5 kanbans gemaakt, voor elk 10. Dit is de laatste stap in deze procedure.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]