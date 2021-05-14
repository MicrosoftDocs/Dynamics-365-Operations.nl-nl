---
title: U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld
description: U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938448"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld

Foutcode: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Symptomen

Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:

> Enkele artikelen die nodig zijn voor lading %1 zijn nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.

U kunt de zending voor de lading daarom nog niet bevestigen.

## <a name="cause"></a>Oorzaak

De lading of zending kan niet in de huidige status worden bevestigd, omdat mogelijk een van de volgende voorwaarden van toepassing is:

- Het gerelateerde werk is nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.
- De verzamelde werkhoeveelheid komt niet overeen met de gemaakte werkhoeveelheid op de ladingsregel.

## <a name="resolution"></a>Oplossing

Controleer de gerelateerde verkooporders of transferorders op de lading of zending. Zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.

1. Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.
1. Selecteer de lading waarvoor de zending niet kan worden bevestigd.
1. Selecteer de ladingsregel op het sneltabblad **Laadregels**.
1. Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.
1. Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.
1. Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.
1. Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.
