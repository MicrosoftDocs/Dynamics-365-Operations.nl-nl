---
title: U kunt een zending niet bevestigen omdat de hoeveelheid nul is
description: U kunt een zending niet bevestigen omdat de hoeveelheid nul is
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712881"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>U kunt een zending niet bevestigen omdat de hoeveelheid nul is

Foutcode: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Symptomen

Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:

> Ladingsregel voor artikel %1 en zending %2 is bijgewerkt tot de hoeveelheid nul vanwege de instellingen voor onderlevering, zodat er geen hoeveelheden voor dit artikel kunnen worden verzonden.

U kunt de zending voor de lading daarom nog niet bevestigen.

## <a name="cause"></a>Oorzaak

Het systeem evalueert of de verzamelde hoeveelheid binnen de verwachte limieten valt, op basis van de verzamelde hoeveelheid, de hoeveelheid op de ladingsregel en het minderleveringspercentage. Als op de ladingsregel wordt vastgesteld dat de verzamelde hoeveelheid 0 (nul) is, kunt u de zending niet bevestigen. Dit probleem kan zich bijvoorbeeld voordoen als het werk is geannuleerd en het minderleveringspercentage op de ladingsregel 100 procent is.

## <a name="resolution"></a>Oplossing

Controleer uw ladingsregels om na te gaan of het minderleveringspercentage en de hoeveelheden zijn afgestemd op de verzamelde werkhoeveelheid.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de minderlevering overschrijdt.
1. Pas de waarde in het veld **Minderlevering** of het veld **Hoeveelheid** zo nodig aan.

> [!TIP]
> Als het probleem nog steeds niet is verholpen, moet u mogelijk meer orderverzamelingswerk uitvoeren voor de gerelateerde verkooporders of transferorders totdat de beschikbare hoeveelheid is afgestemd op de lading of zending.
