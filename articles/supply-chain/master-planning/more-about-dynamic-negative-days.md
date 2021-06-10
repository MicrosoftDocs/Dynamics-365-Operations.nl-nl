---
title: Negatieve dagen en dynamische negatieve dagen
description: In dit onderwerp vindt u informatie over negatieve dagen en dynamische negatieve dagen en hoe u deze kunt gebruiken om uw bedrijf te helpen.
author: ChristianRytt
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37ae6ebd4347d3bbb414b7f1e4e0d54150878c02
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097229"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Negatieve dagen en dynamische negatieve dagen

[!include [banner](../includes/banner.md)]

In dit onderwerp vindt u informatie over negatieve dagen en dynamische negatieve dagen en hoe u deze kunt gebruiken om uw bedrijf te helpen. De *time fence voor negatieve dagen* staat voor het aantal dagen dat u bereid bent om te wachten voordat u nieuwe aanvulling bestelt wanneer u negatieve voorraad hebt.

Dit onderwerp omvat de volgende informatie:

- Hoe geplande orders worden gemaakt
- De correlatie tussen de time fence voor negatieve dagen en de levertijd van het artikel
- De manier waarop de time fence voor dynamische negatieve dagen wordt berekend en hoe de levertijd van het artikel in de berekening wordt meegenomen
- Hoe u de [suggesties voor het verbeteren van de uitvoeringstijd voor materiaalbehoeftenplanning (material requirements planning; MRP) (hoofdplanning)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) kunt interpreteren die zijn gerelateerd aan negatieve dagen

In dit onderwerp worden drie hypothetische scenario's gebruikt om u te helpen bij het begrijpen van deze informatie. Het verschil tussen de scenario's is het punt waarop u vraag krijgt: vóór, gedurende of na de doorlooptijd van het artikel.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>Scenario 1: U krijgt vraag vóór de levertijd van het artikel

U kunt al relatief vroeg in de levertijd van uw artikel of vlak voor het begin van de levertijd vraag krijgen. Hier volgt een voorbeeld van dit scenario:

- Het artikel Demoproduct heeft een inkooplevertijd van zes dagen.
- Op dag nul (1 januari) is het voorraadniveau voor het artikel Demoproduct 0 (nul).
- Op dag nul (1 januari) krijgt u een verkooporder voor een hoeveelheid van 10 voor het artikel Demoproduct.
- Op dag 7 (8 januari) is er een bestaande inkooporder voor een hoeveelheid van 10 van het artikel Demoproduct.

De volgende afbeelding toont een grafische weergave van dit scenario.

