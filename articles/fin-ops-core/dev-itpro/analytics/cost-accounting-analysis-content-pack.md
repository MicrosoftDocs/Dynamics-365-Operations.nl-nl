---
title: Analyse van kostprijsboekhouding Power BI-inhoud
description: In dit onderwerp wordt beschreven wat wordt opgenomen in de Power BI-inhoud voor de analyse van kostprijsboekhouding.
author: AndersGirke
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d3b8832e5a5612fd0311811f43454689d5b274c36404b4fb92b710411d45e573
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747364"
---
# <a name="cost-accounting-analysis-power-bi-content"></a>Analyse van kostprijsboekhouding Power BI-inhoud

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Analyse van kostprijsboekhouding**. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Analyse kostprijsboekhouding** is bedoeld voor kostencontrollers of iemand anders die verantwoordelijk is voor het uitvoeren van het kostenbeheer van een organisatie. Het bevat de belangrijkste metrische gegevens, zoals kosten, magnitude en kostentarief op basis van werkelijke kosten, budgetkosten en flexibele budgetkosten. Hierin worden transactiegegevens uit de module **Kostprijsboekhouding** gebruikt en wordt een samengevoegde weergave van kosten verschaft voor de gehele organisatie in één rapportagevaluta. Managers kunnen de gegevens filteren op basis van kostenobjecten om kostenbeheer van hun organisatie-eenheden uit te voeren, zelfs als de organisatie meerdere rechtspersonen heeft.

Omdat de inhoud **Analyse kostprijsboekhouding** afwijkingen tussen de werkelijke en gebudgetteerde kosten markeert, kunnen managers worden geïnformeerd over positieve en negatieve trends voor hun operationele eenheden. Managers kunnen inzoomen op de kostenelementhiërarchieën of op afzonderlijke kostenelementen. Op deze manier krijgen managers een gedetailleerd inzicht in de wijze waarop kostenafwijkingen hebben plaatsgevonden, en kunnen vervolgens doeltreffende actie ondernemen.

Met de inhoud **Analyse kostprijsboekhouding** kunnen kostenaccountants analyseren hoe kosten de kostenobjecten van de gehele organisatie doorlopen.

Zie voor meer informatie over kostprijsboekhouding [Startpagina kostprijsboekhouding](../../../finance/cost-accounting/cost-accounting-home-page.md).

Als u beveiliging op toegangsniveau in kostprijsboekhouding definieert en combineert met beveiliging op rijniveau in Power BI, kunt u alle kostenobjecteigenaren toegang verlenen tot de Power BI-inhoud voor **Analyse kostprijsboekhouding**. Alle gegevens in de visualisaties worden vervolgens gefilterd op basis van het toegangsniveau dat in de kostprijsboekhouding wordt beheerd. Zie [Beveiliging instellen voor de kostprijsboekhoudingsanalyse van Power BI-inhoud](setup-security-cost-accounting-content-pack.md) voor meer informatie over beveiliging op toegangsniveau en beveiliging op rijniveau .

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud
U vindt de Power BI-inhoud voor **Analyse kostprijsboekhouding** in de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).

Let erop dat u de inhoud **Analyse kostprijsboekhouding** downloadt die geldt voor de versie van Microsoft Dynamics 365 die u gebruikt.

> [!NOTE]
> KB 4011327 is vereist voor deze Power BI-inhoud. Nadat u bent aangemeld bij LCS, hebt u toegang tot de KB op <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

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
De volgende gegevens worden gebruikt om de rapportpagina's in de Power BI-inhoud **Analyse kostprijsboekhouding** in te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

De volgende belangrijke samengevoegde metingen worden gebruikt als de basis van de inhoud.

| Entiteit                  | Belangrijke samengevoegde meting | Gegevensbron voor Dynamics 365      | Veld     | Omschrijving                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Kostprijsboekhoudingsposten | SUM(Amount)               | CAMDATAAggregatedCostEntry        | Bedrag    | Het bedrag in de grootboekvaluta voor de kostprijsboekhouding. |
| Statistische boekingen     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry | Magnitude |                                                    |

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]