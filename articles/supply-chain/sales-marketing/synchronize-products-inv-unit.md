---
title: Producten met voorraadeenheid uit Supply Chain Management synchroniseren met Field Service
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 741b823d6cc5dbd23cda4f07e463f28d6bbe77d6
ms.sourcegitcommit: a2f9dce06322dada6b5f1c82051ef2359f8c0f12
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/24/2020
ms.locfileid: "3081859"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="58425-103">Producten met voorraadeenheid uit Supply Chain Management synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="58425-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="58425-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="58425-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="58425-105">[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="58425-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="58425-106">De gebruikte sjabloon **Field Service-producten met Voorraadeenheid (Supply Chain Management naar Field Service)** is gebaseerd op de sjabloon **Field Service-producten (Supply Chain Management naar Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="58425-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="58425-107">Zie voor meer informatie [Producten in Supply Chain Management synchroniseren met producten in Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="58425-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="58425-108">In dit onderwerp worden alleen de verschillen tussen de twee sjablonen beschreven:</span><span class="sxs-lookup"><span data-stu-id="58425-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="58425-109">**Field Service-producten met Voorraadeenheid (Supply Chain Management naar Service)**</span><span class="sxs-lookup"><span data-stu-id="58425-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="58425-110">**Field Service-producten (Supply Chain Management naar Field Service)**</span><span class="sxs-lookup"><span data-stu-id="58425-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="58425-111">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="58425-111">Templates and tasks</span></span>

<span data-ttu-id="58425-112">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="58425-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="58425-113">Field Service-producten met Voorraadeenheid (Supply Chain Management naar Service)</span><span class="sxs-lookup"><span data-stu-id="58425-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="58425-114">**Naam van de taak in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="58425-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="58425-115">Producten</span><span class="sxs-lookup"><span data-stu-id="58425-115">Products</span></span>

<span data-ttu-id="58425-116">De gebruikte sjabloon **Field Service-producten met Voorraadeenheid (Supply Chain Management naar Field Service)** omvat een toewijzing die niet is inbegrepen in de sjabloon **Field Service-producten (Supply Chain Management naar Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="58425-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="58425-117">Deze toewijzing zorgt ervoor dat de voorraadeenheid die nodig is voor synchronisatie op voorraadniveau wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="58425-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="58425-118">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="58425-118">Template mapping in Data integration</span></span>

<span data-ttu-id="58425-119">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="58425-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="58425-120">Field Service-producten met Voorraadeenheid (Supply Chain Management naar Field Service): Products</span><span class="sxs-lookup"><span data-stu-id="58425-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="58425-121">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="58425-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
