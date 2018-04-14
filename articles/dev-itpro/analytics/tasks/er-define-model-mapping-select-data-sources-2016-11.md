--- 
title: "Modeltoewijzing definiëren en gegevensbronnen selecteren voor elektronische aangifte (ER)"
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage gegevensbronnen kan selecteren voor een ER-gegevensmodel (elektronische rapportage).
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e04ff56da694b9c72a72b0a7f130433f34241e78
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="88f18-103">Modeltoewijzing definiëren en gegevensbronnen selecteren voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="88f18-103">Define model mapping and select data sources for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88f18-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage gegevensbronnen kan selecteren voor een ER-gegevensmodel (elektronische rapportage).</span><span class="sxs-lookup"><span data-stu-id="88f18-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="88f18-105">De gegevensbronnen worden verbonden met afzonderlijke onderdelen van het geselecteerde gegevensmodel tijdens ontwerptijd en vullen zakelijke gegevens in dat gegevensmodel in tijdens de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="88f18-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="88f18-106">In dit voorbeeld selecteert u gegevensbronnen voor een bestaand gegevensmodel dat voor het voorbeeldbedrijf, Litware, Inc. is gemaakt. Als u deze stappen wilt uitvoeren, moet u de stappen in de procedure Een nieuw gegevensmodel maken eerst uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="88f18-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="88f18-107">De structuur met ER-configuraties openen</span><span class="sxs-lookup"><span data-stu-id="88f18-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="88f18-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="88f18-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="88f18-109">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="88f18-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="88f18-110">Een nieuwe modeltoewijzing invoegen</span><span class="sxs-lookup"><span data-stu-id="88f18-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="88f18-111">Selecteer "Payments (simplified model)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="88f18-112">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="88f18-112">Click Designer.</span></span>
3. <span data-ttu-id="88f18-113">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="88f18-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="88f18-114">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="88f18-114">Click New.</span></span>
    * <span data-ttu-id="88f18-115">Hiermee wordt een nieuwe record gemaakt waarmee het gegevensmodel wordt toegewezen aan gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="88f18-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="88f18-116">In dit voorbeeld wijst u het gegevensmodel toe aan gegevensbronnen voor het gewenste betalingstype: kredietoverdracht.</span><span class="sxs-lookup"><span data-stu-id="88f18-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="88f18-117">Het is mogelijk om meer dan één toewijzing te ontwerpen voor een bepaald gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="88f18-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="88f18-118">Zo kunt u bijvoorbeeld een toewijzing maken voor de verschillende typen betalingen, zoals voor automatische afschrijving of voor kredietoverdrachten.</span><span class="sxs-lookup"><span data-stu-id="88f18-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="88f18-119">In dit voorbeeld maakt u een toewijzing voor kredietoverdrachten.</span><span class="sxs-lookup"><span data-stu-id="88f18-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="88f18-120">Typ "CT-toewijzing" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="88f18-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="88f18-121">CT-toewijzing</span><span class="sxs-lookup"><span data-stu-id="88f18-121">CT mapping</span></span>  
6. <span data-ttu-id="88f18-122">Typ "Betalingsmodel voor CT-toewijzing" in het veld Beschrijving.</span><span class="sxs-lookup"><span data-stu-id="88f18-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="88f18-123">Betalingsmodel voor CT-toewijzing</span><span class="sxs-lookup"><span data-stu-id="88f18-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="88f18-124">Typ in het veld Definitie: 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="88f18-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="88f18-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="88f18-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="88f18-126">ResolveChanges de definitie.</span><span class="sxs-lookup"><span data-stu-id="88f18-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="88f18-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88f18-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="88f18-128">Vereiste gegevensbronnen voor de huidige modeltoewijzing definiëren</span><span class="sxs-lookup"><span data-stu-id="88f18-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="88f18-129">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="88f18-129">Click Designer.</span></span>
2. <span data-ttu-id="88f18-130">Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.</span><span class="sxs-lookup"><span data-stu-id="88f18-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="88f18-131">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-131">Click Add root.</span></span>
    * <span data-ttu-id="88f18-132">Voer deze gegevensbron in om toegang te krijgen tot betalingstransacties.</span><span class="sxs-lookup"><span data-stu-id="88f18-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="88f18-133">Typ "Transacties" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="88f18-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="88f18-134">Transacties</span><span class="sxs-lookup"><span data-stu-id="88f18-134">Transactions</span></span>  
