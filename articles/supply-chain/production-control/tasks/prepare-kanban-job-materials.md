---
title: Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn
description: Deze taak richt zich op het voorbereiden van een proceskanbantaak wanneer alle materialen voor de werkcel beschikbaar zijn.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf163968474e91da7e3d47fd638a857a76179645
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148960"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a>Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn

[!include [banner](../../includes/banner.md)]

Deze taak richt zich op het voorbereiden van een proceskanbantaak wanneer alle materialen voor de werkcel beschikbaar zijn. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF. Deze taak is bedoeld voor de machineoperator.

1. Ga naar Kanbanplanbord voor procestaken.
2. Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer werkcel 1250 en klik op OK.  
4. Selecteer rij 4 in de lijst.
    * In het schone demobedrijf, is Kanban 000329 in rij 4 de eerste taak die nog niet is voltooid.  
5. Schakel de uitbreiding van de sectie Orderverzamellijst om.
    * Controleer of de voorraadstatus beschikbaar is voor alle artikelen in de orderverzamellijst.  
    * Als meerdere taken zijn geselecteerd, geeft de orderverzamellijst de som weer van alle artikelen die nodig zijn voor de geselecteerde taken.  
6. Klik op Voorbereiden.
    * Het voorbereidingsproces wordt nu voltooid. Het ingeschakelde selectievakje voor alle rijen in de orderverzamellijst geeft aan dat de voorraadstatus wordt verzameld.  

