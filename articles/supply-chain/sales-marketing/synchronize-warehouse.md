---
title: Magazijnen vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt om magazijnen van Microsoft Dynamics 365 for Finance and Operations te synchroniseren met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835665"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="4ef74-103">Magazijnen van Finance and Operations synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="4ef74-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4ef74-104">In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt om magazijnen van Microsoft Dynamics 365 for Finance and Operations te synchroniseren met Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="4ef74-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="4ef74-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="4ef74-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4ef74-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="4ef74-106">Templates and tasks</span></span>
<span data-ttu-id="4ef74-107">De volgende sjabloon en onderliggende taken worden gebruikt om magazijnen te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="4ef74-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="4ef74-108">**Sjabloontoewijzing in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="4ef74-108">**Template in Data integration**</span></span>
- <span data-ttu-id="4ef74-109">Magazijnen (Fin and Ops naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="4ef74-109">Warehouses (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="4ef74-110">**Taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="4ef74-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="4ef74-111">Magazijn</span><span class="sxs-lookup"><span data-stu-id="4ef74-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="4ef74-112">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="4ef74-112">Entity set</span></span>
| <span data-ttu-id="4ef74-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="4ef74-113">Field Service</span></span>    | <span data-ttu-id="4ef74-114">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="4ef74-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="4ef74-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="4ef74-115">msdyn_warehouses</span></span> | <span data-ttu-id="4ef74-116">Magazijnen</span><span class="sxs-lookup"><span data-stu-id="4ef74-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="4ef74-117">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="4ef74-117">Entity flow</span></span>
<span data-ttu-id="4ef74-118">Magazijnen die worden gemaakt en beheerd in Finance and Operations kunnen worden gesynchroniseerd met Field Service via een Common Data Service-gegevensintegratieproject (CDS).</span><span class="sxs-lookup"><span data-stu-id="4ef74-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="4ef74-119">Met de functie voor geavanceerde query's en projectfilters kunnen de magazijnen die u wilt synchroniseren met Field Service worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="4ef74-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="4ef74-120">Magazijnen die vanuit Finance and Operations kunnen worden gesynchroniseerd, worden gemaakt in Field Service met het veld **Wordt extern onderhouden** ingesteld op **Ja** en de record ingesteld op alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="4ef74-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="4ef74-121">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="4ef74-121">Field Service CRM solution</span></span>
<span data-ttu-id="4ef74-122">Ter ondersteuning van de integratie tussen Field Service en Finance and Operations is extra functionaliteit nodig in de CRM-oplossing Field Service.</span><span class="sxs-lookup"><span data-stu-id="4ef74-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="4ef74-123">In de oplossing is het veld **Wordt extern beheerd** toegevoegd aan de entiteit **Magazijn (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="4ef74-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="4ef74-124">Op basis van dit veld kunt u zien of het magazijn wordt beheerd vanuit Finance and Operations of dat het alleen bestaat in Field Service.</span><span class="sxs-lookup"><span data-stu-id="4ef74-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="4ef74-125">De instellingen voor deze velden zijn:</span><span class="sxs-lookup"><span data-stu-id="4ef74-125">The settings for this field include:</span></span>
- <span data-ttu-id="4ef74-126">**Ja**: het magazijn is afkomstig uit Finance and Operations en kan niet worden bewerkt in Sales.</span><span class="sxs-lookup"><span data-stu-id="4ef74-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="4ef74-127">**Nee**: het magazijn is rechtstreeks ingevoerd in Field Service en wordt hier beheerd.</span><span class="sxs-lookup"><span data-stu-id="4ef74-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="4ef74-128">Gebruik het veld **Wordt extern beheerd** om de synchronisatie van voorraadniveaus, -correcties, -overboekingen en -gebruik voor werkorders te beheren.</span><span class="sxs-lookup"><span data-stu-id="4ef74-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="4ef74-129">Alleen magazijnen met **Wordt extern beheerd** = **Ja** kunnen worden gebruikt voor rechtstreekse synchronisatie met hetzelfde magazijn in het andere systeem.</span><span class="sxs-lookup"><span data-stu-id="4ef74-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="4ef74-130">Het is mogelijk om meerdere magazijnen in Field Service te maken (met **Wordt extern beheerd** = Nee) en deze toe te wijzen aan één magazijn in Finance and Operations, met de functies voor geavanceerde query's en filters.</span><span class="sxs-lookup"><span data-stu-id="4ef74-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="4ef74-131">Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau maakt en alleen updates verzendt naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ef74-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="4ef74-132">In dit geval ontvangt Field Service geen updates over voorraadniveaus van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ef74-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="4ef74-133">Zie voor meer informatie [Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) en [Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="4ef74-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="4ef74-134">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="4ef74-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="4ef74-135">Gegevensintegratieproject</span><span class="sxs-lookup"><span data-stu-id="4ef74-135">Data Integration project</span></span>
<span data-ttu-id="4ef74-136">Werk voordat u de magazijnen synchroniseert de functie Geavanceerde query en filtering bij zodat alleen de gewenste magazijnen vanuit Finance and Operations worden overgebracht naar Field Service.</span><span class="sxs-lookup"><span data-stu-id="4ef74-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="4ef74-137">Houd er rekening mee dat u het magazijn in Field Service nodig hebt om het toe te passen op werkorders, correcties en overboekingen.</span><span class="sxs-lookup"><span data-stu-id="4ef74-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="4ef74-138">Om te controleren of de **Integratiesleutel** aanwezig is voor **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="4ef74-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="4ef74-139">Ga naar Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="4ef74-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="4ef74-140">Selecteer het tabblad **Verbindingsset**.</span><span class="sxs-lookup"><span data-stu-id="4ef74-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="4ef74-141">Selecteer de verbindingsset die wordt gebruikt voor synchronisatie van werkorders.</span><span class="sxs-lookup"><span data-stu-id="4ef74-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="4ef74-142">Selecteer het tabblad **Integratiesleutel**.</span><span class="sxs-lookup"><span data-stu-id="4ef74-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="4ef74-143">Zoek msdyn_warehouses en bevestig dat de sleutel **msdyn_name (naam)** is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4ef74-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="4ef74-144">Als deze niet wordt weergegeven, voegt u deze toe door te klikken op **Sleutel toevoegen** en klikt u op **Opslaan** bovenaan de pagina</span><span class="sxs-lookup"><span data-stu-id="4ef74-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4ef74-145">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="4ef74-145">Template mapping in Data integration</span></span>

<span data-ttu-id="4ef74-146">In de volgende afbeelding ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="4ef74-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a><span data-ttu-id="4ef74-147">Magazijnen (Fin and Ops naar Field Service): Magazijn</span><span class="sxs-lookup"><span data-stu-id="4ef74-147">Warehouses (Fin and Ops to Field Service): Warehouse</span></span>

<span data-ttu-id="4ef74-148">[![Sjabloontoewijzing in Gegevensintegratie](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="4ef74-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
