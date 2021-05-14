---
title: Quarantaineorders
description: In dit onderwerp wordt beschreven hoe quarantaineorders kunnen worden gebruikt om voorraad te blokkeren.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956177"
---
# <a name="quarantine-orders"></a><span data-ttu-id="08a2a-103">Quarantaineorders</span><span class="sxs-lookup"><span data-stu-id="08a2a-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08a2a-104">In dit onderwerp wordt beschreven hoe quarantaineorders kunnen worden gebruikt om voorraad te blokkeren.</span><span class="sxs-lookup"><span data-stu-id="08a2a-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="08a2a-105">Met quarantaineorders kunt u voorraad blokkeren.</span><span class="sxs-lookup"><span data-stu-id="08a2a-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="08a2a-106">U wilt bijvoorbeeld artikelen om redenen van kwaliteitscontrole in quarantaine plaatsen.</span><span class="sxs-lookup"><span data-stu-id="08a2a-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="08a2a-107">Voorraad die in quarantaine is geplaatst, wordt verplaatst naar een quarantainemagazijn.</span><span class="sxs-lookup"><span data-stu-id="08a2a-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="08a2a-108">Als u gebruikmaakt van geavanceerde magazijnbeheerprocessen (in Magazijnbeheer), wordt quarantaineorderverwerking alleen gebruikt voor retourverkooporders.</span><span class="sxs-lookup"><span data-stu-id="08a2a-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="08a2a-109">Voorhanden voorraadartikelen in quarantaine plaatsen</span><span class="sxs-lookup"><span data-stu-id="08a2a-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="08a2a-110">Wanneer u artikelen in quarantaine plaatst, kunt u de quarantaineorders handmatig maken of het systeem zo instellen dat er automatisch quarantaineorders worden gemaakt tijdens de verwerking van inkomende artikelen.</span><span class="sxs-lookup"><span data-stu-id="08a2a-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="08a2a-111">Volg deze stappen om het systeem zo in te stellen dat het automatisch quarantaineorders genereert.</span><span class="sxs-lookup"><span data-stu-id="08a2a-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="08a2a-112">Ga naar **Voorraadbeheer \> Instellen \> Voorraad \> Artikelmodelgroepen**.</span><span class="sxs-lookup"><span data-stu-id="08a2a-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="08a2a-113">Selecteer een relevante modelgroep in het lijstvenster of maak een nieuwe modelgroep.</span><span class="sxs-lookup"><span data-stu-id="08a2a-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="08a2a-114">Schakel op het sneltabblad **Voorraadbeleid** het selectievakje **Quarantainebeheer** in.</span><span class="sxs-lookup"><span data-stu-id="08a2a-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="08a2a-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="08a2a-115">Close the page.</span></span>
1. <span data-ttu-id="08a2a-116">Geef in het veld **Quarantainemagazijn** voor de ontvangende magazijnen een standaardquarantainemagazijn op.</span><span class="sxs-lookup"><span data-stu-id="08a2a-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="08a2a-117">Wanneer een artikel dat in het magazijn is geregistreerd als ontvangen, behoort tot een modelgroep waarvoor het selectievakje **Quarantainebeheer** is ingeschakeld, wordt er door het systeem een quarantaineorder voor dat artikel gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="08a2a-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="08a2a-118">De quarantaineorder geeft werknemers de opdracht om het artikel naar het quarantainemagazijn te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="08a2a-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="08a2a-119">Wanneer u quarantaineorders handmatig maakt op de pagina **Quarantaineorders**, hoeft het artikel niet te worden ingesteld voor quarantainebeheer in de gekoppelde artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="08a2a-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="08a2a-120">Voor dit proces moet u de voorhanden voorraad opgeven die in quarantaine moet worden geplaatst, en het quarantainemagazijn dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="08a2a-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="08a2a-121">U kunt de quarantaineorderstatussen gebruiken om het proces plannen.</span><span class="sxs-lookup"><span data-stu-id="08a2a-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="08a2a-122">Statussen van quarantaineorder</span><span class="sxs-lookup"><span data-stu-id="08a2a-122">Quarantine order statuses</span></span>

<span data-ttu-id="08a2a-123">Quarantaineorders kunnen de volgende status hebben:</span><span class="sxs-lookup"><span data-stu-id="08a2a-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="08a2a-124">Gemaakt</span><span class="sxs-lookup"><span data-stu-id="08a2a-124">Created</span></span>
- <span data-ttu-id="08a2a-125">Gestart</span><span class="sxs-lookup"><span data-stu-id="08a2a-125">Started</span></span>
- <span data-ttu-id="08a2a-126">Gereedgemeld</span><span class="sxs-lookup"><span data-stu-id="08a2a-126">Reported as finished</span></span>
- <span data-ttu-id="08a2a-127">Beëindigd</span><span class="sxs-lookup"><span data-stu-id="08a2a-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="08a2a-128">Gemaakt</span><span class="sxs-lookup"><span data-stu-id="08a2a-128">Created</span></span>

