--- 
title: Materialen overboeken met kanbantaken (uitsluitend februari 2016)
description: Deze procedure richt zich op het uitvoeren van een opnamekanbantaak om materialen te boeken.
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
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
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 72403aa502cadf2a727bdd67ad8cd612dafd502b
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a>Materialen overboeken met kanbantaken (uitsluitend februari 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure richt zich op het uitvoeren van een opnamekanbantaak om materialen te boeken. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de magazijnmedewerker.


## <a name="display-transfer-jobs"></a>Overboekingstaken weergeven
1. Ga naar Productiebeheer > Kanban > Kanbanbord voor overboekingstaken.
2. Vouw de sectie Filters uit of samen.
    * In de sectie Filters kunt u opgeven welke taken u wilt weergeven door op Productiestroom, Activiteitsnaam Van magazijn en locatie en Naar magazijn en locatie te filteren.  
3. Typ "11" in het veld Van magazijn.
4. Typ "12" in het veld Naar locatie.

## <a name="start-a-transfer-job"></a>Een overboekingstaak starten
1. Schakel in de lijst de geselecteerde rij uit, indien aanwezig.
2. Selecteer rij 4 in de lijst.
    * Selecteer de eerste taak met de status Niet gepland. Zorg ervoor dat dit de enige geselecteerde taak is.  
3. Klik op Start.
    * Merk op dat een pictogram aangeeft dat de taak is gestart.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Een tweede overboekingstaak en wijzigingshoeveelheid selecteren
1. Zoek en selecteer de gewenste record in de lijst.
    * U kunt meerdere geselecteerde taken hebben, maar selecteert nu moment rij 5.  
2. Zoek en selecteer de gewenste record in de lijst.
    * Zorg ervoor de taak in de vorige stap de enige geselecteerde taak is. Maak de selectie van alle andere taken ongedaan.  
3. Noteer de waarde in het veld Taakhoeveelheid zodat u er later naar kunt verwijzen
4. Stel Taakhoeveelheid in op "30".
    * Let op de waarschuwing! U mag niet 30 overboeken. Volgens de instellingen van de kanbanregel, kunt u alleen de originele hoeveelheid overboeken.  
5. Gebruik de eerder genoteerde waarde in het veld Taakhoeveelheid
    * Stel de taakhoeveelheid in op de vorige waarde.  

## <a name="start-the-second-transfer-job"></a>De tweede overboekingstaak starten
1. Klik op Start.
    * Hiermee wordt de overboeking van de taak in rij 5 gestart.  

## <a name="complete-both-transfer-jobs"></a>Beide overboekingstaken voltooien
1. Selecteer rij 4 in de lijst.
    * Nu worden twee overboekingstaken geselecteerd op rij 4 en 5.  
2. Klik op Voltooien.
    * Hiermee wordt de overboeking van beide taken voltooid.  

