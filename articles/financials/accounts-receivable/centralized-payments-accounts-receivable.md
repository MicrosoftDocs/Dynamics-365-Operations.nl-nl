---
title: Gecentraliseerde betalingen voor Klanten
description: "Organisaties met meerdere rechtspersonen kunnen betalingen maken en beheren door één rechtspersoon te gebruiken die alle betalingen verwerkt. Daarom hoeft een en dezelfde betaling niet te worden ingevoerd in meerdere rechtspersonen. Dit artikel bevat voorbeelden die laten zien hoe de boeking voor gecentraliseerde betalingen in diverse scenario's wordt verwerkt."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7208acc35e656d12b3c4f88a090f36ecfdd4fdfb
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="centralized-payments-for-accounts-receivable"></a>Gecentraliseerde betalingen voor Klanten

[!include[banner](../includes/banner.md)]


Organisaties met meerdere rechtspersonen kunnen betalingen maken en beheren door één rechtspersoon te gebruiken die alle betalingen verwerkt. Daarom hoeft een en dezelfde betaling niet te worden ingevoerd in meerdere rechtspersonen. Dit artikel bevat voorbeelden die laten zien hoe de boeking voor gecentraliseerde betalingen in diverse scenario's wordt verwerkt.

Organisaties met meerdere rechtspersonen kunnen betalingen maken en beheren door een rechtspersoon te gebruiken die alle betalingen verwerkt. Daarom hoeft een en dezelfde betaling niet te worden ingevoerd in meerdere rechtspersonen. Bovendien bespaart de organisatie tijd, doordat de processen voor betalingsvoorstellen, vereffening en het bewerken van openstaande en gesloten transacties voor gecentraliseerde betalingen worden gestroomlijnd. 

In een gecentraliseerde betalingsorganisatie zijn vele rechtspersonen voor verwerkingen, en iedere werkende rechtspersoon beheert zijn eigen informatie over te ontvangen facturen. Betalingen voor alle werkende rechtspersonen worden door één rechtspersoon ontvangen, die de rechtspersoon van de betaling wordt genoemd. Tijdens het vereffeningsproces worden de toepasselijke transacties voor betaling aan en betaling van gegenereerd. U kunt opgeven welke rechtspersoon binnen de organisatie de gerealiseerde winst- of verliestransacties ontvangt, en hoe contantkortingstransacties met betrekking tot een gecentraliseerde betaling worden verwerkt. 

In de volgende voorbeelden ziet u hoe boekingen in diverse scenario's worden verwerkt. Bij al deze voorbeelden is van het volgende uitgegaan:

-   De rechtspersonen zijn Fabrikam, Fabrikam East, en Fabrikam West. Betalingen van klanten worden ingevoerd in Fabrikam.
-   Het veld **Contantkorting boeken** op de pagina **Intercompany-boekhouding** pagina is ingesteld op **Rechtspersoon van de factuur**.
-   Het veld **Winst of verlies bij valutawissel boeken** op de pagina **Intercompany-boekhouding** pagina is ingesteld op **Rechtspersoon van de factuur**.
-   De klant Northwind Traders is ingesteld als klant in alle rechtspersonen. De klanten van de verschillende rechtspersonen worden geïdentificeerd als dezelfde klant, omdat ze dezelfde globaal adresboek-ID delen.

