---
title: Een kanbanregel maken met een gebeurtenis minimale voorraad
description: Deze procedure is gericht op de instellingen die nodig zijn om een kanbanregel te maken met een minimumvoorraadgebeurtenis om ervoor te zorgen dat een specifiek product altijd beschikbaar is op een specifieke locatie.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd7e02a8a3bf62606c680dad91d46658775138df
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566618"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Een kanbanregel maken met een gebeurtenis minimale voorraad

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op de instellingen die nodig zijn om een kanbanregel te maken met een minimumvoorraadgebeurtenis om ervoor te zorgen dat een specifiek product altijd beschikbaar is op een specifieke locatie. Er wordt een kanbanregel gemaakt om materiaal naar de locatie over te dragen wanneer het voorraadniveau tot onder de 200 stuks daalt. Door de verwerking van gebeurtenissen voor tracering van de behoefte uit te voeren, worden de benodigde kanbans gemaakt. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF. Deze taak is bedoeld voor de procestechnicus of de waardestroombeheerder bij het voorbereiden van de productie van een nieuw of gewijzigd product in een lean-omgeving.


## <a name="create-a-new-kanban-rule"></a>Een nieuwe kanbanregel maken
1. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.
2. Klik op Nieuw.
3. Selecteer Opname in het veld Type.
    * Dit type wordt gebruikt om overboekingskanbans te maken.  
4. Selecteer 'Gebeurtenis' in het veld Aanvullingsstrategie.
    * De gebeurtenisstrategie wordt gebruikt voor het maken van overboekingskanbans op basis van een gebeurtenis. Later in de procedure activeert u overboekingskanbans door voorraadaanvulling te gebruiken.  
5. Typ of selecteer een waarde in het veld Eerste planactiviteit.
    * Typ of selecteer ReplenishSpeakerComponents. Deze overboekingsactiviteit heeft magazijn en locatie 12 voor ontvangst (uitvoer), wat betekent dat materialen naar locatie 12 in magazijn 12 worden verplaatst.  
6. Vouw de sectie Details uit.
7. Typ of selecteer een waarde in het veld Product.
    * Selecteer M0007.  
8. Vouw de sectie Gebeurtenissen uit.
9. Selecteer 'Batch' in het veld Voorraadaanvullingsgebeurtenis.
    * Hiermee worden kanbans gemaakt om te voldoen materiaalbehoeften op de gerelateerde locatie tijdens de verwerking van gebeurtenissen voor tracering van de behoefte.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Stel de minimumhoeveelheid voor het artikel in.
1. Klik in het veld Product om de koppeling te volgen.
2. Klik om de koppeling in het veld Artikelnummer te volgen.
3. Vouw het feitenvak Productafbeelding uit.
4. Klik in het actievenster op Plannen.
5. Klik op Artikelbehoefteplanning.
6. Klik op Nieuw.
7. Markeer in de lijst de geselecteerde rij.
8. Typ of selecteer een waarde in het veld Magazijn.
    * Stel Magazijn in op 12.  
9. Stel Minimum in op '200'.

## <a name="run-the-batch-event-creation-job"></a>De taak voor het maken van een batchgebeurtenis uitvoeren
1. Ga naar Productiebeheer > Periodieke taken > Batchverwerking van kanbantaak > Verwerking van gebeurtenis voor tracering van de behoefte.
2. Klik op OK.
3. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer de kanbanregel die u eerder hebt gemaakt.  
5. Vouw de sectie Kanbans uit.
    * Merk op dat een kanban is gemaakt om het benodigde materiaal over te dragen naar magazijn 12.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]