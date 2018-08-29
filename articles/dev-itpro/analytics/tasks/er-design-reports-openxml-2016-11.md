--- 
title: ER-configuraties ontwerpen om rapporten in OpenXML-indeling te genereren
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="a2f86-103">ER-configuraties ontwerpen om rapporten in OpenXML-indeling te genereren</span><span class="sxs-lookup"><span data-stu-id="a2f86-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2f86-104">In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een sjabloon bevat voor het genereren van elektronische documenten in OPENXML-indeling.</span><span class="sxs-lookup"><span data-stu-id="a2f86-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="a2f86-105">Deze configuratie wordt voor de verwerking van leveranciersbetalingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a2f86-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="a2f86-106">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in GBSI-bedrijven worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a2f86-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="a2f86-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="a2f86-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="a2f86-108">U moet ook het Microsoft Excel-bestand [Sjabloon van betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266) downloaden en opslaan.</span><span class="sxs-lookup"><span data-stu-id="a2f86-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="a2f86-109">De gegevensmodelconfiguratie Betalingen uploaden</span><span class="sxs-lookup"><span data-stu-id="a2f86-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="a2f86-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="a2f86-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a2f86-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a2f86-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a2f86-112">Selecteer de configuratieprovider voor het voorbeeldbedrijf Litware,Inc. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="a2f86-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="a2f86-113">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="a2f86-113">Click Set active.</span></span>
4. <span data-ttu-id="a2f86-114">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-114">Click Repositories.</span></span>
    * <span data-ttu-id="a2f86-115">Selecteer een opslagplaats voor het type Bronnen voor bedrijfsactiviteiten, indien beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="a2f86-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="a2f86-116">Als deze beschikbaar is, slaat u de volgende stappen in verband met het maken van een nieuwe opslagplaats over.</span><span class="sxs-lookup"><span data-stu-id="a2f86-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="a2f86-117">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="a2f86-118">Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.</span><span class="sxs-lookup"><span data-stu-id="a2f86-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="a2f86-119">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="a2f86-119">Click Create repository.</span></span>
8. <span data-ttu-id="a2f86-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a2f86-120">Click OK.</span></span>
9. <span data-ttu-id="a2f86-121">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-121">Click Open.</span></span>
10. <span data-ttu-id="a2f86-122">Selecteer Betalingsmodel in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="a2f86-123">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="a2f86-123">Click Import.</span></span>
    * <span data-ttu-id="a2f86-124">Importeer dit gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="a2f86-124">Import this data model.</span></span> <span data-ttu-id="a2f86-125">Het wordt als een gegevensbron in een nieuwe indelingsconfiguratie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a2f86-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="a2f86-126">Sla deze stap over als deze configuratie al is geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="a2f86-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="a2f86-127">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="a2f86-127">Click Yes.</span></span>
13. <span data-ttu-id="a2f86-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a2f86-128">Close the page.</span></span>
14. <span data-ttu-id="a2f86-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a2f86-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="a2f86-130">Een nieuwe indelingsconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="a2f86-130">Create a new format configuration</span></span>
1. <span data-ttu-id="a2f86-131">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="a2f86-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="a2f86-132">Selecteer Betalingsmodel in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="a2f86-133">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a2f86-134">Voer in het veld Nieuw veld "Indeling gebaseerd op gegevensmodel PaymentModel" in.</span><span class="sxs-lookup"><span data-stu-id="a2f86-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="a2f86-135">Maak een indeling die op het gegevensmodel PaymentModel is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="a2f86-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="a2f86-136">Typ Voorbeeldwerkbladrapport in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a2f86-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="a2f86-137">Voorbeeldwerkbladrapport</span><span class="sxs-lookup"><span data-stu-id="a2f86-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="a2f86-138">Typ Voorbeeldwerkbladrapport voor leveranciersbetalingen in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="a2f86-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="a2f86-139">Voorbeeldwerkbladrapport voor betalingen van leveranciers.</span><span class="sxs-lookup"><span data-stu-id="a2f86-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="a2f86-140">Typ of selecteer een waarde in het veld Definitie gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="a2f86-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="a2f86-141">Selecteer de definitie 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="a2f86-142">Klik op Configuratie maken.</span><span class="sxs-lookup"><span data-stu-id="a2f86-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="a2f86-143">Een nieuw document in OPENXML-werkbladindeling ontwerpen</span><span class="sxs-lookup"><span data-stu-id="a2f86-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="a2f86-144">Selecteer Betalingsmodel\Voorbeeldwerkbladrapport in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="a2f86-145">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="a2f86-145">Click Designer.</span></span>
3. <span data-ttu-id="a2f86-146">Klik in het actievenster op Importeren.</span><span class="sxs-lookup"><span data-stu-id="a2f86-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="a2f86-147">Klik op Importeren uit Excel.</span><span class="sxs-lookup"><span data-stu-id="a2f86-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="a2f86-148">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-148">Click Attachments.</span></span>
    * <span data-ttu-id="a2f86-149">Voeg het bestaande Excel-document als een sjabloon toe.</span><span class="sxs-lookup"><span data-stu-id="a2f86-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="a2f86-150">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a2f86-150">Click New.</span></span>
