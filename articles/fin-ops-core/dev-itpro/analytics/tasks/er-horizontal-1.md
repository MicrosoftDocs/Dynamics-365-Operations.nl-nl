---
title: 'ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 1: Indeling ontwerpen)'
description: In dit onderwerp wordt beschreven hoe u een ER-indeling (Electronic Reporting) configureert om rapporten te genereren als OPENXML-werkbladbestanden (Excel). (Deel 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3281f3059562fd34f9ccb71a6a11f64bf664008
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093496"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 1: Indeling ontwerpen)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Voordat u deze stappen uitvoert, moet u eerst deze taakbegeleidingen uitvoeren: 

"ER Een configuratieprovider maken en deze als actief markeren"

"ER Financiële dimensies gebruiken als gegevensbron (deel 1: Gegevensmodel ontwerpen)"

"ER Financiële dimensies gebruiken als gegevensbron (deel 2: Modeltoewijzing)"

U moet ook een lokale kopie van de sjabloon met een hier gevonden voorbeeldrapport downloaden en opslaan: [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


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
2. Schakel de wisselknop 'Details weergeven' in.
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
11. Klik op Toevoegen om het uitklapvenster te openen.
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]