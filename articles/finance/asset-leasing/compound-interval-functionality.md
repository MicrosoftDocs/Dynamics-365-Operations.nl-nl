---
title: Functionaliteit voor samenstellingsintervallen
description: Dit onderwerp bevat informatie waarmee u kunt kiezen uit maandelijkse, driemaandelijkse, halfjaarlijkse en jaarlijkse samenstellingsintervallen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d0f01748d370dfa5351ceb007a630564ca5d3a76c142830f32ce11951db9088
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716688"
---
# <a name="compounding-interval-functionality"></a>Functionaliteit voor samenstellingsintervallen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dit onderwerp bevat informatie waarmee u kunt kiezen uit maandelijkse, driemaandelijkse, halfjaarlijkse en jaarlijkse samenstellingsintervallen. De functionaliteit voor samenstellingsintervallen wordt gebruikt om het aantal samenstellingensperioden per jaar in het betalingsschema van een lease te bepalen. Elk van de vier voorbeelden in dit onderwerp laat zien hoe een betalingsschema van een lease wordt weergegeven voor een ander interval.

U kunt geen samenstellingsinterval selecteren dat minder frequent is dan de betalingsfrequentie van de lease. Een driemaandelijks samenstellingsinterval kan bijvoorbeeld niet worden gebruikt met een maandelijkse betalingsfrequentie en een jaarlijks samenstellingsinterval kan niet worden gebruikt met een halfjaarlijkse betalingsfrequentie. Als u een samenstellingsinterval probeert te selecteren dat minder frequent is dan de betalingsfrequentie van de lease, verschijnt een foutmelding.

> [!NOTE]
> In alle vier voorbeelden in dit onderwerp komt het samenstellingsinterval overeen met de betalingsfrequentie.

## <a name="examples"></a>Voorbeelden

### <a name="setup-for-all-four-leases"></a>Instellingen voor alle vier leases

In de volgende tabellen ziet u de waarden die zijn ingesteld op de tabbladen **Algemeen** en **Betalingsschemaregels** voor de vier leases die in de voorbeelden worden gebruikt.

**Tabblad Algemeen**

| Veld                      | Waarde                        |
|----------------------------|------------------------------|
| Verhoogd leningtarief | **5%**                       |
| Type annuïteit               | **Normale annuïteit**         |
| Samenstellingsinterval       | Zie de afzonderlijke voorbeelden. |
| Betalingsfrequentie          | **Maandelijks**                  |
| Begindatum          | **1-1-2020**                 |

**Tabblad Regels van betalingsschema**

| Veld             | Waarde                        |
|-------------------|------------------------------|
| Begindatum        | **1-1-2020**                 |
| Perioden           | **120**                      |
| Periode-interval   | **Maanden**                   |
| Einddatum          | **12-31-2029**               |
| Betalingsfrequentie | Zie de afzonderlijke voorbeelden. |
| Betalingsbedrag    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Lease 1: maandelijks samenstellingsinterval en maandelijkse betalingsfrequentie

In de volgende tabel worden de eerste twaalf maanden van het betalingsschema weergegeven. Let op de volgende details:

- De waarde in de kolom Periode wordt elke maand met 1 verhoogd, omdat elke maand een nieuw samenstellingsinterval is.
- In de formule in de kolom Huidige waarde wordt het tarief gedeeld door 12, omdat er 12 samenstellingsperioden per jaar zijn. De exponent (dus het superscript cijfer) is gelijk aan de waarde in de kolom Periode.

