---
title: Ladingen plannen via hubconsolidatie
description: In dit artikel wordt de functie beschreven voor het consolideren van zendingen in een hub bij het leveren van goederen vanuit verschillende magazijnen aan dezelfde klant, of wanneer u goederen ontvangt van meerdere leveranciers in hetzelfde magazijn.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 475fa9b73deeddd0f9118b0062e834a053fcb919
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="167e8-103">Ladingen plannen via hubconsolidatie</span><span class="sxs-lookup"><span data-stu-id="167e8-103">Plan loads using hub consolidation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="167e8-104">In dit artikel wordt de functie beschreven voor het consolideren van zendingen in een hub bij het leveren van goederen vanuit verschillende magazijnen aan dezelfde klant, of wanneer u goederen ontvangt van meerdere leveranciers in hetzelfde magazijn.</span><span class="sxs-lookup"><span data-stu-id="167e8-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="167e8-105">Kan het handig zijn om zendingen te consolideren in een hub bij het leveren van goederen vanuit verschillende magazijnen aan dezelfde klant, of wanneer goederen van meerdere leveranciers aan het magazijn worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="167e8-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="167e8-106">Ladingen opbouwen</span><span class="sxs-lookup"><span data-stu-id="167e8-106">Building loads</span></span>
<span data-ttu-id="167e8-107">Voordat u de hubconsolidatie kunt gebruiken, moet u de optie **Planning in transit** inschakelen op de pagina **Transportbeheerparameters**.</span><span class="sxs-lookup"><span data-stu-id="167e8-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="167e8-108">Ook moet u de hubs maken waar de consolidatie zal plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="167e8-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="167e8-109">In het volgende diagram ziet u een voorbeeld van hubconsolidatie.</span><span class="sxs-lookup"><span data-stu-id="167e8-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="167e8-110">In dit geval gaan verkooporders uit verschillende magazijnen naar dezelfde klant.</span><span class="sxs-lookup"><span data-stu-id="167e8-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="167e8-111">De basisladingen worden op de gebruikelijke manier gemaakt op basis van verkooporders met behulp van de pagina **Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="167e8-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="167e8-112">Als u de twee ladingen wilt samenvoegen in een hub voordat ze aan de klant worden geleverd, selecteert u op de pagina **Workbench ladingplanning**, in het veld **Transport**, de optie **Hubconsolidatie**.</span><span class="sxs-lookup"><span data-stu-id="167e8-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="167e8-113">Wanneer u de juiste hub selecteert voor elke lading, hebben de ladingen de hub als afleverbestemming.</span><span class="sxs-lookup"><span data-stu-id="167e8-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="167e8-114">Ook hebt u twee "aanvraagregels van transport" in de sectie **Vraag en aanbod** van de pagina **Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="167e8-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="167e8-115">Vervolgens kunt u deze twee lijnen toevoegen aan een nieuwe lading.</span><span class="sxs-lookup"><span data-stu-id="167e8-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="167e8-116">Deze nieuwe lading bevat beide verkooporderregels en bevat ook de hub als ophaaladres en klant A als afleverbestemming.</span><span class="sxs-lookup"><span data-stu-id="167e8-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="167e8-117">De drie ladingen zijn vervolgens gereed om te worden beoordeeld en doorgestuurd, net als elke andere lading.</span><span class="sxs-lookup"><span data-stu-id="167e8-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="167e8-118">U kunt voor elke lading iedere vervoerder selecteren die in het systeem wordt voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="167e8-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="167e8-119">[![Hubconsolidatie](./media/hubconsol.jpg)](./media/hubconsol.jpg) U kunt dezelfde methode ook gebruiken voor het consolideren van ladingen voor meerdere transferorders.</span><span class="sxs-lookup"><span data-stu-id="167e8-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="167e8-120">In dit geval is klant A in het voorgaande diagram een magazijn.</span><span class="sxs-lookup"><span data-stu-id="167e8-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="167e8-121">U kunt ook ladingen samenvoegen voor meerdere inkooporders, waarbij de ladingen door verschillende leveranciers in het magazijn worden afgeleverd.</span><span class="sxs-lookup"><span data-stu-id="167e8-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="167e8-122">U kunt meer dan één consolidatiehub hebben en kunt consolideren in meerdere hubs voor meer ladingen die afkomstig zijn uit verschillende magazijnen.</span><span class="sxs-lookup"><span data-stu-id="167e8-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="167e8-123">Nadat u uw basisladingen hebt opgebouwd en de optie voor hubconsolidatie gebruikt, bouwt u de nieuwe ladingen op door de geconsolideerde aanvraagregels van transport te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="167e8-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="167e8-124">Vervolgens beoordeelt u uw ladingen en stuurt u deze door.</span><span class="sxs-lookup"><span data-stu-id="167e8-124">You then rate and route your loads.</span></span>




