--- 
title: Een stuklijst berekenen met behulp van een structuur met een enkel niveau (uitsluitend februari 2016)
description: Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op een enkel niveau, die is gebaseerd op de kostprijsberekening.
author: YuyuScheller
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e6829238b244cc01b070fde6acdf37bdaeb9670
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a>Een stuklijst berekenen met behulp van een structuur met een enkel niveau (uitsluitend februari 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op een enkel niveau, die is gebaseerd op de kostprijsberekening. Dit is de zesde taak in de reeks stuklijstberekeningen. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.

1. Ga naar Vrijgegeven producten.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer het product Stuklijst_1.  
3. Klik in het actievenster op Kosten beheren.
4. Klik op Artikelprijs.
5. Klik op Artikelkosten berekenen.
    * Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.  
6. Klik in het veld Kostprijsberekeningsversie op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer voor deze demonstratie 10. Dit is de dezelfde kostprijsberekeningsversie die is gebruikt om de kostprijs aan de onderdelen toe te voegen.  
7. Klik op OK.
8. Klik op Berekeningsdetails weergeven.
    * Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.    Zo zijn de kosten samengesteld: • 10 is afgeleid van ITEM_A, 10 van ITEM_B, 10 van BOM_2. In dit geval zijn er geen details voor Artikel_2, omdat deze is ingevoerd als een standaardkostprijs van 10, maar niet is verkregen door berekening.  •  7 is afgeleid van de insteltijd, die een constante kostenfactor is, en nog eens 7 is afgeleid van de uitvoeringstijdbewerking (Proces).  •  Daarnaast zijn er nog andere bedragen, die met de indirecte kosten overeenkomen.  
9. @SysTaskRecorder:_RequestClose