5. <span data-ttu-id="88f18-135">Typ "Transacties" in het veld Label.</span><span class="sxs-lookup"><span data-stu-id="88f18-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="88f18-136">Transacties</span><span class="sxs-lookup"><span data-stu-id="88f18-136">Transactions</span></span>  
6. <span data-ttu-id="88f18-137">Typ "Grootboekjournaalregels" in het veld Help.</span><span class="sxs-lookup"><span data-stu-id="88f18-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="88f18-138">Grootboekjournaalregels</span><span class="sxs-lookup"><span data-stu-id="88f18-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="88f18-139">Selecteer Ja in het veld Vragen om query.</span><span class="sxs-lookup"><span data-stu-id="88f18-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="88f18-140">Selecteer Ja.</span><span class="sxs-lookup"><span data-stu-id="88f18-140">Select Yes.</span></span>  
8. <span data-ttu-id="88f18-141">Typ "LedgerJournalTrans" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="88f18-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="88f18-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="88f18-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="88f18-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="88f18-143">Click OK.</span></span>
    * <span data-ttu-id="88f18-144">Selecteer de tabel LedgerJournalTrans als gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="88f18-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="88f18-145">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="88f18-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-146">Click Add.</span></span>
    * <span data-ttu-id="88f18-147">Klik op Toevoegen om een nieuw berekend veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="88f18-148">Typ "$EndToEndID" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="88f18-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="88f18-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="88f18-149">$EndToEndID</span></span>  
13. <span data-ttu-id="88f18-150">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="88f18-150">Click Edit formula.</span></span>
14. <span data-ttu-id="88f18-151">Selecteer "String\CONCATENATE" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="88f18-152">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-152">Click Add function.</span></span>
16. <span data-ttu-id="88f18-153">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="88f18-154">Selecteer "Transactions\Voucher" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="88f18-155">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-155">Click Add data source.</span></span>
19. <span data-ttu-id="88f18-156">Typ in het veld Formule: 'CONCATENATE(Transactions.Voucher, "-", '. (Let op de spatie tussen komma en enkel aanhalingsteken.)</span><span class="sxs-lookup"><span data-stu-id="88f18-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="88f18-157">Typ [ , "- ", ] aan het einde van de formule.</span><span class="sxs-lookup"><span data-stu-id="88f18-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="88f18-158">Selecteer "String\TEXT" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="88f18-159">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-159">Click Add function.</span></span>
22. <span data-ttu-id="88f18-160">Selecteer "Transactions\Record-ID(RecId)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="88f18-161">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-161">Click Add data source.</span></span>
24. <span data-ttu-id="88f18-162">Typ in het veld Formule: 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="88f18-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="88f18-163">Typ [))] aan het einde van de formule.</span><span class="sxs-lookup"><span data-stu-id="88f18-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="88f18-164">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88f18-164">Click Save.</span></span>
    * <span data-ttu-id="88f18-165">Controleer of er geen fouten zijn gevonden voor de gemaakte formule.</span><span class="sxs-lookup"><span data-stu-id="88f18-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="88f18-166">Zie het tabblad FOUTEN onder het bedieningselement voor de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="88f18-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="88f18-167">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88f18-167">Close the page.</span></span>
27. <span data-ttu-id="88f18-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="88f18-168">Click OK.</span></span>
    * <span data-ttu-id="88f18-169">Voeg het berekende veld toe aan deze gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="88f18-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="88f18-170">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-170">Click Add.</span></span>
    * <span data-ttu-id="88f18-171">Klik op Toevoegen om een nieuw berekend veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="88f18-172">Typ "$Amount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="88f18-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="88f18-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="88f18-173">$Amount</span></span>  
30. <span data-ttu-id="88f18-174">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="88f18-174">Click Edit formula.</span></span>
31. <span data-ttu-id="88f18-175">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="88f18-176">Selecteer "Transactions\Debit(AmountCurDebit)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="88f18-177">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-177">Click Add data source.</span></span>
34. <span data-ttu-id="88f18-178">Typ in het veld Formule: 'Transactions.AmountCurDebit - '. (Let op de spatie tussen minus-teken en enkel aanhalingsteken.)</span><span class="sxs-lookup"><span data-stu-id="88f18-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="88f18-179">Typ [ - ] aan het einde van de formule.</span><span class="sxs-lookup"><span data-stu-id="88f18-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="88f18-180">Selecteer "Transactions\Credit(AmountCurCredit)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="88f18-181">Klik op Gegevensbron toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-181">Click Add data source.</span></span>
37. <span data-ttu-id="88f18-182">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88f18-182">Click Save.</span></span>
38. <span data-ttu-id="88f18-183">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88f18-183">Close the page.</span></span>
39. <span data-ttu-id="88f18-184">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="88f18-184">Click OK.</span></span>
    * <span data-ttu-id="88f18-185">Hiermee wordt het berekende veld $Amount toegevoegd aan de geselecteerde gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="88f18-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="88f18-186">Selecteer 'Transactions\$Amount' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="88f18-187">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="88f18-188">Zoek in de structuur 'Transactions\$Amount' en vouw dit uit of samen.</span><span class="sxs-lookup"><span data-stu-id="88f18-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="88f18-189">Vouw in de structuur 'Transactions' uit of samen.</span><span class="sxs-lookup"><span data-stu-id="88f18-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="88f18-190">Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.</span><span class="sxs-lookup"><span data-stu-id="88f18-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="88f18-191">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-191">Click Add root.</span></span>
    * <span data-ttu-id="88f18-192">Voer deze gegevensbron in om toegang te krijgen tot de bankrekeninggegevens van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="88f18-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="88f18-193">Typ "BankAccount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="88f18-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="88f18-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="88f18-194">BankAccount</span></span>  