7. <span data-ttu-id="a2f86-151">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="a2f86-151">Click File.</span></span>
    * <span data-ttu-id="a2f86-152">Wijs naar het bestaande Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="a2f86-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="a2f86-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a2f86-153">Close the page.</span></span>
9. <span data-ttu-id="a2f86-154">Typ of selecteer een waarde in het veld Sjabloon.</span><span class="sxs-lookup"><span data-stu-id="a2f86-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="a2f86-155">Selecteer het gekoppelde Excel-bestand dat als sjabloon moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a2f86-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="a2f86-156">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a2f86-156">Click OK.</span></span>
    * <span data-ttu-id="a2f86-157">ER-indelingscomponenten zijn gemaakt in de ontwerpende indeling op basis van de structuur van het verwijzende MS Excel-document (benoemde bereiken).</span><span class="sxs-lookup"><span data-stu-id="a2f86-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="a2f86-158">Een nieuwe gegevensbron maken om totalen per valutacode te berekenen</span><span class="sxs-lookup"><span data-stu-id="a2f86-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="a2f86-159">Klik op het tabblad Toewijzing.</span><span class="sxs-lookup"><span data-stu-id="a2f86-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a2f86-160">Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="a2f86-161">Selecteer in de structuur Functies\Groeperen op.</span><span class="sxs-lookup"><span data-stu-id="a2f86-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="a2f86-162">Typ PaymentByCurrency in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a2f86-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="a2f86-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="a2f86-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="a2f86-164">Klik op Groeperen op bewerken</span><span class="sxs-lookup"><span data-stu-id="a2f86-164">Click Edit group by.</span></span>
