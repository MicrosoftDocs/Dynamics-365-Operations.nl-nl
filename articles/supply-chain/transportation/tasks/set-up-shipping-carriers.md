--- 
title: Vervoerders instellen
description: Deze procedure laat zien hoe u een vervoerder instelt en details bepaalt zoals service, modus van zending, transportaanbesteding, transportbeperkingen en verzendtarief.
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-shipping-carriers"></a>Vervoerders instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een vervoerder instelt en details bepaalt zoals service, modus van zending, transportaanbesteding, transportbeperkingen en verzendtarief. Een transportcoördinator kan vervolgens een vervoerder toewijzen aan een inkomende of uitgaande lading.


## <a name="create-a-new-shipping-carrier"></a>Een nieuwe vervoerder maken
1. Ga naar Transportbeheer > Instellingen > Vervoerders > Vervoerders.
2. Klik op Nieuw.
3. Typ een waarde in het veld Vervoerder.
4. Typ een waarde in het veld Naam.
5. Klik in het veld Modus op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>De algemene informatie voor de vervoerder invullen
1. Schakel de uitbreiding van de sectie Overzicht om.
2. Schakel het selectievakje Vervoerder activeren in of uit.
3. Klik in het veld Leverancier op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer de leverancierrekening waaraan de vervoerder moet worden toegewezen.  
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Selecteer een optie in het veld Type betalingsmethode transport.
    * Selecteer Handmatig om de pagina Transportbetalingsmethode te gebruiken of selecteer EDI om de betalingsmethode bij te werken met Electronic Data Interchange (EDI).  
7. Schakel het selectievakje Vervoerdersbeoordeling activeren in of uit.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>De nodige services voor de vervoerder maken
1. Schakel de uitbreiding van de sectie Services om.
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld Vervoerdersservice.
5. Typ een waarde in het veld Naam.
6. Klik in het veld Transportmethode op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer de gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Het adres voor de vervoerder instellen (optioneel)
1. Schakel de uitbreiding van de sectie Adressen om.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam of omschrijving.
4. Klik in het veld Land/regio op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik in het veld Postcode op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer het gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Typ een waarde in het veld Straat.
10. Klik op OK.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Het tariefprofiel voor de vervoerder instellen
1. Schakel de uitbreiding van de sectie Beoordelingsprofielen om.
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld Beoordelingsprofiel.
5. Typ een waarde in het veld Naam.
6. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer het gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
10. Zoek en selecteer het gewenste record in de lijst.
11. Klik in de lijst op de koppeling in de geselecteerde rij.
12. Klik in het veld Tariefengine op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer de tariefengine die in overeenstemming is met het contract dat u hebt met de vervoerder.  
13. Zoek en selecteer de gewenste record in de lijst.
14. Klik in de lijst op de koppeling in de geselecteerde rij.
15. Klik in het veld Tariefmodel op de vervolgkeuzeknop om de zoekopdracht te openen.
16. Zoek en selecteer het gewenste record in de lijst.
17. Klik in de lijst op de koppeling in de geselecteerde rij.
18. Klik in het veld Engine voor transittijd op de vervolgkeuzeknop om de zoekopdracht te openen.
19. Klik in de lijst op de koppeling in de geselecteerde rij.
20. Klik op Opslaan.


