---
title: Een stuklijst berekenen met behulp van een structuur met één niveau (februari 2016)
description: Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op een enkel niveau, die is gebaseerd op de kostprijsberekening.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013eddf1ba8e8cab3c87cb1f063d9bf886b0f833
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821388"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Een stuklijst berekenen met behulp van een structuur met één niveau (februari 2016)

[!include [banner](../../includes/banner.md)]

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
    * Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.    Zo zijn de kosten samengesteld:  *    10 is afgeleid van ITEM_A, 10 van ITEM_B, 10 van BOM_2. In dit geval zijn er geen details voor Artikel_2, omdat deze is ingevoerd als een standaardkostprijs van 10, maar niet is verkregen door berekening.  *   7 is afgeleid van de insteltijd, die een constante kostenfactor is, en nog eens 7 is afgeleid van de uitvoeringstijdbewerking (Proces).  *    Daarnaast zijn er nog andere bedragen, die met de indirecte kosten overeenkomen.  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]