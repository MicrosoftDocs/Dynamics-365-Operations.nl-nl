---
title: Projecttaken vanuit Project Service Automation synchroniseren
description: In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Dynamics 365 for Finance and Operations.
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="48299-103">Projecttaken vanuit Project Service Automation rechtstreeks synchroniseren met projectactiviteiten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="48299-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="48299-104">In dit onderwerp worden de sjabloon en onderliggende taak beschreven die worden gebruikt om projecttaken rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="48299-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="48299-105">Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling is beschikbaar in Dynamics 365 for Finance and Operations, versie 8.0.</span><span class="sxs-lookup"><span data-stu-id="48299-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="48299-106">Gegevensstroom voor Project Service Automation naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="48299-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="48299-107">De oplossing Project Service Automation-integratie met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="48299-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="48299-108">De integratiesjabloon die beschikbaar is met de functie voor gegevensintegratie maakt de stroom van gegevens over projecttaken van Project Service Automation naar Finance and Operations mogelijk.</span><span class="sxs-lookup"><span data-stu-id="48299-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="48299-109">De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="48299-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="48299-110">[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="48299-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="48299-111">Sjabloon en taak</span><span class="sxs-lookup"><span data-stu-id="48299-111">Template and task</span></span>

<span data-ttu-id="48299-112">Selecteer voor toegang tot de sjabloon in het Microsoft PowerApps Beheercentrum **Projecten** en selecteer vervolgens in de rechterbovenhoek **Nieuw project** om openbare sjablonen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="48299-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="48299-113">De volgende sjabloon en onderliggende taak wordt gebruikt voor het synchroniseren van projecttaken vanuit Project Service Automation naar Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="48299-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="48299-114">-**Naam van de sjabloon in gegevensintegratie:** Projecttaken (PSA naar Fin and Ops) -**Naam van de taak in het project:** Projecttaken</span><span class="sxs-lookup"><span data-stu-id="48299-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="48299-115">Voordat synchronisatie van projecttaken en projecten kan optreden, moet u projectcontracten en projecten synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="48299-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="48299-116">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="48299-116">Entity set</span></span>

|<span data-ttu-id="48299-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="48299-117">Project Service Automation</span></span>               | <span data-ttu-id="48299-118">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="48299-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="48299-119">Projecttaken</span><span class="sxs-lookup"><span data-stu-id="48299-119">Project Tasks</span></span>                           | <span data-ttu-id="48299-120">Integratie-entiteit voor projecttaak.</span><span class="sxs-lookup"><span data-stu-id="48299-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="48299-121">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="48299-121">Entity flow</span></span>

<span data-ttu-id="48299-122">Projecttaken worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projectactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="48299-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="48299-123">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="48299-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="48299-124">Voordat synchronisatie van projecttaken en projecten kan optreden, moet u projectcontracten en projecten synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="48299-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="48299-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="48299-125">Power Query</span></span>

<span data-ttu-id="48299-126">U moet Microsoft Power Query gebruiken om gegevens te filteren als aan deze voorwaarden wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="48299-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="48299-127">U hebt resourcespecifieke records binnen een projecttaak.</span><span class="sxs-lookup"><span data-stu-id="48299-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="48299-128">Als u Power Query moet gebruiken, volgt u deze richtlijnen:</span><span class="sxs-lookup"><span data-stu-id="48299-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="48299-129">De sjabloon Projecttaken (PSA naar Fin and Ops) heeft een standaardfilter voor het uitsluiten van resourcespecifieke records binnen een projecttaak door het filter op de **IsLineTask** op **False** te zetten.</span><span class="sxs-lookup"><span data-stu-id="48299-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="48299-130">Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.</span><span class="sxs-lookup"><span data-stu-id="48299-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="48299-131">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="48299-131">Template mapping in Data integration</span></span>

<span data-ttu-id="48299-132">In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzingen in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="48299-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="48299-133">Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="48299-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="48299-134">[![Sjabloontoewijzing](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="48299-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


