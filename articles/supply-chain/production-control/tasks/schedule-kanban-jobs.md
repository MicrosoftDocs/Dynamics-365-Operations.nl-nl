---
title: Kanbantaken plannen
description: Deze procedure richt zich op het plannen van proceskanbantaken voor een specifieke werkcel.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5dc359309dd96d93a59fbfb6d0b0f64cfaddc5fa
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146578"
---
# <a name="schedule-kanban-jobs"></a>Kanbantaken plannen

[!include [banner](../../includes/banner.md)]

Deze procedure richt zich op het plannen van proceskanbantaken voor een specifieke werkcel. De procedure "Een proceskanbantaak voorbereiden wanneer de materialen niet beschikbaar zijn" is een vereiste voor het maken van deze procedure. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze taak is bedoeld voor de werkvloersupervisor en de productieplanner die met kanbans werken.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Kanbantaken selecteren voor een werkcel
1. Ga naar Productiebeheer > Kanban > Kanbantaakplanning.
2. Vouw het feitenvak Capaciteit van periode uit
    * Vouw het feitenvak Kanban uit.  
3. Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Markeer in de lijst de geselecteerde rij.
    * Selecteer werkcel 1250. Hiermee wordt de weergave gefilterd zodat alleen de taken voor werkcel 1250 worden weergegeven.  
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op Selecteren.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Een kanbantaak plannen tijdens de eerste beschikbare periode
1. Markeer in de lijst de geselecteerde rij.
    * Selecteer de eerste rij in de lijst die de status Niet gepland heeft. Het gestippelde pictogram in het veld Taakstatus geeft Niet gepland aan.  
2. Klik op Plannen.
    * Hiermee wordt de kanbantaak gepland tijdens de eerste beschikbare periode.  
    * Merk op dat de kanbantaak naar het einde van de lijst wordt verplaatst omdat deze is toegevoegd aan de periode die vanaf vandaag start.  
    * Als de periode die vandaag begint volledig is volgeboekt, wordt de taak naar de eerste beschikbare periode verplaatst.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Twee kanbantaken plannen voor een bepaalde dag
1. Selecteer rij 1 in de lijst.
    * U zult zien dat de eerste rij de status Niet gepland heeft in het veld Taakstatus.  
2. Selecteer rij 2 in de lijst.
    * U zult zien dat de tweede rij de status Niet gepland heeft in het veld Taakstatus. Nu hebt u de eerste twee taken geselecteerd.  
3. Klik op Plan vanaf datum om het dialoogvenster voor beëindigen te openen.
4. Schakel het selectievakje Overschrijf reactie bij capaciteitstekort in of uit.
    * Met deze optie kunt u de tekortreactie van de standaardcapaciteit negeren.  
5. Selecteer in het veld Capaciteitstekort de optie Toevoegen aan de aangevraagde periode.
    * Deze optie zorgt ervoor dat de taak wordt toegevoegd aan de aangevraagde periode ongeacht of de werkcel mogelijk overbelast is.  
6. Klik op Plannen.
    * Merk op dat beide taken zijn toegevoegd aan de gewenste periode.  
    * In de sectie Periodecapaciteit kunt u de belasting voor elke periode weergeven. Het veld Verbruik geeft het geplande verbruik tijdens deze periode aan. Als het geplande verbruik hoger is dan de beschikbare capaciteit tijdens deze periode, wordt het overbelaste verbruik geselecteerd.  

