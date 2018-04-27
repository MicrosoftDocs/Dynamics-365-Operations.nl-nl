--- 
title: "Auditbeleid voor brondocumenten definiëren"
description: Deze procedure laat zien hoe u controlebeleidsregels instelt en uitvoert.
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a>Auditbeleid voor brondocumenten definiëren

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u controlebeleidsregels instelt en uitvoert. Het voorbeeld gebruikt onkostennota's met het type hotelkosten. Bij deze procedure wordt het demobedrijf USMF gebruikt. De auditorrol bevat de juiste machtigingen om deze taken uit te voeren.

1. Ga naar Controlewerkbank > Instellen > Type beleidsregel.
2. Klik op Nieuw.
3. Typ een waarde in het veld Regelnaam.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer Onkostennotaregel in het veld Querynaam.
6. Selecteer Samenvoegen in het veld Querytype.
7. Selecteer Rechtspersoon in het veld Rechtspersoon
8. Selecteer Wijzigingsdatum en -tijd in het veld Referentie documentdatum
9. Klik op Opslaan.
10. Ga naar Controlewerkbank > Instellen > Controlebeleid.
11. Klik op Nieuw.
12. Typ een waarde in het veld Naam.
13. Vouw de sectie Beleidorganisaties uit.
14. In de structuur selecteert u "Contoso-entertainmentsysteem USA".
15. Klik op Toevoegen.
16. In de structuur selecteert u "Contoso Consulting USA".
17. Klik op Toevoegen.
18. In de structuur selecteert u "Contoso Retail USA".
19. Klik op Toevoegen.
20. Vouw de sectie Beleidorganisaties samen.
21. Vouw de sectie Beleidsregels uit.
22. Zoek en selecteer in de lijst de Beleidsregel die eerder is gemaakt.
23. Klik op Beleidsregel maken.
24. Typ in het veld Begindatum de datum en een tijd.
25. Klik op Filter.
26. Selecteer in de lijst de rij voor Onkostencategorie, en stel de details in op Hotel
27. Typ of selecteer een waarde in het veld Criteria.
28. Klik op het tabblad Samenvoegen.
29. Klik op Toevoegen.
30. Selecteer in de lijst een veldwaarde Transactiebedrag
31. Typ of selecteer een waarde in het veld Veld.
32. Selecteer Som in het veld AggregateFunction.
33. Klik op het tabblad Groeperen op.
34. Klik op Toevoegen.
35. Selecteer een waarde van Werknemer in de lijst  
36. Klik op Toevoegen.
37. Selecteer een waarde van Onkostencategorie in de lijst
38. Typ of selecteer een waarde in het veld Veld.
39. Klik op het tabblad Met.
40. Klik op Toevoegen.
41. Selecteer Transactiebedrag
42. Typ of selecteer een waarde in het veld Veld.
43. Selecteer Som in het veld AggregateFunction.
44. Typ ´> 2000´ in het veld Criteria.
45. Klik op OK.
46. Klik op Testen.
47. Voer in het veld Begindatum documentselectie een datum en tijd in.
48. Voer in het veld Einddatum documentselectie een datum en tijd in.
49. Klik op Test uitvoeren.
50. Klik in het actievenster op Controlebeleid.
51. Klik op Extra opties.
52. Typ in het veld Begindatum de datum en een tijd.
53. Typ in het veld Einddatum de datum en een tijd.
54. Klik op Batch.
55. Vouw de sectie Op de achtergrond uitvoeren uit.
56. Selecteer Ja in het veld Batchverwerking.
57. Klik op OK.
58. Ga naar Controlewerkbank > Controlecases.
59. Zoek en selecteer de gewenste record in de lijst.
60. Klik in de lijst op de koppeling in de geselecteerde rij.
61. Vouw de sectie Koppelingen uit.
62. Zoek en selecteer de gewenste record in de lijst.
63. Klik in de lijst op de koppeling in de geselecteerde rij.


