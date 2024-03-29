---
title: Een gedeeltelijke leveranciersbetaling met meerdere kortingsperioden vereffenen
description: Dit artikel begeleidt u door een scenario waarin meerdere gedeeltelijke betalingen worden gedaan aan een leverancier die meerdere contantkortingen aanbiedt.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da69d61c657ddc168a27a97fe16909d5f60eb4fd
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778032"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Een gedeeltelijke leveranciersbetaling met meerdere kortingsperioden vereffenen

[!include [banner](../includes/banner.md)]

Dit artikel begeleidt u door een scenario waarin meerdere gedeeltelijke betalingen worden gedaan aan een leverancier die meerdere contantkortingen aanbiedt. 

Leverancier 3054 biedt Fabrikam een contantkorting van 2 procent als een factuur binnen vijf dagen wordt betaald en een contantkorting van 1 procent als de factuur binnen 14 dagen wordt betaald.

## <a name="invoice"></a>Factuur
Op 28 juni maakt April een factuur voor 1.000,00 voor leverancier 3054. April kan deze transactie op de pagina **Leverancierstransacties** weergeven.

| Boekstuk   | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo   | Valuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Factuur-10060 | 6/28/2020 | 10060   |                                      | 1,000.00                              | -1.000,00 | USD      |

De volgende data en bedragen voor contantkorting zijn beschikbaar voor deze factuur.

| Datum van contantkorting | Contantkortingsbedrag | Bedrag in transactievaluta |
|--------------------|----------------------|--------------------------------|
| 7/3/2020           | 20.00                | 980.00                         |
| 7/12/2020          | 10.00                | 990.00                         |
| 7/25/2020          | 0,00                 | 1,000.00                       |

## <a name="payment-on-july-2"></a>Betaling op 2 juli
Op 2 juli wil April 300,00 voor deze factuur betalen. Zij maakt een eenmalige betaling door de pagina **Betalingsjournaal** in Leveranciers te gebruiken. Zij voegt een regel toe voor leverancier 3054 en voert een betalingsbedrag van **300,00** in. April opent vervolgens de pagina **Transacties vereffenen**, zodat zij de factuur kan markeren die zal worden vereffend. Zij werkt de waarde in het veld **Bedrag om te vereffenen** bij met **300,00** en ziet dat de waarde in het veld **Contantkortingsbedrag dat moet worden toegepast** veld is gewijzigd in **6,12**. Omdat deze betaling in de eerste kortingsperiode wordt gemaakt, wordt een korting van 2 procent genomen.

| Markeren | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normaal            | Factuur-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USD      | 300,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/02/2020 |
| Contantkortingsbedrag         | -20,00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -6,12     |

Omdat een contantkorting beschikbaar is, wil April het betalingsbedrag wijzigen zodat het totale vereffende bedrag 300,00 bedraagt voor de betaling en de contantkorting. Zij wijzigt de waarde in het veld **Bedrag om te vereffenen** in **294,00** en ziet dat de waarde in het veld **Contantkortingsbedrag dat moet worden toegepast** veld is gewijzigd in **6,00**.

| Markeren | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normaal            | Factuur-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USD      | 294,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/02/2020 |
| Contantkortingsbedrag         | -20,00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -6,00     |

April boekt de betaling. Op de pagina **Leverancierstransacties** kan zij de transacties bekijken. Ze ziet dat 300,00 is toegepast op de factuur. Dit bedrag is inclusief een korting van 6,00. Het resterende saldo is daarom 700,00.

| Boekstuk    | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | -700,00 | USD      |
| APP-10060  | 7/2/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2020  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Betaling op 8 juli
Op 8 juli voert April een aanvullende betaling voor de factuur uit. Om het bedrag in te voeren, opent zij de pagina **Transacties vereffenen** en klikt vervolgens op het tabblad **Contantkorting**. Ze ziet de datums en bedragen voor de twee contantkortingen die beschikbaar zijn. Omdat deze betaling in de tweede kortingsperiode wordt gemaakt, is een korting van 1 procent, of 5,00, beschikbaar. Dit bedrag wordt berekend als de helft van de korting van 1 procent op 1.000,00, oftewel de helft van 10,00.

| Datum van contantkorting | Contantkortingsbedrag | Bedrag in transactievaluta |
|--------------------|----------------------|--------------------------------|
| 7/3/2020           | 20.00                | 680,00                         |
| 7/12/2020          | 10.00                | 690,00                         |
| 7/25/2020          | 0,00                 | 700.00                         |

April besluit om 495,00 te betalen en de contantkorting van 5,00 toe te passen. Daardoor bedraagt het totale bedrag dat wordt vereffend 500,00.

| Markeren | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normaal            | Factuur-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USD      | 495,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/12/2020 |
| Contantkortingsbedrag         | -10.00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | -6,00     |
| Contantkortingsbedrag dat moet worden toegepast | -5,00     |

Op de pagina **Leveranciertransacties** ziet April dat het nieuwe saldo 200,00 bedraagt.

| Boekstuk    | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | -200,00 | USD      |
| APP-10060  | 7/2/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2020  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 7/12/2020 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 7/12/2020 |         | 5.00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Betaling op 20 juli
Op 20 juli voert April een laatste betaling van 200,00 uit. Er wordt geen korting toegepast omdat de betaling na beide kortingsperioden plaatsvindt. Het saldo van de factuur is 0,00.

| Boekstuk    | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | -200,00 | USD      |
| APP-10060  | 7/2/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2020  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 7/12/2020 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 7/12/2020 |         | 5.00                                 |                                       | 0,00    | USD      |
| APP-10062  | 7/20/2020 |         | 200.00                               |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
