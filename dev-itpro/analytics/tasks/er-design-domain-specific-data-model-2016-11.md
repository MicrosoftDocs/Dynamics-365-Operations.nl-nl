--- 
title: Een domeinspecifiek gegevensmodel voor elektronische aangifte ontwerpen (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een gegevensmodel voor elektronische betalingsdocumenten bevat.
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3349d4e910cf1a97eb099aaa7d1155732be3a21f
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a><span data-ttu-id="7026e-103">Een domeinspecifiek gegevensmodel voor elektronische aangifte ontwerpen (ER)</span><span class="sxs-lookup"><span data-stu-id="7026e-103">Design a domain-specific data model for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7026e-104">In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een gegevensmodel voor elektronische betalingsdocumenten bevat.</span><span class="sxs-lookup"><span data-stu-id="7026e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="7026e-105">Dit gegevensmodel wordt later gebruikt als gegevensbron, wanneer u de indeling van de betalingsdocumenten maakt.</span><span class="sxs-lookup"><span data-stu-id="7026e-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="7026e-106">In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="7026e-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="7026e-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="7026e-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="7026e-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="7026e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="7026e-109">Selecteer de configuratieprovider voor voorbeeldbedrijf, ’Litware, inc.’</span><span class="sxs-lookup"><span data-stu-id="7026e-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="7026e-110">Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.</span><span class="sxs-lookup"><span data-stu-id="7026e-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="7026e-111">Klik op Rapportconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="7026e-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="7026e-112">U maakt een configuratie die een gegevensmodel voor elektronische betalingdocumenten bevat.</span><span class="sxs-lookup"><span data-stu-id="7026e-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="7026e-113">Dit gegevensmodel wordt later gebruikt als gegevensbron wanneer u de indeling gebruikt voor de betalingdocumenten.</span><span class="sxs-lookup"><span data-stu-id="7026e-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="7026e-114">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="7026e-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="7026e-115">Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="7026e-116">Typ "Payments (simplified model)" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="7026e-117">Betalingen (vereenvoudigd model)</span><span class="sxs-lookup"><span data-stu-id="7026e-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="7026e-118">Typ "Configuratie van betalingsmodel" in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="7026e-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="7026e-119">Configuratie van betalingsmodel</span><span class="sxs-lookup"><span data-stu-id="7026e-119">Payment model configuration</span></span>  
    * <span data-ttu-id="7026e-120">De actieve configuratieprovider wordt hier automatisch ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="7026e-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="7026e-121">Deze provider kan deze configuratie onderhouden.</span><span class="sxs-lookup"><span data-stu-id="7026e-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="7026e-122">Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.</span><span class="sxs-lookup"><span data-stu-id="7026e-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="7026e-123">Klik op de knop "Configuratie maken" om de taak van het maken van een configuratie te voltooien</span><span class="sxs-lookup"><span data-stu-id="7026e-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="7026e-124">Een gegevensmodel maken</span><span class="sxs-lookup"><span data-stu-id="7026e-124">Create a data model</span></span>
    * <span data-ttu-id="7026e-125">U maakt een nieuw gegevensmodel voor de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="7026e-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="7026e-126">Deze configuratieversie heeft de status Concept.</span><span class="sxs-lookup"><span data-stu-id="7026e-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="7026e-127">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="7026e-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="7026e-128">De structuur van een partij die deelneemt aan een betalingsproces definiëren</span><span class="sxs-lookup"><span data-stu-id="7026e-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="7026e-129">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="7026e-130">Typ in het veld Naam de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="7026e-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="7026e-131">Partij</span><span class="sxs-lookup"><span data-stu-id="7026e-131">Party</span></span>  
3. <span data-ttu-id="7026e-132">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-132">Click Add.</span></span>
4. <span data-ttu-id="7026e-133">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="7026e-134">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="7026e-135">Naam</span><span class="sxs-lookup"><span data-stu-id="7026e-135">Name</span></span>  
6. <span data-ttu-id="7026e-136">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="7026e-137">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-137">Click Add.</span></span>
8. <span data-ttu-id="7026e-138">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="7026e-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="7026e-139">Partij</span><span class="sxs-lookup"><span data-stu-id="7026e-139">Party</span></span>  
9. <span data-ttu-id="7026e-140">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="7026e-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="7026e-141">De bankstructuur voor dit model definiëren</span><span class="sxs-lookup"><span data-stu-id="7026e-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="7026e-142">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="7026e-143">Typ "Agent" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="7026e-144">Medewerker</span><span class="sxs-lookup"><span data-stu-id="7026e-144">Agent</span></span>  
3. <span data-ttu-id="7026e-145">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="7026e-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-146">Click Add.</span></span>
5. <span data-ttu-id="7026e-147">Typ in het veld Omschrijving: "Financiële instelling (bijvoorbeeld een bank) waar de partij (debiteur/crediteur) een rekening heeft".</span><span class="sxs-lookup"><span data-stu-id="7026e-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="7026e-148">Financiële instelling (bijvoorbeeld een bank) waar de partij (debiteur/credieteur) een rekening heeft.</span><span class="sxs-lookup"><span data-stu-id="7026e-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="7026e-149">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="7026e-150">Typ "Name" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="7026e-151">Naam</span><span class="sxs-lookup"><span data-stu-id="7026e-151">Name</span></span>  
8. <span data-ttu-id="7026e-152">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="7026e-153">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-153">Click Add.</span></span>
10. <span data-ttu-id="7026e-154">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="7026e-155">Typ "SWIFT" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="7026e-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="7026e-156">SWIFT</span></span>  
12. <span data-ttu-id="7026e-157">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-157">Click Add.</span></span>
13. <span data-ttu-id="7026e-158">Typ in het veld Beschrijving de tekst "De ID-code van de bank".</span><span class="sxs-lookup"><span data-stu-id="7026e-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="7026e-159">De ID-code van de bank</span><span class="sxs-lookup"><span data-stu-id="7026e-159">Bank identification code</span></span>  
14. <span data-ttu-id="7026e-160">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="7026e-161">Typ "RoutingNumber" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="7026e-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="7026e-162">RoutingNumber</span></span>  
16. <span data-ttu-id="7026e-163">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-163">Click Add.</span></span>
17. <span data-ttu-id="7026e-164">Typ in het veld Beschrijving de tekst "Routenummer".</span><span class="sxs-lookup"><span data-stu-id="7026e-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="7026e-165">Routenummer</span><span class="sxs-lookup"><span data-stu-id="7026e-165">Routing number</span></span>  
18. <span data-ttu-id="7026e-166">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="7026e-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="7026e-167">De bankrekeningstructuur voor dit model definiëren</span><span class="sxs-lookup"><span data-stu-id="7026e-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="7026e-168">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="7026e-169">Typ "Account" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="7026e-170">Rekening</span><span class="sxs-lookup"><span data-stu-id="7026e-170">Account</span></span>  
3. <span data-ttu-id="7026e-171">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="7026e-172">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-172">Click Add.</span></span>
5. <span data-ttu-id="7026e-173">Typ in het veld Beschrijving: "De ID van een rekening van een partij bij een financiële instelling (bijvoorbeeld een bank)".</span><span class="sxs-lookup"><span data-stu-id="7026e-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="7026e-174">De ID van een rekening van een partij bij een financiële instelling (bijvoorbeeld een bank).</span><span class="sxs-lookup"><span data-stu-id="7026e-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="7026e-175">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="7026e-176">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="7026e-177">Valuta</span><span class="sxs-lookup"><span data-stu-id="7026e-177">Currency</span></span>  
8. <span data-ttu-id="7026e-178">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="7026e-179">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-179">Click Add.</span></span>
10. <span data-ttu-id="7026e-180">Typ in het veld Beschrijving de tekst "Valutacode".</span><span class="sxs-lookup"><span data-stu-id="7026e-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="7026e-181">Valutacode</span><span class="sxs-lookup"><span data-stu-id="7026e-181">Currency code</span></span>  
11. <span data-ttu-id="7026e-182">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="7026e-183">Typ "Number" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="7026e-184">Nummer</span><span class="sxs-lookup"><span data-stu-id="7026e-184">Number</span></span>  
13. <span data-ttu-id="7026e-185">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-185">Click Add.</span></span>
14. <span data-ttu-id="7026e-186">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="7026e-187">Typ "IBAN" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="7026e-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="7026e-188">IBAN</span></span>  
16. <span data-ttu-id="7026e-189">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-189">Click Add.</span></span>
17. <span data-ttu-id="7026e-190">Typ in het veld Beschrijving de tekst "Internationaal bankrekeningnummer".</span><span class="sxs-lookup"><span data-stu-id="7026e-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="7026e-191">Internationaal bankrekeningnummer</span><span class="sxs-lookup"><span data-stu-id="7026e-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="7026e-192">De structuur definiëren van het betalingsbericht voor het betalingstype kredietoverdracht</span><span class="sxs-lookup"><span data-stu-id="7026e-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="7026e-193">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="7026e-194">Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".</span><span class="sxs-lookup"><span data-stu-id="7026e-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="7026e-195">Typ "CustomerCreditTransferInitiation" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="7026e-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="7026e-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="7026e-197">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-197">Click Add.</span></span>
5. <span data-ttu-id="7026e-198">Typ in het veld Zoeken de tekst "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="7026e-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="7026e-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="7026e-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="7026e-200">Klik op Vorige zoeken.</span><span class="sxs-lookup"><span data-stu-id="7026e-200">Click Find previous.</span></span>
7. <span data-ttu-id="7026e-201">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="7026e-202">Typ "MessageIdentification" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="7026e-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="7026e-203">MessageIdentification</span></span>  
9. <span data-ttu-id="7026e-204">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-204">Click Add.</span></span>
10. <span data-ttu-id="7026e-205">Typ in het veld Omschrijving: "De punt-naar-punt-verwijzing, zoals toegewezen door de instruerende partij en verzonden naar de volgende partij in de keten, zodat het bericht ondubbelzinnig kan worden geïdentificeerd".</span><span class="sxs-lookup"><span data-stu-id="7026e-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="7026e-206">De verwijzing van punt naar punt die is toegewezen door de instruerende partij (en verzonden naar de volgende partij) om een bericht te identificeren.</span><span class="sxs-lookup"><span data-stu-id="7026e-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="7026e-207">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="7026e-208">Typ "ProcessingDateTime" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="7026e-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="7026e-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="7026e-210">Selecteer "DateTime" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="7026e-211">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-211">Click Add.</span></span>
15. <span data-ttu-id="7026e-212">Typ in het veld Beschrijving: "De datum en tijd waarop het betalingsbericht is gemaakt".</span><span class="sxs-lookup"><span data-stu-id="7026e-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="7026e-213">De datum en tijd waarop het betalingsbericht is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7026e-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="7026e-214">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="7026e-215">Definieer de betalingstransactiestructuur voor dit model.</span><span class="sxs-lookup"><span data-stu-id="7026e-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="7026e-216">Typ "Payments" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="7026e-217">Betalingen</span><span class="sxs-lookup"><span data-stu-id="7026e-217">Payments</span></span>  
18. <span data-ttu-id="7026e-218">Selecteer "Record list" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="7026e-219">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-219">Click Add.</span></span>
20. <span data-ttu-id="7026e-220">Typ "Betalingsregels van het huidige bericht" in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="7026e-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="7026e-221">Betalingsregels van het huidige bericht</span><span class="sxs-lookup"><span data-stu-id="7026e-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="7026e-222">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="7026e-223">Typ "Creditor" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="7026e-224">Incassant</span><span class="sxs-lookup"><span data-stu-id="7026e-224">Creditor</span></span>  
23. <span data-ttu-id="7026e-225">Selecteer "Record" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="7026e-226">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-226">Click Add.</span></span>
25. <span data-ttu-id="7026e-227">Typ in het veld Beschrijving: "Partij aan wie een geldbedrag verschuldigd is".</span><span class="sxs-lookup"><span data-stu-id="7026e-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="7026e-228">Partij aan wie een geldbedrag verschuldigd is.</span><span class="sxs-lookup"><span data-stu-id="7026e-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="7026e-229">Klik op Artikelverwijzing omschakelen.</span><span class="sxs-lookup"><span data-stu-id="7026e-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="7026e-230">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="7026e-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="7026e-231">Partij</span><span class="sxs-lookup"><span data-stu-id="7026e-231">Party</span></span>  
28. <span data-ttu-id="7026e-232">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="7026e-232">Click Find next.</span></span>
29. <span data-ttu-id="7026e-233">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7026e-233">Click OK.</span></span>
30. <span data-ttu-id="7026e-234">Typ in het veld Zoeken de tekst "Betalingen".</span><span class="sxs-lookup"><span data-stu-id="7026e-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="7026e-235">Betalingen</span><span class="sxs-lookup"><span data-stu-id="7026e-235">Payments</span></span>  
31. <span data-ttu-id="7026e-236">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="7026e-236">Click Find next.</span></span>
32. <span data-ttu-id="7026e-237">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="7026e-238">Typ "Debtor" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="7026e-239">Debiteur</span><span class="sxs-lookup"><span data-stu-id="7026e-239">Debtor</span></span>  
34. <span data-ttu-id="7026e-240">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-240">Click Add.</span></span>
35. <span data-ttu-id="7026e-241">Typ in het veld Beschrijving: "Partij die een geldbedrag verschuldigd is aan de (uiteindelijke) crediteur".</span><span class="sxs-lookup"><span data-stu-id="7026e-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="7026e-242">Partij die een geldbedrag verschuldigd is aan de (uiteindelijke) crediteur.</span><span class="sxs-lookup"><span data-stu-id="7026e-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="7026e-243">Klik op Artikelverwijzing omschakelen.</span><span class="sxs-lookup"><span data-stu-id="7026e-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="7026e-244">Typ in het veld Zoeken de tekst "Partij".</span><span class="sxs-lookup"><span data-stu-id="7026e-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="7026e-245">Partij</span><span class="sxs-lookup"><span data-stu-id="7026e-245">Party</span></span>  
38. <span data-ttu-id="7026e-246">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="7026e-246">Click Find next.</span></span>
39. <span data-ttu-id="7026e-247">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="7026e-247">Click OK.</span></span>
40. <span data-ttu-id="7026e-248">Klik op Volgende zoeken.</span><span class="sxs-lookup"><span data-stu-id="7026e-248">Click Find next.</span></span>
41. <span data-ttu-id="7026e-249">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="7026e-250">Typ "Description" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="7026e-251">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="7026e-251">Description</span></span>  
43. <span data-ttu-id="7026e-252">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="7026e-253">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-253">Click Add.</span></span>
45. <span data-ttu-id="7026e-254">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="7026e-255">Typ "Currency" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="7026e-256">Valuta</span><span class="sxs-lookup"><span data-stu-id="7026e-256">Currency</span></span>  
47. <span data-ttu-id="7026e-257">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-257">Click Add.</span></span>
48. <span data-ttu-id="7026e-258">Typ in het veld Beschrijving de tekst "Valutacode".</span><span class="sxs-lookup"><span data-stu-id="7026e-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="7026e-259">Valutacode</span><span class="sxs-lookup"><span data-stu-id="7026e-259">Currency code</span></span>  
49. <span data-ttu-id="7026e-260">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="7026e-261">Typ "TransactionDate" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="7026e-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="7026e-262">TransactionDate</span></span>  
51. <span data-ttu-id="7026e-263">Selecteer "Date" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="7026e-264">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-264">Click Add.</span></span>
53. <span data-ttu-id="7026e-265">Typ in het veld Beschrijving de tekst "Transactiedatum".</span><span class="sxs-lookup"><span data-stu-id="7026e-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="7026e-266">Transactiedatum</span><span class="sxs-lookup"><span data-stu-id="7026e-266">Transaction date</span></span>  
54. <span data-ttu-id="7026e-267">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="7026e-268">Typ "InstructedAmount" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="7026e-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="7026e-269">InstructedAmount</span></span>  
56. <span data-ttu-id="7026e-270">Selecteer "Real" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="7026e-271">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-271">Click Add.</span></span>
58. <span data-ttu-id="7026e-272">Typ in het veld Beschrijving: "Het geldbedrag dat moet worden verplaatst tussen de debiteur en de crediteur, vóór aftrek van toeslagen".</span><span class="sxs-lookup"><span data-stu-id="7026e-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="7026e-273">Het bedrag moet worden uitgedrukt in de valuta die door de initiërende partij is aangevraagd." in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="7026e-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="7026e-274">Het geldbedrag dat moet worden verplaatst tussen de debiteur en de crediteur, vóór aftrek van toeslagen.</span><span class="sxs-lookup"><span data-stu-id="7026e-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="7026e-275">Het bedrag moet worden uitgedrukt in de valuta die door de initiërende partij is aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="7026e-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="7026e-276">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7026e-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="7026e-277">Typ "End2EndID" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="7026e-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="7026e-278">End2EndID</span></span>  
61. <span data-ttu-id="7026e-279">Selecteer "String" in het veld Artikeltype.</span><span class="sxs-lookup"><span data-stu-id="7026e-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="7026e-280">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7026e-280">Click Add.</span></span>
63. <span data-ttu-id="7026e-281">Typ in het veld Beschrijving: "De unieke identificatie die is toegewezen door de initiërende partij".</span><span class="sxs-lookup"><span data-stu-id="7026e-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="7026e-282">Deze identificatie wordt ongewijzigd doorgegeven door de volledige keten heen, van begin tot einde." in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="7026e-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="7026e-283">De unieke identificatie die is toegewezen door de initiërende partij.</span><span class="sxs-lookup"><span data-stu-id="7026e-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="7026e-284">Deze identificatie wordt ongewijzigd doorgegeven door de volledige keten heen, van begin tot einde.</span><span class="sxs-lookup"><span data-stu-id="7026e-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="7026e-285">Typ "PaymentModel" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="7026e-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="7026e-286">De naam PaymentModel is afgestemd op vooraf gedefinieerde interfaces van betalingsformulieren.</span><span class="sxs-lookup"><span data-stu-id="7026e-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="7026e-287">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="7026e-287">Click Save.</span></span>
66. <span data-ttu-id="7026e-288">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7026e-288">Close the page.</span></span>


