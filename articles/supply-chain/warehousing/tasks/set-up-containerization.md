--- 
title: Containervorming instellen
description: Met deze procedure wordt beschreven hoe u de containervorming van ladingen in Magazijnbeheer kunt automatiseren.
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: c5faf926071dec5d2ddc1c9e921a98ecd0754917
ms.contentlocale: nl-nl
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-containerization"></a>Containervorming instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Met deze procedure wordt beschreven hoe u de containervorming van ladingen in Magazijnbeheer kunt automatiseren. Met geautomatiseerde containervorming worden containers en orderverzamelingen voor zendingen gemaakt wanneer een wave wordt verwerkt en werkregels kunnen worden opgesplitst in hoeveelheden die in de containers passen. Dit helpt werknemers de artikelen direct in de gekozen container te verzamelen. Vergeleken met het handmatige verpakkingsproces worden taken zoals het maken van containers, het toewijzen van artikelen en het sluiten van containers geautomatiseerd door het systeem. In deze procedure wordt het demobedrijf USMF gebruikt en deze procedure wordt door een magazijnmanager uitgevoerd.


## <a name="set-up-a-wave-template"></a>Een wavesjabloon instellen
1. Ga naar Magazijnbeheer > Instellingen > Waves > Wavesjablonen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Wavesjabloon.
4. Typ een waarde in het veld Omschrijving van wavesjabloon.
5. Typ of selecteer een waarde in het veld Locatie.
6. Typ of selecteer een waarde in het veld Magazijn.
7. Vouw de sectie Methoden uit.
    * In het deelvenster Geselecteerde methoden worden de methoden voor het geselecteerde type wavesjabloon weergegeven. De wavesjabloon moet de methode Containervormen bevatten.  
8. Zoek en selecteer de gewenste record in de lijst.
9. Typ een waarde in het veld Wavestapcode.
    * Voer een wavestapcode voor de toegevoegde methode in. Dit kan elke code zijn. Het is mogelijk om de methode meerdere malen toe te voegen en verschillende wavestapcodes toe te wijzen. Selecteer hiervoor Herhaalbaar voor deze methode op de pagina Methoden voor verwerking van waves.  
10. Klik op Opslaan.
11. Sluit de pagina.

## <a name="set-up-a-container-type"></a>Een containertype instellen
1. Ga naar Magazijnbeheer > Instellingen > Containers > Containertypen.
    * U kunt uw containers definiëren op de pagina Containertypen. U kunt de fysieke afmetingen van containers configureren, waaronder tarragewicht, maximumgewicht, maximumvolume, lengte, breedte en hoogte. In dit voorbeeld zijn er drie verschillende formaten van dozen.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Containertype.
4. Voer een getal in het veld Tarragewicht in.
5. Voer in het veld Maximumgewicht een getal in.
6. Voer een getal in het veld Volume in.
7. Voer een getal in het veld Lengte in.
8. Voer een getal in het veld Breedte in.
9. Voer een getal in het veld Hoogte in.
10. Typ een waarde in het veld Omschrijving.
11. Klik op Opslaan.
12. Klik op Nieuw.
13. Typ een waarde in het veld Containertype.
14. Typ een waarde in het veld Omschrijving.
15. Voer een getal in het veld Tarragewicht in.
16. Voer in het veld Maximumgewicht een getal in.
17. Voer een getal in het veld Volume in.
18. Voer een getal in het veld Lengte in.
19. Voer een getal in het veld Breedte in.
20. Voer een getal in het veld Hoogte in.
21. Klik op Opslaan.
22. Klik op Nieuw.
23. Typ een waarde in het veld Containertype.
24. Typ een waarde in het veld Omschrijving.
25. Voer een getal in het veld Tarragewicht in.
26. Voer in het veld Maximumgewicht een getal in.
27. Voer een getal in het veld Volume in.
28. Voer een getal in het veld Lengte in.
29. Voer een getal in het veld Breedte in.
30. Voer een getal in het veld Hoogte in.
31. Klik op Opslaan.
32. Sluit de pagina.

## <a name="set-up-a-container-group"></a>Een containergroep instellen
1. Ga naar Magazijnbeheer > Instellingen > Containers > Containergroepen.
2. Klik op Nieuw.
    * U kunt logische groepen containertypen instellen. Voor elke groep kunt u de volgorde opgeven waarin de containers moeten worden verpakt, en het vulpercentage van elke container. De groottedimensies van het artikel worden gebruikt om te bepalen of het in een container past. De container die het nauwst aansluit bij de groottedimensies van het artikel, wordt gebruikt. Als u meerdere containertypen in een groep hebt, is het raadzaam deze op grootte te rangschikken zodat de grootste container eerste is, nummer 1 is in de volgorde, en de kleinste container laatste is.    
3. Typ een waarde in het veld Containergroep-ID.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Nieuw.
6. Markeer in de lijst de geselecteerde rij.
7. Typ of selecteer een waarde in het veld Containertype.
8. Klik op Nieuw.
9. Markeer in de lijst de geselecteerde rij.
10. Typ of selecteer een waarde in het veld Containertype.
11. Klik op Nieuw.
12. Markeer in de lijst de geselecteerde rij.
13. Typ of selecteer een waarde in het veld Containertype.
14. Klik op Opslaan.
15. Sluit de pagina.

## <a name="set-up-a-container-build-template"></a>Een containervormingsjabloon instellen
1. Ga naar Magazijnbeheer > Instellingen > Containers > Containervormingssjablonen.
2. Klik op Nieuw.
    * Welke containervormingssjabloon wordt gebruikt, wordt gebaseerd op welke containervormingsprocessen worden uitgevoerd. Met elke containervormingssjabloon wordt één containervormingsproces gedefinieerd dat door een wavesjabloon wordt gebruikt. Met de optie Query bewerken kunt u de voorwaarden definiëren waaronder de geselecteerde sjabloon wordt verwerkt. U kunt bijvoorbeeld containervorming alleen voor specifieke klanten, producten of magazijnen uitvoeren of u kunt de bijbehorende querybereiken aan de sjabloon toevoegen. Met het veld Wavestapcode wordt bepaald hoe een containervormingssjabloon wordt gekoppeld aan stappen in een wavesjabloon. Wanneer een wave wordt uitgevoerd, wordt bepaald welke containervormingssjabloon wordt gebruikt om containervorming uit te voeren. Met het veld Basisquerytypen wordt bepaald wat moet worden verpakt en waarop de filterquery moet worden gebaseerd.  
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld ID containersjabloon.
5. Typ of selecteer een waarde in het veld Containergroep-ID.
6. Typ een waarde in het veld Wavestapcode.
7. Schakel het selectievakje Gesplitst verzamelen toestaan in.
8. Klik op Opslaan.
9. Klik op Mengbeperkingen voor containers.
    * Met Logica-onderbrekingen mengen kunt u regels instellen voor het verpakken van toewijzingsregels in containers. Als u bijvoorbeeld het veld Artikelnummer toevoegt, wordt wanneer artikelen aan containers worden toegewezen, een nieuwe container gemaakt wanneer er een nieuw artikelnummer is. Hiermee wordt voorkomen dat werknemers toewijzingsrgels voor twee verschillende klanten in dezelfde container verpakken.  
10. Klik op Nieuw.
11. Selecteer een optie in het veld Tabel.
12. Typ of selecteer een waarde in het veld Veld selecteren.
13. Klik op OK.


