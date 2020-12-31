---
title: ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 3 - Indeling maken)
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
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfcc03fa7470d4f2fa45ef012e30acef0712bf99
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681848"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="f3609-103">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 3 - Indeling maken)</span><span class="sxs-lookup"><span data-stu-id="f3609-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3609-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="f3609-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f3609-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f3609-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f3609-106">Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 2: Gegevensmodel uitbreiden)".</span><span class="sxs-lookup"><span data-stu-id="f3609-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="f3609-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="f3609-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="f3609-108">Maak een indeling om facturen te verwerken</span><span class="sxs-lookup"><span data-stu-id="f3609-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="f3609-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="f3609-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f3609-110">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="f3609-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f3609-111">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="f3609-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="f3609-112">Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).</span><span class="sxs-lookup"><span data-stu-id="f3609-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="f3609-113">U maakt een indeling om elektronische berichten te genereren met informatie over de bestanden die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.</span><span class="sxs-lookup"><span data-stu-id="f3609-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="f3609-114">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="f3609-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="f3609-115">Typ Indeling gebaseerd op gegevensmodel Klantfactuurmodel (aangepast) in het veld Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f3609-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="f3609-116">Typ Voorbeeldbericht elektronische factuur in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="f3609-117">Voorbeeldbericht elektronische factuur</span><span class="sxs-lookup"><span data-stu-id="f3609-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="f3609-118">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="f3609-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="f3609-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="f3609-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="f3609-120">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="f3609-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="f3609-121">Ontwerp een indeling om bijlagen te vullen om een bericht in MIME-indeling te genereren</span><span class="sxs-lookup"><span data-stu-id="f3609-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="f3609-122">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="f3609-122">Click Designer.</span></span>
2. <span data-ttu-id="f3609-123">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="f3609-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="f3609-124">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="f3609-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="f3609-125">Typ Factuur in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="f3609-126">Factuur</span><span class="sxs-lookup"><span data-stu-id="f3609-126">Invoice</span></span>  
5. <span data-ttu-id="f3609-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-127">Click OK.</span></span>
6. <span data-ttu-id="f3609-128">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="f3609-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="f3609-129">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="f3609-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="f3609-130">Typ SalesOrder in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="f3609-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="f3609-131">SalesOrder</span></span>  
9. <span data-ttu-id="f3609-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-132">Click OK.</span></span>
10. <span data-ttu-id="f3609-133">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f3609-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="f3609-134">Typ InvoiceNumber in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="f3609-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="f3609-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="f3609-136">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-136">Click OK.</span></span>
13. <span data-ttu-id="f3609-137">Klik op Kenmerk toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f3609-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="f3609-138">Typ InvoiceAmount in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="f3609-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="f3609-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="f3609-140">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-140">Click OK.</span></span>
16. <span data-ttu-id="f3609-141">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="f3609-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="f3609-142">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="f3609-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="f3609-143">Typ EnclosedDocs in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="f3609-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="f3609-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="f3609-145">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-145">Click OK.</span></span>
20. <span data-ttu-id="f3609-146">Selecteer in de structuur Factuur\EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="f3609-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="f3609-147">Klik op Element toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f3609-147">Click Add Element.</span></span>
22. <span data-ttu-id="f3609-148">Typ Document in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="f3609-149">Document</span><span class="sxs-lookup"><span data-stu-id="f3609-149">Document</span></span>  
23. <span data-ttu-id="f3609-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-150">Click OK.</span></span>
24. <span data-ttu-id="f3609-151">Selecteer in de structuur Factuur\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="f3609-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="f3609-152">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="f3609-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="f3609-153">Selecteer "XML\Attribute" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="f3609-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="f3609-154">Typ FileName in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="f3609-155">FileName</span><span class="sxs-lookup"><span data-stu-id="f3609-155">FileName</span></span>  
28. <span data-ttu-id="f3609-156">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-156">Click OK.</span></span>
29. <span data-ttu-id="f3609-157">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="f3609-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="f3609-158">Selecteer "XML\Element" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="f3609-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="f3609-159">Typ FileContent in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="f3609-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="f3609-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="f3609-160">FileContent</span></span>  
32. <span data-ttu-id="f3609-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-161">Click OK.</span></span>
33. <span data-ttu-id="f3609-162">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent.</span><span class="sxs-lookup"><span data-stu-id="f3609-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="f3609-163">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="f3609-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="f3609-164">Selecteer Tekst\Base64 in de structuur.</span><span class="sxs-lookup"><span data-stu-id="f3609-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="f3609-165">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f3609-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="f3609-166">Indelingselementen aan gegevensmodel toewijzen als gegevensbron</span><span class="sxs-lookup"><span data-stu-id="f3609-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="f3609-167">Selecteer in de structuur Factuur\SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="f3609-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="f3609-168">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="f3609-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="f3609-169">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="f3609-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="f3609-170">Selecteer in de structuur Model\Verkoopordernummer (Salesid).</span><span class="sxs-lookup"><span data-stu-id="f3609-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="f3609-171">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="f3609-171">Click Bind.</span></span>
6. <span data-ttu-id="f3609-172">Selecteer in de structuur Factuur\InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="f3609-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="f3609-173">Vouw in de structuur model\Base invoice(InvoiceBase) uit.</span><span class="sxs-lookup"><span data-stu-id="f3609-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="f3609-174">Selecteer in de structuur model\Base invoice(InvoiceBase)\Factuurnummer(Id).</span><span class="sxs-lookup"><span data-stu-id="f3609-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="f3609-175">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="f3609-175">Click Bind.</span></span>
10. <span data-ttu-id="f3609-176">Selecteer in de structuur Factuur\InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="f3609-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="f3609-177">Selecteer in de structuur model\Base invoice(InvoiceBase)\Factuurbedrag(Amount).</span><span class="sxs-lookup"><span data-stu-id="f3609-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="f3609-178">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="f3609-178">Click Bind.</span></span>
13. <span data-ttu-id="f3609-179">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="f3609-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="f3609-180">Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="f3609-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="f3609-181">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\Base64.</span><span class="sxs-lookup"><span data-stu-id="f3609-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="f3609-182">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="f3609-182">Click Bind.</span></span>
17. <span data-ttu-id="f3609-183">Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="f3609-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="f3609-184">Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\FileName.</span><span class="sxs-lookup"><span data-stu-id="f3609-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="f3609-185">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="f3609-185">Click Bind.</span></span>
20. <span data-ttu-id="f3609-186">Selecteer in de structuur model\Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="f3609-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="f3609-187">Selecteer in de structuur Factuur\EnclosedDocs\Document.</span><span class="sxs-lookup"><span data-stu-id="f3609-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="f3609-188">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="f3609-188">Click Bind.</span></span>
23. <span data-ttu-id="f3609-189">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f3609-189">Click Save.</span></span>
24. <span data-ttu-id="f3609-190">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f3609-190">Close the page.</span></span>

