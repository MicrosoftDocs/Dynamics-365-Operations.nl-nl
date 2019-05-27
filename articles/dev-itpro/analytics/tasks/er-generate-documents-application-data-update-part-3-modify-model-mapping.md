---
title: Modellen en toewijzingen wijzigen voor het genereren van documenten die toepassingsgegevens bevatten
description: "Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 2: Documenten genereren)' voltooien."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 580f00faf6694dc2da476ffa75f995d9a24e0f8b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551271"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="4ec1d-103">Modellen en toewijzingen wijzigen voor het genereren van documenten die toepassingsgegevens bevatten</span><span class="sxs-lookup"><span data-stu-id="4ec1d-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ec1d-104">Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 2: documenten genereren)' voltooien.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="4ec1d-105">De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren en toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="4ec1d-106">In deze procedure wijzigt u de ER-configuraties om ze te gaan gebruiken om elektronische documenten te genereren en om toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="4ec1d-107">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="4ec1d-108">Deze stappen kunnen worden voltooid met de DEMF-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="4ec1d-109">Gegevensmodel wijzigen</span><span class="sxs-lookup"><span data-stu-id="4ec1d-109">Modify data model</span></span>
1. <span data-ttu-id="4ec1d-110">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4ec1d-111">Selecteer in de structuur 'Intrastat (model)'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="4ec1d-112">U gaat uitbreiden hoe u het gegevensmodel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-112">You will extend how you use the data model.</span></span> <span data-ttu-id="4ec1d-113">U gebruikt het niet alleen als gegevensbron om het Intrastat-rapport te genereren, maar het gegevensmodel wordt gebruikt voor het verzamelen van gegevens over het Intrastat-rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="4ec1d-114">De details worden vervolgens gebruikt voor het bijwerken van toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="4ec1d-115">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-115">Click Designer.</span></span>
4. <span data-ttu-id="4ec1d-116">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="4ec1d-117">Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".</span><span class="sxs-lookup"><span data-stu-id="4ec1d-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="4ec1d-118">Typ 'Voor update van toepassingsgegevens' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="4ec1d-119">Voor bijwerken van toepassingsgegevens</span><span class="sxs-lookup"><span data-stu-id="4ec1d-119">For application data update</span></span>  
7. <span data-ttu-id="4ec1d-120">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-120">Click Add.</span></span>
8. <span data-ttu-id="4ec1d-121">Selecteer in de structuur 'Voor update van toepassingsgegevens'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="4ec1d-122">Dit nieuwe basisitem wordt toegevoegd om de gegevensstroom op te geven voor het verplaatsen van gegevens door het Intrastat-rapport (gebruikt als gegevensbron) naar de toepassingstabellen (de updatebestemming).</span><span class="sxs-lookup"><span data-stu-id="4ec1d-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="4ec1d-123">Houd er rekening mee dat verschillende basisitems moeten worden gebruikt voor het ophalen van gegevens die worden geboekt naar het uitgaande document en voor het ophalen van gegevens uit het document dat wordt gebruikt om toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="4ec1d-124">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="4ec1d-125">Typ 'Archiefkoptekst' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="4ec1d-126">Archiefkoptekst</span><span class="sxs-lookup"><span data-stu-id="4ec1d-126">Archive header</span></span>  
11. <span data-ttu-id="4ec1d-127">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="4ec1d-128">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-128">Click Add.</span></span>
    * <span data-ttu-id="4ec1d-129">Omdat u een record maakt voor elk Intrastat-rapport dat wordt gegenereerd, moet u er een nieuw item voor maken.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="4ec1d-130">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="4ec1d-131">Typ Bestandsnaam in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="4ec1d-132">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="4ec1d-132">File name</span></span>  
15. <span data-ttu-id="4ec1d-133">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="4ec1d-134">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-134">Click Add.</span></span>
17. <span data-ttu-id="4ec1d-135">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="4ec1d-136">Typ 'Aantal regels' in het naamveld.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="4ec1d-137">Aantal regels</span><span class="sxs-lookup"><span data-stu-id="4ec1d-137">Number of lines</span></span>  
19. <span data-ttu-id="4ec1d-138">Selecteer 'Geheel getal' in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="4ec1d-139">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-139">Click Add.</span></span>
    * <span data-ttu-id="4ec1d-140">Voeg dit item toe om het nummer voor te stellen van Intrastat-transacties die worden gerapporteerd tijdens het huidige rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="4ec1d-141">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="4ec1d-142">Typ 'Archiefregels' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="4ec1d-143">Archiefregels</span><span class="sxs-lookup"><span data-stu-id="4ec1d-143">Archive lines</span></span>  
23. <span data-ttu-id="4ec1d-144">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="4ec1d-145">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-145">Click Add.</span></span>
    * <span data-ttu-id="4ec1d-146">Voeg dit item toe om de lijst voor te stellen van Intrastat-transacties die worden gerapporteerd tijdens het huidige rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="4ec1d-147">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="4ec1d-148">Typ "Amount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="4ec1d-149">Bedrag</span><span class="sxs-lookup"><span data-stu-id="4ec1d-149">Amount</span></span>  
