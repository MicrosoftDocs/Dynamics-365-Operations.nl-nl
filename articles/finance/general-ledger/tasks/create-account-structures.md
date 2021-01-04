---
title: Rekeningstructuren maken
description: Deze taakbegeleiding helpt u bij het maken van een rekeningstructuur.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: b75ee76a1fb874652415a2174441f629955d763a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442041"
---
# <a name="create-account-structures"></a><span data-ttu-id="805f9-103">Rekeningstructuren maken</span><span class="sxs-lookup"><span data-stu-id="805f9-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="805f9-104">Deze taakbegeleiding helpt u bij het maken van een rekeningstructuur.</span><span class="sxs-lookup"><span data-stu-id="805f9-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="805f9-105">De stappen gebruiken het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="805f9-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="805f9-106">Ga in het navigatievenster naar **Modules > Grootboek > Rekeningschema > Structuren > Regelstructuren configureren**.</span><span class="sxs-lookup"><span data-stu-id="805f9-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="805f9-107">Klik in het **actievenster** op **Nieuw** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="805f9-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="805f9-108">Typ in het veld **Rekeningstructuur** een naam om het doel van de rekeningstructuur te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="805f9-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="805f9-109">Typ in het veld **Beschrijving** een beschrijving om het doel van de rekeningstructuur op te geven.</span><span class="sxs-lookup"><span data-stu-id="805f9-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="805f9-110">Klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="805f9-110">Click **Create**.</span></span>
6. <span data-ttu-id="805f9-111">Klik in **Segmenten en toegestane waarden** op **Segment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="805f9-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="805f9-112">Selecteer in de lijst Dimensies de dimensie die u aan de rekeningstructuur wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="805f9-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="805f9-113">Klik aan het einde van de lijst op **Segment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="805f9-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="805f9-114">Herhaal stap 6 tot en met 9 zo nodig.</span><span class="sxs-lookup"><span data-stu-id="805f9-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="805f9-115">Selecteer in de sectie **Details van toegestane waarden** het segment om de toegestane waarden te bewerken.</span><span class="sxs-lookup"><span data-stu-id="805f9-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="805f9-116">Klik bijvoorbeeld in het veld **Hoofdrekening**.</span><span class="sxs-lookup"><span data-stu-id="805f9-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="805f9-117">Selecteer in het veld **Operator** een optie, zoals 'ligt tussen' en 'bevat'.</span><span class="sxs-lookup"><span data-stu-id="805f9-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="805f9-118">Typ een waarde in het veld **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="805f9-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="805f9-119">Bijvoorbeeld 600000.</span><span class="sxs-lookup"><span data-stu-id="805f9-119">For example, 600000.</span></span>  
13. <span data-ttu-id="805f9-120">Typ een waarde in het veld **Tot en met**.</span><span class="sxs-lookup"><span data-stu-id="805f9-120">In the **through** field, type a value.</span></span> <span data-ttu-id="805f9-121">Bijvoorbeeld 699999.</span><span class="sxs-lookup"><span data-stu-id="805f9-121">For example, 699999.</span></span>  
14. <span data-ttu-id="805f9-122">Klik in de sectie **Details van toegestane waarden** op **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="805f9-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="805f9-123">Herhaal stap 10 tot en met 15 zo nodig.</span><span class="sxs-lookup"><span data-stu-id="805f9-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="805f9-124">Klik in de sectie **Details van toegestane waarden** op **Nieuwe criteria toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="805f9-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="805f9-125">Selecteer in het veld Operator een optie, zoals 'ligt tussen' en 'bevat'.</span><span class="sxs-lookup"><span data-stu-id="805f9-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="805f9-126">Typ een waarde in het veld **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="805f9-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="805f9-127">Bijvoorbeeld 033.</span><span class="sxs-lookup"><span data-stu-id="805f9-127">For example, 033.</span></span>  
19. <span data-ttu-id="805f9-128">Typ een waarde in het veld **Tot en met**.</span><span class="sxs-lookup"><span data-stu-id="805f9-128">In the **through** field, type a value.</span></span> <span data-ttu-id="805f9-129">Bijvoorbeeld 034.</span><span class="sxs-lookup"><span data-stu-id="805f9-129">For example, 034.</span></span>  
20. <span data-ttu-id="805f9-130">Klik op **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="805f9-130">Click **Apply**.</span></span>
21. <span data-ttu-id="805f9-131">Selecteer in het raster het segment om de toegestane waarden te bewerken.</span><span class="sxs-lookup"><span data-stu-id="805f9-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="805f9-132">Bijvoorbeeld Kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="805f9-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="805f9-133">Typ een waarde in het veld **CostCenter**.</span><span class="sxs-lookup"><span data-stu-id="805f9-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="805f9-134">Bijvoorbeeld 007..021.</span><span class="sxs-lookup"><span data-stu-id="805f9-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="805f9-135">Klik in **Segmenten en toegestane waarden** op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="805f9-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="805f9-136">Typ een waarde in het veld **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="805f9-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="805f9-137">Bijvoorbeeld 600000..699999</span><span class="sxs-lookup"><span data-stu-id="805f9-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="805f9-138">Selecteer in het raster het segment om de toegestane waarden te bewerken.</span><span class="sxs-lookup"><span data-stu-id="805f9-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="805f9-139">Bijvoorbeeld Afdeling.</span><span class="sxs-lookup"><span data-stu-id="805f9-139">For example, Department.</span></span>  
26. <span data-ttu-id="805f9-140">Typ een waarde in het veld Afdeling.</span><span class="sxs-lookup"><span data-stu-id="805f9-140">In the Department field, type a value.</span></span> <span data-ttu-id="805f9-141">Bijvoorbeeld 032.</span><span class="sxs-lookup"><span data-stu-id="805f9-141">For example, 032.</span></span>  
27. <span data-ttu-id="805f9-142">Typ een waarde in het veld CostCenter.</span><span class="sxs-lookup"><span data-stu-id="805f9-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="805f9-143">Bijvoorbeeld 086.</span><span class="sxs-lookup"><span data-stu-id="805f9-143">For example, 086.</span></span>  
28. <span data-ttu-id="805f9-144">Klik in het **actievenster** op **Valideren**.</span><span class="sxs-lookup"><span data-stu-id="805f9-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="805f9-145">Klik in het **actievenster** op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="805f9-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="805f9-146">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="805f9-146">Click **Activate**.</span></span>

