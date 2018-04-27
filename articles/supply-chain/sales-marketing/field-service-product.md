---
title: Producten van Finance and Operations synchroniseren met producten in Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taak aan de orde voor het synchroniseren van producten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: nl-nl
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="7b982-103">Producten van Finance and Operations synchroniseren met producten in Field Service</span><span class="sxs-lookup"><span data-stu-id="7b982-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b982-104">In dit onderwerp komen de sjablonen en onderliggende taak aan de orde voor het synchroniseren van producten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="7b982-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="7b982-105">De gebruikte sjabloon **Field Service-producten (Fin and Ops naar Field Service)** is gebaseerd op de sjabloon **Producten (Fin and Ops naar Sales) - Direct** van Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="7b982-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="7b982-106">Zie voor meer informatie [Producten (Fin and Ops naar Sales) - Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="7b982-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="7b982-107">In dit onderwerp worden alleen de verschillen beschreven tussen de sjablonen **Field Service-producten (Fin and Ops naar Field Service)** en **Producten (Fin and Ops naar Sales) - Direct**.</span><span class="sxs-lookup"><span data-stu-id="7b982-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7b982-108">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="7b982-108">Templates and tasks</span></span>

<span data-ttu-id="7b982-109">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="7b982-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="7b982-110">Field Service-producten (Fin and Ops naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="7b982-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="7b982-111">**Naam van de taak in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="7b982-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="7b982-112">Producten - Producten</span><span class="sxs-lookup"><span data-stu-id="7b982-112">Products - Products</span></span>

<span data-ttu-id="7b982-113">De sjabloon **Field Service-producten (Fin and Ops naar Field Service)** omvat één toewijzing die niet is ogpenomen in sjabloon **Producten (Fin and Ops naar Sales) - Direct**.</span><span class="sxs-lookup"><span data-stu-id="7b982-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="7b982-114">Deze toewijzing zorgt ervoor dat het vereiste Field Service-veld **Producttype Field Service** correct wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="7b982-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="7b982-115">De volgende waardetoewijzing wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7b982-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="7b982-116">In Finance and Operations wordt de waarde **Producttype Field Service** in de gegevensentiteit **Verkoopbare vrijgegeven producten** als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="7b982-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="7b982-117">**Voorraad:** producttype = product en Artikelmodelgroep, Product in voorraad = True</span><span class="sxs-lookup"><span data-stu-id="7b982-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="7b982-118">**Niet-voorraad:** producttype = product en Artikelmodelgroep, Product in voorraad = False</span><span class="sxs-lookup"><span data-stu-id="7b982-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="7b982-119">**Service:** Producttype = Service</span><span class="sxs-lookup"><span data-stu-id="7b982-119">**Service:** Product type = Service</span></span>