![Grafische weergave van scenario 1](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Geval A: Minder negatieve dagen dan de levertijd van het artikel

Als u de negatieve dagen instelt op een waarde kleiner dan de levertijd van het artikel, wordt er gezocht naar ontvangsten voor het artikel Demoproduct binnen de time fence voor negatieve dagen. Omdat er geen ontvangsten worden gevonden, wordt door MRP een nieuwe geplande inkooporder gemaakt. Deze geplande order wordt onmiddellijk met zes dagen uitgesteld (de levertijd). Daarom komt deze aan op 7 januari. De bestaande inkooporder krijgt een actiebericht **Annuleren** omdat deze door de nieuwe geplande inkooporder overbodig is geworden.

De volgende afbeelding is een schermafbeelding van dit geval.

![Schermopname van geval A voor scenario 1](./media/negative-days-2.png)

De volgende afbeelding toont een grafische weergave van wat er gebeurt in dit geval.

![Grafische weergave van geval A voor scenario 1](./media/negative-days-3.png)

Als u naar MRP-prestaties en plannervositeit kijkt, presteert dit geval niet goed. Er moet een nieuwe geplande order worden gemaakt en de vertragingen en acties moeten worden berekend. Deze taken zijn tijdrovend. Dit geval voegt ook nog twee transacties aan uw plan toe. Aan de andere kant wordt de verkooporder slechts zes dagen uitgesteld, niet zeven.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Geval B: Meer negatieve dagen dan de levertijd van het artikel

Om de MRP-prestaties te verbeteren, kunt u de negatieve dagen instellen op een waarde die hoger is dan de levertijd van het artikel. Omdat u de voorraad niet binnen de levertijd in dit scenario kunt krijgen, kunt u naar ontvangsten zoeken zolang deze zoekactie zinvol is. Hoewel de uitvoeringstijd voor MRP korter is, moet u waakzaam zijn voor extra vertragingen voor de orders.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Geval C: De levertijd van het artikel automatisch relateren aan de time fence voor negatieve dagen

Gebruik dynamische negatieve dagen om de levertijd van het artikel automatisch te relateren aan de time fence voor negatieve dagen Als u dynamische, negatieve dagen wilt gebruiken, gaat u naar **Hoofdplanning \> Instellen \> Hoofdplanningsparameters** en stelt u op het tabblad **Algemeen** in de sectie **Dekking** de optie **Dynamische negatieve dagen gebruiken** in op **Ja**. Vervolgens wordt naar ontvangsten gezocht in de time fence voor dynamische negatieve dagen. Deze time fence wordt met de volgende formule berekend:

Time fence voor dynamische negatieve dagen = Inkooplevertijd + Time fence voor negatieve dagen + (Huidige datum – Behoeftedatum)

(Als het standaardordertype van het artikel Demoproduct **Productie** of **Overboeking** is, wordt de levertijd de **voorraadlevertijd**.)

Wanneer dynamische negatieve dagen worden gebruikt, wordt als time fence voor ontvangsten nu 6 + 2 + 0 = 8 dagen gebruik. MRP zoekt de bestaande inkooporder en vergelijkt de verkooporder hiermee. Er worden geen nieuwe geplande orders gemaakt. Daarom is de uitvoeringstijd voor MRP korter. In de volgende afbeelding ziet u de nettobehoeften voor het artikel Demoproduct.

![Nettobehoeften voor geval C voor scenario 1](./media/negative-days-4.png)

De volgende afbeelding toont een grafische weergave van wat er gebeurt in dit geval.

![Grafische weergave van geval C voor scenario 1](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Geval D: Alleen dynamische negatieve dagen gebruiken

Als u de negatieve dagen instelt op **0** (nul) en alleen de time fence voor dynamische negatieve dagen gebruikt, is de time fence van de dynamische negatieve dagen 6 + 0 + 0 = 6 dagen. In dit geval is het resultaat hetzelfde als het resultaat in geval A voor dit scenario. Er moet een nieuwe geplande order worden gemaakt en de vertragingen en acties moeten worden berekend. Deze taken zijn tijdrovend en kunnen ook frustrerend zijn. U hebt ook twee transacties meer om te verwerken. Omdat de vraag niet op tijd kan worden afgehandeld om het artikel te ontvangen, voegt dit geval overbodige complicaties aan uw plan toe.

De volgende afbeelding is een schermafbeelding voor dit geval.

![Schermopname van geval D voor scenario 1](./media/negative-days-6.png)

De volgende afbeelding toont een grafische weergave van wat er gebeurt in dit geval.

![Grafische weergave van geval D voor scenario 1](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Geval E: Meer negatieve dagen dan de levertijd van het artikel en de time fence voor dynamische negatieve dagen gebruiken

Als u de negatieve dagen instelt op een hogere waarde dan de levertijd van het artikel en u ook de time fence voor dynamische negatieve dagen gebruikt, is de time fence voor dynamische negatieve dagen 6 + 6 + 0 = 12 dagen. Deze benadering kan een zeer lange time fence produceren waarin naar resultaten moet worden gezocht. Zie de sectie [Conclusie](#conclusion) van dit onderwerp voor meer informatie over de manier waarop geval E betrekking heeft op een situatie waarin u de negatieve dagen instelt op een lange time fence.

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>Scenario 2: U krijgt vraag gedurende de levertijd van het artikel

U krijgt mogelijk vraag tijdens de levertijd van uw artikel. Hier volgt een voorbeeld van dit scenario:

- Het artikel Demoproduct heeft een inkooplevertijd van zes dagen. 
- Op dag nul (1 januari) is het voorraadniveau voor het artikel Demoproduct 0 (nul).
- Op dag vier (5 januari), binnen de levertijd van het artikel, krijgt u een verkooporder voor een hoeveelheid van 10 van het artikel Demoproduct.
- Op dag 8 (8 januari) is er een inkooporder voor een hoeveelheid van 10 van het artikel Demoproduct.

De volgende afbeelding toont een grafische weergave van dit scenario.

![Grafische weergave van scenario 2](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Geval A: Minder negatieve dagen dan de levertijd van het artikel

Als u de negatieve dagen instelt op een waarde kleiner dan de levertijd van het artikel, wordt er gezocht naar ontvangsten voor het artikel Demoproduct binnen de time fence voor negatieve dagen. Omdat er geen ontvangsten worden gevonden, wordt er een nieuwe geplande inkooporder gemaakt die de huidige datum als orderdatum gebruikt. Deze geplande order wordt onmiddellijk met zes dagen uitgesteld (de levertijd). Daarom komt deze aan op 7 januari. De bestaande inkooporder krijgt een actiebericht **Annuleren** omdat deze door de nieuwe geplande inkooporder overbodig is geworden.

De volgende afbeelding is een schermafbeelding voor dit geval.

![Schermopname van geval A voor scenario 2](./media/negative-days-9.png)

De volgende afbeelding toont een grafische weergave van wat er gebeurt in dit geval.

![Grafische weergave van geval A voor scenario 2](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Geval B: Meer negatieve dagen dan de levertijd van het artikel

Dit geval lijkt op geval B voor scenario 1. Als u de negatieve dagen instelt op een hogere waarde dan de levertijd van het artikel, krijgt u geen nieuwe geplande order. De verkooporder is gekoppeld aan de bestaande inkooporder.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Geval C: De levertijd van het artikel automatisch relateren aan de time fence voor negatieve dagen

Dit geval lijkt op geval C voor scenario 1, omdat dynamische negatieve dagen net zo goed werken als in dat geval. De time fence voor dynamische negatieve dagen is nu 6 + 2 – 4 = 4 dagen. Als u deze aanpak gebruikt, wordt de bestaande inkooporder gevonden en wordt de verkooporder hieraan gekoppeld. Omdat er geen nieuwe geplande orders worden gemaakt, is de uitvoeringstijd voor MRP korter.

De volgende afbeelding is een schermafbeelding van dit geval.

![Schermopname van geval C voor scenario 2](./media/negative-days-11.png)

De volgende afbeelding toont een grafische weergave van wat er gebeurt in dit geval.

![Grafische weergave van geval C voor scenario 2](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Geval D: Alleen dynamische negatieve dagen gebruiken

Als u de negatieve dagen instelt op **0** (nul) en alleen de time fence voor dynamische negatieve dagen gebruikt, is de time fence van de dynamische negatieve dagen nu 6 + 0 – 4 = 2 dagen. In dit geval is het resultaat hetzelfde als het resultaat in geval A voor dit scenario. Zie geval A voor een grafische weergave van wat er gebeurt.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Geval E: Meer negatieve dagen dan de levertijd van het artikel en de time fence voor dynamische negatieve dagen gebruiken

Als u de negatieve dagen instelt op een hogere waarde dan de levertijd van het artikel en u ook de time fence voor dynamische negatieve dagen gebruikt, is de time fence voor dynamische negatieve dagen 6 + 6 – 4 = 8 dagen. Deze benadering kan een zeer lange time fence produceren waarin naar resultaten moet worden gezocht. Zie de sectie [Conclusie](#conclusion) van dit onderwerp voor meer informatie over de manier waarop geval E betrekking heeft op een situatie waarin u de negatieve dagen instelt op een lange time fence.

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>Scenario 3: U krijgt vraag na de levertijd van het artikel

U kunt vraag krijgen na de levertijd van het artikel. Hier volgt een voorbeeld van dit scenario:

- Het artikel Demoproduct heeft een inkooplevertijd van zes dagen.
- Op dag nul (1 januari) is de voorraad voor het artikel Demoproduct 0 (nul).
- Op dag zeven (8 januari), buiten de levertijd van het artikel, krijgt u een verkooporder voor een hoeveelheid van 10 van het artikel Demoproduct.
- Op dag tien (11 januari) is er een inkooporder voor een hoeveelheid van 10 van het artikel Demoproduct.

De volgende afbeelding toont een grafische weergave van dit scenario.

![Grafische weergave van scenario 3](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Geval A: Minder negatieve dagen dan de levertijd van het artikel

Als u de negatieve dagen instelt op een waarde kleiner dan de levertijd van het artikel, wordt er twee dagen vóór de behoeftedatum van de verkooporder gezocht. Omdat er niets wordt gevonden, wordt door MRP op 2 januari een geplande inkooporder gemaakt. Deze geplande inkooporder wordt net op tijd verzonden om aan de verkoopordervraag te voldoen. De bestaande inkooporder krijgt een actiebericht **Annuleren** omdat deze niet vereist is.

De volgende afbeelding is een schermafbeelding van dit geval.

![Schermopname van geval A voor scenario 3](./media/negative-days-14.png)

De volgende afbeelding toont een grafische weergave van wat er gebeurt in dit geval.

![Grafische weergave van geval A voor scenario 3](./media/negative-days-15.png)

> [!NOTE]
> In de vorige schermafbeelding is de behoeftedatum van de inkooporder 12 januari. Omdat deze schermopname is gemaakt in 2015, toen 11 januari op een zondag viel, werd de behoeftedatum verplaatst naar de volgende werkdag, maandag 12 januari. Desondanks heeft de inkooporder als leveringsdatum 11 januari.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Geval B: Meer negatieve dagen dan de levertijd van het artikel

Als u de negatieve dagen instelt op een hogere waarde dan de levertijd van het artikel, krijgt u geen nieuwe geplande order. De verkooporder wordt getraceerd voor de bestaande inkooporder. Daarom wordt de verkooporder vertraagd. Als u een geplande order maakt, kunt u de verkooporder op tijd verzenden.

De volgende afbeelding is een schermafbeelding van dit geval.

![Schermopname van geval B voor scenario 3](./media/negative-days-16.png)

De volgende afbeelding toont een grafische weergave van wat er gebeurt in dit geval.

![Grafische weergave van geval B voor scenario 3](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Geval C: De levertijd van het artikel automatisch relateren aan de time fence voor negatieve dagen

Dit geval lijkt op geval C voor scenario 1, omdat dynamische negatieve dagen minstens zo goed werken als in geval B voor dit scenario.

De time fence voor dynamische negatieve dagen is 6 + 2 – 7 = 1 dag. In dit geval houdt het systeem echter nog steeds rekening met de levertijd voor negatieve dagen (2) omdat MRP kijkt naar de maximale waarde tussen de levertijd voor negatieve dagen en de levertijd voor dynamische negatieve dagen. Daarom is het resultaat in dit geval hetzelfde als het resultaat in geval A voor dit scenario.

De volgende afbeelding toont een grafische weergave van wat er gebeurt in dit geval.

![Grafische weergave van geval C voor scenario 3](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Geval D: Alleen dynamische negatieve dagen gebruiken

Als u de negatieve dagen instelt op **0** (nul) en alleen de time fence voor dynamische negatieve dagen gebruikt, is de time fence van de dynamische negatieve dagen nu 6 + 0 – 7 = -1 dag. In dit geval houdt het systeem nog steeds rekening met de levertijd van negatieve dagen (2). Daarom is het resultaat in dit geval hetzelfde als het resultaat in geval A voor dit scenario, met dezelfde nadelen. Zie geval A voor scenario 2 voor een grafische weergave van wat er gebeurt.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Geval E: Meer negatieve dagen dan de levertijd van het artikel en de time fence voor dynamische negatieve dagen gebruiken

Dit geval komt overeen met geval E voor scenario´s 1 en 2. Het biedt dezelfde voordelen en nadelen.

## <a name="conclusion"></a>Conclusie

Zoals de drie scenario's in dit onderwerp laten zien, is het een goed idee om de negatieve dagen in te stellen op een waarde die hoger is dan de levertijd van de artikelen in de behoefteplanningsgroep. Het is ook een goed idee om alleen dynamische negatieve dagen te gebruiken en om de negatieve dagen in te stellen op het aantal dagen dat u bereid bent om wachten voordat u een nieuwe aanvulling bestelt wanneer u een negatieve voorraad hebt (met andere woorden, het aantal dagen dat u bereid bent om vraag verder uit te stellen). Daarnaast moeten artikelen in dezelfde behoefteplanningsgroep dezelfde levertijden hebben.

Als u de negatieve dagen instelt op **0** (nul) en geen dynamische negatieve dagen gebruikt, wordt er in MRP altijd een nieuwe geplande order gemaakt om aan de vraag te voldoen. In deze situatie is het belangrijk dat u werkt met de actieberichten om er zeker van te zijn dat u voorraad niet ophoopt.

U kunt voor de negatieve dagen een lange time fence instellen en vervolgens werken met de actieberichten. Deze aanpak levert goede planningsresultaten op, maar is ook een beetje langzamer. Analyseren kan ook moeilijker worden, omdat u de actieberichten moet analyseren en toepassen. Dit is een voorbeeld:

- Het artikel Demoproduct heeft een inkooplevertijd van zes dagen.
- Op dag nul (1 januari) is de voorraad voor het artikel Demoproduct 0 (nul).
- Op dag nul (1 januari) krijgt u een verkooporder voor een hoeveelheid van 10 voor het artikel Demoproduct.
- Op dag negen (10 januari) krijgt u een verkooporder voor een hoeveelheid van 10 voor het artikel Demoproduct.
- Op dag elf (12 januari) is er een inkooporder voor een hoeveelheid van 10 van het artikel Demoproduct.
- Negatieve dagen worden ingesteld op **20**, wat veel meer is dan de levertijd van het artikel.

De volgende afbeelding toont een grafische weergave van wat er gebeurt.

![Grafische beoordeling van het voorbeeld](./media/negative-days-19.png)

MRP produceert de volgende resultaten.

![Resultatenvoorbeeld 1](./media/negative-days-20.png)

In de voorgaande schermafbeelding is de behoeftedatum van de verkooporder 9 januari in plaats van 10 januari. Omdat deze schermopname is gemaakt in 2015, toen 10 januari op een zaterdag viel, moet de behoeftedatum van de order naar de vorige werkdag, vrijdag 9 januari, worden verplaatst.

Met MRP wordt een geplande inkooporder gemaakt om te voldoen aan de vraag van de eerste verkooporder, maar vervolgens wordt u ook aangeraden de geplande order te annuleren, omdat u de bestaande inkooporder kunt vervroegen en de hoeveelheid hiervan kunt verhogen.

De resultaten zijn niet onjuist, maar de uitvoeringstijd voor MRP kan langer zijn omdat in MRP alle vertragingen en suggesties moeten worden gemaakt. Bovendien kan de planner meer tijd nodig hebben om de MRP-resultaten te begrijpen. In dit geval is het vooral van essentieel belang dat de planner de planningsberichten begrijpt en gebruikt.

Als u de negatieve dagen verlaagt tot een getal dat dichter bij de levertijd van het artikel ligt en u dynamische negatieve dagen gebruikt, produceert MRP de volgende resultaten.

![Resultatenvoorbeeld 2](./media/negative-days-21.png)

Er wordt een geplande order gemaakt die aan de eerste verkooporder is gekoppeld. Vervolgens wordt, zoals verwacht, de behoefte van de tweede verkooporder getraceerd voor de bestaande inkooporder, op basis van de instelling voor negatieve dagen. Dit planningsresultaat is ook correct en de uitvoeringstijd voor MRP is mogelijk korter. In dit geval is het niet van essentieel belang dat u begrijpt en weet hoe u met de actieberichten werkt.

Om te garanderen dat de juiste waarden voor uw bedrijf worden ingevoerd, moet u rekening houden met zowel functionaliteit als MRP-uitvoeringstijd. Daarom kan het even duren om de optimale waarden te bepalen.

## <a name="see-also"></a>Zie ook

Zie voor meer informatie het oorspronkelijke blogbericht [More about (dynamic) negative days](/archive/blogs/axmfg/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
