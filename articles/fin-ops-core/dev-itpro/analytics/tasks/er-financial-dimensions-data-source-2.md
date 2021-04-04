---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 2: Modeltoewijzing)'
description: In dit onderwerp wordt beschreven hoe u een ER-model (Electronic Reporting) configureert om financiële dimensies te gebruiken als gegevensbron voor ER-rapporten. (Deel 2)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59f65962ef8f6ae79190b6595a313831eca53830
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570163"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="e54af-104">ER Financiële dimensies gebruiken als gegevensbron (deel 2: Modeltoewijzing)</span><span class="sxs-lookup"><span data-stu-id="e54af-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e54af-105">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.</span><span class="sxs-lookup"><span data-stu-id="e54af-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="e54af-106">Deze stappen kunnen in elk bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e54af-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="e54af-107">Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure "ER Financiële dimensies gebruiken als gegevensbron (Deel 1: Het gegevensmodel ontwerpen)".</span><span class="sxs-lookup"><span data-stu-id="e54af-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="e54af-108">Vereiste gegevensbronnen toevoegen aan modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="e54af-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="e54af-109">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="e54af-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e54af-110">Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".</span><span class="sxs-lookup"><span data-stu-id="e54af-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="e54af-111">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="e54af-111">Click Designer.</span></span>
4. <span data-ttu-id="e54af-112">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="e54af-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="e54af-113">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e54af-113">Click New.</span></span>
6. <span data-ttu-id="e54af-114">Selecteer Invoer in het veld Definitie.</span><span class="sxs-lookup"><span data-stu-id="e54af-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="e54af-115">Typ Toewijzing dimensiegegevens in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e54af-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="e54af-116">Typ Toewijzing dimensiegegevens in het veld Beschrijving.</span><span class="sxs-lookup"><span data-stu-id="e54af-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="e54af-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e54af-117">Click Save.</span></span>
10. <span data-ttu-id="e54af-118">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="e54af-118">Click Designer.</span></span>
11. <span data-ttu-id="e54af-119">Selecteer in de structuur 'Dynamics 365 for Operations\Tabel'.</span><span class="sxs-lookup"><span data-stu-id="e54af-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="e54af-120">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e54af-120">Click Add root.</span></span>
13. <span data-ttu-id="e54af-121">Typ "Bedrijf" in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e54af-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="e54af-122">Typ "CompanyInfo" in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="e54af-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="e54af-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e54af-123">Click OK.</span></span>
16. <span data-ttu-id="e54af-124">Selecteer in de structuur "Functies\Financiële dimensies".</span><span class="sxs-lookup"><span data-stu-id="e54af-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="e54af-125">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e54af-125">Click Add root.</span></span>
    * <span data-ttu-id="e54af-126">Deze gegevensbron geeft aan hoe het bereik van financiële dimensies wordt gedefinieerd voor elk rapport dat dit model als gegevensbron gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e54af-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="e54af-127">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e54af-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="e54af-128">Selecteer Ja in het veld Vragen naar dimensies.</span><span class="sxs-lookup"><span data-stu-id="e54af-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="e54af-129">Selecteer Ja om toe te staan dat de gebruiker tijdens de uitvoering dimensies selecteert in het formulier Gebruikersdialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="e54af-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="e54af-130">Als dit op Nee is ingesteld, worden standaard alle financiële dimensies van de huidige instantie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e54af-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="e54af-131">Selecteer Rechtspersoon in het selectieveld Financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="e54af-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="e54af-132">Selecteer Alle om toe te staan dat de gebruiker gewenste dimensies selecteert voor het huidige exemplaar in het Opzoekveld.</span><span class="sxs-lookup"><span data-stu-id="e54af-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="e54af-133">Selecteer Rechtspersoon om toe te staan dat de gebruiker dimensies selecteert voor het bedrijf in het Opzoekveld.</span><span class="sxs-lookup"><span data-stu-id="e54af-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="e54af-134">Selecteer Dimensie om toe te staan dat de gebruiker dimensies selecteert via één dimensieset.</span><span class="sxs-lookup"><span data-stu-id="e54af-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="e54af-135">Selecteer Ja in het veld Vragen naar hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="e54af-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="e54af-136">Stel 'Vragen om hoofdrekening' in op Ja aan om gebruikers toe te staan om de hoofdrekening als onderdeel van de lijst van dimensies te selecteren.</span><span class="sxs-lookup"><span data-stu-id="e54af-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="e54af-137">Als dit op Nee is ingesteld, wordt de hoofdrekening niet opgenomen in de lijst van dimensies en wordt de optie 'Is hoofdrekening verplicht' ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e54af-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="e54af-138">Als "Is hoofdrekening verplicht" is ingesteld op Ja, wordt de hoofdrekening in de lijst van dimensies opgenomen ongeacht de keuze van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="e54af-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="e54af-139">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e54af-139">Click OK.</span></span>
