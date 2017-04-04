---
title: Uiterste datums orderinvoer
description: Dit artikel bevat informatie over uiterste datums voor orderinvoer. Een uiterste datum voor orderinvoer is een afsluittijd die bepaalt of een klantorder wordt behandeld (en uitgevoerd) als deze op de huidige dag of de volgende dag wordt ontvangen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d865260679dac6196a69f3182f937df7f9fd8200
ms.lasthandoff: 03/31/2017


---

# <a name="order-entry-deadlines"></a>Uiterste datums orderinvoer

Dit artikel bevat informatie over uiterste datums voor orderinvoer. Een uiterste datum voor orderinvoer is een afsluittijd die bepaalt of een klantorder wordt behandeld (en uitgevoerd) als deze op de huidige dag of de volgende dag wordt ontvangen.

In veel bedrijven worden alleen verkooporders die vóór een bepaald tijdstip van de dag worden ontvangen behandeld alsof zij op die dag zijn ontvangen. Eventuele orders die na dat tijdstip binnenkomen worden behandeld alsof zij op de volgende werkdag zijn ontvangen. Deze afsluittijd voor orders wordt de orderinvoerdeadline of het uiterste tijdstip voor orderinvoer genoemd.  

Orderinvoerdeadlines worden gebruikt als invoer voor orderbelofte. Daarom kunnen zij u helpen bij het beheren van klantverwachtingen met betrekking tot orderleveringen. Zo kunnen klanten bijvoorbeeld zien dat, als zij vóór een specifieke tijd een order bij u plaatsen, u toezegt de goederen nog dezelfde dag te zullen verzenden. Als ze deze termijn mist, kunnen ze de zending alleen op de volgende werkdag verwachten. U instellen deadlines voor orderinvoer op basis van uw magazijn capaciteiten en verzending vervoerder-schema's.  

Op de pagina **Orderinvoerdeadlines** stelt u de uiterste tijden voor orderinvoer in voor alle dagen van de week. Als orders na de opgegeven tijden binnenkomen, worden zij behandeld alsof zij de volgende dag zijn ontvangen. De ontvangsttijd is standaard ingesteld op 23:59 (dat wil zeggen één minuut voor middernacht van die dag). U kunt deze standaardtijden aanpassen aan de werkelijke uiterste tijdstippen voor verzending en ontvangst.  

U kunt het uiterste tijdstip voor orderinvoer voor een bepaalde groep klanten definiëren. Zo wilt u bijvoorbeeld wellicht toestaan dat voor een specifieke groep klanten een later uiterst tijdstip voor orderinvoer geldt dan voor de andere klanten. In dit geval definieert u eerst groepen voor orderinvoerdeadlines op de pagina **Orderinvoerdeadlinegroepen**. Vervolgens wijst u de groepen toe aan klanten op de pagina **Klanten**.  

Als uw bedrijf meerdere locaties telt, kunt u voor elke locatie een uiterst tijdstip voor orderinvoer instellen. Bevinden de locaties zich in verschillende tijdzones, dan worden de uiterste tijdstippen voor orderinvoer ingesteld in de tijdzone van elke locatie. Bij het werken met verkooporders en -offertes wordt het uiterste tijdstip voor orderinvoer echter omgezet naar uw eigen tijdzone op de pagina **Beschikbare datums voor verzending en ontvangst**.  

Op de pagina **Combinaties uiterste datum orderinvoer activeren** definieert u de combinaties van sites en orderinvoerdeadlinegroepen die zijn toegestaan.

## <a name="example-order-entry-deadline"></a>Voorbeeld: uiterst tijdstip voor orderinvoer
Het uiterste tijdstiop voor orderinvoer op dinsdag is ingesteld op 16:00. Op een bepaalde dinsdag, om 17:00, probeert u de huidige datum in te stellen als verzenddatum. (Let erop dat er geen levertijd voor dit voorbeeld.) Als de **controle leveringsdatum** selectievakje is ingeschakeld, ontvangt u een waarschuwing weergegeven waarin wordt gemeld dat de datum is niet geldig. Deze waarschuwing wordt weergegeven op de pagina **Beschikbare datums voor verzending en ontvangst**, waar u vervolgens andere datums kunt selecteren.

## <a name="example-different-order-entry-deadlines-per-site"></a>Voorbeeld: verschillende uiterste tijdstippen voor orderinvoer per locatie
Uw bedrijf bestaat uit twee locaties. De locaties bevinden zich in verschillende tijdzones, zoals in de volgende tabel wordt weergegeven.

| Locatie A                      | Locatie B                      |
|-----------------------------|-----------------------------|
| Californië                  | Florida                     |
| PST (Pacific Standard Time) | EST (Eastern Standard Time) |

Voor locatie A en B zijn de volgende uiterste tijdstippen voor orderinvoer gedefinieerd.

| Dag van de week             | A: bestellen deadlines voor orderinvoer (PST) | B: bestellen deadlines voor orderinvoer (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Maandag                      | 13:00:00                          | 14.00                          |
| Dinsdag                     | 13:00:00                          | 14.00                          |
| Woensdag                   | 13:00:00                          | 14.00                          |
| Donderdag                    | 13:00:00                          | 14.00                          |
| Vrijdag                      | 13:00:00                          | 14.00                          |

U bent orderverwerker in Utah, waar de tijdzone MST (Mountain Standard Time) is. Dit betekent dat als u vóór 14:00 MST orders plaatst bij locatie A en vóór 12:00 MST bij locatie B, u voor beide locaties op tijd bent voor het uiterste tijdstip voor orderinvoer.  

In de volgende tabel wordt weergegeven hoe de uiterste tijdstippen voor orderinvoer voor locatie A en B worden omgezet naar MST.

| Site A: PST         | Site A: MST        | Site B: EST           | Site B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00:00               | 14.00              | 14.00                 | 12:00:00              |

**Opmerking:** In een periode met zomertijd worden de uiterste tijdstippen voor orderinvoer dienovereenkomstig aangepast.

## <a name="example-same-order-entry-deadline-per-site"></a>Voorbeeld: dezelfde uiterste tijdstippen voor orderinvoer per locatie
Uw bedrijf bestaat uit twee locaties. De locaties bevinden zich in verschillende tijdzones, zoals in de volgende tabel wordt weergegeven.

| Locatie A                      | Locatie B                      |
|-----------------------------|-----------------------------|
| Californië                  | Florida                     |
| PST (Pacific Standard Time) | EST (Eastern Standard Time) |

Voor locatie A en B zijn de volgende uiterste tijdstippen voor orderinvoer gedefinieerd.

| Dag van de week | PST en EST |
|-----------------|-------------|
| maandag          | 13:00:00       |
| dinsdag         | 13:00:00       |
| woensdag       | 13:00:00       |
| donderdag        | 13:00:00       |
| vrijdag          | 13:00:00       |

U bent orderverwerker in Utah, waar de tijdzone MST is. Dit betekent dat als u vóór 14:00 MST orders plaatst bij locatie A en vóór 11:00 MST bij locatie B, u voor beide locaties op tijd bent voor het uiterste tijdstip voor orderinvoer. 

In de volgende tabel wordt weergegeven hoe de uiterste tijdstippen voor orderinvoer voor locatie A en B worden omgezet naar MST.

| Site A: PST         | Site A: MST        | Site B: EST           | Site B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00:00               | 14.00              | 13:00:00                 | 11:00:00              |

**Opmerking:** In een periode met zomertijd worden de uiterste tijdstippen voor orderinvoer dienovereenkomstig aangepast.

<a name="see-also"></a>Zie ook
--------

[Delivery schedules](delivery-schedules.md)


