---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 2: Berekeningen configureren)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage configureert voor tellen en totaliseren op basis van de gegevens van de reeds gegenereerde tekstuitvoer. (Deel 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a14fe079515b176cbcda74852ae2ad456dd6434a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749016"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="5373f-104">ER Indeling configureren voor tellen en totaliseren (deel 2: Berekeningen configureren)</span><span class="sxs-lookup"><span data-stu-id="5373f-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5373f-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="5373f-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="5373f-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5373f-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="5373f-107">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 1: Indeling maken)".</span><span class="sxs-lookup"><span data-stu-id="5373f-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="5373f-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="5373f-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="5373f-109">Maak een indelingsconfiguratie om tellen en totaliseren van details toe te voegen</span><span class="sxs-lookup"><span data-stu-id="5373f-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="5373f-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="5373f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5373f-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="5373f-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5373f-112">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="5373f-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="5373f-113">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="5373f-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="5373f-114">Stel dat u de indeling moet aanpassen die door Microsoft wordt geleverd door regels met overzichtdetails toe te voegen aan het einde van het Intrastat-rapport.</span><span class="sxs-lookup"><span data-stu-id="5373f-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="5373f-115">U moet dat doen door een eigen exemplaar van de Intrastat-configuratie af te leiden uit het Microsoft-exemplaar om wijzigingen aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="5373f-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="5373f-116">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="5373f-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="5373f-117">Typ in het veld Nieuw 'Afleiden van naam: Intrastat (DE), Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="5373f-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="5373f-118">Typ 'Intrastat (DE) met tellen en totaliseren' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5373f-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="5373f-119">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="5373f-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="5373f-120">Configureer dit rapport om tellen en totaliseren uit te voeren op basis van uitvoerdetails</span><span class="sxs-lookup"><span data-stu-id="5373f-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="5373f-121">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="5373f-121">Click Designer.</span></span>
2. <span data-ttu-id="5373f-122">Selecteer Ja in de veld Uitvoerdetails verzamelen.</span><span class="sxs-lookup"><span data-stu-id="5373f-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="5373f-123">Deze markering activeert in runtime het proces van het verzamelen van uitvoerdetails voor het genereren van het Intrastat-bestand.</span><span class="sxs-lookup"><span data-stu-id="5373f-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="5373f-124">U moet tellen voor verschillende Intrastat-richtingen, dus voeg een specifieke modelopsomming toe aan de lijst met gegevensbronnen van deze indelingsconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="5373f-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="5373f-125">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="5373f-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="5373f-126">Klik op Basis toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="5373f-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="5373f-127">Selecteer in de structuur Gegevensmodel\Opsomming.</span><span class="sxs-lookup"><span data-stu-id="5373f-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="5373f-128">Typ Richting in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5373f-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="5373f-129">Typ of selecteer een waarde in het veld Modelopsomming.</span><span class="sxs-lookup"><span data-stu-id="5373f-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="5373f-130">Selecteer de waarde Richting.</span><span class="sxs-lookup"><span data-stu-id="5373f-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="5373f-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5373f-131">Click OK.</span></span>
9. <span data-ttu-id="5373f-132">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="5373f-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="5373f-133">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="5373f-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="5373f-134">Typ '$BlockName' in het veld Naam</span><span class="sxs-lookup"><span data-stu-id="5373f-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="5373f-135">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="5373f-135">Click Edit formula.</span></span>
13. <span data-ttu-id="5373f-136">Typ 'blok' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="5373f-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="5373f-137">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-137">Click Save.</span></span>
15. <span data-ttu-id="5373f-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-138">Close the page.</span></span>
16. <span data-ttu-id="5373f-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5373f-139">Click OK.</span></span>
17. <span data-ttu-id="5373f-140">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="5373f-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="5373f-141">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="5373f-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="5373f-142">Typ '$RecName' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5373f-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="5373f-143">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="5373f-143">Click Edit formula.</span></span>
21. <span data-ttu-id="5373f-144">Typ 'record' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="5373f-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="5373f-145">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-145">Click Save.</span></span>
23. <span data-ttu-id="5373f-146">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-146">Close the page.</span></span>
24. <span data-ttu-id="5373f-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5373f-147">Click OK.</span></span>
25. <span data-ttu-id="5373f-148">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="5373f-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="5373f-149">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="5373f-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="5373f-150">Typ '$InvName' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5373f-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="5373f-151">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="5373f-151">Click Edit formula.</span></span>
29. <span data-ttu-id="5373f-152">Typ 'InvoicedAmountEUR' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="5373f-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="5373f-153">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-153">Click Save.</span></span>
31. <span data-ttu-id="5373f-154">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-154">Close the page.</span></span>
32. <span data-ttu-id="5373f-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5373f-155">Click OK.</span></span>
33. <span data-ttu-id="5373f-156">Selecteer Intrastat\Gegevens in de structuur.</span><span class="sxs-lookup"><span data-stu-id="5373f-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="5373f-157">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'</span><span class="sxs-lookup"><span data-stu-id="5373f-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="5373f-158">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5373f-158">Click Add data source.</span></span>
    * <span data-ttu-id="5373f-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="5373f-159">$BlockName</span></span>  
