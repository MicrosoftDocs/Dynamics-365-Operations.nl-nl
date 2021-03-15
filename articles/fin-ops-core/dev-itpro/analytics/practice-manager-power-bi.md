---
title: Power BI-inhoud Praktijkbeheerder
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Praktijkbeheerder.
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f01109b360b23adf84673e84e6240f8f4431340d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092452"
---
# <a name="practice-manager-power-bi-content"></a>Power BI-inhoud Praktijkbeheerder

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Praktijkbeheerder**. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Praktijkbeheerder** is gemaakt voor praktijkbeheerders en projectmanagers. Het biedt essentiële metrische gegevens die zijn gerelateerd aan de projecten waaraan de organisatie werkt. Het dashboard bevat een overzicht van de projecten en gerelateerde klanten. Een filter op rapportniveau kan worden gebruikt om te rapporteren over specifieke rechtspersonen. Deze Power BI-inhoud haalt gegevens uit de samengevoegde metingen uit de projectboekhouding.

De Power BI-inhoud **Praktijkbeheerder** bevat vijf rapportpagina's: één overzichtspagina en vier pagina's met details van projectkosten, opbrengsten, beheer van verdiende waarde en metrische uurgegevens die worden gesegmenteerd en verdeeld over verschillende dimensies.

Alle bedragen in de inhoud worden weergegeven in de systeemvaluta. U kunt de systeemvaluta instellen op de pagina **Systeemparameters**.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud

De Power BI-inhoud **Praktijkbeheerder** wordt weergegeven in het werkgebied **Projectbeheer**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud

De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de Power BI-inhoud **Praktijkbeheerder**.

| Rapportpagina       | Metrische gegevens |
|-------------------|---------|
| Projectenoverzicht | <ul><li>Gemaakte projecten</li><li>Geraamde projecten</li><li>Onderhanden projecten</li><li>Werkelijke opbrengst per klant</li><li>Brutomarge van budget per project</li><li>Overzicht van beheer van verdiende waarde</li></ul> |
| Kosten              | <ul><li>Werkelijke kosten versus budgetkosten per maand</li><li>Werkelijke kosten versus budgetkosten per jaar</li><li>Werkelijke kosten versus budgetkosten per categorie</li><li>Werkelijke kosten per transactietype</li></ul> |
| Opbrengst           | <ul><li>Werkelijke opbrengst per maand</li><li>Werkelijke opbrengst per postcode</li><li>Werkelijke opbrengst versus budgetopbrengst per categorie</li><li>Werkelijke opbrengst per bedrijfstak klant</li></ul> |
| EVM               | Kosten en planningsprestatie-index per project |
| Uren             | <ul><li>Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen versus budgeturen</li><li>Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen per project</li><li>Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen per resource</li><li>Werkelijke factureerbare urenverhouding per project</li><li>Werkelijke factureerbare urenverhouding per resource</li></ul> |

De grafieken en tegels op al deze rapporten kunnen worden gefilterd en op het dashboard worden vastgemaakt. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). U kunt ook de functionaliteit voor het exporteren van onderliggende gegevens gebruiken om de onderliggende gegevens te exporteren die worden samengevat in een visualisatie.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

De volgende gegevens wordt gebruikt om de rapportpagina's in de Power BI-inhoud **Praktijkbeheerder** te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

In de volgende secties worden de samengevoegde metingen uitgelegd die worden gebruikt in elke entiteit.

### <a name="entity-projectaccountingcube_actualhourutilization"></a>Entiteit: ProjectAccountingCube\_ActualHourUtilization
**Gegevensbron**: ProjEmplTrans

| Belangrijke samengevoegde meting      | Veld                              | Omschrijving |
|--------------------------------|------------------------------------|-------------|
| Werkelijke factureerbare gebruikte uren | Sum(ActualUtilizationBillableRate) | Het totaal van de werkelijke factureerbare gebruikte uren. |
| Werkelijke factureerbare lasturen   | Sum(ActualBurdenBillableRate)      | Het totaal van het werkelijk lastpercentage. |

### <a name="entity-projectaccountingcube_actuals"></a>Entiteit: ProjectAccountingCube\_Actuals
**Gegevensbron**: ProjTransPosting

| Belangrijke samengevoegde meting | Veld              | Omschrijving |
|---------------------------|--------------------|-------------|
| Werkelijke opbrengst            | Sum(ActualRevenue) | Het totaal van de geboekte opbrengst voor alle transacties. |
| Werkelijke kosten               | Sum(ActualCost)    | Het totaal van de geboekte kosten voor alle transactietypen. |

