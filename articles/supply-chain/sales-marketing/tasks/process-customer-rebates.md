---
title: Klantkortingen genereren en verwerken
description: Deze procedure demonstreert hoe u klantkortingen verwerkt van het genereren van de claim tot het doorgeven ervan als toerekeningen aan Debiteuren.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c77129abc5c93d7b11445bdaa2c4851d73bb0b62
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383591"
---
# <a name="generate-and-process-customer-rebates"></a>Klantkortingen genereren en verwerken

[!include [banner](../../includes/banner.md)]

Deze procedure demonstreert hoe u klantkortingen verwerkt van het genereren van de claim tot het doorgeven ervan als toerekeningen aan Debiteuren. U wordt geleid door een specifiek voorbeeld om uit te leggen hoe de verschillende voorwaarden van de kortingsregels van invloed zijn op de uiteindelijke bedragen die aan de klant worden gecrediteerd. U moet het demobedrijf USMF gebruiken en de volgende taken uitvoeren voordat u de begeleiding start: (1) Ga naar de pagina Parameters van module Klanten en vouw het tabblad Prijzen en vervolgens het tabblad Prijsgegevens uit en controleer of de optie Prijsdetails inschakelen is ingesteld op Ja. (2) Ga naar de pagina Kortingsovereenkomsten en selecteer de kortingsovereenkomst van de klant: USMF-000001. Als het veld Goedkeuringsstatus workflow niet is ingesteld op Goedgekeurd, moet u in het actievenster op Validatie klikken om deze goed te keuren.


## <a name="review-a-customer-rebate-agreement"></a>Een klantkortingsovereenkomst controleren
1. Ga naar **Navigatiedeelvenster > Modules > Verkoop en marketing > Klantkortingen > Kortingsovereenkomsten**.
    - De volgende paar stappen kijken naar de voorwaarden van de overeenkomst USMF-000001. Dit maakt het gemakkelijker te begrijpen hoe de klantkredietwaarden later in de procedure worden berekend.  
    - De overeenkomst is voor een afzonderlijke klant, in dit voorbeeld klant US-009.  
    - Kortingen worden gegeven aan de klant wanneer deze een specifiek product koopt. In dit geval heeft het product artikelnummer T0020.   
    - De verkoopprestaties van de klant, op basis waarvan de kortingsbedragen worden geraamd, worden op wekelijkse basis samengevoegd.  
    - De instelling voor Prijs gehaald uit is Bruto, wat betekent dat het verkoopbedrag van de regel op basis waarvan de claim wordt geraamd, niet wordt verlaagd met de regelkorting.  
    - Het veld Regelafbrekingstype van korting bevat de methode voor het berekenen van kortingen. In dit geval wordt het verkoopdoel op basis waarvan de kortingen worden geraamd, ingesteld op Hoeveelheid.   
    - De regels van de overeenkomst geven het type kortingsbedrag, de werkelijke kortingswaarde en de drempels aan. In dit voorbeeld komt de klant in aanmerking voor een korting van 20 USD per verkochte eenheid als zijn of haar wekelijkse aankopen van het product vallen tussen 1 en 50 eenheden. De korting is 40 USD per verkochte eenheid als de klant meer dan 50 eenheden koopt.  
2. Sluit de pagina.

