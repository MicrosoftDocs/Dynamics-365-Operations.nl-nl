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
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 60f39b19a627e9c3288f30872d237b8c0ccd8ac4
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="inventory-object-values"></a><span data-ttu-id="95f59-103">Waarden van voorraadobjecten</span><span class="sxs-lookup"><span data-stu-id="95f59-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95f59-104">Dit artikel biedt informatie over hoe de waarden van een voorraadobject worden berekend.</span><span class="sxs-lookup"><span data-stu-id="95f59-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="95f59-105">Met een nieuwe functionaliteit die **fysieke hoeveelheid** wordt genoemd, kunt u de waarden van een specifiek voorraadobject zien.</span><span class="sxs-lookup"><span data-stu-id="95f59-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="95f59-106">Een kostobject geeft het entiteitsniveau weer waarin de voorraadboekhouding wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="95f59-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="95f59-107">Voor meer informatie over kostenobjecten, zie [Kostenobjecten](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="95f59-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="95f59-108">Om de waarden van een specifiek voorraadobject te bekijken, klikt u op **Fysieke hoeveelheid** op de pagina **Kostenobject**.</span><span class="sxs-lookup"><span data-stu-id="95f59-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="95f59-109">De waarde van een voorraadobject wordt als volgt berekend:</span><span class="sxs-lookup"><span data-stu-id="95f59-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="95f59-110">Voorraaobject.Waarde = Kostenobject.Gemiddelde kosten per eenheid × voorraadobject.Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="95f59-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="95f59-111">Het volgende voorbeeld laat ziet hoe de waarden van een voorraadobject en een kostenobject worden berekend.</span><span class="sxs-lookup"><span data-stu-id="95f59-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="95f59-112">Twee productontvangstbongebeurtenissen worden geregistreerd op artikel A:</span><span class="sxs-lookup"><span data-stu-id="95f59-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="95f59-113">Productontvangstbon 1: Hoeveelheid = 100 stuks, Bedrag = $ 1.000,00, Locatie = 1, Magazijn =11, Batchnr.</span><span class="sxs-lookup"><span data-stu-id="95f59-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="95f59-114">= B1</span><span class="sxs-lookup"><span data-stu-id="95f59-114">= B1</span></span>
-   <span data-ttu-id="95f59-115">Productontvangstbon 2: Hoeveelheid = 50 stuks, Bedrag = $ 800,00, Locatie = 1, Magazijn =11, Batchnr.</span><span class="sxs-lookup"><span data-stu-id="95f59-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="95f59-116">= B2</span><span class="sxs-lookup"><span data-stu-id="95f59-116">= B2</span></span>

