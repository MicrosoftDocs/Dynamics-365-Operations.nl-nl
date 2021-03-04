---
title: Datum gewogen gemiddelde
description: Datum gewogen gemiddelde is een voorraadmodel dat is gebaseerd op het principe van het gewogen gemiddelde, waarbij uitgiften worden berekend tegen de gemiddelde waarde van de artikelen die worden ontvangen in voorraad voor elke afzonderlijke dag in de afsluitingsperiode van de voorraad.
author: AndersGirke
manager: tfehr
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d36f60a13fbee91100e406150e7f5ca890320436
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425258"
---
# <a name="weighted-average-date"></a>Datum gewogen gemiddelde

[!include [banner](../includes/banner.md)]

Datum gewogen gemiddelde is een voorraadmodel dat is gebaseerd op het beginsel van gewogen gemiddelden. Voor het principe van gewogen gemiddelden, worden uitgiften uit de voorraad gewaardeerd tegen de gemiddelde waarde van de artikelen die zijn ontvangen in de voorraad voor elke dag in de periode van de eindvoorraad. 

Wanneer u een voorraad afsluit met een datum gewogen gemiddelde, worden alle dagelijkse ontvangsten vereffend met een virtuele uitgifte. Deze virtuele uitgifte omvat de totale hoeveelheid die is ontvangen en de waarde voor die dag. De virtuele uitgifte heeft een bijbehorende virtuele ontvangst waarmee de uitgiften worden vereffend. Daarom hebben alle uitgiften dezelfde gemiddelde kosten. De virtuele uitgifte en virtuele ontvangst kunnen worden gezien als virtuele overboeking, die ook wel een *overboeking van gewogen gemiddelde eindvoorraad* wordt genoemd. 

Als er slechts één ontvangst heeft plaatsgevonden op of vóór de datum, hoeft u het gemiddelde niet te waarderen. Aangezien alle uitgiften met deze ontvangst worden vereffend, wordt er geen virtuele overboeking gemaakt. Tevens geldt dat, als er alleen uitgiften plaatsvinden op de desbetreffende datum, er geen ontvangsten beschikbaar zijn om het gemiddelde te berekenen en wordt er geen virtuele overboeking gemaakt. Wanneer u een datum gewogen gemiddelde gebruikt, kunt u voorraadtransacties markeren zodat een bepaalde artikelontvangst wordt vereffend met een bepaalde uitgifte. In daqt geval maakt u geen gebruik van de regel voor datum gewogen gemiddelde. U wordt aangeraden maandelijks een voorraadafsluiting uit te voeren wanneer u het voorraadmodel Datum gewogen gemiddelde gebruikt. 

De kostprijsberekeningsmethode datum gewogen gemiddelde wordt berekend met behulp van de volgende formule: 

Gewogen gemiddelde = (\[KW1 × P1\] + \[KW2 × P2\] + \[KW *n* × P *n*\]) ÷ (KW1 + KW2 + KW *n*) 

Tijdens de voorraadafsluiting wordt de berekening elke dag via de afsluitperiode uitgevoerd, zoals in de volgende afbeelding wordt weergegeven. 

![Dagelijks rekenmodel datum gewogen gemiddelde](./media/weightedaveragedatedailycalculationmodel.gif) 

Voorraadtransacties die de voorraad verlaten, zoals verkooporders, voorraadjournalen en productieorders, vinden plaats tegen een geraamde kostprijs op de boekingsdatum. De geraamde kostprijs wordt ook wel de lopende gemiddelde kostprijs genoemd. Op de datum van de voorraadafsluiting worden de voorraadtransacties voor vorige perioden, vorige dagen en de huidige dag geanalyseerd. Deze analyse wordt gebruikt om te bepalen welke van de volgende afsluitingsprincipes er moeten worden gebruikt:

-   Directe vereffening
-   Samengevatte vereffening

Vereffeningen zijn voorraadafsluitingsboekingen die de uitgiften vanaf de sluitingsdatum bijwerken met het juiste gewogen gemiddelde. 

