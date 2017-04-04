---
title: Onkostenbeheer configureren
description: In dit artikel worden de overwegingen en de beslissingen beschreven die u tijdens het planningsproces moet maken voordat u Onkostenbeheer configureert In Microsoft Dynamics AX. In het gebied Onkostenbeheer kunt u onder andere informatie over betalingsmethoden, reisaanvragen, onkostennota&quot;s, opslaan en beleid opslaan.
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 88cdf531b6da615034f9982d3503b9add0100479
ms.lasthandoff: 03/31/2017


---

# <a name="configure-expense-management"></a>Onkostenbeheer configureren

In dit artikel worden de overwegingen en de beslissingen beschreven die u tijdens het planningsproces moet maken voordat u Onkostenbeheer configureert In Microsoft Dynamics AX. In het gebied Onkostenbeheer kunt u onder andere informatie over betalingsmethoden, reisaanvragen, onkostennota's, opslaan en beleid opslaan. 

Omdat veel van de beslissingen die u neemt wanneer u uw configuratie voor Onkostenbeheer plant, zijn gebaseerd op de hiërarchie en financiële structuur van uw organisatie, moet u naar de planningsdocumenten voor die gebieden verwijzen.

## <a name="intercompany-expenses"></a>Intercompany-onkosten
Wanneer u intercompany-onkosten inschakelt, stelt u rechtspersonen en werknemers in staat onkosten te maken namens, en te innen van, een andere rechtspersoon in uw organisatie. Een werknemer in rechtspersoon A rondt bijvoorbeeld een project voor rechtspersoon B af. Als Intercompany-onkosten zijn ingeschakeld, kan de werknemer vervolgens een urenstaat indienen bij, en betaald worden door, rechtspersoon B. Als uw organisatie niet meerdere rechtspersonen omvat, hoeft u intercompany-onkosten niet in te schakelen. **Beslissing:** wilt u intercompany-onkosten inschakelen?

## <a name="financial-management"></a>Financieel beheer
Onkostenbeheer is sterk geïntegreerd met het financieel beheer van uw organisatie. Veel van uw configuraties voor Onkostenbeheer zijn gebaseerd op de beslissingen die u over de financiën van uw organisatie hebt genomen. In de volgende secties worden de verschillende gebieden beschreven waarvoor planning en beslissingen vereist zijn die zijn gebaseerd op de financiële beslissingen van uw organisatie en de richtlijnen van uw managementteam.

### <a name="per-diems"></a>Dagvergoedingen

U moet de dagvergoeding per werknemer definiëren die uw organisatie biedt. Omdat dagvergoedingen doorgaan worden gebruikt om onkosten, zoals maaltijden, overnachtingen en andere incidentele kosten, te dekken, kunt u regels maken voor de dagvergoeding die uw organisatie aanbiedt. De dagvergoedingstarieven kunnen worden gebaseerd op de tijd van het jaar en/of de reisbestemming. Wanneer u een dagvergoedingsregel definieert, kunt u instellen dat er een percentage van een dagvergoedingstarief wordt ingehouden als een werknemer extra maaltijden of diensten ontvangt. Ook kunt u dagtariefniveaus definiëren om het minimum of maximum aantal toegestane uren voor het dagvergoedingstarief op te geven dat kan worden toegepast op de reis van een werknemer. **Beslissingen:**

-   Standaardregels voor dagvergoedingen voor de eerste en laatste dagen:
    -   Wat is het minimum aantal uren dat een werknemer voor een dag kan claimen als deze ook nog een dagvergoeding wil ontvangen?
    -   Geldt er een reductie voor het bedrag dat voor maaltijden wordt aangeboden voor de eerste en laatste dag? Zo ja, wat is het percentage van de reductie?
    -   Geldt er een reductie voor het bedrag dat voor een hotel wordt aangeboden voor de eerste en laatste dag? Zo ja, wat is het percentage van de reductie?
    -   Geldt er een reductie voor het bedrag dat voor overige gemaakte onkosten wordt aangeboden voor de eerste en laatste dag? Zo ja, wat is het percentage van de reductie?
-   Standaardregels voor dagvergoedingen:
    -   Geldt er een percentagereductie voor de dagvergoeding voor elke maaltijd als de maaltijd bijvoorbeeld gratis is? Zo ja, wat is dan het reductiepercentage voor elke maaltijd?
    -   Wordt de maaltijdreductie berekend per dag, reis of het aantal maaltijden per dag?
    -   Moeten dagvergoedingen normaal of naar boven afgerond worden?
    -   Worden dagvergoedingen berekend op basis van een periode van 24 uur of op een kalenderdag?
-   Dagvergoedingsregels op basis van locatie:
    -   Variëren dagvergoedingstarieven op basis van locatie en welke locaties zijn opgenomen?
    -   Welk percentagebedrag wordt voor elke locatie geleverd als het dagvergoedingstarief varieert op basis van locatie:
        -   maaltijden
        -   hotel
        -   overige uitgaven

### <a name="expense-management-journals-and-accounts"></a>Journalen en rekeningen voor onkostenbeheer

Onkostenbeheer vereist dat u meerdere journalen en rekeningen gebruikt. U moet bijvoorbeeld bepalen of voor kasvoorschotten en creditcardgeschillen dezelfde rekening moet worden gebruikt. **Beslissingen:**

