---
title: Analyse kostprijsboekhouding Power BI-inhoud
description: Dit onderwerp wordt beschreven wat wordt opgenomen in de kostprijsboekhouding analyse Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de rapporten Power BI en informatie over het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de inhoud.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Analyse kostprijsboekhouding Power BI-inhoud

Dit onderwerp wordt beschreven wat wordt opgenomen in de kostprijsboekhouding analyse Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de rapporten Power BI en informatie over het gegevensmodel en entiteiten die zijn gebruikt voor het bouwen van de inhoud.

<a name="overview"></a>Overzicht
--------

De **Analyse kostprijsboekhouding** Microsoft Power BI-inhoud is bedoeld voor kosten-domeincontrollers of iemand anders die verantwoordelijk is voor het uitvoeren van de kosten van een organisatie te beheren. Bevat de essentiële gegevens, zoals kosten, grootte en kostentarief door werkelijke kosten, budgetkosten en flexibele budgetkosten. Deze transactiegegevens uit kostprijsboekhouding worden gebruikt in Microsoft Dynamics 365 voor bewerkingen en geeft een samengevoegde weergave van kosten voor de hele organisatie in een rapportagevaluta. Managers kunnen de gegevens filteren op kostenobjecten uit te voeren kostenbeheer van hun organisatie-eenheden, zelfs als de organisatie meerdere rechtspersonen kan zijn. Omdat de **Analyse kostprijsboekhouding** Power BI inhoud gemarkeerd afwijkingen tussen de werkelijke en gebudgetteerde kosten managers kunnen worden gewaarschuwd over positieve en negatieve trends voor hun operationele eenheden. Managers kunnen inzoomen op de kosten element hiërarchieën of afzonderlijke kostenelementen inzicht te verwerven gedetailleerde in hoe kostenafwijkingen hebben plaatsgevonden, en dan doeltreffende actie ondernemen. De **Analyse kostprijsboekhouding** Power BI inhoud laten accountants kosten analyseren hoe kosten stromen door de kostenobjecten van de hele organisatie. Zie voor meer informatie over kostprijsboekhouding, [startpagina kostprijsboekhouding](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Als u beveiliging op recordniveau toegang in kostprijsboekhouding definieert en combineert met beveiliging op in Power BI, u kunt alle kosten van objecteigenaren toegang verlenen tot de **Analyse kostprijsboekhouding** Power BI-inhoud. Alle gegevens in de visualisaties wordt vervolgens gefilterd op het toegangsniveau dat in de kostprijsboekhouding wordt geregeld. Zie voor meer informatie over beveiliging op recordniveau toegang en beveiliging op [beveiliging instellen voor kostprijsboekhouding inhoud voor Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Toegang tot de content Power BI
U vindt de **Analyse kostprijsboekhouding** Power BI-inhoud in de bibliotheek met gedeelde elementen in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over het downloaden van de inhoud en deze verbinden met uw Dynamics 365 voor bewerkingen gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md). **opmerking:** KB4011327 ** ** is vereist voor de **Analyse kostprijsboekhouding** Power BI-inhoud.  Nadat u zich bij Lifecycle Services aanmeldt, kunt u de KB hier openen: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Prestatiegegevens die zijn opgenomen in de Power BI-inhoud
De inhoud bevat een reeks rapportpagina's. Elke pagina bestaat uit een set parameters die worden weergegeven als diagrammen, tegels en tabellen. De volgende tabel bevat een overzicht van de visualisaties in de **Analyse kostprijsboekhouding** Power BI-inhoud.

| Rapportpagina.                      | Diagram                                                                                                                         | Tegel                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kostenbeheer per boekingsperiode    | Werkelijke kosten en budgetkosten op kosten element hiërarchieniveau                                                                   | Werkelijke kosten versus gebudgetteerde kosten                    |
|                                  | Budget variantie op basis van kosten element hiërarchieniveau                                                                               | Werkelijke kosten tarief vs budget tarieven          |
|                                  | Top 10 budgetafwijking in procenten door kosten-element                                                                          | Werkelijke grootte vs budget grootte          |
| Kostenbeheer per jaar tot heden     | Werkelijke kosten en budgetkosten per kalenderjaar periode                                                                           | Werkelijke kosten versus gebudgetteerde kosten                    |
|                                  | Budgetafwijking per kalenderjaar periode                                                                                       | Werkelijke kosten tarief vs budget tarieven          |
|                                  | Top 10 budgetafwijking in procenten door kosten-element                                                                          | Werkelijke grootte vs budget grootte          |
| Kostentarief op fiscaal jaar         | Werkelijke kostentarief door kosten gedrag                                                                                             | Werkelijke kosten tarief vs budget tarieven          |
|                                  | Tarief voor werkelijke kosten, gebudgetteerde kosten Koersafwijkingen, gebudgetteerde kosten percentage voor en budget kostentarief door kosten element hiërarchieniveau | Werkelijke grootte vs budget grootte          |
|                                  | Budget variantie op basis van kosten element hiërarchieniveau                                                                               |                                               |
|                                  | Top 10 budgetafwijking in procenten door kosten-element                                                                          |                                               |
| Flexibel budget per boekingsperiode | Werkelijke kosten, budgetkosten en flexibele budgetkosten op kosten element hiërarchieniveau                                             | Werkelijke grootte vs budget grootte          |
|                                  | Budgetafwijking en flexibele budget variantie op basis van kosten element hiërarchieniveau                                                  | Werkelijke kosten versus flexibele budgetkosten           |
|                                  | Werkelijke kosten, budgetkosten en flexibele kosten door gedrag kosten en de element-hiërarchieniveau                                  | Kostentarief voor werkelijke kosten tarief vs flexibel budget |
| Kostenoverzicht per boekingsperiode  | Werkelijke kosten per element hiërarchieniveau kosten en de objectnaam dimensie lid                                             |                                               |
|                                  | Werkelijke kosten per dimensie kosten-lid objectnaam en dimensie kosten-lid elementnaam                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Dynamics 365 voor bewerkingen gegevens wordt gebruikt voor het vullen van de rapportpagina's de **Analyse kostprijsboekhouding** Power BI-inhoud. Deze gegevens wordt vertegenwoordigd door statistische metingen die worden klaargezet in het archief entiteit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [overzicht Power BI-integratie met entiteit winkel](power-bi-integration-entity-store.md). De volgende belangrijke statistische metingen worden gebruikt als basis voor de inhoud.

| Entiteit                  | Belangrijke statistische meting | Gegevensbron voor Dynamics 365 for Operations | Veld     | Omschrijving                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Posten voor kostprijsboekhouding | SUM(Amount)               | CAMDATAAggregatedCostEntry                  | Bedrag    | Bedrag in de valuta voor het grootboek van kostprijsboekhouding |
| Statistische boekingen     | SUM(MAGNITUDE)            | CAMDATAAggregatedStatisctialEntry           | Magnitude |                                               |

De volgende tabel ziet hoe de belangrijkste statistische metingen worden gebruikt voor verschillende berekende eenheden maken in de inhoud van de gegevensset.

| Maat                                       | Hoe de maateenheid wordt berekend                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Werkelijke kosten                                   | BEREKENEN ('Cost accounting vermeldingen'\[eenheid\], transactie-versies\[ISSOURCEVERSIONBUDGET\_waarde\] = 0)            |
| Kosten volgens budget                                   | BEREKENEN ('Cost accounting vermeldingen'\[eenheid\], transactie-versies\[ISSOURCEVERSIONBUDGET\_waarde\] = 1)            |
| Budgetkosten afwijking                          | \[budget kosten\] - \[werkelijke kosten\]                                                                                      |
| Afwijkingspercentage van budget                    | IF (\[gebudgetteerde kosten\] = 0, blank(), \[budgetafwijking\] / \[gebudgetteerde kosten\])                                                |
| Werkelijke grootte                              | BEREKENEN ('Statistische vermeldingen'\[FullMagnitude\], transactie-versies\[ISSOURCEVERSIONBUDGET\_waarde\] = 0)          |
| Grootte budget                              | BEREKENEN (\[FullMagnitude\], transactie-versies\[ISSOURCEVERSIONBUDGET\_waarde\] = 1)                               |
| Statistische budgetafwijking                   | \[Grootte budget\] - \[werkelijke grootte\]                                                                            |
| Afwijkingspercentage statistische budget        | IF (\[budget grootte\] = 0, blank(), \[statistische budgetafwijking\] / \[budget grootte\])                          |
| Werkelijke kostentarief                              | IF (\[werkelijke grootte\] = 0, BLANK(), \[werkelijke kosten\] / \[werkelijke grootte\])                                          |
| Budgetkostentarief                              | IF (\[budget grootte\] = 0, BLANK(), \[gebudgetteerde kosten\] / \[budget grootte\])                                          |
| Koersafwijkingen budgetkosten                     | \[budget kostentarief\] - \[Werkelijk kostentarief\]                                                                            |
| Budgetkosten tarief afwijkingspercentage          | IF (\[gebudgetteerde kosten\] = 0, blank(), \[gebudgetteerde kosten Koersafwijkingen\] / \[budget kostentarief\])                                 |
| Gebudgetteerde vaste kosten                             | BEREKENEN (\[gebudgetteerde kosten\], 'kosten accounting vermeldingen'\[COSTBEHAVIOR\] = 1)                                              |
| Variabele gebudgetteerde kosten                          | BEREKENEN (\[gebudgetteerde kosten\], 'kosten accounting vermeldingen'\[COSTBEHAVIOR\] = 2)                                              |
| Vaste flexibele budgetkosten                    | \[Gebudgetteerde vaste kosten\]                                                                                                  |
| Variabele flexibele budgetkosten                 | IF (\[budget grootte\] = 0, BLANK(), (\[variabele gebudgetteerde kosten\] / \[budget grootte\]) \*\[werkelijke grootte\])       |
| Flexibele budgetkosten                          | \[Flexibele budgetkosten vaste\] + \[variabele flexibele budgetkosten\]                                                     |
| Flexibel budgetafwijking                      | \[Flexibele budgetkosten\] - \[werkelijke kosten\]                                                                             |
| Afwijkingspercentage flexibel budget           | IF (\[flexibele budgetkosten\] = 0, BLANK(), \[flexibel budgetafwijking\] / \[flexibele budgetkosten\])                     |
| Flexibele budgetkosten tarief                     | IF (\[werkelijke grootte\] = 0, BLANK(), \[flexibele budgetkosten\] / \[werkelijke grootte\])                                 |
| Koersafwijkingen flexibele budgetkosten            | \[kostentarief flexibel budget\] - \[Werkelijk kostentarief\]                                                                   |
| Flexibel budget kosten tarief afwijkingspercentage | IF (\[kostentarief flexibel budget\] = 0, BLANK(), \[flexibel budget Koersafwijkingen kosten\] / \[kostentarief flexibel budget\]) |

De volgende belangrijke dimensies worden gebruikt als filters voor het segmenteren van de statistische metingen grotere mate van granulatie bereiken en meer analytische inzicht bieden.

| Entiteit                             | Voorbeelden van kenmerken                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Grootboeken van kostprijsboekhouding            | Grootboek van kostprijsboekhouding                                                                                               |
| Kostenbeheereenheden                 | Naam van kostenbeheereenheid                                                                                               |
| Dimensies van kostenelement            | Kosten elementen dimension naam, naam dimensielid kosten element, kosten element dimensie lid omschrijving          |
| Dimensies van kostenobject             | Dimensienaam kostenobject, dimensie kosten-lid objectnaam, dimensie kosten-lid objectomschrijving              |
| Statistische dimensies             | Statistische dimensienaam, statistische dimensie lidnaam, omschrijving voor de statistische artikeldimensie lid              |
| Dimensiehiërarchieën kostendrager  | Hiërarchie van de objectnaam dimensie kosten, kosten object dimensie-hiërarchieniveau, kosten object dimensiehiërarchiestructuur    |
| Kosten element dimensiehiërarchieën | Hiërarchie van de elementnaam dimensie kosten, kosten element dimensie-hiërarchieniveau, kosten element dimensiehiërarchiestructuur |
| Statistische dimensiehiërarchieën  | Hiërarchie van statistische dimensienaam, statistische dimensie-hiërarchieniveau, statistische dimensiehiërarchiestructuur    |
| Transactieversies               | Versienaam                                                                                                         |
| Fiscale kalenders                   | Kalender, kalender-omschrijving                                                                                       |
| Fiscale jaren                       | Kalenderjaar                                                                                                        |
| Boekperioden                     | Kalenderjaar periode                                                                                                 |

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)
-   [Beveiliging voor inhoud van de kostprijsboekhouding instellen voor Power BI](setup-security-cost-accounting-content-pack.md)


