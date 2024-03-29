---
title: Gedeeltelijke en definitieve betalingen volledig vereffenen vóór de kortingsdatum
description: Dit artikel geeft scenario's die laten zien hoe gedeeltelijke betalingen voor een klant worden vastgelegd en hoe contantkortingen worden verkregen in de contantkortingsperiode.
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
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
ms.openlocfilehash: a8da366b1e770ea649603ae85d4acc5e377ed9fb
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780461"
---
# <a name="settle-partial-and-final-payments-in-full-before-the-discount-date"></a>Gedeeltelijke en definitieve betalingen volledig vereffenen vóór de kortingsdatum

[!include [banner](../includes/banner.md)]

Dit artikel geeft scenario's die laten zien hoe gedeeltelijke betalingen voor een klant worden vastgelegd en hoe contantkortingen worden verkregen in de contantkortingsperiode.

Fabrikam verkoopt goederen aan klant 4028. Fabrikam biedt een contantkorting van 1 procent als de factuur binnen 14 dagen wordt betaald. Facturen moeten worden betaald binnen 30 dagen. Fabrikam biedt ook contantkortingen op gedeeltelijke betalingen. De vereffeningparameters bevinden zich op de pagina **Leveranciersparameters**.

## <a name="customer-invoice"></a>Klantfactuur
Op 25 juni voert Arnie een factuur in en boekt deze voor 1.000,00 voor klant 4028. Arnie kan deze transactie bekijken op de pagina **Klanttransacties**.

| Boekstuk   | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Factuur          | 6/25/2020 | 10010   | 1,000.00                             |                                       | 1,000.00 | USD      |

Op de pagina **Klant** of **Klanttransacties** kan Arnie de pagina **Transacties vereffenen** openen om de data en bedragen van contantkortingen te bekijken die voor de factuur beschikbaar zijn. De vervaldatum is 25 juli en een contantkorting van 10,00 is beschikbaar als de factuur voor 9 juli wordt betaald.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2020 | 7/25/2020 | 10010   | 1,000.00                       | USD      | 990.00           |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven voor de gemarkeerde factuur.

|    &nbsp;                    |  &nbsp;   |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/09/2020 |
| Contantkortingsbedrag         | 10.00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 10,00     |

Arnie klikt op het tabblad **Contantkorting** om het kortingsbedrag te bekijken.

