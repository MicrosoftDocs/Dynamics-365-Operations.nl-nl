---
title: U kunt een zending niet bevestigen vanwege onvolledig of ontbrekend werk
description: U kunt een zending niet bevestigen vanwege onvolledig of ontbrekend werk
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 59def4427f9fff32fd3839bb9f9b5d5cccdc7720f92a84f1af3adad596d8b352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730053"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>U kunt een zending niet bevestigen vanwege onvolledig of ontbrekend werk

Foutcode: WAX515

## <a name="symptoms"></a>Symptomen

Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:

> De verzending voor lading %1 kon niet worden bevestigd omdat alle werk voor de lading moet zijn voltooid.

U kunt de zending voor de lading daarom nog niet bevestigen.

## <a name="cause"></a>Oorzaak

Daarom bevindt de lading of zending zich momenteel in een staat waarbij de verzendingsbevestiging mislukt. Voordat u de zending kunt bevestigen, moet er minimaal enig werk bestaan voor de belasting en moet al het werk de status *Gesloten* of *Geannuleerd* hebben.

## <a name="resolution"></a>Oplossing

Controleer de gerelateerde verkooporders of transferorders voor de lading of zending en ga na of alle gerelateerde werkzaamheden zijn voltooid of geannuleerd.

U kunt op verschillende pagina's werken met zendingen en ladingen. De volgende subsecties bieden enkele voorbeelden.

### <a name="all-loads-page"></a>De pagina Alle ladingen

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.
1. Controleer de status van elke werk-id. Volg elke werk-id op die niet de status *Gesloten* of *Geannuleerd* heeft.
1. Als elke werk-id de status *Gesloten* of *Geannuleerd* heeft, probeert u de zending opnieuw te bevestigen.

### <a name="all-shipments-page"></a>De pagina Alle zendingen

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Selecteer de zending die niet kan worden bevestigd.
1. Selecteer in het actievenster op het tabblad **Zendingen** in de groep **Werk** de optie **Werkgegevens**.
1. Controleer de status van elke werk-id. Volg elke werk-id op die niet de status *Gesloten* of *Geannuleerd* heeft.
1. Als elke werk-id de status *Gesloten* of *Geannuleerd* heeft, probeert u de zending opnieuw te bevestigen.

### <a name="all-work-page"></a>De pagina Alle werk

1. Ga naar **Magazijnbeheer \> Werk \> Alle werk**.
1. Selecteer het werk voor het ordernummer waarvoor de zending niet kan worden bevestigd.
1. Selecteer in het actievenster op het tabblad **Zending** in de groep **Zending** de optie **Zending bevestigen**.
1. Controleer de status van elke werk-id. Volg elke werk-id op die niet de status *Gesloten* of *Geannuleerd* heeft.
1. Als elke werk-id de status *Gesloten* of *Geannuleerd* heeft, probeert u de zending opnieuw te bevestigen.
