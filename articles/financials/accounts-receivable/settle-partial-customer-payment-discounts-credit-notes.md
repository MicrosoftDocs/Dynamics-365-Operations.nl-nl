---
title: Een gedeeltelijke klantenbetaling vereffenen met kortingen op creditnota's
description: Dit artikel begeleidt u door een scenario waarbij een contantkorting op een creditnota wordt genomen wanneer de oorspronkelijke factuur ook een contantkorting had.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa641f996d1ee516f588fcd1520bdc23d5d25f86
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561101"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Een gedeeltelijke klantenbetaling vereffenen met kortingen op creditnota's

[!include [banner](../includes/banner.md)]

Dit artikel begeleidt u door een scenario waarbij een contantkorting op een creditnota wordt genomen wanneer de oorspronkelijke factuur ook een contantkorting had. 

Fabrikam stelt klanten in staat om contantkortingen te nemen op gedeeltelijke betalingen en ook op creditnota's. Een contantkorting kan op een creditnota worden toegepast wanneer de creditnota is uitgegeven voor een factuur waarvoor de klant een contantkorting heeft genomen. In plaats van een creditering te verlenen voor het gehele bedrag, kunt u het saldo van de klant crediteren voor een bedrag dat het contantkortingspercentage uitsluit dat de klant heeft genomen. De vereffeningparameters bevinden zich op de pagina **Leveranciersparameters**.

## <a name="invoice-and-credit-note"></a>Factuur en creditnota
Klant 4035 heeft een factuur voor 1.000,00 en een creditnota voor 100,00. Elk document heeft een korting van 1 procent als het binnen 14 dagen wordt betaald. Arnie kan deze informatie bekijken op de pagina **Klanttransacties**.

| Boekstuk    | Transactietype | Datum      | Factuur  | Debetbedrag in transactievaluta | Creditbedrag in transactievaluta | Saldo  | Valuta |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Factuur          | 6/28/2015 | 10050    | 1.000,00                             |                                       | 1.000,00 | EUR      |
| CCRN-10050 | Creditnota      | 6/28/2015 | CR-10050 |                                      | 100,00                                | -100,00  | EUR      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Een creditnota met een factuur vereffenen
Vanaf de pagina **Klanttransacties** opent Arnie de pagina **Transacties vereffenen**. Hij kan de pagina **Transacties vereffenen** gebruiken om de factuur en de creditnota te vereffenen. Als onderdeel van het vereffeningsproces, bekijkt hij de datums en bedragen voor de contantkorting. Hij markeert de twee documenten en klikt vervolgens op **Boeken** om de transacties te vereffenen. Er is een korting van -1.00 op de creditnota omdat Fabrikam kortingen toestaat op creditnota's.

| Markeren     | Contantkorting gebruiken | Boekstuk    | Rekening | Datum      | Vervaldatum  | Factuur  | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | FTI-10050  | 4035    | 6/28/2015 | 7/28/2015 | 10050    | 1.000,00                       | EUR      | 990,00           |
| Geselecteerd | Normaal            | CCRN-10050 | 4035    | 6/28/2015 | 7/28/2015 | CR-10050 | -100,00                        | EUR      | -99,00           |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven.

|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 7/12/2015 |
| Contantkortingsbedrag         | -1,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | -1,00     |

De vereffening is 100,00 en omvat een betaling van 99,00 en een korting van 1,00.



