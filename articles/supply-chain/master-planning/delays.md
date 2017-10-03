---
title: Vertragingen
description: Dit artikel geeft informatie over vertragingsdatums in de hoofdplanning. Een vertragingsdatum is een realistische vervaldatum waarop een transactie wordt ontvangen als de eerste afhandelingsdatum die de hoofdplanning plant, later is dan de aangevraagde datum.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 84682e08da6da8928004c7971cd2c2a3725446c0
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="delays"></a>Vertragingen

[!include[banner](../includes/banner.md)]


Dit artikel geeft informatie over vertragingsdatums in de hoofdplanning. Een vertragingsdatum is een realistische vervaldatum waarop een transactie wordt ontvangen als de eerste afhandelingsdatum die de hoofdplanning plant, later is dan de aangevraagde datum.

Hoofdplanning kan de vroegste afrondingsdatum voor een transactie berekenen, op basis van levertijden, materiaalbeschikbaarheid, capaciteitsbeschikbaarheid en verschillende planningsparameters. 

Als hoofdplanning een orderdatum berekent die de huidige datum voorafgaat, kan de order niet op tijd worden afgerond. Daarom wordt de order vertraagd. In dit geval plant de hoofdplanning de order vooruit vanaf de huidige datum, inclusief levertijden. Deze levertijden beginnen met alle componentartikelen op lager niveau. De order krijgt vervolgens een vertraagde datum. Een vertraagde datum is een realistische vervaldatum op basis van de huidige gegevens. De hoofdplanning berekent ook het aantal vertragingdagen. 

In bepaalde situaties kiest u er misschien voor om vertragingen te berekenen, zoals wanneer gebruikers weten dat ze levertijden kunnen versnellen door alternatieve leveringsmethoden te selecteren. 

U kunt instellen hoe de vertragingen worden berekend voor een behoefteplanningsgroep. U kunt vervolgens de behoefteplanningsgroep later aan een artikel koppelen. 

Op de pagina **Parameters hoofdplanning** kunt u de begintijd instellen voor de berekening van vertragingen. Als een order na deze tijd wordt uitgevoerd, wordt aan de vertraagde datum van de order een vertraging van één dag toegevoegd. 

**Opmerking:** in eerdere versies stonden berekende vertragingen bekend als *vertragingsberichten*, werd de vertraagde datum *vertragingsdatum* genoemd en werd naar een vertraagde transactie verwezen als *een transactie die in de toekomst is ingesteld*.

<a name="see-also"></a>Zie ook
--------

[Behoefteplanningsinstellingen](coverage-settings.md)



