---
title: Prijssimulatie
description: Dit artikel bevat informatie over prijssimulatie voor offertes. Met prijssimulaties kunt u het effect van inhoudingen op de toekomstige verkoopprijs tijdens het offerteproces evalueren voordat u zich vastlegt op een bepaalde prijs.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationPriceSimulation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: c5381ab48e394702c2423de7a5b5cb9166993388
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="price-simulation"></a>Prijssimulatie

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie over prijssimulatie voor offertes. Met prijssimulaties kunt u het effect van inhoudingen op de toekomstige verkoopprijs tijdens het offerteproces evalueren voordat u zich vastlegt op een bepaalde prijs.

Met een prijssimulatie voor een offerte wordt een nieuw totaalbedrag gemaakt op basis van een voorgestelde nieuwe prijs. Met een prijssimulatie kan ook een nieuw bedrag worden gemaakt voor een specifieke regel die in een bestaande offerte is gemaakt. U kunt een prijssimulatie invoeren en deze later toepassen. U kunt ook de oorspronkelijke offerte zonder prijssimulatie gebruiken en meer wijzigingen aanbrengen terwijl u het verkoopproces met de klant doorloopt.  

Met een prijssimulatie wordt de prijs in de offerte niet gewijzigd. Als de prijssimulatie op een volledige offerte wordt toegepast, wordt hij als speciale korting in de offertekoptekst verwerkt. Als de prijssimulatie op specifieke artikelen wordt toegepast, wordt hij als speciale korting in de offerteregels verwerkt. De verkoopprijs per eenheid op een offerteregel die is gemaakt, verandert niet als een prijssimulatie wordt toegepast. In plaats hiervan wordt een kortingspercentage toegepast dat overeenkomt met de prijsverlaging van de offerteregel. Wanneer een prijssimulatie wordt toegepast, worden de verkoopprijs per eenheid en het kortingspercentage overgebracht naar de offerteregel of de offertekoptekst.  

**Opmerking**: Wanneer u een prijssimulatie uitvoert, wordt alleen de huidige verkoopvaluta gebruikt voor de simulatie. Wanneer u de offertetotalen bekijkt, worden echter de bedrijfsvaluta en de verkoopvaluta weergegeven.  

Bijkomende artikelen die worden toegevoegd aan offerteregels kunnen leiden tot regelkortingen of meerregelkortingen. Zij kunnen ook leiden tot totale kortingen, waardoor de brutowinstbijdragen en brutowinstpercentages van de offerteregels en de gehele korting worden gewijzigd.  

U kunt meerdere prijssimulaties uitvoeren om de effecten van prijscorrecties op de doelen van een offerte bij te houden. Door deze simulaties uit te voeren, kunt u de algehele prijs van de offerte of de prijs van een of meer specifieke regels in de offerte aanpassen en vervolgens de prijssimulatie toepassen die waarschijnlijk leidt tot een geslaagde verkoop.  

Als u een offerte maakt, kunt u een waarschuwing instellen. Hieronder worden enkele manieren beschreven waarop waarschuwingen worden gebruikt:

-   Via waarschuwingen kunt u worden geïnformeerd over de status van de offertes binnen het bedrijf.
-   Via waarschuwingen kan een controle van een specifieke offerte worden geactiveerd of kunt u worden geïnformeerd wanneer kortingslimieten worden overschreden.

## <a name="price-simulation-and-discounts"></a>Prijssimulatie en kortingen
Kortingen en prijzen moeten correct worden berekend. Let daarom goed op als u prijssimulaties uitvoert op offertes met kortingen. Omdat alle prijssimulaties worden behandeld als speciale kortingen voor de actieve offerteregel of de gehele offerte, is het van belang om het verschil tussen kortingen goed voor ogen te houden.

### <a name="types-of-discounts-in-trade-agreements"></a>Kortingstypen in handelsovereenkomsten

