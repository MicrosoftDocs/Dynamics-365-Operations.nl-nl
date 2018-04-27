--- 
title: Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen
description: Deze procedure laat u zien hoe u antwoorden op een offerteaanvraag invoert, biedingen vergelijkt en vervolgens de bieding aan een van de leveranciers toekent.
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat u zien hoe u antwoorden op een offerteaanvraag invoert, biedingen vergelijkt en vervolgens de bieding aan een van de leveranciers toekent. U kunt deze procedure gebruiken in het demobedrijf USMF. Voordat u begint, moet u een offerteaanvraag hebben met twee regels die aan ten minste twee leveranciers is verzonden. U kunt de procedure "Een offerteaanvraag maken" uitvoeren als een vereiste om dit te maken. U moet beoordelingscriteria hebben ingesteld voordat u deze procedure kunt uitvoeren.


## <a name="enter-a-reply-from-a-vendor"></a>Een antwoord van een leverancier invoeren
1. Ga naar Inkoop en sourcing > Offerteaanvragen > Alle offerteaanvragen.
2. Selecteer een offerteaanvraag met de status Verzonden en klik op de koppeling op het nummer van de offerteaanvraagcase.
    * De offerteaanvraag moet naar minstens 2 leveranciers zijn verzonden.  
3. Klik op Koptekst om naar de lijst met leveranciers te gaan.
4. Selecteer de leverancier voor wie u een antwoord op de offerteaanvraag wilt invoeren.
5. Klik op Antwoord invoeren.
6. Klik in het actievenster op Beantwoorden.
7. Klik op Gegevens kopiëren naar antwoord.
    * Met deze actie worden geselecteerde gegevens gekopieerd, bijvoorbeeld de hoeveelheid van de offerteaanvraagcase naar het antwoord op de offerteaanvraag. Ook kunt u deze actie overslaan en alle antwoordvelden handmatig invullen wanneer u het antwoord bewerkt.  
8. Klik op Bewerken.
9. Voer in het veld Eenheidsprijs een getal in.
10. Kies de andere offerteregel.
11. Voer in het veld Eenheidsprijs een getal in.

## <a name="score-the-bid"></a>De bieding beoordelen
1. Klik op Koptekst om naar de beoordeling van de bieding te gaan.
2. Vouw de sectie Beoordeling bieding uit.
3. Voer in het veld Score een nummer voor een van de beoordelingscriteria in.
    * Als u de muis boven een van de beoordelingscriteria plaatst, wordt met knopinfo het bereik getoond waarbinnen u moet scoren. In deze demo kunt u een getal tussen 1 en 5 aan de criteria toevoegen.  
4. Selecteer een ander beoordelingscriterium.
5. Voer een getal in het veld Score in.
6. Vouw de sectie Vragenlijsten uit.
    * Als de offerteaanvraagcase een vragenlijst heeft die naar de leveranciers is verzonden, kunt u de bijbehorende antwoorden in de vragenlijstsectie invoeren.  
7. Sluit de pagina.

## <a name="enter-a-reply-for-another-vendor"></a>Een antwoord voor een andere leverancier invoeren
1. Selecteer de volgende leverancier door de leverancier te wissen voor wie u zojuist het antwoord hebt ingevoerd en vervolgens de rij voor de volgende leverancier te selecteren.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik op Antwoord invoeren.
4. Klik op Gegevens kopiëren naar antwoord.
5. Klik op Bewerken.
6. Voer in het veld Eenheidsprijs een getal in.
7. Kies de andere offerteregel.
8. Voer in het veld Eenheidsprijs een getal in.

## <a name="score-the-second-bid"></a>De tweede bieding beoordelen
1. Klik op Koptekst om naar de beoordeling van de bieding te gaan.
2. Voer een getal in het veld Score in.
3. Zoek en selecteer de gewenste record in de lijst.
4. Voer een getal in het veld Score in.

