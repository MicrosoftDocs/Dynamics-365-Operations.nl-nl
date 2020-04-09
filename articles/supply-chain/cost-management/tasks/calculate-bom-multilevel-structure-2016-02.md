---
title: Een stuklijst berekenen met behulp van een structuur met meerdere niveaus (februari 2016)
description: Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op meerdere niveaus, die is gebaseerd op de kostprijsberekening.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c35d2b2d5c0fdd14c7e0a35316d482b2e3ffb49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150424"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Een stuklijst berekenen met behulp van een structuur met meerdere niveaus (februari 2016)

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op meerdere niveaus, die is gebaseerd op de kostprijsberekening. Dit is de zevende taak in de reeks stuklijstberekeningen. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.

1. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer het product Stuklijst_1.  
3. Klik in het actievenster op Kosten beheren.
4. Klik op Artikelprijs.
5. Klik op Artikelkosten berekenen.
    * Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.  
6. Typ of selecteer een waarde in het veld Kostprijsberekeningsversie.
    * Selecteer kostprijsberekening versie 20, omdat dit het type Geplande kosten is, met explosiemodus Meerdere niveaus.   De explosiemodus voor meerdere niveaus is voor geplande kosten en simulaties. Hij wordt niet gebruikt voor de standaardkostprijzen.  
7. Klik op OK.
8. Klik op Berekeningsdetails weergeven.
    * Mogelijk moet u op de drie puntjes (...) klikken om deze optie in het bovenste menu weer te laten geven.  In dit geval ziet u hoe BOM_2 is berekend, rekening houdend met de grondstoffen, verwerking en overhead met een kostentotaal van 29,40, in plaats van de standaardkosten van 10 die in de eerste taakbegeleider in deze reeks was geactiveerd.  
9. Klik op het tabblad Kostprijsberekening.
    * Als we verdergaan naar het tabblad Kostprijsberekening, zien we dat de totalen per kostengroep afwijken van de berekening die in de vorige taakbegeleider is uitgevoerd.  
10. Selecteer in het veld Niveau de waarde 'Meerdere'.
    * Als u Meerdere niveaus kiest, worden de kosten ingedeeld volgens de samenstelling van Stuklijst_2, waarbij 10 is afgeleid van de kostengroep M1 (Artikel_C), en 15,60 is afgeleid van de productie, waarbij de kostengroep L2 is. De indirecte kosten zijn ook anders.  
11. Sluit de pagina.
12. Sluit de pagina.