In handelsovereenkomsten in Microsoft Dynamics 365 for Finance and Operations kunnen vier typen prijskortingen worden gebruikt. Deze kortingen kunnen worden ingesteld voor verschillende artikelen, klanten of prijsgroepen. De geldigheid ervan kan worden beperkt op datum. U moet bij het uitvoeren van prijssimulaties rekening houden met handelsovereenkomsten om fouten in berekeningen te voorkomen. In handelsovereenkomsten komen de volgende vier typen kortingen voor:

-   **Verkoopprijs**: Het is mogelijk om afzonderlijke verkoopprijzen op te geven voor artikelen. Bij het maken van offerteregels wordt gezocht naar de juiste verkoopprijs voor een artikel, die vervolgens in de offerteregels wordt opgenomen. Daarom is een handelsovereenkomst met dit kortingstype niet van invloed op de prijssimulatie. De verkoopprijs die in de offerteregel wordt gebruikt, is in overeenstemming met de handelsovereenkomst.
-   **Regelkorting**: Afhankelijk van de bestelde hoeveelheden worden speciale kortingen opgegeven voor artikelen. De regelkorting wordt meestal van de regelbedragen afgetrokken vóór het uitvoeren van de prijssimulatie. Daarom is een handelsovereenkomst met dit kortingstype van invloed op de prijssimulatie.
-   **Meerregelkorting**: Als de bij elkaar opgetelde hoeveelheden van vooraf gedefinieerde combinaties van bestelde artikelen hoger zijn dan de door u gedefinieerde limiet, wordt een korting toegepast op de gehele order. De regelkorting wordt meestal van de regelbedragen afgetrokken vóór het uitvoeren van de prijssimulatie. Daarom is een handelsovereenkomst met dit kortingstype van invloed op de prijssimulatie.
-   **Eindkorting**: Als de bij elkaar opgetelde bedragen van vooraf gedefinieerde bestelde artikelen hoger zijn dan de door u gedefinieerde limiet, wordt een korting toegepast op de gehele order. De eindkorting wordt gegenereerd door de offerteregels. Omdat de eindkorting echter wordt toegepast op het offertetotaal, wordt het totaalbedrag van de offerte verlaagd. Daarom is een handelsovereenkomst met dit kortingstype van invloed op de prijssimulatie.

### <a name="quotation-lines-and-trade-agreements"></a>Offerteregels en handelsovereenkomsten

Als u een offerteregel maakt of corrigeert, worden regelkortingen automatisch berekend. Op basis van de handelsovereenkomst wordt gezocht naar de relevante verkoopprijs voor het artikel.

## <a name="price-simulation-examples"></a>Voorbeelden van prijssimulatie
In de volgende voorbeelden wordt gebruikgemaakt van prijssimulatie voor offertekopteksten en afzonderlijke regels met artikelen.

### <a name="price-simulation-for-quotation-headers"></a>Prijssimulatie voor offertekopteksten

U maakt een offerte met de volgende regels:

-   10 eenheden van artikel BR-12 (kostprijs per eenheid EUR 9,52, verkoopprijs per eenheid EUR 15,32)
-   12 eenheden van artikel BR-14 (kostprijs per eenheid EUR 7,48, verkoopprijs per eenheid EUR 13,75)

De volgende tabel bevat de offerteregels:

|                            | Berekening                          | Resultaat   |
|----------------------------|--------------------------------------|----------|
| Verkoophoeveelheid             | 10 eenheden + 12 eenheden                  | 22 eenheden |
| Verkoopwaarde in EUR         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Kostprijs in EUR          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Brutowinstbijdrage in EUR | 318,20 – 184,96                      | 133,24   |
| Winstbedrag         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87%   |

U voert een prijssimulatie uit en past een eindkorting van 15 procent toe op de volledige offerte of de offertekoptekst. De volgende tabel bevat de nieuwe totalen van de offerte nadat de prijssimulatie is uitgevoerd.

