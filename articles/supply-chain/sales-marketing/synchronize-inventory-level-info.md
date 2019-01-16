---
title: Voorraadniveaugegevens vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van voorraadniveaugegevens vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="235ef-103">Voorraadniveaugegevens vanuit Finance and Operations synchroniseren naar Field Service</span><span class="sxs-lookup"><span data-stu-id="235ef-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="235ef-104">In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van voorraadniveaugegevens vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.</span><span class="sxs-lookup"><span data-stu-id="235ef-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="235ef-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="235ef-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="235ef-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="235ef-106">Templates and tasks</span></span>
<span data-ttu-id="235ef-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van voorhanden voorraadniveaus vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="235ef-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="235ef-108">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="235ef-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="235ef-109">Productvoorraad (Finance and Operations naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="235ef-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="235ef-110">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="235ef-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="235ef-111">Productvoorraad</span><span class="sxs-lookup"><span data-stu-id="235ef-111">Product inventory</span></span>

<span data-ttu-id="235ef-112">De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van voorraadniveaus kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="235ef-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="235ef-113">Magazijnen (Finance and Operations naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="235ef-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="235ef-114">Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales)</span><span class="sxs-lookup"><span data-stu-id="235ef-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="235ef-115">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="235ef-115">Entity set</span></span>

| <span data-ttu-id="235ef-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="235ef-116">Field Service</span></span>                      | <span data-ttu-id="235ef-117">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="235ef-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="235ef-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="235ef-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="235ef-119">Voorhanden CDS-voorraad per magazijn</span><span class="sxs-lookup"><span data-stu-id="235ef-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="235ef-120">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="235ef-120">Entity flow</span></span>
<span data-ttu-id="235ef-121">Voorraadniveaugegevens worden vanuit Finance and Operations naar Field Service verzonden voor bepaalde producten.</span><span class="sxs-lookup"><span data-stu-id="235ef-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="235ef-122">Voorraadniveaugegevens bevatten onder andere informatie over het volgende:</span><span class="sxs-lookup"><span data-stu-id="235ef-122">The inventory level information include:</span></span> 
- <span data-ttu-id="235ef-123">Voorhanden hoeveelheid (huidige geregistreerde fysieke hoeveelheid in het magazijn)</span><span class="sxs-lookup"><span data-stu-id="235ef-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="235ef-124">Hoeveelheid in bestelling (totale geregistreerde hoeveelheid in bestelling, d.w.z. verkooporders)</span><span class="sxs-lookup"><span data-stu-id="235ef-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="235ef-125">Bestelde hoeveelheid (totale geregistreerde bestelde hoeveelheid, d.w.z. inkooporders)</span><span class="sxs-lookup"><span data-stu-id="235ef-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="235ef-126">Deze gegevens worden per vrijgegeven product geregistreerd voor elk magazijn en gesynchroniseerd op basis van wijzigingstracering wanneer het voorraadniveau verandert.</span><span class="sxs-lookup"><span data-stu-id="235ef-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="235ef-127">In Field Service worden met de integratieoplossing voorraadjournalen voor de delta gemaakt om ervoor te zorgen dat de niveaus in Field Service overeenkomen met de niveaus in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="235ef-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="235ef-128">Finance and Operations fungeert als master voor voorraadniveaus.</span><span class="sxs-lookup"><span data-stu-id="235ef-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="235ef-129">Daarom is het belangrijk om de integratie voor werkorders, overboekingen en correcties van Field Service naar Finance and Operations in te stellen als deze functionaliteit wordt gebruikt in Field Service. Daarnaast moeten voorraadniveaus vanuit Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="235ef-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="235ef-130">De producten en magazijnen waarvoor voorraadniveaus worden gemaakt via Finance and Operations kunnen worden beheerd met Geavanceerde Query en filtering (Power Query).</span><span class="sxs-lookup"><span data-stu-id="235ef-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="235ef-131">Opmerking: het is mogelijk om meerdere magazijnen in Field Services te maken (met Wordt extern beheerd = Nee) en deze toe te wijzen aan één magazijn in Finance and Operations, met de functies voor geavanceerde query's en filters.</span><span class="sxs-lookup"><span data-stu-id="235ef-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="235ef-132">Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau maakt en alleen updates verzendt naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="235ef-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="235ef-133">In dit geval ontvangt Field Service geen updates over voorraadniveaus van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="235ef-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="235ef-134">Zie Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations en Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="235ef-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="235ef-135">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="235ef-135">Field Service CRM solution</span></span>
<span data-ttu-id="235ef-136">De entiteit Externe productvoorraad is een nieuwe entiteit die alleen voor de back-end wordt gebruikt in de integratie.</span><span class="sxs-lookup"><span data-stu-id="235ef-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="235ef-137">Het ontvangt de voorraadniveauwaarden uit Finance and Operations tijdens de integratie en transformeert die waarden vervolgens in journalen voor handmatige voorraad waarmee vervolgens de voorraadproducten in het magazijn worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="235ef-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="235ef-138">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="235ef-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="235ef-139">In het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="235ef-139">In the Data Integration project</span></span>
<span data-ttu-id="235ef-140">Pas filters toe met Geavanceerde query en filtering om in te stellen dat alleen voorraadniveaugegevens voor de gewenste producten en magazijnen vanuit Finance and Operations naar Field Service worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="235ef-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="235ef-141">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="235ef-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="235ef-142">Productvoorraad (Finance and Operations naar Field Service): Productvoorraad</span><span class="sxs-lookup"><span data-stu-id="235ef-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="235ef-143">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="235ef-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

