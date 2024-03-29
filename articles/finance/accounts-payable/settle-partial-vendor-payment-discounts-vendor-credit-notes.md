---
title: Een gedeeltelijke leveranciersbetaling vereffenen met kortingen op creditnota's
description: Dit artikel begeleidt u door een scenario waarin een creditnota voor een factuur wordt vereffend.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
ms.openlocfilehash: b926d94059fb12b143b9c9b4b5c04cb7f39f8e99
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715932"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-credit-notes"></a>Een gedeeltelijke leveranciersbetaling vereffenen met kortingen op creditnota's

[!include [banner](../includes/banner.md)]

Dit artikel begeleidt u door een scenario waarin een creditnota voor een factuur wordt vereffend.

Leveranciers van Fabrikam geven contantkortingen op creditnota's. Leverancier 3050 laat Fabrikam een contantkorting van 1 procent nemen als een factuur wordt betaald binnen 14 dagen.

## <a name="invoice-and-credit-memo"></a>Factuur en creditnota
Op 29 juni maakt April een factuur voor 1000,00 voor leverancier 3050. Op 2 juli maakt ze een creditnota voor 200,00. Via de pagina **Leveranciers** opent April de pagina **Transacties vereffenen**. Ze kan de pagina **Transacties vereffenen** gebruiken om zowel de creditnota als de factuur voor de vereffening te markeren. Er wordt een korting van 2,00 berekend op de creditnota. Daarom wordt de totale waarde van de creditnota teruggebracht tot 198,00.

| Markeren                     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd                 | Normaal            | Factuur-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070   | -1.000,00                      | USD      | -990,00          |
| Geselecteerd en gemarkeerd | Normaal            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200,00                         | USD      | 198,00           |

Informatie over korting voor de creditnota wordt onder de pagina **Openstaande transacties vereffenen** weergegeven.

| Veld                        | Waarde     |
|------------------------------|-----------|
| Datum voor contantkorting           | 13-7-2015 |
| Contantkortingsbedrag         | 2.00      |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 2,00      |

April klikt op **Boeken**. Ze controleert vervolgens de voltooide vereffening. April ziet dat 198,00 van de creditnota is vereffend en dat een korting van 2,00 is doorgevoerd. Daarom is het totaal 200,00.

| Markeren                     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur  | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Geselecteerd en gemarkeerd | Normaal            | Factuur-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070    | -1.000,00                      | USD      | -200,00          |
| Geselecteerd                 | Normaal            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 | CR-10070 | 200,00                         | USD      | 198,00           |

April kan de leveranciertransacties op de pagina **Leveranciertransacties** controleren door een leverancier op de pagina **Alle leveranciers** te selecteren en vervolgens in het Actievenster te klikken op **Transacties**. Op deze pagina ziet April dat de factuur een saldo van -800,00 heeft. Ze ziet ook een creditnota voor 198,00 en een korting van 2,00.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10070  | Factuur          | 6/29/2015 | 10070   |                                      | 1.000,00                              | -800,00 | USD      |
| Factuur-10071  |                  | 7/2/2015  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| DISC-10071 |  Contantkorting   | 7/2/2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| DISC-10071 |  Contantkorting   | 7/2/2015  |         |                                      | 2,00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
