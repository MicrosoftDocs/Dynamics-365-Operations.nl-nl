---
title: Kanbanstatus bijwerken
description: Wanneer een kanban per ongeluk is geleegd of als een ontvangen kanban moet worden leeggemaakt, moet u de kanbanstatus bijwerken.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 055765452579b1de74f1c2158de9c6cb4ee80f16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252817"
---
# <a name="update-kanban-status"></a>Kanbanstatus bijwerken

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]