27. <span data-ttu-id="4ec1d-150">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="4ec1d-151">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-151">Click Add.</span></span>
29. <span data-ttu-id="4ec1d-152">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="4ec1d-153">Typ 'Basisproductrecord-id' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="4ec1d-154">Basisproductrecord-id</span><span class="sxs-lookup"><span data-stu-id="4ec1d-154">Commodity rec id</span></span>  
31. <span data-ttu-id="4ec1d-155">Selecteer 'Int64' in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="4ec1d-156">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-156">Click Add.</span></span>
33. <span data-ttu-id="4ec1d-157">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="4ec1d-158">Typ 'Artikelnummer' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="4ec1d-159">artikelnummer</span><span class="sxs-lookup"><span data-stu-id="4ec1d-159">Item number</span></span>  
35. <span data-ttu-id="4ec1d-160">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="4ec1d-161">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-161">Click Add.</span></span>
37. <span data-ttu-id="4ec1d-162">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-162">Click Save.</span></span>
38. <span data-ttu-id="4ec1d-163">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="4ec1d-164">Modeltoewijzing wijzigen</span><span class="sxs-lookup"><span data-stu-id="4ec1d-164">Modify model mapping</span></span>
1. <span data-ttu-id="4ec1d-165">Vouw in de structuur 'Intrastat (model)' uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="4ec1d-166">Selecteer in de structuur 'Intrastat (model)\Intrastat (toewijzing)'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="4ec1d-167">Wijzig de bestaande modeltoewijzing om deze te gaan gebruiken voor de update van toepassingsgegevens en om Intrastat-rapportagedetails te archiveren.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="4ec1d-168">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-168">Click Designer.</span></span>
4. <span data-ttu-id="4ec1d-169">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-169">Click New.</span></span>
5. <span data-ttu-id="4ec1d-170">Typ 'Archief bijwerken' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="4ec1d-171">Archief bijwerken</span><span class="sxs-lookup"><span data-stu-id="4ec1d-171">Update archive</span></span>  
6. <span data-ttu-id="4ec1d-172">Selecteer 'Tot bestemming' in het veld Richting.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="4ec1d-173">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-173">Click Save.</span></span>
    * <span data-ttu-id="4ec1d-174">Deze nieuwe toewijzing geeft de gegevensstroom op voor het verplaatsen van gegevens (Intrastat-rapportagedetails) van het gegevensmodel naar de toepassingstabellen (de updatebestemming).</span><span class="sxs-lookup"><span data-stu-id="4ec1d-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="4ec1d-175">Houd er rekening mee dat verschillende basisitems moeten worden gebruikt om gegevens op te halen uit de toepassing voor het rapportageproces en gebruik vervolgens de gegevens uit het gegevensmodel voor de update van de toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="4ec1d-176">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-176">Click Designer.</span></span>
9. <span data-ttu-id="4ec1d-177">Selecteer in de structuur 'Gegevensmodel\Gegevensmodel'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="4ec1d-178">Voeg de vereiste gegevensbron toe.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-178">Add the required data source.</span></span> <span data-ttu-id="4ec1d-179">Dit is het gegevensmodel dat gegevens bevat van de gerapporteerde Intrastat-transacties die moeten worden gearchiveerd.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="4ec1d-180">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-180">Click Add root.</span></span>
11. <span data-ttu-id="4ec1d-181">Typ 'model' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="4ec1d-182">model</span><span class="sxs-lookup"><span data-stu-id="4ec1d-182">model</span></span>  
12. <span data-ttu-id="4ec1d-183">Typ of selecteer in het veld Definitie de waarde voor 'Voor gegevensupdate van toepassing'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="4ec1d-184">Voor bijwerken van toepassingsgegevens</span><span class="sxs-lookup"><span data-stu-id="4ec1d-184">For application data update</span></span>  
13. <span data-ttu-id="4ec1d-185">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-185">Click OK.</span></span>
14. <span data-ttu-id="4ec1d-186">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="4ec1d-187">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="4ec1d-188">Selecteer 'model\Archiefkoptekst' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="4ec1d-189">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-189">Click Add.</span></span>
    * <span data-ttu-id="4ec1d-190">Omdat u gerapporteerde Intrastat-transacties gaat opsommen voor archivering, moet de juiste gegevensbron worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="4ec1d-191">Typ 'Vaste regels' in het naamveld.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="4ec1d-192">Vaste regels</span><span class="sxs-lookup"><span data-stu-id="4ec1d-192">Enumerated lines</span></span>  
