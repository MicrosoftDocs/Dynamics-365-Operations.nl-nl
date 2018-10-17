--- 
title: Grondstoffen maken (februari 2016)
description: Deze taak is gericht op het maken van de componenten van eindproducten en halffabricaten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="cdf37-103">Grondstoffen maken (februari 2016)</span><span class="sxs-lookup"><span data-stu-id="cdf37-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cdf37-104">Deze taak is gericht op het maken van de componenten van eindproducten en halffabricaten.</span><span class="sxs-lookup"><span data-stu-id="cdf37-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="cdf37-105">Dit is de derde taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="cdf37-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="cdf37-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="cdf37-107">De eerste grondstof maken</span><span class="sxs-lookup"><span data-stu-id="cdf37-107">Create the first material</span></span>
1. <span data-ttu-id="cdf37-108">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="cdf37-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="cdf37-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cdf37-109">Click New.</span></span>
3. <span data-ttu-id="cdf37-110">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="cdf37-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="cdf37-111">Typ voor dit voorbeeld: 'Artikel_A'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="cdf37-112">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-113">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="cdf37-113">Select STD.</span></span> <span data-ttu-id="cdf37-114">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="cdf37-115">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-116">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-116">For example, select Audio.</span></span> <span data-ttu-id="cdf37-117">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="cdf37-118">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-119">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-119">Select SiteWH.</span></span> <span data-ttu-id="cdf37-120">Alleen Locatie en Magazijn wordt gebruikt voor de demo.</span><span class="sxs-lookup"><span data-stu-id="cdf37-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="cdf37-121">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-122">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cdf37-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="cdf37-123">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-123">Select None.</span></span>  
8. <span data-ttu-id="cdf37-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cdf37-124">Click OK.</span></span>
9. <span data-ttu-id="cdf37-125">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="cdf37-126">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-126">Click Default order settings.</span></span>
11. <span data-ttu-id="cdf37-127">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-128">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="cdf37-129">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-130">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="cdf37-131">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-132">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="cdf37-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-133">Close the page.</span></span>
15. <span data-ttu-id="cdf37-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-134">Close the page.</span></span>
16. <span data-ttu-id="cdf37-135">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cdf37-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cdf37-136">Klik op Artikel_A.</span><span class="sxs-lookup"><span data-stu-id="cdf37-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="cdf37-137">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="cdf37-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="cdf37-138">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="cdf37-139">Typ voor dit voorbeeld: 'M2'</span><span class="sxs-lookup"><span data-stu-id="cdf37-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="cdf37-140">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="cdf37-141">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="cdf37-141">Click Item price.</span></span>
21. <span data-ttu-id="cdf37-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cdf37-142">Click New.</span></span>
22. <span data-ttu-id="cdf37-143">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="cdf37-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-144">Selecteer voor dit voorbeeld 10, namelijk het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="cdf37-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="cdf37-145">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="cdf37-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-146">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="cdf37-147">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="cdf37-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="cdf37-148">Typ voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="cdf37-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="cdf37-149">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cdf37-149">Click Save.</span></span>
26. <span data-ttu-id="cdf37-150">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="cdf37-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-151">Close the page.</span></span>
28. <span data-ttu-id="cdf37-152">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="cdf37-153">De tweede grondstof maken</span><span class="sxs-lookup"><span data-stu-id="cdf37-153">Create the second material</span></span>
1. <span data-ttu-id="cdf37-154">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cdf37-154">Click New.</span></span>
2. <span data-ttu-id="cdf37-155">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="cdf37-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="cdf37-156">Typ voor dit voorbeeld: 'Artikel_B'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="cdf37-157">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-158">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="cdf37-158">Select STD.</span></span> <span data-ttu-id="cdf37-159">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="cdf37-160">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-161">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-161">For example, select Audio.</span></span> <span data-ttu-id="cdf37-162">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="cdf37-163">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-164">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-164">Select SiteWH.</span></span> <span data-ttu-id="cdf37-165">Alleen Locatie en Magazijn wordt gebruikt voor dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="cdf37-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="cdf37-166">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-167">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cdf37-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="cdf37-168">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-168">Select None.</span></span>  
7. <span data-ttu-id="cdf37-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cdf37-169">Click OK.</span></span>
8. <span data-ttu-id="cdf37-170">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="cdf37-171">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-171">Click Default order settings.</span></span>
10. <span data-ttu-id="cdf37-172">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-173">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="cdf37-174">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-175">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="cdf37-176">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-177">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="cdf37-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-178">Close the page.</span></span>
14. <span data-ttu-id="cdf37-179">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-179">Close the page.</span></span>
15. <span data-ttu-id="cdf37-180">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cdf37-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cdf37-181">Klik op Artikel_B.</span><span class="sxs-lookup"><span data-stu-id="cdf37-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="cdf37-182">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="cdf37-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="cdf37-183">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="cdf37-184">Typ voor dit voorbeeld: 'M2'</span><span class="sxs-lookup"><span data-stu-id="cdf37-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="cdf37-185">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="cdf37-186">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="cdf37-186">Click Item price.</span></span>
20. <span data-ttu-id="cdf37-187">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cdf37-187">Click New.</span></span>
21. <span data-ttu-id="cdf37-188">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="cdf37-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-189">Selecteer voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="cdf37-189">For this example, select 10.</span></span> <span data-ttu-id="cdf37-190">Dit is het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="cdf37-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="cdf37-191">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="cdf37-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-192">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="cdf37-193">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="cdf37-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="cdf37-194">Typ voor de demonstratie 10.</span><span class="sxs-lookup"><span data-stu-id="cdf37-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="cdf37-195">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cdf37-195">Click Save.</span></span>
25. <span data-ttu-id="cdf37-196">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="cdf37-197">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-197">Close the page.</span></span>
27. <span data-ttu-id="cdf37-198">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="cdf37-199">De derde grondstof maken</span><span class="sxs-lookup"><span data-stu-id="cdf37-199">Create the third material</span></span>
1. <span data-ttu-id="cdf37-200">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cdf37-200">Click New.</span></span>
2. <span data-ttu-id="cdf37-201">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="cdf37-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="cdf37-202">Typ voor de demonstratie: 'Artikel_C'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="cdf37-203">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-204">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="cdf37-204">Select STD.</span></span> <span data-ttu-id="cdf37-205">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="cdf37-206">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-207">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-207">For example, select Audio.</span></span> <span data-ttu-id="cdf37-208">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="cdf37-209">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-210">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-210">Select SiteWH.</span></span> <span data-ttu-id="cdf37-211">Alleen Locatie en Magazijn wordt gebruikt voor de demo.</span><span class="sxs-lookup"><span data-stu-id="cdf37-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="cdf37-212">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-213">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cdf37-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="cdf37-214">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="cdf37-214">Select None.</span></span>  
7. <span data-ttu-id="cdf37-215">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cdf37-215">Click OK.</span></span>
8. <span data-ttu-id="cdf37-216">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="cdf37-217">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="cdf37-217">Click Default order settings.</span></span>
10. <span data-ttu-id="cdf37-218">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-219">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="cdf37-220">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-221">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="cdf37-222">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="cdf37-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-223">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="cdf37-224">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-224">Close the page.</span></span>
14. <span data-ttu-id="cdf37-225">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-225">Close the page.</span></span>
15. <span data-ttu-id="cdf37-226">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="cdf37-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cdf37-227">Klik op Artikel_C.</span><span class="sxs-lookup"><span data-stu-id="cdf37-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="cdf37-228">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="cdf37-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="cdf37-229">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="cdf37-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="cdf37-230">Typ voor dit voorbeeld: 'M1'</span><span class="sxs-lookup"><span data-stu-id="cdf37-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="cdf37-231">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="cdf37-232">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="cdf37-232">Click Item price.</span></span>
20. <span data-ttu-id="cdf37-233">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cdf37-233">Click New.</span></span>
21. <span data-ttu-id="cdf37-234">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="cdf37-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-235">Selecteer voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="cdf37-235">For this example, select 10.</span></span> <span data-ttu-id="cdf37-236">Dit is het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="cdf37-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="cdf37-237">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="cdf37-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="cdf37-238">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="cdf37-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="cdf37-239">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="cdf37-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="cdf37-240">Typ voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="cdf37-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="cdf37-241">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cdf37-241">Click Save.</span></span>
25. <span data-ttu-id="cdf37-242">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="cdf37-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="cdf37-243">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-243">Close the page.</span></span>
27. <span data-ttu-id="cdf37-244">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cdf37-244">Close the page.</span></span>

