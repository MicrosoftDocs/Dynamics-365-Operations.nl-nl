---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 2: Berekeningen configureren)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage configureert voor tellen en totaliseren op basis van de gegevens van de reeds gegenereerde tekstuitvoer. (Deel 2)
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: d6eb3d686e8f60de51001deffb4c2460c181a4ab
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565160"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="610c3-104">ER Indeling configureren voor tellen en totaliseren (deel 2: Berekeningen configureren)</span><span class="sxs-lookup"><span data-stu-id="610c3-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="610c3-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="610c3-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="610c3-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="610c3-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="610c3-107">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 1: Indeling maken)".</span><span class="sxs-lookup"><span data-stu-id="610c3-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="610c3-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="610c3-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="610c3-109">Maak een indelingsconfiguratie om tellen en totaliseren van details toe te voegen</span><span class="sxs-lookup"><span data-stu-id="610c3-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="610c3-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="610c3-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="610c3-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="610c3-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="610c3-112">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="610c3-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="610c3-113">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="610c3-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="610c3-114">Stel dat u de indeling moet aanpassen die door Microsoft wordt geleverd door regels met overzichtdetails toe te voegen aan het einde van het Intrastat-rapport.</span><span class="sxs-lookup"><span data-stu-id="610c3-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="610c3-115">U moet dat doen door een eigen exemplaar van de Intrastat-configuratie af te leiden uit het Microsoft-exemplaar om wijzigingen aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="610c3-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="610c3-116">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="610c3-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="610c3-117">Typ in het veld Nieuw 'Afleiden van naam: Intrastat (DE), Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="610c3-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="610c3-118">Typ 'Intrastat (DE) met tellen en totaliseren' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="610c3-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="610c3-119">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="610c3-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="610c3-120">Configureer dit rapport om tellen en totaliseren uit te voeren op basis van uitvoerdetails</span><span class="sxs-lookup"><span data-stu-id="610c3-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="610c3-121">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="610c3-121">Click Designer.</span></span>
2. <span data-ttu-id="610c3-122">Selecteer Ja in de veld Uitvoerdetails verzamelen.</span><span class="sxs-lookup"><span data-stu-id="610c3-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="610c3-123">Deze markering activeert in runtime het proces van het verzamelen van uitvoerdetails voor het genereren van het Intrastat-bestand.</span><span class="sxs-lookup"><span data-stu-id="610c3-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="610c3-124">U moet tellen voor verschillende Intrastat-richtingen, dus voeg een specifieke modelopsomming toe aan de lijst met gegevensbronnen van deze indelingsconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="610c3-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="610c3-125">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="610c3-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="610c3-126">Klik op Basis toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="610c3-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="610c3-127">Selecteer in de structuur Gegevensmodel\Opsomming.</span><span class="sxs-lookup"><span data-stu-id="610c3-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="610c3-128">Typ Richting in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="610c3-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="610c3-129">Typ of selecteer een waarde in het veld Modelopsomming.</span><span class="sxs-lookup"><span data-stu-id="610c3-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="610c3-130">Selecteer de waarde Richting.</span><span class="sxs-lookup"><span data-stu-id="610c3-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="610c3-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="610c3-131">Click OK.</span></span>
9. <span data-ttu-id="610c3-132">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="610c3-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="610c3-133">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="610c3-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="610c3-134">Typ '$BlockName' in het veld Naam</span><span class="sxs-lookup"><span data-stu-id="610c3-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="610c3-135">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="610c3-135">Click Edit formula.</span></span>
13. <span data-ttu-id="610c3-136">Typ 'blok' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="610c3-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="610c3-137">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-137">Click Save.</span></span>
15. <span data-ttu-id="610c3-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-138">Close the page.</span></span>
16. <span data-ttu-id="610c3-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="610c3-139">Click OK.</span></span>
17. <span data-ttu-id="610c3-140">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="610c3-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="610c3-141">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="610c3-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="610c3-142">Typ '$RecName' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="610c3-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="610c3-143">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="610c3-143">Click Edit formula.</span></span>
21. <span data-ttu-id="610c3-144">Typ 'record' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="610c3-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="610c3-145">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-145">Click Save.</span></span>
23. <span data-ttu-id="610c3-146">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-146">Close the page.</span></span>
24. <span data-ttu-id="610c3-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="610c3-147">Click OK.</span></span>
25. <span data-ttu-id="610c3-148">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="610c3-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="610c3-149">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="610c3-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="610c3-150">Typ '$InvName' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="610c3-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="610c3-151">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="610c3-151">Click Edit formula.</span></span>
29. <span data-ttu-id="610c3-152">Typ 'InvoicedAmountEUR' in het veld Formule.</span><span class="sxs-lookup"><span data-stu-id="610c3-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="610c3-153">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-153">Click Save.</span></span>
31. <span data-ttu-id="610c3-154">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-154">Close the page.</span></span>
32. <span data-ttu-id="610c3-155">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="610c3-155">Click OK.</span></span>
33. <span data-ttu-id="610c3-156">Selecteer Intrastat\Gegevens in de structuur.</span><span class="sxs-lookup"><span data-stu-id="610c3-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="610c3-157">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'</span><span class="sxs-lookup"><span data-stu-id="610c3-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="610c3-158">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="610c3-158">Click Add data source.</span></span>
    * <span data-ttu-id="610c3-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="610c3-159">$BlockName</span></span>  
