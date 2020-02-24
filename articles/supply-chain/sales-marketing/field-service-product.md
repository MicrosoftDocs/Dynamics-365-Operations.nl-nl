---
title: Producten in Supply Chain Management synchroniseren met producten in Field Service
description: In dit onderwerp worden de sjablonen besproken en de onderliggende taak die wordt gebruikt om producten van Dynamics 365 Supply Chain Management te synchroniseren met Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c87e4cbfa375ef99d00c9a145c190af78e912d56
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029400"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="a05e6-103">Producten in Supply Chain Management synchroniseren met producten in Field Service</span><span class="sxs-lookup"><span data-stu-id="a05e6-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a05e6-104">Dit onderwerp bespreekt de sjablonen en onderliggende taak die worden gebruikt om producten te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="a05e6-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="a05e6-105">De gebruikte sjabloon **Field Service-producten (Supply Chain Management naar Field Service)** is gebaseerd op de sjabloon **Producten (Supply Chain Management naar Sales) - Direct** van Prospect naar Contant geld.</span><span class="sxs-lookup"><span data-stu-id="a05e6-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="a05e6-106">Zie voor meer informatie [Producten (Supply Chain Management naar Sales) - Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="a05e6-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="a05e6-107">In dit onderwerp worden alleen de verschillen beschreven tussen de sjablonen **Field Service-producten (Supply Chain Management naar Field Service)** en **Producten (Supply Chain Management naar Sales) - Direct**.</span><span class="sxs-lookup"><span data-stu-id="a05e6-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a05e6-108">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="a05e6-108">Templates and tasks</span></span>

<span data-ttu-id="a05e6-109">**Naam van de sjabloon in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="a05e6-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="a05e6-110">Field Service-producten (Supply Chain Management naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="a05e6-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="a05e6-111">**Naam van de taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="a05e6-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="a05e6-112">Producten - Producten</span><span class="sxs-lookup"><span data-stu-id="a05e6-112">Products - Products</span></span>

<span data-ttu-id="a05e6-113">De gebruikte sjabloon **Field Service-producten (Supply Chain Management naar Field Service)** bevat één toewijzing die niet is inbegrepen in de sjabloon **Producten (Supply Chain Management naar Sales) - Direct**.</span><span class="sxs-lookup"><span data-stu-id="a05e6-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="a05e6-114">Deze toewijzing zorgt ervoor dat het vereiste Field Service-veld **Producttype Field Service** correct wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="a05e6-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```Text
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="a05e6-115">De volgende waardetoewijzing wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a05e6-115">The following value mapping is used.</span></span>

```Text
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="a05e6-116">In Supply Chain Management wordt de waarde **Producttype Field Service** in de gegevensentiteit **Verkoopbare vrijgegeven producten** als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="a05e6-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="a05e6-117">**Voorraad:** producttype = product en Artikelmodelgroep, Product in voorraad = True</span><span class="sxs-lookup"><span data-stu-id="a05e6-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="a05e6-118">**Niet-voorraad:** producttype = product en Artikelmodelgroep, Product in voorraad = False</span><span class="sxs-lookup"><span data-stu-id="a05e6-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="a05e6-119">**Service:** Producttype = Service</span><span class="sxs-lookup"><span data-stu-id="a05e6-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a05e6-120">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="a05e6-120">Template mapping in Data integration</span></span>

<span data-ttu-id="a05e6-121">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="a05e6-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="a05e6-122">Field Service-producten (Supply Chain Management naar Field Service): Producten - Producten</span><span class="sxs-lookup"><span data-stu-id="a05e6-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="a05e6-123">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="a05e6-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
