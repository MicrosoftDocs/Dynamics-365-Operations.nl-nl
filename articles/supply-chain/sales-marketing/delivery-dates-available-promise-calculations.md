---
title: Orderbelofte
description: In dit artikel vindt u informatie over het uitvoeren van ordertoezeggingen (orderbeloftes). Als u gebruikt maakt van orderbeloftes, kunt u met zekerheid leveringsdatums aan uw klanten beloven en hebt u de flexibiliteit dat u deze datums ook haalt.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 039bc5c572d204d9fa3e10a9f33cb4f4eb00b31c
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="order-promising"></a>Orderbelofte

[!INCLUDE [banner](../includes/banner.md)]

In dit artikel vindt u informatie over het uitvoeren van ordertoezeggingen (orderbeloftes). Als u gebruikt maakt van orderbeloftes, kunt u met zekerheid leveringsdatums aan uw klanten beloven en hebt u de flexibiliteit dat u deze datums ook haalt.

Met orderbelofte worden de vroegste verzend- en ontvangstdatum berekend. De functie is gebaseerd op de controlemethode voor de leveringsdatum en op de transportdagen. U kunt onder kiezen uit vier controlemethoden voor de leveringsdatum:

-   **Verkooplevertijd**: de verkooplevertijd is de tijd tussen het maken van de verkooporder en de zending van de artikelen. De berekening van de leveringsdatum is gebaseerd op een standaardaantal dagen waarbij geen rekening wordt gehouden met voorraadbeschikbaarheid, bekende vraag of gepland aanbod.
-   **ATP (available-to-promise)**: vrije voorraad (ATP) is de hoeveelheid van een artikel, die beschikbaar is en aan een klant kan worden beloofd op een specifieke datum. Bij de ATP-berekening worden niet-toegezegde voorraad, levertijden, geplande ontvangsten en uitgiften gebruikt.
-   **ATP + uitgiftemarge**: De verzenddatum is gelijk aan de ATP-datum plus de uitgiftemarge voor het artikel. De uitgiftemarge is de tijd die nodig is voor het voorbereiden van artikelen voor verzending.
-   **CTP (capable-to-promise)**: Beschikbaarheid wordt berekend door middel van explosie.

## <a name="atp-calculations"></a>Berekening van de vrije voorraad (ATP)
De hoeveelheid vrije voorraad wordt berekend met de methode "cumulatieve vrije voorraad met vooruitblik". Het belangrijkste voordeel van deze berekeningsmethode van vrije voorraad is dat hiermee aanvragen kunnen worden verwerkt waarbij de som van de uitgiften tussen ontvangsten meer is dan de laatste ontvangst (bijvoorbeeld wanneer een hoeveelheid van een eerdere ontvangst moet worden gebruikt om te voldoen aan een behoefte). De berekeningsmethode van de 'cumulatieve vrije voorraad met vooruitblik' bevat alle uitgiften totdat de cumulatieve te ontvangen hoeveelheid groter is dan de cumulatieve uit te geven hoeveelheid. Daarom kijkt deze berekening van de vrije voorraad of een gedeelte van de vrijevoorraadhoeveelheid uit een eerdere periode kan worden gebruikt voor een latere periode.  

De vrije voorraad is de niet-toegezegde voorraadbalans in de eerste periode. Deze wordt normaal berekend voor elke periode waarin een ontvangst is gepland. De vrijevoorraadperiode wordt berekend in dagen en de huidige datum wordt berekend als de eerste datum voor de hoeveelheid vrije voorraad. In de eerste periode is de vrije voorraad gelijk aan de voorhanden voorraad minus de klantorders die moeten worden geleverd of die achterstallig zijn.  

De vrije voorraad wordt berekend met de volgende formule:  

Vrije voorraad = vrije voorraad voor de vorige periode + ontvangsten voor de huidige periode - uitgiften voor de huidige periode - de netto-uitgiftehoeveelheid voor elke toekomstige periode totdat de periode waarvoor de som van de ontvangsten voor alle toekomstige perioden, tot en met de toekomstige periode, groter is dan de som van de uitgiften, tot en met de toekomstige periode.  