36. <span data-ttu-id="610c3-160">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-160">Click Save.</span></span>
37. <span data-ttu-id="610c3-161">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-161">Close the page.</span></span>
38. <span data-ttu-id="610c3-162">Klik op de knop Bewerken voor het veld Sleutelwaarde verzamelde gegevens</span><span class="sxs-lookup"><span data-stu-id="610c3-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="610c3-163">Typ in het veld Formule 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span><span class="sxs-lookup"><span data-stu-id="610c3-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="610c3-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="610c3-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="610c3-165">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-165">Click Save.</span></span>
41. <span data-ttu-id="610c3-166">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-166">Close the page.</span></span>
    * <span data-ttu-id="610c3-167">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="610c3-167">Count the lines of this sequence.</span></span> <span data-ttu-id="610c3-168">De resultaten worden afzonderlijk voor verschillende richtingen gebruikt met de naam "blok".</span><span class="sxs-lookup"><span data-stu-id="610c3-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="610c3-169">De waarde "Importeren" wordt gebruikt voor Intrastat-transacties voor ontvangsten.</span><span class="sxs-lookup"><span data-stu-id="610c3-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="610c3-170">De waarde "Exporteren" wordt gebruikt voor Intrastat-transacties voor verzendingen.</span><span class="sxs-lookup"><span data-stu-id="610c3-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="610c3-171">Beschouw dit als een virtueel Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="610c3-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="610c3-172">Voor elke transactie een rij waarin de eerste kolom "blok" is ingevuld met de waarden "Import" en "Export".</span><span class="sxs-lookup"><span data-stu-id="610c3-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="610c3-173">Vouw in de structuur 'Intrastat\Gegevens: Reeks' uit.</span><span class="sxs-lookup"><span data-stu-id="610c3-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="610c3-174">Selecteer in de structuur 'Intrastat\Gegevens: Reeks\Ontvangsten?'.</span><span class="sxs-lookup"><span data-stu-id="610c3-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="610c3-175">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'.</span><span class="sxs-lookup"><span data-stu-id="610c3-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="610c3-176">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="610c3-176">Count the lines of this sequence.</span></span> <span data-ttu-id="610c3-177">De resultaten worden onthouden met de naam "record".</span><span class="sxs-lookup"><span data-stu-id="610c3-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="610c3-178">Selecteer in de structuur '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="610c3-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="610c3-179">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="610c3-179">Click Add data source.</span></span>
47. <span data-ttu-id="610c3-180">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-180">Click Save.</span></span>
48. <span data-ttu-id="610c3-181">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-181">Close the page.</span></span>
49. <span data-ttu-id="610c3-182">Klik op de knop Bewerken voor het veld 'Sleutelwaarde verzamelde gegevens'</span><span class="sxs-lookup"><span data-stu-id="610c3-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="610c3-183">Typ in het veld Formule 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="610c3-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="610c3-184">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-184">Click Save.</span></span>
52. <span data-ttu-id="610c3-185">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-185">Close the page.</span></span>
    * <span data-ttu-id="610c3-186">Tel de regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="610c3-186">Count the lines of this sequence.</span></span> <span data-ttu-id="610c3-187">De resultaten worden afzonderlijk voor verschillende basisproductcode gebruikt met de naam "record".</span><span class="sxs-lookup"><span data-stu-id="610c3-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="610c3-188">Beschouw dit als een virtueel Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="610c3-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="610c3-189">Voor elke transactie een rij waarin de eerste kolom "blok" wordt gevuld met de waarden "Import" en "Export" en het tweede blok "record" wordt gevuld met de waarde van de basisproductcode.</span><span class="sxs-lookup"><span data-stu-id="610c3-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="610c3-190">Select in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen?'.</span><span class="sxs-lookup"><span data-stu-id="610c3-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="610c3-191">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'</span><span class="sxs-lookup"><span data-stu-id="610c3-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="610c3-192">Selecteer in de structuur '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="610c3-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="610c3-193">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="610c3-193">Click Add data source.</span></span>
