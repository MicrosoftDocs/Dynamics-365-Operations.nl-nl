---
title: Reductiesleutels van prognose
description: Dit onderwerp bevat voorbeelden waarin het instellen van een reductiesleutel wordt getoond. Het bevat informatie over de verschillende reductiesleutelinstellingen en de resultaten van elk. U kunt een reductiesleutel gebruiken om te definiëren hoe prognosebehoeften worden gereduceerd.
author: roxanadiaconu
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 555f75df1b28d374f2a46481857902c2f9315809c082699355190c54e856899b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736618"
---
# <a name="forecast-reduction-keys"></a>Reductiesleutels van prognose

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over de verschillende methoden die worden gebruikt om prognosebehoeften te reduceren. Het bevat voorbeelden van de resultaten van elke methode. Ook wordt uitgelegd hoe u een prognosereductiesleutel kunt maken, instellen en gebruiken. Bij sommige methoden wordt een prognosereductiesleutel gebruikt om prognosebehoeften te reduceren.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Methoden die worden gebruikt om prognosebehoeften te reduceren

Wanneer u een prognose in een hoofdplan opneemt, kunt u selecteren hoe de prognosebehoeften worden gereduceerd wanneer werkelijke vraag wordt opgenomen. In de hoofdplanning worden prognosebehoeften uit het verleden uitgesloten, dat wil zeggen alle prognosebehoeften vóór de huidige datum.

Als u een prognose wilt opnemen in een hoofdplan en de methode wilt selecteren die wordt gebruikt om prognosebehoeften te reduceren, gaat u naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**. Selecteer in het veld **Prognosemodel** een prognosemodel. Selecteer een methode in het veld **Gebruikte methode voor het reduceren van prognosebehoeften**. De volgende opties zijn beschikbaar:

- Geen
- Percentage - reductiesleutel
- Transacties - reductiesleutel
- Transacties - dynamische periode

De volgende secties bevatten meer informatie over elke optie.

### <a name="none"></a>Geen

Als u **Geen** selecteert, worden de prognosebehoeften niet gereduceerd tijdens de hoofdplanning. In dit geval worden in de hoofdplanning geplande orders gemaakt voor het leveren van de geraamde vraag (prognosebehoeften). Deze geplande orders behouden de voorgestelde hoeveelheid, ongeacht andere soorten vraag. Als bijvoorbeeld verkooporders worden geplaatst, worden in de hoofdplanning extra geplande orders gemaakt voor het leveren van de verkooporders. De hoeveelheid van de prognosebehoeften wordt niet gereduceerd.

### <a name="percent--reduction-key"></a>Percentage - reductiesleutel

Als u **Percentage - reductiesleutel** selecteert, worden de prognosebehoeften gereduceerd volgens de percentages en perioden die zijn gedefinieerd door de reductiesleutel. In dit geval worden in de hoofdplanning geplande orders gemaakt waarin de hoeveelheid wordt berekend als de geraamde hoeveelheid × reductiesleutel in elke periode. Als er andere soorten vraag zijn, worden in de hoofdplanning ook geplande orders gemaakt voor het leveren van die vraag.

#### <a name="example-percent--reduction-key"></a>Voorbeeld: percentage - reductiesleutel

In dit voorbeeld wordt weergegeven hoe een reductiesleutel vraagprognosebehoeften reduceert overeenkomstig de percentages en perioden die door de reductiesleutel worden gedefinieerd.

Voor dit voorbeeld neemt u de volgende vraagprognose in een hoofdplan op.

| Maand    | Vraagprognose |
|----------|-----------------|
| januari  | 1.000           |
| Februari | 1.000           |
| maart    | 1.000           |
| april    | 1.000           |

Op de pagina **Reductiesleutels** stelt u de volgende regels in.

| Wisselgeld | Eenheid  | Percentage |
|--------|-------|---------|
| 1      | Maand | 100     |
| 2      | Maand | 75      |
| 3      | Maand | 50      |
| 4      | Maand | 25      |

U wijst de reductiesleutel aan de behoefteplanningsgroep van het artikel toe. Selecteer vervolgens op de pagina **Hoofdplannen** in het veld **Methode gebruikt voor het reduceren van prognosebehoeften** **Percentage - reductiesleutel**.

In dit geval worden, als u de prognoseplanning op 1 januari uitvoert, de vraagprognosebehoeften verbruikt volgens de percentages die u instelt op de pagina **Reductiesleutels**. De volgende behoeftehoeveelheden worden naar het hoofdplan overgebracht.

| Maand                | Hoeveelheid geplande order | Berekening    |
|----------------------|------------------------|----------------|
| januari              | 0                      | = 0% × 1.000   |
| Februari             | 250                    | = 25% × 1.000  |
| maart                | 500                    | = 50% × 1.000  |
| april                | 750                    | = 75% × 1.000  |
| Mei tot en met december | 1.000                  | = 100% × 1.000 |

