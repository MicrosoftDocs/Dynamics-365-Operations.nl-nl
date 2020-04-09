---
title: Een kanbanregel voor gebeurtenis stuklijstregel maken
description: Deze taak is gericht op de instellingen die nodig zijn om een gebeurteniskanbanregel te maken om te zorgen voor levering voor BOM-productiestuklijstregels in een gemengde lean- en klassieke productieomgeving.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fefb33d568153670dbcb92db478e33db806809fc
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147085"
---
# <a name="create-a-bom-line-event-kanban-rule"></a>Een kanbanregel voor gebeurtenis stuklijstregel maken

[!include [banner](../../includes/banner.md)]

Deze taak is gericht op de instellingen die nodig zijn om een gebeurteniskanbanregel te maken om te zorgen voor levering voor BOM-productiestuklijstregels in een gemengde lean- en klassieke productieomgeving. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF. Deze taak is bedoeld voor de procesingenieur of de waardestroombeheerder, want zij bereiden de productie van een nieuw of gewijzigd product voor.


## <a name="create-a-new-kanban-rule"></a>Een nieuwe kanbanregel maken
1. Ga naar Productiebeheer > Periodieke taken > Berekening kanbanhoeveelheid > Kanbanregels.
2. Klik op Nieuw.
3. Selecteer Opname in het veld Type.
    * Het opnametype wordt gebruikt om overboekingskanbans te maken.  
4. Selecteer 'Gebeurtenis' in het veld Aanvullingsstrategie.
    * De gebeurtenisstrategie wordt geselecteerd om de overboeking van kanbans op basis van een gebeurtenis te maken. Later in de taakbegeleiding wordt dit geactiveerd door een productieorder te ramen.  
5. Typ of selecteer een waarde in het veld Eerste planactiviteit.
    * Typ of selecteer ReplenishSpeakerComponents. Deze overboekingsactiviteit heeft magazijn en locatie 12 voor ontvangst (uitvoer), wat betekent dat materiaal naar locatie 12 in magazijn 12 wordt verplaatst.  
6. Vouw de sectie Details uit.
7. Typ of selecteer M0001 in het veld Product.
8. Vouw de sectie Gebeurtenissen uit.
9. Selecteer 'Automatisch' in het veld Stuklijstgebeurtenis.
    * Met het veld Stuklijstregelgebeurtenis ingesteld op Automatisch wordt de kanban gemaakt om aan de materiaalvereisten voor productieorderstuklijstregels te voldoen.  
10. Sluit de pagina.

## <a name="create-and-modify-a-new-production-order"></a>Een nieuwe productieorder maken en wijzigen
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
2. Klik op Nieuwe productieorder.
3. Typ of selecteer een waarde in het veld Artikelnummer.
    * Typ of selecteer 'L0001'. Artikel L0001 wordt gebruikt omdat artikel M0001 in de stuklijst voor artikel L0001 is opgenomen.  
4. Klik op Maken.
5. Klik in de lijst op de koppeling in de rij voor L0001.
6. Klik op Stuklijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik op Bewerken.
9. Selecteer 'Getraceerd aanbod' in het veld Regeltype.
    * Getraceerd aanbod wordt geselecteerd om het maken van aanbod van een kanban te activeren.  
10. Selecteer Nee in het veld Resourceverbruik.
    * Als het selectievakje Resourceverbruik wordt uitgeschakeld, kan het magazijn worden gewijzigd.  
11. Vouw de sectie Voorraaddimensies uit.
12. Typ "12" in het veld Magazijn.
    * Het magazijn is ingesteld op 12 omdat dit het uitvoermagazijn voor de opnameactiviteit is.  
13. Typ 12 in het veld Locatie.
    * Locatie is ingesteld op 12 omdat dit de uitvoerlocatie van de opnameactiviteit is.  
14. Sluit de pagina.
15. Sluit de pagina.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Een schatting maken van de productieorder en de gemaakte kanban weergeven
1. Klik op Raming.
    * Door de productieorder te ramen wordt het maken van de gekoppelde kanban geactiveerd om artikel M0001 te leveren.  
2. Klik op OK.
3. Sluit de pagina.
4. Sluit de pagina.
5. Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer de gebeurteniskanbanregel die is gemaakt voor artikel M0001.  
7. Vouw de sectie Kanbans uit.
8. Markeer in de lijst de geselecteerde rij.
    * Let op de kanban die is gemaakt om M0001 te leveren voor de geschatte productieorder.  
    * Dit is de laatste stap.  

