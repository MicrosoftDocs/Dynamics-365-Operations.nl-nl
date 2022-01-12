---
title: De fysieke resterende hoeveelheid in de eenheid mag niet nul zijn
description: Wanneer u een pakbon genereert, bevatten de gegevens naar de pakbon een voorraadhoeveelheid die groter is dan nul, maar een verkoophoeveelheid van nul.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d767fdce861ccb481a3fe289480a51a7534dc207
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920219"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>De fysieke resterende hoeveelheid in de eenheid mag niet nul zijn

Foutcode: SYS19591

## <a name="symptoms"></a>Symptomen

Wanneer u een pakbon genereert, bevatten de gegevens naar de pakbon een voorraadhoeveelheid die groter is dan nul, maar een verkoophoeveelheid van nul.

Wanneer u de pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:

> Resterende fysieke hoeveelheid in de eenheid %1 mag niet gelijk zijn aan nul.

U kunt de pakbon voor de lading daarom nog niet genereren.

## <a name="cause"></a>Oorzaak

Het systeem evalueert de fysieke resterende hoeveelheid in de voorraadeenheid en de fysieke resterende hoeveelheid in de verzendeenheid. Als in het systeem wordt gevonden dat de fysieke resterende hoeveelheid in de verzendeenheid 0 (nul) is, maar de fysieke resterende hoeveelheid in de voorraadeenheid niet 0 is, kunt u de pakbon niet genereren. Dit probleem kan zich bijvoorbeeld voordoen als de verkoopeenheid en voorraadeenheid voor het artikel verschillen en de omrekening tussen eenheden niet correct is.

## <a name="resolution"></a>Oplossing

Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt. Om dit probleem te verhelpen, voert u een van de volgende taken uit:

- Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.
- Controleer de ladingsregels en breng correcties aan om ervoor te zorgen dat de hoeveelheid correct kan worden geconverteerd zonder afrondingskwesties.
- Controleer uw ladingsregels en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid.
- Zorg ervoor dat de voorraadmaateenheid kleiner is dan de verkoopmaateenheid.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen

Gebruik de volgende procedure om de ladingsregels te controleren en ervoor te zorgen dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer de ladingsregel op het sneltabblad **Laadregels**.
1. Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.
1. Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.
1. Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.
1. Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Controleer de ladingsregels en breng correcties aan om ervoor te zorgen dat de hoeveelheid correct kan worden geconverteerd zonder afrondingskwesties

Gebruik de volgende procedure om de ladingsregels te controleren en correcties aan te brengen om er zeker van te zijn dat de hoeveelheid correct kan worden geconverteerd zonder afrondingskwesties.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.
1. Selecteer in het actievenster, op het tabblad **Verzenden en ontvangen**, in de groep **Omkeren** de optie **Verzendbevestiging omkeren**.
1. Selecteer op het tabblad **Ladingsregels** de ladingsregel voor het artikel dat de meerlevering overschrijdt.
1. Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.
1. Selecteer op het tabblad **Regeldetails** de optie **Order**.
1. Stel veld **Hoeveelheid** in op de opgenomen hoeveelheid (dat wil zeggen, op de waarde van het veld **Hoeveelheid gemaakt werk**), zodat de pakbon kan worden gegenereerd.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Controleer uw ladingsregels en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid

Gebruik de volgende procedure om de ladingsregels te controleren en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.
1. Selecteer op het sneltabblad **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt. Maak een notitie van de waarde in de velden **Hoeveelheid** en **Eenheid**.
1. Ga naar **Organisatiebeheer \> Eenheden \> Eenheden**.
1. Selecteer de eenheid waarvoor geen pakbon kan worden gegenereerd.
1. Pas de waarde van het veld **Precisie van decimalen** zo nodig aan.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Zorg ervoor dat de voorraadmaateenheid kleiner is dan de verkoopmaateenheid

Zorg ervoor dat de voorraadmaateenheid kleiner is dan de verkoopmaateenheid. Overweeg om de maateenheid voor het artikel zo nodig opnieuw te configureren.
