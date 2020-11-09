---
title: Valutaherwaardering in een consolidatiebedrijf
description: In dit onderwerp wordt beschreven hoe valuta wordt geherwaardeerd in een consolidatiebedrijf.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33db12388c969b8dadb38bfacf4d9df333b78bd4
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014978"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Valutaherwaardering in een consolidatiebedrijf

[!include [banner](../includes/banner.md)]

Wanneer u gegevens van een valuta voor boekhouding naar een andere consolideert, moet u herwaardering alsnog uitvoeren als er een wijziging in wisselkoersen is, zodat de rekeningsaldo's correct worden geherwaardeerd. Als u oorspronkelijk de gegevens consolideert, gebruik het **Valutaomzetting** tabblad om de oorspronkelijke wisselkoers te selecteren voor vertaling tijdens het consolidatieproces. Nadat een nieuwe wisselkoers (bijvoorbeeld in de volgende maand) is ingevoerd, moet u de rekeningsaldo's herwaarderen. De ongerealiseerde winst of verlies worden vervolgens overeenkomstig bijgewerkt, op basis van de nieuwe wisselkoers en datum. Het volgende voorbeeld illustreert de journaalregels die tijdens het proces zijn gemaakt.

## <a name="company-setup"></a>Bedrijfsinstellingen
-   **Bron/werken bedrijf (USMF)** - Amerikaanse dollars (USD) worden gebruikt als boekhouding- en aangiftevaluta.
-   **Geconsolideerd bedrijf (CON)** Euro's (EUR) worden gebruikt als de boekhouding- en aangiftevaluta.
    -   **Gerealiseerde winst** – Grootboekrekening 801500
    -   **Gerealiseerd verlies** – Grootboekrekening 801600
    -   **Ongerealiseerde winst** - Grootboekrekening 801600
    -   **Ongerealiseerd verlies** - Grootboekrekening 801400

## <a name="original-transactions"></a>Oorspronkelijke transacties
### <a name="cash-receipt-transactions-in-usmf"></a>Kasontvangsttransacties in USMF

| Datum       | Grootboekrekening               | Valuta | Bedrag |
|------------|------------------------------|----------|--------|
| 10/11/2015 | 110110 - Contant geld                | USD      | 500    |
| 10/11/2015 | 130100 - Debiteuren | USD      | -500   |

## <a name="exchange-rates"></a>Wisselkoersen

| Vanuit valuta | Naar valuta | Begindatum | Wisselkoers |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 10/1/2015  | 200           |
| EUR           | USD         | 11/1/2015  | 150           |
| EUR           | USD         | 12/1/2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>Voer de consolidatie voor Oktober 2015 uit
### <a name="balances-in-the-consolidation-company"></a>Saldi in het consolidatiebedrijf

| Grootboekrekening | Valuta | Bedrag | Berekening    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50%  |
| 130100         | EUR      | -250   | -500 USD × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Voer de valuta herwaardering voor de rekeningen van 1 oktober 2015, tot en met 30 november 2015
### <a name="balances-in-the-consolidation-company"></a>Saldi in het consolidatiebedrijf

| Grootboekrekening | Valuta | Bedrag  | Berekening                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333.33  | Oorspronkelijk bedrag van 500 × 66,6667%  |
| 130100         | EUR      | -333.33 | Oorspronkelijk bedrag van -500 × 66,6667% |
| 801400         | EUR      | 83.33   | 333.33 – 250                       |
| 801600         | EUR      | -83.33  | -333.33 – (-250)                   |

U kunt extra transacties voor de aangiftevalutabedragen zien.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Voer de valuta herwaardering voor de rekeningen van 1 oktober 2015 tot en met 31 december 2015
### <a name="balances-in-the-consolidation-company"></a>Saldi in het consolidatiebedrijf

| Grootboekrekening | Valuta | Bedrag  | Berekening                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Oorspronkelijk bedrag van 500 × 1                           |
| 130100         | EUR      | -500,00 | Oorspronkelijk bedrag van -500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |





