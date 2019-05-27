---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 2: Berekeningen configureren)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ef657b13bc1f7f4a84676821e4175ace32c069a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551294"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a><span data-ttu-id="7a5e6-103">ER Indeling configureren voor tellen en totaliseren (deel 2: Berekeningen configureren)</span><span class="sxs-lookup"><span data-stu-id="7a5e6-103">ER Configure format to do counting and summing (Part 2: Configure computations)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a5e6-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="7a5e6-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="7a5e6-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 1: Indeling maken)".</span><span class="sxs-lookup"><span data-stu-id="7a5e6-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="7a5e6-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="7a5e6-108">Maak een indelingsconfiguratie om tellen en totaliseren van details toe te voegen</span><span class="sxs-lookup"><span data-stu-id="7a5e6-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="7a5e6-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7a5e6-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7a5e6-111">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="7a5e6-112">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="7a5e6-113">Stel dat u de indeling moet aanpassen die door Microsoft wordt geleverd door regels met overzichtdetails toe te voegen aan het einde van het Intrastat-rapport.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="7a5e6-114">U moet dat doen door een eigen exemplaar van de Intrastat-configuratie af te leiden uit het Microsoft-exemplaar om wijzigingen aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="7a5e6-115">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="7a5e6-116">Typ in het veld Nieuw 'Afleiden van naam: Intrastat (DE), Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="7a5e6-117">Typ 'Intrastat (DE) met tellen en totaliseren' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="7a5e6-118">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="7a5e6-119">Configureer dit rapport om tellen en totaliseren uit te voeren op basis van uitvoerdetails</span><span class="sxs-lookup"><span data-stu-id="7a5e6-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="7a5e6-120">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-120">Click Designer.</span></span>
2. <span data-ttu-id="7a5e6-121">Selecteer Ja in de veld Uitvoerdetails verzamelen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="7a5e6-122">Deze markering activeert in runtime het proces van het verzamelen van uitvoerdetails voor het genereren van het Intrastat-bestand.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="7a5e6-123">U moet tellen voor verschillende Intrastat-richtingen, dus voeg een specifieke modelopsomming toe aan de lijst met gegevensbronnen van deze indelingsconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="7a5e6-124">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="7a5e6-125">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="7a5e6-126">Selecteer in de structuur Gegevensmodel\Opsomming.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="7a5e6-127">Typ Richting in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="7a5e6-128">Typ of selecteer een waarde in het veld Modelopsomming.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="7a5e6-129">Selecteer de waarde Richting.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="7a5e6-130">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-130">Click OK.</span></span>
9. <span data-ttu-id="7a5e6-131">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="7a5e6-132">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="7a5e6-133">Typ '$BlockName' in het veld Naam</span><span class="sxs-lookup"><span data-stu-id="7a5e6-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="7a5e6-134">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-134">Click Edit formula.</span></span>
13. <span data-ttu-id="7a5e6-135">Typ 'blok' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="7a5e6-136">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-136">Click Save.</span></span>
15. <span data-ttu-id="7a5e6-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-137">Close the page.</span></span>
16. <span data-ttu-id="7a5e6-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-138">Click OK.</span></span>
17. <span data-ttu-id="7a5e6-139">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="7a5e6-140">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="7a5e6-141">Typ '$RecName' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="7a5e6-142">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-142">Click Edit formula.</span></span>
21. <span data-ttu-id="7a5e6-143">Typ 'record' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="7a5e6-144">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-144">Click Save.</span></span>
23. <span data-ttu-id="7a5e6-145">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-145">Close the page.</span></span>
24. <span data-ttu-id="7a5e6-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-146">Click OK.</span></span>
25. <span data-ttu-id="7a5e6-147">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="7a5e6-148">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="7a5e6-149">Typ '$InvName' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="7a5e6-150">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-150">Click Edit formula.</span></span>
29. <span data-ttu-id="7a5e6-151">Typ 'InvoicedAmountEUR' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="7a5e6-152">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-152">Click Save.</span></span>
31. <span data-ttu-id="7a5e6-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-153">Close the page.</span></span>
32. <span data-ttu-id="7a5e6-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-154">Click OK.</span></span>
33. <span data-ttu-id="7a5e6-155">Selecteer Intrastat\Gegevens in de structuur.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="7a5e6-156">Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens</span><span class="sxs-lookup"><span data-stu-id="7a5e6-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="7a5e6-157">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-157">Click Add data source.</span></span>
    * <span data-ttu-id="7a5e6-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="7a5e6-158">$BlockName</span></span>  
