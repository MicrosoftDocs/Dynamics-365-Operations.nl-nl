---
title: 'ER Financiële dimensies gebruiken als gegevensbron (deel 3: het rapport ontwerpen)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 29dcf008f342603615241ab75860893cadc2b69e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182434"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a>ER Financiële dimensies gebruiken als gegevensbron (Deel 3: het rapport ontwerpen)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen uitvoeren in de procedure “ER Financiële dimensies gebruiken als gegevensbron (Deel 2: Modeltoewijzing)”.


## <a name="design-a-report-to-present-financial-dimensions"></a>Ontwerp een rapport om financiële dimensies weer te geven
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Selecteer in de structuur "Voorbeeldmodel Financiële dimensies".
3. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
4. Typ in het veld Nieuw veld 'Indeling gebaseerd op gegevensmodel Voorbeeldmodel Financiële dimensies'.
    * Gebruik het model dat vooraf als gegevensbron is gemaakt voor uw nieuwe rapport.  
5. Typ 'Grootboekjournaalrapport' in het veld Naam.
6. Selecteer Invoer in het veld Definitie gegevensmodel.
7. Klik op Configuratie maken.
8. Klik op Ontwerper.
9. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
10. Selecteer "XML\Element" in de structuur.
11. Typ Basis in het veld Naam.
12. Klik op OK.
13. Klik op Toevoegen om het dialoogvenster te openen.
14. Selecteer "XML\Attribute" in de structuur.
15. Typ "Bedrijf" in het veld Naam.
16. Klik op OK.
17. Klik op Toevoegen om het dialoogvenster te openen.
18. Selecteer "XML\Element" in de structuur.
19. Typ Journaal in het veld Naam.
20. Klik op OK.
21. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element".
22. Klik op Toevoegen om het dialoogvenster te openen.
23. Selecteer "XML\Attribute" in de structuur.
24. Typ Batch in het veld Naam.
25. Klik op OK.
26. Klik op Toevoegen om het dialoogvenster te openen.
27. Selecteer "XML\Element" in de structuur.
28. Typ Transactie in het veld Naam.
29. Klik op OK.
30. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element".
31. Klik op Toevoegen om het dialoogvenster te openen.
32. Selecteer "XML\Attribute" in de structuur.
33. Typ Voucher in het veld Naam.
34. Klik op OK.
35. Klik op Kenmerk toevoegen.
36. Typ Datum in het veld Naam.
37. Klik op OK.
38. Klik op Kenmerk toevoegen.
39. Typ "Currency" in het veld Naam.
40. Klik op OK.
41. Klik op Kenmerk toevoegen.
42. Typ 'Dt' in het veld Naam.
43. Klik op OK.
44. Klik op Kenmerk toevoegen.
45. Typ 'Ct' in het veld Naam.
46. Klik op OK.
47. Klik op Toevoegen om het dialoogvenster te openen.
48. Selecteer "XML\Element" in de structuur.
49. Typ Dimensies in het veld Naam.
50. Klik op OK.
51. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element".
52. Klik op Toevoegen om het dialoogvenster te openen.
53. Selecteer "XML\Attribute" in de structuur.
54. Typ Code in het veld Naam.
55. Klik op OK.
56. Klik op Kenmerk toevoegen.
57. Typ Waarde in het veld Naam.
58. Klik op OK.
59. Klik op Kenmerk toevoegen.
60. Typ Desc in het veld Naam.
61. Klik op OK.

## <a name="map-report-elements-to-data-sources"></a>Rapportelementen toewijzen aan gegevensbronnen
1. Klik op het tabblad Toewijzing.
2. Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies" uit.
3. Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst" uit.
4. Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst" uit.
5. Vouw in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst" uit.
6. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Desc: XML-kenmerk".
7. Selecteert in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Beschrijving: tekenreeks".
8. Klik op Binden.
9. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Waarde: XML-kenmerk".
10. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Code: tekenreeks".
11. Klik op Binden.
12. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element\Code: XML-kenmerk".
13. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst\Naam: tekenreeks".
14. Klik op Binden.
15. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Dimensiegegevens: Recordlijst".
16. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dimensies: XML-element".
17. Klik op Binden.
18. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Ct: XML-kenmerk".
19. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Credit: werkelijk" uit.
20. Klik op Binden.
21. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Dt: XML-kenmerk".
22. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Debet: werkelijk" uit.
23. Klik op Binden.
24. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Valuta: XML-kenmerk".
25. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Valuta: tekenreeks" uit.
26. Klik op Binden.
27. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Datum: XML-kenmerk".
28. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Datum: Datum".
29. Klik op Binden.
30. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element\Boekstuk: XML-kenmerk".
31. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst\Boekstuk: tekenreeks" uit.
32. Klik op Binden.
33. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Transactie:XML-element".
34. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Transactie: Recordlijst".
35. Klik op Binden.
36. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element\Batch: XML-kenmerk".
37. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst\Batch: Tekenreeks".
38. Klik op Binden.
39. Selecteer in de structuur "Basis: XML-element\Journaal: XML-element".
40. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Journaal: Recordlijst".
41. Klik op Binden.
42. Selecteer in de structuur "Basis: XML-element\Bedrijf: XML-kenmerk".
43. Selecteer in de structuur "model: Gegevensmodel voorbeeld financiële dimensies\Bedrijf: Tekenreeks".
44. Klik op Binden.
45. Klik op Opslaan.
46. Sluit de pagina.

