---
title: Geavanceerde filter- en querysyntaxis
description: In dit onderwerp worden de filter- en queryopties voor het dialoogvenster Geavanceerd filteren/sorteren beschreven en vindt u uitleg over de operator voor overeenkomsten in het filtervenster of de filters in de rasterkolomkoppen.
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0fefac5a7a2b299ba606a854824ee456c572487
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070004"
---
# <a name="advanced-filtering-and-query-syntax"></a>Geavanceerde filter- en querysyntaxis

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

In dit onderwerp worden de filter- en queryopties beschreven die beschikbaar zijn wanneer u het dialoogvenster Geavanceerd filteren/sorteren of de operator **komt overeen** in het filtervenster of de filters in de rasterkolomkoppen gebruikt.

## <a name="advanced-query-syntax"></a>Geavanceerde querysyntaxis

<table>
<thead>
<tr>
<th>Syntaxis</th>
<th>Tekenomschrijving</th>
<th>Omschrijving</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>waarde</em></td>
<td>Gelijk aan de waarde die is ingevoerd</td>
<td>Typ de te zoeken waarde in.</td>
<td>Een zoekopdracht op <strong>Smit</strong> heeft &quot;Smit&quot; als resultaat.</td>
</tr>
<tr>
<td>!<em>waarde</em> (uitroepteken)</td>
<td>Niet gelijk aan de waarde die is ingevoerd</td>
<td>Typ een uitroepteken gevolgd door de uit te sluiten waarde.</td>
<td>Een zoekopdracht op<strong>!Smit</strong> heeft alle waarden met uitzondering van &quot;Smit&quot; als resultaat.</td>
</tr>
<tr>
<td><em>beginwaarde</em>..<em>eindwaarde</em> (twee puntjes)</td>
<td>Tussen de twee waarden die zijn gescheiden door twee puntjes</td>
<td>Typ de beginwaarde, vervolgens twee puntjes en daarna de eindwaarde.</td>
<td>Een zoekopdracht op <strong>1..10</strong> heeft alle waarden van 1 tot en met 10 als resultaat. In een tekenreeksveld wordt met een zoekopdracht <strong>A..C</strong> echter gezocht naar alle waarden die beginnen met &quot;A&quot; en &quot;B&quot; en waarden die identiek zijn aan &quot;C&quot;. Met deze query wordt &quot;Ca&quot; bijvoorbeeld niet gevonden. Als u alle waarden van &quot;A<em>&quot; tot en met &quot;C</em>&quot; wilt vinden, typt u <strong>A..D</strong>.</td>
</tr>
<tr>
<td>..<em>waarde</em> (twee puntjes)</td>
<td>Kleiner dan of gelijk aan de waarde die is ingevoerd</td>
<td>Typ twee puntjes en vervolgens de waarde.</td>
<td>Een zoekopdracht van <strong>..1000</strong> heeft alle getallen die kleiner zijn dan of gelijk zijn aan 1000 als resultaat, bijvoorbeeld &quot;100&quot;, &quot;999,95&quot; en &quot;1.000&quot;.</td>
</tr>
<tr>
<td><em>waarde</em>.. (twee puntjes)</td>
<td>Groter dan of gelijk aan de waarde die is ingevoerd</td>
<td>Typ de waarde en vervolgens twee puntjes.</td>
<td>Een zoekopdracht <strong>1000..</strong> heeft alle getallen die groter zijn dan of gelijk zijn aan 1000 als resultaat, bijvoorbeeld &quot;1000&quot;, &quot;1000,01&quot; en &quot;1.000.000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>waarde</em> (groter dan-teken)</td>
<td>Groter dan de waarde die is ingevoerd</td>
<td>Typ een groter dan-teken (<strong>&gt;</strong>) en vervolgens de waarde.</td>
<td>Een zoekopdracht <strong>&gt;1000</strong> heeft alle getallen die groter zijn dan 1000 als resultaat, bijvoorbeeld &quot;1000,01&quot;, &quot;20.000&quot; en  &quot;1.000.000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>waarde</em> (kleiner dan-teken)</td>
<td>Kleiner dan de waarde die is ingevoerd</td>
<td>Typ een kleiner dan-teken (<strong>&lt;</strong>) en vervolgens de waarde.</td>
<td>Een zoekopdracht <strong>&lt;1000</strong> heeft alle getallen die kleiner zijn dan 1000 als resultaat, bijvoorbeeld &quot;999,99&quot;, &quot;1&quot; en &quot;-200&quot;.</td>
</tr>
<tr>
<td><em>waarde</em>* (sterretje)</td>
<td>Beginnend vanaf de waarde die is ingevoerd</td>
<td>Typ de beginwaarde en vervolgens een sterretje (<strong>*</strong>).</td>
<td>De zoekopdracht <strong>S*</strong> heeft alle tekenreeksen die beginnen met een &quot;S&quot;, zoals &quot;Stockholm&quot;, &quot;Sydney&quot; en &quot;San Francisco&quot; als resultaat.</td>
</tr>
<tr>
<td>*<em>waarde</em> (sterretje)</td>
<td>Eindigend met de waarde die is ingevoerd</td>
<td>Typ een asterisk en vervolgens de eindwaarde.</td>
<td>De zoekopdracht <strong>*oost</strong> heeft alle tekenreeksen die eindigen op &quot;oost&quot; als resultaat, zoals &quot;Noordoost&quot; en &quot;Zuidoost&quot;.</td>
</tr>
<tr>
<td>*<em>waarde</em>* (sterretje)</td>
<td>Bevat de waarde die is ingevoerd</td>
<td>Typ een asterisk, vervolgens een waarde en nog een asterisk.</td>
<td>De zoekopdracht <strong>*do*</strong> heeft alle tekenreeksen die &quot;do&quot; bevatten als resultaat, zoals &quot;Noordoost&quot; en &quot;Zuidoost&quot;.</td>
</tr>
<tr>
<td>? (vraagteken)</td>
<td>Bevat een of meer onbekende tekens.</td>
<td>Type een vraagteken op de positie van het onbekende teken in de waarde.</td>
<td>De zoekopdracht <strong>Sm?t</strong> heeft &quot;Smit&quot; en &quot;Smet&quot; als resultaat.</td>
</tr>
<tr>
<td><em>waarde</em>,<em>waarde</em> (komma)</td>
<td>Overeenkomend met de waarden die zijn gescheiden door een komma</td>
<td>Typ alle zoekcriteria en scheid deze met behulp van komma's.</td>
<td><strong>A, D, F, G</strong> heeft &quot;A&quot;, &quot;D&quot;, &quot;F&quot; en &quot;G&quot; als resultaat. De zoekopdracht <strong>10, 20, 30, 100</strong> heeft exact &quot;10, 20, 30, 100&quot; als resultaat.</td>
</tr>
<tr>
<td>"" (twee dubbele aanhalingstekens)</td>
<td>Overeenkomend met een lege waarde</td>
<td>Typ twee opeenvolgende dubbele aanhalingstekens om te filteren op lege waarden in dat veld.</td>
<td>Met twee opeenvolgende dubbele aanhalingstekens (<strong>""</strong>) wordt gezocht naar rijen zonder waarde voor de huidige kolom.</td>
</tr>
<tr>
<td>(<span class="code">Finance and Operations-query</span>) (Finance and Operations-query tussen haakjes)</td>
<td>Overeenkomend met een opgegeven query.</td>
<td>Typ een query als een SQL-instructie tussen haakjes met de Finance and Operations-querytaal.</td>
  <td><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong><br><br> 
       Als een voorbeeld van een syntaxis voor een filtervoorwaarde op een veld uit de hoofdgegevensbron en een veld uit een andere gegevensbron (voor de pagina Alle klanten)</td>
