---
title: Projecttaken rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations
description: In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="29525-103">Projecttaken rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29525-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="29525-104">In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="29525-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="29525-105">Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling zijn beschikbaar in Microsoft Dynamics 365 for Finance and Operations, versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="29525-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="29525-106">Als u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren.</span><span class="sxs-lookup"><span data-stu-id="29525-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="29525-107">Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.</span><span class="sxs-lookup"><span data-stu-id="29525-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="29525-108">Integratie van werkelijke waarden is beschikbaar in Microsoft Dynamics 365 for Finance and Operations versie 8.01 of hoger.</span><span class="sxs-lookup"><span data-stu-id="29525-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="29525-109">Gegevensstroom voor Project Service Automation naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29525-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="29525-110">De oplossing Project Service Automation-integratie met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="29525-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="29525-111">De integratiesjabloon die beschikbaar is met de functie voor gegevensintegratie maakt de stroom van gegevens over projecttaken van Project Service Automation naar Finance and Operations mogelijk.</span><span class="sxs-lookup"><span data-stu-id="29525-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="29525-112">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="29525-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="29525-113">[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="29525-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="29525-114">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="29525-114">Template and task</span></span>

<span data-ttu-id="29525-115">Selecteer voor toegang tot de sjabloon in het Microsoft PowerApps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="29525-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="29525-116">De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projecttaken vanuit Project Service Automation naar Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="29525-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="29525-117">**Naam van de sjabloon in Gegevensintegratie:** Projecttaken (PSA naar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="29525-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="29525-118">**Naam van de taak in het project:** Projecttaken</span><span class="sxs-lookup"><span data-stu-id="29525-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="29525-119">Voordat synchronisatie van projecttaken en projecten kan optreden, moet u projectcontracten en projecten synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="29525-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="29525-120">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="29525-120">Entity set</span></span>

| <span data-ttu-id="29525-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="29525-121">Project Service Automation</span></span> | <span data-ttu-id="29525-122">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="29525-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="29525-123">Projecttaken</span><span class="sxs-lookup"><span data-stu-id="29525-123">Project Tasks</span></span>              | <span data-ttu-id="29525-124">Integratie-entiteit voor projecttaak</span><span class="sxs-lookup"><span data-stu-id="29525-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="29525-125">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="29525-125">Entity flow</span></span>

<span data-ttu-id="29525-126">Projecttaken worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projectactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="29525-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="29525-127">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="29525-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="29525-128">Voordat synchronisatie van projecttaken en projecten kan optreden, moet u projectcontracten en projecten synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="29525-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="29525-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="29525-129">Power Query</span></span>

<span data-ttu-id="29525-130">U moet Microsoft Power Query voor Excel gebruiken om gegevens te filteren als aan deze voorwaarde wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="29525-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="29525-131">U hebt resourcespecifieke records in een projecttaak.</span><span class="sxs-lookup"><span data-stu-id="29525-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="29525-132">Als u Power Query moet gebruiken, volgt u deze richtlijn:</span><span class="sxs-lookup"><span data-stu-id="29525-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="29525-133">De sjabloon Projecttaken (PSA naar Fin and Ops) heeft een standaardfilter waarbij resourcespecifieke records binnen een projecttaak worden uitgesloten door het filter op **IsLineTask** op **False** te zetten.</span><span class="sxs-lookup"><span data-stu-id="29525-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="29525-134">Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.</span><span class="sxs-lookup"><span data-stu-id="29525-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="29525-135">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="29525-135">Template mapping in Data integration</span></span>

<span data-ttu-id="29525-136">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzingen in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="29525-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="29525-137">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="29525-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="29525-138">[![Sjabloontoewijzing](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="29525-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
