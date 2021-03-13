---
title: Voorraadoverboekingen en correcties uit Field Service synchroniseren met Supply Chain Management
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om informatie over voorraadcorrecties en -overboekingen te synchroniseren van Dynamics 365 Supply Chain Management met Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: a598f0356034a22ee7fc0902360b8862a1944558
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010967"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="b7664-103">Voorraadoverboekingen en correcties uit Field Service synchroniseren met Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b7664-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b7664-104">In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om informatie over voorraadcorrecties en -overboekingen te synchroniseren van Dynamics 365 Supply Chain Management met Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="b7664-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="b7664-105">[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="b7664-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b7664-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="b7664-106">Templates and tasks</span></span>
<span data-ttu-id="b7664-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van voorraadcorrecties en overboekingen vanuit Field Service naar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b7664-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="b7664-108">**Sjablonen in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="b7664-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="b7664-109">Voorraadcorrectie (Field Service naar Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="b7664-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="b7664-110">Voorraadoverboekingen (Field Service naar Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="b7664-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="b7664-111">**Taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="b7664-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="b7664-112">Voorraadcorrecties</span><span class="sxs-lookup"><span data-stu-id="b7664-112">Inventory Adjustments</span></span>
- <span data-ttu-id="b7664-113">Voorraadoverboekingen</span><span class="sxs-lookup"><span data-stu-id="b7664-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="b7664-114">Tabelset</span><span class="sxs-lookup"><span data-stu-id="b7664-114">Table set</span></span>
| <span data-ttu-id="b7664-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="b7664-115">Field Service</span></span>                     | <span data-ttu-id="b7664-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b7664-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="b7664-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="b7664-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="b7664-118">Dataverse: kopteksten en regels van journalen voor voorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="b7664-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="b7664-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="b7664-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="b7664-120">Dataverse: kopteksten en regels van journalen voor voorraadoverboeking</span><span class="sxs-lookup"><span data-stu-id="b7664-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="b7664-121">Tabelstroom</span><span class="sxs-lookup"><span data-stu-id="b7664-121">Table flow</span></span>
<span data-ttu-id="b7664-122">Voorraadcorrecties en -overboekingen die worden uitgevoerd in Field Service, worden gesynchroniseerd met Supply Chain Management nadat de **Boekstatus** van **Gemaakt** is gewijzigd in **Geboekt**.</span><span class="sxs-lookup"><span data-stu-id="b7664-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="b7664-123">Als dit gebeurt, wordt de correctie- of overboekingsorder vergrendeld en wordt deze alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="b7664-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="b7664-124">Dit betekent dat correcties en overboekingen in Supply Chain Management kunnen worden geboekt, maar niet kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b7664-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="b7664-125">In Supply Chain Management kunt u een batchtaak instellen om automatisch de correcties te boeken en overboekingsvoorraadjournalen over te boeken die zijn gegenereerd bij de integratie.</span><span class="sxs-lookup"><span data-stu-id="b7664-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="b7664-126">Zie de volgende vereisten voor meer informatie over het inschakelen van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="b7664-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b7664-127">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="b7664-127">Field Service CRM solution</span></span> 
<span data-ttu-id="b7664-128">De kolom **Voorraadeenheid** is toegevoegd aan de tabel **Product**.</span><span class="sxs-lookup"><span data-stu-id="b7664-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="b7664-129">Deze kolom is vereist omdat de Verkoop- en voorraadeenheid niet altijd overeenkomt in Supply Chain Management en de Voorraadeenheid nodig is voor de Magazijnvoorraad in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b7664-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="b7664-130">Wanneer u het product voor een voorraadcorrectieproduct instelt voor zowel voorraadcorrecties als voorraadoverboekingen, wordt de eenheid gebaseerd op de voorraadproductwaarde.</span><span class="sxs-lookup"><span data-stu-id="b7664-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="b7664-131">Als een waarde wordt gevonden, wordt de kolom **Eenheid** vergrendeld voor het voorraadcorrectieproduct</span><span class="sxs-lookup"><span data-stu-id="b7664-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="b7664-132">De kolom **Boekstatus** is toegevoegd aan zowel de tabel **Voorraadcorrectie** als de tabel **Voorraadoverboeking**.</span><span class="sxs-lookup"><span data-stu-id="b7664-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="b7664-133">Deze kolom wordt gebruikt als een filter wanneer een correctie of overboeking wordt verzonden naar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b7664-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="b7664-134">De standaardwaarde voor deze kolom is Gemaakt (1), maar wordt niet verzonden naar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b7664-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="b7664-135">Wanneer u de waarde wijzigt in Geboekt (2), wordt deze verzonden naar Supply Chain Management, maar daarna kunt u de correctie of overboeking niet wijzigen of nieuwe regels toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b7664-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="b7664-136">De kolom **Nummerreeks** is toegevoegd aan de tabel **Voorraadcorrectieproduct**.</span><span class="sxs-lookup"><span data-stu-id="b7664-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="b7664-137">Deze kolom zorgt ervoor dat de integratie een uniek nummer heeft, zodat de correctie kan worden gemaakt en bijgewerkt met de integratie.</span><span class="sxs-lookup"><span data-stu-id="b7664-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="b7664-138">Wanneer u uw eerste voorraadcorrectieproduct maakt, wordt er een nieuwe record gemaakt in de P2C-tabel **Automatisch nummeren** om de nummerreeks en het gebruikte voorvoegsel te behouden.</span><span class="sxs-lookup"><span data-stu-id="b7664-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b7664-139">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="b7664-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="b7664-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b7664-140">Supply Chain Management</span></span>
<span data-ttu-id="b7664-141">De integratievoorraadjournalen die worden gegenereerd door de integratie, kunnen automatisch worden geboekt met een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="b7664-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="b7664-142">Dit wordt ingeschakeld via **Voorraadbeheer > Periodieke taken > Dataverse-integratie > Voorraadjournalen voor integratie boeken**.</span><span class="sxs-lookup"><span data-stu-id="b7664-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b7664-143">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="b7664-143">Template mapping in Data integration</span></span>

<span data-ttu-id="b7664-144">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="b7664-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="b7664-145">Voorraadcorrectie (Field Service naar Supply Chain Management): Voorraadcorrectie</span><span class="sxs-lookup"><span data-stu-id="b7664-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="b7664-146">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="b7664-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="b7664-147">Voorraadoverboeking (Field Service naar Supply Chain Management): Voorraadoverboeking</span><span class="sxs-lookup"><span data-stu-id="b7664-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="b7664-148">[![Sjabloontoewijzing in Gegevensintegratie](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="b7664-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
