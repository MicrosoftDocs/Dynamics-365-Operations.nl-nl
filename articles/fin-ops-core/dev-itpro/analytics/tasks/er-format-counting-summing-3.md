---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 3: Berekeningen gebruiken om de uitvoer te maken)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8a4965c07c5a084b21da40667747db36530284c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141943"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>ER Indeling configureren voor tellen en totaliseren (deel 3: Berekeningen gebruiken om de uitvoer te maken)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 2: Berekeningen configureren)".

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Configureer dit rapport om tellings- en totaliseringsgegevens te gebruiken
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Rapportconfiguraties.
3. Vouw in de structuur 'Intrastat-model' uit.
4. Vouw in de structuur 'Intrastat-model\Intrastat (DE)' uit.
5. Selecteer in de structuur 'Intrastat-model\Intrastat (DE)\Intrastat (DE) met tellen en totaliseren'.
6. Klik op Ontwerper.
7. Klik op het tabblad Toewijzing.
8. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
    * Voeg een nieuwe gegevensbron toe om de lijst van onthouden blokken op te halen.  
9. Selecteer "Functions\Calculated field" in de structuur.
10. Typ '$BlocksList' in het veld Naam.
    * $BlocksList  
11. Klik op Formule bewerken.
12. Selecteer in de structuur 'Gegevenscollectiefuncties\COLLECTEDLIST'.
13. Klik op Functie toevoegen.
14. Klik op Gegevensbron toevoegen.
15. Typ in het veld Formule 'COLLECTEDLIST('$BlockName', '.
    * COLLECTEDLIST('$BlockName',  
16. Typ in het veld Formule 'COLLECTEDLIST('$BlockName', "*")'.
    * COLLECTEDLIST('$BlockName', "*")  
17. Klik op Opslaan.
    * Het patroon "*" betekent dat alle blokken in de lijst voor dit record worden opgenomen.  
18. Sluit de pagina.
19. Klik op OK.
20. Klik op het tabblad Indeling.
21. Selecteer Intrastat\Gegevens in de structuur.
22. Klik op Toevoegen om het dialoogvenster te openen.
23. Selecteer in de structuur 'Tekst\Reeks'.
24. Typ 'Totalen per blokken' in het veld Naam.
    * Totalen per blokken  
25. Selecteer in het veld Speciale tekens 'Nieuwe regel - Windows (CR LF)'.
26. Klik op OK.
27. Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken'.
28. Klik op Toevoegen om het dialoogvenster te openen.
29. Selecteer "Text\String" in de structuur.
30. Typ Blokcode in het veld Naam.
    * Blokcode  
31. Klik op OK.
32. Klik Tekenreeks toevoegen.
33. Typ Regels tellen in het veld Naam.
    * Regels tellen  
34. Klik op OK.
35. Klik Tekenreeks toevoegen.
36. Typ Totaalbedrag in het veld Naam.
    * Totaalbedrag  
37. Klik op OK.
38. Klik op het tabblad Toewijzing.
39. Selecteer in de structuur '$BlocksList'.
40. Klik op Binden.
    * Maak een overzichtsregel voor elk onthouden blok.  
41. Klik op het tabblad Indeling.
42. Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Blokcode'.
43. Klik op het tabblad Toewijzing.
44. Klik op Formule bewerken.
45. Typ in het veld Formule '"Blok-id: " & '.
    * "Blok-id: " &  
46. Vouw in de structuur '$BlocksList' uit.
47. Selecteer in de structuur '$BlocksList\Waarde'.
48. Klik op Gegevensbron toevoegen.
49. Klik op Opslaan.
50. Sluit de pagina.
51. Klik op het tabblad Indeling.
52. Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Regels tellen'.
53. Klik op het tabblad Toewijzing.
54. Klik op Formule bewerken.
    * Maak uitvoer voor het aantal regels voor elk blok dat in dit rapport wordt weergegeven.  
55. Typ in het Formuleveld '"Aantal regels in dit blok: " & '.
    * "Aantal regels in dit blok: " &  
56. Typ in het Formuleveld '"Aantal regels in dit blok: " & TEXT('.
    * "Aantal regels in dit blok: " & TEXT(  
57. Selecteer in de structuur 'Gegevenscollectiefuncties\COUNTIFS'.
58. Klik op Functie toevoegen.
59. Klik op Gegevensbron toevoegen.
60. Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '.
    * "Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName',  
61. Vouw in de structuur '$BlocksList' uit.
62. Selecteer in de structuur '$BlocksList\Waarde'.
63. Klik op Gegevensbron toevoegen.
64. Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', , '$BlocksList'.Value, '.
    * "Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Selecteer in de structuur '$RecName'.
66. Klik op Gegevensbron toevoegen.
67. Typ in het veld Formule '"Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', , '$BlocksList'.Value, '$RecName', "*"))'.
    * "Aantal regels in dit blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Klik op Opslaan.
69. Sluit de pagina.
70. Klik op het tabblad Indeling.
71. Selecteer in de structuur 'Intrastat\Gegevens\Totalen per blokken\Totaalbedrag'.
72. Klik op het tabblad Toewijzing.
73. Klik op Formule bewerken.
    * Maak uitvoer die het totaal is van het gefactureerde bedrag voor elk blok dat in dit rapport wordt weergegeven.  
74. Typ in het veld Formule '"Totaal factuurbedrag: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.
    * "Totaal factuurbedrag: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Klik op Opslaan.
76. Sluit de pagina.
77. Klik op Opslaan.
78. Sluit de pagina.

