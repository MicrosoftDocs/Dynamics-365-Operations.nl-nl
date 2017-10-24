--- 
title: Kanbanstatus bijwerken
description: Wanneer een kanban per ongeluk is geleegd of als een ontvangen kanban moet worden leeggemaakt, moet u de kanbanstatus bijwerken.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3c2b5a5fbfc5bd83cc68ffafaa243dac9244c003
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="update-kanban-status"></a>Kanbanstatus bijwerken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Wanneer een kanban per ongeluk is geleegd of als een ontvangen kanban moet worden leeggemaakt, moet u de kanbanstatus bijwerken. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de winkelchef.


## <a name="find-the-kanban"></a>Zoek de kanban.
1. Ga naar Productiebeheer > Kanban > Kanbans.
2. Open de kolomfilter Status materiaalverwerkingseenheid.
3. Klik op Wissen.
    * Hiermee worden de filters opnieuw ingesteld.  
4. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Kaartnummer met een waarde van '000149'.

## <a name="change-emptied-status-to-received-status"></a>Status Geleegd in Ontvangen wijzigen
1. Klik op Omgekeerde lege materiaalverwerkingseenheid.
2. Klik op OK.
    * De status van de materiaalverwerkingseenheid is Ontvangen.  

## <a name="change-received-status-to-emptied-status"></a>Status Ontvangen in Geleegd wijzigen
1. Klik op Lege Kanban.
2. Markeer in de lijst de geselecteerde rij.
    * De status van de materiaalverwerkingseenheid is Geleegd.  


