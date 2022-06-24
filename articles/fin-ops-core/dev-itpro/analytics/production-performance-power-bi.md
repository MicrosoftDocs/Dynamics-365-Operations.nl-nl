---
title: Power BI-inhoud Productieprestaties
description: In dit artikel wordt beschreven wat is opgenomen in de Power BI-inhoud Productieprestaties.
author: AndersGirke
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProductionPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cf0d2bdc37efb66f7aee40f237413a2ef5d9f9f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881456"
---
# <a name="production-performance-power-bi-content"></a>Power BI-inhoud Productieprestaties

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Productieprestaties**. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Productieprestaties** is bedoeld voor productiemanagers of personen in de organisatie die verantwoordelijk voor productiebeheer zijn.

Met de rapporten in de inhoud kunt u Power BI gebruiken om de prestaties van de productiebewerkingen te controleren met betrekking tot tijdige uitvoering, kwaliteit en kosten. De rapporten gebruiken transactiegegevens uit productieorders en batchorders en geven zowel een geaggregeerde weergave van productiemetrics uit het hele bedrijf als ook een analyse van de metrics naar product en resource.

De Power BI-inhoud maakt duidelijk in hoeverre de organisatie de productie op tijd en volledig kan uitvoeren. Toekomstige prestaties wordt geschat op basis van de productieplannen. Uitgebreide rapporten bieden gedetailleerd inzicht in productgebreken die worden veroorzaakt door productie, alsmede de defectenpercentages voor resources en bewerkingen.

Met deze Power BI-inhoud kunt u ook productieafwijkingen analyseren. Productieafwijkingen worden berekend als het verschil tussen geschatte kosten en gerealiseerde kosten. Productieafwijkingen worden berekend wanneer productieorders of batchorders de status **Beëindigd** bereiken.

