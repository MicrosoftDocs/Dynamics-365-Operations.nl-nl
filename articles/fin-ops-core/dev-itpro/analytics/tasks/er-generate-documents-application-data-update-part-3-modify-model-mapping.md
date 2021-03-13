---
title: Modellen en toewijzingen wijzigen voor het genereren van documenten die toepassingsgegevens bevatten
description: Dit onderwerp laat zien hoe u rapportageconfiguraties ontwerpt voor het genereren van elektronische documenten en bijwerken van toepassingsgevens. (Deel 2 - documenten genereren).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 025429c8e6775d20634703853df04d63c0651b98
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092892"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="a15eb-104">Modellen en toewijzingen wijzigen voor het genereren van documenten die toepassingsgegevens bevatten</span><span class="sxs-lookup"><span data-stu-id="a15eb-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a15eb-105">Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure "ER Documenten genereren met update van toepassingsgegevens (deel 2: Documenten genereren)" voltooien.</span><span class="sxs-lookup"><span data-stu-id="a15eb-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="a15eb-106">De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren en toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="a15eb-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="a15eb-107">In deze procedure wijzigt u de ER-configuraties om ze te gaan gebruiken om elektronische documenten te genereren en om toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="a15eb-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="a15eb-108">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="a15eb-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="a15eb-109">Deze stappen kunnen worden voltooid met de DEMF-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="a15eb-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="a15eb-110">Gegevensmodel wijzigen</span><span class="sxs-lookup"><span data-stu-id="a15eb-110">Modify data model</span></span>
1. <span data-ttu-id="a15eb-111">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="a15eb-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a15eb-112">Selecteer in de structuur 'Intrastat (model)'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="a15eb-113">U gaat uitbreiden hoe u het gegevensmodel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a15eb-113">You will extend how you use the data model.</span></span> <span data-ttu-id="a15eb-114">U gebruikt het niet alleen als gegevensbron om het Intrastat-rapport te genereren, maar het gegevensmodel wordt gebruikt voor het verzamelen van gegevens over het Intrastat-rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="a15eb-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="a15eb-115">De details worden vervolgens gebruikt voor het bijwerken van toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="a15eb-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="a15eb-116">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="a15eb-116">Click Designer.</span></span>
4. <span data-ttu-id="a15eb-117">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="a15eb-118">Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".</span><span class="sxs-lookup"><span data-stu-id="a15eb-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="a15eb-119">Typ 'Voor update van toepassingsgegevens' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="a15eb-120">Voor bijwerken van toepassingsgegevens</span><span class="sxs-lookup"><span data-stu-id="a15eb-120">For application data update</span></span>  
7. <span data-ttu-id="a15eb-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-121">Click Add.</span></span>
8. <span data-ttu-id="a15eb-122">Selecteer in de structuur 'Voor update van toepassingsgegevens'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="a15eb-123">Dit nieuwe basisitem wordt toegevoegd om de gegevensstroom op te geven voor het verplaatsen van gegevens door het Intrastat-rapport (gebruikt als gegevensbron) naar de toepassingstabellen (de updatebestemming).</span><span class="sxs-lookup"><span data-stu-id="a15eb-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="a15eb-124">Houd er rekening mee dat verschillende basisitems moeten worden gebruikt voor het ophalen van gegevens die worden geboekt naar het uitgaande document en voor het ophalen van gegevens uit het document dat wordt gebruikt om toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="a15eb-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="a15eb-125">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="a15eb-126">Typ 'Archiefkoptekst' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="a15eb-127">Archiefkoptekst</span><span class="sxs-lookup"><span data-stu-id="a15eb-127">Archive header</span></span>  
11. <span data-ttu-id="a15eb-128">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="a15eb-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="a15eb-129">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-129">Click Add.</span></span>
    * <span data-ttu-id="a15eb-130">Omdat u een record maakt voor elk Intrastat-rapport dat wordt gegenereerd, moet u er een nieuw item voor maken.</span><span class="sxs-lookup"><span data-stu-id="a15eb-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="a15eb-131">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="a15eb-132">Typ Bestandsnaam in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="a15eb-133">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="a15eb-133">File name</span></span>  
