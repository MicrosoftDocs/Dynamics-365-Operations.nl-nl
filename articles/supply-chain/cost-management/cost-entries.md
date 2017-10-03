---
title: Kosteninvoer
description: Dit artikel biedt informatie over kosteninvoer en wanneer deze wordt gemaakt. Kosteninvoer is een record waarin de hoeveelheid en kosten van een bepaalde gebeurtenis worden geregistreerd.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1045ecbf7080f12bc60336609180173544e4e0eb
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="cost-entries"></a>Kosteninvoer

[!include[banner](../includes/banner.md)]


Dit artikel biedt informatie over kosteninvoer en wanneer deze wordt gemaakt. Kosteninvoer is een record waarin de hoeveelheid en kosten van een bepaalde gebeurtenis worden geregistreerd.

Kosteninvoer zijn aggregaties van voorraadtransacties die op actieve financiële voorraaddimensies worden geregistreerd.

## <a name="examples"></a>Voorbeelden
### <a name="example-1-no-cost-entries-are-created"></a>Voorbeeld 1: Er wordt geen kosteninvoer gemaakt

Een overboekingsjournaalgebeurtenis wordt geregistreerd. De gebeurtenis boekt een onderdeel van artikel A van locatie A naar locatie B over. De Locatievoorraaddimensie wordt niet als een onderdeel van het kostenobject beschouwd. Daarom maakt de gebeurtenis twee voorraadtransacties en geen kosteninvoer.

### <a name="example-2-cost-entries-are-created"></a>Voorbeeld 2: Er wordt kosteninvoer gemaakt

Een overboekingsjournaalgebeurtenis wordt geregistreerd. Met de gebeurtenis wordt een onderdeel van artikel A van locatie 1 naar locatie 2 overgeboekt. De locatievoorraaddimensie wordt als een onderdeel van het kostenobject beschouwd. Daarom maakt de gebeurtenis twee voorraadtransacties en twee kostengegevens.

### <a name="example-3-one-cost-entry-is-created"></a>Voorbeeld 3: Er wordt één kosteninvoer gemaakt

Een productontvangstbongebeurtenis wordt geregistreerd voor een inkooporder. De gebeurtenis registreert 100 stuks van artikel A tegen eenheidskosten van 10,00 Amerikaanse dollar (USD). Omdat artikel A een serienummer gebruikt om het doel van voorraadbeheer te volgen, wordt een uniek serienummer gemaakt voor elk artikel dat wordt ontvangen. Daarom maakt de gebeurtenis 100 voorraadtransacties en één kosteninvoer.

## <a name="cost-entries-page"></a>Pagina Kosteninvoer
Op de nieuwe pagina **Kosteninvoer** kunt u registraties van hoeveelheden en kosten weergeven en beheren. Deze pagina vult de pagina **Voorraadtransactie** en **Vereffening voorraad** aan. De records worden in chronologische volgorde geregistreerd voor een gebeurtenis. Daarom kunt u de samengevoegde kosten van een specifieke gebeurtenis of alle gebeurtenissen snel zoeken en controleren die aan een document zijn gekoppeld. Dit is een voorbeeld:

-   Een productontvangstbongebeurtenis is geregistreerd voor artikel A. Honderd stuks worden ontvangen tegen eenheidskosten van 10,00 USD.
-   Een aantal dagen na factuur wordt de gebeurtenis geregistreerd, de kosten worden verhoogd naar 11,00 USD. Daarom is het totaalbedrag 1100 USD. Een tweede boekstuk is gemaakt om het verschil van 100 USD te verantwoorden.
-   Een aantal dagen later wordt een diverse toeslagen van 15,00 USD geregistreerd om de transportkosten op de inkooporder te dekken.

| Boekstuk | Datum       | Verwijzing      | Nummer | Partij-ID  | Hoeveelheid | Bedrag  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01-01-2015 | Inkooporder | 100001 | 0000101 | 100,00   | 1000.00 |
| 00002   | 20-01-2015 | Inkooporder | 100001 | 0000101 |          | 100,00  |
| 00003   | 31-01-2015 | Correctie     | 100001 | 0000101 |          | 15,00   |

Op de pagina **Kosteninvoer** kunt u filteren op document-ID en documentdatum. 

> [!NOTE]
> Kosteninvoer is alleen beschikbaar voor [kostenobjecten](cost-object.md) of vrijgegeven producten.

<a name="see-also"></a>Zie ook
--------

[Kostenobjecten](cost-object.md)



