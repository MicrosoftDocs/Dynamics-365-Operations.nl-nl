---
title: 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 5: Indeling aanpassen en uitvoeren)'
description: In dit onderwerp wordt beschreven hoe u een indeling voor elektronische rapportage (ER) configureert om documentbeheerbestanden (bijlagen) te gebruiken in ER-uitvoer. (Deel 5)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092483"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="b60a7-104">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 5: Indeling aanpassen en uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="b60a7-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b60a7-105">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="b60a7-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b60a7-106">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b60a7-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="b60a7-107">Om deze stappen uit te voeren, moet u eerst de stappen uitvoeren in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4: Indeling uitvoeren)".</span><span class="sxs-lookup"><span data-stu-id="b60a7-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="b60a7-108">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="b60a7-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="b60a7-109">De indeling voor het vullen van bijlagen aanpassen zodat berichten in binaire indeling worden gegenereerd</span><span class="sxs-lookup"><span data-stu-id="b60a7-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="b60a7-110">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="b60a7-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b60a7-111">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="b60a7-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="b60a7-112">Vouw in de structuur 'Customer invoice model\Customer invoice model (custom)' uit.</span><span class="sxs-lookup"><span data-stu-id="b60a7-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="b60a7-113">Selecteer in de structuur 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="b60a7-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="b60a7-114">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="b60a7-114">Click Designer.</span></span>
    * <span data-ttu-id="b60a7-115">U voert het facturenbericht in de producerende uitvoer in als een XML-bestand met UNICODE-codering.</span><span class="sxs-lookup"><span data-stu-id="b60a7-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="b60a7-116">Klik op Basis toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="b60a7-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="b60a7-117">Selecteer "Common\File" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b60a7-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="b60a7-118">Typ "XML-bericht" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="b60a7-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="b60a7-119">Xml=bericht</span><span class="sxs-lookup"><span data-stu-id="b60a7-119">Xml message</span></span>  
9. <span data-ttu-id="b60a7-120">Typ "UTF-8" in het veld Codering.</span><span class="sxs-lookup"><span data-stu-id="b60a7-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="b60a7-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="b60a7-121">UTF-8</span></span>  
10. <span data-ttu-id="b60a7-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b60a7-122">Click OK.</span></span>
    * <span data-ttu-id="b60a7-123">Configureer de producerende uitvoer als gecomprimeerd bestand.</span><span class="sxs-lookup"><span data-stu-id="b60a7-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="b60a7-124">Klik op Basis toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="b60a7-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="b60a7-125">Selecteer in de structuur "Common\Folder".</span><span class="sxs-lookup"><span data-stu-id="b60a7-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="b60a7-126">Typ in het veld Naam 'Zip output'.</span><span class="sxs-lookup"><span data-stu-id="b60a7-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="b60a7-127">Zip-uitvoer</span><span class="sxs-lookup"><span data-stu-id="b60a7-127">Zip output</span></span>  
14. <span data-ttu-id="b60a7-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b60a7-128">Click OK.</span></span>
15. <span data-ttu-id="b60a7-129">Selecteer in de structuur 'Zip output'.</span><span class="sxs-lookup"><span data-stu-id="b60a7-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="b60a7-130">Voeg bijlagen toe aan het producerende gecomprimeerde bestand als bestanden met oorspronkelijke namen en extensies.</span><span class="sxs-lookup"><span data-stu-id="b60a7-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="b60a7-131">Klik op Toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="b60a7-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="b60a7-132">Selecteer "Common\File" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b60a7-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="b60a7-133">Typ in het veld Naam 'Attached file'.</span><span class="sxs-lookup"><span data-stu-id="b60a7-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="b60a7-134">Gekoppeld bestand</span><span class="sxs-lookup"><span data-stu-id="b60a7-134">Attached file</span></span>  
19. <span data-ttu-id="b60a7-135">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b60a7-135">Click OK.</span></span>
20. <span data-ttu-id="b60a7-136">Selecteer in de structuur 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="b60a7-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="b60a7-137">Klik op Toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="b60a7-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="b60a7-138">Selecteer Tekst\Base64 in de structuur.</span><span class="sxs-lookup"><span data-stu-id="b60a7-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="b60a7-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b60a7-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="b60a7-140">Nieuwe indelingselementen toewijzen aan gegevensmodellen</span><span class="sxs-lookup"><span data-stu-id="b60a7-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="b60a7-141">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="b60a7-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="b60a7-142">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="b60a7-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="b60a7-143">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="b60a7-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="b60a7-144">Selecteer in de structuur 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="b60a7-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="b60a7-145">Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="b60a7-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="b60a7-146">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="b60a7-146">Click Bind.</span></span>
7. <span data-ttu-id="b60a7-147">Selecteer in de structuur 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="b60a7-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="b60a7-148">Klik op Bestandsnaam bewerken.</span><span class="sxs-lookup"><span data-stu-id="b60a7-148">Click Edit filename.</span></span>
9. <span data-ttu-id="b60a7-149">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="b60a7-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="b60a7-150">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="b60a7-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="b60a7-151">Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="b60a7-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="b60a7-152">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b60a7-152">Click Add data source.</span></span>
13. <span data-ttu-id="b60a7-153">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b60a7-153">Click Save.</span></span>
14. <span data-ttu-id="b60a7-154">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b60a7-154">Close the page.</span></span>
15. <span data-ttu-id="b60a7-155">Selecteer in de structuur model\Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="b60a7-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="b60a7-156">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="b60a7-156">Click Bind.</span></span>
17. <span data-ttu-id="b60a7-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="b60a7-157">Click Save.</span></span>
18. <span data-ttu-id="b60a7-158">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b60a7-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="b60a7-159">Het ontworpen rapport uitvoeren voor de geselecteerde factuur</span><span class="sxs-lookup"><span data-stu-id="b60a7-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="b60a7-160">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b60a7-160">Click Run.</span></span>
2. <span data-ttu-id="b60a7-161">Vouw de records uit zodat de sectie () is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b60a7-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="b60a7-162">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="b60a7-162">Click Filter.</span></span>
4. <span data-ttu-id="b60a7-163">Selecteer de rij van het Klantfacturenjournaal en het veld Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="b60a7-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="b60a7-164">Type in het veld Criteria in het veld met criteria voor "Verkooporder" het ordernummer 000148.</span><span class="sxs-lookup"><span data-stu-id="b60a7-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="b60a7-165">000148</span><span class="sxs-lookup"><span data-stu-id="b60a7-165">000148</span></span>  
6. <span data-ttu-id="b60a7-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b60a7-166">Click OK.</span></span>
7. <span data-ttu-id="b60a7-167">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="b60a7-167">Click OK.</span></span>
    * <span data-ttu-id="b60a7-168">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="b60a7-168">Review the generated output.</span></span> <span data-ttu-id="b60a7-169">Merk op dat naast het factuurbericht in XML-indeling, voor elke bijlage één bestand is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b60a7-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="b60a7-170">De bijlagebestanden worden gevuld met de gecomprimeerde uitvoer in binaire indeling.</span><span class="sxs-lookup"><span data-stu-id="b60a7-170">The attachment files are populated with the zipped output in binary format.</span></span>  

