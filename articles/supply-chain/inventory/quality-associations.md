---
title: Kwaliteitskoppelingen
description: In dit artikel wordt beschreven hoe u kwaliteitskoppelingen in Microsoft Dynamics 365 Supply Chain Management kunt gebruiken om automatisch kwaliteitsorders te genereren die zijn gerelateerd aan uw verkoop-, inkoop- en productieprocessen.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e96f301d8dec255e57f0f0fbfa9c8e1a5922ae9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887510"
---
# <a name="quality-associations"></a>Kwaliteitskoppelingen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u kwaliteitskoppelingen in Microsoft Dynamics 365 Supply Chain Management kunt gebruiken om automatisch kwaliteitsorders te genereren die zijn gerelateerd aan uw verkoop-, inkoop- en productieprocessen.

Met een kwaliteitskoppeling worden de volgende gegevens gedefinieerd voor een gegenereerde kwaliteitsorder:

- De transactiegebeurtenis
- De tests die op de artikelen moeten worden uitgevoerd
- Het acceptabele kwaliteitsniveau
- Het bemonsteringsplan

U moet een kwaliteitskoppeling opgeven voor elke afwijking in een bedrijfsproces waarvoor automatisch kwaliteitsorders moeten worden gegenereerd. Er kan bijvoorbeeld een kwaliteitsorder worden gegenereerd in de bedrijfsprocessen voor inkooporders, quarantaineorders, verkooporders en productieorders.

## <a name="working-with-quality-associations"></a>Werken met kwaliteitskoppelingen

Bedrijfsprocessen die gebruikmaken van een kwaliteitskoppeling, kunnen betrekking hebben op verschillende brondocumenten, zoals inkooporders, verkooporders of productieorders.

Elk kwaliteitskoppelingsrecord definieert de set met testen, het aanvaardbare kwaliteitsniveau en het bemonsteringsplan dat van toepassing is op de gegenereerde kwaliteitsorders. U moet een kwaliteitskoppelingsrecord definiëren voor elke variatie in een bedrijfsproces. U kunt bijvoorbeeld een kwaliteitskoppeling opzetten die een kwaliteitsorder genereert wanneer een productontvangstbon voor een inkooporder wordt bijgewerkt. Afhankelijk van de instellingen van het uitvoeringsplan, kan het activeringsproces zelf worden geblokkeerd terwijl er een openstaande kwaliteitsorder is. De daaropvolgende processen, zoals het factureren van inkooporders, kunnen ook worden geblokkeerd.

> [!NOTE]
> Wanneer er kwaliteitsorders openstaan, wordt de uitgave van voorraadhoeveelheden automatisch geblokkeerd. Afhankelijk van de instelling in het veld **Volledig blokkeren** op de pagina **Artikelbemonsteringen**, is de hoeveelheid de hoeveelheid op de kwaliteitsorder of op de brondocumentregel. Zie [Artikelbemonstering voor kwaliteitsbeheer](quality-item-sampling.md) voor meer informatie.

De kwaliteitskoppeling identificeert voor een opgegeven bedrijfsproces de gebeurtenis en de omstandigheden waarin een kwaliteitsorder wordt gegenereerd. De voorwaarden kunnen specifiek voor een site of een rechtspersoon zijn. Een kwaliteitsorder waarvoor destructieve testen worden uitgevoerd, kan alleen worden gegenereerd als er voorraad voor de gebeurtenis voorhanden is.

Als u met kwaliteitskoppelingen wilt werken, gaat u naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Kwaliteitskoppelingen**. In de volgende voorbeelden ziet u hoe een kwaliteitskoppelingsrecord wordt gedefinieerd voor de verschillen in elk bedrijfsproces. Voor elk voorbeeld worden in de volgende tabel de gebeurtenissen en voorwaarden samengevat die door een kwaliteitskoppelingsrecord zijn gedefinieerd.

