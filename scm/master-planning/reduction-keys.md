---
title: Reductiesleutels
description: "Dit artikel bevat voorbeelden die het instellen van een reductiesleutel weergeven. Het bevat informatie over de verschillende reductiesleutelinstellingen en de resultaten van elk. U kunt een reductiesleutel gebruiken om te definiëren hoe prognosebehoeften worden gereduceerd."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ce3ff2ac0a5bd9bd342baa05425d7d0957ab8a09
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="reduction-keys"></a>Reductiesleutels

[!include[banner](../includes/banner.md)]


Dit artikel bevat voorbeelden die het instellen van een reductiesleutel weergeven. Het bevat informatie over de verschillende reductiesleutelinstellingen en de resultaten van elk. U kunt een reductiesleutel gebruiken om te definiëren hoe prognosebehoeften worden gereduceerd.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>Voorbeeld 1: prognosereductiemethode Percentage - reductiesleutel
---------------------------------------------------------------

In dit voorbeeld wordt weergegeven hoe een reductiesleutel vraagprognosebehoeften reduceert overeenkomstig de percentages en perioden die door de reductiesleutel worden gedefinieerd.

1.  Stel op de pagina **Reductiesleutels** de volgende regels in.
    | Wisselgeld | Eenheid  | Procent |
    |--------|-------|---------|
    | 1      | Maand | 100     |
    | 2      | Maand | 75      |
    | 3      | Maand | 50      |
    | 4      | Maand | 25      |

2.  Koppel de reductiesleutel aan de behoefteplanningsgroep van het artikel.
3.  Selecteer op de pagina **Hoofdplannen** in het veld **Reductiemethode** de optie **Percentage - reductiesleutel**.
4.  Maak een vraagprognose van 1000 stuks per maand.

Als u de prognoseplanning op 1 januari uitvoert, worden de vraagprognosebehoeften verbruikt volgens de percentages die u instelt op de pagina **Reductiesleutels**. De volgende behoeftehoeveelheden worden naar het hoofdplan overgebracht.

| Maand                | Benodigd aantal stuks |
|----------------------|---------------------------|
| januari              | 0                         |
| februari             | 250                       |
| maart                | 500                       |
| april                | 750                       |
| Mei tot en met december | 1.000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Voorbeeld 2: prognosereductiemethode Transacties - reductiesleutel
In dit voorbeeld wordt weergegeven hoe werkelijke orders, die plaatsvinden tijdens de perioden die zijn gedefinieerd door de reductiesleutel, vraagprognosebehoeften reduceren.

-   Selecteer op de pagina **Hoofdplannen** in het veld **Reductiemethode** de optie **Transacties - reductiesleutel**.

Op 1 januari waren er de volgende verkooporders.

| Maand    | Besteld aantal stuks |
|----------|--------------------------|
| januari  | 956                      |
| februari | 1.176                    |
| maart    | 451                      |
| april    | 119                      |

Als u dezelfde vraagprognose van 1000 stuks per maand gebruikt, worden de volgende behoeftehoeveelheden naar het hoofdplan overgebracht.

| Maand                | Benodigd aantal stuks |
|----------------------|---------------------------|
| januari              | 44                        |
| februari             | 0                         |
| maart                | 549                       |
| april                | 881                       |
| Mei tot en met december | 1.000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Voorbeeld 3: prognosereductiemethode Transacties - dynamische periode
In de meeste gevallen worden systemen zo ingesteld dat transacties vraagprognose reduceren in specifieke prognoseperioden: weken, maanden, enzovoort. Deze perioden worden gedefinieerd in de reductiesleutel. De tijd tussen twee vraagprognoseregels kan echter ook een periode *impliceren*.

1.  Maak een vraagprognose voor de volgende datums en hoeveelheden.
    | Datum       | Vraagprognose |
    |------------|-----------------|
    | 1 januari  | 1.000           |
    | 5 januari  | 500             |
    | 12 januari | 1.000           |

    In deze prognose is er geen duidelijke periode tussen de prognosedatums: tussen de eerste en tweede datum is er een vierdaags tijdsbestek en tussen de tweede en derde datum is er een zevendaags tijdsbestek. Dit zijn de dynamische perioden.
2.  Maak als volgt verkooporderregels.
    | Datum                             | Verkooporderhoeveelheid |
    |----------------------------------|----------------------|
    | 15 december in het vorige jaar | 500                  |
    | 3 januari                        | 100                  |
    | 10 januari                       | 200                  |

De prognose wordt als volgt gereduceerd:

-   De eerste verkooporder ligt niet binnen een periode, zodat het de prognose niet reduceert.
-   De tweede verkooporder ligt tussen 1 januari en 5 januari, zodat het de prognose voor 1 januari met 100 reduceert.
-   De derde verkooporder ligt tussen 5 januari en 12 januari, zodat het de prognose voor 5 januari met 200 reduceert.

De volgende geplande order wordt gemaakt om de prognose te vervullen.

| Vraagprognosedatum | Gereduceerde hoeveelheid |
|----------------------|------------------|
| 1 januari            | 900              |
| 5 januari            | 300              |
| 12 januari           | 1.000            |

Hier is een overzicht van de reductie **Transacties - dynamische periode**:

-   Prognosebehoeften worden gereduceerd door de werkelijke ordertransacties die tijdens de dynamische periode plaatsvinden. De dynamische periode bestrijkt de huidige prognosedatums en eindigt bij het begin van de volgende prognose.
-   Deze methode gebruikt of vereist geen reductiesleutel.
-   Wanneer deze optie wordt gebruikt, vindt het volgende gedrag plaats:
    -   Als de prognose volledig is gereduceerd, worden de prognosebehoeften voor de huidige prognose 0 (nul).
    -   Als er geen toekomstige prognose is, worden de prognosebehoeften van de laatste prognose die is ingevoerd, gereduceerd.
    -   De timefences worden opgenomen in de berekening van de prognosereductie.
    -   Positieve dagen zijn opgenomen in de berekening van de prognosereductie.
    -   Als de werkelijke ordertransacties de prognosebehoeften overschrijden, worden de resterende transacties niet naar de volgende prognoseperiode doorgestuurd.


<a name="see-also"></a>Zie ook
--------

[Hoofdplannen](master-plans.md)




