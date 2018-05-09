--- 
title: Boekingsprofielen voor vaste activa instellen
description: Deze taakbegeleiding stelt boekingsprofielen voor vaste activa in.
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d07df2c2779833485bd70240c47bb569622800f8
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="c0fbd-103">Boekingsprofielen voor vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="c0fbd-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0fbd-104">Deze taakbegeleiding stelt boekingsprofielen voor vaste activa in.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="c0fbd-105">Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="c0fbd-106">De voorbeelden in de taakbegeleiding zijn voor een basisboekingsprofiel, hoewel de boekingsprofielen voor uw specifieke rekeningschema en financiële rapportagebehoeften moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="c0fbd-107">Ga naar Vaste activa > Instellingen > Boekingsprofielen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="c0fbd-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-108">Click New.</span></span>
3. <span data-ttu-id="c0fbd-109">Typ een waarde in het veld Boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="c0fbd-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c0fbd-111">U moet een boekingsprofiel maken voor elk type vaste-activatransactie dat u gebruikt bij het werken met vaste activa.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="c0fbd-112">Deze taakbegeleiding start met het type Bijboekingstransactie.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="c0fbd-113">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-113">Click Add.</span></span>
6. <span data-ttu-id="c0fbd-114">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="c0fbd-115">Met het veld Groeperingen kunt u het boekingsprofiel definiëren tot de Tabel (één rekening ingesteld voor elk vast activum) of Groep (één rekening ingesteld voor elke vaste-activagroep).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="c0fbd-116">Voor deze taakbegeleiding blijft de waarde op "Alle" ingesteld voor toepassing op alle vaste activa met het opgegeven boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="c0fbd-117">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="c0fbd-118">Voor bijboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="c0fbd-119">Selecteer in het veld Transactietype de optie Verwervingscorrectie.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="c0fbd-120">Voor bijboekingscorrectietransacties worden dezelfde rekeningen als voor bijboekingstransacties gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="c0fbd-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-121">Click Add.</span></span>
10. <span data-ttu-id="c0fbd-122">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="c0fbd-123">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="c0fbd-124">Voor bijboekingscorrecties kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="c0fbd-125">Selecteer Afschrijving in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="c0fbd-126">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-126">Click Add.</span></span>
14. <span data-ttu-id="c0fbd-127">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="c0fbd-128">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="c0fbd-129">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="c0fbd-130">Selecteer Afschrijvingscorrectie in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="c0fbd-131">Voor afschrijvingscorrectietransacties worden dezelfde rekeningen als voor afschrijvingstransacties gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="c0fbd-132">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-132">Click Add.</span></span>
19. <span data-ttu-id="c0fbd-133">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="c0fbd-134">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="c0fbd-135">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="c0fbd-136">Selecteer Verkoop/afstoting in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="c0fbd-137">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-137">Click Add.</span></span>
24. <span data-ttu-id="c0fbd-138">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="c0fbd-139">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="c0fbd-140">Voor afboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="c0fbd-141">Selecteer Afstoting - uitval in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="c0fbd-142">We gebruiken dezelfde rekeningen voor Afstotingsverkoop en Afstotingsuitval.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="c0fbd-143">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-143">Click Add.</span></span>
28. <span data-ttu-id="c0fbd-144">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="c0fbd-145">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="c0fbd-146">Voor afboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="c0fbd-147">Vouw de sectie Afstoting uit.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="c0fbd-148">U moet boekingsprofielen voor afboeking voor zowel verkoop als uitval instellen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="c0fbd-149">Wij zullen met de transacties van de afboekingsverkoop starten.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="c0fbd-150">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-150">Click Add.</span></span>
32. <span data-ttu-id="c0fbd-151">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="c0fbd-152">Selecteer Aanschafwaarde in het veld Waarde boeken.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="c0fbd-153">De bijboekingswaarde geldt voor bijboekings- en bijboekingscorrectiewaarden voor alle jaren.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="c0fbd-154">U kunt ook rekeningen voor deze transactietypen afzonderlijk definiëren.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="c0fbd-155">U kunt het afboekingsproces instellen om verschillende rekeningen te gebruiken die afhankelijk zijn van of de afboeking in winst of een verlies resulteert.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="c0fbd-156">Ik stel het type verkoopwaarde in op Alle om dezelfde rekeningen voor alle typen afboekingen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="c0fbd-157">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="c0fbd-158">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="c0fbd-159">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-159">Click Add.</span></span>
37. <span data-ttu-id="c0fbd-160">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="c0fbd-161">Selecteer in het veld Waarde boeken de optie Afschrijving (voorgaande jaren).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="c0fbd-162">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="c0fbd-163">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="c0fbd-164">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-164">Click Add.</span></span>
41. <span data-ttu-id="c0fbd-165">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="c0fbd-166">Selecteer in het veld Waarde boeken de optie Afschrijving (dit jaar).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="c0fbd-167">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="c0fbd-168">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="c0fbd-169">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-169">Click Add.</span></span>
46. <span data-ttu-id="c0fbd-170">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="c0fbd-171">Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (voorgaande jaren).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="c0fbd-172">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="c0fbd-173">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="c0fbd-174">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-174">Click Add.</span></span>
51. <span data-ttu-id="c0fbd-175">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="c0fbd-176">Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (dit jaar).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="c0fbd-177">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="c0fbd-178">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="c0fbd-179">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-179">Click Add.</span></span>
56. <span data-ttu-id="c0fbd-180">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="c0fbd-181">Selecteer Nettoboekwaarde in het veld Waarde boeken.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="c0fbd-182">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="c0fbd-183">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="c0fbd-184">Selecteer Uitval in het veld Verkoop of uitval.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="c0fbd-185">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-185">Click Add.</span></span>
62. <span data-ttu-id="c0fbd-186">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="c0fbd-187">Selecteer Aanschafwaarde in het veld Waarde boeken.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="c0fbd-188">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="c0fbd-189">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="c0fbd-190">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-190">Click Add.</span></span>
67. <span data-ttu-id="c0fbd-191">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="c0fbd-192">Selecteer in het veld Waarde boeken de optie Afschrijving (voorgaande jaren).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="c0fbd-193">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="c0fbd-194">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="c0fbd-195">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-195">Click Add.</span></span>
71. <span data-ttu-id="c0fbd-196">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="c0fbd-197">Selecteer in het veld Waarde boeken de optie Afschrijving (dit jaar).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="c0fbd-198">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="c0fbd-199">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="c0fbd-200">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-200">Click Add.</span></span>
76. <span data-ttu-id="c0fbd-201">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="c0fbd-202">Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (voorgaande jaren).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="c0fbd-203">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="c0fbd-204">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="c0fbd-205">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-205">Click Add.</span></span>
81. <span data-ttu-id="c0fbd-206">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="c0fbd-207">Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (dit jaar).</span><span class="sxs-lookup"><span data-stu-id="c0fbd-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="c0fbd-208">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="c0fbd-209">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="c0fbd-210">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-210">Click Add.</span></span>
86. <span data-ttu-id="c0fbd-211">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="c0fbd-212">Selecteer Nettoboekwaarde in het veld Waarde boeken.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="c0fbd-213">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="c0fbd-214">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="c0fbd-214">In the Offset account field, specify the desired values.</span></span>


