---
title: Kanbanstatus bijwerken
description: Wanneer een kanban per ongeluk is geleegd of als een ontvangen kanban moet worden leeggemaakt, moet u de kanbanstatus bijwerken.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97b6eea4e93967dbe1eea5eac9fe3fbf6b336a49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838458"
---
# <a name="update-kanban-status"></a>Kanbanstatus bijwerken

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

