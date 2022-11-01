---
title: Leveranciersbetalingen voor een gedeeltelijk bedrag
description: Soms wilt u een leverancier minder betalen dan het bedrag van een factuur. In dit artikel worden de verschillende opties beschreven om deze situatie te dekken.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: deb150e35a80cc4c49f46dfc55822625db83cbda
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715373"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Leveranciersbetalingen voor een gedeeltelijk bedrag

[!include [banner](../includes/banner.md)]

Soms wilt u een leverancier minder betalen dan het bedrag van een factuur. In dit artikel worden de verschillende opties beschreven om deze situatie te dekken. Over welke opties u beschikt, is afhankelijk van de behoeften en de configuratie van uw bedrijf. 

## <a name="cash-discount-amounts"></a>Contantkortingsbedragen

Een leverancier kan u een contantkorting geven als u een factuur vóór de vervaldatum betaalt. U voert bijvoorbeeld een factuur in voor 100,00 die een contantkorting van 2% biedt als de factuur binnen 10 dagen wordt betaald. De betalingstermijn is 30 dagen. Als een betalingsvoorstel de contantkorting gebruikt als criterium voor het selecteren van een factuur en als het voorstel op of vóór de datum voor de contantkorting wordt uitgevoerd, wordt de factuur geselecteerd voor betaling en wordt de betaling gemaakt voor 98,00. Een contantkorting kan ook worden uitgevoerd voor een eenmalige betaling die handmatig is gemaakt.

## <a name="partial-payments-with-cash-discounts"></a>Gedeeltelijke betalingen met contantkortingen
Wanneer u een gedeeltelijke betaling uitvoert, wilt u mogelijk een volgende gedeeltelijke betaling doen om de factuur volledig te vereffenen. Om een contantkorting voor een gedeeltelijke betaling aan te nemen, moet u de optie **Contantkortingen berekenen voor gedeeltelijke betalingen** instellen op **Ja** op de pagina **Leverancierparameters**. 

U kunt bijvoorbeeld een contantkorting van 2% krijgen als de factuur binnen 10 dagen na uitgifte wordt betaald. Er wordt een factuur voor 100,00 geboekt. Als u binnen 10 dagen 49,00 betaalt, voert u een debetbedrag van 49,00 in een betalingsjournaal in. Wanneer u de gedeeltelijke betaling vereffent op de pagina **Openstaande transacties vereffenen**, wordt **1,00** weergegeven in het veld **Contantkortingsbedrag dat moet worden toegepast**. 

> [!NOTE] 
> Als u een gedeeltelijke betaling invoert en het volledige factuurbedrag in het veld **Bedrag om te vereffenen** laat staan, wordt het veld **Contantkortingsbedrag dat moet worden toegepast** automatisch opnieuw berekend wanneer u de transacties boekt.

## <a name="credit-notes-with-cash-discounts"></a>Creditnota's met contantkortingen
U retourneert misschien enkele artikelen van een factuur en ontvangt een creditnota. Als een korting werd toegepast op de oorspronkelijke factuur, kunt u de waarde van de korting aftrekken en het juiste bedrag gerestitueerd krijgen. Als de optie **Contantkortingen berekenen voor creditnota's** is ingesteld op **Ja** op de pagina **Leveranciersparameters**, wordt de korting automatisch berekend voor de creditnota. 

U kunt bijvoorbeeld een contantkorting van 2% krijgen als de factuur binnen 10 dagen na uitgifte wordt betaald. Er wordt een factuur voor 100,00 geboekt. Als u de goederen retourneert en u een creditnota ontvangt, kunt u de creditnota voor het volledige bedrag van de oorspronkelijke factuur, 100,00, invoeren samen met de contantkorting van 2 procent die ook op de creditnota is gedefinieerd.  Wanneer u de creditnota op de pagina **Transacties vereffenen** weergeeft, wordt **98,00** weergegeven in het veld **Bedrag om te vereffenen** en wordt **-2,00** weergegeven in het veld **Contantkortingsbedrag**. Het kortingsbedrag wordt naar een contantkortingsrekening geboekt.

## <a name="overpaymentunderpayment-amounts"></a>Overbetalings-/onderbetalingsbedragen
U voert misschien een gedeeltelijke betaling uit, waarbij het bedrag dat nog moet worden vereffend heel klein is. De leveranciersfactuur is bijvoorbeeld voor 1000,00 en u betaalt 999,90. Als het resterende bedrag kleiner is dan het bedrag dat op de pagina **Leveranciersparameters** is opgegeven voor over- of onderbetalingen, wordt het verschil automatisch geboekt naar een overbetalings-/onderbetalingsgrootboekrekening.


Zie [Overzicht van leveranciersbetaling](../cash-bank-management/tasks/vendor-payment-overview.md) voor meer informatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
