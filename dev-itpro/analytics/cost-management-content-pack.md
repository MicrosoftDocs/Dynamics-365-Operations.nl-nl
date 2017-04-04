---
title: kostenbeheer Power BI inhoud
description: Dit onderwerp wordt beschreven wat wordt opgenomen in het kostenbeheer Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de rapporten Power BI en informatie over het gegevensmodel en entiteiten die worden gebruikt voor het bouwen van de inhoud.
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>kostenbeheer Power BI inhoud

Dit onderwerp wordt beschreven wat wordt opgenomen in het kostenbeheer Power BI-inhoud. Deze wordt uitgelegd hoe u toegang tot de rapporten Power BI en informatie over het gegevensmodel en entiteiten die worden gebruikt voor het bouwen van de inhoud.

# <a name="overview"></a>Overzicht

De **kostenbeheer** Microsoft Power BI-inhoud is bedoeld voor accountants van de voorraad of personen in de organisatie die verantwoordelijk voor voorraad zijn. De **kostenbeheer** Power BI inhoud biedt leidinggevende inzicht in de voorraad en voorraad werk onderhanden werk (OHW) en hoe kosten door stroomt door ze te categorie na verloop van tijd. De informatie kan ook worden gebruikt als een uitgebreide aanvulling op het financiële overzicht.

## <a name="key-measures"></a>Belangrijke maatregelen

+ Beginsaldo
+ Eindsaldo
+ Nettowijziging
+ Netto wijziging in %
+ Ouderdomsrangschikking

## <a name="key-performance-indicators"></a>Key Performance Indicators
+ Voorraadomloopsnelheid
+ Voorraadnauwkeurigheid

