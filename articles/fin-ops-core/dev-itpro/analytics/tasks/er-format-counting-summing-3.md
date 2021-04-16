---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 3: Berekeningen gebruiken om de uitvoer te maken)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage configureert voor tellen en totaliseren op basis van de gegevens van de reeds gegenereerde tekstuitvoer. (Deel 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7073539ed4c1d9d5acbb0ca84b43538d87fc8b4b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748992"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="becda-104">ER Indeling configureren voor tellen en totaliseren (deel 3: Berekeningen gebruiken om de uitvoer te maken)</span><span class="sxs-lookup"><span data-stu-id="becda-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="becda-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="becda-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="becda-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="becda-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="becda-107">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 2: Berekeningen configureren)".</span><span class="sxs-lookup"><span data-stu-id="becda-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="becda-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="becda-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="becda-109">Configureer dit rapport om tellings- en totaliseringsgegevens te gebruiken</span><span class="sxs-lookup"><span data-stu-id="becda-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="becda-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="becda-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="becda-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="becda-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="becda-112">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="becda-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="becda-113">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="becda-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="becda-114">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="becda-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="becda-115">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="becda-115">Click Designer.</span></span>
7. <span data-ttu-id="becda-116">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="becda-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="becda-117">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="becda-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="becda-118">Voeg een nieuwe gegevensbron toe om de lijst van onthouden blokken op te halen.</span><span class="sxs-lookup"><span data-stu-id="becda-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="becda-119">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="becda-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="becda-120">Typ '$BlocksList' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="becda-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="becda-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="becda-121">$BlocksList</span></span>  
11. <span data-ttu-id="becda-122">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="becda-122">Click Edit formula.</span></span>
12. <span data-ttu-id="becda-123">Selecteer in de structuur 'Gegevenscollectiefuncties\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="becda-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="becda-124">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-124">Click Add function.</span></span>
14. <span data-ttu-id="becda-125">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-125">Click Add data source.</span></span>
15. <span data-ttu-id="becda-126">Typ in het veld Formule 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="becda-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="becda-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="becda-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="becda-128">Typ in het veld Formule 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="becda-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="becda-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="becda-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="becda-130">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="becda-130">Click Save.</span></span>
    * <span data-ttu-id="becda-131">Het patroon "\*" betekent dat alle blokken in de lijst voor dit record worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="becda-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="becda-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="becda-132">Close the page.</span></span>
19. <span data-ttu-id="becda-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="becda-133">Click OK.</span></span>
20. <span data-ttu-id="becda-134">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="becda-134">Click the Format tab.</span></span>
21. <span data-ttu-id="becda-135">Selecteer Intrastat\Gegevens in de structuur.</span><span class="sxs-lookup"><span data-stu-id="becda-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="becda-136">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="becda-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="becda-137">Selecteer in de structuur 'Tekst\Reeks'.</span><span class="sxs-lookup"><span data-stu-id="becda-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="becda-138">Typ 'Totalen per blokken' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="becda-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="becda-139">Totalen per blokken</span><span class="sxs-lookup"><span data-stu-id="becda-139">Totals by blocks</span></span>  
25. <span data-ttu-id="becda-140">Selecteer in het veld Speciale tekens 'Nieuwe regel - Windows (CR LF)'.</span><span class="sxs-lookup"><span data-stu-id="becda-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="becda-141">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="becda-141">Click OK.</span></span>
27. <span data-ttu-id="becda-142">Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken'.</span><span class="sxs-lookup"><span data-stu-id="becda-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="becda-143">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="becda-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="becda-144">Selecteer "Text\String" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="becda-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="becda-145">Typ Blokcode in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="becda-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="becda-146">Blokcode</span><span class="sxs-lookup"><span data-stu-id="becda-146">Block code</span></span>  
31. <span data-ttu-id="becda-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="becda-147">Click OK.</span></span>
32. <span data-ttu-id="becda-148">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-148">Click Add String.</span></span>
33. <span data-ttu-id="becda-149">Typ Regels tellen in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="becda-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="becda-150">Regels tellen</span><span class="sxs-lookup"><span data-stu-id="becda-150">Lines counting</span></span>  
34. <span data-ttu-id="becda-151">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="becda-151">Click OK.</span></span>
35. <span data-ttu-id="becda-152">Klik Tekenreeks toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-152">Click Add String.</span></span>
36. <span data-ttu-id="becda-153">Typ Totaalbedrag in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="becda-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="becda-154">Totaalbedrag</span><span class="sxs-lookup"><span data-stu-id="becda-154">Total amount</span></span>  
37. <span data-ttu-id="becda-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="becda-155">Click OK.</span></span>
38. <span data-ttu-id="becda-156">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="becda-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="becda-157">Selecteer in de structuur '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="becda-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="becda-158">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="becda-158">Click Bind.</span></span>
    * <span data-ttu-id="becda-159">Maak een overzichtsregel voor elk onthouden blok.</span><span class="sxs-lookup"><span data-stu-id="becda-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="becda-160">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="becda-160">Click the Format tab.</span></span>