## <a name="compare-the-replies"></a>De antwoorden vergelijken
1. Klik in het actievenster op Algemeen.
2. Klik op Antwoorden vergelijken.
3. Voer een getal in het veld Positie in.
    * Deze pagina bevat de biedingen met de koptekst en de regels en de totale score op koptekstniveau. U kunt de regels vergelijken door deze in het raster zo te sorteren dat vergelijkbare regels zich naast elkaar bevinden. De informatie bevat ook: Hoeveelheid: de hoeveelheid die door de leverancier in de offerte is opgenomen. Deze hoeveelheid komt mogelijk niet overeen met de hoeveelheid in de offerteaanvraag.   Nettobedrag: de prijs die door een leverancier is opgegeven na aftrek van eventuele kortingen voor de artikelen op de regel.   Afwijking: het aantal dagen dat de leveringsdatum in de koptekst of de regel van de bieding afwijkt van de gevraagde leveringsdatum in de koptekst van de offerteaanvraag of de offerteaanvraagregel.   U kunt voor elke bieding een positie invoeren:  
4. Selecteer de koptekstregel voor de andere bieding waaraan u een positie wilt toekennen.
5. Voer een getal in het veld Positie in.
6. Klik op Opslaan.

## <a name="reject-a-bid"></a>Een bieding afwijzen
1. Selecteer de koptekstregel voor de bieding die u wilt afwijzen.
    * U kunt slechts één bieding of regels in één bieding tegelijk accepteren, afwijzen of retourneren.  
2. Schakel het selectievakje Markeren in.
    * Als u het selectievakje Markeren in de koptekst van de bieding inschakelt, worden ook alle regels gemarkeerd. U kunt er ook voor kiezen een subset van de regels binnen de bieding te markeren om deze te weigeren of te accepteren. Het is mogelijk om de bieding van één leverancier voor sommige regels van een offerteaanvraag te accepteren en vervolgens andere offerteaanvraagregels aan een andere leverancier toe te kennen. U dient dit echter in 2 stappen te doen, met één bieding tegelijk. Als er alternatieve regels aanwezig zijn, kunt u alleen de originele biedingsregel accepteren of het bijbehorende alternatief, maar niet beide.  
3. Klik op Afwijzen.
4. Klik op Parameters om het dialoogvenster te openen.
5. Typ of selecteer een waarde in het veld Reden afwijzing.
    * De reden voor afwijzing wordt in het antwoord opgeslagen.  
6. Klik op OK.
7. Klik op OK.
8. Sluit de pagina.
9. Sluit de pagina.
10. Vernieuw de pagina.

## <a name="accept-a-bid"></a>Een bieding accepteren
1. Selecteer de bieding die u wilt accepteren en klik vervolgens op de koppeling in het veld Offerteaanvraag.
2. Klik in het actievenster op Beantwoorden.
3. Klik op Accepteren.
    * Als u specifieke regels hebt gemarkeerd en geen andere, worden bij het accepteren alleen de gemarkeerde regels opgenomen. Als u alle regels in de bieding wilt accepteren, hoeft u de regels niet te markeren.  
4. Klik op Parameters om het dialoogvenster te openen.
    * Hiermee kunt u een reden registreren voor acceptatie van de bieding. De reden wordt in de bieding opgeslagen.  
5. Typ of selecteer een waarde in het veld Reden voor accepteren.
6. Klik op OK.
7. Klik op OK.
    * Wanneer u klikt op OK, wordt een inkooporder gegenereerd op basis van de regels die in de acceptatie van de offerteaanvraag zijn opgenomen. Als er andere biedingen zijn die niet zijn verwerkt (geaccepteerd, afgewezen of geretourneerd), wordt u gevraagd de resterende biedingen te weigeren.  

## <a name="view-the-purchase-order-thats-been-generated"></a>De inkooporder weergeven die is gegenereerd.
1. Klik in het actievenster op Algemeen.
2. Klik op Inkooporder.
    * Hier kunt u de inkooporder zien die is gegenereerd toen u de bieding accepteerde.  
3. Sluit de pagina.
4. Sluit de pagina.
5. Sluit de pagina.
6. Sluit de pagina.