### <a name="transactions--reduction-key"></a>Transacties - reductiesleutel

Als u **Transacties - reductiesleutel** selecteert, worden de prognosebehoeften gereduceerd door de transacties die plaatsvinden tijdens de perioden die worden gedefinieerd door de reductiesleutel.

#### <a name="example-transactions--reduction-key"></a>Voorbeeld: Transacties - reductiesleutel

In dit voorbeeld wordt weergegeven hoe werkelijke orders, die plaatsvinden tijdens de perioden die zijn gedefinieerd door de reductiesleutel, vraagprognosebehoeften reduceren.

Voor dit voorbeeld selecteert u **Transacties - reductiesleutel** in het veld **Methode gebruikt voor het reduceren van prognosebehoeften** op de pagina **Hoofdplannen**.

Op 1 januari waren er de volgende verkooporders.

| Maand    | Besteld aantal stuks |
|----------|--------------------------|
| januari  | 956                      |
| februari | 1.176                    |
| maart    | 451                      |
| april    | 119                      |

Als u dezelfde vraagprognose (van het vorige voorbeeld) van 1000 stuks per maand gebruikt, worden de volgende behoeftehoeveelheden naar het hoofdplan overgebracht.

| Maand                | Benodigd aantal stuks |
|----------------------|---------------------------|
| januari              | 44                        |
| Februari             | 0                         |
| maart                | 549                       |
| april                | 881                       |
| Mei tot en met december | 1.000                     |

### <a name="transactions--dynamic-period"></a>Transacties - dynamische periode

Als u **Transacties - dynamische periode** selecteert, worden de prognosebehoeften gereduceerd met de werkelijke ordertransacties die tijdens de dynamische periode plaatsvinden. De dynamische periode bestrijkt de huidige prognosedatums en eindigt bij het begin van de volgende prognose. In dit geval worden in de hoofdplanning geplande orders gemaakt voor het leveren van de geraamde vraag (prognosebehoeften). Wanneer echter werkelijke ordertransacties worden geplaatst, worden de prognosebehoeften gereduceerd. De werkelijke transacties verbruiken een gedeelte van de geraamde behoeften.

Wanneer deze optie wordt gebruikt, vindt het volgende gedrag plaats:

- Reductiesleutels worden niet vereist of gebruikt. 
- Als de prognose volledig is gereduceerd, worden de prognosebehoeften voor de huidige prognose 0 (nul).
- Als er geen toekomstige prognose is, worden de prognosebehoeften van de laatste prognose die is ingevoerd, gereduceerd.
- De timefences worden opgenomen in de berekening van de prognosereductie.
- Positieve dagen zijn opgenomen in de berekening van de prognosereductie.
- Als de werkelijke ordertransacties de prognosebehoeften overschrijden, worden de resterende transacties niet naar de volgende prognoseperiode doorgestuurd.

#### <a name="example-1-transactions--dynamic-period"></a>Voorbeeld 1: Transacties - dynamische periode

Hier vindt u een eenvoudig voorbeeld dat laat zien hoe de methode **Transacties - dynamische periode** werkt.

Voor dit voorbeeld neemt u de volgende vraagprognose in een hoofdplan op.

| Datum       | Vraagprognose |
|------------|-----------------|
| 1 januari  | 1.000           |
| 1 februari | 1.000             |

U maakt ook de volgende verkooporders.

| Datum        | Verkooporderhoeveelheid |
|-------------|----------------------|
| 15 januari  | 200                  |
| 15 februari | 400                  |

In dit geval worden de volgende geplande orders gemaakt.

| Vraagprognosedatum | Hoeveelheid | Uitleg                           |
|--------------------- |----------|---------------------------------------|
| 1 januari            | 800      | Prognosebehoeften (= 1.000 – 200) |
| 15 januari           | 200      | Verkooporderbehoeften             |
| 1 februari           | 600      | Prognosebehoeften (= 1.000 – 400) |
| 15 februari          | 400      | Verkooporderbehoeften             |

#### <a name="example-2-transactions--dynamic-period"></a>Voorbeeld 2: Transacties - dynamische periode

In de meeste gevallen worden systemen zo ingesteld dat met transacties vraagprognose worden gereduceerd in specifieke prognoseperioden: weken, maanden enzovoort. Deze perioden worden gedefinieerd in de reductiesleutel. De tijd tussen twee vraagprognoseregels kan echter ook een periode *impliceren*.

Voor dit voorbeeld maakt u een vraagprognose voor de volgende datums en hoeveelheden.

| Datum       | Vraagprognose |
|------------|-----------------|
| 1 januari  | 1.000           |
| 5 januari  | 500             |
| 12 januari | 1.000           |

