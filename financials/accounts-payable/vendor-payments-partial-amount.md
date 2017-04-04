---
title: Leveranciersbetalingen voor een gedeeltelijk bedrag
description: Soms wilt u een leverancier minder betalen dan het bedrag van een factuur. In dit artikel worden de verschillende opties beschreven om deze situatie te dekken. Over welke opties u beschikt, is afhankelijk van de behoeften en de configuratie van uw bedrijf.
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
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Leveranciersbetalingen voor een gedeeltelijk bedrag

Soms wilt u een leverancier minder betalen dan het bedrag van een factuur. In dit artikel worden de verschillende opties beschreven om deze situatie te dekken. Over welke opties u beschikt, is afhankelijk van de behoeften en de configuratie van uw bedrijf. 

<a name="cash-discount-amounts"></a>Contantkortingsbedragen
---------------------

Een leverancier kan u een contantkorting geven als u een factuur vóór de vervaldatum betaalt. U voert bijvoorbeeld een factuur in voor 100,00 die een contantkorting van 2% biedt als de factuur binnen 10 dagen wordt betaald. De betalingstermijn is 30 dagen. Als u een betalingsvoorstel wordt de korting voor contante betaling gebruikt als criterium voor het selecteren van een factuur en als het voorstel wordt uitgevoerd op of vóór de kortingsdatum, de factuur voor de betaling is geselecteerd en wordt de betaling van 98,00 gemaakt. Een korting voor contante betaling kan ook worden opgehaald voor een eenmalige betaling die handmatig is gemaakt.

## <a name="partial-payments-with-cash-discounts"></a>Gedeeltelijke betalingen met contantkortingen
Wanneer u een gedeeltelijke betaling uitvoert, wilt u mogelijk een volgende gedeeltelijke betaling doen om de factuur volledig te vereffenen. Als u een korting voor contante betaling voor een gedeeltelijke betaling, moet u instellen dat de ** contantkortingen berekenen voor gedeeltelijke betalingen ** optie aan **Ja** op de **leveranciersparameters rekening** pagina. 

U kunt bijvoorbeeld een contantkorting van 2% krijgen als de factuur binnen 10 dagen na uitgifte wordt betaald. Er wordt een factuur voor 100,00 geboekt. Als u binnen 10 dagen een betaling van 49,00, moet u een debetbedrag van 49,00 in een betalingsjournaal invoeren. Wanneer u de gedeeltelijke betaling vereffenen op de **openstaande transacties vereffenen** pagina **1,00** wordt weergegeven in de **kortingsbedrag voor contante betaling te nemen** veld. 

> [!NOTE] 
> Als u een gedeeltelijke betaling invoert en laat u het volledige factuurbedrag in de **te vereffenen bedrag** veld, de **kortingsbedrag voor contante betaling te nemen** veld wordt automatisch opnieuw berekend wanneer u de transacties boeken.

## <a name="credit-notes-with-cash-discounts"></a>Creditnota's met contantkortingen
U retourneert misschien enkele artikelen van een factuur en ontvangt een creditnota. Als een korting werd toegepast op de oorspronkelijke factuur, kunt u de waarde van de korting aftrekken en het juiste bedrag gerestitueerd krijgen. Als de ** contantkortingen voor creditnota's berekenen ** optie is ingesteld op **Ja** op de **leverancierparameters** pagina, de korting automatisch berekend voor de creditnota. 

U kunt bijvoorbeeld een contantkorting van 2% krijgen als de factuur binnen 10 dagen na uitgifte wordt betaald. Er wordt een factuur voor 100,00 geboekt. Als u de goederen retourneert en een creditnota ontvangt, kunt u de creditnota invoeren voor het volledige bedrag van de oorspronkelijke factuur, 100,00, samen met de contantkorting van 2 procent die ook op de creditnota is gedefinieerd.  Wanneer u de creditnota bekijken op de **transacties vereffenen** pagina **98,00** wordt weergegeven in de **te vereffenen bedrag** veld en **-2.00** wordt weergegeven in de **contantkortingsbedrag** veld. Het kortingsbedrag wordt naar een contantkortingsrekening geboekt.

## <a name="overpaymentunderpayment-amounts"></a>Overbetalings-/onderbetalingsbedragen
U voert misschien een gedeeltelijke betaling uit, waarbij het bedrag dat nog moet worden vereffend heel klein is. De leveranciersfactuur is bijvoorbeeld voor 1000,00 en u betaalt 999,90. Als het resterende bedrag kleiner is dan het bedrag dat op de pagina **Leveranciersparameters** is opgegeven voor over- of onderbetalingen, wordt het verschil automatisch geboekt naar een overbetalings-/onderbetalingsgrootboekrekening.


