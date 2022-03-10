---
title: Lineaire afschrijving van restlevensduur
description: Dit onderwerp geeft een overzicht van de afschrijvingsmethode ´Lineaire restlevensduur´.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d3372fe5d77f54c68570314e8ba6db8bae28a60
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675190"
---
# <a name="straight-line-life-remaining-depreciation"></a>Lineaire afschrijving van restlevensduur

[!include [banner](../includes/banner.md)]

Dit onderwerp geeft een overzicht van de afschrijvingsmethode ´Lineaire restlevensduur´.

Wanneer u een profiel voor de afschrijving van vaste activa instelt en **Lineaire restlevensduur** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, dan is de afschrijving van vaste activa die zijn toegewezen aan dit afschrijvingsprofiel gebaseerd op de resterende levensduur van het activum. Over het algemeen is het afschrijvingsbedrag elke afschrijvingsperiode hetzelfde. Als u lineaire resterende afschrijving van de levensduur wilt instellen, moet u ook opties selecteren in het veld **Afschrijvingsjaar** en het veld **Periodefrequentie** op de pagina **Afschrijvingsprofielen**. De opties die beschikbaar zijn in het veld **Periodefrequentie** variëren, afhankelijk van de waarde die in het veld **Afschrijvingsjaar** is geselecteerd.

## <a name="select-a-depreciation-year"></a>Een afschrijvingsjaar selecteren
U kunt **Kalender** of **Fiscaal** selecteren in het veld **Afschrijvingsjaar** op de pagina **Afschrijvingsprofielen**. De standaardwaarde is **Kalender**. Uw keuze bepaalt welke opties beschikbaar zijn in het veld **Periodefrequentie**. Dit veld bepaalt voor het gehele jaar de boekingdatums en bedragen voor de toerekening van de afschrijving.

### <a name="calendar"></a>Kalender

Als u **Kalender** selecteert in het veld **_Afschrijvingsjaar_*_ wordt uitgegaan van een jaar van 1 januari t/m 31 december, zelfs als u de fiscale kalender anders hebt gedefinieerd. Met de optie _* Kalender** wordt de afschrijvingsbasis op 1 januari van elk jaar bijgewerkt. Doorgaans is de afschrijvingsbasis de nettoboekwaarde min de restwaarde. In het voorbeeld verderop in dit onderwerp is de afschrijvingsbasis de teller in de eerste expressie in de berekeningenkolom. Als u **Kalender** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:

- **Jaarlijks**: op 31 december wordt een bedrag geboekt.
- **Maandelijks**: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.
- **Driemaandelijks**: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.
- Met **Zesmaandelijks** wordt aan het einde van elk half jaar (30 juni en 31 december) een halfjaarlijks bedrag geboekt.
- **Dagelijks**: het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode wordt geboekt met één transactie voor elke dag.

Als u bijvoorbeeld **Jaarlijks** selecteert, wordt de jaarlijkse afschrijving wordt slechts één keer geboekt. Dit is telkens op 31 december. Als u **Maandelijks** selecteert, wordt de maandelijkse afschrijving elke maand als 1/12de van het jaarlijkse afschrijvingsbedrag geboekt.

### <a name="fiscal"></a>Fiscaal

Als u **Fiscaal** selecteert in het veld **Afschrijvingsjaar** wordt de lineaire resterende afschrijving van de levensduur gebruikt. Afschrijving wordt berekend op basis van de resterende boekjaren. Voor bijvoorbeeld het boekjaar van 1 juli 2015 t/m 30 juni 2016 wordt de afschrijving vanaf 1 juli berekend. Een boekjaar kan langer of korter dan 12 maanden zijn. De afschrijving wordt voor elke boekperiode aangepast. De lengte van het volgende boekjaar wordt bepaald door de boekperioden die zijn ingesteld op de pagina **Fiscale kalenders**. Als u **Fiscaal** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:

- **Jaarlijks** boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar als één bedrag op de laatste dag van het boekjaar.
- **Boekperiode** berekent het totale bedrag van de afschrijving voor het boekjaar. Dit bedrag wordt vervolgens toegerekend in de boekperioden die zijn gedefinieerd op de pagina **Fiscale kalenders** voor de fiscale kalender die is opgegeven voor het boek.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Voorbeeld van lineaire afschrijving van een ongewijzigd vast activum
Een vast activum heeft de volgende kenmerken.

| Veld               | Waarde  |
|:---------------------|--------:|
| Bijboekingskosten    | 11,000 |
| Restwaarde       | 1.000  |
| Afschrijvingsbasis   | 10.000 |
| Levensduur in jaren  | 5      |
| Jaarafschrijving | 2.000  |

Het afschrijvingsbedrag is elk jaar hetzelfde: (Verwervingskosten - restwaarde) ÷ Levensduur in jaren

| Periode | Berekening van het jaarlijkse afschrijvingsbedrag | Nettoboekwaarde aan het einde van het jaar |
|:--------:|:-----------------------------------------------|---------------------------------------:|
| Jaar 1 | (11.000 – 1000) ÷ 5 = 2000                  | 9000                                 |
| Jaar 2 | (9000 – 1000) ÷ 4 = 2000                   | 7.000                                 |
| Jaar 3 | (7000 – 1000) ÷ 3 = 2000                   | 5.000                                 |
| Jaar 4 | (5000 – 1000) ÷ 2 = 2000                   | 3000                                 |
| Jaar 5 | (3000 – 1000) ÷ 1 = 2000                   | 1.000                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
