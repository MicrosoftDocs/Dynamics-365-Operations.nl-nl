---
title: Projectlijst vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van projecten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="1bcb0-103">Projectlijst vanuit Finance and Operations synchroniseren naar Field Service</span><span class="sxs-lookup"><span data-stu-id="1bcb0-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1bcb0-104">In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van projecten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1bcb0-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="1bcb0-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1bcb0-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="1bcb0-106">Templates and tasks</span></span>
<span data-ttu-id="1bcb0-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projecten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1bcb0-108">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="1bcb0-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="1bcb0-109">Projecten (Finance and Operations naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="1bcb0-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="1bcb0-110">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="1bcb0-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="1bcb0-111">Projecten</span><span class="sxs-lookup"><span data-stu-id="1bcb0-111">Projects</span></span>

<span data-ttu-id="1bcb0-112">De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van een projectlijst kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="1bcb0-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="1bcb0-113">Rekeningen (Sales naar Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="1bcb0-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="1bcb0-114">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="1bcb0-114">Entity set</span></span>
<span data-ttu-id="1bcb0-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1bcb0-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="1bcb0-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="1bcb0-116">Field Service</span></span>           | <span data-ttu-id="1bcb0-117">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="1bcb0-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="1bcb0-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="1bcb0-118">msdynce_externalprojects</span></span> | <span data-ttu-id="1bcb0-119">Projecten</span><span class="sxs-lookup"><span data-stu-id="1bcb0-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="1bcb0-120">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="1bcb0-120">Entity flow</span></span>
<span data-ttu-id="1bcb0-121">Projecten worden gemaakt in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="1bcb0-122">Projecten met Tijd en materiaal als **projecttype** en Onderhanden als **projectfase** orden gesynchroniseerd naar de entiteit **Extern project** in Field Service, inclusief informatie over het projectnummer, de projectnaam, de projectfase en de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="1bcb0-123">De lijst **Extern project** wordt gebruikt om Field Service-werkorders te koppelen aan Finance and Operations-projecten.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="1bcb0-124">De Field Service CRM-oplossing Het externe project is een nieuwe entiteit die alle projecten uit Operations krijgt.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="1bcb0-125">Het veld Extern project is toegevoegd aan de entiteit Werkorder.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="1bcb0-126">Dit veld is een opzoekveld en wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Operations.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="1bcb0-127">Zodra de systeemstatus van Geopend - In uitvoering (690.970.000) in een hogere status wordt gewijzigd, wordt het veld Extern project vergrendeld en kunt u de waarde niet toevoegen, verwijderen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1bcb0-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1bcb0-128">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="1bcb0-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="1bcb0-129">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1bcb0-129">In Finance and Operations</span></span>
<span data-ttu-id="1bcb0-130">Wijzigingen bijhouden voor gegevensentiteitprojecten inschakelen</span><span class="sxs-lookup"><span data-stu-id="1bcb0-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1bcb0-131">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="1bcb0-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="1bcb0-132">Projecten (Finance and Operations naar Field Service): Projecten</span><span class="sxs-lookup"><span data-stu-id="1bcb0-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="1bcb0-133">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="1bcb0-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

