---
title: Kwaliteitsorders instellen
description: "Deze procedure laat zien hoe u een kwaliteitsbeheerproces kunt inschakelen waarbij inkomende voorraad onmiddellijk na aankomstregistratie moet worden geïnspecteerd."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: fbc99ae02576cb76edecb9ac74b1823305c5936b
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="0b9df-103">Kwaliteitsorders instellen</span><span class="sxs-lookup"><span data-stu-id="0b9df-103">Set up quality orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b9df-104">Deze procedure laat zien hoe u een kwaliteitsbeheerproces kunt inschakelen waarbij inkomende voorraad onmiddellijk na aankomstregistratie moet worden geïnspecteerd.</span><span class="sxs-lookup"><span data-stu-id="0b9df-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="0b9df-105">De procedure wordt gewoonlijk uitgevoerd door een kwaliteitsmanager.</span><span class="sxs-lookup"><span data-stu-id="0b9df-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="0b9df-106">Het proces bevat het maken van een kwaliteitsgroep, om de artikelen te definiëren die zullen worden bemonsterd, en een testgroep voor het groeperen van de tests die zullen worden uitgevoerd op artikelen in de kwaliteitsgroep.</span><span class="sxs-lookup"><span data-stu-id="0b9df-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="0b9df-107">U kunt deze taakgeleiding uitvoeren in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="0b9df-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="0b9df-108">Kwaliteitsbeheer inschakelen</span><span class="sxs-lookup"><span data-stu-id="0b9df-108">Enable quality management</span></span>
1. <span data-ttu-id="0b9df-109">Ga naar Voorraadbeheer > Instellingen > Parameters voor voorraad- en magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="0b9df-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="0b9df-110">Klik op het tabblad Kwaliteitsbeheer.</span><span class="sxs-lookup"><span data-stu-id="0b9df-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="0b9df-111">Stel de optie Kwaliteitsbeheer gebruiken in op Ja.</span><span class="sxs-lookup"><span data-stu-id="0b9df-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="0b9df-112">Klik op Rapportinstellingen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-112">Click Report setup.</span></span>
    * <span data-ttu-id="0b9df-113">In USMF is de rapportinstelling voor kwaliteitsbeheer al gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="0b9df-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="0b9df-114">Als dit nog niet is gebeurd, kunt u hier nieuwe regels toevoegen voor verschillende soorten rapporten en het type document selecteren dat voor elk rapport moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0b9df-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="0b9df-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-115">Close the page.</span></span>