**Notitie:** Voor meer informatie over voorraadafsluitingen raadpleegt u het artikel over voorraadafsluiting. De volgende voorbeelden laten het effect zien van het gebruik van gewogen gemiddelden bij vijf configuraties:

-   Datum gewogen gemiddelde directe vereffening zonder dat de optie **Fysieke waarde opnemen** wordt gebruikt
-   Datum gewogen gemiddelde samengevatte vereffening zonder dat de optie **Fysieke waarde opnemen** wordt gebruikt
-   Datum gewogen gemiddelde directe vereffening waarbij de optie **Fysieke waarde opnemen** wel wordt gebruikt
-   Datum gewogen gemiddelde samengevatte vereffening waarbij de optie **Fysieke waarde opnemen** wel wordt gebruikt
-   Datum gewogen gemiddelde met gebruik van markering

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Datum gewogen gemiddelde directe vereffening zonder dat de optie Fysieke waarde opnemen wordt gebruikt
In de huidige versie wordt hetzelfde directe-vereffeningsprincipe gebruikt dat werd toegepast in eerdere versies voor gewogen gemiddelden. Er wordt direct vereffend tussen ontvangsten en uitgiften. Het principe voor directe vereffening wordt in bepaalde situaties gebruikt:

-   Eén ontvangst en een of meer uitgiften zijn in de periode geboekt.
-   Er zijn alleen uitgiften in de periode geboekt en de voorraad bevat voorhanden artikelen uit een vorige afsluiting.

In het volgende scenario zijn een financieel bijgewerkte ontvangst en uitgifte geboekt. Tijdens de voorraadafsluiting wordt de ontvangst direct met de uitgifte vereffend en hoeft de kostprijs bij de uitgifte niet te worden gecorrigeerd. 

De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst wordt bijgewerkt voor een hoeveelheid van 5 tegen een kostprijs van EUR 10,00 per stuk.
-   1b. Financiële voorraadontvangst wordt bijgewerkt voor een hoeveelheid van 5 tegen een kostprijs van EUR 10,00 per stuk.
-   2a. Fysieke voorraaduitgifte wordt bijgewerkt voor een hoeveelheid van 2 tegen een prijs van EUR 10,00 per stuk.
-   2b. Financiële voorraaduitgifte wordt bijgewerkt voor een hoeveelheid van 2 tegen een prijs van EUR 10,00 per stuk.
-   3. Voorraadafsluiting wordt uitgevoerd met behulp van de directe-vereffeningsmethode om de financiële ontvangst van de voorraad te vereffenen met de financiële uitgifte van de voorraad.

