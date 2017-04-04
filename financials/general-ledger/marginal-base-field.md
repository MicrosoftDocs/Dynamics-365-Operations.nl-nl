---
title: Btw-tarieven gebaseerd op de marginale basis- en berekeningsmethoden
description: In dit artikel wordt beschreven hoe de waarden in de velden Marginale basis en Berekeningsmethode het btw-tarief in verkoop- en inkooptransacties bepalen.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ad731401fe553cdc50665cc87aaac64dc48813f2
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Btw-tarieven gebaseerd op de marginale basis- en berekeningsmethoden

In dit artikel wordt beschreven hoe de waarden in de velden Marginale basis en Berekeningsmethode het btw-tarief in verkoop- en inkooptransacties bepalen.

De marginale basis op het sneltabblad Berekening van de pagina Btw-codes bepaalt welk bedrag wordt gebruikt om het gewenste btw-tarief te kiezen uit de percentages op de pagina Waarden btw-code. Het bedragtype in het veld Marginale basis, in combinatie met de methode in het veld Berekeningsmethode, definieert de logica om het juiste btw-tarief voor een transactie te bepalen. 

Verschillende combinaties van waarden in deze velden resulteren in heel verschillende btw-berekeningen, zoals u in de volgende voorbeelden kunt zien. In de voorbeelden worden dezelfde btw-intervalwaarden gebruikt die zijn ingesteld voor elke btw-code op de pagina Waarden btw-code. U opent deze pagina, klikt u op btw-code &gt;waarden in de btw-codes-pagina.

> [!Important]                                                                                                                  
> Als de marginale basis voor een of meer van uw btw-codes is gebaseerd op een regelbedragen of eenheden, moet de waarde van het veld Berekeningsmethode op de pagina Grootboekparameters zijn ingesteld op Regel. |

## <a name="net-amount-per-line"></a>Nettobedrag per regel
Selecteer deze optie om de btw-tarieven te berekenen op basis van het nettobedrag voor de factuurregels, exclusief eventuele overige belastingen.

### <a name="example"></a>voorbeeld

De btw-tarieven worden ingesteld met de volgende intervallen:

| Bedraginterval    | Btw-tarief |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

> [!NOTE]                                                                                                             
> De bovengrens van nul (0) in het laatste interval betekent dat alle bedragen die hoger zijn dan 100, worden opgenomen in het interval.

Marginale basis: **nettobedrag per regel** 

Berekeningsmethode: **Interval** 

U koopt 8 lampen die 25,00 per stuk kosten. 

Het nettobedrag voor de factuurregel is EUR 200,00. 

De btw wordt als volgt berekend: 

Totale btw = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = EUR 35,00. 

Totaal factuurbedrag = 200,00 + 35,00 = EUR 235,00. 

**Variation** 

Als de factuur twee regels met 4 artikelen op elke regel heeft het nettobedrag op elke regel is 100,00 en de btw wordt als volgt berekend: 

Btw-regel 1 = 50 x 30% + 50 x 20% = 15 + 10 = EUR 25,00. 

Btw-regel 2 = 50 x 30% + 50 x 20% = 15 + 10 = EUR 25,00. 

Totale btw = 25,00 + 25,00 = EUR 50,00 

Totaal factuurbedrag = 200,00 + 50,00 = EUR 250,00.

## <a name="net-amount-per-unit"></a>Nettobedrag per eenheid
Selecteer deze optie om het btw-tarief te berekenen op basis van de waarde van elke eenheid, exclusief eventuele overige belastingen. Als een marginale basis op basis van een eenheid is geselecteerd, dan moet voor de btw-code ook een eenheid worden opgegeven.

### <a name="example"></a>Voorbeeld

De btw-tarieven worden ingesteld met de volgende intervallen:

| Bedrag             | Btw-tarief |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginale basis: **netto bedrag per eenheid** 

Berekeningsmethode: **volledige bedrag** 

U koopt 8 lampen die 25,00 per stuk kosten. 

Het nettobedrag voor de factuurregel is EUR 200,00. 

De btw wordt als volgt berekend: Btw per eenheid = 25,00 x 30% = 7,50 Totale btw = 7,50 x 8 eenheden = 60,00 Totaal factuurbedrag = 200,00 + 60,00 = 260,00

## <a name="net-amount-of-invoice-balance"></a>Nettobedrag van factuursaldo

Selecteer deze optie om het btw-tarief te berekenen op basis van de totale waarde van de factuur, exclusief eventuele overige belastingen.

### <a name="example"></a>voorbeeld

De btw-tarieven worden ingesteld met de volgende intervallen:

