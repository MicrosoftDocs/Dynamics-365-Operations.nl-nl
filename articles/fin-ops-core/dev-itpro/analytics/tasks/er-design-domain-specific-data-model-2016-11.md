---
title: ER Ontwerp domeinspecifiek gegevensmodel
description: In dit onderwerp wordt beschreven hoe u een nieuwe ER-configuratie (Electronic Reporting) maakt die een gegevensmodel voor elektronische betalingsdocumenten bevat.
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1eb2c6e5b5f186fb6db7c32a9982807274e5ea1b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092686"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="98a12-103">ER Ontwerp domeinspecifiek gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="98a12-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98a12-104">In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een gegevensmodel voor elektronische betalingsdocumenten bevat.</span><span class="sxs-lookup"><span data-stu-id="98a12-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="98a12-105">Dit gegevensmodel wordt later gebruikt als gegevensbron, wanneer u de indeling van de betalingsdocumenten maakt.</span><span class="sxs-lookup"><span data-stu-id="98a12-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="98a12-106">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="98a12-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="98a12-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="98a12-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="98a12-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="98a12-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="98a12-109">Selecteer de configuratieprovider voor voorbeeldbedrijf, 'Litware, inc.'</span><span class="sxs-lookup"><span data-stu-id="98a12-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="98a12-110">Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="98a12-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="98a12-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="98a12-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="98a12-112">U maakt een configuratie die een gegevensmodel voor elektronische betalingdocumenten bevat.</span><span class="sxs-lookup"><span data-stu-id="98a12-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="98a12-113">Dit gegevensmodel wordt later gebruikt als gegevensbron wanneer u de indeling gebruikt voor de betalingdocumenten.</span><span class="sxs-lookup"><span data-stu-id="98a12-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="98a12-114">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="98a12-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="98a12-115">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="98a12-116">Typ "Payments (simplified model)" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="98a12-117">Typ "Configuratie van betalingsmodel" in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="98a12-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="98a12-118">De actieve configuratieprovider wordt hier automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="98a12-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="98a12-119">Deze provider kan deze configuratie onderhouden.</span><span class="sxs-lookup"><span data-stu-id="98a12-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="98a12-120">Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.</span><span class="sxs-lookup"><span data-stu-id="98a12-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="98a12-121">Klik op de knop 'Configuratie maken' om de taak van het maken van een configuratie te voltooien</span><span class="sxs-lookup"><span data-stu-id="98a12-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="98a12-122">Een gegevensmodel maken</span><span class="sxs-lookup"><span data-stu-id="98a12-122">Create a data model</span></span>
<span data-ttu-id="98a12-123">U maakt een nieuw gegevensmodel voor de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="98a12-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="98a12-124">Deze configuratieversie heeft de status Concept.</span><span class="sxs-lookup"><span data-stu-id="98a12-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="98a12-125">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="98a12-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="98a12-126">De structuur van een partij die deelneemt aan een betalingsproces definiëren</span><span class="sxs-lookup"><span data-stu-id="98a12-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="98a12-127">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="98a12-128">Typ in het veld Naam de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="98a12-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="98a12-129">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-129">Click Add.</span></span>
4. <span data-ttu-id="98a12-130">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="98a12-131">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="98a12-132">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="98a12-133">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-133">Click Add.</span></span>
8. <span data-ttu-id="98a12-134">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="98a12-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="98a12-135">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="98a12-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="98a12-136">De bankstructuur voor dit model definiëren</span><span class="sxs-lookup"><span data-stu-id="98a12-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="98a12-137">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="98a12-138">Typ "Agent" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="98a12-139">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="98a12-140">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-140">Click Add.</span></span>
5. <span data-ttu-id="98a12-141">Typ in het veld Omschrijving: "Financiële instelling (bijvoorbeeld een bank) waar de partij (debiteur/crediteur) een rekening heeft".</span><span class="sxs-lookup"><span data-stu-id="98a12-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="98a12-142">Financiële instelling (bijvoorbeeld een bank) waar de partij (debiteur/credieteur) een rekening heeft.</span><span class="sxs-lookup"><span data-stu-id="98a12-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="98a12-143">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="98a12-144">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="98a12-145">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="98a12-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-146">Click Add.</span></span>
10. <span data-ttu-id="98a12-147">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="98a12-148">Typ "SWIFT" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="98a12-149">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-149">Click Add.</span></span>
13. <span data-ttu-id="98a12-150">Typ in het veld Beschrijving de tekst "De ID-code van de bank".</span><span class="sxs-lookup"><span data-stu-id="98a12-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="98a12-151">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="98a12-152">Typ "RoutingNumber" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="98a12-153">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-153">Click Add.</span></span>
17. <span data-ttu-id="98a12-154">Typ in het veld Beschrijving de tekst "Routenummer".</span><span class="sxs-lookup"><span data-stu-id="98a12-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="98a12-155">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="98a12-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="98a12-156">De bankrekeningstructuur voor dit model definiëren</span><span class="sxs-lookup"><span data-stu-id="98a12-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="98a12-157">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="98a12-158">Typ "Account" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="98a12-159">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="98a12-160">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-160">Click Add.</span></span>
5. <span data-ttu-id="98a12-161">Typ in het veld Beschrijving: "De ID van een rekening van een partij bij een financiële instelling (bijvoorbeeld een bank)".</span><span class="sxs-lookup"><span data-stu-id="98a12-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="98a12-162">De ID van een rekening van een partij bij een financiële instelling (bijvoorbeeld een bank).</span><span class="sxs-lookup"><span data-stu-id="98a12-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="98a12-163">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="98a12-164">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="98a12-165">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="98a12-166">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-166">Click Add.</span></span>
10. <span data-ttu-id="98a12-167">Typ in het veld Beschrijving de tekst "Valutacode".</span><span class="sxs-lookup"><span data-stu-id="98a12-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="98a12-168">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="98a12-169">Typ "Number" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="98a12-170">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-170">Click Add.</span></span>
14. <span data-ttu-id="98a12-171">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="98a12-172">Typ "IBAN" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="98a12-173">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-173">Click Add.</span></span>
17. <span data-ttu-id="98a12-174">Typ in het veld Beschrijving de tekst "Internationaal bankrekeningnummer".</span><span class="sxs-lookup"><span data-stu-id="98a12-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="98a12-175">De structuur definiëren van het betalingsbericht voor het betalingstype kredietoverdracht</span><span class="sxs-lookup"><span data-stu-id="98a12-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="98a12-176">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="98a12-177">Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".</span><span class="sxs-lookup"><span data-stu-id="98a12-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="98a12-178">Typ "CustomerCreditTransferInitiation" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="98a12-179">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-179">Click Add.</span></span>
5. <span data-ttu-id="98a12-180">Typ in het veld Zoeken de tekst "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="98a12-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="98a12-181">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="98a12-181">Click Find previous.</span></span>
7. <span data-ttu-id="98a12-182">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="98a12-183">Typ "MessageIdentification" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="98a12-184">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-184">Click Add.</span></span>
10. <span data-ttu-id="98a12-185">Typ in het veld Omschrijving: "De punt-naar-punt-verwijzing, zoals toegewezen door de instruerende partij en verzonden naar de volgende partij in de keten, zodat het bericht ondubbelzinnig kan worden geïdentificeerd".</span><span class="sxs-lookup"><span data-stu-id="98a12-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="98a12-186">De verwijzing van punt naar punt die is toegewezen door de instruerende partij (en verzonden naar de volgende partij) om een bericht te identificeren.</span><span class="sxs-lookup"><span data-stu-id="98a12-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="98a12-187">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="98a12-188">Typ "ProcessingDateTime" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="98a12-189">Selecteer "DateTime" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="98a12-190">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-190">Click Add.</span></span>
15. <span data-ttu-id="98a12-191">Typ in het veld Beschrijving: "De datum en tijd waarop het betalingsbericht is gemaakt".</span><span class="sxs-lookup"><span data-stu-id="98a12-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="98a12-192">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="98a12-193">Definieer de betalingstransactiestructuur voor dit model.</span><span class="sxs-lookup"><span data-stu-id="98a12-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="98a12-194">Typ "Payments" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="98a12-195">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="98a12-196">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-196">Click Add.</span></span>
20. <span data-ttu-id="98a12-197">Typ "Betalingsregels van het huidige bericht" in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="98a12-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="98a12-198">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="98a12-199">Typ "Creditor" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="98a12-200">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="98a12-201">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-201">Click Add.</span></span>
25. <span data-ttu-id="98a12-202">Typ in het veld Beschrijving: "Partij aan wie een geldbedrag verschuldigd is".</span><span class="sxs-lookup"><span data-stu-id="98a12-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="98a12-203">Klik op Artikelverwijzing omschakelen.</span><span class="sxs-lookup"><span data-stu-id="98a12-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="98a12-204">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="98a12-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="98a12-205">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="98a12-205">Click Find next.</span></span>
29. <span data-ttu-id="98a12-206">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="98a12-206">Click OK.</span></span>
30. <span data-ttu-id="98a12-207">Typ in het veld Zoeken de tekst "Betalingen".</span><span class="sxs-lookup"><span data-stu-id="98a12-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="98a12-208">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="98a12-208">Click Find next.</span></span>
32. <span data-ttu-id="98a12-209">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="98a12-210">Typ "Debtor" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="98a12-211">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-211">Click Add.</span></span>
35. <span data-ttu-id="98a12-212">Typ in het veld Beschrijving: "Partij die een geldbedrag verschuldigd is aan de (uiteindelijke) crediteur".</span><span class="sxs-lookup"><span data-stu-id="98a12-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="98a12-213">Klik op Artikelverwijzing omschakelen.</span><span class="sxs-lookup"><span data-stu-id="98a12-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="98a12-214">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="98a12-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="98a12-215">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="98a12-215">Click Find next.</span></span>
39. <span data-ttu-id="98a12-216">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="98a12-216">Click OK.</span></span>
40. <span data-ttu-id="98a12-217">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="98a12-217">Click Find next.</span></span>
41. <span data-ttu-id="98a12-218">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="98a12-219">Typ "Description" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="98a12-220">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="98a12-221">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-221">Click Add.</span></span>
45. <span data-ttu-id="98a12-222">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="98a12-223">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="98a12-224">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-224">Click Add.</span></span>
48. <span data-ttu-id="98a12-225">Typ in het veld Beschrijving de tekst "Valutacode".</span><span class="sxs-lookup"><span data-stu-id="98a12-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="98a12-226">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="98a12-227">Typ "TransactionDate" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="98a12-228">Selecteer "Date" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="98a12-229">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-229">Click Add.</span></span>
53. <span data-ttu-id="98a12-230">Typ in het veld Beschrijving de tekst "Transactiedatum".</span><span class="sxs-lookup"><span data-stu-id="98a12-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="98a12-231">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="98a12-232">Typ "InstructedAmount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="98a12-233">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="98a12-234">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-234">Click Add.</span></span>
58. <span data-ttu-id="98a12-235">Typ in het veld Beschrijving: "Het geldbedrag dat moet worden verplaatst tussen de debiteur en de crediteur, vóór aftrek van toeslagen".</span><span class="sxs-lookup"><span data-stu-id="98a12-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="98a12-236">Het bedrag moet worden uitgedrukt in de valuta die door de initiërende partij is aangevraagd." in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="98a12-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="98a12-237">Het geldbedrag dat moet worden verplaatst tussen de debiteur en de crediteur, vóór aftrek van toeslagen.</span><span class="sxs-lookup"><span data-stu-id="98a12-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="98a12-238">Het bedrag moet worden uitgedrukt in de valuta die door de initiërende partij is aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="98a12-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="98a12-239">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="98a12-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="98a12-240">Typ "End2EndID" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="98a12-241">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="98a12-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="98a12-242">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="98a12-242">Click Add.</span></span>
63. <span data-ttu-id="98a12-243">Typ in het veld Beschrijving: "De unieke identificatie die is toegewezen door de initiërende partij".</span><span class="sxs-lookup"><span data-stu-id="98a12-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="98a12-244">Deze identificatie wordt ongewijzigd doorgegeven door de volledige keten heen, van begin tot einde." in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="98a12-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="98a12-245">Typ "PaymentModel" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="98a12-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="98a12-246">De naam PaymentModel is afgestemd op vooraf gedefinieerde interfaces van betalingsformulieren.</span><span class="sxs-lookup"><span data-stu-id="98a12-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="98a12-247">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="98a12-247">Click Save.</span></span>
66. <span data-ttu-id="98a12-248">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="98a12-248">Close the page.</span></span>

