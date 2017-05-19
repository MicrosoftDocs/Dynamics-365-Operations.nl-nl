---
title: Degressieve afschrijving van 175 procent
description: Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 175 procent.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: cf428d61f89ea70a83e440c656fbc84d7dbded8d
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="175-percent-reducing-balance-depreciation"></a>Degressieve afschrijving van 175 procent

[!include[banner](../includes/banner.md)]


Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 175 procent.

Wanneer u een profiel voor de afschrijving van vaste activa instelt en **175% degressief** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, worden de vaste activa waaraan dit afschrijvingsprofiel is toegewezen, afgeschreven met hetzelfde percentage in elke afschrijvingsperiode. 

Voor een 175% degressieve afschrijving moet u ook opties selecteren in het veld **Afschrijvingsjaar** en het veld **Periodefrequentie** op de pagina **Afschrijvingsprofielen**. De opties die beschikbaar zijn in het veld **Periodefrequentie** variëren, afhankelijk van de waarde die in het veld **Afschrijvingsjaar** is geselecteerd.

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

Als u **Boekjaar** selecteert in het veld **Afschrijvingsjaar**, wordt de 175% degressieve afschrijving van de levensduur berekend op basis van het boekjaar voor de fiscale kalender die is opgegeven voor het boek of op basis van de pagina **Grootboek**. Fiscale kalenders kunt u instellen op de pagina **Fiscale kalenders**. Zie [Fiscale kalenders, boekjaren en boekperioden](..\budgeting\fiscal-calendars-fiscal-years-periods.md) voor meer informatie.

Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend. Een boekjaar kan langer of korter dan 12 maanden zijn. De afschrijving wordt automatisch voor elke periode aangepast, en de lengte van het volgend boekjaar wordt gehaald uit de instellingen van perioden op de pagina **Fiscale kalenders**. 

Als u **Fiscaal** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:

-   **Jaarlijks**: boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar op de laatste dag van het boekjaar.
-   **Boekperiode**: berekent het totale bedrag van de afschrijving voor het boekjaar. Dit bedrag wordt toegerekend in de boekperioden die zijn gedefinieerd op de pagina **Fiscale kalenders**.

## <a name="example-of-175-reducing-balance-depreciation"></a>Voorbeeld van een 175% degressieve afschrijving
|                                |        |
|--------------------------------|--------|
| Bijboekingskosten               | 11.000 |
| Restwaarde                  | 1.000  |
| Afschrijvingsbasis              | 10.000 |
| Levensduur in jaren             | 5      |
| Jaarlijks afschrijvingspercentage | 35%    |

Bij de methode 175% degressieve afschrijvingsmethode wordt 175 procent door het aantal jaren levensduur gedeeld. Dat percentage wordt vermenigvuldigd met de nettoboekwaarde van de activa om het afschrijvingsbedrag voor het jaar te kunnen bepalen.

| Periode | Berekening van het jaarlijkse afschrijvingsbedrag | Boekwaarde                  | Nettoboekwaarde aan het einde van het jaar |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| Jaar 1 | (11.000 – 1000) × 35% = 3500                | 11.000 – 3500 = 7500      | 11.000 – 1000 – 3500 = 6500        |
| Jaar 2 | 6500 × 35% = 2275                           | 7500 – 2275 = 5225       | 6500 – 2275 = 4225                 |
| Jaar 3 | 4225 × 35% = 1478,75                        | 5225 – 1478,75 = 3746,25 | 4225 – 1478,75 = 2746,25           |

> [!NOTE] 
> Wanneer het bedrag dat wordt berekend met de methode voor 175% degressieve afschrijving lager is dan het bedrag dat wordt berekend door de lineaire methode te gebruiken, vindt er doorgaans een conversie naar de lineaire methode plaats voor de resterende levensduur.




