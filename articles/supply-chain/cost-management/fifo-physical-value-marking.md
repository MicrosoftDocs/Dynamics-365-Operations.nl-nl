---
title: FIFO met fysieke waarde en markering
description: FIFO (First in, First out) is een voorraadmodel waarin de eerste ontvangsten het eerst worden uitgegeven. Financieel bijgewerkte uitgiften uit de voorraad worden vereffend met de eerste financieel bijgewerkte ontvangsten in de voorraad op basis van de financiële datum van de voorraadtransactie.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092135"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO met fysieke waarde en markering

[!include [banner](../includes/banner.md)]


First in, first out (FIFO) is een voorraadbeheer- en waarderingsmethode waarbij de voorraad die het eerst wordt geproduceerd of het eerst wordt gekocht, wordt verkocht, gebruikt of afgevoerd. Tijdens het voorraadafsluitingsproces in Microsoft Dynamics 365 Supply Chain Management worden vereffeningen gemaakt waarbij de eerste ontvangst wordt vereffend met de eerste uitgifte, enzovoort.

De vereffeningen en het afstemmingsprincipe zijn gebaseerd op de financiële datum van de voorraadtransacties. Een voorlopige beoordeling van de vereffeningen en correcties kan worden uitgevoerd door het voorraadherberekeningsproces uit te voeren.

U kunt het FIFO-principe overschrijven door voorraadtransacties te markeren zodat een specifieke artikelontvangst wordt vereffend met een specifieke uitgifte. Er is een periodieke voorraadafsluiting vereist wanneer u met het FIFO-voorraadmodel vereffeningen maakt en de waarde van uitgiften aanpast volgens het FIFO-principe. Totdat u het voorraadafsluitingsproces hebt uitgevoerd, worden uitgiftetransacties gewaardeerd op basis van het lopende gemiddelde wanneer de fysieke en financiële updates hebben plaatsgevonden. Tenzij u markering gebruikt, wordt het lopende gemiddelde berekend wanneer de fysieke of financiële update wordt uitgevoerd. In de volgende voorbeelden wordt het effect geïllustreerd van het gebruik van FIFO in drie configuraties:

- FIFO zonder de optie **Fysieke waarde opnemen**
- FIFO met de optie **Fysieke waarde opnemen**
- FIFO met markering

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO zonder de optie Fysieke waarde opnemen

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
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van de FIFO-methode wordt de eerste financieel bijgewerkte uitgifte vereffend met de eerste financieel bijgewerkte ontvangst, enzovoort. In dit voorbeeld wordt één vereffening gemaakt tussen 1b en 3b. Er wordt een correctie van USD -6,00 naar 3b aangebracht en de resulterende definitieve kosten worden USD 10,00.

De nieuwe lopende gemiddelde kostprijs staat voor het gemiddelde van de bijgewerkte financiële transacties. In de volgende afbeeldingen worden de effecten van het FIFO-voorraadmodel voor deze reeks transacties weergegeven wanneer de optie **Fysieke waarde opnemen** niet wordt gebruikt.

![FIFO zonder de optie Fysieke waarde opnemen.](./media/fifo-without-include-physical-value.png)

**Uitleg bij het diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de tijdlijn.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO met de optie Fysieke waarde opnemen

Als het selectievakje **Fysieke waarde opnemen** is ingeschakeld voor een artikel op de pagina **Artikelmodelgroep**, worden zowel fysieke als financiële ontvangsttransacties gebruikt bij het berekenen van de lopende gemiddelde kostprijs. Indien van toepassing wordt de fysiek bijgewerkte uitgiftetransactie ook gecorrigeerd. Bij voorraadafsluiting waarin het FIFO-voorraadmodel wordt gebruikt, worden alleen vereffeningen uitgevoerd voor transacties die financieel zijn bijgewerkt. De volgende afbeelding geeft deze transacties weer:

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
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van de FIFO-methode wordt de eerste financieel bijgewerkte uitgifte vereffend met de eerste financieel bijgewerkte ontvangst, enzovoort. In dit voorbeeld wordt één vereffening gemaakt tussen 1b en 3b. Er wordt een correctie van USD -6,00 naar 3b aangebracht en de resulterende definitieve kosten worden USD 10,00. Transactie 6a wordt bovendien gecorrigeerd naar de ontvangsttransactiekosten van 2b. Deze transacties worden niet vereffend, omdat de ontvangst fysiek maar niet financieel wordt bijgewerkt. In plaats daarvan wordt er alleen een correctie van USD -1,67 naar de fysieke uitgiftetransactie geboekt en worden de resulterende gecorrigeerde kosten USD 22,00.

