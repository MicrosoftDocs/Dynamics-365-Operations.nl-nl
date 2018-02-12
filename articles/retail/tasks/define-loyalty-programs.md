--- 
title: " Loyaliteitsprogramma's definiëren"
description: Deze procedure laat zien hoe u een loyaliteitsprogramma instelt met twee loyaliteitsniveaus.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 4bc90da445765ab662fe920a3230681959469a90
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---
# <a name="define-loyalty-programs"></a> Loyaliteitsprogramma's definiëren

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een loyaliteitsprogramma instelt met twee loyaliteitsniveaus. Deze procedure gebruikt het demobedrijf USRT.

1. G naar Detailhandel en commerce > .. > Loyaliteitsprogramma's.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Regel toevoegen.
6. Voer een nummer in het veld Niveau in.
7. Voer in het veld Niveau een naam in voor het loyaliteitsniveau.
8. Typ een waarde in het veld Omschrijving.
9. Klik in het veld Datuminterval op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Dit datuminterval moet doorlopen in de toekomst. Als het datuminterval dat is geselecteerd voor het gouden niveau bijvoorbeeld een periode van één jaar is, kan elke klant die in aanmerking komt voor het gouden niveau gedurende een jaar de beloningen ontvangen die aan het gouden niveau zijn toegewezen. Als de klant opnieuw in aanmerking komt voor het gouden niveau terwijl ze op dat niveau zitten, wordt de datum waarop het niveau vervalt, verlengd met nog een jaar, te beginnen vanaf de datum waarop ze opnieuw in aanmerking komen.  
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Klik op Regel toevoegen.
12. Voer een nummer in het veld Niveau in.
13. Voer in het veld Niveau een naam in voor het loyaliteitsniveau.
14. Typ een waarde in het veld Omschrijving.
15. Klik in het veld Datuminterval op de vervolgkeuzeknop om de zoekopdracht te openen.
16. Klik in de lijst op de koppeling in de geselecteerde rij.
17. Klik op Opslaan.
18. Zoek en selecteer de gewenste record in de lijst.
    * De niveauregels definiëren het minimumaantal dat van een beloningspunt nodig is tijdens een periode om in aanmerking te komen voor het niveau.  
19. Schakel de uitbreiding van de sectie Niveauregels om.
20. Klik op Nieuw.
    * U kunt meer dan één niveauregel per niveau hebben. U kunt bijvoorbeeld drie verschillende criteria hebben om een niveau te behalen; door $ 500 in een maand uit te geven, door $ 1000 in een jaar uit te geven en door 20 transacties in een jaar te hebben. Om dit te doen moet u drie niveauregels maken.  
21. Klik in het veld Beloningspunt op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Dit moet een niet-inwisselbaar loyaliteitsbeloningspunt zijn.  
22. Klik in de lijst op de koppeling in de geselecteerde rij.
23. Voer in het veld Minimaal uitgegeven punten een getal in.
    * Als voor het laagste niveau alle klanten in aanmerking komen door gewoon deel te nemen aan het programma, voert u '0' in.  
24. Klik in het veld Evaluatie datuminterval op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Dit datuminterval moet doorlopen in het verleden. Alleen punten die tijdens dit datuminterval zijn behaald, worden meegeteld voor het bereiken van de minimale uitgegeven puntenwaarde.  
25. Klik in de lijst op de koppeling in de geselecteerde rij.
26. Klik op Opslaan.
27. Zoek en selecteer de gewenste record in de lijst.
28. Klik op Nieuw.
29. Klik in het veld Beloningspunt op de vervolgkeuzeknop om de zoekopdracht te openen.
30. Klik in de lijst op de koppeling in de geselecteerde rij.
31. Voer in het veld Minimaal uitgegeven punten een getal in.
32. Klik in het veld Evaluatie datuminterval op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Dit datuminterval moet doorlopen in het verleden.  
33. Klik in de lijst op de koppeling in de geselecteerde rij.
34. Klik op Opslaan.
35. Klik op Prijsgroepen.
    * Als u loyaliteitsklanten kortingen wilt geven, moet u een of meer prijsgroepen aan het loyaliteitsprogramma toewijzen en de prijsgroepen aan kortingen toewijzen. Het is een best practice prijsgroepen niet te mengen over verschillende typen kortingsentiteiten.  Gebruik bijvoorbeeld niet dezelfde prijsgroep voor een loyaliteitskorting en een kanaalkorting.  
36. Klik in het veld Prijsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De koppeling Prijsgroepen boven aan de pagina is voor het loyaliteitsprogramma. De koppeling Prijsgroepen op het sneltabblad Programmalagen is alleen bedoeld voor een specifiek loyaliteitsniveau.  
37. Klik in de lijst op de koppeling in de geselecteerde rij.
38. Klik op Opslaan.
39. Sluit de pagina.
40. Klik op Opslaan.


