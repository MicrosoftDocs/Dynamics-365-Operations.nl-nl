--- 
title: Een configuratie ontwerpen voor het genereren van rapporten in OpenXML-indeling voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een sjabloon bevat voor het genereren van elektronische documenten in OPENXML-indeling.
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="052f3-103">Een configuratie ontwerpen voor het genereren van rapporten in OpenXML-indeling voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="052f3-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="052f3-104">In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een sjabloon bevat voor het genereren van elektronische documenten in OPENXML-indeling.</span><span class="sxs-lookup"><span data-stu-id="052f3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="052f3-105">Deze configuratie wordt voor de verwerking van leveranciersbetalingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="052f3-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="052f3-106">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in GBSI-bedrijven worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="052f3-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="052f3-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="052f3-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="052f3-108">U moet ook het Microsoft Excel-bestand [Sjabloon van betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266) downloaden en opslaan.</span><span class="sxs-lookup"><span data-stu-id="052f3-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="052f3-109">De gegevensmodelconfiguratie Betalingen uploaden</span><span class="sxs-lookup"><span data-stu-id="052f3-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="052f3-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="052f3-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="052f3-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="052f3-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="052f3-112">Selecteer de configuratieprovider voor het voorbeeldbedrijf Litware,Inc. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="052f3-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="052f3-113">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="052f3-113">Click Set active.</span></span>
4. <span data-ttu-id="052f3-114">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="052f3-114">Click Repositories.</span></span>
    * <span data-ttu-id="052f3-115">Selecteer een opslagplaats voor het type Bronnen voor bedrijfsactiviteiten, indien beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="052f3-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="052f3-116">Als deze beschikbaar is, slaat u de volgende stappen in verband met het maken van een nieuwe opslagplaats over.</span><span class="sxs-lookup"><span data-stu-id="052f3-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="052f3-117">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="052f3-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="052f3-118">Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.</span><span class="sxs-lookup"><span data-stu-id="052f3-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="052f3-119">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="052f3-119">Click Create repository.</span></span>
8. <span data-ttu-id="052f3-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="052f3-120">Click OK.</span></span>
9. <span data-ttu-id="052f3-121">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="052f3-121">Click Open.</span></span>
10. <span data-ttu-id="052f3-122">Selecteer Betalingsmodel in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="052f3-123">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="052f3-123">Click Import.</span></span>
    * <span data-ttu-id="052f3-124">Importeer dit gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="052f3-124">Import this data model.</span></span> <span data-ttu-id="052f3-125">Het wordt als een gegevensbron in een nieuwe indelingsconfiguratie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="052f3-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="052f3-126">Sla deze stap over als deze configuratie al is geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="052f3-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="052f3-127">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="052f3-127">Click Yes.</span></span>
13. <span data-ttu-id="052f3-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="052f3-128">Close the page.</span></span>
14. <span data-ttu-id="052f3-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="052f3-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="052f3-130">Een nieuwe indelingsconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="052f3-130">Create a new format configuration</span></span>
1. <span data-ttu-id="052f3-131">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="052f3-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="052f3-132">Selecteer Betalingsmodel in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="052f3-133">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="052f3-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="052f3-134">Voer in het veld Nieuw veld "Indeling gebaseerd op gegevensmodel PaymentModel" in.</span><span class="sxs-lookup"><span data-stu-id="052f3-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="052f3-135">Maak een indeling die op het gegevensmodel PaymentModel is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="052f3-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="052f3-136">Typ Voorbeeldwerkbladrapport in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="052f3-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="052f3-137">Voorbeeldwerkbladrapport</span><span class="sxs-lookup"><span data-stu-id="052f3-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="052f3-138">Typ Voorbeeldwerkbladrapport voor leveranciersbetalingen in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="052f3-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="052f3-139">Voorbeeldwerkbladrapport voor betalingen van leveranciers.</span><span class="sxs-lookup"><span data-stu-id="052f3-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="052f3-140">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="052f3-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="052f3-141">Selecteer de definitie 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="052f3-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="052f3-142">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="052f3-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="052f3-143">Een nieuw document in OPENXML-werkbladindeling ontwerpen</span><span class="sxs-lookup"><span data-stu-id="052f3-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="052f3-144">Selecteer Betalingsmodel\Voorbeeldwerkbladrapport in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="052f3-145">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="052f3-145">Click Designer.</span></span>
3. <span data-ttu-id="052f3-146">Klik in het actievenster op Importeren.</span><span class="sxs-lookup"><span data-stu-id="052f3-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="052f3-147">Klik op Importeren uit Excel.</span><span class="sxs-lookup"><span data-stu-id="052f3-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="052f3-148">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="052f3-148">Click Attachments.</span></span>
    * <span data-ttu-id="052f3-149">Voeg het bestaande Excel-document als een sjabloon toe.</span><span class="sxs-lookup"><span data-stu-id="052f3-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="052f3-150">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="052f3-150">Click New.</span></span>