|                                                      | Berekening                               | Resultaat   |
|------------------------------------------------------|-------------------------------------------|----------|
| Verkoophoeveelheid                                       | 10 eenheden + 12 eenheden                       | 22 eenheden |
| Oude verkoopwaarde in EUR                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Oude kostprijs in EUR                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Oude brutowinstbijdrage in EUR                       | 318,20 – 184,96                           | 133,24   |
| Oude bijdrageverhouding                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87%   |
| Prijssimulatie voor eindkorting van 15% in EUR | (15 × 318,2) ÷ 100                        | 47,73    |
| Nieuwe verkoopwaarde in EUR                               | 318,20 – 47,73                            | 270,47   |
| Nieuwe brutowinstbijdrage in EUR                       | 270,47 – 184,96                           | 85,51    |
| Nieuw winstbedrag                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61%   |

### <a name="price-simulation-for-single-line-items"></a>Prijssimulatie voor afzonderlijk regels met artikelen

U maakt een offerte met de volgende regels:

-   10 eenheden van artikel BR-12 (kostprijs per eenheid EUR 9,52, verkoopprijs per eenheid EUR 15,32)
-   12 eenheden van artikel BR-14 (kostprijs per eenheid EUR 7,48, verkoopprijs per eenheid EUR 13,75)

De volgende tabel bevat de offerteregels:

|                                      | Berekening                          | Resultaat   |
|--------------------------------------|--------------------------------------|----------|
| Verkoophoeveelheid                       | 10 eenheden + 12 eenheden                  | 22 eenheden |
| Verkoopwaarde in EUR voor BR-12         | 10 × 15,32                           | 153,20   |
| Verkoopwaarde in EUR voor BR-14         | 12 × 13,75                           | 165,00   |
| Kostprijs in EUR voor BR-12          | 10 × 9,52                            | 95,20    |
| Kostprijs in EUR voor BR-14          | 12 × 7,48                            | 89,76    |
| Brutowinstbijdrage in EUR voor BR-12 | 153,20 – 95,20                       | 58,00    |
| Brutowinstbijdrage in EUR voor BR-14 | 165,00 – 89,76                       | 75,24    |
| Bijdrageverhouding in EUR voor BR-12  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Bijdrageverhouding in EUR voor BR-14  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Totale verkoopwaarde in EUR             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Totale kostprijs in EUR              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Totale brutowinstbijdrage in EUR     | 318,20 – 184,96                      | 133,24   |
| Totale bijdrageverhouding             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87%   |

U voert een prijssimulatie uit en past een eindkorting van 10 procent toe op de eenheden van artikel BR-12. De volgende tabel bevat de nieuwe totalen van de offerte nadat de prijssimulatie is uitgevoerd voor de afzonderlijke regel met artikelen.

|                                                   | Berekening                             | Resultaat   |
|---------------------------------------------------|-----------------------------------------|----------|
| Verkoophoeveelheid                                    | 10 eenheden + 12 eenheden                     | 22 eenheden |
| Oude verkoopwaarde in EUR voor BR-12                  | 10 × 15,32                              | 153,20   |
| Priijssimulatie voor 10% korting voor BR-12 | (10 × 153,2) ÷ 100                      | 15,32    |
| Nieuwe verkoopwaarde in EUR voor BR-12                  | (10 × 15,32) – 15,32                    | 137,88   |
| Verkoopwaarde in EUR voor BR-14                      | 12 × 13,75                              | 165,00   |
| Kostprijs in EUR voor BR-12                       | 10 × 9,52                               | 95,20    |
| Kostprijs in EUR voor BR-14                       | 12 × 7,48                               | 89,76    |
| Nieuwe brutowinstbijdrage in EUR voor BR-12          | 137,88 – 95,20                          | 42,68    |
| Brutowinstbijdrage in EUR voor BR-14              | 165,00 – 89,76                          | 75,24    |
| Nieuwe bijdrageverhouding in EUR voor BR-12           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Bijdrageverhouding in EUR voor BR-14               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Nieuwe totale verkoopwaarde in EUR                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Totale kostprijs in EUR                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Nieuwe totale brutowinstbijdrage in EUR              | 302,88 – 184,96                         | 117,92   |
| Nieuw totaal winstbedrag                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93%   |

De prijssimulatie is alleen van invloed op de regel waarop deze is toegepast en verlaagt het totaal voor die regel.




