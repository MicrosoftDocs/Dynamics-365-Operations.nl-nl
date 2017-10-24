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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 04def14ddf9b079005bf11acbcaf64b21aa80fdb
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="01f89-103">Een configuratie ontwerpen voor het genereren van rapporten in OpenXML-indeling voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="01f89-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01f89-104">In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een sjabloon bevat voor het genereren van elektronische documenten in OPENXML-indeling.</span><span class="sxs-lookup"><span data-stu-id="01f89-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="01f89-105">Deze configuratie wordt voor de verwerking van leveranciersbetalingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="01f89-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="01f89-106">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in GBSI-bedrijven worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="01f89-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="01f89-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="01f89-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="01f89-108">U moet ook een Excel-bestand hebben dat wordt geïmporteerd bij het maken van de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="01f89-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="01f89-109">Dit bestand kan worden geopend via: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="01f89-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="01f89-110">De gegevensmodelconfiguratie Betalingen uploaden</span><span class="sxs-lookup"><span data-stu-id="01f89-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="01f89-111">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="01f89-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="01f89-112">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="01f89-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="01f89-113">Selecteer de configuratieprovider voor het voorbeeldbedrijf Litware,Inc. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="01f89-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="01f89-114">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="01f89-114">Click Set active.</span></span>
4. <span data-ttu-id="01f89-115">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="01f89-115">Click Repositories.</span></span>
    * <span data-ttu-id="01f89-116">Selecteer een opslagplaats voor het type Bronnen voor bedrijfsactiviteiten, indien beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="01f89-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="01f89-117">Als deze beschikbaar is, slaat u de volgende stappen in verband met het maken van een nieuwe opslagplaats over.</span><span class="sxs-lookup"><span data-stu-id="01f89-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="01f89-118">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="01f89-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="01f89-119">Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.</span><span class="sxs-lookup"><span data-stu-id="01f89-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="01f89-120">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="01f89-120">Click Create repository.</span></span>
8. <span data-ttu-id="01f89-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="01f89-121">Click OK.</span></span>
9. <span data-ttu-id="01f89-122">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="01f89-122">Click Open.</span></span>
10. <span data-ttu-id="01f89-123">Selecteer Betalingsmodel in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="01f89-124">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="01f89-124">Click Import.</span></span>
    * <span data-ttu-id="01f89-125">Importeer dit gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="01f89-125">Import this data model.</span></span> <span data-ttu-id="01f89-126">Het wordt als een gegevensbron in een nieuwe indelingsconfiguratie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="01f89-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="01f89-127">Sla deze stap over als deze configuratie al is geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="01f89-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="01f89-128">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="01f89-128">Click Yes.</span></span>
13. <span data-ttu-id="01f89-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01f89-129">Close the page.</span></span>
14. <span data-ttu-id="01f89-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01f89-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="01f89-131">Een nieuwe indelingsconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="01f89-131">Create a new format configuration</span></span>
1. <span data-ttu-id="01f89-132">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="01f89-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="01f89-133">Selecteer Betalingsmodel in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="01f89-134">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="01f89-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="01f89-135">Voer in het veld Nieuw veld "Indeling gebaseerd op gegevensmodel PaymentModel" in.</span><span class="sxs-lookup"><span data-stu-id="01f89-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="01f89-136">Maak een indeling die op het gegevensmodel PaymentModel is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="01f89-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="01f89-137">Typ Voorbeeldwerkbladrapport in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="01f89-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="01f89-138">Voorbeeldwerkbladrapport</span><span class="sxs-lookup"><span data-stu-id="01f89-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="01f89-139">Typ Voorbeeldwerkbladrapport voor leveranciersbetalingen in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="01f89-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="01f89-140">Voorbeeldwerkbladrapport voor betalingen van leveranciers.</span><span class="sxs-lookup"><span data-stu-id="01f89-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="01f89-141">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="01f89-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="01f89-142">Selecteer de definitie 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="01f89-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="01f89-143">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="01f89-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="01f89-144">Een nieuw document in OPENXML-werkbladindeling ontwerpen</span><span class="sxs-lookup"><span data-stu-id="01f89-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="01f89-145">Selecteer Betalingsmodel\Voorbeeldwerkbladrapport in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="01f89-146">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="01f89-146">Click Designer.</span></span>
3. <span data-ttu-id="01f89-147">Klik in het actievenster op Importeren.</span><span class="sxs-lookup"><span data-stu-id="01f89-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="01f89-148">Klik op Importeren uit Excel.</span><span class="sxs-lookup"><span data-stu-id="01f89-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="01f89-149">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="01f89-149">Click Attachments.</span></span>
    * <span data-ttu-id="01f89-150">Voeg het bestaande Excel-document als een sjabloon toe.</span><span class="sxs-lookup"><span data-stu-id="01f89-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="01f89-151">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="01f89-151">Click New.</span></span>