15. <span data-ttu-id="a15eb-134">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="a15eb-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="a15eb-135">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-135">Click Add.</span></span>
17. <span data-ttu-id="a15eb-136">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="a15eb-137">Typ 'Aantal regels' in het naamveld.</span><span class="sxs-lookup"><span data-stu-id="a15eb-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="a15eb-138">Aantal regels</span><span class="sxs-lookup"><span data-stu-id="a15eb-138">Number of lines</span></span>  
19. <span data-ttu-id="a15eb-139">Selecteer 'Geheel getal' in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="a15eb-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="a15eb-140">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-140">Click Add.</span></span>
    * <span data-ttu-id="a15eb-141">Voeg dit item toe om het nummer voor te stellen van Intrastat-transacties die worden gerapporteerd tijdens het huidige rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="a15eb-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="a15eb-142">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="a15eb-143">Typ 'Archiefregels' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="a15eb-144">Archiefregels</span><span class="sxs-lookup"><span data-stu-id="a15eb-144">Archive lines</span></span>  
23. <span data-ttu-id="a15eb-145">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="a15eb-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="a15eb-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-146">Click Add.</span></span>
    * <span data-ttu-id="a15eb-147">Voeg dit item toe om de lijst voor te stellen van Intrastat-transacties die worden gerapporteerd tijdens het huidige rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="a15eb-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="a15eb-148">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="a15eb-149">Typ "Amount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="a15eb-150">Bedrag</span><span class="sxs-lookup"><span data-stu-id="a15eb-150">Amount</span></span>  
27. <span data-ttu-id="a15eb-151">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="a15eb-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="a15eb-152">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-152">Click Add.</span></span>
29. <span data-ttu-id="a15eb-153">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="a15eb-154">Typ 'Basisproductrecord-id' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="a15eb-155">Basisproductrecord-id</span><span class="sxs-lookup"><span data-stu-id="a15eb-155">Commodity rec id</span></span>  
31. <span data-ttu-id="a15eb-156">Selecteer 'Int64' in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="a15eb-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="a15eb-157">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-157">Click Add.</span></span>
33. <span data-ttu-id="a15eb-158">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="a15eb-159">Typ 'Artikelnummer' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="a15eb-160">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="a15eb-160">Item number</span></span>  
35. <span data-ttu-id="a15eb-161">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="a15eb-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="a15eb-162">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-162">Click Add.</span></span>
37. <span data-ttu-id="a15eb-163">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a15eb-163">Click Save.</span></span>
38. <span data-ttu-id="a15eb-164">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a15eb-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="a15eb-165">Modeltoewijzing wijzigen</span><span class="sxs-lookup"><span data-stu-id="a15eb-165">Modify model mapping</span></span>
1. <span data-ttu-id="a15eb-166">Vouw in de structuur 'Intrastat (model)' uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="a15eb-167">Selecteer in de structuur 'Intrastat (model)\Intrastat (toewijzing)'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="a15eb-168">Wijzig de bestaande modeltoewijzing om deze te gaan gebruiken voor de update van toepassingsgegevens en om Intrastat-rapportagedetails te archiveren.</span><span class="sxs-lookup"><span data-stu-id="a15eb-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="a15eb-169">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="a15eb-169">Click Designer.</span></span>
4. <span data-ttu-id="a15eb-170">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a15eb-170">Click New.</span></span>
5. <span data-ttu-id="a15eb-171">Typ 'Archief bijwerken' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="a15eb-172">Archief bijwerken</span><span class="sxs-lookup"><span data-stu-id="a15eb-172">Update archive</span></span>  
6. <span data-ttu-id="a15eb-173">Selecteer 'Tot bestemming' in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="a15eb-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="a15eb-174">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a15eb-174">Click Save.</span></span>
    * <span data-ttu-id="a15eb-175">Deze nieuwe toewijzing geeft de gegevensstroom op voor het verplaatsen van gegevens (Intrastat-rapportagedetails) van het gegevensmodel naar de toepassingstabellen (de updatebestemming).</span><span class="sxs-lookup"><span data-stu-id="a15eb-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="a15eb-176">Houd er rekening mee dat verschillende basisitems moeten worden gebruikt om gegevens op te halen uit de toepassing voor het rapportageproces en gebruik vervolgens de gegevens uit het gegevensmodel voor de update van de toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="a15eb-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="a15eb-177">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="a15eb-177">Click Designer.</span></span>
