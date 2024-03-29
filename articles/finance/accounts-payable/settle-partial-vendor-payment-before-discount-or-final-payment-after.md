---
title: Gedeeltelijke betaling uitvoeren vóór de kortingsdatum en definitieve betaling na de kortingsdatum
description: Dit artikel begeleidt u door een scenario waarbij meerdere gedeeltelijke betalingen worden gedaan, waarvan enkele binnen de periode van de contantkorting en andere buiten deze periode.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 828c82d88bef1d942af1219505af591d27043fa5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780479"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Gedeeltelijke betaling uitvoeren vóór de kortingsdatum en definitieve betaling na de kortingsdatum

[!include [banner](../includes/banner.md)]

Dit artikel begeleidt u door een scenario waarbij meerdere gedeeltelijke betalingen worden gedaan, waarvan enkele binnen de periode van de contantkorting en andere buiten deze periode.

Fabrikam koopt goederen aan bij leverancier 3057. Fabrikam ontvangt een contantkorting van 1 procent als de factuur wordt betaald binnen 14 dagen. Facturen moeten worden betaald binnen 30 dagen. De leverancier laat Fabrikam ook contantkortingen nemen op gedeeltelijke betalingen. De vereffeningparameters bevinden zich op de pagina **Parameters van module Leveranciers**.

## <a name="invoice-on-june-25"></a>Factuur op 25 juni
Op 25 juni voert April een factuur in en boekt deze voor 1.000,00 voor leverancier 3057. April kan deze transactie op de pagina **Leverancierstransacties** weergeven.

| Boekstuk   | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo   | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Factuur-10020 | Factuur          | 6/25/2020 | 10020   |                                      | 1,000.00                              | -1.000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Gedeeltelijke betaling op 2 juli
Op 2 Juli wil April 300,00 van deze factuur vereffenen. De betaling komt in aanmerking voor een korting, omdat Fabrikam kortingen op gedeeltelijke betalingen neemt. April betaalt daarom 297,00 en neemt een korting van 3,00. Ze maakt een betalingsjournaal aan en voert een regel voor leverancier 3057 in. Ze opent vervolgens de pagina **Transacties vereffenen**, zodat ze de factuur kan markeren voor vereffening.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | Factuur-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | -1.000,00                      | USD      | -297,00          |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/09/2020 |
| Contantkortingsbedrag         | -10.00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -3,00     |

Vervolgens boekt April de betaling. De factuur heeft nu een saldo van 700,00. April kan deze transactie op de pagina **Leverancierstransacties** weergeven.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10020  | Factuur          | 6/25/2020 | 10020   |                                      | 1,000.00                              | -700,00 | USD      |
| APP-10020  | Betaling          | 1-7-2020  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Contantkorting    | 1-7-2020  |         | 3.00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Resterende betalingen op 15 juli, Contantkorting gebruiken = Normaal
April betaalt de rest van deze factuur op 15 juli, wat na de kortingsperiode valt. Op de pagina **Openstaande transacties vereffenen** verschijnt geen kortingsbedrag in het veld **Geraamde contantkorting** en de waarde in het veld **Contantkortingsbedrag** is **0,00**. Wanneer April de resterende 700,00 betaalt, wordt geen extra korting gepakt.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | Factuur-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | -700,00                        | USD      | -700,00          |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven. April ziet dat ze al een korting van 3,00 heeft genomen.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/09/2020 |
| Contantkortingsbedrag         | 0,00      |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | -3,00     |
| Contantkortingsbedrag dat moet worden toegepast | 0,00      |

Vervolgens boekt April de betaling. Wanneer ze de pagina **Leverancierstransacties** opent, ziet ze dat de factuur een saldo van 0,00 heeft. Zij ziet ook dat er twee betalingen zijn. Eén betaling is voor 297,00 en heeft 3,00 korting en de andere betaling is voor 700,00.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10020  | Factuur          | 6/25/2020 | 10020   |                                      | 1,000.00                              | 0,00    | USD      |
| APP-10020  | Betaling          | 1-7-2020  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Contantkorting    | 1-7-2020  |         | 3.00                                 |                                       | 0,00    | USD      |
| APP-10021  | Betaling          | 7/15/2020 |         | 700.00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Resterende betalingen op 15 juli, Contantkorting gebruiken = Altijd
Als de leverancier April een korting geeft, hoewel zij na de kortingsdatum betaalt, kan zij de waarde in het veld **Contantkorting gebruiken** wijzigen in **Altijd**. De instelling **Contantkortingen berekenen voor gedeeltelijke betalingen** wordt overschreven en de korting wordt genomen. Het betalingsbedrag is 693,00 en de korting is de resterende 7,00.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|----------|------|------|-----------|-----------|---------|-----------------------|---------------------------------------|----------|------------------|
| Geselecteerd | Altijd            | Factuur-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | 700.00                   |                   | USD      | -693,00          |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/09/2020 |
| Contantkortingsbedrag         | 7.00      |
| Contantkorting gebruiken            | Altijd    |
| Toegepaste contantkorting          | -3,00     |
| Contantkortingsbedrag dat moet worden toegepast | -7,00     |

Vervolgens boekt April de betaling. Wanneer ze de pagina **Leverancierstransacties** opent, ziet ze dat de factuur een saldo van 0,00 heeft. Zij ziet ook dat er twee betalingen zijn. Eén betaling is voor 297,00 en 3,00 korting en de andere betaling is voor 693,00 en 7,00 korting.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10020  | Factuur          | 6/25/2020 | 10020   |                                      | 1,000.00                              | 0,00    | USD      |
| APP-10020  | Betaling          | 1-7-2020  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Contantkorting    | 1-7-2020  |         | 3.00                                 |                                       | 0,00    | USD      |
| APP-10021  | Betaling          | 7/15/2020 |         | 693,00                               |                                       | 0,00    | USD      |
| DISC-10021 | Contantkorting    | 7/15/2020 |         | 7.00                                 |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
