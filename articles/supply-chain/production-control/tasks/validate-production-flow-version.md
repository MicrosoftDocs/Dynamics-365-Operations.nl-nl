---
title: Een productiestroom en -versie valideren
description: Deze procedure toont aan hoe u een nieuwe productiestroom en een eerste versie voor lean manufacturing maakt.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d87aa427c2bc3868e255c97ea11fd4e79456eef
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573580"
---
# <a name="validate-a-production-flow-and-version"></a>Een productiestroom en -versie valideren

[!include [banner](../../includes/banner.md)]

Deze procedure toont aan hoe u een nieuwe productiestroom en een eerste versie voor lean manufacturing maakt. Vereisten: De productieparameters voor lean manufacturing en de maateenheden voor de klasse Tijd moeten worden gedefinieerd. U moet een Waardestroom en een Productiegroep definiëren. Raadpleeg de whitepapers over lean manufacturing om uzelf vertrouwd te maken met de concepten van productiestromen en activiteiten. Deze procedure verwijst naar de rechtspersoon USMF in demogegevens. Als we er echter van uitgaan dat de rechtspersoon voor lean manufacturing is geconfigureerd, kunnen andere rechtspersonen worden gebruikt.


## <a name="create-a-production-flow"></a>Een productiestromen maken
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ een waarde in het veld Omschrijving.
5. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Een waardestroom is een operationele eenheid die alle activiteiten en stromen van de waardestroom dekt.   In deze fase zijn operationele eenheden beperkt tot een rechtspersoon en hebben ze verder geen functionaliteit.  
7. Klik in het veld Productiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Productieorders maken het definiëren van materiaal, arbeid en OHW-rekeningen mogelijk voor een productieproces. Als u de boekhoudcontext wilt koppelen aan een productiestroom, moet een productiegroep zijn geselecteerd.  
9. Klik op Opslaan.

## <a name="create-a-production-flow-version"></a>Een productiestroomversie maken
1. Klik op Toevoegen.
2. Voer in het veld Vervaldatum een datum en tijd in.
    * U kunt de Vervaldatum van de versie op elk moment bijwerken, zelfs voor actieve versies. Gebruik de vervaldatum van de versie om een stapsgewijze afschaffing van een versie te plannen.  
3. Klik op OK.
4. Markeer in de lijst de geselecteerde rij.
5. Typ een waarde in het veld Eenheid.
6. Selecteer de Takteenheid.
7. Voer in het veld Gemiddelde takttijd een getal in.
    * Definieer voor het taktbeheer van de productiestroomversie een beoogde gemiddelde takttijd.   Takt wordt gedefinieerd als hoeveelheid per periode.  In het voorbeeld is de takttijd 0,2 uur per 10 stuks. Voor een werktijd van 8 uur correspondeert dat met een dagelijkse doorvoercapaciteit van 400 stuks.  
8. Voer in het veld Hoeveelheid per cyclus een getal in.
9. Vouw de sectie Versiegegevens uit of samen.
10. Voer in het veld Minimumtakttijd een getal in.
    * De minimale takttijd moet korter zijn dan of gelijk zijn aan de gemiddelde takttijd.  
11. Voer in het veld Maximumtakttijd een getal in.
    * De maximale takttijd moet langer zijn dan of gelijk zijn aan de gemiddelde takttijd.  
12. Een aantal dagen invoeren bij Periode voor werkelijke cyclusduur
    * De periode voor de werkelijke cyclustijd is het aantal dagen dat taken worden samengevoegd vanaf de werkelijke minuut achterwaarts om de werkelijke cyclustijd te berekenen. De waarde kan altijd worden gewijzigd en wordt alleen gebruikt voor de berekening van de werkelijke cyclustijden.  
13. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]