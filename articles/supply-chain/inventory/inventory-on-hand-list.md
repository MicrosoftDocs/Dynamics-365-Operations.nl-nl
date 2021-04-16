---
title: Lijst met voorhanden voorraad
description: In dit onderwerp wordt beschreven hoe u de lijst Voorhanden voorraad gebruikt om details over voorhanden voorraad te controleren. Er worden enkele manieren weergegeven waarop de verschillende filter- en sorteeropties samenwerken en de manier waarop deze opties kunnen leiden tot onverwachte resultaten wanneer deze worden gecombineerd.
author: sherry-zheng
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1e054c4010f730519532b67fe900573480ea2a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825982"
---
# <a name="inventory-on-hand-list"></a>Lijst met voorhanden voorraad

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de lijst **Voorhanden voorraad** gebruikt om details over voorhanden voorraad te controleren. Er worden enkele manieren weergegeven waarop de verschillende filter- en sorteeropties samenwerken en de manier waarop deze opties kunnen leiden tot onverwachte resultaten wanneer deze worden gecombineerd.

## <a name="query-your-on-hand-inventory"></a>Uw voorhanden voorraad opvragen

Als u de voorraad wilt controleren, gaat u naar **Voorraadbeheer \> Query's en rapporten \> Voorhanden voorraad**.

De pagina **Voorhanden voorraad** wordt automatisch bijgewerkt wanneer transacties worden uitgevoerd in voorraad. Deze transacties kunnen prognose-, fysieke of financiële transacties zijn.

Gebruik de volgende hulpmiddelen om de set producten te vinden die u zoekt:

