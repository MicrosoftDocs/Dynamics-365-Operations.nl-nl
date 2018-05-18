--- 
title: "Gedeeltelijk locatieproces voor cyclustelling definiëren "
description: Wanneer u cyclustellingsplannen gebruikt om telwerk te maken, kunt u de werkelijke telbewerkingen leiden door aan te vragen dat alleen specifieke producten en productvarianten worden geteld in plaats van alle voorhanden voorraad op de locatie.
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 030f0f75d64c97f1109f36c9fd38283c2d1fa7b0
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="define-partial-location-cycle-counting-process"></a>Gedeeltelijk locatieproces voor cyclustelling definiëren  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Wanneer u cyclustellingsplannen gebruikt om telwerk te maken, kunt u de werkelijke telbewerkingen leiden door aan te vragen dat alleen specifieke producten en productvarianten worden geteld in plaats van alle voorhanden voorraad op de locatie. Door te filteren op specifieke producten kan de magazijnbeheerder de overhead voor controle helpen verminderen, fouten bij consolidatie vermijden en tijd besparen. Normaal gesproken voert een magazijnbeheerder de instellingstaken uit. U kunt deze procedure doorlopen in het demobedrijf USMF of in uw eigen gegevens.


## <a name="create-a-cycle-counting-work-template"></a>Een cyclustelwerksjabloon maken
1. Ga naar Magazijnbeheer > Instellingen > Werk > Werksjablonen.
2. Selecteer 'Cyclustelling' in het veld Werkordertype.
3. Klik op Nieuw.
4. Voer een getal in het veld Volgnummer in.
    * De sorteervolgorde is van het kleinste getal naar het grootste getal. De waarde moet groter zijn dan 0 (nul).  
5. Markeer in de lijst de geselecteerde rij.
6. Typ een waarde in het veld Werksjabloon.
7. Typ een waarde in het veld Omschrijving van werksjabloon.
8. Typ of selecteer een waarde in het veld Werkgroep-id.
9. Voer een getal in het veld Werkprioriteit in.
10. Klik op Opslaan.
11. Klik op Nieuw.
12. Markeer in de lijst de geselecteerde rij.
13. Selecteer 'Tellen' in het veld Werktype.
14. Typ of selecteer een waarde in het veld Werkklasse-id.
15. Klik op Opslaan.
16. Klik op Werkregelopsplitsingen.
17. Klik op Nieuw.
18. Voer een getal in het veld Volgnummer in.
    * De sorteervolgorde is van het kleinste getal naar het grootste getal. De waarde moet groter zijn dan 0 (nul).  
19. Klik op Opslaan.
20. Sluit de pagina.
21. Sluit de pagina.

## <a name="create-a-cycle-counting-plan"></a>Een cyclustellingsplan maken
1. Ga naar Magazijnbeheer > Instellingen > Cyclustelling > Cyclustelplannen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Id cyclustelplan.
4. Typ een waarde in het veld Omschrijving.
5. Voer een getal in het veld Maximumaantal cyclustellingen in.
6. Typ of selecteer een waarde in het veld Werksjabloon.
7. Klik op Nieuw.
8. Voer een getal in het veld Volgnummer in.
    * De sorteervolgorde is van het kleinste getal naar het grootste getal. De waarde moet groter zijn dan 0 (nul).  
9. Typ een waarde in het veld Omschrijving.
10. Klik op Opslaan.
11. Klik op Productquery definiëren.
12. Markeer in de lijst de geselecteerde rij.
13. Typ of selecteer een waarde in het veld Criteria.
14. Klik op OK.
15. Sluit de pagina.


