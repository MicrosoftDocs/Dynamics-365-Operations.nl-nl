---
title: Valutaherwaardering in een consolidatiebedrijf
description: In dit artikel wordt beschreven hoe valuta wordt geherwaardeerd in een consolidatiebedrijf.
author: aprilolson
ms.date: 10/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c05ef0d4d05d5113d3b858dafe49ee9c1c7211d9
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779657"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Valutaherwaardering in een consolidatiebedrijf

[!include [banner](../includes/banner.md)]

Wanneer u gegevens van een valuta voor boekhouding naar een andere consolideert, moet u herwaardering alsnog uitvoeren als er een wijziging in wisselkoersen is, zodat de rekeningsaldo's correct worden geherwaardeerd. Als u oorspronkelijk de gegevens consolideert, gebruik het **Valutaomzetting** tabblad om de oorspronkelijke wisselkoers te selecteren voor vertaling tijdens het consolidatieproces. Nadat een nieuwe wisselkoers (bijvoorbeeld in de volgende maand) is ingevoerd, moet u de rekeningsaldo's herwaarderen. De ongerealiseerde winst of verlies worden vervolgens overeenkomstig bijgewerkt, op basis van de nieuwe wisselkoers en datum. Het volgende voorbeeld illustreert de journaalregels die tijdens het proces zijn gemaakt.

## <a name="company-setup"></a>Bedrijfsinstellingen
-   **Bron/werken bedrijf (USMF)** - Amerikaanse dollars (USD) worden gebruikt als boekhouding- en aangiftevaluta.
-   **Geconsolideerd bedrijf (CON)** Euro's (EUR) worden gebruikt als de boekhouding- en aangiftevaluta.
    -   **Gerealiseerde winst** – Grootboekrekening 801500
    -   **Gerealiseerd verlies**– Grootboekrekening 801600
    -   **Ongerealiseerde winst** - Grootboekrekening 801600
    -   **Ongerealiseerd verlies** - Grootboekrekening 801400

## <a name="original-transactions"></a>Oorspronkelijke transacties
### <a name="cash-receipt-transactions-in-usmf"></a>Kasontvangsttransacties in USMF

| Datum       | Grootboekrekening               | Valuta | Bedrag |
|------------|------------------------------|----------|--------|
| 10/11/2020 | 110110 - Contant geld                | USD      | 500    |
| 10/11/2020 | 130100 - Debiteuren | USD      | -500   |

## <a name="exchange-rates"></a>Wisselkoersen

| Vanuit valuta | Naar valuta | Begindatum | Wisselkoers |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 10/1/2020  | 200           |
| EUR           | USD         | 11/1/2020  | 150           |
| EUR           | USD         | 12/1/2017  | 100           |

## <a name="perform-the-consolidation-for-october-2020"></a>Voer de consolidatie voor Oktober 2020 uit
### <a name="balances-in-the-consolidation-company"></a>Saldi in het consolidatiebedrijf

| Grootboekrekening | Valuta | Bedrag | Berekening    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50%  |
| 130100         | EUR      | -250   | -500 USD × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-november-30-2020"></a>Voer de valuta herwaardering voor de rekeningen van 1 oktober 2020, tot en met 30 november 2020
### <a name="balances-in-the-consolidation-company"></a>Saldi in het consolidatiebedrijf

| Grootboekrekening | Valuta | Bedrag  | Berekening                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333.33  | Oorspronkelijk bedrag van 500 × 66,6667%%  |
| 130100         | EUR      | -333.33 | Oorspronkelijk bedrag van -500 × 66,6667%% |
| 801400         | EUR      | 83.33   | 333.33 – 250                       |
| 801600         | EUR      | -83.33  | -333.33 – (-250)                   |

U kunt extra transacties voor de aangiftevalutabedragen zien.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-december-31-2020"></a>Voer de valuta herwaardering voor de rekeningen van 1 oktober 2020 tot en met 31 december 2020
### <a name="balances-in-the-consolidation-company"></a>Saldi in het consolidatiebedrijf

| Grootboekrekening | Valuta | Bedrag  | Berekening                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Oorspronkelijk bedrag van 500 × 1                           |
| 130100         | EUR      | -500,00 | Oorspronkelijk bedrag van -500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
