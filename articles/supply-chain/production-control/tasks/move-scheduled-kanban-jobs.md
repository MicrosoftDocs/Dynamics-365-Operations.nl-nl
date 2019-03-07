---
title: Geplande kanbantaken verplaatsen
description: Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f791c9048ef6efe1585c991f998099cd1fc12df7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "310847"
---
# <a name="move-scheduled-kanban-jobs"></a>Geplande kanbantaken verplaatsen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure is gericht bij het verplaatsen van geplande proceskanbantaken naar een andere periode. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de werkvloersupervisor of de productieplanner die met kanbans werken.

## <a name="select-scheduled-kanban-jobs"></a>Selecteer geplande kanbantaken. 

1. Ga naar **Productiebeheer > Kanban > Kanbantaakplanning**. 

2. Klik in het veld **Werkcel** op de vervolgkeuzeknop om de zoekopdracht te openen. 

3. Markeer in de lijst de geselecteerde rij. 
   - Selecteer werkcel 1250. 
4. Klik op **Selecteren**. 

5. Selecteer in het veld **Taakstatus weergeven** de optie **Gepland**. Hiermee wordt de takenlijst gefilterd om alleen de geplande kanbantaken weer te geven. 

## <a name="move-kanban-jobs-to-a-different-period"></a>Verplaats kanbantaken naar een andere periode. 

1. Zoek en selecteer de gewenste record in de lijst. Selecteer een taak met de status **Geplande taak**, bijvoorbeeld een taak die is gepland op 20 december 2012 in het veld **Geplande periode**. Verplaats vervolgens de taak naar de vorige periode. 

2. Klik op **Vorige periode**. 

3. Klik op **Einde** om de taak naar het einde van de takenlijst te verplaatsen als laatste taak in de vorige periode. 

4. Zoek en selecteer de gewenste record in de lijst. Selecteer een taak met de status **Geplande taak**, bijvoorbeeld een taak die is gepland op 18 december 2012 in het veld **Geplande periode**. Verplaats vervolgens de taak naar de volgende periode. 

5. Klik op **Volgende periode**. 

6. Klik op **Begin** om de taak naar het begin van de takenlijst te verplaatsen als eerste taak in de vorige periode. 

## <a name="move-a-job-within-a-period"></a>Verplaats een taak binnen een periode. 

1. Zoek en selecteer de gewenste record in de lijst. Selecteer een taak met de status Geplande taak, bijvoorbeeld de tweede taak die is gepland op 19 december 2012 in het veld **Geplande periode**. Verplaats vervolgens de taak binnen de geplande periode. 

2. Klik op **Vooruit**. Merk op dat de taak één regel omlaag in de lijst wordt verplaatst. 

3. Klik op **Achteruit**. Merk op dat de taak één regel omhoog in de lijst wordt verplaatst.
