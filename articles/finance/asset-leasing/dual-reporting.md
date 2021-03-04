---
title: Dubbele rapportage
description: In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442149"
---
# <a name="dual-reporting"></a>Dubbele rapportage

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt u begeleid door een voorbeeld dat u toont hoe u de vereisten kunt vervullen voor zowel International Financial Reporting Standard (IFRS)-rapportage als wettelijke rapportage in Activa leasen. Vertrouwdheid met boekingslagen in Microsoft Dynamics 365 Finance is vereist en maakt het voorbeeld gemakkelijker te begrijpen.

## <a name="example"></a>Voorbeeld

In het volgende voorbeeld wordt een lease verantwoord onder de Italiaanse wettelijke rapportering door middel van de cash-basis-methode en de IFRS-rapportagemethoden. Het bedrijf moet drie boeken maken om te verantwoorden voor zowel de Italiaanse wettelijke vereisten als de IFRS 16-vereisten. Eén boek is vereist voor IFRS 16, één boek is vereist voor wettelijke vereisten en één boek is vereist om de wettelijke boekingen automatisch terug te boeken. De boeken worden ingesteld, zoals in de volgende tabellen wordt weergegeven.

**IFRS 16-boek**

Het IFRS 16 boek is zo ingesteld dat het voldoet aan de IFRS 16-boekhoudnorm. Alle posten die in dit boek worden geboekt, worden naar een aangepaste laag geboekt.

| Naam                                    | Beschrijving    |
|-----------------------------------------|----------------|
| Boektype                               | IFRS 16        |
| Boekomschrijving                        | IFRS 16        |
| Boekingslaag                           | Aangepaste laag 1 |
| Leasetype                              | Finance        |
| Boekhoudraamwerk                    | IFRS 16        |
| Leasetermijn/economische levensduur instellen         | 0,00           |
| Huidige waarde/reële waarde van activum instellen | 0,00           |
| Drempel voor de korte termijn                    | 12             |
| Drempel voor geringe waarde                     | 5.000,00       |
| Betalen aan leverancier                           | No             |

**Wettelijk boek**

Het wettelijke boek is een cash-basis-boek waar het bedrijf de leasekosten zal verantwoorden als het bedrag aan geld dat maandelijks wordt betaald voor huur. Dit boek produceert geen RoU-activum of leaseverplichtingen.

| Naam                                    | Beschrijving |
|-----------------------------------------|-------------|
| Boektype                               | Wettelijk   |
| Boekomschrijving                        | Lokale GAAP  |
| Boekingslaag                           | Huidig     |
| Leasetype                              | Automatisch   |
| Boekhoudraamwerk                    | Contante basis  |
| Leasetermijn/economische levensduur instellen         | 0,00        |
| Huidige waarde/reële waarde van activum instellen | 0,00        |
| Drempel voor de korte termijn                    | 0           |
| Drempel voor geringe waarde                     | 0           |
| Betalen aan leverancier                           | No          |

**Wettelijk terugboekingsboek**

Het wettelijke terugboekingsboek wordt op dezelfde manier ingesteld als het wettelijke boek.

| Naam                                    | Beschrijving                    |
|-----------------------------------------|--------------------------------|
| Boektype                               | Wettelijk - terugboeking           |
| Boekomschrijving                        | Boek om wettelijk boek terug te boeken |
| Boekingslaag                           | Aangepaste laag 1                 |
| Leasetype                              | Automatisch                      |
| Boekhoudraamwerk                    | Contante basis                     |
| Leasetermijn/economische levensduur instellen         | 0,00                           |
| Huidige waarde/reële waarde van activum instellen | 0,00                           |
| Drempel voor de korte termijn                    | 0                              |
| Drempel voor geringe waarde                     | 0                              |
| Betalen aan leverancier                           | No                             |

Voor dit voorbeeld is er een lease gemaakt met de volgende instellingen op de tabbladen **Algemeen** en **Betalingsschemaregels**.

**Tabblad Algemeen**

