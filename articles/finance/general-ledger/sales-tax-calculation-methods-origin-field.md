---
title: Btw-berekeningsmethoden in het veld Oorsprong
description: Dit artikel beschrijft de opties in het veld Oorsprong op de btw-codespagina en hoe de btw op basis van de geselecteerde optie voor een btw-code wordt berekend.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e57e97847c6aa7a775b0f2639dff93f1e3a9e7a2
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189368"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Btw-berekeningsmethoden in het veld Oorsprong

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft de opties in het veld Oorsprong op de btw-codespagina en hoe de btw op basis van de geselecteerde optie voor een btw-code wordt berekend.

Voor elke btw-code die u in de pagina Btw-codes maakt, selecteert u welke berekeningsmethode moet worden toegepast op het btw-basisbedrag in het veld Oorsprong.

## <a name="percentage-of-net-amount"></a>Percentage van nettobedrag
Het berekeningsmethode Percentage van nettobedrag is de standaardwaarde in het veld Oorsprong. De btw wordt berekend als een percentage van het aankoop- of verkoopbedrag, exclusief eventuele andere btw.
### <a name="example"></a>Voorbeeld

Het btw-tarief is 25%. De factuurregel bevat een hoeveelheid van 10 artikelen voor € 1,00 per stuk en de klant heeft recht op een regelkorting van 10%. Nettobedrag: (10 x 1,00) -10% = 9,00 Btw: 9,00 x 25% = 2,25 Totaalbedrag: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Percentage van brutobedrag
Als u de methode Percentage van brutobedrag selecteert, wordt de btw berekend als een percentage van het brutoverkoopbedrag. Het brutobedrag is het regelnettobedrag plus alle belastingen en bijzondere kosten voor de regel behalve de ene belasting met Oorsprong = Percentage van brutobedrag.
### <a name="example"></a>Voorbeeld

De belastingdienst heeft een artikel met speciale heffingen belast. De heffingsbedragen worden toegevoegd aan het nettobedrag voordat de btw wordt berekend. Uitgaande van de volgende btw-codes:
-   HEFFING 1 = 10%, met de berekeningsmethode Percentage van nettobedrag
-   HEFFING 2 = 20%, met de berekeningsmethode Percentage van nettobedrag
-   BTW = 25%, met de berekeningsmethode Percentage van brutobedrag

Is het nettobedrag 10,00, dan HEFFING 1 = 1,00 (10,00 x 10%) en HEFFING 2 = 2,00 (10,00 x 20%). De bedragen zijn als volgt: Brutobedrag: nettobedrag + HEFFING 1 bedrag + HEFFING 2 bedrag (10,00 + 1,00 + 2,00) = 13,00 BTW = 13,00 x 25% = 3,25 Totaal HEFFINGEN en BTW: 1,00 + 2,00 + 3,25 = 6,25 Totaalbedrag: 10,00 + 6,25 = 16,25

| **Opmerking**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Slechts één btw-code met Oorsprong = Percentage van brutobedrag kan voor een transactie worden gebruikt. Als meerdere dergelijke btw-codes voor een transactie worden gedefinieerd wordt een fout weergegeven dat de btw niet kan worden berekend. |


## <a name="percentage-of-sales-tax"></a>Btw-percentage

Als u Btw-percentage selecteert in het veld Oorsprong, wordt de btw berekend als het percentage van de btw dat is geselecteerd in het veld Btw op btw. De btw die in het veld Btw op btw is geselecteerd, wordt eerst berekend. De tweede btw wordt berekend op basis van het eerste btw-bedrag.
### <a name="example"></a>Voorbeeld

Uitgaande van de volgende btw-codes:
-   HEFFING 1 = 10%, met de methode Percentage van nettobedrag
-   HEFFING 2 = 20%, waarbij de methode Btw-percentage is gebruikt, met Heffing 1 in het veld Btw op btw
-   BTW = 25%, met de methode Percentage van brutobedrag

Nettobedrag: 10,00 HEFFING 1: 10,00 x 10% = 1,00 HEFFING 2: 1,00 x 20% = 0,20 Brutobedrag: 10,00 + 1,00 + 0,20 = 11,20 BTW: 11,20 x 25% = 2,80 Totaal HEFFINGEN en BTW: 1,00 + 0,20 + 2,80 = 4,00 Totaalbedrag: 10,00 + 4,00 = 14,00

| **Opmerking**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Belasting op meerdere niveaus in belastingberekeningen is niet mogelijk. Een belasting kan niet worden berekend op basis van een belasting die al op basis van een andere belasting wordt berekend. Er kunnen meerdere één-niveau-belastingen op btw-codes worden berekend voor een transactie. |

## <a name="amount-per-unit"></a> Bedrag per eenheid
Wanneer u Bedrag per eenheid in het veld Oorsprong selecteert, wordt de btw als vast bedrag per eenheid berekend, vermenigvuldigd met de hoeveelheid die op de documentregel wordt ingevoerd. De eenheid moet worden geselecteerd in het veld Eenheid. Het bedrag per eenheid wordt opgegeven in de pagina Waarden btw-code.
### <a name="example"></a>Voorbeeld

