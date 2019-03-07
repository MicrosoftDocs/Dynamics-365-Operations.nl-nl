---
title: Voorraadniveaugegevens vanuit Finance and Operations synchroniseren naar Field Service
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om informatie op voorraadniveau te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "356778"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="ce63d-103">Informatie over voorraadniveau uit Finance and Operations synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="ce63d-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ce63d-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om informatie op voorraadniveau te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="ce63d-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ce63d-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="ce63d-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ce63d-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="ce63d-106">Templates and tasks</span></span>
<span data-ttu-id="ce63d-107">De volgende sjabloon en onderliggende taken worden gebruikt om beschikbare voorraadniveaus te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="ce63d-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ce63d-108">**Sjabloontoewijzing in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="ce63d-108">**Template in Data integration**</span></span>
- <span data-ttu-id="ce63d-109">Productvoorraad (Finance and Operations naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="ce63d-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="ce63d-110">**Taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="ce63d-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="ce63d-111">Productvoorraad</span><span class="sxs-lookup"><span data-stu-id="ce63d-111">Product inventory</span></span>

<span data-ttu-id="ce63d-112">De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van voorraadniveaus kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="ce63d-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="ce63d-113">Magazijnen (Finance and Operations naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="ce63d-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="ce63d-114">Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales)</span><span class="sxs-lookup"><span data-stu-id="ce63d-114">Field Service products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="ce63d-115">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="ce63d-115">Entity set</span></span>

| <span data-ttu-id="ce63d-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="ce63d-116">Field Service</span></span>                      | <span data-ttu-id="ce63d-117">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="ce63d-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="ce63d-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="ce63d-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="ce63d-119">Voorhanden CDS-voorraad per magazijn</span><span class="sxs-lookup"><span data-stu-id="ce63d-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="ce63d-120">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="ce63d-120">Entity flow</span></span>
<span data-ttu-id="ce63d-121">Voorraadniveaugegevens worden vanuit Finance and Operations naar Field Service verzonden voor geselecteerde producten.</span><span class="sxs-lookup"><span data-stu-id="ce63d-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="ce63d-122">Voorraadniveaugegevens bevatten:</span><span class="sxs-lookup"><span data-stu-id="ce63d-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="ce63d-123">Voorhanden hoeveelheid (huidige geregistreerde fysieke hoeveelheid in het magazijn)</span><span class="sxs-lookup"><span data-stu-id="ce63d-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="ce63d-124">Hoeveelheid in bestelling (totale geregistreerde hoeveelheid in bestelling, zoals verkooporders)</span><span class="sxs-lookup"><span data-stu-id="ce63d-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="ce63d-125">Bestelde hoeveelheid (totale geregistreerde bestelde hoeveelheid, zoals inkooporders)</span><span class="sxs-lookup"><span data-stu-id="ce63d-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="ce63d-126">Deze gegevens worden per vrijgegeven product geregistreerd voor elk magazijn en gesynchroniseerd op basis van wijzigingstracering wanneer het voorraadniveau verandert.</span><span class="sxs-lookup"><span data-stu-id="ce63d-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="ce63d-127">In Field Service worden met de integratieoplossing voorraadjournalen voor de delta gemaakt om ervoor te zorgen dat de niveaus in Field Service overeenkomen met de niveaus in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ce63d-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="ce63d-128">Finance and Operations fungeert als master voor voorraadniveaus.</span><span class="sxs-lookup"><span data-stu-id="ce63d-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="ce63d-129">Daarom is het belangrijk om de integratie voor werkorders, overboekingen en correcties van Field Service naar Finance and Operations in te stellen als deze functionaliteit wordt gebruikt in Field Service. Daarnaast moeten voorraadniveaus vanuit Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="ce63d-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="ce63d-130">De producten en magazijnen waarvoor voorraadniveaus worden gemaakt via Finance and Operations kunnen worden beheerd met Geavanceerde Query en filtering (Power Query).</span><span class="sxs-lookup"><span data-stu-id="ce63d-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="ce63d-131">Het is mogelijk om meerdere magazijnen in Field Services te maken (met **Wordt extern beheerd = Nee**) en deze toe te wijzen aan één magazijn in Finance and Operations, met de functies voor geavanceerde query's en filters.</span><span class="sxs-lookup"><span data-stu-id="ce63d-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="ce63d-132">Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau beheert en alleen updates verzendt naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ce63d-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="ce63d-133">In dit geval ontvangt Field Service geen updates over voorraadniveaus van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ce63d-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="ce63d-134">Zie voor meer informatie [Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) en [Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="ce63d-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ce63d-135">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="ce63d-135">Field Service CRM solution</span></span>
<span data-ttu-id="ce63d-136">De entiteit **Externe productvoorraad** is een nieuwe entiteit die alleen voor de back-end wordt gebruikt in de integratie.</span><span class="sxs-lookup"><span data-stu-id="ce63d-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="ce63d-137">Deze entiteit ontvangt de voorraadniveauwaarden uit Finance and Operations tijdens de integratie en transformeert die waarden vervolgens in journalen voor handmatige voorraad waarmee vervolgens de voorraadproducten in het magazijn worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="ce63d-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ce63d-138">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="ce63d-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="ce63d-139">Gegevensintegratieproject</span><span class="sxs-lookup"><span data-stu-id="ce63d-139">Data integration project</span></span>
<span data-ttu-id="ce63d-140">U kunt filters toepassen met Geavanceerde query en filtering zodat dat alleen bepaalde producten en magazijnen vanuit Finance and Operations naar Field Service worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="ce63d-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ce63d-141">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="ce63d-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="ce63d-142">Productvoorraad (Finance and Operations naar Field Service): Productvoorraad</span><span class="sxs-lookup"><span data-stu-id="ce63d-142">Product inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="ce63d-143">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="ce63d-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
