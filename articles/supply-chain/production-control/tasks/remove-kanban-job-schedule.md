---
title: Een kanbantaak uit de planning verwijderen
description: Deze procedure richt zich op het verwijderen van een geplande proceskanbantaak uit de planning door de taakstatus terug te zetten op Niet gepland.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcd9247e24323ba606377d7e51bd4447ab51c905
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961610"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Een kanbantaak uit de planning verwijderen

[!include [banner](../../includes/banner.md)]

Deze procedure richt zich op het verwijderen van een geplande proceskanbantaak uit de planning door de taakstatus terug te zetten op Niet gepland. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de werkvloersupervisor of de productieplanner.


## <a name="find-a-planned-kanban-job"></a>Een geplande kanbantaak zoeken
1. Ga naar Productiebeheer > Kanban > Kanbantaakplanning.
2. Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer werkcel 1250.  
4. Klik op Selecteren.
5. Selecteer in het veld Taakstatus weergeven de optie Gepland.

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>De geplande kanbantaak uit de planning verwijderen
1. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer een taak met de status Gepland, bijvoorbeeld een taak van 19 december 2012.  
2. Klik in het actievenster op Plannen.
3. Klik op Taakstatus terugdraaien
4. Klik op OK.
    * Hiermee wordt de huidige taakstatus teruggedraaid van Gepland naar Niet-gepland en wordt de taak verwijderd van het verwerkingsbord.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]