7. <span data-ttu-id="052f3-151">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="052f3-151">Click File.</span></span>
    * <span data-ttu-id="052f3-152">Wijs naar het bestaande Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="052f3-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="052f3-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="052f3-153">Close the page.</span></span>
9. <span data-ttu-id="052f3-154">Typ of selecteer een waarde in het veld Sjabloon.</span><span class="sxs-lookup"><span data-stu-id="052f3-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="052f3-155">Selecteer het gekoppelde Excel-bestand dat als sjabloon moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="052f3-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="052f3-156">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="052f3-156">Click OK.</span></span>
    * <span data-ttu-id="052f3-157">ER-indelingscomponenten zijn gemaakt in de ontwerpende indeling op basis van de structuur van het verwijzende MS Excel-document (benoemde bereiken).</span><span class="sxs-lookup"><span data-stu-id="052f3-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="052f3-158">Een nieuwe gegevensbron maken om totalen per valutacode te berekenen</span><span class="sxs-lookup"><span data-stu-id="052f3-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="052f3-159">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="052f3-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="052f3-160">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="052f3-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="052f3-161">Selecteer in de structuur Functies\Groeperen op.</span><span class="sxs-lookup"><span data-stu-id="052f3-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="052f3-162">Typ PaymentByCurrency in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="052f3-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="052f3-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="052f3-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="052f3-164">Klik op Groeperen op bewerken</span><span class="sxs-lookup"><span data-stu-id="052f3-164">Click Edit group by.</span></span>