U ziet dat in deze prognose er geen duidelijke periode tussen de prognosedatums is. Tussen de eerste en tweede datum bevindt zich een periode van vier dagen en tussen de tweede en derde datum bevindt zich een periode van zeven dagen. Deze perioden zijn de dynamische perioden.

U maakt ook de volgende verkooporderregels.

| Datum                             | Verkooporderhoeveelheid |
|----------------------------------|----------------------|
| 15 december in het vorige jaar | 500                  |
| 3 januari                        | 100                  |
| 10 januari                       | 200                  |

In dit geval wordt de prognose op de volgende manier gereduceerd:

- Omdat de eerste verkooporder in geen enkele periode valt, wordt hiermee geen prognose gereduceerd.
- Omdat de tweede verkooporder tussen 1 januari en 5 januari ligt, wordt hiermee de prognose voor 1 januari met 100 gereduceerd.
- Omdat de derde verkooporder tussen 5 januari en 12 januari ligt, wordt hiermee de prognose voor 5 januari met 200 gereduceerd.

Daarom worden de volgende geplande orders gemaakt.

| Vraagprognosedatum             | Hoeveelheid | Uitleg                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 15 december in het vorige jaar | 500      | Verkooporderbehoeften                                            |
| 1 januari                        | 900      | Periode van prognosebehoeften 1 januari tot en met 5 januari (= 1.000 - 100) |
| 3 januari                        | 100      | Verkooporderbehoeften                                            |
| 5 januari                        | 300      | Periode van prognosebehoeften 5 januari tot en met 10 januari (= 500 - 200)  |
| 12 januari                       | 1.000    | Periode van prognosebehoeften 12 januari tot einde                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Een prognosereductiesleutel maken en instellen

Een prognosereductiesleutel wordt gebruikt in de methoden **Transacties - reductiesleutel** en **Percentage - reductiesleutel** voor het reduceren van prognosebehoeften. Voer deze stappen uit om een reductiesleutel te maken en in te stellen.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanning \> Reductiesleutels**.
2. Selecteer **Nieuw** om een reductiesleutel te maken.
3. Voer in het veld **Reductiesleutel** een unieke id voor de prognosereductiesleutel in. Voer vervolgens in het veld **Naam** een naam in. 
4. Definieer de perioden en het reductiesleutelpercentage in elke periode:

    - Met het veld **Ingangsdatum** wordt de datum aangegeven waarop het maken van de perioden wordt gestart. Wanneer de optie **De ingangsdatum gebruiken** is ingesteld op **Ja**, beginnen de perioden op de ingangsdatum. Als deze is ingesteld op **Nee**, begint de periode op de datum waarop de hoofdplanning wordt uitgevoerd.
    - Definieer de perioden gedurende welke de prognosereductie moet plaatsvinden.
    - Geef voor een bepaalde periode de percentages op waarmee de prognosebehoeften moeten worden gereduceerd. U kunt positieve waarden invoeren om de behoeften te verminderen of negatieve waarden om de behoeften te vergroten.

## <a name="use-a-reduction-key"></a>Een reductiesleutel gebruiken

Een prognosereductiesleutel moet worden toegewezen aan de behoefteplanningsgroep van het artikel. Voer deze stappen uit voor het toewijzen van een reductiesleutel aan de behoefteplanningsgroep van een artikel.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanning \> Behoefteplanningsgroepen**.
2. Selecteer in het veld **Reductiesleutel** op het sneltabblad **Overige** de reductiesleutel die u aan de behoefteplanningsgroep wilt toewijzen. De reductiesleutel wordt vervolgens toegepast op alle artikelen van de behoefteplanningsgroep.
3. Als u een reductiesleutel wilt gebruiken om tijdens de hoofdplanning een prognose reductie te berekenen, moet u deze instelling opgeven in de instellingen van het prognoseplan of het hoofdplan. Ga naar een van de volgende locaties:

    - Hoofdplanning \> Instellen \> Plannen \> Prognoseplannen
    - Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen

4. Selecteer op de pagina **Prognoseplannen** of **Hoofdplannen** op het sneltabblad **Algemeen** in het veld **Gebruikte methode voor het reduceren van prognosebehoeften** **Percentage - reductiesleutel** of **Transacties - reductiesleutel**.

## <a name="reduce-a-forecast-by-transactions"></a>Een prognose op basis van transacties reduceren

Wanneer u **Transacties - reductiesleutel** of **Transacties - dynamische periode** selecteert als de methode voor het reduceren van prognosebehoeften, kunt u opgeven met welke transacties de prognose wordt gereduceerd. Selecteer op de pagina **Behoefteplanningsgroepen** op het sneltabblad **Overige** in het veld **Prognose reduceren met** **Alle transacties** als de prognose moeten worden gereduceerd met alle transacties of **Orders** als de prognose alleen met verkooporders moet worden gereduceerd.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Hoofdplannen](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]