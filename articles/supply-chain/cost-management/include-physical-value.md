---
title: Fysieke waarde opnemen
description: U kunt het selectievakje Fysieke waarde opnemen op het sneltabblad Voorraadmodel van het formulier Artikelmodelgroepen gebruiken om op te geven of fysiek bijgewerkte transacties moeten worden meegenomen wanneer de actieve gemiddelde kostprijs van een artikel wordt berekend.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2d45e7a56851f3f4ac7a7d2d8c4ca9f23b6535fc
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="include-physical-value"></a>Fysieke waarde opnemen

[!include[banner](../includes/banner.md)]


U kunt het selectievakje Fysieke waarde opnemen op het sneltabblad Voorraadmodel van het formulier Artikelmodelgroepen gebruiken om op te geven of fysiek bijgewerkte transacties moeten worden meegenomen wanneer de actieve gemiddelde kostprijs van een artikel wordt berekend.

Het selectievakje **Fysieke waarde opnemen** heeft de volgende waarden.

| Waarde    | Resultaat                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Geselecteerd | Zowel fysiek als financieel bijgewerkte transacties worden gebruikt om de actieve gemiddelde kostprijs te berekenen. |
| Uitgeschakeld  | Alleen financieel bijgewerkte transacties worden gebruikt om de actieve gemiddelde kostprijs te berekenen.                                     |

Het in- of uitschakelen van het selectievakje heeft enigszins verschillende resultaten, afhankelijk van het voorraadmodel dat u gebruikt.

-   Als u het selectievakje **Fysieke waarde opnemen** inschakelt wanneer u het FIFO (First in, first out)-, LIFO (Last in, first out)- of LIFO-datumvoorraadmodel gebruikt, worden ook fysiek bijgewerkte transacties aangepast wanneer u de voorraad sluit.
-   Als u het selectievakje **Fysieke waarde opnemen** niet inschakelt wanneer u deze voorraadmodellen gebruikt, worden alleen financieel bijgewerkte transacties vereffend wanneer u de voorraad sluit.
-   Wanneer u het voorraadmodel gewogen gemiddelde of datum gewogen gemiddelde gebruikt, worden bij voorraadafsluiting altijd alleen financieel bijgewerkte transacties vereffend, ook al schakelt u het selectievakje **Fysieke waarde opnemen** in.

**Voorbeeld 1** U hebt het selectievakje**Fysieke waarde opnemen** ingeschakeld en u ontvangt de volgende inkooporders:

-   Een inkooporder voor 2 stuks tegen een kostprijs van EUR 10,00 die met de pakbon is bijgewerkt
-   Een inkooporder voor 3 stuks tegen een kostprijs van EUR 12,00 die volgens de factuur is bijgewerkt

In dit geval zal de actieve gemiddelde kostprijs EUR 11,20 zijn omdat zowel fysiek als financieel bijgewerkte transacties worden gebruikt om de kostprijs te berekenen. **Voorbeeld 2** U hebt het selectievakje **Fysieke waarde opnemen** niet ingeschakeld en de kostprijs in de artikelinstellingen is EUR 10,00. U ontvangt een inkooporder voor 20 stuks tegen een kostprijs van EUR 12,00 die met de pakbon is bijgewerkt. Wanneer een verkooporder wordt geboekt, is de geboekte kostprijs EUR 10,00 omdat de actieve gemiddelde kostprijs geen fysiek geboekte transacties omvat. **Opmerking:** Ter vergelijking: als u het selectievakje **Fysieke waarde opnemen** voor dit artikel selecteert wanneer een verkooporder wordt geboekt, is de geboekte kostprijs EUR 12.00.



