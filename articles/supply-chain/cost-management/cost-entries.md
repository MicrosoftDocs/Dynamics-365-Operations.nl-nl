---
title: Kosteninvoer
description: Dit artikel biedt informatie over kosteninvoer en wanneer deze wordt gemaakt. Kosteninvoer is een record waarin de hoeveelheid en kosten van een bepaalde gebeurtenis worden geregistreerd.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3116f9fd2d1fe6a0967b114a069f495cea6217a1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425110"
---
# <a name="cost-entries"></a><span data-ttu-id="46804-104">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="46804-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46804-105">Dit artikel biedt informatie over kosteninvoer en wanneer deze wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="46804-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="46804-106">Kosteninvoer is een record waarin de hoeveelheid en kosten van een bepaalde gebeurtenis worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="46804-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="46804-107">Kosteninvoer zijn aggregaties van voorraadtransacties die op actieve financiële voorraaddimensies worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="46804-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="46804-108">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="46804-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="46804-109">Voorbeeld 1: Er wordt geen kosteninvoer gemaakt</span><span class="sxs-lookup"><span data-stu-id="46804-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="46804-110">Een overboekingsjournaalgebeurtenis wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="46804-110">A transfer journal event is registered.</span></span> <span data-ttu-id="46804-111">De gebeurtenis boekt een onderdeel van artikel A van locatie A naar locatie B over. De Locatievoorraaddimensie wordt niet als een onderdeel van het kostenobject beschouwd.</span><span class="sxs-lookup"><span data-stu-id="46804-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="46804-112">Daarom maakt de gebeurtenis twee voorraadtransacties en geen kosteninvoer.</span><span class="sxs-lookup"><span data-stu-id="46804-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="46804-113">Voorbeeld 2: Er wordt kosteninvoer gemaakt</span><span class="sxs-lookup"><span data-stu-id="46804-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="46804-114">Een overboekingsjournaalgebeurtenis wordt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="46804-114">A transfer journal event is registered.</span></span> <span data-ttu-id="46804-115">Met de gebeurtenis wordt een onderdeel van artikel A van locatie 1 naar locatie 2 overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="46804-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="46804-116">De locatievoorraaddimensie wordt als een onderdeel van het kostenobject beschouwd.</span><span class="sxs-lookup"><span data-stu-id="46804-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="46804-117">Daarom maakt de gebeurtenis twee voorraadtransacties en twee kostengegevens.</span><span class="sxs-lookup"><span data-stu-id="46804-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="46804-118">Voorbeeld 3: Er wordt één kosteninvoer gemaakt</span><span class="sxs-lookup"><span data-stu-id="46804-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="46804-119">Een productontvangstbongebeurtenis wordt geregistreerd voor een inkooporder.</span><span class="sxs-lookup"><span data-stu-id="46804-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="46804-120">De gebeurtenis registreert 100 stuks van artikel A tegen eenheidskosten van 10,00 Amerikaanse dollar (USD).</span><span class="sxs-lookup"><span data-stu-id="46804-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="46804-121">Omdat artikel A een serienummer gebruikt om het doel van voorraadbeheer te volgen, wordt een uniek serienummer gemaakt voor elk artikel dat wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="46804-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="46804-122">Daarom maakt de gebeurtenis 100 voorraadtransacties en één kosteninvoer.</span><span class="sxs-lookup"><span data-stu-id="46804-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="46804-123">Pagina Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="46804-123">Cost entries page</span></span>
<span data-ttu-id="46804-124">Op de nieuwe pagina **Kosteninvoer** kunt u registraties van hoeveelheden en kosten weergeven en beheren.</span><span class="sxs-lookup"><span data-stu-id="46804-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="46804-125">Deze pagina vult de pagina **Voorraadtransactie** en **Vereffening voorraad** aan.</span><span class="sxs-lookup"><span data-stu-id="46804-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="46804-126">De records worden in chronologische volgorde geregistreerd voor een gebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="46804-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="46804-127">Daarom kunt u de samengevoegde kosten van een specifieke gebeurtenis of alle gebeurtenissen snel zoeken en controleren die aan een document zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="46804-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="46804-128">Dit is een voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="46804-128">Here is an example:</span></span>

