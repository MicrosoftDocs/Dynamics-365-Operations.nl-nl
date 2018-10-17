--- 
title: Een nomenclatuur met productnummers maken voor geconfigureerde productvarianten
description: In deze procedure wordt getoond hoe u een productnummernomenclatuur instelt voor vooraf geconfigureerde productvarianten, en hoe u deze aan een configureerbaar productmodel koppelt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 800afdf075f0675185514158f3b712a0fe7675e3
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="a4ebc-103">Een nomenclatuur met productnummers maken voor geconfigureerde productvarianten</span><span class="sxs-lookup"><span data-stu-id="a4ebc-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4ebc-104">In deze procedure wordt getoond hoe u een productnummernomenclatuur instelt voor vooraf geconfigureerde productvarianten, en hoe u deze aan een configureerbaar productmodel koppelt.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="a4ebc-105">In deze procedure ziet u ook hoe u een configuratienomenclatuur samenstelt voor een component van een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="a4ebc-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a4ebc-107">De nieuwe productnummernomenclatuur is toegewezen aan het productmodel D0004.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="a4ebc-108">Deze taak wordt meestal uitgevoerd door een productontwerper.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="a4ebc-109">Een productvariantnummer-nomenclatuur maken</span><span class="sxs-lookup"><span data-stu-id="a4ebc-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="a4ebc-110">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a4ebc-111">Klik op Productnomenclatuur.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="a4ebc-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-112">Click New.</span></span>
4. <span data-ttu-id="a4ebc-113">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a4ebc-114">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a4ebc-115">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-115">Click Add.</span></span>
7. <span data-ttu-id="a4ebc-116">Klik op Nummer van basismaster.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-116">Click Product master number.</span></span>
8. <span data-ttu-id="a4ebc-117">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-117">Click Add.</span></span>
9. <span data-ttu-id="a4ebc-118">Klik op Tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-118">Click Text constant.</span></span>
10. <span data-ttu-id="a4ebc-119">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="a4ebc-120">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="a4ebc-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-121">Click Add.</span></span>
13. <span data-ttu-id="a4ebc-122">Klik op Configuratie.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-122">Click Configuration.</span></span>
14. <span data-ttu-id="a4ebc-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="a4ebc-124">De productnummernomenclatuur toewijzen aan een productmodel</span><span class="sxs-lookup"><span data-stu-id="a4ebc-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="a4ebc-125">Klik op Basisproducten.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-125">Click Product masters.</span></span>
2. <span data-ttu-id="a4ebc-126">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a4ebc-127">Filter bijvoorbeeld het veld Productnummer op de waarde 'D'.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="a4ebc-128">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a4ebc-129">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-129">Click Edit.</span></span>
5. <span data-ttu-id="a4ebc-130">Selecteer Ja in het veld Nomenclatuur gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="a4ebc-131">Typ of selecteer een waarde in het veld Productvariantnummer-nomenclatuur.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="a4ebc-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-132">Close the page.</span></span>
8. <span data-ttu-id="a4ebc-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="a4ebc-134">Een nomenclatuur maken voor een productconfiguratiemodelcomponent</span><span class="sxs-lookup"><span data-stu-id="a4ebc-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="a4ebc-135">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="a4ebc-136">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a4ebc-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a4ebc-138">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-138">Click Edit.</span></span>
5. <span data-ttu-id="a4ebc-139">Selecteer Ja in het veld Configuratienomenclatuur gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="a4ebc-140">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-140">Click Add.</span></span>
7. <span data-ttu-id="a4ebc-141">Klik op Kenmerkwaarde.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-141">Click Attribute value.</span></span>
8. <span data-ttu-id="a4ebc-142">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a4ebc-143">Typ of selecteer een waarde in het veld Kenmerk.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="a4ebc-144">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-144">Click Add.</span></span>
11. <span data-ttu-id="a4ebc-145">Klik op Tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-145">Click Text constant.</span></span>
12. <span data-ttu-id="a4ebc-146">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="a4ebc-147">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="a4ebc-148">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-148">Click Add.</span></span>
15. <span data-ttu-id="a4ebc-149">Klik op Kenmerkwaarde.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-149">Click Attribute value.</span></span>
16. <span data-ttu-id="a4ebc-150">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="a4ebc-151">Typ of selecteer een waarde in het veld Kenmerk.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="a4ebc-152">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-152">Click Add.</span></span>
19. <span data-ttu-id="a4ebc-153">Klik op Tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-153">Click Text constant.</span></span>
20. <span data-ttu-id="a4ebc-154">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="a4ebc-155">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="a4ebc-156">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-156">Click Add.</span></span>
23. <span data-ttu-id="a4ebc-157">Klik op Kenmerkwaarde.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-157">Click Attribute value.</span></span>
24. <span data-ttu-id="a4ebc-158">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="a4ebc-159">Typ of selecteer een waarde in het veld Kenmerk.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="a4ebc-160">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-160">Click Add.</span></span>
27. <span data-ttu-id="a4ebc-161">Klik op Tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-161">Click Text constant.</span></span>
28. <span data-ttu-id="a4ebc-162">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="a4ebc-163">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="a4ebc-164">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-164">Click Add.</span></span>
31. <span data-ttu-id="a4ebc-165">Klik op Kenmerkwaarde.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-165">Click Attribute value.</span></span>
32. <span data-ttu-id="a4ebc-166">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="a4ebc-167">Typ of selecteer een waarde in het veld Kenmerk.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="a4ebc-168">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-168">Click Add.</span></span>
35. <span data-ttu-id="a4ebc-169">Klik op Tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-169">Click Text constant.</span></span>
36. <span data-ttu-id="a4ebc-170">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="a4ebc-171">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="a4ebc-172">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-172">Click Add.</span></span>
39. <span data-ttu-id="a4ebc-173">Klik op Nummerreekswaarde.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="a4ebc-174">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="a4ebc-175">Typ of selecteer een waarde in het veld Nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="a4ebc-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-176">Close the page.</span></span>
43. <span data-ttu-id="a4ebc-177">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-177">Close the page.</span></span>
44. <span data-ttu-id="a4ebc-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4ebc-178">Close the page.</span></span>


