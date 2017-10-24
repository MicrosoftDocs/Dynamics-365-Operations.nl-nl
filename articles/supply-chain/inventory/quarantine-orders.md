---
title: Quarantaineorders
description: In dit artikel wordt beschreven hoe quarantaineorders worden gebruikt om voorraad te blokkeren.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17dde4a4e3380beb98eeb71c719fb898b40a94f7
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="quarantine-orders"></a><span data-ttu-id="1a95d-103">Quarantaineorders</span><span class="sxs-lookup"><span data-stu-id="1a95d-103">Quarantine orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1a95d-104">In dit artikel wordt beschreven hoe quarantaineorders worden gebruikt om voorraad te blokkeren.</span><span class="sxs-lookup"><span data-stu-id="1a95d-104">This article describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="1a95d-105">Quarantaineorders kunnen worden gebruikt om voorraad te blokkeren.</span><span class="sxs-lookup"><span data-stu-id="1a95d-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="1a95d-106">U wilt bijvoorbeeld artikelen om redenen van kwaliteitscontrole in quarantaine plaatsen.</span><span class="sxs-lookup"><span data-stu-id="1a95d-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="1a95d-107">Voorraad die in quarantaine is geplaatst, wordt verplaatst naar een quarantainemagazijn.</span><span class="sxs-lookup"><span data-stu-id="1a95d-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="1a95d-108">**Opmerking:** als u gebruikmaakt van geavanceerde magazijnbeheerprocessen (in Magazijnbeheer), wordt quarantaineorderverwerking alleen gebruikt voor retourverkooporders.</span><span class="sxs-lookup"><span data-stu-id="1a95d-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-onhand-inventory-items"></a><span data-ttu-id="1a95d-109">Voorhanden voorraadartikelen in quarantaine plaatsen</span><span class="sxs-lookup"><span data-stu-id="1a95d-109">Quarantine onhand inventory items</span></span>
<span data-ttu-id="1a95d-110">Wanneer u artikelen in quarantaine plaatst, kunt u de quarantaineorders handmatig maken of het systeem zo instellen dat de quarantaineorders automatisch worden gemaakt tijdens inkomende verwerking.</span><span class="sxs-lookup"><span data-stu-id="1a95d-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="1a95d-111">Als u quarantaineorders automatisch wilt maken, selecteert u de optie **Quarantainebeheer** op het tabblad **Voorraadbeleid** op de pagina **Artikelmodelgroepen**.</span><span class="sxs-lookup"><span data-stu-id="1a95d-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="1a95d-112">U moet ook een standaardquarantainemagazijn opgeven in het veld **Quarantainemagazijn** voor de magazijnen van ontvangst.</span><span class="sxs-lookup"><span data-stu-id="1a95d-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="1a95d-113">Wanneer de fysiek voorhanden voorraad wordt geregistreerd in een inkooporder of productieorder, worden in quarantaine geplaatste artikelen automatisch verplaatst naar een quarantainemagazijn in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1a95d-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1a95d-114">Deze verplaatsing vindt plaats omdat de status van de quarantaineorder is gewijzigd in **Gestart**.</span><span class="sxs-lookup"><span data-stu-id="1a95d-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="1a95d-115">Wanneer u quarantaineorders handmatig maakt, hoeft het artikel niet te worden ingesteld voor quarantainebeheer in de gekoppelde artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="1a95d-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="1a95d-116">Voor dit proces moet u de voorhanden voorraad opgeven die in quarantaine moet worden geplaatst, en het quarantainemagazijn dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1a95d-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="1a95d-117">U kunt de quarantaineorderstatussen gebruiken om het proces plannen.</span><span class="sxs-lookup"><span data-stu-id="1a95d-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="1a95d-118">Statussen van quarantaineorder</span><span class="sxs-lookup"><span data-stu-id="1a95d-118">Quarantine order statuses</span></span>
<span data-ttu-id="1a95d-119">Quarantaineorders kunnen de volgende status hebben:</span><span class="sxs-lookup"><span data-stu-id="1a95d-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="1a95d-120">Gemaakt</span><span class="sxs-lookup"><span data-stu-id="1a95d-120">Created</span></span>
-   <span data-ttu-id="1a95d-121">Gestart</span><span class="sxs-lookup"><span data-stu-id="1a95d-121">Started</span></span>
-   <span data-ttu-id="1a95d-122">Gereedgemeld</span><span class="sxs-lookup"><span data-stu-id="1a95d-122">Reported as finished</span></span>
-   <span data-ttu-id="1a95d-123">Beëindigd</span><span class="sxs-lookup"><span data-stu-id="1a95d-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="1a95d-124">Gemaakt</span><span class="sxs-lookup"><span data-stu-id="1a95d-124">Created</span></span>

