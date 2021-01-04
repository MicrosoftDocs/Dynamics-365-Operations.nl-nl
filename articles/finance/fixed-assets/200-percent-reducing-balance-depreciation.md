---
title: Degressieve afschrijving van 200 procent
description: Dit artikel geeft een overzicht van de afschrijvingsmethode Degressieve afschrijving van 200 procent.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0474a8cecccaf1e23874458c27e0bea991140b6c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442009"
---
# <a name="200-percent-reducing-balance-depreciation"></a>Degressieve afschrijving van 200 procent

[!include [banner](../includes/banner.md)]

Dit artikel geeft een overzicht van de afschrijvingsmethode Degressieve afschrijving van 200 procent.

Wanneer u een profiel voor de afschrijving van vaste activa instelt en **200% degressief** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, worden de vaste activa waaraan dit afschrijvingsprofiel is toegewezen, afgeschreven met hetzelfde percentage in elke afschrijvingsperiode. Het percentage wordt berekend aan de hand van de levensduur van het activum. Als een activum een levensduur van bijvoorbeeld vijf jaar heeft, wordt het percentage berekend als 40 procent (200% ÷ 5). 

Deze methode wordt ook 'double declining balance' genoemd.

Voor een 200% degressieve afschrijving moet u ook opties selecteren in het veld **Afschrijvingsjaar** en het veld **Periodefrequentie** op de pagina **Afschrijvingsprofielen**. De opties die beschikbaar zijn in het veld **Periodefrequentie** variëren, afhankelijk van de waarde die u selecteert in het veld **Afschrijvingsjaar**.

## <a name="select-a-depreciation-year"></a>Een afschrijvingsjaar selecteren
U kunt **Kalender** of **Fiscaal** selecteren in het veld **Afschrijvingsjaar** op de pagina **Afschrijvingsprofielen**. De standaardwaarde is **Kalender**. 

Uw keuze bepaalt welke opties beschikbaar zijn in het veld **Periodefrequentie**. Dit veld bepaalt voor het gehele jaar de boekingdatums en bedragen voor de toerekening van de afschrijving.

### <a name="calendar"></a>Kalender

U kunt de standaardwaarde **Kalender** in het veld **Afschrijvingsjaar** behouden. 

Met de optie **Kalender** wordt de afschrijvingsbasis op 1 januari van elk jaar bijgewerkt. Doorgaans is de afschrijving de nettoboekwaarde min de restwaarde. In de voorbeelden verderop in dit onderwerp is de afschrijvingsbasis de teller in de eerste expressie in de berekeningenkolom. 

Als u **Kalender** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:

-   **Jaarlijks**: op 31 december wordt een bedrag geboekt.
-   **Maandelijks**: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.
-   **Driemaandelijks**: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.
-   **Zesmaandelijks**: aan het einde van elk half jaar (30 juni en 31 december) wordt er een halfjaarlijks bedrag geboekt.
-   Met **Dagelijks** wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.

### <a name="fiscal"></a>Fiscaal

Als u **Boekjaar** selecteert in het veld **Afschrijvingsjaar**, wordt de 200% degressieve afschrijving van de levensduur berekend op basis van het boekjaar voor de fiscale kalender die is opgegeven voor het boek of op basis van de pagina **Grootboek**. Fiscale kalenders kunt u instellen op de pagina **Fiscale kalenders**. 

Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend. Een boekjaar kan langer of korter dan 12 maanden zijn. De afschrijving wordt voor elke periode aangepast. De lengte van het volgende boekjaar wordt bepaald door de perioden die zijn ingesteld op de pagina **Fiscale kalenders**. 

Als **Fiscaal** als afschrijvingsjaar wordt geselecteerd, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:

-   **Jaarlijks** boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar als één bedrag op de laatste dag van het boekjaar.
-   **Boekperiode**: boekt het totale bedrag van de afschrijving dat is berekend voor het boekjaar op de laatste dag van het boekjaar. Dit bedrag wordt toegerekend in de boekperioden die zijn gedefinieerd op de pagina **Fiscale kalenders**.

## <a name="example-of-200-reducing-balance-depreciation"></a>Voorbeeld van een 200% degressieve afschrijving

|                                |        |
|--------------------------------|--------|
| Bijboekingskosten               | 11.000 |
| Restwaarde                  | 1.000 |
| Afschrijvingsbasis              | 10.000 |
| Levensduur in jaren             | 5      |
| Jaarlijks afschrijvingspercentage | 40%    |

Bij de methode 200% degressieve afschrijvingsmethode, wordt 200 procent door het aantal jaren levensduur gedeeld. Dat percentage wordt vermenigvuldigd met de nettoboekwaarde van de activa om het afschrijvingsbedrag voor het jaar te kunnen bepalen.

| Periode | Berekening van het jaarlijkse afschrijvingsbedrag | Boekwaarde             | Nettoboekwaarde aan het einde van het jaar |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| Jaar 1 | (11.000 – 1.000) × 40% = 4.000                | 11.000 – 4.000 = 7.000 | 11.000 – 1.000 – 4.000 = 6.000        |
| Jaar 2 | 6.000 × 40% = 2.400                           | 7.000 – 2.400 = 4.600  | 6.000 – 2.400 = 3.600                 |
| Jaar 3 | 3.600 × 40% = 1.440                           | 4.600 – 1.440 = 3.160  | 3.600 – 1.440 = 2.160                 |

> [!NOTE] 
> Wanneer het bedrag dat wordt berekend met de methode voor 200% degressieve afschrijving lager is dan het bedrag dat wordt berekend door de lineaire methode te gebruiken, vindt er doorgaans een conversie naar de lineaire methode plaats voor de resterende levensduur.



