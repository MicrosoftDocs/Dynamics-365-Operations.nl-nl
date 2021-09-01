---
title: Een productiestroomversie maken
description: Deze procedure is gericht op het maken van een nieuwe productstroomversie.
author: cvocph
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4fc158ac70834c5d3b590acbe015cb9200d9f4f99df339bc7c1874a6a74d5f34
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751045"
---
# <a name="create-a-production-flow-version"></a>Een productiestroomversie maken

[!include [banner](../../includes/banner.md)]

Deze procedure is gericht op het maken van een nieuwe productstroomversie. Voor deze procedure moeten de productieparameters voor lean manufacturing en de maateenheden voor klassetijd worden gedefinieerd. U moet ook een waardestroom en een productiegroep definiëren. Als u meer wilt weten over productiestromen en activiteiten in lean manufacturing, raadpleegt u de whitepapers over lean manufacturing voor Microsoft Dynamics AX. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-production-flow"></a>Een productiestromen maken
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ een waarde in het veld Omschrijving.
5. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer een operationele eenheid van het type waardestroom. Een waardestroom is een operationele eenheid die alle activiteiten en stromen van de waardestroom omvat. In deze fase zijn operationele eenheden beperkt tot een rechtspersoon en hebben ze verder geen functionaliteit.  
7. Klik in het veld Productiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer een productiegroep voor de productiestroom. Productieorders maken het definiëren van materiaal, arbeid en OHW-rekeningen mogelijk voor een productieproces. Als u de boekhoudcontext wilt koppelen aan een productiestroom, moet een productiegroep zijn geselecteerd.  
9. Klik op Opslaan.

## <a name="create-a-production-flow-version"></a>Een productiestroomversie maken
1. Klik op Toevoegen.
2. Voer in het veld Vervaldatum een datum en tijd in.
    * Definieer indien nodig een vervaldatum voor de versie. U kunt deze op elk moment bijwerken, zelfs voor actieve versies. U kunt deze gebruiken om een versie uit te faseren.  
3. Klik op OK.
4. Markeer in de lijst de geselecteerde rij.
5. Typ een waarde in het veld Eenheid.
6. Wijzig de takteenheid.
7. Voer in het veld Gemiddelde takttijd een getal in.
    * Definieer de gemiddelde takttijd van de versie. Definieer voor het taktbeheer van de productiestroomversie een beoogde gemiddelde takttijd. De takt wordt gedefinieerd als hoeveelheid per periode. In het voorbeeld is de takttijd 0,2 uur per 10 stuks. Voor een werktijd van 8 uur correspondeert dat met een dagelijkse doorvoercapaciteit van 400 stuks.  
8. Voer in het veld Hoeveelheid per cyclus een getal in.
    * Definieer de hoeveelheid per cyclus, gerelateerd aan de gemiddelde takttijd.  
9. Schakel de uitbreiding van de sectie Versiedetails om.
10. Voer in het veld Minimumtakttijd een getal in.
    * Definieer de minimale takttijd. De minimale takttijd moet korter zijn dan of gelijk zijn aan de gemiddelde takttijd.  
11. Voer in het veld Maximumtakttijd een getal in.
    * De maximale takttijd moet langer zijn dan of gelijk zijn aan de gemiddelde takttijd.  
12. Voer een getal in het veld Periode voor werkelijke cyclusduur (dagen) in.
    * Voer het aantal dagen in het veld Periode voor werkelijke cyclusduur in. De periode voor de werkelijke cyclustijd is het aantal dagen dat taken worden samengevoegd vanaf de werkelijke minuut achterwaarts om de werkelijke cyclustijd te berekenen. De waarde kan altijd worden gewijzigd en wordt alleen gebruikt voor de berekening van de werkelijke cyclustijden.  
13. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]