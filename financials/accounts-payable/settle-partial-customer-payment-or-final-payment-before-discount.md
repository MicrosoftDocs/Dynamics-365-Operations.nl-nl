---
title: "Een gedeeltelijke klantenbetaling vereffenen en de definitieve betaling volledig vereffenen vóór de kortingsdatum"
description: Dit artikel geeft scenario&quot;s die laten zien hoe gedeeltelijke betalingen voor een klant worden vastgelegd en hoe contantkortingen worden verkregen in de contantkortingsperiode.
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
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: ac2c569666b97bc430d3d677366a88446ab76091
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Een gedeeltelijke klantenbetaling vereffenen en de definitieve betaling volledig vereffenen vóór de kortingsdatum

[!include[banner](../includes/banner.md)]


Dit artikel geeft scenario's die laten zien hoe gedeeltelijke betalingen voor een klant worden vastgelegd en hoe contantkortingen worden verkregen in de contantkortingsperiode.

Fabrikam verkoopt goederen aan klant 4028. Fabrikam biedt een contantkorting van 1 procent als de factuur binnen 14 dagen wordt betaald. Facturen moeten worden betaald binnen 30 dagen. Fabrikam biedt ook contantkortingen op gedeeltelijke betalingen. De vereffeningparameters bevinden zich op de pagina **Leveranciersparameters**.

## <a name="customer-invoice"></a>Klantfactuur
Op 25 juni voert Arnie een factuur in en boekt deze voor 1.000,00 voor klant 4028. Arnie kan deze transactie bekijken op de pagina** Klanttransacties**.

| Boekstuk   | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Factuur          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 1.000,00 | USD      |

Op de pagina **Klant** of **Klanttransacties** kan Arnie de pagina **Transacties vereffenen** openen om de data en bedragen van contantkortingen te bekijken die voor de factuur beschikbaar zijn. De vervaldatum is 25 juli en een contantkorting van 10,00 is beschikbaar als de factuur voor 9 juli wordt betaald.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2015 | 25/7/2015 | 10010   | 1.000,00                       | USD      | 990,00           |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven voor de gemarkeerde factuur.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 10,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 10,00     |

Arnie klikt op het tabblad **Contantkorting** om het kortingsbedrag te bekijken.

| Datum van contantkorting | Contantkortingsbedrag | Bedrag in transactievaluta |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Gedeeltelijke betaling via de pagina Klantbetalingen invoeren
Klant 4028 verzendt op 1 juli een betaling van 500,00. Om deze betaling in te voeren, klikt Arnie niet op **Regels**. Hij registreert de betaling door een nieuw betalingsjournaal te maken en vervolgens de pagina **Klantbetalingen invoeren** te openen. Hij voert de betalingsgegevens in en markeert de factuur die hij ingevoerd heeft. Wanneer Arnie **500,00** invoert als het bedrag, typt hij ook **500,00** in het veld **Te betalen bedrag** in het raster. Omdat Fabrikam een contantkorting op gedeeltelijke betalingen toestaat, ziet hij dat een gedeeltelijke contantkorting van 5,05 ook wordt uitgevoerd. De berekening van deze korting is 500,00 ÷ 0,99 × 0,01 = 5,05. (In deze berekening wordt 500,00 gedeeld door 0,99, aangezien er een korting van 1 procent is. Daarom betaalt de klant 99 procent van de factuur. Het resultaat wordt vervolgens vermenigvuldigd met het kortingspercentage van 1 procent of 0,01. Als de klant de volledige korting van 10,00 neemt, is het bedrag dat moet worden vereffend 990,00. De kortinggegevens worden weergegeven in het raster onder aan de pagina **Klantbetalingen invoeren**.

| Contantkortingsbedrag dat moet worden toegepast | Toegepaste contantkorting | Te betalen bedrag |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Gedeeltelijke betaling door de journaalregels te gebruiken
In plaats van in het betalingsjournaal de pagina **Klantbetalingen invoeren** te openen, kan Arnie ook klikken op **Regels** om een betaling uit te voeren. Het betalingsjournaal wordt weergegeven waar Arnie een regel in kan voeren voor klant 4028. Arnie opent vervolgens de pagina **Transacties vereffenen**, zodat hij de factuur kan markeren voor vereffening. Arnie markeert de factuur en wijzigt de waarde in het veld **Bedrag om te vereffenen** naar **500,00**. Nogmaals ziet hij dat de waarde in het veld **Contantkortingsbedrag** voor de volledige factuur **10,00** is en de waarde in het veld **Contantkortingsbedrag dat moet worden toegepast** **5,05** is. Daarom vereffent Arnie 505,05 van deze factuur.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2015 | 25/7/2015 | 10010   | 1.000,00                       | USD      | 500,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 10,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 5,05      |

Als de klant precies de helft van de factuur wil vereffenen, doet de klant een betaling van 495,00. In dit geval typt Arnie **495,00** in het veld **Bedrag om te vereffenen**. De contantkorting voor 5,00 wordt ook toegepast, zodat het totale vereffende bedrag 500,00 is.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2015 | 25/7/2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 10,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 5,00      |

Arnie sluit de pagina **Transacties vereffenen**. Een betalingsregel voor 495,00 wordt in het journaal gemaakt en vervolgens boekt Arnie het journaal. Hij kan de klanttransacties controleren op de pagina **Klanttransacties**. Op deze pagina ziet Arnie dat de factuur een saldo van 500,00 heeft. Hij ziet ook een betaling van 495,00 en een korting van 5,00.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Factuur          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 500,00  | USD      |
| ARP-10010  |  Betaling         | 01-07-2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 |  Contantkorting   | 01-07-2015  |         |                                      | 5,00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Betaling voor het resterende bedrag
Klant 4028 betaalt de rest van het bedrag van 495,00 op 8 juli, wat binnen de periode van de contantkorting valt. Arnie maakt op 8 juli het betalingsjournaal en markeert de transactie voor vereffening. Hij ziet dat het bedrag dat moet worden vereffend 495,00 is. De waarde in het veld **Geraamde contantkorting** is **5,00**, omdat de korting van 5,00 eerder is toegepast.

|                         |        |
|-------------------------|--------|
| Gemarkeerd totaal            | 495,00 |
| Geraamde contantkorting | 5,00   |

Informatie over de gemarkeerde transactieregel wordt weergegeven in het raster op de pagina **Openstaande transacties vereffenen**.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10010 | 4028    | 6/25/2015 | 25/7/2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 10,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 5,00      |
| Contantkortingsbedrag dat moet worden toegepast | 5,00      |

Arnie boekt dit journaal en controleert de klanttransacties op de pagina **Klanttransacties**. Het saldo van de factuur is nu 0,00 en Arnie ziet de twee betalingen en de twee contantkortingen.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Factuur          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10010  | Betaling          | 01-07-2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 | Contantkorting    | 01-07-2015  |         |                                      | 5,00                                  | 0,00    | USD      |
| ARP-10011  | Betaling          | 8-7-2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10011 | Contantkorting    | 8-7-2015  |         |                                      | 5,00                                  | 0,00    | USD      |






