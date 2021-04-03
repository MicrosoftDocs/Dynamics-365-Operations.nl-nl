---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 4: Indeling uitvoeren)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage configureert voor tellen en totaliseren op basis van de gegevens van de reeds gegenereerde tekstuitvoer. (Deel 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ca8449581edc06016b6e387880aad91087b67f1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565412"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="0bc5a-104">ER Indeling configureren voor tellen en totaliseren (deel 4: Indeling uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="0bc5a-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0bc5a-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="0bc5a-106">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="0bc5a-107">Als u deze stappen wilt uitvoeren, voert u eerst de stappen in de procedure ER Indeling configureren voor tellen en totaliseren (Deel 3: Berekeningen gebruiken om de uitvoer te maken) uit.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="0bc5a-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="0bc5a-109">Test deze configuratie voor het genereren van de Intrastat-rapporten</span><span class="sxs-lookup"><span data-stu-id="0bc5a-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="0bc5a-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0bc5a-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0bc5a-112">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="0bc5a-113">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="0bc5a-114">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="0bc5a-115">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="0bc5a-116">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-116">Click User parameters.</span></span>
8. <span data-ttu-id="0bc5a-117">Selecteer Ja in het veld Uitvoeringsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="0bc5a-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-118">Click OK.</span></span>
10. <span data-ttu-id="0bc5a-119">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-119">Click Edit.</span></span>
11. <span data-ttu-id="0bc5a-120">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="0bc5a-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-121">Click Save.</span></span>
13. <span data-ttu-id="0bc5a-122">Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="0bc5a-123">Vouw de sectie Elektronische rapportage uit.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="0bc5a-124">Selecteer de configuratie 'Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="0bc5a-125">Selecteer de configuratie 'Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="0bc5a-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-126">Click Save.</span></span>
18. <span data-ttu-id="0bc5a-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-127">Close the page.</span></span>
19. <span data-ttu-id="0bc5a-128">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="0bc5a-129">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-129">Click Output.</span></span>
21. <span data-ttu-id="0bc5a-130">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-130">Click Report.</span></span>
    * <span data-ttu-id="0bc5a-131">Voer het proces uit om het Intrastat-rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="0bc5a-132">Stel in het veld Begindatum de datum in op "2000-01-01".</span><span class="sxs-lookup"><span data-stu-id="0bc5a-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="0bc5a-133">Definieer begin- en einddatums voor de rapportperiode die de bestaande transacties op het formulier omvatten.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="0bc5a-134">Stel in het veld Einddatum de datum in op "2022-12-31".</span><span class="sxs-lookup"><span data-stu-id="0bc5a-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="0bc5a-135">Definieer begin- en einddatums voor de rapportperiode die de bestaande transacties op het formulier omvatten.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="0bc5a-136">Selecteer Ontvangsten in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="0bc5a-137">Selecteer Ja in het veld Bestand maken.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="0bc5a-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-138">Click OK.</span></span>
    * <span data-ttu-id="0bc5a-139">Controleer de gemaakte uitvoer met de overzichtsregels aan het einde.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="0bc5a-140">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-140">Click New.</span></span>
28. <span data-ttu-id="0bc5a-141">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="0bc5a-142">Selecteer Verzendingen in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="0bc5a-143">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="0bc5a-144">Typ of selecteer een waarde in het veld Basisproduct.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="0bc5a-145">Stel Gewicht in op 10.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="0bc5a-146">Stel Factuurbedrag in op 10000.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="0bc5a-147">Stel Statistisch bedrag in op 10000.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="0bc5a-148">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-148">Click Output.</span></span>
36. <span data-ttu-id="0bc5a-149">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-149">Click Report.</span></span>
37. <span data-ttu-id="0bc5a-150">Selecteer Verzendingen in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="0bc5a-151">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-151">Click OK.</span></span>
    * <span data-ttu-id="0bc5a-152">Controleer de gemaakte uitvoer met de overzichtsregels aan het einde.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="0bc5a-153">Let op dat dit in vergelijking met de eerste uitvoering is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="0bc5a-154">Voer deze configuratie uit in foutoplossingsmodus uit om de verzamelde tel- en totaalgegevens te controleren</span><span class="sxs-lookup"><span data-stu-id="0bc5a-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="0bc5a-155">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0bc5a-156">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="0bc5a-157">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="0bc5a-158">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="0bc5a-159">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="0bc5a-160">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-160">Click User parameters.</span></span>
7. <span data-ttu-id="0bc5a-161">Selecteer Ja in het veld Uitvoeren in foutoplossingsmodus.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="0bc5a-162">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-162">Click OK.</span></span>
9. <span data-ttu-id="0bc5a-163">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-163">Close the page.</span></span>
10. <span data-ttu-id="0bc5a-164">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="0bc5a-165">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-165">Click Output.</span></span>
12. <span data-ttu-id="0bc5a-166">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-166">Click Report.</span></span>
13. <span data-ttu-id="0bc5a-167">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-167">Click OK.</span></span>
14. <span data-ttu-id="0bc5a-168">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-168">Close the page.</span></span>
15. <span data-ttu-id="0bc5a-169">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="0bc5a-170">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="0bc5a-171">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="0bc5a-172">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="0bc5a-173">Klik op Foutopsporingslogboeken.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-173">Click Debug logs.</span></span>
    * <span data-ttu-id="0bc5a-174">Merk op dat er een record met een foutopsporingslogboek is gemaakt voor het uitvoeringsproces van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="0bc5a-175">Klik op Koppelen.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-175">Click Attach.</span></span>
21. <span data-ttu-id="0bc5a-176">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-176">Click Open.</span></span>
    * <span data-ttu-id="0bc5a-177">Controleer het gemaakte XML-bestand dat de tellings- en totaliseringsgegevens bevat die tijdens de uitvoering van de geselecteerde configuratie zijn verzameld.</span><span class="sxs-lookup"><span data-stu-id="0bc5a-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]