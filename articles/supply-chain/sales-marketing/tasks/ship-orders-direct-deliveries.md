---
title: Orders verzenden als rechtstreekse leveringen
description: Dit onderwerp toont hoe een rechtstreekse levering voor een verkooporder wordt gemaakt.
author: omulvad
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a8f214a56c6a5013cab8233d5b2e0126deb9220
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966100"
---
# <a name="ship-orders-as-direct-deliveries"></a>Orders verzenden als rechtstreekse leveringen

[!include [banner](../../includes/banner.md)]

Dit onderwerp toont hoe een rechtstreekse levering voor een verkooporder wordt gemaakt. U gebruikt rechtstreekse levering wanneer u goederen rechtstreeks van uw leverancier naar de klant wilt verzenden in plaats van deze eerst naar uw eigen magazijn te verzenden. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens. Om de tweede subtaak 'Rechtstreekse leveringen vanaf de workbench maken' met succes te voltooien, controleert u dat er voor het artikel dat u op de verkooporder kiest een standaardleverancier is opgegeven op het sneltabblad Inkoop van het model Vrijgegeven product.

## <a name="set-an-individual-order-for-direct-delivery"></a>Een afzonderlijk order voor rechtstreekse levering instellen
1. Ga naar **Navigatievenster > Modules > Klanten > Orders > Alle verkooporders**.
2. Selecteer **Nieuw**.
3. Typ of selecteer een waarde in het veld **Klantaccount** en selecteer **OK**.
4. Typ of selecteer waarden in de velden **Artikelnummer** en **Vestiging** en selecteer **Opslaan**.
5. Selecteer in het actievenster de optie **Verkooporder** en vervolgens **Directe levering**. De pagina Levering maken toont alle openstaande verkooporderregels zoals die van de verkooporder zijn gekopieerd. U kunt de orderdetails controleren en, zo nodig, details zoals inkoophoeveelheid de prijsvoorwaarden wijzigen voordat u de rechtstreekse levering maakt.  
6. Selecteer **Ja** in het veld **Alles opnemen**.
    - Als u een directe levering voor een subset van de verkooporderregels wilt genereren, selecteert u deze afzonderlijk.  
    - Het veld **Leveranciersaccount** is mogelijk al ingevuld met een leveranciersnummer. Als de standaardleverancier is ingesteld voor het product (op de gekoppelde Artikelbehoefteplanning), wordt deze leverancier naar de regel gekopieerd. Anders moet u handmatig een leverancier invoeren. In dit voorbeeld selecteren we een nieuwe leverancier in de volgende stap, zelfs als er al één is ingevuld.   
7. Typ of selecteer een waarde in het veld **Leveranciersrekening** en selecteer **OK**. Het bericht meldt u dat de inkooporder nu is gemaakt.   
8. Vouw de sectie **Regeldetails** uit.
9. Ga naar het tabblad **Levering** en controleer of het veld **Directe levering** is ingesteld op **Ja**.
10. Selecteer **Algemeen** in het actievenster.
11. Selecteer **Gerelateerde orders**.
12. Selecteer de koppeling in het veld **Inkooporder**.
13. Vouw de sectie **Regeldetails** uit en selecteer het tabblad **Adres**.
    - Het afleveradres voor deze inkooporderregel is het afleveradres van de klant en niet het adres van uw bedrijf.  
    - Als u het afleveradres op de inkooporder of de oorspronkelijk verkooporderregel bijgewerkt, wordt het adres op de overeenkomstige orderregel automatisch gewijzigd.  
