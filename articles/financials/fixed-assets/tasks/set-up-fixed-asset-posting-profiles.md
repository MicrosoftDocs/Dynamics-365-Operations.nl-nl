---
title: Boekingsprofielen voor vaste activa instellen
description: Deze taakbegeleiding stelt boekingsprofielen voor vaste activa in.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 286c8732c1f2c92d0f16582b0b9de41990280e5a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554777"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="d71ce-103">Boekingsprofielen voor vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="d71ce-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d71ce-104">Deze taakbegeleiding stelt boekingsprofielen voor vaste activa in.</span><span class="sxs-lookup"><span data-stu-id="d71ce-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="d71ce-105">Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d71ce-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="d71ce-106">De voorbeelden in de taakbegeleiding zijn voor een basisboekingsprofiel, hoewel de boekingsprofielen voor uw specifieke rekeningschema en financiële rapportagebehoeften moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d71ce-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="d71ce-107">Ga naar Vaste activa > Instellingen > Boekingsprofielen voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="d71ce-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="d71ce-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d71ce-108">Click New.</span></span>
3. <span data-ttu-id="d71ce-109">Typ een waarde in het veld Boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="d71ce-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="d71ce-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="d71ce-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d71ce-111">U moet een boekingsprofiel maken voor elk type vaste-activatransactie dat u gebruikt bij het werken met vaste activa.</span><span class="sxs-lookup"><span data-stu-id="d71ce-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="d71ce-112">Deze taakbegeleiding start met het type Bijboekingstransactie.</span><span class="sxs-lookup"><span data-stu-id="d71ce-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="d71ce-113">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-113">Click Add.</span></span>
6. <span data-ttu-id="d71ce-114">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d71ce-115">Met het veld Groeperingen kunt u het boekingsprofiel definiëren tot de Tabel (één rekening ingesteld voor elk vast activum) of Groep (één rekening ingesteld voor elke vaste-activagroep).</span><span class="sxs-lookup"><span data-stu-id="d71ce-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="d71ce-116">Voor deze taakbegeleiding blijft de waarde op "Alle" ingesteld voor toepassing op alle vaste activa met het opgegeven boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="d71ce-117">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d71ce-118">Voor bijboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.</span><span class="sxs-lookup"><span data-stu-id="d71ce-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="d71ce-119">Selecteer in het veld Transactietype de optie Verwervingscorrectie.</span><span class="sxs-lookup"><span data-stu-id="d71ce-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="d71ce-120">Voor bijboekingscorrectietransacties worden dezelfde rekeningen als voor bijboekingstransacties gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d71ce-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="d71ce-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-121">Click Add.</span></span>
10. <span data-ttu-id="d71ce-122">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="d71ce-123">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d71ce-124">Voor bijboekingscorrecties kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.</span><span class="sxs-lookup"><span data-stu-id="d71ce-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="d71ce-125">Selecteer Afschrijving in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="d71ce-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="d71ce-126">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-126">Click Add.</span></span>
14. <span data-ttu-id="d71ce-127">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="d71ce-128">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="d71ce-129">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="d71ce-130">Selecteer Afschrijvingscorrectie in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="d71ce-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="d71ce-131">Voor afschrijvingscorrectietransacties worden dezelfde rekeningen als voor afschrijvingstransacties gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d71ce-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="d71ce-132">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-132">Click Add.</span></span>
19. <span data-ttu-id="d71ce-133">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="d71ce-134">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="d71ce-135">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="d71ce-136">Selecteer Verkoop/afstoting in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="d71ce-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="d71ce-137">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-137">Click Add.</span></span>
24. <span data-ttu-id="d71ce-138">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="d71ce-139">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d71ce-140">Voor afboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.</span><span class="sxs-lookup"><span data-stu-id="d71ce-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="d71ce-141">Selecteer Afstoting - uitval in het veld Transactietype.</span><span class="sxs-lookup"><span data-stu-id="d71ce-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="d71ce-142">We gebruiken dezelfde rekeningen voor Afstotingsverkoop en Afstotingsuitval.</span><span class="sxs-lookup"><span data-stu-id="d71ce-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="d71ce-143">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-143">Click Add.</span></span>
28. <span data-ttu-id="d71ce-144">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="d71ce-145">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d71ce-146">Voor afboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.</span><span class="sxs-lookup"><span data-stu-id="d71ce-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="d71ce-147">Vouw de sectie Afstoting uit.</span><span class="sxs-lookup"><span data-stu-id="d71ce-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="d71ce-148">U moet boekingsprofielen voor afboeking voor zowel verkoop als uitval instellen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="d71ce-149">Wij zullen met de transacties van de afboekingsverkoop starten.</span><span class="sxs-lookup"><span data-stu-id="d71ce-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="d71ce-150">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-150">Click Add.</span></span>
32. <span data-ttu-id="d71ce-151">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="d71ce-152">Selecteer Aanschafwaarde in het veld Waarde boeken.</span><span class="sxs-lookup"><span data-stu-id="d71ce-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="d71ce-153">De bijboekingswaarde geldt voor bijboekings- en bijboekingscorrectiewaarden voor alle jaren.</span><span class="sxs-lookup"><span data-stu-id="d71ce-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="d71ce-154">U kunt ook rekeningen voor deze transactietypen afzonderlijk definiëren.</span><span class="sxs-lookup"><span data-stu-id="d71ce-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="d71ce-155">U kunt het afboekingsproces instellen om verschillende rekeningen te gebruiken die afhankelijk zijn van of de afboeking in winst of een verlies resulteert.</span><span class="sxs-lookup"><span data-stu-id="d71ce-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="d71ce-156">Ik stel het type verkoopwaarde in op Alle om dezelfde rekeningen voor alle typen afboekingen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d71ce-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="d71ce-157">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="d71ce-158">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="d71ce-159">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-159">Click Add.</span></span>
37. <span data-ttu-id="d71ce-160">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d71ce-161">Selecteer in het veld Waarde boeken de optie Afschrijving (voorgaande jaren).</span><span class="sxs-lookup"><span data-stu-id="d71ce-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="d71ce-162">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="d71ce-163">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="d71ce-164">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-164">Click Add.</span></span>
41. <span data-ttu-id="d71ce-165">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="d71ce-166">Selecteer in het veld Waarde boeken de optie Afschrijving (dit jaar).</span><span class="sxs-lookup"><span data-stu-id="d71ce-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="d71ce-167">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="d71ce-168">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="d71ce-169">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-169">Click Add.</span></span>
46. <span data-ttu-id="d71ce-170">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="d71ce-171">Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (voorgaande jaren).</span><span class="sxs-lookup"><span data-stu-id="d71ce-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="d71ce-172">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="d71ce-173">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="d71ce-174">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-174">Click Add.</span></span>
51. <span data-ttu-id="d71ce-175">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="d71ce-176">Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (dit jaar).</span><span class="sxs-lookup"><span data-stu-id="d71ce-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="d71ce-177">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="d71ce-178">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="d71ce-179">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-179">Click Add.</span></span>
56. <span data-ttu-id="d71ce-180">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="d71ce-181">Selecteer Nettoboekwaarde in het veld Waarde boeken.</span><span class="sxs-lookup"><span data-stu-id="d71ce-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="d71ce-182">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="d71ce-183">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="d71ce-184">Selecteer Uitval in het veld Verkoop of uitval.</span><span class="sxs-lookup"><span data-stu-id="d71ce-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="d71ce-185">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-185">Click Add.</span></span>
62. <span data-ttu-id="d71ce-186">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="d71ce-187">Selecteer Aanschafwaarde in het veld Waarde boeken.</span><span class="sxs-lookup"><span data-stu-id="d71ce-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="d71ce-188">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="d71ce-189">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="d71ce-190">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-190">Click Add.</span></span>
67. <span data-ttu-id="d71ce-191">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d71ce-192">Selecteer in het veld Waarde boeken de optie Afschrijving (voorgaande jaren).</span><span class="sxs-lookup"><span data-stu-id="d71ce-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="d71ce-193">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="d71ce-194">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="d71ce-195">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-195">Click Add.</span></span>
71. <span data-ttu-id="d71ce-196">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="d71ce-197">Selecteer in het veld Waarde boeken de optie Afschrijving (dit jaar).</span><span class="sxs-lookup"><span data-stu-id="d71ce-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="d71ce-198">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="d71ce-199">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="d71ce-200">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-200">Click Add.</span></span>
76. <span data-ttu-id="d71ce-201">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="d71ce-202">Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (voorgaande jaren).</span><span class="sxs-lookup"><span data-stu-id="d71ce-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="d71ce-203">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="d71ce-204">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="d71ce-205">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-205">Click Add.</span></span>
81. <span data-ttu-id="d71ce-206">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="d71ce-207">Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (dit jaar).</span><span class="sxs-lookup"><span data-stu-id="d71ce-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="d71ce-208">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="d71ce-209">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="d71ce-210">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d71ce-210">Click Add.</span></span>
86. <span data-ttu-id="d71ce-211">Typ of selecteer een waarde in het veld Boek.</span><span class="sxs-lookup"><span data-stu-id="d71ce-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="d71ce-212">Selecteer Nettoboekwaarde in het veld Waarde boeken.</span><span class="sxs-lookup"><span data-stu-id="d71ce-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="d71ce-213">Geef in het veld Hoofdrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="d71ce-214">Geef in het veld Tegenrekening de gewenste waarden op.</span><span class="sxs-lookup"><span data-stu-id="d71ce-214">In the Offset account field, specify the desired values.</span></span>

