---
title: Orderbelofte
description: In dit artikel vindt u informatie over het uitvoeren van ordertoezeggingen (orderbeloftes). Als u gebruikt maakt van orderbeloftes, kunt u met zekerheid leveringsdatums aan uw klanten beloven en hebt u de flexibiliteit dat u deze datums ook haalt.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228261"
---
# <a name="order-promising"></a>Orderbelofte

[!include [banner](../includes/banner.md)]

In dit artikel vindt u informatie over het uitvoeren van ordertoezeggingen (orderbeloftes). Als u gebruikt maakt van orderbeloftes, kunt u met zekerheid leveringsdatums aan uw klanten beloven en hebt u de flexibiliteit dat u deze datums ook haalt.

Met orderbelofte worden de vroegste verzend- en ontvangstdatum berekend. De functie is gebaseerd op de controlemethode voor de leveringsdatum en op de transportdagen. U kunt onder kiezen uit de volgende controlemethoden voor de leveringsdatum:

- **Verkooplevertijd**: de verkooplevertijd is de tijd tussen het maken van de verkooporder en de zending van de artikelen. De berekening van de leveringsdatum is gebaseerd op een standaardaantal dagen waarbij geen rekening wordt gehouden met beschikbaarheid van voorraad, bekende vraag of gepland aanbod.
- **ATP (available-to-promise)**: vrije voorraad (ATP) is de hoeveelheid van een artikel, die beschikbaar is en aan een klant kan worden beloofd op een specifieke datum. Bij de ATP-berekening worden niet-toegezegde voorraad, levertijden, geplande ontvangsten en uitgiften gebruikt.
- **ATP + uitgiftemarge**: De verzenddatum is gelijk aan de ATP-datum plus de uitgiftemarge voor het artikel. De uitgiftemarge is de tijd die nodig is voor het voorbereiden van artikelen voor verzending.
- **CTP (capable-to-promise)**: Beschikbaarheid wordt berekend door middel van explosie. Als u Planningsoptimalisatie gebruikt, is de controlemethode voor de *CTP*-leveringsdatum niet toegestaan en wordt bij het uitvoeren van de berekening een foutbericht weergegeven als deze methode is geselecteerd. Raadpleeg [Leveringsdatums van verkooporders berekenen met behulp van CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) voor meer informatie over het instellen en gebruiken van CTP.
- **CTP voor planningsoptimalisatie**: gebruik de CTP-berekening die wordt geleverd door Planningsoptimalisatie. Deze optie heeft geen effect als u de ingebouwde hoofdplanning-engine gebruikt. Raadpleeg [Leveringsdatums van verkooporders berekenen met behulp van CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) voor meer informatie over het instellen en gebruiken van CTP.

> [!NOTE]
> Wanneer een verkooporder wordt bijgewerkt, worden de ordertoezeggingsgegevens alleen bijgewerkt als er niet kan worden voldaan aan de bestaande ordertoezeggingsdatum, zoals in de volgende voorbeelden:
>
> - **Voorbeeld 1**: de huidige ordertoezeggingsdatum is 20 juli, maar als gevolg van een toegenomen hoeveelheid kunt u niet leveren vóór 25 juli. Omdat de huidige datum niet meer kan worden gehaald, wordt de ordertoezegging geactiveerd.
> - **Voorbeeld 2**: de huidige ordertoezeggingsdatum is 20 juli, maar als gevolg van afgenomen hoeveelheid kan nu op 15 juli worden geleverd. Omdat de huidige datum echter nog kan worden gehaald, wordt de ordertoezegging niet geactiveerd en blijft 20 juli de ordertoezeggingsdatum.

## <a name="atp-calculations"></a>Berekening van de vrije voorraad (ATP)

De hoeveelheid vrije voorraad wordt berekend met de methode 'cumulatieve vrije voorraad met vooruitblik'. Het belangrijkste voordeel van deze berekeningsmethode van vrije voorraad is dat hiermee aanvragen kunnen worden verwerkt waarbij de som van de uitgiften tussen ontvangsten meer is dan de laatste ontvangst (bijvoorbeeld wanneer een hoeveelheid van een eerdere ontvangst moet worden gebruikt om te voldoen aan een behoefte). De berekeningsmethode van de 'cumulatieve vrije voorraad met vooruitblik' bevat alle uitgiften totdat de cumulatieve te ontvangen hoeveelheid groter is dan de cumulatieve uit te geven hoeveelheid. Daarom kijkt deze berekening van de vrije voorraad of een gedeelte van de vrijevoorraadhoeveelheid uit een eerdere periode kan worden gebruikt voor een latere periode.

De vrije voorraad is de niet-toegezegde voorraadbalans in de eerste periode. Deze wordt normaal berekend voor elke periode waarin een ontvangst is gepland. De vrijevoorraadperiode wordt berekend in dagen en de huidige datum wordt berekend als de eerste datum voor de hoeveelheid vrije voorraad. In de eerste periode is de vrije voorraad gelijk aan de voorhanden voorraad minus de klantorders die moeten worden geleverd of die achterstallig zijn.

De vrije voorraad wordt berekend met de volgende formule:

Vrije voorraad = vrije voorraad voor de vorige periode + ontvangsten voor de huidige periode - uitgiften voor de huidige periode - de netto-uitgiftehoeveelheid voor elke toekomstige periode totdat de periode waarvoor de som van de ontvangsten voor alle toekomstige perioden, tot en met de toekomstige periode, groter is dan de som van de uitgiften, tot en met de toekomstige periode.

