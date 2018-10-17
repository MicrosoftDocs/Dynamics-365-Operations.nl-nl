--- 
title: Stuklijsten maken (februari 2016)
description: Deze taak is gericht op het maken van de stuklijststructuur voor een eindproduct en een halffabricaat.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="create-boms-february-2016"></a><span data-ttu-id="7b418-103">Stuklijsten maken (februari 2016)</span><span class="sxs-lookup"><span data-stu-id="7b418-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b418-104">Deze taak is gericht op het maken van de stuklijststructuur voor een eindproduct en een halffabricaat.</span><span class="sxs-lookup"><span data-stu-id="7b418-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="7b418-105">Dit is de vierde taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="7b418-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="7b418-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="7b418-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="7b418-107">Een stuklijst voor een halffabricaat maken</span><span class="sxs-lookup"><span data-stu-id="7b418-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="7b418-108">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="7b418-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7b418-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="7b418-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7b418-110">Selecteer het artikelnummer Stuklijst_2.</span><span class="sxs-lookup"><span data-stu-id="7b418-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="7b418-111">Klik op Technicus in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="7b418-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="7b418-112">Klik op Stuklijstversies.</span><span class="sxs-lookup"><span data-stu-id="7b418-112">Click BOM versions.</span></span>
5. <span data-ttu-id="7b418-113">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="7b418-113">Click New.</span></span>
6. <span data-ttu-id="7b418-114">Klik op Stuklijst en stuklijstversie.</span><span class="sxs-lookup"><span data-stu-id="7b418-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="7b418-115">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7b418-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7b418-116">Typ bijvoorbeeld Stuklijst_2.</span><span class="sxs-lookup"><span data-stu-id="7b418-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="7b418-117">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="7b418-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7b418-118">Typ of selecteer voor dit voorbeeld Locatie 1.</span><span class="sxs-lookup"><span data-stu-id="7b418-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="7b418-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7b418-119">Click OK.</span></span>
10. <span data-ttu-id="7b418-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="7b418-120">Click New.</span></span>
11. <span data-ttu-id="7b418-121">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="7b418-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7b418-122">Typ voor dit voorbeeld: 'Artikel_C'.</span><span class="sxs-lookup"><span data-stu-id="7b418-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="7b418-123">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="7b418-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7b418-124">Typ of selecteer voor dit voorbeeld 11.</span><span class="sxs-lookup"><span data-stu-id="7b418-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="7b418-125">Klik op Koptekst.</span><span class="sxs-lookup"><span data-stu-id="7b418-125">Click Header.</span></span>
14. <span data-ttu-id="7b418-126">Klik op Goedkeuring om stuklijsten goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="7b418-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="7b418-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7b418-127">Click OK.</span></span>
16. <span data-ttu-id="7b418-128">Klik op Goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="7b418-128">Click Approve.</span></span>
    * <span data-ttu-id="7b418-129">De knop Goedkeuren bevindt zich op de werkbalk in de sectie Stuklijstversies.</span><span class="sxs-lookup"><span data-stu-id="7b418-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="7b418-130">Als de knop Goedkeuren niet zichtbaar is, klikt u op Koptekst in de rechterbovenhoek van de pagina Stuklijsten om de knop zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="7b418-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="7b418-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7b418-131">Click OK.</span></span>
18. <span data-ttu-id="7b418-132">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="7b418-132">Click Activate.</span></span>
19. <span data-ttu-id="7b418-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7b418-133">Close the page.</span></span>
20. <span data-ttu-id="7b418-134">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7b418-134">Close the page.</span></span>
21. <span data-ttu-id="7b418-135">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7b418-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="7b418-136">Een stuklijst voor een eindproduct maken</span><span class="sxs-lookup"><span data-stu-id="7b418-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="7b418-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="7b418-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7b418-138">Selecteer het artikelnummer Stuklijst_1.</span><span class="sxs-lookup"><span data-stu-id="7b418-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="7b418-139">Klik op Technicus in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="7b418-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="7b418-140">Klik op Stuklijstversies.</span><span class="sxs-lookup"><span data-stu-id="7b418-140">Click BOM versions.</span></span>
4. <span data-ttu-id="7b418-141">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="7b418-141">Click New.</span></span>
5. <span data-ttu-id="7b418-142">Klik op Stuklijst en stuklijstversie.</span><span class="sxs-lookup"><span data-stu-id="7b418-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="7b418-143">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7b418-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7b418-144">Typ bijvoorbeeld Stuklijst_1.</span><span class="sxs-lookup"><span data-stu-id="7b418-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="7b418-145">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="7b418-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7b418-146">Typ of selecteer voor dit voorbeeld Locatie 1.</span><span class="sxs-lookup"><span data-stu-id="7b418-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="7b418-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7b418-147">Click OK.</span></span>
9. <span data-ttu-id="7b418-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="7b418-148">Click New.</span></span>
10. <span data-ttu-id="7b418-149">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="7b418-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7b418-150">Typ voor dit voorbeeld: 'Artikel_A'.</span><span class="sxs-lookup"><span data-stu-id="7b418-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="7b418-151">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="7b418-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7b418-152">Selecteer voor dit voorbeeld 11.</span><span class="sxs-lookup"><span data-stu-id="7b418-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="7b418-153">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="7b418-153">Click New.</span></span>
13. <span data-ttu-id="7b418-154">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="7b418-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7b418-155">Typ voor dit voorbeeld: 'Artikel_B'.</span><span class="sxs-lookup"><span data-stu-id="7b418-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="7b418-156">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="7b418-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7b418-157">Typ of selecteer voor dit voorbeeld 11.</span><span class="sxs-lookup"><span data-stu-id="7b418-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="7b418-158">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="7b418-158">Click New.</span></span>
16. <span data-ttu-id="7b418-159">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="7b418-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7b418-160">Typ voor dit voorbeeld: 'Stuklijst_2'.</span><span class="sxs-lookup"><span data-stu-id="7b418-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="7b418-161">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="7b418-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="7b418-162">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="7b418-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7b418-163">Typ of selecteer voor dit voorbeeld magazijn 11.</span><span class="sxs-lookup"><span data-stu-id="7b418-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="7b418-164">Klik op Koptekst.</span><span class="sxs-lookup"><span data-stu-id="7b418-164">Click Header.</span></span>
20. <span data-ttu-id="7b418-165">Klik op Goedkeuring om stuklijsten goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="7b418-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="7b418-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7b418-166">Click OK.</span></span>
22. <span data-ttu-id="7b418-167">Klik op Goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="7b418-167">Click Approve.</span></span>
    * <span data-ttu-id="7b418-168">De knop Goedkeuren bevindt zich op de werkbalk in de sectie Stuklijstversies.</span><span class="sxs-lookup"><span data-stu-id="7b418-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="7b418-169">Als de knop Goedkeuren niet zichtbaar is, klikt u op Koptekst in de rechterbovenhoek van de pagina Stuklijsten om de knop zichtbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="7b418-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="7b418-170">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7b418-170">Click OK.</span></span>
24. <span data-ttu-id="7b418-171">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="7b418-171">Click Activate.</span></span>
25. <span data-ttu-id="7b418-172">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7b418-172">Close the page.</span></span>
26. <span data-ttu-id="7b418-173">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7b418-173">Close the page.</span></span>
27. <span data-ttu-id="7b418-174">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7b418-174">Close the page.</span></span>