<table>
<thead>
<tr>
<th>Verwijzingstype</th>
<th>Gebeurtenistype</th>
<th>Uitvoering</th>
<th>Gebeurtenisblokkering</th>
<th>Documentverwijzing</th>
</tr>
</thead>
<tbody>
<tr>
<td>Voorraad</td>
<td>Niet van toepassing</td>
<td>Niet van toepassing</td>
<td>Geen</td>
<td>Alle</td>
</tr>
<tr>
<td rowspan="7">Verkoop</td>
<td rowspan="4">Verzamelproces is gepland</td>
<td rowspan="4">Vóór</td>
<td>Geen</td>
<td rowspan="22">Specifieke id, Groep of alleen Alle</td>
</tr>
<tr>
<td>Verzamelproces</td>
</tr>
<tr>
<td>Pakbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="3">Pakbon</td>
<td rowspan="3">Vóór</td>
<td>Geen</td>
</tr>
<tr>
<td>Pakbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="15">Inkoop</td>
<td rowspan="7">Ontvangstlijst</td>
<td rowspan="4">Vóór</td>
<td>Geen</td>
</tr>
<tr>
<td>Ontvangstlijst</td>
</tr>
<tr>
<td>Productontvangstbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="3">Na</td>
<td>Geen</td>
</tr>
<tr>
<td>Productontvangstbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="3">Registratie</td>
<td rowspan="3">Niet van toepassing</td>
<td>Geen</td>
</tr>
<tr>
<td>Productontvangstbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="5">Productontvangstbon</td>
<td rowspan="3">Vóór</td>
<td>Geen</td>
</tr>
<tr>
<td>Productontvangstbon</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="2">Na</td>
<td>Geen</td>
</tr>
<tr>
<td>Factuur</td>
</tr>
<tr>
<td rowspan="8">Productie</td>
<td rowspan="3">Registratie</td>
<td rowspan="3">Niet van toepassing</td>
<td>Geen</td>
<td rowspan="12">Alle</td>
</tr>
<tr>
<td>Rapporteren als gereed</td>
</tr>
<tr>
<td>Beëindigen</td>
</tr>
<tr>
<td rowspan="5">Rapporteren als gereed</td>
<td rowspan="3">Vóór</td>
<td>Geen</td>
</tr>
<tr>
<td>Rapporteren als gereed</td>
</tr>
<tr>
<td>Beëindigen</td>
</tr>
<tr>
<td rowspan="2">Na</td>
<td>Geen</td>
</tr>
<tr>
<td>Beëindigen</td>
</tr>
<tr>
<td rowspan="4">Quarantaine</td>
<td rowspan="3">Rapporteren als gereed</td>
<td rowspan="2">Vóór</td>
<td>Rapporteren als gereed</td>
</tr>
<tr>
<td>Beëindigen</td>
</tr>
<tr>
<td>Na</td>
<td>Beëindigen</td>
</tr>
<tr>
<td>Beëindigen</td>
<td>Vóór</td>
<td>Beëindigen</td>
</tr>
<tr>
<td rowspan="3">Routebewerking</td>
<td rowspan="3">Rapporteren als gereed</td>
<td rowspan="2">Vóór</td>
<td>None</td>
<td rowspan="3">Specifieke id, Groep of Alle en specifieke Resources, Groep of Alle</td>
</tr>
<tr>
<td>Rapporteren als gereed</td>
</tr>
<tr>
<td>Na</td>
<td>None</td>
</tr>
<tr>
<td rowspan="3">Productie van coproducten</td>
<td>Registratie</td>
<td>Niet van toepassing</td>
<td rowspan="3">None</td>
<td rowspan="3">Alles</td>
</tr>
<tr>
<td rowspan="2">Rapporteren als gereed</td>
<td>Vóór</td>
</tr>
<tr>
<td>Na</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Met de functie *Kwaliteitsbeheer voor magazijnprocessen* voegt u mogelijkheden toe voor het verwerken van kwaliteitsorders voor productie waarvoor het veld **Gebeurtenistype** is ingesteld op *Gereedgemeld* en het veld **Uitvoering** op *Na* en voor inkopen waarvoor het **Gebeurtenistype** is ingesteld op *Registratie*. Zie [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md) voor meer informatie.

