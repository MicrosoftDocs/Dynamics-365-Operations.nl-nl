---
title: Kostenobjecten
description: Dit artikel biedt informatie over kostenobjecten en uitleg over hoe kosten en hoeveelheden worden samengevoegd. Een kostenopject is een entiteit waarvoor kosten en hoeveelheden worden samengevoegd. Een kostenobjectentiteit kan een product of productvarianten, zoals varianten voor stijl en kleur, zijn.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6829f24b8efa29b39f5ed742d8ca99e09bcef01
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910348"
---
# <a name="cost-objects"></a>Kostenobjecten

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over kostenobjecten en uitleg over hoe kosten en hoeveelheden worden samengevoegd. Een kostenopject is een entiteit waarvoor kosten en hoeveelheden worden samengevoegd. Een kostenobjectentiteit kan een product of productvarianten, zoals varianten voor stijl en kleur, zijn.  

## <a name="cost-objects"></a>Kostenobjecten

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

**Opmerking:** de parameter **Fysieke waarde opnemen** is niet van invloed op de eerdere berekeningen.

<a name="additional-resources"></a>Aanvullende resources
--------

[Productdimensiegroep](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[Opslagdimensiegroep](/dynamicsax-2012//storage-dimension-groups-form)

[Traceringsdimensiegroep](/dynamicsax-2012//tracking-dimension-groups-form)

[Wat is nieuw of gewijzigd](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[Kosteninvoer](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]