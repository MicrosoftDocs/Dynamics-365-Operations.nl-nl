---
title: FIFO met fysieke waarde en markering
description: "FIFO (First in, First out) is een voorraadmodel waarin de eerste ontvangsten het eerst worden uitgegeven. Financieel bijgewerkte uitgiften uit de voorraad worden vereffend met de eerste financieel bijgewerkte ontvangsten in de voorraad op basis van de financiële datum van de voorraadtransactie."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 18 - 57 - 00
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e3d189fc4dbc5c747a3473d3a221c739c323050
ms.lasthandoff: 03/29/2017


---

# <a name="fifo-with-physical-value-and-marking"></a>FIFO met fysieke waarde en markering

FIFO (First in, First out) is een voorraadmodel waarin de eerste ontvangsten het eerst worden uitgegeven. Financieel bijgewerkte uitgiften uit de voorraad worden vereffend met de eerste financieel bijgewerkte ontvangsten in de voorraad op basis van de financiële datum van de voorraadtransactie. 

Wanneer u FIFO gebruikt, moet u de FIFO-regel gebruiken. U kunt ook voorraadtransacties markeren zodat een bepaalde artikelontvangst wordt vereffend met een bepaalde uitgifte. Het wordt aangeraden de voorraad periodiek af te sluiten wanneer u het FIFO-voorraadmodel gebruikt. In de volgende voorbeelden wordt het effect geïllustreerd van het gebruik van FIFO in drie configuraties:

-   FIFO zonder de optie **Fysieke waarde opnemen**
-   FIFO met de optie **Fysieke waarde opnemen**
-   FIFO met markering

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO zonder de optie Fysieke waarde opnemen
In dit voorbeeld is de artikelmodelgroep niet gemarkeerd voor het opnemen van de fysieke waarde. De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor de hoeveelheid 2 met een waarde van USD 10,00 per stuk.
-   2b. Financiële voorraadontvangst voor de hoeveelheid 2 met een waarde van USD 10,00 per stuk.
-   3a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
-   4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   4b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   5a. Fysieke voorraaduitgifte voor de hoeveelheid 1 tegen een prijs van USD 20,00 per stuk (lopend gemiddelde van financieel bijgewerkte transacties).
-   5b. Financiële voorraaduitgifte voor de hoeveelheid 1 tegen een prijs van USD 20,00 per stuk (lopend gemiddelde van financieel bijgewerkte transacties).
-   6. Voorraadafsluiting is uitgevoerd. Op basis van de FIFO-methode wordt de eerste financieel bijgewerkte uitgifte vereffend met de eerste financieel bijgewerkte ontvangst. Op de uitgiftetransactie wordt een correctie van USD -10,00 doorgevoerd.

De nieuwe lopende gemiddelde kostprijs staat voor het gemiddelde van de bijgewerkte financiële transacties. In de volgende afbeeldingen worden de effecten van het FIFO-voorraadmodel voor deze reeks transacties weergegeven wanneer de optie **Fysieke waarde opnemen** niet wordt gebruikt. ![FIFO zonder Fysieke waarde opnemen](./media/fifowithoutincludephysicalvalue.gif) **Sleutel tot de diagram**

-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl wordt de waarde van de voorraadtransactie opgegeven in de indeling Quantity@Unitprice.
-   Een voorraadtransactiewaarde die tussen haakjes staat, geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
-   Een voorraadtransactiewaarde die niet tussen haakjes staat, geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
-   Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO met de optie Fysieke waarde opnemen
Als u het selectievakje **Fysieke waarde opnemen** inschakelt voor een artikel op de pagina **Artikelmodelgroep**, worden zowel fysieke als financiële ontvangsttransacties gebruikt bij het berekenen van de lopende gemiddelde kostprijs. Waar van toepassing wordt de fysiek bijgewerkte uitgiftetransactie ook gecorrigeerd. Als het selectievakje **Fysieke waarde opnemen** is uitgeschakeld, worden bij een voorraadafsluiting met het FIFO-voorraadmodel alleen vereffeningen gemaakt voor transacties die financieel zijn bijgewerkt. De volgende afbeelding geeft deze transacties weer:

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
-   7. Voorraadafsluiting is uitgevoerd. Op basis van de FIFO-methode wordt de eerste financiële uitgiftetransactie gecorrigeerd of vereffend met de eerste bijgewerkte (financiële of fysieke) ontvangst.

Transactie 5b wordt vereffend met ontvangsttransactie 1b. Er wordt een correctie van EUR -11,25 toegepast op deze uitgiftetransactie. De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel en fysiek bijgewerkte transacties, USD 27,50. In de volgende afbeelding worden de effecten van het FIFO-voorraadmodel voor deze reeks transacties weergegeven wanneer de optie **Fysieke waarde opnemen** wordt gebruikt. ![FIFO met Fysieke waarde opnemen](./media/fifowithincludephysicalvalue.gif) **Sleutel tot de diagram**

-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl wordt de waarde van de voorraadtransactie opgegeven in de indeling Quantity@Unitprice.
-   Een voorraadtransactiewaarde die tussen haakjes staat, geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
-   Een voorraadtransactiewaarde die niet tussen haakjes staat, geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
-   Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.