Btw-code is ingesteld als: USD 1,20 per eenheid = doos Op een verkoopfactuurregel worden 25 dozen van een artikel verkocht Btw wordt berekend als 25 x 1,20 = 30,00

| **Opmerking**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Als de transactie in een andere eenheid wordt ingevoerd dan de eenheid die is opgegeven voor de btw-code, wordt deze automatisch omgezet op basis van de eenheidsomrekeningen die in de pagina Eenheidsomrekeningen zijn ingesteld. |

###  <a name="amount-per-unit-additional-option"></a> Bedrag per eenheid, extra optie

Op het tabblad Berekening kunt u selecteren of een als bedrag per eenheid berekende btw wordt berekend vóór andere btw-codes en opgeteld bij het nettobedrag voordat andere btw-codes met Oorsprong = Percentage van nettobedrag worden berekend.

### <a name="examples"></a>Voorbeelden

Stel we berekenen 2 btw-codes voor een transactie:

-   HEFFING: Oorsprong = Bedrag per eenheid en een btw, de waarde is ingesteld op 5,00 per eenheid = stks
-   BTW: Oorsprong = als getoond in de onderstaande voorbeelden, de waarde is ingesteld op 25%

We verkopen 1 stuks van een artikel met een eenheidsprijs van 10,00
#### <a name="example-1"></a>Voorbeeld 1

BTW: Oorsprong = methode Percentage van brutobedrag De optie Berekenen vóór btw heeft geen invloed, omdat BTW wordt berekend als een percentage van het brutobedrag. HEFFING: 1 x 5,00 = 5,00 Brutobedrag: 10,00 + 5,00 = 15,00 BTW: 15,00 x 25% = 3,75 Totaal btw: 5,00 + 3,75 = 8,75 Totaal bedrag: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Voorbeeld 2

BTW: Oorsprong = Percentage van nettobedrag De optie Berekenen vóór btw is niet geselecteerd voor de HEFFING-berekening. Nettobedrag: 10,00 HEFFING: 1 x 5,00 = 5,00 BTW: 10,00 x 25% = 2,50 Totale btw: 5,00 + 2,50 = 7,50 Totaal bedrag: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Voorbeeld 3

BTW: Oorsprong = Percentage van nettobedrag De optie Berekenen vóór btw is geselecteerd voor de HEFFING-berekening. Nettobedrag: 10,00 HEFFING: 1 x 5,00 = 5,00 BTW: (10,00 + 5,00) x 25% = 3,75 Totale btw: 5,00 + 3,75 = 8,75 Totaal bedrag: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Voorbeeld 4

Het resultaat van voorbeeld 1 en 3 is gelijk, omdat er slechts één heffing wordt gebruikt. Stel dat u twee HEFFINGEN hebt en dat slechts één is opgenomen in het nettobedrag voor de btw-berekening: HEFFING 1: 5,00, met de methode Bedrag per eenheid, en de optie Berekenen vóór btw is geselecteerd HEFFING 2: 2,50, met de methode Bedrag per eenheid, en de optie Berekenen vóór btw is niet geselecteerd Btw: 25%, met de methode Percentage van nettobedrag Nettobedrag: 10,00 HEFFING 1: 1 x 5,00 = 5,00 HEFFING 2: 1 x 2,50 = 2,50 Nettobedrag onderhevig aan btw: 10,00 + 5,00 = 15,00 BTW: 15,00 x 25% = 3,75 Totale btw, inclusief heffingen: 5,00 + 2,50 + 3,75 = 11,25 Totaal bedrag: 10,00 + 11,25 = 21,25 De 25% BTW wordt berekend voor de som van het nettobedrag (10,00) + HEFFING 1 (5,00) = 15,00. HEFFING 2 wordt aan het btw-bedrag toegevoegd nadat de btw is berekend.

## <a name="calculated-percentage-of-net-amount"></a> Berekende percentage van het nettobedrag
Het berekende percentage van het nettobedrag verwerkt de btw-berekening verschillend, afhankelijk van de instelling van de parameter Bedragen inclusief BTW voor het document of journaal.
### <a name="example-1"></a>Voorbeeld 1

Document / journaal is ingesteld op Bedragen inclusief BTW = Ja Transactieregelbedrag: 10,00 Btw-tarief: 25% BTW: Transactieregelbedrag x btw-tarief (10,00 x 25%) = 2,50 Basisbedrag belasting (oorsprongbedrag): Transactieregelbedrag - Btw (10,00 - 2,50) = 7,50

### <a name="example-2"></a>Voorbeeld 2

Document / journaal is ingesteld op Bedragen inclusief BTW = Nee Transactieregelbedrag: 10,00 Btw-tarief: 25% BTW: (Transactieregelbedrag x btw-tarief) / (100 - btw-tarief) (10,00 x 25%) / (100% - 25%) = 3,33 Basisbedrag belasting (oorsprongbedrag): Transactieregelbedrag = 10,00



## <a name="additional-resources"></a>Aanvullende resources

[Btw-tarieven op basis van Marginale basis en Berekeningsmethoden](marginal-base-field.md)

[Berekeningsopties Volledige bedrag en interval voor btw-codes](whole-amount-interval-options-sales-tax-codes.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]