6. <span data-ttu-id="a2f86-165">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="a2f86-166">Selecteer "model\Payments" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="a2f86-167">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="a2f86-167">Click Add field to.</span></span>
9. <span data-ttu-id="a2f86-168">Klik op Wat groeperen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-168">Click What to group.</span></span>
10. <span data-ttu-id="a2f86-169">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="a2f86-170">Selecteer 'model\Payments\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="a2f86-171">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="a2f86-171">Click Add field to.</span></span>
13. <span data-ttu-id="a2f86-172">Klik op Gegroepeerde velden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="a2f86-173">Selecteer 'model\Payments\Instructed Amount(InstructedAmount)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="a2f86-174">Klik op Veld toevoegen aan.</span><span class="sxs-lookup"><span data-stu-id="a2f86-174">Click Add field to.</span></span>
16. <span data-ttu-id="a2f86-175">Klik op Aggregatievelden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="a2f86-176">Selecteer een optie in het veld Methode.</span><span class="sxs-lookup"><span data-stu-id="a2f86-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="a2f86-177">Selecteer de aggregatiefunctie SUM.</span><span class="sxs-lookup"><span data-stu-id="a2f86-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="a2f86-178">Typ 'TotalInstructuredAmount' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a2f86-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="a2f86-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="a2f86-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="a2f86-180">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a2f86-180">Click Save.</span></span>
20. <span data-ttu-id="a2f86-181">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a2f86-181">Close the page.</span></span>
21. <span data-ttu-id="a2f86-182">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a2f86-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="a2f86-183">Indelingscomponenten aan gegevensbronnen toewijzen</span><span class="sxs-lookup"><span data-stu-id="a2f86-183">Map format components to data sources</span></span>
1. <span data-ttu-id="a2f86-184">Vouw in de structuur "model" uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="a2f86-185">Vouw "model\Payments" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="a2f86-186">Vouw 'model\Payments\Initiating Party(InitiatingParty)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="a2f86-187">Selecteer 'model\Payments\Initiating Party(InitiatingParty)\Name' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="a2f86-188">Vouw in de structuur 'Excel\ReportHeader' uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="a2f86-189">Selecteer in de structuur 'Excel\ReportHeader\CompanyName'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="a2f86-190">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-190">Click Bind.</span></span>
8. <span data-ttu-id="a2f86-191">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="a2f86-192">Vouw 'model\Payments\Creditor\Identification' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="a2f86-193">Selecteer 'model\Payments\Creditor\Identification\Source ID(SourceID)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="a2f86-194">Vouw in de structuur 'Excel\PaymLines' uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="a2f86-195">Selecteer in de structuur 'Excel\PaymLines\VendAccountName'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="a2f86-196">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-196">Click Bind.</span></span>
14. <span data-ttu-id="a2f86-197">Selecteer "model\Payments\Creditor\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="a2f86-198">Selecteer in de structuur 'Excel\PaymLines\VendName'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="a2f86-199">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-199">Click Bind.</span></span>
17. <span data-ttu-id="a2f86-200">Vouw 'model\Payments\Creditor Agent(CreditorAgent)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="a2f86-201">Selecteer 'model\Payments\Creditor Agent(CreditorAgent)\Name' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="a2f86-202">Selecteer in de structuur 'Excel\PaymLines\Bank'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="a2f86-203">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-203">Click Bind.</span></span>
21. <span data-ttu-id="a2f86-204">Selecteer 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="a2f86-205">Selecteer in de structuur 'Excel\PaymLines\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="a2f86-206">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-206">Click Bind.</span></span>
24. <span data-ttu-id="a2f86-207">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)" uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="a2f86-208">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)\Identification" uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="a2f86-209">Selecteer 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="a2f86-210">Selecteer in de structuur 'Excel\PaymLines\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="a2f86-211">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-211">Click Bind.</span></span>
29. <span data-ttu-id="a2f86-212">Selecteer 'model\Payments\Instructed Amount(InstructedAmount)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="a2f86-213">Selecteer in de structuur 'Excel\PaymLines\Debit'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="a2f86-214">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-214">Click Bind.</span></span>
32. <span data-ttu-id="a2f86-215">Vouw "model\Payments\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="a2f86-216">Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)" uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="a2f86-217">Vouw 'model\Payments\Creditor Agent(CreditorAgent)' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="a2f86-218">Selecteer 'model\Payments\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="a2f86-219">Selecteer in de structuur 'Excel\PaymLines\Currency'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="a2f86-220">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-220">Click Bind.</span></span>
38. <span data-ttu-id="a2f86-221">Vouw 'PaymentByCurrency' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="a2f86-222">Vouw 'PaymentByCurrency\grouped' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="a2f86-223">Selecteer 'PaymentByCurrency\grouped\Currency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="a2f86-224">Vouw in de structuur 'Excel\SummaryLines' uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="a2f86-225">Selecteer in de structuur 'Excel\SummaryLines\SummaryCurrency'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="a2f86-226">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-226">Click Bind.</span></span>
44. <span data-ttu-id="a2f86-227">Vouw 'PaymentByCurrency\aggregated' in de structuur uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="a2f86-228">Selecteer 'PaymentByCurrency\aggregated\TotalInstructuredAmount' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="a2f86-229">Selecteer in de structuur 'Excel\SummaryLines\SummaryAmount'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="a2f86-230">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-230">Click Bind.</span></span>
48. <span data-ttu-id="a2f86-231">Selecteer 'PaymentByCurrency' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="a2f86-232">Selecteer in de structuur 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="a2f86-233">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-233">Click Bind.</span></span>
51. <span data-ttu-id="a2f86-234">Selecteer "model\Payments" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="a2f86-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="a2f86-235">Selecteer in de structuur 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="a2f86-236">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-236">Click Bind.</span></span>
54. <span data-ttu-id="a2f86-237">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a2f86-237">Click Save.</span></span>
55. <span data-ttu-id="a2f86-238">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a2f86-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="a2f86-239">De gemaakte configuratie gebruiken voor betalingsverwerking</span><span class="sxs-lookup"><span data-stu-id="a2f86-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="a2f86-240">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-240">Click Change status.</span></span>
2. <span data-ttu-id="a2f86-241">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="a2f86-241">Click Complete.</span></span>
3. <span data-ttu-id="a2f86-242">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a2f86-242">Click OK.</span></span>
4. <span data-ttu-id="a2f86-243">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a2f86-243">Close the page.</span></span>
5. <span data-ttu-id="a2f86-244">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a2f86-244">Close the page.</span></span>
6. <span data-ttu-id="a2f86-245">Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.</span><span class="sxs-lookup"><span data-stu-id="a2f86-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="a2f86-246">Gebruik het snelfilter om op het veld Betalingsmethode te filteren met de waarde 'Electronisch'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="a2f86-247">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="a2f86-247">Electronic</span></span>  
8. <span data-ttu-id="a2f86-248">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="a2f86-248">Click Edit.</span></span>
9. <span data-ttu-id="a2f86-249">Vouw de sectie Bestandsindelingen uit.</span><span class="sxs-lookup"><span data-stu-id="a2f86-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="a2f86-250">Selecteer Ja in het veld Algemene elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="a2f86-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="a2f86-251">Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.</span><span class="sxs-lookup"><span data-stu-id="a2f86-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="a2f86-252">Selecteer de configuratie ‘Voorbeeldwerkbladrapport’.</span><span class="sxs-lookup"><span data-stu-id="a2f86-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="a2f86-253">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a2f86-253">Click Save.</span></span>
13. <span data-ttu-id="a2f86-254">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a2f86-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="a2f86-255">De gemaakte configuratie gebruiken voor het testen van de verwerking van betalingsjournalen</span><span class="sxs-lookup"><span data-stu-id="a2f86-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="a2f86-256">Ga naar Leveranciers > Betalingen > Betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="a2f86-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="a2f86-257">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a2f86-257">Click New.</span></span>
    * <span data-ttu-id="a2f86-258">Maak een nieuw betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="a2f86-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="a2f86-259">Typ 'VendPay' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="a2f86-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="a2f86-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="a2f86-260">VendPay</span></span>  
