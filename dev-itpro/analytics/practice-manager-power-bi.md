---
title: Praktijkbeheerder - Power BI-inhoud
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud voor Praktijkbeheerder. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 993e88703f19dbeec435d07a4599cbbfcda563bc
ms.openlocfilehash: b63e31f3e4993c1fda229a54b4e5ef2fed824355
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017


---

# <a name="practice-manager-power-bi-content"></a>Praktijkbeheerder - Power BI-inhoud

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud voor **Praktijkbeheerder**. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De **Praktijkbeheerder** Power BI-inhoud is gemaakt voor praktijkbeheerders en projectmanagers. Het biedt essentiële metrische gegevens die zijn gerelateerd aan de projecten waaraan de organisatie werkt. Het dashboard bevat een overzicht van de projecten en gerelateerde klanten. Een filter op rapportniveau kan worden gebruikt om te rapporteren over specifieke rechtspersonen. Deze Power BI-inhoud haalt gegevens uit het samengevoegde metingen uit de projectboekhouding.

De Power BI-inhoud **Praktijkbeheerder** bevat vijf rapportpagina's: één overzichtspagina en vier pagina's met details van projectkosten, opbrengsten, beheer van verdiende waarde en metrische uurgegevens die worden gesegmenteerd en verdeeld over verschillende dimensies.

Alle bedragen in de inhoud worden weergegeven in de systeemvaluta. U kunt de systeemvaluta instellen op de pagina **Systeemparameters**.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
Als u werkt met de update voor juli 2017 van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, vindt u de Power BI-inhoud voor **Praktijkbeheerder** in het werkgebied **Projectbeheer**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud

De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de **Praktijkbeheerder** Power BI-inhoud.

| Rapportpagina       | Metrische gegevens |
|-------------------|---------|
| Projectenoverzicht | <ul><li>Gemaakte projecten</li><li>Geraamde projecten</li><li>Onderhanden projecten</li><li>Aantal projecten per fase</li><li>Aantal projecten per plaats</li><li>Werkelijke opbrengst per klant</li><li>Brutomarge van budget per project</li><li>Overzicht van beheer van verdiende waarde</li></ul> |
| Kosten              | <ul><li>Werkelijke kosten versus budgetkosten per maand</li><li>Werkelijke kosten versus budgetkosten per jaar</li><li>Werkelijke kosten versus budgetkosten per categorie</li><li>Werkelijke kosten per transactietype</li></ul> |
| Opbrengst           | <ul><li>Werkelijke opbrengst per maand</li><li>Werkelijke opbrengst per postcode</li><li>Werkelijke opbrengst versus budgetopbrengst per categorie</li><li>Werkelijke opbrengst per bedrijfstak klant</li></ul> |
| EVM               | Kosten en planningsprestatie-index per project |
| Uren             | <ul><li>Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen versus budgeturen</li><li>Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen per project</li><li>Werkelijke factureerbare gebruikte uren versus werkelijke factureerbare lasturen per resource</li><li>Werkelijke factureerbare urenverhouding per project</li><li>Werkelijke factureerbare urenverhouding per resource</li></ul> |

De grafieken en tegels op al deze rapporten kunnen worden gefilterd en op het dashboard worden vastgemaakt. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). U kunt ook de functionaliteit voor het exporteren van onderliggende gegevens gebruiken om de onderliggende gegevens te exporteren die worden samengevat in een visualisatie.

## <a name="extending-the-power-bi-content"></a>De Power BI-inhoud uitbreiden
Met behulp van de inhoudpakketten die beschikbaar zijn in Microsoft Dynamics Lifecycle Services (LCS) kunt u grondige analyses verschaffen aan personen die zich niet bij Microsoft Dynamics 365 aanmelden. U kunt deze inhoudpacks wijzigen zodat ze andere rapporten of visuele elementen bevatten, en deze vervolgens publiceren in uw Power BI.com-tenant voor analyse. 

U vindt de Power BI-inhoud **Praktijkbeheerder** in de bibliotheek voor gedeelde materialen in LCS. Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md). Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

Let erop dat u de inhoud **Praktijkbeheerder** downloadt, die van toepassing is voor de versie van Dynamics 365 die u gebruikt.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

De volgende gegevens wordt gebruikt om de rapportpagina's in de Power BI-inhoud **Praktijkbeheerder** te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

In de volgende secties worden de samengevoegde metingen uitgelegd die worden gebruikt in elke entiteit.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Entiteit: ProjectAccountingCube_ActualHourUtilization
**Gegevensbron**: ProjEmplTrans

