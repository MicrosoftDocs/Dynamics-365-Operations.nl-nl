--- 
title: Kanbanprocestaken uitvoeren
description: Deze procedure is gericht op het uitvoeren van kanbanprocestaken.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 752eab976f740606154d416678ba2381641697df
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="execute-kanban-process-jobs"></a>Kanbanprocestaken uitvoeren

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