De primaire gegevensbron voor CostAggregatedCostStatementEntryEntity is de tabel CostStatementCache. Deze tabel wordt beheerd door het kader van de cache gegevensset. De tabel wordt elke 24 uur bijgewerkt, maar u kunt handmatig bijwerken in de cache Gegevensconfiguratie inschakelen. Vervolgens kunt u een handmatige update doen in de **kostenbeheer** of **analysis kosten** werkruimte. Nadat het bijwerken van CostStatementCache is uitgevoerd, kunt u de OData-verbinding op stroom BI.com bijgewerkte gegevens bekijken op de site moet bijwerken. De afwijking (inkoop, productie) maatregelen in deze inhoud Power BI hebben alleen betrekking op artikelen die door de methode van de voorraad standaardkosten worden valuated. Productieafwijking wordt berekend als het verschil tussen de actieve kosten en gerealiseerde kosten. De afwijking van de productie wordt berekend wanneer de productieorder de status heeft **beëindigd**. Zie voor meer informatie over de typen productieafwijking productie en de berekening van elk type [over het analyseren van afwijkingen voor een voltooide productieorder](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Toegang tot de content Power BI
De **kostenbeheer** Power BI-inhoud is beschikbaar vanuit PowerBI.com. Zie voor meer informatie over het maken en uw Microsoft Dynamics 365 voor bewerkingen gegevens laden, [toegang Power BI-inhoud van PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Prestatiegegevens die zijn opgenomen in de Power BI-inhoud
De inhoud bevat een reeks rapportpagina's. Elke pagina bestaat uit een set parameters die worden weergegeven als diagrammen, tegels en tabellen. De volgende tabel bevat een overzicht van de visualisaties in de **kostenbeheer** Power BI-inhoud.

| Rapportpagina. | Diagrammen | Titels |
|---|---|---|
|Totale voorraad (standaard door de huidige periode) |Nauwkeurigheid |Voorraad-eenheden:<br>Voorraad eindsaldo<br>Voorraad-mutatie<br>Voorraad netto wijziging %<br>|
| |Voorraadomloopsnelheid | |
| |Voorraad eindsaldo per resourcegroep | |
| |Nettowijziging van voorraad per categorie naam niveau 1 en 2 naam categorieniveau| |
| |Opdracht afwijkingen per groep van bronnen en categorie naam niveau 3 | |
|Van voorraad per site (standaard door de huidige periode) |Voorraad eindsaldo door de naam van Site en de resourcegroep | |
| |Voorraad in te schakelen door de naam van Site en de resourcegroep | |
| |Voorraad eindsaldo per plaats en Resource-groep | |
|Van voorraad per resourcegroep (standaard door de huidige periode) |Voorraad-metingen | |
| |Nauwkeurigheid van de voorraad door het bedrag per resourcegroep | |
| |Voorraad in te schakelen door het bedrag per resourcegroep | |
|Voorraad YOY (standaard huidige jaar vs vorig jaar) |Voorraad-metingen | |
| |Voorraad-KPI's:<br>Voorraadomloopsnelheid<br>Voorraadnauwkeurigheid | |
| |Voorraad eindsaldo per jaar en Resource-groep | |
| |Opdracht afwijkingen per jaar en categorie naam niveau 3 | |
|Voorraad naar ouderdom gerangschikt (standaard door het huidige jaar) |Voorraad vervallen per kwartaal en Resource-groep | |
| |Voorraad vervallen per kwartaal en de locatie | |
|Totale OHW (standaard door de huidige periode) |Netto OHW wijzigen door de categorie naam niveau 1 en de categorie naam niveau 2 |Onderhanden maatregelen:<br>Eindsaldo OHW<br>OHW-mutatie<br>OHW-netto wijziging %<br> |
| |Productieafwijkingen per groep van bronnen en categorie naam niveau 3 | |
| |OHW-mutatie per resourcegroep | |
|OHW per locatie (standaard door de huidige periode) |Onderhanden werk OHW maatregelen | |
| |Netto OHW wijzigen door de naam van de locatie en categorie naam niveau 2 | |
| |Productieafwijkingen locatienaam en categorie naam niveau 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Dynamics 365 voor bewerkingen gegevens wordt gebruikt voor het vullen van de rapportpagina's in de **kostenbeheer** Power BI-inhoud. Deze gegevens wordt vertegenwoordigd door statistische metingen die worden klaargezet in het archief entiteit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [overzicht Power BI-integratie met entiteit winkel](power-bi-integration-entity-store.md). De volgende belangrijke statistische metingen worden gebruikt als basis voor de inhoud.

| Entiteit            | Belangrijke statistische meting | Gegevensbron voor Dynamics 365 for Operations | Veld             | Omschrijving                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Afschriften | Nettowijziging                | CostAggregatedCostStatementEntryEntity      | Som (\[bedrag\])   | Bedrag in de valuta voor boekhouding |
| Afschriften | Netto wijziging hoeveelheid       | CostAggregatedCostStatementEntryEntity      | Som (\[hoeveelheid\]) |                                   |

De volgende tabel ziet hoe de belangrijkste statistische metingen worden gebruikt voor verschillende berekende eenheden maken in de inhoud van de gegevensset.

| Maat                                 | Hoe de maateenheid wordt berekend                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beginsaldo                       | \[Eindsaldo\]-\[mutatie\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Begin Saldohoeveelheid              | \[Saldo eindhoeveelheid\]-\[netto hoeveelheid wijzigen\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Eindsaldo                          | BEREKENEN (som (\[bedrag\]), FILTER (ALLEXCEPT ('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[naam\], 'grootboeken'\[valuta\], 'grootboeken'\[omschrijving\], 'grootboeken'\[naam\]), 'Fiscale kalenders'\[datum\]&lt;= MAX ('Fiscale kalenders'\[datum\])))                                                                                                                                                                                           |
| Einde Saldohoeveelheid                 | BEREKENEN (som (\[hoeveelheid\]), FILTER (ALLEXCEPT ('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[naam\], 'grootboeken'\[valuta\], 'grootboeken'\[omschrijving\], 'grootboeken'\[naam\]), 'Fiscale kalenders'\[datum\]&lt;= MAX ('Fiscale kalenders'\[datum\])))                                                                                                                                                                                         |
| Voorraad beginsaldo             | BEREKENEN (\[beginsaldo\], 'Overzicht vermeldingen'\[instructietype\] = "Voorraad")                                                                                                                                                                                                                                                                                                                                                                                      |
| Voorraad eindsaldo                | BEREKENEN (\[eindsaldo\], 'Overzicht vermeldingen'\[instructietype\] = "Voorraad")                                                                                                                                                                                                                                                                                                                                                                                         |
| Voorraad-mutatie                    | BEREKENEN (\[mutatie\], 'Overzicht vermeldingen'\[instructietype\] = "Voorraad")                                                                                                                                                                                                                                                                                                                                                                                             |
| Hoeveelheid in voorraad Nettowijziging           | BEREKENEN (\[netto hoeveelheid wijzigen\], 'Overzicht vermeldingen'\[instructietype\] = "Voorraad")                                                                                                                                                                                                                                                                                                                                                                                    |
| Voorraad netto wijziging %                  | IF (\[voorraad eindsaldo\] = 0, 0, \[mutatie in voorraad\] / \[voorraad eindsaldo\])                                                                                                                                                                                                                                                                                                                                                                           |
| Voorraad door het bedrag in te schakelen                | Als (OR (\[gemiddeld saldo in voorraad\]&lt;= 0, \[voorraad verkocht of verbruikt problemen\]&gt;= 0), 0, ABS (\[voorraad verkocht of verbruikt problemen\]) /\[gemiddeld saldo in voorraad\])                                                                                                                                                                                                                                                                                                  |
| Gemiddelde voorraadsaldo               | (\[Voorraad eindsaldo\] + \[voorraad beginsaldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Voorraad verkocht of verbruikt problemen       | \[Verkochte voorraad\] + \[voorraad verbruikt materiaalkosten\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Voorraad verbruikt materiaalkosten        | BEREKENEN (\[voorraad mutatie\], 'Overzicht vermeldingen'\[categorienaam - niveau 2\_\] = 'ConsumedMaterialsCost')                                                                                                                                                                                                                                                                                                                                                            |
| Verkochte voorraad                          | BEREKENEN (\[voorraad mutatie\], 'Overzicht vermeldingen'\[categorienaam - niveau 2\_\] = 'Verkocht')                                                                                                                                                                                                                                                                                                                                                                             |
| Nauwkeurigheid van de voorraad met bedrag            | Als (\[voorraad eindsaldo\]&lt;= 0 is, als (of (\[voorraad geteld bedrag\]&lt;&gt; 0, \[eindsaldo in voorraad\]&lt; 0), 0, 1), MAX (0, (\[voorraad eindsaldo\] -ABS (\[voorraad geteld bedrag\])) /\[eindsaldo in voorraad\]))                                                                                                                                                                                                                              |
| Het getelde bedrag voorraad                | BEREKENEN (\[voorraad mutatie\], 'Overzicht vermeldingen'\[categorienaam - niveau 3\_\] = 'Telling')                                                                                                                                                                                                                                                                                                                                                                         |
| Naar ouderdom rangschikken van voorraad                         | Als (ISLEEG (max ('Fiscale kalenders'\[datum\])), blank(), MAX (0, MIN (\[ouderdom van de voorraad ontvangsten hoeveelheid\], \[voorraad ouderdom eindhoeveelheid saldo\] - \[ouderdom van de voorraad ontvangsten hoeveelheid in de toekomst\]))) \*\[voorraad gemiddelde kosten per eenheid\]                                                                                                                                                                                                                                |
| Voorraad naar ouderdom hoeveelheid van ontvangsten       | Als (\[minDate\] = \[minDateAllSelected\], berekenen (\[mutatie hoeveelheid in voorraad\], 'Afschriften'\[hoeveelheid\]&gt; 0, FILTER (ALLEXCEPT ('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[naam\], 'grootboeken'\[valuta\], 'grootboeken'\[omschrijving\], 'grootboeken'\[naam\]), 'Fiscale kalenders'\[datum\]&lt;= MAX ('Fiscale kalenders'\[datum\]))), berekenen (\[mutatie hoeveelheid in voorraad\], 'Overzicht vermeldingen'\[hoeveelheid\]&gt; 0)) |
| Voorraad naar ouderdom gerangschikt saldo eindhoeveelheid | \[Voorraad saldo eindhoeveelheid\] + berekenen (\[mutatie hoeveelheid in voorraad\], FILTER (ALLEXCEPT ('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[naam\], 'grootboeken'\[valuta\], 'grootboeken'\[omschrijving\], 'grootboeken'\[naam\]), 'Fiscale kalenders'\[datum\]&gt; max ('Fiscale kalenders'\[datum\])))                                                                                                                                 |
| Naar ouderdom gerangschikte voorraadontvangsten in de toekomst  | BEREKENEN (\[voorraad mutatie\], 'Afschriften'\[bedrag\]&gt; 0 FILTER (ALLEXCEPT ('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[naam\], 'grootboeken'\[valuta\], 'grootboeken'\[omschrijving\], 'grootboeken'\[naam\]), 'Fiscale kalenders'\[datum\]&gt; MAX ('Fiscale kalenders'\[datum\])))                                                                                                                                             |
| Voorraad gemiddelde kosten per eenheid                 | BEREKENEN (\[voorraad eindsaldo\] / \[voorraad eindhoeveelheid saldo\], ALLEXCEPT ('Fiscale kalenders', 'Fiscale kalenders'\[LedgerRecId\], 'entiteiten'\[ID\], 'entiteiten'\[naam\], 'grootboeken'\[valuta\], 'grootboeken'\[omschrijving\], 'grootboeken'\[naam\]))                                                                                                                                                                                                                 |
| Inkoopafwijkingen                      | BEREKENEN (som (\[bedrag\]), 'Overzicht vermeldingen'\[de naam van de categorie - niveau 2\_\] = 'Procured', 'Overzicht vermeldingen'\[instructietype\] = 'Verschil')                                                                                                                                                                                                                                                                                                                              |
| Beginsaldo OHW                   | BEREKENEN (\[beginsaldo\], 'Overzicht vermeldingen'\[instructietype\] = 'OHW')                                                                                                                                                                                                                                                                                                                                                                                            |
| Eindsaldo OHW                      | BEREKENEN (\[eindsaldo\], 'Overzicht vermeldingen'\[instructietype\] = 'OHW')                                                                                                                                                                                                                                                                                                                                                                                               |
| OHW-mutatie                          | BEREKENEN (\[mutatie\], 'Overzicht vermeldingen'\[instructietype\] = 'OHW')                                                                                                                                                                                                                                                                                                                                                                                                   |
| OHW-netto wijziging %                        | IF (\[OHW eindsaldo\] = 0, 0, \[OHW mutatie\] / \[OHW eindsaldo\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Productieafwijkingen                    | BEREKENEN (som (\[bedrag\]), 'Overzicht vermeldingen'\[de naam van de categorie - niveau 2\_\] = 'ManufacturedCost', 'Overzicht vermeldingen'\[instructietype\] = 'Verschil')                                                                                                                                                                                                                                                                                                                      |
| De naam van de categorie - niveau 1                 | Schakelen (\[de naam van de categorie - niveau 1\_\], 'Geen', 'Geen', 'NetSourcing', 'Netto sourcing', 'NetUsage', 'Netto gebruik', 'NetConversionCost', 'Netto conversie kosten', 'NetCostOfGoodsManufactured', 'Netto kosten van geproduceerde goederen', 'BeginningBalance', 'Beginsaldo')                                                                                                                                                                                                         |
| De naam van de categorie - niveau 2                 | Schakelen (\[de naam van de categorie - niveau 2\_\], 'Geen', 'Geen', 'Procured', 'Procured', 'Disposed', 'Disposed', 'De overgedragen', 'De overgedragen', 'Verkocht', 'Verkocht', 'ConsumedMaterialsCost', 'Verbruikt materiaalkosten', 'ConsumedManufacturingCost', 'Verbruikt manufacturing kosten', 'ConsumedOutsourcingCost', 'Verbruikt uitbesteding kosten', 'ConsumedIndirectCost', 'Verbruikt indirecte kosten', 'ManufacturedCost', 'Gefabriceerd kosten', 'Afwijkingen', 'Afwijkingen')                            |
| De naam van de categorie - niveau 3                 | Schakelen (\[categorienaam - niveau 3\_\], 'Geen', 'Geen', 'Telling', 'Geen', 'productionPriceVariance', 'productieprijs', 'QuantityVariance', 'Aantal', 'SubstitutionVariance', 'Vervangen', 'ScrapVariance', 'Uitval', 'LotSizeVariance', 'Partijgrootte', 'RevaluationVariance', 'Herwaardering', 'PurchasePriceVariance', 'Inkoopprijs', 'CostChangeVariance', 'kostenwijziging', 'RoundingVariance', 'Afrondingsafwijking')                                                   |

De volgende belangrijke dimensies worden gebruikt als filters voor het segmenteren van de statistische metingen grotere mate van granulatie bereiken en meer analytische inzicht bieden.

| Entiteit           | Voorbeelden van kenmerken                       |
|------------------|----------------------------------------------|
| Entiteiten         | ID, naam                                     |
| Fiscale kalenders | Kalender, maand, periode, kwartaal, jaar       |
| KPI-doelstellingen        | Doelstelling van de juistheid voorraad, voorraad schakelen doelstelling |
| Grootboeken          | Valuta, naam, beschrijving                  |
| Vestigingen            | ID, naam, land, plaats                      |

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)



