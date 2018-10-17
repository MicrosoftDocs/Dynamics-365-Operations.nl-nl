--- 
title: ER-configuraties ontwerpen om rapporten in Word-indeling te genereren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met een rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-indeling (elektronische rapportage) kan configureren, waarmee rapporten in de vorm van Microsoft Word-bestanden worden gegenereerd.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="cfe0d-103">ER-configuraties ontwerpen om rapporten in Word-indeling te genereren</span><span class="sxs-lookup"><span data-stu-id="cfe0d-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cfe0d-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met een rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-indeling (elektronische rapportage) kan configureren, waarmee rapporten in de vorm van Microsoft Word-bestanden worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="cfe0d-105">Deze stappen kunnen in het GBSI-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="cfe0d-106">Voordat u deze stappen uitvoert, moet u eerst de stappen uitvoeren in de taakbegeleiding “Een ER-configuratie maken voor het genereren van rapporten in OPENXML-indeling“.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="cfe0d-107">U moet van tevoren ook de volgende sjablonen downloaden en lokaal opslaan voor het voorbeeldrapport:</span><span class="sxs-lookup"><span data-stu-id="cfe0d-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="cfe0d-108">Sjabloon van betalingsrapport</span><span class="sxs-lookup"><span data-stu-id="cfe0d-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="cfe0d-109">Gebonden sjabloon van betalingsrapport</span><span class="sxs-lookup"><span data-stu-id="cfe0d-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="cfe0d-110">Deze procedure is voor een functie die in versie 1611 van Microsoft Dynamics 365 for Operations is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="cfe0d-111">De bestaande ER-rapportconfiguratie selecteren</span><span class="sxs-lookup"><span data-stu-id="cfe0d-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="cfe0d-112">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="cfe0d-113">Controleer of de configuratieprovider 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="cfe0d-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="cfe0d-114">als actief is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-114">is selected as active.</span></span>  
2. <span data-ttu-id="cfe0d-115">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="cfe0d-116">We recyclen de bestaande ER-configuratie die oorspronkelijk is opgezet voor het genereren van de rapportuitvoer in OPENXML-indeling.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="cfe0d-117">Vouw "Betalingsmodel" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="cfe0d-118">Selecteer Betalingsmodel\Voorbeeldwerkbladrapport in de structuur.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="cfe0d-119">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="cfe0d-120">De Excel-sjabloon vervangen door de Word-sjabloon</span><span class="sxs-lookup"><span data-stu-id="cfe0d-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="cfe0d-121">Momenteel wordt het Excel-document gebruikt als sjabloon voor het genereren van de uitvoer in OPENXML-indeling.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="cfe0d-122">We importeren de sjabloon van het rapport in Word-indeling.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="cfe0d-123">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-123">Click Attachments.</span></span>
    * <span data-ttu-id="cfe0d-124">Vervang de bestaande Excel-sjabloon door de Word-sjabloon die u eerder hebt gedownload, SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="cfe0d-125">Houd er rekening mee dat deze sjabloon alleen de indeling bevat van het document dat we willen genereren als ER-uitvoer.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="cfe0d-126">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-126">Click Delete.</span></span>
