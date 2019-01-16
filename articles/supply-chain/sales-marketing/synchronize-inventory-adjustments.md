---
title: Voorraadoverboekingen en -correcties vanuit Field Service synchroniseren naar Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van voorraadcorrecties en -overboekingen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="a11db-103">Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a11db-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a11db-104">In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van voorraadcorrecties en -overboekingen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.</span><span class="sxs-lookup"><span data-stu-id="a11db-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a11db-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="a11db-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a11db-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="a11db-106">Templates and tasks</span></span>
<span data-ttu-id="a11db-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van voorraadcorrecties en -overboekingen vanuit Microsoft Dynamics 365 for Field Service naar Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a11db-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="a11db-108">**Naam van de sjablonen in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="a11db-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="a11db-109">Voorraadcorrectie (Field Service naar Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a11db-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="a11db-110">Voorraadoverboekingen (Field Service naar Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a11db-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="a11db-111">**Namen van de taken in de projecten Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="a11db-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="a11db-112">Voorraadcorrecties</span><span class="sxs-lookup"><span data-stu-id="a11db-112">Inventory Adjustments</span></span>
- <span data-ttu-id="a11db-113">Voorraadoverboekingen</span><span class="sxs-lookup"><span data-stu-id="a11db-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="a11db-114">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="a11db-114">Entity set</span></span>
| <span data-ttu-id="a11db-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="a11db-115">Field Service</span></span>                     | <span data-ttu-id="a11db-116">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="a11db-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="a11db-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="a11db-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="a11db-118">Kopteksten en regels van journaalnamen voor CDS-voorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="a11db-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="a11db-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="a11db-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="a11db-120">Kopteksten en regels van journaalnamen voor CDS-voorraadoverboeking</span><span class="sxs-lookup"><span data-stu-id="a11db-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="a11db-121">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="a11db-121">Entity flow</span></span>
<span data-ttu-id="a11db-122">Voorraadcorrecties en -overboekingen die worden uitgevoerd in Field Service worden gesynchroniseerd naar Finance and Operations wanneer **Boekstatus** van Gemaakt is gewijzigd in Geboekt.</span><span class="sxs-lookup"><span data-stu-id="a11db-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="a11db-123">Wanneer dit gebeurt, wordt de correctie- of overboekingsorder vergrendeld en alleen-lezen, aangezien correcties en overboekingen in Finance and Operations kunnen worden geboekt en dus niet kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="a11db-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="a11db-124">In Finance and Operations kunt u een batchverwerking instellen om automatisch de correcties te boeken en de voorraadjournalen over te boeken die zijn gegenereerd bij de integratie.</span><span class="sxs-lookup"><span data-stu-id="a11db-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="a11db-125">Zie de vereiste hieronder voor meer informatie over het inschakelen van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="a11db-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="a11db-126">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="a11db-126">Field Service CRM solution</span></span> 
<span data-ttu-id="a11db-127">Het veld Voorraadeenheid is toegevoegd aan de entiteit Product.</span><span class="sxs-lookup"><span data-stu-id="a11db-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="a11db-128">Dit veld is vereist omdat de verkoop- en voorraadeenheid niet altijd overeenkomen in Operations en voor de magazijnvoorraad in Operations de voorraadeenheid nodig is.</span><span class="sxs-lookup"><span data-stu-id="a11db-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="a11db-129">Wanneer u het product voor een voorraadcorrectieproduct instelt voor zowel voorraadcorrecties als voorraadoverboekingen, wordt de eenheid gebaseerd op het voorraadproduct.</span><span class="sxs-lookup"><span data-stu-id="a11db-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="a11db-130">Als een waarde wordt gevonden, wordt het veld Eenheid vergrendeld voor het voorraadcorrectieproduct</span><span class="sxs-lookup"><span data-stu-id="a11db-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="a11db-131">Het veld Boekstatus is toegevoegd aan de entiteit Voorraadcorrectie en de entiteit Voorraadoverdracht.</span><span class="sxs-lookup"><span data-stu-id="a11db-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="a11db-132">Dit veld wordt gebruikt als een filter voor wanneer een correctie of overboeking wordt verzonden naar Operations.</span><span class="sxs-lookup"><span data-stu-id="a11db-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="a11db-133">Het veld wordt standaard ingesteld op Gemaakt (1) en wordt vervolgens niet verzonden naar Operations.</span><span class="sxs-lookup"><span data-stu-id="a11db-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="a11db-134">Wanneer u dit wijzigt in Geboekt (2), wordt dit verzonden naar Operations. In dat geval kunt u niets meer wijzigen in de correctie of overboeking of nieuwe regels toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a11db-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="a11db-135">Het veld Nummerreeks is toegevoegd aan de entiteit Voorraadcorrectieproduct.</span><span class="sxs-lookup"><span data-stu-id="a11db-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="a11db-136">Hierdoor heeft de integratie een uniek nummer op basis waarvan kan worden bepaald of iets moet worden gemaakt of bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="a11db-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="a11db-137">Wanneer u uw eerste voorraadcorrectieproduct maakt, wordt er een nieuwe record gemaakt in de P2C-entiteit Automatisch nummeren om de nummerreeks en het gebruikte voorvoegsel te behouden.</span><span class="sxs-lookup"><span data-stu-id="a11db-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a11db-138">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="a11db-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="a11db-139">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a11db-139">In Finance and Operations</span></span>
<span data-ttu-id="a11db-140">De integratievoorraadjournalen die worden gegenereerd door de integratie kunnen automatisch worden geboekt met een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="a11db-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="a11db-141">Dit wordt ingeschakeld via: Voorraadbeheer > Periodieke taken > CDS-integratie > Voorraadjournalen voor integratie boeken</span><span class="sxs-lookup"><span data-stu-id="a11db-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a11db-142">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="a11db-142">Template mapping in Data integration</span></span>

<span data-ttu-id="a11db-143">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="a11db-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="a11db-144">Voorraadcorrectie (Field Service naar Finance and Operations): Voorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="a11db-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="a11db-145">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="a11db-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="a11db-146">Voorraadoverboeking (Field Service naar Finance and Operations): Voorraadoverboeking</span><span class="sxs-lookup"><span data-stu-id="a11db-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="a11db-147">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="a11db-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

