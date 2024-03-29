---
title: Ondersteuning van twee valuta's voor belasting
description: In dit artikel wordt uitgelegd hoe u de functie voor boekhouding met twee valuta's uitbreidt in het belastingdomein en wat de gevolgen zijn bij het berekenen en boeken van belasting
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 13d70d964a83c2efba090244d549bdb38ad25af2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909035"
---
# <a name="dual-currency-support-for-sales-tax"></a>Ondersteuning van twee valuta's voor btw
[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u boekhouding met twee valuta's voor btw uitbreidt en wat de gevolgen zijn voor btw-berekeningen, boekingen en vereffeningen

De functie voor twee valuta's voor Dynamics 365 Finance werd geïntroduceerd in versie 8.1 (oktober 2018). Het verandert de manier waarop boekhoudvermeldingen in de aangiftevaluta worden berekend.

In eerdere versies werden transacties in deze volgorde omgezet naar de aangiftevaluta: 

- Het transactietotaal werd berekend in de transactievaluta > het transactiebedrag werd omgerekend naar de valuta voor boekhouding > het bedrag van de valuta voor boekhouding werd omgerekend naar de aangiftevaluta

Na inschakeling van de functie voor twee valuta's werden transacties in deze volgorde omgezet naar de aangiftevaluta:

- Transactievalutabedrag > Aangiftevalutabedrag

Raadpleeg [Twee valuta's](dual-currency.md) voor meer informatie over twee valuta's.

Als gevolg van de ondersteuning voor twee valuta's zijn er twee nieuwe functies beschikbaar in functiebeheer: 

- Btw-conversie (nieuw in versie 10.0.13)
- Financiële dimensies invoeren in de gerealiseerde winst-/verliesrekeningen voor valutacorrectie voor btw-vereffening (nieuw in 10.0.17)

Ondersteuning voor twee valuta's voor btw zorgt ervoor dat btw nauwkeurig wordt berekend in de belastingvaluta en dat het btw-vereffeningssaldo nauwkeurig wordt berekend in zowel de valuta voor boekhouding als de aangiftevaluta.

## <a name="sales-tax-conversion"></a>Btw-conversie

De parameter **Btw-conversie** biedt twee opties voor het omrekenen van het belastingbedrag van de transactievaluta naar de belastingvaluta. 

- Valuta voor boekhouding: het pad is "Bedrag in transactievaluta > Bedrag in valuta voor boekhouding > Bedrag in aangiftevaluta". Het wisselkoerstype voor de valuta voor boekhouding (geconfigureerd in Grootboek instellen) wordt gebruikt voor de valutaomrekening.
- Aangiftevaluta : het pad is "Bedrag in transactievaluta > Bedrag in aangiftevaluta > Bedrag in belastingvaluta". Het wisselkoerstype voor de aangiftevaluta (geconfigureerd in Grootboek instellen) wordt gebruikt voor de valutaomrekening.

### <a name="example"></a>Voorbeeld

Een eenvoudig voorbeeld om deze functionaliteit te demonstreren is:

Valuta-instelling voor grootboek en belasting

| Transactievaluta | Boekhoudvaluta | Aangiftevaluta | Belastingvaluta |
| -------------------- | ------------------- | ------------------ | ------------ |
| EUR                  | EUR                 | GBP                | GBP          |

Wisselkoers

| Vanuit valuta | Naar valuta | Factor | Wisselkoers |
| ------------- | ----------- | ------ | ------------- |
| EUR           | EUR         | 1      | 1.11          |
| EUR           | GBP         | 1      | 0.83          |
| EUR           | GBP         | 1      | 0.75          |

Berekening van belastingbedrag met verschillende parameteropties

Belastingbedrag = 100 EUR

| Parameters voor btw-conversie | Transactievaluta (EUR) | Boekhoudvaluta (USD) | Aangiftevaluta (GBP) | Belastingvaluta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Boekhoudvaluta             | 100                        | 111                       | 83                       | **83.25**          |
| Aangiftevaluta              | 100                        | 111                       | 83                       | **83**             |

Deze parameter kan worden geconfigureerd op basis van de conformiteitsbehoefte van de belastingdienst.


### <a name="upgrade-consideration"></a>Overweging bij upgrades

Deze functie is alleen van toepassing op nieuwe transacties. Voor belastingtransacties die al zijn opgeslagen in de tabel TAXTRANS maar nog niet zijn vereffend, wordt het belastingbedrag niet opnieuw berekend in de belastingvaluta omdat de wisselkoers op het moment van het boeken van de belasting al ontbreekt.

Om het voorgaande scenario te voorkomen, wordt u aangeraden deze parameterwaarde te wijzigen in een nieuwe (schone) belastingvereffeningsperiode die geen niet-vereffende belastingtransacties bevat. Als u deze waarde wilt wijzigen in het midden van een vereffeningsperiode voor belasting, voert u de optie 'Btw vereffenen en boeken' uit voor de huidige vereffeningsperiode voor belasting voordat u deze parameterwaarde wijzigt.

Met deze functie voegt u boekhoudregels toe die winsten en verliezen door valutaomrekeningen verduidelijken. De posten worden gemaakt in de gerealiseerde winst- en verliesrekeningen van valutacorrecties wanneer de herwaardering wordt uitgevoerd tijdens de btw-vereffening. Zie de sectie [Automatisch belastingsvereffeningssaldo in aangiftevaluta](#tax-settlement-auto-balance-in-reporting-currency) verderop in dit artikel voor meer informatie.

> [!NOTE]
> Tijdens de vereffening worden gegevens voor financiële dimensies overgenomen uit btw-rekeningen, die balansrekeningen zijn, en ingevoerd in winst-en-verliesrekeningen voor valutacorrecties. Dit zijn winst-en-verliesrekeningen. Aangezien de beperkingen voor de waarde van financiële dimensies tussen balansrekeningen en verlies-en-winstrekeningen verschillen, kan er een fout optreden tijdens het proces Btw vereffenen en boeken. Als u wilt voorkomen dat u rekeningstructuren moet wijzigen, kunt u de functie "Financiële dimensies invullen voor de gerealiseerde winst-/verliesrekeningen voor valutacorrectie voor btw-vereffening" inschakelen. Met deze functie wordt de derivatie van financiële dimensies voor winst-/verliesrekeningen voor valutacorrecties afgedwongen. 

## <a name="track-reporting-currency-tax-amount"></a>Belastingbedrag in aangiftevaluta bijhouden

Er zijn drie nieuwe velden toegevoegd aan belastingtabellen om bedragen in de aangiftevaluta bij te houden. Deze velden bevinden zich in de tabellen TAXUNCOMMITTED en TAXTRANS:

- TaxAmountRep: belastingbedrag in aangiftevaluta
- TaxBaseAmountRep: basisbedrag in aangiftevaluta
- TaxInCostPriceRep: niet-aftrekbaar bedrag in aangiftevaluta

Voor belasting die alleen is opgeslagen in de tabel TAXUNCOMMITTED maar nog niet is geboekt, wordt het belastingbedrag opnieuw berekend in de aangiftevaluta op het moment dat de gegevens worden geboekt en opgeslagen in de tabel TAXTRANS.

Deze release bevat geen wijzigingen in rapporten en formulieren waarbij het belastingbedrag wordt weergegeven in de aangiftevaluta. Wijzigingen in rapporten en formulieren worden in de toekomstige versie geleverd.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Automatisch belastingsvereffeningssaldo in aangiftevaluta

Als de belastingvereffening om bepaalde redenen niet wordt gesaldeerd in de aangiftevaluta, bijvoorbeeld wanneer het pad voor btw-conversie "Valuta voor boekhouding" is of wanneer de wisselkoers verandert in een enkele periode voor belastingvereffening, dan genereert het systeem automatisch boekhoudposten om de afwijking van het belastingbedrag te corrigeren en te compenseren tegen gerealiseerde winsten of verliezen voor valutaomrekening.

Stel dat, uitgaand van het vorige voorbeeld om deze functie te demonstreren, de gegevens in de tabel TAXTRANS op het moment van boeken als volgt zijn.

| Parameters voor btw-conversie | Transactievaluta (EUR) | Boekhoudvaluta (USD) | Aangiftevaluta (GBP) | Belastingvaluta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Boekhoudvaluta             | 100                        | 111                       | 83                       | **83,25**          |
| Aangiftevaluta              | 100                        | 111                       | 83                       | **83**             |

Wanneer u het btw-vereffeningsprogramma aan het einde van de maand uitvoert, ziet de boekhoudingsvermelding er als volgt uit.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Scenario: btw-conversie = "Valuta voor boekhouding"

| Hoofdrekening           | Transactievaluta (GBP) | Boekhoudvaluta (USD) | Aangiftevaluta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Te betalen/ontvangen belasting | -83,25                     | -111                      | -83,25                   |
| Belastingvereffening         | 83,25                      | 111                       | 83,25                    |
| Gerealiseerde winst/verlies     | 0                          | 0                         | -0,25                    |
| Te betalen/ontvangen belasting | 0                          | 0                         | 0,25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Scenario: btw-conversie = "Aangiftevaluta"


| Hoofdrekening           | Transactievaluta (GBP) | Boekhoudvaluta (USD) | Aangiftevaluta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Te betalen/ontvangen belasting | -83                        | -110,67                   | -83                      |
| Belastingvereffening         | 83                         | 110,67                    | 83                       |
| Gerealiseerde winst/verlies     | 0                          | 0,33                      | 0                        |
| Te betalen/ontvangen belasting | 0                          | -0,33                     | 0                        |



Zie de volgende onderwerpen voor meer informatie:

- [Twee valuta's](dual-currency.md)
- [Btw-overzicht](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
