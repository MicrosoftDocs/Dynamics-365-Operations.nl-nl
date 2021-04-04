---
title: ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 3 - Indeling maken)
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage configureert om documentbeheerbestanden te gebruiken in ER-uitvoer. (Deel 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec1ebc15cd980734aebec63d6758404868c1e36
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559744"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="a7bdd-104">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 3 - Indeling maken)</span><span class="sxs-lookup"><span data-stu-id="a7bdd-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7bdd-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="a7bdd-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a7bdd-107">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 2: Gegevensmodel uitbreiden)".</span><span class="sxs-lookup"><span data-stu-id="a7bdd-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="a7bdd-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="a7bdd-109">Maak een indeling om facturen te verwerken</span><span class="sxs-lookup"><span data-stu-id="a7bdd-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="a7bdd-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a7bdd-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a7bdd-112">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="a7bdd-113">Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="a7bdd-114">U maakt een indeling om elektronische berichten te genereren met informatie over de bestanden die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="a7bdd-115">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="a7bdd-116">Typ Indeling gebaseerd op gegevensmodel Klantfactuurmodel (aangepast) in het veld Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="a7bdd-117">Typ Voorbeeldbericht elektronische factuur in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="a7bdd-118">Voorbeeldbericht elektronische factuur</span><span class="sxs-lookup"><span data-stu-id="a7bdd-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="a7bdd-119">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="a7bdd-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="a7bdd-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="a7bdd-121">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="a7bdd-122">Ontwerp een indeling om bijlagen te vullen om een bericht in MIME-indeling te genereren</span><span class="sxs-lookup"><span data-stu-id="a7bdd-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="a7bdd-123">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-123">Click Designer.</span></span>
2. <span data-ttu-id="a7bdd-124">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="a7bdd-125">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="a7bdd-126">Typ Factuur in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="a7bdd-127">Factuur</span><span class="sxs-lookup"><span data-stu-id="a7bdd-127">Invoice</span></span>  
5. <span data-ttu-id="a7bdd-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-128">Click OK.</span></span>
6. <span data-ttu-id="a7bdd-129">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="a7bdd-130">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="a7bdd-131">Typ SalesOrder in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="a7bdd-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="a7bdd-132">SalesOrder</span></span>  
9. <span data-ttu-id="a7bdd-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-133">Click OK.</span></span>
10. <span data-ttu-id="a7bdd-134">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="a7bdd-135">Typ InvoiceNumber in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="a7bdd-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="a7bdd-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="a7bdd-137">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-137">Click OK.</span></span>
13. <span data-ttu-id="a7bdd-138">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="a7bdd-139">Typ InvoiceAmount in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="a7bdd-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="a7bdd-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="a7bdd-141">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-141">Click OK.</span></span>
16. <span data-ttu-id="a7bdd-142">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="a7bdd-143">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="a7bdd-144">Typ EnclosedDocs in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="a7bdd-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="a7bdd-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="a7bdd-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-146">Click OK.</span></span>
20. <span data-ttu-id="a7bdd-147">Selecteer in de structuur Factuur\EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="a7bdd-148">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-148">Click Add Element.</span></span>
22. <span data-ttu-id="a7bdd-149">Typ Document in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="a7bdd-150">Document</span><span class="sxs-lookup"><span data-stu-id="a7bdd-150">Document</span></span>  
23. <span data-ttu-id="a7bdd-151">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-151">Click OK.</span></span>
24. <span data-ttu-id="a7bdd-152">Selecteer in de structuur Factuur\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="a7bdd-153">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="a7bdd-154">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="a7bdd-155">Typ FileName in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="a7bdd-156">FileName</span><span class="sxs-lookup"><span data-stu-id="a7bdd-156">FileName</span></span>  
28. <span data-ttu-id="a7bdd-157">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-157">Click OK.</span></span>
29. <span data-ttu-id="a7bdd-158">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="a7bdd-159">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="a7bdd-160">Typ FileContent in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="a7bdd-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="a7bdd-161">FileContent</span></span>  
32. <span data-ttu-id="a7bdd-162">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-162">Click OK.</span></span>
33. <span data-ttu-id="a7bdd-163">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="a7bdd-164">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="a7bdd-165">Selecteer Tekst\Base64 in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="a7bdd-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="a7bdd-167">Indelingselementen aan gegevensmodel toewijzen als gegevensbron</span><span class="sxs-lookup"><span data-stu-id="a7bdd-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="a7bdd-168">Selecteer in de structuur Factuur\SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="a7bdd-169">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="a7bdd-170">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="a7bdd-171">Selecteer in de structuur Model\Verkoopordernummer (Salesid).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="a7bdd-172">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-172">Click Bind.</span></span>
6. <span data-ttu-id="a7bdd-173">Selecteer in de structuur Factuur\InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="a7bdd-174">Vouw in de structuur model\Base invoice(InvoiceBase) uit.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="a7bdd-175">Selecteer in de structuur model\Base invoice(InvoiceBase)\Factuurnummer(Id).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="a7bdd-176">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-176">Click Bind.</span></span>
10. <span data-ttu-id="a7bdd-177">Selecteer in de structuur Factuur\InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="a7bdd-178">Selecteer in de structuur model\Base invoice(InvoiceBase)\Factuurbedrag(Amount).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="a7bdd-179">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-179">Click Bind.</span></span>
13. <span data-ttu-id="a7bdd-180">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="a7bdd-181">Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="a7bdd-182">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\Base64.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="a7bdd-183">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-183">Click Bind.</span></span>
17. <span data-ttu-id="a7bdd-184">Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="a7bdd-185">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\FileName.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="a7bdd-186">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-186">Click Bind.</span></span>
20. <span data-ttu-id="a7bdd-187">Selecteer in de structuur model\Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="a7bdd-188">Selecteer in de structuur Factuur\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="a7bdd-189">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-189">Click Bind.</span></span>
23. <span data-ttu-id="a7bdd-190">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-190">Click Save.</span></span>
24. <span data-ttu-id="a7bdd-191">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]