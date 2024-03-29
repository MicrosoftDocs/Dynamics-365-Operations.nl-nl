---
title: Berekeningsopties Volledige bedrag en Interval voor btw-codes
description: In dit artikel worden de opties voor het veld Berekeningsmethode voor btw-codes uitgelegd en wordt uitgelegd hoe btw wordt berekend voor intervallen en gehele bedragen.
author: kailiang
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b81780e60825021ad7a700d85257ba0f5a2447a
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715236"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Berekeningsopties Volledige bedrag en Interval voor btw-codes

[!include [banner](../includes/banner.md)]

In dit artikel worden de opties voor het veld **Berekeningsmethode** voor btw-codes uitgelegd en wordt uitgelegd hoe btw wordt berekend voor intervallen en gehele bedragen.

U kunt een btw-code instellen die moet worden berekend op basis van het gehele bedrag of een intervalbedrag. Gebruik op de pagina **Btw-codes** het veld **Berekeningsmethode** op het sneltabblad **Berekening** om te selecteren hoe u een btw-code berekent.
- Volledige bedrag – Het btw-tarief wordt toegepast op het gehele belastbare bedrag.
- Interval – Het belastbare bedrag is verdeeld in delen en elk deel valt in een bereik met een bepaald btw-tarief. Het deel van het bedrag dat in een bepaald interval valt, wordt belast volgens het btw-tarief voor dat interval. De btw is de som van de btw-bedragen die worden berekend voor elk intervalbedrag.
  > [!NOTE]                                                                                                                              
  > De optie Interval is alleen beschikbaar wanneer u Regel selecteert in het veld Berekeningsmethode in het btw-gebied van de pagina Grootboekparameters. 

Intervallen worden ingesteld op de pagina Waarden btw-code door bedragen voor Ondergrens en Bovengrens in te voeren per btw-tarief. Voor btw die moet worden berekend over alle belastbare bedragen - ongeacht welke berekeningsmethode is geselecteerd - moeten de intervallen voldoen aan de volgende regels:
-   Het eerste interval moet een ondergrens van nul hebben.
-   Het laatste interval moet een bovengrens van nul hebben, wat oneindig betekent.
-   De bovengrens van een interval moet de ondergrens van het volgende interval zijn.

Als een bedrag de bovengrens van het vorige interval en de ondergrens van het volgende interval is, wordt het tarief van het eerste interval toegepast op het bedrag. Als een bedrag buiten de intervallen valt die zijn gedefinieerd door de boven- en ondergrens, wordt een btw-tarief van 0 toegepast.

## <a name="example-whole-amount-method-of-calculation"></a>Voorbeeld: Berekeningsmethode is volledige bedrag
Op de pagina Waarden btw-code worden de btw-tarieven ingesteld met de volgende intervallen:

| Ondergrens     | Bovengrens     | Btw-tarief     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30%          |
| 50,00             | 100,00            | 20%          |
| 100,00            | 0,00              | 10%          |

De btw wordt berekend op het volledige belastbare bedrag.

| Belastbaar bedrag (prijs) | Berekening    | Btw |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | EUR 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a>Voorbeeld: Berekeningsmethode Interval
Op de pagina Waarden worden de btw-tarieven ingesteld met de volgende intervallen:

| Ondergrens     | Bovengrens     | Btw-tarief     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30%          |
| 50,00             | 100,00            | 20%          |
| 100,00            | 0,00              | 10%          |

De btw is de som van de btw-bedragen die worden berekend voor elk intervalbedrag.

| Belastbaar bedrag (prijs) | Berekening                                                               | Btw |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | EUR 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Zie voor meer informatie het onderwerp [Btw-tarieven op basis van Marginale basis en Berekeningsmethoden](marginal-base-field.md)







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
