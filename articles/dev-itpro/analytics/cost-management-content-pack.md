---
title: Power BI-inhoud voor kostenbeheer
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud voor kostenbeheer.
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: caf1c13d48d1f8af5c88927ccb23118e99cb38e0
ms.contentlocale: nl-nl
ms.lasthandoff: 08/13/2018

---

# <a name="cost-management-power-bi-content"></a>Power BI-inhoud voor kostenbeheer

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overzicht

De Microsoft Power BI-inhoud van **Kostenbeheer** is bedoeld voor voorraadboekhouders of personen in de organisatie die verantwoordelijk zijn voor of belang hebben bij de status van de voorraad of onderhanden werk (OHW), of die verantwoordelijk zijn voor of belang hebben bij het analyseren van afwijkingen voor standaardkosten.

> [!NOTE]
> De Power BI-inhoud voor **Kostenbeheer** die wordt beschreven in dit onderwerp, geldt voor Dynamics 365 voor Finance and Operations 8.0.
> 
> Het Power BI-inhoudpakket voor **Kostenbeheer** dat beschikbaar is gepubliceerd op de site AppSource, is afgeschaft. Zie voor meer informatie hierover [Power BI-inhoudpakketten beschikbaar op AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Deze Power BI-inhoud biedt een gecategoriseerde indeling waarmee u de prestaties van voorraden kunt controleren en kunt visualiseren hoe kostenstromen verlopen. U vindt de beheerinzichten zoals omloopsnelheid, aantal dagen dat de voorraad voorhanden is, nauwkeurigheid en 'ABC-classificatie' op het gewenste totalliseringsniveau (bedrijf, artikel, artikelgroep of locatie). De beschikbare informatie kan ook worden gebruikt als een uitgebreide aanvulling op het financiële overzicht.

De Power BI-inhoud is gebaseerd op de samengevoegde meting **CostObjectStatementCacheMonthly**, waarvoor de tabel **CostObjectStatementCache** de primaire gegevensbron is. Deze tabel wordt beheerd door het raamwerk van de gegevenssetcache. De tabel wordt elke 24 uur standaard bijgewerkt, maar u kunt de updatefrequentie wijzigen of handmatige updates inschakelen in de configuratie van de gegevenssetcache. Handmatige updates kunnen worden uitgevoerd in het werkgebied **Kostenadministratie** of **Kostenanalyse**.

Na elke update van de tabel **CostObjectStatementCache**, moet de samengevoegde meting **CostObjectStatementCacheMonthly** worden bijgewerkt voordat de gegevens in de Power BI-visualisaties worden bijgewerkt.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen

De Power BI-inhoud voor **Kostenbeheer** wordt weergegeven in de werkgebieden **Kostenadministratie** en **Kostenanalyse**.

Het werkgebied **Kostenadministratie** bevat de volgende tabbladen:

- **Overzicht**: hier worden toepassingsgegevens weergegeven.
- **Status voorraadboekhouding**: dit tabblad geeft de Power BI-inhoud weer.
- **Status productieboekhouding**: dit tabblad geeft de Power BI-inhoud weer.

Het werkgebied **Kostenanalyse** bevat de volgende tabbladen:

- **Overzicht**: hier worden toepassingsgegevens weergegeven.
- **Analyse voorraadboekhouding**: dit tabblad geeft de Power BI-inhoud weer.
- **Analyse productieboekhouding**: dit tabblad geeft de Power BI-inhoud weer.
- **Analyse van standaardkostprijsvariantie**: dit tabblad geeft de Power BI-inhoud weer.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Rapportpagina's die zijn opgenomen in de Power BI-inhoud

De Power BI-inhoud voor **Kostenbeheer** bevat een set met rapportpagina's die uit een verzameling van metrische gegevens bestaan. Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen. 

De volgende tabellen bevatten een overzicht van de visualisaties in de Power BI-inhoud voor **Kostenbeheer**.

### <a name="inventory-accounting-status"></a>Status voorraadboekhouding

| Rapportpagina                               | Visualisatie                                   |
|-------------------------------------------|-------------------------------------------------|
| Voorraad - Overzicht                        | Beginsaldo                               |
|                                           | Nettowijziging                                      |
|                                           | Nettowijziging %                                    |
|                                           | Eindsaldo                                  |
|                                           | Voorraadnauwkeurigheid                              |
|                                           | Voorraadomloopsnelheid                        |
|                                           | Dagen voorraad voorhanden                          |
|                                           | Actief product in periode                        |
|                                           | Actieve kostenobjecten in periode                   |
|                                           | Saldo per artikelengroep                           |
|                                           | Saldo per locatie                                 |
|                                           | Overzicht per categorie                           |
|                                           | Nettowijziging per kwartaal                           |
| Voorraadoverzicht per locatie en artikelgroep | Voorraadnauwkeurigheid per locatie                      |
|                                           | Voorraadomloopsnelheid per locatie                |
|                                           | Eindsaldo voorraad per locatie                |
|                                           | Voorraadnauwkeurigheid per artikelgroep                |
|                                           | Voorraadomloopsnelheid per artikelgroep          |
|                                           | Eindsaldo voorraad per locatie en artikelgroep |
| Voorraadafschrift                       | Voorraadafschrift                             |
| Voorraadoverzicht per locatie               | Voorraadoverzicht per locatie                     |
| Voorraadoverzicht per producthiërarchie  | Voorraadafschrift                             |
| Voorraadoverzicht per producthiërarchie  | Voorraadoverzicht per locatie                     |

### <a name="manufacturing-accounting-status"></a>Status productieboekhouding

| Rapportpagina                | Visualisatie                       |
|----------------------------|-------------------------------------|
| Overzicht OHW JTD           | Beginsaldo                   |
|                            | Nettowijziging                          |
|                            | Nettowijziging %                        |
|                            | Eindsaldo                      |
|                            | Omloopsnelheid OHW                  |
|                            | Dagen OHW in voorraad                    |
|                            | Actief kostenobject in periode        |
|                            | Nettowijziging per resourcegroep        |
|                            | Saldo per locatie                     |
|                            | Overzicht per categorie               |
|                            | Nettowijziging per kwartaal               |
| OHW-overzicht              | Beginsaldo                   |
|                            | Eindsaldo                      |
|                            | Overzicht OHW per categorie           |
| Overzicht OHW per locatie      | Beginsaldo                   |
|                            | Eindsaldo                      |
|                            | Overzicht OHW per categorie en locatie  |
| Overzicht OHW per hiërarchie | Beginsaldo                   |
|                            | Eindsaldo                      |
|                            | Overzicht OHW per categoriehiërarchie |

### <a name="inventory-accounting-analysis"></a>Analyse voorraadboekhouding

| Rapportpagina        | Visualisatie                                                                |
|--------------------|------------------------------------------------------------------------------|
| Voorraaddetails  | Top 10 resources per eindsaldo                                           |
|                    | Top 10 resources op toename nettowijziging                                      |
|                    | Top 10 resources op afname nettowijziging                                      |
|                    | Top 10 resources op voorraadomloopsnelheid                                 |
|                    | Resources op lage voorraadomloopsnelheid en eindsaldo boven drempelwaarde |
|                    | Top 10 resources op lage nauwkeurigheid                                             |
| ABC-classificatie | Eindsaldo voorraad                                                     |
|                    | Verbruikte materialen                                                            |
|                    | Verkocht (COGS)                                                                  |
| Voorraadtrends   | Eindsaldo voorraad                                                     |
|                    | Nettowijziging voorraad                                                         |
|                    | Voorraadomloopsnelheid                                                     |
|                    | Voorraadnauwkeurigheid                                                           |

### <a name="manufacturing-accounting-analysis"></a>Analyse productieboekhouding

| Rapportpagina | Visualisatie      |
|-------------|--------------------|
| OHW-trends  | Eindsaldo OHW |
|             | Nettowijziging OHW     |
|             | Omloopsnelheid OHW |

### <a name="std-cost-variance-analysis"></a>Analyse van standaardkostprijsvariantie

| Rapportpagina                             | Visualisatie                                        |
|-----------------------------------------|------------------------------------------------------|
| Inkoopsprijsafwijking (standaardkosten) JTD | Saldo ingekocht                                     |
|                                         | Inkoopsprijsafwijking                              |
|                                         | Verhouding inkoopsprijsafwijking                        |
|                                         | Afwijking per artikelengroep                               |
|                                         | Afwijking per locatie                                     |
|                                         | Inkoopprijs per kwartaal                            |
|                                         | Inkoopprijs per kwartaal en artikelgroep             |
|                                         | Top 10 resources op ongunstige inkoopprijsverhouding |
|                                         | Top 10 resources op gunstige inkoopprijsverhouding   |
| Afwijking productie (standaardkosten) JTD     | Productiekosten                                    |
|                                         | Afwijking productie                                  |
|                                         | Verhouding afwijking productie                            |
|                                         | Afwijking per artikelengroep                               |
|                                         | Afwijking per locatie                                     |
|                                         | Afwijking productie per kwartaal                       |
|                                         | Productieafwijking op kwartaal en afwijkingstype     |
|                                         | Top 10 resources op ongunstige productieafwijkingen  |
|                                         | Top 10 resources op gunstige productieafwijkingen    |

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

Gegevens uit Microsoft Dynamics 365 voor Finance and Operations wordt gebruikt voor het vullen van de rapportpagina's in de Power BI-inhoud voor **Kostenbeheer**. Deze gegevens worden vertegenwoordigd als samengevoegde metingen die worden klaargezet in de entiteitopslag. Dit is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Power BI-integratie met entiteitopslag](power-bi-integration-entity-store.md).

De belangrijkste geaggregeerde metingen van de volgende objecten worden gebruikt als basis voor de Power BI-inhoud.

| Object                          | Belangrijke samengevoegde metingen | Gegevensbron voor Finance and Operations | Veld               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Bedrag                     | CostObjectStatementCache               | Bedrag              |
| CostObjectStatementCacheMonthly | Hoeveelheid                   | CostObjectStatementCache               | Hoev.                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

De volgende tabel bevat de belangrijkste berekende afmetingen in de Power BI-inhoud.

| Maat                            | Berekening |
|------------------------------------|-------------|
| Beginsaldo                  | Beginsaldo = \[Eindsaldo\]-\[Nettowijziging\] |
| Hoeveelheid beginsaldo             | Hoeveelheid beginsaldo = \[Hoeveelheid eindsaldo\]-\[Hoeveelheid nettowijziging\] |
| Eindsaldo                     | Eindsaldo = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Hoeveelheid eindsaldo                | Hoeveelheid eindsaldo = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Nettowijziging                         | Nettowijziging = SUM(\[AMOUNT\]) |
| Hoeveelheid nettowijziging                    | Hoeveelheid nettowijziging = SUM(\[QTY\]) |
| Voorraadomloopsnelheid per bedrag | Voorraadomloopsnelheid per bedrag = if(OR(\[Gemiddeld voorraadsaldo\] \<= 0, \[Verkochte of verbruikte voorraaduitgiften\] \>= 0), 0, ABS(\[Verkochte of verbruikte voorraaduitgiften\])/\[Gemiddeld voorraadsaldo\]) |
| Gemiddeld saldo voorraad          | Gemiddeld voorraadsaldo = ((\[eindsaldo\] + \[beginsaldo\]) / 2) |
| Dagen voorraad voorhanden             | Dagen voorraad voorhanden 365 = / CostObjectStatementEntries\[Voorraadomloopsnelheid per bedrag\] |
| Voorraadnauwkeurigheid                 | Voorraadomloopsnelheid per bedrag = IF(\[Eindsaldo\] \<= 0, IF(OR(\[Geteld bedrag voorraad\] \<\> 0, \[Eindsaldo\] \< 0), 0, 1), MAX(0, (\[Eindsaldo\] - ABS(\[Geteld bedrag voorraad\]))/\[Eindsaldo\])) |

De volgende belangrijke dimensies worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.


| Entiteit                                                  | Voorbeelden van kenmerken                          |
|---------------------------------------------------------|-------------------------------------------------|
| Producten                                                | Productnummer, Productnaam, Eenheid, Artikelengroepen |
| Categoriehiërarchieën (toegewezen aan de rol Kostenbeheer) | Categoriehiërarchie, Categorieniveau              |
| Rechtspersonen                                          | Namen rechtspersonen                              |
| Fiscale kalenders                                        | Fiscale kalender, jaar, kwartaal, periode, maand   |
| Site                                                    | Id, naam, adres, provincie/staat, land               |