### <a name="entity-projectaccountingcube_customer"></a>Entiteit: ProjectAccountingCube\_Customer
**Gegevensbron**: CustTable

| Belangrijke samengevoegde meting | Veld                                             | Omschrijving |
|---------------------------|---------------------------------------------------|-------------|
| Aantal projecten        | COUNTA(ProjectAccountingCube\_Projects\[PROJECTS\]) | Het aantal beschikbare projecten. |

### <a name="entity-projectaccountingcube_forecasts"></a>Entiteit: ProjectAccountingCube\_Forecasts
**Gegevensbron**: ProjTransBudget

| Belangrijke samengevoegde meting | Veld                  | Omschrijving |
|---------------------------|------------------------|-------------|
| Kosten volgens budget               | Sum(BudgetCost)        | Het totaal van de voorspelde kosten voor alle transactietypen. |
| Opbrengst volgens budget            | Sum(BudgetRevenue)     | Het totaal van de voorspelde transitorische/gefactureerde opbrengsten. |
| Brutomarge volgens budget       | Sum(BudgetGrossMargin) | Het verschil tussen de som van de totale voorspelde opbrengsten en de som van de totale voorspelde kosten. |

### <a name="entity-projectaccountingcube_projectplancostsview"></a>Entiteit: ProjectAccountingCube\_ProjectPlanCostsView
**Gegevensbron**: Project

| Belangrijke samengevoegde meting | Veld                    | Omschrijving |
|---------------------------|--------------------------|-------------|
| Geplande kosten              | Sum(SumOfTotalCostPrice) | De totale kostprijs in ramingen voor alle projecttransactietypen met geplande taken. |

### <a name="entity-projectaccountingcube_projects"></a>Entiteit: ProjectAccountingCube\_Projects
**Gegevensbron**: Project

| Belangrijke samengevoegde meting    | Veld | Omschrijving |
|------------------------------|-------|-------------|
| Kostenprestatie-index       | ProjectAccountingCube\_Projects\[Verdiende waarde\] ÷ ProjectAccountingCube\_Projects\[Totale werkelijke kosten van voltooide taken\] | De berekening van de totale verdiende waarde gedeeld door de totale werkelijke kosten. |
| Planningsprestatie-index   | ProjectAccountingCube\_Projects\[Verdiende waarde\] ÷ ProjectAccountingCube\_Projects\[Totale geplande kosten van voltooide taken\] | De berekening van de totale verdiende waarde gedeeld door de totale geplande kosten. |
| Percentage werk voltooid | Percentage voltooid werk = ProjectAccountingCube\_Projects\[Totale werkelijke kosten van voltooide taken\] ÷ (ProjectAccountingCube\_Projects\[Totale werkelijke kosten van voltooide taken\] + ProjectAccountingCube\_Projects\[Totale geplande kosten van project\] – ProjectAccountingCube\_Projects\[Totale geplande kosten van voltooide taken\]) | Het totaal percentage voltooid werk op basis van de totale werkelijke kosten van voltooide taken en de geplande kosten van het project |
| Werkelijke factureerbare urenverhouding  | ProjectAccountingCube\_Projects\[Totale werkelijke factureerbare gebruikte uren van project\] ÷ (ProjectAccountingCube\_Projects\[Totale werkelijke factureerbare gebruikte uren van project\] + ProjectAccountingCube\_Projects\[Totale werkelijke factureerbare lasturen van project\]) | Het totale aantal factureerbare werkelijke uren, op basis van de gebruikte uren en de lasturen. |
| Verdiende waarde                 | ProjectAccountingCube\_Projects\[Totale geplande kosten van project\] × ProjectAccountingCube\_Projects\[Percentage voltooid werk\] | De totale geplande kosten, vermenigvuldigd met het percentage voltooid werk. |

### <a name="entity-projectaccountingcube_totalestimatedcosts"></a>Entiteit: ProjectAccountingCube\_TotalEstimatedCosts 
**Gegevensbron**: ProjTable

| Belangrijke samengevoegde meting       | Veld               | Omschrijving |
|---------------------------------|---------------------|-------------|
| Geplande kosten voltooide activiteit | Sum(TotalCostPrice) | De totale kostprijs in ramingen voor alle projecttransactietypen met voltooide taken. |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]