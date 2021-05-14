---
title: Overzicht module Kortingsbeheer
description: In dit onderwerp vindt u een overzicht van de module Kortingsbeheer voor Microsoft Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 7917f36d8ff3c1ae2d37c5390806ef82771b5211
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920032"
---
# <a name="rebate-management-module-overview"></a>Overzicht module Kortingsbeheer

[!include [banner](../includes/banner.md)]

U kunt de module **Kortingsbeheer** gebruiken om contracten, deals of overeenkomsten te maken tussen uw bedrijf en zijn klanten of leveranciers, zodat u kortingen, inhoudingen en royalty's kunt berekenen. Kortingsbeheer volgt en onderhoudt kortings- en aftrektransacties op een centrale locatie waar gebruikers ze effectief kunnen maken, controleren en verwerken.

Kortingsbeheer ondersteunt het maken, onderhouden en verwerken van *kortingen*. Een korting is het teruggeven van een deel van de inkoopprijs door een verkoper of een koper. Kortingen zijn meestal gebaseerd op de aankoop van een specifieke hoeveelheid of waarde van goederen gedurende een bepaalde periode. In tegenstelling tot kortingen vooraf worden kortingen verstrekt nadat het aankoopbedrag volledig is gefactureerd.

Kortingsbeheer ondersteunt ook *inhoudingen*. Een inhouding is compensatie of een vergoeding die wordt betaald voor een licentie of het voorrecht om intellectueel eigendom zoals een merk, auteursrecht of octrooi te gebruiken, of voor het voorrecht om een natuurlijke hulpbron te gebruiken voor een doel zoals visserij, jacht of mijnbouw. Inhoudingen worden meestal berekend als een percentage van de opbrengst of winst uit gerealiseerd gebruik. Hoe meer het intellectuele eigendom of de natuurlijke hulpbron wordt gebruikt, hoe groter de inhouding die wordt gerealiseerd.

Daarnaast ondersteunt Kortingsbeheer *royalty's* van klanten. Royalty's zijn betalingen die één partij doet aan de licentienemer of franchisenemer voor het recht om een activum te gebruiken.

Met kortingsbeheer kunt u boekingsprofielen definiëren voor voorzieningen, kortingen en afschrijvingen. Bovendien kunnen de boekingen worden gedefinieerd voor een specifieke klant of leverancier. Op deze manier kunnen deals die niet op alle klant- of leveranciersscenario's van toepassing zijn, worden bijgehouden via boekingen.

Kortingstransacties worden automatisch gegenereerd op basis van de berekeningsmethode die is geselecteerd en gepland in batchtaken. Daarnaast kunt u werkstromen instellen voor het beheren, controleren en goedkeuren van overeenkomsten.

## <a name="basis-calculation"></a>Basisberekening

Klantkortingen, klantroyalty's en leverancierskortingen kunnen allemaal een andere basis gebruiken, afhankelijk van uw zakelijke vereisten:

- Klantkortingen kunnen worden gebaseerd op verkooporders, afleveringsbewijzen of facturen.
- Klantroyalty's kunnen worden gebaseerd op verkooporders, afleveringsbewijzen of betaalde facturen.
- Leverancierskortingen kunnen worden gebaseerd op inkooporders of verkooporders. Ze kunnen worden berekend op basis van producten die bij de kortingsleverancier zijn gekocht en via verkoopfacturen aan klanten worden verkocht.

## <a name="flexible-calculations"></a>Flexibele berekeningen

Kortingsberekeningsperioden zijn beschikbaar voor zowel klantdeals als leveranciersdeals. Een berekeningsperiode definieert de lengte van de deal, de berekeningsfrequentie en de berekeningsperiode. De kortingen kunnen worden toegerekend op basis van de verkooporderhoeveelheden of -bedragen voor gekwalificeerde producten tijdens de kortingsperiode.

Voor elke overeenkomstberekening kunnen een van de volgende perioden worden ingesteld:

- Factuur
- Dag
- Week
- Maand
- Kwartaal
- Jaar
- Aangepaste periode
- Elk veelvoud van een van de eerder vermelde perioden

