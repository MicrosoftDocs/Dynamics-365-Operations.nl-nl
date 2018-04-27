--- 
title: Berekeningen gebruiken voor het maken van de uitvoer voor tellen en totaliseren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5b7f0cc5b94ab7be11a013ef3e5909d84847e885
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing"></a><span data-ttu-id="0afdd-103">Berekeningen gebruiken voor het maken van de uitvoer voor tellen en totaliseren</span><span class="sxs-lookup"><span data-stu-id="0afdd-103">Use computations to make the output for counting and summing</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0afdd-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="0afdd-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="0afdd-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0afdd-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0afdd-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 2: Berekeningen configureren)".</span><span class="sxs-lookup"><span data-stu-id="0afdd-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="0afdd-107">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="0afdd-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="0afdd-108">Configureer dit rapport om tellings- en totaliseringsgegevens te gebruiken</span><span class="sxs-lookup"><span data-stu-id="0afdd-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="0afdd-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="0afdd-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0afdd-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="0afdd-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0afdd-111">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="0afdd-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="0afdd-112">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="0afdd-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="0afdd-113">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="0afdd-114">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="0afdd-114">Click Designer.</span></span>
7. <span data-ttu-id="0afdd-115">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="0afdd-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="0afdd-116">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="0afdd-117">Voeg een nieuwe gegevensbron toe om de lijst van onthouden blokken op te halen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="0afdd-118">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="0afdd-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="0afdd-119">Typ '$BlocksList' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="0afdd-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="0afdd-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="0afdd-120">$BlocksList</span></span>  
11. <span data-ttu-id="0afdd-121">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="0afdd-121">Click Edit formula.</span></span>
12. <span data-ttu-id="0afdd-122">Selecteer in de structuur 'Gegevenscollectiefuncties\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="0afdd-123">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-123">Click Add function.</span></span>
14. <span data-ttu-id="0afdd-124">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-124">Click Add data source.</span></span>
15. <span data-ttu-id="0afdd-125">Typ in het veld Formule 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="0afdd-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="0afdd-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="0afdd-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="0afdd-127">Typ in het veld Formule 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="0afdd-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="0afdd-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="0afdd-129">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0afdd-129">Click Save.</span></span>
    * <span data-ttu-id="0afdd-130">Het patroon "\*" betekent dat alle blokken in de lijst voor dit record worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="0afdd-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0afdd-131">Close the page.</span></span>
19. <span data-ttu-id="0afdd-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0afdd-132">Click OK.</span></span>
20. <span data-ttu-id="0afdd-133">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="0afdd-133">Click the Format tab.</span></span>
21. <span data-ttu-id="0afdd-134">Selecteer Intrastat\Gegevens in de structuur.</span><span class="sxs-lookup"><span data-stu-id="0afdd-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="0afdd-135">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="0afdd-136">Selecteer in de structuur 'Tekst\Reeks'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="0afdd-137">Typ 'Totalen per blokken' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="0afdd-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="0afdd-138">Totalen per blokken</span><span class="sxs-lookup"><span data-stu-id="0afdd-138">Totals by blocks</span></span>  
25. <span data-ttu-id="0afdd-139">Selecteer in het veld Speciale tekens 'Nieuwe regel - Windows (CR LF)'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="0afdd-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0afdd-140">Click OK.</span></span>
27. <span data-ttu-id="0afdd-141">Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="0afdd-142">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="0afdd-143">Selecteer "Text\String" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="0afdd-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="0afdd-144">Typ Blokcode in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="0afdd-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="0afdd-145">Blokcode</span><span class="sxs-lookup"><span data-stu-id="0afdd-145">Block code</span></span>  
31. <span data-ttu-id="0afdd-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0afdd-146">Click OK.</span></span>
32. <span data-ttu-id="0afdd-147">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-147">Click Add String.</span></span>
33. <span data-ttu-id="0afdd-148">Typ Regels tellen in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="0afdd-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="0afdd-149">Regels tellen</span><span class="sxs-lookup"><span data-stu-id="0afdd-149">Lines counting</span></span>  
34. <span data-ttu-id="0afdd-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0afdd-150">Click OK.</span></span>
35. <span data-ttu-id="0afdd-151">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-151">Click Add String.</span></span>
36. <span data-ttu-id="0afdd-152">Typ Totaalbedrag in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="0afdd-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="0afdd-153">Totaalbedrag</span><span class="sxs-lookup"><span data-stu-id="0afdd-153">Total amount</span></span>  
37. <span data-ttu-id="0afdd-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0afdd-154">Click OK.</span></span>
38. <span data-ttu-id="0afdd-155">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="0afdd-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="0afdd-156">Selecteer in de structuur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="0afdd-157">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="0afdd-157">Click Bind.</span></span>
    * <span data-ttu-id="0afdd-158">Maak een overzichtsregel voor elk onthouden blok.</span><span class="sxs-lookup"><span data-stu-id="0afdd-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="0afdd-159">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="0afdd-159">Click the Format tab.</span></span>
