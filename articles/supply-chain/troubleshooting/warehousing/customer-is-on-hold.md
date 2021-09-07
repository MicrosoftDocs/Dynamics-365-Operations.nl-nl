---
title: U kunt een zending niet bevestigen omdat de klant in de wacht is
description: U kunt een zending niet bevestigen omdat de klant in de wacht is.
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
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344259"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>U kunt een zending niet bevestigen omdat de klant in de wacht is

Foutcode: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Symptomen

Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:

> Zending %1 kan niet worden bevestigd omdat de klant is geblokkeerd voor %2.

U kunt de zending voor de lading daarom nog niet bevestigen.

## <a name="cause"></a>Oorzaak

De klantrekening van de lading of zending staat in de wacht. Daarom voorkomt de status van de klant dat de zending wordt bevestigd.

## <a name="resolution"></a>Oplossing

Met de volgende procedure kunt u de blokkering van de klantrekening opheffen.

1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Open de klantrekening die niet kan worden bevestigd voor de zending.
1. Stel op het sneltabblad **Crediteringen en incasso's** het veld **Facturering en levering in de wacht** in op *Nee*.
1. Herhaal deze procedure voor alle geblokkeerde klanten voor de lading.
