---
title: Een lean organisatie modelleren
description: Het artikel bevat informatie over de belangrijkste concepten bij het modelleren van een lean organisatie.
author: cvocph
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, KanbanFlowSelection, KanbanFlow
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfc0497286ae0286cde05412c82fcaac76f4042a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837628"
---
# <a name="modeling-a-lean-organization"></a>Een lean organisatie modelleren

[!include [banner](../includes/banner.md)]

Het artikel bevat informatie over de belangrijkste concepten bij het modelleren van een lean organisatie. 

Een lean manufacturingscenario is meestal meer dan alleen een verzameling van niet-verwante kanbanregels of beleidsregels voor materieellevering. De stroom van materialen en producten door werkcellen en locaties voor een bepaald productie- of leveringsscenario kunnen worden beschreven als reeks of klein netwerk van proces- of overdrachtsactiviteiten. Deze reeks of dit netwerk wordt een productiestroom genoemd.

## <a name="production-flows-in-lean-manufacturing"></a>Productiestromen in lean manufacturing
In productiescenario's die zijn gebaseerd op productieorders, worden materialen uitgegeven aan een specifieke productieorder. Tijdens een reeks bewerkingen die is gebaseerd op een stuklijst en routes worden producten gemaakt en ten slotte ontvangen op de verschafte locatie. De doorvoertijd van productieorders varieert in bereiken van minuten tot weken. Alle gerelateerde kosten, materiaal en arbeid worden samengevoegd op de productieorder. 

Om de leveringsdoorlooptijden te verkorten en overmatige voorraad die wordt veroorzaakt door batchproductie tussen werkplaatsen te reduceren, introduceert lean manufacturing kanbanaanvulling en supermarkten in productie en magazijnaanvulling. Deze functies onderbreken meestal de productie van gedeeltelijk onafhankelijke kanbancycli. De aanvulling van een kanban voor een halffabricaat wordt niet meer geactiveerd door een order voor een eindproduct. 

Om een productie- en kostprijs-context te maken voor de verschillende kanbanscenario's die worden voorgesteld, zijn de activiteitgebaseerde productiestromen geïntroduceerd als de basis van lean manufacturing. Alle kanbanregels verwijzen naar deze vooraf gedefinieerde structuur. Het op activiteit gebaseerde model ondersteunt de instelling van een grote verscheidenheid aan scenario's. Dit model voegt echter geen complexiteit toe voor de werkvloerwerknemers, omdat alle scenario's gebruikmaken van dezelfde op activiteiten gebaseerde gebruikersinterface.

## <a name="semi-finished-products-non-bom-levels"></a>Halffabricaten (niet-stuklijstniveaus)
Lean manufacturing integreert kanbans voor geïnventariseerde producten en halffabricaten in één raamwerk, en biedt daarmee een uniforme gebruikerservaring voor alle aanvragen. Vanwege deze architectuur, hoeven geen extra stuklijstniveaus meer te worden opgegeven om het gebruik van kanbans mogelijk te maken voor halffabricaten. Deze architectuur helpt tevens de voorraadtransacties tot een minimum te beperken.

## <a name="products-and-material-in-work-in-progress"></a>Producten en materiaal in onderhanden werk
De verlaging van batchgrootte naar de ideale status van een stroom voor één stuk in lean manufacturing kan zorgen voor een drastische toename van het aantal voorraadtransacties als elke orderverzamelingsproces en elke kanbanregistratie transacties opzet voor de verbruikte artikelen. De productiestroomarchitectuur maakt de overboeking mogelijk van materialen naar de productiestroom, samen met de terugtrekkingskanbans in opslag- of transportmateriaalverwerkingseenheidsgrootten. De waarde van het uitgegeven materiaal wordt toegevoegd aan de OHW-rekening (onderhanden werk) die is gerelateerd aan de productiestroom, op vergelijkbare wijze als materiaal dat wordt uitgegeven aan een productieorder. Hetzelfde principe kan worden toegepast op producten en halffabricaten. Tenzij deze producten worden gemaakt, overgeboekt of verbruikt binnen een productiestroom, zijn voorraadtransacties optioneel. Nadat de producten naar de voorraad zijn geboekt, wordt de OHW-rekening voor de productiestroom verminderd door de gerelateerde standaardkosten in mindering te brengen.

## <a name="value-streams-and-value-stream-mapping"></a>Waardestromen en waardestroomtoewijzing
De architectuur van lean manufacturing is geïnspireerd op de vijf Lean-principes die door Womack en Jones zijn geformuleerd: klantwaarde, waardestroom, stroom, pull en perfectie. Eén goedgekeurde methode voor het implementeren van lean manufacturing-oplossingen in de fysieke wereld van de productie is waardestroomtoewijzing (VSM). Deze methode werd geïntroduceerd door Rother en shook in hun publicatei "Learning to See" aan het Lean Manufacturing Institute. 

De waardestroom van de toekomstige status kan als productiestroomversie worden gemodelleerd. Alle processen van de waardestroom worden gemodelleerd als procesactiviteiten. Mutaties of overboekingen kunnen als overboekingsactiviteiten worden gemodelleerd als de overboekingsstatus moet worden geregistreerd of als een integratie met orderverzameling of geconsolideerde zendingen is vereist. 

De waardestroom zelf wordt gemodelleerd als operationele eenheid. Daarom kan de waardestroom als financiële dimensie worden gebruikt.

Zie [Een operationele eenheid maken](../../fin-and-ops/organization-administration/tasks/create-operating-unit.md) voor meer informatie over het maken van operationele eenheden.

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Kostprijsberekening voor lean manufacturing op basis van de productiestroom
De periodieke consolidatie van de kosten voor een productiestroom corrigeert de verwante OHW-rekening en maakt het mogelijk afwijkingen vast te stellen voor de producten die door de productiestroom worden geleverd.

## <a name="continuous-improvement"></a>Continue verbetering
Om u doorlopende betere ondersteuning te kunnen bieden, worden de productiestromen geïmplementeerd in tijdeffectieve versies. Daarom kan een bestaande productiestroomversie, samen met alle gerelateerde kanbanregels, worden gekopieerd naar een toekomstige versie van de productiestroom. Bovendien kan de productiestroom voor de toekomstige status worden gemodelleerd voordat deze wordt gevalideerd en geactiveerd voor productie. Bestaande kanbans van oude productiestroomversies worden automatisch gekoppeld aan de nieuwe versie om te zorgen voor een naadloze materiaalstroom op de overgangsdatum en daarna.

## <a name="simplicity"></a>Eenvoud
Voor de implementatie van Lean Manufacturing hebben we een productiestroom- en -activiteitbenadering gekozen die modellering mogelijk maakt van eenvoudige en complexe productiescenario's in één schaalbare architectuur. Een nauwkeuriger blik op het concept activiteit toont een nieuwe eenvoud voor de gebruikers die dit nodig hebben: de werkvloer en de logistiekwerknemers. Door op basis van op activiteit gebaseerde taken te rapporteren in plaats van op voorraadtransacties, verplaatst een gecombineerde gebruikersinterface voor alle lean manufacturing-varianten de bedrijfscomplexiteit van de gebruikersinterface naar waar deze thuishoort: de productiestroom als backbone van lean manufacturing.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]