---
title: Werkorders synchroniseren met projecten van Field Service Supply Chain Management
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Dynamics 365 Field Service naar Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5c57b8d1e09fd57611accec83ec3da4bc596fd00
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627546"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="096b7-103">Werkorders synchroniseren met projecten van Field Service Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="096b7-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="096b7-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Dynamics 365 Field Service naar Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="096b7-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="096b7-105">[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="096b7-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="096b7-106">De gebruikte sjabloon **Werkorders met Project (Field Service naar Supply Chain Management)** is gebaseerd op de sjabloon **Werkorders (Field Service naar Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="096b7-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="096b7-107">Zie voor meer informatie [Werkorders in Field Service synchroniseren met verkooporders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="096b7-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="096b7-108">In dit onderwerp worden alleen de verschillen tussen de twee sjablonen beschreven:</span><span class="sxs-lookup"><span data-stu-id="096b7-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="096b7-109">**Werkorders met Project (Field Service naar Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="096b7-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="096b7-110">**Werkorders (Field Service naar Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="096b7-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="096b7-111">Het belangrijkste verschil is dat deze sjabloon toewijzing van het projectnummer omvat dat in Field Service aan de werkorder is toegewezen, zodat de Verkooporder die in Supply Chain Management is gemaakt, het projectnummer bevat en dat de facturering in het gerelateerde project kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="096b7-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="096b7-112">Daarnaast worden de functies voor geavanceerde query's en filters gebruikt.</span><span class="sxs-lookup"><span data-stu-id="096b7-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="096b7-113">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="096b7-113">Templates and tasks</span></span>

<span data-ttu-id="096b7-114">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="096b7-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="096b7-115">Werkorders met Project (Field Service naar Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="096b7-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="096b7-116">**Naam van de taak in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="096b7-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="096b7-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="096b7-117">WorkOrderHeader</span></span>
- <span data-ttu-id="096b7-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="096b7-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="096b7-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="096b7-119">WorkOrderProduct</span></span>
- <span data-ttu-id="096b7-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="096b7-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="096b7-121">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="096b7-121">Field Service CRM solution</span></span>
<span data-ttu-id="096b7-122">Het veld **Extern project** is toegevoegd aan de entiteit Werkorder.</span><span class="sxs-lookup"><span data-stu-id="096b7-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="096b7-123">Dit veld is een opzoekveld en wanneer u uw Werkorder aan een project koppelt, wordt de Verkooporder verbonden met een project in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="096b7-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="096b7-124">Zodra de **Systeemstatus** van Geopend – In uitvoering(690,970,000) in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet toevoegen, verwijderen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="096b7-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="096b7-125">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="096b7-125">Template mapping in Data integration</span></span>

<span data-ttu-id="096b7-126">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="096b7-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="096b7-127">Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="096b7-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="096b7-128">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="096b7-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="096b7-129">Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="096b7-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="096b7-130">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="096b7-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="096b7-131">Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="096b7-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="096b7-132">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="096b7-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="096b7-133">Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="096b7-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="096b7-134">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="096b7-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
