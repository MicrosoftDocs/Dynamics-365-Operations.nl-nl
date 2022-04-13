---
title: Kan geen pakbon boeken voor een gestopte verkooporderregel
description: U kunt geen pakbon boeken voor een gestopte verkooporderregel
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462848"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Kan geen pakbon boeken voor een gestopte verkooporderregel

Foutcode: SYS13203

## <a name="symptoms"></a>Symptomen

Wanneer u probeert een pakbon te boeken voor een lading, wordt het volgende foutbericht weergegeven in het systeem:

> Kan pakbon niet meer boeken bij het stoppen van een verkooporderregel na bevestiging van de uitgaande zending. Er kan geen hoeveelheid worden verzameld.

## <a name="cause"></a>Oorzaak

Een of meer gerelateerde verkooporderregels is mogelijk gestopt, wat betekent dat deze verkooporder niet verder kan worden verwerkt in het systeem. Dit betekent onder andere dat het systeem geen pakbon voor de order zal boeken.

Een gebruiker heeft bijvoorbeeld besloten om een of meer orderregels te stoppen, omdat de klant heeft teruggebeld en de order heeft geannuleerd. Als de uitgaande zending echter al was bevestigd, zou de zending met de verkooporder al fysiek het magazijn hebben verlaten. Dit betekent dat het stoppen van de verkooporderregels geen effect heeft. Aangezien het niet langer mogelijk is om de zending fysiek te stoppen, kunt u net zo goed het stoppen van regels ongedaan maken, zodat u de pakbon kunt boeken. U moet vervolgens de geannuleerde order als een retour verwerken.

## <a name="resolution"></a>Oplossing

Als u de pakbon wilt kunnen boeken, moet u ervoor zorgen dat de relevante verkooporderregels niet zijn gestopt door de volgende stappen uit te voeren.

1. Ga naar **Alle verkooporders \> Verkoop en marketing \> Alle verkooporders**.
1. Zoek en open de verkooporder waarmee u problemen hebt.
1. Selecteer een verkooporderregel in het sneltabblad **Verkooporderregels**.
1. Open op het sneltabblad **Regeldetails** het tabblad **Algemeen** en zorg ervoor dat het veld **Gestopt** is ingesteld op *Nee*.
1. Ga door met het werken totdat alle relevante verkoopregels niet langer zijn gestopt.
1. Probeer opnieuw om de pakbon voor de belasting of verkooporder te boeken.
