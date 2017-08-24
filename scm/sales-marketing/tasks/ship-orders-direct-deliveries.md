--- 
title: Orders verzenden als rechtstreekse leveringen
description: Deze procedure toont hoe een rechtstreekse levering voor een verkooporder wordt gemaakt.
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d98e288a157183fbf4d7c032d86bb4a65166e297
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Orders verzenden als rechtstreekse leveringen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe een rechtstreekse levering voor een verkooporder wordt gemaakt. U gebruikt rechtstreekse levering wanneer u goederen rechtstreeks van uw leverancier naar de klant wilt verzenden in plaats van deze eerst naar uw eigen magazijn te verzenden. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens. Om de tweede subtaak 'Rechtstreekse leveringen vanaf de workbench maken' met succes te voltooien, controleert u dat er voor het artikel dat u op de verkooporder kiest een standaardleverancier is opgegeven op het sneltabblad Inkoop van het model Vrijgegeven product.


## <a name="set-an-individual-order-for-direct-delivery"></a>Een afzonderlijk order voor rechtstreekse levering instellen
1. Ga naar Alle verkooporders.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Klantrekening.
    * Als u USMF gebruikt, kunt u rekening US-001 selecteren.  
4. Klik op OK.
5. Typ of selecteer een waarde in het veld Artikelnummer.
    * Als u USMF gebruikt, kunt u artikel T0020 selecteren.  
6. Klik op Opslaan.
7. Klik in het actievenster op Verkooporder.
8. Klik op Rechtstreekse levering.
    * De pagina Levering maken toont alle openstaande verkooporderregels zoals die van de verkooporder zijn gekopieerd. U kunt de orderdetails controleren en, zo nodig, details zoals inkoophoeveelheid de prijsvoorwaarden wijzigen voordat u de rechtstreekse levering maakt.  
9. Selecteer Ja in het veld Alles opnemen.
    * Als u een directe levering voor een subset van de verkooporderregels wilt genereren, selecteert u deze afzonderlijk.  
    * Het veld Leveranciersrekening is mogelijk al ingevuld met een leveranciersnummer. Als de standaardleverancier is ingesteld voor het product (op de gekoppelde Artikelbehoefteplanning), wordt deze leverancier naar de regel gekopieerd. Anders moet u handmatig een leverancier invoeren. In dit voorbeeld selecteren we een nieuwe leverancier in de volgende stap, zelfs als er al één is ingevuld.   
10. Typ of selecteer een waarde in het veld Leveranciersrekening.
    * Als u USMF gebruikt, kunt u rekening 1001 selecteren.  
11. Klik op OK.
    * Het bericht meldt u dat de inkooporder nu is gemaakt.   
12. Vouw de sectie Regeldetails uit.
13. Klik op het tabblad Levering.
    * Het veld Rechtstreekse levering is nu ingesteld op Ja.  
    * De status Rechtstreekse levering toont de gemaakte inkooporder.   
14. Klik in het actievenster op Algemeen.
15. Klik op Gerelateerde orders.
16. Klik om de koppeling in het veld Inkooporder te volgen.
17. Vouw de sectie Regeldetails uit.
18. Klik op het tabblad Adres.
    * Het afleveradres voor deze inkooporderregel is het afleveradres van de klant en niet het adres van uw bedrijf.  
    * Als u het afleveradres op de inkooporder of de oorspronkelijk verkooporderregel bijgewerkt, wordt het adres op de overeenkomstige orderregel automatisch gewijzigd.  
