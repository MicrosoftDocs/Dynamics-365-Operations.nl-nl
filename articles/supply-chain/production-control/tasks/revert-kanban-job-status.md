---
title: Kanbantaakstatus terugdraaien
description: Deze procedure is gericht op het terugdraaien van een onjuiste kanbantaakstatus.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cca5ea3a4c33c7f36acd18a8af7034466b3b580
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425405"
---
# <a name="revert-kanban-job-status"></a>Kanbantaakstatus terugdraaien

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op het terugdraaien van een onjuiste kanbantaakstatus. Dit is handig in het geval dat de machineoperator per ongeluk de verkeerde taak bijwerkt of de verkeerde status instelt. In deze procedure wordt een kanbantaak per ongeluk als Voorbereid geregistreerd en wordt de status teruggedraaid. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de winkelsupervisor of machineoperator die in een lean manufacturingbedrijf werkt.


## <a name="open-process-board-for-the-work-cell"></a>Verwerkingsbord voor de werkcel openen
1. Ga naar Kanbanplanbord voor procestaken.
2. Typ of selecteer een waarde in het veld Werkcel.
    * Selecteer werkcel 1260.  

## <a name="prepare-kanban-job"></a>Kanbantaak voorbereiden
1. Klik op Voorbereiden.
    * Als u niet op Voorbereiden kunt klikken omdat dit grijs is, moet u ervoor zorgen dat de geselecteerde kanbantaak de status Gepland heeft, wat wordt aangeduid door het lege kanbanpictogram. Als Voorbereiden mislukt, moet u ervoor zorgen dat alle materialen in de Orderverzamellijst beschikbaar zijn.  
2. Selecteer de voorbereide taak in de lijst.
    * Selecteer de eerste taak die u zojuist hebt voorbereid.  
    * De takenstatus is voorbereid, wat wordt aangeduid door een driehoek in het kanbanpictogram.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>De status van de voorbereide kanbantaak herstellen
1. Markeer in de lijst de geselecteerde rij.
    * Selecteer de eerste taak die was voorbereid.  
2. Klik in het actievenster op Fabriceren.
3. Klik op Status herstellen
    * U kunt een andere kanbanregel gebruiken wanneer aan de volgende voorwaarden wordt voldaan: - De aanvullingsstrategie is dezelfde voor beide regels.  - De versie van de productiestroom is dezelfde voor beide regels.  - Het product dat is geleverd is hetzelfde voor beide regels.  - Eventuele downstream activiteiten die voor de laatste activiteit van de kanbanregels zijn geconfigureerd, moeten dezelfde zijn voor beide regels.  - Dezelfde geleverde voorraaddimensies moeten voor beide regels zijn geconfigureerd.  - De status van de verwerkingseenheid moet Niet toegewezen zijn.  - De configuratie voor gebeurteniskanbans moet dezelfde zijn.  
    * Zorg ervoor dat de nieuwe status Gepland is.  
4. Klik op OK.
5. Maak in de lijst de markering van de geselecteerde rij ongedaan.
    * Selecteer dezelfde taak.  
    * De taakstatus voor de kanbantaak is terug Gepland, wat wordt aangeduid door een leeg kanbanpictogram.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]