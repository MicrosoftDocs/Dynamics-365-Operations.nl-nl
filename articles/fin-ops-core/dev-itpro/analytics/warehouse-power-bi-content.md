---
title: Power BI-inhoud Magazijnprestaties
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud voor magazijnprestaties. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: Mirzaab
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4594c6c09abdac72a03ac1338701d2291b234106
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687396"
---
# <a name="warehouse-performance-power-bi-content"></a>Power BI-inhoud Magazijnprestaties

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de **Magazijnprestaties** Power BI-inhoud. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Magazijnprestaties** is gemaakt zodat magazijnbeheerder en operations managers belangrijke inkomende en uitgaande metrische gegevens en voorraadgegevens kunnen controleren. Er wordt gebruikgemaakt van magazijnbeheer-, product- en andere transactionele gegevens uit uw systeem en er wordt zowel een samengevoegde weergave van magazijnprestaties als een onderverdeling voor leveranciers, productgroepen en producten, en locaties en magazijnen geboden.

Magazijnbeheerders kunnen gebruikmaken van de Power BI-inhoud **Magazijnprestaties** om de volgende drie gebieden te meten:

- **Inkomende prestatie**: hierbij wordt gemeten hoe goed een leverancier presteert ten opzicht van vereisten van de klant (dat wil zeggen, leveringsprestaties) als ook wegzetprestaties, zodat u problemen met betrekking tot werknemers of artikelen gedurende een periode kunt identificeren. Het is belangrijk dat u weet of leveranciers op tijd, vroeg of laat leveren, zodat u kunt bepalen hoe de leveranciersprestaties de algehele wegzetprestaties beïnvloeden. Wanneer een leverancier buiten de overeengekomen datums levert, kan dit voor extra druk in het magazijn zorgen vanwege onverwacht werk en kan de gemiddelde wegzettijd toenemen.
- **Verzendprestaties**: hierbij wordt gemeten of het magazijn volledig en op tijd levert aan klanten (met andere woorden meting van de prestaties bij uitgaande verzending en levering), zodat u eventuele problemen met betrekking tot producten, locaties of magazijnen of specifieke klanten kunt identificeren. Als u vaststelt dat u te laat levert aan specifieke gebieden of steden, moet u wellicht meer aandacht besteden aan vervoer of accountmanagement.
- **Voorraadnauwkeurigheid per locatie**: de voorraadnauwkeurigheid is belangrijke interne bedrijfsinformatie (BI) voor magazijnen. Het is erg belangrijk dat u bepaalt hoe nauwkeurig u in het algemeen bent bij het tellen. Het is echter ook belangrijk dat u bepaalt hoe nauwkeurig u bent bij het opslaan van artikelen op de juiste locaties en of dat u afwijkingsgegevens markeert, zodat u betere posities voor artikelen kunt vinden of de totale telling van specifieke artikelen kunt starten. (Momenteel wordt de nieuwe artikelgebaseerde telfunctie geleverd als hotfix.) Als u deze Power BI-inhoud gebruikt om de juistheid van gegevens van de voorhanden voorraad per locatie te bepalen, kunt u ook diefstal identificeren in uw winkels. U kunt ook bepalen of bepaalde locaties voorhanden hoeveelheden hebben die verschillen van ERP-gegevens (Enterprise Resource Planning). Deze locaties zijn mogelijk te groot of zijn onmogelijk om te tellen. Ook is mogelijk in sommige gevallen de fysieke plaatsing slecht, zodat het moeilijk is één type artikel synchroon te houden met de gegevens over voorhanden voorraad.