| Belangrijke samengevoegde meting      | Veld                              | Omschrijving | 
|--------------------------------|------------------------------------|-------------|
| Werkelijke factureerbare gebruikte uren | Sum(ActualUtilizationBillableRate) | Het totaal van de werkelijke factureerbare gebruikte uren. |
| Werkelijke factureerbare lasturen   | Sum(ActualBurdenBillableRate)      | Het totaal van het werkelijk lastpercentage. |

### <a name="entity-projectaccountingcubeactuals"></a>Entiteit: ProjectAccountingCube_Actuals
**Gegevensbron**: ProjTransPosting

| Belangrijke samengevoegde meting | Veld              | Omschrijving | 
|---------------------------|--------------------|-------------|
| Werkelijke opbrengst            | Sum(ActualRevenue) | Het totaal van de geboekte opbrengst voor alle transacties. |   
| Werkelijke kosten               | Sum(ActualCost)    | Het totaal van de geboekte kosten voor alle transactietypen. |

### <a name="entity-projectaccountingcubecustomer"></a>Entiteit: ProjectAccountingCube_Customer
**Gegevensbron**: CustTable

| Belangrijke samengevoegde meting | Veld                                            | Omschrijving | 
|---------------------------|--------------------------------------------------|-------------|
| Aantal projecten        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Het aantal beschikbare projecten. |


### <a name="entity-projectaccountingcubeforecasts"></a>Entiteit: ProjectAccountingCube_Forecasts
**Gegevensbron**: ProjTransBudget

| Belangrijke samengevoegde meting | Veld                  | Omschrijving | 
|---------------------------|------------------------|-------------|
| Kosten volgens budget               | Sum(BudgetCost)        | Het totaal van de voorspelde kosten voor alle transactietypen. |
| Opbrengst volgens budget            | Sum(BudgetRevenue)     | Het totaal van de voorspelde transitorische/gefactureerde opbrengsten.  |
| Brutomarge volgens budget       | Sum(BudgetGrossMargin) | Het verschil tussen de som van de totale voorspelde opbrengsten en de som van de totale voorspelde kosten. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Entiteit: ProjectAccountingCube_ProjectPlanCostsView
**Gegevensbron**: Project

| Belangrijke samengevoegde meting | Veld                    | Omschrijving | 
|---------------------------|--------------------------|-------------|
| Geplande kosten              | Sum(SumOfTotalCostPrice) | De totale kostprijs in ramingen voor alle projecttransactietypen met geplande taken. |

### <a name="entity-projectaccountingcubeprojects"></a>Entiteit: ProjectAccountingCube_Projects
**Gegevensbron**: Project

| Belangrijke samengevoegde meting    | Veld | Omschrijving | 
|------------------------------|-------|-------------|
| Kostenprestatie-index       | ProjectAccountingCube_Projects[Verdiende waarde] / ProjectAccountingCube_Projects[Totale werkelijke kosten van voltooide taken] | De berekening van de totale verdiende waarde gedeeld door de totale werkelijke kosten. |
| Planningsprestatie-index   | ProjectAccountingCube_Projects[Verdiende waarde] / ProjectAccountingCube_Projects[Totale geplande kosten van voltooide taken] | De berekening van de totale verdiende waarde gedeeld door de totale geplande kosten. |
| Percentage werk voltooid | Percentage voltooid werk = ProjectAccountingCube_Projects[Totale werkelijke kosten van voltooide taken] / (ProjectAccountingCube_Projects[Totale werkelijke kosten van voltooide taken] + ProjectAccountingCube_Projects[Totale geplande kosten van project] - ProjectAccountingCube_Projects[Totale geplande kosten van voltooide taken]) | Het totaal percentage voltooid werk op basis van de totale werkelijke kosten van voltooide taken en de geplande kosten van het project |
| Werkelijke factureerbare urenverhouding  | ProjectAccountingCube_Projects[Totale werkelijke factureerbare gebruikte uren van project] / (ProjectAccountingCube_Projects[Totale werkelijke factureerbare gebruikte uren van project] + ProjectAccountingCube_Projects[Totale werkelijke factureerbare lasturen van project]) | Het totale aantal factureerbare werkelijke uren, op basis van de gebruikte uren en de lasturen. |
| Verdiende waarde                 | ProjectAccountingCube_Projects[Totale geplande kosten van project] * ProjectAccountingCube_Projects[Percentage voltooid werk] | De totale geplande kosten, vermenigvuldigd met het percentage voltooid werk. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Entiteit: ProjectAccountingCube_TotalEstimatedCosts 
**Gegevensbron**: ProjTable

| Belangrijke samengevoegde meting       | Veld               | Omschrijving | 
|---------------------------------|---------------------|-------------|
| Geplande kosten voltooide activiteit | Sum(TotalCostPrice) | De totale kostprijs in ramingen voor alle projecttransactietypen met voltooide taken. |