47. <span data-ttu-id="88f18-195">Typ "Bankrekening" in het veld Label.</span><span class="sxs-lookup"><span data-stu-id="88f18-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="88f18-196">Bankrekening</span><span class="sxs-lookup"><span data-stu-id="88f18-196">Bank Account</span></span>  
48. <span data-ttu-id="88f18-197">Typ "Bankrekening" in het veld Help.</span><span class="sxs-lookup"><span data-stu-id="88f18-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="88f18-198">Bankrekening</span><span class="sxs-lookup"><span data-stu-id="88f18-198">Bank Account</span></span>  
49. <span data-ttu-id="88f18-199">Selecteer Ja in het veld Vragen om query.</span><span class="sxs-lookup"><span data-stu-id="88f18-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="88f18-200">Selecteer Ja.</span><span class="sxs-lookup"><span data-stu-id="88f18-200">Select Yes.</span></span>  
50. <span data-ttu-id="88f18-201">Typ "BankAccountTable" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="88f18-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="88f18-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="88f18-202">BankAccountTable</span></span>  
51. <span data-ttu-id="88f18-203">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="88f18-203">Click OK.</span></span>
    * <span data-ttu-id="88f18-204">Selecteer de tabel BankAccountTable als gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="88f18-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="88f18-205">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-205">Click Add root.</span></span>
    * <span data-ttu-id="88f18-206">Voer deze gegevensbron in om toegang te krijgen tot de vereisten van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="88f18-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="88f18-207">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="88f18-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="88f18-208">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="88f18-208">Company</span></span>  
54. <span data-ttu-id="88f18-209">Typ een waarde in het veld Label.</span><span class="sxs-lookup"><span data-stu-id="88f18-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="88f18-210">Bedrijfsgegevens</span><span class="sxs-lookup"><span data-stu-id="88f18-210">Company information</span></span>  
55. <span data-ttu-id="88f18-211">Typ "Bedrijfsinformatie" in het veld Help.</span><span class="sxs-lookup"><span data-stu-id="88f18-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="88f18-212">Bedrijfsgegevens</span><span class="sxs-lookup"><span data-stu-id="88f18-212">Company information</span></span>  
56. <span data-ttu-id="88f18-213">Selecteer Ja in het veld Vragen om query.</span><span class="sxs-lookup"><span data-stu-id="88f18-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="88f18-214">Selecteer Ja.</span><span class="sxs-lookup"><span data-stu-id="88f18-214">Select Yes.</span></span>  
57. <span data-ttu-id="88f18-215">Typ "CompanyInfo" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="88f18-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="88f18-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="88f18-216">CompanyInfo</span></span>  
58. <span data-ttu-id="88f18-217">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="88f18-217">Click OK.</span></span>
    * <span data-ttu-id="88f18-218">Selecteer de tabel CompanyInfo als gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="88f18-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="88f18-219">Selecteer "Functions\Calculated field" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="88f18-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="88f18-220">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-220">Click Add root.</span></span>
    * <span data-ttu-id="88f18-221">Voeg een berekend veld in als nieuwe gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="88f18-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="88f18-222">Typ "ProcessingDateTime" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="88f18-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="88f18-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="88f18-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="88f18-224">Typ Verwerkingsdatum en -tijd in het veld Label.</span><span class="sxs-lookup"><span data-stu-id="88f18-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="88f18-225">Verwerkingsdatum en -tijd</span><span class="sxs-lookup"><span data-stu-id="88f18-225">Processing date & time</span></span>  
63. <span data-ttu-id="88f18-226">Klik op Formule bewerken.</span><span class="sxs-lookup"><span data-stu-id="88f18-226">Click Edit formula.</span></span>
64. <span data-ttu-id="88f18-227">Selecteer in de structuur 'Date/time\SESSIONNOW'.</span><span class="sxs-lookup"><span data-stu-id="88f18-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="88f18-228">Klik op Functie toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88f18-228">Click Add function.</span></span>
66. <span data-ttu-id="88f18-229">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88f18-229">Click Save.</span></span>
67. <span data-ttu-id="88f18-230">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88f18-230">Close the page.</span></span>
68. <span data-ttu-id="88f18-231">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="88f18-231">Click OK.</span></span>
    * <span data-ttu-id="88f18-232">Voeg het berekende veld ProcessingDateTime toe als gegevensbron voor het huidige gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="88f18-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="88f18-233">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88f18-233">Click Save.</span></span>
70. <span data-ttu-id="88f18-234">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88f18-234">Close the page.</span></span>
71. <span data-ttu-id="88f18-235">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88f18-235">Close the page.</span></span>
72. <span data-ttu-id="88f18-236">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88f18-236">Close the page.</span></span>


