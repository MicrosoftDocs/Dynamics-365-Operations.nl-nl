---
title: Grondstoffen maken (februari 2016)
description: Deze taak is gericht op het maken van de componenten van eindproducten en halffabricaten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e20abf8a1b211bff2bc73d1a36a1e5c917ffaab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844580"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="ea279-103">Grondstoffen maken (februari 2016)</span><span class="sxs-lookup"><span data-stu-id="ea279-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea279-104">Deze taak is gericht op het maken van de componenten van eindproducten en halffabricaten.</span><span class="sxs-lookup"><span data-stu-id="ea279-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="ea279-105">Dit is de derde taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="ea279-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="ea279-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="ea279-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="ea279-107">De eerste grondstof maken</span><span class="sxs-lookup"><span data-stu-id="ea279-107">Create the first material</span></span>
1. <span data-ttu-id="ea279-108">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="ea279-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ea279-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ea279-109">Click New.</span></span>
3. <span data-ttu-id="ea279-110">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="ea279-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ea279-111">Typ voor dit voorbeeld: 'Artikel_A'.</span><span class="sxs-lookup"><span data-stu-id="ea279-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="ea279-112">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-113">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="ea279-113">Select STD.</span></span> <span data-ttu-id="ea279-114">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="ea279-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="ea279-115">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-116">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="ea279-116">For example, select Audio.</span></span> <span data-ttu-id="ea279-117">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="ea279-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="ea279-118">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-119">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="ea279-119">Select SiteWH.</span></span> <span data-ttu-id="ea279-120">Alleen Locatie en Magazijn wordt gebruikt voor de demo.</span><span class="sxs-lookup"><span data-stu-id="ea279-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="ea279-121">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-122">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ea279-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ea279-123">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="ea279-123">Select None.</span></span>  
8. <span data-ttu-id="ea279-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ea279-124">Click OK.</span></span>
9. <span data-ttu-id="ea279-125">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="ea279-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="ea279-126">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="ea279-126">Click Default order settings.</span></span>
11. <span data-ttu-id="ea279-127">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-128">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ea279-129">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-130">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ea279-131">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-132">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="ea279-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-133">Close the page.</span></span>
15. <span data-ttu-id="ea279-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-134">Close the page.</span></span>
16. <span data-ttu-id="ea279-135">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ea279-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ea279-136">Klik op Artikel_A.</span><span class="sxs-lookup"><span data-stu-id="ea279-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="ea279-137">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="ea279-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="ea279-138">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ea279-139">Typ voor dit voorbeeld: 'M2'</span><span class="sxs-lookup"><span data-stu-id="ea279-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="ea279-140">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="ea279-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="ea279-141">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="ea279-141">Click Item price.</span></span>
21. <span data-ttu-id="ea279-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ea279-142">Click New.</span></span>
22. <span data-ttu-id="ea279-143">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="ea279-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-144">Selecteer voor dit voorbeeld 10, namelijk het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="ea279-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="ea279-145">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="ea279-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-146">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="ea279-147">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="ea279-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ea279-148">Typ voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="ea279-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="ea279-149">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ea279-149">Click Save.</span></span>
26. <span data-ttu-id="ea279-150">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="ea279-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="ea279-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-151">Close the page.</span></span>
28. <span data-ttu-id="ea279-152">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="ea279-153">De tweede grondstof maken</span><span class="sxs-lookup"><span data-stu-id="ea279-153">Create the second material</span></span>
1. <span data-ttu-id="ea279-154">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ea279-154">Click New.</span></span>
2. <span data-ttu-id="ea279-155">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="ea279-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ea279-156">Typ voor dit voorbeeld: 'Artikel_B'.</span><span class="sxs-lookup"><span data-stu-id="ea279-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="ea279-157">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-158">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="ea279-158">Select STD.</span></span> <span data-ttu-id="ea279-159">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="ea279-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="ea279-160">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-161">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="ea279-161">For example, select Audio.</span></span> <span data-ttu-id="ea279-162">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="ea279-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="ea279-163">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-164">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="ea279-164">Select SiteWH.</span></span> <span data-ttu-id="ea279-165">Alleen Locatie en Magazijn wordt gebruikt voor dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="ea279-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="ea279-166">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-167">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ea279-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ea279-168">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="ea279-168">Select None.</span></span>  
7. <span data-ttu-id="ea279-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ea279-169">Click OK.</span></span>
8. <span data-ttu-id="ea279-170">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="ea279-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="ea279-171">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="ea279-171">Click Default order settings.</span></span>
10. <span data-ttu-id="ea279-172">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-173">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="ea279-174">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-175">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ea279-176">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-177">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ea279-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-178">Close the page.</span></span>
14. <span data-ttu-id="ea279-179">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-179">Close the page.</span></span>
15. <span data-ttu-id="ea279-180">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ea279-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ea279-181">Klik op Artikel_B.</span><span class="sxs-lookup"><span data-stu-id="ea279-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="ea279-182">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="ea279-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="ea279-183">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ea279-184">Typ voor dit voorbeeld: 'M2'</span><span class="sxs-lookup"><span data-stu-id="ea279-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="ea279-185">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="ea279-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="ea279-186">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="ea279-186">Click Item price.</span></span>
20. <span data-ttu-id="ea279-187">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ea279-187">Click New.</span></span>
21. <span data-ttu-id="ea279-188">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="ea279-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-189">Selecteer voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="ea279-189">For this example, select 10.</span></span> <span data-ttu-id="ea279-190">Dit is het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="ea279-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="ea279-191">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="ea279-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-192">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="ea279-193">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="ea279-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ea279-194">Typ voor de demonstratie 10.</span><span class="sxs-lookup"><span data-stu-id="ea279-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="ea279-195">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ea279-195">Click Save.</span></span>
25. <span data-ttu-id="ea279-196">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="ea279-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="ea279-197">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-197">Close the page.</span></span>
27. <span data-ttu-id="ea279-198">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="ea279-199">De derde grondstof maken</span><span class="sxs-lookup"><span data-stu-id="ea279-199">Create the third material</span></span>
1. <span data-ttu-id="ea279-200">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ea279-200">Click New.</span></span>
2. <span data-ttu-id="ea279-201">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="ea279-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ea279-202">Typ voor de demonstratie: 'Artikel_C'.</span><span class="sxs-lookup"><span data-stu-id="ea279-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="ea279-203">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-204">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="ea279-204">Select STD.</span></span> <span data-ttu-id="ea279-205">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="ea279-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="ea279-206">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-207">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="ea279-207">For example, select Audio.</span></span> <span data-ttu-id="ea279-208">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="ea279-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="ea279-209">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-210">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="ea279-210">Select SiteWH.</span></span> <span data-ttu-id="ea279-211">Alleen Locatie en Magazijn wordt gebruikt voor de demo.</span><span class="sxs-lookup"><span data-stu-id="ea279-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="ea279-212">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-213">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ea279-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ea279-214">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="ea279-214">Select None.</span></span>  
7. <span data-ttu-id="ea279-215">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ea279-215">Click OK.</span></span>
8. <span data-ttu-id="ea279-216">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="ea279-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="ea279-217">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="ea279-217">Click Default order settings.</span></span>
10. <span data-ttu-id="ea279-218">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-219">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="ea279-220">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-221">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ea279-222">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="ea279-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-223">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ea279-224">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-224">Close the page.</span></span>
14. <span data-ttu-id="ea279-225">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-225">Close the page.</span></span>
15. <span data-ttu-id="ea279-226">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ea279-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ea279-227">Klik op Artikel_C.</span><span class="sxs-lookup"><span data-stu-id="ea279-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="ea279-228">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="ea279-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="ea279-229">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="ea279-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ea279-230">Typ voor dit voorbeeld: 'M1'</span><span class="sxs-lookup"><span data-stu-id="ea279-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="ea279-231">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="ea279-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="ea279-232">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="ea279-232">Click Item price.</span></span>
20. <span data-ttu-id="ea279-233">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ea279-233">Click New.</span></span>
21. <span data-ttu-id="ea279-234">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="ea279-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-235">Selecteer voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="ea279-235">For this example, select 10.</span></span> <span data-ttu-id="ea279-236">Dit is het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="ea279-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="ea279-237">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="ea279-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ea279-238">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="ea279-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="ea279-239">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="ea279-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ea279-240">Typ voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="ea279-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="ea279-241">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ea279-241">Click Save.</span></span>
25. <span data-ttu-id="ea279-242">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="ea279-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="ea279-243">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-243">Close the page.</span></span>
27. <span data-ttu-id="ea279-244">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea279-244">Close the page.</span></span>

