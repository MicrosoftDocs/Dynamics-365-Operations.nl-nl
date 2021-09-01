---
title: Hoeveelheid overschrijdt meerleveringspercentage tijdens genereren pakbon
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die het percentage van de meerlevering overschrijdt.
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
ms.openlocfilehash: 00e3da7767b80e16f9351f59b109765bffc0128fe149cefafc1edda3a6cbcb96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781340"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Hoeveelheid overschrijdt meerleveringspercentage tijdens genereren pakbon

Foutcode: SYS24920

## <a name="symptoms"></a>Symptomen

Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die het percentage van de meerlevering overschrijdt.

Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:

> Meerlevering van regel is %1 percent, maar de toegestane overlevering is slechts %2 percent.

U kunt de pakbon voor de lading daarom nog niet genereren.

## <a name="cause"></a>Oorzaak

De opgenomen hoeveelheid voor de lading of zending is meer dan de bestelde hoeveelheid en valt niet binnen het bereik van het meerleveringspercentage.

## <a name="resolution"></a>Oplossing

Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt. Om dit probleem te verhelpen, voert u een van de volgende taken uit:

- Pas de hoeveelheid voor de ladingsregel aan.
- Pas het meerleveringspercentage aan.
- Keer het om en breng correcties aan.

### <a name="adjust-the-load-line-quantity"></a>De hoeveelheid voor de ladingsregel aanpassen

Met de volgende procedure kunt u de hoeveelheid op de ladingsregel aanpassen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.
1. Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.
1. Selecteer op het tabblad  **Ladingsregels** de ladingsregel voor het artikel dat het meerleveringspercentage overschrijdt.
1. Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.
1. Selecteer op het tabblad  **Regeldetails** de optie **Order**.
1. Stel veld **Hoeveelheid** in op de opgenomen hoeveelheid (dat wil zeggen, op de waarde van het veld **Hoeveelheid gemaakt werk**), zodat de pakbon kan worden gegenereerd.

### <a name="adjust-the-over-delivery-percentage"></a>Het meerleveringspercentage aanpassen

Met de volgende procedure kunt u het meerleveringspercentage aanpassen.

1. Ga naar **Klanten \> Orders \> Alle orders**.
1. Selecteer de verkooporder waarvoor u geen pakbon voor de lading kunt boeken.
1. Selecteer op het tabblad  **Verkooporderregels** de verkooporderregel voor het artikel dat het percentage voor meerleveringen overschrijdt.
1. Selecteer op het tabblad  **Regeldetails** de optie **Levering**.
1. Stel in het veld **Meerlevering** de waarde in op een groter percentage dat geschikt is voor de hoeveelheid die voor de ladinghoeveelheid was verzameld, zodat het genereren van de pakbon doorgang kan vinden.

### <a name="reverse-and-make-adjustments"></a>Omkeren en correcties aanbrengen

Keer alles om dat voor de lading is geboekt (bijvoorbeeld de pakbon, bevestiging van zending en werk), breng correcties in de verkooporder aan, geef de order opnieuw vrij aan het magazijn en voer de zendingsprocedure uit.

Gebruik de volgende procedure om een pakbon te annuleren.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Pakbonnen annuleren**.

Gebruik de volgende procedure om een verzendingsbevestiging om te keren.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.

Gebruik de volgende procedure om werk om te keren.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer in het actievenster op het tabblad  **Ladingen** in de groep  **Werk** de optie  **Werk omkeren**.
