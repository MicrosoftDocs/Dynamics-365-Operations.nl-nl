---
title: Degressieve afschrijving na een splitsing
description: In dit onderwerp wordt de methode beschreven die wordt gebruikt in vaste activa om de afschrijving te berekenen nadat een activum is gesplitst met de methode degressieve afschrijving.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b3a8fe37ae97cf3b14f5121274603cd30de3304b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356770"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Degressieve afschrijving na een splitsing

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de methode beschreven die wordt gebruikt in vaste activa om de afschrijving te berekenen nadat een activum is gesplitst naar een ander activum met de methode degressieve afschrijving. Het afschrijvingsjaar dat in het activa boek is geconfigureerd, is het fiscaal jaar. Zie [Degressieve afschrijving](reduce-balance-depreciation.md) en [Een vast activum splitsen](tasks/split-fixed-asset.md) voor meer informatie.

Als u een vast activum splitst tijdens een boekperiode die later is dan de periode waarin het activum is aangeschaft, wordt met de degressieve afschrijving rekening gehouden met de netto boekwaarde (NBW) van het activum voor het vorige jaar. Er wordt ook rekening gehouden met de verwervings- en afschrijvingscorrectietransacties die zijn gegenereerd op basis van de transactie waarmee het activum is gesplitst. Bij dit gedrag wordt ervan uitgegaan dat het activum in één fiscaal jaar is verworven en in een later fiscaal jaar is opgesplitst. Het bedrag dat moet worden afgeschreven voor het oorspronkelijke activum na de splitsing weerspiegelt de NBW van het activum voordat het activum is gesplitst, en de verwervings- en afschrijvingscorrectietransactie die voor de splitsing is geboekt.

De volgende voorwaarden zijn bijvoorbeeld van toepassing:

- De boekperiode is van 30 juni tot 1 juli.
- Het degressieve saldopercentage is 18 procent en een activum wordt verworven in juni 2019 tegen een verwervingsprijs van $10.000,-.
- De afschrijving van het eerste fiscale jaar is gelijk aan $18.000,-, de maandelijkse afschrijving is $150,- en het activum wordt vervolgens afgeschreven tot november 2019 in de hoeveelheid $738,75.
- In november 2019 wordt 80 procent van het activum opgesplitst in andere vaste activa.

[![Degressieve afschrijving na een splitsing.](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Het bedrag dat moet worden afgeschreven voor het oorspronkelijke activum, is $1.822,25. Dit bedrag is gelijk aan de NBW voordat de gesplitste transactie is geboekt ($9.111,25), plus de verwervingscorrectie die wordt gegenereerd tijdens het boeken van de gesplitste transactie (-$8.000,-), plus de afschrijvingscorrectie die wordt gegenereerd tijdens de gesplitste transactie ($711,-). Daarom is de afschrijving voor het tweede jaar (1.822,25 × 18 procent) ÷ 12 = $27,33.

Het bedrag dat moet worden afgeschreven voor het nieuwe vaste activum in het eerste jaar is (8.000 × 18 procent) ÷ 12 = $120.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]