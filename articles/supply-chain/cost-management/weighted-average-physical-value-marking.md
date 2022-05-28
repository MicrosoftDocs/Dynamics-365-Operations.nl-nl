---
title: Gewogen gemiddelde met fysieke waarde en markering
description: Het gewogen gemiddelde is een voorraadmodel dat is gebaseerd op het gewogen-gemiddeldeprincipe, waarbij uitgiften vanuit de voorraad worden gewaardeerd op de gemiddelde waarde van de artikelen die in de voorraad worden ontvangen gedurende de voorraadafsluitingsperiode, plus eventuele voorhanden voorraad van de vorige periode.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c80dcdc08432bb68478827c8763735e644aa4a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675258"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Gewogen gemiddelde met fysieke waarde en markering

[!include [banner](../includes/banner.md)]

Het gewogen gemiddelde is een voorraadmodel dat is gebaseerd op een gemiddelde dat resulteert uit de vermenigvuldiging van elke component (artikeltransactie) door een factor (kostprijs) die het belang (hoeveelheid) weerspiegelt. Een andere manier om dit te zeggen is dat het gewogen gemiddelde een voorraadmodel is dat de kosten van uitgiftetransacties toewijst op basis van de gemiddelde waarde van alle voorraad die tijdens de periode is ontvangen, plus eventuele beschikbare voorraad van de vorige periode.

Wanneer u een voorraad afsluit met het gewogen gemiddelde voorraadmodel, kan een vereffening op twee manieren worden gemaakt. Gewoonlijk worden alle ontvangsten vereffend met een virtuele uitgifte, die de totaal ontvangen hoeveelheid en waarde bevat. Deze virtuele uitgifte heeft een bijbehorende virtuele ontvangst, waarmee de uitgiften worden vereffend. Op deze manier hebben alle uitgiften dezelfde gemiddelde kosten. De virtuele uitgifte en ontvangst kunnen worden gezien als virtuele overboeking, die ook wel een *overboeking van gewogen gemiddelde eindvoorraad* wordt genoemd. Deze vereffeningsmethode wordt een *samengevatte vereffening van een gewogen gemiddelde* genoemd. Als er slechts één ontvangst is, kunnen alle uitgiften hiermee worden vereffend en wordt er geen virtuele overboeking gemaakt. Deze vereffeningsmethode wordt een *directe vereffening* genoemd. Alle voorraad die na de voorraadafsluiting wordt uitgevoerd, wordt gewaardeerd op basis van het gewogen gemiddelde van de vorige periode en opgenomen in de berekening van het gewogen gemiddelde in de volgende periode.

U kunt het principe van het gewogen gemiddelde overschrijven door voorraadtransacties te markeren zodat een specifieke artikelontvangst wordt vereffend met een specifieke uitgifte. Er is een periodieke voorraadafsluiting vereist wanneer u met het voorraadmodel voor gewogen gemiddelde vereffeningen maakt en de waarde van uitgiften aanpast volgens het principe van het gewogen gemiddelde. Totdat u het voorraadafsluitingsproces hebt uitgevoerd, worden uitgiftetransacties gewaardeerd op basis van het lopende gemiddelde wanneer de fysieke en financiële updates hebben plaatsgevonden. Tenzij u markering gebruikt, wordt het lopende gemiddelde berekend wanneer de fysieke of financiële update wordt uitgevoerd.

De gewogen gemiddelde kostprijsberekeningsmethode wordt berekend met behulp van de volgende formule:

- Gewogen gemiddelde = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = hoeveelheid van de transactie  
P = prijs van de transactie

Vereffeningen zijn voorraadafsluitingsboekingen die de uitgiften vanaf de sluitingsdatum bijwerken met het juiste gewogen gemiddelde. De volgende voorbeelden laten het effect van het gebruik van gewogen gemiddelden bij vijf verschillende configuraties zien:

- Directe vereffening op basis van een gewogen gemiddelde zonder de optie **Fysieke waarde opnemen**
- Samengevatte vereffening op basis van een gewogen gemiddelde zonder de optie **Fysieke waarde opnemen**
- Directe vereffening op basis van een gewogen gemiddelde met de optie **Fysieke waarde opnemen**
- Samengevatte vereffening op basis van een gewogen gemiddelde met de optie **Fysieke waarde opnemen**
- Gewogen gemiddelde met markering

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Directe vereffening op basis van een gewogen gemiddelde zonder Fysieke waarde opnemen

Met het directe-vereffeningsprincipe worden vereffeningen rechtstreeks tussen ontvangsten en uitgiften gemaakt zonder dat er extra voorraadtransacties worden gemaakt. Het principe voor directe vereffening wordt in de volgende situaties gebruikt:

- Eén ontvangst en een of meer uitgiften zijn in de periode geboekt.
- Er zijn alleen uitgiften in de periode geboekt en de voorraad bevat voorhanden artikelen uit een vorige afsluiting.

In dit voorbeeld is het selectievakje **Fysieke waarde opnemen** uitgeschakeld in de **artikelmodelgroep** voor het vrijgegeven product. De volgende afbeelding geeft deze transacties weer:

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 20,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 10,00 (lopend gemiddelde van financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 10,00 (lopend gemiddelde van financieel geboekte transacties).
- 4a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 10,00 per stuk (lopend gemiddelde van financieel geboekte transacties).
- 4b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 10,00 per stuk (lopend gemiddelde van financieel geboekte transacties).
- 5a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 10,00 per stuk (lopend gemiddelde van financieel geboekte transacties).
- 6\. Voorraadafsluiting is uitgevoerd. Op basis van de methode gewogen gemiddelde wordt de directe-vereffeningsmethode gebruikt, omdat slechts één ontvangst financieel wordt bijgewerkt in de periode. In dit voorbeeld wordt één vereffening gemaakt tussen 1b en 3b en een tweede tussen 1b en 4b. Er wordt geen correctie uitgevoerd, omdat het lopende gemiddelde gelijk is aan het gewogen gemiddelde.

In het volgende diagram wordt voor deze reeks transacties geïllustreerd wat het effect is van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van directe vereffening zonder de optie **Fysieke waarde opnemen**.

![WeightedAverage DS zonder de optie Fysieke waarde opnemen.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Uitleg bij diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Samengevatte vereffening op basis van een gewogen gemiddelde zonder de optie Fysieke waarde opnemen

Als er meerdere ontvangsten zijn in een periode, wordt voor gewogen gemiddelden gebruikgemaakt van het principe met samengevatte vereffening waarbij alle ontvangsten binnen een afsluitingsperiode worden samengevat in een transactie met de naam *Gewogen gemiddelde eindvoorraad*. Alle ontvangsten voor de periode worden vereffend met de uitgifte van deze nieuwe voorraadtransactie. Alle uitgiften voor de periode worden vereffend met de ontvangst van de nieuwe voorraadtransactie. Als er resterende voorhanden voorraad is na de voorraadafsluiting, wordt de waarde van de voorhanden voorraad opgenomen in de ontvangsttransactie van de gewogen gemiddelde eindvoorraad.

De volgende transacties worden in de volgende afbeelding geïllustreerd:

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
- 2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 22,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,00 (lopend gemiddelde van financieel geboekte transacties).
- 7\. Voorraadafsluiting is uitgevoerd.
- 7a. Financiële uitgifte 'gewogen gemiddelde voorraadafsluitingstransactie' wordt gemaakt om de vereffeningen van alle financiële ontvangsten in voorraad bij elkaar op te tellen.
  - Transactie 1b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 10,00.
  - Transactie 2b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 22,00.
  - Transactie 5b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 30,00.
  - Transactie 7a. wordt gemaakt voor een hoeveelheid van 3 met een vereffend bedrag van USD 62,00. Deze transactie compenseert het totaal van de drie ontvangsttransacties die financieel zijn bijgewerkt in de periode.
- 7b. Er wordt een gewogen gemiddelde voor een financiële ontvangst voorraadafsluitingstransactie het verschil met financieel geboekte uitgiften gemaakt.
  - Transactie 3b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 20,67. Deze transactie wordt gecorrigeerd met USD 4,67 in de oorspronkelijke waarde van USD 16,00 naar 20,67 te brengen. Dit is het gewogen gemiddelde van financieel geboekte transacties voor de periode.
  - Transactie 7b. wordt gemaakt voor een hoeveelheid van 1 met een vereffend bedrag van USD 20,67 als verrekening voor 3b. Deze transactie compenseert het totaal van één uitgiftetransacties die financieel wordt bijgewerkt in de periode.

In het volgende diagram wordt voor deze reeks transacties geïllustreerd wat het effect is van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van samengevatte vereffening zonder de optie **Fysieke waarde opnemen**.

![WeightedAverage SS zonder de optie Fysieke waarde opnemen.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Uitleg bij diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Directe vereffening op basis van een gewogen gemiddelde met de optie Fysieke waarde opnemen

De parameter **Fysieke waarde opnemen** werkt anders in combinatie met het voorraadmodel van het gewogen gemiddelde dan in eerdere versies van het product. Als u de optie **Fysieke waarde opnemen** inschakelt voor een artikel op het formulier **Artikelmodelgroep** selecteert, worden fysiek bijgewerkte ontvangsten gebruikt bij het berekenen van de geraamde kostprijs of het lopende gemiddelde. Uitgiften worden geboekt op basis van deze geraamde kostprijs tijdens de periode. Tijdens de voorraadafsluiting worden alleen financieel bijgewerkte ontvangsten meegenomen in de berekening van het gewogen gemiddelde.

De volgende transacties worden in de volgende afbeelding geïllustreerd:

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 10 met een waarde van USD 20,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 15,00 (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 15,00 (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 4a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 15,00 per stuk (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 4b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 15,00 per stuk (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 5a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 15,00 per stuk (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 6\. Voorraadafsluiting is uitgevoerd. Op basis van de methode gewogen gemiddelde wordt de directe-vereffeningsmethode gebruikt, omdat slechts één ontvangst financieel wordt bijgewerkt in de periode. In dit voorbeeld wordt één vereffening gemaakt tussen 1b en 3b en een tweede tussen 1b en 4b. Transactie 3b en 4b worden elk gecorrigeerd met USD -5,00 om de waarde op USD 10,00 brengen.

In het volgende diagram wordt voor deze reeks transacties geïllustreerd wat het effect is van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van directe vereffening met de optie **Fysieke waarde opnemen**.

![WeightedAverage DS met Fysieke waarde opnemen.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Uitleg bij diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Samengevatte vereffening op basis van een gewogen gemiddelde met de optie Fysieke waarde opnemen

De parameter **Fysieke waarde opnemen** werkt anders in combinatie met het gewogen gemiddelde dan in eerdere versies van het programma. Schakel het selectievakje **Fysieke waarde opnemen** in voor een artikel op de pagina **Artikelmodelgroepen**. Vervolgens worden fysiek bijgewerkte ontvangsten gebruikt bij het berekenen van de geraamde kostprijs of de lopende, gemiddelde kostprijs. Uitgiften worden geboekt op basis van deze geraamde kostprijs tijdens de periode. Tijdens de voorraadafsluiting worden alleen financieel bijgewerkte ontvangsten meegenomen in de berekening van het gewogen gemiddelde. We raden u aan een maandelijkse voorraadafsluiting uit te voeren wanneer u het gewogen gemiddelde voorraadmodel gebruikt. In dit voorbeeld van een samengevatte vereffening op basis van een gewogen gemiddelde is het voorraadmodel gemarkeerd voor het opnemen van de fysieke waarde.

De volgende transacties worden in de volgende afbeelding geïllustreerd:

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
- 2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 22,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,67 (lopend gemiddelde van fysiek en financieel geboekte transacties).
- 7\. Voorraadafsluiting is uitgevoerd.
- 7a. Financiële uitgifte 'gewogen gemiddelde voorraadafsluitingstransactie' wordt gemaakt om de vereffeningen van alle financiële ontvangsten in voorraad bij elkaar op te tellen.
  - Transactie 1b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 10,00.
  - Transactie 2b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 22,00.
  - Transactie 5b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 30,00.
  - Transactie 7a. wordt gemaakt voor een hoeveelheid van 3 met een vereffend bedrag van USD 62,00.  
- 7b. Er wordt een gewogen gemiddelde voor een financiële ontvangst voorraadafsluitingstransactie het verschil met de financieel afgesloten uitgiftetransacties gemaakt.
  - Transactie 3b wordt vereffend voor een hoeveelheid van 1 met een vereffend bedrag van USD 20,67. Deze transactie wordt gecorrigeerd met USD 4,67 in de oorspronkelijke waarde van USD 16,00 naar 20,67 te brengen. Dit is het gewogen gemiddelde van financieel geboekte transacties voor de periode.
  - Transactie 7b. wordt gemaakt voor een hoeveelheid van 1 met een vereffend bedrag van USD 20,67 als verrekening voor 3b.

In het volgende diagram wordt voor deze reeks transacties geïllustreerd wat het effect is van het kiezen van het gewogen gemiddelde voorraadmodel en het principe van samengevatte vereffening zonder de optie **Fysieke waarde opnemen**.

![WeightedAverage SS met de optie Fysieke waarde opnemen.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Uitleg bij diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-with-marking"></a>Gewogen gemiddelde met markering

Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markering gebruiken als u zeker wilt zijn van de juiste kosten van de voorraad wanneer de transactie wordt geboekt of wanneer de voorraad wordt afgesloten.

De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor dit artikel betalen om aan de vraag van de klant te voldoen. U moet er zeker van zijn dat de kosten van dit voorraadartikel worden weerspiegeld in de marge, of kosten van verkochte goederen, voor deze verkooporderfactuur.

Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van EUR 120,00. Dit verkooporderdocument is bijvoorbeeld aan de inkooporder gekoppeld voordat de pakbon of factuur wordt geboekt. De kosten van de verkochte goederen bedragen dan EUR 120,00 in plaats van de huidige gemiddelde kosten voor het artikel. Als de pakbon of de factuur van de verkooporder wordt geboekt voordat er wordt gemarkeerd, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs.

Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd.

Een ontvangsttransactie wordt aan een uitgiftetransactie gekoppeld. Vervolgens wordt de waarderingsmethode voor de artikelmodelgroep van het artikel genegeerd en worden deze transacties met elkaar vereffend.

U kunt een uitgiftetransactie aan een ontvangst koppelen voordat de transactie wordt geboekt. U kunt dit doen vanaf een verkooporderregel op de pagina **Details verkooporder**. De openstaande ontvangsttransacties kunnen worden bekeken op de pagina **Markering**.

U kunt een uitgiftetransactie aan een ontvangst koppelen nadat de transactie is geboekt. U kunt een uitgiftetransactie voor een openstaande ontvangsttransactie voor een geïnventariseerd artikel afstemmen of markeren vanuit een geboekt voorraadcorrectiejournaal.

De volgende transacties worden in de volgende afbeelding geïllustreerd:

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
- 2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 22,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3c. Financiële voorraaduitgifte voor 3b wordt gemarkeerd voor financiële voorraaduitgifte voor 2b.
- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,00 (lopend gemiddelde van financieel geboekte transacties).
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van het markeringsprincipe waarin de methode voor gewogen gemiddelde wordt gebruikt, worden de gemarkeerde transacties met elkaar vereffend. In dit voorbeeld wordt 3b vereffend met 2b en wordt een correctie voor USD 6,00 geboekt naar 3b om de waarde op USD 22,00 te brengen. In dit voorbeeld worden er geen extra vereffeningen gemaakt, omdat door de afsluiting alleen vereffeningen worden gemaakt voor financieel bijgewerkte transacties.

In het volgende diagram wordt voor deze reeks transacties het effect geïllustreerd van het kiezen van het gewogen gemiddelde voorraadmodel met markering.

![Gewogen gemiddelde met markering.](media/weighted-average-with-marking.png)

**Uitleg bij diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
