---
title: Gewogen gemiddelde datum inclusief fysieke waarde en markering
description: Datum gewogen gemiddelde is een voorraadmodel dat is gebaseerd op het principe van het gewogen gemiddelde, waarbij uitgiften worden berekend tegen de gemiddelde waarde van de artikelen die worden ontvangen in voorraad voor elke afzonderlijke dag in de afsluitingsperiode van de voorraad.
author: AndersGirke
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cf2206863d891eceb9c65ff879da3f9f72032b1
ms.sourcegitcommit: fcded93fc6c27768a24a3d3dc5cc35e1b4eff22b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/07/2022
ms.locfileid: "8391996"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Gewogen gemiddelde datum inclusief fysieke waarde en markering

[!include [banner](../includes/banner.md)]

*De gewogen gemiddelde datum* is een voorraadmodel dat is gebaseerd op een gemiddelde dat wordt berekend door elke component (artikeltransactie) te vermenigvuldigen met een factor (kostprijs) die het belang (hoeveelheid) weerspiegelt op elke dag van de periode. Met andere woorden wordt met dit voorraadmodel de kosten van uitgiftetransacties toegewezen op basis van de gemiddelde waarde van alle voorraad die elke dag word ontvangen, plus eventuele beschikbare voorraad van de vorige dag.

Wanneer u een voorraad afsluit met het voorraadmodel voor gewogen gemiddelde datum, kan een vereffening op twee manieren worden gemaakt. Gewoonlijk worden alle ontvangsten vereffend met een virtuele uitgifte, die de totaal ontvangen hoeveelheid en waarde bevat. Deze virtuele uitgifte heeft een bijbehorende virtuele ontvangst, waaruit de uitgiften worden vereffend. Op deze manier hebben alle uitgiften elke dag dezelfde gemiddelde kosten. De virtuele uitgifte en de virtuele ontvangst kunnen worden beschouwd als virtuele overboeking. Deze virtuele overboeking wordt ook wel *overboeking van gewogen gemiddelde eindvoorraad* genoemd. Deze vereffeningsmethode wordt daarom een *samengevatte vereffening van een gewogen gemiddelde* genoemd. Als er slechts één ontvangst is, kunnen alle uitgiften hiermee worden vereffend en wordt er geen virtuele overboeking gemaakt. Deze vereffeningsmethode wordt *directe vereffening* genoemd. Alle voorraad die na de voorraadafsluiting wordt uitgevoerd, wordt gewaardeerd op basis van het gewogen gemiddelde van de laatste dag van de vorige periode en opgenomen in de berekening van het gewogen gemiddelde datum in de volgende periode.

U kunt het principe van het gewogen gemiddelde datum overschrijven door voorraadtransacties te markeren zodat een specifieke artikelontvangst wordt vereffend met een specifieke uitgifte. Er is een periodieke voorraadafsluiting vereist wanneer u met het voorraadmodel voor gewogen gemiddelde datum vereffeningen maakt en de waarde van uitgiften aanpast volgens het principe van het gewogen gemiddelde datum. Totdat u de voorraadafsluiting hebt uitgevoerd, worden uitgiftetransacties gewaardeerd op basis van het lopende gemiddelde wanneer de fysieke en financiële updates hebben plaatsgevonden. Tenzij u markering gebruikt, wordt het lopende gemiddelde berekend wanneer de fysieke of financiële update wordt uitgevoerd.

De kostprijsberekeningsmethode voor gewogen gemiddelde datum wordt elke dag berekend met behulp van de volgende formule:

