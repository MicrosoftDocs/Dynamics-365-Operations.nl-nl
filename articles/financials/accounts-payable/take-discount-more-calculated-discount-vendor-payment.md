---
title: Een korting nemen die groter is dan de berekende korting voor een leveranciersbetaling
description: Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is. Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen.
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 08d7c4981aba7e7c092a6f21d3b63635e76437bf
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Een korting nemen die groter is dan de berekende korting voor een leveranciersbetaling

[!include[banner](../includes/banner.md)]


Dit artikel begeleidt u door een scenario waarbij een contantkorting voor een bedrag wordt toegepast die meer is dan de korting die oorspronkelijk op de factuur beschikbaar is. Dit scenario kan optreden als een organisatie een overeenkomst met de leverancier aangaat om een lager bedrag op de factuur te betalen. 

Leverancier 3051 laat Fabrikam een contantkorting van 4 procent nemen als een factuur wordt betaald binnen zeven dagen. Op 29 jnui voert April een factuur in voor 1000,00. De leverancier geeft April een korting van 60,00 in plaats van de standaardkorting van 40,00 die beschikbaar is voor de factuur. April registreert een eenmalige betaling door het Leveranciersbetalingsjournaal te gebruiken. Ze voert de leverancier voor de betaling in en opent vervolgens de pagina **Transacties vereffenen**. Ze ziet de factuur en wijzigt de waarde in het veld **Contantkortingsbedrag** naar **60,00**.
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



