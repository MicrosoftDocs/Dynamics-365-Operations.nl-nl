--- 
title: "Modellen toewijzen voor gebruik van financiële dimensies als gegevensbron"
description: "In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.openlocfilehash: c26713a8a391f9f10a6e24f6619c24c1615d4560
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source"></a><span data-ttu-id="5c2a1-103">Modellen toewijzen voor gebruik van financiële dimensies als gegevensbron</span><span class="sxs-lookup"><span data-stu-id="5c2a1-103">Map models  to use financial dimensions as a data source</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c2a1-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="5c2a1-105">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5c2a1-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure “ER Financiële dimensies gebruiken als gegevensbron (Deel 1: Het gegevensmodel ontwerpen)”.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="5c2a1-107">Vereiste gegevensbronnen toevoegen aan modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="5c2a1-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="5c2a1-108">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5c2a1-109">Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".</span><span class="sxs-lookup"><span data-stu-id="5c2a1-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="5c2a1-110">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-110">Click Designer.</span></span>
4. <span data-ttu-id="5c2a1-111">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="5c2a1-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-112">Click New.</span></span>
6. <span data-ttu-id="5c2a1-113">Selecteer Invoer in het veld Definitie.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="5c2a1-114">Typ Toewijzing dimensiegegevens in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="5c2a1-115">Typ Toewijzing dimensiegegevens in het veld Beschrijving.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="5c2a1-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-116">Click Save.</span></span>
10. <span data-ttu-id="5c2a1-117">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-117">Click Designer.</span></span>
11. <span data-ttu-id="5c2a1-118">Selecteer in de structuur 'Dynamics 365 for Operations\Tabel'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="5c2a1-119">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-119">Click Add root.</span></span>
13. <span data-ttu-id="5c2a1-120">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="5c2a1-121">Typ "CompanyInfo" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="5c2a1-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-122">Click OK.</span></span>
16. <span data-ttu-id="5c2a1-123">Selecteer in de structuur "Functies\Financiële dimensies".</span><span class="sxs-lookup"><span data-stu-id="5c2a1-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="5c2a1-124">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-124">Click Add root.</span></span>
    * <span data-ttu-id="5c2a1-125">Deze gegevensbron geeft aan hoe het bereik van financiële dimensies wordt gedefinieerd voor elk rapport dat dit model als gegevensbron gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="5c2a1-126">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="5c2a1-127">Selecteer Ja in het veld Vragen naar dimensies.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="5c2a1-128">Selecteer Ja om toe te staan dat de gebruiker tijdens de uitvoering dimensies selecteert in het formulier Gebruikersdialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="5c2a1-129">Als dit op Nee is ingesteld, worden standaard alle financiële dimensies van de huidige instantie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="5c2a1-130">Selecteer Rechtspersoon in het selectieveld Financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="5c2a1-131">Selecteer Alle om toe te staan dat de gebruiker gewenste dimensies selecteert voor het huidige exemplaar in het Opzoekveld.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="5c2a1-132">Selecteer Rechtspersoon om toe te staan dat de gebruiker dimensies selecteert voor het bedrijf in het Opzoekveld.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="5c2a1-133">Selecteer Dimensie om toe te staan dat de gebruiker dimensies selecteert via één dimensieset.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="5c2a1-134">Selecteer Ja in het veld Vragen naar hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="5c2a1-135">Stel Vragen om hoofdrekening in op Ja aan om gebruikers toe te staan om de hoofdrekening als onderdeel van de lijst van dimensies te selecteren.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="5c2a1-136">Als dit op Nee is ingesteld, wordt de hoofdrekening niet opgenomen in de lijst van dimensies en wordt de optie Is hoofdrekening verplicht ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="5c2a1-137">Als Is hoofdrekening verplicht is ingesteld op Ja, wordt de hoofdrekening in de lijst van dimensies opgenomen ongeacht de keuze van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="5c2a1-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-138">Click OK.</span></span>
