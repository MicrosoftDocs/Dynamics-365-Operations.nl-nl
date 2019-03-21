---
title: Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2019
ms.locfileid: "836297"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c79c1-103">Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="c79c1-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c79c1-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c79c1-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c79c1-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="c79c1-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="c79c1-106">De gebruikte sjabloon **Field Service-producten met Voorraadeenheid (Finance and Operations met Field Service)** is gebaseerd op de sjabloon **Field Service-producten (Finance and Operations met Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="c79c1-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="c79c1-107">Zie voor meer informatie [Field Service-producten (Finance and Operations met Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="c79c1-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="c79c1-108">In dit onderwerp worden alleen de verschillen tussen de twee sjablonen beschreven:</span><span class="sxs-lookup"><span data-stu-id="c79c1-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="c79c1-109">**Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales)**</span><span class="sxs-lookup"><span data-stu-id="c79c1-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="c79c1-110">**Field Service-producten (Finance and Operations met Field Service)**</span><span class="sxs-lookup"><span data-stu-id="c79c1-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="c79c1-111">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="c79c1-111">Templates and tasks</span></span>

<span data-ttu-id="c79c1-112">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="c79c1-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="c79c1-113">Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales)</span><span class="sxs-lookup"><span data-stu-id="c79c1-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="c79c1-114">**Naam van de taak in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="c79c1-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="c79c1-115">Producten</span><span class="sxs-lookup"><span data-stu-id="c79c1-115">Products</span></span>

<span data-ttu-id="c79c1-116">De sjabloon **Field Service-producten met Voorraadeenheid (Finance and Operations naar Field Service)** bevat één toewijzing die niet is opgenomen in de sjabloon **Field Service-producten (Finance and Operations naar Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="c79c1-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="c79c1-117">Deze toewijzing zorgt ervoor dat de voorraadeenheid die nodig is voor synchronisatie op voorraadniveau wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c79c1-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c79c1-118">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="c79c1-118">Template mapping in Data integration</span></span>

<span data-ttu-id="c79c1-119">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="c79c1-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="c79c1-120">Field Service-producten met Voorraadeenheid (Finance and Operations naar Field Service): Producten</span><span class="sxs-lookup"><span data-stu-id="c79c1-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="c79c1-121">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="c79c1-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
