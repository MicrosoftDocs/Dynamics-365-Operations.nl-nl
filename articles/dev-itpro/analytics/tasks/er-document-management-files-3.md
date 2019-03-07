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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "362942"
---
# <a name="create-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="33bb1-103">Indelingen maken voor gebruik van documentbeheerbestanden in ER-uitvoer</span><span class="sxs-lookup"><span data-stu-id="33bb1-103">Create formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33bb1-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="33bb1-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="33bb1-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="33bb1-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="33bb1-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 2: Gegevensmodel uitbreiden)".</span><span class="sxs-lookup"><span data-stu-id="33bb1-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="33bb1-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="33bb1-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="33bb1-108">Maak een indeling om facturen te verwerken</span><span class="sxs-lookup"><span data-stu-id="33bb1-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="33bb1-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="33bb1-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="33bb1-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="33bb1-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="33bb1-111">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="33bb1-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="33bb1-112">Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).</span><span class="sxs-lookup"><span data-stu-id="33bb1-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="33bb1-113">U maakt een indeling om elektronische berichten te genereren met informatie over de bestanden die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.</span><span class="sxs-lookup"><span data-stu-id="33bb1-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="33bb1-114">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="33bb1-115">Typ Indeling gebaseerd op gegevensmodel Klantfactuurmodel (aangepast) in het veld Nieuw.</span><span class="sxs-lookup"><span data-stu-id="33bb1-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="33bb1-116">Typ Voorbeeldbericht elektronische factuur in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="33bb1-117">Voorbeeldbericht elektronische factuur</span><span class="sxs-lookup"><span data-stu-id="33bb1-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="33bb1-118">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="33bb1-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="33bb1-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="33bb1-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="33bb1-120">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="33bb1-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="33bb1-121">Ontwerp een indeling om bijlagen te vullen om een bericht in MIME-indeling te genereren</span><span class="sxs-lookup"><span data-stu-id="33bb1-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="33bb1-122">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="33bb1-122">Click Designer.</span></span>
2. <span data-ttu-id="33bb1-123">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="33bb1-124">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="33bb1-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="33bb1-125">Typ Factuur in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="33bb1-126">Factuur</span><span class="sxs-lookup"><span data-stu-id="33bb1-126">Invoice</span></span>  
5. <span data-ttu-id="33bb1-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-127">Click OK.</span></span>
6. <span data-ttu-id="33bb1-128">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="33bb1-129">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="33bb1-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="33bb1-130">Typ SalesOrder in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="33bb1-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="33bb1-131">SalesOrder</span></span>  
9. <span data-ttu-id="33bb1-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-132">Click OK.</span></span>
10. <span data-ttu-id="33bb1-133">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="33bb1-134">Typ InvoiceNumber in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="33bb1-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="33bb1-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="33bb1-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-136">Click OK.</span></span>
13. <span data-ttu-id="33bb1-137">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="33bb1-138">Typ InvoiceAmount in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="33bb1-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="33bb1-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="33bb1-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-140">Click OK.</span></span>
16. <span data-ttu-id="33bb1-141">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="33bb1-142">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="33bb1-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="33bb1-143">Typ EnclosedDocs in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="33bb1-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="33bb1-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="33bb1-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-145">Click OK.</span></span>
20. <span data-ttu-id="33bb1-146">Selecteer in de structuur Factuur\EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="33bb1-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="33bb1-147">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-147">Click Add Element.</span></span>
22. <span data-ttu-id="33bb1-148">Typ Document in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="33bb1-149">Document</span><span class="sxs-lookup"><span data-stu-id="33bb1-149">Document</span></span>  
23. <span data-ttu-id="33bb1-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-150">Click OK.</span></span>
24. <span data-ttu-id="33bb1-151">Selecteer in de structuur Factuur\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="33bb1-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="33bb1-152">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="33bb1-153">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="33bb1-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="33bb1-154">Typ FileName in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="33bb1-155">FileName</span><span class="sxs-lookup"><span data-stu-id="33bb1-155">FileName</span></span>  
28. <span data-ttu-id="33bb1-156">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-156">Click OK.</span></span>
29. <span data-ttu-id="33bb1-157">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="33bb1-158">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="33bb1-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="33bb1-159">Typ FileContent in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="33bb1-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="33bb1-160">FileContent</span></span>  
32. <span data-ttu-id="33bb1-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-161">Click OK.</span></span>
33. <span data-ttu-id="33bb1-162">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent.</span><span class="sxs-lookup"><span data-stu-id="33bb1-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="33bb1-163">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="33bb1-164">Selecteer Tekst\Base64 in de structuur.</span><span class="sxs-lookup"><span data-stu-id="33bb1-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="33bb1-165">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="33bb1-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="33bb1-166">Indelingselementen aan gegevensmodel toewijzen als gegevensbron</span><span class="sxs-lookup"><span data-stu-id="33bb1-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="33bb1-167">Selecteer in de structuur Factuur\SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="33bb1-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="33bb1-168">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="33bb1-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="33bb1-169">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="33bb1-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="33bb1-170">Selecteer in de structuur Model\Verkoopordernummer (Salesid).</span><span class="sxs-lookup"><span data-stu-id="33bb1-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="33bb1-171">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="33bb1-171">Click Bind.</span></span>
6. <span data-ttu-id="33bb1-172">Selecteer in de structuur Factuur\InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="33bb1-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="33bb1-173">Vouw in de structuur model\Base invoice(InvoiceBase) uit.</span><span class="sxs-lookup"><span data-stu-id="33bb1-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="33bb1-174">Selecteer in de structuur model\Base invoice(InvoiceBase\Factuurnummer(Id).</span><span class="sxs-lookup"><span data-stu-id="33bb1-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="33bb1-175">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="33bb1-175">Click Bind.</span></span>
10. <span data-ttu-id="33bb1-176">Selecteer in de structuur Factuur\InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="33bb1-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="33bb1-177">Selecteer in de structuur model\Base invoice(InvoiceBase\Factuurbedrag(Amount).</span><span class="sxs-lookup"><span data-stu-id="33bb1-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="33bb1-178">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="33bb1-178">Click Bind.</span></span>
13. <span data-ttu-id="33bb1-179">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="33bb1-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="33bb1-180">Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="33bb1-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="33bb1-181">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\Base64.</span><span class="sxs-lookup"><span data-stu-id="33bb1-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="33bb1-182">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="33bb1-182">Click Bind.</span></span>
17. <span data-ttu-id="33bb1-183">Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="33bb1-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="33bb1-184">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\FileName.</span><span class="sxs-lookup"><span data-stu-id="33bb1-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="33bb1-185">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="33bb1-185">Click Bind.</span></span>
20. <span data-ttu-id="33bb1-186">Selecteer in de structuur model\Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="33bb1-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="33bb1-187">Selecteer in de structuur Factuur\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="33bb1-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="33bb1-188">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="33bb1-188">Click Bind.</span></span>
23. <span data-ttu-id="33bb1-189">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="33bb1-189">Click Save.</span></span>
24. <span data-ttu-id="33bb1-190">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="33bb1-190">Close the page.</span></span>

