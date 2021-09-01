---
title: Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd
description: Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd die de status Wordt gecontroleerd heeft.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721170"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd

KB-nummer: 4612450

## <a name="symptoms"></a>Symptomen

Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd die de status *Wordt gecontroleerd* heeft.

## <a name="resolution"></a>Oplossing

Wanneer wijzigingen bijhouden is ingeschakeld, wordt de status *Wordt gecontroleerd* toegewezen aan gefiatteerde afgeleide orders (uitbestede inkooporders). Als een inkooporder wordt afgeleid (dan is het een uitbestede inkooporder), wordt deze dus alleen naar een werkstroom verzonden. Als een inkooporder een gefiatteerde geplande inkooporder is, is deze automatisch goedgekeurd om ervoor te zorgen dat de planningsengine geen nieuwe geplande orders maakt terwijl de inkooporder nog steeds de status *Concept* heeft.
