---
title: Kanbanprocestaken uitvoeren
description: Deze procedure is gericht op het uitvoeren van kanbanprocestaken.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bccee458ee48c51bdeeb64cee1f62aac9bdf4f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828533"
---
# <a name="execute-kanban-process-jobs"></a>Kanbanprocestaken uitvoeren

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op het uitvoeren van kanbanprocestaken. De eerste taak wordt voltooid met de verwachte hoeveelheid en heeft geen fouten. De tweede taak wordt voltooid met fouten. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de machineoperator.


## <a name="select-a-kanban-job"></a>Een kanbantaak selecteren
1. Ga naar Productiebeheer > Kanban > Kanbanplanbord voor procestaken.
2. Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik op de rij met resourcegroep 1250. Hiermee wordt de lijst met taken gefilterd zodat alleen de taken voor werkcel 1250 worden weergegeven.
    * Markeer de rij met de status Geplande taak.  

## <a name="complete-a-job-with-expected-quantity"></a>Een taak uitvoeren met verwachte hoeveelheid
1. Vouw de sectie Details uit of samen.
    * Deze sectie bevat belangrijke informatie over kaartnummer, artikelnummer, bestelde hoeveelheid en activiteitsnaam.  
2. Vouw de sectie Productie-instructies uit of samen.
    * Deze sectie bevat productie-instructies voor de activiteit. De instructies kunnen tekst, afbeeldingen, tekeningen en andere documenten zijn.  
3. Klik op Start.
    * Selecteer een taak die niet voltooid is. Gebruik statuspictogrammen in het veld Taakstatus om de taakstatus weer te geven.      
4. Klik op Voltooien.
    * De taak is voltooid met de verwachte kwaliteit.  

## <a name="complete-a-job-with-errors"></a>Een taak uitvoeren met fouten
1. Klik op Start.
    * Wanneer een taak is voltooid, wordt de volgende taak in de lijst automatisch geselecteerd. Om deze reden hoeft u geen taak te selecteren voordat u op Start klikt.  
2. Klik in het actievenster op Fabriceren.
3. Klik op Voltooien (details).
4. Markeer in de lijst de geselecteerde rij.
5. Voer in het veld Slechte hoeveelheid een getal in.
6. Voer in het veld Goede hoeveelheid een getal in.
7. Klik op OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]