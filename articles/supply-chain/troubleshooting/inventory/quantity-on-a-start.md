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
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713489"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Hoeveelheid op een gestarte quarantaineorder is niet bijgewerkt wanneer de order wordt gesplitst

KB-nummer: 4613113

## <a name="symptoms"></a>Symptomen

Wanneer u een quarantaineorder maakt en probeert deze te splitsen, wordt de orderhoeveelheid niet bijgewerkt naar de resterende hoeveelheid na het splitsen.

## <a name="resolution"></a>Oplossing

De oorspronkelijke hoeveelheid van een quarantaineorder wordt niet gewijzigd om ervoor te zorgen dat u de oorspronkelijke hoeveelheid die voor die quarantaineorder is gemaakt, kunt bijhouden. De hoeveelheid die is opgesplitst van een quarantaineorder, wordt echter wel bij gehouden. Voor deze tracering wordt een databaseveld met de naam `QuantityThatHasSplitIntoOtherQuarantineOrders` gebruikt. Dit veld is echter niet zichtbaar in de gebruikersinterface (UI).
