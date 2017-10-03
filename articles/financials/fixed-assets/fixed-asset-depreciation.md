---
title: Afschrijving vaste activa
description: Dit onderwerp bevat een overzicht van de afschrijving van vaste activa.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a7f27847832e7c4814f1dc5982b6352c2ba98741
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="fixed-asset-depreciation"></a>Afschrijving vaste activa

[!include[banner](../includes/banner.md)]


Dit onderwerp bevat een overzicht van de afschrijving van vaste activa.

Afschrijving is een periodieke transactie die doorgaans de waarde van het vaste activum in de balans verlaagt en als uitgave in een winst-en-verliesrekening wordt geboekt. Daarom wordt een hoofdrekening gewoonlijk gebruikt voor de creditering van de periodieke afschrijving op de balans. Een tegenrekening is een rekening in het winst-en verliesgedeelte van het rekeningschema.

## <a name="depreciation-adjustment"></a>Afschrijvingscorrectie
Doorgaans wordt alleen een correctie op een geboekte afschrijvingstransactie geboekt als een afschrijvingsaanpassing. Daarom worden zowel de hoofdrekening als de tegenrekening ingesteld als de rekeningen voor de afschrijving. Een afschrijvingscorrectie kan een positief of negatief bedrag zijn, maar de functies van de hoofdrekening (als balansrekening) en van de tegenrekening (meestal als een winst-en-verliesrekening) blijven hetzelfde.

## <a name="extraordinary-depreciation"></a>Buitengewone afschrijving
Buitengewone afschrijving werkt hetzelfde als gewone afschrijving. Daarom wordt een hoofdrekening gebruikt om het afschrijvingsbedrag naar de balans te crediteren en de waarde van het vaste activum te verminderen. Een tegenrekening is een winst-en verliesrekening, waar de afschrijving die is berekend voor de fiscale periode, als een uitgave wordt geboekt. 

Buitengewone afschrijving werkt onafhankelijk van de basisafschrijving. Met buitengewone afschrijving als afzonderlijk transactietype kunt u de buitengewone afschrijving apart van de gewone basisafschrijving boeken en rapporteren.

## <a name="special-depreciation-allowance"></a>Speciale afschrijvingsaftrek
U kunt speciale afschrijvingsaftrekposten gebruiken om extra afschrijvingsbedragen af te schrijven gedurende het eerste jaar dat een activum in gebruik wordt genomen en wordt afgeschreven. Speciale afschrijvingsaftrekposten moeten vóór andere afschrijvingsberekeningen worden toegepast. Omdat de speciale afschrijvingsaftrekposten pas later in de gebruiksduur van het activum bekend worden, kunt u voor dit type afschrijving beter een boek gebruiken dat niet naar het grootboek boekt. U kunt de periodieke functie Transacties verwijderen die niet zijn geboekt naar grootboek gebruiken om de transactiehistorie te verwijderen voor deze boeken. U kunt de afschrijvingshistorie voor het vaste-activaboek vervolgens verwijderen, de speciale afschrijvingsaftrekposten boeken wanneer ze bekend zijn en dan de resterende afschrijvingstransacties voor het jaar boeken. 

U kunt net zoveel speciale afschrijvingsaftrekrecords maken als u wilt. Als u deze records toewijst aan een activagroepsboek, worden deze records op het activumboek toegepast. 

Een speciale afschrijvingsaftrek wordt als een percentage of een vast bedrag ingevoerd. Wanneer u afschrijvingsvoorstellen boekt, worden transacties voor speciale afschrijvingsaftrekposten naar het boek geboekt als transacties die los staan van de afschrijvingstransacties.

## <a name="depreciation-calendars"></a>Afschrijvingskalenders
Elk boek heeft een kalender die wordt gebruikt wanneer u vaste activa afschrijft. Het boek gebruikt standaard de fiscale kalender van het grootboek, als u geen kalender voor het boek opgeeft. U moet een fiscale kalender voor een boek selecteren, wanneer het afschrijvingsprofiel dat aan het boek is gekoppeld een afschrijvingsboekjaar gebruikt. 

U kunt gedeelde kalenders maken op de pagina **Fiscale kalenders** in Grootboek.

Zie voor meer informatie [Afschrijvingsmethoden en conventies](depreciation-methods-conventions.md).