6. <span data-ttu-id="052f3-165">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="052f3-166">Selecteer "model\Payments" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="052f3-167">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="052f3-167">Click Add field to.</span></span>
9. <span data-ttu-id="052f3-168">Klik op Wat groeperen.</span><span class="sxs-lookup"><span data-stu-id="052f3-168">Click What to group.</span></span>
10. <span data-ttu-id="052f3-169">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="052f3-170">Selecteer 'model\Payments\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="052f3-171">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="052f3-171">Click Add field to.</span></span>
13. <span data-ttu-id="052f3-172">Klik op Gegroepeerde velden.</span><span class="sxs-lookup"><span data-stu-id="052f3-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="052f3-173">Selecteer 'model\Payments\Instructed Amount(InstructedAmount)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="052f3-174">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="052f3-174">Click Add field to.</span></span>
16. <span data-ttu-id="052f3-175">Klik op Aggregatievelden.</span><span class="sxs-lookup"><span data-stu-id="052f3-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="052f3-176">Selecteer een optie in het veld Methode.</span><span class="sxs-lookup"><span data-stu-id="052f3-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="052f3-177">Selecteer de aggregatiefunctie SUM.</span><span class="sxs-lookup"><span data-stu-id="052f3-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="052f3-178">Typ 'TotalInstructuredAmount' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="052f3-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="052f3-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="052f3-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="052f3-180">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="052f3-180">Click Save.</span></span>
20. <span data-ttu-id="052f3-181">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="052f3-181">Close the page.</span></span>
21. <span data-ttu-id="052f3-182">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="052f3-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="052f3-183">Indelingscomponenten aan gegevensbronnen toewijzen</span><span class="sxs-lookup"><span data-stu-id="052f3-183">Map format components to data sources</span></span>
1. <span data-ttu-id="052f3-184">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="052f3-185">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="052f3-186">Vouw 'model\Payments\Initiating Party(InitiatingParty)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="052f3-187">Selecteer 'model\Payments\Initiating Party(InitiatingParty)\Name' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="052f3-188">Vouw in de structuur 'Excel\ReportHeader' uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="052f3-189">Selecteer in de structuur 'Excel\ReportHeader\CompanyName'.</span><span class="sxs-lookup"><span data-stu-id="052f3-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="052f3-190">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-190">Click Bind.</span></span>
8. <span data-ttu-id="052f3-191">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="052f3-192">Vouw 'model\Payments\Creditor\Identification' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="052f3-193">Selecteer 'model\Payments\Creditor\Identification\Source ID(SourceID)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="052f3-194">Vouw in de structuur 'Excel\PaymLines' uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="052f3-195">Selecteer in de structuur 'Excel\PaymLines\VendAccountName'.</span><span class="sxs-lookup"><span data-stu-id="052f3-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="052f3-196">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-196">Click Bind.</span></span>
14. <span data-ttu-id="052f3-197">Selecteer "model\Payments\Creditor\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="052f3-198">Selecteer in de structuur 'Excel\PaymLines\VendName'.</span><span class="sxs-lookup"><span data-stu-id="052f3-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="052f3-199">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-199">Click Bind.</span></span>
17. <span data-ttu-id="052f3-200">Vouw 'model\Payments\Creditor Agent(CreditorAgent)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="052f3-201">Selecteer 'model\Payments\Creditor Agent(CreditorAgent)\Name' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="052f3-202">Selecteer in de structuur 'Excel\PaymLines\Bank'.</span><span class="sxs-lookup"><span data-stu-id="052f3-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="052f3-203">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-203">Click Bind.</span></span>
21. <span data-ttu-id="052f3-204">Selecteer 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="052f3-205">Selecteer in de structuur 'Excel\PaymLines\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="052f3-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="052f3-206">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-206">Click Bind.</span></span>
24. <span data-ttu-id="052f3-207">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)" uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="052f3-208">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)\Identification" uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="052f3-209">Selecteer 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="052f3-210">Selecteer in de structuur 'Excel\PaymLines\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="052f3-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="052f3-211">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-211">Click Bind.</span></span>
29. <span data-ttu-id="052f3-212">Selecteer 'model\Payments\Instructed Amount(InstructedAmount)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="052f3-213">Selecteer in de structuur 'Excel\PaymLines\Debit'.</span><span class="sxs-lookup"><span data-stu-id="052f3-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="052f3-214">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-214">Click Bind.</span></span>
32. <span data-ttu-id="052f3-215">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="052f3-216">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)" uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="052f3-217">Vouw 'model\Payments\Creditor Agent(CreditorAgent)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="052f3-218">Selecteer 'model\Payments\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="052f3-219">Selecteer in de structuur 'Excel\PaymLines\Currency'.</span><span class="sxs-lookup"><span data-stu-id="052f3-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="052f3-220">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-220">Click Bind.</span></span>
38. <span data-ttu-id="052f3-221">Vouw 'PaymentByCurrency' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="052f3-222">Vouw 'PaymentByCurrency\grouped' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="052f3-223">Selecteer 'PaymentByCurrency\grouped\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="052f3-224">Vouw in de structuur 'Excel\SummaryLines' uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="052f3-225">Selecteer in de structuur 'Excel\SummaryLines\SummaryCurrency'.</span><span class="sxs-lookup"><span data-stu-id="052f3-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="052f3-226">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-226">Click Bind.</span></span>
44. <span data-ttu-id="052f3-227">Vouw 'PaymentByCurrency\aggregated' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="052f3-228">Selecteer 'PaymentByCurrency\aggregated\TotalInstructuredAmount' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="052f3-229">Selecteer in de structuur 'Excel\SummaryLines\SummaryAmount'.</span><span class="sxs-lookup"><span data-stu-id="052f3-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="052f3-230">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-230">Click Bind.</span></span>
48. <span data-ttu-id="052f3-231">Selecteer 'PaymentByCurrency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="052f3-232">Selecteer in de structuur 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="052f3-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="052f3-233">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-233">Click Bind.</span></span>
51. <span data-ttu-id="052f3-234">Selecteer "model\Payments" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="052f3-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="052f3-235">Selecteer in de structuur 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="052f3-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="052f3-236">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="052f3-236">Click Bind.</span></span>
54. <span data-ttu-id="052f3-237">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="052f3-237">Click Save.</span></span>
55. <span data-ttu-id="052f3-238">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="052f3-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="052f3-239">De gemaakte configuratie gebruiken voor betalingsverwerking</span><span class="sxs-lookup"><span data-stu-id="052f3-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="052f3-240">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="052f3-240">Click Change status.</span></span>
2. <span data-ttu-id="052f3-241">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="052f3-241">Click Complete.</span></span>
3. <span data-ttu-id="052f3-242">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="052f3-242">Click OK.</span></span>
4. <span data-ttu-id="052f3-243">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="052f3-243">Close the page.</span></span>
5. <span data-ttu-id="052f3-244">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="052f3-244">Close the page.</span></span>
6. <span data-ttu-id="052f3-245">Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="052f3-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="052f3-246">Gebruik het snelfilter om op het veld Betalingsmethode te filteren met de waarde 'Electronisch'.</span><span class="sxs-lookup"><span data-stu-id="052f3-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="052f3-247">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="052f3-247">Electronic</span></span>  
8. <span data-ttu-id="052f3-248">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="052f3-248">Click Edit.</span></span>
9. <span data-ttu-id="052f3-249">Vouw de sectie Bestandsindelingen uit.</span><span class="sxs-lookup"><span data-stu-id="052f3-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="052f3-250">Selecteer Ja in het veld Algemene elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="052f3-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="052f3-251">Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.</span><span class="sxs-lookup"><span data-stu-id="052f3-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="052f3-252">Selecteer de configuratie ‘Voorbeeldwerkbladrapport’.</span><span class="sxs-lookup"><span data-stu-id="052f3-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="052f3-253">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="052f3-253">Click Save.</span></span>
13. <span data-ttu-id="052f3-254">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="052f3-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="052f3-255">De gemaakte configuratie gebruiken voor het testen van de verwerking van betalingsjournalen</span><span class="sxs-lookup"><span data-stu-id="052f3-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="052f3-256">Ga naar Leveranciers > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="052f3-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="052f3-257">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="052f3-257">Click New.</span></span>
    * <span data-ttu-id="052f3-258">Maak een nieuw betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="052f3-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="052f3-259">Typ 'VendPay' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="052f3-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="052f3-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="052f3-260">VendPay</span></span>  