-   <span data-ttu-id="46804-129">Een productontvangstbongebeurtenis is geregistreerd voor artikel A. Honderd stuks worden ontvangen tegen eenheidskosten van 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="46804-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="46804-130">Een aantal dagen na factuur wordt de gebeurtenis geregistreerd, de kosten worden verhoogd naar 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="46804-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="46804-131">Daarom is het totaalbedrag 1100 USD.</span><span class="sxs-lookup"><span data-stu-id="46804-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="46804-132">Een tweede boekstuk is gemaakt om het verschil van 100 USD te verantwoorden.</span><span class="sxs-lookup"><span data-stu-id="46804-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="46804-133">Een aantal dagen later wordt een diverse toeslagen van 15,00 USD geregistreerd om de transportkosten op de inkooporder te dekken.</span><span class="sxs-lookup"><span data-stu-id="46804-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="46804-134">Boekstuk</span><span class="sxs-lookup"><span data-stu-id="46804-134">Voucher</span></span> | <span data-ttu-id="46804-135">Datum</span><span class="sxs-lookup"><span data-stu-id="46804-135">Date</span></span>       | <span data-ttu-id="46804-136">Verwijzing</span><span class="sxs-lookup"><span data-stu-id="46804-136">Reference</span></span>      | <span data-ttu-id="46804-137">Nummer</span><span class="sxs-lookup"><span data-stu-id="46804-137">Number</span></span> | <span data-ttu-id="46804-138">Partij-ID</span><span class="sxs-lookup"><span data-stu-id="46804-138">Lot ID</span></span>  | <span data-ttu-id="46804-139">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="46804-139">Quantity</span></span> | <span data-ttu-id="46804-140">Bedrag</span><span class="sxs-lookup"><span data-stu-id="46804-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="46804-141">00001</span><span class="sxs-lookup"><span data-stu-id="46804-141">00001</span></span>   | <span data-ttu-id="46804-142">01-01-2015</span><span class="sxs-lookup"><span data-stu-id="46804-142">01-01-2015</span></span> | <span data-ttu-id="46804-143">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="46804-143">Purchase order</span></span> | <span data-ttu-id="46804-144">100001</span><span class="sxs-lookup"><span data-stu-id="46804-144">100001</span></span> | <span data-ttu-id="46804-145">0000101</span><span class="sxs-lookup"><span data-stu-id="46804-145">0000101</span></span> | <span data-ttu-id="46804-146">100,00</span><span class="sxs-lookup"><span data-stu-id="46804-146">100.00</span></span>   | <span data-ttu-id="46804-147">1000.00</span><span class="sxs-lookup"><span data-stu-id="46804-147">1000.00</span></span> |
| <span data-ttu-id="46804-148">00002</span><span class="sxs-lookup"><span data-stu-id="46804-148">00002</span></span>   | <span data-ttu-id="46804-149">20-01-2015</span><span class="sxs-lookup"><span data-stu-id="46804-149">20-01-2015</span></span> | <span data-ttu-id="46804-150">Inkooporder</span><span class="sxs-lookup"><span data-stu-id="46804-150">Purchase order</span></span> | <span data-ttu-id="46804-151">100001</span><span class="sxs-lookup"><span data-stu-id="46804-151">100001</span></span> | <span data-ttu-id="46804-152">0000101</span><span class="sxs-lookup"><span data-stu-id="46804-152">0000101</span></span> |          | <span data-ttu-id="46804-153">100,00</span><span class="sxs-lookup"><span data-stu-id="46804-153">100.00</span></span>  |
| <span data-ttu-id="46804-154">00003</span><span class="sxs-lookup"><span data-stu-id="46804-154">00003</span></span>   | <span data-ttu-id="46804-155">31-01-2015</span><span class="sxs-lookup"><span data-stu-id="46804-155">31-01-2015</span></span> | <span data-ttu-id="46804-156">Correctie</span><span class="sxs-lookup"><span data-stu-id="46804-156">Adjustment</span></span>     | <span data-ttu-id="46804-157">100001</span><span class="sxs-lookup"><span data-stu-id="46804-157">100001</span></span> | <span data-ttu-id="46804-158">0000101</span><span class="sxs-lookup"><span data-stu-id="46804-158">0000101</span></span> |          | <span data-ttu-id="46804-159">15,00</span><span class="sxs-lookup"><span data-stu-id="46804-159">15.00</span></span>   |

<span data-ttu-id="46804-160">Op de pagina **Kosteninvoer** kunt u filteren op document-ID en documentdatum.</span><span class="sxs-lookup"><span data-stu-id="46804-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="46804-161">Kosteninvoer is alleen beschikbaar voor [kostenobjecten](cost-object.md) of vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="46804-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="46804-162">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="46804-162">Additional resources</span></span>
--------

[<span data-ttu-id="46804-163">Kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="46804-163">Cost objects</span></span>](cost-object.md)



