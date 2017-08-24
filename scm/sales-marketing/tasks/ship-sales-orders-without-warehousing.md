--- 
title: Verkooporders verzenden zonder magazijn
description: Deze handleiding geeft aan hoe u een verkooporder bijwerkt wanneer producten naar de klant zijn verzonden.
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: ab2b52b91bcaef57996ae35120e8713aac5852e7
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="ship-sales-orders-without-warehousing"></a>Verkooporders verzenden zonder magazijn

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze handleiding geeft aan hoe u een verkooporder bijwerkt wanneer producten naar de klant zijn verzonden. De handleiding is van toepassing op de vervullingsstroom die niet is ingesteld voor magazijnbeheer (geen basale of geavanceerd magazijnen) en vereist daarom niet dat productorderverzameling vóór zending wordt geregistreerd. U kunt deze procedure uitvoeren met uw eigen gegevens of in het demogegevensbedrijf USMF. In beide gevallen maakt u voordat u deze taak start, een verkooporder voor een voorraadproduct met een hoeveelheid die groter is dan 1. Als u een boekingsfout wilt voorkomen, moet u controleren of de voorhanden hoeveelheid van het product op de site en in het magazijn dat u hebt geselecteerd op de order, de orderhoeveelheid dekt.


## <a name="post-packing-slip-for-an-order"></a>Een pakbon boeken voor een order
1. Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.
2. Zoek en selecteer in de lijst de order die u voor deze taak hebt gemaakt.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het actievenster op Verzamelen en inpakken.
5. Klik op Pakbon boeken.
6. Vouw de sectie Parameters uit of samen.
7. Selecteer in het veld Hoeveelheid de optie 'Alle'.
    * Andere opties omvatten Nu leveren en Verzameld. Als de orderregel gedeeltelijk moet worden verzonden en het veld Nu leveren op de orderregel een hoeveelheid bevat, selecteert u Nu leveren. Als orderverzameling in de vervullingsstroom van uw organisatie een afzonderlijk proces is dat wordt beheerd door en is geregistreerd met een orderverzamellijst, selecteert u Verzameld.  
    * Controleer of de optie Boeking op Ja is ingesteld.  
8. Stel de optie Pakbon afdrukken in op Ja.
    * Het tabblad Overzicht bevat een lijst met pakbonnen die in deze boeking moeten worden gegenereerd. Als u een afzonderlijk order verzendt, is er meestal één pakbon. Echter, als de regels van die order vanaf verschillende locaties moeten worden verzonden, wordt het boeken automatisch opgesplitst in het juiste aantal documenten. Dit is een verplichte voorwaarde die niet kan worden gewijzigd. Op dezelfde manier wordt de boeking ook in meerdere documenten opgesplitst als de regels van de order naar verschillende afleveradressen moeten worden verzonden. Volgens het verzendbeleid is dan een splitsing vereist.  
9. Selecteer op het tabblad Regels de rij voor de orderregel die moet worden verzonden.
10. Voer in het veld Bijwerken een cijfer in dat lager is dan de oorspronkelijke hoeveelheid.
11. Klik op OK.
12. Klik op Ja.
13. Sluit de pagina.
14. Klik in het actievenster op Opties.
15. Klik op Weergave wijzigen.
16. Klik op Weergave kopteksten.
    * Als alle regels op de order volledig zijn verzonden, wijzigt de orderstatus van Open naar Geleverd.  
    * In dit voorbeeld is de orderregel gedeeltelijk verzonden. Daarom blijft de orderstatus Open.     
    * Het veld Documentstatus is ingesteld op Pakbon omdat tenminste één van de orderregels is verzonden.  
17. Klik in het actievenster op Algemeen.
18. Klik op Regelhoeveelheid.
19. Sluit de pagina.
20. Klik in het actievenster op Verzamelen en inpakken.
21. Klik op Pakbon.
    * De pagina Pakbonjournaal bevat alle pakbondocumenten die voor uw order werden gegenereerd. U kunt details van elk document controleren en deze desgewenst afdrukken.  


