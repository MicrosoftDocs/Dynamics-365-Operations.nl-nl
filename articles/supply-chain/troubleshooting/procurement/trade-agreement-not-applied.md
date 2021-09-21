---
title: Voorwaarden van handelsovereenkomst worden niet toegepast op geïmporteerde orderregels
description: Prijzen en kortingen van handelsovereenkomsten worden niet toegepast op verkoop- of inkooporderregels die via gegevensbeheer worden geïmporteerd
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476040"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Voorwaarden van handelsovereenkomst worden niet toegepast op geïmporteerde orderregels

## <a name="symptoms"></a>Symptomen

Handelsovereenkomsten die van toepassing zijn op verkoop- of inkooporderregels, worden niet toegepast op regels die via gegevensbeheer worden geïmporteerd. Dezelfde handelsovereenkomsten worden echter wel toegepast op verkoop- of inkooporderregels die handmatig zijn gemaakt.

## <a name="cause"></a>Oorzaak

Als inkooporderregels die zijn geïmporteerd via gegevensbeheer al prijsgegevens bevatten, wordt de handelsovereenkomst niet opnieuw geëvalueerd voor deze regels. Als bijvoorbeeld **Regelkortingspercentage** of een van de prijs- en kortingswaarden voor een regel is ingesteld, worden er geen handelsovereenkomsten opgezocht voor die regel.

## <a name="workaround"></a>Tijdelijke oplossing

Dit gedrag is verwacht en treedt op voor zowel verkoop- als inkooporders.

U kunt dit probleem vermijden door de inkooporderregels te importeren zonder prijsgegevens in te stellen. De handelsovereenkomsten worden dan toegepast en de inkooporderregels worden bijgewerkt op basis van de gedefinieerde handelsovereenkomsten.
