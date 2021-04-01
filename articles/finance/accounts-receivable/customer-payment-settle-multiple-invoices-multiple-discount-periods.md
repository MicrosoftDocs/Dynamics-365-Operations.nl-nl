---
title: Eén klantbetaling gebruiken om facturen te vereffenen die verschillende kortingsperioden omvatten
description: Dit onderwerp toont hoe meerdere facturen worden betaald wanneer elke factuur in aanmerking komt voor een contantkorting. De scenario's in dit artikel markeren hoe de verkregen contantkortingen variëren, afhankelijk van wanneer de betaling wordt uitgevoerd.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16e255c471ed2f551a6cf62e9750ac0eee57a5b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236957"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Eén klantbetaling gebruiken om facturen te vereffenen die verschillende kortingsperioden omvatten

[!include [banner](../includes/banner.md)]

Dit onderwerp toont hoe meerdere facturen worden betaald wanneer elke factuur in aanmerking komt voor een contantkorting. De scenario's in dit artikel markeren hoe de verkregen contantkortingen variëren, afhankelijk van wanneer de betaling wordt uitgevoerd.

Fabrikam verkoopt goederen aan klant 4032. Fabrikam biedt een contantkorting van 1 procent als de factuur binnen 14 dagen wordt betaald. Fabrikam biedt ook contantkortingen op gedeeltelijke betalingen. De vereffeningparameters bevinden zich op de pagina **Leveranciersparameters**.

## <a name="invoices"></a>Facturen
Klant 4032 heeft drie facturen van in totaal 3.000,00:

-   Factuur FTI-10040 voor 1000,00 is op 15 mei ingevoerd. Deze factuur komt in aanmerking voor een contantkorting van 1 procent als de factuur binnen 14 dagen wordt betaald.
-   Factuur FTI-10041 voor 1.000,00 is op 25 juni ingevoerd. Deze factuur komt in aanmerking voor een contantkorting van 1 procent als de factuur binnen 14 dagen wordt betaald.
-   Factuur FTI-10042 voor 1.000,00 is op 25 juni ingevoerd. Deze factuur komt in aanmerking voor een contantkorting van 2 procent als deze binnen vijf dagen wordt betaald en een korting van 1 procent als deze binnen 14 dagen wordt betaald.

## <a name="settle-all-invoices-on-june-29"></a>Alle facturen vereffenen op 29 juni
Als Arnie een betalingsdagboek maakt om deze facturen volledig te vereffenen op 29 juni, wordt de betaling 2.970,00. Het totaal van alle kortingsbedragen bedraagt 30,00. Arnie maakt een betaling voor klant 4032 en opent vervolgens de pagina **Transacties vereffenen**. Op de pagina **Transacties vereffenen** markeert Arnie alle drie factuurregels voor vereffening:

-   De betaling voor factuur FTI-10040 bedraagt 1.000,00. Er is geen korting genomen.
-   De betaling voor factuur FTI-10041 bedraagt 990,00. Een contantkorting van 1 procent, of 10,00, wordt toegepast.
-   De betaling voor factuur FTI-10042 bedraagt 980,00. Een contantkorting van 2 procent, of 20,00, wordt toegepast.

| Markeren                     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Geselecteerd                 | Normaal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1.000,00                             |                                       | USD      | 1.000,00         |
| Geselecteerd                 | Normaal            | FTI-10041 | 4032    | 6/25/2015 | 25/7/2015 | 10041   | 1.000,00                             |                                       | USD      | 990,00           |
| Geselecteerd en gemarkeerd | Normaal            | FTI-10042 | 4032    | 6/25/2015 | 25/7/2015 | 10042   | 1.000,00                             |                                       | USD      | 980,00           |

Nadat de betaling is geboekt, bedraagt het klantsaldo 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Alle facturen vereffenen op 1 juli
Als Arnie een betalingsdagboek maakt om deze facturen volledig te vereffenen op 1 juli, wordt de betaling 2.980,00. Arnie maakt een betaling voor klant 4032 en opent vervolgens de pagina **Transacties vereffenen**. Op de pagina **Transacties vereffenen** markeert Arnie alle drie factuurregels voor vereffening:

-   De betaling voor factuur FTI-10040 bedraagt 1.000,00. Er is geen korting genomen.
-   De betaling voor factuur FTI-10041 bedraagt 990,00. Een contantkorting van 1 procent, of 10,00, wordt toegepast.
-   De betaling voor factuur FTI-10042 bedraagt 990,00. Een contantkorting van 1 procent, of 10,00, wordt toegepast. Hoewel 1 juli na de periode voor de korting van 2 procent valt, is dit nog steeds binnen de periode voor de korting van 1 procent.

