--- 
title: Boekingsprofielen voor vaste activa instellen
description: Deze taakbegeleiding stelt boekingsprofielen voor vaste activa in.
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a>Boekingsprofielen voor vaste activa instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding stelt boekingsprofielen voor vaste activa in.  Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.  De voorbeelden in de taakbegeleiding zijn voor een basisboekingsprofiel, hoewel de boekingsprofielen voor uw specifieke rekeningschema en financiële rapportagebehoeften moeten worden gemaakt.

1. Ga naar Vaste activa > Instellingen > Boekingsprofielen voor vaste activa.
2. Klik op Nieuw.
3. Typ een waarde in het veld Boekingsprofiel.
4. Typ een waarde in het veld Omschrijving.
    * U moet een boekingsprofiel maken voor elk type vaste-activatransactie dat u gebruikt bij het werken met vaste activa.  Deze taakbegeleiding start met het type Bijboekingstransactie.  
5. Klik op Toevoegen.
6. Typ of selecteer een waarde in het veld Boek.
    * Met het veld Groeperingen kunt u het boekingsprofiel definiëren tot de Tabel (één rekening ingesteld voor elk vast activum) of Groep (één rekening ingesteld voor elke vaste-activagroep).  Voor deze taakbegeleiding blijft de waarde op "Alle" ingesteld voor toepassing op alle vaste activa met het opgegeven boek.  
7. Geef in het veld Hoofdrekening de gewenste waarden op.
    * Voor bijboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.    
8. Selecteer in het veld Transactietype de optie Verwervingscorrectie.
    * Voor bijboekingscorrectietransacties worden dezelfde rekeningen als voor bijboekingstransacties gebruikt.  
9. Klik op Toevoegen.
10. Typ of selecteer een waarde in het veld Boek.
11. Geef in het veld Hoofdrekening de gewenste waarden op.
    * Voor bijboekingscorrecties kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.    
12. Selecteer Afschrijving in het veld Transactietype.
13. Klik op Toevoegen.
14. Typ of selecteer een waarde in het veld Boek.
15. Geef in het veld Hoofdrekening de gewenste waarden op.
16. Geef in het veld Tegenrekening de gewenste waarden op.
17. Selecteer Afschrijvingscorrectie in het veld Transactietype.
    * Voor afschrijvingscorrectietransacties worden dezelfde rekeningen als voor afschrijvingstransacties gebruikt.  
18. Klik op Toevoegen.
19. Typ of selecteer een waarde in het veld Boek.
20. Geef in het veld Hoofdrekening de gewenste waarden op.
21. Geef in het veld Tegenrekening de gewenste waarden op.
22. Selecteer Verkoop/afstoting in het veld Transactietype.
23. Klik op Toevoegen.
24. Typ of selecteer een waarde in het veld Boek.
25. Geef in het veld Hoofdrekening de gewenste waarden op.
    * Voor afboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.  
26. Selecteer Afstoting - uitval in het veld Transactietype.
    * We gebruiken dezelfde rekeningen voor Afstotingsverkoop en Afstotingsuitval.  
27. Klik op Toevoegen.
28. Typ of selecteer een waarde in het veld Boek.
29. Geef in het veld Hoofdrekening de gewenste waarden op.
    * Voor afboekingen kunt u een tegenrekening invoeren of niets zodat dit later wordt ingevuld voor de specifieke transactie.  
30. Vouw de sectie Afstoting uit.
    * U moet boekingsprofielen voor afboeking voor zowel verkoop als uitval instellen.  Wij zullen met de transacties van de afboekingsverkoop starten.  
