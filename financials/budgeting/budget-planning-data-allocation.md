---
title: Gegevenstoewijzing voor budgetplanning
description: In dit artikel worden de verschillende toewijzingsmethoden beschreven die beschikbaar zijn in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition en hoe ze kunnen worden gebruikt.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fc85775a27a160e951593bb9d40a6294af3ca329
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---

# <a name="budget-planning-data-allocation"></a>Gegevenstoewijzing voor budgetplanning

[!include[banner](../includes/banner.md)]


In dit artikel worden de verschillende toewijzingsmethoden beschreven die beschikbaar zijn in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition en hoe ze kunnen worden gebruikt.  

U kunt de gegevens in een budgetplan op verschillende manieren verspreiden om de verwachte bedragen nauwkeurig af te beelden.

## <a name="allocation-methods"></a>Toewijzingsmethodes
Drie toewijzingsmethoden (Toewijzen aan perioden, Toewijzen aan dimensies en Grootboektoewijzingsregels gebruiken) kunnen de budgetplanregels maken die op regels in hetzelfde budgetplan zijn gebaseerd. Drie andere methoden (Samenvoegen, Verdelen en Kopiëren uit budgetplan) kunnen budgetplanregels maken in andere budgetplannen. Voor alle zes toewijzingsmethoden geeft u het doelscenario op. Het doelscenario kan gelijk zijn aan het bronscenario of van het bronscenario verschillen. Bovendien kunt u opgeven of de nieuwe regels aan het budgetplan worden toegevoegd of de huidige regels in het budgetplan vervangen.

[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Toewijzen aan perioden** – Een periodetoewijzingscategorie wordt gebruikt om de budgetplanregels toe te wijzen vanuit het bronbudgetplanscenario aan perioden in het doelscenario. Het bronbedrag is toegewezen aan meerdere regels in het doelscenario, op basis van het percentage en de datum die zijn opgegeven in de periodetoewijzingscategorie.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Toewijzen aan dimensies** – De budgetplanregels worden toegewezen van het bronbudgetplanningsscenario aan een of meer regels in het doelscenario, op basis van de percentages en financiële dimensies die in een geselecteerde budgettoewijzingstermijn worden gedefinieerd.           

![AggregateChart](./media/aggregatechart-300x230.png)
**Samenvoegen** - De budgetplanregels worden samengevoegd vanuit het bronbudgetplanscenario in de gekoppelde (onderliggende) budgetplannen met het doelscenario in het bovenliggende budgetplan. Dankzij deze methode kunnen budgetbedragen die op een lager niveau in de organisatie zijn voorbereid op een hoger niveau worden geconsolideerd.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Verdelen** – De budgetplanregels worden verdeeld van het bronbudgetplanningsscenario in het bovenliggende budgetplan naar het doelscenario in de gekoppelde (onderliggende) budgetplannen, op basis van de financiële dimensies van de organisatie-eenheden van de gekoppelde plannen. Dankzij deze methode kunnen budgetbedragen die op een hoger niveau in de organisatie zijn voorbereid worden verdeeld voor meer gelokaliseerde controle.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Grootboektoewijzingsregels gebruiken** - De budgetplanregels worden verdeeld vanuit het bronbudgetplanningsscenario naar het doelscenario, op basis van de grootboektoewijzingsregel die is geselecteerd. 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopiëren uit budgetplan** – Zoals in de toewijzingsmethode Verdelen, worden de budgetplanregels gemaakt in het doel, op basis van regels in een gerelateerd budgetplan. Voor deze rapportagemethode moet het bronbudgetplan echter geen bovenliggende zijn maar kan deze zich op elk hoger niveau in de budgetplanhiërarchie bevinden. Deze toewijzingsmethode is handig als de geconsolideerde bedragen oorspronkelijk op een veel hoger niveau worden gebudgetteerd, en moeten worden overgebracht naar een lager niveau van de organisatie voor gedetailleerde controle en correctie voordat deze goedkeuring op het hoogste niveau kunnen ontvangen.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Gebruik van toewijzingsmethoden in een budgetplan
Om toewijzingen uit te voeren op de pagina van het budgetplan, selecteert u de regels die u wilt toewijzen en klikt u vervolgens op **Budget toewijzen**.

[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Selecteer vervolgens een toewijzingsmethode. De resterende velden worden vervolgens ingesteld, op basis van de methode die u hebt geselecteerd. Deze velden bevatten de bron en het doel van de gegevens van het budgetplan en een optie waarmee u de bron met een bepaalde factor kunt vermenigvuldigen wanneer de doelbedragen zijn gemaakt, om bulkcorrectie te vereenvoudigen. U kunt ook de optie **Toevoegen aan plan** instellen. Selecteer **Nee** om de bestaande budgetplanregels te vervangen of selecteer **Ja** om de bestaande budgetplanregels te behouden en nieuwe regels toe te voegen voor de toegewezen bedragen.

## <a name="automating-allocations-during-a-workflow"></a>Toewijzingen automatiseren tijdens een workflow
Met één krachtige functie kunnen toewijzingen automatisch worden uitgevoerd als onderdeel van een budgetplanningsworkflow. Als een budgetplan door de workflow verplaatst, kunnen de geautomatiseerde taken een toewijzing aanroepen in een opgegeven budgetplanningsfase. 

Als u geautomatiseerde toewijzing wilt instellen, moet u eerst een toewijzingsplan maken op de pagina **Configuratie budgetplanning**. Het toewijzingsplan definieert de toewijzingsmethode die wordt gebruikt wanneer de geautomatiseerde toewijzing wordt uitgevoerd en de waarden van de verschillende toewijzingsopties (raadpleeg de vorige sectie voor omschrijvingen). 

Maak vervolgens een fasetoewijzing op de pagina **Configuratie budgetplanning**. De fasetoewijzing wijst een toewijzingsschema toe aan de budgetplanningsworkflow en -fase. 

Voeg tot slot een geautomatiseerde taak toe voor de toewijzing van de budgetplanningsfase op de gewenste workflowfase. In het volgende voorbeeld zijn twee toewijzingen van de budgetplanningsfase (in rood aangegeven) ingevoegd in de workflow.

[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)




