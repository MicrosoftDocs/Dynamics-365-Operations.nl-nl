---
title: Power BI-inhoud voor analyse van inkoopuitgaven
description: In dit onderwerp wordt beschreven wat is opgenomen in de Power BI-inhoud Analyse inkoopuitgaven. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot rapporten in de inhoud en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee de inhoud is samengesteld.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 07b6f433a8355d7f9ed6dce8e26f78d38a86a713
ms.contentlocale: nl-nl
ms.lasthandoff: 12/18/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI-inhoud Analyse inkoopuitgaven

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat is opgenomen in de Microsoft Power BI-inhoud **Analyse inkoopuitgaven**. In dit onderwerp wordt uitgelegd hoe u toegang krijgt tot de Power BI-rapporten en wordt informatie gegeven over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Analyse inkoopuitgaven** is ontworpen om inkoopmanagers en managers met budgetverantwoordelijkheid te helpen de inkoopuitgaven in de gaten te houden. Managers kunnen inkoopuitgaven op de volgende manieren analyseren:

-   Inkoop jaar tot heden (op leveranciersgroep en afzonderlijke leveranciers, aanschaffingscategorie en afzonderlijke producten en locatie van de leverancier)
-   Wijzigingen jaar tot jaar in inkoop (op leveranciersgroep en aanschaffingscategorie)

Op basis van gegevens voor inkooptransacties biedt de inhoud zowel een samengevoegde weergave van de inkoopcijfers uit het hele bedrijf als ook een analyse van de inkoopuitgaven op leverancier en product. Rapporten maken wijzigingen in de inkoopuitgaven in het verloop van de tijd duidelijk. Daarom kunnen de rapporten worden gebruikt om managers te wijzen op positieve en negatieve trends in de uitgaven voor afzonderlijke leveranciers en producten. Daarnaast geven grafieken de inkoopuitgaven weer voor verschillende inkoopcategorieën en leveranciersgroepen. Categorie- en regiomanagers kunnen met deze grafieken veranderingen in het uitgavegedrag opsporen.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
De Power BI-inhoud **Inkoopuitgavenanalyse** wordt weergegeven op de pagina **Inkoop- en uitgavenanalyse** (**Inkoopbeheer** > **Query's en rapporten** > **Inkoopprestatieanalyse** > **Inkoop- en uitgavenanalyse**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
De Power BI-inhoud **Analyse inkoopuitgaven** bevat een rapport dat uit een verzameling van metrische gegevens bestaat. Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen. In de volgende tabel vindt u een overzicht van de visualisaties.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Rapportpagina</th>
<th>Diagrammen</th>
<th>Tegels</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Inkoop op leverancier</td>
<td><ul>
<li>Top 10-leveranciers op inkoop (gestapeld staafdiagram)</li>
<li>Totale inkoop op groep / land / naam leverancier (cirkeldiagram)</li>
<li>Inkoop op groep / land / naam leverancier (kolomdiagram)</li>
<li>Gemiddelde inkoop op groep / land / naam leverancier (kolomdiagram)</li>
</ul></td>
<td><ul>
<li>Totaalinkoop</li>
<li>Inkoopgroei jaar-op-jaar</li>
<li>Totaal aantal leveranciers</li>
<li>Totaal aantal actieve leveranciers</li>
</ul></td>
</tr>
<tr class="even">
<td>Inkoop op product</td>
<td><ul>
<li>Inkoop per aanschaffingscategorie / productnaam (kolomdiagram)</li>
<li>Totale inkoop per aanschaffingscategorie / productnaam (cirkeldiagram)</li>
<li>Top 10-producten op inkoop (gestapeld staafdiagram)</li>
</ul></td>
<td><ul>
<li>Totaal aantal producten</li>
<li>Totaal aantal actieve producten percentage van totale aantal producten</li>
<li>Aantal producten dat 80% van inkoop oplevert</li>
</ul></td>
</tr>
<tr class="odd">
<td>Inkoop op periode*</td>
<td><ul>
<li>Inkoop op maand / dag (kolomdiagram)</li>
<li>Cumulatieve inkoop afwijking jaar-op-jaar (watervalgrafiek)</li>
<li>Totale inkoop groei jaar-op-jaar (kolomdiagram)</li>
<li>Inkoopoverzicht (matrix)</li>
</ul></td>
<td><ul>
<li>Inkoopgroei jaar-op-jaar</li>
<li>Inkoopgroei jaar-op-jaar %</li>
</ul></td>
</tr>
<tr class="even">
<td>Inkoop op leverancierlocatie</td>
<td><ul>
<li>Inkoop op stad</li>
<li>Inkoop groei jaar-op-jaar %</li>
<li>Inkoop op land</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Analyse inkoopuitgaven op tijd</td>
<td><ul>
<li>Inkoop huidige jaar op maand / dag (lijndiagram)</li>
<li>Inkooporders huidig en vorig jaar (lijn- en kolomdiagram)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Analyse inkoopuitgaven op leverancier</td>
<td><ul>
<li>Top 10 leverancier inkoop % van inkoop (trechterdiagram)</li>
<li>Top 10 leveranciers met een gestegen uitgaven jaar-op-jaar</li>
<li>Top 10 leveranciers met een gedaalde uitgaven jaar-op-jaar</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Inkoop dit jaar en vorig jaar en groei per aanschaffingscategorie

## <a name="data-model-and-entities"></a>Gegevensmodel en entiteiten
De volgende gegevens wordt gebruikt om de rapportpagina's in de Power BI-inhoud **Analyse inkoopuitgaven** te vullen. Deze gegevens worden vertegenwoordigd door samengevoegde metingen die zijn klaargezet in de entiteitopslag. De entiteitopslag is een Microsoft SQL Server-database die is geoptimaliseerd voor analyses. Zie voor meer informatie [Overzicht Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md).

De samengevoegde metingen in deze inhoud zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Inkoop-cube in Microsoft Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3. Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken. Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Overzicht van Power BI-integratie met Entiteitopslag](power-bi-integration-entity-store.md). De volgende belangrijke samengevoegde metingen zijn rechtstreeks vanuit de entiteit Factuurregels beschikbaar en worden gebruikt als basis voor de inhoud.

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