De volgende tabel bevat meer informatie over de manier waarop kwaliteitsorders kunnen worden gegenereerd voor specifieke typen processen.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Procestypen</th>
<th>Wanneer automatisch kwaliteitsorders kunnen worden gegenereerd</th>
<th>Wanneer kwaliteitsorders kunnen worden gegenereerd als destructieve testen vereist zijn</th>
<th>Informatie over voorwaarden</th>
<th>Handmatig informatie genereren</th>
</tr>
</thead>
<tbody>
<tr>
<td>Inkooporder</td>
<td>Vóór of nadat een ontvangstlijst of productontvangstbon voor het ontvangen materiaal wordt geboekt</td>
<td>Nadat de productontvangstbon voor het ontvangen materiaal is geboekt, aangezien het materiaal beschikbaar dient te zijn voor destructieve testen</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde leverancier of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een inkooporder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Quarantaineorder</td>
<td>Vóór of nadat de quarantaineorder is gerapporteerd als voltooid of beëindigd</td>
<td>Kwaliteitsorders waarvoor destructieve tests vereist zijn, kunnen niet worden gegenereerd. Er wordt verondersteld dat de functie voor quarantaineorders de rangschikking afhandelt van het materiaal dat wordt vernietigd.</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde leverancier of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een quarantaineorder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Verkooporder</td>
<td>Vóór een gepland orderverzamelproces of pakbonupdate voor de artikelen die worden verzonden</td>
<td>Bij elke stap</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde klant of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een verkooporder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Productieorder</td>
<td>Vóór of nadat de voltooide hoeveelheid voor de productieorder wordt gerapporteerd</td>
<td>Nadat de voltooide hoeveelheid voor de productieorder wordt gerapporteerd</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een productieorder verwijst, kan gebruik maken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Productieorder met een routebewerking</td>
<td>Voor of nadat het rapport voor een bewerking wordt voltooid</td>
<td>Nadat de rapportageproductie voor de laatste bewerking wordt voltooid</td>
<td>De vereiste voor een kwaliteitsorder kan betrekking hebben op een bepaalde site, een bepaald artikel, een bepaalde bron voor bedrijfsactiviteiten of een combinatie van deze voorwaarden.</td>
<td>Een handmatig gegenereerde kwaliteitsorder die naar een routebewerking verwijst, kan gebruikmaken van informatie in een kwaliteitskoppelingsrecord, zoals het testbemonsteringsplan.</td>
</tr>
<tr>
<td>Voorraad</td>
<td>Er kan niet automatisch een kwaliteitsorder worden gegenereerd voor een transactie in een voorraadjournaal of voor transacties met transferorders.</td>
<td></td>
<td></td>
<td>Een kwaliteitsorder moet handmatig worden gemaakt voor de voorraadhoeveelheid van een artikel. Fysieke voorhanden voorraad is vereist.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Voorbeelden van het automatisch genereren van kwaliteitsorders

### <a name="purchasing"></a>Inkopen

Als u in de inkoop het veld **Gebeurtenistype** instelt op *Productontvangstbon* en het veld **Uitvoering** op *Na* op de pagina **Kwaliteitskoppelingen**, krijgt u de volgende resultaten:

- Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op *Ja*, wordt voor elke ontvangst een kwaliteitsorder gegenereerd voor de inkooporder, op basis van de ontvangen hoeveelheid en instellingen in de artikelbemonstering. Telkens wanneer een hoeveelheid wordt ontvangen op basis van de inkooporder, worden nieuwe kwaliteitsorders gegenereerd op basis van de nieuw ontvangen hoeveelheid.
- Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op *Nee*, wordt voor de eerste ontvangst een kwaliteitsorder gegenereerd voor de inkooporder, op basis van de ontvangen hoeveelheid. Daarnaast worden een of meer kwaliteitsorders gemaakt op basis van de resterende hoeveelheid, afhankelijk van de traceringsdimensies. Er worden geen kwaliteitsorders gegenereerd voor volgende ontvangsten op de inkooporder.

### <a name="production"></a>Productie

Als u in de productie het veld **Gebeurtenistype** instelt op *Rapporteren als gereed* en het veld **Uitvoering** op *Na* op de pagina **Kwaliteitskoppelingen**, krijgt u de volgende resultaten:

- Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op *Ja*, wordt een kwaliteitsorder gegenereerd op basis van elke gereedgemelde hoeveelheid en instellingen in de artikelbemonstering. Telkens wanneer een hoeveelheid wordt gereedgemeld op basis van de productieorder, worden er nieuwe kwaliteitsorders gegenereerd op basis van de zojuist gereedgemelde hoeveelheid. Deze generatielogica is consistent met inkoop.
- Als de optie **Per bijgewerkte hoeveelheid** is ingesteld op *Nee*, wordt voor de eerste gereedgemelde hoeveelheid een kwaliteitsorder gegenereerd op basis van de gereedgemelde hoeveelheid. Daarnaast worden een of meer kwaliteitsorders gemaakt op basis van de resterende hoeveelheid, afhankelijk van de traceringsdimensies van de artikelbemonstering. Er worden geen kwaliteitsorders gegenereerd voor daaropvolgende gereedgemelde hoeveelheden.

