---
title: Voorraadcorrecties uit Supply Chain Management synchroniseren met Field Service
description: In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt om magazijnen van Dynamics 365 Supply Chain Management te synchroniseren met Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
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
ms.openlocfilehash: 051bbee28d45a6d4142beef40c5a173f2ca30a11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243028"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="57a1d-103">Voorraadcorrecties uit Supply Chain Management synchroniseren met Field Service</span><span class="sxs-lookup"><span data-stu-id="57a1d-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="57a1d-104">In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt om magazijnen van Dynamics 365 Supply Chain Management te synchroniseren met Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="57a1d-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="57a1d-105">[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="57a1d-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="57a1d-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="57a1d-106">Templates and tasks</span></span>
<span data-ttu-id="57a1d-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van magazijnen vanuit Supply Chain Management naar Field Service.</span><span class="sxs-lookup"><span data-stu-id="57a1d-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="57a1d-108">**Sjabloontoewijzing in Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="57a1d-108">**Template in Data integration**</span></span>
- <span data-ttu-id="57a1d-109">Magazijnen (Supply Chain Management naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="57a1d-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="57a1d-110">**Taak in het project Gegevensintegratie**</span><span class="sxs-lookup"><span data-stu-id="57a1d-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="57a1d-111">Magazijn</span><span class="sxs-lookup"><span data-stu-id="57a1d-111">Warehouse</span></span>

## <a name="table-set"></a><span data-ttu-id="57a1d-112">Tabelset</span><span class="sxs-lookup"><span data-stu-id="57a1d-112">Table set</span></span>
| <span data-ttu-id="57a1d-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="57a1d-113">Field Service</span></span>    | <span data-ttu-id="57a1d-114">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="57a1d-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="57a1d-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="57a1d-115">msdyn_warehouses</span></span> | <span data-ttu-id="57a1d-116">Magazijnen</span><span class="sxs-lookup"><span data-stu-id="57a1d-116">Warehouses</span></span>                             |

## <a name="table-flow"></a><span data-ttu-id="57a1d-117">Tabelstroom</span><span class="sxs-lookup"><span data-stu-id="57a1d-117">Table flow</span></span>
<span data-ttu-id="57a1d-118">Magazijnen die worden gemaakt en beheerd in Supply Chain Management, kunnen worden gesynchroniseerd met Field Service via een Microsoft Dataverse-gegevensintegratieproject (CDS).</span><span class="sxs-lookup"><span data-stu-id="57a1d-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="57a1d-119">Met de functie voor geavanceerde query's en projectfilters kunnen de magazijnen die u wilt synchroniseren met Field Service worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="57a1d-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="57a1d-120">Magazijnen die vanuit Supply Chain Management worden gesynchroniseerd, worden gemaakt in Field Service met de kolom **Wordt extern beheerd** ingesteld op **Ja** en de record ingesteld op alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="57a1d-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** column set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="57a1d-121">Field Service CRM-oplossing</span><span class="sxs-lookup"><span data-stu-id="57a1d-121">Field Service CRM solution</span></span>
<span data-ttu-id="57a1d-122">Ter ondersteuning van de integratie tussen Field Service en Supply Chain Management is extra functionaliteit nodig in de CRM-oplossing Field Service.</span><span class="sxs-lookup"><span data-stu-id="57a1d-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="57a1d-123">In de oplossing is de kolom **Wordt extern beheerd** toegevoegd aan de tabel **Magazijn (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="57a1d-123">In the solution, the **Is Maintained Externally** column has been added to the **Warehouse (msdyn_warehouses)** table.</span></span> <span data-ttu-id="57a1d-124">Op basis van deze kolom kunt u zien of het magazijn wordt beheerd vanuit Supply Chain Management of dat het alleen bestaat in Field Service.</span><span class="sxs-lookup"><span data-stu-id="57a1d-124">This column helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="57a1d-125">De instellingen voor deze kolom zijn:</span><span class="sxs-lookup"><span data-stu-id="57a1d-125">The settings for this column include:</span></span>
- <span data-ttu-id="57a1d-126">**Ja** – het product is afkomstig uit Supply Chain Management en kan niet worden bewerkt in Sales.</span><span class="sxs-lookup"><span data-stu-id="57a1d-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="57a1d-127">**Nee**: het magazijn is rechtstreeks ingevoerd in Field Service en wordt hier beheerd.</span><span class="sxs-lookup"><span data-stu-id="57a1d-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="57a1d-128">Gebruik de kolom **Wordt extern beheerd** om de synchronisatie van voorraadniveaus, -correcties, -overboekingen en -gebruik voor werkorders te beheren.</span><span class="sxs-lookup"><span data-stu-id="57a1d-128">The **Is Externally Maintained** column helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="57a1d-129">Alleen magazijnen met **Wordt extern beheerd** = **Ja** kunnen worden gebruikt voor rechtstreekse synchronisatie met hetzelfde magazijn in het andere systeem.</span><span class="sxs-lookup"><span data-stu-id="57a1d-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="57a1d-130">Het is mogelijk om meerdere magazijnen in Field Service te maken (met **Wordt extern beheerd** = Nee) en deze toe te wijzen aan één magazijn, met de functies voor geavanceerde query's en filters.</span><span class="sxs-lookup"><span data-stu-id="57a1d-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="57a1d-131">Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau beheert en alleen updates naar Supply Chain Management verzendt.</span><span class="sxs-lookup"><span data-stu-id="57a1d-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="57a1d-132">In dit geval ontvangt Field Service geen updates over voorraadniveaus van Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="57a1d-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="57a1d-133">Zie voor meer informatie [Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) en [Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="57a1d-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="57a1d-134">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="57a1d-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="57a1d-135">Gegevensintegratieproject</span><span class="sxs-lookup"><span data-stu-id="57a1d-135">Data Integration project</span></span>
<span data-ttu-id="57a1d-136">Werk voordat u de magazijnen synchroniseert de functie Geavanceerde query en filtering bij zodat alleen de gewenste magazijnen vanuit Supply Chain Management worden overgebracht naar Field Service.</span><span class="sxs-lookup"><span data-stu-id="57a1d-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="57a1d-137">Houd er rekening mee dat u het magazijn in Field Service nodig hebt om het toe te passen op werkorders, correcties en overboekingen.</span><span class="sxs-lookup"><span data-stu-id="57a1d-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="57a1d-138">Om te controleren of de **Integratiesleutel** aanwezig is voor **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="57a1d-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="57a1d-139">Ga naar Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="57a1d-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="57a1d-140">Selecteer het tabblad **Verbindingsset**.</span><span class="sxs-lookup"><span data-stu-id="57a1d-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="57a1d-141">Selecteer de verbindingsset die wordt gebruikt voor synchronisatie van werkorders.</span><span class="sxs-lookup"><span data-stu-id="57a1d-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="57a1d-142">Selecteer het tabblad **Integratiesleutel**.</span><span class="sxs-lookup"><span data-stu-id="57a1d-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="57a1d-143">Zoek msdyn_warehouses en bevestig dat de sleutel **msdyn_name (naam)** is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="57a1d-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="57a1d-144">Als deze niet wordt weergegeven, voegt u deze toe door te klikken op **Sleutel toevoegen** en klikt u op **Opslaan** bovenaan de pagina</span><span class="sxs-lookup"><span data-stu-id="57a1d-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="57a1d-145">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="57a1d-145">Template mapping in Data integration</span></span>

<span data-ttu-id="57a1d-146">In de volgende afbeelding ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="57a1d-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="57a1d-147">Magazijnen (Supply Chain Management naar Field Service): Warehouse</span><span class="sxs-lookup"><span data-stu-id="57a1d-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="57a1d-148">[![Sjabloontoewijzing in Gegevensintegratie](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="57a1d-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]