19. <span data-ttu-id="4ec1d-193">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-193">Click Edit formula.</span></span>
20. <span data-ttu-id="4ec1d-194">Selecteer in de structuur 'Lijst\ENUMERATE'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="4ec1d-195">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-195">Click Add function.</span></span>
22. <span data-ttu-id="4ec1d-196">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="4ec1d-197">Vouw in de structuur 'model\Archiefkoptekst' uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="4ec1d-198">Selecteer 'model\Archiefkoptekst\Archiefregels' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="4ec1d-199">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-199">Click Add data source.</span></span>
26. <span data-ttu-id="4ec1d-200">Voer in het formuleveld 'ENUMERATE (model.'Archiefkoptekst'.'Archiefregels')' in.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="4ec1d-201">ENUMERATE(model. 'Archiefkoptekst'.'Archiefregels')</span><span class="sxs-lookup"><span data-stu-id="4ec1d-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="4ec1d-202">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-202">Click Save.</span></span>
28. <span data-ttu-id="4ec1d-203">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-203">Close the page.</span></span>
29. <span data-ttu-id="4ec1d-204">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-204">Click OK.</span></span>
30. <span data-ttu-id="4ec1d-205">Klik op Bestemming toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-205">Click Add destination.</span></span>
    * <span data-ttu-id="4ec1d-206">Voeg toepassingstabellen toe als vereiste bestemmingen die updates vereisen om details te archiveren van gerapporteerde Intrastat-transacties.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="4ec1d-207">Typ in het veld Naam 'Archief'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="4ec1d-208">Archiveren</span><span class="sxs-lookup"><span data-stu-id="4ec1d-208">Archive</span></span>  
32. <span data-ttu-id="4ec1d-209">Typ in het veld Tabel 'IntrastatArchiveGeneral'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="4ec1d-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="4ec1d-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="4ec1d-211">Houd de recordactie 'Invoegen', zodat u records kunt toevoegen tijdens de detailarchivering van elk Intrastat-rapportageproces.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="4ec1d-212">Selecteer Ja in het veld Infolog registreren.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="4ec1d-213">Selecteer Ja om informatie te krijgen over problemen met de update van toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="4ec1d-214">Selecteer Ja in het veld Validatie van actie registreren overslaan.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="4ec1d-215">Selecteer Ja als u validatiefouten wilt onderdrukken over het lege veld 'Intrastat-archief-id'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="4ec1d-216">Dit wordt gedaan nadat records zijn toegevoegd, op basis van de numerieke reeksvolgorde-instellingen die zijn geconfigureerd voor deze tabel in het parameterformulier voor buitenlandse handel.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="4ec1d-217">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-217">Click OK.</span></span>
    * <span data-ttu-id="4ec1d-218">Bind elementen van de toegevoegde gegevensbron (het gefilterde model op basis van het geselecteerde hoofditem) met elementen uit de toegevoegde bestemming.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="4ec1d-219">Vouw in de structuur 'Archief' uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="4ec1d-220">Vouw in de structuur 'Archief\<Relaties' uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="4ec1d-221">Vouw in de structuur 'Archief\<Relaties\IntrastatArchiveDetail' uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="4ec1d-222">Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Bedrag(AmountMST)'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="4ec1d-223">Vouw in de structuur 'model\Archiefkoptekst\Vaste regels' uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="4ec1d-224">Vouw in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde' uit.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="4ec1d-225">Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Bedrag'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="4ec1d-226">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-226">Click Bind.</span></span>
44. <span data-ttu-id="4ec1d-227">Selecteer in de structuur 'Archief\<Relaties\Intrastat\ArchiveDetail\Basisproduct(IntrastatCommodity)'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="4ec1d-228">Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Basisproductrecord-id'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="4ec1d-229">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-229">Click Bind.</span></span>
47. <span data-ttu-id="4ec1d-230">Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Artikelnummer(ItemId)'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="4ec1d-231">Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Artikelnummer'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="4ec1d-232">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-232">Click Bind.</span></span>
50. <span data-ttu-id="4ec1d-233">Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Regelnummer(Regelnummer)'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="4ec1d-234">Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Getal'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="4ec1d-235">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-235">Click Bind.</span></span>
53. <span data-ttu-id="4ec1d-236">Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="4ec1d-237">Selecteer 'model\Archiefkoptekst\Vaste regels' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="4ec1d-238">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-238">Click Bind.</span></span>
56. <span data-ttu-id="4ec1d-239">Selecteer in de structuur 'Archief\Bestandsnaam(Bestandsnaam)'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="4ec1d-240">Selecteer 'model\Archiefkoptekst\Bestandsnaam' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="4ec1d-241">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-241">Click Bind.</span></span>
59. <span data-ttu-id="4ec1d-242">Selecteer in de structuur 'Archief\Aantal regels(AantalRegels)'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="4ec1d-243">Selecteer 'model\Archiefkoptekst\Aantal regels' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="4ec1d-244">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-244">Click Bind.</span></span>
62. <span data-ttu-id="4ec1d-245">Selecteer in de structuur 'Archief'.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="4ec1d-246">Selecteer 'model\Archiefkoptekst' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="4ec1d-247">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-247">Click Bind.</span></span>
65. <span data-ttu-id="4ec1d-248">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-248">Click Save.</span></span>
66. <span data-ttu-id="4ec1d-249">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-249">Close the page.</span></span>
67. <span data-ttu-id="4ec1d-250">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4ec1d-250">Close the page.</span></span>