42. <span data-ttu-id="becda-161">Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Blokcode'.</span><span class="sxs-lookup"><span data-stu-id="becda-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="becda-162">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="becda-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="becda-163">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="becda-163">Click Edit formula.</span></span>
45. <span data-ttu-id="becda-164">Typ in het veld Formule '"Blok-id: " & '.</span><span class="sxs-lookup"><span data-stu-id="becda-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="becda-165">"Blok-id: " &</span><span class="sxs-lookup"><span data-stu-id="becda-165">"Block id: " &</span></span>  
46. <span data-ttu-id="becda-166">Vouw in de structuur '$BlocksList' uit.</span><span class="sxs-lookup"><span data-stu-id="becda-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="becda-167">Selecteer in de structuur '$BlocksList\Waarde'.</span><span class="sxs-lookup"><span data-stu-id="becda-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="becda-168">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-168">Click Add data source.</span></span>
49. <span data-ttu-id="becda-169">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="becda-169">Click Save.</span></span>
50. <span data-ttu-id="becda-170">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="becda-170">Close the page.</span></span>
51. <span data-ttu-id="becda-171">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="becda-171">Click the Format tab.</span></span>
52. <span data-ttu-id="becda-172">Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Regels tellen'.</span><span class="sxs-lookup"><span data-stu-id="becda-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="becda-173">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="becda-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="becda-174">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="becda-174">Click Edit formula.</span></span>
    * <span data-ttu-id="becda-175">Maak uitvoer voor het aantal regels voor elk blok dat in dit rapport wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="becda-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="becda-176">Typ in het Formuleveld '"Aantal regels in dit blok: " & '.</span><span class="sxs-lookup"><span data-stu-id="becda-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="becda-177">"Aantal regels in dit blok: " &</span><span class="sxs-lookup"><span data-stu-id="becda-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="becda-178">Typ in het Formuleveld '"Aantal regels in dit blok: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="becda-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="becda-179">"Aantal regels in dit blok: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="becda-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="becda-180">Selecteer in de structuur 'Gegevenscollectiefuncties\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="becda-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="becda-181">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-181">Click Add function.</span></span>
59. <span data-ttu-id="becda-182">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-182">Click Add data source.</span></span>
60. <span data-ttu-id="becda-183">Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="becda-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="becda-184">"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="becda-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="becda-185">Vouw in de structuur '$BlocksList' uit.</span><span class="sxs-lookup"><span data-stu-id="becda-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="becda-186">Selecteer in de structuur '$BlocksList\Waarde'.</span><span class="sxs-lookup"><span data-stu-id="becda-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="becda-187">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-187">Click Add data source.</span></span>
64. <span data-ttu-id="becda-188">Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', , '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="becda-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="becda-189">"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="becda-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="becda-190">Selecteer in de structuur '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="becda-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="becda-191">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="becda-191">Click Add data source.</span></span>
67. <span data-ttu-id="becda-192">Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', , '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="becda-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="becda-193">"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="becda-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="becda-194">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="becda-194">Click Save.</span></span>
69. <span data-ttu-id="becda-195">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="becda-195">Close the page.</span></span>
70. <span data-ttu-id="becda-196">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="becda-196">Click the Format tab.</span></span>
71. <span data-ttu-id="becda-197">Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Totaalbedrag'.</span><span class="sxs-lookup"><span data-stu-id="becda-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="becda-198">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="becda-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="becda-199">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="becda-199">Click Edit formula.</span></span>
    * <span data-ttu-id="becda-200">Maak uitvoer die het totaal is van het gefactureerde bedrag voor elk blok dat in dit rapport wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="becda-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="becda-201">Typ in het veld Formule '"Totaal factuurbedrag: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="becda-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="becda-202">"Totaal factuurbedrag: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="becda-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="becda-203">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="becda-203">Click Save.</span></span>
76. <span data-ttu-id="becda-204">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="becda-204">Close the page.</span></span>
77. <span data-ttu-id="becda-205">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="becda-205">Click Save.</span></span>
78. <span data-ttu-id="becda-206">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="becda-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]