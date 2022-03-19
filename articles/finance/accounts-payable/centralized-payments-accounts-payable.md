---
title: Gecentraliseerde betalingen voor leveranciers
description: Organisaties met meerdere rechtspersonen kunnen betalingen maken en beheren door één rechtspersoon te gebruiken die alle betalingen verwerkt. Daarom hoeven dezelfde betalingen niet in meerdere rechtspersonen worden ingevoerd. Dit onderwerp bevat voorbeelden die laten zien hoe de boeking voor gecentraliseerde betalingen in diverse scenario's wordt verwerkt.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df0d2178d1ebd3dcb154e2c4f7821a4007da55d4
ms.sourcegitcommit: 5033d42a2aac852916d726e40bd98a164d1a837d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/23/2022
ms.locfileid: "8331737"
---
# <a name="centralized-payments-for-accounts-payable"></a>Gecentraliseerde betalingen voor leveranciers

[!include [banner](../includes/banner.md)]

Organisaties met meerdere rechtspersonen kunnen betalingen maken en beheren door één rechtspersoon te gebruiken die alle betalingen verwerkt. Daarom hoeven dezelfde betalingen niet in meerdere rechtspersonen worden ingevoerd. Dit onderwerp bevat voorbeelden die laten zien hoe de boeking voor gecentraliseerde betalingen in diverse scenario's wordt verwerkt.

In een gecentraliseerde betalingsorganisatie zijn vele rechtspersonen voor verwerkingen, en iedere werkende rechtspersoon beheert zijn eigen leveranciersfacturen. Betalingen voor alle werkende rechtspersonen worden door één rechtspersoon gegenereerd, die de rechtspersoon van de betaling wordt genoemd. Tijdens het vereffeningsproces worden de toepasselijke transacties voor betaling aan en betaling van gegenereerd. U kunt opgeven welke rechtspersoon binnen de organisatie de gerealiseerde winst- of verliestransacties ontvangt, en hoe contantkortingstransacties met betrekking tot een betaling tussen meerdere bedrijven worden verwerkt. Op de journaalregel voor gecentraliseerde betaling moet **Rekeningtype** worden ingesteld op Leverancier. **Type tegenrekening** moet worden ingesteld op Bank of Grootboek. De bankrekening moet in het huidige bedrijf zijn. 

In de volgende voorbeelden ziet u hoe boekingen in diverse scenario's worden verwerkt. Bij al deze voorbeelden is van het volgende uitgegaan:

-   De rechtspersonen zijn Fabrikam, Fabrikam East, en Fabrikam West. De betalingen worden gemaakt van Fabrikam.
-   Het veld **Contantkorting boeken** op de pagina **Intercompany-boekhouding** pagina is ingesteld op **Rechtspersoon van de factuur**.
-   Het veld **Winst of verlies bij valutawissel boeken** op de pagina **Intercompany-boekhouding** pagina is ingesteld op **Rechtspersoon van de factuur**.
-   De leverancier Fourth Coffee is ingesteld als leverancier in elke rechtspersoon. De leveranciers van de verschillende rechtspersonen worden geïdentificeerd als dezelfde leverancier omdat ze dezelfde globaal adresboek-id delen.