De Power BI-inhoud **Productieprestaties** bevat gegevens die afkomstig zijn uit productieorders en batchorders. De rapporten bevatten geen gegevens die zijn gerelateerd aan kanbanproductie.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud
De Power BI-inhoud **Productieprestaties** wordt weergegeven op de pagina **Productieprestaties** (**Productiebeheer** \> **Query's en rapporten** \> **Productieprestatieanalyse** \> **Productieprestaties**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud

De Power BI-inhoud **Productieprestaties** bevat een set rapportpagina's. Elke pagina bestaat uit een set metrische gegevens die worden gevisualiseerd als diagrammen, tegels en tabellen.

In de volgende tabel vindt u een overzicht van de visualisaties die worden meegeleverd.

| Rapportpagina                                | Diagrammen | Tegels |
|--------------------------------------------|--------|-------|
| Productieprestaties                     | <ul><li>Aantal producties op datum</li><li>Aantal producties op product- en artikelgroep</li><li>Aantal geplande producties op datum</li><li>Onderste 10 producten op tijdigheid en volledigheid</li></ul> | <ul><li>Totaal orders</li><li>Percentage op tijd en volledig</li><li>Percentage onvolledig</li><li>Percentage te vroeg</li><li>Percentage te laat</li></ul> |
| Defecten op product                         | <ul><li>Defectverhoudingen (ppm) op datum</li><li>Defectverhoudingen (ppm) op product- en artikelgroep</li><li>Geproduceerde hoeveelheid op datum</li><li>Top 10 van producten op defectverhouding</li></ul> | <ul><li>Defectverhoudingen (ppm)</li><li>Afwijkend aantal</li><li>Totale hoeveelheid</li></ul> |
| Defectentrend op product                   | Defectverhouding (ppm) op geproduceerde hoeveelheid | Defectverhouding (ppm) |
| Defecten op resource                        | <ul><li>Defectverhouding (ppm) op datum</li><li>Defectverhouding (ppm) op bron en vestiging</li><li>Defectverhouding (ppm) op bewerking</li><li>Top 10 resources op defectverhouding</li></ul> | Afwijkend aantal |
| Defectentrend op resource                  | Defectverhouding (ppm) op verwerkte hoeveelheid | |
| Productieafwijkingen voor kostprijsberekening via taakorders | <ul><li>Productieafwijking op datum en kostengroeptype</li><li>Productieafwijking op vestiging en kostengroeptype</li><li>Top 10 producten met ongunstige productieafwijking</li><li>Top 10 ongunstige productieafwijkingen op resource</li></ul> | <ul><li>Gerealiseerde kosten</li><li>Afwijking productie</li><li>Percentage productieafwijking</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

De volgende gegevens worden gebruikt voor de rapportpagina's in de Power BI-inhoud **Productieprestaties**. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie over de entiteitopslag [Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

In de volgende tabel ziet u de belangrijke geaggregeerde metingen die worden gebruikt als basis voor de Power BI-inhoud.

| Entiteit                   | Belangrijke samengevoegde metingen  | Gegevensbron voor Finance and Operations-apps | Veld              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

In de volgende tabel ziet u hoe de belangrijkste samengevoegde metingen worden gebruikt om verschillende berekende eenheden te maken in de gegevensset van de inhoud.

| Maat                  | Hoe de meting wordt berekend |
|--------------------------|-------------------------------|
| Percentage productieafwijking   | SOM('Productieafwijking'\[Productieafwijking\]) / SOM('Productieafwijking'\[Geschatte kosten\]) |
| Alle geplande orders       | COUNTROWS('Geplande productieorder') |
| Te vroeg                    | COUNTROWS(FILTER('Geplande productieorder', 'Geplande productieorder'\[Geplande einddatum\] \< 'Geplande productieorder'\[Behoeftedatum\])) |
| Te laat                     | COUNTROWS(FILTER('Geplande productieorder', 'Geplande productieorder'\[Geplande einddatum\] \> 'Geplande productieorder'\[Behoeftedatum\])) |
| Op tijd                  | COUNTROWS(FILTER('Geplande productieorder', 'Geplande productieorder'\[Geplande einddatum\] = 'Geplande productieorder'\[Behoeftedatum\])) |
| Percentage op tijd                | IF ( 'Geplande productieorder'\[Op tijd\] \<\> 0, 'Geplande productieorder'\[Op tijd\], IF ('Geplande productieorder'\[Alle geplande orders\] \<\> 0, 0, BLANK()) ) / 'Geplande productieorder'\[Alle geplande orders\] |
| Ingevuld                | COUNTROWS(FILTER ('Productieorder', 'Productieorder'\[Is RAF'ed\] = TRUE)) |
| Defectverhoudingen (ppm)     | IF('Productieorder'\[Totale hoeveelheid\] = 0, BLANK(), (SUM('Productieorder'\[Afwijkend aantal\]) / 'Productieorder'\[Totale hoeveelheid\]) \* 1000000) |
| Percentage vertraagde producties  | 'Productieorder'\[Te laat \#\] / 'Productieorder'\[Voltooid\] |
| Te vroeg en volledig          | COUNTROWS(FILTER('Productieorder', 'Productieorder'\[Is volledig\] = TRUE && 'Productieorder'\[Is te vroeg\] = TRUE)) |
| \# (aantal) te vroeg                 | COUNTROWS(FILTER('Productieorder', 'Productieorder'\[Is te vroeg\] = TRUE)) |
| Percentage te vroeg                  | IFERROR( IF('Productieorder'\[Te vroeg\#\] \<\> 0, 'Productieorder'\[Te vroeg\#\], IF('Productieorder'\[Totaal orders\] = 0, BLANK(), 0)) / 'Productieorder'\[Totaal orders\], BLANK()) |
| Incompleet               | COUNTROWS(FILTER('Productieorder', 'Productieorder'\[Is volledig\] = FALSE && 'Productieorder'\[Is RAF'ed\] = TRUE)) |
| Percentage onvolledig             | IFERROR( IF('Productieorder'\[Onvolledig\]\<\> 0, 'Productieorder'\[Onvolledig\], IF('Productieorder'\[Totaal orders\] = 0, BLANK(), 0)) / 'Productieorder'\[Totaal orders\], BLANK()) |
| Is vertraagd               | 'Productieorder'\[Is RAF'ed\] = TRUE && 'Productieorder'\[Waarde Vertraagd\] = 1 |
| Is te vroeg                 | 'Productieorder'\[Is RAF'ed\] = TRUE && 'Productieorder'\[Dagen vertraagd\] \< 0 |
| Is volledig               | 'Productieorder'\[Hoeveelheid goed\] \>= 'Productieorder'\[Geplande hoeveelheid\] |
| Is RAF'ed                | 'Productieorder'\[Productiestatuswaarde\] = 5 \|\| 'Productieorder'\[Productiestatuswaarde\] = 7 |
| Laat & volledig           | COUNTROWS(FILTER('Productieorder', 'Productieorder'\[Is volledig\] = TRUE && 'Productieorder'\[Is vertraagd\] = TRUE)) |
| \# (aantal) te laat                  | COUNTROWS(FILTER('Productieorder', 'Productieorder'\[Is vertraagd\] = TRUE)) |
| Percentage te laat                   | IFERROR( IF('Productieorder'\[Te laat \#\] \<\> 0, 'Productieorder'\[Te laat \#\], IF('Productieorder'\[Totaal orders\] = 0, BLANK(), 0)) / 'Productieorder'\[Totaal orders\], BLANK()) |
| Op tijd en volledig        | COUNTROWS(FILTER('Productieorder', 'Productieorder'\[Is volledig\] = TRUE && 'Productieorder'\[Is vertraagd\] = FALSE && 'Productieorder'\[Is te vroeg\] = FALSE)) |
| Percentage op tijd en volledig      | IFERROR( IF('Productieorder'\[Tijdig & volledig\] \<\> 0, 'Productieorder'\[Tijdig & volledig\], IF('Productieorder'\[Voltooid\] = 0, BLANK(), 0)) / 'Productieorder'\[Voltooid\], BLANK()) |
| Totaal orders             | COUNTROWS('Productieorder') |
| Totale hoeveelheid           | SUM('Productieorder'\[Goede hoeveelheid\]) + SUM('Productieorder'\[Afwijkend aantal\]) |
| Defectverhouding (ppm)        | IF( 'Routetransacties'\[Hoeveelheid verwerkt\] = 0, BLANK(), (SUM('Routetransacties'\[Afwijkend aantal\]) / 'Routetransacties'\[Hoeveelheid verwerkt\]) \* 1000000) |
| Defectverhouding gemengd (ppm) | IF( 'Routetransacties'\[Totale gemengde hoeveelheid\] = 0, BLANK(), (SUM('Routetransacties'\[Afwijkend aantal\]) / 'Routetransacties'\[Totale gemengde hoeveelheid\]) \* 1000000) |
| Verwerkte hoeveelheid       | SUM('Routetransacties'\[Goede hoeveelheid\]) + SUM('Routetransacties'\[Afwijkend aantal\]) |
| Totale gemengde hoeveelheid     | SUM('Productieorder'\[Goede hoeveelheid\]) + SUM('Routetransacties'\[Afwijkend aantal\]) |

In de volgende tabel ziet u de belangrijke dimensies die worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.

| Entiteit                    | Voorbeelden van kenmerken                                        |
|---------------------------|---------------------------------------------------------------|
| Gereedmeldingsdatum | Voltooiingsdatum (gereedgemeld), Maand en Jaarverschuiving                 |
| Einddatum                | Verschuiving beëindigde maand en Maand                                  |
| Behoeftedatum          | Maandverschuiving Behoeftedatum en Behoeftedatum            |
| Routetransactiedatum    | Routetransactie maandverschuiving en Datum                       |
| Vestigingen                     | Vestigings-id, Vestigingsdatum, Staat en Plaats                          |
| Entiteiten                  | Id en Naam                                                   |
| Resources                 | Resource-id, Resourcenaam, Resourcetype en Resourcegroep |
| Producten                  | Productnummer, Productnaam, Artikel-id en Artikelgroep         |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]