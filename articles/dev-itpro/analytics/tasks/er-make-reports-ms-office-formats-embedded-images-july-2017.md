--- 
title: Rapporten maken in Microsoft Office-indelingen met ingesloten afbeeldingen voor elektronische aangifte (ER) (deel 1)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van 'Systeembeheerder' of 'Elektronische ontwikkelaar' ER-configuraties (Electronic Reporting) kan ontwerpen om elektronische documenten te genereren in MS Office-indelingen (Excel en Word) die ingesloten afbeeldingen bevatten.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: f610fe4b7f265c4fc38db89938d5c208b4f7661a
ms.contentlocale: nl-nl
ms.lasthandoff: 11/02/2017

---
# <a name="make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er--part-1"></a>Rapporten maken in Microsoft Office-indelingen met ingesloten afbeeldingen voor elektronische aangifte (ER) (deel 1) 

[!include[task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van 'Systeembeheerder' of 'Elektronische ontwikkelaar' ER-configuraties (Electronic Reporting) kan ontwerpen om elektronische documenten te genereren in MS Office-indelingen (Excel en Word) die ingesloten afbeeldingen bevatten.

In dit voorbeeld gebruikt u gemaakte ER-configuraties voor voorbeeldbedrijf Litware, Inc.  Als u deze stappen wilt voltooien, voert u eerst de stappen uit in de taakbegeleider ER Rapporten in MS Office-indelingen maken met ingesloten afbeeldingen (deel 2: configuraties controleren). Deze stappen kunnen in het USMF-bedrijf worden uitgevoerd.


## <a name="run-format-with-initial-model-mapping"></a>Indeling uitvoeren met initiële modeltoewijzing
1. Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.
2. Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.
3. Klik in het actievenster op Instellen.
4. Klik op Controleren.
5. Klik op Test afdrukken.
    * Voer de indeling uit voor testdoeleinden.  
6. Selecteer Ja in het veld Overdraagbare cheque.
7. Klik op OK.
    * Controleer de gemaakte uitvoer. Houd er rekening mee dat het bedrijfslogo wordt weergegeven in het rapport, alsmede de handtekening van de bevoegde persoon. De handtekeningafbeelding wordt opgehaald uit het veld van het gegevenstype Container van de cheque-indelingsrecord die is gekoppeld aan de geselecteerde bankrekening.  
8. Vouw de sectie Aantal exemplaren uit.
9. Klik op Bewerken.
10. Voer in het veld Watermerk 'Watermerk afdrukken als Ongeldig' in.
    * Wijzig de instelling van de watermerklay-out om de watermerktekst in het genererende document weer te geven in een Excel-shape-element.  
11. Klik op Test afdrukken.
12. Klik op OK.
    * Controleer de gemaakte uitvoer. Houd er rekening mee dat het watermerk wordt weergegeven in het gemaakte rapport overeenkomstig de selectieoptie.  
13. Sluit de pagina.
14. Klik in het actievenster op Betalingen beheren.
15. Klik op Cheques.
16. Klik op Filters weergeven.
17. Pas de volgende filters toe: Voer een filterwaarde van '381', '385', '389' in het veld 'Chequenummer' in met behulp van de filteroperator 'is een van'.
18. Markeer alle rijen in de lijst.
19. Klik op Kopie van cheque afdrukken.
    * Voer de indeling uit om de geselecteerde cheques opnieuw af te drukken.  
    * Controleer de gemaakte uitvoer. Houd er rekening mee dat de geselecteerde cheques opnieuw zijn afgedrukt. Het bedrijfslogo en de labels worden niet afgedrukt omdat deze worden weergegeven op het voorgedrukte formulier.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>De indeling van het geïmporteerde gegevensmodel wijzigen
1. Sluit de pagina.
2. Sluit de pagina.
3. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
4. Selecteer in de structuur Model voor cheques.
5. Klik op Ontwerper.
6. Klik op Model toewijzen aan gegevensbron.
7. Klik op Ontwerper.
    * We wijzigen de binding van het handtekeningitem van het gegevensmodel om een handtekeningafbeelding te krijgen uit het bestand dat is gekoppeld aan de cheque-indelingsrecord die is gekoppeld aan de geselecteerde bankrekening.  
8. Schakel Details weergeven uit.
9. Vouw in de structuur 'indeling' uit.
10. Vouw in de structuur 'indeling\handtekening' uit.
11. Selecteer in de structuur 'indeling\handtekening\afbeelding = chequerekening.'<Relaties'.BankChequeLayout.Signature1Bmp'.
12. Vouw in de structuur 'chequerekening' uit.
13. Vouw in de structuur 'chequerekening\<Relaties' uit.
14. Vouw in de structuur 'chequerekening\<Relaties\BankChequeIndeling'.
15. Vouw in de structuur 'chequerekening\<RelatiesBankChequeIndeling\<Relaties' uit.
16. Vouw in de structuur 'chequerekening\<RelatiesBankChequeIndeling\<Relaties\<Documenten' uit.
17. Selecteer in de structuur 'chequerekening\<Relaties\BankChequeIndeling\<Relaties\<Documenten\getFileContentAsContainer()'.
18. Klik op Binden.
19. Klik op Opslaan.
20. Sluit de pagina.
21. Sluit de pagina.
22. Sluit de pagina.
23. Sluit de pagina.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Indeling uitvoeren met de aangepaste modeltoewijzing
1. Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Bankrekening met een waarde van 'USMF OPER'.
3. Klik in het actievenster op Instellen.
4. Klik op Controleren.
5. Klik op Test afdrukken.
6. Klik op OK.
    * Controleer de gemaakte uitvoer. Houd er rekening mee dat de afbeelding van de Documentbeheer-bijlage wordt gepresenteerd als de handtekening van een bevoegd persoon.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>MS Word-document gebruiken als sjabloon in de geïmporteerde indeling
1. Sluit de pagina.
2. Sluit de pagina.
3. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
4. Vouw in de structuur 'Model voor cheques' uit.
5. Selecteer in de structuur ' Model voor cheques\Afdrukindeling van cheques'.
6. Klik op Ontwerper.
7. Klik op Bijlagen.
8. Klik op Verwijderen.
9. Klik op Ja.
10. Klik op Nieuw.
11. Klik op Bestand.
    * Klik op Bladeren en selecteer het vooraf gedownloade bestand 'Cheque template Word.docx".  
12. Sluit de pagina.
13. Typ of selecteer een waarde in het veld Sjabloon.
14. Klik op Opslaan.
15. Sluit de pagina.
16. Klik op Bewerken.
17. Selecteer Ja in het veld Concept uitvoeren.
18. Sluit de pagina.
19. Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.
20. Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'USMF OPER'.
21. Klik op Controleren.
22. Klik op Test afdrukken.
23. Klik op OK.
    * Controleer de gemaakte uitvoer. Houd er rekening mee dat de uitvoer als MS Word-document is gegenereerd met ingesloten afbeeldingen die het bedrijfslogo, de handtekening van een bevoegd persoon en de geselecteerde tekst van het watermerk voorstellen.  


