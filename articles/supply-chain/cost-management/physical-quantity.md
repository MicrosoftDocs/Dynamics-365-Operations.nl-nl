---
title: Waarden van voorraadobjecten
description: Dit artikel biedt informatie over hoe de waarden van een voorraadobject worden berekend.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 2cdd1377d3c7c922a3e4cba7f44eef24b0c6824c
ms.contentlocale: nl-nl
ms.lasthandoff: 10/13/2017

---

# <a name="inventory-object-values"></a><span data-ttu-id="7ca50-103">Waarden van voorraadobjecten</span><span class="sxs-lookup"><span data-stu-id="7ca50-103">Inventory object values</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7ca50-104">Dit artikel biedt informatie over hoe de waarden van een voorraadobject worden berekend.</span><span class="sxs-lookup"><span data-stu-id="7ca50-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="7ca50-105">Met een nieuwe functionaliteit die **fysieke hoeveelheid** wordt genoemd, kunt u de waarden van een specifiek voorraadobject zien.</span><span class="sxs-lookup"><span data-stu-id="7ca50-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="7ca50-106">Een kostobject geeft het entiteitsniveau weer waarin de voorraadboekhouding wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7ca50-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="7ca50-107">Voor meer informatie over kostenobjecten, zie [Kostenobjecten](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="7ca50-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="7ca50-108">Om de waarden van een specifiek voorraadobject te bekijken, klikt u op **Fysieke hoeveelheid** op de pagina **Kostenobject**.</span><span class="sxs-lookup"><span data-stu-id="7ca50-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="7ca50-109">De waarde van een voorraadobject wordt als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="7ca50-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="7ca50-110">Voorraaobject.Waarde = Kostenobject.Gemiddelde kosten per eenheid × voorraadobject.Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7ca50-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="7ca50-111">Het volgende voorbeeld laat ziet hoe de waarden van een voorraadobject en een kostenobject worden berekend.</span><span class="sxs-lookup"><span data-stu-id="7ca50-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="7ca50-112">Twee productontvangstbongebeurtenissen worden geregistreerd op artikel A:</span><span class="sxs-lookup"><span data-stu-id="7ca50-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="7ca50-113">Productontvangstbon 1: Hoeveelheid = 100 stuks, Bedrag = $ 1.000,00, Locatie = 1, Magazijn =11, Batchnr.</span><span class="sxs-lookup"><span data-stu-id="7ca50-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="7ca50-114">= B1</span><span class="sxs-lookup"><span data-stu-id="7ca50-114">= B1</span></span>
-   <span data-ttu-id="7ca50-115">Productontvangstbon 2: Hoeveelheid = 50 stuks, Bedrag = $ 800,00, Locatie = 1, Magazijn =11, Batchnr.</span><span class="sxs-lookup"><span data-stu-id="7ca50-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="7ca50-116">= B2</span><span class="sxs-lookup"><span data-stu-id="7ca50-116">= B2</span></span>