| Veld                      | Waarde            |
|----------------------------|------------------|
| Verhoogd leningtarief | 5%               |
| Begindatum          | 1-1-2020         |
| Leasegroep                | Gebouwen        |
| Leverancier                     | 1001             |
| Reële waarde van het activum    | 245,000          |
| Economische levensduur activum          | 120              |
| Type annuïteit               | Normale annuïteit |
| Samenstellingsinterval       | Maandelijks          |

**Tabblad Regels van betalingsschema**

| Veld             | Waarde      |
|-------------------|------------|
| Begindatum        | 1-1-2020   |
| Periode-interval   | Maanden     |
| Perioden           | 24         |
| Einddatum          | 31-12-2020 |
| Betalingsfrequentie | Maandelijks    |
| Betalingsbedrag    | 1.000      |

Als u deze lease onder twee raamwerken wilt verantwoorden, gebruikt u een huidige boekingslaag en een aangepaste boekingslaag. In de volgende tabel ziet u een voorbeeld van elke journaalpost die voor elke rapportagestandaard de financiële waarde reëel moet representeren. Hierna wordt een gedetailleerde omschrijving gegeven van elke journaalpost voor de eerste maand van de lease.

<table>
<thead>
<tr>
<th rowspan='3'>Rekeningnummer</th>
<th rowspan='3'>Beschrijving</th>
<th colspan='3'>Wettelijk boek (huidige laag)</th>
<th rowspan='3'>Huidig laagtotaal</th>
<th>Terugboekingsboek (aangepaste laag)</th>
<th colspan='4'>IFRS 16-boek (aangepaste laag)</th>
<th rowspan='3'>Huidige laag + aangepaste laagtotaal</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Onkosten van lease</td>
<td>1.000,00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Bankkosten</td>
<td></td>
<td>3,00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>Btw-kosten</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Vereffeningsrekening</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Crediteuren</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>RoU-activum</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Financiële leaseverplichting</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>-22.794,00</td>
<td>1,000.00</td>
<td>-94,97</td>
<td></td>
<td>-21.888,87</td>
</tr>
<tr>
<td>8</td>
<td>Rente-uitgaven</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Contant</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Afschrijvingskosten</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Samengevoegde afschrijving</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Zoals in de bovenstaande tabel wordt aangegeven, moeten drie boeken worden gerapporteerd onder zowel wettelijke als IFRS-rapportage.

- In het wettelijke boek wordt de leasebetaling vastgelegd volgens de regels voor cash-basis-boekhouding onder de huidige laag.
- Het wettelijke terugboekingsboek keert de wettelijke journaalposten om.
- In het IFRS 16 boek worden de journaalposten gemaakt die zijn vereist volgens IFRS 16.

U moet een lease slechts één keer invoeren. Vervolgens kunt u de pagina **Boeken** openen om alle boeken te zien die aan de lease zijn gekoppeld.

> [!NOTE]
> Wanneer u de boeken maakt, moeten alle drie aan dezelfde leaserecord zijn gekoppeld.

De eerste journaalpost registreert de leasekosten uit hoofde van het wettelijke boek. U kunt de betalingen maken in een batch of door het betalingsschema te selecteren in het wettelijke boek.

Voor dit voorbeeld wordt de volgende journaalpost gemaakt voor het wettelijk boek van het betalingsschema.

### <a name="lease-payment--1312020--je-100"></a>Leasebetaling – 31-1-2020 – JE 100

| Rekeningtype | Rekeningnummer | Laag   | Rekeningbeschrijving | Debet    | Krediet   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 1              | Huidig | Onkosten van lease       | 1,000.00 |          |
| Ledger       | 4              | Huidig | Vereffeningsrekening    |          | 1,000.00 |

Een medewerker leveranciers gebruikt de standaard Dynamics 365-functionaliteit om een factuur te maken die moet worden betaald voor de lease buiten Activa leasen. In plaats van **Leasekosten** te selecteren als de debetrekening, selecteert de medewerker leveranciers een vereffeningsrekening om de volgende post te genereren.

### <a name="ap-process--1312020--je-110"></a>Leveranciersproces – 31-1-2020 – JE 110

