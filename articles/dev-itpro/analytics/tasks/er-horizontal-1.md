--- 
title: Een indeling ontwerpen voor het gebruik van horizontaal uitvouwbare bereiken voor het dynamisch toevoegen van kolommen in Excel-rapporten voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken.
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0cd1de95630d0f7c40c3b9948015892623a93686
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Een indeling ontwerpen voor het gebruik van horizontaal uitvouwbare bereiken voor het dynamisch toevoegen van kolommen in Excel-rapporten voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Voordat u deze stappen uitvoert, moet u eerst deze taakbegeleiders uitvoeren: 

'ER Een configuratieprovider maken en deze als actief markeren'

'ER Financiële dimensies gebruiken als gegevensbron (Deel 1: gegevensmodel ontwerpen)'

'ER Financiële dimensies gebruiken als gegevensbron (Deel 2: modeltoewijzing)'

U moet ook een lokale kopie van de sjabloon met een hier gevonden voorbeeldrapport downloaden en opslaan: http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx

Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="create-a-new-report-configuration"></a>Een nieuwe rapportconfiguratie maken
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".
3. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
4. Typ in het veld Nieuw veld 'Indeling gebaseerd op gegevensmodel Voorbeeldmodel Financiële dimensies'.
    * Gebruik het model dat vooraf als gegevensbron voor het nieuwe rapport is gemaakt.  
5. Typ in het veld Naam Voorbeeldrapport met horizontaal uitvouwbare bereiken.
    * Voorbeeldrapport met horizontaal uitvouwbare bereiken  
6. Typ in het veld Omschrijving Excel-uitvoer maken door dynamisch toevoegen van kolommen.
    * Excel-uitvoer maken door dynamisch toevoegen van kolommen  
7. Selecteer Invoer in het veld Definitie gegevensmodel.
8. Klik op Configuratie maken.

## <a name="design-the-report-format"></a>De rapportindeling ontwerpen
1. Klik op Ontwerper.
2. Schakel de wisselknop Details weergeven in.
3. Klik in het actievenster op Importeren.
4. Klik op Importeren uit Excel.
5. Klik op Bijlagen.
    * Importeer de sjabloon van het rapport. Gebruik het Excel-bestand dat u daarvoor hebt gedownload.  
6. Klik op Nieuw.
7. Klik op Bestand.
8. Sluit de pagina.
9. Typ of selecteer een waarde in het veld Sjabloon.
    * Selecteer de gedownloade sjabloon.  
10. Klik op OK.
    * Voeg een nieuwe reeks toe om dynamisch Excel-uitvoer te maken met net zoveel kolommen als u (in het formulier van het gebruikersdialoogvenster) voor financiële dimensies hebt geselecteerd. Elke cel voor elke kolom geeft één naam van de financiële dimensie weer.  
11. Klik op Toevoegen om het dialoogvenster te openen.
12. Selecteer Excel-bereik in de structuur.
13. Typ in het veld Excel-bereik DimNames.
    * DimNames  
14. Selecteer Horizontaal in het veld Replicatierichting.
15. Klik op OK.
16. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.
17. Klik op Omhoog.
18. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.
19. Klik op Knippen.
20. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.
21. Klik op Plakken.
22. Vouw in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' uit.
23. Vouw in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical' uit.
24. Vouw in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>Vertical\Range<TransactionLine>: Vertical' uit.
25. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>Vertical\Range<TransactionLine>: Vertical'.
    * Voeg een nieuwe reeks toe om dynamisch Excel-uitvoer te maken met net zoveel kolommen als u (in het formulier van het gebruikersdialoogvenster) voor financiële dimensies hebt geselecteerd. Elke cel voor elke kolom geeft één waarde van de financiële dimensie weer voor elke aangiftetransactie.  
26. Klik op Bereik toevoegen.
27. Typ in het veld Excel-bereik DimValues.
    * DimValues  
28. Selecteer Horizontaal in het veld Replicatierichting.
29. Klik op OK.
30. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.
31. Klik op Knippen.
32. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.
33. Klik op Plakken.
34. Vouw in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal' uit.

## <a name="map-format-elements-to-data-sources"></a>Indelingselementen aan gegevensbronnen toewijzen
1. Klik op het tabblad Toewijzing.
2. Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies" uit.
3. Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst" uit.
4. Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst" uit.
5. Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst" uit.
6. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.
7. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Code: tekenreeks".
8. Klik op Binden.
9. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.
10. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst".
11. Klik op Binden.
12. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.
13. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Credit: werkelijk" uit.
14. Klik op Binden.
15. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.
16. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Debet: werkelijk" uit.
17. Klik op Binden.
18. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.
19. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Valuta: tekenreeks" uit.
20. Klik op Binden.
21. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.
22. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Datum: Datum".
23. Klik op Binden.
24. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.
25. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Boekstuk: tekenreeks" uit.
26. Klik op Binden.
27. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.
28. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Batch: Tekenreeks".
29. Klik op Binden.
30. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>Vertical\Range<TransactionLine>: Vertical'.
31. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst".
32. Klik op Binden.
33. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.
34. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Batch: Tekenreeks".
35. Klik op Binden.
36. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.
37. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst".
38. Klik op Binden.
39. Vouw in de structuur 'model: Gegevensmodel Voorbeeldmodel Financiële dimensies\Instelling Dimensies: Recordlijst' uit.
40. Selecteer in de structuur 'model: Gegevensmodel Voorbeeldmodel Financiële dimensies\Instelling Dimensies: Recordlijst\Code: Tekenreeks' uit.
41. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.
42. Klik op Binden.
43. Selecteer in de structuur 'model: Gegevensmodel Voorbeeldmodel Financiële dimensies\Instelling Dimensies: Recordlijst'.
44. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.
45. Klik op Binden.
46. Selecteer in de structuur 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.
47. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Bedrijf: Tekenreeks".
48. Klik op Binden.
49. Klik op Opslaan.
50. Sluit de pagina.

