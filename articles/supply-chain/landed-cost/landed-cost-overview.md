---
title: De module Francoprijzen
description: Met de module Francoprijzen kunnen bedrijven beter hun inkomende verzendbewerkingen stroomlijnen door gebruikers de volledige financiële en logistieke controle te geven over geïmporteerde vracht, van fabrikant tot magazijn.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e4861c0e8b3680f3cd3229facf059b671a4fc765
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983412"
---
# <a name="landed-cost-module"></a>De module Francoprijzen

[!include [banner](../../includes/banner.md)]

Met de module **Francoprijzen** kunnen bedrijven beter hun inkomende verzendbewerkingen stroomlijnen door gebruikers de volledige financiële en logistieke controle te geven over geïmporteerde vracht, van fabrikant tot magazijn. Voor geïmporteerde goederen kunnen francoprijzen 40 procent of meer van de totale kosten van elk geïmporteerd artikel uitmaken. Daarom is het de uitdaging om nauwkeurige schattingen te maken voor francoprijzen.

Bedrijven kunnen Francoprijzen gebruiken om de volgende taken uit te voeren:

- De francoprijzen schatten op het moment dat ze een reis maken.
- De francoprijzen verdelen over meerdere artikelen en inkooporders of overboekingsorders in één reis.
- De overdracht van goederen ondersteunen tussen fysieke locaties door de francoprijzen te herkennen.
- Toerekeningen herkennen voor goederen in transit.

Francoprijzen biedt nauwkeurige en tijdige kostenramingen voor overhead van francoprijzen. Tegelijkertijd zorgen francoprijzen voor meer financiële en logistieke inzichten in de uitgebreide toeleveringsketen. Hierdoor kunnen ook het beheer van kostprijsberekeningen en fouten bij kostprijsberekeningen worden verminderd.

## <a name="highlights"></a>Hoogtepunten

### <a name="voyages"></a>Reizen

In Francoprijzen is een reis een afzonderlijke verplaatsing van een uitgaande locatie, via een specifieke reeks bestemmingen gedurende een bepaalde periode, naar een opgegeven locatie van een magazijn voor inkomende goederen. Inkooporders en orderregels kunnen voor een reis worden toegevoegd aan één container of aan meerdere containers en de kosten worden weer correct toegewezen aan de artikelregel. Orders en orderregels kunnen ook worden toegevoegd aan rechtspersonen voor één reis.

### <a name="item-ownership"></a>Artikeleigendom

In Microsoft Dynamics 365 Supply Chain Management worden goederen doorgaans ontvangen op de magazijnbestemming en vervolgens gefactureerd. In het kader van de meeste internationale handelsovereenkomsten wordt een bedrijf echter eigenaar van goederen vanaf het moment dat ze de oorspronkelijke haven verlaten, voordat ze fysiek zijn ontvangen. Met Francoprijzen kunnen bedrijven goederen factureren voordat ze fysiek zijn ontvangen. Dit concept staat bekend als een order voor goederen in transit. Er wordt een nieuw type order gemaakt om de ontvangst van goederen te beheren nadat de oorspronkelijke inkooporder is gefactureerd.

### <a name="costs"></a>Kosten

Wanneer u een reis maakt in Francoprijzen, kunnen er automatisch kosten aan worden toegevoegd. Deze kosten zijn ingesteld in Francoprijzen en er zijn verschillende kostenopties en kostenbasissen voor deze kosten beschikbaar. Alle kosten kunnen worden ingesteld voor verschillende niveaus van een reis en worden verdeeld over het artikelniveau via verdelingsregels die hoeveelheid, volume, gewicht, hoeveelheid en gedefinieerde volumetrische delers ondersteunen. Deze geschatte kosten geven een nauwkeurige schatting van alle kosten voor een reis.

Met Francoprijzen wordt vervolgens een voorlopige boeking/toerekening van de geraamde francoprijzen uitgevoerd om ervoor te zorgen dat er een nauwkeurige berekening van de geraamde kosten wordt verstrekt op het moment dat de reis wordt gemaakt. Omdat deze automatische kosten worden gefactureerd, worden de geschatte kosten teruggeboekt en vervangen door de werkelijke kosten, op basis van kostenfacturen.

