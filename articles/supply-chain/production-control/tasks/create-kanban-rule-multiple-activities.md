---
title: Een kanbanregel maken voor meerdere activiteiten
description: Deze procedure laat zien hoe u een kanbanregel kunt maken die meerdere activiteiten van een productiestroom bevat.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c7be4e9da6f3dbaf2683c0dba78e0e780628f4b2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838650"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Een kanbanregel maken voor meerdere activiteiten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een kanbanregel kunt maken die meerdere activiteiten van een productiestroom bevat. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF. Deze taak is bedoeld voor de procestechnicus of de waardestroombeheerder bij het voorbereiden van de productie van een nieuw of gewijzigd product in een lean-omgeving.


## <a name="create-a-new-kanban-rule"></a>Een nieuwe kanbanregel maken
1. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.
2. Klik op Nieuw.
3. Selecteer 'Gepland' in het veld Aanvullingsstrategie.
4. Typ of selecteer een waarde in het veld Eerste planactiviteit.
    * Selecteer SpeakerAssemblyAndPolish.  
5. Schakel het selectievakje Meerdere activiteiten in.
    * Het doel is meer dan één activiteit in de kanbanregel op te nemen. U kiest een pad in de productiestroom wanneer u de laatste planactiviteit selecteert.  
6. Typ of selecteer een waarde in het veld Laatste planactiviteit.
    * Selecteer SpeakerTestAndPackaging. Nadat u de waarde hebt geselecteerd, wordt automatisch een pagina geopend. Selecteer de kanbanwerkstroom SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Klik op OK.  
7. Vouw de sectie Details uit.
8. Typ of selecteer een waarde in het veld Product.
    * Selecteer artikel L0006.  

## <a name="create-kanban-and-view-jobs"></a>Kanban maken en taken weergeven
1. Vouw de sectie Kanbans uit.
2. Klik op Toevoegen.
3. Typ '1' in het veld Aantal nieuwe kanbans.
    * Hierdoor wordt één kanban gemaakt.  
4. Stel Producthoeveelheid in op "3".
    * Door de kanban worden 3 producten verwerkt.  
5. Typ een datum en tijd in het veld Vervaldatum/-tijd.
    * U kunt Vandaag invoeren.  
6. Klik op Maken.
7. Klik op Details.
    * Merk op dat de kanban twee procestaken van de productiestroom bevat. De eerste is SpeakerAssemblyAndPolish, en de tweede is SpeakerTestAndPackaging.  
    * Dit is de laatste stap.  

