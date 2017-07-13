---
title: Kostenobjecten
description: Dit artikel biedt informatie over kostenobjecten en uitleg over hoe kosten en hoeveelheden worden samengevoegd. Een kostenopject is een entiteit waarvoor kosten en hoeveelheden worden samengevoegd. Een kostenobjectentiteit kan een product of productvarianten, zoals varianten voor stijl en kleur, zijn.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 823d3edd106925339607d01fbf5f1921b85ff244
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---

# <a name="cost-objects"></a>Kostenobjecten

[!include[banner](../includes/banner.md)]


Dit artikel biedt informatie over kostenobjecten en uitleg over hoe kosten en hoeveelheden worden samengevoegd. Een kostenopject is een entiteit waarvoor kosten en hoeveelheden worden samengevoegd. Een kostenobjectentiteit kan een product of productvarianten, zoals varianten voor stijl en kleur, zijn.  

<a name="cost-objects"></a>Kostenobjecten
------------

De pagina **Kostenobjecten** bevat alle kostenobjecten die op een product worden geregistreerd. De kostenobjecten worden gedefinieerd door gegevens uit de volgende bronnen:

-   Artikel
-   Productdimensiegroep
-   Opslagdimensiegroep
-   Traceringsdimensiegroep

**Opmerking:** een kostenobject vertegenwoordigt alleen een kostenelement van het type **Direct materiaal**. Een kostenobject en een voorraadobject verschillen daarin dat een kostenobject wordt gedefinieerd door de voorraaddimensies die voor financiële voorraad worden geselecteerd. Een artikel heeft bijvoorbeeld de volgende configuratie:

-   **Locatie:** Fysieke voorraad = Ja, Financiële voorraad = Ja
-   **Magazijn:** Fysieke voorraad = Ja, Financiële voorraad = Nee
-   **Batchnr.:** Fysieke voorraad = Ja, Financiële voorraad = Nee

De volgende tabel toont wat een kostenobject is en wat een voorraadobject is.

| Objecttype      | Artikelnummer | Locatie | Magazijn | Batchnr. |
|------------------|-------------|------|-----------|-----------|
| Kostenobject      | x           | x    |           |           |
| Voorraadobject | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Samenvoeging van kosten en hoeveelheden
-   De waarde in het veld **Waarde** is een som van de volgende waarden:
    -   Fysieke kostprijs
    -   Financiële kostprijs
    -   Correcties
-   De waarde in het veld **Hoeveelheid** is een som van de volgende waarden:
    -   Ontvangen
    -   Ingehouden
    -   Boekingshoeveelheid
-   Het veld **Gemiddelde eenheidskosten** is een berekend veld. De waarde wordt berekend door de waarde **Waarde** te delen door de waarde **Hoeveelheid**.

**Opmerking:** de parameter Fysieke waarde opnemen is niet van invloed op de eerdere berekeningen.

<a name="see-also"></a>Zie ook
--------

[Productdimensiegroep](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Opslagdimensiegroep](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Traceringsdimensiegroep](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Wat is nieuw of gewijzigd](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)

[Kosteninvoer](cost-entries.md)