<span data-ttu-id="08a2a-129">Wanneer een quarantaineorder handmatig is gemaakt, maar het artikel nog niet in het quarantainemagazijn is geplaatst, krijgt de quarantaineorder de status **Gemaakt**.</span><span class="sxs-lookup"><span data-stu-id="08a2a-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="08a2a-130">Er worden twee voorraadtransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="08a2a-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="08a2a-131">Eén transactie is een uitgiftetransactie die de status **In bestelling**, **Fysiek gereserveerd** of **Verzameld** kan hebben.</span><span class="sxs-lookup"><span data-stu-id="08a2a-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="08a2a-132">De andere transactie is een ontvangsttransactie die de status **Besteld** of **Geregistreerd** in het quarantainemagazijn kan hebben.</span><span class="sxs-lookup"><span data-stu-id="08a2a-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="08a2a-133">U kunt updates in de voorraad met de normale processen reserveren, kiezen en registreren.</span><span class="sxs-lookup"><span data-stu-id="08a2a-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="08a2a-134">Gestart</span><span class="sxs-lookup"><span data-stu-id="08a2a-134">Started</span></span>

<span data-ttu-id="08a2a-135">Wanneer een quarantaineorder de status **Gestart** heeft, wordt de voorraad verplaatst van het normale magazijn naar het quarantainemagazijn en worden twee voorraadtransacties gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="08a2a-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="08a2a-136">Een transactie heeft de status **Ingehouden** en de andere transactie heeft de status **Ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="08a2a-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="08a2a-137">Tegelijkertijd worden twee voorraadtransacties gemaakt voor het verwerken van de retouroverdracht.</span><span class="sxs-lookup"><span data-stu-id="08a2a-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="08a2a-138">Deze transacties hebben geen datum.</span><span class="sxs-lookup"><span data-stu-id="08a2a-138">These transactions aren't dated.</span></span> <span data-ttu-id="08a2a-139">Een transactie heeft de status **Fysiek gereserveerd** en de andere transactie heeft de status **Besteld**.</span><span class="sxs-lookup"><span data-stu-id="08a2a-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="08a2a-140">Gereedgemeld</span><span class="sxs-lookup"><span data-stu-id="08a2a-140">Reported as finished</span></span>

<span data-ttu-id="08a2a-141">Als u een gestarte quarantaineorder gereed wilt melden, opent u de order en selecteert u **Rapporteren als gereed** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="08a2a-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="08a2a-142">Het artikel wordt vrijgegeven uit quarantaine, maar wordt nog niet teruggeplaatst in het normale magazijn.</span><span class="sxs-lookup"><span data-stu-id="08a2a-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="08a2a-143">De terugplaatsing in het normale magazijn kan worden verwerkt via een artikelontvangstjournaal, dat kan worden geïnitialiseerd tijdens het gereedmeldingsproces.</span><span class="sxs-lookup"><span data-stu-id="08a2a-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="08a2a-144">Beëindigd</span><span class="sxs-lookup"><span data-stu-id="08a2a-144">Ended</span></span>

<span data-ttu-id="08a2a-145">Wanneer een quarantaineorder wordt beëindigd, wordt het artikel vanuit het quarantainemagazijn teruggeplaatst naar het normale magazijn.</span><span class="sxs-lookup"><span data-stu-id="08a2a-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="08a2a-146">De status van de artikeltransactie wordt ingesteld op *Verkocht* in het quarantainemagazijn en op *Ingekocht* in het normale magazijn.</span><span class="sxs-lookup"><span data-stu-id="08a2a-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="08a2a-147">Quarantaineorderuitval</span><span class="sxs-lookup"><span data-stu-id="08a2a-147">Quarantine order scrap</span></span>

<span data-ttu-id="08a2a-148">Als onderdeel van het quarantaineorderproces kunt u voorraad laten uitvallen.</span><span class="sxs-lookup"><span data-stu-id="08a2a-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="08a2a-149">Wanneer u uitval verwerkt, wordt de status van de voorraad ingesteld op *Verkocht* door een uitgiftetransactie vanuit het quarantainemagazijn.</span><span class="sxs-lookup"><span data-stu-id="08a2a-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08a2a-150">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="08a2a-150">Additional resources</span></span>

- [<span data-ttu-id="08a2a-151">Voorraadblokkering</span><span class="sxs-lookup"><span data-stu-id="08a2a-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