36. <span data-ttu-id="5373f-160">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-160">Click Save.</span></span>
37. <span data-ttu-id="5373f-161">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-161">Close the page.</span></span>
38. <span data-ttu-id="5373f-162">Klik op de knop Bewerken voor het veld Sleutelwaarde verzamelde gegevens</span><span class="sxs-lookup"><span data-stu-id="5373f-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="5373f-163">Typ in het veld Formule 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span><span class="sxs-lookup"><span data-stu-id="5373f-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="5373f-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="5373f-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="5373f-165">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-165">Click Save.</span></span>
41. <span data-ttu-id="5373f-166">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-166">Close the page.</span></span>
    * <span data-ttu-id="5373f-167">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="5373f-167">Count the lines of this sequence.</span></span> <span data-ttu-id="5373f-168">De resultaten worden afzonderlijk voor verschillende richtingen gebruikt met de naam "blok".</span><span class="sxs-lookup"><span data-stu-id="5373f-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="5373f-169">De waarde "Importeren" wordt gebruikt voor Intrastat-transacties voor ontvangsten.</span><span class="sxs-lookup"><span data-stu-id="5373f-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="5373f-170">De waarde "Exporteren" wordt gebruikt voor Intrastat-transacties voor verzendingen.</span><span class="sxs-lookup"><span data-stu-id="5373f-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="5373f-171">Beschouw dit als een virtueel Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="5373f-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="5373f-172">Voor elke transactie een rij waarin de eerste kolom "blok" is ingevuld met de waarden "Import" en "Export".</span><span class="sxs-lookup"><span data-stu-id="5373f-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="5373f-173">Vouw in de structuur 'Intrastat\Gegevens: Reeks' uit.</span><span class="sxs-lookup"><span data-stu-id="5373f-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="5373f-174">Selecteer in de structuur 'Intrastat\Gegevens: Reeks\Ontvangsten?'.</span><span class="sxs-lookup"><span data-stu-id="5373f-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="5373f-175">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'.</span><span class="sxs-lookup"><span data-stu-id="5373f-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="5373f-176">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="5373f-176">Count the lines of this sequence.</span></span> <span data-ttu-id="5373f-177">De resultaten worden onthouden met de naam "record".</span><span class="sxs-lookup"><span data-stu-id="5373f-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="5373f-178">Selecteer in de structuur '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="5373f-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="5373f-179">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5373f-179">Click Add data source.</span></span>
47. <span data-ttu-id="5373f-180">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-180">Click Save.</span></span>
48. <span data-ttu-id="5373f-181">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-181">Close the page.</span></span>
49. <span data-ttu-id="5373f-182">Klik op de knop Bewerken voor het veld 'Sleutelwaarde verzamelde gegevens'</span><span class="sxs-lookup"><span data-stu-id="5373f-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="5373f-183">Typ in het veld Formule 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="5373f-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="5373f-184">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-184">Click Save.</span></span>
52. <span data-ttu-id="5373f-185">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-185">Close the page.</span></span>
    * <span data-ttu-id="5373f-186">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="5373f-186">Count the lines of this sequence.</span></span> <span data-ttu-id="5373f-187">De resultaten worden afzonderlijk voor verschillende basisproductcode gebruikt met de naam "record".</span><span class="sxs-lookup"><span data-stu-id="5373f-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="5373f-188">Beschouw dit als een virtueel Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="5373f-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="5373f-189">Voor elke transactie een rij waarin de eerste kolom "blok" wordt gevuld met de waarden "Import" en "Export" en het tweede blok "record" wordt gevuld met de waarde van de basisproductcode.</span><span class="sxs-lookup"><span data-stu-id="5373f-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="5373f-190">Select in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen?'.</span><span class="sxs-lookup"><span data-stu-id="5373f-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="5373f-191">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'</span><span class="sxs-lookup"><span data-stu-id="5373f-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="5373f-192">Selecteer in de structuur '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="5373f-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="5373f-193">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5373f-193">Click Add data source.</span></span>
