---
title: Query's voor francoprijzen
description: In dit onderwerp wordt beschreven hoe u de verschillende typen query's kunt opzoeken en gebruiken die beschikbaar zijn voor de module Francoprijzen.
author: Weijiesa
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8a1ec063f10634de92b1e7500d4dda111e879b62
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693411"
---
# <a name="landed-cost-inquiries"></a>Query's voor francoprijzen

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Query's voor reisregels

Met de query **Reisregels** worden alle reisregels weergegeven die betrekking hebben op de voorraad. Deze query kan worden gebruikt als filter om u te helpen een artikel, inkooporder of andere nuttige informatie te vinden. De query kan ook worden gebruikt om de verwachte leveringsdatum te bepalen van een artikel dat zich in een of meer reizen bevindt. Op deze manier kunt u de verwachte ontvangst van de voorraad beheren.

Als u deze query wilt openen, gaat u naar **Francoprijzen \> Query's \> Reisregels**.

### <a name="overview-tab"></a>Tabblad Overzicht

Het tabblad **Overzicht** van de querypagina **Reisregels** bevat een raster met basisinformatie over elke relevante reisregel. In de volgende tabel worden de kolommen in het raster beschreven.

| Kolom | Beschrijving |
|---|---|
| **Artikelnummer** | Het artikel voor de reisregel. |
| **Verwijzing** | Het type order (inkooporder of overboekingsorder). |
| **Nummer** | Het nummer van de inkooporder of overboekingsorder. |
| **Folio** | De folio die aan de reisregel is gekoppeld. |
| **Container** | De container die aan de reisregel is gekoppeld. |
| **Reis** | De reis die aan de reisregel is gekoppeld. |
| **Hoeveelheid** | De hoeveelheid van het artikel voor de reisregel. |
| (Overige dimensies) | U kunt indien nodig kolommen voor extra dimensies weergeven. Deze dimensies zijn batchnummer, voorraadstatus en magazijn. Selecteer in het actievenster de optie **Voorraad \> Dimensies weergeven** om een dialoogvenster te openen waarin u de dimensies kunt selecteren die u wilt opnemen. |

### <a name="general-tab"></a>Tabblad Algemeen

Selecteer het tabblad **Algemeen** om meer informatie weer te geven over de regel die momenteel op het tabblad **Overzicht** is geselecteerd.

### <a name="dimensions-tab"></a>Tabblad Dimensies

Selecteer het tabblad **Dimensies** om waarden weer te geven voor alle beschikbare dimensies voor de regel die momenteel is geselecteerd op het tabblad **Overzicht**, ongeacht of de dimensies die u hebt geselecteerd om op dat tabblad weer te geven.

## <a name="cost-estimate-inquiries"></a>Query's voor kostenramingen

Telkens wanneer u een kostenraming genereert, wordt de raming toegevoegd aan de querypagina **Geraamde kosten**. Zie [Francoprijzen ramen en beheren](estimate-manage-landed-costs.md) voor de volledige details over het genereren, weergeven en werken met kostenramingen (inclusief ramingen op de querypagina).

## <a name="item-tracking"></a>Artikeltracering

Gebruik de pagina **Artikeltracering** om openstaande inkooporderregels en de huidige status van de regels weer te geven. Regels hoeven niet aan een reis te zijn gekoppeld om hier te worden weergegeven. Als een artikel echter aan een reis is gekoppeld, wordt bij de recordregel van de artikeltracering de reis-id weergegeven.

U opent deze pagina door naar **Francoprijzen \> Query's \> Tracering \> Artikeltracering** te gaan.

