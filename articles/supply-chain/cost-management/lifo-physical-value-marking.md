---
title: LIFO met fysieke waarde en markering
description: LIFO (Last in, First out) is een voorraadmodel waarin de laatste (nieuwste) ontvangsten het eerst worden uitgegeven. Uitgiften uit de voorraad worden vereffend met de laatste ontvangsten in de voorraad op basis van de datum van de voorraadtransactie.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0ea2c71458f92d048706a6e263d0da1830bdcde
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "344197"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO met fysieke waarde en markering

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

LIFO (Last in, First out) is een voorraadmodel waarin de laatste (nieuwste) ontvangsten het eerst worden uitgegeven. Uitgiften uit de voorraad worden vereffend met de laatste ontvangsten in de voorraad op basis van de datum van de voorraadtransactie. 

LIFO (Last in, First out) is een voorraadmodel waarin de laatste (nieuwste) ontvangsten het eerst worden uitgegeven. Uitgiften uit de voorraad worden vereffend met de laatste ontvangsten in de voorraad op basis van de datum van de voorraadtransactie. Wanneer u LIFO gebruikt, hoeft u de LIFO-regel niet te gebruiken. U kunt ook voorraadtransacties markeren zodat een bepaalde artikelontvangst wordt vereffend met een bepaalde uitgifte. Wanneer u gebruikmaakt van het LIFO-voorraadmodel, is het raadzaam om de voorraad periodiek af te sluiten. 

In de volgende voorbeelden wordt het effect geïllustreerd van het gebruik van LIFO in drie configuraties:

-   LIFO zonder de optie **Fysieke waarde opnemen**
-   LIFO met de optie **Fysieke waarde opnemen**
-   LIFO met markering

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO zonder de optie Fysieke waarde opnemen
In dit voorbeeld is de artikelmodelgroep niet gemarkeerd voor het opnemen van de fysieke waarde. De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   3a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
-   4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   4b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   5a. Fysieke voorraaduitgifte voor de hoeveelheid 1 tegen een prijs van USD 20,00 per stuk (lopend gemiddelde van financieel bijgewerkte transacties).
-   5b. Financiële voorraaduitgifte voor de hoeveelheid 1 tegen een prijs van USD 20,00 per stuk (lopend gemiddelde van financieel bijgewerkte transacties).
-   6. Voorraadafsluiting is uitgevoerd. De laatste, financieel bijgewerkte uitgifte wordt op basis van de LIFO-methode vereffend met de laatste, financieel bijgewerkte ontvangst. Op de uitgiftetransactie wordt een correctie van USD 10,00 doorgevoerd.

De nieuwe lopende gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel bijgewerkte transacties met EUR 15,00. In de volgende afbeeldingen worden de effecten van het LIFO-voorraadmodel voor deze reeks transacties weergegeven wanneer de optie **Fysieke waarde opnemen** niet wordt gebruikt. ![LIFO zonder fysieke waarde opnemen](./media/lifowithoutincludephysicalvalue.gif) 

**Uitleg bij het diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
- Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
- Boven (of onder) elke verticale pijl ziet u de waarde van de voorraadtransactie met de notatie Hoeveelheid@Eenheidsprijs.
- Een voorraadtransactiewaarde die tussen haakjes staat, geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
- Een voorraadtransactiewaarde die niet tussen haakjes staat, geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO met de optie Fysieke waarde opnemen
Als u het selectievakje **Fysieke waarde opnemen** inschakelt voor een artikel op de pagina **Artikelmodelgroepen**, worden zowel fysieke als financiële ontvangsttransacties gebruikt bij het berekenen van de lopende gemiddelde kostprijs. Waar van toepassing wordt de fysiek bijgewerkte uitgiftetransactie ook gecorrigeerd. Als het selectievakje **Fysieke waarde opnemen** is uitgeschakeld, worden bij een voorraadafsluiting met het LIFO-voorraadmodel alleen vereffeningen gemaakt voor transacties die financieel zijn bijgewerkt. 

De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   3a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
-   4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   4b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   5a. Fysieke voorraaduitgifte voor de hoeveelheid 1 tegen een prijs van USD 21,25 per stuk (lopend gemiddelde van financieel en fysiek bijgewerkte transacties).
-   5b. Financiële voorraaduitgifte voor de hoeveelheid 1 tegen een prijs van USD 21,25 per stuk (lopend gemiddelde van financieel en fysiek bijgewerkte transacties).
-   6a. Fysieke voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 21,25 per stuk.
-   7. Voorraadafsluiting is uitgevoerd. Op basis van de LIFO-methode wordt de laatste uitgiftetransactie gecorrigeerd of vereffend met de laatste bijgewerkte ontvangst.