Werkelijke kosten zijn teruggeboekte geschatte kosten die worden geboekt op het moment van kostenfacturering met behulp van vereffeningsrekeningen die zijn ingesteld voor elk type kosten (bijvoorbeeld heffingen, vracht en verzekering). Bij deze boekingen wordt het boekingsgedrag gebruikt dat aan het specifieke item is gekoppeld. Ze werken automatisch voorraadboeking bij, ongeacht of het boekingstype FIFO (First In, First Out), LIFO (Last In First Out), zwevend gewogen gemiddelde of zwevend gemiddelde is. Alle boekingstypen van voorraadmodelgroepen worden ondersteund. Voor het boeken van zwevende gemiddelden en standaardkosten zijn verschillenrekeningen voor inkoopprijzen beschikbaar om de verschillen tussen geschatte kosten en werkelijke kosten te boeken.

### <a name="item-and-order-tracking"></a>Artikel- en ordertracering

Wanneer een reis van de oorspronkelijke uitgaande locatie naar het uiteindelijke doelmagazijn gaat, kunnen gebruikers elke stap of *etappe* van het traject naar behoefte bijwerken. Voor elke etappe wordt een doorlooptijd en een verzendstatus geïdentificeerd. Bevestigde leveringsdatums voor verplaatsing naar de volgende etappe van het traject worden ook geïdentificeerd. Samen bieden deze leveringsdatums een geschatte leveringsdatum van de goederen naar het inkomende magazijn. Gebruikers kunnen deze leveringsdatums wijzigen. In dit geval wordt de geschatte leveringsdatum van de goederen automatisch bijgewerkt, op basis van de doorlooptijden en etappes van het traject. Het inzicht in goederen in transit per reis en per vaartuig is beschikbaar per container voordat de goederen worden ontvangen. Omdat de datums op elke inkooporderregel worden bijgewerkt, hebben bedrijven meer controle over de logistiek en magazijnplanning.

## <a name="landed-cost-concepts"></a>Concepten voor Francoprijzen

In de volgende tabel wordt een overzicht gegeven van enkele kernbegrippen van Francoprijzen.

| Concept | Beschrijving |
|---|---|
| Reis | Doorgaans is een reis één vaartuig. Afhankelijk van uw werkwijzen en procedures kan dit echter één leverancier of één inkooporder zijn. Er gelden geen beperkingen voor het gebruik van dit concept. |
| Folio | Een folio wordt vaak bepaald door douanevoorschriften. Deze kan bestaan uit goederen van één leverancier voor één entiteit/bedrijf per zending. De goederen in een folio kunnen zich in één container bevinden of zijn verdeeld over meerdere containers. |
| container | Met containers worden inkooporderregels opgeslagen. Ze bevinden zich één niveau lager dan het verzendniveau. Ze worden meestal gebruikt als de kosten voor goederen per container worden verdeeld of als de ontvangst per container wordt gedaan. |
| Type container | De typen container kunnen de prijs voor een kostentype (bijvoorbeeld vracht) bepalen. Ze bieden ook nuttige verzendinformatie. |
| Kostentype | Kostentypen identificeren kosten die zijn gekoppeld aan invoer, zoals invoerkosten, vracht en verzekeringen. |
| Automatische kosten | Autokosten werken als handelsovereenkomsten. Autokosten zijn gekoppeld aan een reisniveau. |
| Haven | Havens zijn gebieden waar goederen worden ontvangen en overgedragen. |
| Vaartuig | Een vaartuig is het medium dat wordt gebruikt om goederen te vervoeren, zoals een schip of een vliegtuig. |
| Goederen in transit | Afhankelijk van de instellingen, worden goederen in een transitmagazijn geplaatst nadat een factuur is bijgewerkt. |
| Activiteit | Activiteiten kunnen worden gebruikt om elke belangrijke stap van het traject tussen twee havens op te slaan. Ze kunnen worden gebruikt om datums bij te werken. |
| Trajectsjabloon | Trajectsjablonen zijn routes die goederen afleggen tussen twee havens. |

Zie voor een vergelijking van de terminologie en functies van de modules **Francoprijzen** en **Transportbeheer** (TMS) het onderwerp [Francoprijzen versus Transportbeheer](landed-cost-vs-tms.md).