9. <span data-ttu-id="a15eb-178">Selecteer in de structuur 'Gegevensmodel\Gegevensmodel'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="a15eb-179">Voeg de vereiste gegevensbron toe.</span><span class="sxs-lookup"><span data-stu-id="a15eb-179">Add the required data source.</span></span> <span data-ttu-id="a15eb-180">Dit is het gegevensmodel dat gegevens bevat van de gerapporteerde Intrastat-transacties die moeten worden gearchiveerd.</span><span class="sxs-lookup"><span data-stu-id="a15eb-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="a15eb-181">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-181">Click Add root.</span></span>
11. <span data-ttu-id="a15eb-182">Typ 'model' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a15eb-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="a15eb-183">model</span><span class="sxs-lookup"><span data-stu-id="a15eb-183">model</span></span>  
12. <span data-ttu-id="a15eb-184">Typ of selecteer in het veld Definitie de waarde voor 'Voor gegevensupdate van toepassing'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="a15eb-185">Voor bijwerken van toepassingsgegevens</span><span class="sxs-lookup"><span data-stu-id="a15eb-185">For application data update</span></span>  
13. <span data-ttu-id="a15eb-186">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a15eb-186">Click OK.</span></span>
14. <span data-ttu-id="a15eb-187">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="a15eb-188">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a15eb-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="a15eb-189">Selecteer 'model\Archiefkoptekst' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a15eb-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="a15eb-190">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-190">Click Add.</span></span>
    * <span data-ttu-id="a15eb-191">Omdat u gerapporteerde Intrastat-transacties gaat opsommen voor archivering, moet de juiste gegevensbron worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="a15eb-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="a15eb-192">Typ 'Vaste regels' in het naamveld.</span><span class="sxs-lookup"><span data-stu-id="a15eb-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="a15eb-193">Vaste regels</span><span class="sxs-lookup"><span data-stu-id="a15eb-193">Enumerated lines</span></span>  
19. <span data-ttu-id="a15eb-194">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="a15eb-194">Click Edit formula.</span></span>
20. <span data-ttu-id="a15eb-195">Selecteer in de structuur 'Lijst\ENUMERATE'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="a15eb-196">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-196">Click Add function.</span></span>
22. <span data-ttu-id="a15eb-197">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="a15eb-198">Vouw in de structuur 'model\Archiefkoptekst' uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="a15eb-199">Selecteer 'model\Archiefkoptekst\Archiefregels' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a15eb-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="a15eb-200">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-200">Click Add data source.</span></span>
26. <span data-ttu-id="a15eb-201">Voer in het formuleveld 'ENUMERATE (model.'Archiefkoptekst'.'Archiefregels')' in.</span><span class="sxs-lookup"><span data-stu-id="a15eb-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="a15eb-202">ENUMERATE(model. 'Archiefkoptekst'.'Archiefregels')</span><span class="sxs-lookup"><span data-stu-id="a15eb-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="a15eb-203">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a15eb-203">Click Save.</span></span>
28. <span data-ttu-id="a15eb-204">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a15eb-204">Close the page.</span></span>
29. <span data-ttu-id="a15eb-205">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a15eb-205">Click OK.</span></span>
30. <span data-ttu-id="a15eb-206">Klik op Bestemming toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a15eb-206">Click Add destination.</span></span>
    * <span data-ttu-id="a15eb-207">Voeg toepassingstabellen toe als vereiste bestemmingen die updates vereisen om details te archiveren van gerapporteerde Intrastat-transacties.</span><span class="sxs-lookup"><span data-stu-id="a15eb-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="a15eb-208">Typ in het veld Naam 'Archief'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="a15eb-209">Archiveren</span><span class="sxs-lookup"><span data-stu-id="a15eb-209">Archive</span></span>  
