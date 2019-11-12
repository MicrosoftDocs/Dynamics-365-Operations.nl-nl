---
title: Overzicht van opbrengsten voor reserves
description: Dit onderwerp bevat informatie over de functie voor opbrengsttoerekening. Deze functie biedt een flexibel raamwerk waarmee u bedrijfsspecifieke regels kunt definiëren om zowel de opbrengstprijs als het opbrengstschema voor orders met meerdere elementen toe te rekenen.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 0681636853b38895e4b8875150ea42baadd7b951
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570374"
---
# <a name="revenue-recognition-overview"></a>Overzicht van opbrengsten voor reserves

[!include [banner](../includes/banner.md)]

> [!NOTE]
> De functie voor opbrengsttoerekening kan niet worden ingeschakeld via Functiebeheer. Momenteel moet u configuratiesleutels gebruiken om deze functie in te schakelen.

Bedrijven in industrieën die meerdere elementen verkopen, zoals producten, services, abonnementen enzovoort, moeten orders met meerdere elementen kunnen opsplitsen, zodat opbrengsten kunnen worden toegerekend op basis van een reeks bedrijfsspecifieke en branchespecifieke richtlijnen.

In het algemeen kan het proces voor opbrengsttoerekening worden gebruikt voor het uitvoeren van de volgende taken:

* Wijs opbrengsten toe om te garanderen dat de juiste opbrengstprijs wordt toegerekend op basis van de waarde van de onderdelen op de orders met meerdere elementen.
* Stel opbrengsten uit op basis van een opbrengstschema dat de contractperioden en -percentages voor toerekening van opbrengsten in de tijd aangeeft.

De functie Opbrengsttoerekening biedt een flexibel raamwerk waarmee u bedrijfsspecifieke regels kunt definiëren om zowel de opbrengstprijs als het opbrengstschema toe te rekenen.

Vrijgegeven producten worden gebruikt ter ondersteuning van opbrengsttoerekening voor verkooporderdocumenten. De vrijgegeven producten bevatten de instellingen die nodig zijn om de opbrengstprijs en het opbrengstschema te bepalen. De verkooporder kan afkomstig zijn uit een tijd- en materiaalproject.

Bedrijven kunnen de functionaliteit voor opbrengstschema gebruiken zonder de functionaliteit voor opbrengstprijs te gebruiken. Daarom wordt de prijs op de verkooporderregels gebruikt als opbrengst of uitgestelde opbrengst. Als er een opbrengstschema bestaat voor de verkooporderregel, wordt de prijs op de verkooporderregel uitgesteld. Als er geen opbrengstschema bestaat voor de verkooporderregel, wordt de prijs op de verkooporderregel geboekt naar een opbrengstrekening bij facturering.

De opbrengstprijs wordt berekend op het moment dat de verkooporder wordt bevestigd of wanneer de factuur wordt geboekt. Als u de opbrengstprijs wilt bekijken voordat de factuur wordt geboekt, moet u de verkooporder bevestigen.

Wanneer de verkooporder wordt bevestigd, wordt ook een verwacht opbrengstschema opgesteld als er voor een verkooporderregel een opbrengstschema voorkomt. Wanneer de verkooporder wordt gefactureerd, wordt het verwachte opbrengstschema verwijderd en wordt het verwachte opbrengstschema vervangen door het feitelijke schema voor opbrengsttoerekening.

De details van het schema voor opbrengsttoerekening worden onderhouden voor elke verkooporderregel. Daarom kan de manager voor opbrengsttoerekening de details bekijken en regels vrijgeven voor opbrengst wanneer de contractuele verplichting is voltooid. Aan het einde van elke periode kan de manager voor opbrengsttoerekening een opbrengstjournaal maken om eventuele schemaregels vrij te geven die op of vóór een door hem of haar gedefinieerde datum vervallen. Dit opbrengstjournaal wordt niet direct geboekt. Daarom kan de manager voor opbrengsttoerekening controleren of de juiste bedragen worden vrijgegeven van uitgestelde opbrengsten naar werkelijke opbrengsten.

Als door een contractuele wijziging een nieuwe verkooporderregel moet worden toegevoegd aan de bestaande verkooporder of een nieuwe verkooporder, kan een hertoewijzingsproces worden uitgevoerd om de opbrengstprijs voor alle regels in de verkooporders te corrigeren.
