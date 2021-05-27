---
title: Wanneer een hoeveelheid variabel gewicht wordt opgesplitst, wordt de minimumhoeveelheid gebruikt in plaats van de nominale hoeveelheid
description: Wanneer een catch weight hoeveelheid wordt opgesplitst in batches, gebruikt het veld Verzamelhoeveelheid de minimumhoeveelheid die is ingesteld voor het artikel, en niet de nominale hoeveelheid.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026414"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Wanneer een hoeveelheid variabel gewicht wordt opgesplitst, wordt de minimumhoeveelheid gebruikt in plaats van de nominale hoeveelheid

KB-nummer: 4612073

## <a name="symptoms"></a>Symptomen

Wanneer een catch weight hoeveelheid wordt opgesplitst in batches, gebruikt het veld **Verzamelhoeveelheid** de minimumhoeveelheid die is ingesteld voor het artikel, en niet de nominale hoeveelheid.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp. De minimumhoeveelheid-instellingen van elk artikel worden gebruikt voor order verzamelen.
