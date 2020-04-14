---
title: Boekingsprofielen voor vaste activa instellen
description: Deze taakbegeleiding stelt boekingsprofielen voor vaste activa in.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07961d8613b6b5e0e1c5dc6a91b554305dcb17f5
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138156"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>Boekingsprofielen voor vaste activa instellen

[!include [banner](../../includes/banner.md)]

Deze taakbegeleiding stelt boekingsprofielen voor vaste activa in.  Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.  De voorbeelden in de taakbegeleiding zijn voor een basisboekingsprofiel, hoewel de boekingsprofielen voor uw specifieke rekeningschema en financiële rapportagebehoeften moeten worden gemaakt.

1. Ga in het navigatievenster naar **Modules > Vaste activa > Instellen > Boekingsprofielen vaste activa**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Boekingsprofiel**.
4. Typ een waarde in het veld **Beschrijving**. U moet een boekingsprofiel maken voor elk type vaste-activatransactie dat u gebruikt bij het werken met vaste activa. Deze taakbegeleiding start met het type Verwervingstransactie.  
5. Klik in de werkbalk op **Toevoegen**.
6. Typ of selecteer een waarde in het veld **Boek**. Met het veld **Groeperingen** kunt u het boekingsprofiel definiëren tot de Tabel (één rekening ingesteld voor elk vast activum) of Groep (één rekening ingesteld voor elke vaste-activagroep). Voor deze taakbegeleider laat u de waarde staan op Alle, om het toe te passen op alle vaste activa met het opgegeven boek.  
7. Geef in het veld **Hoofdrekening** de gewenste waarden op. Voor verwervingen kunt u een tegenrekening invoeren. U kunt het veld ook leeg laten, zodat dit later wordt ingevuld voor de specifieke transactie.    
8. Selecteer in het vervolgkeuzemenu op het sneltabblad **Grootboekrekeningen** de optie Verwervingscorrectie. Voor verwervingscorrectietransacties worden dezelfde rekeningen als voor verwervingstransacties gebruikt.  
9. Klik op **Toevoegen**.
10. Typ of selecteer een waarde in het veld **Boek**.
11. Geef in het veld **Hoofdrekening** de gewenste waarden op. Voor verwervingscorrecties kunt u een tegenrekening invoeren. U kunt het veld ook leeg laten, zodat dit later wordt ingevuld voor de specifieke transactie.    
12. Selecteer in het vervolgkeuzemenu op het sneltabblad **Grootboekrekeningen** de optie Afschrijving.
13. Klik op **Toevoegen**.
14. Typ of selecteer een waarde in het veld **Boek**.
15. Geef in het veld **Hoofdrekening** de gewenste waarden op.
16. Geef in het veld **Tegenrekening** de gewenste waarden op.
17. Selecteer in het vervolgkeuzemenu op het sneltabblad **Grootboekrekeningen** de optie Afschrijvingscorrectie. Voor afschrijvingscorrectietransacties worden dezelfde rekeningen gebruikt als voor afschrijvingstransacties.  
18. Klik op **Toevoegen**.
19. Typ of selecteer een waarde in het veld **Boek**.
20. Geef in het veld **Hoofdrekening** de gewenste waarden op.
21. Geef in het veld **Tegenrekening** de gewenste waarden op.
22. Selecteer in het vervolgkeuzemenu op het sneltabblad **Grootboekrekeningen** de optie Afstoting/verkoop.
23. Klik op **Toevoegen**.
24. Typ of selecteer een waarde in het veld **Boek**.
25. Geef in het veld **Hoofdrekening** de gewenste waarden op. Voor afstotingen kunt u een tegenrekening invoeren. U kunt het veld ook leeg laten, zodat dit later wordt ingevuld voor de specifieke transactie.  
26. Selecteer in het vervolgkeuzemenu op het sneltabblad **Grootboekrekeningen** de optie Afstoting/uitval. Gebruik dezelfde rekeningen voor Afstotingsverkoop en Afstotingsuitval.  
27. Klik op **Toevoegen**.
28. Typ of selecteer een waarde in het veld **Boek**.
29. Geef in het veld **Hoofdrekening** de gewenste waarden op. Voor afstotingen kunt u een tegenrekening invoeren. U kunt het veld ook leeg laten, zodat dit later wordt ingevuld voor de specifieke transactie.  
30. Vouw het sneltabblad **Afstoting** uit. U moet boekingsprofielen voor afboeking voor zowel verkoop als uitval instellen.  Wij zullen met de transacties van de afboekingsverkoop starten.  
31. Klik op **Toevoegen**.
32. Typ of selecteer een waarde in het veld **Boek**.
33. Selecteer Verwervingswaarde in het veld **Waarde boeken**.
    * De verwervingswaarde geldt voor verwervings- en verwervingscorrectiewaarden voor alle jaren. U kunt ook rekeningen voor deze transactietypen afzonderlijk definiëren.  
    * U kunt het afboekingsproces instellen om verschillende rekeningen te gebruiken die afhankelijk zijn van of de afboeking in winst of een verlies resulteert. Ik stel het type verkoopwaarde in op Alle om dezelfde rekeningen voor alle typen afboekingen te gebruiken.  