4. <span data-ttu-id="052f3-261">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="052f3-261">Click Lines.</span></span>
5. <span data-ttu-id="052f3-262">Geef in het veld Account de waarde 'GB_SI_000001' op.</span><span class="sxs-lookup"><span data-stu-id="052f3-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="052f3-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="052f3-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="052f3-264">Stel Debet in op '1000'.</span><span class="sxs-lookup"><span data-stu-id="052f3-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="052f3-265">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="052f3-265">Click New.</span></span>
8. <span data-ttu-id="052f3-266">Geef in het veld Account de waarde 'GB_SI_000005' op.</span><span class="sxs-lookup"><span data-stu-id="052f3-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="052f3-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="052f3-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="052f3-268">Stel Debet in op '2000'.</span><span class="sxs-lookup"><span data-stu-id="052f3-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="052f3-269">Typ EUR in het veld Valuta.</span><span class="sxs-lookup"><span data-stu-id="052f3-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="052f3-270">EUR</span><span class="sxs-lookup"><span data-stu-id="052f3-270">EUR</span></span>  
11. <span data-ttu-id="052f3-271">Geef in het veld Tegenrekening de waarde 'GBSI OPER' op.</span><span class="sxs-lookup"><span data-stu-id="052f3-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="052f3-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="052f3-272">GBSI OPER</span></span>  
12. <span data-ttu-id="052f3-273">Typ Elektronisch in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="052f3-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="052f3-274">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="052f3-274">Electronic</span></span>  
13. <span data-ttu-id="052f3-275">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="052f3-275">Click Save.</span></span>
14. <span data-ttu-id="052f3-276">Klik op Betalingen genereren.</span><span class="sxs-lookup"><span data-stu-id="052f3-276">Click Generate payments.</span></span>
15. <span data-ttu-id="052f3-277">Typ Elektronisch in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="052f3-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="052f3-278">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="052f3-278">Electronic</span></span>  
16. <span data-ttu-id="052f3-279">Typ in het veld Bestandsnaam 'Betalingen'.</span><span class="sxs-lookup"><span data-stu-id="052f3-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="052f3-280">Typ bijvoorbeeld Betalingen.</span><span class="sxs-lookup"><span data-stu-id="052f3-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="052f3-281">Typ 'GBSI OPER' in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="052f3-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="052f3-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="052f3-282">GBSI OPER</span></span>  
18. <span data-ttu-id="052f3-283">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="052f3-283">Click OK.</span></span>
19. <span data-ttu-id="052f3-284">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="052f3-284">Click OK.</span></span>
    * <span data-ttu-id="052f3-285">Controleer het gemaakte werkblad, inclusief details van betalingsregels en totalen voor elke valutacode die in dit betalingsbericht wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="052f3-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