6. <span data-ttu-id="0b9df-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="0b9df-117">Een test maken</span><span class="sxs-lookup"><span data-stu-id="0b9df-117">Create a test</span></span>
1. <span data-ttu-id="0b9df-118">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Tests.</span><span class="sxs-lookup"><span data-stu-id="0b9df-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="0b9df-119">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0b9df-119">Click New.</span></span>
3. <span data-ttu-id="0b9df-120">Typ een waarde in het veld Test.</span><span class="sxs-lookup"><span data-stu-id="0b9df-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="0b9df-121">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="0b9df-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b9df-122">Selecteer Optie in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="0b9df-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="0b9df-123">In dit voorbeeld selecteren wij Optie zodat het mogelijk is de testresultaten op basis van vooraf gedefinieerde waarden toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="0b9df-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0b9df-124">Click Save.</span></span>
7. <span data-ttu-id="0b9df-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="0b9df-126">Testvariabelen maken om de manier te definiëren waarop testresultaten worden vastgelegd</span><span class="sxs-lookup"><span data-stu-id="0b9df-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="0b9df-127">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Testvariabelen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="0b9df-128">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0b9df-128">Click New.</span></span>
3. <span data-ttu-id="0b9df-129">Typ een waarde in het veld Variabele.</span><span class="sxs-lookup"><span data-stu-id="0b9df-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="0b9df-130">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="0b9df-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b9df-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0b9df-131">Click Save.</span></span>
6. <span data-ttu-id="0b9df-132">Klik op Resultaten.</span><span class="sxs-lookup"><span data-stu-id="0b9df-132">Click Outcomes.</span></span>
7. <span data-ttu-id="0b9df-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0b9df-133">Click New.</span></span>
8. <span data-ttu-id="0b9df-134">Typ een waarde in het veld Resultaat.</span><span class="sxs-lookup"><span data-stu-id="0b9df-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="0b9df-135">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="0b9df-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="0b9df-136">Selecteer Geslaagd in het veld Uitslagstatus.</span><span class="sxs-lookup"><span data-stu-id="0b9df-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="0b9df-137">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0b9df-137">Click Save.</span></span>
12. <span data-ttu-id="0b9df-138">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0b9df-138">Click New.</span></span>
13. <span data-ttu-id="0b9df-139">Typ een waarde in het veld Resultaat.</span><span class="sxs-lookup"><span data-stu-id="0b9df-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="0b9df-140">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="0b9df-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="0b9df-141">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0b9df-141">Click Save.</span></span>
16. <span data-ttu-id="0b9df-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-142">Close the page.</span></span>
17. <span data-ttu-id="0b9df-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="0b9df-144">Artikelbemonstering instellen</span><span class="sxs-lookup"><span data-stu-id="0b9df-144">Set up item sampling</span></span>
1. <span data-ttu-id="0b9df-145">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Artikelbemonstering.</span><span class="sxs-lookup"><span data-stu-id="0b9df-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="0b9df-146">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0b9df-146">Click New.</span></span>
3. <span data-ttu-id="0b9df-147">Typ een waarde in het veld Artikelbemonstering.</span><span class="sxs-lookup"><span data-stu-id="0b9df-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="0b9df-148">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="0b9df-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b9df-149">Voer een getal in het veld Waarde in.</span><span class="sxs-lookup"><span data-stu-id="0b9df-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="0b9df-150">Deze waarde heeft betrekking op de hoeveelheidsspecificatie die in het aangrenzende veld is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0b9df-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="0b9df-151">Vouw de sectie Proces uit of samen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="0b9df-152">Schakel het selectievakje Volledig blokkeren in of uit.</span><span class="sxs-lookup"><span data-stu-id="0b9df-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="0b9df-153">Als u deze optie selecteert, wordt de gehele partij of orderregelhoeveelheid geblokkeerd als een test is mislukt.</span><span class="sxs-lookup"><span data-stu-id="0b9df-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="0b9df-154">Als u deze niet selecteert, worden alleen de artikelen in de kwaliteitsorder geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="0b9df-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="0b9df-155">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0b9df-155">Click Save.</span></span>
9. <span data-ttu-id="0b9df-156">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="0b9df-157">Een kwaliteitsgroep maken</span><span class="sxs-lookup"><span data-stu-id="0b9df-157">Create a quality group</span></span>
1. <span data-ttu-id="0b9df-158">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Kwaliteitsgroepen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="0b9df-159">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0b9df-159">Click New.</span></span>
3. <span data-ttu-id="0b9df-160">Typ een waarde in het veld Kwaliteitsgroep.</span><span class="sxs-lookup"><span data-stu-id="0b9df-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="0b9df-161">Gebruik een beschrijvende naam om u te helpen bepalen welk type artikelen de groep zal bevatten (uw bemonsteringscriteria).</span><span class="sxs-lookup"><span data-stu-id="0b9df-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="0b9df-162">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="0b9df-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b9df-163">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0b9df-163">Click Save.</span></span>
6. <span data-ttu-id="0b9df-164">Klik op Artikelen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-164">Click Add items.</span></span>
7. <span data-ttu-id="0b9df-165">Selecteer de rij Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="0b9df-165">Select the Item number row</span></span>
    * <span data-ttu-id="0b9df-166">In dit voorbeeld wordt het filteren uitgevoerd op basis van het artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="0b9df-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="0b9df-167">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="0b9df-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0b9df-168">Typ bijvoorbeeld T\* om te filteren op de artikelnummers met T beginnen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="0b9df-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0b9df-169">Click OK.</span></span>
