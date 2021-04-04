---
title: ER-modeltoewijzingen definiëren en gegevensbronnen hiervoor selecteren
description: In dit onderwerp wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage gegevensbronnen kan selecteren voor een ER-gegevensmodel (elektronische rapportage).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b5f291372bc459bc1979dca4a95cfafb39e2ad9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567289"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="e222a-103">ER-modeltoewijzingen definiëren en gegevensbronnen hiervoor selecteren</span><span class="sxs-lookup"><span data-stu-id="e222a-103">Define ER model mappings and select data sources for them</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e222a-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage gegevensbronnen kan selecteren voor een ER-gegevensmodel (elektronische rapportage).</span><span class="sxs-lookup"><span data-stu-id="e222a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="e222a-105">De gegevensbronnen worden verbonden met afzonderlijke onderdelen van het geselecteerde gegevensmodel tijdens ontwerptijd en vullen zakelijke gegevens in dat gegevensmodel in tijdens de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="e222a-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="e222a-106">In dit voorbeeld selecteert u gegevensbronnen voor een bestaand gegevensmodel dat voor het voorbeeldbedrijf, Litware, Inc. is gemaakt. Als u deze stappen wilt uitvoeren, moet u de stappen in de procedure "Een nieuw gegevensmodel maken" eerst uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e222a-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Create a new data model" procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="e222a-107">De structuur met ER-configuraties openen</span><span class="sxs-lookup"><span data-stu-id="e222a-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="e222a-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="e222a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e222a-109">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="e222a-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="e222a-110">Een nieuwe modeltoewijzing invoegen</span><span class="sxs-lookup"><span data-stu-id="e222a-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="e222a-111">Selecteer "Payments (simplified model)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="e222a-112">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="e222a-112">Click Designer.</span></span>
3. <span data-ttu-id="e222a-113">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="e222a-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="e222a-114">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e222a-114">Click New.</span></span>
    * <span data-ttu-id="e222a-115">Hiermee wordt een nieuwe record gemaakt waarmee het gegevensmodel wordt toegewezen aan gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="e222a-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="e222a-116">In dit voorbeeld wijst u het gegevensmodel toe aan gegevensbronnen voor het gewenste betalingstype: kredietoverdracht.</span><span class="sxs-lookup"><span data-stu-id="e222a-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="e222a-117">Het is mogelijk om meer dan één toewijzing te ontwerpen voor een bepaald gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="e222a-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="e222a-118">Zo kunt u bijvoorbeeld een toewijzing maken voor de verschillende typen betalingen, zoals voor automatische afschrijving of voor kredietoverdrachten.</span><span class="sxs-lookup"><span data-stu-id="e222a-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="e222a-119">In dit voorbeeld maakt u een toewijzing voor kredietoverdrachten.</span><span class="sxs-lookup"><span data-stu-id="e222a-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="e222a-120">Typ "CT-toewijzing" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e222a-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="e222a-121">CT-toewijzing</span><span class="sxs-lookup"><span data-stu-id="e222a-121">CT mapping</span></span>  
6. <span data-ttu-id="e222a-122">Typ "Betalingsmodel voor CT-toewijzing" in het veld Beschrijving.</span><span class="sxs-lookup"><span data-stu-id="e222a-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="e222a-123">Betalingsmodel voor CT-toewijzing</span><span class="sxs-lookup"><span data-stu-id="e222a-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="e222a-124">Typ in het veld Definitie: 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="e222a-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="e222a-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="e222a-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="e222a-126">ResolveChanges de definitie.</span><span class="sxs-lookup"><span data-stu-id="e222a-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="e222a-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e222a-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="e222a-128">Vereiste gegevensbronnen voor de huidige modeltoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="e222a-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="e222a-129">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="e222a-129">Click Designer.</span></span>
2. <span data-ttu-id="e222a-130">Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.</span><span class="sxs-lookup"><span data-stu-id="e222a-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="e222a-131">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-131">Click Add root.</span></span>
    * <span data-ttu-id="e222a-132">Voer deze gegevensbron in om toegang te krijgen tot betalingstransacties.</span><span class="sxs-lookup"><span data-stu-id="e222a-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="e222a-133">Typ "Transacties" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e222a-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="e222a-134">Transacties</span><span class="sxs-lookup"><span data-stu-id="e222a-134">Transactions</span></span>  
