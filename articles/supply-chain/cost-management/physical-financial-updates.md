---
title: Fysieke en financiële updates
description: Dit onderwerp biedt een overzicht van de typen transacties die voorraadhoeveelheden vergroten of verkleinen.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba628dbf63d3b124583e6b873530f1459b07562
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547881"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="94d88-103">Fysieke en financiële updates</span><span class="sxs-lookup"><span data-stu-id="94d88-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94d88-104">Dit onderwerp biedt een overzicht van de typen transacties die voorraadhoeveelheden vergroten of verkleinen.</span><span class="sxs-lookup"><span data-stu-id="94d88-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="94d88-105">Voorraadtransacties kunnen in Microsoft Dynamics 365 for Finance and Operations fysiek en financieel worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="94d88-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="94d88-106">Bepaalde typen van fysieke en financiële transacties verhogen voorraadhoeveelheden, terwijl andere de hoeveelheid verlagen.</span><span class="sxs-lookup"><span data-stu-id="94d88-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="94d88-107">Fysieke toename</span><span class="sxs-lookup"><span data-stu-id="94d88-107">Physical increases</span></span>
<span data-ttu-id="94d88-108">Wanneer u een fysieke transactie boekt, wordt de status van de transactierecord **Ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="94d88-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="94d88-109">De volgende transacties worden beschouwd als een fysieke toename:</span><span class="sxs-lookup"><span data-stu-id="94d88-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="94d88-110">Ontvangst van inkooporder</span><span class="sxs-lookup"><span data-stu-id="94d88-110">Purchase order receipt</span></span>
-   <span data-ttu-id="94d88-111">Retour van pakbon voor verkooporder</span><span class="sxs-lookup"><span data-stu-id="94d88-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="94d88-112">Een productieorder gereedmelden</span><span class="sxs-lookup"><span data-stu-id="94d88-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="94d88-113">Bijproduct in een productieorderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="94d88-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="94d88-114">Financiële toename</span><span class="sxs-lookup"><span data-stu-id="94d88-114">Financial increases</span></span>
<span data-ttu-id="94d88-115">Wanneer u een financiële transactie boekt, wordt de status van de transactierecord die de hoeveelheid vergroot **Ingekocht**.</span><span class="sxs-lookup"><span data-stu-id="94d88-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="94d88-116">De volgende transacties worden beschouwd als een financiële toename:</span><span class="sxs-lookup"><span data-stu-id="94d88-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="94d88-117">Leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="94d88-117">Vendor invoice</span></span>
-   <span data-ttu-id="94d88-118">Verkooporderfactuur voor een retour</span><span class="sxs-lookup"><span data-stu-id="94d88-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="94d88-119">Kostprijsberekening voor productieorder</span><span class="sxs-lookup"><span data-stu-id="94d88-119">Production order costing</span></span>
-   <span data-ttu-id="94d88-120">Voorraadjournalen met een positieve hoeveelheid, zoals mutaties, winst en verlies, telling, stuklijsten en overboekingen</span><span class="sxs-lookup"><span data-stu-id="94d88-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="94d88-121">Transacties waardoor de hoeveelheid toeneemt</span><span class="sxs-lookup"><span data-stu-id="94d88-121">Transactions that increase quantity</span></span>
<span data-ttu-id="94d88-122">Transacties waardoor de hoeveelheid toeneemt, worden geboekt tegen het lopend gemiddelde van de kostprijs.</span><span class="sxs-lookup"><span data-stu-id="94d88-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="94d88-123">In Finance and Operations wordt een lopend gemiddelde kostprijs berekend, die is gebaseerd op de kosten van elk van deze transacties voor elke voorraaddimensie die financieel wordt bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="94d88-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="94d88-124">Voor informatie over het uitvoeren van gemiddelde kostprijzen raadpleegt u [Lopende gemiddelde kostprijs](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="94d88-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="94d88-125">Transacties waardoor de hoeveelheid afneemt</span><span class="sxs-lookup"><span data-stu-id="94d88-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="94d88-126">In Finance and Operations wordt het berekende lopend gemiddelde van de kostprijs gebruikt wanneer een transactie wordt geboekt waardoor de hoeveelheid afneemt, ongeacht welk voorraadwaarderingsmodel aan de voorraad is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="94d88-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="94d88-127">De transactie, waardoor de hoeveelheid afneemt, mag vóór de boeking niet worden gekoppeld aan een andere transactie.</span><span class="sxs-lookup"><span data-stu-id="94d88-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="94d88-128">Als de fysieke voorhanden voorraad negatief wordt, worden in Finance and Operations de voorraadkosten gebruikt die zijn gedefinieerd voor het artikel op de pagina **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="94d88-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="94d88-129">**Opmerking:** Als de functionaliteit voor meerdere sites is ingeschakeld, zijn deze kosten daarentegen de voorraadkosten die voor een locatie zijn gedefinieerd op de pagina **Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="94d88-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="94d88-130">Fysieke uitgiften en financiële uitgiften</span><span class="sxs-lookup"><span data-stu-id="94d88-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="94d88-131">Wanneer u een fysieke uitgiftetransactie boekt, wordt de status van de transactierecord **Ingehouden**.</span><span class="sxs-lookup"><span data-stu-id="94d88-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="94d88-132">De volgende transacties worden beschouwd als fysieke uitgiften:</span><span class="sxs-lookup"><span data-stu-id="94d88-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="94d88-133">Productieorderverzamellijstjournaal</span><span class="sxs-lookup"><span data-stu-id="94d88-133">Production order picking list journal</span></span>
-   <span data-ttu-id="94d88-134">Pakbon voor verkooporder</span><span class="sxs-lookup"><span data-stu-id="94d88-134">Sales order packing slip</span></span>
-   <span data-ttu-id="94d88-135">Retour van pakbon voor inkooporder</span><span class="sxs-lookup"><span data-stu-id="94d88-135">Purchase order packing slip return</span></span>

<span data-ttu-id="94d88-136">Wanneer u een financiële transactie boekt, wordt de status van de transactierecord **Verkocht**.</span><span class="sxs-lookup"><span data-stu-id="94d88-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="94d88-137">De volgende transacties worden beschouwd als financiële uitgiften:</span><span class="sxs-lookup"><span data-stu-id="94d88-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="94d88-138">Een productieorder beëindigen</span><span class="sxs-lookup"><span data-stu-id="94d88-138">Ending a production order</span></span>
-   <span data-ttu-id="94d88-139">Verkooporderfactuur</span><span class="sxs-lookup"><span data-stu-id="94d88-139">Sales order invoice</span></span>
-   <span data-ttu-id="94d88-140">Leveranciersfactuur retourneren</span><span class="sxs-lookup"><span data-stu-id="94d88-140">Vendor invoice return</span></span>
-   <span data-ttu-id="94d88-141">Voorraadjournalen met een negatieve hoeveelheid, zoals mutaties, winst en verlies, telling, stuklijsten en overboekingen</span><span class="sxs-lookup"><span data-stu-id="94d88-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="94d88-142">Transacties waardoor de hoeveelheid afneemt, worden geboekt tegen het lopend gemiddelde van de kostprijs.</span><span class="sxs-lookup"><span data-stu-id="94d88-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="94d88-143">Daarom is de procedure voor het afsluiten van voorraden vereist voor het vereffenen van uitgiftetransacties naar ontvangsttransacties op basis van het voorraadwaarderingsmodel dat aan elk artikel is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="94d88-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>