4. <span data-ttu-id="a2f86-261">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="a2f86-261">Click Lines.</span></span>
5. <span data-ttu-id="a2f86-262">Geef in het veld Account de waarde 'GB_SI_000001' op.</span><span class="sxs-lookup"><span data-stu-id="a2f86-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="a2f86-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="a2f86-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="a2f86-264">Stel Debet in op '1000'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="a2f86-265">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a2f86-265">Click New.</span></span>
8. <span data-ttu-id="a2f86-266">Geef in het veld Account de waarde 'GB_SI_000005' op.</span><span class="sxs-lookup"><span data-stu-id="a2f86-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="a2f86-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="a2f86-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="a2f86-268">Stel Debet in op '2000'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="a2f86-269">Typ EUR in het veld Valuta.</span><span class="sxs-lookup"><span data-stu-id="a2f86-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="a2f86-270">EUR</span><span class="sxs-lookup"><span data-stu-id="a2f86-270">EUR</span></span>  
11. <span data-ttu-id="a2f86-271">Geef in het veld Tegenrekening de waarde 'GBSI OPER' op.</span><span class="sxs-lookup"><span data-stu-id="a2f86-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="a2f86-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="a2f86-272">GBSI OPER</span></span>  
12. <span data-ttu-id="a2f86-273">Typ Elektronisch in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="a2f86-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="a2f86-274">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="a2f86-274">Electronic</span></span>  
13. <span data-ttu-id="a2f86-275">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a2f86-275">Click Save.</span></span>
14. <span data-ttu-id="a2f86-276">Klik op Betalingen genereren.</span><span class="sxs-lookup"><span data-stu-id="a2f86-276">Click Generate payments.</span></span>
15. <span data-ttu-id="a2f86-277">Typ Elektronisch in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="a2f86-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="a2f86-278">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="a2f86-278">Electronic</span></span>  
16. <span data-ttu-id="a2f86-279">Typ in het veld Bestandsnaam 'Betalingen'.</span><span class="sxs-lookup"><span data-stu-id="a2f86-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="a2f86-280">Typ bijvoorbeeld Betalingen.</span><span class="sxs-lookup"><span data-stu-id="a2f86-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="a2f86-281">Typ 'GBSI OPER' in het veld Bankrekening.</span><span class="sxs-lookup"><span data-stu-id="a2f86-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="a2f86-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="a2f86-282">GBSI OPER</span></span>  
18. <span data-ttu-id="a2f86-283">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a2f86-283">Click OK.</span></span>
19. <span data-ttu-id="a2f86-284">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a2f86-284">Click OK.</span></span>
    * <span data-ttu-id="a2f86-285">Controleer het gemaakte werkblad, inclusief details van betalingsregels en totalen voor elke valutacode die in dit betalingsbericht wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a2f86-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