19. Klik op het tabblad Levering.
    * Net als de verkooporderregel, wordt het gekoppelde type van inkooporderregel ook ingesteld op Rechtstreekse levering.  
    * De Leveringsdatum en Bevestigde leveringsdatum van de inkooporderregel zijn ingesteld op de Gevraagde ontvangstdatum en Bevestigde ontvangstdatum van de oorspronkelijke verkooporderregel.   
    * Als u elk van deze datums op de inkoopregel of verkoopregel bijwerkt, worden de datums op de bijbehorende order automatisch bijgewerkt.     
    * De inkooporder die is ingesteld om goederen rechtstreeks aan de klant te leveren is gekoppeld aan de oorspronkelijke verkooporder door middel van een speciale koppeling. Deze koppeling legt de regel op dat de update van de pakbon van de verkooporder niet kan worden uitgevoerd vanaf de verkooporder zelf, maar moet worden uitgevoerd door de inkooporder te gebruiken. De klantfacturering moet echter vanaf de verkooporder worden uitgevoerd.  
20. Klik in het actievenster op Inkoop.
21. Klik op Bevestiging.
22. Klik op OK.
23. Klik in het actievenster op Ontvangen.
24. Klik op Productontvangstbon.
25. Typ een waarde in het veld Productontvangstbon.
26. Klik op OK.
27. Klik in het actievenster op Algemeen.
28. Klik op Gerelateerde orders.
29. Markeer in de lijst de geselecteerde rij.
    * Nadat de inkooporder is bijgewerkt en ontvangen of, met andere woorden, nadat de leverancier de goederen naar het adres van de klant heeft verzonden, wordt de status van de oorspronkelijke verkooporder automatisch bijgewerkt naar Geleverd.  
    * De verkooporder kan nu worden gefactureerd.    
30. Klik op OK.
31. Sluit de pagina.
32. Klik op OK.

## <a name="create-direct-deliveries-from-the-workbench"></a>Rechtstreekse leveringen maken vanuit de workbench
1. Sluit de pagina.
2. Sluit de pagina.
3. Ga naar Alle verkooporders.
4. Klik op Nieuw.
5. Typ of selecteer een waarde in het veld Klantrekening.
6. Klik op OK.
7. Typ of selecteer een waarde in het veld Artikelnummer.
8. Vouw de sectie Regeldetails uit.
9. Klik op het tabblad Levering.
    * In plaats van een rechtstreekse levering te maken als onderdeel van de verkooporderverwerking, zoals in de vorige procedure, kunt u ervoor kiezen om deze taak naar een inkoopprofessional door te sturen. Als u de verkooporderregel in het afhandelingsproces van rechtstreekse leveringen wilt opnemen, moet u de regel voor rechtstreekse levering markeren.  
10. Selecteer Ja in het veld Rechtstreekse levering.
    *   Als het artikel standaard al is ingesteld voor directe levering, wordt het veld automatisch ingesteld op Ja op de orderregelinvoer. U kunt een artikel instellen voor directe levering op het model van het Vrijgegeven product door de optie Directe levering in te stellen op Ja en een standaardmagazijn voor rechtstreekse levering te selecteren.  
    * Omdat de inkooporder nog niet is gemaakt, wordt de status Rechtstreekse levering ingesteld op Voor directe levering.   
11. Sluit de pagina.
12. Sluit de pagina.
13. Ga naar Rechtstreekse levering.
    * De pagina Rechtstreekse levering fungeert als workbench die de inkoper voorziet van een overzicht van alle verkooporderregels die rechtstreeks moeten worden geleverd. Deze pagina biedt ook de mogelijkheid om de betreffende inkooporders te maken. Bovendien kunnen ze de openstaande rechtstreekse leveringsorders en bevestigde orders op de tabbladen Bevestiging en Levering weergeven.   
14. Klik op Rechtstreekse levering maken.
15. Klik op het tabblad Bevestiging.
    * Nadat u een order voor rechtstreekse levering hebt gemaakt, verplaatst deze automatisch naar het tabblad Bevestiging. U kunt de order rechtstreeks op deze pagina bevestigen. Als de aankoop is bevestigd, wordt deze automatisch naar het tabblad Levering verplaatst, waar u de ontvangst ervan kunt registreren.  


