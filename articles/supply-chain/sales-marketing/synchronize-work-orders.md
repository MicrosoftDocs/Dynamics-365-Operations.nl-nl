---
title: Werkorders met project vanuit Field Service synchroniseren naar Finance and Operations
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Microsoft Dynamics 365 for Field Service naar Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "329845"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="43785-103">Werkorders met project vanuit Field Service synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43785-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="43785-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Microsoft Dynamics 365 for Field Service naar Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="43785-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="43785-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="43785-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="43785-106">De gebruikte sjabloon **Field Service-producten (Finance and Operations naar Field Service)** is gebaseerd op de sjabloon **Producten (Finance and Operations naar Sales) - Direct** van Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="43785-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="43785-107">Zie voor meer informatie [Producten (Finance and Operations naar Sales) - Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="43785-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="43785-108">In dit onderwerp worden alleen de verschillen beschreven tussen de sjablonen **Field Service-producten (Finance and Operations naar Field Service)** en **Field Service-producten (Finance and Operations naar Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="43785-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="43785-109">Het belangrijkste verschil is dat deze sjabloon toewijzing van het projectnummer toegewezen aan de werkorder in Field Service omvat, zodat de verkooporder gemaakt in Finance and Operations het projectnummer bevat en dat de facturering in het gerelateerde project kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="43785-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="43785-110">Daarnaast worden de functies voor geavanceerde query's en filters gebruikt.</span><span class="sxs-lookup"><span data-stu-id="43785-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="43785-111">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="43785-111">Templates and tasks</span></span>

<span data-ttu-id="43785-112">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="43785-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="43785-113">Werkorders met project (Field Service naar Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="43785-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="43785-114">**Naam van de taak in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="43785-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="43785-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="43785-115">WorkOrderHeader</span></span>
- <span data-ttu-id="43785-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="43785-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="43785-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="43785-117">WorkOrderProduct</span></span>
- <span data-ttu-id="43785-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="43785-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="43785-119">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="43785-119">Field Service CRM solution</span></span>
<span data-ttu-id="43785-120">Het veld **Extern project** is toegevoegd aan de entiteit Werkorder.</span><span class="sxs-lookup"><span data-stu-id="43785-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="43785-121">Dit veld is een opzoekveld en wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="43785-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="43785-122">Zodra de **systeemstatus** van Geopend of In uitvoering in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet toevoegen, verwijderen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="43785-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="43785-123">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="43785-123">Template mapping in Data integration</span></span>

<span data-ttu-id="43785-124">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="43785-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="43785-125">Werkorders met project (Field Service naar Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="43785-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="43785-126">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="43785-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="43785-127">Werkorders met project (Field Service naar Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="43785-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="43785-128">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="43785-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="43785-129">Werkorders met project (Field Service naar Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="43785-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="43785-130">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="43785-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="43785-131">Werkorders met project (Field Service naar Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="43785-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="43785-132">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="43785-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
