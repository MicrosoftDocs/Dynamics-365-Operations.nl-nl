---
title: LIFO-datum met fysieke waarde en markering
description: LIFO-datum (Last In, First Out) is een voorraadmodel dat gebaseerd is op het LIFO-principe. Uitgiften uit de voorraad worden vereffend met de laatste ontvangsten in de voorraad op basis van de datum van de voorraadtransactie. Als er op de LIFO-datum geen artikel vóór de uitgifte wordt ontvangen, wordt de uitgifte vereffend met de ontvangsten die na de datum van de artikeluitgifte plaatsvinden. Meerdere uitgiften op dezelfde datum kunnen in de volgende 'laatste uitgifte - laatste ontvangst' worden vereffend.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6f5f447724ace473bece3007a96c4b56e90a908
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330271"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-datum met fysieke waarde en markering

[!include [banner](../includes/banner.md)]

Last in, first out (LIFO-datum) is een voorraadbeheer- en waarderingsmethode waarbij de voorraad die het laatst is geproduceerd of het laatst is gekocht, het eerst wordt verkocht, gebruikt of afgevoerd. Tijdens het voorraadafsluitingsproces in Microsoft Dynamics 365 Supply Chain Management worden vereffeningen gemaakt waarbij de laatste ontvangst wordt vereffend met de eerste uitgifte voor elke gegeven datum, te beginnen met de oudste datum, enzovoort. Als u het voorraadmodel LIFO-datum (Last In, First Out) gebruikt en er vóór de uitgifte geen artikel wordt ontvangen, wordt de uitgifte vereffend met de ontvangsten die na de datum van de artikeluitgifte plaatsvinden. De vereffeningen en het afstemmingsprincipe zijn gebaseerd op de financiële datum van de voorraadtransacties. Meerdere uitgiften op dezelfde datum worden in de volgoede 'laatste uitgifte - laatste ontvangst' vereffend. Een voorlopige beoordeling van de vereffeningen en correcties kan worden uitgevoerd door het voorraadherberekeningsproces uit te voeren.

U kunt het LIFO-datumprincipe overschrijven door voorraadtransacties te markeren zodat een specifieke artikelontvangst wordt vereffend met een specifieke uitgifte. Er is een periodieke voorraadafsluiting vereist wanneer u met het LIFO-datumvoorraadmodel vereffeningen maakt en de waarde van uitgiften aanpast volgens het LIFO-principe. Totdat u het voorraadafsluitingsproces hebt uitgevoerd, worden uitgiftetransacties gewaardeerd op basis van het lopende gemiddelde wanneer de fysieke en financiële updates hebben plaatsgevonden. Tenzij u markering gebruikt, wordt het lopende gemiddelde berekend wanneer de fysieke of financiële update wordt uitgevoerd.

Het wordt aangeraden de voorraad periodiek af te sluiten wanneer u het LIFO-datumvoorraadmodel gebruikt.

In de volgende voorbeelden wordt het effect geïllustreerd van het gebruik van LIFO-datum in drie configuraties:

- LIFO-datum zonder de optie **Fysieke waarde opnemen**
- LIFO-datum met de optie **Fysieke waarde opnemen**
- LIFO-datum met markering

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-datum zonder de optie Fysieke waarde opnemen

In dit voorbeeld is de artikelmodelgroep niet gemarkeerd voor het opnemen van de fysieke waarde. De volgende afbeelding geeft deze transacties weer:

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
- 2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 22,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,00 (lopend gemiddelde van financieel geboekte transacties)
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van de LIFO-datummethode wordt de eerste financieel bijgewerkte uitgifte vereffend met de laatste financieel bijgewerkte ontvangst, te beginnen op de eerste datum, enzovoort. In dit voorbeeld wordt één vereffening gemaakt tussen 3b en 2b. Er wordt een correctie van USD 6,00 naar 3b aangebracht en de resulterende definitieve kosten worden USD 22,00.

In de volgende afbeelding worden de effecten van het LIFO-datumvoorraadmodel weergegeven wanneer de optie **Fysieke waarde opnemen** niet wordt gebruikt.

![LIFO-datum zonder de optie Fysieke waarde opnemen.](media/lifo-date-without-include-physical-value.png)

**Uitleg bij het diagram**

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-datum met de optie Fysieke waarde opnemen