</tr>
<tr>
<td>D</td>
<td>Datum van vandaag</td>
<td>Typ <strong>T</strong>.</td>
<td><strong>T</strong> stemt overeen met de datum van vandaag.</td>
</tr>
<tr>
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> methode tussen haakjes)</td>
<td>Overeenstemming van de waarde of het bereik van waarden die zijn opgegeven door de parameters van de methode <strong>SysQueryRangeUtil</strong></td>
<td>Typ een methode <strong>SysQueryRangeUtil</strong> die parameters heeft waarmee de waarde of het bereik van waarden wordt opgegeven.</td>
<td>
<ol>
<li>Klik op <strong>Klanten</strong> &gt; <strong>Facturen</strong> &gt; <strong>Openstaande klantfacturen</strong>.</li>
<li>Druk op Ctrl+Shift+F3 om de pagina <strong>Query</strong> te openen.</li>
<li>Klik op <strong>Toevoegen</strong> op het tabblad <strong>Bereik</strong>.</li>
<li>Selecteer <strong>Openstaande transacties</strong> in het veld <strong>Tabel</strong>.</li>
<li>Selecteer <strong>Vervaldatum</strong> in het veld <strong>Veld</strong>.</li>
<li>Voer <strong>(yearRange(-2,0))</strong> in het veld <strong>Criteria</strong> in.</li>
<li>Klik tot slot op <strong>OK</strong>. De lijstpagina wordt bijgewerkt en bevat een lijst met de facturen die voldoen aan de criteria die u hebt ingevoerd. Voor dit voorbeeld worden facturen weergegeven die in de voorgaande twee jaren zijn vervallen.</li>
</ol>
Raadpleeg de tabel in het volgende onderdeel voor meer informatie over datummethoden <strong>SysQueryRangeUtil</strong> en enkele voorbeelden.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Geavanceerde datumquery's die SysQueryRangeUtil-methoden gebruiken

