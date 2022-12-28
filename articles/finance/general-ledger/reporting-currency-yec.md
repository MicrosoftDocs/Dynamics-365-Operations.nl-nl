---
title: Aangiftevaluta niet in balans bij uitvoering jaarafsluiting
description: In dit artikel wordt uitgelegd hoe de aangiftevaluta niet meer in balans kan zijn wanneer de jaarafsluiting wordt uitgevoerd.
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850257"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>Aangiftevaluta niet in balans bij uitvoering jaarafsluiting

Nadat u de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** (de **Bewustzijn**-functie) hebt ingeschakeld, worden grootboektransacties die zijn vereffend, niet meer opgenomen in het openingssaldo van het volgende fiscale jaar wanneer de jaarafsluiting van het grootboek uitvoert. Als grootboektransacties worden uitgesloten die worden vereffend, kan dit een probleem zijn voor klanten bij de jaarafsluiting als het grootboek is gedefinieerd met een aangiftevaluta.

Grootboekvereffening wordt alleen voor de valuta voor boekhouding gedaan. Wanneer de grootboektransacties worden vereffend, zorgt validatie er alleen voor dat de debettransacties in valuta voor boekhouding gelijk zijn aan de creditrekeningvaluta. De aangiftevalutabedragen voor die grootboektransacties worden niet gevalideerd en ze hebben mogelijk geen gelijke debet- en creditbedragen. Bovendien wordt bij een grootboekvereffening niet automatisch een winst/verlies berekend en in de aangiftevaluta overboekt.

Vanwege deze beperkingen moet er een winst-/verliestransactie bestaan in de aangiftevaluta bij het doen van een grootboekvereffening. Als er geen winst/verliesrekening is opgenomen in de grootboekvereffening, wordt bij de jaarafsluiting een bericht getoond over het uit balans zijn.

In het volgende voorbeeld worden de stappen voor het oplossen van dit probleem uitgevoerd voordat de jaarafsluiting wordt uitgevoerd.

## <a name="example-setup"></a>Voorbeeld van instellingen

Om dit voorbeeld in te stellen, moet u de functie **Bewustzijn** inschakelen en hoofdrekening-110180 voor grootboekvereffening instellen. Hieronder ziet u een voorbeeld van de grootboektransacties die zijn geboekt in de rechtspersoon DEMF. De valuta voor boekhouding voor DEMF is Amerikaanse dollars (USD) en de aangiftevaluta is euro's (EUR).

![Geboekte grootboektransacties in de aangiftevaluta.](./media/reporting-currency-1.png)

Op de pagina **Grootboekvereffeningen** worden de grootboektransacties voor hoofdrekeningtransacties 110180. Selecteer de kolom en houd deze vast (of klik met de rechtermuisknop) in het raster en selecteer **Kolommen invoegen**. Voeg de kolom **Bedrag in aangiftevaluta** toe, zodat de transactievaluta, de valuta voor de boekhouding en de bedragen in de aangiftevaluta allemaal worden weergegeven.

![Bedrag in aangiftevaluta-kolom die is toegevoegd aan de pagina Grootboekvereffeningen.](./media/Ledger-settlement2.png)