5. <span data-ttu-id="e222a-135">Typ "Transacties" in het veld Label.</span><span class="sxs-lookup"><span data-stu-id="e222a-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="e222a-136">Transacties</span><span class="sxs-lookup"><span data-stu-id="e222a-136">Transactions</span></span>  
6. <span data-ttu-id="e222a-137">Typ "Grootboekjournaalregels" in het veld Help.</span><span class="sxs-lookup"><span data-stu-id="e222a-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="e222a-138">Grootboekjournaalregels</span><span class="sxs-lookup"><span data-stu-id="e222a-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="e222a-139">Selecteer Ja in het veld Vragen om query.</span><span class="sxs-lookup"><span data-stu-id="e222a-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="e222a-140">Selecteer Ja.</span><span class="sxs-lookup"><span data-stu-id="e222a-140">Select Yes.</span></span>  
8. <span data-ttu-id="e222a-141">Typ "LedgerJournalTrans" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="e222a-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="e222a-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="e222a-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="e222a-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e222a-143">Click OK.</span></span>
    * <span data-ttu-id="e222a-144">Selecteer de tabel LedgerJournalTrans als gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="e222a-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="e222a-145">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="e222a-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-146">Click Add.</span></span>
    * <span data-ttu-id="e222a-147">Klik op Toevoegen om een nieuw berekend veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="e222a-148">Typ "$EndToEndID" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e222a-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="e222a-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="e222a-149">$EndToEndID</span></span>  
13. <span data-ttu-id="e222a-150">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="e222a-150">Click Edit formula.</span></span>
14. <span data-ttu-id="e222a-151">Selecteer "String\CONCATENATE" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="e222a-152">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-152">Click Add function.</span></span>
16. <span data-ttu-id="e222a-153">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="e222a-154">Selecteer "Transactions\Voucher" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="e222a-155">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-155">Click Add data source.</span></span>
19. <span data-ttu-id="e222a-156">Typ in het veld Formule: 'CONCATENATE(Transactions.Voucher, "-", '. (Let op de spatie tussen komma en enkel aanhalingsteken.)</span><span class="sxs-lookup"><span data-stu-id="e222a-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="e222a-157">Typ [ , "-", ] aan het einde van de formule.</span><span class="sxs-lookup"><span data-stu-id="e222a-157">Type [ , "-", ] at the end of the formula.</span></span>  
20. <span data-ttu-id="e222a-158">Selecteer "String\TEXT" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="e222a-159">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-159">Click Add function.</span></span>
22. <span data-ttu-id="e222a-160">Selecteer "Transactions\Record-ID(RecId)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="e222a-161">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-161">Click Add data source.</span></span>
24. <span data-ttu-id="e222a-162">Typ in het veld Formule: 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="e222a-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="e222a-163">Typ [))] aan het einde van de formule.</span><span class="sxs-lookup"><span data-stu-id="e222a-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="e222a-164">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e222a-164">Click Save.</span></span>
    * <span data-ttu-id="e222a-165">Controleer of er geen fouten zijn gevonden voor de gemaakte formule.</span><span class="sxs-lookup"><span data-stu-id="e222a-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="e222a-166">Zie het tabblad FOUTEN onder het bedieningselement voor de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="e222a-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="e222a-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e222a-167">Close the page.</span></span>
27. <span data-ttu-id="e222a-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e222a-168">Click OK.</span></span>
    * <span data-ttu-id="e222a-169">Voeg het berekende veld toe aan deze gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="e222a-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="e222a-170">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-170">Click Add.</span></span>
    * <span data-ttu-id="e222a-171">Klik op Toevoegen om een nieuw berekend veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="e222a-172">Typ "$Amount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e222a-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="e222a-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="e222a-173">$Amount</span></span>  
30. <span data-ttu-id="e222a-174">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="e222a-174">Click Edit formula.</span></span>
31. <span data-ttu-id="e222a-175">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="e222a-176">Selecteer "Transactions\Debit(AmountCurDebit)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="e222a-177">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-177">Click Add data source.</span></span>
34. <span data-ttu-id="e222a-178">Typ in het veld Formule: 'Transactions.AmountCurDebit - '. (Let op de spatie tussen minus-teken en enkel aanhalingsteken.)</span><span class="sxs-lookup"><span data-stu-id="e222a-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="e222a-179">Typ [ - ] aan het einde van de formule.</span><span class="sxs-lookup"><span data-stu-id="e222a-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="e222a-180">Selecteer "Transactions\Credit(AmountCurCredit)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="e222a-181">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-181">Click Add data source.</span></span>
37. <span data-ttu-id="e222a-182">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e222a-182">Click Save.</span></span>
38. <span data-ttu-id="e222a-183">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e222a-183">Close the page.</span></span>
39. <span data-ttu-id="e222a-184">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e222a-184">Click OK.</span></span>
    * <span data-ttu-id="e222a-185">Hiermee wordt het berekende veld $Amount toegevoegd aan de geselecteerde gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="e222a-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="e222a-186">Selecteer 'Transactions\$Amount' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="e222a-187">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="e222a-188">Zoek in de structuur 'Transactions\$Amount' en vouw dit uit of samen.</span><span class="sxs-lookup"><span data-stu-id="e222a-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="e222a-189">Vouw in de structuur 'Transactions' uit of samen.</span><span class="sxs-lookup"><span data-stu-id="e222a-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="e222a-190">Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.</span><span class="sxs-lookup"><span data-stu-id="e222a-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="e222a-191">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-191">Click Add root.</span></span>
    * <span data-ttu-id="e222a-192">Voer deze gegevensbron in om toegang te krijgen tot de bankrekeninggegevens van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="e222a-192">Enter this data source to access the company's bank account details.</span></span>  
