---
title: Projectramingen rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om projectuurschattingen en projectonkostenschattingen rechtstreeks van Microsoft Dynamics 365 Project Service Automation naar Dynamics 365 Finance te synchroniseren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770284"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3e922-103">Projectramingen rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3e922-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3e922-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om projectuurschattingen en projectonkostenschattingen rechtstreeks van Dynamics 365 Project Service Automation naar Dynamics 365 Finance te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="3e922-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="3e922-105">Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling is beschikbaar in versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="3e922-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="3e922-106">Integratie van werkelijke waarden is mogelijk in versie 8.0.1 of hoger.</span><span class="sxs-lookup"><span data-stu-id="3e922-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="3e922-107">Gegevensstroom voor Project Service Automation naar Finance</span><span class="sxs-lookup"><span data-stu-id="3e922-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="3e922-108">De integratieoplossing voor Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance.</span><span class="sxs-lookup"><span data-stu-id="3e922-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="3e922-109">De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over projectuurramingen en projectkostenramingen van Project Service Automation naar Finance mogelijk.</span><span class="sxs-lookup"><span data-stu-id="3e922-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3e922-110">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.</span><span class="sxs-lookup"><span data-stu-id="3e922-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="3e922-111">[![Gegevensstroom voor Project Service Automation-integratie met Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="3e922-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="3e922-112">Ramingen voor projecturen</span><span class="sxs-lookup"><span data-stu-id="3e922-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="3e922-113">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="3e922-113">Template and tasks</span></span>

<span data-ttu-id="3e922-114">Selecteer voor toegang tot de beschikbare sjablonen in het Microsoft Power Apps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3e922-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3e922-115">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projectuurramingen vanuit Project Service Automation naar Finance:</span><span class="sxs-lookup"><span data-stu-id="3e922-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3e922-116">**Naam van de sjabloon in Gegevensintegratie:** Projectuurramingen (PSA naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3e922-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3e922-117">**Naam van de taken in het project:**</span><span class="sxs-lookup"><span data-stu-id="3e922-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3e922-118">Transactierelaties</span><span class="sxs-lookup"><span data-stu-id="3e922-118">Transaction relationships</span></span>
    - <span data-ttu-id="3e922-119">Onkostenramingen</span><span class="sxs-lookup"><span data-stu-id="3e922-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="3e922-120">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="3e922-120">Entity set</span></span>

| <span data-ttu-id="3e922-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3e922-121">Project Service Automation</span></span> | <span data-ttu-id="3e922-122">Financiën</span><span class="sxs-lookup"><span data-stu-id="3e922-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="3e922-123">Projecttaken</span><span class="sxs-lookup"><span data-stu-id="3e922-123">Project tasks</span></span>              | <span data-ttu-id="3e922-124">Integratie-entiteit voor projectuurramingen</span><span class="sxs-lookup"><span data-stu-id="3e922-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="3e922-125">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="3e922-125">Entity flow</span></span>

<span data-ttu-id="3e922-126">Projectuurramingen worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance als projectuurprognoses.</span><span class="sxs-lookup"><span data-stu-id="3e922-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3e922-127">Vereisten</span><span class="sxs-lookup"><span data-stu-id="3e922-127">Prerequisites</span></span>

<span data-ttu-id="3e922-128">Voordat synchronisatie van projectuurramingen kan plaatsvinden, moet u projecten, projecttaken en projectkostentransactiecategorieën synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="3e922-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="3e922-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="3e922-129">Power Query</span></span>

<span data-ttu-id="3e922-130">In de sjabloon voor de raming van projecturen moet u Microsoft Power Query voor Excel gebruiken om het volgende te doen:</span><span class="sxs-lookup"><span data-stu-id="3e922-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="3e922-131">De standaardprognosemodel-id instellen die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.</span><span class="sxs-lookup"><span data-stu-id="3e922-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="3e922-132">Alle resourcespecifieke records in de taak uitfilteren waarvoor integratie tot uurramingen zal mislukken.</span><span class="sxs-lookup"><span data-stu-id="3e922-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="3e922-133">Alle lege transactiecategorierijen uitfilteren.</span><span class="sxs-lookup"><span data-stu-id="3e922-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="3e922-134">Als u deze taak niet uitvoert, kan dit leiden tot onjuiste uurramingen.</span><span class="sxs-lookup"><span data-stu-id="3e922-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="3e922-135">De standaardprognosemodel-id instellen</span><span class="sxs-lookup"><span data-stu-id="3e922-135">Set the default forecast model ID</span></span>

<span data-ttu-id="3e922-136">Als u de standaardprognosemodel-id in de sjabloon wilt bijwerken, klikt u op de pijl **Toewijzen** om de toewijzing te openen.</span><span class="sxs-lookup"><span data-stu-id="3e922-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3e922-137">Selecteer vervolgens de koppeling **Geavanceerde query en filtering**.</span><span class="sxs-lookup"><span data-stu-id="3e922-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="3e922-138">Als u de standaardsjabloon Project-uurramingen (PSA naar Fin and Ops) gebruikt, selecteert u de **Ingevoegde voorwaarde** in de lijst **Toegepaste stappen**.</span><span class="sxs-lookup"><span data-stu-id="3e922-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="3e922-139">Vervang in de vermelding **Functie** de waarde **O\_forecast** door de naam van de prognosemodel-id die moet worden gebruikt met de integratie.</span><span class="sxs-lookup"><span data-stu-id="3e922-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="3e922-140">De standaardsjabloon heeft een prognosemodel-ID vanuit de demonstratiegegevens.</span><span class="sxs-lookup"><span data-stu-id="3e922-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="3e922-141">Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3e922-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="3e922-142">Selecteer in Power Query de optie **Voorwaardelijke kolom toevoegen** en voer een naam voor de nieuwe kolom in, zoals **Model-id**.</span><span class="sxs-lookup"><span data-stu-id="3e922-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="3e922-143">Voer de voorwaarde in voor de kolom waarin als Projecttaak niet null is, dan \<voer de prognosemodel-id in\>; anders null.</span><span class="sxs-lookup"><span data-stu-id="3e922-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="3e922-144">Resourcespecifieke records uitfilteren</span><span class="sxs-lookup"><span data-stu-id="3e922-144">Filter out resource-specific records</span></span>

<span data-ttu-id="3e922-145">De sjabloon voor projectuurramingen (PSA naar Fin and Ops) heeft een standaardfilter waarmee resourcespecifieke records worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="3e922-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="3e922-146">Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3e922-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="3e922-147">Selecteer de koppeling **Geavanceerde query en filtering** om te filteren op de kolom **msdyn\_islinetask** zodat alleen **onware** records worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="3e922-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="3e922-148">Lege transactiecategorierijen uitfilteren</span><span class="sxs-lookup"><span data-stu-id="3e922-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="3e922-149">U moet een filter toevoegen om rijen te verwijderen die lege transactiecategorieën bevat.</span><span class="sxs-lookup"><span data-stu-id="3e922-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="3e922-150">Deze taak is verplicht, ongeacht of u de standaardsjabloon gebruikt of uw eigen sjabloon maakt.</span><span class="sxs-lookup"><span data-stu-id="3e922-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="3e922-151">Dit filter verwijdert overzichtrijen die afkomstig zijn van Project Service Automation die ertoe kunnen leiden dat de uurprognoses in Finance onjuist zijn.</span><span class="sxs-lookup"><span data-stu-id="3e922-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="3e922-152">Selecteer de koppeling **Geavanceerde query en filtering** om null-records uit te filteren in de kolom **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="3e922-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3e922-153">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="3e922-153">Template mapping in Data integration</span></span>

<span data-ttu-id="3e922-154">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="3e922-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="3e922-155">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="3e922-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3e922-156">[![Sjabloontoewijzing](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3e922-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="3e922-157">Projectkostenramingen</span><span class="sxs-lookup"><span data-stu-id="3e922-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="3e922-158">Sjabloon en taken</span><span class="sxs-lookup"><span data-stu-id="3e922-158">Template and tasks</span></span>

<span data-ttu-id="3e922-159">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projectkostenramingen vanuit Project Service Automation naar Finance:</span><span class="sxs-lookup"><span data-stu-id="3e922-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3e922-160">**Naam van de sjabloon in Gegevensintegratie:** Projectkostenramingen (PSA naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3e922-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3e922-161">**Naam van de taken in het project:**</span><span class="sxs-lookup"><span data-stu-id="3e922-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3e922-162">Transactierelaties</span><span class="sxs-lookup"><span data-stu-id="3e922-162">Transaction relationships</span></span> 
    - <span data-ttu-id="3e922-163">Onkostenramingen</span><span class="sxs-lookup"><span data-stu-id="3e922-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="3e922-164">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="3e922-164">Entity set</span></span>

| <span data-ttu-id="3e922-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3e922-165">Project Service Automation</span></span> | <span data-ttu-id="3e922-166">Financiën</span><span class="sxs-lookup"><span data-stu-id="3e922-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="3e922-167">Transactieverbindingen</span><span class="sxs-lookup"><span data-stu-id="3e922-167">Transaction Connections</span></span>    | <span data-ttu-id="3e922-168">Integratie-entiteit voor projectransactierelaties</span><span class="sxs-lookup"><span data-stu-id="3e922-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="3e922-169">Ramingsregels</span><span class="sxs-lookup"><span data-stu-id="3e922-169">Estimate Lines</span></span>             | <span data-ttu-id="3e922-170">Integratie-entiteit voor projectkostenramingen</span><span class="sxs-lookup"><span data-stu-id="3e922-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="3e922-171">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="3e922-171">Entity flow</span></span>

<span data-ttu-id="3e922-172">Projectkostenramingen worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance als projectkostenprognoses.</span><span class="sxs-lookup"><span data-stu-id="3e922-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3e922-173">Vereisten</span><span class="sxs-lookup"><span data-stu-id="3e922-173">Prerequisites</span></span>

<span data-ttu-id="3e922-174">Voordat synchronisatie van projectkostenramingen kan plaatsvinden, moet u projecten, projecttaken en projectkostentransactiecategorieën synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="3e922-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="3e922-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="3e922-175">Power Query</span></span>

<span data-ttu-id="3e922-176">In de projectkostenramingssjabloon moet u Power Query gebruiken om de volgende taken uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="3e922-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="3e922-177">Filteren om alleen onkostenramingsrecords op te nemen.</span><span class="sxs-lookup"><span data-stu-id="3e922-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="3e922-178">De standaardprognosemodel-id instellen die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.</span><span class="sxs-lookup"><span data-stu-id="3e922-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="3e922-179">De factureringstypen transformeren.</span><span class="sxs-lookup"><span data-stu-id="3e922-179">Transform the billing types.</span></span>
- <span data-ttu-id="3e922-180">De transactietypen transformeren.</span><span class="sxs-lookup"><span data-stu-id="3e922-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="3e922-181">Filteren om alleen onkostenramingsregels op te nemen</span><span class="sxs-lookup"><span data-stu-id="3e922-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="3e922-182">De sjabloon voor projectonkostenramingen (PSA naar Fin and Ops) heeft een standaardfilter waarmee alleen onkostenregels in de integratie worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="3e922-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="3e922-183">Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3e922-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="3e922-184">Selecteer de taak **Transactierelaties** en klik vervolgens op de pijl **Toewijzen** om de toewijzing te openen.</span><span class="sxs-lookup"><span data-stu-id="3e922-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3e922-185">Selecteer de koppeling **Geavanceerde query en filtering**.</span><span class="sxs-lookup"><span data-stu-id="3e922-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="3e922-186">Filter de kolom **msdyn\_transactiontype1** zodat deze alleen **msdyn\_estimateline** bevat.</span><span class="sxs-lookup"><span data-stu-id="3e922-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="3e922-187">De standaardprognosemodel-id instellen</span><span class="sxs-lookup"><span data-stu-id="3e922-187">Set the default forecast model ID</span></span>

<span data-ttu-id="3e922-188">Als u de standaardprognosemodel-id in de sjabloon wilt bijwerken, selecteert u de taak **Onkostenramingen** en klikt u vervolgens op de pijl **Toewijzen** om de toewijzing te openen.</span><span class="sxs-lookup"><span data-stu-id="3e922-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3e922-189">Selecteer de koppeling **Geavanceerde query en filtering**.</span><span class="sxs-lookup"><span data-stu-id="3e922-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="3e922-190">Als u de standaardsjabloon Microsoft Project-onkostenramingen (PSA naar Fin and Ops) gebruikt, selecteert u in Power Query eerst de **Ingevoegde voorwaarde** in de sectie **Toegepaste stappen**.</span><span class="sxs-lookup"><span data-stu-id="3e922-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="3e922-191">Vervang in de vermelding **Functie** de waarde **O\_forecast** door de naam van de prognosemodel-id die moet worden gebruikt met de integratie.</span><span class="sxs-lookup"><span data-stu-id="3e922-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="3e922-192">De standaardsjabloon heeft een prognosemodel-ID vanuit de demonstratiegegevens.</span><span class="sxs-lookup"><span data-stu-id="3e922-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="3e922-193">Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3e922-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="3e922-194">Selecteer in Power Query de optie **Voorwaardelijke kolom toevoegen** en voer een naam voor de nieuwe kolom in, zoals **Model-id**.</span><span class="sxs-lookup"><span data-stu-id="3e922-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="3e922-195">Voer de voorwaarde in voor de kolom waarin als ramingsregel-ID niet null is, dan \<voer de prognosemodel-id in\>; anders null.</span><span class="sxs-lookup"><span data-stu-id="3e922-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="3e922-196">De factureringstypen transformeren</span><span class="sxs-lookup"><span data-stu-id="3e922-196">Transform the billing types</span></span>

<span data-ttu-id="3e922-197">De sjabloon Projectonkostenramingen (PSA naar Fin and Ops) bevat een voorwaardelijke kolom die wordt gebruikt voor het transformeren van de factureringstypen die tijdens de integratie van Project Service Automation zijn ontvangen.</span><span class="sxs-lookup"><span data-stu-id="3e922-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="3e922-198">Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3e922-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="3e922-199">Selecteer de koppeling **Geavanceerde query en filtering** en selecteer vervolgens **Voorwaardelijke kolom toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3e922-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="3e922-200">Voer naam in voor de nieuwe kolom, zoals **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="3e922-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="3e922-201">Voer daarna de volgende voorwaarde in:</span><span class="sxs-lookup"><span data-stu-id="3e922-201">Then enter the following condition:</span></span>

<span data-ttu-id="3e922-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="3e922-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="3e922-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="3e922-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="3e922-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="3e922-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="3e922-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="3e922-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="3e922-206">De transactietypen transformeren</span><span class="sxs-lookup"><span data-stu-id="3e922-206">Transform the transaction types</span></span>

<span data-ttu-id="3e922-207">De sjabloon Projectonkostenramingen (PSA naar Fin and Ops) bevat een voorwaardelijke kolom die wordt gebruikt voor het transformeren van de transactietypen die tijdens de integratie van Project Service Automation zijn ontvangen.</span><span class="sxs-lookup"><span data-stu-id="3e922-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="3e922-208">Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3e922-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="3e922-209">Selecteer de koppeling **Geavanceerde query en filtering** en selecteer vervolgens **Voorwaardelijke kolom toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3e922-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="3e922-210">Voer naam in voor de nieuwe kolom, zoals **Transactietype**.</span><span class="sxs-lookup"><span data-stu-id="3e922-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="3e922-211">Voer daarna de volgende voorwaarde in:</span><span class="sxs-lookup"><span data-stu-id="3e922-211">Then enter the following condition:</span></span>

<span data-ttu-id="3e922-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="3e922-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="3e922-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="3e922-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="3e922-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="3e922-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3e922-215">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="3e922-215">Template mapping in Data integration</span></span>

<span data-ttu-id="3e922-216">In de volgende afbeeldingen ziet u voorbeelden van de sjabloontaaktoewijzingen in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="3e922-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="3e922-217">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="3e922-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3e922-218">[![Sjabloontoewijzing](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3e922-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="3e922-219">[![Sjabloontoewijzing](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3e922-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