Omdat het systeem waarschijnlijk een zeer groot aantal inkooporderregels bevat, worden op de pagina **Artikeltracering** in eerste instantie geen records weergegeven. Gebruik de filtervelden boven aan de pagina om de set inkooporderregels te definiëren die u zoekt. Selecteer vervolgens **Bijwerken** in het actievenster om de lijst te genereren. U kunt in de filtervelden een sterretje (\*) als jokerteken gebruiken. Als u bijvoorbeeld alle inkooporderregels wilt vinden voor artikelen die het woord 'dvd' bevatten in de naam, stelt u het veld **Type** in op **Productnaam** en voert u *\*dvd\** in het veld **Veldwaarde** in.

> [!NOTE]
> Momenteel bevatten naleveringen alleen verkooporders. Verkoopoffertes worden niet weergegeven of worden beschouwd als naleveringen.

In de volgende tabel worden de kolommen in het raster op de pagina **Artikeltracering** beschreven.

| Kolom | Beschrijving |
|---|---|
| **Aankomsthaven** | De eindbestemming. |
| **Bevestigd** | De bevestigde datum van de inkooporderregel. |
| **Leveringsdatum** | De leveringsdatum van de inkooporderregel. |
| **Reis** | Als de regel is gekoppeld aan een reis, de reis-id. |
| **Container** | Als de regel is gekoppeld aan een container, de container-id. |
| **Haven** | De huidige haven, op basis van de eerste etappe in het traceringsformulier, waar geen werkelijke datum is ingesteld voor de container die aan de inkooporderregel is gekoppeld. |
| **Activiteit** | De huidige activiteit, op basis van de eerste etappe in het traceringsformulier, waar geen werkelijke datum is ingesteld voor de container die aan de inkooporderregel is gekoppeld. |
| **Geraamde einddatum** | De datum waarop de reis naar verwachting in het doelmagazijn wordt ontvangen. |
| **Naam** | De naam van de leverancier. |
| **Reisstatus** | De verzendstatus die aan de inkooporderregel is gekoppeld. |
| **Artikelnummer** | Het artikelnummer voor de inkooporderregel. |
| **Extern** | De naam van het artikel van de leverancier. |
| **Productnaam** | De naam van het artikel voor de inkooporderregel. |
| **Hoeveelheid** | De hoeveelheid van de inkooporderregel voor de inkooporderregel. |
| **Eenheid** | De maateenheid voor de inkooporderregel. |
| **Verwijzing** | Het type order (inkooporder of overboekingsorder) |
| **Verwijzingsnummer** | Het nummer van de inkooporder of overboekingsorder. |
| **Nalevering** | Een symbool geeft aan dat er naleveringen van verkooporders zijn voor het artikel. |
| (Overige dimensies) | U kunt indien nodig kolommen voor extra dimensies weergeven. Deze dimensies zijn batchnummer, voorraadstatus en magazijn. Selecteer in het actievenster **Dimensies weergeven** om een dialoogvenster te openen waarin u de dimensies kunt selecteren die u wilt opnemen. |

### <a name="related-information-about-backorders"></a>Verwante informatie over naleveringen

Als u meer informatie over naleveringen wilt weergeven, selecteert u het tabblad **Verwante informatie** aan de rechterkant van de pagina en selecteert u **Naleveringen**. Als u nog meer informatie over een bepaalde nalevering wilt weergeven, selecteert u de rij voor de nalevering en selecteert u vervolgens de koppeling **Meer**.

## <a name="individual-shipping-container-tracking"></a>Tracering van individuele containers

Met de query **Afzonderlijke containers traceren** beschikt u over een filter waarmee u naar een container kunt zoeken en vervolgens alle reisregels in die container kunt identificeren.

U opent deze query door naar **Francoprijzen \> Query's \> Tracering \> Afzonderlijke containers traceren** te gaan.

## <a name="multiple-shipping-container-tracking"></a>Tracering van meerdere containers

Met de query **Meerdere containers traceren** beschikt u over een filter waarmee u naar meerdere container kunt zoeken en vervolgens alle reisregels in die containers kunt identificeren.

U opent deze query door naar **Francoprijzen \> Query's \> Tracering \> Meerdere containers traceren** te gaan.
