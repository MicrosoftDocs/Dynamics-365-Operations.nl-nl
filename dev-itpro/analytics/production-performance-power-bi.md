---
title: Power BI-inhoud Productieprestaties
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Productieprestaties. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: sericks
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 915ff93edff0f68f52a536ad169c8f0f917ac9b2
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017

---

# <a name="production-performance-power-bi-content"></a>Power BI-inhoud Productieprestaties

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Productieprestaties**. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Productieprestaties** is bedoeld voor productiemanagers of personen in de organisatie die verantwoordelijk voor productiebeheer zijn.

Met de rapporten in de inhoud kunt u Power BI gebruiken om de prestaties van de productiebewerkingen te controleren met betrekking tot tijdige uitvoering, kwaliteit en kosten. De rapporten gebruiken transactiegegevens uit productieorders en batchorders en geven zowel een geaggregeerde weergave van productiemetrics uit het hele bedrijf als ook een analyse van de metrics naar product en resource.

De Power BI-inhoud maakt duidelijk in hoeverre de organisatie de productie op tijd en volledig kan uitvoeren. Toekomstige prestaties wordt geschat op basis van de productieplannen. Uitgebreide rapporten bieden gedetailleerd inzicht in productgebreken die worden veroorzaakt door productie, alsmede de defectenpercentages voor resources en bewerkingen.

Met deze Power BI-inhoud kunt u ook productieafwijkingen analyseren. Productieafwijkingen worden berekend als het verschil tussen geschatte kosten en gerealiseerde kosten. Productieafwijkingen worden berekend wanneer productieorders of batchorders de status **Beëindigd** bereiken.

De Power BI-inhoud **Productieprestaties** bevat gegevens die afkomstig zijn uit productieorders en batchorders. De rapporten bevatten geen gegevens die zijn gerelateerd aan kanbanproductie.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
Als u werkt met de update voor juli 2017 van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, vindt u de Power BI-inhoud **Productieprestaties** op de pagina **Productieprestaties** (**Productiebeheer** > **Query's en rapporten** > **Productieprestatieanalyse** > **Productieprestaties**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud

De Power BI-inhoud **Productieprestaties** bevat een set rapportpagina's. Elke pagina bestaat uit een set metrische gegevens die worden gevisualiseerd als diagrammen, tegels en tabellen.

In de volgende tabel vindt u een overzicht van de visualisaties die worden meegeleverd.

| Rapportpagina                                | Diagrammen                                               | Tegels |
|--------------------------------------------|------------------------------------------------------|-------|
| Productieprestaties                     | <ul><li>Aantal producties op datum</li><li>Aantal producties op product- en artikelgroep</li><li>Aantal geplande producties op datum</li><li>Onderste 10 producten op tijdigheid en volledigheid</li></ul> | <ul><li>Totaal orders</li><li>Percentage op tijd en volledig</li><li>Percentage onvolledig</li><li>Percentage te vroeg</li><li>Percentage te laat</li></ul> |
| Defecten op product                         | <ul><li>Defectverhoudingen (ppm) op datum</li><li>Defectverhoudingen (ppm) op product- en artikelgroep</li><li>Geproduceerde hoeveelheid op datum</li><li>Top 10 van producten op defectverhouding</li></ul> | <ul><li>Defectverhoudingen (ppm)</li><li>Afwijkend aantal</li><li>Totale hoeveelheid</li></ul> |
| Defectentrend op product                   | Defectverhouding (ppm) op geproduceerde hoeveelheid | Defectverhouding (ppm) |
| Defecten op resource                        | <ul><li>Defectverhouding (ppm) op datum</li><li>Defectverhouding (ppm) op bron en vestiging</li><li>Defectverhouding (ppm) op bewerking</li><li>Top 10 resources op defectverhouding</li></ul> | Afwijkend aantal |
| Defectentrend op resource                  | Defectverhouding (ppm) op verwerkte hoeveelheid | |
| Productieafwijkingen voor kostprijsberekening via taakorders | <ul><li>Productieafwijking op datum en kostengroeptype</li><li>Productieafwijking op vestiging en kostengroeptype</li><li>Top 10 producten met ongunstige productieafwijking</li><li>Top 10 ongunstige productieafwijkingen op resource</li></ul> | <ul><li>Gerealiseerde kosten</li><li>Afwijking productie</li><li>Percentage productieafwijking</li></ul> |

## <a name="extending-the-power-bi-content"></a>De Power BI-inhoud uitbreiden
Met behulp van de inhoudpakketten die beschikbaar zijn in Microsoft Dynamics Lifecycle Services (LCS) kunt u grondige analyses verschaffen aan personen die zich niet bij Microsoft Dynamics 365 aanmelden. U kunt deze inhoudpakketten wijzigen zodat ze andere rapporten of visuele elementen bevatten, en de inhoudpakketten vervolgens publiceren naar uw Power BI.com-tenant voor analyse.

U vindt de Power BI-inhoud **Productieprestaties** in de bibliotheek voor gedeelde materialen in LCS. Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md). Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

