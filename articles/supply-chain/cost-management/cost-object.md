---
title: Kostenobjecten
description: Dit artikel biedt informatie over kostenobjecten en uitleg over hoe kosten en hoeveelheden worden samengevoegd. Een kostenopject is een entiteit waarvoor kosten en hoeveelheden worden samengevoegd. Een kostenobjectentiteit kan een product of productvarianten, zoals varianten voor stijl en kleur, zijn.
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
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee7c170d5a330c0080931a67c1548eb0d3522bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232393"
---
# <a name="cost-objects"></a><span data-ttu-id="9b163-105">Kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="9b163-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b163-106">Dit artikel biedt informatie over kostenobjecten en uitleg over hoe kosten en hoeveelheden worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="9b163-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="9b163-107">Een kostenopject is een entiteit waarvoor kosten en hoeveelheden worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="9b163-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="9b163-108">Een kostenobjectentiteit kan een product of productvarianten, zoals varianten voor stijl en kleur, zijn.</span><span class="sxs-lookup"><span data-stu-id="9b163-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="9b163-109">Kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="9b163-109">Cost objects</span></span>

<span data-ttu-id="9b163-110">De pagina **Kostenobjecten** bevat alle kostenobjecten die op een product worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="9b163-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="9b163-111">De kostenobjecten worden gedefinieerd door gegevens uit de volgende bronnen:</span><span class="sxs-lookup"><span data-stu-id="9b163-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="9b163-112">Artikel</span><span class="sxs-lookup"><span data-stu-id="9b163-112">Product</span></span>
-   <span data-ttu-id="9b163-113">Productdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="9b163-113">Product dimension group</span></span>
-   <span data-ttu-id="9b163-114">Opslagdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="9b163-114">Storage dimension group</span></span>
-   <span data-ttu-id="9b163-115">Traceringsdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="9b163-115">Tracking dimension group</span></span>

<span data-ttu-id="9b163-116">**Opmerking:** een kostenobject vertegenwoordigt alleen een kostenelement van het type **Direct materiaal**.</span><span class="sxs-lookup"><span data-stu-id="9b163-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="9b163-117">Een kostenobject en een voorraadobject verschillen daarin dat een kostenobject wordt gedefinieerd door de voorraaddimensies die voor financiële voorraad worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="9b163-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="9b163-118">Een artikel heeft bijvoorbeeld de volgende configuratie:</span><span class="sxs-lookup"><span data-stu-id="9b163-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="9b163-119">**Locatie:** Fysieke voorraad = Ja, Financiële voorraad = Ja</span><span class="sxs-lookup"><span data-stu-id="9b163-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="9b163-120">**Magazijn:** Fysieke voorraad = Ja, Financiële voorraad = Nee</span><span class="sxs-lookup"><span data-stu-id="9b163-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="9b163-121">**Batchnr.:** Fysieke voorraad = Ja, Financiële voorraad = Nee</span><span class="sxs-lookup"><span data-stu-id="9b163-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="9b163-122">De volgende tabel toont wat een kostenobject is en wat een voorraadobject is.</span><span class="sxs-lookup"><span data-stu-id="9b163-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="9b163-123">Objecttype</span><span class="sxs-lookup"><span data-stu-id="9b163-123">Object type</span></span>      | <span data-ttu-id="9b163-124">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="9b163-124">Item number</span></span> | <span data-ttu-id="9b163-125">Locatie</span><span class="sxs-lookup"><span data-stu-id="9b163-125">Site</span></span> | <span data-ttu-id="9b163-126">Magazijn</span><span class="sxs-lookup"><span data-stu-id="9b163-126">Warehouse</span></span> | <span data-ttu-id="9b163-127">Batchnr.</span><span class="sxs-lookup"><span data-stu-id="9b163-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="9b163-128">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="9b163-128">Cost object</span></span>      | <span data-ttu-id="9b163-129">x</span><span class="sxs-lookup"><span data-stu-id="9b163-129">x</span></span>           | <span data-ttu-id="9b163-130">x</span><span class="sxs-lookup"><span data-stu-id="9b163-130">x</span></span>    |           |           |
| <span data-ttu-id="9b163-131">Voorraadobject</span><span class="sxs-lookup"><span data-stu-id="9b163-131">Inventory object</span></span> | <span data-ttu-id="9b163-132">x</span><span class="sxs-lookup"><span data-stu-id="9b163-132">x</span></span>           | <span data-ttu-id="9b163-133">x</span><span class="sxs-lookup"><span data-stu-id="9b163-133">x</span></span>    |  <span data-ttu-id="9b163-134">x</span><span class="sxs-lookup"><span data-stu-id="9b163-134">x</span></span>        | <span data-ttu-id="9b163-135">x</span><span class="sxs-lookup"><span data-stu-id="9b163-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="9b163-136">Samenvoeging van kosten en hoeveelheden</span><span class="sxs-lookup"><span data-stu-id="9b163-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="9b163-137">De waarde in het veld **Waarde** is een som van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="9b163-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="9b163-138">Fysieke kostprijs</span><span class="sxs-lookup"><span data-stu-id="9b163-138">Physical cost amount</span></span>
    -   <span data-ttu-id="9b163-139">Financiële kostprijs</span><span class="sxs-lookup"><span data-stu-id="9b163-139">Financial cost amount</span></span>
    -   <span data-ttu-id="9b163-140">Correcties</span><span class="sxs-lookup"><span data-stu-id="9b163-140">Adjustments</span></span>
-   <span data-ttu-id="9b163-141">De waarde in het veld **Hoeveelheid** is een som van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="9b163-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="9b163-142">Ontvangen</span><span class="sxs-lookup"><span data-stu-id="9b163-142">Received</span></span>
    -   <span data-ttu-id="9b163-143">Ingehouden</span><span class="sxs-lookup"><span data-stu-id="9b163-143">Deducted</span></span>
    -   <span data-ttu-id="9b163-144">Boekingshoeveelheid</span><span class="sxs-lookup"><span data-stu-id="9b163-144">Posted quantity</span></span>
-   <span data-ttu-id="9b163-145">Het veld **Gemiddelde eenheidskosten** is een berekend veld.</span><span class="sxs-lookup"><span data-stu-id="9b163-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="9b163-146">De waarde wordt berekend door de waarde **Waarde** te delen door de waarde **Hoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="9b163-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="9b163-147">**Opmerking:** de parameter **Fysieke waarde opnemen** is niet van invloed op de eerdere berekeningen.</span><span class="sxs-lookup"><span data-stu-id="9b163-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9b163-148">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="9b163-148">Additional resources</span></span>
--------

[<span data-ttu-id="9b163-149">Productdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="9b163-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="9b163-150">Opslagdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="9b163-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="9b163-151">Traceringsdimensiegroep</span><span class="sxs-lookup"><span data-stu-id="9b163-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="9b163-152">Wat is nieuw of gewijzigd</span><span class="sxs-lookup"><span data-stu-id="9b163-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="9b163-153">Kosteninvoer</span><span class="sxs-lookup"><span data-stu-id="9b163-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]