46. <span data-ttu-id="e222a-193">Typ "BankAccount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e222a-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="e222a-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="e222a-194">BankAccount</span></span>  
47. <span data-ttu-id="e222a-195">Typ "Bankrekening" in het veld Label.</span><span class="sxs-lookup"><span data-stu-id="e222a-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="e222a-196">Bankrekening</span><span class="sxs-lookup"><span data-stu-id="e222a-196">Bank Account</span></span>  
48. <span data-ttu-id="e222a-197">Typ "Bankrekening" in het veld Help.</span><span class="sxs-lookup"><span data-stu-id="e222a-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="e222a-198">Bankrekening</span><span class="sxs-lookup"><span data-stu-id="e222a-198">Bank Account</span></span>  
49. <span data-ttu-id="e222a-199">Selecteer Ja in het veld Vragen om query.</span><span class="sxs-lookup"><span data-stu-id="e222a-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="e222a-200">Selecteer Ja.</span><span class="sxs-lookup"><span data-stu-id="e222a-200">Select Yes.</span></span>  
50. <span data-ttu-id="e222a-201">Typ "BankAccountTable" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="e222a-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="e222a-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="e222a-202">BankAccountTable</span></span>  
51. <span data-ttu-id="e222a-203">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e222a-203">Click OK.</span></span>
    * <span data-ttu-id="e222a-204">Selecteer de tabel BankAccountTable als gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="e222a-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="e222a-205">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-205">Click Add root.</span></span>
    * <span data-ttu-id="e222a-206">Voer deze gegevensbron in om toegang te krijgen tot de vereisten van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="e222a-206">Enter this data source to access the company's requisites.</span></span>  
53. <span data-ttu-id="e222a-207">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e222a-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="e222a-208">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="e222a-208">Company</span></span>  
54. <span data-ttu-id="e222a-209">Typ een waarde in het veld Label.</span><span class="sxs-lookup"><span data-stu-id="e222a-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="e222a-210">Bedrijfsgegevens</span><span class="sxs-lookup"><span data-stu-id="e222a-210">Company information</span></span>  
55. <span data-ttu-id="e222a-211">Typ "Bedrijfsinformatie" in het veld Help.</span><span class="sxs-lookup"><span data-stu-id="e222a-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="e222a-212">Bedrijfsgegevens</span><span class="sxs-lookup"><span data-stu-id="e222a-212">Company information</span></span>  
56. <span data-ttu-id="e222a-213">Selecteer Ja in het veld Vragen om query.</span><span class="sxs-lookup"><span data-stu-id="e222a-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="e222a-214">Selecteer Ja.</span><span class="sxs-lookup"><span data-stu-id="e222a-214">Select Yes.</span></span>  
57. <span data-ttu-id="e222a-215">Typ "CompanyInfo" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="e222a-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="e222a-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="e222a-216">CompanyInfo</span></span>  
58. <span data-ttu-id="e222a-217">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e222a-217">Click OK.</span></span>
    * <span data-ttu-id="e222a-218">Selecteer de tabel CompanyInfo als gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="e222a-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="e222a-219">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="e222a-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="e222a-220">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-220">Click Add root.</span></span>
    * <span data-ttu-id="e222a-221">Voeg een berekend veld in als nieuwe gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="e222a-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="e222a-222">Typ "ProcessingDateTime" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e222a-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="e222a-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="e222a-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="e222a-224">Typ Verwerkingsdatum en -tijd in het veld Label.</span><span class="sxs-lookup"><span data-stu-id="e222a-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="e222a-225">Verwerkingsdatum en -tijd</span><span class="sxs-lookup"><span data-stu-id="e222a-225">Processing date & time</span></span>  
63. <span data-ttu-id="e222a-226">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="e222a-226">Click Edit formula.</span></span>
64. <span data-ttu-id="e222a-227">Selecteer in de structuur 'Date/time\SESSIONNOW'.</span><span class="sxs-lookup"><span data-stu-id="e222a-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="e222a-228">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e222a-228">Click Add function.</span></span>
66. <span data-ttu-id="e222a-229">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e222a-229">Click Save.</span></span>
67. <span data-ttu-id="e222a-230">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e222a-230">Close the page.</span></span>
68. <span data-ttu-id="e222a-231">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e222a-231">Click OK.</span></span>
    * <span data-ttu-id="e222a-232">Voeg het berekende veld ProcessingDateTime toe als gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="e222a-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="e222a-233">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e222a-233">Click Save.</span></span>
70. <span data-ttu-id="e222a-234">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e222a-234">Close the page.</span></span>
71. <span data-ttu-id="e222a-235">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e222a-235">Close the page.</span></span>
72. <span data-ttu-id="e222a-236">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e222a-236">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]