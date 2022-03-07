---
title: Hoeveelheid op een gestarte quarantaineorder is niet bijgewerkt wanneer de order wordt gesplitst
description: Wanneer u een quarantaineorder maakt en probeert deze te splitsen, wordt de orderhoeveelheid niet bijgewerkt naar de gesplitste resterende hoeveelheid.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026418"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Hoeveelheid op een gestarte quarantaineorder is niet bijgewerkt wanneer de order wordt gesplitst

KB-nummer: 4613113

## <a name="symptoms"></a>Symptomen

Wanneer u een quarantaineorder maakt en probeert deze te splitsen, wordt de orderhoeveelheid niet bijgewerkt naar de resterende hoeveelheid na het splitsen.

## <a name="resolution"></a>Oplossing

De oorspronkelijke hoeveelheid van een quarantaineorder wordt niet gewijzigd om ervoor te zorgen dat u de oorspronkelijke hoeveelheid die voor die quarantaineorder is gemaakt, kunt bijhouden. De hoeveelheid die is opgesplitst van een quarantaineorder, wordt echter wel bij gehouden. Voor deze tracering wordt een databaseveld met de naam `QuantityThatHasSplitIntoOtherQuarantineOrders` gebruikt. Dit veld is echter niet zichtbaar in de gebruikersinterface (UI).
