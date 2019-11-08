---
title: Er Wjis gegevensmodel toe aan geselecteerde gegevensbronnen
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan toewijzen aan geselecteerde Microsoft Dynamics 365 Finance-gegevensbronnen.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44f6ac3263f115e76d054e68c99d58dc11e6f1a0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182227"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="6964e-103">Er Wjis gegevensmodel toe aan geselecteerde gegevensbronnen</span><span class="sxs-lookup"><span data-stu-id="6964e-103">ER Map data model to selected data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6964e-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan toewijzen aan geselecteerde gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="6964e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="6964e-105">Deze modeltoewijzing wordt later gebruikt als gegevensbron in een indelingsconfiguratie die wordt gebruikt om elektronische betalingadocumenten te beheren.</span><span class="sxs-lookup"><span data-stu-id="6964e-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="6964e-106">In dit voorbeeld wijst u een gegevensmodel voor voorbeeldbedrijf Litware, Inc. aan gegevensbronnen toe.</span><span class="sxs-lookup"><span data-stu-id="6964e-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="6964e-107">U kunt deze stappen pas uitvoeren nadat u de stappen in de procedure "Gegevensbronnen voor modeltoewijzing selecteren" hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="6964e-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="6964e-108">ER-configuratiestructuur openen</span><span class="sxs-lookup"><span data-stu-id="6964e-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="6964e-109">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="6964e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6964e-110">Klik op Configuraties.</span><span class="sxs-lookup"><span data-stu-id="6964e-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="6964e-111">Gemaakte modeltoewijzing selecteren</span><span class="sxs-lookup"><span data-stu-id="6964e-111">Select created model mapping</span></span>
1. <span data-ttu-id="6964e-112">Selecteer "Payments (simplified model)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="6964e-113">Zorg ervoor dat de modelconfiguratie "Betalingen (vereenvoudigd model)" vooraf is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6964e-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="6964e-114">Ga anders eerst verder met de taakbegeleiding 'Een nieuwe configuratie maken met het gegevensmodel van het geselecteerde domein' voordat u de rest van deze procedure uitvoert.</span><span class="sxs-lookup"><span data-stu-id="6964e-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="6964e-115">Klik op Modelontwerper.</span><span class="sxs-lookup"><span data-stu-id="6964e-115">Click Model designer.</span></span>
3. <span data-ttu-id="6964e-116">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="6964e-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="6964e-117">Selecteer de record "CT-toewijzing".</span><span class="sxs-lookup"><span data-stu-id="6964e-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="6964e-118">CT-toewijzing</span><span class="sxs-lookup"><span data-stu-id="6964e-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="6964e-119">Gemaakte gegevensbronnen aan gegevensmodelelementen binden</span><span class="sxs-lookup"><span data-stu-id="6964e-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="6964e-120">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6964e-120">Click Designer.</span></span>
2. <span data-ttu-id="6964e-121">Selecteer 'Processing date & time(ProcessingDateTime)' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="6964e-122">Selecteer "Processing date(ProcessingDateTime)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="6964e-123">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-123">Click Bind.</span></span>
5. <span data-ttu-id="6964e-124">Selecteer "Payment message identification(MessageIdentification)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="6964e-125">Vouw "Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="6964e-126">Selecteer "Transactions\Journal batch number(JournalNum)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="6964e-127">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-127">Click Bind.</span></span>
9. <span data-ttu-id="6964e-128">Selecteer "Payments" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="6964e-129">Selecteer "Transactions" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="6964e-130">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-130">Click Bind.</span></span>
12. <span data-ttu-id="6964e-131">Vouw "Payments= Transactions" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="6964e-132">Vouw "Payments= Transactions\Creditor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="6964e-133">Vouw "Payments= Transactions\Creditor\Account" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="6964e-134">Vouw "Payments= Transactions\Creditor\Account\Currency code(Currency)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="6964e-135">Vouw "Transactions\vendBankAccountInTransactionCompany()" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="6964e-136">Selecteer "Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="6964e-137">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-137">Click Bind.</span></span>
19. <span data-ttu-id="6964e-138">Selecteer "Payments= Transactions\Creditor\Account\IBAN code(IBAN)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="6964e-139">Selecteer "Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="6964e-140">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-140">Click Bind.</span></span>
22. <span data-ttu-id="6964e-141">Selecteer "Payments= Transactions\Creditor\Account\Number" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="6964e-142">Selecteer "Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="6964e-143">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-143">Click Bind.</span></span>
25. <span data-ttu-id="6964e-144">Vouw "Payments= Transactions\Creditor\Agent" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="6964e-145">Selecteer "Payments= Transactions\Creditor\Agent\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="6964e-146">Selecteer "Transactions\vendBankAccountInTransactionCompany()\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="6964e-147">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-147">Click Bind.</span></span>
29. <span data-ttu-id="6964e-148">Selecteer "Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="6964e-149">Selecteer "Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="6964e-150">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-150">Click Bind.</span></span>
32. <span data-ttu-id="6964e-151">Selecteer "Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="6964e-152">Selecteer "Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="6964e-153">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-153">Click Bind.</span></span>
35. <span data-ttu-id="6964e-154">Selecteer "Payments= Transactions\Creditor\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="6964e-155">Vouw "Transactions\findVendTable()" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="6964e-156">Selecteer 'Transactions\findVendTable()\name()' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="6964e-157">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-157">Click Bind.</span></span>
39. <span data-ttu-id="6964e-158">Selecteer "Payments= Transactions\Currency code(Currency)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="6964e-159">Vouw "Transactions\>Relations" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="6964e-160">Vouw "Transactions\>Relations\Currency table(Currency)" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="6964e-161">Selecteer "Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="6964e-162">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-162">Click Bind.</span></span>
44. <span data-ttu-id="6964e-163">Vouw "Payments= Transactions\Debtor" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="6964e-164">Vouw "Payments= Transactions\Debtor\Account" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="6964e-165">Selecteer "Payments= Transactions\Debtor\Account\Currency code(Currency)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="6964e-166">Selecteer "Bank Account(BankAccount)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="6964e-167">Vouw "Bank Account(BankAccount)" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="6964e-168">Selecteer "Bank Account(BankAccount)\Currency(CurrencyCode)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="6964e-169">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-169">Click Bind.</span></span>
51. <span data-ttu-id="6964e-170">Selecteer "Bank Account(BankAccount)\IBAN" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="6964e-171">Selecteer "Payments= Transactions\Debtor\Account\IBAN code(IBAN)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="6964e-172">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-172">Click Bind.</span></span>
54. <span data-ttu-id="6964e-173">Selecteer "Payments= Transactions\Debtor\Account\Number" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="6964e-174">Selecteer "Bank Account(BankAccount)\Bank account number(AccountNum)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="6964e-175">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-175">Click Bind.</span></span>
57. <span data-ttu-id="6964e-176">Vouw "Payments= Transactions\Debtor\Agent" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="6964e-177">Selecteer "Payments= Transactions\Debtor\Agent\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="6964e-178">Selecteer "Bank Account(BankAccount)\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="6964e-179">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-179">Click Bind.</span></span>
61. <span data-ttu-id="6964e-180">Selecteer "Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="6964e-181">Selecteer "Bank Account(BankAccount)\Routing number(RegistrationNum)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="6964e-182">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-182">Click Bind.</span></span>
64. <span data-ttu-id="6964e-183">Selecteer "Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="6964e-184">Selecteer "Bank Account(BankAccount)\SWIFT code(SWIFTNo)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="6964e-185">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-185">Click Bind.</span></span>
67. <span data-ttu-id="6964e-186">Selecteer "Payments= Transactions\Debtor\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="6964e-187">Selecteer "Company information(Company)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="6964e-188">Vouw "Company information(Company)" uit in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="6964e-189">Selecteer "Company information(Company)\Name" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="6964e-190">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-190">Click Bind.</span></span>
72. <span data-ttu-id="6964e-191">Selecteer "Payments= Transactions\Description" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="6964e-192">Selecteer "Transactions\Description(Txt)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="6964e-193">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-193">Click Bind.</span></span>
75. <span data-ttu-id="6964e-194">Selecteer "Payments= Transactions\End to end identification code(End2EndID)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="6964e-195">Selecteer "Transactions\$EndToEndID" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="6964e-196">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-196">Click Bind.</span></span>
78. <span data-ttu-id="6964e-197">Selecteer "Payments= Transactions\Instructed amount(InstructedAmount)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="6964e-198">Selecteer 'Transactions\$Amount' in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="6964e-199">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-199">Click Bind.</span></span>
81. <span data-ttu-id="6964e-200">Selecteer "Payments= Transactions\Transaction date(TransactionDate)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="6964e-201">Selecteer "Transactions\Date(TransDate)" in de structuur.</span><span class="sxs-lookup"><span data-stu-id="6964e-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="6964e-202">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="6964e-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="6964e-203">Gemaakte toewijzing valideren</span><span class="sxs-lookup"><span data-stu-id="6964e-203">Validate created mapping</span></span>
1. <span data-ttu-id="6964e-204">Klik op Valideren.</span><span class="sxs-lookup"><span data-stu-id="6964e-204">Click Validate.</span></span>
    * <span data-ttu-id="6964e-205">De nieuwe toewijzing valideren om te controleren of alle bindingen in orde zijn.</span><span class="sxs-lookup"><span data-stu-id="6964e-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="6964e-206">Klik op de pijl om de sectie Foutenlijst uit te vouwen of samen te vouwen.</span><span class="sxs-lookup"><span data-stu-id="6964e-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="6964e-207">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6964e-207">Click Save.</span></span>