## <a name="generate-rebate-claims"></a>Kortingclaims genereren
1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Verkooporders > Alle verkooporders**.
2. Klik op **Nieuw**. Om de manier om na te bootsen waarop kortingsclaims worden gegenereerd is de volgende taak een verkooporder te maken waarbij het product en de hoeveelheid de klant doen kwalificeren voor een korting.    
3. Typ of selecteer een waarde in het veld **Klantrekening**.
4. Klik op **OK**.
5. Typ of selecteer een waarde in het veld **Artikelnummer**.
6. Stel **Hoeveelheid** in op '40'.
7. Klik in de sectie **Verkooporderregels** op de optie **Verkooporderregel**.
8. Klik op **Prijsgegevens**. Als u deze optie niet ziet, is dat omdat u de optie **Prijsdetails inschakelen** niet op Ja hebt ingesteld voordat u de guide startte.     
9. Vouw de sectie **Kortingen** uit. Het tabblad **Kortingen** bevat alle kortingsovereenkomsten die van toepassing zijn op de huidige orderregel en toont het geraamde kortingsbedrag. Merk op dat de weergegeven bedragen slechts indicaties zijn van toekomstige kortingen. De werkelijke kortingsbedragen kunnen verschillen, afhankelijk van het totale bereikte verkoopvolume door de klant onder een periodieke kortingsovereenkomst; of de klant alle of gedeeltelijke hoeveelheden had geretourneerd; en of de toepasselijke verkooporder is gefactureerd.
10. Sluit de pagina.
11. Klik op **Regel toevoegen**.
12. Typ of selecteer een waarde in het veld **Artikelnummer**.
13. Stel **Hoeveelheid** in op '60'.
14. Klik op **Opslaan**.
15. Klik in het **actievenster** op **Factuur**.
16. Klik op **Factuur**.
17. Vouw de sectie **Parameters** uit.
18. Selecteer in het veld **Hoeveelheid** de optie Alle.
19. Klik op **OK**.
20. Klik op **OK**.

## <a name="process-rebate-claims"></a>Kortingclaims verwerken
1. Ga naar **Navigatiedeelvenster > Modules > Verkoop en marketing > Klantkortingen > Kortingen**.
    - De pagina Kortingen werkt als een workbench waar u kortingsclaims kunt controleren, goedkeuren en verwerken. Nu gaat u de claims verwerken die zijn gemaakt als resultaat van het factureren van een verkooporder voor klant US-009, die valt onder de kortingsovereenkomst USMF-000001.   
    - De eerste regel vertegenwoordigt een kortingsclaim voor 800 USD, die wordt gebaseerd op de verkoop van 40 eenheden van product T0020, berekend tegen 20 USD per eenheid. Dit komt overeen met de voorwaarden van de eerste hoeveelheidscategorie in de kortingsovereenkomst.  
    - De tweede claim is voor 2400 USD, wat is gebaseerd op de verkoop van 60 eenheden van product T0020, berekend tegen 40 USD per eenheid, op basis van de tweede hoeveelheidscategorie in de overeenkomst.  
    - Beide claims moeten de status Te berekenen hebben. Dit betekent dat ze worden gekoppeld aan een overeenkomst die de verkoopprestaties van de klant op periodieke basis bijhoudt en dat ze opnieuw moeten worden berekend in verband met het totale verkoopvolume binnen de betreffende periode.   
2. Klik op **Cumuleren**.
3. Typ of selecteer een waarde in het veld **Klant**.
4. Selecteer de datum van vandaag in het veld **Begindatum**.
5. Klik op **OK**. Als gevolg van het uitvoeren van de functie **Cumuleren** is het geraamde claimbedrag nu aangepast om rekening te houden met het feit dat het totale verkoopvolume van de klant in de relevante periode hoger is dan toen de eerste korting werd gegenereerd. Specifieker, omdat de totale gekochte hoeveelheid 100 eenheden heeft bereikt, komt de klant nu in aanmerking voor 40 USD per eenheid (volgens de tweede hoeveelheidscategorie) of 400 USD aan totaal kortingsbedrag. Het verschil wordt geregistreerd als nieuwe 'claimcorrectie' voor de extra 800 USD. De status van de kortingsclaims die in de Cumuleren-update zijn opgenomen, wordt nu ingesteld op Berekend. 
6. Markeer alle rijen in de lijst.
7. Klik op **Goedkeuren**.
8. Klik op **Verwerken**.
9. Typ of selecteer een waarde in het veld **Klant**.
10. Klik op **OK**. Een bericht geeft aan dat de korting met succes is verwerkt en dat de status van de claims is gewijzigd in Markeren. Dit betekent dat als gevolg van een boeking van een kortingstoenamejournaal het volgende gebeurt:
    - De vorderingen zijn nu als inhoudingen overgeboekt naar het tijdelijke klantsaldo.
    - De kortingstoenamerekening is gecrediteerd als aanduiding van de toekomstige verplichting naar de klant toe.
    - De kortingsonkostenrekening is gedebiteerd om de kosten te herkennen die zijn gemaakt in verband met de verkoop.   

