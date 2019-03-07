---
title: Grondstoffen maken (uitsluitend februari 2016)
description: Deze taak is gericht op het maken van de componenten van eindproducten en halffabricaten.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 869acddf6f7e9754bb4952176ded4b22c74eaffd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "327292"
---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="f791f-103">Grondstoffen maken (uitsluitend februari 2016)</span><span class="sxs-lookup"><span data-stu-id="f791f-103">Create raw materials (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f791f-104">Deze taak is gericht op het maken van de componenten van eindproducten en halffabricaten.</span><span class="sxs-lookup"><span data-stu-id="f791f-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="f791f-105">Dit is de derde taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f791f-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="f791f-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f791f-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="f791f-107">De eerste grondstof maken</span><span class="sxs-lookup"><span data-stu-id="f791f-107">Create the first material</span></span>
1. <span data-ttu-id="f791f-108">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="f791f-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f791f-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f791f-109">Click New.</span></span>
3. <span data-ttu-id="f791f-110">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="f791f-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f791f-111">Typ voor dit voorbeeld: 'Artikel_A'.</span><span class="sxs-lookup"><span data-stu-id="f791f-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="f791f-112">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-113">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="f791f-113">Select STD.</span></span> <span data-ttu-id="f791f-114">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f791f-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="f791f-115">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-116">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="f791f-116">For example, select Audio.</span></span> <span data-ttu-id="f791f-117">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f791f-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="f791f-118">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-119">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="f791f-119">Select SiteWH.</span></span> <span data-ttu-id="f791f-120">Alleen Locatie en Magazijn wordt gebruikt voor de demo.</span><span class="sxs-lookup"><span data-stu-id="f791f-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="f791f-121">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-122">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f791f-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f791f-123">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="f791f-123">Select None.</span></span>  
8. <span data-ttu-id="f791f-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f791f-124">Click OK.</span></span>
9. <span data-ttu-id="f791f-125">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="f791f-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="f791f-126">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="f791f-126">Click Default order settings.</span></span>
11. <span data-ttu-id="f791f-127">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-128">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f791f-129">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-130">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f791f-131">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-132">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="f791f-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-133">Close the page.</span></span>
15. <span data-ttu-id="f791f-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-134">Close the page.</span></span>
16. <span data-ttu-id="f791f-135">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f791f-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f791f-136">Klik op Artikel_A.</span><span class="sxs-lookup"><span data-stu-id="f791f-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="f791f-137">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="f791f-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="f791f-138">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f791f-139">Typ voor dit voorbeeld: 'M2'</span><span class="sxs-lookup"><span data-stu-id="f791f-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="f791f-140">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="f791f-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="f791f-141">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="f791f-141">Click Item price.</span></span>
21. <span data-ttu-id="f791f-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f791f-142">Click New.</span></span>
22. <span data-ttu-id="f791f-143">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="f791f-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-144">Selecteer voor dit voorbeeld 10, namelijk het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="f791f-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="f791f-145">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="f791f-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-146">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="f791f-147">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="f791f-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f791f-148">Typ voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="f791f-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="f791f-149">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f791f-149">Click Save.</span></span>
26. <span data-ttu-id="f791f-150">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="f791f-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="f791f-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-151">Close the page.</span></span>
28. <span data-ttu-id="f791f-152">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="f791f-153">De tweede grondstof maken</span><span class="sxs-lookup"><span data-stu-id="f791f-153">Create the second material</span></span>
1. <span data-ttu-id="f791f-154">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f791f-154">Click New.</span></span>
2. <span data-ttu-id="f791f-155">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="f791f-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f791f-156">Typ voor dit voorbeeld: 'Artikel_B'.</span><span class="sxs-lookup"><span data-stu-id="f791f-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="f791f-157">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-158">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="f791f-158">Select STD.</span></span> <span data-ttu-id="f791f-159">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f791f-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="f791f-160">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-161">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="f791f-161">For example, select Audio.</span></span> <span data-ttu-id="f791f-162">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f791f-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="f791f-163">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-164">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="f791f-164">Select SiteWH.</span></span> <span data-ttu-id="f791f-165">Alleen Locatie en Magazijn wordt gebruikt voor dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="f791f-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="f791f-166">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-167">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f791f-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f791f-168">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="f791f-168">Select None.</span></span>  
7. <span data-ttu-id="f791f-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f791f-169">Click OK.</span></span>
8. <span data-ttu-id="f791f-170">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="f791f-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="f791f-171">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="f791f-171">Click Default order settings.</span></span>
10. <span data-ttu-id="f791f-172">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-173">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="f791f-174">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-175">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f791f-176">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-177">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f791f-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-178">Close the page.</span></span>
14. <span data-ttu-id="f791f-179">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-179">Close the page.</span></span>
15. <span data-ttu-id="f791f-180">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f791f-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f791f-181">Klik op Artikel_B.</span><span class="sxs-lookup"><span data-stu-id="f791f-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="f791f-182">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="f791f-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="f791f-183">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f791f-184">Typ voor dit voorbeeld: 'M2'</span><span class="sxs-lookup"><span data-stu-id="f791f-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="f791f-185">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="f791f-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="f791f-186">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="f791f-186">Click Item price.</span></span>
20. <span data-ttu-id="f791f-187">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f791f-187">Click New.</span></span>
21. <span data-ttu-id="f791f-188">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="f791f-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-189">Selecteer voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="f791f-189">For this example, select 10.</span></span> <span data-ttu-id="f791f-190">Dit is het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="f791f-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="f791f-191">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="f791f-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-192">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="f791f-193">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="f791f-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f791f-194">Typ voor de demonstratie 10.</span><span class="sxs-lookup"><span data-stu-id="f791f-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="f791f-195">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f791f-195">Click Save.</span></span>
25. <span data-ttu-id="f791f-196">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="f791f-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="f791f-197">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-197">Close the page.</span></span>
27. <span data-ttu-id="f791f-198">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="f791f-199">De derde grondstof maken</span><span class="sxs-lookup"><span data-stu-id="f791f-199">Create the third material</span></span>
1. <span data-ttu-id="f791f-200">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f791f-200">Click New.</span></span>
2. <span data-ttu-id="f791f-201">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="f791f-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f791f-202">Typ voor de demonstratie: 'Artikel_C'.</span><span class="sxs-lookup"><span data-stu-id="f791f-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="f791f-203">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-204">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="f791f-204">Select STD.</span></span> <span data-ttu-id="f791f-205">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f791f-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="f791f-206">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-207">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="f791f-207">For example, select Audio.</span></span> <span data-ttu-id="f791f-208">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f791f-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="f791f-209">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-210">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="f791f-210">Select SiteWH.</span></span> <span data-ttu-id="f791f-211">Alleen Locatie en Magazijn wordt gebruikt voor de demo.</span><span class="sxs-lookup"><span data-stu-id="f791f-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="f791f-212">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-213">Traceringsdimensies worden niet voor dit voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f791f-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f791f-214">Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="f791f-214">Select None.</span></span>  
7. <span data-ttu-id="f791f-215">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f791f-215">Click OK.</span></span>
8. <span data-ttu-id="f791f-216">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="f791f-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="f791f-217">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="f791f-217">Click Default order settings.</span></span>
10. <span data-ttu-id="f791f-218">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-219">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="f791f-220">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-221">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f791f-222">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="f791f-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-223">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f791f-224">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-224">Close the page.</span></span>
14. <span data-ttu-id="f791f-225">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-225">Close the page.</span></span>
15. <span data-ttu-id="f791f-226">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f791f-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f791f-227">Klik op Artikel_C.</span><span class="sxs-lookup"><span data-stu-id="f791f-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="f791f-228">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="f791f-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="f791f-229">Typ een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="f791f-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f791f-230">Typ voor dit voorbeeld: 'M1'</span><span class="sxs-lookup"><span data-stu-id="f791f-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="f791f-231">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="f791f-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="f791f-232">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="f791f-232">Click Item price.</span></span>
20. <span data-ttu-id="f791f-233">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f791f-233">Click New.</span></span>
21. <span data-ttu-id="f791f-234">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="f791f-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-235">Selecteer voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="f791f-235">For this example, select 10.</span></span> <span data-ttu-id="f791f-236">Dit is het kostprijsberekeningstype van de standaardkostprijs.</span><span class="sxs-lookup"><span data-stu-id="f791f-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="f791f-237">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="f791f-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f791f-238">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f791f-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="f791f-239">Voer een getal in het veld Prijs in.</span><span class="sxs-lookup"><span data-stu-id="f791f-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f791f-240">Typ voor dit voorbeeld 10.</span><span class="sxs-lookup"><span data-stu-id="f791f-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="f791f-241">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f791f-241">Click Save.</span></span>
25. <span data-ttu-id="f791f-242">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="f791f-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="f791f-243">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-243">Close the page.</span></span>
27. <span data-ttu-id="f791f-244">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f791f-244">Close the page.</span></span>

