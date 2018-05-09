--- 
title: De indeling uitvoeren voor tellen en totaliseren
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 689514f0614aeb4a8bfad39459267005d0aaf6ef
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="run-the-format-to-do-counting-and-summing"></a><span data-ttu-id="124df-103">De indeling uitvoeren voor tellen en totaliseren</span><span class="sxs-lookup"><span data-stu-id="124df-103">Run the format to do counting and summing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="124df-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.</span><span class="sxs-lookup"><span data-stu-id="124df-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="124df-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="124df-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="124df-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 3: Berekeningen gebruiken om de uitvoer te maken)".</span><span class="sxs-lookup"><span data-stu-id="124df-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="124df-107">Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="124df-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="124df-108">Test deze configuratie voor het genereren van de Intrastat-rapporten</span><span class="sxs-lookup"><span data-stu-id="124df-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="124df-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="124df-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="124df-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="124df-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="124df-111">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="124df-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="124df-112">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="124df-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="124df-113">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="124df-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="124df-114">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="124df-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="124df-115">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="124df-115">Click User parameters.</span></span>
8. <span data-ttu-id="124df-116">Selecteer Ja in het veld Uitvoeringsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="124df-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="124df-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="124df-117">Click OK.</span></span>
10. <span data-ttu-id="124df-118">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="124df-118">Click Edit.</span></span>
11. <span data-ttu-id="124df-119">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="124df-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="124df-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="124df-120">Click Save.</span></span>
13. <span data-ttu-id="124df-121">Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="124df-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="124df-122">Vouw de sectie Elektronische rapportage uit.</span><span class="sxs-lookup"><span data-stu-id="124df-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="124df-123">Selecteer de configuratie 'Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="124df-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="124df-124">Selecteer de configuratie 'Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="124df-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="124df-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="124df-125">Click Save.</span></span>
18. <span data-ttu-id="124df-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="124df-126">Close the page.</span></span>
19. <span data-ttu-id="124df-127">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="124df-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="124df-128">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="124df-128">Click Output.</span></span>
21. <span data-ttu-id="124df-129">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="124df-129">Click Report.</span></span>
    * <span data-ttu-id="124df-130">Voer het proces uit om het Intrastat-rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="124df-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="124df-131">Stel in het veld Begindatum de datum in op "2000-01-01".</span><span class="sxs-lookup"><span data-stu-id="124df-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="124df-132">Definieer begin- en einddatums voor de rapportperiode die de bestaande transacties op het formulier omvatten.</span><span class="sxs-lookup"><span data-stu-id="124df-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="124df-133">Stel in het veld Einddatum de datum in op "2022-12-31".</span><span class="sxs-lookup"><span data-stu-id="124df-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="124df-134">Definieer begin- en einddatums voor de rapportperiode die de bestaande transacties op het formulier omvatten.</span><span class="sxs-lookup"><span data-stu-id="124df-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="124df-135">Selecteer Ontvangsten in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="124df-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="124df-136">Selecteer Ja in het veld Bestand maken.</span><span class="sxs-lookup"><span data-stu-id="124df-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="124df-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="124df-137">Click OK.</span></span>
    * <span data-ttu-id="124df-138">Controleer de gemaakte uitvoer met de overzichtsregels aan het einde.</span><span class="sxs-lookup"><span data-stu-id="124df-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="124df-139">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="124df-139">Click New.</span></span>
28. <span data-ttu-id="124df-140">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="124df-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="124df-141">Selecteer Verzendingen in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="124df-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="124df-142">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="124df-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="124df-143">Typ of selecteer een waarde in het veld Basisproduct.</span><span class="sxs-lookup"><span data-stu-id="124df-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="124df-144">Stel Gewicht in op 10.</span><span class="sxs-lookup"><span data-stu-id="124df-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="124df-145">Stel Factuurbedrag in op 10000.</span><span class="sxs-lookup"><span data-stu-id="124df-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="124df-146">Stel Statistisch bedrag in op 10000.</span><span class="sxs-lookup"><span data-stu-id="124df-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="124df-147">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="124df-147">Click Output.</span></span>
36. <span data-ttu-id="124df-148">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="124df-148">Click Report.</span></span>
37. <span data-ttu-id="124df-149">Selecteer Verzendingen in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="124df-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="124df-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="124df-150">Click OK.</span></span>
    * <span data-ttu-id="124df-151">Controleer de gemaakte uitvoer met de overzichtsregels aan het einde.</span><span class="sxs-lookup"><span data-stu-id="124df-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="124df-152">Let op dat dit in vergelijking met de eerste uitvoering is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="124df-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="124df-153">Voer deze configuratie uit in foutoplossingsmodus uit om de verzamelde tel- en totaalgegevens te controleren</span><span class="sxs-lookup"><span data-stu-id="124df-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="124df-154">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="124df-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="124df-155">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="124df-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="124df-156">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="124df-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="124df-157">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="124df-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="124df-158">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="124df-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="124df-159">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="124df-159">Click User parameters.</span></span>
7. <span data-ttu-id="124df-160">Selecteer Ja in het veld Uitvoeren in foutoplossingsmodus.</span><span class="sxs-lookup"><span data-stu-id="124df-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="124df-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="124df-161">Click OK.</span></span>
9. <span data-ttu-id="124df-162">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="124df-162">Close the page.</span></span>
10. <span data-ttu-id="124df-163">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="124df-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="124df-164">Klik op Uitvoer.</span><span class="sxs-lookup"><span data-stu-id="124df-164">Click Output.</span></span>
12. <span data-ttu-id="124df-165">Klik op Rapport.</span><span class="sxs-lookup"><span data-stu-id="124df-165">Click Report.</span></span>
13. <span data-ttu-id="124df-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="124df-166">Click OK.</span></span>
14. <span data-ttu-id="124df-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="124df-167">Close the page.</span></span>
15. <span data-ttu-id="124df-168">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="124df-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="124df-169">Vouw in de structuur 'Intrastat-model' uit.</span><span class="sxs-lookup"><span data-stu-id="124df-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="124df-170">Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.</span><span class="sxs-lookup"><span data-stu-id="124df-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="124df-171">Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.</span><span class="sxs-lookup"><span data-stu-id="124df-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="124df-172">Klik op Foutopsporingslogboeken.</span><span class="sxs-lookup"><span data-stu-id="124df-172">Click Debug logs.</span></span>
    * <span data-ttu-id="124df-173">Merk op dat er een record met een foutopsporingslogboek is gemaakt voor het uitvoeringsproces van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="124df-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="124df-174">Klik op Koppelen.</span><span class="sxs-lookup"><span data-stu-id="124df-174">Click Attach.</span></span>
21. <span data-ttu-id="124df-175">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="124df-175">Click Open.</span></span>
    * <span data-ttu-id="124df-176">Controleer het gemaakte XML-bestand dat de tellings- en totaliseringsgegevens bevat die tijdens de uitvoering van de geselecteerde configuratie zijn verzameld.</span><span class="sxs-lookup"><span data-stu-id="124df-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


