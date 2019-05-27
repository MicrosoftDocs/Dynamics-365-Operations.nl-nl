---
title: Projectonkostencategorieën tussen Finance and Operations en Project Service Automation synchroniseren
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om projectonkostencategorieën rechtstreeks tussen Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation te synchroniseren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558237"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="0d77f-103">Projectonkostencategorieën tussen Finance and Operations en Project Service Automation synchroniseren</span><span class="sxs-lookup"><span data-stu-id="0d77f-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0d77f-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om projectonkostencategorieën rechtstreeks tussen Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Project Service Automation te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="0d77f-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="0d77f-105">Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling zijn beschikbaar in Microsoft Dynamics 365 for Finance and Operations versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="0d77f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="0d77f-106">Integratie van werkelijke waarden is mogelijk in Microsoft Dynamics 365 for Finance and Operations versie 8.0.1 of hoger.</span><span class="sxs-lookup"><span data-stu-id="0d77f-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="0d77f-107">Als u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren.</span><span class="sxs-lookup"><span data-stu-id="0d77f-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="0d77f-108">Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.</span><span class="sxs-lookup"><span data-stu-id="0d77f-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="0d77f-109">Gegevensstroom voor Project Service Automation en Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0d77f-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="0d77f-110">De integratieoplossing voor Project Service Automation en Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d77f-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="0d77f-111">De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over categorieën projectonkostentransacties tussen Project Service Automation en Finance and Operations mogelijk.</span><span class="sxs-lookup"><span data-stu-id="0d77f-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="0d77f-112">Als de projectonkostencategorieën worden gemaakt in Finance and Operations, is de stroom van de integratie eerst van Finance and Operations naar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="0d77f-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="0d77f-113">De integratie-id's van de onkostencategorieën voor projecten worden dan bijgewerkt via synchronisatie vanuit Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d77f-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="0d77f-114">Als de projectonkostencategorieën worden gemaakt in Project Service Automation, is de stroom van de integratie eerst van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d77f-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="0d77f-115">De projectcategorieën moeten al in Finance and Operations zijn geconfigureerd vóór de synchronisatie vanuit Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="0d77f-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="0d77f-116">Synchroniseer vervolgens van Finance and Operations terug naar Project Service Automation en vervolgens van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d77f-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="0d77f-117">Op deze manier helpt u garanderen dat de categorieën zijn gekoppeld en dat er geen dubbele waarden worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0d77f-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="0d77f-118">Meestal worden de projectonkostencategorieën gemaakt in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d77f-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="0d77f-119">Echter, als ze niet worden gemaakt in Finance and Operations, of als al onkostencategorieën zijn gemaakt in Project Service Automation, moet u eerst synchroniseren met de Project-sjabloon voor onkostentransactiecategorieën (PSA naar Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="0d77f-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="0d77f-120">Synchroniseer vervolgens via de Project-sjabloon voor kostentransactiecategorieën (Fin and Ops naar PSA).</span><span class="sxs-lookup"><span data-stu-id="0d77f-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="0d77f-121">Daarna moet u nog één keer de synchronisatie uitvoeren van Project Service Automation naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d77f-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="0d77f-122">Als u eerst vanuit Project Service Automation synchroniseert, moet aan de volgende vereisten worden voldaan in Finance and Operations voordat de synchronisatie wordt uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="0d77f-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="0d77f-123">De gedeelde categorie die overeenkomt met de projectcategorie die is ingesteld in Project Service Automation moet bestaan en moet worden ingesteld voor zowel **Project** als **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="0d77f-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="0d77f-124">Voor elke rechtspersoon in Finance and Operations waarmee moet volgende geïntegreerd, moeten de volgende projectcategorieën bestaan:</span><span class="sxs-lookup"><span data-stu-id="0d77f-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="0d77f-125">**Projectcategorie** bestaat.</span><span class="sxs-lookup"><span data-stu-id="0d77f-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="0d77f-126">**Gebruiken in Onkosten** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0d77f-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="0d77f-127">**Actief in journaal** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0d77f-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="0d77f-128">**Transactietype** is ingesteld op **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="0d77f-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="0d77f-129">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d77f-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="0d77f-130">[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="0d77f-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="0d77f-131">Synchronisatie van projectonkostencategorieën van Finance and Operations naar Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0d77f-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="0d77f-132">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="0d77f-132">Template and task</span></span>

<span data-ttu-id="0d77f-133">Selecteer voor toegang tot de sjabloon in het Microsoft PowerApps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="0d77f-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="0d77f-134">De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Finance and Operations naar Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="0d77f-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="0d77f-135">**Naam van de sjabloon in Gegevensintegratie:** Categorieën projectkostentransacties (Fin and Ops naar PSA)</span><span class="sxs-lookup"><span data-stu-id="0d77f-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="0d77f-136">**Naam van de taak in het project:** Categorieën synchroniseren naar PSA</span><span class="sxs-lookup"><span data-stu-id="0d77f-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="0d77f-137">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="0d77f-137">Entity set</span></span>

| <span data-ttu-id="0d77f-138">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="0d77f-138">Finance and Operations</span></span>            | <span data-ttu-id="0d77f-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0d77f-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="0d77f-140">Integratie-entiteit voor categorieën</span><span class="sxs-lookup"><span data-stu-id="0d77f-140">Integration entity for categories</span></span> | <span data-ttu-id="0d77f-141">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="0d77f-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="0d77f-142">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="0d77f-142">Entity flow</span></span>

<span data-ttu-id="0d77f-143">Projectkostencategorieën worden beheerd in Finance and Operations en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="0d77f-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="0d77f-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="0d77f-144">Power Query</span></span>

<span data-ttu-id="0d77f-145">Wanneer u synchroniseert naar Project Service Automation, moet u Microsoft Power Query voor Excel gebruiken om het factureringstype in te stellen voor de transactiecategorie.</span><span class="sxs-lookup"><span data-stu-id="0d77f-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="0d77f-146">De Project-sjabloon voor kostentransactiecategorieën (Fin and Ops naar PSA) biedt een standaardkolom en -toewijzing.</span><span class="sxs-lookup"><span data-stu-id="0d77f-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="0d77f-147">Als u uw eigen sjabloon maakt, moet u een voorwaardelijke kolom toevoegen in Power Query.</span><span class="sxs-lookup"><span data-stu-id="0d77f-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="0d77f-148">Volg deze stappen.</span><span class="sxs-lookup"><span data-stu-id="0d77f-148">Follow these steps.</span></span>

1. <span data-ttu-id="0d77f-149">Klik op de pijl om de toewijzing te openen van de taak voor projectonkostencategorieën in de Project-sjabloon voor kostentransactiecategorieën (Fin en Ops voor PSA).</span><span class="sxs-lookup"><span data-stu-id="0d77f-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="0d77f-150">Klik op de koppeling **Geavanceerde query en filtering** om Power Query te openen.</span><span class="sxs-lookup"><span data-stu-id="0d77f-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="0d77f-151">Selecteer **Voorwaardelijke kolom toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0d77f-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="0d77f-152">Voer naam in voor de nieuwe kolom, zoals **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="0d77f-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="0d77f-153">Voer de volgende voorwaarde in: **als CATEGORYID niet gelijk aan null dan 19235001, anders null**.</span><span class="sxs-lookup"><span data-stu-id="0d77f-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="0d77f-154">Klik op **OK** in de kolom.</span><span class="sxs-lookup"><span data-stu-id="0d77f-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="0d77f-155">Zorg ervoor dat deze nieuwe kolom wordt toegewezen op de toewijzingspagina.</span><span class="sxs-lookup"><span data-stu-id="0d77f-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="0d77f-156">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="0d77f-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="0d77f-157">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Finance and Operations naar Project Service Automation worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="0d77f-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="0d77f-158">[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0d77f-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="0d77f-159">Synchronisatie van projectonkostencategorieën van Project Service Automation naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0d77f-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="0d77f-160">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="0d77f-160">Template and task</span></span>

<span data-ttu-id="0d77f-161">De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Project Service Automation naar Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="0d77f-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="0d77f-162">**Naam van de sjabloon in Gegevensintegratie:** Categorieën projectkostentransacties (PSA naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="0d77f-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="0d77f-163">**Naam van de taak in het project:** Categorieën synchroniseren naar Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="0d77f-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="0d77f-164">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="0d77f-164">Entity set</span></span>

| <span data-ttu-id="0d77f-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0d77f-165">Project Service Automation</span></span> | <span data-ttu-id="0d77f-166">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="0d77f-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="0d77f-167">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="0d77f-167">Transaction categories</span></span>     | <span data-ttu-id="0d77f-168">Integratie-entiteit voor categorieën</span><span class="sxs-lookup"><span data-stu-id="0d77f-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="0d77f-169">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="0d77f-169">Entity flow</span></span>

<span data-ttu-id="0d77f-170">Projectkostencategorieën worden beheerd in Finance and Operations en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="0d77f-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="0d77f-171">De synchronisatie terug naar Finance and Operations werkt de projectcategorie in Finance and Operations bij met de integratie-id vanuit Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="0d77f-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0d77f-172">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="0d77f-172">Template mapping in Data integration</span></span>

<span data-ttu-id="0d77f-173">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="0d77f-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="0d77f-174">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="0d77f-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="0d77f-175">[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0d77f-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