![FIFO met de optie Fysieke waarde opnemen.](./media/fifo-with-include-physical-value.png)

Het resultaat van het uitvoeren van het voorraadafsluitingsproces is hetzelfde, ongeacht of u de optie **Fysieke waarde opnemen** selecteert op de pagina **Artikelmodelgroep**. De optie **Fysieke waarde opnemen** heeft alleen invloed op het lopende gemiddelde.

**Uitleg bij het diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de tijdlijn.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="fifo-with-marking"></a>FIFO met markering

Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markering gebruiken als u zeker wilt zijn van de juiste kosten van de voorraad wanneer de transactie wordt geboekt of de voorraad wordt afgesloten.

De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor dit artikel betalen om in de vraag van de klant te voorzien. U moet ervoor zorgen dat de kosten van het voorraadartikel worden weergegeven in de marge, of kosten van verkochte goederen, voor de verkooporderfactuur. Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van EUR 120,00. Als het verkooporderdocument voor de inkooporder wordt gemarkeerd voordat de pakbon of factuur wordt geboekt, bedragen de kosten van de verkochte goederen USD 120,00 en niet de huidige lopende gemiddelde kosten voor het artikel. Als de pakbon of factuur voor de verkooporder wordt geboekt voordat er wordt gemarkeerd, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs. Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd.

Wanneer een ontvangsttransactie wordt gemarkeerd voor een uitgiftetransactie, wordt de waarderingsmethode die in de artikelmodelgroep is gedefinieerd, genegeerd en worden de transacties met elkaar vereffend. U kunt een transactie handmatig markeren voor een verkooporderregel op de pagina **Details verkooporder** door **Voorraad \> Markering** te selecteren op het sneltabblad **Verkooporderregels**. U kunt de openstaande ontvangsttransacties bekijken op de pagina **Markering**. U kunt een uitgiftetransactie voor een openstaande ontvangsttransactie voor een geïnventariseerd artikel afstemmen of markeren vanuit een geboekt voorraadcorrectiejournaal. De volgende afbeelding geeft deze transacties weer:

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
- 7\. Voorraadafsluiting is uitgevoerd. Op basis van het markeringsprincipe waarin de FIFO-methode wordt gebruikt, worden de gemarkeerde transacties met elkaar vereffend. In dit voorbeeld wordt 3b vereffend met 2b en wordt een correctie voor USD 6,00 geboekt naar 3b om de waarde op USD 22,00 te brengen. In dit voorbeeld worden er geen extra vereffeningen gemaakt, omdat door de afsluiting alleen vereffeningen worden gemaakt voor financieel bijgewerkte transacties.

In het volgende afbeelding worden de effecten van het FIFO-voorraadmodel op deze reeks transacties weergegeven wanneer markering tussen uitgiften en ontvangsten wordt gebruikt.

![FIFO met markering.](./media/fifo-with-marking.png)

**Uitleg bij het diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Fysieke transacties worden weergegeven met kortere, lichtgrijze pijlen.
- Financiële transacties worden weergegeven met langere zwarte pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
- Uitgiften uit voorraad worden weergegeven met verticale pijlen onder de tijdlijn.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Elke datum in het diagram wordt gescheiden door een dunne, zwarte verticale lijn. De datum wordt onderaan het diagram aangegeven.
- Voorraadafsluitingen worden aangegeven met een verticale rode streepjeslijn.
- Vereffeningen en markeringen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
