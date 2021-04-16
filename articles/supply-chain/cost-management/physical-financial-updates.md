---
title: Fysieke en financiële updates
description: Dit onderwerp biedt een overzicht van de typen transacties die voorraadhoeveelheden vergroten of verkleinen.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88432b9a5e564f9e81892e0bb379f95ff40d6c9d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842148"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="e8e5a-103">Fysieke en financiële updates</span><span class="sxs-lookup"><span data-stu-id="e8e5a-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8e5a-104">Dit onderwerp biedt een overzicht van de typen transacties die voorraadhoeveelheden vergroten of verkleinen.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="e8e5a-105">Voorraadtransacties kunnen in Dynamics 365 Supply Chain Management fysiek en financieel worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e8e5a-106">Bepaalde typen van fysieke en financiële transacties verhogen voorraadhoeveelheden, terwijl andere de hoeveelheid verlagen.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="e8e5a-107">Fysieke toename</span><span class="sxs-lookup"><span data-stu-id="e8e5a-107">Physical increases</span></span>
<span data-ttu-id="e8e5a-108">Wanneer u een fysieke transactie boekt, wordt de status van de transactierecord **Ontvangen**.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="e8e5a-109">De volgende transacties worden beschouwd als een fysieke toename:</span><span class="sxs-lookup"><span data-stu-id="e8e5a-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="e8e5a-110">Ontvangst van inkooporder</span><span class="sxs-lookup"><span data-stu-id="e8e5a-110">Purchase order receipt</span></span>
-   <span data-ttu-id="e8e5a-111">Retour van pakbon voor verkooporder</span><span class="sxs-lookup"><span data-stu-id="e8e5a-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="e8e5a-112">Een productieorder gereedmelden</span><span class="sxs-lookup"><span data-stu-id="e8e5a-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="e8e5a-113">Bijproduct in een productieorderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="e8e5a-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="e8e5a-114">Financiële toename</span><span class="sxs-lookup"><span data-stu-id="e8e5a-114">Financial increases</span></span>
<span data-ttu-id="e8e5a-115">Wanneer u een financiële transactie boekt, wordt de status van de transactierecord die de hoeveelheid vergroot **Ingekocht**.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="e8e5a-116">De volgende transacties worden beschouwd als een financiële toename:</span><span class="sxs-lookup"><span data-stu-id="e8e5a-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="e8e5a-117">Leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="e8e5a-117">Vendor invoice</span></span>
-   <span data-ttu-id="e8e5a-118">Verkooporderfactuur voor een retour</span><span class="sxs-lookup"><span data-stu-id="e8e5a-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="e8e5a-119">Kostprijsberekening voor productieorder</span><span class="sxs-lookup"><span data-stu-id="e8e5a-119">Production order costing</span></span>
-   <span data-ttu-id="e8e5a-120">Voorraadjournalen met een positieve hoeveelheid, zoals mutaties, winst en verlies, telling, stuklijsten en overboekingen</span><span class="sxs-lookup"><span data-stu-id="e8e5a-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="e8e5a-121">Transacties waardoor de hoeveelheid toeneemt</span><span class="sxs-lookup"><span data-stu-id="e8e5a-121">Transactions that increase quantity</span></span>
<span data-ttu-id="e8e5a-122">Transacties waardoor de hoeveelheid toeneemt, worden geboekt tegen het lopend gemiddelde van de kostprijs.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="e8e5a-123">De berekende lopende gemiddelde kostprijs is gebaseerd op de kosten van elk van deze transacties voor elke voorraaddimensie die financieel wordt bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="e8e5a-124">Voor informatie over het uitvoeren van gemiddelde kostprijzen raadpleegt u [Lopende gemiddelde kostprijs](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="e8e5a-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="e8e5a-125">Transacties waardoor de hoeveelheid afneemt</span><span class="sxs-lookup"><span data-stu-id="e8e5a-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="e8e5a-126">Het berekende lopend gemiddelde van de kostprijs wordt gebruikt wanneer een transactie wordt geboekt waardoor de hoeveelheid afneemt, ongeacht welk voorraadwaarderingsmodel aan de voorraad is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="e8e5a-127">De transactie, waardoor de hoeveelheid afneemt, mag vóór de boeking niet worden gekoppeld aan een andere transactie.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="e8e5a-128">Als de fysieke voorhanden voorraad negatief wordt, worden de voorraadkosten gebruikt die zijn gedefinieerd voor het artikel op de pagina **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="e8e5a-129">Als de functionaliteit voor meerdere sites is ingeschakeld, zijn deze kosten daarentegen de voorraadkosten die voor een locatie zijn gedefinieerd op de pagina **Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="e8e5a-130">Fysieke uitgiften en financiële uitgiften</span><span class="sxs-lookup"><span data-stu-id="e8e5a-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="e8e5a-131">Wanneer u een fysieke uitgiftetransactie boekt, wordt de status van de transactierecord **Ingehouden**.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="e8e5a-132">De volgende transacties worden beschouwd als fysieke uitgiften:</span><span class="sxs-lookup"><span data-stu-id="e8e5a-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="e8e5a-133">Productieorderverzamellijstjournaal</span><span class="sxs-lookup"><span data-stu-id="e8e5a-133">Production order picking list journal</span></span>
-   <span data-ttu-id="e8e5a-134">Pakbon voor verkooporder</span><span class="sxs-lookup"><span data-stu-id="e8e5a-134">Sales order packing slip</span></span>
-   <span data-ttu-id="e8e5a-135">Retour van pakbon voor inkooporder</span><span class="sxs-lookup"><span data-stu-id="e8e5a-135">Purchase order packing slip return</span></span>

<span data-ttu-id="e8e5a-136">Wanneer u een financiële transactie boekt, wordt de status van de transactierecord **Verkocht**.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="e8e5a-137">De volgende transacties worden beschouwd als financiële uitgiften:</span><span class="sxs-lookup"><span data-stu-id="e8e5a-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="e8e5a-138">Een productieorder beëindigen</span><span class="sxs-lookup"><span data-stu-id="e8e5a-138">Ending a production order</span></span>
-   <span data-ttu-id="e8e5a-139">Verkooporderfactuur</span><span class="sxs-lookup"><span data-stu-id="e8e5a-139">Sales order invoice</span></span>
-   <span data-ttu-id="e8e5a-140">Leveranciersfactuur retourneren</span><span class="sxs-lookup"><span data-stu-id="e8e5a-140">Vendor invoice return</span></span>
-   <span data-ttu-id="e8e5a-141">Voorraadjournalen met een negatieve hoeveelheid, zoals mutaties, winst en verlies, telling, stuklijsten en overboekingen</span><span class="sxs-lookup"><span data-stu-id="e8e5a-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="e8e5a-142">Transacties waardoor de hoeveelheid afneemt, worden geboekt tegen het lopend gemiddelde van de kostprijs.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="e8e5a-143">Daarom is de procedure voor het afsluiten van voorraden vereist voor het vereffenen van uitgiftetransacties naar ontvangsttransacties op basis van het voorraadwaarderingsmodel dat aan elk artikel is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e8e5a-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]