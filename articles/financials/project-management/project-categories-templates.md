---
title: "Projectonkostencategorieën vanuit Project Service Automation synchroniseren"
description: "In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om projectonkostencategorieën te synchroniseren tussen Microsoft Dynamics 365 for Project Service Automation en Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: nl-nl
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="b56f3-103">Projectonkostencategorieën tussen Finance and Operations en Project Service Automation synchroniseren</span><span class="sxs-lookup"><span data-stu-id="b56f3-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="b56f3-104">In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om projectonkostencategorieën te synchroniseren tussen Microsoft Dynamics 365 for Project Service Automation en Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b56f3-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="b56f3-105">Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling is beschikbaar in Dynamics 365 for Finance and Operations, versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="b56f3-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="b56f3-106">Gegevensstroom voor Project Service Automation en Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b56f3-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="b56f3-107">De integratieoplossing voor Project Service Automation en Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b56f3-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="b56f3-108">De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over categorieën projectonkostentransacties tussen Project Service Automation en Finance and Operations mogelijk.</span><span class="sxs-lookup"><span data-stu-id="b56f3-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="b56f3-109">Als de projectonkostencategorieën worden gemaakt in Finance and Operations, is de stroom van de integratie van Finance and Operations naar Project Service Automation en vervolgens worden de integratie-ID's van projectonkostencategorieën bijgewerkt doordat wordt gesynchroniseerd van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b56f3-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b56f3-110">Als de projectonkostencategorieën worden gemaakt in Project Service Automation, is de stroom van de integratie eerst van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b56f3-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="b56f3-111">De projectcategorieën moeten in Finance and Operations zijn geconfigureerd al vóór de synchronisatie van Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b56f3-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="b56f3-112">Synchroniseer vervolgens van Finance and Operations terug naar Project Service Automation en vervolgens van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b56f3-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="b56f3-113">Hierdoor worden de categorieën gekoppeld en worden geen duplicaten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b56f3-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="b56f3-114">Meestal worden de projectonkostencategorieën gemaakt in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b56f3-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="b56f3-115">Als dat niet uw situatie is of als u al onkostencategorieën hebt gemaakt in Project Service Automation, moet u eerst synchroniseren met behulp van de categorieën projectonkostentransacties (PSA naar Fin and Ops) en vervolgens synchroniseren met categorieën projectonkostentransacties (Fin and Ops naar PSA).</span><span class="sxs-lookup"><span data-stu-id="b56f3-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="b56f3-116">Vervolgens voert u de synchronisatie nog een keer uit van PSA naar Fin and Ops.</span><span class="sxs-lookup"><span data-stu-id="b56f3-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="b56f3-117">Als u eerst synchroniseert vanuit Project Service Automation, moeten de projectcategorieën al zijn ingesteld in Finance and Operations en moeten alle projectcategorieën die moeten worden gesynchroniseerd met de Project Service Automation-transactiecategorieën, zijn ingesteld als **Actief in journalen**.</span><span class="sxs-lookup"><span data-stu-id="b56f3-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="b56f3-118">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b56f3-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="b56f3-119">[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b56f3-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="b56f3-120">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="b56f3-120">Templates and tasks</span></span>

<span data-ttu-id="b56f3-121">Selecteer voor toegang tot beschikbare sjablonen in het Microsoft PowerApps Beheercentrum **Projecten** en selecteer vervolgens in de rechterbovenhoek **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="b56f3-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b56f3-122">De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Finance and Operations naar Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="b56f3-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="b56f3-123">**Naam van de sjabloon in Gegevensintegratie:** Categorieën projectkostentransacties (Fin and Ops naar PSA)</span><span class="sxs-lookup"><span data-stu-id="b56f3-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="b56f3-124">**Naam van de taak in het project:** Categorieën synchroniseren naar PSA</span><span class="sxs-lookup"><span data-stu-id="b56f3-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="b56f3-125">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="b56f3-125">Entity set</span></span>

| <span data-ttu-id="b56f3-126">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="b56f3-126">Finance and Operations</span></span>               | <span data-ttu-id="b56f3-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b56f3-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="b56f3-128">Integratie-entiteit voor categorieën</span><span class="sxs-lookup"><span data-stu-id="b56f3-128">Integration entity for categories</span></span>    | <span data-ttu-id="b56f3-129">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="b56f3-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="b56f3-130">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="b56f3-130">Entity flow</span></span>

<span data-ttu-id="b56f3-131">Projectkostencategorieën worden beheerd in Finance and Operations en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="b56f3-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="b56f3-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="b56f3-132">Power Query</span></span>

<span data-ttu-id="b56f3-133">U moet Microsoft Power Query gebruiken om het type facturering in te stellen voor de transactiecategorie wanneer u synchroniseert naar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b56f3-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="b56f3-134">De sjabloon Categorieën projectkostentransacties (Fin and Ops naar PSA) heeft al een standaardkolom en -toewijzing.</span><span class="sxs-lookup"><span data-stu-id="b56f3-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="b56f3-135">Als u uw eigen sjabloon maakt, moet u een voorwaardelijke kolom toevoegen in Power Query.</span><span class="sxs-lookup"><span data-stu-id="b56f3-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="b56f3-136">Open het formulier Geavanceerde filtering en query vanuit de toewijzing van de projectkostencategorieëntaak.</span><span class="sxs-lookup"><span data-stu-id="b56f3-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="b56f3-137">Selecteer **Voorwaardelijke kolom toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b56f3-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="b56f3-138">Geef de nieuwe kolom een naam, zoals Factureringstype.</span><span class="sxs-lookup"><span data-stu-id="b56f3-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="b56f3-139">Voer de volgende voorwaarde: als **CATEGORYID niet gelijk aan null dan 19235001, anders null**.</span><span class="sxs-lookup"><span data-stu-id="b56f3-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="b56f3-140">Klik op **OK** in de kolom.</span><span class="sxs-lookup"><span data-stu-id="b56f3-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="b56f3-141">Zorg ervoor dat deze nieuwe kolom wordt toegewezen op de toewijzingspagina.</span><span class="sxs-lookup"><span data-stu-id="b56f3-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="b56f3-142">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="b56f3-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="b56f3-143">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Finance and Operations naar Project Service Automation worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="b56f3-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="b56f3-144">[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b56f3-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="b56f3-145">De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Project Service Automation naar Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b56f3-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="b56f3-146">-**Naam van de sjabloon in gegevensintegratie:** Categorieën projectkostentransacties (PSA naar Fin and Ops) -**Naam van de taak in het project:** Categorieën synchroniseren naar Fin Ops</span><span class="sxs-lookup"><span data-stu-id="b56f3-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="b56f3-147">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="b56f3-147">Entity set</span></span>

| <span data-ttu-id="b56f3-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b56f3-148">Project Service Automation</span></span>      | <span data-ttu-id="b56f3-149">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="b56f3-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="b56f3-150">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="b56f3-150">Transaction categories</span></span>          | <span data-ttu-id="b56f3-151">Integratie-entiteit voor categorieën</span><span class="sxs-lookup"><span data-stu-id="b56f3-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="b56f3-152">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="b56f3-152">Entity flow</span></span>

<span data-ttu-id="b56f3-153">Projectkostencategorieën worden beheerd in Finance and Operations en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="b56f3-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="b56f3-154">De synchronisatie terug naar Finance and Operations werkt de integratie-id bij vanuit Project Service Automation in de Finance and Operations-projectcategorie.</span><span class="sxs-lookup"><span data-stu-id="b56f3-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="b56f3-155">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="b56f3-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="b56f3-156">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="b56f3-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b56f3-157">[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b56f3-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