| Periode | Maand | Datum       | Betalingsbedrag | Huidige waarde                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31-1-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>1</sup> = 49.792,53  |
| 2      | 2     | 29-2-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>2</sup> = 49.585,92  |
| 3      | 3     | 31-3-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>3</sup> = 49.380,17  |
| 4      | 4     | 30-4-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>4</sup> = 49.175,28  |
| 5      | 5     | 31-5-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>5</sup> = 48.971,23  |
| 6      | 6     | 30-6-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>6</sup> = 48.768,03  |
| 7      | 7     | 31-7-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>7</sup> = 48.565,67  |
| 8      | 8     | 31-8-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>8</sup> = 48.364,15  |
| 9      | 9     | 30-9-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>9</sup> = 48.163,47  |
| 10     | 10    | 31-10-2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>10</sup> = 47.963,62 |
| 11     | 11    | 30-11-2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>11</sup> = 47.764,61 |
| 12     | 12    | 31-12-2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>12</sup> = 47.566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Lease 2: samenstellingsinterval per kwartaal en betalingsfrequentie per kwartaal

In de volgende tabel worden de eerste twaalf maanden van het betalingsschema weergegeven. Let op de volgende details:

- De waarde in de kolom Periode wordt om de drie maanden (elk kwartaal) met 1 verhoogd, omdat elk kwartaal een nieuw samenstellingsinterval is.
- In de formule in de kolom Huidige waarde wordt het tarief gedeeld door 4, omdat er 4 samenstellingsperioden per jaar zijn. De exponent is gelijk aan de waarde in de kolom Periode.

| Periode | Maand | Datum       | Betalingsbedrag | Huidige waarde                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31-1-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29-2-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31-3-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 49.382,72 |
| 2      | 4     | 30-4-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31-5-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30-6-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 48.773,05 |
| 3      | 7     | 31-7-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31-8-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30-9-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 48.170,92 |
| 4      | 10    | 31-10-2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 30-11-2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 31-12-2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 47.576,21 |

> [!NOTE]
> Als het type annuïteit is gewijzigd in **Te betalen annuïteit**, wordt de betaling aan het begin van het kwartaal uitgevoerd in plaats van aan het einde van het kwartaal.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Lease 3: samenstellingsinterval per half jaar en betalingsfrequentie per half jaar

In de volgende tabel worden de eerste twaalf maanden van het betalingsschema weergegeven. Let op de volgende details:

- De waarde in de kolom Periode wordt om de zes maanden (per half jaar) met 1 verhoogd, omdat elk half jaar een nieuw samenstellingsinterval is.
- In de formule in de kolom Huidige waarde wordt het tarief gedeeld door 2, omdat er twee samenstellingsperioden per jaar zijn. De exponent is gelijk aan de waarde in de kolom Periode.

| Periode | Maand | Datum       | Betalingsbedrag | Huidige waarde                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31-1-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29-2-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31-3-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30-4-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31-5-2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30-6-2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 48.780,49 |
| 2      | 7     | 31-7-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31-8-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30-9-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 31-10-2020 | 0,00           | 0.00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 30-11-2020 | 0,00           | 0.00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 31-12-2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 47.590,72 |

> [!NOTE]
> Als het type annuïteit is gewijzigd in **Te betalen annuïteit**, vindt de betaling plaats in januari en juli in plaats van juni en december.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Lease 4: samenstellingsinterval per jaar en betalingsfrequentie per jaar

In de volgende tabel worden de eerste twaalf maanden van het betalingsschema weergegeven. Let op de volgende details:

- De waarde in de kolom Periode wordt om de 12 maanden (per jaar) met 1 verhoogd, omdat elk jaar een nieuw samenstellingsinterval is.
- In de formule in de kolom Huidige waarde wordt het tarief gedeeld door 1, omdat er één samenstellingsperiode per jaar is. De exponent is gelijk aan de waarde in de kolom Periode.

| Periode | Maand | Datum       | Betalingsbedrag | Huidige waarde                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31-1-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29-2-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31-3-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30-4-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31-5-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30-6-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31-7-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31-8-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30-9-2020  | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 31-10-2020 | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 30-11-2020 | 0,00           | 0.00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 31-12-2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 47.619,05 |

> [!NOTE]
> Als het type annuïteit is gewijzigd in **Te betalen annuïteit**, vindt de betaling plaats in januari in plaats van in december.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
