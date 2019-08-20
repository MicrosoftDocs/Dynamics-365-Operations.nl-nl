---
title: Rekeningstructuren maken
description: Deze taakbegeleiding helpt u bij het maken van een rekeningstructuur.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2183f88356fc8094781af147bf079c4e53ffb2b4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846698"
---
# <a name="create-account-structures"></a><span data-ttu-id="e592c-103">Rekeningstructuren maken</span><span class="sxs-lookup"><span data-stu-id="e592c-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e592c-104">Deze taakbegeleiding helpt u bij het maken van een rekeningstructuur.</span><span class="sxs-lookup"><span data-stu-id="e592c-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="e592c-105">De stappen gebruiken het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="e592c-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="e592c-106">Ga naar Grootboek > Rekeningschema > Structuren > Rekeningstructuren configureren.</span><span class="sxs-lookup"><span data-stu-id="e592c-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="e592c-107">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="e592c-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="e592c-108">Typ in het veld Rekeningstructuur een naam om het doel van de rekeningstructuur te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="e592c-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="e592c-109">Typ in het veld Beschrijving een beschrijving om het doel van de rekeningstructuur op te geven.</span><span class="sxs-lookup"><span data-stu-id="e592c-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="e592c-110">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="e592c-110">Click Create.</span></span>
6. <span data-ttu-id="e592c-111">Klik op Segment toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-111">Click Add segment.</span></span>
7. <span data-ttu-id="e592c-112">Selecteer in de lijst Dimensies de dimensie die u aan de rekeningstructuur wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="e592c-113">Klik op Segment toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-113">Click Add segment.</span></span>
9. <span data-ttu-id="e592c-114">Klik op Segment toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-114">Click Add segment.</span></span>
10. <span data-ttu-id="e592c-115">Selecteer in de lijst Dimensies de dimensie die u aan de rekeningstructuur wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="e592c-116">Klik op Segment toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-116">Click Add segment.</span></span>
12. <span data-ttu-id="e592c-117">Klik op Segment toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-117">Click Add segment.</span></span>
13. <span data-ttu-id="e592c-118">Selecteer in de lijst Dimensies de dimensie die u aan de rekeningstructuur wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="e592c-119">Klik op Segment toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-119">Click Add segment.</span></span>
15. <span data-ttu-id="e592c-120">Selecteer in het raster het segment om de toegestane waarden te bewerken.</span><span class="sxs-lookup"><span data-stu-id="e592c-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e592c-121">Klik bijvoorbeeld in Hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="e592c-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="e592c-122">Selecteer in het veld Operator een optie, zoals 'ligt tussen' en 'bevat'.</span><span class="sxs-lookup"><span data-stu-id="e592c-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="e592c-123">Typ een waarde in het veld Waarde.</span><span class="sxs-lookup"><span data-stu-id="e592c-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e592c-124">Bijvoorbeeld 600000.</span><span class="sxs-lookup"><span data-stu-id="e592c-124">For example, 600000.</span></span>  
18. <span data-ttu-id="e592c-125">Typ een waarde in het veld Tot.</span><span class="sxs-lookup"><span data-stu-id="e592c-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="e592c-126">Bijvoorbeeld 699999.</span><span class="sxs-lookup"><span data-stu-id="e592c-126">For example, 699999.</span></span>  
19. <span data-ttu-id="e592c-127">Klik op Toepassen.</span><span class="sxs-lookup"><span data-stu-id="e592c-127">Click Apply.</span></span>
20. <span data-ttu-id="e592c-128">Selecteer in het raster het segment om de toegestane waarden te bewerken.</span><span class="sxs-lookup"><span data-stu-id="e592c-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e592c-129">Bijvoorbeeld Afdeling.</span><span class="sxs-lookup"><span data-stu-id="e592c-129">For example, Department.</span></span>  
21. <span data-ttu-id="e592c-130">Selecteer in het veld Operator een optie, zoals 'ligt tussen' en 'bevat'.</span><span class="sxs-lookup"><span data-stu-id="e592c-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="e592c-131">Typ een waarde in het veld Waarde.</span><span class="sxs-lookup"><span data-stu-id="e592c-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e592c-132">Bijvoorbeeld 022.</span><span class="sxs-lookup"><span data-stu-id="e592c-132">For example, 022.</span></span>  
23. <span data-ttu-id="e592c-133">Typ een waarde in het veld Tot.</span><span class="sxs-lookup"><span data-stu-id="e592c-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="e592c-134">Bijvoorbeeld 031.</span><span class="sxs-lookup"><span data-stu-id="e592c-134">For example, 031.</span></span>  
24. <span data-ttu-id="e592c-135">Klik op Nieuwe criteria toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="e592c-136">Selecteer in het veld Operator een optie, zoals 'ligt tussen' en 'bevat'.</span><span class="sxs-lookup"><span data-stu-id="e592c-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="e592c-137">Typ een waarde in het veld Waarde.</span><span class="sxs-lookup"><span data-stu-id="e592c-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="e592c-138">Bijvoorbeeld 033.</span><span class="sxs-lookup"><span data-stu-id="e592c-138">For example, 033.</span></span>  
27. <span data-ttu-id="e592c-139">Typ een waarde in het veld Tot.</span><span class="sxs-lookup"><span data-stu-id="e592c-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="e592c-140">Bijvoorbeeld 034.</span><span class="sxs-lookup"><span data-stu-id="e592c-140">For example, 034.</span></span>  
28. <span data-ttu-id="e592c-141">Klik op Toepassen.</span><span class="sxs-lookup"><span data-stu-id="e592c-141">Click Apply.</span></span>
29. <span data-ttu-id="e592c-142">Selecteer in het raster het segment om de toegestane waarden te bewerken.</span><span class="sxs-lookup"><span data-stu-id="e592c-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e592c-143">Bijvoorbeeld Kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="e592c-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="e592c-144">Typ een waarde in het veld CostCenter.</span><span class="sxs-lookup"><span data-stu-id="e592c-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="e592c-145">Bijvoorbeeld 007..021.</span><span class="sxs-lookup"><span data-stu-id="e592c-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="e592c-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e592c-146">Click Add.</span></span>
32. <span data-ttu-id="e592c-147">Typ een waarde in het veld MainAccount.</span><span class="sxs-lookup"><span data-stu-id="e592c-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="e592c-148">Bijvoorbeeld 600000..699999</span><span class="sxs-lookup"><span data-stu-id="e592c-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="e592c-149">Selecteer in het raster het segment om de toegestane waarden te bewerken.</span><span class="sxs-lookup"><span data-stu-id="e592c-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="e592c-150">Bijvoorbeeld Afdeling.</span><span class="sxs-lookup"><span data-stu-id="e592c-150">For example, Department.</span></span>  
34. <span data-ttu-id="e592c-151">Typ een waarde in het veld Afdeling.</span><span class="sxs-lookup"><span data-stu-id="e592c-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="e592c-152">Bijvoorbeeld 032.</span><span class="sxs-lookup"><span data-stu-id="e592c-152">For example, 032.</span></span>  
35. <span data-ttu-id="e592c-153">Typ een waarde in het veld CostCenter.</span><span class="sxs-lookup"><span data-stu-id="e592c-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="e592c-154">Bijvoorbeeld 086.</span><span class="sxs-lookup"><span data-stu-id="e592c-154">For example, 086.</span></span>  
36. <span data-ttu-id="e592c-155">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="e592c-155">Click Validate.</span></span>
37. <span data-ttu-id="e592c-156">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="e592c-156">Click Activate.</span></span>
38. <span data-ttu-id="e592c-157">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="e592c-157">Click Activate.</span></span>

