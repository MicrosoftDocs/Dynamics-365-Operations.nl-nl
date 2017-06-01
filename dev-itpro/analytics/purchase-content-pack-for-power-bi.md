---
title: Power BI-inhoud voor analyse van inkoopuitgaven
description: In dit onderwerp wordt beschreven wat het inhoudpakket voor analyse van inkoopuitgaven voor Microsoft Power BI-bevat. In dit onderwerp wordt uitgelegd hoe u toegang kunt krijgen tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ad0ee95113d05710cccc1a5e9d215b38244c2047
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI-inhoud voor analyse van inkoopuitgaven

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven wat het inhoudpakket voor analyse van inkoopuitgaven voor Microsoft Power BI-bevat. In dit onderwerp wordt uitgelegd hoe u toegang kunt krijgen tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.

<a name="overview"></a>Overzicht
--------

Het inhoudpakket voor analyse van inkoopuitgaven voor Microsoft Power BI is gemaakt voor inkoopmanagers en managers die verantwoordelijk voor budgetten zijn. Het is bedoeld om hen te helpen de uitgaven voor inkoop in de gaten te houden. Op basis van gegevens voor inkooptransacties uit Microsoft Dynamics 365 for Operations biedt het zowel een samengevoegde weergave van de inkoopcijfers uit het hele bedrijf en een analyse van de inkoopuitgaven op leverancier en product. Rapporten maken wijzigingen in de inkoopuitgaven in het verloop van de tijd duidelijk. Daarom kunnen ze worden gebruikt om managers te wijzen op positieve en negatieve trends in de uitgaven voor afzonderlijke leveranciers en producten. Grafieken geven de inkoopuitgaven weer voor verschillende inkoopcategorieën en leveranciersgroepen. Categorie- en regiomanagers vinden deze grafieken mogelijk nuttig wanneer zij wijzigingen in de uitgaven willen opsporen. Het inhoudspakket geeft inkoopmanagers en managers die verantwoordelijk voor budgetten zijn de mogelijkheid om inkoopuitgaven op de volgende manieren te analyseren:

-   Inkoop jaar tot heden (op leveranciersgroep en afzonderlijke leveranciers, aanschaffingscategorie en afzonderlijke producten en locatie van de leverancier)
-   Wijzigingen jaar tot jaar in inkoop (op leveranciersgroep en aanschaffingscategorie)

## <a name="accessing-the-content-pack"></a>Toegang tot het inhoudpakket
Het inhoudpakket voor analyse van inkoopuitgaven wordt gepubliceerd als een implementatieactivum in Microsoft Dynamics Lifecycle Services (LCS). U hebt er toegang toe vanuit Microsoft Dynamics 365 for Operations. Zie voor meer informatie over toegang tot en het openen van Power BI-rapporten [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).
Opmerking: KB 4011327 is een vereiste voor deze Power BI-inhoud. Nadat u zich bij Lifecycle Services hebt aangemeld, kunt u de KB hier openen: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="metrics-that-are-included-in-the-content-pack"></a>Metrische gegevens die zijn opgenomen in het inhoudpakket
Het inhoudpakket voor analyse van inkoopuitgaven bevat een rapport dat uit een verzameling van metrische gegevens bestaat. Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen. In de volgende tabel vindt u een overzicht van de visualisaties die in het inhoudpakket worden gebruikt.

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
Gegevens uit Dynamics 365 for Operations worden gebruikt voor het rapport in het inhoudpakket voor analyse van inkoopuitgaven. Deze gegevens worden vertegenwoordigd als samengevoegde metingen die worden klaargezet in de Entiteitopslag. Dit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Zie voor meer informatie over de Entiteitopslag het blog-artikel [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De samengevoegde metingen in dit inhoudpakket zijn de subset van de geaggregeerde metingen die beschikbaar waren in de Inkoop-cube in Microsoft Microsoft Dynamics AX 2012 en Microsoft Dynamics AX 2012 R3. Om de samengevoegde metingen uit de cube in de Entiteitopslag klaar te zetten, moet u ze implementeerbaar maken. Zie voor meer informatie hierover de procedure voor het klaarzetten van samengevoegde metingen in de Entiteitopslag in het blog-artikel [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De volgende belangrijke samengevoegde metingen zijn rechtstreeks vanuit de entiteit Factuurregels beschikbaar en worden gebruikt als basis voor het inhoudpakket.

| Entiteit        | Belangrijke samengevoegde metingen | Gegevensbron voor Dynamics 365 for Operations | Veld              | Omschrijving                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Factuurregels | Inkoop                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Het bedrag in de valuta voor de boekhouding. |

De volgende tabel toont de belangrijkste metingen die worden berekend in het inhoudpakket op basis van de entiteit Factuurregels.

| Maat               | Berekening                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Inkoop huidig jaar | Inkoop huidig jaar = SUM('Factuurregels\[Inkoop\])                                            |
| Inkoop vorig jaar    | Inkoop vorig jaar = CALCULATE(SUM('Factuurregels\[Inkoop\]), SAMEPERIODLASTYEAR(Datums\[Datum\])) |
| Inkoopgroei jaar-op-jaar   | Groei inkoop jaar-op-jaar = \[Inkoop huidig jaar\] - \[Inkoop vorig jaar\]                            |

De volgende belangrijke dimensies in het inhoudpakket worden gebruikt als filters voor het segmenteren van de samengevoegde metingen, zodat u een grotere mate van granulatie en analytischere inzichten kunt bereiken.

| Entiteit                 | Voorbeelden van kenmerken                                |
|------------------------|-------------------------------------------------------|
| Leveranciers                | Leveranciersgroepen, Land/regio van leverancier, Leveranciersnaam |
| Producten               | Productnummer, Productnaam, Naam van artikelengroep        |
| Inkoopcategorieën | Aanschaffingscategorie, namen van Aanschaffingscategorieën      |
| Rechtspersonen         | Rechtspersoonnaam                                     |
| Datums                  | Datums, Jaarverschuiving                                    |

Standaard worden gegevens in het inhoudpakket weergegeven voor het huidige kalenderjaar. U kunt echter het datumfilter in de sectie rapportfilters wijzigen. U kunt ook het bedrijfsfilter wijzigen.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)





