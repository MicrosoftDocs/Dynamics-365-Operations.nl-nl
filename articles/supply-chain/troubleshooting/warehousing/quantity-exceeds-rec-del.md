---
title: De hoeveelheid die u probeert bij te werken, overschrijdt de ontvangen/geleverde hoeveelheid.
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die groter is dan de werkhoeveelheid die is verzameld en gereserveerd voor de verkooporder.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249085"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>De hoeveelheid die u probeert bij te werken, overschrijdt de ontvangen/geleverde hoeveelheid

Foutcode: SYS7676

## <a name="symptoms"></a>Symptomen

Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die groter is dan de werkhoeveelheid die is verzameld en gereserveerd voor de verkooporder.

Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:

> De hoeveelheid die u probeert bij te werken, overschrijdt de ontvangen/geleverde hoeveelheid.

U kunt de pakbon voor de lading daarom nog niet genereren.

## <a name="cause"></a>Oorzaak

De verzamelde werkhoeveelheid komt niet overeen met de gemaakte werkhoeveelheid op de ladingsregel. Dit probleem kan zich bijvoorbeeld voordoen als de hoeveelheid op de ladingsregel, de gemaakte werkhoeveelheid of de verzamelde hoeveelheid niet nauwkeurig is.

## <a name="resolution"></a>Oplossing

Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt. Om dit probleem te verhelpen, voert u een van de volgende taken uit:

- Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.
- Pas de hoeveelheid voor de ladingsregel aan.
- Keer alle orderverzamelregistraties om en voer de orderverzameling opnieuw uit.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen

Gebruik de volgende procedure om de ladingsregels te controleren en ervoor te zorgen dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden gegenereerd.
1. Selecteer de ladingsregel op het sneltabblad **Laadregels**.
1. Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.
1. Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.
1. Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.
1. Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.

### <a name="adjust-the-load-line-quantity"></a>De hoeveelheid voor de ladingsregel aanpassen

Met de volgende procedure kunt u de hoeveelheid op de ladingsregel aanpassen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.
1. Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.
1. Selecteer op het tabblad  **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt.
1. Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.
1. Stel het veld **Ladingsregel verminderen** zo in dat correcties op de ladingsregel worden weergegeven.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Alle orderverzamelregistraties omkeren en voer de orderverzameling opnieuw uitvoeren

Als iemand de orderverzamelregistratie heeft gebruikt om een ladingsregel zonder werk af te sluiten, kan er een verschil optreden tussen de hoeveelheid op de ladingsregel en de verzamelde hoeveelheid. In dit geval moet handmatige orderverzamelregistratie worden omgekeerd en moet het verzamelen vervolgens worden uitgevoerd met de mobiele app Warehouse Management.

Gebruik de volgende procedure om de orderverzamelregistratie om te keren.

1. Ga naar **Klanten \> Orders \> Alle orders**.
1. Selecteer de verkooporder waarvoor u geen pakbon voor de lading kunt boeken.
1. Selecteer op het tabblad  **Verkooporderregels** de verkooporderregel waar de orderverzamelregistratie voor is uitgevoerd.
1. Selecteer **Regel bijwerken \> Orderverzamelen** om het verzamelen van de artikelen ongedaan te maken.
