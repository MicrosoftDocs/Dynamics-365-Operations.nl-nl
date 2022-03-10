---
title: U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage minderlevering
description: U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage minderlevering
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a6a5b1140d1bc5d09a1bc582fb1d2ac9446fae0920cbb9957797dbdea4c684e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760317"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage minderlevering

Foutcode: WAX1686

## <a name="symptoms"></a>Symptomen

Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:

> De zending voor lading %1 kan niet worden bevestigd omdat de hoeveelheid voor artikel %2 groter is dan het percentage dat voor minderlevering is gedefinieerd.

U kunt de zending voor de lading daarom nog niet bevestigen.

## <a name="cause"></a>Oorzaak

De hoeveelheid van de lading of zending is slechts gedeeltelijk verzameld. De hoeveelheid is op dit moment kleiner dan de verzamelde hoeveelheid met een percentage dat buiten het toegestane percentage voor minderlevering valt.

## <a name="resolution"></a>Oplossing

Om dit probleem te verhelpen, voert u een van de volgende taken uit:

- Stel de hoeveelheid voor de ladingregel in.
- Stel het percentage voor de minderlevering in.

### <a name="set-the-load-line-quantity"></a>De hoeveelheid voor de ladingregel instellen

Voer de volgende stappen uit om de hoeveelheid voor de ladingregel in te stellen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de minderlevering overschrijdt.
1. Selecteer op het sneltabblad **Regeldetails** de optie **Order**.
1. Stel in het veld **Hoeveelheid** de waarde in op de verzamelde hoeveelheid (dat wil zeggen, op de waarde **Hoeveelheid gemaakt werk**), zodat verzendbevestiging kan worden uitgevoerd.

### <a name="set-the-underdelivery-percentage"></a>Het percentage minderlevering instellen

Voer de volgende stappen uit om het percentage minderlevering in te stellen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de minderlevering overschrijdt.
1. Selecteer op het sneltabblad **Regeldetails** de optie **Algemeen**.
1. Stel in het veld **Minderlevering** de waarde in op een groter percentage die geschikt is voor de hoeveelheid die voor de ladinghoeveelheid is verzameld, zodat verzendbevestiging kan worden uitgevoerd.
