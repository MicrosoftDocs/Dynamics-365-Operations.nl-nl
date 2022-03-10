---
title: LIFO met fysieke waarde en markering
description: LIFO (Last in, First out) is een voorraadmodel waarin de laatste (nieuwste) ontvangsten het eerst worden uitgegeven. Uitgiften uit de voorraad worden vereffend met de laatste ontvangsten in de voorraad op basis van de datum van de voorraadtransactie.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd57d58aa91aa87b1c2feff52a568296fc18ed9b
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092159"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO met fysieke waarde en markering

[!include [banner](../includes/banner.md)]

Last in, first out (LIFO) is een voorraadbeheer- en waarderingsmethode waarbij de voorraad die het laatst is geproduceerd of het laatst is gekocht, het eerst wordt verkocht, gebruikt of afgevoerd. Tijdens het voorraadafsluitingsproces in Microsoft Dynamics 365 Supply Chain Management worden vereffeningen gemaakt waarbij de laatste ontvangst wordt vereffend met de eerste uitgifte, enzovoort. De vereffeningen en het afstemmingsprincipe zijn gebaseerd op de financiële datum van de voorraadtransacties. Een voorlopige beoordeling van de vereffeningen en correcties kan worden uitgevoerd door het voorraadherberekeningsproces uit te voeren.

U kunt het LIFO-principe overschrijven door voorraadtransacties te markeren zodat een specifieke artikelontvangst wordt vereffend met een specifieke uitgifte. Er is een periodieke voorraadafsluiting vereist wanneer u met het LIFO-voorraadmodel vereffeningen maakt en de waarde van uitgiften aanpast volgens het LIFO-principe. Totdat u het voorraadafsluitingsproces hebt uitgevoerd, worden uitgiftetransacties gewaardeerd op basis van het lopende gemiddelde wanneer de fysieke en financiële updates hebben plaatsgevonden. Tenzij u markering gebruikt, wordt het lopende gemiddelde berekend wanneer de fysieke of financiële update wordt uitgevoerd.

In de volgende voorbeelden wordt het effect geïllustreerd van het gebruik van LIFO in drie configuraties:

- LIFO zonder de optie **Fysieke waarde opnemen**
- LIFO met de optie **Fysieke waarde opnemen**
- LIFO met markering

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO zonder de optie Fysieke waarde opnemen

In dit voorbeeld is het selectievakje **Fysieke waarde opnemen** uitgeschakeld in de artikelmodelgroep voor het vrijgegeven product. De volgende afbeelding geeft deze transacties weer:

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
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van de LIFO-methode wordt de eerste financieel bijgewerkte uitgifte vereffend met de laatste financieel bijgewerkte ontvangst, enzovoort. In dit voorbeeld wordt één vereffening gemaakt tussen 5b en 3b. Er wordt een correctie van USD 14,00 naar 3b aangebracht en de resulterende definitieve kosten worden USD 30,00.

In de volgende afbeeldingen worden de effecten van het FIFO-voorraadmodel voor deze reeks transacties weergegeven wanneer de optie **Fysieke waarde opnemen** niet wordt gebruikt.

![LIFO zonder de optie Fysieke waarde opnemen.](./media/lifo-without-including-physical-value.png)

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

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO met de optie Fysieke waarde opnemen

Als het selectievakje **Fysieke waarde opnemen** is ingeschakeld voor een artikel op de pagina **Artikelmodelgroepen**, worden zowel fysieke als financiële ontvangsttransacties gebruikt bij het berekenen van de lopende gemiddelde kostprijs. Indien van toepassing wordt de fysiek bijgewerkte uitgiftetransactie ook gecorrigeerd. Als het selectievakje **Fysieke waarde opnemen** is uitgeschakeld, worden bij een voorraadafsluiting met het voorraadmodel LIFO alleen vereffeningen gemaakt voor transacties die financieel zijn bijgewerkt.

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
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van de LIFO-methode wordt de eerste financieel bijgewerkte uitgifte vereffend met de laatste financieel bijgewerkte ontvangst, enzovoort. In dit voorbeeld wordt één vereffening gemaakt tussen 3b en 5b. Er wordt een correctie van USD 14,00 naar 3b aangebracht en de resulterende definitieve kosten worden USD 30,00. Transactie 6a wordt bovendien gecorrigeerd naar de ontvangsttransactiekosten van 4a. Deze transacties worden niet vereffend, omdat de ontvangst fysiek maar niet financieel wordt bijgewerkt. In plaats daarvan wordt er alleen een correctie van USD 1,33 naar de fysieke uitgiftetransactie geboekt en worden de resulterende gecorrigeerde kosten USD 25,00.

In de volgende afbeelding worden de effecten van het LIFO-voorraadmodel voor deze reeks transacties weergegeven wanneer de optie **Fysieke waarde opnemen** wordt gebruikt.

![LIFO met de optie Fysieke waarde opnemen.](./media/lifo-with-included-physical-value.png)

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

## <a name="lifo-with-marking"></a>LIFO met markering

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
- 3c. Financiële voorraaduitgifte voor 3b wordt gemarkeerd voor financiële voorraaduitgifte voor 2b.
- 4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
- 5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
- 6a. Fysieke voorraaduitgifte voor een hoeveelheid van 1 met een kostprijs van USD 23,00 (lopend gemiddelde van financieel geboekte transacties)
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van het markeringsprincipe waarin de LIFO-methode wordt gebruikt, worden de gemarkeerde transacties met elkaar vereffend. In dit voorbeeld wordt 3b vereffend met 2b en wordt een correctie voor USD 6,00 geboekt naar 3b om de waarde op USD 22,00 te brengen. In dit voorbeeld worden er geen extra vereffeningen gemaakt, omdat door de afsluiting alleen vereffeningen worden gemaakt voor financieel bijgewerkte transacties.

De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel en fysiek bijgewerkte transacties, USD 27,50.

In het volgende afbeelding worden de effecten van het LIFO-voorraadmodel op deze reeks transacties weergegeven wanneer markering tussen uitgiften en ontvangsten wordt gebruikt.

![LIFO met markering.](./media/lifo-with-marking.png)

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
- Vereffeningen en markeringen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
