--- 
title: Geplande kanbantaken verplaatsen
description: Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a>Geplande kanbantaken verplaatsen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de werkvloersupervisor of de productieplanner die met kanbans werken.


## <a name="select-scheduled-kanban-jobs"></a>Geplande kanbantaken selecteren
1. Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.
2. !MtCMR!Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen. áçêìõý !
3. Markér den valgte række på listen.
    * Selecteer werkcel 1250.  
4. Klik på Select.
5. Vælg 'Planlagt' i feltet Display job status.
    * Hiermee wordt de takenlijst gefilterd om alleen de geplande kanbantaken weer te geven.  

## <a name="move-kanban-jobs-to-a-different-period"></a>Kanbantaken verplaatsen naar een andere periode
1. Find og vælg den ønskede post på listen.
    * Selecteer een taak met de taakstatus Gepland, bijvoorbeeld een taak die is gepland op 20 december 2012 in het veld Geplande periode. Verplaats vervolgens de taak naar de vorige periode.  
2. Klik på Previous period.
3. Klik på End.
    * Hiermee wordt de taak naar het einde van de takenlijst verplaatst als laatste taak in de vorige periode.  
4. Find og vælg den ønskede post på listen.
    * Selecteer een taak met de taakstatus Gepland, bijvoorbeeld een taak die is gepland op 18 december 2012 in het veld Geplande periode. Verplaats vervolgens de taak naar de volgende periode.  
5. Klik på Next period.
6. Klik på Start.
    * Hiermee wordt de taak naar het begin van de takenlijst verplaatst als eerste taak in de vorige periode.  

## <a name="task-move-a-job-within-a-period"></a>Taak: Een taak binnen een periode verplaatsen
1. Find og vælg den ønskede post på listen.
    * Selecteer een taak met de taakstatus Gepland, bijvoorbeeld de tweede taak die is gepland op 19 december 2012 in het veld Geplande periode. Verplaats vervolgens de taak binnen de geplande periode.  
2. Klik på Forward.
    * Merk op dat de taak één regel omlaag in de lijst wordt verplaatst.  
3. Klik på Backward.
    * Merk op dat de taak één regel omhoog in de lijst wordt verplaatst.  


