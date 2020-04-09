---
title: ER Ontwerp domeinspecifiek gegevensmodel
description: In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een gegevensmodel voor elektronische betalingsdocumenten bevat.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2b93f74a121de4c23eb5dddfb94c6596b78544d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142657"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="6aa21-103">ER Ontwerp domeinspecifiek gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="6aa21-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6aa21-104">In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een gegevensmodel voor elektronische betalingsdocumenten bevat.</span><span class="sxs-lookup"><span data-stu-id="6aa21-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="6aa21-105">Dit gegevensmodel wordt later gebruikt als gegevensbron, wanneer u de indeling van de betalingsdocumenten maakt.</span><span class="sxs-lookup"><span data-stu-id="6aa21-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="6aa21-106">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="6aa21-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="6aa21-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="6aa21-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="6aa21-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="6aa21-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="6aa21-109">Selecteer de configuratieprovider voor voorbeeldbedrijf, 'Litware, inc.'</span><span class="sxs-lookup"><span data-stu-id="6aa21-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="6aa21-110">Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6aa21-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="6aa21-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="6aa21-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="6aa21-112">U maakt een configuratie die een gegevensmodel voor elektronische betalingdocumenten bevat.</span><span class="sxs-lookup"><span data-stu-id="6aa21-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="6aa21-113">Dit gegevensmodel wordt later gebruikt als gegevensbron wanneer u de indeling gebruikt voor de betalingdocumenten.</span><span class="sxs-lookup"><span data-stu-id="6aa21-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="6aa21-114">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="6aa21-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="6aa21-115">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6aa21-116">Typ "Payments (simplified model)" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="6aa21-117">Typ "Configuratie van betalingsmodel" in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="6aa21-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="6aa21-118">De actieve configuratieprovider wordt hier automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="6aa21-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="6aa21-119">Deze provider kan deze configuratie onderhouden.</span><span class="sxs-lookup"><span data-stu-id="6aa21-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="6aa21-120">Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.</span><span class="sxs-lookup"><span data-stu-id="6aa21-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="6aa21-121">Klik op de knop 'Configuratie maken' om de taak van het maken van een configuratie te voltooien</span><span class="sxs-lookup"><span data-stu-id="6aa21-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="6aa21-122">Een gegevensmodel maken</span><span class="sxs-lookup"><span data-stu-id="6aa21-122">Create a data model</span></span>
<span data-ttu-id="6aa21-123">U maakt een nieuw gegevensmodel voor de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="6aa21-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="6aa21-124">Deze configuratieversie heeft de status Concept.</span><span class="sxs-lookup"><span data-stu-id="6aa21-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="6aa21-125">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="6aa21-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="6aa21-126">De structuur van een partij die deelneemt aan een betalingsproces definiëren</span><span class="sxs-lookup"><span data-stu-id="6aa21-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="6aa21-127">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="6aa21-128">Typ in het veld Naam de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="6aa21-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="6aa21-129">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-129">Click Add.</span></span>
4. <span data-ttu-id="6aa21-130">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="6aa21-131">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="6aa21-132">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="6aa21-133">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-133">Click Add.</span></span>
8. <span data-ttu-id="6aa21-134">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="6aa21-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="6aa21-135">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="6aa21-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="6aa21-136">De bankstructuur voor dit model definiëren</span><span class="sxs-lookup"><span data-stu-id="6aa21-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="6aa21-137">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="6aa21-138">Typ "Agent" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="6aa21-139">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="6aa21-140">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-140">Click Add.</span></span>
5. <span data-ttu-id="6aa21-141">Typ in het veld Omschrijving: "Financiële instelling (bijvoorbeeld een bank) waar de partij (debiteur/crediteur) een rekening heeft".</span><span class="sxs-lookup"><span data-stu-id="6aa21-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="6aa21-142">Financiële instelling (bijvoorbeeld een bank) waar de partij (debiteur/credieteur) een rekening heeft.</span><span class="sxs-lookup"><span data-stu-id="6aa21-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="6aa21-143">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="6aa21-144">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="6aa21-145">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="6aa21-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-146">Click Add.</span></span>
10. <span data-ttu-id="6aa21-147">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="6aa21-148">Typ "SWIFT" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="6aa21-149">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-149">Click Add.</span></span>
13. <span data-ttu-id="6aa21-150">Typ in het veld Beschrijving de tekst "De ID-code van de bank".</span><span class="sxs-lookup"><span data-stu-id="6aa21-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="6aa21-151">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="6aa21-152">Typ "RoutingNumber" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="6aa21-153">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-153">Click Add.</span></span>
17. <span data-ttu-id="6aa21-154">Typ in het veld Beschrijving de tekst "Routenummer".</span><span class="sxs-lookup"><span data-stu-id="6aa21-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="6aa21-155">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="6aa21-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="6aa21-156">De bankrekeningstructuur voor dit model definiëren</span><span class="sxs-lookup"><span data-stu-id="6aa21-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="6aa21-157">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="6aa21-158">Typ "Account" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="6aa21-159">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="6aa21-160">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-160">Click Add.</span></span>
5. <span data-ttu-id="6aa21-161">Typ in het veld Beschrijving: "De ID van een rekening van een partij bij een financiële instelling (bijvoorbeeld een bank)".</span><span class="sxs-lookup"><span data-stu-id="6aa21-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="6aa21-162">De ID van een rekening van een partij bij een financiële instelling (bijvoorbeeld een bank).</span><span class="sxs-lookup"><span data-stu-id="6aa21-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="6aa21-163">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="6aa21-164">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="6aa21-165">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="6aa21-166">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-166">Click Add.</span></span>
10. <span data-ttu-id="6aa21-167">Typ in het veld Beschrijving de tekst "Valutacode".</span><span class="sxs-lookup"><span data-stu-id="6aa21-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="6aa21-168">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="6aa21-169">Typ "Number" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="6aa21-170">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-170">Click Add.</span></span>
14. <span data-ttu-id="6aa21-171">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="6aa21-172">Typ "IBAN" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="6aa21-173">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-173">Click Add.</span></span>
17. <span data-ttu-id="6aa21-174">Typ in het veld Beschrijving de tekst "Internationaal bankrekeningnummer".</span><span class="sxs-lookup"><span data-stu-id="6aa21-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="6aa21-175">De structuur definiëren van het betalingsbericht voor het betalingstype kredietoverdracht</span><span class="sxs-lookup"><span data-stu-id="6aa21-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="6aa21-176">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="6aa21-177">Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".</span><span class="sxs-lookup"><span data-stu-id="6aa21-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="6aa21-178">Typ "CustomerCreditTransferInitiation" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="6aa21-179">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-179">Click Add.</span></span>
5. <span data-ttu-id="6aa21-180">Typ in het veld Zoeken de tekst "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="6aa21-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="6aa21-181">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="6aa21-181">Click Find previous.</span></span>
7. <span data-ttu-id="6aa21-182">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="6aa21-183">Typ "MessageIdentification" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="6aa21-184">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-184">Click Add.</span></span>
10. <span data-ttu-id="6aa21-185">Typ in het veld Omschrijving: "De punt-naar-punt-verwijzing, zoals toegewezen door de instruerende partij en verzonden naar de volgende partij in de keten, zodat het bericht ondubbelzinnig kan worden geïdentificeerd".</span><span class="sxs-lookup"><span data-stu-id="6aa21-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="6aa21-186">De verwijzing van punt naar punt die is toegewezen door de instruerende partij (en verzonden naar de volgende partij) om een bericht te identificeren.</span><span class="sxs-lookup"><span data-stu-id="6aa21-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="6aa21-187">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="6aa21-188">Typ "ProcessingDateTime" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="6aa21-189">Selecteer "DateTime" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="6aa21-190">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-190">Click Add.</span></span>
15. <span data-ttu-id="6aa21-191">Typ in het veld Beschrijving: "De datum en tijd waarop het betalingsbericht is gemaakt".</span><span class="sxs-lookup"><span data-stu-id="6aa21-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="6aa21-192">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="6aa21-193">Definieer de betalingstransactiestructuur voor dit model.</span><span class="sxs-lookup"><span data-stu-id="6aa21-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="6aa21-194">Typ "Payments" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="6aa21-195">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="6aa21-196">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-196">Click Add.</span></span>
20. <span data-ttu-id="6aa21-197">Typ "Betalingsregels van het huidige bericht" in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="6aa21-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="6aa21-198">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="6aa21-199">Typ "Creditor" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="6aa21-200">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="6aa21-201">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-201">Click Add.</span></span>
25. <span data-ttu-id="6aa21-202">Typ in het veld Beschrijving: "Partij aan wie een geldbedrag verschuldigd is".</span><span class="sxs-lookup"><span data-stu-id="6aa21-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="6aa21-203">Klik op Artikelverwijzing omschakelen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="6aa21-204">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="6aa21-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="6aa21-205">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="6aa21-205">Click Find next.</span></span>
29. <span data-ttu-id="6aa21-206">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6aa21-206">Click OK.</span></span>
30. <span data-ttu-id="6aa21-207">Typ in het veld Zoeken de tekst "Betalingen".</span><span class="sxs-lookup"><span data-stu-id="6aa21-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="6aa21-208">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="6aa21-208">Click Find next.</span></span>
32. <span data-ttu-id="6aa21-209">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="6aa21-210">Typ "Debtor" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="6aa21-211">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-211">Click Add.</span></span>
35. <span data-ttu-id="6aa21-212">Typ in het veld Beschrijving: "Partij die een geldbedrag verschuldigd is aan de (uiteindelijke) crediteur".</span><span class="sxs-lookup"><span data-stu-id="6aa21-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="6aa21-213">Klik op Artikelverwijzing omschakelen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="6aa21-214">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="6aa21-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="6aa21-215">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="6aa21-215">Click Find next.</span></span>
39. <span data-ttu-id="6aa21-216">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="6aa21-216">Click OK.</span></span>
40. <span data-ttu-id="6aa21-217">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="6aa21-217">Click Find next.</span></span>
41. <span data-ttu-id="6aa21-218">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="6aa21-219">Typ "Description" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="6aa21-220">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="6aa21-221">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-221">Click Add.</span></span>
45. <span data-ttu-id="6aa21-222">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="6aa21-223">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="6aa21-224">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-224">Click Add.</span></span>
48. <span data-ttu-id="6aa21-225">Typ in het veld Beschrijving de tekst "Valutacode".</span><span class="sxs-lookup"><span data-stu-id="6aa21-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="6aa21-226">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="6aa21-227">Typ "TransactionDate" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="6aa21-228">Selecteer "Date" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="6aa21-229">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-229">Click Add.</span></span>
53. <span data-ttu-id="6aa21-230">Typ in het veld Beschrijving de tekst "Transactiedatum".</span><span class="sxs-lookup"><span data-stu-id="6aa21-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="6aa21-231">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="6aa21-232">Typ "InstructedAmount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="6aa21-233">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="6aa21-234">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-234">Click Add.</span></span>
58. <span data-ttu-id="6aa21-235">Typ in het veld Beschrijving: "Het geldbedrag dat moet worden verplaatst tussen de debiteur en de crediteur, vóór aftrek van toeslagen".</span><span class="sxs-lookup"><span data-stu-id="6aa21-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="6aa21-236">Het bedrag moet worden uitgedrukt in de valuta die door de initiërende partij is aangevraagd." in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="6aa21-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="6aa21-237">Het geldbedrag dat moet worden verplaatst tussen de debiteur en de crediteur, vóór aftrek van toeslagen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="6aa21-238">Het bedrag moet worden uitgedrukt in de valuta die door de initiërende partij is aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="6aa21-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="6aa21-239">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="6aa21-240">Typ "End2EndID" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="6aa21-241">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="6aa21-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="6aa21-242">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6aa21-242">Click Add.</span></span>
63. <span data-ttu-id="6aa21-243">Typ in het veld Beschrijving: "De unieke identificatie die is toegewezen door de initiërende partij".</span><span class="sxs-lookup"><span data-stu-id="6aa21-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="6aa21-244">Deze identificatie wordt ongewijzigd doorgegeven door de volledige keten heen, van begin tot einde." in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="6aa21-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="6aa21-245">Typ "PaymentModel" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6aa21-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="6aa21-246">De naam PaymentModel is afgestemd op vooraf gedefinieerde interfaces van betalingsformulieren.</span><span class="sxs-lookup"><span data-stu-id="6aa21-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="6aa21-247">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="6aa21-247">Click Save.</span></span>
66. <span data-ttu-id="6aa21-248">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6aa21-248">Close the page.</span></span>

