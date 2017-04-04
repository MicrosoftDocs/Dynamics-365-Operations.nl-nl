---
title: Verkoop- en winstgevendheid prestaties Power BI-inhoud
description: Dit onderwerp wordt beschreven wat wordt opgenomen in de Dynamics 365 for Operations - verkoop- en winstgevendheid prestaties content pack voor Microsoft Power BI. Het wordt uitgelegd hoe u toegang tot de rapporten die zijn opgenomen in de content pack en biedt informatie over het gegevensmodel en entiteiten die worden gebruikt voor het bouwen van de content pack.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Verkoop- en winstgevendheid prestaties Power BI-inhoud

Dit onderwerp wordt beschreven wat wordt opgenomen in de Dynamics 365 for Operations - verkoop- en winstgevendheid prestaties content pack voor Microsoft Power BI. Het wordt uitgelegd hoe u toegang tot de rapporten die zijn opgenomen in de content pack en biedt informatie over het gegevensmodel en entiteiten die worden gebruikt voor het bouwen van de content pack.

<a name="overview"></a>Overzicht
--------

Deze content pack is voor verkoopmanagers controleren van de belangrijkste meetwaarden voor de verkoop van opbrengsten, brutowinst en winstmarge gemaakt. Deze Verkoop transactionele gegevens uit Dynamics 365 gebruikt voor bewerkingen en geeft zowel een samengevoegde weergave van de verkoopcijfers van bedrijfs- en een onderverdeling van verkoopprestaties voor klanten en producten. Wijzigingen in de groei van de opbrengsten en winsten na verloop van tijd markeren, kunnen rapporten worden gebruikt voor waarschuwingen managers over positieve en negatieve trends voor afzonderlijke klanten en producten. Categorie en regiomanagers wordt nuttig zijn om inkomsten en rentabiliteit van verschillende productcategorieën en klantengroepen om Laatkomer en leiders met elkaar vergeleken. Een uitgebreid rapport die worden uitgezet winstmarge aanbiedingen accountmanagers omzet van individuele klant een back basis om hun inspanningen verkoop en marketing attune aan het desbetreffende profiel van elke klant. De verkoop- en winstgevendheid prestaties content pack kan managers verkoop Verkoopprestaties per te analyseren:

-   Opbrengst, jaar tot heden (per klantengroep en individuele klanten, verkoopcategorieën, en afzonderlijke producten en regio's)
-   Omzet-wijziging, jaar tot jaar (per categorie van klant regio's en verkoop)

Winstgevendheid kan worden geanalyseerd met:

-   De brutowinst en winstmarge (door klantengroepen en verkoop productcategorieën)
-   Brutowinst wijziging, jaar tot jaar
-   Winstgevendheid klant (per opbrengst versus brutomarge)

## <a name="accessing-the-content-pack"></a>Toegang tot de content pack
De verkoop- en winstgevendheid prestaties Power BI content pack wordt gepubliceerd als een activum implementatie in Lifecycle Services (LCS) en toegankelijk is vanuit Dynamics 365 voor bewerkingen. Zie voor meer informatie over het openen en Power BI rapporten starten [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Prestatiegegevens die zijn opgenomen in de content pack
De inhoud pack bevat een rapport dat uit een set parameters die worden weergegeven als diagrammen, tegels en tabellen bestaat. De volgende tabel bevat een overzicht van de visualisations in de content pack.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Rapportpagina.**        | **Charts**                                 | **Naast elkaar**                                               |
| Omzet per klant    | Top 10-klanten op omzet                | Totale opbrengst                                           |
|                        | Totale omzet per klantgroep            | YOY opbrengststijging                                      |
|                        | Klant gemiddelde omzet per klantgroep | Brutomarge                                            |
|                        | Opbrengst & brutowinst per klantengroep   |                                                         |
| Omzet per product     | Opbrengst & brutowinst per verkoopcategorie   | Totale \#van producten                                    |
|                        | Top 10 producten op basis van opbrengst                 | Totale aantal actieve producten en percentage van totaal |
|                        | Totale opbrengsten per verkoopcategorie            | Aantal producten dat 80% opbrengst verantwoorden           |
| Opbrengsten per periode\*    | Omzet per maand                           | YOY opbrengststijging                                      |
|                        | Aan het einde opbrengst afwijking, YOY             | YOY opbrengst groei %                                    |
|                        | Afwijking in de totale verkoop per regio van de klant    |                                                         |
| Omzet per locatie    | Omzet per plaats                      |                                                         |
|                        | YOY opbrengst groei %                       |                                                         |
|                        | Omzet per regio                    |                                                         |
| Winstgevendheid klant | Brutomarge versus omzet per klant   | Brutowinst, brutomarge, zowel wat inkomstenstijging YOY          |
| Rentabiliteitsanalyse | Opbrengst en brutowinst per maand          |                                                         |
|                        | Belangrijkste 15 klanten op brutomarge           |                                                         |
|                        | Brutowinst per maand, YOY                 |                                                         |

\*Opbrengst dit en laatste jaar en groei per verkoopcategorie.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Dynamics 365 voor bewerkingen gegevens wordt gebruikt voor het vullen van het rapport in de verkoop- en winstgevendheid prestaties content pack. Deze omgeving wordt voorgesteld als statistische metingen die worden klaargezet in het archief entiteit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Lees meer over in de blog [Power BI-integratie met entiteit winkel in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De statistische metingen in deze content pack zijn de subset van de statistische metingen die beschikbaar in de kubus Sales in Dynamics AX 2012 en AX 2012 R3 waren. Het voorbereiden van statistische metingen van de cube in de winkel entiteit moet u doen gebruiken. Zie de procedure voor meer informatie over het klaarzetten van statistische metingen in het archief van de entiteit in de blog [Power BI-integratie met entiteit winkel in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De volgende belangrijke statistische metingen van de factuur regels entiteit worden gebruikt als basis voor de content pack.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Belangrijke statistische metingen**               | **Gegevensbron voor Dynamics 365 for Operations** | **Field**                                    | **Description**                          |
| Factuurregels | Opbrengst                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Bedrag in valuta voor boekhouding            |
|               | Kosten van verkochte goederen                           | InventTrans                                     | SOM (CostAmountPosted + CostAmountAdjustment) | Kostprijs + correctie                 |
|               | Provisieregelbedrag-valuta voor boekhouding | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Het provisiebedrag in valuta voor boekhouding |

De volgende tabel toont de belangrijkste statistische metingen van de factuur regels entiteit die worden gebruikt voor verschillende berekende eenheden maken in de content pack gegevensset.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Berekend als**                                                                                |
| Brutowinst      | SOM (opbrengst: COGS: Commissie – btw (opgenomen in klantfactuurregelbedrag))          |
| Brutomarge      | SOM (brutowinst / (opbrengst - btw (opgenomen in klantfactuurregelbedrag)))             |
| Opbrengst vorig jaar | Opbrengst vorig jaar = berekenen (som ('factuurregels\[opbrengsten\]), SAMEPERIODLASTYEAR (datums\[datum\]) |

De volgende belangrijke dimensies in de **Verkoop-cube** worden gebruikt als filters voor de statistische metingen een grotere mate van granulatie en meer analytische inzicht segmenteren.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Voorbeelden van kenmerken**                           |
| Klanten            | Klantengroepen, klant-regio's, adres, de industrie |
| Producten         | Productnummer, productnaam, de naam van de groepen voor artikel       |
| Verkoopcategorieën | Verkoopcategorie namen                                 |
| Rechtspersonen   | Namen van de rechtspersoon                                   |
| Datums            | Datums                                                |

Standaard de content pack worden gegevens weergegeven voor het huidige kalenderjaar, maar u kunt de filters rapportsectie openen en het datumfilter wijzigen. U kunt ook de Bedrijfsfilter wijzigen.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)