Let erop dat u de inhoud **Productieprestaties** downloadt, die van toepassing is voor de versie van Dynamics 365 die u gebruikt.

> [!NOTE]
> Als u werkt met Microsoft Dynamics 365 for Operations, versie 1611, is KB 4011327 een voorwaarde voor gebruik van deze volgende Power BI-inhoud: Nadat u zich bij LCS hebt aangemeld, kunt u de KB hier openen: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

De volgende gegevens wordt gebruikt voor de rapportpagina's in de Power BI-inhoud **Productieprestaties**. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie over de entiteitopslag, [Power BI-integratie met de Entiteitopslag](power-bi-integration-entity-store.md).

In de volgende tabel ziet u de belangrijke geaggregeerde metingen die worden gebruikt als basis voor de Power BI-inhoud.

| Entiteit                   | Belangrijke samengevoegde metingen  | Gegevensbron voor Finance and Operations | Veld              |
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
| Percentage productieafwijking   | SOM('Productieafwijking'[Productieafwijking]) / SOM('Productieafwijking'[Geschatte kosten]) |
| Alle geplande orders       | COUNTROWS('Geplande productieorder') |
| Te vroeg                    | COUNTROWS(FILTER('Geplande productieorder', 'Geplande productieorder'[Geplande einddatum] \< 'Geplande productieorder'[Behoeftedatum])) |
| Te laat                     | COUNTROWS(FILTER('Geplande productieorder', 'Geplande productieorder'[Geplande einddatum] \> 'Geplande productieorder'[Behoeftedatum])) |
| Op tijd                  | COUNTROWS(FILTER('Geplande productieorder', 'Geplande productieorder'[Geplande einddatum] = 'Geplande productieorder'[Behoeftedatum])) |
| Percentage op tijd                | IF ( 'Geplande productieorder'[Op tijd] \<\> 0, 'Geplande productieorder'[Op tijd], IF ('Geplande productieorder'[Alle geplande orders] \<\> 0, 0, BLANK()) ) / 'Geplande productieorder'[Alle geplande orders] |
| Voltooid                | COUNTROWS (FILTER ('Productieorder', 'Productieorder' [Is RAF'ed] = TRUE)) |
| Defectverhoudingen (ppm)     | IF('Productieorder' [Totale hoeveelheid] = 0, BLANK(), (SUM('Productieorder' [Afwijkend aantal]) / 'Productieorder'[Totale hoeveelheid]) \* 1000000) |
| Percentage vertraagde producties  | 'Productieorder'[Te laat \#] / 'Productieorder'[Voltooid] |
| Te vroeg en volledig          | COUNTROWS(FILTER('Productieorder', 'Productieorder'[Is volledig] = TRUE && 'Productieorder'[Is te vroeg] = TRUE)) |
| \# (aantal) te vroeg                 | COUNTROWS(FILTER('Productieorder', 'Productieorder'[Is te vroeg] = TRUE)) |
| Percentage te vroeg                  | IFERROR( IF('Productieorder'[\# te vroeg] \<\> 0, 'Productieorder'[\# te vroeg], IF('Productieorder'[Totaal orders] = 0, BLANK(), 0)) / 'Productieorder'[Totaal orders], BLANK()) |
| Onvolledig               | COUNTROWS(FILTER('Productieorder', 'Productieorder'[Is volledig] = FALSE && 'Productieorder'[Is RAF'ed] = TRUE)) |
| Percentage onvolledig             | IFERROR( IF('Productieorder'[Onvolledig] \<\> 0, 'Productieorder'[Onvolledig], IF('Productieorder'[Totaal orders] = 0, BLANK(), 0)) / 'Productieorder'[Totaal orders], BLANK()) |
| Is vertraagd               | 'Productieorder'[Is RAF'ed] = TRUE && 'Productieorder'[Waarde Vertraagd] = 1 |
| Is te vroeg                 | 'Productieorder'[Is RAF'ed] = TRUE && 'Productieorder'[Dagen vertraagd] \< 0 |
| Is volledig               | 'Productieorder'[Hoeveelheid goed] \>= 'Productieorder'[Geplande hoeveelheid] |
| Is RAF'ed                | 'Productieorder'[Waarde Productiestatus] = 5 \|\| 'Productieorder'[Waarde Productiestatus] = 7 |
| Laat & volledig           | COUNTROWS(FILTER('Productieorder', 'Productieorder'[Is volledig] = TRUE && 'Productieorder'[Is vertraagd] = TRUE)) |
| \# (aantal) te laat                  | COUNTROWS(FILTER('Productieorder', 'Productieorder'[Is vertraagd] = TRUE)) |
| Percentage te laat                   | IFERROR( IF('Productieorder'[Te laat \#] \<\> 0, 'Productieorder'[\# te laat], IF('Productieorder'[Totaal orders] = 0, BLANK(), 0)) / 'Productieorder'[Totaal orders], BLANK()) |
| Op tijd en volledig        | COUNTROWS(FILTER('Productieorder', 'Productieorder'[Is volledig] = TRUE && 'Productieorder'[Is vertraagd] = FALSE && 'Productieorder'[Is te vroeg] = FALSE)) |
| Percentage op tijd en volledig      | IFERROR( IF('Productieorder'[Tijdig & volledig] \<\> 0, 'Productieorder'[Tijdig & volledig], IF('Productieorder'[Voltooid] = 0, BLANK(), 0)) / 'Productieorder'[Voltooid], BLANK()) |
| Totaal orders             | COUNTROWS('Productieorder') |
| Totale hoeveelheid           | SUM('Productieorder'[Hoeveelheid goed]) + SUM('Productieorder'[Afwijkend aantal]) |
| Defectverhouding (ppm)        | IF( 'Routetransacties'[Hoeveelheid verwerkt] = 0, BLANK(), (SUM('Routetransacties'[Afwijkend aantal]) / 'Routetransacties'[Hoeveelheid verwerkt]) \* 1000000) |
| Defectverhouding gemengd (ppm) | IF( 'Routetransacties'[Totale gemengde hoeveelheid] = 0, BLANK(), (SUM('Routetransacties'[Afwijkend aantal]) / 'Routetransacties'[Totale gemengde hoeveelheid]) \* 1000000) |
| Verwerkte hoeveelheid       | SUM('Routetransacties'[Hoeveelheid goed]) + SUM('Routetransacties'[Afwijkend aantal]) |
| Totale gemengde hoeveelheid     | SUM('Productieorder'[Hoeveelheid goed]) + SUM('Routetransacties'[Afwijkend aantal]) |

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

## <a name="additional-resources"></a>Aanvullende resources

Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

- [Gegevensentiteiten](https://ax.help.dynamics.com/en/wiki/data-entities/)
- [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Power BI-tegels toevoegen aan werkruimten](http://ax.help.dynamics.com/en/wiki/configuring-powerbi-integration/)
