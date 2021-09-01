---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 2: Modeltoewijzing)'
description: In dit onderwerp wordt beschreven hoe u een ER-model (Electronic Reporting) configureert om financiële dimensies te gebruiken als gegevensbron voor ER-rapporten. (Deel 2)
author: NickSelin
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
ms.openlocfilehash: 921077cb3bc2d01c418f653194e948a2f29cc90dbd562d022ca69aa083a6ef54
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713889"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a>ER Financiële dimensies gebruiken als gegevensbron (deel 2: Modeltoewijzing)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure "ER Financiële dimensies gebruiken als gegevensbron (Deel 1: Het gegevensmodel ontwerpen)".


## <a name="add-required-data-sources-to-model-mapping"></a>Vereiste gegevensbronnen toevoegen aan modeltoewijzing
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".
3. Klik op Ontwerper.
4. Klik op Model toewijzen aan gegevensbron.
5. Klik op Nieuw.
6. Selecteer Invoer in het veld Definitie.
7. Typ Toewijzing dimensiegegevens in het veld Naam.
8. Typ Toewijzing dimensiegegevens in het veld Beschrijving.
9. Klik op Opslaan.
10. Klik op Ontwerper.
11. Selecteer in de structuur 'Dynamics 365 for Operations\Tabel'.
12. Klik op Basis toevoegen.
13. Typ "Bedrijf" in het veld Naam.
14. Typ "CompanyInfo" in het veld Tabel.
15. Klik op OK.
16. Selecteer in de structuur "Functies\Financiële dimensies".
17. Klik op Basis toevoegen.
    * Deze gegevensbron geeft aan hoe het bereik van financiële dimensies wordt gedefinieerd voor elk rapport dat dit model als gegevensbron gebruikt.  
18. Typ een waarde in het veld Naam.
19. Selecteer Ja in het veld Vragen naar dimensies.
    * Selecteer Ja om toe te staan dat de gebruiker tijdens de uitvoering dimensies selecteert in het formulier Gebruikersdialoogvenster. Als dit op Nee is ingesteld, worden standaard alle financiële dimensies van de huidige instantie gebruikt.  
20. Selecteer Rechtspersoon in het selectieveld Financiële dimensies.
    * Selecteer Alle om toe te staan dat de gebruiker gewenste dimensies selecteert voor het huidige exemplaar in het Opzoekveld.  Selecteer Rechtspersoon om toe te staan dat de gebruiker dimensies selecteert voor het bedrijf in het Opzoekveld.  Selecteer Dimensie om toe te staan dat de gebruiker dimensies selecteert via één dimensieset.  
21. Selecteer Ja in het veld Vragen naar hoofdrekening.
    * Stel 'Vragen om hoofdrekening' in op Ja aan om gebruikers toe te staan om de hoofdrekening als onderdeel van de lijst van dimensies te selecteren.   Als dit op Nee is ingesteld, wordt de hoofdrekening niet opgenomen in de lijst van dimensies en wordt de optie 'Is hoofdrekening verplicht' ingeschakeld. Als "Is hoofdrekening verplicht" is ingesteld op Ja, wordt de hoofdrekening in de lijst van dimensies opgenomen ongeacht de keuze van de gebruiker.  
22. Klik op OK.
![Pagina voor ontwerper van ER-modeltoewijzingen.](../media/er-financial-dimensions-guides-model-mapping1.png)
23. Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.
24. Klik op Basis toevoegen.
25. Typ 'LedgerJournal' in het veld Naam.
26. Selecteer Ja in het veld Vragen om query.
27. Typ 'LedgerJournalTable' in het veld Tabel.
28. Klik op OK.
![Pagina voor ontwerper van ER-modeltoewijzingen.](../media/er-financial-dimensions-guides-model-mapping2.png)

