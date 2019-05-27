---
title: Factorafschrijving
description: Dit artikel geeft een overzicht van de factorafschrijvingsmethode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa8bc4566def9dd770a97facb459e6b977bfaffb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546750"
---
# <a name="factor-depreciation"></a><span data-ttu-id="54a43-103">Factorafschrijving</span><span class="sxs-lookup"><span data-stu-id="54a43-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54a43-104">Dit artikel geeft een overzicht van de factorafschrijvingsmethode.</span><span class="sxs-lookup"><span data-stu-id="54a43-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="54a43-105">Factoren zijn de percentages die worden gebruikt om activa af te schrijven.</span><span class="sxs-lookup"><span data-stu-id="54a43-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="54a43-106">Wanneer u een profiel voor de afschrijving van vaste activa instelt en de waarde **Factor** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, kunt u progressieve, degressieve of lineaire afschrijving instellen:</span><span class="sxs-lookup"><span data-stu-id="54a43-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="54a43-107">Bij progressieve afschrijving neemt het afschrijvingsbedrag bij elke afschrijvingsperiode toe.</span><span class="sxs-lookup"><span data-stu-id="54a43-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="54a43-108">Bij degressieve afschrijving neemt het afschrijvingsbedrag per periode af.</span><span class="sxs-lookup"><span data-stu-id="54a43-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="54a43-109">Bij lineaire afschrijving is de afschrijving in elke periode hetzelfde.</span><span class="sxs-lookup"><span data-stu-id="54a43-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="54a43-110">De onderstaande regels en voorbeelden geven aan hoe u factoren voor elk type afschrijving in kunt stellen.</span><span class="sxs-lookup"><span data-stu-id="54a43-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="54a43-111">Wanneer u **Factor** selecteert in het veld **Methode**, worden de velden **Factor** en **Interval** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="54a43-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="54a43-112">Progressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="54a43-112">Progressive depreciation</span></span>
<span data-ttu-id="54a43-113">De waarde in het veld **Factor** is groter dan **50**.</span><span class="sxs-lookup"><span data-stu-id="54a43-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="54a43-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="54a43-114">Example</span></span>

<span data-ttu-id="54a43-115">De aanschafprijs is 100.000, de factor is 70, de levensduur van de service is 10 jaar en de afschrijving begint op 1 januari.</span><span class="sxs-lookup"><span data-stu-id="54a43-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="54a43-116">De afschrijvingsbedragen en netboekwaarden worden alleen voor de eerste zes jaar van de levensduur van de service weergegeven.</span><span class="sxs-lookup"><span data-stu-id="54a43-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="54a43-117">Jaar</span><span class="sxs-lookup"><span data-stu-id="54a43-117">Year</span></span> | <span data-ttu-id="54a43-118">Periode</span><span class="sxs-lookup"><span data-stu-id="54a43-118">Period</span></span>      | <span data-ttu-id="54a43-119">Afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="54a43-119">Depreciation amount</span></span> | <span data-ttu-id="54a43-120">Bedrag nettoboekwaarde</span><span class="sxs-lookup"><span data-stu-id="54a43-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="54a43-121">1</span><span class="sxs-lookup"><span data-stu-id="54a43-121">1</span></span>    | <span data-ttu-id="54a43-122">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-122">December 31</span></span> | <span data-ttu-id="54a43-123">307,69</span><span class="sxs-lookup"><span data-stu-id="54a43-123">307.69</span></span>              | <span data-ttu-id="54a43-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="54a43-124">99,692.31</span></span>             |
| <span data-ttu-id="54a43-125">2</span><span class="sxs-lookup"><span data-stu-id="54a43-125">2</span></span>    | <span data-ttu-id="54a43-126">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-126">December 31</span></span> | <span data-ttu-id="54a43-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="54a43-127">1,447.21</span></span>            | <span data-ttu-id="54a43-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="54a43-128">98,245.10</span></span>             |
| <span data-ttu-id="54a43-129">3</span><span class="sxs-lookup"><span data-stu-id="54a43-129">3</span></span>    | <span data-ttu-id="54a43-130">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-130">December 31</span></span> | <span data-ttu-id="54a43-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="54a43-131">3,104.50</span></span>            | <span data-ttu-id="54a43-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="54a43-132">95,140.60</span></span>             |
| <span data-ttu-id="54a43-133">4</span><span class="sxs-lookup"><span data-stu-id="54a43-133">4</span></span>    | <span data-ttu-id="54a43-134">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-134">December 31</span></span> | <span data-ttu-id="54a43-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="54a43-135">5,150.21</span></span>            | <span data-ttu-id="54a43-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="54a43-136">89,990.39</span></span>             |
| <span data-ttu-id="54a43-137">5</span><span class="sxs-lookup"><span data-stu-id="54a43-137">5</span></span>    | <span data-ttu-id="54a43-138">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-138">December 31</span></span> | <span data-ttu-id="54a43-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="54a43-139">7,522.95</span></span>            | <span data-ttu-id="54a43-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="54a43-140">82,467.44</span></span>             |
| <span data-ttu-id="54a43-141">6</span><span class="sxs-lookup"><span data-stu-id="54a43-141">6</span></span>    | <span data-ttu-id="54a43-142">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-142">December 31</span></span> | <span data-ttu-id="54a43-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="54a43-143">10,184.06</span></span>           | <span data-ttu-id="54a43-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="54a43-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="54a43-145">Degressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="54a43-145">Digressive depreciation</span></span>
<span data-ttu-id="54a43-146">De waarde in het veld **Factor** is kleiner dan **50**.</span><span class="sxs-lookup"><span data-stu-id="54a43-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="54a43-147">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="54a43-147">Example</span></span>