| Bedrag            | Btw-tarief |
|-------------------|----------|
| 0 - 50            | 30%      |
| 50 - 100          | 20%      |
| 100 -0 (&gt; 100) | 10%      |

Marginale basis: **nettobedrag van factuursaldo** 

Berekeningsmethode: **Interval** een verkoopfactuur bevat 2 regels met de 4 lampen op elke regels voor 25,00 per stuk. Het nettobedrag van factuursaldo is 4 x 25,00 + 4 x 25,00 = 200,00. De btw wordt als volgt berekend: Totale btw = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Totaal factuurbedrag = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a>Brutobedrag per regel

Selecteer deze optie om het btw-tarief te berekenen op basis van de waarde van de regel, inclusief alle overige belastingen voor die regel.

> [!NOTE]
> In een btw-groep kunt u maar één btw-code met deze selectie hebben in het veld Marginale basis.

### <a name="example"></a>Voorbeeld

De btw-tarieven worden ingesteld met de volgende intervallen:

| Bedrag             | Btw-tarief |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginale basis: **Brutobedrag per regel** Berekeningsmethode: **Interval** Daarnaast is er een andere btw-code voor berekening van een speciale heffing van 5,00 op elke lamp. De heffing wordt toegevoegd aan het nettobedrag voordat de btw wordt berekend. U koopt 8 lampen die 25,00 per stuk kosten. Het nettobedrag voor de factuurregel is EUR 200,00. Het brutobedrag voor de factuurregel is 8 x 25,00 + 8 x 5,00 = 240,00. De btw wordt als volgt berekend: totale btw = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 totaal aan heffingen = 5,00 x 8 = EUR 40,00 Totaal factuurbedrag = 200,00 + 39,00 + 40,00 = EUR 279,00.

**Variation** 

Als de factuur wordt gemaakt met 2 factuurregels met 4 artikelen op elke regel, is het nettobedrag per factuurregel EUR 100,00. Het brutobedrag (inclusief de heffing van 4 x 5,00) per factuurregel zou 120,00 bedragen, en de btw wordt als volgt opgesteld: Btw factuurregel 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Btw factuurregel 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Totale btw = 27,00 + 27,00 = 54,00 Totale heffing = 5,00 x 8 = 40,00 Totaal factuurbedrag = 200,00 + 54,00 + 40,00 = 294,00

## <a name="gross-amount-per-unit"></a>Brutobedrag per eenheid

Selecteer deze optie om het btw-tarief te berekenen op basis van de waarde van de eenheid, inclusief eventuele overige belastingen.

> [!NOTE]
> In een btw-groep kunt u maar één btw-code met deze selectie hebben in het veld Marginale basis.

### <a name="example"></a>Voorbeeld

De btw-tarieven worden ingesteld met de volgende intervallen:

| Bedrag             | Btw-tarief |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginale basis: **Brutobedrag per eenheid** Er is een speciale heffing van 5,00 op elke lamp. De heffing wordt toegevoegd aan het nettobedrag voordat de btw wordt berekend. U koopt 8 lampen die 25,00 per stuk kosten. Het brutobedrag per eenheid is EUR 30,00. De btw wordt als volgt berekend: Btw per eenheid = 30 x 30% = 9,00 Totale btw = 9,00 x 8 = 72,00 Totale heffing = 5,00 x 8 = 40,00 Totaal factuurbedrag = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a>Factuurtotaal incl. andere btw

Selecteer deze optie om het btw-tarief te berekenen op basis van de totale waarde van de factuur, inclusief eventuele overige belastingen.
> [!NOTE]
> In een btw-groep, kunt u slechts één btw-code met deze selectie hebben in het veld Marginale basis

### <a name="example"></a>Voorbeeld

De btw-tarieven worden ingesteld met de volgende intervallen:

| Bedrag             | Btw-tarief |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginale basis: **factuur Totaal incl. andere btw-bedragen** berekeningsmethode: **Interval**   
Op elke lamp is een speciale heffing van toepassing van EUR 5,00. De heffing wordt toegevoegd aan het nettobedrag voordat de btw wordt berekend. U koopt 8 lampen die 25,00 per stuk kosten. Het nettobedrag voor de factuur is EUR 200,00. Het brutobedrag voor de factuur is 200,00 + (8 x 5,00) = EUR 240,00. De btw wordt als volgt berekend: Totale btw = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Totale heffing = 5,00 x 8 = 40,00 Totaal factuurbedrag = 200,00 + 39,00 + 40,00 = 279,00

Zie voor meer informatie [gehele bedrag en de berekeningsopties Interval voor btw-codes](whole-amount-interval-options-sales-tax-codes.md) en [btw-berekeningsmethoden in het veld oorsprong](sales-tax-calculation-methods-origin-field.md).


