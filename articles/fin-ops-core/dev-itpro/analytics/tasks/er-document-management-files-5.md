---
title: 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 5: Indeling aanpassen en uitvoeren)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de075899547d194fb9eb0e68947efd005c101851
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550689"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="91172-103">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 5: Indeling aanpassen en uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="91172-103">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91172-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="91172-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="91172-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="91172-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="91172-106">Om deze stappen uit te voeren, moet u eerst de stappen uitvoeren in de procedure 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4: Indeling uitvoeren)'.</span><span class="sxs-lookup"><span data-stu-id="91172-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="91172-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="91172-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="91172-108">De indeling voor het vullen van bijlagen aanpassen zodat berichten in binaire indeling worden gegenereerd</span><span class="sxs-lookup"><span data-stu-id="91172-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="91172-109">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="91172-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="91172-110">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="91172-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="91172-111">Vouw in de structuur 'Customer invoice model\Customer invoice model (custom)' uit.</span><span class="sxs-lookup"><span data-stu-id="91172-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="91172-112">Selecteer in de structuur 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="91172-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="91172-113">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="91172-113">Click Designer.</span></span>
    * <span data-ttu-id="91172-114">U voert het facturenbericht in de producerende uitvoer in als een XML-bestand met UNICODE-codering.</span><span class="sxs-lookup"><span data-stu-id="91172-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="91172-115">Klik op Basis toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="91172-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="91172-116">Selecteer "Common\File" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="91172-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="91172-117">Typ "XML-bericht" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="91172-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="91172-118">Xml=bericht</span><span class="sxs-lookup"><span data-stu-id="91172-118">Xml message</span></span>  
9. <span data-ttu-id="91172-119">Typ "UTF-8" in het veld Codering.</span><span class="sxs-lookup"><span data-stu-id="91172-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="91172-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="91172-120">UTF-8</span></span>  
10. <span data-ttu-id="91172-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="91172-121">Click OK.</span></span>
    * <span data-ttu-id="91172-122">Configureer de producerende uitvoer als gecomprimeerd bestand.</span><span class="sxs-lookup"><span data-stu-id="91172-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="91172-123">Klik op Basis toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="91172-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="91172-124">Selecteer in de structuur "Common\Folder".</span><span class="sxs-lookup"><span data-stu-id="91172-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="91172-125">Typ in het veld Naam 'Zip output'.</span><span class="sxs-lookup"><span data-stu-id="91172-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="91172-126">Zip-uitvoer</span><span class="sxs-lookup"><span data-stu-id="91172-126">Zip output</span></span>  
14. <span data-ttu-id="91172-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="91172-127">Click OK.</span></span>
15. <span data-ttu-id="91172-128">Selecteer in de structuur 'Zip output'.</span><span class="sxs-lookup"><span data-stu-id="91172-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="91172-129">Voeg bijlagen toe aan het producerende gecomprimeerde bestand als bestanden met oorspronkelijke namen en extensies.</span><span class="sxs-lookup"><span data-stu-id="91172-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="91172-130">Klik op Toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="91172-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="91172-131">Selecteer "Common\File" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="91172-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="91172-132">Typ in het veld Naam 'Attached file'.</span><span class="sxs-lookup"><span data-stu-id="91172-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="91172-133">Gekoppeld bestand</span><span class="sxs-lookup"><span data-stu-id="91172-133">Attached file</span></span>  
19. <span data-ttu-id="91172-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="91172-134">Click OK.</span></span>
20. <span data-ttu-id="91172-135">Selecteer in de structuur 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="91172-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="91172-136">Klik op Toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="91172-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="91172-137">Selecteer Tekst\Base64 in de structuur.</span><span class="sxs-lookup"><span data-stu-id="91172-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="91172-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="91172-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="91172-139">Nieuwe indelingselementen toewijzen aan gegevensmodellen</span><span class="sxs-lookup"><span data-stu-id="91172-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="91172-140">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="91172-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="91172-141">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="91172-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="91172-142">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="91172-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="91172-143">Selecteer in de structuur 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="91172-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="91172-144">Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="91172-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="91172-145">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="91172-145">Click Bind.</span></span>
7. <span data-ttu-id="91172-146">Selecteer in de structuur 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="91172-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="91172-147">Klik op Bestandsnaam bewerken.</span><span class="sxs-lookup"><span data-stu-id="91172-147">Click Edit filename.</span></span>
9. <span data-ttu-id="91172-148">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="91172-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="91172-149">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="91172-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="91172-150">Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="91172-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="91172-151">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="91172-151">Click Add data source.</span></span>
13. <span data-ttu-id="91172-152">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="91172-152">Click Save.</span></span>
14. <span data-ttu-id="91172-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="91172-153">Close the page.</span></span>
15. <span data-ttu-id="91172-154">Selecteer in de structuur model\Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="91172-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="91172-155">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="91172-155">Click Bind.</span></span>
17. <span data-ttu-id="91172-156">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="91172-156">Click Save.</span></span>
18. <span data-ttu-id="91172-157">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="91172-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="91172-158">Het ontworpen rapport uitvoeren voor de geselecteerde factuur</span><span class="sxs-lookup"><span data-stu-id="91172-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="91172-159">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="91172-159">Click Run.</span></span>
2. <span data-ttu-id="91172-160">Vouw de records uit zodat de sectie () is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="91172-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="91172-161">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="91172-161">Click Filter.</span></span>
4. <span data-ttu-id="91172-162">Selecteer de rij van het Klantfacturenjournaal en het veld Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="91172-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="91172-163">Type in het veld Criteria in het veld met criteria voor “Verkooporder” het ordernummer 000148.</span><span class="sxs-lookup"><span data-stu-id="91172-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="91172-164">000148</span><span class="sxs-lookup"><span data-stu-id="91172-164">000148</span></span>  
6. <span data-ttu-id="91172-165">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="91172-165">Click OK.</span></span>
7. <span data-ttu-id="91172-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="91172-166">Click OK.</span></span>
    * <span data-ttu-id="91172-167">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="91172-167">Review the generated output.</span></span> <span data-ttu-id="91172-168">Merk op dat naast het factuurbericht in XML-indeling, voor elke bijlage één bestand is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="91172-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="91172-169">De bijlagebestanden worden gevuld met de gecomprimeerde uitvoer in binaire indeling.</span><span class="sxs-lookup"><span data-stu-id="91172-169">The attachment files are populated with the zipped output in binary format.</span></span>  