| Rekeningtype | Rekeningnummer | Laag   | Rekeningbeschrijving | Debet    | Krediet   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 4              | Huidig | Vereffeningsrekening    | 1,000.00 |          |
| Ledger       | 2              | Huidig | Bankkosten            | 3.00     |          |
| Ledger       | 3              | Huidig | Btw-kosten         | 5.00     |          |
| Leverancier       | 5              | Huidig | Crediteuren    |          | 1,008.00 |

Wanneer het overzicht naar de leverancier wordt verzonden, volgt u het normale betalingsproces. Tijdens dit proces wordt de volgende journaalpost gegenereerd.

### <a name="cash-payment--1312020--je-120"></a>Contante betaling – 31-1-2020 – JE 120

| Rekeningtype | Rekeningnummer | Laag   | Rekeningbeschrijving | Debet    | Krediet   |
|--------------|----------------|---------|---------------------|----------|----------|
| Leverancier       | 5              | Huidig | Leveranciers    | 1,008.00 |          |
| Bank         | 9              | Huidig | Contant                |          | 1,008.00 |

U hebt op dit punt volledig verantwoord voor deze lease onder wettelijke rapportagevereisten en kunt een proefbalans genereren met behulp van de huidige laag. Het systeem geeft een proefbalans weer met de volgende cijfers.

<table>
<thead>
<tr>
<th rowspan='3'>Rekeningnummer</th>
<th rowspan='3'>Beschrijving</th>
<th colspan='3'>Wettelijk boek (huidige laag)</th>
<th rowspan='3'>Huidig laagtotaal</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Onkosten van lease</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Bankkosten</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>Btw-kosten</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Vereffeningsrekening</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Crediteuren</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>RoU-activum</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Financiële leaseverplichting</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Rente-uitgaven</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Contant</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Afschrijvingskosten</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Samengevoegde afschrijving</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Als u de IFRS 16 cijfers wilt gebruiken om dezelfde proefbalans uit te voeren, moeten de wettelijke boekhoudingsjournaalposten worden teruggeboekt en moeten de IFRS 16-journaalposten worden geboekt. Voor het omkeren van de wettelijke journaalposten bevat dit voorbeeld een wettelijk terugboekingsboek met dezelfde instellingen als het wettelijke boek, maar een tegengesteld boekingsprofiel. Het wettelijke boek heeft bijvoorbeeld een leasekostenrekening *gedebiteerd*, maar het terugboekingsboek *crediteert* deze rekening. Deze relaties worden eenvoudig gedefinieerd in de boekingsrekeningen Activa leasen op de pagina **Parameters voor activa leasing** (**Activa leasen \> Instellen \> Parameters voor activa leasing**).

Wanneer hetzelfde proces dat is gebruikt voor het wettelijke boek, wordt gebruikt voor het terugboekingsboek, wordt de volgende journaalpost geproduceerd. Het verschil is dat het terugboekingsboek de stornoposten uit het wettelijke boek boekt. De stornoposten worden ook in de aangepaste laag aangebracht. Wanneer een proefbalans wordt uitgevoerd op de huidige laag, worden de stornojournaalposten niet opgenomen.

### <a name="lease-payment--1312020--je-130"></a>Leasebetaling – 31-1-2020 – JE 130

| Rekeningtype | Rekeningnummer | Laag  | Rekeningbeschrijving | Debet    | Krediet   |
|--------------|----------------|--------|---------------------|----------|----------|
| Ledger       | 4              | Aangepast | Vereffeningsrekening    | 1,000.00 |          |
| Ledger       | 1              | Aangepast | Onkosten van lease       |          | 1,000.00 |

Nu u de wettelijk journaalposten hebt verwijderd, worden alle journaalposten geboekt die IFRS 16 vereist in het IFRS 16 boek. Deze posten omvatten de eerste toerekening van het RoU activum en de verplichting, en de record van rente en afschrijving.

### <a name="initial-recognition--112020--je-140"></a>Initiële toerekening - 1-1-2020 - JE 140

| Rekeningtype | Rekeningnummer | Laag  | Rekeningbeschrijving      | Debet     | Krediet    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Ledger       | 6              | Aangepast | RoU-activum                | 22,793.90 |           |
| Ledger       | 7              | Aangepast | Financiële leaseverplichting |           | 22,793.90 |