Als het selectievakje **Fysieke waarde opnemen** is ingeschakeld voor een artikel op de pagina **Artikelmodelgroepen**, worden zowel fysieke als financiële ontvangsttransacties gebruikt bij het berekenen van de lopende gemiddelde kostprijs. Indien van toepassing wordt de fysiek bijgewerkte uitgiftetransactie ook gecorrigeerd. Als het selectievakje **Fysieke waarde opnemen** is uitgeschakeld, worden bij een voorraadafsluiting met het LIFO-datumvoorraadmodel alleen vereffeningen gemaakt voor transacties die financieel zijn bijgewerkt.

In dit voorbeeld is de artikelmodelgroep niet gemarkeerd voor het opnemen van de fysieke waarde. 

De volgende afbeelding geeft deze transacties weer:

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
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van de LIFO-datummethode wordt de eerste financieel bijgewerkte uitgifte vereffend met de laatste financieel bijgewerkte ontvangst, voor elke datum te beginnen op de eerste datum, enzovoort. In dit voorbeeld wordt één vereffening gemaakt tussen 2b en 3b. Er wordt een correctie van USD 6,00 naar 3b aangebracht en de resulterende definitieve kosten worden USD 22,00. Transactie 6a wordt bovendien gecorrigeerd naar de ontvangsttransactiekosten van 5b. Deze transacties worden niet vereffend, omdat de ontvangst fysiek maar niet financieel wordt bijgewerkt. In plaats daarvan wordt er alleen een correctie van USD 6,33 naar de fysieke uitgiftetransactie geboekt en worden de resulterende gecorrigeerde kosten USD 30,00.

In de volgende afbeelding worden de effecten van het voorraadmodel LIFO-datum weergegeven wanneer de optie **Fysieke waarde opnemen** wel wordt gebruikt.

![LIFO-datum met de optie Fysieke waarde opnemen.](media/lifo-date-with-include-physical-value.png)

**Uitleg bij het diagram**

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

## <a name="lifo-date-with-marking"></a>LIFO-datum met markering

Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markering gebruiken als u zeker wilt zijn van de juiste kosten van de voorraad wanneer de transactie wordt geboekt of de voorraad wordt afgesloten. De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor het artikel betalen om in de vraag van de klant te voorzien.

U moet ervoor zorgen dat de kosten van het voorraadartikel worden weergegeven in de marge, of kosten van verkochte goederen, voor de verkooporderfactuur. Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van EUR 120,00. Als dit verkooporderdocument aan de inkooporder wordt gekoppeld voordat de pakbon of factuur wordt geboekt, bedragen de kosten van de verkochte goederen USD 120,00, niet de huidige gemiddelde kosten voor het artikel. Als de pakbon of factuur voor de verkooporder wordt geboekt voordat er wordt gemarkeerd, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs.

Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd.

U kunt een uitgiftetransactie aan een ontvangst koppelen voordat de transactie wordt geboekt. U kunt deze markering uitvoeren vanaf een verkooporderregel op de pagina **Details verkooporder** door **Voorraad \> Markering** te selecteren op het sneltabblad **Verkooporderregels**. U kunt de openstaande ontvangsttransacties bekijken op de pagina **Markering**.

U kunt ook een uitgiftetransactie aan een ontvangst koppelen nadat de transactie is geboekt. U kunt een uitgiftetransactie voor een openstaande ontvangsttransactie voor een geïnventariseerd artikel afstemmen of markeren vanuit een geboekt voorraadcorrectiejournaal.

De volgende afbeelding geeft deze transacties weer:

- 1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
- 2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
- 2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 22,00 per stuk.
- 3a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3b. Financiële voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 16,00 (lopend gemiddelde van financieel geboekte transacties).
- 3c. Financiële voorraaduitgifte voor 3b wordt gemarkeerd voor financiële voorraaduitgifte voor 1b.
- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,00 (lopend gemiddelde van financieel geboekte transacties)
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van het markeringsprincipe waarin de LIFO-datummethode wordt gebruikt, worden de gemarkeerde transacties met elkaar vereffend. In dit voorbeeld wordt 3b vereffend met 1b en wordt een correctie voor USD -6,00 geboekt naar 3b om de waarde op USD 10,00 te brengen. In dit voorbeeld worden er geen extra vereffeningen gemaakt, omdat door de afsluiting alleen vereffeningen worden gemaakt voor financieel bijgewerkte transacties.

De volgende afbeelding illustreert de gevolgen van het LIFO-datumvoorraadmodel bij gebruik van markering tussen uitgiften en ontvangsten. 

![LIFO-datum met markering.](media/lifo-date-with-marking.png)

**Uitleg bij het diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de as.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de as.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen en markeringen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
