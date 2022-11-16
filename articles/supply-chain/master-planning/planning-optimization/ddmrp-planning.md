---
title: Vraaggestuurde planning
description: In het artikel wordt beschreven hoe u geplande orders genereert voor artikelen die zijn ingesteld als ontkoppelingspunten.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740297"
---
# <a name="demand-driven-planning"></a>Vraaggestuurde planning

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

In het artikel wordt beschreven hoe u geplande orders genereert voor artikelen die zijn ingesteld als ontkoppelingspunten.

## <a name="net-flow-and-qualified-demand"></a>Nettostroom en gekwalificeerde vraag

Tijdens de hoofdplanning wordt het concept van *nettostroom* toegepast om de effectieve, beschikbare hoeveelheid vast te stellen op basis van de werkelijke beschikbare voorraad plus de in bestelling zijnde voorraad (bestaande aanbodorders die nog niet zijn ontvangen), min de *gekwalificeerde vraag* (gekwalificeerde komende verkoop), zoals in de volgende afbeelding wordt weergegeven. Wanneer wordt bepaald tot welke bufferzone een artikel hoort en wat de bestelde hoeveelheid moet zijn, wordt de nettostroom geëvalueerd en niet de werkelijke, beschikbare voorraad.

![Voorbeeld van een diagram voor nettostroomberekening.](media/ddmrp-net-flow-example.png "Voorbeeld van een diagram voor nettostroomberekening")

Wanneer een geplande order wordt geactiveerd tijdens een planningsuitvoering, is de bestelde hoeveelheid het maximumniveau min de nettostroom. Voor het toewijzen van een orderprioriteit gebruikt het systeem [op prioriteit gebaseerde planning](priority-based-planning.md) in plaats van behoeftedatums. Met Demand Driven Material Requirements Planning (DDMRP) wordt de prioriteit van een geplande order toegewezen op basis van de bestelde hoeveelheid als een percentage van de maximumvoorraad. In de vorige afbeelding is de bestelde hoeveelheid 53 procent van de maximumhoeveelheid. De orderprioriteit voor de aanvulling is dan 53. (In de context is 0 de hoogste prioriteit en 100 de laagste prioriteit.)

*Gekwalificeerde vraag* is de achterstallige vraag, plus de vraag van vandaag, plus gekwalificeerde orderpieken in de toekomst. Hieronder ziet u een voorbeeld van vraagniveaus voor vandaag (12 juni) en de volgende drie dagen. Met DDMRP kunt u een orderpiekdrempel instellen om de vraag te bepalen die hoger is dan de normale verwachtingen. Als de drempel is ingesteld op 25 stuks, worden twee van de toekomstige datums in de afbeelding gekwalificeerd als orderpieken. U moet een orderpiekdrempel voor elk product afzonderlijk toewijzen via de pagina **Artikelbehoefteplanning**, zoals beschreven in [Buffers instellen voor een ontkoppelingspuntartikel](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Voorbeeld van een diagram voor berekening van gekwalificeerde vraag.](media/ddmrp-net-qualified-demand-example.png "Voorbeeld van een diagram voor berekening van gekwalificeerde vraag")

Op voorwaarde dat er geen achterstallige vraag, kunt u nu de vraag van vandaag (18) toevoegen aan de hoeveelheden van de twee orderpieken (29 en 26) om een gekwalificeerde vraag van 73 te krijgen. Hoewel er vraag is voor 23 juni, is deze niet opgenomen in de berekening van de nettostroom, omdat DDMRP de geplande order op een andere manier activeert dan traditionele behoefteplanningsgroepen.

## <a name="generating-planned-orders-with-ddmrp"></a>Geplande orders genereren met DDMRP

Tijdens een planningsuitvoering wordt een nieuwe geplande order gemaakt als de nettostroom voor een artikel onder het bestelpunt komt. Wanneer u DDMRP gebruikt, voert u gewoonlijk elke dag een planningsuitvoering uit. Daarom controleert u in wezen eenmaal per dag uw voorraadniveaus om te bepalen welke artikelen moeten worden aangevuld.

Hieronder ziet u een voorbeeld van een situatie waarin u een order hebt voor 18 stuks op 20 juni, 29 stuks op 21 juni, 26 stuks op 22 juni en 20 stuks op 23 juni. Aangezien de piekdrempel is ingesteld op 25 stuks, worden twee van deze orders gemarkeerd als pieken. Er zijn 220 stuks van dit artikel beschikbaar.

![Planningsvoorbeeld 1.](media/ddmrp-planning-example-1.png "Planningsvoorbeeld 1")

Als u de hoofdplanning nu uitvoert, wordt er een geplande order gegenereerd als de nettostroom onder het bestelpunt komt (219 stuks in dit voorbeeld).

![Planningsvoorbeeld 2.](media/ddmrp-planning-example-2.png "Planningsvoorbeeld 2")

In dit voorbeeld wordt een geplande inkooporder gemaakt voor een hoeveelheid van 130, wat gelijk is aan het maximumniveau min de nettostroom. Aan de geplande order wordt een prioriteit van 53,07 toegewezen op basis van het percentage van de maximumhoeveelheid. Omdat deze waarden op 20 juni golden, wordt een geplande order gemaakt met de datum 20 juni plus de ontkoppelde doorlooptijd van het artikel (vijf werkdagen in dit voorbeeld). Omdat vijf werkdagen één week is vanaf vandaag, krijgt de geplande order de datum 27 juni.

> [!NOTE]
> Met de hoofdplanning worden alleen ontkoppelde artikelen berekend met behulp van DDMRP. Alle andere artikelen worden berekend met behulp van standaard-MRP (Material Requirements Planning).