*Kosten* = \[(*Q*<sub>*b*</sub> × *P*<sub>*b*</sub>) + &#x2211;<sub>*n*</sub>(*Q*<sub>*n*</sub> × *P*<sub>*n*</sub>)\] ÷ (*Q*<sub>*b*</sub> + &#x2211;<sub>*n*</sub>*Q*<sub>*n*</sub>)

- *Q* = hoeveelheid van de transactie
- *P* = prijs van de transactie

Met andere woorden, de gewogen gemiddelde kostprijs is gelijk aan de beginhoeveelheid maal de beginprijs, plus de som van elke ontvangsthoeveelheid maal de ontvangstprijs, alle gedeeld door de beginhoeveelheid plus de som van de ontvangsthoeveelheden.

Tijdens de voorraadafsluiting wordt de berekening elke dag gedurende de afsluitperiode uitgevoerd.

> [!NOTE]
> Zie voor meer informatie over vereffeningen [Voorraad sluiten](inventory-close.md).

De volgende voorbeelden laten het effect zien van het gebruik van gewogen gemiddelde datum bij vijf configuraties:

- Datum gewogen gemiddelde directe vereffening zonder dat de optie **Fysieke waarde opnemen** wordt gebruikt
- Samengevatte vereffening op basis van een gewogen gemiddelde als de optie **Fysieke waarde opnemen** niet wordt gebruikt
- Datum gewogen gemiddelde directe vereffening waarbij de optie **Fysieke waarde opnemen** wel wordt gebruikt
- Datum gewogen gemiddelde samengevatte vereffening waarbij de optie **Fysieke waarde opnemen** wel wordt gebruikt
- Datum gewogen gemiddelde met gebruik van markering

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Datum gewogen gemiddelde directe vereffening zonder dat de optie Fysieke waarde opnemen wordt gebruikt

Met het directe-vereffeningsprincipe worden vereffeningen rechtstreeks tussen ontvangsten en uitgiften gemaakt zonder dat er extra voorraadtransacties worden gemaakt. Het principe voor directe vereffening wordt in de volgende situaties gebruikt:

- Eén ontvangst en een of meer uitgiften zijn in de periode geboekt.
- Er zijn alleen uitgiften in de periode geboekt en de voorraad bevat voorhanden artikelen uit een vorige afsluiting.

In dit voorbeeld is het selectievakje **Fysieke waarde opnemen** uitgeschakeld op de pagina **Artikelmodelgroep** voor het vrijgegeven product. Het volgende diagram geeft deze transacties weer:

**Dag 1:**

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 20,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 10,00 (lopend gemiddelde van financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 10,00 (lopend gemiddelde van financieel geboekte transacties).

**Dag 2:**

- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 20,00 per stuk (lopend gemiddelde van financieel geboekte transacties).

**Dag 3:**

- 7\. Voorraadafsluiting is uitgevoerd. Op basis van de methode gewogen gemiddelde datum wordt de directe-vereffeningsmethode gebruikt voor 30 december (30/12), omdat slechts één ontvangst financieel wordt bijgewerkt op 30/12. In dit voorbeeld wordt één vereffening gemaakt tussen de transacties 1b en 3b. Er wordt een correctie van USD 10,00 aangebracht om de waarde van transactie 3b op 20,00 te brengen. Er wordt geen correctie of vereffening gedaan op 31 december (31/12) omdat er geen financieel bijgewerkte uitgiften zijn op 31/12.

In het volgende diagram wordt deze reeks transacties geïllustreerd en ziet u de effecten van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van directe vereffening zonder de optie **Fysieke waarde opnemen**.

![Datum gewogen gemiddelde directe vereffening zonder de optie Fysieke waarde opnemen.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Uitleg bij het diagram:**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Datums worden gescheiden door dunne zwarte verticale lijnen. De datums worden onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met verticale rode streepjeslijnen.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Datum gewogen gemiddelde samengevatte vereffening zonder dat de optie Fysieke waarde opnemen wordt gebruikt

Als er meerdere ontvangsten zijn in een periode, wordt voor gewogen gemiddelde datums gebruikgemaakt van het principe met samengevatte vereffening waarbij alle ontvangsten van één dag worden samengevat in een transactie met de naam *Gewogen gemiddelde eindvoorraad*. Alle ontvangsten voor de dag worden vereffend met de uitgifte van deze nieuwe voorraadtransactie. Alle uitgiften voor de dag worden vereffend met de ontvangst van de nieuwe voorraadtransactie. Als er resterende voorhanden voorraad is na de voorraadafsluiting, wordt de waarde van de voorhanden voorraad opgenomen in de ontvangsttransactie van de gewogen gemiddelde eindvoorraad.

Het volgende diagram geeft deze transacties weer:

**Dag 1:**

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
- 2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 22,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).

**Dag 2:**

- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,00 (lopend gemiddelde van financieel geboekte transacties).

**Dag 3:**

- 7\. Voorraadafsluiting is uitgevoerd.
- 7a. Financiële uitgifte 'gewogen gemiddelde voorraadafsluitingstransactie' wordt gemaakt om de vereffeningen van alle financiële ontvangsten in voorraad bij elkaar op te tellen.

    - Transactie 1b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 10,00.
    - Transactie 2b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 22,00.
    - Transactie 7a wordt gemaakt voor een hoeveelheid van 2 met een vereffend bedrag van USD 32,00. Deze transactie compenseert het totaal van de twee ontvangsttransacties die financieel zijn bijgewerkt in de periode.

- 7b. Er wordt een gewogen gemiddelde voor een financiële ontvangst voorraadafsluitingstransactie het verschil voor financieel geboekte uitgiften gemaakt.

    - Transactie 3b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 16,00. Deze transactie is niet gecorrigeerd omdat dit het gewogen gemiddelde is van financieel geboekte transacties op 1 december (1/12).
    - Transactie 7b wordt gemaakt voor een hoeveelheid van 2 met een financieel bedrag van USD 32,00 en een vereffend bedrag van USD 16,00 voor tegentransactie 3b. Deze transactie compenseert het totaal van één uitgiftetransacties die financieel wordt bijgewerkt in de periode. De transactie blijft open omdat er nog één beschikbaar is.

In het volgende diagram wordt deze reeks transacties getoond en wordt aangegeven wat het effect is van het gebruik van het voorraadmodel van het gewogen gemiddelde en het samengevatte-vereffeningsprincipe zonder dat de optie **Fysieke waarde opnemen** wordt gebruikt.

![Datum gewogen gemiddelde samengevatte vereffening zonder de optie Fysieke waarde opnemen.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Uitleg bij het diagram:**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Datums worden gescheiden door dunne zwarte verticale lijnen. De datums worden onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met verticale rode streepjeslijnen.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Datum gewogen gemiddelde directe vereffening waarbij de optie Fysieke waarde opnemen wel wordt gebruikt

In de huidige versie van het product werkt de optie **Fysieke waarde opnemen** anders in combinatie met het voorraadmodel van de gewogen gemiddelde datum dan in eerdere versies van het product. Als u het selectievakje **Fysieke waarde opnemen** inschakelt voor een artikel op de pagina **Artikelmodelgroep** selecteert, worden fysiek bijgewerkte ontvangsten gebruikt bij het berekenen van de geraamde kostprijs van de uitgifte of het lopende gemiddelde. Uitgiften worden geboekt op basis van deze geraamde kostprijs tijdens de periode. Tijdens de voorraadafsluiting worden alleen de financieel bijgewerkte ontvangsten meegenomen in de berekening voor het gewogen gemiddelde.

Het volgende diagram geeft deze transacties weer:

**Dag 1:**

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 20,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 15,00 (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 15,00 (lopend gemiddelde van fysiek en financieel geboekte transacties).

**Dag 2:**

- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 21,25 per stuk (lopend gemiddelde van fysiek en financieel geboekte transacties).

**Dag 3:**

- 7\. Voorraadafsluiting is uitgevoerd. Op basis van de methode gewogen gemiddelde datum wordt de directe-vereffeningsmethode gebruikt voor 30 december (30/12), omdat slechts één ontvangst financieel wordt bijgewerkt op 30/12. In dit voorbeeld wordt één vereffening gemaakt tussen de transacties 1b en 3b. Er wordt geen correctie in de uitgifte aangebracht op 30-12. Er wordt ook geen correctie of vereffening gedaan op 31 december (31/12) omdat er geen financieel bijgewerkte uitgiften zijn op 31/12.

In het volgende diagram wordt deze reeks transacties geïllustreerd en ziet u de effecten van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van directe vereffening met de optie **Fysieke waarde opnemen**.

![Directe vereffening op basis van een gewogen gemiddelde met Fysieke waarde opnemen.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Uitleg bij het diagram:**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Datums worden gescheiden door dunne zwarte verticale lijnen. De datums worden onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met verticale rode streepjeslijnen.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Datum gewogen gemiddelde samengevatte vereffening waarbij de optie Fysieke waarde opnemen wel wordt gebruikt

In de huidige versie van het product werkt de optie **Fysieke waarde opnemen** anders met het gewogen gemiddelde dan in eerdere versies van het product. Als u het selectievakje **Fysieke waarde opnemen** inschakelt voor een artikel op de pagina **Artikelmodelgroep** selecteert, worden fysiek bijgewerkte ontvangsten gebruikt bij het berekenen van de geraamde kostprijs of het lopende gemiddelde. Uitgiften worden geboekt op basis van deze geraamde kostprijs tijdens de periode. Tijdens de voorraadafsluiting worden alleen de financieel bijgewerkte ontvangsten meegenomen in de berekening voor het gewogen gemiddelde. We raden u aan een maandelijkse voorraadafsluiting uit te voeren wanneer u het voorraadmodel van het gewogen gemiddelde gebruikt. In dit voorbeeld van een samengevatte vereffening op basis van een gewogen gemiddelde datum is het voorraadmodel gemarkeerd voor het opnemen van de fysieke waarde.

Het volgende diagram geeft deze transacties weer:

**Dag 1:**

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
- 2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 22,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van fysiek en financieel geboekte transacties).

**Dag 2:**

- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,67 (lopend gemiddelde van fysiek en financieel geboekte transacties).

**Dag 3:**

- 7\. Voorraadafsluiting is uitgevoerd.
- 7a. Financiële uitgifte 'gewogen gemiddelde voorraadafsluitingstransactie' wordt gemaakt om de vereffeningen van alle financiële ontvangsten in voorraad bij elkaar op te tellen.

    - Transactie 1b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 10,00.
    - Transactie 2b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 22,00.
    - Transactie 7a wordt gemaakt voor een hoeveelheid van 2 met een vereffend bedrag van USD 32,00. Deze transactie compenseert het totaal van de twee ontvangsttransacties die financieel zijn bijgewerkt in de periode.

- 7b. Er wordt een gewogen gemiddelde voor een financiële ontvangst voorraadafsluitingstransactie het verschil voor financieel geboekte uitgiften gemaakt.

    - Transactie 3b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 16,00. Deze transactie is niet gecorrigeerd omdat dit het gewogen gemiddelde is van financieel geboekte transacties op 1 december (1/12).
    - Transactie 7b wordt gemaakt voor een hoeveelheid van 2 met een financieel bedrag van USD 32,00 en een vereffend bedrag van USD 16,00 voor tegentransactie 3b. Deze transactie compenseert het totaal van één uitgiftetransacties die financieel wordt bijgewerkt in de periode. De transactie blijft open omdat er nog één beschikbaar is.

In het volgende diagram wordt deze reeks transacties geïllustreerd en ziet u de effecten van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van samengevatte vereffening zonder de optie **Fysieke waarde opnemen**.

![Samengevatte vereffening op basis van een gewogen gemiddelde met Fysieke waarde opnemen,](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Uitleg bij het diagram:**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Datums worden gescheiden door dunne zwarte verticale lijnen. De datums worden onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met verticale rode streepjeslijnen.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-date-when-marking-is-used"></a>Datum gewogen gemiddelde met gebruik van markering

Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markeren als u de exacte kosten van de voorraad wilt weten wanneer de transactie wordt geboekt of de voorraad wordt afgesloten.

De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor dit artikel betalen om aan de vraag van de klant te voldoen. U moet zeker weten dat de kosten van dit voorraadartikel worden weerspiegeld in de marge, of kosten van verkochte goederen, voor deze verkooporderfactuur.

Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van EUR 120,00. Als het verkooporderdocument voor de inkooporder wordt gemarkeerd voordat de pakbon of factuur wordt geboekt, bedragen de kosten van de verkochte goederen USD 120,00 in plaats van de huidige lopende gemiddelde kosten voor het artikel. Als de markering plaatsvindt nadat de pakbon of de factuur van de verkooporder wordt geboekt, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs.

Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd.

Als een ontvangsttransactie wordt gemarkeerd voor een uitgiftetransactie, wordt de waarderingsmethode die in de artikelmodelgroep voor het artikel is geselecteerd, genegeerd en worden deze transacties met elkaar vereffend.

U kunt een uitgiftetransactie aan een ontvangst koppelen voordat de transactie wordt geboekt. U kunt deze markering aanbrengen vanuit een verkooporderregel op de pagina **Details verkooporder**. De openstaande ontvangsttransacties kunnen worden bekeken op de pagina **Markering**.

U kunt ook een uitgiftetransactie aan een ontvangst koppelen nadat de transactie is geboekt. U kunt een uitgiftetransactie voor een openstaande ontvangsttransactie voor een geïnventariseerd artikel afstemmen of markeren vanuit een geboekt voorraadcorrectiejournaal.

Het volgende diagram geeft deze transacties weer:

**Dag 1:**

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
- 2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 22,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3c. Financiële voorraaduitgifte voor transactie 3b wordt gemarkeerd voor financiële voorraaduitgifte voor transactie 2b.

**Dag 2:**

- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,00 (lopend gemiddelde van financieel geboekte transacties).

**Dag 3:**

- 7\. Voorraadafsluiting is uitgevoerd. Op basis van het markeringsprincipe waarin de methode voor gewogen gemiddelde wordt gebruikt, worden de gemarkeerde transacties met elkaar vereffend. In dit voorbeeld wordt transactie 3b vereffend met transactie 2b en wordt een correctie voor USD 6,00 geboekt naar transactie 3b om de waarde op USD 22,00 te brengen. In dit voorbeeld worden er geen extra vereffeningen gemaakt, omdat door de afsluiting alleen vereffeningen worden gemaakt voor financieel bijgewerkte transacties.

In het volgende diagram worden voor deze reeks transacties de effecten weergegeven van het gebruik van het voorraadmodel voor datum gewogen gemiddelde met markering.

![Gewogen gemiddelde met markering.](media/weighted-average-date-with-marking.png)

**Uitleg bij het diagram:**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Datums worden gescheiden door dunne zwarte verticale lijnen. De datums worden onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met verticale rode streepjeslijnen.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
