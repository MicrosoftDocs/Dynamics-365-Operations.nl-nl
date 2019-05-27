---
title: Een gedeeltelijke leveranciersbetaling vereffenen vóór de kortingsdatum met een definitieve betaling na de kortingsdatum
description: Dit artikel begeleidt u door een scenario waarbij meerdere gedeeltelijke betalingen worden gedaan, waarvan enkele binnen de periode van de contantkorting en andere buiten deze periode.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b44d3d561b5d7fdccf34d2220d5ade0d3974ea8b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512263"
---
# <a name="settle-a-partial-vendor-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Een gedeeltelijke leveranciersbetaling vereffenen vóór de kortingsdatum met een definitieve betaling na de kortingsdatum

[!include [banner](../includes/banner.md)]

Dit artikel begeleidt u door een scenario waarbij meerdere gedeeltelijke betalingen worden gedaan, waarvan enkele binnen de periode van de contantkorting en andere buiten deze periode.

Fabrikam koopt goederen aan bij leverancier 3057. Fabrikam ontvangt een contantkorting van 1 procent als de factuur wordt betaald binnen 14 dagen. Facturen moeten worden betaald binnen 30 dagen. De leverancier laat Fabrikam ook contantkortingen nemen op gedeeltelijke betalingen. De vereffeningparameters bevinden zich op de pagina **Parameters van module Leveranciers**.

## <a name="invoice-on-june-25"></a>Factuur op 25 juni
Op 25 juni voert April een factuur in en boekt deze voor 1.000,00 voor leverancier 3057. April kan deze transactie op de pagina **Leverancierstransacties** weergeven.

| Boekstuk   | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo   | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Factuur-10020 | Factuur          | 6/25/2015 | 10020   |                                      | 1.000,00                              | -1.000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Gedeeltelijke betaling op 2 juli
Op 2 Juli wil April 300,00 van deze factuur vereffenen. De betaling komt in aanmerking voor een korting, omdat Fabrikam kortingen op gedeeltelijke betalingen neemt. April betaalt daarom 297,00 en neemt een korting van 3,00. Ze maakt een betalingsjournaal aan en voert een regel voor leverancier 3057 in. Ze opent vervolgens de pagina **Transacties vereffenen**, zodat ze de factuur kan markeren voor vereffening.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | Factuur-10020 | 3057    | 6/25/2015 | 25/7/2015 | 10020   | -1.000,00                      | USD      | -297,00          |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | -10,00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -3,00     |

Vervolgens boekt April de betaling. De factuur heeft nu een saldo van 700,00. April kan deze transactie op de pagina **Leverancierstransacties** weergeven.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10020  | Factuur          | 6/25/2015 | 10020   |                                      | 1.000,00                              | -700,00 | USD      |
| APP-10020  | Betaling          | 01-07-2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Contantkorting    | 01-07-2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Resterende betalingen op 15 juli, Contantkorting gebruiken = Normaal
April betaalt de rest van deze factuur op 15 juli, wat na de kortingsperiode valt. Op de pagina **Openstaande transacties vereffenen** verschijnt geen kortingsbedrag in het veld **Geraamde contantkorting** en de waarde in het veld **Contantkortingsbedrag** is **0,00**. Wanneer April de resterende 700,00 betaalt, wordt geen extra korting gepakt.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | Factuur-10020 | 3057    | 6/25/2015 | 25/7/2015 | 10020   | -700,00                        | USD      | -700,00          |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven. April ziet dat ze al een korting van 3,00 heeft genomen.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 0,00      |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | -3,00     |
| Contantkortingsbedrag dat moet worden toegepast | 0,00      |

Vervolgens boekt April de betaling. Wanneer ze de pagina **Leverancierstransacties** opent, ziet ze dat de factuur een saldo van 0,00 heeft. Zij ziet ook dat er twee betalingen zijn. Eén betaling is voor 297,00 en heeft 3,00 korting en de andere betaling is voor 700,00.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10020  | Factuur          | 6/25/2015 | 10020   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10020  | Betaling          | 01-07-2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Contantkorting    | 01-07-2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Betaling          | 7/15/2015 |         | 700,00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Resterende betalingen op 15 juli, Contantkorting gebruiken = Altijd
Als de leverancier April een korting geeft, hoewel zij na de kortingsdatum betaalt, kan zij de waarde in het veld **Contantkorting gebruiken** wijzigen in **Altijd**. De instelling **Contantkortingen berekenen voor gedeeltelijke betalingen** wordt overschreven en de korting wordt genomen. Het betalingsbedrag is 693,00 en de korting is de resterende 7,00.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Geselecteerd | Altijd            | Factuur-10020 | 3057    | 6/25/2015 | 25/7/2015 | 10020   | 700,00                               |                                       | USD      | -693,00          |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 7,00      |
| Contantkorting gebruiken            | Altijd    |
| Toegepaste contantkorting          | -3,00     |
| Contantkortingsbedrag dat moet worden toegepast | -7,00     |

Vervolgens boekt April de betaling. Wanneer ze de pagina **Leverancierstransacties** opent, ziet ze dat de factuur een saldo van 0,00 heeft. Zij ziet ook dat er twee betalingen zijn. Eén betaling is voor 297,00 en 3,00 korting en de andere betaling is voor 693,00 en 7,00 korting.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10020  | Factuur          | 6/25/2015 | 10020   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10020  | Betaling          | 01-07-2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Contantkorting    | 01-07-2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Betaling          | 7/15/2015 |         | 693,00                               |                                       | 0,00    | USD      |
| DISC-10021 | Contantkorting    | 7/15/2015 |         | 7,00                                 |                                       | 0,00    | USD      |