<span data-ttu-id="e54af-140">![Pagina voor ontwerper van ER-modeltoewijzingen](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="e54af-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="e54af-141">Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.</span><span class="sxs-lookup"><span data-stu-id="e54af-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="e54af-142">Klik op Basis toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e54af-142">Click Add root.</span></span>
25. <span data-ttu-id="e54af-143">Typ 'LedgerJournal' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e54af-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="e54af-144">Selecteer Ja in het veld Vragen om query.</span><span class="sxs-lookup"><span data-stu-id="e54af-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="e54af-145">Typ 'LedgerJournalTable' in het veld Tabel.</span><span class="sxs-lookup"><span data-stu-id="e54af-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="e54af-146">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e54af-146">Click OK.</span></span>
<span data-ttu-id="e54af-147">![Pagina voor ontwerper van ER-modeltoewijzingen](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="e54af-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="e54af-148">Gegevensmodelelementen toewijzen aan toegevoegde gegevensbronnen</span><span class="sxs-lookup"><span data-stu-id="e54af-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="e54af-149">Vouw in de structuur 'Journaal' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="e54af-150">Vouw in de structuur 'Journaal\Transactie' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="e54af-151">Vouw in de structuur 'Journaal\Transactie\Dimensiegegevens' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="e54af-152">Vouw in de structuur 'Dimensie-instelling'.</span><span class="sxs-lookup"><span data-stu-id="e54af-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="e54af-153">Vouw in de structuur 'LedgerJournal' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="e54af-154">Vouw in de structuur 'LedgerJournal\<Relaties' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="e54af-155">Vouw in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="e54af-156">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Voucher'.</span><span class="sxs-lookup"><span data-stu-id="e54af-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="e54af-157">Selecteer in de structuur 'Journaal\Transactie\Voucher'.</span><span class="sxs-lookup"><span data-stu-id="e54af-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="e54af-158">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-158">Click Bind.</span></span>
11. <span data-ttu-id="e54af-159">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span><span class="sxs-lookup"><span data-stu-id="e54af-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="e54af-160">Merk op dat voor elke verwijzing naar financiële dimensies die op bijvoorbeeld LedgerDimension is ingesteld, een bijbehorend gegevensbronartikel (LedgerDimension.Dimension) beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="e54af-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="e54af-161">Dit gegevensbronartikel biedt de financiële dimensies van die dimensies aan die als recordlijst zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e54af-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="e54af-162">Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="e54af-163">Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="e54af-164">Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="e54af-165">Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Definitie' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="e54af-166">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Definitie\Naam'.</span><span class="sxs-lookup"><span data-stu-id="e54af-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="e54af-167">Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Naam'.</span><span class="sxs-lookup"><span data-stu-id="e54af-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="e54af-168">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-168">Click Bind.</span></span>
19. <span data-ttu-id="e54af-169">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde\Beschrijving'.</span><span class="sxs-lookup"><span data-stu-id="e54af-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="e54af-170">Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Beschrijving'.</span><span class="sxs-lookup"><span data-stu-id="e54af-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="e54af-171">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-171">Click Bind.</span></span>
22. <span data-ttu-id="e54af-172">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde\Code'.</span><span class="sxs-lookup"><span data-stu-id="e54af-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="e54af-173">Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Code'.</span><span class="sxs-lookup"><span data-stu-id="e54af-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="e54af-174">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-174">Click Bind.</span></span>
25. <span data-ttu-id="e54af-175">Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies'.</span><span class="sxs-lookup"><span data-stu-id="e54af-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="e54af-176">Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens'.</span><span class="sxs-lookup"><span data-stu-id="e54af-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="e54af-177">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-177">Click Bind.</span></span>
<span data-ttu-id="e54af-178">![Pagina voor ontwerper van ER-modeltoewijzingen](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="e54af-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="e54af-179">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Debit(AmountCurDebit)'.</span><span class="sxs-lookup"><span data-stu-id="e54af-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="e54af-180">Selecteer in de structuur 'Journaal\Transactie\Debet'.</span><span class="sxs-lookup"><span data-stu-id="e54af-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="e54af-181">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-181">Click Bind.</span></span>
31. <span data-ttu-id="e54af-182">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Date(TransDate)'.</span><span class="sxs-lookup"><span data-stu-id="e54af-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="e54af-183">Selecteer in de structuur 'Journaal\Transactie\Datum'.</span><span class="sxs-lookup"><span data-stu-id="e54af-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="e54af-184">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-184">Click Bind.</span></span>
34. <span data-ttu-id="e54af-185">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="e54af-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="e54af-186">Selecteer in de structuur 'Journaal\Transactie\Valuta'.</span><span class="sxs-lookup"><span data-stu-id="e54af-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="e54af-187">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-187">Click Bind.</span></span>
37. <span data-ttu-id="e54af-188">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Credit(AmountCurCredit)'.</span><span class="sxs-lookup"><span data-stu-id="e54af-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="e54af-189">Selecteer in de structuur 'Journaal\Transactie\Credit'.</span><span class="sxs-lookup"><span data-stu-id="e54af-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="e54af-190">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-190">Click Bind.</span></span>
40. <span data-ttu-id="e54af-191">Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans'.</span><span class="sxs-lookup"><span data-stu-id="e54af-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="e54af-192">Selecteer in de structuur 'Journaal\Transactie'.</span><span class="sxs-lookup"><span data-stu-id="e54af-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="e54af-193">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-193">Click Bind.</span></span>
43. <span data-ttu-id="e54af-194">Selecteer in de structuur 'LedgerJournal\Journal batch number(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="e54af-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="e54af-195">Selecteer in de structuur 'Journaal\Batch'.</span><span class="sxs-lookup"><span data-stu-id="e54af-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="e54af-196">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-196">Click Bind.</span></span>
46. <span data-ttu-id="e54af-197">Selecteer in de structuur 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="e54af-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="e54af-198">Selecteer in de structuur 'Journaal'.</span><span class="sxs-lookup"><span data-stu-id="e54af-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="e54af-199">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-199">Click Bind.</span></span>
49. <span data-ttu-id="e54af-200">Vouw in de structuur 'Dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="e54af-201">Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="e54af-202">Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="e54af-203">Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie\Naam' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="e54af-204">Selecteer in de structuur 'Dimensie-instelling\Code'.</span><span class="sxs-lookup"><span data-stu-id="e54af-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="e54af-205">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-205">Click Bind.</span></span>
55. <span data-ttu-id="e54af-206">Selecteer in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie\Naam rapportkolom' uit.</span><span class="sxs-lookup"><span data-stu-id="e54af-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="e54af-207">Selecteer in de structuur 'Dimensie-instelling\Naam'.</span><span class="sxs-lookup"><span data-stu-id="e54af-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="e54af-208">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-208">Click Bind.</span></span>
58. <span data-ttu-id="e54af-209">Selecteer in de structuur 'Dimensies\Hoofdrekening en dimensies'.</span><span class="sxs-lookup"><span data-stu-id="e54af-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="e54af-210">Selecteer in de structuur 'Dimensie-instelling'.</span><span class="sxs-lookup"><span data-stu-id="e54af-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="e54af-211">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="e54af-211">Click Bind.</span></span>
61. <span data-ttu-id="e54af-212">Selecteer in de structuur 'Bedrijf'.</span><span class="sxs-lookup"><span data-stu-id="e54af-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="e54af-213">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="e54af-213">Click Edit.</span></span>
63. <span data-ttu-id="e54af-214">Typ in het veld expressionAsStringText 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="e54af-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="e54af-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="e54af-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="e54af-216">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e54af-216">Click Save.</span></span>
<span data-ttu-id="e54af-217">![Pagina voor ontwerper van ER-modeltoewijzingen](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="e54af-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="e54af-218">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e54af-218">Close the page.</span></span>
66. <span data-ttu-id="e54af-219">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e54af-219">Click Save.</span></span>
67. <span data-ttu-id="e54af-220">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e54af-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="e54af-221">Voltooi de versie van dit concept</span><span class="sxs-lookup"><span data-stu-id="e54af-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="e54af-222">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e54af-222">Close the page.</span></span>
2. <span data-ttu-id="e54af-223">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e54af-223">Close the page.</span></span>
3. <span data-ttu-id="e54af-224">Klik op Status wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e54af-224">Click Change status.</span></span>
4. <span data-ttu-id="e54af-225">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="e54af-225">Click Complete.</span></span>
5. <span data-ttu-id="e54af-226">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e54af-226">Click OK.</span></span>
<span data-ttu-id="e54af-227">![Pagina voor ontwerper van ER-modeltoewijzingen](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="e54af-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]