---
title: Een gedeeltelijke leverancierbetaling vereffenen en de definitieve betaling volledig vereffenen vóór de kortingsdatum
description: Dit onderwerp begeleidt u door een scenario waarin meerdere gedeeltelijke betalingen worden gedaan voor een leveranciersfactuur en een contantkorting wordt genomen.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04b00c8407ea2fd7d1e4b58db47c392989a20577
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716238"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Een gedeeltelijke leverancierbetaling vereffenen en de definitieve betaling volledig vereffenen vóór de kortingsdatum

[!include [banner](../includes/banner.md)]

Dit onderwerp begeleidt u door een scenario waarin meerdere gedeeltelijke betalingen worden gedaan voor een leveranciersfactuur en een contantkorting wordt genomen.

Fabrikam koopt goederen aan bij leverancier 3064. De leverancier geeft Fabrikam een contantkorting van 1 procent als de factuur wordt betaald binnen 14 dagen. Facturen moeten worden betaald binnen 30 dagen. De leverancier laat Fabrikam ook contantkortingen nemen op gedeeltelijke betalingen. De vereffeningparameters bevinden zich op de pagina **Parameters van module Leveranciers**. Op 25 juni voert April een factuur voor leverancier 3064 in van 1000,00.

## <a name="vendor-invoice-on-june-25"></a>Leveranciersfactuur op 25 juni
Op 25 juni voert April een factuur in en boekt deze voor 1.000,00 voor leverancier 3064. April kan deze transactie op de pagina **Leverancierstransacties** weergeven.

| Boekstuk   | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo   | Valuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Factuur-10010 | 6/25/2015 | 10010   |                                      | 1.000,00                              | -1.000,00 | USD      |

Via de pagina **Leveranciers** opent April de pagina **Transacties vereffenen**. Ze kan de pagina **Transacties vereffenen** gebruiken om de data en de bedragen van contantkortingen te bekijken. De vervaldatum is 25 juli en een contantkorting van -10,00 is beschikbaar als de factuur voor 9 juli wordt betaald.

| Markeren | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normaal            | Factuur-10010 | 3064    | 6/25/2015 | 25/7/2015 | 10010   | 1.000,00                       | USD      | 990,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|       &nbsp;                 | &nbsp;    |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | -10,00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -10,00    |

April klikt op het tabblad **Contantkorting** om het kortingsbedrag te bekijken.

| Datum van contantkorting | Contantkortingsbedrag | Bedrag in transactievaluta |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Gedeeltelijke betaling op 1 juli via de pagina Vereffenen open transacties
April kan voor deze betaling een betalingsjournaal maken door de pagina **Betalingsjournaal** in Leveranciers te openen. Ze maakt een nieuw betalingsjournaal en voert een regel voor leverancier 3064 in. Ze opent vervolgens de pagina **Transacties vereffenen**, zodat ze de factuur kan markeren voor vereffening. April markeert de factuur en wijzigt de waarde in het veld **Bedrag om te vereffenen** naar **-500,00**. Ze ziet dat de waarde in het veld **Contantkortingsbedrag** voor de volledige factuur **-10,00** is en de waarde in het veld **Contantkortingsbedrag dat moet worden toegepast** **-5,05** is. Daarom vereffent April -505,05 van deze factuur.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2015 | 25/7/2015 | 10010   | 1.000,00                       | USD      | -500,00          |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | -10,00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -5,05     |

April wil precies de helft van de factuur vereffenen. Daarom wijzigt ze de waarde in het veld **Bedrag om te vereffenen** naar **-495,00**. Het totale bedrag dat is vereffend bedraagt nu 500,00. Dit bedrag is inclusief de korting van -5,00.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2015 | 25/7/2015 | 10010   | 1.000,00                       | USD      | -495,00          |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | -10,00    |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -5,00     |

April sluit de pagina **Transacties vereffenen**. Een betalingsregel voor 495,00 wordt in het journaal gemaakt en vervolgens boekt April het journaal. April kan de leverancierstransacties controleren op de pagina **Leveranciertransacties**. Ze ziet dat de factuur een saldo van -500,00 heeft. Ze ziet ook een betaling van 495,00 en een contantkorting van 5,00.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10010  | Factuur          | 6/25/2015 | 10010   |                                      | 1.000,00                              | -500,00 | USD      |
| APP-10010  | Betaling          | 01-07-2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Contantkorting    | 01-07-2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Het resterende bedrag betaald op 8 juli
April betaalt de rest van de factuur voor leverancier 3064 op 8 juli, wat binnen de periode van de contantkorting valt. April maakt op 8 juli het betalingsjournaal en markeert de transactie voor vereffening. Ze ziet dat het bedrag dat moet worden vereffend 495,00 is. De waarde in het veld **Geraamde contantkorting** is **-5,00**, omdat de korting van 5,00 eerder is toegepast.

|  &nbsp;                 |  &nbsp; |
|-------------------------|--------|
| Gemarkeerd totaal            | 495,00 |
| Geraamde contantkorting | -5,00  |

Informatie over de gemarkeerde transactieregel wordt weergegeven in het raster op de pagina **Openstaande transacties vereffenen**.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2015 | 25/7/2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|  &nbsp;                      | &nbsp;    |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 10,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 5,00      |
| Contantkortingsbedrag dat moet worden toegepast | 5,00      |

April boekt het betalingsjournaal en controleert de leveranciertransacties op de pagina **Leveranciertransacties**. Het saldo van de factuur is nu 0,00 en April ziet de twee betalingen en de twee contantkortingen.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Factuur-10010  | Factuur          | 6/25/2015 | 10010   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10010  |  Betaling         | 01-07-2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Contantkorting    | 01-07-2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10011  | Betaling          | 8-7-2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10011 | Contantkorting    | 8-7-2015  |         | 5,00                                 |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