31. Klik op Toevoegen.
32. Typ of selecteer een waarde in het veld Boek.
33. Selecteer Aanschafwaarde in het veld Waarde boeken.
    * De bijboekingswaarde geldt voor bijboekings- en bijboekingscorrectiewaarden voor alle jaren.  U kunt ook rekeningen voor deze transactietypen afzonderlijk definiëren.  
    * U kunt het afboekingsproces instellen om verschillende rekeningen te gebruiken die afhankelijk zijn van of de afboeking in winst of een verlies resulteert.  Ik stel het type verkoopwaarde in op Alle om dezelfde rekeningen voor alle typen afboekingen te gebruiken.  
34. Geef in het veld Hoofdrekening de gewenste waarden op.
35. Geef in het veld Tegenrekening de gewenste waarden op.
36. Klik op Toevoegen.
37. Typ of selecteer een waarde in het veld Boek.
    * Selecteer in het veld Waarde boeken de optie Afschrijving (voorgaande jaren).  
38. Geef in het veld Hoofdrekening de gewenste waarden op.
39. Geef in het veld Tegenrekening de gewenste waarden op.
40. Klik op Toevoegen.
41. Typ of selecteer een waarde in het veld Boek.
42. Selecteer in het veld Waarde boeken de optie Afschrijving (dit jaar).
43. Geef in het veld Hoofdrekening de gewenste waarden op.
44. Geef in het veld Tegenrekening de gewenste waarden op.
45. Klik op Toevoegen.
46. Typ of selecteer een waarde in het veld Boek.
47. Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (voorgaande jaren).
48. Geef in het veld Hoofdrekening de gewenste waarden op.
49. Geef in het veld Tegenrekening de gewenste waarden op.
50. Klik op Toevoegen.
51. Typ of selecteer een waarde in het veld Boek.
52. Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (dit jaar).
53. Geef in het veld Hoofdrekening de gewenste waarden op.
54. Geef in het veld Tegenrekening de gewenste waarden op.
55. Klik op Toevoegen.
56. Typ of selecteer een waarde in het veld Boek.
57. Selecteer Nettoboekwaarde in het veld Waarde boeken.
58. Geef in het veld Hoofdrekening de gewenste waarden op.
59. Geef in het veld Tegenrekening de gewenste waarden op.
60. Selecteer Uitval in het veld Verkoop of uitval.
61. Klik op Toevoegen.
62. Typ of selecteer een waarde in het veld Boek.
63. Selecteer Aanschafwaarde in het veld Waarde boeken.
64. Geef in het veld Hoofdrekening de gewenste waarden op.
65. Geef in het veld Tegenrekening de gewenste waarden op.
66. Klik op Toevoegen.
67. Typ of selecteer een waarde in het veld Boek.
    * Selecteer in het veld Waarde boeken de optie Afschrijving (voorgaande jaren).  
68. Geef in het veld Hoofdrekening de gewenste waarden op.
69. Geef in het veld Tegenrekening de gewenste waarden op.
70. Klik op Toevoegen.
71. Typ of selecteer een waarde in het veld Boek.
72. Selecteer in het veld Waarde boeken de optie Afschrijving (dit jaar).
73. Geef in het veld Hoofdrekening de gewenste waarden op.
74. Geef in het veld Tegenrekening de gewenste waarden op.
75. Klik op Toevoegen.
76. Typ of selecteer een waarde in het veld Boek.
77. Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (voorgaande jaren).
78. Geef in het veld Hoofdrekening de gewenste waarden op.
79. Geef in het veld Tegenrekening de gewenste waarden op.
80. Klik op Toevoegen.
81. Typ of selecteer een waarde in het veld Boek.
82. Selecteer in het veld Waarde boeken de optie Afschrijvingscorrecties (dit jaar).
83. Geef in het veld Hoofdrekening de gewenste waarden op.
84. Geef in het veld Tegenrekening de gewenste waarden op.
85. Klik op Toevoegen.
86. Typ of selecteer een waarde in het veld Boek.
87. Selecteer Nettoboekwaarde in het veld Waarde boeken.
88. Geef in het veld Hoofdrekening de gewenste waarden op.
89. Geef in het veld Tegenrekening de gewenste waarden op.