<table>
<thead>
<tr>
<th>Specificatie van kwaliteit</th>
<th>Per bijgewerkte hoeveelheid</th>
<th>Per traceringsdimensie</th>
<th>Resultaat</th>
</tr>
</thead>
<tbody>
<tr>
<td>Percentage: 10%</td>
<td>Ja</td>
<td>
<p>Batchnummer: Nee</p>
<p>Serienummer: Nee</p>
</td>
<td>
<p>Orderhoeveelheid: 100</p>
<ol>
<li>Gereedmelden voor 30
<ul>
<li>Kwaliteitsorder 1 voor 3 (10% van 30)</li>
</ul>
</li>
<li>Gereedmelden voor 70
<ul>
<li>Kwaliteitsorder 2 voor 7 (10% van de resterende orderhoeveelheid, in dit geval 70)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Vaste hoeveelheid: 1</td>
<td>Nee</td>
<td>
<p>Batchnummer: Nee</p>
<p>Serienummer: Nee</p>
</td>
<td>Orderhoeveelheid: 100
<ol>
<li>Gereedmelden voor 30
<ul>
<li>Kwaliteitsorder 1 voor 1 (voor de eerste gereedgemelde hoeveelheid met de vaste waarde 1)</li>
<li>Kwaliteitsorder 2 voor 1 (voor de resterende hoeveelheid, die nog steeds de vaste waarde 1 heeft)</li>
</ul>
</li>
<li>Gereedmelden voor 10
<ul>
<li>Er worden geen kwaliteitsorders gemaakt.</li>
</ul>
</li>
<li>Gereedmelden voor 60
<ul>
<li>Er worden geen kwaliteitsorders gemaakt.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Vaste hoeveelheid: 1</td>
<td>Ja</td>
<td>
<p>Batchnummer: Ja</p>
<p>Serienummer: Ja</p>
</td>
<td>
<p>Orderhoeveelheid: 10</p>
<ol>
<li>Gereedmelden voor 3: 1 voor batchnummer b1, serienummer s1; 1 voor batchnummer b2, serienummer s2 en 1 voor batchnummer b3, serienummer s3
<ul>
<li>Kwaliteitsorder 1 voor 1 van batchnummer b1, serienummer s1</li>
<li>Kwaliteitsorder 2 voor 1 van batchnummer b2, serienummer s2</li>
<li>Kwaliteitsorder 3 voor 1 van batchnummer b3, serienummer s3</li>
</ul>
</li>
<li>Gereedmelden voor 2: 1 voor batchnummer b4, serienummer s4; en 1 voor batchnummer b5, serienummer s5
<ul>
<li>Kwaliteitsorder 4 voor 1 van batchnummer b4, serienummer s4</li>
<li>Kwaliteitsorder 5 voor 1 van batchnummer b5, serienummer s5</li>
</ul>
</li>
</ol>
<p><strong>Opmerking:</strong> de batch kan opnieuw worden gebruikt.</p>
</td>
</tr>
<tr>
<td>Vaste hoeveelheid: 2</td>
<td>Nee</td>
<td>
<p>Batchnummer: Ja</p>
<p>Serienummer: Ja</p>
</td>
<td>
<p>Orderhoeveelheid: 10</p>
<ol>
<li>Gereedmelden voor 4: 1 voor batchnummer b1, serienummer s1; 1 voor batchnummer b2, serienummer s2 en 1 voor batchnummer b3, serienummer s3; en 1 voor batchnummer b4, serienummer s4
<ul>
<li>Kwaliteitsorder 1 voor 1 van batchnummer b1, serienummer s1</li>
<li>Kwaliteitsorder 2 voor 1 van batchnummer b2, serienummer s2</li>
<li>Kwaliteitsorder 3 voor 1 van batchnummer b3, serienummer s3</li>
<li>Kwaliteitsorder 4 voor 1 van batchnummer b4, serienummer s4</li>
</ul>
<ul>
<li>Kwaliteitsorder 5 voor 2 zonder verwijzing naar een batch- en serienummer</li>
</ul>
</li>
<li>Gereedmelden voor 6: 1 voor batchnummer b5, serienummer s5; 1 voor batchnummer b6, serienummer s6; 1 voor batchnummer b7, serienummer s7; 1 voor batchnummer b8, serienummer s8; 1 voor batchnummer b9, serienummer s9; en 1 voor batchnummer b10, serienummer s10
<ul>
<li>Er worden geen kwaliteitsorders gemaakt.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Aanvullende bronnen

- [Processen voor kwaliteitsbeheer](quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
