---
title: Later selecteren wordt niet in acht genomen wanneer productieorders via een batchtaak opnieuw worden ingesteld
description: Wanneer u een terugkerende batchtaak gebruikt om de status van een productieorder opnieuw in te stellen, worden latere selecties niet in acht genomen.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026399"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Later selecteren wordt niet in acht genomen wanneer productieorders via een batchtaak opnieuw worden ingesteld

KB-nummer: 4614634

## <a name="symptoms"></a>Symptomen

Wanneer u een terugkerende batchtaak gebruikt om de status van een productieorder opnieuw in te stellen, worden latere selecties niet in acht genomen.

## <a name="resolution"></a>Oplossing

Het huidige ontwerp biedt geen ondersteuning voor het gebruik van later selecteren voor het proces *Status opnieuw instellen*.
