---
title: Degressieve afschrijving
description: Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving.
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 114264fba678e9dc222a304fc7e2c2214b213c98
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="reduce-balance-depreciation"></a>Degressieve afschrijving

[!include[banner](../includes/banner.md)]


Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving.

Wanneer u een profiel voor de afschrijving van vaste activa instelt en Degressieve afschrijving selecteert in het veld Methode op de pagina Afschrijvingsprofielen, worden de activa waaraan dit afschrijvingsprofiel is toegewezen, afgeschreven met hetzelfde percentage in elke afschrijvingsperiode.

Om degressieve afschrijving in te stellen, moet u ook waarden selecteren in velden op het sneltabblad Algemeen van de pagina Afschrijvingsprofielen. Selecteer eerst een jaar in het veld Afschrijvingsjaar. In het veld Periodefrequentie worden verschillende opties weergegeven, afhankelijk van wat in het andere veld is geselecteerd (zie verderop). 

U dient ook een waarde in te voeren bij het veld Percentage voor het afschrijvingsprofiel. Als u de optie Volledige afschrijving selecteert, wordt de resterende afschrijvingsbasis gekozen in de laatste afschrijvingsperiode en is het mogelijk een grote hoeveelheid. Bepaalde landen/regio's gebruiken geen overschakeling naar een lineaire methode. Wanneer het bedrag van de alternatieve afschrijvingsmethode groter dan of gelijk aan is het bedrag van het primaire afschrijvingsprofiel, wordt overgeschakeld en wordt het bedrag van de alternatieve methode gebruikt als afschrijvingsbedrag. 

Aangezien een activum nooit volledig zal worden afgeschreven op basis van een berekening van het percentage, dient u de optie Volledige afschrijving te selecteren om een activum volledig af te schrijven.

## <a name="select-a-depreciation-year"></a>Een afschrijvingsjaar selecteren
U kunt Kalender of Fiscaal selecteren in het veld Afschrijvingsjaar op de pagina Afschrijvingsprofielen. De selectie bepaalt welke opties beschikbaar zijn in het veld Periodefrequentie. De standaardoptie is Kalender.

### <a name="calendar"></a>Kalender

Met de optie Kalender wordt de afschrijvingsbasis (doorgaans de nettoboekwaarde min de restwaarde) bijgewerkt op 1 januari van elk jaar. In het onderstaande voorbeeld van degressieve saldoafschrijving verder in dit onderwerp, is de afschrijvingsbasis de teller in de eerste uitdrukking in de kolom met berekeningen. 

Als u Kalender selecteert, zijn de volgende opties beschikbaar in het veld Periodefrequentie. Dit veld bepaalt voor het gehele kalenderjaar de boekdatums en bedragen voor de toerekening van de afschrijving:

-   Jaarlijks boekt op 31 december.
-   Maandelijks: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.
-   Driemaandelijks: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.
-   Met Zesmaandelijks wordt aan het einde van elk half jaar (30 juni en 31 december) een halfjaarlijks bedrag geboekt.
-   Met Dagelijks wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.

Als u bijvoorbeeld Jaarlijks selecteert, wordt de jaarlijkse afschrijving wordt slechts één keer geboekt. Dit is telkens op 31 december. Als u Maandelijks selecteert, wordt de maandelijkse afschrijving elke maand als 1/12de van het jaarlijkse afschrijvingsbedrag geboekt.

### <a name="fiscal"></a>Fiscaal

Als u Fiscaal selecteert in het veld Afschrijvingsjaar wordt de lineaire afschrijvingsmethode gebruikt. Het wordt berekend op basis van het fiscaal jaar dat is ingesteld op de pagina Fiscale kalenders voor de fiscale kalender die is geselecteerd op de pagina Grootboek. Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend. Een boekjaar kan langer of korter dan 12 maanden zijn. De afschrijving wordt voor elke boekperiode aangepast. De lengte van het volgende boekjaar is gebaseerd op de boekperioden die u instelt wanneer u een nieuw fiscaal jaar maakt op de pagina Fiscale kalenders.


Als u Fiscaal selecteert in het veld Periodefrequentie, dan zijn de volgende opties beschikbaar:

-   Jaarlijks boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar als één bedrag op de laatste dag van het boekjaar.
-   Boekperiode boekt het totale bedrag van de afschrijving berekend voor het fiscaal jaar, dat wordt toegerekend in de boekperioden die zijn gedefinieerd voor de fiscale kalender die is geselecteerd op de pagina Grootboek of voor de fiscale kalender die is geselecteerd voor het boek voor een vast activum.

## <a name="example-of-reducing-balance-depreciation"></a>Voorbeeld van een degressieve afschrijving

Stel dat de aanschafprijs van het vaste activum 11.000 is, de restwaarde is 1.000 en de afschrijvingspercentagefactor is 30. 

Door de methode Degressief te gebruiken, wordt 30 procent van de afschrijvingsbasis (nettoboekwaarde min restwaarde) berekend aan het einde van de vorige afschrijvingsperiode. De afschrijving voor de eerste drie jaar wordt in de volgende tabel weergegeven.

| Periode | Berekening van het jaarlijkse afschrijvingsbedrag | Nettoboekwaarde aan het einde van het jaar |
|--------|-------------------------------------------|---------------------------------------|
| Jaar 1 | (11.000 - 1000) \* 30% = 3000           | (11 000 - 1000) - 3000 = 7000      |
| Jaar 2 | (7000 - 1000) \* 30% = 1800            | (7000 -1800) = 5200                |
| Jaar 3 | (5200 - 1000) \* 30% = 1260            | (5200 - 1260) = 3940               |

 
-