## <a name="map-data-model-elements-to-added-data-sources"></a>Gegevensmodelelementen toewijzen aan toegevoegde gegevensbronnen
1. Vouw in de structuur 'Journaal' uit.
2. Vouw in de structuur 'Journaal\Transactie' uit.
3. Vouw in de structuur 'Journaal\Transactie\Dimensiegegevens' uit.
4. Vouw in de structuur 'Dimensie-instelling'.
5. Vouw in de structuur 'LedgerJournal' uit.
6. Vouw in de structuur 'LedgerJournal\<Relaties' uit.
7. Vouw in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans' uit.
8. Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Voucher'.
9. Selecteer in de structuur 'Journaal\Transactie\Voucher'.
10. Klik op Binden.
11. Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.
    * Merk op dat voor elke verwijzing naar financiële dimensies die op bijvoorbeeld LedgerDimension is ingesteld, een bijbehorend gegevensbronartikel (LedgerDimension.Dimension) beschikbaar is. Dit gegevensbronartikel biedt de financiële dimensies van die dimensies aan die als recordlijst zijn ingesteld.  
12. Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' uit.
13. Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies' uit.
14. Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde' uit.
15. Vouw in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Definitie' uit.
16. Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Definitie\Naam'.
17. Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Naam'.
18. Klik op Binden.
19. Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde\Beschrijving'.
20. Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Beschrijving'.
21. Klik op Binden.
22. Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies\Waarde\Code'.
23. Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens\Code'.
24. Klik op Binden.
25. Selecteer in de structuur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hoofdrekening en dimensies'.
26. Selecteer in de structuur 'Journaal\Transactie\Dimensiegegevens'.
27. Klik op Binden.
![Pagina voor ontwerper van ER-modeltoewijzingen.](../media/er-financial-dimensions-guides-model-mapping3.png)
28. Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Debit(AmountCurDebit)'.
29. Selecteer in de structuur 'Journaal\Transactie\Debet'.
30. Klik op Binden.
31. Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Date(TransDate)'.
32. Selecteer in de structuur 'Journaal\Transactie\Datum'.
33. Klik op Binden.
34. Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Currency(CurrencyCode)'.
35. Selecteer in de structuur 'Journaal\Transactie\Valuta'.
36. Klik op Binden.
37. Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans\Credit(AmountCurCredit)'.
38. Selecteer in de structuur 'Journaal\Transactie\Credit'.
39. Klik op Binden.
40. Selecteer in de structuur 'LedgerJournal\<Relaties\LedgerJournalTrans'.
41. Selecteer in de structuur 'Journaal\Transactie'.
42. Klik op Binden.
43. Selecteer in de structuur 'LedgerJournal\Journal batch number(JournalNum)'.
44. Selecteer in de structuur 'Journaal\Batch'.
45. Klik op Binden.
46. Selecteer in de structuur 'LedgerJournal'.
47. Selecteer in de structuur 'Journaal'.
48. Klik op Binden.
49. Vouw in de structuur 'Dimensies' uit.
50. Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies' uit.
51. Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie' uit.
52. Vouw in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie\Naam' uit.
53. Selecteer in de structuur 'Dimensie-instelling\Code'.
54. Klik op Binden.
55. Selecteer in de structuur 'Dimensies\Hoofdrekening en dimensies\Definitie\Naam rapportkolom' uit.
56. Selecteer in de structuur 'Dimensie-instelling\Naam'.
57. Klik op Binden.
58. Selecteer in de structuur 'Dimensies\Hoofdrekening en dimensies'.
59. Selecteer in de structuur 'Dimensie-instelling'.
60. Klik op Binden.
61. Selecteer in de structuur 'Bedrijf'.
62. Klik op Bewerken.
63. Typ in het veld expressionAsStringText 'Company.'find()'.'name()''.
    * Company.'find()'.'name()'  
64. Klik op Opslaan.
![Pagina voor ontwerper van ER-modeltoewijzingen.](../media/er-financial-dimensions-guides-model-mapping4.png)
65. Sluit de pagina.
66. Klik op Opslaan.
67. Sluit de pagina.

## <a name="complete-this-draft-models-version"></a>Voltooi de versie van dit concept
1. Sluit de pagina.
2. Sluit de pagina.
3. Klik op Status wijzigen.
4. Klik op Voltooien.
5. Klik op OK.
![Pagina voor ontwerper van ER-modeltoewijzingen.](../media/er-financial-dimensions-guides-model-mapping5.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]