34. Geef in het veld **Hoofdrekening** de gewenste waarden op.
35. Geef in het veld **Tegenrekening** de gewenste waarden op.
36. Klik op **Toevoegen**.
37. Typ of selecteer een waarde in het veld **Boek**.
38. Selecteer in het veld **Waarde boeken** de optie Afschrijving (voorgaande jaren).  
38. Geef in het veld **Hoofdrekening** de gewenste waarden op.
39. Geef in het veld **Tegenrekening** de gewenste waarden op.
40. Klik op **Toevoegen**.
41. Typ of selecteer een waarde in het veld **Boek**.
42. Selecteer in het veld **Waarde boeken** de optie Afschrijving (dit jaar).
43. Geef in het veld **Hoofdrekening** de gewenste waarden op.
44. Geef in het veld **Tegenrekening** de gewenste waarden op.
45. Klik op **Toevoegen**.
46. Typ of selecteer een waarde in het veld **Boek**.
47. Selecteer in het veld **Waarde boeken** de optie Afschrijvingscorrecties (voorgaande jaren).
48. Geef in het veld **Hoofdrekening** de gewenste waarden op.
49. Geef in het veld **Tegenrekening** de gewenste waarden op.
50. Klik op **Toevoegen**.
51. Typ of selecteer een waarde in het veld **Boek**.
52. Selecteer in het veld **Waarde boeken** de optie Afschrijvingscorrecties (dit jaar).
53. Geef in het veld **Hoofdrekening** de gewenste waarden op.
54. Geef in het veld **Tegenrekening** de gewenste waarden op.
55. Klik op **Toevoegen**.
56. Typ of selecteer een waarde in het veld **Boek**.
57. Selecteer in het veld **Waarde boeken** de optie Nettoboekwaarde.
58. Geef in het veld **Hoofdrekening** de gewenste waarden op.
59. Geef in het veld **Tegenrekening** de gewenste waarden op.
60. Selecteer in het veld **Verkoop of uitval** de optie Uitval.
61. Klik op **Toevoegen**.
62. Typ of selecteer een waarde in het veld **Boek**.
63. Selecteer Verwervingswaarde in het veld **Waarde boeken**.
64. Geef in het veld **Hoofdrekening** de gewenste waarden op.
65. Geef in het veld **Tegenrekening** de gewenste waarden op.
66. Klik op **Toevoegen**.
67. Typ of selecteer een waarde in het veld **Boek**.
67. Selecteer in het veld **Waarde boeken** de optie Afschrijving (voorgaande jaren).  
68. Geef in het veld **Hoofdrekening** de gewenste waarden op.
69. Geef in het veld **Tegenrekening** de gewenste waarden op.
70. Klik op **Toevoegen**.
71. Typ of selecteer een waarde in het veld **Boek**.
72. Selecteer in het veld **Waarde boeken** de optie Afschrijving (dit jaar).
73. Geef in het veld **Hoofdrekening** de gewenste waarden op.
74. Geef in het veld **Tegenrekening** de gewenste waarden op.
75. Klik op **Toevoegen**.
76. Typ of selecteer een waarde in het veld **Boek**.
77. Selecteer in het veld **Waarde boeken** de optie Afschrijvingscorrecties (voorgaande jaren).
78. Geef in het veld **Hoofdrekening** de gewenste waarden op.
79. Geef in het veld **Tegenrekening** de gewenste waarden op.
80. Klik op **Toevoegen**.
81. Typ of selecteer een waarde in het veld **Boek**.
82. Selecteer in het veld **Waarde boeken** de optie Afschrijvingscorrecties (dit jaar).
83. Geef in het veld **Hoofdrekening** de gewenste waarden op.
84. Geef in het veld **Tegenrekening** de gewenste waarden op.
85. Klik op **Toevoegen**.
86. Typ of selecteer een waarde in het veld **Boek**.
87. Selecteer in het veld **Waarde boeken** de optie Nettoboekwaarde.
88. Geef in het veld **Hoofdrekening** de gewenste waarden op.
89. Geef in het veld **Tegenrekening** de gewenste waarden op.

