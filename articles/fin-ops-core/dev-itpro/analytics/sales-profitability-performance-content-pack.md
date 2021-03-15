---
title: Power BI-inhoud Verkoop- en winstgevendheidsprestaties
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Verkoop- en winstgevendheidsprestaties.
author: ShylaThompson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7aafaa4c974f6b72e78f870eceb266fd0ef71900
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093558"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>Power BI-inhoud Verkoop- en winstgevendheidsprestaties

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Verkoop- en winstgevendheidsprestaties**. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** is opgesteld zodat verkoopmanagers de belangrijkste verkoopmeetwaarden, namelijk opbrengst, brutowinst en winstmarge, kunnen controleren. Op basis van gegevens voor verkooptransacties biedt het zowel een samengevoegde weergave van de verkoopcijfers uit het hele bedrijf als ook een analyse van de verkoopprestaties voor klanten en producten.

Rapporten markeren wijzigingen in opbrengst en winst die in de loop van de tijd optreden. Daarom kunnen de rapporten worden gebruikt om managers te wijzen op positieve en negatieve trends voor afzonderlijke klanten en producten. Bovendien vergelijken diagrammen de inkomsten en winstgevendheid van de verschillende productcategorieën en klantengroepen met elkaar. Zo kunnen categorie- en regiomanagers achterblijvers en leiders identificeren. Tenslotte geeft een uitgebreid rapport de omzet van een individuele klant ten opzichte van de winstmarge weer. Accountmanagers hebben daarmee een fundament op basis van gegevens, waarmee ze hun inspanningen voor verkoop en marketing op het profiel van elke klant kunnen afstemmen.

Met het inhoudpakket **Verkoop- en winstgevendheidprestaties** kunnen verkoopmanagers verkoopprestaties analyseren op de volgende manieren:

- Opbrengst, boekjaar tot heden (op klantengroep en individuele klanten, verkoopcategorieën en afzonderlijke producten en regio's)
- Opbrengstwijziging, jaar op jaar (op klantenregio en verkoopcategorieën)

Winstgevendheid kan worden geanalyseerd op de volgende manieren:

- Brutowinst en winstmarge (op klantengroepen en categorieën van productverkoop)
- Wijziging brutowinst wijziging, jaar op jaar
- Winstgevendheid klant (op opbrengst versus brutomarge)

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud
De Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** wordt weergegeven op de pagina **Verkoop- en winstgevendheidsprestaties** (**Verkoop en marketing** \> **Query's en rapporten** \> **Verkoopprestatieanalyse** \> **Verkoop- en winstgevendheidsprestaties**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
De Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** bevat een rapport dat uit een verzameling van metrische gegevens bestaat. Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen. In de volgende tabel vindt u een overzicht van de visualisaties die in de inhoud worden gebruikt.

| Rapportpagina            | Diagrammen                                     | Tegels                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Opbrengst op klant    | Top 10-klanten op opbrengst                | Totale opbrengst                                           |
|                        | Totale opbrengst op klantgroep            | Opbrengststijging jaar-op-jaar                                      |
|                        | Gemiddelde omzet van klanten, op klantgroep | Brutomarge                                            |
|                        | Opbrengst & brutowinst op klantengroep   |                                                         |
| Opbrengst op product     | Opbrengst & brutowinst op verkoopcategorie   | Totaal aantal producten                                    |
|                        | Top 10-producten op opbrengst                 | Totaal aantal actieve producten en percentage van totaal |
|                        | Totale opbrengst op verkoopcategorie            | Aantal producten dat 80% van opbrengst oplevert           |
| Opbrengste op periode\*    | Opbrengst per maand                           | Opbrengststijging jaar-op-jaar                                      |
|                        | Achterblijvende opbrengstafwijking, jaar-op-jaar             | % opbrengststijging jaar-op-jaar                                    |
|                        | Totale verkoopafwijking op klantregio    |                                                         |
| Opbrengst op locatie    | Verkoopopbrengst op plaats                      |                                                         |
|                        | % opbrengststijging jaar-op-jaar                       |                                                         |
|                        | Verkoopopbrengst op regio                    |                                                         |
| Winstgevendheid klant | Brutomarge versus opbrengst, op klant   | Brutowinst, brutomarge, opbrengstgroei jaar-op-jaar          |
| Rentabiliteitsanalyse | Opbrengst en brutowinst per maand          |                                                         |
|                        | Top 15-klanten op brutomarge           |                                                         |
|                        | Brutowinst per maand, jaar-op-jaar                 |                                                         |

\* Opbrengst dit jaar en vorig jaar en groei per verkoopcategorie.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
De volgende gegevens worden gebruikt om de rapportpagina's in de Power BI-inhoud **Verkoop- en winstgevendheidsprestaties** te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

De samengevoegde metingen in dit inhoudpakket zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Verkoop-cube in Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3. Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken. Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Power BI-integratie met entiteitopslag in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/).

De volgende belangrijke samengevoegde metingen van de entiteit Factuurregels worden gebruikt als basis voor de inhoud.

| Entiteit        | Belangrijke samengevoegde metingen                   | Gegevensbron voor Dynamics 365 | Veld                                        | Omschrijving                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| Factuurregels | Opbrengst                                      | CustInvoiceTrans             | SUM(LineAmountMST)                           | Het bedrag in de valuta voor boekhouding.            |
|               | Kosten van verkochte goederen                           | InventTrans                  | SUM(CostAmountPosted + CostAmountAdjustment) | De som van het kostenbedrag en de correctie.    |
|               | Provisieregelbedrag – valuta voor boekhouding | CustInvoiceTrans             | SUM(CommissAmountMST)                        | Het provisiebedrag in de boekhoudvaluta. |

In de volgende tabel ziet u de belangrijkste samengevoegde metingen van de entiteit Factuurregel die worden gebruikt om verschillende berekende eenheden te maken in de gegevensset van de inhoud.

| Maat           | Berekening                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Brutowinst      | SUM(Opbrengst – COGS – Provisie – btw (opgenomen in bedrag klantfactuurregel))          |
| Brutomarge      | SUM(Brutowinst / (Opbrengst - btw (opgenomen in bedrag klantfactuurregel)))             |
| Opbrengst vorig jaar | Opbrengst vorig jaar = CALCULATE(SUM('Factuurregels\[Opbrengst\]), SAMEPERIODLASTYEAR(Datums\[Datum\])) |

De volgende belangrijke dimensies in de Verkoop-cube worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.

| Entiteit           | Voorbeelden van kenmerken                               |
|------------------|------------------------------------------------------|
| Klanten        | Klantengroepen, klantregio's, adressen, bedrijfstak |
| Producten         | Productnummer, Productnaam, Naam van artikelengroep       |
| Verkoopcategorieën | Namen verkoopcategorieën                                 |
| Rechtspersonen   | Namen rechtspersonen                                   |
| Datums            | Datums                                                |

Standaard worden gegevens in de inhoud weergegeven voor het huidige kalenderjaar. U kunt echter het datumfilter in de sectie rapportfilters wijzigen. U kunt ook het bedrijfsfilter wijzigen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]