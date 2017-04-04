---
title: Opdracht uitgavenanalyse Power BI-inhoud
description: Dit onderwerp wordt beschreven wat wordt opgenomen in de inkoop besteedt analyse content pack voor Microsoft Power BI. Deze wordt uitgelegd hoe u toegang tot de rapporten die zijn opgenomen in de content pack en informatie over het gegevensmodel en entiteiten die worden gebruikt voor het bouwen van de content pack.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Opdracht uitgavenanalyse Power BI-inhoud

Dit onderwerp wordt beschreven wat wordt opgenomen in de inkoop besteedt analyse content pack voor Microsoft Power BI. Deze wordt uitgelegd hoe u toegang tot de rapporten die zijn opgenomen in de content pack en informatie over het gegevensmodel en entiteiten die worden gebruikt voor het bouwen van de content pack.

<a name="overview"></a>Overzicht
--------

De inkoop uitgavenanalyse content pack voor Microsoft Power BI voor managers en managers die verantwoordelijk voor budgetten zijn inkoop is gemaakt. Het is ontworpen voor deze opdracht uitgaven in de gaten houden. Deze opdracht transactionele gegevens uit Microsoft Dynamics 365 gebruikt voor bewerkingen en geeft een samengevoegde weergave van het hele bedrijf aankoopcijfers zowel een onderverdeling van uitgaven per leverancier en product inkoop. Rapporten markeren wijzigingen in inkoop uitgaven na verloop van tijd. Daarom kunnen ze worden gebruikt voor waarschuwingen managers over positieve en negatieve uitgavenlimiet trends voor afzonderlijke leveranciers en producten. Grafieken weergeven opdracht uitgaven voor verschillende aanschaffingscategorieën en leveranciersgroepen. Categorie en regiomanagers kunnen nuttig zijn deze diagrammen gebruiken om vast te stellen van wijzigingen in gedrag uitgaven. Het inhoudspakket we inkoopmanagers en managers die verantwoordelijk voor budgetten zijn analyseren opdracht uitgaven in de volgende manieren:

-   Jaar tot heden-inkoop (per leveranciersgroep en afzonderlijke leveranciers, aanschaffingscategorie en afzonderlijke producten en locatie van de leverancier)
-   Jaar tot jaar opdracht wijzigen (op leverancier groeperen en aanschaffingscategorieën categorie)

