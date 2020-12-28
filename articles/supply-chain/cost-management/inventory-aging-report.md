---
title: Voorbeelden en logica voor naar ouderdom gerangschikt voorraadrapport
description: Dit onderwerp bevat enkele voorbeelden voor het interpreteren van de resultaten van een naar ouderdom gerangschikt voorraadrapport.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6e708e4dc818f20fc8d835053da75c2fe9c98f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425424"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Voorbeelden en logica voor naar ouderdom gerangschikt voorraadrapport

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat enkele voorbeelden voor het interpreteren van de resultaten van een **Naar ouderdom gerangschikt voorraadrapport**. Dit rapport categoriseert de voorhanden hoeveelheid en voorraadwaarden voor een geselecteerd artikel of een geselecteerde artikelgroep in verschillende periodebuckets. In dit onderwerp wordt ook de interne logica van het rapport weergegeven.

In de voorbeelden in dit onderwerp worden resultaten weergegeven in een standaard **naar ouderdom gerangschikt voorraadrapport**. In het algemeen is het echter raadzaam om de [opslagversie van het naar ouderdom gerangschikte voorraadrapport](inventory-aging-report-storage.md) te gebruiken, vooral wanneer u veel artikelen en magazijnen moet verwerken. Met Opslag naar ouderdom gerangschikt rapport wordt elk gegenereerd rapport opgeslagen, worden de resultaten weergegeven als een interactieve pagina en een grafiek, en kunt u elk opgeslagen rapport exporteren.

## <a name="sample-data-that-is-used-in-these-examples"></a>Voorbeeldgegevens die in deze voorbeelden worden gebruikt

De voorbeelden in dit onderwerp zijn gebaseerd op de voorbeeldgegevens voor voorraadtransacties die in deze sectie worden beschreven.

### <a name="storage-dimension-setup"></a>Instellingen opslagdimensiegroep

Het voorbeeldsysteem bevat de volgende instellingen voor opslagdimensies.

| Naam      | Actief | Fysieke voorraad | Financiële voorraad |
|-----------|--------|--------------------|---------------------|
| Locatie      | Ja    | Ja                | Ja                 |
| Magazijn | Ja    | Ja                | No                  |

### <a name="inventory-model"></a>Voorraadwaarderingsmodel

Voor het voorbeeldsysteem is het voorraadmodel voor de vrijgegeven producten *FIFO* en de instelling voor **Kostprijs** voor het voorraadmodel is *Fysieke waarde opnemen*.

### <a name="inventory-transactions"></a>Voorraadtransacties

Het voorbeeldsysteem bevat de volgende voorraadtransacties voor een vrijgegeven product met artikelnummer *1000*.

| Verwijzing      | Locatie | Magazijn | Ontvangst   | Uitgeven | Fysieke datum | Fin. datum | Hoeveelheid | Kosten | Fysieke kostprijs |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Inkooporder | 1    | 11        | Ingekocht |       | 15 maart      | 15 maart       | 10       | 1.000       | 1.000                |
| Inkooporder | 2    | 21        | Ingekocht |       | 15 maart      | 15 maart       | 10       | 2,000       | 2,000                |
| Inkooporder | 1    | 11        | Ontvangen  |       | 15 april      |                | 5        |             | 375                  |
| Transferorder | 1    | 11        |           | Verkocht  | mei 2         | mei 2          | -5       | -458,33     | -458,33              |
| Transferorder | 1    | 12        | Ingekocht |       | mei 2         | mei 2          | 5        | 458.33      | 458.33               |
| Verkooporder    | 1    | 12        |           | Verkocht  | mei 3         | mei 3          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Berekenen van hoeveelheden en bedragen in de periodebuckets

Met behulp van de voorbeeldgegevens die in de vorige secties worden beschreven, kunt u een **Naar ouderdom gerangschikt rapport** uitvoeren met de volgende instellingen:

- **Vanaf datum:** *9 mei 2020*
- **Locatie:** *Weergave*
- **Magazijn:** *Nee*
- **Artikelnummer:** *Totaal*
- **Ouderdomsperiode:** Stel dit veld in om maandelijkse buckets te genereren.

In dit geval is de inhoud van het gegenereerde rapport vergelijkbaar met het volgende voorbeeld.

<table>
<thead>
<tr>
    <th rowspan="2">artikelnummer</th>
    <th rowspan="2">Locatie</th>
    <th rowspan="2">Voorhanden hoeveelheid</th>
    <th rowspan="2">Waarde voorhanden voorraad</th>
    <th rowspan="2">Hoeveelheid voorraadwaarde</th>
    <th rowspan="2">Voorraadwaarde</th>
    <th rowspan="2">Gemiddelde eenheidskosten</th>
    <th colspan="2">8/5/2020 - 1/5/2020</th>
    <th colspan="2">30/4/2020 - 1/4/2020</th>
    <th colspan="2">31/3/2020 - 1/3/2020</th>
</tr>
<tr>
    <th>P1:Hoeveelheid</th>
    <th>P1:Bedrag</th>
    <th>P2:Hoeveelheid</th>
    <th>P2:Bedrag</th>
    <th>P3:Hoeveelheid</th>
    <th>P3:Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Totalen</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Let op de volgende details in dit voorbeeldrapport:

