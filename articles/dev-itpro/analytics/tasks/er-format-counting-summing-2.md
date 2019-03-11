---
title: 'ER Indeling configureren voor tellen en totaliseren (deel 2: Berekeningen configureren)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ef657b13bc1f7f4a84676821e4175ace32c069a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "338907"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a>ER Indeling configureren voor tellen en totaliseren (deel 2: Berekeningen configureren)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van Systeembeheerder of Ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken voor tellen en totaliseren op basis van gegevens van de reeds gegenereerde tekstuitvoer. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Indeling configureren voor tellen en totaliseren (Deel 1: Indeling maken)".

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Maak een indelingsconfiguratie om tellen en totaliseren van details toe te voegen
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Rapportconfiguraties.
3. Vouw in de structuur 'Intrastat-model' uit.
4. Selecteer in de structuur 'Intrastat-model\Intrastat (DE)'.
    * Stel dat u de indeling moet aanpassen die door Microsoft wordt geleverd door regels met overzichtdetails toe te voegen aan het einde van het Intrastat-rapport. U moet dat doen door een eigen exemplaar van de Intrastat-configuratie af te leiden uit het Microsoft-exemplaar om wijzigingen aan te brengen.  
5. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
6. Typ in het veld Nieuw 'Afleiden van naam: Intrastat (DE), Microsoft'.
7. Typ 'Intrastat (DE) met tellen en totaliseren' in het veld Naam.
8. Klik op Configuratie maken.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Configureer dit rapport om tellen en totaliseren uit te voeren op basis van uitvoerdetails
1. Klik op Ontwerper.
2. Selecteer Ja in de veld Uitvoerdetails verzamelen.
    * Deze markering activeert in runtime het proces van het verzamelen van uitvoerdetails voor het genereren van het Intrastat-bestand.  
    * U moet tellen voor verschillende Intrastat-richtingen, dus voeg een specifieke modelopsomming toe aan de lijst met gegevensbronnen van deze indelingsconfiguratie.  
3. Klik op het tabblad Toewijzing.
4. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
5. Selecteer in de structuur Gegevensmodel\Opsomming.
6. Typ Richting in het veld Naam.
7. Typ of selecteer een waarde in het veld Modelopsomming.
    * Selecteer de waarde Richting.  
8. Klik op OK.
9. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
10. Selecteer "Functions\Calculated field" in de structuur.
11. Typ '$BlockName' in het veld Naam
12. Klik op Formule bewerken.
13. Typ 'blok' in het veld Formule.
14. Klik op Opslaan.
15. Sluit de pagina.
16. Klik op OK.
17. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
18. Selecteer "Functions\Calculated field" in de structuur.
19. Typ '$RecName' in het veld Naam.
20. Klik op Formule bewerken.
21. Typ 'record' in het veld Formule.
22. Klik op Opslaan.
23. Sluit de pagina.
24. Klik op OK.
25. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
26. Selecteer "Functions\Calculated field" in de structuur.
27. Typ '$InvName' in het veld Naam.
28. Klik op Formule bewerken.
29. Typ 'InvoicedAmountEUR' in het veld Formule.
30. Klik op Opslaan.
31. Sluit de pagina.
32. Klik op OK.
33. Selecteer Intrastat\Gegevens in de structuur.
34. Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens
35. Klik op Gegevensbron toevoegen.
    * $BlockName  
36. Klik op Opslaan.
37. Sluit de pagina.
38. Klik op de knop Bewerken voor het veld Sleutelwaarde verzamelde gegevens
39. Typ in het veld Formule 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Klik op Opslaan.
41. Sluit de pagina.
    * Tel de regels van deze reeks. De resultaten worden afzonderlijk voor verschillende richtingen gebruikt met de naam 'blok'. De waarde Importeren wordt gebruikt voor Intrastat-transacties voor ontvangsten. De waarde Exporteren wordt gebruikt voor Intrastat-transacties voor verzendingen. Beschouw dit als een virtueel Excel-spreadsheet. Voor elke transactie een rij waarin de eerste kolom 'blok' is ingevuld met de waarden 'Import' en 'Export'.  
42. Vouw in de structuur 'Intrastat\Gegevens: Reeks' uit.
43. Selecteer in de structuur 'Intrastat\Gegevens: Reeks\Ontvangsten?'.
44. Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens.
    * Tel de regels van deze reeks. De resultaten worden onthouden met de naam 'record'.  
45. Selecteer in de structuur '$RecName'.
46. Klik op Gegevensbron toevoegen.
47. Klik op Opslaan.
48. Sluit de pagina.
49. Klik op de knop Bewerken voor het veld Sleutelwaarde verzamelde gegevens.
50. Typ in het veld Formule 'Intrastat.CommodityRecord.CommodityCode'.
51. Klik op Opslaan.
52. Sluit de pagina.
    * Tel de regels van deze reeks. De resultaten worden afzonderlijk voor verschillende basisproductcode gebruikt met de naam 'record'. Beschouw dit als een virtueel Excel-spreadsheet. Voor elke transactie een rij waarin de eerste kolom 'blok' wordt gevuld met de waarden 'Import' en 'Export' en het tweede blok 'record' wordt gevuld met de waarde van de basisproductcode.  
53. Select in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen?'.
54. Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens
55. Selecteer in de structuur '$RecName'.
56. Klik op Gegevensbron toevoegen.
57. Klik op Opslaan.
58. Sluit de pagina.
59. Klik op de knop Bewerken voor het veld Sleutelwaarde verzamelde gegevens.
60. Typ in het veld Formule 'Intrastat.CommodityRecord.CommodityCode'.
61. Klik op Opslaan.
62. Sluit de pagina.
63. Vouw in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen: Reeks' uit.
64. Vouw in de structuur 'Intrastat\Gegevens: Reeks\Verzendingen: Reeks?\Record =  Intrastat.CommodityRecord' uit.
65. Klik op het tabblad Indeling.
66. Selecteer in de structuur 'Intrastat\Gegevens\Verzendingen\Record\Factuurbedrag EUR'.
67. Klik op het tabblad Toewijzing.
68. Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens.
69. Selecteer in de structuur '$InvName'.
70. Klik op Gegevensbron toevoegen.
71. Klik op Opslaan.
72. Sluit de pagina.
    * Vat de gefactureerde bedragwaarden samen voor regels van deze reeks. De resultaten worden afzonderlijk voor verschillende intrastat-richtingen en basisproductcodes gebruikt met de naam "InvoicedAmountEUR". Beschouw dit als een virtueel gemaakt item in het Excel-spreadsheet. Voor elke transactie een rij waarin de eerste kolom 'blok' is ingevuld met de waarden 'Import' en 'Export'. Het tweede blok 'record' wordt gevuld met de waarde van de basisproductcode, en de derde kolom InvoicedAmountEUR wordt gevuld met de factuurbedragwaarde.  
73. Vouw in de structuur 'Intrastat\Gegevens\Ontvangsten?' uit.
74. Vouw in de structuur 'Intrastat\Gegevens\Ontvangsten?\Record = Intrastat.CommodityRecord' uit.
75. Klik op het tabblad Indeling.
76. Selecteer in de structuur 'Intrastat\Gegevens\Ontvangsten\Record\Factuurbedrag EUR'.
77. Klik op het tabblad Toewijzing.
78. Klik op de knop Bewerken voor het veld Sleutelnaam verzamelde gegevens.
79. Selecteer in de structuur '$InvName'.
80. Klik op Gegevensbron toevoegen.
81. Klik op Opslaan.
82. Sluit de pagina.
83. Klik op Opslaan.
84. Sluit de pagina.

