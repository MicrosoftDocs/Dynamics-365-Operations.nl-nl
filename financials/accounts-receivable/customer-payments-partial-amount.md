---
title: Klantbetalingen voor een gedeeltelijk bedrag
description: Soms voeren klanten een betaling uit die minder is dan het bedrag van een factuur. In dit artikel worden de verschillende opties beschreven om deze situatie te dekken. Over welke opties u beschikt, is afhankelijk van de behoeften en de configuratie van uw bedrijf.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 7025072cd29aac4ceb13b5594c3e321350777cf1
ms.lasthandoff: 03/31/2017


---

# <a name="customer-payments-for-a-partial-amount"></a>Klantbetalingen voor een gedeeltelijk bedrag

Soms voeren klanten een betaling uit die minder is dan het bedrag van een factuur. In dit artikel worden de verschillende opties beschreven om deze situatie te dekken. Over welke opties u beschikt, is afhankelijk van de behoeften en de configuratie van uw bedrijf.

<a name="partial-payment-with-no-discount"></a>Gedeeltelijke betaling zonder korting
--------------------------------

Klanten kan een gedeeltelijke betaling doen omdat ze niet genoeg contant geld bij hebben om de factuur volledig te betalen of omdat er een geschil is over een artikel op de factuur. In deze situatie kan de factuur gedeeltelijk met de betaling worden vereffend. De factuur blijft open en er wordt een saldo weergeven.

## <a name="discount-amounts"></a>Kortingsbedragen
U kunt klanten een contantkorting geven als ze een factuur vóór de vervaldatum betalen. U voert bijvoorbeeld een factuur in voor 100,00 die een contantkorting van 2% biedt als de factuur binnen 10 dagen wordt betaald. De betalingstermijn is 30 dagen. Als u binnen 10 dagen een betaling van 98,00 ontvangt, voert u de betaling van 98,00 in. Wanneer de factuur vervolgens voor vereffening is gemarkeerd, wordt de contantkorting automatisch toegepast.

## <a name="partial-payments-with-cash-discounts"></a>Gedeeltelijke betalingen met contantkortingen
Wanneer klanten een gedeeltelijke betaling doen, willen ze mogelijk een volgende gedeeltelijke betaling doen om de factuur volledig te vereffenen. Als u een korting voor contante betaling voor een gedeeltelijke betaling, moet u instellen dat de ** contantkortingen berekenen voor gedeeltelijke betalingen ** optie naar **Ja** op de **parameters van module klanten** pagina. 

U kunt bijvoorbeeld een contantkorting van 2% aanbieden als de factuur binnen 10 dagen na uitgifte wordt betaald. Er wordt een factuur voor 100,00 geboekt. Als u binnen 10 dagen een betaling van 49,00 ontvangt, voert u een krediet van 49,00 in een betalingsjournaal in. Wanneer u de gedeeltelijke betaling vereffent op de pagina **Transacties vereffenen**, wordt **1,00** weergegeven in het veld **Contantkortingsbedrag dat moet worden toegepast**. Het kortingsbedrag wordt naar een contantkortingsrekening geboekt. 

> [!NOTE] 
> Als u een gedeeltelijke betaling invoert en laat u het volledige factuurbedrag in de **te vereffenen bedrag** veld, de **kortingsbedrag voor contante betaling te nemen** veld wordt automatisch opnieuw berekend wanneer u de transacties boeken.

## <a name="credit-notes-with-discounts"></a>Creditnota's met kortingen
Als klanten enkele artikelen van een factuur retourneren, schrijft u een creditnota uit. Als er een contantkorting op de oorspronkelijke factuur werd genomen, moet de creditnota aan de klant het nettobedrag van de contantkorting zijn die door de klant is opgenomen. Als de optie **Contantkortingen berekenen voor creditnota's** is ingesteld op **Ja** op de pagina **Parameters van module Klanten**, wordt de korting automatisch berekend voor de creditnota. 

U bood bijvoorbeeld betalingsvoorwaarden aan waarbij een korting van 2% werd gegeven als de factuur binnen 10 dagen na uitgifte werd betaald. Een factuur voor 100,00 werd geboekt en de klant nam de contantkorting. Als de klant de goederen retourneert en u een creditnota uitschrijft, kunt u op de creditnota -100,00 invoeren . Wanneer u de creditnota op de pagina **Openstaande transacties vereffenen** weergeeft, wordt** 98,00** weergegeven in het veld **Bedrag om te vereffenen** en wordt **-2,00** weergegeven in het veld **Contantkortingsbedrag**. Het kortingsbedrag wordt naar een contantkortingsrekening geboekt.

## <a name="overpaymentunderpayment-amounts"></a>Overbetalings-/onderbetalingsbedragen
Wanneer klanten een betaling uitvoeren, kan er een heel klein bedrag zijn dat nog moet worden vereffend. U factureert de klant bijvoorbeeld voor 1000,00 en de klant betaalt 999,90. Als het resterende bedrag kleiner is dan het bedrag dat op de pagina** Parameters van module Klanten** is opgegeven voor over- of onderbetalingen, wordt het verschil automatisch geboekt naar een overbetalings-/onderbetalingsgrootboekrekening.

## <a name="full-settlement"></a>Volledige vereffening
Klanten doet een gedeeltelijke betaling waar het restbedrag won't worden betaald, maar groter is dan het bedrag te weinig betaald bedrag dat is opgegeven op de **parameters van leveranciers rekening** pagina. Als u markeren van de factuur als volledig vereffend wilt, kunt u de **volledige vereffening** optie op de **transactie vereffenen** pagina. (U kunt de functionaliteit voor volledige vereffening inschakelen door een configuratiesleutel te gebruiken.) Een factuur wordt bijvoorbeeld geboekt voor 1000,00, en de klant voert een betaling van 990,00 uit. U bent overeengekomen dat de klant betaalt de resterende 10,00 geen. Nadat u de factuur voor vereffening markeren, kunt u ook markeren select **volledige vereffening**. De factuur wordt dan beschouwd als volledig vereffend. Het verschil van 10,00 wordt als een extra kortingsbedrag geboekt naar een contantkortingsrekening.