7. <span data-ttu-id="01f89-152">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="01f89-152">Click File.</span></span>
    * <span data-ttu-id="01f89-153">Wijs naar het bestaande Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="01f89-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="01f89-154">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01f89-154">Close the page.</span></span>
9. <span data-ttu-id="01f89-155">Typ of selecteer een waarde in het veld Sjabloon.</span><span class="sxs-lookup"><span data-stu-id="01f89-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="01f89-156">Selecteer het gekoppelde Excel-bestand dat als sjabloon moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="01f89-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="01f89-157">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="01f89-157">Click OK.</span></span>
    * <span data-ttu-id="01f89-158">ER-indelingscomponenten zijn gemaakt in de ontwerpende indeling op basis van de structuur van het verwijzende MS Excel-document (benoemde bereiken).</span><span class="sxs-lookup"><span data-stu-id="01f89-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="01f89-159">Een nieuwe gegevensbron maken om totalen per valutacode te berekenen</span><span class="sxs-lookup"><span data-stu-id="01f89-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="01f89-160">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="01f89-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="01f89-161">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="01f89-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="01f89-162">Selecteer in de structuur Functies\Groeperen op.</span><span class="sxs-lookup"><span data-stu-id="01f89-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="01f89-163">Typ PaymentByCurrency in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="01f89-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="01f89-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="01f89-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="01f89-165">Klik op Groeperen op bewerken</span><span class="sxs-lookup"><span data-stu-id="01f89-165">Click Edit group by.</span></span>