- Selecteer in het actievenster [**Dimensies**](#dimensions) om een dialoogvenster te openen waarin u kolommen kunt toevoegen of verwijderen die in het raster **Voorhanden** worden weergegeven.
- Voer in het [deelvenster **Filters**](#filters-pane) waarden in voor specifieke velden om alleen records weer te geven die overeenkomen met die waarden. Filters die u hier definieert, gelden voor brontabellen die later kunnen worden samengevoegd op basis van de dimensies die u hebt geselecteerd om weer te geven. Zie de [voorbeelden](#examples) verderop in dit onderwerp voor meer informatie over de manier waarop dit gedrag van invloed kan zijn op de resultaten.
- Selecteer in het deelvenster **Filters** de optie **Toepassen** om de lijst met overeenkomende voorhanden voorraad in het raster **Voorhanden** te genereren.
- Selecteer in het raster **Voorhanden** een kolomkop om te sorteren of filteren op waarden in die kolom. Een snelfilter boven aan het raster bevat extra filteropties. Deze filters zijn van toepassing op de resultaten, niet op de brontabellen. Zie de [voorbeelden](#examples) verderop in dit onderwerp voor meer informatie over de manier waarop dit gedrag van invloed kan zijn op de resultaten.

Voor elk overeenkomend artikel bevat het raster **Voorhanden** de volgende kolommen met voorraadgegevens.

| Kolom | Omschrijving |
|---|---|
| Fysieke voorraad | De fysieke hoeveelheid die beschikbaar is in voorraad. |
| Fysiek gereserveerd | De totale hoeveelheid die fysiek is gereserveerd. |
| Fysiek beschikbaar | De beschikbare (niet gereserveerde) hoeveelheid die beschikbaar is in fysieke voorraad.<p>**Fysiek beschikbaar** is een berekend veld. De waarde is gelijk aan de **fysieke voorraad** min de **Fysiek gereserveerde** waarde.</p> |
| Fysiek beschikbaar in extra dimensies | De beschikbare fysieke hoeveelheid voor alle dimensies die worden weergegeven in het raster. |
| Totaal van order | De totale hoeveelheid die is opgenomen op inkomende orders of die een positieve hoeveelheid in verschillende voorraadjournalen heeft. |
| In bestelling | De totale hoeveelheid die is opgenomen op uitgaande orders of die een negatieve hoeveelheid in verschillende voorraadjournalen heeft. |
| Besteld en gereserveerd | De totale hoeveelheid die is gereserveerd op bestelde ontvangsten. De waarde in dit veld staat voor de totale hoeveelheid artikelen in uitgaande transacties met de status _Besteld en gereserveerd_. Artikelen die zijn gereserveerd als besteld, zijn niet fysiek beschikbaar in de voorraad. Daarom kunnen ze niet rechtstreeks worden verzameld en geleverd. |
| Beschikbaar voor reservering | De totale hoeveelheid voorhanden voorraad kan worden gereserveerd.<p>**Opmerking:** als het selectievakje **Bestelde artikelen reserveren** is ingeschakeld op de pagina **Parameters voor voorraad- en magazijnbeheer**, bevat de waarde in dit veld verwachte ontvangsten. Als het selectievakje is uitgeschakeld, worden verwachte ontvangsten uitgesloten van de waarde.</p> |
| Totaal beschikbaar | De totale beschikbare hoeveelheid.<p>**Totaal beschikbaar** is een berekend veld. De waarde is gelijk aan de **beschikbare fysieke** waarde plus de waarde **Totaal van order** min de waarde **In bestelling**.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Filters toepassen om de records te vinden die u zoekt

Gebruik het deelvenster **Filters** om de voorhanden voorraad te filteren zodat alleen records worden opgenomen waarin de veldwaarden voldoen aan de filtercriteria. Volg deze stappen om een filter te definiëren.

1. Zoek in het deelvenster **Filters** het veld waarop u wilt filteren.
2. Selecteer in het veld onder de naam van het doelveld een logische operator (bijvoorbeeld *begint met*, *gelijk aan* of *groter dan*).
3. Typ of selecteer de waarde waarnaar moet worden gezocht.

> [!IMPORTANT]
> De pagina **Voorhanden voorraad** wordt samengesteld uit een gedetailleerde tabel met voorhanden voorraad waarin alle beschikbare dimensies zijn opgenomen. De lijst op deze pagina is echter een overzicht. Daarom kunnen rijen uit de brontabel worden gecombineerd door waarden te aggregeren op basis van de dimensies die worden weergegeven.
>
> De filters die u in het deelvenster **Filters** definieert, zijn van toepassing op de brontabel en niet op de samengevoegde lijst. Dit gedrag kan soms tot onverwachte resultaten leiden. Zie de [voorbeelden](#examples) verderop in dit onderwerp voor meer informatie over de manier waarop dit gedrag van invloed kan zijn op de resultaten.
> 
> De [filters die in het raster worden vermeld](#grid-filters) hebben echter *wel* betrekking op de samengevoegde lijst. Deze filters bevatten zowel het snelfilter boven aan het raster als het filter voor elke kolomkop.

U kunt de set filters die beschikbaar zijn, in het deelvenster **Filters** wijzigen door de volgende stappen uit te voeren.

- Als u een filter uit het deelvenster wilt verwijderen, selecteert u de knop **Sluiten** (**X**) ervan.
- Als u een filter wilt toevoegen, selecteert u boven aan het deelvenster **Filters** **Toevoegen**. Het dialoogvenster **Filter toevoegen** dat verschijnt, bevat een lijst met de beschikbare velden. Ook wordt informatie weergegeven over het gegevenstype en de tabel voor elk veld. Gebruik de kolomkoppen om de lijst te filteren en te sorteren zoals u wilt en schakel vervolgens het selectievakje in voor elk veld dat u aan het deelvenster **Filter** wilt toevoegen. Wanneer u klaar bent, selecteert u **Invoegen** om de wijzigingen toe te passen.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Selecteer de dimensies die u wilt weergeven

Dimensies geven meer informatie over elk artikel in de lijst met voorhanden voorraad en bieden u meer manieren om de lijst te sorteren en te filteren. De dimensies die u selecteert, bepalen ook hoe rijen worden samengevoegd op de pagina **Voorhanden voorraad**. Deze samenvoeging kan op haar beurt invloed hebben op de manier waarop rijen uit de brontabellen worden gecombineerd in de resultaten die u ziet. Zie de [voorbeelden](#examples) verderop in dit onderwerp voor meer informatie over de manier waarop dit gedrag van invloed kan zijn op de resultaten.

Voer de volgende stappen uit om de selectie van voorraaddimensies aan te passen die worden weergegeven.

1. Selecteer in het actievenster de optie **Dimensies**.

    Het dialoogvenster **Weergave van dimensies** dat wordt weergegeven, bevat alle dimensies.

2. Schakel het selectievakje in van elke dimensie die u in het raster wilt opnemen.
3. Als u wilt dat de selectie standaard wordt gebruikt wanneer u de pagina **Voorhanden voorraad** de volgende keer opent, stelt u de optie **Instellingen opslaan** in op **Ja**. Als u deze optie op **Nee** instelt, wordt de selectie alleen tijdens de huidige sessie gebruikt. De volgende keer dat u de pagina opent, wordt de huidige standaardselectie gebruikt.
4. Selecteer **OK** om de wijzigingen toe te passen en het dialoogvenster te sluiten.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Filteren op de uitvoer van de voorhanden voorraad

U kunt in het raster **Voorhanden** een kolomkop selecteren om te sorteren of filteren op waarden in die kolom. Een snelfilter boven aan het raster bevat extra filteropties. Deze filters zijn van toepassing op de resultaten, niet op de brontabellen. Zie de [voorbeelden](#examples) verderop in dit onderwerp voor meer informatie over de manier waarop dit gedrag van invloed kan zijn op de resultaten.

> [!NOTE]
> U kunt niet op alle kolommen filteren en sorteren. De meeste kolommen met hoeveelheden bevatten geen sorteer- en filterbesturingselementen, omdat dit berekende velden zijn. De kolom **In bestelling** is een uitzondering.

## <a name="examples"></a><a name="examples"></a>Voorbeelden

Uw systeem bevat een gedetailleerde (niet-samengevoegde) voorraadtabel waarin de volgende voorhanden voorraad wordt weergegeven.

| Artikelnummer | Locatie | Magazijn | Fysieke voorraad | Fysiek beschikbaar |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>Scenario 1

De pagina **Voorhanden voorraad** wordt ingesteld om de volgende einddimensies weer te geven:

- artikelnummer
- Locatie
- Magazijn

In het deelvenster **Filters** worden de volgende filtercriteria ingesteld:

- **Artikelnummer** \| **is exact** \| _IA0001_
- **Fysiek beschikbaar** \| **kleiner dan of gelijk aan** \| _1_

Dit is de resulterende uitvoer.

| Artikelnummer | Locatie | Magazijn | Fysieke voorraad | Fysiek beschikbaar |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>Scenario 2

De pagina **Voorhanden voorraad** wordt ingesteld om de volgende einddimensies weer te geven:

- artikelnummer
- Locatie

In het deelvenster **Filters** worden de volgende filtercriteria ingesteld:

- **Artikelnummer** \| **is exact** \| _IA0001_
- **Fysiek beschikbaar** \| **kleiner dan of gelijk aan** \| _1_

Dit is de resulterende uitvoer.

| Artikelnummer | Locatie | Fysieke voorraad | Fysiek beschikbaar |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

De instellingen in het deelvenster **Filters** zijn van toepassing op de gedetailleerde (niet-samengevoegde) voorraadtabel die aan het begin van deze sectie wordt weergegeven. Daarom vindt het criterium **Fysiek beschikbaar** \| **kleiner dan of gelijk aan** \| _1_ twee rijen uit die tabel (de eerste en de derde rij, die elk een waarde **Fysiek beschikbaar** van _1_ hebben). In dit scenario wordt de lijst **Voorhanden voorraad** echter niet ingesteld om de dimensie **Magazijn** weer te geven. Daarom worden de twee oorspronkelijke rijen samengevoegd tot één enkele resulterende rij, omdat beide rijen identieke waarden bevatten in alle dimensies die worden weergegeven. Deze rij lijkt het filtercriterium te schenden, omdat de waarde **Fysiek beschikbaar** wordt weergegeven als _2_. Het resultaat is echter correct, omdat de instellingen in het deelvenster **Filters** van toepassing zijn op de brontabel, niet op de samengevoegde tabel die wordt weergegeven op de pagina **Voorhanden voorraad**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]