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
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026413"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd

KB-nummer: 4612450

## <a name="symptoms"></a>Symptomen

Direct afgeleide gefiatteerde orders worden verwerkt door een werkstroom die wordt gecontroleerd die de status *Wordt gecontroleerd* heeft.

## <a name="resolution"></a>Oplossing

Wanneer wijzigingen bijhouden is ingeschakeld, wordt de status *Wordt gecontroleerd* toegewezen aan gefiatteerde afgeleide orders (uitbestede inkooporders). Als een inkooporder wordt afgeleid (dan is het een uitbestede inkooporder), wordt deze dus alleen naar een werkstroom verzonden. Als een inkooporder een gefiatteerde geplande inkooporder is, is deze automatisch goedgekeurd om ervoor te zorgen dat de planningsengine geen nieuwe geplande orders maakt terwijl de inkooporder nog steeds de status *Concept* heeft.