| Markeren                     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Geselecteerd                 | Normaal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1.000,00                             |                                       | USD      | 1.000,00         |
| Geselecteerd                 | Normaal            | FTI-10041 | 4032    | 6/25/2015 | 25/7/2015 | 10041   | 1.000,00                             |                                       | USD      | 990,00           |
| Geselecteerd en gemarkeerd | Normaal            | FTI-10042 | 4032    | 6/25/2015 | 25/7/2015 | 10042   | 1.000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Gedeeltelijke vereffening op 29 juni
Klant 4032 kan een gedeeltelijk bedrag betalen, zoals de helft van elke factuur. Arnie maakt een betaling voor klant 4032 en opent vervolgens de pagina **Transacties vereffenen**. Op de pagina **Transacties vereffenen** markeert Arnie alle drie factuurregels voor vereffening. Op elke regel voert hij het te vereffenen bedrag in, op basis van de instructies die de klant heeft verstrekt. Wanneer Arnie een regel selecteert, ziet hij het kortingsbedrag voor die regel en het bedrag voor contantkorting dat is toegepast. Omdat de klant de helft van de factuur betaalt, ziet Arnie dat de waarde in het veld **Contantkortingsbedrag** voor FTI-10042 **20,00** is, maar dat de waarde in het veld **Toegepaste contantkorting** **10,00** bedraagt. Het betalingsbedrag is 1485,00.

| Markeren                     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Geselecteerd                 | Normaal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1.000,00                             |                                       | USD      | 500,00           |
| Geselecteerd                 | Normaal            | FTI-10041 | 4032    | 6/25/2015 | 25/7/2015 | 10041   | 1.000,00                             |                                       | USD      | 495,00           |
| Geselecteerd en gemarkeerd | Normaal            | FTI-10042 | 4032    | 6/25/2015 | 25/7/2015 | 10042   | 1.000,00                             |                                       | USD      | 490,00           |

Arnie kan het betalingsbedrag van 1485,00 ook handmatig invoeren voordat hij de pagina **Transacties vereffenen** opent. Als Arnie het betalingsbedrag handmatig invoert en vervolgens alle drie de transacties markeert, maar de waarde in het veld **Bedrag om te vereffenen** niet aanpast voor elke transactie, ontvangt hij het volgende bericht wanneer hij de pagina sluit:

> Het totaalbedrag van de gemarkeerde transacties verschilt van het journaalbedrag. Wilt u het journaalbedrag wijzigen?

Als Arnie wil dat het betalingsbedrag slechts 1485,00 is, moet hij op **Nee** klikken en vervolgens het journaal boeken. De transacties worden als volgt vereffend:

1.  Factuur FTI-10040 is volledig vereffend voor 1.000,00, omdat deze op 15 mei werd ingevoerd en dit de oudste factuur is. Er is geen korting genomen. Het resterende bedrag van de betalingstransactie is 485,00.
2.  Factuur FTI-10041 is helemaal niet vereffend. Facturen FTI-10041 en FTI-10042 werden op dezelfde datum ingevoerd. Er is echter een korting van 1 procent beschikbaar voor factuur FTI-10041 en een korting van 2 voor factuur FTI-10042. Omdat er een betere korting beschikbaar is voor factuur FTI-10042, wordt de resterende 485,00 vereffend met factuur FTI-10042.
3.  Factuur FTI-10042 wordt vereffend met de resterende 485,00. Fabrikam biedt gedeeltelijke kortingen. In dit geval wordt de korting 9,90 (= 485,00 ÷ 0,98 x 0,02). Het bedragt (485,00) wordt gedeeld door 0,98 omdat er een korting van 2 procent is (zodat de klant 98 procent van de factuur betaalt). Het resultaat wordt vervolgens vermenigvuldigd met het kortingspercentage of 2 procent. De betaling van 485,00 plus de korting van 9,90 is gelijk aan 494,90. Het bedrag van de oorspronkelijke factuur was 1000,00. Daarom heeft de transactie een saldo van 505,10 (= 1.000,00 – 494,90).

Arnie bekijkt de informatie op de pagina **Klanttransacties**.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo  | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Factuur          | 15/5/2015 | 10040   | 1.000,00                             |                                       | 0,00     | USD      |
| FTI-10041  | Factuur          | 6/25/2015 | 10041   | 1.000,00                             |                                       | 1.000,00 | USD      |
| FTI-10042  | Factuur          | 6/25/2015 | 10042   | 1.000,00                             |                                       | 505,10   | USD      |
| ARP-10040  | Betaling          | 6/29/2015 |         |                                      | 1.485,00                              | 0,00     | USD      |
| DISC-10040 | Contantkorting    | 6/29/2015 |         |                                      | 9,90                                  | 0,00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]