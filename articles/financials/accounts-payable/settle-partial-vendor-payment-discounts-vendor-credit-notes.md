---
title: Een gedeeltelijke leverancierbetaling vereffenen met kortingen op creditnota's van de leverancier
description: Dit artikel begeleidt u door een scenario waarin een creditnota voor een factuur wordt vereffend.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ec2317f12142f726ad37e39fe11837847b0a5b04
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Een gedeeltelijke leverancierbetaling vereffenen met kortingen op creditnota's van de leverancier

[!include[banner](../includes/banner.md)]


Dit artikel begeleidt u door een scenario waarin een creditnota voor een factuur wordt vereffend.

Leveranciers van Fabrikam geven contantkortingen op creditnota's. Leverancier 3050 laat Fabrikam een contantkorting van 1 procent nemen als een factuur wordt betaald binnen 14 dagen.

## <a name="invoice-and-credit-memo"></a>Factuur en creditnota
Op 29 juni maakt April een factuur voor 1000,00 voor leverancier 3050. Op 2 juli maakt ze een creditnota voor 200,00. Via de pagina **Leveranciers** opent April de pagina **Transacties vereffenen**. Ze kan de pagina **Transacties vereffenen** gebruiken om zowel de creditnota als de factuur voor de vereffening te markeren. Er wordt een korting van 2,00 berekend op de creditnota. Daarom wordt de totale waarde van de creditnota teruggebracht tot 198,00.

| Markeren                     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd                 | Normaal            | Factuur-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070   | -1.000,00                      | USD      | -990,00          |
| Geselecteerd en gemarkeerd | Normaal            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200,00                         | USD      | 198,00           |

Informatie over korting voor de creditnota wordt onder de pagina **Openstaande transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 13-7-2015 |
| Contantkortingsbedrag         | 2,00      |
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






