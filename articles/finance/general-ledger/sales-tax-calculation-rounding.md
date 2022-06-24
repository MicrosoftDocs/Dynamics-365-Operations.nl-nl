---
title: Berekening en afronding van btw
description: In dit artikel wordt een overzicht gegeven van de berekening en afronding van btw. Ook worden de parameters van de instellingen voor berekening en afronding van btw uitgelegd.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939228"
---
# <a name="sales-tax-calculation-and-rounding"></a>Berekening en afronding van btw

[!include [banner](../includes/banner.md)]

Dit artikel biedt een overzicht van de berekening en afronding van btw in Microsoft Dynamics 365 Finance. Daarnaast worden de parameters uitgelegd die worden gebruikt bij het instellen van de berekening en afronding van btw en de manier waarop deze parameters samenwerken.

## <a name="parameters"></a>Parameters

De berekening en afronding van btw worden met verschillende parameters bepaald:

- **Berekeningsmethode**: deze parameter wordt ingesteld op de pagina **Grootboekparameters** en hiermee wordt bepaald of het btw-basisbedrag per document of per regel wordt berekend. Als de parameter **Marginale basis** voor de btw-code is ingesteld op **Nettobedrag van factuursaldo**, wordt het btw-basisbedrag altijd per document berekend, ongeacht de instelling van deze parameter.
- **Afronding door**: deze parameter wordt ingesteld voor de btw-groep en definieert of het btw-bedrag wordt afgerond per btw-code of per btw-codecombinatie.
- **Oorsprong**: deze parameter wordt ingesteld voor de btw-code en definieert hoe het btw-bedrag wordt berekend. Zie voor meer informatie [Btw-berekeningsmethoden in het veld Oorsprong](sales-tax-calculation-methods-origin-field.md).
- **Marginale basis**: deze parameter wordt ingesteld voor de btw-code en bepaalt welk bedrag wordt gebruikt om de juiste btw-tarieven te selecteren op de pagina **Waarden btw-code**. Zie voor meer informatie het onderwerp [Btw-tarieven op basis van Marginale basis en Berekeningsmethoden](marginal-base-field.md)
- **Btw-afrondingsregel**: deze parameter wordt ingesteld voor de btw-code en definieert hoe het bepaalde btw-bedrag wordt afgerond, inclusief de afrondingsprecisie en de afrondingsmethode.

In de rest van dit artikel worden enkele typische voorbeelden gegeven van btw-berekening en -afronding waarin een combinatie van de voorgaande parameters wordt gebruikt.

## <a name="scenario-for-the-examples"></a>Scenario voor de voorbeelden

- Het belastbare document bevat twee regels en het btw-basisbedrag voor elke regel is 42,42.
- Voor elke regel worden twee btw-codes gedefinieerd: btw-code 1 en btw-code 2.
- Het belastingtarief van zowel btw-code 1 als van btw-code 2 is 10 procent.
- De prijs is exclusief btw.
- De afrondingsprecisie is 0,01.
- De afrondingsmethode is **Naar boven afronden**.

## <a name="example-1"></a>Voorbeeld 1

### <a name="parameter-values"></a>Parameterwaarden

| Berekeningsmethode | Afronden op    | Oorsprong                   | Marginale basis       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Regel               | Btw-code | Percentage van nettobedrag | Nettobedrag per regel |

### <a name="calculation-and-rounding-behavior"></a>Berekenings- en afrondingsgedrag

| Regelnummer | Btw-code | Oorsprong van bedrag | Btw-bedrag |
| ------------| ---------------| --------------| -----------------|
| 1           | Code 1         | 42.42         | 4.25             |
| 1           | Code 2         | 42.42         | 4.25             |
| 2           | Code 1         | 42.42         | 4.25             |
| 2           | Code 2         | 42.42         | 4.25             |

Het btw-basisbedrag wordt per regel berekend:

- **Regel 1:** 42,42
- **Regel 2:** 42,42

Het btw-bedrag wordt berekend per btw-code:

- **Regel 1:**

    - Btw-bedrag voor btw-code 1 = 42,42 &times; 10 procent = 4,242
    - Btw-bedrag voor btw-code 2 = 42,42 &times; 10 procent = 4,242

- **Regel 2:**

    - Btw-bedrag voor btw-code 1 = 42,42 &times; 10 procent = 4,242
    - Btw-bedrag voor btw-code 2 = 42,42 &times; 10 procent = 4,242

