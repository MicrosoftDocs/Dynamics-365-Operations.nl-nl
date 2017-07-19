---
title: Degressieve afschrijving van 125 procent
description: Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 125 procent.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 6e9a50c9cc03a7f561a3c23987538c0285c542e8
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a>Degressieve afschrijving van 125 procent

[!include[banner](../includes/banner.md)]


Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 125 procent.

Wanneer u een profiel voor de afschrijving van vaste activa instelt en **125% degressieve afschrijving** in het veld **Methode** op de pagina **Afrschrijvingsprofielen**, worden vaste activa die zijn toegewezen aan het afschrijvingsprofiel met hetzelfde percentage afgeschreven in elke afschrijvingsperiode. Dit percentage wordt berekend aan de hand van de levensduur van het activum. Als een activum een levensduur van bijvoorbeeld vijf jaar heeft, wordt het percentage berekend als 25 procent (125% ÷ 5).

Voor een degressieve afschrijving van 125% moet u ook opties selecteren in het veld **Afschrijvingsjaar** en het veld **Periodefrequentie** op de pagina **Afschrijvingsprofielen**. De opties die beschikbaar zijn in het veld **Periodefrequentie** variëren, afhankelijk van de waarde die in het veld **Afschrijvingsjaar** is geselecteerd.

## <a name="select-a-depreciation-year"></a>Een afschrijvingsjaar selecteren
U kunt **Kalender** of **Fiscaal** selecteren in het veld **Afschrijvingsjaar** op de pagina **Afschrijvingsprofielen**. De standaardwaarde is **Kalender**. 

Uw keuze bepaalt welke opties beschikbaar zijn in het veld **Periodefrequentie**. Dit veld bepaalt voor het gehele jaar de boekingdatums en bedragen voor de toerekening van de afschrijving.

### <a name="calendar"></a>Kalender

U kunt de standaardwaarde **Kalender** in het veld **Afschrijvingsjaar** behouden. 

Met de optie **Kalender** wordt de afschrijvingsbasis op 1 januari van elk jaar bijgewerkt. Doorgaans is de afschrijvingsbasis de nettoboekwaarde min de restwaarde. In de voorbeelden verderop in dit onderwerp is de afschrijvingsbasis de teller in de eerste expressie in de berekeningenkolom. 

Als u **Kalender** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:

-   **Jaarlijks**: op 31 december wordt een bedrag geboekt.
-   **Maandelijks**: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.
-   **Driemaandelijks**: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.
-   **Zesmaandelijks**: aan het einde van elk half jaar (30 juni en 31 december) wordt er een halfjaarlijks bedrag geboekt.
-   Met **Dagelijks** wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.

### <a name="fiscal"></a>Fiscaal

Als u **Boekjaar** selecteert in het veld **Afschrijvingsjaar**, wordt de 125% degressieve afschrijving van de levensduur berekend op basis van het boekjaar voor de fiscale kalender die is opgegeven voor het boek of op basis van de pagina **Grootboek**. Fiscale kalenders kunt u instellen op de pagina **Fiscale kalenders**. 

Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend. Een boekjaar kan langer of korter dan 12 maanden zijn. De afschrijving wordt automatisch voor elke periode aangepast, en de lengte van het volgend boekjaar wordt gehaald uit de instellingen van perioden op de pagina **Fiscale kalenders**. 

Als u **Fiscaal** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:

-   **Jaarlijks** boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar als één bedrag op de laatste dag van het boekjaar.
-   **Boekperiode**: boekt het totale bedrag van de afschrijving dat is berekend voor het boekjaar op de laatste dag van het boekjaar. Dit bedrag wordt toegerekend in de boekperioden die zijn gedefinieerd op de pagina **Fiscale kalenders**.

## <a name="example-of-125-reducing-balance-depreciation"></a>Voorbeeld van een 125% degressieve afschrijving
|                                |        |
|--------------------------------|--------|
| Bijboekingskosten               | 11.000 |
| Restwaarde                  | 1.000  |
| Afschrijvingsbasis              | 10.000 |
| Levensduur in jaren             | 5      |
| Jaarlijks afschrijvingspercentage | 25%    |

Bij de methode 125% degressieve afschrijvingsmethode, wordt 125 procent door het aantal jaren levensduur gedeeld. Dat percentage wordt vermenigvuldigd met de nettoboekwaarde van de activa om het afschrijvingsbedrag voor het jaar te kunnen bepalen.

| Periode | Berekening van het jaarlijkse afschrijvingsbedrag | Boekwaarde                    | Nettoboekwaarde aan het einde van het jaar |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| Jaar 1 | (11.000 – 1000) × 25% = 2500                | (11.000 – 2500) = 8500      | (11.000 – 1000 – 2500) = 7500      |
| Jaar 2 | 7500 × 25% = 1875                           | (8500 – 1875) = 6625       | (7500 – 1875) = 5625               |
| Jaar 3 | 5625 × 25% = 1406,25                        | (6625 – 1406,25) = 5218,75 | (5625 – 1406,25) = 4218,75         |

> [!NOTE] 
> Wanneer het bedrag dat wordt berekend met de methode voor 125% degressieve afschrijving lager is dan het bedrag dat wordt berekend door de lineaire methode te gebruiken, vindt er doorgaans een conversie naar de lineaire methode plaats voor de resterende levensduur.




