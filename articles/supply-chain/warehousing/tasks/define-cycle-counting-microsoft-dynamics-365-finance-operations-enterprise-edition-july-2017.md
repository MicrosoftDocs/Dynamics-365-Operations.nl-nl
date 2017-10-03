--- 
title: "Cyclustelling definiëren "
description: Cyclustelling is een magazijnproces dat u kunt gebruiken om voorhanden voorraadartikelen te controleren.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f0d598bbd13406b27a23dcf349f6c81e758a9e61
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="define-cycle-counting"></a>Cyclustelling definiëren  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Cyclustelling is een magazijnproces dat u kunt gebruiken om voorhanden voorraadartikelen te controleren. Deze taakregistratie laat zien hoe u: de standaardprioriteit van telwerk instelt; een menuoptie voor mobiele apparaten inschakelt om zowel verzamel- als telbewerkingen te verwerken; een teldrempeltrigger inschakelt wanneer een locatie leeg raakt; een cyclustelplan inschakelt voor een specifiek artikel in een specifiek magazijn. Deze taken worden gewoonlijk uitgevoerd door een magazijnmanager. U kunt deze procedure doorlopen in het demobedrijf USMF of in uw eigen gegevens.


## <a name="set-the-priority-of-counting-work"></a>De prioriteit van telwerk instellen
1. Ga naar Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer.
2. Klik op het tabblad Cyclustelling.
3. Voer een getal in het veld Standaard werkprioriteit van cyclustelling in.
    * Deze stap wijzigt de prioriteit van cyclustelwerk vergeleken met andere soorten werk in het magazijn. Als u een nummer invoert dat lager is dan het nummer voor andere typen werk, verhoogt u de prioriteit van het cyclustelwerk.  
4. Klik op Opslaan.
5. Sluit de pagina.

## <a name="enable-the-mobile-device"></a>Het mobiel apparaat inschakelen
1. Ga naar Magazijnbeheer > Instellingen > Mobiel apparaat > Menuopties voor mobiel apparaat.
2. Klik op Nieuw.
3. Typ een waarde in het veld Menuoptie.
4. Typ een waarde in het veld Titel.
5. Selecteer 'Werk' in het veld Modus.
6. Stel de optie Bestaand werk gebruiken in op Ja.
    * Wanneer u deze optie instelt op Ja, zoekt het systeem naar bestaand werk wanneer de menuoptie van het mobiele apparaat wordt gebruikt.  
7. Selecteer 'Door systeem bestuurd' in het veld Bestuurd door.
    * Wanneer 'Door systeem bestuurd' is ingeschakeld, wordt de magazijnmedewerker doorgestuurd naar open werk in de gedefinieerde werkklassen. (We maken deze klassen vervolgens.)  
8. Vouw de sectie Werkklassen uit of samen.
    * Vervolgens maken we twee werkklassen die worden gebruikt met deze menuoptie voor een mobiel apparaat. Wanneer de menuoptie wordt gebruikt, worden query's op deze werkklassen uitgevoerd en wordt het werk met de hoogste prioriteit aan de gebruiker weergegeven.  
9. Klik op Nieuw.
10. Selecteer een waarde in het veld Werkklasse-id.
11. Klik op Nieuw.
12. Selecteer een waarde in het veld Werkklasse-id.
13. Klik op Opslaan.
14. Sluit de pagina.
15. Ga naar Magazijnbeheer > Instellingen > Mobiel apparaat > Menu voor mobiel apparaat.
16. Zoek en selecteer de gewenste record in de lijst.
17. Selecteer in de structuur 'de menuoptie die u zojuist hebt gemaakt'.
18. Klik op Bewerken.
19. Klik op de pijl om de menuoptie aan het menu toe te voegen.
20. Klik op Opslaan.

## <a name="create-a-counting-threshold"></a>Een teldrempel maken
1. Ga naar Magazijnbeheer > Instellingen > Cyclustelling > Drempels voor cyclustelling.
2. Klik op Nieuw.
3. Typ een waarde in het veld Id cyclustellingsdrempel.
4. Stel de optie Cyclustellingsplan onmiddellijk verwerken in op Ja.
5. Typ een waarde in het veld Omschrijving.
6. Klik op Opslaan.
7. Klik op Locaties selecteren.
8. Markeer in de lijst de geselecteerde rij.
9. Selecteer een waarde in het veld Criteria.
10. Klik op OK.
11. Sluit de pagina.

## <a name="create-a-cycle-count-plan"></a>Een cyclustelplan maken
1. Ga naar Magazijnbeheer > Instellingen > Cyclustelling > Cyclustelplannen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Id cyclustelplan.
4. Typ een waarde in het veld Omschrijving.
5. Voer een getal in het veld Maximumaantal cyclustellingen in.
6. Klik op Opslaan.
7. Klik op Locaties selecteren.
8. Markeer in de lijst de geselecteerde rij.
9. Selecteer een waarde in het veld Criteria.
10. Klik op OK.
11. Voer een getal in het veld Dagen tussen cyclustellingen in.
    * Als de waarde die is opgegeven in het veld Dagen bijvoorbeeld 5 is, wordt om de vijf dagen cyclustellingswerk gemaakt. Als cyclustellingswerk echter op dag drie wordt verwerkt, wordt het volgende cyclustellingswerk gecreëerd vijf dagen nadat de laatste cyclustelling werd verwerkt, op dag acht.  
12. Klik op Opslaan.
13. Klik op Nieuw.
14. Voer een getal in het veld Volgnummer in.
    * De sorteervolgorde is van het kleinste getal naar het grootste getal. De waarde moet groter zijn dan 0 (nul).  
15. Markeer in de lijst de geselecteerde rij.
16. Typ een waarde in het veld Omschrijving.
17. Klik op Opslaan.
18. Klik op Productquery definiëren.
19. Markeer in de lijst de geselecteerde rij.
20. Typ of selecteer een waarde in het veld Criteria.
21. Klik op OK.
22. Sluit de pagina.

