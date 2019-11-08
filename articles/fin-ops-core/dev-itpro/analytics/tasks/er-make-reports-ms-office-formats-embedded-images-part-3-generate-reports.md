---
title: Rapporten genereren in Office-indeling die ingesloten afbeeldingen bevatten
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van 'Systeembeheerder' of 'Elektronische ontwikkelaar' ER-configuraties (Electronic Reporting) kan ontwerpen om elektronische documenten te genereren in MS Office-indelingen (Excel en Word) die ingesloten afbeeldingen bevatten.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64fade6578e9cd4f8a51c524e4f6ebbf63b93f20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184756"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="23821-103">Rapporten genereren in Office-indeling die ingesloten afbeeldingen bevatten</span><span class="sxs-lookup"><span data-stu-id="23821-103">Generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23821-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van 'Systeembeheerder' of 'Elektronische ontwikkelaar' ER-configuraties (Electronic Reporting) kan ontwerpen om elektronische documenten te genereren in MS Office-indelingen (Excel en Word) die ingesloten afbeeldingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="23821-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="23821-105">In dit voorbeeld gebruikt u gemaakte ER-configuraties voor voorbeeldbedrijf Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="23821-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="23821-106">Als u deze stappen wilt voltooien, voert u eerst de stappen uit in de taakbegeleiding ER Rapporten in MS Office-indelingen maken met ingesloten afbeeldingen (deel 2: configuraties controleren).</span><span class="sxs-lookup"><span data-stu-id="23821-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="23821-107">Deze stappen kunnen in het USMF-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="23821-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="23821-108">Indeling uitvoeren met initiële modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="23821-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="23821-109">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="23821-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="23821-110">Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="23821-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="23821-111">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="23821-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="23821-112">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="23821-112">Click Check.</span></span>
5. <span data-ttu-id="23821-113">Klik op Test afdrukken.</span><span class="sxs-lookup"><span data-stu-id="23821-113">Click Print test.</span></span>
    * <span data-ttu-id="23821-114">Voer de indeling uit voor testdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="23821-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="23821-115">Selecteer Ja in het veld Overdraagbare cheque.</span><span class="sxs-lookup"><span data-stu-id="23821-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="23821-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23821-116">Click OK.</span></span>
    * <span data-ttu-id="23821-117">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="23821-117">Review the created output.</span></span> <span data-ttu-id="23821-118">Houd er rekening mee dat het bedrijfslogo wordt weergegeven in het rapport, alsmede de handtekening van de bevoegde persoon.</span><span class="sxs-lookup"><span data-stu-id="23821-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="23821-119">De handtekeningafbeelding wordt opgehaald uit het veld van het gegevenstype 'Container' van de cheque-indelingsrecord die is gekoppeld aan de geselecteerde bankrekening.</span><span class="sxs-lookup"><span data-stu-id="23821-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="23821-120">Vouw de sectie Aantal exemplaren uit.</span><span class="sxs-lookup"><span data-stu-id="23821-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="23821-121">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="23821-121">Click Edit.</span></span>
10. <span data-ttu-id="23821-122">Voer in het veld Watermerk 'Watermerk afdrukken als Ongeldig' in.</span><span class="sxs-lookup"><span data-stu-id="23821-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="23821-123">Wijzig de instelling van de watermerklay-out om de watermerktekst in het genererende document weer te geven in een Excel-shape-element.</span><span class="sxs-lookup"><span data-stu-id="23821-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="23821-124">Klik op Test afdrukken.</span><span class="sxs-lookup"><span data-stu-id="23821-124">Click Print test.</span></span>
12. <span data-ttu-id="23821-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23821-125">Click OK.</span></span>
    * <span data-ttu-id="23821-126">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="23821-126">Review the created output.</span></span> <span data-ttu-id="23821-127">Houd er rekening mee dat het watermerk wordt weergegeven in het gemaakte rapport overeenkomstig de selectieoptie.</span><span class="sxs-lookup"><span data-stu-id="23821-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="23821-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-128">Close the page.</span></span>
