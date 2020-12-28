---
title: Projectlijsten uit Supply Chain Management synchroniseren met Field Service
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om projecten te synchroniseren van Dynamics 365 Supply Chain Management met Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d80fce409ee92973a6134d96ce839b9722980918
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425111"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="80c4e-103">Projectlijsten uit Supply Chain Management synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="80c4e-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="80c4e-104">In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om projecten te synchroniseren van Dynamics 365 Supply Chain Management met Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="80c4e-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="80c4e-105">[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="80c4e-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="80c4e-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="80c4e-106">Templates and tasks</span></span>
<span data-ttu-id="80c4e-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projecten vanuit Supply Chain Management naar Field Service.</span><span class="sxs-lookup"><span data-stu-id="80c4e-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="80c4e-108">**Sjabloontoewijzing in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="80c4e-108">**Template in Data integration**</span></span>
- <span data-ttu-id="80c4e-109">Projecten (Supply Chain Management naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="80c4e-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="80c4e-110">**Taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="80c4e-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="80c4e-111">Projecten</span><span class="sxs-lookup"><span data-stu-id="80c4e-111">Projects</span></span>

<span data-ttu-id="80c4e-112">De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van een projectlijst kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="80c4e-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="80c4e-113">Rekeningen (Sales naar Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="80c4e-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="80c4e-114">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="80c4e-114">Entity set</span></span>
| <span data-ttu-id="80c4e-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="80c4e-115">Field Service</span></span>           | <span data-ttu-id="80c4e-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="80c4e-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="80c4e-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="80c4e-117">msdynce_externalprojects</span></span> | <span data-ttu-id="80c4e-118">Projecten</span><span class="sxs-lookup"><span data-stu-id="80c4e-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="80c4e-119">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="80c4e-119">Entity flow</span></span>
<span data-ttu-id="80c4e-120">Projecten worden gemaakt in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="80c4e-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="80c4e-121">Projecten met **Tijd en materiaal** als **Projecttype** en **Onderhanden** als **Projectfase** worden gesynchroniseerd met de entiteit **Extern project** in Field Service, inclusief informatie over het projectnummer, de projectnaam, de projectfase en de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="80c4e-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="80c4e-122">De lijst **Extern project** wordt gebruikt om Field Service-werkorders te koppelen aan Supply Chain Management-projecten.</span><span class="sxs-lookup"><span data-stu-id="80c4e-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="80c4e-123">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="80c4e-123">Field Service CRM solution</span></span>
<span data-ttu-id="80c4e-124">De entiteit **Extern project** ontvangt alle projecten van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="80c4e-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="80c4e-125">Het veld **Extern project** is toegevoegd aan de entiteit **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="80c4e-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="80c4e-126">Dit veld is een opzoekveld, dus wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="80c4e-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="80c4e-127">Nadat de **Systeemstatus** van **Geopend - In uitvoering (690.970.000)** in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet meer toevoegen, verwijderen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="80c4e-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="80c4e-128">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="80c4e-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="80c4e-129">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="80c4e-129">Supply Chain Management</span></span>
<span data-ttu-id="80c4e-130">Wijzigingen bijhouden voor gegevensentiteitprojecten inschakelen</span><span class="sxs-lookup"><span data-stu-id="80c4e-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="80c4e-131">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="80c4e-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="80c4e-132">Projecten (Supply Chain Management naar Field Service): Projects</span><span class="sxs-lookup"><span data-stu-id="80c4e-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="80c4e-133">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="80c4e-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
