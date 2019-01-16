---
title: Magazijnen vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van magazijnen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="76c3a-103">Magazijnen vanuit Finance and Operations synchroniseren naar Field Service</span><span class="sxs-lookup"><span data-stu-id="76c3a-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="76c3a-104">In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van magazijnen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.</span><span class="sxs-lookup"><span data-stu-id="76c3a-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="76c3a-105">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="76c3a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="76c3a-106">Sjablonen en taken</span><span class="sxs-lookup"><span data-stu-id="76c3a-106">Templates and tasks</span></span>
<span data-ttu-id="76c3a-107">De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van magazijnen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="76c3a-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="76c3a-108">**Naam van de sjabloon in Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="76c3a-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="76c3a-109">Magazijnen (Finance and Operations naar Field Service)</span><span class="sxs-lookup"><span data-stu-id="76c3a-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="76c3a-110">**Namen van de taken in het project Gegevensintegratie:**</span><span class="sxs-lookup"><span data-stu-id="76c3a-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="76c3a-111">Magazijn</span><span class="sxs-lookup"><span data-stu-id="76c3a-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="76c3a-112">Entiteitset</span><span class="sxs-lookup"><span data-stu-id="76c3a-112">Entity set</span></span>
| <span data-ttu-id="76c3a-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="76c3a-113">Field Service</span></span>    | <span data-ttu-id="76c3a-114">Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="76c3a-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="76c3a-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="76c3a-115">msdyn_warehouses</span></span> | <span data-ttu-id="76c3a-116">Magazijnen</span><span class="sxs-lookup"><span data-stu-id="76c3a-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="76c3a-117">Entiteitstroom</span><span class="sxs-lookup"><span data-stu-id="76c3a-117">Entity flow</span></span>
<span data-ttu-id="76c3a-118">Magazijnen die worden gemaakt en beheerd in Finance and Operations kunnen worden gesynchroniseerd met Field Service via een Common Data Service-gegevensintegratieproject (CDS).</span><span class="sxs-lookup"><span data-stu-id="76c3a-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="76c3a-119">Met de functie voor geavanceerde query's en projectfilters kunt u bepalen welke magazijnen worden gesynchroniseerd met Field Service.</span><span class="sxs-lookup"><span data-stu-id="76c3a-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="76c3a-120">Magazijnen die vanuit Finance and Operations kunnen worden gesynchroniseerd, worden gemaakt in Field Service met het veld Wordt extern onderhouden ingesteld op Ja en de record ingesteld op alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="76c3a-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="76c3a-121">Field Service CRM-oplossing Ter ondersteuning van de integratie tussen Field Service en Finance and Operations is extra functionaliteit nodig in de CRM-oplossing Field Service.</span><span class="sxs-lookup"><span data-stu-id="76c3a-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="76c3a-122">Het oplossing omvat de volgende wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="76c3a-122">The solution includes the following changes.</span></span>
<span data-ttu-id="76c3a-123">Het veld **Wordt extern beheerd** is toegevoegd aan de entiteit **Magazijn (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="76c3a-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="76c3a-124">Op basis van dit veld kunt u zien of het magazijn wordt beheerd vanuit Operations of dat het alleen bestaat in Field Service.</span><span class="sxs-lookup"><span data-stu-id="76c3a-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="76c3a-125">Ja: het magazijn is afkomstig uit Finance and Operations en kan niet worden bewerkt in Sales.</span><span class="sxs-lookup"><span data-stu-id="76c3a-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="76c3a-126">Nee: het magazijn is rechtstreeks ingevoerd in Field Service en wordt hier beheerd.</span><span class="sxs-lookup"><span data-stu-id="76c3a-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="76c3a-127">Gebruik het veld **Wordt extern beheerd** om de synchronisatie van voorraadniveaus, -correcties, -overboekingen en -gebruik voor werkorders te beheren.</span><span class="sxs-lookup"><span data-stu-id="76c3a-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="76c3a-128">Alleen magazijnen met **Wordt extern beheerd** = Ja kunnen worden gebruikt voor rechtstreekse synchronisatie met hetzelfde magazijn in het andere systeem.</span><span class="sxs-lookup"><span data-stu-id="76c3a-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="76c3a-129">Opmerking: het is mogelijk om meerdere magazijnen in Field Services te maken (met **Wordt extern beheerd** = Nee) en deze toe te wijzen aan één magazijn in Finance and Operations, met de functies voor geavanceerde query's en filters.</span><span class="sxs-lookup"><span data-stu-id="76c3a-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="76c3a-130">Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau maakt en alleen updates verzendt naar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="76c3a-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="76c3a-131">In dit geval ontvangt Field Service geen updates over voorraadniveaus van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="76c3a-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="76c3a-132">Zie Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations en Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="76c3a-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="76c3a-133">Vereisten en instellingen voor toewijzing</span><span class="sxs-lookup"><span data-stu-id="76c3a-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="76c3a-134">In het project Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="76c3a-134">In the Data Integration project</span></span>
<span data-ttu-id="76c3a-135">Werk voordat u de magazijnen synchroniseert de functie Geavanceerde query en filtering bij zodat alleen de gewenste magazijnen vanuit Finance and Operations worden overgebracht naar Field Service.</span><span class="sxs-lookup"><span data-stu-id="76c3a-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="76c3a-136">Houd er rekening mee dat u het magazijn in Field Service nodig hebt om het toe te passen op werkorders, correcties en overboekingen.</span><span class="sxs-lookup"><span data-stu-id="76c3a-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="76c3a-137">Controleer of de **integratiesleutel** aanwezig is voor **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="76c3a-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="76c3a-138">Ga naar Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="76c3a-138">Go to Data Integration</span></span>
2. <span data-ttu-id="76c3a-139">Selecteer het tabblad **Verbindingsset**</span><span class="sxs-lookup"><span data-stu-id="76c3a-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="76c3a-140">Selecteer de verbindingsset die wordt gebruikt voor synchronisatie van werksorders</span><span class="sxs-lookup"><span data-stu-id="76c3a-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="76c3a-141">Selecteer het tabblad **Integratiesleutel**</span><span class="sxs-lookup"><span data-stu-id="76c3a-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="76c3a-142">Zoek msdyn_warehouses en controleer of de sleutel **msdyn_name (naam)** wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="76c3a-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="76c3a-143">Als deze niet wordt weergegeven, voegt u deze toe door te klikken op **Sleutel toevoegen** en klikt u op **Opslaan** bovenaan de pagina</span><span class="sxs-lookup"><span data-stu-id="76c3a-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="76c3a-144">Sjabloontoewijzing in Gegevensintegratie</span><span class="sxs-lookup"><span data-stu-id="76c3a-144">Template mapping in Data integration</span></span>

<span data-ttu-id="76c3a-145">In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="76c3a-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="76c3a-146">Magazijnen (Finance and Operations naar Field Service): Magazijn</span><span class="sxs-lookup"><span data-stu-id="76c3a-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="76c3a-147">[![Sjabloontoewijzing in Gegevensintegratie](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="76c3a-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

