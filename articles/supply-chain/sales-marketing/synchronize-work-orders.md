---
title: Werkorders met project vanuit Field Service synchroniseren naar Finance and Operations
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Microsoft Dynamics 365 for Field Service naar Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536728"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="6a8cb-103">Werkorders met project vanuit Field Service synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6a8cb-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6a8cb-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Microsoft Dynamics 365 for Field Service naar Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="6a8cb-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="6a8cb-106">De gebruikte sjabloon **Werkorders met project (Field Service met Fin and Ops)** is gebaseerd op de sjabloon **Werkorders (Field Service met Fin and Ops)**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="6a8cb-107">Zie voor meer informatie [Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="6a8cb-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="6a8cb-108">In dit onderwerp worden alleen de verschillen tussen de twee sjablonen beschreven:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="6a8cb-109">**Werkorders met project (Field Service met Finance and Operations)**</span><span class="sxs-lookup"><span data-stu-id="6a8cb-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="6a8cb-110">**Werkorders (Field Service met Finance and Operations)**</span><span class="sxs-lookup"><span data-stu-id="6a8cb-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="6a8cb-111">Het belangrijkste verschil is dat deze sjabloon toewijzing van het projectnummer toegewezen aan de werkorder in Field Service omvat, zodat de verkooporder gemaakt in Finance and Operations het projectnummer bevat en dat de facturering in het gerelateerde project kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="6a8cb-112">Daarnaast worden de functies voor geavanceerde query's en filters gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6a8cb-113">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="6a8cb-113">Templates and tasks</span></span>

<span data-ttu-id="6a8cb-114">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="6a8cb-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="6a8cb-115">Werkorders met project (Field Service met Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="6a8cb-116">**Naam van de taak in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="6a8cb-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="6a8cb-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="6a8cb-117">WorkOrderHeader</span></span>
- <span data-ttu-id="6a8cb-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="6a8cb-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="6a8cb-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="6a8cb-119">WorkOrderProduct</span></span>
- <span data-ttu-id="6a8cb-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="6a8cb-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="6a8cb-121">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="6a8cb-121">Field Service CRM solution</span></span>
<span data-ttu-id="6a8cb-122">Het veld **Extern project** is toegevoegd aan de entiteit Werkorder.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="6a8cb-123">Dit veld is een opzoekveld en wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="6a8cb-124">Zodra de **systeemstatus** van Geopend of In uitvoering in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet toevoegen, verwijderen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6a8cb-125">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="6a8cb-125">Template mapping in Data integration</span></span>

<span data-ttu-id="6a8cb-126">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="6a8cb-127">Werkorders met project (Field Service met Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="6a8cb-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="6a8cb-128">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="6a8cb-129">Werkorders met project (Field Service met Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="6a8cb-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="6a8cb-130">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="6a8cb-131">Werkorders met project (Field Service met Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="6a8cb-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="6a8cb-132">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="6a8cb-133">Werkorders met project (Field Service met Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="6a8cb-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="6a8cb-134">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