## <a name="fifo-with-marking"></a>FIFO met markering
Markeren is een proces waarmee u een uitgiftetransactie aan een ontvangsttransactie kunt koppelen (of markeren). Markering kan plaatsvinden voor- of nadat een transactie is geboekt. U kunt markering gebruiken als u zeker wilt zijn van de juiste kosten van de voorraad wanneer de transactie wordt geboekt of de voorraad wordt afgesloten. De afdeling Klantenservice heeft een spoedorder van een belangrijke klant aangenomen. Omdat dit een spoedorder is, moet u meer voor dit artikel betalen om in de vraag van de klant te voorzien. U moet ervoor zorgen dat de kosten van dit voorraadartikel worden weerspiegeld in de marge, of kosten van verkochte goederen, voor deze verkooporderfactuur. Wanneer de inkooporder wordt geboekt, wordt de voorraad ontvangen voor het bedrag van USD 120,00. Als dit verkooporderdocument aan de inkooporder wordt gekoppeld voordat de pakbon of factuur wordt geboekt, bedragen de kosten van de verkochte goederen USD 120,00, niet de huidige gemiddelde kosten voor het artikel. Als de pakbon of factuur voor de verkooporder wordt geboekt voordat er wordt gemarkeerd, wordt de COGS geboekt tegen de lopende, gemiddelde kostprijs. Voordat de voorraad wordt afgesloten, worden deze twee transacties naar elkaar gemarkeerd. Wanneer een ontvangsttransactie overeenkomt met een uitgiftetransactie, wordt de waarderingsmethode die in de artikelmodelgroep is gedefinieerd, genegeerd en worden de transacties met elkaar vereffend. U kunt een uitgiftetransactie aan een ontvangst koppelen voordat de transactie wordt geboekt. U kunt dit doen vanaf een verkooporderregel op de pagina **Details verkooporder**. U kunt de openstaande ontvangsttransacties bekijken op de pagina **Markering**. U kunt ook een uitgiftetransactie aan een ontvangst koppelen nadat de transactie is geboekt. U kunt een uitgiftetransactie voor een openstaande ontvangsttransactie voor een geïnventariseerd artikel afstemmen of markeren vanuit een geboekt voorraadcorrectiejournaal. De volgende afbeelding geeft deze transacties weer:

-   1a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   1b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 10,00 per stuk.
-   2a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   2b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 20,00 per stuk.
-   3a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 25,00 per stuk.
-   4a. Fysieke voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   4b. Financiële voorraadontvangst voor de hoeveelheid 1 met een waarde van USD 30,00 per stuk.
-   5a. Fysieke voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 21,25 per stuk (gemiddelde van financieel en fysiek bijgewerkte transacties).
-   5b. De financiële voorraaduitgifte voor de hoeveelheid 1 wordt gekoppeld aan voorraadontvangst 2b voordat de transactie wordt geboekt. Deze transactie wordt geboekt met een kostprijs van EUR 20,00 per stuk.
-   6a. Fysieke voorraaduitgifte voor de hoeveelheid 1 met een kostprijs van USD 21,25 per stuk.
-   7. Voorraadafsluiting is uitgevoerd. Omdat de financieel bijgewerkte FIFO-transactie is gemarkeerd voor een bestaande ontvangst, worden deze transacties met elkaar vereffend en wordt er niet gecorrigeerd.

De nieuwe gemiddelde kostprijs weerspiegelt het gemiddelde van de financieel en fysiek bijgewerkte transacties, USD 27,50. In het volgende afbeelding worden de effecten van het FIFO-voorraadmodel op deze reeks transacties weergegeven wanneer markering tussen uitgiften en ontvangsten wordt gebruikt. ![FIFO met Markering](./media/fifowithmarking.gif) **Sleutel tot het diagram**

-   Voorraadtransacties worden aangegeven met verticale pijlen.
-   Ontvangsten in voorraad worden aangegeven met verticale pijlen boven de tijdlijn.
-   Uitgiften uit voorraad worden aangegeven met verticale pijlen onder de tijdlijn.
-   Boven (of onder) elke verticale pijl wordt de waarde van de voorraadtransactie opgegeven in de indeling Quantity@Unitprice.
-   Een voorraadtransactiewaarde die tussen haakjes staat, geeft aan dat de voorraadtransactie fysiek naar de voorraad is geboekt.
-   Een voorraadtransactiewaarde die niet tussen haakjes staat, geeft aan dat de voorraadtransactie financieel naar de voorraad is geboekt.
-   Elke nieuwe ontvangst of uitgiftetransactie krijgt een nieuw label.
-   Elke verticale pijl heeft een opeenvolgende id, zoals *1a*. De id's geven de volgorde van voorraadtransactieboekingen op de tijdlijn aan.
-   Voorraadafsluitingen worden aangegeven met verticale rode streepjes en het label *Voorraadafsluiting*.
-   Vereffeningen die door voorraadafsluitingen worden uitgevoerd, worden weergegeven met rode diagonale stippelpijlen die van een ontvangst naar een uitgifte lopen.