De eerste twee grootboektransacties voor transacties 100, 00 EUR worden vereffend als één groep en de volgende twee grootboektransacties voor 200,00 EUR worden vereffend als een andere groep. (De twee transacties hebben dan verschillende vereffenings-id's.) Deze instellingen geven aan dat organisaties meerdere groepen grootboektransacties hebben die op verschillende tijdstippen worden vereffend en verschillende vereffeningsdatums hebben. Nadat de vereffening is voltooid, wordt op de pagina **Ggrootboekvereffeningen** de volgende informatie weergegeven wanneer deze is gefilterd om transacties met de status **Vereffend** weer te geven.

![Vereffende transacties op de pagina Grootboekvereffeningen.](./media/Settled-trans-filtered3.png)

Selecteer op de pagina **Grootboekvereffeningen** de kolom **Bedrag** en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens **Deze kolom totaliseren**. Herhaal deze stap voor de kolommen **Bedrag in aangiftevaluta**. De valuta voor boekhouding moet een verschil van 0 (nul) hebben om te kunnen worden vereffend. Het vereffeningsbedrag voor de aangiftevaluta wordt echter niet gevalideerd. Hieronder ziet u een verschil van -27,79 USD voor de aangiftevaluta.

![Verschil voor de aangiftevaluta.](./media/Difference4.png)

## <a name="year-end-close"></a>Jaarafsluiting

Als de jaarafsluiting nu wordt uitgevoerd voor 2022, eindigt het proces in een niet-in-balansfout. Deze fout wordt direct veroorzaakt door het feit dat de aangiftevaluta geen grootboekvereffeningsbedrag heeft dat netto 0 (nul) is.

![Foutbericht dat aangeeft dat het bedrag van de grootboekvereffening niet 0 (nul) is.](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>Winst/verlies in aangiftevaluta boeken

Om de jaarafsluiting met succes uit te voeren, moet het verschil in het bedrag van de aangiftevaluta worden verantwoord, doorgaans als winst of verlies, en worden opgenomen in de grootboekvereffening. Winst/verlies bij aangiftevaluta kan op meerdere manieren worden geboekt:

- Als de hoofdrekening crediteuren of klanten is, wordt de vereiste winst/verlies gegenereerd door de vereffening van AR/AP van die documenten. Die vermelding in de boekhouding moet worden opgenomen in de grootboekvereffening wanneer de bijbehorende grootboektransacties van de factuur, betalingen, creditnota's, enzovoort worden vereffend.
- Als de hoofdrekening een andere rekening is dan crediteuren of debiteuren, moet winst/verlies handmatig worden ingevoerd. Wanneer winst/verlies wordt geboekt, wordt het detailniveau voor de vermelding in de boekhouding bepaald door uw organisatie.
- Bepaal voor elke hoofdrekening het winst-/verliesbedrag voor de aangiftevaluta dat moet worden geboekt.

Zoals eerder is beschreven, kan deze boeking worden uitgevoerd op de pagina **Grootboekvereffeningen**.

1. Filteren op het datumbereik waar u winst/verlies voor wilt maken. Als u van plan bent om een winst/verlies per maand te boeken, filtert u voor elke maand. Als u van plan bent om een winst/verlies per fiscaal jaar te maken, filtert u het hele jaar.
2. Filter op de hoofdrekening.
3. Filter op de status, zodat alleen **vereffende** transacties worden weergegeven.
4. Tel een totaal op bij het bedrag in de kolom **Bedrag in aangiftevaluta**.
5. Als u winst/verlies op meer gedetailleerd niveau wilt boeken, kunt u extra filteren op de vereffenings-id, financiële dimensies, enzovoort. Het totaalbedrag voor het bedrag in de kolom **Bedrag in aangiftevaluta** staat voor het bedrag dat voor winst/het verlies wordt geboekt.
6. Ga naar **Grootboek \> Journaalboekingen \> Correctiejournalen aangiftevaluta**.
7. Voer de transactie voor winst/verlies in. In dit journaal wordt alleen een correctie in de aangiftevaluta geboekt. De geboekte bedragen voor de transactievaluta en de boekhoudvaluta zijn altijd 0 (nul). Als dit journaal niet eerder is gebruikt, moet u mogelijk een journaalnaam maken met het journaaltype **Correctie aangiftevaluta** via **Grootboek \> Journaalinstellingen \> Journaalnamen**.
8. Deze correctie wordt niet geboekt als handmatige invoer in de hoofdrekening niet is toegestaan. Daarom kan het zijn dat u de parameter **Handmatige invoer niet toestaan** op de pagina **Hoofdrekening** tijdelijk moet uitschakelen.

![Handmatige invoer op de pagina Journaalboekstuk.](./media/Manual-entry6.png)

Nadat u het correctiejournaal hebt geboekt, gaat u terug naar de pagina **Grootboekvereffeningen** en selecteert u de hoofdrekening voor wie u winst/verlies hebt geboekt. De correctie voor winst/verlies moet worden opgenomen in een grootboekvereffening. Aangezien het bedrag van de aangiftevaluta niet hoeft te worden vereffend met 0 (nul), kunt u vereffening van eerdere transacties ongedaan maken en deze vervolgens opnieuw vereffenen, maar deze keer winst/verlies opnemen. Hoe precies u wilt zijn voor het boeken van winst/verlies en de vereffening daarvan in grootboekvereffeningen bepaalt uw organisatie.

In de volgende afbeelding ziet u dat de vereffening van de transacties voor 200 EUR ongedaan zijn gemaakt en vervolgens weer zijn gemarkeerd voor vereffening. Deze keer wordt winst/verlies erin opgenomen.

![Correctie van winst/verlies op de pagina Grootboekvereffeningen.](./media/gain-loss7.png)

Wijzig het filter **Status**, nadat de transacties zijn vereffend, zodat op de pagina **vereffende** transacties worden weergegeven. Het totaal voor het bedrag in de kolom **Bedrag in aangiftevaluta** is nu 0 (nul). De jaarafsluiting kan nu met succes worden uitgevoerd.

![Geslaagde jaarafsluiting.](./media/Zero-settled8.png)