<span data-ttu-id="54a43-148">De aanschafprijs is 100.000, de factor is 20, de levensduur van de service is 10 jaar en de afschrijving begint op 1 januari.</span><span class="sxs-lookup"><span data-stu-id="54a43-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="54a43-149">De afschrijvingsbedragen en netboekwaarden worden alleen voor de eerste zes jaar van de levensduur van de service weergegeven.</span><span class="sxs-lookup"><span data-stu-id="54a43-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="54a43-150">Jaar</span><span class="sxs-lookup"><span data-stu-id="54a43-150">Year</span></span> | <span data-ttu-id="54a43-151">Periode</span><span class="sxs-lookup"><span data-stu-id="54a43-151">Period</span></span>      | <span data-ttu-id="54a43-152">Afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="54a43-152">Depreciation amount</span></span> | <span data-ttu-id="54a43-153">Bedrag nettoboekwaarde</span><span class="sxs-lookup"><span data-stu-id="54a43-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="54a43-154">1</span><span class="sxs-lookup"><span data-stu-id="54a43-154">1</span></span>    | <span data-ttu-id="54a43-155">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-155">December 31</span></span> | <span data-ttu-id="54a43-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="54a43-156">56,080.43</span></span>           | <span data-ttu-id="54a43-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="54a43-157">43,919.57</span></span>             |
| <span data-ttu-id="54a43-158">2</span><span class="sxs-lookup"><span data-stu-id="54a43-158">2</span></span>    | <span data-ttu-id="54a43-159">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-159">December 31</span></span> | <span data-ttu-id="54a43-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="54a43-160">10,665.70</span></span>           | <span data-ttu-id="54a43-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="54a43-161">33,253.87</span></span>             |
| <span data-ttu-id="54a43-162">3</span><span class="sxs-lookup"><span data-stu-id="54a43-162">3</span></span>    | <span data-ttu-id="54a43-163">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-163">December 31</span></span> | <span data-ttu-id="54a43-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="54a43-164">7,156.22</span></span>            | <span data-ttu-id="54a43-165">26.097,65</span><span class="sxs-lookup"><span data-stu-id="54a43-165">26,097.65</span></span>             |
| <span data-ttu-id="54a43-166">4</span><span class="sxs-lookup"><span data-stu-id="54a43-166">4</span></span>    | <span data-ttu-id="54a43-167">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-167">December 31</span></span> | <span data-ttu-id="54a43-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="54a43-168">5,538.06</span></span>            | <span data-ttu-id="54a43-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="54a43-169">20,559.59</span></span>             |
| <span data-ttu-id="54a43-170">5</span><span class="sxs-lookup"><span data-stu-id="54a43-170">5</span></span>    | <span data-ttu-id="54a43-171">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-171">December 31</span></span> | <span data-ttu-id="54a43-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="54a43-172">4,579.89</span></span>            | <span data-ttu-id="54a43-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="54a43-173">15,979.70</span></span>             |
| <span data-ttu-id="54a43-174">6</span><span class="sxs-lookup"><span data-stu-id="54a43-174">6</span></span>    | <span data-ttu-id="54a43-175">31 december</span><span class="sxs-lookup"><span data-stu-id="54a43-175">December 31</span></span> | <span data-ttu-id="54a43-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="54a43-176">3,937.36</span></span>            | <span data-ttu-id="54a43-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="54a43-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="54a43-178">Lineaire afschrijving</span><span class="sxs-lookup"><span data-stu-id="54a43-178">Straight line depreciation</span></span>
<span data-ttu-id="54a43-179">De waarde in het veld **Factor** is gelijk aan **50**.</span><span class="sxs-lookup"><span data-stu-id="54a43-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="54a43-180">In dit geval is de afschrijving in elke periode hetzelfde en u moet rekening houden met de implicaties van de waarden die u hebt opgegeven in andere velden, zoals beschreven in [Lineaire afschrijving van levensduur](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="54a43-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