## <a name="accessing-the-content-pack"></a>Toegang tot de content pack
De inkoop uitgavenanalyse content pack wordt gepubliceerd als een activum implementatie in Microsoft Dynamics Lifecycle Services (LCS) en kunt u vanuit Microsoft Dynamics 365 voor bewerkingen. Zie voor meer informatie over het benaderen en openen Power BI-rapporten, [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Prestatiegegevens die zijn opgenomen in de content pack
De inkoop uitgavenanalyse content pack bevat een rapport dat uit een verzameling van prestatiegegevens bestaat. Deze gegevens worden weergegeven als diagrammen, tegels en tabellen. De volgende tabel bevat een overzicht van de visualisaties in de content pack.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Rapportpagina.</th>
<th>Diagrammen</th>
<th>Naast elkaar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Inkoop per leverancier</td>
<td><ul>
<li>Top 10-leveranciers door inkoop (gestapeld staafdiagram)</li>
<li>Totale inkoop op leverancier groeperen / land / -naam (cirkeldiagram)</li>
<li>Inkoop op leverancier groeperen / land / -naam (kolomdiagram)</li>
<li>Gemiddelde inkoop op leverancier groeperen / land / -naam (kolomdiagram)</li>
</ul></td>
<td><ul>
<li>Totaalinkoop</li>
<li>YOY inkoop groei</li>
<li>Totaal aantal leveranciers</li>
<li>Totaal aantal actieve leveranciers</li>
</ul></td>
</tr>
<tr class="even">
<td>Inkoop per product</td>
<td><ul>
<li>Inkoop per aanschaffingscategorie / productnaam (kolomdiagram)</li>
<li>Totaal inkoop per aanschaffingscategorie / productnaam (cirkeldiagram)</li>
<li>Top 10 producten door inkoop (gestapeld staafdiagram)</li>
</ul></td>
<td><ul>
<li>Totaal aantal producten</li>
<li>Totaal aantal actieve producten percentage van het totale aantal producten</li>
<li>Aantal producten accounting voor 80% inkoop</li>
</ul></td>
</tr>
<tr class="odd">
<td>Inkoop per periode *</td>
<td><ul>
<li>Inkoop per maand / dag (kolomdiagram)</li>
<li>Cumulatieve YOY Inkoopverschil (waterval grafiek)</li>
<li>Totale inkoop YOY groei (kolomdiagram)</li>
<li>Inkoop-instructie (matrix)</li>
</ul></td>
<td><ul>
<li>YOY inkoop groei</li>
<li>YOY inkoop groei %</li>
</ul></td>
</tr>
<tr class="even">
<td>Inkoophoeveelheid op de locatie van de leverancier</td>
<td><ul>
<li>Inkoop per plaats</li>
<li>Opdracht YOY groei %</li>
<li>Inkoop per land</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Opdracht uitgavenanalyse op tijd</td>
<td><ul>
<li>Opdracht huidige jaar per maand / dag (lijndiagram)</li>
<li>Inkooporders Huidig en vorig jaar (regel- en -grafiek)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Opdracht uitgavenanalyse per leverancier</td>
<td><ul>
<li>Top 10 leverancier opdracht % van de opdracht (ongebruikte)</li>
<li>Top 10 van leveranciers met een hogere uitgavenlimiet YOY</li>
<li>Top 10 van leveranciers met een kleinere uitgavenlimiet YOY</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Inkoop dit jaar en vorig jaar en groei per aanschaffingscategorie

## <a name="data-model-and-entities"></a>Gegevensmodel en entiteiten
Dynamics 365 voor bewerkingen die gegevens wordt gebruikt voor het rapport in de opdracht analyse content pack uitgeven. Deze gegevens wordt vertegenwoordigd door statistische metingen die worden klaargezet in het archief entiteit is een Microsoft SQL-database die is geoptimaliseerd voor analyses. Zie voor meer informatie over de winkel entiteit, de [Power BI-integratie met entiteit winkel in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog-update. De statistische metingen in deze content pack zijn de subset van statistische metingen die beschikbaar in de inkoop-Cube in Microsoft Dynamics AX 2012 en Microsoft Dynamics 365 voor bewerkingen 2012 R3 waren. Het voorbereiden van statistische metingen van de cube in de winkel entiteit, moet u doen gebruiken. Voor meer informatie raadpleegt u de procedure voor het klaarzetten van statistische metingen in de winkel entiteit in de [Power BI-integratie met entiteit winkel in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog-update. De volgende belangrijke statistische metingen kunnen rechtstreeks vanaf de factuur regels entiteit en worden gebruikt als basis voor de content pack.

| Entiteit        | Belangrijke statistische metingen | Gegevensbron voor Dynamics 365 for Operations | Veld              | Omschrijving                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Factuurregels | Inkoop                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Het bedrag in de valuta voor de boekhouding. |

De volgende tabel toont de belangrijkste afmetingen die zijn berekend in het inhoudspakket van de factuur regels entiteit.

| Maat               | Berekening                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Opdracht huidige jaar | Opdracht huidige jaar = som ('factuurregels\[opdracht\])                                            |
| Opdracht vorig jaar    | Opdracht vorig jaar = berekenen (som ('factuurregels\[opdracht\]), SAMEPERIODLASTYEAR (datums\[datum\])) |
| YOY inkoop groei   | YOY inkoop groei = \[opdracht huidige jaar\] : \[vorig jaar kopen\]                            |

De volgende belangrijke dimensies in de content pack worden gebruikt als filters opsplitsen van de statistische metingen, zodat u meer granulatie en meer analytische inzicht kunt bereiken.

| Entiteit                 | Voorbeelden van kenmerken                                |
|------------------------|-------------------------------------------------------|
| Leveranciers                   | Leveranciersgroepen, leveranciers-land of regio's, Leveranciersnaam |
| Producten               | Productnummer, productnaam, de naam van de groepen voor artikel        |
| Inkoopcategorieën | Aanschaffingscategorie, categorienamen aanschaffingscategorieën      |
| Rechtspersonen         | Rechtspersoonnaam                                     |
| Datums                  | Datums, jaar-verschuiving                                    |

Standaard worden gegevens in de content pack weergegeven voor het huidige kalenderjaar. U kunt echter het datumfilter in de rapportsectie filters wijzigen. U kunt ook de Bedrijfsfilter wijzigen.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](..\data-entities\data-entities.md)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](configure-power-bi-integration.md)



