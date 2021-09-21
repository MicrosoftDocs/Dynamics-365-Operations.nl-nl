---
title: Eenheidsprijzen op inkooporders worden niet berekend op basis van de eenheidsomrekening
description: Eenheidsprijzen op inkooporders worden niet berekend op basis van de eenheidsomrekening
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
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476007"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Eenheidsprijzen op inkooporders worden niet berekend op basis van de eenheidsomrekening

## <a name="symptoms"></a>Symptomen

Wanneer een eenheid op een inkooporder wordt gewijzigd, worden de prijzen van handelsovereenkomsten niet opnieuw berekend volgens de definities van eenheidsomrekeningen.

## <a name="cause"></a>Oorzaak

Prijzen worden altijd opgehaald uit handelsovereenkomsten (of andere prijsinstellingen in het systeem, zoals verkoopovereenkomsten of artikelprijzen) en worden ingesteld voor een eenheid.

Als de eenheid op een orderregel wordt gewijzigd, zoekt het systeem naar een prijs voor de nieuwe eenheid, waarna die prijs wordt toegepast. Als er geen prijs voor de eenheid wordt gevonden, past het systeem geen prijs toe. De eenheidsomrekening kan niet worden gebruikt om de prijs opnieuw te berekenen in een andere eenheid. Theoretisch gezien zou de prijs voor één doos van tien niet gelijk kunnen zijn aan tien maal de prijs van één doos.

## <a name="workaround"></a>Tijdelijke oplossing

Een manier om dit probleem te omzeilen is ervoor te zorgen dat er handelsovereenkomsten bestaan voor de eenheden die u verwacht op orderregels voor het artikel.
