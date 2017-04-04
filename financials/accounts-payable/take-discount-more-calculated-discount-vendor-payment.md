---
title: Een korting nemen die groter is dan de berekende korting voor een leveranciersbetaling
description: Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is. Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 22ba73681faa509a5144517163cc173a1267a534
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Een korting nemen die groter is dan de berekende korting voor een leveranciersbetaling

Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is. Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen. 

Leverancier 3051 laat Fabrikam een contantkorting van 4 procent nemen als een factuur wordt betaald binnen zeven dagen. Op 29 jnui voert April een factuur in voor 1000,00. De leverancier geeft April een korting van 60,00 in plaats van de standaardkorting van 40,00 die beschikbaar is voor de factuur. April registreert een eenmalige betaling door het Leveranciersbetalingsjournaal te gebruiken. Ze voert u de leverancier voor de betaling en opent vervolgens het **transacties vereffenen** pagina. Ze markeert de factuur en wijzigt de waarde in de **contantkortingsbedrag** veld **60,00**.
| Markeren     | Contantkorting gebruiken | Boekstuk   | Rekening | Datum      | Vervaldatum  | Factuur | Bedrag in transactievaluta | Valuta | Bedrag om te vereffenen |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Geselecteerd | Normaal            | Factuur-10040 | 3051    | 6/29/2015 | 7/29/2015 | 10040   | 1.000,00                       | USD      | 940,00           |

Informatie over korting wordt onder aan de pagina **Transacties vereffenen** weergegeven.
|                              |           |
|------------------------------|-----------|
| Datum van contantkorting           | 7/12/2015 |
| Contantkortingsbedrag         | 60,00     |
| Contantkorting gebruiken            | Normaal    |
| Toegepaste contantkorting          | 0,00      |
| Contantkortingsbedrag dat moet worden toegepast | 60,00     |

Vervolgens boekt April het betalingsjournaal. De factuur is volledig vereffend met een betaling van 940,00 en een korting van 60,00.


