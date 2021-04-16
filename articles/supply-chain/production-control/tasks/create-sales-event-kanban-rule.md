---
title: Een kanbanregel voor verkoopgebeurtenis maken
description: Deze procedure is gericht op de instellingen die nodig is voor het maken van een kanbanregel die tijdens het maken van een verkooporder wordt geactiveerd.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9325bbb8d28587baeb60cdf1fc37121c236f1a10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828917"
---
# <a name="create-a-sales-event-kanban-rule"></a>Een kanbanregel voor verkoopgebeurtenis maken

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op de instellingen die nodig is voor het maken van een kanbanregel die tijdens het maken van een verkooporder wordt geactiveerd. De gebeurteniskanbanregel vult de vereisten aan die afkomstig zijn uit van verkooporderregels. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de procesingenieur of de waardestroombeheerder, want zij bereiden de productie van een nieuw of gewijzigd product voor.




## <a name="create-a-new-kanban-rule"></a>Een nieuwe kanbanregel maken
1. Ga naar Kanbanregels.
2. Klik op Nieuw.
3. Selecteer 'Gebeurtenis' in het veld Aanvullingsstrategie.
    * Door het selecteren van Gebeurtenis wordt de kanbanregel geactiveerd door een gebeurtenis, bijvoorbeeld, het maken van een verkooporderregel.   Dit wordt toegepast op gebieden waarin elke kanban de specifieke vraag moet verwerken.  
4. Typ of selecteer een waarde in het veld Eerste planactiviteit.
    * Selecteer Definitieve assemblage.  
5. Vouw de sectie Details uit.
6. Typ of selecteer een waarde in het veld Product.
    * Selecteer L0050.  

## <a name="define-an-event"></a>Een gebeurtenis definiëren
1. Vouw de sectie Gebeurtenissen uit.
2. Selecteer 'Automatisch' in het veld Verkoopgebeurtenis.
    * Door de verkoopgebeurtenis Automatisch te selecteren, wordt deze kanbanregel automatisch geactiveerd wanneer een verkoopregel overeenkomt met het product en de ontvangstlocatie. In deze procedure is dit product L0050 in magazijn 13.  
3. Stel Minimale gebeurtenishoeveelheid in op '50'.
    * Met een minimale gebeurtenishoeveelheid van 50 wordt de kanbanregel alleen geactiveerd door gebeurtenissen met een hoeveelheid van 50 of meer.  
4. Vouw de sectie Productiestroom uit.
    * De Ontvangstlocatie is magazijn 13. Dit betekent dat deze kanbanregel voor deze locatie zal worden geactiveerd.  
    * In dit voorbeeld zal een verkoopregel voor product L0050, met een hoeveelheid van 50 of meer, in magazijn 13, deze kanbanregel activeren.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Een verkoopregel maken om een gebeurteniskanbanregel te activeren
1. Ga naar Alle verkooporders.
    * Er wordt een waarschuwing weergegeven wanneer de kanbanregel is opgeslagen, wat aangeeft dat de kanbans in realtime worden gemaakt tijdens het maken van de verkooporder.  
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Klantrekening.
    * Selecteer bijvoorbeeld US-003.  
4. Klik op OK.
5. Typ in het veld Artikelnummer de waarde 'L0050'.
6. Typ '1' in het veld Locatie.
    * Selecteer Site 1 omdat Magazijn 13 in Locatie 1 is.  
7. Typ of selecteer een waarde in het veld Magazijn.
    * Stel Magazijn in op 13.  
8. Stel Hoeveelheid in op '75'.
    * Voer een hoeveelheid van 50 of meer in om de gemaakte kanbanregel te activeren.  

## <a name="verify-that-kanban-is-created"></a>Controleer of de kanban is gemaakt
1. Klik op Product en voorraad.
2. Klik op Behoeftetraceringsstructuur weergeven.
    * Er wordt een kanban gemaakt met dezelfde hoeveelheid als de verkoopregel. U kunt ook de materiaaluitgiften zien die nodig zijn om L0050 te produceren. Dit is de laatste stap in deze procedure.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]