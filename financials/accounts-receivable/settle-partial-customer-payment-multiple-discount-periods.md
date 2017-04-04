---
title: Een gedeeltelijke klantenbetaling met meerdere kortingsperioden vereffenen
description: In dit artikel wordt getoond hoe gedeeltelijke klantbetalingen worden vereffend wanneer er meerdere kortingsperioden zijn.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9da48c7861f48ec2a154ac12616149d1208346cf
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Een gedeeltelijke klantenbetaling met meerdere kortingsperioden vereffenen

In dit artikel wordt getoond hoe gedeeltelijke klantbetalingen worden vereffend wanneer er meerdere kortingsperioden zijn.

Fabrikam biedt klant 4031 twee contantkortingsperiodes. De klant ontvangt een korting van 2 procent als de factuur binnen vijf dagen wordt betaald en 1 procent contantkorting als de factuur binnen 14 dagen wordt betaald. Fabrikam biedt ook contantkortingen op gedeeltelijke betalingen. De parameters voor de vereffening bevinden zich op de **parameters van module klanten** pagina.

## <a name="invoice"></a>Factuur
Op 25 juni Arnie invoert en boekt een factuur voor 1.000,00 voor klant 4031. Wanneer hij de contantkortingen voor deze factuur bekijkt, ziet Arnie dat klant 4031 een korting van 20,00 ontvangt als de factuur is betaald met 30 juni. Als de factuur wordt betaald 9 juli, ontvangt de klant een korting van 10,00.

| Datum van contantkorting | Contantkortingsbedrag | Bedrag in transactievaluta |
|--------------------|----------------------|--------------------------------|
| 6/30/2015          | 20,00                | 980,00                         |
| 7/9/2015           | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1.000,00                       |

Arnie kan deze transactie bekijken op de pagina** Klanttransacties**.

| Boekstuk   | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Factuur          | 6/25/2015 | 10030   | 1.000,00                             |                                       | 1.000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Gedeeltelijke betaling vóór de datum van contantkorting
Op 28 juni voert Klant 4031 een gedeeltelijke betaling van 294,00 uit. Omdat 28 juni binnen de eerste periode van contantkorting ligt, neemt de klant een korting van 6,00. Op de pagina **Transacties vereffenen** is de waarde** Contantkortingsbedrag** 20,00 en de waarde **Contantkortingsbedrag dat moet worden toegepast** 6,00.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10030 | 4031    | 6/25/2015 | 25/7/2015 | 10030   | 1.000,00                       | USD      | 294,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven. Als u de waarde **Te vereffenen bedrag** niet wijzigt in **294,00**, zullen de waarden **Contantkortingsbedrag** die worden weergegeven verschillen. Wanneer de betaling wordt geboekt, wordt echter 6,00 als contantkorting toegepast, omdat de vereffening automatisch de waarde **Bedrag om te vereffenen** corrigeert voor u.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 6/30/2015 |
| Contantkortingsbedrag         | 20,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 6,00      |

Nadat Arnie de betaling boekt, is het factuursaldo 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Gedeeltelijke betaling vóór de tweede datum van contantkorting
Op 8 juli betaalt de klant de rest van het factuurbedrag. Er wordt een korting van 7,00 (1 procent) genomen omdat de betaling in de tweede periode van contantkorting werd uitgevoerd.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10030 | 4031    | 6/25/2015 | 25/7/2015 | 10030   | 700,00                               |                                       | USD      | 693,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 30,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 6,00      |
| Contantkortingsbedrag dat moet worden toegepast | 7,00      |

Het factuursaldo is nu 0,00. Arnie bekijkt de informatie op de pagina **Klanttransacties**.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Factuur          | 6/25/2015 | 10030   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Betaling         | 6/28/2015 |         |                                      | 294,00                                | 0,00    | USD      |
| DISC-10030 |  Contantkorting   | 6/28/2015 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Betaling         | 8-7-2015  |         |                                      | 693,00                                | 0,00    | USD      |
| DISC-1031  |  Contantkorting   | 8-7-2015  |         |                                      | 7,00                                  | 0,00    | USD      |




