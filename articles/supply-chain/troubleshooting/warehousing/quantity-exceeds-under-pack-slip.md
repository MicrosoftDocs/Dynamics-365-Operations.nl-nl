---
title: Hoeveelheid overschrijdt minderleveringspercentage tijdens genereren pakbon
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die het percentage van de minderlevering overschrijdt.
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
ms.openlocfilehash: ae02846c0ec937ebaff440dc5272a135e16c8aa7355ecc303929e760a54b6627
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760293"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Hoeveelheid overschrijdt minderleveringspercentage tijdens genereren pakbon

Foutcode: SYS24921

## <a name="symptoms"></a>Symptomen

Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die het percentage van de minderlevering overschrijdt.

Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:

> Minderlevering van regel is %1 percent, maar de toegestane onderlevering is slechts %2 percent.

U kunt de pakbon voor de lading daarom nog niet genereren.

## <a name="cause"></a>Oorzaak

De opgenomen hoeveelheid voor de lading of zending valt onder de bestelde hoeveelheid en valt niet binnen het bereik van het minderleveringspercentage.

## <a name="resolution"></a>Oplossing

Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt. Om dit probleem te verhelpen, voert u een van de volgende taken uit:

- Pas het minderleveringspercentage aan.
- Keer het om en breng correcties aan.

### <a name="adjust-the-under-delivery-percentage"></a>Het minderleveringspercentage aanpassen

Met de volgende procedure kunt u het minderleveringspercentage aanpassen.

1. Ga naar **Klanten \> Orders \> Alle orders**.
1. Selecteer de verkooporder waarvoor u geen pakbon voor de lading kunt boeken.
1. Selecteer op het tabblad  **Verkooporderregels** de verkooporderregel voor het artikel dat het percentage voor minderleveringen overschrijdt.
1. Selecteer op het tabblad  **Regeldetails** de optie **Levering**.
1. Stel in het veld **Minderlevering** de waarde in op een groter percentage dat geschikt is voor de hoeveelheid die voor de ladinghoeveelheid was verzameld, zodat het genereren van de pakbon doorgang kan vinden.

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
