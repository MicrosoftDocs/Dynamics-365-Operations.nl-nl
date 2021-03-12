---
title: Productieplanning
description: In dit onderwerp wordt de planning voor de productie beschreven en wordt uitgelegd hoe u geplande productieorders wijzigt met behulp van Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992390"
---
# <a name="production-planning"></a>Productieplanning

Tijdens Planningsoptimalisaties worden verschillende productiescenario's ondersteund. Als u migreert van de bestaande, ingebouwde hoofdplanningsengine is het belangrijk dat u zich realiseert dat bepaalde zaken gewijzigd zijn.

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a>Geplande productieorders

Wanneer tijdens de hoofdplanning geplande orders worden gemaakt om aan behoeften te voldoen, wordt het ordertype bepaald door de waarde van het veld **Gepland ordertype**. Als het veld **Gepland ordertype** is ingesteld op *Productie*, worden geplande productieorders gemaakt. Deze geplande productieorders bevatten informatie over de actieve stuklijst en de route-id van de gerelateerde productie-instellingen.

## <a name="requirements-from-boms"></a>Behoeften van stuklijsten

Met stuklijstinformatie wordt rekening gehouden tijdens de hoofdplanning. De planuitvoer omvat materiaallevering om de gerelateerde materiaalvraag voor productie te dekken.

Tijdens de hoofdplanning wordt de huidige, actieve stuklijst gebruikt om de materialen te bepalen die nodig zijn voor de productie. Deze stap wordt uitgevoerd via alle niveaus van de stuklijststructuur die is gerelateerd aan de vereiste productieorder. Aan de materiaalbehoefte wordt voldaan door de beschikbare voorhanden voorraad, bestaande voorraad op bestelling en goedgekeurde geplande orders te gebruiken. Als er ergens extra materiaal nodig is, wordt een geplande order gemaakt om aan de vraag te voldoen.

## <a name="scheduling-during-firming"></a>Plannen tijdens fiatteren

Geplande productieorders bevatten de route-id die nodig is voor de productieplanning. De planningsondersteuning tijdens de planningsuitvoering voor geplande orders is echter in behandeling. De route-id wordt gebruikt om geplande productieorders te plannen tijdens de fiattering. Dat betekent dat de doorlooptijd voor geplande productieorders kan afwijken van de doorlooptijd voor gerelateerde geplande, gefiatteerde productieorders die op basis ervan worden gegenereerd, zoals hier wordt beschreven:

- **Geplande productieorder**: de doorlooptijd wordt gebaseerd op de statische doorlooptijd van het vrijgegeven product.
- **Gefiatteerde productieorder**: de doorlooptijd wordt gebaseerd op planning die routegegevens en gerelateerde resourcebeperkingen gebruikt.

Zie [Analyse aanpassen aan Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie over de verwachte functiebeschikbaarheid.

Als u afhankelijk bent van productiefunctionaliteit die nog niet beschikbaar is voor Planningsoptimalisatie, kunt u de ingebouwde hoofdplanningsengine blijven gebruiken. Er is geen uitzondering vereist.

## <a name="delays"></a>Vertragingen

Als de doorlooptijd voor benodigd materiaal langer is dan de periode tussen de datum van vandaag en de materiaalbehoeftedatum, wordt de geplande order voor het benodigde materiaal en de bijbehorende productieorder uitgesteld. Voor geplande orders wordt de vertraging (in dagen) berekend op basis van de doorlooptijd van het vrijgegeven product. De vertragingsinformatie wordt vervolgens via alle niveaus van de stuklijststructuur doorgegeven. Daarom kunt u de impact van vertraagde grondstoffen helemaal volgen tot aan de verkooporder van de klant.

## <a name="modifying-planned-orders"></a>Geplande orders wijzigen

Wanneer u de gegevens van een geplande order wijzigt, wordt het volgende bericht weergegeven: "De gevolgen van handmatige wijzigingen voor geplande orders worden pas in de rest van het plan weergegeven als de volgende hoofdplanning wordt uitgevoerd."

Als u informatie over een geplande order wilt wijzigen en de gevolgen ervan op de gerelateerde materiaalbehoeften wilt bekijken, voert u de volgende stappen uit.

1. Werk de geplande order bij.
2. Keur de geplande order goed.
3. Voer de hoofdplanning uit.

Wanneer u de hoofdplanning uitvoert, moet u geen filters gebruiken als geplande productieorders worden opgenomen. Zie de sectie [Filters](#filters), verderop in dit onderwerp voor meer informatie.

> [!NOTE]
> Als de leveringsdatum van de geplande order wordt gewijzigd in een latere datum, kan de vraag worden getraceerd voor een nieuwe geplande order. Dit gedrag treedt op wanneer de nieuwe leveringsdatum een vertraging veroorzaakt voor de getraceerde vraag, maar deze vertraging kan worden voorkomen volgens de doorlooptijdinstellingen.

## <a name="explosion-page"></a>Pagina Explosie

U kunt op de pagina **Explosie** de vraag analyseren die nodig is voor een bepaalde productieorder of geplande productieorder, de gerelateerde behoefteplanning en informatie over behoeftetracering. De informatie op de pagina **Explosie** wordt bijgewerkt tijdens de hoofdplanning. U kunt de informatie niet rechtstreeks vanaf de pagina **Explosie** bijwerken.

## <a name="filters"></a><a name="filters"></a>Filters

Voor planningsscenario's die productie omvatten, wordt u aangeraden gefilterde hoofdplanningsuitvoeringen te vermijden. Als u er zeker van wilt zijn dat Planningsoptimalisatie de vereiste informatie voor het berekenen van het juiste resultaat bevat, moet u alle producten die een relatie hebben met producten in de gehele stuklijststructuur van de geplande order opnemen.

Hoewel afhankelijke onderliggende artikelen automatisch worden gedetecteerd en opgenomen in hoofdplanningsuitvoeringen wanneer de ingebouwde hoofdplanningsengine wordt gebruikt, wordt deze actie niet uitgevoerd via Planningsoptimalisatie.

Als bijvoorbeeld één bout uit de stuklijststructuur van product A ook wordt gebruikt om product B te produceren, moeten alle producten in de stuklijststructuur van producten A en B in het filter worden opgenomen. Omdat het zeer complex kan zijn ervoor te zorgen dat alle producten deel uitmaken van het filter, raden we u aan om gefilterde hoofdplanningsuitvoeringen te vermijden wanneer het gaat om productieorders.