14. Selecteer het tabblad **Levering**.
    - Net als de verkooporderregel, wordt het gekoppelde type van inkooporderregel ook ingesteld op Rechtstreekse levering.  
    - De Leveringsdatum en Bevestigde leveringsdatum van de inkooporderregel zijn ingesteld op de Gevraagde ontvangstdatum en Bevestigde ontvangstdatum van de oorspronkelijke verkooporderregel.   
    - Als u elk van deze datums op de inkoopregel of verkoopregel bijwerkt, worden de datums op de bijbehorende order automatisch bijgewerkt.     
    - De inkooporder die is ingesteld om goederen rechtstreeks aan de klant te leveren, is door middel van een speciale koppeling gekoppeld aan de oorspronkelijke verkooporder. Deze koppeling legt de regel op dat de update van de pakbon van de verkooporder niet kan worden uitgevoerd vanaf de verkooporder zelf, maar moet worden uitgevoerd door de inkooporder te gebruiken. De klantfacturering moet echter vanaf de verkooporder worden uitgevoerd.  
15. Selecteer in het actievenster de optie **Inkoop**.
16. Selecteer **Bevestiging**.
17. Selecteer **OK**.
18. Selecteer **Ontvangen** in het actievenster.
19. Selecteer **Productontvangstbon**.
20. Typ een waarde in het veld **Productontvangstbon**.
21. Selecteer **OK**.
22. Selecteer **Algemeen** in het actievenster.
23. Selecteer **Gerelateerde orders** en markeer de gewenste record.
    - Nadat de inkooporder is bijgewerkt en ontvangen of, met andere woorden, nadat de leverancier de goederen naar het adres van de klant heeft verzonden, wordt de status van de oorspronkelijke verkooporder automatisch bijgewerkt naar Geleverd.  
    - De verkooporder kan nu worden gefactureerd.    
24. Selecteer **OK**.
25. Sluit de pagina.
26. Selecteer **OK**. Sluit de pagina's en ga terug naar de startpagina.

## <a name="create-direct-deliveries-from-the-workbench"></a>Rechtstreekse leveringen maken vanuit de workbench
1. Ga naar **Navigatievenster > Modules > Klanten > Orders > Alle verkooporders**.
2. Selecteer **Nieuw**.
3. Typ of selecteer een waarde in het veld **Klantrekening** en selecteer **OK**.
4. Typ of selecteer een waarde in de velden **Artikelnummer** en **Vestiging**.
5. Vouw de sectie **Regeldetails** uit en selecteer het tabblad **Levering**. In plaats van een rechtstreekse levering te maken als onderdeel van de verkooporderverwerking, zoals in de vorige procedure, kunt u ervoor kiezen om deze taak naar een inkoopprofessional door te sturen. Als u de verkooporderregel in het afhandelingsproces van rechtstreekse leveringen wilt opnemen, moet u de regel voor rechtstreekse levering markeren.  
6. Selecteer **Ja** in het veld **Rechtstreekse levering**.
    - Als het artikel standaard al is ingesteld voor directe levering, wordt het veld automatisch ingesteld op Ja op de orderregelinvoer. U kunt een artikel instellen voor directe levering op het model van het Vrijgegeven product door de optie Directe levering in te stellen op Ja en een standaardmagazijn voor rechtstreekse levering te selecteren.  
    - Omdat de inkooporder nog niet is gemaakt, wordt de status Rechtstreekse levering ingesteld op "Voor directe levering".   
7. Selecteer **Opslaan**.
8. Sluit de pagina's tot u terugbent op de startpagina.
9. Voer `Direct delivery` in de zoekbalk in.
    - De pagina Rechtstreekse levering fungeert als workbench die de inkoper voorziet van een overzicht van alle verkooporderregels die rechtstreeks moeten worden geleverd. Deze pagina biedt ook de mogelijkheid om de betreffende inkooporders te maken. Bovendien kunnen ze de openstaande rechtstreekse leveringsorders en bevestigde orders op de tabbladen Bevestiging en Levering weergeven.  
    - Nadat u een order voor rechtstreekse levering hebt gemaakt, wordt deze automatisch naar het tabblad Bevestiging verplaatst. U kunt de order rechtstreeks op deze pagina bevestigen. Als de aankoop is bevestigd, wordt deze automatisch naar het tabblad Levering verplaatst, waar u de ontvangst ervan kunt registreren.  

