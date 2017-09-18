--- 
title: "Gegevensmodel ontwerpen voor gebruik van financiële dimensies als gegevensbron voor elektronische aangifte (ER)"
description: "In de volgende stappen wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 35cfeb2220d615e5c9096d524d3deb10a4299f0e
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Gegevensmodel ontwerpen voor gebruik van financiële dimensies als gegevensbron voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan configureren om financiële dimensies te gebruiken als bron voor ER-rapporten. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.


## <a name="create-a-new-data-model"></a>Een nieuw gegevensmodel maken
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Zorg ervoor dat de leverancier 'Litware, Inc.' beschikbaar is en als actief gemarkeerd.  
2. Klik op Rapportconfiguraties.
3. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
4. Typ Voorbeeldmodel Financiële dimensies in het veld Naam.
5. Klik op Configuratie maken.
6. Klik op Ontwerper.
7. Klik op Nieuw om het verwijderdialoogvenster te openen.
8. Typ Invoer in het veld Naam.
9. Klik op Toevoegen.
10. Klik op Nieuw om het verwijderdialoogvenster te openen.
11. Typ "Bedrijf" in het veld Naam.
12. Klik op Toevoegen.
    * Er wordt aan het model een nieuwe recordlijst toegevoegd. Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de instellingen van de geselecteerde financiële dimensies. Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de instelling van de dimensie weergeven.  
13. Klik op Nieuw om het verwijderdialoogvenster te openen.
14. Typ Dimensie-instelling in het veld Naam.
15. Selecteer "Record list" in het veld Artikeltype.
16. Klik op Toevoegen.
17. Klik op Nieuw om het verwijderdialoogvenster te openen.
18. Typ Code in het veld Naam.
19. Selecteer "String" in het veld Artikeltype.
20. Klik op Toevoegen.
21. Klik op Nieuw om het verwijderdialoogvenster te openen.
22. Typ "Name" in het veld Naam.
23. Klik op Toevoegen.
24. Selecteer Invoer in de structuur.
25. Klik op Nieuw om het verwijderdialoogvenster te openen.
26. Typ Journaal in het veld Naam.
27. Selecteer "Record list" in het veld Artikeltype.
28. Klik op Toevoegen.
29. Klik op Nieuw om het verwijderdialoogvenster te openen.
30. Typ Batch in het veld Naam.
31. Selecteer "String" in het veld Artikeltype.
32. Klik op Toevoegen.
33. Klik op Nieuw om het verwijderdialoogvenster te openen.
34. Typ Transactie in het veld Naam.
35. Selecteer "Record list" in het veld Artikeltype.
36. Klik op Toevoegen.
37. Klik op Nieuw om het verwijderdialoogvenster te openen.
38. Typ Datum in het veld Naam.
39. Selecteer "Date" in het veld Artikeltype.
40. Klik op Toevoegen.
41. Klik op Nieuw om het verwijderdialoogvenster te openen.
42. Typ Debet in het veld Naam.
43. Selecteer "Real" in het veld Artikeltype.
44. Klik op Toevoegen.
45. Klik op Nieuw om het verwijderdialoogvenster te openen.
46. Typ Credit in het veld Naam.
47. Klik op Toevoegen.
48. Klik op Nieuw om het verwijderdialoogvenster te openen.
49. Typ "Currency" in het veld Naam.
50. Selecteer "String" in het veld Artikeltype.
51. Klik op Toevoegen.
52. Klik op Nieuw om het verwijderdialoogvenster te openen.
53. Typ Voucher in het veld Naam.
54. Klik op Toevoegen.
55. Klik op Nieuw om het verwijderdialoogvenster te openen.
56. Typ Dimensiegegevens in het veld Naam.
57. Selecteer "Record list" in het veld Artikeltype.
58. Klik op Toevoegen.
    * Er is aan het model een nieuwe recordlijst toegevoegd. Deze lijst bevat (voor ER-rapporten die dit model gebruiken als gegevensbron) de waarden van de geselecteerde financiële dimensies. Elke financiële dimensie wordt in deze lijst voorgesteld als een record met toepasselijke velden die de waarden van de dimensie weergeven. De dimensienaam wordt ook in dit record weergegeven als een veld dat, indien nodig, voor selectiedoeleinden wordt gebruikt.  
59. Klik op Nieuw om het verwijderdialoogvenster te openen.
60. Typ Code in het veld Naam.
61. Selecteer "String" in het veld Artikeltype.
62. Klik op Toevoegen.
63. Klik op Nieuw om het verwijderdialoogvenster te openen.
64. Typ "Description" in het veld Naam.
65. Klik op Toevoegen.
66. Klik op Nieuw om het verwijderdialoogvenster te openen.
67. Typ "Name" in het veld Naam.
68. Klik op Toevoegen.
69. Klik op Opslaan.
70. Sluit de pagina.

