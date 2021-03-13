---
title: Materiaalvervanging in productie
description: Dit onderwerp beschrijft hoe materialen tijdens het productieproces kunnen worden vervangen.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa2f64026ec20a7b7562aac084866b69c5769029
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006961"
---
# <a name="material-substitution-in-manufacturing"></a>Materiaalvervanging in productie

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft hoe materialen tijdens het productieproces kunnen worden vervangen. 

Er zijn drie methoden om materialen tijdens het productieproces te vervangen:

-   Op datum, wanneer materiaal ander materiaal vervangt na een bepaalde datum
-   Tijdens hoofdplanning, wanneer materiaal in een formule wordt vervangen door ander materiaal, omdat het niet in voorraad is
-   Tijdens productie, wanneer materiaal onverwacht niet in voorraad is en wordt vervangen door ander materiaal

## <a name="substituting-material-by-date"></a>Materiaal op datum vervangen
Een voorbeeld is het volgende scenario: Een machine die door het bedrijf wordt gemaakt, bevat een component die over twee maanden vervalt in de leverancierscatalogus. Vanaf de vervaldatum biedt de leverancier een nieuw onderdeel dat de oude component kan vervangen. Van- en t/m-datums kunnen worden ingesteld op stuklijstregels. In dit voorbeeld stelt u in dat de oude component vervalt door de vervaldatum in het veld **Einddatum** in te voeren. Vervolgens stelt u in de stuklijst de nieuwe, vervangende component in zodat deze geldig is vanaf de dag dat de oude component vervalt. Om dit te doen, voert u de begindatum in het veld **Begindatum** in.

## <a name="substituting-material-by-planning"></a>Materiaal vervangen door planning
U kunt materialen alleen tijdens de planning vervangen wanneer u formules gebruikt, niet wanneer u een stuklijst gebruikt. Bekijk het volgende scenario: Een voedselproductiebedrijf maakt een saus van een formule met 20 ingrediënten. Eén ingrediënt in de formule kan door een van twee andere ingrediënten worden vervangen. Omdat deze twee ingrediënten duurder zijn dan het voorkeursingrediënt, wordt vervanging alleen gebruikt als het voorkeursingrediënt niet in voorraad is. Het materiaal dat kan worden vervangen wordt A genoemd, terwijl de twee vervangende materialen B en C worden genoemd. Materiaalvervanging door planning wordt bepaald door de velden **Planningsgroep** en **Prioriteit** op de formuleregels. Voor dit voorbeeld maakt u formuleregels voor de drie materialen, en koppelt u de formuleregels aan dezelfde planningsgroep. In de instellingen heeft de formuleregel voor materiaal A de hoogste prioriteit (het laagste nummer), de formuleregel voor het materiaal C de laagste prioriteit, en de formuleregel voor materiaal B een prioriteit die tussen de prioriteit van de andere twee regels ligt. Als u vraag naar het afgewerkte artikel hebt, bepaalt de hoofdplanning eerst of de vraag naar materiaal A kan worden gedekt. Als de vraag niet kan worden gedekt, kijkt de hoofdplanning naar materialen B en C, op volgorde van prioriteit. Als materiaal B voorhanden is, wordt dit gebruikt nadat een geplande batchorder is gefiatteerd voor de formule. Als geen van de materialen op voorraad is, maakt de hoofdplanning een geplande order voor materiaal A. **Notitie:** Wanneer u formuleregels in een plangroep instelt, geeft u alleen een hoeveelheid op voor het materiaal met de hoogste prioriteit. Deze hoeveelheid wordt gebruikt om de vraag van alle materialen in het plan te berekenen, zelfs de materialen die een lagere prioriteit hebben. U kunt niet verschillende hoeveelheden voor artikelen met een lagere prioriteit in de plangroep opgeven.

## <a name="substituting-material-during-production"></a>Materiaal vervangen tijdens productie
Bekijk het volgende scenario: Voor een lasbewerking is een stukje metalen plaat nodig. Tijdens de bewerking meldt een magazijnwerknemer de machineoperator dat de plaat niet in voorraad is. Er is echter besloten dat de plaat kan worden vervangen door een plaat die iets dikker is. Op die manier kan de bewerking worden voltooid. Materiaal kan aan de stuklijst voor een openstaande productieorder worden toegevoegd. Als de productieorder de status **Gestart** heeft, moeten gebruikers de order opnieuw ramen wanneer ze een nieuw artikel aan de productiestuklijst toevoegen. Nadat het materiaal is toegevoegd, kan een nieuwe orderverzamellijst voor het nieuwe artikel worden gemaakt. U hoeft het nieuwe materiaal niet aan de productiestuklijst toe te voegen. In plaats daarvan kunt u dit direct aan de productieorderverzamellijst toevoegen. Wanneer de orderverzamellijst is geboekt, voegt het systeem het materiaal aan de productiestuklijst toe.



