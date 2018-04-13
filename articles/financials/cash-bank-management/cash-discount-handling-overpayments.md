---
title: Contantkorting voor te veel bedraagde betalingen verwerken
description: Dit artikel biedt scenario's die laten zien hoe een betaling wordt uitgevoerd wanneer de klant een contantkorting neemt maar ook te veel betaalt.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b664ad6d084c5437111149266a859d7157b22ee9
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="handling-cash-discounts-for-overpayments"></a>Contantkorting voor te veel bedraagde betalingen verwerken

[!INCLUDE [banner](../includes/banner.md)]

Dit artikel biedt scenario's die laten zien hoe een betaling wordt uitgevoerd wanneer de klant een contantkorting neemt maar ook te veel betaalt. 

Een factuur wordt beschouwd als overbetaald wanneer het betaalde bedrag hoger is dan het factuurbedrag minus de contantkorting. Om te specificeren hoe een verschil in mogelijke contantkorting wordt behandeld wanneer te veel wordt betaald voor een factuur, gebruikt u de velden **Administratie voor contantkorting** en **Max. te veel/te weinig betaald bedrag** op de pagina **Parameters van module Klanten**. In het volgende voorbeeld heeft de klant de factuur met €0,50 teveel betaald.

| Factuurtotaal | Beschikbare contantkorting | Te betalen bedrag na aftrek van de contantkorting | Het bedrag dat de klant betaalt |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | EUR 10,50                   | EUR 94,50                                               | EUR 95,00                             |

## <a name="cash-discount-administration--specific"></a>Administratie voor contantkorting = Specifiek
Wanneer **Specifiek** is geselecteerd in het veld **Administratie voor contantkorting** op de pagina **Rekeningen voor automatische transacties**, wordt de volledige contantkorting opgehaald. Het overbetalingsbedrag wordt geboekt naar een grootboekrekening voor contantkortingsverschillen of het wordt saldo op de klantrekening. Het gedrag is afhankelijk van de vraag of het overbetalingsbedrag ligt tussen 0,00 en het bedrag dat is ingevoerd in het veld **Max. te veel/te weinig betaald bedrag**, of dat het overbetalingsbedrag meer is dan het bedrag van **Max. te veel/te weinig betaald bedrag**.

### <a name="scenario-1"></a>Scenario 1

In dit scenario ligt het overbetalingsbedrag tussen 0,00 en de maximale overbetaling of onderbetaling. Een factuur voor 105,00 is ingevoerd en een contantkorting is beschikbaar als de factuur binnen zeven dagen wordt betaald.

| Factuurtotaal | Beschikbare contantkorting | Te betalen bedrag na aftrek van de contantkorting |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | EUR 10,50                   | EUR 94,50                                               |

De klant voert een betaling van 95,00 uit in de periode van contantkorting. De betaling wordt vereffend met de factuur voor €105,00. Nadat de factuur en de betaling zijn vereffend, worden voor de klant de volgende transacties uitgevoerd in Klanten.

| Transactie   | Bedrag | Saldo |
|---------------|--------|---------|
| Factuur       | 105,00 | 0,00    |
| Betaling       | €-95.00 | 0,00    |
| Contantkorting | €-10,50 | 0,00    |

De volgende boekhoudvermeldingen worden gegenereerd voor de betaling en de vereffening. **Betaling**

| Rekening             | Debetbedrag | Creditbedrag |
|---------------------|--------------|---------------|
| Contant                | EUR 95,00        |               |
| Klanten |              | EUR 95,00         |

**Vereffening**

| Rekening                                                                                                          | Debetbedrag | Creditbedrag |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Contantkorting (het veld **Hoofdrekening voor klantkortingen** op de pagina **Contantkortingen**)                 | EUR 10,50        |               |
| Klanten                                                                                              |              | EUR 10,50         |
| Contantkorting van klant (het veld **Contantkorting van klant** op de pagina **Rekening voor automatische transacties**) |              | 0,50          |
| Klanten                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>Scenario 2

In dit scenario overschrijdt het overbetalingsbedrag de maximale overbetaling of onderbetaling. Een factuur voor 105,00 is ingevoerd en een contantkorting is beschikbaar als de factuur binnen zeven dagen wordt betaald.

| Factuurtotaal | Beschikbare contantkorting | Te betalen bedrag na aftrek van de contantkorting |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | EUR 10,50                   | EUR 94,50                                               |

De klant voert een betaling van 95,00 uit in de periode van contantkorting. De betaling wordt vereffend met de factuur voor €105,00. Nadat de factuur en de betaling zijn vereffend, worden voor de klant de volgende transacties uitgevoerd in Klanten.

| Transactie   | Bedrag | Saldo |
|---------------|--------|---------|
| Factuur       | 105,00 | 0,00    |
| Betaling       | €-95.00 | €-0,50   |
| Contantkorting | €-10,50 | 0,00    |

Het overbetalingsbedrag van €0,50 wordt als saldo op de betaling weergegeven en kan op een andere factuur worden vereffend. De volgende boekhoudvermeldingen worden gegenereerd voor de betaling en de vereffening. **Betaling**

| Rekening             | Debetbedrag | Creditbedrag |
|---------------------|--------------|---------------|
| Contant                | EUR 95,00        |               |
| Klanten |              | EUR 95,00         |

**Vereffening**

| Rekening                                                                                          | Debetbedrag | Creditbedrag |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Contantkorting (het veld **Hoofdrekening voor klantkortingen** op de pagina **Contantkortingen**) | EUR 10,50        |               |
| Klanten                                                                              |              | EUR 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Administratie voor contantkorting = Flexibel
Wanneer **Flexibel** is geselecteerd in het veld **Administratie voor contantkorting** op de pagina **Rekeningen voor automatische transacties**, wordt de bedrag van de contantkorting verminderd met het bedrag van de overbetaling. Dit gedrag is altijd van toepassing, ongeacht of het overbetalingsbedrag meer of minder is dan het bedrag dat is in gevoerd in het veld **Max. te veel/te weinig betaald bedrag**.

### <a name="scenario-3"></a>Scenario 3

In dit scenario wordt een factuur voor 105,00 ingevoerd en is een contantkorting beschikbaar als de factuur binnen zeven dagen wordt betaald.

| Factuurtotaal | Beschikbare contantkorting | Te betalen bedrag na aftrek van de contantkorting |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | EUR 10,50                   | EUR 94,50                                               |

De klant voert een betaling van 95,00 uit in de datum van de contantkorting. De betaling wordt vereffend met de factuur voor €105,00. Nadat de factuur en de betaling zijn vereffend, worden voor de klant de volgende transacties uitgevoerd in Klanten.

| Transactie   | Bedrag | Saldo |
|---------------|--------|---------|
| Factuur       | 105,00 | 0,00    |
| Betaling       | €-95.00 | €-0,00   |
| Contantkorting | -10,00 | 0,00    |

Het contantkortingsbedrag wordt verminderd van €10,50 tot €10,00. De betaling en de factuur worden beschouwd als vereffend. **Betaling**

| Rekening             | Debetbedrag | Creditbedrag |
|---------------------|--------------|---------------|
| Contant                | EUR 95,00        |               |
| Klanten |              | EUR 95,00         |

**Vereffening**

| Rekening                                                                                          | Debetbedrag | Creditbedrag |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Contantkorting (het veld **Hoofdrekening voor klantkortingen** op de pagina **Contantkortingen**) | EUR 10,50        |               |
| Klanten                                                                                |              | EUR 10,50         |






