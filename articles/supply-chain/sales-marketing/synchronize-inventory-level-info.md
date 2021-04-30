---
title: Voorraadcorrecties uit Supply Chain Management synchroniseren met Field Service
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om informatie op voorraadniveau te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910273"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="f4e3b-103">Voorraadcorrecties uit Supply Chain Management synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="f4e3b-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f4e3b-104">Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om informatie op voorraadniveau te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="f4e3b-105">[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f4e3b-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="f4e3b-106">Templates and tasks</span></span>
<span data-ttu-id="f4e3b-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van grijpvoorraadniveaus vanuit Supply Chain Management naar Field Service.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="f4e3b-108">**Sjabloontoewijzing in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="f4e3b-108">**Template in Data integration**</span></span>
- <span data-ttu-id="f4e3b-109">Productvoorraad (Supply Chain Management naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="f4e3b-110">**Taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="f4e3b-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="f4e3b-111">Productvoorraad</span><span class="sxs-lookup"><span data-stu-id="f4e3b-111">Product inventory</span></span>

<span data-ttu-id="f4e3b-112">De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van voorraadniveaus kan plaatsvinden:</span><span class="sxs-lookup"><span data-stu-id="f4e3b-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="f4e3b-113">Magazijnen (Supply Chain Management naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="f4e3b-114">Field Service-producten met Voorraadeenheid (Supply Chain Management naar Sales)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="f4e3b-115">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="f4e3b-115">Entity set</span></span>

| <span data-ttu-id="f4e3b-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="f4e3b-116">Field Service</span></span>                      | <span data-ttu-id="f4e3b-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f4e3b-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="f4e3b-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="f4e3b-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="f4e3b-119">Voorhanden Dataverse-voorraad per magazijn</span><span class="sxs-lookup"><span data-stu-id="f4e3b-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="f4e3b-120">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="f4e3b-120">Entity flow</span></span>
<span data-ttu-id="f4e3b-121">Voorraadniveaugegevens worden vanuit Finance and Operations naar Field Service verzonden voor geselecteerde producten.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="f4e3b-122">Voorraadniveaugegevens bevatten:</span><span class="sxs-lookup"><span data-stu-id="f4e3b-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="f4e3b-123">Voorhanden hoeveelheid (huidige geregistreerde fysieke hoeveelheid in het magazijn)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="f4e3b-124">Hoeveelheid in bestelling (totale geregistreerde hoeveelheid in bestelling, zoals verkooporders)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="f4e3b-125">Bestelde hoeveelheid (totale geregistreerde bestelde hoeveelheid, zoals inkooporders)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="f4e3b-126">Deze gegevens worden per vrijgegeven product geregistreerd voor elk magazijn en gesynchroniseerd op basis van wijzigingstracering wanneer het voorraadniveau verandert.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="f4e3b-127">In Field Service worden met de integratieoplossing voorraadjournalen voor de delta gemaakt om ervoor te zorgen dat de niveaus in Field Service overeenkomen met de niveaus in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="f4e3b-128">Supply Chain Management fungeert als master voor voorraadniveaus.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="f4e3b-129">Daarom is het belangrijk om de integratie voor werkorders, overboekingen en correcties van Field Service naar Supply Chain Management in te stellen als deze functionaliteit wordt gebruikt in Field Service. Daarnaast moeten voorraadniveaus vanuit Supply Chain Management worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="f4e3b-130">De producten en magazijnen waarvoor voorraadniveaus worden gemaakt via Supply Chain Management kunnen worden beheerd met Geavanceerde query's en filters (Power Query).</span><span class="sxs-lookup"><span data-stu-id="f4e3b-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="f4e3b-131">Het is mogelijk om meerdere magazijnen in Field Services te maken (met **Wordt extern beheerd = Nee**) en deze toe te wijzen aan één magazijn in Supply Chain Management met de functies voor Geavanceerde query's en filters.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="f4e3b-132">Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau beheert en alleen updates verzendt naar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="f4e3b-133">In dit geval ontvangt Field Service geen updates over voorraadniveaus van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="f4e3b-134">Zie voor meer informatie [Voorraadcorrecties vanuit Field Service synchroniseren naar Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) en [Werkorders in Field Service synchroniseren met verkooporders in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="f4e3b-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="f4e3b-135">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="f4e3b-135">Field Service CRM solution</span></span>
<span data-ttu-id="f4e3b-136">De entiteit **Externe productvoorraad** is een nieuwe entiteit die alleen voor de back-end wordt gebruikt in de integratie.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="f4e3b-137">Deze entiteit ontvangt de voorraadniveauwaarden uit Supply Chain Management tijdens de integratie en transformeert die waarden vervolgens in Journalen voor handmatige voorraad waarmee vervolgens de voorraadproducten in het Magazijn worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f4e3b-138">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="f4e3b-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="f4e3b-139">Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="f4e3b-139">Data integration</span></span>
<span data-ttu-id="f4e3b-140">Het project werkt alleen als u ervoor zorgt dat de integratiesleutel wordt bijgewerkt voor msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="f4e3b-141">Ga naar **Gegevensintegratie > Verbindingssets**.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="f4e3b-142">Selecteer de gebruikte verbindingsset.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="f4e3b-143">Controleer op het tabblad **Integratiesleutel** of de volgende sleutels aan msdynce_externalproductinventories zijn toegevoegd:</span><span class="sxs-lookup"><span data-stu-id="f4e3b-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="f4e3b-144">msdynce_productnumber (productnummer)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="f4e3b-145">msdynce_warehouseid (magazijn-id)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="f4e3b-146">Gegevensintegratieproject</span><span class="sxs-lookup"><span data-stu-id="f4e3b-146">Data integration project</span></span>
<span data-ttu-id="f4e3b-147">U kunt filters toepassen met Geavanceerde query´s en filters, zodat dat alleen bepaalde producten en magazijnen informatie over het voorraadniveau vanuit Supply Chain Management naar Field Service worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="f4e3b-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f4e3b-148">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="f4e3b-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="f4e3b-149">Productvoorraad (Supply Chain Management naar Field Service): Productvoorraad</span><span class="sxs-lookup"><span data-stu-id="f4e3b-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="f4e3b-150">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]