---
title: Lineaire afschrijving van levensduur
description: Dit artikel geeft een overzicht van de afschrijvingsmethode Lineaire levensduur.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6848aaa679ae42d21b40fdc5f46596aa1f2e899
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009263"
---
# <a name="straight-line-service-life-depreciation"></a>Lineaire afschrijving van levensduur

[!include [banner](../includes/banner.md)]

Dit artikel geeft een overzicht van de afschrijvingsmethode Lineaire levensduur.

Wanneer u een afschrijvingsprofiel voor vaste activa instelt en Lineaire levensduur selecteert in het veld Methode van de pagina Afschrijvingsprofielen, worden de activa waaraan dit afschrijvingsprofiel is toegewezen, afgeschreven op basis van de totale levensduur van het activum. Dit is over het algemeen in elke afschrijvingsperiode hetzelfde afschrijvingsbedrag. 

Het enige verschil in het afschrijvingsbedrag dat is berekend tussen een restlevensduur rechte lijn en levensduur rechte lijn is wanneer er een correctie in de activa is geboekt. 

Voor een lineaire levensduurafschrijving moet u ook opties selecteren in het veld Afschrijvingsjaar en het veld Periodefrequentie op de pagina Afschrijvingsprofielen.

## <a name="select-a-depreciation-year"></a>Een afschrijvingsjaar selecteren
U kunt Kalender of Fiscaal selecteren in het veld Afschrijvingsjaar op de pagina Afschrijvingsprofielen. De selectie bepaalt welke opties beschikbaar zijn in het veld Periodefrequentie. De standaardoptie is Kalender.

### <a name="calendar"></a>Kalender

Als u Kalender selecteert, wordt uitgegaan van een jaar van 1 januari t/m 31 december, zelfs als u de fiscale kalender anders hebt ingesteld. 

Met de optie Kalender wordt de afschrijvingsbasis (doorgaans de nettoboekwaarde min de restwaarde) bijgewerkt op 1 januari van elk jaar. In de voorbeelden verderop in dit onderwerp is de afschrijvingsbasis de teller in de eerste expressie in de berekeningenkolom. 

Als u Kalender selecteert, zijn de volgende opties beschikbaar in het veld Periodefrequentie. Dit veld bepaalt voor het gehele kalenderjaar de boekdatums en bedragen voor de toerekening van de afschrijving:
-   Met Jaarlijks wordt een bedrag geboekt op 31 december.
-   Maandelijks: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.
-   Driemaandelijks: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.
-   Met Zesmaandelijks wordt aan het einde van elk half jaar (30 juni en 31 december) een halfjaarlijks bedrag geboekt.
-   Met Dagelijks wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.

Als u bijvoorbeeld Jaarlijks selecteert, wordt de jaarlijkse afschrijving wordt slechts één keer geboekt. Dit is telkens op 31 december. Als u Maandelijks selecteert, wordt de maandelijkse afschrijving elke maand als 1/12de van het jaarlijkse afschrijvingsbedrag geboekt.

### <a name="fiscal"></a>Fiscaal

Als u Fiscaal selecteert in het veld Afschrijvingsjaar wordt de lineaire afschrijving van de levensduur gebruikt. Deze wordt berekend op basis van het boekjaar, dat is gedefinieerd door de fiscale kalender die is opgegeven voor het waardemodel of afschrijvingsboek, of door de fiscale kalender die is geselecteerd op de pagina Grootboek. Fiscale kalenders kunt u instellen in de pagina Fiscale kalenders.

Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend. Een boekjaar kan langer of korter dan 12 maanden zijn. De afschrijving wordt automatisch voor elke boekperiode aangepast. De lengte van het volgende boekjaar is gebaseerd op de boekperioden die u instelt wanneer u een nieuw boekjaar maakt in de pagina Fiscale kalenders. 

Als u Fiscaal selecteert in het veld Periodefrequentie, dan zijn de volgende opties beschikbaar:
-   De optie Jaarlijks boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar als één bedrag op de laatste dag van het boekjaar.
-   De optie Fiscale periode berekent het totale bedrag van de afschrijving voor het boekjaar, dat wordt toegerekend in de boekperioden die zijn gedefinieerd in de pagina Fiscale kalenders voor de fiscale kalender.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Voorbeeld: lineaire afschrijving van een ongewijzigd vast activum
Stel dat een vast activum de volgende kenmerken heeft.

|                     |        |
|---------------------|--------|
| Verwervingskosten    | 11.000 |
| Restwaarde       | 1.000  |
| Afschrijvingsbasis   | 10.000 |
| Levensduur in jaren  | 5      |
| Jaarafschrijving | 2.000  |

U krijgt elk jaar hetzelfde afschrijvingsbedrag. (Aanschafkosten - restwaarde) / jaren levensduur

| Periode | Berekening van het jaarlijkse afschrijvingsbedrag | Nettoboekwaarde aan het einde van het jaar |
|--------|-------------------------------------------|---------------------------------------|
| Jaar 1 | (11.000 - 1.000) / 5 = 2.000              | 9.000                                 |
| Jaar 2 | (11.000 - 1.000) / 5 = 2.000              | 7.000                                 |
| Jaar 3 | (11.000 - 1.000) / 5 = 2.000              | 5.000                                 |
| Jaar 4 | (11.000 - 1.000) / 5 = 2.000              | 3.000                                 |
| Jaar 5 | (11.000 - 1.000) / 5 = 2.000              | 1.000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a>Voorbeeld: lineaire afschrijving van een gewijzigd vast activum

Stel dat u een bijboekingscorrectie van 4000 in jaar 2 aan hetzelfde vaste activum toevoegt. 

De levensduur van de bijboekingscorrectie is gelijk aan die van het vaste activum en begint op het moment van bijboeken. Aan het eind van jaar 5 blijft er een nettoboekwaarde over die overeenkomt met de nettoboekwaarde van de bijboekingscorrectie. De afschrijving per periode wordt berekend zoals in de volgende tabel.

| Periode | Berekening van het jaarlijkse afschrijvingsbedrag | Nettoboekwaarde aan het einde van het jaar |
|--------|-------------------------------------------|---------------------------------------|
| Jaar 1 | 10.000 / 5 = 2.000                        | 11.000 - 2.000 = 9.000                |
| Jaar 2 | 4.000 (verwervingscorrectie)            | 9.000 + 4.000 =13.000                 |
| Jaar 2 | 14.000 / 5 = 2.800                        | 13.000 - 2.800 = 10.200               |
| Jaar 3 | 14.000 / 5 = 2.800                        | 10.200 - 2.800 = 7.400                |
| Jaar 4 | 14.000 / 5 = 2.800                        | 7.400 - 2.800 = 4.600                 |
| Jaar 5 | 14.000 / 5 = 2.800                        | 4.600 - 2.800 = 1.800                 |
| Jaar 6 | Resterende 800\*                           | 1.800 – 800 = 1.000                   |

\* Omdat het resterende bedrag lager is dan het afschrijvingsbedrag, wordt alleen het resterende bedrag min de restwaarde gebruikt.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]