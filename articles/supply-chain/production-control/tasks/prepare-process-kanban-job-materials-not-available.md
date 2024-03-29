---
title: Een proceskanbantaak voorbereiden wanneer de materialen niet beschikbaar zijn voor de werkcel
description: Deze procedure is gericht op het voorbereiden van een proceskanbantaak wanneer bepaalde materialen niet beschikbaar zijn voor de werkcel. Daarom is het noodzakelijk om materialen in het magazijn te verzamelen.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f75cdbc6ce6f7e427bf266c90428d73c065eac3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576731"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Een proceskanbantaak voorbereiden wanneer de materialen niet beschikbaar zijn voor de werkcel

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op het voorbereiden van een proceskanbantaak wanneer bepaalde materialen niet beschikbaar zijn voor de werkcel. Daarom is het noodzakelijk om materialen in het magazijn te verzamelen. De procedure "Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn" is een vereiste voor het maken van deze procedure. Deze procedure is bedoeld voor de machineoperator. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.

1. Ga naar Productiebeheer > Kanban > Kanbanplanbord voor procestaken.
2. Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer werkcel 1250.  
4. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer Kanban 000356.  
5. Zoek en selecteer de gewenste record in de lijst.
    * Heft de selectie van rij 4 in de lijst op. Of selecteer rij 4 als u de taak "Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn" niet hebt voltooid.  
6. Schakel de uitbreiding van de sectie Orderverzamellijst om.
    * Het pictogram Geen vermelding in de aanbodstatus geeft aan dat 48 ea van artikel P0002 ontbreken voor de werkcel.  

## <a name="transfer-materials-to-work-cell"></a>Materialen overboeken naar werkcel
1. Schakel de uitbreiding van de sectie Overboekingstaken om.
2. Gebruik het snelfilter om te filteren op het veld Artikelnummer met de waarde 'P0002'.
3. Zoek en selecteer de gewenste record in de lijst.
4. Klik op Start.
    * Bezig met overboeken.  
5. Klik op Voltooien.
    * Het artikel P0002 is nu beschikbaar in de orderverzamellijst voor de kanbantaak. Dit betekent dat we de kanban kunnen voorbereiden met alle benodigde materialen.  
6. Klik op Voorbereiden.
    * Merk op dat een pictogram in de Taakstatus aangeeft dat de taak nu gereed is.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]