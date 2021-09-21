---
title: U kunt niet meerdere productontvangstbonnen in één inkooporder consolideren
description: U kunt niet meerdere productontvangstbonnen consolideren in één inkooporder als de verschillende productontvangstbonregels verschillende boekingsdatums hebben.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475981"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>U kunt niet meerdere productontvangstbonnen in één inkooporder consolideren

## <a name="symptoms"></a>Symptomen

U kunt niet meerdere productontvangstbonnen consolideren in één inkooporder als de verschillende productontvangstbonregels verschillende boekingsdatums hebben.

## <a name="resolution"></a>Oplossing

In eerdere versies van Dynamics 365 Supply Chain Management was consolidatie in deze situatie toegestaan. Dit bleek is echter foutgevoelig te zijn. De boekhoudingsdatum op de gemaakte inkooporderregels mag niet verschillen van de boekhoudingsdatum op de productontvangstbonregels waarop deze inkooporderregels zijn gemaakt. (De boekhoudingsdatum op de inkooporderregels komt overeen met de boekhoudingsdatum in de koptekst van de inkooporder.) De consolidatie van meerdere productontvangstbonnen in één inkooporder is daarom niet meer toegestaan.

De boekhoudingsdatum wordt bijvoorbeeld gebruikt voor budgetreserveringen en vordering. Daarom moet deze tijdens de overgang van productontvangstbon naar de inkooporder worden bewaard.
