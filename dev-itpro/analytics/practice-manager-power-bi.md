---
title: Praktijkbeheerder - Power BI-inhoud
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud voor Praktijkbeheerder. In dit onderwerp wordt uitgelegd hoe u toegang kunt krijgen tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Praktijkbeheerder - Power BI-inhoud

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud voor **Praktijkbeheerder**. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De **Praktijkbeheerder** Power BI-inhoud is gemaakt voor praktijkbeheerders en projectmanagers. Het biedt essentiële metrische gegevens die zijn gerelateerd aan de projecten waaraan de organisatie werkt. Het dashboard bevat een overzicht van de projecten en gerelateerde klanten. Een filter op rapportniveau kan worden gebruikt om te rapporteren over specifieke rechtspersonen. Deze Power BI-inhoud haalt gegevens uit de samengevoegde metingen van projectadministratie voor Microsoft Dynamics 365 for Operations.

De **Praktijkbeheerder** Power BI-inhoud bevat vijf rapportpagina's: één overzichtspagina en vier pagina's met details van projectkosten, opbrengsten, beheer van verdiende waarde en metrische uurgegevens die worden gesegmenteerd en verdeeld over verschillende dimensies.

Alle bedragen in de inhoud worden weergegeven in de systeemvaluta. U kunt de systeemvaluta instellen op de pagina **Systeemparameters**.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen

U vindt de **Praktijkbeheerder** Power BI-inhoud in de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u het inhoudspakket downloadt en koppelt aan uw Microsoft Dynamics 365 for Operations-gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud

De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de **Praktijkbeheerder** Power BI-inhoud.

| Rapportpagina                                          | Metrische gegevens               |
|------------------------------------------------------|-----------------------------------------------|
| Dashboard  | Gemaakte projecten<br>Geraamde projecten<br>Onderhanden projecten<br>Aantal projecten per fase<br>Aantal projecten per plaats<br>Werkelijke opbrengst per klant<br>Brutomarge van budget per project<br>Overzicht van beheer van verdiende waarde |
| Kosten                                                 | Werkelijke kosten versus budgetkosten per maand<br>Werkelijke kosten versus budgetkosten per jaar<br>Werkelijke kosten versus budgetkosten per categorie<br>Werkelijke kosten per transactietype       |
| Opbrengst                                              | Werkelijke opbrengst per maand<br>Werkelijke opbrengst per postcode<br>Werkelijke opbrengst versus budgetopbrengst per categorie<br>Werkelijke opbrengst per bedrijfstak klant        |
| EVM                                                  | Kosten en planningsprestatie-index per project                 |
| Uren                                                | Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen versus budgeturen<br>Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen per project<br>Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen per resource<br>Werkelijke factureerbare urenverhouding per project<br>Werkelijke factureerbare urenverhouding per resource |

De grafieken en tegels op al deze rapporten kunnen worden gefilterd en op het dashboard worden vastgemaakt. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). U kunt ook de functionaliteit voor het exporteren van onderliggende gegevens gebruiken om de onderliggende gegevens te exporteren die worden samengevat in een visualisatie.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

Dynamics 365 for Operations-gegevens worden gebruikt voor het vullen van de rapportpagina's in de **Praktijkbeheerder** Power BI-inhoud. Deze gegevens worden vertegenwoordigd als samengevoegde metingen die worden klaargezet in de Entiteitopslag. Dit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

In de volgende secties worden de samengevoegde metingen uitgelegd die worden gebruikt in elke entiteit.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Entiteit: ProjectAccountingCube_ActualHourUtilization
**Gegevensbron**: ProjEmplTrans

| Belangrijke samengevoegde meting                | Veld                                | Omschrijving                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Totaal van werkelijke factureerbare gebruikte uren |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Totaal van werkelijk lastpercentage             |

### <a name="entity-projectaccountingcubeactuals"></a>Entiteit: ProjectAccountingCube_Actuals
**Gegevensbron**: ProjTransPosting

| Belangrijke samengevoegde meting                | Veld                                | Omschrijving                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Totaal van geboekte opbrengst voor alle transacties |   
| ActualCost   |                             Sum(ActualCost)           |    Totaal van geboekte kosten voor alle transactietypen    |

### <a name="entity-projectaccountingcubecustomer"></a>Entiteit: ProjectAccountingCube_Customer
**Gegevensbron**: CustTable

| Belangrijke samengevoegde meting                | Veld                                | Omschrijving                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Aantal projecten        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Aantal beschikbare projecten    |


### <a name="entity-projectaccountingcubeforecasts"></a>Entiteit: ProjectAccountingCube_Forecasts
**Gegevensbron**: ProjTransBudget

| Belangrijke samengevoegde meting                | Veld                                | Omschrijving                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Totaal van voorspelde kosten voor alle transactietypen     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Totaal van voorspelde transitorische/gefactureerde opbrengsten         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Verschil tussen de som van de totale voorspelde opbrengsten en de som van de totale voorspelde kosten

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Entiteit: ProjectAccountingCube_ProjectPlanCostsView
**Gegevensbron**: Project

| Belangrijke samengevoegde meting                | Veld                                | Omschrijving                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Totale kostprijs in ramingen voor alle projecttransactietypen met geplande taken |

### <a name="entity-projectaccountingcubeprojects"></a>Entiteit: ProjectAccountingCube_Projects
**Gegevensbron**: Project

| Belangrijke samengevoegde meting                | Veld                                | Omschrijving                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Kostenprestatie-index  |ProjectAccountingCube_Projects[Verdiende waarde] / ProjectAccountingCube_Projects[Totale werkelijke kosten van voltooide taken] |     Berekening van de totale verdiende waarde gedeeld door totale werkelijke kosten|
|  Planningsprestatie-index |ProjectAccountingCube_Projects[Verdiende waarde] / ProjectAccountingCube_Projects[Totale geplande kosten van voltooide taken]|Berekening van de totale verdiende waarde gedeeld door totale geplande kosten |
|Percentage werk voltooid |Percentage voltooid werk = ProjectAccountingCube_Projects[Totale werkelijke kosten van voltooide taken] / (ProjectAccountingCube_Projects[Totale werkelijke kosten van voltooide taken] + ProjectAccountingCube_Projects[Totale geplande kosten van project] - ProjectAccountingCube_Projects[Totale geplande kosten van voltooide taken])|Totaal percentage voltooid werk op basis van de totale werkelijke kosten van voltooide taken en geplande kosten van het project|
|Werkelijke factureerbare urenverhouding van project|ProjectAccountingCube_Projects[Totale werkelijke factureerbare gebruikte uren van project] / (ProjectAccountingCube_Projects[Totale werkelijke factureerbare gebruikte uren van project] + ProjectAccountingCube_Projects[Totale werkelijke factureerbare lasturen van project])|Totale werkelijke factureerbare uren op basis van gebruikte uren + lasturen|
|Verdiende waarde|ProjectAccountingCube_Projects[Totale geplande kosten van project] * ProjectAccountingCube_Projects[Percentage voltooid werk]|Totale geplande kosten vermenigvuldigen met percentage voltooid werk|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Entiteit: ProjectAccountingCube_TotalEstimatedCosts 
**Gegevensbron**: ProjTable

| Belangrijke samengevoegde meting                | Veld                                | Omschrijving                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Totale kostprijs in ramingen voor alle projecttransactietypen met voltooide taken|

## <a name="additional-resources"></a>Aanvullende resources

Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

- [Gegevensentiteiten](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Power BI-integratie voor werkgebieden configureren](configure-power-bi-integration.md)