57. <span data-ttu-id="5373f-194">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-194">Click Save.</span></span>
58. <span data-ttu-id="5373f-195">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-195">Close the page.</span></span>
59. <span data-ttu-id="5373f-196">Klik op de knop Bewerken voor het veld 'Sleutelwaarde verzamelde gegevens'.</span><span class="sxs-lookup"><span data-stu-id="5373f-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="5373f-197">Typ in het veld Formule 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="5373f-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="5373f-198">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-198">Click Save.</span></span>
62. <span data-ttu-id="5373f-199">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-199">Close the page.</span></span>
63. <span data-ttu-id="5373f-200">Vouw in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen: Reeks' uit.</span><span class="sxs-lookup"><span data-stu-id="5373f-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="5373f-201">Vouw in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen: Reeks?\Record =  Intrastat.CommodityRecord' uit.</span><span class="sxs-lookup"><span data-stu-id="5373f-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="5373f-202">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="5373f-202">Click the Format tab.</span></span>
66. <span data-ttu-id="5373f-203">Selecteer in de structuur 'Intrastat\Gegevens\Verzendingen\Record\Factuurbedrag EUR'.</span><span class="sxs-lookup"><span data-stu-id="5373f-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="5373f-204">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="5373f-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="5373f-205">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'.</span><span class="sxs-lookup"><span data-stu-id="5373f-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="5373f-206">Selecteer in de structuur '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="5373f-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="5373f-207">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5373f-207">Click Add data source.</span></span>
71. <span data-ttu-id="5373f-208">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-208">Click Save.</span></span>
72. <span data-ttu-id="5373f-209">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-209">Close the page.</span></span>
    * <span data-ttu-id="5373f-210">Vat de gefactureerde bedragwaarden samen voor regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="5373f-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="5373f-211">De resultaten worden afzonderlijk voor verschillende intrastat-richtingen en basisproductcodes gebruikt met de naam "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="5373f-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="5373f-212">Beschouw dit als een virtueel gemaakt item in het Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="5373f-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="5373f-213">Voor elke transactie een rij waarin de eerste kolom "blok" is ingevuld met de waarden "Import" en "Export".</span><span class="sxs-lookup"><span data-stu-id="5373f-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="5373f-214">Het tweede blok "record" wordt gevuld met de waarde van de basisproductcode, en de derde kolom "InvoicedAmountEUR" wordt gevuld met de factuurbedragwaarde.</span><span class="sxs-lookup"><span data-stu-id="5373f-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="5373f-215">Vouw in de structuur 'Intrastat\Gegevens\Ontvangsten?' uit.</span><span class="sxs-lookup"><span data-stu-id="5373f-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="5373f-216">Vouw in de structuur 'Intrastat\Gegevens\Ontvangsten?\Record = Intrastat.CommodityRecord' uit.</span><span class="sxs-lookup"><span data-stu-id="5373f-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="5373f-217">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="5373f-217">Click the Format tab.</span></span>
76. <span data-ttu-id="5373f-218">Selecteer in de structuur 'Intrastat\Gegevens\Ontvangsten\Record\Factuurbedrag EUR'.</span><span class="sxs-lookup"><span data-stu-id="5373f-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="5373f-219">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="5373f-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="5373f-220">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'.</span><span class="sxs-lookup"><span data-stu-id="5373f-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="5373f-221">Selecteer in de structuur '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="5373f-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="5373f-222">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5373f-222">Click Add data source.</span></span>
81. <span data-ttu-id="5373f-223">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-223">Click Save.</span></span>
82. <span data-ttu-id="5373f-224">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-224">Close the page.</span></span>
83. <span data-ttu-id="5373f-225">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5373f-225">Click Save.</span></span>
84. <span data-ttu-id="5373f-226">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5373f-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]