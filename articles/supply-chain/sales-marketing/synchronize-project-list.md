---
title: Projectlijst vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om projecten te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "312503"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e28de-103">Projectlijst van Finance and Operations synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="e28de-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e28de-104">In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om projecten te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e28de-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e28de-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="e28de-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e28de-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="e28de-106">Templates and tasks</span></span>
<span data-ttu-id="e28de-107">De volgende sjabloon en onderliggende taken worden gebruikt om projecten te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e28de-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e28de-108">**Sjabloontoewijzing in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="e28de-108">**Template in Data integration**</span></span>
- <span data-ttu-id="e28de-109">Projecten (Finance and Operations naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="e28de-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="e28de-110">**Taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="e28de-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="e28de-111">Projecten</span><span class="sxs-lookup"><span data-stu-id="e28de-111">Projects</span></span>

<span data-ttu-id="e28de-112">De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van een projectlijst kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="e28de-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="e28de-113">Rekeningen (Sales naar Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e28de-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e28de-114">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="e28de-114">Entity set</span></span>
| <span data-ttu-id="e28de-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="e28de-115">Field Service</span></span>           | <span data-ttu-id="e28de-116">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="e28de-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="e28de-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="e28de-117">msdynce_externalprojects</span></span> | <span data-ttu-id="e28de-118">Projecten</span><span class="sxs-lookup"><span data-stu-id="e28de-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="e28de-119">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="e28de-119">Entity flow</span></span>
<span data-ttu-id="e28de-120">Projecten worden gemaakt in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e28de-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="e28de-121">Projecten met **Tijd en materiaal** als **Projecttype** en **Onderhanden** als **Projectfase** worden gesynchroniseerd met de entiteit **Extern project** in Field Service, inclusief informatie over het projectnummer, de projectnaam, de projectfase en de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="e28de-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="e28de-122">De lijst **Extern project** wordt gebruikt om Field Service-werkorders te koppelen aan Finance and Operations-projecten.</span><span class="sxs-lookup"><span data-stu-id="e28de-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e28de-123">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="e28de-123">Field Service CRM solution</span></span>
<span data-ttu-id="e28de-124">De entiteit **Extern project** ontvangt alle projecten van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e28de-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="e28de-125">Het veld **Extern project** is toegevoegd aan de entiteit **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="e28de-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="e28de-126">Dit veld is een opzoekveld. Dus wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e28de-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="e28de-127">Nadat de **Systeemstatus** van **Geopend - In uitvoering (690.970.000)** in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet meer toevoegen, verwijderen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e28de-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e28de-128">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="e28de-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="e28de-129">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="e28de-129">Finance and Operations</span></span>
<span data-ttu-id="e28de-130">Wijzigingen bijhouden voor gegevensentiteitprojecten inschakelen</span><span class="sxs-lookup"><span data-stu-id="e28de-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e28de-131">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="e28de-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="e28de-132">Projecten (Finance and Operations naar Field Service): Projecten</span><span class="sxs-lookup"><span data-stu-id="e28de-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="e28de-133">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="e28de-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