14. <span data-ttu-id="23821-129">Klik in het actievenster op Betalingen beheren.</span><span class="sxs-lookup"><span data-stu-id="23821-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="23821-130">Klik op Cheques.</span><span class="sxs-lookup"><span data-stu-id="23821-130">Click Checks.</span></span>
16. <span data-ttu-id="23821-131">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="23821-131">Click Show filters.</span></span>
17. <span data-ttu-id="23821-132">Pas de volgende filters toe: Voer een filterwaarde van '381', '385', '389' in het veld 'Chequenummer' in met behulp van de filteroperator 'is een van'.</span><span class="sxs-lookup"><span data-stu-id="23821-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="23821-133">Markeer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="23821-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="23821-134">Klik op Kopie van cheque afdrukken.</span><span class="sxs-lookup"><span data-stu-id="23821-134">Click Print check copy.</span></span>
    * <span data-ttu-id="23821-135">Voer de indeling uit om de geselecteerde cheques opnieuw af te drukken.</span><span class="sxs-lookup"><span data-stu-id="23821-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="23821-136">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="23821-136">Review the created output.</span></span> <span data-ttu-id="23821-137">Houd er rekening mee dat de geselecteerde cheques opnieuw zijn afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="23821-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="23821-138">Het bedrijfslogo en de labels worden niet afgedrukt omdat deze worden weergegeven op het voorgedrukte formulier.</span><span class="sxs-lookup"><span data-stu-id="23821-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="23821-139">De indeling van het geïmporteerde gegevensmodel wijzigen</span><span class="sxs-lookup"><span data-stu-id="23821-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="23821-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-140">Close the page.</span></span>
2. <span data-ttu-id="23821-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-141">Close the page.</span></span>
3. <span data-ttu-id="23821-142">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="23821-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="23821-143">Selecteer in de structuur 'Model voor cheques'.</span><span class="sxs-lookup"><span data-stu-id="23821-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="23821-144">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="23821-144">Click Designer.</span></span>
6. <span data-ttu-id="23821-145">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="23821-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="23821-146">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="23821-146">Click Designer.</span></span>
    * <span data-ttu-id="23821-147">We wijzigen de binding van het handtekeningitem van het gegevensmodel om een handtekeningafbeelding te krijgen uit het bestand dat is gekoppeld aan de cheque-indelingsrecord die is gekoppeld aan de geselecteerde bankrekening.</span><span class="sxs-lookup"><span data-stu-id="23821-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="23821-148">Schakel Details weergeven uit.</span><span class="sxs-lookup"><span data-stu-id="23821-148">Turn Show details off.</span></span>
9. <span data-ttu-id="23821-149">Vouw in de structuur 'indeling' uit.</span><span class="sxs-lookup"><span data-stu-id="23821-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="23821-150">Vouw in de structuur 'indeling\handtekening' uit.</span><span class="sxs-lookup"><span data-stu-id="23821-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="23821-151">Selecteer in de structuur 'indeling\handtekening\afbeelding = chequerekening.'<Relaties'.BankChequeLayout.Signature1Bmp'.</span><span class="sxs-lookup"><span data-stu-id="23821-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="23821-152">Vouw in de structuur 'chequerekening' uit.</span><span class="sxs-lookup"><span data-stu-id="23821-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="23821-153">Vouw in de structuur 'chequerekening\<Relaties' uit.</span><span class="sxs-lookup"><span data-stu-id="23821-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="23821-154">Vouw in de structuur 'chequerekening\<Relaties\BankChequeIndeling'.</span><span class="sxs-lookup"><span data-stu-id="23821-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="23821-155">Vouw in de structuur 'chequerekening\<RelatiesBankChequeIndeling\<Relaties' uit.</span><span class="sxs-lookup"><span data-stu-id="23821-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="23821-156">Vouw in de structuur 'chequerekening\<RelatiesBankChequeIndeling\<Relaties\<Documenten' uit.</span><span class="sxs-lookup"><span data-stu-id="23821-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="23821-157">Selecteer in de structuur 'chequerekening\<Relaties\BankChequeIndeling\<Relaties\<Documenten\getFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="23821-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="23821-158">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="23821-158">Click Bind.</span></span>
19. <span data-ttu-id="23821-159">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="23821-159">Click Save.</span></span>
20. <span data-ttu-id="23821-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-160">Close the page.</span></span>
21. <span data-ttu-id="23821-161">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-161">Close the page.</span></span>
22. <span data-ttu-id="23821-162">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-162">Close the page.</span></span>
23. <span data-ttu-id="23821-163">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="23821-164">Indeling uitvoeren met de aangepaste modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="23821-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="23821-165">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="23821-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="23821-166">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="23821-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="23821-167">Filter bijvoorbeeld op het veld Bankrekening met een waarde van 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="23821-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="23821-168">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="23821-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="23821-169">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="23821-169">Click Check.</span></span>
5. <span data-ttu-id="23821-170">Klik op Test afdrukken.</span><span class="sxs-lookup"><span data-stu-id="23821-170">Click Print test.</span></span>
6. <span data-ttu-id="23821-171">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23821-171">Click OK.</span></span>
    * <span data-ttu-id="23821-172">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="23821-172">Review the created output.</span></span> <span data-ttu-id="23821-173">Houd er rekening mee dat de afbeelding van de Documentbeheer-bijlage wordt gepresenteerd als de handtekening van een bevoegd persoon.</span><span class="sxs-lookup"><span data-stu-id="23821-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="23821-174">MS Word-document gebruiken als sjabloon in de geïmporteerde indeling</span><span class="sxs-lookup"><span data-stu-id="23821-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="23821-175">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-175">Close the page.</span></span>