![Datum gewogen gemiddelde directe vereffening zonder de optie Fysieke waarde opnemen](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Sleutel voor de afbeelding:**

-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl ziet u de waarde van de voorraadtransactie met de notatie *Hoeveelheid*@*Eenheidsprijs*.
-   Als een voorraadtransactiewaarde tussen haakjes staat, wordt de voorraadtransactie fysiek naar de voorraad geboekt.
-   Als een voorraadtransactiewaarde niet tussen haakjes staat, wordt de voorraadtransactie financieel naar de voorraad geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De ID's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
-   Vereffeningen door voorraadafsluitingen worden weergegeven met rode stippelpijlen die diagonaal van een ontvangst naar een uitgifte lopen.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Datum gewogen gemiddelde samengevatte vereffening zonder dat de optie Fysieke waarde opnemen wordt gebruikt
Gewogen gemiddelde is gebaseerd op het principe dat alle ontvangsten in een afsluitingsperiode worden samengevat in een nieuwe voorraadoverboekingstransactie. Deze transactie wordt *gewogen gemiddelde eindvoorraad* genoemd. Alle ontvangsten voor de dag worden vereffend met de uitgifte van deze nieuwe voorraadoverboekingstransactie. Alle uitgiften voor de dag worden vereffend met de ontvangst van de nieuwe voorraadoverboekingstransactie. Als de voorhanden voorraad na de voorraadafsluiting positief is, worden de voorhanden voorraad en de waarde van de voorraad samengevat in de nieuwe voorraadoverboekingstransactieontvangst. Is de voorhanden voorraad na de voorraadafsluiting negatief, dan zijn de voorhanden voorraad en de waarde van de voorraad de som van de afzonderlijke uitgiften die nog niet volledig zijn vereffend. 

In het volgende scenario zijn diverse financieel bijgewerkte ontvangsten en uitgiften tijdens de periode geboekt. Tijdens de voorraadafsluiting wordt elke dag bepaald hoe elke dag door de afsluitingen moeten worden afgehandeld. 

De volgende afbeelding geeft deze transacties weer: 

**Dag 1:**

-   1a. Fysieke voorraadontvangst wordt bijgewerkt voor een hoeveelheid van 3 tegen een prijs van EUR 15,00 per stuk.
-   1b. Financiële voorraadontvangst wordt bijgewerkt voor een hoeveelheid van 3 tegen een prijs van EUR 15,00 per stuk.
-   2a. Fysieke voorraadontvangst voor een hoeveelheid 1 tegen een lopende gemiddelde kostprijs van USD 15,00.
-   2b. Financiële voorraadontvangst voor een hoeveelheid 1 tegen een lopende gemiddelde kostprijs van USD 15,00.

Voor dag 1 wordt de aanpak met de directe vereffening gebruikt. 

**Dag 2:**

-   3a. Fysieke voorraadontvangst voor een hoeveelheid van 1 tegen een lopende gemiddelde kostprijs van EUR 15,00
-   3b. financiële voorraaduitgifte voor een hoeveelheid van 1 tegen een gemiddelde kostprijs van EUR 15,00

Voor dag 2 wordt de aanpak met de directe vereffening gebruikt. 

**Dag 3:**

-   4a. Fysieke voorraadontvangst voor een hoeveelheid van 1 tegen een lopende gemiddelde kostprijs van EUR 15,00
-   4b. financiële voorraaduitgifte voor een hoeveelheid van 1 tegen een gemiddelde kostprijs van EUR 15,00
-   5a. Fysieke voorraadontvangst voor een hoeveelheid van 1 tegen een prijs van EUR 17,00 per stuk
-   5b. Financiële voorraadontvangst voor een hoeveelheid van 1 tegen een prijs van EUR 17,00 per stuk

Voorraadafsluiting is uitgevoerd. De directe vereffening moet worden gebruikt omdat er meerdere ontvangsten zijn die meerdere dagen omvatten.

-   7a. Er wordt een gewogen gemiddelde voor een financiële uitgifte voorraadafsluitingstransactie gemaakt voor een hoeveelheid van 2 tegen een prijs van EUR 32,00 om de vereffeningen van alle financiële voorraadontvangsten die niet zijn afgesloten, tot aan de huidige datum samen te vatten.
-   7b. Er wordt een gewogen gemiddelde voor een financiële ontvangst voorraadafsluitingstransactie als tegenrekening voor 7a gemaakt.

De samengevatte voorraadoverboekingstransactie worden gegenereerd en geboekt. Ook worden alle ontvangsten voor de dag en voorhanden voorraad voor vorige dagen vereffend met de samengevatte voorraadoverboekingsuitgiftetransactie. Alle uitgiften voor de dag worden vereffend met de samengevatte voorraadoverboekingsontvangsttransactie. De gewogen gemiddelde kostprijs wordt berekend als EUR 16,00. De uitgifte wordt gecorrigeerd met EUR 1,00 en wordt zo gelijkgetrokken met de gewogen gemiddelde kostprijs. De nieuwe, lopende gemiddelde kostprijs wordt USD 16,00. 

In de volgende illustratie wordt deze reeks transacties getoond en wordt aangegeven wat het effect is van het gebruik van het voorraadmodel van het gewogen gemiddelde en het samengevatte-vereffeningsprincipe zonder dat de optie **Fysieke waarde opnemen** wordt gebruikt. 

![Datum gewogen gemiddelde samengevatte vereffening zonder de optie Fysieke waarde opnemen](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Sleutel voor de afbeelding**

-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl ziet u de waarde van de voorraadtransactie met de notatie *Hoeveelheid*@*Eenheidsprijs*.
-   Als een voorraadtransactiewaarde tussen haakjes staat, wordt de voorraadtransactie fysiek naar de voorraad geboekt.
-   Als een voorraadtransactiewaarde niet tussen haakjes staat, wordt de voorraadtransactie financieel naar de voorraad geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De ID's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
-   Vereffeningen door voorraadafsluitingen worden weergegeven met rode stippelpijlen die diagonaal van een ontvangst naar een uitgifte lopen.
-   Rode diagonale pijlen geven de ontvangsttransacties aan die zijn vereffend met de uitgiftetransactie die door het systeem is gemaakt.
-   De groene diagonale pijlen geven de tegengerekende, door het systeem gegeneerde ontvangsttransactie aan waarnaar de oorspronkelijke geboekte uitgiftetransactie wordt vereffend.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Datum gewogen gemiddelde directe vereffening waarbij de optie Fysieke waarde opnemen wel wordt gebruikt
In de huidge versie wordt hetzelfde principe voor directe vereffening voor de datum gewogen gemiddelde gebruikt als in eerdere versies. Er wordt direct vereffend tussen ontvangsten en uitgiften. Het principe voor directe vereffening wordt in bepaalde situaties gebruikt:

-   Eén ontvangst en een of meer uitgiften zijn in de periode geboekt.
-   Er zijn alleen uitgiften in de periode geboekt en de voorraad bevat voorhanden voorraad uit een vorige afsluiting.

Als u het selectievakje **Fysieke waarde opnemen** inschakelt voor een artikel op de pagina **Artikelmodelgroep** selecteert, worden fysiek bijgewerkte ontvangsten gebruikt bij het berekenen van de geraamde kostprijs of het lopende gemiddelde. Uitgiften worden geboekt op basis van deze geraamde kostprijs tijdens de periode. Tijdens de voorraadafsluiting worden alleen de financieel bijgewerkte ontvangsten meegenomen in de berekening voor het gewogen gemiddelde.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Datum gewogen gemiddelde samengevatte vereffening waarbij de optie Fysieke waarde opnemen wel wordt gebruikt
Als u het selectievakje **Fysieke waarde opnemen** inschakelt voor een artikel op de pagina **Artikelmodelgroep** selecteert, worden fysiek bijgewerkte ontvangsten gebruikt bij het berekenen van de geraamde kostprijs of het lopende gemiddelde. Uitgiften worden geboekt op basis van deze geraamde kostprijs tijdens de periode. Tijdens de voorraadafsluiting worden alleen de financieel bijgewerkte ontvangsten meegenomen in de berekening voor het gewogen gemiddelde. Vereffening op basis van een gewogen gemiddelde gebaseerd op het principe dat alle ontvangsten binnen een afsluitingsperiode worden samengevat in een nieuwe voorraadoverboekingstransactie, die *gewogen gemiddelde eindvoorraad* wordt genoemd. Alle ontvangsten voor de dag worden vereffend met de uitgifte van deze nieuwe voorraadoverboekingstransactie. Alle uitgiften voor de dag worden vereffend met de ontvangst van de nieuwe voorraadoverboekingstransactie. Als de voorhanden voorraad na de voorraadafsluiting positief is, worden deze voorhanden voorraad en de waarde van de voorraad samengevat in de nieuwe voorraadoverboekingstransactie (ontvangst). Is de voorhanden voorraad na de voorraadafsluiting negatief, dan zijn de voorhanden voorraad en de waarde van de voorraad de som van de afzonderlijke uitgiften die nog niet volledig zijn vereffend.

## <a name="weighted-average-date-when-marking-is-used"></a>Datum gewogen gemiddelde met gebruik van markering
Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markeren als u de exacte kosten van de voorraad wilt weten wanneer de transactie wordt geboekt of wanneer de voorraad wordt afgesloten. 

De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor dit artikel betalen om aan de vraag van de klant te voldoen. U moet er zeker van zijn dat de kosten van dit voorraadartikel worden weerspiegeld in de marge, of kosten van verkochte goederen, voor deze verkooporderfactuur. Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van USD 120,00. Het verkooporderdocument is aan de inkooporder gekoppeld voordat de pakbon of factuur wordt geboekt. De kosten van de verkochte goederen bedragen dan EUR 120,00 in plaats van de huidige gemiddelde kosten voor het artikel. Als de pakbon of de factuur van de verkooporder wordt geboekt voordat er wordt gemarkeerd, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs. Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd. Wanneer een ontvangsttransactie is gemarkeerd met een uitgiftetransactie, wordt de waarderingsmethode die in de artikelmodelgroep van het artikel is gedefinieerd, genegeerd. In plaats daarvan worden deze transacties met elkaar vereffend. 

U kunt een uitgiftetransactie aan een ontvangst koppelen voordat de transactie wordt geboekt. U kunt dit doen vanaf een verkooporderregel op de pagina **Details verkooporder**. U kunt de openstaande ontvangsttransacties bekijken op de pagina **Markering**. U kunt een uitgiftetransactie aan een ontvangst koppelen nadat de transactie is geboekt. U kunt een uitgiftetransactie voor een openstaande ontvangsttransactie voor een geïnventariseerd artikel afstemmen of markeren vanuit een geboekt voorraadcorrectiejournaal. De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst voor een hoeveelheid 1 tegen een kostprijs van USD 10,00 per stuk.
-   1a. Financiële voorraadontvangst voor een hoeveelheid 1 tegen een kostprijs van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor een hoeveelheid 1 tegen een kostprijs van USD 20,00 per stuk.
-   2b. Financiële voorraadontvangst voor een hoeveelheid 1 tegen een prijs van USD 20,00 per stuk.
-   3a. Fysieke voorraadontvangst voor een hoeveelheid 1 tegen een kostprijs van USD 25,00 per stuk.
-   4a. Fysieke voorraadontvangst voor een hoeveelheid 1 tegen een kostprijs van USD 30,00 per stuk.
-   4b. Financiële voorraadontvangst voor een hoeveelheid 1 tegen een kostprijs van USD 30,00 per stuk.
-   5a. Fysieke voorraaduitgifte voor een hoeveelheid 1 tegen een kostprijs van USD 21,25 (lopend gemiddelde van financieel en fysiek bijgewerkte transacties).
-   5b. De financiële voorraaduitgifte voor een hoeveelheid 1 wordt gemarkeerd voor de voorraadontvangst 2b voordat de transactie wordt geboekt. De transactie wordt geboekt tegen een kostprijs van USD 20,00.
-   6a. Fysieke voorraadontvangst voor een hoeveelheid 1 tegen een kostprijs van USD 21,25.
-   7. Voorraadafsluiting is uitgevoerd. Omdat de financieel bijgewerkte transactie is gemarkeerd voor een bestaande ontvangst, worden deze transacties met elkaar vereffend en wordt er niet gecorrigeerd.

De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel en fysiek bijgewerkte transacties met USD 27,50. In de volgende illustratie wordt voor deze reeks transacties de effecten weergegeven van het gebruik van het voorraadmodel voor datum gewogen gemiddelde en markering.

![Datum gewogen gemiddelde met markering](./media/weightedaveragedatewithmarking.gif) 

**Sleutel voor de afbeelding:**

-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl ziet u de waarde van de voorraadtransactie met de notatie *Hoeveelheid*@*Eenheidsprijs*.
-   Als een voorraadtransactiewaarde tussen haakjes staat, wordt de voorraadtransactie fysiek naar de voorraad geboekt.
-   Als een voorraadtransactiewaarde niet tussen haakjes staat, wordt de voorraadtransactie financieel naar de voorraad geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De ID's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
-   Vereffeningen door voorraadafsluitingen worden weergegeven met rode stippelpijlen die diagonaal van een ontvangst naar een uitgifte lopen.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]