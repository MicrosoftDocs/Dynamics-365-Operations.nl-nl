---
title: Werkstroomvoorwaarden voor voorraadjournaal zijn van toepassing op journaalniveau, niet op regelniveau
description: Werkstroomvoorwaarden voor voorraadjournaal zijn alleen van toepassing op journaalniveau, niet op regelniveau.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476011"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Werkstroomvoorwaarden voor voorraadjournaal zijn van toepassing op journaalniveau, niet op regelniveau

## <a name="symptoms"></a>Symptomen

Dit probleem kan zich bijvoorbeeld voordoen als u probeert een werkstroomvoorwaarde voor het voorraadjournaal in te stellen voor het kostenbedrag. U stelt de voorwaarde zo in dat stap 1 alleen wordt uitgevoerd wanneer het kostenbedrag lager is dan 100. U stelt vervolgens een andere voorwaarde in zodat stap 2 alleen wordt uitgevoerd wanneer het kostenbedrag meer is dan of gelijk is aan 100. Wanneer de werkstroom wordt uitgevoerd, wordt in de werkstroomhistorie slechts één regel weergegeven en wordt de eerste voorwaarde altijd als *waar* geëvalueerd, ongeacht de waarde die wordt ingediend.

## <a name="workaround"></a>Tijdelijke oplossing

In de huidige versie zijn werkstroomvoorwaarden voor de voorraad alleen van toepassing op journaalniveau, niet op regelniveau. Dit is zo ontworpen. We raden u aan om uw voorwaardecriteria alleen in te stellen op kenmerken op journaalniveau.