3. <span data-ttu-id="cfe0d-127">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-127">Click Yes.</span></span>
4. <span data-ttu-id="cfe0d-128">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-128">Click New.</span></span>
5. <span data-ttu-id="cfe0d-129">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-129">Click File.</span></span>
6. <span data-ttu-id="cfe0d-130">Klik op Bladeren.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-130">Click Browse.</span></span> <span data-ttu-id="cfe0d-131">Navigeer naar en selecteer het bestand SampleVendPaymDocReport.docx, dat u eerder hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="cfe0d-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-132">Click OK.</span></span>
    * <span data-ttu-id="cfe0d-133">Selecteer de sjabloon die u in de vorige stap hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="cfe0d-134">Typ of selecteer een waarde in het veld Sjabloon.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="cfe0d-135">De Word-sjabloon uitbreiden met een aangepast XML-onderdeel</span><span class="sxs-lookup"><span data-stu-id="cfe0d-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="cfe0d-136">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-136">Click Save.</span></span>
    * <span data-ttu-id="cfe0d-137">De actie Opslaan legt niet alleen de configuratiewijzigingen vast, maar werkt ook tegelijk de gekoppelde Word-sjabloon bij.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="cfe0d-138">De structuur van de ontworpen indeling wordt overgezet naar het gekoppelde Word-document als een nieuw aangepast XML-onderdeel met de naam 'Report'.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="cfe0d-139">Let erop dat de gekoppelde Word-sjabloon niet alleen de indeling van het document bevat dat we wilt genereren als ER-uitvoer, maar ook de structuur van gegevens die ER in deze sjabloon tijdens runtime invult.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="cfe0d-140">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-140">Click Attachments.</span></span>
    * <span data-ttu-id="cfe0d-141">Nu moet u de elementen van het aangepaste XML-onderdeel 'Report' binden aan de delen van het Word-document.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="cfe0d-142">Als u ervaring hebt met Word-documenten die zijn ontwikkeld als formulieren met inhoudsbesturingselementen die gebonden zijn aan met elementen van aangepaste XML-onderdelen: speel alle stappen van de volgende subtaak af om een dergelijk document te maken.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="cfe0d-143">Zie deze koppeling https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US voor nadere details.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="cfe0d-144">Zo niet, dan kunt u alle stappen in de volgende subtaak overslaan.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="cfe0d-145">Word met aangepast XML-onderdeel gegevensbindingen laten uitvoeren</span><span class="sxs-lookup"><span data-stu-id="cfe0d-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="cfe0d-146">Open dit document in Word en doe het volgende: - Ga naar het tabblad Word-ontwikkelaar (pas het lint aan als dit tabblad nog niet is ingeschakeld).</span><span class="sxs-lookup"><span data-stu-id="cfe0d-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="cfe0d-147">- Selecteer het deelvenster XML-toewijzing.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="cfe0d-148">- Selecteer het aangepaste XML-onderdeel 'Rapport' in de zoekopdracht.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="cfe0d-149">- Voer de toewijzing uit van de elementen van het geselecteerde, aangepaste XML-onderdeel aan de inhoudsbesturingselementen van het Word-document.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="cfe0d-150">- Sla het bijgewerkte Word-document op een lokaal station op.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="cfe0d-151">De Word-sjabloon met aangepaste XML-onderdeel, dat is gebonden aan inhoudsbesturingselementen, uploaden</span><span class="sxs-lookup"><span data-stu-id="cfe0d-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="cfe0d-152">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-152">Click Delete.</span></span>
2. <span data-ttu-id="cfe0d-153">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-153">Click Yes.</span></span>
    * <span data-ttu-id="cfe0d-154">Voeg een nieuwe sjabloon toe.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-154">Add a new template.</span></span> <span data-ttu-id="cfe0d-155">Als u de stappen in de vorige subtaak hebt uitgevoerd, selecteert u het Word-document dat u hebt voorbereid en lokaal opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="cfe0d-156">Selecteer anders de MS Word-sjabloon SampleVendPaymDocReportBounded.docx, die u eerder hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="cfe0d-157">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-157">Click New.</span></span>
4. <span data-ttu-id="cfe0d-158">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-158">Click File.</span></span>
5. <span data-ttu-id="cfe0d-159">Klik op Bladeren.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-159">Click Browse.</span></span> <span data-ttu-id="cfe0d-160">Navigeer naar en selecteer het bestand SampleVendPaymDocReportBounded.docx, dat u eerder hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="cfe0d-161">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-161">Click OK.</span></span>
6. <span data-ttu-id="cfe0d-162">Selecteer in het veld Sjabloon het document dat u in de vorige stap hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="cfe0d-163">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-163">Click Save.</span></span>
8. <span data-ttu-id="cfe0d-164">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="cfe0d-165">De indeling uitvoeren om Word-uitvoer te maken</span><span class="sxs-lookup"><span data-stu-id="cfe0d-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="cfe0d-166">Klik in het actievenster op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="cfe0d-167">Klik op Gebruikersparameters.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-167">Click User parameters.</span></span>
3. <span data-ttu-id="cfe0d-168">Selecteer Ja in het veld Uitvoeringsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="cfe0d-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-169">Click OK.</span></span>
5. <span data-ttu-id="cfe0d-170">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-170">Click Edit.</span></span>
6. <span data-ttu-id="cfe0d-171">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="cfe0d-172">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-172">Click Save.</span></span>
8. <span data-ttu-id="cfe0d-173">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-173">Close the page.</span></span>
9. <span data-ttu-id="cfe0d-174">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-174">Close the page.</span></span>
10. <span data-ttu-id="cfe0d-175">Ga naar Leveranciers > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="cfe0d-176">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-176">Click Lines.</span></span>
12. <span data-ttu-id="cfe0d-177">Selecteer of deselecteer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="cfe0d-178">Klik op Betalingsstatus.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-178">Click Payment status.</span></span>
14. <span data-ttu-id="cfe0d-179">Klik op Geen.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-179">Click None.</span></span>
15. <span data-ttu-id="cfe0d-180">Klik op Betalingen genereren.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-180">Click Generate payments.</span></span>
16. <span data-ttu-id="cfe0d-181">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-181">Click OK.</span></span>
17. <span data-ttu-id="cfe0d-182">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-182">Click OK.</span></span>
    * <span data-ttu-id="cfe0d-183">Analyseer de gegenereerde uitvoer.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-183">Analyze the generated output.</span></span> <span data-ttu-id="cfe0d-184">Merk op dat de uitvoer wordt weergegeven in Word-indeling en de details van de verwerkte betalingen bevat.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


