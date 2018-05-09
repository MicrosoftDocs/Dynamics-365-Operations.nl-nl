---
title: Uitgaand proces
description: Dit onderwerp biedt een overzicht van het uitgaande proces in Voorraadbeheer.
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c672a2ce6e962e49043cba4593a9899a8613c23e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="outbound-process"></a><span data-ttu-id="63437-103">Uitgaand proces</span><span class="sxs-lookup"><span data-stu-id="63437-103">Outbound process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63437-104">Dit onderwerp biedt een overzicht van het uitgaande proces in Voorraadbeheer.</span><span class="sxs-lookup"><span data-stu-id="63437-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="63437-105">Uitvoerorders</span><span class="sxs-lookup"><span data-stu-id="63437-105">Output orders</span></span>

<span data-ttu-id="63437-106">Uitvoerorders worden gebruikt om verkooporderregels en transferorderregels te koppelen aan de processen voor uitgaande orderverzamelingen waarvoor wordt gebruikgemaakt van orderverzamellijsten.</span><span class="sxs-lookup"><span data-stu-id="63437-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="63437-107">Wanneer orderverzamellijsten worden gegenereerd op basis van verkooporders of transferorders, worden er automatisch uitvoerorders en verzendingen gemaakt.</span><span class="sxs-lookup"><span data-stu-id="63437-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="63437-108">Een orderverzamellijst heeft een één-op-één-relatie met een zending.</span><span class="sxs-lookup"><span data-stu-id="63437-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="63437-109">De transferorderzending of pakbon van de verkooporder kan worden verwerkt vanuit de zending.</span><span class="sxs-lookup"><span data-stu-id="63437-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="63437-110">In het volgende diagram wordt een overzicht gegeven van het proces voor uitgaande orders.</span><span class="sxs-lookup"><span data-stu-id="63437-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="63437-111">[![Overzicht van het proces voor uitgaande orders](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="63437-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="63437-112">U kunt uitgaande regels instellen om te bepalen hoe het uitgaande proces moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="63437-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="63437-113">U kunt het verzendproces aansturen door middel van deze regels.</span><span class="sxs-lookup"><span data-stu-id="63437-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="63437-114">U kunt de regels in het bijzonder gebruiken om te bepalen tijdens welke fase van het proces een zending kan worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="63437-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="63437-115">De volgende instellingen bepalen hoe de uitgaande processen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="63437-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="63437-116">Status van de orderverzamelroute voor verkoop- en transferorders</span><span class="sxs-lookup"><span data-stu-id="63437-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="63437-117">Ga naar **Klant** \> **Instellingen** \> **Parameters van module Klanten** en selecteer op het tabblad **Updates** een waarde in het veld **Status orderverzamelroute**.</span><span class="sxs-lookup"><span data-stu-id="63437-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="63437-118">[![Veld Status orderverzamelroute voor verkooporders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="63437-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="63437-119">Als het veld **Status orderverzamelroute** is ingesteld op **Voltooid**, wordt het orderverzamelproces automatisch uitgevoerd als onderdeel van het proces voor het genereren van orderverzamellijsten.</span><span class="sxs-lookup"><span data-stu-id="63437-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="63437-120">Als het veld is ingesteld op **Geactiveerd**, moeten de regels van de orderverzamellijst handmatig worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="63437-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="63437-121">Dezelfde instellingen zijn van toepassing op transferorders.</span><span class="sxs-lookup"><span data-stu-id="63437-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="63437-122">Ga naar **Voorraadbeheer** \> **Instellingen** \> **Parameters voor voorraad- en magazijnbeheer** en selecteer op het tabblad **Transport** een waarde in het veld **Status orderverzamelroute**.</span><span class="sxs-lookup"><span data-stu-id="63437-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="63437-123">[![Veld Status orderverzamelroute voor transferorders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="63437-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="63437-124">Uitvoerorders voor voorraad beëindigen</span><span class="sxs-lookup"><span data-stu-id="63437-124">End output inventory orders</span></span>

<span data-ttu-id="63437-125">Ga naar **Voorraadbeheer** \> **Instellingen** \> **Parameters voor voorraad- en magazijnbeheer** en stel op het tabblad **Algemeen** de optie **Uitvoerorder voor voorraad beëindigen** in.</span><span class="sxs-lookup"><span data-stu-id="63437-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="63437-126">[![Optie Uitvoerorder voor voorraad beëindigen](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="63437-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="63437-127">Als de orderverzamellijsthoeveelheden worden verlaagd door de magazijnmedewerker, worden de betreffende voorraadorderhoeveelheden verwijderd uit de zending.</span><span class="sxs-lookup"><span data-stu-id="63437-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="63437-128">Als de orderverzamellijst op een bepaald moment wordt bijgewerkt, worden de resterende hoeveelheden weer gerapporteerd aan de order als de optie **Uitvoerorder voor voorraad beëindigen** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="63437-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="63437-129">Als de optie **Uitvoerorder voor voorraad beëindigen** is ingesteld op **Nee**, worden de resterende hoeveelheden bewaard als openstaande uitvoerorderhoeveelheid en moeten deze worden toegevoegd aan een nieuwe orderverzamellijst als onderdeel van de functie **Openstaande uitvoerorders**.</span><span class="sxs-lookup"><span data-stu-id="63437-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="63437-130">[![Opdracht Openstaande uitvoerorders in het menu Functies](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="63437-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="63437-131">[![Menu Functies op de pagina Openstaande uitvoerorders](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="63437-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="63437-132">Hoeveelheid verminderen</span><span class="sxs-lookup"><span data-stu-id="63437-132">Reduce quantity</span></span>

<span data-ttu-id="63437-133">De derde parameter die u gebruiken kunt als onderdeel van het proces voor het genereren van orderverzamellijsten, is de parameter **Hoeveelheid verminderen**.</span><span class="sxs-lookup"><span data-stu-id="63437-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="63437-134">De instelling van deze parameter werkt samen met de instelling **Reservering** om een reserveringsproces te genereren als onderdeel van de vrijgave naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="63437-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="63437-135">[![Parameter Hoeveelheid verminderen](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="63437-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="63437-136">Voorbeeld van een uitgaand proces voor een verkooporder</span><span class="sxs-lookup"><span data-stu-id="63437-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="63437-137">In dit voorbeeld is er een verkooporder voor twee artikelen.</span><span class="sxs-lookup"><span data-stu-id="63437-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="63437-138">Tijdens het genereren van de orderverzamellijst selecteert u de parameter **Hoeveelheid verminderen**.</span><span class="sxs-lookup"><span data-stu-id="63437-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="63437-139">Daarom worden orderverzamelregels alleen gemaakt en vrijgegeven voor beschikbare voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="63437-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="63437-140">De orderverzameling moet worden gerapporteerd via een registratieproces voor orderverzamellijsten (**Status orderverzamelroute** = **Geactiveerd**).</span><span class="sxs-lookup"><span data-stu-id="63437-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="63437-141">De voorraad die nog niet is gereserveerd, wordt gereserveerd tijdens het genereren van de orderverzamellijst.</span><span class="sxs-lookup"><span data-stu-id="63437-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="63437-142">De niet-beschikbare voorraad kan worden verwijderd uit de verkooporder of worden vrijgegeven aan het magazijn voor uitgaande verwerking op een later tijdstip, wanneer voorraad beschikbaar is voor orderverzameling.</span><span class="sxs-lookup"><span data-stu-id="63437-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="63437-143">[![De orderverzamellijst bijwerken](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="63437-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="63437-144">Zodra alle orderverzamelregels zijn verzameld op de pagina **Orderverzamellijstregistratie**, wordt de bijbehorende zending voltooid.</span><span class="sxs-lookup"><span data-stu-id="63437-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="63437-145">Het proces voor pakbonnen voor verkooporders kan vervolgens worden geïnitialiseerd op basis van de verzamelde voorraad.</span><span class="sxs-lookup"><span data-stu-id="63437-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="63437-146">[![Uitgaande zendingen bijwerken](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="63437-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

