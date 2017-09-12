--- 
title: De indeling uitvoeren voor tellen en totaliseren voor elektronische aangifte (ER)
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 60a34e35a376635669b764457617cb997822bdcd
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="edc87-103">De indeling uitvoeren voor tellen en totaliseren voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="edc87-103">Run the format to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="edc87-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="edc87-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="edc87-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="edc87-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="edc87-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 3: Berekeningen gebruiken om de uitvoer te maken)".</span><span class="sxs-lookup"><span data-stu-id="edc87-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="edc87-107">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="edc87-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="edc87-108">Test deze configuratie voor het genereren van de Intrastat-rapporten</span><span class="sxs-lookup"><span data-stu-id="edc87-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="edc87-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="edc87-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="edc87-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="edc87-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="edc87-111">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="edc87-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="edc87-112">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="edc87-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="edc87-113">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="edc87-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="edc87-114">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="edc87-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="edc87-115">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="edc87-115">Click User parameters.</span></span>
8. <span data-ttu-id="edc87-116">Selecteer Ja in het veld Uitvoeringsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="edc87-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="edc87-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edc87-117">Click OK.</span></span>
10. <span data-ttu-id="edc87-118">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="edc87-118">Click Edit.</span></span>
11. <span data-ttu-id="edc87-119">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="edc87-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="edc87-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="edc87-120">Click Save.</span></span>
13. <span data-ttu-id="edc87-121">Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="edc87-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="edc87-122">Vouw de sectie Elektronische rapportage uit.</span><span class="sxs-lookup"><span data-stu-id="edc87-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="edc87-123">Selecteer de configuratie 'Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="edc87-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="edc87-124">Selecteer de configuratie 'Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="edc87-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="edc87-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="edc87-125">Click Save.</span></span>
18. <span data-ttu-id="edc87-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edc87-126">Close the page.</span></span>
19. <span data-ttu-id="edc87-127">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="edc87-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="edc87-128">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="edc87-128">Click Output.</span></span>
21. <span data-ttu-id="edc87-129">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="edc87-129">Click Report.</span></span>
    * <span data-ttu-id="edc87-130">Voer het proces uit om het Intrastat-rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="edc87-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="edc87-131">Stel in het veld Begindatum de datum in op "2000-01-01".</span><span class="sxs-lookup"><span data-stu-id="edc87-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="edc87-132">Definieer begin- en einddatums voor de rapportperiode die de bestaande transacties op het formulier omvatten.</span><span class="sxs-lookup"><span data-stu-id="edc87-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="edc87-133">Stel in het veld Einddatum de datum in op "2022-12-31".</span><span class="sxs-lookup"><span data-stu-id="edc87-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="edc87-134">Definieer begin- en einddatums voor de rapportperiode die de bestaande transacties op het formulier omvatten.</span><span class="sxs-lookup"><span data-stu-id="edc87-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="edc87-135">Selecteer Ontvangsten in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="edc87-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="edc87-136">Selecteer Ja in het veld Bestand maken.</span><span class="sxs-lookup"><span data-stu-id="edc87-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="edc87-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edc87-137">Click OK.</span></span>
    * <span data-ttu-id="edc87-138">Controleer de gemaakte uitvoer met de overzichtsregels aan het einde.</span><span class="sxs-lookup"><span data-stu-id="edc87-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="edc87-139">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="edc87-139">Click New.</span></span>
28. <span data-ttu-id="edc87-140">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="edc87-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="edc87-141">Selecteer Verzendingen in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="edc87-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="edc87-142">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="edc87-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="edc87-143">Typ of selecteer een waarde in het veld Basisproduct.</span><span class="sxs-lookup"><span data-stu-id="edc87-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="edc87-144">Stel Gewicht in op 10.</span><span class="sxs-lookup"><span data-stu-id="edc87-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="edc87-145">Stel Factuurbedrag in op 10000.</span><span class="sxs-lookup"><span data-stu-id="edc87-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="edc87-146">Stel Statistisch bedrag in op 10000.</span><span class="sxs-lookup"><span data-stu-id="edc87-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="edc87-147">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="edc87-147">Click Output.</span></span>
36. <span data-ttu-id="edc87-148">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="edc87-148">Click Report.</span></span>
37. <span data-ttu-id="edc87-149">Selecteer Verzendingen in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="edc87-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="edc87-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edc87-150">Click OK.</span></span>
    * <span data-ttu-id="edc87-151">Controleer de gemaakte uitvoer met de overzichtsregels aan het einde.</span><span class="sxs-lookup"><span data-stu-id="edc87-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="edc87-152">Let op dat dit in vergelijking met de eerste uitvoering is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="edc87-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="edc87-153">Voer deze configuratie uit in foutoplossingsmodus uit om de verzamelde tel- en totaalgegevens te controleren</span><span class="sxs-lookup"><span data-stu-id="edc87-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="edc87-154">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="edc87-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="edc87-155">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="edc87-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="edc87-156">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="edc87-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="edc87-157">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="edc87-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="edc87-158">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="edc87-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="edc87-159">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="edc87-159">Click User parameters.</span></span>
7. <span data-ttu-id="edc87-160">Selecteer Ja in het veld Uitvoeren in foutoplossingsmodus.</span><span class="sxs-lookup"><span data-stu-id="edc87-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="edc87-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edc87-161">Click OK.</span></span>
9. <span data-ttu-id="edc87-162">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edc87-162">Close the page.</span></span>
10. <span data-ttu-id="edc87-163">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="edc87-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="edc87-164">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="edc87-164">Click Output.</span></span>
12. <span data-ttu-id="edc87-165">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="edc87-165">Click Report.</span></span>
13. <span data-ttu-id="edc87-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edc87-166">Click OK.</span></span>
14. <span data-ttu-id="edc87-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edc87-167">Close the page.</span></span>
15. <span data-ttu-id="edc87-168">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="edc87-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="edc87-169">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="edc87-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="edc87-170">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="edc87-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="edc87-171">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="edc87-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="edc87-172">Klik op Foutopsporingslogboeken.</span><span class="sxs-lookup"><span data-stu-id="edc87-172">Click Debug logs.</span></span>
    * <span data-ttu-id="edc87-173">Merk op dat er een record met een foutopsporingslogboek is gemaakt voor het uitvoeringsproces van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="edc87-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="edc87-174">Klik op Koppelen.</span><span class="sxs-lookup"><span data-stu-id="edc87-174">Click Attach.</span></span>
21. <span data-ttu-id="edc87-175">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="edc87-175">Click Open.</span></span>
    * <span data-ttu-id="edc87-176">Controleer het gemaakte XML-bestand dat de tellings- en totaliseringsgegevens bevat die tijdens de uitvoering van de geselecteerde configuratie zijn verzameld.</span><span class="sxs-lookup"><span data-stu-id="edc87-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