6. <span data-ttu-id="01f89-166">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="01f89-167">Selecteer "model\Payments" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="01f89-168">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="01f89-168">Click Add field to.</span></span>
9. <span data-ttu-id="01f89-169">Klik op Wat groeperen.</span><span class="sxs-lookup"><span data-stu-id="01f89-169">Click What to group.</span></span>
10. <span data-ttu-id="01f89-170">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="01f89-171">Selecteer 'model\Payments\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="01f89-172">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="01f89-172">Click Add field to.</span></span>
13. <span data-ttu-id="01f89-173">Klik op Gegroepeerde velden.</span><span class="sxs-lookup"><span data-stu-id="01f89-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="01f89-174">Selecteer 'model\Payments\Instructed Amount(InstructedAmount)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="01f89-175">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="01f89-175">Click Add field to.</span></span>
16. <span data-ttu-id="01f89-176">Klik op Aggregatievelden.</span><span class="sxs-lookup"><span data-stu-id="01f89-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="01f89-177">Selecteer een optie in het veld Methode.</span><span class="sxs-lookup"><span data-stu-id="01f89-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="01f89-178">Selecteer de aggregatiefunctie SUM.</span><span class="sxs-lookup"><span data-stu-id="01f89-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="01f89-179">Typ 'TotalInstructuredAmount' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="01f89-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="01f89-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="01f89-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="01f89-181">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="01f89-181">Click Save.</span></span>
20. <span data-ttu-id="01f89-182">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01f89-182">Close the page.</span></span>
21. <span data-ttu-id="01f89-183">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="01f89-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="01f89-184">Indelingscomponenten aan gegevensbronnen toewijzen</span><span class="sxs-lookup"><span data-stu-id="01f89-184">Map format components to data sources</span></span>
1. <span data-ttu-id="01f89-185">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="01f89-186">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="01f89-187">Vouw 'model\Payments\Initiating Party(InitiatingParty)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="01f89-188">Selecteer 'model\Payments\Initiating Party(InitiatingParty)\Name' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="01f89-189">Vouw in de structuur 'Excel\ReportHeader' uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="01f89-190">Selecteer in de structuur 'Excel\ReportHeader\CompanyName'.</span><span class="sxs-lookup"><span data-stu-id="01f89-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="01f89-191">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-191">Click Bind.</span></span>
8. <span data-ttu-id="01f89-192">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="01f89-193">Vouw 'model\Payments\Creditor\Identification' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="01f89-194">Selecteer 'model\Payments\Creditor\Identification\Source ID(SourceID)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="01f89-195">Vouw in de structuur 'Excel\PaymLines' uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="01f89-196">Selecteer in de structuur 'Excel\PaymLines\VendAccountName'.</span><span class="sxs-lookup"><span data-stu-id="01f89-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="01f89-197">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-197">Click Bind.</span></span>
14. <span data-ttu-id="01f89-198">Selecteer "model\Payments\Creditor\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="01f89-199">Selecteer in de structuur 'Excel\PaymLines\VendName'.</span><span class="sxs-lookup"><span data-stu-id="01f89-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="01f89-200">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-200">Click Bind.</span></span>
17. <span data-ttu-id="01f89-201">Vouw 'model\Payments\Creditor Agent(CreditorAgent)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="01f89-202">Selecteer 'model\Payments\Creditor Agent(CreditorAgent)\Name' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="01f89-203">Selecteer in de structuur 'Excel\PaymLines\Bank'.</span><span class="sxs-lookup"><span data-stu-id="01f89-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="01f89-204">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-204">Click Bind.</span></span>
21. <span data-ttu-id="01f89-205">Selecteer 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="01f89-206">Selecteer in de structuur 'Excel\PaymLines\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="01f89-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="01f89-207">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-207">Click Bind.</span></span>
24. <span data-ttu-id="01f89-208">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)" uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="01f89-209">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)\Identification" uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="01f89-210">Selecteer 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="01f89-211">Selecteer in de structuur 'Excel\PaymLines\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="01f89-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="01f89-212">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-212">Click Bind.</span></span>
29. <span data-ttu-id="01f89-213">Selecteer 'model\Payments\Instructed Amount(InstructedAmount)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="01f89-214">Selecteer in de structuur 'Excel\PaymLines\Debit'.</span><span class="sxs-lookup"><span data-stu-id="01f89-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="01f89-215">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-215">Click Bind.</span></span>
32. <span data-ttu-id="01f89-216">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="01f89-217">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)" uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="01f89-218">Vouw 'model\Payments\Creditor Agent(CreditorAgent)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="01f89-219">Selecteer 'model\Payments\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="01f89-220">Selecteer in de structuur 'Excel\PaymLines\Currency'.</span><span class="sxs-lookup"><span data-stu-id="01f89-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="01f89-221">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-221">Click Bind.</span></span>
38. <span data-ttu-id="01f89-222">Vouw 'PaymentByCurrency' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="01f89-223">Vouw 'PaymentByCurrency\grouped' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="01f89-224">Selecteer 'PaymentByCurrency\grouped\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="01f89-225">Vouw in de structuur 'Excel\SummaryLines' uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="01f89-226">Selecteer in de structuur 'Excel\SummaryLines\SummaryCurrency'.</span><span class="sxs-lookup"><span data-stu-id="01f89-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="01f89-227">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-227">Click Bind.</span></span>
44. <span data-ttu-id="01f89-228">Vouw 'PaymentByCurrency\aggregated' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="01f89-229">Selecteer 'PaymentByCurrency\aggregated\TotalInstructuredAmount' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="01f89-230">Selecteer in de structuur 'Excel\SummaryLines\SummaryAmount'.</span><span class="sxs-lookup"><span data-stu-id="01f89-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="01f89-231">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-231">Click Bind.</span></span>
48. <span data-ttu-id="01f89-232">Selecteer 'PaymentByCurrency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="01f89-233">Selecteer in de structuur 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="01f89-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="01f89-234">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-234">Click Bind.</span></span>
51. <span data-ttu-id="01f89-235">Selecteer "model\Payments" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="01f89-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="01f89-236">Selecteer in de structuur 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="01f89-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="01f89-237">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="01f89-237">Click Bind.</span></span>
54. <span data-ttu-id="01f89-238">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="01f89-238">Click Save.</span></span>
55. <span data-ttu-id="01f89-239">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01f89-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="01f89-240">De gemaakte configuratie gebruiken voor betalingsverwerking</span><span class="sxs-lookup"><span data-stu-id="01f89-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="01f89-241">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="01f89-241">Click Change status.</span></span>
2. <span data-ttu-id="01f89-242">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="01f89-242">Click Complete.</span></span>
3. <span data-ttu-id="01f89-243">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="01f89-243">Click OK.</span></span>
4. <span data-ttu-id="01f89-244">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01f89-244">Close the page.</span></span>
5. <span data-ttu-id="01f89-245">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01f89-245">Close the page.</span></span>
6. <span data-ttu-id="01f89-246">Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="01f89-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="01f89-247">Gebruik het snelfilter om op het veld Betalingsmethode te filteren met de waarde 'Electronisch'.</span><span class="sxs-lookup"><span data-stu-id="01f89-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="01f89-248">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="01f89-248">Electronic</span></span>  
8. <span data-ttu-id="01f89-249">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="01f89-249">Click Edit.</span></span>
9. <span data-ttu-id="01f89-250">Vouw de sectie Bestandsindelingen uit.</span><span class="sxs-lookup"><span data-stu-id="01f89-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="01f89-251">Selecteer Ja in het veld Algemene elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="01f89-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="01f89-252">Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.</span><span class="sxs-lookup"><span data-stu-id="01f89-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="01f89-253">Selecteer de configuratie ‘Voorbeeldwerkbladrapport’.</span><span class="sxs-lookup"><span data-stu-id="01f89-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="01f89-254">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="01f89-254">Click Save.</span></span>
13. <span data-ttu-id="01f89-255">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="01f89-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="01f89-256">De gemaakte configuratie gebruiken voor het testen van de verwerking van betalingsjournalen</span><span class="sxs-lookup"><span data-stu-id="01f89-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="01f89-257">Ga naar Leveranciers > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="01f89-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="01f89-258">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="01f89-258">Click New.</span></span>
    * <span data-ttu-id="01f89-259">Maak een nieuw betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="01f89-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="01f89-260">Typ 'VendPay' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="01f89-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="01f89-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="01f89-261">VendPay</span></span>  
