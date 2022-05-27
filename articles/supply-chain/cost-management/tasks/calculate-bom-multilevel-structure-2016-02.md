---
title: Een stuklijst berekenen met behulp van een structuur met meerdere niveaus (februari 2016)
description: Deze procedure laat zien hoe u de kostprijs van een eindproduct berekent door middel van explosiemodus op meerdere niveaus, die is gebaseerd op de kostprijsberekening.
author: JennySong-SH
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f5bfacbcf4238102c5f9f26fdf1a30f5da27fc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672145"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]