De leasebetaling wordt geboekt zoals de andere leasebetalingen. De reden voor het gebruik van de vereffeningsrekening is ervoor te zorgen dat contant geld slechts één keer wordt gecrediteerd.

### <a name="lease-payment--1312020--je-150"></a>Leasebetaling – 31-1-2020 – JE 150

| Rekeningtype | Rekeningnummer | Laag  | Rekeningbeschrijving      | Debet    | Krediet   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Ledger       | 7              | Aangepast | Financiële leaseverplichting | 1,000.00 |          |
| Ledger       | 4              | Aangepast | Vereffeningsrekening         |          | 1,000.00 |

De journaalpost voor rentelasten wordt gegenereerd op basis van het afschrijvingsschema voor verplichtingen.

### <a name="interest-expense--1312020--je-160"></a>Rente-uitgaven - 31-1-2020 - JE 160

| Rekeningtype | Rekeningnummer | Laag  | Rekeningbeschrijving      | Debet | Krediet |
|--------------|----------------|--------|--------------------------|-------|--------|
| Ledger       | 8              | Aangepast | Rente-uitgaven         | 94.97 |        |
| Ledger       | 7              | Aangepast | Financiële leaseverplichting |       | 94.97  |

De journaalpost voor afschrijvingskosten wordt gegenereerd op basis van het schema activumafschrijvingen.

### <a name="depreciation-expense--1312020--je-170"></a>Afschrijvingskosten - 31-1-2020 - JE 170

| Rekeningtype | Rekeningnummer | Laag  | Rekeningbeschrijving      | Debet  | Krediet |
|--------------|----------------|--------|--------------------------|--------|--------|
| Ledger       | 10             | Aangepast | Afschrijvingskosten     | 949.75 |        |
| Ledger       | 11             | Aangepast | Samengevoegde afschrijving |        | 949.75 |

Nadat al deze journaalposten zijn gemaakt en geboekt, ziet u de volgende waarden voor "aangepaste laag 1". De laatste kolom bevat de bankkosten, de kosten voor de toegevoegde waarde (btw) en de reductie van contant geld uit de vorige laag, maar bevat niet de journaalposten voor wettelijke rapportage. Daarom bereikt u echte mogelijkheden voor dubbele rapportage. Op dit punt hoeft het bedrijf alleen zijn proefbalans uit te voeren en de huidige laag en de aangepaste laag combineren om een IFRS-proefbalans te maken.

| Rekeningnummer | Beschrijving              | Wettelijk boek\-Huidige laag\-JE\-100\-Dr \(Cr\) | Wettelijk boek\-Huidige laag\-JE\-110\-Dr \(Cr\) | Wettelijk boek\-Huidige laag\-JE\-120\-Dr \(Cr\) | Huidige laag \- Totalen | - | Terugboekingsboek\-Aangepaste laag\-JE\-130\-Dr \(Cr\) | IFRS 16-boek\-Aangepaste laag\-JE\-140\-Dr \(Cr\) | IFRS 16-boek\-Aangepaste laag\-JE\-150\-Dr \(Cr\) | IFRS 16-boek\-Aangepaste laag\-JE\-160\-Dr \(Cr\) | IFRS 16-boek\-Aangepaste laag\-JE\-170\-Dr \(Cr\) | Aangepaste laag \+ Huidige laag \- Totalen |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Onkosten van lease            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1.000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Bankkosten                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | Btw-kosten              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Vereffeningsrekening         | \-1.000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1.000                                           |                                                | \-1.000                                        |                                                |                                                | 0\.00                                   |
| 5          | Crediteuren         |                                                   | \-1.008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | RoU-activum                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Financiële leaseverplichting |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22.794                                       | 1.000                                          | \-94\.97                                       |                                                | \-21.888\.87                            |
| 8          | Rente-uitgaven         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Contant                     |                                                   |                                                   | \-1.008\.00                                       | \-1.008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1.008\.00                             |
| 10         | Afschrijvingskosten     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Samengevoegde afschrijving |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]