| Map-ID | Leveranciersrekening | Naam          | Rechtspersoon  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam East |
| 1050         | 3004           | Fourth Coffee | Fabrikam West |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Voorbeeld 1: leveranciersbetaling van factuur vanuit een andere rechtspersoon
Fabrikam East heeft een openstaande factuur voor leverancierrekening 100, Fourth Coffee. Fabrikam voert een betaling in en boekt deze voor Fabrikam-leverancierrekening 3004, Fourth Coffee. De betaling wordt vereffend met de openstaande factuur.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Factuur wordt geboekt in Fabrikam East voor leverancier 100

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Onkosten (Fabrikam East)          | 600,00       |               |
| Leveranciers (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Betaling wordt gegenereerd en geboekt in Fabrikam voor leverancier 3004

| Rekening                     | Debetbedrag | Creditbedrag |
|-----------------------------|--------------|---------------|
| Leveranciers (Fabrikam) | 600,00       |               |
| Contant geld (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betaling wordt vereffend met Fabrikam East-factuur

**Fabrikam-boeking**

| Rekening                           | Debetbedrag | Creditbedrag |
|-----------------------------------|--------------|---------------|
| Te betalen door Fabrikam East (Fabrikam) | 600,00       |               |
| Leveranciers (Fabrikam)       |              | 600,00        |

**Fabrikam East-boeking**

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Leveranciers (Fabrikam East) | 600,00       |               |
| Te betalen aan Fabrikam East (Fabrikam)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Voorbeeld 2: leveranciersbetaling van factuur vanuit een andere rechtspersoon met contantkorting
Fabrikam East heeft een openstaande factuur voor leverancier 100, Fourth Coffee. De factuur heeft een beschikbare contantkorting van 20,00. Fabrikam voert een betaling van 580,00 in en boekt deze voor Fabrikam-leverancier 3004, Fourth Coffee. De betaling wordt vereffend met de openstaande Fabrikam East-facturen. De contantkorting wordt geboekt naar de te betalen rechtspersoon, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Factuur wordt geboekt in Fabrikam East voor Fabrikam East-leverancier 100

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Onkosten (Fabrikam East)          | 600,00       |               |
| Leveranciers (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Betaling wordt gegenereerd en geboekt in Fabrikam voor Fabrikam-leverancier 3004

| Rekening                     | Debetbedrag | Creditbedrag |
|-----------------------------|--------------|---------------|
| Leveranciers (Fabrikam) | 580,00       |               |
| Contant geld (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betaling wordt vereffend met Fabrikam East-factuur

**Fabrikam-boeking**

| Rekening                           | Debetbedrag | Creditbedrag |
|-----------------------------------|--------------|---------------|
| Te betalen door Fabrikam East (Fabrikam) | 580,00       |               |
| Leveranciers (Fabrikam)       |              | 580,00        |

**Fabrikam East-boeking**

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Leveranciers (Fabrikam East) | 580,00       |               |
| Te betalen aan Fabrikam (Fabrikam East)  |              | 580,00        |
| Leveranciers (Fabrikam East) | 20,00        |               |
| Contantkorting (Fabrikam East)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Voorbeeld 3: leverancierbetaling van factuur door een andere rechtspersoon met gerealiseerd wisselkoersverlies
Fabrikam East heeft een openstaande factuur voor leverancier 100, Fourth Coffee. Fabrikam voert een betaling in en boekt deze voor Fabrikam-leverancier 3004, Fourth Coffee. De betaling wordt vereffend met de openstaande Fabrikam East-factuur. Er wordt een valutawisselverliestransactie tijdens het vereffeningsproces gegenereerd.

-   De wisselkoers van de euro naar USD was op de factuurdatum: 1,2062
-   De wisselkoers van de euro naar USD was op de betalingsdatum: 1.2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Factuur wordt geboekt in Fabrikam East voor Fabrikam East-leverancier 100

| Rekening                          | Debetbedrag            | Creditbedrag           |
|----------------------------------|-------------------------|-------------------------|
| Onkosten (Fabrikam East)          | 600,00 EUR / 723,72 USD |                         |
| Leveranciers (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Betaling wordt gegenereerd en geboekt in Fabrikam voor Fabrikam-leverancier 3004

| Rekening                     | Debetbedrag            | Creditbedrag           |
|-----------------------------|-------------------------|-------------------------|
| Leveranciers (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Contant geld (Fabrikam)             |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betaling wordt vereffend met Fabrikam East-factuur

**Fabrikam-boeking**

| Rekening                           | Debetbedrag            | Creditbedrag           |
|-----------------------------------|-------------------------|-------------------------|
| Te betalen door Fabrikam East (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Leveranciers (Fabrikam)       |                         | 600,00 EUR / 736,62 USD |
| Gerealiseerd verlies (Fabrikam)          | 0,00 EUR / 12,90 USD    |                         |
| Te betalen door Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East-boeking**

| Rekening                          | Debetbedrag            | Creditbedrag           |
|----------------------------------|-------------------------|-------------------------|
| Leveranciers (Fabrikam East) | 600,00 EUR / 736,62 USD |                         |
| Te betalen aan Fabrikam (Fabrikam East)  |                         | 600,00 EUR / 736,62 USD |
| Te betalen aan Fabrikam (Fabrikam East)  | 0,00 EUR / 12,90 USD    |                         |
| Leveranciers (Fabrikam East) |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Voorbeeld 4: leveranciersbetaling van factuur vanuit een andere rechtspersoon met contantkorting en gerealiseerd verlies door wisselkoers
Fabrikam East heeft een openstaande factuur voor leverancier 100, Fourth Coffee. Op de factuur is een contantkorting gegeven en er is een btw-transactie gegenereerd. Fabrikam boekt een betaling voor Fabrikam-leverancier 3004, Fourth Coffee. De betaling wordt vereffend met de openstaande Fabrikam East-factuur. Er wordt een valutawisselverliestransactie tijdens het vereffeningsproces gegenereerd. De contantkorting wordt naar de te betalen rechtspersoon (Fabrikam East) geboekt en het verlies bij valutawissel wordt naar de te factureren rechtspersoon (Fabrikam) geboekt.

-   De wisselkoers van de euro naar USD was op de factuurdatum: 1.2062
-   De wisselkoers van de euro naar USD was op de betalingsdatum: 1.2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Factuur wordt geboekt en er wordt een belastingtransactie gegenereerd in Fabrikam East voor leverancier 100

| Rekening                          | Debetbedrag            | Creditbedrag           |
|----------------------------------|-------------------------|-------------------------|
| Onkosten (Fabrikam East)          | 564,07 EUR / 680,38 USD |                         |
| Btw (Fabrikam East)        | 35,93 EUR / 43,34 USD   |                         |
| Leveranciers (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Betaling wordt gegenereerd en geboekt in Fabrikam voor leverancier 3004

| Rekening                     | Debetbedrag            | Creditbedrag           |
|-----------------------------|-------------------------|-------------------------|
| Leveranciers (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Contant geld (Fabrikam East)        |                         | 588,72 EUR / 722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-betaling wordt vereffend met Fabrikam East-factuur

**Fabrikam-boeking**

| Rekening                           | Debetbedrag            | Creditbedrag           |
|-----------------------------------|-------------------------|-------------------------|
| Te betalen door Fabrikam East (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Leveranciers (Fabrikam)       |                         | 588,72 EUR / 722,77 USD |
| Gerealiseerd verlies (Fabrikam)          | 0,00 EUR / 12,66 USD    |                         |
| Te betalen door Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,66 USD    |

**Fabrikam East-boeking**

| Rekening                          | Debetbedrag            | Creditbedrag           |
|----------------------------------|-------------------------|-------------------------|
| Leveranciers (Fabrikam East) | 588,72 EUR / 722,77 USD |                         |
| Te betalen aan Fabrikam (Fabrikam East)  |                         | 588,72 EUR / 722,77 USD |
| Te betalen aan Fabrikam (Fabrikam East)   | 0,00 EUR / 12,66 USD    |                         |
| Leveranciers (Fabrikam East) |                         | 0,00 EUR / 12,66 USD    |
| Leveranciers (Fabrikam East) | 11,28 EUR / 13,61 USD   |                         |
| Contantkorting (Fabrikam East)    |                         | 11,28 EUR / 13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Voorbeeld 5: creditnota van leverancier met primaire betaling
Fabrikam genereert een betaling van 75,00 voor leverancier 3004, Fourth Coffee. De betaling wordt vereffend met een openstaande factuur voor Fabrikam West-leverancier 3004 en een openstaande creditnota voor Fabrikam East-leverancier 100. De betaling wordt als de primaire betaling op de pagina **Transacties vereffenen** geselecteerd.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Factuur wordt geboekt naar Fabrikam West voor leverancier 3004

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Onkosten (Fabrikam West)          | 100,00       |               |
| Leveranciers (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Creditnota wordt geboekt naar Fabrikam East voor leverancier 100

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Leveranciers (Fabrikam East) | 25,00        |               |
| Inkoopretouren (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Betaling wordt geboekt naar Fabrikam voor leverancier 3004

| Rekening                     | Debetbedrag | Creditbedrag |
|-----------------------------|--------------|---------------|
| Leveranciers (Fabrikam) | 75,00        |               |
| Contant geld (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betaling wordt vereffend met Fabrikam West-factuur en Fabrikam East-creditnota

**Fabrikam-boeking**

| Rekening                           | Debetbedrag | Creditbedrag |
|-----------------------------------|--------------|---------------|
| Leveranciers (Fabrikam)       | 25,00        |               |
| Te betalen aan Fabrikam East (Fabrikam)   |              | 25,00         |
| Te betalen door Fabrikam West (Fabrikam) | 100,00       |               |
| Leveranciers (Fabrikam)       |              | 100,00        |

**Fabrikam East-boeking**

| Rekening                           | Debetbedrag | Creditbedrag |
|-----------------------------------|--------------|---------------|
| Te betalen door Fabrikam (Fabrikam East) | 25,00        |               |
| Leveranciers (Fabrikam East)  |              | 25,00         |

**Fabrikam West-boeking**

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Leveranciers (Fabrikam West) | 100,00       |               |
| Te betalen aan Fabrikam (Fabrikam West)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Voorbeeld 6: creditnota van leverancier zonder primaire betaling
Fabrikam genereert een betaling van 75,00 voor leverancier 3004, Fourth Coffee. De betaling wordt vereffend met een openstaande factuur voor Fabrikam West-leverancier 3004 en een openstaande creditnota voor Fabrikam East-leverancier 100. De betaling wordt niet als de primaire betaling op de pagina **Transacties vereffenen** geselecteerd.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Factuur wordt geboekt naar Fabrikam West voor leverancier 3004

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Onkosten (Fabrikam West)          | 100,00       |               |
| Leveranciers (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Creditnota wordt geboekt naar Fabrikam East voor leverancier 100

| Rekening                          | Debetbedrag | Creditbedrag |
|----------------------------------|--------------|---------------|
| Leveranciers (Fabrikam East) | 25,00        |               |
| Inkoopretouren (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Betaling wordt geboekt naar Fabrikam voor leverancier 3004

| Rekening                     | Debetbedrag | Creditbedrag |
|-----------------------------|--------------|---------------|
| Leveranciers (Fabrikam) | 75,00        |               |
| Contant geld (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-betaling wordt vereffend met Fabrikam West-factuur en Fabrikam East-creditnota

**Fabrikam-boeking**

| Rekening                           | Debetbedrag | Creditbedrag |
|-----------------------------------|--------------|---------------|
| Te betalen door Fabrikam West (Fabrikam) | 75,00        |               |
| Leveranciers (Fabrikam)       |              | 75,00         |

**Fabrikam East-boeking**

| Rekening                                | Debetbedrag | Creditbedrag |
|----------------------------------------|--------------|---------------|
| Te betalen door Fabrikam West (Fabrikam East) | 25,00        |               |
| Leveranciers (Fabrikam East)       |              | 25,00         |

**Fabrikam West-boeking**

| Rekening                              | Debetbedrag | Creditbedrag |
|--------------------------------------|--------------|---------------|
| Leveranciers (Fabrikam West)     | 75,00        |               |
| Te betalen aan Fabrikam (Fabrikam West)      |              | 75,00         |
| Leveranciers (Fabrikam West)     | 25,00        |               |
| Te betalen aan Fabrikam East (Fabrikam West) |              | 25,00         |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
