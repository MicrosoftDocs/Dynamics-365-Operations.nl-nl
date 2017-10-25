--- 
title: " Loyaliteitsschema's definiëren"
description: Deze procedure laat zien hoe u een loyaliteitsschema definieert.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 23c8876b1983d6bc20b68f24fa7cd5b042cfd488
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="define-loyalty-schemes"></a> Loyaliteitsschema's definiëren

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een loyaliteitsschema definieert. Loyaliteitsschema's zijn regels voor het verdienen en inwisselen van beloningen voor een loyaliteitsprogramma. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Detailhandel en commerce > Klanten > Loyaliteit > Loyaliteitsschema's.
2. Klik op Nieuw.
3. Typ een waarde in het veld Schema-id.
4. Typ een waarde in het veld Omschrijving.
5. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
    * U kunt meerdere loyaliteitsschema's voor een loyaliteitsprogramma hebben. Loyaliteitsschema's kunnen voor alle kanalen zijn of alleen voor een subset van kanalen.  
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik op Opslaan.
9. Klik op Regel toevoegen.
10. Selecteer een optie in het veld Activiteitstype.
    * Selecteer Inkoopproducten per bedrag als u wilt dat klanten beloningen verdienen op basis van hoeveel ze uitgeven. Selecteer Inkoopproducten per hoeveelheid als u wilt dat klanten beloningen verdienen op basis van hoeveel producten ze kopen.  Selecteer Aantal verkooptransacties om beloningen te verdienen voor elke verkooptransactie, ongeacht wat en hoeveel er wordt gekocht.  
    * Een categorie selecteren. De categorie beperkt op welke producten deze verdienregel van toepassing is.  
    * Als u wilt dat de verdienregel van toepassing is op alle producten, laat u dit veld leeg.  
11. Voer een getal in het veld Activiteitbedrag/hoeveelheid in.
    *  Voor het activiteitstype Aantal verkooptransacties moet u altijd de waarde '1.0' gebruiken. Voor de activiteitstypen Inkoopproducten per bedrag en Inkoopproducten per hoeveelheid activeert elke transactie die kleiner is dan de ingevoerde waarde, de verdienregel niet. Als het activiteittype bijvoorbeeld Inkoopproducten per bedrag is en u '10,00' invoert, verdient een verkooptransactie voor '9.00' geen beloningen voor deze verdienregel.  
12. Typ een waarde in het veld Activiteitvaluta.
13. Klik in het veld Beloningspunt-id op de vervolgkeuzeknop om de zoekopdracht te openen.
14. Klik in de lijst op de koppeling in de geselecteerde rij.
15. Voer in het veld Beloningspunten een getal in.
    * Voor beloningspunten van het type bedrag worden verdiende hoeveelheden met decimalen vastgelegd. Als de verdienregel bijvoorbeeld zegt dat er 1 beloningspunt wordt verdiend voor elke 1 uitgegeven euro, en de klant 1,25 euro besteedt, verdient de klant 1,25 beloningspunten. Voor beloningspunten van het type hoeveelheid worden verdiende hoeveelheden in gehele getallen vastgelegd. In het voorbeeld waarin de verdienregel zegt dat er 1 beloningspunt wordt verdiend voor elke 1 uitgegeven euro, en de klant 1,25 euro besteedt, verdient de klant 1,0 beloningspunten.  
16. Klik op Opslaan.
17. Klik op Regel toevoegen.
    * Inwisselregels worden gebruikt wanneer de methode loyaliteitsbetaling wordt gebruikt.  
18. Klik in het veld Beloningspunt-id op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Alleen inwisselbare beloningspunten worden weergegeven.  
19. Klik in de lijst op de koppeling in de geselecteerde rij.
20. Voer in het veld Beloningspunten een getal in.
21. Selecteer een optie in het veld Type inwisseling.
    * Als u Betaling per bedrag selecteert, wordt het bedrag- of hoeveelheidveld behandeld als een valutawaarde. In dit geval is het aantal beloningspunten dat per valutaeenheid van betaling wordt gebruikt, een vaste verhouding. Als u Betaling per hoeveelheid selecteert, wordt het bedrag- of hoeveelheidveld behandeld als een hoeveelheidswaarde. In dit geval is het aantal beloningspunten dat per artikelhoeveelheid wordt gebruikt, een vaste verhouding, maar de hoeveelheid in valuta kan variëren als de prijs van artikelen waarvoor met beloningspunten is betaald, voor dezelfde hoeveelheid varieert. Inwisseling van het type Korting voor loyaliteitspunten is alleen geldig als de land/regio-specifieke functieconfiguratiesleutel 'Rusland' is ingeschakeld en de POS-functionaliteitsprofielen de ISO-code 'RU' hebben.  
    * Een categorie selecteren. De categorie beperkt op welke producten deze inwisselregel van toepassing is.  
    * Als u wilt dat de inwisselregel van toepassing is op alle producten, laat u dit veld leeg.  
22. Typ een getal in het veld Bedrag of hoeveelheid.
23. Typ een waarde in het veld Valuta.
24. Klik op Opslaan.
25. Klik op Regel toevoegen.
    * Selecteer een of meer knooppunten in de lijst Beschikbare organisatieknooppunten en verplaats deze naar de lijst Geselecteerde organisatieknooppunten door op de pijl tussen de twee lijsten te klikken.  
26. Klik op OK.
27. Klik op Opslaan.
    * Elke keer dat u de kanalen voor een loyaliteitsschema wijzigt, moet u Loyaliteitsschema verwerken uitvoeren. Op die manier krijgen de kanalen bijgewerkte loyaliteitsschema's.  

