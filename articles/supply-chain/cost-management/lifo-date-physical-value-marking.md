---
title: LIFO-datum met fysieke waarde en markering
description: LIFO-datum (Last In, First Out Date) is een voorraadmodel dat gebaseerd is op het LIFO-principe. Uitgiften uit de voorraad worden vereffend met de recentste ontvangsten in de voorraad op basis van de datum van de voorraadtransactie. Als er op de LIFO-datum geen artikel vóór de uitgifte wordt ontvangen, wordt de uitgifte vereffend met de ontvangsten die na de datum van de artikeluitgifte plaatsvinden. Meerdere uitgiften op dezelfde datum kunnen in de volgende 'laatste uitgifte - laatste ontvangst' worden vereffend.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fed3de8741b375cf4992578db3e57d6e5a35a93
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425499"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-datum met fysieke waarde en markering

[!include [banner](../includes/banner.md)]

LIFO-datum (Last In, First Out Date) is een voorraadmodel dat gebaseerd is op het LIFO-principe. Uitgiften uit de voorraad worden vereffend met de recentste ontvangsten in de voorraad op basis van de datum van de voorraadtransactie. Als er op de LIFO-datum geen artikel vóór de uitgifte wordt ontvangen, wordt de uitgifte vereffend met de ontvangsten die na de datum van de artikeluitgifte plaatsvinden. Meerdere uitgiften op dezelfde datum kunnen in de volgende 'laatste uitgifte - laatste ontvangst' worden vereffend. 

Als u het voorraadmodel LIFO-datum (Last In, First Out Date) gebruikt en er vóór de uitgifte geen artikel wordt ontvangen, wordt de uitgifte vereffend met de ontvangsten die na de datum van de artikeluitgifte plaatsvinden. Meerdere uitgiften op dezelfde datum kunnen in de volgorde van laatste uitgifte worden vereffend. Wanneer u LIFO-datum gebruikt, hoeft u de LIFO-datumregel niet te gebruiken. U kunt ook voorraadtransacties markeren zodat een bepaalde artikelontvangst wordt vereffend met een bepaalde uitgifte. 

Het wordt aangeraden de voorraad periodiek af te sluiten wanneer u het LIFO-datumvoorraadmodel gebruikt. 

In de volgende voorbeelden wordt het effect geïllustreerd van het gebruik van LIFO-datum in drie configuraties:

-   LIFO-datum zonder de optie **Fysieke waarde opnemen**
-   LIFO-datum met de optie **Fysieke waarde opnemen**
-   LIFO-datum met markering

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-datum zonder de optie Fysieke waarde opnemen
In dit voorbeeld is de artikelmodelgroep niet gemarkeerd voor het opnemen van de fysieke waarde. De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   3a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
-   4a. Fysieke voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 15,00 (gemiddelde van financieel bijgewerkte transacties).
-   4b. Financiële voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 15,00 (gemiddelde van financieel bijgewerkte transacties).
-   5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   6. Voorraadafsluiting is uitgevoerd. Op basis van de methode LIFO-datum wordt de uitgifte die het laatst financieel is bijgewerkt, vereffend met de ontvangst die het laatst financieel is bijgewerkt. Voor de uitgiftetransactie is een correctie van USD 5,00 vereist. Deze transacties worden met elkaar vereffend.

De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel bijgewerkte transacties met USD 15,00. 

In de volgende afbeelding worden de effecten van het voorraadmodel LIFO-datum weergegeven wanneer de optie **Fysieke waarde opnemen** niet wordt gebruikt. ![LIFO-datum met fysieke waarde opnemen](./media/lifodatewithoutincludephysicalvalue.gif) 

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-datum met de optie Fysieke waarde opnemen
U kunt het selectievakje **Fysieke waarde opnemen** inschakelen voor een artikel op de pagina **Artikelmodelgroepen**. In dit geval worden zowel fysieke als financiële ontvangsttransacties gebruikt voor het berekenen van de lopende gemiddelde kostprijs. Waar van toepassing wordt de fysiek bijgewerkte uitgiftetransactie ook gecorrigeerd. Als het selectievakje **Fysieke waarde opnemen** is uitgeschakeld, worden bij een voorraadafsluiting met het voorraadmodel LIFO-datum alleen vereffeningen gemaakt voor transacties die financieel zijn bijgewerkt. 

In dit voorbeeld is de artikelmodelgroep niet gemarkeerd voor het opnemen van de fysieke waarde. 

De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   3a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
-   4a. Fysieke voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 18,33 per stuk (gemiddelde van financieel bijgewerkte transacties).
-   4b. Financiële voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 18,33 per stuk (gemiddelde van financieel bijgewerkte transacties).
-   5a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   5b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   6. Voorraadafsluiting is uitgevoerd. Op basis van de methode LIFO-datum wordt de laatst bijgewerkte uitgifte gecorrigeerd of vereffend met de laatst bijgewerkte ontvangst. Deze transacties worden niet met elkaar vereffend, omdat de financiële ontvangsttransactie is gecorrigeerd naar een fysieke bijwerktransactie. In plaats daarvan wordt voor de uitgiftetransactie slechts een correctie van EUR 6,67 uitgevoerd.

De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel bijgewerkte transacties met USD 20,00. 

In de volgende afbeelding worden de effecten van het voorraadmodel LIFO-datum weergegeven wanneer de optie **Fysieke waarde opnemen** wel wordt gebruikt. ![LIFO-datum met fysieke waarde opnemen](./media/lifodatewithincludephysicalvalue.gif) 

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

## <a name="lifo-date-with-marking"></a>LIFO-datum met markering
Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markering gebruiken als u zeker wilt zijn van de juiste kosten van de voorraad wanneer de transactie wordt geboekt of de voorraad wordt afgesloten. 

De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor dit artikel betalen om aan de vraag van de klant te voldoen. U moet ervoor zorgen dat de kosten van dit voorraadartikel worden weerspiegeld in de marge, of kosten van verkochte goederen, voor deze verkooporderfactuur. 

Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van USD 120,00. Als dit verkooporderdocument aan de inkooporder wordt gekoppeld voordat de pakbon of factuur wordt geboekt, bedragen de kosten van de verkochte goederen USD 120,00, niet de huidige gemiddelde kosten voor het artikel. Als de pakbon of factuur voor de verkooporder wordt geboekt voordat er wordt gemarkeerd, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs. 

Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd. 

Een ontvangsttransactie wordt bijvoorbeeld aan een uitgiftetransactie gekoppeld. In dit geval wordt de waarderingsmethode die is gedefinieerd in de artikelmodelgroep van het artikel genegeerd en worden deze transacties met elkaar vereffend. 

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
-   7. Voorraadafsluiting is uitgevoerd. Omdat de financieel bijgewerkte FIFO-transactie (First in, First out) is gemarkeerd voor een bestaande ontvangst, worden deze transacties met elkaar vereffend en wordt er niet gecorrigeerd.

De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel en fysiek bijgewerkte transacties met USD 27,50. 

De volgende afbeelding illustreert de gevolgen van het LIFO-voorraadmodel bij gebruik van markering tussen uitgiften en ontvangsten. ![LIFO-datum met markering](./media/lifodatewithmarking.gif) 

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




