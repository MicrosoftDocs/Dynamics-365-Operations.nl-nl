---
title: Recency-, frequentie- en monetaire analyse (RFM) instellen
description: In dit onderwerp wordt beschreven hoe u een Recency-, Frequentie-, en Monetaire analyse (RFM) van uw klanten kunt instellen.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c7cb79fa82b579bee01e51cb635597cc5f711a98
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411452"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Recency-, frequentie- en monetaire analyse (RFM) instellen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een Recency-, Frequentie-, en Monetaire analyse (RFM) van uw klanten kunt instellen.

Recency-, frequentie-, monetaire (RFM)-analyse is een marketinghulpmiddel dat uw organisatie kan gebruiken om de gegevens te beoordelen die door klantaankopen worden gegenereerd. Nadat u RFM analyse instelt, krijgen klanten een berekende RFM-score wanneer ze aankopen doen. De RFM-score kan een beoordeling zijn met drie cijfers of een samengeteld cijfer zijn, zijn afhankelijk van hoe uw organisatie RFM-analyse heeft geconfigureerd. Als uw organisatie een beoordeling met drie cijfers voor de score gebruikt, werkt dit als volgt:

- Het eerste cijfer is de recencybeoordeling, waarmee wordt aangegeven hoe recent de klant een aankoop heeft gedaan bij uw organisatie.
- Het tweede cijfer is de frequentiebeoordeling, waarmee wordt aangegeven hoe vaak de klant iets aanschaft van uw organisatie.
- Het derde cijfer is de monetaire beoordeling, waarmee wordt aangegeven hoeveel de klant uitgeeft wanneer deze iets aanschaft van uw organisatie.

Uw organisatie heeft bijvoorbeeld de beoordelingen op een schaal van 1 tot 5 ingesteld, waar 5 het hoogste cijfer is. In dit geval geeft een klantbeoordeling van 535 u de volgende informatie over de klant:

- **Recencyscore van 5** – De klant heeft onlangs een aankoop gedaan.
- **Frequentiebeoordeling van 3** – De klant koopt redelijk vaak producten van uw organisatie.
- **Monetaire score van 5** - Wanneer de klant een inkoop doet, geeft deze een aanzienlijk bedrag uit.

Als uw organisatie een samengeteld cijfer gebruikt voor de score, worden de individuele beoordelingen samengevoegd. Voor hetzelfde voorbeeld heeft de klant een beoordeling van 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>RFM-analyse voor de klanten in uw organisatie instellen

1. Ga naar **Callcenter** \> **Periodiek** \> **RFM-analyse**.
2. Op de pagina **RFM-analyse** selecteert u **Nieuw**. Voer in het veld **RFM-definitie** een naam voor de RFM-definitie in. U kunt bijvoorbeeld, kunt u de definitie RFM-A noemen.
3. Voer een begin- en einddatum voor deze RFM-definitie in.
4. Doe op het sneltabblad **Algemeen** het volgende:

    - Als elke sectie van de RFM-score een gelijk aantal klanten moet bevatten, schakelt u het selectievakje **Gelijkmatige distributie** in.
    - Schakel het selectievakje **Scores toevoegen** in om de drie scores bij elkaar op te tellen. Dit geeft een klant bijvoorbeeld een RFM-score van 13 in plaats van 535.
    - Schakel het selectievakje **Historie opslaan** in om te vereisen dat het systeem de statistische gegevens opslaat voor klanten, zodat de gegevens kunnen worden gebruikt om de RFM-score te berekenen.

5. Doe op het sneltabblad **Recency** het volgende:

    - Voer in het veld **Afdelingen** het aantal onderverdelingen of groepen in die worden gebruikt om de recencyscore voor klanten te berekenen. Als u bijvoorbeeld 100 klanten hebt, betekent een afdeling van 5 dat er 20 klanten zijn voor elke score. De 20 klanten die het meest recent een aankoop hebben gedaan, hebben een recencyscore van 5. De volgende 20 klanten hebben een recencyscore van 4, enzovoort. Als u 50 klanten hebt, hebben 10 klanten een recencyscore van 5, 10 hebben een recencyscore van 4, enzovoort.
    - Selecteer in het veld **Prioriteit** hoeveel gewicht de recencyparameter krijgt in vergelijking met de andere parameters wanneer de RFM-score wordt berekend voor een klant. U kunt bijvoorbeeld meer waarde hechten aan de recencyscore dan de monetaire score.
    - Voer in het veld **Factor** de waarde in waarmee de recencyscore moet worden vermenigvuldigd. Als u geen waarde invoert, wordt de score niet vermenigvuldigd.
    - Selecteer in het veld **Periode** de periode waarvoor de recencyscore wordt berekend. Bijvoorbeeld per week of per maand.

6. Doe op het sneltabblad **Frequentie** het volgende:

    - Voer in het veld **Afdelingen** het aantal onderverdelingen of groepen in die worden gebruikt om de frequentiescore voor klanten te berekenen.
    - Selecteer in het veld **Prioriteit** hoeveel gewicht de frequentieparameter krijgt in vergelijking met de andere parameters wanneer de RFM-score wordt berekend voor een klant.
    - Voer in het veld **Factor** de waarde in waarmee de frequentiescore moet worden vermenigvuldigd. Als u geen waarde invoert, wordt de score niet vermenigvuldigd.

7. Doe op het sneltabblad **Monetair** het volgende:

    - Voer in het veld **Afdelingen** het aantal onderverdelingen of groepen in die worden gebruikt om de monetaire score voor klanten te berekenen.
    - Selecteer in het veld **Prioriteit** hoeveel gewicht de monetaire parameter krijgt in vergelijking met de andere parameters wanneer de RFM-score wordt berekend voor een klant.
    - Voer in het veld **Factor** de waarde in waarmee de monetaire score moet worden vermenigvuldigd. Als u geen waarde invoert, wordt de score niet vermenigvuldigd.
    - Geef in het veld **Bruto/netto** op of de monetaire score van de klant moet worden vermenigvuldigd met het bruto- of nettofactuurbedrag.
    - Als de retourbedragen van een klant moeten worden afgetrokken van de totale factuurberekening van de klant, schakelt u het selectievakje **Retouren aftrekken** in.

## <a name="view-a-customers-rfm-score"></a>RFM-score van klanten weergeven

Via deze procedure kunt u de RFM-score van een klant weergeven.

1. Ga naar **Callcenter** \> **Journalen** \> **Klantenservice**.
2. Selecteer op de pagina **Klantenservice** in het deelvenster **Klantenservice** in de zoekvelden het type trefwoord om op te zoeken en voer de zoektekst in.
3. Selecteer **Zoeken**.
4. Selecteer op de pagina **Klant zoeken** de gewenste klantrecord en klik op **Klant selecteren**.

De RFM-score wordt weergegeven in de groep **Orderhistorie** rechts op de pagina **Klantenservice**.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>Weergeef of wis de historie van een RFM-analyserecord

Met deze procedure kunt u de historie van een FRM-analyse record weergeven of wissen.

1. Ga naar **Callcenter** \> **Periodiek** \> **RFM-analyse**.
2. Selecteer op de pagina **RFM-analyse** de record die u wilt weergeven.
3. Selecteer het sneltabblad **Historie** om de recordhistorie te bekijken.
4. Selecteer **Historie wissen** om de recordhistorie te wissen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]