Het btw-bedrag wordt afgerond per btw-code:

- **Regel 1:**

    - Afgerond btw-bedrag voor btw-code 1 = 4,25
    - Afgerond btw-bedrag voor btw-code 2 = 4,25

- **Regel 2:**

    - Afgerond btw-bedrag voor btw-code 1 = 4,25
    - Afgerond btw-bedrag voor btw-code 2 = 4,25

## <a name="example-2"></a>Voorbeeld 2

### <a name="parameter-values"></a>Parameterwaarden

| Berekeningsmethode | Afronden op    | Oorsprong                   | Marginale basis                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Regel/totaal         | Btw-code | Percentage van nettobedrag | Nettobedrag van factuursaldo |

### <a name="calculation-and-rounding-behavior"></a>Berekenings- en afrondingsgedrag

| Regelnummer | Btw-code | Oorsprong van bedrag | Btw-bedrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.25             |
| 1           | Code 2         | 42.42         | 4.25             |
| 2           | Code 1         | 42.42         | 4.24             |
| 2           | Code 2         | 42.42         | 4.24             |

Het btw-basisbedrag wordt per document berekend:

- Btw-basisbedrag = 42,42 + 42,42 = 84,84

Het btw-bedrag wordt berekend per btw-code:

- Btw-bedrag voor btw-code 1 = 84,84 &times; 10 procent = 8,484
- Btw-bedrag voor btw-code 2 = 84,84 &times; 10 procent = 8,484

Het btw-bedrag wordt afgerond per btw-code:

- Afgerond btw-bedrag voor btw-code 1 = 8,49
- Afgerond btw-bedrag voor btw-code 2 = 8,49

Het afgeronde btw-bedrag wordt toegewezen aan elke regel per btw-code:

- Wijs het afgeronde btw-bedrag voor btw-code 1 (8,49) toe aan regel 1 (4,25) en regel 2 (4,24).
- Wijs het afgeronde btw-bedrag voor btw-code 2 (8,49) toe aan regel 1 (4,25) en regel 2 (4,24).

## <a name="example-3"></a>Voorbeeld 3

### <a name="parameter-values"></a>Parameterwaarden

| Berekeningsmethode | Afronden op    | Oorsprong                              | Marginale basis       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Regel               | Btw-code | Berekende percentage van het nettobedrag | Nettobedrag per regel |

### <a name="calculation-and-rounding-behavior"></a>Berekenings- en afrondingsgedrag

| Regelnummer | Btw-code | Oorsprong van bedrag | Btw-bedrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.72             |
| 1           | Code 2         | 42.42         | 4.72             |
| 2           | Code 1         | 42.42         | 4.72             |
| 2           | Code 2         | 42.42         | 4.72             |

Het btw-basisbedrag wordt per regel berekend:

- **Regel 1:** 42,42
- **Regel 2:** 42,42

Het btw-bedrag wordt berekend per btw-code:

- **Regel 1:**

    - Btw-bedrag voor btw-code 1 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133
    - Btw-bedrag voor btw-code 2 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133

- **Regel 2:**

    - Btw-bedrag voor btw-code 1 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133
    - Btw-bedrag voor btw-code 2 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133

Het btw-bedrag wordt afgerond per btw-code:

- **Regel 1:**

    - Afgerond btw-bedrag voor btw-code 1 = 4,72
    - Afgerond btw-bedrag voor btw-code 2 = 4,72

- **Regel 2:**

    - Afgerond btw-bedrag voor btw-code 1 = 4,72
    - Afgerond btw-bedrag voor btw-code 2 = 4,72

## <a name="example-4"></a>Voorbeeld 4

### <a name="parameter-values"></a>Parameterwaarden

| Berekeningsmethode | Afronden op    | Oorsprong                              | Marginale basis                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Regel/totaal         | Btw-code | Berekende percentage van het nettobedrag | Nettobedrag van factuursaldo |

### <a name="calculation-and-rounding-behavior"></a>Berekenings- en afrondingsgedrag

| Regelnummer | Btw-code | Oorsprong van bedrag | Btw-bedrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.72             |
| 1           | Code 2         | 42.42         | 4.72             |
| 2           | Code 1         | 42.42         | 4.71             |
| 2           | Code 2         | 42.42         | 4.71             |

Het btw-basisbedrag wordt per document berekend:

- Btw-basisbedrag = 42,42 + 42,42 = 84,84

Het btw-bedrag wordt berekend per btw-code:

- Btw-bedrag voor btw-code 1 = 84,84 &times; 10 procent &divide; (1 – 10 procent) = 9,4267
- Btw-bedrag voor btw-code 2 = 84,84 &times; 10 procent &divide; (1 – 10 procent) = 9,4267

Het btw-bedrag wordt afgerond per btw-code:

- Afgerond btw-bedrag voor btw-code 1 = 9,43
- Afgerond btw-bedrag voor btw-code 2 = 9,43

Het afgeronde btw-bedrag wordt toegewezen aan elke regel per btw-code:

- Wijs het afgeronde btw-bedrag voor btw-code 1 (9,43) toe aan regel 1 (4,72) en regel 2 (4,71).
- Wijs het afgeronde btw-bedrag voor btw-code 2 (9,43) toe aan regel 1 (4,72) en regel 2 (4,71).

## <a name="example-5"></a>Voorbeeld 5

### <a name="parameter-values"></a>Parameterwaarden

| Berekeningsmethode | Afronden op                | Oorsprong                   | Marginale basis       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Regel               | Btw-codecombinatie | Percentage van nettobedrag | Nettobedrag per regel |

### <a name="calculation-and-rounding-behavior"></a>Berekenings- en afrondingsgedrag

| Regelnummer | Btw-code | Oorsprong van bedrag | Btw-bedrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.25             |
| 1           | Code 2         | 42.42         | 4.24             |
| 2           | Code 1         | 42.42         | 4.24             |
| 2           | Code 2         | 42.42         | 4.24             |

Het btw-basisbedrag wordt per regel berekend:

- **Regel 1:** 42,42
- **Regel 2:** 42,42

Het btw-bedrag wordt berekend per btw-code:

- **Regel 1:**

    - Btw-bedrag voor btw-code 1 = 42,42 &times; 10 procent = 4,242
    - Btw-bedrag voor btw-code 2 = 42,42 &times; 10 procent = 4,242

- **Regel 2:**

    - Btw-bedrag voor btw-code 1 = 42,42 &times; 10 procent = 4,242
    - Btw-bedrag voor btw-code 2 = 42,42 &times; 10 procent = 4,242

Het btw-bedrag wordt afgerond per btw-codecombinatie:

- Totaal btw-bedrag = 4,242 + 4,242 + 4,242 + 4,242 = 16,968. Dit wordt naar boven afgerond naar 16,97

Het afgeronde btw-bedrag wordt toegewezen aan elke regel per btw-code:

- Wijs het btw-bedrag (16,97) toe aan regel 1 en regel 2:

    - **Regel 1:**

        - Btw-bedrag voor btw-code 1 = 4,25
        - Btw-bedrag voor btw-code 2 = 4,24

    - **Regel 2:**

        - Btw-bedrag voor btw-code 1 = 4,24
        - Btw-bedrag voor btw-code 2 = 4,24

## <a name="example-6"></a>Voorbeeld 6

### <a name="parameter-values"></a>Parameterwaarden

| Berekeningsmethode | Afronden op                | Oorsprong                   | Marginale basis                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Regel/totaal         | Btw-codecombinatie | Percentage van nettobedrag | Nettobedrag van factuursaldo |

### <a name="calculation-and-rounding-behavior"></a>Berekenings- en afrondingsgedrag

| Regelnummer | Btw-code | Oorsprong van bedrag | Btw-bedrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.25             |
| 1           | Code 2         | 42.42         | 4.24             |
| 2           | Code 1         | 42.42         | 4.24             |
| 2           | Code 2         | 42.42         | 4.24             |

Het btw-basisbedrag wordt per document berekend:

- Btw-basisbedrag = 42,42 + 42,42 = 84,84

Het btw-bedrag wordt berekend per btw-code:

- Btw-bedrag voor btw-code 1 = 84,84 &times; 10 procent = 8,484
- Btw-bedrag voor btw-code 2 = 84,84 &times; 10 procent = 8,484

Het btw-bedrag wordt afgerond per btw-codecombinatie:

- Totaal btw-bedrag = 8,484 + 8,484 = 16,968. Dit wordt naar boven afgerond naar 16,97

Het afgeronde btw-bedrag wordt toegewezen aan elke regel per btw-code:

