---
title: "Een gedeeltelijke klantenbetaling uitvoeren vóór de kortingsdatum met een definitieve betaling na de kortingsdatum"
description: Dit artikel bespreekt het effect van het vereffenen van betalingen aan facturen voor klanten. Het scenario richt zich op de gevolgen in de subadministratie, niet in het grootboek.
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
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: f3234bf607ef9ce1643226894716b975a2c2a7b9
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Een gedeeltelijke klantenbetaling uitvoeren vóór de kortingsdatum met een definitieve betaling na de kortingsdatum

[!include[banner](../includes/banner.md)]


Dit artikel bespreekt het effect van het vereffenen van betalingen aan facturen voor klanten. Het scenario richt zich op de gevolgen in de subadministratie, niet in het grootboek.

Fabrikam verkoopt goederen aan klant 4027. Fabrikam biedt een contantkorting van 1 procent als de factuur binnen 14 dagen wordt betaald. Facturen moeten worden betaald binnen 30 dagen. Fabrikam biedt ook contantkortingen op gedeeltelijke betalingen. De vereffeningparameters bevinden zich op de pagina **Leveranciersparameters**.

## <a name="invoice"></a>Factuur
Op 25 juni voert Arnie een factuur in en boekt deze voor 1.000,00 voor klant 4027. Arnie kan deze factuur weergeven met de knop **Transacties** op de pagina **Klanten**.

| Boekstuk   | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | Factuur          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 1.000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Gedeeltelijke betaling vóór de datum van contantkorting
Op 2 juli verricht klant 4027 een gedeeltelijke betaling van 297,00 voor de factuur. De betaling komt in aanmerking voor een contantkorting, omdat Fabrikam contantkortingen op gedeeltelijke betalingen biedt, en de gedeeltelijke betaling wordt uitgevoerd vóór de datum van de contantkorting. Klant 4027 heeft daarom een contantkorting van 3,00. Arnie registreert de betaling voor klant 4027 door het Betalingsjournaal te gebruiken. Arnie opent vervolgens de pagina **Transacties vereffenen**, zodat hij de factuur kan markeren voor vereffening.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10020 | 4027    | 6/25/2015 | 25/7/2015 | 10020   | 1.000,00                             | USD      | 297,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven. Als u de waarde **Te vereffenen bedrag** niet wijzigt in 297,00, verschillen de waarden **Contantkortingsbedrag**. Wanneer de betaling wordt geboekt, wordt echter 3,00 als contantkorting toegepast, omdat de vereffening automatisch de waarde **Bedrag om te vereffenen **corrigeert.

|                              |           |
|------------------------------|-----------|
| Datum voor contantkorting           | 09-07-2015 |
| Contantkortingsbedrag         | 10,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 3,00      |

Arnie boekt deze betaling. De factuur heeft nu een saldo van 700,00. De volgende transacties zijn zichtbaar voor de klant.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Factuur          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 700,00  | USD      |
| ARP-10020  |  Betaling         | 7/1/2015  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |  Contantkorting   | 7/1/2015  |         |                                      | 3,00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Resterende betaling na de contantkortingdatum
Op 11 juli (wat na de kortingsperiode is) betaalt klant 4027 de rest van de factuur. Op de pagina **Transacties vereffenen** verschijnt geen kortingsbedrag in het veld **Geraamde contantkorting** en de waarde in het veld **Contantkortingsbedrag** is **0,00** Wanneer klant 4027 de resterende 700,00 betaalt, wordt geen extra korting toegepast.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10020 | 4027    | 6/25/2015 | 25/7/2015 | 10020   | 700,00                               | USD      | 700,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 7/09/2015 |
| Contantkortingsbedrag         | 0,00      |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 3,00      |
| Contantkortingsbedrag dat moet worden toegepast | 0,00      |

Als Arnie de waarde in het veld **Contantkorting gebruiken** wijzigt in **Altijd**, wordt de instelling **Contantkortingen berekenen voor gedeeltelijke betalingen** overschreven en wordt de contantkorting toegepast. Het betalingsbedrag verandert in 693,00 en de contantkorting is de resterende 7,00.

| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Geselecteerd | Altijd            | FTI-10020 | 4027    | 6/25/2015 | 25/7/2015 | 10020   | 700,00                               |                                       | USD      | 693,00           |

Informatie over korting wordt onder aan de pagina **Openstaande transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 7/09/2015 |
| Contantkortingsbedrag         | 7,00      |
| Contantkorting gebruiken            | Altijd    |
| Toegepaste contantkorting          | 3,00      |
| Contantkortingsbedrag dat moet worden toegepast | 7,00      |

Arnie wijzigt de waarde in het veld **Contantkorting gebruiken** terug naar **Normaal**, omdat hij deze klant niet de resterende contantkorting van 7,00 laat nemen. Vervolgens boekt Arnie de betaling. Wanneer Arnie de pagina** Klanttransacties** opent, ziet hij dat de factuur een saldo van 0,00 heeft. Hij ziet ook dat er twee betalingen zijn. Eén betaling is voor 297,00 en heeft 3,00 contantkorting en de andere betaling is voor 700,00.

| Boekstuk    | Transactietype | Datum      | Factuur | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Factuur          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 7/1/2015  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |                  | 7/1/2015  |         |                                      | 3,00                                  | 0,00    | USD      |
| ARP-10021  |                  | 7/11/2015 |         |                                      | 700,00                                | 0,00    | USD      |