-   Naar welk grootboekjournaal worden goedgekeurde onkostennota's geboekt?
-   Welke rekening wordt gebruikt voor kasvoorschotten?
-   Moeten kasvoorschotten onmiddellijk worden geboekt?

### <a name="payment-methods"></a>Betalingsmethoden

Als u werknemers toestemming geeft om onkosten namens uw bedrijf te maken, moet u de betalingsmethoden definiëren die werknemers kunnen gebruiken. U kunt werknemers bijvoorbeeld toestemming geven contant geld of een zakelijke creditcard te gebruiken. U kunt werknemers ook toestemming geven om persoonlijke creditcards te gebruiken en de werknemers vervolgens terugbetalen. U moet de volgende beslissingen nemen voor elke betalingsmethode die u toestaat. **Beslissingen:**

-   Welke betalingsmethoden zijn toegestaan?
-   Wie betaalt de onkosten voor de betalingsmethode?
-   Is er een soort tegenrekening? Zo ja, welke?
-   Wat is de tegenrekening, indien van toepassing?
-   Kan de betalingsmethode alleen voor geïmporteerde transacties worden gebruikt als de betalingsmethode een creditcard is?

### <a name="expense-categories-and-shared-categories"></a>Onkostencategorieën en gedeelde categorieën

Wanneer werknemers een onkostennota maken, moeten alle geregistreerde onkosten aan een onkostencategorie worden gekoppeld. Onkostencategorieën worden afgeleid van gedeelde categorieën die door alle rechtspersonen in uw organisatie kunnen worden gebruikt. Deze categorieën kunnen ook in Projectbeheer en boekhouding worden gedeeld, afhankelijk van hoe uw organisatie is gedefinieerd. Bepaal op basis van de definitie van uw organisatie en richtlijnen van het implementatieteam of de gebruikte categorieën voor onkostenbeheer alleen in Onkosten moeten worden gebruikt of moeten worden gedeeld tussen Project en Onkosten. Deze categorieën kunnen tussen Project en Onkosten of Project en Productie worden gedeeld, maar niet tussen Onkosten en Productie. U moet de volgende beslissingen nemen voor elke onkostencategorie. **Beslissingen:**

-   Wat is de onkostencategorie? Dit kan bijvoorbeeld vluchten, hotel of kilometervergoeding zijn.
-   Kan deze onkostencategorie ook worden gebruikt in Projectbeheer en boekhouding?
-   Wat is het onkostentype?
-   Wat is de standaardbetalingsmethode voor de onkostencategorie?
-   Moeten onkosten in deze categorie worden gespecificeerd?
-   Wat is de belangrijkste standaardrekening voor de onkostencategorie?
-   Wat is de standaard btw-groep voor artikelen voor de onkostencategorie?
-   Zijn extra betalingsmethoden toegestaan voor de onkostencategorie? Zo ja, welke?
-   Zijn er subcategorieën binnen deze onkostencategorie? Zo ja:
    -   Zijn er subcategorieën uitgesloten van btw-teruggave?
    -   Wat is de btw-groep voor artikelen van de subcategorieën?

    Als deze onkostencategorie ook in Projectbeheer en boekhouding wordt gebruikt, moet u ook de resterende vragen beantwoorden. In het andere geval bent u klaar met deze sectie.
-   Welke kostenrekeningen worden voor het volgende gebruikt?
    -   Kosten
    -   Salaristoewijzing
    -   OHW - kostprijs
    -   Kosten - artikel
    -   OHW - kostprijs - artikel
    -   Transitorisch verlies
    -   OHW - transitorisch verlies
-   Welke opbrengstrekeningen worden voor het volgende gebruikt?
    -   Gefactureerde opbrengst
    -   Transitorische opbrengsten - verkoopwaarde
    -   OHW - verkoopwaarde
    -   Transitorische opbrengsten - productie
    -   OHW - productie
    -   Transitorische opbrengsten - winst
    -   OHW - winst
    -   Transitorische opbrengsten - abonnement
    -   OHW - abonnement

 

### <a name="taxes"></a>Belasting

Voor btw gerelateerd aan onkosten moet u bepalen wat wordt opgenomen of ingeschakeld op onkostennota's. **Beslissingen:**

-   Is btw inbegrepen in de onkostenbedragen?
-   Moet btw-teruggave worden ingeschakeld voor onkosten?

Als u tijdens de planning van het grootboek hebt besloten Amerikaanse btw- en gebruiksbelastingregels toe te passen, door het veld **Belastingregels btw toepassen** in te stellen op Ja, kunt u geen btw-teruggave voor onkosten inschakelen.

## <a name="policies"></a>Beleidsrichtlijnen
U kunt beleid voor onkostennota's maken zodat uw organisatie tijd en geld kan besparen wanneer werknemers onkosten maken namens het bedrijf. Beleid zorgt ervoor dat werknemers binnen het budget blijven, alle vereiste gegevens doorgeven en alleen waar nodig geld uitgeven. U moet de volgende beslissingen nemen voor elk gemaakt beleid en goedkeuringsbeleid voor onkostennota's. **Beslissingen:**

-   Wat is de naam van het beleid?
-   Waarvoor is het onkostenbeleid bedoeld?
-   Op welke bedrijven in uw organisatie is dit beleid van toepassing als u eerder hebt besloten intercompany-onkosten in te schakelen?
-   Wanneer gaat het beleid in?
-   Wanneer verloopt het beleid?
-   Wat is de beleidsregel?
-   Wat is de uitkomt van de beleidsregel?