57. <span data-ttu-id="610c3-194">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-194">Click Save.</span></span>
58. <span data-ttu-id="610c3-195">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-195">Close the page.</span></span>
59. <span data-ttu-id="610c3-196">Klik op de knop Bewerken voor het veld 'Sleutelwaarde verzamelde gegevens'.</span><span class="sxs-lookup"><span data-stu-id="610c3-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="610c3-197">Typ in het veld Formule 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="610c3-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="610c3-198">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-198">Click Save.</span></span>
62. <span data-ttu-id="610c3-199">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-199">Close the page.</span></span>
63. <span data-ttu-id="610c3-200">Vouw in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen: Reeks' uit.</span><span class="sxs-lookup"><span data-stu-id="610c3-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="610c3-201">Vouw in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen: Reeks?\Record =  Intrastat.CommodityRecord' uit.</span><span class="sxs-lookup"><span data-stu-id="610c3-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="610c3-202">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="610c3-202">Click the Format tab.</span></span>
66. <span data-ttu-id="610c3-203">Selecteer in de structuur 'Intrastat\Gegevens\Verzendingen\Record\Factuurbedrag EUR'.</span><span class="sxs-lookup"><span data-stu-id="610c3-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="610c3-204">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="610c3-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="610c3-205">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'.</span><span class="sxs-lookup"><span data-stu-id="610c3-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="610c3-206">Selecteer in de structuur '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="610c3-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="610c3-207">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="610c3-207">Click Add data source.</span></span>
71. <span data-ttu-id="610c3-208">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-208">Click Save.</span></span>
72. <span data-ttu-id="610c3-209">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-209">Close the page.</span></span>
    * <span data-ttu-id="610c3-210">Vat de gefactureerde bedragwaarden samen voor regels van deze reeks.</span><span class="sxs-lookup"><span data-stu-id="610c3-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="610c3-211">De resultaten worden afzonderlijk voor verschillende intrastat-richtingen en basisproductcodes gebruikt met de naam "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="610c3-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="610c3-212">Beschouw dit als een virtueel gemaakt item in het Excel-spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="610c3-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="610c3-213">Voor elke transactie een rij waarin de eerste kolom "blok" is ingevuld met de waarden "Import" en "Export".</span><span class="sxs-lookup"><span data-stu-id="610c3-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="610c3-214">Het tweede blok "record" wordt gevuld met de waarde van de basisproductcode, en de derde kolom "InvoicedAmountEUR" wordt gevuld met de factuurbedragwaarde.</span><span class="sxs-lookup"><span data-stu-id="610c3-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="610c3-215">Vouw in de structuur 'Intrastat\Gegevens\Ontvangsten?' uit.</span><span class="sxs-lookup"><span data-stu-id="610c3-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="610c3-216">Vouw in de structuur 'Intrastat\Gegevens\Ontvangsten?\Record = Intrastat.CommodityRecord' uit.</span><span class="sxs-lookup"><span data-stu-id="610c3-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="610c3-217">Klik op het tabblad Indeling.</span><span class="sxs-lookup"><span data-stu-id="610c3-217">Click the Format tab.</span></span>
76. <span data-ttu-id="610c3-218">Selecteer in de structuur 'Intrastat\Gegevens\Ontvangsten\Record\Factuurbedrag EUR'.</span><span class="sxs-lookup"><span data-stu-id="610c3-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="610c3-219">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="610c3-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="610c3-220">Klik op de knop Bewerken voor het veld 'Sleutelnaam verzamelde gegevens'.</span><span class="sxs-lookup"><span data-stu-id="610c3-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="610c3-221">Selecteer in de structuur '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="610c3-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="610c3-222">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="610c3-222">Click Add data source.</span></span>
81. <span data-ttu-id="610c3-223">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-223">Click Save.</span></span>
82. <span data-ttu-id="610c3-224">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-224">Close the page.</span></span>
83. <span data-ttu-id="610c3-225">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="610c3-225">Click Save.</span></span>
84. <span data-ttu-id="610c3-226">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="610c3-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]