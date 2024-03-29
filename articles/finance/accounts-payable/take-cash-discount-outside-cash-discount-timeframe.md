---
title: Een contantkorting buiten de periode van contantkorting nemen
description: Dit artikel biedt twee scenario's die laten zien hoe een contantkorting kan worden verkregen, zelfs als de betaling buiten de contantkortingsperiode wordt gedaan.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26b1eb5e542acf7496d1a0cf7196716a5de75e4e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780474"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Een contantkorting buiten de periode van contantkorting nemen

[!include [banner](../includes/banner.md)]

Dit artikel biedt twee scenario's die laten zien hoe een contantkorting kan worden verkregen, zelfs als de betaling buiten de contantkortingsperiode wordt gedaan.

Op 28 juni maakt April een factuur voor 2.000,00 voor leverancier 3052. De factuur biedt een contantkorting van 1 procent als de factuur binnen 14 dagen wordt betaald.

## <a name="use-cash-discount-option--always"></a>De optie Contantkorting gebruiken = altijd
April voert een betaling uit op 1 juli, wat na de kortingsdatum is. April opent de pagina **Transacties vereffenen** om de transacties weer te geven die kunnen worden vereffend. 

April markeert de factuur voor betaling. Er wordt geen contantkorting genomen omdat de betaling na de kortingsdatum komt. De leverancier heeft April echter goedkeuring gegeven om de contantkorting toch te nemen. Daarom wijzigt April de waarde in het veld **Contantkorting gebruiken** in **Altijd**.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum van contantkorting | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Altijd            | Factuur-10030 | 3052    | 6/28/2020          | 7/12/2020 | 10030   | -2000,00                      | USD      | -1980,00        |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/12/2020 |
| Contantkortingsbedrag         | -20,00    |
| Contantkorting gebruiken            | Altijd    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Datum die moet worden gebruikt voor berekenen van kortingen = Geselecteerde datum
Als zowel de factuur als de betaling is geboekt, kan de contantkorting nog worden genomen als de transacties op de pagina **Transacties vereffenen** worden vereffend. April wijzigt de waarde in het veld **Datum die moet worden gebruikt voor berekenen van kortingen** in **Geselecteerde datum**. Ze voert vervolgens als datum 28 juni in, wat binnen de kortingsperiode voor de factuur ligt. Die datum wordt gebruikt om een contantkorting te berekenen voor de transactie. Op de pagina **Openstaande transacties vereffenen** ziet April dat de gehele korting van 20,00 standaard wordt weergegeven. De factuurregel geeft aan dat het te vereffenen bedrag 1980,00 is.

| Markeren          | Contantkorting gebruiken | Boekstuk   | Rekening | Datum van contantkorting | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|--------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd en gemarkeerd | Normaal    | Factuur-10030 | 3052    | 6/28/2020         | 7/12/2020 | 10030   | -2000,00                      | USD      | -1980,00        |
| Geselecteerd                 | Normaal    | APP-10030 | 3052    | 7/15/2020          | 7/15/2020 |         | 500.00                         | USD      | 500.00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven. Het kortingsbedrag dat is genomen is 20,00 omdat het te vereffenen bedrag voor de factuur het standaardbedrag is, 1980,00.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/12/2020 |
| Contantkortingsbedrag         | -20,00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -20,00    |

April wijzigt de waarde in het veld **Bedrag om te vereffenen** naar **500,00**. De waarde in het veld **Contantkortingsbedrag dat moet worden toegepast** wordt berekend als **5,05**.

| Markeren                     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd en gemarkeerd | Normaal            | Factuur-10030 | 3052    | 6/28/2020 | 7/12/2020 | 10030   | 2,000.00                       | USD      | -500.00          |
| Geselecteerd                 | Normaal            | APP-10030 | 3052    | 7/15/2020 | 7/15/2020 |         | 500.00                         | USD      | 500.00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven. De waarde in het veld **Contantkortingsbedrag dat moet worden toegepast** is **5,05** omdat het te vereffenen bedrag voor de factuur werd gewijzigd naar het bedrag van de betaling, 500,00.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/12/2020 |
| Contantkortingsbedrag         | -20,00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