32. <span data-ttu-id="a15eb-210">Typ in het veld Tabel 'IntrastatArchiveGeneral'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="a15eb-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="a15eb-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="a15eb-212">Houd de recordactie 'Invoegen', zodat u records kunt toevoegen tijdens de detailarchivering van elk Intrastat-rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="a15eb-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="a15eb-213">Selecteer Ja in het veld Infolog registreren.</span><span class="sxs-lookup"><span data-stu-id="a15eb-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="a15eb-214">Selecteer Ja om informatie te krijgen over problemen met de update van toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="a15eb-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="a15eb-215">Selecteer Ja in het veld Validatie van actie registreren overslaan.</span><span class="sxs-lookup"><span data-stu-id="a15eb-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="a15eb-216">Selecteer Ja als u validatiefouten wilt onderdrukken over het lege veld 'Intrastat-archief-id'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="a15eb-217">Dit wordt gedaan nadat records zijn toegevoegd, op basis van de numerieke reeksvolgorde-instellingen die zijn geconfigureerd voor deze tabel in het parameterformulier voor buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="a15eb-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="a15eb-218">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a15eb-218">Click OK.</span></span>
    * <span data-ttu-id="a15eb-219">Bind elementen van de toegevoegde gegevensbron (het gefilterde model op basis van het geselecteerde hoofditem) met elementen uit de toegevoegde bestemming.</span><span class="sxs-lookup"><span data-stu-id="a15eb-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="a15eb-220">Vouw in de structuur 'Archief' uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="a15eb-221">Vouw in de structuur 'Archief\<Relaties' uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="a15eb-222">Vouw in de structuur 'Archief\<Relaties\IntrastatArchiveDetail' uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="a15eb-223">Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Bedrag(AmountMST)'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="a15eb-224">Vouw in de structuur 'model\Archiefkoptekst\Vaste regels' uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="a15eb-225">Vouw in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde' uit.</span><span class="sxs-lookup"><span data-stu-id="a15eb-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="a15eb-226">Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Bedrag'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="a15eb-227">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a15eb-227">Click Bind.</span></span>
44. <span data-ttu-id="a15eb-228">Selecteer in de structuur 'Archief\<Relaties\Intrastat\ArchiveDetail\Basisproduct(IntrastatCommodity)'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="a15eb-229">Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Basisproductrecord-id'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="a15eb-230">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a15eb-230">Click Bind.</span></span>
47. <span data-ttu-id="a15eb-231">Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Artikelnummer(ItemId)'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="a15eb-232">Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Artikelnummer'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="a15eb-233">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a15eb-233">Click Bind.</span></span>
50. <span data-ttu-id="a15eb-234">Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Regelnummer(Regelnummer)'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="a15eb-235">Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Getal'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="a15eb-236">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a15eb-236">Click Bind.</span></span>
53. <span data-ttu-id="a15eb-237">Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="a15eb-238">Selecteer 'model\Archiefkoptekst\Vaste regels' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a15eb-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="a15eb-239">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a15eb-239">Click Bind.</span></span>
56. <span data-ttu-id="a15eb-240">Selecteer in de structuur 'Archief\Bestandsnaam(Bestandsnaam)'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="a15eb-241">Selecteer 'model\Archiefkoptekst\Bestandsnaam' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a15eb-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="a15eb-242">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a15eb-242">Click Bind.</span></span>
59. <span data-ttu-id="a15eb-243">Selecteer in de structuur 'Archief\Aantal regels(AantalRegels)'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="a15eb-244">Selecteer 'model\Archiefkoptekst\Aantal regels' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a15eb-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="a15eb-245">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a15eb-245">Click Bind.</span></span>
62. <span data-ttu-id="a15eb-246">Selecteer in de structuur 'Archief'.</span><span class="sxs-lookup"><span data-stu-id="a15eb-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="a15eb-247">Selecteer 'model\Archiefkoptekst' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a15eb-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="a15eb-248">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a15eb-248">Click Bind.</span></span>
65. <span data-ttu-id="a15eb-249">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a15eb-249">Click Save.</span></span>
66. <span data-ttu-id="a15eb-250">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a15eb-250">Close the page.</span></span>
67. <span data-ttu-id="a15eb-251">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a15eb-251">Close the page.</span></span>