<span data-ttu-id="1a95d-125">Wanneer een quarantaineorder handmatig is gemaakt, maar het artikel nog niet in het quarantainemagazijn is geplaatst, krijgt de quarantaineorder de status **Gemaakt**.</span><span class="sxs-lookup"><span data-stu-id="1a95d-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="1a95d-126">Er worden twee voorraadtransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1a95d-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="1a95d-127">Eén transactie is een uitgiftetransactie die de status **In bestelling**, **Fysiek gereserveerd** of **Verzameld** kan hebben.</span><span class="sxs-lookup"><span data-stu-id="1a95d-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="1a95d-128">De andere transactie is een ontvangsttransactie die de status **Besteld** of **Geregistreerd** in het quarantainemagazijn kan hebben.</span><span class="sxs-lookup"><span data-stu-id="1a95d-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="1a95d-129">U kunt updates in de voorraad met de normale processen reserveren, kiezen en registreren.</span><span class="sxs-lookup"><span data-stu-id="1a95d-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="1a95d-130">Gestart</span><span class="sxs-lookup"><span data-stu-id="1a95d-130">Started</span></span>

<span data-ttu-id="1a95d-131">Wanneer een quarantaineorder de status **Gestart** heeft, wordt de voorraad verplaatst van het normale magazijn naar het quarantainemagazijn en worden twee voorraadtransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1a95d-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="1a95d-132">Een transactie heeft de status **Ingehouden** en de andere transactie heeft de status **Ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="1a95d-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="1a95d-133">Tegelijkertijd worden twee voorraadtransacties gemaakt voor het verwerken van de retouroverdracht.</span><span class="sxs-lookup"><span data-stu-id="1a95d-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="1a95d-134">Deze transacties hebben geen datum.</span><span class="sxs-lookup"><span data-stu-id="1a95d-134">These transactions aren't dated.</span></span> <span data-ttu-id="1a95d-135">Een transactie heeft de status **Fysiek gereserveerd** en de andere transactie heeft de status **Besteld**.</span><span class="sxs-lookup"><span data-stu-id="1a95d-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="1a95d-136">Gereedgemeld</span><span class="sxs-lookup"><span data-stu-id="1a95d-136">Reported as finished</span></span>

<span data-ttu-id="1a95d-137">Als u op **Rapporteren als gereed** klikt, kunt u een gestarte quarantaineorder gereedmelden.</span><span class="sxs-lookup"><span data-stu-id="1a95d-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="1a95d-138">Het artikel wordt vrijgegeven uit quarantaine, maar wordt nog niet naar het normale magazijn teruggeplaatst.</span><span class="sxs-lookup"><span data-stu-id="1a95d-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="1a95d-139">Dit kan worden verwerkt via een artikelontvangstjournaal dat tijdens het proces voor gereedmelding kan worden geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="1a95d-139">The movement back to the regular warehouse can be procesed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="1a95d-140">Beëindigd</span><span class="sxs-lookup"><span data-stu-id="1a95d-140">Ended</span></span>

<span data-ttu-id="1a95d-141">Wanneer een quarantaineorder wordt beëindigd, wordt het artikel vanuit het quarantainemagazijn teruggeplaatst naar het normale magazijn.</span><span class="sxs-lookup"><span data-stu-id="1a95d-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="1a95d-142">De status van de artikeltransactie wordt ingesteld op **Verkocht** in het quarantainemagazijn en op **Ingekocht** in het normale magazijn.</span><span class="sxs-lookup"><span data-stu-id="1a95d-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="1a95d-143">Quarantaineorderuitval</span><span class="sxs-lookup"><span data-stu-id="1a95d-143">Quarantine order scrap</span></span>
<span data-ttu-id="1a95d-144">Als onderdeel van het quarantaineorderproces kunt u voorraad laten uitvallen.</span><span class="sxs-lookup"><span data-stu-id="1a95d-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="1a95d-145">Wanneer u uitval verwerkt, wordt de status van de voorraad ingesteld op **Verkocht** door een uitgiftetransactie vanuit het quarantainemagazijn.</span><span class="sxs-lookup"><span data-stu-id="1a95d-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="see-also"></a><span data-ttu-id="1a95d-146">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1a95d-146">See also</span></span>
--------

[<span data-ttu-id="1a95d-147">Voorraadblokkering</span><span class="sxs-lookup"><span data-stu-id="1a95d-147">Inventory blocking</span></span>](inventory-blocking.md)