23. <span data-ttu-id="5c2a1-139">Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="5c2a1-140">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-140">Click Add root.</span></span>
25. <span data-ttu-id="5c2a1-141">Typ 'LedgerJournal' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="5c2a1-142">Selecteer Ja in het veld Vragen om query.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="5c2a1-143">Typ 'LedgerJournalTable' in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="5c2a1-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="5c2a1-145">Gegevensmodelelementen toewijzen aan toegevoegde gegevensbronnen</span><span class="sxs-lookup"><span data-stu-id="5c2a1-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="5c2a1-146">Vouw in de structuur 'Journaal' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="5c2a1-147">Vouw in de structuur 'Journaal\Transactie' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="5c2a1-148">Vouw in de structuur 'Journaal\Transactie\Dimensiegegevens' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="5c2a1-149">Vouw in de structuur 'Dimensie-instelling'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="5c2a1-150">Vouw in de structuur 'LedgerJournal' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="5c2a1-151">Vouw in de structuur 'LedgerJournal\<Relaties' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="5c2a1-152">Vouw in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="5c2a1-153">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Voucher'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="5c2a1-154">Selecteer in de structuur 'Journaal\Transactie\Voucher'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="5c2a1-155">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-155">Click Bind.</span></span>
11. <span data-ttu-id="5c2a1-156">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="5c2a1-157">Merk op dat voor elke verwijzing naar financiële dimensies die op bijvoorbeeld LedgerDimension is ingesteld, een bijbehorend gegevensbronartikel (LedgerDimension.Dimension) beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="5c2a1-158">Dit gegevensbronartikel biedt de financiële dimensies van die dimensies aan die als recordlijst zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="5c2a1-159">Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="5c2a1-160">Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="5c2a1-161">Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="5c2a1-162">Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Definitie' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="5c2a1-163">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Definitie\Naam'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="5c2a1-164">Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Naam'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="5c2a1-165">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-165">Click Bind.</span></span>
19. <span data-ttu-id="5c2a1-166">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde\Beschrijving'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="5c2a1-167">Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Beschrijving'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="5c2a1-168">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-168">Click Bind.</span></span>
22. <span data-ttu-id="5c2a1-169">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde\Code'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="5c2a1-170">Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Code'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="5c2a1-171">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-171">Click Bind.</span></span>
25. <span data-ttu-id="5c2a1-172">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="5c2a1-173">Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="5c2a1-174">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-174">Click Bind.</span></span>
28. <span data-ttu-id="5c2a1-175">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Debit(AmountCurDebit)'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="5c2a1-176">Selecteer in de structuur 'Journaal\Transactie\Debet'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="5c2a1-177">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-177">Click Bind.</span></span>
31. <span data-ttu-id="5c2a1-178">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Date(TransDate)'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="5c2a1-179">Selecteer in de structuur 'Journaal\Transactie\Datum'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="5c2a1-180">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-180">Click Bind.</span></span>
34. <span data-ttu-id="5c2a1-181">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="5c2a1-182">Selecteer in de structuur 'Journaal\Transactie\Valuta'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="5c2a1-183">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-183">Click Bind.</span></span>
37. <span data-ttu-id="5c2a1-184">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Credit(AmountCurCredit)'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="5c2a1-185">Selecteer in de structuur 'Journaal\Transactie\Credit'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="5c2a1-186">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-186">Click Bind.</span></span>
40. <span data-ttu-id="5c2a1-187">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="5c2a1-188">Selecteer in de structuur 'Journaal\Transactie'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="5c2a1-189">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-189">Click Bind.</span></span>
43. <span data-ttu-id="5c2a1-190">Selecteer in de structuur 'LedgerJournal\Journal batch number(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="5c2a1-191">Selecteer in de structuur 'Journaal\Batch'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="5c2a1-192">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-192">Click Bind.</span></span>
46. <span data-ttu-id="5c2a1-193">Selecteer in de structuur 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="5c2a1-194">Selecteer in de structuur 'Journaal'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="5c2a1-195">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-195">Click Bind.</span></span>
49. <span data-ttu-id="5c2a1-196">Vouw in de structuur 'Dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="5c2a1-197">Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="5c2a1-198">Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="5c2a1-199">Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie\Naam' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="5c2a1-200">Selecteer in de structuur 'Dimensie-instelling\Code'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="5c2a1-201">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-201">Click Bind.</span></span>
55. <span data-ttu-id="5c2a1-202">Selecteer in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie\Naam rapportkolom' uit.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="5c2a1-203">Selecteer in de structuur 'Dimensie-instelling\Naam'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="5c2a1-204">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-204">Click Bind.</span></span>
58. <span data-ttu-id="5c2a1-205">Selecteer in de structuur 'Dimensies\Hoofdrekening en dimensies'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="5c2a1-206">Selecteer in de structuur 'Dimensie-instelling'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="5c2a1-207">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-207">Click Bind.</span></span>
61. <span data-ttu-id="5c2a1-208">Selecteer in de structuur 'Bedrijf'.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="5c2a1-209">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-209">Click Edit.</span></span>
63. <span data-ttu-id="5c2a1-210">Typ in het veld expressionAsStringText 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="5c2a1-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="5c2a1-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="5c2a1-212">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-212">Click Save.</span></span>
65. <span data-ttu-id="5c2a1-213">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-213">Close the page.</span></span>
66. <span data-ttu-id="5c2a1-214">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-214">Click Save.</span></span>
67. <span data-ttu-id="5c2a1-215">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="5c2a1-216">Voltooi de versie van dit concept</span><span class="sxs-lookup"><span data-stu-id="5c2a1-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="5c2a1-217">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-217">Close the page.</span></span>
2. <span data-ttu-id="5c2a1-218">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-218">Close the page.</span></span>
3. <span data-ttu-id="5c2a1-219">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-219">Click Change status.</span></span>
4. <span data-ttu-id="5c2a1-220">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-220">Click Complete.</span></span>
5. <span data-ttu-id="5c2a1-221">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5c2a1-221">Click OK.</span></span>


