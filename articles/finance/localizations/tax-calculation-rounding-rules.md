---
title: Afrondingsregels voor btw-berekening
description: Dit onderwerp biedt informatie over de afrondingsregels in de parameters voor de btw-berekening van de btw-berekeningsservice.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 38760879d84d8262cc1e8395c59bcbc0429bc753
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7347680"
---
# <a name="tax-calculation-rounding-rules"></a>Afrondingsregels voor btw-berekening

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over hoe de afrondingsregels in de parameters voor de btw-berekening van de btw-berekeningsservice functioneren.

> [!NOTE] 
> Wanneer de service voor het berekenen van de btw is ingeschakeld, zijn de afrondingsregels op de pagina's **Btw-code** en **Btw-groep** niet van kracht.

U kunt de configuratie van afrondingsregels voor de btw-berekeningsservice bekijken in het gedeelte **Regel voor btw-afronding** in het sneltabblad **Berekening** in het tabblad **Algemeen** van de pagina **Parameters voor btw-berekening** (**Btw** \> **Instellingen** \> **Btw-configuratie** \> **Parameters btw-configuratie**).

[![Configuratie van afrondingsregel op de pagina Parameters voor btw-berekening](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

De velden **Afrondingsprecisie** en **Afrondingsmethode** bepalen hoe berekende bedragen in de nettolading van de btw-berekeningsservice worden afgerond.

## <a name="rounding-precision"></a>Afrondingsprecisie

De velden voor **Afrondingsprecisie** ondersteunen een waarde met maximaal zes decimalen. Als u het veld **Afrondingsprecisie** bijvoorbeeld instelt op **0,000000**, worden berekende bedragen afgerond op zes decimalen en vervolgens naar Microsoft Dynamics 365 Finance verzonden. Als bijvoorbeeld de **normale** afrondingsmethode wordt gebruikt, wordt het bedrag **987,1234567** afgerond naar **987,123457**.

> [!NOTE]
> Finance rondt bedragen af conform de regels voor valuta-afronding. Daarom worden de btw-bedragen die in transacties worden weergegeven en vastgelegd, beïnvloed door de afrondingsregels voor de btw-berekening en door de afrondingsregels voor valuta.

## <a name="rounding-method"></a>Afrondingsmethode

De afrondingsmethode voor btw-berekening kan voor elke rechtspersoon worden geconfigureerd. In het veld **Afrondingsmethode** kunt u uit drie opties kiezen: **Normaal**, **Naar beneden** en **Naar boven** afronden.

### <a name="rounding-example"></a>Voorbeeld van afronding

De volgende tabel toont een voorbeeld dat laat zien hoe het bedrag **987,345** wordt afgerond voor verschillende combinaties van afrondingsprecisie en afrondingsmethoden.

<table>
<thead>
<tr>
<th rowspan="2">Afrondingsmethode</th>
<th colspan="8">Afrondingsprecisie</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10.00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Normaal</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Naar beneden afronden</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Naar boven afronden</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

De berekenings- en afrondingslogica van btw-bedragen kan volgens de belastingregels worden geconfigureerd.

## <a name="rounding-by"></a>Afronden op 

Selecteer in het veld **Afronden op** het afrondbeginsel dat op de belastingen van toepassing is. De volgende opties zijn beschikbaar:

- **Btw-codes**: afronding van het btw-bedrag binnen elke btw-code.
- **Combinaties van btw-codes**: afronding van het btw-bedrag binnen de btw-codecombinatie voor de regel.

## <a name="calculation-method"></a>Berekeningsmethode

Selecteer in het veld **Berekeningsmethode** of btw wordt berekend op facturen voor elke regel of voor alle regels. De volgende opties zijn beschikbaar:

- **Regel**: bereken het btw-bedrag regel voor regel. Het btw-bedrag op elke regel wordt niet beïnvloed door het btw-bedrag op andere regels.
- **Totaal**: het btw-bedrag op alle regels in één document berekenen.

### <a name="rounding-calculation-example"></a>Voorbeeld van afrondingsberekening

In dit voorbeeld ziet u de verschillende berekeningen die voor één factuur kunnen worden uitgevoerd, voor verschillende combinaties van de waarden **Afronding op** en **Berekeningsmethode**. Voor dit voorbeeld zijn de volgende instellingen gemaakt:

- De factuur bestaat uit vier regels.
- Er zijn twee btw-codes: **BTW1** (10 procent) en **BTW2** (10 procent).
- De afrondingsprecisie is ingesteld op **0,01**.
- De afrondingsmethode is ingesteld op **Naar boven** afronden.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Afronding op = Btw-codes en Berekeningsmethode = Regel

| Regelnummer | Nettobedrag per regel | Vastgestelde btw-codes | Btw-bedrag vóór afronding | Afgerond btw-bedrag |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | BTW1                 | 1.111                      | 1.12               |
| 2           | 22.22           | BTW1; BTW2           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33.33           | BTW1                 | 3.333                      | 3.34               |
| 4           | 44.44           | BTW1; BTW2           | 4,444; 4,444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Afronding op = Btw-codecombinaties en Berekeningsmethode = Regel

| Regelnummer | Nettobedrag per regel | Vastgestelde btw-codes | Btw-bedrag vóór afronding | Afgerond btw-bedrag |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | BTW1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | BTW1; BTW2           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33.33           | BTW1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | BTW1; BTW2           | 4,444; 4,444               | 4,45; 4,44         |

\* Regel 2 = Afronding\[22,22 × (10 procent + 10 procent)\] = 2,23 + 2,22

\*\* Regel 4 = Afronding\[44,44 × (10 procent + 10 procent)\] = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Afronding op = Btw-codes en Berekeningsmethode = Totaal

| Regelnummer | Nettobedrag per regel | Vastgestelde btw-codes | Btw-bedrag vóór afronding | Afgerond btw-bedrag |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | BTW1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | BTW1\*; BTW2\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33.33           | BTW1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | BTW1\*; BTW2\*\*     | 4,444; 4,444               | 4,44; 4,44         |

\* Btw1 (regel 1, regel 2, regel 3, regel 4) = Afronding\[(11,11 + 22,22 + 33,33 + 44,44) × 10 procent\] = 1,12 + 2,22 + 3,33 + 4,44

\*\* Btw2(Regel 2, Regel 4) = Afronding\[(22,22 + 44,44) × 10 procent\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Afronding op = Btw-codecombinaties en Berekeningsmethode = Totaal

| Regelnummer | Nettobedrag per regel | Vastgestelde btw-codes | Btw-bedrag vóór afronding | Afgerond btw-bedrag |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | BTW1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | BTW1; BTW2           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33.33           | BTW1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | BTW1; BTW2           | 4,444; 4,444               | 4,44; 4,45         |

\* Regel 1, Regel 3 = Afronding\[(11,11 + 33,33) × 10 procent\] = 1,12 + 3,33

\*\* Regel 2, regel 4 = Afronding\[(22,22 + 44,44) × (10 procent + 10 procent)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