De berekening kan worden toegepast op afzonderlijke klanten en producten, groepen klanten en producten of op alle klanten en producten. Kortingen met meerdere detailregels kunnen verschillende datumbereiken voor kwalificatie hebben. De voorzienings- en claimperioden kunnen verschillen. Zo kunnen voorzieningen elke dag worden verwerkt, terwijl claims eenmaal per maand worden verwerkt.

Kortingen kunnen worden geconfigureerd op basis van een groot aantal verschillende parameters. Deze kunnen bijvoorbeeld worden geconfigureerd als een percentage, een tarief of een vast bedrag. Er zijn vier hoofdberekeningsmethoden:

- Getrapt
- Cumulatief
- Opvolgend
- Totale waarde

Het resultaat van kortingsberekeningen kan ook worden verminderd met andere kortingen, afhankelijk van of de korting kan worden berekend op basis van het nettobedrag.

Voor de leverancier kunnen kortingen de prijs berekenen op basis van een FIFO-regel (First In, First Out), de meest recente inkoopprijs, de gemiddelde inkoopprijs of de verkoopprijs.

## <a name="rebate-target-transactions"></a>Kortingsdoeltransacties

De uitvoer die door de kortingsdeal of overeenkomst wordt gegenereerd, kan financieel of in artikelen zijn.

Financiële uitvoer wordt bepaald door het betalingstype dat aan de overeenkomst is toegewezen op basis van het boekingsprofiel. Deze uitvoer kan klantinhoudingsjournaal, vrije-tekstfacturen en leveranciersfacturen bevatten. Voor controledoeleinden bevatten doeltransacties voor financiële kortingen een verwijzing naar de oorspronkelijke kortingsovereenkomst.

Met artikeluitvoer wordt een vrije artikelverkooporder voor klantkortingen en een inkooporder voor leverancierskortingen gemaakt. Artikelkortingsdoeltransacties bevatten opties om te bepalen welke kortingsverwijzing moet worden ingevoerd op de vrije artikelverkooporder of -inkooporder.

## <a name="accurate-rebate-calculations"></a>Nauwkeurige kortingsberekeningen

De combinatie van de gekoppelde acties, de frequentie van de berekeningen, de berekeningsbasis en de geselecteerde berekeningsmethode bepaalt de nauwkeurigheid en precisie van kortingsberekeningen. Met kortingsvoorzieningen kunnen geboekte en geclaimde waarden worden toegerekend.

Voorzieningen kunnen dagelijks of maandelijks worden beheerd. Met de functionaliteit kan de korting echter met elke gedefinieerde frequentie worden toegewezen, betaald of ontvangen. Gebruikers kunnen op elk moment tijdens de uitbetaling eenvoudig een plan of betalingsbedragen aanpassen.

Gebruikers hoeven niet langer deals of voorzieningen in twee stappen te verwerken. Voorzieningen en afschrijvingen worden rechtstreeks naar het grootboek geboekt. Verder kunnen er automatisch creditnota's worden gemaakt. Daarom is er volledige integratie met leveranciers en klanten. Tijdens de verwerking worden vereffeningskortingen, betaalde facturen, handelskortingen en bestaande creditnota's meegenomen om er zeker van te zijn dat bedragen en waarden correct worden berekend.

Wanneer kortingen worden berekend, worden transacties gemaakt die kunnen worden gecontroleerd voordat de boeking plaatsvindt. Er kan vervolgens een journaal, creditnota of debettransactie worden gemaakt. Kortings- en inhoudingstransacties worden met een afzonderlijk proces geboekt. Rapportageoverzichten en transactielijsten kunnen worden verkregen om conformiteit, effectiviteit en transparantie te garanderen.

## <a name="guaranteed-royalty-payments"></a>Gegarandeerde royaltybetalingen

In Kortingsbeheer kunnen bij het automatisch genereren van betalingen de royalty's snel en eenvoudig worden verwerkt, zelfs wanneer er minimale kortingen van toepassing zijn. 

## <a name="maximizing-spend-versus-rebates"></a>Uitgaven versus kortingen maximaliseren

Leveranciers en producten kunnen per rayon worden gegroepeerd en er kunnen verschillende aanbiedingen worden geboden, afhankelijk van het land of de regio waar de transactie zich bevindt. Wanneer gebruikers producten selecteren, kunnen ze de artikelen definiëren die worden opgenomen en het aantal artikelen dat wordt gebruikt in de kortingsregeling.
