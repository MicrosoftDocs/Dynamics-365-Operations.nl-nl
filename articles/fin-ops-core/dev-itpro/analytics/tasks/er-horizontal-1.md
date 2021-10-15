---
title: 'ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 1: Indeling ontwerpen)'
description: In dit onderwerp wordt beschreven hoe u een ER-indeling (Electronic Reporting) configureert om rapporten te genereren als OPENXML-werkbladbestanden (Excel). (Deel 1)
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab360c259af37ce3995d3cd2560bc2e765e0bceb
ms.sourcegitcommit: e3290eb58ae569a59d6ae2e6922e7d8be8f1980f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2021
ms.locfileid: "7551771"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen (deel 1: Indeling ontwerpen)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die aan de rol van systeembeheerder of ontwikkelaar elektronische rapportage is toegewezen, een elektronische rapportindeling (ER) kan configureren om rapporten als OPENXML-werkbladen (Excel-bestanden) te genereren waarin de vereiste kolommen dynamisch kunnen worden gemaakt als horizontaal uitvouwbare bereiken. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Voordat u deze stappen uitvoert, moet u eerst deze taakbegeleidingen uitvoeren:

"ER Een configuratieprovider maken en deze als actief markeren"

"ER Financiële dimensies gebruiken als gegevensbron (deel 1: Gegevensmodel ontwerpen)"

"ER Financiële dimensies gebruiken als gegevensbron (deel 2: Modeltoewijzing)"

U moet ook een lokale kopie van de sjabloon met een hier gevonden voorbeeldrapport downloaden en opslaan: [Sample Financial Dimensions Web Service Report](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.

## <a name="create-a-new-report-configuration"></a>Een nieuwe rapportconfiguratie maken

1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Selecteer in de structuur `Financial dimensions sample model`.
3. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
4. Voer in het veld Nieuw `Format based on data model Financial dimensions sample model` in.
    * Gebruik het model dat vooraf als gegevensbron voor het nieuwe rapport is gemaakt.  
5. Typ `Sample report with horizontally expandable ranges` in het veld Naam.
    * Voorbeeldrapport met horizontaal uitvouwbare bereiken  
6. Typ in het veld Omschrijving `To make Excel output with dynamically adding columns`.
    * Excel-uitvoer maken door dynamisch toevoegen van kolommen  
7. Selecteer Invoer in het veld Definitie gegevensmodel.
8. Klik op Configuratie maken.

## <a name="design-the-report-format"></a>De rapportindeling ontwerpen

1. Klik op Ontwerper.
2. Schakel de wisselknop `Show details` in.
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
12. Selecteer in de structuur `Excel\Range`.
13. Typ in het veld Excel-bereik `DimNames`.
    * DimNames  
14. Selecteer `Horizontal` in het veld Replicatierichting.
15. Klik op OK.
16. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
17. Klik op Omhoog.
18. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Cell<DimNames>`.
19. Klik op Knippen.
20. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
21. Klik op Plakken.
22. Vouw in de structuur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` uit.
23. Vouw in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical` uit.
24. Vouw in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` uit.
25. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
    * Voeg een nieuwe reeks toe om dynamisch Excel-uitvoer te maken met net zoveel kolommen als u (in het formulier van het gebruikersdialoogvenster) voor financiële dimensies hebt geselecteerd. Elke cel voor elke kolom geeft één waarde van de financiële dimensie weer voor elke aangiftetransactie.  
26. Klik op Bereik toevoegen.
27. Typ in het veld Excel-bereik `DimValues`.
    * DimValues  
28. Selecteer `Horizontal` in het veld Replicatierichting.
29. Klik op OK.
30. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>`.
31. Klik op Knippen.
32. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
33. Klik op Plakken.
34. Vouw in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` uit.

## <a name="map-format-elements-to-data-sources"></a>Indelingselementen aan gegevensbronnen toewijzen

1. Klik op het tabblad Toewijzing.
2. Vouw in de structuur `model: Data model Financial dimensions sample model` uit.
3. Vouw in de structuur `model: Data model Financial dimensions sample model\Journal: Record list` uit.
4. Vouw in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list` uit.
5. Vouw in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list` uit.
6. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>`.
7. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String`.
8. Klik op Binden.
9. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
10. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
11. Klik op Binden.
12. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>`.
13. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real`.
14. Klik op Binden.
15. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>`.
16. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real`.
17. Klik op Binden.
18. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>`.
19. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String`.
20. Klik op Binden.
21. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>`.
22. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date`.
23. Klik op Binden.
24. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>`.
25. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String`.
26. Klik op Binden.
27. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>`.
28. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
29. Klik op Binden.
30. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
31. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
32. Klik op Binden.
33. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>`.
34. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
35. Klik op Binden.
36. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
37. Selecteer in de structuur `model: Data model Financial dimensions sample model\Journal: Record list`.
38. Klik op Binden.
39. Vouw in de structuur `model: Data model Financial dimensions sample model\Dimensions setting: Record list` uit.
40. Selecteer in de structuur `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String`.
41. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>`.
42. Klik op Binden.
43. Selecteer in de structuur `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
44. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
45. Klik op Binden.
46. Selecteer in de structuur `Excel = "SampleFinDimWsReport"\Cell<CompanyName>`.
47. Selecteer in de structuur `model: Data model Financial dimensions sample model\Company: String`.
48. Klik op Binden.
49. Klik op Opslaan.
50. Sluit de pagina.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
