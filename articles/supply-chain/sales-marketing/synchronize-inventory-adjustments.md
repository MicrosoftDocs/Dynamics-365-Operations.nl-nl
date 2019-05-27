---
title: Voorraadoverboekingen en -correcties vanuit Field Service synchroniseren naar Finance and Operations
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om informatie over voorraadcorrecties en -overboekingen te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: e94fa87c2f8b66574d6c5b2930cebf2e1b144fea
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536291"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="3dc08-103">Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dc08-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3dc08-104">In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om informatie over voorraadcorrecties en -overboekingen te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="3dc08-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="3dc08-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="3dc08-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3dc08-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="3dc08-106">Templates and tasks</span></span>
<span data-ttu-id="3dc08-107">De volgende sjabloon en onderliggende taken worden gebruikt om voorraadcorrecties en -overboekingen te synchroniseren van Microsoft Dynamics 365 for Field Service met Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dc08-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="3dc08-108">**Sjablonen in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="3dc08-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="3dc08-109">Voorraadcorrectie (Field Service naar Fin en Ops)</span><span class="sxs-lookup"><span data-stu-id="3dc08-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="3dc08-110">Voorraadoverboekingen (Field Service naar Fin en Ops)</span><span class="sxs-lookup"><span data-stu-id="3dc08-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="3dc08-111">**Taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="3dc08-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="3dc08-112">Voorraadcorrecties</span><span class="sxs-lookup"><span data-stu-id="3dc08-112">Inventory Adjustments</span></span>
- <span data-ttu-id="3dc08-113">Voorraadoverboekingen</span><span class="sxs-lookup"><span data-stu-id="3dc08-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="3dc08-114">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="3dc08-114">Entity set</span></span>
| <span data-ttu-id="3dc08-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="3dc08-115">Field Service</span></span>                     | <span data-ttu-id="3dc08-116">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="3dc08-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="3dc08-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="3dc08-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="3dc08-118">Kopteksten en regels van journaalnamen voor CDS-voorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="3dc08-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="3dc08-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="3dc08-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="3dc08-120">Kopteksten en regels van journaalnamen voor CDS-voorraadoverboeking</span><span class="sxs-lookup"><span data-stu-id="3dc08-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="3dc08-121">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="3dc08-121">Entity flow</span></span>
<span data-ttu-id="3dc08-122">Voorraadcorrecties en -overboekingen die worden uitgevoerd in Field Service, worden gesynchroniseerd met Finance and Operations nadat **Boekstatus** van **Gemaakt** is gewijzigd in **Geboekt**.</span><span class="sxs-lookup"><span data-stu-id="3dc08-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="3dc08-123">Als dit gebeurt, wordt de correctie- of overboekingsorder vergrendeld en wordt deze alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="3dc08-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="3dc08-124">Dit betekent dat correcties en overboekingen in Finance and Operations kunnen worden geboekt, maar niet kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="3dc08-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="3dc08-125">In Finance and Operations kunt u een batchtaak instellen om automatisch de correcties te boeken en overboekingsvoorraadjournalen over te boeken die zijn gegenereerd bij de integratie.</span><span class="sxs-lookup"><span data-stu-id="3dc08-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="3dc08-126">Zie de volgende vereisten voor meer informatie over het inschakelen van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="3dc08-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="3dc08-127">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="3dc08-127">Field Service CRM solution</span></span> 
<span data-ttu-id="3dc08-128">Het veld **Voorraadeenheid** is toegevoegd aan de entiteit **Product**.</span><span class="sxs-lookup"><span data-stu-id="3dc08-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="3dc08-129">Dit veld is vereist omdat de verkoop- en voorraadeenheid niet altijd overeenkomt in Finance and Operations en de voorraadeenheid is nodig voor de magazijnvoorraad in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dc08-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="3dc08-130">Wanneer u het product voor een voorraadcorrectieproduct instelt voor zowel voorraadcorrecties als voorraadoverboekingen, wordt de eenheid gebaseerd op de voorraadproductwaarde.</span><span class="sxs-lookup"><span data-stu-id="3dc08-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="3dc08-131">Als een waarde wordt gevonden, wordt het veld **Eenheid** vergrendeld voor het voorraadcorrectieproduct</span><span class="sxs-lookup"><span data-stu-id="3dc08-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="3dc08-132">Het veld **Boekstatus** is toegevoegd aan zowel de entiteit **Voorraadcorrectie** als de entiteit **Voorraadoverboeking**.</span><span class="sxs-lookup"><span data-stu-id="3dc08-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="3dc08-133">Dit veld wordt gebruikt als een filter wanneer een correctie of overboeking wordt verzonden naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dc08-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="3dc08-134">De standaardwaarde voor dit veld is Gemaakt (1), maar wordt niet verzonden naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dc08-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="3dc08-135">Wanneer u de waarde wijzigt in Geboekt (2), wordt deze verzonden naar Finance and Operations, maar daarna kunt u de correctie of overboeking niet wjzigen of nieuwe regels toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3dc08-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="3dc08-136">Het veld **Nummerreeks** is toegevoegd aan de entiteit **Voorraadcorrectieproduct**.</span><span class="sxs-lookup"><span data-stu-id="3dc08-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="3dc08-137">Dit veld zorgt ervoor dat de integratie een uniek nummer heeft, zodat de correctie kan worden gemaakt en bijgewerkt met de integratie.</span><span class="sxs-lookup"><span data-stu-id="3dc08-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="3dc08-138">Wanneer u uw eerste voorraadcorrectieproduct maakt, wordt er een nieuwe record gemaakt in de P2C-entiteit **Automatisch nummeren** om de nummerreeks en het gebruikte voorvoegsel te behouden.</span><span class="sxs-lookup"><span data-stu-id="3dc08-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="3dc08-139">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="3dc08-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="3dc08-140">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="3dc08-140">Finance and Operations</span></span>
<span data-ttu-id="3dc08-141">De integratievoorraadjournalen die worden gegenereerd door de integratie, kunnen automatisch worden geboekt met een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="3dc08-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="3dc08-142">Dit wordt ingeschakeld via **Voorraadbeheer > Periodieke taken > CDS-integratie > Voorraadjournalen voor integratie boeken**.</span><span class="sxs-lookup"><span data-stu-id="3dc08-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3dc08-143">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="3dc08-143">Template mapping in Data integration</span></span>

<span data-ttu-id="3dc08-144">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="3dc08-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="3dc08-145">Voorraadcorrectie (Field Service naar Fin and Ops): Voorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="3dc08-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="3dc08-146">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="3dc08-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="3dc08-147">Voorraadoverboeking (Field Service naar Fin and Ops): Voorraadoverboeking</span><span class="sxs-lookup"><span data-stu-id="3dc08-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="3dc08-148">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="3dc08-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
