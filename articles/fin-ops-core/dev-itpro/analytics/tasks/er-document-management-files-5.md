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
ms.openlocfilehash: ba9cc4dcdfcfbc1bdb933336e85da9b4b6d97a40
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182503"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5-modify-and-run-format"></a><span data-ttu-id="04492-103">ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 5: Indeling aanpassen en uitvoeren)</span><span class="sxs-lookup"><span data-stu-id="04492-103">ER Use Document Management files in format outputs (Part 5: Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04492-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="04492-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="04492-105">Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="04492-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="04492-106">Om deze stappen uit te voeren, moet u eerst de stappen uitvoeren in de procedure 'ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4: Indeling uitvoeren)'.</span><span class="sxs-lookup"><span data-stu-id="04492-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="04492-107">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="04492-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="04492-108">De indeling voor het vullen van bijlagen aanpassen zodat berichten in binaire indeling worden gegenereerd</span><span class="sxs-lookup"><span data-stu-id="04492-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="04492-109">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="04492-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="04492-110">Vouw in de structuur Klantfactuurmodel uit.</span><span class="sxs-lookup"><span data-stu-id="04492-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="04492-111">Vouw in de structuur 'Customer invoice model\Customer invoice model (custom)' uit.</span><span class="sxs-lookup"><span data-stu-id="04492-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="04492-112">Selecteer in de structuur 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="04492-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="04492-113">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="04492-113">Click Designer.</span></span>
    * <span data-ttu-id="04492-114">U voert het facturenbericht in de producerende uitvoer in als een XML-bestand met UNICODE-codering.</span><span class="sxs-lookup"><span data-stu-id="04492-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="04492-115">Klik op Basis toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="04492-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="04492-116">Selecteer "Common\File" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="04492-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="04492-117">Typ "XML-bericht" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="04492-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="04492-118">Xml=bericht</span><span class="sxs-lookup"><span data-stu-id="04492-118">Xml message</span></span>  
9. <span data-ttu-id="04492-119">Typ "UTF-8" in het veld Codering.</span><span class="sxs-lookup"><span data-stu-id="04492-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="04492-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="04492-120">UTF-8</span></span>  
10. <span data-ttu-id="04492-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="04492-121">Click OK.</span></span>
    * <span data-ttu-id="04492-122">Configureer de producerende uitvoer als gecomprimeerd bestand.</span><span class="sxs-lookup"><span data-stu-id="04492-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="04492-123">Klik op Basis toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="04492-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="04492-124">Selecteer in de structuur "Common\Folder".</span><span class="sxs-lookup"><span data-stu-id="04492-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="04492-125">Typ in het veld Naam 'Zip output'.</span><span class="sxs-lookup"><span data-stu-id="04492-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="04492-126">Zip-uitvoer</span><span class="sxs-lookup"><span data-stu-id="04492-126">Zip output</span></span>  
14. <span data-ttu-id="04492-127">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="04492-127">Click OK.</span></span>
15. <span data-ttu-id="04492-128">Selecteer in de structuur 'Zip output'.</span><span class="sxs-lookup"><span data-stu-id="04492-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="04492-129">Voeg bijlagen toe aan het producerende gecomprimeerde bestand als bestanden met oorspronkelijke namen en extensies.</span><span class="sxs-lookup"><span data-stu-id="04492-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="04492-130">Klik op Toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="04492-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="04492-131">Selecteer "Common\File" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="04492-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="04492-132">Typ in het veld Naam 'Attached file'.</span><span class="sxs-lookup"><span data-stu-id="04492-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="04492-133">Gekoppeld bestand</span><span class="sxs-lookup"><span data-stu-id="04492-133">Attached file</span></span>  
19. <span data-ttu-id="04492-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="04492-134">Click OK.</span></span>
20. <span data-ttu-id="04492-135">Selecteer in de structuur 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="04492-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="04492-136">Klik op Toevoegen om het uitklapvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="04492-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="04492-137">Selecteer Tekst\Base64 in de structuur.</span><span class="sxs-lookup"><span data-stu-id="04492-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="04492-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="04492-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="04492-139">Nieuwe indelingselementen toewijzen aan gegevensmodellen</span><span class="sxs-lookup"><span data-stu-id="04492-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="04492-140">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="04492-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="04492-141">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="04492-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="04492-142">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="04492-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="04492-143">Selecteer in de structuur 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="04492-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="04492-144">Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.</span><span class="sxs-lookup"><span data-stu-id="04492-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="04492-145">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="04492-145">Click Bind.</span></span>
7. <span data-ttu-id="04492-146">Selecteer in de structuur 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="04492-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="04492-147">Klik op Bestandsnaam bewerken.</span><span class="sxs-lookup"><span data-stu-id="04492-147">Click Edit filename.</span></span>
9. <span data-ttu-id="04492-148">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="04492-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="04492-149">Vouw in de structuur model\Factuurbijlagen uit.</span><span class="sxs-lookup"><span data-stu-id="04492-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="04492-150">Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="04492-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="04492-151">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="04492-151">Click Add data source.</span></span>
13. <span data-ttu-id="04492-152">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="04492-152">Click Save.</span></span>
14. <span data-ttu-id="04492-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04492-153">Close the page.</span></span>
15. <span data-ttu-id="04492-154">Selecteer in de structuur model\Factuurbijlagen.</span><span class="sxs-lookup"><span data-stu-id="04492-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="04492-155">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="04492-155">Click Bind.</span></span>
17. <span data-ttu-id="04492-156">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="04492-156">Click Save.</span></span>
18. <span data-ttu-id="04492-157">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="04492-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="04492-158">Het ontworpen rapport uitvoeren voor de geselecteerde factuur</span><span class="sxs-lookup"><span data-stu-id="04492-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="04492-159">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="04492-159">Click Run.</span></span>
2. <span data-ttu-id="04492-160">Vouw de records uit zodat de sectie () is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="04492-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="04492-161">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="04492-161">Click Filter.</span></span>
4. <span data-ttu-id="04492-162">Selecteer de rij van het Klantfacturenjournaal en het veld Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="04492-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="04492-163">Type in het veld Criteria in het veld met criteria voor “Verkooporder” het ordernummer 000148.</span><span class="sxs-lookup"><span data-stu-id="04492-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="04492-164">000148</span><span class="sxs-lookup"><span data-stu-id="04492-164">000148</span></span>  
6. <span data-ttu-id="04492-165">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="04492-165">Click OK.</span></span>
7. <span data-ttu-id="04492-166">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="04492-166">Click OK.</span></span>
    * <span data-ttu-id="04492-167">Controleer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="04492-167">Review the generated output.</span></span> <span data-ttu-id="04492-168">Merk op dat naast het factuurbericht in XML-indeling, voor elke bijlage één bestand is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="04492-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="04492-169">De bijlagebestanden worden gevuld met de gecomprimeerde uitvoer in binaire indeling.</span><span class="sxs-lookup"><span data-stu-id="04492-169">The attachment files are populated with the zipped output in binary format.</span></span>  

