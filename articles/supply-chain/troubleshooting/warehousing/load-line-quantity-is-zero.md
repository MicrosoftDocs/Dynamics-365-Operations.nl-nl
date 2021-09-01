---
title: U kunt een zending niet bevestigen omdat laadregels een hoeveelheid van nul hebben
description: U kunt een zending niet bevestigen omdat laadregels een hoeveelheid van nul hebben.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5dc5f8962ba37d21d7ef505fea940dc8767a9d9295588cb0e12e9eebe379a35c
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012155"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>U kunt een zending niet bevestigen omdat laadregels een hoeveelheid van nul hebben

Foutcode: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Symptomen

Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:

> Alle regels in lading %1 hebben een hoeveelheid van nul.  
> De zending voor lading %1 kon niet worden bevestigd.

U kunt de zending voor de lading daarom nog niet bevestigen.

## <a name="cause"></a>Oorzaak

Het systeem evalueert of de ladingsregel kan worden bevestigd voor verzending op basis van de gemaakte werk-ID's, de hoeveelheid van de ladingsregel en het percentage van de minder geleverde hoeveelheid. Als het systeem vindt dat er geen werk-ID's zijn en als het percentage voor minder geleverde hoeveelheid is ingesteld op 100 procent, kunt u de zending niet bevestigen.

Dit probleem kan zich bijvoorbeeld voordoen als het werk is geannuleerd en het minderleveringspercentage op de ladingsregel 100 procent is.

## <a name="resolution"></a>Oplossing

Daarom bevindt de lading of zending zich momenteel in een staat waarbij de verzendingsbevestiging mislukt. Om dit probleem te verhelpen, voert u een van de volgende taken uit:

- Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.
- Controleer uw ladingsregels om na te gaan of het minderleveringspercentage en de hoeveelheden zijn afgestemd op de verzamelde werkhoeveelheid.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen

Gebruik de volgende procedure om de ladingsregels te controleren en ervoor te zorgen dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Open de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer de ladingsregel op het sneltabblad **Laadregels**.
1. Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.
1. Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.
1. Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.
1. Als er een mismatch is, annuleert u het desbetreffende werk, configureert u de locatierichtlijn opnieuw en geeft u de lading opnieuw vrij. Voor instructies zie [U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld](picked-quantity-is-not-on-final.md).
1. Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Controleer uw ladingsregels om na te gaan of het minderleveringspercentage en de hoeveelheden zijn afgestemd op de verzamelde werkhoeveelheid

Doe het volgende om uw ladingsregels te controleren om na te gaan of het minderleveringspercentage en de hoeveelheden zijn afgestemd op de verzamelde werkhoeveelheid.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Open de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de minderlevering overschrijdt.
1. Pas de waarde in het veld **Minderlevering** of het veld **Hoeveelheid** zo nodig aan.

> [!TIP]
> Als het probleem nog steeds niet is verholpen, moet u mogelijk meer orderverzamelingswerk uitvoeren voor de gerelateerde verkooporders of transferorders totdat de beschikbare hoeveelheid is afgestemd op de lading of zending.
