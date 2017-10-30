---
title: Overheadberekening
description: In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a>Overheadberekening

[!include[banner](../includes/banner.md)]


In dit onderwerp worden de kenmerkende processen voor het berekenen en toewijzen van overheadkosten beschreven.

<a name="term-definition"></a>Definitie van term
---------------

Overheadkosten zijn de kosten die normaal verbonden zijn aan de bedrijfsvoering van een onderneming, maar die niet rechtstreeks aan bepaalde bedrijfsactiviteiten, producten of services kunnen worden toegeschreven. Overheadkosten bieden kritieke ondersteuning voor het genereren van winstgevende activiteiten. Hieronder staan enkele voorbeelden van overheadkosten:

-   Huur
-   Elektriciteit
-   Administratieve salarissen

## <a name="overhead-calculation-overview"></a>Overzicht van overheadberekening
Bij overheadberekening wordt het beleid voor kostprijsboekhouding in de juiste volgorde uitgevoerd. U kunt meerdere keren overheadkosten berekenen voor deze boekperiode als het beleid voor kostprijsboekhouding is gewijzigd of als specifieke fouten zijn gevonden. Elke uitvoering van de berekening van de overheadkosten wordt opgeslagen en ontvangt een unieke versie-id waarmee u de berekeningen in verschillende versies kunt vergelijken. De kostenposten die bij de berekening van de overhead worden gegenereerd ontvangen een boekingsdatum. Deze boekingsdatum komt overeen met de einddatum van de boekperiode die wordt gebruikt in de berekening. De unieke versie-id bestaat uit de volgende elementen:

-   Versietype
-   Datum en tijd
-   Grootboek van kostprijsboekhouding
-   Boekjaar
-   Boekperiode

De overheadberekening wordt onafhankelijk van de versie uitgevoerd. Daarom kunt u de budgetversie vóór de huidige versie berekenen. De berekening van de overheadkosten bestaat uit vier stappen, zoals in de volgende afbeelding wordt weergegeven. In elke stap wordt een journaalkop gemaakt met journaalposten. Deze journaalkop bevat de ingevoerde gegevens voor elke berekeningsstap. Er worden beleid en regels toegepast op elke journaalregel en er worden kostenposten gegenereerd als uitvoer. Daarom beschikt u altijd over volledige traceerbaarheid. 