De berekening van de vrije voorraad bevat geen informatie over de vervaldatum en na de ATP-time fence die het systeem verwacht voor het toezeggen van een hoeveelheid.

Wanneer er geen uitgiften of ontvangsten meer zijn om te verwerken, is de hoeveelheid vrije voorraad gelijk aan de hoeveelheid die als laatste is berekend.

Als niet alle dimensies die voor een artikel worden gebruikt, zijn ingevoerd wanneer de vrijevoorraadcontrole wordt uitgevoerd, kunnen deze alsnog worden ingevoerd tijdens de uitgifte of ontvangst. In dit geval moeten de ontvangsten en uitgiften tijdens de berekening van de vrije voorraad worden opgeteld bij de bestaande dimensies om het aantal ontvangst- en uitgifteregels te beperken dat wordt gebruikt in de berekening van de vrije voorraad.

De hoeveelheid vrije voorraad die wordt weergegeven is altijd groter dan of gelijk aan 0 (nul). Als een negatieve hoeveelheid vrije voorraad wordt geretourneerd (bijvoorbeeld als de eerder toegezegde hoeveelheid groter is dan de beschikbare hoeveelheid), wordt de hoeveelheid automatisch ingesteld op 0.

### <a name="example"></a>Voorbeeld

Het veld **Time fence voor achterwaartse vraag ATP** controleert hoe ver terug in de tijd kan worden gezocht naar uitgestelde vraagorders of voorraaduitgiften. Het veld **Time fence voor achterwaarts aanbod ATP** controleert hoe ver terug in de tijd kan worden gezocht naar uitgestelde aanbodorders of voorraadontvangsten. Als bijvoorbeeld orders die slechts zeven dagen zijn uitgesteld moeten worden meegenomen in de vrijevoorraadberekening, moeten beide velden worden ingesteld op **7**.

De velden **Offsettijd voor uitgestelde vraag ATP** en **Offsettijd voor uitgesteld aanbod ATP** bepalen wanneer de uitgestelde vraag of levering in de berekening van de vrije voorraad wordt meegenomen. Als bijvoorbeeld de uitgestelde vraag en aanbod overmorgen moeten worden meegenomen in de berekening van de vrije voorraad, moeten beide velden zijn ingesteld op **2**. De waarde **2** betekent dat de hoeveelheid van een artikel voor een uitgestelde inkooporder die moet worden meegenomen in de berekening van de vrije voorraad, twee dagen na de huidige datum wordt beschouwd als beschikbaar.

In het volgende voorbeeld wordt **7** ingevoerd in de velden **Time fence voor achterwaartse vraag ATP** en **Time fence voor achterwaarts aanbod ATP**, en **1** in de velden **Offsettijd voor uitgesteld aanbod ATP** en **Offsettijd voor uitgestelde vraag ATP**.

Een inkooporder voor 200 stuks van een product dat al drie dagen geleden binnen moest zijn, is nog steeds niet ontvangen. Hierdoor kon een verkooporderregel voor 75 stuks van dit product, die gisteren moest zijn verzonden, nog niet worden verzonden.

Een klant belt en wil 150 stuks van hetzelfde product bestellen. U controleert de beschikbaarheid van het product en vindt een andere inkooporder voor 100 stuks van het product, die 10 dagen later wordt geleverd.

U maakt een verkooporderregel aan voor het product en voert als hoeveelheid **150** in.

Omdat de controlemethode voor de leveringsdatum ATP is, worden de vrijevoorraadgegevens berekend om de vroegst mogelijke verzenddatum te bepalen. Op basis van de instellingen worden de uitgestelde inkooporder en verkooporder meegenomen en is de resulterende hoeveelheid vrije voorraad voor de huidige datum 0. Morgen, wanneer de uitgestelde inkooporder naar verwachting wordt ontvangen, wordt de hoeveelheid vrije voorraad berekend als meer dan 0 (in dit geval wordt deze berekend als 125). Echter, 10 dagen vanaf nu, wanneer de aanvullende inkooporder voor 100 stuks naar verwachting wordt ontvangen, wordt de hoeveelheid vrije voorraad meer dan 150.

Daarom wordt de verzenddatum ingesteld op 10 dagen vanaf nu, gebaseerd op de berekening van de vrije voorraad. U kunt de klant daarom vertellen dat het gevraagde aantal kan worden geleverd binnen 10 dagen na nu.

## <a name="ctp-calculations"></a>CTP-berekeningen

Met de CTP-functionaliteit kunt u klanten realistische datums geven voor de datums waarop u specifieke goederen kunt leveren. Voor elke verkoopregel kunt u een datum leveren die rekening houdt met bestaande voorraad, productiecapaciteit en transporttijden.

CTP vergroot de ATP-functionaliteit door rekening te houden met capaciteitsgegevens. Hoewel ATP alleen rekening houdt met de beschikbaarheid van materialen en uitgaat van onbeperkte capaciteitsbronnen, houdt CTP rekening met de beschikbaarheid van zowel materialen als capaciteit. Daarom biedt CTP een realistischer beeld van de vraag of binnen een bepaald tijdsbestek aan vraag kan worden voldaan.

CTP werkt iets anders, afhankelijk van van de engine die voor hoofdplanning wordt gebruikt (Planningsoptimalisatie of de ingebouwde engine). CTP voor Planningsoptimalisatie ondersteunt momenteel alleen een subset van de CTP-scenario's die worden ondersteund door de ingebouwde engine.

Raadpleeg [Leveringsdatums van verkooporders berekenen met behulp van CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) voor gedetailleerde informatie over het instellen en gebruiken van CTP voor elke engine.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
