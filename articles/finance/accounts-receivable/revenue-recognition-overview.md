---
title: Overzicht van opbrengsttoerekening
description: Dit onderwerp bevat informatie over de functie voor opbrengsttoerekening. Deze functie biedt een flexibel raamwerk waarmee u bedrijfsspecifieke regels kunt definiëren om zowel de opbrengstprijs als het opbrengstschema voor orders met meerdere elementen toe te rekenen.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a7e37a0800ec7909f79e5a2354f59c7450995641
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995609"
---
# <a name="revenue-recognition-overview"></a>Overzicht van opbrengsttoerekening

[!include [banner](../includes/banner.md)]

Bedrijven in industrieën die meerdere elementen verkopen, zoals producten, services, abonnementen, enzovoort, moeten orders met meerdere elementen kunnen opsplitsen, zodat opbrengsten kunnen worden toegerekend op basis van een reeks bedrijfs- en branchespecifieke richtlijnen.

> [!NOTE]
> De functie voor opbrengsttoerekening kan niet worden ingeschakeld via Functiebeheer. Momenteel moet u configuratiesleutels gebruiken om deze functie in te schakelen.

> Opbrengsttoerekening, inclusief bundelfunctionaliteit, wordt niet ondersteund voor gebruik in Commerce-kanalen (e-commerce, POS, callcenter). Artikelen die zijn geconfigureerd met opbrengsttoerekening mogen niet worden toegevoegd aan orders of transacties die zijn gemaakt in Commerce-kanalen.

Over het algemeen kan het proces voor opbrengsttoerekening worden gebruikt voor het uitvoeren van de volgende taken:

* Wijs opbrengsten toe om te garanderen dat de juiste opbrengstprijs wordt toegerekend op basis van de waarde van de componenten in orders met meerdere elementen.
* Stel opbrengsten uit op basis van een opbrengstschema dat de contractperioden en -percentages voor toerekening van opbrengsten in de tijd aangeeft.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

De video [Opbrengsttoerekening gebruiken in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (zie hierboven) is opgenomen in de [afspeellijst voor Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.

De functie Opbrengsttoerekening biedt een flexibel raamwerk waarmee u bedrijfsspecifieke regels kunt definiëren om zowel de opbrengstprijs als het opbrengstschema toe te rekenen.

Vrijgegeven producten worden gebruikt ter ondersteuning van opbrengsttoerekening voor verkooporderdocumenten. De vrijgegeven producten bevatten de instellingen die nodig zijn om de opbrengstprijs en het opbrengstschema te bepalen. De verkooporder kan afkomstig zijn uit een tijd- en materiaalproject.

Bedrijven kunnen de functionaliteit voor opbrengstschema gebruiken zonder de functionaliteit voor opbrengstprijs te gebruiken. Daarom wordt de prijs op de verkooporderregels gebruikt als opbrengst of uitgestelde opbrengst. Als er een opbrengstschema bestaat voor de verkooporderregel, wordt de prijs op de verkooporderregel uitgesteld. Als er geen opbrengstschema bestaat voor de verkooporderregel, wordt de prijs op de verkooporderregel geboekt naar een opbrengstrekening bij facturering.

De opbrengstprijs wordt berekend op het moment dat de verkooporder wordt bevestigd of wanneer de factuur wordt geboekt. Als u de opbrengstprijs wilt bekijken voordat de factuur wordt geboekt, moet u de verkooporder bevestigen.

Wanneer de verkooporder wordt bevestigd, wordt ook een verwacht opbrengstschema opgesteld als er voor een verkooporderregel een opbrengstschema voorkomt. Wanneer de verkooporder wordt gefactureerd, wordt het verwachte opbrengstschema verwijderd en wordt het verwachte opbrengstschema vervangen door het feitelijke schema voor opbrengsttoerekening.

De details van het schema voor opbrengsttoerekening worden onderhouden voor elke verkooporderregel. Daarom kan de manager voor opbrengsttoerekening de details bekijken en regels vrijgeven voor opbrengst wanneer de contractuele verplichting is voltooid. Aan het einde van elke periode kan de manager voor opbrengsttoerekening een opbrengstjournaal maken om eventuele schemaregels vrij te geven die op of vóór de gedefinieerde datum vervallen. Dit opbrengstjournaal wordt niet direct geboekt. Daarom kan de manager voor opbrengsttoerekening controleren of de juiste bedragen worden vrijgegeven van uitgestelde opbrengsten naar werkelijke opbrengsten.

Als door een contractuele wijziging een nieuwe verkooporderregel moet worden toegevoegd aan de bestaande verkooporder of een nieuwe verkooporder, kan een hertoewijzingsproces worden uitgevoerd om de opbrengstprijs voor alle regels in de verkooporders te corrigeren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]