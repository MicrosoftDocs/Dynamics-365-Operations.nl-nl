---
title: Projectonkostencategorieën tussen Finance and Operations en Project Service Automation synchroniseren
description: In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om projectonkostencategorieën rechtstreeks tussen Microsoft Dynamics 365 Finance en Dynamics 365 Project Service Automation te synchroniseren.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770307"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="e6cd4-103">Projectonkostencategorieën tussen Finance and Operations en Project Service Automation synchroniseren</span><span class="sxs-lookup"><span data-stu-id="e6cd4-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e6cd4-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om projectonkostencategorieën rechtstreeks tussen Dynamics 365 Finance en Dynamics 365 Project Service Automation te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="e6cd4-105">Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling zijn beschikbaar in versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="e6cd4-106">Integratie van werkelijke waarden is mogelijk in versie 8.0.1 of hoger.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="e6cd4-107">Als u Enterprise edition 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="e6cd4-108">Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="e6cd4-109">Gegevensstroom voor Project Service Automation en Finance</span><span class="sxs-lookup"><span data-stu-id="e6cd4-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="e6cd4-110">De integratieoplossing voor Project Service Automation en Finance gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="e6cd4-111">De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over categorieën projectonkostentransacties tussen Finance en Project Service Automation mogelijk.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="e6cd4-112">Als de projectonkostencategorieën worden gemaakt in Finance, is de stroom van de integratie eerst van Finance naar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="e6cd4-113">De integratie-id's van de onkostencategorieën voor projecten worden dan bijgewerkt via synchronisatie vanuit Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e6cd4-114">Als de projectonkostencategorieën worden gemaakt in Project Service Automation, is de stroom van de integratie eerst van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="e6cd4-115">De projectcategorieën moeten al in Finance zijn geconfigureerd vóór de synchronisatie vanuit Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="e6cd4-116">Synchroniseer vervolgens van Finance terug naar Project Service Automation en vervolgens van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="e6cd4-117">Op deze manier helpt u garanderen dat de categorieën zijn gekoppeld en dat er geen dubbele waarden worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="e6cd4-118">Meestal worden de projectonkostencategorieën gemaakt in Finance.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="e6cd4-119">Echter, als ze niet worden gemaakt in Finance, of als al onkostencategorieën zijn gemaakt in Project Service Automation, moet u eerst synchroniseren met de Project-sjabloon voor onkostentransactiecategorieën (PSA naar Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="e6cd4-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="e6cd4-120">Synchroniseer vervolgens via de Project-sjabloon voor kostentransactiecategorieën (Fin and Ops naar PSA).</span><span class="sxs-lookup"><span data-stu-id="e6cd4-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="e6cd4-121">Daarna moet u nog één keer de synchronisatie uitvoeren van Project Service Automation naar Finance.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="e6cd4-122">Als u eerst vanuit Project Service Automation synchroniseert, moet aan de volgende vereisten worden voldaan in Finance voordat de synchronisatie wordt uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="e6cd4-123">De gedeelde categorie die overeenkomt met de projectcategorie die is ingesteld in Project Service Automation moet bestaan en moet worden ingesteld voor zowel **Project** als **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="e6cd4-124">Voor elke rechtspersoon in Finance waarmee moet volgende geïntegreerd, moeten de volgende projectcategorieën bestaan:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="e6cd4-125">**Projectcategorie** bestaat.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="e6cd4-126">**Gebruiken in Onkosten** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="e6cd4-127">**Actief in journaal** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="e6cd4-128">**Transactietype** is ingesteld op **Onkosten**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="e6cd4-129">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="e6cd4-130">[![Gegevensstroom voor Project Service Automation-integratie met Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e6cd4-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="e6cd4-131">Synchronisatie van projectonkostencategorieën van Finance naar Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e6cd4-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="e6cd4-132">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="e6cd4-132">Template and task</span></span>

<span data-ttu-id="e6cd4-133">Selecteer voor toegang tot de sjabloon in het Microsoft Power Apps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e6cd4-134">De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Finance naar Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="e6cd4-135">**Naam van de sjabloon in Gegevensintegratie:** Categorieën projectkostentransacties (Fin and Ops naar PSA)</span><span class="sxs-lookup"><span data-stu-id="e6cd4-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="e6cd4-136">**Naam van de taak in het project:** Categorieën synchroniseren naar PSA</span><span class="sxs-lookup"><span data-stu-id="e6cd4-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="e6cd4-137">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="e6cd4-137">Entity set</span></span>

| <span data-ttu-id="e6cd4-138">Financiën</span><span class="sxs-lookup"><span data-stu-id="e6cd4-138">Finance</span></span>                           | <span data-ttu-id="e6cd4-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e6cd4-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="e6cd4-140">Integratie-entiteit voor categorieën</span><span class="sxs-lookup"><span data-stu-id="e6cd4-140">Integration entity for categories</span></span> | <span data-ttu-id="e6cd4-141">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="e6cd4-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="e6cd4-142">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="e6cd4-142">Entity flow</span></span>

<span data-ttu-id="e6cd4-143">Projectkostencategorieën worden beheerd in Finance en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="e6cd4-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="e6cd4-144">Power Query</span></span>

<span data-ttu-id="e6cd4-145">Wanneer u synchroniseert naar Project Service Automation, moet u Microsoft Power Query voor Excel gebruiken om het factureringstype in te stellen voor de transactiecategorie.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="e6cd4-146">De Project-sjabloon voor kostentransactiecategorieën (Fin and Ops naar PSA) biedt een standaardkolom en -toewijzing.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="e6cd4-147">Als u uw eigen sjabloon maakt, moet u een voorwaardelijke kolom toevoegen in Power Query.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="e6cd4-148">Volg deze stappen.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-148">Follow these steps.</span></span>

1. <span data-ttu-id="e6cd4-149">Klik op de pijl om de toewijzing te openen van de taak voor projectonkostencategorieën in de Project-sjabloon voor kostentransactiecategorieën (Fin en Ops voor PSA).</span><span class="sxs-lookup"><span data-stu-id="e6cd4-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="e6cd4-150">Klik op de koppeling **Geavanceerde query en filtering** om Power Query te openen.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="e6cd4-151">Selecteer **Voorwaardelijke kolom toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="e6cd4-152">Voer naam in voor de nieuwe kolom, zoals **Factureringstype**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="e6cd4-153">Voer de volgende voorwaarde in: **als CATEGORYID niet gelijk aan null dan 19235001, anders null**.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="e6cd4-154">Klik op **OK** in de kolom.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="e6cd4-155">Zorg ervoor dat deze nieuwe kolom wordt toegewezen op de toewijzingspagina.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="e6cd4-156">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="e6cd4-157">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Finance naar Project Service Automation worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="e6cd4-158">[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e6cd4-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="e6cd4-159">Synchronisatie van projectonkostencategorieën van Project Service Automation naar Finance</span><span class="sxs-lookup"><span data-stu-id="e6cd4-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="e6cd4-160">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="e6cd4-160">Template and task</span></span>

<span data-ttu-id="e6cd4-161">De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Project Service Automation naar Finance:</span><span class="sxs-lookup"><span data-stu-id="e6cd4-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e6cd4-162">**Naam van de sjabloon in Gegevensintegratie:** Categorieën projectkostentransacties (PSA naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="e6cd4-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e6cd4-163">**Naam van de taak in het project:** Categorieën synchroniseren naar Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="e6cd4-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="e6cd4-164">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="e6cd4-164">Entity set</span></span>

| <span data-ttu-id="e6cd4-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e6cd4-165">Project Service Automation</span></span> | <span data-ttu-id="e6cd4-166">Financiën</span><span class="sxs-lookup"><span data-stu-id="e6cd4-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="e6cd4-167">Transactiecategorieën</span><span class="sxs-lookup"><span data-stu-id="e6cd4-167">Transaction categories</span></span>     | <span data-ttu-id="e6cd4-168">Integratie-entiteit voor categorieën</span><span class="sxs-lookup"><span data-stu-id="e6cd4-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="e6cd4-169">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="e6cd4-169">Entity flow</span></span>

<span data-ttu-id="e6cd4-170">Projectkostencategorieën worden beheerd in Finance en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="e6cd4-171">De synchronisatie terug naar Finance werkt de projectcategorie in Finance bij met de integratie-id vanuit Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e6cd4-172">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="e6cd4-172">Template mapping in Data integration</span></span>

<span data-ttu-id="e6cd4-173">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="e6cd4-174">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="e6cd4-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e6cd4-175">[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e6cd4-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
