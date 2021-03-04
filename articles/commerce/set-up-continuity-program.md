---
title: Continuïteitsprogramma's instellen voor callcenters
description: In dit artikel wordt beschreven hoe u een continuïteitsprogramma instelt voor een callcenter.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 738841407b63ef604da092b7c8f4d0f2064d3886
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411255"
---
# <a name="set-up-continuity-programs-for-call-centers"></a>Continuïteitsprogramma's instellen voor callcenters

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een continuïteitsprogramma instelt voor een callcenter.

In een continuïteitsprogramma, dat ook bekend staat als een terugkerend orderprogramma, ontvangen klanten regelmatige productzendingen op basis van een vooraf gedefinieerde planning. Elke zending kan een ander product bevatten, zoals in het geval van een boek-van-de-maand club, of hetzelfde product kan herhaaldelijk worden verzonden. Als u een continuïteitsprogrammma instelt, moet u de volgende taken uitvoeren.

1. Stel de continuïteitsparameters op de **Parameters van callcenter** in.
2. Maak een continuïteitsprogramma waarmee details worden opgegeven, zoals het betalingsschema, de timing van de zendingen en of de facturering vooraf gebeurt. U moet ook een lijst met producten toevoegen die in het continuïteitsprogramma zijn opgenomen. Elk product ontvangt een gebeurtenis-ID die opeenvolgend wordt toegewezen, te beginnen met 1. Met de gebeurtenis-ID's wordt de volgorde bepaald waarin de producten worden verzonden.

    - Als klanten een ander product in elke zending ontvangen, worden de producten achtereenvolgens op basis van de bijbehorende gebeurtenis-ID's verzonden, te beginnen met de huidige gebeurtenis.
    - Als klanten hetzelfde product in elke zending ontvangen, bevat de lijst slechts één product dat een gebeurtenis-ID heeft. Dezelfde gebeurtenis komt herhaaldelijk voor. U kunt opgeven hoe vaak u elke gebeurtenis wordt herhaald.

3. Maak vervolgens een bovenliggend product dat het continuïteitsprogramma vertegenwoordigt dat u in taak 2 hebt gemaakt. Als u dit product aan een verkooporder toevoegt, wordt de pagina **Continuïteit** geopend. U kunt die pagina vervolgens gebruiken om de werkelijke continuïteitsorder te maken. Met het bovenliggende product worden de afzonderlijke producten die de klant in elke zending ontvangt, niet opgegeven.

Nadat u een continuïteitsprogramma hebt ingesteld zoals hierboven beschreven , kunt u een continuïteitsorder maken voor een klant. U moet mogelijk ook de volgende aanvullende onderhoudstaken uitvoeren.

- **De huidige continuïteitsgebeurtenisperiode bijwerken**: stel een batchtaak in waarmee aan het systeem wordt doorgegeven wat de huidige gebeurtenisperiode is.
- **Onderliggende continuïteitsorders maken**: maak onderliggende orders op basis van de bovenliggende continuïteitsorder.
- **Continuïteitsbetalingen verwerken**: facturering en meldingen verwerken voor betalingen die zijn gekoppeld aan continuïteitsverkooporders.
- **Continuïteitsregels uitbreiden** (indien nodig): breid het aantal keren uit dat een continuïteitsgebeurtenis kan worden herhaald. De herhaling van zendingen kan vervolgens worden uitgebreid buiten de limiet die is ingesteld in het veld **Drempel voor continuïteitsherhaling** in de parameters van het callcenter.
- **Een continuïteitsupdate uitvoeren** (indien nodig): synchroniseer wijzigingen tussen het continuïteitsprogramma en de bovenliggende continuïteitsverkooporders.
- **Bovenliggende continuïteitsregels en -orders sluiten**: sluit continuïteitsorders.


[!INCLUDE[footer-include](../includes/footer-banner.md)]