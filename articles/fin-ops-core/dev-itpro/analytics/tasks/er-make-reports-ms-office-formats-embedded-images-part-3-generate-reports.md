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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78dcdbd83dc717104d437662f7f451c9ecb714cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684374"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="922b4-103">Rapporten genereren in Office-indeling die ingesloten afbeeldingen bevatten</span><span class="sxs-lookup"><span data-stu-id="922b4-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="922b4-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van 'Systeembeheerder' of 'Elektronische ontwikkelaar' ER-configuraties (Electronic Reporting) kan ontwerpen om elektronische documenten te genereren in MS Office-indelingen (Excel en Word) die ingesloten afbeeldingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="922b4-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="922b4-105">In dit voorbeeld gebruikt u gemaakte ER-configuraties voor voorbeeldbedrijf 'Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="922b4-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="922b4-106">Als u deze stappen wilt voltooien, voert u eerst de stappen uit in de taakbegeleiding "ER Rapporten in MS Office-indelingen maken met ingesloten afbeeldingen (deel 2: configuraties controleren)".</span><span class="sxs-lookup"><span data-stu-id="922b4-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="922b4-107">Deze stappen kunnen in het 'USMF'-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="922b4-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="922b4-108">Indeling uitvoeren met initiële modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="922b4-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="922b4-109">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="922b4-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="922b4-110">Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="922b4-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="922b4-111">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="922b4-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="922b4-112">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="922b4-112">Click Check.</span></span>
5. <span data-ttu-id="922b4-113">Klik op Test afdrukken.</span><span class="sxs-lookup"><span data-stu-id="922b4-113">Click Print test.</span></span>
    * <span data-ttu-id="922b4-114">Voer de indeling uit voor testdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="922b4-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="922b4-115">Selecteer Ja in het veld Overdraagbare cheque.</span><span class="sxs-lookup"><span data-stu-id="922b4-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="922b4-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="922b4-116">Click OK.</span></span>
    * <span data-ttu-id="922b4-117">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="922b4-117">Review the created output.</span></span> <span data-ttu-id="922b4-118">Het bedrijfslogo wordt weergegeven in het rapport, evenals de handtekening van de bevoegde persoon.</span><span class="sxs-lookup"><span data-stu-id="922b4-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="922b4-119">De handtekeningafbeelding wordt opgehaald uit het veld van het gegevenstype 'Container' van de cheque-indelingsrecord die is gekoppeld aan de geselecteerde bankrekening.</span><span class="sxs-lookup"><span data-stu-id="922b4-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="922b4-120">Vouw de sectie Aantal exemplaren uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="922b4-121">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="922b4-121">Click Edit.</span></span>
10. <span data-ttu-id="922b4-122">Voer in het veld Watermerk 'Watermerk afdrukken als Ongeldig' in.</span><span class="sxs-lookup"><span data-stu-id="922b4-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="922b4-123">Wijzig de instelling van de watermerklay-out om de watermerktekst in het genererende document weer te geven in een Excel-shape-element.</span><span class="sxs-lookup"><span data-stu-id="922b4-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="922b4-124">Klik op Test afdrukken.</span><span class="sxs-lookup"><span data-stu-id="922b4-124">Click Print test.</span></span>
12. <span data-ttu-id="922b4-125">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="922b4-125">Click OK.</span></span>
    * <span data-ttu-id="922b4-126">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="922b4-126">Review the created output.</span></span> <span data-ttu-id="922b4-127">Het watermerk wordt weergegeven in het gemaakte rapport overeenkomstig de selectieoptie.</span><span class="sxs-lookup"><span data-stu-id="922b4-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="922b4-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-128">Close the page.</span></span>