42. <span data-ttu-id="0afdd-160">Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Blokcode'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="0afdd-161">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="0afdd-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="0afdd-162">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="0afdd-162">Click Edit formula.</span></span>
45. <span data-ttu-id="0afdd-163">Typ in het veld Formule '"Blok-id: " & '.</span><span class="sxs-lookup"><span data-stu-id="0afdd-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="0afdd-164">"Blok-id: " &</span><span class="sxs-lookup"><span data-stu-id="0afdd-164">"Block id: " &</span></span>  
46. <span data-ttu-id="0afdd-165">Vouw in de structuur '$BlocksList' uit.</span><span class="sxs-lookup"><span data-stu-id="0afdd-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="0afdd-166">Selecteer in de structuur '$BlocksList\Waarde'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="0afdd-167">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-167">Click Add data source.</span></span>
49. <span data-ttu-id="0afdd-168">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0afdd-168">Click Save.</span></span>
50. <span data-ttu-id="0afdd-169">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0afdd-169">Close the page.</span></span>
51. <span data-ttu-id="0afdd-170">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="0afdd-170">Click the Format tab.</span></span>
52. <span data-ttu-id="0afdd-171">Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Regels tellen'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="0afdd-172">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="0afdd-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="0afdd-173">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="0afdd-173">Click Edit formula.</span></span>
    * <span data-ttu-id="0afdd-174">Maak uitvoer voor het aantal regels voor elk blok dat in dit rapport wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0afdd-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="0afdd-175">Typ in het Formuleveld '"Aantal regels in dit blok: " & '.</span><span class="sxs-lookup"><span data-stu-id="0afdd-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="0afdd-176">"Aantal regels in dit blok: " &</span><span class="sxs-lookup"><span data-stu-id="0afdd-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="0afdd-177">Typ in het Formuleveld '"Aantal regels in dit blok: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="0afdd-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="0afdd-178">"Aantal regels in dit blok: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="0afdd-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="0afdd-179">Selecteer in de structuur 'Gegevenscollectiefuncties\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="0afdd-180">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-180">Click Add function.</span></span>
59. <span data-ttu-id="0afdd-181">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-181">Click Add data source.</span></span>
60. <span data-ttu-id="0afdd-182">Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="0afdd-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="0afdd-183">"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="0afdd-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="0afdd-184">Vouw in de structuur '$BlocksList' uit.</span><span class="sxs-lookup"><span data-stu-id="0afdd-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="0afdd-185">Selecteer in de structuur '$BlocksList\Waarde'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="0afdd-186">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-186">Click Add data source.</span></span>
64. <span data-ttu-id="0afdd-187">Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', , '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="0afdd-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="0afdd-188">"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="0afdd-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="0afdd-189">Selecteer in de structuur '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="0afdd-190">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0afdd-190">Click Add data source.</span></span>
67. <span data-ttu-id="0afdd-191">Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', , '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="0afdd-192">"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="0afdd-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="0afdd-193">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0afdd-193">Click Save.</span></span>
69. <span data-ttu-id="0afdd-194">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0afdd-194">Close the page.</span></span>
70. <span data-ttu-id="0afdd-195">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="0afdd-195">Click the Format tab.</span></span>
71. <span data-ttu-id="0afdd-196">Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Totaalbedrag'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="0afdd-197">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="0afdd-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="0afdd-198">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="0afdd-198">Click Edit formula.</span></span>
    * <span data-ttu-id="0afdd-199">Maak uitvoer die het totaal is van het gefactureerde bedrag voor elk blok dat in dit rapport wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0afdd-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="0afdd-200">Typ in het veld Formule '"Totaal factuurbedrag: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="0afdd-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="0afdd-201">"Totaal factuurbedrag: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="0afdd-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="0afdd-202">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0afdd-202">Click Save.</span></span>
76. <span data-ttu-id="0afdd-203">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0afdd-203">Close the page.</span></span>
77. <span data-ttu-id="0afdd-204">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0afdd-204">Click Save.</span></span>
78. <span data-ttu-id="0afdd-205">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0afdd-205">Close the page.</span></span>


