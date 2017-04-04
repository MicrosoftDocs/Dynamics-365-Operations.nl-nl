---
title: "Een continuïteitsprogramma instellen voor een callcenter"
description: "In dit artikel wordt beschreven hoe u een continuïteitsprogramma instelt voor een callcenter."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: e32961f2a0e0e41715d98075cbc5777d256eb187
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Een continuïteitsprogramma instellen voor een callcenter

In dit artikel wordt beschreven hoe u een continuïteitsprogramma instelt voor een callcenter.

In een continuïteitsprogramma, dat ook bekend staat als een terugkerend orderprogramma, ontvangen klanten regelmatige productzendingen op basis van een vooraf gedefinieerde planning. Elke zending kan een ander product bevatten, zoals in het geval van een boek-van-de-maand club, of hetzelfde product kan herhaaldelijk worden verzonden. Als u een continuïteitsprogrammma instelt, moet u de volgende taken uitvoeren.

1.  Stel de continuïteitsparameters op de **Parameters van callcenter** in.
2.  Maak een continuïteitsprogramma waarmee details worden opgegeven, zoals het betalingsschema, de timing van de zendingen en of de facturering vooraf gebeurt. U moet ook een lijst met producten toevoegen die in het continuïteitsprogramma zijn opgenomen. Elk product ontvangt een gebeurtenis-ID-nummer dat is na elkaar toegewezen beginnen met 1. De gebeurtenis-id's bepalen de volgorde waarin de producten worden verzonden in.
    -   Als klanten een ander product in elke zending ontvangen, worden de producten achtereenvolgens op basis van de bijbehorende gebeurtenis-ID´s verzonden, te beginnen met de huidige gebeurtenis.
    -   Als klanten hetzelfde product in elke zending ontvangen, bevat de lijst slechts één product dat een gebeurtenis-ID heeft. Dezelfde gebeurtenis komt herhaaldelijk voor. U kunt opgeven hoe vaak u elke gebeurtenis wordt herhaald.

3.  Een bovenliggend productmodel voor het programma continuïteit die u hebt gemaakt in taak 2 maken. Als u dit product aan een verkooporder toevoegt, de **continuïteit** pagina wordt geopend. U kunt die pagina vervolgens gebruiken om de werkelijke continuïteitsorder te maken. Met het bovenliggende product worden de afzonderlijke producten die de klant in elke zending ontvangt, niet opgegeven.

Nadat u een continuïteitsprogramma hebt ingesteld zoals hierboven beschreven , kunt u een continuïteitsorder maken voor een klant. U moet mogelijk ook de volgende aanvullende onderhoudstaken uitvoeren.

-   **De huidige continuïteitsgebeurtenisperiode bijwerken**: stel een batchtaak in waarmee aan het systeem wordt doorgegeven wat de huidige gebeurtenisperiode is.
-   **Onderliggende continuïteitsorders maken**: maak onderliggende orders op basis van de bovenliggende continuïteitsorder.
-   **Continuïteitsbetalingen verwerken**: facturering en meldingen verwerken voor betalingen die zijn gekoppeld aan continuïteitsverkooporders.
-   **Continuïteitsregels uitbreiden** (indien nodig): breid het aantal keren uit dat een continuïteitsgebeurtenis kan worden herhaald. De herhaling van zendingen kan vervolgens worden uitgebreid buiten de limiet die is ingesteld in het veld **Drempel voor continuïteitsherhaling** in de parameters van het callcenter.
-   **Een continuïteitsupdate uitvoeren** (indien nodig): synchroniseer wijzigingen tussen het continuïteitsprogramma en de bovenliggende continuïteitsverkooporders.
-   **Bovenliggende continuïteitsregels en -orders sluiten**: sluit continuïteitsorders.



