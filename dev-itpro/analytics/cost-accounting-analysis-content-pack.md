---
title: Power BI-inhoud voor analyse van kostprijsboekhouding
description: In dit onderwerp wordt beschreven wat wordt opgenomen in de Power BI-inhoud voor kostprijsboekhoudingsanalyse. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
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

# <a name="cost-accounting-analysis-power-bi-content"></a>Power BI-inhoud voor analyse van kostprijsboekhouding

In dit onderwerp wordt beschreven wat wordt opgenomen in de Power BI-inhoud voor kostprijsboekhoudingsanalyse. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

<a name="overview"></a>Overzicht
--------

De Microsoft Power BI-inhoud voor **Analyse kostprijsboekhouding** is bedoeld voor kostencontrollers of iemand anders die verantwoordelijk is voor het uitvoeren van het kostenbeheer van een organisatie. Het bevat de belangrijkste metrische gegevens, zoals kosten, magnitude en kostentarief op basis van werkelijke kosten, budgetkosten en flexibele budgetkosten. Hierin worden transactiegegevens uit de kostprijsboekhouding in Microsoft Dynamics 365 for Operations gebruikt en wordt een samengevoegde weergave van kosten verschaft voor de gehele organisatie in één rapportagevaluta. Managers kunnen de gegevens filteren op basis van kostenobjecten om kostenbeheer van hun organisatie-eenheden uit te voeren, zelfs als de organisatie meerdere rechtspersonen heeft. Omdat de Power BI-inhoud voor **Analyse kostprijsboekhouding** afwijkingen tussen de werkelijke en gebudgetteerde kosten markeert, kunnen managers worden geïnformeerd over positieve en negatieve trends voor hun operationele eenheden. Managers kunnen inzoomen op de kostenelementhiërarchieën of op afzonderlijke kostenelementen om een gedetailleerd inzicht te verwerven in hoe kostenafwijkingen hebben plaatsgevonden. Vervolgens kunnen ze doeltreffende actie ondernemen. Met de Power BI-inhoud voor **Analyse kostprijsboekhouding** kunnen accountants analyseren hoe kosten de kostenobjecten van de gehele organisatie doorlopen. Zie voor meer informatie over kostprijsboekhouding [Startpagina kostprijsboekhouding](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Als u beveiliging op toegangsniveau in kostprijsboekhouding definieert en combineert met beveiliging op rijniveau in Power BI, kunt u alle kostenobjecteigenaren toegang verlenen tot de Power BI-inhoud voor **Analyse kostprijsboekhouding**. Alle gegevens in de visualisaties worden vervolgens gefilterd op basis van het toegangsniveau dat in de kostprijsboekhouding wordt beheerd. Zie voor meer informatie over beveiliging op toegangsniveau en beveiliging op rijniveau [Beveiliging instellen voor kostprijsboekhoudingsinhoud voor Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
U vindt de Power BI-inhoud voor **Kostprijsboekhouding** in de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u de inhoud downloadt en koppelt aan uw Microsoft Dynamics 365 for Operations-gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md). **Opmerking:** KB4011327 is een vereiste voor de Power BI-inhoud voor **Analyse kostprijsboekhouding**.  Nadat u zich bij Lifecycle Services hebt aangemeld, kunt u de KB hier openen: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
De inhoud bevat een reeks rapportpagina's. Elke pagina bestaat uit een set metrische gegevens die worden gevisualiseerd als diagrammen, tegels en tabellen. De volgende tabel bevat een overzicht van de visualisaties in de Power BI-inhoud voor **Analyse kostprijsboekhouding**.

| Rapportpagina                      | Diagram                                                                                                                         | Tegel                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kostenbeheer per boekperiode    | Werkelijke kosten en budgetkosten per hiërarchieniveau kostenelement                                                                   | Werkelijke kosten versus budgetkosten                    |
|                                  | Budgetafwijking per hiërarchieniveau kostenelement                                                                               | Tarief werkelijke kosten versus tarief budgetkosten          |
|                                  | Top 10 budgetafwijkingen in percentage per kostenelement                                                                          | Werkelijke magnitude versus budgetmagnitude          |
| Kostenbeheer per jaar tot heden     | Werkelijke kosten en budgetkosten per kalenderjaarperiode                                                                           | Werkelijke kosten versus budgetkosten                    |
|                                  | Budgetafwijking per kalenderjaarperiode                                                                                       | Tarief werkelijke kosten versus tarief budgetkosten          |
|                                  | Top 10 budgetafwijkingen in percentage per kostenelement                                                                          | Werkelijke magnitude versus budgetmagnitude          |
| Kostentarief per boekjaar         | Tarief werkelijke kosten per kostengedrag                                                                                             | Tarief werkelijke kosten versus tarief budgetkosten          |
|                                  | Tarief werkelijke kosten, afwijking tarief budgetkosten, percentage voor tarief budgetkosten en tarief budgetkosten per hiërarchieniveau kostenelement | Werkelijke magnitude versus budgetmagnitude          |
|                                  | Budgetafwijking per hiërarchieniveau kostenelement                                                                               |                                               |
|                                  | Top 10 budgetafwijkingen in percentage per kostenelement                                                                          |                                               |
| Flexibel budget per boekperiode | Werkelijke kosten, budgetkosten en flexibele budgetkosten per hiërarchieniveau kostenelement                                             | Werkelijke magnitude versus budgetmagnitude          |
|                                  | Budgetafwijking en flexibele budgetafwijking per hiërarchieniveau kostenelement                                                  | Werkelijke kosten versus flexibele budgetkosten           |
|                                  | Werkelijke kosten, budgetkosten en flexibele kosten per kostengedrag en hiërarchieniveau kostenelement                                  | Tarief werkelijke kosten versus tarief flexibele budgetkosten |
| Kostenoverzicht per boekperiode  | Werkelijke kosten per hiërarchieniveau kostenelement en dimensielidnaam kostenobject                                             |                                               |
|                                  | Werkelijke kosten per dimensielidnaam kostenobject en dimensielidnaam kostenelement                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Dynamics 365 for Operations-gegevens worden gebruikt voor het vullen van de rapportpagina's in de Power BI-inhoud voor **Analyse kostprijsboekhouding**. Deze gegevens worden vertegenwoordigd als samengevoegde metingen die worden klaargezet in de Entiteitopslag. Dit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md). De volgende belangrijke samengevoegde metingen worden gebruikt als de basis van de inhoud.

| Entiteit                  | Belangrijke samengevoegde meting | Gegevensbron voor Dynamics 365 for Operations | Veld     | Omschrijving                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Kostprijsboekhoudingsposten | SUM(Amount)               | CAMDATAAggregatedCostEntry                  | Bedrag    | Bedrag in de grootboekvaluta voor de kostprijsboekhouding |
| Statistische boekingen     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry           | Magnitude |                                               |

In de volgende tabel ziet u hoe de belangrijkste samengevoegde metingen worden gebruikt om verschillende berekende eenheden te maken in de gegevensset van de inhoud.

| Maat                                       | Hoe de meting wordt berekend                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Werkelijke kosten                                   | CALCULATE('Kostprijsboekhoudingsposten'\[Measure\], 'Transactieversies'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Kosten volgens budget                                   | CALCULATE('Kostprijsboekhoudingsposten'\[Measure\], 'Transactieversies'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Budgetkostenafwijking                          | \[Budgetkosten\] - \[Werkelijke kosten\]                                                                                      |
| Budgetafwijkingspercentage                    | IF(\[Budgetkosten\] = 0, blank(), \[Budgetafwijking\] / \[Budgetkosten\])                                                |
| Werkelijke magnitude                              | CALCULATE('Statistische boekingen'\[FullMagnitude\], 'Transactieversies'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Budgetmagnitude                              | CALCULATE(\[FullMagnitude\], 'Transactieversies'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| Statistische budgetafwijking                   | \[Budgetmagnitude\] - \[Werkelijke magnitude\]                                                                            |
| Statistisch budgetafwijkingspercentage        | IF(\[Budgetmagnitude\] = 0, blank(), \[Statistische budgetafwijking\] / \[Budgetmagnitude\])                          |
| Werkelijke kostentarief                              | IF(\[Werkelijke magnitude\] = 0, BLANK(), \[Werkelijke kosten\] / \[Werkelijke magnitude\])                                          |
| Budgetkostentarief                              | IF(\[Budgetmagnitude\] = 0, BLANK(), \[Budgetkosten\] / \[Budgetmagnitude\])                                          |
| Afwijking budgetkostentarief                     | \[Tarief budgetkosten\] - \[tarief werkelijke kosten\]                                                                            |
| Percentage afwijking budgetkostentarief          | IF(\[Budgetkosten\] = 0, blank(), \[Afwijking budgetkostentarief\] / \[Tarief budgetkosten\])                                 |
| Vaste budgetkosten                             | CALCULATE(\[Budgetkosten\], 'Kostprijsboekhoudingsposten'\[COSTBEHAVIOR\] = 1)                                              |
| Variabele budgetkosten                          | CALCULATE(\[Budgetkosten\], 'Kostprijsboekhoudingsposten'\[COSTBEHAVIOR\] = 2)                                              |
| Vaste flexibele budgetkosten                    | \[Vaste budgetkosten\]                                                                                                  |
| Variabele flexibele budgetkosten                 | IF(\[Budgetmagnitude\] = 0, BLANK(), (\[Variabele budgetkosten\] / \[Budgetmagnitude\]) \* \[Werkelijke magnitude\])       |
| Flexibele budgetkosten                          | \[Vaste flexibele budgetkosten\] + \[variabele flexibele budgetkosten\]                                                     |
| Afwijking flexibel budget                      | \[Flexibele budgetkosten\] - \[Werkelijke kosten\]                                                                             |
| Percentage afwijking flexibel budget           | IF (\[Flexibele budgetkosten\] = 0, BLANK(), \[Afwijking flexibel budget\] / \[Flexibele budgetkosten\])                     |
| Tarief flexibele budgetkosten                     | IF(\[Werkelijke magnitude\] = 0, BLANK(), \[Flexibele budgetkosten\] / \[Werkelijke magnitude\])                                 |
| Afwijking tarief flexibele budgetkosten            | \[Tarief flexibele budgetkosten\] - \[Tarief werkelijke kosten\]                                                                   |
| Percentage afwijking van tarief flexibele budgetkosten | IF (\[Tarief flexibele budgetkosten\] = 0, BLANK(), \[Afwijking tarief flexibele budgetkosten\] / \[Tarief flexibele budgetkosten\]) |

De volgende belangrijke dimensies worden gebruikt als filters voor het segmenteren van de samengevoegde metingen om een grotere mate van granulatie te bereiken en analytischere inzichten te bieden.

| Entiteit                             | Voorbeelden van kenmerken                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Grootboeken van kostprijsboekhouding            | Grootboek van kostprijsboekhouding                                                                                               |
| Kostenbeheereenheden                 | Naam van kostenbeheereenheid                                                                                               |
| Dimensies van kostenelement            | Dimensienaam kostenelementen, dimensielidnaam kostenelement en dimensielidbeschrijving kostenelement          |
| Dimensies van kostenobject             | Dimensienaam kostenobject, dimensielidnaam kostenobject en dimensielidbeschrijving kostenobject              |
| Statistische dimensies             | Statistische dimensienaam, statistische dimensielidnaam, statistische dimensielidbeschrijving              |
| Dimensiehiërarchieën kostenobject  | Hiërarchienaam kostenobjectdimensie, hiërarchieniveau kostenobjectdimensie, hiërarchiestructuur kostenobjectdimensie    |
| Hiërarchieën kostenelementdimensie | Hiërarchienaam kostenelementdimensie, hiërarchieniveau kostenelementdimensie, hiërarchiestructuur kostenelementdimensie |
| Statistische dimensiehiërarchieën  | Hiërarchienaam statistische dimensie, hiërarchieniveau statistische dimensie, hiërarchiestructuur statistische dimensie    |
| Transactieversies               | Versienaam                                                                                                         |
| Fiscale kalenders                   | Kalender, kalenderomschrijving                                                                                       |
| Boekjaren                       | Kalenderjaar                                                                                                        |
| Boekperioden                     | Kalenderjaarperiode                                                                                                 |

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)
-   [Beveiliging instellen voor kostprijsboekhoudingsinhoud voor Power BI](setup-security-cost-accounting-content-pack.md)