Transactie 6a wordt gecorrigeerd naar ontvangsttransactie 4b. Deze transacties worden niet vereffend, omdat de ontvangst fysiek maar niet financieel wordt bijgewerkt. In plaats daarvan wordt er alleen een correctie van USD 8,75 naar de fysieke uitgiftetransactie geboekt. Transactie 5b wordt gecorrigeerd naar fysieke ontvangsttransactie 3a. Deze transacties worden niet door het systeem vereffend, omdat deze beide transacties niet financieel worden bijgewerkt. In plaats daarvan wordt er alleen een correctie van USD -3,75 naar de fysieke uitgiftetransactie geboekt. De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel en fysiek bijgewerkte transacties, USD 20,00. 

In de volgende afbeelding worden de effecten van het LIFO-voorraadmodel voor deze reeks transacties weergegeven wanneer de optie **Fysieke waarde opnemen** wordt gebruikt. ![LIFO met fysieke waarde opnemen](./media/lifowithincludephysicalvalue.gif) 

**Uitleg bij het diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
- Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
- Boven (of onder) elke verticale pijl ziet u de waarde van de voorraadtransactie met de notatie Hoeveelheid@Eenheidsprijs.
- Een voorraadtransactiewaarde die tussen haakjes staat, geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
- Een voorraadtransactiewaarde die niet tussen haakjes staat, geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="lifo-with-marking"></a>LIFO met markering
Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markering gebruiken als u zeker wilt zijn van de juiste kosten van de voorraad wanneer de transactie wordt geboekt of de voorraad wordt afgesloten. De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor dit artikel betalen om in de vraag van de klant te voorzien. 

U moet ervoor zorgen dat de kosten van dit voorraadartikel worden weerspiegeld in de marge, of kosten van verkochte goederen, voor deze verkooporderfactuur. Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van USD 120,00. Als dit verkooporderdocument aan de inkooporder wordt gekoppeld voordat de pakbon of factuur wordt geboekt, bedragen de kosten van de verkochte goederen USD 120,00, niet de huidige gemiddelde kosten voor het artikel. Als de pakbon of factuur voor de verkooporder wordt geboekt voordat er wordt gemarkeerd, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs. 

Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd. 

U kunt een uitgiftetransactie aan een ontvangst koppelen voordat de transactie wordt geboekt. U kunt dit doen vanaf een verkooporderregel op de pagina **Details verkooporder**. U kunt de openstaande ontvangsttransacties bekijken op de pagina **Markering**. 

U kunt ook een uitgiftetransactie aan een ontvangst koppelen nadat de transactie is geboekt. U kunt een uitgiftetransactie voor een openstaande ontvangsttransactie voor een geïnventariseerd artikel afstemmen of markeren vanuit een geboekt voorraadcorrectiejournaal. 

De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   3a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
-   4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   4b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   5a. Fysieke voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 21,25 per stuk (gemiddelde van financieel en fysiek bijgewerkte transacties).
-   5b. De financiële voorraaduitgifte voor de hoeveelheid 1 wordt gekoppeld aan voorraadontvangst 2b voordat de transactie wordt geboekt. Deze transactie wordt geboekt met een kostprijs van USD 20,00 per stuk.
-   6a. Fysieke voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 21,25 per stuk.
-   7. Voorraadafsluiting is uitgevoerd. Omdat de financieel bijgewerkte FIFO-transactie is gemarkeerd voor een bestaande ontvangst, worden deze transacties met elkaar vereffend en wordt er niet gecorrigeerd.

De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel en fysiek bijgewerkte transacties, USD 27,50. 

In het volgende afbeelding worden de effecten van het LIFO-voorraadmodel op deze reeks transacties weergegeven wanneer markering tussen uitgiften en ontvangsten wordt gebruikt. ![LIFO met markering](./media/lifowithmarking.gif) 

**Uitleg bij diagram**

- Voorraadtransacties worden aangegeven met verticale pijlen.
- Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
- Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
- Boven (of onder) elke verticale pijl ziet u de waarde van de voorraadtransactie met de notatie Hoeveelheid@Eenheidsprijs.
- Een voorraadtransactiewaarde die tussen haakjes staat, geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
- Een voorraadtransactiewaarde die niet tussen haakjes staat, geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
- Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
- Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
- Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
- Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.




