---
title: Power BI-inhoud voor kostenbeheer
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud voor kostenbeheer. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 50889ffbbbc44d966081d60e5d631bd17476b6df
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="cost-management-power-bi-content"></a>Power BI-inhoud voor kostenbeheer

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud voor kostenbeheer. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

# <a name="overview"></a>Overzicht

De Microsoft Power BI-inhoud voor **Kostenbeheer** is bedoeld voor accountants van de voorraad of personen in de organisatie die verantwoordelijk zijn voor de voorraad. De Power BI-inhoud voor **Kostenbeheer** biedt het management inzicht in de voorraad en OHW-voorraad (onderhanden werk) en hoe de voortgang van de kosten hierin per categorie in de loop van de tijd verloopt. De informatie kan ook worden gebruikt als een uitgebreide aanvulling op het financiële overzicht.

## <a name="key-measures"></a>Belangrijke metingen

+ Beginsaldo
+ Eindsaldo
+ Nettowijziging
+ Nettowijziging in %
+ Ouderdomsrangschikking

## <a name="key-performance-indicators"></a>Key Performance Indicators
+ Voorraadomloopsnelheid
+ Voorraadnauwkeurigheid

De primaire gegevensbron voor CostAggregatedCostStatementEntryEntity is de tabel CostStatementCache. Deze tabel wordt beheerd door het raamwerk van de gegevenssetcache. De tabel wordt elke 24 uur standaard bijgewerkt, maar u kunt handmatige updates inschakelen in de gegevenscacheconfiguratie. Vervolgens kunt u een handmatige update in het werkgebied **Kostenbeheer** of **Kostenanalyse** uitvoeren. Nadat de update van CostStatementCache is uitgevoerd, kunt u de OData-verbinding op PowerBI.com bijwerken om bijgewerkte gegevens op de site te bekijken. De afwijkingsmetingen (inkoop, productie) in deze Power BI-inhoud hebben alleen betrekking op artikelen die door de standaardkostenvoorraadmethode worden gewaardeerd. Productieafwijking wordt berekend als het verschil tussen actieve kosten en gerealiseerde kosten. De afwijking van de productie wordt berekend wanneer de productieorder de status **Beëindigd** heeft. Zie voor meer informatie over de typen productieafwijking en de berekening van elk type [Info over het analyseren van afwijkingen voor een voltooide productieorder](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
De Power BI-inhoud voor **Kostenbeheer** is beschikbaar via PowerBI.com. Zie voor meer informatie over het koppelen en laden van Microsoft Dynamics 365 for Operations-gegevens [Toegang tot Power BI-inhoud via PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
De inhoud bevat een reeks rapportpagina's. Elke pagina bestaat uit een set metrische gegevens die worden gevisualiseerd als diagrammen, tegels en tabellen. De volgende tabel bevat een overzicht van de visualisaties in de Power BI-inhoud voor **Kostenbeheer**.

| Rapportpagina | Diagrammen | Titels |
|---|---|---|
|Totale voorraad (standaard per huidige periode) |Nauwkeurigheid |Voorraadmetingen:<br>Eindsaldo voorraad<br>Nettowijziging voorraad<br>Nettowijziging voorraad in %<br>|
| |Voorraadomloopsnelheid | |
| |Eindsaldo voorraad per resourcegroep | |
| |Nettowijziging van voorraad per categorienaam, niveau 1 en categorienaam, niveau 2| |
| |Inkoopafwijkingen per resourcegroep en categorienaam, niveau 3 | |
|Voorraad per site (standaard per huidige periode) |Eindsaldo voorraad per sitenaam en resourcegroep | |
| |Voorraadomloopsnelheid per sitenaam en resourcegroep | |
| |Eindsaldo voorraad per plaats en resourcegroep | |
|Voorraad per resourcegroep (standaard per huidige periode) |Voorraadmetingen | |
| |Nauwkeurigheid van voorraad per bedrag per resourcegroep | |
| |Voorraadomloopsnelheid per bedrag per resourcegroep | |
|Voorraad jaar-op-jaar (huidig jaar versus vorig jaar) |Voorraadmetingen | |
| |KPI's voor voorraad:<br>Voorraadomloopsnelheid<br>Voorraadnauwkeurigheid | |
| |Eindsaldo voorraad per jaar en resourcegroep | |
| |Inkoopafwijkingen per jaar en categorienaam, niveau 3 | |
|Voorraad naar ouderdom gerangschikt (standaard per huidig jaar) |Voorraad naar ouderdom gerangschikt per kwartaal en resourcegroep | |
| |Voorraad naar ouderdom gerangschikt per kwartaal en sitenaam | |
|Totaal OHW (standaard per huidige periode) |Nettowijziging OHW per categorienaam, niveau 1 en categorienaam, niveau 2 |OHM-metingen onderhanden werk:<br>Eindsaldo OHW<br>Nettowijziging OHW<br>Nettowijziging OHW in %<br> |
| |Productieafwijkingen per resourcegroep en categorienaam, niveau 3 | |
| |Nettowijziging OHW per resourcegroep | |
|OHW per site (standaard per huidige periode) |OHM-metingen onderhanden werk | |
| |Nettowijziging OHW per sitenaam en categorienaam, niveau 2 | |
| |Productieafwijkingen per sitenaam en categorienaam, niveau 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Dynamics 365 for Operations-gegevens worden gebruikt voor het vullen van de rapportpagina's in de Power BI-inhoud voor **Kostenbeheer**. Deze gegevens worden vertegenwoordigd als samengevoegde metingen die worden klaargezet in de Entiteitopslag. Dit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md). De volgende belangrijke samengevoegde metingen worden gebruikt als de basis van de inhoud.

| Entiteit            | Belangrijke samengevoegde meting | Gegevensbron voor Dynamics 365 for Operations | Veld             | Omschrijving                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Overzichtvermeldingen | Nettowijziging                | CostAggregatedCostStatementEntryEntity      | sum(\[Bedrag\])   | Bedrag in de boekhoudingsvaluta |
| Overzichtvermeldingen | Hoeveelheid nettowijziging       | CostAggregatedCostStatementEntryEntity      | sum(\[Hoeveelheid\]) |                                   |

In de volgende tabel ziet u hoe de belangrijkste samengevoegde metingen worden gebruikt om verschillende berekende eenheden te maken in de gegevensset van de inhoud.

| Maat                                 | Hoe de meting wordt berekend                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beginsaldo                       | \[Eindsaldo\]-\[Nettowijziging\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Hoeveelheid beginsaldo              | \[Hoeveelheid eindsaldo\]-\[Hoeveelheid nettowijziging\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Eindsaldo                          | CALCULATE(SUM(\[Bedrag\]), FILTER(ALLEXCEPT('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[Naam\], 'Grootboeken'\[Valuta\], 'Grootboeken'\[Beschrijving\], 'Grootboeken'\[Naam\]), 'Fiscale kalenders'\[Datum\] &lt;= MAX('Fiscale kalenders'\[Datum\])))                                                                                                                                                                                           |
| Hoeveelheid eindsaldo                 | CALCULATE(SUM(\[Hoeveelheid\]), FILTER(ALLEXCEPT('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[Naam\], 'Grootboeken'\[Valuta\], 'Grootboeken'\[Beschrijving\], 'Grootboeken'\[Naam\]), 'Fiscale kalenders'\[Datum\] &lt;= MAX('Fiscale kalenders'\[Datum\])))                                                                                                                                                                                         |
| Beginsaldo voorraad             | CALCULATE(\[Beginsaldo\], 'Overzichtvermeldingen'\[Overzichttype\] = "Voorraad")                                                                                                                                                                                                                                                                                                                                                                                      |
| Eindsaldo voorraad                | CALCULATE(\[Eindsaldo\], 'Overzichtvermeldingen'\[Overzichttype\] = "Voorraad")                                                                                                                                                                                                                                                                                                                                                                                         |
| Nettowijziging voorraad                    | CALCULATE(\[Nettowijziging\], 'Overzichtvermeldingen'\[Overzichttype\] = "Voorraad")                                                                                                                                                                                                                                                                                                                                                                                             |
| Hoeveelheid nettowijziging voorraad           | CALCULATE(\[Hoeveelheid nettowijziging\], 'Overzichtvermeldingen'\[Overzichttype\] = "Voorraad")                                                                                                                                                                                                                                                                                                                                                                                    |
| Nettowijziging voorraad in %                  | IF(\[Eindsaldo voorraad\] = 0, 0, \[Nettowijziging voorraad\] / \[Eindsaldo voorraad\])                                                                                                                                                                                                                                                                                                                                                                           |
| Voorraadomloopsnelheid per bedrag                | if(OR (\[Gemiddeld saldo voorraad\] &lt;= 0, \[Verkochte of verbruikte uitgiften voorraad\] &gt;= 0), 0, ABS (\[Verkochte of verbruikte uitgiften voorraad\]) /\[Gemiddeld saldo voorraad\])                                                                                                                                                                                                                                                                                                  |
| Gemiddeld saldo voorraad               | (\[Eindsaldo voorraad\] + \[Beginsaldo voorraad\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Verkochte of verbruikte uitgiften voorraad       | \[Voorraad verkocht\] + \[Kosten verbruikte materiaal voorraad\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Kosten verbruikt materiaal voorraad        | CALCULATE(\[Nettowijziging voorraad\], 'Overzichtvermeldingen'\[Categorienaam - niveau 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Voorraad verkocht                          | CALCULATE(\[Nettowijziging voorraad\], 'Overzichtvermeldingen'\[Categorienaam - niveau 2\_\] = "Verkocht")                                                                                                                                                                                                                                                                                                                                                                             |
| Voorraadnauwkeurigheid per bedrag            | IF(\[Eindsaldo voorraad\] &lt;= 0, IF(OR(\[Geteld bedrag voorraad\] &lt;&gt; 0, \[Eindsaldo voorraad\] &lt; 0), 0, 1), MAX(0, (\[Eindsaldo voorraad\] - ABS(\[Geteld bedrag voorraad\]))/\[Eindsaldo voorraad\]))                                                                                                                                                                                                                              |
| Geteld bedrag voorraad                | CALCULATE(\[Nettowijziging voorraad\], 'Overzichtvermeldingen'\[Categorienaam - niveau 3\_\] = "Tellen")                                                                                                                                                                                                                                                                                                                                                                         |
| Naar ouderdom rangschikken van voorraad                         | if(ISBLANK(max('Fiscale kalenders'\[Datum\])), blank(), MAX(0, MIN(\[Hoeveelheid ontvangsten naar ouderdom gerangschikte voorraad\], \[Eindsaldo naar ouderdom gerangschikte voorraad\] - \[Hoeveelheid ontvangsten naar ouderdom gerangschikte voorraad in de toekomst\]))) \* \[Gemiddelde kosten per eenheid voorraad\]                                                                                                                                                                                                                                |
| Ontvangsten hoeveelheid naar ouderdom gerangschikte voorraad       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Hoeveelheid nettowijziging voorraad\], 'Overzichtvermeldingen'\[Hoeveelheid\] &gt; 0, FILTER(ALLEXCEPT('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[Id\], 'entiteiten'\[Naam\], 'Grootboeken'\[Valuta\], 'Grootboeken'\[Beschrijving\], 'Grootboeken'\[Naam\]), 'Fiscale kalenders'\[Datum\] &lt;= MAX('Fiscale kalenders'\[Datum\]))), CALCULATE(\[Hoeveelheid nettowijziging voorraad\], 'Overzichtvermeldingen'\[Hoeveelheid\] &gt; 0)) |
| Hoeveelheid eindsaldo naar ouderdom gerangschikte voorraad | \[Hoeveelheid eindsaldo voorraad\] + CALCULATE(\[Hoeveelheid nettowijziging voorraad\], FILTER(ALLEXCEPT('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[Naam\], 'Grootboeken'\[Valuta\], 'Grootboeken'\[Beschrijving\], 'Grootboeken'\[Naam\]), 'Fiscale kalenders'\[Datum\] &gt; max('Fiscale kalenders'\[Datum\]) ))                                                                                                                                 |
| Ontvangsten in de toekomst naar ouderdom gerangschikte voorraad  | CALCULATE(\[Nettowijziging voorraad\], 'Overzichtvermeldingen'\[Bedrag\] &gt; 0, FILTER(ALLEXCEPT('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[Id\], 'entiteiten'\[Naam\], 'Grootboeken'\[Valuta\], 'Grootboeken'\[Beschrijving\], 'Grootboeken'\[Naam\]), 'Fiscale kalenders'\[Datum\] &gt; MAX('Fiscale kalenders'\[Datum\])))                                                                                                                                             |
| Gemiddelde kosten per eenheid voorraad                 | CALCULATE(\[Eindsaldo voorraad\] / \[Hoeveelheid eindsaldo voorraad\],ALLEXCEPT('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[Id\], 'entiteiten'\[Naam\], 'Grootboeken'\[Valuta\], 'Grootboeken'\[Beschrijving\], 'Grootboeken'\[Naam\]))                                                                                                                                                                                                                 |
| Inkoopafwijkingen                      | CALCULATE(SUM(\[Bedrag\]), 'Overzichtvermeldingen'\[Categorienaam - niveau 2\_\] = "Aangeschaft", 'Overzichtvermeldingen'\[Overzichttype\] = "Afwijking")                                                                                                                                                                                                                                                                                                                              |
| Beginsaldo OHW                   | CALCULATE(\[Beginsaldo\], 'Overzichtvermeldingen'\[Overzichttype\] = "OHW")                                                                                                                                                                                                                                                                                                                                                                                            |
| Eindsaldo OHW                      | CALCULATE(\[Eindsaldo\], 'Overzichtvermeldingen'\[Overzichttype\] = "OHW")                                                                                                                                                                                                                                                                                                                                                                                               |
| Nettowijziging OHW                          | CALCULATE(\[Nettowijziging\], 'Overzichtvermeldingen'\[Overzichttype\] = "OHW")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Nettowijziging OHW in %                        | IF (\[Eindsaldo\] = 0, 0, \[Nettowijziging OHW\] / \[Eindsaldo OHW\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Productieafwijkingen                    | CALCULATE(SUM(\[Bedrag\]), 'Overzichtvermeldingen'\[Categorienaam - niveau 2\_\] = "Productiekosten", 'Overzichtvermeldingen'\[Overzichttype\] = "Afwijking")                                                                                                                                                                                                                                                                                                                      |
| Categorienaam - niveau 1                 | switch(\[Categorienaam - niveau 1\_\], "None", "Geen", "NetSourcing", "Nettosourcing", "NetUsage", "Nettogebruik", "NetConversionCost", "Netto-conversiekosten", "NetCostOfGoodsManufactured", "Nettokosten van geproduceerde goederen", "BeginningBalance", "Beginsaldo")                                                                                                                                                                                                         |
| Categorienaam - niveau 2                 | switch(\[Categorienaam - niveau 2\_\], "None", "Geen", "Procured", "Aangeschaft", "Disposed", "Afgestoten", "Transferred", "Overgeboekt", "Sold", "Verkocht", "ConsumedMaterialsCost", "Kosten verbruikte materialen", "ConsumedManufacturingCost", "Kosten van verbruikte productie", "ConsumedOutsourcingCost", "Kosten van verbruikte uitbesteding", "ConsumedIndirectCost", "Verbruikte indirecte kosten", "ManufacturedCost", "Productiekosten", "Variances", "Afwijkingen")                            |
| Categorienaam - niveau 3                 | switch(\[Categorienaam - niveau 3\_\], "None", "Geen", "Tellen", "Geen", "ProductionPriceVariance", "Productieprijs", "QuantityVariance", "Hoeveelheid", "SubstitutionVariance", "Vervanging", "ScrapVariance", "Uitval", "LotSizeVariance", "Partijgrootte", "RevaluationVariance", "Herwaardering", "PurchasePriceVariance", "Inkoopprijs", "CostChangeVariance", "Kostenwijziging", "RoundingVariance", "Afrondingsafwijking")                                                   |

De volgende belangrijke dimensies worden gebruikt als filters voor het segmenteren van de samengevoegde metingen om een grotere mate van granulatie te bereiken en analytischere inzichten te bieden.

| Entiteit           | Voorbeelden van kenmerken                       |
|------------------|----------------------------------------------|
| Entiteiten         | ID, naam                                     |
| Fiscale kalenders | Kalender, maand, periode, kwartaal, jaar       |
| KPI-doelstellingen        | Doelstelling voorraadnauwkeurigheid, doelstelling voorraadomloopsnelheid |
| Grootboeken          | Valuta, naam, beschrijving                  |
| Vestigingen            | Id, naam, land, plaats                      |

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)





