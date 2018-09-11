--- 
title: Een inkooporder maken op basis van een verkooporder
description: Deze procedure toont u hoe u een inkooporder maakt op basis van een verkooporder.
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 412a8c7acca06fc1be073019f91144e2a3f1c94b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Een inkooporder maken op basis van een verkooporder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont u hoe u een inkooporder maakt op basis van een verkooporder. De hoeveelheden van het product op de inkooporder worden vervolgens toegewezen om te voldoen aan de vraag van de oorspronkelijke verkooporder. Het op deze manier vervullen van de verkoopvraag is een alternatief voor een meer uitvoerige en geoptimaliseerde methode van Distributiebehoeftenplanning. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Een inkooporder maken op basis van een verkooporder
1. Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.
2. Klik op Nieuw.
3. Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik op OK.
6. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer de gewenste record in de lijst.
    * Als u USMF gebruikt, kunt u D0001 selecteren.  
8. Voer in het veld Hoeveelheid een getal in.
9. Klik op Regel toevoegen.
10. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Zoek en selecteer de gewenste record in de lijst.
    * Als u USMF gebruikt, kunt u T0020 selecteren.  
12. Klik in de lijst op de koppeling in de geselecteerde rij.
13. Voer in het veld Hoeveelheid een getal in.
14. Klik op Opslaan.
15. Klik in het actievenster op Verkooporder.
16. Klik op Inkooporder.
    * De pagina Inkooporder maken toont alle openstaande verkooporderregels die van de verkooporder zijn gekopieerd. U kunt de orderdetails controleren en, zo nodig, geselecteerde details zoals inkoophoeveelheid de prijsvoorwaarden wijzigen voordat u de inkopen maakt.  
17. Selecteer de optie Alles opnemen.
    * Als u inkooporders wilt genereren voor slechts een subset van de verkooporderregels, selecteert u deze afzonderlijk.  
    * Het veld Leveranciersrekening is mogelijk al ingevuld met een leveranciersnummer. Als de standaardleverancier is ingesteld voor het product (op de gekoppelde Artikelbehoefteplanning), wordt deze leverancier naar de regel gekopieerd. Anders moet u handmatig een leverancier invoeren.  Ongeacht of het veld Leveranciersrekening al een waarde bevat, begeleiden de volgende stappen in deze handleiding u bij het selecteren van een nieuwe leverancier die voor elke regel verschillend is.  
18. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
19. Zoek en selecteer het gewenste record in de lijst.
20. Klik in de lijst op de koppeling in de geselecteerde rij.
21. Selecteer de tweede orderregel.
22. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
23. Zoek en selecteer het gewenste record in de lijst.
24. Klik in de lijst op de koppeling in de geselecteerde rij.
25. Klik op Valideren.
26. Klik op OK.
    * Het bericht meldt u dat er nu een or meer inkooporders zijn gemaakt. Het systeem genereert een aparte inkooporder voor elke leverancier die u voor de verkooporderregels hebt opgegeven. Dit betekent dat als verschillende verkooporderregels door dezelfde leverancier moeten worden geleverd, er één inkooporder met meerdere regels wordt gegenereerd.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Inkooporders controleren die werden gemaakt op basis van verkooporders
1. Klik in het actievenster op Algemeen.
2. Klik op Gerelateerde orders.
    * De pagina Gerelateerde orders toont alle orders die met de verkooporder werden gemaakt. In dit voorbeeld zijn er twee inkooporders gegenereerd voor twee verschillende leveranciers.  
3. Klik om de koppeling in het veld Inkooporder te volgen.
    * Elke inkooporderregel wordt gekoppeld aan de verkooporderregel die heeft geleid tot de inkoop. De relatie met de verkooporder wordt opgegeven op het Tabblad Product in het snelttabblad Regeldetails, in de velden Verwijzingstype, Verwijzingsnummer en Verwijzingspartij.  
4. Vouw de sectie Regeldetails uit of samen.
5. Klik op het tabblad Product.
    * De verwijzingspartij garandeert dat de kosten van de huidige inkoop worden doorbelast in de bijgevoegde verkooporder.  
    * U kunt naar de oorspronkelijke verkooporder navigeren door de koppeling te openen in het veld Verwijzingsnummer.  


