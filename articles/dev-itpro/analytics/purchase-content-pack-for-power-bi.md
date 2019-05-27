---
title: Power BI-inhoud - inkoop- en uitgavenanalyse
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Analyse inkoopuitgaven. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3206573022c0f843b07a468987a112ca6ac435ef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1527712"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI-inhoud - inkoop- en uitgavenanalyse

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud **Analyse inkoopuitgaven**. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Inkoopuitgavenanalyse** is ontworpen om inkoopmanagers en managers met budgetverantwoordelijkheid te helpen de inkoopuitgaven bij te houden. Managers kunnen inkoopuitgaven op de volgende manieren analyseren:

- Inkoop jaar tot heden (op leveranciersgroep en afzonderlijke leveranciers, aanschaffingscategorie en afzonderlijke producten en locatie van de leverancier)
- Wijzigingen jaar tot jaar in inkoop (op leveranciersgroep en aanschaffingscategorie)

Op basis van gegevens voor inkooptransacties biedt de inhoud zowel een samengevoegde weergave van de inkoopcijfers uit het hele bedrijf als ook een analyse van de inkoopuitgaven op leverancier en product. Rapporten maken wijzigingen in de inkoopuitgaven in het verloop van de tijd duidelijk. Daarom kunnen de rapporten worden gebruikt om managers te wijzen op positieve en negatieve trends in de uitgaven voor afzonderlijke leveranciers en producten. Daarnaast geven grafieken de inkoopuitgaven weer voor verschillende inkoopcategorieën en leveranciersgroepen. Categorie- en regiomanagers kunnen met deze grafieken veranderingen in het uitgavegedrag opsporen.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud
De Power BI-inhoud **Analyse inkoopuitgaven** wordt weergegeven op de pagina **Inkoop- en uitgavenanalyse** (**Inkoopbeheer** \> **Query's en rapporten** \> **Inkoopprestatieanalyse** \> **Inkoop- en uitgavenanalyse**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
Het Power BI-inhoudpakket **Analyse inkoopuitgaven** bevat een rapport dat uit een verzameling van metrische gegevens bestaat. Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen. 

De volgende secties bieden een overzicht van de visualisaties.

### <a name="purchase-by-vendor-report-page"></a>Pagina Inkoop op leverancier (rapport)
**Diagrammen**
- Top 10-leveranciers op inkoop (gestapeld staafdiagram)
- Totale inkoop op groep / land / naam leverancier (cirkeldiagram)
- Inkoop op groep / land / naam leverancier (kolomdiagram)
- Gemiddelde inkoop op groep / land / naam leverancier (kolomdiagram)

**Tegels**
- Totaalinkoop
- Inkoopgroei jaar-op-jaar
- Totaal aantal leveranciers
- Totaal aantal actieve leveranciers

**Voorbeeld:**
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Pagina Inkoop op product (rapport)

**Diagrammen**
- Inkoop per aanschaffingscategorie / productnaam (kolomdiagram)
- Totale inkoop per aanschaffingscategorie / productnaam (cirkeldiagram)
- Top 10-producten op inkoop (gestapeld staafdiagram)

**Tegels**
- Totaal aantal producten</li>
- Totaal aantal actieve producten percentage van totale aantal producten
- Aantal producten dat 80% van inkoop oplevert

**Voorbeeld:**


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Pagina Inkoop op periode (rapport)
Deze pagina geeft inkopen van dit jaar en vorig jaar en groei per aanschaffingscategorie weer.

**Diagrammen** 
- Inkoop op maand / dag (kolomdiagram)
- Cumulatieve inkoop afwijking jaar-op-jaar (watervalgrafiek)
- Totale inkoop groei jaar-op-jaar (kolomdiagram)
- Inkoopoverzicht (matrix)

**Tegels**
- Inkoopgroei jaar-op-jaar
- Inkoopgroei jaar-op-jaar %

**Voorbeeld:**
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Pagina Inkoop op leverancierslocatie (rapport)

**Diagrammen**
- Inkoop op stad
- Inkoop groei jaar-op-jaar %
- Inkoop op land

**Voorbeeld:**
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Pagina Analyse inkoopuitgaven op tijd (rapport)

**Diagrammen** 
- Inkoop huidige jaar op maand / dag (lijndiagram)
- Inkooporders huidig en vorig jaar (lijn- en kolomdiagram)

**Voorbeeld:**
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Pagina Analyse inkoopuitgaven op leverancier (rapport)

**Diagrammen** 
- Top 10 leverancier inkoop % van inkoop (trechterdiagram)
- Top 10 leveranciers met een gestegen uitgaven jaar-op-jaar
- Top 10 leveranciers met een gedaalde uitgaven jaar-op-jaar

**voorbeeld** 
<img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Gegevensmodel en entiteiten
De volgende gegevens worden gebruikt om de rapportpagina's in de Power BI-inhoud **Analyse inkoopuitgaven** te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

De samengevoegde metingen in dit inhoudpakket zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Inkoop-cube in Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3. Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken. Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Overzicht van Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md). De volgende belangrijke samengevoegde metingen zijn rechtstreeks vanuit de entiteit Factuurregels beschikbaar en worden gebruikt als basis voor de inhoud.

| Entiteit        | Belangrijke samengevoegde metingen | Gegevensbron                                 | Veld              | Omschrijving                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Factuurregels | Inkoop                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Het bedrag in de valuta voor boekhouding. |

De volgende tabel toont de belangrijkste metingen in de inhoud die worden berekend op basis van de entiteit Factuurregels.

| Maat               | Berekening                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Inkoop huidig jaar | Inkoop huidig jaar = SUM('Factuurregels\[Inkoop\])                                            |
| Inkoop vorig jaar    | Inkoop vorig jaar = CALCULATE(SUM('Factuurregels\[Inkoop\]), SAMEPERIODLASTYEAR(Datums\[Datum\])) |
| Inkoopgroei jaar-op-jaar   | Groei inkoop jaar-op-jaar = \[Inkoop huidig jaar\] - \[Inkoop vorig jaar\]                            |

De volgende belangrijke dimensies in de inhoud worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.

| Entiteit                 | Voorbeelden van kenmerken                                |
|------------------------|-------------------------------------------------------|
| Leveranciers                | Leveranciersgroepen, Land/regio van leverancier, Leveranciersnaam |
| Producten               | Productnummer, Productnaam, Naam van artikelengroep        |
| Inkoopcategorieën | Aanschaffingscategorie, namen van Aanschaffingscategorieën      |
| Rechtspersonen         | Rechtspersoonnaam                                     |
| Datums                  | Datums, Jaarverschuiving                                    |

Standaard worden gegevens in de inhoud weergegeven voor het huidige kalenderjaar. U kunt echter het datumfilter in de sectie rapportfilters wijzigen. U kunt ook het bedrijfsfilter wijzigen.