10. <span data-ttu-id="0b9df-170">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="0b9df-170">Click OK.</span></span>
11. <span data-ttu-id="0b9df-171">Klik op Artikelkwaliteitsgroepen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="0b9df-172">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-172">Close the page.</span></span>
13. <span data-ttu-id="0b9df-173">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="0b9df-174">Een testgroep maken</span><span class="sxs-lookup"><span data-stu-id="0b9df-174">Create a test group</span></span>
1. <span data-ttu-id="0b9df-175">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Testgroepen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="0b9df-176">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0b9df-176">Click New.</span></span>
3. <span data-ttu-id="0b9df-177">Typ een waarde in het veld Testgroep.</span><span class="sxs-lookup"><span data-stu-id="0b9df-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="0b9df-178">Geef de Testgroep een naam die u zal helpen onthouden welk type van testen wordt uitgevoerd en welke kwaliteitsgroep hieraan moet worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="0b9df-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="0b9df-179">Als het bijvoorbeeld moet worden gebruikt met een kwaliteitsgroep die artikelen selecteert die beginnen met "T" beginnen, kunt u het "T-artikelen testen" noemen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="0b9df-180">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="0b9df-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b9df-181">Selecteer in het veld Artikelbemonstering de artikelbemonsteringsregel die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0b9df-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="0b9df-182">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0b9df-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0b9df-183">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-183">Click Add.</span></span>
8. <span data-ttu-id="0b9df-184">Voer een getal in het veld Volgnummer in.</span><span class="sxs-lookup"><span data-stu-id="0b9df-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="0b9df-185">Selecteer in het veld Test de test die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0b9df-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="0b9df-186">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0b9df-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="0b9df-187">Klik op het tabblad Test.</span><span class="sxs-lookup"><span data-stu-id="0b9df-187">Click the Test tab.</span></span>
12. <span data-ttu-id="0b9df-188">Selecteer in het veld Variabele de testvariabele die u eerder hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="0b9df-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="0b9df-189">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0b9df-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0b9df-190">Klik in het veld Standaarduitslag op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="0b9df-191">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0b9df-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="0b9df-192">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0b9df-192">Click Save.</span></span>
17. <span data-ttu-id="0b9df-193">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="0b9df-194">Definiëren wanneer kwaliteitsorders worden gemaakt</span><span class="sxs-lookup"><span data-stu-id="0b9df-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="0b9df-195">Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Kwaliteitskoppelingen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="0b9df-196">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0b9df-196">Click New.</span></span>
3. <span data-ttu-id="0b9df-197">Selecteer een optie in het veld Verwijzingstype.</span><span class="sxs-lookup"><span data-stu-id="0b9df-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="0b9df-198">Selecteer Groep in het veld Artikelcode.</span><span class="sxs-lookup"><span data-stu-id="0b9df-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="0b9df-199">In dit voorbeeld selecteren we "Groep" en gebruiken we de kwaliteitsgroep die we eerder hebben gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0b9df-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="0b9df-200">U kunt dit ook instellen op "Tabel" om handmatig de artikelen op te geven of "Alle" selecteren om alle artikelen toe te voegen aan de kwaliteitsorder.</span><span class="sxs-lookup"><span data-stu-id="0b9df-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="0b9df-201">Selecteer in het veld Artikel de artikelgroep die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0b9df-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="0b9df-202">Welke opties beschikbaar zijn in het veld Artikel is afhankelijk van wat u hebt ingesteld in het veld Artikelcode.</span><span class="sxs-lookup"><span data-stu-id="0b9df-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="0b9df-203">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0b9df-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0b9df-204">Vouw de sectie Proces uit of samen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="0b9df-205">Selecteer een optie in het veld Gebeurtenistype.</span><span class="sxs-lookup"><span data-stu-id="0b9df-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="0b9df-206">Dit is de gebeurtenis waarmee de test wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="0b9df-206">This is the event that triggers the test.</span></span> <span data-ttu-id="0b9df-207">Welke opties hier beschikbaar zijn is afhankelijk van het proces dat u hebt geselecteerd in het veld Verwijzingstype.</span><span class="sxs-lookup"><span data-stu-id="0b9df-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="0b9df-208">Selecteer een optie in het veld Uitvoering.</span><span class="sxs-lookup"><span data-stu-id="0b9df-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="0b9df-209">Vouw de sectie Kwaliteitsorderproces uit of samen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="0b9df-210">Klik in het veld Gebeurtenisblokkering op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0b9df-211">In dit veld wordt de lijst weergegeven van processen die kunnen worden geblokkeerd als de kwaliteitsorder nog open staat.</span><span class="sxs-lookup"><span data-stu-id="0b9df-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="0b9df-212">De opties zijn afhankelijk van wat u in het veld Gebeurtenistype hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0b9df-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="0b9df-213">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="0b9df-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0b9df-214">Dit is afhankelijk van de vorige geselecteerde waarden.</span><span class="sxs-lookup"><span data-stu-id="0b9df-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="0b9df-215">Selecteer of de volgende processen moeten worden geblokkeerd terwijl er openstaande kwaliteitsorders aan een brondocumentregel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="0b9df-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="0b9df-216">Vouw de sectie Specificaties uit of samen.</span><span class="sxs-lookup"><span data-stu-id="0b9df-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="0b9df-217">Selecteer in het veld Testgroep de testgroep die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0b9df-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="0b9df-218">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0b9df-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="0b9df-219">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0b9df-219">Click Save.</span></span>
17. <span data-ttu-id="0b9df-220">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0b9df-220">Close the page.</span></span>

