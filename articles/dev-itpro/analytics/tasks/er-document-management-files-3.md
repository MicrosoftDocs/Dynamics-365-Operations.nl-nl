---
title: Indelingen maken voor gebruik van documentbeheerbestanden in ER-uitvoer
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de documentbeheerbestanden in ER-uitvoer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1815a0004eee6734b3c7d2c2f9e75ce5fe16af1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544743"
---
# <a name="create-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="4605d-103">Indelingen maken voor gebruik van documentbeheerbestanden in ER-uitvoer</span><span class="sxs-lookup"><span data-stu-id="4605d-103">Create formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4605d-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="4605d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="4605d-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4605d-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="4605d-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 2: Gegevensmodel uitbreiden)".</span><span class="sxs-lookup"><span data-stu-id="4605d-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="4605d-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="4605d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="4605d-108">Maak een indeling om facturen te verwerken</span><span class="sxs-lookup"><span data-stu-id="4605d-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="4605d-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="4605d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4605d-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="4605d-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4605d-111">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="4605d-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="4605d-112">Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).</span><span class="sxs-lookup"><span data-stu-id="4605d-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="4605d-113">U maakt een indeling om elektronische berichten te genereren met informatie over de bestanden die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.</span><span class="sxs-lookup"><span data-stu-id="4605d-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="4605d-114">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="4605d-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="4605d-115">Typ Indeling gebaseerd op gegevensmodel Klantfactuurmodel (aangepast) in het veld Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4605d-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="4605d-116">Typ Voorbeeldbericht elektronische factuur in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="4605d-117">Voorbeeldbericht elektronische factuur</span><span class="sxs-lookup"><span data-stu-id="4605d-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="4605d-118">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="4605d-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="4605d-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="4605d-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="4605d-120">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="4605d-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="4605d-121">Ontwerp een indeling om bijlagen te vullen om een bericht in MIME-indeling te genereren</span><span class="sxs-lookup"><span data-stu-id="4605d-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="4605d-122">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="4605d-122">Click Designer.</span></span>
2. <span data-ttu-id="4605d-123">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="4605d-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="4605d-124">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4605d-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="4605d-125">Typ Factuur in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="4605d-126">Factuur</span><span class="sxs-lookup"><span data-stu-id="4605d-126">Invoice</span></span>  
5. <span data-ttu-id="4605d-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-127">Click OK.</span></span>
6. <span data-ttu-id="4605d-128">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4605d-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="4605d-129">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4605d-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="4605d-130">Typ SalesOrder in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="4605d-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="4605d-131">SalesOrder</span></span>  
9. <span data-ttu-id="4605d-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-132">Click OK.</span></span>
10. <span data-ttu-id="4605d-133">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4605d-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="4605d-134">Typ InvoiceNumber in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="4605d-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="4605d-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="4605d-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-136">Click OK.</span></span>
13. <span data-ttu-id="4605d-137">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4605d-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="4605d-138">Typ InvoiceAmount in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="4605d-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="4605d-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="4605d-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-140">Click OK.</span></span>
16. <span data-ttu-id="4605d-141">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4605d-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="4605d-142">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4605d-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="4605d-143">Typ EnclosedDocs in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="4605d-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="4605d-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="4605d-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-145">Click OK.</span></span>
20. <span data-ttu-id="4605d-146">Selecteer in de structuur Factuur\EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="4605d-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="4605d-147">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4605d-147">Click Add Element.</span></span>
22. <span data-ttu-id="4605d-148">Typ Document in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="4605d-149">Document</span><span class="sxs-lookup"><span data-stu-id="4605d-149">Document</span></span>  
23. <span data-ttu-id="4605d-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-150">Click OK.</span></span>
24. <span data-ttu-id="4605d-151">Selecteer in de structuur Factuur\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="4605d-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="4605d-152">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4605d-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="4605d-153">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4605d-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="4605d-154">Typ FileName in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="4605d-155">FileName</span><span class="sxs-lookup"><span data-stu-id="4605d-155">FileName</span></span>  
28. <span data-ttu-id="4605d-156">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-156">Click OK.</span></span>
29. <span data-ttu-id="4605d-157">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4605d-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="4605d-158">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4605d-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="4605d-159">Typ FileContent in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="4605d-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="4605d-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="4605d-160">FileContent</span></span>  
32. <span data-ttu-id="4605d-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-161">Click OK.</span></span>
33. <span data-ttu-id="4605d-162">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent.</span><span class="sxs-lookup"><span data-stu-id="4605d-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="4605d-163">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="4605d-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="4605d-164">Selecteer Tekst\Base64 in de structuur.</span><span class="sxs-lookup"><span data-stu-id="4605d-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="4605d-165">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4605d-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="4605d-166">Indelingselementen aan gegevensmodel toewijzen als gegevensbron</span><span class="sxs-lookup"><span data-stu-id="4605d-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="4605d-167">Selecteer in de structuur Factuur\SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="4605d-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="4605d-168">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="4605d-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="4605d-169">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="4605d-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="4605d-170">Selecteer in de structuur Model\Verkoopordernummer (Salesid).</span><span class="sxs-lookup"><span data-stu-id="4605d-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="4605d-171">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4605d-171">Click Bind.</span></span>
6. <span data-ttu-id="4605d-172">Selecteer in de structuur Factuur\InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="4605d-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="4605d-173">Vouw in de structuur model\Base invoice(InvoiceBase) uit.</span><span class="sxs-lookup"><span data-stu-id="4605d-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="4605d-174">Selecteer in de structuur model\Base invoice(InvoiceBase\Factuurnummer(Id).</span><span class="sxs-lookup"><span data-stu-id="4605d-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="4605d-175">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4605d-175">Click Bind.</span></span>
10. <span data-ttu-id="4605d-176">Selecteer in de structuur Factuur\InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="4605d-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="4605d-177">Selecteer in de structuur model\Base invoice(InvoiceBase\Factuurbedrag(Amount).</span><span class="sxs-lookup"><span data-stu-id="4605d-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="4605d-178">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4605d-178">Click Bind.</span></span>
13. <span data-ttu-id="4605d-179">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="4605d-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="4605d-180">Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="4605d-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="4605d-181">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\Base64.</span><span class="sxs-lookup"><span data-stu-id="4605d-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="4605d-182">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4605d-182">Click Bind.</span></span>
17. <span data-ttu-id="4605d-183">Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="4605d-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="4605d-184">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\FileName.</span><span class="sxs-lookup"><span data-stu-id="4605d-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="4605d-185">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4605d-185">Click Bind.</span></span>
20. <span data-ttu-id="4605d-186">Selecteer in de structuur model\Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="4605d-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="4605d-187">Selecteer in de structuur Factuur\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="4605d-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="4605d-188">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="4605d-188">Click Bind.</span></span>
23. <span data-ttu-id="4605d-189">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4605d-189">Click Save.</span></span>
24. <span data-ttu-id="4605d-190">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4605d-190">Close the page.</span></span>