36. <span data-ttu-id="7a5e6-159">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-159">Click Save.</span></span>
37. <span data-ttu-id="7a5e6-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-160">Close the page.</span></span>
38. <span data-ttu-id="7a5e6-161">Klik op de knop Bewerken voor het veld Sleutelwaarde verzamelde gegevens</span><span class="sxs-lookup"><span data-stu-id="7a5e6-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="7a5e6-162">Typ in het veld Formule 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="7a5e6-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="7a5e6-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="7a5e6-164">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-164">Click Save.</span></span>
41. <span data-ttu-id="7a5e6-165">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-165">Close the page.</span></span>
    * <span data-ttu-id="7a5e6-166">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-166">Count the lines of this sequence.</span></span> <span data-ttu-id="7a5e6-167">De resultaten worden afzonderlijk voor verschillende richtingen gebruikt met de naam 'blok'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="7a5e6-168">De waarde Importeren wordt gebruikt voor Intrastat-transacties voor ontvangsten.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="7a5e6-169">De waarde Exporteren wordt gebruikt voor Intrastat-transacties voor verzendingen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="7a5e6-170">Beschouw dit als een virtueel Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="7a5e6-171">Voor elke transactie een rij waarin de eerste kolom 'blok' is ingevuld met de waarden 'Import' en 'Export'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="7a5e6-172">Vouw in de structuur 'Intrastat\Gegevens: Reeks' uit.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="7a5e6-173">Selecteer in de structuur 'Intrastat\Gegevens: Reeks\Ontvangsten?'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="7a5e6-174">Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="7a5e6-175">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-175">Count the lines of this sequence.</span></span> <span data-ttu-id="7a5e6-176">De resultaten worden onthouden met de naam 'record'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="7a5e6-177">Selecteer in de structuur '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="7a5e6-178">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-178">Click Add data source.</span></span>
47. <span data-ttu-id="7a5e6-179">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-179">Click Save.</span></span>
48. <span data-ttu-id="7a5e6-180">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-180">Close the page.</span></span>
49. <span data-ttu-id="7a5e6-181">Klik op de knop Bewerken voor het veld Sleutelwaarde verzamelde gegevens.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="7a5e6-182">Typ in het veld Formule 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="7a5e6-183">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-183">Click Save.</span></span>
52. <span data-ttu-id="7a5e6-184">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-184">Close the page.</span></span>
    * <span data-ttu-id="7a5e6-185">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-185">Count the lines of this sequence.</span></span> <span data-ttu-id="7a5e6-186">De resultaten worden afzonderlijk voor verschillende basisproductcode gebruikt met de naam 'record'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="7a5e6-187">Beschouw dit als een virtueel Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="7a5e6-188">Voor elke transactie een rij waarin de eerste kolom 'blok' wordt gevuld met de waarden 'Import' en 'Export' en het tweede blok 'record' wordt gevuld met de waarde van de basisproductcode.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="7a5e6-189">Select in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen?'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="7a5e6-190">Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens</span><span class="sxs-lookup"><span data-stu-id="7a5e6-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="7a5e6-191">Selecteer in de structuur '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="7a5e6-192">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-192">Click Add data source.</span></span>
57. <span data-ttu-id="7a5e6-193">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-193">Click Save.</span></span>
58. <span data-ttu-id="7a5e6-194">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-194">Close the page.</span></span>
59. <span data-ttu-id="7a5e6-195">Klik op de knop Bewerken voor het veld Sleutelwaarde verzamelde gegevens.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="7a5e6-196">Typ in het veld Formule 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="7a5e6-197">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-197">Click Save.</span></span>
62. <span data-ttu-id="7a5e6-198">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-198">Close the page.</span></span>
63. <span data-ttu-id="7a5e6-199">Vouw in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen: Reeks' uit.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="7a5e6-200">Vouw in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen: Reeks?\Record =  Intrastat.CommodityRecord' uit.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="7a5e6-201">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-201">Click the Format tab.</span></span>
66. <span data-ttu-id="7a5e6-202">Selecteer in de structuur 'Intrastat\Gegevens\Verzendingen\Record\Factuurbedrag EUR'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="7a5e6-203">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="7a5e6-204">Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="7a5e6-205">Selecteer in de structuur '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="7a5e6-206">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-206">Click Add data source.</span></span>
71. <span data-ttu-id="7a5e6-207">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-207">Click Save.</span></span>
72. <span data-ttu-id="7a5e6-208">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-208">Close the page.</span></span>
    * <span data-ttu-id="7a5e6-209">Vat de gefactureerde bedragwaarden samen voor regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="7a5e6-210">De resultaten worden afzonderlijk voor verschillende intrastat-richtingen en basisproductcodes gebruikt met de naam "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="7a5e6-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="7a5e6-211">Beschouw dit als een virtueel gemaakt item in het Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="7a5e6-212">Voor elke transactie een rij waarin de eerste kolom 'blok' is ingevuld met de waarden 'Import' en 'Export'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="7a5e6-213">Het tweede blok 'record' wordt gevuld met de waarde van de basisproductcode, en de derde kolom InvoicedAmountEUR wordt gevuld met de factuurbedragwaarde.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="7a5e6-214">Vouw in de structuur 'Intrastat\Gegevens\Ontvangsten?' uit.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="7a5e6-215">Vouw in de structuur 'Intrastat\Gegevens\Ontvangsten?\Record = Intrastat.CommodityRecord' uit.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="7a5e6-216">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-216">Click the Format tab.</span></span>
76. <span data-ttu-id="7a5e6-217">Selecteer in de structuur 'Intrastat\Gegevens\Ontvangsten\Record\Factuurbedrag EUR'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="7a5e6-218">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="7a5e6-219">Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="7a5e6-220">Selecteer in de structuur '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="7a5e6-221">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-221">Click Add data source.</span></span>
81. <span data-ttu-id="7a5e6-222">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-222">Click Save.</span></span>
82. <span data-ttu-id="7a5e6-223">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-223">Close the page.</span></span>
83. <span data-ttu-id="7a5e6-224">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-224">Click Save.</span></span>
84. <span data-ttu-id="7a5e6-225">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7a5e6-225">Close the page.</span></span>