| Datum van contantkorting | Contantkortingsbedrag | Bedrag in transactievaluta |
|--------------------|----------------------|--------------------------------|
| 7/9/2020           | 10.00                | 990.00                         |
| 7/25/2020          | 0,00                 | 1,000.00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Gedeeltelijke betaling via de pagina Klantbetalingen invoeren
Klant 4028 verzendt op 1 juli een betaling van 500,00. Om deze betaling in te voeren, klikt Arnie niet op **Regels**. Arnie registreert de betaling door een nieuw betalingsjournaal te maken en vervolgens de pagina **Klantbetalingen invoeren** te openen. Arnie voert de betalingsgegevens in en markeert de factuur die hij ingevoerd heeft. Wanneer Arnie **500,00** invoert als het bedrag, voert hij ook **500,00** in het veld **Te betalen bedrag** in het raster in. Omdat Fabrikam een contantkorting op gedeeltelijke betalingen toestaat, ziet Arnie dat een gedeeltelijke contantkorting van 5,05 ook wordt uitgevoerd. De berekening van deze korting is 500,00 ÷ 0,99 × 0,01 = 5,05. (In deze berekening wordt 500,00 gedeeld door 0,99, aangezien er een korting van 1 procent is. Daarom betaalt de klant 99 procent van de factuur. Het resultaat wordt vervolgens vermenigvuldigd met het kortingspercentage van 1 procent of 0,01. Als de klant de volledige korting van 10,00 neemt, is het bedrag dat moet worden vereffend 990,00. De kortinggegevens worden weergegeven in het raster onder aan de pagina **Klantbetalingen invoeren**.

| Contantkortingsbedrag dat moet worden toegepast | Toegepaste contantkorting | Te betalen bedrag |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Gedeeltelijke betaling door de journaalregels te gebruiken
In plaats van in het betalingsjournaal de pagina **Klantbetalingen invoeren** te openen, kan Arnie ook klikken op **Regels** om een betaling uit te voeren. Het betalingsjournaal wordt weergegeven waar Arnie een regel in kan voeren voor klant 4028. Arnie opent vervolgens de pagina **Transacties vereffenen**, zodat Arnie de factuur kan markeren voor vereffening. Arnie markeert de factuur en wijzigt de waarde in het veld **Bedrag om te vereffenen** naar **500,00**. Nogmaals ziet Arnie dat de waarde in het veld **Contantkortingsbedrag** voor de volledige factuur **10,00** is en de waarde in het veld **Contantkortingsbedrag dat moet worden toegepast** **5,05** is. Daarom vereffent Arnie 505,05 van deze factuur.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2020 | 7/25/2020 | 10010   | 1,000.00                       | USD      | 500.00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|        &nbsp;                | &nbsp;    |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/09/2020 |
| Contantkortingsbedrag         | 10.00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 5,05      |

Als de klant precies de helft van de factuur wil vereffenen, doet de klant een betaling van 495,00. In dit geval typt Arnie **495,00** in het veld **Bedrag om te vereffenen**. De contantkorting voor 5,00 wordt ook toegepast, zodat het totale vereffende bedrag 500,00 is.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2020 | 7/25/2020 | 10010   | 1,000.00                       | USD      | 495,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|     &nbsp;                   | &nbsp;    |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/09/2020 |
| Contantkortingsbedrag         | 10.00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 5,00      |

Arnie sluit de pagina **Transacties vereffenen**. Een betalingsregel voor 495,00 wordt in het journaal gemaakt en vervolgens boekt Arnie het journaal. Arnie kan de klanttransacties controleren op de pagina **Klanttransacties**. Op deze pagina ziet Arnie dat de factuur een saldo van 500,00 heeft. En ziet ook een betaling van 495,00 en een korting van 5,00.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Factuur          | 6/25/2020 | 10010   | 1,000.00                             |                                       | 500.00  | USD      |
| ARP-10010  |  Betaling         | 1-7-2020  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 |  Contantkorting   | 1-7-2020  |         |                                      | 5.00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Betaling voor het resterende bedrag
Klant 4028 betaalt de rest van het bedrag van 495,00 op 8 juli, wat binnen de periode van de contantkorting valt. Arnie maakt op 8 juli het betalingsjournaal en markeert de transactie voor vereffening. Arnie ziet dat het bedrag dat moet worden vereffend 495,00 is. De waarde in het veld **Geraamde contantkorting** is **5,00**, omdat de korting van 5,00 eerder is toegepast.

|   &nbsp;                | &nbsp; |
|-------------------------|--------|
| Gemarkeerd totaal            | 495,00 |
| Geraamde contantkorting | 5,00   |

Informatie over de gemarkeerde transactieregel wordt weergegeven in het raster op de pagina **Openstaande transacties vereffenen**.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2020 | 7/25/2020 | 10010   | 1,000.00                       | USD      | 495,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Datum voor contantkorting           | 7/09/2020 |
| Contantkortingsbedrag         | 10.00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 5,00      |
| Contantkortingsbedrag dat moet worden toegepast | 5,00      |

Arnie boekt dit journaal en controleert de klanttransacties op de pagina **Klanttransacties**. Het saldo van de factuur is nu 0,00 en Arnie ziet de twee betalingen en de twee contantkortingen.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Factuur          | 6/25/2020 | 10010   | 1,000.00                             |                                       | 0,00    | USD      |
| ARP-10010  | Betaling          | 1-7-2020  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 | Contantkorting    | 1-7-2020  |         |                                      | 5.00                                  | 0,00    | USD      |
| ARP-10011  | Betaling          | 7/8/2020  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10011 | Contantkorting    | 7/8/2020  |         |                                      | 5.00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