[![Overheadberekening](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>De overheadkosten voor elektriciteit berekenen en toewijzen
In de financiële boekhouding worden sommige kosten, zoals elektriciteit, geregistreerd als een vast bedrag. Daarom worden geen managementinzichten verstrekt voor kostprijsboekhouding. Als u in de kostprijsboekhouding het juiste leidinggevende inzicht wilt bieden voor alle organisatie-eenheden en niveaus, moeten kosten door de organisatie-eenheden stromen. Deze stroom moet zijn gebaseerd op een nauwkeurig overzicht van het verbruik of op een reële beoordeling. In het grootboek kunnen kosten voor elektriciteit worden geboekt, zoals weergegeven in de volgende tabel.

<table>
<thead>
<tr>
<th>Grootboekdatum</th>
<th colspan="2">Kostenplaats</th>
<th colspan="2">Hoofdrekening</th>
<th>Bedrag in de boekhoudingsvaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>3 januari 2017</td>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>Stap 1: Het gedrag voor kostenberekening verwerken

Standaard worden kostenposten die worden geïmporteerd vanuit de brongegevens automatisch geclassificeerd met het kostengedrag **Ongeclassificeerd** in de kostprijsboekhouding. Door beleidsregels voor kostengedrag toe te passen, kunt u kostenposten opnieuw indelen als **Vaste kosten** of **Variabele kosten**.

#### <a name="define-the-cost-behavior-rule"></a>De regel voor kostengedrag definiëren

In sommige gevallen bestaat een gedeelte van de kosten uit een vast tarief en zijn de resterende kosten gebaseerd op het verbruik. Elektriciteitrekeningen voldoen vaak aan deze definitie. Nadat u een specifieke vast tarief hebt betaald, betaalt u voor het verbruik per kilowattuur (Kwh). Als bijvoorbeeld de vaste kosten € 1.000,00 bedragen, wordt als volgt de regel voor kostengedrag gedefinieerd:

-   Vast bedrag 1.000,00
    -   0 &lt;= 1.000,00 = Vast
    -   1.000,01 &lt; N = Variabel

##### <a name="journal"></a>Journaal

<table>
<thead>
<tr>
<th>Journaal</th>
<th>Type journaal</th>
<th colspan="3">Fiscale kalenderperiode</th>
<th>Versie</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Journaal van berekening kostengedrag</td>
<td>Fiscaal</td>
<td>2017</td>
<td>Periode 1</td>
<td>Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Journaalboekingen (journaalboekingen voor kostenobjectsaldo)

<table>
<thead>
<tr>
<th>Grootboekdatum</th>
<th colspan="2">Kostenobject</th>
<th colspan="2">Kostenelement</th>
<th>Kostengedrag</th>
<th>Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>3 januari 2017</td>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Ongeclassificeerd</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kosteninvoer

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th colspan="2">Kostenelement</th>
<th>Kostengedrag</th>
<th>Bedrag</th>
<th>Grootboekdatum</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Ongeclassificeerd</td>
<td>10.000,00</td>
<td>3 januari 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Ongeclassificeerd</td>
<td>-10,000.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>1.000,00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>9.000,00</td>
<td>31 januari 2017</td>
</tr>
</tbody>
</table>

Zie Kostengedragbeleid voor gedetailleerde informatie over kostengedrag. (Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)

### <a name="step-2-process-the-cost-distribution-calculation"></a>Stap 2: De berekening van kostenverdeling verwerken

Kostenverdeling wordt gebruikt om de kosten van een kostenobject te herverdelen over een of meer andere kostenobjecten door een relevante toewijzingsgrondslag toe te passen. Het verschil tussen kostenverdeling en kostentoewijzing is dat kostenverdeling altijd plaatsvindt op het niveau van het primaire kostenelement van de oorspronkelijke kosten.

#### <a name="define-the-cost-distribution-rule"></a>De regel voor kostenverdeling definiëren

In de financiële boekhouding worden elektriciteitskosten vaak geregistreerd als een vast bedrag. In de kostprijsboekhouding is deze benadering niet gedetailleerd genoeg. De variabele kosten moeten op een reële basis worden verdeeld over de afzonderlijke kostenobjecten. De meest logische toewijzingsgrondslag is het verbruik van elektriciteit (Kwh). Er wordt een statistisch dimensielid met de naam Elektriciteit gemaakt en het elektriciteitsverbruik wordt geregistreerd. Standaard komen alle statistische dimensieleden beschikbaar als toewijzinggrondslagen.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Kwh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1.000</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>6.000</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>0</td>
</tr>
</tbody>
</table>

De volgende tabel laat het resultaat zien van toepassing van het elektriciteitsverbruik als toewijzingsbasis voor variabele kosten.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Magnitude</th>
<th>Toewijzingsfactor</th>
<th>Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1.000</td>
<td>(1.000 ÷ 7.000) × 9.000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>6.000</td>
<td>(6.000 ÷ 7.000) × 9.000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>0</td>
<td>(0 ÷ 7.000) × 9.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

De vaste kosten moet gelijkmatig worden verdeeld over de afzonderlijke kostenobjecten die elektriciteit hebben verbruikt. U kunt dit resultaat bereiken door het statistische dimensielid Elektriciteit te gebruiken in een formuletoewijzingsgrondslag: (elektriciteit &gt; 0,00). De volgende tabel laat het resultaat zien wanneer het elektriciteitsverbruik wordt toegepast als een toewijzingsgrondslag voor variabele kosten.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Formule</th>
<th>Magnitude</th>
<th>Toewijzingsfactor</th>
<th>Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>(1.000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>(6.000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Journaal

<table>
<thead>
<tr>
<th>Journaal</th>
<th>Type journaal</th>
<th colspan="3">Fiscale kalenderperiode</th>
<th>Versie</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Berekeningsjournaal voor kostenverdeling</td>
<td>Fiscaal</td>
<td>2017</td>
<td>Periode 1</td>
<td>Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Journaalboekingen (journaalboekingen voor kostenobjectsaldo)

<table>
<thead>
<tr>
<th>Grootboekdatum</th>
<th colspan="2">Kostenobject</th>
<th colspan="2">Kostenelement</th>
<th>Kostengedrag</th>
<th>Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>31 januari 2017</td>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>1.000,00</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>9.000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kosteninvoer

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th colspan="2">Kostenelement</th>
<th>Kostengedrag</th>
<th>Bedrag</th>
<th>Grootboekdatum</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>-1.000,00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>500,00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>500,00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standaardkostenplaats</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>-9,000.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>1,285.71</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>7,714.29</td>
<td>31 januari 2017</td>
</tr>
</tbody>
</table>

Zie Kostenverdelingsbeleid en Toewijzigingsgrondslagen voor gedetailleerde informatie over kostenverdeling en toewijzingsgrondslagen. (Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)

### <a name="step-3-process-the-overhead-rate-calculation"></a>Stap 3: De berekening van overheadtarieven verwerken

Het overheadtarief wordt gebruikt om een of meer specifieke kostenobjecten te belasten. De toeslag is gebaseerd op een vooraf vastgesteld kostentarief en de magnitude van de toegewezen toewijzingsgrondslag. 

#### <a name="define-the-overhead-rate"></a>Het overheadtarief definiëren

Kostenobject CC001 HR draagt bij aan een reeks van interne projecten. Er wordt een statistisch dimensielid met de naam HR-projecten gemaakt om de verbruikte magnitude te meten.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Uren</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Project 1</td>
<td>3</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Project 2</td>
<td>1</td>
</tr>
</tbody>
</table>

Er is een vooraf vastgesteld kostentarief voor bijdrage aan de projectkosten gedefinieerd.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Kostenelement</th>
<th>Kostengedrag</th>
<th>Eenheden</th>
<th>Tarief</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Variabele kosten</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

De volgende tabel laat het resultaat zien wanneer de HR-projecten worden toegepast als toewijzingsgrondslag.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Magnitude</th>
<th>Kostenelement</th>
<th>Toewijzingsfactor</th>
<th>Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Project 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30,00</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Project 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Journaal

<table>
<thead>
<tr>
<th>Journaal</th>
<th>Type journaal</th>
<th colspan="3">Fiscale kalenderperiode</th>
<th>Versie</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Journaal voor berekening van overheadtarieven</td>
<td>Fiscaal</td>
<td>2017</td>
<td>Periode 1</td>
<td>Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Journaalboekingen (Journaalboekingen voor berekening van overheadtarieven)

<table>
<thead>
<tr>
<th>Grootboekdatum</th>
<th colspan="2">Kostenobject</th>
<th>Magnitude</th>
</tr>
</thead>
<tbody>
<tr>
<td>31 januari 2017</td>
<td>Proj 1</td>
<td>intern proj 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>Proj 2</td>
<td>intern proj 2</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kosteninvoer

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th colspan="2">Kostenelement</th>
<th>Kostengedrag</th>
<th>Bedrag</th>
<th>Grootboekdatum</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>HR</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>-30.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Proj 1</td>
<td>intern proj 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>30,00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>-10.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Proj 2</td>
<td>intern proj 2</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>10,00</td>
<td>31 januari 2017</td>
</tr>
</tbody>
</table>

Zie Beleid voor overheadtarief en Toewijzingsgrondslagen voor gedetailleerde informatie over beleid voor overheadtarieven. (Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)

### <a name="step-4-process-the-cost-allocation-calculation"></a>Stap 4: De berekening van kostentoewijzing verwerken

Toewijzing wordt gebruikt om het saldo van een kostenobject toe te wijzen aan andere kostenobjecten door een toewijzingsgrondslag toe te passen. Finance and Operations ondersteunt de wederzijdse toewijzingsmethode. Bij de wederzijdse toewijzingsmethode worden de onderlinge services die bijkomende kostenobjecten uitwisselen volledig erkend. Het systeem bepaalt automatisch de juiste volgorde voor het uitvoeren van de toewijzingen. Het saldo van een kostenobject wordt toegewezen door een enkele toewijzingsgrondslag. Toewijzingen over dimensies voor kostenobjecten en hun respectievelijke leden heen worden ondersteund. De toewijzingsvolgorde wordt bepaald door de kostenbeheereenheid. 

[![Wederzijdse methode](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>De kostentoewijzing definiëren

Hier volgt een eenvoudig voorbeeld waarin wordt uitgelegd hoe u de stroom van kosten kunt traceren. Kostenobject CC001 HR draagt bij aan verschillende kostenobjecten. Er wordt een statistisch dimensielid met de naam HR-services gemaakt om de verbruikte magnitude te meten.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>HR-services</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>10</td>
</tr>
</tbody>
</table>

Kostenobject CC002 Financiën draagt bij aan verschillende kostenobjecten. Er wordt een statistisch dimensielid met de naam Financiële services gemaakt om de verbruikte magnitude te meten.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Financiële services</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>35</td>
</tr>
</tbody>
</table>

Kostenobject CC003 Assemblage draagt bij aan verschillende kostenobjecten. Er wordt een statistisch dimensielid met de naam Assemblageservices gemaakt om de verbruikte magnitude te meten.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Assemblageservices (uren)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>60</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Kostenobject CC004 Verpakking draagt bij aan verschillende kostenobjecten. Er wordt een statistisch dimensielid met de naam Verpakkingsservices gemaakt om de verbruikte magnitude te meten.

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Verpakkingsservices (uren)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>80</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>15</td>
</tr>
</tbody>
</table>

**Opmerking:** In Finance and Operations kunnen statistische metingen, zoals de productie-uren die een product verbruikt, worden afgeleid uit brongegevens. Zie Sjablonen van provider van statistische maateenheden voor gedetailleerdere informatie over statistische providers van statistische maateenheden. (Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.) In de volgende tabel ziet u het resultaat wanneer de HR-services worden toegepast als toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Magnitude</th>
<th>Toewijzingsfactor</th>
<th>Bedrag</th>
<th>Kostengedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>35</td>
<td>(35 ÷ 100) × 1.245,71</td>
<td>436.00</td>
<td>Variabele kosten</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>55</td>
<td>(55 ÷ 100) × 1.245,71</td>
<td>685.14</td>
<td>Variabele kosten</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>10</td>
<td>(10 ÷ 100) × 1.245,71</td>
<td>124.57</td>
<td>Variabele kosten</td>
</tr>
</tbody>
</table>

In de volgende tabel ziet u het resultaat wanneer de financiële services worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Magnitude</th>
<th>Toewijzingsfactor</th>
<th>Bedrag</th>
<th>Kostengedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>65</td>
<td>(65 ÷ 100) × (7.714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Variabele kosten</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>35</td>
<td>(35 ÷ 100) × (7.714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Variabele kosten</td>
</tr>
</tbody>
</table>

In de volgende tabel ziet u het resultaat wanneer de assemblageservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Magnitude</th>
<th>Toewijzingsfactor</th>
<th>Bedrag</th>
<th>Kostengedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5.297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Variabele kosten</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5.297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Variabele kosten</td>
</tr>
</tbody>
</table>

In de volgende tabel ziet u het resultaat wanneer de verpakkingsservices worden toegepast als een toewijzingsgrondslag voor de totale kosten (vaste kosten en variabele kosten).

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th>Magnitude</th>
<th>Toewijzingsfactor</th>
<th>Bedrag</th>
<th>Kostengedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Vaste kosten</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2.852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Variabele kosten</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2.852,60 + 124,57)</td>
<td>470.08</td>
<td>Variabele kosten</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Journaalboekingen (journaalboekingen voor kostenobjectsaldo)

<table>
<thead>
<tr>
<th>Journaal</th>
<th>Type journaal</th>
<th colspan="3">Fiscale kalenderperiode</th>
<th>Versie</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Kostentoewijzingsjournaal</td>
<td>Fiscaal</td>
<td>2017</td>
<td>Periode 1</td>
<td>Berekening overheadkosten / 01-02-2017 23:51:00 uur / Grootboek /2017 / Periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Journaalregels

<table>
<thead>
<tr>
<th>Grootboekdatum</th>
<th colspan="2">Kostenobject</th>
<th colspan="2">Kostenelement</th>
<th>Kostengedrag</th>
<th>Bedrag</th>
</tr>
</thead>
<tbody>
<tr>
<td>31 januari 2017</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>500,00</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>CC002</td>
<td>Financiën</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>675.00</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>CC002</td>
<td>Financiën</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>713.75</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>CC003</td>
<td>Verpakking</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>286.25</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>CC003</td>
<td>Verpakking</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>Prod 1</td>
<td>Product 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>776.36</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>Prod 1</td>
<td>Product 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>Prod 2</td>
<td>Product 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>223.64</td>
</tr>
<tr>
<td>31 januari 2017</td>
<td>Prod 2</td>
<td>Product 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kosteninvoer

<table>
<thead>
<tr>
<th colspan="2">Kostenobject</th>
<th colspan="2">Kostenelement</th>
<th>Kostengedrag</th>
<th>Bedrag</th>
<th>Grootboekdatum</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>-500.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>175.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>275.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>50,00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>-1,245.71</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>436.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>685.14</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>124.57</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>-675.00</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>438.75</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>236.25</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Financiën</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>-8,150.29</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>5,297.69</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Verpakking</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>2,852.60</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>-713.75</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>535.31</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>178.44</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>-5,982.83</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>4,487.12</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>1,495.71</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>-286.25</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>241.05</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Vaste kosten</td>
<td>45.20</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembleren</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>-2,977.17</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Product 1</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>2,507.09</td>
<td>31 januari 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Product 2</td>
<td>10001</td>
<td>Elektriciteit</td>
<td>Variabele kosten</td>
<td>470.08</td>
<td>31 januari 2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Conclusie
In het financiële boekhouding worden kosten van 10.000,00 voor elektriciteit geboekt naar een dummy kostenplaats-id. Hierdoor weten kostenaccountants dat deze kosten moeten worden toegewezen. In de kostprijsboekhouding stromen de kosten door de organisatie-eenheden en niveaus, op basis van het beleid en de regels die worden toegepast. Elke kostenpost is gekoppeld aan een toewijzingsgrondslag die de beste beoordeling biedt voor de toewijzing van kosten.

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">Kostenelement</th>
<th colspan="9">Kostenobject</th>
<th rowspan="2">Totaal</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>Proj 1</th>
<th>Proj 2</th>
<th>Prod 1</th>
<th>Prod 2</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 Elektriciteit</td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30.00</strong></td>
<td style="text-align: right;"><strong>10.00</strong></td>
<td style="text-align: right;"><strong>7,770.57</strong></td>
<td style="text-align: right;"><strong>2,189.43</strong></td>
<td style="text-align: right;"><strong>10,000.00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">Ongeclassificeerd</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Vaste kosten</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1,000.00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Variabele kosten</td>
<td style="text-align: right;">000</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">30,00</td>
<td style="text-align: right;">10,00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9,000.00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Dit onderwerp laat zien beschreven hoe een primair kostenelement, 10001 Elektriciciteit, door de kostenobjecten stroomt. Daarom worden deze overheadkosten toegewezen aan het laagste niveau in de organisatie. Met andere woorden, de kostenobjecten op het laagste niveau dragen de kosten. Als u een visuele stroom van de kosten tussen de kostenobjecten nodig hebt, kunt u de beleidsregels voor kostenaggregatie gebruiken om de stroom van de kosten zichtbaar te maken. Zie Beleid voor kostenaggregatie voor meer gedetailleerde informatie. (Let op: dit onderwerp is nog niet voltooid, maar komt binnenkort beschikbaar.)