- De waarden van **Hoeveelheid voorraadwaarde**, **Voorraadwaarde** en **Gemiddelde eenheidskosten** die in het rapport worden weergegeven, zijn waarden voor de financiële voorraaddimensie (**site** in dit geval).

    Voor site 1 bevat het rapport bijvoorbeeld de volgende informatie:

    - De **Hoeveelheid voorraadwaarde** is *14* (= 10 + 5 – 5 + 5 – 1).
    - De **Voorraadwaarde** is *1.283,33* (= 1.000 + 375 – 458,33 + 458,33 – 91,67).
    - De **Gemiddelde eenheidskosten** is *91,67*.
    - De waarde voor **Voorhanden voorraad** en de waarde voor **Bedrag** in elke periodebucket worden berekend met behulp van **Gemiddelde eenheidskosten**.

- Het rapport bepaalt de voorhanden hoeveelheid voor elke periodebucket door de totale ontvangen voorraadhoeveelheid voor elke periodebucket samen te vatten. Vervolgens wordt het FIFO-principe (First In, First Out) toegepast om de totale uitgegeven hoeveelheid af te trekken, ongeacht het voorraadmodel dat de artikelen gebruiken.

Als u hetzelfde rapport opnieuw uitvoert, maar deze keer de velden **Site** en **Magazijn** instelt op *Weergeven*, ziet het nieuwe rapport eruit als in het volgende voorbeeld.

<table>
<thead>
<tr>
    <th rowspan="2">artikelnummer</th>
    <th rowspan="2">Locatie</th>
    <th rowspan="2">Magazijn</th>
    <th rowspan="2">Voorhanden hoeveelheid</th>
    <th rowspan="2">Waarde voorhanden voorraad</th>
    <th rowspan="2">Hoeveelheid voorraadwaarde</th>
    <th rowspan="2">Voorraadwaarde</th>
    <th rowspan="2">Gemiddelde eenheidskosten</th>
    <th colspan="2">8/5/2020 - 1/5/2020</th>
    <th colspan="2">30/4/2020 - 1/4/2020</th>
    <th colspan="2">31/3/2020 - 1/3/2020</th>
</tr>
<tr>
    <th>P1:Hoeveelheid</th>
    <th>P1:Bedrag</th>
    <th>P2:Hoeveelheid</th>
    <th>P2:Bedrag</th>
    <th>P3:Hoeveelheid</th>
    <th>P3:Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Totalen</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Deze keer wordt site 1 opgesplitst in twee rijen, één voor magazijn 11 en één voor magazijn 12. De waarden van **Hoeveelheid voorraadwaarde**, **Voorraadwaarde** en **Gemiddelde eenheidskosten** zijn echter hetzelfde, omdat **Magazijn** geen financiële voorraaddimensie is.

U ziet ook dat de hoeveelheidsdistributie van site 1 afwijkt. In het eerste rapport dat u hebt uitgevoerd, is de overdrachtsorder genegeerd die zich op dezelfde locatie heeft voorgedaan en wordt de hoeveelheid van de verkoopfactuur in mindering gebracht op de periodebucket **31/3/2020-1/3/2020** in site 1. In het nieuwe rapport trekt het systeem echter de hoeveelheid van de verkoopfactuur af van de periodebucket **8/5/2020-1/5/2020** in magazijn 12.

## <a name="effects-of-inventory-closing"></a>Effecten van voorraadafsluiting

Als u de voorraadafsluiting uitvoert voor mei en vervolgens het vorige rapport opnieuw uitvoert, maar het veld **Begindatum** instelt op *31 mei 2020* , zult u de volgende resultaten opmerken:

- De waarden voor **Voorraadwaarde** en **Gemiddelde eenheidskosten** worden bijgewerkt.
- De **Waarde voorhanden voorraad** en alle waarden voor **Bedrag** in elke periodebucket worden dienovereenkomstig bijgewerkt.

Het nieuwe rapport lijkt op het volgende voorbeeld.

<table>
<thead>
<tr>
    <th rowspan="2">artikelnummer</th>
    <th rowspan="2">Locatie</th>
    <th rowspan="2">Magazijn</th>
    <th rowspan="2">Voorhanden hoeveelheid</th>
    <th rowspan="2">Waarde voorhanden voorraad</th>
    <th rowspan="2">Hoeveelheid voorraadwaarde</th>
    <th rowspan="2">Voorraadwaarde</th>
    <th rowspan="2">Gemiddelde eenheidskosten</th>
    <th colspan="2">31/5/2020 - 1/5/2020</th>
    <th colspan="2">30/4/2020 - 1/4/2020</th>
    <th colspan="2">31/3/2020 - 1/3/2020</th>
</tr>
<tr>
    <th>P1:Hoeveelheid</th>
    <th>P1:Bedrag</th>
    <th>P2:Hoeveelheid</th>
    <th>P2:Bedrag</th>
    <th>P3:Hoeveelheid</th>
    <th>P3:Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0,00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Totalen</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>
