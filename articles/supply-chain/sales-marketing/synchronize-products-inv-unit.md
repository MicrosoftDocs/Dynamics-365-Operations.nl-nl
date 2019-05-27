---
title: Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535854"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="95925-103">Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="95925-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="95925-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="95925-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="95925-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="95925-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="95925-106">De gebruikte sjabloon **Field Service-producten met Voorraadeenheid (Fin and Ops naar Field Service)** is gebaseerd op de sjabloon **Field Service-producten (Fin and Ops naar Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="95925-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="95925-107">Zie voor meer informatie [Field Service-producten (Finance and Operations met Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="95925-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="95925-108">In dit onderwerp worden alleen de verschillen tussen de twee sjablonen beschreven:</span><span class="sxs-lookup"><span data-stu-id="95925-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="95925-109">**Field Service-producten met Voorraadeenheid (Fin and Ops naar Sales)**</span><span class="sxs-lookup"><span data-stu-id="95925-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="95925-110">**Field Service-producten (Fin and Ops naar Field Service)**</span><span class="sxs-lookup"><span data-stu-id="95925-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="95925-111">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="95925-111">Templates and tasks</span></span>

<span data-ttu-id="95925-112">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="95925-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="95925-113">Field Service-producten met Voorraadeenheid (Fin and Ops naar Sales)</span><span class="sxs-lookup"><span data-stu-id="95925-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="95925-114">**Naam van de taak in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="95925-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="95925-115">Producten</span><span class="sxs-lookup"><span data-stu-id="95925-115">Products</span></span>

<span data-ttu-id="95925-116">De sjabloon **Field Service-producten met Voorraadeenheid (Fin and Ops naar Field Service)** bevat één toewijzing die niet is opgenomen in de sjabloon **Field Service-producten (Fin and Ops naar Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="95925-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="95925-117">Deze toewijzing zorgt ervoor dat de voorraadeenheid die nodig is voor synchronisatie op voorraadniveau wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="95925-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="95925-118">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="95925-118">Template mapping in Data integration</span></span>

<span data-ttu-id="95925-119">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="95925-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="95925-120">Field Service-producten met Voorraadeenheid (Fin and Ops naar Field Service): Producten</span><span class="sxs-lookup"><span data-stu-id="95925-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="95925-121">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="95925-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
