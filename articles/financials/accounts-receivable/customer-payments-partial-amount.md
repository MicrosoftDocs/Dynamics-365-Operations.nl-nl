---
title: Klantbetalingen voor een gedeeltelijk bedrag
description: Soms voeren klanten een betaling uit die minder is dan het bedrag van een factuur. In dit artikel worden de verschillende opties beschreven om deze situatie te dekken. Over welke opties u beschikt, is afhankelijk van de behoeften en de configuratie van uw bedrijf.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymEntry
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 6b7494a05392cbee70e6d5883bae0295e8b55ac9
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="customer-payments-for-a-partial-amount"></a>Klantbetalingen voor een gedeeltelijk bedrag

[!include[banner](../includes/banner.md)]


Soms voeren klanten een betaling uit die minder is dan het bedrag van een factuur. In dit artikel worden de verschillende opties beschreven om deze situatie te dekken. Over welke opties u beschikt, is afhankelijk van de behoeften en de configuratie van uw bedrijf.

<a name="partial-payment-with-no-discount"></a>Gedeeltelijke betaling zonder korting
--------------------------------

Klanten kan een gedeeltelijke betaling doen omdat ze niet genoeg contant geld bij hebben om de factuur volledig te betalen of omdat er een geschil is over een artikel op de factuur. In deze situatie kan de factuur gedeeltelijk met de betaling worden vereffend. De factuur blijft open en er wordt een saldo weergeven.

## <a name="discount-amounts"></a>Kortingsbedragen
U kunt klanten een contantkorting geven als ze een factuur vóór de vervaldatum betalen. U voert bijvoorbeeld een factuur in voor 100,00 die een contantkorting van 2% biedt als de factuur binnen 10 dagen wordt betaald. De betalingstermijn is 30 dagen. Als u binnen 10 dagen een betaling van 98,00 ontvangt, voert u de betaling van 98,00 in. Wanneer de factuur vervolgens voor vereffening is gemarkeerd, wordt de contantkorting automatisch toegepast.

## <a name="partial-payments-with-cash-discounts"></a>Gedeeltelijke betalingen met contantkortingen
Wanneer klanten een gedeeltelijke betaling doen, willen ze mogelijk een volgende gedeeltelijke betaling doen om de factuur volledig te vereffenen. Om een contantkorting voor een gedeeltelijke betaling aan te nemen, moet u de optie **Contantkortingen berekenen voor gedeeltelijke betalingen** instellen op **Ja** op de pagina **Parameters van module Klanten**. 

U kunt bijvoorbeeld een contantkorting van 2% aanbieden als de factuur binnen 10 dagen na uitgifte wordt betaald. Er wordt een factuur voor 100,00 geboekt. Als u binnen 10 dagen een betaling van 49,00 ontvangt, voert u een krediet van 49,00 in een betalingsjournaal in. Wanneer u de gedeeltelijke betaling vereffent op de pagina **Transacties vereffenen**, wordt **1,00** weergegeven in het veld **Contantkortingsbedrag dat moet worden toegepast**. Het kortingsbedrag wordt naar een contantkortingsrekening geboekt. 

> [!NOTE] 
> Als u een gedeeltelijke betaling invoert en het volledige factuurbedrag in het veld **Bedrag om te vereffenen** laat staan, wordt het veld **Contantkortingsbedrag dat moet worden toegepast** automatisch opnieuw berekend wanneer u de transacties boekt.

## <a name="credit-notes-with-discounts"></a>Creditnota's met kortingen
Als klanten enkele artikelen van een factuur retourneren, schrijft u een creditnota uit. Als er een contantkorting op de oorspronkelijke factuur werd genomen, moet de creditnota aan de klant het nettobedrag van de contantkorting zijn die door de klant is opgenomen. Als de optie **Contantkortingen berekenen voor creditnota's** is ingesteld op **Ja** op de pagina **Parameters van module Klanten**, wordt de korting automatisch berekend voor de creditnota. 

U bood bijvoorbeeld betalingsvoorwaarden aan waarbij een korting van 2% werd gegeven als de factuur binnen 10 dagen na uitgifte werd betaald. Een factuur voor 100,00 werd geboekt en de klant nam de contantkorting. Als de klant de goederen retourneert en u een creditnota uitschrijft, kunt u op de creditnota -100,00 invoeren . Wanneer u de creditnota op de pagina **Openstaande transacties vereffenen** weergeeft, wordt **98,00** weergegeven in het veld **Bedrag om te vereffenen** en wordt **-2,00** weergegeven in het veld **Contantkortingsbedrag**. Het kortingsbedrag wordt naar een contantkortingsrekening geboekt.

## <a name="overpaymentunderpayment-amounts"></a>Overbetalings-/onderbetalingsbedragen
Wanneer klanten een betaling uitvoeren, kan er een heel klein bedrag zijn dat nog moet worden vereffend. U factureert de klant bijvoorbeeld voor 1000,00 en de klant betaalt 999,90. Als het resterende bedrag kleiner is dan het bedrag dat op de pagina **Parameters van module Klanten** is opgegeven voor over- of onderbetalingen, wordt het verschil automatisch geboekt naar een overbetalings-/onderbetalingsgrootboekrekening.

## <a name="full-settlement"></a>Volledige vereffening
Klanten doen een gedeeltelijke betaling waarbij het restbedrag niet wordt betaald, maar groter is dan het bedrag dat te weinig is betaald, dat is opgegeven op de pagina **Parameters van module Leveranciers**. Als u de factuur als volledig vereffend wilt markeren, kunt u de optie **Volledige vereffening** op de pagina **Transactie vereffenen** gebruiken. (U kunt de functionaliteit voor volledige vereffening inschakelen door een configuratiesleutel te gebruiken.) Een factuur wordt bijvoorbeeld geboekt voor 1000,00, en de klant voert een betaling van 990,00 uit. U bent overeengekomen dat de klant de rest van 10,00 niet hoeft te betalen. Nadat u de factuur voor vereffening hebt gemarkeerd, kunt u ook **Volledige vereffening** selecteren. De factuur wordt dan beschouwd als volledig vereffend. Het verschil van 10,00 wordt als een extra kortingsbedrag geboekt naar een contantkortingsrekening.


Zie [Klantbetalingen storten](tasks/deposit-customer-payments.md) voor meer informatie.

