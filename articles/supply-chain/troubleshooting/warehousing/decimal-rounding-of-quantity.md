---
title: De decimale afronding van de fysieke bijwerkingshoeveelheid is onjuist
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die niet gelijk is aan de precisie van decimalen die in de eenheid is gedefinieerd.
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
ms.openlocfilehash: ddfac7106eb0e8b934516ca10e3950891d10910a2ccdef1868faf25812243159
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726556"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>De decimale afronding van de fysieke bijwerkingshoeveelheid is onjuist

Foutcode: SYS19589

## <a name="symptoms"></a>Symptomen

Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die niet gelijk is aan de precisie van decimalen die in de eenheid is gedefinieerd.

Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:

> Decimale afronding van de fysieke bijwerkhoeveelheid in de eenheid %1 is verkeerd.

U kunt de pakbon voor de lading daarom nog niet genereren.

## <a name="cause"></a>Oorzaak

Het systeem evalueert of de decimale afronding van de verzendhoeveelheid overeenkomt met de precisie van decimalen die is gedefinieerd voor de verzendeenheid. Wanneer het systeem de verzendhoeveelheid naar het opgegeven aantal decimalen afrondt, kunt u de pakbon niet genereren als blijkt dat de afgeronde verzendhoeveelheid niet gelijk is aan de werkelijke verzendhoeveelheid. Dit probleem kan zich bijvoorbeeld voordoen als de verkoophoeveelheid 1,75 kilogram (kg) is en de precisie van decimalen is ingesteld op *1*.

## <a name="resolution"></a>Oplossing

Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt. Om dit probleem te verhelpen, voert u een van de volgende taken uit:

- Controleer de ladingsregels en breng correcties aan om er zeker van te zijn dat de hoeveelheid correct kan worden geconverteerd zonder decimale getallen en andere afrondingskwesties.
- Controleer uw ladingsregels en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>De ladingsregels te controleren en correcties aanbrengen om er zeker van te zijn dat de hoeveelheid correct kan worden geconverteerd zonder decimale getallen en andere afrondingskwesties

Gebruik de volgende procedure om de ladingsregels te controleren en correcties aanbrengen om er zeker van te zijn dat de hoeveelheid correct kan worden geconverteerd zonder decimale getallen en andere afrondingskwesties.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.
1. Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.
1. Selecteer op het tabblad  **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt.
1. Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.
1. Selecteer op het tabblad  **Regeldetails** de optie **Order**.
1. Stel veld **Hoeveelheid** in op de opgenomen hoeveelheid (dat wil zeggen, op de waarde van het veld **Hoeveelheid gemaakt werk**), zodat de pakbon kan worden gegenereerd.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Controleer uw ladingsregels en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid

Gebruik de volgende procedure om de ladingsregels te controleren en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.
1. Selecteer op het sneltabblad **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt. Maak een notitie van de waarde in de velden **Hoeveelheid** en **Eenheid**.
1. Ga naar **Organisatiebeheer \> Eenheden \> Eenheden**.
1. Selecteer de eenheid waarvoor geen pakbon kan worden gegenereerd.
1. Pas de waarde van het veld **Precisie van decimalen** zo nodig aan.