14. <span data-ttu-id="922b4-129">Klik in het actievenster op Betalingen beheren.</span><span class="sxs-lookup"><span data-stu-id="922b4-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="922b4-130">Klik op Cheques.</span><span class="sxs-lookup"><span data-stu-id="922b4-130">Click Checks.</span></span>
16. <span data-ttu-id="922b4-131">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="922b4-131">Click Show filters.</span></span>
17. <span data-ttu-id="922b4-132">Pas de volgende filters toe: Voer een filterwaarde van '381', '385', '389' in het veld 'Chequenummer' in met behulp van de filteroperator 'is een van'.</span><span class="sxs-lookup"><span data-stu-id="922b4-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="922b4-133">Markeer alle rijen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="922b4-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="922b4-134">Klik op Kopie van cheque afdrukken.</span><span class="sxs-lookup"><span data-stu-id="922b4-134">Click Print check copy.</span></span>
    * <span data-ttu-id="922b4-135">Voer de indeling uit om de geselecteerde cheques opnieuw af te drukken.</span><span class="sxs-lookup"><span data-stu-id="922b4-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="922b4-136">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="922b4-136">Review the created output.</span></span> <span data-ttu-id="922b4-137">De geselecteerde cheques zijn opnieuw afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="922b4-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="922b4-138">Het bedrijfslogo en de labels worden niet afgedrukt omdat deze worden weergegeven op het voorgedrukte formulier.</span><span class="sxs-lookup"><span data-stu-id="922b4-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="922b4-139">De indeling van het geïmporteerde gegevensmodel wijzigen</span><span class="sxs-lookup"><span data-stu-id="922b4-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="922b4-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-140">Close the page.</span></span>
2. <span data-ttu-id="922b4-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-141">Close the page.</span></span>
3. <span data-ttu-id="922b4-142">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="922b4-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="922b4-143">Selecteer in de structuur 'Model voor cheques'.</span><span class="sxs-lookup"><span data-stu-id="922b4-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="922b4-144">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="922b4-144">Click Designer.</span></span>
6. <span data-ttu-id="922b4-145">Klik op Model toewijzen aan gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="922b4-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="922b4-146">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="922b4-146">Click Designer.</span></span>
    * <span data-ttu-id="922b4-147">We wijzigen de binding van het handtekeningitem van het gegevensmodel om een handtekeningafbeelding te krijgen uit het bestand dat is gekoppeld aan de cheque-indelingsrecord die is gekoppeld aan de geselecteerde bankrekening.</span><span class="sxs-lookup"><span data-stu-id="922b4-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="922b4-148">Schakel Details weergeven uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-148">Turn off Show details.</span></span>
9. <span data-ttu-id="922b4-149">Vouw in de structuur 'indeling' uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="922b4-150">Vouw in de structuur 'indeling\handtekening' uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="922b4-151">Selecteer in de structuur 'indeling\handtekening\afbeelding = chequerekening.'<Relaties'.BankChequeLayout.Signature1Bmp'.</span><span class="sxs-lookup"><span data-stu-id="922b4-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="922b4-152">Vouw in de structuur 'chequerekening' uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="922b4-153">Vouw in de structuur 'chequerekening\<Relaties' uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="922b4-154">Vouw in de structuur 'chequerekening\<Relaties\BankChequeIndeling'.</span><span class="sxs-lookup"><span data-stu-id="922b4-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="922b4-155">Vouw in de structuur 'chequerekening\<RelatiesBankChequeIndeling\<Relaties' uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="922b4-156">Vouw in de structuur 'chequerekening\<RelatiesBankChequeIndeling\<Relaties\<Documenten' uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="922b4-157">Selecteer in de structuur 'chequerekening\<Relaties\BankChequeIndeling\<Relaties\<Documenten\getFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="922b4-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="922b4-158">Klik op Binden.</span><span class="sxs-lookup"><span data-stu-id="922b4-158">Click Bind.</span></span>
19. <span data-ttu-id="922b4-159">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="922b4-159">Click Save.</span></span>
20. <span data-ttu-id="922b4-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-160">Close the page.</span></span>
21. <span data-ttu-id="922b4-161">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-161">Close the page.</span></span>
22. <span data-ttu-id="922b4-162">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-162">Close the page.</span></span>
23. <span data-ttu-id="922b4-163">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="922b4-164">Indeling uitvoeren met de aangepaste modeltoewijzing</span><span class="sxs-lookup"><span data-stu-id="922b4-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="922b4-165">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="922b4-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="922b4-166">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="922b4-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="922b4-167">Filter bijvoorbeeld op het veld Bankrekening met een waarde van 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="922b4-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="922b4-168">Klik in het actievenster op Instellen.</span><span class="sxs-lookup"><span data-stu-id="922b4-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="922b4-169">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="922b4-169">Click Check.</span></span>
5. <span data-ttu-id="922b4-170">Klik op Test afdrukken.</span><span class="sxs-lookup"><span data-stu-id="922b4-170">Click Print test.</span></span>
6. <span data-ttu-id="922b4-171">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="922b4-171">Click OK.</span></span>
    * <span data-ttu-id="922b4-172">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="922b4-172">Review the created output.</span></span> <span data-ttu-id="922b4-173">De afbeelding van de Documentbeheer-bijlage wordt gepresenteerd als de handtekening van een bevoegd persoon.</span><span class="sxs-lookup"><span data-stu-id="922b4-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="922b4-174">MS Word-document gebruiken als sjabloon in de geïmporteerde indeling</span><span class="sxs-lookup"><span data-stu-id="922b4-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="922b4-175">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-175">Close the page.</span></span>