<table>
<thead>
<tr>
<th>Methode</th>
<th>Beschrijving</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr>
<td>Day (_relativeDays=0)</td>
<td>Zoek een datum ten opzichte van de sessiedatum. Positieve waarden geven toekomstige datums aan en negatieve waarden geven datums in het verleden aan.</td>
<td>
<ul>
<li><strong>Morgen</strong> – Voer <strong>(Day(1))</strong> in.</li>
<li><strong>Vandaag</strong> – Voer <strong>(Day(0))</strong> in.</li>
<li><strong>Gisteren</strong> – Voer <strong>(Day(-1))</strong> in.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Zoek een bereik van datums ten opzichte van de sessiedatum. Positieve waarden geven toekomstige datums aan en negatieve waarden geven datums in het verleden aan.</td>
<td>
<ul>
<li><strong>Laatste 30 dagen</strong> – Voer <strong>(DayRange(-30,0))</strong> in.</li>
<li><strong>De vorige 30 dagen en komende 30 dagen</strong> – Voer <strong>(DayRange(-30,30))</strong> in.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Zoek alle datums na de opgegeven relatieve datum.</td>
<td>
<ul>
<li><strong>Meer dan 30 dagen vanaf nu</strong> – Voer <strong>(GreaterThanDate (30))</strong> in.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Zoek alle datum-/tijdvermeldingen na de huidige tijd.</td>
<td>
<ul>
<li><strong>Alle toekomstige datums/tijden</strong> – Voer <strong>(GreaterThanUtcNow())</strong> in.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Zoek alle datums vóór de opgegeven relatieve datum.</td>
<td>
<ul>
<li><strong>Minder dan zeven dagen vanaf nu</strong>– Voer <strong>(LessThanDate (7))</strong> in.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Zoek alle datum-/tijdvermeldingen vóór de huidige tijd.</td>
<td>
<ul>
<li><strong>Alle eerdere datums/tijden</strong> – Voer <strong>(LessThanUtcNow())</strong> in.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Zoek een datumbereik op basis van maanden gerelateerd aan de huidige maand.</td>
<td>
<ul>
<li><strong>Vorige twee maanden</strong> – Voer <strong>(MonthRange (- 2,0))</strong> in.</li>
<li><strong>Volgende drie maanden</strong> – Voer <strong>(MonthRange (0,3))</strong> in.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Zoek een datumbereik op basis van jaren gerelateerd aan het huidige jaar.</td>
<td>
<ul>
<li><strong>Volgend jaar</strong> – Voer <strong>(YearRange (0, 1))</strong> in.</li>
<li><strong>Vorig jaar</strong> – Voer <strong>(YearRange(-1,0))</strong> in.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]