| Adresboek-id | Klantrekening | Naam              | Rechtspersoon  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam East |
| 4050            | 10000            | Northwind Traders | Fabrikam West |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Voorbeeld 1: klantbetaling van factuur vanuit een andere rechtspersoon
Fabrikam ontvangt een betaling van 600,00 EUR voor Fabrikam-klantrekening 4000, Northwind Traders. De betaling wordt vereffend met een openstaande factuur voor klantrekening 4000 in Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>De factuur wordt geboekt in Fabrikam East voor klant 4000

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Klanten (Fabrikam East) | 600,00       |               |
| Verkoop (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>De betaling wordt ontvangen en geboekt in Fabrikam voor klant 4000

| Rekening                        | Debetbedrag | Creditbedrag |
|--------------------------------|--------------|---------------|
| Contant geld (Fabrikam)                | 600,00       |               |
| Klanten (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>De Fabrikam-betaling wordt vereffend met de Fabrikam East-factuur

**Boeken naar Fabrikam**

| Rekening                         | Debetbedrag | Creditbedrag |
|---------------------------------|--------------|---------------|
| Klanten (Fabrikam)  | 600,00       |               |
| Te betalen aan Fabrikam East (Fabrikam) |              | 600,00        |

**Boeken naar Fabrikam East**

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Te ontvangen van Fabrikam (Fabrikam East)   | 600,00       |               |
| Klanten (Fabrikam East) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Voorbeeld 2: klantbetaling van factuur vanuit een andere rechtspersoon met contantkorting
Fabrikam ontvangt een betaling van 580,00 EUR voor Fabrikam-klant 4000, Northwind Traders. Fabrikam East heeft een openstaande factuur voor klant 4000. De factuur heeft een beschikbare contantkorting van 20,00. De betaling wordt vereffend met de openstaande Fabrikam East-facturen. De contantkorting wordt geboekt naar de te betalen rechtspersoon, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>De factuur wordt geboekt in Fabrikam East voor Fabrikam East-klant 4000

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Klanten (Fabrikam East) | 600,00       |               |
| Verkoop (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>De betaling wordt ontvangen en geboekt in Fabrikam voor Fabrikam-klant 4000

| Rekening                        | Debetbedrag | Creditbedrag |
|--------------------------------|--------------|---------------|
| Contant geld (Fabrikam)                | 600,00       |               |
| Klanten (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>De Fabrikam-betaling wordt vereffend met de Fabrikam East-factuur

**Boeken naar Fabrikam**

| Rekening                         | Debetbedrag | Creditbedrag |
|---------------------------------|--------------|---------------|
| Klanten (Fabrikam)  | 580,00       |               |
| Te betalen aan Fabrikam East (Fabrikam) |              | 580,00        |

**Boeken naar Fabrikam East**

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Te ontvangen van Fabrikam (Fabrikam East)   | 580,00       |               |
| Klanten (Fabrikam East) |              | 580,00        |
| Contantkorting (Fabrikam East)       | 20,00        |               |
| Klanten (Fabrikam East) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Voorbeeld 3: klantbetaling van factuur vanuit een andere rechtspersoon met gerealiseerde winst door wisselkoers
Fabrikam ontvangt een betaling van EUR 600,00 voor Fabrikam-klant 4000, Northwind Traders. De betaling wordt vereffend met een openstaande factuur voor klant 4000 in Fabrikam East. Tijdens het vereffenen wordt er een transactie winst bij valutawissel gegenereerd.

-   De wisselkoers van EUR naar USD bedroeg op de factuurdatum: 1,2062.
-   De wisselkoers van de euro naar USD was op de betalingsdatum: 1.2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>De factuur wordt geboekt in Fabrikam East voor Fabrikam East-klant 4000

| Rekening                             | Debetbedrag            | Creditbedrag           |
|-------------------------------------|-------------------------|-------------------------|
| Klanten (Fabrikam East) | 600,00 EUR / 723,72 USD |                         |
| Verkoop (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>De betaling wordt ontvangen en geboekt in Fabrikam voor Fabrikam-klant 4000

| Rekening                        | Debetbedrag            | Creditbedrag           |
|--------------------------------|-------------------------|-------------------------|
| Contant geld (Fabrikam)                | 600,00 EUR / 736,62 USD |                         |
| Klanten (Fabrikam) |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>De Fabrikam-betaling wordt vereffend met de Fabrikam East-factuur

**Boeken naar Fabrikam**

| Rekening                         | Debetbedrag            | Creditbedrag           |
|---------------------------------|-------------------------|-------------------------|
| Klanten (Fabrikam)  | 600,00 EUR / 736,62 USD |                         |
| Te betalen aan Fabrikam East (Fabrikam) |                         | 600,00 EUR / 736,62 USD |
| Te betalen aan Fabrikam East (Fabrikam) | 0,00 EUR / 12,90 USD    |                         |
| Gerealiseerde winst (Fabrikam)        |                         | 0,00 EUR / 12,90 USD    |

**Boeken naar Fabrikam East**

| Rekening                             | Debetbedrag            | Creditbedrag           |
|-------------------------------------|-------------------------|-------------------------|
| Te ontvangen van Fabrikam (Fabrikam East)   | 600,00 EUR / 736,62 USD |                         |
| Klanten (Fabrikam East) |                         | 600,00 EUR / 736,62 USD |
| Klanten (Fabrikam East) | 0,00 EUR / 12,90 USD    |                         |
| Te ontvangen van Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Voorbeeld 4: klantbetaling van factuur vanuit een andere rechtspersoon met contantkorting en gerealiseerde winst door wisselkoers
Fabrikam boekt een betaling voor Fabrikam-klant 4000, Northwind Traders, voor een openstaande factuur in Fabrikam East. Op de factuur is een contantkorting gegeven en er is een btw-transactie gegenereerd. De betaling wordt vereffend met de openstaande Fabrikam East-factuur. Tijdens het vereffenen wordt er een transactie winst bij valutawissel gegenereerd. De contantkorting wordt naar de te rechtspersoon van de factuur (Fabrikam East) geboekt en de winst bij valutawissel wordt naar de rechtspersoon van de betaling (Fabrikam) geboekt.

-   De wisselkoers van de euro naar USD was op de factuurdatum: 1.2062
-   De wisselkoers van de euro naar USD was op de betalingsdatum: 1.2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>De vrije-tekstfactuur wordt geboekt en er wordt een btw-transactie in Fabrikam East voor klant 4000 gegenereerd

| Rekening                             | Debetbedrag            | Creditbedrag           |
|-------------------------------------|-------------------------|-------------------------|
| Klanten (Fabrikam East) | 638,22 EUR / 769,82 USD |                         |
| Verkoop (Fabrikam East)               |                         | 600,00 EUR / 723.72 USD |
| Btw (Fabrikam East)           |                         | 38,22 EUR / 46,10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>De betaling wordt ontvangen en geboekt in Fabrikam voor klant 4000

| Rekening                        | Debetbedrag            | Creditbedrag           |
|--------------------------------|-------------------------|-------------------------|
| Contant geld (Fabrikam)                | 626,22 EUR / 768,81 USD |                         |
| Klanten (Fabrikam) |                         | 626,22 EUR / 768,81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>De Fabrikam-betaling wordt vereffend met de Fabrikam East-factuur

**Boeken naar Fabrikam**

| Rekening                         | Debetbedrag            | Creditbedrag           |
|---------------------------------|-------------------------|-------------------------|
| Klanten (Fabrikam)  | 626,22 EUR / 768,81 USD |                         |
| Te betalen aan Fabrikam East (Fabrikam) |                         | 626,22 EUR / 768,81 USD |
| Te betalen aan Fabrikam East (Fabrikam) | 0,00 EUR / 13,46 USD    |                         |
| Gerealiseerde winst (Fabrikam)        |                         | 0,00 EUR / 13,46 USD    |

**Boeken naar Fabrikam East**

| Rekening                             | Debetbedrag            | Creditbedrag           |
|-------------------------------------|-------------------------|-------------------------|
| Te ontvangen van Fabrikam (Fabrikam East)   | 626,22 EUR / 768,81 USD |                         |
| Klanten (Fabrikam East) |                         | 626,22 EUR / 768,81 USD |
| Klanten (Fabrikam East)  | 0,00 EUR / 13,46 USD    |                         |
| Te ontvangen van Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 13,46 USD    |
| Contantkorting (Fabrikam East)       | 12,00 EUR / 14,47 USD   |                         |
| Klanten (Fabrikam East) |                         | 12,00 EUR / 14,47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Voorbeeld 5: creditnota van klant met eerste betaling
Fabrikam ontvangt een betaling van 75,00 EUR van klant 4000, Northwind Traders. De betaling wordt vereffend met een openstaande factuur voor Fabrikam West-klant 10000 en een openstaande creditnota voor Fabrikam East-klant 4000. De betaling wordt als de primaire betaling op de pagina **Transacties vereffenen** geselecteerd.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>De factuur wordt geboekt naar Fabrikam West voor klant 10000

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Klanten (Fabrikam West) | 100,00       |               |
| Verkoop (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>De creditnota wordt geboekt naar Fabrikam East voor klant 4000

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Verkoopretouren (Fabrikam East)       | 25,00        |               |
| Klanten (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>De betaling wordt geboekt naar Fabrikam voor klant 4000

| Rekening                        | Debetbedrag | Creditbedrag |
|--------------------------------|--------------|---------------|
| Contant geld (Fabrikam)                | 75,00        |               |
| Klanten (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>De Fabrikam-betaling wordt vereffend met de Fabrikam West-factuur en de Fabrikam East-creditnota

**Boeken naar Fabrikam**

| Rekening                           | Debetbedrag | Creditbedrag |
|-----------------------------------|--------------|---------------|
| Te ontvangen van Fabrikam East (Fabrikam) | 25,00        |               |
| Klanten (Fabrikam)    |              | 25,00         |
| Klanten (Fabrikam)    | 100,00       |               |
| Te betalen aan Fabrikam West (Fabrikam)   |              | 100,00        |

**Boeken naar Fabrikam East**

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Klanten (Fabrikam East) | 25,00        |               |
| Te betalen aan Fabrikam East (Fabrikam)     |              | 25,00         |

**Boeken naar Fabrikam West**

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Te ontvangen van Fabrikam (Fabrikam West)   | 100,00       |               |
| Klanten (Fabrikam West) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Voorbeeld 6: creditnota van klant zonder eerste betaling
Fabrikam ontvangt een betaling van 75,00 EUR van klant 4000, Northwind Traders. De betaling wordt vereffend met een openstaande factuur voor Fabrikam West-klant 10000 en een openstaande creditnota voor Fabrikam East-klant 4000. De betaling wordt niet als de primaire betaling op de pagina **Transacties vereffenen** geselecteerd.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>De factuur wordt geboekt naar Fabrikam West voor klant 10000

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Klanten (Fabrikam West) | 100,00       |               |
| Verkoop (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>De creditnota wordt geboekt naar Fabrikam East voor klant 4000

| Rekening                             | Debetbedrag | Creditbedrag |
|-------------------------------------|--------------|---------------|
| Verkoopretouren (Fabrikam East)       | 25,00        |               |
| Klanten (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>De betaling wordt geboekt naar Fabrikam voor klant 4000

| Rekening                        | Debetbedrag | Creditbedrag |
|--------------------------------|--------------|---------------|
| Contant geld (Fabrikam)                | 75,00        |               |
| Klanten (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>De Fabrikam-betaling wordt vereffend met de Fabrikam West-factuur en de Fabrikam East-creditnota

**Boeken naar Fabrikam**

| Rekening                         | Debetbedrag | Creditbedrag |
|---------------------------------|--------------|---------------|
| Klanten (Fabrikam)  | 75,00        |               |
| Te betalen aan Fabrikam West (Fabrikam) |              | 75,00         |

**Boeken naar Fabrikam East**

| Rekening                              | Debetbedrag | Creditbedrag |
|--------------------------------------|--------------|---------------|
| Klanten (Fabrikam East)  | 25,00        |               |
| Te betalen aan Fabrikam West (Fabrikam East) |              | 25,00         |

**Boeken naar Fabrikam West**

| Rekening                                | Debetbedrag | Creditbedrag |
|----------------------------------------|--------------|---------------|
| Te ontvangen van Fabrikam (Fabrikam West)      | 75,00        |               |
| Klanten (Fabrikam West)    |              | 75,00         |
| Te ontvangen van Fabrikam East (Fabrikam West) | 25,00        |               |
| Crediteuren (Fabrikam West)    |              | 25,00         |