- Wijs het btw-bedrag (16,97) toe aan regel 1 en regel 2:

    - **Regel 1:**

        - Btw-bedrag voor btw-code 1 = 4,25
        - Btw-bedrag voor btw-code 2 = 4,24

    - **Regel 2:**

        - Btw-bedrag voor btw-code 1 = 4,24
        - Btw-bedrag voor btw-code 2 = 4,24

## <a name="example-7"></a>Voorbeeld 7

### <a name="parameter-values"></a>Parameterwaarden

| Berekeningsmethode | Afronden op                | Oorsprong                              | Marginale basis       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Regel               | Btw-codecombinatie | Berekende percentage van het nettobedrag | Nettobedrag per regel |

### <a name="calculation-and-rounding-behavior"></a>Berekenings- en afrondingsgedrag

| Regelnummer | Btw-code | Oorsprong van bedrag | Btw-bedrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.72             |
| 1           | Code 2         | 42.42         | 4.71             |
| 2           | Code 1         | 42.42         | 4.71             |
| 2           | Code 2         | 42.42         | 4.72             |

Het btw-basisbedrag wordt per regel berekend:

- **Regel 1:** 42,42
- **Regel 2:** 42,42

Het btw-bedrag wordt berekend per btw-code:

- **Regel 1:**

    - Btw-bedrag voor btw-code 1 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133
    - Btw-bedrag voor btw-code 2 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133

- **Regel 2:**

    - Btw-bedrag voor btw-code 1 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133
    - Btw-bedrag voor btw-code 2 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133

Het btw-bedrag wordt afgerond per btw-codecombinatie:

- Totaal btw-bedrag = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532. Dit wordt naar boven afgerond naar 18,86

Het afgeronde btw-bedrag wordt toegewezen aan elke regel per btw-code:

- Wijs het btw-bedrag (18,86) toe aan regel 1 en regel 2:

    - **Regel 1:**

        - Btw-bedrag voor btw-code 1 = 4,72
        - Btw-bedrag voor btw-code 2 = 4,71

    - **Regel 2:**

        - Btw-bedrag voor btw-code 1 = 4,71
        - Btw-bedrag voor btw-code 2 = 4,72

## <a name="example-8"></a>Voorbeeld 8

### <a name="parameter-values"></a>Parameterwaarden

| Berekeningsmethode | Afronden op                | Oorsprong                              | Marginale basis                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Regel/totaal         | Btw-codecombinatie | Berekende percentage van het nettobedrag | Nettobedrag van factuursaldo |

### <a name="calculation-and-rounding-behavior"></a>Berekenings- en afrondingsgedrag

| Regelnummer | Btw-code | Oorsprong van bedrag | Btw-bedrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.72             |
| 1           | Code 2         | 42.42         | 4.71             |
| 2           | Code 1         | 42.42         | 4.71             |
| 2           | Code 2         | 42.42         | 4.72             |

Het btw-basisbedrag wordt per document berekend:

- Btw-basisbedrag = 42,42 + 42,42 = 84,84

Het btw-bedrag wordt berekend per btw-code:

- Btw-bedrag voor btw-code 1 = 84,84 &times; 10 procent &divide; (1 – 10 procent) = 9,4267
- Btw-bedrag voor btw-code 2 = 84,84 &times; 10 procent &divide; (1 – 10 procent) = 9,4267

Het btw-bedrag wordt afgerond per btw-codecombinatie:

- Totaal btw-bedrag = 9,4267 + 9,4267 = 18,8534. Dit wordt naar boven afgerond naar 18,86

Het afgeronde btw-bedrag wordt toegewezen aan elke regel per btw-code:

- Wijs het btw-bedrag (18,86) toe aan regel 1 en regel 2:

    - **Regel 1:**

        - Btw-bedrag voor btw-code 1 = 4,72
        - Btw-bedrag voor btw-code 2 = 4,71

    - **Regel 2:**

        - Btw-bedrag voor btw-code 1 = 4,71
        - Btw-bedrag voor btw-code 2 = 4,72

## <a name="additional-resources"></a>Aanvullende bronnen

- [Btw-berekeningsmethoden in het veld Oorsprong](sales-tax-calculation-methods-origin-field.md)
- [Btw-tarieven op basis van Marginale basis en Berekeningsmethoden](marginal-base-field.md)
- [Berekeningsopties Volledige bedrag en interval voor btw-codes](whole-amount-interval-options-sales-tax-codes.md)
