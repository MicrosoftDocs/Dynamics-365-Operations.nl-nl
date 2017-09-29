--- 
title: Afdrukken van nummerplaatlabel inschakelen
description: Met deze procedure schakelt u het automatisch afdrukken van een SSCC-label (Serial Shipping Container Code) in nadat het laatste artikel is verzameld van de voorraad in het werkproces orderverzamelen voor verkoop.
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="77270-103">Afdrukken van nummerplaatlabel inschakelen</span><span class="sxs-lookup"><span data-stu-id="77270-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="77270-104">Met deze procedure schakelt u het automatisch afdrukken van een SSCC-label (Serial Shipping Container Code) in nadat het laatste artikel is verzameld van de voorraad in het werkproces orderverzamelen voor verkoop.</span><span class="sxs-lookup"><span data-stu-id="77270-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="77270-105">U kunt deze procedure in het bedrijf USMF van de demogegevens uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="77270-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="77270-106">Als u het met behulp van uw eigen gegevens uitvoert, moet u een ingestelde nummerreeks voor nummerplaten hebben.</span><span class="sxs-lookup"><span data-stu-id="77270-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="77270-107">U moet een labelprinter instellen voordat u deze taak start.</span><span class="sxs-lookup"><span data-stu-id="77270-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="77270-108">Ga naar Organisatiebeheer > Instellingen > Netwerkprinters.</span><span class="sxs-lookup"><span data-stu-id="77270-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="77270-109">Klik in het actievenster op Opties en vervolgens op de knop Installatieprogramma van documentrouteringsagent downloaden.</span><span class="sxs-lookup"><span data-stu-id="77270-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="77270-110">Voer het installatieprogramma uit en zorg ervoor dat een netwerkprinter Actief is voordat u met de procedure vervolgt.</span><span class="sxs-lookup"><span data-stu-id="77270-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="77270-111">Het GS1-bedrijfsvoorvoegsel instellen</span><span class="sxs-lookup"><span data-stu-id="77270-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="77270-112">Ga naar Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="77270-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="77270-113">Geef in het veld GS1-bedrijfsvoorvoegsel het 7-cijferige GS1-bedrijfsnummer op.</span><span class="sxs-lookup"><span data-stu-id="77270-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="77270-114">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="77270-114">Click Save.</span></span>
4. <span data-ttu-id="77270-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77270-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="77270-116">De nummerreeks voor het SSCC-nummerplaatnummer instellen</span><span class="sxs-lookup"><span data-stu-id="77270-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="77270-117">Ga naar Organisatiebeheer > Nummerreeksen > Nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="77270-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="77270-118">Selecteer een optie in het veld Gebied.</span><span class="sxs-lookup"><span data-stu-id="77270-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="77270-119">Selecteer een optie in het veld Verwijzing.</span><span class="sxs-lookup"><span data-stu-id="77270-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="77270-120">Typ een waarde in het veld Bedrijf.</span><span class="sxs-lookup"><span data-stu-id="77270-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="77270-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="77270-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="77270-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="77270-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="77270-123">Vouw de sectie Segmenten uit.</span><span class="sxs-lookup"><span data-stu-id="77270-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="77270-124">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="77270-124">Click Edit.</span></span>
9. <span data-ttu-id="77270-125">Selecteer in de tabel Segmenten de eerste rij</span><span class="sxs-lookup"><span data-stu-id="77270-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="77270-126">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="77270-126">Click Remove.</span></span>
11. <span data-ttu-id="77270-127">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="77270-127">Click Remove.</span></span>
12. <span data-ttu-id="77270-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="77270-128">Click Save.</span></span>
13. <span data-ttu-id="77270-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77270-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="77270-130">De documentrouteringsindeling maken</span><span class="sxs-lookup"><span data-stu-id="77270-130">Create the document route layout</span></span>
1. <span data-ttu-id="77270-131">Ga naar Magazijnbeheer > Instellingen > Documentroutering > Routeringsindelingen voor documenten.</span><span class="sxs-lookup"><span data-stu-id="77270-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="77270-132">Schakel de SSCC-indeling in.</span><span class="sxs-lookup"><span data-stu-id="77270-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="77270-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="77270-133">Click New.</span></span>
3. <span data-ttu-id="77270-134">Typ een waarde in het veld Indelings-id.</span><span class="sxs-lookup"><span data-stu-id="77270-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="77270-135">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="77270-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="77270-136">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="77270-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="77270-137">Klik op Invoegen aan het einde van de tekst.</span><span class="sxs-lookup"><span data-stu-id="77270-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="77270-138">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="77270-138">Click Save.</span></span>
8. <span data-ttu-id="77270-139">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77270-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="77270-140">De documentroutering instellen</span><span class="sxs-lookup"><span data-stu-id="77270-140">Set up the document routing</span></span>
1. <span data-ttu-id="77270-141">Ga naar Magazijnbeheer > Instellingen > Documentroutering > Documentroutering.</span><span class="sxs-lookup"><span data-stu-id="77270-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="77270-142">Selecteer een optie in het veld Werkordertype.</span><span class="sxs-lookup"><span data-stu-id="77270-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="77270-143">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="77270-143">Click New.</span></span>
4. <span data-ttu-id="77270-144">Typ een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="77270-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="77270-145">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="77270-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="77270-146">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="77270-146">Click New.</span></span>
7. <span data-ttu-id="77270-147">Typ of selecteer een waarde in het veld Indelings-id.</span><span class="sxs-lookup"><span data-stu-id="77270-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="77270-148">Voer in het veld Naam de naam in van de printer die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="77270-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="77270-149">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="77270-149">Click Save.</span></span>
10. <span data-ttu-id="77270-150">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77270-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="77270-151">Menu voor mobiel apparaat maken</span><span class="sxs-lookup"><span data-stu-id="77270-151">Create mobile device menu</span></span>
1. <span data-ttu-id="77270-152">Ga naar Magazijnbeheer > Instellingen > Mobiel apparaat > Menuopties voor mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="77270-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="77270-153">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="77270-153">Click New.</span></span>
3. <span data-ttu-id="77270-154">Typ een waarde in het veld Menuoptie.</span><span class="sxs-lookup"><span data-stu-id="77270-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="77270-155">Typ een waarde in het veld Titel.</span><span class="sxs-lookup"><span data-stu-id="77270-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="77270-156">Selecteer een optie in het veld Modus.</span><span class="sxs-lookup"><span data-stu-id="77270-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="77270-157">Selecteer Ja in het veld Bestaand werk gebruiken.</span><span class="sxs-lookup"><span data-stu-id="77270-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="77270-158">Selecteer Ja in het veld Nummerplaat maken.</span><span class="sxs-lookup"><span data-stu-id="77270-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="77270-159">Vouw de werkklassensectie uit.</span><span class="sxs-lookup"><span data-stu-id="77270-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="77270-160">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="77270-160">Click New.</span></span>
10. <span data-ttu-id="77270-161">Typ een waarde in het veld Werkklasse-id.</span><span class="sxs-lookup"><span data-stu-id="77270-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="77270-162">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="77270-162">Click Save.</span></span>
12. <span data-ttu-id="77270-163">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77270-163">Close the page.</span></span>
13. <span data-ttu-id="77270-164">Ga naar Magazijnbeheer > Instellingen > Mobiel apparaat > Menu voor mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="77270-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="77270-165">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="77270-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="77270-166">Selecteer in de structuur ´Selecteer in de structuur de menuoptie die u eerder hebt gemaakt.´.</span><span class="sxs-lookup"><span data-stu-id="77270-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="77270-167">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="77270-167">Click Edit.</span></span>
17. <span data-ttu-id="77270-168">Klik op de pijl om de menuoptie aan het menu toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="77270-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="77270-169">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="77270-169">Click Save.</span></span>
19. <span data-ttu-id="77270-170">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77270-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="77270-171">Een werksjabloon bijwerken</span><span class="sxs-lookup"><span data-stu-id="77270-171">Update a work template</span></span>
1. <span data-ttu-id="77270-172">Ga naar Magazijnbeheer > Instellingen > Werk > Werksjablonen.</span><span class="sxs-lookup"><span data-stu-id="77270-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="77270-173">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="77270-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="77270-174">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="77270-174">Click Edit.</span></span>
4. <span data-ttu-id="77270-175">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="77270-175">Click New.</span></span>
5. <span data-ttu-id="77270-176">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="77270-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="77270-177">Selecteer Afdrukken in het veld Werktype.</span><span class="sxs-lookup"><span data-stu-id="77270-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="77270-178">Typ of selecteer een waarde in het veld Werkklasse-id.</span><span class="sxs-lookup"><span data-stu-id="77270-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="77270-179">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="77270-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="77270-180">Klik op Omhoog.</span><span class="sxs-lookup"><span data-stu-id="77270-180">Click Move up.</span></span>
10. <span data-ttu-id="77270-181">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="77270-181">Click Save.</span></span>
11. <span data-ttu-id="77270-182">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="77270-182">Close the page.</span></span>