Wanneer er geen uitgiften of ontvangsten meer zijn om te verwerken, is de hoeveelheid vrije voorraad gelijk aan de hoeveelheid die als laatste is berekend.  

Als niet alle dimensies die voor een artikel worden gebruikt, zijn ingevoerd wanneer de vrijevoorraadcontrole wordt uitgevoerd, kunnen deze alsnog worden ingevoerd tijdens de uitgifte of ontvangst. In dit geval moeten de ontvangsten en uitgiften tijdens de berekening van de vrije voorraad worden opgeteld bij de bestaande dimensies om het aantal ontvangst- en uitgifteregels te beperken dat wordt gebruikt in de berekening van de vrije voorraad.  

De hoeveelheid vrije voorraad die wordt weergegeven is altijd groter dan of gelijk aan 0 (nul). Als een negatieve hoeveelheid vrije voorraad wordt geretourneerd (bijvoorbeeld als de eerder toegezegde hoeveelheid groter is dan de beschikbare hoeveelheid), wordt de hoeveelheid automatisch ingesteld op **0**.

### <a name="example"></a>Voorbeeld

Het veld **Time fence voor achterwaartse vraag ATP** controleert hoe ver terug in de tijd kan worden gezocht naar uitgestelde vraagorders of voorraaduitgiften. Het veld **Time fence voor achterwaarts aanbod ATP** controleert hoe ver terug in de tijd kan worden gezocht naar uitgestelde aanbodorders of voorraadontvangsten. Als bijvoorbeeld orders die slechts zeven dagen zijn uitgesteld moeten worden meegenomen in de vrijevoorraadberekening, moeten beide velden worden ingesteld op **7**.  

De velden **Offsettijd voor uitgestelde vraag ATP** en **Offsettijd voor uitgesteld aanbod ATP** bepalen wanneer de uitgestelde vraag of levering in de berekening van de vrije voorraad wordt meegenomen. Als bijvoorbeeld de uitgestelde vraag en aanbod overmorgen moeten worden meegenomen in de berekening van de vrije voorraad, moeten beide velden zijn ingesteld op **2**. De waarde **2** betekent dat de hoeveelheid van een artikel voor een uitgestelde inkooporder die moet worden meegenomen in de berekening van de vrije voorraad, twee dagen na de huidige datum wordt beschouwd als beschikbaar.  

In het volgende voorbeeld wordt **7** ingevoerd in de velden **Time fence voor achterwaartse vraag ATP** en **Time fence voor achterwaarts aanbod ATP**, en **1** in de velden **Offsettijd voor uitgesteld aanbod ATP** en **Offsettijd voor uitgestelde vraag ATP**.  

Een inkooporder voor 200 stuks van een product dat al drie dagen geleden binnen moest zijn, is nog steeds niet ontvangen. Hierdoor kon een verkooporderregel voor 75 stuks van dit product, die gisteren moest zijn verzonden, nog niet worden verzonden.  

Een klant belt en wil 150 stuks van hetzelfde product bestellen. U controleert de beschikbaarheid van het product en vindt een andere inkooporder voor 100 stuks van het product, die 10 dagen later wordt geleverd.  

U maakt een verkooporderregel aan voor het product en voert als hoeveelheid **150** in.  

Omdat de controlemethode voor de leveringsdatum ATP is, worden de vrijevoorraadgegevens berekend om de vroegst mogelijke verzenddatum te bepalen. Op basis van de instellingen worden de uitgestelde inkooporder en verkooporder meegenomen en is de resulterende hoeveelheid vrije voorraad voor de huidige datum 0. Morgen, wanneer de uitgestelde inkooporder naar verwachting wordt ontvangen, wordt de hoeveelheid vrije voorraad berekend als meer dan 0 (in dit geval wordt deze berekend als 125). Echter, 10 dagen vanaf nu, wanneer de aanvullende inkooporder voor 100 stuks naar verwachting wordt ontvangen, wordt de hoeveelheid vrije voorraad meer dan 150.  

Daarom wordt de verzenddatum ingesteld op 10 dagen vanaf nu, gebaseerd op de berekening van de vrije voorraad. U kunt de klant daarom vertellen dat het gevraagde aantal kan worden geleverd binnen 10 dagen na nu.