2. <span data-ttu-id="922b4-176">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-176">Close the page.</span></span>
3. <span data-ttu-id="922b4-177">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="922b4-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="922b4-178">Vouw in de structuur 'Model voor cheques' uit.</span><span class="sxs-lookup"><span data-stu-id="922b4-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="922b4-179">Selecteer in de structuur ' Model voor cheques\Afdrukindeling van cheques'.</span><span class="sxs-lookup"><span data-stu-id="922b4-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="922b4-180">Klik op Ontwerper.</span><span class="sxs-lookup"><span data-stu-id="922b4-180">Click Designer.</span></span>
7. <span data-ttu-id="922b4-181">Klik op Bijlagen.</span><span class="sxs-lookup"><span data-stu-id="922b4-181">Click Attachments.</span></span>
8. <span data-ttu-id="922b4-182">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="922b4-182">Click Delete.</span></span>
9. <span data-ttu-id="922b4-183">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="922b4-183">Click Yes.</span></span>
10. <span data-ttu-id="922b4-184">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="922b4-184">Click New.</span></span>
11. <span data-ttu-id="922b4-185">Klik op Bestand.</span><span class="sxs-lookup"><span data-stu-id="922b4-185">Click File.</span></span>
    * <span data-ttu-id="922b4-186">Klik op Bladeren en selecteer het vooraf gedownloade bestand 'Cheque template Word.docx'.</span><span class="sxs-lookup"><span data-stu-id="922b4-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="922b4-187">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-187">Close the page.</span></span>
13. <span data-ttu-id="922b4-188">Typ of selecteer een waarde in het veld Sjabloon.</span><span class="sxs-lookup"><span data-stu-id="922b4-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="922b4-189">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="922b4-189">Click Save.</span></span>
15. <span data-ttu-id="922b4-190">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-190">Close the page.</span></span>
16. <span data-ttu-id="922b4-191">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="922b4-191">Click Edit.</span></span>
17. <span data-ttu-id="922b4-192">Selecteer Ja in het veld Concept uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="922b4-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="922b4-193">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="922b4-193">Close the page.</span></span>
19. <span data-ttu-id="922b4-194">Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.</span><span class="sxs-lookup"><span data-stu-id="922b4-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="922b4-195">Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="922b4-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="922b4-196">Klik op Controleren.</span><span class="sxs-lookup"><span data-stu-id="922b4-196">Click Check.</span></span>
22. <span data-ttu-id="922b4-197">Klik op Test afdrukken.</span><span class="sxs-lookup"><span data-stu-id="922b4-197">Click Print test.</span></span>
23. <span data-ttu-id="922b4-198">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="922b4-198">Click OK.</span></span>
    * <span data-ttu-id="922b4-199">Controleer de gemaakte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="922b4-199">Review the created output.</span></span> <span data-ttu-id="922b4-200">De uitvoer als MS Word-document is gegenereerd met ingesloten afbeeldingen die het bedrijfslogo, de handtekening van een bevoegd persoon en de geselecteerde tekst van het watermerk voorstellen.</span><span class="sxs-lookup"><span data-stu-id="922b4-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  