4. <span data-ttu-id="01f89-262">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="01f89-262">Click Lines.</span></span>
5. <span data-ttu-id="01f89-263">Geef in het veld Account de waarde 'GB_SI_000001' op.</span><span class="sxs-lookup"><span data-stu-id="01f89-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="01f89-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="01f89-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="01f89-265">Stel Debet in op '1000'.</span><span class="sxs-lookup"><span data-stu-id="01f89-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="01f89-266">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="01f89-266">Click New.</span></span>
8. <span data-ttu-id="01f89-267">Geef in het veld Account de waarde 'GB_SI_000005' op.</span><span class="sxs-lookup"><span data-stu-id="01f89-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="01f89-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="01f89-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="01f89-269">Stel Debet in op '2000'.</span><span class="sxs-lookup"><span data-stu-id="01f89-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="01f89-270">Typ EUR in het veld Valuta.</span><span class="sxs-lookup"><span data-stu-id="01f89-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="01f89-271">EUR</span><span class="sxs-lookup"><span data-stu-id="01f89-271">EUR</span></span>  
11. <span data-ttu-id="01f89-272">Geef in het veld Tegenrekening de waarde 'GBSI OPER' op.</span><span class="sxs-lookup"><span data-stu-id="01f89-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="01f89-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="01f89-273">GBSI OPER</span></span>  
12. <span data-ttu-id="01f89-274">Typ Elektronisch in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="01f89-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="01f89-275">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="01f89-275">Electronic</span></span>  
13. <span data-ttu-id="01f89-276">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="01f89-276">Click Save.</span></span>
14. <span data-ttu-id="01f89-277">Klik op Betalingen genereren.</span><span class="sxs-lookup"><span data-stu-id="01f89-277">Click Generate payments.</span></span>
15. <span data-ttu-id="01f89-278">Typ Elektronisch in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="01f89-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="01f89-279">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="01f89-279">Electronic</span></span>  
16. <span data-ttu-id="01f89-280">Typ in het veld Bestandsnaam 'Betalingen'.</span><span class="sxs-lookup"><span data-stu-id="01f89-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="01f89-281">Typ bijvoorbeeld Betalingen.</span><span class="sxs-lookup"><span data-stu-id="01f89-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="01f89-282">Typ 'GBSI OPER' in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="01f89-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="01f89-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="01f89-283">GBSI OPER</span></span>  
18. <span data-ttu-id="01f89-284">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="01f89-284">Click OK.</span></span>
19. <span data-ttu-id="01f89-285">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="01f89-285">Click OK.</span></span>
    * <span data-ttu-id="01f89-286">Controleer het gemaakte werkblad, inclusief details van betalingsregels en totalen voor elke valutacode die in dit betalingsbericht wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="01f89-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


