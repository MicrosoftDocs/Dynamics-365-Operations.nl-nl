---
title: Kostenobjecten
description: Dit artikel biedt informatie over kostenobjecten en uitleg over hoe kosten en hoeveelheden worden samengevoegd. Een kostenopject is een entiteit waarvoor kosten en hoeveelheden worden samengevoegd. Een kostenobjectentiteit kan een product of productvarianten, zoals varianten voor stijl en kleur, zijn.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8043c81057b5bb79f405642b199f80fc2fbcd8d4
ms.lasthandoff: 03/31/2017


---

# <a name="cost-objects"></a>Kostenobjecten

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

**opmerking:** de ** fysieke waarde opnemen ** parameter heeft geen effect op de voorgaande berekeningen.

<a name="see-also"></a>Zie ook
--------

[Product dimension group](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Storage dimension group](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Tracking dimension group](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Wat is nieuw of gewijzigd in Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

[Cost entries](cost-entries.md)