4. <span data-ttu-id="6964e-208">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6964e-208">Close the page.</span></span>
5. <span data-ttu-id="6964e-209">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6964e-209">Close the page.</span></span>
6. <span data-ttu-id="6964e-210">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6964e-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="6964e-211">De status van de huidige versie van de modelconfiguratie wijzigen</span><span class="sxs-lookup"><span data-stu-id="6964e-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="6964e-212">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6964e-212">Click Change status.</span></span>
    * <span data-ttu-id="6964e-213">Wijzig de status van de ontworpen modelconfiguratie van Concept in Voltooid, om deze beschikbaar te maken voor het het ontwerp van betalingsindelingen.</span><span class="sxs-lookup"><span data-stu-id="6964e-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="6964e-214">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="6964e-214">Click Complete.</span></span>
    * <span data-ttu-id="6964e-215">Selecteer Voltooien.</span><span class="sxs-lookup"><span data-stu-id="6964e-215">Select Complete.</span></span>  
3. <span data-ttu-id="6964e-216">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="6964e-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6964e-217">Bijvoorbeeld: 'versie 1'.</span><span class="sxs-lookup"><span data-stu-id="6964e-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="6964e-218">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6964e-218">Click OK.</span></span>
5. <span data-ttu-id="6964e-219">Selecteer de ingevulde versie van de huidige configuratie.</span><span class="sxs-lookup"><span data-stu-id="6964e-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="6964e-220">Merk op dat de gemaakte configuratie wordt opgeslagen als voltooide versie 1.</span><span class="sxs-lookup"><span data-stu-id="6964e-220">Note that the created configuration is saved as completed version 1.</span></span>  