<span data-ttu-id="7ca50-117">De volgende tabel geeft het resultaat van de berekening voor een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="7ca50-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="7ca50-118">U kunt het resultaat op de pagina **Kostenobject** weergeven.</span><span class="sxs-lookup"><span data-stu-id="7ca50-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ca50-119">Objecttype</span><span class="sxs-lookup"><span data-stu-id="7ca50-119">Object type</span></span></th>
<th><span data-ttu-id="7ca50-120">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="7ca50-120">Item number</span></span></th>
<th><span data-ttu-id="7ca50-121">Locatie</span><span class="sxs-lookup"><span data-stu-id="7ca50-121">Site</span></span></th>
<th><span data-ttu-id="7ca50-122">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7ca50-122">Quantity</span></span></th>
<th><span data-ttu-id="7ca50-123">Voorraadeenheid</span><span class="sxs-lookup"><span data-stu-id="7ca50-123">Inventory unit</span></span></th>
<th><span data-ttu-id="7ca50-124">Waarde</span><span class="sxs-lookup"><span data-stu-id="7ca50-124">Value</span></span></th>
<th><span data-ttu-id="7ca50-125">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="7ca50-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ca50-126">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="7ca50-126">Cost object</span></span></td>
<td><span data-ttu-id="7ca50-127">A</span><span class="sxs-lookup"><span data-stu-id="7ca50-127">A</span></span></td>
<td><span data-ttu-id="7ca50-128">1</span><span class="sxs-lookup"><span data-stu-id="7ca50-128">1</span></span></td>
<td><span data-ttu-id="7ca50-129">150</span><span class="sxs-lookup"><span data-stu-id="7ca50-129">150</span></span></td>
<td><span data-ttu-id="7ca50-130">Stuks</span><span class="sxs-lookup"><span data-stu-id="7ca50-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="7ca50-131">$°1800,00</span><span class="sxs-lookup"><span data-stu-id="7ca50-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="7ca50-132">$°12,00</span><span class="sxs-lookup"><span data-stu-id="7ca50-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7ca50-133">De volgende tabel geeft het resultaat van de berekening voor een voorraadobject.</span><span class="sxs-lookup"><span data-stu-id="7ca50-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="7ca50-134">U kunt het resultaat bekijken door te klikken op **Fysieke hoeveelheid** op de pagina **Kostenobject**.</span><span class="sxs-lookup"><span data-stu-id="7ca50-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ca50-135">Objecttype</span><span class="sxs-lookup"><span data-stu-id="7ca50-135">Object type</span></span></th>
<th><span data-ttu-id="7ca50-136">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="7ca50-136">Item number</span></span></th>
<th><span data-ttu-id="7ca50-137">Locatie</span><span class="sxs-lookup"><span data-stu-id="7ca50-137">Site</span></span></th>
<th><span data-ttu-id="7ca50-138">Magazijn</span><span class="sxs-lookup"><span data-stu-id="7ca50-138">Warehouse</span></span></th>
<th><span data-ttu-id="7ca50-139">Batchnr.</span><span class="sxs-lookup"><span data-stu-id="7ca50-139">Batch No.</span></span></th>
<th><span data-ttu-id="7ca50-140">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="7ca50-140">Quantity</span></span></th>
<th><span data-ttu-id="7ca50-141">Voorraadeenheid</span><span class="sxs-lookup"><span data-stu-id="7ca50-141">Inventory unit</span></span></th>
<th><span data-ttu-id="7ca50-142">Waarde</span><span class="sxs-lookup"><span data-stu-id="7ca50-142">Value</span></span></th>
<th><span data-ttu-id="7ca50-143">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="7ca50-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ca50-144">Voorraadobject</span><span class="sxs-lookup"><span data-stu-id="7ca50-144">Inventory object</span></span></td>
<td><span data-ttu-id="7ca50-145">A</span><span class="sxs-lookup"><span data-stu-id="7ca50-145">A</span></span></td>
<td><span data-ttu-id="7ca50-146">1</span><span class="sxs-lookup"><span data-stu-id="7ca50-146">1</span></span></td>
<td><span data-ttu-id="7ca50-147">11</span><span class="sxs-lookup"><span data-stu-id="7ca50-147">11</span></span></td>
<td><span data-ttu-id="7ca50-148">B1</span><span class="sxs-lookup"><span data-stu-id="7ca50-148">B1</span></span></td>
<td><span data-ttu-id="7ca50-149">100</span><span class="sxs-lookup"><span data-stu-id="7ca50-149">100</span></span></td>
<td><span data-ttu-id="7ca50-150">Stuks</span><span class="sxs-lookup"><span data-stu-id="7ca50-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="7ca50-151">$ 1200,00</span><span class="sxs-lookup"><span data-stu-id="7ca50-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="7ca50-152">$°12,00</span><span class="sxs-lookup"><span data-stu-id="7ca50-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ca50-153">Voorraadobject</span><span class="sxs-lookup"><span data-stu-id="7ca50-153">Inventory object</span></span></td>
<td><span data-ttu-id="7ca50-154">A</span><span class="sxs-lookup"><span data-stu-id="7ca50-154">A</span></span></td>
<td><span data-ttu-id="7ca50-155">1</span><span class="sxs-lookup"><span data-stu-id="7ca50-155">1</span></span></td>
<td><span data-ttu-id="7ca50-156">11</span><span class="sxs-lookup"><span data-stu-id="7ca50-156">11</span></span></td>
<td><span data-ttu-id="7ca50-157">B2</span><span class="sxs-lookup"><span data-stu-id="7ca50-157">B2</span></span></td>
<td><span data-ttu-id="7ca50-158">50</span><span class="sxs-lookup"><span data-stu-id="7ca50-158">50</span></span></td>
<td><span data-ttu-id="7ca50-159">Stuks</span><span class="sxs-lookup"><span data-stu-id="7ca50-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="7ca50-160">$ 600,00</span><span class="sxs-lookup"><span data-stu-id="7ca50-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="7ca50-161">$°12,00</span><span class="sxs-lookup"><span data-stu-id="7ca50-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="7ca50-162">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7ca50-162">See also</span></span>
--------

[<span data-ttu-id="7ca50-163">Kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="7ca50-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="7ca50-164">Kostenboekingen</span><span class="sxs-lookup"><span data-stu-id="7ca50-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="7ca50-165">Wat is nieuw of gewijzigd</span><span class="sxs-lookup"><span data-stu-id="7ca50-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)




