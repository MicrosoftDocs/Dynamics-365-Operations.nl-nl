---
title: Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taak aan de orde voor het synchroniseren van producten met een voorraadeenheid vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="31a0b-103">Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="31a0b-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="31a0b-104">In dit onderwerp komen de sjablonen en onderliggende taak aan de orde voor het synchroniseren van producten met een voorraadeenheid vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="31a0b-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="31a0b-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="31a0b-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="31a0b-106">De gebruikte sjabloon **Field Service-producten (Finance and Operations naar Field Service)** is gebaseerd op de sjabloon **Producten (Finance and Operations naar Sales) - Direct** van Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="31a0b-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="31a0b-107">Zie voor meer informatie [Producten (Finance and Operations naar Sales) - Direct](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="31a0b-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="31a0b-108">In dit onderwerp worden alleen de verschillen beschreven tussen de sjablonen **Field Service-producten (Finance and Operations naar Field Service)** en **Field Service-producten (Finance and Operations naar Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="31a0b-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="31a0b-109">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="31a0b-109">Templates and tasks</span></span>

<span data-ttu-id="31a0b-110">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="31a0b-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="31a0b-111">Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales)</span><span class="sxs-lookup"><span data-stu-id="31a0b-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="31a0b-112">**Naam van de taak in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="31a0b-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="31a0b-113">Producten</span><span class="sxs-lookup"><span data-stu-id="31a0b-113">Products</span></span>

<span data-ttu-id="31a0b-114">De sjabloon **Field Service-producten met Voorraadeenheid (Finance and Operations naar Field Service)** bevat één toewijzing die niet is opgenomen in de sjabloon **Field Service-producten (Finance and Operations naar Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="31a0b-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="31a0b-115">Deze toewijzing zorgt ervoor dat de voorraadeenheid die nodig is voor synchronisatie op voorraadniveau wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="31a0b-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="31a0b-116">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="31a0b-116">Template mapping in Data integration</span></span>

<span data-ttu-id="31a0b-117">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="31a0b-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="31a0b-118">Field Service-producten met Voorraadeenheid (Finance and Operations naar Field Service): Producten</span><span class="sxs-lookup"><span data-stu-id="31a0b-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="31a0b-119">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="31a0b-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>