## <a name="accessing-the-power-bi-content-pack"></a>Toegang tot het Power BI-inhoudpakket
De Power BI-inhoud **Magazijnprestaties** wordt weergegeven op de pagina **Magazijnprestaties** (**Magazijnbeheer** \> **Query's en rapporten** \> **Magazijnprestatieanalyse** \> **Magazijnprestaties**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
De Power BI-inhoud **Magazijnprestaties** bevat een rapport. Dit rapport bestaat uit een set metrische gegevens die worden gevisualiseerd als diagrammen, tegels en tabellen. De volgende tabel bevat een overzicht van de visualisaties in de Power BI-inhoud **Magazijnprestaties**.

| Rapportpagina                 | Diagrammen                                   | Omschrijving |
|-----------------------------|------------------------------------------|-------------|
| Inkomende prestatie         | Totale wegzettingen                          | Het aantal werkregels voor wegzetten dat wordt verwerkt gedurende een bepaalde tijd. |
| Inkomende prestatie         | Gemiddelde tijd voor wegzetten                    | De gemiddelde tijd in uren, voor alle wegzetregels voor inkooporders die zijn verwerkt, van registratie van de artikelen totdat de laatste opslag is verwerkt. |
| Inkomende prestatie         | Vroeg ontvangen                           | Het aantal inkooporderregels dat vroegtijdig is ontvangen. |
| Inkomende prestatie         | Op tijd ontvangen                         | Het aantal inkooporderregels dat op tijd is ontvangen. |
| Inkomende prestatie         | Te laat ontvangen                            | Het aantal inkooporderregels dat te laat is ontvangen. |
| Inkomende prestatie         | Op tijd per leverancier                        | Een weergave van het percentage inkooporderregels dat te vroeg, op tijd of en te laat is ontvangen van een leverancier of leveranciersgroep. |
| Inkomende prestatie         | Gemiddelde wegzettijd van dock tot voorraad (uren) | De gemiddelde wegzettijd van dock tot voorraad in uren na verloop van tijd. |
| Inkomende prestatie         | Gemiddelde wegzethoeveelheid per werknemer               | De gemiddelde tijd in uren, die een werknemer nodig heeft gehad voor de verwerking van het wegzetten van inkooporderregels. |
| Inkomende prestatie         | Gemiddelde uren wegzettijd per leverancier          | De gemiddelde wegzettijd in uren per leverancier of leveranciersgroep. |
| Inkomende prestatie         | Gemiddelde uren wegzettijd per product         | De gemiddelde wegzettijd in uren per artikel of artikelgroep. |
| Voorraadnauwkeurigheid per locatie | Totaaltelling                              | Het aantal telregels dat wordt verwerkt gedurende een bepaalde periode. |
| Voorraadnauwkeurigheid per locatie | Verschilpercentage                         | Het totale verschil als percentage van alle regels die zijn geteld voor een bepaalde periode. |
| Voorraadnauwkeurigheid per locatie | Telling zonder verschil                | Van het totale aantal telregels dat is verwerkt, het aantal regels dat is verwerkt zonder verschillen. |
| Voorraadnauwkeurigheid per locatie | Artikelen die zijn geteld na verloop van tijd                  | Het percentage van de artikelen die zijn geteld met en zonder verschillen na verloop van tijd. |
| Voorraadnauwkeurigheid per locatie | Verschil in artikelhoeveelheid groter dan % | Een tabelweergave van de telregels die verschillen bevat die een opgegeven percentage overschrijden. De tabel bevat informatie over locaties, artikelen, gemiddeld verschil, totaal aantal telregels dat is geteld, aantal telregels met verschillen voor de vestiging, gemiddelde hoeveelheid die is geteld, verwachte totale hoeveelheid die moet worden geteld en werkelijke artikelhoeveelheid die is geteld. |
| Voorraadnauwkeurigheid per locatie | Aantal artikelen per medewerker                     | De telprestaties van medewerkers. De prestaties worden uitgedrukt als percentage van het aantal telregels met en zonder verschillen. |
| Voorraadnauwkeurigheid per locatie | Artikeltelling per locatie/magazijn           | Telprestaties bij het aantal verwerkte telregels per locatie of magazijn, waar wel of niet verschillen bestaan. |
| Voorraadnauwkeurigheid per locatie | Verschilpercentage per product              | Het verschilpercentage voor de telprestaties. Dit is het percentage telregels per artikel of artikelengroep. |
| Verzendprestaties        | Verzonden regels                            | Het aantal zendingsregels dat is verzonden gedurende een bepaalde periode. |
| Verzendprestaties        | Te vroeg                                    | Het percentage zendingsregels die te vroeg zijn verzonden. |
| Verzendprestaties        | Op tijd                                  | Het percentage zendingsregels die op tijd zijn verzonden. |
| Verzendprestaties        | Te laat                                     | Het percentage zendingsregels die te laat zijn verzonden. |
| Verzendprestaties        | Zendingen na verloop van tijd                      | Het percentage van zendingsregels die te vroeg, op tijd of te laat worden verzonden gedurende een bepaalde periode. Een trendlijn toont de trend voor regels die op tijd worden verzonden. |
| Verzendprestaties        | Te laat verzonden per plaats                     | Een kaartvisualisatie van steden en gebieden waarbij sprake is van te late zendingen. |
| Verzendprestaties        | Verzonden per product                       | Het percentage dat te vroeg, op tijd of te laat is verzonden per artikel of artikelgroep. |
| Verzendprestaties        | Verzonden per klant                      | Het percentage dat te vroeg, op tijd of te laat is verzonden per klant of klantgroep. |
| Verzendprestaties        | Verzonden per locatie/magazijn              | Het percentage dat te vroeg, op tijd of te laat is verzonden per locatie of magazijn. |

## <a name="understanding-the-data-model-and-calculations"></a>Het gegevensmodel en de berekeningen begrijpen
De volgende gegevens wordt gebruikt om de rapportpagina's in de Power BI-inhoud **Magazijnprestaties** te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

De volgende belangrijke samengevoegde metingen worden gebruikt als de basis van de inhoud.

| Rapportpagina                 | Diagrammen                                   | Tabellen                                | Beschrijvingen van berekeningen |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Inkomende prestatie         | Totale wegzettingen                          | WHSWorkLine                           | Het aantal werkregels waarin het type werk **wegzetten** is. |
| Inkomende prestatie         | Gemiddelde tijd voor wegzetten                    | WHSWorkLine                           | De som van de maximale tijd voor werkregels gedeeld door de totale maximale tijd voor werkregels is de maximaal toegestane ruimte tussen de datum waarop de werkzaamheden zijn gemaakt en de sluitingsdatum. |
| Inkomende prestatie         | Vroeg ontvangen                           | WHSWorkLine                           | Het aantal werkregels waarbij de datum waarop de werkzaamheden zijn gemaakt vóór de gebruikte leveringsdatum valt. Als de datum voor leveringsbevestiging niet is ingesteld, gebruikt u de standaard leverdatum. |
| Inkomende prestatie         | Op tijd ontvangen                         | WHSWorkLine                           | Het aantal werkregels waarbij de datum waarop de werkzaamheden zijn gemaakt gelijk is aan de gebruikte leveringsdatum. Als de datum voor leveringsbevestiging niet is ingesteld, gebruikt u de standaard leverdatum. |
| Inkomende prestatie         | Te laat ontvangen                            | WHSWorkLine                           | Het aantal werkregels waarbij de datum waarop de werkzaamheden zijn gemaakt na de gebruikte leveringsdatum valt. Als de datum voor leveringsbevestiging niet is ingesteld, gebruikt u de standaard leverdatum. |
| Inkomende prestatie         | Op tijd per leverancier                        | WHSWorkLine                           | Vroeg ontvangen, Op tijd ontvangen en Laat ontvangen (zie de beschrijvingen eerder in deze tabel). |
| Inkomende prestatie         | Gemiddelde wegzettijd van dock tot voorraad (uren)   | WHSWorkLine                           | Gemiddelde wegzettijd (zie de beschrijving eerder in deze tabel). |
| Inkomende prestatie         | Gemiddelde wegzethoeveelheid per werknemer               | WHSWorkLine                           | Gemiddelde wegzettijd (zie de beschrijving eerder in deze tabel). |
| Inkomende prestatie         | Gemiddelde uren wegzettijd per leverancier          | WHSWorkLine                           | Gemiddelde wegzettijd (zie de beschrijving eerder in deze tabel). |
| Inkomende prestatie         | Gemiddelde uren wegzettijd per product         | WHSWorkLine                           | Gemiddelde wegzettijd (zie de beschrijving eerder in deze tabel). |
| Voorraadnauwkeurigheid per locatie | Totaaltelling                              | WHSWorkLineCycleCount                 | Cyclustellingen waarbij de absolute verschilhoeveelheid gelijk is aan of groter is dan 0 (nul). |
| Voorraadnauwkeurigheid per locatie | Verschilpercentage                         | WHSWorkLineCycleCount                 | Cyclustellingen met afwijkingen, gedeeld door het totale aantal. Een cyclustelling wordt geacht verschillen te bevatten als de absolute hoeveelheid van het verschil groter is dan 0 (nul). |
| Voorraadnauwkeurigheid per locatie | Telling zonder verschil                | WHSWorkLineCycleCount                 | Cyclustellingen waarbij de absolute verschilhoeveelheid groter is dan 0 (nul). |
| Voorraadnauwkeurigheid per locatie | Telling met verschil                   | WHSWorkLineCycleCount                 | Cyclustellingen waarbij de absolute verschilhoeveelheid gelijk is aan 0 (nul). |
| Voorraadnauwkeurigheid per locatie | Artikelen die zijn geteld na verloop van tijd                  | WHSWorkLineCycleCount                 | Telling zonder verschil en aantal met verschil (Zie de omschrijvingen eerder in deze tabel.) |
| Voorraadnauwkeurigheid per locatie | Verschil in artikelhoeveelheid groter dan % | WHSWorkLineCycleCount                 | Het gemiddelde verschil is het absolute verschilhoeveelheid gedeeld door de verwachte hoeveelheid waarbij de hoeveelheid van het absolute verschil groter is dan 0 (nul). De gemiddelde verschilhoeveelheid is de gemiddelde absolute verschilhoeveelheid waarbij de absolute verschilhoeveelheid groter is dan 0 (nul). Aantal met verschil, totaal aantal, verwachte hoeveelheid en getelde hoeveelheid waarbij de volledige hoeveelheid is gegroepeerd per artikel en locatie (zie de beschrijvingen eerder in deze tabel). |
| Voorraadnauwkeurigheid per locatie | Aantal artikelen per medewerker                     | WHSWorkLineCycleCount                 | Telling zonder verschil en aantal met verschil (zie de beschrijvingen eerder in deze tabel). |
| Voorraadnauwkeurigheid per locatie | Artikeltelling per locatie/magazijn           | WHSWorkLineCycleCount                 | Telling zonder verschil en aantal met verschil (zie de beschrijvingen eerder in deze tabel). |
| Voorraadnauwkeurigheid per locatie | Verschilpercentage per product              | WHSWorkLineCycleCount                 | Verschilpercentage (zie de beschrijving die eerder in deze tabel). |
| Verzendprestaties        | Verzonden regels                            | VerkoopRegel               | Het aantal verkoopregels waarbij verkoopregels worden verzonden. |
| Verzendprestaties        | Te vroeg                                    | CustPackingSlipOnTimeStatus           | Verkoopregels waarbij de status van de verzenddatum **1 (Vroeg)** is. Vroeg betekent dat de verzenddatum van de pakbon vóór de bevestigde verzenddatum van de verkoopregel valt. Als de bevestigde verzenddatum niet is ingesteld, gebruikt u de gewenste verzenddatum |
| Verzendprestaties        | Op tijd                                  | CustPackingSlipOnTimeStatus           | Verkoopregels waarbij de status van de verzenddatum **2 (Op tijd)** is. Op tijd betekent dat de verzenddatum van de pakbon gelijk is aan de bevestigde verzenddatum van de verkoopregel. Als de bevestigde verzenddatum niet is ingesteld, gebruikt u de gewenste verzenddatum |
| Verzendprestaties        | Te laat                                     | CustPackingSlipOnTimeStatus           | Verkoopregels waarbij de status van de verzenddatum **3 (Laat)** is. Laat betekent dat de verzenddatum van de pakbon na de bevestigde verzenddatum van de verkoopregel valt. Als de bevestigde verzenddatum niet is ingesteld, gebruikt u de gewenste verzenddatum |
| Verzendprestaties        | Zendingen na verloop van tijd                      | SalesLine CustPackingSlipOnTimeStatus | Orders die volledig zijn verzonden, waarbij de gehele hoeveelheid van de verkoopregel is verzonden, plus Vroeg, Op tijd en Laat (zie de omschrijvingen eerder in deze tabel). |
| Verzendprestaties        | Te laat verzonden per plaats                     | CustPackingSlipOnTimeStatus           | Laat (zie de beschrijvingen eerder in deze tabel). |
| Verzendprestaties        | Verzonden per product                       | CustPackingSlipOnTimeStatus           | Vroeg, Op tijd en Laat (zie de beschrijvingen eerder in deze tabel). |
| Verzendprestaties        | Verzonden per klant                      | CustPackingSlipOnTimeStatus           | Vroeg, Op tijd en Laat (zie de beschrijvingen eerder in deze tabel). |
| Verzendprestaties        | Verzonden per locatie/magazijn              | CustPackingSlipOnTimeStatus           | Vroeg, Op tijd en Laat (zie de beschrijvingen eerder in deze tabel). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]