2. <span data-ttu-id="23821-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-176">Close the page.</span></span>
3. <span data-ttu-id="23821-177">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="23821-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="23821-178">Vouw in de structuur 'Model voor cheques' uit.</span><span class="sxs-lookup"><span data-stu-id="23821-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="23821-179">Selecteer in de structuur ' Model voor cheques\Afdrukindeling van cheques'.</span><span class="sxs-lookup"><span data-stu-id="23821-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="23821-180">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="23821-180">Click Designer.</span></span>
7. <span data-ttu-id="23821-181">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="23821-181">Click Attachments.</span></span>
8. <span data-ttu-id="23821-182">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="23821-182">Click Delete.</span></span>
9. <span data-ttu-id="23821-183">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="23821-183">Click Yes.</span></span>
10. <span data-ttu-id="23821-184">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="23821-184">Click New.</span></span>
11. <span data-ttu-id="23821-185">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="23821-185">Click File.</span></span>
    * <span data-ttu-id="23821-186">Klik op Bladeren en selecteer het vooraf gedownloade bestand 'Cheque template Word.docx".</span><span class="sxs-lookup"><span data-stu-id="23821-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="23821-187">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-187">Close the page.</span></span>
13. <span data-ttu-id="23821-188">Typ of selecteer een waarde in het veld Sjabloon.</span><span class="sxs-lookup"><span data-stu-id="23821-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="23821-189">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="23821-189">Click Save.</span></span>
15. <span data-ttu-id="23821-190">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-190">Close the page.</span></span>
16. <span data-ttu-id="23821-191">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="23821-191">Click Edit.</span></span>
17. <span data-ttu-id="23821-192">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="23821-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="23821-193">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23821-193">Close the page.</span></span>
19. <span data-ttu-id="23821-194">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="23821-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="23821-195">Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="23821-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="23821-196">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="23821-196">Click Check.</span></span>
22. <span data-ttu-id="23821-197">Klik op Test afdrukken.</span><span class="sxs-lookup"><span data-stu-id="23821-197">Click Print test.</span></span>
23. <span data-ttu-id="23821-198">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23821-198">Click OK.</span></span>
    * <span data-ttu-id="23821-199">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="23821-199">Review the created output.</span></span> <span data-ttu-id="23821-200">Houd er rekening mee dat de uitvoer als MS Word-document is gegenereerd met ingesloten afbeeldingen die het bedrijfslogo, de handtekening van een bevoegd persoon en de geselecteerde tekst van het watermerk voorstellen.</span><span class="sxs-lookup"><span data-stu-id="23821-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  