<span data-ttu-id="95f59-117">De volgende tabel geeft het resultaat van de berekening voor een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="95f59-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="95f59-118">U kunt het resultaat op de pagina **Kostenobject** weergeven.</span><span class="sxs-lookup"><span data-stu-id="95f59-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="95f59-119">Objecttype</span><span class="sxs-lookup"><span data-stu-id="95f59-119">Object type</span></span></th>
<th><span data-ttu-id="95f59-120">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="95f59-120">Item number</span></span></th>
<th><span data-ttu-id="95f59-121">Locatie</span><span class="sxs-lookup"><span data-stu-id="95f59-121">Site</span></span></th>
<th><span data-ttu-id="95f59-122">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="95f59-122">Quantity</span></span></th>
<th><span data-ttu-id="95f59-123">Voorraadeenheid</span><span class="sxs-lookup"><span data-stu-id="95f59-123">Inventory unit</span></span></th>
<th><span data-ttu-id="95f59-124">Waarde</span><span class="sxs-lookup"><span data-stu-id="95f59-124">Value</span></span></th>
<th><span data-ttu-id="95f59-125">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="95f59-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95f59-126">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="95f59-126">Cost object</span></span></td>
<td><span data-ttu-id="95f59-127">A</span><span class="sxs-lookup"><span data-stu-id="95f59-127">A</span></span></td>
<td><span data-ttu-id="95f59-128">1</span><span class="sxs-lookup"><span data-stu-id="95f59-128">1</span></span></td>
<td><span data-ttu-id="95f59-129">150</span><span class="sxs-lookup"><span data-stu-id="95f59-129">150</span></span></td>
<td><span data-ttu-id="95f59-130">Stuks</span><span class="sxs-lookup"><span data-stu-id="95f59-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="95f59-131">$°1800,00</span><span class="sxs-lookup"><span data-stu-id="95f59-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="95f59-132">$°12,00</span><span class="sxs-lookup"><span data-stu-id="95f59-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="95f59-133">De volgende tabel geeft het resultaat van de berekening voor een voorraadobject.</span><span class="sxs-lookup"><span data-stu-id="95f59-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="95f59-134">U kunt het resultaat bekijken door te klikken op **Fysieke hoeveelheid** op de pagina **Kostenobject**.</span><span class="sxs-lookup"><span data-stu-id="95f59-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="95f59-135">Objecttype</span><span class="sxs-lookup"><span data-stu-id="95f59-135">Object type</span></span></th>
<th><span data-ttu-id="95f59-136">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="95f59-136">Item number</span></span></th>
<th><span data-ttu-id="95f59-137">Locatie</span><span class="sxs-lookup"><span data-stu-id="95f59-137">Site</span></span></th>
<th><span data-ttu-id="95f59-138">Magazijn</span><span class="sxs-lookup"><span data-stu-id="95f59-138">Warehouse</span></span></th>
<th><span data-ttu-id="95f59-139">Batchnr.</span><span class="sxs-lookup"><span data-stu-id="95f59-139">Batch No.</span></span></th>
<th><span data-ttu-id="95f59-140">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="95f59-140">Quantity</span></span></th>
<th><span data-ttu-id="95f59-141">Voorraadeenheid</span><span class="sxs-lookup"><span data-stu-id="95f59-141">Inventory unit</span></span></th>
<th><span data-ttu-id="95f59-142">Waarde</span><span class="sxs-lookup"><span data-stu-id="95f59-142">Value</span></span></th>
<th><span data-ttu-id="95f59-143">Gemiddelde eenheidskosten</span><span class="sxs-lookup"><span data-stu-id="95f59-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95f59-144">Voorraadobject</span><span class="sxs-lookup"><span data-stu-id="95f59-144">Inventory object</span></span></td>
<td><span data-ttu-id="95f59-145">A</span><span class="sxs-lookup"><span data-stu-id="95f59-145">A</span></span></td>
<td><span data-ttu-id="95f59-146">1</span><span class="sxs-lookup"><span data-stu-id="95f59-146">1</span></span></td>
<td><span data-ttu-id="95f59-147">11</span><span class="sxs-lookup"><span data-stu-id="95f59-147">11</span></span></td>
<td><span data-ttu-id="95f59-148">B1</span><span class="sxs-lookup"><span data-stu-id="95f59-148">B1</span></span></td>
<td><span data-ttu-id="95f59-149">100</span><span class="sxs-lookup"><span data-stu-id="95f59-149">100</span></span></td>
<td><span data-ttu-id="95f59-150">Stuks</span><span class="sxs-lookup"><span data-stu-id="95f59-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="95f59-151">$ 1200,00</span><span class="sxs-lookup"><span data-stu-id="95f59-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="95f59-152">$°12,00</span><span class="sxs-lookup"><span data-stu-id="95f59-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f59-153">Voorraadobject</span><span class="sxs-lookup"><span data-stu-id="95f59-153">Inventory object</span></span></td>
<td><span data-ttu-id="95f59-154">V</span><span class="sxs-lookup"><span data-stu-id="95f59-154">A</span></span></td>
<td><span data-ttu-id="95f59-155">1</span><span class="sxs-lookup"><span data-stu-id="95f59-155">1</span></span></td>
<td><span data-ttu-id="95f59-156">11</span><span class="sxs-lookup"><span data-stu-id="95f59-156">11</span></span></td>
<td><span data-ttu-id="95f59-157">B2</span><span class="sxs-lookup"><span data-stu-id="95f59-157">B2</span></span></td>
<td><span data-ttu-id="95f59-158">50</span><span class="sxs-lookup"><span data-stu-id="95f59-158">50</span></span></td>
<td><span data-ttu-id="95f59-159">Stuks</span><span class="sxs-lookup"><span data-stu-id="95f59-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="95f59-160">$ 600,00</span><span class="sxs-lookup"><span data-stu-id="95f59-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="95f59-161">$°12,00</span><span class="sxs-lookup"><span data-stu-id="95f59-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="95f59-162">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="95f59-162">Additional resources</span></span>
--------

[<span data-ttu-id="95f59-163">Kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="95f59-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="95f59-164">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="95f59-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="95f59-165">Wat is nieuw of gewijzigd</span><span class="sxs-lookup"><span data-stu-id="95f59-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)




